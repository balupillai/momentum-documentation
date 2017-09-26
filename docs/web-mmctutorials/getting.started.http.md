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

| Chapter 8. Generating a Transmission |
| [Prev](p.sending.php)  | Part III. How-To Guides: Sending |  [Next](getting.started.sub.php) |

## Chapter 8. Generating a Transmission

**Introduction**

Message generation is one of SparkPost Elite's most powerful and flexible features. When using SMTP, your client mail application must send fully formed messages to SparkPost Elite. But what if the components of your transmission are in different systems? SparkPost Elite offers a set of REST API enabling you to inject your recipient list, template, and message content separately. It takes these components of a transmission and generates personalized messages for each recipient.

The REST API integrates with SparkPost Elite using the HTTP protocol and conforms to REpresentational State Transfer (REST) architecture style, which uses client-server communications. The [SparkPost Elite REST API](https://www.sparkpost.com/api#/reference) provide the means to send HTTP requests to SparkPost Elite, while SparkPost Elite processes the requests and returns appropriate HTTP responses. SparkPost Elite's REST API exposes common HTTP methods and returns standard error code formats. JSON is the basis for the request and response format.

**Sending Email Using the REST API** 

In this tutorial, you will learn how to send an email using the REST API. It introduces you to the Transmissions API, which provides the means for creating and managing transmissions. In this simple case, the components of the transmission are included "inline".

You will use the cURL command line tool to send an HTTP request. cURL provides an easy way for doing URL transfers, but you can use any HTTP client or create your own scripts using the language of your choice.

### Note

This tutorial is intended for beginners. However, a general knowledge of command line tools, JSON, HTTP protocol, and templating languages is required.

You must have a valid API key to complete this tutorial. If you do not, complete the tutorial in [Chapter 3, *Creating, Modifying, and Deleting an API Key*](getting.started.apikey_ui.php "Chapter 3. Creating, Modifying, and Deleting an API Key") .

Follow these steps to create a simple transmission:

1.  Specify your input data.

    You create a transmission by first specifying all input data in a JSON blob that will be included in the Transmissions API call. The input data includes required and optional transmission attributes. At a minimum, you must specify the "return_path", "recipients", and "content". The recipients can be specified inline or can reference a stored recipient list. Likewise, the content can be an inline template or can reference a stored template. This example specifies the recipients inline and uses a simple inline template with a plain-text message.

    Using your text editor, create the following JSON file named `inline_template.json`. Be sure to use your sender address and recipient address.

    {  
       "return_path":"*`sender@your_address.com`*",
       "recipients":[  
          {  
             "address":{  
                "email":"*`recipient@their_address.com`*"
             }
          }
       ],
       "content":{  
          "from":"*`sender@your_address.com`*",
          "subject":"Sending Email Using HTTP",
          "text":"Welcome to SparkPost Elite!\r\nThis email was sent using an inline template."
       }
    }

    The attribute "return_path" is the email address to use in the FROM portion of the email header. The attribute "recipients" is a JSON array of recipient objects. This array must include the recipient's "email" address. For inline templates, the transmission includes the "content" object providing the message content. Content for a template is described in a JSON object. At a minimum, it must include a "from" address, a "subject", and "html" or "text" string.

2.  Inject your message.

    You inject your message by sending a HTTP POST request to the appropriate URL with your JSON blob. The path part specifies which REST API to use. For example to access the Transmissions API, you send an HTTP request to **https://*`your.server.domain`*/api/v1/transmissions/**.

    At the command line, enter the following command to inject your email:

    curl -X POST https://*`your.server.domain`*/api/v1/transmissions/ \
    -d @*`path/to/file/`*inline_template.json \
    -H "Content-Type: application/json" \
    -H "Authorization: *`your_api_key`*"

    where `inline_template.json` is the name of your JSON file, `application/json` specifies the format as JSON, and *`your_api_key`* is your valid API key.

    If successful, a response similar to the following will be displayed at the command line:

    {  
       "results":{  
          "total_rejected_recipients":0,
          "total_accepted_recipients":1,
          "id":"*`11668787484950529`*"
       }
    }

    This response shows that one email was accepted and none were rejected.

3.  Confirm your email delivery.

    Verify that your recipient received the email, then open the UI and confirm that your message was successfully injected into SparkPost Elite (Targeted) and accepted by the ISP (Accepted). For instructions to view reports in the UI, see [Chapter 17, *Using the UI for Reporting*](getting.started.reports_ui.php "Chapter 17. Using the UI for Reporting") .

Congratulations! You have sent your first email using SparkPost Elite's Transmissions API and a simple inline template. In addition to the POST method used in this example, the Transmissions API supports the GET method to retrieve or list details about your transmissions. You can find more information in the Transmissions API documentation available at [SparkPost Elite REST API](https://www.sparkpost.com/api#/reference).

| [Prev](p.sending.php)  | [Up](p.sending.php) |  [Next](getting.started.sub.php) |
| Part III. How-To Guides: Sending  | [Table of Contents](index.php) |  Chapter 9. Using Substitution Data |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)