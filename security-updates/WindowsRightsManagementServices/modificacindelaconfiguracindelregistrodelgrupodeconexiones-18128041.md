---
TOCTitle: Modificación de la configuración del registro del grupo de conexiones
Title: Modificación de la configuración del registro del grupo de conexiones
ms:assetid: 'c61d91db-a1ad-4ca5-a492-015da629afbc'
ms:contentKeyID: 18128041
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747660(v=WS.10)'
---

Modificación de la configuración del registro del grupo de conexiones
=====================================================================

Para mejorar el rendimiento del sistema, puede utilizar las entradas de clave del Registro para establecer las propiedades del conjunto de conexiones del Protocolo ligero de acceso a directorios (LDAP) que se utiliza en RMS.

En equipos con la versión de 32 bits de Windows Server 2003, la siguiente clave del registro es la ruta de subclave completa para las entradas del registro del grupo de conexiones:

**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\DRMS\\1.0**

En equipos con la versión de 64 bits de Windows Server 2003, la siguiente clave del registro es la ruta de subclave completa para las entradas del registro del grupo de conexiones:

**HKEY\_LOCAL\_MACHINE\\SoftwareWOW6432Node\\Microsoft\\DRMS\\1.0**

En la siguiente tabla, se muestran las entradas que puede agregar para omitir la configuración del conjunto de conexiones predeterminadas de Active Directory. Los valores que se muestran son los valores predeterminados. Para obtener más información sobre cómo RMS crea una lista de consultas y utiliza esta configuración, vea "Optimización de la configuración del grupo de conexiones de Active Directory", anteriormente en este tema.

###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre</th>
<th style="border:1px solid black;" >Tipo</th>
<th style="border:1px solid black;" >Valor predeterminado</th>
<th style="border:1px solid black;" >Descripción</th>
<th style="border:1px solid black;" >Notas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">GC</td>
<td style="border:1px solid black;">Cadena</td>
<td style="border:1px solid black;">nombre-1, ..., nombre-n</td>
<td style="border:1px solid black;">Lista separada por comas de catálogos globales (usando nombres DNS). Esta clave limita RMS a que utilice sólo los catálogos globales especificados.</td>
<td style="border:1px solid black;">Si no desea que RMS cree una lista de consultas, utilice esta configuración para especificar los catálogos globales que se utilizarán.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MinGC</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">1</td>
<td style="border:1px solid black;">Número mínimo de catálogos globales que deben estar disponibles para que se pueda iniciar RMS.</td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">MaxGC</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">15</td>
<td style="border:1px solid black;">Número máximo de catálogos globales que el algoritmo de detección de topologías agregará a la lista de consultas.</td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ThreshHoldAlive</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">1</td>
<td style="border:1px solid black;">Número mínimo de conexiones que deben responder antes de que DiscoveryServices empiece a buscar catálogos globales para agregarlos a la lista de consultas de forma que RMS pueda aceptar solicitudes.</td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">RetryDown</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">5</td>
<td style="border:1px solid black;">Número de veces que se intentará restablecer una conexión que no responde antes de declarar que no responde.</td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">TimeRetryDown</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">300</td>
<td style="border:1px solid black;">Número de segundos que se esperará antes de intentar restablecer una conexión que no responde.</td>
<td style="border:1px solid black;">No tiene que cambiar esta configuración predeterminada, excepto en circunstancias inusuales.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">TimeRetrySlow</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">30</td>
<td style="border:1px solid black;">Número de segundos que se esperará antes de reintentar una conexión lenta.</td>
<td style="border:1px solid black;">No tiene que cambiar esta configuración predeterminada, excepto en circunstancias inusuales.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">WtRoundRobin</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">1</td>
<td style="border:1px solid black;">Peso de la operación por turnos durante el equilibrio de carga.</td>
<td style="border:1px solid black;">Importancia relativa de la operación por turnos en el equilibrio de carga. Un valor de 1 es el valor más pequeño.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">WtThreadCount</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">100</td>
<td style="border:1px solid black;">Peso del número de subprocesos por conexión durante el equilibrio de carga.</td>
<td style="border:1px solid black;">Importancia relativa de un número bajo de subprocesos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">WtSlow</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">1,000</td>
<td style="border:1px solid black;">Peso de una conexión lenta durante el equilibrio de carga.</td>
<td style="border:1px solid black;">Importancia relativa de que la conexión no sea lenta.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">TimeOutForGC</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">5</td>
<td style="border:1px solid black;">Número de segundos que se esperará antes de considerar que una solicitud excede el tiempo de espera para agregar un catálogo global a la lista de consultas.</td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">LdapTimeOut</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">5</td>
<td style="border:1px solid black;">Número de segundos que se esperará antes de considerar que las API de LDAP exceden el tiempo de espera.</td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">TopDownExpansionLDAPTimeOut</td>
<td style="border:1px solid black;">DWORD</td>
<td style="border:1px solid black;">40</td>
<td style="border:1px solid black;">Número de segundos que se esperará antes de considerar que las consultas LDAP de expansión arriba-abajo exceden el tiempo de espera.</td>
<td style="border:1px solid black;"></td>
</tr>
</tbody>
</table>
  
| ![](images/Cc747660.Caution(WS.10).gif)Precaución                                                                                                         |  
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| La edición incorrecta del Registro puede dañar gravemente el sistema. Antes de realizar cambios en el Registro, debe realizar una copia de seguridad de los datos de valor del equipo. |
