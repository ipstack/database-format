# IP Stack database format

Content for file is a binary string.

|Size|Caption|
|---|---|
|3|A control word that confirms the authenticity of the file. It is always equal to DIT|
|1|Unpack format for header size reading|
|1 or 4|Header size|
|1|Ipstack format version|
|1|Registers count (RC)|
|4|Size of registers metadata unpack formats (RF)|
|RF|Registers metadata unpack format|
|4|Size of register metadata (RS)|
|RS*(RC+1)|Registers metadata|
|1024|Index of first octets|
|?|Database of intervals|
|?|Database of Register 1|
|?|Database of Register 2|
|...|...|
|?|Database of Register RC|
|4|Unixstamp of database creation time|
|128|Author|
|?|Database license|
