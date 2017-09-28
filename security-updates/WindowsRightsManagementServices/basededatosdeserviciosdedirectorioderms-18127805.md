---
TOCTitle: Base de datos de servicios de directorio de RMS
Title: Base de datos de servicios de directorio de RMS
ms:assetid: '6f6b8586-5d17-4a40-94a3-4dc738195301'
ms:contentKeyID: 18127805
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747617(v=WS.10)'
---

Base de datos de servicios de directorio de RMS
===============================================

El servidor de base de datos alberga la base de datos de servicios de directorio, que contiene información sobre usuarios, identificadores (como direcciones de correo electrónico), Id. de seguridad (SID), pertenencia a grupos e identificadores alternativos. Esta información se obtiene a partir de consultas LDAP que el servicio de emisión de licencias de RMS realiza al catálogo global de Active Directory. Para obtener más información sobre este proceso y su objetivo, vea "[Caché de Active Directory de RMS](https://technet.microsoft.com/c721a2eb-2fe9-4346-b426-3cc169b97265)", más adelante en este tema.

El grupo de servicio de RMS (RMS Service Group) tiene permiso de ejecución sobre los procedimientos almacenados que se encuentran en la base de datos de servicios de directorio.

En la tabla siguiente, se enumeran los atributos de Active Directory almacenados en las tablas de la base de datos de servicios de directorio.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tabla</th>
<th>Atributo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>GroupAliases</p></td>
<td style="border:1px solid black;"><ul>
<li>GroupName: alias de un grupo<br />
<br />
</li>
<li>GroupID: Id. único de este grupo<br />
<br />
</li>
</ul></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>GroupIdentifiers</p></td>
<td style="border:1px solid black;"><ul>
<li>GroupDN: nombre distintivo de Active Directory para este grupo<br />
<br />
</li>
<li>GroupID: Id. único de este grupo<br />
<br />
</li>
<li>Expiration: fecha y hora en que caduca la información almacenada sobre este grupo<br />
<br />
</li>
</ul></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>GroupMembership</p></td>
<td style="border:1px solid black;"><ul>
<li>GroupID: Id. único de este grupo<br />
<br />
</li>
<li>ParentID: Id. único del grupo del que este grupo es un integrante<br />
<br />
</li>
</ul></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>PrincipalAliases</p></td>
<td style="border:1px solid black;"><ul>
<li>PrincipalName: alias de la entidad principal<br />
<br />
</li>
<li>PrincipalID: Id. único de esta entidad principal<br />
<br />
</li>
</ul></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>PrincipalIdentifiers</p></td>
<td style="border:1px solid black;"><ul>
<li>PrincipalID: Id. único de esta entidad principal<br />
<br />
</li>
<li>Expiration: fecha y hora en que caduca la información almacenada sobre esta entidad principal<br />
<br />
</li>
</ul></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>PrincipalMembership</p></td>
<td style="border:1px solid black;"><p>Todas las filas de esta tabla incluyen el Id. único de una entidad principal y el Id. único del grupo del que es integrante.</p>
<ul>
<li>PrincipalID: Id. único de esta entidad principal<br />
<br />
</li>
<li>ParentID: Id. único de un grupo del que esta entidad principal es un integrante.<br />
<br />
</li>
</ul></td>
</tr>
</tbody>
</table>
