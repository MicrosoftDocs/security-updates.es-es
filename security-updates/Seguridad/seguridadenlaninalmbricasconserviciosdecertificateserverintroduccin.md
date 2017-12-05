---
TOCTitle: 'Seguridad en LAN inalámbricas con Servicios de Certificate Server: introducción'
Title: 'Seguridad en LAN inalámbricas con Servicios de Certificate Server: introducción'
ms:assetid: '30f90d1c-7faa-432f-b6c8-d4927fe36229'
ms:contentKeyID: 20200268
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc527055(v=TechNet.10)'
---

Información general
===================

Publicado: octubre 11, 4

### Seguridad en LAN inalámbricas con Servicios de Certificate Server

*Seguridad en LAN inalámbricas con* *Servicios de Certificate Server* es una guía normativa que trata de las vulnerabilidades en las redes inalámbricas de hoy día. Muchas organizaciones han probado las LAN inalámbricas (WLAN) pero han acabado por resistirse a las implementaciones a gran escala o por prohibir completamente su utilización. A pesar de los muchos beneficios derivados de los sistemas inalámbricos en cuanto a productividad y tecnología, el bajo nivel de seguridad que ofrecen no contribuye a su popularidad y muchas organizaciones no se plantean la implementación de WLAN. Otras empresas han implementado un sistema WLAN 802.11 con las características limitadas de seguridad integradas o sin ningún tipo de seguridad.

Esta guía se ha actualizado para mejorar el uso de esta estructura y proporcionar información más detallada sobre las ventajas y los inconvenientes de las diferentes técnicas de seguridad inalámbrica. Incluye una guía de planeamiento para organizaciones que se encuentran considerando la implementación de una infraestructura inalámbrica, así como una guía de generación que proporciona los detalles de implementación necesarios. Presenta, además, una guía de operaciones con información completa sobre el mantenimiento de un entorno inalámbrico seguro y una guía de prueba que revela la estrategia de pruebas utilizada para comprobar el contenido de la documentación. Adicionalmente, esta guía de prueba muestra a los usuarios el modo de validar su implementación.

Al igual que el manual sobre seguridad en LAN inalámbricas con PEAP y contraseñas publicado en 2004, esta guía trata de las vulnerabilidades en las redes inalámbricas de hoy día y va dirigida a organizaciones que desean implementar la tecnología WLAN con un alto grado de confianza en su seguridad. Sin embargo, la guía está diseñada para su uso en organizaciones de varios cientos a muchos miles de usuarios de redes inalámbricas y toma como base la implementación de WLAN en Microsoft.

Proporciona información a los profesionales de TI acerca del diseño, la implementación y el funcionamiento de una infraestructura de seguridad inalámbrica con 802.1X y cifrado de WLAN, RADIUS y una infraestructura de claves públicas (PKI). Para los arquitectos de TI y aquellos que se ocupan de los planes de negocio, la guía ofrece una descripción de las vulnerabilidades de redes inalámbricas, así como una evaluación de las diferentes opciones de seguridad disponibles. Además incluye un diseño detallado de una solución global y sus componentes. Los responsables de operaciones y aquellos al cargo de las implementaciones en el entorno encontrarán en la guía instrucciones detalladas y secuencias de comandos que les permitirán implementar y administrar una infraestructura de seguridad inalámbrica satisfactoriamente.

[![](images/Cc527055.00fig0-1(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc527055.00fig0-1_big(es-es,technet.10).gif)

**Figura 1 Seguridad en LAN inalámbricas con Servicios de Certificate Server: descripción general**

#### Contenido de la solución

*Seguridad en LAN inalámbricas* *con Servicios de Certificate Server* se compone de una serie de guías, planeamiento, generación, operaciones y prueba, correspondientes a las diferentes fases de implementación de una solución de seguridad de WLAN. (Adicionalmente, uno de los apéndices constituye una guía de entrega.) Estos documentos vienen acompañados de un conjunto de herramientas que incluye un plan de proyecto de ejemplo y planes de riesgo, secuencias de comandos y archivos de configuración para la automatización de las tareas de implementación y operaciones, así como una serie detallada de casos de prueba que puede utilizar para comprobar la funcionalidad de la solución según la incorpora en su propio entorno.

##### Guía de planeamiento

Esta guía proporciona a los arquitectos de TI la información siguiente:

-   razones comerciales y técnicas para la implementación de seguridad inalámbrica.

-   estrategias para la seguridad inalámbrica.

-   una descripción detallada de las decisiones de diseño que afectan a la solución en su totalidad y a sus componentes individuales.

Adicionalmente, los capítulos sobre diseño incluyen amplias consideraciones sobre temas técnicos e información general que permiten la personalización del diseño en caso de resultar necesario en su entorno específico.

##### Guía de generación

Esta guía proporciona a los responsables de implementaciones instrucciones paso a paso para la implementación de todos los componentes de la solución: una PKI basada en Servicios de Certificate Server de Microsoft® Windows Server™ 2003, una infraestructura de RADIUS basada en el servicio de autenticación de Internet (IAS, Internet Authentication Service) de Microsoft y detalles sobre la configuración de clientes y puntos de acceso (AP, Access Point) inalámbrico. Cada capítulo presenta los procedimientos detallados para instalar y proteger el sistema operativo, configurar los componentes de software e integrarlos en la solución. Los pasos principales aparecen vinculados a procedimientos de comprobación que contribuyen a evitar errores.

##### Guía de operaciones

Esta guía describe los procedimientos para el mantenimiento a largo plazo de los componentes de la solución. Las soluciones de Microsoft para la administración (MSM, Microsoft Solutions for Management) sirven de base a esta guía, que proporciona una serie completa de tareas e instrucciones para operar, supervisar, modificar y facilitar el funcionamiento correcto de los componentes de IAS y los Servicios de Certificate Server. Incluye información sobre tareas de configuración para implementar el sistema de administración y tareas de operaciones diarias y semanales. Adicionalmente se proporcionan secuencias de comandos de supervisión y comprobación, procedimientos de copia de seguridad y recuperación, así como herramientas y técnicas para la solución de problemas que puedan presentarse.

##### Guía de prueba

Esta guía explica la estrategia de prueba global utilizada por Microsoft para validar esta solución y describe los casos de prueba principales que puede usar para validar la solución en sus laboratorios. La solución incluye la serie completa de casos de prueba.

#### Descargar,

La solución y las herramientas y plantillas asociadas están disponibles para la [descarga](http://go.microsoft.com/fwlink/?linkid=14844) en el Centro de descargas de Microsoft.

#### Compatibilidad

Para obtener más información sobre la compatibilidad en la solución de los componentes de Microsoft Windows Server 2003, incluidas rutas de traslado, aspectos de soporte, recursos y niveles de compatibilidad, consulte el sitio Web de [ayuda y soporte técnico de Microsoft](http://support.microsoft.com/) en http://support.microsoft.com/.

#### Recursos adicionales

Otros recursos que pueden resultar de utilidad incluyen:

-   [Kits de recursos e implementación de Windows](http://www.microsoft.com/windows/reskits/) en http://www.microsoft.com/windows/reskits/.

-   Sitio Web del [centro de recursos de seguridad de Microsoft TechNet](http://www.microsoft.com/technet/security/default.mspx) en http://www.microsoft.com/technet/security/default.mspx.

-   Página [Wi-Fi](http://www.microsoft.com/wifi) del sitio Web de Microsoft Windows Server 2003 en http://www.microsoft.com/wifi.

-   Sitio Web de la asociación [Wi-Fi Alliance](http://www.wi-fialliance.org/) en http://www.wi-fialliance.org/OpenSection/index.asp.

-   La página Web del [comité de estándares de IEEE 802 LAN/MAN](http://www.ieee802.org/) en http://www.ieee802.org/.

#### Comuníquenos su opinión

Microsoft valora su opinión acerca de este material. Especialmente le agradeceremos el tiempo que se tome en responder las preguntas siguientes:

-   ¿En qué medida ha resultado útil la información proporcionada?

-   ¿Los procedimientos paso a paso fueron precisos?

-   ¿Los capítulos le resultaron fáciles de leer e interesantes?

-   ¿Cómo calificaría esta guía en líneas generales?

Envíe su opinión a [SecWish@Microsoft.com](mailto:secwish@microsoft.com?subject=feedback%20re:%20microsoft%20solution%20for%20secure%20wireless%20lans)

#### Créditos

Administración de versiones: Flicka Crandell

Autoría: Ian Hellen y Stirling Goetz

Contribuciones: Carsten Kinder y Andrew Hawkins

Equipo de pruebas: Mehul Mediwala y Jon Stone

Edición: Wendy Cleary, John Cobb y Steve Wacker

Dirección del programa: Jeff Coon, Karl Grunwald y Bomani Siwatu

Administración de versiones: Flicka Crandell

[](#mainsection)[Principio de la página](#mainsection)

**Descargar la solución completa**

[Seguridad en LAN inalámbricas con Servicios de Certificate Server](http://go.microsoft.com/fwlink/?linkid=14844)

[](#mainsection)[Principio de la página](#mainsection)
