---
layout: post
title: Apache Spark
---
<div class="row">
    <div class="col-sm-2">
        <img src="/images/spark-logo.png" alt="Spark logo"/>
    </div>
    <div class="col-sm-10">
        Apache Spark is an open source, distributed computing engine that aims to provide a unified platform for large-scale data processing. It can be used for a variety of tasks, such as large-scale data analysis, machine learning, streaming data applications, and much more. With its advanced features and reliability, Apache Spark has become the go-to tool for working with large data sets.
        Spark is designed to be easy to use and highly performant, allowing users to quickly analyze and process their data. It utilizes a directed acyclic graph (DAG) execution engine, which allows for a wide variety of operations to be carried out quickly and efficiently. The DAG engine also optimizes operations across the cluster, making it easier to scale out computations. Additionally, Spark provides an API that allows developers to write applications in Java, Scala, Python, and R.
    </div>
</div>


# Apache Spark

Apache Spark is an open-source distributed computing framework originally developed at the University of California, Berkeley. It was built on top of Hadoop, a batch-processing and distributed computing system, to provide a more interactive and powerful way of performing data analysis operations. Apache Spark allows for data processing of massive amounts of datasets using distributed computing clusters. This makes it ideal for use in data science and analytics, as well as machine learning.
Spark is written in Scala and was first released in 2010. It has since become one of the most popular platforms for data scientists and data engineers, as well as businesses seeking to make better use of their data.
Spark is an ultrafast distributed computing platform that can efficiently process large amounts of data in-memory while providing fault tolerance, scalability, and ease of programmability. It is designed to integrate with the existing Hadoop Distributed File System (HDFS) and other components of the Big Data ecosystem.
Spark is based on a cluster computing architecture, which is a group of computers working together to run a set of tasks. By distributing the work across many computers, Spark is able to achieve high throughput and low latency. It also provides easy access to massive amounts of data stored in HDFS or other distributed storage systems.
The core technology of Spark is the Resilient Distributed Dataset (RDD), which is used to store data and make it available for distributed computations. RDDs are resilient to data loss, so if one node fails, another node can be brought up to take its place without data loss.
Spark also includes several libraries for facilitating data analysis, such as Spark SQL, MLlib, and GraphX. Each of these libraries provides different features for different tasks, such as querying data, machine learning applications, and graph analytics.

Spark is used in a variety of applications that require high-speed distributed computing. Some examples include:

* Machine learning: Spark is a popular choice for building and training machine learning models, especially deep learning models.
* Business intelligence: Spark can quickly perform online queries and OLAP operations on large datasets.
* Big data processing: Spark makes it easy to process large datasets stored in a Hadoop cluster, allowing for faster analysis.
* Streaming analytics: Spark's streaming API makes it easy to ingest and process streaming data in real-time.

In addition to its uses in data science and big data, Spark is also used in production systems. Examples include airline route optimization, streaming fraud detection, and personalized recommendation systems.

## History

Apache Spark was initially developed at the University of California, Berkeley's AMPLab in 2009 as part of the [STORM](https://en.wikipedia.org/wiki/Storm_(software)) project. Spark was later donated to the Apache Software Foundation in 2014. Since then, it has seen exponential growth in its community and user base. As of 2021, Apache Spark is the most widely used open source computing engine in the world, with over 3 million downloads each month.

## Features

Apache Spark offers many powerful features that enable users to quickly and easily analyze their data. These features include:

* **In-memory caching** - Spark stores data in memory for faster access and processing. This allows for faster computation and iterative algorithms which require frequent access to the same data.
* **Parallel processing** -  Spark takes advantage of computer clusters to parallelize tasks across multiple cores, providing immense scalability and performance.
* **Machine learning libraries** - Spark includes MLlib, a library of ML algorithms that can be used for predictive analytics, clustering, and classification.
* **Streaming analytics** - Spark Streaming enables real-time processing of streaming data, such as stock market data or live web traffic.

## Advantages of Apache Spark 
Apache Spark offers several advantages over traditional big data processing frameworks. One major advantage is speed. Spark is much faster than Hadoop; it can process data up to 100 times faster than Hadoop MapReduce. Spark also provides better scalability than Hadoop by using in-memory processing and fault tolerance. Additionally, Spark has a unified programing model that makes it easier to develop applications. This model allows developers to write code in multiple languages, including Java, Scala, Python, and R.

## Adoption of Apache Spark Usages 
Apache Spark is used in many different types of organizations. Here are a few examples:

* Netflix uses Spark to process data from millions of customers to provide personalized recommendations.
* Amazon Web Services (AWS) uses Spark to power their Machine Learning services.
* eBay uses Spark to process the large amounts of data from its customers.
* NASA uses Spark to monitor climate data from satellites.
* Adobe uses Spark for text analysis of customer feedback and to detect fraud.

## Usage

Apache Spark has a wide variety of applications, both in academia and industry. Here are just a few examples of how it can be used:

* **Data processing** - Spark is frequently used to process large datasets. It can ingest both structured and unstructured data and provides APIs in Java, Scala, Python, and R to quickly query and analyze it.
* **Machine learning** - Companies use Spark to build and deploy sophisticated machine learning algorithms at scale. Spark’s MLlib library enables users to easily develop models on very large datasets.
* **Real-time analytics** - Organizations can use Spark for real-time analytics, such as tracking customer activity, monitoring financial markets, and detecting fraud.

## Example Code

The following code shows how to use Apache Spark to calculate the mean of a set of numbers:

```
import org.apache.spark.SparkContext
val sc = new SparkContext()

val data = sc.parallelize(Array(1, 2, 3, 4, 5))
val mean = data.mean
```

In this example, we first create a SparkContext object which allows us to interact with our cluster. We then create a parallelized collection of numbers which we assign to the variable `data`. Finally, we use the `mean` method to calculate the average of the numbers, which is stored in the `mean` variable.

Here are some code examples of Spark written in Java and Python.

### Java
```
import org.apache.spark.SparkConf;
import org.apache.spark.api.java.JavaRDD;
import org.apache.spark.api.java.JavaSparkContext;

public class Sample {
    public static void main(String[] args) {

        // Create a SparkConf object
        SparkConf conf = new SparkConf();

        // Set application name
        conf.setAppName("My App");

        // Create a JavaSparkContext object
        JavaSparkContext sc = new JavaSparkContext(conf);

        // Create a JavaRDD of strings
        JavaRDD<String> lines = sc.textFile("/path/to/input.txt");

        // Use filter to remove empty lines
        JavaRDD<String> nonEmptyLines = lines.filter(line -> !line.isEmpty());

        // Print out the non-empty lines
        System.out.println(nonEmptyLines.collect());
    }
}
```

### Python
```
from pyspark import SparkConf, SparkContext

# Create SparkConf object
conf = SparkConf()

# Set application name
conf.setAppName('My App')

# Create a SparkContext object
sc = SparkContext(conf=conf)

# Read input file 
lines = sc.textFile('/path/to/input.txt')

# Use filter to remove empty lines
nonEmptyLines = lines.filter(lambda line: line != '')

# Print out the non-empty lines 
print(nonEmptyLines.collect())
```

### Streaming Analytics
The following example shows how to process a stream of data using the Spark Streaming API:

```scala
object SparkStreaming {
  def main(args: Array[String]) {
    // Create a local StreamingContext with two working thread
    val conf = new SparkConf().setMaster("local[2]").setAppName("NetworkWordCount")
    val ssc = new StreamingContext(conf, Seconds(1))

    // Create a DStream that will connect to hostname:port, like localhost:9999
    val lines = ssc.socketTextStream("localhost", 9999)

    // Split each line into words
    val words = lines.flatMap(_.split(" "))

    // Count each word in each batch
    val pairs = words.map(word => (word, 1))
    val wordCounts = pairs.reduceByKey(_ + _)

    // Print the first ten elements of each RDD generated in this DStream to the console
    wordCounts.print()

    // Start the computation
    ssc.start()
    // Wait for the computation to terminate
    ssc.awaitTermination()
  }
}
```

### Machine Learning
The following example shows how to use the MLlib API to implement a machine learning algorithm:

```scala
object MLlibExample {
  def main(args: Array[String]) {
    val spark = SparkSession
      .builder
      .appName("MLlibExample")
      .getOrCreate()

    // Load and parse the data file, converting it to a DataFrame.
    val data = spark.read.format("libsvm").load("data/mllib/sample_libsvm_data.txt")

    // Automatically identify categorical features, and index them.
    val featureIndexer = new VectorIndexer()
      .setInputCol("features")
      .setOutputCol("indexedFeatures")
      .fit(data)

    // Split the data into training and test sets (30% held out for testing)
    val Array(trainingData, testData) = data.randomSplit(Array(0.7, 0.3))

    // Train a RandomForest model.
    val rf = new RandomForestClassifier()
      .setLabelCol("label")
      .setFeaturesCol("indexedFeatures")

    // Chain indexers and forest in a Pipeline
    val pipeline = new Pipeline()
      .setStages(Array(featureIndexer, rf))

    // Train model.  This also runs the indexers.
    val model = pipeline.fit(trainingData)

    // Make predictions.
    val predictions = model.transform(testData)

    // Select example rows to display.
    predictions.select("prediction", "label", "features").show(5)

    // Select (prediction, true label) and compute test error
    val evaluator = new MulticlassClassificationEvaluator()
      .setLabelCol("label")
      .setPredictionCol("prediction")
      .setMetricName("accuracy")
    val accuracy = evaluator.evaluate(predictions)
    println("Test Error = " + (1.0 - accuracy))

    spark.stop()
  }
}
```

### Graph Processing
The following example shows how to use the GraphX library to analyze a graph:

```scala
object GraphXExample {
  def main(args: Array[String]) {
    val spark = SparkSession
      .builder
      .appName("GraphXExample")
      .getOrCreate()

    // An edge is defined by two nodes and an optional relation
    val edges = spark.sparkContext.makeRDD(
      Array(
        Edge(1L, 2L, 5),
        Edge(2L, 3L, 3),
        Edge(3L, 4L, 5)))
    
    // Build the initial graph
    val graph = Graph.fromEdges(edges, "defaultProperty")
    
    // Run PageRank
    val ranks = graph.pageRank(0.0001).vertices
    
    // Join the ranks with the nodes
    val users = spark.sparkContext.makeRDD(
      Array(
        (1L, "Alice"),
        (2L, "Bob"),
        (3L, "Charley"),
        (4L, "Dennis")))
    val ranksByUsername = users.join(ranks).map {
      case (id, (username, rank)) => (username, rank)
    }
    
    // Print the result
    println(ranksByUsername.collect().mkString("\n"))
  }
}
```

### Machine Learning

Using the MLlib library, Spark can easily perform machine learning algorithms in-memory, allowing for faster model training. For example, the following code Train a logistic regression model on a sample dataset:

```
import org.apache.spark.ml.classification.LogisticRegression

val training = spark.read.format("libsvm").load("data/mllib/sample_libsvm_data.txt")

val lr = new LogisticRegression()
  .setMaxIter(10)
  .setRegParam(0.3)
  .setElasticNetParam(0.8)

val lrModel = lr.fit(training)
```

This code loads a dataset in libsvm format, then creates a logistic regression model, trains it on the dataset, and returns the trained model.

### Business Intelligence

Spark SQL can be used to quickly query and analyze large datasets. The following example shows how to query and aggregate data from a table in Hive:

```
// Create a temporary view corresponding to a Hive table
val sqlContext = new org.apache.spark.sql.hive.HiveContext(sc)
sqlContext.sql("CREATE TEMPORARY VIEW sales AS SELECT * FROM hivesampletable")

// Compute the average revenue per day
val result = sqlContext.sql("SELECT day, AVG(revenue) AS avg_revenue FROM sales GROUP BY day")

// Print the results
result.collect().foreach(println)
```

This code uses the HiveContext to create a temporary view of a Hive table, then runs an SQL query on the table to compute the average revenue per day. The result is printed out.

### Streaming Analytics

Spark Streaming makes it easy to ingest streaming data into a Spark cluster and process it in real-time. For example, the following code reads from a Kafka topic, performs a word count on the data, then prints out the results:

```
// Create a streaming context
val ssc = new StreamingContext(sc, Seconds(1))

// Read from a Kafka topic
val lines = KafkaUtils.createStream(ssc, zkQuorum, "my-topic", Map("my-topic" -> 1)).map(_._2)

// Perform a word count
val words = lines.flatMap(_.split(" "))
val wordCounts = words.map(x => (x, 1)).reduceByKey(_ + _)

wordCounts.print()

// Start the streaming context
ssc.start()
ssc.awaitTermination()
```

In this code, the streaming context reads data from a Kafka topic, then counts the number of times each word appears in the stream. The results are printed out.

## Conclusion

Apache Spark is a powerful and popular open-source distributed computing framework used for data processing and analytics. Its efficient use of memory and its ability to handle large datasets make it ideal for performing machine learning, business intelligence, and big data processing tasks.
Spark provides easy access to a variety of distributed storage systems, including HDFS and other components of the Big Data ecosystem. It also includes multiple libraries for facilitating data analysis, such as Spark SQL, MLlib, and GraphX.
Finally, Spark is used in a variety of production systems, including airline route optimization, streaming fraud detection, and personalized recommendation systems.
