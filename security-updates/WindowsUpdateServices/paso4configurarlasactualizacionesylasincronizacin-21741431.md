---
TOCTitle: 'Paso 4: configurar las actualizaciones y la sincronización'
Title: 'Paso 4: configurar las actualizaciones y la sincronización'
ms:assetid: 'deeaa7e1-9b50-45cb-9537-d75f70de3405'
ms:contentKeyID: 21741431
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd939924(v=WS.10)'
---

Paso 4: configurar las actualizaciones y la sincronización
==========================================================

En esta sección se describe cómo configurar el conjunto de actualizaciones que desee descargar utilizando Windows Server Update Services 3.0 Service Pack 2 (WSUS 3.0 SP2).

Procedimientos del paso 4
-------------------------

Puede realizar estos procedimientos utilizando tanto el asistente para configuración WSUS como la consola de administración de WSUS.

1.  Guardar y descargar información sobre el servidor que precede en la cadena y el servidor proxy.
2.  Elegir el idioma de las actualizaciones.
3.  Elegir los productos para los que desea obtener actualizaciones.
4.  Elegir las clasificaciones de actualizaciones.
5.  Especificar la programación de sincronización para este servidor.

Después de configurar la conexión de red, puede descargar las actualizaciones sincronizando el servidor WSUS. La sincronización comienza cuando el servidor WSUS se ponga en contacto con Microsoft Update. Tras ponerse en contacto, WSUS determina si hay nuevas actualizaciones disponibles desde la última sincronización. Cuando sincronice el servidor WSUS por primera vez, todas las actualizaciones están disponibles y preparadas para su aprobación y posterior instalación. La sincronización inicial puede tardar bastante rato.

Los procedimientos de esta sección describen la sincronización con la configuración predeterminada. WSUS 3.0 SP2 también incluye las opciones que le permiten minimizar el uso del ancho de banda durante la sincronización.

Si está utilizando el asistente para configuración de Windows Server Update Services
------------------------------------------------------------------------------------

En los procedimientos del paso 3, ha completado la configuración del servidor que precede en la cadena y del servidor proxy. El siguiente conjunto de procedimientos comienza en la página **Conectar al servidor que precede en la cadena** de este asistente para configuración.

**Guardar y descargar información sobre el servidor que precede en la cadena y el servidor proxy**
1.  En la página Conectar al servidor que precede en la cadena del asistente para configuración, haga clic en el botón **Iniciar conexión**. De esta manera su configuración se guarda y se carga y se reúne información acerca de las actualizaciones disponibles.

2.  Mientras se realiza la conexión, el botón **Detener conexión** estará disponible. Si hay problemas con la conexión, haga clic en **Detener conexión**, resuelva los problemas y reinicie la conexión.

3.  Después de que la descarga se haya completado correctamente, haga clic en **Siguiente**.

**Para elegir los idiomas de actualización**
1.  La página Elegir idiomas permite recibir actualizaciones de todos los idiomas o de un subconjunto de idiomas. Si se selecciona un subconjunto de idiomas, se ahorrará espacio en disco, pero es importante elegir todos los idiomas que necesitan todos los clientes de este servidor WSUS.

    Si elige obtener actualizaciones sólo para algunos idiomas, seleccione **Descargar actualizaciones sólo en estos idiomas** y seleccione los idiomas para los que desea las actualizaciones.

2.  Haga clic en **Siguiente**.

**Para elegir los productos de actualización**
1.  La página Elegir productos permite especificar los productos para los que desea obtener actualizaciones. Seleccione categorías de productos, como Windows, o productos específicos, como Windows Server 2008. Si selecciona una categoría de productos, se seleccionarán también todos los productos bajo ella.

2.  Haga clic en **Siguiente**.

**Para elegir las clasificaciones de actualización**
1.  La página Elegir clasificaciones le permite especificar las clasificaciones de actualización que desea obtener. Elija todas las clasificaciones o un subconjunto.

2.  Haga clic en **Siguiente**.

**Para configurar una programación de sincronización**
1.  En la página Establecer una programación de sincronización, elija si desea realizar una sincronización manual o automática.

    Si elige **Sincronizar manualmente**, tendrá que iniciar el proceso de sincronización desde la consola de administración de WSUS.

    Si elige **Sincronizar automáticamente**, el servidor WSUS sincronizará en los intervalos especificados. Establezca la hora de la **Primera sincronización** y especifique el número de **Sincronizaciones por día** que desea que realice este servidor. Por ejemplo, si especifica que debe haber cuatro sincronizaciones al día, comenzando a las 3:00, las sincronizaciones tendrán lugar a las 3:00, 9:00, 15:00 y 21:00.

2.  Haga clic en **Siguiente**.

3.  En la página Finalizada, puede iniciar la consola de administración de WSUS si deja activada la casilla **Iniciar el complemento de administraciones de Windows Server Update Services** e iniciar la primera sincronización si deja activada la casilla **Iniciar sincronización inicial**.

4.  Haga clic en **Finalizar**.
    > [!Importante]
    > No se pueden guardar los cambios en la configuración realizados mientras el servidor está sincronizando. Espere hasta que haya terminado la sincronización para hacer los cambios.
 

Si está utilizando la consola de administración de WSUS
-------------------------------------------------------

Los procedimientos siguientes explican cómo realizar los pasos de la configuración utilizando la consola de administración de WSUS.

**Para elegir los productos y clasificaciones de actualizaciones**
1.  En el panel **Opciones**, haga clic en **Productos y clasificaciones**. Aparece un cuadro de diálogo con las fichas **Productos** y **Clasificaciones**.

2.  En la ficha **Productos**, seleccione la categoría de producto o producto específico para el que desea que este servidor obtenga actualizaciones, o bien, seleccione **Todos los productos**.

3.  En la ficha **Clasificaciones**, seleccione las clasificaciones de actualización que desee, o bien, seleccione **Todas las clasificaciones**.

4.  Haga clic en **Aceptar** para guardar las selecciones.

**Para elegir idiomas y archivos de actualizaciones**
1.  En el panel **Opciones**, haga clic en **Actualizar archivos e idiomas**. Aparece un cuadro de diálogo con las fichas de **Archivos de actualización** e **Idiomas de clasificación**.

2.  En la ficha **Actualizar archivos**, elija **Almacenar archivos de actualización localmente en este servidor** o haga que todos los equipos cliente instalen desde Microsoft Update. Si decide almacenar los archivos de actualización en este servidor, puede elegir entre descargar sólo aquellas actualizaciones aprobadas o descargar archivos de instalación rápida.

3.  En la ficha **Actualizar idiomas**, si almacena archivos de actualización localmente, elija **Descargar actualizaciones para todos los idiomas** (opción predeterminada) o **Descargar actualizaciones sólo en los idiomas especificados**. Si el servidor WSUS tiene servidores que siguen en la cadena, éstos obtendrán actualizaciones sólo en los idiomas especificados por el servidor que precede en la cadena.

4.  Haga clic en **Aceptar** para guardar los cambios.

**Para sincronizar el servidor WSUS**
1.  En el panel **Opciones**, haga clic en **Programación de sincronización**.

2.  En la ficha **Programación de sincronización**, elija si realizar una sincronización manual o automática.

    Si elige **Sincronizar manualmente**, tendrá que iniciar el proceso de sincronización desde la consola de administración de WSUS.

    Si elige **Sincronizar automáticamente**, el servidor WSUS sincronizará en los intervalos especificados. Establezca la hora de la **Primera sincronización** y especifique el número de **Sincronizaciones por día** que desea que realice este servidor. Por ejemplo, si especifica que debe haber cuatro sincronizaciones al día, comenzando a las 3:00, las sincronizaciones tendrán lugar a las 3:00, 9:00, 15:00 y 21:00.

3.  Haga clic en **Aceptar** para guardar las selecciones.

4.  En el panel de navegación de la consola de administración de WSUS, seleccione **Sincronizaciones**.

5.  Haga clic con el botón secundario o vaya al panel **Acciones** de la derecha y haga clic en **Sincronizar ahora**.

    Si no ve el panel **Acciones** en la parte derecha de la consola, en la barra de herramientas de la consola haga clic en **Ver**, haga clic en **Personalizar** y asegúrese de que está activada la casilla de verificación **Panel de acción**.

6.  Una vez finalizada la sincronización, haga clic en **Actualizaciones** en el panel izquierdo para ver la lista de actualizaciones.

Paso siguiente
--------------

[Paso 5: configurar las actualizaciones de clientes](https://technet.microsoft.com/5ae60ead-3e94-456c-a692-c0f193ea5d5a).

Recursos adicionales
--------------------

[Guía paso a paso para Windows Server Update Services 3.0 SP2](https://technet.microsoft.com/4b504edc-93b3-45b0-a7e8-d0107f1a4442)
