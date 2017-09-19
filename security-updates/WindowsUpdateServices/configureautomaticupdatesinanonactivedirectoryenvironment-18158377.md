---
TOCTitle: 'Configure Automatic Updates in a Non–Active Directory Environment'
Title: 'Configure Automatic Updates in a Non–Active Directory Environment'
ms:assetid: '75ee9da8-0ffd-400c-b722-aeafdb68ceb3'
ms:contentKeyID: 18158377
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708449(v=WS.10)'
---

Configure Automatic Updates in a Non–Active Directory Environment
=================================================================

In a non-Active Directory environment, you can configure Automatic Updates by using any of the following methods:

-   Using Group Policy Object Editor and editing the Local Group Policy object
-   Editing the registry directly by using the registry editor (Regedit.exe)
-   Centrally deploying these registry entries by using System Policy in Windows NT 4.0 style

WSUS Environment Options
------------------------

The registry entries for the WSUS environment options are located in the following subkey:

**HKEY\_LOCAL\_MACHINE\\Software\\Policies\\Microsoft\\Windows\\WindowsUpdate**

The keys and their value ranges are listed in the following table.

### Windows Update Agent Environment Options Registry Keys

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Entry Name</th>
<th>Values</th>
<th>Data Type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p><strong>ElevateNonAdmins</strong></p></td>
<td style="border:1px solid black;"><p>Range = 1|0</p>
<p>1 = Users in the Users security group are allowed to approve or disapprove updates.</p>
<p>0 = Only users in the Administrators user group can approve or disapprove updates.</p></td>
<td style="border:1px solid black;"><p>Reg_DWORD</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>TargetGroup</strong></p></td>
<td style="border:1px solid black;"><p>Name of the computer group to which the computer belongs, used to implement client-side targeting—for example, &quot;TestServers.&quot; This policy is paired with <strong>TargetGroupEnabled</strong>.</p></td>
<td style="border:1px solid black;"><p>Reg_String</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>TargetGroupEnabled</strong></p></td>
<td style="border:1px solid black;"><p>Range = 1|0</p>
<p>1 = Use client-side targeting.</p>
<p>0 = Do not use client-side targeting. This policy is paired with <strong>TargetGroup</strong>.</p></td>
<td style="border:1px solid black;"><p>Reg_DWORD</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>WUServer   </strong></p></td>
<td style="border:1px solid black;"><p>HTTP(S) URL of the WSUS server used by Automatic Updates and (by default) API callers. This policy is paired with <strong>WUStatusServer</strong>; both must be set to the same value in order for them to be valid.</p></td>
<td style="border:1px solid black;"><p>Reg_String</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>WUStatusServer</strong></p></td>
<td style="border:1px solid black;"><p>The HTTP(S) URL of the server to which reporting information will be sent for client computers that use the WSUS server configured by the <strong>WUServer</strong> key. This policy is paired with <strong>WUServer</strong>; both must be set to the same value in order for them to be valid.</p></td>
<td style="border:1px solid black;"><p>Reg_String</p></td>
</tr>  
</tbody>  
</table>
  
Automatic Update Configuration Options  
--------------------------------------
  
The registry entries for the Automatic Update configuration options are located in the following subkey:
  
**HKEY\_LOCAL\_MACHINE\\Software\\Policies\\Microsoft\\Windows\\WindowsUpdate\\AU**
  
The keys and their value ranges are listed in the following table.
  
### Automatic Updates Configuration Registry Keys

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="33%" />  
<col width="33%" />  
<col width="33%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th>Entry Name</th>  
<th>Value Range and Meanings</th>  
<th>Data Type</th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>AUOptions</strong></p></td>
<td style="border:1px solid black;"><p>Range = 2|3|4|5</p>
<p>2 = Notify before download.</p>  
<p>3 = Automatically download and notify of installation.</p>  
<p>4 = Automatic download and scheduled installation. (Only valid if values exist for <strong>ScheduledInstallDay</strong> and <strong>ScheduledInstallTime</strong>.)</p>
<p>5 = Automatic Updates is required, but end users can configure it.</p></td>
<td style="border:1px solid black;"><p>Reg_DWORD</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>AutoInstallMinorUpdates</strong></p></td>
<td style="border:1px solid black;"><p>Range = 0|1</p>
<p>0 = Treat minor updates like other updates.</p>
<p>1 = Silently install minor updates.</p></td>
<td style="border:1px solid black;"><p>Reg_DWORD</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>DetectionFrequency</strong></p></td>
<td style="border:1px solid black;"><p>Range=n; where n=time in hours (1-22).</p>
<p>Time between detection cycles.</p></td>
<td style="border:1px solid black;"><p>Reg_DWORD</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>DetectionFrequencyEnabled</strong></p></td>
<td style="border:1px solid black;"><p>Range = 0|1</p>
<p>1 = Enable DetectionFrequency.</p>
<p>0 = Disable custom DetectionFrequency (use default value of 22 hours).</p></td>
<td style="border:1px solid black;"><p>Reg_DWORD</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>NoAutoRebootWithLoggedOnUsers</strong></p></td>
<td style="border:1px solid black;"><p>Range = 0|1;</p>
<p>1 = Logged-on user gets to choose whether or not to restart his or her computer.</p>
<p>0 = Automatic Updates notifies user that the computer will restart in 5 minutes.</p></td>
<td style="border:1px solid black;"><p>Reg_DWORD</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>NoAutoUpdate</strong></p></td>
<td style="border:1px solid black;"><p>Range = 0|1</p>
<p>0 = Enable Automatic Updates.</p>
<p>1 = Disable Automatic Updates.</p></td>
<td style="border:1px solid black;"><p>Reg_DWORD</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>RebootRelaunchTimeout</strong></p></td>
<td style="border:1px solid black;"><p>Range=n; where n=time in minutes (1-1440).</p>
<p>Time between prompting again for a scheduled restart.</p></td>
<td style="border:1px solid black;"><p>Reg_DWORD</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>RebootRelaunchTimeoutEnabled</strong></p></td>
<td style="border:1px solid black;"><p>Range = 0|1</p>
<p>1 = Enable <strong>RebootRelaunchTimeout</strong>.</p>
<p>0 = Disable custom <strong>RebootRelaunchTimeout</strong>(use default value of 10 minutes).</p></td>
<td style="border:1px solid black;"><p>Reg_DWORD</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>RebootWarningTimeout</strong></p></td>
<td style="border:1px solid black;"><p>Range=n; where n=time in minutes (1-30).</p>
<p>Length, in minutes, of the restart warning countdown after installing updates with a deadline or scheduled updates.</p></td>
<td style="border:1px solid black;"><p>Reg_DWORD</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>RebootWarningTimeoutEnabled</strong></p></td>
<td style="border:1px solid black;"><p>Range = 0|1</p>
<p>1 = Enable <strong>RebootWarningTimeout</strong>.</p>
<p>0 = Disable custom <strong>RebootWarningTimeout</strong> (use default value of 5 minutes).</p></td>
<td style="border:1px solid black;"><p>Reg_DWORD</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>RescheduleWaitTime</strong></p></td>
<td style="border:1px solid black;"><p>Range=n; where n=time in minutes (1-60).</p>
<p>Time, in minutes, that Automatic Updates should wait at startup before applying updates from a missed scheduled installation time.</p>
<p>Note that this policy applies only to scheduled installations, not deadlines. Updates whose deadlines have expired should always be installed as soon as possible.</p></td>
<td style="border:1px solid black;"><p>Reg_DWORD</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>RescheduleWaitTimeEnabled</strong></p></td>
<td style="border:1px solid black;"><p>Range = 0|1</p>
<p>1 = Enable <strong>RescheduleWaitTime</strong></p>
<p>0 = Disable <strong>RescheduleWaitTime</strong>(attempt the missed installation during the next scheduled installation time).</p></td>
<td style="border:1px solid black;"><p>Reg_DWORD</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>ScheduledInstallDay</strong></p></td>
<td style="border:1px solid black;"><p>Range = 0|1|2|3|4|5|6|7</p>
<p>0 = Every day.</p>  
<p>1 through 7 = The days of the week from Sunday (1) to Saturday (7).</p>
<p>(Only valid if <strong>AUOptions</strong> equals 4.)</p></td>
<td style="border:1px solid black;"><p>Reg_DWORD</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>ScheduledInstallTime</strong></p></td>
<td style="border:1px solid black;"><p>Range = n; where n = the time of day in 24-hour format (0-23).</p></td>
<td style="border:1px solid black;"><p>Reg_DWORD</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>UseWUServer</strong></p></td>
<td style="border:1px solid black;"><p>The <strong>WUServer</strong> value is not respected unless this key is set.</p></td>
<td style="border:1px solid black;"><p>Reg_DWORD</p></td>
</tr>  
</tbody>  
</table>
