---
layout: post
title: What is Java release cycle & how often?
---
<div class="row">
    <div class="col-sm-2">
        <img src="/images/java.png" alt="Java logo"/>
    </div>
    <div class="col-sm-10">
        Java release cycle is a specified time sequence or schedule in which a new Java version is released. Currently, there is six months release cycle which usually occurs in March and September of every year. However, in the past, Java had a 2 or 3-years release cycle where a new Java version would come out. The current release cycle introduced in 2018 has been successful to date, unlike the old release cycle.
    The release of major versions is currently spread across multiple and regular releases, but the rate of Java development is the same. In fact, the current release cycle features two different types of releases, which includes:
    </div>
</div>

 * Long term support releases
 * Feature releases – which are the regular releases.

The Features release type lasts until the next release (which is 6 months) and is only supported by oracle.

### Which major version will be released now and when?

Java 17 is the next major version that is set to be released in September 2021. This version is set to feature a restored always-strict floating-point semantics along with other upgraded features. Furthermore, this version is also set to be the next long-term support (LTS) version of the JDK, making it the third-ever LTS release after Java 11 and Java 8 LTS.

H2. Which version is Long Term Support (8,11,17), and for how long? (use dates from Oracle JVM and OpenJDK)

As of now, there are only two Long Term Support versions that have already been released; Java 8 and 11. However, the third LTS version of JDK, Java 17, is set to be released in September this year. These three versions are better than the standard editions which are not LTS and since they ensure a steady release of computer software is sustained for a more extended period of time. For legacy releases, Java SE 8 has now gone through the End of Public Updates process. This means no more free public updates – it will continue providing Java SE 8’s auto and public updates via java.com for Development, Personal, and other Users.

The release and use dates according to Oracle JVM and OpenJDK for these versions are as follows:
 * **Java SE 8** – Released March 2014 with extended support until December 2030 and premium support until March 2022.
 * **Java SE 11** – Released September 2018 with extended support until September 2026 and premium support until September 202.
 * **Java SE 17** – Set to be released on September 2021and its extended support time yet to be confirmed. But according to Oracle, it has premium support until September 2026 and extended support to September 2029.

Note: The end of free public updates for each version varies depending on the user.

### What is special about Java 17 release? (it is LTS + features)

Since Java switch from 2-3 years releases cadence to 6 months, they have created one long-term support (LTS) release, Java 11. As of now, Java 17 is under active development, and it is set to be the second long-term support (LTS) due out in September. 
The release date is based on their current 6-month release cycles, following the Java 16 March release. Apart from being the next LTS version making it a special release, it is also set to come with consistent strict floating-point operations, among other upgraded standard features. 
Java Development Kit (JDK) has the following proposed features:

 * **Always-strict floating-point semantics**
Instead of having both slightly diverse default floating-point semantics and strict floating-point semantics (strictfp), the new release JKD 17 is expected to have always strict.
 * **Vector API (Second Incubator)**
This feature was first integrated into JDK 16 and is set to be integrated into JDK 17 too. Its vector API will be more enhanced to handle the translation of byte vectors to and from Boolean arrays. It will also have improved performance and implementation for graceful degradation and better platform agnostic.
 * **Foreign Function & Memory API**
This API is ideally designed to securely access foreign memory and efficiently invoke foreign functions. With that, an API can efficiently and securely permit Java programs to call up native libraries and process native data while avoiding JNI risks. 
 * **Security Manager Censured for Future Removal**
Java has always had a security manager included since Java 1.0; however, it has rarely been used for many years. Therefore, Java 17 future a deprecated security manager, which will be removed in future versions to allow a unified evolution of Java.  Also, the legacy Applet API (JEP 398) will also be removed in future versions.
 * **Deprecate the Applet API for Removal**
The release JDK 18 will remove the Applet API since the JDK 17 will feature this API marked as deprecated for removal. In fact, this API had not been marked for removal despite being been deprecated in JDK 9. 
Most browsers have plans to or have ended this API support as it has been a long-overdue feature.  
 * **Experimental AOT and JIT Compiler Removal**
The effort required to maintain the experimental Java-based ahead-of-time (AOT) and just-in-time (JIT) compiler is relatively high. Considering its limited usage, Java has therefore chosen to remove them. The JVM compiler interface will be retained to allows developers to complete JIT compilation using the externally-built compiler versions.
 * **Porting the JDK to MacOS/AArch64**
Apple is set to transition from Intel’s x86–64 CPU to Apple-designed chips that use the ARM64/AArch64 architecture. This is according to their 2020 Apple Silicon announcements that will see a two-year transition plan commence. 
 * **New macOS Rendering Pipeline**
With the aid of the new Apple Metal Framework, a new Java 2D rendering pipeline has been implemented for macOS by JEP 382. This will replace the OpenGL rendering library, which was deprecated in macOS 10.14 by Apple in September 2018. 
Currently, Java 2D is totally reliant on OpenGL, which isn’t good, considering Apple may remove the OpenGL API from its future macOS versions.  
 * **Improved pseudorandom number generators**
Th feature will enable implementations for pseudorandom number generators (PRNGs) and provide new interface types. This feature’s goals include:
    * Eliminating duplicated code in existing PRGNs 
    * Preservation of the current behavior of Java.util.Random, 
    * Facilitate interchangeable use of PRGNs algorithms
    * To provide PRNG objects’ streams while enhancing support for the stream-based programming
