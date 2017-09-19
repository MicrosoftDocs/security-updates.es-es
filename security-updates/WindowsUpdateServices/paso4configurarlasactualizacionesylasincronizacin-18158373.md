---
TOCTitle: 'Paso 4: configurar las actualizaciones y la sincronización'
Title: 'Paso 4: configurar las actualizaciones y la sincronización'
ms:assetid: '734cc2ed-98be-4772-a42c-8fd38b39d864'
ms:contentKeyID: 18158373
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708447(v=WS.10)'
---

Paso 4: configurar las actualizaciones y la sincronización
==========================================================

Antes de descargar las actualizaciones, debe especificar qué actualizaciones desea descargar. En esta sección se describe cómo configurar el conjunto de actualizaciones que desea descargar.

Los procedimientos de este paso describen cómo:

-   Guardar y descargar información sobre el servidor que precede en la cadena y el servidor proxy.
-   Elegir el idioma de las actualizaciones que desea.
-   Elegir los productos para los que desea obtener actualizaciones.
-   Elegir las clasificaciones de las actualizaciones que desea.
-   Especificar la programación de sincronización para este servidor.

Los cinco procedimientos siguientes describen cómo configurar sus actualizaciones utilizando el Asistente para la configuración. Los procedimientos posteriores describen cómo realizar esta configuración desde la consola de administración de WSUS eligiendo opciones específicas.

**Guardar y descargar información sobre el servidor que precede en la cadena y el servidor proxy.**
1.  Debería haber completado la configuración del servidor que precede en la cadena y del servidor proxy en el Asistente para la configuración y ver la página **Conectar al servidor que precede en la cadena**.

2.  Haga clic en el botón **Iniciar conexión**, que guardará y cargará su configuración y obtendrá información acerca de las actualizaciones disponibles.

3.  Mientras se realiza la conexión, el botón **Detener conexión** estará disponible. Si hay problemas con la conexión, haga clic en **Detener conexión**, resuelva los problemas y reinicie la conexión.

4.  Una vez que la descarga se haya completado correctamente, haga clic en **Siguiente** para ir a la página **Elegir idiomas**, o bien seleccione una página diferente en el panel izquierdo.

**Elegir los idiomas de la actualización**
1.  La página **Elegir idiomas** permite obtener actualizaciones de todos los idiomas o de un subconjunto de idiomas. Si se selecciona un subconjunto de idiomas se ahorrará espacio en disco, pero es importante elegir todos los idiomas que necesitan todos los clientes de este servidor WSUS.

2.  Si elige obtener actualizaciones sólo para algunos idiomas, seleccione **Descargar actualizaciones sólo en estos idiomas** y seleccione los idiomas para los que desea las actualizaciones. Haga clic en **Siguiente** para ir a la página **Elegir productos**, o bien seleccione una página diferente en el panel izquierdo.

**Elegir productos de actualización**
1.  La página **Elegir productos** permite especificar los productos para los que se desea obtener actualizaciones.

2.  Puede seleccionar categorías de productos, como Windows, o productos específicos, como Windows Server 2003. Si selecciona una categoría de productos, se seleccionarán también todos los productos bajo ella. Haga clic en **Siguiente** para ir a la página **Elegir clasificaciones** o seleccione una página diferente en el panel izquierdo.

**Elegir las clasificaciones de actualización**
1.  La página **Elegir clasificaciones** le permite elegir las clasificaciones de actualización que desee obtener. Puede elegir todas las clasificaciones o un subconjunto de ellas.

2.  Haga clic en **Siguiente** para ir a la página **Configurar programación de sincronización** o seleccione una página diferente en el panel izquierdo.

**Configurar una programación de sincronización**
1.  Aparecerá la página **Establecer una programación de sincronización**, que permite elegir si realizar la sincronización manual o automáticamente.

2.  Si elige sincronizar manualmente en este servidor, tendrá que iniciar el proceso de sincronización desde la consola de administración de WSUS.

3.  Si elige sincronizar automáticamente, el servidor WSUS sincronizará en los intervalos especificados. Establezca la hora de la primera sincronización y especifique el número de sincronizaciones por día que desea que realice este servidor. Por ejemplo, si especifica que debe haber cuatro sincronizaciones al día, comenzando a las 3:00 a.m., las sincronizaciones tendrán lugar a las 3:00 a.m., 9:00 a.m., 3:00 p.m. y 9:00 p.m.

Tras haber completado todos los pasos de configuración anteriores, seleccione la página **Finalizada** en el Asistente para la configuración. Puede iniciar la consola de administración de WSUS si deja activada la casilla de verificación **Iniciar el complemento de administraciones de Windows Server Update Services** e iniciar la primera sincronización si deja activada la casilla de verificación **Iniciar sincronización inicial**.

| ![](images/Cc708447.note(WS.10).gif)Nota                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| No se pueden guardar los cambios en la configuración realizados mientras el servidor está sincronizando. Espere hasta que haya terminado la sincronización para hacer los cambios. |

![](images/Cc708447.3f774fd1-af87-47d8-8f50-a5d585687d70(WS.10).gif)

En los procedimientos siguientes se explica cómo realizar los pasos de configuración anteriores a través de la página **Opciones** de la consola de administración de WSUS:

-   Elegir productos y clasificaciones
-   Actualizar archivos e idiomas

**Elegir productos y clasificaciones**
1.  Iniciar la consola de administración de WSUS: Haga clic en **Inicio**, elija **Todos los programas** y seleccione **Herramientas administrativas**. A continuación, haga clic en **Microsoft Windows Server Update Services**.

2.  Seleccione **Opciones** bajo su servidor WSUS del panel izquierdo.

3.  En el panel central, seleccione **Productos y clasificaciones**.

4.  Aparecerá un cuadro de diálogo con dos fichas: **Productos** y **Clasificaciones**.

5.  En la ficha **Productos**, seleccione la categoría de producto o producto específico para el que desea que este servidor obtenga actualizaciones, o bien, seleccione **Todos los productos**.

6.  En la ficha **Clasificaciones**, seleccione las clasificaciones de actualización que desee, o bien, seleccione **Todas las clasificaciones**.

7.  Haga clic en **Aceptar** para guardar las selecciones.

**Actualizar archivos e idiomas**
1.  En la página **Opciones**, seleccione **Actualizar archivos e idiomas**.

2.  Aparecerá un cuadro de diálogo con dos fichas: **Actualizar archivos** y **Actualizar idiomas**.

3.  En la ficha **Actualizar archivos**, puede elegir almacenar los archivos de actualización localmente o hacer que todos los equipos cliente instalen desde Microsoft Update. Si elige almacenar los archivos de actualización en este servidor, puede elegir entre descargar sólo aquellas actualizaciones aprobadas o descargar archivos de instalación rápida.

4.  En la ficha **Actualizar idiomas**, puede elegir obtener actualizaciones para todos los idiomas (la opción predeterminada) u obtener actualizaciones sólo para los idiomas especificados. Si el servidor WSUS tiene servidores que siguen en la cadena, éstos obtendrán actualizaciones sólo en los idiomas especificados por el servidor que precede en la cadena.

5.  Haga clic en **Aceptar** para guardar los cambios.

Después de configurar la conexión de red, puede descargar las actualizaciones sincronizando el servidor WSUS.

La sincronización implica que el servidor WSUS se ponga en contacto con Microsoft Update. Tras ponerse en contacto, WSUS determina si hay nuevas actualizaciones disponibles desde la última sincronización. Dado que es la primera vez que sincroniza el servidor WSUS, todas las actualizaciones están disponibles y preparadas para su aprobación y posterior instalación. La sincronización inicial puede tardar bastante rato.

| ![](images/Cc708447.note(WS.10).gif)Nota                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En este documento se describe la sincronización con la configuración predeterminada, pero WSUS incluye opciones que permiten minimizar el uso de ancho de banda durante la sincronización. |

**Para sincronizar el servidor WSUS**
1.  En la consola de administración de WSUS, seleccione **Sincronizaciones**.

2.  Haga clic con el botón secundario del mouse o vaya al panel **Acciones** de la derecha y haga clic en **Sincronizar ahora**.

| ![](images/Cc708447.note(WS.10).gif)Nota                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Si no ve el panel **Acciones** en la parte derecha de la consola, en la barra de herramientas de la consola haga clic en **Ver**, haga clic en **Personalizar** y asegúrese de que está activada la casilla de verificación **Panel de acción**. |

Una vez finalizada la sincronización, haga clic en **Actualizaciones** en el panel izquierdo para ver la lista de actualizaciones.
