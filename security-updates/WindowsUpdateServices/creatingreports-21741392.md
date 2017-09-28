---
TOCTitle: Creating Reports
Title: Creating Reports
ms:assetid: 'b78c9652-a5de-4c5a-9668-ad4157720a9d'
ms:contentKeyID: 21741392
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd939891(v=WS.10)'
---

Creating Reports
================

Reports enable you to monitor different aspects of the WSUS network: updates, client computers, and downstream servers. If a WSUS server has replica servers, you can choose to roll up the replica servers' client status to the upstream server. For information about creating a replica server and status rollup, see the [WSUS Deployment Guide](http://go.microsoft.com/fwlink/?linkid=139832) (http://go.microsoft.com/fwlink/?LinkId=139832).

You can generate different kinds of update reports from different places in the WSUS administration console.

1.  General reports on the Reports page.
2.  Reports on specific updates: right-click the update (or go to the **Actions** pane) and choose **Status Report.**
3.  Reports on specific computers: right-click the computer (or go to the **Actions** pane) and choose **Status Report**.

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><img src="images/Dd939891.note(WS.10).gif" />Nota</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Generating detailed reports for large numbers of computers and/or updates can be very memory-intensive. Detailed reports are most effective for smaller subsets of your computers or updates. If you need to create a very large report and are concerned about using CPU and memory resources on the WSUS server, you may generate the report from a remote WSUS Administration console.
<p></p></td>
</tr>
</tbody>
</table>
<p> </p>

Using the Reports Page
----------------------

You can generate three kinds of reports as described in the following table.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Report name</th>
<th>Function</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Update Reports</p></td>
<td style="border:1px solid black;"><p>View update status.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Computer Reports</p></td>
<td style="border:1px solid black;"><p>View computer status.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Synchronization Reports</p></td>
<td style="border:1px solid black;"><p>View the results of the last synchronization.</p></td>
</tr>
</tbody>
</table>
  
### Update Reports
  
Update reports show you the status of your updates. You can run update reports in four ways: summary, detailed, tabular, and tabular for approved updates. You can also filter an update report by update classification, product, target computer group, and update installation status.
  
The report displays information from the most recent contact between client computers and the WSUS server. The frequency with which client computers contact the WSUS server is configured through Group Policy. By default, this is every 22 hours. Unless you want to change the contact frequency for your client computers, generate this report the day after you approve updates, so that it reflects your latest approvals.

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><img src="images/Dd939891.note(WS.10).gif" />Nota</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">You can run <strong>wuauclt /detectnow</strong> from the command prompt on computers that are running WSUS client software (Automatic Updates) in order to start contact between the client computer and WSUS server. This is used primarily to update status for a particular computer. There will be a few minutes delay between running the command and seeing the results on the WSUS server. After forcing the client to contact the server, you can get its status with an update status report. For more information about wuauclt, see <a href="https://technet.microsoft.com/7cc1c5f9-5678-4bb4-a7a6-18939dcc120c">Appendix H: The wuauclt Utility</a>.
<p></p></td>
</tr>
</tbody>
</table>
<p> </p>

**To run an update report**
1.  In the WSUS Administration console, select the **Reports** node

2.  In the **Reports** pane, click one of the options in the **Update Reports** section: **Update Status Summary**, **Update Detailed Status**, **Update Tabular Status**, or **Update Tabular Status for Approved Updates**.

3.  In the **Updates Report** window you can select the updates you want to see by classification, product, computer group, and update installation status.

4.  Click **Run Report**. See the [Terminology for Update Status](https://technet.microsoft.com/d10ba0c8-8d94-4bc5-a82d-bc8872e68667) section for information about the Status values shown on the report.

5.  You can change the view of an Update report to a detail, summary, or tabular view by clicking **Report View** in the **Updates Report** toolbar.

#### Update Status Summary View

The Update Status Summary view contains the elements listed in the following table.

### Description of elements displayed in the Update Status Summary view

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Column name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Updates Report tree view</p></td>
<td style="border:1px solid black;"><p>The tree listing all the updates in the report.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Title</p></td>
<td style="border:1px solid black;"><p>The title of the update.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Description</p></td>
<td style="border:1px solid black;"><p>The description of the update.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Classification</p></td>
<td style="border:1px solid black;"><p>The classification of the update.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Products</p></td>
<td style="border:1px solid black;"><p>The products to which the update applies.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>MSRC Severity Rating</p></td>
<td style="border:1px solid black;"><p>Microsoft Security Response Center rating.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>MSRC Number</p></td>
<td style="border:1px solid black;"><p>Microsoft Security Response Center identification number.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>More information</p></td>
<td style="border:1px solid black;"><p>Redirection to the relevant Web site.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Approval Summary for Computer Group</p></td>
<td style="border:1px solid black;"><p>The listing of groups and approvals.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Group</p></td>
<td style="border:1px solid black;"><p>The computer group.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Approval</p></td>
<td style="border:1px solid black;"><p>Approval status (Approved, Not approved, Declined).</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Deadline</p></td>
<td style="border:1px solid black;"><p>The date by which the update must be installed.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Administrator</p></td>
<td style="border:1px solid black;"><p>The administrative action.</p></td>
</tr>
</tbody>
</table>
  
### Computer Reports
  
Computer reports show you the status of computers. You can run computer reports in four ways: summary, detailed, tabular, and tabular for approved updates. You can also filter a computer report by update classification, product, target computer group, and update installation status.
  
**To run a status report for computers**  
1.  In the WSUS administrative console, select the **Reports** node.
  
2.  In the **Reports** pane, click one of the options in the **Computer Reports** section: **Computer Status Summary**, **Computer Detailed Status**, **Computer Tabular Status**, or **Computer Tabular Status for Approved Updates**.
  
3.  In the **Computers Report** window, you can select the updates you want to see by classification, product, computer group, and update installation status.
  
    Note that for the **Computer Tabular Status for Approved Updates** report both the update approvals and the set of computers considered by the report are scoped based on the selected target group.
  
    -   The updates considered by the report are those for which the selected target group has a direct or inherited approval for install.  
    -   The computers considered by the report are those that are direct members of the selected target group, and optionally its child target groups.
  
4.  Click **Run Report**.
  
5.  You can change the view of a Computer report to a detail, summary, or tabular view by clicking **Report View** in the **Updates Report** toolbar.
  
### Synchronization Results Report
  
The Synchronization Results report enables you to see synchronization information for the WSUS server for a given time period, including errors that occurred during synchronization and a list of new updates. In addition, you can get general, status, and revision information for each new update.
  
**To run a Synchronization Results report**  
1.  In the WSUS administrative console, click **Reports**.
  
2.  On the **Reports** pane, click **Synchronization Results**. By default, the report shows any synchronization done today.
  
3.  To change the synchronization period for the report, in the **Synchronization Report** window, click **Between these dates** and specify the dates you want included in the report.
  
4.  Click **Run Report**.
  
The report has four components, which are described in the following table.
  
### Components of the Synchronization Results Report

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Component name</th>
<th>Purpose</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Report Options</p></td>
<td style="border:1px solid black;"><p>Shows the start and end dates of the period shown in the report, as well as the date of the report and the server for which the report was made.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Synchronization Summary</p></td>
<td style="border:1px solid black;"><p>Displays summary information of the numbers of new, revised, and expired updates in each synchronization.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>New Updates</p></td>
<td style="border:1px solid black;"><p>Displays the new updates that have been synchronized to the WSUS server during the report's time period.</p>
<p>You can view the properties for each update by clicking the update. An update status report will be generated for that individual report.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Revised Updates</p></td>
<td style="border:1px solid black;"><p>Displays the revised updates that have been synchronized to the WSUS server during the report's time period.</p>
<p>You can view the properties for each update by clicking the update. An update status report will be generated for that individual report.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Expired Updates</p></td>
<td style="border:1px solid black;"><p>Displays the updates that have been expired during the report's time period.</p></td>
</tr>
</tbody>
</table>
  
#### Printing a Report
  
You can print the report in update summary, detailed, or tabular views, depending on how you have formatted the update status report.
  
**To print a report**  
1.  On the report toolbar, click the printer icon.
  
2.  In the **Print** dialog, select your options and click **Print**.
  
#### Exporting a Report
  
You can print a report in its original format, or you can export it to Microsoft Excel or PDF formats.

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><img src="images/Dd939891.Important(WS.10).gif" />Importante</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Exporting a large report can be extremely time-consuming and may exceed your computer's memory resources. If you are planning to export a report, consider limiting the size of the report to 200 pages or fewer. You can use different filters to reduce the size of the report, or you can choose the tabular format rather than the detailed format to reduce the number of pages to export.
<p></p></td>
</tr>
</tbody>
</table>
<p> </p>

**To export a report to Excel or PDF format**
1.  Run the report you want to export.

2.  On the report toolbar, click the down arrow associated with the **Save** icon.

3.  You will see two options: **Excel** and **Acrobat (PDF) file**. Click one of the options.

Extending Reports
-----------------

You can customize WSUS reports in different ways:

1.  Use the WSUS APIs to create a custom report
2.  Use WSUS public views to create and extend custom reports

#### Use WSUS APIs to Create Custom Reports

For more information on WSUS APIs, see the [Windows Server Update Services SDK](http://go.microsoft.com/fwlink/?linkid=85713) documentation on MSDN (http://go.microsoft.com/fwlink/?LinkId=85713). You can use these APIs to create reports on updates, approvals, installation information, and the like.

#### Use WSUS Public Views to Create Custom Reports

For more information on public views, as well as sample queries, see the [WSUS SDK conceptual documentation](http://go.microsoft.com/fwlink/?linkid=85715) on MSDN (http://go.microsoft.com/fwlink/?LinkId=85715.) If you are using SQL Server as the WSUS database, you can use the SQL Server Report Builder to generate custom reports using these views, or you can access the views from the command line. If you are using Windows Internal Database as the WSUS database, you can access it via the command line if you download the Microsoft SQL Server Command Line Query Utility and the SQL Native Client. You can download the install packages from the [Microsoft Download Center](http://go.microsoft.com/fwlink/?linkid=70728) (http://go.microsoft.com/fwlink/?LinkId=70728).
