---
TOCTitle: Seguridad durante el establecimiento de los servicios en línea
Title: Seguridad durante el establecimiento de los servicios en línea
ms:assetid: '9f1282c5-5642-4870-a9a4-c3a485f8ff76'
ms:contentKeyID: 18127893
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747616(v=WS.10)'
---

Seguridad durante el establecimiento de los servicios en línea
==============================================================

Se puede utilizar el sitio Web Administración de RMS para establecer servicios en línea de recursos de RMS en un sitio Web existente. Durante el establecimiento de servicios en línea, se crearán directorios virtuales y grupos de aplicaciones en este sitio Web. Asimismo, se crearán y configurarán bases de datos de RMS en un servidor de base de datos. Opcionalmente, si el servidor está conectado a Internet, el servidor puede inscribirse con el servicio de inscripción de Microsoft durante el procedimiento de establecimiento de servicios en línea.

Durante el establecimiento de servicios en línea, RMS utiliza las cuentas que se describen en la tabla siguiente.

###  

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Cuenta</th>
<th style="border:1px solid black;" >Finalidad</th>
<th style="border:1px solid black;" >Permisos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Cuenta del usuario que inició sesión</td>
<td style="border:1px solid black;">Crear directorios virtuales y grupos de aplicaciones. IIS requiere autenticación de Windows, y RMS suplanta al usuario que inició sesión, que debe haber iniciado la sesión localmente.</td>
<td style="border:1px solid black;">Control total (el usuario que inició sesión debe ser un administrador local).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cuenta del sistema</td>
<td style="border:1px solid black;">Crear el ensamblado temporal para la serialización.</td>
<td style="border:1px solid black;">Permisos de lectura y escritura para la carpeta temporal de Windows, C:\Windows\Temp.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Cuenta ASPNET</td>
<td style="border:1px solid black;">Crear el ensamblado temporal de los archivos *.aspx.</td>
<td style="border:1px solid black;">Acceso al directorio de la caché de ensamblados temporal, C:\Windows\Microsoft.NET\Framework\v1.1.4322\Temporary ASP.NET Files, de forma predeterminada.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cuenta de los servicios de red</td>
<td style="border:1px solid black;">Registrar el punto de conexión de los servicios en Active Directory.</td>
<td style="border:1px solid black;"><ul>
<li>Permisos de sólo lectura en el sitio de establecimiento de servicios en línea (suele ser C:\Inetpub\Wwwroot\Provisioning).<br />
<br />
</li>
<li>Permisos de lectura y escritura para la clave del Registro <strong>DRMS</strong>. Los permisos los otorga el programa de instalación de RMS, que también crea la siguiente clave del Registro.<br />
<br />
En equipos con la versión de 32 bits de Windows Server 2003:<br />
<br />
<code>HKEY_LOCAL_MACHINE\Software\Microsoft\DRMS\1.0</code><br />
<br />
En equipos con la versión de 64 bits de Windows Server 2003:<br />
<br />
<code>HKEY_LOCAL_MACHINE\Software\WOW6432Node\Microsoft\DRMS\1.0</code><br />
<br />
</li>
</ul></td>
</tr>
</tbody>
</table>
 

Durante el establecimiento de servicios en línea, RMS realiza las siguientes tareas:

-   En el servidor de base de datos:
    -   Crea las bases de datos de configuración, servicios de directorio y de registro.
    -   Otorga permiso de inicio de sesión al grupo de servicio de RMS (RMS Service Group).
    -   Instala procedimientos almacenados en las bases de datos y otorga permiso de ejecución al grupo de servicio de RMS.
    -   Ejecuta consultas en la base de datos principal.
-   Agrega el grupo de servicio de RMS al grupo IIS\_WPG.
-   En C:\\Inetpub\\Wwwroot\\\_wmcs, crea una jerarquía de directorios virtuales, archivos y grupos de aplicaciones para los servicios Web y para el sitio Web Administración de RMS.
-   Establece las listas DACL en los directorios virtuales, archivos y grupos de aplicaciones.
-   Permite al grupo de servicio de RMS el acceso a la carpeta temporal.
-   Cuando se especifica protección de clave de software, cifra la clave privada del emisor de licencias de servidor antes de almacenarla en la base de datos. RMS solicita una contraseña durante el establecimiento de servicios en línea, y obtiene acceso a DPAPI a nivel de equipo.
-   Instala el servicio de escucha de registro.
-   Crea la cola de mensajes de registro.
-   Si se están estableciendo los servicios en línea en el servidor de certificación raíz, establece el punto de conexión de servicio en Active Directory.
