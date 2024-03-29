# Страницы данных
Для страниц данных 3 части информации кодируются после заголовка страницы. На странице представлены

- данные об уровнях определения, 

- данные уровней повторения, 

- закодированные значения. Размер, указанный в заголовке, предназначен для всех 3 частей в целом.

Данные для страницы данных всегда обязательны. Уровни определения и повторения являются необязательными, исходя из определения схемы. Если столбец не является вложенным (т.е. путь к столбцу имеет длину 1), мы не кодируем уровни повторения (они всегда будут иметь значение 1). Для данных, которые являются обязательными, уровни определения пропускаются (если они закодированы, то всегда будут иметь значение максимального уровня определения).

Например, в случае, когда колонка не является вложенной и обязательной, данные на странице - это только закодированные значения.

Поддерживаемые кодировки описаны в файле Encodings.md

[Encodings](./Encodings/ApacheParquetEncodings.md)

[Checksumming](./Checksumming/ApacheParquetChecksumming.md)

[Column Chunks](./ColumnChunks/ApacheParquetColumnChunks.md)

[Error Recovery](./ErrorRecovery/ApacheParquetErrorREcovery.md)