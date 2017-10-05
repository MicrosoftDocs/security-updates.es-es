---
TOCTitle: 'Notas de la versión de Windows Server Update Services 3.0 SP2'
Title: 'Notas de la versión de Windows Server Update Services 3.0 SP2'
ms:assetid: 'b3723422-489d-47b7-abfa-663353647da0'
ms:contentKeyID: 21741388
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd939886(v=WS.10)'
---

Notas de la versión de Windows Server Update Services 3.0 SP2
=============================================================

Estas notas de la versión describen la versión Windows Server Update Services 3.0 Service Pack 2 (WSUS 3.0 SP2). Este documento contiene las siguientes secciones:

1.  Novedades de la versión
2.  Requisitos del sistema para la instalación de WSUS 3.0 SP2 Server
3.  Requisitos previos de configuración y recomendaciones para WSUS Server
4.  Requisitos previos de Windows Small Business Server
5.  Requisitos del sistema para la instalación de la consola remota de WSUS 3.0 SP2
6.  Requisitos del sistema para la instalación del cliente
7.  Requisitos y recomendaciones de actualización
8.  Instalación de WSUS 3.0 SP2
9.  Parámetros de línea de comandos del programa de instalación para instalaciones de WSUS 3.0 SP2
10. Problemas conocidos

Novedades de la versión
-----------------------

-   Integración con Windows Server 2008 R2.
-   Compatibilidad con la característica BranchCache en Windows Server 2008 R2
-   Compatibilidad con los clientes de Windows 7.
-   Mejoras del cliente Agente de Windows Update (WUA). El nuevo cliente WUA ofrece un grupo de mejoras relacionadas con el rendimiento y la experiencia del usuario, además de una selección de correcciones de errores basada en los comentarios de los clientes.
    -   El tiempo de detección del cliente es más rápido que en las versiones anteriores.
    -   Los equipos gestionados por servidores WSUS ahora pueden ejecutar análisis "de ámbito" en los mismos servidores de WSUS, en lugar de realizar un análisis completo. Como consecuencia, los análisis serán más rápidos y se ordenarán según la magnitud de las aplicaciones que utilicen las API de Microsoft Update como, por ejemplo, Windows Defender.
    -   Las mejoras en la experiencia del usuario del Agente de Windows Update (WUA) ayudan a los usuarios a organizar mejor las actualizaciones y proporcionan mayor claridad en el valor y comportamiento de las mismas.
    -   Los equipos digitalizados se mostrarán con mayor claridad en la consola de WSUS. Para obtener más información, consulte el artículo titulado [Un equipo basado en Windows 2000, Windows Server 2003 o Windows XP configurado mediante una imagen de Windows 2000, Windows Server 2003 o Windows XP no aparece en la consola de WSUS](http://go.microsoft.com/fwlink/?linkid=159749).
-   Características nuevas:
    -   Ahora, las reglas de aprobación automática incluyen la posibilidad de especificar la fecha y hora límite de aprobación para todos los equipos o para grupos de equipos determinados.
    -   La administración mejorada de la selección de idioma en servidores que siguen en la cadena incluye un nuevo cuadro de diálogo de advertencia que aparece cuando decide descargar actualizaciones sólo para idiomas específicos.
    -   Los nuevos informes del estado de la actualización y del equipo le permiten filtrar actualizaciones aprobadas para la instalación. Puede ejecutar estos informes desde la consola de WSUS o usar la interfaz de programación de aplicaciones (API) para incorporar esta funcionalidad en sus propios informes.
-   La interfaz de usuario es compatible entre el Service Pack 1 y el Service Pack 2 de WSUS 3.0, tanto en el cliente como en el servidor.
-   Actualizaciones de software.
-   Problemas conocidos con el Agente de Windows Update que se solucionan en esta versión:
    1.  WSUS 3.0 SP2 y Windows 7 incluyen una nueva versión del Agente de Windows Update (para Windows XP, Vista, Windows Server 2000, Windows Server 2003 y Windows Server 2008). Esta versión soluciona el problema siguiente: Se producirá un error en las API que sean llamadas por llamadores de sistemas no locales en una sesión no interactiva.
    2.  Problema solucionado por la versión 7.2.6001.788 del Agente de Windows Update. Esta actualización soluciona el problema siguiente: Al intentar instalar 80 o más actualizaciones al mismo tiempo desde la página web de Windows Update o desde la página web de Microsoft Update, es posible que reciba el código de error 0x80070057.
    3.  Mejoras y problemas solucionados con la versión 7.2.6001.784 del Agente de Windows Update. Esta actualización incluye lo siguiente: Mejora los tiempos de análisis de Windows Update, mejora la rapidez con la que se entregan las actualizaciones de firmas, ofrece soporte para la funcionalidad de reinstalación de Windows Installer y mejora los mensajes de error.

<span id="BKMK_SysReqWSUS30SP2"></span>
Requisitos del sistema para la instalación de WSUS 3.0 SP2 Server
-----------------------------------------------------------------

En esta sección se describen los requisitos de software y hardware necesarios para la instalación de WSUS 3.0 SP2.

### Requisitos previos de software de WSUS Server

-   Debe tener instalado uno de los siguientes sistemas operativos compatibles:
    -   Windows Server 2008 R2
    -   Windows Server 2008 SP1 o versiones posteriores
 
        <table style="border:1px solid black;">
        <colgroup>
        <col width="100%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th style="border:1px solid black;" ><img src="images/Dd939886.Warning(WS.10).gif" />Advertencia</th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td style="border:1px solid black;">Si WSUS 3.0 SP2 se instala en Windows Server 2008 antes de actualizar a Windows Server 2008 R2, la actualización a Windows Server 2008 R2 no se realizará correctamente. Consulte la sección <a href="#bkmk_knownissues">Problemas conocidos</a> para obtener más información.
        </td>
        </tr>
        </tbody>
        </table>
 

    -   Windows Server 2003 SP1 o versiones posteriores
    -   Windows Small Business Server 2008
    -   Windows Small Business Server 2003

    Tenga en cuenta que en el caso de Windows Small Business Server se aplican requisitos previos adicionales. Para obtener más información, consulte la sección “Requisitos previos de Windows Small Business Server”.
-   Internet Information Services (IIS) 6.0 o versiones posteriores
-   Microsoft .NET Framework 2.0 o versiones posteriores
-   Debe tener instalada una de las siguientes bases de datos compatibles:
    -   Microsoft SQL Server 2008 Standard o Enterprise Edition
    -   Microsoft SQL Server 2005 SP3 o versiones posteriores
    -   Windows Internal Database

    Si no hay instalada ninguna de las versiones compatibles de SQL Server, el asistente para instalación de WSUS 3.0 SP2 instalará Windows Internal Database.
-   Microsoft Management Console 3.0
-   Microsoft Report Viewer 2008 redistribuible

 
<table style="border:1px solid black;">
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" ><img src="images/Dd939886.Important(WS.10).gif" />Importante</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Windows Server 2008 R2 requiere WSUS 3.0 SP2. Si instala Windows Server 2008 R2, a continuación debe instalar WSUS 3.0 SP2. No instale WSUS 3.0 SP1 en Windows Server 2008 R2.

WSUS 3.0 SP2 no es compatible con Terminal Services en el servidor front-end en una configuración de SQL remota.
</td>
</tr>
</tbody>
</table>
 

### Requisitos previos de software de la consola de administración de WSUS

-   Uno de los siguientes sistemas operativos compatibles: Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 SP2 o versiones posteriores, Windows Small Business Server 2008 ó 2003, Windows Vista o Windows XP SP2
-   Microsoft .NET Framework 2.0 o versiones posteriores
-   Microsoft Management Console 3.0
-   Microsoft Report Viewer 2008 redistribuible

### Requisitos mínimos de hardware del servidor WSUS

La siguiente lista contiene los requisitos mínimos de hardware necesarios para una instalación del servidor básica. Consulte la Guía de implementación de WSUS 3.0 SP2 en [http://go.microsoft.com/fwlink/?LinkId=139832](http://go.microsoft.com/fwlink/?linkid=139832) donde encontrará una lista completa de las configuraciones de hardware admitidas.

-   Tanto la partición del sistema como la partición en la que se instala WSUS 3.0 SP2 deben estar formateadas con el sistema de archivos NTFS.
-   Mínimo 1 GB de espacio libre en la partición del sistema
-   Mínimo 2 GB de espacio libre en el volumen en el que se van a almacenar los archivos de la base de datos.
-   Es necesario disponer de un mínimo 20 GB de espacio libre en el volumen en el que se almacena el contenido. Se recomienda disponer de 30 GB.

 
<table style="border:1px solid black;">
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" ><img src="images/Dd939886.Important(WS.10).gif" />Importante</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">No se puede instalar WSUS 3.0 SP2 en unidades comprimidas.
</td>
</tr>
</tbody>
</table>
 

Requisitos previos de configuración y recomendaciones para WSUS Server
----------------------------------------------------------------------

Asegúrese de completar las tareas correspondientes en esta sección antes de instalar WSUS 3.0 SP2.

### IIS

-   En la página Servicios de función de Server Manager Web Server (IIS), instale todas las características necesarias y todos los servicios de función IIS, así como los siguientes: **ASP.NET**, **Autenticación de Windows**, **Compresión de contenido dinámico** y **Compatibilidad con la administración de IIS 6**.
-   Si IIS se ejecuta en el modo de aislamiento de IIS 5.0, se producirá un error en la instalación. Deshabilite el modo de aislamiento de IIS 5.0 antes de instalar WSUS 3.0 SP2.
-   Si cualquier componente de IIS se instala en modo compatible de 32 bits en una plataforma de 64 bits, se pueden producir errores en la instalación de WSUS 3.0 SP2. Todos los componentes de IIS deben instalarse en modo nativo en plataformas de 64 bits.

### Servidores proxy

WSUS 3.0 SP2 permite que un servidor proxy admita HTTP únicamente. Se recomienda configurar un segundo servidor proxy que ejecute HTTPS mediante la línea de comandos (**wsusutil configuresslproxy**) antes de configurar el servidor WSUS en el Asistente para la configuración o la Consola de administración.

### Sitios web que se ejecutan en el puerto 80

Si tiene dos o más sitios web que se ejecutan en el puerto 80 (por ejemplo, Windows SharePoint Services), elimine todos menos uno antes de instalar WSUS. De no hacerlo, es posible que se produzca un error en los clientes del servidor al actualizarse automáticamente.

### Programas antivirus

Al instalar WSUS 3.0 SP2, puede que tenga que deshabilitar programas antivirus para poder realizar la instalación correctamente. Después de deshabilitar el software antivirus, reinicie el equipo antes de instalar WSUS. Al reiniciar el equipo se evita que los archivos estén bloqueados cuando el proceso de instalación necesite tener acceso a ellos. Una vez que se complete la instalación, asegúrese de volver a habilitar el software antivirus. Visite el sitio web del proveedor de software antivirus con el fin de seguir el procedimiento exacto para deshabilitar y volver a habilitar el software y la versión antivirus.

 
<table style="border:1px solid black;">
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" ><img src="images/Dd939886.Caution(WS.10).gif" />Precaución</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Esta solución alternativa puede hacer que su equipo o la red sean más vulnerables a los ataques de usuarios malintencionados o por software dañino como los virus. No se recomienda esta solución alternativa pero le facilitamos esta información para que pueda implementarla según su criterio. Usted asume todo el riesgo derivado del uso de esta solución.

El software antivirus ayuda a proteger su equipo de los virus. No descargue ni abra archivos de orígenes que no sean de confianza, visitar sitios Web en los que no confíe ni abrir adjuntos de correo electrónico cuando su programa antivirus esté deshabilitado.
</td>
</tr>
</tbody>
</table>
 

### Opción de desencadenadores anidados en SQL Server

Si tiene previsto utilizar una base de datos de SQL Server como almacén de datos de Windows Server Update Services, el administrador de SQL Server deberá comprobar que la opción de desencadenadores anidados esté activada antes de que el administrador de WSUS instale WSUS 3.0 SP2. La opción de desencadenadores anidados está activada de manera predeterminada; sin embargo, un administrador de SQL Server puede desactivarla. El programa de instalación de WSUS 3.0 SP2 activa la opción RECURSIVE\_TRIGGERS, que es una opción específica de la base de datos. Sin embargo, el programa de instalación de WSUS 3.0 SP2 no activa la opción de desencadenadores anidados, que es una opción global del servidor.

### Limitaciones y requisitos de SQL remoto

WSUS 3.0 SP2 admite la ejecución de una versión compatible del software de SQL Server en un equipo independiente del equipo en el que se esté ejecutando la aplicación WSUS 3.0 SP2. Los requisitos siguientes se aplican a una instalación de SQL remota.

-   No se puede usar un servidor configurado como controlador de dominio para el back-end del par SQL remoto.
-   No es posible ejecutar Terminal Services en el equipo que vaya a ser el servidor front-end de una instalación de SQL remota.
-   Tanto los equipos front-end como los back-end deben unirse a un dominio de Active Directory. Si los equipos front-end y back-end se encuentran en dominios distintos, establezca una relación de confianza entre los dominios antes de ejecutar el programa de instalación de WSUS.
-   Si WSUS 2.0 ya se encuentra instalado en una configuración de SQL remota y desea actualizar a WSUS 3.0 SP2, antes de instalar WSUS haga lo siguiente:
    1.  Desinstale WSUS 2.0 (mediante **Agregar o quitar programas** en el Panel de control) asegurándose de que la base de datos existente permanece intacta.
    2.  Instale SQL Server 2005 SP2 o SQL Server 2008 y actualice la base de datos existente.

### IIS se reiniciará durante la instalación de WSUS 3.0 SP2

El programa de instalación de WSUS 3.0 SP2 reiniciará IIS sin notificación, lo que puede afectar a los sitios web existentes de su organización. Se recomienda notificar a las partes afectadas antes de realizar la instalación. Tenga en cuenta que si IIS no se está ejecutando, el programa de instalación de WSUS 3.0 SP2 iniciará IIS durante la instalación.

Requisitos previos de Windows Small Business Server
---------------------------------------------------

Si instala WSUS 3.0 SP2 en Windows Small Business Server, se aplicarán los siguientes requisitos previos.

### Si la raíz virtual de IIS está restringida a determinadas direcciones IP o nombres de dominio

Algunas instalaciones de Windows Small Business Server pueden tener el sitio Web de IIS configurado para **Restricciones de nombre de dominio y dirección IP**. En tal caso, es posible que el cliente de Windows Update del servidor no pueda actualizarse por sí mismo. Quite la restricción antes de instalar WSUS 3.0 SP2.

### Si usa un servidor proxy ISA

-   Si Windows Small Business Server utiliza un servidor proxy ISA para obtener acceso a Internet, escriba **la configuración del servidor proxy, el nombre del servidor proxy y el puerto** en la interfaz de usuario **Configuración**.
-   Si ISA utiliza autenticación de Windows, escriba las credenciales del servidor proxy en el formulario *DOMAIN*\\*user*. El usuario debe ser miembro del grupo de usuarios de Internet.

### Si ha agregado una subred a su red sin usar los asistentes de Microsoft Windows Small Business Server

El proceso de instalación del servidor WSUS instala dos raíces virtuales de IIS en el servidor: SelfUpdate y ClientWebService. El programa de instalación coloca también algunos archivos bajo el directorio raíz del sitio web predeterminado (en el puerto 80) que permite a los equipos cliente actualizarse a sí mismos a través del sitio web predeterminado. De forma predeterminada, el sitio Web predeterminado se configura para denegar el acceso a cualquier dirección IP que no sea el host local o subredes específicas vinculadas al servidor. Por lo tanto, los equipos cliente que no están en el host local o en esas subredes específicas no se pueden actualizar a sí mismos. Si ha agregado una subred a la red sin usar los asistentes de Microsoft Windows Small Business Server, siga este procedimiento:

1.  En Administración de servidores, expanda **Administración avanzada**, expanda **Internet Information Server**, expanda **Sitios Web**, expanda **Sitio Web predeterminado**, haga clic con el botón secundario en el directorio virtual **Selfupdate** y, a continuación, haga clic en **Propiedades**.
2.  Haga clic en **Seguridad de directorios**.
3.  Bajo **Restricciones de nombre de dominio y dirección IP**, haga clic en **Editar** y, a continuación, en **Concederá el acceso**.
4.  Haga clic en **Aceptar**, clic con el botón secundario en el directorio virtual **ClientWebService** y, a continuación, clic en **Propiedades**.
5.  Haga clic en **Seguridad de directorios**.
6.  Bajo **Restricciones de nombre de dominio y dirección IP**, haga clic en **Editar** y, a continuación, en **Concederá el acceso**.

Requisitos del sistema para la instalación de la consola remota de WSUS 3.0 SP2
-------------------------------------------------------------------------------

La consola remota de WSUS 3.0 SP2 se puede instalar en cualquiera de los sistemas operativos siguientes:

-   Windows Server 2008 R2, Windows Server 2008 SP1 o versiones posteriores, Windows Server 2003 SP2 o versiones posteriores, Windows Small Business Server 2003, 2005 ó 2008, Windows Vista o Windows XP Professional SP2 o versiones posteriores.

Requisitos del sistema para la instalación del cliente de WSUS
--------------------------------------------------------------

Las actualizaciones automáticas, el software del cliente de WSUS, se pueden instalar en cualquiera de los siguientes sistemas operativos:

-   Windows Server 2008 R2, Windows Server 2008 SP1 o versiones posteriores, Windows Server 2003 SP2 o versiones posteriores, Windows Small Business Server 2003, 2005 ó 2008, Windows Vista, Windows XP Professional RTM, Windows XP Professional SP1, SP2, SP3 o versiones posteriores, Windows 2000 SP4 o cliente de Windows 7.

Requisitos y recomendaciones de actualización
---------------------------------------------

Las siguientes versiones de WSUS se pueden actualizar a WSUS 3.0 SP2 y no requieren la desinstalación de la versión anterior:

-   WSUS 2.0, 2.0 SP1, 3.0 y 3.0 SP1.

No se admiten actualizaciones de WSUS 1.0 a WSUS 3.0 SP2. Antes de instalar WSUS 3.0 SP2, desinstale Servicios de actualización de software (SUS) 1.0.

Windows Server 2008 R2 requiere WSUS 3.0 SP2. Si instala Windows Server 2008 R2, a continuación debe instalar WSUS 3.0 SP2. No instale WSUS 3.0 SP1 en Windows Server 2008 R2.

#### Antes de actualizar a WSUS 3.0 SP2

1.  Compruebe si hay versiones recientes en los registros de eventos, problemas con la sincronización entre servidores que siguen en la cadena y servidores que preceden en la cadena, así como problemas con los informes del cliente. Solucione estos problemas antes de actualizar.

2.  Opcionalmente, puede ejecutar DBCC CHECKDB para garantizar que la base de datos de WSUS se indiza correctamente. Para obtener más información acerca de DBCC CHECKDB, consulte [DBCC CHECKDB](http://go.microsoft.com/fwlink/?linkid=86948).

3.  Realice una copia de seguridad de la base de datos de WSUS. Tenga en cuenta que el programa de instalación de WSUS 3.0 SP2 agregará la nueva base de datos al directorio predeterminado, que es *unidad*\\WSUS (*unidad* es la unidad NTFS local con mayor cantidad de espacio libre). Si ya existe una copia de seguridad de la base de datos en este directorio, es posible que se sobrescriba. Se recomienda guardar una copia de seguridad de la base de datos de la versión actual de WSUS en una ubicación distinta antes de actualizar a WSUS 3.0 SP2.

4.  Si ha cambiado manualmente el puerto que utiliza WSUS (es decir, no ha usado la utilidad Wsusutil) y está ejecutando actualmente SUS 1.0 o WSUS 2.0, inicie el sitio web predeterminado antes de desinstalar SUS 1.0 o WSUS 2.0 de 64 bits.

5.  Es posible que la instalación no se realice correctamente si hay conexiones abiertas a una base de datos de WSUS existente (por ejemplo, si SQL Server Management Studio está abierto). Cierre todas las conexiones antes de instalar WSUS 3.0 SP2.

### Recuperación de una actualización realizada con errores

Si está actualizando desde una versión anterior de WSUS a WSUS 3.0 SP2 y se produce un error en la actualización (por cualquier motivo que no sea intentar aplicar una actualización no admitida de SUS 1.0), realice las tareas siguientes:

1.  Vuelva a instalar la versión anterior de WSUS.
2.  Restaure la base de datos de la copia de seguridad que realizó antes de intentar actualizar. No es posible completar correctamente una actualización si existe una base de datos de WSUS 3.0 SP2 de una instalación anterior. En la mayoría de los casos, WSUS también crea una copia de seguridad automáticamente. Vea el archivo WSUSSetup.log para conocer la ubicación.
3.  Revise los registros para determinar la causa del error y resolver el problema.
4.  Instale WSUS 3.0 SP2.

### Cambiar el nombre del equipo antes de actualizar a WSUS 3.0 SP2 puede causar un error en la actualización

Si cambia el nombre del equipo después de instalar WSUS 2.0 y antes de actualizar a WSUS 3,0, puede producirse un error en la actualización.

Use la siguiente secuencia de comandos para quitar y volver a agregar los grupos de administradores de ASPNET y WSUS. A continuación, ejecute de nuevo la actualización.

        ```

### Si ha realizado la migración de MSDE a SQL Server 2008 o SQL Server 2005 en WSUS 2.0, debe modificar un valor del Registro

Si tiene una instalación de WSUS 2.0 y ha migrado a SQL Server 2008 o SQL Server 2005, debe cambiar el valor **HKLM\\SOFTWARE\\Microsoft\\Update Services\\Server\\Setup\\WmsdeInstalled** de 1 a 0. De no cambiarlo antes de actualizar a WSUS 3.0 SP2, se producirá un error en la actualización.

### Si se desinstala WSUS 3.0 SP2 y se dejan los archivos de registro, éstos podrían no tener los permisos correctos después de reinstalar

Al desinstalar WSUS 3.0 SP2, tiene la opción de conservar los archivos de registro de la instalación. Al reinstalar WSUS 3.0 SP2, los archivos de registro antiguos pueden perder sus permisos (normalmente sólo para administradores de WSUS). Se recomienda confirmar los permisos en estos archivos de registro tras la instalación.

### Si los clientes de WSUS 2.0 tienen actualizaciones con el estado "No aplicable", las actualizaciones aparecerán como "Desconocido" durante un breve período de tiempo tras actualizar a WSUS 3.0 SP2

Si un servidor WSUS 2.0 existente tiene clientes con actualizaciones con el estado **No aplicable**, estas actualizaciones pueden mostrar el estado **Desconocido** durante un breve período de tiempo tras actualizar a WSUS 3.0 SP2. La próxima vez que el cliente realice un análisis, el estado de la actualización volverá a ser **No aplicable**.

Instalación de WSUS 3.0 SP2
---------------------------

La guía de instalación paso a paso de WSUS, que se encuentra en [http://go.microsoft.com/fwlink/?LinkId=139836](http://go.microsoft.com/fwlink/?linkid=139836), proporciona instrucciones para instalar WSUS 3.0 SP2 mediante Windows Server Manager o el archivo WUSSetup.exe.

Para obtener información completa acerca de la instalación y el uso de WSUS, vea:

La guía de implementación de WSUS en [http://go.microsoft.com/fwlink/?LinkId=139832](http://go.microsoft.com/fwlink/?linkid=139832).

La guía de operaciones de WSUS en [http://go.microsoft.com/fwlink/?LinkId=139838](http://go.microsoft.com/fwlink/?linkid=139838).

Parámetros de línea de comandos del programa de instalación para instalaciones de WSUS 3.0 SP2
----------------------------------------------------------------------------------------------

Puede realizar instalaciones desatendidas de WSUS 3.0 SP2 si utiliza el programa de instalación de línea de comandos de WSUS. Esta tabla muestra los parámetros de línea de comandos para el programa de instalación de WSUS 3.0 SP2.

###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Opción</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>/q</strong></td>
<td style="border:1px solid black;">Realizar instalación silenciosa.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>/u</strong></td>
<td style="border:1px solid black;">Desinstalar.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>/p</strong></td>
<td style="border:1px solid black;">Comprobar requisitos previos. Inspecciona el sistema e informa de los requisitos previos que faltan.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>/?, /h</strong></td>
<td style="border:1px solid black;">Mostrar parámetros de línea de comandos y sus descripciones.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>/g</strong></td>
<td style="border:1px solid black;">Actualizar desde la versión anterior de WSUS. (Las actualizaciones desde SUS 1.0 no se admiten). El único parámetro válido con esta opción es /q (instalación silenciosa). La única propiedad valida con esta opción es DEFAULT_WEBSITE.</td>
</tr>
</tbody>
</table>
  
Esta tabla muestra las propiedades de línea de comandos para WSUS 3.0 SP2.
  
###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Propiedad</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">CONTENT_LOCAL</td>
<td style="border:1px solid black;">0=contenido alojado localmente, 1=alojado en Microsoft Update</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">CONTENT_DIR</td>
<td style="border:1px solid black;">Ruta de acceso al directorio de contenido. La ruta predeterminada es <em>WSUSInstallationDrive\WSUS\WSUSContent</em>, donde <em>WSUSInstallationDrive</em> es la unidad local con la mayor cantidad de espacio libre.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">WYUKON_DATA_DIR</td>
<td style="border:1px solid black;">Ruta al directorio de datos de Windows Internal Database.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SQLINSTANCE_NAME</td>
<td style="border:1px solid black;">El nombre debería aparecer con el formato <em>NombreServidor</em>\<em>NombreInstanciaSQL</em>. Si la instancia de la base de datos se encuentra en el equipo local, use la variable de entorno %COMPUTERNAME%. Si no está presente una instancia existente, de forma predeterminada sería %COMPUTERNAME%\WSUS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">DEFAULT_WEBSITE</td>
<td style="border:1px solid black;">0=puerto 8530, 1=puerto 80</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">PREREQ_CHECK_LOG</td>
<td style="border:1px solid black;">Ruta de acceso y nombre de archivo del archivo de registro</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">CONSOLE_INSTALL</td>
<td style="border:1px solid black;">0=instalar el servidor WSUS, 1=instalar únicamente la consola</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ENABLE_INVENTORY</td>
<td style="border:1px solid black;">0=no instalar características de inventario, 1=instalar características de inventario</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">DELETE_DATABASE</td>
<td style="border:1px solid black;">0=mantener base de datos, 1=quitar base de datos</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">DELETE_CONTENT</td>
<td style="border:1px solid black;">0=mantener archivos de contenido, 1=quitar archivos de contenido</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">DELETE_LOGS</td>
<td style="border:1px solid black;">0=mantener archivos de registro, 1=quitar archivos de registro (se usa con el modificador de instalación /u)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">CREATE_DATABASE</td>
<td style="border:1px solid black;">0=usar base de datos actual, 1=crear base de datos</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">PROGRESS_WINDOW_HANDLE</td>
<td style="border:1px solid black;">Controlador de ventana para devolver los mensajes de progreso de Windows Installer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MU_ROLLUP</td>
<td style="border:1px solid black;">1=participar en el programa de mejora de Microsoft Update, 0=no participar en el programa de mejora de Microsoft Update</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">FRONTEND_SETUP</td>
<td style="border:1px solid black;">1=no escribir la ubicación del contenido en la base de datos, 0=escribir la ubicación del contenido en la base de datos (para NLB)</td>
</tr>
</tbody>
</table>
  
### Ejemplo de uso
  
```  
WSUSSetup.exe /q DEFAULT\_WEBSITE=0 (instalar en modo silencioso utilizando el puerto 8530) WSUSSetup.exe /q /u (desinstalar WSUS)  
```
 
<table style="border:1px solid black;">
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" ><img src="images/Dd939886.Important(WS.10).gif" />Importante</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Si instala WSUS 3.0 SP2 en modo silencioso (/q) y el equipo no tiene todos los requisitos previos instalados, la instalación generará un archivo llamado WSUSPreReqCheck.xml y lo guardará en el directorio %TEMP%.
</td>
</tr>
</tbody>
</table>
 

<span id="BKMK_KnownIssues"></span>
Problemas conocidos
-------------------

-   Una vez completado correctamente el proceso del Asistente para la instalación de WSUS, se solicitará al usuario que haga clic en **Finalizar**. Excepcionalmente, aparecerá un cuadro de diálogo de error con el siguiente mensaje: “**Se produjo un error al comunicar con el servidor y este asistente se cerrará. Tiene que reiniciar el Asistente para la configuración del servidor WSUS desde la página Opciones de la consola de WSUS**”. Para garantizar que se guardan las selecciones de instalación, abra la página **Opciones** en la consola de administración de WSUS y confirme la configuración de cada sección.
-   **Las versiones localizadas del cliente Agente de Windows Update (WUA) aparecerán con posterioridad a la versión WSUS 3.0 SP2**, ya que depende del programa de localización de Windows 7. Durante el tiempo que transcurra entre la versión WSUS 3.0 SP2 y la versión localizada del cliente WUA, éste solo admite cinco idiomas (inglés, alemán, francés, español y japonés).
-   **Los nuevos informes del estado de la actualización y del equipo que se han presentado en esta versión de SP2 no funcionan en un entorno donde los servidores WSUS 3.0 SP1 que sigan en la cadena se gestionen desde un servidor WSUS 3.0 SP2**. Si los nuevos informes se ejecutan para un servidor de SP1, aparece el siguiente mensaje de error: "Se produjo un error al generar el informe. Ejecute nuevamente el informe o póngase en contacto con su administrador de red si el problema persiste". Ejecutar el informe una vez más no solucionará el problema, que tampoco está relacionado con las redes. Los nuevos informes dependen de funciones de API que no existen en SP1; sin embargo, la consola de administración de SP2 no bloquea los informes nuevos al gestionar un servidor SP1.
-   **La actualización a WSUS 3.0 SP2 no se realiza correctamente cuando SSL se configura sin nombre del certificado**. Es necesario proporcionar un nombre del certificado para configurar SSL.
-   **WSUS 3.0 SP2 ejecutando Windows Internal Database instalado en Windows Server 2008 impide la actualización a Windows Server 2008 R2**. Antes de continuar con la actualización a Windows Server 2008 R2, aparece un mensaje de error de Informe de compatibilidad que le solicita que apague el Windows Internal Database. Es necesario actualizar Windows Internal Database antes que la actualización a Windows Server 2008 R2 pueda continuar. Consulte [Cómo obtener el último Service Pack para Windows Internal Database](http://go.microsoft.com/fwlink/?linkid=162104) (http://go.microsoft.com/fwlink/?LinkId=162104) para recibir instrucciones y más información acerca de la actualización Windows Internal Database.

Avisos de derechos de autor
---------------------------

La información contenida en este documento, incluidas las direcciones URL y otras referencias a sitios web de Internet, está sujeta a modificaciones sin previo aviso. A menos que se especifique lo contrario, las compañías, organizaciones, productos, nombres de dominio, direcciones de correo electrónico, logotipos, personas, lugares y acontecimientos de ejemplo mencionados son ficticios. No se pretende ni se debe inferir de ningún modo relación con ninguna compañía, organización, producto, nombre de dominio, dirección de correo electrónico, logotipo, persona, lugar o acontecimiento reales. Es responsabilidad del usuario el cumplimiento de todas las leyes de derechos de autor u otros derechos de propiedad industrial o intelectual aplicables. Ninguna parte de este documento puede ser reproducida, almacenada o introducida en un sistema de recuperación, o transmitida de ninguna forma, ni por ningún medio (ya sea electrónico, mecánico, por fotocopia, grabación o de otra manera) con ningún propósito, sin la previa autorización por escrito de Microsoft Corporation, sin que ello suponga ninguna limitación a los derechos de propiedad industrial o intelectual.

Microsoft puede ser titular de patentes, solicitudes de patentes, marcas, derechos de autor, u otros derechos de propiedad industrial o intelectual sobre los contenidos de este documento. La entrega de este documento no le otorga ninguna licencia sobre dichas patentes, marcas, derechos de autor u otros derechos de propiedad industrial o intelectual, a menos que ello se prevea en un contrato escrito de licencia de Microsoft.

© 2009 Microsoft Corporation. Reservados todos los derechos.

Microsoft, Active Directory, ActiveX, Authenticode, Excel, InfoPath, Internet Explorer, MSDN, Outlook, Visual Studio, Win32, Windows, Windows Server y Windows Vista son marcas comerciales del grupo de empresas de Microsoft.

Todas las restantes marcas comerciales son propiedad de sus respectivos propietarios.
