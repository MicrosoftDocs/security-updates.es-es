---
TOCTitle: 'Appendix G: Windows Update Agent Result Codes'
Title: 'Appendix G: Windows Update Agent Result Codes'
ms:assetid: '061d0423-f7f1-401e-9ef7-b7d02cd50b7a'
ms:contentKeyID: 18158153
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720442(v=WS.10)'
---

Appendix G: Windows Update Agent Result Codes
=============================================

The Windows Update Agent uses the following set of result codes.

Windows Update Agent result codes
---------------------------------

The tables in this section show the result code (hexadecimal value), the corresponding string, and the description.

The following table shows WUA success codes.

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
<th>Result Code</th>
<th>Result String</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>0x240001</p></td>
<td style="border:1px solid black;"><p>WU_S_SERVICE_STOP</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent was stopped successfully.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x240002</p></td>
<td style="border:1px solid black;"><p>WU_S_SELFUPDATE</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent updated itself.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x240003</p></td>
<td style="border:1px solid black;"><p>WU_S_UPDATE_ERROR</p></td>
<td style="border:1px solid black;"><p>Operation completed successfully but there were errors applying the updates..</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x240004</p></td>
<td style="border:1px solid black;"><p>WU_S_MARKED_FOR_DISCONNECT</p></td>
<td style="border:1px solid black;"><p>A callback was marked to be disconnected later because the request to disconnect the operation came while a callback was executing.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x240005</p></td>
<td style="border:1px solid black;"><p>WU_S_REBOOT_REQUIRED</p></td>
<td style="border:1px solid black;"><p>The system must be restarted to complete installation of the update.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x240006</p></td>
<td style="border:1px solid black;"><p>WU_S_ALREADY_INSTALLED</p></td>
<td style="border:1px solid black;"><p>The update to be installed is already installed on the system.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x240007</p></td>
<td style="border:1px solid black;"><p>WU_S_ALREADY_UNINSTALLED</p></td>
<td style="border:1px solid black;"><p>The update to be removed is not installed on the system.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x240008</p></td>
<td style="border:1px solid black;"><p>WU_S_ALREADY_DOWNLOADED</p></td>
<td style="border:1px solid black;"><p>The update to be downloaded has already been downloaded.</p></td>
</tr>  
</tbody>  
</table>
  
The following table shows WUA error codes.
  
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
<th>Result Code</th>  
<th>Result String</th>  
<th>Description</th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240001</p></td>
<td style="border:1px solid black;"><p>WU_E_NO_SERVICE</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent was unable to provide the service.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240002</p></td>
<td style="border:1px solid black;"><p>WU_E_MAX_CAPACITY_REACHED</p></td>
<td style="border:1px solid black;"><p>The maximum capacity of the service was exceeded.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240003</p></td>
<td style="border:1px solid black;"><p>WU_E_UNKNOWN_ID</p></td>
<td style="border:1px solid black;"><p>An ID cannot be found.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240004</p></td>
<td style="border:1px solid black;"><p>WU_E_NOT_INITIALIZED</p></td>
<td style="border:1px solid black;"><p>The object could not be initialized.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240005</p></td>
<td style="border:1px solid black;"><p>WU_E_RANGEOVERLAP</p></td>
<td style="border:1px solid black;"><p>The update handler requested a byte range overlapping a previously requested range.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240006</p></td>
<td style="border:1px solid black;"><p>WU_E_TOOMANYRANGES</p></td>
<td style="border:1px solid black;"><p>The requested number of byte ranges exceeds the maximum number (2^31 - 1).</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240007</p></td>
<td style="border:1px solid black;"><p>WU_E_INVALIDINDEX</p></td>
<td style="border:1px solid black;"><p>The index to a collection was invalid.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240008</p></td>
<td style="border:1px solid black;"><p>WU_E_ITEMNOTFOUND</p></td>
<td style="border:1px solid black;"><p>The key for the item queried could not be found.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240009</p></td>
<td style="border:1px solid black;"><p>WU_E_OPERATIONINPROGRESS</p></td>
<td style="border:1px solid black;"><p>Another conflicting operation was in progress. Some operations such as installation cannot be performed twice simultaneously.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024000A</p></td>
<td style="border:1px solid black;"><p>WU_E_COULDNOTCANCEL</p></td>
<td style="border:1px solid black;"><p>Cancellation of the operation was not allowed.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024000B</p></td>
<td style="border:1px solid black;"><p>WU_E_CALL_CANCELLED</p></td>
<td style="border:1px solid black;"><p>Operation was cancelled.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024000C</p></td>
<td style="border:1px solid black;"><p>WU_E_NOOP</p></td>
<td style="border:1px solid black;"><p>No operation was required.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024000D</p></td>
<td style="border:1px solid black;"><p>WU_E_XML_MISSINGDATA</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent could not find required information in the update's XML data.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024000E</p></td>
<td style="border:1px solid black;"><p>WU_E_XML_INVALID</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent found invalid information in the update's XML data.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024000F</p></td>
<td style="border:1px solid black;"><p>WU_E_CYCLE_DETECTED</p></td>
<td style="border:1px solid black;"><p>Circular update relationships were detected in the metadata.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240010</p></td>
<td style="border:1px solid black;"><p>WU_E_TOO_DEEP_RELATION</p></td>
<td style="border:1px solid black;"><p>Update relationships too deep to evaluate were evaluated.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240011</p></td>
<td style="border:1px solid black;"><p>WU_E_INVALID_RELATIONSHIP</p></td>
<td style="border:1px solid black;"><p>An invalid update relationship was detected.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240012</p></td>
<td style="border:1px solid black;"><p>WU_E_REG_VALUE_INVALID</p></td>
<td style="border:1px solid black;"><p>An invalid registry value was read.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240013</p></td>
<td style="border:1px solid black;"><p>WU_E_DUPLICATE_ITEM</p></td>
<td style="border:1px solid black;"><p>Operation tried to add a duplicate item to a list.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240016</p></td>
<td style="border:1px solid black;"><p>WU_E_INSTALL_NOT_ALLOWED</p></td>
<td style="border:1px solid black;"><p>Operation tried to install while another installation was in progress or the system was pending a mandatory restart.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240017</p></td>
<td style="border:1px solid black;"><p>WU_E_NOT_APPLICABLE</p></td>
<td style="border:1px solid black;"><p>Operation was not performed because there are no applicable updates.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240018</p></td>
<td style="border:1px solid black;"><p>WU_E_NO_USERTOKEN</p></td>
<td style="border:1px solid black;"><p>Operation failed because a required user token is missing.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240019</p></td>
<td style="border:1px solid black;"><p>WU_E_EXCLUSIVE_INSTALL_CONFLICT</p></td>
<td style="border:1px solid black;"><p>An exclusive update cannot be installed with other updates at the same time.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024001A</p></td>
<td style="border:1px solid black;"><p>WU_E_POLICY_NOT_SET</p></td>
<td style="border:1px solid black;"><p>A policy value was not set.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024001B</p></td>
<td style="border:1px solid black;"><p>WU_E_SELFUPDATE_IN_PROGRESS</p></td>
<td style="border:1px solid black;"><p>The operation could not be performed because the Windows Update Agent is self-updating.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024001D</p></td>
<td style="border:1px solid black;"><p>WU_E_INVALID_UPDATE</p></td>
<td style="border:1px solid black;"><p>An update contains invalid metadata.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024001E</p></td>
<td style="border:1px solid black;"><p>WU_E_SERVICE_STOP</p></td>
<td style="border:1px solid black;"><p>Operation did not complete because the service or system was being shut down.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024001F</p></td>
<td style="border:1px solid black;"><p>WU_E_NO_CONNECTION</p></td>
<td style="border:1px solid black;"><p>Operation did not complete because the network connection was unavailable.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240020</p></td>
<td style="border:1px solid black;"><p>WU_E_NO_INTERACTIVE_USER</p></td>
<td style="border:1px solid black;"><p>Operation did not complete because there is no logged-on interactive user.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240021</p></td>
<td style="border:1px solid black;"><p>WU_E_TIME_OUT</p></td>
<td style="border:1px solid black;"><p>Operation did not complete because it timed out.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240022</p></td>
<td style="border:1px solid black;"><p>WU_E_ALL_UPDATES_FAILED</p></td>
<td style="border:1px solid black;"><p>Operation failed for all the updates.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240023</p></td>
<td style="border:1px solid black;"><p>WU_E_EULAS_DECLINED</p></td>
<td style="border:1px solid black;"><p>The license terms for all updates were declined.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240024</p></td>
<td style="border:1px solid black;"><p>WU_E_NO_UPDATE</p></td>
<td style="border:1px solid black;"><p>There are no updates.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240025</p></td>
<td style="border:1px solid black;"><p>WU_E_USER_ACCESS_DISABLED</p></td>
<td style="border:1px solid black;"><p>Group Policy settings prevented access to Windows Update.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240026</p></td>
<td style="border:1px solid black;"><p>WU_E_INVALID_UPDATE_TYPE</p></td>
<td style="border:1px solid black;"><p>The type of update is invalid.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240027</p></td>
<td style="border:1px solid black;"><p>WU_E_URL_TOO_LONG</p></td>
<td style="border:1px solid black;"><p>The URL exceeded the maximum length.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240028</p></td>
<td style="border:1px solid black;"><p>WU_E_UNINSTALL_NOT_ALLOWED</p></td>
<td style="border:1px solid black;"><p>The update could not be uninstalled because the request did not originate from a WSUS server.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240029</p></td>
<td style="border:1px solid black;"><p>WU_E_INVALID_PRODUCT_LICENSE</p></td>
<td style="border:1px solid black;"><p>Search may have missed some updates before there is an unlicensed application on the system.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024002A</p></td>
<td style="border:1px solid black;"><p>WU_E_MISSING_HANDLER</p></td>
<td style="border:1px solid black;"><p>A component required to detect applicable updates was missing.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024002B</p></td>
<td style="border:1px solid black;"><p>WU_E_LEGACYSERVER</p></td>
<td style="border:1px solid black;"><p>An operation did not complete because it requires a newer version of server.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024002C</p></td>
<td style="border:1px solid black;"><p>WU_E_BIN_SOURCE_ABSENT</p></td>
<td style="border:1px solid black;"><p>A delta-compressed update could not be installed because it required the source.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024002D</p></td>
<td style="border:1px solid black;"><p>WU_E_SOURCE_ABSENT</p></td>
<td style="border:1px solid black;"><p>A full-file update could not be installed because it required the source.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024002E</p></td>
<td style="border:1px solid black;"><p>WU_E_WU_DISABLED</p></td>
<td style="border:1px solid black;"><p>Access to an unmanaged server is not allowed.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024002F</p></td>
<td style="border:1px solid black;"><p>WU_E_CALL_CANCELLED_BY_POLICY</p></td>
<td style="border:1px solid black;"><p>Operation did not complete because the DisableWindowsUpdateAccess policy was set.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240030</p></td>
<td style="border:1px solid black;"><p>WU_E_INVALID_PROXY_SERVER</p></td>
<td style="border:1px solid black;"><p>The format of the proxy list was invalid.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240031</p></td>
<td style="border:1px solid black;"><p>WU_E_INVALID_FILE</p></td>
<td style="border:1px solid black;"><p>The file is in the wrong format.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240032</p></td>
<td style="border:1px solid black;"><p>WU_E_INVALID_CRITERIA</p></td>
<td style="border:1px solid black;"><p>The search criteria string was invalid.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240033</p></td>
<td style="border:1px solid black;"><p>WU_E_EULA_UNAVAILABLE</p></td>
<td style="border:1px solid black;"><p>License terms could not be downloaded.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240034</p></td>
<td style="border:1px solid black;"><p>WU_E_DOWNLOAD_FAILED</p></td>
<td style="border:1px solid black;"><p>Update failed to download.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240035</p></td>
<td style="border:1px solid black;"><p>WU_E_UPDATE_NOT_PROCESSED</p></td>
<td style="border:1px solid black;"><p>The update was not processed.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240036</p></td>
<td style="border:1px solid black;"><p>WU_E_INVALID_OPERATION</p></td>
<td style="border:1px solid black;"><p>The object's current state did not allow the operation.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240037</p></td>
<td style="border:1px solid black;"><p>WU_E_NOT_SUPPORTED</p></td>
<td style="border:1px solid black;"><p>The functionality for the operation is not supported.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240038</p></td>
<td style="border:1px solid black;"><p>WU_E_WINHTTP_INVALID_FILE</p></td>
<td style="border:1px solid black;"><p>The downloaded file has an unexpected content type.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240039</p></td>
<td style="border:1px solid black;"><p>WU_E_TOO_MANY_RESYNC</p></td>
<td style="border:1px solid black;"><p>Agent is asked by server to resync too many times.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240040</p></td>
<td style="border:1px solid black;"><p>WU_E_NO_SERVER_CORE_SUPPORT</p></td>
<td style="border:1px solid black;"><p>WUA API method does not run on Server Core installation.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240041</p></td>
<td style="border:1px solid black;"><p>WU_E_SYSPREP_IN_PROGRESS</p></td>
<td style="border:1px solid black;"><p>Service is not available while sysprep is running.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80240042</p></td>
<td style="border:1px solid black;"><p>WU_E_UNKNOWN_SERVICE</p></td>
<td style="border:1px solid black;"><p>The update service is no longer registered with AU.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80240FFF</p></td>
<td style="border:1px solid black;"><p>WU_E_UNEXPECTED</p></td>
<td style="border:1px solid black;"><p>An operation failed due to reasons not covered by another error code.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80241001</p></td>
<td style="border:1px solid black;"><p>WU_E_MSI_WRONG_VERSION</p></td>
<td style="border:1px solid black;"><p>Search may have missed some updates because the Windows Installer is less than version 3.1.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80241002</p></td>
<td style="border:1px solid black;"><p>WU_E_MSI_NOT_CONFIGURED</p></td>
<td style="border:1px solid black;"><p>Search may have missed some updates because the Windows Installer is not configured.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80241003</p></td>
<td style="border:1px solid black;"><p>WU_E_MSP_DISABLED</p></td>
<td style="border:1px solid black;"><p>Search may have missed some updates because policy has disabled Windows Installer patching.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80241004</p></td>
<td style="border:1px solid black;"><p>WU_E_MSI_WRONG_APP_CONTEXT</p></td>
<td style="border:1px solid black;"><p>An update could not be applied because the application is installed per-user.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80241FFF</p></td>
<td style="border:1px solid black;"><p>WU_E_MSP_UNEXPECTED</p></td>
<td style="border:1px solid black;"><p>Search may have missed some updates because there was a failure of the Windows Installer.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80242000</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_REMOTEUNAVAILABLE</p></td>
<td style="border:1px solid black;"><p>A request for a remote update handler could not be completed because no remote process is available.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80242001</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_LOCALONLY</p></td>
<td style="border:1px solid black;"><p>A request for a remote update handler could not be completed because the handler is local only.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80242002</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_UNKNOWNHANDLER</p></td>
<td style="border:1px solid black;"><p>A request for an update handler could not be completed because the handler could not be recognized.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80242003</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_REMOTEALREADYACTIVE</p></td>
<td style="border:1px solid black;"><p>A remote update handler could not be created because one already exists.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80242004</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_DOESNOTSUPPORTACTION</p></td>
<td style="border:1px solid black;"><p>A request for the handler to install (uninstall) an update could not be completed because the update does not support install (uninstall).</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80242005</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_WRONGHANDLER</p></td>
<td style="border:1px solid black;"><p>An operation did not complete because the wrong handler was specified.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80242006</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_INVALIDMETADATA</p></td>
<td style="border:1px solid black;"><p>A handler operation could not be completed because the update contains invalid metadata.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80242007</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_INSTALLERHUNG</p></td>
<td style="border:1px solid black;"><p>An operation could not be completed because the installer exceeded the time limit.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80242008</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_OPERATIONCANCELLED</p></td>
<td style="border:1px solid black;"><p>An operation being done by the update handler was cancelled.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80242009</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_BADHANDLERXML</p></td>
<td style="border:1px solid black;"><p>An operation could not be completed because the handler-specific metadata is invalid.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024200A</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_CANREQUIREINPUT</p></td>
<td style="border:1px solid black;"><p>A request to the handler to install an update could not be completed because the update requires user input.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024200B</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_INSTALLERFAILURE</p></td>
<td style="border:1px solid black;"><p>The installer failed to install (uninstall) one or more updates.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024200C</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_FALLBACKTOSELFCONTAINED</p></td>
<td style="border:1px solid black;"><p>The update handler should download self-contained content rather than delta-compressed content for the update.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024200D</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_NEEDANOTHERDOWNLOAD</p></td>
<td style="border:1px solid black;"><p>The update handler did not install the update because it needs to be downloaded again.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024200E</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_NOTIFYFAILURE</p></td>
<td style="border:1px solid black;"><p>The update handler failed to send notification of the status of the install (uninstall) operation.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024200F</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_INCONSISTENT_FILE_NAMES</p></td>
<td style="border:1px solid black;"><p>The file names contained in the update metadata and in the update package are inconsistent.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80242010</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_FALLBACKERROR</p></td>
<td style="border:1px solid black;"><p>The update handler failed to fall back to the self-contained content.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80242011</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_TOOMANYDOWNLOADREQUESTS</p></td>
<td style="border:1px solid black;"><p>The update handler has exceeded the maximum number of download requests.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80242012</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_UNEXPECTEDCBSRESPONSE</p></td>
<td style="border:1px solid black;"><p>The update handler has received an unexpected response from CBS.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80242013</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_BADCBSPACKAGEID</p></td>
<td style="border:1px solid black;"><p>The update metadata contains an invalid CBS package identifier.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80242014</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_POSTREBOOTSTILLPENDING</p></td>
<td style="border:1px solid black;"><p>he post-reboot operation for the update is still in progress.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80242015</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_POSTREBOOTRESULTUNKNOWN</p></td>
<td style="border:1px solid black;"><p>The result of the post-reboot operation for the update could not be determined.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80242016</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_POSTREBOOTUNEXPECTEDSTATE</p></td>
<td style="border:1px solid black;"><p>The state of the update after its post-reboot operation has completed is unexpected.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80242017</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_NEW_SERVICING_STACK_REQUIRED</p></td>
<td style="border:1px solid black;"><p>The operating system servicing stack must be updated before this update is downloaded or installed.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80242FFF</p></td>
<td style="border:1px solid black;"><p>WU_E_UH_UNEXPECTED</p></td>
<td style="border:1px solid black;"><p>An update handler error not covered by another WU_E_UH_* code.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80243001</p></td>
<td style="border:1px solid black;"><p>WU_E_INSTALLATION_RESULTS_UNKNOWN_VERSION</p></td>
<td style="border:1px solid black;"><p>The results of download and installation could not be read from the registry due to an unrecognized data format version.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80243002</p></td>
<td style="border:1px solid black;"><p>WU_E_INSTALLATION_RESULTS_INVALID_DATA</p></td>
<td style="border:1px solid black;"><p>The results of download and installation could not be read from the registry due to an invalid data format.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80243003</p></td>
<td style="border:1px solid black;"><p>WU_E_INSTALLATION_RESULTS_NOT_FOUND</p></td>
<td style="border:1px solid black;"><p>The results of download and installation are not available; the operation may have failed to start.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80243004</p></td>
<td style="border:1px solid black;"><p>WU_E_TRAYICON_FAILURE</p></td>
<td style="border:1px solid black;"><p>A failure occurred when trying to create an icon in the taskbar notification area.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80243FFD</p></td>
<td style="border:1px solid black;"><p>WU_E_NON_UI_MODE</p></td>
<td style="border:1px solid black;"><p>Unable to show UI when in non-UI mode; WU client UI modules may not be installed.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80243FFE</p></td>
<td style="border:1px solid black;"><p>WU_E_WUCLTUI_UNSUPPORTED_VERSION</p></td>
<td style="border:1px solid black;"><p>Unsupported version of WU client UI exported functions.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80243FFF</p></td>
<td style="border:1px solid black;"><p>WU_E_AUCLIENT_UNEXPECTED</p></td>
<td style="border:1px solid black;"><p>There was a user interface error not covered by another WU_E_AUCLIENT_* error code.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244000</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SOAPCLIENT_BASE</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SOAPCLIENT_* error codes map to the SOAPCLIENT_ERROR enum of the ATL Server Library.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244001</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SOAPCLIENT_INITIALIZE</p></td>
<td style="border:1px solid black;"><p>SOAPCLIENT_INITIALIZE_ERROR - initialization of the SOAP client failed, possibly because of an MSXML installation failure.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244002</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SOAPCLIENT_OUTOFMEMORY</p></td>
<td style="border:1px solid black;"><p>SOAPCLIENT_OUTOFMEMORY - SOAP client failed because it ran out of memory.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244003</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SOAPCLIENT_GENERATE</p></td>
<td style="border:1px solid black;"><p>SOAPCLIENT_GENERATE_ERROR - SOAP client failed to generate the request.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244004</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SOAPCLIENT_CONNECT</p></td>
<td style="border:1px solid black;"><p>SOAPCLIENT_CONNECT_ERROR - SOAP client failed to connect to the server.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244005</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SOAPCLIENT_SEND</p></td>
<td style="border:1px solid black;"><p>SOAPCLIENT_SEND_ERROR - SOAP client failed to send a message for reasons of WU_E_WINHTTP_* error codes.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244006</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SOAPCLIENT_SERVER</p></td>
<td style="border:1px solid black;"><p>SOAPCLIENT_SERVER_ERROR - SOAP client failed because there was a server error.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244007</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SOAPCLIENT_SOAPFAULT</p></td>
<td style="border:1px solid black;"><p>SOAPCLIENT_SOAPFAULT - SOAP client failed because there was a SOAP fault for reasons of WU_E_PT_SOAP_* error codes.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244008</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SOAPCLIENT_PARSEFAULT</p></td>
<td style="border:1px solid black;"><p>SOAPCLIENT_PARSEFAULT_ERROR - SOAP client failed to parse a SOAP fault.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244009</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SOAPCLIENT_READ</p></td>
<td style="border:1px solid black;"><p>SOAPCLIENT_READ_ERROR - SOAP client failed while reading the response from the server.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024400A</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SOAPCLIENT_PARSE</p></td>
<td style="border:1px solid black;"><p>SOAPCLIENT_PARSE_ERROR - SOAP client failed to parse the response from the server.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024400B</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SOAP_VERSION</p></td>
<td style="border:1px solid black;"><p>SOAP_E_VERSION_MISMATCH - SOAP client found an unrecognizable namespace for the SOAP envelope.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024400C</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SOAP_MUST_UNDERSTAND</p></td>
<td style="border:1px solid black;"><p>SOAP_E_MUST_UNDERSTAND - SOAP client was unable to understand a header.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024400D</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SOAP_CLIENT</p></td>
<td style="border:1px solid black;"><p>SOAP_E_CLIENT - SOAP client found the message was malformed; fix before resending.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024400E</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SOAP_SERVER</p></td>
<td style="border:1px solid black;"><p>SOAP_E_SERVER - The SOAP message could not be processed due to a server error; resend later.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024400F</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_WMI_ERROR</p></td>
<td style="border:1px solid black;"><p>There was an unspecified Windows Management Instrumentation (WMI) error.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244010</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_EXCEEDED_MAX_SERVER_TRIPS</p></td>
<td style="border:1px solid black;"><p>The number of round trips to the server exceeded the maximum limit.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244011</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SUS_SERVER_NOT_SET</p></td>
<td style="border:1px solid black;"><p>WUServer policy value is missing in the registry.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244012</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_DOUBLE_INITIALIZATION</p></td>
<td style="border:1px solid black;"><p>Initialization failed because the object was already initialized.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244013</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_INVALID_COMPUTER_NAME</p></td>
<td style="border:1px solid black;"><p>The computer name could not be determined.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244015</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_REFRESH_CACHE_REQUIRED</p></td>
<td style="border:1px solid black;"><p>The reply from the server indicates that the server was changed or the cookie was invalid; refresh the state of the internal cache and retry.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244016</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_HTTP_STATUS_BAD_REQUEST</p></td>
<td style="border:1px solid black;"><p>HTTP 400 - the server could not process the request due to invalid syntax.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244017</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_HTTP_STATUS_DENIED</p></td>
<td style="border:1px solid black;"><p>HTTP 401 - the requested resource requires user authentication.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244018</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_HTTP_STATUS_FORBIDDEN</p></td>
<td style="border:1px solid black;"><p>HTTP 403 - server understood the request, but declined to fulfill it.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244019</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_HTTP_STATUS_NOT_FOUND</p></td>
<td style="border:1px solid black;"><p>HTTP 404 - the server cannot find the requested URI (Uniform Resource Identifier).</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024401A</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_HTTP_STATUS_BAD_METHOD</p></td>
<td style="border:1px solid black;"><p>HTTP 405 - the HTTP method is not allowed.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024401B</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_HTTP_STATUS_PROXY_AUTH_REQ</p></td>
<td style="border:1px solid black;"><p>HTTP 407 - proxy authentication is required.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024401C</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_HTTP_STATUS_REQUEST_TIMEOUT</p></td>
<td style="border:1px solid black;"><p>HTTP 408 - the server timed out waiting for the request.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024401D</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_HTTP_STATUS_CONFLICT</p></td>
<td style="border:1px solid black;"><p>HTTP 409 - the request was not completed due to a conflict with the current state of the resource.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024401E</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_HTTP_STATUS_GONE</p></td>
<td style="border:1px solid black;"><p>HTTP 410 - requested resource is no longer available at the server.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024401F</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_HTTP_STATUS_SERVER_ERROR</p></td>
<td style="border:1px solid black;"><p>HTTP 500 - an error internal to the server prevented fulfilling the request.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244020</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_HTTP_STATUS_NOT_SUPPORTED</p></td>
<td style="border:1px solid black;"><p>HTTP 501 - server does not support the functionality required to fulfill the request.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244021</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_HTTP_STATUS_BAD_GATEWAY</p></td>
<td style="border:1px solid black;"><p>HTTP 502 - the server, while acting as a gateway or proxy, received an invalid response from the upstream server it accessed in attempting to fulfill the request.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244022</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_HTTP_STATUS_SERVICE_UNAVAIL</p></td>
<td style="border:1px solid black;"><p>HTTP 503 - the service is temporarily overloaded.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244023</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_HTTP_STATUS_GATEWAY_TIMEOUT</p></td>
<td style="border:1px solid black;"><p>HTTP 504 - the request was timed out waiting for a gateway.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244024</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_HTTP_STATUS_VERSION_NOT_SUP</p></td>
<td style="border:1px solid black;"><p>HTTP 505 - the server does not support the HTTP protocol version used for the request.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244025</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_FILE_LOCATIONS_CHANGED</p></td>
<td style="border:1px solid black;"><p>Operation failed due to a changed file location; refresh internal state and resend.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244026</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_REGISTRATION_NOT_SUPPORTED</p></td>
<td style="border:1px solid black;"><p>Operation failed because Windows Update Agent does not support registration with a non-WSUS server.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244027</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_NO_AUTH_PLUGINS_REQUESTED</p></td>
<td style="border:1px solid black;"><p>The server returned an empty authentication information list.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244028</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_NO_AUTH_COOKIES_CREATED</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent was unable to create any valid authentication cookies.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244029</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_INVALID_CONFIG_PROP</p></td>
<td style="border:1px solid black;"><p>A configuration property value was wrong.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024402A</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_CONFIG_PROP_MISSING</p></td>
<td style="border:1px solid black;"><p>A configuration property value was missing.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024402B</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_HTTP_STATUS_NOT_MAPPED</p></td>
<td style="border:1px solid black;"><p>The HTTP request could not be completed and the reason did not correspond to any of the WU_E_PT_HTTP_* error codes.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024402C</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_WINHTTP_NAME_NOT_RESOLVED</p></td>
<td style="border:1px solid black;"><p>ERROR_WINHTTP_NAME_NOT_RESOLVED - the proxy server or target server name cannot be resolved.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024402F</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_ECP_SUCCEEDED_WITH_ERRORS</p></td>
<td style="border:1px solid black;"><p>External cab file processing completed with some errors.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244030</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_ECP_INIT_FAILED</p></td>
<td style="border:1px solid black;"><p>The external cab processor initialization did not complete.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244031</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_ECP_INVALID_FILE_FORMAT</p></td>
<td style="border:1px solid black;"><p>The format of a metadata file was invalid.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244032</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_ECP_INVALID_METADATA</p></td>
<td style="border:1px solid black;"><p>External cab processor found invalid metadata.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244033</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_ECP_FAILURE_TO_EXTRACT_DIGEST</p></td>
<td style="border:1px solid black;"><p>The file digest could not be extracted from an external cab file.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244034</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_ECP_FAILURE_TO_DECOMPRESS_CAB_FILE</p></td>
<td style="border:1px solid black;"><p>An external cab file could not be decompressed.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80244035</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_ECP_FILE_LOCATION_ERROR</p></td>
<td style="border:1px solid black;"><p>External cab processor was unable to get file locations.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80244FFF</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_UNEXPECTED</p></td>
<td style="border:1px solid black;"><p>A communication error not covered by another WU_E_PT_* error code</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80245001</p></td>
<td style="border:1px solid black;"><p>WU_E_REDIRECTOR_LOAD_XML</p></td>
<td style="border:1px solid black;"><p>The redirector XML document could not be loaded into the DOM class.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80245002</p></td>
<td style="border:1px solid black;"><p>WU_E_REDIRECTOR_S_FALSE</p></td>
<td style="border:1px solid black;"><p>The redirector XML document is missing some required information.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80245003</p></td>
<td style="border:1px solid black;"><p>WU_E_REDIRECTOR_ID_SMALLER</p></td>
<td style="border:1px solid black;"><p>The redirector ID in the downloaded redirector cab is less than in the cached cab.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024502D</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_SAME_REDIR_ID</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent failed to download a redirector cabinet file with a new redirector ID value from the server during the recovery.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024502E</p></td>
<td style="border:1px solid black;"><p>WU_E_PT_NO_MANAGED_RECOVER</p></td>
<td style="border:1px solid black;"><p>A redirector recovery action did not complete because the server is managed.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80245FFF</p></td>
<td style="border:1px solid black;"><p>WU_E_REDIRECTOR_UNEXPECTED</p></td>
<td style="border:1px solid black;"><p>The redirector failed for reasons not covered by another WU_E_REDIRECTOR_* error code.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80246001</p></td>
<td style="border:1px solid black;"><p>WU_E_DM_URLNOTAVAILABLE</p></td>
<td style="border:1px solid black;"><p>A download manager operation could not be completed because the requested file does not have a URL.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80246002</p></td>
<td style="border:1px solid black;"><p>WU_E_DM_INCORRECTFILEHASH</p></td>
<td style="border:1px solid black;"><p>A download manager operation could not be completed because the file digest was not recognized.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80246003</p></td>
<td style="border:1px solid black;"><p>WU_E_DM_UNKNOWNALGORITHM</p></td>
<td style="border:1px solid black;"><p>A download manager operation could not be completed because the file metadata requested an unrecognized hash algorithm.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80246004</p></td>
<td style="border:1px solid black;"><p>WU_E_DM_NEEDDOWNLOADREQUEST</p></td>
<td style="border:1px solid black;"><p>An operation could not be completed because a download request is required from the download handler.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80246005</p></td>
<td style="border:1px solid black;"><p>WU_E_DM_NONETWORK</p></td>
<td style="border:1px solid black;"><p>A download manager operation could not be completed because the network connection was unavailable.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80246006</p></td>
<td style="border:1px solid black;"><p>WU_E_DM_WRONGBITSVERSION</p></td>
<td style="border:1px solid black;"><p>A download manager operation could not be completed because the version of Background Intelligent Transfer Service (BITS) is incompatible.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80246007</p></td>
<td style="border:1px solid black;"><p>WU_E_DM_NOTDOWNLOADED</p></td>
<td style="border:1px solid black;"><p>The update has not been downloaded.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80246008</p></td>
<td style="border:1px solid black;"><p>WU_E_DM_FAILTOCONNECTTOBITS</p></td>
<td style="border:1px solid black;"><p>A download manager operation failed because the download manager was unable to connect the Background Intelligent Transfer Service (BITS).</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80246009</p></td>
<td style="border:1px solid black;"><p>WU_E_DM_BITSTRANSFERERROR</p></td>
<td style="border:1px solid black;"><p>A download manager operation failed because there was an unspecified Background Intelligent Transfer Service (BITS) transfer error.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024600a</p></td>
<td style="border:1px solid black;"><p>WU_E_DM_DOWNLOADLOCATIONCHANGED</p></td>
<td style="border:1px solid black;"><p>A download must be restarted because the location of the source of the download has changed.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024600B</p></td>
<td style="border:1px solid black;"><p>WU_E_DM_CONTENTCHANGED</p></td>
<td style="border:1px solid black;"><p>A download must be restarted because the update content changed in a new revision.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80246FFF</p></td>
<td style="border:1px solid black;"><p>WU_E_DM_UNEXPECTED</p></td>
<td style="border:1px solid black;"><p>There was a download manager error not covered by another WU_E_DM_* error code.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80247001</p></td>
<td style="border:1px solid black;"><p>WU_E_OL_INVALID_SCANFILE</p></td>
<td style="border:1px solid black;"><p>An operation could not be completed because the scan package was invalid.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80247002</p></td>
<td style="border:1px solid black;"><p>WU_E_OL_NEWCLIENT_REQUIRED</p></td>
<td style="border:1px solid black;"><p>An operation could not be completed because the scan package requires a greater version of the Windows Update Agent.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80247FFF</p></td>
<td style="border:1px solid black;"><p>WU_E_OL_UNEXPECTED</p></td>
<td style="border:1px solid black;"><p>Search using the scan package failed.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80248000</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_SHUTDOWN</p></td>
<td style="border:1px solid black;"><p>An operation failed because Windows Update Agent is shutting down.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80248001</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_INUSE</p></td>
<td style="border:1px solid black;"><p>An operation failed because the data store was in use.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80248002</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_INVALID</p></td>
<td style="border:1px solid black;"><p>The current and expected states of the data store do not match.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80248003</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_TABLEMISSING</p></td>
<td style="border:1px solid black;"><p>The data store is missing a table.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80248004</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_TABLEINCORRECT</p></td>
<td style="border:1px solid black;"><p>The data store contains a table with unexpected columns.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80248005</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_INVALIDTABLENAME</p></td>
<td style="border:1px solid black;"><p>A table could not be opened because the table is not in the data store.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80248006</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_BADVERSION</p></td>
<td style="border:1px solid black;"><p>The current and expected versions of the data store do not match.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80248007</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_NODATA</p></td>
<td style="border:1px solid black;"><p>The information requested is not in the data store.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80248008</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_MISSINGDATA</p></td>
<td style="border:1px solid black;"><p>The data store is missing required information or has a NULL in a table column that requires a non-null value.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80248009</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_MISSINGREF</p></td>
<td style="border:1px solid black;"><p>The data store is missing required information or has a reference to missing license terms, file, localized property or linked row.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024800A</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_UNKNOWNHANDLER</p></td>
<td style="border:1px solid black;"><p>The update was not processed because its update handler could not be recognized.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024800B</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_CANTDELETE</p></td>
<td style="border:1px solid black;"><p>The update was not deleted because it is still referenced by one or more services.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024800C</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_LOCKTIMEOUTEXPIRED</p></td>
<td style="border:1px solid black;"><p>The data store section could not be locked within the allotted time.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024800D</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_NOCATEGORIES</p></td>
<td style="border:1px solid black;"><p>The category was not added because it contains no parent categories and is not a top-level category itself.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024800E</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_ROWEXISTS</p></td>
<td style="border:1px solid black;"><p>The row was not added because an existing row has the same primary key.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024800F</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_STOREFILELOCKED</p></td>
<td style="border:1px solid black;"><p>The data store could not be initialized because it was locked by another process.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80248010</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_CANNOTREGISTER</p></td>
<td style="border:1px solid black;"><p>The data store is not allowed to be registered with COM in the current process.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80248011</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_UNABLETOSTART</p></td>
<td style="border:1px solid black;"><p>Could not create a data store object in another process.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80248013</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_DUPLICATEUPDATEID</p></td>
<td style="border:1px solid black;"><p>The server sent the same update to the client with two different revision IDs.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80248014</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_UNKNOWNSERVICE</p></td>
<td style="border:1px solid black;"><p>An operation did not complete because the service is not in the data store.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80248015</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_SERVICEEXPIRED</p></td>
<td style="border:1px solid black;"><p>An operation did not complete because the registration of the service has expired.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80248016</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_DECLINENOTALLOWED</p></td>
<td style="border:1px solid black;"><p>A request to hide an update was declined because it is a mandatory update or because it was deployed with a deadline.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80248017</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_TABLESESSIONMISMATCH</p></td>
<td style="border:1px solid black;"><p>A table was not closed because it is not associated with the session.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80248018</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_SESSIONLOCKMISMATCH</p></td>
<td style="border:1px solid black;"><p>A table was not closed because it is not associated with the session.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80248019</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_NEEDWINDOWSSERVICE</p></td>
<td style="border:1px solid black;"><p>A request to remove the Windows Update service or to unregister it with Automatic Updates was declined because it is a built-in service and/or Automatic Updates cannot fall back to another service.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024801A</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_INVALIDOPERATION</p></td>
<td style="border:1px solid black;"><p>A request was declined because the operation is not allowed.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024801B</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_SCHEMAMISMATCH</p></td>
<td style="border:1px solid black;"><p>The schema of the current data store and the schema of a table in a backup XML document do not match.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024801C</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_RESETREQUIRED</p></td>
<td style="border:1px solid black;"><p>The data store requires a session reset; release the session and retry with a new session.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024801D</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_IMPERSONATED</p></td>
<td style="border:1px solid black;"><p>A data store operation did not complete because it was requested with an impersonated identity.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80248FFF</p></td>
<td style="border:1px solid black;"><p>WU_E_DS_UNEXPECTED</p></td>
<td style="border:1px solid black;"><p>A data store error not covered by another WU_E_DS_* code.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80249001</p></td>
<td style="border:1px solid black;"><p>WU_E_INVENTORY_PARSEFAILED</p></td>
<td style="border:1px solid black;"><p>Parsing of the rule file failed.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80249002</p></td>
<td style="border:1px solid black;"><p>WU_E_INVENTORY_GET_INVENTORY_TYPE_FAILED</p></td>
<td style="border:1px solid black;"><p>Failed to get the requested inventory type from the server.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80249003</p></td>
<td style="border:1px solid black;"><p>WU_E_INVENTORY_RESULT_UPLOAD_FAILED</p></td>
<td style="border:1px solid black;"><p>Failed to upload inventory result to the server.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x80249004</p></td>
<td style="border:1px solid black;"><p>WU_E_INVENTORY_UNEXPECTED</p></td>
<td style="border:1px solid black;"><p>There was an inventory error not covered by another error code.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x80249005</p></td>
<td style="border:1px solid black;"><p>WU_E_INVENTORY_WMI_ERROR</p></td>
<td style="border:1px solid black;"><p>A WMI error occurred when enumerating the instances for a particular class.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024A000</p></td>
<td style="border:1px solid black;"><p>WU_E_AU_NOSERVICE</p></td>
<td style="border:1px solid black;"><p>Automatic Updates was unable to service incoming requests.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024A002</p></td>
<td style="border:1px solid black;"><p>WU_E_AU_NONLEGACYSERVER</p></td>
<td style="border:1px solid black;"><p>The old version of the Automatic Updates client has stopped because the WSUS server has been upgraded.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024A003</p></td>
<td style="border:1px solid black;"><p>WU_E_AU_LEGACYCLIENTDISABLED</p></td>
<td style="border:1px solid black;"><p>The old version of the Automatic Updates client was disabled.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024A004</p></td>
<td style="border:1px solid black;"><p>WU_E_AU_PAUSED</p></td>
<td style="border:1px solid black;"><p>Automatic Updates was unable to process incoming requests because it was paused.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024A005</p></td>
<td style="border:1px solid black;"><p>WU_E_AU_NO_REGISTERED_SERVICE</p></td>
<td style="border:1px solid black;"><p>No unmanaged service is registered with AU.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024AFFF</p></td>
<td style="border:1px solid black;"><p>WU_E_AU_UNEXPECTED</p></td>
<td style="border:1px solid black;"><p>An Automatic Updates error not covered by another WU_E_AU * code.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024C001</p></td>
<td style="border:1px solid black;"><p>WU_E_DRV_PRUNED</p></td>
<td style="border:1px solid black;"><p>A driver was skipped.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024C002</p></td>
<td style="border:1px solid black;"><p>WU_E_DRV_NOPROP_OR_LEGACY</p></td>
<td style="border:1px solid black;"><p>A property for the driver could not be found. It may not conform with required specifications.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024C003</p></td>
<td style="border:1px solid black;"><p>WU_E_DRV_REG_MISMATCH</p></td>
<td style="border:1px solid black;"><p>The registry type read for the driver does not match the expected type.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024C004</p></td>
<td style="border:1px solid black;"><p>WU_E_DRV_NO_METADATA</p></td>
<td style="border:1px solid black;"><p>The driver update is missing metadata.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024C005</p></td>
<td style="border:1px solid black;"><p>WU_E_DRV_MISSING_ATTRIBUTE</p></td>
<td style="border:1px solid black;"><p>The driver update is missing a required attribute.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024C006</p></td>
<td style="border:1px solid black;"><p>WU_E_DRV_SYNC_FAILED</p></td>
<td style="border:1px solid black;"><p>Driver synchronization failed.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024C007</p></td>
<td style="border:1px solid black;"><p>WU_E_DRV_NO_PRINTER_CONTENT</p></td>
<td style="border:1px solid black;"><p>Information required for the synchronization of applicable printers is missing.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024CFFF</p></td>
<td style="border:1px solid black;"><p>WU_E_DRV_UNEXPECTED</p></td>
<td style="border:1px solid black;"><p>A driver error not covered by another WU_E_DRV_* code.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024D001</p></td>
<td style="border:1px solid black;"><p>WU_E_SETUP_INVALID_INFDATA</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent could not be updated because an INF file contains invalid information.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024D002</p></td>
<td style="border:1px solid black;"><p>WU_E_SETUP_INVALID_IDENTDATA</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent could not be updated because the wuident.cab file contains invalid information.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024D003</p></td>
<td style="border:1px solid black;"><p>WU_E_SETUP_ALREADY_INITIALIZED</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent could not be updated because of an internal error that caused setup initialization to be performed twice.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024D004</p></td>
<td style="border:1px solid black;"><p>WU_E_SETUP_NOT_INITIALIZED</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent could not be updated because setup initialization never completed successfully.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024D005</p></td>
<td style="border:1px solid black;"><p>WU_E_SETUP_SOURCE_VERSION_MISMATCH</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent could not be updated because the versions specified in the INF do not match the actual source file versions.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024D006</p></td>
<td style="border:1px solid black;"><p>WU_E_SETUP_TARGET_VERSION_GREATER</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent could not be updated because a WUA file on the target system is newer than the corresponding source file.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024D007</p></td>
<td style="border:1px solid black;"><p>WU_E_SETUP_REGISTRATION_FAILED</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent could not be updated because regsvr32.exe returned an error.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024D008</p></td>
<td style="border:1px solid black;"><p>WU_E_SELFUPDATE_SKIP_ON_FAILURE</p></td>
<td style="border:1px solid black;"><p>An update to the Windows Update Agent was skipped because previous attempts to update have failed.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024D009</p></td>
<td style="border:1px solid black;"><p>WU_E_SETUP_SKIP_UPDATE</p></td>
<td style="border:1px solid black;"><p>An update to the Windows Update Agent was skipped due to a directive in the wuident.cab file.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024D00A</p></td>
<td style="border:1px solid black;"><p>WU_E_SETUP_UNSUPPORTED_CONFIGURATION</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent could not be updated because the current system configuration is not supported.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024D00B</p></td>
<td style="border:1px solid black;"><p>WU_E_SETUP_BLOCKED_CONFIGURATION</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent could not be updated because the system is configured to block the update.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024D00C</p></td>
<td style="border:1px solid black;"><p>WU_E_SETUP_REBOOT_TO_FIX</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent could not be updated because a restart of the system is required.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024D00D</p></td>
<td style="border:1px solid black;"><p>WU_E_SETUP_ALREADYRUNNING</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent setup is already running.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024D00E</p></td>
<td style="border:1px solid black;"><p>WU_E_SETUP_REBOOTREQUIRED</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent setup package requires a reboot to complete installation.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024D00F</p></td>
<td style="border:1px solid black;"><p>WU_E_SETUP_HANDLER_EXEC_FAILURE</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent could not be updated because the setup handler failed during execution.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024D010</p></td>
<td style="border:1px solid black;"><p>WU_E_SETUP_INVALID_REGISTRY_DATA</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent could not be updated because the registry contains invalid information.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024D011</p></td>
<td style="border:1px solid black;"><p>WU_E_SELFUPDATE_REQUIRED</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent must be updated before search can continue.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024D012</p></td>
<td style="border:1px solid black;"><p>WU_E_SELFUPDATE_REQUIRED_ADMIN</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent must be updated before search can continue. An administrator is required to perform the operation.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024D013</p></td>
<td style="border:1px solid black;"><p>WU_E_SETUP_WRONG_SERVER_VERSION</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent could not be updated because the server does not contain update information for this version.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024DFFF</p></td>
<td style="border:1px solid black;"><p>WU_E_SETUP_UNEXPECTED</p></td>
<td style="border:1px solid black;"><p>Windows Update Agent could not be updated because of an error not covered by another WU_E_SETUP_* error code.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024E001</p></td>
<td style="border:1px solid black;"><p>WU_E_EE_UNKNOWN_EXPRESSION</p></td>
<td style="border:1px solid black;"><p>An expression evaluator operation could not be completed because an expression was unrecognized.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024E002</p></td>
<td style="border:1px solid black;"><p>WU_E_EE_INVALID_EXPRESSION</p></td>
<td style="border:1px solid black;"><p>An expression evaluator operation could not be completed because an expression was invalid.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024E003</p></td>
<td style="border:1px solid black;"><p>WU_E_EE_MISSING_METADATA</p></td>
<td style="border:1px solid black;"><p>An expression evaluator operation could not be completed because an expression contains an incorrect number of metadata nodes.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024E004</p></td>
<td style="border:1px solid black;"><p>WU_E_EE_INVALID_VERSION</p></td>
<td style="border:1px solid black;"><p>An expression evaluator operation could not be completed because the version of the serialized expression data is invalid.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024E005</p></td>
<td style="border:1px solid black;"><p>WU_E_EE_NOT_INITIALIZED</p></td>
<td style="border:1px solid black;"><p>The expression evaluator could not be initialized.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024E006</p></td>
<td style="border:1px solid black;"><p>WU_E_EE_INVALID_ATTRIBUTEDATA</p></td>
<td style="border:1px solid black;"><p>An expression evaluator operation could not be completed because there was an invalid attribute.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024E007</p></td>
<td style="border:1px solid black;"><p>WU_E_EE_CLUSTER_ERROR</p></td>
<td style="border:1px solid black;"><p>An expression evaluator operation could not be completed because the cluster state of the computer could not be determined.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024EFFF</p></td>
<td style="border:1px solid black;"><p>WU_E_EE_UNEXPECTED</p></td>
<td style="border:1px solid black;"><p>There was an expression evaluator error not covered by another WU_E_EE_* error code.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024F001</p></td>
<td style="border:1px solid black;"><p>WU_E_REPORTER_EVENTCACHECORRUPT</p></td>
<td style="border:1px solid black;"><p>The event cache file was defective.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024F002</p></td>
<td style="border:1px solid black;"><p>WU_E_REPORTER_</p>
<p>EVENTNAMESPACEPARSEFAILED</p></td>
<td style="border:1px solid black;"><p>The XML in the event namespace descriptor could not be parsed.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024F003</p></td>
<td style="border:1px solid black;"><p>WU_E_INVALID_EVENT</p></td>
<td style="border:1px solid black;"><p>The XML in the event namespace descriptor could not be parsed.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x8024F004</p></td>
<td style="border:1px solid black;"><p>WU_E_SERVER_BUSY</p></td>
<td style="border:1px solid black;"><p>The server rejected an event because the server was too busy.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x8024FFFF</p></td>
<td style="border:1px solid black;"><p>WU_E_REPORTER_UNEXPECTED</p></td>
<td style="border:1px solid black;"><p>There was a reporter error not covered by another error code.</p></td>
</tr>  
</tbody>  
</table>
