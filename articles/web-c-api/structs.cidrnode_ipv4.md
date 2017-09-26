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

| 68.7. cidrnode_ipv4 |
| [Prev](structs.apn_error_response.php)  | Chapter 68. Structs |  [Next](structs.command_construct.php) |

## 68.7. cidrnode_ipv4

This struct is a typedef of `_cidrnode_ipv4`. It is defined as follows:

```
struct _cidrnode_ipv4 {
  int threadsafe;
  ck_spinlock_t lock;
  u_int8_t type;
  u_int32_t mask;
  u_int32_t base; /* IP address _NOT_ struct in_addr as it is in host format */
  u_int32_t size;
  struct _cidrnode_ipv4 *low;
  struct _cidrnode_ipv4 *high;
};
```

To use this struct, include the file `cidrtree.h`.

### 68.7.1. See Also

[Chapter 10, *CIDR Functions*](cidr.php "Chapter 10. CIDR Functions") 

| [Prev](structs.apn_error_response.php)  | [Up](structs.php) |  [Next](structs.command_construct.php) |
| 68.6. apn_error_response  | [Table of Contents](index.php) |  68.8. command_construct |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)