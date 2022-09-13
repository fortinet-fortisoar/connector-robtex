## About the connector
Robtex uses various sources to gather public information about IP numbers, domain names, host names, autonomous systems, routes, etc., doing data forensics, investigating competitors, tracking spammers, hackers, or hackers or a virus.This connector facilitates automated operations to pull forward and reverse of an IP number and an AS number together with GEO-location data and network data.
<p>This document provides information about the Robtex Connector, which facilitates automated interactions, with a Robtex server using FortiSOAR&trade; playbooks. Add the Robtex Connector as a step in FortiSOAR&trade; playbooks and perform automated operations with Robtex.</p>

### Version information

Connector Version: 1.0.0


Authored By: spryIQ.co

Certified: No
## Installing the connector
<p>From FortiSOAR&trade; 5.0.0 onwards, use the <strong>Connector Store</strong> to install the connector. For the detailed procedure to install a connector, click <a href="https://docs.fortinet.com/document/fortisoar/0.0.0/installing-a-connector/1/installing-a-connector" target="_top">here</a>.<br>You can also use the following <code>yum</code> command as a root user to install connectors from an SSH session:</p>
`yum install cyops-connector-robtex`

## Prerequisites to configuring the connector
- You must have the URL of Robtex server to which you will connect and perform automated operations and credentials to access that server.
- The FortiSOAR&trade; server should have outbound connectivity to port 443 on the Robtex server.

## Minimum Permissions Required
- N/A

## Configuring the connector
For the procedure to configure a connector, click [here](https://docs.fortinet.com/document/fortisoar/0.0.0/configuring-a-connector/1/configuring-a-connector)
### Configuration parameters
<p>In FortiSOAR&trade;, on the Connectors page, click the <strong>Robtex</strong> connector row (if you are in the <strong>Grid</strong> view on the Connectors page) and in the <strong>Configurations&nbsp;</strong> tab enter the required configuration details:&nbsp;</p>
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Server URL<br></td><td>URL of the robtex connector to access the connector website.<br>
</tbody></table>

## Actions supported by the connector
The following automated operations can be included in playbooks and you can also use the annotations to access operations from FortiSOAR&trade; release 4.10.0 and onwards:
<table border=1><thead><tr><th>Function<br></th><th>Description<br></th><th>Annotation and Category<br></th></tr></thead><tbody><tr><td>Get IP Query Details<br></td><td>Retrieved information includes the current forward and reverse of an IP number, together with GEO-location data and network data.<br></td><td>ip_query_details <br/>Investigation<br></td></tr>
<tr><td>Get Autonomous System Query Details<br></td><td>The ASN allows autonomous systems to exchange routing information with other autonomous systems.<br></td><td>autonomous_system_query_details <br/>Investigation<br></td></tr>
</tbody></table>

### operation: Get IP Query Details
#### Input parameters
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>IP Address<br></td><td>Required IP addresses whose geolocation data needs to be retrieved.<br>
</td></tr></tbody></table>

#### Output
The output contains the following populated JSON schema:
<code><br>{
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "status": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "act": [],
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "acth": [],
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "pas": [],
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "pash": [],
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "city": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "country": " ",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "as": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "asname": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "whoisdesc": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "routedesc": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "bgproute": ""
</code><code><br>}</code>

### operation: Get Autonomous System Query Details
#### Input parameters
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Autonomous System Number<br></td><td>Autonomous System Number (ASN) is a globally unique identifier that defines a group of one or more IP prefixes run by one or more network operators.<br>
</td></tr></tbody></table>

#### Output
The output contains the following populated JSON schema:
<code><br>{
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "status": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "nets": []
</code><code><br>}</code>
## Included playbooks
The `Sample - robtex - 1.0.0` playbook collection comes bundled with the Robtex connector. These playbooks contain steps using which you can perform all supported actions. You can see bundled playbooks in the **Automation** > **Playbooks** section in FortiSOAR<sup>TM</sup> after importing the Robtex connector.

- Get IP Query Details
- Get Autonomous System Query Details

**Note**: If you are planning to use any of the sample playbooks in your environment, ensure that you clone those playbooks and move them to a different collection, since the sample playbook collection gets deleted during connector upgrade and delete.
