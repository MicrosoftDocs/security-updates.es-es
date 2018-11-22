---
TOCTitle: 'Paso 2: instalar la consola de administración o el servidor WSUS'
Title: 'Paso 2: instalar la consola de administración o el servidor WSUS'
ms:assetid: '6db6fcb0-c55d-43b9-9b07-4040c6267759'
ms:contentKeyID: 21741366
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd939859(v=WS.10)'
---

Paso 2: instalar la consola de administración o el servidor WSUS
================================================================

Tras asegurar que el servidor cumple con los requisitos mínimos del sistema y que se han otorgado los permisos de cuentas necesarios, ya está listo para instalar Windows Server Upgrade Services 3.0 Service Pack 2 (WSUS 3.0 SP2). Para comenzar la instalación de WSUS 3.0 SP2, utilice el procedimiento adecuado para su sistema operativo y el tipo de instalación (usando o bien el Administrador del servidor o el archivo WUSSetup.exe).

Si está utilizando el Administrador del servidor
------------------------------------------------

**Para comenzar la instalación de WSUS 3.0 SP2 Server a través del Administrador del servidor**
1.  Inicie sesión en el servidor en el que va a instalar WSUS 3.0 SP2 utilizando una cuenta que sea miembro del grupo de administradores local.

2.  Haga clic en **Inicio**, seleccione **Herramientas administrativas** y, a continuación, haga clic en **Administrador del servidor**.

3.  En el panel del lateral derecho de la ventana del Administrador del servidor, en la sección Resumen de funciones, haga clic en **Agregar funciones**.

4.  Si aparece la página Antes de comenzar, haga clic en **Siguiente**.

5.  En la página Seleccionar funciones de servidor, seleccione **Windows Server Update Services**.

6.  En la página Windows Server Update Services, haga clic en **Siguiente**.

7.  En la página Confirmar selecciones de instalación, haga clic en **Instalar**.

8.  Cuando se inicia el asistente para instalación de WSUS 3.0 SP2, salte a la siguiente sección y consulte el procedimiento de “Para continuar con la instalación de WSUS 3.0 SP2”.

Si está utilizando el archivo WUSSetup.exe
------------------------------------------

**Para iniciar la instalación de WSUS 3.0 PS2 Server o la consola de administración de WSUS 3.0 SP2 mediante el archivo WUSSetup.exe**
1.  Inicie sesión en el servidor en el que va a instalar WSUS 3.0 SP2 utilizando una cuenta que sea miembro del grupo de administradores local.

2.  Haga doble clic en el archivo del instalador **WSUSSetup.exe**.

3.  Cuando haya comenzado el asistente para instalación de Windows Server Update Services 3.0 SP2, consulte el procedimiento “Para continuar con la instalación de WSUS 3.0 SP2”.

Utilizando el asistente para instalación WSUS 3.0 SP2
-----------------------------------------------------

El asistente para instalación WSUS se inicia desde el Administrador del servidor o desde el archivo WUSSetup.exe.

**Para continuar con la instalación de WSUS 3.0 SP2**
1.  En la página de bienvenida del asistente para instalación de Windows Server Update Services 3.0, haga clic en **Siguiente**.

2.  En la página Selección del modo de instalación, seleccione **Instalación de servidor completa incluida la consola de administración** si desea instalar el servidor WSUS en este equipo o **solo la consola de administración** si desea instalar sólo la consola de administración.

3.  En la página Contrato de licencia, lea los términos del contrato de licencia con atención, haga clic en **Acepto los términos del Contrato de licencia** y, a continuación, haga clic en **Siguiente**.

4.  En la página Seleccionar origen de la actualización del asistente para instalación, puede especificar dónde obtienen las actualizaciones los clientes. De forma predeterminada, la casilla **Almacenar actualizaciones localmente** está activada y las actualizaciones se almacenarán en el servidor WSUS en la ubicación que usted especifique. Si desactiva la casilla **Almacenar actualizaciones localmente**, los equipos cliente obtienen las actualizaciones aprobadas al conectar Microsoft Update. Realice la selección y, a continuación, haga clic en **Siguiente**.

5.  En la página Opciones de base de datos, seleccione el software utilizado para administrar la base de datos de WSUS 3.0. De manera predeterminada, el asistente para instalación ofrece la instalación de Windows Internal Database.

    Si no desea utilizar Windows Internal Database, indique una instancia de SQL Server para WSUS para utilizarla, seleccionando **Usar una base de datos existente en este servidor** o **Usar un servidor de base de datos en un equipo remoto**. Introduzca el nombre de las instancias en la casilla aplicable. El nombre de la instancia debe aparecer como &lt;*nombreServidor*&gt;\\&lt;*nombreInstancia*&gt;, donde *nombreServidor* es el nombre del servidor y *nombreInstancia* es el nombre de la instancia SQL. Realice la selección y, después, haga clic en **Siguiente**.

6.  Si ha optado por conectar a un SQL Server, en la página **Conectar con la instancia de SQL Server**, WSUS intentará conectarse a la instancia especificada de SQL Server. Cuando se haya conectado correctamente, haga clic en **Siguiente** para continuar.

7.  En la página Selección de sitio web, indique el sitio web que utilizará WSUS 3.0. Si desea utilizar el sitio web predeterminado en el puerto 80, seleccione **Usar el sitio web predeterminado de IIS existente**. Si ya posee un sitio web en el puerto 80, puede crear un sitio alternativo en el puerto 8530 al seleccionar **Crear un sitio web de Windows Server Update Services 3.0 SP2**. Haga clic en **Siguiente**.

8.  En la página **Preparado para instalar Windows Server Update Services**, compruebe las selecciones y haga clic en **Siguiente**.

9.  La última página del asistente para instalación le permitirá saber si la instalación de WSUS se ha completado correctamente. Después de hacer clic en **Finalizar**, el asistente para configuración se iniciará.

Paso siguiente
--------------

[Paso 3: configurar las conexiones de red](https://technet.microsoft.com/42a144c5-f08e-4a6e-b360-47ddea77bd24).

Recursos adicionales
--------------------

[Guía paso a paso para Windows Server Update Services 3.0 SP2](https://technet.microsoft.com/4b504edc-93b3-45b0-a7e8-d0107f1a4442)
