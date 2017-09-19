---
TOCTitle: Revocación en plantillas de directiva de permisos
Title: Revocación en plantillas de directiva de permisos
ms:assetid: '287c5b92-fcb5-4295-9c2b-4e37e643beb2'
ms:contentKeyID: 18127762
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720226(v=WS.10)'
---

Revocación en plantillas de directiva de permisos
=================================================

Las condiciones de revocación se especifican en las plantillas de directiva de permisos. Los valores de la condición de revocación que se escriban en una de estas plantillas se capturan en una etiqueta XrML REFRESH de la licencia de publicación emitida para esa plantilla. La licencia de uso resultante que emite el servidor contiene también la etiqueta REFRESH.

En la tabla siguiente, se enumeran los parámetros de la etiqueta REFRESH.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parámetro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>ID</p></td>
<td style="border:1px solid black;"><p>Id. de la lista de revocaciones.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>ADDRESS</p></td>
<td style="border:1px solid black;"><p>Dirección URL o ruta UNC en que se puede obtener la lista de revocaciones.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>PUBLICKEY</p></td>
<td style="border:1px solid black;"><p>Clave pública del emisor de la lista de revocaciones. Esta clave pública corresponde a la clave privada que se utilizó para firmar la lista de revocaciones.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>INTERVALTIME</p></td>
<td style="border:1px solid black;"><p>Duración máxima de la lista de revocaciones expresada en días. Si la lista de revocaciones de la caché es más antigua que el intervalo INTERVALTIME admitido, el cliente de RMS obtiene la lista de revocaciones más reciente de la dirección URL especificada en el parámetro ADDRESS, lo que garantiza la utilización de una lista de revocaciones actualizada.</p></td>
</tr>  
</tbody>  
</table>
  
Para obtener más información sobre cómo crear plantillas de directiva de permisos, vea "Creación y modificación de plantillas de directiva de permisos" en "Operación de un servidor de RMS", en esta recopilación de documentación.
