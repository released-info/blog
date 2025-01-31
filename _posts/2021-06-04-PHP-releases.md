---
layout: post
title: PHP release cycle
---
<div class="row">
    <div class="col-sm-2">
        <img src="/images/php-logo.png" alt="PHP logo"/>
    </div>
    <div class="col-sm-10">
        PHP is a widely-used, open-source scripting language, also known as a server-side scripting language embedded in HTML. This language was originally created in 1994 by Danish-Canadian programmer Rasmus Lerdorf, and it is free to download and use. It is a valuable language that is used in managing session tracking, databases, dynamic content, as well as building entire e-commerce sites.
    </div>
</div>

<meta property="og:title" content="PHP Release Cycle" />
<meta property="og:description" content="PHP follows a structured release cycle with major versions released annually, typically in November or December. Each major version has a lifespan of three years: two years of active support for bug fixes, followed by one year of security fixes only." />
<meta property="og:type" content="article" />
<meta property="og:url" content="https://blog.released.info/2021/06/04/PHP-releases.html" />
<meta property="og:image" content="https://blog.released.info/images/php-logo.png" />
<meta property="article:author" content="Released.info Blog Team" />
<meta property="article:published_time" content="2021-06-04" />


# What is PHP release cycle?
Good question. Well, a PHP release cycle is a set timeline template that showcases when a new PHP version is set to be released. But hold on, what about the minor release cycle? This is the timeline schedule that is based on an in-need basis in which updates and security fixes for the already released and in-use versions will be rolled out.

## How often do these cycles take? 

The PHP’s major release cycle for major versions usually occurs once every year, usually in November or December of every year. However, the minor release follows an in-need basis meaning its release cycle is quite random; it can be once every week or every month.
The current release cycle for new PHP versions was introduced on June 28, 2011, eliminating a chaotic release roadmap that wasn’t clearly defined and understood by many. The newly implemented timeline brought about more visibility and ideal development plans, which proofed essential to users and 3rd parties.

## Key takeaways
Every major version released has a life span of 3 years and is clearly defined as: 
 * Yearly release cycle
 * 3 years release life cycle/span
   * 2 years bug fixes only
   * 1-year security fixes only

## Which major version will be released now and when?
After PHP 8.0 version, released on November 26, 2020, a new PHP version, PHP 8.1, is set to release on November 25, 2021. This version is currently under active development, and it is important to note that its release date can change based on several factors.
Besides it not being released yet, we already have a glimpse of its proposed new features, changes, depreciation, and performance improvements; so, let’s have a look.

### New features:
 * Fibers (rfc)
Among two major new features included in this version, Fibers is one of them. This feature is a low-level mechanism that will help in the management of parallelism. Also known as “green threads,” – is a feature that will be useful for extensive use in frameworks like Amphp and ReactPHP, and probably you won’t use them directly. 
 * Enums (rfc)
Enums is another feature that will be added to version 8.1, which will be a powerful feature that can be utilized for different purposes. For example, Enums can define methods, just like classes. It can also represent a collection of constant values, but most importantly, you can type in those values yourself. Furthermore, Enums can be used to implement interfaces.

Other new features that will be added to version 8.1 include – [Click here](https://php.watch/versions/8.1) for a more detailed explanation for each of these features:
 * final class constants
 * New fsync and fdatasync functions
 * Curl: DNS-over-HTTPS support
 * FPM: Configurable child-process spawn rate
 * New array_is_list function
 * New Sodium XChaCha20 functions
 * Hash functions accept algorithm-specific $options
 * MySQLi: A new MYSQLI_REFRESH_REPLICA constant will be added
 * MurmurHash3 hash algorithm support
 * $_FILES: New full_path value for directory-uploads
 * Intl: New IntlDatePatternGenerator class
 * Array unpacking support for string-keyed arrays
 * Explicit Octal numeral notation
 * xxHash hash algorithms support
 * Curl: File uploads from strings with CURLStringFile
 * never return type

### Syntax/Functionality Changes!

 * Migrations from resource to object, which is part of the long-term vision for converting all resources to dedicated objects
 * Restrict $GLOBALS usage, meaning some edge cases won’t be excitable anymore in $GLOBALS.
 * Default error mode set to exceptions (MySQLi)
For more about future changes, [click here](https://php.watch/versions/8.1).

### Deprecations
Some of the deprecated features or tools include:
 * Serializable interface 
 * mysqli_get_client_info($param) and mysqli::get_client_info method 
 * Return types in PHP built-in class methods and deprecation notices
 * Float to int conversion (implicit incompatible)
 * MySQLi: mysqli_driver->driver_version property 
 * Internal function parameters passing null to non-nullable 

## Key Takeaways!
Due to the major internal changes in phpng as well as the entire version, there have been significant performance improvements, including:
 * Memory consumption has improved by 30-50%  
 * 2-3x increased speed
 * For WordPress users, this version grants the ability to serve up to 3x as many requests per second
However, despite its advantages, this version also still has some drawbacks.

## Problems with PHP 7!

As you may be aware on December 3, 2015, PHP 7 was unveiled after they abandoned PHP 6 version. This caused a lot of confusion, with some unveiling it as PHP 6 instead of 7, but in the end, after a vote, they agreed to name it PHP 7. 
PHP branch, which is considered the foundation of PHP 7 and was originally dubbed PHP next generation (phpng). This version aimed to retain the near-complete language compatibility while refactoring the Zend Engine to optimize PHP performance. This was one of many changes along with new features added to this version, meaning significant internal changes had to be done. The main problem with PHP 7 is that it is backward incompatible.
Backward incompatible

What is it, how has it influenced PHP 7 performance?
 * Despite 80% of web being powered by PHP, version 7 faced a slow transition for the majority of the web. For example, as of February 2017, only 6.6 percent of WordPress sites are on PHP 7 despite having being released two years ago. This issue was mainly because of this version’s compatibility issues with most sites. For example, if you switch from PHP 5 to PHP7, you will not be able to revert to the older legacy systems.
 * Furthermore, if your site isn’t PHP 7 compatible and you end up switching to it, then it is highly likely that you will experience issues with themes and plugins.
All these issues were a blessing in disguise since it presented PHP 7 with futures opportunities for major improvements that steered its evolution.  
