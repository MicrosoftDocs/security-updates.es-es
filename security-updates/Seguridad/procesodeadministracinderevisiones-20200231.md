---
TOCTitle: Proceso de administración de revisiones
Title: Proceso de administración de revisiones
ms:assetid: 'dc3893d5-6e12-443a-9e7d-f2b999b4bff2'
ms:contentKeyID: 20200231
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc700831(v=TechNet.10)'
---

Proceso de administración de revisiones
=======================================

### Fase 2: Identificación

Actualizado: junio 1, 2007

##### En esta página

[Descripción del módulo](#eyc)

[Objetivos](#end)

[Aplicable a](#ezd)

[Uso del módulo](#e6d)

[Información general](#ete)

[Detectar una nueva actualización de software](#eif)

[Determinar si las actualizaciones de software son relevantes](#ebbac)

[Obtener y comprobar los archivos fuente de la actualización de software](#ekeac)

[Decidir la naturaleza de la actualización de software y enviar RFC](#eciac)

[Resumen](#e3iac)

[Paso a la fase de evaluación y planeación](#emjac)

Descripción del módulo
----------------------

En este módulo se describe la segunda fase, Identificación, del proceso de administración de actualizaciones de cuatro fases. La fase de identificación está relacionada con el descubrimiento confiable de nuevas actualizaciones de software, si las nuevas actualizaciones son importantes para su entorno de producción y si una actualización representa un cambio normal o de emergencia.

El objetivo de este módulo es describir los principios de la fase de identificación del proceso de administración de actualizaciones, así como ofrecer una introducción de los tipos de tareas que le permitirán llevar a cabo la identificación mediante Microsoft Windows Server Update Service (WSUS) y Microsoft Systems Management Server (SMS).

**Nota:** la versión beta 2 del próximo lanzamiento de SMS, denominada System Center Configuration Manager 2007, está disponible para su descarga en <http://www.microsoft.com/technet/sms/2007/evaluate/download.mspx>. Con excelentes mejoras en simplicidad, configuración, implementación y seguridad, Configuration Manager 2007 simplifica en gran medida la implementación del sistema, la automatización de tareas, la administración del cumplimiento de normativas así como la administración de la seguridad basada en directivas, lo cual permite la mejora de la agilidad empresarial.

Después de leer este módulo podrá planear las tareas que necesita para:

-   Detectar nuevas actualizaciones de software.

-   Determinar si se requieren nuevas actualizaciones en su entorno.

-   Determinar si una actualización requiere implementación de actualizaciones estándar o de emergencia.

Sin un proceso de identificación, no sabrá qué actualizaciones de software están disponibles, qué actualizaciones requiere, cómo obtener actualizaciones sin virus, comprobadas y probadas y si una actualización se debe implementar rápidamente o como parte de una instalación programada.

[Principio de la página](#mainsection)

Objetivos
---------

Use este módulo para:

-   Detectar nuevas actualizaciones de software.

-   Determinar si las actualizaciones de software son relevantes.

-   Obtener archivos de origen de actualización de software confiables y seguros.

-   Clasificar la actualización de software como un cambio normal o una emergencia.

[Principio de la página](#mainsection)

Aplicable a
-----------

Este módulo se aplica a los siguientes productos y tecnologías:

-   Todos los productos y tecnologías de Microsoft

[Principio de la página](#mainsection)

Uso del módulo
--------------

Este módulo describe la fase de identificación del proceso de administración de actualizaciones de cuatro fases. Describe las tareas básicas requeridas para llevar a cabo la identificación mediante Microsoft Windows Server Update Service (WSUS) y Microsoft Systems Management Server (SMS). Se ofrecen instrucciones detalladas en las bibliotecas técnicas de WSUS y SMS indicadas más adelante.

Para obtener el máximo rendimiento del módulo:

-   lea el capítulo Introducción del módulo "Proceso de administración de actualizaciones". En este capítulo se ofrece información general de todas las fases del proceso de administración de actualizaciones de cuatro fases y se proporciona una introducción a las herramientas disponibles para aplicar la administración de actualizaciones en los entornos del sistema operativo Microsoft Windows.

-   Use las bibliotecas técnicas de WSUS y SMS para obtener materiales de referencia más detallados. Estas bibliotecas se encuentran en:

    -   [Biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true)

    -   [Biblioteca técnica de Systems Management Server 2003](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true)

[Principio de la página](#mainsection)

Información general
-------------------

La fase de identificación es la segunda fase del proceso de administración de actualizaciones que se muestra en la figura 1.

![](images/Cc700831.secmod195figure1(es-es,TechNet.10).gif)
**Figura 1 El proceso de administración de revisiones**

El objetivo de la fase de identificación es:

-   Detectar nuevas actualizaciones de software de una forma confiable.

-   Determinar si las actualizaciones de software son relevantes para su entorno de producción.

-   Obtener archivos fuente de actualización de software y confirmar que sean seguros e instalarlos correctamente.

-   Determinar si la actualización de software se debe considerar un cambio normal o una emergencia y enviar una solicitud de cambio (RFC) para implementarla. Enviar una RFC es el activador de la siguiente fase de la administración de actualizaciones: evaluación y planeación.

En el resto de este módulo se describe esos objetivos de forma más detallada. También se trata cómo puede alcanzar esos objetivos más rápidamente si trata una emergencia.

[Principio de la página](#mainsection)

Detectar una nueva actualización de software
--------------------------------------------

La identificación de una actualización de software comienza con su detección de una forma segura y confiable. La detección tiene dos componentes principales:

-   Cómo se le notifica una nueva actualización de software

-   Cómo sabe que puede confiar en la fuente y en la notificación

### Cómo se le notifica una nueva actualización de software

La detección de una nueva actualización de software comienza con la notificación. La notificación se debe proporcionar a través de una suscripción a una fuente confiable que proporcione actividades de examen e informe o por otro mecanismo de notificación confiable. Los mecanismos de notificación usados con más frecuencia son:

-   Notificaciones por correo electrónico.

-   Herramientas de examen de vulnerabilidades.

-   La página de administración del servidor WSUS.

-   La característica de administración de actualizaciones de software de SMS.

#### Notificaciones por correo electrónico

La notificación por correo electrónico es la forma más habitual de notificar actualizaciones. Una opción para la notificación por correo electrónico es suscribirse a Microsoft Security Notification Service en <http://www.microsoft.com/technet/security/bulletin/notify.mspx>. Para lanzamientos provisionales de productos, o actualizaciones de software, normalmente recibirá un mensaje de correo electrónico que le informará acerca de la disponibilidad de nuevas actualizaciones de software en el sitio web de Microsoft.

Un ejemplo de un mensaje de correo electrónico que notifique a los administradores acerca de actualizaciones nuevas de seguridad se muestra en la figura 2.

[![](images/Cc700831.secmod195figure2_l(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc700831.secmod195figure2(es-es,technet.10).gif)
**Figura 2 Ejemplo de mensaje de correo electrónico que notifica a los administradores acerca de nuevas actualizaciones de software**

### Cómo sabe que puede confiar en la fuente y en la notificación

Es importante tratar las notificaciones de correo electrónico cuidadosamente. Las siguientes instrucciones están diseñadas para ayudarle a validar cada notificación y asegurarse que es la información más reciente del boletín de seguridad disponible:

-   Elimine inmediatamente cualquier notificación de correo electrónico que pretenda ser de Microsoft que incluya archivos de software adjuntos. Nunca ejecute ni instale un archivo ejecutable adjunto a una notificación por correo electrónico.

    **Nota:** Microsoft tiene una directiva de nunca distribuir software a través de datos adjuntos al correo electrónico. Revise las directivas de Microsoft acerca de la distribución de software en <http://www.microsoft.com/technet/security/bulletin/info/swdist.mspx>.

-   No haga clic en ninguno de los vínculos directamente desde una notificación de correo electrónico. En su lugar, debe pegar las direcciones URL en una ventana de explorador para confirmar que le lleva al sitio web de Microsoft.

-   Visite siempre el sitio web del Centro de seguridad de Microsoft Technet en <http://www.microsoft.com/technet/security/default.mspx> para leer los detalles de autorización de un boletín de seguridad. Como alternativa, si no espera tener acceso a Internet cuando reciba los boletines, familiarícese con las herramientas de cifrado de Pretty Good Privacy (PGP) y use una para comprobar la autenticidad de la firma PGP que se incluye en cada boletín de seguridad.

-   Puede descargar la clave del boletín de seguridad de Microsoft Security Response Center (MSRC) en: <http://www.microsoft.com/technet/security/bulletin/pgp.mspx>

-   Microsoft firma digitalmente todas las notificaciones por correo electrónico relacionadas con actualizaciones cuando las envía a los clientes. Para obtener más información acerca de cómo comprobar la firma digital consulte <http://www.microsoft.com/technet/security/bulletin/notify.mspx>

**Note:** hay varios correos electrónicos falsos que fingen ser notificaciones de Microsoft. Cuando reciba un boletín de seguridad de Microsoft, confírmelo, así como todos los hipervínculos a las actualizaciones de software mediante una visita al sitio web de la herramienta de búsqueda de boletines de seguridad en <http://www.microsoft.com/technet/security/current.aspx>. Para obtener más información acerca de estos tipos de mensajes engañosos, consulte el artículo acerca de cómo reconocer y evitar el correo electrónico fraudulento a los clientes de Microsoft en <http://www.microsoft.com/technet/security/bulletin/info/patch_hoax.mspx>

Si usa WSUS, puede suscribirse al servicio de alertas de actualizaciones que le informa de las nuevas actualizaciones a través de un mensaje de correo electrónico. Para identificar estas actualizaciones, debe aplicar una sincronización entre el servidor WSUS y el servidor público Windows Update cada vez que reciba una notificación de actualización por correo electrónico. Use la opción Sincronizar ahora de la página de administración del servidor WSUS para hacer esto. Para obtener más información acerca del uso de WSUS en la fase de identificación, consulte la [biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true).

Si usa SMS, cada vez que reciba una notificación por correo electrónico nueva debe determinar si SMS 2003 podrá detectar que la actualización aplica a los sistemas en su entorno de producción:

-   Si la actualización es para software que no admite o no detecta Microsoft Baseline Security Analyzer (MBSA), necesitará usar agentes cliente de inventario de hardware y de software de SMS 2003 para determinar qué equipos necesitan la actualización de software.

-   Si MBSA puede detectar la actualización, puede usar las herramientas de administración de actualizaciones de software de SMS 2003 para identificar los equipos que requieren la actualización.

-   Si la actualización es para una aplicación de Microsoft Office y se encuentra en la lista de actualizaciones proporcionada por Microsoft Office Inventory Tool for Updates, puede usar las herramientas de actualización de software para identificar el equipo que requiere la actualización.

Para obtener más información acerca del uso de SMS en la fase de identificación, consulte la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).

### Herramientas de examen de vulnerabilidades

Como se mencionó anteriormente en este módulo, los administradores pueden usar MBSA junto con WSUS para detectar actualizaciones de seguridad que faltan o que estén instaladas en equipos locales y remotos y para determinar si el equipo está expuesto a vulnerabilidades de seguridad habituales como la contraseña de administrador en blanco. Para obtener más información acerca del uso de WSUS en la fase de identificación, consulte la [biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true).

También puede usar los componentes de la característica Software Update Management en SMS 2003 para examinar y notificar actualizaciones de software que faltan y aplicadas en su entorno. Para obtener más información acerca de SMS, consulte la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).

[Principio de la página](#mainsection)

Determinar si las actualizaciones de software son relevantes
------------------------------------------------------------

Una gran cantidad de actualizaciones de software se lanzan regularmente en la comunidad de operaciones de tecnología de información (TI). Provienen de varias fuentes y se han creado por varios motivos, incluso para atender problemas que podrían provocar infracciones de seguridad. Todas las actualizaciones de software se deben revisar en detalle por su importancia para la infraestructura de TI de su organización. El proceso de filtrado descrito en esta sección debe eliminar la mayoría de actualizaciones de software irrelevantes, pero es probable que todavía existan más que pueda eliminar.

Por cada actualización de software que reciba se debe revisar su relevancia. Cuando una notificación incluye información acerca de varias actualizaciones de software, cada una se debe revisar individualmente en cuanto a su relevancia para la organización.

El primer paso para comprobar la relevancia es determinar si la actualización de software está diseñada para el sistema operativo o las aplicaciones en su entorno de producción.

Una vez que haya determinado que la actualización de software se aplica a algún elemento de su entorno de producción, la siguiente pregunta es si la aplicación o el sistema al que aplica la actualización tiene la vulnerabilidad para la cual está diseñada la actualización de software. Por ejemplo, una actualización de software puede estar diseñada para todos los sistemas operativos Windows Server™ que ejecuten Internet Information Server (IIS) con páginas Active Server (ASP) habilitadas.

Aunque su entorno puede incluir varios sistemas operativos Windows Server, la actualización de seguridad no es relevante si su organización no tiene ASP habilitado en ningún servidor IIS.

No todas las actualizaciones de seguridad que aplica a algún elemento de su entorno serán relevantes. Aunque es importante conocer y comprender bien las actualizaciones de seguridad existentes, sólo debe implementar las que sean relevantes para su entorno. Esto reducirá el esfuerzo que se requiere para mantener su entorno actualizado y seguro.

Aunque la información de una actualización de software se pueda clasificar como irrelevante, es importante indicar que existe al pasar la información al personal de administración de problemas. Si después es importante y se requiere, la organización obtendrá acceso a esta información en la fuente original.

Hay varios métodos de filtrado que puede usar para determinar la aplicabilidad de una actualización de software a su infraestructura de TI:

-   Lectura de los boletines de seguridad y los artículos de Microsoft Knowledge Base (KB).

-   Revisión de las actualizaciones de software individuales.

-   Uso de la Consola de administrador de SMS.

-   Uso de los informes integrados de SMS.

### Lectura de los boletines de seguridad y artículos de KB

La información de los boletines de seguridad en el sitio web de Microsoft se organiza en secciones para ayudarle a determinar lo críticas que son las vulnerabilidades para su entorno. Aunque de consultar toda la información de un boletín de seguridad, preste atención a las secciones de la tabla 1 cuando examine por primera vez un boletín de seguridad.

**Tabla 1: Boletines de seguridad: información clave**

 
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Apartado</th>
<th style="border:1px solid black;" >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Resumen</td>
<td style="border:1px solid black;">Consulte inmediatamente la sección Resumen de un boletín de seguridad. Los elementos Nivel de gravedad máxima, Consecuencia de la vulnerabilidad, Software afectado y Recomendación incluyen información que le ayudará a determinar lo susceptible que es su entorno a la vulnerabilidad.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Detalles de la vulnerabilidad</td>
<td style="border:1px solid black;">La sección Detalles de la vulnerabilidad proporciona una descripción técnica detallada de las vulnerabilidades. En esta sección también se describen los factores atenuantes y la gravedad de la vulnerabilidad de todos los productos afectados.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Soluciones provisionales</td>
<td style="border:1px solid black;">La sección Soluciones provisionales incluye información acerca de las soluciones que Microsoft ha probado para ayudar a mitigar las amenazas hasta que haya actualizado su entorno. Se debe leer esta sección como parte de la valoración de riesgos.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Preguntas más frecuentes</td>
<td style="border:1px solid black;">La sección Preguntas más frecuentes proporciona respuestas a las preguntas específicas de la vulnerabilidad o revisión. Es un buen lugar de partida después de leer la sección Resumen.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Información sobre la actualización de seguridad</td>
<td style="border:1px solid black;">En esta sección se enumeran elementos como los requisitos previos, la información de instalación específica para la plataforma, la información de implementación, la información de reinicio, la información de desinstalación, la información de archivo (incluidos los nombres de archivo, el tamaño, las versiones, la carpeta de destino) y los pasos de comprobación de la actualización.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Artículo de Knowledge Base</td>
<td style="border:1px solid black;">Consulte el artículo de KB identificado en el título de un boletín de seguridad. En el artículo de KB se proporciona información adicional acerca de las vulnerabilidades y cualquier actualización recomendada en el boletín de seguridad. El número entre paréntesis a la derecha del título del boletín de seguridad indica el artículo de KB correspondiente al boletín de seguridad. Use este número para buscar el artículo en el sitio web de soporte técnico de Microsoft en <a href="http://www.support.microsoft.com/" class="uri">http://www.support.microsoft.com/</a>.</td>
</tr>
</tbody>
</table>
  
Para obtener más información sobre el proceso de publicación del boletín de seguridad, consulte las notas del producto acerca de la modernización de la publicación del boletín de seguridad en <http://www.microsoft.com/technet/security/bulletin/revsbwp.mspx>.
  
La información recolectada en la notificación inicial y en la información adicional detectada al leer el boletín de seguridad y el artículo de KB asociado le ayudará a decidir si la actualización de software tiene relevancia para su organización.
  
Las descripciones breves de la sección Resumen de un boletín de seguridad deben permitirle realizar una valoración rápida de las posibles consecuencias que la vulnerabilidad puede tener en su entorno sin tener que revisar detalladamente el contenido completo de un boletín.
  
En Resumen se resalta el tipo de vulnerabilidad, se ofrece una lista del software afectado y se recomienda la acción adecuada. Después de revisar el Resumen, debe poder determinar si tiene que realizar una consulta detallada e inmediata de las secciones restantes del boletín de seguridad.
  
Mediante comprobaciones de relevancia de alto nivel, debe poder aislar los equipos de su entorno que probablemente estarán afectados por la vulnerabilidad.
  
Además de los elementos descritos en la tabla 1, Microsoft Security Response Center (MSRC) ha implementado el sistema de nivel de gravedad máxima para ayudarle a determinar rápidamente la importancia de una actualización para su organización. Estas clasificaciones se basan en las consecuencias posibles de la vulnerabilidad y tienen como propósito informarle de la urgencia de cualquier acción necesaria.
  
La determinación de la relevancia de las actualizaciones de software de tecnología específicas puede suponer desafíos importantes en cualquier entorno. Las tecnologías como Microsoft Data Engine (MSDE) o IIS, que se pueden instalar en clientes o servidores, pueden dificultar la determinación de si una actualización de software es relevante para cualquier subgrupo específico de equipos de su entorno. Esto destaca la importancia de mantener un inventario lo más exacto posible de su entorno.
  
### Revisar las actualizaciones de software individuales
  
Cada actualización de software de una notificación requiere una revisión detallada y a fondo. Esta revisión debe incluir toda la documentación asociada, incluso la enviada con la actualización de software y la información complementaria que pudiera encontrar, por ejemplo, en el sitio web de Microsoft TechNet.
  
Después de recibir un mensaje de correo electrónico que identifique las actualizaciones de software aplicables, debe elegir a un responsable para que las investigue. Este miembro del equipo debe tomar posesión de la actualización de software. El revisor debe leer el artículo de KB y comprender qué se corrige con la actualización de software.
  
La actualización de software puede ser específica de escenarios o configuraciones determinadas. El revisor debe comprobar si el escenario o configuración implementados en producción coinciden con lo tratado en el artículo de KB.
  
También existen preguntas que se deben plantear en términos de dependencias de actualización de software:
  
-   ¿Existen dependencias relacionadas con la actualización? Por ejemplo, ¿es necesario habilitar o deshabilitar ciertas características para que la actualización sea efectiva?
  
-   ¿Necesita la actualización de software que se instale determinado Service Pack? ¿Se reemplaza la actualización de software por un Service Pack u otra actualización de software y tiene sentido esperar una versión más reciente?
  
La identificación de las dependencias anteriores es importante debido a que tendrá una repercusión directa en su planeación de lanzamiento e implementación de la actualización de software. Documente en qué Service Pack (SP) aparecerá la actualización de software y si se requiere una versión diferente de actualización de software, según el Service Pack activo. (Es importante saberlo en caso de que se produzcan problemas de cumplimiento a medida que los usuarios se actualizan de un Service Pack a otro).
  
Puede usar los resultados del examen y los informes que generaron las características de SMS 2003 Software Update Management para ver la información específica y aplicable acerca de una actualización de software. Si usa WSUS, esta documentación se puede consultar desde la página de administración del servidor WSUS. Para obtener más información acerca de WSUS y SMS, consulte la [biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true) y la [biblioteca técnica de Systems Management Server 2003](http://www.microsoft.com/technet/sms/2003/library/default.mspx).
  
[Principio de la página](#mainsection)
  
Obtener y comprobar los archivos fuente de la actualización de software  
-----------------------------------------------------------------------
  
Una vez identificada una actualización de software y establecida su relevancia, debe obtener los archivos fuente de la actualización de software y confirmar que sean seguros y que se instalarán correctamente. El proceso de comprobación autenticará las actualizaciones de seguridad o resaltará las actualizaciones que no tienen validación de seguridad. En último caso, cuando se reciba una notificación no válida, se debe enviar información acerca de la notificación a los responsables del proceso de suscripción y al equipo de seguridad para que lleven a cabo una investigación adicional. Por ejemplo, si una notificación proviene de una fuente de información en la que se confía normalmente, pero la notificación específica tiene errores de validación, pueden surgir preocupaciones de seguridad acerca de la calidad de las notificaciones de esta fuente determinada. La fuente se debe investigar y se deben resolver los problemas.
  
Como mínimo, la comprobación de la actualización de software debe constar de los siguientes pasos:
  
-   Identificación y comprobación de la actualización de software.
  
-   Revisión de toda la documentación que se incluye:
  
    -   Revisión de los archivos de la actualización de software.
  
    -   Identificación del tamaño de la actualización de software.
  
    -   Identificación de las dependencias de la actualización de software:
  
    -   Identificación de cualquier acción necesaria antes y después de la actualización.
  
    -   Comprobación de que existen procedimientos de instalación de la actualización de software.
  
    -   Comprobación de que existen procedimientos de desinstalación de la actualización de software.
  
-   Garantía de que la actualización de software es segura.
  
### Identificación y comprobación de la actualización de software
  
Microsoft notifica a los administradores de nuevas actualizaciones de software mediante mensajes de correo electrónico, pero nunca incluye (o adjunta) archivos de software en dichos mensajes. A continuación se incluyen las prácticas clave de Microsoft con respecto a la notificación y comprobación de Microsoft como propietario de actualizaciones de software:
  
-   En ocasiones Microsoft enviará un mensaje de correo electrónico a los clientes para informarles de actualizaciones y actualizaciones de software disponibles. Sin embargo, el mensaje únicamente proporcionará vínculos a los sitios de descarga. El software nunca se adjuntará. Estos vínculos siempre le conducirán al sitio web de Microsoft o al sitio del protocolo de transferencia de archivos (FTP) de Microsoft, nunca a un sitio de terceros. Determinados mensajes de correo electrónico malintencionados podrían incluir vínculos de Internet en los cuales el vínculo no sea el mismo que el texto del mensaje de correo electrónico con formato HTML. Es importante asegurarse de que alguien sea responsable de comprobar la dirección URL (localizador uniforme de recursos) del sitio web visitado.
  
-   Además de los vínculos proporcionados en notificaciones por correo electrónico, Microsoft pone a disposición actualizaciones de software en Internet. Se puede obtener acceso a los archivos desde [http://www.microsoft.com](http://www.microsoft.com/), a través del sitio FTP en [ftp://ftp.microsoft.com](ftp://ftp.microsoft.com/) o a través del sitio web de Microsoft Update en [http://windowsupdate.microsoft.com](http://windowsupdate.microsoft.com/).
  
-   Los archivos de actualización de software también se pueden proporcionar en medios físicos como CD- ROM y discos.
  
-   Microsoft siempre usa la tecnología Authenticode para firmar digitalmente sus productos y permitir que los administradores se aseguren de que los archivos no se han alterado, como se muestra en la figura 3.
  
[![](images/Cc700831.secmod195figure3(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc700831.secmod195figure3(es-es,technet.10).gif)  
**Figure 3 Firma digital Authenticode**
  
Hay disponible más información acerca de las directivas de Microsoft acerca de la distribución de software en <http://www.microsoft.com/technet/security/bulletin/info/swdist.mspx>.
  
### Revisar toda la documentación adjunta
  
Antes de aplicar una actualización de software, debe leer y contrastar toda la documentación importante. El proceso de evaluación por expertos es importante ya que mitiga el riesgo de que una sola persona pase por alto determinados puntos importantes y relevantes al evaluar la actualización. Mientras lea la documentación, busque respuestas a las siguientes preguntas:
  
-   ¿Ocasionará la adopción de la actualización otros problemas que podrán en peligro el sistema de producción?
  
-   ¿Es necesario realizar alguna acción antes de implementar la actualización?
  
-   ¿Es preciso realizar cualquier acción después de implementar las actualizaciones?
  
-   ¿Existen soluciones provisionales o pasos de mitigación disponibles mientras actualiza su entorno?
  
-   ¿Se cuenta con procedimientos de instalación de la actualización de software?
  
-   ¿Se dispone de procedimientos de desinstalación de la actualización de software?
  
-   ¿Cuál es el tamaño del archivo de actualización de software? El tamaño del archivo influirá en su proceso de lanzamiento general y planeación; por ejemplo, en la forma de administrar los usuarios móviles.
  
Puede encontrar información en el boletín de seguridad, en las secciones descritas anteriormente en la tabla 1, que le ayudará a encontrar las respuestas a estas preguntas.
  
### Garantía de que la actualización de software es segura
  
Para evitar infección por virus o código malintencionado que afecte su infraestructura de TI, debe examinar los archivos relacionados con una actualización de software en un entorno aislado (en cuarentena). Esta cuarentena se debe exigir para todo el software y documentación. Deben existir controles estrictos en el lugar del entorno de cuarentena y, para garantizarlo, el proceso de cuarentena lo debe llevar a cabo un grupo de especialistas de la organización.
  
En muy pocas ocasiones, las actualizaciones de software sólo requerirán que realice cambios en el Registro o en los archivos de configuración, o que ajuste los parámetros de la aplicación, pero la mayoría de actualizaciones de software conllevarán la descarga de archivos. Siempre ponga en cuarentena los archivos que descargue mediante su exclusión de la red de producción mientras los examina en busca de virus y confirma su autenticidad digital.
  
Si usa WSUS, cada actualización está firmada; se calcula un hash y se envía con los metadatos (metadatos que describen para qué es útil una actualización). Cuando se descarga una actualización, WSUS comprueba la firma digital y el hash. Si la actualización se ha manipulado, no se instala. Para obtener información más detallada acerca del uso de WSUS en la fase de identificación, consulte la [biblioteca técnica de Windows Server Update Services (WSUS)](http://technet2.microsoft.com/windowsserver/en/library/d446d310-413f-4844-8aad-c557712397401033.mspx?mfr=true).
  
**Nota:** el Centro de descarga de Microsoft, Microsoft Update y SMS 2003 con las funciones de Administración de las actualizaciones de software proporcionan únicamente actualizaciones de software auténticas de Microsoft. Si recibe una actualización de software de Microsoft por otro medio, asegúrese de confirmar su validez y firma digital.
  
### Comprobar los procedimientos de instalación de las actualizaciones de software
  
A continuación se ofrecen algunas instrucciones para comprobar los procedimientos de instalación de actualizaciones de software:
  
-   Siga las instrucciones proporcionadas en los artículos de Knowledge Base y en el boletín de seguridad que acompaña a la actualización de software para comprobar que se instala correctamente.
  
-   Determine si la actualización de software necesita reiniciar el equipo. Si requiere reinicio, deberá tener en cuenta algunas consideraciones especiales durante las fases de planeación e implementación de servidores críticos, servidores de infraestructura básicos y servidores que ejecuten aplicaciones de línea de negocios (LOB). Para obtener más información acerca de estos problemas, lea el módulo "[Fase 3 de la administración de actualizaciones: Evaluación y planeación](https://technet.microsoft.com/es-es/library/d90522b7-21dd-4183-a81e-cfc05a0315dc(v=TechNet.10))".
  
-   Valore cuánto espacio en disco requiere la actualización de software (incluida una carpeta de desinstalación).
  
-   Compruebe si la actualización proporciona opciones de configuración que estén disponibles durante la instalación.
  
-   Lea cualquier documentación complementaria para obtener información adicional acerca de la instalación de una actualización de software.
  
A pesar de la comprobación, puede tener problemas después de instalar la actualización de software que sea preciso desinstalar. Por lo tanto, es importante probar que funcione el procedimiento de desinstalación. Después de desinstalar, debe comprobar que el servidor siga ejecutándose como se espera y continúe con la revisión del registro de eventos y los contadores del Monitor del sistema.
  
Algunas actualizaciones publicadas por Microsoft proporcionan una ruta de desinstalación y otras no. Tendrá que determinar las actualizaciones de software que se pueden desinstalar; para ello, consulte los detalles técnicos en el boletín de seguridad en la sección Información sobre la actualización de seguridad.
  
[Principio de la página](#mainsection)
  
Decidir la naturaleza de la actualización de software y enviar RFC  
------------------------------------------------------------------
  
Ahora que ha identificado la actualización de software, ha determinado la relevancia para su organización, ha obtenido los archivos fuente de actualización de software y ha confirmado que son seguros y se instalarán correctamente, el siguiente paso es enviar una solicitud de cambio (RFC) para comenzar la fase de evaluación y planeación de la actualización de software.
  
La solicitud de cambio que envíe debe incluir la siguiente información:
  
-   ¿Cuál es el cambio?
  
-   ¿A qué vulnerabilidad responde el cambio?
  
-   ¿A qué servicios afectará el cambio?
  
-   ¿Se implementa una actualización de software para ese servicio?
  
-   ¿Requiere la actualización de software reinicio para terminar la instalación?
  
-   ¿Se puede desinstalar la actualización de software?
  
-   ¿Qué contramedidas, si existe alguna, se pueden implementar para darle más tiempo para comprobar e implementar la actualización de software?
  
-   ¿Cuáles son las estrategias de prueba recomendadas para este cambio?
  
-   ¿Cuál es la prioridad recomendada de RFC?
  
-   ¿Cuál es la repercusión (categoría) del cambio?
  
Si una actualización de software trata un problema de seguridad importante o una inestabilidad del sistema, la prioridad de RFC se debe marcar como "emergencia". Una RFC de emergencia se debe crear únicamente cuando la implementación de una actualización de software o la implementación de contramedidas de seguridad, como cerrar puertos de red, se debe realizar con carácter de urgencia.
  
[Principio de la página](#mainsection)
  
Resumen  
-------
  
Estos son los puntos clave para recordar de la fase de identificación:
  
-   Debe asegurarse de que recibe notificación de todas las nuevas actualizaciones de software.
  
-   Debe confirmar que la notificación de actualización de software proceda de una fuente autorizada.
  
-   Debe comprobar que la actualización de software sea relevante para los sistemas en su entorno de producción.
  
-   Debe obtener los archivos fuente de la actualización de software y confirmar que no tengan virus.
  
-   Debe comprobar que la actualización de software se instale correctamente.
  
-   Debe decidir si la actualización es una emergencia y enviar una RFC para implementarla en producción.
  
[Principio de la página](#mainsection)
  
Paso a la fase de evaluación y planeación  
-----------------------------------------
  
Han finalizado los requisitos de la fase de identificación y se puede continuar con la fase de evaluación y planeación cuando:
  
-   Haya comprobado que tiene una actualización de software relevante cuya implementación es segura.
  
-   Haya enviado una solicitud de cambio (RFC) que desencadene la fase de evaluación y planeación.
  
Para obtener más información acerca de la fase de evaluación y planeación, lea el módulo, "[Fase 3 de la administración de revisiones: Evaluación y planeación](https://technet.microsoft.com/es-es/library/d90522b7-21dd-4183-a81e-cfc05a0315dc(v=TechNet.10))".
  
**Descargar la solución completa**
  
[Administración de revisiones con SMS 2003](http://www.microsoft.com/downloads/details.aspx?familyid=959ee7d6-7ddf-409a-9522-7d270bdcf12a&displaylang=en)
  
[Principio de la página](#mainsection)
