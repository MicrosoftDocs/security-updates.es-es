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
<th style="border:1px solid black;" >Nombre</th>
<th style="border:1px solid black;" >Tipo de datos</th>
<th style="border:1px solid black;" >Valores NULL</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">i_MachineId</td>
<td style="border:1px solid black;">int</td>
<td style="border:1px solid black;">IDENTITY (1,1) No NULL</td>
<td style="border:1px solid black;">Índice interno</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">b_PubKeyHash</td>
<td style="border:1px solid black;">binary(20)</td>
<td style="border:1px solid black;">(20) No NULL</td>
<td style="border:1px solid black;">Algoritmo hash del id. de hardware</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">dt_CreateDate</td>
<td style="border:1px solid black;">datetime</td>
<td style="border:1px solid black;">No NULL</td>
<td style="border:1px solid black;">Fecha y hora en que se agregó la entrada a la tabla</td>
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
<th style="border:1px solid black;" >Nombre</th>
<th style="border:1px solid black;" >Tipo de datos</th>
<th style="border:1px solid black;" >Valores NULL</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">i_UserId</td>
<td style="border:1px solid black;">int</td>
<td style="border:1px solid black;">No NULL</td>
<td style="border:1px solid black;">Índice interno</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">i64_Puid</td>
<td style="border:1px solid black;">bigint</td>
<td style="border:1px solid black;">(50) NULL</td>
<td style="border:1px solid black;">Id. de usuario de .NET Passport</td>
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
<th style="border:1px solid black;" >Nombre</th>
<th style="border:1px solid black;" >Tipo de datos</th>
<th style="border:1px solid black;" >Valores NULL</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">i_MachineId</td>
<td style="border:1px solid black;">int</td>
<td style="border:1px solid black;">No NULL</td>
<td style="border:1px solid black;">Índice interno</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">i_UserId</td>
<td style="border:1px solid black;">int</td>
<td style="border:1px solid black;">No NULL</td>
<td style="border:1px solid black;">Índice interno</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">dt_CreateDate</td>
<td style="border:1px solid black;">datetime</td>
<td style="border:1px solid black;">No NULL</td>
<td style="border:1px solid black;">Fecha y hora en que se agregó la entrada a la tabla</td>
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
<th style="border:1px solid black;" >Nombre</th>
<th style="border:1px solid black;" >Tipo de datos</th>
<th style="border:1px solid black;" >Valores NULL</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">i_UserId</td>
<td style="border:1px solid black;">int</td>
<td style="border:1px solid black;">IDENTITY (1,1) No NULL</td>
<td style="border:1px solid black;">Índice interno</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">b_KeyData</td>
<td style="border:1px solid black;">varbinary(2000)</td>
<td style="border:1px solid black;">(2000) No NULL</td>
<td style="border:1px solid black;">Clave privada o pública de usuario cifrada</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">i_KeyDataLength</td>
<td style="border:1px solid black;">int</td>
<td style="border:1px solid black;">No NULL</td>
<td style="border:1px solid black;">Longitud de la clave privada / pública no cifrada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">b_PublicKey</td>
<td style="border:1px solid black;">PublicKey</td>
<td style="border:1px solid black;">No NULL</td>
<td style="border:1px solid black;">Clave pública de usuario</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">i_EncryptionDbId</td>
<td style="border:1px solid black;">int</td>
<td style="border:1px solid black;">No NULL</td>
<td style="border:1px solid black;">Índice para el certificado emisor de licencias utilizado para cifrar el par de claves pública y privada</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">s_Certificate</td>
<td style="border:1px solid black;">ntext</td>
<td style="border:1px solid black;">No especificado</td>
<td style="border:1px solid black;">No se utiliza</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">dt_Expiration</td>
<td style="border:1px solid black;">datetime</td>
<td style="border:1px solid black;">No NULL</td>
<td style="border:1px solid black;">Fecha de caducidad de la clave de usuario</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">dt_TemporaryExpiration</td>
<td style="border:1px solid black;">datetime</td>
<td style="border:1px solid black;">No NULL</td>
<td style="border:1px solid black;">Fecha y hora de caducidad del uso temporal de la clave</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">f_Modified</td>
<td style="border:1px solid black;">bit</td>
<td style="border:1px solid black;">No NULL</td>
<td style="border:1px solid black;">No se utiliza</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">i_Quota</td>
<td style="border:1px solid black;">int</td>
<td style="border:1px solid black;">No NULL</td>
<td style="border:1px solid black;">Nivel actual de la cuota para el usuario</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">i_WaitDays</td>
<td style="border:1px solid black;">int</td>
<td style="border:1px solid black;">No NULL</td>
<td style="border:1px solid black;">Número de días antes de que se admitan solicitudes de cuota adicionales</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">dt_LastConsumption</td>
<td style="border:1px solid black;">datetime</td>
<td style="border:1px solid black;">No NULL</td>
<td style="border:1px solid black;">Fecha y hora de la última certificación de usuario adicional</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">dt_CreateDate</td>
<td style="border:1px solid black;">datetime</td>
<td style="border:1px solid black;">No NULL</td>
<td style="border:1px solid black;">Fecha y hora en que se agregó la entrada a la tabla</td>
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
<th style="border:1px solid black;" >Nombre</th>
<th style="border:1px solid black;" >Tipo de datos</th>
<th style="border:1px solid black;" >Valores NULL</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">i_UserId</td>
<td style="border:1px solid black;">int</td>
<td style="border:1px solid black;">No NULL</td>
<td style="border:1px solid black;">Índice interno</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">s_Sid</td>
<td style="border:1px solid black;">Sid</td>
<td style="border:1px solid black;">No NULL</td>
<td style="border:1px solid black;">Id. de seguridad (SID) del usuario</td>
</tr>
</tbody>
</table>
