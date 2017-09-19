---
TOCTitle: Información general sobre la Guía de seguridad de Windows Server 2003
Title: Información general sobre la Guía de seguridad de Windows Server 2003
ms:assetid: '9911b568-c474-465f-998f-4f0fa31bebc6'
ms:contentKeyID: 20200265
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163140(v=TechNet.10)'
---

Guía de Seguridad de Windows Server 2003
========================================

### Información general

Actualizado: 27/12/05

La *Guía de seguridad de Windows Server 2003* proporciona recomendaciones específicas acerca de cómo reforzar la seguridad de los equipos que ejecutan Microsoft® Windows Server™ 2003 con Service Pack 1 (SP1) en tres entornos empresariales distintos: uno que debe ser compatible con sistemas operativos antiguos, como Windows NT® 4.0 y Windows® 98; otro en el que Windows 2000 es la versión más antigua del sistema operativo que se utiliza; y otro en el que la preocupación por la seguridad es tan importante que se considera aceptable una pérdida significativa de funcionalidad y capacidad de administración a cambio de lograr el máximo nivel de seguridad. Estos entornos se denominan respectivamente Cliente heredado (LC), Cliente de empresa (EC) y Seguridad especializada: Funcionalidad limitada (SSLF) en esta guía.

Se proporciona orientación sobre cómo reforzar la seguridad de los equipos en estos tres entornos para un grupo de diferentes funciones de servidor. Las contramedidas que se describen y las herramientas que se proporcionan asumen que cada servidor tendrá una sola función. Si necesita combinar funciones para algunos de los servidores en su entorno, puede personalizar las plantillas de seguridad que se incluyen en la versión descargable de la guía con el fin de crear la combinación apropiada de servicios y opciones de seguridad. Entre las funciones de servidor a las que se hace referencia en esta guía se incluyen las siguientes:

-   Controladores de dominio que también proporcionan servicios DNS

-   Servidores de infraestructura que ofrecen servicios WINS y DHCP

-   Servidores de archivos

-   Servidores de impresión

-   Servidores web que ejecutan los Servicios de Internet Information Server (IIS) de Microsoft.

-   Servidores IAS (Servicios de autenticación de Internet)

-   Servidores de Servicios de Certificate Server

-   Hosts de baluarte

Se han realizado muchos esfuerzos para que la información de esta guía se presente de forma organizada y resulte de fácil acceso con el fin de que pueda encontrar rápidamente la información que necesita y determinar qué configuración es la más adecuada para los equipos de su organización. Aunque esta guía está destinada a los clientes empresariales, gran parte de su contenido también resulta adecuado para organizaciones de cualquier tamaño.

Para sacar el máximo provecho de este material, debe leer la totalidad de la guía. Asimismo, es posible que desee consultar la guía complementaria, [Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP](http://go.microsoft.com/fwlink/?linkid=15159), que está disponible en http://go.microsoft.com/fwlink/?LinkId=15159.

##### En esta página

[](#eeaa)[Destinatarios de la guía](#eeaa)
[](#edaa)[Información general acerca de la guía](#edaa)
[](#ecaa)[Recursos relacionados](#ecaa)
[](#ebaa)[Comuníquenos su opinión](#ebaa)
[](#eaaa)[Servicios de consultoría y soporte técnico](#eaaa)

### Destinatarios de la guía

Esta guía está destinada principalmente a consultores, expertos en seguridad, arquitectos de sistemas y profesionales de TI responsables de las fases de planeamiento del desarrollo de las aplicaciones o la infraestructura y la implementación de Windows Server 2003. Esta guía no se ha diseñado para los usuarios domésticos.

Los expertos en seguridad y los arquitectos de TI pueden necesitar información más detallada acerca de las opciones de configuración de seguridad que se tratan en esta guía. Se puede encontrar más información en la guía complementaria [Amenazas y contramedidas: Configuración de la seguridad en Windows Server 2003 y Windows XP](http://go.microsoft.com/fwlink/?linkid=15159), en http://go.microsoft.com/fwlink/?LinkId=15159.

[](#mainsection)[Principio de la página](#mainsection)

### Información general acerca de la guía

#### Capítulo 1: Introducción a la Guía de seguridad de Windows Server 2003

Este capítulo proporciona un resumen ejecutivo de la *Guía de seguridad de Windows Server 2003* e incluye una breve descripción general de cada capítulo. También describe los entornos Cliente heredado, Cliente de empresa y Seguridad especializada: Funcionalidad limitada, así como los equipos que se ejecutan en éstos.

#### Capítulo 2: Mecanismos de seguridad de Windows Server 2003

Este capítulo proporciona información general sobre los principales mecanismos utilizados para reforzar la seguridad de Windows Server 2003 con SP1 en esta guía: el Asistente para configuración de seguridad (SCW) y la directiva de grupo de Active Directory. Explica cómo SCW proporciona un marco interactivo para crear, administrar y probar directivas de seguridad para equipos basados en Windows Server 2003 que cumplen distintas funciones de servidor. También evalúa las capacidades de SCW dentro del contexto de los tres entornos que se describen en el capítulo 1.

La siguiente parte del capítulo proporciona descripciones de alto nivel del diseño de Active Directory, el diseño de unidades organizativas (UO), los objetos de directiva de grupo (GPO), el diseño de grupos administrativos y la directiva de dominio. Estos temas se analizan en el contexto de los tres entornos que se describen en el capítulo 1 para proporcionar una visión de un entorno de estado final seguro ideal.

Este capítulo concluye con un examen detallado de cómo esta guía combina las mejores funciones de SCW y los planteamientos tradicionales basados en GPO para reforzar la seguridad de Windows Server 2003 con SP1.

#### Capítulo 3: Directiva de dominio

En este capítulo se explican contramedidas adicionales y las configuraciones de las plantillas de seguridad para las directivas de nivel de dominio de los tres entornos que se describen en el capítulo 1. Este capítulo no se centra en una función específica de servidor, sino en las directivas y la configuración específicas que son útiles para las directivas de dominio de nivel superior.

#### Capítulo 4: Directiva de línea de base de servidores miembro

Este capítulo se centra en cómo establecer una Directiva de línea de base de servidores miembro (MSBP) para las funciones de servidor que se tratan posteriormente en la guía.

#### Capítulo 5: Directiva de línea de base de controladores de dominio

La función de servidor controlador de dominio es una de las más importantes para garantizar la seguridad de cualquier entorno de Active Directory con equipos que ejecutan Windows Server 2003 con SP1. Cualquier problema en la seguridad de un controlador de dominio podría afectar a los equipos clientes, servidores y aplicaciones que dependan de controladores de dominio para la autenticación, de la directiva de grupo y de un directorio LDPA (Protocolo ligero de acceso a directorios). En los tres entornos definidos en la guía, los controladores de dominio también proporcionan servicios DNS.

#### Capítulo 6: Función de servidor de infraestructura

En este capítulo, la función de servidor de infraestructura es aquella que proporciona servicios DHCP o WINS. Se proporcionan detalles acerca de cómo los servidores de infraestructura Windows Server 2003 con SP1 en su entorno pueden beneficiarse de la configuración de seguridad no aplicada por la Directiva de línea de base de servidores miembro (MSBP).

#### Capítulo 7: Función de servidor de archivos

Este capítulo se centra en cómo reforzar la seguridad de los equipos que funcionan como servidores de archivos y por qué es un desafío reforzar dichos servidores. Los servicios más esenciales que los servidores de archivos precisan son los protocolos relacionados con NetBIOS, bloque de mensajes del servidor (SMB) y sistema común de archivos de Internet (CIFS). Los protocolos SMB y CIFS se utilizan normalmente para permitir el acceso de usuarios autenticados pero, cuando se aseguran de forma incorrecta, pueden revelar también gran cantidad de información a usuarios sin autenticar o atacantes. A causa de esta amenaza, estos protocolos a menudo se desactivan en entornos de alta seguridad. Este capítulo describe cómo los servidores de archivos que ejecutan Windows Server 2003 con SP1 pueden beneficiarse de la configuración de seguridad no aplicada por el MSBP.

#### Capítulo 8: Función de servidor de impresión

Este capítulo se centra en los servidores de impresión. Al igual que los servidores de archivos, los servicios más esenciales que los servidores de impresión precisan son los protocolos relacionados con NetBIOS de Windows y los protocolos SMB y CIFS. Como se ha indicado anteriormente, los protocolos SMB y CIFS están a menudo deshabilitados en los entornos de alta seguridad. Este capítulo describe cómo se puede reforzar la configuración de seguridad del servidor de impresión de Windows Server 2003 SP1 en áreas no contempladas por MSBP.

#### Capítulo 9: Función de servidor web

En este capítulo se describe la forma en la que la seguridad de aplicaciones y sitios web requiere un servidor IIS completo (incluidos cada sitio web y aplicación que se ejecute en el mismo) para protegerse de los equipos cliente del entorno. Las aplicaciones y sitios web también se deben proteger de otras aplicaciones y sitios web que se ejecuten en el mismo servidor IIS. En este capítulo se describen con todo detalle las prácticas para garantizar que los servidores IIS que ejecutan Windows Server 2003 con SP1 del entorno logren estas medidas.

#### Capítulo 10: Función de servidor IAS

Los servidores de autenticación de Internet (IAS) proporcionan Servicios de usuario de acceso telefónico de autenticación remota (RADIUS), un protocolo de autenticación basado en estándares que se ha diseñado para verificar la identidad de clientes que tienen acceso a las redes de forma remota. Este capítulo describe cómo los servidores IAS que ejecutan Windows Server 2003 con SP1 pueden beneficiarse de la configuración de seguridad no aplicada por MSBP.

#### Capítulo 11: Función de servidor de Servicios de Certificate Server

Los Servicios de Certificate Server ofrecen los mecanismos de cifrado y administración de certificados necesarios para crear una infraestructura de claves públicas (PKI) en el entorno de servidor. Este capítulo describe cómo los servidores de Servicios de Certificate Server que ejecutan Windows Server 2003 con SP1 pueden beneficiarse de la configuración de seguridad no aplicada por MSBP.

#### Capítulo 12: Función de los hosts de baluarte

Los equipos cliente pueden acceder a los servidores de host de baluarte a través de Internet. En este capítulo se explica cómo estos sistemas expuestos públicamente son susceptibles a ataques por parte de una gran cantidad usuarios que pueden permanecer completamente anónimos si así lo desean. Como muchas organizaciones no extienden su infraestructura de dominios a Internet, este capítulo se centra en cómo reforzar los equipos independientes que ejecutan Windows Server 2003 con SP1, pero que no pertenecen a un dominio basado en Active Directory.

#### Capítulo 13: Conclusión

El capítulo que concluye esta guía resume brevemente el contenido que se ha presentado en los capítulos anteriores.

#### Apéndice A: Herramientas de seguridad y formatos

Aunque la *Guía de seguridad de Windows Server 2003* se centra en cómo utilizar SCW para crear directivas que luego se convierten en plantillas de seguridad y objetos de directiva de grupo, existen otras herramientas y formatos de datos que se pueden utilizar para aumentar o reemplazar esta metodología. Este apéndice proporciona una lista corta de estas herramientas y formatos.

#### Apéndice B: Opciones clave que se deben considerar

La *Guía de seguridad de Windows Server 2003* trata numerosas contramedidas y opciones de seguridad; sin embargo, debe tenerse presente que algunas son especialmente importantes. En este apéndice se describen las opciones de configuración que tendrán mayor repercusión sobre la seguridad de los equipos en los que se ejecuta Windows Server 2003 con SP1.

#### Apéndice C: Resumen de configuración de plantillas de seguridad

Este apéndice ofrece información sobre el libro de Microsoft Excel® denominado "[Windows Server 2003 Security Guide Settings](http://go.microsoft.com/fwlink/?linkid=14846)", que se incluye con las herramientas y plantillas de la [versión descargable](http://go.microsoft.com/fwlink/?linkid=14846) de esta guía, en http://go.microsoft.com/fwlink/?LinkId=14846. Esta hoja de cálculo proporciona una referencia completa en un formato compacto y práctico sobre toda la configuración recomendada para los tres entornos que se definen en esta guía.

#### Apéndice D: Prueba de la Guía de seguridad de Windows Server 2003

La *Guía de seguridad de Windows Server 2003* proporciona una gran cantidad de información acerca de cómo reforzar la seguridad de los servidores que ejecutan Windows Server 2003 con SP1. No obstante, se recomienda constantemente al lector probar y validar todos los parámetros de configuración antes de implementarlos en un entorno de producción.

Este apéndice muestra cómo crear un entorno de laboratorio de pruebas adecuado que se pueda utilizar para garantizar la implementación satisfactoria de la configuración recomendada en un entorno de producción. Ayuda a los usuarios a realizar la validación necesaria y minimiza la cantidad de recursos necesarios para dicha acción.

#### Herramientas y plantillas

La versión descargable de esta guía incluye un conjunto de plantillas de seguridad, secuencias de comandos y herramientas adicionales que facilitarán a su organización las tareas de evaluar, probar e implementar las contramedidas recomendadas. Las plantillas de seguridad son archivos de texto que se pueden importar a directivas de grupo basadas en dominios o aplicarse de forma local con el complemento de análisis y configuración de seguridad de Microsoft Management Console (MMC). Estos procedimientos se detallan en el capítulo 2, "Mecanismos de seguridad de Windows Server 2003". Las secuencias de comandos incluidas en esta guía incluyen secuencias de comandos para crear y vincular objetos de directiva de grupos así como secuencias de comandos de prueba que se utilizan para probar las contramedidas recomendadas.

[](#mainsection)[Principio de la página](#mainsection)

### Recursos relacionados

Para obtener información adicional acerca de la configuración de seguridad recomendada en esta guía, descargue la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://www.microsoft.com/spain/technet/recursos/articulos/secmod48.mspx), en http://go.microsoft.com/fwlink/?LinkId=15160, así como la [*Guía de seguridad de Windows XP*](http://go.microsoft.com/fwlink/?linkid=14840) en http://go.microsoft.com/fwlink/?LinkId=14840. Hay disponibles [otras soluciones de seguridad](http://www.microsoft.com/technet/community/columns/sectip/st0805.mspx) del equipo de Microsoft Solutions for Security and Compliance (MSSC) en www.microsoft.com/technet/community/columns/sectip/st0805.mspx (en inglés).

[](#mainsection)[Principio de la página](#mainsection)

### Comuníquenos su opinión

El equipo de Microsoft Solutions for Security and Compliance (MSSC) agradece sus ideas acerca de ésta y otras soluciones de seguridad.

¿Tiene una opinión? Háganosla saber en la [bitácora de soluciones de seguridad para el profesional de TI](http://blogs.technet.com/secguide).

O envíe sus comentarios por correo electrónico a la dirección siguiente: [SecWish@microsoft.com](mailto:secwish@microsoft.com?subject=guía%20de%20seguridad%20de%20windows%20server%202003%20). Respondemos con frecuencia a los comentarios que se envían a este buzón.

Nos interesa su opinión.

[](#mainsection)[Principio de la página](#mainsection)

### Servicios de consultoría y soporte técnico

Existen muchos servicios disponibles para ayudar a las organizaciones en sus esfuerzos por mejorar su seguridad. Utilice los siguientes vínculos para encontrar los servicios que necesita:

Para buscar servicios de consultoría y soporte técnico adecuados a las necesidades de su organización, visite [Microsoft Services](http://www.microsoft.com/services/microsoftservices/default.mspx) en http://support.microsoft.com/msservices.

**Descargar**

[Obtenga la Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14846)

**Notificaciones de actualizaciones**

[Suscríbase para obtener más información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)

**Comentarios**

[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?asunto=guía%20de%20seguridad%20de%20windows%20server%202003)

[](#mainsection)[Principio de la página](#mainsection)
