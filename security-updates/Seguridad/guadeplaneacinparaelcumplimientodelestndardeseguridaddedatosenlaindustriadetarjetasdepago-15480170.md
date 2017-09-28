---
TOCTitle: Guía de planeación para el cumplimiento del Estándar de seguridad de datos en la industria de tarjetas de pago
Title: Guía de planeación para el cumplimiento del Estándar de seguridad de datos en la industria de tarjetas de pago
ms:assetid: '6687efc1-44db-4015-ae35-d1a853dc8a06'
ms:contentKeyID: 15480170
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Bb821241(v=TechNet.10)'
---

Guía de planeación para el cumplimiento del Estándar de seguridad de datos en la industria de tarjetas de pago
==============================================================================================================

##### On This Page

[![Introducción](images/Bb821241.arrow_px_down(es-es,TechNet.10).gif)](#ecaa)[Introducción](#ecaa)
[![Cumplimiento de los requisitos del Estándar PCI DSS](images/Bb821241.arrow_px_down(es-es,TechNet.10).gif)](#ebaa)[Cumplimiento de los requisitos del Estándar PCI DSS](#ebaa)
[![Apéndices](images/Bb821241.arrow_px_down(es-es,TechNet.10).gif)](#eaaa)[Apéndices](#eaaa)

### Introducción

La *Guía de planeación para el cumplimiento del Estándar de seguridad de datos en la industria de tarjetas de pago* está concebida para ayudar a las organizaciones a cumplir con los requisitos del Estándar de seguridad de datos en la industria de tarjetas de pago (PCI DSS). En concreto, esta guía está destinada a los comerciantes que aceptan tarjetas de crédito, a las instituciones financieras que procesan transacciones de tarjetas de pago y a los proveedores de servicios (compañías de terceros que ofrecen servicios de procesamiento de tarjetas de pago o de almacenamiento de datos). Las soluciones de TI para cada uno de estos grupos deben cumplir con todos los requisitos del Estándar PCI DSS. Esta guía tiene como objeto ampliar la [*Guía de planeación para el cumplimiento normativo*](http://www.microsoft.com/technet/security/guidance/complianceandpolicies/compliance/rcguide/default.mspx?mfr=true) (en inglés), que presenta un enfoque basado en el marco de creación de controles de TI como parte de los esfuerzos por cumplir con los distintos estándares y normas. En esta guía, también se describen los productos y las soluciones de tecnología de Microsoft que se pueden usar para implementar una serie de controles de TI que ayuden a cumplir los requisitos del Estándar PCI DSS, así como otras normas aplicables a las empresas.

**Nota**   Si su organización ofrece cajeros automáticos como parte de su gama de servicios, Microsoft proporciona orientación acerca de la arquitectura y la seguridad del software, los sistemas y las redes compatibles con los cajeros automáticos. Para obtener más información, consulte la página de Microsoft [*Servicios bancarios: descargas*](http://msdn2.microsoft.com/en-us/architecture/86e3451d-8219-46af-bf99-4a610e4bf1f4.aspx) (en inglés) en el sitio web de MSDN.

Esta guía no ofrece información completa acerca de la forma de cumplir con el Estándar PCI DSS para cada organización. Para obtener respuestas a preguntas relacionadas con su organización, consulte a su asesor jurídico o auditor.

La introducción de esta guía incluye las siguientes secciones:

-   **Resumen ejecutivo**: en esta sección, se ofrece una amplia información acerca de los requisitos del Estándar PCI DSS y de los objetivos principales de la guía de planeación. Se analizan los conocimientos que deben tener los administradores de TI para tratar los requisitos de cumplimiento del Estándar PCI DSS.

-   **Destinatarios de esta guía:** en esta sección, se describen los destinatarios, la finalidad y el ámbito de aplicación de esta guía, así como los riesgos y los avisos de exención de responsabilidad acerca de las limitaciones de la misma.

-   **Definición de Estándar de seguridad de datos en la industria de tarjetas de pago:** en esta sección, se ofrece información general acerca del Estándar PCI DSS y de sus requisitos.

-   **Planeación para el cumplimiento del Estándar PCI DSS**: en esta sección, se introduce el uso de un marco para satisfacer los requisitos del Estándar PCI DSS. Este enfoque incluye la creación de distintos tipos de controles de TI, el modo de funcionamiento conjunto de los controles y las razones que los convierten en componentes importantes para facilitar a la organización el cumplimiento de los requisitos del Estándar PCI DSS y otras obligaciones de cumplimiento normativo.

-   **Proceso de auditoría del Estándar PCI DSS**: en esta sección, se ofrece información general acerca del proceso de auditoría del Estándar PCI DSS que siguen los auditores para evaluar el cumplimiento de los requisitos del Estándar PCI DSS en la organización.

Puesto que estas notas del producto pretenden complementar la [*Guía de planeación para el cumplimiento normativo*](http://www.microsoft.com/technet/security/guidance/complianceandpolicies/compliance/rcguide/default.mspx?mfr=true)* *(en inglés), debe consultar también esa guía cuando planee una solución integral para cumplir con los requisitos normativos aplicables a la organización.

#### Resumen ejecutivo

Si su organización procesa, almacena o transmite información de titulares de tarjetas de pago, sus requisitos de negocio deben cumplir con el Estándar de seguridad de datos en la industria de tarjetas de pago (PCI DSS). Los requisitos que se definen en estos estándares, desarrollados por el organismo denominado PCI Security Standards Council, están diseñados para crear un nivel mínimo de seguridad aceptable para los titulares de tarjetas que usan los servicios de su organización.

Existen tres cuestiones que hacen de esta una situación complicada. La primera es que el cumplimiento de los requisitos del Estándar PCI DSS puede afectar a la organización. Es importante coordinar las labores de cumplimiento en todos los departamentos e implantar una estrategia de cumplimiento del Estándar PCI DSS para toda la organización. La segunda dificultad es que es posible que la organización deba cumplir con distintos conjuntos de normas, cada uno de los cuales exige el cumplimiento de una serie de requisitos. De hecho, a muchas compañías les cuesta asimilar la forma de responder adecuadamente a esta diversidad de requisitos normativos, al tiempo que usan procesos y procedimientos económicos para el cumplimiento ininterrumpido de las normas. La tercera cuestión complicada es que el Estándar PCI DSS, como otras muchas normas, menciona los controles de TI superficialmente, hecho que provoca que los administradores de TI deban determinar exactamente cómo tienen que obrar para cumplir de forma continuada con las normas, con escasa orientación.

La *Guía de planeación para el cumplimiento del Estándar de seguridad de datos en la industria de tarjetas de pago* está dirigida a los administradores de TI responsables del cumplimiento de las obligaciones de sus compañías en el marco del Estándar PCI DSS. El objetivo de esta guía es ayudar a los administradores de TI a conocer la forma de afrontar muchos de los requisitos de control de TI que se aplican a las organizaciones, incluidos los requisitos de cumplimiento del Estándar PCI DSS. Para ello, esta guía proporciona información acerca de las soluciones que puede aplicar en este proceso.

Para un análisis más amplio acerca de la forma de cumplir con distintos estándares normativos, consulte la [*Guía de planeación para el cumplimiento normativo*](http://www.microsoft.com/technet/security/guidance/complianceandpolicies/compliance/rcguide/default.mspx?mfr=true) (en inglés).

**Importante**   Esta guía de planeación no ofrece asesoramiento legal. La guía solo presenta información técnica y objetiva acerca del cumplimiento normativo. No consulte sólo esta guía para obtener asesoramiento acerca del tratamiento de los requisitos normativos. Si tiene preguntas concretas, consulte a su asesor jurídico o auditor.

#### Destinatarios de este documento

La *Guía de planeación para el cumplimiento del Estándar PCI DSS* está destinada fundamentalmente a aquellas personas que sean responsables de asegurarse de que sus organizaciones recopilen, procesen, transmitan y almacenen datos de los titulares de tarjetas de forma segura y confiable, al tiempo que mantienen la privacidad de esos titulares. Entre los lectores de esta guía, se incluyen los administradores de TI que trabajan en sus organizaciones en los siguientes cargos:

-   **Directores de información (CIO)** encargados de la implementación y el funcionamiento de sistemas y de los procesos asociados a TI.

-   **Directores de seguridad de la información (CISO)** encargados del programa de seguridad de la información global y de las directivas de cumplimiento de la seguridad de la información.

-   **Directores financieros (CFO)** encargados del entorno de control global de sus organizaciones.

-   **Directores de privacidad (CPO)** responsables de la implementación de directivas relacionadas con la administración de la información personal, incluidas las directivas que son compatibles con el cumplimiento de la legislación en materia de privacidad y protección de datos.

-   **Responsables de la toma de decisiones técnicas** que determinan las soluciones de tecnología adecuadas para determinados problemas de la empresa.

-   **Directores de operaciones de TI** que dirigen los sistemas y procesos que ejecutan el programa de cumplimiento del Estándar PCI DSS.

-   **Arquitectos de seguridad de TI** que diseñan los sistemas de control y seguridad de TI para proporcionar un nivel de seguridad adecuado con objeto de cubrir las necesidades empresariales de sus organizaciones.

-   **Arquitectos de infraestructuras de TI** que diseñan infraestructuras que son compatibles con los controles y la seguridad de TI que diseñan los arquitectos de seguridad de TI.

-   **Consultores y asociados** que recomiendan o implementan procedimientos recomendados de privacidad y seguridad para cumplir los objetivos de cumplimiento del Estándar PCI DSS.

Esta guía, además de estar dirigida a estos lectores, puede ser de gran valor para las siguientes personas:

-   **Directores de riesgo/cumplimiento** que son responsables de la administración global de los riesgos que conlleva el cumplimiento de los requisitos del Estándar PCI DSS para sus organizaciones.

-   **Directores de auditoría de TI** encargados de la auditoría de sistemas de TI y de la reducción de la carga de trabajo de los auditores de TI internos y externos.

#### Definición de Estándar de seguridad de datos en la industria de tarjetas de pago:

El Estándar de seguridad de datos (DSS) en la industria de tarjetas de pago (PCI) es un conjunto de requisitos globales diseñados para asegurar que la información de la tarjeta de crédito o débito del titular permanece protegida independientemente de la forma o el lugar en que se recopile, procese, transmita y almacene. Desarrollado por los miembros fundadores del organismo PCI Security Standards Council (incluidos American Express, Discover Financial Services, JCB, MasterCard Worldwide y Visa International), el Estándar PCI DSS pretende fomentar la adopción internacional de medidas sistemáticas de seguridad de datos.

El Estándar PCI DSS está dirigido a compañías y organizaciones que trabajan a diario con datos de los titulares de tarjeta. En concreto, define los requisitos para instituciones financieras, comerciantes y proveedores de servicios que tratan con datos de titulares de tarjeta durante cualquier día de trabajo normal. Este estándar consta de una lista de requisitos para administración de seguridad, directivas, procedimientos, arquitectura de red, diseño de software y otras medidas para proteger los datos.

La versión 1.1 del Estándar PCI DSS es la más reciente, publicada en septiembre de 2006. Está organizado en un conjunto de seis principios y doce requisitos complementarios. Cada requisito contiene requisitos secundarios para los que se debe implementar procesos, directivas o soluciones de tecnología para cumplir con el requisito. Las directivas y requisitos del Estándar PCI DSS incluyen:

-   Creación y mantenimiento de una red de seguridad

    -   Requisito 1: instalar y mantener una configuración de firewall para proteger los datos del titular de la tarjeta

    -   Requisito 2: no usar los valores predeterminados facilitados por el proveedor para las contraseñas de sistema y otros parámetros de seguridad

-   Protección de los datos del titular de la tarjeta

    -   Requisito 3: proteger los datos del titular de la tarjeta almacenados

    -   Requisito 4: cifrar la transmisión de los datos del titular de la tarjeta a través de redes abiertas y públicas

-   Uso de un programa de administración de vulnerabilidades

    -   Requisito 5: usar y actualizar regularmente software antivirus

    -   Requisito 6: desarrollar y mantener sistemas y aplicaciones de seguridad

-   Implementación de medidas de control de acceso seguro

    -   Requisito 7: limitar el acceso a los datos del titular de la tarjeta a las operaciones empresariales imprescindibles

    -   Requisito 8: asignar un identificador único a cada persona que tenga acceso al equipo

    -   Requisito 9: restringir el acceso físico a los datos del titular de la tarjeta

-   Control y prueba periódica de las redes

    -   Requisito 10: seguir y controlar los accesos a los recursos de la red y a los datos del titular la de tarjeta

    -   Requisito 11: probar regularmente los sistemas y procesos de seguridad

-   Mantenimiento de una directiva de seguridad de la información

    -   Requisito 12: mantener una directiva que controle la seguridad de la información

Los requisitos 9 y 12 no requieren la implementación de soluciones de tecnología. El requisito 9 le exige controlar la seguridad física de las ubicaciones en las que se almacenan y procesan los datos del titular de la tarjeta. Esto puede incluir implementar medidas de seguridad de acceso a los edificios, instalar y mantener un equipo de vigilancia y exigir comprobaciones de identidad para las personas que trabajan en las instalaciones o las visitan. El requisito 12 demanda la creación de una directiva de seguridad de la información y la difusión entre los empleados, proveedores y otras personas de la organización que trabajen con los datos del titular de la tarjeta.

#### Planeación para el cumplimiento del Estándar PCI DSS

La creación de soluciones aisladas para el cumplimiento del Estándar PCI DSS no resulta una solución eficaz ni económica. Existe una serie de normas que debe tener en cuenta a la hora de planear el enfoque que desea aplicar para cumplir los requisitos del Estándar PCI DSS. Entre otras, se incluyen las siguientes:

-   Normativa Sarbanes-Oxley (SOX)

-   Ley Gramm-Leach-Bliley (GLBA)

-   Ley de transferencia y responsabilidad de seguros de salud (HIPAA)

-   Directiva de Protección de Datos de la Unión Europea (EUDPD)

-   ISO 17799:2005, Código de buenas prácticas para la Gestión de la Seguridad de la Información (ISO 17799)

**Nota**   Si su organización es una empresa multinacional, deberá asegurarse de que cumple con las normas gubernamentales para todas las ubicaciones en las que desarrolla su actividad. Microsoft le recomienda que consulte a un asesor jurídico con conocimientos acerca de todas las normas aplicables a las ubicaciones en las que opera la organización.

Para obtener más información acerca de las labores de planeación para cumplir todas estas normas, consulte la [*Guía de planeación para el cumplimiento normativo*](http://www.microsoft.com/technet/security/guidance/complianceandpolicies/compliance/rcguide/default.mspx?mfr=true) (en inglés).

Las soluciones de cumplimiento del Estándar PCI DSS que la organización cree, se deben desarrollar teniendo en cuenta estas dos cuestiones:

-   Las soluciones ya existentes para satisfacer otros requisitos normativos;

-   Los métodos óptimos de crear soluciones nuevas que cumplan con los requisitos normativos.

Para alcanzar sus objetivos de cumplimiento de forma eficiente y eficaz, Microsoft le recomienda usar un marco de control que le ayude a administrar los objetivos de cumplimiento normativo de la organización. Mediante un marco de control, la organización puede asignar las normas y estándares aplicables al marco. La organización podrá entonces dedicar más eficazmente los controles de TI a los requisitos definidos en el marco, en lugar de las normas individuales.

Además, a medida que nuevas normas y estándares afecten a la organización, podrá asignarlos al marco y concentrar sus esfuerzos en aquellas secciones del marco en las que los requisitos hayan cambiado. Asimismo, puede asignar al marco una amplia variedad de requisitos relacionados con los controles de TI, incluidos requisitos específicos del sector, como los requisitos de seguridad de la industria de tarjetas de pago, las directivas internas, etc.

Un marco presenta ventajas importantes para las organizaciones que desean cumplir sus objetivos de cumplimiento normativo. El enfoque de cumplimiento normativo basado en el marco permite a las organizaciones:

-   Combinar los controles de TI para cumplir con varios estándares normativos, como los del Estándar PCI DSS y EUDPD, con lo que se evitan auditorías separadas;

-   Tratar las nuevas normas con eficacia en cuanto son introducidas;

-   Dar prioridad a los gastos mediante la elección de los controles de TI con mayor impacto;

-   Evitar la repetición del trabajo para cumplir los objetivos de cumplimiento en distintos departamentos de la compañía;

-   Actualizar las normas actuales de forma más eficaz mediante la realización de cambios incrementales en los controles de TI existentes en la organización;

-   Establecer una base común para el departamento de TI y los auditores.

Por supuesto, deberá revisar también el Estándar PCI DSS cuando comience a planear las labores de cumplimiento. Puede descargar el Estándar PCI DSS en <https://www.pcisecuritystandards.org/pdfs/pci_dss_v1-1.pdf> (en inglés). Por otra parte, el organismo PCI Security Standards Council ha creado un cuestionario de autoevaluación que puede ayudar a su organización a determinar si cumple con el Estándar PCI DSS. También puede ayudarle a planear las labores de cumplimiento del Estándar PCI DSS de la organización. Puede descargar el cuestionario de autoevaluación del Estándar PCI DSS en <https://www.pcisecuritystandards.org/pdfs/pci_saq_v1-0.pdf> (en inglés).

Para obtener más información acerca del tratamiento de los requisitos normativos mediante los controles de TI en un marco de control, consulte la [*Guía de planeación para el cumplimiento normativo*](http://www.microsoft.com/technet/security/guidance/complianceandpolicies/compliance/rcguide/default.mspx?mfr=true) (en inglés).

#### Proceso de auditoría del Estándar PCI DSS

El proceso de auditoría para cumplir el Estándar PCI DSS es, por norma general, parecido al proceso descrito en la [*Guía de planeación para el cumplimiento normativo*](http://www.microsoft.com/technet/security/guidance/complianceandpolicies/compliance/rcguide/default.mspx?mfr=true) (en inglés). Sin embargo, hay algunos detalles específicos de la auditoría del Estándar PCI DSS que debe conocer.

Los análisis de auditoría los realizan dos tipos de organizaciones de terceros, conocidas como evaluadores de seguridad calificados (QSA, *Qualified Security Assessors*) y proveedores de servicios de escaneo aprobados (ASV, *Approved Scanning Vendors*). Los evaluadores QSA realizan la parte in situ de la auditoría, mientras que los proveedores ASV realizan los exámenes de vulnerabilidad en los entornos de Internet de la organización. El organismo PCI Data Security Council (PCI DSC) se encarga de la evaluación anual de las empresas que se convierten en QSA o ASV para su certificación correspondiente.

El evaluador QSA es necesario para preparar un informe posterior a la auditoría de la organización; este informe debe seguir unas directrices concretas definidas por el PCI DSC. Estas directrices se encuentran en un documento con procedimientos de auditoría de PCI que puede descargar en <https://www.pcisecuritystandards.org/pdfs/pci_audit_procedures_v1-1.pdf> (en inglés). Las directrices especifican la forma en que se debe organizar el informe que el evaluador QSA debe archivar después de la auditoría. Este informe incluye información de contacto de la organización, la fecha de la auditoría, un resumen ejecutivo, una descripción del ámbito de trabajo y el enfoque que adoptó el evaluador QSA para realizar la auditoría en la organización, resultados trimestrales del examen, y los hallazgos y las observaciones del evaluador QSA. La última sección contiene la mayor parte de la información acerca del cumplimiento del Estándar PCI DSS de la organización. En ella, el evaluador QSA usa una plantilla para informar acerca del cumplimiento de cada uno de los requisitos principales y secundarios del Estándar PCI DSS por parte de la organización.

Antes de programar las auditorías del Estándar PCI DSS para la organización, o mejor, a medida que planea el cumplimiento del Estándar PCI DSS, los miembros clave de la organización deben revisar los procedimientos de auditoría específicos. Esta medida le puede ayudar a comprender completamente lo que analiza el evaluador QSA durante la auditoría.

El proveedor ASV también debe preparar un informe acerca de los resultados de los exámenes de vulnerabilidad realizados en los entornos de Internet de la organización. Las directrices para la creación de este informe se encuentran en un documento de procedimientos para el examen PCI, que se puede descargar en <https://www.pcisecuritystandards.org/pdfs/pci_scanning_procedures_v1-1.pdf> (en inglés). Este documento especifica los elementos que el proveedor ASV debe examinar en el entorno de la organización e incluye una clave que ayudará a leer e interpretar el informe del proveedor ASV.

Como comerciante o proveedor de servicios, deberá seguir cada requisito del informe de cumplimiento de las respectivas compañías de tarjetas de pago para asegurarse de que cada una de estas compañías es consciente del estado de cumplimiento de su organización. Con otras palabras, si su organización es un proveedor de servicios que administra datos de titulares de tarjetas Visa y American Express, debe enviar los informes de cumplimiento a Visa y a American Express.

Cada compañía de tarjetas de pago tiene reglas y procedimientos de cumplimiento ligeramente diferentes. Para obtener más información acerca de los requisitos de cumplimiento concretos del Estándar PCI DSS y de los programas de respaldo que cada compañía ofrece para habilitar el cumplimiento del comerciante o proveedor de servicios, póngase en contacto con las compañías de tarjetas de pago para las que la organización procesa, transmite o almacena datos de titulares de tarjetas.

[![](images/Bb821241.arrow_px_up(es-es,TechNet.10).gif)](#mainsection)[Top Of Page](#mainsection)

### Cumplimiento de los requisitos del Estándar PCI DSS

En esta sección, se detallan las soluciones de tecnología de Microsoft que la organización puede tener en cuenta a la hora de planear el cumplimiento del Estándar PCI DSS. Debe incorporar las soluciones seleccionadas a las labores cotidianas de la organización. Como se ha mencionado en la sección Planeación para el cumplimiento del Estándar PCI DSS, las directivas corporativas, los procedimientos y las soluciones de tecnología deben tener en cuenta el cumplimiento para toda la organización, por lo que deberá plantearse la forma en que el cumplimiento del Estándar PCI DSS afectará a los distintos departamentos de la compañía.

Para consultar un análisis más detallado de las consideraciones implicadas en la asignación de controles de TI a soluciones de tecnología, consulte la [*Guía de planeación de cumplimiento normativo*](http://www.microsoft.com/technet/security/guidance/complianceandpolicies/compliance/rcguide/default.mspx?mfr=true) (en inglés).

#### Administración de documentos

Las soluciones de administración de documentos combinan el software y una serie de procesos para facilitar la administración de información sin estructurar de la organización. Esta información puede estar contenida en distintos formatos digitales, incluidos documentos, imágenes, archivos de audio y vídeo, y archivos XML.

##### Cumplimiento de los requisitos del Estándar PCI DSS

La implementación de las soluciones de administración de documentos facilita el cumplimiento del Estándar PCI DSS de dos formas. En primer lugar, al usar estas soluciones para administrar documentos que contienen datos de titulares de tarjetas, se facilita el cumplimiento de los requisitos del Estándar PCI DSS relacionados con el acceso, la administración y la protección de los datos. En concreto, puede usar las soluciones de administración de documentos para cumplir con el requisito 7 y el requisito secundario 10.2.1. En segundo lugar, puede usar los sistemas de administración de documentos para mantener y publicar directivas como las requeridas para cumplir con las secciones 3.6, 6.4, 9.2 y 12.

Para obtener el texto completo de cualquiera de estos requisitos, consulte el [*Estándar de seguridad de datos en la industria de tarjetas de pago,* *versión 1.1.*](https://www.pcisecuritystandards.org/pdfs/pci_dss_v1-1.pdf) (en inglés).

##### Tecnologías disponibles

Microsoft ofrece una serie de tecnologías que se pueden usar de forma conjunta e individual con objeto de crear controles de TI para la administración de documentos. Deberá diseñar estos controles para cumplir con los requisitos del Estándar PCI DSS, así como con cualquier otro requisito normativo que sea aplicable a su organización.

-   **Servicios de Microsoft® Windows® Rights Management**: los Servicios de Microsoft Windows Rights Management (RMS) ofrecen una plataforma de software que ayuda a que las aplicaciones protejan la información digital del uso no autorizado (tanto en línea como sin conexión, fuera y dentro del firewall). RMS es la tecnología base que está detrás de las características de Information Rights Management (IRM) de Microsoft Office y Windows SharePoint® Services. Para usar estas características, es necesario un servidor RMS, implementado de forma interna o accesible desde un servicio de host.

    RMS puede mejorar la estrategia de seguridad de la organización mediante la protección de la información a través de directivas de uso persistentes, que se mantienen con la información independientemente de donde esta vaya. Las aplicaciones con tecnología RMS habilitada se pueden usar para administrar, controlar y auditar el acceso a los documentos que contienen información del titular de la tarjeta. El cliente RMS está integrado en el sistema operativo de Windows Vista™. Para otras versiones de Windows, el cliente RMS está disponible como descarga gratuita.
    Para obtener más información, consulte [*Servicios de Microsoft Windows Rights Management*](http://www.microsoft.com/rms) (en inglés) en <http://www.microsoft.com/rms>.

-   **Microsoft Office SharePoint Server**: SharePoint Server es un servidor de colaboración y administración de contenido que le permite tener una plataforma integrada compatible con el portal y las necesidades de administración de documentos de su organización. Le brinda compatibilidad con aplicaciones web, de extranet e intranet para toda la empresa, y proporciona a los profesionales de TI y a los desarrolladores la plataforma y las herramientas que necesitan para la administración del servidor, las posibilidades de ampliación de la aplicación y la interoperabilidad. SharePoint Server se puede usar como repositorio central para documentos con datos de titulares de tarjetas, así como para documentos que describen directivas y procesos. SharePoint Server 2007 está integrado con RMS, de modo que las directivas de control se pueden aplicar en todas las copias del contenido descargado desde SharePoint Server 2007. Esta característica permite que todos los administradores de sitio protejan las descargas desde una biblioteca de documentos con IRM. Cuando un usuario intenta descargar un archivo desde una biblioteca, Microsoft Windows SharePoint Services comprueba que el usuario tenga los permisos necesarios para el archivo concreto y emite una licencia para el usuario que permite el acceso al archivo en función del nivel de permiso correspondiente. A continuación, Windows SharePoint Services descarga el archivo en el equipo del usuario en un formato de archivo cifrado y administrado a partir de derechos.
    Para obtener más información, consulte el sitio web [*Productos y tecnologías de Microsoft SharePoint*](http://go.microsoft.com/fwlink/?linkid=12632) (en inglés) en <http://go.microsoft.com/fwlink/?linkid=12632>.

-   **Microsoft Exchange Server**: hoy día, muchos negocios consideran el correo electrónico como la herramienta de comunicación fundamental que los empleados deben usar para obtener resultados óptimos. Esta gran confianza depositada en el correo electrónico ha aumentado el número de mensajes enviados y recibidos, la cantidad y variedad de los trabajos realizados a través del correo electrónico e incluso ha acelerado el ritmo en que se desarrolla el propio negocio. Exchange Server proporciona una plataforma de mensajería completa para la administración del intercambio de información en la organización, a la vez que facilita el cumplimiento de los objetivos relacionados con el Estándar PCI DSS. Exchange Server 2007 incluye servicios de mensajería unificada, que compila el correo electrónico, correo de voz y fax que se envía a un usuario en una única bandeja de entrada. Ofrece además características que permiten a la organización aplicar reglas de retención, funciones de detección e intervención en mensajes en curso, diario flexible y búsquedas de texto enriquecido en todos los buzones implementados.
    Para obtener más información, consulte el sitio web de Microsoft Exchange Server (en inglés) en <http://www.microsoft.com/exchange/default.mspx>.

-   **Microsoft Office**: Office es un conjunto primordial de aplicaciones de productividad para las empresas. La característica IRM de Microsoft Office ayuda a que las organizaciones controlen el acceso a información confidencial, como los datos del titular de la tarjeta.

    En concreto, la característica IRM de Office ayuda a la organización de las siguientes formas:

    -   Evita que un destinatario con acceso a la información protegida reenvíe, copie, modifique, imprima, envíe faxes o corte y pegue la información para su uso sin autorización.

    -   Evita que la información protegida se copie mediante la función de Windows Imprimir pantalla.

    -   Proporciona información con el mismo nivel de protección a donde esta se envíe. Esta característica conforma la denominada *protección persistente*.

    -   Proporciona el mismo nivel de protección a los datos adjuntos de correo electrónico, siempre que estos sean archivos creados con otros programas de Office, como Microsoft Excel® o Microsoft Word.

    -   Protege la información contenida en los mensajes de correo electrónico o documentos con fecha de expiración, de modo que la información no se pueda ver hasta pasado un período de tiempo determinado.

    -   Aplica las directivas corporativas que determinan el uso y difusión de la información dentro y fuera de la compañía.

#### Evaluación de riesgos

La evaluación de riesgos es el proceso mediante el cual la organización identifica y establece las prioridades de los riesgos del negocio. Por norma general, se usa un método sistemático para identificar los activos de un sistema de procesamiento de la información, las amenazas para dichos activos y la vulnerabilidad del sistema antes tales amenazas. Desde la perspectiva del cumplimiento normativo, la evaluación de riesgos es el proceso de evaluación del nivel de cumplimiento y las deficiencias de cumplimiento de la organización. Cuando se planea el cumplimiento del Estándar PCI DSS, lo principal es identificar los riesgos para los datos del titular de la tarjeta y establecer las prioridades de esas amenazas.

##### Cumplimiento de los requisitos del Estándar PCI DSS

La evaluación de riesgos le puede ayudar a cumplir con los requisitos del Estándar PCI DSS de distintas formas. Le permite identificar las áreas de su red que necesitan una actualización para el cumplimiento. Incluso después de haber alcanzado un cumplimiento inicial, la evaluación de riegos es importante para determinar si la organización sigue cumpliendo con los requisitos después de un período de tiempo. Puesto que puede usar la evaluación de riesgos para tratar una serie de posibles problemas, le puede ayudar a cumplir muchos de los requisitos del Estándar PCI DSS, incluidos los números 1, 3, 4, 5, 6, 7, 8 y 11.

Para obtener el texto completo de cualquiera de estos requisitos, consulte el [*Estándar de seguridad de datos en la industria de tarjetas de pago,* *versión 1.1.*](https://www.pcisecuritystandards.org/pdfs/pci_dss_v1-1.pdf) (en inglés).

##### Tecnologías disponibles

Microsoft ofrece una serie de tecnologías que se pueden usar de forma conjunta e individual para crear controles de TI para la evaluación de riegos. Deberá diseñar estos controles para cumplir con los requisitos del Estándar PCI DSS, así como cualquier otro requisito normativo que sea aplicable a su organización.

<ul>
<li>
**Microsoft Baseline Security Analyzer (MBSA)**: una de las herramientas principales que puede usar para evaluar los riesgos de los datos de los titulares de tarjetas en la organización es MBSA. Se trata de una herramienta fácil de usar que identifica configuraciones incorrectas de seguridad comunes en una serie de productos de Microsoft, incluidos los sistemas operativos de Microsoft Windows, Internet Information Services (IIS), SQL Server™, Microsoft Internet Explorer® y Microsoft Office. MBSA también detecta las actualizaciones de seguridad, los paquetes acumulativos de actualizaciones y los service packs que faltan con respecto a los publicados en Microsoft Update. Puede ejecutar MBSA desde el símbolo del sistema o en la GUI, así como usarlo con Microsoft Update y Microsoft Windows Server® Update Services. Dado que mantener los sistemas actualizados es una tarea muy importante para proteger los datos de titulares de tarjetas tanto como sea posible, MBSA se puede mostrar como una herramienta irremplazable para la evaluación de los riegos para los datos de la organización.

</li>
Para obtener más información acerca de MBSA, consulte el artículo sobre Microsoft Baseline Security Analyzer (en inglés) en <http://www.microsoft.com/technet/security/tools/mbsahome.mspx>.

<li>
**Microsoft Systems Management Server**: si su organización usa Microsoft Systems Management Server (SMS) para administrar los equipos cliente y servidores, es posible que ya cuente con algunas de las herramientas necesarias para realizar la evaluación de riesgos para los datos de titulares de tarjetas. Con SMS, la organización puede administrar de forma remota la configuración de seguridad de los equipos que ejecutan sistemas operativos de Windows a través de redes distribuidas. Puede realizar un inventario de los equipos de la red que tienen instaladas las actualizaciones de software obligatorias y seguir el progreso de la instalación de actualizaciones en dichos equipos. SMS también le permite generar informes que identifiquen el inventario completo de hardware y software, los detalles de configuración y el estado de los equipos de su red, así como el estado de las implementaciones de software y los errores de implementación. Estas características de SMS pueden ser muy importantes para la evaluación de riesgos para los datos de titulares de tarjetas dentro de la organización.

</li>
Para obtener más información acerca de SMS, consulte la página principal de Microsoft Systems Management Server (en inglés) en <http://www.microsoft.com/smserver/default.mspx>.

<li>
**Recopilación de auditorías de Microsoft System Center Operations Manager**: Operations Manager 2007 puede extraer y recopilar de forma segura y eficaz los registros de seguridad de sistemas operativos de Windows y almacenarlos para su análisis y notificación posterior. Los registros extraídos se almacenan en una base de datos de recopilación de auditorías independiente. Operations Manager enviará los informes que se pueden usar para los datos de la recopilación de auditorías. La recopilación de auditorías se puede usar para generar distintos informes de cumplimiento, como las auditorías de la normativa Sarbanes-Oxley. La recopilación de auditorías se puede usar también para los análisis de seguridad, como la detección de intrusiones y los intentos de acceso no autorizado.

</li>
Para obtener más información, consulte el artículo sobre Audit Collection Services (en inglés) en <http://technet.microsoft.com/en-us/library/bb381258.aspx>.

<li>
**Windows Server Update Services**:** **Windows Server Update Services (WSUS) con Service Pack 1 permite a la organización implementar muchas de las últimas actualizaciones de productos de Microsoft publicadas en el sitio de Microsoft Update. Windows Server Update Services es un componente de actualización de Windows Server que presenta una forma rápida y eficaz de ayudar a mantener los sistemas actualizados. WSUS ofrece una infraestructura de evaluación de riesgos que consta de lo siguiente:

-   **Microsoft Update**: el sitio web de Microsoft al que se conectan los componentes de WSUS para las actualizaciones de los productos de Microsoft

-   **Servidor de Windows Server Update Services**: el componente servidor instalado en un equipo que ejecuta un sistema operativo Microsoft Windows 2000 Server con Service Pack 4 (SP4) o Windows Server 2003 en el firewall corporativo. El servidor de Windows Server Update Services ofrece características que los administradores necesitan para administrar y distribuir las actualizaciones a través de una herramienta basada en Internet, a la que se puede tener acceso desde Internet Explorer en cualquier equipo de Windows de la red corporativa. Asimismo, un servidor de Windows Server Update Services puede ser el origen de actualización para los servidores de Windows Server Update Services.

-   **Actualizaciones automáticas**: el componente de equipo cliente integrado en los sistemas operativos Microsoft Windows Vista, Windows Server 2003, Windows XP y Windows 2000 con Service Pack 3. Este componente facilita al servidor y a los equipos cliente recibir actualizaciones de Microsoft Update o de un servidor que ejecute Windows Server Update Services.

</li>
Estos servicios le permiten ofrecer todos los entornos de host en la red con las últimas correcciones de seguridad de Microsoft para los productos instalados en un host determinado.

Para obtener más información, consulte la página principal de Windows Server Update Services (en inglés) en <http://www.microsoft.com/windowsserversystem/updateservices/default.mspx>.

<li>
**Directiva de grupo**: la directiva de grupo es una infraestructura que permite a los profesionales de TI implementar parámetros concretos a usuarios y equipos. Los parámetros de directiva de grupo están contenidos en los objetos de directiva de grupo (GPO), que a su vez están vinculados a los siguientes contenedores de servicios de directorio de Microsoft Active Directory®: sitios, dominios o unidades organizativas. Puede administrar de forma centralizada los equipos a través de la red distribuida mediante una directiva de grupo. Puesto que los administradores pueden usar una directiva de grupo para distribuir el software en un sitio, dominio o una serie de unidades organizativas, puede mostrarse como una herramienta importante para determinar los posibles riesgos del entorno de TI de la organización.

</li>
Puede usar la Consola de administración de directivas de grupo de Microsoft (GPMC) para administrar los parámetros de directiva de grupo. La consola GPMC está diseñada para simplificar la administración de directivas de grupo al brindar un único sitio para administrar los puntos principales de tales directivas. GPMC administra los requisitos de implementación de las directivas de grupo, en función de lo que soliciten los clientes, mediante los siguientes elementos:

-   Una interfaz de usuario (UI) que facilita el uso de las directivas de grupo;

-   La capacidad de crear copias de seguridad de los GPO y restaurarlos;

-   La capacidad de importar y exportar, así como de copiar y pegar los GPO y los filtros de Instrumental de administración de Windows (WMI);

-   Una forma simplificada de administrar los aspectos de seguridad relacionados con la directiva de grupo;

-   La capacidad de generar informes HTML para los parámetros de GPO y los datos del Conjunto resultante de directivas (RSoP);

-   La capacidad de realizar script de las operaciones de GPO expuestas por la GPMC (sin la funcionalidad para realizar scripts de los parámetros de un GPO).

Para obtener más información, consulte la directiva de grupo de Windows Server 2003 (en inglés) en <http://technet2.microsoft.com/windowsserver/en/technologies/featured/gp/default.mspx> e *Introducción a la Consola de administración de directivas de grupo* (en inglés) en <http://www.microsoft.com/windowsserver2003/gpmc/gpmcintro.mspx>.

</ul>
#### Administración de cambios

La administración de cambios es un proceso estructurado por el que la organización evalúa los cambios realizados en un plan del proyecto, una infraestructura de TI, las implementaciones de software u otros procesos y procedimientos realizados en la organización. Un sistema de administración de cambios puede ayudar a definir un cambio, evaluar el efecto del mismo, determinar las acciones necesarias para implementarlo y difundir la información relacionada a través de la organización. También le puede ayuda a seguir los cambios realizados en la organización. Esto le permite controlar el entorno de TI a medida que realiza los cambios.

Por ejemplo, el sistema para una organización puede incluir una base de datos para ayudar a que los empleados tomen decisiones más acertadas acerca de los cambios futuros en función de datos anteriores que indiquen el éxito o el fracaso de cambios similares realizados en el pasado. La administración de cambios también es un proceso estructurado que informa acerca de la existencia y el estado de los cambios que afectan a todas las partes implicadas. El proceso puede generar un sistema de inventario que indique las acciones emprendidas y el momento en que dichas acciones afectaron al estado de los recursos clave, para ayudar a prever y eliminar los problemas, y a simplificar la administración de recursos.

##### Cumplimiento de los requisitos del Estándar PCI DSS

La administración de cambios es tan esencial para el cumplimiento del Estándar PCI DSS como para cualquier otra labor de cumplimiento normativo. Si la organización no conoce los cambios realizados en el entorno de TI, será difícil afirmar con rotundidad que el entorno es seguro. El seguimiento de los cambios realizados en la red, los sistemas, las directivas y los procedimientos ayudará a cumplir con los requisitos 6 y 11 del Estándar PCI DSS.

Para obtener el texto completo de cualquiera de estos requisitos, consulte el [*Estándar de seguridad de datos en la industria de tarjetas de pago,* *versión 1.1.*](https://www.pcisecuritystandards.org/pdfs/pci_dss_v1-1.pdf) (en inglés).

##### Tecnologías disponibles

Microsoft le ofrece una serie de tecnologías a tener en cuenta cuando diseñe las soluciones de administración de cambios.

-   **Microsoft Office SharePoint Server**: además de ser una opción de tecnología para las soluciones de administración de documentos, Microsoft Office SharePoint Server puede ser también un elemento clave en el sistema de administración de cambios de la organización. Puede usar las funciones de seguimiento de versión para controlar los cambios realizados en documentos de directivas y procesos, actualizaciones y otros cambios realizados en las aplicaciones, así como cambios realizados a lo largo del tiempo en el software aprobado.

-   **Microsoft Systems Management Server**: no sólo puede usar SMS para administrar la evaluación de riesgos de la organización, sino que también puede recurrir a sus características de administración para seguir los cambios realizados en los sistemas de los equipos de la organización. SMS realizará un seguimiento de los cambios realizados en la configuración de seguridad, así como las aplicaciones instaladas en los servidores y equipos cliente de toda la red. Asimismo, puede usar la eficaz funcionalidad de informe integrada en SMS para revisar los cambios realizados en los equipos de la organización y si dichos cambios cumplen con los requisitos de seguridad que ha establecido.

-   **Microsoft SMS 2003 Desired Configuration Monitoring 2.0**: puede aumentar las operaciones de SMS con la característica SMS 2003 Desired Configuration Monitoring (DCM). Puede usar DCM para automatizar las auditorías de administración de configuración entre los parámetros de configuración deseados o definidos y los parámetros de configuración reales. DCM realiza esta función al permitir al usuario definir los parámetros de configuración deseados para hardware, sistema operativo y aplicación en varios orígenes de datos de configuración. A continuación, mediante el motor de auditoría facilitado, DCM compara los parámetros deseados con los reales e informa acerca del cumplimiento de la configuración.

-   **Microsoft Desktop Optimization Pack for Software Assurance**: Microsoft Desktop Optimization Pack for Software Assurance es un servicio de suscripción que reduce los costos de implementación de aplicaciones, permite la entrega de aplicaciones como servicios y ofrece una mejor administración y control de los entornos de escritorio de la empresa. Este paquete de optimización de escritorio le permite mejorar los procesos de administración de cambios y las reversiones mediante los siguientes elementos:

    -   Mejora en la administración de directivas de grupo;

    -   Menor tiempo de inactividad;

    -   Acceso a petición a las aplicaciones para los usuarios aprobados.

#### Seguridad de red

Las soluciones de seguridad de red constituyen una amplia categoría de soluciones diseñadas para tratar la seguridad de todos los aspectos de la red de una organización, incluidos firewalls, servidores, clientes, enrutadores, conmutadores y puntos de acceso. La planeación y el control de la seguridad de las redes de su organización constituyen un elemento clave en la consecución del cumplimiento del Estándar PCI DSS. Aunque existe una amplia variedad de soluciones disponibles para administrar la seguridad de red, su organización debe tener ya muchos de los elementos de una red segura por norma. Probablemente, sea más eficaz y económico partir de las soluciones de seguridad de red que ya tiene implementadas en lugar de comenzar desde el principio.

Sin embargo, puede estar pensando en realizar un cambio en alguna de las tecnologías que usa su organización, o bien, es posible que desee implementar nuevas soluciones que no ha incluido aún en la estrategia de seguridad de red. Microsoft le ofrece una serie de soluciones de tecnología y material orientativo para implementar soluciones de seguridad de red que cubran las necesidades de su organización.

##### Cumplimiento de los requisitos del Estándar PCI DSS

El Estándar de seguridad de datos en la industria de tarjetas de pago indica claramente que necesita establecer redes seguras en toda la organización para cumplir con los requisitos. La directiva 1 indica que para cumplir con los requisitos, una organización debe crear y mantener una red segura. El requisito 1 indica que las organizaciones deben instalar y mantener una configuración de firewall para proteger los datos de los titulares de tarjetas. El requisito 2 indica que las organizaciones deben cambiar la configuración predeterminada del proveedor para las contraseñas de sistema y otros parámetros de seguridad. Las soluciones de seguridad de red también facilitan que su organización cumpla con los requisitos 4 y 11, que exigen el cifrado de las transmisiones de los datos de los titulares de tarjetas a través de la red, además del seguimiento y control del acceso a la red, respectivamente.

Para obtener el texto completo de cualquiera de estos requisitos, consulte el [*Estándar de seguridad de datos en la industria de tarjetas de pago,* *versión 1.1.*](https://www.pcisecuritystandards.org/pdfs/pci_dss_v1-1.pdf) (en inglés).

##### Tecnologías disponibles

Microsoft le ofrece una serie de tecnologías para cumplir con los dos primeros requisitos del Estándar PCI DSS.

-   **Firewall de Microsoft Windows**: Windows XP Service Pack 2 (SP2) incluye Firewall de Windows, que reemplaza al Servidor de seguridad de conexión a Internet (ICF). Firewall de Windows es un firewall con estado basado en host que omite el tráfico entrante no solicitado que no se corresponde con el tráfico enviado en respuesta a una solicitud del equipo (tráfico solicitado) ni con el tráfico no solicitado especificado como permitido (tráfico excepcional). Firewall de Windows proporciona un nivel de protección ante usuarios y programas malintencionados que confían en tráfico entrante no solicitado para atacar los equipos de una red. Estas características se han mejorado en Firewall de Windows con seguridad avanzada en Windows Vista y Windows Server “Longhorn”.

-   **Microsoft Internet Security and Acceleration Server**: Microsoft Internet Security and Acceleration (ISA) Server le puede ayudar a proteger su red de distintas formas. En primer lugar, puede usarlo para permitir a los usuarios el acceso remoto a las aplicaciones corporativas a través de Internet. Para ello, puede configurar ISA Server para autenticar previamente las solicitudes de usuarios entrantes, inspeccionar todo el tráfico en el nivel de aplicaciones (incluido el tráfico cifrado) y proporcionar herramientas de publicación automatizadas. En segundo lugar, si su organización incluye sucursales, ISA Server le permite usar las funciones de compresión HTTP, almacenamiento en caché del contenido y la red privada virtual (VPN) para ampliar su red de forma fácil y segura. En tercer lugar, con ISA Server puede proteger su red de las amenazas de Internet internas y externas. Para ello, se usa la arquitectura proxy-firewall, las funciones de inspección de contenido, la configuración granular de directivas, así como las funciones completas de alerta y control.

-   **Aislamiento de servidor y dominio mediante el protocolo de seguridad de Internet (IPsec) y la directiva de seguridad de Active Directory:** el aislamiento de servidor y dominio crea un nivel de protección íntegro que puede reducir considerablemente el riesgo de ataques malintencionados y de acceso no autorizado a los recursos en red. A partir de Windows IPsec y de la directiva de grupo de Active Directory, esta solución le permite segmentar de forma dinámica su entorno de Windows en redes lógicas y aisladas más seguras. Son varios los métodos para crear una red aislada, por lo que tiene flexibilidad para aislar de forma lógica todo un dominio administrado o crear redes virtuales de determinados servidores más seguras, con lo que limita el acceso a los usuarios autenticados y autorizados, o requiere que los servidores o redes concretos protejan todos los datos mediante el cifrado. Al requerir el cifrado de datos para el tráfico intercambiado entre las submáscaras de red y los hosts de red específicos, puede cumplir con los requisitos normativos y de socios empresariales para cifrar datos cuando estos pasen por una red.

-   **Asistente para configuración de seguridad de Windows Server 2003**: el Asistente para configuración de seguridad puede ayudarle a proteger la red mediante la reducción de la superficie de ataque de los servidores que ejecutan Windows Server 2003, Service Pack 1. El Asistente para configuración de seguridad determina la funcionalidad mínima necesaria para las funciones de un servidor y deshabilita la funcionalidad que no es necesaria. En concreto, el Asistente para configuración de seguridad:

    -   deshabilita los servicios innecesarios;

    -   bloquea los puertos que no se usan;

    -   permite más restricciones de direcciones o de seguridad para puertos que se han dejado abiertos;

    -   prohíbe extensiones web de IIS innecesarias, si procede;

    -   reduce la exposición de protocolo en bloques de mensaje del servidor (SMB), LanMan y Protocolo ligero de acceso a directorios (LDAP);

    -   define una directiva de auditoría con una elevada relación señal-ruido.

-   **Conexión a escritorio remoto mediante la autenticación de servidor**: las conexiones a escritorio remoto son una forma eficaz de permitir a los usuarios tener acceso a los equipos cliente y servidores compartidos. Esta tecnología puede ser una forma económica de crear un desarrollo y unos equipos de prueba compartidos. Por otro lado, puede usar estos equipos como puntos de acceso centralizados para muchos tipos de proyectos, así como permitir a los usuarios externos a la red tener acceso a estos equipos, con lo que se aíslan los riesgos que suponen para la seguridad de la red. Además, la actualización del cliente Conexión a Escritorio remoto 6.0 permite a los profesionales de TI configurar la autenticación del servidor. Con la autenticación del servidor, puede evitar que los usuarios se conecten a un equipo o servidor que no sea el deseado y la exposición potencial de información confidencial. Microsoft introduce esta característica en Windows Vista y Windows Server “Longhorn”. El cliente Conexión a Escritorio remoto 6.0 se puede usar en otros equipos que ejecutan Windows Server 2003 con Service Pack 1 o Windows XP con Service Pack 2 (SP2). El cliente se puede usar para conectarse a servidores de Terminal Services heredados o a escritorios remotos como anteriormente, pero la autenticación de servidor sólo se produce cuando el equipo remoto ejecuta Windows Vista o Windows Server “Longhorn”.

-   **Acceso protegido Wi-Fi 2**: si su organización usa una red inalámbrica, debe reflexionar acerca de la actualización a enrutadores inalámbricos, puntos de acceso y otros dispositivos compatibles con la certificación de producto de Acceso protegido Wi-Fi 2 (WPA2). WPA2 es una certificación de producto que otorga Wi-Fi Alliance y certifica que los equipos inalámbricos son compatibles con el estándar IEEE 802.11i. El objetivo de la certificación WPA2 es ser compatible con otras características de seguridad obligatorias del estándar IEEE 802.11i que todavía no está incluido para los productos compatibles con WPA. Por ejemplo, WPA2 requiere compatibilidad para el cifrado TKPI y AES. WPA2 está disponible en dos modos diferentes:

    -   WPA2-Enterprise usa la autenticación 802.1X y está diseñado para redes con infraestructuras medianas y grandes;

    -   WPA2-Personal usa una PSK para la autenticación y está diseñado para redes con infraestructura SOHO.

-   **Protección de acceso a redes**: la Protección de acceso a redes (NAP) es una plataforma para Windows Server “Longhorn” y Windows Vista. Proporciona componentes de aplicación de directivas que ayudan a garantizar que los equipos conectados a una red o que se comunican a través de una red cumplen con los requisitos definidos por el administrador para el mantenimiento del sistema. Su organización puede emplear una combinación de los componentes de validación de directivas y de limitación de acceso a red para controlar el acceso o la comunicación entre redes. También se puede decidir por limitar temporalmente el acceso a una red restringida a los equipos que no cumplan con los requisitos. En función de la configuración seleccionada, la red restringida puede contener recursos necesarios para la actualización de los equipos para que estos cumplan con los requisitos de mantenimiento para un acceso a redes sin límite y una comunicación normal. NAP incluye una interfaz de programación de aplicaciones (API) definida por desarrolladores y proveedores para crear soluciones completas para la validación de directivas de estado, la limitación de acceso a redes y el cumplimiento continuo de las condiciones de estado. NAP ofrece componentes de aplicación de acceso limitado para IPsec, conexiones de red autenticadas con el estándar IEEE 802.1X, redes VPN y Protocolo de configuración dinámica de host (DCHP). Puede usar estas tecnologías de forma conjunta o individual. Con estas funciones, NAP puede ser una herramienta eficaz para facilitarle la protección del estado y la seguridad de la red.

-   **Microsoft Virtual Server**: Microsoft Virtual Server 2005 R2 proporciona una plataforma de virtualización que ejecuta la mayoría de los sistemas operativos x86 en un entorno de invitado. Es compatible con Microsoft en calidad de host para los sistemas operativos Windows Server y las aplicaciones Windows Server System. Su integración con una amplia variedad de herramientas de administración de Microsoft y de terceros permite a los administradores administrar a la perfección un entorno de Virtual Server 2005 R2 con las herramientas de administración de los servidores físicos existentes. Puesto que Microsoft Virtual Server permite a la organización ejecutar varios sistemas operativos en un equipo, puede ayudarle a cumplir con el requisito 2.2.1 del Estándar PCI DSS que exige que la organización sólo ejecute una función principal por servidor. Por ejemplo, puede usar Virtual Server para implementar un servidor web virtual, un servidor de bases de datos virtual y un servidor de archivos virtual en el mismo equipo.

#### Control de host

Las soluciones de control de host controlan los sistemas operativos de servidores y estaciones de trabajo. Las soluciones de control de host también incluyen procedimientos recomendados para implementar la seguridad en todos los niveles del sistema operativo de cada host, a la vez que se mantienen las actualizaciones y revisiones más recientes y se usan métodos seguros para las operaciones diarias.

##### Cumplimiento de los requisitos del Estándar PCI DSS

Las soluciones de control de host pueden ayudarle a cumplir con los requisitos del Estándar PCI DSS mediante el mantenimiento de los sistemas operativos actualizados y configurados de forma segura. En concreto, el control de host puede ayudarle a cumplir con los requisitos 6 y 11 del Estándar PCI DSS.

Para obtener el texto completo de cualquiera de estos requisitos, consulte el [*Estándar de seguridad de datos en la industria de tarjetas de pago,* *versión 1.1.*](https://www.pcisecuritystandards.org/pdfs/pci_dss_v1-1.pdf) (en inglés).

##### Tecnologías disponibles

Microsoft le ofrece una serie de tecnologías que puede usar de forma conjunta o independiente para crear soluciones de control de host. Al igual que con otras soluciones de tecnología, deberá diseñar estas soluciones para cumplir con los requisitos del Estándar PCI DSS, así como cualquier otro requisito normativo que sea aplicable a su organización.

-   **Microsoft Baseline Security Analyzer (MBSA)**: una de las herramientas principales que puede usar para evaluar los riesgos de los datos de los titulares de tarjetas en la organización es MBSA. MBSA es una herramienta fácil de usar que identifica configuraciones incorrectas de seguridad comunes en una serie de productos de Microsoft, incluidos el sistema operativo de Windows, Internet Information Services, SQL Server, Internet Explorer y Microsoft Office. MBSA también detecta las actualizaciones de seguridad, los paquetes acumulativos de actualizaciones y los service packs que faltan con respecto a los publicados en Microsoft Update. Puede ejecutar MBSA desde el símbolo del sistema o en una GUI, así como usarlo con Microsoft Update y Windows Server Update Services. Dado que mantener los sistemas actualizados es una tarea muy importante para proteger los datos de los titulares de tarjetas tanto como sea posible, MBSA se puede mostrar como una herramienta irremplazable para la evaluación de los riegos para los datos de la organización.

-   **Microsoft Windows Server Update Services**:** **Microsoft Windows Server Update Services (WSUS) con Service Pack 1 permite a la organización implementar muchas de las últimas actualizaciones de productos de Microsoft publicadas en el sitio de Microsoft Update. WSUS es un componente de actualización de Windows Server que le ofrece una forma rápida y eficaz de mantener actualizados los sistemas. WSUS ofrece una infraestructura de administración que consta de lo siguiente:

    -   **Microsoft Update**: el sitio web de Microsoft al que se conectan los componentes de WSUS para las actualizaciones de los productos de Microsoft.

    -   **Servidor de Windows Server Update Services**: el componente servidor que está instalado en un equipo que ejecuta un sistema operativo Microsoft Windows 2000 Server con Service Pack 4 (SP4) o Windows Server 2003 en el firewall corporativo. El servidor WSUS ofrece características que los administradores necesitan para administrar y distribuir las actualizaciones a través de una herramienta basada en Internet, a la que se puede tener acceso desde Internet Explorer en cualquier equipo de Windows de la red corporativa. Asimismo, un servidor WSUS puede ser el origen de actualización de otros servidores WSUS.

    -   **Actualizaciones automáticas**: el componente de equipo cliente integrado en los sistemas operativos Windows Vista, Windows Server 2003, Windows XP y Windows 2000 con SP3. Con Actualizaciones automáticas, el servidor y los equipos cliente pueden recibir actualizaciones desde Microsoft Update o desde un servidor que ejecute WSUS.

-   **Microsoft Systems Management Server**: si su organización usa SMS para administrar los equipos cliente y servidores, es posible que ya cuente con algunas de las herramientas necesarias para realizar la evaluación de riesgos para los datos de titulares de tarjeta. Con SMS, la organización puede administrar de forma remota la configuración de seguridad de los equipos que ejecutan sistemas operativos de Windows a través de redes distribuidas. Puede realizar un inventario de los equipos de la red que tienen instaladas las actualizaciones de software obligatorias y seguir el progreso de la instalación de actualizaciones en dichos equipos. SMS también le permite generar informes que identifiquen el inventario completo de hardware y software, los detalles de configuración y el estado de los equipos de su red, así como el estado de las implementaciones de software y los errores de implementación. Estas características de SMS pueden ser muy importantes para la evaluación de riesgos para los datos de titulares de tarjetas dentro de la organización.

-   **Microsoft Desktop Optimization Pack for Software Assurance**: Microsoft Desktop Optimization Pack for Software Assurance es un servicio de suscripción que reduce los costos de implementación de aplicaciones, permite la entrega de aplicaciones como servicios y ofrece una mejor administración y control de los entornos de escritorio de la empresa. El paquete de optimización de escritorio es una solución de control de host eficaz que le permite realizar las siguientes acciones:

    -   Simplificar y acelerar el ciclo de vida de administración de aplicaciones desde la planeación y la implementación previsible hasta el uso, el mantenimiento y la migración de software;

    -   Mejorar la administración de los activos de software de la organización;

    -   Acelerar y simplificar las implementaciones de escritorio y las migraciones.

#### Prevención de software malintencionado

Las soluciones de prevención de software malintencionado son elementos clave para mantener protegidos los datos de los titulares de tarjetas a través de la red. Al evitar el correo no deseado y mantener los sistemas sin virus ni spyware, estas soluciones pueden garantizar que los sistemas de la red trabajan al máximo de sus posibilidades y que la información confidencial no se transmite de forma no intencionada a partes no autorizadas.

##### Cumplimiento de los requisitos del Estándar PCI DSS

Las soluciones de prevención de software malintencionado que elija pueden ayudarle a cumplir con los requisitos 5 y 6 del Estándar PCI DSS.

Para obtener el texto completo de cualquiera de estos requisitos, consulte el [*Estándar de seguridad de datos en la industria de tarjetas de pago,* *versión 1.1.*](https://www.pcisecuritystandards.org/pdfs/pci_dss_v1-1.pdf) (en inglés).

##### Tecnologías disponibles

Microsoft le presenta una serie de tecnologías que puede usar de forma conjunta o individual para evitar el software malintencionado. Debe tener en cuenta estas tecnologías junto con las labores de cumplimiento del Estándar PCI DSS de mayor envergadura, así como los requisitos normativos más exigentes para la organización.

-   **Microsoft Forefront™**: Forefront es un conjunto de aplicaciones de productos de seguridad de línea de negocio que proporciona protección a los sistemas operativos cliente, los servidores de aplicaciones y la red al completo. Puede usar Forefront con la infraestructura de TI existente para proteger servidores y equipos cliente de malware y otros ataques malintencionados que se originen dentro o fuera de la organización.

-   **Herramienta de eliminación de software malintencionado**: la herramienta de eliminación de software malintencionado de Microsoft Windows busca en los equipos con Windows XP, Windows 2000 y Windows Server 2003 infecciones por software malintencionado específico y de ataques más frecuentes, y ayuda a eliminarlas. Cuando el proceso de detección y eliminación ha concluido, la herramienta muestra un informe en el que se describe el resultado e incluye, si lo hubiera, el software malintencionado que se ha detectado y eliminado. Microsoft publica una versión actualizada de esta herramienta el segundo martes de cada mes, o según se requiera para responder a incidentes de seguridad.

-   **Filtros de terceros con Microsoft ISA Server**: además de ofrecer soluciones de seguridad de red, ISA Server puede ayudarle a proteger la organización de ataques de malware. Para ello, use filtros personalizados o de terceros que eliminen el malware antes de que llegue a la red corporativa.

#### Seguridad de las aplicaciones

Para cumplir con los requisitos del Estándar PCI DSS, debe pensar en soluciones para la seguridad de las aplicaciones desde dos puntos de vista. Por un lado, debe exigir que todas las aplicaciones nuevas que creen los desarrolladores de su organización cumplan procedimientos de desarrollo seguros. Por otro, debe asegurarse de usar las directrices de seguridad proporcionadas junto con las aplicaciones de software que adquiera de Microsoft o de otro proveedor.

##### Cumplimiento de los requisitos del Estándar PCI DSS

El desarrollo y mantenimiento de aplicaciones seguras, independientemente de si están basadas en Internet o en Windows, es un paso importante para las tareas de cumplimiento del Estándar PCI DSS que realice. Concretamente, estas soluciones de tecnología le permiten cumplir el requisito 6.

Para obtener el texto completo de este requisito, consulte el [*Estándar de seguridad de datos en la industria de tarjetas de pago,* *versión 1.1.*](https://www.pcisecuritystandards.org/pdfs/pci_dss_v1-1.pdf) (en inglés).

##### Tecnologías disponibles

Microsoft ofrece orientación y herramientas específicas para el desarrollo de aplicaciones seguras. También ofrece directrices específicas para usar sus productos de servidor principales de forma segura.

-   **Microsoft Visual Studio® 2005**: Visual Studio 2005 proporciona una serie de herramientas que permiten que sus desarrolladores comprueben el código para las infracciones de seguridad durante la etapa de desarrollo:

    -   FxCop comprueba el código administrado en caso de defecto, incluidos los defectos de seguridad.

    -   PREfast es una herramienta estática de análisis del código de C y C++. Puede ayudar a sus desarrolladores a que detecten una serie de problemas de seguridad.

    -   El Lenguaje de Anotación Estándar puede ayudar a los desarrolladores a detectar errores de seguridad que podrían pasar inadvertidos para los compiladores del código de C o C++.

    -   A la hora de compilar código no administrado escrito en C o C++, los desarrolladores deben compilarlo siempre con la función de detección de saturación de la pila /GS y vincular el código a la opción /SafeESH.

    -   Los desarrolladores de RPC deben compilar su código con el marcador MIDL /robust especificado.

-   **Intelligent Application Gateway (IAG) 2007 de Microsoft**: como parte de Microsoft Forefront Network Edge Security, IAG proporciona una VPN de capa de sockets seguros (SSL), un firewall de aplicaciones web y una administración de la seguridad de extremos que habilita el control de acceso, la autorización y la inspección de contenidos en una amplia variedad de aplicaciones de línea de negocio. En conjunto, estas tecnologías proporcionan a los trabajadores móviles y remotos un acceso fácil, flexible y seguro desde una amplia gama de dispositivos y ubicaciones, incluidos los quioscos multimedia, los equipos de escritorio y los dispositivos móviles. IAG también permite que los administradores de TI exijan el cumplimiento de las directrices de uso de la información y de las aplicaciones a través de una directiva de acceso remoto personalizado basada en dispositivos, usuarios, aplicaciones u otros criterios empresariales. Entre los beneficios principales, se incluyen los siguientes:

    -   Una combinación única de acceso basado en SSL VPN, protección integrada de las aplicaciones y administración de la seguridad de extremos;

    -   Un firewall de aplicaciones web eficiente que ayuda a mantener fuera el tráfico malintencionado y la información confidencial dentro;

    -   Una menor complejidad a la hora de administrar el acceso seguro y proteger los activos de la empresa con una plataforma completa y fácil de usar;

    -   Interoperabilidad con la infraestructura principal de las aplicaciones de Microsoft, con los sistemas empresariales de terceros y con herramientas internas personalizadas.

##### Directrices

-   **Código de ciclo de vida del desarrollo de seguridad**: si su organización decide desarrollar algunas soluciones propias para controlar los datos de los titulares de tarjetas, debe considerar que los desarrolladores usen el código de ciclo de vida del desarrollo de seguridad desarrollado en Microsoft. Es un enfoque completo para el desarrollo de aplicaciones web y de escritorio seguras que sirvan para organizaciones que procesen y almacenen información confidencial, como los datos de titulares de tarjetas. El código de ciclo de vida del desarrollo de seguridad comienza con la planeación de aplicaciones seguras, garantiza que se usan técnicas de codificación seguras e incluye la prueba e implementación de aplicaciones de forma segura una vez completado el desarrollo.

-   **Cumplimiento de directrices de seguridad de productos**: Microsoft ofrece directrices de seguridad para algunos de sus productos de software. Las directrices de seguridad para Exchange Server, Systems Management Server y SQL Server son de especial interés para las organizaciones medianas y grandes. Para obtener información acerca de directrices de seguridad para estos productos, consulte la sección sobre seguridad de aplicaciones de la [*Guía de planeación de cumplimiento normativo*](http://www.microsoft.com/technet/security/guidance/complianceandpolicies/compliance/rcguide/default.mspx?mfr=true) (en inglés).

#### Mensajería y colaboración

Para cumplir con los requisitos del Estándar PCI DSS, debe garantizar que el software de mensajería y colaboración que usa su organización está configurado e instalado de forma segura. Las aplicaciones de mensajería y colaboración se han convertido en herramientas fundamentales dentro de la industria de las tarjetas de pago, por lo que es esencial que haga todo lo que esté en su mano para asegurarse de que los documentos y mensajes de correo electrónico que puedan contener datos de titulares de tarjetas estén seguros.

##### Cumplimiento de los requisitos del Estándar PCI DSS

Entre los métodos comunes para ayudar a evitar infracciones de seguridad de la mensajería, se encuentran las puertas de enlace de mensajería, los servidores de mensajería seguros y la filtración de contenido de mensajería. Tanto las puertas de enlace de mensajería como la filtración de contenido de mensajería enrutan los mensajes a una aplicación de software especializada. Esta aplicación puede usar una gran variedad de métodos para aislar cadenas de palabras, cadenas de números, patrones de palabras y otros elementos específicos según la forma en que fue diseñada la solución. Los mensajes que contengan esas cadenas o palabras clave se pueden poner en cuarentena hasta que se pueda comprobar la información sospechosa, o simplemente la solución puede eliminar y purgar el mensaje. Estos métodos pueden ayudarle a asegurar los datos de los titulares de tarjetas cuando se envíen a través de un mensaje de correo electrónico o de un documento en un entorno de colaboración. Todas estas técnicas y soluciones pueden ayudarle a cumplir con el requisito 4 del Estándar PCI DSS.

Para obtener el texto completo de este requisito, consulte el [*Estándar de seguridad de datos en la industria de tarjetas de pago,* *versión 1.1.*](https://www.pcisecuritystandards.org/pdfs/pci_dss_v1-1.pdf) (en inglés).

##### Tecnologías disponibles

Microsoft proporciona una serie de soluciones que pueden ayudarle a asegurar el software de mensajería y colaboración. Cada una de esas soluciones ofrece una solución para diferentes aspectos de su empresa. Debe implementarlas de forma organizada para que queden tan pocas vulnerabilidades en la seguridad como sea posible después de haber terminado.

-   **Microsoft Exchange Server**: al igual que con la administración de documentos, Exchange puede ayudarle a definir soluciones eficientes para las necesidades de mensajería de su organización a la vez que mantiene la seguridad de los datos de los titulares de tarjetas en los mensajes de correo electrónico. Exchange Server 2007 incluye servicios de mensajería unificada, que compila el correo electrónico, correo de voz y fax que se envía a un usuario en una única bandeja de entrada. Ofrece además características que permiten a la organización aplicar reglas de retención, funciones de detección e intervención en mensajes en curso, diario flexible y realizar búsquedas de texto enriquecido en todos los buzones implementados.
    Para obtener más información, consulte el sitio web de Microsoft Exchange Server (en inglés) en <http://www.microsoft.com/exchange/default.mspx>.

-   **Microsoft Forefront Security para Exchange Server**: Microsoft Forefront Security para Exchange Server le ayuda a proteger la infraestructura de correo electrónico ante infecciones y tiempo de inactividad a través de un enfoque que hace hincapié en las defensas en niveles, la optimización del rendimiento y la disponibilidad de Exchange Server y el control simplificado de la administración.

    -   **Protección exhaustiva**: Microsoft Forefront Security para Exchange Server incluye varios motores de detección de empresas de seguridad líderes en el sector integrados en una única solución para ayudar a las empresas a proteger sus entornos de mensajería de Exchange ante virus, gusanos y correo no deseado.

    -   **Rendimiento optimizado**: gracias a su estrecha integración con Exchange Server, así como su innovador sistema de análisis y de control del rendimiento, Forefront Security para Exchange Server ayuda a proteger los entornos de mensajería a la vez que mantiene el tiempo límite del servidor y optimiza el rendimiento de este.

    -   **Administración simplificada**: Forefront Security para Exchange Server también permite a los administradores administrar fácilmente la configuración y el funcionamiento, las actualizaciones automáticas de las firmas del motor de detección y un sistema de generación de informes, tanto en el nivel del servidor como de la empresa.

-   **Servicios hospedados de Microsoft Exchange**: los Servicios hospedados de Microsoft Exchange para la administración y seguridad de la mensajería se componen de cuatro servicios diferentes que ayudan a las organizaciones a protegerse frente al software malintencionado a través del correo electrónico, a satisfacer los requisitos de retención para el cumplimiento, a cifrar los datos para mantener la confidencialidad y a mantener el acceso al correo electrónico durante y después de las situaciones de emergencia. Los servicios se implementan en Internet mediante un modelo de “software como servicio” que ayuda a minimizar la inversión de capital adicional, a liberar recursos de TI para centrarse en otras iniciativas que producen valor y a mitigar los riesgos de la mensajería antes de que lleguen al firewall de la empresa.

    Para obtener más información, consulte *Servicios hospedados de Microsoft Exchange* (en inglés) <http://www.microsoft.com/exchange/services/default.mspx>.

-   **Information Right Management (IRM) de Microsoft Office**: Office es un conjunto primordial de aplicaciones de productividad para las empresas. La característica IRM de Microsoft Office puede ayudarle a que sus organizaciones controlen el acceso a la información confidencial, como los datos de los titular de tarjetas.

    En concreto, la característica IRM de Office le ayuda de las siguientes formas:

    -   Evita que un destinatario con acceso a la información protegida reenvíe, copie, modifique, imprima, envíe faxes o corte y pegue la información para su uso sin autorización.

    -   Evita que la información protegida se copie mediante la función Imprimir pantalla de Microsoft Windows.

    -   Proporciona información con el mismo nivel de protección a donde esta se envíe. Esta característica conforma la denominada "protección persistente".

    -   Proporciona el mismo nivel de protección a los datos adjuntos de correo electrónico, siempre que estos sean archivos creados con otros programas de Office, como Excel o Word.

    -   Protege la información contenida en los mensajes de correo electrónico o documentos con fecha de expiración, de modo que la información no se pueda ver hasta pasado un período de tiempo determinado.

    -   Aplica las directivas corporativas que determinan el uso y la difusión de la información dentro y fuera de la compañía.

-   **Information Rights Management (IRM) de** **Microsoft Windows SharePoint Services**: al igual que con las soluciones de administración de documentos, IRM de SharePoint Services puede ayudarle a hacer que sus soluciones de colaboración cumplan con los requisitos del Estándar PCI DSS. Esta tecnología le permite crear un conjunto persistente de controles de acceso que están asociados con el contenido en lugar de con una ubicación de red específica, lo que le ayudará a controlar el acceso a los archivos incluso después de que ya no estén bajo su control directo. IRM está disponible para archivos que se encuentran en bibliotecas de documentos y que estén almacenados como datos adjuntos a los elementos de lista. Los administradores de sitio pueden decidir proteger las descargas desde una biblioteca de documentos con IRM. Cuando un usuario intenta descargar un archivo desde una biblioteca, Windows SharePoint Services comprueba que el usuario tenga los permisos necesarios del archivo y emite una licencia para el usuario que permite el acceso al archivo en función del nivel de permiso correspondiente. A continuación, Windows SharePoint Services descarga el archivo en el equipo del usuario en un formato de archivo cifrado y administrado a partir de derechos.

    La característica IRM de Office está integrada en la plataforma de los Servicios de Microsoft Windows Rights Management. Para habilitar esta característica en Office, debe adquirir licencias de servidor RMS.

    Para obtener más información, consulte el sitio web [*Productos y tecnologías de Microsoft SharePoint*](http://go.microsoft.com/fwlink/?linkid=12632) (en inglés) en <http://go.microsoft.com/fwlink/?linkid=12632>.

#### Clasificación y protección de datos

Las soluciones de clasificación y protección de datos son elementos centrales para el correcto cumplimiento de los requisitos del Estándar PCI DSS y el mantenimiento seguro de los datos de titulares de tarjetas. Estas soluciones tratan la forma de aplicar niveles de clasificación de la seguridad en los datos de titulares de tarjetas de un sistema o aquellos que están en transmisión. Esta categoría de soluciones también comprende la protección de los datos en cuanto que ofrecen confidencialidad e integridad tanto de los datos que están almacenados como de los que se están transmitiendo. Las soluciones de cifrado constituyen el método más habitual usado por las organizaciones para proporcionar protección de datos.

##### Cumplimiento de los requisitos del Estándar PCI DSS

Las soluciones de clasificación y protección de datos le ayudan a cumplir con los requisitos del Estándar PCI DSS mediante la protección de los datos de los titulares de tarjeta cuando están almacenados en una base de datos, se están transmitiendo de un servidor a otro o se están transmitiendo a una red cuando un titular de tarjeta realiza una compra. El uso de estas soluciones le permiten cumplir con los requisitos 3 y 7 del Estándar PCI DSS.

Para obtener el texto completo de cualquiera de estos requisitos, consulte el [*Estándar de seguridad de datos en la industria de tarjetas de pago,* *versión 1.1.*](https://www.pcisecuritystandards.org/pdfs/pci_dss_v1-1.pdf) (en inglés).

##### Tecnologías disponibles

Microsoft ofrece una serie de tecnologías que le pueden ayudar a clasificar y proteger los datos de los titulares de tarjetas, independientemente de si se están transmitiendo por su red, si están almacenados en un documento del equipo de un empleado o si están almacenados en una base de datos. Estas recomendaciones son:

-   **Cifrado de unidad BitLocker™**: el Cifrado de unidad BitLocker le ayuda a proteger los datos de los titulares de tarjetas mediante el cifrado de la unidad y la comprobación de la integridad de los componentes que primero se ejecutan en el arranque. El cifrado de unidad protege los datos evitando que los usuarios no autorizados traspasen la protección del sistema y de los archivos de Windows en equipos perdidos o robados. Ese grado de protección se alcanza mediante el cifrado de todo el volumen de Windows. Con BitLocker, se cifran todos los archivos de usuario y de sistema, incluidos los archivos de intercambio e hibernación. La comprobación de la integridad de los componentes que primero se ejecutan en el arranque ayuda a asegurar que el descifrado de los datos se realice exclusivamente si esos componentes aparecen como intactos y que la unidad cifrada se encuentre en el equipo original. BitLocker está disponible en Windows Vista Enterprise y Windows Vista Ultimate, así como en Windows Server “Longhorn”.

-   **Sistema de cifrado de archivos (EFS) de Windows**: EFS proporciona la principal tecnología de cifrado de archivos usada para almacenar archivos cifrados en volúmenes de sistema de archivos NTFS. Después de cifrar un archivo o carpeta, trabaja con el archivo o la carpeta que se han cifrado igual que lo haría con cualquier otro archivo o carpeta.

    El cifrado es transparente para el usuario que ha cifrado el archivo. Esto quiere decir que no tiene que descifrar manualmente ningún archivo cifrado antes de poder usarlo. Puede abrir y cambiar el archivo de la misma forma que lo hace normalmente.

-   **Servicios de Microsoft Windows Rights Management**: los Servicios de Microsoft Windows Rights Management (RMS) son una plataforma de software que facilita a las aplicaciones la protección de los datos de titulares de tarjetas ante el uso no autorizado (tanto en línea como sin conexión, fuera y dentro del firewall).

    RMS mejora la estrategia de seguridad de una organización mediante la protección de la información a través de directivas de uso persistentes, que se mantienen con la información independientemente de donde esta vaya. Las aplicaciones con RMS habilitado se pueden usar para administrar, controlar y auditar el acceso a los documentos que contienen información del titular de la tarjeta. El cliente RMS está integrado en el sistema operativo de Windows Vista. Para otras versiones de Windows, el cliente RMS está disponible como descarga gratuita.
    Para obtener más información, consulte [*Servicios de Microsoft Windows Rights Management*](http://www.microsoft.com/rms) (en inglés) en <http://www.microsoft.com/rms>.

-   **Cifrado en Microsoft SQL Server**: cuando almacena datos de titulares de tarjetas en SQL Server, se cifran los datos con una infraestructura de cifrado jerárquico y de administración de claves. Cada capa cifra la capa inferior mediante una combinación de certificados, claves asimétricas y claves simétricas. Existe una clave maestra para SQL Server y una clave independiente para cada base de datos en esa instancia de SQL Server. De esta forma, se proporciona seguridad al almacenamiento de datos de titulares de tarjetas de su organización.

#### Administración de identidades

La administración de identidades es otro elemento importante a la hora de cumplir con el Estándar PCI DSS. Las soluciones de administración de identidades le permiten limitar el personal que podrá tener acceso, procesar y transmitir datos de titulares de tarjetas. Su organización puede usar dichas soluciones de administración de identidades para ayudar a administrar los permisos e identidades digitales de sus empleados, clientes y asociados.

##### Cumplimiento de los requisitos del Estándar PCI DSS

El uso de soluciones de administración de identidades le pueden permitir cumplir con el requisito 8 del Estándar PCI DSS ayudándole a crear y asignar un identificador único a cada persona de la organización que tenga acceso a un equipo. Estas soluciones también pueden ayudarle a restringir el acceso a datos de los titulares de tarjetas basado en ese identificador único, lo que constituye la base del requisito 7 del Estándar PCI DSS.

Para obtener el texto completo de este requisito, consulte el [*Estándar de seguridad de datos en la industria de tarjetas de pago,* *versión 1.1.*](https://www.pcisecuritystandards.org/pdfs/pci_dss_v1-1.pdf) (en inglés).

##### Tecnologías disponibles

Microsoft proporciona numerosas tecnologías para ayudarle a cumplir con los requisitos de administración de identidades de su organización.

<ul>
<li>
**Microsoft Active Directory:** Active Directory es compatible con una serie de técnicas que le ayudan a controlar el personal que puede tener acceso a datos de los titulares de tarjetas, tanto dentro como fuera de la red. En primer lugar, Active Directory es compatible con la autenticación Kerberos, una de las técnicas de autenticación de Windows predeterminadas. Kerberos proporciona autenticación de usuario segura con un estándar del sector que permite la interoperabilidad. El controlador de dominio de Active Directory mantiene la información de inicio de sesión y de cuentas de usuario para ser compatible con el servicio Kerberos. En segundo lugar, Active Directory es compatible con la autenticación de tarjeta inteligente. Puede exigir que los usuarios y administradores remotos de sistemas que contengan datos de titulares de tarjetas usen una tarjeta inteligente y un número de identificación personal para obtener acceso a la red. En tercer lugar, Active Directory es compatible con las credenciales móviles, un servicio que permite a los usuarios que tienen que usar varios equipos el uso de las mismas credenciales en esos equipos. En cuarto lugar, Active Directory permite que su organización personalice los proveedores de credenciales que usa para autenticar a los usuarios. Estas características pueden ayudarle a controlar la forma en que las cuentas de Active Directory puedan tener acceso a datos de los titulares de tarjetas y las cuentas que le proporcionan acceso a esos datos.

</li>
Para obtener más información, consulte el centro de tecnología de Active Directory de Windows Server 2003 (en inglés) en <http://www.microsoft.com/windowsserver2003/technologies/directory/activedirectory/default.mspx>.

<li>
**Servicios de federación de Active Directory de Microsoft**: con los Servicios de federación de Active Directory (ADFS), puede crear soluciones de administración de identidades que van más allá de los límites tradicionales de su bosque de Active Directory. Mediante la implementación de ADFS, su organización puede ampliar su infraestructura de Active Directory existente para proporcionar acceso a recursos ofrecidos por asociados de confianza en Internet. Estos asociados de confianza pueden incluir terceros externos, otros departamentos o subsidiarias de la misma organización.

</li>
ADFS está altamente integrado en Active Directory. ADFS recupera atributos de usuario de Active Directory y autentica usuarios con Active Directory. ADFS también usa la autenticación integrada de Windows. ADFS está disponible en los sistemas operativos Windows Server 2003 R2 y Windows Server “Longhorn”.

Para obtener más información, consulte *Información general acerca de los Servicios de federación de Active Directory (ADFS) en Windows Server 2003 R2* (en inglés) en [http://www.microsoft.com/WindowsServer2003/R2/Identity\_Management/ADFSwhitepaper.mspx](http://www.microsoft.com/windowsserver2003/r2/identity_management/adfswhitepaper.mspx).

<li>
**Microsoft Identity Lifecycle Manager**: Microsoft Identity Lifecycle Manager (ILM) simplifica el proceso de coincidencias y administración de los registros de identidad de repositorios de datos dispares y evita anomalías, como los registros activos de empleados que se han marchado de la organización. ILM proporciona a la organización un marco de directiva para controlar y realizar un seguimiento de los datos de identidad y acceso que ayudan a administrar el cumplimiento. También incluye herramientas de autoayuda para usuarios finales, lo que permite que su departamento de TI mejore la eficiencia mediante la delegación segura de muchas tareas en usuarios finales. Otra característica clave de ILM es que incluye una solución de administración de certificados basada en Windows que se integra con el sistema operativo Windows Server 2003 y con Active Directory para proporcionar una solución de puesta a punto para la administración del ciclo de vida completo de las tarjetas inteligentes y de los certificados digitales de la entidad de certificación de Windows Server 2003.

</li>
ILM brinda a su organización las siguientes ventajas:

-   Sincronización de la información de identidad en una gran variedad de almacenes de identidades heterogéneos en directorios u otras ubicaciones. Esto le permite automatizar el proceso de actualización de la información de identidad en plataformas dispares al tiempo que mantiene la integridad y la propiedad de los datos a través de la empresa.

-   Provisión y eliminación de cuentas de usuario e información de identidad como distribución, cuentas de correo electrónico y grupos de seguridad a través de sistemas y plataformas. Se pueden crear nuevas cuentas para empleados de forma rápida en función de los eventos o los cambios de los almacenes de autoridad, como el sistema de recursos humanos. Además, cuando los empleados se marchan de la compañía, se les puede excluir inmediatamente de tales sistemas.

-   Administración de certificados y tarjetas inteligentes. ILM incluye una solución basada en directivas y en el flujo de trabajo que permite que las organizaciones administren fácilmente el ciclo de vida de los certificados digitales y de las tarjetas inteligentes. ILM maximiza los Servicios de Active Directory y los servicios de certificados de Active Directory para entregar certificados digitales y tarjetas inteligentes, con flujo de trabajo automatizado para administrar el ciclo de vida completo de las credenciales basadas en certificados. ILM reduce de forma significativa los costos asociados a los certificados digitales y a las tarjetas inteligentes permitiendo que las organizaciones implementen, administren y mantengan la infraestructura basada en certificados de una forma más eficiente. También simplifica el aprovisionamiento, la configuración y la administración de certificados digitales, al tiempo que aumenta la seguridad a través de una sólida tecnología de autenticación multifactor.

Para obtener más información, consulte la página principal de Microsoft Identity Lifecycle Manager (en inglés) en <http://www.microsoft.com/windowsserver/ilm2007/default.mspx>.

<li>
**Microsoft SQL Server**: puede usar el servidor SQL Server junto con otras tecnologías para crear soluciones de administración de identidades. Use bases de datos de SQL Server para almacenar información de nombre de usuario y contraseña, así como para asignar certificados a cuentas de usuario y otras soluciones. Puede usar el servidor SQL Server junto con ILM de Microsoft, Active Directory, directivas de grupo y listas de control de acceso para restringir el acceso de los usuarios a los datos de los titulares de tarjetas almacenados en otra base de datos, en documentos o en directorios.

</li>
Para obtener más información, consulte la página sobre Microsoft SQL Server (en inglés) en <http://www.microsoft.com/sql/default.mspx>.

</ul>
##### Características de compatibilidad con sistemas operativos

-   **Infraestructura de clave pública**: una infraestructura de clave pública (PKI) es un sistema de certificados digitales, entidades de certificación (CA) y otras entidades de registro que comprueban y autentican la validez de cada parte que interviene en una transacción electrónica mediante el uso de criptografía de clave pública. Esta infraestructura le permite asegurar e intercambiar datos de titular de tarjeta con un nivel alto de seguridad en Internet, extranets, intranets y aplicaciones.

#### Autenticación, autorización y control de acceso

La autenticación es el proceso de identificación de un usuario. En entornos de TI, la autenticación suele incluir un nombre de usuario y una contraseña, aunque también puede implicar otros métodos para demostrar la identidad, como el uso de tarjetas inteligentes, exámenes de retina, reconocimiento de voz o el análisis de las huellas dactilares. La autorización se centra en determinar si a la identidad autenticada se le permite el acceso a los recursos solicitados. Puede decidir otorgar o denegar el acceso en función de una serie de criterios, como la dirección de red del cliente, la hora del día o el explorador que use esa persona.

A la hora de planear una estrategia de autenticación, autorización y control de acceso, también debe desarrollar una estrategia para otorgar permisos de cuenta de usuario a todos los recursos de su red. Para obtener más información, consulte [*Aplicación del principio de privilegios mínimos a cuentas de usuarios en Windows XP*](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/luawinxp.mspx).

##### Cumplimiento de los requisitos del Estándar PCI DSS

La autenticación, la autorización y el control de acceso son partes clave de su estrategia de seguridad de los datos de titulares de tarjetas, especialmente en combinación con las soluciones de clasificación y protección de datos y de administración de identidades. En este contexto, la autenticación, la autorización y el control de acceso pueden ayudar a que su organización cumpla con los requisitos 6, 7 y 8 del Estándar PCI DSS.

Para obtener el texto completo de cualquiera de estos requisitos, consulte el [*Estándar de seguridad de datos en la industria de tarjetas de pago,* *versión 1.1.*](https://www.pcisecuritystandards.org/pdfs/pci_dss_v1-1.pdf) (en inglés).

##### Tecnologías disponibles

Microsoft ofrece varias tecnologías que pueden ayudarle a crear e integrar estrategias de autenticación, autorización y control de acceso en su solución completa de cumplimiento del Estándar PCI DSS.

-   **Microsoft Active Directory**: gran parte del servicio de Active Directory en Microsoft Windows 2000 Server, Windows Server 2003 y Windows Server “Longhorn” se centra en la autenticación, la autorización y el control de acceso. Por ejemplo, Active Directory es compatible con la autenticación Kerberos, una de las técnicas de autenticación de Windows predeterminadas. Kerberos proporciona autenticación de usuario segura con un estándar del sector que permite la interoperabilidad. El controlador de dominio de Active Directory mantiene la información de inicio de sesión y de cuentas de usuario para ser compatible con el servicio Kerberos. Además, Active Directory es compatible con la autenticación de tarjetas inteligentes. Puede exigir que los usuarios y administradores remotos de sistemas que contengan datos de titulares de tarjetas usen una tarjeta inteligente y un número de identificación personal para obtener acceso a la red. Active Directory es compatible con las credenciales móviles, un servicio que permite a los usuarios que tienen que usar varios equipos el uso de las mismas credenciales en esos equipos. Con Active Directory, su organización también puede personalizar los proveedores de credenciales que usa para autenticar a los usuarios. Además, Active Directory le permite delegar tareas administrativas en la organización. Estas características pueden ayudarle a controlar la forma en que permite que las cuentas de Active Directory puedan obtener acceso a datos de los titulares de tarjetas y a las cuentas que le proporcionan acceso a esos datos.

-   **Servicio de autenticación de Internet de Microsoft**: el Servicio de autenticación de Internet (IAS) es la implementación de Microsoft de un servidor y un proxy de Servicio de autenticación remota telefónica de usuario (RADIUS). Como servidor RADIUS, IAS lleva a cabo tareas de información, autorización y autenticación con conexión centralizada de muchos tipos de acceso de red, incluidas las conexiones inalámbricas y VPN. Como proxy RADIUS, IAS reenvía mensajes de autenticación e información a otros servidores RADIUS. Al hacer esto, IAS lleva a cabo pasos de autenticación para conexiones remotas antes de que lleguen a la red de la organización. Con las credenciales que el usuario facilitó para conectarse remotamente, puede autorizarlo para que tenga acceso sólo a los recursos de la red que necesite para realizar su trabajo.

##### Características de compatibilidad con sistemas operativos

-   **Uso de listas de control de acceso para otorgar permisos de recurso**: una lista de control de acceso (ACL) es un mecanismo usado por los sistemas operativos a partir de Microsoft Windows NT para proteger recursos como archivos y carpetas. Las ACL contienen varias entradas de control de acceso (ACE) que asocian una entidad de seguridad (normalmente una cuenta de usuario o un grupo de cuentas) con una regla que regula el uso del recurso. Las ACL y las ACE otorga a su organización la posibilidad de permitir o denegar derechos sobre recursos en función de los permisos que pueda asociar a cuentas de usuario. Por ejemplo, puede crear una ACE y aplicarla a la ACL de un archivo para prohibir a todos los usuarios, salvo a un administrador, la lectura del archivo. Debe usar esta tecnología como parte de la solución de administración de identidades más amplia, pero sigue siendo una buena alternativa para limitar el acceso a datos de titulares de tarjetas exclusivamente a las personas con una necesidad empresarial.

-   **Firewall de Windows en Microsoft Windows Vista y Windows Server “Longhorn”**: como se ha comentado anteriormente, Firewall de Windows en Windows Vista y Windows Server “Longhorn” puede ayudarle a proteger sus sistemas y redes ante ataques malintencionados. También puede ayudarle a controlar los usuarios, equipos y grupos que pueden tener acceso a los recursos de un equipo o dominio. Cuando use Firewall de Windows con seguridad avanzada, puede crear reglas que filtren las conexiones de los usuarios, equipos y grupos de Active Directory. Para crear este tipo de reglas, debe asegurar la conexión con IPsec usando credenciales que portan información de cuenta de Active Directory, como Kerberos versión 5.

Para obtener vínculos a información conceptual y guías de planeación acerca de la autenticación, la autorización y el control de acceso, consulte la sección sobre autenticación, autorización y control de acceso de la [*Guía de planeación de cumplimiento normativo*](http://www.microsoft.com/technet/security/guidance/complianceandpolicies/compliance/rcguide/default.mspx?mfr=true) (en inglés).

#### Identificación de vulnerabilidades

Las soluciones de identificación de vulnerabilidades proporcionan herramientas que su organización puede usar para ayudarle a probar las vulnerabilidades de los sistemas de información. El personal de TI de la empresa debe ser consciente de las vulnerabilidades del entorno de TI antes de que puedan abordarlas de forma eficiente. También forma parte de la identificación de vulnerabilidades la capacidad de restaurar datos que se perdieron accidentalmente debido a un error de usuario.

##### Cumplimiento de los requisitos del Estándar PCI DSS

Las soluciones para las vulnerabilidades permiten que la organización cumpla con el requisito 11 del Estándar PCI DSS, mediante pruebas frecuentes de los sistemas y procedimientos de seguridad.

Para obtener el texto completo de este requisito, consulte el [*Estándar de seguridad de datos en la industria de tarjetas de pago,* *versión 1.1.*](https://www.pcisecuritystandards.org/pdfs/pci_dss_v1-1.pdf) (en inglés).

##### Tecnologías disponibles

Microsoft ofrece soluciones que le ayudan a diseñar soluciones de identificación de vulnerabilidades para cumplir con los requisitos del Estándar PCI DSS.

-   **Microsoft Baseline Security Analyzer (MBSA)**: como en la evaluación de riesgos a la hora de diseñar diversos controles de protección de datos de titulares de tarjetas, MBSA le permite examinar periódicamente las vulnerabilidades que pueden comprometer la seguridad de estos datos. Puede usar MBSA para localizar configuraciones incorrectas de seguridad comunes en una serie de productos de Microsoft, incluidos el sistema operativo de Windows, Internet Information Services, SQL Server, Internet Explorer y Microsoft Office. MBSA también detecta las actualizaciones de seguridad, los paquetes acumulativos de actualizaciones y los service packs que faltan con respecto a los publicados en Microsoft Update. Puede ejecutar MBSA desde el símbolo del sistema o en una GUI, así como usarlo con Microsoft Update y Windows Server Update Services. Mantener actualizados los sistemas es una forma muy importante de asegurar los datos de titulares de tarjetas en la mayor medida posible, por lo que MBSA puede ser una herramienta muy valiosa a la hora de determinar si las instalaciones de productos han generado vulnerabilidades en estos datos a lo largo del tiempo.

#### Supervisión, auditoría y generación de informes

Las soluciones de supervisión y generación de informes recopilan y auditan registros derivados de la autenticación y del acceso a sistemas. Puede diseñar estas soluciones para recopilar información específica en función del Estándar PCI DSS o usar registros existentes integrados en sistemas operativos o paquetes de software.

Una subcategoría de la supervisión y la generación de informes es la recopilación, el análisis y la correlación de todos los datos registrados en la organización. A veces, esto se realiza a través de una solución similar a un panel, en la que puede analizar mejor los diversos datos recopilados en la organización. Este tipo de solución permite que la administración de TI determine más eficazmente si hay una correlación entre eventos.

##### Cumplimiento de los requisitos del Estándar PCI DSS

Las soluciones de supervisión, auditoría y generación de informes pueden ayudarle a cumplir con el requisito 10 del Estándar PCI DSS para seguir y supervisar todos los accesos a los recursos de red y a los datos de los titulares de tarjetas.

##### Tecnologías disponibles

Microsoft ofrece una serie de tecnologías que le permiten supervisar el acceso a redes y a los datos de los titulares de tarjetas.

-   **Recopilación de auditorías de Microsoft System Center Operations Manager**: Operations Manager 2007 puede extraer y recopilar de forma segura y eficaz los registros de seguridad de sistemas operativos de Windows y almacenarlos para su análisis y notificación posterior. Los registros extraídos se almacenan en una base de datos de recopilación de auditorías independiente. Operations Manager enviará los informes que se pueden usar para los datos de la recopilación de auditorías. La recopilación de auditorías se puede usar para generar distintos informes de cumplimiento, como las auditorías de la normativa Sarbanes-Oxley. La recopilación de auditorías se puede usar también para los análisis de seguridad, como la detección de intrusiones y los intentos de acceso no autorizado.

-   **Infraestructura de registro de eventos de Microsoft Windows Vista**: las mejoras de la infraestructura de registro de eventos de Windows facilitan la administración y supervisión del escritorio de Windows Vista y proporcionan información más exacta acerca de la solución de problemas. Unos estándares estrictos aseguran que los eventos son coherentes, aplicables y están bien documentados. Muchos componentes que almacenaban información de registro en archivos de texto en versiones anteriores de Windows agregan ahora eventos al registro de eventos. Con el reenvío de eventos, los administradores pueden administrar de forma centralizada los eventos de equipos de cualquier punto de la red, lo que facilita la identificación activa de problemas y la correlación de problemas que afectan a varios equipos. Por último, se ha vuelto a escribir por completo el visor de eventos para permitir que los usuarios creen vistas personalizadas a fin de asociar de una forma sencilla los eventos con tareas y ver de forma remota registros de otros equipos. Esta aportación hace más práctico para los administradores el uso del registro de eventos para solucionar problemas de los usuarios.

-   **Microsoft SQL Server**: SQL Server Reporting Services es una completa solución basada en servidor que permite crear, administrar y suministrar informes tradicionales destinados a su impresión en papel e informes interactivos basados en Web. Como parte integrada del marco de Microsoft Business Intelligence, Reporting Services combina la administración de datos de SQL Server y Microsoft Windows Server con las conocidas y eficaces aplicaciones de Microsoft Office System para suministrar información en tiempo real con objeto de admitir operaciones diarias y fundamentar la toma de decisiones. Puede usar estos servicios para generar informes que analicen los datos de los titulares de tarjetas y realizar un seguimiento de los cambios en tales datos. También puede usar servicios de generación de informes para supervisar de una forma sencilla los patrones de uso de red y el flujo de información.

##### Características de compatibilidad con sistemas operativos

-   **Listas de control de acceso del sistema NTFS**: su organización puede usar listas de control de acceso del sistema NTFS (SACL) en archivos y directorios para ayudarle a seguir los cambios de esos archivos y carpetas de un sistema. Cuando establece una SACL en un archivo o una carpeta, cada vez que un usuario realice una acción en esa archivo o carpeta, la SACL hace que el sistema operativo de Windows registre la acción, así como la persona que la realizó. No puede establecer listas SACL en sistemas que tienen el sistema de archivos FAT, por lo que su organización debe usar el formato del sistema de archivos NTFS en todos los volúmenes que almacenan datos de los usuarios y de los titulares de tarjetas.

#### Administración de soluciones de tecnología del Estándar PCI DSS

Aunque los productos de administración no ayudan a que su organización cumpla con los requisitos específicos del Estándar PCI DSS, sí que pueden ayudarle a realizar un seguimiento de los controles de TI que haya implementado por razones de cumplimiento. A la hora de crear un marco para los controles de TI, siempre es importante poder administrar de forma centralizada esos controles desde el menor número posible de escritores de administradores.

##### Tecnologías disponibles

Microsoft le ofrece dos herramientas principales para la administración del marco de los controles de TI para cumplir con los requisitos del Estándar PCI DSS y otros requisitos normativos.

-   **Microsoft Forefront**: Microsoft Forefront es un conjunto de aplicaciones de productos de seguridad de línea de negocio que proporcionan protección para los sistemas operativos cliente, los servidores de aplicaciones y la red al completo. Puede usar Forefront con la infraestructura de TI que tenga para proteger lo servidores y los equipos cliente ante malware y otros ataques malintencionados a través de una integración sencilla con las servidores de aplicaciones como Exchange, SharePoint y el servicio de mensajería instantánea. Forefront también incluye integración incorporada con Active Directory y usa ISA Server para trabajar con Active Directory para ser compatible con RADIUS, DHCP y el uso de tarjetas inteligentes. Asimismo, Forefront proporciona una herramienta de administración centralizada para una ubicación central de informe junto con una ubicación centralizada para establecer medidas de control de directivas.

-   **Microsoft System Center**: Microsoft System Center es una familia de productos de administración destinada a proporcionar las herramientas que necesite su organización para automatizar la administración del sistema. System Center incluye tecnologías que ayudan a automatizar las tareas de administración más comunes y también proporciona herramientas que ayudan a los profesionales de TI a detectar, diagnosticar y corregir problemas en el entorno informático. Concretamente, System Center proporciona productos que realizan las siguientes funciones:

    -   Supervisión del hardware y el software en un entorno distribuido para detectar problemas y, a continuación, aportación de las herramientas para arreglar esos problemas.

    -   Automatización del proceso de instalación, actualización y aplicación de revisiones de software.

    -   Aportación de implementaciones de procesos estándar para la administración de sistemas.

    -   Control de las copias de seguridad y de la restauración de los datos de servidor de archivos de Windows.

    -   Tratamiento de los requisitos de supervisión y configuración de las organizaciones más pequeñas.

    -   Administración de máquinas virtuales. Dado que un hardware más rápido permite la ejecución de un mayor número de aplicaciones en cada equipo, las organizaciones cada vez usan más la virtualización para aislar esas aplicaciones.

    -   Ajuste del tamaño de las instalaciones mediante la aportación de herramientas para la estimación de los recursos necesarios.

#### Resumen

En esta sección, se describen soluciones de tecnología que su organización puede usar para conseguir y mantener el cumplimiento del Estándar PCI DSS. Se analizan las razones de la importancia de estas soluciones y se ofrecen vínculos para la orientación y la tecnología de Microsoft que puede ayudar a que la organización alcance el cumplimiento normativo.

El efecto de la implementación de esas soluciones no sólo ayuda a proporcionar estándares de seguridad y cumplimiento para su entorno de TI, sino que también tiene un efecto positivo sobre los procesos empresariales de su organización. Antes de implementar alguna de las soluciones identificadas, asegúrese de recibir asesoramiento legal de sus asesores jurídicos y auditores acerca de las necesidades únicas de cumplimiento del Estándar PCI DSS y considere con detenimiento la repercusión de esas aplicaciones sobre toda la organización, no sólo en materia de cumplimiento. Microsoft trabaja por ofrecer estudios y soluciones más exhaustivas para el Estándar PCI DSS y otros tipos de cumplimiento normativo. No obstante, también puede realizar una búsqueda pública para adquirir más información acerca de este complejo e importante asunto.

[![](images/Bb821241.arrow_px_up(es-es,TechNet.10).gif)](#mainsection)[Top Of Page](#mainsection)

### Apéndices

Esta sección contiene preguntas que suelen hacer los clientes acerca de las soluciones de tecnología de Microsoft y de su idoneidad para cumplir con los requisitos del Estándar PCI DSS. También contiene una tabla de las soluciones de tecnología que pueden ayudar a su organización a cumplir esos requisitos.

#### Preguntas más frecuentes

**P: ¿Por qué debe mi organización esforzarse por cumplir con el Estándar de seguridad de datos en la industria de tarjetas de pago? ¿No se trata de otro estándar inútil y caro?**

R: Las razones por las que la organización debe cumplir con el Estándar PCI DSS son tres. La primera, porque las marcas de tarjetas como Visa se han comprometido a ofrecer incentivos financieros por el cumplimiento del Estándar e imponer sanciones si no se cumple. La segunda, porque el cumplimiento de este estándar puede ayudar a reducir las responsabilidades en casos de pérdidas de datos. La tercera, porque mediante un análisis detallado y el diseño adecuado de sus sistemas, el proceso le puede ayudar realmente a seguir los datos del cliente y, por lo tanto, a mejorar el servicio y la satisfacción del cliente.

**P: ¿Exagera Microsoft la idoneidad de sus soluciones con respecto al cumplimiento del Estándar PCI DSS?**

R: La situación de cada organización es distinta y esta guía pretende ser lo más completa posible. Microsoft puede desarrollar una orientación específica para segmentos verticales del sector. También se puede poner en contacto con el representante de ventas de Microsoft y plantearle su consulta. Como se ha afirmado anteriormente, puede obtener mejores resultados empresariales si considera este proceso, no como un simple proyecto de cumplimiento, sino como una forma de mejorar sus procesos de seguimiento y administración de la información del cliente.

**P: Este documento describe muchas tecnologías que ayudan a cumplir con el Estándar PCI DSS,** **pero pocas soluciones de cumplimiento. ¿Por qué?**

R: Cada situación es única y, por lo tanto, no se puede presentar una sola solución ideal para todos. Microsoft se compromete a ofrecer a su organización información más detallada, como se ha mencionado en el resumen.

**P: ¿Qué puede hacer Microsoft para ayudar a mi organización a obtener la certificación del Estándar PCI DSS?**

R: Microsoft puede ofrecer software y servicios que facilitan el cumplimiento de los requisitos del Estándar PCI DSS, pero no puede garantizar que su organización los cumplirá. Como proveedor, estamos interesados en ayudar a su organización a cumplir con dichos requisitos, pero el cumplimiento se extiende a la organización, los auditores y las marcas de tarjetas con las que se trabaja.

**P: ¿No implica la sección 3.4.1 que no se pueden usar las tecnologías de protección de datos de Microsoft?**

R: No. Dicha sección dice exactamente lo siguiente:

“En caso de hacer uso del cifrado de disco (en lugar de aplicar el cifrado por archivos o columnas de la base de datos), el acceso lógico se debe administrar independientemente de los mecanismos de control de acceso del sistema operativo (por ejemplo, sin usar las cuentas de sistema local o de Active Directory). Las claves de descifrado no deben estar vinculadas a las cuentas de usuario”.

Las tecnologías de protección de datos de Microsoft no vinculan las claves de descifrado a las cuentas de usuario. Por ejemplo, el Cifrado de unidad BitLocker nunca vincula las claves de descifrado (números de identificación personal ni contraseñas de recuperación) a las cuentas de usuario de Active Directory. El Sistema de cifrado de archivos (EFS) tampoco vincula las claves de descifrado a las cuentas de usuario. Su organización puede revocar la capacidad de una persona de descifrar un documento sin cambiar los privilegios de acceso al sistema. Para determinadas configuraciones, EFS intenta optimizar la experiencia del usuario mediante la colocación automática de algunas claves de descifrado en los perfiles de usuario de determinados usuarios. Sin embargo, este comportamiento se puede cambiar mediante la configuración apropiada.

#### Requisitos del Estándar PCI DSS y soluciones de tecnología asociadas

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Requisito</th>
<th>Secciones de la solución de tecnología</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Requisito 1</td>
<td style="border:1px solid black;"><a href="#_risk_assessment">Evaluación de riesgos</a>; <a href="#_network_security">Seguridad de red</a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Requisito 2</td>
<td style="border:1px solid black;"><a href="#_network_security">Seguridad de red</a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Requisito 3</td>
<td style="border:1px solid black;"><a href="#_document_management">Administración de documentos</a>; <a href="#_risk_assessment">Evaluación de riesgos</a>; <a href="#_data_classification_and_protection">Clasificación y protección de datos</a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Requisito 4</td>
<td style="border:1px solid black;"><a href="#_risk_assessment">Evaluación de riesgos</a>; <a href="#_messaging_and_collaboration">Mensajería y colaboración</a>; <a href="#_data_classification_and_protection">Clasificación y protección de datos</a>; <a href="#_network_security">Seguridad de red</a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Requisito 5</td>
<td style="border:1px solid black;"><a href="#_risk_assessment">Evaluación de riesgos</a>; <a href="#_malicious_software_prevention">Prevención de software malintencionado</a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Requisito 6</td>
<td style="border:1px solid black;"><a href="#_document_management">Administración de documentos</a>; <a href="#_risk_assessment">Evaluación de riesgos</a>; <a href="#_change_management">Administración de cambios</a>; <a href="#_host_control">Control de host</a>; <a href="#_malicious_software_prevention">Prevención de software malintencionado</a>; <a href="#_application_security">Seguridad de las aplicaciones</a>; <a href="#_authentication,_authorization,_and_">Autenticación, autorización y control de acceso</a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Requisito 7</td>
<td style="border:1px solid black;"><a href="#_document_management">Administración de documentos</a>; <a href="#_risk_assessment">Evaluación de riesgos</a>; <a href="#_identity_management">Administración de identidades</a>; <a href="#_authentication,_authorization,_and_">Autenticación, autorización y control de acceso</a>; <a href="#_data_classification_and_protection">Clasificación y protección de datos</a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Requisito 8</td>
<td style="border:1px solid black;"><a href="#_risk_assessment">Evaluación de riesgos</a>; <a href="#_authentication,_authorization,_and_">Autenticación, autorización y control de acceso</a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Requisito 9</td>
<td style="border:1px solid black;"><a href="#_document_management">Administración de documentos</a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Requisito 10</td>
<td style="border:1px solid black;"><a href="#_document_management">Administración de documentos</a>; <a href="#_change_management">Administración de cambios</a>; <a href="#_monitoring,_auditing,_and_reporting">Supervisión, auditoría y generación de informes</a>; <a href="#_network_security">Seguridad de red</a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Requisito 11</td>
<td style="border:1px solid black;"><a href="#_risk_assessment">Evaluación de riesgos</a>; <a href="#_host_control">Control de host</a>; <a href="#_vulnerability_identification">Identificación de vulnerabilidades</a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Requisito 12</td>
<td style="border:1px solid black;"><a href="#_document_management">Administración de documentos</a></td>
</tr>
</tbody>
</table>
  
#### Recursos adicionales
  
[*Estándar de seguridad de datos en la industria de tarjetas de pago,* *versión 1.1 (en inglés)*](https://www.pcisecuritystandards.org/pdfs/pci_dss_v1-1.pdf)
  
[*Guía de planeación para el cumplimiento normativo (en inglés)*](http://www.microsoft.com/technet/security/guidance/complianceandpolicies/compliance/rcguide/default.mspx?mfr=true)
  
[*Cuestionario de autoevaluación del Estándar PCI DSS (en inglés)*](https://www.pcisecuritystandards.org/pdfs/pci_saq_v1-0.pdf)
  
[*Procedimientos de auditoría para el evaluador QSA del Estándar PCI DSS (en inglés)*](https://www.pcisecuritystandards.org/pdfs/pci_audit_procedures_v1-1.pdf)
  
[*Procedimientos de examen para el proveedor ASV del Estándar PCI DSS (en inglés)*](https://www.pcisecuritystandards.org/pdfs/pci_scanning_procedures_v1-1.pdf)** **
  
[*Aplicación del principio de privilegios mínimos a cuentas de usuario de Windows XP (en inglés)*](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/luawinxp.mspx)* *
  
[*Procedimientos recomendados para delegar la administración de Active Directory (en inglés)*](http://www.microsoft.com/downloads/details.aspx?familyid=631747a3-79e1-48fa-9730-dae7c0a1d6d3&displaylang=en)
  
[Servicios bancarios: descargas (en inglés*)*](http://msdn2.microsoft.com/en-us/architecture/86e3451d-8219-46af-bf99-4a610e4bf1f4.aspx)
  
#### Comentarios
  
Envíe las preguntas y los comentarios relacionados con esta guía a <cisfdbk@microsoft.com>.
  
[![Top Of Page](images/Bb821241.arrow_px_up(es-es,TechNet.10).gif)](#mainsection)[Top Of Page](#mainsection)
