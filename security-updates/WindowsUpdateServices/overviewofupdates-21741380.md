---
TOCTitle: Overview of Updates
Title: Overview of Updates
ms:assetid: '7ff77123-01bb-4047-9ce6-fab29c86686c'
ms:contentKeyID: 21741380
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd939871(v=WS.10)'
---

Overview of Updates
===================

Updates are used for updating or providing a full file replacement for software that is installed on a computer. Every update that is available on Microsoft Update is made up of two components:

-   Metadata: Provides information about the update. For example, metadata supplies information for the properties of an update, thus enabling you to find out for what the update is useful. Metadata also includes Microsoft Software License Terms. The metadata package downloaded for an update is typically much smaller than the actual update file package.
-   Update files: The actual files required to install an update on a computer.

How WSUS Stores Updates
-----------------------

When updates are synchronized to your WSUS server, the metadata and update files are stored in two separate locations. Metadata is stored in the WSUS database. Update files can be stored either on your WSUS server or on Microsoft Update servers, depending on how you have configured your synchronization options. If you choose to store update files on Microsoft Update servers, only metadata is downloaded at the time of synchronization; you approve the updates through the WSUS console, and then client computers get the update files directly from Microsoft Update at the time of installation. For more information about your options for storing updates, see the [WSUS Deployment Guide](http://go.microsoft.com/fwlink/?linkid=139832) (http://go.microsoft.com/fwlink/?LinkId=139832).

Managing Updates with WSUS
--------------------------

You will be setting up and running synchronizations, adding computers and computer groups, and deploying updates on a regular basis. The following list gives examples of general tasks you might undertake in updating computers with WSUS.

1.  Determine an overall update management plan based on your network topology and bandwidth, company needs, and organizational structure. Considerations might include the following:
    -   Whether to set up a hierarchy of WSUS servers, and how the hierarchy should be structured.
    -   Which database to use for update metadata (for example, Windows® Internal Database, SQL Server 2005).
    -   What computer groups to create, and how to assign computers to them (server-side or client-side targeting).
    -   Whether updates should be synchronized automatically, and at what time.
2.  Set synchronization options, such as update source, product and update classification, language, connection settings, storage location, and synchronization schedule.
3.  Get the updates and associated metadata on your WSUS server through synchronization from either Microsoft Update or an upstream WSUS server.
4.  Approve or decline updates. You have the option of allowing users to install the updates themselves (if they are local administrators on their client computers).
5.  Configure automatic approvals. You can also configure whether you want to enable automatic approval of revisions to existing updates or approve revisions manually. If you choose to approve revisions manually, then your WSUS server will continue using the older version until you manually approve the new revision.
6.  Check the status of updates. You can view update status, print a status report, or configure e-mail for regular status reports.

Update Products and Classifications
-----------------------------------

Updates available on Microsoft Update are differentiated by product (or product family) and classification.

### Products Updated by WSUS

A product is a specific edition of an operating system or application, for example Windows Server 2003. A product family is the base operating system or application from which the individual products are derived. An example of a product family is Microsoft Windows, of which Windows Server 2003 is a member. You can select the products or product families for which you want your server to synchronize updates. You can specify a product family or individual products within the family. Selecting any product or product family will get updates for current and future versions of the product.

### Update Classifications

Update classifications represent the type of update. For any given product or product family, updates could be available among multiple update classifications (for example, Windows XP family Critical Updates and Security Updates). The following table lists update classifications.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Update Classification</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Critical updates</p></td>
<td style="border:1px solid black;"><p>Broadly released fixes for specific problems addressing critical, non-security related bugs.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Definition updates</p></td>
<td style="border:1px solid black;"><p>Updates to virus or other definition files.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Drivers</p></td>
<td style="border:1px solid black;"><p>Software components designed to support new hardware.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Feature packs</p></td>
<td style="border:1px solid black;"><p>New feature releases, usually rolled into products at the next release.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Security updates</p></td>
<td style="border:1px solid black;"><p>Broadly released fixes for specific products, addressing security issues.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Service packs</p></td>
<td style="border:1px solid black;"><p>Cumulative sets of all hotfixes, security updates, critical updates, and updates created since the release of the product. Service packs might also contain a limited number of customer-requested design changes or features.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Tools</p></td>
<td style="border:1px solid black;"><p>Utilities or features that aid in accomplishing a task or set of tasks.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Update rollups</p></td>
<td style="border:1px solid black;"><p>Cumulative set of hotfixes, security updates, critical updates, and updates packaged together for easy deployment. A rollup generally targets a specific area, such as security, or a specific component, such as Internet Information Services (IIS).</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Updates</p></td>
<td style="border:1px solid black;"><p>Broadly released fixes for specific problems addressing non-critical, non-security related bugs.</p></td>
</tr>
</tbody>
</table>
