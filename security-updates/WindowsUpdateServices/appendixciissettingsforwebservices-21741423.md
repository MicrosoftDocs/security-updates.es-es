---
TOCTitle: 'Appendix C: IIS Settings for Web Services'
Title: 'Appendix C: IIS Settings for Web Services'
ms:assetid: 'b940c212-f4c4-493f-906a-29bcdc7c9186'
ms:contentKeyID: 21741423
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd939903(v=WS.10)'
---

Appendix C: IIS Settings for Web Services
=========================================

Troubleshooting WSUS Web services may be simplified if you compare your current IIS settings for the different WSUS Web services with the ones given below, which are the ones set by WSUS setup. A service may have stopped working correctly because one of these settings was changed by another installation or application.

The values of these IIS settings are sometimes represented with variable names instead of actual values. This is because the actual value may vary from one installation to another.

The variable names used in the settings, and in the instructions below, are:

-   *windir*-: The standard environment variable for the Windows directory (on Windows Server 2003, usually C:\\WINDOWS).
-   *InetpubDir*-: The IIS inetpub directory on Windows Server 2003 (usually C:\\Inetpub).
-   *WSUSInstallDir*-: The directory where WSUS is installed (usually C:\\Program Files\\Update Services).
-   *WebSiteID*-: The number IIS uses to identify Web sites (1 is the ID of the default Web site, but other Web sites are assigned random numbers).

IIS vroots
----------

The following virtual directories (vroots) are created in IIS (in the Default Web Site by default) for client-to-server synchronization, server to server synchronization, reporting, and client self-update.

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
<p>Security: Anonymous Access Enabled</p>
<p>Execute Permissions: Scripts Only</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Content</p></td>
<td style="border:1px solid black;"><p>Directory[the location of the WSUS content directory]</p>
<p>Security: Anonymous Access Enabled</p>
<p>Execute Permissions: None</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DssAuthWebService</p></td>
<td style="border:1px solid black;"><p>Directory: %ProgramFiles%Update Services\WebServices\DssAuthWebService</p>
<p>Application Pool: WsusPool</p>
<p>Security: Anonymous Access Enabled</p>
<p>Execute Permissions: Scripts Only</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Inventory</p></td>
<td style="border:1px solid black;"><p>Directory: %ProgramFiles%Update Services\ Inventory</p>
<p>Application Pool: WsusPool</p>
<p>Security: Anonymous Access Enabled</p>
<p>Execute Permissions: Scripts Only</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>ReportingWebService</p></td>
<td style="border:1px solid black;"><p>Directory: %ProgramFiles%Update Services\WebServices\ReportingWebService</p>
<p>Application Pool: WsusPool</p>
<p>Security: Anonymous Access Enabled</p>
<p>Execute Permissions: Scripts Only</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>ServerSyncWebService</p></td>
<td style="border:1px solid black;"><p>Directory: %ProgramFiles%Update Services\WebServices\ServerSyncWebService</p>
<p>Application Pool: WsusPool</p>
<p>Security: Anonymous Access Enabled</p>
<p>Execute Permissions: Scripts Only</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>SimpleAuthWebService</p></td>
<td style="border:1px solid black;"><p>Directory: %ProgramFiles%Update Services\WebServices\SimpleAuthWebService</p>
<p>Application Pool: WsusPool</p>
<p>Security: Anonymous Access Enabled</p>
<p>Execute Permissions: Scripts Only</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>ApiRemoting30</p></td>
<td style="border:1px solid black;"><p>Directory: %ProgramFiles%Update Services\Administration</p>
<p>Application Pool: WsusPool</p>
<p>Security: Integrated Windows Authentication, Digest Authentication</p>
<p>Execute Permissions: Scripts Only</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>SelfUpdate</p></td>
<td style="border:1px solid black;"><p>Directory: %ProgramFiles%Update Services\SelfUpdate</p>
<p>Security: Anonymous Access Enabled</p>
<p>Execute Permissions: Scripts Only</p></td>
</tr>
</tbody>
</table>
<p> </p>

Using the adsutil IIS utility
-----------------------------

The adsutil IIS utility can be found on your server in the Inetpub\\AdminScripts directory. For more information about using adsutil.vbs, see [Using the Adsutil.vbs Administration Script](http://go.microsoft.com/fwlink/?linkid=162432) (http://go.microsoft.com/fwlink/?LinkId=162432).

Finding Web service paths with adsutil
--------------------------------------

You can use adsutil to find the paths for different Web services on your computer with the following procedure.

**To find the paths of Web services**
1.  Open a command window.

2.  Navigate to the directory where adsutil is located: **cd %Inetpubdir%\\AdminScripts**

3.  Type the following command: **adsutil.vbs find path**

4.  If you have WSUS installed, you should see output like the following:

**Property path found at:**

**W3SVC/***WebSiteID***/ROOT**

**W3SVC/***WebSiteID***/ROOT/ApiRemoting30**

**W3SVC/***WebSiteID***/D/ROOT/ClientWebService**

**W3SVC/***WebSiteID***/ROOT/Content**

**W3SVC/***WebSiteID***/ROOT/DssAuthWebService**

**W3SVC/***WebSiteID***/ROOT/Inventory**

**W3SVC/***WebSiteID***/ROOT/ReportingWebService**

**W3SVC/***WebSiteID***/ROOT/Selfupdate**

**W3SVC/***WebSiteID***/ROOT/ServerSyncWebService**

**W3SVC/***WebSiteID***/ROOT/SimpleAuthWebService**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><img src="images/Dd939903.note(WS.10).gif" />Nota</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">If you have installed WSUS on the default Web site, <em>WebSiteID</em> will be 1, but if you have installed it on another Web site, <em>WebSiteID</em> will be a random number.
<p></p></td>
</tr>
</tbody>
</table>
<p> </p>

Checking the properties of a Web service
----------------------------------------

You can also use adsutil to find the properties of a given Web service. You will use one of the Web service paths listed above to specify the Web service you want to check. For example, if you want to check the properties of the Reporting Web service, you use the path **W3SVC/***WebSiteID***/ROOT/ReportingWebService**, where *WebSiteID* stands for the number of the WSUS Web site.

**To check the properties of a Web service**
1.  Open a command window.

2.  Navigate to the directory where adsutil is located: **cd** *Inetpubdir***\\AdminScripts**

3.  Type the following command: **adsutil.vbs enum** *WebServicePath*
    where *WebServicePath* stands for the path of the Web service you want to check.

4.  Compare the output to the standard values given in the sections below.

Global properties
-----------------

These global properties can be retrieved with the following adsutil command:

**adsutil.vbs enum W3SVC**

The properties listed below are a partial list.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Property</strong></th>
<th><strong>Value</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>KeyType</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;IIsWebService&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>MaxConnections</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 4294967295</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AnonymousUserName</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;IUSR_&lt;machinename&gt;&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>ConnectionTimeout</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 120</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AllowKeepAlive</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DefaultDoc</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;Default.htm,Default.asp,index.htm&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>CacheISAPI</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>CGITimeout</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 300</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>ContentIndexed</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DownlevelAdminInstance</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 1</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspBufferingOn</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspLogErrorRequests</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspScriptErrorSentToBrowser</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspScriptErrorMessage</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;An error occurred on the server when</p>
<p>processing the URL. Please contact the system administrator&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspAllowOutOfProcComponents</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True &gt;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspScriptFileCacheSize</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 500</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspDiskTemplateCacheDirectory</p></td>
<td style="border:1px solid black;"><p>(EXPANDSZ) &quot;%windir%\system32\inetsrv\ASP</p>
<p>Compiled Templates&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspMaxDiskTemplateCacheFiles</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 2000</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspScriptEngineCacheMax</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 250</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspScriptTimeout</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 90</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspSessionTimeout</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 20</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspEnableParentPaths</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspAllowSessionState</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspScriptLanguage</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;VBScript&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspExceptionCatchEnable</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True&lt;br&gt;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspCodepage</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 0</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspLCID</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 2048</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspQueueTimeout</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 4294967295</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspEnableAspHtmlFallback</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspEnableChunkedEncoding</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspEnableTypelibCache</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspErrorsToNTLog</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspProcessorThreadMax</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 25</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspTrackThreadingModel</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspRequestQueueMax</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 3000</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspEnableApplicationRestart</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspQueueConnectionTestTime</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 3</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspSessionMax</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 4294967295</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AppAllowDebugging</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AppAllowClientDebug</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>PasswordChangeFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 6</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthChangeUnsecure</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthChangeDisable</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthAdvNotifyDisable</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DirBrowseFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 1073741886</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>EnableDirBrowsing</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DirBrowseShowDate</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DirBrowseShowTime</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DirBrowseShowSize</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DirBrowseShowExtension</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DirBrowseShowLongDate</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>EnableDefaultDoc</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 1</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthBasic</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthAnonymous</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthNTLM</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthMD5</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthPassport</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>InProcessIsapiApps</p></td>
<td style="border:1px solid black;"><p>(LIST) (6 Items)</p>
<p>&quot;%windir%\system32\inetsrv\httpext.dll&quot;</p>
<p>&quot;%windir%\system32\inetsrv\httpodbc.dll&quot;</p>
<p>&quot;%windir%\system32\inetsrv\ssinc.dll&quot;</p>
<p>&quot;%windir%\system32\msw3prt.dll&quot;</p>
<p>&quot;%windir%\Microsoft.NET\Framework\v2.0.50727\aspnet_isapi.dll&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>LogOdbcDataSource</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;HTTPLOG&quot;&gt;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>LogOdbcTableName</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;InternetLog&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>LogOdbcUserName</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;InternetAdmin&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>WAMUserName</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;IWAM_&lt;machinename&gt;&quot;&gt;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthChangeURL</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;/iisadmpwd/achg.asp&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthExpiredURL</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;/iisadmpwd/aexp.asp&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthNotifyPwdExpURL</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;/iisadmpwd/anot.asp&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthExpiredUnsecureURL</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;/iisadmpwd/aexp3.asp&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthNotifyPwdExpUnsecureURL</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;/iisadmpwd/anot3.asp&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AppPoolId</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;DefaultAppPool&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>IIs5IsolationModeEnabled</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>MaxGlobalBandwidth</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 4294967295</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>MinFileBytesPerSec</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 240</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>LogInUTF8</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspAppServiceFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 0</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspEnableTracker</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspEnableSxs</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspUsePartition</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspKeepSessionIDSecure</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 0</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspExecuteInMTA</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 0</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>CentralBinaryLoggingEnabled</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspRunOnEndAnonymously</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspBufferingLimit</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 4194304</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspCalcLineNumber</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>ApplicationDependencies</p></td>
<td style="border:1px solid black;"><p>(LIST) (6 Items)</p>
<p>&quot;Active Server Pages;ASP&quot;</p>
<p>&quot;Internet Data Connector;HTTPODBC&quot;</p>
<p>&quot;Server Side Includes;SSINC&quot;</p>
<p>&quot;WebDAV;WEBDAV&quot;</p>
<p>&quot;ASP.NET v1.1.4322;ASP.NET v1.1.4322&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>WebSvcExtRestrictionList</p></td>
<td style="border:1px solid black;"><p>(LIST) (8 Items)</p>
<p>&quot;0,*.dll&quot;</p>
<p>&quot;0,*.exe&quot;&gt;</p>
<p>&quot;0,&lt;windir&gt;\system32\inetsrv\asp.dll,0,ASP,Active Server Pages&quot;&gt;</p>
<p>&quot;0,&lt;windir&gt;\system32\inetsrv\httpodbc.dll,0,HTTPODBC,Internet Data</p>
<p>Connector&quot;</p>
<p>&quot;0,&lt;windir&gt;\system32\inetsrv\ssinc.dll,0,SSINC,Server Side Includes&quot;</p>
<p>&quot;0,&lt;windir&gt;\system32\inetsrv\httpext.dll,0,WEBDAV,WebDAV&quot;&gt;</p>
<p>&quot;1,&lt;windir&gt;\Microsoft.NET\Framework\v2.0.50727\aspnet_isapi.dll,0,ASP.NET</p>
<p>v2.0.50727,ASP.NET v2.0.50727&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspMaxRequestEntityAllowed</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 204800</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>[/w3svc/1]</p></td>
<td style="border:1px solid black;"><p><strong>n/a</strong></p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>[/w3svc/AppPools]</p></td>
<td style="border:1px solid black;"><p><strong>n/a</strong></p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>[/w3svc/Filters]</p></td>
<td style="border:1px solid black;"><p><strong>n/a</strong></p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>[/w3svc/Info]</p></td>
<td style="border:1px solid black;"><p><strong>n/a</strong></p></td>
</tr>
</tbody>
</table>
  
Global Properties of the WWW Web site  
-------------------------------------
  
These properties can be retrieved with the following adsutil command:
  
**adsutil.vbs enum W3SVC/***WebSiteID*
  
The properties listed below comprise a partial list.
  
###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Property</strong></th>
<th><strong>Value</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>KeyType</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;IIsWebServer&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>ServerState</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 2</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>ServerComment</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;Default Web site&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>ServerSize</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 1</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>ServerBindings</p></td>
<td style="border:1px solid black;"><p>(LIST) (1 Items) &quot;:80:&quot; (or 8530)</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>SecureBindings</p></td>
<td style="border:1px solid black;"><p>(LIST) (1 Items) &quot;:443:&quot; (or 8531)</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>ConnectionTimeout</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 180</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DefaultDoc</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;Default.htm,Default.asp,index.htm,iisstart.htm&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspBufferingOn</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>LogPluginClsid</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;{FF160663-DE82-11CF-BC0A-00AA006111E0}&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Win32Error</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 0</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AppPoolId</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;DefaultAppPool&quot;</p></td>
</tr>
</tbody>
</table>
  
Properties of the API Remoting Web service  
------------------------------------------
  
###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Property</strong></th>
<th><strong>Value</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>KeyType</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;IIsWebVirtualDir&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AppRoot</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;/LM/W3SVC/<em>WebSiteID</em>/ROOT/ApiRemoting30&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AppFriendlyName</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;ApiRemoting30&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AppIsolated</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 2</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Path</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;&lt;WSUSInstallDir&gt;\WebServices\ApiRemoting30&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 513</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessExecute</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessSource</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessRead</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessWrite</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessScript</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoRemoteExecute</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessNoRemoteRead</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoRemoteWrite</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessNoRemoteScript</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoPhysicalDir</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspScriptErrorSentToBrowser</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspEnableParentPaths</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 21</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthBasic</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthAnonymous</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthNTLM</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthMD5</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthPassport</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AppPoolId</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;WsusPool&quot;</p></td>
</tr>
</tbody>
</table>
  
Properties of the Client Web service  
------------------------------------
  
###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Property</th>
<th>Value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>KeyType</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;IIsWebVirtualDir&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AppRoot</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;/LM/W3SVC/<em>WebSiteID</em>/ROOT/ClientWebService&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AppFriendlyName</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;ClientWebService&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AppIsolated</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 2</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Path</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;&lt;WSUSInstallDir&gt;\WebServices\ClientWebService&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 513</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessExecute</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessSource</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessRead</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessWrite</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessScript</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoRemoteExecute</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessNoRemoteRead</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoRemoteWrite</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessNoRemoteScript</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoPhysicalDir</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspScriptErrorSentToBrowser</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspEnableParentPaths</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 1</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthBasic</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthAnonymous</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthNTLM</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthMD5</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthPassport</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AppPoolId</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;WsusPool&quot;</p></td>
</tr>
</tbody>
</table>
  
Properties of the Downstream Server Authentication Web service  
--------------------------------------------------------------
  
###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Property</strong></th>
<th><strong>Value</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>KeyType</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;IIsWebVirtualDir&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AppRoot</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;/LM/W3SVC/<em>WebSiteID</em>/ROOT/DssAuthWebService&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AppFriendlyName</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot; DssAuthWebService &quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AppIsolated</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 2</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Path</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;&lt;WSUSInstallDir&gt;\WebServices\DssAuthWebService&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 513</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessExecute</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessSource</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessRead</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessWrite</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessScript</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoRemoteExecute</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessNoRemoteRead</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoRemoteWrite</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessNoRemoteScript</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoPhysicalDir</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspScriptErrorSentToBrowser</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspEnableParentPaths</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 1</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthBasic</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthAnonymous</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthNTLM</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthMD5</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthPassport</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AppPoolId</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;WsusPool&quot;</p></td>
</tr>
</tbody>
</table>
  
Properties of the Inventory Collection Web service  
--------------------------------------------------
  
###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Property</strong></th>
<th><strong>Value</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>KeyType</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;IIsWebVirtualDir&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AppRoot</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;/LM/W3SVC/<em>WebSiteID</em>/ROOT/Inventory&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AppFriendlyName</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;Inventory&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AppIsolated</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 2</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Path</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;&lt;WSUSInstallDir&gt;\WebServices\Inventory&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 513</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessExecute</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessSource</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessRead</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessWrite</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessScript</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoRemoteExecute</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessNoRemoteRead</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoRemoteWrite</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessNoRemoteScript</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoPhysicalDir</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspScriptErrorSentToBrowser</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspEnableParentPaths</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 1</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthBasic</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthAnonymous</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthNTLM</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthMD5</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthPassport</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AppPoolId</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;WsusPool&quot;</p></td>
</tr>
</tbody>
</table>
  
Checking the properties of the Reporting Web service  
----------------------------------------------------
  
###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Property</strong></th>
<th><strong>Value</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>KeyType</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;IIsWebVirtualDir&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AppRoot</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;/LM/W3SVC/<em>WebSiteID</em>/ROOT/ReportingWebService&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AppFriendlyName</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot; ReportingWebService &quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AppIsolated</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 2</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Path</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;&lt;WSUSInstallDir&gt;\WebServices\ReportingWebService&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 513</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessExecute</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessSource</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessRead</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessWrite</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessScript</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoRemoteExecute</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessNoRemoteRead</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoRemoteWrite</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessNoRemoteScript</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoPhysicalDir</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspScriptErrorSentToBrowser</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspEnableParentPaths</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 1</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthBasic</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthAnonymous</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthNTLM</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthMD5</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthPassport</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AppPoolId</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;WsusPool&quot;</p></td>
</tr>
</tbody>
</table>
  
Properties of the Selfupdate Web service  
----------------------------------------
  
###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Property</strong></th>
<th><strong>Value</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>KeyType</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;IIsWebVirtualDir&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Path</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;&lt;WSUSInstallDir&gt;\WebServices\ServerSyncWebService&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 513</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessExecute</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessSource</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessRead</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessWrite</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessScript</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessNoRemoteExecute</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoRemoteRead</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessNoRemoteWrite</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoRemoteScript</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessNoPhysicalDir</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
</tbody>
</table>
  
Properties of the Server Synchronization Web service  
----------------------------------------------------
  
###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Property</strong></th>
<th><strong>Value</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>KeyType</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;IIsWebVirtualDir&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AppRoot</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;/LM/W3SVC/<em>WebSiteID</em>/ROOT/ServerSyncWebService&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AppFriendlyName</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot; ServerSyncWebService &quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AppIsolated</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 2</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Path</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;&lt;WSUSInstallDir&gt;\WebServices\ServerSyncWebService&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 513</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessExecute</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessSource</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessRead</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessWrite</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessScript</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoRemoteExecute</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessNoRemoteRead</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoRemoteWrite</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessNoRemoteScript</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoPhysicalDir</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspScriptErrorSentToBrowser</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspEnableParentPaths</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 1</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthBasic</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthAnonymous</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthNTLM</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthMD5</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthPassport</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AppPoolId</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;WsusPool&quot;</p></td>
</tr>
</tbody>
</table>
  
Properties of the Simple Authorization Web service  
--------------------------------------------------
  
###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Property</strong></th>
<th><strong>Value</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>KeyType</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;IIsWebVirtualDir&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AppRoot</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;/LM/W3SVC/<em>WebSiteID</em>/ROOT/SimpleAuthWebService&quot;</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AppFriendlyName</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;SimpleAuthWebService&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AppIsolated</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 2</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Path</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;&lt;WSUSInstallDir&gt;\WebServices\SimpleAuthWebService&quot;</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 513</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessExecute</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessSource</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessRead</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessWrite</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessScript</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoRemoteExecute</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessNoRemoteRead</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoRemoteWrite</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AccessNoRemoteScript</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AccessNoPhysicalDir</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AspScriptErrorSentToBrowser</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AspEnableParentPaths</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthFlags</p></td>
<td style="border:1px solid black;"><p>(INTEGER) 1</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthBasic</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthAnonymous</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) True</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthNTLM</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AuthMD5</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>AuthPassport</p></td>
<td style="border:1px solid black;"><p>(BOOLEAN) False</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>AppPoolId</p></td>
<td style="border:1px solid black;"><p>(STRING) &quot;WsusPool&quot;</p></td>
</tr>
</tbody>
</table>
