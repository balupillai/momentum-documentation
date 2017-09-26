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

| Chapter 18. Using the Metrics API for Reporting |
| [Prev](getting.started.reports_ui.php)  | Part IV. How-To Guides: Reporting and Tracking |  [Next](getting.started.raw_log.php) |

## Chapter 18. Using the Metrics API for Reporting

**Introduction**

Throughout the previous tutorials, you have used the UI to provide insight into your message deliverability and campaign performance. The examples provided have been simple in nature, yet SparkPost Elite provides a vast amount of reporting and analytics data. All the capabilities provided in the UI are also available using the Metrics API.

The Metrics API enables you to retrieve a wide variety of reports using the HTTP protocol. You can retrieve a high-level summary of the aggregate metrics; group the metrics by various parameters; or order them by various conditions. The UI’s powerful drill-down capability is mirrored in the Metrics API by applying various filters to each of these reports. The reports included in the HTTP response are in JSON format.

**Reporting Data Using the Metrics API** 

In this tutorial, you will view the engagement data generated in the tutorial in [Chapter 22, *Tracking Engagement for HTTP*                    ](getting.started.engage.php "Chapter 22. Tracking Engagement for HTTP") using the REST API, instead of the UI. It introduces the Metrics API, which provides the means for retrieving the statistical, real-time data captured by SparkPost Elite.

### Note

This tutorial assumes that you have completed the tutorial in [Chapter 22, *Tracking Engagement for HTTP*](getting.started.engage.php "Chapter 22. Tracking Engagement for HTTP") . A general knowledge of command line tools, JSON, and HTTP protocol is required.

You must have a valid API key to complete this tutorial. If you do not, complete the tutorial [Chapter 3, *Creating, Modifying, and Deleting an API Key*](getting.started.apikey_ui.php "Chapter 3. Creating, Modifying, and Deleting an API Key") .

Follow these steps to report data using the Metrics API:

1.  Request reporting data.

    You retrieve the reporting data by sending a HTTP GET request to the appropriate URL. The path part specifies which REST API to use. For example to access the Metrics API, you send an HTTP request to **https://*`your.server.domain`*/api/v1/metrics/**.

    You can retrieve deliverability metrics that are specific to click events by providing the URI of the link in the GET method.

    At the command line, enter the following command:

    curl -X GET "https://*`your.server.domain`*/api/v1/metrics/deliverability/link-name?from=*`your_date`*&metrics=count_clicked" \
    -H "Authorization: *`your_api_key`*"

    where *`your_date`* is in the format YYYY-MM-DDTHH:MM, and *`your_api_key`* is your valid API key.

2.  Confirm engagement tracking data.

    Confirm that you received the following response at the command line:

    ```
    {  
       "results":{  
          "link_name":"http://www.messagesystems.com",
          "count_clicked":1
       }
    }
    ```

    This response shows that there was one unique click for the link to www.messagesystems.com.

Congratulations! You have successfully retrieved reporting data using the Metrics API. This tutorial demonstrated retrieving data for only one event type. The Metrics API supports many different reports. For detailed information about all the reporting options, see the Metrics API documentation available at [SparkPost Elite REST API](https://www.sparkpost.com/api#/reference).

| [Prev](getting.started.reports_ui.php)  | [Up](p.reporting_tracking.php) |  [Next](getting.started.raw_log.php) |
| Chapter 17. Using the UI for Reporting  | [Table of Contents](index.php) |  Chapter 19. Retrieving Reporting Logs |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)