\# Overview Exploits/CVE

* MSG\_ReadBitsCompressed (by Sabotage), same as described by Momo5502 (Huffman), resides inside SV\_ExecuteClientMessage

"In the function SV\_ExecuteClientMessage, the length of the

compressed data is not checked to be smaller than the

allocated buffer on the stack before the call to MSG\_ReadBitsCompress.



Overflowing the buffer using a modified client message

enables arbitrary code execution"

