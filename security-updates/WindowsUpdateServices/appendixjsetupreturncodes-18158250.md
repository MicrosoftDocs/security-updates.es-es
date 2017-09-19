---
TOCTitle: 'Appendix J: Setup Return Codes'
Title: 'Appendix J: Setup Return Codes'
ms:assetid: '34e14364-0b3e-4558-87f6-abf08656a073'
ms:contentKeyID: 18158250
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720501(v=WS.10)'
---

Appendix J: Setup Return Codes
==============================

Windows Server Update Services 3.0 uses the following return codes to determine the success or the failure of its Setup.

Windows Server Update Services 3.0 Setup Return Codes
-----------------------------------------------------

The table in this section shows the return codes (hexadecimal values) returned by **wsussetup.exe**, the return string, and the meaning. A return code of zero indicates success; anything else indicates a failure.

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
<th>Return Code</th>
<th>Return String</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>0x001450</p></td>
<td style="border:1px solid black;"><p>SUS_LAUNCH_ERROR</p></td>
<td style="border:1px solid black;"><p>Setup Launch Conditions not satisfied.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x001451</p></td>
<td style="border:1px solid black;"><p>SUS_UNKNOWN_ERROR</p></td>
<td style="border:1px solid black;"><p>Unknown error.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x001452</p></td>
<td style="border:1px solid black;"><p>SUS_REBOOT_REQUIRED</p></td>
<td style="border:1px solid black;"><p>Reboot required to complete the installation. This most commonly occurs when installing wMSDE.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x001453</p></td>
<td style="border:1px solid black;"><p>SUS_INVALID_COMMANDLINE</p></td>
<td style="border:1px solid black;"><p>Invalid CommandLine</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x001454</p></td>
<td style="border:1px solid black;"><p>SUS_LOWSQLVERSION</p></td>
<td style="border:1px solid black;"><p>Low SQL version—SQL 2005 is required.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x001455</p></td>
<td style="border:1px solid black;"><p>SUS_TRIGGERSNOTSET</p></td>
<td style="border:1px solid black;"><p>SQL triggers are not set. When installing on an existing SQL instance, that instance must support nested triggers.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x001456</p></td>
<td style="border:1px solid black;"><p>SUS_INVALIDPATH</p></td>
<td style="border:1px solid black;"><p>Invalid content path specified.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x001457</p></td>
<td style="border:1px solid black;"><p>SUS_NETWORKPATH</p></td>
<td style="border:1px solid black;"><p>Specified content path is a network path.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x001458</p></td>
<td style="border:1px solid black;"><p>SUS_NONNTFS_PATH</p></td>
<td style="border:1px solid black;"><p>Specified content path is not NTFS.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x001459</p></td>
<td style="border:1px solid black;"><p>SUS_NONFIXEDDRIVE</p></td>
<td style="border:1px solid black;"><p>Specified content path is not on a fixed drive.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x00145a</p></td>
<td style="border:1px solid black;"><p>SUS_NONTFS_DRIVES_PRESENT</p></td>
<td style="border:1px solid black;"><p>No NTFS drives present on the system.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x00145b</p></td>
<td style="border:1px solid black;"><p>SUS_INSUFFICIENT_SPACE</p></td>
<td style="border:1px solid black;"><p>Not enough space is available at the given path. At least 6 GB of space is required.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x00145c</p></td>
<td style="border:1px solid black;"><p>SUS_NEED_SERVER_AND_PORT</p></td>
<td style="border:1px solid black;"><p>Need both server name and port for replica mode.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x00145d</p></td>
<td style="border:1px solid black;"><p>SUS_MSCOM_SERVER</p></td>
<td style="border:1px solid black;"><p>Specified server name ends in &quot;.microsoft.com&quot;.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x001460</p></td>
<td style="border:1px solid black;"><p>SUS_ERROR_PREREQCHECK_FAIL</p></td>
<td style="border:1px solid black;"><p>Prerequisite check failed.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>0x001461</p></td>
<td style="border:1px solid black;"><p>SUS_LOWDBSCHEMAUPGRADE_VERSION</p></td>
<td style="border:1px solid black;"><p>This database schema is too old to be upgraded.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>0x001462</p></td>
<td style="border:1px solid black;"><p>SUS_UPGRADE_REQUIRED</p></td>
<td style="border:1px solid black;"><p>Setup needs to upgrade from a previous version. Use the /G to avoid this error.</p></td>
</tr>  
</tbody>  
</table>
