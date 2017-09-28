---
TOCTitle: Servicio de retiro de RMS
Title: Servicio de retiro de RMS
ms:assetid: '97677e3b-bc83-47ec-b6db-d326cd94566c'
ms:contentKeyID: 18127901
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747695(v=WS.10)'
---

Servicio de retiro de RMS
=========================

El servicio de retiro es un servicio Web personalizado que se instala con RMS. Se ejecuta en los clústeres raíz y de sólo licencias. Cuando se habilita este servicio, el resto de los servicios Web de RMS del servidor quedan deshabilitados.

Este servicio descifra la clave de contenido que se encuentra en la licencia de publicación del contenido protegido con derechos y se la proporciona al cliente en respuesta a una solicitud de licencia. Esta clave permite que el contenido se guarde sin protección de RMS. El servicio de retiro registra todas las solicitudes de cliente que recibe y las envía al servicio de escucha de registro para grabarlas en la base de datos de registro.

Este servicio se habilita en la página **Configuración de seguridad** del sitio Web de administración. Una vez habilitado este servicio, no se podrá restablecer una configuración de RMS estándar en el servidor.

Después de habilitar el servicio, debe establecer la lista DACL del archivo decommission.asmx para permitir el acceso a usuarios de su empresa que hayan utilizado este servidor para obtener licencias para su contenido y agregar el grupo de servicio de RMS (RMS Service Group) a la lista DACL con permisos de lectura y ejecución para que RMS administre su funcionamiento. Una vez desprotegido todo el contenido publicado por el servidor, se debe realizar una copia de seguridad de la información de clave privada y, a continuación, quitar RMS del servidor.

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
<td style="border:1px solid black;"><p>SYSTEM</p></td>
<td style="border:1px solid black;"><p>Control total</p></td>
</tr>
</tbody>
</table>
