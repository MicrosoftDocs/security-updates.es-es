---
TOCTitle: Tablas principales de la base de datos de configuración de RMS
Title: Tablas principales de la base de datos de configuración de RMS
ms:assetid: '8f9e15a2-92bc-41f7-a4fd-329567afb142'
ms:contentKeyID: 18127891
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747676(v=WS.10)'
---

Tablas principales de la base de datos de configuración de RMS
==============================================================

En este tema se describen las tablas principales de la base de datos de configuración de RMS.

DRMS\_ApplicationExclusionList
------------------------------

En la siguiente tabla, se muestra información acerca de las aplicaciones excluidas.

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
<td style="border:1px solid black;"><p>ID</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>IDENTITY (100,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Nombre</p></td>
<td style="border:1px solid black;"><p>nvarchar(256)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Nombre de aplicación</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>VersionMinMajor</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Número de versión mínima principal de la aplicación</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>VersionMinMinor</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Número de versión mínima menor de la aplicación</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>VersionMinBuild</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Número de versión de compilación mínima de la aplicación</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>VersionMinRevision</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Número de versión de revisión mínima de la aplicación</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>VersionMaxMajor</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Número de versión principal máxima de la aplicación</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>VersionMaxMinor</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Número de versión menor máxima de la aplicación</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>VersionMaxBuild</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Número de versión de compilación máxima de la aplicación</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>VersionMaxRevision</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Número de versión de revisión máxima de la aplicación</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Descripción</p></td>
<td style="border:1px solid black;"><p>nvarchar(256)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Descripción de la aplicación</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>dt_DateUpdated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de actualización</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>dt_DateCreated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de creación</p></td>
</tr>
</tbody>
</table>
  
DRMS\_AsynchronousQueue  
-----------------------
  
En la siguiente tabla, se muestra información acerca de la cola de mensajes.
  
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
<td style="border:1px solid black;"><p>AsyncQueueID</p></td>
<td style="border:1px solid black;"><p>Int (PK)</p></td>
<td style="border:1px solid black;"><p>IDENTITY (100,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>QueueName</p></td>
<td style="border:1px solid black;"><p>nvarchar(256)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Ruta de la cola de mensajes</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DateUpdated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de actualización</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DateCreated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de creación</p></td>
</tr>
</tbody>
</table>
  
DRMS\_CaType  
------------
  
En la siguiente tabla, se muestra información sobre el tipo de certificado emitido para el cliente.
  
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
<td style="border:1px solid black;"><p>ID</p></td>
<td style="border:1px solid black;"><p>Int (PK)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>El Id. para el certificado</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>TypeName</p></td>
<td style="border:1px solid black;"><p>nvarchar(256)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Escritorio, Dispositivo móvil o Servidor</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DateUpdated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de actualización</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DateCreated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de creación</p></td>
</tr>
</tbody>
</table>
  
DRMS\_ClusterConfiguration  
--------------------------
  
En la siguiente tabla, se muestra información sobre el certificado emisor de licencias de servidor actual que se encuentra en la tabla DRMS\_LicensorCertificate.
  
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
<td style="border:1px solid black;"><p>CurrentLicensorCertID</p></td>
<td style="border:1px solid black;"><p>int (FK)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Certificado emisor de licencias activo</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DateUpdated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de actualización</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DateCreated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de creación</p></td>
</tr>
</tbody>
</table>
  
DRMS\_ClusterPolicies  
---------------------
  
En la siguiente tabla, se muestra información sobre las ubicaciones en las que se almacenan las directivas de clúster.
  
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
<td style="border:1px solid black;"><p>PolicyID</p></td>
<td style="border:1px solid black;"><p>Int (PK)</p></td>
<td style="border:1px solid black;"><p>IDENTITY (100,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Id. de la directiva</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>PolicyName</p></td>
<td style="border:1px solid black;"><p>nvarchar(64)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Nombre de la directiva</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>PolicyData</p></td>
<td style="border:1px solid black;"><p>sql_variant</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Datos de la directiva</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DateUpdated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de actualización</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DateCreated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de creación</p></td>
</tr>
</tbody>
</table>
  
DRMS\_ClusterServer  
-------------------
  
En la siguiente tabla, se muestra información sobre los servidores que se encuentran en el clúster.
  
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
<td style="border:1px solid black;"><p>ServerID</p></td>
<td style="border:1px solid black;"><p>Int (PK)</p></td>
<td style="border:1px solid black;"><p>IDENTITY (100,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Id. del servidor</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>ServerName</p></td>
<td style="border:1px solid black;"><p>nvarchar(256)</p></td>
<td style="border:1px solid black;"><p>No especificado</p></td>
<td style="border:1px solid black;"><p>Nombre de equipo del servidor</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DateUpdated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de actualización</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DateCreated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de creación</p></td>
</tr>
</tbody>
</table>
  
DRMS\_GICExclusionList  
----------------------
  
En la siguiente tabla, se muestra información sobre los certificados de cuenta de permisos excluidos.
  
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
<td style="border:1px solid black;"><p>PublicKeyIndex</p></td>
<td style="border:1px solid black;"><p>Int (PK)</p></td>
<td style="border:1px solid black;"><p>IDENTITY (100,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>PublicKey</p></td>
<td style="border:1px solid black;"><p>PublicKey</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Bytes de clave pública</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>UserID</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Índice de id. de usuario</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>ExpirationDate</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Fecha en la que caduca el certificado de cuenta de permisos</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Descripción</p></td>
<td style="border:1px solid black;"><p>nvarchar(256)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Nombre (NAME) asociado con esta clave de certificado de cuenta de permisos excluida</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>dt_DateUpdated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de actualización</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>dt_DateCreated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de creación</p></td>
</tr>
</tbody>
</table>
  
DRMS\_LicensorCertificate  
-------------------------
  
En la siguiente tabla, se muestra información sobre el certificado emisor de licencias de servidor activo.
  
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
<td style="border:1px solid black;"><p>i_CertID</p></td>
<td style="border:1px solid black;"><p>Int (PK)</p></td>
<td style="border:1px solid black;"><p>IDENTITY (100,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Id. de la directiva</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>s_CertGUIDType</p></td>
<td style="border:1px solid black;"><p>nvarchar(64)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Tipo de id. de par de claves</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>s_CertGUID</p></td>
<td style="border:1px solid black;"><p>nvarchar(128)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>GUID de id. de par de claves</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>i_CertificateID</p></td>
<td style="border:1px solid black;"><p>int (FK)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Puntero para el certificado real</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>dt_DateUpdated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de actualización</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>dt_DateCreated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de creación</p></td>
</tr>
</tbody>
</table>
  
DRMS\_LicensorPrivateKey  
------------------------
  
La siguiente tabla contiene información sobre la clave privada del certificado emisor de licencias de servidor activo.
  
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
<td style="border:1px solid black;"><p>PrivateKeyID</p></td>
<td style="border:1px solid black;"><p>Int (PK)</p></td>
<td style="border:1px solid black;"><p>IDENTITY (100,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>CertGUIDType</p></td>
<td style="border:1px solid black;"><p>nvarchar(64)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Tipo de id. de par de claves</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>CertGUID</p></td>
<td style="border:1px solid black;"><p>nvarchar(128)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>GUID de id. de par de claves</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>PrivateKey</p></td>
<td style="border:1px solid black;"><p>varbinary(2048)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Representación binaria de la clave</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>CSP</p></td>
<td style="border:1px solid black;"><p>nvarchar(512)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Nombre del proveedor de servicios de cifrado (CSP)</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>CSPType</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Tipo de CSP</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>KeyContainerName</p></td>
<td style="border:1px solid black;"><p>nvarchar(512)</p></td>
<td style="border:1px solid black;"><p>No especificado</p></td>
<td style="border:1px solid black;"><p>Nombre del contenedor de la clave</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>KeyNumber</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Número de clave</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DateUpdated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de actualización</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DateCreated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de creación</p></td>
</tr>
</tbody>
</table>
  
DRMS\_PassportDenyList  
----------------------
  
En la siguiente tabla, se muestra información sobre las cuentas de Microsoft® .NET Passport a las que se deben denegar licencias.
  
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
<td style="border:1px solid black;"><p>DenyID</p></td>
<td style="border:1px solid black;"><p>Int (PK)</p></td>
<td style="border:1px solid black;"><p>IDENTITY (100,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DenyAddressPattern</p></td>
<td style="border:1px solid black;"><p>nvarchar(500)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Nombre de usuario o nombre de dominio</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DateUpdated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de actualización</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DateCreated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de creación</p></td>
</tr>
</tbody>
</table>
  
DRMS\_Plugin  
------------
  
En la siguiente tabla, se muestra información acerca de los complementos.
  
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
<td style="border:1px solid black;"><p>PluginID</p></td>
<td style="border:1px solid black;"><p>Int</p></td>
<td style="border:1px solid black;"><p>IDENTITY (100,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>PluginTypeID</p></td>
<td style="border:1px solid black;"><p>int (FK)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Tipo de complemento</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>NameSpace</p></td>
<td style="border:1px solid black;"><p>nvarchar(128)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Espacio de nombres para este complemento</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>PluginName</p></td>
<td style="border:1px solid black;"><p>nvarchar(128)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Nombre de este complemento</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Ordinal</p></td>
<td style="border:1px solid black;"><p>Int</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Número de secuencia en la que se ejecuta el complemento</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Path</p></td>
<td style="border:1px solid black;"><p>nvarchar(512)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Ruta del archivo DLL</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>ObjectTypeName</p></td>
<td style="border:1px solid black;"><p>nvarchar(50)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>No se utiliza</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DebugMode</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Especifica si se ejecuta un complemento en modo de depuración</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>PublicKey</p></td>
<td style="border:1px solid black;"><p>PublicKey</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Clave pública del complemento</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Version</p></td>
<td style="border:1px solid black;"><p>nvarchar(64)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Versión del complemento</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DateUpdated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de actualización</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DateCreated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de creación</p></td>
</tr>
</tbody>
</table>
  
DRMS\_AllowedPluginVersions  
---------------------------
  
En la siguiente tabla, se muestra información acerca de las versiones de los complementos permitidas en el sistema RMS.
  
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
<td style="border:1px solid black;"><p>RowID</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>PluginID</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>IDENTITY (100,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>VersionInfo</p></td>
<td style="border:1px solid black;"><p>nvarchar(64)</p></td>
<td style="border:1px solid black;"><p>No especificado</p></td>
<td style="border:1px solid black;"><p>Versión del complemento</p></td>
</tr>
</tbody>
</table>
  
DRMS\_PluginProperties  
----------------------
  
En la siguiente tabla, se muestra información acerca de las propiedades de complementos.
  
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
<td style="border:1px solid black;"><p>PropertyID</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>IDENTITY (100,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>PluginID</p></td>
<td style="border:1px solid black;"><p>int (FK)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Id. del complemento al que pertenece la propiedad</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>PropertyName</p></td>
<td style="border:1px solid black;"><p>nvarchar(256)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Nombre de la propiedad para estos datos de configuración</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>PropertyValue</p></td>
<td style="border:1px solid black;"><p>text</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Valor de la propiedad para estos datos de configuración</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DateUpdated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de actualización</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DateCreated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de creación</p></td>
</tr>
</tbody>
</table>
  
DRMS\_PluginType  
----------------
  
En la siguiente tabla, se muestra información acerca del tipo de complemento.
  
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
<td style="border:1px solid black;"><p>PluginTypeID</p></td>
<td style="border:1px solid black;"><p>Int (PK)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>PluginTypeName</p></td>
<td style="border:1px solid black;"><p>nvarchar(256)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Nombre de este complemento</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DateUpdated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de actualización</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DateCreated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de creación</p></td>
</tr>
</tbody>
</table>
  
DRMS\_RightsTemplate  
--------------------
  
En la siguiente tabla, se muestra información acerca de las plantillas de directiva de permisos.
  
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
<td style="border:1px solid black;"><p>Guid</p></td>
<td style="border:1px solid black;"><p>nvarchar(128) (PK)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>GUID de la plantilla de directiva de permisos</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>TemplateData</p></td>
<td style="border:1px solid black;"><p>ntext</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Este campo contiene los datos de la plantilla XrML.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DateUpdated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de actualización</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DateCreated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de creación</p></td>
</tr>
</tbody>
</table>
  
DRMS\_TrustedCertificateAuthorities  
-----------------------------------
  
En la siguiente tabla, se muestra información acerca de las entidades emisoras de certificados de confianza.
  
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
<td style="border:1px solid black;"><p>ID</p></td>
<td style="border:1px solid black;"><p>Int (PK)</p></td>
<td style="border:1px solid black;"><p>IDENTITY(1,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>CertificateID</p></td>
<td style="border:1px solid black;"><p>int (FK)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Id. del certificado</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>CertificateGUID</p></td>
<td style="border:1px solid black;"><p>nvarchar(128)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>GUID del certificado</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>CaTypeID</p></td>
<td style="border:1px solid black;"><p>int (FK)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Tipo de entidad emisora de certificados</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DateUpdated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de actualización</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DateCreated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de creación</p></td>
</tr>
</tbody>
</table>
  
DRMS\_TrustedEmailDomains  
-------------------------
  
En la siguiente tabla, se muestra información sobre los dominios de correo electrónico de confianza en el entorno RMS.
  
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
<td style="border:1px solid black;"><p>ID</p></td>
<td style="border:1px solid black;"><p>int (PK)</p></td>
<td style="border:1px solid black;"><p>IDENTITY (100,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>i_TrustedIdentityDomainID</p></td>
<td style="border:1px solid black;"><p>int (FK)t</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>s_EmailDomainName</p></td>
<td style="border:1px solid black;"><p>nvarchar(256)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Lista de nombres de dominio de correo electrónico que son válidos para el dominio de usuario de confianza</p></td>
</tr>
</tbody>
</table>
  
DRMS\_TrustedIdentityDomain  
---------------------------
  
En la siguiente tabla, se muestra información acerca de los dominios de usuarios de confianza y los dominios de publicación de confianza.
  
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
<td style="border:1px solid black;"><p>i_TrustedIdentityDomainID</p></td>
<td style="border:1px solid black;"><p>Int (PK)</p></td>
<td style="border:1px solid black;"><p>IDENTITY (100,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>s_DomainType</p></td>
<td style="border:1px solid black;"><p>nvarchar(64)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Tipo de dominio</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>CertGUIDType</p></td>
<td style="border:1px solid black;"><p>nvarchar(64)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Tipo de GUID de certificado</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>CertGUID</p></td>
<td style="border:1px solid black;"><p>nvarchar(128)</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>GUID del certificado</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>i_CertificateID</p></td>
<td style="border:1px solid black;"><p>int (FK)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Id. del certificado</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>i_allowSID</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>SID del dominio</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>S_friendlyname</p></td>
<td style="border:1px solid black;"><p>nvarchar(255)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Nombre descriptivo del certificado</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>dt_DateUpdated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de actualización</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>dt_DateCreated</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Marca de tiempo de creación</p></td>
</tr>
</tbody>
</table>
  
DRMS\_XrML\_Certificate  
-----------------------
  
En la siguiente tabla, se muestra información acerca de los certificados emisores de licencias de servidor XrML a los que se hace referencia en la tabla DRMS\_LicensorCertificate. También sirve de mapa de la cadena de certificados.
  
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
<td style="border:1px solid black;"><p>i_CertificateID</p></td>
<td style="border:1px solid black;"><p>Int (PK)</p></td>
<td style="border:1px solid black;"><p>IDENTITY (100,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Puntero para el certificado real</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>s_Certificate</p></td>
<td style="border:1px solid black;"><p>ntext</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Puntero para el certificado real</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>i_ParentCertificateID</p></td>
<td style="border:1px solid black;"><p>int (FK)</p></td>
<td style="border:1px solid black;"><p>NULL</p></td>
<td style="border:1px solid black;"><p>Puntero para el certificado real</p></td>
</tr>
</tbody>
</table>
