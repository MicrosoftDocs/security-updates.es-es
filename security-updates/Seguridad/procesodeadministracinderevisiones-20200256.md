---
TOCTitle: Proceso de administración de revisiones
Title: Proceso de administración de revisiones
ms:assetid: '6ff9a7c3-6adf-4a30-94a0-a0666c4d05d3'
ms:contentKeyID: 20200256
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc700833(v=TechNet.10)'
---

Proceso de administración de revisiones
=======================================

### Fase 4: Implementación

Actualizado: junio 1, 2007

#### En esta página

[](#eyc)[Descripción del módulo](#eyc)
[](#emd)[Objetivos](#emd)
[](#ewd)[Aplicable a](#ewd)
[](#ezd)[Uso del módulo](#ezd)
[](#ene)[Información general](#ene)
[](#ecf)[Preparación de la implementación](#ecf)
[](#ewaac)[Implementar la actualización de software en equipos de destino](#ewaac)
[](#e3eac)[Revisión posterior a la implementación](#e3eac)
[](#erfac)[Resumen](#erfac)
[](#ebgac)[Pasos siguientes](#ebgac)
Descripción del módulo
----------------------

En este módulo se describe la cuarta fase, Implementación, del proceso de administración de actualizaciones de cuatro fases. La fase de implementación se centra en la instalación correcta de las actualizaciones de software aprobadas en su entorno de producción, de manera que cumpla con todos los requisitos de cualquier contrato de nivel de servicio (SLA) de implementación que esté vigente.

El objetivo de este módulo es describir los principios de la fase de implementación del proceso de administración de actualizaciones, así como presentar los tipos de tareas que permiten llevar a cabo la implementación mediante Microsoft Windows Server Update Service (WSUS) y Microsoft Systems Management Server (SMS).

N**ota**: la versión beta 2 del próximo lanzamiento de SMS, denominada System Center Configuration Manager 2007, está disponible para su descarga en <http://www.microsoft.com/technet/sms/2007/evaluate/download.mspx>. Con excelentes mejoras en simplicidad, configuración, implementación y seguridad, Configuration Manager 2007 simplifica en gran medida la implementación del sistema, la automatización de tareas, la administración del cumplimiento de normativas así como la administración de la seguridad basada en directivas, lo cual permite la mejora de la agilidad empresarial.

Después de haber leído este módulo podrá planear las tareas que necesita para lograr correctamente:

-   Ejecutar la actualización de software aprobada.

-   Implementar cualquier contramedida necesaria.

Sin un proceso de implementación, no dispondrá del conjunto de tareas y actividades probado y probado que se requiere para implementar una actualización de software en su entorno de producción o implementar cualquier contramedida necesaria o pasos de mitigación.

[](#mainsection)[Principio de la página](#mainsection)

Objetivos
---------

Use este módulo para:

-   Prepararse para la implementación.

-   Implementar una actualización de software en equipos de destino.

-   Revisar la implementación posteriormente.

[](#mainsection)[Principio de la página](#mainsection)

Aplicable a
-----------

Este módulo se aplica a todos los productos y tecnologías de Microsoft.

[](#mainsection)[Principio de la página](#mainsection)

Uso del módulo
--------------

Aunque las tareas básicas necesarias para realizar la implementación mediante WSUS Y SMS se describen en este módulo, también puede encontrar instrucciones más detalladas en las bibliotecas técnicas indicadas a continuación.

Para obtener el máximo rendimiento de este módulo, debe realizar las siguientes acciones:

-   Lea el capítulo Introducción del módulo "Proceso de administración de actualizaciones". En este capítulo se ofrece información general de todas las fases del proceso de administración de actualizaciones de cuatro fases y se proporciona una introducción a las herramientas disponibles para aplicar la administración de actualizaciones en los entornos del sistema operativo Microsoft Windows.

-   Use las bibliotecas técnicas de WSUS y SMS para obtener materiales de referencia más detallados. Estas bibliotecas se encuentran en:

    -   [Biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true)

    -   [Biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx)

[](#mainsection)[Principio de la página](#mainsection)

Información general
-------------------

La fase de implementación es la cuarta fase del proceso de administración de actualizaciones que se muestra en la figura 1.

![](images/Cc700833.gr35(es-es,TechNet.10).gif)

**Figura 1. El proceso de administración de actualizaciones**

La fase de implementación se centra en las tareas y actividades que se requieren para implementar una actualización de software en el entorno de producción. Se pueden requerir tareas adicionales para implementar alguna contramedida o paso de mitigación.

El punto de entrada para esta fase es una determinación de que la actualización de software está lista para implementarse en producción y que se ha obtenido la aprobación para implementarla.

El objetivo para la fase de implementación es transferir la actualización de software aprobada y cualquier contramedida a su entorno de producción.

La implementación de una actualización de software consta de las siguientes actividades:

-   Preparación de la implementación.

-   Implementación de la actualización de software en equipos de destino.

-   Revisión posterior a la implementación.

[](#mainsection)[Principio de la página](#mainsection)

Preparación de la implementación
--------------------------------

El entorno de producción se debe preparar para cada nueva versión. Los pasos necesarios para preparar la actualización de software para la implementación incluyen los siguientes:

-   Comunicación de la programación de implementación a la organización.

-   Si está implementado WSUS:

    -   almacenamiento provisional de las actualizaciones en los servidores WSUS.

-   Si está implementado SMS:

    -   Importación de programas y anuncios del entorno de prueba.

    -   Asignación de los puntos de distribución.

    -   Almacenamiento de las actualizaciones en los puntos de distribución.

    -   Selección de grupos de implementación.

Para obtener más información acerca de la preparación de la implementación en entornos WSUS o SMS, consulte la [biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true) o la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).

### Comunicar el programa de implementación a la organización

Es importante informar a los usuarios finales y administradores acerca del lanzamiento inminente de una actualización. Debe enviar un mensaje claro y fácilmente identificable a los usuarios y administradores, el cual debe informarles de la actualización y proporcionarles información de cómo instalarla. Debe marcar el correo para seguimiento con el fin de recordar a los usuarios y administradores de las acciones que deben realizar.

Cuando implemente una actualización en los equipos de escritorio fuera de horas de actividad principales, el mensaje de correo electrónico debe informar a los usuarios que durante la noche dejen sus equipos en una fecha especificada. Si este mensaje tiene una marca de seguimiento tal como se muestra en la figura 2, los usuarios recibirán un recordatorio el 30 de mayo a las 4:30 p.m. de 2003 para que dejen sus equipos encendidos durante la noche.

[![](images/Cc700833.gr36(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc700833.gr36(es-es,technet.10).gif)
**Figura 2. Esta captura de pantalla muestra cómo un mensaje de correo electrónico marcado para seguimiento se puede usar como recordatorio**

Si usa WSUS, el proceso de comunicaciones incluye consideraciones adicionales que dependen de los parámetros de la directiva de instalación y descarga para el cliente WSUS:

-   **Notificación de descarga e instalación.** Un usuario que haya iniciado sesión con derechos de administrador local tendrá que seleccionar la opción para descargar la actualización cuando aparezca la notificación de **nueva actualización disponible para descarga** en la barra de tareas. Para completar la instalación, tendrá que instalar la actualización de software cuando aparezca la notificación de **nueva actualización disponible para instalación**.

-   **Descarga automática y notificación de instalación.** El cliente de Actualizaciones automáticas puede descargar automáticamente actualizaciones recientemente aprobadas que se aplican al equipo cliente. Para instalar las actualizaciones, un usuario que ha iniciado sesión con derechos de administrador local tendrá que seleccionar la opción para instalar la actualización de software cuando aparezca la notificación de **nueva actualización de software disponible para instalación**.

-   **Descarga automática y programación de la instalación.** Un usuario que ha iniciado sesión con derechos de administrador local puede instalar una actualización antes de la hora de instalación programada o retrasar el inicio del sistema (si es necesario) después de que se finalice la instalación. Para usuarios sin derechos de administrador local, la actualización se instalará en segundo plano en el tiempo programado. Estos usuarios únicamente pueden retrasar un reinicio del equipo, si se ha habilitado la configuración de la directiva **No reiniciar automáticamente para instalaciones de actualizaciones automáticas**.

Para obtener información más detallada acerca del uso de WSUS en la fase de implementación, consulte la [biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true).

### Preparación de la implementación con SMS

Si usa SMS 2003, hay varios pasos adicionales que debe considerar para preparar la implementación:

-   Importación de programas y anuncios de su entorno de prueba. Primero, los paquetes que se han creado y probado en el entorno de prueba se deben importar al entorno SMS 2003 de producción.

-   **Asignación de los puntos de distribución.** Debe asignar puntos de distribución; los binarios de la actualización de software se deben colocar en puntos de distribución en todos los sitios donde se encuentren clientes de destino. Si se puede usar el **Asistente para distribuir actualizaciones de software**, los puntos de distribución se pueden asignar a través del asistente (y se deben corregir manualmente una vez se ha creado el paquete).

-   **Almacenamiento de las actualizaciones en puntos de distribución**. El siguiente paso es asegurarse de que las copias de todos los archivos estén colocadas en los servidores de punto de distribución. El proceso para enviar los binarios de la actualización de software a los puntos de distribución implica enviar los archivos entre sitios de SMS y desde sitios de SMS a puntos de distribución local.

-   **Selección de los grupos de implementación.** Si usa el **Asistente para distribuir actualizaciones de software** para distribuir una nueva actualización de software, no tiene que dirigirse a los equipos de forma precisa. Esto se debe a que el asistente implementa un agente inteligente que se invoca cuando se tiene que instalar una nueva actualización. El agente determina automáticamente si una actualización es aplicable a ese equipo (y si ya se instaló). Si las actualizaciones se distribuyen a través de una colección y un paquete personalizado, es probable que tenga que crear una o más consultas de SMS para implementar la actualización en los equipos apropiados.

Para obtener más información acerca del uso de SMS en la fase de implementación, consulte la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).

[](#mainsection)[Principio de la página](#mainsection)

Implementar la actualización de software en equipos de destino
--------------------------------------------------------------

El proceso que use para implementar la actualización de software en el entorno de producción dependerá del tipo y naturaleza del lanzamiento, así como del mecanismo de lanzamiento que seleccione.

También dependerá considerablemente de si la actualización del software es una emergencia. Debido a la urgencia asociada a los cambios de la emergencia, habrá algunas diferencias en la forma en que los implemente. Esas diferencias se destacarán en esta sección.

Idealmente, debe realizar el lanzamiento de las actualizaciones de software a través de una implementación por fases, lo que reduce las consecuencias de los errores o efectos negativos que podrían presentarse en la distribución inicial de una actualización de software.

Los pasos necesarios para implementar una actualización de software en producción incluyen los siguientes:

-   Anunciar la actualización de software a los equipos cliente.

-   Controlar y notificar del progreso de la implementación.

-   Administrar las implementaciones con error.

### Anunciar la actualización de software a los equipos cliente

Si usa WSUS y no es necesaria una ejecución por fases, sólo tiene que aprobar la actualización en el servidor WSUS principal para que ésta esté disponible para los clientes. Los clientes WSUS comenzarán a descargar la actualización que se aprobó recientemente, ya sea en el siguiente ciclo de detección o cuando lo indique el administrador local (si el cliente de actualizaciones automáticas está configurado para notificar al administrador local cuando hay nuevas actualizaciones disponibles).

Sin embargo, si va a haber una ejecución por fases, primero debe aprobar la actualización únicamente en el servidor WSUS principal. A continuación, una vez se haya implementado correctamente la actualización en los clientes admitidos por ese servidor, debe habilitar la sincronización de la lista de aprobaciones en el servidor WSUS secundario que admite clientes en la siguiente fase de la ejecución.

Para obtener información más detallada acerca del uso de WSUS en la fase de implementación, consulte la [biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true).

Si usa SMS y el **Asistente para distribuir actualizaciones de software**, se crea automáticamente un anuncio repetitivo que ejecuta el agente de instalación de actualizaciones de software en los equipos de la colección de destino. Si es necesario, puede cambiar el valor predeterminado de siete días del intervalo de repetición. Por ejemplo, una colección que incluye servidores puede ejecutar el agente una vez al día. Al usar el mismo paquete y programa, puede crear anuncios para varias colecciones, si debe crear distintas programaciones para distintos tipos de equipos. Si la ejecución se realiza por partes, debe modificar la consulta después de cada fase, de manera que se incluyan los clientes de la siguiente fase.

Si no está usando el **Asistente para distribuir actualizaciones de software**, cuando un anuncio está configurado para instalar una actualización, también debe configurar su programación para que se repita a intervalos. Se hace de esta manera para que una instalación con error se pueda reintentar automáticamente. El intervalo de repetición de anuncios se tiene que elegir cuidadosamente, porque los clientes que ya han instalado correctamente la actualización permanecerán en la colección de destino hasta que se haya recopilado un nuevo inventario, que puede activar el propio programa de instalación, o hasta que el inventario se haya actualizado en la base de datos de SMS y la colección se haya evaluado de nuevo. Por lo tanto, el programa se puede ejecutar de nuevo en un cliente que lo ha ejecutado correctamente una vez. Por este motivo, es esencial que el programa primero ejecute comprobaciones para ver si están instaladas las actualizaciones de software y que salga sin retrasos si están instaladas.

Para obtener más información acerca del uso de SMS en la fase de implementación, consulte la [biblioteca técnica Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).

**Solicitud de cambio de emergencia**

Para obtener más información acerca de cómo administrar las solicitudes de cambio de emergencia mediante WSUS, consulte la [biblioteca técnica de Windows Server Update Services (WSUS) y para obtener más información acerca de cómo administrar las](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true)solicitudes de cambio de emergencia mediante SMS, consulte la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).

Controlar e informar del progreso de la implementación

Los equipos pueden no instalar una actualización debido a diversos motivos, como los siguientes:

-   El equipo está sin conexión.

-   El equipo se está reconstruyendo o se está volviendo a crear la imagen.

-   El equipo no tiene suficiente espacio en disco.

-   En entornos WSUS:

    -   El equipo no se comunica con el servidor WSUS (para equipos que tienen el cliente de actualizaciones automáticas).

    -   El servicio del cliente de actualizaciones automáticas se ha detenido.

-   En entornos SMS:

    -   Los clientes SMS de los equipos no se comunican con los servidores del sitio SMS.

    -   Se detenido el servicio de agente del equipo, ya sea por parte del usuario o como parte de mantenimiento.

-   En entornos SMS 2003:

    -   El equipo tiene MSXML 3 hasta SP1 (SMS 2003 requiere MSXML 3.0 SP4).

Para obtener más información acerca del uso de WSUS en la fase de implementación, consulte la [biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true).

Para supervisar la publicación correcta de actualizaciones, puede usar el **Visor de estado de anuncio** para mostrar el estado de implementación de los anuncios, según sus mensajes de estado. Los mensajes de estado notifican únicamente de si se ejecutó el anuncio repetitivo, no si se instaló la actualización. Para obtener esta información, debe analizar los mensajes de estado para determinar cuándo se ejecutó correctamente el programa **Instalación de revisión** por última vez en cada cliente; si el tiempo desde que éste se ejecutó es más largo que el período de repetición para algunos clientes, debe realizar una investigación.

Para las actualizaciones de software identificadas a través de Security Updates Inventory Tool, Inventory Tool for Microsoft Updates o Microsoft Office Inventory Tool for Updates, puede usar los informes integrados para comprobar si la implementación fue correcta. El informe de cumplimiento por identificador de software se puede usar para proporcionar un resumen del número total de sistemas en los que se instaló la actualización o en los que aún no se ha instalado, así como el estado relacionado con la distribución de la actualización de software.

Para obtener más información acerca del uso de SMS en la fase de implementación, consulte la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).

### Administrar las implementaciones con error

Si se producen excepciones durante una implementación normal, debe tener suficiente tiempo para detenerse, determinar la causa y volver a implementar. Sin embargo, durante una implementación de emergencia, el tiempo disponible para procesar y valorar la causa será mucho menor.

Su organización también puede decidir que una implementación no es correcta y, por lo tanto, debe detenerla y volver a ejecutarla. Debe tener un plan establecido para detener la ejecución, desinstalar las actualizaciones con error y volver a implementarlas.

#### En entornos WSUS

Para implementaciones con error en un entorno WSUS, debe cancelar la aprobación de la actualización en el servidor WSUS para evitar instalaciones posteriores. En los clientes que ya han descargado la actualización, pero que aún no la han instalado, los administradores locales pueden eliminarla manualmente de la lista de las actualizaciones que se deben instalar. Si un equipo ha instalado una actualización aprobada, la actualización únicamente se puede eliminar mediante el servicio **Agregar o quitar programas** del Panel de control (si la actualización se puede desinstalar). Para obtener más información acerca del uso de WSUS en la fase de implementación, consulte la [biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true).

#### En entornos SMS

Si usa SMS, la administración de implementaciones con error implica cuatro tareas principales:

-   La interrupción de la implementación del paquete activo hasta que el problema se haya resuelto.

-   La identificación y solución del problema; es decir, investigar por qué la implementación no se realizó correctamente.

-   Anunciar de nuevo el paquete.

-   La desinstalación de la actualización de software, a través de la creación de un paquete de desinstalación (si la actualización se puede desinstalar).

Para obtener más información acerca del uso de SMS en la fase de implementación, consulte la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).

[](#mainsection)[Principio de la página](#mainsection)

Revisión posterior a la implementación
--------------------------------------

La revisión posterior a la implementación se debe realizar generalmente después de una a cuatro semanas una vez se haya llevado a cabo la implementación del lanzamiento para identificar las mejoras que se deben realizar en el proceso de administración de actualizaciones.

Una agenda habitual para una revisión incluye:

-   Asegurarse de que las vulnerabilidades se han agregado a sus informes de examen de vulnerabilidad y estándares de directiva de seguridad, de manera que el ataque no tenga oportunidad de repetirse.

-   Asegurarse de que las imágenes creadas se hayan actualizado para incluir las actualizaciones de software más recientes después de la implementación.

-   Describir los resultados planeados en comparación con los reales.

-   Describir los riesgos asociados al lanzamiento.

-   Revisar el rendimiento de la organización a través del incidente. Aproveche esta oportunidad para mejorar su plan de respuesta para que incluya cualquier lección aprendida.

-   Describir los cambios en sus intervalos de servicio.

-   Evaluar los daños y costos totales del incidente, incluidos tanto los costos de recuperación como de tiempo de inactividad.

-   Crear otra línea de base o actualizar la existente para el entorno.

[](#mainsection)[Principio de la página](#mainsection)

Resumen
-------

Durante la fase de implementación, debe haber llevado a cabo las siguientes actividades clave:

-   Establecer el orden en que se instalan las actualizaciones de software en producción.

-   Inspeccionar el entorno de producción para asegurarse de que haya podido realizar la actualización de software.

-   Colocar los archivos de la actualización de software en servidores WSUS y puntos de distribución SMS.

-   Implementar la actualización de software en producción.

-   Explorar de nuevo el entorno para evaluar el éxito y actualizar cualquier equipo que no haya instalado la actualización de software.

-   Realizar una revisión del proceso de administración de actualizaciones una vez completada la implementación.

[](#mainsection)[Principio de la página](#mainsection)

Pasos siguientes
----------------

Después de implementar la actualización de software, debe volver a la fase de valoración, donde puede continuar con:

-   El inventario o detección de activos informáticos existentes.

-   La valoración de las vulnerabilidades y amenazas de seguridad.

-   La determinación de la mejor fuente de información acerca de las actualizaciones de software.

-   La valoración de la infraestructura de distribución de software existente.

-   La valoración de la efectividad operativa.

**Descargar la solución completa**

[Administración de revisiones con SMS 2003](http://www.microsoft.com/downloads/details.aspx?familyid=959ee7d6-7ddf-409a-9522-7d270bdcf12a&displaylang=en)

[](#mainsection)[Principio de la página](#mainsection)
