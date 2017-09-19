---
TOCTitle: 'Paso 7: aprobar e implementar actualizaciones'
Title: 'Paso 7: aprobar e implementar actualizaciones'
ms:assetid: '38db25a9-6702-4e43-b536-764e8814afc6'
ms:contentKeyID: 18158191
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720504(v=WS.10)'
---

Paso 7: aprobar e implementar actualizaciones
=============================================

En este paso se aprueba la actualización de los equipos cliente de prueba del grupo de prueba. Los equipos del grupo se comprobarán con el servidor WSUS durante las 24 horas siguientes. Transcurrido este período de tiempo, puede utilizar la característica de generación de informes de WSUS para determinar si esas actualizaciones se implementaron en los equipos. Si la comprobación es correcta, puede aprobar la misma actualización para el resto de los equipos de la organización.

El paso 7 contiene los procedimientos siguientes:

-   Aprobar e implementar una actualización
-   Comprobar el estado del informe de actualizaciones

**Para aprobar e implementar una actualización**
1.  En la barra de herramientas de la consola de WSUS, haga clic en **Actualizaciones**. De manera predeterminada, la lista de actualizaciones se filtra para mostrar únicamente las actualizaciones críticas y de seguridad que han sido aprobadas para su detección en los equipos cliente. Use el filtro predeterminado para este procedimiento.

2.  En la lista de actualizaciones, seleccione aquéllas que desea aprobar para la instalación. En la ficha **Detalles** dispone de información sobre cada actualización seleccionada. Para seleccionar varias actualizaciones contiguas, presione la tecla MAYÚS y manténgala presionada mientras las selecciona; para seleccionar varias actualizaciones no contiguas, presione y mantenga presionada la tecla CTRL mientras las selecciona.

3.  En **Tareas de actualización**, haga clic en **Cambiar aprobación**. Aparece el cuadro de diálogo **Aprobar actualizaciones**.

4.  En la lista **Configuración de aprobación de grupo para las actualizaciones seleccionadas**, haga clic en **Instalar** en la lista de la columna **Aprobación** del grupo de prueba y, después, haga clic en **Aceptar**.

| ![](images/Cc720504.note(WS.10).gif)Nota                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hay muchas opciones asociadas a la aprobación de actualizaciones, como establecer fechas límite y desinstalar actualizaciones. Éstas se describen en las notas del producto “Microsoft Windows Server Update Services Operations Guide” (el documento puede estar en inglés). |

Transcurridas 24 horas, puede utilizar la característica de generación de informes de WSUS para determinar si esas actualizaciones se implementaron en los equipos.

**Para comprobar el estado del informe de actualizaciones**
1.  En la barra de herramientas de la consola de WSUS, haga clic en **Informes**.

2.  En la página **Informes**, haga clic en **Estado de las actualizaciones**.

3.  Si desea filtrar la lista de actualizaciones, en **Vista**, seleccione los criterios que desee utilizar y haga clic en **Aplicar**.

4.  Si desea ver el estado de una actualización por grupo de equipos y, después, por equipo, expanda la vista de la actualización como sea necesario.

5.  Si desea imprimir el informe Estado de las actualizaciones, en **Tareas**, haga clic en **Imprimir informe**.

Si las actualizaciones se han implementado correctamente en el grupo de prueba, puede aprobar las mismas para los demás equipos de la organización.
