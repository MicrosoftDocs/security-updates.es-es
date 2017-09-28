---
TOCTitle: Listas de revocaciones de RMS
Title: Listas de revocaciones de RMS
ms:assetid: '688d4dfa-c928-4b2f-8116-2f9e87d2b6f7'
ms:contentKeyID: 18127787
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720287(v=WS.10)'
---

Listas de revocaciones de RMS
=============================

Las listas de revocaciones especifican el contenido, las aplicaciones, los usuarios u otras entidades principales que han sido revocadas. Una organización puede incluir una entidad en una lista de revocaciones por una o varias de las siguientes razones:

-   Se ha desvelado una clave privada o se sospecha que está en una situación comprometida.
-   Un propietario solicita la revocación de una clave que se cree que está en una situación comprometida.
-   Una entidad principal ya no es válida (por ejemplo, un empleado que ha sido despedido).
-   Existe un problema de seguridad (por ejemplo, un certificado emitido a un equipo cliente que está en una situación comprometida).
-   Se requiere la repetición de la certificación debido a cambios en la autorización.
-   Los puntos vulnerables en la seguridad que existen en una aplicación compatible con RMS no la hacen apropiada para utilizar contenido altamente confidencial, o para cualquier contenido protegido.
-   Un fragmento de contenido que se distribuyó con anterioridad está desfasado o ya no es apropiado para su uso.

En la tabla siguiente, se describen las entidades que se pueden especificar en las listas de revocaciones, además de la información utilizada para identificar a cada una de ellas.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Entidad</th>
<th>Identificador</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Un grupo de licencias o certificados</p></td>
<td style="border:1px solid black;"><p>Id. o clave pública del emisor</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Un grupo de manifiestos de aplicaciones</p></td>
<td style="border:1px solid black;"><p>Id. o clave pública del emisor</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Una licencia o un certificado determinado</p></td>
<td style="border:1px solid black;"><p>Id. o algoritmo hash de la licencia</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Un manifiesto de aplicación determinado</p></td>
<td style="border:1px solid black;"><p>Id. o algoritmo hash de la licencia</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Una entidad principal determinada</p></td>
<td style="border:1px solid black;"><p>Id. o clave pública de la entidad principal</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Un fragmento de contenido determinado</p></td>
<td style="border:1px solid black;"><p>Id. del contenido</p></td>
</tr>
</tbody>
</table>
  
| ![](images/Cc720287.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |  
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| Para la revocación y la exclusión, todos los algoritmos hash son SHA-1 \[NIS94c\], una revisión del algoritmo hash seguro (SHA, Secure Hash Algorithm), especificado en el estándar de hash seguro (SHS, Secure Hash Standard, FIPS 180). SHA-1 se describe en el estándar ANSI X9.30 (parte 2). Para revocar mediante un manifiesto de la aplicación, debe extraer el Id., la clave pública o el algoritmo hash del emisor del manifiesto de la aplicación. Sin embargo, los manifiestos de aplicaciones están cifrados en base 64, para que la información no esté a la vista. Con el kit de desarrollo de software (SDK) de cliente de Rights Management, puede desarrollarse un programa utilizando los métodos **DRMConstructCertificateChain**, **DRMDeconstructCertificateChain** y **DRMDecode** para descodificar el manifiesto de la aplicación y obtener la información requerida. Si desea impedir que una aplicación utilice contenido protegido por RMS, considere el uso de la exclusión de aplicaciones para prohibir que el servidor de RMS les otorgue licencias de uso a estas aplicaciones. La limitación de exclusión implica que no puede evitar que alguien con una licencia de uso válida descifre contenido protegido por RMS. Para obtener más información sobre la exclusión de aplicaciones, vea Exclusión de aplicaciones en "Operación de un servidor de RMS", en esta recopilación de documentación. |
  
Las listas de revocaciones son archivos XrML que especifican los parámetros siguientes.
  
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
<td style="border:1px solid black;"><p>ISSUEDTIME</p></td>
<td style="border:1px solid black;"><p>Hora del sistema en que se creó el archivo XrML. Este parámetro lo usa la condición REFRESH que se incluye en una licencia de uso para determinar la antigüedad de la lista de revocaciones.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>ISSUER</p></td>
<td style="border:1px solid black;"><p>Nombre, Id. y dirección del emisor de la lista de revocaciones.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>PUBLICKEY</p></td>
<td style="border:1px solid black;"><p>Clave pública del emisor de la lista de revocaciones.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>REVOCATIONLIST</p></td>
<td style="border:1px solid black;"><p>Nombre, tipo e Id. de cada entidad revocada.</p></td>
</tr>
</tbody>
</table>
