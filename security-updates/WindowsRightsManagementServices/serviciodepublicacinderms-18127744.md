---
TOCTitle: Servicio de publicación de RMS
Title: Servicio de publicación de RMS
ms:assetid: '4c0c8fe3-695c-4b2c-a2d3-cab9b52bbb25'
ms:contentKeyID: 18127744
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720267(v=WS.10)'
---

Servicio de publicación de RMS
==============================

El servicio de publicación, que emite licencias de publicación, se ejecuta en el clúster raíz de RMS y en cualquier clúster de sólo licencias. Las licencias de publicación definen la directiva mediante la que se pueden otorgar las licencias de uso.

El archivo de aplicación del servicio de publicación, Publish.asmx, está ubicado en el directorio virtual Licensing, que se encuentra en IIS.

La lista de control de acceso predeterminada de este servicio se muestra en la siguiente tabla:

###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Usuario o grupo</th>
<th>Permiso predeterminado</th>
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
<tr class="even">
<td style="border:1px solid black;">Usuarios</td>
<td style="border:1px solid black;">Leer y ejecutar</td>
</tr>
</tbody>
</table>
