# **Spark Overview**

Apache Spark is a unified analytics engine for large-scale data processing. It provides high-level APIs in Java, Scala, Python and R, and an optimized engine that supports general execution graphs. It also supports a rich set of higher-level tools including [Spark SQL](https://spark.apache.org/docs/latest/sql-programming-guide.html) 
for SQL and structured data processing, [pandas API on Spark](https://spark.apache.org/docs/latest/api/python/getting_started/quickstart_ps.html) for pandas workloads, [MLlib](https://spark.apache.org/docs/latest/ml-guide.html) for machine learning, [GraphX](https://spark.apache.org/docs/latest/ml-guide.html) for graph processing, and [Structured Streaming](https://spark.apache.org/docs/latest/ml-guide.html) for incremental computation and stream processing.

## **Downloading**
[Get Spark from the [downloads page](https://spark.apache.org/downloads.html) of the project website. This documentation is for Spark version 3.3.1. Spark uses Hadoop’s client libraries for HDFS and YARN. Downloads are pre-packaged for a handful of popular Hadoop versions. Users can also download a “Hadoop free” binary and run Spark with any Hadoop version [by augmenting Spark’s classpath](https://spark.apache.org/docs/latest/hadoop-provided.html). Scala and Java users can include Spark in their projects using its Maven coordinates and Python users can install Spark from PyPI.

If you’d like to build Spark from source, visit [Building Spark](https://spark.apache.org/docs/latest/building-spark.html).

Spark runs on both Windows and UNIX-like systems (e.g. Linux, Mac OS), and it should run on any platform that runs a supported version of Java. This should include JVMs on x86_64 and ARM64. It’s easy to run locally on one machine — all you need is to have java installed on your system PATH, or the JAVA_HOME environment variable pointing to a Java installation.

Spark runs on Java 8/11/17, Scala 2.12/2.13, Python 3.7+ and R 3.5+. Java 8 prior to version 8u201 support is deprecated as of Spark 3.2.0. When using the Scala API, it is necessary for applications to use the same version of Scala that Spark was compiled for. For example, when using Scala 2.13, use Spark compiled for 2.13, and compile code/applications for Scala 2.13 as well.

For Python 3.9, Arrow optimization and pandas UDFs might not work due to the supported Python versions in Apache Arrow. Please refer to the latest [Python Compatibility](https://arrow.apache.org/docs/python/install.html#python-compatibility) page. For Java 11, `-Di.netty.tryReflectionSetAccessible=true` is required additionally for Apache Arrow library. This prevents `java.lang.UnsupportedOperationException: sun.misc.Unsafe or java.nio.DirectByteBuffer.(long, int) not available` when Apache Arrow uses Netty internally.


# **Running the Examples and Shell**
Spark comes with several sample programs. Scala, Java, Python and R examples are in the `examples/src/main` directory. To run one of the Java or Scala sample programs, use `bin/run-example <class> [params]` in the top-level Spark directory. (Behind the scenes, this invokes the more general [spark-submit script](https://spark.apache.org/docs/latest/submitting-applications.html) for launching applications). For example,

```bash
./bin/run-example SparkPi 10
```

You can also run Spark interactively through a modified version of the Scala shell. This is a great way to learn the framework.


```
./bin/spark-shell --master local[2]
```

The `--master` option specifies the [master URL for a distributed cluster](https://spark.apache.org/docs/latest/submitting-applications.html#master-urls), or local to run locally with one thread, or `local[N]`to run locally with N threads. You should start by using `local` for testing. For a full list of options, run Spark shell with the `--help` option.


Spark also provides a Python API. To run Spark interactively in a Python interpreter, use `bin/pyspark`:

Spark also provides a Python API. To run Spark interactively in a Python interpreter, use bin/pyspark:
```bash
./bin/pyspark --master local[2]
```
Example applications are also provided in Python. For example,

```
./bin/spark-submit examples/src/main/python/pi.py 10
```

Spark also provides an [R API](https://spark.apache.org/docs/latest/sparkr.html) since 1.4 (only DataFrames APIs included). To run Spark interactively in an R interpreter, use bin/sparkR:

```
./bin/sparkR --master local[2]
```

Example applications are also provided in R. For example,
```
./bin/spark-submit examples/src/main/r/dataframe.R
```


 #  Launching on a Cluster

The  Spark cluster mode overview explains the key concepts in running on a cluster. Spark can run both by itself, or over several existing cluster managers. It currently provides several options for deployment:

- [Standalone Deploy Mode](https://spark.apache.org/docs/latest/spark-standalone.html): simplest way to deploy Spark on a private cluster
- [Apache Mesos](https://spark.apache.org/docs/latest/running-on-mesos.html) (deprecated)
- [Hadoop YARN](https://spark.apache.org/docs/latest/running-on-yarn.html)
- [Kubernetes](https://spark.apache.org/docs/latest/running-on-yarn.html)


# **Where to Go from Here**
## **Programming Guides**:

- [Quick Start](https://spark.apache.org/docs/latest/quick-start.html): a quick introduction to the Spark API; start here!
- [RDD Programming Guide](https://spark.apache.org/docs/latest/rdd-programming-guide.html): overview of Spark basics - RDDs (core but old API), accumulators, and broadcast variables
- [Spark SQL, Datasets, and DataFrames](https://spark.apache.org/docs/latest/sql-programming-guide.html): processing structured data with relational queries (newer API than RDDs)
- [Structured Streaming](https://spark.apache.org/docs/latest/structured-streaming-programming-guide.html): processing structured data streams with relation queries (using Datasets and DataFrames, newer API than DStreams)
- [Spark Streaming](https://spark.apache.org/docs/latest/structured-streaming-programming-guide.html): processing data streams using DStreams (old API)
[MLlib](https://spark.apache.org/docs/latest/ml-guide.html): applying machine learning algorithms
- [GraphX](https://spark.apache.org/docs/latest/graphx-programming-guide.html): processing graphs
- [SparkR](https://spark.apache.org/docs/latest/sparkr.html): processing data with Spark in R
- [PySpark](https://spark.apache.org/docs/latest/api/python/getting_started/index.html): processing data with Spark in Python
- [Spark SQL CLI](https://spark.apache.org/docs/latest/api/python/getting_started/index.html): processing data with SQL on the command line
    - dcd
    - gfg
        - nested2
        - nested1

         
- vddvv   


1. first.1
1. second.2
