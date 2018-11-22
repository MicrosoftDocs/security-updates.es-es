---
TOCTitle: 'Paso 1: confirmar los requisitos de instalación de WSUS 3.0 SP2'
Title: 'Paso 1: confirmar los requisitos de instalación de WSUS 3.0 SP2'
ms:assetid: 'ec01bd75-5def-4899-8cee-ddab827bbd83'
ms:contentKeyID: 21741450
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd939916(v=WS.10)'
---

Paso 1: confirmar los requisitos de instalación de WSUS 3.0 SP2
===============================================================

Antes de instalar o actualizar Windows Server Upgrade Services 3.0 Service Pack 2 (WSUS 3.0 SP2), debe confirmar que tanto el servidor como los equipos cliente cumplen con los requisitos del sistema WSUS 3.0 SP2 y que posee los permisos necesarios para completar la instalación.

Requisitos del hardware y software del servidor para la instalación de WSUS 3.0 SP2
-----------------------------------------------------------------------------------

1.  Confirme que el servidor cumple con los requisitos del sistema WSUS 3.0 SP2 para hardware, sistema operativo y otro software solicitado. Los requisitos del sistema se enumeran en las Notas de la versión de WSUS 3.0 SP2 en [http://go.microsoft.com/fwlink/?LinkId=139840](http://go.microsoft.com/fwlink/?linkid=139840). Si está usando el Administrador del servidor para instalar WSUS 3.0 SP2 Server, puede confirmar que cumple con los requisitos del software siguiendo los pasos de la sección "Preparando la instalación de WSUS 3.0 SP2".
2.  Si instala las funciones o actualizaciones de software que requieren reiniciar el servidor cuando la instalación finalice, reinicie el servidor antes de instalar WSUS 3.0 SP2.

Requisitos de software del cliente
----------------------------------

Actualizaciones automáticas es el cliente de WSUS 3.0. Actualizaciones automáticas no tiene más requisitos de hardware que estar conectado a la red.

1.  Confirme que el equipo en el que está instalando Actualizaciones automáticas cumple con los requisitos del sistema WSUS 3.0 SP2 para equipos cliente. Los requisitos del sistema se enumeran en las Notas de la versión de WSUS 3.0 SP2 en [http://go.microsoft.com/fwlink/?LinkId=139840](http://go.microsoft.com/fwlink/?linkid=139840).
2.  Si instala actualizaciones de software que solicitan el reinicio del equipo, reinícielo antes de instalar WSUS 3.0 SP2.

Permisos
--------

Los siguientes permisos se solicitan para directorios y usuarios específicos:

1.  La cuenta de NT Authority\\Network Service debe tener permiso de Control total para las siguientes carpetas con el fin de mostrar correctamente el complemento de administración de WSUS:
    -   %windir%\\Microsoft .NET\\Framework\\v2.0.50727\\Temporary ASP.NET Files
    -   %windir%\\Temp
2.  Confirme que la cuenta que piensa utilizar para la instalación de WSUS 3.0 SP2 es miembro del grupo de administradores local.

Preparar la instalación de WSUS 3.0 SP2
---------------------------------------

Si está ejecutando Windows 7 o Windows Server 2008 SP2, puede instalar WSUS 3.0 SP2 desde el Administrador del servidor. Si utiliza otro sistema operativo compatible o sólo instala la consola de administración de WSUS, vaya a la siguiente sección de la guía para instalar WSUS 3.0 SP2 mediante el archivo WUSSetup.exe.

**Para preparar la instalación de WSUS 3.0 SP2 Server a través del Administrador del servidor**
1.  Inicie sesión en el servidor en el que va a instalar WSUS 3.0 SP2 utilizando una cuenta que sea miembro del grupo de administradores local.

2.  Haga clic en **Inicio**, seleccione **Herramientas administrativas** y, a continuación, haga clic en **Administrador del servidor**.

3.  En el panel del lateral derecho de la ventana del Administrador del servidor, en la sección Resumen de funciones, haga clic en **Agregar funciones**.

4.  Si aparece la página Antes de comenzar, haga clic en **Siguiente**.

5.  En la página Seleccionar funciones de servidor, confirme que están seleccionados **Servidor de aplicaciones** y **Servidor web (IIS)**. Si se han seleccionado, utilice el resto de este paso para confirmar que los servicios de función necesarios están seleccionados. De lo contrario, instale el Servidor de aplicaciones y el Servidor web (IIS) como se indica a continuación.

    1.  En la página Seleccionar funciones de servidor, seleccione **Servidor de aplicaciones** y **Servidor web (IIS)**. Haga clic en **Siguiente**.
    2.  Si está instalando los Servicios de función de aplicaciones, haga clic en **Siguiente** en la página Servidor de aplicaciones. En la página de Servicios de función de servidor de aplicaciones, acepte la configuración predeterminada y, a continuación, haga clic en **Siguiente**.
    3.  Si está instalando el Servidor web de IIS, haga clic en **Siguiente** en la página del Servidor web (IIS). En la página de Servicios de función de servidor web (IIS), además de la configuración predeterminada, seleccione **ASP.NET**, **Autenticación de Windows**, **Compresión de contenido dinámico** y **Compatibilidad con la administración de IIS 6**. Si aparece la ventana Asistente para agregar funciones, haga clic en **Agregar servicios de función requeridos**. Haga clic en **Siguiente**.
    4.  En la página Confirmar selecciones de instalación, haga clic en **Instalar**.
    5.  En la página de Resultados de la instalación, confirme que aparece un mensaje de "Instalación correcta” para los servicios de función que haya instalado en este paso y haga clic en **Cerrar**.

Paso siguiente
--------------

[Paso 2: instalar la consola de administración o el servidor WSUS](https://technet.microsoft.com/6db6fcb0-c55d-43b9-9b07-4040c6267759)

Recursos adicionales
--------------------

[Guía paso a paso para Windows Server Update Services 3.0 SP2](https://technet.microsoft.com/4b504edc-93b3-45b0-a7e8-d0107f1a4442)
