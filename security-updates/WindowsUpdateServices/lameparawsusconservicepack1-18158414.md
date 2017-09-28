---
TOCTitle: Léame para WSUS con Service Pack 1
Title: Léame para WSUS con Service Pack 1
ms:assetid: '937ecfe9-e8e0-41ac-85f7-4b65956f3d1e'
ms:contentKeyID: 18158414
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708486(v=WS.10)'
---

Léame para WSUS con Service Pack 1
==================================

Este documento describe problemas conocidos que afectan a Windows Server Update Services con Service Pack 1 (WSUS con SP1). Inmediatamente después de la información de WSUS con SP1, encontrará toda la información incluida anteriormente en las notas originales de Léame de WSUS. Esta información incluye recomendaciones y requisitos para instalar WSUS. Para descargar WSUS con SP1, consulte el [Centro de descarga Microsoft](http://go.microsoft.com/fwlink/?linkid=67516).

Novedades en WSUS con SP1
-------------------------

WSUS con SP1 es una versión de service pack que mejora la seguridad, confiabilidad, escalabilidad, compatibilidad y rendimiento de WSUS. Éstas son las nuevas características y mejoras:

-   compatibilidad con clientes con Windows Vista: Los equipos que ejecutan Windows Vista se pueden actualizar con el servidor WSUS con SP1.
-   Compatibilidad con más idiomas de clientes: compatibilidad para todos los idiomas de Office y Windows Vista.
-   Nueva versión de WMSDE: la instancia de WMSDE se actualizará a WMSDE SP4 mediante WSUS con SP1 (WSUS RTM usa WMSDE SP3).
-   Mejoras de rendimiento: WSUS con SP1 incluye distintas mejoras de rendimiento para acelerar los tiempos de respuesta de la interfaz de usuario.
-   Todas las revisiones: WSUS con SP1 incluye todos los cambios y revisiones que se han editado desde WSUS RTM.
-   Compatibilidad con SQL Server 2005.

Antes de comenzar la actualización de WSUS con SP1
--------------------------------------------------

Los siguientes problemas son específicos de la actualización de WSUS con SP1. Tenga en cuenta que los problemas y requisitos descritos en la sección “Antes de comenzar” de la versión original de este tema no se tratan en esta sección y siguen siendo válidos. Por ejemplo, los requisitos para la instalación descritos en dicha sección original siguen siendo válidos.

**Nota**   Después de aplicar SP1 a WSUS 2.0, el service pack no se puede desinstalar. Al desinstalar SP1, se desinstalará todo el producto.

**Importante**   Este documento contiene información acerca de la modificación del Registro. Asegúrese de realizar una copia de seguridad del mismo antes de modificarlo. Asegúrese de que sabe cómo restaurar el Registro si se produce un problema. Para obtener más información acerca de la copia de seguridad, restauración y modificación del Registro, consulte el siguiente artículo en Microsoft Knowledge Base:

[Definición del Registro de Microsoft Windows](http://support.microsoft.com/kb/256986) (http://support.microsoft.com/kb/256986/)

#### Problema 1: asegúrese de que tiene suficiente espacio en disco para la copia de seguridad de la base de datos

Al actualizar desde WSUS RTM, el programa de instalación de WSUS con SP1 automáticamente crea una copia de seguridad de la base de datos de WSUS. Debe asegurarse de que hay suficiente espacio en disco en el sistema de archivos del servidor WSUS para almacenar la copia de seguridad de la base de datos de WSUS, de lo contrario no se podrá realizar la instalación de WSUS con SP1.

**Para determinar si hay suficiente espacio en disco**
1.  Abra el Explorador de Windows y navegue a la carpeta en la que está almacenada la base de datos de WSUS. De forma predeterminada, WSUS instala la base de datos aquí:

    
        ```
2.  Mantenga pulsada la tecla **CTRL**, seleccione **SUSDB.MDF** y **SUSDB\_log.LDF** y, a continuación, haga clic con el botón secundario y seleccione **Propiedades**.

3.  En el cuadro de diálogo **Archivos**, lea el valor de **Tamaño en disco**. El disco debe tener al menos este espacio en disco libre para instalar WSUS con SP1.

4.  En el menú **Inicio**, haga clic en **Mi PC**. Asegúrese de que el disco en el que está instalado WSUS tiene la cantidad de espacio libre en disco necesaria.

Si por algún motivo no se puede instalar WSUS con SP1, restaure manualmente la copia de seguridad de la base de datos. Para obtener instrucciones para la restauración de la base de datos de WSUS, consulte la [Guía de operaciones de WSUS](http://technet2.microsoft.com/windowsserver/en/library/05f2e884-ae62-4c90-9681-6c9f2f3c9fd91033.mspx).

#### Problema 2: WSUS con SP1 sólo actualizar WSUS RTM

Sólo puede usar WSUS con SP1 para actualizar WSUS RTM. En este momento, no es compatible la actualización desde el candidato para versión comercial de WSUS. Si tiene instalado el candidato para versión comercial de WSUS o cualquier versión de compilación anterior de WSUS, debe desinstalar dichas versiones de compilación y, a continuación, ejecutar WSUS con SP1.

#### Problema 3: el servicio IIS del servidor se detendrá durante la actualización de WSUS con SP1

El instalador de la actualización de WSUS con SP1 detiene el servicio de Internet Information Services (IIS) en el servidor durante el proceso de actualización. Esto significa que todos los sitios Web alojados en la instalación de IIS del servidor no estarán disponibles durante la actualización. IIS se iniciará automáticamente al final de la actualización.

#### Problema 4: durante la actualización, no debe ejecutar aplicaciones que llamen a las API de WSUS

Las llamadas a las interfaces de programación de aplicaciones (API) de WSUS entrarán en conflicto con el instalador de WSUS con SP1, con lo que no se podrá realizar la actualización (recibirá un mensaje en el que se le pedirá que reinicie el servidor para completar la actualización).

#### Problema 5: al actualizar a WSUS con SP1, es posible que tenga que deshabilitar los programas antivirus

Cuando actualiza WSUS aplicando WSUS con SP1, es posible que tenga que deshabilitar los programas antivirus para poder realizar correctamente la actualización o aplicar el service pack. Después de deshabilitar los programas antivirus, reinicie el equipo con Windows Server antes de aplicar la actualización o service pack. Este procedimiento impide que se bloqueen los archivos a los que el proceso de actualización necesita obtener acceso. Una vez completada la instalación, asegúrese de volver a habilitar los programas antivirus. Visite el sitio Web del proveedor de los programas antivirus para conocer los pasos exactos para deshabilitar y volver a habilitar el programa antivirus y la versión.

| ![](images/Cc708486.Caution(WS.10).gif)Precaución                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Esta solución para el problema puede hacer que el equipo o la red sea más vulnerable a ataques por parte de usuarios o software malintencionados como virus. No se recomienda esta solución, pero se proporciona esta información para que pueda implementarla según su propio criterio. Use esta solución bajo su propia responsabilidad. |

| ![](images/Cc708486.note(WS.10).gif)Nota                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Los programas antivirus están diseñados para proteger el equipo frente a virus. No debe descargar ni abrir archivos de orígenes en los que no confíe, visitar sitios Web en los que no confíe, ni abrir archivos adjuntos de correo electrónico cuando el programa antivirus esté deshabilitado. |

#### Problema 6: si usa un servidor proxy, la actualización de SP1 puede borrar el nombre de usuario y contraseña de configuración de proxy

Si usa un servidor proxy, en algunos casos la actualización de SP1 puede borrar el nombre de usuario y contraseña de configuración de proxy. Esto puede causar que la sincronización de las actualizaciones de los servidores de Microsoft genere un error de “parámetro no válido”. Para resolver este problema, restablezca el nombre de usuario y contraseña de configuración de proxy y vuelva a sincronizar el servidor.

#### Problema 7: cómo recuperarse de un error de actualización para restaurar el servidor WSUS a un estado coherente y, a continuación, vuelva a intentar la actualización.

Si no se puede realizar la actualización a WSUS con SP1, puede dejar la instalación de WSUS con un estado incoherente o quedar inservible. Para volver a intentar la actualización a WSUS con SP1, tendrá que restaurar la instalación de WSUS a un estado coherente. Para ello, puede usar la copia de seguridad de la base de datos creada al principio del proceso de actualización para restaurar el servidor WSUS a un estado previo a la actualización.

En caso de un error de actualización, siga estos pasos para volver a intentar la actualización a WSUS con SP1:

**Para volver a intentar la actualización a WSUS con SP1**
1.  Determine la ubicación de la copia de seguridad de la base de datos revisando el contenido del archivo WSUSSetup\_%timestamp%.log. Este archivo se encuentra en la siguiente carpeta:

    -   %programfiles%\\Update Services\\LogFiles

2.  Restaure la copia de seguridad de la base de datos en el equipo con WSUS con lo siguiente:

    -   osql.exe -S &lt;DatabaseInstance&gt; -E -Q "USE master ALTER DATABASE SUSDB SET SINGLE\_USER WITH ROLLBACK IMMEDIATE RESTORE DATABASE SUSDB FROM DISK=N'&lt;PathToDatabaseBackup&gt;' WITH REPLACE ALTER DATABASE SUSDB SET MULTI\_USER"
    -   Recuerde reemplazar &lt;DatabaseInstance&gt; y &lt;PathToDatabaseBackup&gt; por los valores de la instalación.
    -   Para &lt;DatabaseInstance&gt; use el valor de la siguiente clave del Registro:
    -   HKLM\\Software\\Microsoft\\Update Services\\Server\\Setup\\SqlServerName
    -   Para &lt;PathToDatabaseBackup&gt; use el valor identificado en el paso 1.

3.  Desinstale WSUS, pero mantenga la base de datos de WSUS, los archivos de registro y los archivos de actualización cuando se le pregunte si desea eliminarlos. (Asegúrese de que están desactivadas todas las opciones de **Quitar Microsoft Windows Server Update Services**.)

4.  Vuelva a instalar WSUS RTM (la versión original, no WSUS con SP1). Use la base de datos existente cuando se le solicite. De esta forma, el sistema de WSUS volverá a un estado coherente.

5.  Instale WSUS con SP1.

**Nota**    No puede usar la copia de seguridad de la base de datos del paso 1 anterior directamente en una instalación limpia de WSUS con SP1. El esquema de la base de datos ha cambiado por lo que esta base de datos no será compatible sin la actualización a WSUS con SP1.

#### Problema 8: la actualización de WSUS con SP1 puede fallar en algunos casos cuando la base de datos de WMSDE se ha migrado

La solución varía en función de si migró a un servidor SQL Server local o remoto.

#### Base de datos de WMSDE migrada a un servidor SQL Server 2000 local

Se debe cambiar un valor de clave del Registro para que el paquete de instalación de WSUS con SP1 reconozca que no hay ninguna base de datos de WMSDE que actualizar.

Si migró WMSDE a un servidor SQL Server 2000 local, debe realizar el siguiente cambio en el Registro antes de intentar actualizar a WSUS con SP1:

-   Cambie el valor de la siguiente clave del Registro de "1" a "0":
    -   HKLM\\Software\\Microsoft\\Update Services\\Server\\Setup\\WmsdeInstalled  

#### Base de datos de WMSDE migrada a un servidor SQL Server 2000 remoto

Se deben cambiar dos valores de clave del Registro para que el paquete de instalación de WSUS con SP1 reconozca que no hay ninguna base de datos de WMSDE que actualizar. La actualización se debe iniciar en el servidor back-end y, a continuación, en el servidor front-end.  

Si migró WMSDE a un servidor SQL Server remoto, debe realizar los siguientes cambios en el Registro antes de intentar actualizar a WSUS con SP1:

1.  Cambie el valor de la siguiente clave del Registro de "1" a "0":
    -   HKLM\\Software\\Microsoft\\Update Services\\Server\\Setup\\WmsdeInstalled 
2.  Cambie el valor de la siguiente clave del Registro de "0x80" a "0x20":
    -   HKLM\\Software\\Microsoft\\Update Services\\Server\\Setup\\InstallType 

Después de actualizar estos valores de clave del Registro, inicie la actualización en los servidores back-end y, a continuación, en los servidores front-end.

#### Problema 9: WSUS con SP1 no actualiza los servidores WSUS configurados mediante implementaciones de SQL remoto

Debe ejecutar el paquete de instalación de WSUS con SP1 en los servidores front-end y back-end.

**Para actualizar a WSUS con SP1 cuando se usa SQL remoto**
1.  Ejecute el paquete de instalación en el servidor front-end sin modificadores y seleccione la actualización.

2.  Ejecute el paquete de instalación en el servidor back-end sin modificadores y seleccione la actualización.

#### Problema 10: el cambio del nombre del equipo antes de actualizar a WSUS con SP1 puede producir un error en la actualización

Si cambia el nombre del equipo después de instalar WSUS RTM y antes de actualizar a WSUS con SP1, es posible que no se actualice a WSUS con SP1.

Use el siguiente script para eliminar y volver a agregar los grupos Administradores de WSUS y ASPNET. A continuación, vuelva a realizar la actualización.

        ```
| ![](images/Cc708486.note(WS.10).gif)Nota                                                          |
|--------------------------------------------------------------------------------------------------------------------------------|
| Es posible que tenga que reemplazar &lt;ContentDirectory&gt; en la última línea por la ruta de acceso al almacén de contenido. |

A continuación se muestra el contenido origina de Léame de WSUS
---------------------------------------------------------------

Éste es el contenido original de Léame de WSUS. WSUS con SP1 *no* trata ninguno de los siguientes problemas. Este contenido se incluye aquí por comodidad.

Antes de comenzar
-----------------

#### Problema 1: es necesario instalar IIS

Microsoft® Windows Server™ Update Services (WSUS) requiere que esté instalado Servicios de Internet Information Server (IIS). Sin embargo, en Microsoft Windows Server 2003 y Microsoft Windows® 2000 Server, IIS no se instala de manera predeterminada, por lo que es posible que el programa de instalación de Windows Server Update Services se detenga y muestre un mensaje de error que indique que IIS no está instalado.

Para instalar IIS:

1.  Abra el Panel de control.
2.  Haga doble clic en **Agregar o quitar programas**.
3.  Haga clic en **Agregar o quitar componentes de Windows**.
4.  En la lista **Componentes**, haga clic en **Servidor de aplicaciones**.
5.  Haga clic en **Detalles**.
6.  Active la casilla de verificación **ASP.NET**. Habilite el **acceso de red COM+** y se seleccionarán automáticamente los servicios de Internet Information Server (IIS).
7.  Seleccione **Servicios de Internet Information Server (IIS)** y, a continuación, haga clic en **Detalles** para ver la lista de componentes opcionales de IIS.
8.  Seleccione todos los componentes opcionales que desee instalar. El componente opcional Servicio World Wide Web incluye subcomponentes importantes como, por ejemplo, Páginas Active Server y Administración remota (HTML). Para ver y seleccionar estos subcomponentes, haga clic en Servicio World Wide Web y, a continuación, en Detalles. Haga clic en Aceptar hasta que vuelva al Asistente para componentes de Windows.
9.  Haga clic en **Siguiente** y complete el Asistente para componentes de Windows.
10. Después de instalar IIS, ejecute el programa de instalación de Windows Server Update Services.

#### Problema 2: para los servidores que ejecutan Windows 2000 Server, es necesario que haya al menos un sitio Web en IIS antes de instalar WSUS

Es posible que el programa de instalación de Windows Server Update Services no pueda crear un sitio Web si no había ninguno en IIS al ejecutar el programa de instalación. Esto puede suceder, por ejemplo, si tiene un sitio Servicios de actualización de software (SUS) 1.0 como único sitio en IIS y lo elimina antes de instalar WSUS.

En este caso, tiene que crear un nuevo sitio Web mediante el complemento Administrador de Servicios de Internet Information Server (IIS). A continuación, puede seleccionar este sitio o especificar uno nuevo durante la instalación de WSUS.

Si ya intentó instalar WSUS y se produjo un error del programa de instalación porque no hay ningún sitio presente, abra el complemento Administrador IIS y elimine el sitio "Sitio Web \#1". A continuación, siga los pasos descritos anteriormente y vuelva a ejecutar el programa de instalación.

#### Problema 3: instalación de componentes necesarios

#### Requisitos de software

La siguiente tabla muestra el software necesario para cada sistema operativo compatible. Asegúrese de que el servidor WSUS cumple la lista de requisitos antes de ejecutar el programa de instalación de WSUS. Si alguna de estas actualizaciones requiere el reinicio del equipo una vez terminada la instalación, debe reiniciar antes de instalar WSUS.

###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Sistema operativo</th>
<th>Requisitos</th>
<th>Descargas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Todos los sistemas operativos</td>
<td style="border:1px solid black;">Servicios de Microsoft Internet Information Server (IIS) 5.0</td>
<td style="border:1px solid black;">Instale desde el sistema operativo.
Consulte Problema 1: es necesario instalar IIS.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Todos los sistemas operativos</td>
<td style="border:1px solid black;">Servicio de transferencia inteligente en segundo plano (BITS) 2.0</td>
<td style="border:1px solid black;">Para los sistemas operativos Windows Server 2003, consulte Actualización para el Servicio de transferencia inteligente en segundo plano (BITS) 2.0 y WinHTTP 5.1 de Windows Server 2003 (KB842773) en el Centro de descarga (<a href="http://go.microsoft.com/fwlink/?linkid=47251">http://go.microsoft.com/fwlink/?LinkId=47251</a>).
Para los sistemas operativos Windows Server 2000, consulte Actualización para el Servicio de transferencia inteligente en segundo plano (BITS) 2.0 y WinHTTP 5.1 de Windows 2000 (KB842773) en el Centro de descarga (<a href="http://go.microsoft.com/fwlink/?linkid=46794">http://go.microsoft.com/fwlink/?LinkId=46794</a>).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Server 2003</td>
<td style="border:1px solid black;">Microsoft .NET Framework 1.1 Service Pack 1 para Windows Server 2003</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=47358">Microsoft .NET Framework 1.1 Service Pack 1 para Windows Server 2003</a>
Como alternativa, vaya a <a href="http://go.microsoft.com/fwlink/?linkid=47370">Windows Update</a> y busque actualizaciones críticas y Service Packs; instale Microsoft .NET Framework 1.1 Service Pack 1 para Windows Server 2003.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows Server 2003</td>
<td style="border:1px solid black;">Software de base de datos totalmente compatible con Microsoft SQL Server</td>
<td style="border:1px solid black;">No disponible</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows 2000 Server</td>
<td style="border:1px solid black;">Software de base de datos totalmente compatible con Microsoft SQL Server</td>
<td style="border:1px solid black;">Si no usa Microsoft SQL Server 2000, puede instalar Microsoft SQL Server 2000 Desktop Engine (MSDE 2000). Para ello, se requieren varios pasos. Para obtener más información, consulte Instalación de MSDE 2000 en Windows 2000 a continuación.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows 2000 Server</td>
<td style="border:1px solid black;">Microsoft Internet Explorer 6.0 Service Pack 1</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=47359">Internet Explorer 6 Service Pack 1</a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows 2000 Server</td>
<td style="border:1px solid black;">Paquete redistribuible de Microsoft .NET Framework versión 1.1</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=47369">Paquete redistribuible de Microsoft .NET Framework versión 1.1</a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows 2000 Server</td>
<td style="border:1px solid black;">Microsoft .NET Framework 1.1 Service Pack 1</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=47368">Microsoft .NET Framework 1.1 Service Pack 1</a>
Como alternativa, vaya a <a href="http://go.microsoft.com/fwlink/?linkid=47370">Windows Update</a> y busque actualizaciones críticas y Service Packs; instale Microsoft .NET Framework 1.1 Service Pack 1 para Windows Server 2000.</td>
</tr>
</tbody>
</table>
 

Además de estos requisitos, WSUS puede instalar o configurar ASP.NET versión 1.1 en el servidor, si es necesario. (El programa de instalación de WSUS configura ASP.NET.)

#### Instalación de MSDE 2000 en Windows 2000

Si usa Windows 2000 para WSUS y no tiene acceso a Microsoft SQL Server 2000, debe instalar Microsoft SQL Server 2000 Desktop Engine (MSDE) antes de ejecutar el programa de instalación de WSUS. Si ya tiene instalado MSDE en el servidor WSUS, no tiene que instalar una versión especial del mismo para WSUS. Puede simplemente indicar el nombre de la instancia existente durante el proceso de instalación de WSUS.

La instalación de MSDE en Windows 2000 Server es un proceso de cuatro pasos. Primero, debe descargar y expandir el archivo de MSDE en una carpeta del servidor WSUS. Después, use un símbolo del sistema y opciones de la línea de comandos para ejecutar el programa de instalación de MSDE, definir la contraseña del administrador del sistema y asignar WSUS como nombre de instancia. A continuación, una vez terminada la instalación de MSDE, debe comprobar que la instancia de WSUS se ejecuta como servicio de NT. Finalmente, debe agregar una revisión de seguridad a MSDE para proteger el servidor WSUS.

#### Paso 1: descargar y expandir el archivo de MSDE

Debe descargar y expandir el archivo de MSDE en una carpeta del servidor WSUS. Consulte [Microsoft SQL Server 2000 Desktop Engine (MSDE 2000) Release A](http://go.microsoft.com/fwlink/?linkid=47366).

#### Paso 2: instalar MSDE

Use un símbolo del sistema y opciones de la línea de comandos para ejecutar el programa de instalación de MSDE, definir la contraseña del administrador del sistema y asignar WSUS como nombre de instancia. Una vez terminada la instalación de MSDE, debe comprobar que la instancia de WSUS se ejecuta como servicio de NT.

Para instalar MSDE, defina la contraseña del administrador del sistema y asigne un nombre de instancia:

1.  En el símbolo del sistema, navegue a la carpeta de instalación de MSDE especificada en “Paso 1: Descargar y expandir el archivo de MSDE”.
2.  Escriba lo siguiente: **setup sapwd="***contraseña***" instancename=WSUS**
    donde *contraseña* es una contraseña segura para la cuenta del administrador del sistema de esta instancia de MSDE e **instancename** es el nombre de la instancia de base de datos. Como alternativa, puede usar el nombre de instancia predeterminado (en lugar de "WSUS") para la base de datos de WSUS. Si decide hacer esto, no tiene que escribir **instancename=WSUS** en el parámetro de la línea de comandos. Este comando inicia el programa de instalación de MSDE, define la contraseña del administrador del sistema y asigna el valor especificado como nombre para esta instancia de MSDE.

#### Paso 3: comprobar que la instancia de WSUS de MSDE está instalada

1.  Haga clic en **Inicio** y, a continuación, en **Ejecutar**.
2.  En el cuadro **Abrir**, escriba **services.msc** y, a continuación, haga clic en **Aceptar**.

Desplácese por la lista de servicios y compruebe que existe un servicio con el nombre MSSQL$WSUS (si usó "WSUS" para instancename) o MSSQLSERVER (si usó el valor predeterminado para instancename).

#### Paso 4: iniciar la instancia de MSDE

Al final de la instalación de MSDE, tiene que iniciar la instancia. Si usó "WSUS" para instancename, debe iniciar "MSSQL$WSUS". Si usó el valor predeterminado para instancename, debe iniciar MSSQLSERVER. Si no inicia este servicio, WSUS no podrá usar la instancia de base de datos.

#### Paso 5: actualizar MSDE

Debe descargar e instalar la revisión de seguridad descrita en el boletín [MS03-031: Revisión de seguridad acumulativa para SQL Server](http://go.microsoft.com/fwlink/?linkid=47364).

Para descargar la revisión de seguridad, consulte [Revisión de seguridad de SQL Server 2000 (32 bits) MS03-031](http://go.microsoft.com/fwlink/?linkid=47363).

#### Problema 4: requisitos mínimos de espacio en disco

A continuación se indican los requisitos mínimos de espacio en disco para instalar Windows Server Update Services:

-   1 gigabyte (GB) en la partición del sistema
-   2 GB para el volumen en el que se almacenarán los archivos de base de datos
-   6 GB, según los números de proyección de contenido

#### Problema 5: se deben desinstalar versiones anteriores de WSUS mediante Agregar o quitar programas antes de instalar la última versión

Si ha pensado instalar Windows Server Update Services en un servidor que tiene instalado Windows Update Services Beta 1 o Beta 2, primero tiene que desinstalar la versión anterior mediante Agregar o quitar programas del Panel de control.

#### Problema 6: WSUS requiere que se active la opción de desencadenadores anidados en SQL Server

Esta opción está activada de forma predeterminada; sin embargo, la puede desactivar un administrador de SQL Server.

Si ha pensado usar una base de datos de SQL Server como almacén de datos de Windows Server Update Services, el administrador de SQL Server debe verificar que la opción de desencadenadores anidados del servidor está activada antes de que el administrador de WSUS instale WSUS y especifique la base de datos durante la instalación.

El programa de instalación de WSUS activa la opción RECURSIVE\_TRIGGERS, que es una opción específica de base de datos; no obstante, no activa la opción de desencadenadores anidados, que es una opción global del servidor.

Para ver si los desencadenadores anidados están activados, use lo siguiente:

**sp\_configure 'nested triggers'**

Para activar la opción de desencadenadores anidados en SQL Server, ejecute lo siguiente en un archivo por lotes en el equipo que ejecuta SQL Server:

**sp\_configure 'nested triggers', 1**

**GO**

**RECONFIGURE**

**GO**

#### Problema 7: parámetros de la línea de comandos del programa de instalación de WSUS

Puede realizar instalaciones desatendidas de WSUS. Para obtener más información y los parámetros de la línea de comandos, consulte "Apéndice A: instalación desatendida" en [Guía paso a paso para empezar a trabajar con Microsoft Windows Server Update Services](http://go.microsoft.com/fwlink/?linkid=41777).

Problemas conocidos
-------------------

#### Problema 1: asistente para Lockdown de IIS

Si ejecuta los servicios de Internet Information Server (IIS) en un equipo con Windows 2000 Server, instale la última versión del asistente para Lockdown de IIS (que incluye URLScan) desde la página Herramienta Lockdown de IIS en Microsoft TechNet. Microsoft recomienda instalar esta herramienta para proteger los servidores IIS. El asistente para Lockdown de IIS funciona desactivando características innecesarias de IIS, reduciendo así la exposición a riesgos de seguridad.

| ![](images/Cc708486.note(WS.10).gif)Nota                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El programa de instalación de WSUS no instala estos componentes. Debe instalarlos manualmente. No es necesario que instale Lockdown de IIS en los equipos que ejecuten Windows Server 2003, porque la funcionalidad está integrada. |

#### Problema 2: no se admite el cambio de configuración de WSUS directamente en la base de datos

Windows Server Update Services almacena sus datos de configuración en una base de datos (MSDE o SQL Server). Sin embargo, no se admite el cambio de los datos de configuración mediante el acceso directo a la base de datos. Los administradores no deben intentar modificar la configuración de WSUS de esta forma. La forma admitida para cambiar la configuración de WSUS es mediante la consola de WSUS o llamando a las API de WSUS.

#### Problema 3: Active scripting debe estar activado para tener acceso al sitio de administración de WSUS

En la estación de trabajo del administrador, debe configurar Internet Explorer para permitir Active scripting con el fin de poder utilizar Internet Explorer para tener acceso al sitio de administración de WSUS.

#### Problema 4: IIS se reiniciarán durante la instalación de WSUS

El programa de instalación de Windows Server Update Services reiniciará IIS sin previo aviso. Esto puede afectar a los sitios Web existentes de la organización.

#### Problema 5: cambio del acceso de directorio virtual de los puntos de administración (MP) de WSUS o SMS

De forma predeterminada, el directorio virtual de contenido para Windows Server Update Services está definido con acceso anónimo. Si cambia esta configuración para requerir autenticación, los clientes recibirán errores de autenticación y se les denegará el acceso para descargar actualizaciones. Se trata de un problema conocido en el que Winhttp.dll usa el contexto de autenticación incorrecto cuando se requiere la autenticación implícita, por lo que no se podrá realizar el desafío de autenticación. Para evitar este problema, asegúrese de que el servidor WSUS y los MP de SMS están configurados con acceso anónimo a directorios virtuales de IIS.

#### Problema 6: al instalar WSUS en Windows Small Business Server 2003, se debe modificar la configuración de acceso de vroots de WSUS del sitio Web predeterminado para permitir a los clientes WSUS actualizarse automáticamente desde el servidor

El servidor WSUS instala dos vroots, SelfUpdate y ClientWebService, así como algunos archivos en el directorio principal del sitio Web predeterminado (en el puerto 80). De esta forma, los clientes pueden actualizarse automáticamente a través del sitio Web predeterminado. De forma predeterminada, en Windows Small Business Server 2003, el sitio Web predeterminado se configura para denegar el acceso a cualquier IP o host local que no sean los del servidor. Esto significa que se deniega el acceso a las vroots SelfUpdate y ClientWebService y que los clientes no actualizarán automáticamente. Para conceder acceso a los clientes para que se actualicen automáticamente, realice los siguientes pasos en las vroots SelfUpdate y ClientWebService del sitio Web predeterminado.

1.  Haga clic en **Propiedades** de las vroots, haga clic en **Seguridad de directorios**, en **Restricciones de nombre de dominio y dirección IP** y, a continuación, en **Editar**.
2.  Seleccione **Concederá el acceso** y haga clic en **Aceptar**. Cierre todas las páginas de propiedades.

#### Problema 7: instalación de WSUS en Small Business Server: problemas de integración

-   Si Windows Small Business Server 2003 usa un servidor proxy ISA para obtener acceso a Internet, se debe introducir manualmente lo siguiente en la interfaz de usuario de **configuración**: configuración del servidor proxy, nombre del servidor proxy y puerto.
-   Si ISA utiliza Autenticación de Windows, se deben introducir las credenciales del servidor proxy con el formato "DOMINIO\\usuario" (el usuario que pertenece al grupo "Usuarios de Internet").

#### Problema 8: al mover un equipo de un grupo de equipos a otro, el equipo puede tardar hasta una hora en aparece en el nuevo grupo cuando se visualiza en la consola de administración

Cuando se asigna un equipo a un grupo de destino por primera vez, los datos del equipo se modifican con la información del grupo. Dichos datos se actualizan periódicamente o cada hora. Por lo tanto, al mover un equipo de un grupo de equipos a otro, dicha información puede tardar hasta una hora en actualizarse en el cliente y mostrarse cambiada en la consola de administración de WSUS.

#### Problema 9: si instala WSUS en un servidor miembro y, a continuación, desea promocionar dicho servidor a un controlador de dominio, primero debe desinstalar WSUS

Si instala WSUS en un servidor miembro y, a continuación, desea promocionar dicho servidor a un controlador de dominio, tendrá que realizar los siguientes pasos:

1.  Desinstale WSUS.
2.  Promocione el servidor a un controlador de dominio.
3.  Vuelva a instalar WSUS.

#### Problema 10: si desea degradar un servidor WSUS de un controlador de dominio, primero debe desinstalar WSUS

Si ejecuta un servidor WSUS en un controlador de dominio y desea degradar dicho controlador a un servidor miembro, tendrá que realizar los siguientes pasos:

1.  Desinstale WSUS y mantenga la base de datos.
2.  Cree una cuenta de usuario denominada ASPNET.
3.  En el símbolo del sistema, escriba **aspnet\_regiis -i**.
4.  Vuelva a instalar WSUS y use la base de datos mantenida.

#### Problema 11: si se instala .NET Framework 1.0 o 2.0 después de instalar WSUS, no aparecerá la consola de administración de WSUS

Esto se debe al hecho de que .NET Framework 1.0 se registra con IIS y que el servidor WSUS necesita .NET Framework 1.1. Para resolver este problema, abra aspnet\_regiis.exe y ejecute los siguientes comandos, donde *Id. de sitio Web* es el valor incluido en la siguiente clave del Registro:

HKLM\\Software\\Microsoft\\WindowsUpdateServices\\Server\\Setup\\IISTargetWebsiteIndex

-   %windir%\\Microsoft.NET\\Framework\\v1.1.4322\\\\aspnet\_regiis.exe -s W3SVC\\&lt;*Id. de sitio Web*&gt;\\ROOT\\ReportingWebService
-   %windir%\\Microsoft.NET\\Framework\\v1.1.4322\\\\aspnet\_regiis.exe -s W3SVC\\&lt;*Id. de sitio Web*&gt;\\ROOT\\ClientWebService
-   %windir%\\Microsoft.NET\\Framework\\v1.1.4322\\\\aspnet\_regiis.exe -s W3SVC\\&lt;*Id. de sitio Web*&gt;\\ROOT\\SimpleAuthWebService
-   %windir%\\Microsoft.NET\\Framework\\v1.1.4322\\\\aspnet\_regiis.exe -s W3SVC\\&lt;*Id. de sitio Web*&gt;\\ROOT\\WSUSAdmin
-   %windir%\\Microsoft.NET\\Framework\\v1.1.4322\\\\aspnet\_regiis.exe -s W3SVC\\&lt;*Id. de sitio Web*&gt;\\ROOT\\AdministrationWebService
-   %windir%\\Microsoft.NET\\Framework\\v1.1.4322\\\\aspnet\_regiis.exe -s W3SVC\\&lt;*Id. de sitio Web*&gt;\\ROOT\\ServrSyncWebService
-   %windir%\\Microsoft.NET\\Framework\\v1.1.4322\\\\aspnet\_regiis.exe -s W3SVC\\&lt;*Id. de sitio Web*&gt;\\ROOT\\DssAuthWebService
-   %windir%\\Microsoft.NET\\Framework\\v1.1.4322\\\\aspnet\_regiis.exe -s W3SVC\\&lt;*Id. de sitio Web*&gt;\\ROOT\\Content

#### Problema 12: limitaciones de SQL remoto

WSUS ofrece soporte limitado para ejecutar el software de base de datos en un equipo independiente del equipo con el resto de la aplicación WSUS.

-   No puede usar Windows 2000 Server como equipo cliente en un par de SQL remoto.
-   Puede usar un servidor configurado como controlador de dominio para el cliente o el servidor del par de SQL remoto.
-   No puede usar WMSDE ni MSDE para el software de base de datos en el equipo servidor.
-   No se puede configurar un servidor SQL Server remoto (para utilizarlo como base de datos de WSUS) si se ha instalado Servicios de Terminal Server en el servidor remoto y se ejecutan en modo de aplicación. Al instalar SQL Server en un servidor de Servicios de Terminal Server, debe llevar a cabo lo siguiente:
    1.  Antes de ejecutar el programa de instalación, abra un símbolo del sistema y escriba: "change user /install"
    2.  Ejecute el programa de instalación de SQL Server.
    3.  Una vez ejecutado el programa de instalación, en el símbolo del sistema escriba: "change user /execute"
-   Debe ser miembro del grupo de seguridad Administradores locales en el equipo cliente y servidor para configurar la base de datos de WSUS del servidor SQL Server remoto.
-   Para obtener más información acerca de los problemas de SQL remoto, consulte "Apéndice C: SQL remoto" en [Guía paso a paso para empezar a trabajar con Microsoft Windows Server Update Services](http://go.microsoft.com/fwlink/?linkid=41777).

#### Problema 13: es posible que un servidor que sigue en la cadena de réplica tenga menos aprobaciones que el servidor que precede en la cadena principal

Es posible que un servidor que sigue en la cadena de réplica tenga menos aprobaciones que el servidor que precede en la cadena principal. Esto se debe a las aprobaciones de instalación no fluyen al servidor que sigue en la cadena hasta que termina de descargarse el contenido en el servidor que precede en la cadena.

#### Problema 14: volver a intentar la sincronización tras un error de sincronización inicial

Si se produce un error en la sincronización, la primera acción para solucionar el problema debe ser volver a intentar sincronizar el servidor. En caso de error de la sincronización posterior, use la información de solución de problemas de la Guía de operaciones de WSUS.

#### Problema 15: al intentar obtener acceso a la consola de administración de WSUS, aparece un mensaje de error System.IO.FileNotFoundException

Si aparece el siguiente mensaje de error, es posible que tenga que ajustar los permisos en las cuentas del servicio de red o de ASP.NET:

System.IO.FileNotFoundException: No se encuentra el archivo o el nombre del ensamblado *xxxxxx*.dll o una de sus dependencias.

Donde *xxxx* es un nombre aleatorio.

Para resolver este problema en los sistemas operativos Windows Server 2003, conceda a la cuenta del servicio de red acceso de lectura/escritura a %systemroot%\\Temp. En Windows 2000 Server, conceda a la cuenta de ASP.NET acceso de lectura/escritura a %systemroot%\\Temp.

#### Problema 16: SQL Security Update MS03-031 (KB815495)

Puede parecer que esta actualización se haya instalado en el servidor WSUS aunque en realidad haya habido errores en la instalación en el cliente. Esto puede hacer que se vuelva a ofrecer el paquete al cliente. Para solucionar este problema, no apruebe la actualización en el servidor.

#### Problema 17: la configuración de IIS se pierde durante la actualización de RTM

Si instala WSUS RTM en un servidor en el que hay una versión anterior de WSUS (por ejemplo, RC), WSUS RTM desinstalará la versión anterior e instalará la nueva. Esto significa que vroots y los archivos asociados a WSUS en IIS se eliminarán.

Si instaló WSUS en el sitio Web predeterminado, perderá toda la configuración relacionada con WSUS hecha en vroots de WSUS. Por ejemplo, si ha configurado vroots de WSUS para SSL con el fin de proteger WUS, tendrá que volver a configurarlos después de instalar la versión RTM de WSUS. Nota: recibirá una notificación en la consola de WSUS que indica que SSL no está habilitado.

Si ha instalado WSUS en un sitio Web que no sea el predeterminado, se perderá toda la configuración adicional del sitio Web de WSUS.

#### Problema 18: uso de encabezados de host

Si desea asignar valores de encabezado de host al sitio Web predeterminado (sitio Web de WSUS) en IIS, es necesario agregar “Todas sin asignar” o una dirección IP asignada a la lista de direcciones IP sin ningún valor de encabezado de host al sitio Web predeterminado. También se debe agregar al sitio Web no predeterminado.

**Advertencia**: puede impedir la funcionalidad de Microsoft SharePoint y Exchange.

#### Problema 19: es necesario agregar la dirección URL de la consola de WSUS a la lista de zonas de contenido Web Sitios de confianza e Intranet local en equipos en los que el endurecimiento de Internet Explorer está habilitado

Si el endurecimiento de Internet Explorer (también conocido como componente Configuración de seguridad mejorada de Internet Explorer de Microsoft Windows Server 2003) está habilitado en un equipo y no agrega la consola de WSUS en las zonas de contenido Web Sitios de confianza e Intranet local, se le pedirán las credenciales de usuario cada vez que abra una página en la consola de WSUS.

Para agregar la consola de WSUS a las zonas de contenido Web **Intranet local** y **Sitios de confianza**:

1.  Abra **Opciones de Internet** (por ejemplo, haga clic en **Inicio**, seleccione **Panel de control** y, a continuación, haga clic en **Opciones de Internet**).
2.  En la ficha **Seguridad**, haga clic en **Intranet local**, en **Sitios** y en **Opciones avanzadas**, agregue la dirección URL (http://*WSUSServername*/WSUSAdmin) y haga clic en **Aceptar**.
3.  Haga clic en **Sitios de confianza** y en **Sitios**, agregue la dirección URL de la consola de WSUS, haga clic en **Aceptar** y, a continuación, en **Aceptar** otra vez para salir de **Opciones de Internet**.

#### Copyright

La información que contiene este documento representa la visión actual de Microsoft Corporation sobre los temas tratados en la fecha de publicación. Dado que Microsoft debe responder a las condiciones cambiantes del mercado, no debe interpretarse como un compromiso por parte de Microsoft, y Microsoft no puede garantizar la precisión de cualquier información presentada después de la fecha de publicación.

Este documento tiene únicamente fines informativos. MICROSOFT NO OTORGA NINGUNA GARANTÍA, EXPLÍCITA, IMPLÍCITA O ESTATUTARIA, A LA INFORMACIÓN INCLUIDA EN ESTE DOCUMENTO.

Es responsabilidad del usuario el cumplimiento de todas las leyes de derechos de autor aplicables. Sin limitar los derechos correspondientes de acuerdo con la ley de derechos de autor, ninguna parte de este documento puede ser reproducida, almacenada ni introducida en un sistema de recuperación, ni transmitida de ninguna forma, por ningún medio (ya sea electrónico, mecánico, mediante fotocopias, grabación u otros) y con ningún propósito sin la previa autorización por escrito de Microsoft Corporation.

Microsoft puede ser titular de patentes o tener solicitudes de patentes, marcas comerciales, derechos de autor y otros derechos sobre la propiedad intelectual acerca del contenido de este documento. La difusión del mismo no le otorga ninguna licencia sobre estas patentes, marcas comerciales, derechos de autor ni otros derechos sobre la propiedad intelectual, a menos que se indique por escrito en un contrato de licencia de Microsoft.

A menos que se indique lo contrario, los nombres de las compañías, organizaciones, productos, nombres de dominio, direcciones de correo electrónico, logotipos, personas, lugares y acontecimientos utilizados en los ejemplos son ficticios y no representan de ningún modo a ninguna compañía, organización, producto, nombre de dominio, dirección de correo electrónico, logotipo, persona, lugar o acontecimiento real.

© 2006 Microsoft Corporation. Reservados todos los derechos.

Microsoft, SQL Server, Windows y Windows Server son marcas registradas o marcas comerciales de Microsoft Corporation en Estados Unidos y otros países.

Los nombres de compañías y productos reales mencionados en este documento pueden ser marcas comerciales de sus respectivos propietarios.
