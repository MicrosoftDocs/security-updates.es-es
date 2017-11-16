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
<th style="border:1px solid black;" >Tecnología</th>
<th style="border:1px solid black;" >Descripción</th>
<th style="border:1px solid black;" >Emitido por</th>
<th style="border:1px solid black;" >Para más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Aplicaciones compatibles con RMS</td>
<td style="border:1px solid black;">Necesarias para crear y publicar contenido protegido con RMS. Las aplicaciones pueden estar desarrolladas específicamente para RMS o pueden ser aplicaciones existentes adaptadas para trabajar con RMS.</td>
<td style="border:1px solid black;">Desarrolladores que no son de Microsoft.</td>
<td style="border:1px solid black;">Aplicaciones compatibles con RMS</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Certificados de equipo de RMS</td>
<td style="border:1px solid black;">Identifican un equipo determinado como de confianza en RMS.</td>
<td style="border:1px solid black;">Servicio de activación para RMS versión 1.0. No se requiere ningún servicio para obtener un certificado de equipo con RMS SP1.</td>
<td style="border:1px solid black;">Certificados de equipo de RMS</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Cajas de seguridad</td>
<td style="border:1px solid black;">Contienen la clave privada del equipo y el certificado correspondiente, que contiene a su vez la clave pública del equipo.</td>
<td style="border:1px solid black;">Servicio de activación para RMS versión 1.0. No se requiere ningún servicio para obtener una caja de seguridad con RMS SP1. La caja de seguridad contiene la clave privada del equipo; es el centro de seguridad principal para el cifrado y el descifrado.</td>
<td style="border:1px solid black;">Cajas de seguridad</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Certificados de cuenta de permisos</td>
<td style="border:1px solid black;">Identifican un usuario determinado como de confianza en RMS.</td>
<td style="border:1px solid black;">Servicio de certificación de cuenta de permisos.</td>
<td style="border:1px solid black;">Certificados de cuenta de permisos</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Certificados emisores de licencias de cliente</td>
<td style="border:1px solid black;">Permite a un usuario publicar contenido protegido con RMS mientras está desconectado de la red.
(Opcional)</td>
<td style="border:1px solid black;">Servicio de publicación de RMS.</td>
<td style="border:1px solid black;">Certificados emisores de licencias de cliente</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Licencias de publicación</td>
<td style="border:1px solid black;">Define los permisos de uso para un fragmento de contenido.</td>
<td style="border:1px solid black;">El servicio de publicación de RMS o, en el caso de la publicación sin conexión, el certificado emisor de licencias de cliente puede emitir esta licencia.</td>
<td style="border:1px solid black;">Licencias de publicación</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Licencias de uso</td>
<td style="border:1px solid black;">Permiten a un usuario utilizar contenido protegido con RMS.</td>
<td style="border:1px solid black;">Servicio de emisión de licencias de RMS.</td>
<td style="border:1px solid black;">Licencias de uso</td>
</tr>
</tbody>
</table>
