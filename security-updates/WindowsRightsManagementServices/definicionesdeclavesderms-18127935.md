---
TOCTitle: Definiciones de claves de RMS
Title: Definiciones de claves de RMS
ms:assetid: 'b052305c-1db7-434a-bad9-26d704156776'
ms:contentKeyID: 18127935
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747729(v=WS.10)'
---

Definiciones de claves de RMS
=============================

En la tabla siguiente se muestran las claves que se utilizan en un sistema RMS.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Clave</th>
<th>Uso</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Claves de servidor</p></td>
<td style="border:1px solid black;"><p><strong>Clave pública</strong></p>
<p>Cifra la clave de contenido que se encuentra en una licencia de publicación, de forma que sólo el servidor de RMS pueda recuperar esta clave y emitir licencias de uso para esa licencia de publicación.</p>  
<p><strong>Clave privada</strong></p>
<p>Firma todos los certificados y licencias que emita el servidor.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Claves de equipo</p></td>
<td style="border:1px solid black;"><p><strong>Clave pública</strong></p>
<p>Cifra una clave privada del certificado de cuenta de permisos.</p>  
<p><strong>Clave privada</strong></p>
<p>Descifra un certificado de cuenta de permisos.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Claves de emisor de licencias de cliente</p></td>
<td style="border:1px solid black;"><p><strong>Clave pública</strong></p>
<p>Cifra la clave de contenido simétrica de las licencias de publicación que emite.</p>  
<p><strong>Clave privada</strong></p>
<p>Firma las licencias de publicación que se emiten localmente mientras el usuario no está conectado a la red.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Claves de usuario</p></td>
<td style="border:1px solid black;"><p><strong>Clave pública</strong></p>
<p>Cifra la clave de contenido que se encuentra en una licencia de uso, de forma que sólo un usuario determinado pueda utilizar contenido protegido con RMS con esta licencia.</p>  
<p><strong>Clave privada</strong></p>
<p>Permite a un usuario utilizar contenido protegido con RMS.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Claves de contenido</p></td>
<td style="border:1px solid black;"><p>Cifra el contenido protegido con RMS cuando el autor lo publica.</p></td>
</tr>  
</tbody>  
</table>
