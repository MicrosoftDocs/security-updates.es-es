---
TOCTitle: Protección de la información confidencial de las amenazas de la ingeniería social
Title: Protección de la información confidencial de las amenazas de la ingeniería social
ms:assetid: '2c21c5d6-325c-4eb9-b3be-873915701f6d'
ms:contentKeyID: 20200267
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc875841(v=TechNet.10)'
---

Cómo proteger la información confidencial de las amenazas de la ingeniería social
=================================================================================

Publicado: 18/08/2006

##### En esta página

[](#efaa)[Introducción](#efaa)
[](#eeaa)[Amenazas y defensas de la ingeniería social](#eeaa)
[](#edaa)[Diseño de defensas frente a las amenazas de la ingeniería social](#edaa)
[](#ecaa)[Implementación de defensas frente a las amenazas de la ingeniería social](#ecaa)
[](#ebaa)[Apéndice 1: Listas de comprobación de la directiva de seguridad para amenazas de ingeniería social](#ebaa)
[](#eaaa)[Apéndice 2: Glosario](#eaaa)

### Introducción

Bienvenido a este documento de la colección Guías de seguridad para medianas empresas. Microsoft espera que esta información le ayude a crear un entorno informático más seguro y productivo.

#### Quién debería leer este artículo

Este artículo proporciona información sobre la administración de seguridad de las amenazas que suponen la ingeniería social y las defensas disponibles que permiten ayudar a enfrentarse a los piratas informáticos de la ingeniería social. La ingeniería social incluye principalmente amenazas no técnicas para la seguridad de la compañía. La amplia naturaleza de estas posibles amenazas hace necesario el contar con información sobre las amenazas y las posibles defensas a una amplia variedad de personal técnico y de dirección de una compañía, incluidos:

-   Miembros del consejo de administración

-   Administradores de servicios y de operaciones técnicas

-   Personal de soporte técnico

-   Personal de seguridad

-   Ejecutivos

#### Información general

Para atacar a su organización, los piratas informáticos de la ingeniería social se aprovechan de la credulidad, pereza, buenas maneras o incluso el entusiasmo de su personal. Por tanto, es difícil defenderse de un ataque de este tipo, ya que los destinatarios no se dan cuenta de que los están engañando o tal vez prefieran no admitirlo ante otras personas. Los objetivos de un pirata informático de ingeniería social, es decir, alguien que intenta conseguir acceso no autorizado a sus sistemas informáticos, son similares a los de cualquier otro pirata informático: desean obtener dinero, información o recursos de TI de su compañía.

Un pirata informático de ingeniería social intenta persuadir a su personal para que le proporcione información que le permitirá usar sus sistemas o los recursos de éstos. Normalmente, este método se conoce como *engaño por confianza*. Muchas pequeñas y medianas empresas consideran que los ataques de los piratas informáticos suponen un problema para las grandes corporaciones u organizaciones que ofrecen importantes recompensas. Si bien éste puede haber sido el caso en el pasado, el aumento de los delitos por Internet hace que los piratas informáticos ahora se dirijan a todos los sectores de la comunidad, desde las corporaciones hasta los individuos. Los delincuentes pueden robar directamente de una compañía, desviando fondos o recursos, pero también pueden usar a ésta como punto de partida para perpetrar delitos contra otros. Esto hace que las autoridades encuentren más dificultades para seguir la pista a estos delincuentes.

Para proteger a su personal de los ataques de ingeniería social, tiene que conocer los tipos de ataque que puede sufrir, saber lo que quiere el pirata informático y valorar lo que podría suponer la pérdida para su organización. Con estos datos, puede hacer más estricta su directiva de seguridad para que incluya defensas contra la ingeniería social. En este artículo se asume que cuenta con una directiva de seguridad con objetivos, prácticas y procedimientos que la compañía reconoce como elementos necesarios para proteger sus activos de información, sus recursos y su personal frente a ataques tecnológicos o físicos. Los cambios en la directiva de seguridad ayudarán al personal a contar con una guía acerca de cómo reaccionar cuando se encuentren con una persona o una aplicación que intenta coaccionarlos o persuadirlos para que proporcionen recursos de la empresa o desvelen información de seguridad.

[](#mainsection)[Principio de la página](#mainsection)

### Amenazas y defensas de la ingeniería social

Hay cinco tipos principales de vectores de ataque que un pirata informático de ingeniería social usa:

-   En línea

-   Telefónicos

-   Gestión de residuos

-   Contactos directos

-   Ingeniería social inversa

Además de reconocer estos puntos iniciales, también debe saber lo que el pirata informático espera obtener. Sus objetivos se basan en las mismas necesidades que nos guían a todos: el dinero, el avance social y la autoestima. Los piratas informáticos desean obtener dinero y recursos, desean que se les reconozca en la sociedad o en su grupo y desean sentirse bien con ellos mismos. Desgraciadamente, logran todo esto de forma ilegal robando o dañando los sistemas informáticos. Los ataques de cualquier tipo le costarán dinero, al perder ingresos, recursos, información, disponibilidad o credibilidad comercial. Cuando diseñe sus defensas contra esas amenazas, debe calcular lo que le costará un ataque.

#### Amenazas en línea

En nuestro mundo donde los negocios están cada vez más relacionados, el personal suele usar y responder a solicitudes e información que recibe de forma electrónica tanto desde dentro como desde fuera de la compañía. Esta conectividad permite a los piratas informáticos contactar con su personal desde el anonimato relativo de Internet. En ocasiones habrá oído hablar en la prensa de los ataques en línea, como ataques por correo electrónico, aplicaciones emergentes y mensajes instantáneos que usan caballos de Troya, gusanos y virus, a los que se conoce conjuntamente como *malware*, para dañar o trastocar los recursos informáticos. Puede empezar a poder hacer frente a muchos de estos ataques de malware mediante la implementación de fuertes defensas antivirus.

**Nota**   Para obtener más información acerca de las defensas antivirus, consulte la [*Guía de defensa en profundidad antivirus*](http://go.microsoft.com/fwlink/?linkid=28732) en http://go.microsoft.com/fwlink/?linkid=28732 (puede estar en inglés).

El pirata informático de ingeniería social persuade a un empleado para que le proporcione información mediante una artimaña creíble, en lugar de infectando un equipo con malware mediante un ataque directo. Un ataque puede proporcionar información que permitirá al pirata informático realizar un posterior ataque de malware, pero este resultado no es una función de la ingeniería social. Por tanto, debe aconsejar a su personal sobre cómo poder identificar mejor y evitar los ataques de ingeniería social en línea.

##### Amenazas por correo electrónico

Muchos empleados reciben decenas e incluso cientos de mensajes de correo electrónico cada día, tanto de sistemas de correo electrónico privados como de empresas. El volumen del correo electrónico manejado puede hacer que no se preste la atención necesaria a cada uno de los mensajes que se reciben. Este hecho es muy útil para un pirata informático de ingeniería social. La mayoría de los usuarios del correo electrónico se sienten bien consigo mismos cuando manejan la correspondencia; se trata del equivalente electrónico de mover el papel de una bandeja de entrada a una de salida. Si el pirata informático puede realizar una solicitud que no requiera acciones complicadas por parte de la víctima de su ataque, ésta aceptará hacer algo sin ni siquiera pensar en lo que está haciendo.

Un ejemplo de este tipo de ataque sencillo consiste en enviar un mensaje de correo electrónico a un empleado que indique que su jefe desea que se le envíen todas las fechas de vacaciones para una reunión y se copia a todo el mundo en el mensaje. Es muy fácil incluir un nombre externo en la lista de personas con copia y *suplantar* el nombre del remitente para que el mensaje parezca proceder de una fuente interna. La suplantación es especialmente sencilla si un pirata informático tiene acceso al sistema informático de una compañía, ya que no es necesario traspasar los firewalls del perímetro. Conocer las vacaciones de un departamento puede que no parezca una amenaza de seguridad, pero significa que un pirata informático sabe cuándo estará ausente un empleado. Será entonces cuando pueda hacerse pasar por esa persona con pocas posibilidades de ser descubierto.

El uso del correo electrónico como herramienta de ingeniería social se ha convertido en endémico en la última década. El término *suplantación de identidad (phishing)* describe el uso del correo electrónico para obtener información restringida o personal identificable de un usuario. Los piratas informáticos pueden enviar mensajes de correo electrónico que parezcan proceder de organizaciones válidas, como bancos o socios comerciales.

En la siguiente figura se muestra un vínculo aparentemente válido al sitio de administración de cuentas de Contoso.

![](images/Cc875841.HPISET01(es-es,TechNet.10).gif)

**Figura 1. Hipervínculo de suplantación de identidad (phishing) mediante correo electrónico**

Sin embargo, si observa más detenidamente podrá notar dos diferencias:

-   El texto del mensaje indica que el sitio es seguro, lo que viene denotado por https, si bien la sugerencia de la pantalla muestra que el sitio usa realmente http.

-   El nombre de la compañía del mensaje es “Contoso,” pero el vínculo lleva a una compañía denominada “Comtoso”.

Como indica el término suplantación de identidad (phishing), estos métodos suelen ser especulativos y en ellos se realiza una solicitud genérica de información a un cliente. El camuflaje realista que se usa en los mensajes de correo electrónico, con logotipos de compañía, fuentes e incluso números de soporte telefónico gratuito aparentemente válidos, hace que el mensaje parezca más creíble. En cada mensaje de suplantación de identidad (phishing) hay una solicitud de información del usuario, que suele proporcionar, a cambio, un servicio adicional o una actualización. Una extensión de la suplantación de identidad (phishing) es el *spear-phishing*, en el que se contacta con una persona o grupo departamental explícitos. Este método es mucho más sofisticado, porque se necesita información personal y relevante de la compañía para conseguir que el engaño sea creíble. Para él se necesitan más conocimientos sobre la persona objeto del ataque, pero con él se puede obtener información más detallada y específica.

El mensaje de correo electrónico también puede llevar hipervínculos que pueden tentar a un empleado a incumplir la seguridad de la compañía. Como se muestra en la Figura 1, los vínculos no siempre llevan al usuario a la ubicación esperada o prometida. El pirata informático cuenta con una serie de opciones adicionales en el mensaje de correo electrónico de suplantación de identidad (phishing), incluidas imágenes que son hipervínculos que descargan malware, como virus o software espía, o texto que se presenta en una imagen con el fin de eludir los filtros de seguridad de los hipervínculos.  

La mayoría de las medidas de seguridad ayudan a mantener alejados a los usuarios no autorizados. Un pirata informático puede eludir muchas defensas si puede engañar a un usuario para que introduzca un caballo de Troya, un gusano o un virus en la compañía mediante un vínculo. El hipervínculo también puede llevar a un usuario a un sitio en el que se usen aplicaciones emergentes para solicitar información u ofrecer ayuda.

Puede usar una matriz de vectores de ataque, objetivos de los ataques, descripciones y el costo que suponen para su compañía similar a la que aparece en la siguiente tabla para poder clasificar los ataques y establecer el riesgo de cada uno de ellos para su compañía. En ocasiones, una amenaza representa algo más que un riesgo. Cuando éste sea el caso, en los siguientes ejemplos se muestran los principales riesgos en negrita.

**Tabla 1. Ataques en línea por correo electrónico y costos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objetivos de los ataques</p></th>
<th><p>Descripción</p></th>
<th><p>Costo</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Robo de información de la compañía</p></td>
<td style="border:1px solid black;"><p>El pirata informático se hace pasar por (suplanta a) un usuario interno para obtener información de la compañía.</p></td>
<td style="border:1px solid black;"><p><strong>Información confidencial</strong></p>
<p>Credibilidad comercial</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Robo de información financiera</p></td>
<td style="border:1px solid black;"><p>El pirata informático usa la técnica de suplantación de identidad (phishing) (o &quot;spear-phishing&quot;) para solicitar información confidencial de la compañía, como detalles de cuentas.</p></td>
<td style="border:1px solid black;"><p><strong>Dinero</strong></p>
<p><strong>Información confidencial</strong></p>
<p>Credibilidad comercial</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Descarga de malware</p></td>
<td style="border:1px solid black;"><p>El pirata informático engaña a un usuario para que haga clic en un hipervínculo o abra un archivo adjunto y, de esta forma, infecte la red de la compañía.</p></td>
<td style="border:1px solid black;"><p><strong>Disponibilidad comercial</strong></p>
<p>Credibilidad comercial</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Descarga de software del pirata informático</p></td>
<td style="border:1px solid black;"><p>El pirata informático engaña a un usuario para que haga clic en un hipervínculo o abra un archivo adjunto y, de esta forma, descargue un programa suyo que use recursos de la red de la compañía.</p></td>
<td style="border:1px solid black;"><p><strong>Recursos</strong></p>
<p><strong>Credibilidad comercial</strong></p>
<p>Dinero</p></td>
</tr>
</tbody>
</table>
<p> </p>

Al igual que en la mayoría de los engaños de confianza, puede conseguir resistirse a los ataques de piratas de ingeniería social de forma más efectiva mediante una actitud de prudencia ante cualquier mensaje inesperado que reciba en la bandeja de entrada. Para que se implante este método en una organización, debe incluir en la directiva de seguridad unas directrices específicas sobre uso del correo electrónico que incluyan:

-   Archivos adjuntos en documentos.

-   Hipervínculos en documentos.

-   Solicitudes de información personal o de la compañía desde dentro de ésta.

-   Solicitudes de información personal o de la compañía desde fuera de ésta.

Además de estas directrices, debe incluir ejemplos de ataques de suplantación de identidad (phishing). Cuando un usuario reconozca una estafa mediante suplantación de identidad (phishing), notará que es mucho más fácil detectar otras.

**Aplicaciones y cuadros de diálogo emergentes**
No es realista pensar que los empleados no usan el acceso a Internet de la compañía para actividades no relacionadas con su trabajo. La mayoría de los empleados en algún momento navegan por Internet para asuntos personales, como para realizar búsquedas o compras en línea. Esta navegación para fines personales puede hacer que los empleados y, por tanto, los sistemas informáticos de la compañía, entren en contacto con ingenieros sociales genéricos. Si bien puede que no vayan destinados de forma específica a su compañía, usarán a su personal en su esfuerzo por obtener acceso a los recursos de su empresa. Uno de los objetivos más habituales consiste en incrustar un motor de correo en el entorno del equipo, mediante el cual, el pirata informático puede iniciar ataques de suplantación de identidad (phishing) o de otro tipo mediante correo electrónico en otras compañías o personas.

En la siguiente figura se muestra cómo un hipervínculo parece llevar a un sitio de administración de cuentas seguro (secure.contosa.com account\_id?Amendments), mientras que la barra de estado muestra que va a llevar al usuario al sitio de un pirata informático. Dependiendo del explorador que use, un pirata informático puede suprimir o cambiar el formato de la información de la barra de estado.

[![](images/Cc875841.HPISET02(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875841.hpiset02_big(es-es,technet.10).gif)

**Figura 2. Hipervínculo de suplantación de identidad (phishing) a una página web**

Los dos métodos más habituales de engañar a un usuario para que haga clic en un botón de un cuadro de diálogo son el advertir de un problema, por ejemplo, mostrando un mensaje de error de la aplicación o del sistema operativo realista, u ofreciendo servicios adicionales, por ejemplo, una descarga gratuita que haga que el equipo del usuario vaya más rápido. Para los usuarios de TI y web experimentados, estos métodos pueden parecer engaños clarísimos. Sin embargo, para los usuarios no experimentados, estas aplicaciones o cuadros de diálogo emergentes pueden ser intimidatorios o atractivos.

**Tabla 2. Ataques en línea mediante aplicaciones y cuadros de diálogo emergentes y costos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objetivos de los ataques</p></th>
<th><p>Descripción</p></th>
<th><p>Costo</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Robo de información personal</p></td>
<td style="border:1px solid black;"><p>El pirata informático solicita información personal de un empleado</p></td>
<td style="border:1px solid black;"><p>Información confidencial</p>
<p>Dinero (empleado)</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Descarga de malware</p></td>
<td style="border:1px solid black;"><p>El pirata informático engaña a un usuario para que haga clic en un hipervínculo o abra un archivo adjunto</p></td>
<td style="border:1px solid black;"><p>Disponibilidad comercial</p>
<p>Credibilidad comercial</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Descarga de software del pirata informático</p></td>
<td style="border:1px solid black;"><p>El pirata informático engaña a un usuario para que haga clic en un hipervínculo o abra un archivo adjunto</p></td>
<td style="border:1px solid black;"><p>Recursos</p>
<p>Credibilidad comercial</p>
<p>Dinero</p></td>
</tr>
</tbody>
</table>
<p> </p>

Proteger a los usuarios de aplicaciones emergentes de ingeniería social es principalmente una función de concienciación. Para evitar el problema, puede configurar el explorador de forma predeterminada para que bloquee los elementos emergentes y las descargas automatizadas, pero algunos elementos emergentes pueden eludir esta configuración. Resulta más efectivo asegurarse de que los usuarios son conscientes de que no deben hacer clic en elementos emergentes a menos que lo consulten con el personal de soporte técnico. Por tanto, su personal debe poder confiar en que el personal de soporte técnico no va a juzgarle por haber navegado por la Web. Esta relación de confianza puede verse afectada por la directiva de la compañía sobre la navegación por Internet para fines personales.

**Mensajería instantánea**
La mensajería instantánea (IM) es un medio de comunicación relativamente nuevo, pero que cada vez es más popular como herramienta en el trabajo. Algunos analistas calculan que habrá 200 millones de usuarios de productos de mensajería instantánea en 2006. La inmediatez y la familiaridad de la mensajería instantánea la convierte en un lugar adecuado para los ataques de ingeniería social, ya que los usuarios lo consideran como el teléfono y no lo relacionan con posibles amenazas para el software del equipo. Los dos ataques principales que se realizan con mensajería instantánea son el envío de un vínculo de malware en un mensaje de mensajería instantánea y el envío de un archivo real. Por supuesto, la mensajería instantánea también representa otra forma de solicitar información de manera sencilla.

Existen una serie de posibles amenazas inherentes a la mensajería instantánea cuando se trata el tema de la ingeniería social. La primera es el carácter informal de la mensajería instantánea. La naturaleza de chat de la mensajería instantánea, junto con la opción de asignarse un nombre falso o inventado, hace que no esté totalmente claro que se esté hablando con la persona con la que se cree estar hablando, lo que aumenta de forma significativa la posibilidad de suplantaciones casuales.

En la siguiente figura se muestra el funcionamiento de la suplantación, tanto para correo electrónico como para la mensajería instantánea.

![](images/Cc875841.HPISET03(es-es,TechNet.10).gif)

**Figura 3. Suplantación mediante mensajería instantánea y correo electrónico**

El pirata informático (de color rojo) se hace pasar por otro usuario conocido y envía un mensaje de correo electrónico o de la mensajería instantánea que el destinatario asumirá que procede de alguien conocido. La familiaridad hace que se relajen las defensas del usuario, por lo que es mucho más probable que éste haga clic en un vínculo o abra un archivo adjunto de alguien que conozca o que crea conocer. La mayoría de los proveedores de mensajería instantánea permiten la identificación de los usuarios según la dirección de correo electrónico, lo que permite a un pirata informático que ha identificado un estándar de direcciones en una compañía enviar invitaciones de contactos de mensajería instantánea a otras personas de la organización. Esta funcionalidad no supone una amenaza, pero significa que aumenta significativamente el número de personas que pueden ser objeto de un ataque en la compañía.

**Tabla 3. Ataques por mensajería instantánea y costos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objetivos de los ataques</p></th>
<th><p>Descripción</p></th>
<th><p>Costo</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Solicitud de información confidencial de la compañía</p></td>
<td style="border:1px solid black;"><p>Los piratas informáticos usan la suplantación por mensajería instantánea para hacerse pasar por un compañero de trabajo y solicitar información de la compañía.</p></td>
<td style="border:1px solid black;"><p><strong>Información confidencial</strong></p>
<p>Credibilidad comercial</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Descarga de malware</p></td>
<td style="border:1px solid black;"><p>El pirata informático engaña a un usuario para que haga clic en un hipervínculo o abra un archivo adjunto y, de esta forma, infecte la red de la compañía.</p></td>
<td style="border:1px solid black;"><p><strong>Disponibilidad comercial</strong></p>
<p>Credibilidad comercial</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Descarga de software del pirata informático</p></td>
<td style="border:1px solid black;"><p>El pirata informático engaña a un usuario para que haga clic en un hipervínculo o abra un archivo adjunto y, de esta forma, descargue un programa suyo, como un motor de correo, que use recursos de la red de la compañía.</p></td>
<td style="border:1px solid black;"><p><strong>Recursos</strong></p>
<p><strong>Credibilidad comercial</strong></p>
<p>Dinero</p></td>
</tr>
</tbody>
</table>
<p> </p>

Si desea aprovechar la inmediatez y las reducciones de costos que puede proporcionar la mensajería instantánea, debe incluir en sus directivas de seguridad defensas específicas para la mensajería instantánea. Para ayudarle a controlar la mensajería instantánea en su empresa, debe establecer las cinco reglas de uso siguientes:

-   **Estandarizar su uso en una sola plataforma de mensajería instantánea**. Con esta norma se minimizará el esfuerzo de compatibilidad y se desanimará a los usuarios para que no charlen con su propio proveedor de mensajería instantánea personal. Si desea un método más controlado para limitar las opciones de los usuarios, puede decidir bloquear los puertos que usan los servicios de mensajería instantánea comunes.

-   **Definir una configuración de seguridad de implementación**. Los clientes de mensajería instantánea ofrecen una serie de opciones de privacidad y seguridad, como la detección de virus.

-   **Establecer directrices de contacto**. Recomiende que los usuarios no acepten de forma predeterminada nuevas invitaciones de contacto.

-   **Establecer estándares de contraseñas**. Haga que las contraseñas de mensajería instantánea cumplan con los estrictos estándares de contraseñas establecidos para las contraseñas de host.

-   **Ofrecer ayuda para el uso**. Cree un conjunto de directrices de prácticas recomendadas para sus usuarios, en las que explique los motivos inherentes a ellas.

**Amenazas telefónicas**
El teléfono ofrece un vector de ataque excelente para los piratas informáticos de ingeniería social. Se trata de un medio familiar, pero también impersonal, ya que la persona objeto del ataque no puede ver al pirata informático. Las opciones de comunicación de la mayoría de los sistemas informáticos también pueden convertir a la central de conmutación (PBX) en un objetivo atractivo. Otro ataque, tal vez muy rudimentario, es el robo de PIN de tarjetas telefónicas o de crédito en cabinas telefónicas. Este ataque suele realizarse como robo a una persona, pero las tarjetas de crédito de las compañías son igualmente útiles. La mayoría de las personas saben que tienen que ser prudentes ante los fisgones en los cajeros automáticos, pero la mayoría suele tener menos precaución cuando usan un PIN en una cabina telefónica.

El sistema de voz sobre IP (VoIP) es un mercado en desarrollo que ofrece reducciones de costos a las compañías. Actualmente, debido al relativamente reducido número de instalaciones, las actividades de piratas informáticos sobre VoIP no se considera una amenaza importante. Sin embargo, conforme cada vez más empresas usan esta tecnología, la suplantación mediante VoIP puede generalizarse tanto como lo está ahora en el correo electrónico y en mensajería instantánea.

**Central de conmutación (PBX)**
El pirata informático que ataca una central PBX tiene tres objetivos principales:

-   Solicitar información, normalmente imitando a un usuario legítimo, ya sea para tener acceso al propio sistema telefónico o para obtener acceso remoto a sistemas informáticos.

-   Obtener acceso al uso “gratuito” del teléfono.

-   Obtener acceso a la red de comunicaciones.

Cada uno de estos objetivos supone un tema distinto, en el que el pirata informático llama a la compañía para intentar obtener los números de teléfono que proporcionan acceso directo a una central PBX o mediante una central PBX a la red telefónica pública. El término que se usa para este hecho es *phreaking*. El método más habitual consiste en que el pirata informático finja ser un técnico telefónico, que solicita línea exterior o una contraseña para analizar y resolver los problemas indicados en el sistema telefónico interno, como se muestra en la siguiente figura.

![](images/Cc875841.HPISET04(es-es,TechNet.10).gif)

**Figura 4. Ataques telefónicos a centrales PBX**

Las solicitudes de información o acceso telefónico constituyen una forma de ataque relativamente sin riesgos. Si el destinatario sospecha o no decide responder a una solicitud, el pirata informático sólo tiene que colgar. Sin embargo, tenga en cuenta que dichos ataques son más sofisticados que el hecho de que un pirata informático simplemente llame a una compañía y solicite el Id. y la contraseña de un usuario. Éste normalmente presenta una situación, en la que pide u ofrece ayuda, antes de realmente solicitar la información personal o de la empresa, casi como si se tratara de algo que se le hubiera ocurrido a última hora.

**Tabla 4. Ataques a centrales de conmutación y costos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objetivos de los ataques</p></th>
<th><p>Descripción</p></th>
<th><p>Costo</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Solicitud de información de la compañía</p></td>
<td style="border:1px solid black;"><p>El pirata informático se hace pasar por un usuario legítimo para obtener información confidencial.</p></td>
<td style="border:1px solid black;"><p>Información confidencial</p>
<p>Credibilidad comercial</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Solicitud de información telefónica</p></td>
<td style="border:1px solid black;"><p>El pirata informático se hace pasar por un técnico telefónico para obtener acceso a la central PBX con el fin de realizar llamadas externas.</p></td>
<td style="border:1px solid black;"><p>Recursos</p>
<p>Dinero</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Uso de la central PBX para tener acceso a sistemas informáticos</p></td>
<td style="border:1px solid black;"><p>El pirata informático entra en los sistemas informáticos, mediante una central PBX, para robar o manipular información, infectar con malware o usar recursos.</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
</tbody>  
</table>
  
La mayoría de los usuarios no tienen ningún tipo de conocimientos sobre el sistema telefónico interno, aparte del propio teléfono. Éste es el factor más importante de defensa que puede incluir en su directiva de seguridad. No es habitual que los piratas informáticos contacten con los usuarios generales con este sistema. Los destinatarios más habituales suelen ser el personal de recepción o de centralitas. Debe indicarles que el servicio de ayuda es el único que está autorizado a ofrecer ayuda a los proveedores telefónicos. De esta forma, todo el personal autorizado trata con todas las llamadas de soporte de ingeniería. Este método permite que el personal destinatario pueda redirigir eficaz y rápidamente tales consultas al empleado cualificado.
  
**Servicio de ayuda**  
El departamento de soporte es una de las defensas fundamentales frente a los piratas informáticos, pero supone, a la vez, un objetivo para estos piratas de la ingeniería social. Si bien el personal de soporte técnico suele ser precavido frente a la amenaza de estos piratas, también se somete a aprendizaje para ayudar y atender a las personas que llaman y a ofrecerles consejos y soluciones para sus problemas. En ocasiones, el entusiasmo demostrado por el personal de soporte técnico a la hora de proporcionar una solución hace olvidar su compromiso con el cumplimiento de los procedimientos de seguridad y hace que este personal se enfrente a un dilema: si aplican los estrictos estándares de seguridad, pidiendo pruebas que demuestren que la solicitud o pregunta proviene de un usuario autorizado, puede parecer que no son serviciales o incluso que ponen obstáculos. El personal de producción o ventas y marketing que considere que el departamento de TI no esté proporcionando el servicio inmediato que necesitan pueden quejarse; también es cierto que cuando se pide a los miembros de la directiva que demuestren su identidad, éstos no se suelen mostrar muy comprensivos ante la rigurosidad del personal de soporte.
  
**Tabla 5. Ataques telefónicos al servicio de ayuda y costos**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="33%" />  
<col width="33%" />  
<col width="33%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Objetivos de los ataques</p></th>  
<th><p>Descripción</p></th>  
<th><p>Costo</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Solicitud de información</p></td>
<td style="border:1px solid black;"><p>El pirata informático se hace pasar por un usuario legítimo para obtener información de la empresa.</p></td>
<td style="border:1px solid black;"><p><strong>Información confidencial</strong></p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Solicitud de acceso</p></td>
<td style="border:1px solid black;"><p>El pirata informático se hace pasar por un usuario legítimo para obtener acceso de seguridad a los sistemas comerciales.</p></td>
<td style="border:1px solid black;"><p><strong>Información confidencial</strong></p>
<p><strong>Credibilidad comercial</strong></p>  
<p><strong>Disponibilidad comercial</strong></p>  
<p><strong>Recursos</strong></p>
<p>Dinero</p></td>
</tr>
</tbody>
</table>
<p> </p>

El servicio de ayuda debe conseguir un equilibrio entre la seguridad y la eficacia comercial y, en este contexto, las directivas y procedimientos de seguridad deben servirles de apoyo. Una prueba de identidad, como proporcionar el número de empleado, departamento, y nombre del jefe, no debe suponer un gran problema para que el analista del servicio de ayuda lo solicite, ya que todo el mundo sabe estos datos. Sin embargo, esta prueba tal vez no sea completamente segura, ya que un pirata informático puede haber robado esta información. No obstante, puede ser una forma realista de empezar. En verdad, el único método de identificación seguro al 99,99% es una prueba de DNA, lo cual es claramente poco realista.

Es más difícil defender al analista del servicio de ayuda frente a un pirata informático que sea un trabajador interno o un contratista. Dicho pirata tendrá un conocimiento detallado de los procedimientos internos y tendrá tiempo para asegurarse de que cuenta con toda la información necesaria antes de llamar al servicio de ayuda. Los procedimientos de seguridad deben proporcionar una función doble ante esta situación:

-   El analista del servicio de ayuda debe asegurarse de que se realiza una pista de auditoría de todas las acciones. Si un pirata informático consigue obtener acceso no autorizado a información o recursos mediante una llamada al servicio de ayuda, dicho servicio debe registrar todas las actividades para que se pueda reparar o limitar de forma rápida cualquier daño o pérdida. Si cada llamada desencadena un mensaje de correo electrónico automatizado o manual que indique el problema o solicitud, también será más fácil para un empleado que sufriera un robo de identidad darse cuenta de lo sucedido y llamar al servicio de ayuda.

-   El analista del servicio de ayuda debe contar con un procedimiento bien estructurado sobre cómo tratar los distintos tipos de llamadas. Por ejemplo, si el jefe del empleado debe enviar por correo electrónico solicitudes de cambio de acceso, no debe producirse ningún cambio informal o no autorizado en los niveles de seguridad.

Si los usuarios son conscientes de estas reglas y la directiva apoya su implementación, los piratas informáticos lo tendrán mucho más difícil a la hora de conseguir sus objetivos o pasar inadvertidos. La pista de auditoría de 360 grados es la herramienta más valiosa para evitar y detectar actos ilícitos.

**Amenazas en la gestión de residuos**
El análisis ilícito de los residuos, o *búsqueda en contenedores*, como se conoce habitualmente, es una actividad muy valiosa para los piratas informáticos. Los restos de documentos comerciales pueden contener información de utilidad inmediata para un pirata informático, por ejemplo, números de cuenta e Id. de usuario desechados, o bien puede servir como información de base, por ejemplo, para listados telefónicos y gráficos de organizaciones. Este último tipo de información es importantísimo para un pirata informático de ingeniería social, ya que permite que parezca creíble cuando realiza un ataque. Por ejemplo, si el pirata informático parece tener un buen conocimiento del personal del departamento de una compañía, es mucho más probable que tenga éxito cuando contacte con el mismo; la mayoría del personal asumirá que alguien que sabe mucho de su compañía tiene que ser un empleado de ésta.

Los medios electrónicos pueden ser incluso más útiles. Si las compañías no cuentan con reglas de gestión de residuos que incluyan el desecho de medios redundantes, se podrá encontrar todo tipo de información en unidades de disco duro, CDs y DVDs desechados. La naturaleza sólida de los medios fijos y extraíbles implica que los responsables de la seguridad de TI deban estipular directivas de gestión de medios que incluyan instrucciones de borrado o destrucción.

**Tabla 6: Ataques de gestión de residuos y costos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objetivos de los ataques</p></th>
<th><p>Descripción</p></th>
<th><p>Costo</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Restos de papel en contenedores externos</p></td>
<td style="border:1px solid black;"><p>El pirata informático toma el papel de contenedores externos para robar cualquier tipo de información relevante de la compañía.</p></td>
<td style="border:1px solid black;"><p><strong>Información confidencial</strong></p>
<p>Credibilidad comercial</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Restos de papel en papeleras internas</p></td>
<td style="border:1px solid black;"><p>El pirata informático toma el papel de las papeleras internas de la oficina, eludiendo cualquier directriz de gestión externa de residuos de papel.</p></td>
<td style="border:1px solid black;"><p><strong>Información confidencial</strong></p>
<p>Credibilidad comercial</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Residuos de medios  electrónicos</p></td>
<td style="border:1px solid black;"><p>El pirata informático roba información y aplicaciones de medios electrónicos desechados. El pirata informático también roba el propio medio.</p></td>
<td style="border:1px solid black;"><p><strong>Información confidencial</strong></p>
<p>Recursos</p>
<p>Credibilidad comercial</p></td>
</tr>
</tbody>
</table>
<p> </p>

Su personal debe comprender las implicaciones que tiene el arrojar residuos de papel o medios electrónicos a una papelera o contenedor. Una vez que los residuos salen del edificio, su propiedad puede entrar en un vacío legal. La búsqueda en contenedores tal vez no se considere ilegal en todas las circunstancias, por lo que debe asegurarse de que aconseja a su personal sobre cómo tratar los residuos. Triture los documentos y borre o destruya los medios magnéticos que vaya a desechar. Si algún residuo es lo demasiado grande o rígido como para poderlo destruir en una trituradora, como una agenda telefónica, o técnicamente el usuario no lo puede destruir, se deberá crear un protocolo específico para su desecho. También debe colocar los contenedores en una zona segura a la que no pueda acceder todo el mundo.

Cuando diseñe una directiva de gestión de residuos, es importante que se asegure de que cumple con la normativa local sobre seguridad. También puede ser una buena medida desde el punto de vista social adoptar estrategias de gestión de recursos que respeten el medioambiente.

Además de la gestión de residuos externos (el papel o los medios electrónicos que se puedan enviar a personas externas a la compañía) también debe gestionar los residuos internos. Las directivas de seguridad no suelen tener en cuenta este asunto, porque se suele asumir que cualquier persona que tenga acceso a la compañía debe ser de confianza. Está claro que éste no es siempre el caso. Una de las medidas más efectivas a la hora de gestionar los residuos de papel es la especificación de una clasificación de datos. Puede definir distintas categorías de información en papel y especificar cómo debe desechar el personal los residuos en cada caso. Entre las categorías de ejemplo se podrían incluir:

-   **Información confidencial de la compañía**. Triture todos los documentos confidenciales de la compañía antes de desecharlos en cualquier papelera o contenedor.

-   **Información privada**. Triture todos los documentos privados antes de desecharlos en cualquier papelera o contenedor.

-   **Información del departamento**. Triture todos los documentos del departamento antes de desecharlos en contenedores públicos.

-   **Información pública**. Deseche todos los documentos públicos en cualquier papelera o recíclelos.

Para obtener más información acerca del desarrollo de clasificaciones de datos, consulte el tema [Función SMF de administración de la seguridad](http://go.microsoft.com/fwlink/?linkid=37696) en Microsoft® TechNet en la dirección http://go.microsoft.com/fwlink/?linkid=37696 (puede estar en inglés).

**Contactos directos**
La forma más sencilla y barata en la que un pirata informático puede obtener información es solicitarla directamente. Este método puede parecer rudimentario y obvio, pero se ha convertido en la base de los engaños por confianza desde el comienzo. Hay cuatro métodos principales que demuestran ser útiles para los ingenieros sociales:

-   **Intimidación**. Este método puede implicar la suplantación de una figura de autoridad para coaccionar a una persona a responder a una solicitud.

-   **Persuasión**. Las formas más habituales de persuasión suelen incluir la adulación o el mencionar a alguien importante.

-   **Congraciamiento**. Este método suele ser una estratagema más a largo plazo, en la que un compañero de trabajo de la misma categoría de una inferior inicia una relación para conseguir la confianza y, finalmente, información de esta persona.

-   **Ayuda**. En este método, el pirata informático se ofrece a ayudar al objetivo del ataque. La ayuda normalmente hará que finalmente el objetivo del ataque divulgue información personal que permitirá al pirata informático robar su identidad.

La mayoría de las personas asumen que cualquiera que les hable es una persona de confianza, lo que es interesante ya que es un hecho que la mayoría de las personas admite que se mienten a sí mismas. *The Lying Ape: An Honest Guide to a World of Deception* (El mono mentiroso: una guía honesta en un mundo de engaños), Brian King, Icon Books Limited. La confianza total es uno de los objetivos de un pirata informático de ingeniería social.

Es muy difícil defender a los usuarios frente a estos tipos de contactos directos. Algunos usuarios tienen una predisposición natural a que la ingeniería social use uno de estos cuatro ataques. La defensa frente a un ataque por intimidación es el resultado de una cultura “sin miedo” dentro de una empresa. Si el comportamiento habitual es la educación, se reduce el éxito que tendrá la intimidación, ya que es más probable que los empleados consulten las situaciones polémicas. Una actitud de apoyo en la directiva y funciones de supervisión que busquen la consulta de problemas y la toma de decisiones es lo peor con lo que se puede encontrar un pirata informático de ingeniería social. Su objetivo consiste en alentar a los destinatarios del ataque a tomar una decisión rápida. Si el problema se consulta a una autoridad superior, es mucho menos probable que consigan su objetivo.

La persuasión siempre ha sido un método muy usado por los humanos para lograr objetivos personales. No puede conseguir esto sin más de sus empleados, pero puede proporcionar una guía firme sobre lo que un individuo debe y no debe hacer. El pirata informático siempre preguntará o creará una situación en la que un usuario ofrece voluntariamente información restringida. Su mejor defensa son las campañas de concienciación continuadas y la ayuda básica sobre dispositivos de seguridad como las contraseñas.

Los piratas informáticos necesitan tiempo para congraciarse con los usuarios. Tendrán que contactar habitualmente, probablemente asumiendo el papel de un compañero de trabajo. Para la mayoría de las medianas empresas, la principal amenaza de un compañero de trabajo procede del personal de contratas o de servicio habitual. El grupo de recursos humanos debe tener la misma precaución al investigar los antecedentes del personal de contratas que al hacerlo con el personal fijo. Puede encargar la mayor parte de este trabajo al contratista. Para asegurarse de que esta empresa realiza un trabajo efectivo, puede pedirle que cumpla con sus propias directivas de investigación de antecedentes que se aplica al personal fijo. Si un pirata informático de ingeniería social consigue un puesto fijo en la compañía, la mejor defensa sería la concienciación del personal y su cumplimiento de las reglas de la directiva de seguridad sobre la seguridad de la información.

Finalmente, los ataques de ayuda se pueden reducir si cuenta con un servicio de ayuda efectivo. El recurrir a la ayuda de alguien interno suele ser el resultado de una animadversión hacia los servicios de soporte existentes de la compañía. Debe aplicar dos elementos para asegurarse de que el personal contacta con el servicio de ayuda en lugar de con un experto interno no autorizado o, lo que es peor aún, un experto externo a la compañía:

-   Especifique en la directiva de seguridad que el servicio de ayuda es el único lugar al que deben informar los usuarios sobre sus problemas.

-   Asegúrese de que el personal de servicio cuente con un proceso de respuesta acordado dentro de acuerdo de nivel de servicio del departamento. Realice una auditoría frecuente del rendimiento del servicio de ayuda para asegurarse de que los usuarios reciban el nivel adecuado de respuesta y solución.

No debe subestimar la importancia del servicio de ayuda a la hora de proporcionar una defensa de primer nivel frente a los ataques de la ingeniería social.

**Contactos virtuales**
Los piratas de ingeniería social deben contactar con los objetivos de sus ataques para poder realizarlos. La mayoría de las veces, este contacto se llevará a cabo mediante algún medio electrónico, como un mensaje de correo electrónico o una ventana emergente. El volumen de correo no deseado que llega a la mayor parte de los buzones de correo personales hace que este método de ataque sea menos exitoso, ya que los usuarios son cada vez más escépticos frente a las solicitudes de correo en cadena y solicitudes de complicidad para formar parte de transacciones financieras lucrativas y “legales”. A pesar de esto, el volumen de este tipo de correo y el uso de motores de correo con caballos de Troya hacen que siga siendo un método atractivo, con sólo un índice de éxito mínimo, para algunos piratas informáticos. La mayoría de estos ataques son personales y tienen como objetivo descubrir información sobre la identidad de la persona objeto de los mismos. Sin embargo, en el caso de las empresas, el abuso extendido de los sistemas comerciales, como equipos y acceso a Internet, para fines personales hace que los piratas informáticos puedan entrar en la red corporativa.

Los teléfonos ofrecen un método de contacto más personal y de menor volumen. Las pocas posibilidades de ser detenido hacen que algunos piratas informáticos usen el teléfono como medio de contacto, pero este método se usa principalmente para ataques al servicio de ayuda y centrales PBX; la mayoría de los usuarios desconfiaría de una llamada que solicite información de una persona a la que no conozcan personalmente.

**Contactos directos**
Menos habitual, aunque más efectivo para el pirata informático es el contacto directo y personal con una persona objeto de un ataque. Sólo el empleado más cauto dudará de la validez de alguien que se presente y que pida u ofrezca ayuda con un sistema informático. Si bien estos métodos tienen muchos más riesgos para el que los perpetra, las ventajas son obvias. El pirata informático puede obtener un acceso sin límites a equipos de la compañía, en cualquier defensa de perímetro tecnológica que exista.

El aumento del uso de tecnologías móviles, que permite a los usuarios conectarse a redes corporativas mientras se encuentran de viaje o en sus casas, suponen otra importante amenaza para los recursos de TI de la compañía. Los posibles ataques en este campo incluyen el ataque de observación más sencillo, en el que un pirata informático observa por detrás de un usuario de un equipo móvil en un tren para ver su Id. de usuario y contraseña, hasta ataques más sofisticados donde un técnico de servicio muy solícito entrega e instala un lector de tarjetas o una actualización de enrutador para poder obtener acceso a la red de la empresa pidiendo el Id. de usuario, su contraseña y, tal vez, un café. Un pirata informático concienzudo incluso podría solicitar al usuario una firma de autorización; ahora ya tiene la firma del usuario. Entre estos tipos de ataques se incluyen amenazas como vecinos que usan el ancho de banda que paga la compañía para tener acceso a Internet mediante una LAN inalámbrica desprotegida.

Si bien la mayoría de las grandes empresas cuentan con infraestructuras de seguridad para sus instalaciones altamente desarrolladas, las oficinas más pequeñas, de tamaño medio, tal vez no pongan tantos impedimentos para el acceso a sus instalaciones. El *seguimiento*, en el que una persona no autorizada sigue a alguien que tiene un pase para entrar a una oficina, es un ataque de ingeniería social muy sencillo. El intruso abre la puerta, que el usuario autorizado traspasa y, a continuación, el primero inicia una conversación sobre el tiempo o un partido del fin de semana mientras pasan juntos por el área de recepción. Este método no funcionaría en una gran compañía, donde cada persona tendría que pasar su tarjeta por un torniquete o en una pequeña compañía donde todos se conocen. Sin embargo, es perfectamente válido en una compañía con mil empleados, donde es habitual que un empleado no conozca a todos los demás. Si el impostor hubiera obtenido acceso anteriormente a la información de la compañía, como nombres de departamentos, nombres de empleados o algún otro tipo informe interno, la conversación de distracción sería más creíble.

La seguridad de los trabajadores en casa suele estar limitada a la tecnología. La directiva de seguridad debe exigir que los firewalls garanticen que los piratas informáticos externos no puedan tener acceso a las redes. Aparte de este requisito, la mayoría de las medianas empresas permiten que sus empleados que trabajan en casa se ocupen de su propia seguridad e incluso de las copias de seguridad.

**Tabla 7. Ataques con acceso físico y costos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objetivos de los ataques</p></th>
<th><p>Descripción</p></th>
<th><p>Costo</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Robo de la identidad del usuario móvil</p></td>
<td style="border:1px solid black;"><p>El pirata informático observa al usuario legítimo cuando éste especifica la información de inicio de sesión u otros detalles en el equipo. Esto puede permitir el robo de un equipo físico.</p></td>
<td style="border:1px solid black;"><p><strong>Información confidencial</strong></p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Robo de la identidad del usuario que trabaja en casa</p></td>
<td style="border:1px solid black;"><p>El pirata informático se hace pasar por un trabajador de soporte de TI o un socio de mantenimiento para obtener acceso a la red del trabajador en casa y solicita el Id. y la contraseña del usuario para probar que la actualización se realizó con éxito.</p></td>
<td style="border:1px solid black;"><p><strong>Información confidencial</strong></p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Contacto directo con la red mediante la red del trabajador en casa</p></td>
<td style="border:1px solid black;"><p>El pirata informático tiene acceso a la red de la compañía mediante la red del trabajador en casa haciéndose pasar por un ingeniero de soporte técnico. El pirata informático tiene un acceso sin límites a los recursos de la red y la compañía.</p></td>
<td style="border:1px solid black;"><p><strong>Información confidencial</strong></p>
<p><strong>Credibilidad comercial</strong></p>  
<p><strong>Disponibilidad comercial</strong></p>  
<p><strong>Recursos</strong></p>
<p>Dinero</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Acceso continuado a la red del trabajador en casa</p></td>
<td style="border:1px solid black;"><p>El pirata informático o el usuario local tiene acceso de banda ancha a Internet mediante una red doméstica desprotegida.</p></td>
<td style="border:1px solid black;"><p><strong>Recursos</strong></p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Acceso a las oficinas de la compañía sin compañía</p></td>
<td style="border:1px solid black;"><p>El pirata informático sigue a un empleado autorizado para entrar en las oficinas de la compañía.</p></td>
<td style="border:1px solid black;"><p>Información confidencial</p>
<p>Credibilidad comercial</p>  
<p>Disponibilidad comercial</p>  
<p>Dinero</p>
<p>Recursos</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Acceso de un individuo a una oficina de la compañía</p></td>
<td style="border:1px solid black;"><p>El pirata informático obtiene acceso a un individuo, lo que le permite intentar usar el equipo informático o recursos en papel, como archivadores.</p></td>
<td style="border:1px solid black;"><p><strong>Información confidencial</strong></p>
<p><strong>Recursos</strong></p>
<p>Dinero</p></td>
</tr>
</tbody>
</table>
<p> </p>

Las defensas frente a estas amenazas dependen fundamentalmente de la implementación de procedimientos recomendados por parte de los usuarios, basados en una directiva de seguridad efectiva de la compañía que debe tratar las tres áreas siguientes:

-   Las instalaciones de la compañía

-   El hogar

-   El trabajo móvil

Sería imposible acceder a las instalaciones de una compañía si no se contara con la autorización adecuada. El personal de recepción debe ser educado pero firme cuando reciban al personal, a los contratistas o a los visitantes. Unas pocas y sencillas condiciones dentro de la directiva de seguridad de la compañía harán que sea prácticamente imposible que una persona dispuesta a realizar un ataque de ingeniería social físico tenga acceso al edificio. Estas condiciones podrían incluir el uso de:

-   Pases con identificación fotográfica, que se deben mostrar cada vez que un empleado entre o salga del edificio.

-   Un libro de visitas firmado por el visitante y autorizado por el empleado al que visita tanto al llegar como al salir.

-   Pases de visita con fecha visibles en todo momento y que se deben devolver en la recepción al salir.

-   Un libro de contratistas firmado por el contratista y autorizado por el empleado que autorizó su trabajo al llegar y salir.

-   Pases de contratistas con fecha visibles en todo momento y que se deben devolver en la recepción al salir.

Para asegurarse de que todas las personas se presentan al empleado de la recepción, la compañía debe crear barreras para asegurarse de que los visitantes pasan directamente por delante de éste para presentar sus credenciales o firmar. Dichas barreras no tienen que ser torniquetes o barreras por las que tendrán que pasar.

Por ejemplo, un área de recepción puede tener algo tan relajante como un sofá para que la gente se siente mirando hacia la persona de recepción, como muestran los dos ejemplos de la siguiente figura.

![](images/Cc875841.HPISET05(es-es,TechNet.10).gif)

**Figura 5. Diseño de la recepción**

El área de recepción de la izquierda permite a un visitante no autorizado *seguir a una persona*, usando a un empleado legítimo para ocultarse. En el ejemplo de la derecha cualquier visitante tendría que pasar por delante de la recepción. La posición del equipo no tapa la visión del empleado de la recepción. El espacio debe ser lo suficientemente amplio como para permitir que cualquier persona pueda pasar sin problemas, incluidas las personas que usan sillas de ruedas. Es fundamental que los empleados de recepción reciban la instrucción necesaria y sean coherentes cuando reciban y comprueben la identidad de los visitantes. Todas las entradas al edificio deben cumplir con estos estándares y el personal sólo debe usar las entradas y salidas autorizadas al edificio; no debe haber puertas traseras.

Cuando se cree cualquier sistema de control de puertas o separaciones, debe asegurarse de que cumple con la normativa sobre seguridad y accesibilidad.

En el domicilio, no es realista autorizar a que entre cualquier vendedor o persona que venga. En realidad, la mayoría de las personas suelen ser mucho más precavidas sobre las visitas que reciben en su hogar de lo que lo son con las que visitan la oficina. Lo que es más importante aún, debe asegurarse de que un ataque no pueda tener acceso a los recursos de la empresa. Un protocolo sobre los servicios de TI externos debe incluir reglas que estipulen las siguientes condiciones:

-   Cada acción de soporte técnico, ya sea una solución in situ o una actualización, debe estar planeada y autorizada por el personal de soporte técnico.

-   Los contratistas y el personal interno que realizan tareas in situ de mantenimiento o de instalaciones deben tener una identificación, que incluya preferiblemente una fotografía.

-   El usuario debe contactar con el departamento de soporte de TI para indicarles cuándo llega el técnico y cuándo finaliza el trabajo.

-   Cada puesto tiene una hoja correspondiente, que firma el usuario.

-   El usuario nunca debe proporcionar información de acceso personal ni iniciar sesión en el equipo para proporcionar acceso a un técnico.

Este último punto es crucial. Es responsabilidad del grupo de servicios de TI asegurarse de que cualquier técnico externo tenga el acceso personal suficiente para realizar su trabajo. Si el técnico no tiene un acceso de usuario suficiente para realizar una tarea, debe contactar con el servicio de ayuda. Este requisito es esencial, ya que trabajar como modesto técnico para una compañía de servicios informáticos es uno de los puestos más rentables que un posible pirata informático puede encontrar, ya que lo convierte en una figura de autoridad técnica y en ayudante a la vez.

Los trabajadores móviles suelen usar sus equipos en lugares con mucha gente, como trenes o estaciones, aeropuertos o restaurantes. Claramente, es mucho más improbable asegurarse de que nadie le observa mientras escribe en uno de estos lugares, pero la directiva de seguridad de la compañía debe ofrecer consejo sobre cómo reducir los riesgos que suponen para la información personal y de la empresa. Si los empleados usan asistentes digitales personales (PDA), debe incluir información sobre la administración de seguridad y la sincronización.

**Ingeniería social inversa**
La *ingeniería social inversa* describe una situación en la que la persona o personas objetivo realizan el contacto inicial y ofrecen al pirata informático la información que desean. Aunque esta situación pueda parecer improbable, figuras de autoridad, sobre todo autoridad técnica o social, suelen recibir información personal fundamental, como los Id. y contraseñas de los usuarios porque están por encima de toda sospecha. Por ejemplo, ningún trabajador del departamento de soporte pediría a la persona que llama su Id. o contraseña de usuario; simplemente soluciona los problemas sin esta información. Muchos usuarios que tienen problemas de TI ofrecerían de forma voluntaria estos elementos de seguridad fundamentales para conseguir rápidamente una solución a su problema. El pirata informático no tendría ni que preguntar. Los ataques de ingeniería social no son tan reactivos como puede sugerir este contexto.

Un ataque de ingeniería social crea un situación, aconseja una solución y proporciona ayuda cuando se solicita, puede que de forma tan sencilla como en el siguiente caso:

Un compañero de trabajo, que es en realidad un pirata informático, cambia el nombre o mueve un archivo para que el objetivo de su ataque piense que ya no existe dicho archivo. El pirata informático especula con la posibilidad de recuperar el archivo. El objetivo del ataque, que desea poder continuar con su trabajo, o preocupado por ser culpable de esa pérdida de información, cede ante su oferta. El pirata informático dice que para poder recuperarlo tendría que iniciar sesión como si fuera la otra persona. Incluso puede decir que la directiva de la compañía prohíbe esto. El objetivo del ataque pedirá al pirata informático que inicie sesión como si fuera él para intentar recuperar el archivo. De mala gana, el pirata informático acepta, recupera el archivo original y roba el Id. y la contraseña del usuario. Incluso puede que mejore su reputación de forma que reciba solicitudes de ayuda de otros compañeros de trabajo. Con este método se pueden eludir los canales de soporte técnico de TI habituales y permitir que el pirata informático no sea detectado.

No siempre es necesario tener información o incluso conocer a un objetivo para usar la ingeniería social inversa. Inventar problemas mediante cuadros de diálogo puede ser útil en un ataque de ingeniería social inversa no específico. En el cuadro de diálogo se avisa de que hay un problema o de que se debe realizar una actualización para continuar. En el cuadro de diálogo se ofrece una descarga para solucionar el problema. Cuando la descarga finaliza, el problema supuesto desaparece y el usuario sigue trabajando, sin saber que incumplió la directiva de seguridad y descargó un programa de malware.

**Tabla 8. Ataques de ingeniería social inversa y costos**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objetivos de los ataques</p></th>
<th><p>Descripción</p></th>
<th><p>Costo</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Robo de identidad</p></td>
<td style="border:1px solid black;"><p>El pirata informático recibe el ID. y la contraseña de un usuario autorizado.</p></td>
<td style="border:1px solid black;"><p>Información confidencial</p>
<p>Credibilidad comercial</p>  
<p>Disponibilidad comercial</p>  
<p>Dinero</p>
<p>Recursos</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Robo de información</p></td>
<td style="border:1px solid black;"><p>El pirata informático usa el Id. y la contraseña del usuario autorizado para obtener acceso a los archivos de la compañía.</p></td>
<td style="border:1px solid black;"><p><strong>Información confidencial</strong></p>
<p><strong>Dinero</strong></p>  
<p><strong>Recursos</strong></p>  
<p>Credibilidad comercial</p>
<p>Disponibilidad comercial</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Descarga de malware</p></td>
<td style="border:1px solid black;"><p>El pirata informático engaña a un usuario para que haga clic en un hipervínculo o abra un archivo adjunto y, de esta forma, infecte la red de la compañía.</p></td>
<td style="border:1px solid black;"><p><strong>Disponibilidad comercial</strong></p>
<p>Credibilidad comercial</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Descarga de software del pirata informático</p></td>
<td style="border:1px solid black;"><p>El pirata informático engaña a un usuario para que haga clic en un hipervínculo o abra un archivo adjunto y, de esta forma, descargue un programa suyo, como un motor de correo, que use recursos de la red de la compañía.</p></td>
<td style="border:1px solid black;"><p><strong>Recursos</strong></p>
<p><strong>Credibilidad comercial</strong></p>
<p>Dinero</p></td>
</tr>
</tbody>
</table>
<p> </p>

Defenderse frente a la ingeniería social inversa es probablemente el desafío más difícil. El objetivo del ataque no tiene motivos para sospechar del pirata informático, porque cree que controlan la situación. La principal defensa es la estipulación en la directiva de seguridad de que todos los problemas se deben resolver mediante el servicio de ayuda. Si los miembros del servicio de ayuda son eficientes, educados y no se erigen en jueces, el resto de empleados acudirán a ellos, en lugar de pedir ayuda a un empleado no autorizado o a conocidos.

[](#mainsection)[Principio de la página](#mainsection)

### Diseño de defensas frente a las amenazas de la ingeniería social

Una vez comprendida la amplia gama de amenazas que existen, se necesitan tres pasos para diseñar un sistema de defensa frente a las amenazas de la ingeniería social hacia el personal de su compañía. Una defensa efectiva es contar con una función de planeamiento. Las defensas suelen ser reactivas: se detecta un ataque que tuvo éxito y se crea una barrera para garantizar que el problema no vuelva a producirse. Si bien este método demuestra cierto nivel de concienciación, la solución llega demasiado tarde si el problema es grave o costoso. Para adelantarse a esta situación, debe realizar los tres pasos siguientes:

-   **Crear un marco de administración de la seguridad**. Debe definir un conjunto de objetivos de seguridad de ingeniería social y de empleados responsables de lograr que se cumplan.

-   **Realizar evaluaciones sobre la administración de riesgos**. Amenazas similares no presentan el mismo nivel de riesgo para distintas compañías. Debe revisar cada una de las amenazas de ingeniería social y racionalizar el peligro que presenta cada una para su organización.

-   **Implementar defensas de ingeniería social en su directiva de seguridad**. Cree un conjunto escrito de directivas y procedimientos que estipulen la forma en que su personal debe enfrentarse a las situaciones que puedan suponer ataques de ingeniería social. En este paso se asume que existe una directiva de seguridad, aparte de la amenaza que supone la ingeniería social. Si actualmente no dispone de una directiva de seguridad, tendrá que crear una. Los elementos que identifique su evaluación de riesgos de ingeniería social serán un comienzo, pero tendrá que tener en cuenta otras posibles amenazas.

    Para obtener más información acerca de las directivas de seguridad, consulte el sitio web sobre [seguridad de Microsoft](http://www.microsoft.com/security) en www.microsoft.com/security (puede estar en inglés).

#### Creación de un marco de administración de la seguridad

Un marco de administración de la seguridad define una visión general de las posibles amenazas que suponen para su organización la ingeniería social y asigna funciones con puestos responsables del desarrollo de directivas y procedimientos que mitiguen esas amenazas. Este método no significa que tenga que contratar a personal cuyas únicas funciones sean asegurar la seguridad de los activos de la empresa. Si bien este método puede ser una opción en grandes organizaciones, resulta poco viable o deseable tener asignadas esas funciones en las medianas empresas. El requisito consiste en asegurarse de que un grupo de personas asuma las responsabilidades clave de las siguientes funciones de seguridad:

-   **Patrocinador de seguridad**. Miembro de la directiva, probablemente del consejo, que pueda tener la autoridad necesaria para asegurar que todo el personal asuma con seriedad el tema de la seguridad.

-   **Administrador de seguridad**. Empleado de la directiva que tiene la responsabilidad de orquestar el desarrollo y mantenimiento de una directiva de seguridad.

-   **Empleado de seguridad de TI**. Empleado técnico que tiene la responsabilidad de desarrollar la infraestructura de TI y las directivas y procedimientos de seguridad operativos.

-   **Empleado de seguridad de las instalaciones**. Miembro del equipo de instalaciones responsable de desarrollar directivas y procedimientos del sitio y operativos.

-   **Empleado de concienciación sobre la seguridad**. Miembro de la directiva, normalmente del departamento de recursos humanos o de desarrollo de personal, responsable del desarrollo y la ejecución de campañas de concienciación sobre la seguridad.

Este grupo, el comité de control de seguridad, representa a los moderadores de la compañía. Como responsables seleccionados para la seguridad, este comité debe establecer los principales objetivos del marco de administración de la seguridad. Sin un conjunto de objetivos definibles, es difícil fomentar la participación del resto del personal o medir el éxito del proyecto. La tarea inicial del comité de control de seguridad es identificar las vulnerabilidades de ingeniería social que existen en la compañía. Una sencilla tabla como la siguiente le permitirá hacerse rápidamente una idea de estos vectores de ataque.

**Tabla 9. Vulnerabilidades vectoriales de los ataques de ingeniería social a compañías**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Vector de ataque</p></th>
<th><p>Descripción de uso de la compañía</p></th>
<th><p>Comentarios</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p><em>En línea</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Correo electrónico</p></td>
<td style="border:1px solid black;"><p>Todos los usuarios tienen Microsoft Outlook® en sus equipos de escritorio.</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Internet</p></td>
<td style="border:1px solid black;"><p>Los usuarios móviles tienen Outlook Web Access (OWA) además de acceso al cliente de Outlook.</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Aplicaciones emergentes</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Actualmente no se implementa ninguna barrera tecnológica contra los elementos emergentes.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Mensajería instantánea</p></td>
<td style="border:1px solid black;"><p>La compañía permite el uso no administrado de una serie de productos de mensajería instantánea.</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><em>Teléfono</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Central de conmutación (PBX)</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Servicio de ayuda</p></td>
<td style="border:1px solid black;"><p>Actualmente el “servicio de ayuda” es una función de soporte informal que ofrece el departamento de TI.</p></td>
<td style="border:1px solid black;"><p>Necesitamos ampliar los servicios de soporte para que incluyan otras áreas adicionales a la de TI.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><em>Gestión de residuos</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Interno</p></td>
<td style="border:1px solid black;"><p>Todos los departamentos gestionan sus propios residuos.</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Externo</p></td>
<td style="border:1px solid black;"><p>Los contenedores están situados fuera de las instalaciones de la compañía. La recogida de basura se produce los jueves.</p></td>
<td style="border:1px solid black;"><p>Actualmente no tenemos espacio para contenedores dentro de las instalaciones.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><em>Contactos directos</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Seguridad física</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Seguridad de la oficina</p></td>
<td style="border:1px solid black;"><p>Todas las oficinas permanecen abiertas durante el día.    </p></td>
<td style="border:1px solid black;"><p>El 25% del personal trabaja desde casa.    No contamos con estándares escritos para la seguridad de los trabajadores en casa.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Trabajadores en casa</p></td>
<td style="border:1px solid black;"><p>No tenemos protocolos de mantenimiento in situ para los trabajadores en casa.</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><em>Otros, específicos de la compañía</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Franquicias internas</p></td>
<td style="border:1px solid black;"><p>Todo el catering lo realiza una franquicia.</p></td>
<td style="border:1px solid black;"><p>No sabemos nada sobre este personal y no hay ninguna directiva de seguridad para ellos.</p></td>
</tr>  
</tbody>  
</table>
  
Cuando el comité de control de seguridad conozca bien las vulnerabilidades, podrá crear una tabla Vulnerabilidades vectoriales de ataque de ingeniería social a compañías (como se muestra en el ejemplo anterior). En la tabla se señalan los protocolos de la compañía en áreas potencialmente vulnerables. Conocer las vulnerabilidades permite al comité crear un borrador con los posibles requisitos de directivas.
  
El comité de control de seguridad debe identificar en primer lugar las áreas que pueden suponen un riesgo para la compañía. Este proceso debe incluir todos los vectores de ataque identificados en este artículo y los elementos específicos de la compañía, como el uso de terminales públicas o procedimientos de administración de la oficina.
  
#### Evaluación de riesgos
  
Cualquier tipo de seguridad exige que se evalúe el nivel de riesgo que supone un ataque para la compañía. Si bien la evaluación de riesgos debe ser concienzuda, no tiene que tardarse mucho tiempo en realizarse. Según el trabajo realizado para identificar los elementos principales de un marco de administración de la seguridad por parte del comité de control de seguridad, podrá establecer categorías y prioridades en los riesgos. Entre las categorías de riesgo se incluyen:
  
-   Información confidencial
  
-   Credibilidad comercial
  
-   Disponibilidad comercial
  
-   Recursos
  
-   Dinero
  
Debe establecer prioridades mediante la identificación del riesgo y el cálculo del costo que implica su mitigación; si mitigar un riesgo es más caro que el propio riesgo, puede que dicho costo no sea justificable. La fase de evaluación de riesgos puede resultar muy útil en el desarrollo final de la directiva de seguridad.
  
Por ejemplo, el comité de control de seguridad puede resaltar al personal de recepción el peligro para la seguridad que suponen los visitantes. En el caso de una compañía que no espera más de 20 visitantes a la hora, no hay necesidad de tener que pensar en algo más sofisticado que un(a) recepcionista, un libro de firmas y algunos pases de visitantes numerados. Sin embargo, en el caso de una compañía que espera 150 visitas a la hora, puede que sea necesario más personal de recepción o terminales de registro de autoservicio. Si bien la compañía más pequeña no podría justificar los costos de estos terminales, la compañía grande no podría justificar el costo de la pérdida de actividad debido a largas esperas.
  
Por otro lado, una compañía que nunca tenga visitas ni personal contratista puede considerar que existe un riesgo mínimo de dejar documentos en una ubicación central mientras esperan a ser recogidos. Sin embargo, una compañía que tenga una gran número de personas que no sean empleados puede considerar que tiene que salvar el riesgo comercial que presentaría que hubiera información confidencial en una impresora mediante la instalación de dispositivos de impresión locales en cada puesto de trabajo. La compañía puede obviar este riesgo mediante la estipulación de que un miembro del personal acompañe a un visitante durante su visita. Esta solución es mucho menos cara, excepto, posiblemente en términos de tiempo del personal.
  
Según la evaluación comercial de la matriz Vulnerabilidades vectoriales de ataque de ingeniería social a compañías, el comité de control de seguridad podrá definir los requisitos de directivas, los tipos y niveles de riesgo para la compañía, como se muestra en la siguiente tabla.
  
**Tabla 10. Requisitos del comité de control de seguridad y matriz de riesgos**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="20%" />  
<col width="20%" />  
<col width="20%" />  
<col width="20%" />  
<col width="20%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Vector de ataque</p></th>  
<th><p>Posible requisito de directiva</p></th>  
<th><p>Tipo de riesgo Información confidencial Credibilidad comercial Disponibilidad comercial Recursos Dinero</p></th>  
<th><p>Nivel de riesgo Alto = 5 Bajo = 1</p></th>  
<th><p>Acción</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Conjunto escrito de directivas de seguridad frente a la ingeniería social</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Cambios para crear la parte de cumplimiento de la directiva del contrato del empleado estándar</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Cambios para crear la parte de cumplimiento de la directiva del contrato del contratista estándar</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><em>En línea</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Correo electrónico</p></td>
<td style="border:1px solid black;"><p>Directiva sobre los tipos de archivos adjuntos y cómo tratarlos</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Internet</p></td>
<td style="border:1px solid black;"><p>Directiva de uso de Internet</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Aplicaciones emergentes</p></td>
<td style="border:1px solid black;"><p>Directiva sobre el uso de Internet, con una especial atención en qué hacer con los cuadros de diálogo inesperados</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Mensajería instantánea</p></td>
<td style="border:1px solid black;"><p>Directiva sobre los clientes de mensajería instantánea admitidos y permitidos</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><em>Teléfono</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Central de conmutación (PBX)</p></td>
<td style="border:1px solid black;"><p>Directiva sobre la administración del soporte de centrales PBX</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Servicio de ayuda</p></td>
<td style="border:1px solid black;"><p>Directiva para permitir el acceso a los datos</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><em>Gestión de residuos</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Papel</p></td>
<td style="border:1px solid black;"><p>Directiva para la gestión de residuos de papel</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>Directrices para la gestión de contenedores</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Medios electrónicos</p></td>
<td style="border:1px solid black;"><p>Directiva para la gestión de los materiales de residuo de medios electrónicos</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><em>Contactos directos</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Seguridad física</p></td>
<td style="border:1px solid black;"><p>Directiva para la administración de visitas</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Seguridad de la oficina</p></td>
<td style="border:1px solid black;"><p>Directiva para la administración de Id. de usuario y contraseñas: no escribir las contraseñas en una nota adhesiva ni pegarla a la pantalla, por ejemplo.</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Trabajadores en casa</p></td>
<td style="border:1px solid black;"><p>Directiva para el uso de equipos móviles fuera de la compañía</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><em>Otros/</em><br />
<em>específicos de la compañía</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Franquicias internas</p></td>
<td style="border:1px solid black;"><p>Directa para conocer los antecedentes de los empleados de franquicias internas</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
</tbody>  
</table>
  
El comité de control de seguridad debe lograr un consenso sobre la importancia de un riesgo. Cada grupo comercial tendrá distintos puntos de vista sobre los riesgos que suponen las distintas amenazas.
  
Para obtener más información acerca de las herramientas y metodologías de la evaluación de riesgos, consulte la [*Guía de administración de riesgos de seguridad*](http://go.microsoft.com/fwlink/?linkid=30794) en http://go.microsoft.com/fwlink/?linkid=30794 (puede estar en inglés).
  
#### La ingeniería social en la directiva de seguridad
  
El personal de administración y TI de una compañía debe desarrollar y ayudar a implementar una directiva de seguridad efectiva en la organización. En ocasiones, el centro de atención de una directiva de seguridad son los controles tecnológicos que le ayudarán a protegerse frente a amenazas tecnológicas, como virus y gusanos. Los controles tecnológicos ayudan a defender las tecnologías, como archivos de datos, archivos de programas y sistemas operativos. Las defensas frente a la ingeniería social deben ayudar a anticipar los posibles ataques genéricos de ingeniería social contra los empleados.
  
El comité de control de seguridad tiene las principales áreas de seguridad y la evaluación de riesgos en los que debe delegar el desarrollo de procedimientos, procesos y documentación comercial. En la siguiente tabla se muestra cómo el comité de control de seguridad, con la ayuda de grupos de interés, puede definir la documentación necesaria para apoyar la directiva de seguridad.
  
**Tabla 11. Procedimiento del comité de control y documentos necesarios**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="33%" />  
<col width="33%" />  
<col width="33%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Requisito de directiva</p></th>  
<th><p>Procedimiento / documento necesario</p></th>  
<th><p>Acción / fecha</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Conjunto escrito de directivas de seguridad frente a la ingeniería social</p></td>
<td style="border:1px solid black;"><p>Ninguna</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Cambios para crear la parte de cumplimiento de la directiva del contrato del empleado estándar</p></td>
<td style="border:1px solid black;"><ol>
<li><p>Texto para los requisitos de nuevos contratos (legal)</p></li>  
<li><p>Nuevo formato para los contratos de los contratistas</p></li>
</ol></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Cambios para crear la parte de cumplimiento de la directiva del contrato del contratista estándar</p></td>
<td style="border:1px solid black;"><ol>
<li><p>Texto para los requisitos de nuevos contratos (legal)</p></li>  
<li><p>Nuevo formato para los contratos de los contratistas</p></li>
</ol></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Directiva para la administración de visitas</p></td>
<td style="border:1px solid black;"><ol>
<li><p>Procedimiento para la firma a la llegada y salida de los visitantes</p></li>  
<li><p>Procedimiento para el acompañamiento a los visitantes</p></li>
</ol></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Directrices para la gestión de contenedores</p></td>
<td style="border:1px solid black;"><ol>
<li><p>Procedimiento para el desecho de los residuos de papel (consulte Datos)</p></li>  
<li><p>Procedimiento para el desecho de los medios electrónicos (consulte Datos)</p></li>
</ol></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Directiva para permitir el acceso a los datos</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Directiva para la gestión de residuos de papel</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Directiva para la gestión de los materiales de residuo de medios electrónicos</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Directiva para el uso de Internet, con una atención especial en lo que hacer con cuadros de diálogo inesperados</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Directiva para la administración de Id. de usuario y contraseñas: no escribir las contraseñas en una nota adhesiva ni pegarlas a la pantalla, etc.</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Directiva para el uso de equipos móviles fuera de la compañía</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Directiva para tratar los problemas relacionados con la conexión a aplicaciones relacionadas (bancarias, financieras, de compra, de administración de existencias)</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
</tbody>  
</table>
  
Como puede ver, esta lista puede ser muy larga. Puede decidir contratar ayuda especializada para agilizar este elemento del proceso. El comité de control de seguridad debe centrarse en las áreas que considere de gran importancia, según el proceso de evaluación de riesgos.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Implementación de defensas frente a las amenazas de la ingeniería social
  
Después de escribir y acordar la directiva de seguridad, debe darla a conocer al personal y hacer que la cumpla. Si bien puede implementar controles técnicos sin que lo sepan sus empleados, debe conseguir su apoyo si desea implementar con éxito defensas frente a la ingeniería social. Para apoyar la implementación, debe desarrollar protocolos de respuesta a incidentes para el personal del servicio de ayuda.
  
#### Concienciación
  
No hay ningún sustituto a una buena campaña de concienciación cuando se implementan los elementos de ingeniería social de la directiva de seguridad. Claro está, la implementación es una forma de ingeniería social y debe conseguir que su personal conozca la directiva, aprenda por qué existe y sepa cómo debe reaccionar ante un posible ataque. El elemento clave de un ataque de ingeniería social es la confianza; la persona objeto del ataque confía en el pirata informático. Para enfrentarse a este tipo de ataque, debe estimular a que haya un saludable escepticismo entre su personal sobre cualquier cosa que se salga de lo normal y conseguir que éstos confíen en la infraestructura de soporte de TI de la compañía.
  
Los elementos de una campaña de concienciación dependen de cómo se transmite la información al personal de la compañía. Puede optar por un aprendizaje estructurado, reuniones menos formales, campañas con pósteres u otros eventos para anunciar las directivas de seguridad. Cuanto más refuerce los mensajes de sus directivas, más exitosa será su implementación. Si bien puede iniciar la concienciación sobre seguridad con un gran evento, es igualmente importante que la seguridad siga siendo un asunto importante de la agenda de la directiva y el personal. La seguridad es un modo de pensar de la compañía, por lo que debe asegurarse de que las sugerencias sobre seguridad acerca del mantenimiento de la concienciación sobre este tema vengan de todas las personas de la compañía. Consiga opiniones de todos los departamentos y de distintos tipos de usuarios, especialmente, de los que trabajan fuera del entorno de la oficina.
  
#### Administración de incidentes
  
Cuando se produce un ataque de ingeniería social, asegúrese de que el personal de servicio de ayuda sabe cómo tratarlo. Deben existir protocolos reactivos en los procedimientos relacionados con la directiva de seguridad, pero la administración de incidentes significa que se usa el ataque para iniciar posteriores revisiones de la seguridad. La seguridad es más un viaje que un destino, ya que los vectores de ataque cambian.
  
Cada incidente proporciona nueva información para una revisión continua de la seguridad en el modelo de respuesta a incidentes, que se muestra en la siguiente figura.
  
![](images/Cc875841.HPISET06(es-es,TechNet.10).gif)
  
**Figura 6. Modelo de respuesta a incidentes**
  
Conforme se produzcan nuevos incidentes, el comité de control de seguridad revisará si éstos representan un riesgo nuevo o modificado para la compañía y creará o renovará las directivas y los procedimientos según esos datos. Todas las modificaciones que se realicen en las directivas de seguridad deben cumplir con los estándares de administración de cambios de la compañía.
  
Para administrar un incidente, el personal del servicio de ayuda debe contar con un sólido protocolo de comunicación de incidentes que registre la siguiente información:
  
-   Nombre de la persona objeto del ataque
  
-   Departamento objeto del ataque
  
-   Fecha
  
-   Vector de ataque
  
-   Descripción del ataque
  
-   Resultado del ataque
  
-   Efecto del ataque
  
-   Recomendaciones
  
Al registrar los incidentes, se pueden identificar patrones y posiblemente adelantarse a posteriores ataques. En el Apéndice 1 del final del documento se ofrece una plantilla de formulario con un informe de incidente.
  
#### Consideraciones operativas
  
Cuando se revisa la seguridad, puede existir la tendencia de convertirse en demasiado sensible ante la ingente cantidad de posibles amenazas contra la empresa. La directiva de seguridad debe mantener la idea de que su empresa está ahí para hacer negocios. Si las propuestas de seguridad afectan negativamente a la rentabilidad o al agilidad comercial de la organización, tal vez tenga que volver a evaluar el riesgo. Debe lograr un equilibro entre la seguridad y la operatividad.
  
También es importante reconocer que una reputación como compañía que se preocupa por la seguridad puede tener ventajas comerciales. No desalentará a los piratas informáticos, pero, por su parte, mejorará el perfil comercial de la compañía con los clientes y socios.
  
#### Ingeniería social y el modelo de niveles de defensa en profundidad
  
El modelo de niveles de defensa en profundidad clasifica las soluciones de seguridad frente a vectores de ataque (áreas de debilidad) que los piratas informáticos pueden usar para amenazar a sus equipos. Estos vectores de ataque son:
  
-   **Directivas, procedimientos y concienciación**. Reglas escritas que desarrolle para administrar todas las áreas de seguridad y el programa de enseñanza que implante para conseguir que los empleados conozcan, aprendan e implementen dichas reglas.
  
-   **Seguridad física**. Barreras que administran el acceso a sus instalaciones y recursos. Es importante recordar este último elemento; si coloca los contenedores de residuos fuera de la compañía, por ejemplo, quedarán fuera de la seguridad física de la compañía.
  
-   **Datos**. Información de la empresa: detalles de cuentas, correo, etc. Cuando tenga en cuenta las amenazas de la ingeniería social, debe incluir tanto los materiales impresos como en medios electrónicos en el planeamiento de la seguridad de los datos.
  
-   **Aplicación**. Programas ejecutados por los usuarios. Debe tratar el método en que los piratas informáticos de ingeniería social pueden trastocar las aplicaciones, como el correo electrónico y la mensajería instantánea.
  
-   **Host**. Servidores y equipos clientes que se usan en la organización. Ayudan a asegurar que los usuarios estén protegidos frente a ataques directos en dichos equipos al definir directrices estrictas sobre el software que se debe usar en los equipos de la empresa y sobre cómo administrar los dispositivos de seguridad, como Id. de usuario y contraseñas.
  
-   **Red interna**. Red mediante la que se comunica el sistema informático. Puede ser local, inalámbrica o una red de área extensa (WAN). La red interna cada vez es menos “interna” en los últimos años, debido a los cada vez más extendidos trabajo móvil y en casa. Por lo tanto, debe asegurarse de que los usuarios entiendan lo que deben hacer para trabajar de forma segura en todos los entornos de red.
  
-   **Perímetro**. El punto de contacto entre las redes internas y externas, como Internet o las redes que pertenecen a los socios comerciales, tal vez como parte de una extranet. Los ataques de ingeniería social suelen intentar romper el perímetro para atacar los datos, aplicaciones y hosts mediante la red interna.
  
![](images/Cc875841.HPISET07(es-es,TechNet.10).gif)
  
**Figura 7. Modelo de defensa en profundidad**
  
Cuando diseñe sus defensas, este modelo le ayudará a visualizar las áreas de su empresa que están amenazadas. El modelo no es específico de las amenazas de ingeniería social, pero cada uno de los niveles debe contar con defensas frente a la ingeniería social.
  
Las defensas globales del modelo son: las directivas de seguridad, los procedimientos y la concienciación. Estas defensas van destinadas al personal de una organización, y en ellas se explica qué hacer, cuándo, por qué y quién debe hacerlo. Los demás niveles pueden ajustar las defensas, pero la protección esencial proviene de contar con un conjunto de reglas bien estructurado y conocido que proteja su entorno de TI.
  
Para obtener más información acerca del modelo de defensa en profundidad, consulte el tema [Función SMF de administración de la seguridad](http://go.microsoft.com/fwlink/?linkid=37696) en Microsoft TechNet en la dirección http://go.microsoft.com/fwlink/?linkid=37696 (puede estar en inglés).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Apéndice 1: Listas de comprobación de la directiva de seguridad para amenazas de ingeniería social
  
Se presentó una serie de tablas para capturar las vulnerabilidades de la ingeniería social y los requisitos de directiva de defensa en los documentos. En este apéndice encontrará versiones de plantillas de éstas que podrá copiar y rellenar.
  
#### Vulnerabilidades vectoriales de ataque de ingeniería social a compañías

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="33%" />  
<col width="33%" />  
<col width="33%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Vector de ataque</p></th>  
<th><p>Descripción de uso de la compañía</p></th>  
<th><p>Comentarios</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p><em>En línea</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Correo electrónico</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Internet</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Aplicaciones emergentes</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Mensajería instantánea</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><em>Teléfono</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Central de conmutación (PBX)</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Servicio de ayuda</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><em>Gestión de residuos</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Interno</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Externo</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><em>Contactos directos</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Seguridad física</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Seguridad de la oficina</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><em>Otros/específicos de la compañía</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
</tbody>  
</table>
  
#### Requisitos del comité de control de seguridad y matriz de riesgos

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="20%" />  
<col width="20%" />  
<col width="20%" />  
<col width="20%" />  
<col width="20%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Vector de ataque</p></th>  
<th><p>Posible requisito de directiva</p></th>  
<th><p>Tipo de riesgo Información confidencial Credibilidad comercial Disponibilidad comercial Recursos Dinero</p></th>  
<th><p>Nivel de riesgo Alto = 5 Bajo = 1</p></th>  
<th><p>Acción</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p><em>En línea</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><em>Teléfono</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><em>Gestión de residuos</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><em>Contactos directos</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><em>Otros/</em><br />
<em>específicos de la compañía</em></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
</tbody>  
</table>
  
#### Procedimiento del comité de control y documentos necesarios

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="33%" />  
<col width="33%" />  
<col width="33%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Requisito de directiva</p></th>  
<th><p>Procedimiento / documento necesario</p></th>  
<th><p>Acción en / fecha</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
</tbody>  
</table>
  
#### Lista de comprobación de implementación de la directiva de seguridad

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="33%" />  
<col width="33%" />  
<col width="33%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Acción</p></th>  
<th><p>Descripción</p></th>  
<th><p>Acción en / fecha</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Desarrollar directivas de seguridad en línea</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Desarrollar directivas de seguridad física</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Desarrollar directivas de seguridad telefónica</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Desarrollar directivas de seguridad de gestión de residuos</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Desarrollar directivas de administración de seguridad del servicio de ayuda</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Desarrollar un modelo de respuesta a incidentes</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Desarrollar una campaña de concienciación</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>...</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
</tbody>  
</table>
  
#### Informe de incidentes

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Representante del servicio de ayuda</p></td>
<td style="border:1px solid black;"><p>                     </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Nombre de la persona objeto del ataque</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Departamento objeto del ataque</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Fecha</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Vector de ataque</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Descripción del ataque</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Resultado del ataque</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Efecto del ataque</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Recomendaciones,</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
</tbody>  
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Apéndice 2: Glosario

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Término</p></th>  
<th><p>Definición</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>acceso</p></td>
<td style="border:1px solid black;"><p>En el contexto de la privacidad, capacidad de un individuo de ver, modificar y comprobar la precisión e integridad de la información personal identificable recopilada sobre él o ella. El acceso forma parte de las prácticas de información justas.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>software antivirus</p></td>
<td style="border:1px solid black;"><p>Programa informático diseñado para detectar y responder al software malintencionado, como virus y gusanos. Entre las respuestas se pueden incluir el bloqueo del acceso del usuario a los archivos infectados, la limpieza de los archivos o equipos infectados o la notificación al usuario que se detectó un programa infectado.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>ataque</p></td>
<td style="border:1px solid black;"><p>Intento deliberado de poner en peligro la seguridad de un sistema informático o de privar a los demás usuarios del uso del sistema.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>autenticación</p></td>
<td style="border:1px solid black;"><p>Proceso de validación de las credenciales de una persona, proceso informático o dispositivo. Para la autenticación se necesita que la persona, proceso o dispositivo que realiza la solicitud proporcione una credencial que demuestre que se trata en realidad de la entidad o persona que dice ser. Entre las formas habituales de credenciales se incluyen las firmas digitales, las tarjetas inteligentes, los datos biométricos y una combinación formada por los nombres de usuario y sus contraseñas.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>autorización</p></td>
<td style="border:1px solid black;"><p>Proceso por el que otorga a una persona, proceso informático o dispositivo acceso a determinada información, servicios o funcionalidades. La autorización se obtiene de la identidad de la persona, proceso informático o dispositivo que solicita el acceso, lo que se verifica mediante la autenticación.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>administración de cambios</p></td>
<td style="border:1px solid black;"><p>Práctica de administración de cambios con la ayuda de métodos y técnicas probados con el fin de evitar nuevos errores y reducir el impacto de los cambios.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>seguridad del equipo</p></td>
<td style="border:1px solid black;"><p>Protección de los activos de información mediante tecnología, procesos y aprendizaje.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>pirata informático</p></td>
<td style="border:1px solid black;"><p>Malhechor que entra en un equipo mediante estrategias tecnológicas y no de ingeniería social.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>descargar</p></td>
<td style="border:1px solid black;"><p>Transferir una copia de un archivo de un equipo remoto a un equipo que realiza la solicitud mediante un módem o una red.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>extranet</p></td>
<td style="border:1px solid black;"><p>Extensión de la intranet de una organización que se usa para facilitar la comunicación con los socios de confianza de la misma. Una extranet permite que estos socios de confianza obtengan acceso limitado a los datos comerciales internos de la organización.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>firewall</p></td>
<td style="border:1px solid black;"><p>Solución de seguridad que segrega una parte de una red de otra, lo que permite que sólo pase el tráfico de red autorizado según unas reglas de filtrado del tráfico.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>malware</p></td>
<td style="border:1px solid black;"><p>Software que cumple la intención deliberada de un atacante de producir daños cuando se ejecuta. Por ejemplo, los virus, gusanos y caballos de Troya constituyen código malintencionado.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>inicio de sesión de red</p></td>
<td style="border:1px solid black;"><p>Proceso de conexión a un equipo mediante una red. Normalmente, el usuario inicia sesión de forma interactiva en un equipo local y, a continuación, proporciona las credenciales de inicio de sesión a otro equipo de la red, como un servidor, que está autorizado a usar.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>contraseña</p></td>
<td style="border:1px solid black;"><p>Cadena de caracteres que un usuario escribe para verificar su identidad en una red o en un equipo local. Consulte también contraseña segura.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>permisos</p></td>
<td style="border:1px solid black;"><p>Autorización para realizar operaciones relacionadas con un recurso compartido específico, como un archivo, un directorio o una impresora. Los permisos los debe otorgar el administrador del sistema a cuentas de usuario individuales o grupos administrativos.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>número de identificación personal (PIN)</p></td>
<td style="border:1px solid black;"><p>Código de identificación secreto similar a una contraseña y que se asigna a un usuario autorizado. El PIN se usa junto con una tarjeta de cajero o inteligente, por ejemplo, para desbloquear una funcionalidad autorizada, como el acceso a una cuenta bancaria.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>información personal identificable</p></td>
<td style="border:1px solid black;"><p>Cualquier información relacionada con un individuo identificado o identificable. Esta información puede incluir: el nombre, el país, la dirección postal, la dirección de correo electrónico, el número de la tarjeta de crédito, el número de la Seguridad Social, el número del documento nacional de identidad, la dirección IP o cualquier otro identificador único relacionado con esta información personal identificable en otro sistema. También conocida como información personal o datos personales.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>información personal</p></td>
<td style="border:1px solid black;"><p>Consulte información personal identificable.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>phreaker</p></td>
<td style="border:1px solid black;"><p>Usuario malintencionado que usa de forma no autorizada la central de conmutación (PBX) para realizar llamadas.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>timador</p></td>
<td style="border:1px solid black;"><p>Usuario o sitio web malintencionado que engaña a las personas para que revelen información personal, como las contraseñas de sus cuentas y los números de sus tarjetas de crédito. Un timador suele usar mensajes de correo electrónico engañosos o anuncios en línea como anzuelo para que los usuarios confiados usen sitios web fraudulentos, donde se les engaña para que proporcionen información personal.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>vulnerabilidad física</p></td>
<td style="border:1px solid black;"><p>Imposibilidad de proporcionar seguridad física a un equipo, como dejar una estación de trabajo en funcionamiento desbloqueada en un área de trabajo, lo que permite el acceso a la misma de usuarios no autorizados.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>privacidad</p></td>
<td style="border:1px solid black;"><p>Control que los clientes tienen sobre la recopilación, uso y distribución de su información personal.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>vulnerabilidad de seguridad</p></td>
<td style="border:1px solid black;"><p>Vulnerabilidad del software que se soluciona con una actualización de seguridad de Microsoft y un boletín de seguridad o Service Pack.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>correo no deseado</p></td>
<td style="border:1px solid black;"><p>Mensajes de correo electrónico comercial no solicitado. También conocido como correo electrónico no deseado.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>suplantar</p></td>
<td style="border:1px solid black;"><p>Hacer que una transmisión parezca provenir de un usuario que no es el que realizó la acción.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>software espía</p></td>
<td style="border:1px solid black;"><p>Software que puede mostrar anuncios (como anuncios emergentes), recopilar información sobre el usuario o incluso cambiar la configuración del equipo, generalmente sin obtener antes su consentimiento.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>contraseña segura</p></td>
<td style="border:1px solid black;"><p>Contraseña que ofrece una defensa efectiva frente al acceso no autorizado a un recurso. Una contraseña segura tiene al menos 6 caracteres de longitud, no contiene ni la totalidad ni parte del nombre de la cuenta de usuario y contiene al menos tres de las cuatro categorías siguientes de caracteres: letras mayúsculas, letras minúsculas, dígitos en base 10 y símbolos del teclado como !, @ y #.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>caballo de Troya</p></td>
<td style="border:1px solid black;"><p>Programa que parece ser útil o inofensivo, pero que contiene código oculto diseñado para explotar o dañar el equipo en el que se ejecuta. Los programas de caballos de Troya suelen llegar a los usuarios mediante mensajes de correo electrónico que engañan sobre la función y objetivo del programa. También se denominan código troyano.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>actualización</p></td>
<td style="border:1px solid black;"><p>Paquete de software que sustituye a una versión instalada por una más reciente del mismo software. El proceso de actualización suele dejar intactos los datos y preferencias existentes del cliente y sólo sustituye el software existente por el de una versión más actual.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Id. del usuario</p></td>
<td style="border:1px solid black;"><p>Nombre único con el que un usuario puede iniciar sesión en un equipo.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>virus</p></td>
<td style="border:1px solid black;"><p>Código escrito con la intención específica de autorreplicarse. Un virus intenta propagarse de un equipo a otro adjuntándose a un programa del host. Puede dañar el hardware, el software o los datos. Similar a un gusano. Consulte también la definición proporcionada por Virus Info Alliance (f-secure.com).</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>vulnerabilidad</p></td>
<td style="border:1px solid black;"><p>Cualquier debilidad, proceso o acto administrativo o exposición física que hace que un equipo pueda ser objeto de una amenaza.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>gusano</p></td>
<td style="border:1px solid black;"><p>Código malintencionado que se autopropaga y que puede distribuirse automáticamente de un equipo a otro sin conexiones de red. Un gusano puede realizar una acción dañina, por ejemplo, usar recursos del sistema local o de la red, lo que probablemente provoque un ataque de denegación de servicio. Similar a un virus.</p></td>
</tr>  
</tbody>  
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtener el artículo Cómo proteger la información confidencial de las amenazas de la ingeniería social](http://go.microsoft.com/fwlink/?linkid=71053)
  
[](#mainsection)[Principio de la página](#mainsection)
