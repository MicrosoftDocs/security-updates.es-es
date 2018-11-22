---
TOCTitle: Servicio de certificación de cuentas RMS
Title: Servicio de certificación de cuentas RMS
ms:assetid: 'fb294969-850e-44b4-8f6a-ca5d5cec1bf1'
ms:contentKeyID: 18128037
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747802(v=WS.10)'
---

Servicio de certificación de cuentas RMS
========================================

El servicio de certificación de cuenta sólo se ejecuta en el clúster raíz. El servicio de certificación de cuentas crea certificados de cuenta de permisos, que asocian cuentas de usuario con equipos específicos. Un certificado de cuenta de permisos permite a un usuario publicar o utilizar contenido protegido con derechos mientras usa un equipo específico.

El archivo de aplicación del servicio de certificación de cuentas, Certification.asmx, está ubicado en el directorio virtual Certification, que se encuentra en IIS.

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
