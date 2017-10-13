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

| Chapter 23. Using DomainKeys Identified Mail (DKIM) Signatures |
| [Prev](using_domainkeys.validation.php)  | Part III. Configuring Momentum |  [Next](using_dkim.validation.php) |

## Chapter 23. Using DomainKeys Identified Mail (DKIM) Signatures

**Table of Contents**

<dl class="toc">

<dt>[23.1\. DKIM Signing](using_dkim.php#using_dkim.signing)</dt>

<dt>[23.2\. DKIM Validation](using_dkim.validation.php)</dt>

</dl>

DomainKeys Identified Mail (DKIM) is a mechanism that allows verification of the source and contents of email messages. Using DKIM, sending domains can include a cryptographic signature in outgoing email messages. A message's signature may be verified by any (or all) MTAs during transit and by the Mail User Agent (MUA) upon delivery. A verified signature indicates the message was sent by the sending domain and the message was not altered in transit. A signature that fails verification indicates the message may have been altered during transit or that the sender is fraudulently using the sending domain name. Unsigned messages contain no guarantee about the sending domain or integrity of the message contents. For more information about DKIM, see [draft-ietf-dkim-base-00](http://tools.ietf.org/html/draft-ietf-dkim-base-00).

To determine subsequent handling of incoming email messages, service providers may use the success/failure of DKIM signature verification or the lack of a DKIM signature. The provider can drop invalid messages without impacting the final recipient, exposing the results of DKIM verification directly to the recipient, or exposing the lack of a signature directly to the recipient. Additionally, service providers may use signature verification as the basis for persistent reputation profiles to support anti-spam policy systems or to share with other service providers.

[Figure 23.1, “DKIM schematic”](using_dkim.php#figure_dkim_schematic "Figure 23.1. DKIM schematic") gives a graphical view of how DKIM works.

<a name="figure_dkim_schematic"></a>

**Figure 23.1. DKIM schematic**

![](images/gr_dkeys_1.gif)

## For Sending Servers

1.  Set up

    The domain owner (typically the team running the email systems within a company or service provider) generates a public/private key pair to use for signing all outgoing messages (multiple key pairs are allowed). The public key is published in DNS, and the private key is made available to their DKIM-enabled outbound email servers. This is step "A" in the diagram to the right.

2.  Signing

    When each email is sent by an authorized end-user within the domain, the DKIM-enabled email system automatically uses the stored private key to generate a digital signature of the message. This signature is included in a DKIM-Signature header and prepended to the email. The email is then sent on to the recipient's mail server. This is step "B" in the diagram to the right.

## For Receiving Servers

1.  Preparation

    The DKIM-enabled receiving email system extracts and parses the message's DKIM-Signature header. The signing domain asserted by the header is used to fetch the signer's public key from DNS. This is step "C" in the diagram to the right.

2.  Verification

    The signer's public key is then used by the receiving mail system to verify that the signature contained in the DKIM-Signature header was generated by the sending domain's private key. This proves that the email was truly sent by, and with the permission of, the claimed sending domain. It also provides that all the headers signed by the sending domain and the message body were not altered during transit.

3.  Delivery

    The receiving email system uses the outcome of signature verification along with other local policies and tests to determine the disposition of the message. If local policy does not prohibit delivery, the message is passed to the user's inbox. Optionally, the email recipient may be informed of the results of the signature verification. This is step "D" in the diagram on the right.

## 23.1. DKIM Signing

Enabling DKIM signing in Momentum is a two-step process:

1.  Generate public and private keys for each signing domain and create the DKIM public key DNS records for those domains.

    *   For instructions, see [Section 23.1.1, “Generating DKIM Keys”](using_dkim.php#using_dkim.generating "23.1.1. Generating DKIM Keys")

2.  Configure Momentum to conditionally attach DKIM signatures to emails that are submitted into the MTA.

    *   Load the opendkim module. For details, see [Section 71.50, “opendkim – Open Source DKIM”](modules.opendkim.php "71.50. opendkim – Open Source DKIM").

    *   Configure the opendkim module to sign messages or write policy to do so at runtime using Lua functions. For details, see [Section 71.50.2, “Lua Functions”](modules.opendkim.php#modules.opendkim.lua.functions "71.50.2. Lua Functions").

    *   Set the `opendkim_sign` option to `true` in the appropriate scope to enable DKIM signing on a global, per domain, per binding, or per binding-per domain basis. For details, see [opendkim_sign](conf.ref.opendkim_sign.php "opendkim_sign").

To control how OpenDKIM signing statistics are recorded, see [signing_stats](conf.ref.signing_stats.php "signing_stats"). The console command [signing_stats](console_commands.signing_stats.php "signing_stats") is used to examine signing statistics and [signing_stats reset](console_commands.signing_stats_reset.php "signing_stats reset") resets statistics.

### 23.1.1. Generating DKIM Keys

The OpenSSL cryptography toolkit is used to generate RSA keys for DKIM. As an example, the following openssl commands are used to generate public and private keys for the domain `example.com` with a selector called `dkim1024`. Typically, the directory `/opt/msys/ecelerity/etc/conf/dkim` is used for key storage.

```
# mkdir -p /opt/msys/ecelerity/etc/conf/dkim/example.com
# openssl genrsa -out /opt/msys/ecelerity/etc/conf/dkim/example.com/dkim1024.key 1024
# openssl rsa -in /opt/msys/ecelerity/etc/conf/dkim/example.com/dkim1024.key \
        -out /opt/msys/ecelerity/etc/conf/dkim/example.com/dkim1024.pub -pubout -outform PEM
```

All DKIM verification implementations must support key sizes of 512, 768, 1024, 1536, and 2048 bits. A signer may choose to sign messages using any of these sizes and may use a different size for different selectors. Larger key sizes provide greater security but impose higher CPU costs during message signing and verification.

### Warning

Note that Google requires all senders to sign with a 1024 bit or greater DKIM key size.

The resulting public key should look similar to:

```
-----BEGIN PUBLIC KEY-----
MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQCrZXNwzXOk0mRqPcgSUOnmVHro
rg/BZHybpiBoDS/g6IaMjmVwaQf2E72x9yDBTgiUBtTCqydQRZJ3EbfYfvo+WAHq
2yz6HKR0XCwMDSE2S3brVe7mbV/GPEvnCuFPPEVjbfL4w0tEAd8Seb5h07uVQqy1
Q7jIOnF5fG9AQNd1UQIDAQAB
-----END PUBLIC KEY-----
```

Once the public and private keys have been generated, create a DNS text record for `dkim1024._domainkey.example.com`. The DNS record contains several DKIM "tag=value" pairs and should be similiar to the record shown below:

```
dkim1024._domainkey.example.com. 86400 IN TXT
"v=DKIM1; k=rsa; h=sha256; t=y; p=MHww...QAB"
```

DKIM DNS text record tags are defined below (do not include the quotes below when including a tag value in the DNS text record):

<dl class="variablelist">

<dt>v=</dt>

<dd>

DKIM key record version. The value of this tag must be set to "DKIM1".

</dd>

<dt>k=</dt>

<dd>

Key type. This tag defines the syntax and semantics of the p= tag value. Currently, this tag should have the value "rsa".

</dd>

<dt>h=</dt>

<dd>

Hash algorithm. Currently, this tag should have the value "sha1" or "sha256".

</dd>

<dt>t=</dt>

<dd>

Flags. The only value currently defined is "y". If specified, this tag indicates the signing domain is testing DKIM.

</dd>

<dt>p=</dt>

<dd>

DKIM public key value generated as described above.

</dd>

<dt>s=</dt>

<dd>

Service Type. If specified, this tag should be set to "*" or "email" which represents all service types or the email service type. Currently, "email" is the only service using this key.

</dd>

<dt>n=</dt>

<dd>

Notes. If specified, the value of this tag is quoted-printable text used as a note to anyone reading the DNS text record. The tag is not interpreted by DKIM verification and should be used sparingly because of space limitations of the DNS text record.

</dd>

</dl>

| [Prev](using_domainkeys.validation.php)  | [Up](p.configuration.php) |  [Next](using_dkim.validation.php) |
| 22.2. DomainKeys Validation  | [Table of Contents](index.php) |  23.2. DKIM Validation |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)