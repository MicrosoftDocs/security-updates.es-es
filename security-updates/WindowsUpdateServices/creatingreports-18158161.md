---
TOCTitle: Creating Reports
Title: Creating Reports
ms:assetid: '1e0e5df4-dedf-4bae-bbbc-87d43f16693c'
ms:contentKeyID: 18158161
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720459(v=WS.10)'
---

Creating Reports
================

Reports enable you to monitor different aspects of the WSUS network: updates, client computers, and downstream servers. If a WSUS server has replica servers, you can choose to roll up the replica servers' client status to the upstream server. For details on creating a replica server and status rollup, see [Deploying Microsoft Windows Server Updates Services](http://go.microsoft.com/fwlink/?linkid=79983) (http://go.microsoft.com/fwlink/?linkid=79983).

You can generate different kinds of update reports from different places in the WSUS administration console.

1.  General reports on the Reports page: as described below.
2.  Reports on specific updates: right-click the update (or go to the **Actions** pane) and choose **Status Report.**
3.  Reports on specific computers: right-click the computer (or go to the **Actions** pane)and choose **Status Report**.

| ![](images/Cc720459.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Generating detailed reports for large numbers of computers and/or updates can be very memory-intensive. Detailed reports are most effective for smaller subsets of your computers or updates. If you need to create a very large report and are concerned about using CPU and memory resources on the WSUS server, you may generate the report from a remote WSUS Administration console. |

Using the Reports page
----------------------

You can generate three kinds of reports, as described in the following table.

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
  
#### Update reports
  
Update reports show you the status for your updates. You can view the report in three ways: summary, detailed, and tabular. You can also filter the report by update classification, product, target computer group, or update installation status.
  
The report displays information from the most recent contact between client computers and the WSUS server. The frequency with which client computers contact the WSUS server is configured through Group Policy. By default, this is every 22 hours. Unless you want to change the contact frequency for your client computers, generate this report the day after you approve updates, so that it reflects your latest approvals. For more information about configuring Group Policy, see [Deploying Microsoft Windows Server Updates Services](http://go.microsoft.com/fwlink/?linkid=79983) (http://go.microsoft.com/fwlink/?linkid=79983).
  
| ![](images/Cc720459.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |  
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| You can run **wuauclt /detectnow** from the command line on computers that are running WSUS client software (Automatic Updates) in order to start contact between the client computer and WSUS server). This is used primarily to update status for a particular computer. There will be a few minutes' delay between running the command and seeing the results on the WSUS server. After forcing the client to contact the server, you can get its status with an update status report. For more information about wuauclt, see [Appendix H: The wuauclt Utility](https://technet.microsoft.com/26807cd7-72c0-44b1-80f4-a39793801c45). |
  
**To run an update report**  
1.  In the WSUS administrative console, select the **Reports** node
  
2.  In the **Reports** pane, click **Update Status Summary**. This will give you an overview update report.
  
3.  In the **Updates Report** window you can configure the updates you want to see by classification, product, computer group, or update installation status.
  
4.  Click **Run Report**.
  
#### Update Status Summary view
  
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
  
You can change the view of an Update Status Summary report to a detail view or a tabular view by clicking **Report View** in the **Updates Report** toolbar.
  
#### Computer Status report
  
The Computer Status report provides an update status summary for the computers you specify.
  
**To run a status report for computers**  
1.  In the WSUS administrative console, select the **Reports** node.
  
2.  In the **Reports** pane, click **Computer Status Summary**. This will give you an overview computer report.
  
3.  In the **Computers Report** window, you can configure the updates you want to see by classification, product, computer group, or update installation status.
  
4.  Click **Run Report**.
  
You can reformat the computer status report in summary, detailed, and tabular views, as with the update status report.
  
#### Synchronization Results report
  
The Synchronization Results report enables you to see synchronization information for your server for a given time period, including errors that occurred during synchronization and a list of new updates. In addition, you can get general, status, and revision information for each new update.
  
**To run a Synchronization Results report**  
1.  In the WSUS administrative console, click **Reports**.
  
2.  On the **Reports** pane, click **Synchronization Results**. By default, the report shows any synchronizations done today.
  
3.  To change the synchronization period for the report, in the **Synchronization Report** window, click **Between these dates** and specify the dates you want included in the report.
  
4.  Click **Run Report**.
  
The report has four components, which are described in the following table.
  
### Components of Synchronization Results Report

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
<td style="border:1px solid black;"><p>Displays the updates that have been expired during the report's time period..</p></td>
</tr>
</tbody>
</table>
  
#### Printing the report
  
You can print the report in update summary, detailed, or tabular views, depending on how you have formatted the update status report.
  
**To print the update status report**  
1.  On the **Updates Report** toolbar, click the printer icon.
  
2.  In the **Print** dialog, select your options and click **Print**.
  
#### Exporting the report
  
You can print the report in its original format, or you can export it to Microsoft Excel or PDF formats.
  
| ![](images/Cc720459.Important(WS.10).gif)Importante                                                                                                                                                                                                                                                                   |  
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| Exporting a large report can be extremely time consuming. If you are planning to export your report, consider limiting the size of the report to 200 pages or fewer. You can use different filters to reduce the size of the report, or you can choose the tabular format rather than the detailed format to reduce the number of pages to export. |
  
**To export a report to Excel or PDF format**  
1.  Run the report you wish to export.
  
2.  On the **Updates Report** toolbar, click the down arrow associated with the save icon.
  
3.  You will see two options: **Excel** and **Acrobat (PDF) file**. Click one of the options.
  
Extending reports  
-----------------
  
You can customize WSUS reports in different ways:
  
1.  Use the WSUS APIs to create a custom report  
2.  Use WSUS public views to create and extend custom reports
  
#### Use WSUS APIs to create custom reports
  
For more information on WSUS APIs, see the [Windows Server Update Services SDK](http://go.microsoft.com/fwlink/?linkid=85713) documentation on MSDN (http://go.microsoft.com/fwlink/?LinkId=85713). You can use these APIs to create reports on updates, approvals, installation information, and the like.
  
#### Use WSUS public views to create custom reports
  
For more information on public views, as well as sample queries, see the [WSUS SDK conceptual documentation](http://go.microsoft.com/fwlink/?linkid=85715) on MSDN (http://go.microsoft.com/fwlink/?LinkId=85715.) If you are using SQL Server 2005 as the WSUS database, you can use the SQL Server 2005 Report Builder to generate custom reports using these views, or you can access the views from the command line. If you are using Windows Internal Database as the WSUS database, you can access it via the command line if you download the Microsoft SQL Server 2005 Command Line Query Utility and the SQL Native Client from [Microsoft Download Center](http://go.microsoft.com/fwlink/?linkid=70728) (http://go.microsoft.com/fwlink/?LinkId=70728).
