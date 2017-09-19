---
TOCTitle: Verifying WSUS Server Settings
Title: Verifying WSUS Server Settings
ms:assetid: 'aae0c0a0-0bc7-46f8-b3ea-bc441a3796b4'
ms:contentKeyID: 18158445
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708545(v=WS.10)'
---

Verifying WSUS Server Settings
==============================

This topic covers typical WSUS Server settings.

Settings for Update File Synchronization and Download
-----------------------------------------------------

This section covers the following issues which affect update file synchronization and download:

-   Registry settings
-   Configuration settings
-   IIS settings
-   Permissions

| ![](images/Cc708545.Important(WS.10).gif)Importante                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| These settings are configured during WSUS setup by default. They are listed here as a reference, to use as checkpoints when troubleshooting. When troubleshooting, you can verify that these settings are in place. |

#### Registry settings

Following are registry settings configured during setup on the WSUS server. These settings do not store server configuration information. All configuration information is stored in the WSUS database (SUSDB.mdf).

All of the following Registry entries are within the **\\HKLM\\Software\\Microsoft\\Update Services\\Server\\Setup** Registry key:

-   **ContentDir** – the location under which update binaries and end user license agreement files are stored. If the user chose to install WMSDE during setup, this location also contains the database storage files and log files; for example, C:\\WSUS. Note the following:
    -   **&lt;ContentDir&gt;\\WsusContent** contains the update files
    -   **&lt;ContentDir&gt;\\MSSQL$WSUS** contains the database files (if WMSDE)
-   **TargetDir** – the product installation location; for example, C:\\Program Files\\Update Services
-   **WmsdeInstalled** – this entry specifies whether or not WMSDE was used in the original installation; for example, 1=yes, 0=no. Note: This key does not get modified if your later migrate the WMSDE database to a full SQL Server database.
-   **SqlServerName** – The main registry key used under regular server operation. This is used to bootstrap the server components with the database server where the rest of data and server configuration is used. Ex: %computername%\\WSUS for WMSDE. Use this key to quickly figure out which SQL server the WSUS server is using (especially in the remote SQL case).
-   **SqlDatabaseName** – the name of the database. For WSUS 2.0, this is always SUSDB.
-   **SqlAuthenticationMode** – the authentication mode WSUS uses to talk to the database server. For WSUS 2.0, this is always WindowsAuthentication.

#### Configuration settings

All of the following server configuration settings are stored inside the WSUS database (SUSDB.mdf).

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>What is configured</th>
<th>Database storage location</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Update Storage</p></td>
<td style="border:1px solid black;"><p><em>tbConfigurationA.SyncToMu</em></p>
<p><em>tbConfigurationA.UpstreamServerName</em></p></td>
<td style="border:1px solid black;"><p>The first database location specifies the update source for client computers. The values possible are:</p>
<p>0 – WSUS server</p>  
<p>1 – Microsoft Update</p>
<p>The second database location specifies the name of the upstream WSUS server, if you have chosen one as the update source.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Express (PSF) file download</p></td>
<td style="border:1px solid black;"><p><em>tbConfigurationC.DownloadExpressPackages</em></p></td>
<td style="border:1px solid black;"><p>This setting controls whether or not express installation files are downloaded. The values possible are:</p>
<p>0 – Do not download express files (default) option.</p>  
<p>1 – Download express files.</p>
<p>On the WSUS console, this is configured on the Advanced Synchronization Options box.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Language options</p></td>
<td style="border:1px solid black;"><p><em>tbLanguage.Enabled</em></p></td>
<td style="border:1px solid black;"><p>This setting controls which language binaries are to be downloaded. By default, all languages are enabled.</p>
<p>On the WSUS console this is configured on the Advanced Synchronization Options box.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>BITS download priority</p></td>
<td style="border:1px solid black;"><p><em>tbConfigurationC.BitsDownloadPriorityForeground</em></p></td>
<td style="border:1px solid black;"><p>This internal setting specifies whether or not to use foreground priority for BITS downloads. The default is to use throttled downloads. This setting was added to handle issues with certain proxy servers that did not correctly handle HTTP 1.1 restartable downloads.</p></td>
</tr>  
</tbody>  
</table>
  
IIS settings  
------------
  
The following virtual directories (vroots) are created in IIS (in the Default Web Site by default) for client to server synchronization, server to server synchronization, reporting, and client self-update.
  
###  

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th>Vroot in IIS</th>  
<th>Properties</th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>ClientWebService</p></td>
<td style="border:1px solid black;"><p>Directory: %ProgramFiles%Update Services\WebServices\ClientWebService</p>
<p>Application Pool: WsusPool</p>  
<p>Security: Anonymous Access Enabled.</p>
<p>Execute Permissions: Scripts Only</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Content</p></td>
<td style="border:1px solid black;"><p>Directory: e:\wsus\wsuscontent</p>
<p>Security: Anonymous Access Enabled</p>
<p>Execute Permissions: None</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DssAuthWebService</p></td>
<td style="border:1px solid black;"><p>Directory: %ProgramFiles%Update Services\WebServices\DssAuthWebService</p>
<p>Application Pool: WsusPool</p>  
<p>Security: Anonymous Access Enabled.</p>
<p>Execute Permissions: Scripts Only</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>ReportingWebService</p></td>
<td style="border:1px solid black;"><p>Directory: %ProgramFiles%Update Services\WebServices\ReportingWebService</p>
<p>Application Pool: WsusPool</p>  
<p>Security: Anonymous Access Enabled.</p>
<p>Execute Permissions: Scripts Only</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>ServerSyncWebService</p></td>
<td style="border:1px solid black;"><p>Directory: %ProgramFiles%Update Services\WebServices\ServerSyncWebService</p>
<p>Application Pool: WsusPool</p>  
<p>Security: Anonymous Access Enabled.</p>
<p>Execute Permissions: Scripts Only</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>SimpleAuthWebService</p></td>
<td style="border:1px solid black;"><p>Directory: %ProgramFiles%Update Services\WebServices\SimpleAuthWebService</p>
<p>Application Pool: WsusPool</p>  
<p>Security: Anonymous Access Enabled.</p>
<p>Execute Permissions: Scripts Only</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>WSUSAdmin</p></td>
<td style="border:1px solid black;"><p>Directory: %ProgramFiles%Update Services\Administration</p>
<p>Application Pool: WsusPool</p>  
<p>Security: Integrated Windows Authentication.</p>
<p>Execute Permissions: Scripts Only</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>SelfUpdate</p></td>
<td style="border:1px solid black;"><p>Directory: %ProgramFiles%Update Services\SelfUpdate</p>
<p>Security: Anonymous Access Enabled, Integrated Windows Authentication.</p>
<p>Execute Permissions: Scripts Only</p></td>
</tr>
</tbody>
</table>
<p> </p>

#### Permissions

The following lists permissions necessary for specific folders on the WSUS server disk and registry permissions.

#### Disk

The following permissions are configured during WSUS setup, and are important for BITS downloads to work:

-   The root folder on the drive where the **WSUSContent** folder resides (for example, **&lt;%windir%&gt;**\\WSUS\\WSUSContent) must have **Read** permissions for either the **Users** account or the **NT Authority\\Network Service** account (on Windows 2003). If this permission is not set, BITS downloads will fail. Note: this is the permission that WSUS setup does not configure, so make sure the permissions are set as described here
-   The WSUS content directory, usually **&lt;%windir%&gt;\\WSUS\\WSUSContent** must have **Full Control** permission granted to the **NT Authority\\Network Service** account. This permission is set by WSUS server setup when it creates the directory, but it is possible that your security software might reset this. permission. Not having this permission set will also cause BITS downloads to fail.
-   The **NT Authority\\Network Service** account (on Windows 2003) must have **Full Control** permissions to the following folders for the WSUS console to display the pages correctly:
    -   **&lt;%windir%&gt;\\Microsoft .NET\\Framework\\v1.1.4322\\Temporary ASP.NET Files**
    -   **&lt;%windir%&gt;\\Temp**

#### Registry

The following permissions are set for the Registry during WSUS setup.

-   The **Users** group must have Read access to the **\\HKLM\\Software\\Microsoft\\Update Services\\Server** Registry key.
-   The following accounts must have Full Control permissions to the **\\HKLM\\Software\\Microsoft\\Update Services\\Server\\Setup** Registry key:
    -   **ASP.NET**
    -   **Network Service** (for Windows Server 2003)
    -   **WSUS Administrators**
