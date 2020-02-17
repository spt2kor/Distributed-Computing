# Map Reduce Concept with Simple Example
https://www.youtube.com/watch?v=PhdRyrmbRYQ
  Mapper->Shuffle->Reducer


# What is the difference between Apache Spark and Apache Hadoop MapReduce?
https://www.youtube.com/watch?v=TX-JgUNT_Ck

Speed vs Memory vs RDD vs Streaming vs API.

Apache Spark vs Apache Hadoop MapReduce
I. Speed: Apache Spark is 10X to 100X faster than Hadoop due to its usage of in memory processing.

II. Memory: Apache Spark stores data in memory, whereas Hadoop MapReduce stores data in hard disk. 

III. RDD: Spark uses Resilient Distributed Dataset (RDD) that guarantee fault tolerance. MapReduce create multiple copy to guarantee fault tolerance

iv. Streaming - Spark does stream data processing, mapReduce store stream data to file then read it back.

v. API - Spark API connects to multiple data source and diff languages(R-Language, Scala, Java, Hive Data Rouse), hadoop not that extensible




















