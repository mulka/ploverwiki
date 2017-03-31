.dix files contain:

0x00: Magic number: "6345 206c 2e34 2030 6964 7463 0d2e 1a0a" (i.e. "Ecl 4.0 dict.\r\n^Z")
0x10: 4-byte big-endian word: length of compressed data
0x14: The compressed data, in XML, compressed using zlib including headers.