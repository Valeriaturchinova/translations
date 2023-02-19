# Кодировки 
Простая: (PLAIN = 0)

Поддерживаемые типы: все

Это простая кодировка, поддерживаемая для различных типов. Значения кодируются в последовательном порядке.

Обычное кодирование используется в тех случаях, когда невозможно использовать более эффективное кодирование. Она хранит данные в следующем формате: 

- BOOLEAN: Bit Packed, LSB first

- INT32: 4 bytes little endian

- INT64: 8 bytes little endian 

- INT96: 12 bytes little endian (deprecated) 

- FLOAT: 4 bytes IEEE little endian 

- DOUBLE: 8 bytes IEEE little endian 

- BYTE_ARRAY: length in 4 bytes little endian followed by the bytes contained in the array 

- FIXED_LEN_BYTE_ARRAY: the bytes contained in the array 

