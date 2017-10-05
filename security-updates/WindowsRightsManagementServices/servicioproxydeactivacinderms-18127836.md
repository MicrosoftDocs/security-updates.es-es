---
TOCTitle: Servicio proxy de activación de RMS
Title: Servicio proxy de activación de RMS
ms:assetid: '6b9d33ef-466b-405b-a768-54e5615d6770'
ms:contentKeyID: 18127836
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747608(v=WS.10)'
---

Servicio proxy de activación de RMS
===================================

Todas las solicitudes de activación de equipos de RMS versión 1.0 pasan por el servicio proxy de activación, que sólo se ejecuta en el clúster raíz de RMS. Es preciso activar un equipo cliente para poder usarlo con RMS para publicar o utilizar contenido protegido con derechos. Para RMS con Service Pack 1, el cliente se “activa automáticamente” y no necesita usar el servidor proxy de activación ni Microsoft Activation Service para generar y un certificado de equipo y liquidación.

El servicio proxy de activación reenvía las solicitudes de activación de equipo de los clientes de RMS versión 1.0 al servicio de activación de Microsoft, que devuelve una caja de seguridad generada de forma personalizada y un certificado de equipo RMS coincidente que son exclusivos para ese usuario y ese equipo. A continuación, el servicio proxy de activación reenvía estos elementos al cliente que efectuó la solicitud.

El archivo de aplicación del servicio proxy de activación, Activation.asmx, está ubicado en el directorio virtual Certification, que se encuentra en IIS. La lista de control de acceso predeterminada de este servicio se muestra en la siguiente tabla:

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
<td style="border:1px solid black;">Invitados</td>
<td style="border:1px solid black;">Leer y ejecutar</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Grupo de servicio RMS</td>
<td style="border:1px solid black;">Leer y ejecutar</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SYSTEM</td>
<td style="border:1px solid black;">Control total</td>
</tr>
</tbody>
</table>
