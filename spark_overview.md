# Что такое Spark

Apache Spark - это фреймворк для аналитической обработки больших данных. Он предоставляет API для Java, Scala, Python и R и движок для вычисления на графах. Фреймворк также поддерживает богатый набор инструментов:
- [Spark SQL](https://spark.apache.org/docs/latest/sql-programming-guide.html) для обработки структурированных данных при помощи SQL;
- [pandas API](https://spark.apache.org/docs/latest/api/python/getting_started/quickstart_ps.html) для вычислений на pandas;
- [MLlib](https://spark.apache.org/docs/latest/ml-guide.html) для машинного обучения;
- [GraphX](https://spark.apache.org/docs/latest/graphx-programming-guide.html) для обработки графов; 
- [Structured Streaming](https://spark.apache.org/docs/latest/structured-streaming-programming-guide.html) для инкрементных вычислений и потоковой обработки.

# Загрузка

Загузить Spark можно со страницы [downloads](https://spark.apache.org/downloads.html).
Эта документация предназначена для Spark версии 3.3.1. Spark использует библиотеки Hadoop для HDFS и YARN.
Дистрибутивы подготовлены для нескольких популярных версий Hadoop.
Пользователи также могут скачать сборку без Hadoop и запускать Spark с любой версией Hadoop,
отредактировав classpath фреймворка Spark. Пользователи Scala и Java могут подключать Spark в свои проекты через Maven,
а пользователи Python могут устанавливать Spark из PyPI.

Если вы хотите запустить Spark из исходного кода, перейдите в Building Spark.

Spark запускается как на Windows, так и на UNIX-подобных системах (например, Linux, Mac OS)
и должен работать на любой платформе, для которой существует ожидаемая версия Java.
Это правило относится к JVM как на `x86_64`, так и на `ARM64`. Spark можно запускать локально, достаточно
иметь доступ к java через PATH или переменную окружения JAVA_HOME, указывающую на Java.

Spark работает на Java 8/11/17, Scala 2.12/2.13, Python 3.7+ и R 3.5+.
Поддержка Java 8 до версии 8u201 объявлена устаревшей в Spark 3.2.0. При использовании Scala API необходимо,
чтобы приложения использовали ту же версию Scala, для которой был скомпилирован Spark.
Например, для Scala 2.13 нужно использовать Spark, собранный для 2.13, и компилировать приложения при помощи Scala 2.13.

Для Python 3.9 оптимизация Arrow и пользовательские функции pandas могут не работать из-за проблем совместимости Python и Apache Arrow. Пожалуйста, обратитесь к [странице совместимости](https://arrow.apache.org/docs/python/install.html#python-compatibility) с Python. Для Java 11 дополнительно требуется `-Dio.netty.tryReflectionSetAccessible=true` для библиотеки Apache Arrow. Этa опция предотвращает `java.lang.UnsupportedOperationException: sun.misc.Unsafe или java.nio.DirectByteBuffer.(long, int) not available`, когда Apache Arrow использует Netty.

# Запуск примеров и командная оболочка
