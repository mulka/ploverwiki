These are my observations on the format of Eclipse .dix files, from dissecting a few specimens. The shortest two of these specimens, "oneentry" and "severalentries", are provided at the end of this page.

At a minimum, a .dix file must contain three things: a record structure, the steno strokes, and the English text. It may also contain a header and so on; Eclipse keeps track of a lot of other information.

# Header

## Magic number

In all cases the magic number, at the start of the file, is these sixteen bytes:

    000000 45 63 6c 20 34 2e 30 20 64 69 63 74 2e 0d 0a 1a

which spells "Ecl 4.0 dict." + CR LF ^Z

The CR/LF pair shows this is a DOS-based format. Similarly the ^Z is an MS-DOS convention: if the user attempts to show the file using the "type" command, the display will stop at that character.

## The word at 0x10

I've been working on the assumption that there's no header other than the magic number, because last year Mirabai posted a .dix file with zero entries containing only the magic number. However, that may have been corrupted.

If there wasn't a header, the first record would begin at 0x10. None of my ideas about the beginning of a record look like the word at 0x10.

However, the value of the 4-byte big-endian word at 0x10 increases as the size of the file increases:

* 0xbf (decimal 191) for oneentry
* 0x56d (decimal 1389) for severalentries
* 0x27245 for candeo
* 0xf13d1 for stephen
* 0xb541d1 for MKK

What can it be? It's not a line count. It isn't a pointer into the file-- even in severalentries it would point beyond the end. Perhaps it's an edit count, for deciding which version of a dictionary is newer?

# A record structure

This ought to be the simplest part to find, and yet it's still opaque.

oneentry is 188 bytes long. If there's no header beyond the magic number, we have the single record being 172 bytes long. This is improbable, and argues for the existence of a header.

If the records are stored straight, as in the RTF, then oneentry contains 1 entry and severalentries contains 15 entries.

However, perhaps the records are stored as a tree for fast searching. If we have one node for every stroke, with branching according to the next stroke, then oneentry contains 4 entries and severalentries contains 22.

If so, each record would have to have:
 - optional text which would be printed here
 - a list of following nodes, each with an offset
 - and a list terminator.

It's also possible that the nodes branch only when there's multiple options. In that case, oneentry contains 1 entry and severalentries contains 17 entries.

None of these hypotheses match observed behaviour in the file.

## The 0000ff structure

A glance at any .dix other than oneentry shows several occurrences of "0000ff..." or similar. They look like record separators, which would explain why they're not in oneentry. But if we take these to be record separators, we generally end up with about a quarter of the number of records we'd need.

The byte after "0000ff..." appears to be a bitmask. It's drawn from a restricted set. These are the values in MKK.dix, and their counts:

      4051 02
       631 0a
     10397 22
       440 2a
      2105 32
      8072 42
       406 4a
       233 52
       434 72
      5614 82
         1 84
        20 8a
      2663 a2
        63 aa
       538 b2
      9901 c2
       462 ca
         1 d1
        99 d2
       270 f2

So the second nibble is almost always 2 (0010) or a (1010), with 2 being far more likely. The two singleton outliers have 1 (0001) and 4 (1000). But let's ignore those for now. (The rest of their values may well be interesting.)

The most common values for the first nibble are: 0 (0000), 2 (0010), 4 (0100), 8 (1000), a (1010), c (1100). Oddly 6 (0110) and e (1110) are missing; this seems to show that the middle bits can't both be set.

## Steno strokes

Bear in mind that Eclipse supports palantype etc, so the format would need to be flexible.

Both oneentry and severalentries begin with a steno stroke containing only one key. (Assuming, for severalentries, that the entries are in the same order as the RTF.) There's no obvious place in the file where this happens.

## The English text 

The English text must be encoded in there somewhere. That should be far more predictable than the steno.

There's no visible ASCII-encoded text in the file.

Possibly it's using some kind of compression system? Anything involving sliding trees etc would be overkill for such short phrases, and would be rather difficult to update without rewriting the entire file.

Maybe it uses fewer bits than 8 for each character. Encoding of capital letters might involve shift characters, and so on, so I looked for the text "ritish" given 5, 6, or 7 bits for a character, and given "a"=0 up to the maximum possible. I found nothing.

# Specimen files
Thanks to Mirabai for providing these. You can find the files at http://chiark.greenend.org.uk/~tthurman/plover/dix/ .

## oneentry.dix

    000000 45 63 6c 20 34 2e 30 20 64 69 63 74 2e 0d 0a 1a
    000010 bf 00 00 00 78 da 4d 8d 5d 0b 82 30 18 85 ff ca
    000020 cb 7b 5f 9a a9 4c d8 26 59 46 17 7d 21 8e ae 4d
    000030 57 0e 6c c6 36 c2 fe 7d f3 ae 8b 03 87 f3 70 ce
    000040 a1 f9 f4 1a e0 23 8d 55 a3 66 b8 5a 86 08 52 b7
    000050 63 a7 f4 93 a1 a8 f7 0b 82 60 5d a3 bb 66 18 b5
    000060 64 a8 47 84 9c d3 b2 1d d4 db ca 9d 9a 38 95 b0
    000070 f5 cd 38 4d 48 1c a6 24 42 38 31 f4 33 c2 87 51
    000080 46 92 2c 49 c9 1a e1 cc d0 a3 c7 8c 38 b5 7c 51
    000090 c3 f5 56 95 a2 86 52 54 05 1c aa cd 65 36 34 b0
    0000a0 9c 3a ee 7a 09 85 51 4e d9 1e 8e ea 6e 1a f3 a5
    0000b0 81 e3 34 90 5e 7f df 3f b2 bb 37 68

Which contains one entry:

    {\*\cxs -T/PWREUT/EURB/HRAOEURB}the British Library

## severalentries.dix

    000000 45 63 6c 20 34 2e 30 20 64 69 63 74 2e 0d 0a 1a
    000010 6d 05 00 00 78 da 6c cd 5f 0f c1 30 14 87 e1 af
    000020 72 72 ee 59 f7 47 3b 49 5b 11 c6 85 30 d9 34 ae
    000030 c5 4a 96 4c 2b 3a 6c df de cc 8d 88 bb f3 5e 9c
    000040 e7 c7 27 cd a5 82 87 be b9 d2 1a 81 fe 90 20 68
    000050 73 b4 45 69 ce 02 d5 6e 31 88 11 5c 7d 30 c5 a1
    000060 b2 46 0b 34 16 61 22 79 72 ac ca ab d3 f3 b2 91
    000070 5c c3 ac fb 8c e8 28 8e 08 0b 19 c2 ba cb c0 ef
    000080 ce 31 65 5d aa 77 52 46 03 1a 92 08 61 23 30 40
    000090 38 09 24 28 b9 93 0a 76 ab 2c 55 39 ac f6 59 a2
    0000a0 b8 e7 24 af 65 6b ef 50 dc ec d3 b5 dc ab 25 f7
    0000b0 f4 ff 15 f2 c1 c3 98 c4 e3 51 c0 48 8f fb bf fa
    0000c0 76 3f 4d 13 b5 cc bf ec f3 bd 75 bd fc 02 00 00
    0000d0 ff ff c2 34 d9 02 9b fb 21 26 1b a0 18 1c 1c 1a
    0000e0 14 00 35 b2 b4 b8 b4 a8 00 af 79 30 97 9a 58 1a
    0000f0 1a 02 43 c1 02 e2 52 54 f3 82 1c b5 90 fd 9f 91
    000100 58 96 aa 90 48 9c a9 86 26 86 40 41 4b 2c 81 0b
    000110 32 d5 15 b7 a9 00 00 00 00 ff ff 22 d7 ef 01 1e
    000120 c0 30 0d 70 42 32 38 37 35 31 4f a1 38 9f 08 f7
    000130 62 35 10 18 fb 40 87 86 2a 38 ba 22 c7 93 57 62
    000140 a5 7a 31 51 41 60 66 69 68 62 64 61 62 89 2d 60
    000150 43 1c 91 a2 3f b5 14 98 9c 93 33 32 13 f3 40 e6
    000160 02 00 00 00 ff ff a2 28 10 42 82 40 09 cb 4d 21
    000170 c4 1f c9 c9 c5 25 45 99 c0 20 2e c9 27 ca d9 a6
    000180 16 66 86 06 06 c6 86 60 e3 4d 91 8d 8f 52 08 08
    000190 77 75 72 07 b9 1e 1e ce a1 55 49 a9 d9 99 a0 ec
    0001a0 48 8a db 81 f9 c3 c4 c4 cc cc 00 1a 38 46 66 26
    0001b0 66 70 8b 00 00 00 00 ff ff 02 5a e4 82 70 bc 7a
    0001c0 0a 85 61 e2 a2 e0 ea 03 73 6b 4a 6a 4e 0e e5 c6
    0001d0 05 c1 b2 58 4a 4a 6a 11 15 8c 0b 46 36 af d8 06
    0001e0 00 00 00 ff ff 23 25 18 8d 2c 2c 2d cc cc 8c 2d
    0001f0 21 65 98 09 aa c9 5a 38 5c aa 8f 54 52 02 00 8a
    000200 ac 5a 68

Which contains 16 entries:

    {\*\cxs U/TKROUS/KWREU}you drowsy
    {\*\cxs U/TKPWAOEUGS}you guys
    {\*\cxs U/SURP}usurp
    {\*\cxs U/SRA*U}you have a
    {\*\cxs U/SRA*E}you have a
    {\*\cxs U/SPHAOEPB}you mean so
    {\*\cxs U/SKWRA*EU/AES}you Jay's
    {\*\cxs U/STAEUGS}eustachian
    {\*\cxs U/STRAOEUF/TO}you strive to
    {\*\cxs UZ/PWEBG/STAPB}Uzbekistan
    {\*\cxs UD}you'd
    {\*\cxs UD/EL}Udell
    {\*\cxs UD/ER}udder
    {\*\cxs UD/ERS}udders
    {\*\cxs UD/*ER}udder
