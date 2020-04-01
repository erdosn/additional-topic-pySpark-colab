# additional-topic-pySpark-colab

# Instructions
* open a colab notebook at [colab.research.google.com](colab.research.google.com)
* paste the following into a notebook cell
  ```python
  !apt-get install openjdk-8-jdk-headless -qq > /dev/null
  !wget -q https://downloads.apache.org/spark/spark-2.4.5/spark-2.4.5-bin-hadoop2.7.tgz
  !tar xf spark-2.4.5-bin-hadoop2.7.tgz
  !pip install -q findspark
  ```
* set your environment variables by running the following in the next notebook cell
 ```python
 import os
 os.environ["JAVA_HOME"] = "/usr/lib/jvm/java-8-openjdk-amd64"
 os.environ["SPARK_HOME"] = "/spark-2.4.5-bin-hadoop2.7"
 ```
* verify by running this cell
 ```python
 from pyspark.sql import SparkSession
 spark = SparkSession.builder.master("local[*]").getOrCreate()
```

Video Walkthrough Here
