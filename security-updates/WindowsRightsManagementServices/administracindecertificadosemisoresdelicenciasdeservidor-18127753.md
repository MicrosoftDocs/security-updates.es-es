---
TOCTitle: Administración de certificados emisores de licencias de servidor
Title: Administración de certificados emisores de licencias de servidor
ms:assetid: '549979ad-13ee-4abc-8281-3e002a5a9561'
ms:contentKeyID: 18127753
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720272(v=WS.10)'
---

Administración de certificados emisores de licencias de servidor
================================================================

Los certificados emisores de licencias de servidor caducan después de un período de tiempo especificado, normalmente transcurrido un año. Para renovar un certificado emisor de licencias de servidor, debe iniciar sesión como administrador local. Cuando renueve el certificado emisor de licencias de servidor del clúster de certificación raíz, RMS enviará una solicitud para renovar el certificado emisor de licencias de servidor al servicio de inscripción de Microsoft. Cuando renueve el certificado de un servidor de licencias, RMS enviará la solicitud de renovación al servidor de certificación raíz que emitió el certificado que va a caducar.

Debe supervisar tres sucesos que RMS expondrá en el registro de sucesos del sistema. Estos sucesos le informan cuando el certificado emisor de licencias de servidor haya caducado o esté a punto de hacerlo. En la siguiente tabla, se enumeran los id. y los nombres de los sucesos.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Id. de suceso</th>
<th>Nombre del suceso</th>
<th>Tipo de suceso</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>16</p></td>
<td style="border:1px solid black;"><p>LicensorCertExpiresInOneMonthEvent</p></td>
<td style="border:1px solid black;"><p>Advertencia. El servicio continúa funcionando con normalidad.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>17</p></td>
<td style="border:1px solid black;"><p>LicensorCertExpiresInOneWeekEvent</p></td>
<td style="border:1px solid black;"><p>Advertencia. El servicio continúa funcionando con normalidad.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>18</p></td>
<td style="border:1px solid black;"><p>LicensorCertExpiredEvent</p></td>
<td style="border:1px solid black;"><p>Error. Se desactiva el servicio.</p></td>
</tr>  
</tbody>  
</table>
