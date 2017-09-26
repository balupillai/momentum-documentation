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

| ec_log |
| [Prev](sieve.ref.ec_ip_rejections_cluster.php)  | Chapter 15. Sieve++ Function Reference |  [Next](sieve.ref.ec_log_file.php) |

<a name="sieve.ref.ec_log"></a>
## Name

ec_log — log to the paniclog

## Synopsis

`ec_log` { *`message`* }

<a name="idp14894592"></a>
## Description

`ec_log` allows you to log arbitrary information to the paniclog. The log record will be prefixed with the script source filename and the line number at which the `ec_log` was executed. The message is logged at the CRITICAL level for the LOG1 subsystem. These messages will appear in the paniclog under the default Debug_Flags settings.

<a name="example.ec_log"></a>

**Example 15.75. ec_log example**

```
if envelope :domain :is "from" "good-guy.com" {
  ec_log "got mail from the good guys";
}
```

### Note

This function cannot log messages longer than `1972` characters. Longer messages are truncated. If your requirements exceed this maximum use [ec_log_file](sieve.ref.ec_log_file.php "ec_log_file") instead.

| [Prev](sieve.ref.ec_ip_rejections_cluster.php)  | [Up](sieve.ref.php) |  [Next](sieve.ref.ec_log_file.php) |
| ec_ip_rejections_cluster  | [Table of Contents](index.php) |  ec_log_file |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)