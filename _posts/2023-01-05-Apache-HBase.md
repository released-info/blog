---
layout: post
title: Apache HBase
---
<div class="row">
    <div class="col-sm-2">
        <img src="/images/hbase-logo.png" alt="hbase logo"/>
    </div>
    <div class="col-sm-10">
       Apache HBase is an open source, distributed, versioned, non-relational database written in Java. It is a part of the Apache Hadoop project and runs on top of the HDFS (Hadoop Distributed File System). HBase provides random access and strong consistency for large amounts of unstructured data, and is used for real-time read/write access to your Big Data.
    </div>
</div>

<meta property="og:title" content="Apache HBase">
<meta property="og:description" content="Apache HBase is an open-source, distributed, versioned, non-relational database built on top of the Hadoop Distributed File System (HDFS). It provides real-time read/write access to large datasets and is designed to scale from single servers to thousands of machines.">
<meta property="og:type" content="article">
<meta property="og:url" content="https://blog.released.info/2023/01/05/Apache-HBase.html">
<meta property="og:image" content="https://blog.released.info/images/hbase-logo.png">
<meta property="article:author" content="Released.info Blog Team">
<meta property="article:published_time" content="2023-01-05">


# Apache HBase

HBase was developed out of the need for real-time, random read/write access to very large datasets. Since it is built
upon HDFS, it provides low-latency access to structured data by utilizing distributed computing techniques.
Apache HBase was first developed at Powerset, a search startup that was later acquired by Microsoft in 2008. The goal
was to provide a system to support real-time access to petabytes of unstructured data for interactive search.
In 2006, Powerset engineers started building a distributed storage system based on Google's BigTable design. To meet
their performance requirements, they had to extend the design and wrote a new code base. This code base was eventually
open sourced in 2009 as Apache HBase.
Since then, Apache HBase has been heavily used in production by many companies and powers applications such as
Facebook’s Messages Service, Yahoo’s Messaging Infrastructure, LinkedIn’s Realtime Activity Streams, OpenX advertising
platform and many others.

## History of Apache HBase

Apache HBase was originally created in the spring of 2006 by Powerset, a technology company in San Francisco, CA. The
company's goal was to build an efficient system to handle large datasets of unstructured data. The first version of
HBase was released in July 2008 as an open source project under the Apache Software Foundation. Since then, the project
has grown rapidly, with more than 5,000 commits to its source code and close to 1,000 contributors all over the world.

## What is Apache HBase

Apache HBase is a distributed, column-oriented database that runs on top of HDFS. It is modelled on Google's BigTable
and provides random read/write access to data using HDFS as the underlying storage layer. It supports both batch
processing and real-time search.

HBase is designed to scale from single servers to thousands of machines, each offeringlocal computation and storage.
This enables HBase to handle massive data sets with billions of rows and millions of columns, and at the same time
provides low latency and high throughput for a wide range of Big Data applications.

## How to Use Apache HBase

HBase is mainly used for real-time lookup and analysis of large datasets. For example, HBase can be used as a storage
layer for a website to provide real-time search and analytics capabilities. It can also be used in conjunction with
other Apache projects such as Apache Hive and Apache Pig to provide interactive queries and analytics.

In order to use Apache HBase, you need to deploy a cluster of machines and install the HBase software. Once the HBase
software is installed, you can create tables and insert data. You can then query the data using MapReduce or JRuby.

## Apache HBase adoption

Apache HBase is commonly used for a variety of different purposes, including:

* Storing web logs and clickstream data
* Maintaining user profiles and session data
* Real-time analytics on streaming data
* Building real-time recommendation systems
* Indexing the full text of documents

## Features

At its core, Apache HBase is a column-oriented database management system that runs on top of the Hadoop Distributed
File System (HDFS). It allows users to store and process large amounts of data quickly and reliably.
Some of the key features of Apache HBase include:

* Flexible schema: HBase has a schema-less data model that allows users to add, modify, or delete columns on the fly.
  This makes it easy to store and query massive amounts of structured and semi-structured data.
* Real-time read/write access: HBase provides real-time read and write access to large-amounts of unstructured data.
  This makes it well suited for applications that require low latency response times.
* Fault tolerance: Apache HBase is designed for fault tolerance, meaning it can automatically recover from hardware or
  software failures without any manual intervention.
* Scalability: Apache HBase is designed for horizontal scalability, meaning it can easily scale across multiple machines
  if needed.

## Code Examples

Here are some examples of how to use Apache HBase:

### Creating a Table

The following example shows how to create a table in HBase using the Java API:

```java
// Create an HBase admin object
HBaseAdmin admin=new HBaseAdmin(configuration);

// Create a Description of the table
        HTableDescriptor tableDescriptor=new HTableDescriptor("my_table");

// Create a column family
        HColumnDescriptor family=new HColumnDescriptor("my_family");
        tableDescriptor.addFamily(family);

// Create the table
        admin.createTable(tableDescriptor);
```

### Inserting Data

The following example shows how to insert data into a table in HBase using the Java API:

```java
// Create an HBase connection object
Configuration configuration=HBaseConfiguration.create();
        HTable table=new HTable(configuration,"my_table");

// Create aPut object to insert data
        Put put=new Put("row1" .getBytes());
        put.add("my_family","column1" .getBytes(),"value1" .getBytes());
        put.add("my_family","column2" .getBytes(),"value2" .getBytes());

// Insert the data
        table.put(put);
```

### Querying Data

The following example shows how to query data from a table in HBase using the Java API:

```java
// Create an HBase connection object
Configuration configuration=HBaseConfiguration.create();
        HTable table=new HTable(configuration,"my_table");

// Create a Get object to query data
        Get get=new Get("row1" .getBytes());
        get.addColumn("my_family","column1" .getBytes());

// Retrieve the data
        Result result=table.get(get);
        String value=new String(result.getValue("my_family","column1" .getBytes()));
        System.out.println(value); // prints "value1"
```

Below is a basic example of how to set up and use a HBase table in Java. This example creates a table named "TestTable"
and adds two columns, "name" and "age".

```java
// Create configuration
Configuration conf=HBaseConfiguration.create();

// Create a connection
        Connection connection=ConnectionFactory.createConnection(conf);

// Create a new table
        Admin admin=connection.getAdmin();
        TableName tableName=TableName.valueOf("TestTable");
        HTableDescriptor desc=new HTableDescriptor(tableName);

// Add columns
        HColumnDescriptor namecol=new HColumnDescriptor("name");
        desc.addFamily(namecol);
        HColumnDescriptor agecol=new HColumnDescriptor("age");
        desc.addFamily(agecol);

        admin.createTable(desc);

// Put some data
        Table table=connection.getTable(tableName);
        Put put=new Put(Bytes.toBytes("row1"));
        put.addColumn(Bytes.toBytes("name"),Bytes.toBytes("John"),Bytes.toBytes("Smith"));
        put.addColumn(Bytes.toBytes("age"),Bytes.toBytes("34"));
        table.put(put);

// Get some data
        Get get=new Get(Bytes.toBytes("row1"));
        get.addColumn(Bytes.toBytes("name"));
        Result result=table.get(get);
        String name=Bytes.toString(result.getValue(Bytes.toBytes("name"),Bytes.toBytes("John")));
        System.out.println("Name: "+name);

// Close resources
        table.close();
        connection.close();
```

This example shows how to create a table, add columns, insert data, and retrieve data from the table.

HBase also provides a rich set of APIs, such as the Java API, REST API, Thrift API, Avro API, and so on that can be used
to interact with the data stored in HBase tables.

## Examples of Usage

There are many use cases for Apache HBase, including:

### Storing Web Log Data

Apache HBase can be used to store huge amounts of web log data. HBase's schema-less data model and real-time access make
it ideal for logging and analyzing user activity on websites.

For example, Yahoo uses HBase to store terabytes of web logs to analyze user usage patterns and optimize their website
performance.

### Real-time Analytics

Apache HBase can be used to store and analyze streaming datasets in real-time. This makes it well suited for anyone who
needs to make decisions quickly, such as stock traders, data scientists, and researchers.

For example, Apache HBase is used by financial firms to store and analyze streaming market data in real-time to make
trading decisions.

### Storing Social Network Data

Apache HBase can be used to store and analyze large amounts of social network data. This makes it well suited for
applications that require understanding user relationships and trends such as recommendation engines.

For example, Facebook uses HBase to store and analyze terabytes of social network data to understand user relationships
and trends.

## Code Examples

### Writing Data

This example shows how to write some data to an HBase table using the Java API:

```java
Configuration conf=HBaseConfiguration.create();
        HTable table=new HTable(conf,"TABLE_NAME");
        Put put=new Put(Bytes.toBytes("rowKey"));
        put.add(Bytes.toBytes("cf"),Bytes.toBytes("columnName"),
        Bytes.toBytes("value"));
        table.put(put);
```

### Reading Data

This example shows how to read some data from an HBase table using the Java API:

```java
Configuration conf=HBaseConfiguration.create();
        HTable table=new HTable(conf,"TABLE_NAME");
        Get get=new Get(Bytes.toBytes("rowKey"));
        Result result=table.get(get);
        byte[]value=result.getValue(Bytes.toBytes("cf"),
        Bytes.toBytes("columnName"));
        String valueStr=Bytes.toString(value);
```

```java
import org.apache.hadoop.hbase.*;
import org.apache.hadoop.conf.Configuration;
 
Configuration config=HBaseConfiguration.create();
        HTable table=new HTable(config,"myTableName");

        Put put=new Put(Bytes.toBytes("row_key"));
        put.add(Bytes.toBytes("column_family"),Bytes.toBytes("column_name"),Bytes.toBytes("value"));
        table.put(put);
```

The above code creates a new row in an HBase table and sets the value of a specific column.

## Conclusion

Apache HBase is an open source, distributed, versioned, column-oriented store modeled after Google’s BigTable. It
provides data model facilities to store huge amounts of unstructured, sparse data with low latency and is used by many
companies and organizations for various applications. Examples of applications that can use HBase include time series
data, real-time updates, full-text search, and fast analytics over large datasets.
