---
TOCTitle: Issues with BITS
Title: Issues with BITS
ms:assetid: '22c0533b-927a-4ace-9f5a-815879446c99'
ms:contentKeyID: 18158187
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720473(v=WS.10)'
---

Issues with BITS
================

Background Intelligent Transfer Service (BITS) is the service used by WSUS to download updates from Microsoft Update to the main WSUS server, as well as from WSUS servers to their clients. BITS also supports the transfer of files between peer computers in a domain.

Some download issues may be caused by problems with running BITS on the server or client computers. When you are troubleshooting download problems, after you have verified that all WSUS settings are correct on both the server and its clients, you should ensure that BITS is running properly on all affected computers.

BITS provides a downloadable tool called bitsadmin that allows you to verify and change BITS settings. For more information about the bitsadmin utility, see [BITSAdmin Tool](http://go.microsoft.com/fwlink/?linkid=80934) (http://go.microsoft.com/fwlink/?LinkId=80934). This tool is available as part of the Windows Vista operating system, and also as part of the Windows XP Service Pack 2 Support Tools.

Finding BITS
------------

        ```
        ```
        ```

Stopping and restarting BITS
----------------------------

Often it is possible to resolve BITS issues simply by stopping the service and restarting it. The following procedure shows how to stop and restart the service from the command line. You must be logged on as a local administrator to stop and restart BITS.

| ![](images/Cc720473.note(WS.10).gif)Nota        |
|------------------------------------------------------------------------------|
| To modify, stop, or restart BITS, you must be logged on as an administrator. |

**To stop and restart BITS**
1.  Open a command shell.

2.  Type **sc stop bits**

3.  Type **sc start bits**

Troubleshooting BITS download issues
------------------------------------

The following sections are an incomplete list of possible problems with BITS configuration. To get more information about BITS, see [Background Intelligent Transfer Service](http://go.microsoft.com/fwlink/?linkid=81083) (http://go.microsoft.com/fwlink/?LinkId=81083).

#### The BITS service must run under the Local System user account

By default BITS runs under the LocalSystem account.

**To configure the service to run under the correct account**
1.  Open a command shell.

    Type: `sc config bits obj= LocalSystem`

    (note that a space must occur between `obj=` and `LocalSystem`)

2.  Verify that output from the command is:

    \[SC\] ChangeServiceConfig SUCCESS

3.  Stop and restart BITS.

#### Proxy servers must support HTTP 1.1 RANGE requests

-   BITS supports HTTP and HTTPS downloads and uploads and requires that the server support the HTTP 1.1 protocol. For downloads, the HTTP server's HEAD method must return the file size, and its GET method must support the Content-Range and Content-Length headers. BITS can use an HTTP/1.0 server as long as it meets the HEAD and GET method requirements (MIME headers must include the standard Content-Range and Content-Type headers plus a maximum of 180 bytes of other headers, and a maximum of two CR/LF characters may occur between the HTTP headers and the first boundary string).

#### There is a mismatch between the BITS per-user job limit and the per-computer job limit

**To detect or correct a mismatch between the per-user job limit and the per-computer job limit specified through Group Policy**
1.  Run gpedit.msc, if the policy is specified locally; if the policy is a domain policy edit the Group Policy object with GPMC.

2.  In the Group Policy Object Editor, navigate to Computer Configuration\\Administrative Templates\\Network\\Background Intelligent Transfer Service (BITS).

3.  Ensure that the setting "Maximum number of BITS jobs for each user" is set to a lower value than the setting "Maximum number of BITS jobs for this computer"

4.  Type **gpupdate /force**

5.  Stop and restart BITS.

6.  Verify that there are no errors in the event logs.

#### BITS jobs are failing

If BITS jobs fail, look in the event log to find errors. You can use the following table to diagnose the cause of the errors.

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
<th><strong>Error name</strong></th>
<th><strong>Error code</strong></th>
<th><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>E_INVALIDARG</p></td>
<td style="border:1px solid black;"><p>0x80070057</p></td>
<td style="border:1px solid black;"><p>An incorrect proxy server name was specified in the user’s Internet Explorer proxy settings. This error is also seen when credentials are supplied for authentication schemes that are not NTLM/Negotiate, but the user name or password is null. Change the user’s IE settings to be a valid proxy server or Change the credentials not to be NULL user name/password for schemes other than NTLM/Negotiate.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>ERROR_WINHTTP_NAME_NOT_RESOLVED</p></td>
<td style="border:1px solid black;"><p>0x80072ee7</p></td>
<td style="border:1px solid black;"><p>The server/proxy could not be resolved by BITS. Internet Explorer on the same machine in the context of the job owner would see the same problem. Try downloading the same file via the web browser using the context of the job owner.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>ERROR_HTTP_INVALID_SERVER_RESPONSE</p></td>
<td style="border:1px solid black;"><p>0x80072f78</p></td>
<td style="border:1px solid black;"><p>This is a transient error and the job will continue downloading.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>BG_E_INSUFFICIENT_RANGE_SUPPORT</p></td>
<td style="border:1px solid black;"><p>0x80200013</p></td>
<td style="border:1px solid black;"><p>BITS uses range headers in HTTP requests to request parts of a file. If the server or proxy server doesn’t understand Range requests and returns the full file instead of the requested range, BITS puts the job into the ERROR state with this error. Capture the network traffic during the error and examine if HTTP GET requests with “Range” header are getting valid responses. Check proxy servers to ensure that they are configured correctly to support Range requests.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>BG_E_MISSING_FILE_SIZE</p></td>
<td style="border:1px solid black;"><p>0x80200011</p></td>
<td style="border:1px solid black;"><p>When BITS sends a HEAD request and the server/proxy does not return Content-Length header in the response, BITS puts the job in ERROR state with this error. Check the proxy server and WSUS server to ensure that they are configured correctly. Some versions of the Apache 2.0 proxy server are known to exhibit this behavior.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>BG_E_HTTP_ERROR_403</p></td>
<td style="border:1px solid black;"><p>0x80190193</p></td>
<td style="border:1px solid black;"><p>When the server returns HTTP 403 response in any of the requests, BITS puts the job in ERROR state with this error code. HTTP 403 corresponds to “Forbidden: Access is denied.&quot; Check access permissions for the account running the job.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>ERROR_NOT_LOGGED_ON</p></td>
<td style="border:1px solid black;"><p>0x800704dd</p></td>
<td style="border:1px solid black;"><p>The SENS service is not receiving user logon notifications. BITS (version 2.0 and up) depends on logon notifications from Service Control Manager, which in turn depends on the SENS service. Ensure that the SENS service is started and running correctly.</p></td>
</tr>
</tbody>
</table>
  
#### BITS fails to start
  
If the BITS service fail to start, use the following table to diagnose the cause of the error.
  
###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>ERROR_SERVICE_DOES_NOT_EXIST</p></td>
<td style="border:1px solid black;"><p>0x80070424</p></td>
<td style="border:1px solid black;"><p>See the section on repairing the BITS configuration below.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>ERROR_SERVICE_NOT_IN_EXE</p></td>
<td style="border:1px solid black;"><p>0x8007043B</p></td>
<td style="border:1px solid black;"><p>BITS is not listed as one of the services in the netsvcs svchost group (does not apply to Windows 2000).</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>ERROR_SERVICE_DISABLED</p></td>
<td style="border:1px solid black;"><p>0x80070422</p></td>
<td style="border:1px solid black;"><p>BITS has been disabled. Enable the BITS service.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>ERROR_SERVICE_DEPENDENCY_DELETED ERROR_SERVICE_DEPENDENCY_FAIL</p></td>
<td style="border:1px solid black;"><p>0x80070433, 0x8007042c</p></td>
<td style="border:1px solid black;"><p>A service appearing in the BITS service dependency list cannot be started. Make sure the dependency list for the BITS service is correct:</p>
<ul>
<li>Windows Vista: RpcSs, EventSystem (also http.sys and LanManWorkstation when peercaching is enabled)<br />
<br />
</li>
<li>Windows Server 2003: Rpcss, EventSystem<br />
<br />
</li>
<li>Windows XP: Rpcss<br />
<br />
</li>
<li>Windows 2000: Rpcss, SENS, Wmi<br />
<br />
</li>
</ul></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>ERROR_PATH_NOT_FOUND</p></td>
<td style="border:1px solid black;"><p>0x80070003</p></td>
<td style="border:1px solid black;"><p>Pre-Windows Vista: %ALLUSERSPROFILE%\Microsoft\Network doesn’t exist</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>ERROR_FILE_NOT_FOUND</p></td>
<td style="border:1px solid black;"><p>0x80070002</p></td>
<td style="border:1px solid black;"><p>The “Parameters” key is missing. Ensure that the following keys and values exist: HKLM\SYSTEM\CurrentControlSet\Services\BITS\Parameters\ServiceDll= %SystemRoot%\System32\qmgr.dll</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>REGDB_E_CLASSNOTREG, EVENT_E_INTERNALERROR</p></td>
<td style="border:1px solid black;"><p>0x80040154, 0x80040206</p></td>
<td style="border:1px solid black;"><p>BITS for Windows 2000 is dependent on SENS and EventSystem services. If the COM+ catalog is corrupted, BITS may fail with this error code. See KB article Q315296 for details.</p></td>
</tr>
</tbody>
</table>
  
#### Repairing a corrupted BITS configuration
  
To repair corrupted BITS service configuration, you can enter the BITS service configuration manually.
  
| ![](images/Cc720473.Important(WS.10).gif)Importante                                                                                       |  
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| This action should only be taken in circumstances where all other troubleshooting attempts have failed. You must be an administrator to modify the BITS configuration. |
  
**To repair a corrupted BITS configuration**  
1.  Open a command shell.
  
2.  Type:
  
    Sc config bits binpath=”%systemroot%\\system32\\svchost.exe –k netsvcs“ Sc config bits depend = RpcSs EventSystem
  
    Sc config bits start=delayed-auto
  
    Sc config bits type=interact
  
    Sc config bits error=normal
  
    Sc config bits obj=LocalSystem
  
    Sc privs bits privileges=SeCreateGlobalPrivilege/SeImpersonatePrivilege/SeTcbPrivilege/SeAssignPrimaryTokenPrivilege/SeIncreateQuotaPrivilege
  
    Sc sidtype bits type= unrestricted
  
    Sc failure bits reset= 86400 actions=restart/60000/restart/120000
  
3.  Stop and restart BITS.
