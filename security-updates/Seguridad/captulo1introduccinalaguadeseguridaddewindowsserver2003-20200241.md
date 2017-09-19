---
TOCTitle: 'Capítulo 1: Introducción a la Guía de seguridad de Windows Server 2003'
Title: 'Capítulo 1: Introducción a la Guía de seguridad de Windows Server 2003'
ms:assetid: '8a6cda2e-32c2-4945-897f-0353cd6e908a'
ms:contentKeyID: 20200241
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163108(v=TechNet.10)'
---

Guía de Seguridad de Windows Server 2003
========================================

### Capítulo 1: Introducción a la Guía de seguridad de Windows Server 2003

Actualizado: 27/12/05

### En esta página

[](#eiaa)[Información general](#eiaa)
[](#ehaa)[Resumen ejecutivo](#ehaa)
[](#egaa)[Destinatarios de la guía](#egaa)
[](#efaa)[Ámbito de esta guía](#efaa)
[](#eeaa)[Descripción de los capítulos](#eeaa)
[](#edaa)[Capacitación y conocimientos previos](#edaa)
[](#ecaa)[Requisitos de software](#ecaa)
[](#ebaa)[Convenciones de estilo](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Información general

Guía de seguridad de *Windows* *Server* *2003*. El objetivo de esta guía es proporcionarle la mejor información disponible para que pueda evaluar y hacer frente a los riesgos de seguridad de su organización que sean específicos de Microsoft® Windows Server™ 2003 con Service Pack 1 (SP1). Los capítulos de esta guía proporcionan una orientación detallada acerca de cómo mejorar la configuración y las características de seguridad de Windows Server 2003 con SP1 para hacer frente de la mejor manera posible a las amenazas identificadas en su entorno. Esta guía está destinada a los ingenieros de sistemas, los consultores y los administradores de red que trabajan en un entorno basado en Windows Server 2003 con SP1.

La guía ha sido revisada y aprobada por equipos de ingeniería, consultores, ingenieros de soporte técnico, clientes y socios de Microsoft. Microsoft ha trabajado con consultores e ingenieros de sistemas que han implementado Windows Server 2003, Windows® XP y Windows 2000 en una variedad de entornos con el fin de establecer las últimas recomendaciones para garantizar la seguridad de estos clientes y servidores. Estas recomendaciones se describen en detalle en la guía.

La guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en*
*Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159) (disponible en http://go.microsoft.com/fwlink/?LinkId=15159), proporciona información general completa sobre los principales parámetros de configuración de seguridad de Windows Server 2003 con SP1 y Windows XP con SP2. Los capítulos del 2 al 12 de esta guía incluyen prescripciones, procedimientos y recomendaciones de seguridad paso a paso para proporcionarle listas de tareas que le ayudarán a alcanzar un nivel elevado de seguridad en los equipos de su organización que ejecutan Windows Server 2003 con SP1. Si precisa información más detallada de los conceptos que se presentan en este material, consulte recursos como el *Kit de recursos de Microsoft Windows 2003 Server*, el *Kit de recursos de Microsoft Windows* *XP*, el *Kit de recursos de seguridad de Microsoft Windows* *2000* y Microsoft TechNet.

[](#mainsection)[Principio de la página](#mainsection)

### Resumen ejecutivo

Se recomienda a los usuarios, sea cual sea el entorno del que dispongan, que se tomen muy en serio las cuestiones relacionadas con la seguridad. Muchas organizaciones subestiman el valor de su entorno de tecnología de la información (TI), a menudo porque no incluyen gastos indirectos considerables. Si un ataque a los servidores del entorno resulta ser lo suficientemente grave, toda la organización se podría ver enormemente afectada. Por ejemplo, un ataque que provocara la interrupción del servicio ofrecido en el sitio web de la organización podría ocasionar importantes pérdidas de beneficios o de la confianza de los clientes y a su vez afectar a la rentabilidad de la empresa. Al evaluar los costos de la seguridad, se deben incluir los gastos indirectos asociados a cualquier ataque, además de los correspondientes a la pérdida de la funcionalidad de TI.

Un análisis de la situación, la vulnerabilidad y los riesgos en lo que respecta a la seguridad puede informar de las concesiones que hay que hacer para equilibrar la seguridad y la capacidad de uso de todos los equipos de un entorno de red. En esta guía se detallan las principales contramedidas de seguridad disponibles en Windows Server 2003 con SP1, las vulnerabilidades a las que hacen frente y las posibles consecuencias negativas, en el caso de que las hubiera, derivadas de la implementación de cada una de ellas.

La guía proporciona también recomendaciones específicas acerca de cómo reforzar la seguridad de los equipos que ejecutan Windows Server 2003 con SP1 en tres entornos de empresa. El entorno Cliente heredado (LC) debe ser compatible con sistemas operativos antiguos, como Windows 98. El entorno Cliente de empresa (EC) es aquel en el que Windows 2000 es la versión del sistema operativo Windows más baja que se utiliza en los equipos. El tercer entorno es aquel en el que la preocupación por la seguridad es tan importante que se considera aceptable una pérdida significativa de funcionalidad y capacidad de administración a cambio de lograr el máximo nivel de seguridad. Este tercer entorno se conoce como Seguridad Especializada: Funcionalidad limitada (SSLF). Gracias a los esfuerzos realizados para que la información de esta guía se presente de forma organizada y resulte de fácil acceso, podrá encontrar y determinar con facilidad qué parámetros son los más adecuados para los equipos de su organización. Aunque esta guía va destinada a los clientes empresariales, gran parte de su contenido también resulta adecuado para organizaciones de cualquier tamaño.

Para sacar el máximo provecho del material, deberá leer la totalidad de la guía. Puede consultar también la guía complementaria, [*Amenazas y contramedidas: configuración de seguridad en*
*Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), en http://go.microsoft.com/fwlink/?LinkId=15159.

El equipo que ha elaborado esta guía espera que el material le resulte útil, informativo e interesante.

[](#mainsection)[Principio de la página](#mainsection)

### Destinatarios de la guía

Esta guía está destinada principalmente a consultores, especialistas en seguridad, arquitectos de sistemas y profesionales de TI que planean el desarrollo de aplicaciones o infraestructuras y la implementación de Windows Server 2003. Estas funciones incluyen las siguientes descripciones de trabajo comunes:

-   Arquitectos y programadores responsables de las tareas en materia de arquitectura para los clientes de sus organizaciones.

-   Expertos en seguridad de TI que se centren estrictamente en garantizar la seguridad de las distintas plataformas de la organización.

-   Analistas de negocio y responsables de la toma de decisiones relacionadas con requisitos y objetivos empresariales de vital importancia que dependan de la compatibilidad de los clientes.

-   Consultores de socios y servicios de Microsoft que precisen recursos detallados con información útil y relevante para asociados y clientes empresariales.

[](#mainsection)[Principio de la página](#mainsection)

### Ámbito de esta guía

Esta guía se centra en la creación y el mantenimiento de un entorno seguro para los equipos que ejecutan Windows Server 2003 con SP1 dentro la organización. En ella se explican las diferentes fases para garantizar la seguridad de los tres entornos definidos en la guía y los parámetros de configuración de servidor que se deben aplicar teniendo en cuenta las dependencias del cliente. Los tres entornos se describen de la siguiente manera:

-   El entorno Cliente heredado (LC) consta de un dominio del servicio de directorio de Active Directory®, con servidores miembro y controladores de dominio que ejecutan Windows Server 2003 y algunos equipos cliente que ejecutan Microsoft Windows 98 y Windows NT® 4.0. Los equipos que ejecutan Windows 98 deben tener instalada la extensión de cliente de Active Directory (DSClient). Hay disponible más información en el artículo de Microsoft Knowledge Base "[Cómo instalar la extensión del cliente de Active Directory](http://support.microsoft.com/kb/288358)" en http: //support.microsoft.com/kb/288358.

-   El entorno Cliente de empresa (EC) consta de un dominio de Active Directory®, con servidores miembro y controladores de dominio que ejecutan Windows Server 2003 con SP1 y equipos cliente que ejecutan Microsoft Windows 2000 y Windows XP®.

-   El entorno Seguridad especializada: Funcionalidad limitada (SSLF) también consta de un dominio de Active Directory, con servidores miembro y controladores de dominio que ejecutan Windows Server 2003 con SP1 y clientes que ejecutan Windows 2000 y Windows XP. Sin embargo, la configuración del entorno Seguridad especializada: Funcionalidad limitada es tan restrictiva que puede que muchas aplicaciones no funcionen. Por esta razón, el rendimiento de los servidores se puede ver afectado y será mucho más que un reto administrarlos.

    Además, los equipos cliente que no estén protegidos con las directivas de SSLF pueden experimentar problemas de comunicación con los equipos cliente y servidores que sí lo estén. Consulte la *Guía de seguridad de Windows XP* para obtener más información acerca de cómo asegurar equipos cliente con la configuración compatible con SSLF.

Se proporciona orientación sobre las formas de reforzar la seguridad de los equipos de estos tres entornos para un grupo de diferentes funciones de servidor. Las contramedidas que se describen y las herramientas que se proporcionan asumen que cada servidor tendrá una sola función. Si necesita combinar las funciones de algunos de los servidores en su entorno, puede personalizar las plantillas de seguridad que se incluyen en el archivo de descarga que acompaña a esta guía para crear la combinación apropiada de servicios y opciones de seguridad. Las funciones que se describen en esta guía incluyen:

-   Controladores de dominio

-   Servidores de infraestructura

-   Servidores de archivos

-   Servidores de impresión

-   Servidores IIS (Internet Information Services)

-   Servidores IAS (Servicios de autenticación de Internet)

-   Servidores de Servicios de Certificate Server

-   Hosts de baluarte

La configuración recomendada en esta guía se ha probado de forma minuciosa en entornos de laboratorio que simulaban los entornos anteriormente descritos: Cliente heredado, Cliente de empresa y Seguridad especializada: Funcionalidad limitada. Aunque los parámetros han probado su eficacia en el laboratorio, es importante que su organización también realice pruebas en su propio laboratorio con un entorno que represente el entorno de producción real. Probablemente sea necesario realizar algunas modificaciones en las plantillas de seguridad y en los procedimientos manuales presentados en la guía para que todas las aplicaciones empresariales sigan funcionando como se espera. La información detallada que se proporciona en la guía complementaria, *Amenazas y contramedidas: configuración de seguridad en Windows* *Server* *2003 y Windows* *XP*, proporciona la información necesaria para evaluar cada contramedida específica y decidir cuáles de ellas son apropiadas para el entorno y las necesidades empresariales únicas de su organización.

[](#mainsection)[Principio de la página](#mainsection)

### Descripción de los capítulos

La *Guía de seguridad de Windows* *Server* *2003* consta de 13 capítulos, cada uno de los cuales se basa en el proceso de solución de un extremo a otro necesario para implementar y garantizar la seguridad de Windows Server 2003 con SP1 en su entorno. Los primeros capítulos describen cómo crear una base que le permita reforzar la seguridad de los servidores de la organización; en el resto de los capítulos se explican los procedimientos que son exclusivos de cada función de servidor.

#### Capítulo 1: Introducción a la Guía de seguridad de Windows Server 2003

Este capítulo presenta la *Guía de seguridad de Windows* *Server* *2003* e incluye una breve descripción general de cada capítulo. Describe los entornos de cliente heredado, cliente de empresa y seguridad especializada (funcionalidad limitada), y los equipos que se ejecutan en éstos.

#### Capítulo 2: Mecanismos de seguridad de Windows Server 2003

Este capítulo proporciona información general sobre los principales mecanismos utilizados para reforzar la seguridad del SP1 de Windows Server 2003 en esta guía: el Asistente para configuración de seguridad (SCW) y la directiva de grupo de Active Directory. Explica cómo SCW proporciona un marco interactivo para crear, administrar y probar directivas de seguridad para servidores Windows con distintas funciones. También evalúa las capacidades de SCW dentro del contexto de los tres entornos que se describen en el capítulo 1.

La siguiente parte del capítulo proporciona descripciones de alto nivel del diseño de Active Directory, el diseño de unidades organizativas (UO), los objetos de directiva de grupo (GPO), el diseño de grupos administrativos y la directiva de dominio. Estos temas se analizan en el contexto de los tres entornos que se describen en el capítulo 1 para proporcionar una visión de un entorno de estado final seguro ideal.

Este capítulo concluye con un examen detallado de cómo esta guía combina las mejores funciones de SCW y los planteamientos tradicionales basados en GPO para reforzar la seguridad de Windows Server 2003 con SP1.

#### Capítulo 3: Directiva de dominio

En este capítulo se explican contramedidas adicionales y las configuraciones de las plantillas de seguridad para las directivas de nivel de dominio de los tres entornos que se describen en el capítulo 1. El capítulo no se centra en una función específica del servidor, sino en las directivas y la configuración específicas que son útiles para directivas de dominio de nivel superior.

#### Capítulo 4: Directiva de línea de base de servidores miembro

En este capítulo se explican contramedidas adicionales y las configuraciones de las plantillas de seguridad de las funciones de servidor de los tres entornos definidos en el capítulo 1. El capítulo se centra en cómo establecer una Directiva de línea de base de servidores miembro (MSBP) para las funciones de servidor que se tratan posteriormente en la guía.

El objetivo de las recomendaciones de este capítulo es permitir a las organizaciones implementar sin riesgos configuraciones para implementaciones existentes y nuevas de Windows Server 2003 con SP1. Las configuraciones predeterminadas de seguridad del SP1 de Windows Server 2003 se han investigado y probado; además, las recomendaciones de este capítulo se han creado para ofrecer una mayor seguridad que la configuración predeterminada del sistema operativo. En determinados casos, se sugiere usar una configuración menos restrictiva que la presente en la instalación predeterminada de Windows Server 2003 con SP1 para proporcionar compatibilidad con los entornos Cliente Heredado.

#### Capítulo 5: Directiva de línea de base de controladores de dominio

La función de servidor controlador de dominio es una de las más importantes para garantizar la seguridad de cualquier entorno de Active Directory con equipos que ejecutan Windows Server 2003 con SP1. Cualquier problema en la seguridad de un controlador de dominio podría afectar a los equipos clientes, servidores y aplicaciones que dependan de controladores de dominio para la autenticación, de la directiva de grupo y de un directorio LDPA (Protocolo ligero de acceso a directorios).

En este capítulo se describe la necesidad de almacenar siempre los controladores de dominio en ubicaciones físicas seguras a las que sólo pueda tener acceso personal administrativo autorizado. También se describen los riesgos que supone almacenar los controladores de dominio en ubicaciones poco seguras, como oficinas sucursales, y una parte importante del capítulo se destina a la explicación de las consideraciones de seguridad que son la base de la directiva de grupo de controladores de dominio recomendada.

Los controladores de dominio de Active Directory requieren un servicio DNS estable que esté configurado de forma apropiada. De forma predeterminada, Windows Server 2003 con SP1 integra zonas DNS en Active Directory, lo que permite a los controladores de dominio ejecutar el servicio DNS y responder a las solicitudes de DNS de los clientes del dominio de Active Directory. Este capítulo asume que el controlador de dominio proporcionará también el servicio DNS y proporciona la guía apropiada.

#### Capítulo 6: Función de servidor de infraestructura

En este capítulo, la función de servidor de infraestructura se define como un servidor DHCP o como un servidor WINS. Se proporcionan detalles acerca de cómo los servidores de infraestructura Windows Server 2003 con SP1 en su entorno pueden beneficiarse de la configuración de seguridad no aplicada por la Directiva de línea de base de servidores miembro (MSBP). Este capítulo no incluye información de configuración para el servicio DNS, que se incluye en la función de controlador de dominio.

#### Capítulo 7: Función de servidor de archivos

Este capítulo se centra en la función de servidor de archivos y los aspectos difíciles acerca de cómo reforzar la seguridad de dichos servidores. Los servicios más esenciales para los servidores de archivos precisan de los protocolos relacionados con NetBIOS de Windows y de los protocolos SMB y CIFS. Los protocolos Bloque de mensajes del servidor (SMB) y Sistema común de archivos de Internet (CIFS) se utilizan normalmente para permitir el acceso de usuarios autenticados pero, cuando se aseguran de forma incorrecta, pueden revelar también gran cantidad de información a usuarios sin autenticar o atacantes. A causa de esta amenaza, estos protocolos a menudo se desactivan en entornos de alta seguridad. Este capítulo describe cómo los servidores de archivos que ejecutan Windows Server 2003 con SP1 pueden beneficiarse de la configuración de seguridad no aplicada por el MSBP.

#### Capítulo 8: Función de servidor de impresión

Este capítulo se centra en los servidores de impresión. Al igual que los servidores de archivos, los servicios más esenciales para los servidores de impresión precisan de los protocolos relacionados con NetBIOS de Windows y de los protocolos SMB y CIFS. Como se ha indicado anteriormente, estos protocolos a menudo se desactivan en entornos de alta seguridad. Este capítulo describe cómo se puede reforzar la configuración de seguridad del servidor de impresión de Windows Server 2003 SP1 en áreas no contempladas por MSBP.

#### Capítulo 9: Función de servidor web

En este capítulo se describe la forma en la que la seguridad de aplicaciones y sitios web requiere un servidor IIS completo (incluidos cada sitio web y aplicación que se ejecute en el mismo) para protegerse de los equipos cliente del entorno. Las aplicaciones y sitios web también se deben proteger de otras aplicaciones y sitios web que se ejecuten en el mismo servidor IIS. En este capítulo se describen con todo detalle las prácticas para garantizar que los servidores IIS que ejecutan Windows Server 2003 con SP1 del entorno logran estas medidas.

IIS no se instala de forma predeterminada en los miembros de la familia del sistema de servidores Windows Server System™. La instalación inicial de IIS se realiza en un modo de "bloqueo" muy seguro. Por ejemplo, la configuración predeterminada sólo permite que IIS sirva contenido estático. Algunas características, como páginas Active Server (ASP), ASP.NET, inclusiones de servidor, publicación en WebDAV y extensiones de servidor de Microsoft FrontPage®, las debe habilitar el administrador desde el nodo Extensiones de servicio web del Administrador de servicios de Internet Information Server (Administrador IIS).

Las secciones de este capítulo proporcionan detalles acerca de una variedad de parámetros de configuración que puede utilizar para reforzar la seguridad de los servidores IIS del entorno. Se hace énfasis en la necesidad de supervisar, detectar y responder a los problemas de seguridad para garantizar una seguridad continua de los servidores. Este capítulo se centra en las aplicaciones y los protocolos web de IIS, como HTTP, y no incluye ninguna orientación sobre los demás protocolos que IIS puede proporcionar, como SMTP, FTP y NNTP.

#### Capítulo 10: Función de servidor IAS

Los servidores de autenticación de Internet (IAS) proporcionan Servicios de usuario de acceso telefónico de autenticación remota (RADIUS), un protocolo de autenticación basado en estándares que se ha diseñado para verificar la identidad de clientes que tienen acceso a las redes de forma remota. Este capítulo describe cómo los servidores IAS que ejecutan Windows Server 2003 con SP1 pueden beneficiarse de la configuración de seguridad no aplicada por MSBP.

#### Capítulo 11: Función de servidor de Servicios de Certificate Server

Los Servicios de Certificate Server ofrecen los mecanismos de cifrado y administración de certificados necesarios para crear una infraestructura de claves públicas (PKI) en el entorno de servidor. Este capítulo describe cómo los servidores de Servicios de Certificate Server que ejecutan Windows Server 2003 con SP1 pueden beneficiarse de la configuración de seguridad no aplicada por MSBP.

#### Capítulo 12: Función de los hosts de baluarte

Los equipos cliente pueden acceder a los servidores de host de baluarte a través de Internet. En este capítulo se explica cómo estos equipos expuestos públicamente son susceptibles a ataques por parte de una gran cantidad usuarios que pueden permanecer completamente anónimos si así lo desean. La infraestructura de dominios de muchas organizaciones no abarca Internet. Por este motivo, el contenido de este capítulo se centra en cómo reforzar la seguridad en equipos independientes. Se proporcionan detalles sobre las formas en que los host de baluarte que ejecutan Windows Server 2003 con SP1 pueden beneficiarse de las recomendaciones de seguridad de esta guía para los equipos que no son miembros de un dominio basado en Active Directory.

#### Capítulo 13: Conclusión

El capítulo que concluye esta guía revisa los puntos más importantes de los temas que se han presentado en los capítulos anteriores.

#### Apéndice A: Herramientas de seguridad y formatos

Aunque esta guía se centra en cómo utilizar SCW para crear las directivas que se convierten en plantillas de seguridad y objetos de directiva de grupo, existen otras herramientas y formatos de archivos que se pueden utilizar para aumentar o reemplazar esta metodología. Este apéndice proporciona una lista corta de estas herramientas y formatos.

#### Apéndice B: Opciones clave que se deben considerar

Esta guía trata numerosas contramedidas y opciones de seguridad; sin embargo, debe tenerse presente que algunas son especialmente importantes. En este apéndice se describen las opciones de configuración que tendrán mayor repercusión sobre la seguridad de los equipos en los que se ejecuta Windows Server 2003 con SP1.

#### Apéndice C: Resumen de configuración de plantillas de seguridad

Este apéndice ofrece información sobre el libro de Microsoft Excel® denominado "Windows Server 2003 Security Guide Settings", que se incluye con las herramientas y plantillas de la [versión descargable](http://go.microsoft.com/fwlink/?linkid=14846) de esta guía, en http://go.microsoft.com/fwlink/?LinkId=14846. Esta hoja de cálculo proporciona una referencia completa en una forma compacta y práctica de toda la configuración recomendada para los tres entornos que se definen en esta guía.

#### Apéndice D: Prueba de la Guía de seguridad de Windows Server 2003

Esta guía proporciona una gran cantidad de información acerca de cómo reforzar la seguridad de los servidores que ejecutan Windows Server 2003 con SP1. No obstante, se recomienda constantemente al lector probar y validar todos los parámetros de configuración antes de implementarlos en un entorno de producción.

Este apéndice muestra cómo crear un entorno de laboratorio de pruebas adecuado que se pueda utilizar para garantizar la implementación satisfactoria de la configuración recomendada en un entorno de producción. Ayuda a los usuarios a realizar la validación necesaria y minimiza la cantidad de recursos necesarios para dicha acción.

#### Herramientas y plantillas

La versión descargable de esta guía incluye un conjunto de plantillas de seguridad, secuencias de comandos y herramientas adicionales que permiten a su organización evaluar, probar e implementar las contramedidas recomendadas. Las plantillas de seguridad son archivos de texto que se pueden importar a directivas de grupo basadas en dominios o aplicarse de forma local con el complemento de análisis y configuración de seguridad de Microsoft Management Console (MMC). Estos procedimientos se detallan en el capítulo 2, "Mecanismos de seguridad de Windows Server 2003". Las secuencias de comandos incluidas en esta guía incluyen secuencias de comandos para crear y vincular objetos de directiva de grupos así como secuencias de comandos de prueba que se utilizan para probar las contramedidas recomendadas. También se incluye el libro de Excel en el que se resumen los parámetros de configuración de las plantillas de seguridad (mencionado anteriormente en la sección "Apéndice C").

Se utiliza el término herramientas y plantillas para designar a todos los archivos que acompañan a esta guía. Estos archivos se incluyen en un archivo .msi que forma parte del archivo WinZip autoextraíble que contiene esta guía, que está disponible en el Centro de descarga de Microsoft en http://go.microsoft.com/fwlink/?LinkId=14846. Al ejecutar el archivo .msi, se creará la siguiente estructura de carpetas en la ubicación especificada:

-   **\\Windows Server 2003 Security Guide Tools and Templates\\Security Templates**. Esta carpeta contiene todas plantillas de seguridad que se describen en la guía.

-   **\\Windows Server 2003 Security Guide Tools and Templates\\Test Tools**. Esta carpeta contiene varios archivos y herramientas relacionados con el "Apéndice D: Prueba de la Guía de seguridad de Windows Server 2003".

[](#mainsection)[Principio de la página](#mainsection)

### Capacitación y conocimientos previos

Los profesionales de TI que desarrollan, implementan y garantizan la seguridad de las instalaciones de Windows Server 2003 y Windows XP en un entorno de empresa deben poseer los siguientes conocimientos y habilidades:

-   Certificación MCSE 2000 o 2003, con más de dos años de experiencia en materia de seguridad.

-   Conocimiento profundo en materia de dominios corporativos y entornos de Active Directory.

-   Uso de herramientas de administración, entre las que se incluyen: Microsoft Management Console (MMC), Secedit, Gpupdate y Gpresult.

-   Experiencia en la administración de directivas de grupo.

-   Experiencia en la implementación de aplicaciones y estaciones de trabajo en entornos de empresa.

[](#mainsection)[Principio de la página](#mainsection)

### Requisitos de software

Los requisitos de software para las herramientas y plantillas que se describen en esta guía son:

-   Windows Server 2003 Standard Edition con SP1, Windows Server 2003 Enterprise Edition con SP1 o Windows Server 2003 Datacenter Edition con SP1.

-   Un dominio de Active Directory basado en Windows Server 2003.

-   Microsoft Excel 2000 o posterior.

[](#mainsection)[Principio de la página](#mainsection)

### Convenciones de estilo

En esta guía se utilizan las siguientes convenciones de estilo y terminología.

**Tabla 1.1: Convenciones de estilo**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Elemento</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p><strong>Negrita</strong></p></td>
<td style="border:1px solid black;"><p>Caracteres que se escriben exactamente tal y como se muestran, incluidos comandos, modificadores y nombres de archivo. Los elementos de la interfaz de usuario también aparecen en negrita.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><em>Cursiva</em></p></td>
<td style="border:1px solid black;"><p>Los títulos de libros y otras publicaciones importantes aparecen en cursiva.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><em>&lt;Cursiva&gt;</em></p></td>
<td style="border:1px solid black;"><p>Los marcadores de posición en cursiva y entre corchetes angulares, <em>&lt;nombre de archivo&gt;</em>, representan variables.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Fuente Monospace</p></td>
<td style="border:1px solid black;"><p>Define ejemplos de código y de secuencia de comandos.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>Nota</strong></p></td>
<td style="border:1px solid black;"><p>Avisa al lector de que hay información adicional.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>Importante</strong></p></td>
<td style="border:1px solid black;"><p>Avisa al lector de que hay información adicional básica.</p></td>
</tr>  
</tbody>  
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Este capítulo ha proporcionado información general sobre los factores principales relacionados con la seguridad de los equipos que ejecutan Windows Server 2003 con SP1. Esta información se considerará y tratará más detenidamente en el resto de la guía. Ahora que ya conoce cómo está organizada la guía, puede decidir si leerla de principio a fin o seleccionar sólo aquellas partes que le interesen.
  
Sin embargo, es importante recordar que para que las operaciones sean eficaces y consigan el fin esperado es necesario mejorar todas las áreas descritas en esta guía, no sólo algunas. Por esta razón y con el fin de garantizar la seguridad de los equipos de la organización que ejecutan Windows Server 2003 con SP1, Microsoft recomienda leer toda la guía y sacar así el máximo provecho de toda la información que contiene.
  
#### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de temas relacionados con seguridad y Windows Server 2003 con SP1.
  
-   Para obtener más información acerca de la seguridad en Microsoft, consulte la página [Trustworthy Computing](http://www.microsoft.com/mscorp/twc/default.mspx) (en inglés) en www.microsoft.com/mscorp/twc/default.msp.
  
-   Para obtener más información acerca de cómo MOF puede ayudar a la empresa, consulte la página de [Microsoft Operations Framework](http://www.microsoft.com/technet/itsolutions/cits/mo/mof/default.mspx) en www.microsoft.com/technet/itsolutions/cits/mo/mof/default.mspx.
  
-   Para obtener información acerca de las notificaciones de seguridad de Microsoft, consulte la página de [búsqueda de boletines de seguridad de Microsoft](http://www.microsoft.com/technet/security/current.mspx) en www.microsoft.com/technet/security/current.aspx.
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtenga la Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14846)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener más información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?asunto=guía%20de%20seguridad%20de%20windows%20server%202003)
  
[](#mainsection)[Principio de la página](#mainsection)
