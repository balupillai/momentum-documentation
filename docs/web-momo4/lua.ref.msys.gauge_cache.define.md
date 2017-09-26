Logged in as: OmniTI, Inc.  ([logout](https://support.messagesystems.com/logout.php))

[![Message Systems](https://support.messagesystems.com/images/ms-white205.png)](https://support.messagesystems.com/start.php) 

*   [Changelog](https://support.messagesystems.com/start.php?show=changelog)
*   [Documentation](https://support.messagesystems.com/docs/)
*   [Downloads](https://support.messagesystems.com/start.php)

*   [Licenses](https://support.messagesystems.com/license_summary.php)
*   <a href="">Clients</a>
    *   [Support](https://support.messagesystems.com/cs.php)
    *   [Add/Edit](https://support.messagesystems.com/edit_client.php)
    *   [Legal/Products](https://support.messagesystems.com/edit_products.php)
*   [Users](https://support.messagesystems.com/edit_customer.php)

## Search Help

Search for a single word or perform multi-word searches by enclosing your search in quotation marks.

Where you have multiple words but no quotation marks, an **OR** search is performed. For example, **"REST Injection"** searches for the phrase **"REST Injection"**, and, without quotation marks, searches for **REST OR Injection**--the operator is understood.

### Warning

You must escape the following special characters: **+ - && || ! ( ) { } [ ] ^ " ~ * ? : \**. Use the **\** character as the escape character. For example: **B0/00-11719-46C328D4\:default\:**

You can also perform **AND** searches, for example, **rest AND port** (no quotation marks) finds pages where both these words occur.

Terms used in searches are case-insensitive but operators are not. Alphabetic operators **must** be in uppercase.

Other operators can also be used. For more information see "[Query Parser Syntax](https://lucene.apache.org/core/old_versioned_docs/versions/3_0_0/queryparsersyntax.html)". Use of fields in searches is not currently supported.

| msys.gauge_cache.define |
| [Prev](lua.ref.msys.gauge_cache.dec.php)  | Chapter 70. Lua Functions Reference |  [Next](lua.ref.msys.gauge_cache.get.php) |

<a name="lua.ref.msys.gauge_cache.define"></a>
## Name

msys.gauge_cache.define — Create a cache that can be used to maintain a set of counters

<a name="idp18121088"></a>
## Synopsis

`msys.gauge_cache.define(name, maxelems, ttl, replicated);`

```
name: string
maxelems: number
ttl: number
replicated: boolean, optional
```
<a name="idp18124160"></a>
## Description

Creates a cache that can be used to maintain a set of counters based on a string key. The `ttl` parameter is the number of seconds that a given entry will be maintained after it was last modified, and `maxelems` is the maximum number of named entries that will be stored in the cache. If a new entry is added, the oldest entry in the cache will be dropped to make room for the new entry. If replicated is set to `true`, (the default is `false`), then increments and decrements will be broadcast across the cluster.

Enable this function with the statement `require(' msys.gauge_cache ');`.

<a name="idp18129152"></a>
## See Also

[msys.gauge_cache.inc](lua.ref.msys.gauge_cache.inc.php "msys.gauge_cache.inc"), [msys.gauge_cache.dec](lua.ref.msys.gauge_cache.dec.php "msys.gauge_cache.dec"), [Section 28.1.9, “Shared Gauge Caches”](cluster.config.replication.php#cluster.replication.gauge_cache "28.1.9. Shared Gauge Caches")

| [Prev](lua.ref.msys.gauge_cache.dec.php)  | [Up](lua.function.details.php) |  [Next](lua.ref.msys.gauge_cache.get.php) |
| msys.gauge_cache.dec  | [Table of Contents](index.php) |  msys.gauge_cache.get |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)