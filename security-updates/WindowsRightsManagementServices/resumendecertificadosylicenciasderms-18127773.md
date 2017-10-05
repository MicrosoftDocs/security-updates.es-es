---
TOCTitle: Resumen de certificados y licencias de RMS
Title: Resumen de certificados y licencias de RMS
ms:assetid: '637ccfca-318e-4346-85b5-0945b058fb9c'
ms:contentKeyID: 18127773
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747595(v=WS.10)'
---

Resumen de certificados y licencias de RMS
==========================================

En la tabla siguiente, se muestran los certificados y las licencias utilizados en RMS, que se explican en detalle en el resto de los temas de la sección.

###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Certificado o licencia</th>
<th style="border:1px solid black;" >Finalidad</th>
<th style="border:1px solid black;" >Contenido</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Certificados emisores de licencias de servidor</td>
<td style="border:1px solid black;">El certificado emisor de licencias de servidor, que se emite para otorgar licencias a los servidores, concede el permiso de emitir:
<ul>
<li>Licencias de publicación<br />
<br />
</li>
<li>Licencias de uso<br />
<br />
</li>
<li>Certificados emisores de licencias de cliente<br />
<br />
</li>
<li>Plantillas de directiva de permisos<br />
<br />
</li>
</ul>
El certificado emisor de licencias de servidor, que se concede al clúster de certificación raíz, concede además el permiso de emitir:
<ul>
<li>Certificados de cuenta de permisos a los clientes<br />
<br />
</li>
<li>Certificados emisores de licencias de servidor para servidores de licencias<br />
<br />
</li>
</ul></td>
<td style="border:1px solid black;">El certificado emisor de licencias de servidor que se concede a un servidor de licencias contiene la clave pública del servidor de licencias.
El certificado emisor de licencias de servidor que se concede al servidor de certificación raíz contiene la clave pública del servidor de certificación raíz.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Certificados emisores de licencias de cliente</td>
<td style="border:1px solid black;">Otorga a un usuario el permiso para publicar contenido protegido con RMS sin estar conectado a la red corporativa</td>
<td style="border:1px solid black;">Contiene las claves pública y privada del certificado, esta última cifrada con la clave pública del usuario que solicitó el certificado. Contiene, asimismo, la clave pública del servidor que emitió el certificado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Certificados de equipo de RMS</td>
<td style="border:1px solid black;">Identifica a un equipo o dispositivo que el sistema RMS considera de confianza.</td>
<td style="border:1px solid black;">Contiene la clave pública del equipo activado. La clave privada correspondiente se encuentra en la caja de seguridad del equipo.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Certificados de cuenta de permisos</td>
<td style="border:1px solid black;">Identifica a un usuario en el contexto de un equipo o dispositivo determinado.</td>
<td style="border:1px solid black;">Contiene las claves pública y privada del usuario, esta última cifrada con la clave pública del equipo activado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Licencias de publicación</td>
<td style="border:1px solid black;">Especifica los permisos que se aplican al contenido protegido con RMS.</td>
<td style="border:1px solid black;">Contiene la clave de contenido simétrica necesaria para descifrar el contenido que está cifrado con la clave pública del servidor que ha emitido la licencia.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Licencias de uso</td>
<td style="border:1px solid black;">Especifica los permisos que se aplican a contenido protegido con RMS en el contexto de un usuario autenticado específico.</td>
<td style="border:1px solid black;">Contiene la clave de contenido simétrica necesaria para descifrar el contenido, que se encuentra cifrada con la clave pública del usuario.</td>
</tr>
</tbody>
</table>
