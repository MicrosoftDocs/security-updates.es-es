---
TOCTitle: Modificación de la configuración de caché de Active Directory
Title: Modificación de la configuración de caché de Active Directory
ms:assetid: '8789a7a5-2065-4fae-9104-e0a70f1f2fb6'
ms:contentKeyID: 18127859
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747586(v=WS.10)'
---

Modificación de la configuración de caché de Active Directory
=============================================================

La configuración del Registro especifica el número de entradas que se almacenarán en la caché de Active Directory. Para mejorar el tiempo de respuesta de las solicitudes de clientes puede modificar esta configuración. Para obtener más información, vea "Optimización del rendimiento de los servicios de directorio", anteriormente en este tema. También puede especificar el período de validez de la información que se almacena en la caché.

En equipos con la versión de 32 bits de Windows Server 2003, la siguiente clave del Registro es la ruta de subclave completa para las entradas de la caché:

**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\DRMS\\1.0\\DirectoryServices**

En equipos con la versión de 64 bits de Windows Server 2003, la siguiente clave del Registro es la ruta de subclave completa para las entradas de la caché:

**HKEY\_LOCAL\_MACHINE\\SoftwareWOW6432Node\\Microsoft\\DRMS\\1.0\\DirectoryServices**

En la siguiente tabla, se muestran las entradas que controlan el comportamiento de la caché en memoria.

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
<th style="border:1px solid black;" >Tipo</th>
<th style="border:1px solid black;" >Valor predeterminado</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">PrincipalCacheMax</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">1,000</td>
<td style="border:1px solid black;">Número máximo de entidades principales y sus direcciones de correo electrónico y SID que se pueden almacenar en caché.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">PrincipalCacheExpireMinutes</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">12</td>
<td style="border:1px solid black;">Período de validez de la información de entidades principales almacenada en la caché.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">GroupIDCacheMax</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">1,000</td>
<td style="border:1px solid black;">Número máximo de grupos y sus direcciones de correo electrónico y SID que se pueden almacenar en la caché.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">GroupIDCacheExpireMinutes</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">12</td>
<td style="border:1px solid black;">Período de validez de la información de pertenencia a grupos almacenada en la caché.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">GroupMembershipCacheMax</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">1,000</td>
<td style="border:1px solid black;">Número máximo de contactos que pertenecen a un grupo que puede almacenarse en la caché.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">GroupMembershipCacheExpireMinutes</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">12</td>
<td style="border:1px solid black;">Período de validez de la información almacenada en la caché de contactos que pertenecen a un grupo.</td>
</tr>
</tbody>
</table>
  
> [!CAUTION]
> La edición incorrecta del Registro puede dañar gravemente el sistema. Antes de realizar cambios en el Registro, debe realizar una copia de seguridad de los datos de valor del equipo. 

  
> [!NOTE]
> Las entradas del Registro **PrincipalCacheExpireMinutes**, **GroupIDCacheExpireMinutes**, **GroupMembershipCacheExpireMinutes** y **ContactMembersofGroupCacheExpireMinutes** también controlan la caducidad de la caché en la caché local de Active Directory almacenado en la base de datos de servicios de directorio de su servidor de bases de datos. |
