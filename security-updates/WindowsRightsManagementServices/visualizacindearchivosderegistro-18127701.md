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
<td style="border:1px solid black;">HostMachineName</td>
<td style="border:1px solid black;">Equipo que procesa la solicitud.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">HostMachineRequestId</td>
<td style="border:1px solid black;">Identifica inequívocamente esta solicitud en este equipo. La combinación de HostMachineName y HostMachineRequestId identifica inequívocamente la solicitud en el clúster.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">RequestTime</td>
<td style="border:1px solid black;">Hora, en formato de hora universal coordenada (hora del meridiano de Greenwich), a la que se recibió la solicitud.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">RequestPath</td>
<td style="border:1px solid black;">Dirección URL relativa del archivo .asmx, por ejemplo: /_wmcs/licensing/License.asmx.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">RequestType</td>
<td style="border:1px solid black;">Nombre del método Web invocado, por ejemplo: AcquireLicense.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">RequestUserAddress</td>
<td style="border:1px solid black;">Dirección IP de origen del solicitante.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">RequestUserAgent</td>
<td style="border:1px solid black;">Valor de agente de usuario del encabezado HTTP.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">AuthenticatedState</td>
<td style="border:1px solid black;">Si se autenticó la conexión HTTP (True/False).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SecureConnectionState</td>
<td style="border:1px solid black;">Si se trata de una conexión SSL o no (True/False).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">AuthenticatedId</td>
<td style="border:1px solid black;">Nombre de inicio de sesión para solicitudes autenticadas. En blanco si AuthenticatedState=False.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">ReceivedXrMLDocument</td>
<td style="border:1px solid black;">Documento XrML que se recibe del solicitante.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ReceivedXrMLDocumentIssuerChain</td>
<td style="border:1px solid black;">Cadena de emisor del archivo XrML recibido.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">IssuedXrMLDocument</td>
<td style="border:1px solid black;">Documento XrML devuelto al solicitante.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">IssuedXrMLDocumentIssuerChain</td>
<td style="border:1px solid black;">Cadena de emisor del archivo XrML emitido.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SuccessOrFailure</td>
<td style="border:1px solid black;">Si se aceptó o no la solicitud (Succeeded/Failed).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Metadata</td>
<td style="border:1px solid black;">Campo de metadatos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">ErrorInformation</td>
<td style="border:1px solid black;">Mensaje de error descriptivo, si se ha producido un error.</td>
</tr>
</tbody>
</table>
