---
TOCTitle: Guía de planeamiento de acceso seguro con tarjetas inteligentes
Title: Guía de planeamiento de acceso seguro con tarjetas inteligentes
ms:assetid: 'd2a7a146-1779-4f8d-b618-1fd51e24dd85'
ms:contentKeyID: 20200257
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc170941(v=TechNet.10)'
---

Guía de planeamiento de acceso seguro con tarjetas inteligentes
===============================================================

### Información general

Actualizado: 30/06/2005

##### En esta página

[](#ehaa)[El desafío empresarial](#ehaa)
[](#egaa)[Las ventajas empresariales](#egaa)
[](#efaa)[Quién debería leer esta guía](#efaa)
[](#eeaa)[Requisitos previos para el lector](#eeaa)
[](#edaa)[Guía de planeamiento: descripción general](#edaa)
[](#ecaa)[Recursos relacionados](#ecaa)
[](#ebaa)[Envíenos sus comentarios](#ebaa)
[](#abcm)[Capítulo 1: Introducción](#abcm)
[](#abcq)[Capítulo 2: Tecnologías de tarjeta inteligente](#abcq)
[](#abcr)[Capítulo 3: Uso de tarjetas inteligentes para la protección de las cuentas de los administradores](#abcr)
[](#abck)[Capítulo 4: Uso de tarjetas inteligentes para la protección de las cuentas de acceso remoto](#abck)

Cada vez más, los administradores son conscientes del riesgo que supone depender únicamente de nombres de usuario y contraseñas para la autenticación de acceso a los recursos de red. Los atacantes pueden adivinar nombres de usuarios o, incluso, utilizar información que se puede obtener públicamente (como la dirección de correo electrónico impresa en una tarjeta de visita) para identificar un nombre de usuario. Cuando un atacante conoce un nombre de usuario, el único mecanismo de seguridad que se mantiene es la contraseña del usuario.

Los controles de seguridad basados en claves secretas individuales, como las contraseñas, pueden resultar eficaces. Una contraseña larga, compuesta de más de 10 caracteres, en la que se alternen letras, números y signos especiales puede resultar muy difícil de descifrar. Lamentablemente no siempre los usuarios pueden recordar ese tipo de contraseñas, en parte debido a limitaciones humanas fundamentales.

Según un estudio de George A. Miller, publicado en *The Psychological Review* en 1956, el cerebro humano puede retener en la memoria a corto plazo secuencias con un número máximo de caracteres comprendido entre cinco y nueve, con un promedio de siete. Sin embargo, entre las directrices de seguridad suele recomendarse casi siempre el uso de contraseñas aleatorias de ocho caracteres, como mínimo. Dado que la mayoría de los usuarios no pueden memorizar con garantías contraseñas de más de ochos caracteres, muchos optan por anotarlas en un papel.

Normalmente, los usuarios no suelen ser discretos cuando anotan una contraseña, por lo que ponen en peligro sus credenciales ante posibles atacantes. Cuando no existen restricciones en cuanto a la complejidad de las contraseñas, los usuarios tienden a elegir contraseñas con palabras relativamente fáciles de adivinar.

Las contraseñas codificadas tienen una mayor longitud, pero resultan más fáciles de recordar. Microsoft® Windows® 2000 y las versiones posteriores del sistema operativo Windows admiten contraseñas de hasta 127 caracteres. Una contraseña codificada en una frase como "¡Me gusta el fútbol sala 5 contra 5!" aumenta considerablemente la dificultad de descubrir con herramientas que utilizan la "fuerza bruta" de procesamiento y resulta más fácil de recordar para el usuario que si utilizara una combinación aleatoria de letras y números.

Los sistemas de autenticación de dos factores superan los problemas de la autenticación asociados a una sola clave solicitando un segundo dato secreto. En la autenticación de dos factores se utiliza una combinación de los siguientes elementos:

-   Algo que posee el usuario, como un testigo (token) de hardware o una tarjeta inteligente.

-   Algo que el usuario sabe, como un número de identificación personal (NIP).

Las tarjetas inteligentes y los NIP asociados son una forma cada vez más popular, fiable y rentable de una autenticación en dos fases. Además de establecerse los controles adecuados, el usuario debe poseer la tarjeta inteligente y saber el NIP para obtener acceso a los recursos de red. Con el requisito de dos factores se reducen considerablemente las probabilidades de acceso no autorizado a la red de la organización.

Las tarjetas inteligentes proporcionan controles de seguridad particularmente eficaces en dos casos: para proteger las cuentas de administrador y para proteger el acceso remoto. Esta guía se centra en estos dos casos generales como áreas prioritarias para la implantación de tarjetas inteligentes.

Dado que las cuentas en el nivel de administrador tienen asignados numerosos derechos de usuario, si una de estas cuentas queda expuesta, existe el riesgo de que un intruso obtenga acceso a todos los recursos de la red. Es esencial salvaguardar el acceso al nivel del administrador, ya que la usurpación de credenciales de cuentas en el nivel de administrador de dominio pone en peligro la integridad del dominio y, posiblemente, de todo el bosque y de cualquier otro bosque que confíe. La autenticación de dos factores es esencial para la validación de la identidad de los administradores.

Las organizaciones pueden incorporar un nivel de seguridad adicional con la implantación de tarjetas inteligentes para los usuarios que tengan necesidad de conectarse a los recursos de la red. La autenticación de dos factores es particularmente importante en el caso de los usuarios remotos, ya que no es posible proporcionar ningún tipo de control de acceso físico para las conexiones remotas. Con tarjetas inteligentes, la autenticación de dos factores puede aumentar el grado de seguridad del proceso de validación de identidad los usuarios remotos que se conecten a través de red privada virtual (VPN).

### El desafío empresarial

Si quedan expuestas las credenciales de cuentas de administrador en equipos unidos por un dominio, puede ponerse en peligro la integridad de todo el dominio, del bosque en el que éste se encuentra y en otros bosques que mantengan relaciones de confianza con el bosque expuesto. Si las cuentas de acceso remoto quedan expuestas, existe el riesgo de acceso por parte de atacantes externos a información confidencial por medio de conexiones de acceso telefónico o de red privada virtual.

El desafío empresarial que supone salvaguardar las conexiones de administrador y acceso remoto consiste en proporcionar un nivel de seguridad adecuado que no comprometa las posibilidades de uso. Una organización que implante un sistema de autenticación de dos factores para mejorar la seguridad no puede funcionar de un modo óptimo si los usuarios no tienen acceso a la información que necesitan para trabajar. Es de capital importancia encontrar un equilibrio entre la autenticación de dos factores y las posibilidades de uso.

[](#mainsection)[Principio de la página](#mainsection)

### Las ventajas empresariales

El uso de tarjetas inteligentes para proteger cuentas de importancia crítica puede reportar a la empresa las siguientes ventajas:

-   **Mayor protección de los datos confidenciales**. Las tarjetas inteligentes reducen la amenaza de accesos no autorizados con credenciales usurpadas, ya que el intruso debe sustraer también la tarjeta inteligente y obtener el NIP.

-   **Mayor seguridad para las credenciales de inicio de sesión**. Para las credenciales de inicio de sesión, las tarjetas inteligentes utilizan certificados digitales, que son difíciles de falsificar.

-   **Mayor nivel de cumplimiento de normativas**. La capacidad de identificar que el usuario que ha iniciado sesión es quien dice ser proporciona una mayor credibilidad a los registros supervisados.

-   **Menor probabilidad de rechazo**. La autenticación con tarjeta inteligente reduce la posibilidad de que los usuarios puedan negar sus propias acciones.

-   **Mejor integración con sistemas de administración de acceso**. Algunas tarjetas inteligentes también funcionan como tarjetas que permiten administrar el acceso físico, a modo de "llaves" controladas para entrar y salir de instalaciones y sectores específicos dentro de éstas. La combinación de tarjeta inteligente y tarjeta de acceso permite controlar con mayor exactitud el nivel de acceso físico y a través de la red de un usuario o administrador, además de reducir el temor de poner en peligro la seguridad.

[](#mainsection)[Principio de la página](#mainsection)

### Quién debería leer esta guía

Entre los destinatarios previstos de esta guía se encuentran los responsables de la toma de decisiones técnicas, los arquitectos y los administradores de seguridad de la empresa que planean, implantan o trabajan con las conexiones de acceso remoto y la seguridad de la red. Esta información también resultará de utilidad a los consultores que vayan a planear, implantar o trabajar con redes basadas en Windows.

La información que figura en esta guía es válida para organizaciones de cualquier tamaño que precisen un alto grado de protección de las identidades y control de acceso a datos.

[](#mainsection)[Principio de la página](#mainsection)

### Requisitos previos para el lector

Para comprender las soluciones que se presentan en esta guía, los usuarios deben conocer y estar familiarizados con los siguientes aspectos y tecnologías de Microsoft Windows Server™ 2003:

-   Enrutamiento y acceso remoto, que incluye los componentes de una red privada virtual.

-   Servicios de Certificate Server e infraestructura de claves públicas (PKI).

-   Servicio de directorio Active Directory®

-   Directiva de grupo

En esta guía se describen los cuadrantes del modelo de procesos de operación y soporte en Microsoft Operations Framework (MOF). También se describen las funciones de administración de los servicios (SMF) de administración de seguridad y administración de incidentes en MOF. Si desea obtener más información acerca de MOF, visite el sitio Web de [Microsoft Operations Framework](http://www.microsoft.com/mof)en http://www.microsoft.com/mof.

[](#mainsection)[Principio de la página](#mainsection)

### Guía de planeamiento: descripción general

Esta guía incluye cuatro capítulos que se centran en los problemas y conceptos esenciales que son necesarios para el planeamiento de la autenticación con tarjetas inteligentes. Estos capítulos son:

#### Capítulo 1: Introducción

En este capítulo se ofrece un resumen ejecutivo, se tienen en cuenta los desafíos a los que debe enfrentarse la empresa y se describen las ventajas que puede obtener con la implantación de un sistema de autenticación con tarjetas inteligentes. En esta introducción se indica a quién va dirigida la guía, se enumeran los requisitos previos para el lector y se ofrece información general sobre el resto de capítulos y escenarios de solución.

#### Capítulo 2: Tecnologías de las tarjetas inteligentes

En este capítulo se destacan los planteamientos de uso de las tarjetas inteligentes para proteger las cuentas de especial importancia. También se discuten los elementos esenciales de los dos escenarios de solución descritos en los capítulos 3 y 4. Por último, en este capítulo se presenta a la entidad financiera Woodgrove Bank, en la que se basan los dos escenarios de solución.

#### Capítulo 3: Uso de tarjetas inteligentes para la protección de las cuentas de los administradores

En este capítulo se describen las consideraciones sobre el diseño necesarias para proteger las cuentas de los administradores con tarjetas inteligentes. El capítulo continúa con el examen de problemas y requisitos para la entidad Woodgrove Bank. Se discute el concepto de la solución, los requisitos previos, la arquitectura y el funcionamiento de la solución para el escenario en cuestión. Por último, se analizan las distintas posibilidades de ampliar la solución para que incorpore el proceso de administración de cambios.

#### Capítulo 4: Uso de tarjetas inteligentes para la protección de las cuentas de acceso remoto

En este capítulo se describen las consideraciones de diseño para el acceso remoto con tarjetas inteligentes. El capítulo continúa con el examen de los problemas y los requisitos necesarios para la implantación de un acceso remoto seguro en la entidad Woodgrove Bank. Se discute el concepto de la solución, los requisitos previos, la arquitectura y el funcionamiento de la solución para el escenario en cuestión. Por último, en este capítulo se analiza cómo se puede ampliar la solución para que incorpore un sistema de control de acceso físico.

[](#mainsection)[Principio de la página](#mainsection)

### Recursos relacionados

Lea [otras soluciones de seguridad](http://www.microsoft.com/technet/community/columns/sectip/st0805.mspx) del equipo de Microsoft Solutions for Security and Compliance (MSSC).

[](#mainsection)[Principio de la página](#mainsection)

### Envíenos sus comentarios

El equipo Microsoft Solutions for Security and Compliance (MSSC) agradece sus ideas acerca de ésta y otras soluciones de seguridad.

¿Desea hacer algún comentario? Envíelos a través del [Blog de Soluciones de seguridad](http://blogs.technet.com/secguide) para profesionales de TI.

O envíe sus comentarios por correo electrónico a la dirección siguiente: [SecWish@microsoft.com](mailto:secwish@microsoft.com). A menudo respondemos los comentarios enviados a este buzón.

Esperamos sus comentarios.

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 1: Introducción

[](#ecaam)[Resumen ejecutivo](#ecaam)
[](#ecara)[Guía de planeamiento: descripción general](#ecara)

### Resumen ejecutivo

Cada vez más, los administradores son conscientes del riesgo que supone depender únicamente de nombres de usuario y contraseñas para la autenticación de acceso a los recursos de red. Los atacantes pueden adivinar nombres de usuarios o, incluso, utilizar información que se puede obtener públicamente (como la dirección de correo electrónico impresa en una tarjeta de visita) para identificar un nombre de usuario. Cuando un atacante conoce un nombre de usuario, el único mecanismo de seguridad que se mantiene es la contraseña del usuario.

Los controles de seguridad basados en claves secretas individuales, como las contraseñas, pueden resultar eficaces. Una contraseña larga, compuesta de más de 10 caracteres, en la que se alternen letras, números y signos especiales puede resultar muy difícil de descifrar. Lamentablemente no siempre los usuarios pueden recordar ese tipo de contraseñas, en parte debido a limitaciones humanas fundamentales.

Según un estudio de George A. Miller, publicado en *The Psychological Review* en 1956, el cerebro humano puede retener en la memoria a corto plazo secuencias con un número máximo de caracteres comprendido entre cinco y nueve, con un promedio de siete. Sin embargo, entre las directrices de seguridad suele recomendarse casi siempre el uso de contraseñas aleatorias de ocho caracteres, como mínimo. Dado que la mayoría de los usuarios no pueden memorizar con garantías contraseñas de más de ochos caracteres, muchos optan por anotarlas en un papel.

Normalmente, los usuarios no suelen ser discretos cuando anotan una contraseña, por lo que ponen en peligro sus credenciales ante posibles atacantes. Cuando no existen restricciones en cuanto a la complejidad de las contraseñas, los usuarios tienden a elegir contraseñas con palabras relativamente fáciles de adivinar.

Las contraseñas codificadas tienen una mayor longitud, pero resultan más fáciles de recordar. Microsoft® Windows® 2000 y las versiones posteriores del sistema operativo Windows admiten contraseñas de hasta 127 caracteres. Una contraseña codificada en una frase como "¡Me gusta el fútbol sala 5 contra 5!" aumenta considerablemente la dificultad de descubrir con herramientas que utilizan la "fuerza bruta" de procesamiento y resulta más fácil de recordar para el usuario que si utilizara una combinación aleatoria de letras y números.

Los sistemas de autenticación de dos factores superan los problemas de la autenticación asociados a una sola clave solicitando un segundo dato secreto. En la autenticación de dos factores se utiliza una combinación de los siguientes elementos:

-   Algo que posee el usuario, como un testigo (token) de hardware o una tarjeta inteligente.

-   Algo que el usuario sabe, como un número de identificación personal (NIP).

Las tarjetas inteligentes y los NIP asociados son una forma cada vez más popular, fiable y rentable de una autenticación en dos fases. Además de establecerse los controles adecuados, el usuario debe poseer la tarjeta inteligente y saber el NIP para obtener acceso a los recursos de red. Con el requisito de dos factores se reducen considerablemente las probabilidades de acceso no autorizado a la red de la organización.

Las tarjetas inteligentes proporcionan controles de seguridad particularmente eficaces en dos casos: para proteger las cuentas de administrador y para proteger el acceso remoto. Esta guía se centra en estos dos casos generales como áreas prioritarias para la implantación de tarjetas inteligentes.

Dado que las cuentas en el nivel de administrador tienen asignados numerosos derechos de usuario, si una de estas cuentas queda expuesta, existe el riesgo de que un intruso obtenga acceso a todos los recursos de la red. Es esencial salvaguardar el acceso al nivel del administrador, ya que la usurpación de credenciales de cuentas en el nivel de administrador de dominio pone en peligro la integridad del dominio y, posiblemente, de todo el bosque y de cualquier otro bosque que confíe. La autenticación de dos factores es esencial para la validación de la identidad de los administradores.

Las organizaciones pueden incorporar un nivel de seguridad adicional con la implantación de tarjetas inteligentes para los usuarios que tengan necesidad de conectarse a los recursos de la red. La autenticación de dos factores es particularmente importante en el caso de los usuarios remotos, ya que no es posible proporcionar ningún tipo de control de acceso físico para las conexiones remotas. Con tarjetas inteligentes, la autenticación de dos factores puede aumentar el grado de seguridad del proceso de validación de identidad los usuarios remotos que se conecten a través de red privada virtual (VPN).

#### El desafío empresarial

Si quedan expuestas las credenciales de cuentas de administrador en equipos unidos por un dominio, puede ponerse en peligro la integridad de todo el dominio, del bosque en el que éste se encuentra y en otros bosques que mantengan relaciones de confianza con el bosque expuesto. Si las cuentas de acceso remoto quedan expuestas, existe el riesgo de acceso por parte de atacantes externos a información confidencial por medio de conexiones de acceso telefónico o de red privada virtual.

El desafío empresarial que supone salvaguardar las conexiones de administrador y acceso remoto consiste en proporcionar un nivel de seguridad adecuado que no comprometa las posibilidades de uso. Una organización que implante un sistema de autenticación de dos factores para mejorar la seguridad no puede funcionar de un modo óptimo si los usuarios no tienen acceso a la información que necesitan para trabajar. Es de capital importancia encontrar un equilibrio entre la autenticación de dos factores y las posibilidades de uso.

#### Las ventajas empresariales

El uso de tarjetas inteligentes para proteger cuentas de importancia crítica puede reportar a la empresa las siguientes ventajas:

-   **Mayor protección de los datos confidenciales**. Las tarjetas inteligentes reducen la amenaza de accesos no autorizados con credenciales usurpadas, ya que el intruso debe sustraer también la tarjeta inteligente y obtener el NIP.

-   **Mayor seguridad para las credenciales de inicio de sesión**. Para las credenciales de inicio de sesión, las tarjetas inteligentes utilizan certificados digitales, que son difíciles de falsificar.

-   **Mayor nivel de cumplimiento de normativas**. La capacidad de identificar que el usuario que ha iniciado sesión es quien dice ser proporciona una mayor credibilidad a los registros supervisados.

-   **Menor probabilidad de rechazo**. La autenticación con tarjeta inteligente reduce la posibilidad de que los usuarios puedan negar sus propias acciones.

-   **Mejor integración con sistemas de administración de acceso**. Algunas tarjetas inteligentes también funcionan como tarjetas que permiten administrar el acceso físico, a modo de "llaves" controladas para entrar y salir de instalaciones y sectores específicos dentro de éstas. La combinación de tarjeta inteligente y tarjeta de acceso permite controlar con mayor exactitud el nivel de acceso físico y a través de la red de un usuario o administrador, además de reducir el temor de poner en peligro la seguridad.

#### Quién debería leer esta guía

Entre los destinatarios previstos de esta guía se encuentran los responsables de la toma de decisiones técnicas, los arquitectos y los administradores de seguridad de la empresa que planean, implantan o trabajan con las conexiones de acceso remoto y la seguridad de la red. Esta información también resultará de utilidad a los consultores que vayan a planear, implantar o trabajar con redes basadas en Windows.

La información que figura en esta guía es válida para organizaciones de cualquier tamaño que precisen un alto grado de protección de las identidades y control de acceso a datos.

#### Requisitos previos para el lector

Para comprender las soluciones que se presentan en esta guía, los usuarios deben conocer y estar familiarizados con los siguientes aspectos y tecnologías de Microsoft Windows Server™ 2003:

-   Enrutamiento y acceso remoto, que incluye los componentes de una red privada virtual.

-   Servicios de Certificate Server e infraestructura de claves públicas (PKI).

-   Servicio de directorio Active Directory®

-   Directiva de grupo

En esta guía se describen los cuadrantes del modelo de procesos de operación y soporte en Microsoft Operations Framework (MOF). También se describen las funciones de administración de los servicios (SMF) de administración de seguridad y administración de incidentes en MOF. Si desea obtener más información acerca de MOF, visite el sitio Web de [Microsoft Operations Framework](http://www.microsoft.com/mof)en http://www.microsoft.com/mof.

[](#mainsection)[Principio de la página](#mainsection)

### Guía de planeamiento: descripción general

Esta guía incluye cuatro capítulos que se centran en los problemas y conceptos esenciales que son necesarios para el planeamiento de la autenticación con tarjetas inteligentes. Estos capítulos son:

#### Capítulo 1: Introducción

En este capítulo se ofrece un resumen ejecutivo, se tienen en cuenta los desafíos a los que debe enfrentarse la empresa y se describen las ventajas que puede obtener con la implantación de un sistema de autenticación con tarjetas inteligentes. En esta introducción se indica a quién va dirigida la guía, se enumeran los requisitos previos para el lector y se ofrece información general sobre el resto de capítulos y escenarios de solución.

#### Capítulo 2: Tecnologías de las tarjetas inteligentes

En este capítulo se destacan los planteamientos de uso de las tarjetas inteligentes para proteger las cuentas de especial importancia. También se discuten los elementos esenciales de los dos escenarios de solución descritos en los capítulos 3 y 4. Por último, en este capítulo se presenta a la entidad financiera Woodgrove Bank, en la que se basan los dos escenarios de solución.

#### Capítulo 3: Uso de tarjetas inteligentes para la protección de las cuentas de los administradores

En este capítulo se describen las consideraciones sobre el diseño necesarias para proteger las cuentas de los administradores con tarjetas inteligentes. El capítulo continúa con el examen de problemas y requisitos para la entidad Woodgrove Bank. Se discute el concepto de la solución, los requisitos previos, la arquitectura y el funcionamiento de la solución para el escenario en cuestión. Por último, se analizan las distintas posibilidades de ampliar la solución para que incorpore el proceso de administración de cambios.

#### Capítulo 4: Uso de tarjetas inteligentes para la protección de las cuentas de acceso remoto

En este capítulo se describen las consideraciones de diseño para el acceso remoto con tarjetas inteligentes. El capítulo continúa con el examen de los problemas y los requisitos necesarios para la implantación de un acceso remoto seguro en la entidad Woodgrove Bank. Se discute el concepto de la solución, los requisitos previos, la arquitectura y el funcionamiento de la solución para el escenario en cuestión. Por último, en este capítulo se analiza cómo se puede ampliar la solución para que incorpore un sistema de control de acceso físico.

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 2: Tecnologías de tarjeta inteligente

El almacenamiento de datos en red es un requisito esencial para casi cualquier organización. Con frecuencia, las organizaciones deben conectar a Internet redes que contienen datos confidenciales y privados para la comunicación y con fines de generación de ingresos. El constante impulso hacia una mayor conectividad supone un considerable riesgo para la seguridad, ya que la mayoría de las organizaciones utilizan nombres de usuario y contraseñas para la autenticación y la autorización de acceso a recursos de red.

En el Capítulo 1, "Introducción", se ponía de relieve el principal problema que planteaban las combinaciones de nombre de usuario y contraseña. Dado que los nombres de usuario no son secretos, sólo la contraseña proporciona un mecanismo de seguridad eficaz frente a un atacante que intente hacerse pasar por un usuario autorizado. La constatación de la vulnerabilidad de las credenciales basadas en un nombre de usuario y una contraseña ha estimulado un interés creciente en los sistemas de autenticación de dos factores.

[](#eeaan)[Autenticación de dos factores](#eeaan)
[](#edaao)[Requisitos previos para la implantación](#edaao)
[](#ecaap)[El caso de la entidad financiera Woodgrove National Bank](#ecaap)
[](#ebaaq)[Resumen](#ebaaq)

### Autenticación de dos factores

La autenticación en dos fases va más allá de la combinación simple de nombre de usuario y contraseña y requiere que un usuario envíe algún tipo de toquen único junto con un NIP. Existen diversos medios para implantar la autenticación de dos factores y, sin duda, surgirán más en el futuro.

#### Testigos de hardware

Los testigos de hardware constituyen un método de dos factores en virtud del cual los usuarios cuentan con un elemento físico, como una llave electrónica similar a las de control remoto o un autenticador de tarjetas de crédito. Este hardware proporciona un código simple de un solo uso para autenticación, el cual suele cambiar cada 60 segundos. El usuario debe combinar el código de un solo uso con un NIP secreto para identificarse de forma exclusiva y obtener acceso.

Los testigos de hardware proporcionan muchas de las ventajas de las tarjetas inteligentes, pero su proceso de planeamiento e implantación puede resultar mucho más complejo. Microsoft® Windows Server™ 2003 y Windows® XP no ofrecen compatibilidad integrada con testigos de hardware.

#### Tarjetas inteligentes

Las tarjetas inteligentes tienen el tamaño de una tarjeta de crédito, son de plástico y contienen una microcomputadora y una pequeña cantidad de memoria que proporcionan almacenamiento seguro a prueba de alteraciones para claves privadas y certificados de seguridad X.509. Por lo general, las tarjetas inteligentes tienen 32 ó 64 KB de memoria EEPROM (Electrically Erasable Programmable Read Only Memory, memoria sólo de lectura programable y borrable eléctricamente) y memoria ROM (memoria de sólo lectura), con un 1 KB de RAM. La ROM contiene el sistema operativo de la tarjeta inteligente. La EEPROM contiene las estructuras de directorios y archivos, el subprograma de administración de NIP y el certificado de autenticación. La RAM proporciona memoria para las operaciones de la tarjeta, como el cifrado y el descifrado.

Para la autenticación en un equipo o a través de una conexión de acceso remoto, el usuario inserta la tarjeta inteligente en el lector correspondiente y especifica el NIP. El usuario no podrá obtener acceso si sólo utiliza el NIP o la tarjeta inteligente. Los NIP asociados a las tarjetas inteligentes no son susceptibles de sufrir ataques basados en la "fuerza bruta" de procesamiento, dado que la tarjeta inteligente se bloquea al cabo de varios intentos fallidos en la especificación del NIP. Dado que los NIP suelen tener ocho caracteres como máximo, suelen ser más fáciles de recordar que las contraseñas largas compuestas de caracteres aleatorios. Las tarjetas inteligentes constituyen el mecanismo de autenticación de dos factores preferido por Microsoft.

**Nota:** Los NIP de las tarjetas inteligentes no tienen por qué ser numéricos. Los kits de desarrollo de los fabricantes de tarjetas inteligentes permiten especificar el número de caracteres alfabéticos, numéricos, en mayúsculas, minúsculas o no alfanuméricos que se necesitan.

Microsoft implanta tarjetas inteligentes para administradores de dominios y para el acceso remoto a recursos de red, y tiene un gran interés en fomentar esta práctica como parte de la iniciativa de defensa exhaustiva. Servicios de consultoría de Microsoft, Soporte técnico Premier, Servicios de soporte al cliente, socios de Microsoft y otros proveedores de soluciones animan a las organizaciones a que utilicen las tarjetas inteligentes para proteger el acceso a sus redes.

En la siguiente lista se resumen los pasos necesarios que debe seguir un administrador de redes para implantar una solución basada en tarjetas inteligentes:

-   Habilitar la compatibilidad de los servidores de destino con inicios de sesión interactivo, secundario y de escritorio remoto con cuentas preparadas para tarjetas inteligentes.

-   Identificar qué administradores deben utilizar una cuenta de administrador de nivel de dominio habilitada para el uso de tarjetas inteligentes.

-   Implantar lectores de tarjetas inteligentes.

-   Desarrollar un proceso seguro para distribuir las tarjetas inteligentes e inscribir a los administradores.

En la siguiente lista se resume el proceso necesario para integrar una solución basada en tarjetas inteligentes para el acceso remoto.

-   Actualizar los servidores de acceso remoto para que admitan la autenticación con tarjetas inteligentes.

-   Identificar qué usuarios deben utilizar tarjetas inteligentes para el acceso remoto.

-   Implantar lectores de tarjetas inteligentes.

-   Distribuir tarjetas inteligentes a los administradores que corresponda e inscribir a los usuarios remotos.

[](#mainsection)[Principio de la página](#mainsection)

### Requisitos previos para la implantación

Para implantar un sistema de tarjetas inteligentes es necesario un planteamiento con el que se garantice que las organizaciones tienen en cuenta todos los problemas antes de iniciar la fase de implantación. En esta sección se describen los requisitos previos más frecuentes, aunque quizá haya requisitos adicionales en su entorno.

#### Identificación de cuentas

La identificación de los usuarios y grupos que precisan acceso con tarjeta inteligente es una parte importante en el proceso de implantación de un sistema basado en tarjetas inteligentes.

**Nota:** Pueden omitir este paso las organizaciones que cuentan con el presupuesto y cumplen los requisitos de seguridad necesarios para implantar el acceso mediante tarjetas inteligentes para todos los usuarios.

Entre los grupos y usuarios que necesiten tarjetas inteligentes pueden encontrarse los siguientes:

-   Administradores de dominio para todos los dominios del bosque

-   Administradores de esquema

-   Administradores de organización

-   Administradores de bases de datos

-   Administradores de recursos humanos

-   Usuarios con acceso remoto

-   Usuarios con acceso de usuario o administrativo a recursos importantes, como datos de contabilidad o información financiera.

En una organización también puede ser necesario el acceso mediante tarjeta inteligente para usuarios y grupos no incluidos en la lista anterior, como los miembros del consejo de administración. La identificación de estas cuentas en una fase temprana del proceso contribuye a definir el alcance del proyecto y a controlar los costos.

Para identificar las cuentas de especial importancia es necesario que defina cuándo deben utilizarse las tarjetas inteligentes. Por ejemplo, un procedimiento de seguridad recomendado aconseja que los administradores tengan dos cuentas de usuario: Una cuenta estándar para las tareas cotidianas, como el correo electrónico, y una cuenta de nivel de administrador para el mantenimiento de los servidores y otras tareas administrativas. Normalmente, el administrador iniciará sesión con la cuenta de nivel de usuario y utilizará el servicio de inicio de sesión secundario para llevar a cabo tareas administrativas. El administrador también puede utilizar el componente Escritorio remoto para administración de Windows Server 2003, que admite inicios de sesión con tarjetas inteligentes. Para obtener más información acerca de las cuentas de administrador, consulte la sección Identificación de cuentas de administrador y grupos, en el Capítulo 3, "Uso de tarjetas inteligentes para la protección de las cuentas de los administradores".

#### Compatibilidad con la infraestructura de tarjetas inteligentes

Las tarjetas inteligentes necesitan una infraestructura apropiada que admita el sistema operativo y los elementos de red. Microsoft ofrece compatibilidad con las implantaciones de soluciones de tarjeta inteligente que utilizan los siguientes componentes:

-   Servicios de Certificate Server de Microsoft o infraestructura de claves públicas (PKI) externa

-   Plantillas de certificado

-   Windows Server 2003

-   Servicio de directorio Active Directory®

    -   Grupos de seguridad

    -   Directiva de grupo

    -   Estaciones de inscripción y agentes de inscripción

    -   Servidor Web de activación

-   Protocolo de autenticación extensible – Seguridad de la capa de transporte (EAP – TLS), necesarios sólo en el caso de las soluciones de acceso remoto

Entre los componentes adicionales se encuentran las estaciones de inscripción y los agentes de inscripción.

#### Infraestructura de clave pública

Las tarjetas inteligentes necesitan una infraestructura de claves públicas que permita proporcionar certificados con pares de claves pública/privada para la asignación de cuentas en Active Directory. Esta PKI se puede implementar de dos formas: suministrar la infraestructura interna de certificados a una organización externa o utilizar Servicios de Certificate Server en Windows Server 2003. Las organizaciones pueden subcontratar de forma total o parcial el proceso de administración de certificados para las tarjetas inteligentes.

Las organizaciones financieras pueden aprovechar la posibilidad de vincular su infraestructura de claves públicas a una raíz externa de confianza para la comprobación del correo electrónico y para transacciones seguras con organizaciones asociadas. Un método alternativo consiste en utilizar servicios de Certificate Server en Windows Server 2003 para proporcionar la infraestructura de claves públicas.

Para obtener más información acerca de Servicios de Certificate Server en Windows Server 2003, consulte el sitio Web de [infraestructura de claves públicas para Windows Server 2003](http://www.microsoft.com/windowsserver2003/technologies/pki/default.mspx), en la dirección www.microsoft.com/windowsserver2003/technologies/pki/default.mspx

La PKI debe tener un mecanismo que se encargue de la revocación de certificados. La revocación de certificados es necesaria cuando un certificado caduca o cuando un atacante puede haber puesto en peligro un certificado. Cada certificado incluye la ubicación de su lista de revocaciones de certificados (CRL). Para obtener más información acerca de cómo administrar la revocación de certificados, consulte el tema [Administrar la revocación de certificados](http://www.microsoft.com/resources/documentation/windowsserv/2003/standard/proddocs/en-us/sag_cs_procs_revocation.asp) en la dirección www.microsoft.com/resources/documentation/WindowsServ/2003/standard/proddocs/en-us/sag\_CS\_procs\_revocation.asp

##### Plantillas de certificado

Windows Server 2003 proporciona plantillas específicas para la emisión de certificados digitales destinados al uso en tarjetas inteligentes. Puede copiar y personalizar estos certificados de acuerdo con los requisitos de su organización. Las tres plantillas de certificado para el uso de tarjetas inteligentes son:

-   **Agente de inscripción**. Permite que un usuario autorizado solicite certificados para otros usuarios.

-   **Usuario de tarjeta inteligente**. Permite a un usuario iniciar sesión con una tarjeta inteligente y firmar el correo electrónico. También proporciona autenticación de cliente.

-   **Inicio de sesión con tarjeta inteligente**. Permite a un usuario iniciar sesión con una tarjeta inteligente y proporciona autenticación de cliente, pero no permite firmar el correo electrónico.

Windows Server 2003 Enterprise Edition proporciona plantillas de la versión 2 (v2) que se pueden modificar y ampliar para proporcionar múltiples prestaciones, como inicio de sesión, mensajes de correo electrónico firmados y cifrado de archivos. También puede ampliar las plantillas de certificados para que proporcionen información adicional necesaria en su organización, como datos médicos o derechos de pensión. Windows Server 2003 Enterprise Edition admite la inscripción automática, que facilita la administración de tarjetas inteligentes en las grandes organizaciones. Cuando se solicita la renovación de un certificado existe la posibilidad de utilizar el certificado actual para firmar la solicitud.

**Nota:** Microsoft recomienda actualizar una infraestructura de claves públicas (PKI) de Windows Server 2003 a una PKI de Windows Server 2003 con Service Pack 1 (SP1) para aprovechar las características de seguridad mejoradas.

Para obtener más información acerca de las plantillas de certificados, consulte el tema [Plantillas de certificados](http://www.microsoft.com/resources/documentation/windowsserv/2003/standard/proddocs/en-us/sag_ct_topnode.asp), en la dirección www.microsoft.com/resources/documentation/WindowsServ/2003/standard/proddocs/en-us/sag\_ct\_topnode.asp.

##### Windows Server 2003

Microsoft Windows 2000 Server admite tarjetas inteligentes para el acceso remoto y autenticación de administrador para inicio de sesión en consola únicamente. Si se desea implantar tarjetas inteligentes para los administradores, es necesario que en los servidores administrados se ejecute Windows Server 2003, que admite acciones secundarias como el inicio de sesión con tarjetas inteligentes a través de conexiones de protocolo de escritorio remoto (RDP). Este requisito del sistema operativo incluye a los controladores de dominio. Para obtener más información acerca de este requisito, consulte el Capítulo 3: "Uso de tarjetas inteligentes para la protección de las cuentas de los administradores".

##### Active Directory

Active Directory es un componente fundamental para la implantación de sistemas basados en tarjetas inteligentes. En Windows Server 2003, Active Directory permite exigir un inicio de sesión interactivo con tarjetas inteligentes. Asimismo, ofrece la posibilidad de asignar cuentas a certificados. Esta capacidad para asignar cuentas de usuario a certificados vincula la clave privada de la tarjeta inteligente al certificado integrado en Active Directory. La presentación de credenciales de tarjeta inteligente en el inicio de sesión requiere que Active Directory establezca una correspondencia entre esa tarjeta en particular y una única cuenta de usuario. Para obtener más información acerca de la asignación de certificados, consulte el tema [Asignar certificados a cuentas de usuario](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/deployguide/en-us/dssch_pki_cyek.asp), en la dirección www.microsoft.com/resources/documentation/WindowsServ/2003/all/deployguide/en-us/dssch\_pki\_cyek.asp.

Active Directory también admite grupos de seguridad y la Directiva de grupo para facilitar la administración del proceso de inicio de sesión con tarjetas inteligentes y la emisión de esas tarjetas.

###### Grupos de seguridad

El proceso de implementación y administración de tarjetas inteligentes es significativamente más fácil si se usan grupos de seguridad en Active Directory para organizar a los usuarios. Por ejemplo, una tarjeta inteligente típica puede requerirle que cree los siguientes grupos de seguridad:

-   **Agentes de inscripción de tarjetas inteligentes**. Los agentes de inscripción de tarjeta inteligente son los responsables de la distribución de tarjetas inteligentes a los usuarios. En la sección siguiente se describen detalladamente los agentes de inscripción.

-   **Ensayo de tarjetas inteligentes**. En el grupo de ensayo de tarjetas inteligentes se encuentran todos los usuarios autorizados para recibir tarjetas inteligentes, pero para los que ningún agente de inscripción ha inscrito y activado tarjetas.

-   **Usuarios de tarjetas inteligentes**. Este grupo contiene todos los usuarios que han terminado el proceso de inscripción y tienen una tarjeta inteligente activada. El agente de inscripción desplaza al usuario transfiere el grupo de ensayo de tarjeta inteligente al grupo de usuarios de tarjeta inteligente.

Para obtener más información acerca de cómo crear grupos, consulte el tema [Lista de comprobación: Crear un grupo](http://www.microsoft.com/resources/documentation/windowsserv/2003/standard/proddocs/en-us/sag_adgroups_checklist_create_group.asp), en la dirección www.microsoft.com/resources/documentation/WindowsServ/2003/standard/proddocs/en-us/sag\_adgroups\_checklist\_create\_group.asp.

###### Directiva de grupo

La Directiva de grupo permite aplicar una configuración a varios equipos. Puede configurar el requisito de utilización de tarjetas inteligentes para inicio de sesión interactivo en un objeto de directiva de grupo (GPO) y después aplicar ese GPO a unidades o sitios de la organización en Active Directory. Para obtener más información acerca de cómo utilizar la Directiva de grupo, consulte el Capítulo 3: "Uso de tarjetas inteligentes para la protección de las cuentas de los administradores".

##### Estaciones de inscripción y agentes de inscripción

Una organización puede utilizar una interfaz basada en Web para emitir tarjetas inteligentes o inscribir a usuarios, que deberán especificar sus credenciales para obtener una tarjeta inteligente. En la práctica, sin embargo, esta disposición reduce el nivel de seguridad de la tarjeta inteligente al de las credenciales que se presentan a la interfaz Web. La solución preferida es crear estaciones de inscripción y designar uno o varios administradores como agentes de inscripción.

**Nota:** Las organizaciones pueden utilizar una interfaz Microsoft Management Console (MMC) o desarrollar sus propias aplicaciones de activación.

Una estación de inscripción típica es un equipo que tiene conectados dos lectores de tarjetas inteligentes. Un lector permite al agente de inscripción iniciar sesión y el otro emite nuevas tarjetas inteligentes para los usuarios. Las estaciones de inscripción requieren un certificado de inscripción y deben tener permiso para el acceso a las plantillas de certificados. La estación de inscripción tiene una configuración de Directiva de grupo que exige que se cierre la sesión cuando el agente de inscripción quita su tarjeta inteligente.

Un administrador designado asume la función del agente de inscripción y utiliza su tarjeta inteligente para iniciar sesión en la estación de inscripción. A continuación abre la página Web correspondiente a los servicios de certificados, comprueba la identidad del usuario, inscribe al usuario y emite la tarjeta inteligente inscrita.

Las organizaciones deben estudiar detenidamente el número de estaciones de inscripción necesarias, así como la ubicación de éstas. La organización podría ubicar una estación de inscripción en las oficinas de su departamento de seguridad junto con los servicios que emiten pases de acceso a las instalaciones u otro tipo de pases de seguridad. Para agilizar la implantación inicial en una gran organización, los equipos de agentes de inscripción pueden utilizar PC portátiles como estaciones de inscripción móviles en las sucursales.

**Nota:** Para reducir la complejidad administrativa y controlar la inscripción de tarjetas inteligentes, se recomienda restringir el número de agentes y estaciones de inscripción al mínimo necesario para la implantación.

##### Servidor Web de activación

Un servidor Web de activación es un componente personalizado que permite a los usuarios activar las nuevas tarjetas inteligentes mediante el restablecimiento del NIP. Algunos kits de desarrollo de software (SDK) que ofrecen los fabricantes incluyen herramientas de ayuda para la creación de un servidor Web de activación. Microsoft no proporciona el componente del servidor de activación.

Para restablecer el NIP, el usuario ejecuta una utilidad de proveedor de servicios de cifrado (CSP) que genera una cadena hexadecimal de desafío desde la tarjeta inteligente. El usuario escribe esta cadena de desafío en un campo en la página Web y el servidor Web de activación genera una respuesta. El usuario escribe la respuesta en el campo correspondiente de la utilidad que permitirá entonces al usuario establecer el NIP de la tarjeta inteligente.

El servidor Web de activación también puede formar parte del proceso de administración. Los operadores del departamento de soporte pueden aplicar este proceso para desbloquear tarjetas cuando el usuario haya especificado incorrectamente el NIP un número máximo de veces. En este caso, el usuario lee el desafío para el operador del departamento de soporte, quien devuelve una respuesta.

##### EAP-TLS

En los entornos de seguridad basados en certificados se utiliza EAP-TLS (EAP-Seguridad en el nivel de transporte) para proporcionar la autenticación y el método de determinación de claves más seguros. EAP-TLS proporciona autenticación mutua, negociación del método de cifrado y determinación de las claves cifradas entre el cliente y el autenticador. RFC 2284 proporciona una descripción detallada del protocolo EAP.

#### Evaluar las tarjetas inteligentes

Lo más importante en la evaluación de las tarjetas inteligentes es asegurarse de que el modelo elegido admite la longitud que se ha previsto para las claves. Windows Server 2003 admite longitudes de clave de certificado comprendidas entre 384 bits (seguridad de bajo nivel) y 16.384 bits (máxima seguridad).

Los certificados que tienen claves de longitud superior proporcionan una mayor seguridad que los que tienen claves más cortas, pero también aumentan considerablemente el inicio de sesión con una tarjeta inteligente. Las limitaciones de memoria en la tarjeta inteligente también imponen una restricción a la longitud máxima de las claves de memoria que se pueden utilizar.

Una longitud de clave de certificado de 1.024 bits resulta adecuada para proteger cuentas de administrador o el acceso remoto. Un certificado con una clave de 1.024 bits ocupa, aproximadamente, 2,5 KB de espacio en la memoria de la tarjeta inteligente. Entre otros requisitos de memoria se incluye el sistema operativo (16 KB), aplicaciones del fabricante para la tarjeta inteligente, como el CSP (8 KB), y la estructura de archivos y directorios de la tarjeta inteligente (4 KB). En consecuencia, es poco probable que las tarjetas inteligentes con menos de 32 KB de memoria sean aptas para el almacenamiento de certificados de inicio de sesión y proporcionen la funcionalidad necesaria para ampliar una solución de tarjeta inteligente.

El segundo factor que se debe tener en cuenta es si la tarjeta dispone de compatibilidad integrada con Windows Server 2003 y Windows XP. Antes de adquirir tarjetas inteligentes, discuta con el fabricante los requisitos que le interesan.

**Nota:** Debe obtener las tarjetas inteligentes directamente de los fabricantes respectivos. Las tarjetas inteligentes no pueden obtenerse a través de Microsoft.

Aunque Windows XP y la familia Windows Server 2003 dispongan de compatibilidad integrada con algunas tarjetas inteligentes, otras tarjetas inteligentes con cifrado basadas en RSA también funcionan correctamente con esos sistemas operativos. Para las tarjetas con las que Windows no es compatible de forma nativa, el fabricante de la tarjeta debe implantar un CSP para la tarjeta que utilice la CAPI.

Para obtener más información acerca de la evaluación de tarjetas inteligentes, consulte el tema sobre [evaluación de tarjetas inteligentes y lectores](http://technet2.microsoft.com/windowsserver/en/library/0eae38ec-d6e5-4ca7-96a3-42f2fd6c6e741033.mspx), en la dirección http://technet2.microsoft.com/windowsserver/en/library/0eae38ec-d6e5-4ca7-96a3-42f2fd6c6e741033.mspx.

##### Administración de NIP

Un usuario puede cambiar el NIP de una tarjeta inteligente cuando lo desee mediante una utilidad que permite al CSP mostrar el cuadro de diálogo del NIP de la clave privada. El usuario especifica el NIP antiguo y el NIP nuevo dos veces. Como a los usuarios les resulta más fácil recordar los NIP si los seleccionan personalmente, deben disponer de herramientas que les permitan cambiar de NIP.

**Nota:** Quizá sea preciso recordar a los usuarios que no establezcan NIP demasiado fáciles de adivinar, como su fecha de nacimiento, la matrícula de su automóvil o alguno de sus números de teléfono.

El usuario es responsable de la administración de los NIP a través de los servicios que presta el CSP. Windows XP y la familia de sistemas operativos Windows Server 2003 no administran NIP. Para conocer las herramientas de administración de NIP y las instrucciones correspondientes, póngase en contacto con el fabricante de las tarjetas inteligentes.

La mayoría de los fabricantes ofrecen tarjetas inteligentes que se integran directamente con Windows 2000 o posterior sin que sea necesaria ninguna tarea adicional de personalización o programación. Los fabricantes suministran estas tarjetas inteligentes con un NIP predeterminado y ofrecen la posibilidad de establecer restricciones para la tarjeta; por ejemplo, que sea necesario un restablecimiento del NIP en el momento de la inscripción. Sin embargo, en el caso de muchas empresas se considera que esta disposición no es aceptable.

Para crear un NIP más complejo y seguro, especifique con las herramientas de administración de NIP que los usuarios elijan un NIP con una longitud de entre cinco y ocho caracteres. Asegúrese de que el fabricante de tarjetas inteligentes seleccionado admite un NIP de hasta ocho caracteres.

##### Kits de desarrollo de software para tarjetas inteligentes

Microsoft no proporciona ninguna solución de serie para la implantación de tarjetas inteligentes. Quizá deba realizar más operaciones de personalización si su entorno lo requiere.

Los fabricantes de tarjetas inteligentes ofrecen kits de desarrollo de software y herramientas de personalización con las que las organizaciones puedan personalizar sus implantaciones de tarjetas inteligentes. Por ejemplo, los desarrolladores tienen la posibilidad de utilizar un kit de desarrollo de software para emitir tarjetas inteligentes en estado pendiente. Cuando el agente de inscripción emite la tarjeta, el usuario la activa y cambia el NIP. Si desea aprovechar el mayor nivel de seguridad que ofrece este método, deberá prever tareas de personalización y programación adicionales.

#### Evaluar lectores de tarjetas inteligentes

El factor más importante a la hora de seleccionar un lector de tarjetas inteligentes es que se adapte a la finalidad que se pretende. Por ejemplo, una estación de trabajo moderna situada en el escritorio de un administrador tiene dos conexiones USB o más, por lo que es probable que un lector de tarjetas inteligentes USB constituya la opción más adecuada. El usuario puede conectar el lector de tarjetas inteligentes junto al monitor o en otra ubicación que resulte práctica. Los usuarios que establezcan conexiones de acceso remoto desde equipos portátiles suelen preferir los lectores de tarjetas inteligentes con formato PC Card.

Los teclados pueden incluir lectores de tarjetas inteligentes que también funcionen a través de una interfaz USB. Estos teclados son aptos para un solo equipo. Pueden funcionar con varios equipos instalados en bastidores de servidor si se utilizan conmutadores de teclado, vídeo y mouse (KVM) equipados con USB. Consulte al fabricante del conmutador KVM si el dispositivo admite la autenticación con tarjetas inteligentes para varios servidores.

Windows XP y la familia Windows Server 2003 admiten los lectores de tarjetas inteligentes que se enumeran en la tabla siguiente. Windows instala los controladores adecuados al detectar el hardware del lector de tarjetas inteligentes Plug and Play.

**Nota:** Microsoft recomienda utilizar lectores de tarjetas inteligentes que hayan obtenido el logotipo de compatibilidad con Windows.

**Tabla 2.1: Lectores de tarjetas inteligentes compatibles con Windows Server 2003**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Marca</th>
<th>Modelo</th>
<th>Interfaz</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">American Express</td>
<td style="border:1px solid black;">GCR435</td>
<td style="border:1px solid black;">USB</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Bull</td>
<td style="border:1px solid black;">SmarTLP3</td>
<td style="border:1px solid black;">Serie</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Compaq</td>
<td style="border:1px solid black;">Lector serie</td>
<td style="border:1px solid black;">Serie</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Gemplus</td>
<td style="border:1px solid black;">GCR410P</td>
<td style="border:1px solid black;">Serie</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Gemplus</td>
<td style="border:1px solid black;">GPR400</td>
<td style="border:1px solid black;">PCMCIA</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Gemplus</td>
<td style="border:1px solid black;">GemPC430</td>
<td style="border:1px solid black;">USB</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Hewlett Packard</td>
<td style="border:1px solid black;">ProtectTools</td>
<td style="border:1px solid black;">Serie</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Litronic</td>
<td style="border:1px solid black;">220P</td>
<td style="border:1px solid black;">Serie</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Schlumberger</td>
<td style="border:1px solid black;">Reflex 20</td>
<td style="border:1px solid black;">PCMCIA</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Schlumberger</td>
<td style="border:1px solid black;">Reflex 72</td>
<td style="border:1px solid black;">Serie</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Schlumberger</td>
<td style="border:1px solid black;">Reflex Lite</td>
<td style="border:1px solid black;">Serie</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SConnection Manager Microsystems</td>
<td style="border:1px solid black;">SCR111</td>
<td style="border:1px solid black;">Serie</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SConnection Manager Microsystems</td>
<td style="border:1px solid black;">SCR200</td>
<td style="border:1px solid black;">Serie</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SConnection Manager Microsystems</td>
<td style="border:1px solid black;">SCR120</td>
<td style="border:1px solid black;">PCMCIA</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">SConnection Manager Microsystems</td>
<td style="border:1px solid black;">SCR300</td>
<td style="border:1px solid black;">USB</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Systemneeds</td>
<td style="border:1px solid black;">Externo</td>
<td style="border:1px solid black;">Serie</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Omnikey AG</td>
<td style="border:1px solid black;">2010</td>
<td style="border:1px solid black;">Serie</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Omnikey AG</td>
<td style="border:1px solid black;">2020</td>
<td style="border:1px solid black;">USB</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Omnikey AG</td>
<td style="border:1px solid black;">4000</td>
<td style="border:1px solid black;">PCMCIA</td>
</tr>
</tbody>
</table>
  
**Nota:** Los lectores de tarjetas inteligentes que utilizan una interfaz serie necesitan que se reinicie el equipo después de la instalación. Este requisito puede no ser aceptable para implantaciones de servidor.
  
Microsoft no admite ni recomienda el uso de lectores de tarjetas inteligentes que no sean Plug and Play. Si utiliza un lector de ese tipo, debe obtener instrucciones para la instalación (esto incluye el software del controlador del dispositivo asociado) directamente del fabricante del lector de tarjetas inteligentes.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### El caso de la entidad financiera Woodgrove National Bank
  
En los restantes capítulos de esta guía se utiliza el caso del banco Woodgrove National Bank. Woodgrove National Bank es un banco ficticio de inversiones de ámbito global, líder en su sector, que en su papel como intermediario financiero tiene clientes institucionales, corporativos, gubernamentales y particulares. Sus actividades incluyen valores, ventas y operaciones bursátiles, servicios de asesoramiento financiero, investigación relacionada con la inversión, capital de riesgo y servicios de correduría para instituciones financieras.
  
Woodgrove National Bank tiene más de 15.000 empleados en más de 60 oficinas distribuidas por todo el mundo. Tiene sedes corporativas (centros de concentración) con un gran número de empleados en Nueva York (5.000 empleados), Londres (5.200 empleados) y Tokio (500 empleados). Cada centro de concentración da soporte a varias oficinas.
  
Aunque Woodgrove National Bank cuenta con un entorno de servidor mixto que en el que se utilizan Windows Server y UNIX, su infraestructura se ejecuta sobre una red troncal basada en Windows Server. Tienen 1.712 servidores Windows, en la mayoría de los cuales se ejecuta Windows Server 2003. Alrededor de un centenar de estos servidores están conectados a Internet. En la organización también hay 18.000 estaciones de trabajo y 2.000 equipos portátiles. La organización está estableciendo una arquitectura de referencia normalizada en torno a Windows XP Professional con SP2 y un estándar para servidores basado en Windows Server 2003 con SP1.
  
La mayoría de los servidores se encuentran en tres sedes corporativas. La organización ha distribuido las estaciones de trabajo y los equipos portátiles por todas las ubicaciones. Los equipos portátiles se trasladan con frecuencia entre países y regiones. La entidad Woodgrove National Bank utiliza Microsoft Systems Management Server 2003 para administrar equipos de escritorio y portátiles, y Microsoft Operations Manager (MOM) 2005 para administrar los servidores.
  
Woodgrove National Bank debe ajustarse a los requisitos de la normativa financiera vigente en cada país o región en que opera. También debe cumplir con las leyes de protección de datos y demostrar eficacia en la seguridad de las operaciones.
  
En el resto de este documento se describen las opciones de diseño disponibles para la entidad Woodgrove National Bank ante el planeamiento de la implantación del sistema de tarjetas inteligentes.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
En este capítulo se han descrito consideraciones comunes necesarias para planear soluciones de autenticación con tarjetas inteligentes. Esto incluye los requisitos previos, como la infraestructura de claves públicas y Active Directory. Se ha destacado la necesidad de evaluar las tarjetas inteligentes y los lectores de tarjetas inteligentes, y se han tratado los aspectos relacionados con la memoria de las tarjetas inteligentes, la longitud de las claves y la administración de los NIP. Los siguientes capítulos se concentran en los aspectos exclusivos del uso de las tarjetas inteligentes para ayudar a proteger las cuentas de administrador y el acceso remoto a redes.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 3: Uso de tarjetas inteligentes para la protección de las cuentas de los administradores
  
Microsoft® Windows Server™ 2003 ayuda a las organizaciones a proteger las cuentas administrativas a través de un conjunto de características de seguridad específicas. Además del requisito de que los administradores inicien sesión con tarjetas inteligentes, Windows Server 2003 admite la autenticación con tarjetas inteligentes con las acciones secundarias que se enumeran:
  
-   Crear una unidad asignada con el comando **net use**.
  
-   Utilizar el servicio de inicio de sesión secundario escribiendo **runas** en el símbolo del sistema.
  
-   Instalar el servicio de directorio Active Directory® mediante el Asistente para instalación de Active Directory (al que puede tener acceso si se escribe **dcpromo** en el símbolo del sistema).
  
-   Iniciar sesión a través de las sesiones de Escritorio remoto de Windows Server 2003.
  
-   Iniciar sesión a través de las sesiones de Terminal Server de Windows Server 2003.
  
**Nota:** Aunque Microsoft Windows® 2000 admite el acceso con tarjetas inteligentes para la autenticación, no es compatible con estas características adicionales, que sólo están disponibles en Windows Server 2003.
  
[](#edaar)[Planteamientos para proteger cuentas de administrador con tarjetas inteligentes](#edaar)  
[](#ecaas)[Problemas y requisitos](#ecaas)  
[](#ebaat)[Diseño de la solución](#ebaat)
  
### Planteamientos para proteger cuentas de administrador con tarjetas inteligentes
  
La compatibilidad de Windows Server 2003 con la autenticación mediante tarjetas inteligentes de acciones secundarias permite una mejor separación de las cuentas de usuario y administrador. Para las acciones cotidianas, los administradores pueden iniciar sesión en estaciones de trabajo con cuentas no administrativas. Si deben realizar una tarea administrativa, los administradores pueden utilizar sus tarjetas inteligentes para autenticar la operación mediante una acción secundaria. Esta disposición resulta más segura y práctica que si el administrador tiene que especificar un nombre de usuario o una contraseña o si debe cerrar sesión y volver a iniciarla con una cuenta de administrador.
  
#### Identificación de cuentas y grupos de administradores
  
En la implantación de tarjetas inteligentes para administradores es preciso que una organización identifique las cuentas de administrador que requieren autenticación de dos factores. Para ejecutar este paso correctamente, deben comprenderse las características de las distintas cuentas y de los grupos de administradores en Windows XP y Windows Server 2003.
  
Los grupos permiten a los administradores administrar varias cuentas de usuario a la vez. Microsoft Windows NT® y los sistemas operativos posteriores incluyen grupos de seguridad con derechos administrativos integrados.
  
Estos grupos de seguridad pueden ser locales (equipos unidos a dominios, como estaciones de trabajo y servidores miembros) o grupos predeterminados (en controladores de dominio). Las cuentas de administrador reciben los privilegios por la pertenencia a uno o varios de estos grupos de seguridad.
  
##### Grupos locales
  
Los grupos locales en equipo unidos a dominios presentan distintos niveles de derechos administrativos. Estas recomendaciones son:
  
-   **Administradores**. Los miembros de este grupo tienen un control completo del equipo local. La cuenta de usuario Administrador forma parte de este grupo de forma predeterminada. Si el equipo es miembro de un dominio, el grupo Admins. del dominio correspondiente también será miembro de este grupo.
  
-   **Operadores de copia de seguridad (todos los tipos de equipos)**. Los miembros de este grupo pueden omitir los permisos del sistema de archivos NTFS para realizar copias de seguridad de archivos y carpetas. Los operadores de copia de seguridad también pueden apagar los servidores miembros.
  
-   **Usuarios avanzados**. Los miembros de este grupo tienen derechos administrativos limitados sobre los recursos de una estación de trabajo local o un servidor miembro. También pueden apagar un servidor miembro.
  
-   **Operadores de impresión**. Los miembros de este grupo pueden administrar servidores de impresión, impresoras y trabajos de impresión. También pueden apagar un servidor miembro.
  
Para obtener una descripción completa de los grupos predeterminados en Windows Server 2003, consulte el tema [Grupos locales predeterminados](http://www.microsoft.com/resources/documentation/windowsserv/2003/standard/proddocs/en-us/lsm_local_groups.asp), en la dirección www.microsoft.com/resources/documentation/WindowsServ/2003/standard/proddocs/en-us/lsm\_local\_groups.asp.
  
Las directivas de seguridad de la organización deben definir qué miembros de los grupos Administradores, Operadores de servidores y Usuarios avanzados necesitan tarjeta inteligentes para el inicio de sesión y las tareas de administración.
  
##### Grupos predeterminados
  
Cada dominio cuenta con varios grupos predeterminados que proporcionan funciones administrativas en los controladores de dominio. Entre estos grupos se encuentran los siguientes:
  
-   **Administradores**. Los miembros de este grupo tienen pleno control administrativo sobre los controladores de dominio. La cuenta Administrador y el grupo Admins. del dominio son miembros de este grupo de forma predeterminada.
  
-   **Operadores de copia de seguridad**. Los miembros de este grupo pueden omitir los permisos del sistema de archivos NTFS para realizar copias de seguridad de archivos y carpetas. Los operadores de copia de seguridad también pueden iniciar sesión localmente y apagar los controladores de dominio.
  
-   **Operadores de servidores**. Este grupo cuenta con derechos administrativos limitados sobre los controladores de dominio, de modo similar a lo que ocurre con los Usuarios avanzados en las estaciones de trabajo. Los operadores de servidores pueden iniciar sesión localmente y apagar los controladores de dominio.
  
-   **Operadores de impresión**. Los miembros de este grupo administran servidores de impresión, impresoras y trabajos de impresión. También pueden iniciar sesión localmente y apagar los controladores de dominio.
  
-   **Operadores de cuentas**.** **Los miembros de este grupo tienen derechos limitados para administrar las cuentas y los grupos de usuarios. Pueden iniciar sesión de forma interactiva pero no tienen la posibilidad de apagar los controladores de dominio.
  
Para obtener más información acerca de los grupos predeterminados, consulte el tema sobre [Grupos predeterminados](http://go.microsoft.com/fwlink/?linkid=81737), en la dirección http://go.microsoft.com/fwlink/?LinkId=81737.
  
Las directivas de la organización deben especificar que el uso de tarjetas inteligentes para tareas de administración sea un requisito para todos los miembros de estos grupos.
  
##### Grupos predeterminados de dominios y bosques
  
Además de los grupos predeterminados, con la creación de un bosque de Active Directory se configuran los siguientes grupos de seguridad:
  
-   **Admins. del dominio**. Los miembros de este grupo tienen pleno control sobre todos los objetos del dominio. Cada dominio posterior del bosque tiene también un grupo Admins. del dominio.
  
-   **Administradores de empresa (sólo en el dominio raíz del bosque)**.** **Los miembros de este grupo tienen pleno control sobre todos los objetos del bosque.
  
-   **Administradores de esquema (sólo en el dominio raíz del bosque)**. Los miembros de este grupo pueden crear clases y atributos en el esquema, así como administrar el maestro de operaciones de esquema.
  
    **Nota:** Para aumentar el nivel de seguridad, procure que el número de miembros de estos grupos sea el mínimo posible.
  
Todos los miembros de estos grupos deben necesitar tarjetas inteligentes para la administración.
  
#### Requerir la tarjeta inteligente para el inicio de sesión interactivo
  
Existen dos medios para requerir una tarjeta inteligente en el inicio de sesión interactivo. Puede configurar:
  
-   Propiedades de cuentas de usuario en Usuarios y equipos de Active Directory.
  
-   Directiva de grupo para equipos específicos o para grupos de equipos específicos.
  
En la mayoría de los entornos resulta más fácil administrar la Directiva de grupo.
  
##### Propiedades de cuentas de usuarios    
  
Puede configurar como requisito para cualquier cuenta de usuario el uso de una tarjeta inteligente para el inicio de sesión interactivo. Para ello, en Usuarios y equipos de Active Directory haga doble clic en el usuario, haga clic en la ficha **Cuenta** y, en **Opciones de cuenta**, active la casilla de verificación **La tarjeta inteligente es necesaria para un inicio de sesión interactivo**. Con la activación de esta opción cambia la contraseña del usuario a un valor complejo aleatorio y se establece la propiedad **La contraseña nunca caduca**. Si después desactiva el requisito de uso de la tarjeta inteligente, también deberá restablecer la contraseña del usuario.
  
Como al establecer el requisito de uso de tarjeta inteligente se restablece la contraseña del usuario con un valor desconocido, el usuario ya no podrá utilizar la combinación de nombre de usuario y contraseña que conocía para iniciar sesión en el dominio. En consecuencia, el usuario no podrá iniciar sesión en programas como Microsoft Outlook® Web Access para Microsoft Exchange Server 2003 con un nombre de usuario y una contraseña.
  
Se puede utilizar una secuencia de comandos que habilite esta opción durante la inscripción. Sin embargo, este método exige desarrollar secuencias de comandos adecuadas que puedan habilitar y deshabilitar el requisito de tarjetas inteligentes para usuarios específicos.
  
Con el requisito de uso de tarjeta inteligente seleccionado para la cuenta, el administrador debe utilizar una tarjeta inteligente para iniciar sesión de forma interactiva en cualquier equipo del dominio, no sólo en los servidores protegidos. Esto puede resultar poco práctico si no todos los equipos tienen lectores de tarjetas inteligentes conectados.
  
Si exige el uso de tarjetas inteligentes a través de las propiedades de las cuentas de usuario, los administradores no podrán administrar de forma remota equipos en los que se ejecute Windows 2000 Server. Las sesiones de servicios de Terminal Server de Windows 2000 Server no admiten la redirección de las tarjetas inteligentes, por lo que el administrador deberá iniciar sesión localmente para administrar los equipos en los que se ejecute Windows 2000. Este requisito podría suponer un trastorno si el administrador se encuentra en una ubicación distinta de la del servidor.
  
##### Directiva de grupo
  
Un planteamiento que facilitaría la administración consiste en utilizar la configuración de Directiva de grupo para requerir el uso de tarjetas inteligentes en ciertos equipos para el inicio de sesión interactivo, además de controlar qué ocurre cuando un usuario extrae una tarjeta inteligente. Con esta configuración puede crear objetos de directiva de grupo (GPO) y vincularlos a la unidad organizativa que contiene el equipo para el que se requiere el inicio de sesión con tarjeta inteligente. La ruta de acceso a las opciones relacionadas con las tarjetas inteligentes en la directiva de grupo es Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\Opciones de seguridad. La configuración es **Inicio de sesión interactivo: Requiere una tarjeta inteligente** e **Inicio de sesión interactivo: Comportamiento de extracción de tarjeta inteligente**.
  
**Nota:** Para esta opción se necesita Windows XP con Service Pack 2 o una actualización de la configuración. Para obtener más información, consulte el artículo de Knowledge Base acerca de la [actualización de la opción de seguridad de Windows XP "Inicio interactivo: requiere tarjeta inteligente"](http://support.microsoft.com/?id=834875), en la dirección http://support.microsoft.com/?id=834875.
  
Para mayor seguridad, debe especificar como requisito el uso de tarjetas inteligentes para el inicio de sesión interactivo y después establecer en la directiva de extracción de tarjeta inteligente que se bloquee la estación de trabajo o se cierre la sesión del usuario. Esta configuración de Directiva de grupo debe pasar a formar parte de un GPO personalizado para los administradores. Los GPO se pueden aplicar en el nivel de sitio, dominio o unidad organizativa. En la mayoría de los casos, los GPO que aplican opciones de configuración de tarjeta inteligente lo hacen en el nivel de las unidades organizativas.
  
**Nota:** Microsoft recomienda no modificar la Directiva predeterminada de controladores de dominio ni la Directiva predeterminada de dominio para incluir opciones de configuración de tarjetas inteligentes o cualquier otro cambio de directiva. Cree siempre un nuevo GPO o utilice uno ya existente si desea establecer la configuración de Directiva de grupo para el inicio de sesión con tarjetas inteligentes.
  
La configuración de Directiva de grupo para las tarjetas inteligentes controla el inicio de sesión interactivo y no afecta al acceso a un servidor a través de la red. El inicio de sesión interactivo incluye la conexión a través de Escritorio remoto o de servicios de Terminal Server.
  
Microsoft recomienda implantar las tarjetas inteligentes para los administradores con otros mecanismos de control, como IPsec o Directiva de grupo, a fin de impedir la administración de un servidor con herramientas de administración remota, como las de Microsoft Management Console (MMC).
  
#### Administración del acceso con tarjetas inteligentes en varios dominios y bosques
  
La implantación de tarjetas inteligentes para los administradores requiere un conocimiento de los problemas relacionados con el acceso a distintos dominios y bosques. Por ejemplo, los administradores que son miembros del grupo Admins. del dominio en más de un bosque podrían necesitar una tarjeta inteligente para cada bosque del que tienen derechos administrativos. La consecuencia de este requisito puede ser que esos administradores deban llevar consigo varias tarjetas inteligentes.
  
Aunque las tarjetas inteligentes pueden contener más de un certificado, Windows Server 2003 sólo acepta actualmente un certificado de inicio de sesión con una tarjeta inteligente (el certificado de la ranura 0 de la tarjeta inteligente) para cada raíz de certificados de entidad emisora de certificados. Esta restricción puede obligar a algunos administradores de red a llevar consigo varias tarjetas inteligentes, a menos que la organización mantenga relaciones de confianza entre los bosques.
  
#### Protección de los servidores
  
Los equipos en los que se ejecutan servicios, como los de archivo e impresión, bases de datos, correo electrónico y directorios precisan un mayor nivel de seguridad que las estaciones de trabajo. En concreto, debe considerarse la posibilidad de utilizar la autenticación con tarjetas inteligentes para todas las cuentas que administren equipos con las siguientes funciones:
  
-   Controladores de dominio
  
-   Servidores de bases de datos
  
-   Servidores de certificados
  
-   Servidores de archivo e impresión
  
##### Protección de controladores de dominio
  
Los controladores de dominio son los equipos más importantes para la autenticación de dos factores, ya que contienen y controlan toda la información de las cuentas del dominio, a las que aplican las reglas de seguridad. A través de un controlador de dominio expuesto, un atacante podría crear una nueva cuenta, elevar privilegios u obtener acceso a todos los controladores de dominio como administrador.
  
##### Protección de servidores de bases de datos
  
En los servidores de bases de datos se almacena información muy importante para el funcionamiento de una organización. Esta información almacenada podría estar sujeta a estrictos procesos de protección y desprotección, con un seguimiento de auditoría de las solicitudes de acceso a datos. Son ejemplos de servidores de bases de datos aquéllos que almacenan el código fuente de una empresa de software, las fórmulas secretas de un fabricante de bebidas o la información sobre las cuentas de los clientes de una empresa. La autenticación con tarjetas inteligentes debe proteger el acceso a todos los servidores de bases de datos.
  
Una organización deberá identificar los servidores que requieren un alto grado de seguridad y trabajar con sus propietarios para cambiar el tipo de cuenta con que se ejecuta el servicio o la tarea programada, o bien asignar las cuentas y los servidores a grupos especiales de seguridad que tengan más restricciones de acceso y uso.
  
##### Protección de servidores de certificados
  
Los servidores en los que se alojan entidades emisoras de certificados y servicios de Certificate Server deben caracterizarse por un alto nivel de seguridad. Si se pone en peligro la entidad emisora de certificados, se anulará la integridad de la organización y todos los certificados emitidos deberán considerarse no seguros. Los servidores en los que se alojan servicios de Certificate Server deben tener la máxima prioridad por lo que respecta a la seguridad, tanto a través de la red como en los accesos físicos.
  
##### Protección de los servidores de archivo e impresión
  
Un servidor de archivos puede alojar información confidencial y documentos importantes para la empresa. Si se pone en peligro esta información, la empresa puede sufrir pérdidas de ingresos o sanciones de los organismos reguladores competentes. Por supuesto, la autenticación con tarjetas inteligentes debe proteger los servidores de impresión que se utilicen para imprimir facturas o cheques.
  
Para obtener más información acerca de las características de seguridad de Windows Server 2003, consulte la [Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14845), en la dirección http://go.microsoft.com/fwlink/?LinkId=14845
  
#### Instalación de lectores de tarjetas inteligentes en servidores
  
Debe conectar un lector de tarjetas inteligentes a cada uno de los servidores en las que la Directiva de grupo requiera el uso de tarjetas inteligentes para inicios de sesión interactivos. La mayoría de los equipos montados en bastidor tienen en la parte posterior puertos USB que permiten la conexión de lectores de tarjetas inteligentes. Después se puede colocar el lector de tarjetas inteligentes en la parte frontal del bastidor para facilitar el acceso al usuario. Es importante etiquetar claramente los lectores de tarjetas inteligentes, de modo que los administradores sepan qué lector pertenece a cada servidor.
  
Si un administrador tiene que iniciar sesión en otro servidor, deberá extraer su tarjeta inteligente del primer lector e insertarla en el lector conectado al otro equipo. Esta incomodidad hace que la administración de servidores con Escritorio remoto resulte mucho más atractiva.
  
#### Distribución de tarjetas inteligentes
  
El planeamiento del proceso de distribución de tarjetas inteligentes para administradores incluye las siguientes actividades:
  
-   Crear grupos adecuados para la distribución de tarjetas inteligentes.
  
-   Nombrar a responsables de seguridad que puedan actuar como agentes de inscripción.
  
-   Seleccionar un método adecuado para el transporte de las tarjetas.
  
-   Realizar comprobaciones de identificación rigurosas.
  
Debe crearse un grupo de seguridad de ensayo que contenga las cuentas de administrador seleccionadas. También necesita un grupo de seguridad que contenga las cuentas activadas. Una parte del proceso de inscripción consiste en trasladar las cuentas de administrador del grupo de ensayo al grupo de cuentas activadas.
  
Para el proceso de distribución es necesario nombrar a responsables de seguridad. Estos responsables de seguridad podrán:
  
-   Entregar las tarjetas inteligentes a la estación de inscripción.
  
-   Actuar como agentes de inscripción.
  
-   Llevar a cabo comprobaciones de identificación.
  
Las comprobaciones de identificación deben ser rigurosas. Los responsables de seguridad deben comprobar personalmente la identidad de los administradores a través de un documento identificativo adecuado, como un pasaporte o un permiso de conducir; la identidad deberá ser confirmada por el jefe de línea correspondiente.
  
Las organizaciones también deben realizar comprobaciones de antecedentes con respecto a sus administradores. Estas comprobaciones son especialmente importantes en los sectores financieros o para cualquier organización sujeta a requisitos normativos. Para obtener más información acerca de las comprobaciones de seguridad sobre los administradores, consulte la [Guía de implantación de supervisión de seguridad y detección de ataques](http://go.microsoft.com/fwlink/?linkid=41309), en la dirección http://go.microsoft.com/fwlink/?LinkId=41309.
  
#### Activación de tarjetas inteligentes
  
La activación de las tarjetas inteligentes debe realizarse en un lugar seguro, como la oficina que se utiliza para emitir pases de acceso a las instalaciones. El responsable de seguridad configura una estación de inscripción con dos lectores de tarjetas inteligentes e inicia sesión con su tarjeta inteligente.
  
Después de que el responsable de seguridad confirme la identidad del administrador, crea una solicitud de certificado para esa cuenta de usuario. Abre una nueva tarjeta inteligente e instala el certificado solicitado. A continuación, el responsable de seguridad mueve la cuenta de administrador desde el grupo de pendientes al de activadas. Por último, anota el número de serie de la tarjeta antes de entregar ésta al administrador.
  
El administrador utiliza después la herramienta de restablecimiento de NIP para restablecer el NIP predeterminado o utiliza la herramienta de desbloqueo de NIP junto con el servidor Web de activación para establecer un nuevo NIP. La tarjeta inteligente del administrador está ahora lista para ser utilizada.
  
#### Activación de tarjetas inteligentes
  
La implantación de tarjetas inteligentes no es una acción aislada en el tiempo, ya que se deben administrar los certificados de seguridad incrustados en las tarjetas y deberá hacer frente a situaciones como la pérdida, el descuido o la sustracción de tarjetas inteligentes de administradores. Será necesario establecer los procedimientos pertinentes y un presupuesto adecuado para la administración de las tarjetas inteligentes.
  
##### Administración de excepciones
  
La empresa necesita desarrollar un plan centrado en cómo administrar situaciones en las que las tarjetas inteligentes del administrador se olviden, pierdan o roben. El modo en que la empresa implementa el plan depende de cómo se aplican los requisitos de inicio de sesión de las tarjetas inteligentes en la empresa.
  
Si la empresa ha decidido aplicar un requisito de inicio de sistema de la tarjeta inteligente a través de cuentas de usuario en Active Directory, podrá conceder una excepción al usuario afectado en tal situación. El método de concesión de excepciones consistiría en eliminar de la cuenta el requisito de inicio de sesión de la tarjeta inteligente y, a continuación, restablecer la contraseña después de asegurarse de que la configuración **El usuario debe cambiar la contraseña al iniciar una sesión de nuevo** esté habilitada. Puede proporcionar la contraseña al propietario de la cuenta y, después de un periodo razonable, volver a habilitar el requisito. Para aplicar este método, desde el menú Usuarios y equipos de Active Directory haga doble clic en la ficha **Cuenta** y, a continuación, en el menú **Opciones de cuenta**, desactive la casilla **La tarjeta inteligente es necesaria para un inicio de sesión interactivo** y seleccione la casilla **El usuario debe cambiar la contraseña al iniciar una sesión de nuevo**. Haga clic en **Aceptar** y, a continuación, desde el menú contextual, haga clic con el botón secundario en el nombre de usuario y seleccione **Restablecer contraseña** para establecer la contraseña y aplicar estos requisitos al administrador.
  
Si la empresa usa Directivas de grupo para aplicar el requisito de inicio de sesión de la tarjeta inteligente, no hay ninguna forma de crear una excepción para un usuario en este punto. En este caso, tendrá que determinar una directiva adecuada para la empresa que los administradores puedan seguir en el caso de que olviden o pierdan las tarjetas inteligentes.
  
Podrá implementar diferentes respuestas si se pierden las tarjetas inteligentes. Por ejemplo, una directiva podría requerir que los administradores vuelvan a casa para recuperar las tarjetas inteligentes extraviadas.
  
Si la empresa va a subcontratar la infraestructura de tarjeta inteligente, podría implementar una directiva que requiera que el administrador mantenga unas cuantas tarjetas inteligentes genéricas vinculadas a cuentas de usuario en el sitio. Si un usuario pierde la tarjeta inteligente, el administrador podría emitir una de esas tarjetas genéricas al usuario de forma temporal con la condición de que el usuario sea responsable de las acciones que realice para acceder a recursos con la cuenta genérica. En tal directiva, se recomienda que el administrador que guarda la tarjeta inteligente restablezca el NIP de contraseña de la tarjeta antes de emitirla a cualquier usuario.
  
Si la empresa mantiene su propia infraestructura de tarjeta inteligente, podría emitir un nuevo certificado con un corto periodo de vida a una cuenta de usuario genérica. Con este método de administración de excepciones, el administrador será responsable del uso de la cuenta genérica para acceder a recursos.
  
Por último, si el administrador pierde una tarjeta inteligente, la empresa tendrá que establecer una directiva para emitir una nueva tarjeta al administrador y revocar el certificado antiguo del administrador.
  
##### Revocación de certificados
  
Quizá deba revocar un certificado en determinadas circunstancias; por ejemplo, si la clave privada está en peligro, si cambian las asignaciones del usuario de la tarjeta inteligente o si el usuario causa baja en la organización. Cuando se revoca un certificado, esta acción publica detalles acerca del certificado en la ubicación de la lista de revocaciones de certificados (CRL). Esta ubicación suele ser una dirección URL o una ruta (UNC) de red.
  
Un certificado emitido incluye una lista de puntos de distribución en los que el servidor de autenticación puede comprobar el estado del certificado con la CRL. Para obtener más información acerca de la revocación de certificados, consulte el tema [Revocar certificados y publicar listas de revocaciones de certificados](http://www.microsoft.com/resources/documentation/windowsserv/2003/standard/proddocs/en-us/sag_cs_srvadcrl.asp), en la dirección www.microsoft.com/resources/documentation/WindowsServ/2003/standard/proddocs/en-us/sag\_CS\_SrvAdCRL.asp.
  
##### Renovación de certificados
  
La fecha de caducidad del certificado digital de una tarjeta inteligente depende de la configuración de la plantilla de certificados a partir de la que se crea el certificado para la tarjeta inteligente. Los certificados destinados al uso de tarjetas inteligentes suelen tener una duración comprendida entre seis meses y dos años.
  
Cuando un certificado se acerca al final de su período de vigencia, es preciso renovarlo para que el propietario pueda seguir utilizando el certificado o bien reemplazarlo. Para proceder a la renovación, el solicitante ya debe poseer un certificado. La información del certificado actual se tiene en cuenta cuando se envía la solicitud de renovación. Podrá renovar el certificado con una clave nueva o bien utilizar la clave actual.
  
##### Inscripción automática de certificados
  
La inscripción automática de certificados es una característica de los servicios de Certificate Server en Windows Server 2003 Enterprise Edition, en virtud de la cual se firma automáticamente una solicitud de renovación mediante el certificado existente para obtener un nuevo certificado. Esta característica constituye una ayuda en la administración de grandes cantidades de certificados. Para obtener más información acerca de la inscripción automática de certificados, consulte el artículo sobre[inscripción automática de certificados en Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=69027), en la dirección http://go.microsoft.com/fwlink/?LinkId=69027.
  
#### Supervisión del uso de las tarjetas inteligentes
  
Los administradores utilizan cuentas habilitadas para el uso de tarjetas inteligentes cuando realizan operaciones que requieren privilegios elevados, como el reinicio de servidores, la administración de cuentas de usuarios y la configuración de permisos relacionados con archivos. Un administrador malintencionado o poco preparado tiene muchas probabilidades de dañar la infraestructura de la red. En consecuencia, es necesario supervisar los registros de seguridad para tener constancia de cuándo inician y cierran sesión los administradores con tarjetas inteligentes.
  
Las herramientas de administración empresarial que pueden supervisar y evaluar los registros de eventos, como Microsoft Operations Manager (MOM) 2005, resultan adecuadas para la supervisión del uso de las tarjetas inteligentes. Para obtener más información acerca de la supervisión de los registros de eventos de seguridad, consulte el artículo sobre [la guía de implantación de supervisión de seguridad y detección de ataques](http://go.microsoft.com/fwlink/?linkid=41309), en la dirección http://go.microsoft.com/fwlink/?LinkId=41309.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Problemas y requisitos
  
En esta sección se describen los problemas y requisitos específicos que tuvo que afrontar Woodgrove National Bank durante el diseño de una solución para proteger las cuentas de los administradores con tarjetas inteligentes.
  
#### Información de referencia
  
Woodgrove National Bank posee varios servidores de especial importancia que precisan un estricto control administrativo y acceso seguro. Actualmente, los administradores se autentican para el acceso a esos servidores críticos mediante una combinación de nombre de usuario y contraseña. Algunos usuarios no autorizados han intentado el acceso a los servidores críticos con credenciales robadas.
  
#### Aspectos de la empresa
  
Woodgrove National Bank ha identificado los tres siguientes problemas de continuidad y responsabilidad de los administradores:
  
-   **Responsabilidad**. El departamento de TI no puede comprobar los cambios importantes que puedan realizar en los servidores los administradores que utilizan la autenticación basada en el nombre de usuario y la contraseña, ya que es habitual que los administradores compartan las credenciales.
  
-   **Protección de credenciales**. Un usuario malintencionado o sin escrúpulos que robe las credenciales de un administrador puede perjudicar seriamente la reputación de una organización y originar costos económicos asociados a los tiempos de inactividad. La autenticación con tarjetas inteligentes reduciría considerablemente la posibilidad de robo de credenciales de administrador.
  
-   **Continuidad empresarial**. Como Woodgrove National Bank no puede permitir que los cambios de configuración de red afecten a los servicios de la empresa es esencial un planteamiento planeado al detalle en la fase de implantación de la solución de tarjetas inteligentes.
  
#### Aspectos técnicos
  
El departamento de TI de Woodgrove National Bank ha identificado los siguientes problemas técnicos que deben superarse para implantar una solución basada en tarjetas inteligentes:
  
-   **Compatibilidad con los lectores de tarjetas inteligentes**. El hardware de los servidores a los que los administradores necesiten tener acceso con tarjetas inteligentes debe ser compatible con un lector de tarjetas inteligentes.
  
-   **Implantar procedimientos recomendados para las operaciones**. La integridad de una implantación de tarjetas inteligentes depende de una administración y un mantenimiento efectivos a largo plazo. El equipo de TI de Woodgrove National Bank debe implantar los procedimientos recomendados para los operaciones que se destacan en Microsoft Operations Framework (MOF).
  
-   **Tareas programadas que se ejecutan con derechos de administrador en un servidor con restricción para tarjetas inteligentes**.** **Woodgrove National Bank ejecuta tareas programadas en las que se utilizan cuentas con privilegios de nivel de administrador. Woodgrove National Bank necesita revisar estas cuentas y, en la medida de lo posible, utilizar cuentas que no requieran privilegios administrativos. Asimismo, Woodgrove National Bank debe implantar un grupo de exclusiones permanentes que incluya las cuentas con las que se ejecuten tareas programadas, de modo que queden exentas del requisito de iniciar sesión con un tarjeta inteligente.
  
-   **Integración con UNIX**. Woodgrove National Bank opera en un entorno heterogéneo, por lo que la integración de las tarjetas inteligentes con los equipos en los que se ejecuta UNIX constituye un motivo de preocupación. Woodgrove National Bank planea investigar productos tales como TrustBroker, de CyberSafe Limited, que proporcionen autenticación con tarjetas inteligentes tanto para Windows como para UNIX.
  
#### Problemas de seguridad
  
El uso de tarjetas inteligentes como medida de protección de las cuentas de los administradores tiene por objeto mejorar los niveles de seguridad y responsabilidad. El departamento de TI de Woodgrove National Bank ha identificado los siguientes aspectos relacionados con la seguridad que el banco debe abordar para poder implantar la solución:
  
-   **Distribución y activación**.** **La** **distribución y activación de las tarjetas inteligentes son importantes para mantener la integridad de la solución. Como Woodgrove National Bank cuenta con sedes en todo el mundo, el departamento de TI de Woodgrove no puede distribuir las tarjetas inteligentes desde una sola ubicación. La comprobación de los destinatarios de las tarjetas inteligentes es esencial para mantener la integridad del proyecto. Woodgrove National Bank planea implantar equipos de seguridad que utilicen datos de identificación de Recursos humanos para asegurarse de que cada tarjeta inteligente que se emite corresponde a la persona adecuada.
  
-   **Privilegios mínimos para los derechos administrativos**. Woodgrove National Bank debe examinar su modelo actual de administración de red y reducir el número de cuentas de usuarios y servicios que se ejecutan con plenos privilegios administrativos. El banco debe asignar únicamente los privilegios que necesiten los administradores para realizar su trabajo. El análisis y la reducción del número de cuentas de administrador pueden facilitar la implantación, supervisión y administración continua de la solución basada en tarjetas inteligentes.
  
-   **Administración de cuentas de servicios**.** **El equipo de TI de Woodgrove revisó las cuentas de servicios de programas y se ha asegurado de reducir al mínimo el número de servicios que requieren un contexto de seguridad de administrador. Se ha indicado la actualización o el reemplazo de numerosos programas.
  
-   **Una tarjeta inteligente para cada bosque en una relación de plena confianza**. Woodgrove National Bank tiene dos bosques vinculados por una relación de confianza bidireccional. Aunque una tarjeta inteligente puede contener varios certificados, Windows Server 2003 utiliza únicamente el certificado que se encuentra en la ranura 0 de la tarjeta inteligente para el inicio de sesión interactivo. Para este diseño es necesario que los administradores de red que trabajan con más de un bosque no vinculado tengan varias tarjetas inteligentes. Sin embargo, un administrador con una tarjeta inteligente tiene acceso a recursos en todos los bosques con los que el bosque que autentica al administrador mantiene una relación de confianza completa, a menos que este acceso se vea anulado por una restricción de seguridad en el bosque que confía.
  
-   **Administración de NIP**. La seguridad e integridad de la solución basada en tarjetas inteligentes aumenta si los usuarios pueden cambiar de NIP con facilidad. El departamento de TI de Woodgrove National Bank adquirió por tanto al fabricante de tarjetas inteligentes seleccionado las herramientas de administración de NIP adecuadas.
  
#### Requisitos de la solución
  
Después de revisar la fase piloto inicial, el departamento de TI de Woodgrove elaboró requisitos específicos para la solución. La solución empleada por Woodgrove National Bank para contribuir a la protección de las cuentas de administradores que tienen tarjetas inteligentes debe:
  
-   Establecer la necesidad de una tarjeta inteligente válida para un inicio de sesión de inicio interactivo, secundario o de Escritorio remoto en los servidores protegidos.
  
-   Distribuir y activar tarjetas inteligentes de un modo seguro y con puntualidad.
  
-   Proporcionar una auditoría del acceso a los servidores seguros y recopilar los datos de seguridad resultantes en un repositorio central.
  
-   Habilitar la administración y la supervisión del uso de las tarjetas inteligentes.
  
-   Asegurar una rápida revocación de los certificados que se encuentren expuestos, como los de las tarjetas inteligentes que se hayan perdido o hayan sido sustraídas.
  
-   Proporcionar una estructura para la administración continua.
  
Woodgrove National Bank ha identificado distintos problemas empresariales, técnicos y de seguridad que surgieron durante el plan inicial. El departamento de TI de Woodgrove realizó un análisis para responder a estos problemas y llevó a cabo pruebas de soluciones provisionales y revisiones. Woodgrove National Bank ha creado planes detallados para la fase de implantación de la solución.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Diseño de la solución
  
Después de comprender los problemas empresariales, técnicos y de seguridad a los que debe responder la solución de seguridad basada en tarjetas inteligentes, puede diseñar una solución que se adapte a su entorno. En el proceso de diseño se identifican los elementos esenciales y se analiza la lógica de los requisitos de planeamiento de la solución.
  
Woodgrove National Bank ha llevado a cabo esta valoración. En esta sección se describen los problemas a partir del plan inicial que los diseñadores de sistemas de Woodgrove National Bank tuvieron en cuenta, las conclusiones a las que llegaron y las decisiones sobre diseño que adoptaron.
  
En esta sección se ponen de relieve las opciones de diseño elegidas por el departamento de TI de Woodgrove National Bank para contribuir a proteger las cuentas de los administradores mediante tarjetas inteligentes. Se detalla el concepto de la solución y sus requisitos previos; además, se describe la arquitectura planeada por la entidad Woodgrove National Bank.
  
#### Concepto de la solución
  
En la solución propuesta, para todas las actividades de administración de servidores se precisa la autenticación de la identidad del administrador por medio de la presentación de un certificado almacenado en una tarjeta inteligente y el NIP correspondiente. En la solución se utiliza una combinación de opciones de Directiva de grupo, certificados de usuario X.509 versión 3 (v3), tarjetas inteligentes y lectores de tarjetas inteligentes. Para la solución se precisa la instalación de un certificado X.509 v3 en la tarjeta inteligente.
  
Para iniciar sesión en un servidor, el administrador inserta la tarjeta inteligente en un lector instalado en el equipo. La inserción de la tarjeta provoca que el sistema operativo pida el NIP. El administrador escribe el NIP de la tarjeta inteligente. Si el NIP es correcto, el administrador podrá obtener acceso al servidor en calidad de administrador.
  
#### Requisitos previos de la solución
  
Cuando se pretende abordar un proyecto de esta naturaleza, es necesario cumplir algunos requisitos previos. Entre estos requisitos previos se encuentra la selección del equipo del proyecto, las consultas con los usuarios, la implantación de pruebas o fases piloto y la necesidad de actualizar el hardware y el software para responder a las exigencias de la solución.
  
##### Consultas a los equipos administrativos
  
Una consideración muy importante cuando se plantea el cambio de un servicio es la consulta a los usuarios y grupos a los que afecta. Por su parte, los usuarios deben saber a qué atenerse con respecto a las posibilidades y limitaciones del servicio. Las consultas mutuas y la administración de las expectativas de los usuarios suelen ser decisivas para la aceptación de la solución por parte de los usuarios. Deberán establecerse objetivos cuantificables para poder juzgar el éxito del proyecto. Entre estos objetivos cabría incluir la reducción de los incidentes relacionados con la seguridad debidos al robo de credenciales.
  
Woodgrove National Bank opera en varios países y regiones y utiliza centros regionales de soporte. El equipo de diseño inicial sondeó a los equipos administrativos de todas las sedes con el fin de identificar servidores aptos para la solución basada en tarjetas inteligentes. El equipo también identificó qué servidores no se podrían actualizar para cumplir con los requisitos previos de la solución dentro de una escala temporal aceptable.
  
##### Selección del equipo del proyecto
  
Asegúrese de contar con el personal y los recursos adecuados para implantar un proyecto de estas características. Es probable que el equipo del proyecto recabe opiniones de los siguientes representantes:
  
-   Director del programa
  
-   Diseñador de sistemas de información
  
-   Analista o integrador de sistemas
  
-   Ingenieros de sistemas
  
-   Responsable de lanzamiento de productos
  
-   Responsable de pruebas de productos
  
-   Responsable de soporte o asistencia técnica
  
-   Especialista de soporte a los usuarios
  
-   Responsables de seguridad
  
Para obtener más información acerca de los oficios representativos y las asociaciones de funciones en MOF, consulte el documento (en inglés) [The Microsoft Solutions Framework Supplemental Whitepapers – IT Occupation Taxonomy](http://www.microsoft.com/downloads/details.aspx?familyid=839058c3-d998-4700-b958-3bedfee2c053), en la dirección www.microsoft.com/downloads/details.aspx?FamilyID=839058c3-d998-4700-b958-3bedfee2c053
  
Si no dispone de los recursos internos necesarios, deberá contratar más personal. Como este proyecto no suele precisar la intervención simultánea del personal participante en todas las etapas, será preciso determinar la disponibilidad individual a lo largo del proyecto.
  
#### Arquitectura de la solución
  
La implantación de una solución basada en tarjetas inteligentes para contribuir a proteger las cuentas de los administradores requiere lo siguiente:
  
-   Active Directory
  
-   Directiva de grupo
  
-   Windows Server 2003 Enterprise Edition, infraestructura de claves públicas (PKI).
  
-   Que los servidores en los que se ejecuta Windows Server 2003 dispongan de lectores de tarjetas inteligentes.
  
-   Estaciones de inscripción
  
-   Personalización de las tarjetas inteligentes.
  
-   Herramientas de administración de NIP.
  
Antes de implantar la solución, Woodgrove National Bank llevó a cabo los siguientes procedimientos:
  
-   Se actualizaron los servicios de Certificate Server a Windows Server 2003 Enterprise Edition o posterior.
  
-   Se actualizaron todos los servidores administrados a Windows Server 2003 para posibilitar el inicio de sesión interactivo que utilizan los servicios de Terminal Server. Este requisito depende de la compatibilidad de la aplicación.
  
-   Se personalizaron las plantillas de certificados para tarjetas inteligentes y se establecieron los permisos correspondientes.
  
-   Se crearon y probaron objetos de directiva de grupo (GPO) para el uso obligado de tarjetas inteligentes, así como para las exclusiones temporales y permanentes.
  
El departamento de TI de Woodgrove National Bank también implantó soluciones para responder a los siguientes retos:
  
-   Distribución de las tarjetas inteligentes.
  
-   Activación de las tarjetas inteligentes.
  
-   Administración y soporte de las tarjetas inteligentes.
  
-   Administración de excepciones.
  
##### Distribución de las tarjetas inteligentes
  
Antes de proceder a la distribución de las tarjetas inteligentes, el departamento de TI de Woodgrove National Bank asignó las cuentas de sus administradores a un grupo de seguridad de ensayo en Active Directory. Se precisó un equipo de responsables de seguridad para comprobar las identidades de los administradores y para distribuir las tarjetas inteligentes. Al hacerse entrega de la tarjeta al administrador, el departamento de TI traslada la cuenta de esa persona del grupo de ensayo al grupo de usuarios de tarjetas inteligentes. A partir de ahí, el administrador tiene acceso al servidor Web de activación para activar su tarjeta inteligente y cambiar el NIP.
  
##### Activación de las tarjetas inteligentes
  
Como los administradores reciben sus tarjetas inteligentes en estado pendiente, es preciso activar las tarjetas para poder utilizarlas. El administrador activa su tarjeta inteligente cuando la inserta en un lector, especifica un desafío y después cambia el NIP.
  
##### Administración y soporte de tarjetas inteligentes
  
Aunque los administradores de Woodgrove National Bank son un grupo bien preparado técnicamente, el equipo de implantación del sistema de tarjetas inteligentes tenía que trabajar estrechamente con el departamento de asistencia. El personal de asistencia precisaba la formación adecuada para responder a las consultas que pudieran surgir.
  
###### Administración de excepciones
  
Woodgrove National Bank instituyó una directiva corporativa en previsión de los casos de pérdida, robo o descuido de tarjetas. En los casos de pérdida o robo de tarjetas, el departamento de TI revoca todos los certificados asignados y emite nuevas tarjetas en un plazo no superior a 24 horas. Cuando un administrador olvida llevar al trabajo su tarjeta inteligente, el departamento de TI emite tarjetas inteligentes temporales. Aunque se podría revocar un certificado, eso no significa que la tarjeta inteligente quede desactivada durante ese mismo período. Woodgrove debe revisar las directivas de CRL para que coincidan con las de seguridad.
  
###### Revocación de certificados
  
Los certificados de inicio de sesión con tarjetas inteligentes para los administradores de Woodgrove National Bank utilizan direcciones URL de intranet para localizar la CRL y consultar los certificados revocados. El departamento de TI implantó la función de equilibrio de carga de red (NLB) de Windows para garantizar una alta disponibilidad del sitio Web en el que se aloja la CRL.
  
###### Renovación de certificados
  
El departamento de TI de Woodgrove National Bank elaboró un proceso de renovación de certificados que requiere que el jefe del administrador apruebe la solicitud de renovación de cada tarjeta inteligente. Después de que el responsable apruebe una solicitud, se utiliza el certificado actual para firmar la solicitud de certificado y se procede a la renovación del certificado de la tarjeta inteligente.
  
##### Supervisión de la solución
  
Woodgrove National Bank utiliza Microsoft Operations Manager (MOM) 2005 para recopilar y analizar registros de eventos de seguridad, además de supervisar la disponibilidad y el rendimiento de la solución. La solución basada en tarjetas inteligentes se integra con MOM, supervisa los registros de eventos de seguridad, proporciona alertas y presenta informes de uso. Woodgrove National Bank planea revisar trimestralmente el servicio y elaborar informes a partir de los datos de MOM.
  
#### Cómo funciona la solución
  
En esta sección se describen en detalle los procesos que se suceden durante la autenticación en un inicio de sesión con tarjeta inteligente.
  
1.  Un administrador inserta una tarjeta inteligente en el lector conectado a un equipo con el archivo DLL de Autenticación e identificación gráfica de Microsoft (MSGINA). El equipo pide al usuario que escriba el NIP.
  
2.  MSGINA transfiere el NIP a la autoridad de seguridad local (LSA) y el equipo utiliza el NIP para obtener acceso a la tarjeta inteligente.
  
3.  El paquete Kerberos del cliente lee el certificado X.509 v3 y la clave privada de la tarjeta inteligente del administrador.
  
4.  El paquete Kerberos envía una solicitud de autenticación al servicio del Centro de distribución de claves (KDC) que se ejecuta en un controlador de dominio, para solicitar la autenticación y un tíquet de obtención de tíquet (TGT, Ticket Granting Ticket). La solicitud del servicio de autenticación consta de un certificado de atributos de privilegios (PAC), en el que se enumeran el identificador de seguridad del usuario (SID), los SID de todos los grupos a los que pertenezca el usuario y una solicitud para el servicio de obtención de vales (TGS, Ticket Granting Service), junto con los datos de preautenticación.
  
5.  El KDC comprueba la ruta de certificación del certificado del usuario para asegurarse de que el certificado procede de un origen de confianza. El KDC utiliza CAPI (CrytoAPI) para crear una ruta de certificación desde el certificado del administrador hasta un certificado de la entidad emisora de certificados raíz que se encuentra en el almacén raíz del controlador de dominio. El KDC utiliza después CryptoAPI para comprobar la firma digital en el autenticador incluido como datos firmados en los campos de datos de preautenticación. El controlador de dominio comprueba la firma y utiliza la clave pública del certificado del administrador para demostrar que la solicitud procedía del propietario de la clave pública. El KDC también comprueba que el emisor es de confianza y aparece en el almacén de certificados NTAUTH.
  
6.  El servicio KDC recupera la información de las cuentas de los usuarios desde Active Directory a partir del nombre principal de usuario (UPN) especificado en el campo **Nombre alternativo del sujeto** del certificado del administrador. El KDC construye un TGT a partir de la información de la cuenta del usuario que recupera de Active Directory. El TGT incluye el identificador de seguridad del usuario (SID), los SID de todos los grupos del dominio a los que pertenece el administrador y (en un entorno con varios dominios), los SID de todos los grupos universales de los que es miembro el usuario. Los campos de datos de autorización del TGT incluyen la lista de SID.
  
    **Nota:** Un SID es un identificador de seguridad que se genera para cada usuario o grupo en el momento en el que se crea una cuenta de usuario o un grupo dentro de la base de datos local de cuentas de seguridad en equipos con Windows NT o superiores, o bien dentro de Active Directory. El SID nunca se modifica, aunque se cambie el nombre de la cuenta del usuario o del grupo
  
7.  El controlador de dominio devuelve el TGT al cliente. El cliente o la tarjeta descifran el TGT y utilizan su clave privada para obtener la clave secreta del KDC. Esta operación depende del tipo de tarjeta o certificado que se utilice.
  
8.  El cliente valida la respuesta del KDC. En primer lugar comprueba la firma del KDC mediante la construcción de una ruta de certificación desde el certificado del KDC hasta una entidad emisora de certificados raíz de confianza y después utiliza la clave pública del KDC para comprobar la firma de respuesta.
  
El proceso se muestra en la siguiente ilustración.
  
[![](images/Cc170941.pgfg0301(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc170941.pgfg0301_big(es-es,technet.10).gif)
  
**Ilustración 3.1 Proceso de autenticación en el inicio de sesión con tarjeta inteligente**
  
El departamento de TI de Woodgrove National Bank vinculó un GPO a las unidades organizativas en las que se encuentran los servidores para los que se precisa autenticación con tarjetas inteligentes. Este GPO aplica los cambios a las siguientes opciones de configuración del equipo:
  
-   Para el inicio de sesión interactivo se requiere una tarjeta inteligente.
  
-   La extracción de la tarjeta inteligente provoca el cierre de la sesión.
  
Estas opciones de configuración contribuyen a evitar que los administradores compartan las tarjetas inteligentes o que dejen un servidor desatendido con una sesión iniciada.
  
#### Ampliación de la solución
  
Woodgrove National Bank prevé la integración de la solución basada en tarjetas inteligentes en el proceso de administración de cambios en las aplicaciones y el servidor. El objetivo consiste en autenticar todas las etapas del proceso de administración de cambios e integrar ese proceso en el flujo de trabajo. Por ejemplo, para aplicar cambios al servidor Web de Woodgrove se precisaría la comprobación de dos o más administradores Web.
  
#### Resumen
  
El uso de tarjetas inteligentes para autenticar cuentas de administradores permite reducir el acceso fraudulento a equipos de especial importancia y aumenta la integridad y la responsabilidad de la administración de los servidores. La implantación de tarjetas inteligentes para los administradores reportará a la organización ventajas como la reducción de los incidentes relacionados con la seguridad y una mayor calidad de los procedimientos administrativos.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 4: Uso de tarjetas inteligentes para la protección de las cuentas de acceso remoto
  
La mayoría de las organizaciones deben proporcionar acceso remoto a sus recursos de red a través de conexiones de acceso telefónico o de red privada virtual (VPN). Esta tendencia se acentúa con la evolución actual de las prácticas empresariales, que se orienta a un mayor soporte a los usuarios remotos y a los representantes comerciales que se desplazan. Aunque el acceso remoto ofrece numerosas ventajas, por el hecho de ser externo expone la red de la organización a posibles amenazas para la seguridad. La autenticación de dos factores es un requisito cada vez más extendido en el caso de las redes que permiten el acceso remoto.
  
[](#eeal)[Protección del acceso remoto con tarjetas inteligentes](#eeal)  
[](#edam)[Problemas y requisitos](#edam)  
[](#ecan)[Diseño de la solución](#ecan)  
[](#ebaj)[Resumen](#ebaj)
  
### Protección del acceso remoto con tarjetas inteligentes
  
El acceso remoto debe posibilitar el acceso de todos los empleados autorizados a los recursos de la intranet de una organización. Para facilitar el acceso remoto a través de VPN, es necesario abrir puertos en los servidores de seguridad externos. Esa ampliación de las posibilidades de acceso abre una vía que los atacantes podrían aprovechar para introducirse en la red.
  
En el Capítulo 1, "Introducción", se destaca que la autenticación de cuentas basada en nombres de usuario y contraseñas concentra toda la seguridad del control de los accesos en la contraseña. Las contraseñas son vulnerables, y las credenciales de una cuenta expuesta que tenga acceso remoto a la red corporativa pueden constituir un objetivo preferente para los delincuentes.
  
Aunque existe la posibilidad de configurar una directiva de bloqueo de contraseñas de dominio para las cuentas de usuario, este tipo de directiva puede propiciar ataques de denegación de servicio a través de un bloqueo constante de la cuenta del usuario remoto. Aunque este tipo de ataques no pone en peligro la información de la red, supone una evidente molestia para el usuario cuya cuenta queda bloqueada.
  
La autenticación de usuarios sólida, en la que se utilizan certificados digitales incrustados en una tarjeta inteligente, proporciona un método eficaz y flexible para proteger las conexiones de acceso remoto.
  
#### Requisitos de los clientes
  
El uso de tarjetas inteligentes para controlar el acceso remoto depende de los componentes que se ejecutan en el cliente remoto. Debe conocer bien esos componentes y, en particular, Connection Manager y el Kit de administración de Connection Manager (CMAK). Connection Manager centraliza y automatiza el establecimiento y la administración de conexiones de red. Connection Manager es compatible con los siguientes elementos clave de la configuración de acceso con tarjetas inteligentes:
  
-   Protocolo de autenticación extensible - Seguridad de la capa de transporte (EAP-TLS) para conexiones VPN y de acceso remoto.
  
-   Comprobaciones de seguridad en el nivel de las aplicaciones para administrar automáticamente las configuraciones de equipos cliente.
  
-   Comprobaciones y validaciones de la seguridad de los equipos que intervienen en el proceso de inicio de sesión.
  
Para obtener más información acerca de Connection Manager y CMAK, consulte el artículo relativo al kit de administración de Connection Manager, en la dirección [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/ServerHelp/be5c1c37-109e-49bc-943e-6595832d5761.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/be5c1c37-109e-49bc-943e-6595832d5761.mspx).
  
##### Connection Manager para el cliente
  
Para implantar una solución de acceso remoto administrable, debe crearse una configuración de Connection Manager para varios clientes y realizar la implantación correspondiente. Para implantar Connection Manager en varios clientes se crean perfiles de Connection Manager.
  
Los perfiles de Connection Manager son paquetes de marcador de cliente de Connection Manager personalizados que se crean con CMAK y se implantan en equipos cliente en un archivo ejecutable autoextraíble. Es posible utilizar cualquier mecanismo de distribución de software para asignar los perfiles, ya sea Directiva de grupo, Microsoft® Systems Management Server 2003, CD, o llaves USB.
  
Cuando se inicia el archivo ejecutable, éste instala el perfil en el equipo local, junto con los números de teléfono o las direcciones de host para la conexión a los servidores de acceso remoto. Cuando un usuario inicia una conexión a través de su perfil de Connection Manager, Connection Manager comprueba automáticamente si hay una tarjeta inteligente y pide al usuario que especifique el NIP. Si el usuario suministra el NIP correcto, Connection Manager establece las conexiones de acceso telefónico y VPN apropiadas y autentica las credenciales del usuario.
  
Connection Manager también simplifica el proceso de conexión para el usuario. Limita el número de opciones de configuración que puede cambiar el usuario y contribuye a garantizar que éste pueda conectarse siempre sin problemas. Una organización puede personalizar Connection Manager para definir lo siguiente:
  
-   **Números de teléfono disponibles**. Una lista de números de teléfono disponibles para el usuario en función de su ubicación física.
  
-   **Contenido personalizado**. El marcador puede incluir contenido personalizado, como gráficos, iconos, mensajes e información de ayuda.
  
-   **Conexiones antes del túnel**. Conexión de acceso telefónico a Internet que se produce automáticamente antes del intento de conexión VPN.
  
-   **Acciones previas y posteriores a la conexión**. Por ejemplo, la posibilidad de restablecer el perfil del marcador o la configuración del servidor de seguridad (Firewall) de Windows para que omita las excepciones a las reglas de filtrado de paquetes.
  
##### Requisitos del sistema operativo
  
La solución basada en tarjetas inteligentes para el acceso remoto sólo funciona con Microsoft Windows® XP Professional. Microsoft recomienda Windows XP Professional con SP2 o posterior. Los equipos cliente deben tener instaladas todas las actualizaciones de seguridad.
  
#### Requisitos de los servidores
  
Los requisitos de un servidor para el acceso con tarjetas inteligentes son relativamente sencillos. En los servidores de acceso remoto debe ejecutarse Windows 2000 Server o posterior y debe asegurarse la compatibilidad con EAP-TLS.
  
**Nota:** A diferencia de las tarjetas inteligentes para los administradores, las destinadas al acceso remoto no precisan Microsoft Windows Server™ 2003, aunque es recomendable actualizar la infraestructura de claves públicas a la de Windows Server 2003 con Service Pack 1 (SP1) o posterior.
  
##### Consideraciones sobre el acceso telefónico y VPN
  
La solución en la que se utilizan tarjetas inteligentes para proteger el acceso remoto admite el acceso telefónico a través de conexiones RDSI (Red digital de servicios integrados) o PSTN (Red telefónica pública conmutada), pero el inicio de sesión puede resultar más lento.
  
Las conexiones remotas a través de VPN imponen una carga adicional al procesador del servidor de acceso remoto. La protección mediante tarjetas inteligentes no contribuye sensiblemente a esa carga, pero puede ralentizar los inicios de sesión. Los servidores de acceso remoto VPN que atienden muchas conexiones entrantes requieren procesadores rápidos, preferentemente en configuraciones de multiprocesador. Las organizaciones que utilizan redes VPN protegidas con IPsec pueden implantar tarjetas de red que descarguen el proceso de cifrado IPsec en un procesador independiente.
  
##### Compatibilidad con el protocolo de autenticación extensible
  
EAP-TLS es un mecanismo de autenticación mutua desarrollado para métodos de autenticación combinados con dispositivos de seguridad, como tarjetas inteligentes y testigos de hardware. EAP-TLS es compatible con el Protocolo punto a punto (PPP) y con las conexiones VPN, y posibilita el intercambio de claves secretas compartidas para el Cifrado punto a punto de Microsoft (MPPE).
  
Las principales ventajas de EAP-TLS son su resistencia a los ataques basados en la "fuerza bruta" de procesamiento y el hecho de que admite autenticación mutua. La autenticación mutua implica que el cliente debe demostrar su identidad al servidor y viceversa. Si el cliente o el servidor no envían un certificado para validar la identidad, se interrumpe la conexión.
  
Windows Server 2003 es compatible con EAP-TLS para las conexiones de acceso telefónico y VPN, lo que permite el uso de tarjetas inteligentes para usuarios remotos. Para obtener más información acerca de EAP-TLS, consulte el tema Protocolo de autenticación extensible, en la dirección <http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/auth_eap.mspx>
  
Para obtener más información acerca de los requisitos de los certificados con EAP, consulte el tema Requisitos de certificado cuando se usa EAP-TLS o PEAP con EAP-TLS, en la dirección <http://support.microsoft.com/default.aspx?scid=kb;en-us;814394>
  
#### Identificación de requisitos para los servidores de autenticación
  
Para iniciar sesión, los usuarios remotos deben presentar sus credenciales a un servicio de autenticación. Windows proporciona dos servicios de autenticación para usuarios remotos:
  
-   Servidores IAS (Servicios de autenticación de Internet)
  
-   Servicio de directorio Active Directory®
  
Si su organización decide utilizar el proveedor de autenticación RADIUS (Servicio de usuario de acceso telefónico de autenticación remota), deberá incluir servidores IAS en la configuración. IAS es la implantación de RADIUS que realiza Microsoft y funciona como servicio en Windows 2000 Server o posterior.
  
Las organizaciones pueden obtener ventajas con la implantación de IAS para la autenticación RADIUS con tarjetas inteligentes, entre las que se incluyen las siguientes:
  
-   Autorización y autenticación centralizada de usuarios
  
-   Mecanismos de administración y contabilidad independientes
  
-   Amplia gama de opciones de autorización y autenticación
  
El servidor IAS administra el proceso de autenticación. IAS entrega la solicitud de autenticación del usuario y la información del certificado de inicio de sesión a Active Directory, que compara el certificado de inicio de sesión con la información almacenada sobre el certificado correspondiente a ese usuario remoto. Si la información del certificado coincide, Active Directory autentica al usuario.
  
Para obtener más información acerca de una solución de diseño en la que se utilice IAS, consulte el apartado "Diseño de la solución", más adelante en este capítulo.
  
#### Distribución e inscripción de tarjetas inteligentes para el acceso remoto
  
La distribución e inscripción de tarjetas inteligentes para el acceso remoto sigue un proceso similar al que se utiliza en la solución para cuentas de administrador, descrita en el Capítulo 3, "Uso de tarjetas inteligentes para la protección de las cuentas de los administradores". Las principales diferencias estriban en que el número de usuarios es mayor y que el proceso podría llevarse a cabo en varios países o regiones.
  
La comprobación de la identidad del usuario remoto sigue siendo una parte importante del proceso. Pero como no obstante los usuarios remotos no tienen los mismos derechos que los administradores, la presentación de documentos de identidad con fotografía como un pasaporte o permiso de conducir debe bastar para la identificación. Un responsable de la empresa debe presentar los justificantes para que el administrador otorgue acceso al usuario remoto.
  
Las estaciones de inscripción deben encontrarse en ubicaciones adecuadas, como el departamento de personal o de seguridad, adonde podrán dirigirse los usuarios para retirar las tarjetas inteligentes que les sean asignadas. Si un usuario no puede desplazarse hasta una estación de inscripción, existe la posibilidad de utilizar herramientas para desbloquear la tarjeta inteligente, inscribir al usuario y activar la tarjeta de forma remota.
  
Para el procedimiento de inscripción es necesario que un agente de inscripción genere la solicitud de certificado en nombre del usuario y que instale el certificado resultante en la tarjeta inteligente. El agente de inscripción envía al usuario la tarjeta inteligente a través de un método seguro de entrega. Después, el usuario se pone en contacto con el departamento de asistencia, establece su identidad y desbloquea la tarjeta inteligente, como se describe en la sección relativa al servidor Web de activación en el Capítulo 2, "Tecnologías de tarjeta inteligente".
  
#### Otras consideraciones
  
La introducción de un acceso remoto seguro en una organización contribuye a menudo a que aumente el número de usuarios que desean utilizar el servicio. Las organizaciones deben analizar su infraestructura de red y, cuando sea necesario, procurar recursos adicionales. Entre los elementos y aspectos que deben tenerse en cuenta podemos citar los siguientes:
  
-   Listas de revocaciones de certificados
  
-   Alto grado de disponibilidad y ancho de banda
  
-   Distribución de actualizaciones de software
  
##### Listas de revocaciones de certificados
  
La implantación de certificados para usuarios remotos implica cambios en la manera en que los clientes pueden localizar una lista de revocaciones de certificados (CRL) para comprobar la vigencia de un certificado. El localizador de recursos universal (URL) predeterminado de las CRL para Windows Server 2003 apunta a una ubicación de intranet; por ejemplo URL=http://Certification\_Root\_Server\_DNS\_Name/CertEnroll/  
Certification\_Authority\_Name.crl.
  
Para los usuarios remotos, esta dirección URL debe apuntar a una ubicación a la que se pueda tener acceso desde Internet. Este requisito afecta a todos los certificados emitidos e incluye tanto las direcciones URL de extranet como la intranet para la CRL. Para obtener más información acerca de la personalización de CRL, consulte el tema Especificar puntos de distribución de la lista de revocaciones de certificados en certificados emitidos, en la dirección [http://www.microsoft.com/resources/documentation/WindowsServ/2003/standard/proddocs/en-us/sag\_CSprocs\_CDP.asp](http://www.microsoft.com/resources/documentation/windowsserv/2003/standard/proddocs/en-us/sag_csprocs_cdp.asp).
  
**Nota:** Los equipos remotos pueden sufrir problemas de tiempo de espera si descargan la CRL a través de una conexión lenta.
  
##### Distribución de actualizaciones de software
  
La implantación de un mecanismo para la distribución de actualizaciones de software constituye un paso importante en el suministro de tarjetas inteligentes para el acceso de los usuarios. Las actualizaciones de software incluyen perfiles actualizados de Connection Manager y nuevas versiones de las herramientas relacionadas con las tarjetas inteligentes.
  
Puede distribuir actualizaciones de software mediante:
  
-   Servidores Web con las actualizaciones a los que se pueda obtener acceso externamente.
  
-   CD o llaves USB.
  
-   Soluciones de administración de software tales como Systems Management Server (SMS) 2003.
  
-   Mensajes de correo electrónico que contengan actualizaciones firmadas con código.
  
Si implanta la función de cuarentena de VPN, puede distribuir actualizaciones de perfiles de Connection Manager con el mismo método que utilice para suministrar actualizaciones y software antivirus. Para obtener más información acerca de la cuarentena de VPN, consulte el artículo sobre la guía de planeamiento para la implementación de servicios de cuarentena con una red privada virtual de Microsoft, en la dirección [http://go.microsoft.com/fwlink/?LinkId=41307](http://go.microsoft.com/fwlink/?linkid=41307).
  
La disponibilidad de Connection Manager y de actualizaciones de tarjetas inteligentes a través de servidores Web a los que se pueda tener acceso externo permite a los usuarios descargar las actualizaciones antes de la conexión a la red de una organización. El inconveniente de esta solución es que quizá no sea posible utilizar la tarjeta inteligente para la autenticación en el servidor Web externo. En este caso, los usuarios tienen que depender de las combinaciones de nombre de usuario y contraseña para iniciar sesión y descargar actualizaciones. Aunque esto parece contradecir el propósito de la autenticación de dos factores (ya que este servidor Web sólo proporciona recursos de actualización), quizá el riesgo le parezca aceptable.
  
El uso de CD para distribuir actualizaciones constituye un método útil para implantaciones a gran escala en una fase inicial debido a que el costo unitario de los CD disminuye cuando se producen en grandes cantidades. Las llaves USB resultan más adecuadas para la distribución individualizada de actualizaciones.
  
Para utilizar sistemas de administración de software como Systems Management Server 2003 con objeto de distribuir actualizaciones de software es necesario que los equipos se conecten a la red. Este mecanismo puede resultar adecuado para usuarios móviles y remotos que se conectan a la LAN de forma habitual y que utilizan equipos que pertenecen al dominio de la organización. Sin embargo, los mecanismos de actualización de software como Systems Management Server no son apropiados para usuarios remotos que utilizan sus propios equipos domésticos.
  
En determinadas situaciones se pueden enviar actualizaciones por correo electrónico. Para implantar este método de distribución de software debe facilitar actualizaciones firmadas con código e instruir a los usuarios para que comprueben la veracidad del certificado de firma con código.
  
En esta sección se ha descrito los componentes que pueden proporcionar autenticación con tarjetas inteligentes para cuentas de acceso remoto. En la siguiente sección, Problemas y requisitos, se examinan las dificultades que debe afrontar la entidad Woodgrove National Bank durante la implantación de un sistema basado en tarjetas inteligentes.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Problemas y requisitos
  
Durante la fase de planeamiento y diseño de la solución de acceso remoto con tarjetas inteligentes, el departamento de TI de Woodgrove se encontró con diversos problemas de tipo empresarial, técnico y de seguridad. En el siguiente apartado se identifican todos esos problemas.
  
#### Información general de situación de Woodgrove National Bank
  
Woodgrove National Bank proporciona acceso remoto a su red corporativa al personal de ventas, ejecutivo y de soporte técnico de TI. Para la solución actual de acceso remoto se emplea acceso telefónico a través de circuitos privados a servidores de acceso remoto dedicados que están equipados con modems o adaptadores RDSI. Estas conexiones son lentas y caras en comparación con las de banda ancha, sobre todo para los usuarios remotos que viajan por más de un país.
  
La mayor disponibilidad de acceso de banda ancha a Internet permite a las organizaciones utilizar redes privadas virtuales para el acceso remoto. Con este sistema se reducen costos al eliminar el acceso telefónico y el usuario disfruta de prestaciones superiores. No obstante, también aumenta la vulnerabilidad del banco ante posibles ataques malintencionados.
  
##### Cumplimiento de requisitos legales
  
Como toda institución financiera, Woodgrove National Bank debe cumplir con estrictos requisitos legales en los distintos países y regiones en los que opera. El banco debe mantener la confianza de los clientes mediante la protección de los activos corporativos y de los clientes. Woodgrove National Bank implantó una iniciativa de protección de los equipos y estableció directivas de seguridad estrictas para todos los equipos con acceso a la red de la compañía, ya sea a través de la red de área local (LAN) o de forma remota.
  
##### Comprobación de los usuarios
  
La solución actual de acceso remoto de Woodgrove National Bank no es capaz de responder adecuadamente ante posibles ataques de suplantación (en los que el atacante intenta adivinar combinaciones de nombre de usuario y contraseña). Los ataques de suplantación provocan el bloqueo de las cuentas de acceso remoto, con lo que se impide al usuario legítimo la posibilidad de conectarse a la red. Esta vulnerabilidad aumenta el riesgo para la red corporativa y ha obligado a Woodgrove National Bank a limitar las opciones de conexión que ofrece a sus empleados.
  
#### Aspectos de la empresa
  
Muchos ejecutivos utilizan el acceso remoto. Aunque la seguridad es esencial durante la implantación de una solución basada en tarjeta inteligentes, el mantenimiento de la productividad de los trabajadores remotos también es importante. En la solución implantada se debe alcanzar un equilibrio entre estas necesidades.
  
##### Mantener la productividad
  
A menudo, los empleados pierden la confianza en las soluciones de seguridad que afectan a la productividad. Para los usuarios constituye un motivo de frustración no poder tener acceso a los recursos de la red durante la implantación de una solución y justo después. El equipo de TI de Woodgrove debe proporcionar otros métodos de acceso para intentar superar esos inconvenientes. Las herramientas de la siguiente lista proporcionan otros métodos de acceso a redes:
  
-   **Outlook Web Access**. Proporciona al usuario un acceso seguro al correo electrónico a través de un explorador Web.
  
-   **Servicios de Terminal Server y Escritorio remoto**. Los empleados pueden utilizar los servicios de Terminal Server y Escritorio remoto para obtener acceso a aplicaciones de línea de negocio y a archivos de escritorio.
  
##### Soporte al personal de asistencia
  
La aceptación por parte de los usuarios y la integridad de una solución de acceso remoto dependen a menudo del nivel de soporte disponible. Para los ejecutivos resulta frustrante perder tiempo en colas para obtener soporte. Las organizaciones deben prever recursos de formación tanto para el usuario final como para el personal de soporte.
  
#### Aspectos técnicos
  
Woodgrove National Bank ha identificado diversos aspectos técnicos clave que reclaman atención antes de la implantación de un sistema de tarjetas inteligentes para el acceso remoto. Entre estos aspectos podemos citar la distribución de tarjetas inteligentes y lectores, la integración de la solución en la red actual de manera que la repercusión sea mínima, y la integración en la infraestructura de administración de TI actual.
  
-   **Lectores de tarjetas inteligentes compatibles**. Lo usuarios remotos podrían trabajar desde sus casas con distintos equipos y sistemas operativos. El departamento de TI de Woodgrove decidió que la única configuración admitida sería Windows XP Professional con SP2 o posterior. Los usuarios remotos que utilizaban Windows 2000 Professional no tenían garantías de que los lectores de tarjetas inteligentes funcionaran con sus equipos.
  
-   **Latencia de la red**. El tiempo que tardan los paquetes en ir y volver entre el cliente y el servidor de acceso remoto pueden provocar errores en las conexiones VPN protegidas. Esto resulta especialmente problemático en las conexiones de banda ancha por satélite. Woodgrove National Bank decidió no admitir conexiones remotas con tiempos de latencia superiores a 300 milisegundos.
  
-   **Distribución de tarjetas inteligentes**. Como Woodgrove National Bank opera en distintos países y regiones, la distribución de tarjetas inteligentes plantea problemas tanto técnicos como de seguridad. Los agentes de inscripción deben tener la posibilidad de ponerse en contacto con el servidor Web de activación independientemente del país o región en que se encuentren. Como alternativa, los usuarios tendrían que desbloquear tarjetas inteligentes a través de un sistema de desafío y respuesta. El sistema de desafío/respuesta puede requerir programación con el kit de desarrollo de software (SDK) del fabricante.
  
#### Problemas de seguridad
  
Los siguientes aspectos afectan a la estrategia de seguridad de la implantación en la entidad Woodgrove National Bank de un sistema de acceso seguro con tarjetas inteligentes:
  
-   **Identificación de usuarios de acceso remoto**. El departamento de TI de Woodgrove National Bank debe validar la identidad de los usuarios de acceso remoto durante el proceso de distribución y activación de tarjetas inteligentes.
  
-   **Excepciones en las conexiones para la solución de Woodgrove**. Como las tarjetas inteligentes se pueden perder, robar o, simplemente, olvidar, el equipo de TI de Woodgrove IT debe asegurarse de que su solución de implantación incluya un método ágil para distribuir con seguridad las tarjetas inteligentes de reemplazo, así como un sistema para administrar las excepciones durante el tránsito de las tarjetas de reemplazo.
  
#### Requisitos de la solución
  
Para proteger las cuentas de acceso remoto con tarjetas inteligentes, la solución debe incluir los siguientes componentes:
  
-   **Servicio de autenticación de Internet (IAS)**. Los servidores IAS actuales requieren actualizaciones a Windows Server 2003 con Service Pack 1 o posterior para facilitar los filtros de IP mejorados y la aceptación de atributos específicos del fabricante. Además, el departamento de TI de Woodgrove debe posibilitar la compatibilidad con EAP-TLS en los servidores de acceso remoto.
  
-   **Plantillas para usuarios de tarjetas inteligentes**. Woodgrove National Bank debe llevar a cabo la personalización de las plantillas de certificados y establecer los permisos adecuados para las plantillas. El agente de inscripción de certificados y las plantillas de inicio de sesión con tarjetas inteligentes requieren los permisos correspondientes.
  
    **Nota:** Es posible restringir el acceso remoto a los certificados de las tarjetas inteligentes si se establece una directiva de acceso remoto en virtud de la cual sólo se acepte un certificado con un identificador de objeto determinado. Para obtener más información acerca de las plantillas de certificados y los identificadores de objetos, consulte el documento sobre implementación y administración de plantillas de certificados en Windows Server 2003, en la dirección <http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03crtm.mspx>.
  
-   **Herramientas de administración de NIP**. Los usuarios necesitan una utilidad de software para administrar sus propios NIP. La mayoría de los fabricantes de tarjetas inteligentes proporcionan herramientas básicas para la administración de NIP. El departamento de TI de Woodgrove optó por ampliar la personalización para integrar la herramienta de administración de NIP con una utilidad de desbloqueo remoto de NIP.
  
-   **Objetos de directiva de grupo (GPO)**.** **El departamento de TI de Woodgrove debe crear el GPO adecuado a la estructura de sus unidades organizativas. Estos GPO deben incluir opciones de configuración para las excepciones, como los casos de los usuarios que pierden u olvidan su tarjeta inteligente o su NIP.
  
-   **Perfiles de Connection Manager**. El departamento de TI de Woodgrove debe crear perfiles de Connection Manager configurados especialmente que contengan la configuración de conexión de servidor de acceso telefónico o VPN para los servidores de acceso remoto de Woodgrove. El equipo de TI de Woodgrove también tiene que personalizar el texto de la interfaz de usuario del perfil de Connection Manager para ayudar a los usuarios a comprender el proceso de conexión y a indicarles qué deben hacer si surgen problemas. El departamento de TI de Woodgrove creó distintos perfiles de Connection Manager para diferentes tipos de usuarios, como ejecutivos, usuarios regulares y personal administrativo. Cada perfil tenía distintas prioridades durante la configuración de la conexión. Los administradores pueden conectarse de forma remota, independientemente del tráfico que haya en la red.
  
-   **Windows XP Professional con Service Pack 2**. Woodgrove National Bank debe actualizar todos los equipos de acceso remoto a Windows XP Professional con SP2 o posterior. Windows XP Professional con SP2 ofrece características de seguridad mejoradas, como el servidor de seguridad de Windows (Firewall) y avances en las prestaciones de actualización automática, con lo que aumenta la integridad de la solución de acceso remoto. Windows XP Home con SP2 proporciona estas ventajas desde el punto de vista de la seguridad, pero no puede unirse a un dominio y utilizar la Directiva de grupo. Windows 2000 Professional con SP4 no ofrece las mejoras de seguridad que incluye Windows XP Professional con SP2.
  
-   **Proceso de adquisición de tarjetas inteligentes y lectores**. Aunque Woodgrove National Bank cuenta con una infraestructura de claves públicas consolidada, el banco obtendría un escaso beneficio con la instalación del sistema Windows para tarjetas inteligentes si éstas estuvieran vacías. La mayoría de los fabricantes ofrecen tarjetas inteligentes con el sistema operativo ya instalado. La elección de tarjetas inteligentes y lectores de un mismo fabricante ofrece la ventaja de contar con un punto de contacto único para el soporte técnico.
  
-   **Lectores de tarjetas inteligentes USB o PC Card**.** **El establecimiento de estándares para la implantación minimiza el costo de instalación de una solución basada en tarjetas inteligentes. Woodgrove National Bank implantó una directiva corporativa en virtud de la cual todos los nuevos equipos portátiles integrarían lectores de tarjetas inteligentes. Woodgrove National Bank también ha establecido un estándar común para el suministro de lectores de tarjetas inteligentes USB. El banco suministra lectores de tarjetas inteligentes USB a los empleados que utilizan sus propios equipos para trabajar desde sus casas. Woodgrove se ha asegurado la continuidad a través de un contrato con el proveedor de lectores de tarjetas inteligentes que le permitirá contar con el mismo modelo de lectores durante dos años.
  
-   **Relaciones de confianza**. Para la implantación de tarjetas inteligentes en Woodgrove National Bank se utilizaron las relaciones de confianza actuales entre bosques independientes y cualquier confianza unidireccional, como las que existen entre bosques de los equipos de desarrollo más pequeños y el bosque corporativo principal. Para esta disposición no fue preciso realizar cambios en las plantillas de certificados.
  
-   **Infraestructura de claves públicas (PKI) de Windows Server 2003**. Los servicios de Certificate Server de Windows Server 2003 proporcionan la posibilidad de asignar permisos a elementos de una plantilla predeterminada de certificados de tarjetas inteligentes, así como de personalizar las plantillas. La mayor flexibilidad de los permisos con respecto a las plantillas es fundamental, ya que permite que el departamento de TI de Woodgrove delegue de un modo seguro el modelo de emisión de certificados definido. El departamento de TI de Woodgrove utiliza las características mejoradas de la infraestructura de claves públicas de Windows Server 2003 para establecer reglas de renovación automática de certificados. El equipo de TI utiliza las características de los permisos asociados a las plantillas de certificados para requerir que sean los responsables de seguridad de Woodgrove National Bank quienes creen todas las inscripciones de certificados de las nuevas tarjetas inteligentes. No obstante, el usuario puede renovar automáticamente todos los certificados de tarjeta inteligente actuales.
  
Woodgrove National Bank ya contaba con una infraestructura de claves pública de Windows 2000 Server cuando la organización decidió implantar tarjetas inteligentes. Para la fase piloto inicial, el departamento de TI de Woodgrove National Bank optó por utilizar su infraestructura de seguridad actual basada en Windows 2000 para la creación y administración de certificados destinados a tarjetas inteligentes, en lugar de recurrir a servicios de terceros. Sin embargo, la solución de seguridad con tarjetas inteligentes de Woodgrove requiere que los certificados caduquen en un plazo de un año. Este requisito supondría un considerable costo en soporte, ya que iba a ser necesario renovar decenas de miles de certificados de usuario cada año. Ante el consiguiente incremento de la carga de trabajo administrativo, el equipo de TI de Woodgrove National Bank decidió actualizar su infraestructura de claves públicas a la de Windows Server 2003.
  
Si Woodgrove National Bank hubiera utilizado la infraestructura de claves públicas de Windows 2000 Server para la renovación automática de certificados, las opciones relacionadas habrían quedado limitadas a dos: establecer todas las renovaciones de certificados como automáticas o renovar manualmente todos los certificados. La renovación automática de todos los certificados eliminaría la flexibilidad en cuanto a opciones de renovación.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Diseño de la solución
  
En esta sección se señalan las opciones de diseño que aplicó el departamento de TI de Woodgrove National Bank para utilizar las tarjetas inteligentes como método de protección de las conexiones de acceso remoto. En esta sección se incluye el concepto de la solución y los requisitos previos. Además, se describe la arquitectura de la solución.
  
#### Concepto de la solución
  
En la solución se utiliza una combinación de configuración de Directiva de grupo, directivas de acceso remoto, perfiles de Connection Manager, certificados de usuario X.509 v3 instalados en las tarjetas inteligentes y lectores de tarjetas inteligentes. Básicamente, la idea consiste en que un usuario de acceso remoto inicie un perfil de Connection Manager personalizado, con el que se pide al usuario que inserte una tarjeta inteligente en el lector conectado. Después, el sistema operativo le indica al usuario que escriba el NIP. Si el NIP es correcto, el lector extrae un certificado de tarjeta inteligente y la información de la cuenta. A continuación, Connection Manager establece una conexión con el servidor de acceso remoto y presenta las credenciales de la tarjeta inteligente. Active Directory autentica estas credenciales y el servidor de acceso remoto otorga al usuario acceso a la red corporativa.
  
#### Requisitos previos de la solución
  
Los requisitos previos para utilizar tarjetas inteligentes con el fin de proteger las cuentas de acceso remoto son similares a los de la solución basada en tarjetas inteligentes para proteger las cuentas de administrador. Deberá:
  
-   Consultar a los usuarios y grupos.
  
-   Seleccionar el personal para el proyecto.
  
-   Establecer las expectativas de los usuarios
  
-   Actualizar el hardware y el software.
  
-   Distribuir y activar las tarjetas inteligentes de un modo seguro.
  
##### Consulta a usuarios y grupos
  
Dentro del ciclo planeado, debe evaluar las soluciones de acceso remoto actuales y consultar a quienes las utilizan. Woodgrove National Bank opera en varios países y regiones, y en todos ellos hay usuarios que se conectan mediante acceso remoto. El equipo inicial sondeó las opiniones de los usuarios de acceso remoto y de los equipos de soporte actuales para identificar e implicar en la fase piloto a posibles usuarios, grupos y personal de soporte.
  
##### Selección del personal para el proyecto.
  
Debe asegurarse de contar con el personal y los recursos adecuados para implantar un proyecto de estas características. Es probable que el equipo del proyecto recabe opiniones de los siguientes representantes:
  
-   Director del programa
  
-   Diseñador de sistemas de información
  
-   Analista o integrador de sistemas
  
-   Ingenieros de sistemas
  
-   Responsable de lanzamiento de productos
  
-   Responsable de pruebas de productos
  
-   Responsable de soporte o asistencia técnica
  
-   Especialista de soporte a los usuarios
  
-   Responsables de seguridad
  
Para obtener más información acerca de los oficios representativos y las asociaciones de funciones en Microsoft Operations Framework (MOF), consulte el documento The Microsoft Solutions Framework Supplemental Whitepapers – IT Occupation Taxonomy (en inglés), en la dirección [http://www.microsoft.com/downloads/details.aspx?FamilyID=839058c3-d998-4700-b958-3bedfee2c053](http://www.microsoft.com/downloads/details.aspx?familyid=839058c3-d998-4700-b958-3bedfee2c053)
  
Si no dispone de los recursos internos necesarios, deberá contratar más personal. Como este proyecto no suele precisar la intervención simultánea del personal participante en todas las etapas, será preciso determinar la disponibilidad individual a lo largo del proyecto.
  
##### Establecimiento de las expectativas de los usuarios
  
El principal problema que plantean las tarjetas inteligentes y el acceso remoto desde el punto de vista de los usuarios es que se tarda más tiempo en iniciar sesión. Los usuarios deben prever que se incrementarán los tiempos de inicio de sesión en varios segundos con la autenticación mediante tarjetas inteligentes.
  
##### Actualización de hardware y software
  
En la solución basada en tarjetas inteligentes para el acceso remoto se necesitan los sistemas operativos y Service Pack de Microsoft más recientes. Este requisito permite aprovechar con la solución de acceso remoto los últimos avances y servicios de seguridad que ofrecen Windows XP Professional con SP2 y Windows Server 2003 con SP1, como el Firewall de Windows, Prevención de ejecución de datos (DEP), Asistente de configuración de seguridad y Cuarentena de VPN.
  
Las actualizaciones de software quizá precisen que se actualice el hardware de cliente o de servidor. Mediante un programa piloto se puede establecer si en los equipos antiguos se pueden ejecutar sistemas operativos más recientes. Para comprobar si los equipos están certificados para Windows XP o Windows Server 2003, consulte el tema sobre productos diseñados para Microsoft Windows: Catálogo de Windows y lista de compatibilidad de hardware, en la dirección <http://www.microsoft.com/whdc/hcl/default.mspx?gssnb=1>.
  
##### Distribución y activación de las tarjetas inteligentes de un modo seguro
  
En la implantación de tarjetas inteligentes para el acceso remoto se necesita un método seguro para la distribución y activación de las tarjetas. Normalmente, para este proceso de distribución sería preciso que los usuarios remotos informasen a su oficina administrativa local para que el agente de inscripción pueda comprobar su identidad, emitir la tarjeta inteligente y llevar a cabo el procedimiento de activación. En la sección relativa al modelo de emisión delegada, que encontrará más adelante en este capítulo, se describe el sistema utilizado por Woodgrove National Bank para la distribución y activación de las tarjetas inteligentes destinadas a los usuarios remotos.
  
#### Arquitectura de la solución
  
La implantación de la solución basada en tarjetas inteligentes adoptada por Woodgrove National Bank para el acceso remoto precisa los siguientes componentes:
  
-   Active Directory
  
-   IAS instalado en un servidor con Windows Server 2003.
  
-   Windows Server 2003 con SP1, con enrutamiento y acceso remoto.
  
-   Directiva de grupo
  
-   Equipos cliente en los que se ejecute Windows XP Professional con SP2 o posterior.
  
-   Lectores de tarjetas inteligentes.
  
-   Tarjetas inteligentes con 32 KB de memoria, como mínimo.
  
-   Perfiles de Connection Manager creados con CMAK.
  
-   Secuencias de comandos de cliente para el perfil de Connection Manager.
  
El departamento de TI de Woodgrove consideró en principio la posibilidad de admitir todas las versiones de Windows implantadas. Sin embargo, conscientes de la amenaza a la que se exponen los equipos conectados a Internet, optaron por normalizarse con Windows XP Professional con SP2.
  
Las cuentas de usuarios y las pertenencias a grupos almacenadas en Active Directory regulan la conexión y el acceso a los recursos corporativos de la entidad Woodgrove National Bank. El departamento de TI de Woodgrove también utiliza GPO para la configuración de equipos cliente a fin de cumplir las directivas de seguridad de las redes corporativas.
  
#### Cómo funciona la solución
  
En esta sección se proporcionan detalles técnicos de la solución adoptada por Woodgrove National Bank. Se explica cómo autentica Active Directory al usuario y cómo realiza el seguimiento de la ruta de autenticación para las credenciales de la tarjeta inteligente.
  
El siguiente procedimiento posibilita el acceso remoto con tarjetas inteligentes:
  
1.  Un usuario remoto inicia sesión en un equipo con acceso a Internet que tiene conectado un lector de tarjetas inteligentes. El usuario inicia el perfil personalizado de Connection Manager; para esto hace doble clic en la conexión **Connection Manager de TI de Woodgrove para tarjetas inteligentes**.
  
2.  El perfil de Connection Manager comprueba si hay una tarjeta inteligente en el lector. Aparece un cuadro de diálogo en el que se pide al usuario que escriba el NIP. Connection Manager utiliza el NIP para realizar operaciones importantes con la tarjeta como servicio del sistema, ya que no puede presentar mensajes ni mostrar la interfaz de usuario en el escritorio. Si el usuario escribe el NIP adecuado, la tarjeta se desbloquea y permite que continúe el proceso de inicio de sesión para el acceso remoto.
  
3.  La Autoridad de seguridad local (LSA) es el componente de confianza del sistema operativo que realiza todas las autenticaciones. SChannel, que es el código que implanta SSL, se ejecuta parcialmente en la LSA e inicia la secuencia de asignación.
  
4.  El perfil de Connection Manager inicia un vínculo con los servidores IAS de Woodgrove National Bank mediante una conexión de acceso telefónico o VPN. El servidor IAS realiza una comprobación de revocación con el certificado del cliente. Con la asignación del certificado al nombre principal del usuario (UPN), la entidad emisora de certificados debe encontrarse en el almacén NTAUTH. También se puede establecer una asignación explícita en la cuenta de usuario de Active Directory.
  
5.  La LSA presenta la información del usuario al servidor IAS. El código SChannel que se ejecuta en el servidor IAS envía un mensaje al código SChannel del controlador de dominio y le transfiere la información de UPN del certificado.
  
6.  El código SChannel que se ejecuta en el servidor IAS valida el certificado y después realiza una búsqueda del usuario con Active Directory en el controlador de dominio. El controlador de dominio genera un certificado de acceso a privilegios (Privilege Access Certificate, PAC) que contiene el identificador de 128 bits del usuario y su pertenencia al grupo. A partir de ese punto, en las comunicaciones posteriores se utiliza el protocolo Kerberos v5.
  
7.  El controlador de dominio transmite una clave de sesión generada aleatoriamente que incluye el tíquet de obtención de tíquet (TGT) de Kerberos para el equipo cliente. Con la recepción de esta clave se autentica el servidor de acceso remoto para el cliente. Ahora, los dos equipos se han autenticado mutuamente.
  
8.  El equipo cliente descifra la clave de inicio de sesión y presenta el TGT de Kerberos v5 al servicio de concesión de vales. Una vez concluido este proceso, en todas las restantes comunicaciones con el protocolo Kerberos v5 se utiliza el cifrado simétrico.
  
9.  Si el usuario estableció una conexión de acceso telefónico, se le piden el nombre de usuario y la contraseña. El usuario escribe las credenciales y, a partir de ese momento, puede obtener acceso a todos los recursos de la red de Woodgrove Bank. Los usuarios que se conectan a través de VPN no tienen que realizar esta operación.   
  
En la ilustración siguiente se muestran los pasos que deben seguirse para utilizar una tarjeta inteligente con fines de autenticación de acceso remoto.
  
[![](images/Cc170941.pabc0401(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc170941.pabc0401_big(es-es,technet.10).gif)
  
**Ilustración 4.1 Inicio de sesión de acceso remoto y proceso de autenticación con una tarjeta inteligente**
  
Los ciclos de procesador adicionales que se necesitan para procesar la información de la tarjeta inteligente equivalen a prolongar entre 20 y 25 segundos el proceso de autenticación inicial. Una vez finalizada la autenticación, el rendimiento no se ve afectado.
  
#### Consideraciones de diseño adicionales
  
En la siguiente sección se detallan consideraciones adicionales para la implantación de tarjetas inteligentes y se incluye el mecanismo de distribución de tarjetas inteligentes utilizado por la entidad Woodgrove National Bank.
  
##### Modelo de emisión delegada
  
El departamento de TI de Woodgrove National Bank desarrolló un modelo de emisión delegada de las tarjetas inteligentes. Este modelo ofrece una respuesta más ágil que contribuye a asegurar el máximo nivel de seguridad para la distribución en todo el mundo de tarjetas inteligentes para los empleados.
  
El equipo de TI de Woodgrove National Bank utilizó un modelo de emisión delegada para implantar la solución de tarjetas inteligentes fuera de la sede central de TI en Londres. El departamento de TI de Woodgrove National Bank envió técnicos a las oficinas de todo el mundo para formar a los responsables delegados de emisión (DIO, Delegated Issuance Officers). Los técnicos formaron a los DIO en la distribución de tarjetas inteligentes y en el uso de las herramientas relacionadas con las tarjetas. Tras la visita inicial, los DIO participaban en conferencias semanales con el equipo de TI de la sede central de Woodgrove National Bank para tratar las cuestiones que iban surgiendo.
  
En la siguiente ilustración se muestran los pasos del modelo de emisión delegada para la aprobación de solicitudes de certificados.
  
[![](images/Cc170941.pabc0402(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc170941.pabc0402_big(es-es,technet.10).gif)
  
**Ilustración 4.2 Proceso de delegación utilizado para emitir tarjetas inteligentes destinadas al acceso remoto**
  
Los pasos que se siguen de acuerdo con este diagrama de flujo son los siguientes:
  
1.  El usuario solicita una tarjeta inteligente al DIO.
  
2.  El DIO valida la identidad del usuario a partir de un documento de identificación válido, como un pasaporte o un permiso de conducir, y comprueba la identidad del usuario con el jefe del departamento. Después de confirmar la identidad del usuario, el DIO envía una solicitud a uno de los responsables de seguridad que se encuentran en Londres.
  
3.  Para validar la solicitud, el responsable de seguridad comprueba si se había emitido anteriormente algún otro certificado para ese usuario. El responsable de seguridad determina también si el usuario ha solicitado alguna otra tarjeta inteligente. Si no hay objeciones para la emisión de la tarjeta inteligente, el responsable de seguridad da su aprobación. Si el responsable de seguridad detecta algún problema, el proceso debe someterse a una auditoría, tal como se describe en el quinto paso.
  
4.  El DIO recibe la aprobación y utiliza la cuenta del agente de inscripción para emitir el certificado. Este certificado se adjunta a una nueva tarjeta inteligente, que el DIO expide al usuario en persona. Así se completa el proceso de emisión delegada.
  
5.  Si existen dudas acerca de la validez de la solicitud, el responsable de seguridad inicia una auditoría de la solicitud para determinar si debe otorgarse la aprobación a ese usuario. Una vez concluida la auditoría, el usuario debe presentar una nueva solicitud.
  
6.  Se completa el proceso de emisión delegada.
  
Woodgrove National Bank sólo podía implantar el modelo de emisión delegada después de que el departamento de TI realizara la migración de las entidades emisoras de certificados de la empresa a Windows Server 2003. La infraestructura de claves públicas de Windows Server 2003 permite aplicar permisos detallados a secciones de las plantillas de certificados, lo que posibilita la función de los DIO en el modelo de emisión delegada. Dentro del modelo de emisión, Woodgrove desarrolló procedimientos para volver a emitir de forma segura tarjetas inteligentes perdidas o robadas.  
  
##### Configuración de cuentas RADIUS
  
Aunque no sea imprescindible, Microsoft recomienda el mantenimiento de registros para la implantación de una solución de acceso remoto basada en tarjetas inteligentes. Si utiliza IAS, una de las ventajas es la compatibilidad integrada con el proveedor de cuentas RADIUS, que registra las solicitudes de conexión y las sesiones de cliente. Woodgrove National Bank desea supervisar qué usuarios inician sesión, en qué momento y durante cuánto tiempo están conectados a la red corporativa. RADIUS brinda a Woodgrove la posibilidad de analizar tendencias por lo que respecta a las conexiones, con objeto de revisar y mejorar el servicio.
  
Cada servidor IAS recopila datos de las sesiones de los usuarios, que almacena en Microsoft SQL Server™ Desktop Engine (Windows) (WMSDE) en el caso de Windows Server 2003, o en SQL Server 2000 Desktop Engine (MSDE 2000) con Windows 2000 Server y anteriores. IAS transfiere la información de cuentas desde WMSDE o MSDE a una base de datos central SQL Server 2000 casi en tiempo real. Esta disposición garantiza un uso rentable de las licencias de SQL Server y no altera el rendimiento del servidor.
  
Woodgrove National Bank implantó a escala regional servidores de recopilación de datos basados en SQL Server para recabar información de las sesiones de acceso remoto con IAS.
  
##### Implantación en fases piloto
  
El departamento de TI de Woodgrove National Bank prueba todas las soluciones en un entorno de laboratorio y realiza más de una prueba piloto antes de la implantación en la red de producción. El equipo de TI de Woodgrove desarrolló dos pruebas piloto para la implantación de tarjetas inteligentes destinadas al acceso remoto: en una participó un grupo reducido de usuarios experimentados y la otra incluía un grupo más heterogéneo de usuarios de distintos países y regiones, con distintos grados de experiencia en cuanto al acceso remoto.
  
Las pruebas piloto con los usuarios más experimentados permitieron a Woodgrove National Bank identificar los principales problemas de la implantación de tarjetas inteligentes. Los usuarios con más experiencia sortearon sin dificultad los problemas menores y los cuadros de diálogo inesperados. Cuando el departamento de TI de Woodgrove terminó la primera fase piloto, sabían que la solución basada en tarjetas inteligentes funcionaría, pero eran necesarios algunos ajustes.
  
La segunda fase piloto, en la que intervinieron usuarios de características muy diversas, permitió al departamento de TI de Woodgrove conocer en la práctica el tipo de llamadas al soporte técnico que cabe esperar con la implantación completa. Gracias a estas pruebas piloto, el departamento de asistencia pudo resolver problemas técnicos y fue posible detectar la necesidad de ciertas mejoras antes de la implantación de un sistema de tarjetas inteligentes para todos los usuarios remotos.
  
##### Garantía de alta disponibilidad
  
El escenario de la solución debe ofrecer una gran confiabilidad debido a que el mantenimiento de la productividad es un requisito fundamental de la solución de acceso remoto. Woodgrove National Bank debe considerar las disposiciones necesarias para mantener un alto grado de disponibilidad. Estas recomendaciones son:
  
-   Servidores de acceso remoto con carga equilibrada.
  
-   Servidores IAS con carga equilibrada.
  
-   Rutas de acceso a red redundantes.
  
    **Nota:** Woodgrove Bank cuenta con puntos de entrada de Enrutamiento de acceso remoto/IAS ubicados geográficamente debido al diseño físico de la red.
  
##### Garantía de un ancho de banda de red adecuado
  
Los diseñadores de sistemas deben tener en cuenta las actuales rutas de acceso a la red, los tiempos de conexión previstos y el tipo y volumen de tráfico de acceso remoto previsto. No debe subestimarse el ancho de banda adicional que los usuarios de acceso remoto pueden precisar. Las implantaciones piloto deben servir de ayuda en el análisis de los patrones de tráfico de acceso remoto y de las repercusiones que puede tener ese tráfico en la infraestructura de red actual. Es importante que en las pruebas participen usuarios no técnicos y que se incluyan patrones de uso típicos, que es más probable que se reproduzcan en la implantación completa. Los conmutadores de hardware que incorporan control de ancho de banda y las redes de área local virtuales (VLAN) pueden reducir la incidencia del tráfico de acceso remoto en otros usuarios.
  
Woodgrove National Bank utiliza varios proveedores de servicios Internet para conseguir una buena conectividad. Una gran parte del ancho de banda actual proporciona acceso a Internet para la investigación en Web y el correo electrónico. El departamento de TI de Woodgrove debe revisar las disposiciones actuales para acomodar el tráfico adicional asociado a las conexiones de acceso remoto.
  
##### Excepciones
  
Los diseñadores de sistemas de Woodgrove National Bank son conscientes de que, cualquiera que sea la solución, tiene que prever situaciones en las que las necesidades de la empresa dicten exenciones temporales de los requisitos de seguridad normales para uno o varios dispositivos. Por ejemplo, el acceso remoto para los ejecutivos durante una reunión de especial importancia puede quedar exento de autenticación mediante tarjetas inteligentes. Si la solución basada en tarjetas inteligentes no puede permitir excepciones individualizadas para dispositivos determinados, el departamento de TI se verá obligado a deshabilitar todos los requisitos para el acceso remoto a causa de una sola excepción. Así pues, la solución basada en tarjetas inteligentes debe admitir excepciones.
  
**Nota:** El grupo de seguridad de TI de Woodgrove debe ser la única autoridad que determine cuándo procede una excepción por necesidades empresariales y si se justifica el consiguiente riesgo para la seguridad.
  
El equipo de TI de Woodgrove creó un nuevo grupo de seguridad, con el nombre RemoteSmartCardUsersTempException, para las excepciones temporales al requisito de uso de tarjeta inteligente en el acceso remoto. A continuación configuraron las directivas de acceso remoto para el servidor de acceso remoto entrante según se indica en la tabla que se muestra a continuación.
  
**Tabla 4.1: Condiciones de la directiva de acceso remoto de Woodgrove National Bank**

 
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Requisito</th>
<th>Condiciones de la directiva</th>
<th>Tipo de autenticación</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Requerir la autenticación con tarjetas inteligentes para los miembros del grupo de usuarios de acceso remoto</td>
<td style="border:1px solid black;">Los grupos de Windows coinciden con &quot;WOODGROVE\RemoteSmartCardUsers&quot;</td>
<td style="border:1px solid black;">EAP - tarjeta inteligente u otro certificado únicamente.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">No requerir la autenticación con tarjetas inteligentes para los miembros del grupo de exclusiones temporales</td>
<td style="border:1px solid black;">Los grupos de Windows coinciden con &quot;WOODGROVE\RemoteSmartCardUsersTempException&quot;</td>
<td style="border:1px solid black;">MSCHAP v2</td>
</tr>
</tbody>
</table>
  
Esta disposición exige el requisito de la tarjeta inteligente para los miembros del grupo RemoteSmartCardUsers, pero no para los del grupo RemoteSmartCardUsersTempException. Para obtener más información acerca de cómo requerir la autenticación con tarjeta inteligente para los usuarios remotos, consulte el tema Configurar el acceso remoto con tarjetas inteligentes, en la dirección [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/ServerHelp/863638a6-f9e0-48d7-9db5-0b54af3cf135.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/863638a6-f9e0-48d7-9db5-0b54af3cf135.mspx).
  
##### Aplicación de los procedimientos recomendados
  
El departamento de TI de Woodgrove National Bank estableció la siguiente lista de recomendaciones para los procedimientos:
  
-   **Implicar al personal de asistencia**. Un departamento de asistencia bien preparado debe ser uno de los componentes esenciales de cualquier proyecto relacionado con tarjetas inteligentes. Después de la implantación, el papel del personal de asistencia pasa a ser de mantenimiento. Es esencial que el personal de asistencia esté puntualmente informado de cualquier cambio del sistema interno y de las novedades técnicas que afecten al uso.
  
-   **Proporcionar administración de NIP**.** **Como el principal objetivo del uso de las tarjetas inteligentes es mejorar la seguridad de la red, es esencial mantener seguros los datos almacenados en las tarjetas. El olvido de un NIP constituye un reto, tanto durante la implantación del sistema de tarjetas inteligentes como posteriormente. Debe consultar al fabricante de las tarjetas inteligentes acerca del suministro de herramientas de administración de NIP e implementar procesos de restablecimiento de NIP para usuarios que no puedan hacerlo en una ubicación de la empresa (por ejemplo, cuando se desplazan).
  
-   **Implementar medidas contra alteraciones**. Las tarjetas inteligentes necesitan protección contra las alteraciones, de modo que se bloqueen si un usuario escribe mal el NIP cinco veces consecutivas.
  
-   **Mantener un equipo para la fase posterior a la implantación**. El equipo dedicado a administrar la fase posterior a la implantación puede ser mucho más reducido que el equipo inicial, pero es necesario para supervisar periódicamente la integridad del sistema, así como para probar y coordinar las posibles actualizaciones de la infraestructura de claves públicas.
  
#### Supervisión y administración
  
Una solución en la que se utilicen tarjetas inteligentes para proteger el acceso remoto debe incluir la posibilidad de supervisar el estado de funcionamiento de la propia solución. Este proceso tiene que posibilitar la supervisión de toda la red, de un activo en particular o de una lista de activos en tiempo real. A través de las herramientas de supervisión debe mostrarse toda la información que necesita una organización para apoyar las operaciones. Si no se cumple ese requisito, el personal de seguridad no podrá determinar si la solución mantiene con eficacia conexiones de acceso remoto seguras.
  
##### Identificación de consideraciones sobre las operaciones
  
El departamento de TI de Woodgrove identificó las siguientes consideraciones sobre el funcionamiento durante la implantación de la solución:
  
-   **Comprobar la autenticación de acceso a las aplicaciones internas**. Una tarjeta inteligente sólo debe afectar al inicio de sesión inicial. El programa de prueba debe probar y comprobar la correcta autenticación de aplicaciones internas.
  
-   **Solucionar problemas relacionados con clientes remotos**. Para una solución de problemas con éxito, los problemas del cliente pueden requerir una estrecha cooperación entre varios equipos repartidos en diferentes zonas horarias. La realización de pruebas rigurosas y una adecuada implantación piloto contribuyen a reducir el número de llamadas al departamento de soporte técnico
  
-   **Comprender el contexto del acceso remoto y las posibles amenazas para la organización**. Debe comprender los escenarios de acceso remoto en la organización, las amenazas para la seguridad y cómo alcanzar un punto de equilibrio. Es necesario dar prioridad a los activos que necesitan una mayor protección y determinar equilibrio adecuado entre costo y riesgo; estas decisiones estratégicas corresponden a la directiva de la empresa.
  
-   **Anticiparse a los desafíos técnicos**. Debe anticiparse a los retos técnicos, como las rutinas de instalación y la distribución de herramientas de administración de tarjetas inteligentes. Es posible que necesite integrar la solución de tarjeta inteligente en sus herramientas de administración empresarial existentes.
  
-   **Supervisión y administración de problemas de rendimiento**. Debe supervisar y administrar los problemas de rendimiento y establecer las expectativas del usuario antes de la implementación. Por ejemplo, los usuarios remotos que inicien sesión por primera vez pueden experimentar una considerable demora en el inicio de sesión si seleccionan la opción **Iniciar sesión usando una conexión de acceso telefónico**, del cuadro de diálogo **Iniciar sesión en Windows**. Debe asegurarse de que los usuarios remotos están informados de esta demora.
  
-   **Actualizar**. Si ha planeado una actualización con la tecnología más reciente, hágalo en una fase temprana del proceso de implantación. Esta estrategia proporciona una plataforma de referencia de cliente y servidor y evita muchas de las variables que podrían surgir durante la implantación. La estabilidad del servicio también aumentará y contribuirá a reducir el costo de soporte a los usuarios.
  
-   **Implantar el proyecto en varias fases**. La implantación del proyecto debe realizarse en varias fases, con un margen de tiempo suficiente entre éstas para que los usuarios vayan adaptándose progresivamente y se estabilicen los procesos. El solapamiento de fases puede tener repercusiones negativas en el servicio e impedir la identificación de problemas.
  
-   **Tener en cuenta los activos personales**. Recuerde que los equipos domésticos de los empleados no son propiedad de la empresa y que no los administra el departamento de TI. Si un empleado no desea o no puede instalar el hardware o el software necesarios para el uso de tarjetas inteligentes para el acceso remoto seguro, hay otras opciones disponibles. Por ejemplo, Microsoft Outlook® Web Access proporciona a los empleados un acceso seguro a su buzón de correo en Microsoft Exchange Server.
  
-   **Administrar los cambios realizados en la solución**. Debe administrar cualquier cambio y mejora realizados en la solución a través de procesos similares a los requeridos para la implementación inicial.
  
-   **Optimizar la solución.** Todos los aspectos de la solución de tarjeta inteligente requieren revisiones y optimizaciones periódicas. De forma regular, el departamento de TI de Woodgrove debe revisar los procesos de inscripción y la necesidad de excepciones en las cuentas, con objeto de mejorar la seguridad y la integridad.
  
##### Cómo ampliar la solución
  
Las tarjetas inteligentes ofrecen un potencial considerable para la implantación de aplicaciones. Por ejemplo, los programadores pueden adaptar la plataforma abierta extensible para las tarjetas inteligentes y proteger la memoria para usos tales como un sistema de pago para la cafetería en el que no intervenga el dinero en metálico.
  
Aunque el uso de tarjetas inteligentes para proteger el acceso remoto reduce la posibilidad de ataques por parte de usuarios no autorizados, la solución no garantiza que los equipos desde los que se obtiene acceso remoto cumplan con las directivas de seguridad de la red. El Control de cuarentena para el acceso a redes, que es una característica de Windows Server 2003 con SP1, puede confirmar que en los equipos remotos se ejecutan las últimas actualizaciones de software antivirus y de seguridad. La función de control de cuarentena permite realizar otras comprobaciones; por ejemplo, que está habilitado el Firewall de Windows en Windows XP con SP2. Para obtener más información acerca del control de cuarentena, consulte el artículo sobre la guía de planeamiento para la implementación de servicios de cuarentena con una red privada virtual de Microsoft, en la dirección [http://go.microsoft.com/fwlink/?LinkId=41307](http://go.microsoft.com/fwlink/?linkid=41307).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
La implementación de tarjetas inteligentes para autenticar conexiones de acceso remoto ofrece más seguridad que las combinaciones simples de nombre de usuario y contraseña. Las tarjetas inteligentes implementan autenticación en dos fases mediante la combinación de la tarjeta inteligente y un NIP. La autenticación de dos factores es mucho más difícil de poner en peligro y el NIP es más fácil de recordar que una contraseña segura.
  
La autenticación de tarjetas inteligentes para usuarios de acceso remoto constituye un método confiable y rentable para aumentar la seguridad de la red. En esta guía se han mostrado los pasos necesarios para planear e implementar esta solución.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Apéndice A: Vínculos relacionados
  
Los siguientes recursos contienen más información acerca de los puntos tratados en esta guía:
  
Para obtener más información acerca de las nueva mejoras en PKI que incorporan Windows XP y Windows Server 2003, consulte el artículo [Mejoras de la infraestructura de claves públicas (PKI) en Windows XP Professional y Windows Server 2003](http://www.microsoft.com/technet/prodtechnol/winxppro/plan/pkienh.mspx), en la dirección www.microsoft.com/technet/prodtechnol/winxppro/plan/pkienh.mspx
  
Para obtener más información acerca de las implantaciones de tarjetas inteligentes, consulte el artículo sobre [planeamiento de una implantación de tarjetas inteligentes](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/deployguide/en-us/dsscg_smc_overview.asp), en la dirección www.microsoft.com/resources/documentation/WindowsServ/2003/all/deployguide/en-us/DSSCG\_SMC\_OVERVIEW.asp
  
Para obtener ayuda en el planeamiento de implantaciones de tarjetas inteligentes, descargue [Job\_Aids\_Designing\_and\_Deploying\_Directory\_and\_Security\_Services.zip](http://download.microsoft.com/download/0/0/a/00a285c4-9980-48b9-bef6-a2e6f077d5dd/job_aids_designing_and_deploying_directory_and_security_services.zip) de http://download.microsoft.com/download/0/0/a/00a285c4-9980-48b9-bef6-a2e6f077d5dd/Job\_Aids\_Designing\_and\_Deploying\_Directory\_and\_Security\_Services.zip. Los documentos de apoyo sobre tareas con tarjetas inteligentes son los que están comprendidos entre DSSSMC\_1.doc y DSSSMC\_5.doc.
  
Para obtener la información más reciente acerca de Windows Server 2003, visite el [sitio Web de Windows Server 2003](http://www.microsoft.com/windowsserver2003), en la dirección www.microsoft.com/windowsserver2003.
  
Para obtener más información acerca de la implementación de tarjetas inteligentes, consulte [The Smart Card Deployment Cookbook](http://www.microsoft.com/technet/security/guidance/identitymanagement/smrtcdcb/default.mspx) (en inglés), en www.microsoft.com/technet/security/guidance/identitymanagement/smrtcdcb/default.mspx.
  
Para obtener más información acerca de los procedimientos recomendados para la implantación de una infraestructura de claves públicas con Windows Server 2003, consulte el artículo sobre [prácticas recomendadas para la implantación de una infraestructura de claves públicas con Microsoft Windows Server 2003](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws3pkibp.mspx), en la dirección www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws3pkibp.mspx.
  
Si desea adquirir lectores de tarjetas inteligentes con fines de evaluación, visite [Windows Marketplace](http://www.windowsmarketplace.com/results.aspx?text=smartcard), en la dirección www.windowsmarketplace.com/results.aspx?text=smartcard.
  
Para obtener más información acerca de la arquitectura de referencia de Windows Server System, consulte el artículo sobre la [arquitectura de referencia de Windows Server System](http://www.microsoft.com/technet/itsolutions/wssra/default.mspx), en la dirección www.microsoft.com/technet/itsolutions/wssra/default.mspx
  
Para obtener más información acerca de la certificación cruzada y la subordinación completa, consulte el artículo sobre [planeamiento e implantación de la certificación cruzada y la subordinación completa con Windows Server 2003](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03qswp.mspx), en la dirección www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03qswp.mspx
  
Para obtener más información acerca de la implantación y administración de plantillas de certificados en Windows Server 2003, consulte el artículo sobre [implantación y administración de plantillas de Certificate en Windows Server 2003](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03crtm.mspx), en la dirección www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03crtm.mspx
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Agradecimientos
  
El equipo Solution Accelerators: Security and Compliance (SA-SC) y el Security Center of Excellence (SCoE) desea agradecer y reconocer la labor realizada por el equipo que elaboró la *Guía de planeamiento de acceso seguro con tarjetas inteligentes*. Las siguientes personas fueron responsables directamente de la escritura, el desarrollo y la prueba de la solución, o bien realizaron una contribución importante a estas tareas.
  
#### Autores
  
Anthony Steven, *Content Master*
  
Terry Tull, *Content Master*
  
Lee Walker
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Revisores
  
Mert Biyikly
  
Chase Carpenter
  
David Cross
  
Kurt Dillard
  
John Howie
  
Greg Lenti
  
Jose Maldonado
  
John Morello
  
Dave Mowers
  
Steve Patrick
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Directores del programa
  
Neil Bufton, *Content Master*
  
Chase Carpenter
  
Tom Cloward
  
Alison Woolford, *Content Master*
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Editores
  
John Cobb, *Wadeware, LLC*
  
Deborah Jay, *Content Master*
  
Jennifer Kerns, *Content Master*
  
Frank Manning, *Volt*
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Evaluadores
  
Ashish Java, *Infosys Technologies*
  
Mehul Mediwala, *Infosys Technologies*
  
Gaurav Singh Bora, *Infosys Technologies*
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Administrador de versiones
  
Flicka Enloe
  
Karina Larson
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Colaboradores
  
Tony Bailey
  
Krishna Bhardwaj, *Vidyatech Solutions*
  
Prabish Chandran, *Vidyatech Solutions*
  
Charles Denny
  
Christine Duell, *Valente Solutions*
  
Amy Frampton
  
Michael Glass, *Volt*
  
Karl Grunwald
  
Joanne Kennedy
  
Karina Larson, *Volt*
  
Chrissy Lewis, *Siemens*
  
Don McGowan
  
Tessa Porterfield
  
Bivin Pachatt *Vidyatech Solutions*
  
Vivek Manohar Prabhu, *Vidyatech Solutions*
  
Stacey Tsurusaki, *Volt*
  
David Visintainer, *Volt*
  
Vikas Walia, *Vidyatech Solutions*
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
-   [Guía de planeamiento de acceso seguro con tarjetas inteligentes](http://go.microsoft.com/fwlink/?linkid=41314)  
-   [Obtenga la Guía de planeamiento de acceso seguro con tarjetas inteligentes](http://go.microsoft.com/fwlink/?linkid=41314)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener información acerca de las actualizaciones y las nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=guía%20de%20planeamiento%20de%20acceso%20seguro%20con%20tarjetas%20inteligentes)
  
[](#mainsection)[Principio de la página](#mainsection)
