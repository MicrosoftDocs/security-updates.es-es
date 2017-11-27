---
TOCTitle: 'Notas de la versión de Microsoft Windows Server Update Services 3.0 SP1'
Title: 'Notas de la versión de Microsoft Windows Server Update Services 3.0 SP1'
ms:assetid: 'a5aa93bf-842b-4ad4-ab0f-fe867843cb02'
ms:contentKeyID: 18158440
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708525(v=WS.10)'
---

Notas de la versión de Microsoft Windows Server Update Services 3.0 SP1
=======================================================================

Estas notas de la versión describen los problemas conocidos que afectan a Microsoft® Windows® Server Update Services (WSUS) 3.0 Service Pack 1 e incluyen recomendaciones y requisitos para instalar la aplicación. Estas notas contienen las siguientes secciones:

-   Requisitos del sistema para la instalación del servidor WSUS 3.0 SP1
-   Requisitos de configuración para la instalación del servidor WSUS 3.0 SP1
-   Requisitos del sistema para la instalación de la consola remota de WSUS 3.0 SP1
-   Requisitos del sistema para la instalación del cliente
-   Requisitos de software para la instalación del servidor WSUS SP1
-   Requisitos de espacio mínimo en disco para la instalación del servidor WSUS 3.0 SP1
-   Requisitos de actualización de WSUS 3.0 SP1
-   Parámetros de la línea de comandos de instalación
-   Problemas de instalación
-   Problemas de actualización
-   Problemas conocidos
-   WSUS 3.0 SP1 en Windows Server® 2008
-   WSUS 3.0 SP1 en Windows Small Business Server 2003

Requisitos del sistema para la instalación del servidor WSUS 3.0 SP1
--------------------------------------------------------------------

#### El servidor WSUS 3.0 SP1 es compatible con Windows Server 2008 y Windows Server 2003 Service Pack 1

El servidor WSUS 3.0 SP1 es compatible con Windows Server 2008 y Windows Server 2003 Service Pack 1.

#### Windows 2000 Server no es compatible con los servidores WSUS 3.0 SP1

Microsoft Windows® 2000 Server no es un sistema operativo compatible con los servidores WSUS 3.0 SP1.

#### WSUS 3.0 SP1 no es compatible con los servidores que ejecutan Terminal Services

Aunque WSUS 3.0 SP1 puede ejecutarse aún en los servidores que ejecutan Terminal Services, no es recomendable utilizar esta compatibilidad. WSUS 3.0 SP1 no se ejecutará en un servidor que ejecute Terminal Services en las configuraciones que utilicen implementaciones de un servidor SQL remoto. Puede que la instalación no se complete correctamente debido a que todas las acciones personalizadas remotas (incluida la instalación) en un servidor de licencias de Terminal Services se ejecutarán como cuenta del sistema y es posible que ésta no disponga de los permisos necesarios en el servidor SQL remoto.

Requisitos de configuración para la instalación del servidor WSUS 3.0 SP1
-------------------------------------------------------------------------

#### Debe instalarse IIS

Para utilizar WSUS 3.0 SP1, es necesario instalar Internet Information Services (IIS), ya que no se instala de forma predeterminada en Windows Server 2008 o Microsoft Windows Server 2003. Si intenta instalar WSUS 3.0 SP1 sin IIS, la instalación de Windows Server Update Services mostrará un mensaje de error que indica que no se ha instalado este componente.

#### Si IIS se ejecuta en el modo de aislamiento de IIS 5.0, la instalación presentará errores

Si ha actualizado el servidor de Windows 2000 Server a Windows Server 2003, IIS podría estar ejecutándose en el modo de compatibilidad de IIS 5.0. También es posible habilitar el modo de aislamiento de IIS 5.0 en IIS Manager, pero esto provocará que la instalación presente errores. Deberá deshabilitar el modo de aislamiento de IIS 5.0 para poder instalar WSUS 3.0 SP1.

#### Si cualquier componente de IIS se instala con el modo de compatibilidad de 32 bits en una plataforma de 64 bits, la instalación de WSUS 3.0 SP1 presentará errores

Todos los componentes de IIS deben instalarse en el modo nativo en las plataformas de 64 bits. Es posible que la instalación presente errores si alguno de los componentes de IIS se encuentra en el modo de compatibilidad de 32 bits.

#### Los servidores proxy pueden admitir sólo HTTP o HTTP y HTTPS

En WSUS 3.0 SP1, es posible que el servidor proxy sólo admita HTTP. Debería configurar un segundo servidor proxy que ejecute HTTPS mediante la línea de comandos (**wsusutil configuresslproxy**) antes de configurar el servidor WSUS en el Asistente para la configuración o la consola de administración.

#### Si dos o más sitios web ya se están ejecutando en el puerto 80, elimínelos todos excepto uno, antes de instalar WSUS

Si dos o más sitios web ya se están ejecutando en el puerto 80 (por ejemplo, Windows® SharePoint® Services), debe eliminarlos todos menos uno, antes de instalar WSUS. De lo contrario, es posible que los clientes del servidor no puedan actualizarse automáticamente.

#### Al instalar WSUS 3.0 SP1, es posible que deba deshabilitar los programas antivirus

Al instalar WSUS 3.0 SP1, es posible que deba deshabilitar los programas antivirus para poder realizar con éxito la instalación. Una vez deshabilitado el programa antivirus, reinicie el equipo antes de instalar WSUS. De esta forma, se impide que se bloqueen los archivos cuando el proceso de instalación necesite obtener acceso a ellos. Una vez completada la instalación, asegúrese de volver a habilitar el programa antivirus. Visite el sitio web del proveedor de su programa antivirus para conocer los pasos exactos que permiten deshabilitar y volver a habilitar el programa antivirus y la versión.

> [!CAUTION]
> Esta solución puede hacer que su equipo o red sea más vulnerable a los ataques por parte de usuarios malintencionados o software nocivo como, por ejemplo, virus. No recomendamos que lleve a cabo esta solución; simplemente le proporcionamos esta información para que pueda implementar esta solución según su criterio. Use esta solución por su cuenta y riesgo. 

> [!NOTE]
> Un programa antivirus está diseñado para proteger su equipo de los virus. No debe descargar o abrir archivos de fuentes que no sean de confianza, visitar sitios web que no sean seguros o abrir archivos adjuntos cuando el programa antivirus esté deshabilitado. 

#### Es necesario activar la opción de desencadenadores anidados para WSUS 3.0 SP1 en SQL Server

La opción de desencadenadores anidados se activa de forma predeterminada. Sin embargo, un administrador de SQL Server puede desactivarla.

Si tiene intención de utilizar una base de datos de SQL Server como almacén de datos de Windows Server Update Services, el administrador de SQL Server debe verificar que la opción de desencadenadores anidados esté activada en el servidor antes de que el administrador de WSUS 3.0 SP1 instale esta aplicación y especifique la base de datos durante este proceso.

Durante la instalación de WSUS 3.0 SP1 se activa RECURSIVE\_TRIGGERS, que es una opción específica de la base de datos. Sin embargo, no se activa la opción de desencadenadores anidados, que es una opción global del servidor.

Para comprobar si la opción de desencadenadores anidados está activada, utilice lo siguiente:

**sp\_configure 'nested triggers'**

Para activar la opción de desencadenadores activados en SQL Server, ejecute lo siguiente en un archivo por lotes en el equipo que ejecuta SQL Server:

**sp\_configure 'nested triggers', 1**

**GO**

**RECONFIGURE**

**GO**

Si no dispone de SQL Server Management Studio en el equipo, debe ejecutar las secuencias de comandos SQL desde la línea de comandos. Puede obtener la utilidad de consulta de línea de comandos de Microsoft SQL Server 2005 en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=70728) (http://go.microsoft.com/fwlink/?LinkId=70728). En primer lugar, ejecute **sqlcmd**.

Si desea ejecutar secuencias de comandos SQL en Windows Internal Database, debe descargar también SQL Server Native Client desde la misma página de descarga.

#### Limitaciones y requisitos del servidor SQL remoto

WSUS 3.0 SP1 permite ejecutar el software de base de datos en un equipo distinto al equipo en el que se encuentre el resto de la aplicación WSUS 3.0 SP1. Existen algunos requisitos para configurar una instalación de un servidor SQL remoto:

-   Puede utilizar un servidor configurado como controlador de dominio para el back-end de la pareja de servidores SQL.
-   No se debe ejecutar Terminal Server en el equipo que se utilizará como servidor front-end de una instalación del servidor SQL remoto.
-   Debe utilizar, como mínimo, Microsoft SQL Server 2005 Service Pack 1 (disponible en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=66143) (http://go.microsoft.com/fwlink/?LinkId=66143) como software de base de datos en el equipo back-end si ese equipo está ejecutando Windows Server 2003 y SQL Server 2005 Service Pack 2 o si ese equipo está ejecutando Windows Server® 2008.
-   Tanto el equipo front-end como el equipo back-end deben unirse en un dominio de Active Directory. De lo contrario, si se encuentran en diferentes dominios, deberá establecer una relación cruzada de confianza entre los dominios antes de ejecutar la instalación de WSUS.
-   Si ya ha instalado WSUS 2.0 en una configuración del servidor SQL remoto y desea actualizar a WSUS 3.0 SP1, debe desinstalar WSUS 2.0 (mediante **Agregar o quitar programas** en el Panel de control) en el equipo back-end asegurándose de que la base de datos existente permanezca intacta. A continuación, debe desinstalar SQL Server 2005 SP1 o SP2 y actualizar la base de datos existente. Por último, debe instalar WSUS 3.0 SP1 en el equipo front-end.

Requisitos del sistema para la instalación de la consola remota de WSUS 3.0 SP1
-------------------------------------------------------------------------------

La consola remota de WSUS 3.0 SP1 puede instalarse en las siguientes plataformas:

-   Windows Server 2008
-   Windows Vista® o posterior
-   Windows Server 2003 SP1 o posterior
-   Windows XP SP2 o posterior

Requisitos del sistema para la instalación del cliente
------------------------------------------------------

Actualizaciones automáticas es el software de cliente de WSUS. Puede utilizarse con WSUS en cualquiera de los siguientes sistemas operativos:

-   Windows Vista o posterior
-   Windows Server 2008 o posterior
-   Microsoft Windows Server 2003, cualquier edición
-   Microsoft Windows XP Professional SP2 o posterior
-   Microsoft Windows 2000 Professional SP4, Windows 2000 Server SP4 o Windows 2000 Advanced Server con SP4

Requisitos de software para la instalación del servidor WSUS 3.0 SP1
--------------------------------------------------------------------

La siguiente tabla muestra el software necesario para las plataformas Windows Server 2003 SP1. El software necesario para Windows Server 2008 se indicará en la sección que trata sobre WSUS 3.0 SP1 en Windows Server 2008.

Asegúrese de que el servidor WSUS 3.0 SP1 cumpla esta lista de requisitos antes de ejecutar la instalación de WSUS 3.0 SP1. Si es necesario reiniciar el equipo para cualquiera de estas actualizaciones una vez completada la instalación, debería efectuar el reinicio antes de instalar WSUS 3.0 SP1.

###  

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Requisito</th>
<th style="border:1px solid black;" >Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Internet Information Services (IIS)</td>
<td style="border:1px solid black;">Se instala desde el sistema operativo.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft .NET Framework versión 2.0 Redistributable Package</td>
<td style="border:1px solid black;">Consulte Microsoft .NET Framework versión 2.0 Redistributable Package (x86) en el <a href="http://go.microsoft.com/fwlink/?linkid=68935">Centro de descarga de Microsoft</a> (http://go.microsoft.com/fwlink/?LinkId=68935). Para las plataformas de 64 bits, consulte Microsoft .NET Framework versión 2.0 Redistributable Package (x64) en el <a href="http://go.microsoft.com/fwlink/?linkid=70637">Centro de descarga de Microsoft</a> (http://go.microsoft.com/fwlink/?LinkId=70637).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Management Console 3.0`para Windows Server 2003</td>
<td style="border:1px solid black;">Se trata de un requisito previo para usar la interfaz de usuario de WSUS 3.0 SP1. Consulte Microsoft Management Console 3.0 para Windows Server 2003 (KB907265) en el <a href="http://go.microsoft.com/fwlink/?linkid=70412">Centro de descarga de Microsoft</a> (http://go.microsoft.com/fwlink/?LinkId=70412). Para las plataformas de 64 bits, consulte Microsoft Management Console 3.0 para Windows Server 2003 x64 Edition (KB907265) en el <a href="http://go.microsoft.com/fwlink/?linkid=70638">Centro de descarga de Microsoft</a>(http://go.microsoft.com/fwlink/?LinkId=70638).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Report Viewer</td>
<td style="border:1px solid black;">Se trata de un requisito previo para usar la interfaz de usuario de WSUS 3.0 SP1. Consulte Microsoft Report Viewer Redistributable 2005 en el <a href="http://go.microsoft.com/fwlink/?linkid=70410">Centro de descarga de Microsoft</a> (http://go.microsoft.com/fwlink/?LinkId=70410).</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SQL Server 2005 (opcional)</td>
<td style="border:1px solid black;">WSUS 3.0 SP1 instalará automáticamente Windows Internal Database si no se ha instalado aún ninguna versión compatible de SQL Server. Si tiene intención de utilizar una base de datos completa de SQL Server, debe utilizar como mínimo SQL Server 2005 SP1 (disponible en el <a href="http://go.microsoft.com/fwlink/?linkid=66143">Centro de descarga de Microsoft</a> (http://go.microsoft.com/fwlink/?LinkId=66143) en Windows Server 2003 o SQL Server 2005 SP2 (disponible en el <a href="http://go.microsoft.com/fwlink/?linkid=84823">Centro de descarga de Microsoft</a> (http://go.microsoft.com/fwlink/?LinkId=84823) en Windows Server 2008.</td>
</tr>
</tbody>
</table>
  
> [!Nota]
> Si se ha instalado anteriormente WSUS 2.0 y esta versión utiliza SQL Server 2000, SQL Server Desktop Engine 2000 o cualquier base de datos de SQL Server anterior a SQL Server 2005 SP1 (o SQL Server 2005 SP2 en Windows Server 2008), el programa de instalación de WSUS 3.0 SP1 instalará Windows® Internal Database y migrará la base de datos a éste.
  
Requisitos de espacio mínimo en disco para la instalación del servidor WSUS 3.0 SP1  
-----------------------------------------------------------------------------------
  
A continuación, se muestran los requisitos de espacio en mínimo en disco para instalar Windows Server Update Services:
  
-   1 GB en la partición del sistema  
-   2 GB para el volumen en el que se almacenarán los archivos de base de datos  
-   20 GB para el volumen en el que se almacenará el contenido
  
> [!Importante]
> WSUS 3.0 SP1 no puede instalarse en unidades comprimidas. Compruebe que la unidad que ha seleccionado no se haya comprimido. 
  
Requisitos de actualización de WSUS 3.0 SP1  
-------------------------------------------
  
#### Asegúrese de que la instalación de WSUS se ejecute correctamente y realice una copia de seguridad de la base de datos de WSUS antes de realizar la actualización
  
Si va actualizar una versión anterior de WSUS a WSUS 3.0 SP1, asegúrese de que la instalación de WSUS se ejecute correctamente y realice una copia de seguridad de la base de datos de WSUS antes de realizar la actualización
  
1.  Consulte los registros de eventos en busca de errores recientes, problemas de sincronización entre los servidores que siguen y preceden en la cadena o problemas con clientes que no respondan. Asegúrese de que se hayan solucionado estos problemas antes de continuar.  
2.  Debe ejecutar DBCC CHECKDB para asegurarse de que la base de datos de WSUS se haya indizado correctamente. Para obtener más información sobre DBCC CHECKDB, consulte [DBCC CHECKDB](http://go.microsoft.com/fwlink/?linkid=86948) (http://go.microsoft.com/fwlink/?LinkId=86948).  
3.  Realice una copia de seguridad de la base de datos de WSUS.
  
#### Si ha modificado manualmente el puerto utilizado por WSUS, desinstale la aplicación antes de efectuar la actualización
  
Al modificar el puerto de WSUS, utilice siempre la utilidad wsusutil en lugar de intentar modificarlo manualmente. Si ha modificado manualmente el puerto y ha actualizado anteriormente Software Update Services 1.0 a WSUS 2.0:
  
1.  Si aún no ha instalado WSUS 3.0, desinstale WSUS 2.0, conservando la base de datos y el contenido. (Si, por el contrario, ya ha instalado WSUS 3.0, desinstale esta aplicación, conservando la base de datos y el contenido.)  
2.  Inicie el sitio web predeterminado, habilitando de nuevo temporalmente SUS 1.0 y permitiendo su acceso al programa de desinstalación.  
3.  Desinstale SUS 1.0.  
4.  Instale WSUS 3.0.
  
#### Software Update Services 1.0 debe desinstalarse
  
La instalación de WSUS 3.0 SP1 no se realizará con éxito si Software Update Services 1.0 se ha instalado en el mismo equipo. Debe desinstalar Software Update Services 1.0 antes de instalar WSUS 3.0 SP1.
  
#### No se puede actualizar WSUS 2.0 a WSUS 3.0 SP1 en un sistema operativo de 64 bits
  
WSUS 2.0 no se admite en los sistemas operativos de 64 bits. No se puede actualizar WSUS 2.0 a WSUS 3.0 SP1 en los sistemas operativos de 64 bits
  
Parámetros de la línea de comandos de instalación  
-------------------------------------------------
  
Puede realizar una instalación desatendida de WSUS 3.0 SP1 mediante el programa de instalación de la línea de comandos de WSUS. En esta tabla, se muestran los parámetros de la línea de comandos para la instalación de WSUS 3.0 SP1.
  
###  

 
<p> </p>
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
<td style="border:1px solid black;">Realiza una instalación silenciosa.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>/u</strong></td>
<td style="border:1px solid black;">Desinstala el producto. También desinstala la instancia de Windows Internal Database, si se encuentra instalada.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>/p</strong></td>
<td style="border:1px solid black;">Sólo para la comprobación de requisitos previos. No instala el producto, pero inspecciona el sistema e informa de los requisitos previos que no se han cumplido.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>/?, /h</strong></td>
<td style="border:1px solid black;">Muestra los parámetros de la línea de comandos y su descripción.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>/g</strong></td>
<td style="border:1px solid black;">Realiza una actualización de la versión anterior de WSUS. (No intente realizar una actualización de SUS 1.0.) El único parámetro válido que se puede utilizar con esta opción es /q (instalación silenciosa). La única propiedad válida que se puede utilizar con esta opción es DEFAULT_WEBSITE.</td>
</tr>
</tbody>
</table>
  
En esta tabla, se muestran las propiedades de la línea de comandos para WSUS 3.0 SP1.
  
###  

 
<p> </p>
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
<td style="border:1px solid black;">0=contenido alojado de forma local, 1=alojado en Microsoft Update</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">CONTENT_DIR</td>
<td style="border:1px solid black;">Ruta al directorio de contenido. El valor predeterminado es <em>unidadDeInstalaciónDeWSUS</em><strong>&gt;\WSUS\contenidoWSUS</strong>, donde <em>WSUSInstallationDrive</em> es la unidad local con la mayor cantidad de espacio libre.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">WYUKON_DATA_DIR</td>
<td style="border:1px solid black;">Ruta al directorio de datos de Windows Internal Database.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SQLINSTANCE_NAME</td>
<td style="border:1px solid black;">El nombre debería presentar el formato <em>nombreDeServidor</em>\<em>nombreDeLaInstanciaDeSQL</em>. Si la instancia de la base de datos se encuentra en el equipo local, utilice la variable de entorno %NOMBREEQUIPO % Si no hay ninguna instancia, el valor predeterminado es %NOMBREEQUIPO%\WSUS.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">DEFAULT_WEBSITE</td>
<td style="border:1px solid black;">0=puerto 8530, 1=puerto 80</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">PREREQ_CHECK_LOG</td>
<td style="border:1px solid black;">Ruta y nombre del archivo de registro</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">CONSOLE_INSTALL</td>
<td style="border:1px solid black;">0=instalar el servidor de WSUS, 1=instalar sólo la consola</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ENABLE_INVENTORY</td>
<td style="border:1px solid black;">0=no instalar las características de inventario, 1=instalar las características de inventario</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">DELETE_DATABASE</td>
<td style="border:1px solid black;">0=conservar la base de datos, 1=eliminar la base de datos</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">DELETE_CONTENT</td>
<td style="border:1px solid black;">0=conservar los archivos de contenido, 1=eliminar los archivos de contenido</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">DELETE_LOGS</td>
<td style="border:1px solid black;">0=conservar los archivos de registro, 1=eliminar los archivos de registros (utilizados con el conmutador de instalación /u)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">CREATE_DATABASE</td>
<td style="border:1px solid black;">0=utilizar base de datos actual, 1=crear base de datos</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">PROGRESS_WINDOW_HANDLE</td>
<td style="border:1px solid black;">Identificador de ventana para devolver mensajes de progreso de MSI</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">MU_ROLLUP</td>
<td style="border:1px solid black;">1`=participar en el Programa de mejora de Microsoft Update, 0=no participar en el Programa de mejora de Microsoft Update</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">FRONTEND_SETUP</td>
<td style="border:1px solid black;">1=no escribir la ubicación del contenido en la base datos, 0= escribir la ubicación del contenido en la base datos (para NLB)</td>
</tr>
</tbody>
</table>
  
#### Sintaxis de ejemplo
  
```  
    WSUSSetup.exe /q DEFAULT\_WEBSITE=0 (install in quiet mode using port 8530) WSUSSetup.exe /q /u (uninstall WSUS)  
```  

> [!Importante]
> Si instala WSUS 3.0 SP1 en el modo silencioso (/q) y no se han instalado en el equipo todos los requisitos previos, la instalación generará un archivo con el nombre WSUSPreReqCheck.xml y lo guardará en el directorio %TEMP%.
  
Problemas de instalación  
------------------------
  
#### IIS se reiniciará durante la instalación de WSUS 3.0 SP1
  
Durante la instalación de WSUS 3.0 SP1, se reiniciará IIS sin que se emita sin ninguna notificación, lo que podría afectar a los sitios web de su organización. Si IIS no se está ejecutando, el proceso de instalación de WSUS 3.0 SP1 lo iniciará.
  
#### Si hay conexiones abiertas a una base de datos de WSUS existente, es posible que no se complete la instalación
  
Si realiza una actualización a WSUS 3.0 SP1 desde una instalación existente y aún hay conexiones abiertas a la base de de WSUS existente (por ejemplo, si SQL Server Management Studio está abierto), es posible que la instalación no se complete correctamente. Cierre todas las conexiones y reinstale WSUS 3.0 SP1.
  
#### La instalación de WSUS muestra un directorio incorrecto para los archivos de base de datos
  
Durante la instalación de WSUS, la pantalla **Preparado para instalar** informa incorrectamente de que la ubicación de la base de datos es el directorio principal de esta ubicación. Por ejemplo, la ubicación predeterminada es %systemdrive%\\WSUS\\UpdateServicesDbFiles, pero se indica de forma incorrecta la ubicación %systemdrive%\\WSUS.
  
#### Si WSUS se instala en un equipo con paquetes de idiomas de la Interfaz de usuario multilingüe con un idioma predeterminado distinto del inglés, la Ayuda se mostrará en el idioma predeterminado en lugar de en inglés
  
Si, en el equipo, dispone de paquetes de idiomas de la Interfaz de usuario multilingüe con un idioma predeterminado distinto del inglés, podrá instalar WSUS sólo cuando la configuración regional del usuario actual sea la inglesa. La IU se mostrará en inglés, pero debe aplicar la siguiente solución para que la Ayuda se muestre también en ese idioma. Copie el archivo Help.chm del idioma inglés (*directorioDeInstalaciónDeWSUS*\\documentation\\mui\\0409\\WSUS30Help.chm) en el directorio de documentación principal (*directorioDeInstalaciónDeWSUS*\\documentation\\WSUS30Help.chm). Una vez realizada esta tarea, la Ayuda debería mostrarse correctamente en todos los idiomas.
  
Problemas de actualización  
--------------------------
  
#### Recuperación a partir de una actualización con errores
  
Si realiza una actualización desde una versión anterior de WSUS (WSUS 3.0, WSUS 2.0 SP1 o WSUS 2.0) a WSUS 3.0 SP1 y la actualización presenta errores por cualquier motivo:
  
1.  Reinstale la versión anterior de WSUS.  
2.  Restablezca la base de datos a partir de la copia de seguridad efectuada al intentar realizar la actualización. (En la mayoría de los casos, WSUS crea automáticamente también una copia de seguridad. Consulte el archivo de registro WSUSSetup.log para conocer su ubicación.)  
3.  Revise los registros para determinar la causa del error y corrija el problema.  
4.  Intente actualizar de nuevo WSUS.
  
#### No se puede actualizar WSUS 2.0 a WSUS 3.0 SP1 si hay una base de datos de WSUS 3.0 SP1 de una instalación anterior
  
Si ha instalado anteriormente WSUS 3.0 SP1 y, a continuación, ha reinstalado WSUS 2.0, debe eliminar la base de datos de WSUS 3.0 SP1 en el equipo antes de reinstalar esta aplicación.
  
#### Si cambia el nombre del equipo antes de actualizar a WSUS 3.0 SP1, la actualización puede presentar errores
  
Si cambia el nombre del equipo después de instalar WSUS 2.0 y antes de actualizar a WSUS 3.0 SP1, la actualización puede presentar errores.
  
Utilice la siguiente secuencia de comandos para eliminar y volver a agregar los grupos de administradores de ASPNET y WSUS. A continuación, vuelva a ejecutar la actualización.
  
Deberá sustituir *&lt;DBLocation&gt;* por la carpeta en la que se ha instalado la base de datos y *&lt;ContentDirectory&gt;* por la carpeta de almacenamiento local.
  
```  
    sqlcmd.exe -S <DBLocation> -E -Q "USE SUSDB DECLARE @asplogin varchar(200) SELECT @asplogin=name from sysusers WHERE name like '%ASPNET' EXEC sp_revokedbaccess @asplogin"
    sqlcmd.exe -S <DBLocation> -E -Q "USE SUSDB DECLARE @wsusadminslogin varchar(200) SELECT @wsusadminslogin=name from sysusers WHERE name like '%WSUS Administrators' EXEC sp_revokedbaccess @wsusadminslogin"
    
    sqlcmd.exe -S <DBLocation> -E -Q "USE SUSDB DECLARE @asplogin varchar(200) SELECT @asplogin=HOST_NAME()+'\ASPNET' EXEC sp_grantlogin @asplogin EXEC sp_grantdbaccess @asplogin EXEC sp_addrolemember webService,@asplogin"
    sqlcmd.exe -S <DBLocation> -E -Q "USE SUSDB DECLARE @wsusadminslogin varchar(200) SELECT @wsusadminslogin=HOST_NAME()+'\WSUS Administrators' EXEC sp_grantlogin @wsusadminslogin EXEC sp_grantdbaccess @wsusadminslogin EXEC sp_addrolemember webService,@wsusadminslogin"
    
    sqlcmd.exe -S <DBLocation> -E -Q "backup database SUSDB to disk=N'<ContentDirectory>\SUSDB.Dat' with init"
```
  
#### Durante la instalación se sobrescribirá una copia de seguridad anterior de la base de datos
  
El programa de instalación de WSUS 3.0 SP1 agregará la base de datos al directorio predeterminado, que es *unidad*\\WSUS (donde *unidad* es la unidad NTFS local con la mayor cantidad de espacio libre). Si en este directorio existe una copia de seguridad de la base de datos, puede que se sobrescriba. Antes de actualizar a WSUS 3.0 SP1, los administradores deben guardar una copia de seguridad de la base de datos de la versión actual en una ubicación diferente.
  
#### Si ha migrado de MSDE a SQL Server 2000 o a SQL Server 2005 en WSUS 2.0, deberá cambiar un valor del Registro
  
Si tiene una instalación de WSUS 2.0 y ha migrado a SQL Server 2000 o SQL Server 2005, deberá cambiar el valor **HKLM\\SOFTWARE\\Microsoft\\Update Services\\Server\\Setup\\WmsdeInstalled** de 1 a 0, ya que si no lo hace antes de actualizarse a WSUS 3.0 SP1, la actualización presentará errores.
  
#### Si se inicia y cancela la instalación de WSUS 2.0, se eliminará la clave del Registro de WSUS
  
Si inicia la instalación de WSUS 2.0 y luego la cancela, se eliminará la clave del Registro de WSUS. Esto puede ocasionar problemas si ya tiene instalado WSUS 3.0 SP1. Se puede presentar el mismo problema si comienza a desinstalar WSUS 2.0, luego cancela la operación e intenta actualizar WSUS 2.0 a WSUS 3.0 SP1.
  
#### Si desinstala WSUS 3.0 SP1 y deja los archivos de registro, puede que no tengan los permisos correctos después de realizar una nueva instalación
  
Al desinstalar WSUS 3.0 SP1, tiene la opción de conservar los archivos de registro de la instalación. Cuando se vuelve a instalar WSUS 3.0 SP1, los archivos de registro antiguos pierden sus permisos (por lo habitual, sólo para los administradores de WSUS). Será necesario restaurar los permisos de estos archivos de registro.
  
#### Si los clientes de WSUS 2.0 tienen actualizaciones con el estado "No aplicable", éstas aparecerán como "Desconocido" durante un breve periodo después de la actualización a WSUS 3.0 SP1
  
Si un servidor de WSUS 2.0 tiene clientes con actualizaciones **No aplicable**, éstas aparecerán con un estado **Desconocido** durante un breve periodo después de que el servidor se ha actualizado a WSUS 3.0 SP1. El estado de actualización volverá a **No aplicable** la próxima vez que el cliente realice una búsqueda.
  
Problemas conocidos  
-------------------
  
#### Solución de problemas de varios errores de descarga o de errores repetidos de sincronización de clientes
  
Si los clientes de WSUS 3.0 SP1 informan de varios errores de descarga o si no se pueden sincronizar con el servidor WSUS 3.0 SP1 durante un largo periodo de tiempo, es posible que la caché de descarga del cliente esté dañada. Para recuperarse de este estado, puede intentar eliminar la caché de descarga del cliente del sistema de archivos.
  
Para eliminar la caché de descarga del cliente:
  
1.  Elimine del equipo cliente todos los archivos y subdirectorios que haya en esta ubicación: **%windir%\\SoftwareDistribution\\Download**  
2.  Pruebe a instalar la actualización sincronizando de nuevo el equipo cliente con WSUS 3.0 SP1. Este intento de instalación dará el siguiente error: **WU\_E\_DM\_NOTDOWNLOADED, "No se descargó la actualización".**  
3.  Después de este error, el equipo cliente reiniciará automáticamente la descarga y la instalación podrá continuar.
  
#### Si la sincronización no se realiza correctamente, vuelva a intentarla
  
Si el problema continúa, lo primero que deberá hacer es volver a intentar sincronizar el servidor. Si tras sucesivos intentos, la sincronización no se realiza correctamente, use la información de solución de problemas de la [Guía de operaciones de Windows Server Update Services 3.0](http://go.microsoft.com/fwlink/?linkid=81072) (http://go.microsoft.com/fwlink/?LinkId=81072).
  
#### No se permite cambiar la configuración de WSUS 3.0 SP1 directamente en la base de datos
  
Windows Server Update Services almacena su configuración en una base de datos SQL Server. Sin embargo, no se permite cambiar los datos de configuración mediante el acceso directo a la base de datos. No intente modificar la configuración de WSUS 3.0 SP1 mediante el acceso directo a la base de datos. Cambie la configuración de WSUS 3.0 SP1 mediante la consola de WSUS 3.0 SP1 o llame a las API de WSUS 3.0 SP1.
  
#### Los errores de descarga no se notifican rápidamente cuando están activadas las cuotas de disco
  
Si están activadas las cuotas de disco y se alcanza la cuota, puede que los errores de descarga de actualizaciones en el servidor de WSUS no se notifiquen de forma oportuna. Para evitar este problema, deshabilite las cuotas de disco o aumente la cuota.
  
#### Si se implementa WSUS 3.0 SP1 con SSL, puede que los equipos cliente presenten errores con el código de error 0x8024400a
  
En ocasiones, puede que los equipos cliente no puedan comunicarse correctamente con un servidor WSUS 3.0 SP1 mediante SSL y presenten el código de error 0x8024400a. Para obtener una actualización que solucione este problema, consulte [KB 905422](http://go.microsoft.com/fwlink/?linkid=70593) (http://go.microsoft.com/fwlink/?LinkId=70593).
  
#### La cuenta de dominio Administradores de WSUS no se elimina cuando se desinstala WSUS
  
El grupo Administradores de WSUS se crea como cuenta de dominio (no como cuenta local) en los controladores de dominio, de modo que si se eliminara la cuenta al desinstalar WSUS todas las instalaciones que usan esta cuenta de dominio se deshabilitarían. Por lo tanto, con la desinstalación de WSUS no se elimina la cuenta de dominio Administradores de WSUS.
  
#### Si un servidor que sigue en la cadena se convierte en uno que precede en la cadena, las actualizaciones del sitio del catálogo se deben volver a importar
  
Al aumentar nivel de un servidor que sigue en la cadena para convertirlo en un servidor que precede en la cadena, también debe volver a importar todas las actualizaciones del sitio del catálogo. De lo contrario, el sitio no podrá sincronizar las revisiones de actualización del sitio del catálogo con este servidor.
  
#### Aunque use IIS con SSL, es posible el acceso descifrado a menos que se tenga activada la opción "Requerir canal seguro"
  
Aunque configure IIS para usar SSL instalando un certificado, se puede tener acceso al sitio mediante HTTP descifrado a menos que esté activada la opción **Requerir canal seguro**. Para obtener más información, consulte la documentación de [IIS](http://go.microsoft.com/fwlink/?linkid=98084) (http://go.microsoft.com/fwlink/?LinkId=98084).
  
#### Puede que la importación del sitio del catálogo presente errores sin permisos de lectura o escritura para la carpeta %windir%\\TEMP
  
Al realizar una importación del sitio del catálogo, puede que se genere el siguiente mensaje de error si la cuenta Servicio de red no tiene permiso de lectura o escritura para la carpeta %windir%\\TEMP: El servidor no pudo procesar la solicitud. ---&gt; No se pudo encontrar el archivo "C:\\WINDOWS\\TEMP\\*NombreDeArchivoTemporal*.dll".
  
#### Al sincronizar WSUS 3.0 SP1 y un servidor de réplicas que sigue en la cadena en el que se ejecuta WSUS 2.0, el rendimiento puede ser lento
  
Si instala WSUS 3.0 SP1 en un servidor que precede en la cadena e intenta sincronizarlo con un servidor de réplicas que sigue en la cadena, donde se ejecuta WSUS 2.0, podría experimentar problemas de rendimiento. Para solucionar este problema, consulte [KB 910847](http://go.microsoft.com/fwlink/?linkid=70669) (http://go.microsoft.com/fwlink/?LinkId=70669).
  
#### Si el servidor de correo electrónico está inactivo o es inaccesible, las notificaciones por correo electrónico se realizan de manera incorrecta sin avisar
  
Si el servidor de correo electrónico de la red está sin conexión, WSUS 3.0 SP1 no envía notificaciones por correo electrónico pero no avisa del error. Sin embargo, escribe el evento 10052 (HealthCoreEmailNotificationRed) en el registro de eventos.
  
#### Los cambios en la configuración de un servidor que precede en la cadena no se aplican inmediatamente al servidor que sigue en la cadena
  
Cuando se cambia la configuración del servidor que precede en la cadena, puede que estos cambios tarden algún tiempo en hacerse efectivos. Por ejemplo, si cambia un valor del servidor que precede en la cadena, como puede ser la selección de un nuevo idioma e inmediatamente activa una sincronización en el servidor que sigue en la cadena, el cambio no aparecerá. En su lugar, se aplicará al servidor que sigue en la cadena en la próxima sincronización programada. En función del número de actualizaciones presentes en el servidor que precede en la cadena, el tiempo de espera aumentará.
  
#### Al desinstalar WSUS 3.0 SP1 no se desinstala la instancia de base de datos
  
Si se desinstala WSUS 3.0 SP1, no se desinstalará la instancia de base de datos. Puede que más de una aplicación comparta la instancia y, si se elimina, otras aplicaciones no funcionarán correctamente.
  
Si es necesario desinstalar Windows Internal Database, los siguientes comandos desinstalarán la aplicación:
  
(en plataformas de 32 bits)
  
```
    msiexec /x {CEB5780F-1A70-44A9-850F-DE6C4F6AA8FB} callerid=ocsetup.exe  
```

(en plataformas de 64 bits)
  
```
    msiexec /x {BDD79957-5801-4A2D-B09E-852E7FA64D01} callerid=ocsetup.exe  
```

Si desea desinstalar Windows Internal Database Service Pack 2 de Windows Server 2008, podría hacerlo con Server Manager.
  
Sin embargo, puede que con la eliminación de la aplicación no se eliminen los archivos .mdf y .ldf predeterminados, lo que dará lugar a que una posterior instalación de WSUS 3.0 SP1 presente errores. Estos archivos se pueden eliminar desde el directorio %windir%\\SYSMSI\\SSEE.
  
#### Si un servidor que sigue en la cadena cambia su servidor que precede en la cadena, las actualizaciones con estado "Desconocido" se notifican como "No aplicable"
  
Si un servidor que sigue en la cadena comienza a sincronizarse desde un servidor que precede en la cadena diferente, las actualizaciones con un estado de **Desconocido** se notificarán en el nuevo servidor que precede en la cadena como **No aplicable**. Este estado es temporal y se corregirá la próxima vez que el servidor que sigue en la cadena notifique su estado, una vez que sus clientes se hayan sincronizado con él.
  
#### Si el Asistente para limpieza de servidores agota su tiempo de espera en un servidor cuando se ejecuta en varios servidores desde una consola remota, se perderá la conexión con todos los servidores
  
Se puede ejecutar el Asistente para limpieza de servidores en varios servidores desde una sola consola remota. Sin embargo, si el proceso de limpieza agota el tiempo de espera en uno de los servidores, la consola perderá la conexión con todos los servidores. Si bien no se perderán los datos, el administrador tendrá que reiniciar la conexión remota con cada uno de los servidores.
  
#### Al iniciar y detener la conexión en rápida sucesión aparece el mensaje de error "No hubo error de sincronización" en el Asistente para la configuración
  
Cuando configura WSUS, se le pide que se conecte al servidor que precede en la cadena (Microsoft Update o el servidor que precede en la cadena de la intranet) con el fin de transferir la información básica acerca del servidor. Si hace clic en **Iniciar la conexión** e inmediatamente en **Detener la conexión**, recibirá el mensaje de error incorrecto "No hubo error de sincronización".
  
WSUS 3.0 SP1 en Windows Server 2008  
-----------------------------------
  
#### Versiones compatibles
  
WSUS 3.0 SP1 es compatible con versiones de Windows Server 2008 de 32 y 64 bits.
  
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
<th style="border:1px solid black;" >Requisito</th>
<th style="border:1px solid black;" >Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Internet Information Services (IIS)</td>
<td style="border:1px solid black;">Se instala desde el sistema operativo. Asegúrese de que los siguientes componentes están habilitados:
<ul>
<li>Autenticación de Windows<br />
<br />
</li>
<li>Contenido estático<br />
<br />
</li>
<li>ASP.NET<br />
<br />
</li>
<li>Compatibilidad con 6.0 Management<br />
<br />
</li>
<li>Compatibilidad con 6.0 IIS Metabase<br />
<br />
</li>
</ul></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft .NET Framework versión 2.0 Redistributable Package (x86)</td>
<td style="border:1px solid black;">No es necesario en Windows Server 2008; ya está instalado como parte del sistema operativo.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Management Console 3.0</td>
<td style="border:1px solid black;">No es necesario en Windows Server 2008; ya está instalado como parte del sistema operativo.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Report Viewer</td>
<td style="border:1px solid black;">Se trata de un requisito previo para usar la interfaz de usuario de WSUS. Consulte Microsoft Report Viewer Redistributable 2005 en el <a href="http://go.microsoft.com/fwlink/?linkid=70410">Centro de descarga de Microsoft</a> (http://go.microsoft.com/fwlink/?LinkId=70410).</td>
</tr>
</tbody>
</table>
  
#### Uso del Asistente para configuración de seguridad
  
En Windows Server 2008, al ejecutar el Asistente para configuración de seguridad (SCW), puede seleccionar la función WSUS y habilitar sus dependencias. Para ejecutar el SCW, haga clic en **Inicio**, seleccione **Herramientas administrativas** y, a continuación, haga clic en **Asistente para configuración de seguridad**.
  
Cuando se usa el SCW en combinación con la función WSUS, existen los siguientes problemas conocidos:
  
-   **El servicio Windows Internal Database se habilita a pesar de que WSUS podría no usarlo.** WSUS se configura para usar una base de datos: Windows Internal Database o una base de datos SQL Server. Si WSUS se instala con SQL Server y selecciona la función WSUS en el SCW, el servicio Windows Internal Database se habilita si está instalado en el equipo, aunque WSUS no lo use. Si usa una base de datos SQL Server en lugar de Windows Internal Database, debe deshabilitar el servicio Windows Internal Database.  
-   **En un sitio web personalizado, las reglas de firewall para WSUS no se seleccionan de manera predeterminada.** Si instala WSUS en un sitio web personalizado (puerto 8530 o 8531), las reglas de firewall necesarias no se seleccionan automáticamente aunque seleccione la función WSUS en el SCW. Deberá habilitar las reglas de firewall adecuadas para WSUS en función de si está configurado Secure Sockets Layer (SSL) para el servidor de WSUS.
  
WSUS 3.0 SP1 en Windows Small Business Server 2003  
--------------------------------------------------
  
#### Si la raíz virtual de IIS está limitada a determinadas direcciones IP o nombres de dominio, el servidor WSUS 3.0 SP1 no se podrá actualizar automáticamente
  
Algunas instalaciones de Windows Small Business Server pueden tener configurado el sitio web de IIS predeterminado **con restricciones de dirección IP y nombre de dominio**. Cuando esto sucede, el Cliente de Windows Update del servidor no se puede actualizar automáticamente.
  
#### Instalación de WSUS 3.0 SP1 en Small Business Server: problemas de integración
  
-   Si Windows Small Business Server 2003 usa un servidor proxy ISA para tener acceso a Internet, se debe escribir lo siguiente en la interfaz de usuario de **Configuración**: **configuración del servidor proxy, nombre del servidor proxy, puerto**.  
-   Si ISA usa Autenticación de Windows, las credenciales del servidor proxy se deben escribir con el formato *DOMINIO*\\*usuario* y el usuario debe ser miembro del grupo Usuarios de Internet.
  
#### Si ha agregado una subred a la red sin usar los asistentes de Windows SBS, debe realizar este procedimiento
  
El proceso de instalación del servidor WSUS instala dos raíces virtuales IIS en el servidor: SelfUpdate y ClientWebService. Además, coloca algunos archivos en el directorio principal del sitio web predeterminado (en el puerto 80), que permiten a los equipos cliente actualizarse automáticamente a través del sitio web predeterminado. De manera predeterminada, el sitio web predeterminado está configurado para denegar el acceso a toda dirección IP que no sea localhost o a determinadas subredes vinculadas al servidor. Como consecuencia, los equipos cliente que no están en localhost o en esas subredes concretas no se pueden actualizar automáticamente. Si ha agregado una subred a la red sin usar los asistentes de Microsoft Windows Small Business Server 2003 (Windows SBS), debe realizar este procedimiento:
  
1.  En Administración de servidores, expanda sucesivamente **Administración avanzada**, **Internet Information Services**, **Sitios web**, **Sitio web predeterminado**, haga clic con el botón secundario en el directorio virtual **Selfupdate** y, a continuación, haga clic en **Propiedades**.  
2.  Haga clic en **Seguridad de directorios**.  
3.  En **Restricciones de nombre de dominio y dirección IP**, haga clic en **Editar** y, a continuación, en **Concederá el acceso**.  
4.  Haga clic en **Aceptar**, haga clic con el botón secundario en el directorio virtual **ClientWebService** y, a continuación, haga clic en **Propiedades**.  
5.  Haga clic en **Seguridad de directorios**.  
6.  En **Restricciones de nombre de dominio y dirección IP**, haga clic en **Editar** y, a continuación, en **Concederá el acceso**.
  
Copyright  
---------
  
La información de este documento, incluida las URL y otras referencias a sitios web de Internet, puede estar sujeta a cambios sin aviso previo. A menos que se indique lo contrario, las compañías, las organizaciones, los productos, los nombres de dominio, las direcciones de correo electrónico, los logotipos, las personas, los lugares y los eventos utilizados en los ejemplos del presente documento son ficticios. No se pretende indicar, ni debe deducirse, ninguna asociación con compañías, organizaciones, productos, nombres de dominio, direcciones de correo electrónico, logotipos, personas, lugares y eventos reales. Es responsabilidad del usuario cumplir todas las leyes de derechos de autor vigentes. Sin limitar los derechos en virtud del copyright, ninguna parte de este documento puede reproducirse, almacenarse o introducirse en un sistema de recuperación o transmitirse de ninguna forma o mediante ningún medio (electrónico, mecánico, de fotocopia, grabación o cualquier otro tipo) para ningún fin sin el permiso expreso por escrito de Microsoft Corporation.
  
Microsoft puede tener patentes, aplicaciones de patentes, marcas comerciales, derechos de autor u otros derechos de propiedad intelectual en relación con los temas tratados en este documento. A menos que se indique de forma expresa en cualquier acuerdo de licencia por escrito de Microsoft, la distribución de este documento no le proporciona ninguna licencia en relación con estas patentes, marcas comerciales, derechos de autor u otra propiedad intelectual.
  
© 2007 Microsoft Corporation. Todos los derechos reservados.
  
Microsoft, SQL Server, Windows y Windows Server son marcas comerciales o marcas comerciales registradas de Microsoft Corporation en los Estados Unidos u otros países.
  
Todas las demás marcas comerciales pertenecen a sus respectivos propietarios.
