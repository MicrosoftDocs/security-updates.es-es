---
TOCTitle: 'Apéndice C: Guía de entrega'
Title: 'Apéndice C: Guía de entrega'
ms:assetid: '10a01b29-c3de-4d20-9fee-ad444046b4ad'
ms:contentKeyID: 20112542
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd458720(v=TechNet.10)'
---

Apéndice C: Guía de entrega
===========================

Publicado: 10/11/2004 12:00:00 a.m. | Actualizado: 24/11/2004 12:00:00 a.m.

##### En esta página

[](#edaa)[Introducción](#edaa)  
[](#ecaa)[Microsoft Solution Framework](#ecaa)  
[](#ebaa)[Microsoft Operations Framework](#ebaa)  
[](#eaaa)[Resumen](#eaaa)

### Introducción

En esta guía se proporciona información general dirigida a responsables de planes de empresa, arquitectos de TI o gerentes de proyectos en relación con las prácticas recomendadas de Microsoft para coordinar e implementar la solución *Seguridad en LAN inalámbricas con Servicios de Certificate Server*. En esta guía también se incluyen punteros a los siguientes recursos:

-   Microsoft Solution Framework (MSF).

-   Microsoft Operations Framework (MOF).

-   Guía de administración de riesgos de seguridad (GARS).

-   Fuentes de los conocimientos previos y cursos sobre los temas fundamentales de esta solución.

-   Descripciones de las herramientas y recursos proporcionados con la solución, y específicos de ella, para ayudarle a planear, programar y administrar la implementación.

[](#mainsection)[Principio de la página](#mainsection)

### Microsoft Solution Framework

MSF proporciona prácticas probadas para planear, crear e implementar diversas soluciones de tecnología. MSF combina prácticas recomendadas del diseño y desarrollo de software con la creación e implementación de infraestructuras en un solo ciclo de vida de proyecto para dirigir soluciones de tecnología de todo tipo. MSF ayuda a las organizaciones a alcanzar el delicado equilibrio de flexibilidad a la que vez que se cumplen los compromisos y se reducen los riesgos. MSF proporciona una gran cantidad de recursos a los clientes de Microsoft para que los descarguen de MSDN en la página Web de [Microsoft Solutions Framework (MSF)](http://www.microsoft.com/msf/) en www.microsoft.com/MSF/.

Entre los enfoques fundamentales de MSF se incluyen:

-   Administración de conocimientos

-   Administración de proyectos

-   Administración de riesgos

-   Modelo de equipo

-   Modelo de proceso

#### Administración de conocimientos

Al comienzo de un proyecto de solución, antes de la fase de visión/alcance, la organización tiene que comprender claramente los siguientes puntos:

-   Su escenario de seguridad específicos y los requisitos:

    -   Para atender las necesidades de las organizaciones que inician implementaciones de soluciones de seguridad, Microsoft Solutions for Security (MSS) ha creado la [GARS](http://www.microsoft.com/latam/technet/articulos/adminriesgos/default.mspx). La GARS es un proceso detallado que se utiliza para determinar las amenazas y vulnerabilidades que pueden tener un efecto importante en una determinada organización. Debido a que cada organización tiene necesidades de negocios diferentes, es imposible crear una lista de vulnerabilidades que tengan el mismo impacto en cada entorno. Por lo tanto, la GARS permite que una organización genere de forma incremental su seguridad e identifique áreas posibles que requieran soluciones en el futuro.

-   Sus competencias internas:

    -   Esta solución está diseñada para que la comprenda fácilmente y la implemente de forma oportuna un profesional con la certificación Microsoft Certified Systems Engineer (MCSE) con dos años de experiencia y que, como mínimo, esté familiarizado de forma básica con los siguientes materiales de Microsoft Official Curriculum (MOC):

        -   Curso 2810: Fundamentos de seguridad de redes

        -   Curso 2821: Designing and Managing a Public Key Infrastructure

        -   Curso 2830: Designing Security for Microsoft Networks

        -   Curso 2150: Designing a Secure Microsoft Windows 2000 Network

        -   Curso 2153: La implementación de una infraestructura de red de Microsoft Windows 2000

#### Administración de proyectos

MSF proporciona un amplio y variado conjunto de materiales para ayudar a las organizaciones en la administración de proyectos de implementación de aplicaciones y de infraestructuras. Esta solución emplea un subconjunto de estas herramientas y metodologías de MSF para derivar una serie de herramientas de administración de proyectos diseñadas para ayudar a los responsables de planes de empresa o arquitectos de TI a implementar esta solución, entre las que se incluyen:

-   Una programación de Microsoft® Project de ejemplo en la que se detallan las tareas, el tiempo necesario y los recursos para una implementación de referencia de la solución que se incluye en el kit de descarga de herramientas y recursos proporcionado con esta solución. (Securing\_Wireless\_LANs\_Master\_Project\_Sched.mpp)

-   También se incluyen un análisis de costos de proyecto de ejemplo derivado directamente de la programación de proyecto de ejemplo y detalles de implementación de referencia de Microsoft. De este modo se proporciona una aproximación a los costos de hardware, software y mano de obra para implementar la solución. Esta hoja de cálculo está diseñada para ser una plantilla que el usuario final puede modificar para reflejar el número de servidores necesarios y los costos de mano de obra de la organización para elaborar rápidamente una estimación del costo de implementación. (Secure Wireless LAN Cost Analysis.xls)

#### Administración de riesgos

Un elemento fundamental de la administración de proyectos es el control de los riesgos inherentes de un proyecto. La mayoría de las personas asocian el concepto de riesgo con la posibilidad de pérdida, incluyendo valor, control, funcionalidad, calidad o tiempo. No obstante, los riesgos también proceden de la incertidumbre que rodea a las decisiones de proyecto y sus resultados, que pueden ocasionar la imposibilidad de maximizar la ganancia de oportunidades.

MSF afronta la administración agresiva de riesgos mediante el planeamiento de estrategias de mitigación y planes de contingencia antes de que estos riesgos se puedan convertir en problemas reales o en factores de bloqueo del éxito.

Para que los profesionales de TI puedan comprender de un modo más exhaustivo los riesgos a los que se pueden enfrentar al considerar la implementación de esta solución, de este enfoque de MSF se deriva una evaluación de riesgos de ejemplo y se basa en una implementación real de esta solución, que se proporciona en la descarga de herramientas y recursos. (Secure Wireless LAN Risk Analysis.xls)

#### Modelo de equipo

MSF proporciona tanto un marco para separar las funciones y responsabilidad de las iniciativas de implementación de aplicaciones y de infraestructuras como las herramientas para definir las funciones y sus interacciones. Las funciones son:

-   **Administración del programa**: el recurso de esta función administra la especificación del proyecto y actúa de arquitecto principal, mantiene el programa del proyecto e informe del estado del mismo, dirige la administración de evaluaciones y de riesgos, facilita la negociación dentro del equipo y coordina la toma de decisiones sopesando las características, el programa y los recursos.

-   **Administración de productos**: el recurso de esta función actúa de defensor del cliente y administra los requisitos del mismo, dirige la visión/alcance compartido del proyecto, desarrolla y mantiene la situación de negocios y dirige las decisiones sopesando las características, el programa y los recursos.

-   **Desarrollo**: el recurso de esta función especifica las características del diseño de la solución, estima el tiempo y el esfuerzo necesario para completar cada característica y crea o supervisa la creación de la solución.

-   **Pruebas**: el recurso de esta función comprueba la funcionalidad de la operación y garantiza que todos los problemas conocidos están documentos.

-   **Experiencia del usuario**: el recurso de esta función actúa de defensor del usuario, administra los requisitos de los usuarios, dirige la toma de decisiones sopesando la facilidad de uso y el rendimiento y desarrolla y proporciona cursos a los usuarios.

-   **Administración de versiones**: el recurso de esta función actúa de defensor de los canales de operaciones, soporte técnico y entrega, administra el aprovisionamiento, coordina la implementación de la solución y dirige la toma de decisión sopesando la capacidad de administración y la compatibilidad.

#### Modelo de proceso

El modelo de proceso es el elemento principal de MSF y representa las prácticas recomendadas que Microsoft ha identificado, utilizado y optimizado a partir de sus propias experiencias en la coordinación de proyectos de implementación de aplicaciones e infraestructuras a gran escala. Entre los principales conceptos del modelo de proceso de MSF se incluyen:

-   **Administración de los factores que se deben considerar**: debe existir un equilibrio entre los recursos (personas y dinero), el programa (tiempo) y las características (alcance). Si se tiene que cambiar uno de estos elementos, también se deben cambiar los demás en cierta medida.

-   **Enfoque orientado a hitos**: los hitos constituyen un tema clave en MSF. Se utilizan para planear y supervisar el progreso del proyecto y sirven de puntos intermedios en el proyecto. Se utilizan para medir el progreso, garantizar la sincronización con las expectativas del cliente, coordinar los componentes con otros miembros del equipo y hablar con los participantes o patrocinadores en relación con el progreso y la dirección del proyecto.

-   **Enfoque iterativo**: MSF recomienda que las soluciones se desarrollen mediante la creación, prueba e implementación de la funcionalidad básica en primer lugar y, posteriormente, agregar periódicamente conjuntos de características. Este enfoque se basa en documentos “vivos” que se actualizan periódicamente a medida que se agregan nuevos conjuntos de características. Se basa en el uso de la creación diaria de la solución, la medición frecuente del progreso y el seguimiento y control continuos de los elementos del proyecto

-   **Fases e hitos periódicos**: para cada una de las siguientes fases del proyecto hay disponible en línea en [MSF](http://www.microsoft.com/msf/) una amplia variedad de valiosas herramientas y plantillas de proyecto:

    -   **Fase de visión**

        -   Plantilla de visión/alcance

        -   Plantilla de estructura del proyecto

        -   Herramienta de evaluación del riesgo y herramientas de administración

    -   **Fase de planeamiento**

        -   Plantillas de empresa, usuario, sistema y otros requisitos

        -   Plantillas de especificaciones funcionales

        -   Plantillas de desarrollo, administración de riesgos, pruebas, cursos, calidad y planeamiento

    -   **Fase de creación**

        -   Plantillas para componentes de contenido y código

        -   Plan de prueba y plantillas de casos de prueba (se incluyen un plan de prueba de la solución detallado y casos de prueba en el capítulo 13, “Cómo probar la solución”).

    -   **Fase de implementación**

        -   Plantillas de implementación y comunicación del plan

MSF está estrechamente relacionado con [MOF](http://technet.microsoft.com/es-es/library/bb232042.aspx), que es el enfoque de Microsoft para lograr la confiabilidad, la disponibilidad y la facilidad de administración de sistemas de producción clave. MOF se basa en un conjunto aceptado internacionalmente de prácticas recomendadas en la administración de servicios de TI denominada IT Infrastructure Library ([ITIL](http://www.itil.co.uk/)). MSF y MOF han sido diseñados tanto para interaccionar entre sí como para desarrollarse de forma independiente.

[](#mainsection)[Principio de la página](#mainsection)

### Microsoft Operations Framework

Microsoft Operations Framework (MOF) proporciona orientación técnica que permite a las empresas aumentar la fiabilidad, disponibilidad, compatibilidad y manejabilidad de los productos y las tecnologías de Microsoft que resultan fundamentales para su labor. La guía de operaciones de esta solución se basa en MOF y describe las tareas adecuadas y necesarias para hacer funcionar, ofrecer soporte técnico, optimizar y cambiar la solución.

MOF proporciona orientación operativa y valiosa en notas del producto, guías de operaciones, herramientas de evaluación, prácticas recomendadas, estudios de casos, plantillas, herramientas de asistencia y servicios. Esta puede ayudarle a afrontar las cuestiones de personal, de proceso, tecnológicas y administrativas que suelen surgir en las operaciones en cualquier entorno de TI distribuido, heterogéneo y complejo.

MOF y MSM se tratan en más detalle en el capítulo 10, “Introducción a la guía de operaciones”.

[](#mainsection)[Principio de la página](#mainsection)

### Resumen

Esta guía de entrega proporciona información general acerca de las prácticas recomendadas de Microsoft para coordinar e implementar la solución para *Seguridad en LAN inalámbricas con Servicios de Certificate Server.*

[](#mainsection)[Principio de la página](#mainsection)
