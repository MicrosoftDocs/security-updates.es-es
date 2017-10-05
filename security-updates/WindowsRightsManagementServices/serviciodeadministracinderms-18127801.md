---
TOCTitle: Servicio de administración de RMS
Title: Servicio de administración de RMS
ms:assetid: '4bd3e142-f0f6-40e9-a160-deab28ce5b88'
ms:contentKeyID: 18127801
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747560(v=WS.10)'
---

Servicio de administración de RMS
=================================

El servicio de administración se ejecuta en el clúster raíz de RMS y en cualquier clúster de sólo licencias. Este servicio aloja el sitio Web de administración y permite administrar RMS.

El archivo de aplicación del servicio de administración, Default.aspx, está ubicado en el directorio virtual Admin *sitio Web de RMS*\\\_wmcs\\Admin, donde *sitio\_Web\_RMS* se reemplaza por el nombre del sitio Web en el que haya establecido los servicios en línea de RMS.

La lista de control de acceso predeterminada de este servicio se muestra en la siguiente tabla:

###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Usuario o grupo</th>
<th style="border:1px solid black;" >Permiso predeterminado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Administradores</td>
<td style="border:1px solid black;">Control total</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Grupo de servicio RMS</td>
<td style="border:1px solid black;">Leer y ejecutar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SYSTEM</td>
<td style="border:1px solid black;">Control total</td>
</tr>
</tbody>
</table>
