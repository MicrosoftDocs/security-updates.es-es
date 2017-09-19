---
TOCTitle: 'Capítulo 7: Conclusión'
Title: 'Capítulo 7: Conclusión'
ms:assetid: '8001f9fb-f330-4ab4-a134-ff756091ea0d'
ms:contentKeyID: 20200281
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163082(v=TechNet.10)'
---

Guía de seguridad de Windows XP
===============================

### Capítulo 7: Conclusión

Actualizado: 20-10-2005

Enhorabuena. Ahora que ha terminado esta guía, comprenderá mejor cómo evaluar los riesgos que pueden afectar a la seguridad de los equipos de su organización que ejecutan el sistema operativo Microsoft® Windows® XP Profesional con Service Pack 2 (SP2). Ya sabe cómo planear y diseñar la seguridad de los equipos cliente de la infraestructura en los que es posible hacerlo.

Esta guía incluye material de consultores e ingenieros de sistemas que han implementado soluciones basadas en Windows XP, Microsoft Windows Servidor™ 2003 y Windows 2000 en diversos tipos de configuraciones de organizaciones. Su objetivo es ofrecerle un conjunto actual de recomendaciones para trabajar con Windows XP. Además, la información recomendada en esta guía se puede aplicar a cualquier organización.

La seguridad es un tema muy importante, ya se utilice uno u otro tipo de entorno en la organización. Sin embargo, muchas organizaciones no asignan la importancia debida a la seguridad porque la ven erróneamente como algo que limitará la agilidad y la flexibilidad de las operaciones. Cuando un buen diseño de seguridad se convierte en un requisito empresarial clave y se planea desde el principio de cada uno de los proyectos de tecnología de la información (TI), una estrategia de seguridad implementada adecuadamente puede ser útil para mejorar la disponibilidad y el rendimiento de los sistemas informáticos. En cambio, si la estrategia de seguridad se agrega a un proyecto como un elemento complementario, la funcionalidad, estabilidad y flexibilidad de la administración se pueden ver afectadas negativamente. Por estos motivos, en esta guía se recomienda a las organizaciones considerar la seguridad como una de las máximas prioridades.

##### En esta página

[](#ecaa)[Seguridad del cliente](#ecaa)
[](#ebaa)[Directiva de restricción de software](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Seguridad del cliente

Windows XP Professional ofrece un completo conjunto de soluciones de seguridad para proteger los equipos de escritorio y portátiles de las amenazas. Aunque los usuarios de los equipos que no están unidos a un dominio disponen de menos opciones de seguridad, tanto unos como otros (unidos a un dominio o independientes) se benefician de un acceso seguro a sus equipos.

#### Clientes de empresa

Cuando un equipo cliente forma parte de la red de una organización, es posible que el administrador de la red lo configure con las características de seguridad de la directiva de grupo del servicio de directorio de Active Directory® que se describen en esta guía. Cualquier configuración de directiva de grupo aplicada por un administrador de red tiene prioridad sobre la configuración local que los usuarios establezcan en los equipos. La directiva de grupo permite a los administradores administrar los entornos que incluyen muchos tipos distintos de equipos cliente.

#### Clientes del entorno Seguridad especializada: Funcionalidad limitada (SSLF)

En el entorno Seguridad Especializada: Funcionalidad limitada (SSLF) que se describe en esta guía se hace énfasis en los problemas de acceso, servicios y entorno de la infraestructura. Además de unos controles elevados de la seguridad y de la autenticación de usuarios, los administradores disponen de un mayor control del acceso a los recursos y objetos de la red y las estaciones de trabajo cliente. Este control es necesario para que los administradores mantengan la seguridad de los datos y recursos, pero también limita inevitablemente las tareas que se pueden realizar en un equipo cliente del entorno SSLF. Sin embargo, esta capacidad limitada es necesaria, ya que hay un mayor número de requisitos de seguridad en este tipo de entornos.

#### Clientes independientes

Aunque hay menos parámetros de configuración de directiva de seguridad para los equipos cliente independientes que para los que pertenecen a un dominio de Active Directory, también hay disponibles características de seguridad clave para estos equipos. Una configuración adecuada de estos parámetros de configuración de directiva en los equipos independientes ayudará a reducir el riesgo de que se exploten vulnerabilidades. Un entorno independiente supone más carga administrativa, ya que estos equipos no se pueden administrar mediante la directiva de grupo basada en el dominio. Sin embargo, el uso de las herramientas que se describen en esta guía permitirán reducir la carga administrativa.

[](#mainsection)[Principio de la página](#mainsection)

### Directiva de restricción de software

La directiva de restricción de software proporciona a los administradores una forma de identificar el software que se ejecuta en los equipos cliente de un dominio o entorno independiente, además de controlar la capacidad de ejecución del software. Se puede utilizar para bloquear secuencias de comandos o código malintencionados e impedir la ejecución de aplicaciones no deseadas. La directiva de restricción de software se puede configurar para sistemas independientes o administrados a través de la directiva de grupo basada en el dominio con el fin de mejorar la integridad y capacidad de administración del sistema.

[](#mainsection)[Principio de la página](#mainsection)

### Resumen

En esta guía se ha explicado cómo evaluar, establecer prioridades y mitigar los riesgos de seguridad de una forma eficaz en tres entornos con equipos que ejecutan Windows XP con SP2. Se han proporcionado métodos documentados acerca de cómo planear y diseñar la seguridad de la infraestructura de red de una organización, además de una orientación detallada sobre cómo evaluar y mitigar vulnerabilidades específicas en los equipos de los tipos de entornos definidos en la guía.

Los motivos de las decisiones tomadas se han explicado en términos de las ventajas y los inconvenientes a los que se enfrenta una organización cuando decide implementar las distintas configuraciones de directiva para los tres entornos. La guía también incluye información detallada sobre cómo puede afectar una configuración de directiva específica a la funcionalidad, capacidad de administración, rendimiento y confiabilidad para que se puedan tomar decisiones informadas acerca de la configuración que se debe implementar en el propio entorno.

Es importante entender que la tarea de garantizar la seguridad de los equipos cliente de la red no es un proyecto puntual, sino continuo. Las organizaciones deben incluir tareas relacionadas con la seguridad y un planeamiento en sus presupuestos y programas. La implementación de las distintas configuraciones de directiva que se describen en esta guía mejorará la seguridad de la mayoría de las organizaciones que utilizan Windows XP Profesional. No obstante, cuando se detecte la siguiente vulnerabilidad grave, es posible que estos entornos vuelvan a ser susceptibles a los ataques. Por este motivo, es esencial supervisar una variedad de recursos con el fin de estar informado de los problemas de seguridad relacionados con los sistemas operativos, las aplicaciones y los dispositivos utilizados en el entorno.

Los miembros del equipo que han elaborado esta guía esperan que el material le resulte útil, informativo y fácil de entender.

#### Información adicional

Los siguientes vínculos proporcionan información adicional acerca de temas relacionados con la seguridad en Windows XP Professional.

-   Para ver vínculos a preguntas y respuestas habituales, instrucciones y las últimas descargas, entre otras cosas, visite el [Centro de ayuda y soporte técnico de Windows XP](http://support.microsoft.com/winxp) en http://support.microsoft.com/winxp.

-   Para obtener información acerca de cómo mantener la seguridad en Windows XP, visite el sitio de [seguridad de Trustworthy Computing](http://www.microsoft.com/security/default.mspx) en www.microsoft.com/security/default.mspx (en inglés).

-   Para obtener información acerca de [seguridad](http://www.microsoft.com/technet/security/default.mspx) en TechNet, visite www.microsoft.com/technet/security/default.mspx (en inglés).

-   Para obtener información acerca del planeamiento en Windows XP Professional, visite la página sobre [Windows XP Professional – Plan](http://www.microsoft.com/technet/prodtechnol/winxppro/plan/default.mspx) de TechNet en www.microsoft.com/technet/prodtechnol/winxppro/plan/default.mspx (en inglés).

-   Para ver [recursos de procedimientos de seguridad](http://www.microsoft.com/technet/itsolutions/howto/sechow.mspx) para Windows XP Professional, visite www.microsoft.com/technet/itsolutions/howto/sechow.mspx (en inglés).

-   Para obtener información de procedimientos acerca del [cifrado y descifrado de datos](http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/sag_seconceptsunencrypt.mspx) con el sistema de cifrado de archivos (EFS), visite www.microsoft.com/resources/documentation/windows/xp/all/proddocs/
    en-us/sag\_seconceptsunencrypt.mspx (en inglés).

#### Download

[![](images/Cc163082.icon_exe(es-es,TechNet.10).gif)Descargar la Guía de seguridad de Windows XP](http://go.microsoft.com/fwlink/?linkid=14840)

[](#mainsection)[Principio de la página](#mainsection)
