---
TOCTitle: 'Paso 5: actualizar y configurar actualizaciones automáticas'
Title: 'Paso 5: actualizar y configurar actualizaciones automáticas'
ms:assetid: '4ac8d574-f48e-4d9d-86c9-9aeb0f57e750'
ms:contentKeyID: 18158334
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720533(v=WS.10)'
---

Paso 5: actualizar y configurar actualizaciones automáticas
===========================================================

Los equipos cliente WSUS requieren una versión compatible de actualizaciones automáticas. El programa de instalación de WSUS configura IIS automáticamente para que distribuya la última versión de actualizaciones automáticas a cada equipo cliente que se conecte con el servidor WSUS.

> [!NOTE]
> Aunque la mayoría de las versiones de actualizaciones automáticas pueden señalar al servidor WSUS y se actualizarán automáticamente a la versión compatible con WSUS, la versión de actualizaciones automáticas incluida con Windows XP sin Service Packs no se actualiza automáticamente. Si su entorno tiene Windows XP sin Service Packs y no ha utilizado nunca Servicio de actualización de software (SUS), lea las instrucciones en las notas del producto “Deploying Microsoft Windows Server Update Services” (el documento puede estar en inglés). 

La manera más adecuada de configurar las actualizaciones automáticas depende del entorno de red. En un entorno de Active Directory, puede utilizar el objeto Directiva de grupo (GPO) de Active Directory. En un entorno que no sea de Active Directory, use el objeto Directiva de grupo local. Tanto si utiliza el objeto Directiva de grupo local como un GPO almacenado en un controlador de dominio, debe hacer que los equipos cliente señalen al servidor WSUS y, después, configurar las actualizaciones automáticas.

En las instrucciones siguientes se da por supuesto que la red ejecuta Active Directory. En estos procedimientos también se asume que ya ha configurado Directiva de grupo, que está familiarizado con ella y la utiliza para administrar la red. Necesita crear un nuevo objeto Directiva de grupo (GPO) para la configuración de WSUS y vincular el GPO en el nivel de dominio.

Para obtener más información acerca de Directiva de grupo, vea la página correspondiente ([Group Policy](http://go.microsoft.com/fwlink/?linkid=47375)), en la dirección http://go.microsoft.com/fwlink/?LinkID=47375 (puede estar en inglés).

El paso 5 contiene los procedimientos siguientes:

-   Cargar la plantilla administrativa de WSUS
-   Configurar las actualizaciones automáticas
-   Orientar los equipos cliente al servidor WSUS
-   Iniciar manualmente la detección en el equipo cliente

Realice los tres procedimientos siguientes en un objeto Directiva de grupo basado en Active Directory.

**Para agregar la plantilla administrativa de WSUS**
1.  En el Editor de objetos de directiva de grupo, haga clic en uno de los nodos **Plantillas administrativas**.

2.  En el menú **Acción**, haga clic en **Agregar o quitar plantillas**.

3.  Haga clic en **Agregar**.

4.  En el cuadro de diálogo **Plantillas de directiva**, haga clic en **wuau.adm** y, después, en **Abrir**.

5.  En el cuadro de diálogo **Agregar o quitar plantillas**, haga clic en **Cerrar**.

**Para configurar el comportamiento de las actualizaciones automáticas**
1.  En el Editor de objetos de directiva de grupo, expanda **Configuración del equipo**, expanda **Plantillas administrativas**, expanda **Componentes de Windows** y haga clic en **Windows Update**.

2.  En el panel de detalles, haga doble clic en **Configurar actualizaciones automáticas**.

3.  Haga clic en **Habilitado** y, a continuación, haga clic en una de las opciones siguientes:

    -   **Notificar descarga y notificar instalación**. Si se selecciona esta opción, el usuario administrativo que ha iniciado sesión recibe una notificación antes de la descarga y antes de la instalación de las actualizaciones.
    -   **Descargar automáticamente y notificar instalación**. Si se selecciona esta opción, la descarga de las actualizaciones se inicia automáticamente y, después, el usuario administrativo que ha iniciado sesión recibe una notificación antes de que se instalen las actualizaciones.
    -   **Descargar automáticamente y programar instalación**. Si Actualizaciones automáticas se ha configurado para que se realice una instalación programada, también deberá establecerse la fecha y la hora de la instalación periódica programada.
    -   **Permitir que el administrador local elija la configuración**. Si se selecciona esta opción, los administradores locales pueden utilizar Actualizaciones automáticas en Panel de control para elegir la opción de configuración que deseen. Pueden elegir, por ejemplo, su propia hora de instalación programada. Los administradores locales no pueden deshabilitar las actualizaciones automáticas.

4.  Haga clic en **Aceptar**.

> [!NOTE]
> La opción **Permitir que el administrador local elija la configuración** solamente aparece si Actualizaciones automáticas se ha actualizado a la versión compatible con WSUS. 

**Para orientar el equipo cliente al servidor WSUS**
1.  En el Editor de objetos de directiva de grupo, expanda **Configuración del equipo**, expanda **Plantillas administrativas**, expanda **Componentes de Windows** y haga clic en **Windows Update**.

2.  En el panel de detalles, haga doble clic en **Especificar la ubicación del servicio Windows Update de la intranet**.

3.  Haga clic en **Habilitada** y escriba la dirección URL HTTP del mismo servidor WSUS en los cuadros **Establecer el servicio de actualización de la intranet para detectar actualizaciones** y **Establecer el servidor de estadísticas de la intranet**. Por ejemplo, escriba **http://***nombreDeServidor* en ambos cuadros.

4.  Haga clic en **Aceptar**.

> [!NOTE]
> Si utiliza el objeto Directiva de grupo local para orientar este equipo a WSUS, esta configuración tiene efecto inmediatamente y el equipo debería aparecer en la consola administrativa de WSUS en 20 minutos aproximadamente. Para acelerar el proceso, inicie un ciclo de detección manualmente. 

Una vez que se ha configurado un equipo cliente, pasarán algunos minutos hasta que aparezca en la página **Equipos** de la consola de WSUS. En el caso de los equipos cliente configurados con un GPO basado en Active Directory, transcurrirán unos 20 minutos hasta que Directiva de grupo se actualice, es decir, hasta que se aplique la nueva configuración al equipo cliente. De manera predeterminada, Directiva de grupo se actualiza en segundo plano cada 90 minutos, con un desplazamiento aleatorio de 0 a 30 minutos. Si desea que se actualice antes, abra el símbolo del sistema en el equipo cliente y escriba: **gpupdate /force**.

En el caso de los equipos cliente configurados con el GPO local, la Directiva de grupo se aplica inmediatamente y tarda unos 20 minutos.

Una vez aplicada la Directiva de grupo, la detección se puede iniciar manualmente. Si realiza este procedimiento, no tiene que esperar 20 minutos a que el equipo cliente se ponga en contacto con WSUS.

**Para iniciar manualmente la detección por parte del servidor WSUS**
1.  En el equipo cliente, haga clic en **Inicio** y, a continuación, en **Ejecutar**.

2.  Escriba **cmd** y haga clic en **Aceptar**.

3.  En el símbolo del sistema, escriba **wuauclt.exe /detectnow**. Esta opción de línea de comandos indica a Actualizaciones automáticas que se ponga en contacto con el servidor WSUS de inmediato.
