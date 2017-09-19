---
TOCTitle: Tablas de certificación de la base de datos de configuración de RMS
Title: Tablas de certificación de la base de datos de configuración de RMS
ms:assetid: 'd392663a-1a46-42f6-a71d-f0f2c1843566'
ms:contentKeyID: 18127972
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747760(v=WS.10)'
---

Tablas de certificación de la base de datos de configuración de RMS
===================================================================

En este tema, se describen las tablas de certificación que se encuentran en la base de datos de configuración de RMS. Las tablas contienen información acerca de los certificados de cuenta de permisos que se emiten para usuarios de esta instalación.

UD\_Machines
------------

En la siguiente tabla, se muestran los id. de hardware de todos los equipos.

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
<td style="border:1px solid black;"><p>i_MachineId</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>IDENTITY (1,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>b_PubKeyHash</p></td>
<td style="border:1px solid black;"><p>binary(20)</p></td>
<td style="border:1px solid black;"><p>(20) No NULL</p></td>
<td style="border:1px solid black;"><p>Algoritmo hash del id. de hardware</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>dt_CreateDate</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Fecha y hora en que se agregó la entrada a la tabla</p></td>
</tr>  
</tbody>  
</table>
  
UD\_PassportAuthIdentities  
--------------------------
  
En la siguiente tabla, se muestra la información de Microsoft® .NET Passport de los usuarios.
  
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
<td style="border:1px solid black;"><p>i_UserId</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>i64_Puid</p></td>
<td style="border:1px solid black;"><p>bigint</p></td>
<td style="border:1px solid black;"><p>(50) NULL</p></td>
<td style="border:1px solid black;"><p>Id. de usuario de .NET Passport</p></td>
</tr>  
</tbody>  
</table>
  
UD\_UserMachine  
---------------
  
La siguiente tabla vincula los usuarios certificados con su información de equipo correspondiente.
  
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
<td style="border:1px solid black;"><p>i_MachineId</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>i_UserId</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>dt_CreateDate</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Fecha y hora en que se agregó la entrada a la tabla</p></td>
</tr>  
</tbody>  
</table>
  
UD\_Users  
---------
  
En la siguiente tabla, se muestra información acerca de los datos de usuario.
  
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
<td style="border:1px solid black;"><p>i_UserId</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>IDENTITY (1,1) No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>b_KeyData</p></td>
<td style="border:1px solid black;"><p>varbinary(2000)</p></td>
<td style="border:1px solid black;"><p>(2000) No NULL</p></td>
<td style="border:1px solid black;"><p>Clave privada o pública de usuario cifrada</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>i_KeyDataLength</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Longitud de la clave privada / pública no cifrada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>b_PublicKey</p></td>
<td style="border:1px solid black;"><p>PublicKey</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Clave pública de usuario</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>i_EncryptionDbId</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Índice para el certificado emisor de licencias utilizado para cifrar el par de claves pública y privada</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>s_Certificate</p></td>
<td style="border:1px solid black;"><p>ntext</p></td>
<td style="border:1px solid black;"><p>No especificado</p></td>
<td style="border:1px solid black;"><p>No se utiliza</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>dt_Expiration</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Fecha de caducidad de la clave de usuario</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>dt_TemporaryExpiration</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Fecha y hora de caducidad del uso temporal de la clave</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>f_Modified</p></td>
<td style="border:1px solid black;"><p>bit</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>No se utiliza</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>i_Quota</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Nivel actual de la cuota para el usuario</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>i_WaitDays</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Número de días antes de que se admitan solicitudes de cuota adicionales</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>dt_LastConsumption</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Fecha y hora de la última certificación de usuario adicional</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>dt_CreateDate</p></td>
<td style="border:1px solid black;"><p>datetime</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Fecha y hora en que se agregó la entrada a la tabla</p></td>
</tr>  
</tbody>  
</table>
  
UD\_Windows AuthIdentities  
--------------------------
  
En la siguiente tabla, se muestran los id. de todos los usuarios certificados y autenticados de Windows.
  
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
<td style="border:1px solid black;"><p>i_UserId</p></td>
<td style="border:1px solid black;"><p>int</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Índice interno</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>s_Sid</p></td>
<td style="border:1px solid black;"><p>Sid</p></td>
<td style="border:1px solid black;"><p>No NULL</p></td>
<td style="border:1px solid black;"><p>Id. de seguridad (SID) del usuario</p></td>
</tr>  
</tbody>  
</table>
