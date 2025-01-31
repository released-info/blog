---
layout: post
title: Microsoft .NET release cycle
---
<div class="row">
    <div class="col-sm-2">
        <img src="/images/net-logo.png" alt="Microsoft .NET"/>
    </div>
    <div class="col-sm-10">
        NET is a software development ecosystem and framework created and supported by Microsoft. The goal for creating this framework enables easy engineering of desktop and web applications. This platform has provided an ideal programming ecosystem for most phases of software development. It has also been used for several different application types due to its popular free platform.
So, what is .NET release cycle, and how often does it occur? Well, .NET release cycle is a schedule to which a new .NET release framework version is released. This released cycle usually occurs after about every one year unless otherwise stated. The new version may sometimes be released before time if the previous release has a crucial problem that needs to be fixed, thus causing the developers (Microsoft) to release a new minor version outside its roadmap schedule. 
    </div>
</div>

<meta property="og:title" content="Microsoft .NET Release Cycle">
<meta property="og:description" content="An overview of the Microsoft .NET release cycle, detailing its history, major versions, minor releases, and point releases, along with code examples demonstrating new features.">
<meta property="og:type" content="article">
<meta property="og:url" content="https://blog.released.info/2021/06/03/Microsoft-NET-releases.html">
<meta property="og:image" content="https://blog.released.info/images/net-logo.png">
<meta property="article:author" content="Released.info Blog Team">
<meta property="article:published_time" content="2021-06-03">


# Which major version will be released now and when?

The next Microsoft .Net version to be released is .NET 6, and it is set to be released on November 9. During this year’s
Build 202 (Microsoft Build conference), Microsoft revealed the final release date after issuing preview 4 for .NET 6
version. `It’s also ready for real-world testing if you haven’t yet tried .NET 6 in your environment`, says Microsoft’s
Richard Lander during the reveal.
Downloadable Preview 4 for .NET 6 is available in [dotnet.microsoft.com](https://dotnet.microsoft.com/). The .NET 6
build comes with finished features and experiences with “Go live” builds expected in August.

What is special about the next .NET release? (features)
So, what makes this next version special? Well, .NET 6 version will feature some of the great and well-integrated
features, which include:
Below are features (additions and improvements) for Preview 3, which was unveiled on April 8:

* **Improved interface casting performance** The interface casting performance has been enhanced to 38% from 16%, which
  profitable for to and between interfaces C# pattern matching.
* **Introduction of .NET Hot Reload supports** using dotnet watch for Blazor and ASP.NET Core projects. This step is
  first and part of a more comprehensive plan to bring this technology to cross-platform client settings in .NET MAUI (
  Multi-platform App UI), supporting desktop development, all .NET developers, among others.
* **Improved generation code through multiple changes in RyuJIT** for the faster running of resulting code as well as a
  more efficient code generation process.
* **The New unsafe API ()** This new CollectionsMarshal.GetValueRef API features improved high-performance that boost
  the updating struct values’ speed in dictionaries.

## The Preview 4 reveals featured the following additions and improvements:

* Extended the Blazor client web app development tool
  This feature is ideally essential for developers set to build hybrid client apps that combine native UIs and web for
  mobile and desktop usage. It isn’t a new feature; the Blazor WebAssembly was among the first .NET 5 unified platform
  deliverable.
* Microsoft .NET 6 will also integrate the existing Xamarin open-source mobile capabilities for Android, iOS, and macOS.
* Improved Linq along with new API
* Date, time, and time zone support enhancements
* Enhanced Hot Reload capabilities:
  The enhancement to hot reload will allow the unstopped app to run while editing its source code. This means you can
  edit the source code while the app keeps running without the need to hit a breakpoint or pause an app.
* Writeable JSON DOM feature
  This feature is Text.Json’s advanced programming model that will provide a straightforward and high-performance
  modelling process. The features will help evade serialization complexities as well as DOM’s traditional cost by
  providing an API.
* Text.Json support for IAsyncEnumerable
  With IAsyncEnumerable<T> objects, this feature will enable System.Text.Json (de)serialization, which currently exists
  as JSON arrays, and supports IAsyncEnumerable<T> objects serializing.
* Windows FileStream performance is significantly enhanced
* Enhancements to RyuJIT compiler
* Inclusion of SDK version checking, which is built-in
* Default enabled Crossgen2 feature
  This feature only applies when publishing for ReadyToRun images, enabling you to use ahead-of-time compilation to
  generate and optimize code.
* Performant logging APIs generated by the LoggerMessageAttribute type.
* Default-enabled warnings for intermediate language (IL) trimming, which alert developers on where trimming may remove
  codes essential for runtime.

## What is .NET Core? Now it will be merge to .NET

.NET Core is a set of frameworks (i.e., library, runtime, and compiler components) that can be used to design
applications for all operating systems, including Mac, Windows, IoTs, Linux, etc. This new cross-platform and
open-source framework will provide flexibility, lightweight developments, and various configurations for all clouds and
devices workloads.

Keep in mind that UWP and ASP.NET Core are the only supported versions in .NET Core, in which ASP.NET Core is to be used
to design browser-based web applications.
If you’re a .NET developer or want to be, then there is nothing to worry about the future of the .NET framework. In the
IT industry, .NET actually is one of the most used frameworks with it been commonly used to build software for most
fortune 500 companies using.    
Currently, most developers have or are planning to port their code from .NET Framework to .NET Core. Porting process is
relatively straightforward for most projects. In fact, what will dictate your merging process from .NET framework to
.NET core is the complexity of your work. The work being referred to here is what you will have to do after the initial
porting of project files. The main reason for this is simply because UWP, among few other .NET features, will not be
playing a significant role in the future of .NET. Remember, .NET 5 came out in 2020, which was termed the next step
evolution or the future of the .NET Framework and .NET Core.

.NET 5 version, published in November 2020, is a unified version that, in fact, marked the foundation of the unification
process. This version has laid the basis for Xamarin developers to use the unified version.
So, if you are planning to migrate program files from .NET Framework to .NET
Core, [here](https://docs.microsoft.com/en-us/dotnet/core/porting/) is an overview of porting guide for you from
Microsoft. 






