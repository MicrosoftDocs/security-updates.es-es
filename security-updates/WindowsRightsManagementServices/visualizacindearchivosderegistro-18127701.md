---
TOCTitle: Visualización de archivos de registro
Title: Visualización de archivos de registro
ms:assetid: '2dc9ed54-76d8-4721-ba93-194845de726a'
ms:contentKeyID: 18127701
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720228(v=WS.10)'
---

Visualización de archivos de registro
=====================================

Dependiendo de la manera en que haya implementado RMS, los archivos de registro se almacenan en un servidor de base de datos como SQL Server o Microsoft SQL Server 2000 Desktop Engine (MSDE 2000) versión A. Puede escribir filtros para reducir la información que se almacena en los archivos de registro. Para obtener instrucciones, consulte la Ayuda del Administrador corporativo de SQL Server.

El tamaño de una entrada de registro típica es aproximadamente 300 bytes. La siguiente tabla describe los cambios que se registran.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>HostMachineName</p></td>
<td style="border:1px solid black;"><p>Equipo que procesa la solicitud.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>HostMachineRequestId</p></td>
<td style="border:1px solid black;"><p>Identifica inequívocamente esta solicitud en este equipo. La combinación de HostMachineName y HostMachineRequestId identifica inequívocamente la solicitud en el clúster.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>RequestTime</p></td>
<td style="border:1px solid black;"><p>Hora, en formato de hora universal coordenada (hora del meridiano de Greenwich), a la que se recibió la solicitud.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>RequestPath</p></td>
<td style="border:1px solid black;"><p>Dirección URL relativa del archivo .asmx, por ejemplo: /_wmcs/licensing/License.asmx.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>RequestType</p></td>
<td style="border:1px solid black;"><p>Nombre del método Web invocado, por ejemplo: AcquireLicense.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>RequestUserAddress</p></td>
<td style="border:1px solid black;"><p>Dirección IP de origen del solicitante.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>RequestUserAgent</p></td>
<td style="border:1px solid black;"><p>Valor de agente de usuario del encabezado HTTP.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>AuthenticatedState</p></td>
<td style="border:1px solid black;"><p>Si se autenticó la conexión HTTP (True/False).</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>SecureConnectionState</p></td>
<td style="border:1px solid black;"><p>Si se trata de una conexión SSL o no (True/False).</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>AuthenticatedId</p></td>
<td style="border:1px solid black;"><p>Nombre de inicio de sesión para solicitudes autenticadas. En blanco si AuthenticatedState=False.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>ReceivedXrMLDocument</p></td>
<td style="border:1px solid black;"><p>Documento XrML que se recibe del solicitante.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>ReceivedXrMLDocumentIssuerChain</p></td>
<td style="border:1px solid black;"><p>Cadena de emisor del archivo XrML recibido.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>IssuedXrMLDocument</p></td>
<td style="border:1px solid black;"><p>Documento XrML devuelto al solicitante.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>IssuedXrMLDocumentIssuerChain</p></td>
<td style="border:1px solid black;"><p>Cadena de emisor del archivo XrML emitido.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>SuccessOrFailure</p></td>
<td style="border:1px solid black;"><p>Si se aceptó o no la solicitud (Succeeded/Failed).</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Metadata</p></td>
<td style="border:1px solid black;"><p>Campo de metadatos.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>ErrorInformation</p></td>
<td style="border:1px solid black;"><p>Mensaje de error descriptivo, si se ha producido un error.</p></td>
</tr>  
</tbody>  
</table>
