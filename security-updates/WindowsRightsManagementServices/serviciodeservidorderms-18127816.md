---
TOCTitle: Servicio de servidor de RMS
Title: Servicio de servidor de RMS
ms:assetid: '772d0a89-c9fb-4430-9434-38cd5add1e86'
ms:contentKeyID: 18127816
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747566(v=WS.10)'
---

Servicio de servidor de RMS
===========================

El servicio de servidor sólo se ejecuta en el clúster raíz de RMS. El servicio de servidor expone una solicitud, realizada por un cliente mediante publicación en línea, para recuperar un certificado emisor de licencias de servidor.

El archivo de aplicación del servicio de servidor, Server.asmx, está ubicado en el directorio virtual Certification, que se encuentra en IIS.

La lista de control de acceso predeterminada de este servicio se muestra en la siguiente tabla:

###  

<p> </p>
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
<td style="border:1px solid black;"><p>Administradores</p></td>
<td style="border:1px solid black;"><p>Control total</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Grupo de servicio RMS</p></td>
<td style="border:1px solid black;"><p>Leer y ejecutar</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>SYSTEM</p></td>
<td style="border:1px solid black;"><p>Control total</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Usuarios</p></td>
<td style="border:1px solid black;"><p>Leer y ejecutar</p></td>
</tr>  
</tbody>  
</table>
