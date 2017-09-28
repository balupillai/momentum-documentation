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

| 14.53. persist_io – Persistent IO Wrapper |
| [Prev](modules.pe2_logger.php)  | Chapter 14. Modules Reference |  [Next](modules.pipeio.php) |

## 14.53. persist_io – Persistent IO Wrapper

<a class="indexterm" name="idp20781072"></a>

The `persist_io` module provides a non-volatile cache wrapper for any other IO wrapper. For example, one could load a file over the HTTP IO wrapper, such that if the HTTP server is down then the consumer of the file will be provided with the locally cached copy. An example of how to use the persist IO wrapper with the HTTP IO wrapper to load a script in the Sieve module is below:

**Configuration Change. ** In version 3.0, this module is loaded automatically as required and does not need to be explicitly included.

<a name="example.persist_io.3"></a>

**Example 14.81. persist_io module**

```
persist_io {
  dirmode = 0700
}
sieve "sieve1" {
  script "connect_phase1" {
    source = "persist://http://www.foo.com/mysievescript.siv"
  }
}
```

It should not be necessary to use this module in version 3.0, since the configuration repository functionality provides for persistent configurations that can be centrally managed.

Find below a description of the configuration options for the `persist_io` module.

<dl class="variablelist">

<dt>dirmode</dt>

<dd>

The octal representation of the permissions for the directory that holds the cached files. The default value is `0700`

</dd>

<dt>filemode</dt>

<dd>

The octal representation of the permissions for cached files. The default value is `0600`

</dd>

<dt>persist_path</dt>

<dd>

The path to the directory that holds the cached files. The default value is `/var/log/ecelerity/persist`.

</dd>

</dl>

| [Prev](modules.pe2_logger.php)  | [Up](modules.php) |  [Next](modules.pipeio.php) |
| 14.52. pe2_logger – Module  | [Table of Contents](index.php) |  14.54. pipe_io – Pipe IO Wrapper |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)