---
TOCTitle: Información general de la Guía de seguridad de Windows XP
Title: Información general de la Guía de seguridad de Windows XP
ms:assetid: 'fb31fa9b-58c8-4b6c-aa93-f49128e79916'
ms:contentKeyID: 20200260
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163061(v=TechNet.10)'
---

Guía de seguridad de Windows XP
===============================

### Información general

Publicado: 22/05/2003 | Actualizado: 20/10/05

Un entorno de TI es tan seguro como su eslabón más débil. Por desgracia, en los proyectos relacionados con la seguridad los sistemas operativos cliente se pasan a menudo por alto. Cuando su organización planee implementar Microsoft® Windows® XP Professional con Service Pack 2 (SP2), asegúrese de que ese aspecto de la seguridad constituya una parte esencial de sus planes de implementación.

Aunque la instalación predeterminada de Windows XP sea bastante segura, es importante recordar la necesidad de alcanzar un equilibrio entre seguridad, utilidad y funcionalidad de los equipos cliente en su entorno. Una comprensión exhaustiva de este equilibrio sitúa a su organización en posición de maximizar la seguridad de la implementación de Windows XP.

En la guía se proporcionan recomendaciones específicas acerca de cómo configurar la seguridad de equipos en los que se ejecuta Windows XP con SP2 en tres entornos distintos:

-   **Cliente de empresa (EC)**. Los equipos cliente en este entorno se encuentran en un dominio de servicio de directorio Active Directory® y sólo necesitan comunicarse con sistemas en los que se ejecuta Windows 2000 o versiones posteriores del sistema operativo Windows.

-   **Independiente.** Los equipos cliente en este entorno no son miembros de un dominio Active Directory y pueden necesitar comunicarse con sistemas en los que se ejecuta Windows NT® 4.0.

-   **Seguridad especializada: Funcionalidad limitada (SSLF)**. La preocupación por la seguridad en este entorno llega a tal punto que resulta aceptable una pérdida significativa de la funcionalidad y la capacidad de administración. Por ejemplo, los equipos del ejército y de las agencias de inteligencia funcionan en este tipo de entorno.

##### En esta página

[](#eeaa)[Destinatarios de la guía](#eeaa)
[](#edaa)[Esquema del contenido](#edaa)
[](#ecaa)[Recursos relacionados](#ecaa)
[](#ebaa)[Comuníquenos su opinión](#ebaa)
[](#eaaa)[Servicios de consultoría y soporte técnico](#eaaa)

### Destinatarios de la guía

Esta guía está destinada principalmente a consultores, expertos en seguridad, arquitectos de sistemas y profesionales de TI responsables de las fases de planeamiento del desarrollo de las aplicaciones o la infraestructura y la implementación de estaciones de trabajo Windows XP en un entorno de empresa. Esta guía no se ha diseñado para los usuarios domésticos.

Los expertos en seguridad y los arquitectos de TI pueden necesitar información más detallada acerca de las opciones de configuración de seguridad que se tratan en esta guía. Esta información se puede encontrar en la guía complementaria [Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP](http://go.microsoft.com/fwlink/?linkid=15159), en http://go.microsoft.com/fwlink/?LinkId=15159.

[](#mainsection)[Principio de la página](#mainsection)

### Esquema del contenido

Windows XP proporciona la versión más fiable de un sistema operativo cliente de Windows hasta la fecha, con características mejoradas en seguridad y privacidad. Se ha optimizado la seguridad global de Windows XP para garantizar a las organizaciones que puedan trabajar en un entorno informático mejor protegido y más seguro. La *Guía de seguridad de Windows XP* consta de siete capítulos. En los capítulos dos a seis se tratan los procedimientos necesarios para crear ese entorno. Cada uno de ellos describe un proceso completo diseñado para proteger los equipos que funcionan con Windows XP.

[![](images/Cc163061.default1(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163061.default1_big(es-es,technet.10).gif)

**Figura 1: Resumen de capítulos de la Guía de seguridad de Windows XP**

#### Capítulo 1: Introducción a la Guía de seguridad de Windows XP

Este capítulo reúne información general sobre la guía, que incluye descripciones de la audiencia de destino, problemas que se tratan y finalidad principal de la guía.

#### Capítulo 2: Configuración de la infraestructura de dominios de Active Directory

Se puede utilizar Directiva de grupo para administrar entornos de equipos y usuarios en dominios Windows Server 2003 y Windows 2000. Constituye una herramienta esencial para garantizar la seguridad de Windows XP, y se puede utilizar para aplicar y mantener una directiva de seguridad coherente en una red desde una ubicación central. En este capítulo se describen los pasos preliminares que se deben llevar a cabo en el dominio antes de aplicar Directiva de grupo a los equipos cliente Windows XP.

La configuración de Directiva de grupo se almacena en objetos de directiva de grupo (GPO) en controladores de dominio. Los GPO se vinculan a sitios, dominios y unidades organizativas dentro de la estructura de Active Directory. Dado que la directiva de grupo está tan estrechamente integrada con Active Directory, es importante tener un conocimiento básico de las implicaciones de seguridad y la estructura de Active Directory antes de implementarla.

#### Capítulo 3: Configuración de seguridad para clientes Windows XP

En este capítulo se describe la configuración de seguridad para equipos cliente Windows XP que se puede establecer a través de Directiva de grupo en un dominio Active Directory Windows 2000 o Windows Server 2003. No se proporciona información de todas las opciones de configuración disponibles; sólo de las que ayudarán a proteger un entorno de la mayoría de las amenazas actuales. La guía permite también a los usuarios seguir realizando funciones típicas de su trabajo en los equipos. Las opciones que configuren se deben basar en los objetivos de seguridad de la organización.

#### Capítulo 4: Plantillas administrativas para Windows XP

Este capítulo trata sobre las opciones de configuración que se pueden agregar a Windows XP mediante plantillas administrativas. Las plantillas administrativas son archivos Unicode que puede utilizar para configurar los valores basados en el Registro que determinan el comportamiento de un gran número de servicios, aplicaciones y componentes del sistema operativo. Hay numerosas plantillas administrativas que se pueden utilizar con Windows XP y que contienen centenares de parámetros de configuración.

#### Capítulo 5: Seguridad de clientes Windows XP independientes

Aunque la mayor parte de esta guía se centra en los entornos de Cliente de empresa (EC) y Seguridad especializada: Funcionalidad limitada (SSLF), en este capítulo se trata también la configuración de equipos cliente Windows XP independientes. Microsoft recomienda que Windows XP se implemente en una infraestructura de dominios de Active Directory, si bien reconoce que no es siempre posible. En este capítulo se proporciona orientación acerca de cómo aplicar las configuraciones recomendadas a equipos cliente Windows XP con SP2 que no sean miembros de un dominio Windows 2000 ni Windows Server 2003.

#### Capítulo 6: Directiva de restricción de software para clientes Windows XP

En este capítulo se proporciona información general básica de la directiva de restricción de software, que proporciona a los administradores un mecanismo controlado por directivas para identificar y limitar el software que se puede ejecutar en su dominio. Los administradores pueden utilizar una directiva de restricción de software para evitar que se ejecuten programas no deseados e impedir la propagación de virus, troyanos u otro tipo de código con fines malintencionados. Las directivas de restricción de software se integran completamente con Active Directory y Directiva de grupo. También pueden ser utilizadas en un entorno sin una infraestructura de dominios Windows Server 2003 cuando se aplican únicamente al equipo local.

#### Capítulo 7: Conclusión

En el capítulo final se revisan los puntos importantes de la guía en un breve resumen de la información presentada en los capítulos anteriores.

#### Apéndice A: Opciones clave que se deben considerar

Aunque en esta guía se tratan numerosas contramedidas y opciones de seguridad, debe tenerse presente que algunas son especialmente importantes. En este apéndice se describe la configuración que tendrá mayor repercusión en la seguridad de los equipos en los que se ejecuta Windows XP con SP2.

#### Apéndice B: Prueba de la Guía de seguridad de Windows XP

En este apéndice se explica cómo se probó la *Guía de seguridad de Windows XP* en un entorno de laboratorio para asegurar la respuesta esperada.

[](#mainsection)[Principio de la página](#mainsection)

### Recursos relacionados

Para obtener información adicional acerca de la configuración de seguridad recomendada en esta guía, descargue la guía complementaria, [Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP](http://go.microsoft.com/fwlink/?linkid=15159), en http://go.microsoft.com/fwlink/?LinkId=15159.

Lea [otras soluciones de seguridad](http://www.microsoft.com/technet/community/columns/sectip/st0805.mspx) del equipo de Microsoft Solutions for Security and Compliance (MSSC).

[](#mainsection)[Principio de la página](#mainsection)

### Comuníquenos su opinión

El equipo de Microsoft Solutions for Security and Compliance (MSSC) agradece sus ideas acerca de ésta y otras soluciones de seguridad.

¿Tiene algún comentario? Háganoslo saber en la [bitácora de soluciones de seguridad para el profesional de TI](http://blogs.technet.com/secguide).

O envíe sus comentarios por correo electrónico a la dirección siguiente: [SecWish@microsoft.com](mailto:secwish@microsoft.com?subject=guía%20de%20seguridad%20de%20windows%20xp). Respondemos con frecuencia a los comentarios que se envían a este buzón.

Nos interesa su opinión.

[](#mainsection)[Principio de la página](#mainsection)

### Servicios de consultoría y soporte técnico

Existen muchos servicios disponibles para ayudar a las organizaciones en sus esfuerzos por mejorar su seguridad. Utilice los siguientes vínculos para encontrar los servicios que necesita:

Para buscar servicios de consultoría y soporte técnico adecuados a las necesidades de su organización, visite [Microsoft Services](http://www.microsoft.com/services/microsoftservices/default.mspx) en http://support.microsoft.com/msservices.

##### Descargar

[![](images/Cc163061.icon_exe(es-es,TechNet.10).gif)Descargar la Guía de seguridad de Windows XP](http://go.microsoft.com/fwlink/?linkid=14840)

[](#mainsection)[Principio de la página](#mainsection)
