---
layout: post
title: MariaDB release cycle
---
<div class="row">
    <div class="col-sm-2">
        <img src="/images/maria-db.png" alt="MariaDB logo"/>
    </div>
    <div class="col-sm-10">
        MariaDB is an open-source relational database management system (RDBMS). It is a fork of the popular MySQL project and provides the same feature set with additional scalability, scalability and security enhancements. MariaDB is part of the MariaDB Foundation and is widely used as a database engine for web applications, embedded applications and an alternative to proprietary database systems.
    </div>
</div>

# MariaDB Release Cycle

In this article, we will explore the MariaDB release cycle and how it has been continuously developed over the years.
We'll also discuss how to choose the right version of MariaDB as well as look at some code examples.

## History of MariaDB

MariaDB was released in 2009 by MySQL founder and original developer, Michael “Monty” Widenius. After MySQL was acquired
by Oracle in 2008, Widenius decided to fork the source code and create a new project that would remain free, open
source, and community-oriented.

MariaDB quickly grew in popularity and made it into the top 20 of relational databases in use at large websites
according to the DB-Engines Ranking. Today, MariaDB is a widely used database engine powering many large websites,
including Wikipedia and Google.

## MariaDB Release Cycle

MariaDB follows a regular software release cycle which includes versions from 5.5 to 10.5. These versions are designated
as "major" releases, each of which contains important new features and updates.

Minor versions are released on an as-needed basis, with bug fixes and other smaller patches. They are usually released
as needed, usually within 2 weeks of the major release.

The release cycle for MariaDB also includes "bugfix" releases which address only minor stability and security issues.
These releases come out less often, typically when needed.

Finally, MariaDB also participates in the Long Term Support (LTS) program, which guarantees support and security fixes
for the entire duration of the LTS. Currently, the latest LTS release is MariaDB 10.4 and is slated to be supported
until 2024.

## Choosing the Right Version of MariaDB

Choosing the right version of MariaDB for your project can be difficult. Generally, you'll want to choose the newest
version available as it will have the most up-to-date features and security patches. However, if you need certain
specific features or need to remain compatible with existing applications, you may opt for an older version.

When choosing a version of MariaDB, keep in mind the following points:

- Is the version compatible with your existing applications?
- Does the version contain the features you need?
- Are there any security vulnerabilities with the version?
- Is the version still being supported and maintained?
- Do you need to upgrade anytime soon?

## Code Examples

Below is an example of how to connect to a MariaDB database in Node.js:

```javascript
const mariadb = require('mariadb');

const pool = mariadb.createPool({
    host: 'localhost',
    user: 'user',
    password: 'password',
    database: 'test',
    connectionLimit: 5
});

let conn;

try {
    conn = await pool.getConnection();
    const rows = await conn.query('SELECT 1+1 as solution');
    console.log(rows);
} catch (err) {
    throw err;
} finally {
    if (conn) conn.end();
}
```

In this example, we are using the `mariadb` package to create a connection pool to connect to a MariaDB database. We
then use the `getConnection()` method to get a connection object from the pool and use the `query()` method to execute a
simple query.

We also use a `finally` block to ensure that the connection is closed when the execution reaches the end. This is
important to ensure that the connection resources are not wasted.

## Conclusion

The MariaDB release cycle is a highly organized and efficient process that ensures new features, bugfixes, and security
patches are applied to the database regularly. It also allows users to choose the right version of MariaDB for their
applications, as each version has its own set of features and is supported for a certain amount of time.

Finally, with MariaDB's steady development and growth, it has become one of the most popular open-source relational
databases.
