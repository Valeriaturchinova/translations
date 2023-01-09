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

В таблице представлены N столбцов, разбитых на M групп строк. Метаданные файла содержат местоположение всех начальных мест метаданных столбцов. Более подробную информацию о том, что содержится в метаданных, можно найти в файлах thrift.

Метаданные записываются после данных, чтобы обеспечить однопроходную запись.

Ожидается, что читатели в первую очередь прочитают метаданные файла, чтобы найти все интересующие их столбцы. Затем эти столбцы должны быть прочитаны последовательно.

Формат явно предназначен для отделения метаданных от данных. Это позволяет разделять столбцы на несколько файлов, а также иметь один файл метаданных, ссылающийся на несколько файлов parquet. 

![This is an image](https://parquet.apache.org/images/FileLayout.gif)

---

## Конфигурации 

## Расширение 

## Метаданные 

## Типы  

## Вложенное кодирование 

## Страницы данных

## Пустые значения (Nulls) 