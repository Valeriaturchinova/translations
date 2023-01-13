# Типы 

The types supported by the file format are intended to be as minimal 
as possible, with a focus on how the types effect on disk storage. 
Например, 16-битные инты явно не поддерживаются в формате хранения, 
поскольку они покрываются 32-битными интами с эффективным кодированием. 
Это снижает сложность реализации считывающих и записывающих 
устройств для формата. К типам относятся: 
```
BOOLEAN: 1 bit boolean
INT32: 32 bit signed ints
INT64: 64 bit signed ints
INT96: 96 bit signed ints
FLOAT: IEEE 32-bit floating point values
DOUBLE: IEEE 64-bit floating point values
BYTE_ARRAY: arbitrarily long byte arrays.
``` 

[Logical Types](ApacheParquetLogicalTypes.md)
