---
layout: post
title: Apache Hadoop release cycle
---
<div class="row">
    <div class="col-sm-2">
        <img src="/images/hadoop-logo.png" alt="hadoop logo"/>
    </div>
    <div class="col-sm-10">
       Apache Hadoop is an open-source framework for large-scale distributed processing of datasets across clusters of computer systems. It enables users to store large amounts of data, process it in parallel using a distributed computing model, and make use of the data at scale. Hadoop was originally created by Doug Cutting in 2005 and is currently developed by the Apache Software Foundation.
       The release cycle of Apache Hadoop is designed to ensure that the latest version is always available and up-to-date with the most recent changes and bug fixes. The development process involves both major and minor releases. Major releases involve significant new features or changes to existing features. Minor releases involve resolving existing bugs or adding small features.
    </div>
</div>


# Apache Hadoop Release Cycle

Major releases are released on an 18-month cycle. This includes an initial release, followed by any necessary patch releases for bug fixes and other updates. Minor releases are released on a 4-month cycle and involve minor features and bug fixes.

When planning a new Hadoop release, developers need to consider what features to include, what code to write, and how to test the code. First, developers establish an official release plan which outlines what they wish to accomplish over the course of the release. This plan typically outlines the major and minor features that will be included, as well as any new APIs and improvements. Next, developers write and test the code, making sure that any new features are well-documented and compatible across different versions of the software. Finally, the code is tested thoroughly in a simulated environment before being uploaded to the Apache Hadoop repository.

Once the code is uploaded to the repository, it is made available to the public. Users can then download the code and start using it in their Hadoop environments. It is important to note that, in order to ensure stability, releases should not be upgraded immediately. Instead, users should wait until the release has stabilized and is tested in production environments before upgrading.

Below is an example of a typical release cycle for Apache Hadoop:

1. Preparation - During this phase, the development team should decide what features to work on, plan out the design of the release, and allocate resources for the release.

2. Development - During this phase, developers will write the code for the planned features and review it to make sure it works as expected. They will also test it in a simulated environment.

3. Release Candidate - At this stage, the code is reviewed again and tested in a larger environment. If all tests pass, the release candidate is approved and uploaded to the Apache Hadoop repository.

4. Production - After the release is uploaded, users can download it and begin using it in their Hadoop environment. In order to ensure stability, they should wait until the release has been tested in production environments before upgrading.

By following the Apache Hadoop release cycle, users can ensure that their applications are running on the latest version and are up-to-date with the most recent changes and bug fixes. The development of Apache Hadoop is an ongoing process that involves both major and minor releases. By carefully planning and testing each release, users can take advantage of these new features and ensure that their applications are running smoothly and efficiently.

## History
The Apache Hadoop project was started at Yahoo! in 2006, as an effort to create an open source distributed file system for big data analysis. It was later contributed to the Apache Software Foundation and has since become an essential part of the big data landscape.

The first Apache Hadoop release was 0.1.0 on February 5, 2007, with subsequent versions released every few months until version 3.2.0 in October of 2018. Since then, the Apache Hadoop project has been focused on providing major releases with new features and bug fixes.

## Feature Releases
The feature releases are the main releases which bring new features to Apache Hadoop. They are generally released once every six months, but they could also be released earlier if needed. These releases include improvements to existing features as well as new features.

For example, version 2.9.1 included improvements to existing features such as improved scheduling performance, and new features such as improved support for YARN (Yet Another Resource Negotiator) and MapReduce frameworks. Version 3.3.0 included further improvements to YARN and MapReduce, as well as a new feature called hive-query scheduling.

## Bug Fixes
The bug fixes are released between feature releases and are designed to fix any bugs or issues that were discovered since the previous feature release. These releases also include security upgrades and other minor changes.

For example, version 2.9.2 included bug fixes and security upgrades, while version 3.3.1 included bug fixes and minor improvements.

## Code Examples
Hadoop is written in Java and can be used to store and process data in distributed systems. Below is an example of code that can be used to read data from a Hadoop file system:

```java
Path path = new Path("/user/hadoop");
FileSystem fs = path.getFileSystem(conf);
FSDataInputStream in = fs.open(path);
String s = null;
while ((s=in.readLine()) != null) {
    // Read each line in the file
    System.out.println(s);
}
```

This example uses the FileSystem and FSDataInputStream classes to read data from a file on the Hadoop file system.

## Conclusion
The Apache Hadoop release cycle consists of feature releases and bug fixes. The feature releases bring new features and improvements to the platform, while the bug fixes address any issues that may have been discovered since the last feature release. Code examples can also be found to demonstrate how Hadoop can be used to read and write data in distributed systems.
