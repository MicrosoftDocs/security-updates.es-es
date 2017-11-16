---
TOCTitle: 'Guía de planeamiento de la implementación de servicios de cuarentena con red privada virtual (VPN) de Microsoft: Información general'
Title: 'Guía de planeamiento de la implementación de servicios de cuarentena con red privada virtual (VPN) de Microsoft: Información general'
ms:assetid: '40028620-c153-4851-bf15-d79d55d056bd'
ms:contentKeyID: 20200234
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc162926(v=TechNet.10)'
---

Guía de planeamiento de la implementación de servicios de cuarentena con red privada virtual (VPN) de Microsoft
===============================================================================================================

### Información general

Actualizado: mayo 24, 2005

La disponibilidad generalizada de Internet ha conducido a una serie de cambios significativos en el funcionamiento de las organizaciones. Para mantener su ventaja competitiva, cada vez es más necesario que los empleados de estas organizaciones se conecten a las redes empresariales desde ubicaciones remotas, como su casa, una sucursal, un hotel, un cibercafé o las instalaciones de un cliente. Estas conexiones remotas se suelen implementar mediante tecnologías de red privada virtual (VPN).

Las conexiones de VPN permiten que tanto empleados como socios se conecten a la red de área local (LAN) de una empresa a través de una red pública con total seguridad. El acceso remoto que utiliza tecnologías de VPN constituye un factor clave para obtener numerosas oportunidades empresariales, como la administración remota o aplicaciones de alta seguridad. Gran cantidad de grupos empresariales y usuarios utilizan aplicaciones de productividad y administración que exigen tener acceso remoto frecuente y fiable a las redes de área local empresariales.

Aunque una VPN ofrece acceso seguro gracias al cifrado de los datos a través del túnel de VPN, no evita las intrusiones por parte de software malintencionado, como virus o gusanos originados en el equipo remoto. Los ataques con virus o gusanos pueden provenir de los equipos infectados conectados a la LAN.

Para algunas organizaciones, como las del sector de los servicios financieros, es fundamental mantener una reputación de transacciones seguras. Por ello, la mínima intrusión en su seguridad puede deteriorar la percepción pública de una empresa. En consecuencia, las conexiones de las VPN deben someterse a férreas comprobaciones y validaciones de los requisitos de acceso.

El acceso a una VPN potencialmente no seguro tiene lugar cuando el equipo remoto no cumple los requisitos de seguridad de la organización. La mayor parte de las implementaciones de VPN no permiten comprobar si el equipo remoto dispone de las actualizaciones de seguridad o firmas de virus más recientes antes de conectarse a la red empresarial. Por lo tanto, muchas organizaciones no consideran que el acceso remoto basado en VPN cumpla con sus requisitos de seguridad.

Los servicios de cuarentena de VPN proporcionan un mecanismo para abordar estos problemas. Los servicios de cuarentena de VPN garantizan que los equipos que se conectan a la red mediante protocolos VPN se sometan a comprobaciones previas y posteriores a la conexión, y que queden aislados hasta que cumplan la directiva de seguridad exigida. Estas comprobaciones, que se llevan a cabo mediante secuencias de comandos personalizadas, pueden examinar las versiones de Service Pack, las actualizaciones de seguridad y si se está ejecutando un programa antivirus aprobado con los archivos de definición de virus más recientes. Asimismo, las organizaciones pueden comprobar otros requisitos con estas secuencias de comandos personalizadas.

La solución de servicios de cuarentena de VPN pone todos los equipos conectados que satisfacen la directiva de acceso remoto especificada en una red de cuarentena, y comprueba que cumplan la directiva de seguridad de la organización. El servidor de la VPN de acceso remoto sólo levanta las restricciones de la cuarentena y permite el acceso a los recursos de la empresa si el equipo de acceso remoto ha superado todas las comprobaciones.

En esta guía se describen los desafíos que plantea el planeamiento y la implementación de los servicios de cuarentena con VPN mediante las nuevas características disponibles en Microsoft® Windows Server™ 2003 con Service Pack 1 (SP1).

##### En esta página

[](#wort)[El desafío empresarial](#wort)
[](#klpp)[Las ventajas empresariales](#klpp)
[](#klph)[Destinatarios de la guía](#klph)
[](#kqph)[Requisitos previos del lector](#kqph)
[](#rqph)[Información general de la guía de planeamiento](#rqph)
[](#aaa)[Capítulo 1: Introducción](#aaa)
[Capítulo 2: Planteamientos para los servicios de cuarentena de red privada virtual](#aab)
[](#abc)[Capítulo 3: Problemas y requisitos](#abc)
[](#abd)[Capítulo 4: Diseño de la solución](#abd)
[](#add)[Apéndice A: Ejemplos de secuencias de comandos de servicios de cuarentena](#add)
[](#bbb)[Apéndice B: Parámetros del servicio de cuarentena de acceso remoto](#bbb)
[](#ddd)[Apéndice C: Vínculos relacionados](#ddd)
[](#ccc)[Agradecimientos](#ccc)

### El desafío empresarial

Las organizaciones se enfrentan a muchos desafíos cuando proporcionan acceso remoto a través de conexiones de VPN. Estos desafíos varían según los servicios prestados, el marco normativo en que opera la empresa y el entorno de seguridad. Los desafíos más frecuentes son:

-   Cómo definir una directiva eficaz de acceso a la VPN.

-   Cómo reducir la probabilidad de que equipos infectados o no conformes se conecten a la LAN empresarial.

-   Cómo cumplir los requisitos legales para el mantenimiento de la seguridad de los datos y de la información de carácter personal.

[](#mainsection)[Principio de la página](#mainsection)

### Las ventajas empresariales

Las organizaciones que implementan servicios de cuarentena de VPN eficaces pueden obtener gran cantidad de ventajas. Entre dichas ventajas se cuentan:

-   **Mejora del acceso seguro a los activos empresariales**. Los servicios de cuarentena de VPN mejoran la seguridad del acceso a la red gracias al cumplimiento estricto de los requisitos de actualización de los antivirus y la seguridad.

-   **Simplificación de la administración y el mantenimiento de los servicios**.** **Las organizaciones pueden estandarizar las tecnologías más novedosas y seguras para la implementación de su VPN. Pueden quitar de la infraestructura de la red las implementaciones de hardware de la VPN, como los sistemas de equipos de acceso remoto especializados, lo que permite simplificar las herramientas de mantenimiento, la documentación y los procesos de conexión. Esta simplificación mejora la asistencia técnica cotidiana para el funcionamiento de la solución de acceso a la VPN y compensa los costos de administración generados al implementar la solución de servicios de cuarentena.

-   **Mejora de la previsibilidad y facilidad de uso del acceso remoto**.** **La mayor fiabilidad y facilidad de uso anima a los usuarios a utilizar el servicio de VPN, con lo que se aumenta la confianza en la protección del trabajo importante y de los recursos críticos de la empresa.

-   **Reducción del costo total de propiedad (TCO)**. Al obligar a los equipos remotos a cumplir directivas informáticas confiables estrictas, se reducen los costos globales de administración y asistencia técnica. Este ahorro se deriva de la disminución de las llamadas de asistencia técnica y de la reducción del tiempo dedicado a solucionar los ataques de virus y gusanos.

-   **Mejora de la seguridad de la información crítica de la empresa**. La información de los clientes es de vital importancia para la mayor parte de las organizaciones, en particular para las que operan en un entorno normativo específico. Mantener esta información lo más segura posible ayuda a cumplir los requisitos normativos y conservar la reputación empresarial de la organización.

-   **Mejora de los procesos empresariales**. La implementación de una solución de servicios de cuarentena de VPN mejora la disponibilidad de las aplicaciones y los procesos de la empresa para los representantes comerciales ejecutivos, los directores de cuentas de clientes y los consultores. Esta mayor disponibilidad reduce el tiempo de toma de decisiones y mejora la flexibilidad a la hora de proporcionar productos y servicios.

Para obtener más información sobre estas ventajas, consulte el capítulo 2, "Planteamientos para los servicios de cuarentena de red privada virtual".

[](#mainsection)[Principio de la página](#mainsection)

### Destinatarios de la guía

Esta guía ofrece información de gran utilidad para las personas de una gran organización responsables de las cuestiones de máxima privacidad y para quienes trabajan en un entorno normativo estricto. También resultará útil a organizaciones de todos los tamaños que necesiten servicios de protección de identidad y control de acceso a los datos.

Entre las personas a quienes va dirigida esta guía se encuentran los responsables de tomar decisiones técnicas, diseñadores empresariales y administradores de seguridad de la empresa encargados de planear, implementar o manejar los vínculos de acceso remoto y la seguridad de la red. Los consultores que se encarguen de planear, implementar o manejar redes privadas virtuales basadas en Microsoft Windows® también encontrarán esta información de gran utilidad.

[](#mainsection)[Principio de la página](#mainsection)

### Requisitos previos del lector

En esta guía se supone que sus lectores cuentan con conocimientos funcionales de los conceptos y las tecnologías de la administración del acceso remoto. Para implementar las soluciones de esta guía, los lectores deberán comprender las siguientes áreas y tecnologías y estar familiarizados con ellas:

-   Acceso remoto con Windows Server 2003

-   Servicio de autenticación de Internet (IAS) u otras implementaciones de servicio de usuario de acceso telefónico de autenticación remota (RADIUS)

-   Connection Manager y Kit de administración de Connection Manager (CMAK)

-   Programas de secuencias de comandos o archivos por lotes

-   Servicios de Certificate Server e infraestructura de claves públicas (PKI)

En esta guía se describen los cuadrantes del modelo de procesos de operación y soporte en Microsoft Operations Framework (MOF). También se describen las funciones de administración de los servicios (SMF) de administración de seguridad y administración de incidentes en MOF. Para obtener más información sobre MOF, consulte el sitio Web de [Microsoft Operations Framework](http://www.microsoft.com/mof) en http://www.microsoft.com/mof.

[](#mainsection)[Principio de la página](#mainsection)

### Información general de la guía de planeamiento

Esta guía incluye los siguientes capítulos:

**Capítulo 1: Introducción**

En este capítulo se ofrece un resumen ejecutivo, se presentan los desafíos empresariales y las ventajas de implementar redes privadas virtuales con servicios de cuarentena, se sugieren los destinatarios recomendados del documento, se enumeran los requisitos del lector y se ofrece información general de los capítulos y casos de soluciones de esta guía.

**Capítulo 2: Planteamientos para los servicios de cuarentena de red privada virtual**

En este capítulo se describen los planteamientos para el acceso a los servicios de cuarentena de VPN. También se abordan los elementos esenciales del acceso a VPN para una solución dirigida a un caso con trabajadores remotos.

**Capítulo 3: Problemas y requisitos**

En este capítulo se presenta el caso de la entidad financiera Woodgrove National Bank. A continuación se definen los antecedentes, los problemas empresariales, los problemas técnicos y de seguridad y los requisitos de la solución para los casos de servicios de cuarentena de VPN para Woodgrove National Bank. En este capítulo también se explica el caso de la solución de acceso a VPN para trabajadores remotos, y se estudian los desafíos empresariales, técnicos y de seguridad de este caso.

**Capítulo 4: Diseño de la solución**

En este capítulo se describe con detalle cómo planear la solución del caso para acceso de trabajadores remotos a la red privada virtual. Se describe el concepto de la solución, así como sus requisitos, la arquitectura de la solución y cómo funciona. Por último, se explica cómo ampliar la solución.

Además de una descripción general del uso de redes privadas virtuales con servicios de cuarentena, en esta guía se ofrece orientación específica para implementar una solución de acceso remoto seguro, basada en el caso de la entidad financiera Woodgrove National Bank que se presenta en esta serie. Este caso muestra cómo implementar un acceso a VPN seguro para trabajadores remotos.

Microsoft creó el caso de la entidad financiera Woodgrove National Bank para ilustrar los desafíos típicos a los que se enfrentan las organizaciones para proporcionar los servicios de cuarentena en una red privada virtual, y mostrar cómo las tecnologías de Microsoft permiten abordar estos desafíos. Este caso explica cómo:

-   Implementar acceso remoto de alta seguridad para los representantes comerciales que casi nunca están en la oficina.

-   Proporcionar continuidad empresarial en caso de condiciones meteorológicas extremadamente adversas, para que los empleados puedan seguir trabajando desde casa.

-   Proporcionar condiciones laborales flexibles para que los empleados puedan trabajar desde casa si lo prefieren.

-   Distribuir puntualmente las actualizaciones de software a los equipos remotos.

#### Díganos su opinión

Microsoft valora su opinión acerca de este material. Agradeceríamos en especial cualquier comentario relacionado con las preguntas siguientes:

-   ¿En qué medida le ha parecido útil la información proporcionada?

-   ¿Ha sido precisa la descripción de los procedimientos paso a paso?

-   ¿Le resultaron los capítulos fáciles de leer e interesantes?

-   ¿Cómo calificaría esta solución en líneas generales?

O envíenos sus comentarios a la siguiente dirección de correo electrónico: [SecWish@microsoft.com](mailto:secwish@microsoft.com). Solemos responder con frecuencia a los comentarios que se envían a este buzón de correo.

Nos interesa su opinión.

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 1: Introducción

[](#ebaaq)[Resumen ejecutivo](#ebaaq)
[](#eaaar)[Información general de la guía de planeamiento](#eaaar)

### Resumen ejecutivo

La disponibilidad generalizada de Internet ha conducido a una serie de cambios significativos en el funcionamiento de las organizaciones. Para mantener su ventaja competitiva, cada vez es más necesario que los empleados de estas organizaciones se conecten a las redes empresariales desde ubicaciones remotas, como su casa, una sucursal, un hotel, un cibercafé o las instalaciones de un cliente. Estas conexiones remotas se suelen implementar mediante tecnologías de red privada virtual (VPN).

Las conexiones de VPN permiten que tanto empleados como socios se conecten a la red de área local (LAN) de una empresa a través de una red pública con total seguridad. El acceso remoto que utiliza tecnologías de VPN constituye un factor clave para obtener numerosas oportunidades empresariales, como la administración remota o aplicaciones de alta seguridad. Gran cantidad de grupos empresariales y usuarios utilizan aplicaciones de productividad y administración que exigen tener acceso remoto frecuente y fiable a las redes de área local empresariales.

Aunque una VPN ofrece acceso seguro gracias al cifrado de los datos a través del túnel de VPN, no evita las intrusiones por parte de software malintencionado, como virus o gusanos originados en el equipo remoto. Los ataques con virus o gusanos pueden provenir de los equipos infectados conectados a la LAN.

Para algunas organizaciones, como las del sector de los servicios financieros, es fundamental mantener una reputación de transacciones seguras. Por ello, la mínima intrusión en su seguridad puede deteriorar la percepción pública de una empresa. En consecuencia, las conexiones de las VPN deben someterse a férreas comprobaciones y validaciones de los requisitos de acceso.

El acceso a una VPN potencialmente no seguro tiene lugar cuando el equipo remoto no cumple los requisitos de seguridad de la organización. La mayor parte de las implementaciones de VPN no permiten comprobar si el equipo remoto dispone de las actualizaciones de seguridad o firmas de virus más recientes antes de conectarse a la red empresarial. Por lo tanto, muchas organizaciones no consideran que el acceso remoto básico basado en VPN cumpla con sus requisitos de seguridad.

Los servicios de cuarentena de VPN proporcionan un mecanismo para abordar estos problemas. Los servicios de cuarentena de VPN garantizan que los equipos que se conectan a la red mediante protocolos VPN se sometan a comprobaciones previas y posteriores a la conexión, y que queden aislados hasta que cumplan la directiva de seguridad exigida. Estas comprobaciones, que se llevan a cabo mediante secuencias de comandos personalizadas, pueden examinar las versiones de Service Pack, las actualizaciones de seguridad y si se está ejecutando un programa antivirus aprobado con los archivos de definición de virus más recientes. Asimismo, las organizaciones pueden comprobar otros requisitos con estas secuencias de comandos personalizadas.

La solución de servicios de cuarentena de VPN pone todos los equipos conectados que satisfacen la directiva de acceso remoto especificada en una red de cuarentena, y comprueba que cumplan la directiva de seguridad de la organización. El servidor de la VPN de acceso remoto sólo levanta las restricciones de la cuarentena y permite el acceso a los recursos de la empresa si el equipo de acceso remoto ha superado todas las comprobaciones.

En esta guía se describen los desafíos que plantea el planeamiento y la implementación de los servicios de cuarentena con VPN mediante las nuevas características disponibles en Microsoft® Windows Server™ 2003 con Service Pack 1 (SP1).

#### El desafío empresarial

Las organizaciones se enfrentan a muchos desafíos cuando proporcionan acceso remoto a través de conexiones de VPN. Estos desafíos varían según los servicios prestados, el marco normativo en que opera la empresa y el entorno de seguridad. Los desafíos más frecuentes son:

-   Cómo definir una directiva eficaz de acceso a la VPN.

-   Cómo reducir la probabilidad de que equipos infectados o no conformes se conecten a la LAN empresarial.

-   Cómo cumplir los requisitos legales para el mantenimiento de la seguridad de los datos y de la información de carácter personal.

#### Las ventajas empresariales

Las organizaciones que implementan servicios de cuarentena de VPN eficaces pueden obtener gran cantidad de ventajas. Entre dichas ventajas se cuentan:

-   **Mejora del acceso seguro a los activos empresariales**. Los servicios de cuarentena de VPN mejoran la seguridad del acceso a la red gracias al cumplimiento estricto de los requisitos de actualización de los antivirus y la seguridad.

-   **Simplificación de la administración y el mantenimiento de los servicios**.** **Las organizaciones pueden estandarizar las tecnologías más novedosas y seguras para la implementación de su VPN. Pueden quitar de la infraestructura de la red las implementaciones de hardware de la VPN, como los sistemas de equipos de acceso remoto especializados, lo que permite simplificar las herramientas de mantenimiento, la documentación y los procesos de conexión. Esta simplificación mejora la asistencia técnica cotidiana para el funcionamiento de la solución de acceso a la VPN y compensa los costos de administración generados al implementar la solución de servicios de cuarentena.

-   **Mejora de la previsibilidad y facilidad de uso del acceso remoto**.** **La mayor fiabilidad y facilidad de uso anima a los usuarios a utilizar el servicio de VPN, con lo que se aumenta la confianza en la protección del trabajo importante y de los recursos críticos de la empresa.

-   **Reducción del costo total de propiedad (TCO)**. Al obligar a los equipos remotos a cumplir directivas informáticas confiables estrictas, se reducen los costos globales de administración y asistencia técnica. Este ahorro se deriva de la disminución de las llamadas de asistencia técnica y de la reducción del tiempo dedicado a solucionar los ataques de virus y gusanos.

-   **Mejora de la seguridad de la información crítica de la empresa**. La información de los clientes es de vital importancia para la mayor parte de las organizaciones, en particular para las que operan en un entorno normativo específico. Mantener esta información lo más segura posible ayuda a cumplir los requisitos normativos y conservar la reputación empresarial de la organización.

-   **Mejora de los procesos empresariales**. La implementación de una solución de servicios de cuarentena de VPN mejora la disponibilidad de las aplicaciones y los procesos de la empresa para los representantes comerciales ejecutivos, los directores de cuentas de clientes y los consultores. Esta mayor disponibilidad reduce el tiempo de toma de decisiones y mejora la flexibilidad a la hora de proporcionar productos y servicios.

Para obtener más información sobre estas ventajas, consulte el capítulo 2, "Planteamientos para los servicios de cuarentena de red privada virtual".

#### Destinatarios de la guía

Esta guía ofrece información de gran utilidad para las personas de una gran organización responsables de las cuestiones de máxima privacidad y para quienes trabajan en un entorno normativo estricto. También resultará útil a organizaciones de todos los tamaños que necesiten servicios de protección de identidad y control de acceso a los datos.

Entre las personas a quienes va dirigida esta guía se encuentran los responsables de tomar decisiones técnicas, diseñadores empresariales y administradores de seguridad de la empresa encargados de planear, implementar o manejar los vínculos de acceso remoto y la seguridad de la red. Los consultores que se encarguen de planear, implementar o manejar redes privadas virtuales basadas en Microsoft Windows® también encontrarán esta información de gran utilidad.

#### Requisitos previos del lector

En esta guía se supone que sus lectores cuentan con conocimientos funcionales de los conceptos y las tecnologías de la administración del acceso remoto. Para implementar las soluciones de esta guía, los lectores deberán comprender las siguientes áreas y tecnologías y estar familiarizados con ellas:

-   Acceso remoto con Windows Server 2003

-   Servicio de autenticación de Internet (IAS) u otras implementaciones de servicio de usuario de acceso telefónico de autenticación remota (RADIUS)

-   Connection Manager y Kit de administración de Connection Manager (CMAK)

-   Programas de secuencias de comandos o archivos por lotes

-   Servicios de Certificate Server e infraestructura de claves públicas (PKI)

En esta guía se describen los cuadrantes del modelo de procesos de operación y soporte en Microsoft Operations Framework (MOF). También se describen las funciones de administración de los servicios (SMF) de administración de seguridad y administración de incidentes en MOF. Para obtener más información acerca de MOF, visite el sitio Web de [Microsoft Operations Framework](http://www.microsoft.com/mof) en http://www.microsoft.com/mof (en inglés).

[](#mainsection)[Principio de la página](#mainsection)

### Información general de la guía de planeamiento

Esta guía incluye los siguientes capítulos:

**Capítulo 1: Introducción**

En este capítulo se ofrece un resumen ejecutivo, se presentan los desafíos empresariales y las ventajas de implementar redes privadas virtuales con servicios de cuarentena, se sugieren los destinatarios recomendados del documento, se enumeran los requisitos del lector y se ofrece información general de los capítulos y casos de soluciones de esta guía.

**Capítulo 2: Planteamientos para los servicios de cuarentena de red privada virtual**

En este capítulo se describen los planteamientos para el acceso a los servicios de cuarentena de VPN. También se abordan los elementos esenciales del acceso a VPN para una solución dirigida a un caso con trabajadores remotos.

**Capítulo 3: Problemas y requisitos**

En este capítulo se presenta el caso de la entidad financiera Woodgrove National Bank. A continuación se definen los antecedentes, los problemas empresariales, los problemas técnicos y de seguridad y los requisitos de la solución para los casos de servicios de cuarentena de VPN para Woodgrove National Bank. En este capítulo también se explica el caso de la solución de acceso a VPN para trabajadores remotos, y se estudian los desafíos empresariales, técnicos y de seguridad de este caso.

**Capítulo 4: Diseño de la solución**

En este capítulo se describe con detalle cómo planear la solución del caso para acceso de trabajadores remotos a la red privada virtual. Se describe el concepto de la solución, así como sus requisitos, la arquitectura de la solución y cómo funciona. Por último, se explica cómo ampliar la solución.

Además de una descripción general del uso de redes privadas virtuales con servicios de cuarentena, en esta guía se ofrece orientación específica para implementar una solución de acceso remoto seguro, basada en el caso de la entidad financiera Woodgrove National Bank que se presenta en esta serie. Este caso muestra cómo implementar un acceso a VPN seguro para trabajadores remotos.

Microsoft creó el caso de la entidad financiera Woodgrove National Bank para ilustrar los desafíos típicos a los que se enfrentan las organizaciones para proporcionar los servicios de cuarentena en una red privada virtual, y mostrar cómo las tecnologías de Microsoft permiten abordar estos desafíos. Este caso explica cómo:

-   Implementar acceso remoto de alta seguridad para los representantes comerciales que casi nunca están en la oficina.

-   Proporcionar continuidad empresarial en caso de condiciones meteorológicas extremadamente adversas, para que los empleados puedan seguir trabajando desde casa.

-   Proporcionar condiciones laborales flexibles para que los empleados puedan trabajar desde casa si lo prefieren.

-   Distribuir puntualmente las actualizaciones de software a los equipos remotos.

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 2: Planteamientos para los servicios de cuarentena de red privada virtual

[](#keaa)[Introducción](#keaa)
[](#ldaa)[Información general sobre servicios de cuarentena de red privada virtual](#ldaa)
[](#jcaa)[Componentes del cliente](#jcaa)
[](#elaa)[Componentes de servidor](#elaa)
[](#kaaa)[Requisitos de red](#kaaa)

### Introducción

Las conexiones de acceso remoto de red privada virtual (VPN) son una tecnología cada vez más madura. Sin embargo, proporcionar servicios de cuarentena para conexiones a VPN es un concepto más reciente. En este capítulo se presentan los elementos siguientes que ofrecen servicios de cuarentena de VPN:

-   Componentes basados en el cliente

-   Componentes basados en el servidor

-   Componentes de la red

**Nota:** Microsoft® Windows Server™ 2003 con Service Pack 1 (SP1) proporciona una implementación de servicios de cuarentena de VPN compatible. Aunque Servidor ISA (Internet Security and Acceleration) de Microsoft 2004 también proporciona control de cuarentena de VPN, Servicios de soporte al cliente de Microsoft no presta soporte pleno para esta implementación de control de cuarentena de VPN en este momento.

[](#mainsection)[Principio de la página](#mainsection)

### Información general sobre servicios de cuarentena de red privada virtual

Las tecnologías de red privada virtual (VPN) permiten a los usuarios tener acceso a una red privada mediante una conexión segura y autenticada que se ejecuta por encima de los servicios de la red pública, como Internet. Estas conexiones utilizan un protocolo de túnel que sella digitalmente (cifra) cada paquete antes de enrutarlo por la red pública. Los detalles de este proceso varían según el mecanismo de VPN utilizado. La red de destino recibe los paquetes y los descifra. En apariencia el equipo cliente parece tener sencillamente una conexión directa con la red privada virtual.

El servicio de cuarentena de VPN funciona retrasando la conectividad plena con la red privada virtual mientras examina y valida la configuración del equipo que pretende obtener acceso remotamente con respecto a los estándares de la organización. Si el equipo que se conecta no cumple la directiva de la organización, el proceso del servicio de cuarentena puede instalar Service Packs, actualizaciones de seguridad y definiciones de virus antes de permitir al equipo conectarse a los demás recursos de la red. Debido a que el servicio de cuarentena de VPN se basa en las comprobaciones efectuadas por el cliente, un usuario malintencionado podría eludirlas. El servicio de cuarentena de VPN no está diseñado para proteger la red contra un atacante en particular, sino para ayudar a evitar el acceso por parte de un usuario autorizado cuyo equipo, por error, no cumpla los requisitos de configuración de los equipos de la organización.

**Nota:** el servicio de cuarentena de VPN no garantiza una solución de seguridad total, pero sí ayuda a evitar que los equipos con configuraciones no seguras se conecten a la red privada virtual. Sin embargo, el servicio de cuarentena de VPN no protege la red privada virtual contra usuarios malintencionados que hayan obtenido unas credenciales válidas y se registren utilizando equipos que cumplan la directiva de seguridad informática de la organización. Los servicios de cuarentena de VPN tampoco protegen contra usuarios no autorizados que se conecten con equipos que cumplan los requisitos de seguridad y, a continuación, decidan lanzar un ataque malintencionado.

Para la implementación del servicio de cuarentena de VPN se necesitan los componentes siguientes:

-   Clientes de acceso remoto compatibles con el servicio de cuarentena

-   Servidor de acceso remoto compatible con el servicio de cuarentena

-   Servidor de servicio de usuario de acceso telefónico de autenticación remota (RADIUS) compatible con el servicio de cuarentena (opcional)

-   Recursos del servicio de cuarentena

-   Base de datos de cuentas

-   Directiva de acceso remoto del servicio de cuarentena

En esta sección se facilita información general sobre cómo funcionan entre sí estos componentes para proporcionar la solución de cuarentena de VPN

**Nota:  **una solución de cuarentena de VPN puede utilizar la autenticación mediante RADIUS o Windows, aunque es preferible el método RADIUS. La sección sobre implementación del servicio de autenticación de Internet (IAS), que figura más adelante en este capítulo, proporciona más información sobre IAS, que es la implementación de Microsoft de RADIUS.

#### Conexión mediante una red privada virtual

Cuando un equipo inicia una conexión de VPN a un servidor de acceso remoto basado en Microsoft Windows®, el servidor lleva a cabo las acciones siguientes:

1.  El servidor de acceso remoto permite la conexión y lleva a cabo comprobaciones con respecto a las directivas de acceso remoto configuradas.

2.  El servidor de acceso remoto comprueba que el usuario tenga derecho a conectarse de manera remota.

3.  El servidor de acceso remoto autentica las credenciales del usuario con respecto al servicio de directorio o el servicio de autenticación.

4.  El equipo de acceso remoto asigna una dirección IP al equipo remoto.

En las implementaciones de VPN estándar, el usuario tiene acceso a todos los recurso de red autorizados una vez se han realizado con éxito estos cuatro pasos. El equipo no comprueba en ningún momento si existen actualizaciones de seguridad, protección antivirus, ni otras características semejantes.

#### Conexión mediante un servicio de cuarentena de red privada virtual

En la figura siguiente se resume un planteamiento del servicio de cuarentena de VPN que utiliza los servidores de recursos situados en una subred de cuarentena.

[![](images/Cc162926.PGFG0201(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc162926.pgfg0201_big(es-es,technet.10).gif)

**Figura 2.1 Ruta del proceso del servicio de cuarentena de VPN**

El servicio de cuarentena de VPN implementa un proceso modificado cuando el usuario intenta conectarse a la red remota. El proceso incluye los pasos siguientes:

1.  El equipo realiza una comprobación antes de conectar para asegurarse de que el equipo cumpla determinados requisitos básicos. Entre ellos pueden incluirse revisiones, actualizaciones de seguridad o firmas de virus. La secuencia de comandos de antes de conectar almacena localmente los resultados de esta comprobación. Una organización también puede ejecutar comprobaciones de seguridad posteriores a la conexión si se desea.

2.  Una vez superadas las comprobaciones de antes de conectar, el equipo se conecta al servidor de acceso remoto mediante la VPN.

3.  El servidor de acceso remoto autentica las credenciales del usuario con el servidor RADIUS con respecto al nombre de usuario y la contraseña almacenados en el servicio de directorio Active Directory®. RADIUS es un componente opcional en este proceso.

4.  Si Active Directory autentica al usuario, el servidor de acceso remoto pone al cliente en cuarentena aplicando la directiva de acceso remoto del servicio de cuarentena de VPN. El acceso del equipo cliente de acceso remoto está limitado a los recursos del servicio de cuarentena especificados por la directiva de acceso remoto. El servicio de cuarentena se puede aplicar de dos maneras en el equipo cliente de acceso remoto: mediante un período de espera específico, para que el equipo cliente no quede en cuarentena indefinidamente, o mediante un filtro IP que limite el tráfico IP exclusivamente a los recursos de red especificados.

5.  La secuencia de comandos de después de conectar notifica al servidor de acceso remoto que el cliente cumple los requisitos especificados. Si la conexión no cumple los requisitos en el período de espera especificado, la secuencia de comandos se lo notifica al usuario y anula la conexión.

6.  El servidor de acceso remoto quita el equipo cliente del modo de cuarentena quitando el filtro IP y concede el acceso apropiado a los recursos de la red especificados por la directiva de acceso remoto.

**Nota:** si la conexión no se realiza correctamente, el usuario recibe un mensaje que describe el motivo del error.

En el modo de cuarentena, el cliente únicamente tiene acceso a los recursos situados en la red de cuarentena. Esta red puede estar compuesta por una subred de cuarentena independiente o por un conjunto definido de servidores con acceso a Internet. La red de cuarentena proporciona recursos para permitir que el equipo remoto cumpla plenamente los requisitos de seguridad prescritos. Estos recursos suelen incluir un servidor DNS para la resolución de nombres, un servidor Web para publicar instrucciones del usuario y un servidor de archivos desde el que descargar las actualizaciones necesarias, los Service Packs o las los programas antivirus. El servidor de acceso remoto implementa un filtro IP personalizado que restringe al cliente para que sólo tenga acceso a los recursos de cuarentena específicos. El filtro IP personalizado sólo permite la comunicación a través de puertos limitados con equipos con nombre pertenecientes a una subred independiente.

Para utilizar una subred de cuarentena se necesita un tiempo de espera de sesión prolongado, a fin de garantizar que el equipo cliente pueda descargar todas las actualizaciones necesarias si los recursos se encuentran en la subred de cuarentena. El uso de servidores de actualización con conexión a Internet a fin de realizar la actualización antes de efectuar la conexión a la VPN tiene la ventaja de que permite aplicar un tiempo de espera de cuarentena breve. En ambos casos, la secuencia de comandos es la que efectúa las actualizaciones en el cliente, no la propia red de cuarentena.

La directiva de acceso del servicio de cuarentena de VPN especifica el valor configurable del tiempo de espera. El servidor de acceso remoto termina la conexión si el cliente no supera la prueba de conformidad de la red dentro del plazo establecido. Para obtener más información sobre la configuración del servicio de cuarentena de VPN, consulte el capítulo 4, "Diseño de la solución".

Cuando se implementa un servicio de cuarentena de VPN, es importante asegurarse de que todos los componentes de la solución interactúen correctamente. En la próxima sección se estudian estos componentes y se explican brevemente los problemas de planeamiento de cada uno de ellos.

[](#mainsection)[Principio de la página](#mainsection)

### Componentes del cliente

Debido a que el servicio de cuarentena de VPN se basa en los componentes que se ejecutan en el cliente remoto, es importante comprender la función y configuración de los mismos. Connection Manager y el Kit de administración de Connection Manager (CMAK) revisten especial importancia.

#### Información general de Connection Manager

Connection Manager centraliza y automatiza el establecimiento y la administración de conexiones de red. Connection Manager presta soporte para varios aspectos clave de la configuración del servicio de cuarentena de VPN:

-   Comprobaciones de seguridad antes de conectar para administrar automáticamente las configuraciones de equipos cliente.

-   Comprobaciones después de conectar y validaciones de inicio de sesión.

El equipo administrativo instala el software de marcador cliente de Connection Manager en cada cliente de acceso remoto. Este software puede incluir características más avanzadas que las que proporciona una conexión de acceso remoto configurada manualmente.

#### Simplificación del proceso de conexión

Connection Manager también simplifica el proceso de conexión para el usuario. Limita el número de opciones de configuración que puede modificar el usuario, lo que contribuye a garantizar que éste pueda conectarse sin problemas. En los ejemplos siguientes se muestran aspectos para los que cada organización puede personalizar las entradas de Connection Manager:

-   Los usuarios pueden seleccionar los números de teléfono en una lista según su ubicación física.

-   Los usuarios ven gráficos, iconos, mensajes y Ayuda personalizados.

-   Connection Manager puede crear una conexión de acceso telefónico a Internet antes de efectuar la conexión a la VPN.

-   Connection Manager puede ejecutar acciones personalizadas durante el proceso de conexión, como acciones antes y después de la conexión. Ejemplos de ello son restablecer el perfil del marcador o configurar el servidor de seguridad Windows Firewall para que pase por alto las excepciones a las reglas de filtrado de paquetes.

Para implementar una solución administrable, los administradores tienen que poder crear e implementar configuraciones de Connection Manager en varios equipos; para ello, deben crear perfiles de Connection Manager.

#### Creación de un perfil de Connection Manager

Los perfiles de Connection Manager son paquetes de marcador de cliente de Connection Manager en forma de archivos ejecutables autoextraíbles. Los administradores de redes pueden utilizar un CMAK para crearlos. Las organizaciones pueden utilizar la directiva de grupo de Active Directory u otros mecanismos de instalación de software, como un servidor Web con conexión a Internet o la distribución de software de Microsoft Systems Management Server 2003, para implementar los perfiles de Connection Manager resultantes en los equipos cliente.

Cuando el usuario ejecuta el archivo ejecutable, éste instala el perfil en el equipo local junto con la configuración correcta para conectarse a los servidores de acceso remoto. Un usuario sólo tiene que iniciar el nombre del perfil en el menú **Conectar con** de Windows XP; el perfil establecerá automáticamente las conexiones apropiadas de acceso telefónico y de VPN.

#### Personalización de un perfil de Connection Manager

El diseño flexible de Connection Manager permite a los administradores de TI escribir e insertar módulos correspondientes a requisitos de administración o de seguridad específicos. El asistente del Kit de administración de Connection Manager le guiará por gran variedad de opciones al configurar un perfil de Connection Manager. Para obtener más información sobre el Kit de administración de Connection Manager, consulte el tema [Connection Manager Administration Kit](http://www.microsoft.com/resources/documentation/windowsserv/2003/standard/proddocs/en-us/sag_cmaktopnode.asp) (en inglés) en http://www.microsoft.com/resources/documentation/WindowsServ/2003/standard/proddocs/en-us/sag\_CMAKtopnode.asp.

##### Implementación de acciones personalizadas en Connection Manager

Puede utilizar el asistente del CMAK para incluir acciones personalizadas en los perfiles de Connection Manager a fin de iniciar programas automáticamente cuando los usuarios se conectan a la red. El asistente del CMAK permite especificar acciones personalizadas para su ejecución en cinco puntos distintos a lo largo del proceso de conexión:

-   **Acciones antes de inicializar (previas a la inicialización)**. Tan pronto como los usuarios inician Connection Manager, se ejecutan las acciones previas a la inicialización especificadas. Estas acciones se ejecutan antes de que aparezca la pantalla de inicio de sesión de Connection Manager. Tenga en cuenta que las acciones de antes de conectar de Connection Manager se ejecutan cuando se hace clic en el cuadro de diálogo **Propiedades** o en el perfil de servicio.

-   **Acciones antes de la conexión**. Cuando el usuario hace clic en **Conectar**, Connection Manager ejecuta las acciones de antes de conectar especificadas en el perfil del servicio. Las acciones previas a la conexión se ejecutan antes de que Connection Manager establezca una conexión con el servicio de acceso remoto. Para las acciones relacionadas específicamente con túneles, Connection Manager utiliza acciones antes del túnel.

-   **Acciones antes del túnel (para VPN)**. Connection Manager ejecuta las acciones antes del túnel una vez que ha establecido una conexión con el proveedor de servicios de Internet, pero antes de establecer el túnel con el servidor VPN. Este tipo de acción únicamente está disponible si la VPN forma parte de un perfil de servicio de Connection Manager.

-   **Acciones después de la conexión**. Connection Manager ejecuta las acciones después de la conexión una vez que ha establecido el túnel. Cada acción posterior a la conexión especificada en el asistente del CMAK se puede configurar de modo que se ejecute cada vez que el usuario se conecte al servicio de acceso remoto.

-   **Acciones de desconexión.** Connection Manager ejecuta las acciones de desconexión inmediatamente antes de desconectarse del servicio. Puede utilizar las acciones de desconexión para la administración rutinaria, por ejemplo, recopilar datos sobre el total de minutos transcurridos en línea. El usuario puede ver esta información. El equipo de operaciones también puede utilizar estos datos para analizar la experiencia del usuario.

    **Nota:** las acciones de desconexión se ejecutan aunque Connection Manager no sea la causa de la misma. Por ejemplo, si un problema del servicio telefónico termina la conexión del usuario, Connection Manager intenta ejecutar las acciones de desconexión especificadas en el perfil del servicio después de la desconexión inesperada.

Una acción de antes del túnel típica sería ejecutar una secuencia de comandos de requisitos de la directiva de red para comprobar si el equipo cliente cumple con los mismos. Para obtener descripciones de una secuencia de comandos de requisitos de la directiva de red, consulte el apéndice A, "Ejemplos de secuencias de comandos para servicios de cuarentena", en este mismo documento.

#### Agente de cuarentena de acceso remoto

El servicio de cuarentena de VPN necesita en este momento un agente de cliente que trabaje con el componente de escucha apropiado que se ejecuta en el servidor de acceso remoto. El agente de cliente informa al componente de servidor de que el cliente ha superado las comprobaciones necesarias, para que el servidor de acceso remoto permita el acceso a los recursos de la intranet.

Windows Server 2003 con SP1 proporciona un agente de cliente (RQC.exe) que se comunica con el servicio de cuarentena de acceso remoto (RQS.exe) mediante el puerto 7250 del Protocolo de control de transmisión (TCP). En el punto de la conexión con cuarentena, el componente de escucha (RQS) envía al cliente (RQC) una clave compartida secreta. Si el cliente satisface las condiciones necesarias, el cliente envía al servidor la clave compartida, para que el servidor de acceso remoto levante la cuarentena. El agente de cuarentena de acceso remoto se instala como parte del Kit de administración de Connection Manager.

[](#mainsection)[Principio de la página](#mainsection)

### Componentes de servidor

El componente fundamental del servicio de cuarentena de VPN es el servidor de acceso remoto de VPN, que desempeña las funciones siguientes:

-   Ejecuta el servicio de cuarentena de acceso remoto

-   Aplica la directiva de acceso remoto para el acceso en cuarentena

-   Negocia las comunicaciones con el agente de cliente

-   Recibe la notificación de conformidad con la directiva enviada por el agente de cliente

-   Aplica la directiva de acceso remoto para el acceso sin restricciones

El servicio de cuarentena de acceso remoto de Windows Server 2003 con SP1 admite las interfaces de programación de aplicaciones (API) necesarias para poner el equipo remoto en cuarentena y, posteriormente, levantar las restricciones de la cuarentena del equipo una vez el agente de cliente notifica su conformidad.

El servicio de cuarentena de acceso remoto es un componente opcional de Windows Server 2003 con SP1. El servicio de cuarentena de acceso remoto consiste en un archivo ejecutable (RQS.exe) que escucha en el puerto TCP 7250 para recibir la notificación del agente de cliente. El componente de servicio de cuarentena de acceso remoto de Windows 2003 Server con SP1 es la única versión del servicio de cuarentena soportado por los Servicios de soporte al cliente de Microsoft.

**Nota:** los servidores de seguridad que existan entre el servidor de acceso remoto y el cliente deben permitir el tráfico por el puerto 7250. El servidor de acceso remoto necesita que se permita el tráfico entrante para el puerto TCP 7250.

Las restricciones de la cuarentena que se aplican a las conexiones de VPN individuales consisten en:

-   Filtros de paquetes de cuarentena que restringen el tráfico que el cliente de acceso remoto en cuarentena puede enviar o recibir.

-   Un temporizador de la sesión de cuarentena que limita el tiempo que el cliente puede permanecer conectado en modo de cuarentena antes de su desconexión forzosa.

[](#mainsection)[Principio de la página](#mainsection)

### Requisitos de red

Los componentes de red necesarios para una solución de cuarentena de VPN incluyen:

-   Servidores IAS (Servicios de autenticación de Internet)

-   Servidores SUS (Software Update Services) (componente opcional)

-   Windows Update (componente opcional)

-   Componentes de red adicionales

La red también debe proporcionar el ancho de banda necesario para la solución. Además, la red debe proporcionar las rutas y las puertas de enlace necesarias para la transmisión eficaz de los paquetes.

#### Implementación del servicio de autenticación de Internet (IAS)

RADIUS ofrece mayor flexibilidad para autenticar a los usuarios mediante conexiones de VPN, como la compatibilidad con los estándares del Protocolo de autenticación extensible (EAP). EAP permite controles de autenticación por dos factores con certificados digitales o tarjetas inteligentes.  

Las organizaciones únicamente necesitan los servidores IAS en caso de que deseen configurar el servidor de acceso remoto para utilizar RADIUS como proveedor de autenticación. El uso de IAS para la autenticación RADIUS en un caso de servicios de cuarentena de VPN ofrece numerosas ventajas. El uso de IAS:

-   Permite la autorización y autenticación centralizada de usuarios.

-   Se integra con Active Directory.

-   Ofrece una amplia gama de opciones de autorización y autenticación.

El servidor IAS administra el proceso de autenticación, que entrega a Active Directory la solicitud de autenticación y la información de inicio de sesión del usuario. A continuación, Active Directory compara la información de inicio de sesión con las credenciales de ese usuario remoto. Si las credenciales coinciden, IAS autentica al usuario. Para obtener más información sobre IAS, consulte [Internet Authentication Service](http://www.microsoft.com/windowsserver2003/technologies/ias/default.mspx) (en inglés) en el sitio Web www.microsoft.com/windowsserver2003/technologies/ias/default.mspx.

**Nota:** sólo IAS en Windows Server 2003 admite la configuración de los atributos avanzados para los perfiles de las directivas de acceso remoto que se necesitan para configurar el servicio de cuarentena de VPN. Otras implementaciones de RADIUS podrían no ser compatibles con esta característica. Para obtener más información al respecto, consulte el capítulo 4 "Diseño de la solución".

IAS es el único servidor RADIUS que admite los dos atributos específicos del proveedor que requiere el servicio de cuarentena de VPN: MS-Quarantine-Session-Timeout y MS-Quarantine-IPFilter. Para obtener más información sobre la importancia de ambos atributos, consulte el capítulo 4 "Diseño de la solución".

#### Uso de Software Update Services

Antes de poder conectar los equipos remotos a los recursos de la intranet, es preciso asegurarse de que estos equipos tengan instalados los Service Packs y las actualizaciones de seguridad más recientes. SUS proporciona una base de datos centralizada de actualizaciones de software que permiten actualizar los equipos remotos. Los equipos cliente de acceso remoto comprueban las actualizaciones mediante una acción personalizada del perfil de Connection Manager.

SUS únicamente es adecuado para actualizar clientes una vez que éstos se conectan a la red empresarial. Debido a que SUS utiliza el ancho de banda inactivo, puede tardar demasiado en actualizar los equipos de acceso remoto.

#### Uso de Windows Update

Windows Update es un sitio Web de Internet que aloja las actualizaciones de seguridad y las revisiones disponibles públicamente para los sistemas operativos de Microsoft. Los equipos remotos pueden utilizar Windows Update para descargar las actualizaciones antes de conectarse a la red empresarial. Como alternativa, el servicio de actualizaciones automáticas de Windows XP puede comprobar regularmente el sitio Web de Windows Update e instalar de manera automática las actualizaciones de seguridad. Windows Update es independiente de Active Directory.

Una secuencia de comandos antes de la conexión puede comprobar si el equipo no cumple alguno de los requisitos de la red empresarial. La secuencia de comandos puede, entonces, ejecutar Microsoft Internet Explorer y dirigir al usuario al sitio Web de Windows Update. Para obtener más información sobre Windows Update, consulte el sitio Web de [Windows Update](http://windowsupdate.microsoft.com/) en http://windowsupdate.microsoft.com.

#### Implementación de componentes de red adicionales

El servicio de cuarentena de VPN puede necesitar los siguientes componentes de red adicionales:

-   **Servidores del Protocolo de configuración dinámica de servidores (DHCP).** DHCP proporciona asignación automática de direcciones IP para clientes remotos. (Recomendado)

-   **Active Directory**.** **Active Directory proporciona un método de autenticar las cuentas de los usuarios. Active Directory se integra con IAS y admite otras utilidades de seguridad, como la autenticación mediante tarjeta inteligente. (Recomendado)

-   **Servidores del sistema de nombres de dominio(DNS)**. DNS proporciona servicios de resolución de nombres para que los equipos cliente de la red de cuarentena puedan conectarse a los servidores SUS, servidores Web y servidores de archivos que contienen los archivos antivirus y otras actualizaciones. (Recomendado)

-   **Servidores de archivos.** Contienen las actualizaciones del software antivirus e instalaciones completas del mismo. Los servidores de archivos sólo se necesitan si se van a actualizar los equipos de acceso remoto mientras están en cuarentena. (Opcional)

-   **Servidores Web**. Proporcionan instrucciones a los usuarios finales sobre el proceso que deben seguir para levantar la cuarentena de sus equipos, así como vínculos para comprobar si el proceso se ha completado. También puede usar un servidor Web para distribuir actualizaciones antes de realizar la conexión a la VPN. (Opcional)

Para obtener más información sobre cómo planear la implementación de estos componentes, consulte el capítulo 4, "Diseño de la solución".

En este capítulo hemos estudiado los componentes que pueden proporcionar el servicio de cuarentena de VPN, que incluye las características específicas de Windows Server 2003 con SP1. En el capítulo 3, "Problemas y requisitos", se describen los problemas y las limitaciones concretos a los que debe hacer frente Woodgrove National Bank al implementar esta tecnología.

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 3: Problemas y requisitos

[](#edla)[Introducción](#edla)
[](#ecma)[El caso de la entidad financiera Woodgrove National Bank](#ecma)
[](#ezaa)[Implementación del acceso a la VPN para trabajadores remotos](#ezaa)
[](#exaa)[Uso de Microsoft Operations Framework (MOF)](#exaa)

### Introducción

Para utilizar los servicios de cuarentena de red privada virtual (VPN) para ayudar a proteger el acceso remoto es preciso que la organización implemente varias tecnologías que deben integrarse sin fisuras y funcionar de manera confiable como una sola unidad. Para lograr el éxito, la organización debe comprender con claridad las cuestiones y los requisitos subyacentes de cada tecnología, así como la manera en que todas ellas interactúan entre sí.

En este capítulo se analiza el caso de la solución para la entidad financiera Woodgrove National Bank, y los problemas relacionados con ella. En el capítulo 4, "Diseño de la solución" se incorpora todo ello a una solución aceptable para esos requisitos.

[](#mainsection)[Principio de la página](#mainsection)

### El caso de la entidad financiera Woodgrove National Bank

Woodgrove National Bank es un banco ficticio de inversiones de ámbito global, líder en su sector, que en su papel como intermediario financiero tiene clientes institucionales, corporativos, gubernamentales y particulares. Sus actividades incluyen: emisión de seguros, venta, comercio, servicios de asesoramiento financiero, investigación relacionada con la inversión, capital de riesgo y servicios de correduría para instituciones financieras.

Woodgrove National Bank es una filial propiedad al 100% de WG Holding Company. WG Holding Company es una empresa líder mundial en servicios financieros con sede en Londres, Inglaterra. WG posee cinco empresas: Woodgrove National Bank, NorthWind Trading, Contoso, Ltd., Litware Financials y Humongous Insurance. Todas ellas son grandes empresas, cada a de las cuales cuenta con más de 5.000 usuarios.

#### Perfil geográfico

Woodgrove National Bank tiene más de 15.000 empleados en más de 60 oficinas distribuidas por todo el mundo. Tiene sedes corporativas (centros de concentración) con un gran número de empleados en Nueva York (5.000 empleados), Londres (5.200 empleados) y Tokio (500 empleados). Cada centro de concentración da soporte a varias oficinas.

Para cada región a la que presta servicio la sede corporativa, existen varios sitios secundarios (por ejemplo, Boston y Atlanta en Norteamérica). Además de los centros de concentración, existen otras dos sedes corporativas principales, Sydney y Johannesburgo, ambas con sus propios servidores dedicados de archivos, impresión y aplicaciones.

#### Perfil de la organización de TI

Aunque Woodgrove National Bank tiene un entorno de servidor mixto que utiliza Microsoft® Windows® y UNIX, su infraestructura se ejecuta sobre una red troncal basada en Windows Server. La mayoría de servidores se encuentran ubicados en las tres sedes corporativas en Nueva York, Londres y Tokio. En la siguiente ilustración se muestra el diseño de las sedes corporativas y los vínculos existentes entre ellas.

[![](images/Cc162926.PGFG0302(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc162926.pgfg0302_big(es-es,technet.10).gif)

**Figura 3.1 Entorno de red de Woodgrove National Bank.**

Woodgrove National Bank utiliza en la actualidad varios productos y tecnologías de Microsoft para servicios de intranet y extranet. Woodgrove National Bank usa una infraestructura de servicios de directorio basada en Windows 2000 Active Directory® y está actualizando todos los controladores de dominio a Microsoft Windows Server™ 2003. Woodgrove no tiene equipos cliente heredados; todos los equipos de sobremesa y portátiles ejecutan los sistemas operativos Windows 2000 Professional con Service Pack 4 (SP4) o posterior, o bien Windows XP Professional con SP2 o posterior. El departamento de TI de Woodgrove National Bank tiene mucha experiencia con Windows Server 2003.

#### Integración de los requisitos normativos

Woodgrove National Bank debe ajustarse a los requisitos de la normativa financiera vigente en cada país o región en que opera. También debe cumplir con las leyes de protección de datos y demostrar eficacia en la seguridad de las operaciones.

#### Prestación de un acceso seguro a los trabajadores remotos

Woodgrove National Bank proporciona acceso remoto a su red corporativa al personal de ventas, ejecutivo y de soporte técnico de TI. Para la solución actual de acceso remoto se emplea acceso telefónico a través de circuitos privados a servidores de acceso remoto dedicados que están equipados con modems o adaptadores RDSI. Estas conexiones son lentas y caras en comparación con las de banda ancha, sobre todo para los usuarios remotos que viajan a otros países.

La mayor disponibilidad de acceso de banda ancha a Internet permite a las organizaciones utilizar redes privadas virtuales para los casos en que se precisa acceso remoto. Aunque este sistema permite ahorrar, al eliminar el acceso telefónico, y proporciona una experiencia mejor al usuario, aumenta la vulnerabilidad ante ataques malintencionados cuando los datos propiedad de la empresa se transmiten por Internet.

#### Cumplimiento de los requisitos normativos

Como toda institución financiera, Woodgrove National Bank debe cumplir con estrictos requisitos legales en los distintos países y regiones en los que opera. Además, el banco debe mantener la confianza de los clientes protegiendo los activos corporativos y de los clientes. Woodgrove National Bank ha implementado una iniciativa de protección de los equipos y establecido directivas de seguridad estrictas para todos los equipos con acceso a la red de la empresa, ya sea a través de la red de área local (LAN) o mediante conexiones remotas.

#### Comprobación de las actualizaciones de software

Con la solución existente de acceso remoto, resulta difícil garantizar que los equipos remotos dispongan de las últimas actualizaciones de seguridad, de sus aplicaciones y de sus sistemas operativos. Hasta ahora, el departamento de TI de Woodgrove National Bank no ha podido prevenir el acceso por parte de equipos no autorizados que utilizan programas antivirus obsoletos o con virus activos que puedan infectar la red. Esta debilidad puede suponer un riesgo para la red corporativa y ha obligado a Woodgrove National Bank a limitar la conectividad a un número de usuarios reducido.

El departamento de TI de Woodgrove tiene que superar estos desafíos y proporcionar un servicio confiable y seguro que puedan utilizar los trabajadores remotos, pero sin poner en riesgo la red corporativa. En el resto de este documento se recogen los factores de planeamiento y las decisiones que tuvo que adoptar Woodgrove National Bank para abordar los problemas de la implementación de los servicios de cuarentena de VPN.

[](#mainsection)[Principio de la página](#mainsection)

### Implementación del acceso a la VPN para trabajadores remotos

Al igual que muchas organizaciones, Woodgrove National Bank ha descubierto que numerosos ejecutivos y directores de cuentas son más productivos si pueden trabajar desde su casa al menos un día a la semana. Por ejemplo, los directores de cuentas pueden escribir propuestas, planear reuniones y modificar la información de contacto de sus clientes sin estar en la oficina. Woodgrove National Bank desea ampliar la opción de trabajar desde casa a otras divisiones y departamentos, pero le preocupan los riesgos que pueda conllevar permitir que equipos no conformes con las directivas establecidas por el departamento de TI de Woodgrove se conecten a la red corporativa. Por consiguiente, el departamento de TI de Woodgrove únicamente permite conectarse desde ubicaciones remotas a los empleados que disponen de equipos pertenecientes a los dominios autorizados.

#### Problemas empresariales

El equipo que planea la implementación del acceso a VPN para los trabajadores remotos ha identificado los problemas siguientes:

-   **Coherencia**. Para desarrollar e implementar un servicio de acceso remoto seguro y confiable en toda la empresa, todas las organizaciones y las filiales de Woodgrove National Bank deben cumplir un marco de seguridad uniforme definido con claridad.

-   **Funciones y responsabilidades** **bien definidas**. Diversos grupos del equipo de TI de Woodgrove National Bank se han enfrentado a la falta de claridad con respecto a las funciones y las responsabilidades para poder prestar un servicio seguro. Cuando se planteó la estrategia de seguridad, se hizo patente que la organización tenía que decidir quién sería responsable de la red de acceso remoto. Las discusiones del proceso condujeron a la evaluación de las responsabilidades de los equipos administrativos de TI.

#### Problemas técnicos

El planeamiento y las fases piloto iniciales permitieron identificar los siguientes problemas técnicos:

-   **Almacenamiento de actualizaciones de seguridad y revisiones**. El departamento de TI de Woodgrove decidió utilizar Windows Update para garantizar que los equipos de acceso remoto dispusieran de las actualizaciones de seguridad más recientes. Debido a que Software Update Services (SUS) utiliza el servicio de transferencia inteligente en segundo plano (BITS), Woodgrove consideró que los servidores SUS conectados a Internet resultaban demasiado lentos para actualizar los equipos de acceso remoto. El departamento de TI de Woodgrove descubrió que iniciar Internet Explorer y llevar al usuario a Windows Update permitía actualizar los equipos con rapidez y sin el gasto adicional que suponía tener que administrar servidores adicionales.

-   **Falta de alertas, supervisiones y medidas detalladas**. Para que Woodgrove National Bank administrase con eficacia los aspectos de seguridad, calidad, costo y experiencia del usuario de la solución, los equipos de soporte de TI de Woodgrove necesitaban medir con precisión la calidad de servicio de la solución de acceso remoto. Woodgrove National Bank puede supervisar los principales aspectos del rendimiento del servidor de acceso remoto y el estado global del sistema de acceso remoto, pero no el estado ni la calidad de las conexiones de VPN.

-   **Retraso de aplicaciones en el modo de cuarentena**. Cuando se ejecuta una secuencia de comandos de cuarentena se crea un retraso entre la conexión inicial y el momento en que se levanta la cuarentena del equipo cliente. Este retraso depende del tiempo que se tarde en ejecutar la secuencia de comandos de cuarentena, enviar la notificación y en que el servidor de acceso remoto levante las restricciones de la cuarentena. Sin embargo, algunas aplicaciones intentan realizar conexiones inmediatamente después de que el equipo cliente establece la conexión inicial a la red. Si los filtros de los servicios de cuarentena de VPN no permiten el tráfico de aplicaciones, el servicio de acceso remoto anula el tráfico inicial de la aplicación, y ésta no funcionará correctamente. Los usuarios de acceso remoto deben recibir formación para que no inicien las aplicaciones hasta que la conexión se haya completado.

#### Problemas de seguridad

Los siguientes problemas afectan a la estrategia de seguridad para la implementación de los servicios de cuarentena de VPN en Woodgrove National Bank:

-   **Imposibilidad de administrar clientes remotos**. En la actualidad, Woodgrove National Bank no tiene establecido ni aplica ningún tipo de estándar para los equipos cliente, ni cuenta con ningún modo de obligar a que los clientes remotos cumplan los requisitos de configuración de software, como la habilitación de Windows Firewall, como parte del proceso de inicio de sesión.

-   **Validación de actualizaciones de software**. Woodgrove National Bank no tiene ninguna manera de validar el estado de las actualizaciones de software antivirus y de otros programas relacionados con la seguridad en el equipo cliente antes de permitir su conexión a la red corporativa. Esta situación puede provocar que equipos cliente remotos infectados ataquen los activos de la empresa, con los costos de corrección y tiempo de inactividad consiguientes.

#### Requisitos de la solución

La solución que Woodgrove National Bank implemente para los servicios de cuarentena de VPN debe cumplir los requisitos siguientes:

-   Garantizar que se cumplan todos los requisitos de seguridad de acceso remoto en un marco de tiempo predeterminado antes de permitir las conexiones de acceso remoto sin restricciones a la red corporativa.

-   Garantizar que, cuando los dispositivos se conecten a la red corporativa, no estén accesibles desde otros equipos de la red.

-   Exigir que todos los equipos que se conecten a la red corporativa cumplan las directivas de seguridad de red estandarizadas. Estas directivas incluyen un programa antivirus específico y cumplimiento pleno de las normas de actualización de firmas del antivirus y de instalación de las actualizaciones de seguridad aprobadas.

-   Proporcionar una experiencia al usuario no intrusiva, rápida y fácil de usar.

-   Permitir una implementación sencilla y rentable del software de cliente.

-   Supervisar y registrar toda la actividad de acceso remoto.

-   Proporcionar un servicio confiable y con un alto nivel de disponibilidad.

Una vez marcados estos objetivos, Woodgrove National Bank realizó una investigación y un estudio exhaustivos de las opciones de diseño posibles. En el capítulo 4, "Diseño de la solución", se presentan los resultados de esta investigación.

[](#mainsection)[Principio de la página](#mainsection)

### Uso de Microsoft Operations Framework (MOF)

Woodgrove National Bank utiliza los principios de Microsoft Operations Framework (MOF) para administrar e implementar los cambios en la red empresarial. MOF proporciona una serie de procedimientos recomendados, principios y modelos que ofrecen orientación para lograr el máximo nivel de disponibilidad, confiabilidad y seguridad. Las dos áreas principales a las que afecta el MOF son la administración de cambios y las operaciones.

Para obtener más información sobre MOF, consulte el sitio Web [Microsoft Operations Framework](http://www.microsoft.com/technet/itsolutions/cits/mo/mof/default.mspx) de TechNet, en www.microsoft.com/technet/itsolutions/cits/mo/mof/default.mspx (en inglés).

#### Implementación de la administración de cambios

Los diseñadores de sistemas de Woodgrove National Bank saben que cualquier proyecto de esta envergadura requiere un planeamiento y una administración eficaces. Un comité directivo administrativo debe supervisar el presupuesto, la programación y el desarrollo de los componentes de la solución, y dar su aprobación definitiva en cada fase del proyecto.

El departamento de TI de Woodgrove National Bank entiende la necesidad de probar la solución y realizar implementaciones piloto antes de implementarla en el entorno de producción. Woodgrove opera en un entorno mundial, y conoce la necesidad de cumplir procesos específicos para programar los cambios y proporcionar una comunicación clara al personal directivo, los usuarios y los operadores del servicio de asistencia.

Para garantizar una ejecución sin problemas de los servicios de cuarentena de VPN, Woodgrove National Bank ha planeado establecer equipos virtuales en todo el mundo. Estos equipos deben colaborar estrechamente en el diseño, el desarrollo y las pruebas del diseño y las tecnologías en distintas situaciones. A continuación, los mismos equipos trabajarán en la programación, comunicación y administración de los cambios en el entorno de acceso remoto durante la implementación.

Además, el departamento de TI de Woodgrove debe trabajar con los equipos de soporte de operaciones para programar los cambios, normalmente teniendo en cuenta la hora local que menos afecta a los usuarios o las unidades de negocio. En la mayoría de los casos de acceso remoto, la mejor hora para realizar cambios importantes es el horario laboral entre las 9 a.m. y las 5 p.m. de lunes a viernes, ya que la mayor parte de las conexiones remotas se realizan fuera de este horario. Sin embargo, con el uso cada vez mayor en Woodgrove National Bank del acceso remoto para respaldar la estrategia empresarial durante las horas de trabajo más importantes, esto no siempre es así. Por consiguiente, se necesita un análisis eficaz en cada ubicación individual para garantizar el mínimo efecto de los cambios en el desarrollo de las operaciones.

#### Supervisión de operaciones

Woodgrove National Bank dispone de un marco de supervisión y alertas en toda su red empresarial que utiliza Microsoft Operations Manager (MOM) 2005. El departamento de TI de Woodgrove debe ampliar este marco de modo que abarque la implementación de las soluciones de acceso remoto. Antes de supervisar los servicios de cuarentena de VPN, es preciso instalar [Routing and Remote Access Service Management Pack for MOM](http://www.microsoft.com/downloads/details.aspx?familyid=d1005486-2eeb-44a5-8196-5d4eb24f6ea0&displaylang=en) (en inglés), disponible en www.microsoft.com/downloads/details.aspx?FamilyId=D1005486-2EEB-44A5-8196-5D4EB24F6EA0&displaylang=en.

Para detectar las áreas problemáticas durante la implementación, Woodgrove National Bank utiliza métodos de recopilación y análisis de los datos. El departamento de TI de Woodgrove National Bank utiliza un elemento clave en el proceso de gran utilidad para ayudar a administrar el estado del servicio. Este elemento consiste en un mural de acceso remoto (una serie de indicadores visuales) que supervisa los datos en tiempo real. Este mural permite capturar, mostrar y resaltar incidencias de usuarios individuales que indican problemas de conectividad.

La recopilación y el análisis de los datos son críticos para la administración de los servicios durante cualquier cambio importante y para las funciones de administración del servicio. Al combinar los datos e informes recopilados con los datos del servicio de asistencia, el departamento de TI de Woodgrove National Bank puede determinar cuál es el estado general de un servicio en un momento dado con un alto grado de confiabilidad. Los equipos de operaciones pueden usar estos datos para revisar los eventos que afectan al servicio, contrastar sus efectos en el servicio y generar planes de respuesta activa y predicciones futuras para el servicio.

El registro de estos datos es muy valioso, tanto para medir el uso cotidiano como para identificar las tendencias a largo plazo. Los equipos de soporte de operaciones del departamento de TI de Woodgrove utilizan Microsoft SQL Server™ 2000 y OLAP para generar informes a fin de realizar el seguimiento, medir y analizar con rapidez:

-   El estado general del servicio, con la capacidad de centrarse en aspectos específicos.

-   Los datos de la infraestructura que reflejan el estado y el rendimiento del servidor.

-   Los datos de clientes que reflejan experiencias concretas de los usuarios, como el tiempo que se tarda en conectar, el éxito a la primera, acciones concretas que provocan errores, ubicación de los usuarios y número de acceso de ISP.

-   Los problemas que afectan al servicio y a la productividad de los usuarios.

-   Detalles sobre los costos de funcionamiento más elevados con fines presupuestarios y de planeamiento.

-   Resolución de problemas por parte del servicio de asistencia con respecto a los acuerdos de nivel de servicio (SLA) internos, para detectar las necesidades de mejora de los procesos o la documentación.

Este marco de supervisión y operaciones proporciona a Woodgrove National Bank un entorno apropiado para implementar la solución de cuarentena de VPN. En el último capítulo de esta guía se describe cómo se planeó en Woodgrove National Bank la implementación de los servicios de cuarentena de VPN y las decisiones que se tomaron antes del proceso de ejecución.

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 4: Diseño de la solución

[](#eeac)[Introducción](#eeac)
[](#edad)[Implementación del acceso remoto para trabajadores remotos](#edad)
[](#ecae)[Consideraciones adicionales](#ecae)
[](#ebad)[Implementación de la supervisión y la administración](#ebad)
[](#eaaz)[Resumen](#eaaz)

### Introducción

Ahora que ya conoce los factores que debe abordar toda solución de red privada virtual (VPN), puede comenzar con el proceso de diseño. Este proceso de diseño incluye la identificación de los elementos de planeamiento esenciales y la realización de un análisis lógico de los requisitos de la solución.

Woodgrove National Bank ha llevado a cabo una valoración de los problemas empresariales, técnicos y de seguridad que la solución debe abordar. En este capítulo se explican los problemas de planeamiento que tuvieron en cuenta los diseñadores de sistemas, las conclusiones a las que llegaron y las decisiones resultantes que tomaron para crear la solución elegida.

[](#mainsection)[Principio de la página](#mainsection)

### Implementación del acceso remoto para trabajadores remotos

Los trabajadores remotos de Woodgrove National Bank que trabajan desde ubicaciones remotas requieren una conexión uniforme y confiable a la red corporativa. Las dificultades o un retraso excesivo en la conexión provocan frustración y falta de confianza en el servicio. Implementar servicios de cuarentena de VPN puede aumentar la frustración, puesto que se tarda más tiempo en conectarse a la red. El departamento de TI de Woodgrove National Bank debe supervisar los plazos de conexión y tomar medidas para minimizarlos. Las secuencias de comandos de conexión deben informar a los usuarios del estado de la conexión en cada fase del proceso.

Los administradores de la red necesitan que los equipos de acceso remoto cumplan las directivas de acceso a la red antes de tener acceso a los recursos de la red. La mejor manera de proteger la red corporativa es poner en cuarentena los equipos de acceso remoto y asegurarse de que cumplan las directivas de seguridad de la red antes de permitirles tener acceso a sus recursos.

#### Concepto de la solución

La solución utiliza una combinación de secuencias de comandos antes de conectar, agentes de cliente y componentes de Microsoft® Windows Server™ 2003 con Service Pack 1 (SP1). Los equipos cliente inician la conexión a la VPN utilizando un perfil de Connection Manager personalizado. Un perfil de Connection Manager es un archivo ejecutable autoextraíble que se crea mediante el Kit de administración de Connection Manager (CMAK) e incluye secuencias de comandos y configuraciones. Una secuencia de comandos de acciones antes del túnel obliga al cliente a instalar las actualizaciones de seguridad más recientes antes de crear la conexión a la VPN. Los equipos de acceso remoto obtienen sus actualizaciones a través de servidores conectados a Internet administrados por Woodgrove National Bank, del proveedor del programa antivirus y del sitio Web de Windows Update.

El equipo cliente establece una conexión a la VPN después de haber obtenido las actualizaciones necesarias y autentica las credenciales del usuario con respecto al servicio de directorios Active Directory® mediante el Servicio de autenticación de Internet (IAS). A continuación, el servidor de acceso remoto restringe la conexión entrante mediante filtros de paquetes de cuarentena que únicamente permiten un acceso limitado a los recursos. Una vez el cliente ha confirmado que el equipo cumple los requisitos de seguridad necesarios, el servidor de acceso remoto levanta las restricciones de la cuarentena y el equipo cliente puede tener acceso a todos los recursos autorizados de la intranet.

#### Requisitos previos de la solución

Antes de empezar un proyecto de esta naturaleza, es preciso cumplir algunos requisitos previos. En la sección siguiente se proporcionan algunos requisitos previos generales para los servicios de cuarentena de VPN.

#### Consulta a usuarios y grupos

Uno de los pasos más importantes al planear un cambio que afecta a un servicio prestado a los usuarios es consultar a los propios usuarios y grupos afectados. Los usuarios ofrecen comentarios de gran valor sobre los problemas y el rendimiento de un servicio existente. Además, los usuarios pueden señalar qué características y experiencia desean obtener del nuevo servicio. Los usuarios deben comprender qué pueden esperar del servicio y qué no. Administrar sus expectativas puede ser clave para conseguir la aceptación de los usuarios. La organización puede valorar el éxito del proyecto si se establecen objetivos medibles.

Woodgrove opera en varios países y regiones y tiene centros regionales de soporte. El equipo inicial sondeó exhaustivamente las opiniones de los usuarios y de los equipos de soporte para identificar e implicar en la fase piloto a posibles usuarios, grupos y personal de soporte.

#### Selección del personal para el proyecto

Es importante tener en cuenta la combinación de tipos de personal y las habilidades que se necesitan para implementar un proyecto de esta naturaleza. El equipo del proyecto debe determinar si dispone internamente de los requisitos necesarios en cuanto a habilidades o si es preciso contratar personal adicional. Dado que no todas estas personas son necesarias en todas las fases del proyecto, se debe comprobar la disponibilidad de cada una de ellas a lo largo del plan del proyecto. Las funciones necesarias son, entre otras, diseñadores de redes, administración de redes, equipo de administración de servidores, programadores de secuencias de comandos, equipo de seguridad de infraestructuras y equipo de dirección del proyecto.

#### Planeamiento de la solución

Durante el proceso de planeamiento, Woodgrove tuvo en cuenta las necesidades siguientes:

-   Implementación de proyectos piloto o pruebas.

-   Administración de servidores de la red perimetral con Servicios de Terminal Server.

-   Actualización de las secuencias de comandos de cuarentena.

-   Recopilación de datos de rendimiento.

#### Implementación de proyectos piloto o pruebas

El tamaño y la envergadura de la organización rigen el tamaño y la cantidad de proyectos piloto. El departamento de TI de Woodgrove implementó dos proyectos piloto, el primero de ellos para probar el concepto y conseguir la participación de usuarios de acceso remoto experimentados que pusieran de manifiesto los puntos débiles potenciales a fin de mitigar los posibles problemas empresariales y tecnológicos. El proyecto piloto inicial proporcionaba acceso limitado a los recursos corporativos para garantizar que ningún equipo que pareciese cumplir la directiva de seguridad tuviese problemas de seguridad. Antes de implementar una solución que pueda poner en riesgo la red corporativa, cualquier organización que implemente una solución de cuarentena de VPN debe asegurarse de que ningún equipo infectado o que carezca de las actualizaciones apropiadas pueda eludir las comprobaciones de seguridad de los servicios de cuarentena. En el segundo proyecto piloto participó una base de usuarios mucho mayor, que incluía a varios usuarios sin experiencia que ofreciesen una prueba más realista de los problemas de soporte que probablemente surgirían.

#### Administración de servidores de la red perimetral con Servicios de Terminal Server

El equipo de TI de Woodgrove utiliza el modo de administración con Servicios de Terminal Server para administrar los servidores existentes en la red perimetral. El equipo de TI de Woodgrove debía incorporar a esta lista los servidores de actualización conectados a Internet y los servidores de acceso remoto a la VPN. Woodgrove debía tener en cuenta cómo actualizar y mantener estos importantes servidores.

#### Actualización de las secuencias de comandos de cuarentena

Con el paso del tiempo, es preciso actualizar las secuencias de comandos de cuarentena con nuevas generaciones de los perfiles de Connection Manager. Woodgrove decidió distribuir los perfiles de Connection Manager por medio de un servidor Web que requiere la autenticación del usuario. Los usuarios de acceso remoto reciben un mensaje de correo electrónico para notificar al usuario el punto de distribución.

#### Recopilación de datos de rendimiento

La medición del rendimiento es un factor clave para mejorar el servicio. El departamento de TI de Woodgrove debe supervisar los servidores para comprobar su rendimiento, confiabilidad y seguridad. El equipo de red debe poder integrar la solución de cuarentena de VPN en la estructura existente de supervisión y administración.

#### Arquitectura de la solución

La solución de cuarentena de VPN de Woodgrove National Bank necesita los componentes siguientes:

-   Equipos cliente en los que se ejecute Windows XP Professional con SP2 o posterior.

-   Perfiles de Connection Manager creados con CMAK.

-   Secuencias de comandos de cliente incrustadas en los paquetes de cliente de Connection Manager.

-   Componente de cliente de los servicios de cuarentena de VPN.

-   Un servidor de acceso remoto que ejecute Windows Server 2003 con SP1 o posterior y que tenga instalado el Servicio de cuarentena de acceso remoto.

-   Un filtro de puerto IP de cuarentena.

-   Servicio de autenticación de Internet (IAS) ejecutándose en Windows Server 2003.

-   Active Directory.

El departamento de TI de Woodgrove consideró en principio la posibilidad de admitir todas las versiones de Windows implementadas actualmente. Sin embargo, la mayor concienciación en cuanto a la amenaza a que se exponen los equipos conectados a Internet llevó al departamento de TI a estandarizar los sistemas operativos de los equipos a Windows XP Professional con SP2. Aunque Woodgrove podría permitir que equipos que ejecuten Windows XP Home Edition con SP2 se conecten a través de la VPN, el departamento de TI de Woodgrove decidió no admitir esta configuración porque un equipo basado en Windows XP Home Edition no puede unirse a un dominio. Cuando el departamento de TI implemente la solución inicial, Woodgrove pretende ampliar la solución a los equipos que los usuarios tienen en sus casas.

Una de las comprobaciones antes de la conexión es confirmar que Windows Firewall está habilitado. Woodgrove no especifica ninguna excepción en la secuencia de comandos, pero establece excepciones como la conexión posterior de Escritorio remoto.

CMAK es la herramienta utilizada para configurar el perfil de Connection Manager que contiene todo el software con licencia para comenzar el intento de conexión, incluido el componente de notificación de cliente (RQC.exe) y la secuencia de comandos inicial de los servicios de cuarentena. Woodgrove National Bank utiliza un servidor Web para distribuir estos perfiles. Cuando Woodgrove National Bank actualiza el perfil de Connection Manager, notifica a los usuarios por correo electrónico que el nuevo perfil es obligatorio a partir de una fecha determinada.

**Nota:** otras estrategias alternativas pueden incluir el uso de cualquier mecanismo de distribución del software, como una Directiva de grupo, Microsoft Systems Management Server (SMS) 2003; o bien, para los usuarios que desean conectarse a la red desde el equipo de su casa, se puede colocar el perfil en una llave USB protegida mediante contraseña.

El acceso remoto en Windows Server 2003 proporciona características apropiadas para actuar como host y enrutador de la red privada virtual (VPN). Windows Server 2003 con SP1 incluye el servicio de cuarentena de acceso remoto (RQS), un componente clave en la solución de cuarentena de VPN. RQS es el componente de escucha de servidor, que se implementa en un archivo ejecutable, RQS.exe. El CMAK incluye el componente de notificación (RQC.exe).

El filtro de puerto de cuarentena permite únicamente las comunicaciones entre el cliente de VPN en cuarentena y una serie de recursos limitados de la red. Los filtros de paquetes permiten que el agente de cliente se comunique con el componente de escucha del servidor de acceso remoto para que se pueda llevar a cabo la autenticación del usuario.

El servicio IAS que se ejecuta en Windows Server 2003 es la implementación de Microsoft de un servidor RADIUS y un servidor proxy RADIUS. IETF (Internet Engineering Task Force) describe RADIUS en los RFC 2865 y 2866. IAS autentica las solicitudes de acceso remoto y proporciona información de cuentas. El departamento de TI de Woodgrove tiene contratos con varios proveedores de servicios de Internet (ISP), lo que permite disponer de acceso itinerante a Internet en varios países y regiones. El ISP configura sus servidores RADIUS de modo que las solicitudes de autenticación pasen por los servidores IAS de Woodgrove. Este proceso de autenticación requiere el uso de un servidor proxy RADIUS con los servidores RADIUS del ISP configurado para volver a los servidores IAS de Woodgrove. Al utilizar IAS para la autorización, Woodgrove se beneficia de las características de administración de cuentas de RADIUS para realizar el seguimiento del uso de la VPN de acceso remoto.

Las cuentas de usuarios y las pertenencias a grupos de Active Directory regulan la conexión remota y el acceso subsiguiente a los recursos corporativos de la entidad Woodgrove National Bank. Además, Woodgrove National Bank utiliza objetos de Directiva de grupo (GPO) para configurar las estaciones de trabajo de Windows de modo que satisfagan las directivas de seguridad de la red corporativa.

#### Cómo funciona la solución

En la siguiente figura se ilustra cómo implementó Woodgrove National Bank la solución de cuarentena de VPN.

[![](images/Cc162926.PGFG0401(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc162926.pgfg0401_big(es-es,technet.10).gif)

**Figura 4.1 Proceso de los servicios de cuarentena de VPN en Woodgrove National Bank**

La solución de cuarentena de VPN de Woodgrove National Bank funciona de la manera siguiente:

1.  El usuario selecciona el perfil de conexión a la VPN. Como alternativa, una aplicación puede solicitar un recurso en la intranet corporativa.

2.  El perfil de Connection Manager inicia una conexión a Internet mediante una entrada de acceso telefónico. Si el cliente ya está conectado a Internet, Connection Manager omite este paso.

3.  Las acciones personalizadas antes del túnel ejecutan secuencias de comandos para asegurarse de que el equipo tenga instaladas las actualizaciones de seguridad y las firmas del antivirus actualizadas. El equipo cliente se conecta a Windows Update para instalar estas actualizaciones. Para obtener ejemplos de secuencias de comandos personalizadas adecuadas para las acciones personalizadas antes del túnel, consulte el apéndice A, "Ejemplos de secuencias de comandos para servicios de cuarentena" en esta guía.

4.  Si las actualizaciones se aplican correctamente, el perfil de Connection Manager se conecta al servidor de VPN. Si cualquiera de las actualizaciones no se realiza correctamente, el perfil de Connection Manager informa de ello al usuario y termina el intento de conexión a la VPN.

5.  El equipo cliente de acceso remoto pasa las credenciales de autenticación al servidor de acceso remoto, que envía un mensaje de solicitud de acceso RADIUS al servidor IAS. IAS autentica las credenciales del usuario con respecto a Active Directory. Si las credenciales son válidas, IAS comprueba las directivas de acceso remoto para ese usuario.

6.  El servidor de VPN acepta la conexión y establece el tiempo de espera de cuarentena y los atributos de los filtros IP. El servidor IAS envía un mensaje de aceptación del acceso que contiene los atributos MS-Quarantine-IPfilter y MS-Quarantine-Session-Timeout. El servidor de VPN aplica estos atributos al filtro del servicio de cuarentena y establece el temporizador de la sesión. El equipo cliente de acceso remoto sólo puede transmitir correctamente el tráfico que coincida con los criterios de los filtros de cuarentena. El cliente de acceso remoto debe notificar al servidor de acceso remoto que la secuencia de comandos de cuarentena se ha completado correctamente antes de que transcurra el número de segundos especificado por el atributo MS-Quarantine-Session-Timeout.

7.  El componente de escucha informa al servidor de acceso remoto de que el cliente cumple los requisitos de la directiva. El servidor de acceso remoto recibe esta notificación porque se corresponde con la regla de tráfico (puerto 7250) especificada en el atributo MS-Quarantine-IPfilter. El servidor de acceso remoto levanta las restricciones de la configuración de MS-Quarantine-IPfilter y MS-Quarantine-Session-Timeout de la conexión, y configura las restricciones normales de conexión prescritas en la directiva de acceso remoto.

8.  A partir de ese momento los usuarios pueden tener acceso a los recursos de red autorizados.

**Nota:** Una secuencia de comandos después de la conexión comprueba la versión del paquete de Connection Manager. Si la versión del equipo remoto está atrasada en más de dos versiones secundarias o una versión principal, el equipo remoto descarga el paquete de Connection Manager más reciente, informa al usuario y anula la conexión. En este momento, el equipo remoto ya tiene la lista de revisiones más recientes y el usuario remoto puede conectarse de nuevo.

Para implementar esta solución es preciso que varios procesos se ejecuten en el cliente y el servidor. En la siguiente sección se explican estos requisitos.

#### Implementación de acciones personalizadas mediante secuencias de comandos

Las secuencias de comandos que se ejecutan en varios puntos del ciclo de conexión llevan a cabo la mayoría de las operaciones del cliente para la solución de cuarentena de VPN. Un elemento vital de esta solución depende de si determinadas comprobaciones se ejecutan antes del túnel o después de la conexión. Si una comprobación determinada se ejecuta fuera de orden, puede dejar el equipo a merced de vulnerabilidades innecesarias y crear otras dificultades. La sección siguiente contiene la lista de comprobaciones diseñadas para esta solución.

##### Implementación de las comprobaciones antes del túnel

Si el cliente aún no está conectado, Connection Manager inicia una conexión a Internet. Después de que el cliente se conecta a Internet, las acciones antes del túnel sincrónicas llevan a cabo las comprobaciones de seguridad obligatorias antes de establecer el túnel de VPN.

Connection Manager ejecuta todas las comprobaciones de seguridad necesarias en orden secuencial. Connection Manager implementa cada comprobación en una serie de secuencias de comandos. En los siguientes pasos se facilita la lógica de trabajo que necesitan esas secuencias de comandos.

1.  **¿Sistema operativo admitido?**  

    -   En caso negativo, mostrar cuadro de mensaje al usuario y anular la conexión.

    -   En caso afirmativo, continuar.

2.  **¿Software antivirus instalado y en ejecución?**  

    -   En caso negativo, mostrar cuadro de mensaje al usuario y anular la conexión. El software con licencia que se necesita como parte de una acción antes del túnel debe incluirse en el paquete de instalación de Connection Manager para evitar la necesidad de instalarlo desde un servidor remoto.

    -   En caso afirmativo, continuar.

3.  **Actualizar archivos de firmas del antivirus**

    -   Si se realiza correctamente, continuar.

    -   Si no se realiza correctamente, continuar con advertencia o mostrar cuadro de mensaje al usuario y anular la conexión.

4.  **¿Está configurado el cliente de actualización automática de Windows?**  

    -   En caso negativo, configurar el cliente del servicio de actualización automática de Windows.

    -   Si se realiza correctamente, continuar.

    -   Si no se realiza correctamente, continuar con advertencia o mostrar cuadro de mensaje al usuario y anular la conexión.

    -   En caso afirmativo, continuar.

5.  **Descargar e instalar actualizaciones de software de alta prioridad**

    -   Si se realiza correctamente, continuar.

    -   Si no se realiza correctamente, continuar con advertencia o mostrar cuadro de mensaje al usuario y anular la conexión.

6.  **Exigir el uso de “Iniciar sesión mediante una conexión de acceso telefónico” (opcional)**

    -   Si se utiliza, continuar.

    -   Si no se utiliza, continuar con advertencia o mostrar cuadro de mensaje al usuario y anular la conexión. El uso de esta comprobación implica que únicamente podrán conectarse los equipos que se hayan unido al dominio y que los clientes remotos deben unirse al dominio conectándose al menos una vez a la red de área local (LAN) corporativa. Si se utiliza esta opción, no es posible unirse al dominio mediante una conexión remota a no ser que el departamento de TI de Woodgrove proporcione una excepción provisional para las comprobaciones de seguridad obligatorias (consulte el tema Administración de excepciones y exclusiones en este mismo capítulo).

7.  **Ejecutar las comprobaciones adicionales de seguridad personalizadas (opcional)**

    Debido a que el acceso a Internet únicamente está disponible en este punto del proceso de conexión, es preciso diseñar las comprobaciones de seguridad personalizadas teniendo en cuenta esta limitación.

**Nota:** para obtener una descripción de un conjunto de ejemplos de secuencias de comandos, consulte el apéndice A, "Ejemplos de secuencias de comandos para servicios de cuarentena" en esta guía.

Connection Manager registra los resultados de estas acciones antes del túnel en el Registro, con la clave siguiente:

**HKEY\_CURRENT\_USER\\Software\\MyCompany\\MyConnectionManager\\PreTunnelResults.**

Las acciones antes del túnel siempre deben devolver registros de acierto y la acción después de la conexión del agente del servicio de cuarentena de acceso remoto debe comprobar estos resultados para determinar el estado que debe enviar al servidor de VPN. Este planteamiento permite una administración de excepciones flexible sin modificar Connection Manager. En la ilustración siguiente se muestra la lógica de la secuencia de comandos de acciones personalizadas antes del túnel utilizada por Woodgrove National Bank.

[![](images/Cc162926.PGFG0402(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc162926.pgfg0402_big(es-es,technet.10).gif)

**Figura 4.2 Acciones antes del túnel de Woodgrove National Bank**

##### Implementación de las comprobaciones después de la conexión

Una vez el cliente ha superado todas las comprobaciones antes del túnel, Connection Manager establece la conexión a la VPN. Las secuencias de comandos después de la conexión pueden llevar a cabo cualquier comprobación adicional no obligatoria y acciones administrativas después de que el cliente ha obtenido acceso a la red corporativa.

1.  **Conexión a la red privada virtual**

    Cuando se han completado todas las acciones antes del túnel, Connection Manager establece una conexión al servidor de VPN.

2.  **Envío de la notificación**

    Connection Manager utiliza el componente de cliente (RQC.exe) para enviar la clave compartida al servicio de cuarentena de acceso remoto (RQS.exe) del servidor de VPN, que levanta las restricciones de la directiva de cuarentena.

3.  **Caducidad de la contraseña**

    Woodgrove National Bank ejecuta una secuencia de comandos que comprueba cuándo caduca la contraseña y notifica al usuario si debe cambiarla.

    **Nota:** la notificación de la caducidad de la contraseña tiene lugar únicamente si el cliente utiliza la opción **Iniciar sesión mediante una conexión de acceso telefónico** para conectarse remotamente a la red corporativa.

4.  **Actualización de directiva de grupo**

    Si un cliente que pertenece a un dominio no utiliza la opción **Iniciar sesión mediante una conexión de acceso telefónico** para conectarse remotamente a la red corporativa, no se aplican las actualizaciones de la Directiva de grupo. Esto puede provocar riesgos para la seguridad cuando la Directiva de grupo se utiliza para imponer las opciones de seguridad críticas a los clientes. Para mitigar este problema potencial, Woodgrove National Bank ejecuta una secuencia de comandos después de la conexión que actualiza la Directiva de grupo después de que el usuario haya iniciado sesión. Una secuencia de comandos utiliza el comando **gpupdate.exe /force /wait:0** para actualizar inmediatamente la configuración de la Directiva de grupo. Para obtener más información sobre las utilidades de actualización de la Directiva de grupo, consulte [Una descripción de la utilidad de actualización de Directiva de grupo](http://support.microsoft.com/default.aspx?scid=kb;es-es;298444) en http://support.microsoft.com/default.aspx?scid=kb;es-es;298444.

En la ilustración siguiente se proporcionan los detalles de la lógica de la secuencia de comandos de acciones personalizadas después de la conexión.

[![](images/Cc162926.PGFG0403(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc162926.pgfg0403_big(es-es,technet.10).gif)

**Figura 4.3 Acciones después de la conexión de Woodgrove National Bank**

#### Creación y distribución de perfiles de Connection Manager

Connection Manager ofrece un mecanismo cómodo para proporcionar a los usuarios acceso rápido, sencillo y confiable a los recursos corporativos. Woodgrove National Bank decidió implementar sus conexiones personalizadas a la VPN mediante perfiles de Connection Manager creados por su departamento de TI mediante el CMAK.

Dado que Woodgrove National Bank tiene que configurar las conexiones de decenas de miles de clientes y cientos de números de acceso telefónico, el departamento de TI de Woodgrove debe estudiar la información siguiente antes de la configuración:

-   Las configuraciones de las conexiones de acceso telefónico o de conexión a la VPN varían, según algunos factores como ubicación, hora del día, etc.

-   Para ayudar a evitar errores, no se permite a los usuarios configurar ni modificar las propiedades de acceso telefónico ni de conexión a la VPN.

-   Algunas funciones tienen que ser dinámicas y el personal de TI de Woodgrove administra estos valores para asegurarse de que se cumplan las normas de seguridad.

-   El método de configuración debe ampliarse a la escala de una empresa mundial.

La tabla siguiente incluye algunas de las capacidades de Connection Manager para las conexiones de acceso remoto utilizadas por el departamento de TI de Woodgrove.

**Tabla 4.1: Características de Connection Manager utilizadas por el departamento de TI de Woodgrove**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Característica</th>
<th style="border:1px solid black;" >Capacidad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Transmisión de la imagen de marca</td>
<td style="border:1px solid black;">Gráficos, iconos, mensajes y ayuda personalizados dotan al paquete del aspecto y el diseño corporativos. Los paquetes de Connection Manager pueden proporcionar números de asistencia técnica locales para los usuarios que viajan.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Acciones personalizadas</td>
<td style="border:1px solid black;">Registro y actualizaciones de aplicaciones.</td>
</tr>
</tbody>
</table>
  
El departamento de TI de Woodgrove puede distribuir los perfiles de Connection Manager a usuarios remotos en un CD-ROM, por correo electrónico, a través de un sitio Web o en archivos compartidos. Woodgrove National Bank ya distribuye software y actualizaciones en un sitio Web conectado a Internet. Dado que ya contaba con una infraestructura de soporte, Woodgrove eligió este método para distribuir los perfiles de Connection Manager.
  
#### Uso de filtros IP para el acceso a la red en cuarentena
  
La combinación de acciones personalizadas y el soporte de atributos específicos del proveedor permite que Connection Manager admita el acceso a la red en cuarentena. Los atributos específicos del proveedor son extensiones permitidas del estándar de RADIUS, que no se definen en el estándar de RADIUS RFC 2138. Los atributos del proveedor de Microsoft que constituyen la versión para Windows Server 2003 de IAS son:
  
-   MS-Quarantine-IPFilter
  
-   MS-Quarantine-Session-Timeout
  
#### Atributo MS-Quarantine-IPFilter
  
Este atributo permite el tráfico entrante desde el componente de notificación del cliente (RQC) una vez que la secuencia de comandos se ha completado correctamente. Por ejemplo, la red de Woodgrove National Bank debe permitir los protocolos DNS y DHCP para que el cliente remoto se pueda comunicar con los servidores de la infraestructura durante las operaciones de los servicios de cuarentena.
  
**Nota:** el uso de filtros para permitir protocolos específicos reduce la seguridad global. Únicamente deben incluirse estos protocolos en la definición de los servicios de cuarentena en caso de que sea necesario.
  
La tabla siguiente muestra los puertos TCP/IP que abre el filtro IP de cuarentena de Woodgrove National Bank.
  
**Tabla 4.2: Puertos TCP/IP abiertos en el filtro de cuarentena de VPN**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Número de puerto</th>
<th style="border:1px solid black;" >Uso</th>
<th style="border:1px solid black;" >Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">UDP 67, 68</td>
<td style="border:1px solid black;">DHCP</td>
<td style="border:1px solid black;">Solicita una dirección IP para el cliente</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">UDP 53</td>
<td style="border:1px solid black;">DNS</td>
<td style="border:1px solid black;">Resolución de nombres</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">UDP 137</td>
<td style="border:1px solid black;">WINS</td>
<td style="border:1px solid black;">Resolución de nombres NetBIOS</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">TCP 139, 445</td>
<td style="border:1px solid black;">Uso compartido de archivos</td>
<td style="border:1px solid black;">Sólo se debe habilitar si es absolutamente necesario, proporciona sesión de NetBIOS y uso compartidos de archivos SMB</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">TCP 7250</td>
<td style="border:1px solid black;">RQC, RQS</td>
<td style="border:1px solid black;">Permite la comunicación entre el agente de cliente de los servicios de cuarentena de VPN y el componente de escucha del servidor</td>
</tr>
</tbody>
</table>
  
#### MS-Quarantine-Session-Timeout
  
Este atributo establece el máximo tiempo de espera durante el que permanecerá en cuarentena el equipo cliente. Si la secuencia de comandos no se completa en este plazo, el servidor de acceso remoto desconecta el equipo cliente. Woodgrove National Bank implementó un límite del tiempo de espera de 120 segundos; con este plazo se anula menos del uno por ciento de las conexiones entrantes.
  
En la siguiente ilustración se muestran los atributos específicos del proveedor que es preciso configurar en la directiva de acceso remoto para dar soporte a los servicios de cuarentena de VPN.
  
[![](images/Cc162926.PGFG0404(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc162926.pgfg0404_big(es-es,technet.10).gif)
  
**Figura 4.4 Atributos específicos del proveedor de MS necesarios para los servicios de cuarentena de VPN.**
  
Durante el proceso de pruebas del proyecto piloto, compruebe si quitar cualquiera de los puertos permitidos en el filtro IP de cuarentena evita que el cliente se conecte. Reduzca el valor del tiempo de espera al mínimo que resulte práctico y auméntelo lo necesario para soportar el incremento de la latencia de red o los vínculos de baja velocidad.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Consideraciones adicionales
  
En esta sección se abordan algunos aspectos adicionales que el departamento de TI de Woodgrove tuvo en cuenta al implementar los servicios de cuarentena de VPN.
  
#### Configuración del registro de datos y cuentas
  
Una ventaja de utilizar IAS es el soporte incorporado para el registro de las conexiones de clientes a través de RADIUS. Woodgrove National Bank desea supervisar qué trabajadores se conectan a la red corporativa. El registro no es necesario para implementar una solución de acceso remoto utilizando los servicios de cuarentena de VPN, pero Microsoft lo considera muy recomendable. RADIUS/IAS brinda a Woodgrove la posibilidad de analizar tendencias por lo que respecta a las conexiones, con objeto de mejorar el servicio.
  
Cada servidor IAS RADIUS recopila datos sobre la sesión del usuario, que almacena en SQL Server 2000 Desktop Engine (MSDE 2000), una base de datos ligera y local de SQL Server 2000. Esta base de datos puede recopilar datos de rendimiento de los servidores de la infraestructura y datos específicos de los clientes, y se ejecuta en cada servidor IAS que recopila datos de las sesiones de los usuarios.
  
El servidor IAS transfiere la información desde MSDE a una base de datos central SQL Server 2000 casi en tiempo real. Esta disposición garantiza un uso rentable de las licencias de SQL Server y no altera el rendimiento.
  
Woodgrove National Bank implementó a escala regional servidores de recopilación de datos basados en SQL Server para recabar información de las sesiones de acceso remoto. Para obtener más información sobre la configuración del registro de datos en SQL Server con IAS, consulte el tema [Deploying SQL Server Logging with Windows Server 2003 Internet Authentication Service (IAS)](http://www.microsoft.com/downloads/details.aspx?familyid=6e4357f7-4070-4902-95f1-3ad411d963b2&displaylang=en) (en inglés) en www.microsoft.com/downloads/details.aspx?FamilyId=6E4357F7-4070-4902-95F1-3AD411D963B2&displaylang=en.
  
#### Implementación de proyectos piloto
  
Antes de ejecutar cualquier solución de acceso remoto en el entorno de producción, es preciso probarla en una implementación piloto. Lo ideal es que el proyecto piloto sea una versión a escala reducida de la solución planeada.
  
Woodgrove National Bank implementó dos programas piloto: un proyecto piloto inicial para usuarios experimentados y otro más general con una mayor variedad de participantes. El equipo de TI de Woodgrove supervisó el proyecto piloto y utilizó los resultados para modificar el diseño definitivo.  
  
#### Garantía de alta disponibilidad
  
Puesto que Woodgrove National Bank opera en un entorno internacional con sitios en todo el mundo, la solución elegida debe ofrecer la máxima confiabilidad. Por consiguiente, Woodgrove National Bank debe tener en cuenta sus necesidades de disponibilidad, que incluyen:
  
-   Varios servidores de VPN con carga equilibrada.
  
-   Servidores IAS con carga equilibrada.
  
-   Tolerancia a fallos en sus servidores de actualizaciones de software y antivirus.
  
-   Rutas de acceso a la red internas redundantes para garantizar que el fallo de un enrutador o un conmutador no impida el acceso a los servidores internos.
  
El departamento de TI de Woodgrove utiliza Microsoft Application Center 2000 para proporcionar clústeres de aplicaciones Web y la funcionalidad de equilibrio de carga de red (NLB) para sus sitios Web. Además, Microsoft Application Center y NLB proporcionan tolerancia a fallos en los servidores de actualización conectados a Internet. Woodgrove National Bank utiliza NLB, una característica estándar de Windows Server 2003 Enterprise Edition para equilibrar la carga en los servidores IAS.
  
#### Garantía de un ancho de banda de red adecuado
  
Los diseñadores de sistemas deben tener en cuenta las rutas existentes de acceso a la red, los tiempos de conexión previstos y el tipo y volumen de tráfico de acceso remoto previsto. No debe subestimarse el ancho de banda adicional que los usuarios de acceso remoto pueden precisar.
  
Las implementaciones piloto deben ayudar a analizar el tráfico de acceso remoto y el efecto que puede ejercer en la infraestructura existente. Es importante que las pruebas incluyan a trabajadores típicos realizando un uso ordinario, porque la solución no tendrá éxito si el servicio es insuficiente. Los conmutadores de red que incorporan perfiles de ancho de banda pueden reducir los efectos del tráfico de acceso remoto sobre los demás usuarios.
  
Woodgrove National Bank dispone de una conectividad de Internet adecuada con alto ancho de banda. El banco utiliza la mayoría del ancho de banda existente para el acceso interno a Internet con fines de exploración de la Web y de correo electrónico, por lo que es posible que sea necesario realizar algunos ajustes para acomodar el tráfico de acceso remoto adicional.
  
#### Administración de excepciones y exclusiones
  
Los diseñadores de sistemas de Woodgrove National Bank comprenden que cualquier solución debe incluir las situaciones en que las necesidades de la empresa requieren la capacidad de conceder excepciones provisionales a uno o varios dispositivos con respecto a los requisitos de los servicios de cuarentena. Por ejemplo, puede suceder que el equipo de IT tenga que proporcionar una excepción para el acceso de un ejecutivo durante una reunión de especial importancia. En consecuencia, la solución de acceso a la VPN debe admitir las excepciones.
  
La incapacidad para proporcionar excepciones para un equipo individual podría obligar al administrador a quitar los requisitos de acceso remoto. A no ser que la organización sea capaz de administrar excepciones individuales, el equipo de TI no puede implementar la solución.
  
**Nota:** el grupo de seguridad de TI de Woodgrove debe ser la única autoridad que determine si las necesidades empresariales que motivan una excepción son mayores que el consiguiente riesgo para la seguridad.
  
La organización debe considerar los siguientes casos excepcionales:
  
-   **Miembros que no pertenecen al dominio**. Una empresa puede permitir que tengan acceso a la red clientes remotos no pertenecientes a un dominio. Sin embargo, esta excepción provoca costos adicionales de administración, porque muchas otras opciones de seguridad y administrativas requieren la Directiva de grupo. La Directiva de grupo sólo está disponible para los equipos que pertenecen a un dominio.
  
-   **Opción de inicio de sesión en un dominio**. Si un usuario de un equipo perteneciente a un dominio no selecciona la opción de inicio de sesión de Windows al iniciar sesión mediante Connection Manager, Windows inicia la sesión del usuario con las credenciales almacenadas en caché. Las credenciales en caché pueden no autenticarse en caso de que se modifique o caduque una contraseña.
  
-   **Tiempos de espera de las aplicaciones**. Las aplicaciones pueden no funcionar bien si un equipo permanece en cuarentena demasiado tiempo y el retraso hace que se agote el tiempo de espera de la aplicación. Este efecto puede deteriorar los datos.
  
Una forma de evitar este problema es crear filtros de paquetes de entrada que permitan que el tráfico de la aplicación funcione de la manera prevista mientras el cliente de acceso remoto está en cuarentena. El inconveniente de seguir este sistema es el mayor costo que supone identificar el tráfico de red de la aplicación y la creación de los filtros de paquetes adicionales.
  
Microsoft recomienda mantener el mínimo número posible de filtros de paquetes de cuarentena y utilizar acciones personalizadas antes del túnel para superar este problema. La implementación de filtros de paquetes de cuarentena incorrectos puede exponer a los controladores de dominio a la red de cuarentena.
  
Algunas configuraciones pueden mitigar el retraso que sufren las aplicaciones al conectarse a una red de cuarentena. Aunque Microsoft no recomienda configuraciones que expongan la red, las organizaciones deben proporcionar soluciones para las aplicaciones esenciales. Deben considerarse las siguientes soluciones:
  
-   Comentarios para el usuario
  
-   Uso de un tiempo de espera de la sesión de cuarentena únicamente
  
-   Uso de la notificación inmediata
  
#### Comentarios para el usuario
  
Puede proporcionar comentarios al usuario mediante la interfaz de Connection Manager, para informarle del punto del proceso de conexión en que se encuentra. Esto ayuda a mitigar la frustración que experimentan los usuarios cuando parece que no sucede nada.
  
#### Uso de un tiempo de espera de la sesión de cuarentena únicamente
  
Esta configuración requiere que se configure el atributo MS-Quarantine-Session-Timeout pero no el atributo MS-Quarantine-IPFilter. El servidor de acceso remoto proporciona acceso normal inmediato al cliente de acceso remoto, sin restringirlo mediante filtros de paquetes de cuarentena. Sin embargo, el cliente de acceso remoto debe enviar igualmente el mensaje de notificación que indica que cumple las directivas de la red. El servidor de acceso remoto desconectará el equipo cliente si no envía la notificación antes de que se agote el tiempo de espera de la sesión de cuarentena.
  
Las ventajas de esta configuración son que no se necesita configurar ningún filtro de paquetes de cuarentena y que no se presentan problemas de retraso en las aplicaciones. El acceso remoto se produce de la misma forma que si no hubiera servicios de cuarentena. El inconveniente de esta configuración es que el servidor de acceso remoto concede acceso normal a la red al cliente de acceso remoto durante el tiempo de espera de la sesión de cuarentena, aunque no cumpla las directivas de la red. Esta situación presenta una carencia de seguridad evidente.
  
#### Uso de la notificación inmediata
  
En esta configuración, la secuencia de comandos de cuarentena ejecuta RQC.exe para enviar la notificación antes de completar ninguna de las comprobaciones. El servidor de acceso remoto levanta las restricciones de la cuarentena de la conexión, y el cliente de acceso remoto dispone de acceso normal inmediato. En la secuencia de comandos de cuarentena, se siguen ejecutando las comprobaciones de cumplimiento de la directiva de la red. Si cualquiera de las comprobaciones no se supera correctamente, la secuencia de comandos de cuarentena notifica al usuario las acciones correctivas que se necesitan y lo desconecta automáticamente transcurrido un período de tiempo concreto, emulando el modo de cuarentena y el uso de un temporizador de la sesión de cuarentena.
  
**Nota:** en esta configuración, se configuran igualmente los atributos MS-Quarantine-Session-Timeout o MS-Quarantine-IPFilter para proporcionar las restricciones de cuarentena necesarias cuando el equipo tiene un paquete de Connection Manager o una secuencia de comandos que no se ha actualizado.
  
La ventaja de la notificación inmediata es que no se producen problemas de retraso en las aplicaciones. El acceso remoto se produce de la misma forma que si no hubiera servicios de cuarentena. No obstante, no se recomienda este enfoque.
  
#### Aplicación de los procedimientos recomendados
  
En esta sección se proporcionan algunos procedimientos recomendados fundamentales para la solución de Woodgrove. Estas recomendaciones incluyen:
  
-   Uso de una directiva de cuarentena de bloqueo de la totalidad del tráfico.
  
-   Posibilidad de inicio de sesión mediante una conexión de acceso telefónico.
  
-   Uso de acciones personalizadas antes del túnel para las comprobaciones de seguridad obligatorias.
  
-   Inclusión de software con licencia en el paquete del cliente.
  
#### Uso de una directiva de cuarentena de bloqueo de la totalidad del tráfico
  
Al conectar, el servidor DHCP asigna al cliente una dirección IP. El componente de notificación del cliente (RQC.exe) intenta pasar la clave compartida al componente de escucha del servidor (RQS.exe) del servidor de acceso remoto. RQS escucha únicamente en la dirección IP interna del servidor de acceso remoto. Ésta es la única dirección IP donde la directiva de cuarentena debe permitir la comunicación. El filtro IP debe bloquear todo el tráfico restante hasta que el RQS reciba la clave compartida correcta del RQC y el servidor de acceso remoto levante las restricciones de la cuarentena.
  
#### Posibilidad de inicio de sesión mediante una conexión de acceso telefónico
  
Cuando los usuarios seleccionan la opción de inicio de sesión de Windows **Iniciar sesión mediante una conexión de acceso telefónico**, los clientes de la red privada virtual (VPN) pueden recibir la actualización de la Directiva de grupo prácticamente de la misma manera que los clientes de la red de área local (LAN). Esta configuración proporciona una administración unificada de los clientes internos y remotos.
  
**Nota: **no existe ningún método disponible que permita aplicar secuencias de comandos de inicio y asignaciones de software informático a través de una conexión de acceso telefónico.
  
El uso de esta opción permite a los usuarios recibir notificaciones de la caducidad de su contraseña y permite que los equipos actualicen sus cuentas cuando se necesita. Debido a que la configuración de la Directiva de grupo se aplica a los clientes remotos después del proceso de conexión, la primera acción después de la conexión en Connection Manager debe ser levantar la cuarentena de la VPN. Un retraso al levantar la cuarentena puede provocar errores en la actualización de la Directiva de grupo, la notificación de caducidad de la contraseña y la actualización de las cuentas de los equipos.
  
Puede garantizar que la configuración de la Directiva de grupo se aplique de igual forma a los clientes de la VPN y de la LAN deshabilitando la opción **Detección de vínculo de baja velocidad** al menos en un objeto de Directiva de grupo que se aplique a todos los clientes. La organización debe comprobar y evaluar exhaustivamente el impacto global de esta configuración antes de considerar su implementación. Únicamente se debe implementar esta opción si es absolutamente necesario. Para obtener más información sobre la configuración de la Directiva de grupo, consulte [Introduction to Group Policy in Windows Server 2003](http://www.microsoft.com/windowsserver2003/techinfo/overview/gpintro.mspx) (en inglés) en www.microsoft.com/windowsserver2003/techinfo/overview/gpintro.mspx.
  
Para obtener más información sobre la detección de vínculos de baja velocidad, consulte [Specifying Group Policy for Slow Link Detection](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/deployguide/en-us/dmebb_gpu_fvfu.asp) (en inglés) en www.microsoft.com/resources/documentation/WindowsServ/2003/all/deployguide/en-us/dmebb\_gpu\_fvfu.asp.
  
#### Uso de acciones personalizadas antes del túnel para las comprobaciones de seguridad obligatorias
  
Para evitar retrasos innecesarios en el modo de cuarentena, realice todas las comprobaciones de seguridad en acciones personalizadas antes del túnel. Si el cliente de acceso remoto procesa estas actualizaciones antes de la conexión, la experiencia del usuario es más positiva.
  
#### Inclusión de software con licencia en el paquete del cliente
  
La organización debe asegurarse de que el equipo remoto tenga todo el software con licencia que necesita para realizar la conexión. Este software se debe distribuir como parte del paquete de Connection Manager para reducir las llamadas al servicio de soporte y los problemas de configuración.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Implementación de la supervisión y la administración
  
Una solución de cuarentena de VPN debe permitir la asignación y la supervisión de alarmas y umbrales adecuados para supervisar el estado operativo de la solución. La solución debe posibilitar la supervisión de toda la red, de un activo en particular o de una lista de activos en tiempo real. La supervisión debe mostrar los indicadores necesarios para la organización encargada del soporte operativo. Si este requisito no se cumple, el departamento de seguridad no podrá determinar si la solución protege realmente las conexiones de acceso remoto.
  
#### Supervisión de las operaciones de cuarentena
  
En la sección siguiente se proporcionan algunas consideraciones adicionales para la supervisión de las operaciones de cuarentena de VPN. Éstas incluyen:
  
-   Garantizar una cooperación estrecha entre los diversos equipos distribuidos en distintas zonas horarias al analizar y solucionar los problemas de los clientes remotos en las organizaciones de gran tamaño. La realización de pruebas rigurosas y una adecuada implantación piloto contribuyen a reducir los requisitos de solución de problemas.
  
-   Comprender plenamente los casos de acceso remoto, las amenazas para la seguridad y la manera de lograr el equilibrio entre ambos. Los directivos deben clasificar según su prioridad los activos que más protección necesitan y determinar el equilibrio apropiado entre costos y riesgos.
  
-   Anticiparse a los desafíos técnicos, como las rutinas de instalación y la distribución de CD. Debe tenerse en cuenta la necesidad de herramientas de administración empresarial adicionales en el proceso de planeamiento.
  
-   Supervisar y administrar los posibles problemas de rendimiento y establecer de antemano las expectativas de los usuarios. Por ejemplo, los usuarios remotos que últimamente no han iniciado sesión en la red mediante el acceso remoto pueden experimentar tiempos de inicio de sesión prolongados si utilizan la opción de inicio de sesión de Windows. Si el cliente necesita un Service Pack, pueden tardarse varias horas para iniciar la sesión según la velocidad de conexión del cliente. El equipo de TI de Woodgrove puede evitar este retraso enviando un mensaje de correo electrónico al usuario y dándole la posibilidad de enviarle un CD o utilizar un sitio de descarga.
  
-   Realizar la actualización a la tecnología más reciente al comienzo del diseño del proyecto global para los equipos cliente y servidor. De este modo se proporciona la plataforma básica de la solución y se elimina la mayoría de las variables causantes de problemas que pueden surgir en la organización durante la implementación de la solución. Gracias a este esfuerzo, debe aumentar la estabilidad del servicio y reducirse el costo del soporte técnico a los usuarios.
  
-   Implementar el proyecto en varias fases, dejando el tiempo suficiente entre ellas para su adopción por parte de los usuarios, la estabilización del sistema y de los procesos de la red, y el ajuste. La superposición de fases puede afectar negativamente a los usuarios del servicio. Además, pueden proliferar las dificultades con la identificación y el aislamiento de problemas en el servicio.
  
-   Recuerde que los equipos domésticos de los empleados no son propiedad de la empresa y que no los administra el departamento de TI. Si un empleado no desea o no puede instalar la solución de software y hardware exigida para poder tener acceso remoto desde ese equipo, existen otras opciones disponibles. Por ejemplo, Microsoft Outlook® Web Access proporciona una alternativa segura de ámbito mundial que permite a los empleados utilizar conexiones cifradas a sus datos personales (correo electrónico, contactos, tareas y funciones del calendario) y a las carpetas públicas de Microsoft Exchange Server 2003.
  
#### Ampliación de la solución
  
La solución de cuarentena de VPN no evita que alguien robe las credenciales de un usuario e intente iniciar una sesión en la red. Para reducir la probabilidad de que suceda algo así, considere cómo ampliar la solución para utilizar los certificados digitales contenidos en las tarjetas inteligentes.
  
El uso de mecanismos de autenticación de dos factores, como las tarjetas inteligentes, para autenticar las conexiones remotas aumenta la seguridad de la red y permite, al mismo tiempo, que los empleados adicionales se beneficien de la posibilidad de trabajar desde ubicaciones remotas. Para implementar tarjetas inteligentes se necesita el protocolo EAP-TLS (Protocolo de autenticación extensible-Seguridad de la capa de transporte).
  
Woodgrove National Bank ya cuenta con una infraestructura de claves públicas (PKI) madura y, por consiguiente, podría ampliar la solución de acceso remoto e incluir las tarjetas inteligentes. Para obtener más información sobre el planeamiento de la autenticación de dos factores, consulte la [Guía de planeamiento de acceso seguro con tarjetas inteligentes](http://go.microsoft.com/fwlink/?linkid=41313) en http://go.microsoft.com/fwlink/?LinkId=41313.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Las nuevas características de Windows Server 2003 con SP1 permiten a las organizaciones implementar los servicios de cuarentena de VPN de una manera confiable y totalmente compatible. Es esencial un planeamiento adecuado de la ejecución del proyecto de servicios de cuarentena de VPN, para evitar interrupciones innecesarias del servicio prestado a los usuarios remotos. En esta guía se estudian los factores y los procesos que deben tenerse en cuenta al planear una implementación de servicios de cuarentena de VPN y se describe cómo ha implementado esta solución la entidad financiera Woodgrove National Bank para su red. Para obtener más información sobre cómo implementar servicios de cuarentena de VPN, consulte el apéndice C, "Vínculos relacionados", de este mismo documento.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Apéndice A: Ejemplos de secuencias de comandos de servicios de cuarentena
  
[](#ecja)[Ejemplos de secuencias de comandos de servicios de cuarentena](#ecja)  
[](#ebaak)[Componentes de acceso remoto](#ebaak)  
[](#eaaaj)[Inicio de la secuencia de comandos de actualización de Windows](#eaaaj)
  
### Ejemplos de secuencias de comandos de servicios de cuarentena
  
En la sección siguiente se describen algunos ejemplos de secuencias de comandos disponibles para su descarga en el sitio Web de Microsoft. Las secuencias de comandos se incluyen en un archivo ejecutable autoextraíble denominado VPN Quarantine Sample Scripts.exe. Este archivo contiene un archivo léame.txt y documentación adicional para cada secuencia de comandos.
  
Para obtener más información sobre las secuencias de comandos para servicios de cuarentena de red privada virtual (VPN), consulte [VPN Quarantine Sample Scripts for Verifying Client Health Configurations](http://www.microsoft.com/downloads/details.aspx?familyid=a290f2ee-0b55-491e-bc4c-8161671b2462&displaylang=en) (en inglés) en www.microsoft.com/downloads/details.aspx?FamilyID=a290f2ee-0b55-491e-bc4c-8161671b2462&displaylang=en
  
Estas secuencias de comandos son ejemplos y es posible que deba modificarlos antes de aplicarlos al entorno de su empresa. En la tabla siguiente se muestran las secuencias de comandos y se describe su finalidad.
  
**Tabla A.1: Ejemplos de secuencias de comandos para servicios de cuarentena**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre de la secuencia de comandos</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Qsamples.cmd</td>
<td style="border:1px solid black;">Se trata del archivo de nivel superior al que se llama como acción posterior a la conexión desde el perfil de Connection Manager y que inicia las demás secuencias de comandos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">AV.Bat</td>
<td style="border:1px solid black;">Comprueba si el software antivirus del cliente es la versión más reciente e incluye los archivos de firmas de virus más actuales. Esta secuencia de comandos únicamente valida el software antivirus eTrust. Póngase en contacto con su proveedor para obtener ayuda sobre cómo desarrollar una secuencia de comandos parecida para los demás paquetes de software antivirus.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">CheckHotFixes.vbs</td>
<td style="border:1px solid black;">Comprueba si se han realizado las actualizaciones críticas en el equipo cliente. El administrador debe facilitar una lista de actualizaciones obligatorias.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ICS.vbs</td>
<td style="border:1px solid black;">Comprueba si existe una Conexión compartida a Internet y la deshabilita, si fuese necesario.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Passwd.vbs</td>
<td style="border:1px solid black;">Comprueba si la contraseña cumple la directiva de la empresa.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">ScrSaver.vbs</td>
<td style="border:1px solid black;">Comprueba la configuración de salvapantallas del usuario actual y se asegura de que esté habilitada y protegida mediante contraseña.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">WF.vbs</td>
<td style="border:1px solid black;">Comprueba si existe el servidor de seguridad Windows Firewall en todas las interfaces de red y lo activa, si fuera necesario.</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Componentes de acceso remoto
  
En la sección siguiente se describe la sintaxis de dos componentes de servicios de cuarentena de acceso remoto.
  
#### Servicio de agente de cuarentena de acceso remoto (RQS)
  
Para iniciar el servicio de agente de cuarentena de acceso remoto, escriba lo siguiente en la línea de comandos:
  
```  
Net start rqs  
```  
Para detener el servicio de agente de cuarentena de acceso remoto, escriba lo siguiente en la línea de comandos:
  
```  
Net stop rqs  
```  
#### Sintaxis de agente cliente de cuarentena de acceso remoto (RQC)
  
RQC tiene la sintaxis siguiente:
  
```  
rqc ConnName TunnelConnName Port Domain UserName String  
```  
En la tabla siguiente se muestran los parámetros del agente cliente de cuarentena de acceso remoto y su descripción.
  
**Tabla A.2 Parámetros del agente RQC**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Parámetro</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>ConnName</strong></td>
<td style="border:1px solid black;">Especifica el nombre de la conexión al servidor de acceso remoto en el host. El valor de este parámetro puede heredarse de la variable %DialRasEntry% del perfil de Connection Manager.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>TunnelConnName</strong></td>
<td style="border:1px solid black;">Especifica el nombre de la conexión de túnel al servidor de acceso remoto en el host. El valor de este parámetro se puede heredar de la variable %TunnelRasEntry% del perfil de Connection Manager.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Port</strong></td>
<td style="border:1px solid black;">Especifica el puerto al que se envía la cadena de cuarentena. El puerto predeterminado utilizado por el agente de cuarentena de acceso remoto (RQS) en el servidor de acceso remoto es el puerto TCP 7250. Sólo debe especificar un número de puerto distinto para RQC si RQS utiliza un número de puerto diferente.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Domain</strong></td>
<td style="border:1px solid black;">Especifica el dominio del usuario que se conecta. El valor de este parámetro se puede heredar de la variable %Domain% del perfil de Connection Manager.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>UserName</strong></td>
<td style="border:1px solid black;">Especifica el nombre de usuario del usuario que se conecta. El valor de este parámetro se puede heredar de la variable %UserName% del perfil de Connection Manager.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>String</strong></td>
<td style="border:1px solid black;">Especifica una cadena de texto que contiene la versión de la secuencia de comandos creada por el administrador. Se admiten todos los caracteres excepto la secuencia de caracteres /0.</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Inicio de la secuencia de comandos de actualización de Windows
  
El código siguiente se utiliza con la secuencia de comandos CheckHotFixes.vbs para guiar al usuario al sitio Web de Microsoft® Windows® Update, donde podrá instalar las últimas actualizaciones de seguridad:
  
```  
Prog = """C:\\Archivos de programa\\Internet Explorer\\iexplore.exe""" WUSite= " http://windowsupdate.microsoft.com" Set WshShell = CreateObject("Wscript.Shell") WshShell.Run(prog & WUsite),1,TRUE  
```  
[](#mainsection)[Principio de la página](#mainsection)
  
### Apéndice B: Parámetros del servicio de cuarentena de acceso remoto
  
La instalación del servicio de cuarentena de acceso remoto crea varias entradas en el Registro, que le permiten modificar los elementos que se muestran a continuación.   
  
**Nota:** Si utiliza de manera incorrecta el Editor del Registro podría provocar problemas graves que podrían obligarle a reinstalar el sistema operativo. Microsoft no puede garantizar que usted sea capaz de resolver los problemas que pueden derivarse de un uso indebido del Editor del Registro. El uso que haga del Editor del Registro será bajo su propia responsabilidad.
  
La ruta de acceso completa para configurar los parámetros del Registro es:
  
HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\rqs
  
Los parámetros que puede configurar son:
  
-   **AllowedSet**. El parámetro AllowedSet permite establecer la versión de la secuencia de comandos aceptada por el servidor de servicios de cuarentena de VPN de acceso remoto.
  
    ```  
AllowedSet, REG\_MULTI\_SZ  
```
  
La lista de cadenas que el servicio aceptará para quitar la cuarentena es:
  
-   **Port (REG\_DWORD)**. El parámetro Port especifica el puerto TCP en que el servicio RQS escuchará. Se utiliza 7250 si no se especifica ningún puerto.
  
-   **Authenticator (REG\_SZ)**. Especifica el módulo al que se llamará para quitar la cuarentena; el valor predeterminado es mprapi.dll.
  
    Si crea un archivo DLL personalizado para implementar la retirada de la funcionalidad de filtro del servicio de cuarentena, debe exponer la función siguiente:
  
    ```  
DWORD MprAdminConnectionRemoveQuarantine (HANDLE hRasServer,  HANDLE hRasConnection,  BOOL fIsIpAddress)  
```
  
<!-- -->
  
-   **Validator (REG\_SZ)**. Especifica el módulo que comprueba si la cadena de firma enviada por RQC es aceptable o no. De manera predeterminada, RQS.exe comparará las cadenas de AllowedSet. El archivo DLL de autenticación personalizado deberá exponer la siguiente función:
  
    ```  
BOOL ClientAuthenticate(LPCWSTR lpwsString).   
```
  
    Donde lpwsString contiene la cadena que hay que autenticar.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Apéndice C: Vínculos relacionados
  
[](#efaaz)[Red privada virtual](#efaaz)  
[](#eeaax)[Control de cuarentena](#eeaax)  
[](#edaal)[Servicio de autenticación de Internet](#edaal)  
[](#ecaam)[Sistema de nombres de dominio](#ecaam)  
[](#ebaan)[Connection Manager](#ebaan)  
[](#eaaao)[Windows Server 2003](#eaaao)
  
### Red privada virtual
  
Para obtener más información sobre las redes privadas virtuales, consulte [Virtual Private Networks with Windows Server 2003](http://www.microsoft.com/windowsserver2003/technologies/networking/vpn/default.mspx) (en inglés) en el sitio Web www.microsoft.com/vpn.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Control de cuarentena
  
Para obtener más información sobre cómo planear una solución de servicio de cuarentena de acceso a la red, consulte [Planning for Network Access Quarantine Control](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/deployguide/en-us/dnsbf_vpn_aosh.asp) (en inglés) en www.microsoft.com/resources/documentation/WindowsServ/2003/all/deployguide/en-us/dnsbf\_vpn\_aosh.asp.
  
Para obtener más información sobre cómo utilizar una solución de cuarentena de acceso a la red, consulte [Using Network Access Quarantine Control](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/deployguide/en-us/dnsbk_ias_rbpk.asp) (en inglés) en www.microsoft.com/resources/documentation/WindowsServ/2003/all/deployguide/en-us/dnsbk\_ias\_rbpk.asp.
  
Para obtener más información sobre cómo establecer un servicio de cuarentena en la red, consulte [Step-by-Step Guide for Setting Up Network Quarantine and Remote Access Certificate Provisioning in a Test Lab](http://www.microsoft.com/downloads/details.aspx?familyid=fe902704-52dd-4bbe-8a75-f8fbb76cd28a&displaylang=en) (en inglés) en www.microsoft.com/downloads/details.aspx?FamilyID=fe902704-52dd-4bbe-8a75-f8fbb76cd28a&DisplayLang=en.
  
Para obtener más información sobre la característica de control de cuarentena de acceso a la red de Microsoft Windows Server™ 2003, consulte [Network Access Quarantine Control in Windows Server 2003](http://www.microsoft.com/windowsserver2003/techinfo/overview/quarantine.mspx) (en inglés) en www.microsoft.com/windowsserver2003/techinfo/overview/quarantine.mspx.
  
Para obtener más información sobre cómo configurar el control de cuarentena de acceso a la red, consulte [Configuring Network Access Quarantine Control](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/deployguide/en-us/dnsbf_vpn_myfb.asp) (en inglés) en www.microsoft.com/resources/documentation/WindowsServ/2003/all/deployguide/en-us/dnsbf\_vpn\_myfb.asp.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Servicio de autenticación de Internet
  
Para obtener más información sobre IAS, consulte [Internet Authentication Service](http://www.microsoft.com/windowsserver2003/technologies/ias/default.mspx) (en inglés) en el sitio Web http://www.microsoft.com/ias.
  
Para obtener más información sobre cómo implementar IAS, consulte [Deploying Network Services](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/depkit/119050c9-7c4d-4cbf-8f38-97c45e4d01ef.mspx) (en inglés) en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/DepKit/119050c9-7c4d-4cbf-8f38-97c45e4d01ef.mspx.
  
Para obtener más información sobre IAS y el control de cuarentena de acceso a la red, consulte [IAS Network Access Quarantine Control](http://www.microsoft.com/resources/documentation/windowsserv/2003/standard/proddocs/en-us/sag_rap_quarantine_network.asp) (en inglés) en www.microsoft.com/resources/documentation/WindowsServ/2003/standard/proddocs/en-us/sag\_rap\_quarantine\_network.asp.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Sistema de nombres de dominio
  
Para obtener más información sobre cómo implementar el sistema de nombres de dominio (DNS), consulte [Deploying DNS](http://www.microsoft.com/resources/documentation/windowsserv/2003/standard/proddocs/en-us/sag_dns_imp_planningnode.asp) (en inglés) en www.microsoft.com/resources/documentation/WindowsServ/2003/standard/proddocs/en-us/sag\_DNS\_imp\_PlanningNode.asp.
  
Para obtener más información sobre DNS, consulte [Overview of DNS Deployment](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/deployguide/en-us/dnsbd_dns_mmdr.asp) (en inglés) en www.microsoft.com/resources/documentation/WindowsServ/2003/all/deployguide/en-us//dnsbd\_dns\_mmdr.asp.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Connection Manager
  
Para obtener más información sobre Connection Manager, consulte [What Is Connection Manager?](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/techref/en-us/w2k3tr_cm_what.asp) (en inglés) en www.microsoft.com/resources/documentation/WindowsServ/2003/all/techref/en-us//w2k3tr\_cm\_what.asp.
  
Para obtener más información sobre el funcionamiento de Connection Manager, consulte [How Connection Manager Works](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/techref/en-us/w2k3tr_cm_how.asp) (en inglés) en www.microsoft.com/resources/documentation/WindowsServ/2003/all/techref/en-us/w2k3tr\_cm\_how.asp.
  
Para obtener más información sobre cómo utilizar Connection Manager para implementar clientes de acceso remoto, consulte [Deploying Remote Access Clients Using Connection Manager](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/deployguide/en-us/dnsbg_rac_overview.asp) (en inglés) en www.microsoft.com/resources/documentation/WindowsServ/2003/all/deployguide/en-us/dnsbg\_rac\_overview.asp.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Windows Server 2003
  
Para obtener la información más actualizada sobre Microsoft® Windows Server™ 2003, consulte el [sitio Web de Windows Server 2003](http://www.microsoft.com/windowsserver2003) en http://www.microsoft.com/windowsserver2003.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Agradecimientos
  
El grupo Microsoft Solutions for Security (MSS) y Security Center of Excellence (SCoE) desean agradecer y reconocer la labor realizada por el equipo que elaboró la *Guía de planeamiento de la implementación de servicios de cuarentena con red privada virtual (VPN) de Microsoft*. Las personas que se citan a continuación fueron responsables directos o contribuyeron de forma decisiva en la redacción, desarrollo y comprobación de esta solución.
  
El grupo Microsoft Solutions for Security (MSS) y Security Center of Excellence (SCoE) desean agradecer y reconocer la labor realizada por el equipo que elaboró la *Guía de planeamiento de la implementación de servicios de cuarentena con red privada virtual (VPN) de Microsoft*. Las personas que se citan a continuación fueron responsables directos o contribuyeron de forma decisiva en la redacción, desarrollo y comprobación de esta solución.
  
### Autores
  
Anthony Steven, *Content Master*
  
Terry Tull, *Content Master*
  
Lee Walker
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Revisores
  
Chase Carpenter
  
Santosh Chandwani
  
Charles Denny
  
Kurt Dillard
  
Karl Grunwald
  
John Hawkins
  
Greg Lenti
  
Elliot Lewis
  
Claudio Vacalebre
  
Didier Vandenbroeck
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Evaluadores
  
Ashish Java, *Infosys Technologies*
  
Mehul Mediwala, *Infosys Technologies*
  
Gaurav Singh Bora, *Infosys Technologies*
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Editores
  
Deborah Jay, *Content Master*
  
Jennifer Kerns, *Content Master*
  
Frank Manning, *Volt*
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Directores del programa
  
Neil Bufton, *Content Master*
  
Chase Carpenter
  
Alison Woolford, *Content Master*
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Administrador de versiones
  
Flicka Crandell
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Colaboradores
  
Tony Bailey
  
Krishna Bhardwaj, *Vidyatech Solutions*
  
Prabish Chandran, *Vidyatech Solutions*
  
Christine Duell, *Valente Solutions*
  
Amy Frampton
  
Michael Glass, *Volt*
  
Joanne Kennedy
  
Karina Larson, *Volt*
  
Chrissy Lewis, *Siemens*
  
Vivek Manohar Prabhu, *Vidyatech Solutions*
  
Don McGowan
  
Bivin Pachatt, *Vidyatech Solutions*
  
Tessa Porterfield
  
Stacey Tsurusaki, *Volt*
  
David Visintainer, *Volt*
  
Vikas Walia, *Vidyatech Solutions*
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Descargar
  
[Guía de planeamiento de la implementación de servicios de cuarentena con red privada virtual (VPN) de Microsoft](http://go.microsoft.com/fwlink/?linkid=41308)
  
[](#mainsection)[Principio de la página](#mainsection)
