---
TOCTitle: Determine WSUS Capacity Requirements
Title: Determine WSUS Capacity Requirements
ms:assetid: '92170771-83e7-47bb-abbc-7d93ee5d7867'
ms:contentKeyID: 18158411
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708483(v=WS.10)'
---

Determine WSUS Capacity Requirements
====================================

Hardware and database software requirements are driven by the number of client computers being updated in your organization. The following tables offer guidelines for server hardware and database software, based on the number of client computers being serviced. A WSUS server using the recommended hardware can support a maximum number of 60,000 clients. Both the system partition and the partition on which you install WSUS must be formatted with the NTFS file system.

| ![](images/Cc708483.Important(WS.10).gif)Importante                              |
|---------------------------------------------------------------------------------------------------------------|
| WSUS 3.0 cannot be installed on a compressed drive. Please check that the drive you choose is not compressed. |

### Minimum hardware recommendations

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>Hardware</th>
<th>Low-end 500 or fewer clients</th>
<th>Typical 500–3,000 clients</th>
<th>High-end 3,000–20,000 clients, or rollup of 30,000 clients</th>
<th>Super high-end 10,000 clients, or rollup of 100,000 clients</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>CPU</p></td>
<td style="border:1px solid black;"><p>1 GHz</p></td>
<td style="border:1px solid black;"><p>1.5 GHz or faster</p></td>
<td style="border:1px solid black;"><p>3 GHz hyper threaded processor, x64 hardware</p></td>
<td style="border:1px solid black;"><p>3 GHz hyper threaded dual processor</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Graphics card</p></td>
<td style="border:1px solid black;"><p>16 MB hardware accelerated PCI/AGP video card capable of 1-24*86*16bpp</p></td>
<td style="border:1px solid black;"><p>16 MB hardware accelerated PCI/AGP video card capable of 1-24*86*16bpp</p></td>
<td style="border:1px solid black;"><p>16 MB hardware accelerated PCI/AGP video card capable of 1-24*86*16bpp</p></td>
<td style="border:1px solid black;"><p>16 MB hardware accelerated PCI/AGP video card capable of 1-24*86*16bpp</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>RAM</p></td>
<td style="border:1px solid black;"><p>1 GB</p></td>
<td style="border:1px solid black;"><p>2 GB</p></td>
<td style="border:1px solid black;"><p>2 GB</p></td>
<td style="border:1px solid black;"><p>4 GB</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Page file</p></td>
<td style="border:1px solid black;"><p>At least 1.5 times physical memory</p></td>
<td style="border:1px solid black;"><p>At least 1.5 times physical memory</p></td>
<td style="border:1px solid black;"><p>At least 1.5 times physical memory</p></td>
<td style="border:1px solid black;"><p>At least 1.5 times physical memory</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>I/O subsystem</p></td>
<td style="border:1px solid black;"><p>Fast ATA/IDE 100 hard disk or equivalent SCSI drives</p></td>
<td style="border:1px solid black;"><p>Fast ATA/IDE 100 hard disk or equivalent SCSI drives</p></td>
<td style="border:1px solid black;"><p>Fast ATA/IDE 100 hard disk or equivalent SCSI drives</p></td>
<td style="border:1px solid black;"><p>Fast ATA/IDE 100 hard disk or equivalent SCSI drives</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Network card</p></td>
<td style="border:1px solid black;"><p>10 MB</p></td>
<td style="border:1px solid black;"><p>100 MB</p></td>
<td style="border:1px solid black;"><p>1 GB</p></td>
<td style="border:1px solid black;"><p>1 GB</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Hard drive—system partition</p></td>
<td style="border:1px solid black;"><p>1 GB</p></td>
<td style="border:1px solid black;"><p>1 GB</p></td>
<td style="border:1px solid black;"><p>1 GB</p></td>
<td style="border:1px solid black;"><p>1 GB</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Hard drive—content storage</p></td>
<td style="border:1px solid black;"><p>20 GB</p></td>
<td style="border:1px solid black;"><p>30 GB</p></td>
<td style="border:1px solid black;"><p>30 GB</p></td>
<td style="border:1px solid black;"><p>30 GB</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Hard drive—SQL Server installation</p></td>
<td style="border:1px solid black;"><p>2 GB</p></td>
<td style="border:1px solid black;"><p>2 GB</p></td>
<td style="border:1px solid black;"><p>2 GB</p></td>
<td style="border:1px solid black;"><p>2 GB</p></td>
</tr>
</tbody>
</table>
  
| ![](images/Cc708483.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                                                                    |  
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| These guidelines assume that WSUS clients are synchronizing with the server every eight hours (for the high-end configuration) or every two hours (for the super high-end configuration). If they synchronize more often, there will be a corresponding increment in the server load. For example, if clients synchronize twice a day, the load will be twice as much as if they synchronize once a day. |
  
| ![](images/Cc708483.note(WS.10).gif)Nota                                                                                                           |  
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| Increasing the number of languages will also increase the load. Supporting five languages rather than one language will approximately double the size of the content directory. |
