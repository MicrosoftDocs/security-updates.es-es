---
TOCTitle: 'Paso 6: crear un grupo de equipos'
Title: 'Paso 6: crear un grupo de equipos'
ms:assetid: '6039e5dc-d2ce-4d4b-b737-17ebcadbd4a7'
ms:contentKeyID: 18158344
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720536(v=WS.10)'
---

Paso 6: crear un grupo de equipos
=================================

Los grupos de equipos son una parte importante de las implementaciones de WSUS, incluso para una implementación básica. Los grupos de equipos permiten dirigir las actualizaciones a equipos específicos. Hay dos grupos de equipos predeterminados: Todos los equipos y Equipos sin asignar. De manera predeterminada, la primera vez que un equipo cliente se pone en contacto con el servidor WSUS, el servidor lo agrega a ambos grupos.

Se pueden crear grupos de equipos personalizados. Una ventaja de crear grupos de equipos es que permiten comprobar las actualizaciones antes de implementarlas de manera global. Si la comprobación es correcta, puede distribuir las actualizaciones en el grupo Todos los equipos. No existe un límite para el número de grupos personalizados que se pueden crear.

La configuración de grupos de equipos es un proceso de tres pasos. Primero, se especifica cómo se van a asignar los equipos a los grupos de equipos. Hay dos opciones: *dirigida al servidor* y *dirigida al cliente*. En la asignación dirigida al servidor es necesario agregar manualmente cada equipo a su grupo mediante WSUS. En la asignación dirigida al cliente, los clientes se agregan automáticamente mediante Directiva de grupo o claves del Registro. En segundo lugar, se crea el grupo de equipos en WSUS. En tercer lugar, los equipos se trasladan a los grupos con el método elegido en el primer paso.

En este documento se explica cómo utilizar la asignación dirigida al servidor y cómo mover manualmente los equipos a sus grupos mediante la consola de WSUS. Si tiene muchos equipos cliente que asignar a grupos de equipos, podría utilizar la asignación dirigida al cliente, que traslada automáticamente los equipos a los grupos.

Si desea configurar un grupo de prueba que contenga al menos un equipo de prueba, puede seguir el paso 6.

Este paso contiene los procedimientos siguientes:

-   Especificar la asignación dirigida al servidor
-   Crear un grupo
-   Trasladar equipos al grupo

**Para especificar el método de asignación de equipos a grupos**
1.  En la barra de herramientas de la consola de WSUS, haga clic en **Opciones** y, a continuación, en **Opciones de equipo**.

2.  En el cuadro **Opciones de equipo**, haga clic en **Usar la tarea Mover equipos en Windows Server Update Services**.

3.  En **Tareas**, haga clic en **Guardar configuración** y, después, haga clic en **Aceptar** cuando aparezca el cuadro de diálogo de confirmación.

**Para crear un grupo**
1.  En la barra de herramientas de la consola de WSUS, haga clic en **Equipos**.

2.  En **Tareas**, haga clic en **Crear un grupo de equipos**.

3.  En el cuadro **Nombre de grupo**, escriba **Prueba** y, después, haga clic en **Aceptar**.

Realice el siguiente procedimiento para asignar un equipo cliente adecuado para las pruebas al grupo de pruebas. Un equipo cliente adecuado para las pruebas es cualquier equipo que tenga software y hardware representativo de la mayoría de los equipos de la red, pero no un equipo que tenga asignada una función crítica. De esta forma, podrá saber, al compararlos con el equipo de prueba, cómo se comportarán los equipos con las actualizaciones que apruebe.

**Para agregar manualmente un equipo al grupo de pruebas**
1.  En la barra de herramientas de la consola de WSUS, haga clic en **Equipos**.

2.  En el cuadro **Grupos**, haga clic en el grupo del equipo que desea mover.

3.  En la lista de equipos, haga clic en el equipo que desee mover.

4.  En **Tareas**, haga clic en **Mover el equipo seleccionado**.

5.  En la lista **Grupo de equipos**, seleccione el grupo al que desee mover el equipo y, después, haga clic en **Aceptar**.
