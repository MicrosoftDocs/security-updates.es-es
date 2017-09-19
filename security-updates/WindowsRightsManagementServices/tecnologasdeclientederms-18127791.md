---
TOCTitle: Tecnologías de cliente de RMS
Title: Tecnologías de cliente de RMS
ms:assetid: '6980468a-fc8c-489b-966f-2921ec268e74'
ms:contentKeyID: 18127791
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720288(v=WS.10)'
---

Tecnologías de cliente de RMS
=============================

Los equipos cliente que se encuentran en una implementación de RMS utilizan las siguientes tecnologías, que permiten a los usuarios crear, publicar y utilizar contenido protegido con RMS.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Tecnología</th>
<th>Descripción</th>
<th>Emitido por</th>
<th>Para más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Aplicaciones compatibles con RMS</p></td>
<td style="border:1px solid black;"><p>Necesarias para crear y publicar contenido protegido con RMS. Las aplicaciones pueden estar desarrolladas específicamente para RMS o pueden ser aplicaciones existentes adaptadas para trabajar con RMS.</p></td>
<td style="border:1px solid black;"><p>Desarrolladores que no son de Microsoft.</p></td>
<td style="border:1px solid black;"><p>Aplicaciones compatibles con RMS</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Certificados de equipo de RMS</p></td>
<td style="border:1px solid black;"><p>Identifican un equipo determinado como de confianza en RMS.</p></td>
<td style="border:1px solid black;"><p>Servicio de activación para RMS versión 1.0. No se requiere ningún servicio para obtener un certificado de equipo con RMS SP1.</p></td>
<td style="border:1px solid black;"><p>Certificados de equipo de RMS</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Cajas de seguridad</p></td>
<td style="border:1px solid black;"><p>Contienen la clave privada del equipo y el certificado correspondiente, que contiene a su vez la clave pública del equipo.</p></td>
<td style="border:1px solid black;"><p>Servicio de activación para RMS versión 1.0. No se requiere ningún servicio para obtener una caja de seguridad con RMS SP1. La caja de seguridad contiene la clave privada del equipo; es el centro de seguridad principal para el cifrado y el descifrado.</p></td>
<td style="border:1px solid black;"><p>Cajas de seguridad</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Certificados de cuenta de permisos</p></td>
<td style="border:1px solid black;"><p>Identifican un usuario determinado como de confianza en RMS.</p></td>
<td style="border:1px solid black;"><p>Servicio de certificación de cuenta de permisos.</p></td>
<td style="border:1px solid black;"><p>Certificados de cuenta de permisos</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Certificados emisores de licencias de cliente</p></td>
<td style="border:1px solid black;"><p>Permite a un usuario publicar contenido protegido con RMS mientras está desconectado de la red.</p>
<p>(Opcional)</p></td>
<td style="border:1px solid black;"><p>Servicio de publicación de RMS.</p></td>
<td style="border:1px solid black;"><p>Certificados emisores de licencias de cliente</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Licencias de publicación</p></td>
<td style="border:1px solid black;"><p>Define los permisos de uso para un fragmento de contenido.</p></td>
<td style="border:1px solid black;"><p>El servicio de publicación de RMS o, en el caso de la publicación sin conexión, el certificado emisor de licencias de cliente puede emitir esta licencia.</p></td>
<td style="border:1px solid black;"><p>Licencias de publicación</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Licencias de uso</p></td>
<td style="border:1px solid black;"><p>Permiten a un usuario utilizar contenido protegido con RMS.</p></td>
<td style="border:1px solid black;"><p>Servicio de emisión de licencias de RMS.</p></td>
<td style="border:1px solid black;"><p>Licencias de uso</p></td>
</tr>  
</tbody>  
</table>
