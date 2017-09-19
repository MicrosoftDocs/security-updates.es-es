---
TOCTitle: Métodos de la mediana empresa para combatir el correo no deseado en un entorno de Exchange Server
Title: Métodos de la mediana empresa para combatir el correo no deseado en un entorno de Exchange Server
ms:assetid: '3eed9be9-ffd4-4138-9384-d8d849ad979c'
ms:contentKeyID: 20200227
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc875815(v=TechNet.10)'
---

Métodos para combatir el correo no deseado en un entorno de Exchange Server
===========================================================================

Publicado: 18/08/2006

##### En esta página

[](#efaa)[Introducción](#efaa)
[](#eeaa)[Definición](#eeaa)
[](#edaa)[Desafíos](#edaa)
[](#ecaa)[Soluciones](#ecaa)
[](#ebaa)[Resumen](#ebaa)
[](#eaaa)[Referencias](#eaaa)

### Introducción

Bienvenido a este documento de la colección de Guías de seguridad para medianas empresas. Microsoft espera que la siguiente información le ayude a crear un entorno informático más seguro y productivo.

#### Resumen ejecutivo

Los mensajes de correo electrónico no solicitados, conocidos también como correo electrónico no deseado o spam, son mensajes enviados desde una sola fuente con la intención de difundirse a muchos buzones a la vez. El objetivo de los remitentes de correo no deseado es enviar el mensaje al usuario final para que lo abra y lo lea, ya que es así como el remitente de correo no deseado gana dinero. Existen, sin duda, muchas técnicas que los remitentes de correo no deseado usan para colocar los mensajes en áreas ocultas, donde no pueden ser detectados fácilmente en el nivel de puerta de enlace.

El sector estima que el 40% o más de los mensajes entrantes de correo electrónico se pueden designar como correo electrónico no deseado. Este aumento de correo electrónico no deseado o spam continúa siendo un reto para las medianas empresas. No sólo es un incordio, sino que puede ser una propuesta cara cuando se produce una pérdida de productividad potencial y se requieren recursos adicionales para afrontar este problema.

Por tanto, es necesaria una solución práctica en el desarrollo de métodos para combatirlo.

Microsoft® Exchange Server 2003 con Service Pack 2 (SP2) presenta un marco que combina métodos diferentes para combatir el correo no deseado en uno o varios entornos de Exchange Server. Este marco se denomina marco contra correo no deseado de Exchange Server 2003 y está formado por un filtrado a nivel de conexión, de protocolo y de contenido.

Los métodos de este marco permiten tanto a los administradores como los usuarios finales filtrar y clasificar de un modo preciso el correo no deseado, así como decidir si se trata de correo no deseado o es correo electrónico de empresa legítimo.

El objetivo principal de este marco es proporcionar a los administradores y usuarios soluciones que sean lo suficientemente flexibles para aplicarlas en el servidor y en el cliente. En este documento se describen detalladamente estos métodos y se demuestra cómo se comporta cada método dentro del marco y cómo funcionan colectivamente. Presenta planes de desarrollo y de evaluación, así como también una guía detallada en la sección Implementación y administración.

**Nota**   Microsoft también proporciona un importante servicio de ayuda para combatir el correo no deseado. Este servicio se conoce como Exchange Hosted Services o EHS. EHS está compuesto por cuatro servicios diferentes que ayudan a las medianas empresas a protegerse frente al software malintencionado a través del correo electrónico, a satisfacer los requisitos de retención para la conformidad, a cifrar los datos para mantener la confidencialidad y a mantener el acceso al correo electrónico durante y después de las situaciones de emergencia.
La base de Exchange Hosted Services es una red distribuida de centros de datos ubicados en sitios clave a lo largo de la columna vertebral de Internet. Cada centro de datos contiene servidores con tolerancia a errores, cuya carga se equilibra de sitio a sitio y de servidor a servidor.
La descripción detallada de este servicio no es objeto de esta guía. Para obtener más información, consulte el artículo técnico [Información general de Microsoft Exchange Hosted Services](http://www.microsoft.com/exchange/services/services.mspx) en www.microsoft.com/exchange/services/services.mspx (puede estar en inglés).

#### Información general

Este documento consta de cuatro secciones principales donde se describen las opciones y las soluciones con el fin de proporcionar métodos prácticos para combatir el correo no deseado en un entorno de Exchange Server. Las cuatro secciones son: Introducción, Definición, Desafíos y Soluciones.

##### Introducción

Esta sección proporciona un resumen ejecutivo del documento junto con información general de la estructura del mismo, así como información sobre los destinatarios previstos.

##### Definición

Esta sección proporciona algunos detalles sobre la definición y la descripción general del marco contra correo no deseado de Exchange Server 2003. Estos detalles resultarán útiles para comprender las soluciones expuestas en este documento.

##### Desafíos

En esta sección se describen algunos de los desafíos a los que una mediana empresa debe hacer frente cuando determina cómo filtrar el correo no deseado en los distintos niveles que proporciona el marco contra correo no deseado.

##### Soluciones

En esta sección se describen las soluciones prácticas para afrontar los desafíos que supone el correo electrónico no solicitado. Se valoran los métodos y los planes de desarrollo para afrontar los desafíos, junto con información detallada sobre la administración e implementación de los métodos siguientes:

-   Protección a nivel de conexión

    -   Filtrado de conexiones IP

    -   Listas de bloqueo en tiempo real

-   Protección a nivel de protocolo

    -   Bloqueo de destinatarios y remitentes

    -   Sender ID

-   Protección a nivel de contenido

    -   Filtro inteligente de mensajes de Exchange

    -   Correo electrónico no deseado de Outlook 2003 y Outlook Web Access

Además del marco contra correo no deseado de Exchange Server 2003, es importante reconocer que la concienciación del usuario es una parte fundamental para combatir el correo no deseado en los entornos de Exchange Server. Este tema se tratará al final de la sección "Implementación y administración".

#### Quién debería leer esta guía

Este documento va dirigido principalmente a profesionales de tecnologías de la información (TI) y de administración empresarial responsables de los métodos de planeamiento e implementación para combatir el correo no deseado dentro del entorno de Exchange Server de las medianas empresas. Tales profesionales pueden desempeñar las funciones siguientes:

-   **Diseñadores de sistemas**. Son los responsables del diseño de la infraestructura del servidor general, desarrollan las directivas y estrategias de implementación del servidor, el sistema de protección y colaboran con el diseño de conectividad de la red.

-   **Directivos de tecnologías de la información**. Son los responsables de la toma de decisiones técnicas y los administradores del personal de tecnologías de la información responsable de la infraestructura, de la implementación del servidor y escritorio, y de la administración del servidor Exchange y de las operaciones entre los sitios.

-   **Administradores de sistemas**. Son los responsables del planeamiento y de la implementación de tecnología entre los servidores de Exchange de Microsoft, así como de la evaluación y recomendación de las nuevas soluciones tecnológicas.

-   **Administradores de mensajería de Exchange**. Son los responsables de la implementación y de la administración de la mensajería de la organización.

[](#mainsection)[Principio de la página](#mainsection)

### Definición

El marco contra correo no deseado de Exchange Server 2003 es un mecanismo para combatir el correo no deseado dentro del entorno de Exchange Server. La versión Exchange Server 2003 SP2 mejora el marco al incluir la tecnología de autenticación de correo electrónico estándar del sector, denominada filtrado de Sender ID. Esta tecnología contribuye a reducir la cantidad de correo no deseado que se recibe en la bandeja de entrada de un usuario.

En esta sección se describe detalladamente el marco contra correo no deseado de Exchange Server 2003.

#### Marco contra correo no deseado de Exchange Server 2003

Exchange Server 2003 aplica una protección contra el correo no deseado en tres niveles distintos: el nivel de conexión, el nivel de protocolo y el nivel de contenido, como se muestra en la siguiente figura.

![](images/Cc875815.AFSESE01(es-es,TechNet.10).gif)

**Figura 1. Tres niveles de protección contra el correo no deseado**

La protección a nivel de conexión analiza el host SMTP de conexión, la protección a nivel de protocolo analiza a los destinatarios y remitentes del mensaje, mientras que la protección a nivel de contenido evalúa el contenido del mensaje. Cada uno de estos tipos de protección contra el correo no deseado se describen con más detalle en las subsecciones siguientes.

##### Protección a nivel de conexión

La protección a nivel de conexión se encuentra entre los niveles más beneficiosos de defensa contra el correo no deseado, ya que con este nivel de protección, el mensaje de correo no deseado nunca llega a la mediana empresa. Como se muestra en la siguiente figura, la protección a nivel de conexión funciona mediante la evaluación de cada conexión SMTP entrante por si se tratara de un origen de correo no deseado.

[![](images/Cc875815.AFSESE02(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese02_big(es-es,technet.10).gif)

**Figura 2. Protección a nivel de conexión**

Si el host SMTP de conexión se identifica como un host que envía correo no deseado o como uno que normalmente no envía mensajes SMTP, la conexión puede ser rechazada; así se eliminan los costosos ciclos empleados para determinar si el mensaje entrante es un correo no deseado. Para este fin, existen dos tipos de filtrado a nivel de conexión disponibles con Exchange Server 2003.

###### Filtrado de conexiones IP

Con Exchange Server 2003, puede elegir explícitamente denegar las conexiones SMTP basadas en direcciones IP. Este método es uno de los métodos más rudimentarios para proteger un servidor Exchange, ya que las listas de filtrado de conexión se administran de forma manual. Si desea denegar las conexiones SMTP entrantes de un host específico por algún motivo conocido (al incluir la posibilidad de que sea un origen de correo no deseado), las conexiones se deniegan en este nivel.

Se pueden permitir las conexiones SMTP de forma explícita. Si desea recibir correo de un host SMTP bloqueado e identificado como un origen de correo no deseado, puede elegir que se permitan los mensajes de un host SMTP específico que, de otra manera, hubiera sido denegado.

###### Listas de bloqueo en tiempo real

Un medio más dinámico que proporcione protección a nivel de conexión se consigue con el uso de listas de bloqueo en tiempo real. Las listas de bloqueo son listas de direcciones IP que son orígenes conocidos de correo no deseado, retransmisiones abiertas o parte del ámbito de la dirección IP que no debería incluir un host SMTP como, por ejemplo, una dirección IP de agrupaciones de acceso telefónico MSN® de Microsoft.

Los proveedores de listas de bloqueo de terceros recopilan direcciones IP que se adaptan cada perfil. Cuando el host de envío inicia una sesión SMTP con un suscriptor del servicio de listas de bloqueo, el suscriptor emite una consulta de tipo Servicio de nombres de dominio (DNS) al proveedor de listas de bloqueo con la dirección IP del host de conexión. El proveedor de listas de bloqueo, a continuación, responde con un código que indica si el host de conexión se encuentra en una lista. El código puede indicar también en qué lista se encuentra el host SMTP de conexión.

El proceso de filtrado de listas de bloqueo en tiempo real se describe y se muestra en la figura siguiente.

1.  Un host SMTP se conecta al servidor Exchange Server 2003 a través del puerto 25 del Protocolo de control de transporte (TCP).

2.  El servidor Exchange Server 2003 consulta al proveedor de listas de bloqueo configurado para comprobar que el host SMTP de conexión no se encuentre en la lista de bloqueo.

3.  Si el host SMTP de conexión no se encuentra en la lista de bloqueo, se permite la conexión. Si el host está en la lista de bloqueo, la conexión se cierra.

[![](images/Cc875815.AFSESE03(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese03_big(es-es,technet.10).gif)

**Figura 3. Cómo funciona el filtrado de listas de bloqueo en tiempo real**

Antes de Exchange Server 2003 SP2, la funcionalidad de filtrado de conexión no estaba disponible si el firewall o los hosts SMTP intermediarios se encontraban entre Exchange y la identidad de envío (Exchange se encuentra detrás de la red perimetral), debido a que el filtrado de conexión, antes de Exchange Server 2003 SP2, sólo se consideraba como el host de conexión. Cuando un host intermediario (como, por ejemplo, un firewall u otro dispositivo SMTP) se encuentra entre el host de envío y Exchange, sólo se considera el host intermediario.

Con el lanzamiento de Exchange Server 2003 SP2, el servidor Exchange se puede ubicar en cualquier lugar de la mediana empresa y aún así filtraría las conexiones correctamente. Esta funcionalidad se consigue al proporcionar listas IP perimetrales y una configuración de rangos IP interna en el Administrador del sistema de Exchange. De ese modo, la funcionalidad de las listas de bloqueo en tiempo real y Sender ID analizarán la dirección IP que se conecte al host SMTP intermediario como, por ejemplo, un firewall.

##### Protección a nivel de protocolo

[![](images/Cc875815.AFSESE04(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese04_big(es-es,technet.10).gif)

**Figura 4. Protección a nivel de protocolo**

Después de que el mensaje SMTP pase la protección a nivel de conexión, el nivel siguiente de defensa es a nivel de protocolo SMTP. La comunicación SMTP entre el host SMTP de envío y el host SMTP de recepción se analiza para comprobar que se permitan los destinatarios y el remitente, y para determinar el nombre de dominio SMTP del remitente.

###### Bloqueo de destinatarios y remitentes

Otra forma de reducir manualmente el correo no deseado es definir los dominios o los remitentes individuales de los que no desea aceptar mensajes. El bloqueo de remitentes le permite especificar los dominios o direcciones SMTP individuales que bloquear. Con Exchange Server 2003, puede impedir también que lleguen mensajes que tengan una dirección de remitente en blanco y archivar mensajes filtrados.

El filtrado de destinatarios le permite filtrar mensajes enviados a un remitente específico. También puede filtrar destinatarios que no se encuentren en la lista del directorio. Sin embargo, al activar el filtrado de destinatarios que no se encuentren en el directorio, puede hacer vulnerable a la compañía frente a un ataque de recopilación de direcciones de correo electrónico SMTP, conocido como Ataque de recopilación de directorios (DHA). En esta situación, el servidor Exchange responde a los comandos *RFC2821 RCPT TO:* que se analizan para buscar direcciones SMTP válidas. El protocolo SMTP reconoce a los destinatarios aceptables durante una sesión SMTP mediante una respuesta *250 2.1.5*. Cuando un correo electrónico se envía a un destinatario no existente, el servidor Exchange devuelve el error *550 5.1.1 Usuario desconocido*. En consecuencia, un remitente de correo no deseado puede crear un programa automatizado que use nombres comunes o términos del diccionario para crear direcciones de correo electrónico para un dominio específico. A continuación, el programa puede recopilar todas las direcciones de correo electrónico que devuelvan *250 2.1.5 a RCPT TO: SMTP* y descartar todas las direcciones de correo electrónico que produzcan los errores *550 5.1.1 Usuario desconocido*. El remitente de correo no deseado puede entonces vender las direcciones de correo electrónico válidas o usarlas como destinatarios de correo no solicitado.

Esta amenaza se puede eliminar mediante el uso de un método conocido como *retraso del tráfico de red (tarpitting)*. Este tipo de característica de SMTP de Microsoft Windows Server™ 2003 SP1 permite al administrador insertar un retraso configurable antes de devolver algunas respuestas de protocolo SMTP. El host atacante no espera a la respuesta lo suficiente.

Para obtener más información, consulte el artículo de Microsoft Knowledge Base [Característica de retraso del tráfico de red (tarpitting) de SMTP para Microsoft Windows Server 2003](http://support.microsoft.com/?kbid=842851) en http://support.microsoft.com/?kbid=842851 (puede estar en inglés).

###### Sender ID

Una de las características más recientes para la defensa frente al correo no deseado de Exchange Server 2003 es el filtrado de Sender ID. Esta característica de Exchange Server 2003 SP2 intenta comprobar que el host SMTP de envío está aprobado para enviar mensajes desde el dominio especificado en la dirección de correo electrónico de envío. Muchos mensajes de correo no deseado son suplantados, para que el mensaje parezca proceder de una dirección de correo electrónico legítima. Mediante el engaño del destinatario para que crea que el correo electrónico es de una persona legítima (representante de banco, de servicio al cliente, etc.), se puede convencer a los usuarios para que faciliten información de valor que podría culminar en un robo de identidad. Sender ID intenta reducir o eliminar los mensajes suplantados.  

Existen dos partes necesarias en Sender ID para que el sistema funcione. La primera parte es un registro DNS conocido como registro de marco de directiva de remitente (SPF). El registro SPF define qué servidores están autorizados a enviar direcciones SMTP para el dominio. No es necesario tener configurado Sender ID para disponer de un registro SPF. La segunda parte es un host SMTP que admite Sender ID como, por ejemplo, Exchange Server 2003 SP2.

El registro SPF se agrega a la zona DNS para que otras organizaciones con Sender ID puedan comprobar que los mensajes que reciben que pretenden ser del dominio se envíen a través de los servidores autorizados en el registro SPF. Los pasos y las figuras siguientes describen cómo funciona el proceso; primero sin un registro SPF y, a continuación, tras aplicar un registro SPF.

1.  Se envía un mensaje al servidor Exchange Server 2003 desde el dominio fabrikam.com del host SMTP de correo no deseado con un Sender ID habilitado. La dirección del remitente es susanaf@nwtraders.com.

2.  El servidor Exchange consulta al DNS el registro SPF de nwtraders.com.

3.  Debido a que nwtraders.com no dispone de un registro SPF, el mensaje pasa a Sender ID.

[![](images/Cc875815.AFSESE05(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese05_big(es-es,technet.10).gif)

**Figura 5. Correo no deseado que entra en una organización sin Sender ID ni registro SPF**

Los comerciantes de Northwind, a continuación, agregan un registro SPF a la zona DNS nwtraders.com de la siguiente manera:

1.  Se envía un mensaje al servidor Exchange Server 2003 desde el dominio fabrikam.com de host SMTP de correo no deseado con un Sender ID habilitado. La dirección del remitente es susanaf@nwtraders.com.

2.  El servidor Exchange consulta al DNS el registro SPF de nwtraders.com.

3.  Debido a que la dirección IP de envío (208.217.184.82) no se encuentra en la lista de direcciones IP autorizadas a enviar correo electrónico de nwtraders.com, como se define en SPF (131.107.76.156), Sender ID actúa sobre el mensaje.

[![](images/Cc875815.AFSESE06(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese06_big(es-es,technet.10).gif)

**Figura 6. Correo no deseado reconocido en una organización con Sender ID o registro SPF**

A través de la implementación de Sender ID, se puede reducir considerablemente el correo no deseado tratado (suplantado) desde los dominios que disponen de un registro SPF. Sin embargo, se debe tener en cuenta que la protección de Sender ID tiene tanta importancia como el número de organizaciones que disponen de registros SPF.

Para Microsoft.com, el filtrado a nivel de protocolo bloquea el 59% de los mensajes entrantes que pasan el filtrado a nivel de conexión.

##### Protección a nivel de contenido

[![](images/Cc875815.AFSESE07(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese07_big(es-es,technet.10).gif)

**Figura 7. Protección a nivel de contenido**

Después de que el filtrado a nivel de conexión y el filtrado a nivel de protocolo se apliquen para determinar si un mensaje entrante es correo no deseado, la siguiente línea de defensa es analizar el contenido del mensaje para buscar pistas comunes que pudieran indicar que se trata de un correo electrónico no solicitado. Los remitentes de correo no deseado realizan esfuerzos constantes para encontrar nuevos e ingeniosos modos de evitar la detección, para que los mensajes consigan pasar los filtros de contenido y lleguen a las bandejas de entrada de los usuarios.

###### Filtro inteligente de mensajes de Exchange

El filtro inteligente de mensajes (FIM) es un filtro de contenido diseñado específicamente para Exchange. Se basa en la tecnología de aprendizaje automático patentada por Microsoft Research, conocida como tecnología SmartScreen® de Microsoft. MSN, Microsoft Hotmail®, Microsoft Office Outlook® 2003 y Exchange usan actualmente SmartScreen. FIM se diseñó para distinguir las características de los mensajes de correo electrónico legítimo y las del correo no deseado, en función de millones de mensajes. FIM valora la probabilidad de que un mensaje de correo electrónico entrante sea un mensaje legítimo o un correo no deseado. A diferencia de muchas otras tecnologías de filtrado, FIM usa características de una muestra estadísticamente segura de mensajes de correo electrónico. Además del correo no deseado, la inclusión de mensajes legítimos en esta muestra reduce la posibilidad de errores. La eficacia de FIM aumenta al reconocer las características de los mensajes legítimos y los de correo no deseado.

FIM se instala en los servidores Exchange que aceptan mensajes SMTP entrantes de Internet. Cuando un usuario externo envía mensajes de correo electrónico a un servidor Exchange que dispone de FIM, éste evalúa el contenido del texto de los mensajes y les asigna a cada mensaje una clasificación según la probabilidad de que el mensaje sea un correo no deseado. Esta clasificación oscila entre 1 y 9 y se almacena como una propiedad de mensaje conocida como clasificación de nivel de confianza contra correo no deseado (SCL). Esta clasificación se mantiene en el mensaje cuando se envía a otros servidores Exchange. El proceso general se muestra en la figura siguiente.

[![](images/Cc875815.AFSESE08(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese08_big(es-es,technet.10).gif)

**Figura 8. Proceso del filtro inteligente de mensajes de Exchange**

Después de que FIM asigne un SCL al mensaje, se evalúa de la siguiente manera, teniendo en cuenta dos umbrales configurados por el administrador:

1.  **Configuración de bloqueo de la puerta de enlace: Bloquear mensajes con una clasificación SCL mayor o igual que**. Si el SCL del mensaje es mayor o igual que el valor establecido en el umbral, se puede realizar una de las siguientes acciones en el mensaje:

    -   Archivar

    -   Eliminar

    -   Ninguna acción

    -   Rechazar

2.  **Configuración de almacenamiento de correo electrónico no deseado: Mueva los mensajes con clasificación SCL mayor que**. Si el mensaje es mayor que el valor establecido en este umbral, el mensaje se recibirá en la carpeta de correo electrónico no deseado de la bandeja de entrada del usuario, a menos que el usuario tenga al remitente en la lista de remitentes seguros.

###### Tecnologías contra la suplantación de identidad (phishing)

La suplantación de identidad (phishing) es un tipo de engaño diseñado para usurpar la identidad del usuario. En las estafas de suplantación de identidad (phishing), los timadores intentan convencer al usuario para que revele datos personales importantes, como los números de las tarjetas de crédito, contraseñas, datos de cuentas u otro tipo de información, con algún falso pretexto (por ejemplo, utilizando un mensaje de correo electrónico en el que se solicita la comprobación de la información de la cuenta).

Exchange Server 2003 SP2 agrega tecnología contra la suplantación de identidad (phishing) a FIM para que se asigne un SCL adecuado a los mensajes de suplantación de identidad (phishing) y se administren en consecuencia.

###### Ponderación personalizada

Exchange Server 2003 SP2 también proporciona una característica de ponderación personalizada que permite a los administradores personalizar el comportamiento de FIM, según las frases que se encuentren en el cuerpo de un mensaje de correo electrónico, en el título o en ambos sitios.

Al insertar un archivo XML (Lenguaje de marcado extensible) denominado MSExchange.UceContentFilter.xml en el mismo directorio que los archivos MSExchange.UceContentFilter.dll y .dat del servidor con FIM instalado, se implementa la característica de ponderación personalizada. Cuando se ejecuta el servidor virtual SMTP y se inicia FIM, el archivo XML se carga.

El archivo XML define frases en las que FIM puede hacer más o menos hincapié. Esta funcionalidad le permite personalizar FIM si se exige a la empresa aceptar o rechazar los mensajes según las frases a las que, de otra manera, FIM les podría dar una clasificación SCL distinta.

Para Microsoft.com, FIM bloquea el 38% de los mensajes entrantes que pasan el filtrado a nivel de conexión y de protocolo.

###### Correo electrónico no deseado de Outlook 2003 y Outlook Web Access

Después de que un mensaje consiga pasar las defensas frente al correo no deseado basadas en servidor, el cliente de Outlook 2003 puede actuar sobre los mensajes que tengan un valor SCL mayor o igual que el valor de configuración de almacenamiento de correo electrónico no deseado en FIM. Los mensajes que sean mayores que este valor de servidor se envían a la carpeta de correo electrónico no deseado en la bandeja de entrada de Outlook 2003.

Outlook 2003 y Outlook Web Access para Exchange Server 2003 también permiten a los usuarios crear una lista de remitentes seguros de los que el usuario aceptaría siempre los mensajes de correo electrónico, así como una lista de remitentes bloqueados de los que el usuario nunca aceptaría los mensajes de correo electrónico. En el almacén del buzón, independientemente de la clasificación SCL asignada al mensaje, Exchange envía todos los mensajes de remitentes seguros a la bandeja de entrada del usuario y todos los mensajes de remitentes bloqueados a la carpeta de correo electrónico no deseado. Sin embargo, si el umbral de puerta de enlace bloquea el mensaje de correo electrónico, éste no se enviará a la bandeja de entrada del usuario debido a que el mensaje nunca se envió al almacén del buzón.

[](#mainsection)[Principio de la página](#mainsection)

### Desafíos

La transmisión de correo electrónico no deseado, conocido con frecuencia como spam, a menudo ofensivo y a veces engañoso, afecta a la capacidad colectiva de usar el correo electrónico como un canal de comunicación y comercio electrónico legítimo.

Para muchos individuos y regiones, el correo no deseado es un problema en el que la bandeja de entrada ya no es un área de almacenamiento de comunicación válida, debido a que el correo electrónico comercial legítimo se pierde en el océano del correo no deseado. Para las medianas empresas, el correo no deseado no hace más que aumentar el coste de la mensajería, en relación con el uso de recursos del servidor, de la red y de discos.

El desafío al que se enfrentan las medianas empresas es cómo permitir mensajes de correo electrónico buenos y cómo bloquear los mensajes de correo electrónico no deseado. Necesitan fórmulas para combatirlos en un entorno de Exchange Server.

Microsoft Exchange Server 2003 con SP2 usa varios métodos de filtrado para reducir el correo no deseado. Estos métodos son las soluciones en varios niveles contra el correo no deseado, que incluyen protección a nivel de conexión, a nivel de protocolo y a nivel de contenido, descritos de manera breve anteriormente. Estos métodos son flexibles. Cuando el mecanismo de cada método queda claro, los administradores de TI y los usuarios pueden ajustar el nivel de protección frente al correo no deseado. Permiten a las medianas empresas equilibrar el acceso de correo electrónico y el filtrado de correo no deseado.

Es importante que los administradores de Exchange y los implementadores entiendan cómo funciona cada uno de estos métodos y cómo lo hacen conjuntamente para reducir el total de correo no deseado que llega a la bandeja de entrada del usuario. La figura siguiente muestra el método de niveles para la defensa contra el correo no deseado.

[![](images/Cc875815.AFSESE09(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese09_big(es-es,technet.10).gif)

**Figura 9. Marco contra correo no deseado de Exchange Server 2003**

[](#mainsection)[Principio de la página](#mainsection)

### Soluciones

En esta sección se describen la evaluación, el desarrollo, la implementación y la administración de las soluciones del marco contra correo no deseado de Exchange Server 2003 para combatir el correo no deseado en el entorno de la mediana empresa.

#### Evaluación

Para combatir el correo no deseado de forma efectiva, tiene que ser evaluada la composición general del sistema de correo electrónico de Exchange Server 2003, incluidas la herramientas disponibles y el uso eficaz que se les va a dar. Se debe realizar un estudio detallado del entorno como parte de la estrategia de la valoración de riesgos.

El marco contra correo no deseado de Exchange Server 2003 es una recopilación de métodos que incluye el filtrado de conexión, de protocolo y de contenido. Las consideraciones acerca del funcionamiento de cada uno de estos métodos y de cómo lo hacen conjuntamente es esencial. Además, la concienciación del usuario sobre estas tecnologías mejorará las probabilidades de una administración e implementación con éxito.

Deben tenerse en cuenta las preguntas siguientes:

1.  ¿Está instalado Exchange Server 2003?

    Para aprovechar los métodos proporcionados por el marco contra correo no deseado de Exchange Server 2003, Exchange Server 2003 debe estar instalado en la plataforma Windows adecuada.

    **Nota**   Microsoft Exchange Server 2003 puede instalarse en Windows 2003 o Windows 2000 con SP3 o posterior. Los requisitos detallados de instalación para Exchange Server no son objeto de esta guía. Consulte el tema [Instalación de los nuevos servidores Exchange 2003](http://www.microsoft.com/technet/prodtechnol/exchange/guides/ex2k3depguide/a3318f57-3536-4e65-9309-9300cda23c73.mspx?mfr=true) en Microsoft TechNet, www.microsoft.com/technet/prodtechnol/exchange/guides/Ex2k3DepGuide/a3318f57-3536-4e65-9309-9300cda23c73.mspx?mfr=true (puede estar en inglés).

2.  ¿Tiene Exchange Server aplicado el Service Pack 2 de Exchange 2003?

    El Service Pack 2 de Exchange Server 2003 es una actualización acumulativa que mejora el entorno de mensajería de Exchange Server 2003 con:

    -   Mejoras de correo electrónico móvil

    -   Avances de buzón

    -   Mejor protección frente al correo no deseado

    SP2 proporciona protección mejorada frente al correo no deseado (descrito anteriormente en este documento) para asegurar un entorno de mensajería confiable y eficaz. Esta protección mejorada incluye:

    -   Un filtro inteligente de mensajes de Exchange integrado y actualizado, basado en la tecnología de filtrado patentada SmartScreen desarrollada por Microsoft Research.

    -   Un nuevo soporte para el protocolo de autenticación de correo electrónico de Sender ID, que ayuda a evitar las estafas de suplantación y la suplantación de identidad (phishing).

3.  ¿Está habilitado el servidor virtual SMTP predeterminado en el Administrador del sistema de Exchange?

    El filtrado de destinatarios, el filtrado inteligente, el filtrado de Sender ID y el filtrado de conexión se establecen en la configuración global y, es también necesario, que estén habilitados en el nivel de SMTP. Por tanto, SMTP tiene que habilitarse antes de aplicar los cambios en estos servicios.

4.  ¿Tienen las estaciones de trabajo cliente instalado Outlook 2003?

    Los servidores se tienen que configurar con todos los requisitos necesarios, pero si un cliente dispone de una versión anterior de Outlook, no podrá disponer de las ventajas de los métodos ofrecidos en el marco contra correo no deseado de Exchange Server 2003.

    Cuando Exchange Server 2003 y sus clientes cumplan todos los requisitos necesarios, se pueden emplear los métodos siguientes:

    -   Protección a nivel de conexión

        Filtrado de conexiones IP

        Listas de bloqueo en tiempo real

    -   Protección a nivel de protocolo

        Bloqueo de destinatarios y remitentes

        Sender ID

    -   Protección a nivel de contenido

        Filtro inteligente de mensajes de Exchange

        Correo electrónico no deseado de Outlook 2003 y Outlook Web Access

#### Desarrollo

La sección de evaluación plantea algunas preguntas y proporciona algunas respuestas acerca de Exchange Server 2003 y los requisitos de cliente para aprovechar el marco contra correo no deseado de Microsoft Exchange Server 2003.

Las soluciones para combatir el correo no deseado en el entorno de Exchange incluyen también la seguridad de los clientes y la formación de los usuarios. Todos estos métodos se deben usar para luchar contra el correo no deseado en un entorno de Exchange.

Cuando se cumplan los siguientes requisitos, todos los métodos de protección frente al correo no deseado que proporciona el marco contra correo no deseado de Microsoft Exchange Server 2003 estarán listos para ser implementados:

-   Que Exchange Server 2003 esté instalado en las plataformas de Windows adecuadas.

-   Que Outlook 2003 y Outlook Web Access estén instalados y configurados.

-   Que todas las revisiones y actualizaciones más recientes recomendadas estén aplicadas, incluido el Service Pack 2.

Una mejor comprensión del funcionamiento de cada método y de qué manera interactúan asegurará una mejor implementación. Aunque se trató de manera breve anteriormente, en esta sección se proporcionan más detalles acerca de estos métodos, necesarios para la implementación y la administración.

##### Protección a nivel de conexión

Exchange Server 2003 SP2 incluye un filtrado de conexión, que compara la dirección IP del servidor de conexión con una lista de direcciones IP denegadas (conocida también como una lista de bloqueo en tiempo real). La comparación de las direcciones IP se produce inmediatamente, cuando se inicia la sesión SMTP, lo que permite a la mediana empresa bloquear las conexiones de las puertas de enlace en los primeros niveles de envío de mensajes. Antes de que un servidor que está en la lista de bloqueo en tiempo real pueda enviar los mensajes, la conexión se cierra. Este método provoca un ahorro de rendimiento tanto de los niveles de mensajería como de red.

Las medianas empresas pueden establecer un filtrado de conexión en Exchange Server 2003 SP2 manualmente, al crear una lista de denegación global y una lista de aceptación global, o al usar bases de datos mantenidas por terceros de direcciones IP conocidas bloqueadas.

La mayoría de servidores Exchange Server 2003 SP2 se implementan detrás del perímetro de la organización y no directamente en Internet. Esta ubicación hace que el filtrado de conexión sea menos eficaz, debido a que la característica se basa en la obtención de la dirección IP del remitente original para ejecutar la consulta DNS. La versión de SP2 corrige esta deficiencia al incluir un nuevo algoritmo de análisis de encabezado para originar una recuperación de direcciones IP. Exchange Server 2003 SP2 con filtrado de conexión implementado se puede ubicar en cualquier lugar de la organización y realizar el filtrado como si estuviera en el perímetro.

###### Filtrado de conexiones IP

Una mediana empresa puede crear una lista estática propia de las direcciones IP denegadas. Como su propio nombre indica, la lista de denegación global contiene ciertas redes y direcciones IP de las que una organización nunca desearía aceptar un correo electrónico. Por otro lado, una mediana empresa puede crear una lista de aceptación global, es decir, una lista de redes y direcciones IP a las que una organización no desearía aplicar un bloqueo de correo electrónico o de directivas de filtrado. La lista de aceptación global puede incluir direcciones IP que se correspondan con empresas subsidiarias o socios comerciales con los que la mediana empresa tiene relaciones de confianza. En estas circunstancias, la mediana empresa no desea arriesgarse a tener falsos positivos, por lo que agrega las direcciones IP de confianza de los servidores de correo electrónico del remitente a la lista de aceptación global.

###### Listas de bloqueo en tiempo real

Una lista de bloqueo en tiempo real es una base de datos basada en DNS de direcciones IP de orígenes de correo no deseado conocidos y comprobados. Las listas de bloqueo en tiempo real están disponibles en las compañías que se dedican a supervisar continuamente Internet y a localizar los orígenes conocidos del correo no deseado. Cuando se detectan, las direcciones IP con formato incorrecto se agregan a una base de datos de lista de bloqueo en tiempo real. Estas listas a menudo están disponibles de forma gratuita o por una cuota si el administrador de mensajería desea servicios ampliados.

Exchange Server 2003 SP2 permite el uso de listas de bloqueo en tiempo real de terceros. Al configurar el uso de las listas de bloqueo en tiempo real de terceros, el servidor Exchange Server 2003 SP2 comprueba la dirección IP del servidor de envío con la base de datos de listas de bloqueo en tiempo real y deniega la conexión si encuentra una coincidencia.

Dado que la funcionalidad de la lista de bloqueo en tiempo real se basa en las decisiones de filtrado de la dirección IP del servidor de envío en vez de en el contenido del mensaje, las listas de bloqueo en tiempo real se clasifican técnicamente en una categoría independiente a las del software contra correo no deseado de terceros. La lista de bloqueo en tiempo real actúa como un equipo selector (gatekeeper), con lo que evita que entren al entorno los mensajes de servidores dudosos o malintencionados conocidos. Un mensaje que pasa la lista de bloqueo en tiempo real está un paso más cerca de entrar en la red, pero sólo hasta que el nivel siguiente de defensa de mensajería como, por ejemplo, el filtro inteligente de mensajes, examine el contenido del mensaje.

Debido al volumen de consultas DNS relacionadas con la lista de bloqueo en tiempo real que Microsoft IT realiza diariamente (decenas de millones), Microsoft IT transfiere una copia gemela de las listas de bloqueo en tiempo real a los servidores DNS de forma regular y predeterminada (generalmente varias veces al día). La mayoría de los proveedores de listas necesitan copias locales de las listas de bloqueo en tiempo real para volúmenes de consulta mayores a 250.000 al día. La transferencia de una copia de la lista de bloqueo en tiempo real se conoce como transferencia de zona desde el proveedor de listas. Microsoft IT configura las puertas de enlace de Exchange Server 2003 SP2 para crear consultas DNS relacionadas con la listas de bloqueo en tiempo real contra esos servidores DNS locales.

##### Protección a nivel de protocolo

Después de que el mensaje SMTP pase la protección a nivel de conexión, el nivel siguiente de defensa es a nivel de protocolo SMTP. La comunicación SMTP entre el host SMTP de envío y el host SMTP de recepción se analiza para comprobar que se permitan los destinatarios y el remitente, y para determinar el nombre de dominio SMTP del remitente.

###### Bloqueo de destinatarios y remitentes

Las características de filtrado de destinatarios de Exchange Server 2003 SP2 permiten a las medianas empresas protegerse o reducir el impacto del bombardeo de correo. A menudo, los destinatarios a los que se dirigen tales ataques no necesitan en absoluto recibir mensajes desde Internet. El filtrado de destinatarios rechaza los mensajes en los niveles de puerta de enlace según criterios como, por ejemplo, a quién se envía el mensaje.

Aunque el filtrado de destinatarios no es tan efectivo en la lucha contra las amenazas de correo no deseado en tiempo real como las soluciones contra correo no deseado en tiempo real, el filtrado de destinatarios puede ser extremadamente útil a la hora de disminuir los riesgos de ataques de bombardeo de correo. Recientemente, el uso de filtrado de destinatarios permite a Microsoft IT bloquear millones de mensajes dirigidos a unos cuantos destinatarios en un solo día.

###### Sender ID

El marco de Sender ID es un protocolo de tecnología de autenticación de correo electrónico que ayuda a solucionar el problema de la suplantación de identidad (spoofing o phishing) mediante la comprobación del nombre de dominio desde el que se envía el correo electrónico. Sender ID valida el origen del correo electrónico mediante la comprobación de la dirección IP del remitente con respecto al supuesto propietario del dominio remitente.

El objetivo de Sender ID es comprobar que cada mensaje de correo electrónico se origina en un dominio de Internet desde donde supuestamente dice enviarse. Esta comprobación se consigue con la comprobación de la dirección del servidor que envía el correo electrónico con una lista registrada de servidores que el propietario del dominio autorizó para enviar el correo electrónico. El proveedor de servicios de Internet (ISP) o el servidor de correo del destinatario realizan automáticamente esta comprobación antes de que el mensaje de correo electrónico se envíe al usuario. El resultado de la comprobación de Sender ID se puede usar como entrada adicional en las tareas de filtrado que el servidor de correo ya realizó. Cuando el remitente se autentica, el servidor de correo puede tener en cuenta los comportamientos anteriores, los patrones de tráfico y la reputación del remitente, así como aplicar filtros de contenido convencionales al determinar si entrega un correo al destinatario.

##### Protección a nivel de contenido

Lo ideal sería que el correo no deseado no llegara nunca al nivel de cliente. La realidad es que algunos mensajes de correo no deseado llegan a los equipos de escritorio de los usuarios. Uno de los principales motivos es que algunos mensajes de correo electrónico legítimos como, por ejemplo, los boletines, contienen a menudo características de correo no deseado y, en consecuencia, no es correcto establecer el umbral de filtrado tan bajo como para que todos los mensajes sospechosos se eliminen. Además, los usuarios pueden tener preferencias individuales a las que una única configuración de ámbito empresarial no pueda responder.

###### Filtro inteligente de mensajes de Exchange

El filtro inicial por donde tiene que pasar el correo electrónico entrante de Internet es el filtro inteligente de mensajes, que se ejecuta en los servidores de puerta de enlace de Exchange Server 2003 SP2 en el extremo del entorno de mensajería. El filtro inteligente de mensajes usa SCL, PCL (del inglés Phishing Confidence Level, que es uno de los factores que activan las asignaciones SCL finales) y el marco de Sender ID integrado en Exchange Server 2003 SP2. El filtro de mensajes de Internet clasifica algunas partes del mensaje, realiza análisis de mensajes basados en la heurística, y asigna una clasificación SCL del 0 al 9 a cada mensaje explorado. Cuanto más alta sea la clasificación, mayor será la probabilidad de que el mensaje sea correo no deseado.

Exchange Server 2003 SP2 incluye las actualizaciones y datos más recientes en el filtro inteligente de mensajes. Las mejoras en las actualizaciones quincenales y en FIM aseguran una concentración continuada en identificar el correo no deseado y en reducir los falsos positivos. Estas mejoras incluyen nuevas posibilidades para combatir el correo no deseado, como el bloqueo de prácticas de suplantación de identidad (phishing). Las prácticas de suplantación de identidad (phishing) intentan, a través del engaño, conseguir de forma fraudulenta información personal confidencial al hacerse pasar por sitios web legítimos.

El entorno de Exchange Server 2003 SP2 puede configurarse para realizar acciones de filtrado en los mensajes con clasificaciones SCL mayores que los umbrales configurados por los administradores. El filtro inteligente de mensajes usa dos umbrales que se establecen en Exchange Server 2003 SP2: el umbral de puerta de enlace y el de almacenamiento.

###### Correo electrónico no deseado de Outlook 2003 y Outlook Web Access

-   **Filtro de correo electrónico no deseado**. Outlook 2003 usa tecnología de vanguardia desarrollada por Microsoft Research para evaluar si se debe tratar un mensaje como correo electrónico no deseado según una serie de factores como, por ejemplo, la hora en la que se envió el mensaje y el contenido y estructura del mismo. El filtro no identifica ningún remitente en particular ni ningún tipo de mensaje de correo electrónico. En su lugar, usa análisis avanzados para determinar la probabilidad que tiene de que el destinatario lo identifique como un mensaje de correo electrónico no deseado.

    De forma predeterminada, este filtro se establece en una configuración baja diseñada para detectar los mensajes de correo electrónico no deseado más obvios. Los mensajes detectados por el filtro se trasladan a una carpeta de correo electrónico no deseado especial para su acceso posterior. Si lo desea, puede hacer que el filtro sea más estricto (quizás detecte por error más mensajes legítimos) o incluso establecer que Outlook 2003 elimine permanentemente los mensajes de correo electrónico no deseado en cuanto entren. Obtenga más información acerca del Filtro de correo electrónico no deseado.

-   **Listas de remitentes seguros**. Si el filtro marca por error un mensaje de correo electrónico como mensaje de correo electrónico no deseado, puede agregar sin dificultad el remitente de ese mensaje a la lista de remitentes seguros. Las direcciones de correo electrónico y los nombres de dominio de la lista de remitentes seguros nunca se tratarán como mensajes de correo electrónico no deseado, independientemente del contenido del mensaje. Los contactos son de confianza de forma predeterminada y los mensajes procedentes de estos nunca se tratarán como mensajes de correo electrónico no deseado. Cuando la empresa use Microsoft Exchange Server, los mensajes internos de la organización no se tratarán nunca como mensajes de correo electrónico no deseado. Outlook 2003 se puede configurar para que acepte solamente los mensajes de la lista de remitentes seguros, lo que le otorga un control absoluto de los mensajes que recibe.

-   **Lista de remitentes bloqueados**. Los mensajes de correo electrónico de ciertas direcciones de correo electrónico o nombres de dominio se pueden bloquear fácilmente al agregar los remitentes a la lista de remitentes bloqueados. Los mensajes de los nombres de persona o de dominio que aparezcan en la lista de remitentes bloqueados se tratarán siempre como mensajes de correo electrónico no deseado, independientemente del contenido del mensaje.

-   **Lista de destinatarios seguros**. Se puede agregar un grupo o una lista de correo electrónico de la que sea miembro a su lista de destinatarios seguros. Cualquier mensaje que envíe a las direcciones de correo electrónico o a los nombres de dominio de esta lista no se tratará como mensaje de correo electrónico no deseado, independientemente del remitente o el contenido del mensaje.

-   **Actualización automática**. Se puede actualizar el filtro de correo electrónico no deseado con actualizaciones periódicas de Microsoft, para que disponga de los métodos más recientes de bloqueo de mensajes no deseados. Microsoft se compromete a proporcionar actualizaciones periódicas del filtro de correo electrónico no deseado.

#### Implementación y administración

La capacidad de comprender el funcionamiento de cada uno de estos métodos en este marco y cómo funcionan estos métodos juntos es el principal objetivo del marco contra correo no deseado de Exchange Server 2003. Cuando se entienda el ámbito de este marco, la administración e implementación adecuadas de estas tecnologías permitirán que las medianas empresas combatan de forma eficaz contra el correo no deseado en los entornos Microsoft Exchange Server. Para ayudar a combatir el correo no deseado, los usuarios deben adquirir un conocimiento básico sobre la materia para poder administrar los equipos cliente en sus entornos. Además, la supervisión y la solución de problemas de filtrado inteligente de mensajes se tratarán como parte de la administración constante.

Las siguientes características tienen que configurarse en ambos niveles: de configuración global y SMTP. La concienciación del usuario se explica al final de la sección.

En esta sección se explican los procedimientos paso a paso para:

-   Protección a nivel de conexión

    -   Filtrado de conexiones IP

    -   Listas de bloqueo en tiempo real

-   Protección a nivel de protocolo

    -   Bloqueo de destinatarios y remitentes

    -   Sender ID

-   Protección a nivel de contenido

    -   Filtro inteligente de mensajes de Exchange

    -   Correo electrónico no deseado de Outlook 2003 y Outlook Web Access

##### Protección a nivel de conexión

Exchange Server 2003 admite el *filtrado de conexión* basado en las listas de bloqueo en tiempo real. Esta característica comprueba una dirección de Protocolo Internet (IP) entrante con respecto al proveedor de listas de bloqueo en tiempo real (RBL) de las categorías que se desea filtrar. Si se detecta una coincidencia en la lista de proveedores RBL, SMTP emite un error *550 5.x.x* en respuesta al comando *RCPT TO* y la respuesta de error personalizada se envía al remitente. Se pueden usar varios filtros de conexión y establecer prioridades en el orden de aplicación de cada filtro.

Cuando se crea un filtro de conexión, se establece una regla que SMTP usa para realizar una búsqueda DNS en la lista proporcionada por el servicio RBL de terceros. El filtro de conexión hace coincidir cada dirección IP entrante con la lista de bloqueo proporcionada por el tercero. El proveedor RBL emite una de las dos respuestas:

-   **Host no encontrado**. Esta respuesta indica que la dirección IP no se encuentra en la lista de bloqueo.

-   **127.0.0.x**. Esta respuesta es un código de estado de respuesta que indica que se encontró una coincidencia de la dirección IP en la lista de infractores. La variable x depende del proveedor.

Si se encuentra la dirección IP entrante en la lista, SMTP devuelve un error *5.x.x* en respuesta al comando *RCPT TO* (comando SMTP que emite el servidor de conexión para identificar al destinatario previsto del mensaje).

###### Proveedores de listas de bloqueo en tiempo real

Debido a que distintos proveedores de listas de bloqueo en tiempo real ofrecen diferentes tipos de listas y servicios, las medianas empresas tiene que estudiar detenidamente varios proveedores antes de seleccionar uno. Dos proveedores conocidos son [Spam Haus](http://www.spamhaus.org/) en www.spamhaus.org y [Spam Cop](http://www.spamcop.net/) en www.spamcop.net.

Las respuestas a las siguientes preguntas pueden ayudar a elegir un proveedor de RBL.

-   **Calidad de la lista**. ¿Alguien comprueba si una dirección IP agregada a la lista es en realidad un remitente de correo no deseado? ¿Cualquiera puede agregar direcciones a la lista?

-   **Seguridad de la lista**. ¿La lista pasa por alguna comprobación de seguridad? ¿Alguien comprueba que no se hayan agregado direcciones IP de forma malintencionada o equivocada?

-   **Proceso para la actualización de la lista**. ¿Qué es el proceso de revisión? Si la inclusión en la lista se realiza de forma automatizada, la eliminación de la lista se debe realizar también de forma automatizada después de que se detenga el envío de correo no deseado. ¿Cuánto tiempo tarda en actualizarse la lista?

-   **Proceso de transferencia de listas**. ¿Permite el proveedor transferencias de tipo BIND (del inglés Berkeley Internet Name Domain) completas o incrementales que sean directamente compatibles con DNS de Windows?

-   **Soporte técnico del proveedor de listas de bloqueo**. ¿Qué nivel de soporte técnico ofrece el proveedor?

###### Filtrado de conexiones IP

**Para configurar el filtrado de conexiones IP**

1.  En el Administrador del sistema de Exchange, expanda el contenedor **Configuración global** .

2.  Haga clic con el botón secundario en **Entrega de mensajes** y, a continuación, en **Propiedades**.

3.  Haga clic en la ficha **Filtrar conexión**.

4.  Decida si va a **Aceptar**, **Denegar** o a hacer una **Excepción**. Denegar está seleccionado en el ejemplo siguiente.

5.  Se puede seleccionar tanto una **Dirección IP única** como un **Grupo de direcciones IP**, como se muestra en la captura de pantalla siguiente.

    [![](images/Cc875815.AFSESE10(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese10_big(es-es,technet.10).gif)

###### Listas de bloqueo en tiempo real (RBL)

**Para configurar la funcionalidad de listas de bloqueo en tiempo real en el nivel de configuración global**

1.  En el Administrador del sistema de Exchange, expanda el contenedor **Configuración global** .

2.  Haga clic con el botón secundario en el objeto **Entrega de mensajes** y elija **Propiedades**.

3.  Haga clic en la ficha **Filtrar conexión**.

4.  Para crear una regla de filtro de conexión, haga clic en **Agregar** (como se muestra en la captura de pantalla siguiente).

    [![](images/Cc875815.AFSESE11(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese11_big(es-es,technet.10).gif)

5.  En el campo **Nombre para mostrar**, escriba un nombre para el filtro de conexión.

6.  En **Sufijo DNS del proveedor**, escriba el sufijo DNS del proveedor (por ejemplo, contoso.com).

7.  En **Mensaje de error personalizado que se devolverá** se puede escribir un mensaje de error personalizado para devolver al remitente si lo desea. Deje este campo en blanco para usar el mensaje de error predeterminado siguiente:

    *&lt;Nombre de regla de filtro de conexión&gt;* bloqueó *&lt;Dirección IP&gt;*

    Se puede generar un mensaje personalizado mediante el uso de las siguientes variables:

    -   **%0**. Dirección IP de conexión

    -   **%1**. Nombre de regla del filtro de conexión

    -   **%2**. Proveedor RBL

    Por ejemplo, si desea que el mensaje personalizado sea:

    El siguiente proveedor RBL *&lt;nombre del proveedor RBL&gt;* bloqueó la dirección IP *&lt;dirección IP&gt;*.

    tendría que escribir lo siguiente en **Mensaje de error personalizado que se devolverá**:

    El proveedor RBL %2 rechazó la dirección IP %0.

    **Nota**   Exchange reemplazará %0 por la dirección IP de conexión y %2 por el proveedor RBL.

8.  Para configurar qué códigos de estado devuelto recibidos del proveedor RBL desea colocar en este filtro de conexión, haga clic en **Código de estado devuelto**. Aparecerá el siguiente cuadro de diálogo.

    ![](images/Cc875815.AFSESE12(es-es,TechNet.10).gif)

9.  Seleccione una de las opciones siguientes en el cuadro de diálogo **Código de estado devuelto**:

    -   **Hacer coincidir la regla del filtro con cualquier código de retorno**. Esta regla del filtro de conexión coincidirá con cualquier código de estado devuelto recibido del servicio del proveedor. Esta regla establece el valor predeterminado que hace coincidir el filtro de conexión con cualquier estado devuelto.

        Ejemplos:

        **127.0.0.1**. Lista de bloqueo

        **127.0.0.2**. Retransmisión abierta conocida

        **127.0.0.4**. Dirección IP de acceso telefónico

    <!-- -->

    -   **Hacer coincidir la regla del filtro de conexión con la siguiente máscara**. Esta regla del filtro de conexión coincidirá con los códigos de estado devueltos recibidos del proveedor utilizando una máscara para su interpretación. Escriba la máscara que desee filtrar según las máscaras usadas por los proveedores.

        Ejemplos:

        **0000 | 0001**. Lista de bloqueo

        **0000 | 0010**. Retransmisión abierta

        **0000 | 0011**. Retransmisión abierta o lista de bloqueo

        **0000 | 0100**. Host de acceso telefónico

        **0000 | 0101**. Acceso telefónico o lista de bloqueo

        **0000 | 0110**. Acceso telefónico o retransmisión abierta

        **0000 | 0111**. Acceso telefónico, retransmisión abierta o lista de bloqueo

    <!-- -->

    -   **Hacer coincidir la regla del filtro con cualquiera de las respuestas siguientes**. Esta regla del filtro de conexión coincidirá con los códigos de estado devueltos recibidos del proveedor utilizando los valores específicos de los códigos de estado devueltos.

10. Haga clic en **Aceptar**.

Las características de filtrado de conexión, filtrado inteligentes de mensajes, de destinatario y de remitente se deben aplicar también en el nivel SMTP para que funcionen correctamente. Para ello, lleve a cabo los siguientes pasos.

**Para habilitar las características de filtrado en el nivel SMTP**

1.  Inicie el Administrador del sistema de Exchange.

2.  Expanda **Servidores**.

3.  Expanda ***&lt;nombre del servidor&gt;*** (del servidor de correo electrónico que desea configurar).

4.  Expanda **Protocolos**.

5.  Expanda **SMTP**.

6.  Haga clic con el botón secundario en **Servidor virtual SMTP predeterminado** y seleccione **Propiedades**.

7.  En **Propiedades de Servidor virtual SMTP predeterminado**, haga clic en **Avanzadas**.

8.  En **Avanzadas**, haga clic en **Editar**.

9.  En **Identificación**, active la casilla **Aplicar filtro de conexión** para aplicar el filtro que estableció previamente (como se muestra en la captura de pantalla siguiente).

    [![](images/Cc875815.AFSESE13(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese13_big(es-es,technet.10).gif)

#### Protección a nivel de protocolo

Después de que el mensaje SMTP pase la protección a nivel de conexión, el nivel siguiente de defensa es a nivel de protocolo SMTP. La comunicación SMTP entre el host SMTP de envío y el host SMTP de recepción se analiza para comprobar que se permitan los destinatarios y el remitente, y para determinar el nombre de dominio SMTP del remitente.

##### Filtrado de destinatarios

Use la característica de filtrado de destinatarios para evitar la entrega de mensajes que se envían a direcciones de destino particulares.

**Para configurar el filtrado de destinatarios**

1.  Inicie el Administrador del sistema de Exchange.

2.  Expanda el contenedor **Configuración global**.

3.  Haga clic con el botón secundario en **Entrega de mensajes** y seleccione **Propiedades**.

4.  Haga clic en la ficha **Filtro de destinatarios**.

5.  Seleccione **Filtrar los destinatarios que no están en el directorio**.

6.  Haga clic en **Agregar** y, a continuación, agregue la dirección del destinatario (como se muestra en la captura de pantalla siguiente).

    [![](images/Cc875815.AFSESE14(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese14_big(es-es,technet.10).gif)

##### Filtrado de Sender ID

Use las opciones de filtrado de Sender ID para configurar las acciones de Sender ID. Cuando se usan estas opciones, se puede especificar cómo el servidor debe procesar los mensajes que no pasaron la validación de Sender ID. La característica Sender ID es un estándar del sector que puede usar para proporcionar una mayor protección frente a correo electrónico comercial no solicitado (UCE) y prácticas de suplantación de identidad.

De forma predeterminada, el filtrado de Sender ID se establece en **Aceptar**. Sin embargo, puede habilitar el filtro de Sender ID detrás el perímetro de la red. Para realizar esto, especifique las direcciones IP de los servidores de la red interna que desee excluir del filtrado de Sender ID.

**Para configurar el filtrado de Sender ID**

1.  Inicie el Administrador del sistema de Exchange.

2.  Expanda el contenedor **Configuración global**.

3.  Haga clic con el botón secundario en **Entrega de mensajes** y seleccione **Propiedades**.

4.  Haga clic en la ficha **Filtrado de Sender ID**.

5.  Seleccione las opciones de filtrado de Sender ID deseadas (como se muestra en la captura de pantalla siguiente).

    ![](images/Cc875815.AFSESE15(es-es,TechNet.10).gif)

#### Protección a nivel de contenido

El filtrado de contenido de Exchange Server 2003 SP2 se basa en la tecnología de aprendizaje automático SmartScreen de Microsoft Research, que se incorpora en el filtrado inteligente de mensajes (FIM). Los mensajes desde Internet llegan a la puerta de enlace SMTP de Exchange y entran en el marco contra correo no deseado de Exchange Server. Los niveles anteriores de la solución contra correo no deseado de Exchange (filtrado de conexión, remitente y destinatario) bloquean los envíos de mensajes antes de que se reciban los datos reales del mensaje. Si un mensaje pasa con éxito todos esos filtros anteriores, entonces se recibe el cuerpo del mensaje.

El FMI puede realizar una evaluación precisa de la posibilidad que tiene un mensaje entrante de ser un mensaje legítimo o correo no deseado.

##### Filtro inteligente de mensajes de Exchange

El filtro inteligente de mensajes de Exchange es un componente muy importante en la lucha contra el correo no deseado. Es un filtro compatible con SCL que proporciona un filtrado de mensajes de servidor avanzado diseñado específicamente para combatir la entrada de correo no deseado. Para obtener más información, consulte el sitio web [Filtro inteligente de mensajes de Exchange](http://go.microsoft.com/fwlink/?linkid=21607) en http://go.microsoft.com/fwlink/?linkid=21607 (puede estar en inglés).

**Para configurar el filtro inteligente de mensajes de Exchange**

1.  Inicie el Administrador del sistema de Exchange.

2.  Expanda el contenedor **Configuración global**.

3.  Haga clic con el botón secundario en **Entrega de mensajes** y seleccione **Propiedades**.

4.  Haga clic en la ficha **Filtrado inteligente de mensajes**.

5.  En **Bloquear mensajes con una clasificación SCL mayor o igual que** (como se muestra en la captura de pantalla siguiente), seleccione el nivel que desee.

    La escala de nivel oscila entre 0 y 9. Cuanto mayor sea el nivel, mayor posibilidad de que el mensaje sea correo no deseado.

    [![](images/Cc875815.AFSESE16(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese16_big(es-es,technet.10).gif)

##### Correo electrónico no deseado de Outlook 2003 y Outlook Web Access

Tanto Outlook 2003 como Outlook Web Access 2003 incluyen características que pueden ayudar a proteger a los usuarios frente al correo no deseado. Entre estas características, están las siguientes:

-   **Listas seguras y listas de bloqueo mantenidas por el usuario**. Las listas de bloqueo y las listas seguras de Outlook 2003 y Outlook Web Access se almacenan en el buzón del usuario. Debido a que ambos programas cliente usan la misma lista, los usuarios no necesitan mantener las dos versiones.

-   **Bloqueo de contenido externo**. Outlook 2003 y Outlook Web Access 2003 ponen difícil a los remitentes de mensajes de correo electrónico no deseado el uso de señales para recuperar direcciones de correo electrónico. Los mensajes entrantes que contienen cualquier contenido que pueda ser usado como una señal activan la función de Outlook y Outlook Web Access para mostrar un mensaje de advertencia, independientemente si contienen en realidad una señal. Si los usuarios saben que un mensaje es legítimo, pueden hacer clic en el mensaje de advertencia para descargar el contenido. Si los usuarios no están seguros del mensaje, pueden eliminarlo sin activar las señales que avisan a un remitente de que se puede tratar de correo electrónico no deseado.

-   **Administración de correo electrónico no deseado mejorada**. Con Outlook 2003, los usuarios pueden crear reglas para buscar mensajes de correo electrónico por frases específicas, y automáticamente enviar los mensajes que contengan estas frases de la bandeja de entrada a la carpeta especificada (como, por ejemplo, las carpetas de elementos eliminados o de correo no deseado). Los usuarios tienen también la opción de eliminar permanentemente el correo electrónico que se sospecha que es no deseado en vez de enviarlo a la carpeta especificada.

-   **Filtro de correo electrónico no deseado**. Outlook 2003 incluye un filtro de correo electrónico no deseado que busca los atributos comunes del correo no deseado. Estos atributos se actualizan junto con las actualizaciones de Office. Para cada atributo sospechoso, Outlook incrementa el contador un número. Cuanto mayor sea el recuento de un determinado componente de correo, mayor probabilidad hay de que sea correo no deseado. Configure el nivel de protección de correo electrónico no deseado que desee en el cuadro de diálogo **Opciones de correo electrónico no deseado**.

**Para configurar el filtro de correo electrónico no deseado de Outlook 2003**

1.  En Outlook 2003, haga clic en **Acciones** en la barra de menús.

2.  Seleccione **Correo electrónico no deseado** y después **Opciones para el correo no deseado** (como se muestra en la captura de pantalla siguiente).

    [![](images/Cc875815.AFSESE17(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese17_big(es-es,technet.10).gif)

3.  Aparecerá el cuadro de diálogo que se muestra en la captura de pantalla siguiente, que permite al usuario elegir el nivel de protección frente al correo electrónico no deseado que desee.

    [![](images/Cc875815.AFSESE18(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese18_big(es-es,technet.10).gif)

**Para configurar el filtro de correo electrónico no deseado en Outlook Web Access (OWA)**

1.  Inicie una cuenta de Outlook Web Access.

2.  Haga clic en **Opciones**.

3.  Haga clic en **Administrar listas de correo electrónico no deseado**.

4.  Seleccione la característica correspondiente en la opción **Ver o modificar la lista** (como se muestra en la captura de pantalla siguiente).

    [![](images/Cc875815.AFSESE19(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese19_big(es-es,technet.10).gif)

5.  **Agregue**, **edite** o **quite** direcciones de correo electrónico de remitentes.

**Nota**   Cuando los usuarios comienzan por primera vez a usar estas características de correo electrónico no deseado o si modifican las opciones en cualquier momento, deben comprobar periódicamente los mensajes que se han quitado de la bandeja de entrada para asegurarse de que ningún mensaje válido se ha eliminado. Las actualizaciones de las características de correo electrónico no deseado de Outlook 2003 se enumeran en la sección **Office Update** del sitio web de [Microsoft Office Online](http://go.microsoft.com/fwlink/?linkid=24393), en http://go.microsoft.com/fwlink/?LinkId=24393.

#### Supervisión y solución de problemas de filtrado inteligente de mensajes

Los problemas de supervisión y solución de problemas con el filtro inteligente de mensajes de Microsoft Exchange se pueden solucionar mediante el uso del Visor de sucesos y del Monitor del sistema. En esta sección se proporcionará información paso a paso acerca de cómo supervisar y solucionar problemas.

##### Uso del Visor de sucesos

En Visor de sucesos, tanto el registro de aplicación como el registro del sistema contienen errores, advertencias y eventos de carácter informativo relacionados con el funcionamiento de Exchange, el servicio SMTP y otras aplicaciones. Para ayudar a identificar la causa de los problemas del filtro inteligente de mensajes, examine detalladamente los datos que se encuentran en el registro de aplicación y en el del sistema. El filtro inteligente de mensajes graba los eventos para que el Visor de sucesos use el origen de MSExchangeTransport y el protocolo SMTP de la categoría.

**Para encontrar los eventos del filtro inteligente de mensajes mediante el uso del Visor de sucesos**

1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Herramientas administrativas** y, a continuación, haga clic en **Visor de sucesos**.

2.  En el árbol de la consola, haga clic en **Registro de aplicación**.

3.  Para ordenar el registro alfabéticamente y localizar rápidamente una entrada de un servicio de Exchange, haga clic en **Origen** en el panel de detalles (como se muestra en la captura de pantalla siguiente).

    [![](images/Cc875815.AFSESE20(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese20_big(es-es,technet.10).gif)

4.  Para filtrar en el registro las entradas de la lista de eventos registrados para el filtro inteligente de mensajes, haga clic en **Filtro** en el menú **Ver**.

5.  En **Propiedades de Registro de aplicación**, use la lista **Origen del suceso** para seleccionar **MSExchangeTransport**.

6.  En la lista **Categoría**, seleccione **Protocolo SMTP**.

##### Uso de alertas y registros de rendimiento y supervisión de sistemas

El filtro inteligente de mensajes dispone de varios contadores de rendimiento que se pueden usar para visualizar el rendimiento y funcionamiento.

**Para usar Alertas y registros de rendimiento y supervisión de sistemas**

1.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Herramientas administrativas** y, a continuación, haga clic en **Rendimiento**.

2.  Seleccione **Monitor de sistema** y haga clic en el botón **+** para agregar contadores.

3.  En el cuadro de diálogo **Agregar contadores**, en la sección **Objeto de rendimiento**, seleccione **Filtro inteligente de mensajes de MSExchange** (como se muestra en la captura de pantalla siguiente).

    [![](images/Cc875815.AFSESE21(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875815.afsese21_big(es-es,technet.10).gif)

#### Concienciación de usuarios

Como con cualquier otro tema, si va a combatir virus, proteger las estaciones de trabajo de los usuarios no autorizados o combatir el correo no deseado, la tecnología por sí sola no debe ser la única defensa contra amenazas o ataques. Cuando cuentan con los conocimientos necesarios, los usuarios pueden desempeñar una función bastante notable a la hora de ayudar a administrar el correo no deseado. Los usuarios deben recibir la información necesaria acerca de cómo evitar o filtrar el correo electrónico no deseado dentro del entorno de Outlook.

Dicha información debe incluir:  

-   No responder nunca a un correo electrónico que le solicite información personal o financiera.

-   No proporcionar nunca contraseñas.

-   No abrir archivos adjuntos de correo electrónico sospechoso,

-   No responder a ningún correo electrónico no deseado o sospechoso.

-   Configurar las opciones de correo electrónico no deseado en Outlook 2003 como se describe en la sección anterior “Correo electrónico no deseado de Outlook 2003 y Outlook Web Access” en este documento.

[](#mainsection)[Principio de la página](#mainsection)

### Resumen

Muchas medianas empresas basan un número de procesos empresariales fundamentales alrededor de la funcionalidad de Microsoft Exchange Server 2003. Una cantidad considerable de las actividades diarias dependen de los servicios que proporciona Exchange Server.

El aumento del flujo de correo no deseado continúa siendo un desafío para las medianas empresas. No sólo es molesto, sino que el correo no deseado puede dañar las redes y hacer perder tiempo, dinero y otros recursos de personas y empresas de todo el mundo.

En este documento se muestran las formas de reducir el correo no deseado en los entornos de Exchange Server 2003. El marco contra correo no deseado de Exchange Server 2003 combina métodos de protección contra el correo no deseado, lo que proporciona flexibilidad suficiente a los administradores y usuarios finales para ayudarles a disminuir el correo electrónico no deseado y aumentar los niveles de productividad.

[](#mainsection)[Principio de la página](#mainsection)

### Referencias

Puede descargar el documento [Información general del marco contra correo no deseado de Exchange Server 2003](http://download.microsoft.com/download/0/e/6/0e6a7113-dda4-4fd7-aaba-b9e264700225/anti-spam.doc) del centro de descarga de Microsoft en http://download.microsoft.com/download/0/E/6/0E6A7113-DDA4-4FD7-AABA-B9E264700225/Anti-Spam.doc (puede estar en inglés).

El tema sobre [mejor protección frente al correo no deseado](http://www.microsoft.com/exchange/evaluation/sp2/overview.mspx#antispam) del documento de información general de Exchange Server 2003 SP2 está disponible en www.microsoft.com/exchange/evaluation/sp2/overview.mspx\#antispam (puede estar en inglés).

Encontrará información acerca del [filtro inteligente de mensajes de Exchange](http://www.microsoft.com/technet/prodtechnol/exchange/downloads/2003/imf/default.mspx) (FIM) y las actualizaciones de FIM en Microsoft TechNet en www.microsoft.com/technet/prodtechnol/exchange/downloads/2003/imf/default.mspx (puede estar en inglés).

El artículo técnico [Protección de la mensajería en Microsoft: cómo Microsoft IT se defiende contra correo no deseado, virus y ataques de correo electrónico](http://www.microsoft.com/technet/itsolutions/msit/security/messaginghygienewp.mspx) está disponible en Microsoft TechNet en www.microsoft.com/technet/itsolutions/msit/security/messaginghygienewp.mspx (puede estar en inglés).

El artículo "[Listas de bloqueo en tiempo real de Exchange Server 2003](http://www.microsoft.com/technet/prodtechnol/exchange/2003/insider/block_lists.mspx)" está disponible en Microsoft TechNet en www.microsoft.com/technet/prodtechnol/exchange/2003/insider/Block\_Lists.mspx (puede estar en inglés).

El artículo de Microsoft Knowledge Base "[Cómo configurar el filtrado de conexiones para usar listas de bloqueo en tiempo real (RBL) y cómo configurar el filtrado de destinatarios en Exchange 2003](http://support.microsoft.com/default.aspx?scid=823866)" está disponible en http://support.microsoft.com/default.aspx?scid=823866 (puede estar en inglés).

[](#mainsection)[Principio de la página](#mainsection)

**Descargar**

[Obtener el artículo Métodos para combatir el correo no deseado en un entorno de Exchange Server](http://go.microsoft.com/fwlink/?linkid=71052)

[](#mainsection)[Principio de la página](#mainsection)
