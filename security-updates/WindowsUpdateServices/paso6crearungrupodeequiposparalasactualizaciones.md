---
TOCTitle: 'Paso 6: crear un grupo de equipos para las actualizaciones'
Title: 'Paso 6: crear un grupo de equipos para las actualizaciones'
ms:assetid: 'fe219654-eae8-45ca-a44b-c1e05c3c3e93'
ms:contentKeyID: 18158623
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708629(v=WS.10)'
---

Paso 6: crear un grupo de equipos para las actualizaciones
==========================================================

Los grupos de equipos son una parte importante de las implementaciones de WSUS, incluso una implementación básica. Los grupos de equipos permiten dirigir las actualizaciones a equipos específicos. Hay dos grupos de equipos predeterminados: Todos los equipos y Equipos sin asignar. De manera predeterminada, cuando cada equipo cliente se pone en contacto inicialmente con el servidor WSUS, éste agrega dicho equipo cliente a cada uno de estos grupos.

Puede crear grupos de equipos personalizados. Una ventaja de crear grupos de equipos es que permiten probar las actualizaciones antes de implementar las actualizaciones de forma extensiva. Si la prueba es correcta, puede distribuir las actualizaciones al grupo Todos los equipos. No hay ningún límite en cuanto al número de grupos personalizados que puede crear.

**Para configurar grupos de equipos**
1.  Especifique cómo va a asignar los equipos a los grupos de equipos. Hay dos opciones: destinatarios del lado del servidor y destinatarios del lado del cliente. Los destinatarios del lado del servidor implican que hay que agregar manualmente cada equipo a su grupo utilizando WSUS. Los destinatarios del lado del cliente implican agregar automáticamente los clientes utilizando la directiva de grupo o las claves del Registro.

2.  Crear el grupo de equipos en WSUS.

3.  Mueva los equipos en grupos utilizando el método elegido en el paso 1.

En esta sección se explica cómo utilizar los destinatarios del lado del servidor y mover manualmente los equipos a sus grupos utilizando la consola de administración de WSUS. Si tiene varios equipos cliente para asignar a los grupos de equipos, puede usar destinatarios del lado del cliente, que automatizan el movimiento de equipos a los grupos de equipos.

Puede usar el paso 6 para configurar un grupo de pruebas que contenga al menos un equipo de prueba.

**El paso 6 contiene los procedimientos siguientes:**

-   Crear un grupo.
-   Agregar un equipo al grupo.

**Para crear un grupo**
1.  En la consola de administración de WSUS, expanda **Equipos** y seleccione **Todos los equipos**.

2.  Haga clic con el botón secundario del mouse **Todos los equipos** o vaya al panel **Acciones** y después haga clic en **Agregar grupo de equipos**.

3.  Aparecerá el cuadro de diálogo **Agregar grupo de equipos**. Escriba el nombre del grupo nuevo.

Use el procedimiento siguiente para asignar un equipo cliente al grupo de prueba. Un equipo cliente adecuado para realizar pruebas es cualquier equipo con software y hardware indicativo de la mayoría de los equipos de su red, pero no un equipo asignado a una función importante. De esta manera, puede decir cómo se comportarán los equipos similares al equipo de pruebas con las actualizaciones que va a aprobar.

**Para agregar un equipo al grupo**
1.  En la consola de administración de WSUS, haga clic en **Equipos**.

2.  Haga clic en el grupo del equipo que desea mover.

3.  En la lista de equipos, seleccione el equipo que desea mover.

4.  Haga clic con el botón secundario del mouse en **Cambiar pertenencia**.

5.  Aparecerá el cuadro de diálogo **Establecer pertenencia a un grupo de equipos** con una lista de grupos.

6.  Seleccione el grupo al que desea mover el equipo y, después, haga clic en **Aceptar**.
