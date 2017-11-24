---
TOCTitle: Cómo implementar el cliente de RMS
Title: Cómo implementar el cliente de RMS
ms:assetid: 'c84f1724-cf71-4385-9003-ff68bc23c927'
ms:contentKeyID: 18127945
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747749(v=WS.10)'
---

Cómo implementar el cliente de RMS
==================================

Si utiliza Microsoft Windows XP o Microsoft Windows 2000, el cliente de los Servicios de Rights Management (RMS) debe instalarse primero para poder utilizar cualquiera de las características de RMS, como la administración de permisos de acceso a la información en Microsoft® Office System 2003 y el Complemento Rights Management para Internet Explorer. El cliente RMS está integrado en Windows Vista®.

Muchas organizaciones prefieren controlar la implementación del software de cliente en su organización. Se pueden utilizar Systems Management Server (SMS) o la directiva de grupo para implementar el cliente RMS con Service Pack 2 (SP2).

Antes de comenzar la implementación, visite [http://go.microsoft.com/fwlink/?LinkId=67736](http://go.microsoft.com/fwlink/?linkid=67736) para descargar el cliente de RMS.

> [!IMPORTANT]
> El cliente RMS está integrado en Windows Vista. Por tanto, ya no es necesaria una instalación independiente. 

Extracción de los archivos de instalación
-----------------------------------------

Tras descargar el archivo WindowsRightsManagementServicesSP2-KB917275-Client-ENU.exe, debe extraer los archivos de Microsoft® Windows® Installer del paquete ejecutable.

Para ello, puede utilizar el siguiente comando desde el símbolo del sistema:

```
WindowsRightsManagementServicesSP2-KB917275-Client-ENU.exe /x <path>
```

donde &lt;ruta&gt; es el directorio de destino en que desea colocar los archivos extraídos.

Al ejecutar este comando se extraen los siguientes archivos al directorio de destino especificado:

-   Bootstrap.exe
    Se trata de un archivo contenedor que el archivo ejecutable utiliza para instalar los demás archivos incluidos. No se utiliza cuando se instala el cliente RMS con SP2 utilizando SMS o la directiva de grupo.
-   MSDrmClient.msi
    Es el archivo de instalación del cliente de RMS con SP2. Esta instalación desinstala cualquier versión anterior del cliente de RMS que haya en el equipo. Este programa debe instalarse primero en los equipos cliente.
-   RMClientBackCompat.msi
    Es el archivo de instalación que identifica el nuevo cliente RMS para aplicaciones compatibles con RMS (como Microsoft Office Professional 2003 o 2007 Microsoft Office system) que dependen de la versión anterior del cliente RMS, de forma que el cliente RMS con SP2 puede utilizarse en su lugar. Este programa debe instalarse en los equipos cliente después de haber instalado correctamente MSDrmClient.msi.

> [!NOTE]
> Independientemente del método de instalación que decida implementar, asegúrese de que los dos archivos de Windows Installer se instalan correctamente. Si se produce un error que impide la instalación de MSDrmClient.msi, no instale RMClientBackCompat.msi. 

Implementación del cliente RMS con una instalación desatendida
--------------------------------------------------------------

La extracción de los archivos para instalar los archivos de Windows Installer es opcional. También puede implementar el cliente RMS con un método de instalación desatendida. Para ello, puede utilizar el siguiente comando desde el símbolo del sistema:

```
WindowsRightsManagementServicesSP2-KB917275-Client-ENU.exe -override 1 /I MsDrmClient.msi REBOOT=ReallySuppress /q -override 2 /I RmClientBackCompat.msi REBOOT=ReallySuppress /q
```

Este comando inicia la instalación desatendida en el cliente RMS.

> [!NOTE]
> Dado que se trata de una instalación desatendida, el instalador no le informa cuando se completa la instalación. Las instalaciones desatendidas se suelen ejecutar en un archivo por lotes o en una secuencia de comandos. 

Implementación del cliente de RMS con SMS
-----------------------------------------

**Para implementar el cliente de RMS utilizando SMS**
1.  Abra la consola de administrador de SMS.

2.  Expanda la base de datos del sitio que desee utilizar.

3.  En el panel izquierdo, haga clic con el botón secundario en **Paquetes**, seleccione **Nuevo** y, a continuación, haga clic en **Package From Definition**.

4.  Cree paquetes a partir de los archivos MSDRMClient.msi y RMClientBackCompat.msi. Los paquetes deben tener las siguientes propiedades:

    **General**:

    -   En **Línea de comandos**, escriba lo siguiente:
        ```
        msiexec.exe /q ALLUSERS=2 /m MSIDGHOG /i "<file_name>.msi"
        ```
 
        | ![](images/Cc747749.note(WS.10).gif)Nota                                                                        |
        |----------------------------------------------------------------------------------------------------------------------------------------------|
        | MSIDGHOG es un valor aleatorio. Reemplace &lt;nombre\_archivo&gt; por el nombre del archivo de Windows Installer que instalará este paquete. |

    -   En **Ejecutar**, seleccione la opción **Oculto**.
    -   En **After running**, seleccione la opción **No action required**.
    -   En **Categoría**, seleccione la opción **Software de administración**.

    **Requisitos:**

    -   En **Espacio en disco estimado**, escriba **445 KB**.
    -   En **Tiempo de ejecución máximo permitido**, seleccione **Desconocido**.
    -   Seleccione la casilla de verificación **Este programa puede ejecutarse en cualquier plataforma**.

    **Entorno:**

    -   En **Puede ejecutar**, seleccione la opción **Tanto si un usuario inició sesión como si no**.
    -   En **Run mode**, seleccione la opción **Run with administrative rights**.
    -   En **Drive mode**, seleccione la opción **Runs with UNC name**.

    **Avanzadas:**

    -   Desactive la casilla de verificación **Ejecutar otro programa primero**.
    -   Desactive la casilla de verificación **Suprimir notificación de programa** en **Cuando el programa está asignado a un equipo**.
    -   Desactive la casilla de verificación **Deshabilitar este programa en los equipos donde se anuncia**.

5.  Defina la opción **Cuentas de acceso y puntos de distribución** según convenga a su organización.

6.  Cree un anuncio para la colección adecuada. En una implementación de SMS es recomendable utilizar un programa **Desatendido específico para cada sistema**.

7.  Programe este anuncio de acuerdo con las necesidades de su organización.

Implementación del cliente de RMS con la directiva de grupo
-----------------------------------------------------------

Puede utilizar la característica de instalación y mantenimiento de software de la directiva de grupo para implementar el cliente de RMS en los equipos de destino.

La directiva de grupo es el método recomendado para administrar activamente la implementación de los clientes de RMS en el caso de organizaciones pequeñas a medianas que no estén utilizando ya una solución de administración corporativa actualizada como Systems Management Server 2003.

Si utiliza la directiva de grupo para distribuir un programa, puede asignar dicho programa a equipos. El programa se instala cuando el equipo se inicia y está disponible para todos los usuarios que inicien sesión en el equipo. Para obtener más información sobre la directiva de grupo, consulte Diseño de una infraestructura de directivas de grupo (<http://go.microsoft.com/fwlink/?linkid=24328>). Este procedimiento requiere la utilización de la consola de administración de directivas de grupo (GPMC). Para descargar la GPMC, consulte Consola de administración de directivas de grupo con Service Pack 1 (<http://go.microsoft.com/fwlink/?linkid=21813>).

El siguiente procedimiento constituye una guía rápida para los administradores que no estén familiarizados con la distribución de software basada en directivas de grupo. Puede modificar estos pasos según convenga para adecuarse a las necesidades de su organización.

**Para implementar el cliente de RMS utilizando la directiva de grupo**
1.  En un controlador de dominio, abra el complemento de Microsoft Management Console (MMC) **Usuarios y equipos de Active Directory**.

2.  Cree una nueva unidad organizativa (UO) o seleccione una UO existente.

    Si ha creado una nueva UO, agregue los equipos en los que desee instalar el cliente de RMS.

3.  Haga clic con el botón secundario en la UO y seleccione **Propiedades**.

4.  Seleccione la ficha **Directiva de grupo**.

5.  Haga clic en **Nuevo** para crear un nuevo objeto de directiva de grupo (GPO).

6.  Haga clic en **Editar** para editar el nuevo GPO.

7.  En el árbol de la consola, expanda **Configuración del equipo, Configuración de software** y, a continuación, seleccione **Instalación de software**.

8.  Haga clic con el botón secundario en el panel de detalles, haga clic en **Nuevo** y, a continuación, en **Paquete**.

9.  Proporcione una ruta para el archivo MSDRMclient.msi en una carpeta compartida en red a la que tengan acceso los equipos cliente.

10. Haga clic en **Aceptar** para asignar el paquete.

11. Repita los pasos 5 a 10 para crear un GPO que instale el archivo RMClientBackCompat.msi.

> [!NOTE]
> Estos pasos se indican únicamente como orientación para los usuarios que no tienen experiencia en el uso de directivas de grupo. Si usted es un administrador de directivas de grupo con experiencia, puede seguir sus propios procedimientos operativos para distribuir el paquete MSDrmClient.msi. Además, estos pasos son los indicados para un controlador de dominio que ejecute Windows Server 2003; el proceso y la terminología pueden ser diferentes en un dominio de Windows 2000. 

Actualización desde una versión anterior
----------------------------------------

Se puede utilizar un método de instalación desatendida dentro de una secuencia de comandos que detectará si está instalado el cliente RMS con SP2. Si el cliente no está instalado, la secuencia de comandos actualiza el cliente existente o instala el cliente de RMS con SP2. La secuencia de comandos es la siguiente:  

```
Set objShell = Wscript.CreateObject("Wscript.Shell")
Set objWindowsInstaller = Wscript.CreateObject("WindowsInstaller.Installer") 
Set colProducts = objWindowsInstaller.Products 

For Each product In colProducts 
strProductName = objWindowsInstaller.ProductInfo (product, "ProductName")

if strProductName = "Windows Rights Management Client with Service Pack 2" then
strInstallFlag = "False"
Exit For
else
strInstallFlag = "True"
end if
Next

if strInstallFlag = "True" then
objShell.run "WindowsRightsManagementServicesSP2-KB917275-Client-ENU.exe -override 1 /I MsDrmClient.msi REBOOT=ReallySuppress /q -override 2 /I RmClientBackCompat.msi REBOOT=ReallySuppress /q "
else
wscript.echo "No installation required"
end if
```

> [!NOTE]
> Esta secuencia de comandos no funciona con Windows Vista porque el cliente RMS está integrado en el sistema operativo. 
