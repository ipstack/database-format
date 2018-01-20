# IP Stack database format

Content for file is a binary string.

|Size of block, bytes|Description|
|---|---|
|3|A control word that confirms the authenticity of the file. It is always equal to ISD|
|2|Header size|
|1|Ipstack format version|
|1|Registers count ($RGC)|
|2|Size of registers definition unpack format ($RGF)|
|2|Size of registers definition row ($RGD)|
|1|Relations count ($RLC)|
|1|Size of relations definition unpack format ($RLF)|
|2|Size of relation definition row ($LRD)|
|$RLF|Relation unpack format|
|$RGF|Registers metadata unpack format|
|$RLC*$LRD|Relations|
|$RGC*$RGD|Registers metadata|
|$RGD|Networks metadata|
|1024|Index|
|?|Database of intervals|
|?|Database of Register 1|
|?|Database of Register 2|
|...|...|
|?|Database of Register $RGC|
|4|Unixtime of database actuality time|
|128|Author|
|?|Database license|
