---
TOCTitle: 'Microsoft Windows Server Update Services 3.0 - WSUS y el proceso de administración de las actualizaciones'
Title: 'Microsoft Windows Server Update Services 3.0 - WSUS y el proceso de administración de las actualizaciones'
ms:assetid: 'a2674ba9-b003-4031-accd-cf57879ca8d7'
ms:contentKeyID: 18158435
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708520(v=WS.10)'
---

Microsoft Windows Server Update Services 3.0
============================================

### WSUS y el proceso de administración de las actualizaciones

Publicado: septiembre 11, 2007

Este método recomendado de Microsoft para llevar a cabo el proceso de administración de las actualizaciones consiste en un conjunto de cuatro fases continuado, tal como se muestra en la figura siguiente. Es esencial repetir este proceso de forma progresiva, a medida que las actualizaciones nuevas pasan a estar disponibles, para así mejorar y proteger el entorno de producción.

Tras la ilustración tenemos los objetivos de cada fase y ejemplos de cómo los administradores pueden usar las características de WSUS para asegurar un correcto desarrollo durante cada una de las cuatro fases del proceso. Es importante tener en cuenta que muchas de las características pueden emplearse en más de una fase.

![](images/Cc708520.wsus_um_process_01(es-es,WS.10).gif)

Las cuatro fases del proceso de administración de las actualizaciones

### 1. Valoración

Los objetivos del administrador para la fase de valoración son:

-   Establecer un entorno de producción que sea compatible con la administración de las actualizaciones para escenarios tanto rutinarios y como de urgencia.

Aunque se trata del primer paso, la fase de valoración es básicamente un proceso continuo. Por ejemplo, los administradores tienen que valorar cuántos servidores y equipos cliente necesitan actualizar, cuáles son los requisitos de almacenamiento y de ancho de banda de la red y, finalmente, qué margen de tiempo es aceptable para implementar una actualización media. Los administradores tienen también que determinar qué plataformas, productos e idiomas desean actualizar. Basándose en estos factores, los administradores pueden determinar la topología más eficaz para el escalado horizontal de los componentes de WSUS.

WSUS ofrece numerosas opciones para la configuración de los componentes de WSUS, incluida la capacidad de almacenar el contenido de las actualizaciones localmente en servidores de WSUS o la descarga de contenidos a petición desde Microsoft Update. Los administradores pueden configurar también la función Actualizaciones automáticas para descargar e instalar automáticamente las actualizaciones que falten en un equipo. WSUS ofrece opciones para administrar los equipos cliente tanto en entornos Active Directory como en entornos que no sean de Active Directory.

WSUS ofrece informes estandarizados agregados que los administradores pueden ejecutar de forma continuada. Estos informes ofrecen información completa acerca de las diferentes actividades de la implementación de WSUS, incluida información acerca de las actualizaciones que se han sincronizado para un servidor de WSUS y las actualizaciones que se instalan o faltan en cada equipo.

[](#mainsection)[Principio de la página](#mainsection)

### 2. Identificación

Los objetivos del administrador para la fase de identificación son:

-   Detectar actualizaciones nuevas de una manera adecuada.

-   Determinar si estas actualizaciones son pertinentes para el entorno de producción.

WSUS permite que los administradores determinen qué tipo de actualizaciones deben sincronizarse desde Microsoft Update y cuándo deben sincronizarse. Dado que WSUS reúne automáticamente datos acerca de todos los equipos conocidos para el servidor de WSUS para así poder determinar si una actualización es relevante, los administradores pueden consultar rápidamente cuántos equipos necesitan esa actualización y cuál sería la repercusión en la red de su implementación antes de haberla instalado en el entorno de producción.

[](#mainsection)[Principio de la página](#mainsection)

### 3. Evaluación y planeación

Los objetivos del administrador para la fase de evaluación y planeación son:

-   Probar las actualizaciones en un entorno separado del entorno de producción pero que se parezca a éste.

-   Determinar las tareas necesarias para implementar las actualizaciones en la producción, planear sus lanzamientos, crear las versiones y, a continuación, dirigir las pruebas de aceptación de dichos lanzamientos.

Al evaluar las actualizaciones en un entorno de pruebas, los administradores pueden ejecutar muchas de las características de WSUS que usarían en una implementación real. Pueden establecer los criterios y programaciones para una sincronización automática de los servidores WSUS, crear grupos de equipos y, a continuación, destinar actualizaciones para estos grupos aprobando las actualizaciones para su instalación. Durante y después de las pruebas, los administradores podrán usar los informes estandarizados que ofrece WSUS para supervisar la correcta instalación de las actualizaciones de prueba.

WSUS permite a los administradores evaluar el resultado de la instalación de las actualizaciones antes de implementarlas en un entorno de producción. Mediante la creación de un grupo de equipos y la aprobación automática de diferentes conjuntos de actualizaciones por producto, idioma y otras clasificaciones, los administradores podrán probar varios tipos de actualizaciones por medio de la automatización. Durante y después de las pruebas, los administradores pueden correlacionar los informes de las actualizaciones de WSUS con los resultados de las pruebas y así validar las actualizaciones instaladas y decidir cómo y cuándo programar las aprobaciones de descarga e instalación para el entorno de producción.

[](#mainsection)[Principio de la página](#mainsection)

### 4. Implementación

Los objetivos del administrador para la fase de implementación son:

-   Aprobar y programar las instalaciones de las actualizaciones.

-   Revisar el proceso una vez que se ha completado la implementación.

WSUS permite que los administradores especifiquen los grupos de equipos de destino y aprueben la implementación de las actualizaciones para esos grupos. Para establecer el orden en el que las actualizaciones deben implementarse, los administradores pueden usar WSUS para crear una configuración lo más eficaz posible del servidor de WSUS que precede y que sigue en la cadena para la red y los recursos de personal. Además, los administradores pueden configurar qué equipos cliente se comunicarán con los servidores de WSUS o Microsoft Update mediante una directiva de grupo o mediante scripting con la API de WSUS. El administrador puede, a continuación, usar estos informes para determinar que se hayan implementado las actualizaciones correctamente, ya sea por equipo o por grupo de destino.

[](#mainsection)[Principio de la página](#mainsection)
