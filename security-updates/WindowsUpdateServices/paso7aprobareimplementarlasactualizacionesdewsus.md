---
TOCTitle: 'Paso 7: aprobar e implementar las actualizaciones de WSUS'
Title: 'Paso 7: aprobar e implementar las actualizaciones de WSUS'
ms:assetid: 'c4e58e17-d5e3-4194-8f26-b459e0c03b86'
ms:contentKeyID: 21741402
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd939909(v=WS.10)'
---

Paso 7: aprobar e implementar las actualizaciones de WSUS
=========================================================

En este paso, usted aprueba una actualización para cualquier equipo en el grupo de prueba para Windows Server Update Services 3.0 Service Pack 2 (WSUS 3.0 SP2). Los equipos del grupo se pondrán en contacto de manera automática con el servidor WSUS en las siguientes 24 horas para adquirir la actualización. Puede usar la característica de informes de WSUS para determinar si dichas actualizaciones se implementaron en los equipos de prueba. Cuando las pruebas se hayan completado correctamente, podrá aprobar las actualizaciones para los grupos de equipos aplicables en su organización.

Procedimientos del paso 7
-------------------------

-   Aprobar e implementar una actualización.
-   Comprobar el estado de la actualización.

**Para aprobar e implementar una actualización**
1.  En la consola de administración de WSUS, haga clic en **Actualizaciones**. Se ha mostrado un resumen de estado de la actualización para **Todas las actualizaciones**, **Actualizaciones críticas**, **Actualizaciones de seguridad** y **Actualizaciones de WSUS**.

2.  En la sección **Todas las actualizaciones**, haga clic en **Actualizaciones requeridas por equipos**.

3.  En la lista de actualizaciones, seleccione aquéllas que desea aprobar para la instalación en su grupo de equipos de prueba. La información acerca de una actualización seleccionada está disponible en el panel inferior del panel Actualizaciones. Para seleccionar varias actualizaciones contiguas, mantenga presionada la tecla **MAYÚS** mientras hace clic en las actualizaciones; para seleccionar varias actualizaciones no contiguas, mantenga presionada la tecla **CTRL** mientras hace clic en las actualizaciones.

4.  Haga clic con el botón secundario del mouse en la selección y, a continuación, haga clic en **Aprobar**.

5.  En el cuadro de diálogo **Aprobar actualizaciones**, seleccione su grupo de prueba y, a continuación, haga clic en la flecha ABAJO.

6.  Haga clic en **Aprobada para su instalación** y haga clic en **Aceptar**.

7.  Aparece la ventana de Progreso de la aprobación que muestra el progreso de las tareas que afectan a la aprobación de actualización. Cuando finalice la aprobación, haga clic en **Cerrar**.

Transcurridas 24 horas, podrá usar la característica de informes de WSUS para determinar si las actualizaciones se han implementado en los equipos del grupo de prueba.

**Para comprobar el estado de una actualización**
1.  En el panel de navegación de la consola de administración de WSUS, haga clic en **Informes**.

2.  En la página **Informes**, haga clic en el informe **Actualizar resumen de estado**. Aparece la ventana **Informe de actualizaciones**.

3.  Si desea filtrar la lista de actualizaciones, seleccione los criterios que quiere usar (por ejemplo, **Incluir actualizaciones en estas clasificaciones**) y, a continuación, haga clic en **Ejecutar informe** en la barra de herramientas de la ventana.

4.  Verá el panel **Informe de actualizaciones**. Puede comprobar el estado de las actualizaciones individuales si selecciona la actualización de la sección izquierda del panel. La última sección del panel del informe muestra el resumen de estado de la actualización.

5.  Puede guardar o imprimir este informe si hace clic en el icono adecuado en la barra de herramientas.

6.  Después de probar las actualizaciones, puede aprobarlas para su instalación en los grupos de equipo adecuados en su organización.

Recursos adicionales
--------------------

[Guía paso a paso para Windows Server Update Services 3.0 SP2](https://technet.microsoft.com/4b504edc-93b3-45b0-a7e8-d0107f1a4442)

Si desea más información acerca de cómo utilizar WSUS 3.0 SP2, consulte:

La guía de implementación de WSUS en [http://go.microsoft.com/fwlink/?LinkId=139832](http://go.microsoft.com/fwlink/?linkid=139832).

La guía de operaciones de WSUS en [http://go.microsoft.com/fwlink/?LinkId=139838](http://go.microsoft.com/fwlink/?linkid=139838).
