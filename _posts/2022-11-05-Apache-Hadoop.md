---
layout: post
title: Apache Hadoop
---
<div class="row">
    <div class="col-sm-2">
        <img src="/images/hadoop-logo.png" alt="hadoop logo"/>
    </div>
    <div class="col-sm-10">
        Apache Hadoop is an open source software framework for distributed storage and processing of large datasets on computer clusters. It consists of four main components: HDFS, YARN, MapReduce and Apache HBase. Hadoop can be used for a variety of tasks such as data mining, machine learning, real-time analytics, log processing and more. The framework is highly scalable and allows developers to quickly and easily process large datasets.
    </div>
</div>

# Apache Hadoop

Apache Hadoop is a comprehensive, open-source software framework for large-scale distributed storage and processing of big data. It is designed to scale up from single servers to thousands of machines, each offering local computation and storage. It consists of two main components: the Hadoop Distributed File System (HDFS) and MapReduce. HDFS provides distributed storage of data and MapReduce provides distributed computing and processing of data.

Apache Hadoop is an open-source software framework for distributed storage and processing of large datasets on computer clusters. It is based on Java technology and uses the MapReduce computing algorithm.

## History of Hadoop

Hadoop was initially created in 2005 by Doug Cutting, who was then working at Yahoo! It was named after his son’s toy elephant. The project was then open-sourced to become a part of the Apache Software Foundation in 2008.

The first release of Hadoop was in April 2006. It was based on Doug Cutting’s MapReduce algorithm and Google’s File System (GFS) research paper. Since then, Hadoop has grown in popularity and extensive adoption into many enterprises.

## Main Components of Hadoop

Apache Hadoop consists of four main components: Hadoop Distributed File System (HDFS), YARN (MapReduce), MapReduce and Apache HBase. 

### HDFS

Hadoop Distributed File System (HDFS) is the primary data storage system used by Hadoop applications. It is designed to store and manage large datasets with streaming access patterns.

HDFS stores data across multiple nodes and replicates them for fault-tolerance. This makes it a reliable data storage platform for large-scale distributed applications.

### YARN

YARN (Yet Another Resource Negotiator) is the component of Hadoop that manages resources and scheduling. It is responsible for allocating resources to applications, running them on the cluster and providing fault-tolerance. YARN enables developers to build more powerful applications that can be used for data mining, machine learning, real-time analytics and other Big Data processing applications.

### MapReduce

MapReduce is the component of Hadoop that processes data in a distributed fashion. It works by dividing large datasets into smaller chunks and using a map-reduce algorithm to process each chunk in parallel.

MapReduce enables Hadoop to perform complex calculations on large datasets without needing to store them in memory. This increases the scalability and throughput of Hadoop applications.

### Apache HBase

Apache HBase is the component of Hadoop that provides low-latency and random read/write access to large datasets stored in HDFS. HBase is a NoSQL database and is used to store large amounts of data in a distributed fashion.

## How to Use Hadoop

To use Hadoop, you need to install it and configure it for your environment. Hadoop works on any platform that supports a Java Virtual Machine (JVM).

Once Hadoop is installed, you can begin running applications on the cluster. You will need to write a program or use a library to run an application, but once it's set up, you can launch it from the command line.

A common use case for Hadoop is to analyze large datasets. You can use MapReduce to process data in parallel and create reports and visualizations from the results.

Another popular use case is to ingest streaming data and transform it into meaningful insights. For example, Hadoop can be used to collect log data from web servers and perform analysis on it in real time.

Finally, Hadoop can be used for machine learning and predictive analytics. By leveraging the distributed processing power of Hadoop, it is possible to create models and run analytics on large data sets faster than ever before.

## Example Code

Here is an example of how to run a MapReduce job on Hadoop:

```java
public class MyMapReduceJob {
    public static void main(String[] args) throws Exception {
        // Create a job and set the jar option
        Job job = new Job();
        job.setJarByClass(MyMapReduceJob.class);

        // Set the mapper and reducer classes
        job.setMapperClass(Mapper.class);
        job.setReducerClass(Reducer.class);

        // Set the input and output paths
        FileInputFormat.setInputPaths(job, new Path("in"));
        FileOutputFormat.setOutputPath(job, new Path("out"));

        // Submit the job and wait for it to complete
        job.waitForCompletion(true);
    }
}
```

In this example, we are creating a MapReduce job and setting the mapper and reducer classes. We are also specifying the input and output paths for the job. Finally, we submit the job and wait for it to complete.


### Origins of Hadoop

The original version of Hadoop was released in 2006 by Doug Cutting, who named it after his son's stuffed toy elephant. The term “Hadoop” was often used as a nickname for the platform given its elephant associations. In 2007, Yahoo! began using the platform for internal operations. It wasn’t until 2008 that the Apache Software Foundation announced Hadoop as an open source project.

### Hadoop Ecosystem

Since that time, the Apache Hadoop ecosystem has grown to include many sub-projects such as MapReduce, Pig, Hive, and Spark. The core technology of Apache Hadoop lies in the HDFS (Hadoop Distributed File System), which enables the storage and retrieval of data across many separate nodes of the cluster. The MapReduce component allows users to perform distributed processing on large data sets by breaking down the data into smaller chunks, which are then processed in parallel. The other components of the Hadoop ecosystem work in concert with the HDFS and MapReduce tools to provide additional utility and flexibility.

### Usage

Apache Hadoop is used in a variety of different applications and industries, from finance and healthcare to video streaming and social media. One example of its usage is in finance, where Hadoop is used to process large banking transactions and store them securely in a distributed manner. This helps to ensure that financial data is always secure and can be easily accessed whenever needed. It can also be used for fraud detection and analytics, as well as creating complex financial models. 

Another use case of Hadoop is in healthcare. It can be used to manage patient data and records more efficiently, as well as to process large volumes of medical imaging data. Hadoop can also be used to help develop personalized treatments and make care decisions based on individual patient needs.

### Code Examples

The following code samples are examples of how MapReduce can be used in Apache Hadoop:

#### Word Count Algorithm

This example counts the number of words in a file.

```java
import java.io.IOException;
import org.apache.hadoop.fs.Path;
import org.apache.hadoop.conf.*;
import org.apache.hadoop.io.*;
import org.apache.hadoop.mapreduce.*;
import org.apache.hadoop.mapreduce.lib.input.*;
import org.apache.hadoop.mapreduce.lib.output.*;

public class WordCount {

  public static void main(String[] args) throws Exception {
    Configuration conf = new Configuration();
    Job job = new Job(conf, "wordcount");
    job.setOutputKeyClass(Text.class);
    job.setOutputValueClass(IntWritable.class);
    job.setMapperClass(WordCountMapper.class);
    job.setReducerClass(WordCountReducer.class);
    job.setInputFormatClass(TextInputFormat.class);
    job.setOutputFormatClass(TextOutputFormat.class);
    FileInputFormat.addInputPath(job, new Path(args[0]));
    FileOutputFormat.setOutputPath(job, new Path(args[1]));
    job.waitForCompletion(true);
  }

  public static class WordCountMapper 
      extends Mapper<LongWritable, Text, Text, IntWritable> {
    private final static IntWritable one = new IntWritable(1);
    private Text word = new Text();
    public void map(LongWritable key, Text value, Context context) 
        throws IOException, InterruptedException {
      String line = value.toString();
      StringTokenizer tokenizer = new StringTokenizer(line);
      while (tokenizer.hasMoreTokens()) {
        word.set(tokenizer.nextToken());
        context.write(word, one);
      }
    }
  }

  public static class WordCountReducer
      extends Reducer<Text, IntWritable, Text, IntWritable> {
    public void reduce(Text key, Iterable<IntWritable> values, Context context)
        throws IOException, InterruptedException {
      int sum = 0;
      for (IntWritable val : values) {
        sum += val.get();
      }
      context.write(key, new IntWritable(sum));
    }
  }

}
```

#### WeatherData Processing

This example reads weather data and calculates temperature averages.

```java
import java.io.IOException;
import org.apache.hadoop.conf.*;
import org.apache.hadoop.fs.Path;
import org.apache.hadoop.io.*;
import org.apache.hadoop.mapreduce.*;
import org.apache.hadoop.mapreduce.lib.input.*;
import org.apache.hadoop.mapreduce.lib.output.*;

public class WeatherData {

  public static void main(String[] args) throws Exception {
    Configuration conf = new Configuration();
    Job job = new Job(conf, "weatherdata");
    job.setOutputKeyClass(Text.class);
    job.setOutputValueClass(DoubleWritable.class);
    job.setMapperClass(WeatherDataMapper.class);
    job.setReducerClass(WeatherDataReducer.class);
    job.setInputFormatClass(TextInputFormat.class);
    job.setOutputFormatClass(TextOutputFormat.class);
    FileInputFormat.addInputPath(job, new Path(args[0]));
    FileOutputFormat.setOutputPath(job, new Path(args[1]));
    job.waitForCompletion(true);
  }

  public static class WeatherDataMapper 
      extends Mapper<LongWritable, Text, Text, DoubleWritable> {
    private Text location = new Text();
    private DoubleWritable temperature = new DoubleWritable();
    public void map(LongWritable key, Text value, Context context) 
        throws IOException, InterruptedException {
      String[] parts = value.toString().split("\t");
      location.set(parts[0]);
      double temp = Double.parseDouble(parts[2]);
      temperature.set(temp);
      context.write(location, temperature);
    }
  }

  public static class WeatherDataReducer
      extends Reducer<Text, DoubleWritable, Text, DoubleWritable> {
    public void reduce(Text key, Iterable<DoubleWritable> values, 
        Context context) 
        throws IOException, InterruptedException {
      double sum = 0.0;
      int count = 0;
      for (DoubleWritable val : values) {
        sum += val.get();
        count++;
      }
      double average = sum/count;
      context.write(key, new DoubleWritable(average));
    }
  }

}
```



## History
Apache Hadoop was created by Doug Cutting and Mike Cafarella in 2006. It was initially developed to support distribution for the Nutch search engine project. The original goal was to enable distributed processing of large datasets across clusters of commodity computers. Since its inception, Hadoop has grown into a complete distributed computing platform that supports large scale data processing. 

## Architecture
Apache Hadoop is based on the "master-slave" architecture where the master node manages the cluster of compute nodes. The master node runs the NameNode daemons, which stores the metadata about the files stored in the cluster. The compute nodes run DataNode daemons, which store the actual data contained in the files. The compute nodes also run MapReduce tasks, which perform the distributed computations over the data contained in the files.

## Usage
Apache Hadoop can be used for a variety of applications including distributed big data analytics, text analysis, machine learning, graph processing, and stream processing. 

### Text Analysis
Apache Hadoop can be used to perform large scale text analysis using the various text processing tools in the Hadoop ecosystem. For example, Apache Pig can be used to perform natural language processing tasks such as tokenization, part-of-speech tagging, lemmatization, stemming, and named-entity recognition. Apache Hive can be used to perform advanced text analytics such as sentiment analysis and topic modeling.

### Machine Learning
Apache Hadoop can also be used to perform distributed machine learning tasks. Apache Mahout is a popular tool for performing distributed machine learning tasks such as clustering, classification, and collaborative filtering. Apache Spark is also popular for performing distributed machine learning tasks using the MLlib library.

### Graph Processing
Apache Hadoop can also be used for distributed graph processing. Apache Giraph is a popular tool for performing graph processing tasks such as shortest path calculation, connected components, and PageRank. Spark GraphX is also popular for performing distributed graph processing tasks.

### Stream Processing
Apache Hadoop can also be used for stream processing. Apache Storm is a popular tool for performing stream processing tasks such as real-time analytics, complex event processing, and continuous computation. Apache Flink is also popular for performing distributed stream processing tasks. 

# Apache Hadoop
Apache Hadoop is an open source framework for distributed storage and processing of large datasets across clusters of computers. It was created by Apache Software Foundation (ASF) in 2006 and has since become one of the most popular big data frameworks used today. The Hadoop platform consists of several modules, such as HDFS (Hadoop Distributed File System), Map Reduce, YARN (Yet Another Resource Negotiator), and HBase (Hadoop Database). These modules are used to store and process large amounts of data in a distributed manner.

## History of Apache Hadoop 
The development of Apache Hadoop began in 2006 as a research project at Yahoo! Research. It was made publically available in 2011 and soon after began to be used by many large organizations such as Facebook, Twitter, and LinkedIn. In 2012, Apache Hadoop was accepted into the Apache Incubator program and became a Top Level Project in 2013.

## Usage of Apache Hadoop
Apache Hadoop is used for many different purposes, such as analyzing logs, streaming data, connecting disparate data sources, extracting insights from large datasets, and more. Many companies utilize Hadoop to store and analyze vast amounts of data from various sources. Hadoop can also be used to create data-driven applications and services, such as recommendation systems, fraud detection systems, and event correlation platforms.

## Features of Apache Hadoop
The main features of Apache Hadoop include its scalability, fault tolerance, and availability. Apache Hadoop is designed to scale up from single servers to thousands of machines. It uses replication and redundancy to ensure that the data is safe and accessible even if some nodes fail or become unavailable. The system also provides high levels of parallelism, allowing for fast and efficient data processing.

## Code Examples
Below is a simple example of how to use Apache Hadoop to store and process data. First, we need to set up Hadoop on our cluster of computers. Then, we can transfer data from our local machine to the cluster using HDFS. We can then use the MapReduce framework to process the data in parallel. Lastly, we can use HBase to store the processed results.

```
// Set up Hadoop on the cluster
$ hadoop-setup.sh

// Transfer data to HDFS
$ hadoop fs -copyFromLocal <local_file> <hdfs_folder>

// Run MapReduce
$ hadoop jar <jar_name>.jar <main_class> <input_path> <output_path>

// Store output in HBase
$ hbase shell
create '<table_name>', '<column_family_name>'
put '<table_name>', '<row_key>', '<column_family_name>':'<column_name>', '<value>'
```

## Conclusion

Apache Hadoop is a popular open source distributed computing framework for large scale data processing. It is based on the "master-slave" architecture and consists of two main components: the Hadoop Distributed File System (HDFS) and MapReduce. Hadoop is used for a variety of applications including distributed big data analytics, text analysis, machine learning, graph processing, and stream processing.

Apache Hadoop is a powerful open source framework for distributed storage and processing of large datasets. It offers scalability, fault tolerance, availability, and high levels of parallelism for processing data in an efficient manner. It is used by many companies for various purposes, such as analyzing logs, streaming data, extracting insights from large datasets, and creating data-driven applications.
