---
TOCTitle: 'Seguridad en LAN inalámbricas con Servicios de Certificate Server: descripción general'
Title: 'Seguridad en LAN inalámbricas con Servicios de Certificate Server: descripción general'
ms:assetid: '23ea72db-2fae-4155-a307-e017c2c9d8e2'
ms:contentKeyID: 20112561
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd458739(v=TechNet.10)'
---

Capítulo 1: Descripción general de la solución
==============================================

Publicado: octubre 11, 2004 | Actualizado: 24/11/04

##### En esta página

[](#edaa)[Introducción](#edaa)
[](#ecaa)[Descripción general de la solución](#ecaa)
[](#ebaa)[Convenciones de estilo](#ebaa)
[](#eaaa)[Comentarios y soporte técnico](#eaaa)

### Introducción

Hoy día, muchas organizaciones han probado las LAN inalámbricas (WLAN) pero han acabado por resistirse a las implementaciones a gran escala o por prohibir completamente su utilización. A pesar de los muchos beneficios derivados de los sistemas inalámbricos en cuanto a productividad y tecnología, el bajo nivel de seguridad que ofrecen no contribuye a su popularidad y muchas organizaciones no se plantean la implementación de WLAN.

Esta guía, *Seguridad en LAN inalámbricas con Servicios de Certificate Server*, va destinada a empresas que desean implementar redes inalámbricas de una forma totalmente segura. Está escrita específicamente para proporcionar orientación normativa (trata de los aspectos de diseño, implementación y administración) y se basa en la implementación segura de WLAN propia de Microsoft.

Existen dos características importantes que distinguen a esta guía de la documentación y muchas de las notas de productos disponibles. La primera es la naturaleza *normativa* de la orientación: en casos en que el diseño dio lugar a opciones múltiples, las decisiones se tomaron con base a la información ofrecida por los clientes y la implementación interna de Microsoft. La solución se construyó en consecuencia y se realizaron las pruebas oportunas en los laboratorios de Microsoft para garantizar su funcionamiento. La segunda característica es que se trata de una solución *completa* que se ocupa de los aspectos de diseño, planeamiento, generación y configuración, además de la supervisión, el mantenimiento y la administración constantes de la arquitectura.

Tal y como se describe en capítulos posteriores, la solución se basa en el sistema 802.1X del IEEE (Instituto de ingenieros eléctricos y electrónicos) y requiere una infraestructura de servicio de usuario de acceso telefónico de autenticación remota (RADIUS, Remote Authentication Dial-In User Service), así como una infraestructura de claves públicas (PKI, Public Key Infrastructure). Utiliza un diseño flexible y resulta ideal para organizaciones de varios cientos a muchos miles de usuarios de redes inalámbricas. Los componentes RADIUS y PKI se diseñaron específicamente para permitir su reutilización en otras aplicaciones de red, como VPN de acceso remoto, y aplicaciones de seguridad como, por ejemplo, el sistema de archivos cifrados (EFS, Encrypting File System). La construcción y las pruebas de la solución se llevaron a cabo en clientes con Microsoft® Windows® XP y servidores Microsoft Windows Server™ 2003 (incluidos controladores de dominio del servicio de directorio Active Directory®), aunque su diseño es compatible con controladores de dominio de Windows 2000 y equipos con Windows 2000 y versiones anteriores.

[![](images/Dd458739.01fig1-1(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd458739.01fig1-1_big(es-es,technet.10).gif)

**Figura 1.1 Seguridad en LAN inalámbricas con Servicios de Certificate Server**

[](#mainsection)[Principio de la página](#mainsection)

### Descripción general de la solución

La solución *Seguridad de LAN inalámbricas* se compone de cuatro secciones principales: las guías de planeamiento, generación, operaciones y la guía de prueba. Adicionalmente, uno de los apéndices constituye una guía de entrega. Estos documentos vienen acompañados de un conjunto de herramientas que incluye un plan de proyecto de ejemplo, archivos de comandos para la automatización de las tareas de implementación y operaciones, así como una serie detallada de casos de prueba que puede utilizar para comprobar la funcionalidad de la solución según la incorpora en su propio entorno.

Las secciones a continuación ofrecen descripciones breves de las guías, así como una explicación de su finalidad y los usuarios a los que va dirigida. Las descripciones de las guías incluyen un resumen de los capítulos que las componen. Gran parte de las guías puede tratarse como material de referencia y no es necesario llevar a cabo una lectura de principio a fin, especialmente en el caso de la guía de operaciones (capítulos 11 y 12). Sin embargo, para lograr un entendimiento satisfactorio del diseño y la arquitectura de la solución, deberá leer al completo los capítulos 2 al 6 (correspondientes a la guía de planeamiento).

#### Guía de planeamiento: capítulos 2 al 6

Ésta es la primera guía de la solución. Tiene dos finalidades principales: ayudarle a tomar decisiones bien informadas sobre si esta solución es adecuada para su organización, y ofrecerle información exhaustiva acerca del diseño técnico de la solución y las razones que motivaron dicho diseño.

La guía se divide en tres partes; cada una de éstas es la sucesión lógica de la anterior. La primera parte (capítulo 2) trata de las razones comerciales para utilizar LAN inalámbricas (WLAN) y las evalúa teniendo en cuenta las amenazas de seguridad que suponen graves vulnerabilidades de muchas implementaciones de WLAN. Esta argumentación se utiliza como punto de partida para sugerir una estrategia de implementación segura de WLAN. La segunda parte (capítulo 3) desarrolla un diseño de solución lógica a partir de la estrategia de WLAN sugerida e identifica los principales componentes que se deben implementar. La tercera parte incluye los capítulos 4, 5 y 6, que constituyen la sección principal de la guía. En estos capítulos se define el diseño pormenorizado de cada uno de los componentes identificados en el capítulo 3. Las subsecciones siguientes ofrecen información detallada sobre el contenido de los capítulos.

A diferencia de muchas guías de planeamiento, ésta tiene un carácter preceptivo deliberado cuya finalidad es producir un único diseño de trabajo que sirva como referencia para el uso de este tipo de solución. En los apartados del documento donde hay distintas opciones de diseño disponibles, se ofrece la razón para tomar la decisión elegida. Si resulta apropiado, se presentan estrategias opcionales. En estos casos, los capítulos ofrecen la información necesaria que le permitirá alejarse del diseño en caso de requerirlo su entorno. La intención en toda la guía es conseguir una única solución que se haya implementado y probado de antemano y funcione exactamente como se describe en las guías.

Los destinatarios principales de esta guía son los diseñadores de arquitecturas de TI y los responsables de la toma de decisiones de la organización (si bien sólo el capítulo 2 es de especial importancia para los últimos). Los arquitectos encontrarán la información relevante a sus tareas en los capítulos 2 y 3 y en los datos técnicos que se incluyen en los capítulos restantes. Los profesionales de TI dedicados a la generación, implementación y administración de esta solución deberán familiarizarse con la arquitectura y diseño globales de la solución presentada en estos capítulos.

Los profesionales de seguridad de TI también deben leer esta guía, sobre todo los últimos capítulos. Es muy importante que los responsables de la seguridad de TI de la organización lean y aprueben las instrucciones de diseño, generación y funcionamiento antes de realizar ninguna implementación y de poner el sistema en fase de producción.

##### Capítulo 2: Determinación de una estrategia segura para redes inalámbricas

Este capítulo se centra en la selección de una solución técnica para el uso seguro de redes inalámbricas. El capítulo se centra en las razones empresariales que justifican la adopción de tecnología WLAN y en los obstáculos de seguridad que deben superarse para adoptarla de forma segura. Seguidamente se ocupa de las opciones para hacer frente a estos problemas de seguridad y sugiere soluciones basadas en autenticación segura y protección de datos, haciendo uso de los certificados de claves públicas. La decisión se basa en las necesidades de seguridad probadas de organizaciones medianas y grandes. Se trata de conseguir un equilibrio entre las necesidades inmediatas de una seguridad eficaz y una visión a largo plazo de cómo la solución protegerá la inversión realizada.

##### Capítulo 3: Arquitectura de la solución de LAN inalámbrica segura

En este capítulo se estudia el diseño de la arquitectura de la solución inalámbrica segura. El punto de partida es una introducción al funcionamiento de una solución de WLAN basada en 802.1X y el protocolo de autenticación extensible - protocolo de seguridad de la capa de transporte (EAP - TLS, Extensible Authentication Protocol–Transport Layer Security Protocol). También se consideran los componentes clave de dicha solución:

-   una infraestructura de WLAN que admita una autenticación eficaz y estándares de protección de datos.

-   una infraestructura de autenticación de RADIUS.

-   una PKI.

Los requisitos de seguridad del capítulo anterior se unen al perfil de la organización de destino y se utilizan para elaborar un conjunto de criterios de diseño para la solución. A continuación se describe un diseño lógico basado en dichos criterios, en el que se muestran las opciones para modificar el tamaño y ajustarlo a organizaciones de distintos tamaños.

Por último, el capítulo muestra algunas de las formas en que se puede utilizar el diseño propuesto como punto de partida para generar otras soluciones de acceso a redes, por ejemplo una red privada virtual (VPN) o el control de acceso a la red por cable. Se ofrece también una breve descripción de cómo se puede aprovechar el componente PKI del diseño para ofrecer compatibilidad con una gran variedad de servicios y aplicaciones de seguridad.

##### Capítulo 4: Diseño de la infraestructura de claves públicas

En este capítulo se describe, paso a paso, el diseño de una PKI basada en Servicios de Certificate Server de Microsoft. Además de la seguridad de WLAN, es probable que muchas organizaciones deseen utilizar su PKI para otras aplicaciones: correo electrónico seguro, cifrado de archivos, inicio de sesión de tarjeta inteligente, etc. Por ello, el diseño es un equilibrio entre una solución de certificado relativamente sencilla y de bajo costo para WLAN seguras y otra que ofrezca la flexibilidad y seguridad suficientes para poder ampliarse y admitir aplicaciones distintas.

La documentación de sus necesidades de certificado va seguida del diseño de una jerarquía de entidades emisoras de certificados (CA) adecuada. También se trata de la integración de estas entidades emisoras de certificados con Active Directory, Internet Information Services (IIS) y otras infraestructuras de claves públicas. Finalmente se describe el desarrollo de un plan de administración de certificados y la creación de plantillas de certificado.

##### Capítulo 5: Diseño de una infraestructura de RADIUS para la seguridad de LAN inalámbricas

Este capítulo presenta un diseño pormenorizado de la infraestructura de RADIUS.  Dicha infraestructura proporciona autenticación segura y servicios de administración de claves segura a la WLAN. El capítulo ofrece información general acerca del uso de RADIUS, implementado mediante el servicio de autenticación de Internet (IAS, Internet Authentication Service) de Microsoft, para proporcionar una solución de administración de acceso a la red y su aplicación a las WLAN en concreto. Se enumeran los requisitos previos del entorno para la solución y se describen minuciosamente las decisiones que deben tomarse al diseñar la arquitectura de la infraestructura de RADIUS para una WLAN 802.1X. También se presentan las estrategias de administración para el mantenimiento de la infraestructura de servidores IAS en el futuro.

##### Capítulo 6: Diseño de la seguridad para LAN inalámbrica mediante 802.1X

Este capítulo describe la arquitectura y el diseño de los aspectos de seguridad concernientes a las redes inalámbricas. (No se incluyen cuestiones de diseño de las redes inalámbricas ajenos a la seguridad.) Los temas tratados incluyen la forma en que una solución basada en 802.1X afronta los errores de seguridad de WLAN básicas de privacidad equivalente por cable (WEP, Wired Equivalent Privacy), la decisión de utilizar certificados en lugar de contraseñas y la identificación de los requisitos previos para lograr una implementación satisfactoria. Las secciones siguientes se ocupan de la elección de opciones de seguridad de WLAN y la configuración de dichas opciones en la directiva de acceso de RADIUS, puntos de acceso (AP) inalámbricos y clientes (mediante la directiva de grupo). Por último, en el capítulo se describen aspectos clave de la implementación, como el tratamiento de los perfiles móviles y la aplicación de bootstrap a la configuración de clientes exclusivamente inalámbricos.

#### Guía de generación: capítulos 7 al 9

Esta guía proporciona instrucciones paso a paso para la implementación de todos los componentes de la solución: una PKI basada en Servicios de Certificate Server de Windows Server 2003, una infraestructura de RADIUS basada en IAS y la configuración de clientes y puntos de acceso (AP) inalámbrico. Cada capítulo presenta los procedimientos detallados para instalar y proteger el sistema operativo, configurar los componentes de software e integrarlos en la solución. Los pasos principales aparecen vinculados a procedimientos de comprobación que contribuyen a evitar errores.

Los destinatarios principales de esta guía son los profesionales de TI que participan en el diseño, generación e implementación de los componentes PKI, RADIUS y WLAN. Entre estos usuarios se incluyen los profesionales de ingeniería de TI que participan en el diseño y la especificación de infraestructuras de TI y los proveedores de TI responsables de la implementación de soluciones en entornos de producción.

Los pasos de generación permitirán a los arquitectos de TI asegurarse de que la solución se ajusta a los estándares y prácticas de la organización. Sin embargo, gran parte de la información que contienen estos capítulos no será de relevancia para estos usuarios. Es posible que los profesionales de seguridad de TI deseen leer esta guía después de leer la Guía de planeamiento. Como ya mencionamos anteriormente, es muy importante que los responsables de la seguridad de TI de la organización lean y aprueben las instrucciones de diseño, generación y funcionamiento antes de realizar la implementación.

Los directores de operaciones y asistencia técnica de TI responsables de los componentes de esta solución se beneficiarán de la consulta de estos capítulos para comprender las interdependencias entre los componentes de la solución y el resto de la infraestructura de TI. Los profesionales de asistencia técnica necesitarán utilizar esta guía y la guía de planeamiento como referencia.

##### Capítulo 7: Implementación de la infraestructura de claves públicas

Este capítulo ofrece instrucciones detalladas para la generación de la PKI de la solución, incluida la preparación del hardware y el sistema operativo para los servidores de CA, la aplicación de directivas de seguridad a los servidores y la disposición de la infraestructura de apoyo para la PKI (IIS y Active Directory). A continuación se lleva a cabo la instalación y configuración de Servicios de Certificate Server para generar una CA raíz sin conexión y CA emisoras. Adicionalmente se ofrece una explicación de la configuración de la PKI cliente mediante Active Directory y la directiva de grupo, así como de la delegación de tareas de configuración y administración. Esto proporciona la infraestructura de certificados que utilizan los capítulos posteriores de esta guía para crear la solución completa.

##### Capítulo 8: Implementación de la infraestructura de RADIUS

Este capítulo describe la implementación de la infraestructura de RADIUS de la solución, incluido el proceso de preparación y montaje de servidores, la aplicación de directivas de seguridad, la preparación de grupos de seguridad de Active Directory y, finalmente, la configuración del servicio de autenticación de Internet (IAS) en cada servidor. El resultado es una infraestructura de RADIUS resistente que proporciona los componentes de autenticación y autorización de la solución.

##### Capítulo 9: Implementación de la infraestructura de seguridad para LAN inalámbricas

Este capítulo se ocupa de la configuración de la solución de seguridad de WLAN con los componentes PKI y RADIUS generados en los capítulos anteriores. Entre los temas tratados se incluye la preparación de la infraestructura de red (DHCP, o protocolo de configuración dinámica de host, y Active Directory), la creación y emisión de los tipos de certificado correctos, la creación de directivas de acceso remoto en los servidores IAS y la configuración de puntos de acceso (PA) inalámbricos para utilizarlos en la nueva infraestructura de RADIUS. En este capítulo se completa la instalación de la solución.

#### Guía de operaciones: capítulos 10 al 12

Esta guía describe los procedimientos para el mantenimiento a largo plazo de los componentes de la solución. Las soluciones de Microsoft para la administración (MSM, Microsoft Solutions for Management) sirven de base a esta guía, que proporciona una serie completa de tareas e instrucciones para operar, supervisar, modificar y facilitar el funcionamiento correcto de los componentes de IAS y los Servicios de Certificate Server. Se presentan tareas de configuración para implementar el sistema de administración (incluidas secuencias de comandos para procesos de supervisión y comprobación diarios y semanales), procedimientos de copia de seguridad y recuperación y recursos para la solución de problemas.

A diferencia de lo que ocurre con otras guías que forman parte de esta solución, no es necesario llevar a cabo una lectura exhaustiva de estos capítulos. Cada uno de los capítulos principales consta de dos partes. La primera es relativamente corta y su objetivo es el de proporcionarle toda la información necesaria para planear y configurar la infraestructura técnica y los procesos. Realice una lectura completa de esta parte. La segunda parte comprende mayoritariamente material de referencia que documenta todas las operaciones y tareas de soporte necesarias para el mantenimiento de los componentes de la solución.

Los destinatarios principales de esta guía son los profesionales de TI que se ocupan de la administración de los componentes PKI, RADIUS y WLAN de la solución. En muchas organizaciones, es posible que los encargados del mantenimiento de los distintos componentes de la solución sean personas diferentes o incluso departamentos diferentes de la organización; por ello, no todos los capítulos serán de interés para todas las personas o grupos.

Los arquitectos de TI deben familiarizarse con el contenido de estos capítulos para comprender el impacto global que los requisitos operativos de esta solución tienen en la totalidad de la infraestructura de TI. Sin embargo, gran parte de la información que contienen estos capítulos no será de relevancia para estos usuarios. En caso de que los arquitectos realicen modificaciones en el diseño descrito en la guía de planeamiento, deberán mantener a los encargados de la administración del servicio de TI informados al respecto, de modo que puedan llevarse a cabo los cambios correspondientes en la guía operativa.

Los profesionales de TI al cargo de la generación e implementación de la infraestructura de TI de la organización necesitarán conocer el contenido de esta guía en términos generales. Esto les permitirá transmitir eficazmente la información necesaria acerca de la generación e implementación de la solución al personal de administración del servicio de TI.

Los profesionales de seguridad de TI deben leer esta guía tras la lectura de las guías de planeamiento y generación para garantizar que las prácticas operativas se ajustan a los estándares de seguridad de la empresa.

##### Capítulo 10: Introducción a la guía de operaciones

En este capítulo se ofrece información general sobre Microsoft Operations Framework (MOF) y datos esenciales para una comprensión satisfactoria de los dos capítulos siguientes. Si no está familiarizado con los conceptos de MOF, lea la información general a la que se hace referencia en la sección "Información adicional" al final de este capítulo.

##### Capítulo 11: Administración de la infraestructura de claves públicas

La finalidad de este capítulo es permitirle implementar un sistema de administración completo para su PKI. Esto incluye todas las tareas de instalación necesarias para empezar a supervisar y mantener el sistema, las tareas operativas normales necesarias para su funcionamiento correcto y los procedimientos que le ayudarán a solucionar los problemas de compatibilidad, administrar los cambios del entorno y optimizar el rendimiento del sistema.

##### Capítulo 12: Administración de la infraestructura de seguridad de LAN inalámbrica y RADIUS

La finalidad de este capítulo es permitirle implementar un sistema de administración completo para la infraestructura de seguridad de LAN inalámbrica (WLAN) y del servidor del Servicio de usuario de acceso telefónico de autenticación remota (RADIUS). Al igual que el capítulo anterior, contiene todas las tareas de instalación necesarias para empezar a supervisar y mantener el sistema, las tareas operativas típicas y necesarias para su funcionamiento correcto y los procedimientos que le ayudarán a solucionar los problemas de compatibilidad, administrar los cambios del entorno y optimizar el rendimiento del sistema.

##### Guía de prueba: capítulo 13

La guía de prueba ocupa el capítulo 13 con una explicación de la estrategia de prueba global utilizada por Microsoft para validar esta solución. Además ofrece una descripción de los casos de prueba principales que puede utilizar para validar la solución en los laboratorios de su organización. El desarrollo del capítulo se llevó a cabo a partir de los procesos y casos de prueba utilizados por Microsoft para validar la solución en sus laboratorios. Se incluye la serie completa de los casos de prueba estudiados. Adicionalmente, esta solución se sometió a una prueba de infiltración llevada a cabo por una tercera parte.

#### Apéndices y archivos complementarios

Los apéndices siguientes vienen incluidos con las guías de la solución.

##### Apéndice A: Matriz de compatibilidad con la plataforma

Se trata de una tabla que proporciona detalles sobre las versiones de sistemas operativos compatibles con los clientes inalámbricos y las diferentes funciones de servidor en la solución.

##### Apéndice B: Secuencias de comandos y archivos auxiliares

Los procedimientos presentados en las guías de generación y operaciones hacen uso de varias secuencias de comandos y otros archivos auxiliares. Este apéndice ofrece una descripción de estos componentes, así como del archivo Léame.txt aparte que se proporciona con las secuencias.

##### Apéndice C: Guía de entrega

El apéndice C presenta una estructura basada en Microsoft Solutions Framework (MSF) y MSM que puede servir de ayuda a la hora de implementar la solución.

##### Apéndice D: Compatibilidad con WPA

Este apéndice incluye información sobre el estado de la compatibilidad de la solución en lo que respecta a seguridad de acceso protegido Wi-Fi (WPA, WiFi Protected Access). La solución está diseñada para ofrecer compatibilidad con WPA y las guías incluyen numerosas referencias a este estándar. Sin embargo, la compatibilidad de WPA con Windows XP, así como con puntos de acceso y adaptadores de WLAN no estaba completamente resuelta cuando la solución se encontraba en proceso de desarrollo.

[](#mainsection)[Principio de la página](#mainsection)

### Convenciones de estilo

La tabla siguiente describe las convenciones estilísticas utilizadas en este manual.

**Tabla 1.1: Convenciones de estilo**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Negrita</strong></td>
<td style="border:1px solid black;">Caracteres que se escriben exactamente tal y como se muestran, incluidos comandos y modificadores. Los elementos de la interfaz de usuario que aparecen en el texto con carácter normativo también se muestran en negrita.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><em>Cursiva</em></td>
<td style="border:1px solid black;">Este tipo de fuente se utiliza en dos contextos:
cuando aparece en la sección de texto principal, indica el título de otro documento.
cuando se utiliza como parte de comandos o código (o en texto que hace referencia a comandos o código), indica un marcador de posición para variables que deben reemplazarse por valores específicos. Por ejemplo, <em>nombre_de_archivo.ext</em> indica que debe reemplazar el <em>nombre_de_archivo.ext</em> en cursiva con el nombre de archivo de su elección.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Texto de pantalla</td>
<td style="border:1px solid black;">Utilizado para texto que se muestra en pantalla (por ejemplo, el resultado de una herramienta de línea de comandos) y para comandos que necesitan especificarse en la línea de comandos.
Algunos comandos no caben en el espacio de la página restringido por los márgenes. En este caso, el texto de comando se divide en varias líneas con sangría (esto aparece indicado por una nota que sigue al comando).</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><pre><code>Monospace font</code></pre></td>
<td style="border:1px solid black;">Ejemplos de código y contenido de los archivos de configuración.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">%SystemRoot%</td>
<td style="border:1px solid black;">La carpeta en la que se ha instalado el sistema operativo Windows.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Nota</strong></td>
<td style="border:1px solid black;">Avisa al lector de que hay información adicional.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Importante</strong></td>
<td style="border:1px solid black;">Avisa al lector de información adicional esencial para completar la tarea.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Precaución</strong></td>
<td style="border:1px solid black;">Avisa al lector de que si no se realiza o pasa por alto una determinada acción, se podrá producir una pérdida de datos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Advertencia</strong></td>
<td style="border:1px solid black;">Avisa al lector de que si no se realiza o pasa por alto una determinada acción, el usuario o el hardware podría resultar dañado físicamente.</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Comentarios y soporte técnico
  
Si necesita asistencia adicional con la implementación de las tecnologías tratadas en esta solución, quizás le resulte de utilidad contactar con la oficina de Microsoft más cercana o con un socio de Microsoft Services.
  
-   Para averiguar cuál es la oficina de Microsoft más cercana a usted, visite el sitio Web de [Microsoft Worldwide](http://www.microsoft.com/worldwide/) en http://www.microsoft.com/worldwide/ y seleccione el país y la región apropiados.
  
-   Si desea encontrar un socio de Microsoft en su zona, busque en la sección de **soluciones y servicios** del [directorio de recursos de Microsoft](http://directory.microsoft.com/resourcedirectory/solutions.aspx) en http://directory.microsoft.com/ResourceDirectory/Solutions.aspx
  
-   Para obtener más información sobre la compatibilidad de los componentes de Windows Server 2003 utilizados en la solución, incluidas rutas de traslado, aspectos de soporte, recursos y niveles de compatibilidad, consulte el sitio Web de [ayuda y soporte técnico de Microsoft](http://support.microsoft.com/) en http://support.microsoft.com/
  
Microsoft valora su opinión acerca de este material. Especialmente procure responder las preguntas siguientes:
  
-   ¿En qué medida ha resultado útil la información proporcionada?
  
-   ¿Los procedimientos paso a paso fueron precisos?
  
-   ¿Los capítulos le resultaron fáciles de leer e interesantes?
  
-   ¿Cómo calificaría esta guía en líneas generales?
  
Envíe su opinión a [SecWish@Microsoft.com](mailto:secwish@microsoft.com?subject=feedback%20re:%20microsoft%20solution%20for%20secure%20wireless%20lans)
  
[](#mainsection)[Principio de la página](#mainsection)
