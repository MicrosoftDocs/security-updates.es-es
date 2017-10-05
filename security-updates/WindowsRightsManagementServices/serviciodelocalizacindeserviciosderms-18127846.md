---
TOCTitle: Servicio de localización de servicios de RMS
Title: Servicio de localización de servicios de RMS
ms:assetid: '6f410cc9-5d5b-4df3-bf4f-7b13811eb52f'
ms:contentKeyID: 18127846
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747548(v=WS.10)'
---

Servicio de localización de servicios de RMS
============================================

El servicio de localización de servicios se ejecuta en los clústeres raíz y de sólo licencias de RMS. El servicio de localización de servicios proporciona la dirección URL de conexión de servicios del clúster a Active Directory para que los clientes compatibles con RMS puedan detectarlos.

El archivo de aplicación del servicio de localización de servicios, ServiceLocator.asmx, está ubicado en los directorios virtuales Certification y Licensing, que se encuentran en IIS.

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
<tr class="even">
<td style="border:1px solid black;">Usuarios</td>
<td style="border:1px solid black;">Leer y ejecutar</td>
</tr>
</tbody>
</table>
