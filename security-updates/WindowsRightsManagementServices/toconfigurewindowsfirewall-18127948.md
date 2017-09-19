---
TOCTitle: To Configure Windows Firewall
Title: To Configure Windows Firewall
ms:assetid: 'c35d3f34-ee8b-4fa8-a6ab-a85534d67f5f'
ms:contentKeyID: 18127948
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747747(v=WS.10)'
---

To Configure Windows Firewall
=============================

Windows Firewall is a host-based firewall application that is installed with Microsoft Windows XP Service Pack 2 (SP2), Windows Server 2003 with Service Pack 1 (SP1), and Windows Vista®. Unlike Windows XP with SP2 and Windows Vista, Windows Firewall in Windows Server 2003 with SP1 is not turned on by default. If you would like to use the functionality of Windows Firewall within your RMS infrastructure, you must create a few firewall exceptions. These exceptions are described below.

| ![](images/Cc747747.note(WS.10).gif)Nota                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| This topic discusses only the firewall exceptions that should be added specific to RMS. It is likely that additional exceptions need to be made for other applications. |

On the Active Directory domain controllers, the following Windows Firewall exceptions should be made:

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Port Exception</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>TCP 389</p></td>
<td style="border:1px solid black;"><p>Lightweight Directory Access Protocol (LDAP), used by Active Directory</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>TCP 3268</p></td>
<td style="border:1px solid black;"><p>Active Directory global catalog</p></td>
</tr>  
</tbody>  
</table>
  
The following table shows the port exceptions that should be made on the RMS servers in the RMS cluster. Both of the ports do not have to be open at the same time. For HTTP transmission, you should open only TCP port 80. If your RMS environment is using SSL or HTTPS, you should open only TCP port 443. If your organization is using a port number other than the default for RMS, you should use that port instead.
  
###  

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th>Port Exception</th>  
<th>Description</th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>TCP 80</p></td>
<td style="border:1px solid black;"><p>HTTP</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>TCP 443</p></td>
<td style="border:1px solid black;"><p>HTTPS or Secure Sockets Layer communication (SSL)</p></td>
</tr>  
</tbody>  
</table>
  
If the logging database server is not on a server in the RMS cluster, the following port exceptions should be created on the database server that is hosting the RMS logging database. This following table assumes that you are using Microsoft SQL Server 2000 or later.
  
###  

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th>Port Exception</th>  
<th>Description</th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>TCP 1433</p></td>
<td style="border:1px solid black;"><p>Default SQL Server listening port</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>TCP 445</p></td>
<td style="border:1px solid black;"><p>SQL Server Named Pipes (used for provisioning the RMS server)</p></td>
</tr>  
</tbody>  
</table>
  
In addition to creating these port exceptions, special considerations should be taken when configuring the firewall scope. Unless your RMS environment is used in an extranet scenario, you should restrict all traffic to your organization's network. If your RMS environment needs to be available to client computers outside of your organization's network, you should allow any computer on the Internet to connect only through TCP port 443 or TCP port 80.
  
| ![](images/Cc747747.Caution(WS.10).gif)Precaución                                                                                                                                                                                                                                                                                                                                                 |  
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| In an RMS environment, TCP port 445 is used to provision the RMS cluster, but this port is also the file sharing port for all computers that are running Microsoft Windows 2000 or later. Unless you have specific need for other computers on your network to have access to this port, you should restrict the scope so that only the servers in the RMS cluster have access to TCP port 445 on the logging database server. |
  
For more information regarding the Windows Firewall, please see the help documentation for Windows Server 2003 with SP1.
