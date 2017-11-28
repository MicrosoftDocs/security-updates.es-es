---
TOCTitle: 'Paso 5: configurar las actualizaciones de clientes'
Title: 'Paso 5: configurar las actualizaciones de clientes'
ms:assetid: '5ae60ead-3e94-456c-a692-c0f193ea5d5a'
ms:contentKeyID: 21741312
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd939830(v=WS.10)'
---

Paso 5: configurar las actualizaciones de clientes
==================================================

En Windows Server Update Services 3.0 (WSUS 3.0 SP2), el programa de instalación de WSUS configura automáticamente IIS para distribuir la versión más reciente de Actualizaciones automáticas en cada equipo cliente que se ponga en contacto con el servidor WSUS.

La mejor forma de configurar las Actualizaciones automáticas depende de su entorno de red. En un entorno que utiliza el servicio de directorio Active Directory®, puede usar un objeto de directiva de grupo (GPO) basado en dominios o crear un nuevo GPO. En un entorno sin Active Directory, use el objeto de directiva de grupo local. En este paso, podrá configurar las Actualizaciones automáticas y dirigir los equipos cliente al servidor WSUS.

En las instrucciones siguientes se supone que su red ejecuta Active Directory. En estos procedimientos se supone que conoce la directiva de grupos y que la usa para administrar su red.

Para obtener más información acerca de la directiva de grupo, vea el sitio web del centro técnico de directivas de grupo en [http://go.microsoft.com/fwlink/?LinkID=47375](http://go.microsoft.com/fwlink/?linkid=47375).

 
-

Procedimientos del paso 5
-------------------------

En el paso 4, ha completado la configuración de las actualizaciones que desea descargar. Utilice este conjunto de procedimientos para configurar las actualizaciones automáticas para los equipos cliente.

1.  Configurar actualizaciones automáticas en la directiva de grupo.
2.  Señalar un equipo cliente al servidor WSUS.
3.  Iniciar manualmente la detección del servidor WSUS.

Realizará los dos primeros procedimientos en el GPO basado en dominios a su elección y el tercer procedimiento, en un símbolo de sistema en el equipo cliente.

**Para configurar Actualizaciones automáticas**
1.  En la Consola de administración de directivas de grupo (GPMC), dirija su explorador al GPO en el que desee configurar WSUS y, a continuación, haga clic en **Editar**.

2.  En la GPMC, expanda **Configuración del equipo**, expanda **Plantillas administrativas** y **Componentes de Windows** y haga clic en **Windows Update**.

3.  En el panel de detalles, haga doble clic en **Configurar actualizaciones automáticas**.

4.  Haga clic en **Habilitadas** y realice una de las acciones siguientes:

    -   **Notificar descarga y notificar instalación**. Esta opción envía una notificación a un usuario administrativo que ha iniciado sesión antes de que comience la descarga y la instalación de las actualizaciones.
    -   **Descargar automáticamente y notificar instalación**. Esta opción comienza automáticamente a descargar actualizaciones y, a continuación, envía una notificación a un usuario administrativo que ha iniciado sesión antes de instalar las actualizaciones.
    -   **Descargar automáticamente y programar la instalación**. Esta opción inicia la descarga de actualizaciones de forma automática y, a continuación, instala las actualizaciones en el día y la hora que se especifican.
    -   **Permitir que el administrador local elija la opción**. Esta opción permite que los administradores locales usen Actualizaciones automáticas del Panel de control para seleccionar la opción de configuración que deseen. Por ejemplo, pueden elegir su propia hora de instalación programada. Los administradores locales no pueden deshabilitar las Actualizaciones automáticas.

5.  Haga clic en **Aceptar**.

**Para dirigir los equipos cliente al servidor WSUS.**
1.  En el panel de detalles de **Windows Update**, haga doble clic en **Especificar la ubicación del servicio Windows Update en la intranet**.

2.  Haga clic en **Habilitada** y escriba la dirección URL de HTTP del mismo servidor WSUS en los cuadros **Establecer el servicio de actualización de la intranet para detectar actualizaciones** y **Establecer el servidor de estadísticas de la intranet**. Por ejemplo, escriba *http://nombreServidor* en ambos cuadro y, a continuación, haga clic en **Aceptar**.

 
<p> </p>

> [!NOTE]
> Si utiliza el objeto de directiva de grupo local para dirigir el equipo a WSUS, esta configuración entra en vigor inmediatamente y este equipo aparece en la consola administrativa de WSUS transcurrido un breve período de tiempo. Puede acelerar este proceso si inicia manualmente un ciclo de detección.
 

Tras configurar un equipo cliente, transcurrirán unos minutos antes de que aparezca en la página **Equipos** de la consola administrativa de WSUS. Para los equipos cliente configurados con una directiva de grupo basada en dominios, tardará alrededor de 20 minutos después de que la directiva de grupo se actualice (es decir, se aplique cualquier configuración de directiva nueva al equipo cliente). De forma predeterminada, la directiva de grupo se actualiza en segundo plano cada 90 minutos, con un intervalo aleatorio de 0 a 30 minutos. Si desea actualizar la directiva de grupo antes, puede ir a un símbolo del sistema del equipo cliente y escribir **gpupdate /force**.

Para los equipos cliente configurados con el GPO local, la directiva de grupo se aplica inmediatamente y la actualización dura alrededor de 20 minutos.

Si inicia manualmente la detección, no tendrá que esperar 20 minutos para que el equipo cliente se ponga en contacto con WSUS.

**Para iniciar manualmente la detección del servidor WSUS**
1.  En un equipo cliente, haga clic en **Inicio** y después en **Ejecutar**.

2.  Escriba **cmd** en el cuadro **Abrir** y haga clic en **Aceptar**.

3.  En el símbolo de sistema, escriba **wuauclt.exe /detectnow**. Esta opción de línea de comandos hace que Actualizaciones automáticas se ponga en contacto con el servidor WSUS inmediatamente.

Paso siguiente
--------------

[Paso 6: configurar los grupos de equipos](https://technet.microsoft.com/70518732-2179-4e41-9609-7f9999867f41)

Recursos adicionales
--------------------

[Guía paso a paso para Windows Server Update Services 3.0 SP2](https://technet.microsoft.com/4b504edc-93b3-45b0-a7e8-d0107f1a4442)
