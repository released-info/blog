---
layout: post
title: Apache Solr
---
<div class="row">
    <div class="col-sm-2">
        <img src="/images/solr.png" alt="solr logo"/>
    </div>
    <div class="col-sm-10">
       Apache Solr is an open source enterprise search engine based on the Apache Lucene library. It provides a distributed, scalable, fault-tolerant platform for indexing and searching large volumes of data. Solr is used in many industries including media, telecoms, retail, healthcare, and government.
    </div>
</div>


# Apache Solr

Apache Solr was first released in 2004 by CNET Networks. It was originally written as a web crawler to index webpages, but the scope has since been expanded to include a variety of document types such as PDFs, Word documents, spreadsheets, emails, and more.

In 2007, the Apache Software Foundation adopted Solr as a top-level project. Since then, Solr has become the most popular open source enterprise search platform, used by many of the world's largest companies.

Apache Solr is an open source search engine technology based on Apache Lucene. It is an enterprise ready, scalable, and fault tolerant search platform capable of full-text search over large volumes of data. Apache Solr is a popular choice for websites and applications requiring powerful text search functionality.

## History

Apache Solr was first released in 2004 as an open source project. The goal of the project was to create an easily usable and fully customizable search engine platform. Since then, Apache Solr has become a widely used search technology and is currently maintained by the Lucene project.

## Features

Apache Solr offers a number of powerful features, including: 

- Full-text search capabilities 
- Faceted search 
- Geospatial search 
- Advanced search algorithms 
- High performance scalability 
- Fault tolerance

## Usage Examples

Apache Solr is used in many different types of applications, from e-commerce sites to knowledge bases and more. Some common use cases include: 

- Full-text search of product catalogs 
- Faceted product navigation 
- Autosuggest and spell checking 
- Search engine optimization (SEO) 
- Enterprise search applications 
- Knowledge management systems 

## Code Examples 

The following code example demonstrates how to configure a Solr core and define search fields. 

```xml
<?xml version="1.0" encoding="UTF-8" ?> 
<config> 
    <luceneMatchVersion>LUCENE_8_7</luceneMatchVersion> 
    <requestHandler name="/select" class="solr.SearchHandler"> 
        <lst name="defaults"> 
            <str name="df">text</str> 
        </lst> 
    </requestHandler> 

    <schema name="example" version="1.6"> 
        <fieldType name="text" class="solr.TextField" positionIncrementGap="100"> 
            <analyzer type="index"> 
                <tokenizer class="solr.StandardTokenizerFactory"/> 
                <filter class="solr.StopFilterFactory" ignoreCase="true" words="stopwords.txt"/> 
                <filter class="solr.LowerCaseFilterFactory"/> 
            </analyzer> 
            <analyzer type="query"> 
                <tokenizer class="solr.StandardTokenizerFactory"/> 
                <filter class="solr.StopFilterFactory" ignoreCase="true" words="stopwords.txt"/> 
                <filter class="solr.SynonymGraphFilterFactory" synonyms="synonyms.txt" ignoreCase="true" expand="true"/> 
                <filter class="solr.LowerCaseFilterFactory"/> 
            </analyzer> 
        </fieldType> 

        <field name="title" type="text" indexed="true" stored="true"/> 
        <field name="desc" type="text" indexed="true" stored="true"/> 
        <field name="body" type="text" indexed="true" stored="false"/> 
    </schema>
</config>
```

This example configures a Solr core with three search fields: `title`, `desc`, and `body`. The `text` field type is defined which uses both the standard Solr tokenizer and filters, as well as a synonym graph filter. This allows us to perform searches that take into account synonyms as well.

## Features
Apache Solr offers a variety of features for developers, including:
* Full-text search
* Faceted search
* Spell checking
* Query autocomplete 
* Geospatial search
* Relevancy tuning
* Highlighting

## Usage Examples
Solr is used by businesses for myriad reasons, including:
* Improving customer experience and search capabilities on ecommerce sites
* Storing, indexing, and serving documents from legal databases
* Powering real-time recommendations for streaming services
* Automatically tagging images
* Indexing logs for analytics and monitoring

## Code Example
A simple query using the Solr Query Syntax might look like this:

```
http://localhost:8983/solr/gettingstarted/select?indent=on&q=title:example&wt=json
```

This query will search for any documents with the word "example" in the title field and return the results in JSON format.

### Basic Query

The following example demonstrates a basic Solr query which searches for documents containing the term "Solr":

```
http://localhost:8983/solr/collection1/select?q=Solr
```

### Faceted Search

The following example demonstrates a faceted search, which performs a query on the field "title" and returns the count of each unique term in the field:

```
http://localhost:8983/solr/collection1/select?q=title:[* TO *]&facet=true&facet.field=title
```

### Geospatial Search

The following example performs a geospatial search for documents within a 5km radius of San Francisco, California:

```
http://localhost:8983/solr/collection1/select?q=*:*&fq={!geofilt%20sfield=location%20pt=37.7749,-122.4194%20d=5}
```

## Usages 

Apache Solr is widely used for search applications in website and enterprise applications. It can be used for full-text search of webpages, text documents, and even database records. It is also used for natural language processing, document summarization, and machine learning applications. Some popular websites using Apache Solr are Digg, Craigslist, Reddit, and Zappos. 

Apache Solr is also used by many enterprises for indexing and searching large datasets. It is being used by major companies such as AOL, Apple, IBM, Oracle, and Salesforce. It is also used by government agencies and public universities such as the US Department of Justice, US Air Force, and Harvard University. 

## Code Examples 

Apache Solr is written in Java and can be used with any JVM language, including Scala, Clojure, Groovy, and Kotlin. Here's an example of how to index and search a simple document using Apache Solr: 

### Indexing

```java
// create a new solr client
SolrClient solr = new HttpSolrClient("http://localhost:8983/solr");
 
// create a new Solr input document
SolrInputDocument doc = new SolrInputDocument();
 
// add fields to the document
doc.addField("id", "12345");
doc.addField("title", "My Document");
doc.addField("content", "This is the content of my document.");
 
// add the document to the index
solr.add(doc);
 
// commit the changes to the index
solr.commit();
```

### Searching

```java
// create a new solr client
SolrClient solr = new HttpSolrClient("http://localhost:8983/solr");
 
// create a query
SolrQuery query = new SolrQuery();
query.setQuery("content:document");
 
// execute the query
QueryResponse response = solr.query(query);
 
// process the results
for (SolrDocument doc : response.getResults()) {
    String title = (String) doc.getFieldValue("title");
    System.out.println(title);
}
```

## Conclusion 

Apache Solr is a powerful, enterprise-level search platform that enables robust full-text searches. It is open source, fast, scalable and feature-rich, making it a popular choice for many developers and organizations. With its built-in support for caching, replication, failover, and load balancing, Apache Solr is an ideal solution for large-scale search projects.
