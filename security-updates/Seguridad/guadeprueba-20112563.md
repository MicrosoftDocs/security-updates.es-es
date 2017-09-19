---
TOCTitle: Guía de prueba
Title: Guía de prueba
ms:assetid: '29c9e543-4dec-46f9-8d02-5ce78a690576'
ms:contentKeyID: 20112563
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd458741(v=TechNet.10)'
---

Capítulo 13: Guía de prueba
===========================

Publicado: octubre 11, 2004 | Actualizado: 24/11/04

##### En esta página

[](#ehaa)[Introducción](#ehaa)
[](#egaa)[Ámbito de la prueba](#egaa)
[](#efaa)[Objetivos de la prueba](#efaa)
[](#eeaa)[Estrategia de la prueba](#eeaa)
[](#edaa)[Herramientas de la prueba](#edaa)
[](#ecaa)[Casos de prueba](#ecaa)
[](#ebaa)[Criterios para el lanzamiento](#ebaa)
[](#eaaa)[Información adicional](#eaaa)

### Introducción

Esta guía de prueba le servirá de ayuda a la hora de comprobar que la implementación en su empresa de la solución *Seguridad de LAN inalámbricas con Servicios de Certificate Server* funciona tal como se esperaba. El equipo de pruebas de soluciones de seguridad de Microsoft (MSS, Microsoft Solutions for Security) desarrolló y utilizó la información orientativa en este capítulo como parte de las pruebas internas relacionadas con la solución. Esta información describe el ámbito de las pruebas, sus objetivos y la estrategia utilizada, el entorno de laboratorio y las herramientas de que se hizo uso, así como los casos de prueba. Finalmente, ofrece un informe de los resultados obtenidos en la pruebas llevadas a cabo en los laboratorios de Microsoft.

#### Finalidad de este documento

Este capítulo se propone suministrarle una estructura de pruebas lista para su uso que podrá utilizar para probar la implementación de la solución en su entorno. Tras realizar los casos de prueba satisfactoriamente contará con garantías de que la solución implementada, tanto en el laboratorio de pruebas como en el entorno de producción, funcionará como se espera.

[](#mainsection)[Principio de la página](#mainsection)

### Ámbito de la prueba

La solución probada se basa en el perfil de empresa ficticio descrito en el capítulo 3, Arquitectura de la solución de LAN inalámbrica segura.

#### Dentro del ámbito

El equipo de la prueba ha realizado diferentes tipos de prueba para validar la solución. En cada fase se probaron diferentes combinaciones de estas pruebas. Los tipos fueron los siguientes:

-   Pruebas de línea base

-   Pruebas funcionales

-   Pruebas operativas

Estas pruebas se describen en la sección Casos de prueba, incluida más adelante en este capítulo.

El equipo efectuó estos tres tipos de pruebas en los componentes siguientes, tal como se utilizaron en la solución:

-   PKI, que incluye:

    -   Entidad emisora de certificados (CA) raíz

    -   Entidad emisora de certificados

-   Servicio de autenticación de Internet (IAS) de Microsoft

-   clientes inalámbricos:

    -   Microsoft® Windows® XP Professional con Service Pack 1 (SP1).

    -   Windows XP Tablet PC Edition con SP1.

Además, las pruebas se utilizaron para comprobar que tras la instalación de cada componente, los clientes podían acceder a los servicios siguientes con el mismo nivel de funcionalidad que antes: Las pruebas se diseñaron para mostrar la regresión en funcionalidad debido a la introducción de cualquiera de los componentes de la solución enumerados anteriormente o como consecuencia de modificaciones llevadas a cabo en dichos componentes durante el proceso de configuración:

-   Conectividad a la red

-   Controlador de dominio

-   configuración de IP: protocolo de configuración dinámica de host (DHCP, Dynamic Host Configuration Protocol).

-   servicios de resolución de nombres: sistema de nombres de dominio (DNS, Domain Name System).

-   servicios de archivos: servidor de archivos.

-   servicios Web: servicios de Internet Information Server (IIS, Internet Information Services).

-   servicios de correo electrónico: Microsoft Exchange 2000.

-   Acceso a red inalámbrica

#### Fuera del ámbito

Los siguientes aspectos quedaron excluidos del ámbito de las pruebas:

-   prueba de infiltración y evaluación de vulnerabilidad de la solución, llevadas a cabo por una consultoría de seguridad comercial.

-   integración con una infraestructura de claves públicas (PKI, Public Key Infrastructure) de otra organización.

-   pruebas extensas de las siguientes funciones de servidor (aparte de las necesarias para comprobar el comportamiento correcto de la solución):

    -   controlador de dominio, DHCP y DNS.

    -   Exchange Server 2000

    -   servidor Web y servidor de archivos e impresión.

    -   Microsoft Operations Manager (MOM)

-   pruebas extensas de los servicios de cliente siguientes (una vez más, éstos se utilizaron para comprobar la funcionalidad de la solución):

    -   DNS y DHCP

    -   Archivo

    -   Web

    -   correo electrónico.

-   los clientes con el software siguiente quedaron excluidos del ámbito de las pruebas:

    -   Windows 2000 Professional.

    -   Pocket PC con Windows CE.

    -   Microsoft Windows NT® 4.0.

    -   Windows 9*x*.

    -   Clientes que no usan Windows.

[](#mainsection)[Principio de la página](#mainsection)

### Objetivos de la prueba

Los objetivos de la prueba han sido comprobar lo siguiente:

1.  La totalidad de la información orientativa de la solución debía ser clara, completa y técnicamente correcta.

2.  La solución debía proporcionar una red de LAN inalámbrica (WLAN) segura mediante servicios de Certificate Server sin efectos negativos en ningún aspecto de la funcionalidad, rendimiento y directiva de seguridad de la infraestructura existente.

3.  La implementación de la solución debía ser un proceso sencillo. Los profesionales de TI que cuentan con la certificación MCSE (Microsoft Certified Systems Engineer) para Windows 2000 (o Server 2003) o disponen de un nivel de conocimientos equivalente y están familiarizados con los servicios de Certificate Server e IAS deberían poder usar esta información sin ningún tipo de problemas.

[](#mainsection)[Principio de la página](#mainsection)

### Estrategia de la prueba

Para conseguir los objetivos, el equipo desarrolló un laboratorio de pruebas basado en Woodgrove Bank, una organización ficticia de 15000 usuarios. El entorno del laboratorio de pruebas se describe más adelante en este capítulo. Las pruebas incluyeron las fases siguientes:

-   como parte del proceso de desarrollo, la solución se probó como unidad.

-   prueba del sistema, ciclo 1.

-   prueba del sistema, ciclo 2.

-   pruebas de regresión del sistema.

En las pruebas, los servidores básicos de la infraestructura incluyeron las funciones siguientes (algunas de estas funciones se combinaron en un solo servidor):

-   controlador de dominio, DHCP y DNS.

-   servidor Web y servidor de archivos e impresión.

-   servidor de correo electrónico Microsoft Exchange Server.

-   servidor de acceso a Web Microsoft Outlook®.

-   controlador de dominio de Active Directory®.

Estos servicios se comprobaron mediante la realización de pruebas de línea base previas a la implementación de los componentes de la solución. Se crearon copias de seguridad de imagen de cada servidor en la infraestructura para su uso durante el segundo ciclo de las pruebas. La prueba de regresión utilizó la misma infraestructura que el segundo ciclo de las pruebas.

Los ciclos 1 y 2 de las pruebas del sistema se dividieron, a su vez, en dos fases de generación incremental:

1.  fase de servicios de Certificate Server de PKI.

2.  fase de WLAN.

Encontrará una descripción detallada de estas dos fases más adelante en esta sección.

El equipo se ocupó del registro de errores relacionados con problemas importantes surgidos en una fase determinada. Los errores se resolvieron durante el desarrollo de dicha fase, antes de pasar a la siguiente. Esta estrategia ayudó al equipo de pruebas a resolver problemas graves rápidamente, lo que permite un ahorro de tiempo y recursos económicos considerable.

Además, la realización de las pruebas en varios ciclos garantizó que cualquier problema encontrado en el ciclo de prueba *N* quedase resuelto en el ciclo de prueba de regresión *N+1*, con lo que se consigue una solución de alta calidad. La solución era estable al final del tercer ciclo de prueba de regresión.

La figura siguiente representa el enfoque de prueba por fases utilizado en esta guía:

[![](images/Dd458741.13fig13-1(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458741.13fig13-1_big(es-es,technet.10).gif)

**Figura 13.1 Enfoque de prueba por fases de la solución**

#### Fases de la prueba

La prueba ha seguido un enfoque por fases lógico. Cada fase es incremental y consta de los pasos siguientes:

1.  Criterios de entrada: inicio de la fase

2.  Generación de componentes

3.  Diferentes tipos de pruebas realizadas en la generación

4.  Criterios de salida: fin de la fase

#### Fase de PKI

La ejecución satisfactoria de las pruebas de línea base en los servidores de la infraestructura constituye el criterio de entrada para esta fase. Los pasos implicados en esta primera fase son los siguientes:

1.  **Generación de PKI:** consiste en la implementación de los servicios de Certificate Server para la red. Ha implicado la instalación, generación y configuración de los servidores de entidad emisora raíz y entidad emisora. También ha sido el paso de Generación de componentes para la fase.

2.  **Ejecución de pruebas de línea base:** este paso garantiza que la configuración de los servicios de Certificate Server no interfiere con los servicios de cliente ni la infraestructura existente.

3.  **Ejecución de pruebas funcionales:** este paso garantiza que las entidades emisoras de certificados se han implementado correctamente en la red y se encuentran en un estado totalmente funcional.

4.  **Ejecución de pruebas de operaciones:** este paso garantiza que las entidades emisoras de certificados pueden administrarse y mantenerse mediante funciones administrativas apropiadas. Estas pruebas han comprobado los distintos procedimientos operativos de los componentes de los servicios de Certificate Server mencionados en Solution Guide.

La culminación satisfactoria de todas las pruebas mencionadas anteriormente constituye el criterio de salida para esta fase.

#### Fase de WLAN

La generación de la segunda fase incremental, la fase de WLAN, comienza tras la finalización satisfactoria de la fase de PKI. La instalación satisfactoria de la fase de PKI es el criterio de entrada para esta fase. El segundo paso tiene su inicio en la instalación de los servidores IAS. A continuación se lleva a cabo la configuración de los componentes de WLAN. Los pasos implicados en esta fase son:

1.  **Generación de IAS:** este paso consiste en la instalación y configuración de los servidores IAS en la red, tanto en la oficina central como en la sucursal, de acuerdo con las instrucciones de implementación de la solución.

2.  **Componentes de WLAN:** este paso se ocupa de la generación y configuración de los componentes de WLAN.

3.  **Clientes de WLAN:** en este paso se lleva a cabo la configuración de los clientes de WLAN.

4.  **Ejecución completa de pruebas de línea base:** por medio de este paso se verifica que no se han producido impactos negativos en los servicios de cliente ni en la infraestructura base.

5.  **Ejecución completa de pruebas funcionales:** este paso sirve para comprobar que la solución se ha generado e implementado satisfactoriamente. Incluye la comprobación de los servicios de acceso inalámbrico seguro a la red y el uso que éstos hacen de la PKI generada en la fase anterior.

6.  **Ejecución completa de pruebas de operaciones:** este paso garantiza que la red segura ya puede administrarse y mantenerse. Incluye la repetición de las pruebas operativas y administrativas en relación con los componentes de los servicios de Certificate Server.

La culminación satisfactoria de todas las pruebas mencionadas anteriormente constituye el criterio de salida para esta fase.

#### Entorno de prueba

El entorno de prueba se diseñó como un subconjunto funcional de los servicios de TI que utilizaría una organización como Woodgrove Bank. Todos los servicios básicos de la infraestructura requeridos por la solución se representaron en el entorno de laboratorio, que ofrecía una emulación de la oficina central y una sucursal más pequeña conectadas mediante una red de área amplia (WAN, Wide Area Network) enrutada. En el laboratorio se configuraron los servidores de infraestructura siguientes:

-   controlador de dominio, DHCP y DNS (para la oficina central y la sucursal).

-   Microsoft Exchange 2000 (en Windows Advanced Server 2000) en la oficina central.

-   servidor Web y servidor de archivos e impresión en la oficina central.

-   MOM en la oficina central.

Los servidores de la solución consistían de:

-   la entidad emisora raíz en la oficina central.

-   la entidad emisora en la oficina central.

-   servidores IAS principal y secundario en la oficina central y un servicio IAS secundario instalado en el controlador de dominio de la sucursal.

#### Hardware

Para la configuración de hardware de los equipos de servidor en el laboratorio de pruebas se tomaron como base los perfiles de hardware proporcionados en la guía de la solución, con la adición de lo siguiente:

-   clientes estándar de escritorio.

-   clientes estándar de equipo portátil.

-   clientes estándar de Tablet PC.

-   puntos de acceso (PA) inalámbrico con capacidad para 802.1X en la oficina central y en la sucursal.

-   equipos de escritorio para la simulación de WAN y enrutamiento.

-   Conmutador de nivel 3

#### Software

Microsoft Windows Server™ 2003 se utilizó como sistema operativo base en el laboratorio de pruebas para todas las funciones de servidor (excepto Microsoft Exchange 2000). Además, durante las pruebas, se utilizaron los siguientes componentes de software:

-   Windows 2000 Advanced Server con SP3

-   Windows Server 2003 Enterprise Edition.

-   Windows Server 2003 Standard Edition.

-   Exchange 2000 con SP3.

-   Windows XP Professional con SP1

-   Windows XP Professional con SP1 (versión para Tablet PC)

-   MOM 2000 con SP1

-   Microsoft SQL Server™ 2000 con SP3.

-   Outlook 2000 con SP1.

Para probar el acceso inalámbrico seguro, los clientes del laboratorio de pruebas han utilizado el siguiente sistema operativo.

-   Windows XP Professional con SP1

-   Windows XP Tablet PC Edition con SP1.

#### Diagrama de red

El diagrama incluido a continuación constituye un esquema detallado del entorno de pruebas.

[![](images/Dd458741.13fig13-2(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458741.13fig13-2_big(es-es,technet.10).gif)

**Figura 13.2 Diagrama de red del laboratorio de pruebas**

#### Configuraciones

La figura anterior muestra la red que se generó en el laboratorio de pruebas para simular el entorno de Woodgrove Bank. En este escenario, hay una red de oficina central que contiene la mayoría de los servidores de la solución y la infraestructura, y una red de sucursal que cuenta con un solo servidor que ejecuta los servicios de la solución e infraestructura. El equipo simulador de WAN suministra la latencia de red y la restricción de ancho de banda entre estas redes. La configuración del laboratorio de pruebas se mantuvo idéntica a la recomendada en la guía de la solución.

[](#mainsection)[Principio de la página](#mainsection)

### Herramientas de la prueba

Esta sección describe las distintas clases de herramientas utilizadas en la prueba de la solución. La mayoría están disponibles en el CD de instalación del sistema operativo. Alternativamente, pueden instalarse desde la carpeta de soporte técnico\\herramientas incluida en el CD de instalación de Windows Server 2003.

#### Software

Se han utilizado las siguientes herramientas durante la prueba:

-   Certutil: se trata de una herramienta de utilidades muy eficaz de los servicios de Certificate Server que puede utilizarse para la instalación, configuración y resolución de problemas de las entidades emisoras.

-   Certreq: sirve para solicitar certificados de entidades emisoras manualmente. Está disponible en el CD de instalación de Windows Server 2003.

-   Ldifde: sirve para importar y exportar información de Active Directory mediante archivos de formato de intercambio de datos de LDAP (LDIF, LDAP Data Interchange Format). Esta herramienta se utilizó en la solución para algunas operaciones relacionadas con plantillas de certificados.

-   Ntbackup: se usa para restaurar y hacer copias de seguridad de archivos, y está disponible en el CD de instalación de Windows Server 2003.

#### Supervisión del sistema

Durante las pruebas se utilizaron las siguientes herramientas de supervisión del sistema:

-   Dcdiag: analiza el estado de los controladores de dominio en un bosque de Active Directory e informa de los posibles problemas para ayudar a resolverlos.

-   Jetpack: se utiliza para comprobar la coherencia de la base de datos DHCP.

-   Agenthelper: utilidad de MOM que verifica la ejecución del servicio OnePoint en los agentes administrados por MOM.

-   PerfMon: permite ver los contadores, las alertas y los registros de rendimiento del sistema.

-   NetMon: captura y filtra las tramas del tráfico de red que entran y salen del equipo en el que está instalada la utilidad.

-   IASparse: interpreta los archivos de registro IAS y detalla los distintos parámetros del servicio de usuario de acceso telefónico de autenticación remota (RADIUS, Remote Authentication Dial-In User Service).

-   EventViewer: permite ver, filtrar y exportar los registros de supervisión del sistema, seguridad y aplicación de Windows.

-   MMC MOM: consola de administración de MOM que supervisa la información, las advertencias, las alertas, los errores y los registros de errores críticos para los agentes que administra el servidor MOM.

-   PKIHealth: herramienta muy útil para diagnosticar problemas del punto de distribución de las listas CRL (CDP, CRL Distribution Point) y del acceso a la información de entidad emisora (AIA, Authority Information Access) de todas las entidades emisoras de la empresa.

#### Secuencias de comandos personalizadas

Las secuencias de comandos siguientes se utilizaron durante las pruebas en distintas fases definidas por la solución:

-   ca\_setup.wsf: esta secuencia contiene los comandos de trabajo requeridos durante la configuración y la generación de los servicios de Certificate Server.

-   ca\_setup.vbs: esta secuencia contiene el código funcional para implementar los trabajos definidos en la secuencia de comandos ca\_setup.wsf.

-   ca\_monitor.wsf: esta secuencia contiene los comandos de trabajo requeridos para supervisar los servicios de las entidades emisoras.

-   ca\_monitor.vbs: esta secuencia contiene el código funcional para implementar los trabajos definidos en la secuencia de comandos ca\_monitor.wsf.

-   ca\_operations.wsf: esta secuencia contiene los comandos de trabajo requeridos para llevar a cabo las tareas operativas y de supervisión de los servicios de Certificate Server.

-   ca\_operations.vbs: esta secuencia contiene el código funcional para implementar los trabajos definidos en la secuencia de comandos ca\_operations.wsf.

-   constants.vbs: esta secuencia contiene los parámetros de constantes para los servicios de Certificate Server utilizados en otras secuencias de comandos.

-   helper.vbs: esta secuencia contiene las funciones básicas y las variables utilizadas por las secuencias de comandos relacionadas con Certificate, IAS y WLAN.

-   IASAccessPrep.txt: este archivo de texto contiene las filas de encabezado que se agregan a los archivos de registro de IAS para convertirlos en archivos de Microsoft Access.

-   IASClientExport.bat: este archivo por lotes vuelca la configuración de cliente RADIUS del servidor IAS en un archivo de configuración de texto de la unidad A:\\.

-   IASClientImport.bat: este archivo por lotes importa la configuración de cliente RADIUS de un archivo de configuración de texto de la unidad A:\\ al servidor IAS.

-   IASExport.bat: este archivo por lotes vuelca las configuraciones específicas de IAS en un archivo de configuración de texto.

-   IASImport.bat: este archivo por lotes importa configuraciones específicas de IAS de un archivo de configuración de texto en el servidor IAS.

-   ias\_tools.wsf: esta secuencia contiene los comandos de trabajo requeridos para configurar servidores IAS.

-   ias\_tools.vbs: esta secuencia contiene el código funcional para implementar los trabajos definidos en la secuencia de comandos ias\_tools.wsf.

-   IAS\_Data.bat: este archivo por lotes contiene un comando que se necesita durante la configuración de los servidores IAS para la solución.

-   pkiparms.vbs: esta secuencia contiene constantes específicas del usuario utilizadas durante la configuración de los servicios de Certificate Server.

-   wl\_tools.wsf: esta secuencia contiene los comandos de trabajo requeridos para configurar los componentes de WLAN.

-   wl\_tools.vbs: esta secuencia contiene el código funcional para implementar los trabajos definidos en la secuencia de comandos wl\_tools.wsf.

Todas las secuencias de comandos anteriores se incluyen en el paquete de descarga de la solución.

[](#mainsection)[Principio de la página](#mainsection)

### Casos de prueba

Esta sección detalla las pruebas utilizadas para comprobar la solución y garantizar la consecución de sus objetivos. Adicionalmente incluye los criterios para aprobar o suspender los casos de prueba. Los casos principales enumerados constituyen un pequeño subconjunto de la serie completa de casos de prueba. La lista completa de casos de prueba se proporciona en dos hojas de cálculo de Microsoft Excel incluidas con el paquete de descarga de la solución (consulte las referencias sobre estos archivos en la página siguiente).

Los escenarios en la lista a continuación se probaron una vez finalizada la creación del laboratorio de acuerdo con las instrucciones de la solución. Los equipos y usuarios del dominio se agregaron a los servicios de certificados y grupos de seguridad de acceso inalámbrico apropiados. Mediante una conexión por cable, los usuarios se conectaron a la red una sola vez, de modo que la directiva de grupo pudiera aplicarse correctamente a los equipos cliente inalámbricos.

Los escenarios principales siguientes se probaron en el laboratorio para validar la solución.

-   **Inscripción automática de certificados para usuario y equipo**: cuando el usuario inicia la sesión en el dominio por medio de una conexión por cable, la directiva de grupo se aplica al usuario y al equipo. La entidad emisora emite correctamente los certificados de autenticación de usuario y de equipo, que están disponibles en los almacenes de certificados personales del equipo y el perfil de usuario.

-   **Certificados de entidad emisora y emisora raíz en almacén raíz de confianza**: cuando el usuario inicia la sesión en el dominio mediante una conexión por cable, la directiva de grupo se aplica al usuario y al equipo. El complemento Certificados de MMC verifica los almacenes de certificados del equipo y el usuario. Se comprueba la presencia del certificado de entidad emisora raíz en la carpeta de entidades emisoras de certificados raíz de confianza. También se verifica la presencia de un certificado de entidad emisora bajo las entidades emisoras intermedias.

-   **Certificado de autenticación de servidor IAS**: los servidores IAS se reinician tras completar la generación y agregar estos servidores a las unidades organizativas (UO) y los grupos de seguridad adecuados (el reinicio es necesario para que los equipos puedan convertirse en miembros de grupos). Cada servidor IAS recibe un certificado de autenticación de servidor nuevo. La verificación de este proceso tiene lugar mediante el uso del complemento Certificados MMC para ver el almacén de certificados del equipo.

-   **Las listas CRL y los certificados de entidad emisora raíz y entidad emisora están disponibles en el servidor Web**: desde Internet Explorer en un equipo cliente se accede al directorio virtual de la PKI del servidor Web para verificar que el cliente puede ver los certificados de entidad emisora raíz y entidad emisora y las listas CRL. El resultado de la verificación debe coincidir con la ubicación HTTP configurada en el certificado del cliente en la ficha de **detalles**.

-   **Acceso inalámbrico a la red mediante certificados de autenticación**: cuando un usuario recibe los certificados nuevos y válidos de autenticación de equipo y usuario, se conecta la tarjeta de red inalámbrica y se elimina la conexión por cable. Tras el reinicio se produce la autenticación del equipo con la WLAN. La autenticación del equipo con la WLAN se verifica mediante la consulta del registro de sucesos del sistema del servidor IAS. Seguidamente, el usuario puede acceder al dominio a través de la WLAN. La autenticación del usuario con la WLAN se verifica por medio de una entrada en el registro de sucesos del sistema generada en el servidor IAS.

-   **Disponibilidad de servidor IAS para usuarios de sucursal**: en caso de que el servicio IAS de la sucursal no esté disponible, los usuarios pueden autenticarse en los servidores IAS de la oficina central. La configuración necesaria para esta prueba requiere que el servidor IAS de la oficina central haga las veces de servidor IAS secundario en los puntos de acceso inalámbrico de la sucursal. Seguidamente se desconecta el servicio IAS de la sucursal. Los usuarios aún pueden llevar a cabo la autenticación y conectar a la WLAN. La autenticación se confirma mediante la consulta de los sucesos de autenticación incluidos en el registro de sucesos del sistema del servidor IAS de la oficina central.

Los detalles sobre los diferentes tipos de casos de prueba ejecutados por el equipo de pruebas para comprobar la solución se describen en las secciones siguientes.

#### Pruebas de línea base

Estas pruebas validan los servicios de la infraestructura base. Incluyen pruebas básicas de funcionalidad de cliente y servidor a las que se hizo referencia durante el proceso de pruebas del sistema.

Desde la perspectiva del cliente, las pruebas de línea base incluyen pruebas de servicios de cliente básicos, como la autenticación en el dominio y el acceso a un servidor Web, de archivos y de correo electrónico. Las pruebas de línea base se repitieron después de cada fase de generación de la solución para verificar que al aplicar la configuración de la solución no se crearon problemas en la funcionalidad existente del entorno.

Desde la perspectiva de los servidores, estas pruebas verifican que los servidores funcionan correctamente y que no se producen impactos negativos en sus funciones como resultado de la implementación de los componentes de la solución.

Para obtener más información acerca de los casos de prueba utilizados durante la fase de pruebas de línea base, consulte el archivo Baseline Test Cases.xls que se incluye con la solución.

#### Pruebas funcionales

Estas pruebas se diseñaron para verificar que la solución podía generarse tal y como se describía en la documentación y ofrecería la funcionalidad esperada. Estos casos de pruebas funcionales incluyen la verificación de funciones, estado e interoperabilidad de los servicios y componentes WLAN, IAS y PKI, tal como recomienda la solución.

Para obtener más información acerca de los casos de prueba utilizados durante la fase de pruebas funcionales, consulte el archivo Functional & Operational Test Cases.xls que se incluye con la solución.

#### Pruebas operativas

Estas pruebas sirven para validar las operaciones, el mantenimiento y la capacidad de administración de los servidores de la solución. Estos factores se documentan en los procedimientos de administración de la guía de operaciones, en los capítulos 11, Administración de la infraestructura de claves públicas, y 12, Administración de la infraestructura de seguridad de RADIUS y LAN inalámbrica.

Para obtener más información acerca de los casos de prueba utilizados durante la fase de pruebas operativas, consulte el archivo Functional & Operational Test Cases.xls que se incluye con la solución.

[](#mainsection)[Principio de la página](#mainsection)

### Criterios para el lanzamiento

El lanzamiento principal de la solución está vinculado a la gravedad y la prioridad de errores sin resolver de acuerdo con los criterios siguientes:

-   no existen errores sin solucionar de Gravedad 1 o Gravedad 2.

-   no existen errores sin solucionar de Prioridad 1 o Prioridad 2 de ningún nivel de gravedad.

-   las guías de la solución no tienen comentarios ni revisiones pendientes.

-   el equipo líder trata todos los errores sin solucionar.

-   Todos los casos de prueba del entorno de laboratorio de prueba se han completado satisfactoriamente.

-   el contenido de la solución no contiene declaraciones conflictivas.

#### Clasificación de los errores

La tabla siguiente define los criterios de gravedad y prioridad de los errores utilizados en el laboratorio de pruebas.

**Tabla 13.1: Clasificación de errores**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Calificación</p></th>
<th><p>Definición de gravedad</p></th>
<th><p>Definición de prioridad</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>El error provoca el bloqueo del sistema o la pérdida de datos.</p></td>
<td style="border:1px solid black;"><p>El error debe corregirse lo antes posible. El error bloquea el progreso en esta área.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>2</p></td>
<td style="border:1px solid black;"><p>El error causa problemas graves en la funcionalidad u otros aspectos importantes; el producto se bloquea en casos poco claros.</p></td>
<td style="border:1px solid black;"><p>El error debe corregirse antes del lanzamiento del producto.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>3</p></td>
<td style="border:1px solid black;"><p>El error provoca problemas de menor importancia en la funcionalidad que pueden influir en la calidad.</p></td>
<td style="border:1px solid black;"><p>Si hay tiempo, el error debe corregirse; no es muy importante. Puede posponerse.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>4</p></td>
<td style="border:1px solid black;"><p>El error contiene fallos tipográficos, frases poco claras o mensajes de error en campos de visibilidad reducida.</p></td>
<td style="border:1px solid black;"><p>No está definido</p></td>
</tr>  
</tbody>  
</table>
  
#### Resultados de la prueba
  
Se obtuvieron resultados positivos de todos los casos de prueba. No hubo errores sin resolver de Gravedad 1 y 2 ni de un nivel de Prioridad 2 o superior. Esto demuestra la consecución de los objetivos de las pruebas, con lo que la solución está lista para el lanzamiento.
  
#### Información del diagnóstico
  
Las sugerencias siguientes han ayudado a solucionar problemas durante las pruebas:
  
-   Cree HKCU\\Software\\Microsoft\\Cryptography\\Autoenrollment\\AEEventLogLevel {**DWORD** establecido en **0**}. A continuación, la inscripción automática se registrará en el registro de sucesos de la aplicación. Cree la misma clave de registro en HKLM para la inscripción de equipos.
  
-   Asegúrese de que el secreto compartido del punto de acceso inalámbrico y el servidor IAS es el mismo y es correcto (utilice el proceso de copiar y pegar desde el archivo de secretos). De lo contrario, el punto de acceso no se autenticará en el servidor IAS como cliente RADIUS. Esto dará como resultado registros de error en el servidor IAS con uno de los mensajes siguientes:
  
    -   Autenticador no válido.
  
        - O bien -
  
    -   Atributo autenticador de mensaje no válido.
  
-   Si el servidor IAS genera un registro con el identificador de suceso 2 y la advertencia de que la autenticación no pudo llevarse a cabo porque se usó un nombre de usuario desconocido o una contraseña incorrecta, asegúrese de que la directiva de acceso remoto para redes inalámbricas está configurada adecuadamente en el servidor IAS. Compruebe también que el usuario se haya agregado a los grupos de seguridad inalámbrica apropiados.
  
-   Si el servidor IAS genera un registro con el identificador de suceso 2 y la advertencia de que el procesamiento de una de las cadenas de certificados se llevó a cabo correctamente pero el proveedor de la directiva no confía en uno de los certificados de la entidad emisora, compruebe que el certificado de servidor IAS y el certificado del usuario puedan validarse con el certificado de la entidad emisora actual. Asegúrese también de que los certificados de las entidades emisora y emisora raíz estén presentes en el almacén de certificados del usuario.
  
-   Si SCHANNEL genera un registro de advertencia con el identificador de suceso 36877 y la advertencia de que el certificado recibido de la aplicación cliente remota no se ha validado correctamente, El código de error es 0x80096004. Los datos adjuntos contienen el certificado de cliente. Asegúrese de que el certificado de autenticación inalámbrica del equipo y el usuario no se revocó o ha caducado.
  
-   Consulte las secciones dedicadas a la solución de problemas en la guía de operaciones si desea obtener información de diagnóstico adicional.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Información adicional
  
Puede encontrar más información sobre las pruebas en las guías de planeamiento, generación y operaciones de la solución. Adicionalmente, los vínculos siguientes ofrecen información de referencia muy útil para la solución de problemas durante las pruebas:
  
-   Para obtener información sobre solución de problemas de acceso inalámbrico IEEE 802.11 con Windows XP, consulte las notas del producto “[Troubleshooting Windows XP IEEE 802.11 Wireless Access](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/wifitrbl.mspx)” en http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/wifitrbl.mspx.
  
-   Si desea consultar información sobre la inscripción automática de certificados en Windows XP, consulte las notas del producto “[Certificate Autoenrollment in Windows XP](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/certenrl.mspx)” en http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/certenrl.mspx.
  
-   Para obtener detalles sobre mejoras de PKI, vea las notas del producto “[PKI Enhancements in Windows XP Professional and Windows Server 2003](http://www.microsoft.com/technet/prodtechnol/winxppro/plan/pkienh.mspx)” en http://www.microsoft.com/technet/prodtechnol/winxppro/plan/pkienh.mspx.
  
-   Para obtener una descripción general de los componentes y la tecnología de implementación inalámbrica en Windows XP, consulte el artículo “[Windows XP Wireless Deployment Technology and Component Overview](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/wificomp.mspx)” en http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/wificomp.mspx.
  
[](#mainsection)[Principio de la página](#mainsection)
