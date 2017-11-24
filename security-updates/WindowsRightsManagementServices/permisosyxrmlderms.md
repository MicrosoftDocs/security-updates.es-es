---
TOCTitle: Permisos y XrML de RMS
Title: Permisos y XrML de RMS
ms:assetid: '7eb5cdd1-cd48-4b2b-96b6-fc74f7b42e7f'
ms:contentKeyID: 18127860
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747645(v=WS.10)'
---

Permisos y XrML de RMS
======================

En la siguiente tabla, se muestra cómo se corresponden los permisos que puede seleccionar para una plantilla de directiva de permisos con los elementos correctos que se encuentran en XrML.

###  

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Permisos</th>
<th style="border:1px solid black;" >Elementos XrML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Control total</td>
<td style="border:1px solid black;">OWNER</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Ver permisos</td>
<td style="border:1px solid black;">VIEWRIGHT</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Exportar (Guardar como)</td>
<td style="border:1px solid black;">EXPORT</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Guardar</td>
<td style="border:1px solid black;">EDIT</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Ver</td>
<td style="border:1px solid black;">VIEW</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Imprimir</td>
<td style="border:1px solid black;">PRINT</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Extraer</td>
<td style="border:1px solid black;">EXTRACT</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Editar</td>
<td style="border:1px solid black;">DOCEDIT</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Permitir macros</td>
<td style="border:1px solid black;">OBJMODEL</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Reenviar</td>
<td style="border:1px solid black;">FORWARD</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Responder</td>
<td style="border:1px solid black;">REPLY</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Responder a todos</td>
<td style="border:1px solid black;">REPLYALL</td>
</tr>
</tbody>
</table>
  
Una aplicación cliente de RMS también puede proporcionar una interfaz de usuario de forma que los autores pueden seleccionar determinados permisos para el contenido protegido sin utilizar una plantilla. En ese caso, la aplicación determina cómo se muestran los permisos al usuario y la correspondencia entre las opciones mostradas y los elementos XrML.
