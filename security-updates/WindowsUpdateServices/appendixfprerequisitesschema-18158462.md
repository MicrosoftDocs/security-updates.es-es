---
TOCTitle: 'Appendix F: Prerequisites Schema'
Title: 'Appendix F: Prerequisites Schema'
ms:assetid: 'b79857ab-5037-47bc-bca9-65c3a755e4f5'
ms:contentKeyID: 18158462
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708561(v=WS.10)'
---

Appendix F: Prerequisites Schema
================================

The prerequisites.xml file is used to define the prerequisites for an installation. The schema is described in the following section

Prerequisites Schema
--------------------

The elements of the prerequisites schema are listed in the following table.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Schema Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>PrereqResults</p></td>
<td style="border:1px solid black;"><p>Root element.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Result</p></td>
<td style="border:1px solid black;"><p>The result of a single prerequisite check. There may be 0…<em>n</em><strong>Result</strong> elements, one for each prerequisite.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Status</p></td>
<td style="border:1px solid black;"><p>The localized description of the status code.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Check</p></td>
<td style="border:1px solid black;"><p>The product or component to be checked.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Components</p></td>
<td style="border:1px solid black;"><p>The component(s) for which this is a prerequisite. There may be 0…<em>n</em><strong>Component</strong> elements in a Components element.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Component</p></td>
<td style="border:1px solid black;"><p>One of the component(s) for which this is a prerequisite.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Description</p></td>
<td style="border:1px solid black;"><p>The description of the problem.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Resolution</p></td>
<td style="border:1px solid black;"><p>The way the customer may resolve the problem.</p></td>
</tr>
</tbody>
</table>
  
In addition, the **Result** element has an attribute **StatusCode**. The possible values of **StatusCode** are 0 (success), 1 (error), 2 (warning).
  
#### Example
  
The following is an example of a prerequisites.xml file.
  
```  
&lt;?xml version="1.0" encoding="utf-8"?&gt; &lt;PrereqResults&gt; &lt;Result StatusCode="0"&gt; &lt;Status&gt;Passed&lt;/Status&gt; &lt;Check&gt; Microsoft Windows Server 2003 Server &lt;/Check&gt; &lt;Components&gt; &lt;Component&gt;Windows Server Update Services&lt;/Component&gt; &lt;/Components&gt; &lt;/Result&gt; &lt;Result StatusCode="1"&gt; &lt;Status&gt;Failed&lt;/Status&gt; &lt;Check&gt;SQL Server 2005&lt;/Check&gt; &lt;Components&gt; &lt;Component&gt;Windows Server Update Services&lt;/Component&gt; &lt;/Components&gt; &lt;Description&gt;SQL Server 2005 or later not detected&lt;/Description&gt; &lt;Resolution&gt;Download the required version from http://www.microsoft.com/downloads/&lt;/Resolution&gt; &lt;/Result&gt; &lt;Result StatusCode="1"&gt; &lt;Status&gt;Warning&lt;/Status&gt; &lt;Check&gt;SQLINSTANCE\_NAME&lt;/Check&gt; &lt;Components&gt; &lt;Component&gt;Windows Server Update Services&lt;/Component&gt; &lt;/Components&gt; &lt;Description&gt;This database version can not be upgraded. Version is too old.&lt;/Description&gt; &lt;Resolution&gt;Choose another location for the database to keep this one otherwise this database will be overridden.&lt;/Resolution&gt; &lt;/Result&gt; … &lt;/PrereqResults&gt;  
```
