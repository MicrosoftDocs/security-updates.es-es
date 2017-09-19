---
TOCTitle: 'Appendix A: Unattended Installation'
Title: 'Appendix A: Unattended Installation'
ms:assetid: '3e8fcb38-d5a9-4285-baa2-23323a384cb1'
ms:contentKeyID: 18158326
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720513(v=WS.10)'
---

Appendix A: Unattended Installation
===================================

You can use command-line parameters to run WSUS Setup in *unattended mode*. When running this way, WSUS Setup does not display a user interface (UI). If you need to troubleshoot the setup process, use the log files, which you can find at the following location:

*WSUSInstallationDrive*:\\Program Files\\Microsoft Windows Server Update Services\\LogFiles\\

Use command-line parameters from a command prompt.

Type the following command:

**WSUSSetup.exe** *command-line parameter* **/v"** **property="***value***" "**

where *command-line parameter* is a command-line parameter from the WSUS Setup command-line parameters table, where *property* is a property from the WSUS Setup properties table, and where *value* is the actual value of the property being passed to WSUS. Both tables can be found below.

If you need to pass a value to WSUS Setup, use the command-line parameter **/v** along with a property and its value. Properties are always paired with values. Microsoft Windows Installer requires values passed using a leading and trailing space. For example, if you wanted WSUS Setup to install the WSUS Content Directory to D:\\WSUS you would use the following syntax:

**WSUSSetup.exe /v" CONTENT\_DIR= "D:\\WSUS" "**

If you need help with WSUSutil.exe, you can use the **help** command. For example, use the following command to display the list of command-line parameters:

**WSUSSetup.exe help**

WSUS Setup accepts the following command-line parameters.

### WSUS Setup Command-line Parameters

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p><strong>/q</strong></p></td>
<td style="border:1px solid black;"><p>Perform silent installation.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>/u</strong></p></td>
<td style="border:1px solid black;"><p>Uninstall the product. Also uninstalls the WMSDE instance if it is installed.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>/d</strong></p></td>
<td style="border:1px solid black;"><p>Use the existing database server (the SQL_INSTANCE property will define the instance to use).</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>/o</strong></p></td>
<td style="border:1px solid black;"><p>Overwrite the existing database.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>/?</strong></p></td>
<td style="border:1px solid black;"><p>Display command-line Help</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>/v</strong></p></td>
<td style="border:1px solid black;"><p>Passes specified values to the Windows Installer package (.msi file). The property Name value pairs should conform to the format specified by Windows Installer. The properties should be enclosed in quotation marks with a leading and trailing space.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>/f</strong></p></td>
<td style="border:1px solid black;"><p>Install WSUS in a special mode designed to be used with remote SQL. This option is used to set up the front-end of the WSUS installation, which includes IIS and the update storage location. For more information about remote SQL, see <a href="https://technet.microsoft.com/9e01d057-6b39-4eb7-b151-dff7ad0cd638">Appendix C: Remote SQL</a>.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>/b</strong></p></td>
<td style="border:1px solid black;"><p>Install WSUS in a special mode designed to be used with remote SQL. This option is used to set up the database on the back-end SQL server. For more information about remote SQL, see <a href="https://technet.microsoft.com/9e01d057-6b39-4eb7-b151-dff7ad0cd638">Appendix C: Remote SQL</a>.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>/l</strong></p></td>
<td style="border:1px solid black;"><p>This option used in combination with a language variable allows you to force the setup wizard to use a different language than the one detected as the default. Use a colon followed by a language variable from the Language Variables table below to set the language.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>/g</strong></p></td>
<td style="border:1px solid black;"><p>Use this option to perform an upgrade from the RC1 version of WSUS.</p></td>
</tr>  
</tbody>  
</table>
  
Use the following properties to configure WSUS by using the command-line parameter **/v**.
  
### WSUS Setup Properties

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th>Windows Installer Property</th>  
<th>Description</th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>CONTENT_DIR</p></td>
<td style="border:1px solid black;"><p>The directory where content will be stored. Must be an NTFS drive and can be a non-local mapped network drive.</p>
<p>Default is <em>WSUSInstallationDrive</em><strong>:\WSUS\WSUSContent</strong>, where <em>WSUSInstallationDrive</em> is the local drive with largest free space.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>CONTENT_LOCAL</p></td>
<td style="border:1px solid black;"><p>If set to &quot;1&quot; the .cab files will be stored locally (this is the default).</p>
<p>If set to &quot;0&quot; the client computers will be redirected to the Microsoft Update server for downloading the .cab files.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>INSTANCE_NAME</p></td>
<td style="border:1px solid black;"><p>The name of the SQL Server instance to be used. If an existing instance is not present, the default is &quot;WSUS.&quot;</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>WMSDE_DIR</p></td>
<td style="border:1px solid black;"><p>The directory where WMSDE database will be stored. The directory must be on an NTFS drive.</p>
<p>The default is <em>drive</em><strong>:\WSUS</strong>, where <em>drive</em> is the local drive with largest free space.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>RETAIN_DATA</p></td>
<td style="border:1px solid black;"><p>This option is used during uninstallation to define what data should be left.</p>
<p>RETAIN_DATA=0 - Delete everything.</p>  
<p>RETAIN_DATA=1 – Leave the database.</p>  
<p>RETAIN_DATA=2 – Leave logs.</p>  
<p>RETAIN_DATA=3 - Leave the database and logs.</p>  
<p>RETAIN_DATA=4 – Leave content.</p>  
<p>RETAIN_DATA=5 - Leave the database and content.</p>  
<p>RETAIN_DATA=6 – Leave logs and content.</p>
<p>RETAIN_DATA=7 - Leave everything (default).</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>ENABLE_REPLICA</p></td>
<td style="border:1px solid black;"><p>If set to 1, enable replica mode.</p>
<p>If set to 0, do not enable replica mode.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>REPLICA_PARENT_PORT</p></td>
<td style="border:1px solid black;"><p>Set to the ID of the replica parent port.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>REPLICA_PARENT</p></td>
<td style="border:1px solid black;"><p>Set to the name of the replica's parent server.</p></td>
</tr>  
</tbody>  
</table>
  
Use the following properties in combination with the **/l** option.
  
### Language Variables

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th>Variable</th>  
<th>Language name</th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>CHS</p></td>
<td style="border:1px solid black;"><p>Simplified Chinese</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>CHT</p></td>
<td style="border:1px solid black;"><p>Traditional Chinese</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>CSY</p></td>
<td style="border:1px solid black;"><p>Czech</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>DEU</p></td>
<td style="border:1px solid black;"><p>German</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>ENU</p></td>
<td style="border:1px solid black;"><p>English</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>ESN</p></td>
<td style="border:1px solid black;"><p>Spanish</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>FRA</p></td>
<td style="border:1px solid black;"><p>French</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>HUN</p></td>
<td style="border:1px solid black;"><p>Hungarian</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>ITA</p></td>
<td style="border:1px solid black;"><p>Italian</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>JPN</p></td>
<td style="border:1px solid black;"><p>Japanese</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>KOR</p></td>
<td style="border:1px solid black;"><p>Korean</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>NLD</p></td>
<td style="border:1px solid black;"><p>Dutch</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>PLK</p></td>
<td style="border:1px solid black;"><p>Polish</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>PTB</p></td>
<td style="border:1px solid black;"><p>Portuguese-Brazil</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>PTG</p></td>
<td style="border:1px solid black;"><p>Portuguese-Portugal</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>RUS</p></td>
<td style="border:1px solid black;"><p>Russian</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>SVE</p></td>
<td style="border:1px solid black;"><p>Swedish</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>TRK</p></td>
<td style="border:1px solid black;"><p>Turkish</p></td>
</tr>  
</tbody>  
</table>
