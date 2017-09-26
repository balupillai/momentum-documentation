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

| dns_cache |
| [Prev](console_commands.dig.php)  | 12.2. System Console Commands |  [Next](console_commands.domain.php) |

<a name="console_commands.dns_cache"></a>
## Name

dns_cache stats, dns_cache refcnts, dns_cache submit, dns_cache lookup — manage Momentum's DNS cache

## Synopsis

`dns_cache lookup` { *`record`* } { *`type`* }

`dns_cache refcnts`

`dns_cache stats`

`dns_cache submit` { *`record`* } { *`type`* }

<a name="idp9661584"></a>
## Description

The following commands help you to collect information on Momentum's dns cache.

**dns_cache stats**       shows summary statistics about the MTA's dns cache.

**dns_cache refcnts**         shows the count of references of each entry in the MTA's dns cache. A cache entry can only be purged when its reference count becomes zero.

**dns_cache submit record type**                    submits a dns query, whose result will be stored in cache if not already.

**dns_cache lookup record type**                    looks up a dns query in the cache.

record type can be `A`, `MX`, `PTR`, `X`, `X_AAAA`, `TXT`, `AAAA`, or `CNAME`.

```
10:47:35 /tmp/2025> dns_cache lookup mail.yahoo.com A
Cached result not found, try a submit.
16:59:26 ecelerity(/tmp/2025)> dns_cache submit mail.yahoo.com A
Submitted
16:59:32 ecelerity(/tmp/2025)> dns_cache lookup mail.yahoo.com A
;; QUESTION SECTION:
;mail.yahoo.com         IN      A

;; ANSWER SECTION:
mail.yahoo.com          299     IN      A       209.73.177.115

16:59:33 ecelerity(/tmp/2025)> dns_cache stats
DNS Queries:
        TXT: 1
        PTR: 1
         MX: 1
          A: 2
  arpa IPv4: 0
  arpa IPv6: 0

DNS responses:
      Total: 5
        Bad: 0

DNS cache:
    Lookups: 14
   Hit Rate: 35.7143%

16:59:41 ecelerity(/tmp/2025)> dns_cache refcnts
[  3] mail.omniti.com [213s]
      (null)
[  3] mail.yahoo.com [282s]
      (null)
[  3] mail.yahoo.com [248s]
      (null)
[  3] mail.yahoo.com [272s]
      (null)
```

### Note

These console commands manipulate the *DNS cache* . The [dig](console_commands.dig.php "dig"), [refresh domain](console_commands.refresh_domain.php "refresh domain") and [domain](console_commands.domain.php "domain") commands manipulate the *route cache* .

| [Prev](console_commands.dig.php)  | [Up](console.commands.non-module.php) |  [Next](console_commands.domain.php) |
| dig  | [Table of Contents](index.php) |  domain |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)