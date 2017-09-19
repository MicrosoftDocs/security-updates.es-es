---
TOCTitle: Tablas de la base de datos de registro de RMS
Title: Tablas de la base de datos de registro de RMS
ms:assetid: '7ab2104c-b12d-4807-8a4b-bcabb145ff9b'
ms:contentKeyID: 18127823
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747569(v=WS.10)'
---

Tablas de la base de datos de registro de RMS
=============================================

En esta sección se describen las tablas de la base de datos de registro de RMS.

DRMS\_Log\_Master
-----------------

En la siguiente tabla, se muestra una entrada de cada registro.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre</th>
<th>Tipo de datos</th>
<th>Valores NULL</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>i_LogID</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>IDENTITY (100,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Id. único de este registro</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>s_HostMachineName</p></td>
<td style="border:1px solid black;"><p>nvarchar(64)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Servidor que generó este registro</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>s_HostMachineRequestId</p></td>
<td style="border:1px solid black;"><p>nvarchar(64)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Id. de solicitud</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>dt_RequestTime</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Fecha y hora de la solicitud</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>s_RequestPath</p></td>
<td style="border:1px solid black;"><p>nvarchar(128)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Ruta URL de la solicitud</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>s_RequestType</p></td>
<td style="border:1px solid black;"><p>nvarchar(64)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Tipo de solicitud</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>s_RequestUserAddress</p></td>
<td style="border:1px solid black;"><p>nvarchar(32)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Dirección IP del cliente</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>s_RequestUserAgent</p></td>
<td style="border:1px solid black;"><p>nvarchar(128)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Encabezado de agente de usuario del cliente</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>s_AuthenticatedState</p></td>
<td style="border:1px solid black;"><p>nvarchar(64)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Estado de autenticación de la solicitud</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>s_SecureConnectionState</p></td>
<td style="border:1px solid black;"><p>nvarchar(64)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Protección SSL de la solicitud</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>s_AuthenticatedId</p></td>
<td style="border:1px solid black;"><p>nvarchar(128)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Id. del usuario autenticado</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>s_ReceivedXrML</p></td>
<td style="border:1px solid black;"><p>ntext</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>XrML recibido del cliente de la solicitud</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>s_IssuedXrML</p></td>
<td style="border:1px solid black;"><p>ntext</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Licencia XrML emitida en la solicitud</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>s_Metadata</p></td>
<td style="border:1px solid black;"><p>ntext</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Metadata</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>s_SuccessOrFailure</p></td>
<td style="border:1px solid black;"><p>nvarchar(32)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Procesamiento o no procesamiento de la solicitud</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>s_ErrorInformation</p></td>
<td style="border:1px solid black;"><p>ntext</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Datos de error</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>dt_LogCreateTime</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Hora de creación del registro</p></td>
</tr>  
</tbody>  
</table>
  
DRMS\_Log\_Detail  
-----------------
  
En la siguiente tabla, se muestran datos adicionales para un registro. Normalmente se registran datos XrML en esta tabla.
  
###  

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="25%" />  
<col width="25%" />  
<col width="25%" />  
<col width="25%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th>Nombre</th>  
<th>Tipo de datos</th>  
<th>Valores NULL</th>  
<th>Descripción</th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>i_LogDetailID</p></td>
<td style="border:1px solid black;"><p>int (PK)</p></td>
<td style="border:1px solid black;"><p>IDENTITY(100,1)</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>i_LogID</p></td>
<td style="border:1px solid black;"><p>int (FK)</p></td>
<td style="border:1px solid black;"><p>No NULL (FK)</p></td>
<td style="border:1px solid black;"><p>Id. del registro principal</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>s_Name</p></td>
<td style="border:1px solid black;"><p>nvarchar(128)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Nombre de la propiedad</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>s_Value</p></td>
<td style="border:1px solid black;"><p>ntext</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Valor de la propiedad</p></td>
</tr>  
</tbody>  
</table>
  
DRMS\_Log\_Filter  
-----------------
  
En la siguiente tabla, se muestran los campos que registra el servicio de escucha de registro.
  
###  

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="25%" />  
<col width="25%" />  
<col width="25%" />  
<col width="25%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th>Nombre</th>  
<th>Tipo de datos</th>  
<th>Valores NULL</th>  
<th>Descripción</th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>i_ID</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>IDENTITY (100,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>s_FieldName</p></td>
<td style="border:1px solid black;"><p>nvarchar(255)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Nombre del campo</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>s_FieldDescription</p></td>
<td style="border:1px solid black;"><p>nvarchar(1024)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Descripción del campo</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>i_IsIncluded</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Indica si el campo está registrado</p></td>
</tr>  
</tbody>  
</table>
