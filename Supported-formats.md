Plover is (or will be) able to import dictionaries from other steno programs. Here are some technical notes on each file format.

## json

The standard Plover format. Described at [[Dictionary format]].

## rtf (aka CRE)

A standard interchange format. Described at http://www.legalxml.org/workgroups/substantive/transcripts/cre-spec.htm .

## dct (aka Stentura, Jet, MDB, Microsoft Access)

These are standard Microsoft Access databases (otherwise known as Microsoft Jet databases, or MDB files. They contain a single table named "Steno", which has columns named "Steno", "English", and "Flags". Each row represents a translation.

"Steno" is a text column containing the stroke, encoded as a concatenated sequence of six-digit hex strings representing bitmasks; each bit represents a key in the standard steno order

"English" is a text column giving the text translation of that stroke.

"Flags" is an integer bitmap. 0x8000 indicates a suffix; 0x4000 indicates a prefix; 0x2000 indicates that the next word should be capitalised.

Python lacks good cross-platform MDB support, so Plover reads the files using pure Python.

## sgdct (CaseCat)

CaseCATalyst dictionaries have the extension ".sgdct". There is often a corresponding ".sgxml" file, but this contains no dictionary data.

Much of the detail of the file format remains unknown. Contributions and corrections are very welcome. Thanks are due to Sooty, who provided example files for dissection.

The files begin with a 640-byte header, which begins with the magic number SGCAT32. Nothing is known about header fields at present.

One or more records follow the header. Each record gives a single translation from steno to text.

The record header is 21 bytes. header[18] contains the number of strokes, and header[19] gives the number of letters in the text. Each is an unsigned byte. The purpose of all other fields in the record header is unknown at present.

The stroke follows, as a sequence of four-byte unsigned integers. Each integer is a bitmap of keys in the standard steno order, with the first "S" as the most significant bit.

Then the text follows, as ordinary ASCII text. Nothing is currently known about coding of text outside the ASCII range. Various non-ASCII characters crop up, apparently as control codes.

Finally, there are zero to three padding bytes, in order to bring us up to a four-byte boundary.