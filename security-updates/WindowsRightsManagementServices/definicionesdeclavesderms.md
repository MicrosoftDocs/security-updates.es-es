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
<th style="border:1px solid black;" >Clave</th>
<th style="border:1px solid black;" >Uso</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Claves de servidor</td>
<td style="border:1px solid black;"><strong>Clave pública</strong></br></br>
Cifra la clave de contenido que se encuentra en una licencia de publicación, de forma que sólo el servidor de RMS pueda recuperar esta clave y emitir licencias de uso para esa licencia de publicación.</br></br>
<strong>Clave privada</strong></br></br>
Firma todos los certificados y licencias que emita el servidor.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Claves de equipo</td>
<td style="border:1px solid black;"><strong>Clave pública</strong></br></br>
Cifra una clave privada del certificado de cuenta de permisos.</br></br>
<strong>Clave privada</strong></br></br>
Descifra un certificado de cuenta de permisos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Claves de emisor de licencias de cliente</td>
<td style="border:1px solid black;"><strong>Clave pública</strong></br></br>
Cifra la clave de contenido simétrica de las licencias de publicación que emite.</br></br>
<strong>Clave privada</strong></br></br>
Firma las licencias de publicación que se emiten localmente mientras el usuario no está conectado a la red.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Claves de usuario</td>
<td style="border:1px solid black;"><strong>Clave pública</strong></br></br>
Cifra la clave de contenido que se encuentra en una licencia de uso, de forma que sólo un usuario determinado pueda utilizar contenido protegido con RMS con esta licencia.</br></br>
<strong>Clave privada</strong></br></br>
Permite a un usuario utilizar contenido protegido con RMS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Claves de contenido</td>
<td style="border:1px solid black;">Cifra el contenido protegido con RMS cuando el autor lo publica.</td>
</tr>
</tbody>
</table>
