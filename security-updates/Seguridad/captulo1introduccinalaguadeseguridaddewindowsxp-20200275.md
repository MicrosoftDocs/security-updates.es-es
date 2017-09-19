---
TOCTitle: 'Capítulo 1: Introducción a la Guía de seguridad de Windows XP'
Title: 'Capítulo 1: Introducción a la Guía de seguridad de Windows XP'
ms:assetid: '4eddb4e4-fd7b-444c-8484-bb8ee220c0e1'
ms:contentKeyID: 20200275
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163069(v=TechNet.10)'
---

Guía de seguridad de Windows XP
===============================

### Capítulo 1: Introducción a la Guía de seguridad de Windows XP

Actualizado: 20/10/05

##### En esta página

[](#ehaa)[Información general](#ehaa)
[](#egaa)[Resumen ejecutivo](#egaa)
[](#efaa)[Destinatarios de la guía](#efaa)
[](#eeaa)[Ámbito de esta guía](#eeaa)
[](#edaa)[Descripción general del capítulo](#edaa)
[](#ecaa)[Descarga de contenido](#ecaa)
[](#ebaa)[Convenciones de estilo](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Información general

Bienvenido a la *Guía de seguridad de Windows XP.* Esta guía se ha elaborado para proporcionarle la mejor información disponible que le permita evaluar y hacer frente a los riesgos de seguridad específicos de Microsoft® Windows® XP Professional con Service Pack 2 (SP2) en su entorno. Los capítulos de esta guía proporcionan información detallada sobre cómo configurar características y parámetros de seguridad mejorados en Windows XP para hacer frente a las posibles amenazas que se identifiquen en el entorno. Esta guía se diseñó teniendo en mente a los consultores, diseñadores o ingenieros de sistemas que trabajan en entornos Windows XP.

La información de esta guía ha sido revisada y aprobada por equipos de ingeniería, consultores, ingenieros de soporte técnico, socios y clientes de Microsoft para ofrecer un material:

-   **Probado**. Basado en la experiencia de campo.

-   **Serio**. Ofrece el mejor asesoramiento disponible.

-   **Preciso**. Validado y probado desde el punto de vista técnico.

-   **Aplicable**. Proporciona los pasos necesarios para ejecutar el procedimiento con éxito.

-   **Útil**. Aborda problemas de seguridad reales.

Se elaboraron prácticas recomendadas para proteger tanto los equipos cliente como los servidores. De este desarrollo se encargaron consultores e ingenieros de sistemas que han implementado Windows XP Professional, Microsoft Windows Server™ 2003 y Windows 2000 en una diversidad de entornos. Esas prácticas recomendadas se detallan en la guía. También se incluyen recomendaciones, procedimientos e instrucciones de seguridad paso a paso para ayudarle a aumentar al máximo el nivel de seguridad de los equipos de su organización en los que se ejecuta Windows XP Professional con SP2.

Si precisa información más detallada de los conceptos que se presentan en este material, consulte *Amenazas y contramedidas: configuración de seguridad de Windows* *Server 2003 y Windows* *XP*, el kit de recursos de *Microsoft Windows* *XP*, el kit de recursos de *Microsoft Windows* *Server 2003*, el kit de recursos de seguridad de *Microsoft Windows* y Microsoft TechNet.

Esta guía se creó originalmente para Windows XP con SP1. La presente versión actualizada, en la que se reflejan las considerables mejoras en materia de seguridad que proporciona Windows XP con SP2, se desarrolló y fue probada en equipos en los que se ejecuta Windows XP Professional con SP2. Todas las referencias a Windows XP de esta guía son relativas a Windows XP con SP2, a menos que se indique lo contrario.

[](#mainsection)[Principio de la página](#mainsection)

### Resumen ejecutivo

Sea cual sea el entorno, es recomendable tomarse muy en serio los aspectos relacionados con la seguridad. En muchas organizaciones se subestima el valor del entorno de tecnología de la información (TI); a menudo, porque se excluyen costos indirectos sustanciales. Si un ataque a los servidores del entorno resulta ser lo suficientemente grave, toda la organización podría verse seriamente afectada. Por ejemplo, un ataque que provoque que su sitio web deje de estar disponible y cause una importante pérdida de ingresos o de confianza de los clientes puede provocar el desplome de la rentabilidad de su organización. A la hora de evaluar los costos de seguridad deben incluirse los costos indirectos asociados a cualquier ataque, además de los relativos a la pérdida de funcionalidad de TI.

Un análisis de la situación, la vulnerabilidad y los riesgos en lo que respecta a la seguridad puede informar de las concesiones que hay que hacer para equilibrar la seguridad y la capacidad de uso, y a las que quedan sujetos todos los sistemas informáticos en un entorno conectado en red. En esta guía se detallan las principales contramedidas relacionadas con la seguridad disponibles en Windows XP con SP2, las vulnerabilidades a las que hacen frente y las posibles consecuencias negativas (en caso de que las hubiera) de la implementación de cada una de las contramedidas.

La guía proporciona recomendaciones específicas para configurar la seguridad de equipos en los que se ejecuta Windows XP con SP2 en tres entornos comunes:

-   **Cliente de empresa (EC)**. En este entorno, los equipos cliente están ubicados en un dominio de servicio de directorio de Active Directory® y sólo es necesario que se comuniquen con sistemas en los que se ejecuta Windows 2000 o versiones posteriores del sistema operativo Windows.

-   **Independiente (SA).** En este entorno, los equipos cliente no son miembros de un dominio Active Directory y puede que sea necesario que se comuniquen con sistemas en los que se ejecuta Windows NT® 4.0.

-   **Seguridad especializada: Funcionalidad limitada (SSLF)**. La preocupación por la seguridad en este entorno llega a tal punto que resulta aceptable una pérdida significativa de la funcionalidad y la capacidad de administración. Por ejemplo, los equipos del ejército y de las agencias de inteligencia funcionan en este tipo de entorno.

La guía se ha organizado de forma que pueda encontrar rápidamente la información que necesita para determinar la configuración que mejor se adapta a las características de los equipos de su organización en los que se ejecuta Windows XP con SP2. Aunque, en esencia, va destinada a los clientes empresariales, buena parte de su contenido puede servir a organizaciones de cualquier tamaño.

Para sacar el máximo provecho de este material, deberá leer la totalidad de la guía. El equipo que la ha elaborado espera que el material le resulte útil, informativo e interesante. Para obtener más información, también puede consultar la guía complementaria [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que se puede descargar en http://go.microsoft.com/fwlink/?LinkId=15159.

[](#mainsection)[Principio de la página](#mainsection)

### Destinatarios de la guía

Esta guía va destinada principalmente a consultores, expertos en seguridad, arquitectos de sistemas y profesionales de TI encargados de planear el desarrollo de las aplicaciones o la infraestructura y la implementación de estaciones de trabajo Windows XP en un entorno de empresa. Esta guía no se ha diseñado para los usuarios domésticos. Está pensada para aquellas personas cuyas funciones laborales se incluyan dentro de las siguientes:

-   Arquitectos de sistemas y programadores responsables de las tareas en materia de arquitectura para los equipos de sus organizaciones.

-   Expertos en seguridad de TI que se centran en garantizar la seguridad de las distintas plataformas de la organización.

-   Analistas de negocio y responsables de la toma de decisiones con requisitos y objetivos empresariales de vital importancia para los que se precisen equipos portátiles y de escritorio con el soporte de TI.

-   Consultores de socios y servicios de Microsoft que precisen herramientas de transferencia de conocimientos para asociados y clientes empresariales.

#### Capacitación y conocimientos previos

Disponer de la capacitación y los conocimientos que se señalan a continuación es un requisito con el que deben contar los administradores y arquitectos encargados de desarrollar, implementar y garantizar la seguridad de los equipos cliente Windows XP en una empresa.

-   MCSE 2000 o una certificación posterior con más de dos años de experiencia en materia de seguridad o equivalente.

-   Conocimientos detallados del dominio de la organización y de entornos de Active Directory.

-   Uso de herramientas de administración, entre las que se incluyen MMC, Secedit, Gpupdate y Gpresult.

-   Experiencia en la administración de Directiva de grupo.

-   Experiencia en la implementación de aplicaciones y equipos cliente en entornos empresariales.

[](#mainsection)[Principio de la página](#mainsection)

### Ámbito de esta guía

Esta guía se centra en cómo crear y mantener un entorno seguro para equipos de escritorio portátiles en los que se ejecuta Windows XP Professional con SP2. En la guía se explican las distintas etapas para configurar la seguridad de tres entornos diferentes y qué objetivo tienen los parámetros de los equipos de escritorio y portátiles que se implementan en cada caso. Se proporciona información para los entornos de Cliente de empresa (EC), Independiente (SA) y Seguridad Especializada: Funcionalidad limitada (SSLF).

No se describen configuraciones no recomendadas específicamente como parte de esta guía. Para obtener información más detallada acerca de todos los parámetros de seguridad en Windows XP, consulte la guía complementaria [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159) en http://go.microsoft.com/fwlink/?LinkId=15159.

#### Cliente de empresa

El entorno de cliente de empresa (EC) se compone de un dominio de Active Directory Windows 2000 o Windows Server 2003. Los equipos cliente de este entorno se administrarán mediante la característica Directiva de grupo, que se aplica a sitios, dominios y unidades organizativas (UO). Directiva de grupo proporciona un método centralizado para administrar la directiva de seguridad en todo el entorno.

#### Entorno de cliente independiente

El entorno de cliente independiente (SA) incluye equipos cliente que no se pueden unir a un dominio ni equipos miembros de un dominio Windows NT 4.0. Estos equipos cliente se tienen que configurar a través de la directiva local. La administración de equipos independientes puede constituir un desafío considerablemente mayor que la administración de cuentas de usuario y directivas en un dominio Active Directory.

#### Seguridad especializada: Funcionalidad limitada

El entorno Seguridad especializada: Funcionalidad limitada (SSLF) proporciona parámetros de configuración de seguridad elevada para equipos cliente. Cuando se aplican estas configuraciones de directiva de seguridad, los usuarios pueden ver reducida la funcionalidad notablemente porque queda limitada a las funciones específicas que se requieren para las tareas que resultan necesarias. El acceso queda restringido a entornos de infraestructura, servicios y aplicaciones aprobadas. En esencia, las configuraciones de directiva de seguridad en el entorno SSLF sólo se aplican a algunos sistemas en un número muy reducido de organizaciones, como los organismos militares y las agencias de inteligencia. Estas configuraciones tienden a anteponer la seguridad sobre la capacidad de administración y de uso; sólo deben utilizarse en equipos que si quedasen expuestos podrían causar pérdidas económicas significativas o incluso poner vidas en riesgo. Es decir, la configuración SSLF no constituye una buena elección para la mayoría de las organizaciones.

[](#mainsection)[Principio de la página](#mainsection)

### Descripción general del capítulo

Windows XP con SP2 proporciona la versión más fiable de un sistema operativo cliente Windows hasta la fecha, con características mejoradas en materia de seguridad y privacidad. Se ha optimizado la seguridad global en Windows XP para garantizar a las organizaciones que puedan trabajar en un entorno informático más seguro y protegido. La *Guía de seguridad* de *Windows* XP consta de siete capítulos. Los capítulos dos a seis tratan acerca de los procedimientos necesarios para crear un entorno de ese tipo. Cada uno de estos capítulos se basa en un proceso de extremo a extremo diseñado para proteger los equipos Windows XP.

#### Capítulo 1: Introducción a la Guía de seguridad de Windows XP

Este capítulo reúne información general sobre la guía, que incluye descripciones de la audiencia de destino, problemas que se tratan y finalidad principal de la guía.

#### Capítulo 2: Configuración de la infraestructura de dominios de Active Directory

Puede utilizar Directiva de grupo para administrar entornos de equipos y usuarios en dominios Windows Server 2003 y Windows 2000. Constituye una herramienta esencial para garantizar la seguridad de Windows XP y se puede utilizar para aplicar y mantener una directiva de seguridad coherente en una red desde una ubicación central. En este capítulo se describen los pasos preliminares que se deben llevar a cabo en el dominio antes de aplicar Directiva de grupo a los equipos cliente Windows XP.

La configuración de Directiva de grupo se almacena en objetos de directiva de grupo (GPO) en controladores de dominio. Los GPO se vinculan a sitios, dominios y unidades organizativas (UO) dentro de la estructura de Active Directory. Dado que la directiva de grupo está tan estrechamente integrada con Active Directory, es importante tener un conocimiento básico de las implicaciones de seguridad y la estructura de Active Directory antes de implementarla.

#### Capítulo 3: Configuración de seguridad para clientes Windows XP

En este capítulo se describe la configuración de seguridad para equipos cliente Windows XP que se puede establecer a través de Directiva de grupo en un dominio Active Directory Windows 2000 o Windows Server 2003. No se proporciona información de todas las opciones de configuración disponibles; sólo de las que ayudarán a proteger un entorno de la mayoría de las amenazas actuales. La guía permite también a los usuarios seguir realizando funciones típicas de su trabajo en los equipos. Las opciones que configuren se deben basar en los objetivos de seguridad de la organización.

#### Capítulo 4: Plantillas administrativas para Windows XP

Este capítulo trata sobre las opciones de configuración que se pueden agregar a Windows XP mediante plantillas administrativas. Las plantillas administrativas son archivos Unicode que puede utilizar para configurar los valores basados en el Registro que determinan el comportamiento de un gran número de servicios, aplicaciones y componentes del sistema operativo. Hay numerosas plantillas administrativas que se pueden utilizar con Windows XP y que contienen centenares de parámetros de configuración.

#### Capítulo 5: Seguridad de clientes Windows XP independientes

Aunque la mayor parte de esta guía se centra en los entornos de Cliente de empresa (EC) y Seguridad especializada: Funcionalidad limitada (SSLF), en este capítulo se trata también sobre la configuración de equipos cliente Windows XP independientes. Microsoft recomienda que Windows XP se implemente en una infraestructura de dominios de Active Directory, si bien reconoce que no es siempre posible. En este capítulo se proporciona orientación acerca de cómo aplicar las configuraciones recomendadas a equipos cliente Windows XP con SP2 que no sean miembros de un dominio Windows 2000 ni Windows Server 2003.

#### Capítulo 6: Directiva de restricción de software para clientes Windows XP

En este capítulo se proporciona información general básica de la directiva de restricción de software, que proporciona a los administradores un mecanismo controlado por directivas para identificar y limitar el software que se puede ejecutar en su dominio. Los administradores pueden utilizar una directiva de restricción de software para evitar que se ejecuten programas no deseados e impedir la propagación de virus, troyanos u otro tipo de código con fines malintencionados. Las directivas de restricción de software se integran completamente con Active Directory y Directiva de grupo. También pueden ser utilizadas en un entorno sin una infraestructura de dominios Windows Server 2003 cuando se aplican únicamente al equipo local.

#### Capítulo 7: Conclusión

En el capítulo final se revisan los puntos importantes de la guía en un breve resumen de la información presentada en los capítulos anteriores.

#### Apéndice A: Opciones clave que se deben considerar

Aunque en esta guía se tratan numerosas contramedidas y opciones de seguridad, debe tenerse presente que algunas son especialmente importantes. En este apéndice se describe la configuración que tendrá mayor repercusión en la seguridad de los equipos en los que se ejecuta Windows XP con SP2.

#### Apéndice B: Prueba de la Guía de seguridad de Windows XP

En este apéndice se explica cómo se probó la *Guía de seguridad* de *Windows* XP en un entorno de laboratorio para asegurar la respuesta esperada.

[](#mainsection)[Principio de la página](#mainsection)

### Descarga de contenido

En estas instrucciones se incluyen un conjunto de plantillas de seguridad, secuencias de comandos y archivos adicionales que permiten a su organización evaluar, probar e implementar con mayor facilidad las contramedidas recomendadas.

Las plantillas de seguridad son archivos de texto que se pueden importar desde directivas de grupo basadas en dominios o aplicarse de forma local con el complemento de análisis y configuración de seguridad de Microsoft Management Console (MMC). Los procedimientos en los que se describe cómo llevar a cabo estas tareas se detallan en el capítulo 2, "Configuración de la infraestructura de dominios de Active Directory". Puede utilizar las secuencias de comandos que se incluyen con esta guía para implementar las contramedidas recomendadas en estaciones de trabajo independientes.

En el contenido de la descarga también se incluye el libro de Microsoft Excel® con la configuración de la guía de seguridad de Windows XP, en el que se documentan los parámetros incluidos en cada una de las plantillas de seguridad.

A los archivos que acompañan a esta guía se hace referencia como herramientas y plantillas. Estos archivos se incluyen en un archivo .msi dentro del archivo de WinZip autoextraíble que contiene esta guía, disponible en el Centro de descarga de Microsoft, en http://go.microsoft.com/fwlink/?LinkId=14840. Cuando ejecute el archivo .msi se creará la siguiente estructura de carpetas en la ubicación que especifique:

-   **\\Windows XP Security Guide Tools and Templates\\Security Templates**. Esta carpeta contiene todas plantillas de seguridad que se tratan en los capítulos 2 y 3 de la guía. Contiene también una hoja de cálculo de Excel con un resumen de todas las recomendaciones de la guía.

-   **\\Windows XP Security Guide Tools and Templates\\SCE Update**. Esta carpeta contiene secuencias de comandos y archivos de datos que permiten actualizar automáticamente la interfaz de usuario para el Editor de configuración de seguridad según se describe en el capítulo 3 de la guía.

-   **\\Windows XP Security Guide Tools and Templates\\Stand Alone Clients**. Esta carpeta contiene todas las secuencias de comandos y plantillas de ejemplo que se utilizan para configurar la seguridad de equipos independientes, tal como se describe en el capítulo 5 de la guía.

-   **\\Windows XP Security Guide Tools and Templates\\Test Tools**. Esta carpeta contiene herramientas relacionadas con el "Apéndice B: Prueba de la Guía de seguridad de Windows XP".

[](#mainsection)[Principio de la página](#mainsection)

### Convenciones de estilo

En esta guía se utilizan las siguientes convenciones de estilo.

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
<td style="border:1px solid black;"><p>Los títulos de libros y otras publicaciones importantes aparecen en <em>cursiva.</em></p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><em>&lt;Cursiva&gt;</em></p></td>
<td style="border:1px solid black;"><p>Los marcadores de posición establecidos en cursiva y entre corchetes angulares, &lt; <em>nombre de archivo</em>&gt;, representan variables.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><pre><code>Monospace font</code></pre></td>
<td style="border:1px solid black;"><p>Define ejemplos de código y de secuencias de comandos.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>Nota</strong></p></td>
<td style="border:1px solid black;"><p>Avisa al lector de que hay información adicional.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Importante</p></td>
<td style="border:1px solid black;"><p>Avisa al lector de que hay información adicional básica.</p></td>
</tr>  
</tbody>  
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
En este capítulo se ofrecía una introducción a la *Guía de seguridad* de *Windows* XP y se resumían los capítulos de la guía. Cuando sepa cómo se ha organizado la guía, podrá sacar el máximo provecho de las opciones clave de seguridad que se han integrado en Windows XP con SP2.
  
Para que las operaciones de seguridad se realicen correctamente y con eficacia es necesario cubrir todas las áreas que se tratan en esta guía; no basta con hacer avances sólo en una. Por eso se aconseja expresamente implementar las recomendaciones de esta guía que resulten adecuadas para su organización como parte de una arquitectura de defensa en profundidad más amplia.
  
#### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de temas relacionados con la seguridad en Windows XP Professional.
  
-   Para obtener más información acerca de la configuración de seguridad que se puede configurar en Microsoft Windows XP, consulte la guía complementaria [*Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159), que está disponible en http://go.microsoft.com/fwlink/?LinkId=15159.
  
-   Para obtener más información acerca de cómo implementar mecanismos de seguridad en servidores de manera análoga a la que se describe en esta guía, consulte la [*Guía de seguridad de Windows Server 2003*](http://go.microsoft.com/fwlink/?linkid=14845). Las recomendaciones en esta guía están diseñadas para ser aplicadas a servidores que deben ser compatibles con equipos cliente Windows XP configurados según se describe en los capítulos restantes. Esta información está disponible en línea en http://go.microsoft.com/fwlink/?LinkId=14845.
  
-   Para obtener información acerca de cómo implementar la administración de riesgos de seguridad de un modo más eficaz en su organización, consulte la [Guía de administración de riesgos de seguridad](http://go.microsoft.com/fwlink/?linkid=30794) en http://go.microsoft.com/fwlink/?LinkID=30794.
  
-   Para obtener información acerca de cómo minimizar la repercusión del software malintencionado, consulte la [Guía de defensa en profundidad antivirus](http://www.microsoft.com/spain/technet/recursos/articulos/avdind_0.mspx) en http://www.microsoft.com/spain/technet/recursos/articulos/avdind\_0.mspx.
  
-   Para obtener información acerca de cómo minimizar la dependencia del uso de contraseñas para la autenticación en su organización, consulte la [Guía de planeamiento de acceso seguro con tarjetas inteligentes](http://www.microsoft.com/spain/technet/recursos/articulos/smartcard/default.mspx) en http://www.microsoft.com/spain/technet/recursos/articulos/smartcard/default.mspx.
  
-   Para obtener información acerca de cómo observar y responder de un modo más eficaz a posibles infracciones de la seguridad en su organización, consulte la [Guía de planeamiento de supervisión de la seguridad y detección de ataques](http://www.microsoft.com/spain/technet/recursos/articulos/attack_detection/esn/default.mspx) en http://www.microsoft.com/spain/technet/recursos/articulos/attack\_detection/ESN/default.mspx.
  
-   Para obtener información más detallada acerca de cómo puede servir de ayuda en su organización [Microsoft Operations Framework (MOF)](http://www.microsoft.com/technet/itsolutions/cits/mo/mof/default.mspx), consulte www.microsoft.com/technet/itsolutions/cits/mo/mof/default.mspx.
  
-   Para obtener información acerca de la [seguridad de Microsoft Windows](http://www.microsoft.com/security/), consulte www.microsoft.com/security/.
  
-   Para obtener información acerca del servicio [Microsoft Technical Security Notifications](http://www.microsoft.com/technet/security/bulletin/notify.mspx), consulte www.microsoft.com/technet/security/bulletin/notify.asp.
  
##### Descargar
  
[![](images/Cc163069.icon_exe(es-es,TechNet.10).gif)Descargar la Guía de seguridad de Windows XP](http://go.microsoft.com/fwlink/?linkid=14840)
  
[](#mainsection)[Principio de la página](#mainsection)
