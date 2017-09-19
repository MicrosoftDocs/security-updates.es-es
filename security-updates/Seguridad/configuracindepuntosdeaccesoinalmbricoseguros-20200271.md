---
TOCTitle: Configuración de puntos de acceso inalámbrico seguros
Title: Configuración de puntos de acceso inalámbrico seguros
ms:assetid: '57bb98c2-763f-468b-8eac-84910cfcca70'
ms:contentKeyID: 20200271
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc875845(v=TechNet.10)'
---

Configuración de puntos de acceso inalámbrico seguros
=====================================================

##### En esta página

[](#eeaa)[Introducción](#eeaa)
[](#edaa)[Definiciones](#edaa)
[](#ecaa)[Retos](#ecaa)
[](#ebaa)[Soluciones](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Introducción

Este documento forma parte de la colección de guías de seguridad para medianas empresas. Microsoft espera que esta información le ayude a crear un entorno informático más seguro y productivo.

#### Resumen ejecutivo

Las redes de área local inalámbricas (WLAN) constituyen un tema que ha suscitado controversia en el mundo empresarial; en la mayoría de las empresas ya se ha implementado una WLAN de algún tipo o, al menos, se han sopesado las ventajas y los inconvenientes de la tecnología inalámbrica. En cualquier caso, a las empresas que han implementado redes inalámbricas les suele preocupar la seguridad de la solución utilizada, en tanto que a las que han rehuido de la tecnología inalámbrica les inquieta haber podido perder una evidente productividad y un considerable ahorro en infraestructura.

La mayoría de los responsables de tomar decisiones tecnológicas han sentido en el pasado un miedo justificado acerca de la seguridad de la tecnología inalámbrica e, incluso en la actualidad, dicha tecnología lleva el estigma de no haber sido nunca segura, debido a la detección y divulgación de brechas de seguridad en la primera generación de protocolos de seguridad WLAN IEEE 802.11. A pesar de que se han desarrollado muchas soluciones alternativas a lo largo de los años, las soluciones habituales que se han diseñado para abordar los problemas de la seguridad inalámbrica han tenido un coste excesivo o han presentado imperfecciones inherentes.

Desde aquella primera etapa de las redes inalámbricas se han producido numerosos desarrollos y, al igual que la tecnología ha avanzado para admitir velocidades superiores y una mayor confiabilidad, también han evolucionado los estándares empleados para garantizar la seguridad de las transmisiones inalámbricas. Los últimos protocolos de seguridad inalámbrica, WPA y WPA2, basados en el estándar IEEE 802.11i, contribuyen a ofrecer una mayor protección del tráfico inalámbrico incluso en los entornos con una seguridad más rigurosa. Estos estándares actuales, si se configuran correctamente, son mucho más seguros y se pueden utilizar con un elevado nivel de confianza en el entorno de una mediana empresa.

#### Descripción general

Este documento consta de cuatro secciones principales que analizan los detalles necesarios para diseñar e implementar una solución eficaz que garantice la seguridad de la red inalámbrica de una mediana empresa. Estas secciones son las siguientes:

-   **Introducción**. Esta sección presenta un resumen ejecutivo del documento, junto con una descripción general del esquema del documento e información sobre los destinatarios recomendados del mismo.

-   **Definiciones**. Esta sección ofrece información y definiciones útiles para comprender la terminología empleada en el documento.

-   **Retos**. Esta sección describe algunas de las cuestiones comunes a las que se enfrentan las medianas empresas cuando se plantean usar redes inalámbricas y ofrece un marco general de la solución que pretende abordar este documento.

-   **Soluciones**. Esta sección analiza en detalle orientaciones paso a paso específicas que serán útiles para planear, desarrollar e implementar una infraestructura inalámbrica segura y ofrecer compatibilidad con ella. De ahí que la sección de soluciones se divida en tres subsecciones principales:

    -   **Evaluación de la seguridad de las redes WLAN**. Esta sección explica la información necesaria y las posibles opciones para sentar una base sobre la que desarrollar un plan de soluciones.

    -   **Desarrollo de una solución WLAN segura**. Esta sección utiliza la información obtenida en la fase de evaluación anterior para tomar decisiones, crear un plan y desarrollar la base de la solución.

    -   **Implementación y administración**. Esta sección presenta en detalle la solución real paso a paso, junto con información útil para administrar y validar la solución de red inalámbrica segura que se describe en este documento.

#### Quién debería leer este documento

Este documento está destinado al personal técnico, los implementadores de tecnología y los administradores técnicos de medianas empresas que estén planteándose utilizar la solución Acceso protegido Wi-Fi (WPA) o Acceso protegido Wi-Fi 2 (WPA2) para garantizar la seguridad de la infraestructura inalámbrica. En este documento se asume que el lector posee conocimientos técnicos generales sobre dispositivos inalámbricos, conceptos de red básicos, Microsoft® Windows Server™ 2003, Servicio de autenticación Internet (IAS), Servicios de Certificate Server, servicio de directorio de Active Directory®, y configuración y aplicación de la directiva de grupo.

[](#mainsection)[Principio de la página](#mainsection)

### Definiciones

El lector debe comprender y estar familiarizado con los siguientes términos y conceptos que se utilizan en este documento.

**AES**. El Estándar de cifrado avanzado (AES) utiliza una técnica de cifrado simétrico de datos de bloque y forma parte de WPA2.

**EAP**. El Protocolo de autenticación extensible (EAP) es un estándar 802.1X que permite a los programadores transferir datos de autenticación entre los servidores RADIUS y los puntos de acceso inalámbrico. EAP dispone de una serie de variantes, entre las que se incluyen las siguientes: EAP MD5, EAP-TLS, EAP-TTLS, LEAP y PEAP.

**EAP-TLS**. Microsoft desarrolló EAP-Seguridad de la capa de transporte (EAP-TLS) sobre la base del estándar 802.1X para utilizar certificados digitales en el proceso de autenticación. Actualmente, constituye el estándar del sector para la autenticación 802.11i.

**IEEE 802.1X**. El estándar IEEE 802.1X controla el proceso de encapsulación EAP que se produce entre los suplicantes (clientes), los autenticadores (puntos de acceso inalámbrico) y los servidores de autenticación (RADIUS).

**IEEE 802.11**. El estándar IEEE 802.11 controla las comunicaciones de red por aire e incluye varias especificaciones que abarcan desde el estándar 802.11g, que proporciona un tráfico de 20+ Mbps en la banda de 2,4 GHz, y el estándar 802.11i, que controla la autenticación y el cifrado WPA2.

**IEEE 802.11i**. La enmienda IEEE 802.11i al estándar 802.11 especifica los métodos de seguridad (WPA2) que utilizan cifrado de bloque AES para garantizar la seguridad de los procesos de autenticación de origen (EAP) con el fin de solucionar las deficiencias anteriores de las especificaciones y los estándares de seguridad inalámbrica.

**MS-CHAP v2**. El Protocolo de autenticación por desafío mutuo de Microsoft, versión 2 (MS-CHAP v2) es un protocolo de autenticación mutua de desafío-respuesta que se basa en contraseña y utiliza el cifrado MD4 y DES. Se utiliza junto con PEAP (PEAP-MS-CHAP v2) para garantizar la seguridad de las comunicaciones inalámbricas.

**PEAP**. El Protocolo de autenticación extensible protegido (PEAP) es un tipo de comunicación EAP que soluciona problemas de seguridad asociados con transmisiones EAP de texto no cifrado al crear un canal seguro cifrado y protegido mediante TLS.

**SSID**. El Identificador de red SSID es el nombre asignado a una WLAN y que el cliente utiliza para identificar la configuración correcta y las credenciales que se necesitan para tener acceso a una WLAN.

**TKIP**. El Protocolo de integridad de clave temporal (TKIP) forma parte del estándar de cifrado WPA para redes inalámbricas. TKIP es la siguiente generación de WEP, que proporciona una combinación de claves por paquete para solucionar las imperfecciones detectadas en el estándar WEP.

**WEP**. La Privacidad equivalente por cable (WEP) forma parte del estándar IEEE 802.11 y utiliza el cifrado RC4 de 64 o 128 bits. En 2001 se detectaron brechas de seguridad graves en el estándar WEP, principalmente ocasionadas porque la longitud del vector de inicialización del cifrado de secuencias RC4 permitía la descodificación pasiva de la clave RC4.

**WLAN**. Red de área local inalámbrica.

**WPA**. Como respuesta a las deficiencias detectadas en el estándar WEP, en 2003 se presentó la solución Acceso protegido Wi-Fi (WPA) como un subconjunto interoperable de especificaciones de seguridad inalámbrica del estándar IEEE 802.11. Este estándar ofrece funciones de autenticación y utiliza TKIP para el cifrado de datos.

**WPA2**. La Wi-Fi Alliance estableció en septiembre de 2004 el estándar WPA2, que constituye la versión interoperable certificada de la especificación IEEE 802.11i completa ratificada en junio de 2004. Al igual que su predecesor, WPA2 es compatible con la autenticación IEEE 802.1X/EAP o la tecnología PSK, pero incluye un nuevo mecanismo de cifrado avanzado que utiliza CCMP (del inglés Counter-Mode/CBC-MAC Protocol) que se conoce como Estándar de cifrado avanzado (AES).

[](#mainsection)[Principio de la página](#mainsection)

### Retos

Muchas organizaciones son conscientes de las ventajas que supone el uso de la tecnología inalámbrica para mejorar la productividad y la colaboración, pero dudan en implementarla porque les preocupan, de forma justificada, las vulnerabilidades que aparentemente presentan las redes inalámbricas en el entorno de una organización. Confunden aún más la amplia variedad de métodos propuestos que se pueden utilizar para garantizar la seguridad de las comunicaciones inalámbricas y la existencia de informes con posturas divergentes respecto a la eficacia de estas medidas.

La tecnología inalámbrica plantea un buen número de retos a las medianas empresas, no sólo con relación a cómo garantizar la seguridad de la implementación, sino también respecto a si se debe o no implementar. A continuación se indican algunas de las cuestiones más frecuentes relacionadas con las redes inalámbricas que se van a tratar en este documento.

-   Decidir si se debe implementar una WLAN

-   Comprender y mitigar los riesgos de las redes inalámbricas

-   Determinar el modo de hacer seguro un entorno WLAN

-   Seleccionar las opciones de seguridad adecuadas para una red WLAN

-   Validar el nivel de seguridad de una implementación de red inalámbrica

-   Incorporar activos existentes a una solución de seguridad inalámbrica

-   Detectar y prevenir las conexiones malintencionadas de dispositivos inalámbricos

[](#mainsection)[Principio de la página](#mainsection)

### Soluciones

En esta sección se describe el diseño, el desarrollo, la implementación y la compatibilidad de las soluciones inalámbricas seguras que se pueden implementar en los entornos de las medianas empresas. Como se ha mencionado anteriormente, hay muchos interrogantes en torno al uso de la tecnología inalámbrica. Se analizará cada uno de ellos de forma que se pueda sacar provecho, del modo más eficaz y seguro posible, de las ventajas que aporta el uso de las redes inalámbricas.

#### Evaluación de la seguridad de las redes WLAN

Aunque la tecnología inalámbrica ha avanzado hasta el punto de que actualmente ofrece una velocidad y seguridad suficientes para implementarse en una mediana empresa, hay todavía muchos factores que se deben tener en cuenta y diversos métodos para garantizar la seguridad de una red inalámbrica. En esta sección se analizan los métodos más frecuentes que se utilizan para hacer que las redes inalámbricas sean más seguras, se ofrece orientación para determinar cuál es la mejor solución para un determinado entorno y se proponen argumentos a favor y en contra de cada enfoque.

##### Ventajas de las redes inalámbricas

Las ventajas que aporta la implementación de la tecnología WLAN se pueden incluir en una de las dos siguientes categorías: ventajas empresariales y ventajas operativas. Entre las ventajas operativas se incluyen un coste de administración más bajo y una inversión reducida en activos fijos; por otro lado, entre las ventajas empresariales se incluyen una mejora de la productividad, unos procesos empresariales más eficaces y un mayor potencial para crear nuevas funciones empresariales.

###### Ventajas empresariales

La mayoría de las principales ventajas empresariales que se derivan del uso de la tecnología WLAN son fruto de una mayor flexibilidad y movilidad de los empleados. Cuando se utilizan redes inalámbricas, los recursos ya no están atados a una mesa y pueden moverse por la oficina con relativa facilidad. Este tipo de libertad puede generar las siguientes ventajas:

-   Los miembros de los recursos móviles de una empresa, como el personal de ventas, pueden desplazarse sin esfuerzo entre las oficinas o llegar de un lugar y conectarse de forma transparente a la red de la empresa. La conectividad es prácticamente instantánea y se realiza sin tener que buscar un puerto de red ni desenredar cables, con lo que se ahorra mucho tiempo y se reducen las preocupaciones asociadas a las redes cableadas.

-   El personal técnico puede permanecer en contacto constante con los sistemas que administra, independientemente de dónde se encuentre, en el edificio, en una reunión o fuera de su puesto de trabajo. El uso de tecnología portátil, como equipos portátiles, Tablet PC o equipos de mano, permite al personal de TI de una empresa responder al instante a cualquier necesidad.

-   La información siempre se encuentra al alcance de la mano. Las reuniones ya no se retrasarán cuando alguien tenga que hacer copias de un informe o buscar informes en su puesto de trabajo. Las presentaciones se comparten en el equipo en lugar de tener que verlas en una exposición general en la que las imágenes aparecen borrosas y, en las reuniones, se pueden utilizar tecnologías interactivas para colaborar con las oficinas remotas y los teletrabajadores.

-   La flexibilidad organizativa mejora enormemente debido a que los cambios estructurales se pueden implementar rápida y fácilmente, incluso es posible reestructurar oficinas completas porque el cableado de la red ya no supone un problema.

-   La tecnología inalámbrica introduce toda una nueva gama de aplicaciones y soluciones tecnológicas en un entorno empresarial. Dispositivos tales como los asistentes digitales personales (PDA) o los Tablet PC se pueden integrar perfectamente en un entorno de red. Los empleados y las funciones empresariales que anteriormente se encontraban fuera del ámbito de TI ahora pueden beneficiarse de la conectividad de red; los comedores, las salas de conferencias, las salas de hospital, los puntos de venta, los restaurantes e incluso las fábricas pueden lograr una mayor productividad gracias al uso de soluciones tecnológicas de fácil acceso.

###### Ventajas operativas

Las ventajas operativas de la tecnología inalámbrica también son muy variadas y dependen del tipo específico de empresa y de las instalaciones y los servicios empleados. Algunas de estas ventajas incluyen:

-   Los costes de aprovisionamiento de la red son considerablemente reducidos, ya que disminuye la dependencia de las infraestructuras de red cableada. Las áreas en las que la conectividad de red era poco práctica ahora son accesibles de forma económica a través de la tecnología WLAN, incluidas las zonas al aire libre o las zonas de las oficinas distribuidas.

-   La escalabilidad de la red tiene una mayor capacidad de respuesta y es más eficaz con respecto a los niveles variables de demanda, ya que resulta mucho más fácil implementar o mover puntos de acceso inalámbrico a otras ubicaciones que aumentar el número de puertos de red si hay que solucionar un problema de congestión.

-   Se reduce la cantidad de capital destinado a la infraestructura de las instalaciones, porque el equipo de red inalámbrica no es un accesorio fijo tan permanente como la infraestructura del cableado de una red convencional. Esto permite una mayor flexibilidad a la hora de realizar ampliaciones o si, por cualquier motivo, es necesario trasladar la oficina a otra ubicación. Una red inalámbrica de alta velocidad (802.11a/g/n) también constituye una alternativa rentable a reemplazar antiguos sistemas de red cableada Ethernet o Token Ring de baja velocidad.

##### Vulnerabilidades de las redes inalámbricas

Para comprender el nivel de seguridad que ofrecen las distintas soluciones de seguridad disponibles para redes inalámbricas, es importante conocer las amenazas habituales a las que este tipo de redes se pueden enfrentar. Las vulnerabilidades y los perfiles de ataque de las redes tradicionales se conocen muy bien, pero las redes inalámbricas presentan vulnerabilidades que van más allá de los riesgos tradicionales.

**Tabla 1. Amenazas de seguridad habituales de las redes WLAN**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Amenaza</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Divulgación de datos a través de la escucha informática</p></td>
<td style="border:1px solid black;"><p>Los ataques de escucha informática a un tráfico inalámbrico que no es seguro pueden ocasionar una divulgación de datos confidenciales, el descubrimiento de credenciales de usuario e incluso un robo de identidades. Los atacantes sofisticados pueden utilizar información recopilada a través de una escucha informática para organizar ataques a sistemas que, de otro modo, no serían vulnerables.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Interceptación y modificación de datos transmitidos</p></td>
<td style="border:1px solid black;"><p>Un atacante que obtiene acceso a los recursos de una red también puede instalar sistemas malintencionados en ella para interceptar y modificar los datos que se transfieren de un sistema legítimo a otro.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Suplantación de identidad (spoofing)</p></td>
<td style="border:1px solid black;"><p>El acceso a una red interna brinda al atacante la oportunidad de falsificar datos para que parezca que son parte del tráfico legítimo. Tales ataques pueden incluir mensajes de correo electrónico simulados en los que los usuarios internos confiarán más fácilmente que si se tratasen de comunicaciones procedentes de fuentes exteriores, lo que proporciona una plataforma para ataques de ingeniería social y propagación de troyanos.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Denegación de servicio (DoS)</p></td>
<td style="border:1px solid black;"><p>Independientemente del tipo de solución de seguridad que se implemente, una WLAN está excepcionalmente expuesta a ataques por denegación de servicio, tanto intencionados como accidentales. Tales interrupciones pueden tener su origen en algo tan simple como el desbordamiento de la red ante el tráfico indiscriminado generado por un microondas o un conjunto de dispositivos.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Acceso gratuito<br />
(robo de recursos)</p></td>
<td style="border:1px solid black;"><p>Es posible que algunos intrusos sólo deseen obtener acceso gratuito a Internet. Aunque su intención no sea directamente malintencionada o dañina, tales actividades pueden provocar una conectividad de red más lenta para los usuarios legítimos o un vector no administrado para las amenazas de malware.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Amenazas accidentales y conexiones no administradas</p></td>
<td style="border:1px solid black;"><p>En los entornos WLAN no seguros, cualquier visitante puede obtener acceso a la red interna con tan sólo iniciar un dispositivo que pueda tener acceso a redes inalámbricas. Estos dispositivos no administrados pueden haberse puesto ya en peligro o proporcionar a un atacante un punto vulnerable de ataque contra una red.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Puntos de acceso WLAN malintencionados</p></td>
<td style="border:1px solid black;"><p>Aunque una empresa no disponga de una red inalámbrica, puede ser vulnerable a amenazas de seguridad desde redes inalámbricas no administradas. El hardware inalámbrico es relativamente económico, por lo que cualquier empleado puede configurar una red no administrada y desprotegida dentro de un entorno.</p></td>
</tr>  
</tbody>  
</table>
  
Aunque muchos de los riesgos de seguridad asociados a la transmisión de datos por aire son bastante evidentes en el entorno actual preocupado por la seguridad, estas cuestiones no eran tan obvias cuando surgió la primera generación de la tecnología de seguridad inalámbrica. Cuando se creó WEP para garantizar la seguridad de las difusiones inalámbricas de datos, apenas parecía necesario compensar la falta inherente de seguridad, en comparación con la seguridad inherente de la transmisión de datos en las redes cableadas, porque la tecnología era tan reciente que muy pocas personas se habían planteado las posibles amenazas a las que dichas redes podrían tener que hacer frente. Cuando los métodos empleados por los atacantes evolucionaron, se puso de manifiesto que la transmisión de datos por aire atravesaba entornos potencialmente hostiles y que debía protegerse y hacerse tan segura como las comunicaciones LAN cableadas.
  
Cuando se empezaron a conocer públicamente las brechas de seguridad del estándar WEP, el entorno de seguridad de las redes fue cambiando con rapidez. Los casos de hackers de redes inalámbricas se destacaban en los principales medios de comunicación y los gobiernos aplicaban leyes para regular la seguridad de los datos y las identidades en los sectores. A consecuencia de estos sucesos, muchas empresas rechazaron la tecnología inalámbrica por inviable o insegura o bien desarrollaron soluciones complejas como respuesta a las brechas de seguridad inherentes del estándar WEP.
  
Algunas de estas soluciones complejas se siguen utilizando y comercializando en la actualidad. Sin embargo, como se pone de manifiesto en las siguientes secciones, tales soluciones ya no son necesarias para proteger a las redes inalámbricas de dichas amenazas y es posible que se tengan que volver a evaluar porque la tecnología inalámbrica ha evolucionado como respuesta a un panorama de seguridad en constante cambio.
  
##### Selección de la solución de seguridad adecuada para una red WLAN
  
Desde que se conocieron públicamente las debilidades de la primera generación de la tecnología WLAN se ha hecho un gran esfuerzo para solucionar las vulnerabilidades del sistema inalámbrico. Mientras el sector de sistemas inalámbricos, Microsoft y otros proveedores dedicaban sus esfuerzos a mejorar el estándar inalámbrico, otros analistas, proveedores de seguridad de red, etc., encontraron modos de solucionar las debilidades del antiguo estándar inalámbrico. Esta situación ha desembocado en la disponibilidad de una amplia variedad de enfoques para tratar los problemas relacionados con la seguridad inalámbrica.
  
En la siguiente tabla se comparan las principales alternativas, excepto el enfoque más frecuente, que es optar por no implementar la tecnología WLAN.
  
**Tabla 2. Comparación de los enfoques de seguridad para las redes WLAN**

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
<th><p>Característica</p></th>  
<th><p>WPA y WPA2</p></th>  
<th><p>WEP estático</p></th>  
<th><p>VPN</p></th>  
<th><p>IPsec</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Autenticación firme</p>
<p>(véase la nota)</p></td>
<td style="border:1px solid black;"><p>Sí</p></td>
<td style="border:1px solid black;"><p>No</p></td>
<td style="border:1px solid black;"><p>Sí, sólo cuando no se utiliza<br />
Autenticación de clave compartida</p></td>
<td style="border:1px solid black;"><p>Sí, si se utiliza un certificado o la autenticación Kerberos</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Cifrado de datos de alta seguridad</p></td>
<td style="border:1px solid black;"><p>Sí</p></td>
<td style="border:1px solid black;"><p>No</p></td>
<td style="border:1px solid black;"><p>Sí</p></td>
<td style="border:1px solid black;"><p>Sí</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Conexión y reconexión transparente</p></td>
<td style="border:1px solid black;"><p>Sí</p></td>
<td style="border:1px solid black;"><p>Sí</p></td>
<td style="border:1px solid black;"><p>No</p></td>
<td style="border:1px solid black;"><p>Sí</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Autenticación de usuario</p>
<p>(véase la nota)</p></td>
<td style="border:1px solid black;"><p>Sí</p></td>
<td style="border:1px solid black;"><p>No</p></td>
<td style="border:1px solid black;"><p>Sí</p></td>
<td style="border:1px solid black;"><p>No</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Autenticación de equipo</p>
<p>(véase la nota)</p></td>
<td style="border:1px solid black;"><p>Sí</p></td>
<td style="border:1px solid black;"><p>Sí</p></td>
<td style="border:1px solid black;"><p>No</p></td>
<td style="border:1px solid black;"><p>Sí</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Protección del tráfico de difusión y multidifusión</p></td>
<td style="border:1px solid black;"><p>Sí</p></td>
<td style="border:1px solid black;"><p>Sí</p></td>
<td style="border:1px solid black;"><p>Sí</p></td>
<td style="border:1px solid black;"><p>No</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Se necesitan dispositivos de red adicionales</p></td>
<td style="border:1px solid black;"><p>Sí, servidores RADIUS</p></td>
<td style="border:1px solid black;"><p>No</p></td>
<td style="border:1px solid black;"><p>Sí, servidores VPN y RADIUS</p></td>
<td style="border:1px solid black;"><p>No</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Acceso seguro a la WLAN en lugar de solo a los paquetes</p></td>
<td style="border:1px solid black;"><p>Sí</p></td>
<td style="border:1px solid black;"><p>Sí</p></td>
<td style="border:1px solid black;"><p>No</p></td>
<td style="border:1px solid black;"><p>No</p></td>
</tr>  
</tbody>  
</table>
  
**Nota**   Con relación a la autenticación firme, muchas implementaciones VPN que emplean el modo de túnel IPsec utilizan un esquema de autenticación de clave compartida poco seguro denominado XAuth.  
Las versiones actuales del sistema operativo Windows no son compatibles con la autenticación de usuario de las asociaciones IPsec, pero esta funcionalidad estará disponible con Windows Vista y Longhorn.  
La autenticación de equipo implica que el equipo permanecerá conectado a la WLAN y LAN incluso cuando ningún usuario haya iniciado sesión en el equipo. Esta función es necesaria para que algunas funcionalidades basadas en dominio, como los perfiles móviles, funcionen correctamente.
  
Como se observa en esta tabla, hay una serie de factores que se deben tener en cuenta al examinar las distintas posibilidades disponibles para garantizar la seguridad de las redes inalámbricas. Esta evaluación implica todo, desde los costes asociados a la implementación y administración hasta la seguridad general de la solución concreta. Cada uno de los enfoques presenta ventajas e inconvenientes, y es necesario examinar de forma más detallada cada una de las soluciones para garantizar que se toma una decisión justificada.
  
Para facilitar la comprensión de las opciones disponibles a la hora de garantizar la seguridad de las implementaciones WLAN, se analizarán en detalle los siguientes temas, ordenados por el grado de seguridad que ofrecen.
  
-   No implementación de la tecnología WLAN
  
-   Uso de WPA con EAP-TLS
  
-   Uso de WPA con PEAP-MS-CHAP v2
  
-   Uso de WPA con PEAP-MS-CHAP v2 y Servicios de Certificate Server
  
-   Uso de VPN
  
-   Uso de IPsec
  
-   Uso de WEP
  
-   Seguridad nula en WLAN
  
###### No implementación de la tecnología WLAN
  
Existe una máxima común entre las profesiones relacionadas con la seguridad: “el sistema más seguro es el que nunca se enciende”. Por tanto, el método más seguro de implementar una tecnología, incluidas las redes inalámbricas, consiste en no implementarla nunca. Por supuesto, el problema de este enfoque es que las empresas que no utilizan tecnología pueden no ser competitivas en el entorno empresarial actual, en el que cada ventaja cuenta, sobre todo las relacionadas con la tecnología.
  
Tal y como se ha mencionado anteriormente, es importante que las empresas evalúen sus propias necesidades, su tolerancia al riesgo y la cantidad de riesgo que conlleva la adopción de cualquier tecnología que estén considerando; en esto, la tecnología inalámbrica no es una excepción. Hay muchas ventajas que las redes inalámbricas pueden ofrecer, pero se pueden subestimar o incluso no ser aplicables para una determinada organización.
  
Al evaluar la solución de seguridad inalámbrica apropiada para una empresa, considere todas las opciones, incluida la alternativa de no implementar ninguna solución inalámbrica. Sin embargo, si una organización decide que no está preparada para implementar una WLAN, esta decisión debería formar parte de una directiva de empresa que se respete rigurosamente para evitar que usuarios finales implementen WLAN malintencionadas y se ponga de este modo en peligro la seguridad de la red.
  
###### Uso de WPA con EAP-TLS
  
WPA o WPA2 con Protocolo de autenticación extensible-Seguridad de la capa de transporte (EAP-TLS) y con certificados de usuario y equipo constituye el método más firme de autenticación 802.1X compatible con las versiones actuales de los clientes inalámbricos basados en Windows. EAP-TLS utiliza certificados digitales para la autenticación mutua, donde el cliente inalámbrico se autentica en un servidor de autenticación y viceversa. La autenticación EAP-TLS requiere una infraestructura de clave pública (PKI) para emitir y mantener actualizados los certificados. Para obtener el máximo nivel de seguridad, la PKI se debe configurar para que se emitan certificados de usuario y equipo para el acceso inalámbrico.
  
Debido a los costes administrativos y de implementación asociados con las PKI, esta solución tan segura solía estar limitada a las medianas y grandes empresas, pero ahora se puede utilizar en los entornos de las pequeñas empresas gracias al lanzamiento de Microsoft Small Business Server, que ofrece los servicios de certificado subyacentes que se necesitan para implementar EAP-TLS.
  
**Nota**   Actualmente no hay ningún objeto de directiva de grupo (GPO) compatible con el estándar WPA2 que pueda afectar a la capacidad de implementar eficazmente dicho estándar en entornos de mayores dimensiones. No obstante, se están desarrollando actualizaciones para Windows Server 2003 y Windows XP que agreguen compatibilidad de GPO con WPA2. La siguiente generación de Windows, Vista y Longhorn, incluirá compatibilidad nativa para el estándar WPA2.
  
###### Uso de WPA con PEAP-MS-CHAP v2
  
WPA o WPA2 con EAP protegido (PEAP) y Protocolo de autenticación por desafío mutuo de Microsoft versión 2 (MS-CHAP v2), así como con el requisito de usar contraseña segura, es la segunda implementación segura más eficaz compatible con las versiones actuales de los clientes basados en Windows. Si no es factible implementar una PKI, PEAP-MS-CHAP v2 constituye una opción viable y segura de implementar una red inalámbrica confiable. PEAP es un esquema de autenticación unidireccional que utiliza TLS para crear un canal cifrado desde el servidor de autenticación, a través del que el cliente usa otro protocolo para autenticarse. Diseñado originalmente para el acceso telefónico y el acceso remoto VPN, MS-CHAP v2 es compatible con la autenticación basada en contraseña segura de los clientes inalámbricos, pero sólo cuando se emplea junto con directivas de contraseña segura de usuario en la red.
  
###### Uso de WPA con PEAP-MS-CHAP v2 y Servicios de Certificate Server
  
Es posible combinar el uso de Servicios de Certificate Server con una solución PEAP-MS-CHAP v2 basada en contraseña para las empresas cuya solución necesite elementos de ambos enfoques. Sin embargo, PEAP-MS-CHAP v2 no agrega ninguna ventaja de seguridad adicional relevante reconocida a la solución EAP-TLS, que ya es razonablemente segura, al menos hasta el momento de la redacción del presente documento. De hecho, el uso de PEAP-MS-CHAP v2 con EAP-TLS ralentiza el proceso de autenticación porque crea dos canales TLS, uno dentro del otro. Este cifrado doble no proporciona ningún valor adicional.
  
###### Uso de VPN
  
Cuando se empezaron a detectar brechas de seguridad en el estándar WEP, una de las primeras respuestas que propusieron muchos expertos en seguridad y líderes del sector fue la de utilizar redes privadas virtuales (VPN) para hacer seguras las redes inalámbricas. La tecnología VPN es sin duda un método seguro y confiable a lo largo del tiempo para proteger las comunicaciones de red que atraviesan redes hostiles, como Internet, y esta solución al problema de las brechas de seguridad del estándar WEP se sigue utilizando en numerosos entornos.
  
Aunque parezca una solución ventajosa desde el punto de vista de la seguridad, presenta algunas imperfecciones obvias que la convierten en una opción poco atractiva si se compara con la flexibilidad que ofrecen las soluciones que utilizan WPA, que se diseñó específicamente para hacer frente a las amenazas de los sistemas inalámbricos. Aunque es perfectamente posible implementar soluciones WPA junto con la tecnología VPN para garantizar la seguridad de una red inalámbrica, dicha solución no ofrece ninguna ventaja con respecto a una solución pura basada en WPA, especialmente si se considera el nivel adicional de complejidad que se agrega a la red inalámbrica si se utiliza en combinación con una solución VPN.
  
La funcionalidad es otra de las cuestiones que se deben tener en cuenta a la hora de decidir si se debe agregar una VPN como parte de la solución de seguridad para la red WLAN. Aunque cuando los usuarios se conectan a una red empresarial a través de Internet esperan que existan requisitos de autenticación adicionales y límites de tiempo de espera asociados al uso de una VPN, estos pasos adicionales pueden resultar pesados para los usuarios que están acostumbrados a conectarse fácilmente a recursos desde dentro de una red de área local.
  
Algunas empresas pueden estar interesadas en utilizar esta solución porque simplemente ya cuentan con una solución VPN para los usuarios remotos y consideran que es necesario hacer un mayor uso de dicho sistema para justificar los costes. Si éste es el caso, deben tenerse en cuenta cuestiones adicionales antes de seleccionar este método, incluidos los siguientes aspectos:
  
-   Puesto que es necesario establecer una conexión VPN antes de que se permita la comunicación a través del túnel, la directiva de grupo del equipo no se aplicará si el usuario se conecta a la VPN después de iniciar sesión en el equipo local. (Si el usuario selecciona **Iniciar sesión mediante una conexión de acceso telefónico** al iniciar sesión en el equipo, la conexión VPN finaliza primero y se aplicará la directiva de grupo.)
  
-   La mayoría de los servidores VPN están diseñados para proteger las conexiones más lentas, como de acceso telefónico o de tráfico de banda ancha, y pueden crear cuellos de botella en la red si se establecen muchas conexiones de alta velocidad.
  
-   En función de la configuración de VPN, los usuarios pueden experimentar problemas al pasar entre los puntos de acceso inalámbrico porque las VPN cortan a menudo las conexiones, incluso tras las desconexiones más breves, lo que obliga al usuario a tener que volver a autenticarse manualmente cada vez que pasa de un punto de acceso a otro. Esto mismo también ocurre cuando el equipo de un usuario entra en el modo de espera.
  
###### Uso de IPsec
  
El uso de IPsec para garantizar la seguridad de las redes inalámbricas surge de la misma necesidad que utilizar VPN para hacer seguras las WLAN, es decir, como una solución a las brechas de seguridad detectadas en WEP. Por supuesto, IPsec ofrece un modo confiable de garantizar la seguridad de muchos tipos específicos de tráfico de red y su uso en las WLAN proporciona algunas ventajas, como la transparencia, la independencia de las limitaciones del hardware WLAN y el bajo coste, ya que no necesita servidores adicionales ni software para su funcionamiento.
  
Sin embargo, el uso de IPsec para hacer seguras las redes inalámbricas presenta algunos problemas, entre los que se incluyen los siguientes:
  
-   IPsec no puede proteger el tráfico de difusión ni de multidifusión, ya que sólo controla la comunicación entre dos partes que se han autenticado mutuamente y que han intercambiado claves.
  
-   IPsec no protege la red inalámbrica, sólo los paquetes de red.
  
-   Aunque IPsec es transparente para los usuarios, no lo es totalmente para los dispositivos de red porque funciona en el nivel de red, no en el de MAC. Esto agrega requisitos adicionales para las normas del firewall.
  
-   Cualquier dispositivo que no pueda utilizar IPsec estará expuesto a sondeos o ataques por parte de los usuarios que puedan supervisar el tráfico de la WLAN.
  
-   La administración de la directiva IPsec en entornos de mayores dimensiones puede resultar muy complicada si IPsec se utiliza para proporcionar una protección de un extremo a otro para otras aplicaciones, además de para el tráfico de la red inalámbrica.
  
###### Uso de WEP
  
La forma más básica de seguridad basada en 802.11 es el WEP estático, que utiliza una clave compartida para controlar el acceso y emplea esa misma clave como base para cifrar el tráfico inalámbrico. El principal atractivo de este método radica en su simplicidad y, aunque ofrezca una seguridad ligeramente superior a la de una configuración inalámbrica desprotegida, presenta problemas graves de administración y seguridad; concretamente, se puede tardar desde un par de minutos hasta unas horas en detectar la clave compartida y el SSID (si no se difunde) en una WLAN basada en WEP y, por tanto, obtener acceso a una red con un portátil convencional y con herramientas sencillas que están disponibles en Internet.
  
Una forma de mejorar adicionalmente el WEP estático consiste en configurar los puntos de acceso de modo que únicamente se permita a un grupo predefinido de clientes el acceso a la red mediante filtrado MAC. No obstante, también es posible atacar fácilmente un sistema que emplee este enfoque si se utilizan herramientas para detectar y suplantar las direcciones MAC de los equipos conectados a una WLAN.
  
Es posible combinar algunas tecnologías de seguridad con WEP para aumentar ligeramente la seguridad de los entornos que no disponen de compatibilidad con WPA o WPA2, pero estas configuraciones también se desaconsejan, excepto si se usan durante la fase de transición entre una implementación de WLAN no segura y una configuración basada en WPA seguro. Estos métodos, en orden de mayor a menor seguridad, son los siguientes:
  
-   WEP con autenticación 802.1X basada en EAP-TLS con certificados de usuario y equipo y reautenticación periódica obligatoria.
  
-   WEP con autenticación 802.1X basada en PEAP-MS-CHAP v2 con directivas de contraseña segura de usuario y reautenticación periódica obligatoria.
  
###### Seguridad nula en WLAN
  
Aunque nunca debe recomendarse la implementación de una red inalámbrica no segura en el entorno de una mediana empresa, existen algunas situaciones en las que una configuración de red inalámbrica no segura puede ser la solución preferida. Por ejemplo, muchas ciudades y municipios han considerado o incluso implementado zonas de acceso inalámbrico libre y, en tales casos, se puede preferir utilizar una red de puntos de acceso inalámbrico no seguros que sólo proporcione conexiones directas a Internet. Sin embargo, ya sea una u otra la finalidad o intención, se debe tener en cuenta que las redes inalámbricas no seguras son enormemente vulnerables a una amplia variedad de ataques.
  
##### WPA o WPA2
  
Los protocolos Acceso protegido Wi-Fi (WPA) y Acceso protegido Wi-Fi 2 (WPA2) se han diseñado específicamente para hacer frente a las amenazas que atentan contra las redes inalámbricas basadas en IEEE 802.11. No obstante, hay algunas diferencias entre ambos protocolos. WPA se desarrolló en 2003 como respuesta a las brechas de seguridad detectadas en el estándar WEP y solucionó dichas brechas con bastante eficacia gracias a la implementación de compatibilidad con la autenticación mutua, el uso de TKIP para el cifrado de datos y la incorporación de una comprobación de la integridad de los mensajes firmados con el fin de frustrar la suplantación de identidad y los ataques de reproducción. WPA2 mejora adicionalmente dicha seguridad al utilizar AES en lugar de TKIP para garantizar la seguridad del tráfico de red y, por tanto, este protocolo debería preferirse siempre frente al estándar WPA.
  
Los protocolos WPA y WPA2 son mucho más seguros que WEP y, si la protección se realiza correctamente, no existen hasta la fecha brechas de seguridad en ninguno de ellos. Sin embargo, WPA2 se sigue considerando mucho más seguro que WPA y se debe utilizar, cuando sea posible, si la infraestructura lo permite y se pueden mitigar los gastos administrativos adicionales.
  
La mayoría de los dispositivos de acceso inalámbrico fabricados actualmente están certificados para el uso con WPA2, al igual que la mayoría de las versiones más recientes de Windows, concretamente Windows XP con Service Pack 2 (SP2) y Windows Server 2003 con SP1. Los dispositivos inalámbricos y los clientes compatibles con WPA2 también pueden usar el antiguo estándar WPA si algunos de los puntos de acceso inalámbrico o clientes implementados en el entorno no son compatibles con WPA2.
  
**Nota**   Los clientes basados en el SP2 de Windows XP necesitan un paquete de actualización adicional, la [actualización Acceso protegido Wi-Fi 2 (WPA2) y Elemento de información de los Servicios de aprovisionamiento inalámbricos (WPS IE)](http://support.microsoft.com/default.aspx?scid=kb;es-es;893357), para que se permite la compatibilidad con la certificación WPA2. Para obtener más información sobre esta actualización, vaya a la dirección URL http://support.microsoft.com/default.aspx?scid=kb;es-es;893357.  
Asimismo, las versiones actuales de Windows no ofrecen compatibilidad de GPO con WPA2, lo que constituye una desventaja considerable desde el punto de vista de administración que hace que la implementación de WPA2 resulte mucho más compleja que la de WPA. Puede que éste sea un factor determinante para elegir entre WPA y WPA2, ya que ambos estándares son relativamente seguros.
  
#### Desarrollo de una solución WLAN segura
  
En la sección anterior se han explicado algunos de los antecedentes sobre las distintas opciones de seguridad que se pueden considerar para las redes WLAN y se ha ofrecido una descripción de las amenazas más frecuentes a las que se enfrentan las redes inalámbricas y cómo cada uno de estos enfoques hace frente o es vulnerable a dichas amenazas. Con esa información es posible tomar decisiones justificadas sobre cómo se puede aplicar cada opción a entornos empresariales específicos.
  
Las últimas mejoras de seguridad realizadas en los estándares de redes inalámbricas con la implementación de WPA y WPA2 se han centrado en las graves brechas de seguridad de WEP y, por tanto, han marginado la necesidad de buscar soluciones, como el uso de IPsec o de una VPN, para garantizar la seguridad de las conexiones inalámbricas. No se recomienda en absoluto la alternativa de utilizar el estándar WEP estático o dinámico y, por otro lado, el enfoque de no utilizar ninguna funcionalidad de seguridad sólo es útil en un número reducido de situaciones. Si se considera lo anterior, sólo quedan un par de opciones que se pueden tener en cuenta al formular una solución de seguridad completa y eficaz para las implementaciones de WLAN.
  
Esta sección guía a los responsables de tomar las decisiones a través de los demás enfoques recomendados para garantizar la seguridad de las redes inalámbricas. Estas soluciones recomendadas de Microsoft se consideran ampliamente como los métodos más seguros de implementar una red inalámbrica segura y eficaz por parte de los analistas del sector, los expertos en seguridad y los principales proveedores. Aunque este documento se centra en el método que mejor se adapta al entorno de una mediana empresa, es importante tener en cuenta todas las opciones y realizar un proceso de toma de decisiones, puesto que siempre hay excepciones válidas a la norma.
  
##### Proceso de toma de decisiones para una WLAN segura de Microsoft
  
Hay dos procesos de seguridad recomendados entre los que se puede elegir para las redes WLAN, además de un tercer enfoque combinado. Las dos principales soluciones, ordenadas por nivel de seguridad, son:
  
-   WPA2 con EAP-TLS y Servicios de Certificate Server
  
-   WPA2 con PEAP-MS-CHAPv2
  
Aparte del nivel de seguridad proporcionado por cada una de estas soluciones, el factor determinante básico para elegir entre estos dos enfoques se reduce a los recursos necesarios para implementar las soluciones y ofrecer compatibilidad con ellas.
  
WPA o WPA2 con PEAP-MS-CHAPv2 tiene menos requisitos en cuanto a conocimientos técnicos y equipamiento porque no necesita una infraestructura de certificados subyacente. Puesto que todos los dispositivos que hay actualmente en el mercado están certificados para el uso con WPA2 y no son prohibitivos desde el punto de vista de los costes, tiene cierto sentido utilizar dispositivos compatibles con WPA2, incluso si se decide usar WPA por las ventajas administrativas que presenta actualmente con respecto a WPA2. El método de cifrado AES de WPA2 se considera en general más seguro que el método TKIP de WPA y, si se considera que está previsto ofrecer compatibilidad de GPO con WPA2 en versiones futuras, conviene ir preparando las bases para una implementación futura de WPA2.
  
El uso de WPA o WPA2 con EAP-TLS es la opción disponible más segura para garantizar la seguridad de una WLAN, pero conlleva una implementación mayor y tiene asociados unos costes superiores de administración ya que depende de la infraestructura de certificados subyacente. Sin embargo, muchos entornos de medianas empresas ya disponen de sistemas que cumplen los requisitos necesarios para WPA2 con EAP-TLS, por lo que en realidad puede ser una opción más atractiva para muchas empresas. Incluso si no se dispone de la tecnología necesaria, muchas empresas necesitan la misma tecnología en la que se basa esta solución, los certificados y RADIUS para cubrir otras necesidades, por lo que incluso en ese caso existen muy buenos motivos empresariales y técnicos que justifican la implementación de esta solución.
  
[![](images/Cc875845.SWCG1(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875845.swcg1_big(es-es,technet.10).gif)
  
**Figura 1. Árbol de decisiones para una WLAN de Microsoft**
  
El diagrama de flujo de la figura 1 se ha utilizado en una guía anterior de Microsoft para ayudar a las organizaciones a determinar qué enfoque de seguridad para redes WLAN es el que mejor se ajusta al entorno concreto; asimismo, plantea algunas suposiciones con respecto a la definición de un empresa grande. Cuando utilice este diagrama de flujo, tenga en cuenta que las empresas grandes deben contar con 500 o más empleados y con un equipo de IT de al menos 5 profesionales de la tecnología.
  
Como se ha explicado anteriormente, el árbol de decisiones puede malinterpretarse en este caso, porque muchas medianas empresas, a las que está destinado este documento, tienen los recursos y la capacidad necesarios para implementar fácilmente WPA2 con EAP-TLS y Servicios de Certificate Server, dado que la mayoría de las medianas empresas poseen al menos cinco profesionales de TI en plantilla y tienen capacidad para los requisitos de infraestructura adicionales de una implementación básica de EAP-TLS (cuatro servidores adicionales, uno de los cuales permanecerá desconectado de la red).
  
Ante estos hechos, queda claro que la mejor solución para la mayoría de las medianas empresas es WPA2 con EAP-TLS y Servicios de Certificate Server. Por tanto, éste será el método en el que nos centraremos en este documento. No obstante, siempre hay excepciones válidas a la norma y, si una organización necesita un enfoque distinto, hay un gran número de guías para satisfacer dichas necesidades. Concretamente, si se prefiere usar WPA con PEAP-MS-CHAP v2, se puede encontrar información adicional en [Protección de las LAN inalámbricas con PEAP y contraseñas](http://go.microsoft.com/fwlink/?linkid=23459) (en inglés), en la dirección http://go.microsoft.com/fwlink/?linkid=23459
  
###### Requisitos de los servidores EAP-TLS
  
Como se ha mencionado anteriormente, EAP-TLS necesita al menos cuatro servidores (o más en el caso de un entorno distribuido o de mayores dimensiones), de los cuales dos se utilizarán como servidores redundantes del Servicio de autenticación Internet (IAS) (la implementación de Microsoft de un Servicio de autenticación remota telefónica de usuario) y los otros dos formarán parte de una infraestructura de certificados básica (PKI). Uno de los dos servidores de certificados servirá para alojar la entidad de certificación (CA) raíz, será independiente y permanecerá desconectado de la red para proteger el certificado raíz.
  
**Tabla 3. Requisitos de hardware recomendados para el servidor de la CA raíz**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Componente</p></th>  
<th><p>Requisito</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>CPU</p></td>
<td style="border:1px solid black;"><p>CPU a 733 MHz o superior</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Memoria</p></td>
<td style="border:1px solid black;"><p>256 MB de RAM</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Interfaz de red</p></td>
<td style="border:1px solid black;"><p>Ninguna (o deshabilitada)</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Unidad de almacenamiento en disco</p></td>
<td style="border:1px solid black;"><p>Controlador IDE o SCSI RAID</p>
<p>2 discos duros de 18 GB configurados como un único volumen RAID (unidad C)</p>
<p>Unidad extraíble de almacenamiento local para la transferencia de datos (certificado raíz).</p></td>
</tr>
</tbody>
</table>
<p> </p>

Como muestra la tabla, los requisitos (basados en los requisitos genéricos de Windows Server 2003 Standard Edition) de la CA raíz son en buena parte mínimos e incluso se pueden crear en una plataforma más antigua que se vaya a retirar o como una máquina virtual si fuese necesario. Para muchos clientes puede ser útil emplear un equipo portátil porque es muy sencillo garantizar su seguridad física al guardarlo en una caja fuerte de la sala de equipos. Independientemente del enfoque que se adopte para crear la CA raíz, es importante asegurarse de que el equipo en cuestión se pueda iniciar o restaurar de forma confiable si es necesario.

Los requisitos de hardware de la entidad emisora de certificados (CA emisora) son similares, pero tienen requisitos de almacenamiento adicionales y es necesario que el servidor esté conectado a la red. Como este servidor debe almacenar todos los certificados emitidos, se recomienda que el disco duro tenga una capacidad de al menos 2 GB por cada 1.000 usuarios.

Los requisitos de los servidores RADIUS son superiores porque estos servidores son decisivos para mantener la funcionalidad de la WLAN y deben ser capaces de administrar un gran número de intentos de autenticación en períodos breves de tiempo. Por este motivo, se necesita una plataforma de hardware sólida para los entornos que vayan a tener miles de clientes inalámbricos. Asimismo, aunque las entidades emisoras de certificados sólo necesitan utilizar Windows Server 2003 Standard Edition, es posible que los servidores IAS necesiten utilizar la versión Enterprise Edition porque la Standard Edition sólo admite 50 clientes RADIUS.

Por estos motivos, se suele recomendar la instalación de IAS en controladores de dominio, ya que de este modo se reduce la necesidad de tener que disponer de hardware de servidor adicional al aprovechar las sólidas plataformas de servidor ya existentes que necesitan los controladores de dominio; además, el uso de IAS en controladores de dominio aumenta en realidad el rendimiento de IAS al reducir el tráfico de red que se produce entre los controladores de dominio e IAS durante la autenticación del usuario.

La conmutación por error y la redundancia, así como las consideraciones sobre la ubicación remota, también entran en juego a la hora de determinar los requisitos de los servidores RADIUS. Aunque los requisitos mínimos recomendados son para dos servidores IAS, es posible que algunas empresas tengan muchas oficinas remotas y que necesiten servidores IAS en algunas de dichas ubicaciones. Algunas empresas también pueden tener requisitos superiores en cuanto a la redundancia o el equilibrio de carga de los servidores.

Aunque no existen recomendaciones en contra del uso de servidores multifunción, como los servidores RADIUS, es importante considerar la carga adicional que puede crearse en un servidor de este tipo y la naturaleza de dichas demandas. Un servidor RADIUS debe ser escalable para tolerar aquellas situaciones en las que todos los clientes inalámbricos se intenten conectar en un breve período de tiempo.

##### Certificados

Independientemente del enfoque WPA adoptado para garantizar la seguridad de una WLAN, se necesitan certificados de algún tipo como parte de la solución. PEAP sólo necesita certificados en el servidor de autenticación y, por tanto, se puede utilizar simplemente un servicio de certificados de un tercero para proporcionar los certificados necesarios; de este modo, no sería necesario implementar una PKI. Éste es el principal motivo por el que se recomienda el enfoque PEAP para las organizaciones pequeñas que tal vez carezcan de los conocimientos o los recursos necesarios para ocuparse de la implementación y compatibilidad de una infraestructura de certificados.

La implementación compatible con Windows de EAP-TLS con Servicios de Certificate Server no requiere que exista necesariamente una PKI subyacente para ofrecer compatibilidad con la emisión de certificados, pero como cada cliente debe tener un certificado para establecer la autenticación con el servidor RADIUS, el uso de certificados de terceros puede tener un coste prohibitivo para todas las empresas, excepto para las más pequeñas. Estas mismas consideraciones también son aplicables si se utiliza PEAP combinado con el enfoque de Servicios de Certificate Server.

Si una organización ya tiene una PKI, el proceso de toma de decisiones será probablemente más sencillo; al fin y al cabo, si los componentes ya están instalados, también se podrán utilizar y será posible implementar la opción que sea más segura para la seguridad de la WLAN. Incluso en el caso de que no haya establecida una implementación de PKI, una mediana empresa puede seguir considerando acertada la decisión de invertir en una infraestructura de certificados si tiene en cuenta los otros usos que pueda dar a tales implementaciones, entre los que se incluyen:

-   Firmas de código

-   Mensajería segura de correo electrónico

-   Entrega segura de contenido web

-   Seguridad de VPN

-   Servicios de archivos cifrados

Si se considera todo lo anterior, el uso de Servicios de Certificate Server con EAP-TLS o con PEAP es el enfoque más adecuado para las medianas empresas, por lo que constituye el objeto de atención de este documento.

###### Creación de una declaración de prácticas de certificación (CPS)

La planeación inicial de una PKI debe incluir documentación acerca del modo en que los certificados se van a utilizar en el entorno empresarial. Aunque tales decisiones se pueden modificar a medida que surgen las necesidades, es importante exponer estas decisiones en una declaración formal de directiva de certificados.

En términos formales, una directiva de certificados es un conjunto de reglas que rigen el funcionamiento de la PKI. Registra información relacionada con la aplicación de certificados a determinados grupos o aplicaciones de la organización que tienen requisitos de seguridad comunes. La declaración de prácticas de certificación indica las prácticas que una empresa utiliza para administrar los certificados que emite. Describe cómo se interpreta la directiva de certificados en el contexto de la infraestructura de los sistemas empresariales y las directivas de los procedimientos operativos. Si bien una directiva de certificados es un documento aplicable a toda la organización, la declaración de prácticas de certificación es específica de una CA, aunque las CA pueden tener una declaración de prácticas de certificación común si realizan las mismas tareas.

En el caso de algunas empresas, estas declaraciones son documentos legales de obligada creación en virtud de requisitos normativos que regulan los sectores en los que se lleva a cabo la actividad y para cuya creación se necesita asistencia jurídica. No obstante, aunque una empresa no esté regulada por tales requisitos, sigue siendo una buena idea crear estos documentos.

###### Jerarquía de las entidades de certificación

El diseño especificado en esta guía utiliza un modelo de confianza jerárquico con una única raíz interna. Este enfoque presenta una serie de ventajas y desventajas, por lo que puede ser necesario realizar un análisis posterior para determinar si este enfoque concreto es adecuado para la empresa en la que se va a implementar. Para obtener más información sobre este tema, consulte el capítulo “[Diseño de una infraestructura de clave pública](http://technet2.microsoft.com/windowsserver/en/library/b1ee9920-d7ef-4ce5-b63c-3661c72e0f0b1033.mspx)” (en inglés) del Kit de implementación de Windows Server 2003 en http://technet2.microsoft.com/WindowsServer/en/library/b1ee9920-d7ef-4ce5-b63c-3661c72e0f0b1033.mspx.

![](images/Cc875845.SWCG2(es-es,TechNet.10).gif)

**Figura 2. Jerarquía de las entidades de certificación**

###### Seguridad de la entidad emisora raíz

La implementación de Microsoft de EAP-TLS no funcionará a menos que la CA raíz sea segura “de forma inalámbrica” (desconectada de la red). Existen algunos motivos de seguridad de peso para utilizar el diseño de una CA raíz independiente de este tipo, en lugar de una CA raíz de empresa y, por tanto, suele ser el enfoque recomendado para cualquier implementación de PKI.

Puesto que este enfoque tal vez se considere un derroche de recursos, hay algunos métodos que una empresa puede utilizar para volver a implementar al menos una parte del hardware empleado para crear una CA raíz que nunca se conectará a la red. Algunas de estas recomendaciones son:

-   Después de crear el certificado raíz y distribuirlo a una CA emisora, las unidades de disco duro de la CA raíz se pueden quitar y almacenar de forma segura hasta que se vuelvan a necesitar. El inconveniente de este enfoque es que si se necesita la CA raíz, se tendrá que reclamar el hardware correspondiente de dichas unidades.

-   Después de crear el certificado raíz y distribuirlo a una CA emisora, se puede realizar una imagen del servidor si se hace una copia de seguridad y se guarda en cintas u otro tipo de medio sin conexión, lo que permitirá volver a utilizar el hardware del servidor. Una vez más, existe el mismo problema si se necesita de nuevo: sería necesario reclamar dicho hardware.

-   Utilice un servidor virtual, un PC virtual o algún otro tipo de software de máquina virtual para crear la CA raíz; una vez creado y distribuido el certificado raíz, la imagen de la máquina virtual se puede guardar en un medio de almacenamiento sin conexión y archivarse por si se vuelve a necesitar. Si se utiliza una plataforma genérica estándar (como el sistema de escritorio estándar de la organización si cumple los requisitos de hardware) para este enfoque, es más sencillo reclamar el hardware necesario en caso de que se necesite de nuevo la CA raíz.

-   Cree la CA raíz sin conexión en el equipo portátil del año pasado y guárdelo en una caja fuerte de la sala de equipos. De este modo, dará uso a un recurso de hardware que, de otro modo, acabaría desechando.

##### Autenticación de Internet

El Servicio de autenticación Internet (IAS) es la implementación de Microsoft de un servidor proxy y RADIUS. IAS permite realizar procesos centralizados de autenticación, autorización y contabilidad para una variedad de conexiones de red. IAS se puede utilizar con otros servidores RADIUS (como un reenviador de autenticación, autorización y contabilidad), con otros servidores VPN (como servidores de acceso remoto y enrutamiento) o con otra infraestructura de red (como puntos de acceso inalámbrico).

Al desarrollar un plan de implementación para una infraestructura IAS, es importante aprovechar el valor de una infraestructura RADIUS basada en IAS, ya que no se ha diseñado para proporcionar acceso a una sola red aislada. Por tanto, la planeación e implementación de una infraestructura IAS debe incluir una decisión sobre si se debe utilizar un servicio centralizado para administrar el acceso a la red, incluido el uso de una base de datos centralizada de cuentas como Active Directory, además de garantizar que se verán satisfechas las necesidades presentes y futuras de la organización. En otras palabras, la implementación de una infraestructura IAS también debe ser estratégica, no solamente táctica.

Esta guía sólo abordará los aspectos de la planeación e implementación de IAS relacionados con una infraestructura inalámbrica segura. Para conocer otras posibilidades y cuestiones relativas a la planeación e implementación de IAS, consulte la sección "Recursos de implementación" (en inglés) que está disponible en la página de inicio del [Servicio de autenticación Internet](http://www.microsoft.com/technet/itsolutions/network/ias/default.mspx), en www.microsoft.com/technet/itsolutions/network/ias/default.mspx.

###### Implementaciones de RADIUS ya existentes

Aunque esta solución puede integrarse en implementaciones de RADIUS ya existentes, esta guía no proporciona dicho proceso. En la mayoría de los casos conviene utilizar IAS para las características descritas en la guía. Para tal fin, es posible actualizar las plataformas antiguas a Windows Server 2003 para que actúen como servidores RADIUS básicos o bien modificar los servidores RADIUS existentes en el tráfico de proxy RADIUS en nuevos servidores RADIUS basados en Windows Server 2003.

Para obtener una orientación detallada de planeación sobre la migración de una infraestructura RADIUS existente a servidores RADIUS basados en Windows Server 2003, consulte la página de [referencia técnica de IAS](http://technet2.microsoft.com/windowsserver/en/library/8f5c89d5-fdaf-430c-9ef4-318f8c15baf11033.mspx) (en inglés) en http://technet2.microsoft.com/WindowsServer/en/Library/8f5c89d5-fdaf-430c-9ef4-318f8c15baf11033.mspx o póngase en contacto con un representante de cuentas o un profesional de servicios de consultoría de Microsoft.

###### Conmutación por error y equilibrio de carga de los servidores RADIUS

Puesto que RADIUS es un componente crítico de cualquier solución de seguridad inalámbrica 802.1X, la disponibilidad de una red inalámbrica depende de la disponibilidad de los servidores RADIUS. Por tanto, una solución RADIUS compatible con redes inalámbricas debe ser confiable y redundante, además de ofrecer capacidad de respuesta, para garantizar una disponibilidad y un rendimiento equivalentes a los de una red cableada. De ahí que se suela recomendar la instalación de IAS en controladores de dominio existentes.

Antes de tomar una decisión sobre la estrategia de equilibrio de carga, es importante comprender que 802.1X implementa EAP dentro de RADIUS (EAP-RADIUS), entre el punto de acceso inalámbrico y el servidor RADIUS. Aunque RADIUS utilice UDP, EAP es un protocolo orientado a sesiones que crea un túnel dentro de RADIUS. Esto significa que los distintos paquetes EAP-RADIUS de una operación de autenticación individual deben devolverse al mismo servidor RADIUS o, de lo contrario, se generarán errores en el intento de autenticación concreto.

Hay dos enfoques disponibles para el equilibrio de carga y la conmutación por error de los servidores IAS por lo que respecta a las redes inalámbricas. El primero consiste en el uso de servidores proxy IAS con grupos de servidores RADIUS; y el segundo, en la configuración de los servidores RADIUS principales y secundarios con los valores de hardware de los puntos de acceso inalámbrico. En la siguiente lista se incluyen las ventajas y desventajas de cada uno de los enfoques.

**Tabla 4. Conmutación por error y equilibrio de carga de RADIUS para EAP**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Método</p></th>
<th><p>Ventajas</p></th>
<th><p>Desventajas</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Servidores proxy IAS con grupos de servidores RADIUS</p></td>
<td style="border:1px solid black;"><ul>
<li><p>Detección de errores de los servidores RADIUS con conmutación por error y conmutación por recuperación.</p></li>  
<li><p>Distribución de la carga del tráfico en función de las propiedades del tráfico.</p></li>  
<li><p>Mantenimiento del estado de la sesión EAP durante el equilibrio de carga.</p></li>  
<li><p>Distribución configurable de las peticiones a los servidores en función de valores de prioridad y peso.</p></li>
</ul></td>
<td style="border:1px solid black;"><ul>
<li><p>Se necesitan servidores IAS adicionales.</p></li>  
<li><p>Sigue siendo necesario configurar las direcciones de los servidores proxy RADIUS principales y secundarios.</p></li>
</ul></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Configuración de los servidores RADIUS principales y secundarios en los puntos de acceso inalámbrico</p></td>
<td style="border:1px solid black;"><ul>
<li><p>Configuración más sencilla para los entornos más pequeños.</p></li>  
<li><p>El punto de acceso inalámbrico detecta los errores en el tráfico y realiza la conmutación por error.</p></li>  
<li><p>Utiliza la funcionalidad nativa de los puntos de acceso inalámbrico.</p></li>
</ul></td>
<td style="border:1px solid black;"><ul>
<li><p>Conlleva costes superiores de planeación y supervisión de la distribución del tráfico de los servidores RADIUS principales y secundarios.</p></li>  
<li><p>Algunos puntos de acceso inalámbrico siguen sin ser compatibles con la funcionalidad de conmutación por recuperación, lo que puede provocar cargas de tráfico desequilibradas.</p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p>

Las empresas de mayores dimensiones deben considerar el uso de servidores proxy RADIUS configurados en grupos de servidores RADIUS para distribuir las cargas en los servidores RADIUS. Esta opción proporciona un cierto grado de flexibilidad al permitir distribuir el tráfico según una serie de elementos configurables, como el tipo de tráfico RADIUS y los atributos de RADIUS, además de en función de los valores de peso y prioridad. Este tipo de arquitectura también ofrece la máxima flexibilidad y escalabilidad a la hora de dar servicio a las peticiones de autenticación, además de ser menos estricta desde el punto de vista administrativo.

La funcionalidad de conmutación por error más sencilla de los servidores RADIUS integrada en los puntos de acceso inalámbrico puede proporcionar un nivel suficiente de resistencia para la mayoría de las organizaciones, pero no es una solución tan sofisticada como utilizar grupos de servidores proxy. No obstante, la migración de esta arquitectura a una solución de conmutación por error y equilibrio de carga basada en servidores proxy RADIUS es relativamente sencilla, por lo que esta solución también deja cierta cabida para el crecimiento. Para las empresas que únicamente desean una cobertura inalámbrica pequeña o limitada, esta solución es eficaz y fácil de implementar. Sin embargo, a medida que aumente el tamaño y la complejidad de la red inalámbrica, también crecerá el esfuerzo de administración e implementación, ya que cada dispositivo necesita una supervisión y planeación minuciosas para mantener el equilibrio de carga entre todos los servidores.

[![](images/Cc875845.SWCG3(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875845.swcg3_big(es-es,technet.10).gif)

**Figura 3. Métodos de conmutación por error y equilibrio de carga en una WLAN RADIUS**

El equilibrio de carga con la funcionalidad integrada de puntos de acceso inalámbrico implica la configuración de aproximadamente la mitad de puntos de acceso inalámbrico en cada ubicación para su utilización en el servidor RADIUS principal con otro conjunto como secundario, mientras que la otra mitad de los puntos de acceso inalámbrico utilizan asignaciones inversas en los campos principal y secundario, tal y como se muestra en la figura 3. Es evidente la elevada sobrecarga, ya que puede haber más carga en algunos puntos de acceso inalámbrico que en otros, lo que conlleva una supervisión superior para alcanzar y mantener un nivel eficaz del equilibrio de carga.

###### Requisitos de registro de RADIUS

Los servidores IAS pueden registrar dos tipos de eventos opcionales:

-   Intentos correctos e incorrectos de autenticación

-   Información sobre las cuentas y la autenticación RADIUS

Los eventos de autenticación se generan cuando los dispositivos y los usuarios intentan tener acceso a la WLAN. IAS los registra en el registro de eventos del sistema de Windows Server 2003. Estos eventos son útiles para solucionar problemas y como parte de una auditoría de seguridad y del sistema de detección de intrusiones. Es necesario habilitar inicialmente el registro de los eventos correctos e incorrectos, aunque puntualmente se deban filtrar para evitar un desbordamiento del registro de eventos del sistema. Si se registran las peticiones de autenticación RADIUS puede que sea innecesario utilizar estos eventos por motivos de seguridad.

###### Servidores IAS centralizados o distribuidos

Como diseño de punto de partida, se debe considerar una arquitectura centralizada de servidores IAS para la mayoría de las medianas empresas, ya que la mayor parte de ellas tienen conexiones WAN resistentes de alta velocidad a instalaciones remotas y el tráfico de RADIUS no consume mucho ancho de banda porque se ha diseñado para funcionar con conexiones de acceso telefónico y vínculos WAN. El diseño centralizado es más rentable si hay instalada una infraestructura WAN redundante y de alta velocidad.

Incluso en ese caso, se debe analizar minuciosamente la capacidad actual de los vínculos WAN existentes para determinar si se trata de la mejor opción, ya que se puede agotar el tiempo de espera de otra comunicación, como el tráfico DHCP, mientras se espera a que finalice el intento de autenticación 802.1X durante una conexión congestionada. La conectividad de los clientes no es la única preocupación a la hora de plantearse si se debe utilizar una arquitectura IAS centralizada, ya que la comunicación entre los servidores IAS y los controladores de dominio requiere conexiones de red sólidas para evitar tiempos de espera mientras se determinan los derechos de acceso a la red y la pertenencia a grupos.

Es posible que algunas empresas no saquen provecho de una arquitectura centralizada debido a los costes asociados a las conexiones WAN redundantes de gran ancho de banda y al sofisticado equipo de red necesario. Estas empresas optarán por utilizar un diseño IAS distribuido, especialmente si ya tienen una infraestructura de servidores descentralizados.

Hay por otro lado un tercer enfoque que es un híbrido de los dos anteriores y que permite ubicar de forma estratégica los servidores IAS en lugares compatibles con la infraestructura para que dichos servidores puedan proporcionar autenticación a sucursales que tal vez no tengan una base subyacente de servidores, como se muestra en la siguiente figura.

[![](images/Cc875845.SWCG4(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875845.swcg4_big(es-es,technet.10).gif)

**Figura 4. Enfoque mixto de infraestructura de WLAN con IAS**

En esta guía se incluyen los tres modelos y se ofrece orientación para configurar oficinas de coordinación grandes que tienen dos servidores RADIUS con capacidad para dar servicio a peticiones locales y remotas, así como instrucciones para configurar oficinas centrales grandes con sucursales que tienen un solo servidor opcional.

**Nota**   De nuevo, el acceso a la WLAN desde oficinas remotas sin una infraestructura de servidor depende de la disponibilidad de la WAN.

###### Consideraciones sobre la colocación y co-emplazamiento de los servidores IAS

Para mantener la accesibilidad a los servicios WLAN, es necesario que haya al menos dos servidores RADIUS para cada bosque independiente de Active Directory. Aparte de este requisito básico, hay una serie de factores que determinan el número de servidores necesarios y si éstos pueden ser candidatos de un co-emplazamiento con otras funciones de servidor.

En general, la colocación de los servidores IAS debe ser posterior a la colocación de los controladores de dominio; es decir, si una oficina depende del vínculo WAN de alta velocidad de otra oficina para disfrutar de los servicios del dominio, es probable que también deba utilizar un servidor RADIUS remoto. Las oficinas de mayor tamaño que ya tienen controladores de dominio propios probablemente necesitarán disponer de al menos un servidor RADIUS, con una posible funcionalidad de conmutación por error ubicada en otro lugar según el vínculo WAN disponible. Se debe evaluar con mucha atención la capacidad del vínculo WAN cuando se planea la colocación de los servidores RADIUS para la confiabilidad de la autenticación de usuario local y para la colocación de controladores de dominio empleados para autenticación debido al tráfico adicional generado. Asimismo, para obtener un rendimiento mejorado, los servidores RADIUS deben ubicarse en el dominio raíz de un bosque para optimizar las operaciones Kerberos.

Otra consideración puede estar relacionada con si es factible colocar servidores adicionales en ubicaciones remotas donde parece haber esa necesidad, ya que las oficinas más pequeñas tal vez no dispongan del espacio o la infraestructura necesarios para el hardware de servidor adicional. Para abordar estas cuestiones, es posible el co-emplazamiento de un servidor IAS con un controlador de dominio de Active Directory. En la siguiente tabla se describen algunas de las ventajas y desventajas de este enfoque.

**Tabla 5. Consideraciones sobre el co-emplazamiento de IAS y un controlador de dominio**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Ubicación de IAS</p></th>
<th><p>Ventajas</p></th>
<th><p>Desventajas</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Co-emplazamiento en el controlador de dominio</p></td>
<td style="border:1px solid black;"><ul>
<li><p>Aumenta el rendimiento de la autorización y autenticación de usuarios y equipos.</p></li>  
<li><p>Reduce la necesidad de hardware de servidor adicional.</p></li>
</ul></td>
<td style="border:1px solid black;"><ul>
<li><p>No hay separación entre los grupos de administración de IAS y los administradores de dominio.</p></li>  
<li><p>No hay separación inherente de los errores o problemas de rendimiento asociados a los servicios de co-emplazamiento.</p></li>
</ul></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Servidores IAS independientes</p></td>
<td style="border:1px solid black;"><ul>
<li><p>Separación de la administración de IAS de los administradores de dominio.</p></li>  
<li><p>El comportamiento y la carga de IAS no afectan al controlador de dominio.</p></li>
</ul></td>
<td style="border:1px solid black;"><ul>
<li><p>Se necesita hardware de servidor adicional.</p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p>

Como se muestra en esta tabla, hay una razón de peso por la que muchas organizaciones disponen de directivas que aíslan la funcionalidad de los controladores de dominio en los propios servidores, ya que son críticos para el entorno de red. También puede que preocupe la seguridad si los servicios de IAS se colocan en un controlador de dominio y hay una separación de las tareas que afectan a ambos grupos administrativos, porque no existe una separación inherente de la administración de IAS y las funciones del grupo local de administradores de Windows. Se deben tener en cuenta estas cuestiones antes de tomar una decisión sobre el posible co-emplazamiento de los servicios de IAS. No obstante, hay algunas ventajas de rendimiento si se toma esta decisión, además de la obvia ventaja en cuanto a costes, sobre todo en las ubicaciones remotas.

Para compensar los costes derivados de agregar hardware de servidor a las oficinas remotas, se pueden utilizar controladores de dominio existentes (tal vez ya existan en las ubicaciones remotas) como servidores IAS, bien directamente o si se agrega una máquina virtual al controlador de dominio existente.

###### Estimación de la carga en el servidor y los requisitos de hardware

La evaluación y planeación de las posibles cargas en el servidor debe enfocarse desde la perspectiva de los peores casos. Concretamente, ¿qué sucede si todos los posibles usuarios de la WLAN necesitan autenticarse en un breve período de tiempo durante un evento de conmutación por error? Por supuesto, el diseño óptimo es aquel que implementa el número mínimo de servidores con los que es posible resistir y que deja al mismo tiempo espacio para un futuro crecimiento si es necesario.

Es necesario tener en cuenta la siguiente información a la hora de planear los requisitos y las cargas de los servidores IAS:

-   El número de usuarios y dispositivos que necesitan autenticación y contabilidad.

-   Las opciones de autenticación, como el tipo de EAP, y la frecuencia de reautenticación.

-   Las opciones de RADIUS, como la información de registro y el seguimiento del software IAS.

En el caso de que se utilice WPA o WPA2 con EAP-TLS y Servicios de Certificate Server para esta solución, es importante tener en cuenta que WPA y WPA2, a diferencia de WEP, eliminan la necesidad de forzar la reautenticación para actualizar las claves de sesión, por lo que la sobrecarga es menor en ese sentido. También es importante considerar que EAP-TLS exige una operación de clave pública de CPU intensiva tras cada autenticación inicial, pero más adelante utiliza credenciales almacenadas en la memoria caché para obtener una reconexión rápida durante cada inicio de sesión posterior hasta que caduca la credencial almacenada en la memoria caché, que sucede de forma predeterminada cada 8 horas. También merece la pena destacar que la reautenticación se producirá cuando un cliente se mueva de un punto de acceso inalámbrico que se autentica en un servidor RADIUS a un punto de acceso inalámbrico que se autentica en otro servidor de autenticación; esto sólo sucede una vez por cada servidor de autenticación y el proceso es transparente para el usuario.

Al calcular la capacidad del servidor IAS, es útil usar el número de autenticaciones por segundo como estimación de las posibles cargas. En la siguiente tabla se muestra la capacidad estimada de autenticación por segundo de un servidor IAS con Active Directory en una plataforma con una CPU Intel Pentium 4 a 2 GHz.

**Tabla 6. Autenticaciones por segundo**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de autenticación</p></th>
<th><p>Autenticaciones por segundo</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Nuevas autenticaciones de EAP-TLS</p></td>
<td style="border:1px solid black;"><p>36</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Nuevas autenticaciones de EAP-TLS con compatibilidad con tarjeta de carga</p></td>
<td style="border:1px solid black;"><p>50</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Autenticaciones con reconexión rápida</p></td>
<td style="border:1px solid black;"><p>166</p></td>
</tr>  
</tbody>  
</table>
  
**Nota**   La información de esta tabla sólo se debe considerar como una estimación que puede utilizarse a modo de orientación para planear la capacidad.
  
Según esta tabla, un servidor de este tipo puede procesar 36 nuevas autenticaciones por segundo en caso de que se produzca una conmutación por error o un pico de demanda; por lo tanto, la autenticación de 100 usuarios tardaría aproximadamente 3 segundos.
  
Otro factor que se debe tener en cuenta es cómo afecta el registro basado en disco al tiempo de autenticación. Un subsistema de disco lento puede afectar negativamente al tiempo de autenticación si se utiliza el registro detallado para el seguimiento de la actividad de autenticación. Asegúrese de utilizar un subsistema de disco rápido para que el tiempo de respuesta de los servidores IAS sea razonable.
  
##### Autenticación 802.11 de WPA
  
Hasta ahora se ha descrito el uso de una infraestructura de certificados y RADIUS para garantizar la seguridad de las comunicaciones inalámbricas mediante la autenticación de usuarios y dispositivos. Ahora pasaremos a analizar cómo se protegen los datos transmitidos entre los dispositivos inalámbricos frente a los sondeos y otros riesgos.
  
La utilización de transmisiones por radio siempre se ha considerado menos segura que las comunicaciones cableadas, ya que es mucho más sencillo interceptar los datos transmitidos por aire que los datos que pasan por un cable o tablero de conexiones, especialmente si se utiliza seguridad en los puertos. Para contrarrestar la naturaleza inherentemente insegura de las comunicaciones inalámbricas, es necesario cifrar los datos para que, ante una interceptación, los posibles interceptadores no consigan leer fácilmente la información.
  
Las especificaciones WEP iniciales para el cifrado inalámbrico resultaron ser inadecuadas para esta tarea y por ello se creó el estándar WPA como una medida provisional y un subconjunto de la especificación 802.11i, pendiente en aquel momento. Por último, se elaboró un borrador de WPA2 como una implementación completa del actual estándar oficial 802.11i. La principal diferencia entre WPA y WPA2 es el método de cifrado: WPA usa TKIP y WPA2 utiliza el estándar AES-CCMP, que es más seguro.
  
Aunque la solución propuesta en esta guía se puede utilizar para proteger WEP o WPA, se recomienda usar WPA2, siempre que sea viable desde el punto de vista administrativo, si se desea disponer de la seguridad máxima y más confiable que hay disponible actualmente para las comunicaciones inalámbricas. Si no es posible, el uso de WPA junto con la solución proporcionada en esta guía también ofrece un nivel adecuado de seguridad.
  
###### Requisitos de los clientes
  
La solución descrita en esta guía se ha diseñado para equipos cliente con capacidad inalámbrica que utilicen Windows XP Professional con SP2 o Windows XP Tablet Edition. Estas versiones del sistema operativo Windows ofrecen compatibilidad integrada para WLAN y 802.1X. Asimismo, los clientes basados en Windows XP disponen de funcionalidad de inscripción automática y renovación de certificados, lo que hace que este tipo de solución basada en certificados sea especialmente rentable cuando está asociada a una infraestructura de certificados.
  
Aunque el SP2 de Windows XP incluye compatibilidad integrada para WPA, es necesario instalar una actualización adicional para habilitar la compatibilidad con WPA2 IEEE 802.11i en los clientes basados en el SP2 de Windows XP. Para obtener más información sobre esta actualización adicional, además de las instrucciones de descarga, consulte el artículo que informa que [está disponible la actualización de Acceso protegido Wi-Fi 2 (WPA2) y el Elemento de información de los Servicios de aprovisionamiento inalámbricos (WPS IE)  
para Windows XP con Service Pack 2](http://support.microsoft.com/default.aspx?scid=kb;es-es;893357), en http://support.microsoft.com/default.aspx?scid=kb;es-es;893357.
  
###### Requisitos de la infraestructura de servidor
  
Como se ha comentado anteriormente, esta solución requiere el uso de los componentes Servicios de Certificate Server e IAS de Windows Server 2003. Hay algunas características integradas compatibles con la implementación de Windows Server 2003 de Servicios de Certificate Server e IAS que son específicas de las WLAN de 802.1X. Aunque Servicios de Certificate Server e IAS se pueden implementar en versiones anteriores de Windows, esta guía se ha elaborado específicamente para un entorno con Windows Server 2003 Active Directory.
  
###### Requisitos de los puntos de acceso inalámbrico
  
Esta guía se centra en el elemento de seguridad de una solución WLAN, por lo que no se ofrece orientación sobre la implementación, ubicación o selección de canales del hardware de los puntos de acceso inalámbrico. Para obtener más información sobre problemas específicos, configuraciones o ubicación del hardware de los puntos de acceso inalámbrico, consulte las instrucciones o el sitio web del proveedor.
  
Esta solución es más segura si se utiliza hardware de punto de acceso inalámbrico que esté certificado para el uso con WPA2 de IEEE 802.11i y que incluya funcionalidad integrada de conmutación por error y conmutación por recuperación. Es posible implementar esta solución con equipos certificados para el uso con WPA sin que apenas varíen las orientaciones proporcionadas y, al mismo tiempo, mantener un nivel elevado de seguridad. Sin embargo, aunque también se puede implementar esta solución con el estándar WEP, no se recomienda hacerlo y en esta guía no se apoya dicha decisión.
  
#### Implementación y administración
  
Aunque esta sección incluye una orientación paso a paso sobre la instalación y configuración de los servidores y servicios necesarios para la solución, no contiene los pasos reales de instalación y configuración que es preciso seguir para sistemas operativos como Windows Server 2003 y Windows XP Professional. Se asume que en la mayoría de las empresas se han establecido procesos de creación y directrices de seguridad.
  
##### Certificados
  
Aunque esta sección ofrece una orientación detallada sobre la instalación de una PKI, no incluye detalles relacionados con el proceso de creación y protección de los servidores, ya que se considera que ya existe un proceso normalizado para estos procedimientos.
  
También se asume que los servidores de CA ya se han configurado con una imagen base y que se han protegido mediante un proceso estándar de la organización antes de llegar a esta fase de la solución.
  
**Nota**   No olvide que la CA raíz nunca se conectará a la red, por lo que será necesario modificar los pasos del proceso de creación y protección de servidores de la organización que impliquen una conexión a la red para ajustarse a esta excepción.
  
###### Información de configuración necesaria definida por el usuario
  
La siguiente tabla incluye parámetros específicos de la organización que deben recopilarse o sobre los que hay que tomar una decisión antes de comenzar a implementar la solución proporcionada más adelante en esta guía. A lo largo de la guía verá marcadores de posición que sirven para describir los parámetros y que usan un formato similar al nombre del parámetro. Por ejemplo, el nombre DNS del dominio raíz de un bosque de Active Directory puede aparecer como *NombreDeDominio*.com. Los valores que aparecen en cursiva se deben sustituir con la información específica de la organización que se haya recopilado durante este proceso.
  
**Tabla 7. Información de configuración definida por el usuario**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="33%" />  
<col width="33%" />  
<col width="33%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Elemento de configuración</p></th>  
<th><p>Referencia</p></th>  
<th><p>Parámetro</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Nombre DNS del bosque de Active Directory</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Nombre distintivo (DN) de la raíz del bosque</p></td>
<td style="border:1px solid black;"><p>Pkiparams.vbs</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Nombre NetBIOS del dominio</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Nombre NetBIOS del grupo de trabajo de la CA raíz</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Nombre del servidor de la CA raíz</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Nombre del servidor de la CA emisora</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Nombre común X.500 de la CA raíz</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Nombre común X.500 de la CA emisora</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Nombre completo de host del servidor web utilizado para publicar los certificados de la CA</p></td>
<td style="border:1px solid black;"><p>Pkiparams.vbs</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
</tbody>  
</table>
  
###### Elementos de configuración necesaria que se recomiendan para la solución
  
Los parámetros identificados en la siguiente tabla no necesitan cambiarse, excepto si se precisa otro parámetro. Antes de cambiar los parámetros de esta tabla, asegúrese de comprender bien las repercusiones de tales cambios, así como las dependencias que pueden alterarse al modificarlos.
  
**Tabla 8. Elementos de configuración recomendados para la solución**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="33%" />  
<col width="33%" />  
<col width="33%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Elemento de configuración</p></th>  
<th><p>Referencia</p></th>  
<th><p>Parámetro</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>Grupos de seguridad de funciones de administración</strong></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Administradores del contenedor de configuración Servicios de clave pública</p></td>
<td style="border:1px solid black;"><p>ca_setup.wsf</p></td>
<td style="border:1px solid black;"><p>Administradores de PKI de empresa</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Grupo administrativo que puede publicar CRL y certificados de CA en el contenedor de configuración Empresa.</p></td>
<td style="border:1px solid black;"><p>ca_setup.wsf</p></td>
<td style="border:1px solid black;"><p>Publicadores de PKI de empresa</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Grupo administrativo que configura y mantiene las CA y controla la posibilidad de asignar el resto de funciones de CA y renovar el certificado de CA.</p></td>
<td style="border:1px solid black;"><p>ca_setup.wsf</p></td>
<td style="border:1px solid black;"><p>Administradores de CA</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Grupo administrativo que aprueba las peticiones de inscripción y revocación de certificados (función de responsable de CA).</p></td>
<td style="border:1px solid black;"><p>ca_setup.wsf</p></td>
<td style="border:1px solid black;"><p>Administradores de certificados</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Grupo administrativo que administra la auditoría de CA y los registros de seguridad.</p></td>
<td style="border:1px solid black;"><p>ca_setup.wsf</p></td>
<td style="border:1px solid black;"><p>Auditores de CA</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Grupo administrativo que administra las copias de seguridad de CA.</p></td>
<td style="border:1px solid black;"><p>ca_setup.wsf</p></td>
<td style="border:1px solid black;"><p>Operadores de copia de seguridad de CA</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>Configuración de IIS</strong></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Nombre del directorio virtual de IIS que se utiliza para publicar la información de los certificados de CA y las CRL.</p></td>
<td style="border:1px solid black;"><p>Pkiparams.vbs</p></td>
<td style="border:1px solid black;"><p>pki</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Ruta física de la CA emisora asignada al directorio virtual de IIS.</p></td>
<td style="border:1px solid black;"><p>C:\CAWWWPub</p></td>
<td style="border:1px solid black;"><p>Pkiparams.vbs</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>Parámetros de CA comunes</strong></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Unidad y ruta de los archivos de petición de Servicios de Certificate Server</p></td>
<td style="border:1px solid black;"><p>C:\CAConfig</p></td>
<td style="border:1px solid black;"><p>Pkiparams.vbs</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Unidad y ruta de los registros de base de datos de Servicios de Certificate Server.</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>%windir%\System32\CertLog</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>Configuración de la CA raíz</strong></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Longitud de la clave de la CA raíz (véase la nota)</p></td>
<td style="border:1px solid black;"><p>4096</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Período de validez del certificado de la CA raíz (años)</p></td>
<td style="border:1px solid black;"><p>Pkiparams.vbs</p></td>
<td style="border:1px solid black;"><p>16</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Período de validez máximo de los certificados emitidos por la CA raíz (años)</p></td>
<td style="border:1px solid black;"><p>Pkiparams.vbs</p></td>
<td style="border:1px solid black;"><p>8</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Intervalo de publicación de la CRL de la CA raíz (meses)</p></td>
<td style="border:1px solid black;"><p>Pkiparams.vbs</p></td>
<td style="border:1px solid black;"><p>6</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Período de superposición de la CRL (días)</p></td>
<td style="border:1px solid black;"><p>Pkiparams.vbs</p></td>
<td style="border:1px solid black;"><p>10</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Período de publicación de la CRL Delta (horas, 0=deshabilitado)</p></td>
<td style="border:1px solid black;"><p>Pkiparams.vbs</p></td>
<td style="border:1px solid black;"><p>0</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p><strong>Configuración de la CA emisora</strong></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Unidad y ruta de la base de datos de Servicios de Certificate Server</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>D:\CertLog</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Longitud de la clave de la CA emisora</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>2048</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Período de validez del certificado de la CA emisora (años)</p></td>
<td style="border:1px solid black;"><p>Pkiparams.vbs</p></td>
<td style="border:1px solid black;"><p>8</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Período de validez máximo de los certificados de la CA emisora (años)</p></td>
<td style="border:1px solid black;"><p>Pkiparams.vbs</p></td>
<td style="border:1px solid black;"><p>4</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Intervalo de publicación de la CRL de la CA emisora (días)</p></td>
<td style="border:1px solid black;"><p>Pkiparams.vbs</p></td>
<td style="border:1px solid black;"><p>7</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Período de superposición de la CRL (días)</p></td>
<td style="border:1px solid black;"><p>Pkiparams.vbs</p></td>
<td style="border:1px solid black;"><p>4</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Período de publicación de la CRL Delta de la CA emisora (días, 0=deshabilitado)</p></td>
<td style="border:1px solid black;"><p>Pkiparams.vbs</p></td>
<td style="border:1px solid black;"><p>1</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Período de superposición de la CRL Delta (días)</p></td>
<td style="border:1px solid black;"><p>Pkiparams.vbs</p></td>
<td style="border:1px solid black;"><p>1</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p><strong>Varios</strong></p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Ruta de los scripts de instalación</p></td>
<td style="border:1px solid black;"><p> </p></td>
<td style="border:1px solid black;"><p>C:\MSSScripts</p></td>
</tr>  
</tbody>  
</table>
  
**Nota**   Si algunos dispositivos o software antiguo de otros proveedores utilizan claves de una longitud de 4.096 bits, pueden surgir problemas de compatibilidad. Es necesario comprobar con claves de certificado de este tamaño todas las aplicaciones que puedan utilizar certificados emitidos por la CA raíz para asegurarse de que funcionan correctamente. La longitud de la clave de la CA raíz puede reducirse a 2.048 bits si surgen problemas de compatibilidad con la longitud de la clave.
  
###### Instalación de los scripts de configuración en los servidores de CA
  
Los scripts auxiliares que se suministran con esta guía están diseñados para ayudarle a configurar la solución proporcionada en las siguientes secciones. Estos scripts se deben instalar en todos los servidores de CA y no se deben eliminar después de su uso puesto que ayudan a su funcionamiento. Para instalar estos scripts, cree en primer lugar una carpeta denominada C:\\MSSScripts y, a continuación, copie los scripts en ese directorio.
  
###### Instalación y configuración de IIS en el servidor de la CA emisora
  
Los Servicios de Internet Information Server (IIS) se utilizan como punto de descarga para los clientes no basados en Windows con el fin de recuperar los certificados de CA y las CRL. La CA raíz no necesita ofrecer este servicio, básicamente porque se supone que no está conectada a una red, pero la CA emisora sí debe tener acceso a este servicio.
  
IIS también se puede utilizar para alojar las páginas web de inscripción de Servicios de Certificate Server, aunque no se usen en esta solución. Si las páginas web de inscripción están instaladas en un sistema distinto al de la CA emisora, dicho servidor debe estar marcado como “Se confía para delegación”. Para ello, es necesario configurar esa propiedad en el objeto de equipo del servidor en Active Directory.
  
IIS se puede instalar con el administrador de componentes opcionales de Windows, disponible a través de la opción Agregar o quitar componentes de Windows del Panel de control. La siguiente lista muestra los componentes que es necesario instalar:
  
-   Servidor de aplicaciones
  
-   Habilitar el acceso de red COM+
  
-   Servicios de Internet Information Server
  
-   Archivos comunes
  
-   Administrador de Servicios de Internet Information Server
  
-   Servicio World Wide Web
  
**Para instalar IIS**
  
1.  Ejecute lo siguiente en un símbolo del sistema:
  
    ```  
 Sysocmgr /i:sysoc.inf /u:C:\\MSSScripts\\OC\_AddIIS.txt   
```
  
    Este comando indica al administrador de componentes opcionales que debe utilizar las configuraciones de componentes especificadas en el archivo de instalación desatendida C:\\MSSScripts\\OC\_AddIIS.txt, tal como se muestra a continuación:
  
    ```  
 \[Components\] complusnetwork = On iis\_common = On iis\_asp = On iis\_inetmgr = On iis\_www = On   
```
  
    **Nota**    Las páginas Active Server (ASP) están habilitadas en este archivo de configuración; sin embargo, si no se necesitan las páginas web de inscripción de Servicios de Certificate Server, ASP se debe deshabilitar. Para ello, elimine la línea **iis\_asp = on** antes de ejecutar sysocmgr.exe. Este parámetro se puede habilitar posteriormente si es necesario.
  
2.  Ejecute de nuevo el administrador de componentes opcionales como se indica a continuación y compruebe que los componentes instalados coinciden con los enumerados anteriormente.
  
    ```  
 sysocmgr /i:sysoc.inf   
```
  
    No se necesitan otros subcomponentes del Servidor de aplicaciones, por lo que no es necesario seleccionarlo.
  
Configuración de IIS para la publicación de AIA y CDP de CRL en la CA emisora  
Se debe crear un directorio virtual en IIS para utilizarlo como la ubicación HTTP de los puntos de publicación de los certificados de CA y las CRL, que se conocen como AIA (Acceso a la información de entidad emisora) y CDP (Punto de distribución de CRL), respectivamente.
  
**Para crear un directorio virtual en IIS**
  
1.  Inicie sesión en el servidor IIS con privilegios de administrador local.
  
2.  Cree una carpeta denominada **C:\\CAWWWPub** para almacenar en ella los certificados de CA y las CRL.
  
3.  Configure la seguridad de la carpeta según se indica en la siguiente tabla:
  
    **Tabla 9. Permisos del directorio virtual**

<p> </p>
    <table style="border:1px solid black;">  
    <colgroup>  
    <col width="33%" />  
    <col width="33%" />  
    <col width="33%" />  
    </colgroup>  
    <thead>  
    <tr class="header">  
    <th><p>Usuario o grupo</p></th>  
    <th><p>Permiso</p></th>  
    <th><p>Permitir o denegar</p></th>  
    </tr>  
    </thead>  
    <tbody>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>Administradores</p></td>
    <td style="border:1px solid black;"><p>Control total</p></td>
    <td style="border:1px solid black;"><p>Permitir</p></td>
    </tr>  
    <tr class="even">
    <td style="border:1px solid black;"><p>Sistema</p></td>
    <td style="border:1px solid black;"><p>Control total</p></td>
    <td style="border:1px solid black;"><p>Permitir</p></td>
    </tr>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>Propietarios del creador</p></td>
    <td style="border:1px solid black;"><p>Control total (sólo subcarpetas y archivos)</p></td>
    <td style="border:1px solid black;"><p>Permitir</p></td>
    </tr>  
    <tr class="even">
    <td style="border:1px solid black;"><p>Usuarios</p></td>
    <td style="border:1px solid black;"><p>Leer y Mostrar el contenido de la carpeta</p></td>
    <td style="border:1px solid black;"><p>Permitir</p></td>
    </tr>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>IIS_WPG</p></td>
    <td style="border:1px solid black;"><p>Leer y Mostrar el contenido de la carpeta</p></td>
    <td style="border:1px solid black;"><p>Permitir</p></td>
    </tr>  
    <tr class="even">
    <td style="border:1px solid black;"><p>Cuenta de invitado para Internet</p></td>
    <td style="border:1px solid black;"><p>Escribir</p></td>
    <td style="border:1px solid black;"><p>Denegar</p></td>
    </tr>  
    </tbody>  
    </table>
  
4.  Utilice la consola de administración de IIS para crear un nuevo directorio virtual en el sitio web predeterminado:
  
    -   Asigne al directorio virtual el nombre **pki**.
  
    -   Especifique la ruta **C:\\CAWWWPub**.
  
5.  Desactive la opción **Ejecutar secuencias de comandos** en los permisos de acceso al directorio virtual.
  
6.  Asegúrese de que se ha habilitado la autenticación anónima para el directorio virtual.
  
Selección de un alias DNS para el punto de publicación HTTP  
Se debe crear un alias DNS genérico (CNAME) para resolver el modo en el que el servidor IIS aloja CDP y AIA. Este alias DNS debe utilizarse al configurar las rutas de CDP y AIA para las CA en las secciones posteriores. Si se utilizan alias, los puntos de publicación de CA se pueden mover fácilmente a otros servidores o ubicaciones de red sin que sea necesario volver a emitir los certificados de CA.
  
###### Otros elementos de configuración y componentes del sistema operativo
  
Además de los pasos de configuración descritos hasta ahora, hay otros elementos recomendados que requieren atención, entre los que se incluyen:
  
-   Servicio de actualización de certificados raíz. El servicio de actualización de certificados raíz debe estar deshabilitado, ya que no es recomendable que se actualice automáticamente la confianza de la raíz de las CA. Para quitar este servicio, ejecute lo siguiente en un símbolo del sistema:
  
    ```  
 sysocmgr /i:sysoc.inf /u:C:\\MSSScripts\\OC\_RemoveRootUpdate.txt   
```
  
    El archivo OC\_RemoveRootUpdate.txt contiene las siguientes líneas:
  
    ```  
 \[Componentes\] rootautoupdate = off   
```
  
-   Asegúrese de que la CA raíz no tiene conectividad de red y de que la CA emisora no tiene conectividad de entrada ni de salida a Internet.
  
-   Compruebe si se necesitan Service Pack y actualizaciones adicionales debido a la instalación de IIS.
  
-   Instale las herramientas de soporte de Windows Server 2003. Aunque no son necesarias, es muy útil contar con estas herramientas para realizar ciertas operaciones de CA y solucionar problemas generales.
  
-   Instale CAPICOM. Es necesario que CAPICOM 2.1 se encuentre en la CA raíz y la CA emisora para algunos de los scripts de configuración y administración que se facilitan con esta guía. Para obtener más información sobre [CAPICOM](http://www.microsoft.com/downloads/details.aspx?familyid=860ee43a-a843-462f-abb5-ff88ea5896f6&displaylang=en) y un vínculo a la ubicación de descarga, vaya a la página http://www.microsoft.com/downloads/details.aspx?displaylang=es&FamilyID=860ee43a-a843-462f-abb5-ff88ea5896f6.
  
###### Preparación de Active Directory para la PKI
  
Los requisitos fundamentales que debe cumplir una infraestructura de dominio de Active Directory que se describen en esta sección se basan en una arquitectura de Microsoft Windows Server 2003 Active Directory. Si la implementación de Active Directory en uso se basa en Windows 2000, es posible que los requisitos sean diversos. Para obtener más información sobre los requisitos adicionales de una estructura de dominio basada en Windows 2000, consulte el artículo [Cómo elevar los niveles funcionales de dominio y bosque en Windows Server 2003](http://support.microsoft.com/kb/322692) en http://support.microsoft.com/kb/322692.
  
Esta solución también exige un nivel funcional mínimo de dominio en el modo nativo de Windows 2000, al menos para el dominio en el que se van a instalar los servidores de CA. Este requisito existe porque la solución utiliza grupos universales de Active Directory, que están disponibles en el modo nativo de Windows 2000 y posteriores.
  
Creación de la PKI y los grupos de administración de CA  
Esta solución define varios grupos de seguridad que se corresponden con funciones administrativas independientes. Este enfoque proporciona un alto grado de control sobre la delegación de la administración de CA si se utiliza junto con principios de seguridad de menos privilegios. Sin embargo, no hay ningún otro motivo que exija su utilización si no se corresponden con un determinado modelo administrativo de la organización.
  
**Para crear grupos de administración de CA en un dominio**
  
1.  Inicie sesión en un equipo miembro del dominio con una cuenta con permisos para crear objetos de usuario y grupo en el contenedor Usuarios.
  
2.  Ejecute el siguiente comando para crear los grupos de administración de CA del dominio:
  
    ```  
 Cscript //job:CertDomainGroups C:\\MSSScripts\\ca\_setup.wsf   
```
  
    Este script creará los grupos de seguridad que se indican en la siguiente tabla. Estos grupos se crean como grupos universales en el contenedor Usuarios del dominio y se pueden mover a una unidad organizativa más adecuada si así lo requiere cualquier directiva vigente de la organización.
  
    **Tabla 10. Nombres y funciones de los grupos**

<p> </p>
    <table style="border:1px solid black;">  
    <colgroup>  
    <col width="50%" />  
    <col width="50%" />  
    </colgroup>  
    <thead>  
    <tr class="header">  
    <th><p>Nombre del grupo</p></th>  
    <th><p>Función</p></th>  
    </tr>  
    </thead>  
    <tbody>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>Administradores de PKI de empresa</p></td>
    <td style="border:1px solid black;"><p>Administradores del contenedor de configuración Servicios de clave pública.</p></td>
    </tr>  
    <tr class="even">
    <td style="border:1px solid black;"><p>Publicadores de PKI de empresa</p></td>
    <td style="border:1px solid black;"><p>Pueden publicar CRL y certificados de CA en el contenedor de configuración Empresa.</p></td>
    </tr>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>Administradores de CA</p></td>
    <td style="border:1px solid black;"><p>Tienen funciones administrativas completas sobre la CA, incluida la capacidad de determinar la pertenencia de otras funciones.</p></td>
    </tr>  
    <tr class="even">
    <td style="border:1px solid black;"><p>Administradores de certificados</p></td>
    <td style="border:1px solid black;"><p>Administran la emisión y revocación de certificados.</p></td>
    </tr>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>Auditores de CA</p></td>
    <td style="border:1px solid black;"><p>Administran los datos de auditoría de la CA.</p></td>
    </tr>  
    <tr class="even">
    <td style="border:1px solid black;"><p>Operadores de copia de seguridad de CA</p></td>
    <td style="border:1px solid black;"><p>Tienen permisos para hacer copias de seguridad y restauraciones de los datos y las claves de CA.</p></td>
    </tr>  
    </tbody>  
    </table>
  
Los procedimientos de configuración que se describen en el resto del documento requieren el uso de cuentas que sean miembro de Administradores de PKI de empresa, Publicadores de PKI de empresa y Administradores de CA. Por tanto, es necesario rellenar estos grupos con las cuentas adecuadas antes de continuar. Si sólo hay una persona responsable de todas las funciones relacionadas con CA, se puede asignar una sola cuenta a todos los grupos; sin embargo, en la mayoría de las empresas existe un cierto grado de separación de las funciones y tareas entre el personal, aunque no sea tan compleja como la que se indica en la tabla anterior. Para aquellas empresas con una separación simplificada de tareas, el siguiente gráfico ofrece las divisiones de responsabilidad más comunes.
  
**Tabla 11. Modelo de administración simplificado**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Función administrativa</p></th>  
<th><p>Pertenencia a grupos</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Administrador de CA</p></td>
<td style="border:1px solid black;"><p>Administradores de PKI de empresa, Administradores de CA, Administradores de certificados, Administradores</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Auditor de CA</p></td>
<td style="border:1px solid black;"><p>Auditores de CA, Administradores</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Operador de copia de seguridad de CA</p></td>
<td style="border:1px solid black;"><p>Operadores de copia de seguridad de CA</p></td>
</tr>  
</tbody>  
</table>
  
Estructura propuesta para las unidades organizativas del dominio  
Hay varias cuentas de usuario y grupos que se asociarán a la administración y operación de una PKI. En función de las directivas establecidas vigentes, puede que sea necesario organizar estos grupos y usuarios en una estructura de unidades organizativas específica. Como esta estructura puede regirse por instrucciones de la empresa ya existentes, a continuación se ofrece una propuesta de estructura que puede modificarse si es necesario.
  
**Para crear una jerarquía de unidades organizativas de Servicios de Certificate Server**
  
1.  Inicie sesión con una cuenta que tenga permisos para crear unidades organizativas y delegar permisos dentro de esas unidades organizativas.
  
2.  Cree una estructura de unidades organizativas que se base en lo indicado en la siguiente tabla:
  
    **Tabla 12. Ejemplo de estructura de unidades organizativas**

<p> </p>
    <table style="border:1px solid black;">  
    <colgroup>  
    <col width="50%" />  
    <col width="50%" />  
    </colgroup>  
    <thead>  
    <tr class="header">  
    <th><p>Unidad organizativa</p></th>  
    <th><p>Función</p></th>  
    </tr>  
    </thead>  
    <tbody>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>Servicios de Certificate Server</p></td>
    <td style="border:1px solid black;"><p>Unidad organizativa principal</p></td>
    </tr>  
    <tr class="even">
    <td style="border:1px solid black;"><p>\-Administración de Servicios de Certificate Server</p></td>
    <td style="border:1px solid black;"><p>Contiene grupos administrativos para administrar las CA y la configuración de la PKI de empresa.</p></td>
    </tr>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>\-Administración de plantillas de certificados</p></td>
    <td style="border:1px solid black;"><p>Contiene grupos para administrar las plantillas de certificados individuales.</p></td>
    </tr>  
    <tr class="even">
    <td style="border:1px solid black;"><p>\-Inscripción de plantillas de certificados</p></td>
    <td style="border:1px solid black;"><p>Contiene grupos que tienen permisos de inscripción o inscripción automática de las plantillas con el mismo nombre. El control de estos grupos se puede delegar al personal adecuado sin modificar las propias plantillas.</p></td>
    </tr>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>\-Usuarios de prueba de Servicios de Certificate Server</p></td>
    <td style="border:1px solid black;"><p>Contiene cuentas de prueba temporales.</p></td>
    </tr>  
    </tbody>  
    </table>
  
3.  Conceda permisos al grupo Administradores de PKI de empresa para crear y eliminar grupos de la unidad organizativa de Servicios de Certificate Server y sus contenedores secundarios.
  
Concesión de permisos al contenedor Servicios de clave pública  
La seguridad del contenedor Servicios de clave pública debe modificarse para que los Administradores de PKI de empresa puedan instalar las CA de empresa y configurar las plantillas de certificados, sin que sea necesario que las cuentas de este grupo formen parte del grupo Administradores de empresa. También es necesario permitir a los Publicadores de PKI de empresa publicar listas de revocación de certificados y certificados de CA sin tener derechos de Administradores de empresa.
  
Para realizar los siguientes cambios, es necesario utilizar una cuenta equivalente a Administradores de empresa de Active Directory.
  
**Para conceder permisos al grupo Administradores de PKI de empresa**
  
1.  Inicie sesión como miembro del grupo de seguridad Administradores de empresa.
  
2.  En el complemento MMC de Sitios y servicios de Active Directory, expanda el nodo **Servicios** del menú **Ver** y, a continuación, busque el subcontenedor Servicios de clave pública y abra sus propiedades.
  
3.  En la ficha **Seguridad**, agregue el grupo de seguridad Administradores de PKI de empresa y conceda el permiso Control total a este grupo.
  
4.  En **Vista avanzada**, edite los permisos de este grupo para garantizar que se aplica el permiso Control total a este objeto y todos los objetos secundarios.
  
5.  Seleccione el contenedor **Servicios** y abra sus propiedades.
  
6.  En la ficha **Seguridad**, agregue el grupo de seguridad Administradores de PKI de empresa y conceda el permiso Control total a este grupo.
  
7.  En **Vista avanzada**, edite los permisos de este grupo para garantizar que se aplica el permiso Control total sólo a este objeto.
  
**Para conceder permisos al grupo Publicadores de PKI de empresa**
  
1.  Inicie sesión como miembro del grupo de seguridad Administradores de empresa.
  
2.  En el complemento MMC de Sitios y servicios de Active Directory, expanda el nodo **Servicios** y abra las propiedades del contenedor Servicios de clave pública\\AIA.
  
3.  En la ficha **Seguridad**, agregue el grupo de seguridad Publicadores de PKI de empresa y conceda los siguientes permisos a este grupo:
  
    -   Leer
  
    -   Escribir
  
    -   Crear todos los objetos secundarios
  
    -   Eliminar todos los objetos secundarios
  
4.  En **Vista avanzada**, edite los permisos de este grupo para garantizar que se aplican los permisos a este objeto y a todos los objetos secundarios.
  
5.  Repita los pasos del 2 al 4 para los siguientes contenedores:
  
    -   Servicios de clave pública\\CDP
  
    -   Servicios de clave pública\\Entidades de certificación
  
Concesión de permisos al grupo Publicadores de certificados  
Todas las cuentas de equipos de CA de empresa del dominio residirán en el grupo de seguridad Publicadores de certificados. Este grupo se utilizará para aplicar permisos a los objetos de usuario y equipo, así como a los objetos del contenedor CDP que se han mencionado en el procedimiento anterior. Siempre que se instale una CA, se deberá agregar la cuenta de equipo a este grupo.
  
Para permitir que los miembros del grupo Administradores de PKI de empresa instalen CA de empresa, se deben cambiar los permisos de este grupo.
  
**Para conceder permisos para modificar la pertenencia a grupos al grupo Publicadores de certificados**
  
1.  Inicie sesión como miembro del grupo Administradores de dominio para el dominio en el que se van a instalar las CA emisoras.
  
2.  Abra el complemento MMC de Usuarios y equipos de Active Directory.
  
3.  En el menú **Ver** de MMC, asegúrese de seleccionar **Características avanzadas**.
  
4.  Busque el grupo Publicadores de certificados (de forma predeterminada, en el contenedor Usuarios) y vea las propiedades del grupo.
  
5.  En la ficha **Seguridad**, agregue el grupo Administradores de PKI de empresa y haga clic en el botón **Configuración avanzada**.
  
6.  Seleccione el grupo Administradores de PKI de empresa en la lista y haga clic en el botón **Modificar**.
  
7.  Seleccione la ficha **Propiedades** y asegúrese de activar la opción **Sólo este objeto** en el cuadro **Aplicar en**.
  
8.  Desplácese hacia abajo y haga clic en el cuadro **Escribir miembros** y, a continuación, en la columna **Permitir**.
  
9.  Guarde los cambios y cierre los cuadros de diálogo. Para ello, haga clic en **Aceptar** en cada uno de los cuadros de diálogo.
  
10. Reinicie el servidor de la CA emisora antes de instalar el componente Servicios de Certificate Server. Al reiniciar, el servidor puede asumir la pertenencia al nuevo grupo en el token de acceso.
  
Concesión de permisos de restauración al grupo Administradores de PKI de empresa  
El proceso de instalación de Servicios de Certificate Server requiere el derecho de usuario Restaurar archivos y directorios en el dominio en el que se colocará la CA de empresa. En concreto, este derecho es necesario para permitir descriptores de seguridad en las plantillas y en otros de objetos de directorio que se van a combinar, y conceder de este modo los permisos correctos a los objetos de PKI del dominio. Los grupos integrados del dominio Administradores, Opers. de servidores y Operadores de copia de seguridad tienen este derecho de forma predeterminada.
  
Como el grupo Administradores de PKI de empresa se utilizará para instalar la CA, es necesario conceder el derecho de usuario Restaurar archivos y directorios a este grupo.
  
**Para conceder derechos de restauración al grupo Administradores de PKI de empresa**
  
1.  Inicie sesión como miembro del grupo Administradores de dominio en el dominio en el que se instalará la CA emisora.
  
2.  Abra el complemento MMC de Usuarios y equipos de Active Directory.
  
3.  Seleccione la unidad organizativa Controladores de dominio y abra las propiedades de dicha unidad organizativa.
  
4.  En la ficha **Directiva de grupo**, seleccione **GPO de Directiva predeterminada de controladores de dominio** y, a continuación, haga clic en **Editar**.
  
5.  Vaya a Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\Asignación de derechos de usuario y haga doble clic en **Restaurar archivos y directorios**.
  
6.  Agregue el grupo Administradores de PKI de empresa a la lista mostrada.
  
7.  Cierre el cuadro de diálogo y el MMC de edición del objeto de directiva de grupo (GPO).
  
    **Nota**   Si hay otros GPO que configuran el derecho de usuario Recuperar archivos y directorios en los controladores de dominio, se debe llevar a cabo este procedimiento en el GPO con la máxima prioridad en lugar de en la directiva predeterminada de controladores de dominio. La configuración de los derechos de usuario no es acumulativa y sólo será válida en el último GPO aplicado que tenga configurado este derecho.
  
###### Implementación de un servidor de CA raíz
  
Como se ha mencionado con anterioridad, esta guía no ofrece instrucciones paso a paso para instalar Windows Server 2003, ya que la mayoría de las empresas ya tienen un proceso documentado de creación de servidores. Sin embargo, los servidores de CA raíz son en cierto modo distintos de otros servidores porque nunca se deben conectar a una red con el fin de garantizar que nunca se van a poner en peligro.
  
Por tanto, es importante asegurarse de que el servidor de CA raíz no está conectado a la red durante el proceso de creación, así como que los adaptadores de red están deshabilitados en un determinado momento para garantizar que no se realice nunca una conexión por error. También es importante tener en cuenta que, puesto que el servidor no se conectará a la red, residirá en un grupo de trabajo cuyo nombre se debe seleccionar y documentar antes de la instalación.
  
**Nota**   Aunque la CA raíz se cree y se mantenga desconectada, es importante que su nombre sea único en el entorno de red.
  
Archivo CAPolicy.inf  
Después de hacerse con el hardware de servidor necesario para el servidor de CA raíz y de instalar el sistema operativo, el siguiente paso debe ser la creación de un archivo capolicy.inf. El archivo capolicy.inf se necesita para crear una CA raíz porque especifica características del certificado autofirmado de la CA raíz, como la longitud de la clave y el período de validez del certificado.
  
La información de CRL y AIA no se necesita para un certificado de CA raíz, por lo que los parámetros CRLDistributionPoint y AuthorityInformationAccess se configuran como Empty en el archivo capolicy.inf.
  
**Para crear un archivo CAPolicy.inf**
  
1.  Mediante un editor de texto, como el Bloc de notas, cree un archivo de texto sin formato que incluya el siguiente texto:
  
    ```  
 \[version\] Signature=”$Windows NT$” \[Certsrv\_server\] RednewalKeyLength=4096 RenewalValidityPeriod=Years RenewalValidityPeriodUnits=16 \[CRLDistributionPoint\] Empty=true \[AuthorityInformationAccess\] Empty=true   
```
  
2.  Si esta CA tiene definida una declaración de prácticas de certificación (CPS), incluya el siguiente texto en el archivo capolicy.inf y sustituya los valores en cursiva por los específicos de esta implementación:
  
    ```  
 \[CAPolicy\] Policies=nombre de la CPS de la empresa \[nombre de la CPS de la empresa\] OID=OID.de.la.empresa URL=”http://www.urlDeLaEmpresa.com/nombreDeLaPáginaDeCps.htm”   
```
  
3.  Guarde este archivo de texto como *%windir%*\\Capolicy.inf (sustituya *%windir%* por la ruta absoluta de la carpeta en la que está instalado Windows; por ejemplo, C:\\Windows). Para realizar este paso, se debe utilizar la cuenta del administrador o una cuenta con permisos equivalentes para guardar el archivo en la carpeta de Windows.
  
Instalación de los componentes de software de Servicios de Certificate Server  
Utilice el Asistente para componentes de Windows para instalar los componentes de software de CA. Tenga en cuenta que los medios de instalación de Windows Server 2003 deben ser accesibles para que se pueda realizar la instalación.
  
**Para instalar Servicios de Certificate Server**
  
1.  Inicie sesión como miembro del grupo local Administradores y ejecute el administrador de componentes opcionales o, en el Panel de control, abra Agregar o quitar programas o bien Agregar o quitar componentes de Windows.
  
    ```  
 sysocmgr /i:sysoc.inf   
```
  
2.  Seleccione el componente Servicios de Certificate Server (haga clic en **Sí** para omitir la advertencia de cambio de nombre).
  
3.  Seleccione **Entidad emisora de certificados raíz independiente** como tipo de CA y asegúrese de activar la casilla **Usar la configuración personalizada**.
  
4.  Deje los valores predeterminados en el cuadro de diálogo **Pareja de claves pública y privada**, excepto en los campos **Longitud de la clave**, que debe configurarse como **4096**, y **Tipo de proveedor de servicios de cifrado**, que debe establecerse como **Microsoft Strong Cryptographic Provider**.
  
5.  Especifique la información de identificación de la entidad de certificación, tal como se ha recopilado en la fase de requisitos, en los siguientes campos:
  
    -   Nombre común para esta entidad emisora de certificados:
  
    -   Sufijo de nombre completo:
  
    -   Período de validez: 8 años
  
    En este momento, el proveedor de servicios de cifrado (CSP) genera el par de claves y las escribe en el almacén de claves del equipo local.
  
    **Nota**   Si se instaló una CA previamente en el sistema, aparecerá un cuadro de diálogo para advertirle de que se puede sobrescribir la clave privada de la instalación anterior. Antes de continuar, asegúrese de que no va a volver a necesitar esta clave.
  
6.  Deje los valores predeterminados para las ubicaciones de la base de datos de certificados, los registros de la base de datos y la carpeta de configuración. En ese momento, el administrador de componentes opcionales instalará los componentes de Servicios de Certificate Server y se necesitarán los medios de instalación de Windows Server 2003.
  
7.  Haga clic en **Aceptar** para rechazar las advertencias sobre IIS y continúe la instalación hasta que finalice.
  
Configuración de las propiedades de la CA raíz  
Al configurar la CA raíz, se utilizarán varios parámetros específicos del entorno, tal como se describe en esta sección. Antes de continuar, se deben haber recopilado estos parámetros tal como se ha descrito anteriormente en la sección de información necesaria de esta guía.
  
**Para configurar las propiedades de la CA raíz**
  
1.  Inicie sesión en el servidor de CA como miembro del grupo local Administradores.
  
2.  Personalice el script C:\\MSSScripts\\pkiparams.vbs de modo que incluya lo siguiente:
  
    -   Cambie el valor del parámetro AD\_ROOT\_DN para que coincida con el DN del dominio raíz del bosque de Active Directory.
  
    -   Cambie el parámetro HTTP\_PKI\_VROOT para que coincida con la ruta HTTP de acceso al directorio virtual de IIS configurado anteriormente.
  
3.  Ejecute el siguiente script:
  
    ```  
 Cscript //job:RootCAConfig C:\\MSSScripts\\ca\_setup.wsf   
```
  
Configuración de las funciones administrativas  
Es necesario asignar los grupos de seguridad creados anteriormente a las funciones administrativas, como auditor y administrador de certificados, que se vayan a utilizar.
  
**Nota**   Aunque la mayoría de las medianas empresas probablemente utilicen el modelo de delegación simplificado que se ha mencionado anteriormente en esta guía, aquí se muestra un modelo más flexible por si se necesita una separación de funciones mayor.
  
**Para configurar las funciones administrativas de una CA raíz**
  
1.  En la Consola de administración de entidades de certificación, haga clic en **Propiedades**.
  
2.  Haga clic en la ficha **Seguridad** y agregue los grupos de seguridad locales que figuran en la siguiente tabla, además del permiso mostrado para cada uno de ellos.
  
    **Tabla 13. Entradas de permiso de CA**

<p> </p>
    <table style="border:1px solid black;">  
    <colgroup>  
    <col width="33%" />  
    <col width="33%" />  
    <col width="33%" />  
    </colgroup>  
    <thead>  
    <tr class="header">  
    <th><p>Grupo</p></th>  
    <th><p>Permiso</p></th>  
    <th><p>Permitir o denegar</p></th>  
    </tr>  
    </thead>  
    <tbody>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>Administradores de CA</p></td>
    <td style="border:1px solid black;"><p>Administrar entidad emisora</p></td>
    <td style="border:1px solid black;"><p>Permitir</p></td>
    </tr>  
    <tr class="even">
    <td style="border:1px solid black;"><p>Administradores de certificados</p></td>
    <td style="border:1px solid black;"><p>Emitir y administrar certificados</p></td>
    <td style="border:1px solid black;"><p>Permitir</p></td>
    </tr>  
    </tbody>  
    </table>
  
3.  Otras funciones de seguridad de CA ya se han definido para este servidor mediante la directiva de seguridad aplicada anteriormente.
  
Transferencia del certificado y la CRL de la CA raíz al disco  
El certificado y la CRL de la CA raíz deben copiarse de la CA para que se puedan publicar en Active Directory y en el servidor de publicación de certificados IIS y CRL. Aunque en este ejemplo se menciona el uso de un disco, se puede utilizar cualquier medio portátil, incluidas las unidades USB.
  
**Para copiar el certificado y la CRL de la CA raíz en el disco**
  
1.  Inicie sesión en la CA raíz como miembro del grupo local Administradores de CA e inserte el medio portátil en el servidor.
  
2.  Ejecute el siguiente script para copiar el certificado de CA en el disco:
  
    ```  
 Cscript //job:GetCACerts C:\\MSSScripts\\CA\_Operations.wsf   
```
  
3.  Ejecute el siguiente script para copiar la CRL de CA en el disco:
  
    ```  
 Cscript //job:GetCRLs C:\\MSSScripts\\CA\_Operations.wsf   
```
  
4.  Etiquete, feche y conserve este disco para futuros usos.
  
###### Publicación de la información de la CA raíz
  
Antes de instalar la CA emisora, es necesario publicar el certificado de la CA raíz en el almacén raíz de confianza de Active Directory, y la CRL raíz, en el contenedor CDP de Active Directory. Este proceso provocará que todos los miembros del dominio importen el certificado de la CA raíz en sus propios almacenes raíz de confianza, lo que les permitirá comprobar el estado de revocación de los certificados emitidos por la CA raíz.
  
Se recomienda utilizar la CA emisora para realizar este procedimiento, ya que tiene instalados los archivos y las bibliotecas Certutil.exe, certadm.dll y certcli.dll necesarios. No obstante, se puede utilizar cualquier servidor miembro que tenga instalados el archivo certutil.exe y los archivos DLL auxiliares en el sistema basado en Windows Server 2003.
  
**Para publicar el certificado y la CRL de la CA raíz en Active Directory**
  
1.  Inicie sesión en un equipo miembro del dominio que cumpla los requisitos indicados anteriormente como miembro del grupo Administradores de PKI de empresa e inserte el disco creado para almacenar el certificado y la CRL de la CA raíz.
  
2.  Ejecute la siguiente secuencia de comandos para publicar el certificado de la CA en Active Directory:
  
    ```  
 Cscript //job:PublishCertstoAD C:\\MSSScripts\\CA\_Operations.wsf   
```
  
3.  Ejecute la siguiente secuencia de comandos para publicar la CRL en Active Directory:
  
    ```  
 Cscript //job:PublishCRLstoAD C:\\MSSScript\\CA\_Operations.wsf   
```
  
Publicación del certificado y la CRL de la CA raíz en el servidor web  
Es necesario realizar esta tarea porque las versiones de HTTP de las URL de CDP y AIA están especificadas en las extensiones de los certificados emitidos por esta CA. Si estas extensiones están presentes, las CRL y los certificados que se publiquen deben incluirlas en las URL configuradas.
  
**Nota**   Este procedimiento no depende de si el servidor web de publicación de CDP y AIA se encuentra en la CA emisora. Sin embargo, se considera que el directorio virtual coincide con el establecido anteriormente para configurar IIS (C:\\CAWWWPub). Si se seleccionó otra ruta, será necesario modificar el valor WWW\_LOCAL\_PUB\_PATH en el script PKIParams.vbs.
  
**Para publicar el certificado y la CRL de la CA raíz en la URL del servidor web**
  
1.  Inicie sesión en el servidor web como administrador local o con una cuenta equivalente.
  
2.  Asegúrese de insertar el disco que contiene el certificado y la CRL de la CA raíz.
  
3.  Ejecute el siguiente script para publicar el certificado de la CA en la carpeta del servidor web:
  
    ```  
 Cscript //job:PublishRootCerttoIIS C:\\MSSScripts\\CA\_Operations.wsf   
```
  
4.  Ejecute el siguiente script para publicar las CRL de la CA en la carpeta del servidor web:
  
    ```  
 Cscript //job:PublishRootCRLstoIIS C:\\MSSScripts\\CA\_Operations.wsf   
```
  
###### Implementación del servidor de la CA emisora
  
Una vez instalada la CA raíz y publicados los certificados correspondientes, se puede implementar el servidor de la CA emisora. La instalación de Servicios de Certificate Server conlleva un complejo conjunto de interacciones entre la CA emisora, la CA raíz, Active Directory y el servidor web. Es posible que sea más sencillo comprender estas interacciones si se utiliza el siguiente diagrama como referencia.
  
[![](images/Cc875845.SWCG5(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875845.swcg5_big(es-es,technet.10).gif)
  
**Figura 5. Proceso de instalación de certificados**
  
Las interacciones numeradas que aparecen en este diagrama son:
  
1.  Publicar el certificado y la CRL de la CA raíz en Active Directory mediante medios extraíbles.
  
2.  Publicar el certificado y la CRL de la CA raíz en el servidor web mediante medios extraíbles.
  
3.  Instalar el software Servicios de Certificate Server, que genera una petición de certificado que tendrá que entregarse a la CA raíz mediante medios extraíbles y donde se emitirá un certificado basado en dicha petición.
  
4.  Instalar el certificado de la CA emisora correspondiente mediante medios extraíbles.
  
5.  Publicar el certificado y la CRL de la CA emisora en el servidor web.
  
    x.   Este paso se ejecuta automáticamente durante la rutina de instalación de la CA de empresa.
  
Preparación del archivo Capolicy.inf para la CA emisora  
Aunque la CA emisora no necesita el archivo CAPolicy.inf, éste es necesario si se debe cambiar el tamaño de la clave que utiliza la CA. Este archivo se debe crear antes de instalar la CA emisora, aunque posteriormente se pueda agregar otro y, a continuación, renovar el certificado de la CA, si es necesario.
  
**Para crear un archivo CAPolicy.inf**
  
1.  Inicie sesión en el servidor de la CA emisora con la cuenta local Administrador o con una cuenta equivalente.
  
2.  Utilice un editor de texto, como el Bloc de notas, para crear un archivo de texto sin formato que incluya la siguiente información:
  
    ```  
 \[Version\] Signature= “$Windows NT$” \[Certsrv\_Server\] RenewalKeyLength=2048   
```
  
3.  Si se define una CPS para esta CA, incluya las siguientes líneas en el archivo Capolicy.inf:
  
    ```  
 \[CAPolicy\] Policies=nombreDeLaDirectiva \[nombreDeLaDirectiva\] OID=OID.de.la.organización URL=”http://URL.de.la.organización/páginaDeCPS.htm”   
```
  
    **Nota**   Los elementos en cursiva se deben reemplazar por la información específica de la organización.
  
4.  Guarde el archivo como *%windir%*\\Capolicy.inf (reemplace *%windir%* por la ruta absoluta de la carpeta de instalación de Windows; por ejemplo, C:\\Windows).
  
Instalación de los componentes de software de Servicios de Certificate Server  
Al igual que en la instalación de Servicios de Certificate Server en la CA raíz, en este paso también será necesario usar los medios de instalación de Windows Server 2003 junto con el Asistente para componentes de Windows.
  
**Para instalar Servicios de Certificate Server**
  
1.  Inicie sesión en la CA emisora como miembro del grupo local Administradores o con una cuenta equivalente y ejecute el administrador de componentes opcional:
  
    ```  
 sysocmgr /i:sysoc.inf   
```
  
2.  Seleccione el componente Servicios de Certificate Server y haga clic en **Aceptar** para omitir el cuadro de mensaje de advertencia de cambio de nombre.
  
3.  Seleccione Entidad emisora subordinada de la empresa como tipo de CA y asegúrese de activar la casilla de verificación **Usar la configuración personalizada**.
  
4.  Deje los valores predeterminados en el cuadro de diálogo **Pareja de claves pública y privada**, excepto en los siguientes campos:
  
    -   Longitud de la clave: 2.048 bits
  
    -   Tipo de proveedor de servicios de cifrado: Microsoft Strong Cryptographic Provider
  
5.  Especifique la información de identificación de la entidad de certificación del siguiente modo:
  
    -   Nombre común para esta entidad emisora de certificados
  
    -   Sufijo de nombre completo
  
    -   Período de validez: (según lo determine la CA principal)
  
6.  En este momento, el proveedor de servicios de cifrado (CSP) generará un par de claves y las escribirá en el almacén de claves del equipo local.
  
7.  Especifique las ubicaciones de la base de datos de certificados, los registros de la base de datos y la configuración, tal como se propone a continuación:
  
    -   Base de datos de certificados: D:\\CertLog
  
    -   Registro de la base de datos de certificados: %windir%\\System32\\CertLog
  
    -   Carpeta compartida: Deshabilitada
  
    Los registros y la base de datos de la CA se deben almacenar en volúmenes físicamente independientes, siempre que sea posible, por motivos de rendimiento y resistencia. La base de datos de certificados y los registros de la base de datos deben residir en unidades locales con formato NTFS.
  
8.  Llegados a este punto, se genera un archivo de peticiones de certificados que debe copiarse en un disco. El administrador de componentes opcionales instalará a continuación los componentes de Servicios de Certificate Server que necesitan tener acceso a los medios de instalación de Windows Server 2003.
  
9.  Haga clic en **Aceptar** para omitir la advertencia sobre IIS y continúe con la instalación hasta que finalice. El Asistente para configuración mostrará el aviso de que, antes de continuar, se necesita un certificado de la CA principal.
  
Envío de la petición de certificado a la CA raíz  
En este momento, la petición de certificado de la CA emisora se debe enviar a la CA raíz para solicitarle que firme la petición y emita un certificado a la CA emisora.
  
**Para enviar la petición de certificado a la CA raíz**
  
1.  Inicie sesión en la CA raíz con la cuenta de un miembro del grupo Administradores de certificados.
  
2.  Asegúrese de que el disco utilizado para almacenar el archivo de la petición de certificado está insertado en la unidad.
  
3.  En el menú **Tareas de CA** de la Consola de administración de entidades de certificación, seleccione **Enviar solicitud nueva** y, a continuación, envíe la petición transferida desde la CA emisora.
  
4.  Busque el certificado que se acaba de emitir en el contenedor Certificados emitidos y ábralo.
  
5.  Compruebe que los detalles del certificado son correctos y, a continuación, exporte el certificado a un archivo. Para ello, haga clic en Copiar en archivo. Guarde este archivo en un disco como un archivo PKCS\#7 y seleccione la opción de incluir todos los posibles certificados en la cadena.
  
Actualización de la información del certificado en la CA emisora  
El certificado de la CA raíz ya se ha publicado en el almacén raíz de confianza de Active Directory y ahora es necesario comprobar que la CA emisora ha descargado esta información y ha colocado el certificado en su propio almacén raíz.
  
**Para actualizar y comprobar la información de confianza del certificado en la CA emisora**
  
1.  Inicie sesión en la CA emisora con la cuenta local Administrador o con una cuenta equivalente.
  
2.  Ejecute lo siguiente en un símbolo del sistema:
  
    ```  
 certutil –pulse   
```
  
    Este comando hará que la CA descargue la nueva información raíz de confianza del directorio y coloque el certificado de la CA raíz en su propio almacén raíz de confianza. Aunque este paso no es necesario, sirve para comprobar que los pasos de publicación anteriores se realizaron correctamente antes de continuar.
  
3.  Ejecute mmc.exe y agregue el complemento Certificados.
  
4.  Seleccione **Cuenta de equipo** como el almacén de certificados que desea administrar.
  
5.  Asegúrese de que el certificado de la CA raíz se encuentra en la carpeta Entidades emisoras de certificados raíz de confianza.
  
Instalación del certificado en la CA emisora  
La respuesta firmada de la CA raíz se ha creado como un paquete de certificados PKCS\#7 y está preparada para su instalación en la CA emisora. Para publicar el certificado de la CA en el almacén NTAuth de Active Directory, que identifica a la CA como una CA de empresa, es necesario instalar el certificado de la CA con una cuenta que sea miembro tanto del grupo Administradores de PKI de empresa como del grupo local Administradores en la CA emisora. El primer grupo tiene derechos para instalar el certificado de la CA en el directorio, y el segundo, para instalar el certificado en el servidor de la CA. Si se utiliza el modelo de administración simple mencionado anteriormente, la función Administradores de CA ya es miembro de ambos grupos.
  
**Para instalar el certificado de la CA emisora**
  
1.  Inicie sesión en la CA emisora con una cuenta que sea miembro tanto del grupo Administradores de PKI de empresa como del grupo local Administradores.
  
2.  Inserte el disco que contiene el certificado firmado emitido por la CA raíz.
  
3.  Seleccione **Instalar certificado** en el menú **Tareas de CA** en la Consola de administración de entidades de certificación para instalar el certificado de la CA emisora desde el disco.
  
    La CA debe iniciarse en este momento.
  
Configuración de las propiedades de la CA emisora  
Mediante el siguiente procedimiento se configurarán los parámetros específicos del entorno que se han recopilado en la sección de requisitos de la CA emisora. Antes de continuar con este paso, es importante asegurarse de que la información específica de la organización (recopilada en los pasos de requisitos) se ha insertado en el archivo C:\\MSSScripts\\pkiparams.vbs de la CA raíz y de que estos cambios también se han transferido a la CA emisora.
  
**Para configurar las propiedades de la CA emisora**
  
1.  Inicie sesión en el servidor de la CA emisora como miembro del grupo local Administradores.
  
2.  Compruebe que los cambios realizados en el archivo C:\\MSSScripts\\pkiparams.vbs coinciden con los valores específicos del entorno que se han descrito anteriormente en esta sección.
  
3.  Ejecute el siguiente script:
  
    ```  
 Cscript //job:IssCAConfig C:\\MSSScripts\\ca\_setup.wsf   
```
  
Configuración de las funciones administrativas de la CA emisora  
Para utilizar las funciones administrativas descritas en esta guía, es necesario asignarlas a grupos de seguridad. Como se ha mencionado anteriormente, aunque las funciones simplificadas sean suficientes para la mayoría de las medianas empresas, con este proceso se implementarán funciones detalladas para ofrecer una flexibilidad máxima y una separación de responsabilidades.
  
**Para configurar funciones en la CA emisora**
  
1.  Inicie sesión en el servidor de la CA emisora como miembro del grupo local Administradores.
  
2.  Haga clic en Propiedades en la Consola de administración de entidades de certificación para editar las propiedades de la CA.
  
3.  Haga clic en la ficha **Seguridad** y agregue los grupos de seguridad de dominio que figuran en la siguiente tabla, así como los permisos mostrados para cada uno de ellos.
  
    **Tabla 14. Permisos de la CA emisora**

<p> </p>
    <table style="border:1px solid black;">  
    <colgroup>  
    <col width="33%" />  
    <col width="33%" />  
    <col width="33%" />  
    </colgroup>  
    <thead>  
    <tr class="header">  
    <th><p>Grupo</p></th>  
    <th><p>Permiso</p></th>  
    <th><p>Permitir o denegar</p></th>  
    </tr>  
    </thead>  
    <tbody>  
    <tr class="odd">
    <td style="border:1px solid black;"><p>Administradores de CA</p></td>
    <td style="border:1px solid black;"><p>Administrar entidad emisora</p></td>
    <td style="border:1px solid black;"><p>Permitir</p></td>
    </tr>  
    <tr class="even">
    <td style="border:1px solid black;"><p>Administradores de certificados</p></td>
    <td style="border:1px solid black;"><p>Emitir y administrar certificados</p></td>
    <td style="border:1px solid black;"><p>Permitir</p></td>
    </tr>  
    </tbody>  
    </table>
  
4.  El grupo Auditores de CA se debe agregar al grupo local Administradores, aunque este grupo ya se haya definido de forma parcial mediante la directiva de seguridad aplicada anteriormente.
  
###### Publicación de la información de la CA emisora
  
Aunque los certificados y las CRL se publican automáticamente desde la CA emisora en Active Directory, no ocurre así con la publicación del certificado de CA y las CRL en las rutas HTTP de CDP y AIA. Para automatizar la publicación del certificado de CA en las rutas HTTP de CDP y AIA, debe existir un trabajo programado que realice esa tarea.
  
Los certificados de CA se actualizan en raras ocasiones, por lo que se pueden publicar en AIA de forma manual si se sigue el siguiente proceso.
  
**Para publicar el certificado de la CA emisora**
  
1.  Inicie sesión en la CA emisora con una cuenta que tenga permisos de escritura en la carpeta del servidor web de publicación.
  
2.  Actualice el parámetro WWW\_REMOTE\_PUB\_PATH del archivo C:\\MSSScripts\\PKIParams.vbs para que coincida con la ruta de destino de la carpeta del servidor web.
  
    1.  Si el servidor web se encuentra en un servidor remoto, asegúrese de que la carpeta del servidor web está compartida y registre esa ruta UNC para la carpeta compartida.
  
    2.  Si el servidor web se encuentra en el mismo servidor que la CA, registre la ruta local a esa carpeta (el valor predeterminado es la ruta local C:\\CAWWWPub).
  
3.  Ejecute el siguiente script para publicar el certificado de CA en el servidor web:
  
    ```  
 Cscript //job:PublishIssCertsToIIS C:\\MSSScripts\\CA\_Operations.wsf   
```
  
    **Nota**   Este procedimiento se ha diseñado para servidores web internos. Si los certificados se van a publicar en un servidor web de Internet, será necesario llevar a cabo pasos adicionales porque esta solución se basa en el uso compartido de archivos de la red de Windows, que suele estar bloqueado en los firewall para Internet.
  
Las CRL se publican con más frecuencia que los certificados de CA, por lo que es necesario utilizar un método automático para publicarlas en el servidor web.
  
**Para automatizar la publicación de las CRL**
  
1.  Inicie sesión en la CA emisora con una cuenta que sea miembro del grupo local Administradores.
  
2.  Asegúrese de que la carpeta del servidor web es accesible desde este servidor.
  
3.  Si el servidor web es remoto, la CA emisora necesitará disponer de acceso con permiso de escritura a la carpeta del sistema de archivos (permitir Modificar acceso) y al recurso compartido (permitir Cambiar acceso). Si el servidor web remoto es miembro del bosque, se debe utilizar el grupo Publicadores de certificados para conceder acceso con el fin de garantizar que cualquier CA de empresa puede publicar certificados y CRL.
  
4.  Cree un trabajo programado para copiar las CRL. Para ello, ejecute el siguiente comando:
  
    **Nota**   Algunas partes del siguiente fragmento de código se han dispuesto en varias líneas únicamente para facilitar su lectura. Deben especificarse en una sola línea.
  
    ```  
 schtasks /creat /tn “Publish CRLs” /tr “cscript.exe //job:PublishIssCRLsToIIS C:\\ MSSScripts\\CA\_Operations.wsf” /sc Hourly /ru “System”   
```
  
Eliminación de plantillas no deseadas de la CA emisora  
Suele ser una práctica recomendada quitar las plantillas correspondientes a cualquier tipo de certificado que no se va a utilizar para que no se puedan emitir por error. Estas plantillas se pueden volver a crear fácilmente si es necesario, ya que siempre están disponibles en el directorio.
  
**Para quitar plantillas no deseadas de la CA emisora**
  
1.  Inicie sesión como miembro del grupo de dominio Administradores de CA.
  
2.  Seleccione el contenedor Plantillas de certificado en la Consola de administración de entidades de certificación.
  
3.  Quite los siguientes tipos de plantilla:
  
    -   Agente de recuperación de EFS
  
    -   EFS básico
  
    -   Servidor Web
  
    -   Equipo
  
    -   Usuario
  
    -   Entidad emisora de certificados subordinada
  
    -   Administrador
  
##### Autenticación de Internet
  
Esta sección incluye información detallada que le ayudará a implementar una infraestructura RADIUS compatible con la solución WLAN segura proporcionada en esta guía. La infraestructura RADIUS implementada en esta guía se basa en el Servicio de autenticación Internet (IAS) de Windows Server 2003.
  
###### Diseño de la infraestructura RADIUS
  
Las siguientes tablas se pueden utilizar como hojas de cálculo en las que recopilar la información necesaria a la que se hará referencia en la guía. Parte de esta información se ha configurado con los scripts proporcionados con esta guía o de forma manual, como se indica en las secciones correspondientes.
  
Información de configuración necesaria definida por el usuario  
La siguiente tabla incluye información que es específica de cada organización. Antes de continuar, asegúrese de que esta información se ha recopilado, se han tomado decisiones respecto a ella y se ha registrado.
  
**Tabla 15. Parámetros de configuración definidos por el usuario**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Elemento de configuración</p></th>  
<th><p>Parámetro</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Nombre DNS del dominio raíz del bosque de Active Directory</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Nombre NetBIOS del dominio</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Nombre del servidor IAS principal</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Nombre del servidor IAS secundario</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
</tbody>  
</table>
  
Información de configuración necesaria definida por la solución  
La siguiente tabla incluye parámetros que no deben cambiarse, excepto si hay una necesidad específica para hacerlo. Asegúrese de comprender completamente las repercusiones y dependencias que producen estos cambios y crear un plan antes de realizar cualquier modificación, incluidos los cambios en los scripts que sean necesarios.
  
**Tabla 16. Parámetros de configuración definidos por la solución**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Elemento de configuración</p></th>  
<th><p>Parámetro</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Nombre completo del grupo administrativo que controla la configuración de IAS</p></td>
<td style="border:1px solid black;"><p>Administradores de IAS</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Nombre completo del grupo que revisa los registros de solicitudes de cuentas y autenticación IAS</p></td>
<td style="border:1px solid black;"><p>Auditores de seguridad de IAS</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Ruta de los scripts de instalación</p></td>
<td style="border:1px solid black;"><p>C:\MSSScripts</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Archivo por lotes de exportación de configuración IAS</p></td>
<td style="border:1px solid black;"><p>IASExport.bat</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Archivo por lotes de importación de configuración IAS</p></td>
<td style="border:1px solid black;"><p>IASImport.bat</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Archivo por lotes de exportación de configuración del cliente RADIUS IAS</p></td>
<td style="border:1px solid black;"><p>IASClientExport.bat</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Archivo por lotes de importación de configuración del cliente RADIUS IAS</p></td>
<td style="border:1px solid black;"><p>IASClientImport.bat</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Ruta de los archivos de copia de seguridad de configuración</p></td>
<td style="border:1px solid black;"><p>D:\IASConfig</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Ubicación de los registros de peticiones de auditoría y autenticación IAS</p></td>
<td style="border:1px solid black;"><p>D:\IASLogs</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Nombre del recurso compartido que contiene los registros de las peticiones RADIUS</p></td>
<td style="border:1px solid black;"><p>IASLogs</p></td>
</tr>  
</tbody>  
</table>
  
###### Implementación del servidor IAS
  
La solución que se indica en las siguientes secciones está compuesta por dos servidores IAS ubicados de forma centralizada y configurados como servidores RADIUS para controlar el acceso a la WLAN. Tenga esto en cuenta esto y realice las siguientes tareas antes de continuar.
  
-   El hardware de servidor se debe asignar y configurar.
  
-   El sistema operativo del servidor se debe instalar y configurar para cada procedimiento organizativo establecido.
  
-   Active Directory debe estar instalado y debe funcionar correctamente.
  
-   Asimismo, se deben haber aplicado los procedimientos de protección del servidor organizativo y las aplicaciones adicionales que exijan las directivas establecidas.
  
Instalación de los scripts de configuración  
Con esta solución se proporcionan un gran número de scripts que facilitarán la implementación. Estos scripts se deben instalar en todos los servidores antes de continuar y no deben eliminarse, ni siquiera después de llevar a cabo los pasos descritos en esta guía.
  
**Para instalar los scripts de configuración**
  
1.  Cree una carpeta denominada C:\\MSSScripts.
  
2.  Copie los scripts del origen de distribución en la carpeta que acaba de crear.
  
Requisitos adicionales del software de servidor  
Además del sistema operativo del servidor y otras aplicaciones que pueden ser necesarias en virtud de una directiva de creación de servidores establecida, se deben instalar el ejecutable CAPICOM 2.1 y las bibliotecas DLL auxiliares para que se admitan los scripts proporcionados en esta guía.
  
Para obtener más información sobre [CAPICOM](http://www.microsoft.com/downloads/details.aspx?familyid=860ee43a-a843-462f-abb5-ff88ea5896f6&displaylang=en), incluida la ubicación de descarga y las instrucciones de instalación, vaya a http://www.microsoft.com/downloads/details.aspx?displaylang=es&FamilyID=860ee43a-a843-462f-abb5-ff88ea5896f6.
  
Configuración de los grupos de administración de IAS  
El siguiente comando de script creará los grupos de seguridad Administradores de IAS y Auditores de seguridad de IAS:
  
```  
 Cscript //job:CreateIASGroups C:\\MSSScripts\\IAS\_Tools.wsf   
```  
En entornos de varios dominios, estos grupos se deben crear en el mismo dominio en el que residen los servidores IAS.
  
Después de crear los grupos necesarios, se deben configurar de modo que puedan realizar tareas de configuración de IAS del siguiente modo:
  
-   Agregue el grupo global de dominio Administradores de IAS al grupo local Administradores en todos los servidores IAS.
  
-   Si se ha instalado IAS en los controladores de dominio, el grupo Administradores de IAS se debe agregar al grupo Administradores del dominio.
  
-   Los grupos Administradores de IAS y Auditores de seguridad de IAS necesitan rellenarse con las cuentas de usuario correspondientes.
  
Configuración de los parámetros de seguridad del sistema del servidor  
Como se ha mencionado anteriormente, en esta guía se asume que en la mayoría de las medianas empresas hay establecidos procedimientos y directivas de protección de los servidores. Por este motivo, no se proporcionan instrucciones detalladas sobre el proceso de garantizar la seguridad de los servidores que necesita esta solución. Si no se han establecido directivas o procedimientos para la protección de los servidores o si se necesita más información acerca de la protección de los servidores IAS, consulte la [Guía de seguridad de Windows 2003](http://go.microsoft.com/fwlink/?linkid=14846) en http://go.microsoft.com/fwlink/?LinkId=14846 (puede estar en inglés).
  
###### Instalación y configuración de IAS
  
La siguiente sección describe cómo instalar IAS en los servidores. Es importante que cada paso de instalación y configuración se lleve a cabo como se indica en cada servidor IAS.
  
IAS se instala al seleccionar el componente Servicios de red – Servicio de autenticación Internet en el administrador de componentes opcionales de Windows (accesible desde la opción Agregar o quitar componentes de Windows del Panel de control). Para simplificar este proceso, utilice el siguiente script:
  
```  
 sysocmgr /i:sysoc.inf /u:C:\\MSSScripts\\OC\_AddIAS.txt   
```  
 Registro de IAS en Active Directory  
Los servidores IAS se deben registrar en los dominios y, para ello, la cuenta del equipo de cada servidor IAS debe ser miembro del grupo de seguridad Servidores RAS e IAS en los dominios en los que se necesitarán para la autenticación. La pertenencia a estos grupos garantiza que los servidores IAS tienen permiso de lectura de las propiedades de acceso remoto de todas las cuentas de usuario y equipo de los dominios.
  
**Para registrar IAS en Active Directory**
  
1.  Inicie sesión en cada servidor con una cuenta que tenga privilegios de Administradores de dominio en los dominios en los que sea necesario registrar el servidor IAS.
  
2.  En el caso del dominio predeterminado, ejecute lo siguiente en un símbolo del sistema:
  
    ```  
 netsh ras add registeredserver   
```
  
3.  En el caso de los dominios distintos del predeterminado, ejecute lo siguiente en un símbolo del sistema:
  
    ```  
 netsh ras add registeredserver domain = DomainName   
```
  
    **Nota**   El objeto de equipo del servidor IAS también se puede agregar a los grupos de seguridad Servidores RAS e IAS mediante el complemento MMC de Usuarios y equipos de Active Directory.
  
Creación y protección de los directorios de datos de IAS  
Existen algunos requisitos para el directorio en el que se van a almacenar los datos de configuración y registro de los servidores IAS. Con el fin de facilitar el proceso de configuración para crear y garantizar la seguridad de estos directorios, se puede ejecutar el siguiente archivo por lotes en un símbolo del sistema:
  
```  
 C:\\MSSScripts\\IAS\_Data.bat   
```  
**Nota**   Puede que, antes de ejecutar este archivo por lotes, sea necesario editar y reemplazar las entradas %*DomainName*% para reflejar el nombre NETBIOS del dominio de un determinado entorno.
  
###### Configuración del servidor IAS principal
  
El servidor seleccionado para actuar como servidor IAS principal se debe configurar antes que ningún otro servidor IAS del entorno, ya que se utilizará como plantilla para configurar los parámetros del resto de los servidores IAS.
  
Registro de las peticiones de autenticación y cuentas  
IAS registra de forma predeterminada las peticiones de autenticación RADIUS y cuentas, pero es necesario habilitar las dos opciones correspondientes para garantizar el registro de los eventos de seguridad y su ulterior utilización en caso de que sea necesario llevar a cabo una investigación.
  
**Para configurar el registro de las peticiones de autenticación y cuentas**
  
1.  Seleccione Registro de acceso remoto en el complemento MMC de Servicio de autenticación Internet y, a continuación, consulte las propiedades del método de registro Archivo local.
  
2.  Seleccione las opciones Solicitudes de cuentas y Solicitudes de autenticación.
  
3.  Asegúrese de que el directorio del archivo de registro se ha configurado como D:\\IASLogs y de que se ha seleccionado un formato compatible con la base de datos (de este modo, los registros se podrán importar directamente en bases de datos como Microsoft SQL Server™).
  
##### Autenticación 802.1X de WLAN
  
En esta sección se ofrecen los pasos del proceso de implementación de seguridad para WLAN con la especificación del protocolo 802.1X, tal y como se aplica en las plataformas con Windows Server 2003 y el SP1 de Windows XP. Estas instrucciones incluyen información relacionada con la configuración de los grupos de Active Directory, la implementación de los certificados X.509, la modificación de los parámetros del servidor IAS, la implementación de la directiva de grupo de WLAN y algunas sugerencias para configurar los puntos de acceso inalámbrico para admitir la implementación 802.1X de EAP-TLS en la que se basa esta guía.
  
###### Preparación del entorno para una WLAN segura
  
Una vez establecidas las infraestructuras RADIUS y de los certificados subyacentes, se pueden implementar los pasos reales de configuración específicos de 802.1X. Las siguientes tablas de parámetros necesarios pueden ayudarle en el proceso de recopilación de información que se debe realizar antes de la implementación real. Algunos de estos parámetros se habilitan manualmente y otros forman parte de los scripts proporcionados en esta guía.
  
Parámetros de configuración necesarios definidos por el usuario  
La siguiente tabla incluye parámetros específicos de la organización que se deben recopilar o sobre los que hay que tomar una decisión antes de continuar con esta fase de implementación de una WLAN segura. El espacio facilitado se puede utilizar para registrar los parámetros necesarios para cada entorno concreto.
  
**Tabla 17. Parámetros necesarios definidos por el usuario**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Elemento de configuración</p></th>  
<th><p>Parámetro</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Nombre DNS del dominio raíz del bosque de Active Directory</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Nombre NetBIOS del dominio</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Nombre del servidor IAS principal</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Nombre del servidor IAS secundario</p></td>
<td style="border:1px solid black;"><p> </p></td>
</tr>  
</tbody>  
</table>
  
Parámetros de configuración necesarios definidos por la solución  
La siguiente tabla incluye parámetros que no deben cambiarse, excepto si hay una necesidad específica para hacerlo. Asegúrese de comprender completamente las repercusiones y dependencias que producen estos cambios y crear un plan antes de realizar cualquier modificación, incluidos los cambios en los scripts que sean necesarios.
  
**Tabla 18. Parámetros de configuración definidos por la solución**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Elemento de configuración</p></th>  
<th><p>Parámetro</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Grupo global de Active Directory que controla la implementación de certificados de autenticación de usuario 802.1X</p></td>
<td style="border:1px solid black;"><p>Inscribir automáticamente autenticación de usuario – Certificado de usuario</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Grupo global de Active Directory que controla la implementación de certificados de autenticación de equipo 802.1X</p></td>
<td style="border:1px solid black;"><p>Inscribir automáticamente autenticación de usuario – Certificado de equipo</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Grupo global de Active Directory que contiene el servidor IAS que necesita certificados de autenticación 802.1X</p></td>
<td style="border:1px solid black;"><p>Inscribir automáticamente certificado de autenticación de servidor IAS y RAS</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Grupo global de Active Directory que contiene los usuarios que pueden tener acceso a la red inalámbrica</p></td>
<td style="border:1px solid black;"><p>Directiva de acceso remoto – Usuarios inalámbricos</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Grupo global de Active Directory que contiene los equipos que pueden tener acceso a la red inalámbrica</p></td>
<td style="border:1px solid black;"><p>Directiva de acceso remoto – Equipos inalámbricos</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Grupo universal de Active Directory que contiene los grupos Usuarios inalámbricos y Equipos inalámbricos</p></td>
<td style="border:1px solid black;"><p>Directiva de acceso remoto – Acceso inalámbrico</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Grupo global de Active Directory que contiene los equipos que necesitan una configuración de las propiedades de la red inalámbrica</p></td>
<td style="border:1px solid black;"><p>Directiva de red inalámbrica – Equipo</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Plantilla de certificado que se utiliza para generar certificados para la autenticación de usuario del cliente</p></td>
<td style="border:1px solid black;"><p>Autenticación del cliente – Usuario</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Plantilla de certificado que se utiliza para generar certificados para la autenticación de equipo del cliente</p></td>
<td style="border:1px solid black;"><p>Autenticación del cliente – Equipo</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Plantilla de certificado que se utiliza para generar certificados para la autenticación del servidor para IAS</p></td>
<td style="border:1px solid black;"><p>Autenticación del servidor IAS y RAS</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Ruta de los scripts de instalación</p></td>
<td style="border:1px solid black;"><p>C:\MSSScripts</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Ruta de los archivos de copia de seguridad de configuración</p></td>
<td style="border:1px solid black;"><p>D:\IASConfig</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Ruta de los registros de auditoría y autenticación IAS</p></td>
<td style="border:1px solid black;"><p>D:\IASLogs</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Nombre de directiva</p></td>
<td style="border:1px solid black;"><p>Permitir acceso inalámbrico</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Nombre GPO de Active Directory</p></td>
<td style="border:1px solid black;"><p>Directiva de red inalámbrica</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Directiva de red inalámbrica en el GPO anterior</p></td>
<td style="border:1px solid black;"><p>Configuración inalámbrica de equipo cliente</p></td>
</tr>  
</tbody>  
</table>
  
Creación de los grupos de Active Directory necesarios para el acceso de WLAN  
El siguiente script se debe ejecutar con una cuenta que tenga permisos de creación de grupos de seguridad de Active Directory, ya que crea los grupos necesarios para implementar la inscripción de certificados de autenticación inalámbrica, la directiva de acceso remoto y la directiva de grupo de red inalámbrica:
  
```  
 Cscript //job:CreateWirelessGroups C:\\MSSScripts\\wl\_tools.wsf   
```  
**Nota**   En los entornos de bosque de varios dominios, los grupos se deben crear en el mismo dominio que los usuarios inalámbricos.
  
Comprobación de la configuración DHCP  
Para admitir el uso de redes inalámbricas, los servidores DHCP se deben configurar con ámbitos inalámbricos específicos y tiempos permitidos para la dirección IP más breves que los de otros clientes cableados. Consulte a los administradores del servidor DHCP para asegurarse de que DHCP se ha configurado correctamente. Para obtener más información sobre la planeación de DHCP para las LAN inalámbricas, consulte el [Kit de implementación de Windows Server 2003](http://www.microsoft.com/windowsserver2003/techinfo/reskit/deploykit.mspx) en www.microsoft.com/windowsserver2003/techinfo/reskit/deploykit.mspx (puede estar en inglés).
  
###### Configuración de los certificados de autenticación WLAN
  
Para implementar una seguridad WLAN basada en EAP-TLS como se indica en esta guía, es necesario crear e implementar los siguientes tipos de certificados:
  
-   Autenticación del cliente – Equipo
  
-   Autenticación del cliente – Usuario
  
-   Autenticación del servidor IAS y RAS
  
Creación de una plantilla de certificado para la autenticación del servidor IAS  
Los servidores IAS necesitan un certificado de servidor para que los equipos se autentiquen en los clientes durante el protocolo de enlace EAP-TLS. El administrador de Servicios de Certificate Server debe llevar a cabo los siguientes pasos para crear una plantilla de certificado de autenticación de servidores que puedan utilizar los servidores IAS.
  
**Para crear una plantilla de certificado para la autenticación de servidores**
  
1.  Inicie sesión en la CA emisora con una cuenta del grupo administrativo de CA y ejecute el complemento MMC de Plantillas de certificado.
  
2.  Cree un duplicado de la plantilla de certificado de Servidor RAS e IAS. En la ficha **General** de las propiedades de la nueva plantilla, en el campo **Nombre para mostrar plantilla**, escriba **Autenticación del servidor IAS y RAS**.
  
3.  En la ficha **Extensiones**, asegúrese de que las directivas de emisión sólo incluyen la autenticación del servidor (IDO 1.3.6.1.5.5.7.3.1).
  
4.  Asimismo, en la ficha **Extensiones**, edite las directivas de emisión para agregar la directiva Seguridad media.
  
5.  En la ficha **Nombre de sujeto**, seleccione **Construido a partir de esta información de Active Directory**. Asegúrese también de que **Formato de nombre de sujeto** se ha configurado como **Nombre común** y que sólo se ha seleccionado **Nombre DNS** en **Incluir esta información**, en **Nombre de sujeto alternativo**.
  
6.  En la ficha **Tratamiento de la petición**, haga clic en el botón **Proveedores de servicios de cifrado (CSP)**, asegúrese de que se ha seleccionado **Las solicitudes tienen que usar uno de los siguientes CSP** y de que sólo se ha seleccionado **Microsoft RSA SChannel Cryptographic Provider**.
  
7.  En la ficha **Seguridad**, agregue el grupo de seguridad **Inscribir automáticamente certificado de autenticación de servidor IAS y RAS** con permisos de lectura, inscripción e inscripción automática, y quite otros grupos que tengan permisos de inscripción o inscripción automática de esta plantilla de certificado.
  
    **Nota**   Puede que sea aconsejable configurar este certificado de modo que se necesite la aprobación del administrador de certificados, ya que se considera que tiene un valor de seguridad relativamente alto. Al habilitar este valor, se contribuye a garantizar que no se va a inscribir un servidor IAS malintencionado, pero será necesario realizar una aprobación manual después de que el servidor IAS emita y envíe automáticamente los certificados.
  
Creación de una plantilla de certificado para la autenticación de usuarios  
Es necesario que los usuarios finales tengan certificados de usuario para autenticarse en el servidor IAS durante el proceso del protocolo de enlace EAP-TLS. De nuevo, es necesario que el titular de la cuenta designado como administrador de Servicios de Certificate Server lleve a cabo los siguientes pasos.
  
**Para crear una plantilla de certificado de autenticación de usuarios**
  
1.  Inicie el complemento MMC de Plantillas de certificado en el servidor de la CA emisora.
  
2.  Cree un duplicado de la plantilla Sesión autenticada y en la ficha **General** de la nueva plantilla, en el campo **Nombre para mostrar plantilla**, escriba **Autenticación del cliente – Usuario**.
  
3.  En la ficha **Tratamiento de la petición**, seleccione **Proveedores de servicios de cifrado (CSP)** y desactive las casillas de verificación **Microsoft Base DSS** **Cryptographic Provider**.
  
4.  En la ficha **Nombre de sujeto**, asegúrese de que esté seleccionada la opción **Construido a partir de esta información de Active Directory**. En **Formato de nombre de sujeto**, seleccione **Nombre común**. Asegúrese de que **Nombre principal del** **usuario** (UPN) es la única opción que aparece seleccionada en **Incluir esta información en Nombre de sujeto alternativo**.
  
5.  En la ficha **Extensiones**, asegúrese de que únicamente se incluye **Autenticación del cliente (IDO 1.3.6.1.5.5.7.3.2)** en **Directivas de aplicación**. Edite también las directivas de emisión y agregue la directiva **Seguridad baja**.
  
6.  En la ficha **Seguridad**, agregue el grupo de seguridad **Inscribir automáticamente autenticación de usuario – Certificado de usuario** con permisos de lectura, inscripción e inscripción automática. También deben quitarse todos los grupos con permisos de inscripción o inscripción automática.
  
Creación de una plantilla de certificado para la autenticación de equipos  
Este certificado es el que utilizan los equipos cuando se autentican en el servidor IAS durante el protocolo de enlace EAP-TLS. Una vez más, el administrador de Servicios de Certificate Server debe realizar las siguientes tareas.
  
**Para crear una plantilla de certificado de autenticación de equipos**
  
1.  Inicie el complemento MMC de Plantillas de certificado en la CA emisora.
  
2.  Cree un duplicado de la plantilla Autenticación de estación de trabajo. En la ficha **General** de la nueva plantilla, en el campo **Nombre para mostrar plantilla**, escriba **Autenticación del cliente – Equipo**.
  
3.  En la ficha **Nombre de sujeto**, asegúrese de que está seleccionada la opción **Construido a partir de esta información de Active Directory**. En **Formato de nombre de sujeto**, seleccione **Nombre común**. Asegúrese de que **Nombre DNS** es la única opción que aparece seleccionada en **Incluir esta información en Nombre de sujeto alternativo**.
  
4.  En la ficha **Extensiones**, edite las directivas de aplicación y asegúrese de que únicamente se incluye **Autenticación del cliente (IDO 1.3.6.1.5.5.7.3.2)**. Edite también las directivas de **emisión** y agregue la directiva **Seguridad baja**.
  
5.  En la ficha **Seguridad**, agregue el grupo de seguridad **Inscribir automáticamente autenticación de usuario – Certificado de equipo** con permisos de lectura, inscripción e inscripción automática. Debe quitarse cualquier otro grupo con permisos.
  
Cómo agregar certificados de autenticación WLAN a la CA  
Una vez configuradas las plantillas de certificado, hay que agregarlas a la CA para habilitar la inscripción. Para ello, el administrador de Servicios de Certificate Server tendrá que realizar las siguientes tareas.
  
**Para agregar plantillas de certificado a la CA**
  
-   En la CA emisora, inicie el complemento MMC de Entidad de certificación y haga clic con el botón secundario en la carpeta **Plantillas de certificado**, seleccione **Nuevo** y, a continuación, haga clic en **Plantilla de certificado que se va a emitir**. Seleccione los siguientes certificados y, a continuación, haga clic en **Aceptar**:
  
    -   Autenticación del cliente – Equipo
  
    -   Autenticación del cliente – Usuario
  
    -   Autenticación del servidor IAS y RAS
  
Inscripción del certificado del servidor IAS  
La implementación de los certificados de autenticación de servidor en los servidores IAS es un proceso bastante sencillo y automático.
  
**Para inscribir un servidor IAS**
  
1.  Inicie el complemento MMC de Usuarios y equipos de Active Directory y agregue las cuentas del equipo IAS al grupo de seguridad Inscribir automáticamente certificado de autenticación de servidor IAS y RAS.
  
2.  Reinicie el servidor IAS e inicie sesión como miembro del grupo local Administradores.
  
3.  En un símbolo del sistema, ejecute GPUPDATE /force.
  
4.  Abra MMC y agregue el complemento Certificados. Cuando se le pida, seleccione la opción Cuenta de equipo y, a continuación, Equipo local.
  
5.  Seleccione **Certificados (equipo local)** en el árbol de la consola y, en el menú **Acción**, haga clic en **Todas las tareas** y, a continuación, seleccione **Inscribir certificados automáticamente**.
  
    **Nota**   Si se activó la opción de requerir la aprobación del administrador de certificados, el administrador de CA tendrá que comprobar la validez de esta petición y emitir el certificado.
  
Cómo agregar usuarios y equipos a los grupos de inscripción automática  
Los usuarios y equipos que requieren conectividad WLAN necesitarán certificados de usuario y equipo emitidos para poder autenticarse en la red y tener acceso a ésta a través de una conexión inalámbrica. El proceso de emisión y renovación de estos certificados es transparente para el usuario final debido a los grupos de inscripción automática que se han configurado con anterioridad.
  
Para agregar usuarios y sus equipos a los grupos de inscripción automática, sólo tiene que utilizar el complemento MMC de Usuarios y equipos de Active Directory para agregar las cuentas de usuario al grupo Inscribir automáticamente autenticación del cliente – Certificado de usuario y agregar sus equipos al grupo Inscribir automáticamente autenticación del cliente – Certificado de equipo. Una vez realizada esta asignación, el usuario en cuestión recibirá los certificados de usuario y de equipo correspondientes tras reiniciar los equipos y volver a iniciar sesión en la red.
  
**Nota**   Esta solución utiliza grupos personalizados para controlar qué usuarios y equipos pueden recibir certificados. Si el entorno exige que todos los usuarios y equipos requieran certificados, sólo tiene que agregar los usuarios del dominio al grupo Inscribir automáticamente autenticación de cliente - Certificado de usuario, y los equipos del dominio, al grupo Inscribir automáticamente autenticación de cliente – Certificado de equipo.
  
###### Configuración de la infraestructura de acceso WLAN
  
El servidor IAS principal debe configurarse con una directiva de acceso remoto y la configuración de solicitud de conexión que determina la autenticación y autorización de los clientes inalámbricos en la WLAN. A continuación, esta configuración debe replicarse en otros servidores IAS y, posteriormente, cada uno de ellos debe configurarse de manera exclusiva para aceptar conexiones de clientes RADIUS, como los puntos de acceso inalámbrico. Después, es necesario configurar estos puntos de acceso inalámbrico para que utilicen el servidor IAS como los orígenes de autenticación y autorización para la red inalámbrica 802.1X.
  
Creación de una directiva de acceso remoto IAS para redes WLAN  
Utilice el complemento MMC de Servicio de autenticación Internet en el servidor IAS principal para configurar IAS con una directiva de acceso remoto como se describe a continuación.
  
**Para crear una directiva de acceso remoto**
  
1.  Haga clic con el botón secundario en la carpeta **Directivas de acceso remoto** y, a continuación, seleccione **Crear nueva directiva de acceso remoto**.
  
2.  Asigne un nombre a la nueva directiva **Permitir acceso inalámbrico** e indique al asistente que desea configurar **Una directiva típica para un escenario común**.
  
3.  Seleccione **Inalámbrico** como método de acceso.
  
4.  Conceda acceso en función de los grupos y utilice el grupo de seguridad Directiva de acceso remoto – Acceso inalámbrico.
  
5.  Elija el tipo **Tarjeta inteligente u otros certificados para el tipo Protocolo de autenticación extensible (EAP)** y, a continuación, seleccione el certificado de autenticación de servidor instalado para IAS.
  
6.  Finalice el proceso y salga del asistente.
  
7.  Abra las propiedades de la directiva Permitir acceso inalámbrico y, a continuación, haga clic en **Editar perfil**.
  
8.  En la ficha **Opciones avanzadas**, agregue el atributo **Ignore-User-Dialin-Properties**, configúrelo como **True** y, a continuación, agregue el atributo **Termination-Action** y defínalo como **RADIUS Request**.
  
    **Nota**   La directiva Permitir acceso inalámbrico puede coexistir con otras directivas creadas por el usuario o con las directivas de acceso predeterminadas, pero, para que funcione correctamente, la directiva de acceso remoto predeterminada debe incluirse después de la directiva Permitir acceso inalámbrico en la carpeta Directivas de acceso remoto.
  
Cómo agregar clientes RADIUS a IAS  
Los puntos de acceso inalámbrico y los proxy RADIUS deben agregarse a IAS como clientes RADIUS para que puedan utilizar los servicios de autenticación y cuentas mediante el protocolo RADIUS.
  
**Para agregar clientes RADIUS a IAS**
  
1.  Inicie el complemento MMC de Servidor de autenticación Internet.
  
2.  Haga clic con el botón secundario en la carpeta **Clientes RADIUS** y, a continuación, haga clic en **Nuevo cliente RADIUS**.
  
3.  Especifique el nombre descriptivo y la dirección IP del punto de acceso inalámbrico.
  
4.  Seleccione RADIUS/Estándar como atributo client-vendor y especifique el secreto compartido del punto de acceso inalámbrico específico. A continuación, seleccione el atributo **Request Must Contain the Message Authenticator**.
  
    **Nota**   Este proceso debe repetirse en todos los servidores IAS para garantizar que cada uno tiene un conjunto único de clientes y secretos compartidos de punto de acceso inalámbrico. Para facilitar este proceso, esta guía contiene un script que se puede utilizar para generar secretos compartidos que, a su vez, pueden almacenarse en una ubicación segura por si es necesario realizar una restauración del sistema. Para utilizar este script, escriba lo siguiente en un símbolo del sistema:
  
    ```  
 Cscript //job:GenPWD C:\\MSSScripts\\wl\_tools.wsf /client:ClientName   
```
  
###### Implementación de configuraciones en varios servidores IAS
  
Una vez configurados los siguientes elementos en el servidor IAS principal, podrán exportarse a archivos de texto mediante el comando **netsh**. Tras exportarse, estos archivos de texto se pueden importar a los servidores IAS que tengan una función similar en el entorno; de esta forma, se garantiza la existencia de una configuración común en todo el entorno.
  
Los parámetros de configuración que se pueden exportar son los siguientes:
  
-   Configuración de servidor
  
-   Configuración de registro
  
-   Directivas de acceso remoto
  
-   Clientes RADIUS
  
-   Configuración completa
  
Los servidores IAS deben contener una lista única propia de clientes RADIUS y secretos compartidos; por lo tanto, esta información se debe configurar de manera individual en cada servidor y es necesario hacer una copia de seguridad de esta información de forma independiente. Además, un volcado completo de la configuración contiene información muy confidencial que es necesario proteger, ya que esta información puede utilizarse para obtener acceso a la red inalámbrica si se roba.
  
Exportación de la configuración del servidor IAS principal  
Los siguientes tipos de parámetros se deben exportar como archivos de texto para la replicación en otros servidores IAS.
  
-   Configuración del servidor
  
-   Configuración de registro
  
-   Directiva de acceso remoto
  
-   Directivas de petición de conexión
  
Para facilitar este proceso, esta guía incluye archivos por lotes que contienen los comandos **netsh**, que permiten exportar la información común de configuración a archivos de texto en el directorio D:\\IASConfig mediante la emisión de la siguiente línea en un símbolo del sistema.
  
```  
 C:\\MSSScripts\\IASExport.bat   
```  
 Importación de la información de configuración del servidor IAS principal  
Como se ha mencionado anteriormente, IAS utiliza el comando **netsh** para transferir los estados de configuración entre los servidores. Este proceso permite que la implementación sea más eficaz y además reduce las probabilidades de error durante el proceso de configuración. Ahora que ya se ha exportado la configuración del servidor IAS principal, los servidores IAS secundarios pueden importar el estado de configuración.
  
**Para importar el estado de configuración del servidor IAS principal en otros servidores IAS**
  
1.  Copie todos los archivos de configuración del directorio D:\\IASConfig del servidor IAS principal en el directorio D:\\IASConfig correspondiente de los demás servidores IAS.
  
2.  Utilice el siguiente archivo por lotes (incluido en esta guía) en una línea de comandos en los servidores secundarios para importar el estado de configuración:
  
    ```  
 C:\\MSSScripts\\IASImport.bat   
```
  
##### Clientes y puntos de acceso inalámbrico
  
El procedimiento de configuración de los puntos de acceso inalámbrico puede variar notablemente en función de la marca y el modelo del dispositivo concreto. Sin embargo, los proveedores de puntos de acceso inalámbrico normalmente proporcionan instrucciones detalladas de configuración de los dispositivos junto con los siguientes detalles necesarios:
  
-   Configuración de red 802.1X
  
-   Configuración de la dirección del servidor RADIUS principal
  
-   Configuración de la dirección del servidor RADIUS secundario
  
-   Secreto compartido de RADIUS con el servidor RADIUS principal
  
-   Secreto compartido de RADIUS con el servidor RADIUS secundario
  
Para obtener más instrucciones sobre la configuración de un modelo y marca de dispositivo inalámbrico concreto, consulte las instrucciones del proveedor o el sitio web de soporte técnico.
  
###### Implementación de los certificados de autenticación WLAN
  
En esta sección se describen algunas tareas de configuración importantes que es necesario realizar para habilitar la inscripción automática de certificados para los clientes basados en Windows XP. Aunque en las secciones anteriores se ha explicado cómo habilitar las directivas y plantillas para ofrecer compatibilidad con la inscripción automática de certificados en la infraestructura de certificados, la compatibilidad de Windows XP con esta funcionalidad está deshabilitada de forma predeterminada. Para habilitar la compatibilidad con la inscripción automática de certificados, es necesario configurar los parámetros adecuados mediante la directiva de grupo. Gracias a que los grupos de seguridad pueden controlar la inscripción automática, se puede habilitar esta capacidad para todos los usuarios y equipos de un dominio y estos grupos de seguridad pueden determinar quién recibirá los certificados de cada tipo.
  
**Para habilitar la inscripción automática para todos los usuarios y equipos de un dominio**
  
1.  Inicie sesión con una cuenta que tenga permisos para crear GPO y vincular GPO al dominio.
  
2.  En Usuarios y equipos de Active Directory, seleccione el objeto de dominio, haga clic sobre él con el botón secundario y elija Propiedades.
  
3.  En la ficha **Directiva de grupo**, haga clic en **Nuevo** y, a continuación, escriba un nombre para el GPO (por ejemplo, Directivas de PKI de dominio).
  
4.  Haga clic en **Editar** y, a continuación, busque **Directivas de claves públicas** en Configuración del equipo\\Configuración de Windows\\Configuración de seguridad.
  
5.  En el panel **Detalles**, haga doble clic en **Configuración de inscripción automática**.
  
6.  Asegúrese de que estén seleccionados los siguientes elementos:
  
    -   Registrar certificados automáticamente
  
    -   Renovar certificados caducados, actualizar certificados pendientes y quitar certificados revocados
  
    -   Actualizar certificados que usan plantillas de certificado
  
7.  Repita los pasos 5 y 6 de la configuración de inscripción automática de usuario en Configuración de usuario\\Configuración de Windows\\Configuración de seguridad\\Directivas de claves públicas.
  
8.  Cierre el GPO.
  
9.  Asegúrese de que el GPO tiene una prioridad mayor que el GPO de la directiva de dominio predeterminada.
  
10. Repita este proceso para cada dominio en el que se vaya a habilitar la inscripción automática de certificados si se encuentra en un bosque de varios dominios.
  
    **Nota**   Si los usuarios no utilizan perfiles móviles y la inscripción automática está permitida universalmente, se emitirán certificados para los usuarios en todos los equipos en los que inicien sesión. Es posible que no desee que suceda esto cuando los usuarios administrativos inicien sesión en los servidores. Para evitarlo, se recomienda crear un GPO para servidores que deshabilite la inscripción automática. Además, si no le interesa que se habilite la inscripción automática para todos los usuarios, se puede vincular un GPO con varias unidades organizativas que contengan el subconjunto de usuarios que necesitan la inscripción automática.
  
###### Habilitación del acceso WLAN para usuarios y equipos
  
Los últimos pasos para permitir a los usuarios y equipos el acceso WLAN seguro incluyen algunas acciones que deben realizarse en objetos Active Directory. Estas acciones incluyen la modificación de los permisos de cuenta y los permisos de grupo, además de la implementación de la configuración de la directiva de grupo WLAN.
  
Cómo agregar usuarios a grupos de directiva de acceso remoto  
La directiva de acceso remoto de IAS utiliza grupos de seguridad basados en Active Directory para determinar si los usuarios y equipos están autorizados para establecer conexiones con la red WLAN. Estos grupos de seguridad que se han creado en secciones anteriores incluyen:
  
-   Directiva de acceso remoto – Usuarios inalámbricos
  
-   Directiva de acceso remoto – Equipos inalámbricos
  
-   Directiva de acceso remoto – Acceso inalámbrico
  
**Para agregar usuarios y equipos a los grupos de acceso WLAN**
  
1.  Abra el complemento MMC de Usuarios y equipos de Active Directory.
  
2.  Agregue la Directiva de acceso remoto – Usuarios inalámbricos y la Directiva de acceso remoto – Equipos inalámbricos al grupo Acceso remoto – Acceso inalámbrico.
  
3.  Agregue los usuarios que tienen permiso de acceso a la WLAN al grupo Directiva de acceso remoto – Usuarios inalámbricos.
  
4.  Agregue los equipos que tiene permiso de acceso a la WLAN al grupo Directiva de acceso remoto – Usuarios inalámbricos.
  
    **Nota**   Si se decide que se prefiere permitir a todos los usuarios y equipos el acceso a la red WLAN de forma predeterminada, se pueden agregar los grupos Usuarios del dominio y Equipos del dominio a los grupos de directiva correspondientes para simplificar la administración.
  
Creación de la directiva de grupo WLAN de Active Directory  
La directiva de grupo se puede utilizar para automatizar y hacer cumplir los parámetros de configuración WLAN del equipo cliente ya que el MMC de Directiva de grupo de Windows Server 2003 contiene parámetros de directiva de red inalámbrica relacionados con los estándares 802.1X y 802.11.
  
**Para crear una directiva de grupo de red inalámbrica**
  
1.  Abra el complemento MMC de Usuarios y equipos de Active Directory en un servidor con Windows Server 2003 o en una estación de trabajo con las herramientas de administración de Windows Server 2003 instaladas.
  
2.  Seleccione las propiedades del objeto de dominio y, en la ficha **Directiva de grupo**, haga clic en **Nuevo** y, a continuación, asigne un nombre a la directiva de red inalámbrica de GPO.
  
3.  Haga clic en el botón **Propiedades** y, en la ficha **Seguridad**, conceda al grupo de seguridad Directiva de red inalámbrica - Equipo los permisos Leer y Aplicar directiva de grupos. Además, quite los permisos Aplicar directiva de grupos de los usuarios autenticados en el GPO.
  
4.  En la ficha **General**, seleccione **Deshabilitar los parámetros de configuración de usuario** en el objeto de directiva y haga clic en **Sí** en cualquier mensaje de advertencia que aparezca. Aplique los cambios y cierre la ventana.
  
5.  Haga clic en el botón **Editar** y busque \\Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas de redes inalámbrica (IEEE 802.11).
  
6.  Seleccione el objeto de directiva de redes inalámbrica (IEEE 802.11) en el panel de exploración y, a continuación, en el menú **Acción**, haga clic en **Crear directiva de red inalámbrica**. Utilice el asistente para asignar un nombre a la directiva **Configuración inalámbrica de equipo cliente**. Deje seleccionada la opción **Modificar propiedades** y, a continuación, haga clic en **Finalizar** para cerrar el asistente.
  
7.  En la directiva **Configuración inalámbrica de equipo cliente**, en la ficha **Redes preferidas**, seleccione **Agregar** y, a continuación, especifique el nombre de la red o el Identificador de red SSID de la red inalámbrica.
  
8.  Haga clic en la ficha **IEEE 802.1X** y, a continuación, abra los parámetros del **tipo EAP de tarjeta inteligente u otro certificado**. En **Entidades de certificación raíz de confianza**, seleccione el certificado de la CA raíz para la PKI que emitió los certificados del servidor IAS.
  
9.  Cierre las propiedades de Configuración inalámbrica de equipo cliente y Editor de objetos de directiva de grupo.
  
    **Nota**   WPA2 no se puede aplicar actualmente mediante GPO. No obstante, la compatibilidad con GPO de WPA2 se va a incluir en la versión de Windows Vista y Longhorn; además, también hay planeadas actualizaciones para solucionar este problema en las versiones actuales de Windows.
  
Cómo agregar equipos a grupos de seguridad para la directiva de grupo WLAN  
Los grupos de seguridad basados en Active Directory se utilizan para determinar qué equipos tendrán aplicadas las directivas de red inalámbrica para configurar automáticamente los parámetros de 802.11 y 802.1X necesarios. Estos parámetros deben implementarse antes de configurar los parámetros de 802.1X en cualquier punto de acceso inalámbrico y antes de activar la red WLAN. Este método garantiza que los equipos cliente tengan una oportunidad adecuada para descargar y aplicar la directiva de grupo basada en equipo, incluso si no se conectan con frecuencia a la red cableada.
  
La configuración de directiva de grupo se puede aplicar incluso antes de la instalación del adaptador de interfaz de red WLAN (nic), porque recuperará y aplicará automáticamente la configuración correcta de la directiva de grupo de red inalámbrica.
  
Para agregar equipos a los grupos de la directiva de grupo de red inalámbrica, utilice el complemento MMC de Usuarios y equipos de Active Directory para agregar los objetos de equipo autorizados al grupo Directiva de red inalámbrica – Equipo.
  
**Nota**   La configuración del GPO de la red inalámbrica se actualizará en los equipos cliente durante el siguiente intervalo de actualización de la directiva de grupo del equipo. Para forzar una actualización, sólo tiene que emitir el comando GPUPDATE /force.
  
###### Requisitos del cliente WPA2
  
La solución descrita en esta guía se ha diseñado para equipos cliente con capacidad inalámbrica que utilicen Windows XP Professional con SP2 o Windows XP Tablet Edition. Estas versiones de Windows ofrecen compatibilidad integrada para 802.1X y WLAN. Asimismo, los clientes basados en Windows XP disponen de funcionalidad de inscripción automática y renovación de certificados, lo que hace que este tipo de solución basada en certificados sea especialmente rentable cuando está asociada a una infraestructura de certificados.
  
Aunque Windows XP con SP2 incluye compatibilidad integrada para WPA, es necesario instalar una actualización adicional para habilitar la compatibilidad con WPA2 IEEE 802.11i en los clientes basados en el SP2 de Windows XP. Para obtener más información sobre esta actualización adicional, además de las instrucciones de descarga, consulte el artículo que informa que [está disponible la actualización de Acceso protegido Wi-Fi 2 (WPA2) y el Elemento de información de los Servicios de aprovisionamiento inalámbricos (WPS IE)  
para Windows XP con Service Pack 2](http://support.microsoft.com/default.aspx?scid=kb;es-es;893357), en http://support.microsoft.com/default.aspx?scid=kb;es-es;893357.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Tras analizar la multitud de soluciones disponibles para solucionar las imperfecciones más conocidas de los estándares anteriores de seguridad inalámbrica y ver cómo los estándares del sector han convertido en obsoletas esas soluciones, se ha aclarado cuál es la solución para mejorar la seguridad de las redes inalámbricas en el entorno de una mediana empresa. Actualmente, las medianas empresas pueden implementar con eficacia esta útil tecnología para aprovechar las grandes mejoras de productividad de una manera confiable y más segura al utilizar la solución WPA o WPA2 con EAP-TLS y Servicios de Certificate Server que se proporciona esta guía. Después de seguir los pasos detallados y utilizar las herramientas que se proporcionan este documento, una empresa mediana puede disfrutar de una solución inalámbrica confiable y más segura que fomente la productividad, sin que el usuario final de la red sufra interrupciones.
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtener el documento Configuración de puntos de acceso inalámbrico seguros](http://go.microsoft.com/fwlink/?linkid=71716)
  
[](#mainsection)[Principio de la página](#mainsection)
