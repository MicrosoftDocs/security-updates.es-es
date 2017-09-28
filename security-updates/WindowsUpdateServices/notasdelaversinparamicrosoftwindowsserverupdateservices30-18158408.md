---
TOCTitle: 'Notas de la versión para Microsoft Windows Server Update Services 3.0'
Title: 'Notas de la versión para Microsoft Windows Server Update Services 3.0'
ms:assetid: '94d1385f-4872-4c29-8822-3a4ec5e45ae4'
ms:contentKeyID: 18158408
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708491(v=WS.10)'
---

Notas de la versión para Microsoft Windows Server Update Services 3.0
=====================================================================

Estas notas de la versión describen problemas conocidos que afectan a Microsoft® Windows® Server Update Services (WSUS) 3.0, además de incluir las recomendaciones y los requisitos necesarios para instalar la aplicación. Estas notas contienen las siguientes secciones:

-   Requisitos del sistema para la instalación de servidor WSUS 3.0
-   Requisitos de configuración para la instalación de servidor WSUS 3.0
-   Requisitos del sistema para la instalación de consola remota de WSUS 3.0
-   Requisitos de configuración para consolas remotas de WSUS 3.0
-   Requisitos del sistema para la instalación de cliente
-   Requisitos de software para la instalación de servidor WSUS 3.0
-   Requisitos de espacio mínimo en disco para la instalación de servidor WSUS 3.0
-   Requisitos de actualización de WSUS 3.0
-   Parámetros de línea de comandos de instalación
-   Problemas de instalación y actualización
-   Problemas conocidos
-   WSUS 3.0 en Windows Server® 2008
-   WSUS 3.0 en Windows Small Business Server 2003

| ![](images/Cc708491.note(WS.10).gif)Nota                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Puede descargar una copia de este documento en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=71220) ([http://go.microsoft.com/fwlink/?LinkId=71220](http://go.microsoft.com/fwlink/?linkid=71220)). |

Cuestión de configuración importante: debe sobrescribir la contraseña de servidor proxy en el asistente para la configuración
-----------------------------------------------------------------------------------------------------------------------------

Si usa un servidor proxy que requiere autenticación de nombre de usuario/contraseña, el servidor WSUS no podrá sincronizar las actualizaciones si no sobrescribe la contraseña de servidor proxy al ejecutar el asistente para la configuración del servidor WSUS. Como el asistente para la configuración se inicia automáticamente al final de la instalación, este problema puede provocar errores de sincronización después de actualizar a WSUS 3.0 desde una versión anterior de WSUS.

Puede evitar este problema si cancela el asistente para la configuración después de la actualización o si vuelve a especificar la contraseña de proxy correcta cuando se ejecute el asistente para la configuración. Para recuperarse de este problema después de que se haya producido, vaya a **Actualizar origen y servidor proxy** en la página **Opciones**, vuelva a especificar la contraseña de proxy y, a continuación, guarde la configuración.

Requisitos del sistema para la instalación de servidor WSUS 3.0
---------------------------------------------------------------

#### El servidor WSUS 3.0 se admite en Windows Server 2003 Service Pack 1 y Windows Server 2008

El servidor WSUS 3.0 se admite en Windows Server 2003 Service Pack 1 y Windows Server 2008.

#### Windows 2000 Server no es compatible con servidores WSUS 3.0

Microsoft Windows® 2000 Server no es un sistema operativo compatible con servidores WSUS 3.0.

#### no se admite WSUS 3.0 en aquellos servidores que ejecutan Servicios de Terminal Server

Aunque WSUS 3.0 se puede ejecutar en servidores con Terminal Services, no se admite ni se recomienda. WSUS 3.0 no se ejecutará en un servidor con Terminal Services en configuraciones que usen implementaciones de SQL Server remoto. Dado que todas las acciones personalizadas remotas (incluida la instalación) en un servidor de licencia de Servicios de Terminal Server se ejecutarán como la cuenta del sistema, y la cuenta de sistema del servidor puede no tener permisos en el SQL Server remoto, la instalación podría no realizarse correctamente.

Requisitos de configuración para la instalación de servidor WSUS 3.0
--------------------------------------------------------------------

#### hay que tener instalado IIS

Microsoft Windows Server Update Services 3.0 requiere Servicios de Internet Information Server (IIS), que no se instala de forma predeterminada en Microsoft Windows Server 2003 ni en Windows Server 2008. Si intenta instalar WSUS 3.0 sin tener instalado IIS, el programa de instalación de Windows Server Update Services muestra un mensaje de error que indica que IIS no está instalado

#### Si IIS se ejecuta en modo aislado de IIS 5.0, no se realizará la instalación

Si ha actualizado el servidor de Windows 2000 Server a Windows Server 2003, IIS puede estar ejecutándose en modo de compatibilidad con IIS 5.0. También se puede habilitar el modo aislado de IIS 5.0 en Administrador de IIS. Esto provocará un error en la instalación. Deberá deshabilitar el modo aislado de IIS 5.0 antes de instalar WSUS 3.0.

#### si cualquier componente de IIS se instala en modo compatible de 32 bits en una plataforma de 64 bits, puede fallar la instalación de WSUS 3.0

Todos los componentes de IIS deben instalarse en modo nativo en plataformas de 64 bits. Si cualquier componente de IIS está en modo compatible de 32 bits, la instalación puede fallar.

#### los servidores proxy deben admitir tanto HTTP como HTTPS

Cuando se configura el servidor WSUS raíz (es decir, el servidor WSUS que obtiene las actualizaciones directamente de Microsoft Update) y hay un servidor proxy entre el servidor WSUS e Internet, este servidor proxy debe admitir tanto HTTP como HTTPS.

#### Si dos o más sitios web ya se ejecutan en el puerto 80, elimine todos menos uno antes de instalar WSUS

Si ya tiene dos o más sitios web que se ejecutan en el puerto 80 (por ejemplo, Windows® SharePoint® Services), debe eliminar todos menos uno antes de instalar WSUS. Si no lo hace así, puede que los clientes del servidor no se actualicen automáticamente.

#### al instalar WSUS 3.0, puede que tenga que deshabilitar los programas antivirus

Al instalar WSUS 3.0, puede que tenga que deshabilitar programas antivirus antes de que pueda realizar la instalación correctamente. Después de deshabilitar el programa antivirus, reinicie el equipo antes de iniciar la instalación de WSUS. Al reiniciar el equipo se evita que los archivos estén bloqueados cuando el proceso de instalación necesite tener acceso a ellos. Una vez que se complete la instalación, asegúrese de volver a habilitar los programas antivirus. Visite el sitio Web del proveedor de programas antivirus con el fin de seguir el procedimiento exacto para deshabilitar y volver a habilitar programas y versiones antivirus.

| ![](images/Cc708491.Caution(WS.10).gif)Precaución                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Esta solución alternativa puede hacer que su equipo o su red sean más vulnerables a los ataques de usuarios malintencionados o por software dañino como los virus. No se recomienda esta solución alternativa pero le facilitamos esta información para que pueda implementarla según su criterio. Usted asume todo el riesgo derivado del uso de esta solución. |

| ![](images/Cc708491.note(WS.10).gif)Nota                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Un programa antivirus está diseñado para proteger su equipo de virus. No debe descargar ni abrir archivos de orígenes que no sean de confianza, visitar sitios Web en los que no confíe ni abrir adjuntos de correo electrónico cuando su programa antivirus esté deshabilitado. |

#### WSUS 3.0 requiere que se active la opción de desencadenadores anidados en SQL Server

La opción de desencadenadores anidados está activada de manera predeterminada; sin embargo, un administrador de SQL Server puede desactivarla.

Si tiene pensado utilizar una base de datos de SQL Server como almacén de datos de Windows Server Update Services, el administrador de SQL Server deberá comprobar que la opción de desencadenadores anidados esté activada antes de que el administrador de WSUS 3.0 instale WSUS 3.0 y especifique la base de datos durante la instalación.

El programa de instalación de WSUS 3.0 activa la opción RECURSIVE\_TRIGGERS, que es una opción específica de base de datos; sin embargo, no activa la opción de desencadenadores anidados, que es una opción global de servidor.

Para ver si la opción de desencadenadores anidados está activada, use lo siguiente:

**sp\_configure 'nested triggers'**

Para activar la opción de desencadenadores anidados en SQL Server, ejecute lo siguiente desde un archivo por lotes en el equipo que ejecuta SQL Server:

**sp\_configure 'nested triggers', 1**

**GO**

**RECONFIGURE**

**GO**

Si no tiene SQL Server Management Studio en su servidor, puede ejecutar las secuencias de comandos de SQL desde la línea de comandos. Puede obtener la herramienta de consulta de línea de comandos de Microsoft SQL Server 2005 en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=70728) (http://go.microsoft.com/fwlink/?LinkId=70728; esta página puede estar en inglés). Para comenzar, ejecute **sqlcmd**.

Si desea ejecutar las secuencias de comandos SQL en Windows Internal Database, también debe descargar SQL Native Client desde la misma página de descarga.

#### limitaciones y requisitos de SQL remoto

WSUS 3.0 ofrece soporte para ejecutar software de base de datos en un equipo independiente del equipo con el resto de la aplicación WSUS 3.0. Existen algunos requisitos para configurar una instalación de SQL remoto

-   No se puede usar un servidor configurado como controlador de dominio para el back-end del par remoto.
-   No debe ejecutar Terminal Server en el equipo que será el servidor front-end de una instalación de SQL remoto.
-   Debe usar al menos Microsoft SQL Server 2005 Service Pack 1 (disponible en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=66143) (http://go.microsoft.com/fwlink/?LinkId=66143) para el software de base de datos en el equipo back-end si dicho equipo ejecuta Windows Server 2003 y SQL Server 2005 Service Pack 2 si ejecuta Windows Server® 2008.
-   Tanto los equipos front-end como back-end se deben unir a un dominio de Active Directory; de lo contrario, si se encuentran en dominios diferentes, debe establecer una confianza entre los dominios antes de ejecutar el programa de instalación de WSUS.
-   Si ya tiene instalado WSUS 2.0 en una configuración SQL remota y desea actualizarlo a WSUS 3.0, deberá desinstalar WSUS 2.0 (mediante **Agregar o quitar programas** en el Panel de control) del equipo back-end, además de asegurarse de que la base de datos permanece intacta. A continuación, debe instalar SQL Server 2005 SP1 o SP2 y actualizar la base de datos existente. Finalmente, debe instalar WSUS 3.0 en el equipo front-end.

#### no se puede instalar WSUS cuando ya están instaladas determinadas versiones preliminares de Internet Explorer 7 más Terminal Services

El programa de instalación de WSUS no podrá completarse si están presentes determinados candidatos a la versión comercial de Internet Explorer 7 junto con Terminal Services.

Requisitos del sistema para la instalación de consola remota de WSUS 3.0
------------------------------------------------------------------------

La consola remota de WSUS 3.0 se puede instalar en las siguientes plataformas:

-   Windows Server 2008
-   Windows Vista®
-   Windows Server 2003 SP1
-   Windows XP SP2

Requisitos de configuración para consolas remotas de WSUS 3.0
-------------------------------------------------------------

#### Debe usar una conexión de banda ancha entre una consola de administración remota y un servidor WSUS 3.0

Se pueden producir problemas de rendimiento si se conecta al servidor WSUS 3.0 con una consola de administración remota a través de una conexión WAN de banda estrecha. Puede limitar el número de actualizaciones y equipos que ve si filtra las vistas de actualizaciones y de equipos, pero se recomienda usar una conexión de banda ancha entre la consola de administración remota y los servidores WSUS 3.0. Si tiene problemas de rendimiento con la consola remota, se recomienda conectar con el servidor con Terminal Server para la administración remota.

Requisitos del sistema para la instalación de cliente
-----------------------------------------------------

Actualizaciones automáticas es el software del cliente de WSUS. Se puede usar con WSUS en cualquiera de los sistemas operativos siguientes:

-   Windows Vista
-   Windows Server 2008
-   Microsoft Windows Server 2003, cualquier edición
-   Microsoft Windows XP Professional SP2
-   Microsoft Windows 2000 Professional SP4, Windows 2000 Server SP4 o Windows 2000 Advanced Server con SP4

Requisitos de software para la instalación de servidor WSUS 3.0
---------------------------------------------------------------

En la tabla siguiente se muestra el software requerido para las plataformas Windows Server 2003 SP1. El software requerido para Windows Server 2008 se abordará en la sección que trata de WSUS 3.0 en Windows Server 2008.

Asegúrese de que el servidor WSUS 3.0 cumple los requisitos de esta lista antes de ejecutar el programa de instalación de WSUS 3.0. Si cualquiera de estas actualizaciones requiere reiniciar el equipo una vez completada la instalación, deberá reiniciar antes de instalar WSUS 3.0.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Requisito</th>
<th>Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Servicios de Microsoft Internet Information Server (IIS)</p></td>
<td style="border:1px solid black;"><p>Instalar desde el sistema operativo.</p>
<p>Ver problema 1: hay que tener instalado IIS.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Microsoft .NET Framework 2.0 Redistributable Package (x86)</p></td>
<td style="border:1px solid black;"><p>Vea Microsoft .NET Framework 2.0 Redistributable Package (x86) en el <a href="http://go.microsoft.com/fwlink/?linkid=68935">Centro de descarga de Microsoft</a> (http://go.microsoft.com/fwlink/?LinkId=68935; esta página puede estar en inglés). Para plataformas de 64 bits, vea Microsoft .NET Framework 2.0 Redistributable Package (x64) en el <a href="http://go.microsoft.com/fwlink/?linkid=70637">Centro de descarga de Microsoft</a> (http://go.microsoft.com/fwlink/?LinkId=70637; esta página puede estar en inglés).</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Microsoft Management Console 3.0 para Windows Server 2003</p></td>
<td style="border:1px solid black;"><p>Este es un requisito previo para poder usar la interfaz de usuario de WSUS 3.0. Vea Microsoft Management Console 3.0 para Windows Server 2003 (KB907265) en el <a href="http://go.microsoft.com/fwlink/?linkid=70412">Centro de descarga de Microsoft</a> (http://go.microsoft.com/fwlink/?LinkId=70412; esta página puede estar in inglés). Para plataformas de 64 bits, vea Microsoft Management Console 3.0 para Windows Server 2003 x64 Edition (KB907265) en el <a href="http://go.microsoft.com/fwlink/?linkid=70638">Centro de descarga de Microsoft</a> (http://go.microsoft.com/fwlink/?LinkId=70638; esta página puede estar en inglés).</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Microsoft Report Viewer</p></td>
<td style="border:1px solid black;"><p>Este es un requisito previo para usar la interfaz de usuario de WSUS 3.0. Vea Microsoft Report Viewer Redistributable 2005 en el <a href="http://go.microsoft.com/fwlink/?linkid=70410">Centro de descarga de Microsoft</a> (http://go.microsoft.com/fwlink/?LinkId=70410; esta página puede estar en inglés).</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>SQL Server 2005 (opcional)</p></td>
<td style="border:1px solid black;"><p>WSUS 3.0 instalará Windows Internal Database automáticamente si no hay instalada una versión compatible de SQL Server. Si planea usar una base de datos de SQL Server completa, debe usar, como mínimo, SQL Server 2005 SP1 (disponible en el <a href="http://go.microsoft.com/fwlink/?linkid=66143">Centro de descarga de Microsoft</a> (http://go.microsoft.com/fwlink/?LinkId=66143) en Windows Server 2003 o SQL Server 2005 SP2 (disponible en el <a href="http://go.microsoft.com/fwlink/?linkid=84823">Centro de descarga de Microsoft</a> en http://go.microsoft.com/fwlink/?LinkId=84823) para Windows Server 2008.</p></td>
</tr>
</tbody>
</table>
  
| ![](images/Cc708491.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                     |  
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| Si se ha instalado WSUS 2.0 anteriormente y se está usando SQL Server 2000, SQL Server Desktop Engine 2000 o cualquier base de datos de SQL Server anterior a SQL Server 2005 SP1 (o SQL Server 2005 SP2 en Windows Server 2008), el programa de instalación de WSUS 3.0 instalará Windows® Internal Database y migrará la base de datos a esa ubicación. |
  
Requisitos de espacio mínimo en disco para la instalación de servidor WSUS 3.0  
------------------------------------------------------------------------------
  
Los requisitos mínimos de espacio en disco para instalar Windows Server Update Services son los siguientes:
  
-   1 GB en la partición del sistema  
-   2 GB para el volumen en el que se almacenarán los archivos de base de datos  
-   20 GB para el volumen en el que se almacena el contenido
  
| ![](images/Cc708491.Important(WS.10).gif)Importante                           |  
|------------------------------------------------------------------------------------------------------------|  
| No se puede instalar WSUS 3.0 en unidades comprimidas. Compruebe que la unidad elegida no esté comprimida. |
  
Requisitos de actualización de WSUS 3.0  
---------------------------------------
  
#### Asegúrese de que la instalación de WSUS funciona correctamente y haga una copia de seguridad de la base de datos de WSUS antes de realizar la actualización
  
Si está actualizando a WSUS 3.0 desde una versión anterior, asegúrese de que la instalación actual funciona correctamente y haga una copia de seguridad de la base de datos de WSUS antes de la actualización.
  
1.  Compruebe si hay errores recientes en los registros de eventos, problemas con la sincronización entre los servidores que siguen en la cadena y los servidores que preceden en la cadena, o problemas con clientes que no notifican. Asegúrese de que estos problemas se han resuelto antes de continuar.  
2.  Puede ejecutar DBCC CHECKDB para asegurarse de que la base de datos de WSUS está indizada correctamente. Para obtener más información acerca de CHECKDB, vea [DBCC CHECKDB](http://go.microsoft.com/fwlink/?linkid=86948) (http://go.microsoft.com/fwlink/?LinkId=86948).  
3.  Haga una copia de seguridad de la base de datos de WSUS.
  
#### hay que desinstalar Software Update Services 1.0
  
La instalación de WSUS 3.0 no se realizará correctamente si Software Update Services 1.0 está instalado en el mismo equipo. Debe instalar Software Update Services 1.0 antes de instalar WSUS 3.0.
  
#### no se admite la actualización de una versión beta de WSUS 3.0 a la versión de lanzamiento de WSUS 3.0, pero se permite la actualización de la versión RC a la versión de lanzamiento
  
Si ya tiene instalada una versión beta de WSUS 3.0, deberá desinstalarla y eliminar la base de datos antes de realizar la instalación de la versión de lanzamiento de WSUS 3.0. Es posible realizar únicamente la actualización de la versión RC a la versión de lanzamiento.
  
#### no es posible actualizar WSUS 2.0 a WSUS 3.0 en un sistema operativo de 64 bits
  
WSUS 2.0 no es compatible con los sistema operativos de 64 bits. No es posible actualizar WSUS 2.0 a WSUS 3.0 en sistemas de 64 bits.
  
Parámetros de línea de comandos de instalación  
----------------------------------------------
  
Puede realizar instalaciones desatendidas de WSUS 3.0 si utiliza parámetros de línea de comandos de WSUS. Esta tabla muestra los parámetros de línea de comandos para WSUS 3.0.
  
###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opción</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p><strong>/q</strong></p></td>
<td style="border:1px solid black;"><p>Realizar una instalación silenciosa.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p><strong>/u</strong></p></td>
<td style="border:1px solid black;"><p>Desinstalar el producto. También desinstala la instancia de Windows Internal Database si está instalada.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p><strong>/p</strong></p></td>
<td style="border:1px solid black;"><p>Comprobación de requisitos previos únicamente. No instala el producto, sino que inspecciona el sistema y notifica cualquier requisito previo que falte.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p><strong>/?, /h</strong></p></td>
<td style="border:1px solid black;"><p>Muestra los parámetros de línea de comandos y sus descripciones.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p><strong>/g</strong></p></td>
<td style="border:1px solid black;"><p>Actualizar desde la versión 2.0 de WSUS. El único parámetro válido con esta opción es /q (instalación silenciosa). La única propiedad válida con esta opción es DEFAULT_WEBSITE.</p></td>
</tr>
</tbody>
</table>
  
Esta tabla muestra las propiedades de línea de comandos para WSUS 3.0.
  
###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propiedad</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>CONTENT_LOCAL</p></td>
<td style="border:1px solid black;"><p>0=contenido alojado localmente, 1=alojado en Microsoft Update</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>CONTENT_DIR</p></td>
<td style="border:1px solid black;"><p>Ruta de acceso al directorio de contenido. El valor predeterminado es <em>unidadDeInstalaciónDeWSUS</em><strong>\WSUS\WSUSContent</strong>, donde <em>unidadDeInstalaciónDeWSUS</em> es la unidad local con la mayor cantidad de espacio libre.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>WYUKON_DATA_DIR</p></td>
<td style="border:1px solid black;"><p>Ruta de acceso al directorio de datos de Windows Internal Database.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>SQLINSTANCE_NAME</p></td>
<td style="border:1px solid black;"><p>El nombre debería aparecer con el formato <em>NombreServidor</em>\<em>NombreInstanciaSQL</em>. Si la instancia de la base de datos se encuentra en el equipo local, use la variable de entorno %COMPUTERNAME%. Si no está presente una instancia existente, de forma predeterminada sería %COMPUTERNAME%\WSUS.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DEFAULT_WEBSITE</p></td>
<td style="border:1px solid black;"><p>0=puerto 8530, 1=puerto 80</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>PREREQ_CHECK_LOG</p></td>
<td style="border:1px solid black;"><p>Ruta de acceso y nombre de archivo del archivo de registro</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>CONSOLE_INSTALL</p></td>
<td style="border:1px solid black;"><p>0=instala el servidor WSUS, 1=instala sólo la consola</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>ENABLE_INVENTORY</p></td>
<td style="border:1px solid black;"><p>0=no instalar características de inventario, 1=instalar características de inventario</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DELETE_DATABASE</p></td>
<td style="border:1px solid black;"><p>0=mantener base de datos, 1=quitar base de datos</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>DELETE_CONTENT</p></td>
<td style="border:1px solid black;"><p>0=mantener archivos de contenido, 1=quitar archivos de contenido</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>DELETE_LOGS</p></td>
<td style="border:1px solid black;"><p>0=mantener archivos de registro, 1=quitar archivos de registro (se usa con el modificador de instalación /u).</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>CREATE_DATABASE</p></td>
<td style="border:1px solid black;"><p>0=usar base de datos actual, 1=crear base de datos</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>PROGRESS_WINDOW_HANDLE</p></td>
<td style="border:1px solid black;"><p>Controlador de ventana para regresar a los mensajes de progreso de MSI.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>MU_ROLLUP</p></td>
<td style="border:1px solid black;"><p>1=unirse al Programa de mejora de Microsoft Update, 0=no unirse</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>FRONTEND_SETUP</p></td>
<td style="border:1px solid black;"><p>1=no escribir la ubicación del contenido en la base de datos, 0=escribir la ubicación del contenido en la base de datos (para NLB)</p></td>
</tr>
</tbody>
</table>
  
#### Ejemplo de uso
  
```  
WSUSSetup.exe /q DEFAULT\_WEBSITE=0 (install in quiet mode using port 8530) WSUSSetup.exe /q /u (uninstall WSUS)  
```  
| ![](images/Cc708491.Important(WS.10).gif)Importante                                                                                                                                |  
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| Si instala WSUS 3.0 en modo silencioso (/q) y el equipo no tiene todos los requisitos previos instalados, la instalación generará un archivo llamado WSUSPreReqCheck.xml y lo guardará en el directorio %TEMP%. |
  
Problemas de instalación  
------------------------
  
#### IIS se reiniciará durante la instalación de WSUS 3.0
  
El programa de instalación de WSUS 3.0 reiniciará IIS sin notificación, lo que puede afectar a los sitios Web existentes en su organización. Si IIS no se está ejecutando, el programa de instalación de WSUS 3.0 lo iniciará.
  
#### si las conexiones están abiertas a una base de datos de WSUS existente, pueden producirse errores de instalación
  
Si actualiza a WSUS 3.0 desde una instalación existente y las conexiones están aún abiertas a una base de datos de WSUS existente (por ejemplo, si SQL Server Management Studio está abierto), pueden producirse errores de instalación. Cierre todas las conexiones y vuelva a instalar WSUS 3.0.
  
#### el programa de instalación de WSUS indica un directorio incorrecto para los archivos de base de datos
  
En el programa de instalación de WSUS, la pantalla **Listo para instalar** informa erróneamente de que la ubicación de la base de datos es el directorio primario de la ubicación de la base de datos. Por ejemplo, la ubicación predeterminada es %systemdrive%\\WSUS\\UpdateServicesDbFiles, pero esta ubicación aparece incorrectamente como %systemdrive%\\WSUS.
  
#### Si WSUS se instala en un equipo que tenga paquetes de idioma de interfaz de usuario multilingüe con un idioma predeterminado distinto del inglés, la Ayuda se mostrará en el idioma predeterminado en vez hacerlo en inglés
  
Si tiene un equipo con paquetes de idioma de interfaz de usuario multilingüe con un idioma predeterminado distinto del inglés, podrá instalar WSUS cuando la configuración regional del usuario actual sea inglés. La interfaz de usuario se mostrará en inglés, pero debe usar una solución para que la Ayuda también se muestre en inglés. Copie el archivo .chm de la Ayuda en inglés (*directorioInstalaciónWSUS*\\documentation\\mui\\0409\\WSUS30Help.chm) al directorio de documentación principal (*directorioInstalaciónWSUS*\\documentation\\WSUS30Help.chm). En este punto, la Ayuda se debe mostrar correctamente en todos los idiomas.
  
Problemas de actualización  
--------------------------
  
#### La actualización de WSUS 3.0 RC a WSUS 3.0 RTM provocará que el certificado SSL no se asigne al sitio web de WSUS
  
El sitio web de WSUS se elimina y se vuelve a crear durante la actualización de WSUS 3.0 RC a WSUS 3.0 RTM. Como consecuencia, el certificado SSL ya no estará asignado al sitio web de WSUS. Deberá reasignar el certificado después de la actualización.
  
#### recuperación de una actualización realizada con errores
  
Si actualiza de WSUS 2.0 a WSUS 3.0 y se producen errores por cualquier razón, debe volver a instalar WSUS 2.0 y restaurar su base de datos desde la copia de seguridad.
  
#### no es posible actualizar de WSUS 2.0 a WSUS 3.0 si hay una base de datos de WSUS 3.0 de una instalación anterior
  
Si ha instalado previamente WSUS 3.0 y, a continuación, reinstala WSUS 2.0, tiene que eliminar la base de datos de WSUS 3.0 del equipo antes de intentar volver a instalar WSUS 3.0.
  
#### cambiar el nombre del equipo antes de actualizar a WSUS 3.0 puede causar un error en la actualización
  
Si cambia el nombre del equipo después de instalar WSUS 2.0 y antes de actualizar a WSUS 3.0, puede producirse un error en la actualización.
  
Use la siguiente secuencia de comandos para quitar y volver a agregar los grupos de administradores de ASPNET y WSUS. A continuación, ejecute de nuevo la actualización.
  
Tendrá que reemplazar *&lt;DBLocation&gt;* con la carpeta donde está instalada la base de datos, y *&lt;ContentDirectory&gt;* con la carpeta de almacenamiento local.
  
```  
sqlcmd.exe -S *&lt;DBLocation&gt;* -E -Q "USE SUSDB DECLARE @asplogin varchar(200) SELECT @asplogin=name from sysusers WHERE name like '%ASPNET' EXEC sp\_revokedbaccess @asplogin" sqlcmd.exe -S *&lt;DBLocation&gt;* -E -Q "USE SUSDB DECLARE @wsusadminslogin varchar(200) SELECT @wsusadminslogin=name from sysusers WHERE name like '%WSUS Administrators' EXEC sp\_revokedbaccess @wsusadminslogin"   sqlcmd.exe -S *&lt;DBLocation&gt;* -E -Q "USE SUSDB DECLARE @asplogin varchar(200) SELECT @asplogin=HOST\_NAME()+'\\ASPNET' EXEC sp\_grantlogin @asplogin EXEC sp\_grantdbaccess @asplogin EXEC sp\_addrolemember webService,@asplogin" sqlcmd.exe -S *&lt;DBLocation&gt;* -E -Q "USE SUSDB DECLARE @wsusadminslogin varchar(200) SELECT @wsusadminslogin=HOST\_NAME()+'\\WSUS Administrators' EXEC sp\_grantlogin @wsusadminslogin EXEC sp\_grantdbaccess @wsusadminslogin EXEC sp\_addrolemember webService,@wsusadminslogin"   sqlcmd.exe -S *&lt;DBLocation&gt;* -E -Q "backup database SUSDB to disk=N'*&lt;ContentDirectory&gt;*\\SUSDB.Dat' with init"  
```
  
#### el programa de instalación puede sobrescribir una copia de seguridad de base de datos anterior
  
El programa de instalación de WSUS 3.0 agregará la base de datos al directorio especificado durante la instalación. De forma predeterminada, el directorio es *%systemdrive%*\\WSUS\\UpdateServicesDbFiles. Si hay una copia de seguridad de base de datos anterior en el directorio, la nueva base de datos la sobrescribirá. Los administradores deben realizar una copia de seguridad de los archivos de base de datos antes de aplicar actualizaciones al equipo donde se ubique la base de datos.
  
#### Si ha migrado de MSDE a SQL Server 2000 o SQL Server 2005 en WSUS 2.0, deberá cambiar un valor del Registro
  
Si tiene una instalación de WSUS 2.0 y ha migrado de SQL Server 2000 o SQL Server 2005, deberá cambiar el valor **HKLM\\SOFTWARE\\Microsoft\\Update Services\\Server\\Setup\\WmsdeInstalled** de 1 a 0. Si no lo hace antes de actualizar a WSUS 3.0, la actualización no se realizará.
  
#### si se inicia y después se cancela el programa de instalación de WSUS 2.0, se eliminará la clave del Registro de WSUS
  
Si inicia el programa de instalación de WSUS 2.0 y después lo cancela, se eliminará la clave del Registro de WSUS. Esto puede causar problemas si WSUS 3.0 ya está instalado. Puede que se produzca el mismo problema si comienza a desinstalar WSUS 2.0, cancela esta operación y, a continuación, intenta actualizar WSUS 2.0 a WSUS 3.0.
  
#### si se desinstala WSUS 3.0 y se dejan los archivos de registro, éstos podrían no tener los permisos correctos después de reinstalar
  
Al desinstalar WSUS 3.0, tiene la opción de conservar los archivos de registro de la instalación. Al reinstalar WSUS 3.0, los archivos de registro antiguos pierden sus permisos (normalmente sólo para administradores de WSUS). Debe restaurar los permisos de esos archivos de registro.
  
#### si se instaló Windows SharePoint Services después de la versión RC de WSUS 3.0, la actualización a la versión de lanzamiento de WSUS 3.0 tendrá lugar mediante una solución alternativa
  
Si instaló la versión RC de WSUS 3.0 y después instaló Windows SharePoint Services en el mismo equipo, únicamente puede realizar la actualización a la versión de lanzamiento de WSUS 3.0 si elige realizar la instalación en el puerto personalizado (puerto 8530). Para realizar esta instalación desde la línea de comandos, abra un shell de comando y después escriba el comando: **WSUSSetup /q / g/ DEFAULT\_WEBSITE=0**. (Para realizar esta instalación a través de la interfaz de usuario, escriba **WSUSSetup /g DEFAULT\_WEBSITE=0**.)
  
Si WSUS se instala en un equipo con paquetes de idioma de interfaz de usuario multilingüe instalados, la Ayuda se mostrará en el idioma predeterminado en vez hacerlo en el idioma actual del usuario
  
#### Si los clientes WSUS 2.0 tienen actualizaciones con el estado No aplicable, las actualizaciones aparecerán como "Desconocido" durante breve periodo después de actualizar a WSUS 3.0
  
Si un servidor WSUS 2.0 tiene clientes con actualizaciones de tipo No aplicable, estas actualizaciones aparecerán con el estado Desconocido durante un breve periodo después de que el servidor se actualice a WSUS 3.0. El estado de actualización volverá a No disponible la próxima vez que el cliente realice un análisis.
  
Problemas conocidos  
-------------------
  
#### error de solución de problemas de diversos errores de descarga o de la sincronización repetida del cliente
  
Si los clientes de WSUS 3.0 notifican diversos errores de descarga o si no pueden realizar la sincronización con el servidor WSUS 3.0 durante un período de tiempo prolongado, es probable que tenga dañada la caché de descarga del equipo cliente. Para recuperarla de este estado, puede eliminar la caché de descarga del equipo cliente desde el sistema de archivos.
  
Para eliminar la caché de descarga del equipo cliente:
  
1.  Elimine todos los archivos y subdirectorios de esta ubicación en el equipo cliente: **%windir%\\SoftwareDistribution\\Download**  
2.  Intente instalar la actualización sincronizando nuevamente el equipo cliente con WSUS 3.0. Este intento de instalación debe dar el siguiente error: **WU\_E\_DM\_NOTDOWNLOADED, "la actualización no se ha descargado".**  
3.  Tras este error, el equipo cliente reiniciará automáticamente la descargar y la instalación podrá reanudarse.
  
#### si la sincronización falla, vuelva a intentarlo
  
Si la sincronización falla, su primera medida para solucionar el problema debe ser intentar sincronizar el servidor de nuevo. Si la siguiente sincronización falla, use la información para solucionar problemas que se proporciona en la [guía de operaciones de Windows Server Update Services 3.0](http://go.microsoft.com/fwlink/?linkid=81072) (http://go.microsoft.com/fwlink/?LinkId=81072; esta página puede estar en inglés).
  
#### no se puede cambiar la configuración de WSUS 3.0 directamente en la base de datos
  
Windows Server Update Services almacena sus datos de configuración en una base de datos de SQL Server. Sin embargo, no se pueden cambiar los datos de configuración accediendo directamente a la base de datos. No intente modificar la configuración de WSUS 3.0 accediendo directamente a la base de datos. Debe cambiar la configuración de WSUS 3.0 utilizando la consola de WSUS 3.0 o llamando a las API de WSUS 3.0.
  
#### los errores de descarga no se notifican rápidamente si están activadas las cuotas de disco
  
Si las cuotas de disco están activadas y se alcanza la cuota, puede que no se informe oportunamente de los errores de descarga de la actualización en el servidor WSUS. Para evitar este problema, deshabilite las cuotas de disco o aumente la cuota.
  
#### Si WSUS 3.0 se implementa con SSL, los equipos cliente pueden presentar errores con un código de error 0x8024400a
  
Los equipos cliente en ocasiones pueden presentar errores con un código de error "0x8024400a" cuando se comunican con un servidor WSUS 3.0 utilizando SSL. Para obtener una actualización que trata este problema, vea [KB 905422](http://go.microsoft.com/fwlink/?linkid=70593) (http://go.microsoft.com/fwlink/?LinkId=70593; esta página puede estar en inglés).
  
#### la cuenta de dominio de los administradores de WSUS no se eliminará cuando se desinstale WSUS
  
El grupo de administradores de WSUS se crea como una cuenta de dominio (no como una cuenta local) en los controladores de dominio, de manera que todas las instalaciones que usan esa cuenta de dominio se deshabilitarían si la cuenta se eliminase al desinstalar WSUS. Por lo tanto, la desinstalación de WSUS no eliminará la cuenta de dominio de administradores de WSUS.
  
#### si un servidor que sigue en la cadena se convierte a un servidor que precede en la cadena, las actualizaciones del sitio del catálogo deben volver a importarse
  
Cuando se promociona un servidor que sigue en la cadena para ser un servidor que precede en la cadena, también tiene que volver a importar todas las actualizaciones del sitio del catálogo. De lo contrario, el sitio no sincronizará correctamente las nuevas revisiones de actualización del sitio del catálogo en este servidor.
  
#### si utiliza IIS con SSL, el acceso no cifrado es aún posible a menos que esté activada la casilla de verificación "Requerir canal seguro"
  
Si configura IIS para utilizar SSL instalando un certificado, aún es posible tener acceso al sitio mediante HTTP no cifrado a menos que esté activada la opción "Requerir canal seguro". Para obtener más información, vea la página acerca de la [habilitación del cifrado](http://go.microsoft.com/fwlink/?linkid=70601) (http://go.microsoft.com/fwlink/?LinkId=70601; esta página puede estar en inglés).
  
#### la importación del sitio del catálogo puede fallar si no se tienen permisos de lectura o escritura para la carpeta %windir%\\TEMP
  
Cuando se realiza la importación del sitio del catálogo, si la cuenta del servicio de red no tiene permisos de lectura o escritura para la carpeta %windir%\\TEMP, puede fallar la importación y mostrar un mensaje de error como el que aparece a continuación: "El servidor no pudo procesar la solicitud. ---&gt; No se encuentra el archivo 'C:\\WINDOWS\\TEMP\\*tempNombreArchivo*.dll'."
  
#### el rendimiento puede ser lento al sincronizar entre WSUS 3.0 y el servidor de réplica que sigue en la cadena que ejecuta WSUS 2.0
  
Si instala WSUS 3.0 en un servidor que precede en la cadena e intenta sincronizar con un servidor de réplica que sigue en la cadena que ejecuta WSUS 2.0, puede experimentar problemas de rendimiento. Para solucionar este problema, vea [KB 910847](http://go.microsoft.com/fwlink/?linkid=70669) (http://go.microsoft.com/fwlink/?LinkId=70669; esta página puede estar en inglés).
  
#### si el servidor de correo electrónico no funciona, la notificación de correo electrónico no se realiza
  
Si el servidor de correo electrónico de red está desactivado, WSUS 3.0 no enviará las notificaciones de correo electrónico. Sin embargo, escribirá el evento 10052 (HealthCoreEmailNotificationRed) en el registro de eventos.
  
#### las opciones cambiadas en un servidor que precede en la cadena no se envían inmediatamente al servidor que sigue en la cadena
  
Cuando se cambia la configuración del servidor que precede en la cadena, puede tardar un tiempo que estos cambios de configuración se hagan efectivos. Por ejemplo, si cambia una configuración en el servidor que precede en la cadena como la selección de un nuevo idioma, e inmediatamente desencadena una sincronización en el servidor que sigue en la cadena, el cambio no aparecerá. En su lugar, se enviará al servidor que sigue en la cadena en la próxima sincronización programada. El tiempo de espera aumenta dependiendo del número de actualizaciones que se encuentren en el servidor que precede en la cadena.
  
#### al desinstalar WSUS 3.0 no se desinstala la instancia de base de datos
  
Si se desinstala WSUS 3.0, no se desinstalará la instancia de base de datos. Ésta puede estar compartida por más de una aplicación, por lo que si se quita provocaría errores en otras aplicaciones.
  
Si es necesario desinstalar Windows Internal Database, los comandos siguientes instalarán la aplicación:
  
(en plataformas de 32 bits)
  
```  
msiexec /x {CEB5780F-1A70-44A9-850F-DE6C4F6AA8FB} callerid=ocsetup.exe  
```  
(en plataformas de 64 bits)
  
```  
msiexec /x {BDD79957-5801-4A2D-B09E-852E7FA64D01} callerid=ocsetup.exe  
```  
Si desea desinstalar Windows Internal Database Service Pack 2 desde Windows Server 2008, puede hacerlo por medio del Administrador del servidor.
  
Sin embargo, al quitar la aplicación puede que no se quiten los archivos .mdf y .ldf predeterminados, lo que provocará un error posterior en la instalación de WSUS 3.0. Estos archivos se pueden eliminar desde el directorio %windir%\\SYSMSI\\SSEE.
  
#### si un servidor que sigue en la cadena cambia su servidor que precede en la cadena, las actualizaciones de estado "Desconocido" se notifican como "No aplicable"
  
Si un servidor que sigue en la cadena comienza a sincronizar desde un servidor que precede en la cadena diferente, las actualizaciones que tengan el estado "Desconocido" se notificarán en el nuevo servidor que precede en la cadena como "No aplicable". Este estado es temporal y se corregirá la próxima vez que el servidor que sigue en la cadena informe de su estado, una vez que sus clientes se hayan sincronizado con él.
  
#### si un servidor de réplica de WSUS 3.0 administra más de un equipo con el mismo nombre, el paquete acumulativo de informes no se realizará correctamente
  
Si un servidor de réplica de WSUS 3.0 administra más de un equipo con el mismo nombre, el paquete acumulativo de informes no se realizará correctamente. Como resultado, los informes disponibles para el servidor WSUS raíz estarán incompletos. Este problema se resuelve eliminando todas las entradas de equipo duplicadas en el servidor de réplica.
  
#### si el Asistente para la limpieza del servidor alcanza el límite de tiempo en un servidor cuando se ejecutan varios servidores desde una consola remota, la conexión a todos los servidores se perderá
  
Es posible ejecutar el Asistente para la limpieza del servidor en varios servidores desde una única consola remota. Sin embargo, si el proceso de limpieza alcanza el límite de tiempo en uno de los servidores, la consola perderá su conexión a todos los servidores. No se perderá ningún dato, pero el administrador necesitará reiniciar la conexión remota a cada uno de los servidores.
  
#### el Asistente para la limpieza del servidor elimina archivos pasados treinta días, no tres meses
  
En el Asistente para la limpieza del servidor aparece un texto inexacto. Es el siguiente: "Elimine las actualizaciones que hayan caducado y que no se hayan aprobado en tres meses, y elimine las revisiones de actualizaciones antiguas que no se hayan aprobado en tres meses." El plazo de tiempo correcto es treinta días, y no tres meses.
  
#### iniciar y detener la conexión sucesiva y rápidamente causa un mensaje de error "sin error" del Asistente para la configuración
  
Al configurar WSUS, se le solicita que se conecte al servidor que precede en la cadena (bien Microsoft Update, o bien el servidor que precede en la cadena de la intranet) para transferir información básica acerca del servidor. Al hacer clic en **Iniciar conexión** e, inmediatamente, en **Detener conexión**; recibirá el mensaje de error incorrecto “No hubo errores de sincronización.”
  
#### los clientes WSUS que usan la versión de lanzamiento de Windows Vista ahora pueden buscar actualizaciones en Microsoft Update
  
En versiones anteriores de WSUS, los clientes que usaban la versión de lanzamiento de Windows Vista podían conseguir las actualizaciones solamente desde el servidor WSUS. Con la versión de lanzamiento de WSUS 3.0, los clientes de Vista ahora también pueden obtener las actualizaciones de Microsoft Updates. Puede indicar Microsoft Update a los clientes de Vista abriendo Windows Update desde el Panel de control y haciendo clic en el hipervínculo **Compruebe las actualizaciones en línea desde el servicio Microsoft Update**. Si está habilitada la opción **Quitar el acceso a todas las características de Windows Update** de Directiva de grupo, Windows Update no mostrará el hipervínculo.
  
WSUS 3.0 en Windows Server 2008  
-------------------------------
  
#### Versiones compatibles
  
WSUS 3.0 es compatible con Windows Server 2008 tanto en la versión de 32 bits como en la de 64 bits.
  
#### Requisitos previos
  
###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Requisito</th>
<th>Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Servicios de Microsoft Internet Information Server (IIS)</p></td>
<td style="border:1px solid black;"><p>Instalación desde el sistema operativo. Asegúrese de que los siguientes componentes están habilitados:</p>
<p>Autenticación de Windows</p>
<p>Contenido estático</p>
<p>ASP.NET</p>
<p>Compatibilidad con la administración 6.0</p>
<p>Compatibilidad con la metabase IIS</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Microsoft .NET Framework 2.0 Redistributable Package (x86)</p></td>
<td style="border:1px solid black;"><p>No es necesario en Windows Server 2008; ya está instalado como parte del sistema operativo.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Microsoft Management Console 3.0</p></td>
<td style="border:1px solid black;"><p>No es necesario en Windows Server 2008; ya está instalado como parte del sistema operativo.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Microsoft Report Viewer</p></td>
<td style="border:1px solid black;"><p>Este es un requisito previo para usar la interfaz de usuario de WSUS. Vea Microsoft Report Viewer Redistributable 2005 en el <a href="http://go.microsoft.com/fwlink/?linkid=70410">Centro de descarga de Microsoft</a> (http://go.microsoft.com/fwlink/?LinkId=70410).</p></td>
</tr>
</tbody>
</table>
  
#### Problema 1: el archivo de configuración de IIS 7.0 debe estar actualizado antes de ejecutar WSUS 3.0
  
Antes de ejecutar WSUS 3.0 en Windows Server 2008, el archivo de configuración de IIS debe estar actualizado. Deberá realizar los pasos siguientes:
  
1. Abra el archivo de configuración de IIS: %WINDIR%\\system32\\inetsrv\\applicationhost.config
  
2. En la etiqueta &lt;System.webServer&gt;&lt;modules&gt;, quite &lt;add name="CustomErrorMode"&gt;, en el caso de que exista.
  
3. En la etiqueta &lt;System.webServer&gt;&lt;modules&gt;, agregue &lt;remove name="CustomErrorMode"&gt;.
  
El resultado debería ser:
  
```  
 &lt;System.webServer&gt; &lt;modules&gt; &lt;remove name="CustomErrorMode"&gt; &lt;/modules&gt; &lt;/System.webServer&gt;  
```
  
#### Problema 2: Si desea instalar WSUS 3.0 en el puerto personalizado en Windows Server 2008 Beta 3, debe crear previamente el sitio web
  
Si piensa instalar WSUS 3.0 en Windows Server 2008 Beta 3 y desea configurar WSUS para usar el puerto personalizado 8530, deberá crear un sitio web denominado "Administración de WSUS" en el puerto 8530 antes de iniciar el programa de instalación de WSUS.
  
WSUS 3.0 en Windows Small Business Server 2003  
----------------------------------------------
  
#### Problema 1: si la raíz virtual de IIS está restringida a determinadas direcciones IP o nombres de dominio, el servidor WSUS 3.0 no podrá actualizarse a sí mismo
  
Algunas instalaciones de Windows Small Business Server pueden tener el sitio Web de IIS configurado para "Restricciones de nombre de dominio y dirección IP". En este caso, es posible que el cliente de Windows Update del servidor no pueda actualizarse a sí mismo.
  
#### Problema 2: instalación de WSUS 3.0 en Small Business Server. Problemas de integración
  
-   Si Windows Small Business Server 2003 utiliza un servidor proxy ISA para tener acceso a Internet, tiene que escribir lo siguiente en la interfaz de usuario de **Configuración**: configuración del servidor proxy, nombre del servidor proxy y puerto.  
-   Si ISA utiliza autenticación de Windows, las credenciales del servidor proxy se deben escribir en el formulario "DOMAIN\\user" y el usuario debe ser un miembro del grupo de usuarios de Internet.
  
#### Problema 3: si ha agregado una subred a su red sin usar los asistentes de Windows SBS, tiene que realizar este procedimiento
  
El proceso de instalación del servidor WSUS instala dos raíces virtuales de IIS en el servidor: SelfUpdate y ClientWebService. El programa de instalación coloca también algunos archivos bajo el directorio principal del sitio Web predeterminado (en el puerto 80) que permite a los equipos cliente actualizarse a sí mismos a través del sitio Web predeterminado. De forma predeterminada, el sitio Web predeterminado se configura para denegar el acceso a cualquier dirección IP que no sea el host local o subredes específicas vinculadas al servidor. Como resultado, los equipos cliente que no están en el host local o en esas subredes específicas no se pueden actualizar a sí mismos. Si ha agregado una subred a su red sin usar los asistentes de Microsoft Windows Small Business Server 2003 (Windows SBS), tiene que realizar este procedimiento.
  
1.  En Administración de servidores, expanda **Administración avanzada**, expanda **Internet Information Server**, expanda **Sitios Web**, expanda **Sitio Web predeterminado**, haga clic con el botón secundario en el directorio virtual **Selfupdate** y, a continuación, haga clic en **Propiedades**.  
2.  Haga clic en **Seguridad de directorios**.  
3.  Bajo **Restricciones de nombre de dominio y dirección IP**, haga clic en **Editar** y, a continuación, en **Concederá el acceso**.  
4.  Haga clic en **Aceptar**, clic con el botón secundario en el directorio virtual **ClientWebService** y, a continuación, clic en **Propiedades**.  
5.  Haga clic en **Seguridad de directorios**.  
6.  Bajo **Restricciones de nombre de dominio y dirección IP**, haga clic en **Editar** y, a continuación, en **Concederá el acceso**.
  
#### Copyright
  
Este documento es válido para una versión preliminar de un producto de software que se puede cambiar sustancialmente antes de la versión comercial final, y es información confidencial y propiedad de Microsoft Corporation. Se divulga de acuerdo con un contrato de confidencialidad entre el destinatario y Microsoft. Este documento se proporciona con fines informativos únicamente y Microsoft no otorga ninguna garantía, ya sean expresas o implícitas, en este documento. La información contenida en este documento, incluidas las direcciones URL y otras referencias a sitios Web de Internet, está sujeta a modificaciones sin previo aviso. El usuario asume todo el riesgo derivado del uso o de los resultados de la utilización de este documento. A menos que se especifique lo contrario, las compañías, organizaciones, productos, nombres de dominio, direcciones de correo electrónico, logotipos, personas, lugares y acontecimientos de ejemplo mencionados son ficticios. No se pretende ni se debe inferir de ningún modo relación con ninguna compañía, organización, producto, nombre de dominio, dirección de correo electrónico, logotipo, persona, lugar o acontecimiento reales. Es responsabilidad del usuario el cumplimiento de todas las leyes de derechos de autor u otros derechos de propiedad industrial o intelectual aplicables. Ninguna parte de este documento puede ser reproducida, almacenada o introducida en un sistema de recuperación, o transmitida de ninguna forma, ni por ningún medio (ya sea electrónico, mecánico, por fotocopia, grabación o de otra manera) con ningún propósito, sin la previa autorización por escrito de Microsoft Corporation, sin que ello suponga ninguna limitación a los derechos de propiedad industrial o intelectual.
  
Microsoft puede ser titular de patentes, solicitudes de patentes, marcas, derechos de autor, u otros derechos de propiedad industrial o intelectual sobre los contenidos de este documento. La entrega de este documento no le otorga a usted ninguna licencia sobre dichas patentes, marcas, derechos de autor, u otros derechos de propiedad industrial o intelectual, a menos que ello se prevea en un contrato escrito de licencia de Microsoft.
  
© 2007 Microsoft Corporation. Reservados todos los derechos.
  
Microsoft, SQL Server, Windows y Windows Server son marcas registradas o marcas comerciales de Microsoft Corporation en EE.UU. y en otros países.
  
Todas las restantes marcas comerciales son propiedad de sus respectivos propietarios.
