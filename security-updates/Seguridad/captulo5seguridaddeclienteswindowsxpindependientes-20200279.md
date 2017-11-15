---
TOCTitle: 'Capítulo 5: Seguridad de clientes Windows XP independientes'
Title: 'Capítulo 5: Seguridad de clientes Windows XP independientes'
ms:assetid: 'a134d1cb-2ad1-4549-99c8-2a5e0128f2dc'
ms:contentKeyID: 20200279
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163078(v=TechNet.10)'
---

Guía de seguridad de Windows XP
===============================

### Capítulo 5: Seguridad de clientes Windows XP independientes

Actualizado: 20/10/05

##### En esta página

[](#eeaa)[Información general](#eeaa)
[](#edaa)[Windows XP en un dominio Windows NT 4.0](#edaa)
[](#ecaa)[Configuración del objeto de directiva de grupo local](#ecaa)
[](#ebaa)[Importación de plantillas de seguridad a Windows XP](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Información general

Los equipos basados en Microsoft® Windows® XP Profesional que no son miembros de un dominio basado en el servicio de directorio de Active Directory® presentan algunos retos únicos en cuanto a administración. En este capítulo se analiza cómo aplicar y administrar de forma más eficaz la configuración de directiva recomendada en los capítulos anteriores de esta guía. La configuración de directiva recomendada ayudará a proteger los equipos de escritorio y portátiles independientes de la organización en los que se ejecuta Windows XP Professional. La configuración se aplica mediante la directiva local, que es válida para todos los usuarios que inician sesión en el equipo cliente, incluido el administrador local.

Este capítulo no incluye una orientación sobre todas las configuraciones de directiva disponibles en Windows XP. Sin embargo, la configuración de directiva recomendada ofrecerá un entorno operativo seguro para la mayoría de las amenazas actuales, además de permitir a los usuarios continuar utilizando sus equipos. Cualquier configuración de directiva que se aplique debe basarse en los objetivos de seguridad de su organización.

[](#mainsection)[Principio de la página](#mainsection)

### Windows XP en un dominio Windows NT 4.0

Un ejemplo específico de un equipo cliente Windows XP en un entorno de dominio que no sea Active Directory sería un equipo con Windows XP en un dominio Microsoft Windows NT® 4.0. En un entorno de este tipo, los clientes Windows XP se tratan como equipos independientes. La carga de administración en este tipo de entorno es superior, ya que no existe una ubicación central desde la que administrar la configuración de directiva. Microsoft recomienda instalar los controladores de dominio basados en Windows NT 4.0 con el Service Pack 6a (SP6a) y las actualizaciones más recientes. Windows NT 4.0 SP6a contiene varias actualizaciones para la autenticación en NTLM. Sin estas actualizaciones, los equipos basados en Windows XP de un dominio Windows NT 4.0 podrían experimentar problemas de comunicación y de conectividad de red o dominio. El administrador debería comprobar con frecuencia la existencia de nuevas actualizaciones.

Windows XP Professional proporciona más configuraciones de directiva que las versiones anteriores de Windows, lo que permite personalizar mejor la configuración de los equipos y usuarios. Ofrece cientos de nuevos parámetros de configuración de directiva, además de los que ya estaban disponibles para Windows 2000 Professional. La directiva local es una eficaz característica de administración que permite bloquear y ajustar los equipos de escritorio. También admite la posibilidad de contar con muchos escenarios personalizados. Los administradores de dominio son miembros del grupo de **administradores** locales en todos los equipos cliente unidos al dominio; por tanto, la seguridad de los equipos cliente Windows XP estará determinada por el dominio al que pertenezcan.

Los equipos cliente Windows XP de un entorno heredado utilizan una versión modificada de las plantillas de seguridad descritas en el capítulo 3, "Configuración de seguridad para clientes Windows XP", para garantizar que se pueden comunicar con los controladores de dominio de Windows NT 4.0. Estas configuraciones de directiva se aplican mediante las secuencias de comandos que se describen al final de este capítulo.

Para comunicarse con un controlador de dominio Windows NT 4.0, se modifican las siguientes configuraciones de directiva que se encuentran en **Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\Opciones de seguridad**:

-   **Miembro de dominio: requerir clave de sesión protegida (Windows 2000 o más reciente) - Deshabilitado**

-   **Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (siempre) - Deshabilitado**

Estos parámetros de directiva están preconfigurados en los archivos de las plantillas de seguridad de cliente heredado que se incluyen con la guía.

[](#mainsection)[Principio de la página](#mainsection)

### Configuración del objeto de directiva de grupo local

Cada sistema operativo Windows XP Professional dispone de un objeto de directiva de grupo local (LGPO). La configuración de directiva se aplica al objeto LGPO de forma manual mediante el Editor de objetos de directiva de grupo o con secuencias de comandos. Los objetos LGPO contienen menos parámetros de configuración de directiva que los GPO basados en dominios, especialmente los que se encuentran en Configuración de seguridad. Los LGPO no son compatibles con Redireccionamiento de carpetas, Servicios de instalación remota o la instalación de software de directiva de grupo si se configuran como equipos cliente independientes, aunque puede usarlos para proporcionar un entorno operativo seguro en esos equipos.

En la siguiente tabla se muestran las extensiones de complemento de Directiva de grupo que se abren cuando este complemento se centra en un LGPO.

**Tabla 5.1 Extensiones del complemento de directiva de grupo**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Extensión del complemento de directiva de grupo</th>
<th style="border:1px solid black;" >Disponible en LGPO</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Instalación de software</td>
<td style="border:1px solid black;">No</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Secuencias de comandos</td>
<td style="border:1px solid black;">Sí</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Configuración de seguridad</td>
<td style="border:1px solid black;">Sí</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Plantillas administrativas</td>
<td style="border:1px solid black;">Sí</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Redireccionamiento de carpetas</td>
<td style="border:1px solid black;">No</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Mantenimiento de Internet Explorer</td>
<td style="border:1px solid black;">Sí</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servicios de instalación remota</td>
<td style="border:1px solid black;">No</td>
</tr>
</tbody>
</table>
  
#### Directivas de cuentas
  
Entre las directivas de cuentas se incluyen las configuraciones Directiva de contraseñas, Directiva de bloqueo de cuentas y Directiva Kerberos. La directiva de contraseñas puede ayudar a proteger la mayoría de los entornos gracias a su capacidad de requerir complejidad y cambio frecuente de las contraseñas. La directiva de bloqueo de cuentas permite deshabilitar automáticamente una cuenta después de varios intentos erróneos de inicio de sesión. La configuración de la directiva Kerberos determina los atributos relacionados con Kerberos, como **Vigencia máxima del vale de servicio** y **Forzar restricciones de inicio de sesión de usuario**. Sin embargo, estas configuraciones de directiva no se utilizan para los equipos cliente independientes, ya que no forman parte de un dominio.
  
Normalmente, las directivas de cuentas se establecen en el nivel de dominio y, por lo tanto, se configuran para los equipos cliente de dominio. En el caso de los equipos cliente Windows XP independientes, estas configuraciones de directiva deben aplicarse localmente, de forma similar a la configuración local que se describe en el capítulo 2, "Configuración de la infraestructura de dominios de Active Directory", de esta guía.
  
#### Directivas locales
  
Las directivas locales, en **Configuración del equipo\\Configuración de Windows\\Configuración de seguridad**, se aplicarán al equipo cliente mediante las plantillas que se describen en el capítulo 3, "Configuración de seguridad para clientes Windows XP", de esta guía. Se utiliza una combinación de esas plantillas y de las creadas para los equipos cliente independientes; puede automatizar la aplicación de las plantillas de seguridad mediante secuencias de comandos que puede aplicar a varios equipos del entorno. En la siguiente sección se describe el proceso de creación e implementación de directivas locales.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Importación de plantillas de seguridad a Windows XP
  
Hay varias plantillas que puede usar para configurar el equipo cliente independiente mediante una secuencia de comandos; debe usar una plantilla compatible con los requisitos de seguridad del cliente. En la sección anterior hemos tratado las configuraciones de directiva local y la forma en la que se utiliza el Editor de objetos de directiva de grupo para establecerlas. Puede utilizar las plantillas proporcionadas para automatizar el proceso de configuración para muchos equipos cliente en un entorno de equipos conectados en red o de equipos independientes. En esta sección se explicará el proceso de automatización de la configuración de las directivas de seguridad.
  
#### Configuración
  
Una plantilla de seguridad es un archivo que representa una configuración de seguridad. Para aplicar plantillas de seguridad a un equipo local, puede importarlas al LGPO. Las plantillas creadas en el capítulo 3, "Configuración de seguridad para clientes Windows XP", se utilizarán para configurar las directivas locales. El administrador utilizará los complementos Configuración y análisis de seguridad y Plantillas de seguridad de Microsoft Management Console (MMC), así como Secedit.exe, para crear las directivas de cuentas y combinar las dos plantillas de seguridad en el equipo independiente.
  
##### Creación de una base de datos de seguridad
  
Para automatizar el proceso de importación de la configuración de seguridad en un equipo cliente independiente, deberá crear una base de datos de referencia para escribir la directiva de seguridad local. La base de datos de línea de base se creó con el complemento Configuración y análisis de seguridad de MMC. Se siguieron los pasos que se indican a continuación para crear la base de datos XP Default Security.sdb. En esta base de datos se utilizó Setup security.inf como plantilla para establecer la configuración de directiva predeterminada para el equipo cliente independiente.
  
**Para crear una nueva base de datos de seguridad predeterminada**
  
1.  En el menú **Inicio**, haga clic en **Ejecutar**, escriba **mmc** y, a continuación, haga clic en **Aceptar**.
  
2.  En el menú **Archivo**, haga clic en **Nuevo** para crear una nueva consola.
  
3.  En el menú **Archivo**, haga clic en **Agregar o quitar complemento**. A continuación, haga clic en la ficha **Independiente** en el cuadro de diálogo de **propiedadesAgregar o quitar complemento** y haga clic en **Agregar**.
  
4.  Seleccione **Configuración y análisis de seguridad**, haga clic en **Agregar**, seleccione **Cerrar** y, a continuación, haga clic en **Aceptar**.
  
5.  Haga clic con el botón secundario del mouse en el elemento **Configuración y análisis de seguridad** y, a continuación, seleccione **Abrir base de datos**.
  
6.  Escriba un nuevo nombre de base de datos (XP Default Security) y, a continuación, haga clic en **Abrir**.
  
7.  Seleccione la plantilla de seguridad que desea importar (**setup security.inf**) y, a continuación, haga clic en **Abrir**.
  
8.  Haga clic con el botón secundario del mouse en el elemento **Configuración y análisis de seguridad** y, a continuación, haga clic en **Configurar el equipo ahora**.
  
9.  En el cuadro de diálogo **Configurar el sistema**, escriba el nombre del archivo de registro que desea utilizar y, a continuación, haga clic en **Aceptar**.
  
Este proceso crea un archivo de base de datos con la configuración de seguridad predeterminada que se utilizará en el proceso de automatización. Copie la base de datos de seguridad a la misma carpeta en la que haya copiado las secuencias de comandos y los archivos de información. Las secuencias de comandos personalizadas se utilizarán para configurar la base de datos, que establecerá la directiva de seguridad local. El administrador puede seguir un procedimiento similar para crear una base de datos personalizada en lugar de utilizar la que se proporciona con esta guía.
  
##### Creación de plantillas personalizadas
  
Puede utilizar el complemento Plantillas de Seguridad de MMC para definir la configuración de directiva de seguridad en las plantillas y después aplicarlas a un equipo local. A continuación se indican los pasos que se siguieron para crear las plantillas Standalone-EC-Account.inf y Standalone-SSLF-Account.inf utilizando las configuraciones de directiva de las tablas de directivas de cuentas del capítulo 2, "Configuración de la infraestructura de dominios de Active Directory".
  
**Para crear una plantilla personalizada**
  
1.  En el menú **Inicio**, haga clic en **Ejecutar**, escriba **mmc** y, a continuación, haga clic en **Aceptar**.
  
2.  En el menú **Archivo**, haga clic en **Nuevo** para crear una nueva consola.
  
3.  En el menú **Archivo**, haga clic en **Agregar o quitar complemento**. A continuación, haga clic en la ficha **Independiente** en el cuadro de diálogo de **propiedadesAgregar o quitar complemento** y haga clic en **Agregar**.
  
4.  Haga clic en **Plantillas de seguridad**, seleccione **Agregar**, **Cerrar** y, a continuación, haga clic en **Aceptar**.
  
5.  Abra **Plantillas de seguridad**.
  
6.  Seleccione la carpeta predeterminada en la que desea almacenar la nueva plantilla y, a continuación, haga clic en **Nueva plantilla**.
  
7.  En el cuadro de texto **Nombre de plantilla**, escriba el nombre de la nueva plantilla de seguridad.
  
8.  En el cuadro de texto **Descripción**, escriba la descripción de la nueva plantilla de seguridad y, a continuación, haga clic en **Aceptar**.
  
9.  En el árbol de consola, haga doble clic en la nueva plantilla de seguridad para mostrar las áreas de seguridad y, a continuación, navegue hasta que los parámetros de directiva que desea configurar aparezcan en el panel de detalles.
  
10. En el panel de detalles, haga clic con el botón secundario del mouse en la configuración de seguridad que desee establecer y, a continuación, haga clic en **Propiedades**.
  
11. En el cuadro de diálogo **Propiedades**, active la casilla de verificación **Definir esta configuración de la directiva en la plantilla**, modifique la configuración y, a continuación, haga clic en **Aceptar**.
  
Una vez creados los archivos, podrá encontrarlos en **%windir%\\security\\templates**. Copie las plantillas de seguridad en la misma carpeta en la que creó la base de datos de seguridad para ejecutar las secuencias de comandos. Estos archivos se utilizarán en la siguiente fase para automatizar la importación de las plantillas.
  
#### Aplicación de la directiva
  
La herramienta Secedit.exe es útil cuando es necesario configurar la seguridad en varios equipos. Puede llamar a la herramienta Secedit.exe en una ventana del símbolo del sistema, desde un archivo por lotes o desde el programador de tareas automático para crear y aplicar las plantillas de forma automática. También puede ejecutarla de forma dinámica desde un símbolo del sistema. Las secuencias de comandos proporcionadas en esta guía emplean la herramienta Secedit.exe para combinar y aplicar la directiva local a los equipos cliente.
  
##### Aplicación manual de la directiva local
  
Para aplicar toda la configuración de directiva del archivo .inf de la plantilla de seguridad para equipos independientes que se incluye en esta guía, use el complemento Configuración y análisis de seguridad de MMC en lugar del complemento Directiva de equipo local. No es posible importar la plantilla de seguridad con el complemento Directiva de equipo local porque no le permite aplicar la configuración de directiva de seguridad para los servicios del sistema.
  
Para importar y aplicar la plantilla de seguridad, utilice el complemento Configuración y análisis de seguridad con el fin de seguir los pasos de los siguientes procedimientos.
  
**Para importar una plantilla de seguridad**
  
1.  Inicie el complemento Configuración y análisis de seguridad de MMC.
  
2.  Haga clic con el botón secundario en el elemento **Configuración y análisis de seguridad**.
  
3.  Haga clic en **Abrir base de datos**.
  
4.  Escriba un nuevo nombre de base de datos y, a continuación, haga clic en **Abrir**.
  
5.  Seleccione la nueva plantilla de seguridad (archivo .inf) que desea importar y, a continuación, haga clic en **Abrir**.
  
Se importará toda la configuración de directiva de la plantilla, que podrá revisar o aplicar a partir de ese momento.
  
**Para aplicar la configuración de directiva**
  
1.  Haga clic con el botón secundario en el elemento **Configuración y análisis de seguridad**.
  
2.  Seleccione **Configurar el equipo ahora**.
  
3.  En el cuadro de diálogo **Configurar el equipo ahora**, escriba el nombre del archivo de registro que desea utilizar y, a continuación, haga clic en **Aceptar**.
  
Deberá importar ambas plantillas para cada entorno. Se aplicará toda la configuración de directiva pertinente de la plantilla de seguridad a la directiva local del equipo cliente. En las siguientes secciones se describe la configuración de directiva aplicada mediante la directiva local.
  
##### Secedit
  
Esta herramienta configura y analiza la seguridad del sistema; para ello, compara la configuración actual con al menos una plantilla. La sintaxis que se debe utilizar en la herramienta Secedit.exe es la siguiente:
  
**secedit /configure /db** *&lt;nombreDeArchivo&gt;* \[**/cfg** *&lt;nombreDeArchivo&gt;*\] \[**/overwrite**\]\[**/areas** *&lt;Área1&gt; &lt;Área2&gt;* ...\]  
**\[/log** *&lt;nombreDeArchivo&gt;*\] \[**/quiet**\]
  
En la lista siguiente se explican los parámetros de la herramienta Secedit.exe.
  
-   **/db** *&lt;nombreDeArchivo&gt;*. Especifica la base de datos utilizada para realizar la configuración de seguridad.
  
-   **/cfg** *&lt;nombreDeArchivo&gt;*. Especifica la plantilla de seguridad que se va a importar a la base de datos antes de configurar el equipo. Las plantillas de seguridad se crean utilizando el complemento Plantillas de seguridad.
  
-   **/overwrite**. Especifica que se debe vaciar la base de datos antes de importar la plantilla de seguridad. Si no se especifica este parámetro, la configuración de directiva de la plantilla de seguridad se acumulará en la base de datos. Si este parámetro no se especifica y hay conflictos entre la configuración de directiva de la plantilla que desea importar y la configuración de directiva existente en la base de datos, se aplicará la configuración de la plantilla.
  
-   **/areas** *&lt;Área1&gt;* *&lt;Área2&gt;*. Especifica las áreas de seguridad que se van a aplicar al sistema. Si no se especifica este parámetro, se aplicará al sistema la configuración de directiva de seguridad definida en la base de datos. Para configurar varias áreas, separe cada una de ellas con un espacio. En la tabla siguiente se muestran las áreas de seguridad que se admiten.
  
    **Tabla 5.2 Áreas de seguridad**

 
    <p> </p>
<table style="border:1px solid black;">
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th style="border:1px solid black;" >Nombre de área</th>
    <th style="border:1px solid black;" >Descripción</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td style="border:1px solid black;">SECURITYPOLICY</td>
    <td style="border:1px solid black;">Incluye directivas de cuentas, directivas de auditoría, configuración del registro de eventos y opciones de seguridad.</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">GROUP_MGMT</td>
    <td style="border:1px solid black;">Incluye la configuración de grupo restringido.</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">USER_RIGHTS</td>
    <td style="border:1px solid black;">Incluye la configuración de asignación de derechos de usuario.</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">REGKEYS</td>
    <td style="border:1px solid black;">Incluye permisos del Registro.</td>
    </tr>
    <tr class="odd">
    <td style="border:1px solid black;">FILESTORE</td>
    <td style="border:1px solid black;">Incluye permisos del sistema de archivos.</td>
    </tr>
    <tr class="even">
    <td style="border:1px solid black;">SERVICES</td>
    <td style="border:1px solid black;">Incluye la configuración del servicio del sistema.</td>
    </tr>
    </tbody>
    </table>
  
-   **/log** *&lt;nombreDeArchivo&gt;*. Especifica un archivo que se utiliza para registrar el estado del proceso de configuración. Si no se especifica, los datos de configuración se registran en el archivo Scesrv.log, ubicado dentro del directorio **%windir%\\security\\logs**.
  
-   **/quiet**. Especifica que el proceso de configuración debe realizarse sin avisar al usuario.
  
##### Secuencias de comandos automatizadas
  
Siempre resulta más fácil utilizar una secuencia de comandos para aplicar la misma configuración de directiva a un gran número de equipos cliente. Puede utilizar la herramienta Secedit.exe descrita anteriormente en este capítulo para automatizar la aplicación de la directiva local con una secuencia de comandos sencilla. Copie la secuencia de comandos y todos los archivos asociados en un subdirectorio del disco duro local y, a continuación, ejecute la secuencia de comandos desde el subdirectorio.
  
Puede utilizar la siguiente secuencia de comandos para importar plantillas de seguridad en el LGPO con el fin de garantizar la seguridad de los equipos cliente Windows XP independientes de su entorno.
  
**Importante**: asegúrese de que el archivo de la base de datos de seguridad, **XP Default Security.sdb**, no está marcado como de sólo lectura. Para que la siguiente secuencia de comandos funcione correctamente, es necesario que se puedan realizar cambios en ese archivo.
  
```  
 REM (c) Microsoft Corporation 1997-2005 REM Script for Securing Stand-Alone Windows XP Client Computers REM REM Name:        Standalone-EC-Desktop.cmd REM Version: 2.0 REM This CMD file provides the proper secedit.exe syntax for importing REM the security policy for a secure stand-alone Windows XP desktop REM client computer. Please read the entire guide before using this REM CMD file. REM Resets the Policy to Default Values secedit.exe /configure /cfg %windir%\\repair\\secsetup.inf /db secsetup.sdb /verbose REM Sets the Account Settings secedit.exe /configure /db "XP Default Security.sdb" /cfg "Standalone-EC-Account.inf" /overwrite /quiet REM Sets the Security Settings secedit.exe /configure /db "XP Default Security.sdb" /cfg "EC-Desktop.inf" REM Deletes the Shared Folder reg delete "HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Explorer\\ MyComputer\\NameSpace\\DelegateFolders\\ {59031a47-3f72-44a7-89c5-5595fe6b30ee}" /f REM Updates the Local Policy gpupdate.exe /force   
```  
En las siguientes tablas se incluye una lista de las secuencias de comandos y los archivos asociados que se incluyen en esta guía. Para cada entorno, hay archivos tanto para equipos cliente de escritorio como equipos cliente portátiles.
  
**Tabla 5.3 Secuencias de comandos y archivos para equipos cliente independientes**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombres de las secuencias de comandos y los archivos</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Standalone-EC-Desktop.cmd</td>
<td style="border:1px solid black;">Secuencia de comandos para equipos cliente independientes que se utiliza para establecer la directiva de Cliente de empresa en equipos cliente de escritorio.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Standalone-EC-Laptop.cmd</td>
<td style="border:1px solid black;">Secuencia de comandos para equipos cliente independientes que se utiliza para establecer la directiva de Cliente de empresa en equipos cliente portátiles.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Standalone-SSLF-Desktop.cmd</td>
<td style="border:1px solid black;">Secuencia de comandos para equipos cliente independientes que se utiliza para establecer la directiva de Seguridad especializada: Funcionalidad limitada en equipos cliente de escritorio.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Standalone-SSLF-Laptop.cmd</td>
<td style="border:1px solid black;">Secuencia de comandos para equipos cliente independientes que se utiliza para establecer la directiva de Seguridad especializada: Funcionalidad limitada en equipos cliente portátiles.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Standalone-EC-Account.inf</td>
<td style="border:1px solid black;">Plantilla de la directiva de cuentas para el entorno Cliente de empresa.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Standalone-SSLF-Account.inf</td>
<td style="border:1px solid black;">Plantilla de la directiva de cuentas para el entorno Seguridad especializada: Funcionalidad limitada.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">EC-Desktop.inf</td>
<td style="border:1px solid black;">Plantilla de seguridad para los equipos cliente de escritorio del entorno Cliente de empresa.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">EC-Laptop.inf</td>
<td style="border:1px solid black;">Plantilla de seguridad para los equipos cliente portátiles del entorno Cliente de empresa.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SSLF-Desktop.inf</td>
<td style="border:1px solid black;">Plantilla de seguridad para los equipos cliente de escritorio del entorno Seguridad especializada: Funcionalidad limitada.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SSLF-Laptop.inf</td>
<td style="border:1px solid black;">Plantilla de seguridad para los equipos cliente portátiles del entorno Seguridad especializada: Funcionalidad limitada.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">XP Default Security.sdb</td>
<td style="border:1px solid black;">Base de datos de directiva predeterminada.</td>
</tr>
</tbody>
</table>
  
**Tabla 5.4 Secuencias de comandos y archivos para equipos heredados**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombres de las secuencias de comandos y los archivos</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Legacy-EC-Desktop.cmd</td>
<td style="border:1px solid black;">Secuencia de comandos para equipos heredados que se utiliza para establecer la directiva de Cliente de empresa en equipos cliente de escritorio.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Legacy-EC-Laptop.cmd</td>
<td style="border:1px solid black;">Secuencia de comandos para equipos heredados que se utiliza para establecer la directiva de Cliente de empresa en equipos cliente portátiles.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Legacy-SSLF-Desktop.cmd</td>
<td style="border:1px solid black;">Secuencia de comandos para equipos heredados que se utiliza para establecer la directiva de Seguridad especializada: Funcionalidad limitada en equipos cliente de escritorio.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Legacy-SSLF-Laptop.cmd</td>
<td style="border:1px solid black;">Secuencia de comandos para equipos heredados que se utiliza para establecer la directiva de Seguridad especializada: Funcionalidad limitada en equipos cliente portátiles.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Legacy-EC-Account.inf</td>
<td style="border:1px solid black;">Plantilla de directiva de cuentas de empresa para equipos heredados.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Legacy-SSLF-Account.inf</td>
<td style="border:1px solid black;">Plantilla de directiva de cuentas del entorno Seguridad especializada: Funcionalidad limitada para equipos heredados.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Legacy-EC-Desktop.inf</td>
<td style="border:1px solid black;">Plantilla de seguridad para los equipos cliente de escritorio heredados del entorno Cliente de empresa.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Legacy-EC-Laptop.inf</td>
<td style="border:1px solid black;">Plantilla de seguridad para los equipos cliente portátiles heredados del entorno Cliente de empresa.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Legacy-SSLF-Desktop.inf</td>
<td style="border:1px solid black;">Plantilla de seguridad para los equipos cliente de escritorio heredados del entorno Seguridad especializada: Funcionalidad limitada.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Legacy-SSLF-Laptop.inf</td>
<td style="border:1px solid black;">Plantilla de seguridad para los equipos cliente portátiles heredados del entorno Seguridad especializada: Funcionalidad limitada.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">XP Default Security.sdb</td>
<td style="border:1px solid black;">Base de datos de directiva predeterminada.<br />
<strong>Nota:</strong> asegúrese de que la base de datos tiene privilegios de escritura. No se puede establecer como de sólo lectura.</td>
</tr>
</tbody>
</table>
 

[](#mainsection)[Principio de la página](#mainsection)

### Resumen

La directiva local de Windows XP es una forma muy útil de proporcionar una configuración de directiva de seguridad coherente en los sistemas Windows XP que no son miembros de un dominio de Active Directory. Para implementar la directiva local de forma eficaz, asegúrese de que conoce el proceso de aplicación y compruebe que todos los equipos cliente se han configurado con los parámetros correctos y que ha definido un nivel de seguridad adecuado para cada equipo del entorno.

#### Información adicional

Los siguientes vínculos proporcionan información adicional acerca de temas relacionados con la seguridad en Windows XP Professional.

-   Para obtener más información acerca del [Administrador de configuración de seguridad](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/74d8fed6-cf2f-4ba4-94f3-fc95bad914b0.mspx), visite www.microsoft.com/technet/prodtechnol/windowsserver2003/library/ServerHelp/
    74d8fed6-cf2f-4ba4-94f3-fc95bad914b0.mspx.

-   Para obtener más información acerca de la [directiva de grupo de Windows Server 2003](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/featured/gp/default.mspx), visite www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/
    featured/gp/default.mspx.

-   Para obtener información acerca de la solución de problemas relacionados con la directiva de grupo en Windows Server, consulte las notas del producto sobre [solución de problemas de la directiva de grupo en Microsoft Windows Server](http://www.microsoft.com/downloads/details.aspx?familyid=b24bf2d5-0d7a-4fc5-a14d-e91d211c21b2&displaylang=en) en
    www.microsoft.com/downloads/details.aspx?FamilyId=B24BF2D5-0D7A-4FC5-A14D-E91D211C21B2 (en inglés).

-   Para obtener más información sobre la [solución de problemas relacionados con la aplicación de la directiva de grupo](http://support.microsoft.com/default.aspx?scid=250842), consulte el artículo de Knowledge Base 250842 en http://support.microsoft.com/default.aspx?scid=250842.

-   Para obtener más información sobre las [herramientas de seguridad](http://www.microsoft.com/technet/security/tools/) y las listas de comprobación, visite www.microsoft.com/technet/security/tools/ (en inglés).

-   Para obtener más información sobre [cómo identificar objetos de directiva de grupo en Active Directory y SYSVOL](http://support.microsoft.com/default.aspx?scid=216359), consulte el artículo de Knowledge Base 216359 en http://support.microsoft.com/default.aspx?scid=216359.

-   Para obtener más información acerca de la [función de las plantillas administrativas](http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/adminad.mspx), visite la página web en www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/auth\_eap.mspx (en inglés).

[](#mainsection)[Principio de la página](#mainsection)

##### Descargar

[![](images/Cc163078.icon_exe(es-es,TechNet.10).gif)Descargar la Guía de seguridad de Windows XP](http://go.microsoft.com/fwlink/?linkid=14840)
