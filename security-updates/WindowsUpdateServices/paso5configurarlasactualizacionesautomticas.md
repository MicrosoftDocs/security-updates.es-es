---
TOCTitle: 'Paso 5: configurar las actualizaciones automáticas'
Title: 'Paso 5: configurar las actualizaciones automáticas'
ms:assetid: '5da6d10a-6ff1-4de8-b53a-4893bf8bd9fa'
ms:contentKeyID: 18158340
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720532(v=WS.10)'
---

Paso 5: configurar las actualizaciones automáticas
==================================================

Los equipos cliente de WSUS requieren una versión compatible de Actualizaciones automáticas. El programa de instalación de WSUS configura automáticamente IIS para distribuir la versión más reciente de Actualizaciones automáticas en cada equipo cliente que se ponga en contacto con el servidor WSUS.

La mejor manera de configurar las Actualizaciones automáticas depende de su entorno de red. En un entorno con Active Directory, puede usar un objeto de directiva de grupo (GPO) basado en dominios. En un entorno sin Active Directory, use el objeto de directiva de grupo local. Si usa el objeto de directiva de grupo local o un GPO basado en dominios, tiene que señalar con sus equipos cliente al servidor WSUS y, a continuación, configurar Actualizaciones automáticas.

En las instrucciones siguientes se supone que su red ejecuta Active Directory. En estos procedimientos se supone que conoce la directiva de grupos y que la usa para administrar su red. Tiene que crear un nuevo GPO para la configuración de WSUS y vincular el GPO al dominio.

Para obtener más información acerca de la directiva de grupo, vea el sitio Web del centro técnico de directivas de grupo en ([http://go.microsoft.com/fwlink/?LinkID=47375](http://go.microsoft.com/fwlink/?linkid=47375)).

**El paso 5 contiene los procedimientos siguientes**:

-   Agregar la plantilla administrativa de WSUS.
-   Configurar las actualizaciones automáticas.
-   Señalar con su equipo cliente a su servidor WSUS.
-   Iniciar manualmente la detección del servidor WSUS.

Realice el primero de los tres procedimientos del objeto de directiva de grupo basado en dominios. Deberá crear un nuevo GPO o usar uno existente. Si utiliza la Consola de administración de directivas de grupo (GPMC) para administrar sus GPO, seleccione el GPO que desea modificar y haga clic en **Editar**.

Para ver la configuración de directivas para administrar WSUS, deberá asegurarse de que el archivo de plantilla administrativa de WSUS, wuau.adm, se agrega al editor de objetos de directiva de grupo. Dado que wuau.adm se incluye de manera predeterminada en el sistema operativo, ya debería estar presente en el editor de objetos de directiva de grupo.

**Para agregar la plantilla administrativa de WSUS.**
1.  En el editor de objetos de directiva de grupo, haga clic en cualquiera de los nodos de **Plantillas administrativas**.

2.  En el menú **Acción**, haga clic en **Agregar o quitar plantillas** y después en **Agregar**.

3.  En el cuadro de diálogo **Plantillas de directivas**, haga clic en **wuau.adm** y, a continuación, en **Abrir**.

4.  En el cuadro de diálogo **Agregar o quitar plantillas**, haga clic en **Cerrar**.

**Para configurar Actualizaciones automáticas**
1.  En el **Editor de objetos de directiva de grupo**, expanda **Configuración del equipo**, expanda **Plantillas administrativas**, expanda **Componentes de Windows** y haga clic en **Windows Update**.

2.  En el panel de detalles, haga doble clic en **Configurar actualizaciones automáticas**.

3.  Haga clic en **Habilitadas** y realice una de las acciones siguientes:

    -   **Notificar descarga y notificar instalación**: Esta opción envía una notificación a un usuario administrativo que ha iniciado sesión antes de que comience la descarga y la instalación de las actualizaciones.
    -   **Descargar automáticamente y notificar instalación**: Esta opción comienza automáticamente a descargar actualizaciones y, a continuación, envía una notificación a un usuario administrativo que ha iniciado sesión antes de instalar las actualizaciones.
    -   **Descargar automáticamente y programar la instalación**: Si Actualizaciones automáticas se configura para realizar una instalación programada, tiene que establecer el día y la hora para la instalación programada recurrente.
    -   **Permitir que el administrador local elija la opción**: Con esta opción, los administradores locales pueden usar Actualizaciones automáticas del Panel de control para seleccionar la opción de configuración que deseen. Por ejemplo, pueden elegir su propia hora de instalación programada. Los administradores locales no pueden deshabilitar las actualizaciones automáticas.

4.  Haga clic en **Aceptar**.

> [!NOTE]
> La opción **Permitir que el administrador local elija su opción** aparece sólo si Actualizaciones automáticas se ha actualizado automáticamente a la versión compatible con WSUS. 

**Para señalar con su equipo cliente a su servidor WSUS.**
1.  En el **Editor de objetos de directiva de grupo**, expanda **Configuración del equipo**, expanda **Plantillas administrativas**, expanda **Componentes de Windows** y haga clic en **Windows Update**.

2.  En el panel de detalles, haga doble clic en **Especificar la ubicación del servicio Windows Update en la intranet**.

3.  Haga clic en **Habilitada** y escriba la dirección URL de HTTP del mismo servidor WSUS en los cuadros **Establecer el servicio de actualización de la intranet para detectar actualizaciones** y **Establecer el servidor de estadísticas de la intranet**. Por ejemplo, escriba *http://nombreServidor* en ambos cuadro y, a continuación, haga clic en **Aceptar**.

> [!NOTE]
> Si utiliza el objeto de directiva de grupo local para señalar con este equipo a WSUS, esta configuración entra en vigor inmediatamente y este equipo debe aparece en la consola administrativa de WSUS transcurrido un breve período de tiempo. Puede acelerar este proceso si inicia manualmente un ciclo de detección. 

Tras configurar un equipo cliente, transcurrirán unos minutos antes de que aparezca en la página **Equipos** de la consola de WSUS. Para los equipos cliente configurados con una directiva de grupo basada en dominios, tardará alrededor de 20 minutos después de que la directiva de grupo se actualice (es decir, se aplique cualquier configuración de directiva nueva al equipo cliente). De manera predeterminada, la directiva de grupo se actualiza en segundo plano cada 90 minutos, con un intervalo aleatorio de 0 a 30 minutos. Si desea actualizar la directiva de grupo antes, puede ir a un símbolo del sistema del equipo cliente y escribir: **gpupdate /force**.

Para los equipos cliente configurados con la GPO local, la directiva de grupo se aplica inmediatamente y la actualización dura alrededor de 20 minutos.

Una vez aplicada la directiva de grupo, puede iniciar manualmente la detección. Si inicia manualmente la detección, no tendrá que esperar 20 minutos para que el equipo cliente se ponga en contacto con WSUS.

**Para iniciar manualmente la detección del servidor WSUS.**
1.  En un equipo cliente, haga clic en **Inicio** y después en **Ejecutar**.

2.  Escriba **cmd** en el cuadro **Abrir** y después haga clic en **Aceptar**.

3.  En el símbolo del sistema, escriba **wuauclt.exe /detectnow**. Esta opción de línea de comandos hace que Actualizaciones automáticas se ponga en contacto con el servidor WSUS inmediatamente.
