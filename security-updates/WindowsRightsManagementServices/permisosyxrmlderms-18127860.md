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
<th>Permisos</th>
<th>Elementos XrML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Control total</p></td>
<td style="border:1px solid black;"><p>OWNER</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Ver permisos</p></td>
<td style="border:1px solid black;"><p>VIEWRIGHT</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Exportar (Guardar como)</p></td>
<td style="border:1px solid black;"><p>EXPORT</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Guardar</p></td>
<td style="border:1px solid black;"><p>EDIT</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Ver</p></td>
<td style="border:1px solid black;"><p>VIEW</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Imprimir</p></td>
<td style="border:1px solid black;"><p>PRINT</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Extraer</p></td>
<td style="border:1px solid black;"><p>EXTRACT</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Editar</p></td>
<td style="border:1px solid black;"><p>DOCEDIT</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Permitir macros</p></td>
<td style="border:1px solid black;"><p>OBJMODEL</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Reenviar</p></td>
<td style="border:1px solid black;"><p>FORWARD</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Responder</p></td>
<td style="border:1px solid black;"><p>REPLY</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Responder a todos</p></td>
<td style="border:1px solid black;"><p>REPLYALL</p></td>
</tr>
</tbody>
</table>
  
Una aplicación cliente de RMS también puede proporcionar una interfaz de usuario de forma que los autores pueden seleccionar determinados permisos para el contenido protegido sin utilizar una plantilla. En ese caso, la aplicación determina cómo se muestran los permisos al usuario y la correspondencia entre las opciones mostradas y los elementos XrML.
