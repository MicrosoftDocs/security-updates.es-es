---
TOCTitle: Certificados emisores de licencias de servidor
Title: Certificados emisores de licencias de servidor
ms:assetid: '0b35fbcd-25a9-4587-898d-9a30fd1d3c5b'
ms:contentKeyID: 18127682
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720184(v=WS.10)'
---

Certificados emisores de licencias de servidor
==============================================

Un certificado emisor de licencias de servidor otorga a un servidor de RMS el permiso para emitir certificados y licencias. Cuando se establecen los servicios en línea del primer servidor de certificación raíz de la implementación de RMS, éste recibe un certificado emisor de licencias de servidor del servicio de inscripción de Microsoft. Este proceso se conoce como inscripción. Este certificado contiene la clave pública del servidor de certificación raíz, y está firmado con la clave privada del servicio de inscripción. El resto de los servidores que se agreguen al clúster de certificación raíz compartirán este certificado.

Durante el establecimiento de servicios en línea, el primer servidor de licencias de un clúster recibe un certificado emisor de licencias de servidor desde el servidor o clúster de certificación raíz de RMS en un proceso que se denomina subinscripción. Este certificado contiene la clave pública del servidor de licencias, y está firmado con la clave privada del servidor o clúster de certificación raíz. El resto de los servidores que se agreguen al clúster de licencias compartirán este certificado.

En la tabla siguiente, se enumeran los permisos otorgados a los servidores por los certificados emisores de licencias de servidor.

###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Otorga el permiso para emitir</th>
<th style="border:1px solid black;" >Certificado emisor de licencias de servidor concedido a un servidor de certificación raíz</th>
<th style="border:1px solid black;" >Certificado emisor de licencias de servidor concedido a un servidor de licencias</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Certificados de cuenta de permisos</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">No</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Licencias de publicación</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">Sí</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Licencias de uso</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">Sí</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Certificados emisores de licencias de servidor subordinados</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">No</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Certificados emisores de licencias de cliente</td>
<td style="border:1px solid black;">Sí</td>
<td style="border:1px solid black;">Sí</td>
</tr>
</tbody>
</table>
  
| ![](images/Cc720184.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |  
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| RMS no requiere servidores ni clústeres de licencias independientes, pero se pueden usar para descargar solicitudes de licencias del clúster de certificación raíz Los administradores pueden instalar también servidores de licencias para ajustarse a las necesidades internas de organizaciones que requieran un control directo sobre la publicación de contenido seguro. Por ejemplo, puede haber casos en los que las directivas corporativas generales, implementadas en las plantillas de directiva de permisos del servidor o clúster de certificación raíz, no especifiquen algunos de los permisos necesarios para un departamento en particular. En estos casos, el departamento puede implementar un servidor o clúster de licencias para almacenar sus plantillas de directiva de permisos y administrar así sus solicitudes de licencias. |
