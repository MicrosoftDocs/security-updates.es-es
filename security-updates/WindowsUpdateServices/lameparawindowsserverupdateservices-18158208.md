---
TOCTitle: Léame para Windows Server Update Services
Title: Léame para Windows Server Update Services
ms:assetid: '4244109a-395a-4ff8-9989-ea55ab0964a3'
ms:contentKeyID: 18158208
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720505(v=WS.10)'
---

Léame para Windows Server Update Services
=========================================

Este documento describe problemas conocidos que afectan a Windows Server Update Services (WSUS). Incluye recomendaciones y requisitos para instalar WSUS.

| ![](images/Cc720505.note(WS.10).gif)Nota                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Puede descargar una copia de este documento en el Centro de descarga de Microsoft [http://go.microsoft.com/fwlink/?LinkId=48126](http://go.microsoft.com/fwlink/?linkid=48126). |

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
<th style="border:1px solid black;" >Sistema operativo</th>
<th style="border:1px solid black;" >Requisitos</th>
<th style="border:1px solid black;" >Descargas</th>
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
<td style="border:1px solid black;">Para sistemas operativos Windows Server 2003, vea <a href="http://go.microsoft.com/fwlink/?linkid=47251">Actualización del Servicio de transferencia inteligente en segundo plano (BITS) 2.0 y WinHTTP 5.1 Windows Server 2003</a> (KB842773) en el Centro de descarga (http://go.microsoft.com/fwlink/?LinkId=47251).
Para sistemas operativos Windows Server 2000, vea <a href="http://go.microsoft.com/fwlink/?linkid=46794">Actualización del Servicio de transferencia inteligente en segundo plano (BITS) 2.0 y WinHTTP 5.1 Windows 2000</a> (KB842773) en el Centro de descarga de Microsoft (http://go.microsoft.com/fwlink/?LinkId=46794).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Server 2003</td>
<td style="border:1px solid black;">Microsoft .NET Framework 1.1 Service Pack 1 para Windows Server 2003</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=47358">Microsoft .NET Framework 1.1 Service Pack 1 para Windows Server 2003</a>
Como alternativa, vaya a <a href="http://go.microsoft.com/fwlink/?linkid=47370">Windows Update</a> y busque actualizaciones críticas y Service Packs; instale Microsoft .NET Framework 1.1 Service Pack 1 para Windows Server 2003.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows Server 2003</td>
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=47359">Internet Explorer 6 Service Pack 1</a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows 2000 Server</td>
<td style="border:1px solid black;">Paquete redistribuible de Microsoft .NET Framework versión 1.1</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=47369">Paquete redistribuible de Microsoft .NET Framework versión 1.1</a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows 2000 Server</td>
<td style="border:1px solid black;">Microsoft .NET Framework 1.1 Service Pack 1</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=47368">Microsoft .NET Framework 1.1 Service Pack 1</a>
Como alternativa, vaya a <a href="http://go.microsoft.com/fwlink/?linkid=47370">Windows Update</a> y busque actualizaciones críticas y Service Packs; instale Microsoft .NET Framework 1.1 Service Pack 1 para Windows Server 2000.</td>
</tr>
</tbody>
</table>
 

Además de estos requisitos, WSUS puede instalar o configurar ASP.NET versión 1.1 en el servidor, si es necesario. (El programa de instalación de WSUS configura ASP.NET.)

#### Instalación de MSDE 2000 en Windows 2000

Si usa Windows 2000 para WSUS y no tiene acceso a Microsoft SQL Server 2000, debe instalar Microsoft SQL Server 2000 Desktop Engine (MSDE) antes de ejecutar el programa de instalación de WSUS. Si ya tiene instalado MSDE en el servidor WSUS, no tiene que instalar una versión especial del mismo para WSUS. Puede simplemente indicar el nombre de la instancia existente durante el proceso de instalación de WSUS.

La instalación de MSDE en Windows 2000 Server es un proceso de cuatro pasos. Primero, debe descargar y expandir el archivo de MSDE en una carpeta del servidor WSUS. Después, use un símbolo del sistema y opciones de la línea de comandos para ejecutar el programa de instalación de MSDE, definir la contraseña del administrador del sistema y asignar WSUS como nombre de instancia. A continuación, una vez terminada la instalación de MSDE, debe comprobar que la instancia de WSUS se ejecuta como servicio de NT. Finalmente, debe agregar una actualización de seguridad a MSDE para proteger su servidor WSUS.

#### Paso 1: descargar y expandir el archivo de MSDE

Debe descargar y expandir el archivo de MSDE en una carpeta del servidor WSUS. Consulte [Microsoft SQL Server 2000 Desktop Engine (MSDE 2000) Release A](http://go.microsoft.com/fwlink/?linkid=47366).

#### Paso 2: instalar MSDE

Use un símbolo del sistema y opciones de la línea de comandos para ejecutar el programa de instalación de MSDE, definir la contraseña del administrador del sistema y asignar WSUS como nombre de instancia. Una vez terminada la instalación de MSDE, debe comprobar que la instancia de WSUS se ejecuta como servicio de NT.

Para instalar MSDE, defina la contraseña del administrador del sistema y asigne un nombre de instancia:

1.  En el símbolo del sistema, navegue a la carpeta de instalación de MSDE especificada en “Paso 1: Descargar y expandir el archivo de MSDE”.
2.  Escriba lo siguiente: **setup sapwd="***contraseña***" instancename=WSUS**
    donde *contraseña* es una contraseña segura para la cuenta del administrador del sistema de esta instancia de MSDE e **instancename** es el nombre de la instancia de base de datos. Como alternativa, puede usar el nombre de instancia predeterminado (en lugar de "WSUS") para la base de datos de WSUS. Si decide hacer esto, no tiene que escribir **instancename=WSUS** en el parámetro de la línea de comandos. Este comando inicia el programa de instalación de MSDE, define la contraseña del administrador del sistema y asigna el valor especificado como nombre para esta instancia de MSDE.

#### Paso 3: comprobar que la instancia de WSUS de MSDE está instalada

Debe asegurarse de que puede ver la instancia de WSUS de MSDE.

1.  Haga clic en **Inicio** y, a continuación, en **Ejecutar**.
2.  En el cuadro **Abrir**, escriba **services.msc** y, a continuación, haga clic en **Aceptar**.

Desplácese por la lista de servicios y compruebe que existe un servicio con el nombre MSSQL$WSUS (si usó "WSUS" para instancename) o MSSQLSERVER (si usó el valor predeterminado para instancename).

#### Paso 4: iniciar la instancia de MSDE

Al final de la instalación de MSDE, tiene que iniciar la instancia. Si usó "WSUS" para instancename, debe iniciar "MSSQL$WSUS". Si usó el valor predeterminado para instancename, debe iniciar MSSQLSERVER. Si no inicia este servicio, WSUS no podrá usar la instancia de base de datos.

#### Paso 5: actualizar MSDE

Debe descargar e instalar la actualización de seguridad descrita en el boletín [MS03-031: Revisión de seguridad acumulativa para SQL Server](http://go.microsoft.com/fwlink/?linkid=47364).

Para descargar la actualización de seguridad, vea [Revisión de seguridad de SQL Server 2000 (32 bits) MS03-031](http://go.microsoft.com/fwlink/?linkid=47363).

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

Si ejecuta los servicios de Internet Information Server (IIS) en un equipo con Windows 2000 Server, instale la última versión del asistente para Lockdown de IIS (que incluye URLScan) desde la página Herramienta Lockdown de IIS en Microsoft TechNet. Microsoft recomienda instalar esta herramienta para proteger los servidores IIS. El Asistente para bloqueo de IIS desactiva las características innecesarias de IIS, por lo que se reduce la exposición a riesgos de seguridad.

| ![](images/Cc720505.note(WS.10).gif)Nota                                                                                                                                                               |
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
-   La instalación de un SQL Server remoto (para su uso como base de datos de WSUS) no se realiza correctamente si Terminal Services está instalado en el servidor remoto y se ejecuta en modo de aplicación. Al instalar SQL Server en un servidor Terminal Services, debe realizar lo siguiente:
    1.  Antes de ejecutar el programa de instalación, abra un símbolo del sistema y escriba: **change user /install**
    2.  Ejecute el programa de instalación de SQL Server.
    3.  Una vez ejecutado el programa de instalación, en el símbolo del sistema escriba: **change user /execute**
-   Debe ser miembro del grupo de seguridad Administradores locales en el equipo cliente y servidor para configurar la base de datos de WSUS del servidor SQL Server remoto.
-   Para obtener más información acerca de los problemas de SQL remoto, consulte "Apéndice C: SQL remoto" en [Guía paso a paso para empezar a trabajar con Microsoft Windows Server Update Services](http://go.microsoft.com/fwlink/?linkid=41777).

#### Problema 13: es posible que un servidor que sigue en la cadena de réplica tenga menos aprobaciones que el servidor que precede en la cadena principal

Es posible que un servidor que sigue en la cadena de réplica tenga menos aprobaciones que el servidor que precede en la cadena principal. Esto se debe a las aprobaciones de instalación no fluyen al servidor que sigue en la cadena hasta que termina de descargarse el contenido en el servidor que precede en la cadena.

#### Problema 14: si se produce un error de sincronización, vuelva a intentarlo

Si se produce un error de sincronización, puede obtener un mensaje de error. En este caso, primero debe intentar la sincronización.

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

**Advertencia**: esto puede afectar a la funcionalidad de Windows® SharePoint® Services y Exchange.

#### Problema 19: es necesario agregar la dirección URL de la consola de WSUS a la lista de zonas de contenido Web Sitios de confianza e Intranet local en equipos en los que el endurecimiento de Internet Explorer está habilitado

Si el endurecimiento de Internet Explorer (también conocido como componente Configuración de seguridad mejorada de Internet Explorer de Microsoft Windows Server 2003) está habilitado en un equipo y no agrega la consola de WSUS en las zonas de contenido Web Sitios de confianza e Intranet local, se le pedirán las credenciales de usuario cada vez que abra una página en la consola de WSUS.

Para agregar la consola de WSUS a las zonas de contenido Web **Intranet local** y **Sitios de confianza**:

1.  Abra **Opciones de Internet** (por ejemplo, haga clic en **Inicio**, seleccione **Panel de control** y, a continuación, haga clic en **Opciones de Internet**).
2.  En la ficha **Seguridad**, haga clic en **Intranet local**, en **Sitios** y en **Opciones avanzadas**, agregue la dirección URL (http://*WSUSServername*/WSUSAdmin) y haga clic en **Aceptar**.
3.  Haga clic en **Sitios de confianza** y en **Sitios**, agregue la dirección URL de la consola de WSUS, haga clic en **Aceptar** y, a continuación, en **Aceptar** otra vez para salir de **Opciones de Internet**.

#### Problema 20: no se realiza la actualización desde el candidato de versión comercial de WSUS

Se puede producir un error en la actualización desde el candidato de versión comercial de WSUS debido a un problema de actualización automática del árbol. Esto puede suceder si varios clientes se actualizan automáticamente al mismo tiempo que intenta realizar la actualización.

Para solucionar este problema:

1.  Desconecte el servidor WSUS de la red y asegúrese de que los clientes no se pueden conectar a él.
2.  En el símbolo del sistema, escriba: **iisrestart /reset** y, a continuación, presione ENTRAR.
3.  Ejecute la actualización.

#### Problema 21: algunas aprobaciones de SUS 1.0 no migran a WSUS.

Al migrar de SUS 1.0 a WSUS, algunas aprobaciones en el servidor SUS 1.0 no migran al servidor WSUS. Esto se debe a que el número de actualizaciones disponibles para SUS 1.0 ya no están disponibles para WSUS. Asimismo, como WSUS admite más actualizaciones que SUS, puede haber actualizaciones importantes en el servidor WSUS que no están aprobadas después de que finaliza el proceso de migración.

Microsoft recomienda revisar el conjunto de actualizaciones no aprobadas en el servidor WSUS después de la migración desde SUS 1.0.

Para obtener más información acerca de la migración de SUS 1.0 a WSUS, vea [Guía paso a paso para migrar de Software Update Services a Windows Server Update Services](http://go.microsoft.com/fwlink/?linkid=48042) en http://go.microsoft.com/fwlink/?LinkId=48042.

#### Problema 22: corrija esta entrada del Registro antes de actualizar a WSUS 2.0 Service Pack 1 si ha migrado WMSDE a SQL Server

Si planea actualizar WSUS 2.0 a Service Pack 1 y ha migrado la instalación de WMSDE a SQL Server (tanto si es remota como local), asegúrese de cambiar la siguiente entrada del Registro:

HKLM\\Software\\Microsoft\\Update Services\\Server\\Setup\\WmsdeInstalled

El valor se debe cambiar de 1 a 0.

#### Problema 23: migración de instalación de SQL remoto a WSUS 2.0 Service Pack 1

Realice los siguientes pasos cuando migre a WSUS 2.0 Service Pack 1 con una configuración de SQL remoto:

1) Ejecute el paquete de instalación en el front-end sin modificadores y elija actualizarse.

2) Ejecute el paquete de instalación en el back-end sin modificadores y elija actualizarse.

#### Copyright

La información que contiene este documento representa la visión actual de Microsoft Corporation sobre los temas tratados en la fecha de publicación. Dado que Microsoft debe responder a las condiciones cambiantes del mercado, no debe interpretarse como un compromiso por parte de Microsoft, y Microsoft no puede garantizar la precisión de cualquier información presentada después de la fecha de publicación.

Este documento tiene únicamente fines informativos. MICROSOFT NO OTORGA NINGUNA GARANTÍA, EXPLÍCITA, IMPLÍCITA O ESTATUTARIA, A LA INFORMACIÓN INCLUIDA EN ESTE DOCUMENTO.

Es responsabilidad del usuario el cumplimiento de todas las leyes de derechos de autor aplicables. Sin limitar los derechos correspondientes de acuerdo con la ley de derechos de autor, ninguna parte de este documento puede ser reproducida, almacenada ni introducida en un sistema de recuperación, ni transmitida de ninguna forma, por ningún medio (ya sea electrónico, mecánico, mediante fotocopias, grabación u otros) y con ningún propósito sin la previa autorización por escrito de Microsoft Corporation.

Microsoft puede ser titular de patentes o tener solicitudes de patentes, marcas comerciales, derechos de autor y otros derechos sobre la propiedad intelectual acerca del contenido de este documento. La difusión del mismo no le otorga ninguna licencia sobre estas patentes, marcas comerciales, derechos de autor ni otros derechos sobre la propiedad intelectual, a menos que se indique por escrito en un contrato de licencia de Microsoft.

A menos que se indique lo contrario, los nombres de las compañías, organizaciones, productos, nombres de dominio, direcciones de correo electrónico, logotipos, personas, lugares y acontecimientos utilizados en los ejemplos son ficticios y no representan de ningún modo a ninguna compañía, organización, producto, nombre de dominio, dirección de correo electrónico, logotipo, persona, lugar o acontecimiento real.

© 2005 Microsoft Corporation. Reservados todos los derechos.

Microsoft, SQL Server, Windows y Windows Server son marcas registradas o marcas comerciales de Microsoft Corporation en Estados Unidos y otros países.

Los nombres de compañías y productos reales mencionados en este documento pueden ser marcas comerciales de sus respectivos propietarios.
