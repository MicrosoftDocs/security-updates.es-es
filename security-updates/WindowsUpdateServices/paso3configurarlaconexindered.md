---
TOCTitle: 'Paso 3: configurar la conexión de red'
Title: 'Paso 3: configurar la conexión de red'
ms:assetid: 'cd77566d-7780-4ce4-aa56-41183c65c4a7'
ms:contentKeyID: 18158568
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708559(v=WS.10)'
---

Paso 3: configurar la conexión de red
=====================================

Después de instalar WSUS, estará preparado para obtener acceso a la consola de WSUS para configurar WSUS y comenzar a trabajar. De manera predeterminada, WSUS está configurado para utilizar Microsoft Update como lugar del que obtener las actualizaciones. Si tiene un servidor proxy en la red, utilice la consola de WSUS para configurar WSUS de modo que utilice el servidor proxy. Si hay un servidor de seguridad corporativo entre WSUS e Internet, puede que tenga que configurar el servidor de seguridad para asegurarse de que WSUS puede obtener las actualizaciones.

> [!NOTE]
> Aunque es necesaria una conexión a Internet para descargar las actualizaciones desde Microsoft Update, WSUS le ofrece la posibilidad de importarlas a redes no conectadas a Internet. Para obtener más información, vea las notas del producto “Deploying Microsoft Windows Server Update Services” (el documento puede estar en inglés). 

El paso 3 contiene los procedimientos siguientes:

-   Configurar el servidor de seguridad para que WSUS pueda obtener actualizaciones
-   Abrir la consola de WSUS
-   Configurar las opciones del servidor proxy para que WSUS pueda obtener actualizaciones

**Para configurar el servidor de seguridad**
-   Si hay un servidor de seguridad corporativo entre WSUS e Internet, puede que tenga que configurar el servidor de seguridad para asegurarse de que WSUS puede obtener las actualizaciones. Para obtener actualizaciones de Microsoft Update, el servidor WSUS utiliza el puerto 80 para el protocolo HTTP y el puerto 443 para el protocolo HTTPS. Esto no puede configurarse.

-   Si su organización no permite que estos puertos y protocolos estén abiertos a todas las direcciones, puede restringir el acceso a los dominios siguientes de manera que WSUS y Actualizaciones automáticas puedan comunicarse con Microsoft Update:

    -   http://windowsupdate.microsoft.com
    -   http://\*.windowsupdate.microsoft.com
    -   https://\*.windowsupdate.microsoft.com
    -   http://\*.update.microsoft.com
    -   https://\*.update.microsoft.com
    -   http://\*.windowsupdate.com
    -   http://download.windowsupdate.com
    -   http://download.microsoft.com
    -   http://\*.download.windowsupdate.com
    -   http://wustat.windows.com
    -   http://ntservicepack.microsoft.com

> [!NOTE]
> Los pasos para configurar el servidor de seguridad están pensados para un servidor de seguridad corporativo ubicado entre WSUS e Internet. Debido a que WSUS inicia todo su tráfico de red, no es necesario configurar Windows Firewall en el servidor WSUS. Aunque la conexión entre Microsoft Update y WSUS requiere que los puertos 80 y 443 estén abiertos, puede configurar varios servidores WSUS para que se sincronicen con un puerto personalizado. Para obtener más información sobre cómo sincronizar servidores WSUS con un puerto personalizado, vea las notas del producto “Deploying Microsoft Windows Server Update Services” (el documento puede estar en inglés). 

**Para abrir la consola de WSUS**
-   En el servidor WSUS, haga clic en **Inicio**, seleccione **Todos los programas** y **Herramientas administrativas** y, a continuación, haga clic en **Microsoft Windows Server Update Services**.

> [!NOTE]
> Para poder utilizar la consola de WSUS, debe ser miembro de Administradores de WSUS o de los grupos de seguridad locales Administradores en el servidor en el que WSUS está instalado. Si no agrega **http://&lt;***nombre del sitio Web de WSUS***&gt;** a la lista de sitios de la zona Intranet local de Internet Explorer en Windows Server 2003, puede que se le pidan sus credenciales cada vez que abra la consola de WSUS. Si cambia la asignación de puertos en IIS después de instalar WSUS, necesitará actualizar manualmente el acceso directo en el menú **Inicio**. También puede abrir la consola de WSUS desde Internet Explorer en cualquier servidor o equipo de la red a través de la siguiente dirección URL: **http://***nombreDeServidorWSUS***/WSUSAdmin** 

**Para especificar un servidor proxy**
1.  En la barra de herramientas de la consola de WSUS, haga clic en **Opciones** y, a continuación, en **Opciones de sincronización**.

2.  En el cuadro **Servidor proxy**, active la casilla de verificación **Usar un servidor proxy al sincronizarse** y, después, escriba el nombre y el número de puerto del servidor proxy (de manera predeterminada, el puerto 80) en los cuadros correspondientes.

3.  Si desea conectarse al servidor proxy con unas credenciales de usuario específicas, active la casilla de verificación **Usar credenciales de usuario para conectarse al servidor proxy** y, después, escriba el nombre de usuario, el dominio y la contraseña del usuario en los cuadros correspondientes. Si desea habilitar la autenticación básica para el usuario que se conecta al servidor proxy, active la casilla de verificación **Permitir autenticación básica (la contraseña se envía como texto no cifrado)**.

4.  En **Tareas**, haga clic en **Guardar configuración** y, después, haga clic en **Aceptar** en el cuadro de diálogo de confirmación.
