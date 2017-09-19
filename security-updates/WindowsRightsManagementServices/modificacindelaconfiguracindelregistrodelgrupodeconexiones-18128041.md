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

<p> </p>
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
<th>Nombre</th>
<th>Tipo</th>
<th>Valor predeterminado</th>
<th>Descripción</th>
<th>Notas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>GC</p></td>
<td style="border:1px solid black;"><p>Cadena</p></td>
<td style="border:1px solid black;"><p>nombre-1, ..., nombre-n</p></td>
<td style="border:1px solid black;"><p>Lista separada por comas de catálogos globales (usando nombres DNS). Esta clave limita RMS a que utilice sólo los catálogos globales especificados.</p></td>
<td style="border:1px solid black;"><p>Si no desea que RMS cree una lista de consultas, utilice esta configuración para especificar los catálogos globales que se utilizarán.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MinGC</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>Número mínimo de catálogos globales que deben estar disponibles para que se pueda iniciar RMS.</p></td>
<td style="border:1px solid black;"></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MaxGC</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>15</p></td>
<td style="border:1px solid black;"><p>Número máximo de catálogos globales que el algoritmo de detección de topologías agregará a la lista de consultas.</p></td>
<td style="border:1px solid black;"></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>ThreshHoldAlive</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>Número mínimo de conexiones que deben responder antes de que DiscoveryServices empiece a buscar catálogos globales para agregarlos a la lista de consultas de forma que RMS pueda aceptar solicitudes.</p></td>
<td style="border:1px solid black;"></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>RetryDown</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>5</p></td>
<td style="border:1px solid black;"><p>Número de veces que se intentará restablecer una conexión que no responde antes de declarar que no responde.</p></td>
<td style="border:1px solid black;"></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>TimeRetryDown</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>300</p></td>
<td style="border:1px solid black;"><p>Número de segundos que se esperará antes de intentar restablecer una conexión que no responde.</p></td>
<td style="border:1px solid black;"><p>No tiene que cambiar esta configuración predeterminada, excepto en circunstancias inusuales.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>TimeRetrySlow</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>30</p></td>
<td style="border:1px solid black;"><p>Número de segundos que se esperará antes de reintentar una conexión lenta.</p></td>
<td style="border:1px solid black;"><p>No tiene que cambiar esta configuración predeterminada, excepto en circunstancias inusuales.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>WtRoundRobin</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>Peso de la operación por turnos durante el equilibrio de carga.</p></td>
<td style="border:1px solid black;"><p>Importancia relativa de la operación por turnos en el equilibrio de carga. Un valor de 1 es el valor más pequeño.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>WtThreadCount</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>100</p></td>
<td style="border:1px solid black;"><p>Peso del número de subprocesos por conexión durante el equilibrio de carga.</p></td>
<td style="border:1px solid black;"><p>Importancia relativa de un número bajo de subprocesos.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>WtSlow</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1,000</p></td>
<td style="border:1px solid black;"><p>Peso de una conexión lenta durante el equilibrio de carga.</p></td>
<td style="border:1px solid black;"><p>Importancia relativa de que la conexión no sea lenta.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>TimeOutForGC</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>5</p></td>
<td style="border:1px solid black;"><p>Número de segundos que se esperará antes de considerar que una solicitud excede el tiempo de espera para agregar un catálogo global a la lista de consultas.</p></td>
<td style="border:1px solid black;"></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>LdapTimeOut</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>5</p></td>
<td style="border:1px solid black;"><p>Número de segundos que se esperará antes de considerar que las API de LDAP exceden el tiempo de espera.</p></td>
<td style="border:1px solid black;"></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>TopDownExpansionLDAPTimeOut</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>40</p></td>
<td style="border:1px solid black;"><p>Número de segundos que se esperará antes de considerar que las consultas LDAP de expansión arriba-abajo exceden el tiempo de espera.</p></td>
<td style="border:1px solid black;"></td>
</tr>  
</tbody>  
</table>
  
| ![](images/Cc747660.Caution(WS.10).gif)Precaución                                                                                                         |  
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| La edición incorrecta del Registro puede dañar gravemente el sistema. Antes de realizar cambios en el Registro, debe realizar una copia de seguridad de los datos de valor del equipo. |
