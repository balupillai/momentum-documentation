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

| 14.52. sievelib – The sievelib Module |
| [Prev](modules.sieve.php)  | Chapter 14. Modules Reference |  [Next](modules.smtp_cbv.php) |

## 14.52. sievelib – The sievelib Module

<a class="indexterm" name="idp12865776"></a>

Include this module to make full use of the Sieve language.

### 14.52.1. Configuration

The `sievelib` module is defined in the following way:

<a name="idp12870384"></a>

**Example 14.72. sievelib module**

```
Module generic/sievelib sievelib{
}
```

The `sievelib` module has no parameters. You must include this module if you plan to use Sieve commands such as **ec_add**. For more information see [ec_add](sieve.ref.ec_add.php "ec_add") and following.

### 14.52.2. sievelib Management Using Console Commands

**Configuration Change. ** This feature is available starting from Momentum 2.2.2.45.

The sievelib console commands add, subtract, delete and view gauge cache counters created using the the Sieve **ec_gauge_cache_init** command. For more information about this command see [ec_gauge_cache](sieve.ref.ec_gauge_cache.php "ec_gauge_cache").

**14.52.2.1. sievelib help**

Display the available console commands.

**14.52.2.2. sievelib gauge_cache add *`name`* *`key`* *`number`***

Add a number to the key in the specified cache.

**14.52.2.3. sievelib gauge_cache sub *`name`* *`key`* *`number`***

Subtract a number from the key in the specified cache.

**14.52.2.4. sievelib gauge_cache show *`name`* *`key`***

Show the key in the specified cache.

**14.52.2.5. sievelib gauge_cache delete *`name`* *`key`***

Delete the key in the specified cache.

| [Prev](modules.sieve.php)  | [Up](modules.php) |  [Next](modules.smtp_cbv.php) |
| 14.51. sieve – The Sieve Module  | [Table of Contents](index.php) |  14.53. smtp_cbv – SMTP Callback Verification |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)