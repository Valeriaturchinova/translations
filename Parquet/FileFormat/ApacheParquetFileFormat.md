# Формат файла 

Документация о файловом формате Parquet. 

Этот файл и его определение в thrift следует читать вместе для разбора. 

```
4-byte magic number "PAR1"
<Column 1 Chunk 1 + Column Metadata>
<Column 2 Chunk 1 + Column Metadata>
...
<Column N Chunk 1 + Column Metadata>
<Column 1 Chunk 2 + Column Metadata>
<Column 2 Chunk 2 + Column Metadata>
...
<Column N Chunk 2 + Column Metadata>
...
<Column 1 Chunk M + Column Metadata>
<Column 2 Chunk M + Column Metadata>
...
<Column N Chunk M + Column Metadata>
File Metadata
4-byte length in bytes of file metadata
4-byte magic number "PAR1"
```

В приведенном выше примере изображена таблица из N столбцов разбитых на M групп строк (row groups). Метаданные файла содержат ссылки на начало метаданных всех столбцов. Более подробную информацию о том, что содержится в метаданных, можно найти в файлах thrift.

Раздел с метаданными расположен в файле после данных для обеспечения однопроходной записи на диск.

Ожидается, что процесс чтения в первую очередь обратится к метаданным файла, чтобы найти все необходимые блоки значений столбцов (column chunks). Затем необходимо прочитать эти значения последовательно.

Формат Parquet разделяет метаданные и данные, что позволяет разбить столбцы на несколько файлов, или же иметь один файл с метаданными, который ссылается на несколько файлов типа parquet.

![This is an image](https://parquet.apache.org/images/FileLayout.gif)

---

## [Конфигурации]

## [Расширение]

## [Метаданные] 

## [Типы]

## [Вложенное кодирование]

## [Страницы данных]

## [Пустые значения (Nulls)] 