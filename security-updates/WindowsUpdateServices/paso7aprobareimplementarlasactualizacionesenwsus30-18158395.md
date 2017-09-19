---
TOCTitle: 'Paso 7: aprobar e implementar las actualizaciones en WSUS 3.0'
Title: 'Paso 7: aprobar e implementar las actualizaciones en WSUS 3.0'
ms:assetid: '88fac442-a9d3-4e74-92f6-3822b7237af1'
ms:contentKeyID: 18158395
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708475(v=WS.10)'
---

Paso 7: aprobar e implementar las actualizaciones en WSUS 3.0
=============================================================

En este paso, se aprueba una actualización para cualquier equipo cliente de prueba del grupo de pruebas. Los equipos del grupo se pondrán en contacto con el servidor WSUS en las siguientes 24 horas. Transcurrido este período, podrá usar la característica de informes de WSUS para determinar si dichas actualizaciones se han implementado en los equipos. Si las pruebas se realizan correctamente, puede aprobar las mismas actualizaciones para el resto de equipos de su organización.

**El paso 7 contiene los procedimientos siguientes**:

-   Aprobar e implementar una actualización.
-   Comprobar el estado de la actualización.

**Para aprobar e implementar una actualización.**
1.  En la consola de administración de WSUS, haga clic en **Actualizaciones**. Con ello se mostrará un resumen de actualizaciones en las vistas predeterminadas (**Todas las actualizaciones**, **Actualizaciones críticas**, **Actualizaciones de seguridad** y **Actualizaciones de WSUS**). Use **Todas las Actualizaciones** para este procedimiento.

2.  En la lista de actualizaciones, seleccione las actualizaciones que desea aprobar para la instalación. La información acerca de una actualización seleccionada está disponible en el panel inferior del panel Actualizaciones. Para seleccionar varias actualizaciones contiguas, mantenga presionada la tecla **MAYÚS** mientras hace clic en las actualizaciones; para seleccionar varias actualizaciones no contiguas, mantenga presionada la tecla **CTRL** mientras hace clic en las actualizaciones.

3.  Haga clic con el botón secundario del mouse en la selección y, a continuación, haga clic en **Aprobar**. Aparecerá el cuadro de diálogo **Aprobar actualizaciones**.

4.  Seleccione uno de los grupos (por ejemplo, **Pruebas**) y haga clic en la flecha situada a su izquierda. Verá un menú contextual con las opciones **Aprobada para su instalación**, **Aprobada para su eliminación**, **No aprobada**, **Fecha límite**, **Igual que primario** y **Aplicar a los elementos secundarios**. Haga clic en **Aprobada para su instalación** y haga clic en **Aceptar**.

5.  Verá una nueva ventana, **Progreso de aprobación**, que muestra el progreso de las diferentes tareas que afectan a la aprobación de las actualizaciones. Una vez completada la aprobación, haga clic en **Cerrar** para cerrar esta ventana.

| ![](images/Cc708475.note(WS.10).gif)Nota                                                              |
|------------------------------------------------------------------------------------------------------------------------------------|
| Muchas opciones están asociadas con la aprobación de actualizaciones, como configurar fechas límite y desinstalar actualizaciones. |

Transcurridas 24 horas, podrá usar la característica de informes de WSUS para determinar si las actualizaciones se han implementado en los equipos.

**Para comprobar el estado de una actualización**
1.  En la consola de administración de WSUS, haga clic en **Informes** en el panel izquierdo.

2.  En la página **Informes**, verá un número de informes estandarizados. Haga clic en el informe **Actualizar resumen de estado**. Verá la ventana **Informe de actualizaciones**.

3.  Si desea filtrar la lista de actualizaciones, seleccione los criterios que desea usar (por ejemplo, **Incluir actualizaciones en estas clasificaciones**) y, a continuación, haga clic en **Ejecutar informe** en la barra de herramientas de la ventana.

4.  Verá el panel **Informe de actualizaciones**. Puede comprobar el estado de las actualizaciones individuales si selecciona la actualización de la sección izquierda del panel. La última sección del panel del informe muestra el resumen de estado de la actualización.

5.  Puede guardar o imprimir este informe si hace clic en el icono adecuado en la barra de herramientas.

Si las actualizaciones se implementaron correctamente para el grupo de pruebas, podrá aprobar las mismas actualizaciones para el resto de equipos de su organización.
