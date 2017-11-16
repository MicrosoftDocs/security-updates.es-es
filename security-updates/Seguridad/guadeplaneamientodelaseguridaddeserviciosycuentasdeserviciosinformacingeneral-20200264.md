---
TOCTitle: 'Guía de planeamiento de la seguridad de servicios y cuentas de servicios: Información general'
Title: 'Guía de planeamiento de la seguridad de servicios y cuentas de servicios: Información general'
ms:assetid: '551a769e-d7c1-41c2-8c2e-301350aedfbb'
ms:contentKeyID: 20200264
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc170953(v=TechNet.10)'
---

Guía de planeamiento de la seguridad de servicios y cuentas de servicios
========================================================================

### Información general

Actualizado: mayo 31, 2005

Esta guía constituye un importante recurso para planear estrategias de ejecución de servicios de forma segura con los sistemas operativos Microsoft® Windows Server™ 2003 y Windows® XP. Trata el problema habitual de los servicios de Windows establecidos para ejecutarse con los mayores privilegios posibles, que un atacante podría poner en peligro para obtener acceso completo y sin restricciones al equipo o dominio, o incluso a todo el bosque. Describe las formas de identificación de servicios que se pueden ejecutar con menores privilegios y explica cómo reducir dichos privilegios metódicamente. Esta guía le servirá de ayuda para evaluar la infraestructura actual de los servicios y tomar decisiones importantes en el planeamiento de futuras implementaciones.

Microsoft ya ha comprobado la ejecución de los servicios incluidos en los sistemas operativos Windows Server 2003 y Windows XP con las cuentas de inicio de sesión predeterminadas, con el fin de garantizar que se ejecutan con el nivel mínimo de privilegios posible y que resultan lo suficientemente seguros. Estos servicios no necesitan modificarse. El principal objeto de análisis de esta guía consiste en asegurar los servicios que no se proporcionan con el sistema operativo como, por ejemplo, los que se ofrecen como componente de otros productos del servidor de Microsoft: por ejemplo, Microsoft SQL Server™ o Microsoft Operations Manager (MOM). Los servicios instalados con aplicaciones de software de terceros y las aplicaciones de la línea de negocios desarrolladas de forma interna pueden requerir mejoras de seguridad adicionales.

El objetivo fundamental de esta guía es el de ayudar a los administradores a reducir el efecto de un servicio en situación de riesgo en un sistema operativo host. La guía se basa en la experiencia de Security Center of Excellence (SCoE) en entornos de clientes y representa las prácticas recomendadas de Microsoft.

##### En esta página

[](#eeaa)[Información general](#eeaa)
[](#edaa)[Motivos para una ejecución más segura de los servicios](#edaa)
[](#ecaa)[Destinatarios de la guía](#ecaa)
[](#ebaa)[Información general de la guía de planeamiento](#ebaa)
[](#eaaa)[Comuníquenos su opinión](#eaaa)
[](#zxcv)[Capítulo 1: Introducción](#zxcv)
[](#zxcb)[Capítulo 2: Cómo mejorar la seguridad de la ejecución de servicios](#zxcb)
[](#zxcn)[Capítulo 3: Ejecución más segura de servicios](#zxcn)
[](#xzcn)[Capítulo 4: Resumen](#xzcn)

### Información general

Las organizaciones deben garantizar una ejecución segura de sus servicios. Si se dispone de directivas y prácticas adecuadas, los servicios no seguros se pueden proteger frente a los ataques. En estos ataques, se facilita acceso a nombres de usuario y contraseñas que el servicio emplea para la autenticación cuando se inicia o se conecta a otros equipos del dominio. En el peor de los casos, un usuario no autorizado puede obtener acceso de administrador de nivel de dominio.

Los servicios de Windows son programas ejecutables que funcionan en sesiones fuera de la sesión del usuario conectado actualmente. Su ejecución se produce en segundo plano, independiente de cualquier sesión de usuario. Los servicios pueden comenzar automáticamente cuando se inicie el equipo, se pueden detener y volver a iniciar y por sí mismos no muestran ninguna interfaz de usuario (IU), aunque se suelen comunicar con una de ellas para su control y administración. Debido a este comportamiento, los servicios resultan idóneos para utilizarse en un servidor o donde sea necesaria una funcionalidad a largo plazo que no interfiera con otros usuarios que se encuentren trabajando en el mismo equipo. Además de los servicios creados por Microsoft, muchos otros proveedores diseñan productos para que se implementen como servicios que se ejecutan continuamente en segundo plano.

La vulnerabilidad de seguridad de los servicios se origina en el modo en que las organizaciones han acostumbrado a implementarlos. Al igual que sucede con los usuarios, los servicios requieren un medio de autenticación para utilizar recursos de red o equipo. Antes del lanzamiento del sistema operativo Windows 2000, los servicios que tenían acceso a los recursos de una red debían utilizar una cuenta de usuario de dominio para autenticarse en cada servidor remoto que utilizaran, ya que la cuenta del sistema local no podía realizar la autenticación en la red. Con Windows 2000, la cuenta del sistema local se modificó para permitir la autenticación en los recursos de red, al igual que sucede con las cuentas de usuario de dominio, aunque en cambio se utilizan las credenciales del equipo para la autenticación. Una cuenta de equipo es esencialmente una cuenta de usuario que no dispone del atributo UserAccountControl, por lo que este tipo de cuentas puede iniciar sesión y tener acceso a los recursos del mismo modo que un usuario. Debido a estos cambios, la cuenta del sistema local pasó a ser una de las cuentas más habituales en la implementación de servicios. Con la aparición de Windows Server 2003, la situación volvió a cambiar cuando se agregaron dos nuevos tipos de cuenta integrada similar al sistema local: la cuenta Servicio de red y la cuenta Servicio local.

La nueva cuenta Servicio de red también utiliza las credenciales del equipo cuando se autentica de forma remota, aunque tiene un nivel de privilegio muy reducido en el propio servidor, por lo que no dispone de privilegios de administrador local. La cuenta Servicio local tiene los mismos privilegios reducidos que la cuenta Servicio de red, pero, como su propio nombre indica, no dispone de la capacidad de autenticar en los recursos de red.

La ejecución más segura de los servicios es una iniciativa importante para las organizaciones que desean garantizar la seguridad de sus activos de red.

[](#mainsection)[Principio de la página](#mainsection)

### Motivos para una ejecución más segura de los servicios

Si los servicios se ejecutan de forma más segura, se pueden obtener importantes ventajas empresariales. Con la mejora de la seguridad de los servicios, se podrá reducir con rapidez el tamaño del área de superficie de ataque de los equipos, mejorar la seguridad organizativa general y ayudar a proteger los datos confidenciales y críticos. Los equipos serán más estables y el tiempo de actividad del sistema mejorará. Se puede reducir la carga administrativa y, por lo tanto, el costo de propiedad de los servidores de la organización.

Esta guía le servirá de ayuda para evaluar la infraestructura actual de los servicios y tomar decisiones importantes en el planeamiento de futuras implementaciones.

[](#mainsection)[Principio de la página](#mainsection)

### Destinatarios de la guía

Esta guía se destina a consultores, expertos en seguridad, arquitectos de sistemas y profesionales de TI responsables de las fases de planeamiento del desarrollo de la aplicación o infraestructura, así como de la implementación de Windows Server 2003. Entre las descripciones de las tareas habituales para estas funciones, se encuentran:

-   Arquitectos y programadores responsables de las tareas en materia de arquitectura para los clientes de sus organizaciones.

-   Expertos en seguridad de TI que garanticen la seguridad en las distintas plataformas de sus organizaciones.

-   Arquitectos empresariales que administren toda la empresa y no sólo una red concreta.

-   Administradores de TI que determinen qué tecnología se debe emplear para resolver determinados problemas empresariales.

-   Analistas empresariales y responsables de la toma de decisiones que cuenten con requisitos y objetivos empresariales de vital importancia que dependen de la compatibilidad del cliente.

-   Consultores de socios y servicios de Microsoft que necesiten recursos detallados de información útil y relevante para socios y clientes empresariales.

Aunque se ha elaborado fundamentalmente para estas funciones, la *Guía de planeamiento de la seguridad de servicios y cuentas de servicios* también puede resultar útil para los generalistas de TI en organizaciones de mediano y gran tamaño, y las funciones de los equipos de infraestructura, operaciones y seguridad identificadas en el modelo de equipo de Microsoft Operations Framework (MOF).

[](#mainsection)[Principio de la página](#mainsection)

### Información general de la guía de planeamiento

Esta guía incluye los siguientes capítulos:

**Capítulo 1: Introducción**

En este capítulo se ofrece un resumen ejecutivo, se presentan las ventajas y desafíos empresariales, se sugieren los destinatarios recomendados de la guía y se brinda información general de los demás capítulos.

**Capítulo 2: Cómo mejorar la seguridad de la ejecución de servicios**

En este capítulo se facilita información general sobre los tipos de cuenta utilizados para iniciar sesión en los servicios y se describen los principios y estrategias que se aplican para que el programa ejecute los servicios de forma más segura.

**Capítulo 3: Ejecución más segura de servicios**

En este capítulo se describe la forma de ejecutar servicios de un modo más seguro con los principios y estrategias incluidos en el capítulo anterior. Asimismo, se analiza el nuevo Asistente para configuración de seguridad en Windows Server 2003 Service Pack 1, recurso indispensable en el plan de ejecución más segura de servicios.

**Capítulo 4: Resumen**

En este capítulo se resumen las instrucciones y los problemas analizados en esta guía. Incluye vínculos relacionados con importante material de lectura adicional.

[](#mainsection)[Principio de la página](#mainsection)

### Comuníquenos su opinión

Microsoft valora su opinión acerca de este material. Agradeceríamos en especial cualquier comentario relacionado con las preguntas siguientes:

-   ¿En qué medida ha resultado útil la información proporcionada?

-   ¿Fueron los procedimientos paso a paso precisos?

-   ¿Le resultaron los capítulos fáciles de leer e interesantes?

-   ¿Cómo calificaría esta solución en líneas generales?

Envíe sus comentarios a la siguiente dirección de correo electrónico: [cisfdbk@microsoft.com](mailto:cisfdbk@microsoft.com?subject=guía%20de%20planeamiento%20de%20la%20seguridad%20de%20servicios%20y%20cuentas%20de%20servicios)

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 1: Introducción

### Resumen ejecutivo

Esta guía constituye un importante recurso para planear estrategias de ejecución de servicios de forma segura con los sistemas operativos Microsoft® Windows Server™ 2003 y Windows® XP. Trata el problema habitual de los servicios de Windows establecidos para ejecutarse con los mayores privilegios posibles, que un atacante podría poner en peligro para obtener acceso completo y sin restricciones al equipo o dominio, o incluso a todo el bosque. Describe las formas de identificación de servicios que se pueden ejecutar con menores privilegios y explica cómo reducir dichos privilegios metódicamente. Esta guía le servirá de ayuda para evaluar la infraestructura actual de los servicios y tomar decisiones importantes en el planeamiento de futuras implementaciones.

Microsoft ya ha comprobado la ejecución de los servicios incluidos en los sistemas operativos Windows Server 2003 y Windows XP con las cuentas de inicio de sesión predeterminadas, con el fin de garantizar que se ejecutan con el nivel mínimo de privilegios posible y que resultan lo suficientemente seguros. Estos servicios no necesitan modificarse. El principal objeto de análisis de esta guía consiste en asegurar los servicios que no se proporcionan con el sistema operativo como, por ejemplo, los que se ofrecen como componente de otros productos del servidor de Microsoft: por ejemplo, Microsoft SQL Server™ o Microsoft Operations Manager. Los servicios instalados con aplicaciones de software de terceros y las aplicaciones de la línea de negocios desarrolladas de forma interna pueden requerir mejoras de seguridad adicionales.

El objetivo fundamental de esta guía es el de ayudar a los administradores a reducir el efecto de un servicio en situación de riesgo en un sistema operativo host. La guía se basa en la experiencia de Security Center of Excellence (SCoE) en entornos de clientes y representa las prácticas recomendadas de Microsoft.

#### Información general

Las organizaciones deben garantizar una ejecución segura de sus servicios. Si se dispone de directivas y prácticas adecuadas, los servicios no seguros se pueden proteger frente a los ataques. En estos ataques, se facilita acceso a nombres de usuario y contraseñas que el servicio emplea para la autenticación cuando se inicia o se conecta a otros equipos del dominio. En el peor de los casos, un usuario no autorizado puede obtener acceso de administrador de nivel de dominio.

Los servicios de Windows son programas ejecutables que funcionan en sesiones fuera de la sesión del usuario conectado actualmente. Su ejecución se produce en segundo plano, independiente de cualquier sesión de usuario. Los servicios pueden comenzar automáticamente cuando se inicie el equipo, se pueden detener y volver a iniciar y por sí mismos no muestran ninguna interfaz de usuario (IU), aunque se suelen comunicar con una de ellas para su control y administración. Debido a este comportamiento, los servicios resultan idóneos para utilizarse en un servidor o donde sea necesaria una funcionalidad a largo plazo que no interfiera con otros usuarios que se encuentren trabajando en el mismo equipo. Además de los servicios creados por Microsoft, muchos otros proveedores diseñan productos para que se implementen como servicios que se ejecutan continuamente en segundo plano.

La vulnerabilidad de seguridad de los servicios se origina en el modo en que las organizaciones han acostumbrado a implementarlos. Al igual que sucede con los usuarios, los servicios requieren un medio de autenticación para utilizar recursos de red o equipo. Antes del lanzamiento del sistema operativo Windows 2000, los servicios que tenían acceso a los recursos de una red debían utilizar una cuenta de usuario de dominio para autenticarse en cada servidor remoto que utilizaran, ya que la cuenta del sistema local no podía realizar la autenticación en la red. Con Windows 2000, la cuenta del sistema local se modificó para permitir la autenticación en los recursos de red, al igual que sucede con las cuentas de usuario de dominio, aunque en cambio se utilizan las credenciales del equipo para la autenticación. Una cuenta de equipo es esencialmente una cuenta de usuario que no dispone del atributo UserAccountControl, por lo que este tipo de cuentas puede iniciar sesión y tener acceso a los recursos del mismo modo que un usuario. Debido a estos cambios, la cuenta del sistema local pasó a ser una de las cuentas más habituales en la implementación de servicios. Con la aparición de Windows Server 2003, la situación volvió a cambiar cuando se agregaron dos nuevos tipos de cuenta integrada similar al sistema local: la cuenta Servicio de red y la cuenta Servicio local.

La nueva cuenta Servicio de red también utiliza las credenciales del equipo cuando se autentica de forma remota, aunque tiene un nivel de privilegio muy reducido en el propio servidor, por lo que no dispone de privilegios de administrador local. La cuenta Servicio local tiene los mismos privilegios reducidos que la cuenta Servicio de red, pero, como su propio nombre indica, no dispone de la capacidad de autenticar en los recursos de red.

La ejecución más segura de los servicios es una iniciativa importante para las organizaciones que desean garantizar la seguridad de sus activos de red.

#### Motivos para una ejecución más segura de los servicios

Si los servicios se ejecutan de forma más segura, se pueden obtener importantes ventajas empresariales. Con la mejora de la seguridad de los servicios, se podrá reducir con rapidez el tamaño del área de superficie de ataque de los equipos, mejorar la seguridad organizativa general y ayudar a proteger los datos confidenciales y críticos. Los equipos serán más estables y el tiempo de actividad del sistema mejorará. Se puede reducir la carga administrativa y, por lo tanto, el costo de propiedad de los servidores de la organización.

Esta guía le servirá de ayuda para evaluar la infraestructura actual de los servicios y tomar decisiones importantes en el planeamiento de futuras implementaciones.

#### Destinatarios de la guía

Esta guía se destina a consultores, expertos en seguridad, arquitectos de sistemas y profesionales de TI responsables de las fases de planeamiento del desarrollo de la aplicación o infraestructura, así como de la implementación de Windows Server 2003. Entre las descripciones de las tareas habituales para estas funciones, se encuentran:

-   Arquitectos y programadores responsables de las tareas en materia de arquitectura para los clientes de sus organizaciones.

-   Expertos en seguridad de TI que garanticen la seguridad en las distintas plataformas de sus organizaciones.

-   Arquitectos empresariales que administren toda la empresa y no sólo una red concreta.

-   Administradores de TI que determinen qué tecnología se debe emplear para resolver determinados problemas empresariales.

-   Analistas empresariales y responsables de la toma de decisiones que cuenten con requisitos y objetivos empresariales de vital importancia que dependen de la compatibilidad del cliente.

-   Consultores de socios y servicios de Microsoft que necesiten recursos detallados de información útil y relevante para socios y clientes empresariales.

Aunque se ha elaborado fundamentalmente para estas funciones, la *Guía de planeamiento de la seguridad de servicios y cuentas de servicios* también puede resultar útil para los generalistas de TI en organizaciones de mediano y gran tamaño, y las funciones de los equipos de infraestructura, operaciones y seguridad identificadas en el modelo de equipo de Microsoft Operations Framework (MOF).

#### Información general de la guía de planeamiento

Esta guía incluye los siguientes capítulos:

**Capítulo 1: Introducción**

En este capítulo se ofrece un resumen ejecutivo, se presentan las ventajas y desafíos empresariales, se sugieren los destinatarios recomendados de la guía y se brinda información general de los demás capítulos.

**Capítulo 2: Cómo mejorar la seguridad de la ejecución de servicios**

En este capítulo se facilita información general sobre los tipos de cuenta utilizados para iniciar sesión en los servicios y se describen los principios y estrategias que se aplican para que el programa ejecute los servicios de forma más segura.

**Capítulo 3: Ejecución más segura de servicios**

En este capítulo se describe la forma de ejecutar servicios de un modo más seguro con los principios y estrategias incluidos en el capítulo anterior. Asimismo, se analiza el nuevo Asistente para configuración de seguridad en Windows Server 2003 Service Pack 1, recurso indispensable en el plan de ejecución más segura de servicios.

**Capítulo 4: Resumen**

En este capítulo se resumen las instrucciones y los problemas analizados en esta guía. Incluye vínculos relacionados con importante material de lectura adicional.

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 2: Cómo mejorar la seguridad de la ejecución de servicios

En este capítulo se proporciona información sobre los riesgos inherentes a la ejecución de servicios y se analizan los tipos de cuenta utilizados para este fin. Asimismo, se describen los principios y estrategias que se deben aplicar cuando se planea ejecutar servicios con más seguridad.

[](#puol)[Vulnerabilidades del servicio](#puol)
[](#wnkl)[Cuentas del sistema](#wnkl)
[](#pvcx)[Cuentas de usuario](#pvcx)
[](#trnm)[Cambios en la configuración de seguridad predeterminada de los servicios en Windows Server 2003](#trnm)
[](#oulk)[Principios para mejorar la seguridad de la ejecución de servicios](#oulk)
### Vulnerabilidades del servicio

Debido a que los servicios se ejecutan sin vigilancia cuando se inician, resultan muy adecuados en aplicaciones de tipo servidor como, por ejemplo, servicios Web. No obstante, esta característica presenta inconvenientes, ya que el usuario puede ignorar que se esté ejecutando un servicio. Aunque puede que algunos servicios abran una ventana o cuadro de diálogo visible para el usuario, no suele existir casi interacción alguna con ellos, por lo que un usuario puede ejecutar una serie de servicios predeterminados y no conocer nunca los riesgos potenciales de seguridad. Gusanos de Internet recientes, como Nimda, se aprovechan de que el usuario puede ejecutar servicios Web de forma inconsciente en las estaciones de trabajo, las cuales, una vez infectadas, propagan el gusano a miles de equipos a través de Internet.

Algunos servicios, concretamente los que utilizan las herramientas de administración empresariales como Microsoft® Systems Management Server, Microsoft Operations Manager y Tivoli, necesitan iniciar sesión con una cuenta de usuario de dominio, ya que suelen requerir acceso a todo el dominio y posiblemente también a otros dominios de confianza. En otras situaciones, el uso de una cuenta de usuario de dominio para ejecutar servicios constituía una práctica estándar, pero recientemente las organizaciones han reconocido que supone un riesgo para la seguridad.

La información de nombre de usuario y contraseña de cada servicio que utiliza una cuenta de usuario local o de dominio se almacena en el registro, lo que puede ser objetivo de un atacante si éste obtiene acceso administrativo al equipo. Como resultado, se produce exposición de la seguridad si se configura un servicio para iniciar sesión como usuario.

Debido a que la exposición de la seguridad se crea siempre que un servicio se configura para iniciar sesión como cuenta de usuario de dominio, la posibilidad de aprovechar esta vulnerabilidad aumenta en función de varios factores, entre los que se encuentran:

-   **Número de servidores en los que se configura una cuenta de usuario de dominio determinada para ejecutar servicios**. En un entorno de servidor bien administrado, todos los servidores deben ser igualmente seguros. Si una organización no garantiza la seguridad de todos sus servidores por igual, el riesgo aumentará con cada servidor poco protegido. Cuantos más servidores haya en los que se ejecute el servicio con autenticación de dominio, más posibilidades habrá de que alguien aproveche la vulnerabilidad de la seguridad. Por ejemplo, puede que un servicio utilice la misma cuenta de dominio para autenticarse a sí mismo en cientos o miles de servidores de una organización. Por lo tanto, si un atacante pone en peligro uno de estos servidores y se apropia del nombre de usuario y contraseña del servicio, dicho atacante puede obtener acceso a los demás servidores que lo ejecuten.

-   **Ámbito de privilegios de red para cualquier cuenta de usuario de dominio configurada para ejecutar un servicio**. Cuanto más extenso sea el ámbito de privilegio, mayor será el número de recursos en situación de riesgo. Las cuentas de administrador de dominio suponen un alto riesgo, ya que el ámbito de vulnerabilidad en la red lo forman todos los equipos que residen en el dominio, incluyendo los controladores de dominio. Asimismo, si esta cuenta de usuario de dominio dispone de privilegios de administrador local en uno o varios servidores, existe la posibilidad de que se produzcan ataques continuos debido a la vulnerabilidad de seguridad.

    Resulta especialmente importante la protección de los recursos de red a los que tienen acceso las cuentas de nivel de administrador, ya que las credenciales del administrador de dominio crean vulnerabilidades transitivas y oportunidades de elevaciones en el dominio. Estas credenciales se suelen utilizar para inicios de sesión remotos o interactivos en todos los equipos del dominio; por lo tanto, cuando las credenciales se ponen en peligro, todos los equipos se encuentran vulnerables frente al ataque.

#### Escenarios de vulnerabilidad del servicio

Existen varios ejemplos distintos, cada uno de ellos con diferentes niveles de riesgo de seguridad. Éstos se describen en la siguiente figura y en la tabla que se muestra a continuación. Se asume que todas las cuentas de la figura son cuentas de dominio. Cada cuenta ejecuta al menos un servicio en uno de los servidores.

Descripciones de las cuentas de dominio en el diagrama:

-   La cuenta A dispone de privilegios equivalentes a los de administrador en varios controladores de dominio.

-   Las cuentas A, B, C y D tienen privilegios equivalentes a los de administrador en varios servidores miembros.

-   La cuenta E dispone de privilegios equivalentes a los de administrador en un único servidor miembro.

    [![](images/Cc170953.APGFG0201(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc170953.apgfg0201_big(es-es,technet.10).gif)

    **Figura 2.1 Privilegios de cuenta de administrador en servidores y controladores de dominio**

##### Prioridades en la vulnerabilidad de seguridad

Los niveles de prioridad utilizados en la siguiente tabla son:

-   **Nivel de riesgo máximo**. El escenario planteado pone inmediatamente en peligro la seguridad corporativa.

-   **Nivel de riesgo elevado**. El escenario planteado arriesga la seguridad corporativa, aunque ésta no se pone en peligro de inmediato.

-   **Nivel de riesgo medio**. El escenario planteado reviste importancia, pero el peligro no implica un servidor de alta seguridad.

-   **Nivel de riesgo bajo**. Si se elimina el escenario, existe un mínimo efecto en los objetivos de seguridad.

En la siguiente tabla se incluye una descripción detallada de los escenarios de vulnerabilidad del servicio y sus posteriores niveles de prioridad de vulnerabilidad.

**Tabla 2.1: Escenarios de vulnerabilidad de seguridad**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Escenario</th>
<th style="border:1px solid black;" >Descripción</th>
<th style="border:1px solid black;" >Nivel de riesgo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>1</strong></td>
<td style="border:1px solid black;">La cuenta A ejecuta un servicio en el servidor 1. Una vez descubierta la contraseña de la cuenta A en el servidor 1, el usuario tiene acceso al controlador de dominio 1, que pasa a ser vulnerable. Se trata de un caso de prioridad <em>máxima</em>; no se deben utilizar cuentas de dominio con privilegios equivalentes a los de administrador en un controlador de dominio para ejecutar servicios en un servidor miembro.</td>
<td style="border:1px solid black;"><strong>Máximo</strong></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>2</strong></td>
<td style="border:1px solid black;">La cuenta B ejecuta un servicio en el servidor 2. Esta cuenta también tiene acceso al servidor 1, donde la cuenta A está ejecutando un servicio. Una vez que la contraseña de la cuenta B se descubre en el servidor 2, el usuario obtiene el mismo estado de inicio que en el escenario 1, por lo que el controlador de dominio 1 es vulnerable. Esta lógica se puede aplicar a la cuenta C que ejecuta un servicio en el servidor 3 que, a su vez, puede facilitar el acceso al servidor 2, donde la cuenta B está ejecutando un servicio, y así sucesivamente. Éste es un caso de prioridad <em>elevada</em>, no máxima, ya que, al resolver el problema del escenario 1, el problema del escenario 2 se limita únicamente a los servidores miembros.</td>
<td style="border:1px solid black;"><strong>Elevado</strong></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>3</strong></td>
<td style="border:1px solid black;">La cuenta D ejecuta un servicio en el servidor 4 o 5. Una vez descubierta la contraseña de la cuenta D en el servidor, el usuario tiene acceso a todos los servidores miembros en los que la cuenta D tiene privilegios. Se trata de un caso de prioridad <em>media</em> (no existe la naturaleza transitiva del escenario 2).</td>
<td style="border:1px solid black;"><strong>Medio</strong></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>4</strong></td>
<td style="border:1px solid black;">La cuenta E ejecuta un servicio en el servidor 5 y solamente tiene acceso a dicho servidor.</td>
<td style="border:1px solid black;"><strong>Bajo</strong></td>
</tr>
</tbody>
</table>
  
#### Resumen de las vulnerabilidades del servicio
  
Los servicios constituyen puntos de vulnerabilidad excelentes para los atacantes que desean obtener acceso al servidor local o a otros servidores de la red. Si no necesita utilizar un servicio determinado, se recomienda deshabilitarlo. De este modo, la superficie de ataque se puede reducir de forma rápida y sencilla, además de obtener ventajas adicionales de rendimiento al no ejecutar servicios innecesarios.
  
Para proteger un servicio correctamente, se deben conocer sus vulnerabilidades y reducir al mínimo la exposición del servicio a las mismas.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Cuentas del sistema
  
Un servicio debe iniciar sesión como cuenta para obtener acceso a los recursos y objetos del sistema operativo. Si se asigna una cuenta a un servicio que no dispone de los permisos adecuados para iniciar la sesión, el complemento Servicios para Microsoft Management Console (MMC) otorgará automáticamente a dicha cuenta el derecho de usuario para iniciar sesión como servicio en el equipo que se está administrando. Microsoft Windows Server™ 2003 incluye tres cuentas locales integradas que se utilizan como cuentas de inicio de sesión para diversos servicios del sistema:
  
-   **Cuenta del sistema local**
  
    Se trata de una cuenta local predefinida que puede iniciar un servicio y ofrecer el contexto de seguridad para el mismo. Es una cuenta eficaz con acceso total al equipo, incluyendo el servicio de directorio cuando se utiliza con servicios que se ejecutan en controladores de dominio. La cuenta actúa como cuenta del equipo host en la red y como tal tiene acceso a los recursos de red de igual modo que cualquier otra cuenta de dominio. En la red, esta cuenta aparece como DOMAIN\\&lt;*nombre del equipo*&gt;$. Si un servicio inicia la sesión utilizando la cuenta del sistema local en un controlador de dominio, dispone de acceso al sistema local en el propio controlador, el cual, si se pone en peligro, puede permitir que los usuarios malintencionados modifiquen cualquier información en el dominio deseado. Windows Server 2003 configura algunos servicios para que inicien la sesión como la cuenta del sistema local de forma predeterminada. El nombre real de la cuenta es NT AUTHORITY\\System y no dispone de ninguna contraseña que un administrador deba administrar.
  
-   **Cuenta Servicio local**
  
    Es una cuenta integrada especial con privilegios reducidos, similar a una cuenta de usuario local autenticado. Este acceso limitado ayuda a proteger el equipo si un atacante pone en peligro procesos o servicios individuales. Un servicio que se ejecuta como cuenta Servicio local tiene acceso a los recursos de red como sesión nula; es decir, utiliza credenciales anónimas. El nombre real de la cuenta es NT AUTHORITY\\LocalService y no dispone de ninguna contraseña que un administrador deba administrar.
  
-   **Cuenta Servicio de red**
  
    Es una cuenta integrada especial con privilegios reducidos, similar a una cuenta de usuario autenticado. Este acceso limitado ayuda a proteger el equipo si un atacante pone en peligro procesos o servicios individuales. Un servicio que se ejecuta como cuenta Servicio de red tiene acceso a los recursos de red que utilizan las credenciales de la cuenta del equipo del mismo modo que un servicio del sistema local. El nombre real de la cuenta es NT AUTHORITY\\NetworkService y no dispone de ninguna contraseña que un administrador deba administrar.
  
    **Importante:** Si se modifica la configuración predeterminada del servicio, puede que los servicios clave no se ejecuten correctamente. Se debe proceder con especial cuidado al cambiar los valores de **Tipo de inicio** e **Iniciar sesión como** de los servicios configurados para que se inicien automáticamente de forma predeterminada.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Cuentas de usuario
  
Las distintas categorías de cuentas de usuario pueden iniciar sesión como servicio. Cada categoría tiene propios privilegios y capacidades:
  
-   **Cuentas de usuario local**
  
    Esta categoría incluye las cuentas que se crean localmente en un equipo; por ejemplo, con la consola de administración Usuarios y grupos locales. Estas cuentas disponen de privilegios muy limitados en el equipo local a no ser que se les conceda específicamente privilegios mayores o se agreguen a grupos que ya los posean.
  
-   **Cuentas de administrador local**
  
    En esta categoría se incluye la cuenta integrada de administrador que se crea y utiliza al instalar por primera vez Windows Server 2003 o Microsoft Windows® XP en el equipo. Incluye cualquier otra cuenta de usuario que posteriormente se cree y se agregue al grupo de administradores integrado. Los miembros de este grupo disponen de acceso completo sin restricciones al equipo local.
  
-   **Cuentas de usuario de dominio**
  
    A esta categoría pertenecen las cuentas creadas en el dominio; por ejemplo, mediante el uso de la consola de administración Usuarios y equipos de Active Directory®. Estas cuentas disponen de privilegios limitados en el dominio a no ser que se les conceda específicamente privilegios mayores o se agreguen a grupos que ya los posean.
  
-   **Cuentas de administrador de dominio**
  
    Esta categoría incluye la cuenta de administrador de dominio integrada que se crea y utiliza al instalar por primera vez Active Directory. Incluye las cuentas de usuario que se creen y agreguen posteriormente al grupo de administradores local integrado o a los grupos de administradores de dominio o de organización. Los miembros de estos grupos tienen acceso completo sin restricciones al dominio y, en el caso del grupo de administradores de organización, a todo el bosque.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Cambios en la configuración de seguridad predeterminada de los servicios en Windows Server 2003
  
Con las versiones de Windows anteriores a Windows XP y Windows Server 2003, casi todos los servicios incluidos con el sistema operativo utilizaban la cuenta del sistema local de forma predeterminada. Los programas que se ejecutan en este contexto disponen de privilegios ilimitados en el equipo local, lo cual implica un riesgo obvio para la seguridad. Con la aparición de Windows Server 2003, los desarrolladores modificaron la configuración predeterminada para que el entorno resultara más seguro. Uno de estos cambios es que un menor número de servicios se ejecutan con la cuenta del sistema local de forma predeterminada. En lugar de utilizar esta cuenta, muchos servicios comunes utilizan la cuenta Servicio de red o Servicio local. Estas cuentas tienen un nivel de privilegios mucho más bajo que la cuenta del sistema local y, por lo tanto, representan una amenaza menor para la seguridad.
  
Diversos servicios aún inician la sesión como sistema local, incluyendo Actualizaciones automáticas, Examinador de equipos, Mensajero y el servicio Windows Installer. Otros no lo hacen. Por ejemplo, aunque el Servicio de alerta utilizaba la cuenta del sistema local en Windows 2000, emplea la cuenta Servicio local en Windows Server 2003. El Cliente DNS utilizaba la cuenta del sistema local en Windows 2000, pero usa la cuenta Servicio de red en Windows Server 2003. En la siguiente tabla se incluyen los servicios que ya no utilizan la cuenta del sistema local en Windows Server 2003 y se indica qué cuenta de servicio están empleando ahora.
  
**Precaución:** No intente cambiar las cuentas que los servicios incluidos en el sistema operativo Windows Server 2003 utilizan, ya que se pueden originar graves problemas y detener la correcta ejecución de servicios importantes. Por ejemplo, el servicio Cliente DNS utiliza la cuenta Servicio de red porque debe tener acceso a recursos de red tales como los servidores DNS. Este servicio no funciona con la cuenta Servicio local ni con ninguna otra que no se pueda autenticar en los recursos de red.
  
**Tabla 2.2: Nueva configuración de la cuenta de servicios en Windows Server 2003**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre del servicio</th>
<th style="border:1px solid black;" >Inicia la sesión como</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Servicio de alerta</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servicio de puerta de enlace de capa de aplicación</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Registro remoto</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Tarjeta inteligente</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Ayuda de NetBIOS sobre TCP/IP</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Telnet</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Sistema de alimentación ininterrumpida</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cliente Web</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Adquisición de imágenes de Windows (WIA)</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Horario de Windows</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servicio de Descubrimiento automático de proxy Web WinHTTP</td>
<td style="border:1px solid black;">Servicio local</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cliente DHCP</td>
<td style="border:1px solid black;">Servicio de red</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Coordinador de transacciones distribuidas</td>
<td style="border:1px solid black;">Servicio de red</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Cliente DNS</td>
<td style="border:1px solid black;">Servicio de red</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Registro de licencias</td>
<td style="border:1px solid black;">Servicio de red</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Registros y alertas de rendimiento</td>
<td style="border:1px solid black;">Servicio de red</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Localizador de llamadas a procedimiento remoto (RPC)</td>
<td style="border:1px solid black;">Servicio de red</td>
</tr>
</tbody>
</table>
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Principios para mejorar la seguridad de la ejecución de servicios
  
Para obtener la seguridad deseada, se debe comprender la naturaleza de los servicios disponibles en el entorno de red y establecer procedimientos con los que proteger el uso de los mismos. En esta sección se analizan tres principios esenciales que se deben seguir para planear una ejecución segura:
  
-   Conocimiento del sistema
  
-   Utilización del principio de privilegios mínimos
  
-   Aplicación del principio de servicios mínimos
  
Si estos principios se incorporan correctamente en los procedimientos de seguridad de TI, se podrá lograr un nivel adecuado de seguridad.
  
#### Conocimiento del sistema
  
Aunque la recomendación parece obvia, muchas organizaciones no conocen a fondo las funciones y servicios que se ejecutan en todos sus equipos.
  
Para saber si los equipos son seguros, se deben conocer los servicios que ejecutan, así como sus propiedades. Esta información es de vital importancia para mantener la seguridad de los servidores. Gracias a una tabla con los servicios que se ejecutan en los equipos y las propiedades de aquéllos, los riesgos se podrían evaluar de forma inmediata. La creación de una tabla de este tipo puede resultar en un principio un proceso largo y complejo, pero el esfuerzo bien merece la pena, ya que es de vital importancia comprender las propiedades de una *configuración válida* para las distintas funciones del servidor.
  
Existen varias herramientas que pueden ayudar a crear una lista de los servicios en ejecución y sus propiedades. Entre ellas, se incluyen:
  
-   **Controlador de servicios (sc.exe)**. Esta herramienta de línea de comandos se facilita con Windows Server 2003 y Windows XP. Proporciona una forma de comunicarse con el componente Administrador de control de servicios desde la línea de comandos para consultar y establecer las propiedades del servicio.
  
-   **Instrumental de administración de Windows (WMI)**. Se trata de un componente preinstalado de los sistemas operativos Windows Server 2003 y Windows XP que ofrece información de administración y control en un entorno empresarial. Con el uso de estándares de la industria, los administradores de sistemas pueden utilizar WMI para consultar y establecer información en los equipos de escritorio, aplicaciones, redes y otros componentes empresariales. Varias herramientas de administración son compatibles con WMI, entre las que se incluyen Información del sistema y el componente Dependencias de la consola Servicios. Las dependencias de los servicios identifican los servicios de los que depende el servicio actual y los servicios dependientes de éste. Los administradores del sistema también pueden utilizar secuencias de comandos de WMI para automatizar sus tareas.
  
-   **Línea de comandos del Instrumental de administración de Windows (WMI)**. WMI incluye una herramienta de línea de comandos, WMIC, que ofrece una interfaz sencilla para WMI con la que se puede consultar y administrar de forma remota los equipos que ejecutan sistemas operativos Windows. Para invocar WMIC, se escribe **wmic** en el símbolo del sistema. Por ejemplo, para recuperar información de los servicios de un servidor denominado Server1, escriba lo siguiente en el símbolo del sistema:
  
    **wmic /output:c:\\services.htm /node:server1 service list full / format:htable**
  
    Utilice Microsoft Internet Explorer para examinar el archivo resultante c:\\services.htm con formato de tabla HTML (lenguaje de marcado de hipertexto). Si el nombre del servidor contiene espacios o caracteres especiales, escríbalo entre comillas al ejecutar el comando **wmic**.
  
    **Nota:** Existe otra herramienta de línea de comandos, **sclist.exe**, incluida en el Kit de recursos de Windows 2000 Server. Esta herramienta puede mostrar los servicios que se ejecutan actualmente, los detenidos o todos los servicios de los equipos locales y remotos. Sclist.exe puede identificar servicios que se ejecutan en un equipo remoto físicamente, o bien, en un equipo que no dispone de monitor como, por ejemplo, un soporte de servidor.
  
#### Utilización del principio de privilegios mínimos
  
La mayor parte de la documentación y los cursos relacionados con la seguridad analizan la implementación del principio de privilegios mínimos. Aunque este principio es sencillo, el impacto de su implementación aumenta enormemente la seguridad y reduce el riesgo. Con el principio se plantea conceder a una entidad la cantidad mínima de acceso necesario para realizar únicamente su tarea. En Windows Server 2003, este principio se aplica tanto a las cuentas de usuario como a las de equipo, ya que en Active Directory ambas cuentas constituyen puntos principales de seguridad, lo que significa que se les puede asignar permisos y privilegios.
  
Una razón por la que este principio funciona tan bien es que obliga a evaluar los recursos de red y los riesgos potenciales de seguridad. Se deben conocer los privilegios de acceso que realmente son necesarios para un equipo o usuario determinado y, posteriormente, comprobar que solamente se apliquen dichos privilegios.
  
La ejecución más segura de servicios requiere que las organizaciones implementen servicios con un enfoque de privilegios mínimos. Siempre que sea posible, ejecute los servicios como la cuenta Servicio local, de modo que sólo se pueda obtener acceso a un único equipo y no a todo el dominio. Los servicios que requieren acceso de red con autenticación pueden necesitar utilizar la cuenta Servicio de red; asimismo, se deben implementar servicios que requieran una mayor implementación como cuenta del sistema local. Si se determina que es necesaria una cuenta de administrador de nivel de dominio para implementar un servicio, el servidor en el que se realice la implementación se debe tratar como un *servidor de alta seguridad* y se debe proteger con las mismas medidas utilizadas para otros recursos de red de gran importancia como, por ejemplo, controladores de dominio. Para obtener más información sobre este tema, consulte la sección Creación de un grupo de servidores de alta seguridad para excepciones de administrador de dominio del capítulo 3, "Ejecución más segura de servicios".
  
Microsoft ha realizado una comprobación exhaustiva de Windows Server 2003 para garantizar que los servicios principales del sistema operativo se ejecuten con la cuenta de menos privilegios; por lo tanto, generalmente no es necesario modificar estos servicios. El principal objetivo debe ser asegurar los servicios que no formen parte del sistema operativo como, por ejemplo, los que se proporcionan como componente de otras ofertas de productos de servidor; por ejemplo, Microsoft SQL Server™, Microsoft Operations Manager y servicios ofrecidos por otros fabricantes de software.
  
Se puede emplear Directiva de grupo de Windows Server 2003 para controlar servicios específicos que se pueden ejecutar en uno o varios equipos. Para ello, abra el objeto de directiva de grupo de la unidad organizativa que incluye el equipo que se desee configurar. Examine el nodo **Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Servicios del sistema** y abra la página **Propiedades** del servicio que desea controlar. En el cuadro de diálogo **Propiedades**, defina el modo de inicio del servicio (**Automático**, **Manual** o **Deshabilitado**) y establezca los permisos de seguridad que controlan qué cuentas de usuario pueden realizar operaciones concretas en el servicio como, por ejemplo, detención o inicio del servicio.
  
Para obtener más información sobre lo que hay que considerar al decidir qué tipo de cuenta se debe utilizar para la ejecución de un servicio, consulte la figura 3.1, "Jerarquía de privilegios mínimos para la implementación de servicios", del capítulo 3, "Ejecución más segura de servicios".
  
Cuando se implemente el principio de privilegios mínimos en los equipos, funcionará junto con la norma de *conocimiento del sistema*. ¿Cómo se sabe si los equipos ejecutan la cantidad mínima de servicios si no se conoce cuáles se están ejecutando realmente? Con la combinación de estos dos principios, el personal de administración puede evaluar qué servicios se ejecutan en un equipo, el estado de éstos y las credenciales que se emplean con cada servidor; a continuación, otorgue metódicamente a todos los servicios posibles el mínimo privilegio necesario. Supervise los equipos para garantizar que no se agregue ninguno nuevo sin realizar los procedimientos adecuados de control de cambios.
  
#### Aplicación del principio de servicios mínimos
  
Este principio indica que el sistema operativo y los protocolos de red disponibles en cualquier dispositivo en red deben ejecutar únicamente los servicios y protocolos justos que sean necesarios para cumplir el objetivo empresarial. Por ejemplo, si no se necesita que un servidor aloje ninguna aplicación Web, se debe eliminar o deshabilitar el servicio World Wide Web. La mayoría de los sistemas operativos y programas instalan muchos más servicios y protocolos en su configuración predeterminada de los que realmente son necesarios para situaciones de uso normal.
  
El mejor modo de configurar un nuevo servidor es incluir un paso en el que el administrador del sistema cierre todas las necesidades del sistema operativo menos las imprescindibles. Por ejemplo, en los sistemas operativos Windows antes de Windows Server 2003, era una práctica habitual cerrar el Servicio de alerta y Mensajero. Asimismo, compruebe la correcta situación de los servicios en la red. Por ejemplo, el servicio Enrutamiento y acceso remoto o los Servicios de Internet Information Server (IIS) no se deben situar en un controlador de dominio, ya que ejecutan servicios en segundo plano que pueden aumentar la vulnerabilidad del controlador. Microsoft recomienda que no se ejecute ningún servicio adicional en el controlador de dominio, excepto los necesarios para que opere correctamente como tal.
  
Para obtener más información sobre la seguridad de los servicios en Windows Server 2003 y Windows XP, consulte las siguientes guías:
  
-   [*Guía de seguridad de Windows Server 2003*](http://go.microsoft.com/fwlink/?linkid=14845) en http://go.microsoft.com/fwlink/?linkid=14845
  
-   [*Guía de seguridad de Windows XP*](http://go.microsoft.com/fwlink/?linkid=14839) en http://go.microsoft.com/fwlink/?LinkId=14839
  
-   [*Introducción a las amenazas y contramedidas: Configuración de la seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15159) en http://go.microsoft.com/fwlink/?linkid=15159
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 3: Ejecución más segura de servicios
  
En este capítulo se describen las tareas que se deben llevar a cabo al planear una ejecución más segura de los servicios, a través de los enfoques y principios que se han abordado en los capítulos anteriores.
  
Para proteger los servicios, se deben realizar las siguientes tareas:
  
-   Auditar todos los servidores para determinar las propiedades fundamentales de los servicios.
  
-   Determinar qué servicios se deben ejecutar.
  
-   Identificar y eliminar todas las cuentas de administrador de dominio para los servicios.
  
-   Utilizar una jerarquía de privilegios mínimos para la implementación de servicios.
  
-   Crear un grupo de servidores de alta seguridad para las excepciones de administrador de dominio.
  
-   Administrar los cambios de las contraseñas de cuentas de servicios.
  
-   Utilizar contraseñas seguras.
  
-   Automatizar las pruebas de contraseñas de administrador poco seguras.
  
[](#zhaa)[Auditoría de todos los servidores para determinar propiedades fundamentales de los servicios](#zhaa)  
[](#ygaa)[Determinación de los servicios necesarios](#ygaa)  
[](#xfaa)[Identificación y eliminación de todas las cuentas de administrador de dominio para los servicios](#xfaa)  
[](#veaa)[Uso de una jerarquía de privilegios mínimos para implementar servicios](#veaa)  
[](#wdaa)[Creación de un grupo de servidores de alta seguridad para excepciones de administrador de dominio](#wdaa)  
[](#mcaa)[Administración de cambios de contraseñas de cuentas de servicios](#mcaa)  
[](#nbaa)[Uso de contraseñas seguras](#nbaa)  
[](#oaaa)[Comprobación automática de contraseñas de administrador poco seguras](#oaaa)  
### Auditoría de todos los servidores para determinar propiedades fundamentales de los servicios
  
Se debe determinar la cantidad exacta de servidores existentes en la organización. Aunque esta tarea parezca sencilla, para una organización de gran tamaño puede resultar sorprendentemente complicado identificar todos los servidores que posee y determinar el nivel de administración que requieren los servicios de cada equipo. Por ejemplo, los equipos que pertenecen a la red perimetral necesitan unos niveles de administración de servicios considerablemente más altos para reducir la superficie de ataque.
  
Se recomienda auditar cada servidor para elaborar una lista de todos los servicios en ejecución y registrar las credenciales de inicio de sesión que cada uno utiliza para la autenticación. Para llevar a cabo esta tarea, se pueden utilizar las siguientes herramientas:
  
-   **Información del sistema de Microsoft® Windows Server™ 2003**. Con esta herramienta, se puede ver una lista completa de las propiedades de todos los servicios del equipo local o de otros equipos remotos. Sin embargo, este método no es escalable a aquellas situaciones en las que se deba auditar una gran cantidad de servidores. Para obtener acceso a esta herramienta, haga clic en **Inicio**, elija **Todos los programas**, **Accesorios**, **Herramientas del sistema** y, a continuación, haga clic en **Información del sistema**.
  
-   **Consola de administración de servicios**. En la consola de administración de servicios, se puede utilizar la ficha **Iniciar sesión** de la página de propiedades de un servicio para buscar la cuenta que utiliza el servicio para iniciar sesión con el fin de realizar la autenticación. También se puede utilizar la ficha **Dependencias** para ver los servicios de los que depende el servicio actual y los servicios dependientes de éste. Los datos sobre las dependencias son una información fundamental que se debe recabar cuando se auditan los servidores. Sin embargo, este método no es escalable a aquellas situaciones en las que se deba auditar una gran cantidad de servidores.
  
-   **Instrumental de administración de Windows (WMI)**.** Utilice WMI para obtener información sobre los servicios que se ejecutan en todos los servidores. Se puede utilizar WMI con herramientas de programación o utilidades de secuencias de comandos, tales como Windows Scripting Host, para recuperar información detallada sobre la configuración de la mayoría de los aspectos de los equipos o para realizar cambios en los mismos. Existen diversas herramientas de administración habilitadas para WMI, tales como Propiedades del sistema, Información del sistema y el componente Dependencias de los servicios. Las dependencias de los servicios identifican los servicios de los que depende el servicio actual y los servicios dependientes de éste.
  
-   **Línea de comandos de Instrumental de administración de Windows (WMIC)**.** Con WMIC, se facilita una sencilla herramienta de interfaz de línea de comandos para WMI que permite administrar equipos remotos que utilicen sistemas operativos Windows. WMIC interopera con los comandos de shell y de utilidades, y se puede ampliar fácilmente con secuencias de comandos u otras aplicaciones orientadas a la administración.
  
    Por ejemplo, puede utilizar el comando **wmic service get** para obtener información sobre todas las propiedades de un servicio específico, entre las que se incluyen:
  
    -   Description
  
    -   DisplayName
  
    -   ErrorControl
  
    -   InstallDate
  
    -   PathName
  
    -   ProcessId
  
    -   StartMode
  
    -   StartName
  
    -   Status
  
    Ejemplo de sintaxis:
  
    **Nota:** Algunas partes del siguiente fragmento de código se muestran en varias líneas sólo para facilitar la lectura, pero se deben escribir en una única línea.
  
    ```  
 SERVICE GET Name,DisplayName,ProcessId,Started, StartMode,StartName  
```
  
    El comando **wmic service list brief** se puede utilizar para recuperar una lista de propiedades básicas de todos los servicios instalados de la siguiente forma:
  
    -   ExitCode
  
    -   Name
  
    -   ProcessId
  
    -   StartMode
  
    -   State
  
    -   Status
  
    Puede utilizar WMIC desde cualquier equipo que lo tenga instalado para administrar un equipo remoto que ejecute WMI. No es necesario que el equipo de destino tenga WMIC instalado o en ejecución para que WMIC lo pueda administrar de forma remota. Para administrar un equipo de forma remota, deberá utilizar el comando **/node:**&lt;*nombreEquipo&gt;*, el cual solicita el equipo que se debe agregar a la lista de nodos desde la que desea recuperar la información.
  
    Ejemplo de sintaxis:
  
    **Nota:** Algunas partes del siguiente fragmento de código se muestran en varias líneas sólo para facilitar la lectura, pero se deben escribir en una única línea.
  
    ```  
 WMIC /NODE:Server1,Server2,Server3 SERVICE GET Name,DisplayName,ProcessId,Started,StartMode, SystemName  
```
  
    También se puede proporcionar la ubicación de un archivo de texto que contenga una lista de los equipos remotos en los que se desea utilizar WMIC para llevar a cabo acciones.
  
    Ejemplo de sintaxis:
  
    ```  
 WMIC /NODE:@"C:\\MyServerList.txt" SERVICE LIST BRIEF  
```
  
    Puede usar WMIC para facilitar las tareas en las siguientes situaciones típicas:
  
    -   **Administración local de un equipo**. Está en un equipo y utiliza el comando WMIC para administrarlo.
  
    -   **Administración remota de un equipo**. Está en un equipo y utiliza WMIC para administrar otro.
  
    -   **Administración remota de varios equipos**. Está en un equipo y utiliza WMIC para administrar varios equipos con un único comando.
  
    -   **Administración remota de un equipo con una sesión remota**. Utiliza tecnologías de sesión remota, como Telnet o Servicios de Terminal Server, para conectarse con un equipo remoto y administrarlo con WMIC.
  
-   **Administración automatizada mediante secuencia de comandos administrativa**.** Con WMIC, se puede escribir una secuencia de comandos de administración sencilla para automatizar la administración de un equipo (local, remota o de varios equipos, tanto en serie como de forma simultánea).
  
    Si desea obtener más información sobre WMI, consulte el tema [WMI: Introducción al Instrumental de administración de Windows](http://technet.microsoft.com/es-es/library/cc736575.aspx) en http://www.microsoft.com/technet/prodtechnol/windowsserver2003/es/library/ServerHelp/03d4cfdf-bc6b-41cd-8154-462cf51e8c70.mspx  
    y la página [Introducción al Instrumental de administración de Windows](http://technet.microsoft.com/es-es/library/cc736575.aspx) en http://www.microsoft.com/windows2000/es/advanced/help/default.asp?url=/windows2000/es/advanced/  
    help/windows\_wmi\_overview.htm.
  
-   **Otras herramientas de administración empresarial**. Existen otras herramientas de administración disponibles para facilitar las auditorías, entre las que se incluyen:
  
    -   Microsoft Systems Management Server
  
    -   Tivoli
  
    -   OpenView
  
    -   Service Account Manager de Lieberman Software
  
La creación de una lista general de los servidores y sus servicios ayuda a identificar y solucionar riesgos en la seguridad relacionados con los servicios.
  
Puede emplear la auditoría para crear inventarios de todos los servicios que utilizan:
  
-   Una cuenta de usuario de dominio con privilegios de administrador de dominio.
  
-   Una única cuenta de usuario de dominio usada en más de un servidor.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Determinación de los servicios necesarios
  
La primera vez que se instala Windows Server 2003, este sistema operativo crea varios servicios predeterminados y los configura para que se ejecuten cuando se inicie el equipo. El libro de Microsoft Excel sobre configuración de la seguridad y los servicios predeterminados de Windows, que se incluye en la guía [*Introducción a las amenazas y contramedidas: Configuración de la seguridad en Windows Server 2003 y Windows XP*](http://www.microsoft.com/spain/technet/recursos/articulos/secmod48.mspx), documenta la configuración predeterminada del tipo de inicio de todos los servicios del sistema.
  
Estos servicios predeterminados proporcionan compatibilidad con el cliente o las aplicaciones, o facilitan la administración de sistemas. Sin embargo, probablemente no se necesitan todos estos servicios en el entorno de la organización, por lo que se deberá evaluar detenidamente cuáles se requieren.
  
Definir los servicios que son necesarios y los que se deben deshabilitar puede resultar un proceso complicado. Existen algunos que obviamente se deben desactivar, pero la decisión de desactivar otros no resulta tan evidente. La estrategia básica que se debe seguir es la siguiente:
  
-   Si no existe un motivo específico para utilizar un determinado servicio, deshabilítelo.
  
-   Si cree que podría necesitar el servicio en el futuro, deshabilítelo hasta que lo necesite.
  
Los servicios que se necesitan ejecutar en un equipo dependen en gran medida de la función que desempeña dicho equipo. Por ejemplo, sólo se debe instalar Servicios de Internet Information Server (IIS) en un servidor Web o en un equipo que lo requiera como, por ejemplo, un servidor de aplicaciones. Si el servidor no aloja servicios de acceso remoto o sesiones Telnet, se recomienda deshabilitar o quitar estos servicios. Existen varias situaciones en las que software como, por ejemplo, las herramientas de administración de sistemas, agregan sus propios servicios a los que ya se ejecutan en los equipos. Es importante que conozca estos servicios, las cuentas que utilizan para iniciar sesión y el nivel de acceso que requieren.
  
Microsoft ha publicado varias guías sobre cómo proteger los equipos según las funciones que desempeñen. En estas guías se explica qué servicios se requieren para determinadas funciones como, por ejemplo, controladores de dominio, servidores Web, clientes Windows XP, etc. Están disponibles en las siguientes direcciones:
  
-   [*Guía de seguridad de Windows Server 2003*](http://go.microsoft.com/fwlink/?linkid=14845) en http://go.microsoft.com/fwlink/?linkid=14845
  
-   [*Guía de seguridad de Windows XP*](http://go.microsoft.com/fwlink/?linkid=14839) en http://go.microsoft.com/  
    fwlink/?LinkId=14839
  
-   [*Guía de consolidación de seguridad de Windows 2000*](http://go.microsoft.com/fwlink/?linkid=22380) en http://go.microsoft.com/fwlink/?LinkID=22380 (en inglés)
  
-   [*Introducción al servicio y requisitos del puerto de red para el sistema Windows Server*](http://support.microsoft.com/default.aspx?scid=kb;es;832017) en http://support.microsoft.com/default.aspx?scid=kb;es;832017
  
En un entorno de prueba o preproducción, a fin de determinar si se requiere un servicio, se puede desactivar y, a continuación, controlar el equipo durante un tiempo para comprobar si algo no funciona correctamente. No obstante, hay que tener en cuenta que la consola Servicios no permitirá detener algunos servicios principales ni modificar el tipo de inicio de éstos. Entre estos servicios, se encuentran Llamada a procedimiento remoto (RPC) y Plug and Play. Además, existen algunos servicios que la consola Servicios no le permitirá detener, aunque sí le dejará cambiar el tipo de inicio de los mismos, como, por ejemplo, los servicios Registro de sucesos y Administrador de cuentas de seguridad.
  
Si no está seguro de qué función específica realiza un servicio, utilice uno o varios de los siguientes métodos para obtener más información:
  
-   Consulte las descripciones de servicios más detalladas en el capítulo 7, "Servicios del sistema", de la guía [*Introducción a las amenazas y contramedidas: Configuración de la seguridad en Windows Server 2003 y Windows XP*](http://go.microsoft.com/fwlink/?linkid=15160), que se puede descargar en http://go.microsoft.com/fwlink/?LinkId=15160.
  
-   Lea la descripción del servicio. Para obtener acceso a ella, abra la consola Servicios, busque el servicio que desea, haga clic con el botón secundario del *mouse* (ratón) en el nombre del mismo y, a continuación, seleccione **Propiedades**.
  
-   Utilice el Asistente para configuración de seguridad para obtener una descripción del servicio.
  
Este asistente, que se ofrece con Windows Server 2003 Service Pack 1 (SP1), puede resultar de gran ayuda para analizar qué servicios se necesita ejecutar.
  
#### Reducción de la superficie de ataque con el Asistente para configuración de seguridad
  
El Asistente para configuración de seguridad (SCW) permite configurar fácil y rápidamente los servidores que ejecutan Microsoft Windows según los requisitos funcionales de la organización (servidor Web, controlador de dominio u otro), durante la creación de directivas de seguridad para minimizar la vulnerabilidad frente a ataques. Para instalar SCW, abra el Panel de control, haga doble clic en **Agregar o quitar programas**, seleccione **Agregar o quitar componentes de Windows**, en la página **Componentes de Windows**, bajo **Componentes**, active la casilla de verificación **Asistente para configuración de seguridad** y haga clic en **Siguiente**. Cuando se haya completado el asistente, haga clic en **Finalizar**. A través de este proceso, se agrega un acceso directo al asistente en la carpeta Herramientas administrativas.
  
Con el Asistente para configuración de seguridad, se pueden descubrir los servicios que los servidores de la organización están ejecutando y la dependencia de ellos respecto a otros servicios. También puede resultar de utilidad para determinar qué servicios son necesarios cuando se implementan nuevos servidores. Puede implementar directivas generadas por SCW a través de Directiva de grupo, lo cual permite implementar funciones de servidor específicas en varios equipos similares al mismo tiempo dentro de una unidad organizativa (UO) o una jerarquía de unidades organizativas.
  
El término *función de servidor* define las funciones principales que un equipo lleva a cabo en una organización, como, por ejemplo: servidor de archivos, controlador de dominio y servidor Web. Puesto que los servicios necesarios, los puertos de entrada y la configuración varían con cada función, las directivas de SCW que se creen deben coincidir con la función que se desee que cada equipo realice.
  
Puede utilizar SCW para reducir la superficie de ataque de los equipos que utilicen Windows Server 2003 con SP1. El asistente le guía a través del proceso de creación de una directiva de seguridad basada en las funciones que realiza un determinado servidor. Una vez creada la directiva, se puede aplicar a uno o varios servidores con una configuración similar.
  
SCW se compone de las siguientes secciones:
  
-   Configuración de servicio basado en funciones
  
-   Seguridad de red
  
-   Configuración de Registro
  
-   Directiva de auditoría
  
-   Servicios de Internet Information Server (sólo visibles cuando está seleccionada la función Servidor Web)
  
La única sección del asistente relevante para la finalidad de esta guía es Configuración de servicio basado en funciones. Esta parte del asistente se utiliza para configurar servicios según las funciones del servidor seleccionado y otras características.
  
La directiva de seguridad se crea según las funciones instaladas en el servidor seleccionado. Se puede aplicar la directiva al servidor seleccionado o utilizarlo para crear la directiva y, a continuación, aplicarla a un grupo de servidores que tengan funciones similares.
  
#### Funcionamiento del Asistente para configuración de seguridad
  
Para reducir la superficie de ataque de los servidores que utilizan Windows, SCW realiza una serie de preguntas al usuario con el fin de determinar los requisitos funcionales de un servidor. A continuación, deshabilita la funcionalidad que no sea necesaria para las funciones realizadas por el servidor. Además de suponer una recomendación de seguridad fundamental, la reducción de la superficie de ataque aumenta la diversidad del entorno Windows y disminuye el número de equipos que se deben actualizar inmediatamente cuando se exponen las vulnerabilidades.
  
Con SCW se responden las preguntas más frecuentes sobre Windows Server 2003: ¿Qué servicios se pueden desactivar?
  
Hasta la fecha, ha sido difícil responder a esta pregunta debido a los millares de posibles combinaciones de tecnologías instaladas, cada una con una jerarquía de dependencias que pueden existir en cualquier equipo basado en Windows. Cuando se agregan otros servidores, como Microsoft Exchange Server o SQL Server™, las dependencias cambian de nuevo. SCW soluciona este problema y ofrece a los administradores una forma de configurar los servidores para que ejecuten únicamente los servicios que se requieran según las funciones asignadas a dicho servidor. Para ello, SCW obtiene acceso a una base de datos XML (lenguaje de marcado extensible) que contiene los datos necesarios sobre Windows Server 2003 y los productos de Microsoft que se ejecutan en Windows Server 2003.
  
#### Ventajas del Asistente para configuración de seguridad
  
Cuando se utiliza SCW para elegir las funciones, automáticamente sucede lo siguiente:
  
-   Se deshabilitan los servicios innecesarios.
  
-   Se deshabilitan las extensiones Web de IIS innecesarias.
  
-   Se bloquean los puertos que no se utilizan.
  
#### Ventajas del Asistente para configuración de seguridad
  
Aunque SCW no bloquea configuraciones de seguridad tales como el nivel de autenticación LM y la firma de bloques de mensajes de servidor (SMB), en las guías de seguridad de Windows Server 2003 y Windows XP mencionadas anteriormente en esta sección se abordan estas configuraciones y se ofrecen recomendaciones.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Identificación y eliminación de todas las cuentas de administrador de dominio para los servicios
  
Con la información de la auditoría del servidor, puede identificar y eliminar todas las posibles cuentas de administrador de dominio utilizadas para los servicios. La eliminación de todas las instancias posibles de servicios que utilicen cuentas de administrador de dominio representa un primer paso importante para la seguridad de los servicios. Siempre que sea posible, se recomienda volver a implementar los servicios a través de las cuentas Servicio local, Servicio de red o de sistema local, como se describe en la siguiente sección de este capítulo.
  
Las organizaciones deben intentar eliminar las implementaciones de servicios que incluyan:
  
-   Cuentas de usuario con privilegios equivalentes a los de administrador que inicien sesión como un servicio.
  
-   Cuentas de administrador integradas que inicien sesión como un servicio.
  
-   Cuentas de administrador de dominio que inicien sesión como un servicio en servidores de baja seguridad.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Uso de una jerarquía de privilegios mínimos para implementar servicios
  
Para ejecutar un servicio, se recomienda utilizar la cuenta que tiene los privilegios mínimos. Los servicios implementados con cuentas que tienen privilegios mayores se deben volver a implementar con cuentas que tengan menos privilegios.
  
Una jerarquía de privilegios mínimos debe utilizar las cuentas según el orden siguiente:
  
1.  **Servicio local**. Esta cuenta es similar a la de sistema local, aunque tiene privilegios mínimos en el equipo local. Los servicios que inician sesión como servicio local tienen acceso a los recursos de red como una sesión nula con credenciales anónimas. Los privilegios de la cuenta se deben limitar únicamente a los necesarios para el correcto funcionamiento del servicio.
  
2.  **Servicio de red**. Esta cuenta es similar a la de sistema local, aunque tiene privilegios mínimos en el equipo local. Los servicios que inician sesión como servicio de red tienen acceso a los recursos de red a través de las credenciales de la cuenta del equipo (al que se hace referencia como &lt;*nombre\_dominio\\nombre\_equipo*&gt;$). Los privilegios de la cuenta se deben limitar únicamente a los necesarios para el correcto funcionamiento del servicio.
  
3.  **Cuenta de usuario única**. Un servicio se debe ejecutar como una cuenta de usuario única si no resulta práctico ejecutarla como un servicio local o de red. Se recomienda utilizar una cuenta de usuario local única para ejecutar servicios que sólo requieren privilegios en el equipo local, tales como IIS y SQL Server. Sin embargo, las aplicaciones que se deben ejecutar en equipos distribuidos, como ocurre con aplicaciones distribuidas como Systems Management Server y Microsoft Operations Manager, deberán utilizar una cuenta de usuario de dominio única. También se necesitará este tipo de cuenta para cualquier aplicación que requiera tener acceso a recursos de red. Se debe utilizar una cuenta de usuario de dominio única independiente con cada aplicación que la necesite. Por ejemplo, si ejecuta varias aplicaciones ASP.NET, se deberá asegurar de que todas las aplicaciones utilizan su propia cuenta de usuario única. Los privilegios de la cuenta de usuario única se deben limitar exclusivamente a los necesarios para el correcto funcionamiento del servicio. Puede asignar otros privilegios administrativos a la cuenta única para la que se ha configurado el servicio, pero sólo si fuera necesario. También se debe restringir la pertenencia a grupos de la cuenta única a los grupos que se requieran. Estas cuentas deben cumplir una directiva organizativa para el uso de contraseñas seguras. Si varios equipos utilizan el mismo servicio o servicios relacionados, las contraseñas de cada cuenta de usuario única deben ser también únicas.
  
4.  **Sistema local**. Tenga en cuenta que los servicios que inician sesión como sistema local tienen amplios privilegios en el equipo local y presentan credenciales de equipo en la red (a las que se hace referencia como &lt;*nombre\_dominio\\nombre\_equipo*&gt;$). Los privilegios de la cuenta se deben limitar únicamente a los necesarios para el correcto funcionamiento del servicio.
  
5.  **Cuenta de administrador local**. Se recomienda ejecutar un servicio como una cuenta de administrador local sólo si no resultara práctico ejecutarla como servicio local, servicio de red, como cuenta de usuario de dominio única o como cuenta de sistema local. Para disminuir el nivel de un servicio que se ejecuta como administrador local, se puede utilizar una cuenta de usuario local y agregar los privilegios específicos que se requieran o cambiar las entradas en la lista de control de acceso al sistema (SACL). Resulta mucho más recomendable utilizar uno de estos enfoques en lugar de ejecutar como administrador en el equipo un servicio de terceros que tenga vulnerabilidades no conocidas. Asimismo, debe dar a conocer a sus proveedores de software la importancia de disponer de unos servicios de privilegios mínimos en el entorno. Para ello, déjeles desempeñar un papel fundamental en los procesos de evaluación y compra. Además, los proveedores de software deben hacer algo para evitar que se ejecute el servicio que proporcionan como cuenta de administrador. Se debe asesorar al proveedor sobre los recursos a los que el servicio realmente necesita tener acceso y sobre los niveles de permisos que requiere. Se deben asignar privilegios de administrador local en la cuenta exclusivamente al equipo en el que está configurado el servicio y sólo si resultara necesario. Esta cuenta debe cumplir una directiva organizativa para el uso de contraseñas seguras. Si varios equipos utilizan el mismo servicio o servicios relacionados, las contraseñas de cada cuenta de administrador local deben ser también únicas.
  
6.  **Cuenta de administrador de dominio**. La ejecución de un servicio con una cuenta de administrador de dominio constituye un ejemplo de seguridad pésima. Las organizaciones deben eliminar tales situaciones. De utilizar este método, se deben administrar todos los equipos de este escenario como servidores de alta seguridad y protegerlos de la misma forma que a los controladores de dominio u otros activos de red muy valiosos. En las secciones posteriores, se abordarán los servidores de alta seguridad.
  
En el diagrama de la imagen siguiente se muestran los puntos que hay que tener en cuenta cuando se decida qué tipo de cuenta utilizar para ejecutar los servicios de forma segura.
  
[![](images/Cc170953.APGFG0301(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc170953.apgfg0301_big(es-es,technet.10).gif)
  
**Figura 3.1 Jerarquía de privilegios mínimos para la implementación de servicios**
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Creación de un grupo de servidores de alta seguridad para excepciones de administrador de dominio
  
Si decide que un servicio se ejecute con una autenticación de nivel de administrador de dominio, dicho servicio se debe alojar únicamente en un servidor de alta seguridad. Entre los servidores de alta seguridad, normalmente se incluyen:
  
-   Controladores de dominio.
  
-   Servidores que ejecutan servicios configurados para iniciar sesión como una cuenta que dispone de privilegios equivalentes a los de administrador de dominio.
  
-   Servidores de confianza para la delegación dentro de un bosque.
  
-   Servidores que ejecutan servicios de confianza para la delegación dentro de un bosque, mediante la delegación limitada de Windows Server 2003. Si desea obtener más información sobre esta característica, consulte [Transición del protocolo Kerberos y delegación restringida](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/constdel.mspx) en www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    technologies/security/constdel.mspx (en inglés).
  
Los principales pasos en la creación de un grupo de servidores de alta seguridad son los siguientes:
  
1.  Decidir a qué servidores se les asignará un nivel de seguridad alto.
  
2.  Crear un grupo de seguridad universal en cada bosque de la empresa denominado, por ejemplo, Servidores de alta seguridad.
  
3.  Agregar las cuentas de equipo de los servidores designados como seguros a los nuevos grupos universales.
  
4.  En cada dominio de cada bosque, crear un grupo local de dominio denominado, por ejemplo, Todas las cuentas de administrador de dominio, y agregar cuentas equivalentes a las de administrador de dominio a este grupo nuevo.
  
5.  En cada dominio de cada bosque, crear un objeto de directiva de grupo (GPO) de nivel de dominio y configurar la directiva para que limite el uso de cuentas de administrador de nivel de dominio en los servicios de todos los equipos. Configure la directiva con los derechos de usuario **Denegar el inicio de sesión como servicio** y **Denegar el inicio de sesión como trabajo por lotes** y, a continuación, aplique los permisos de **lectura y aplicación** en el GPO al grupo local de dominio Todas las cuentas de administrador de dominio que creó anteriormente.
  
6.  En cada dominio de cada bosque, utilice el filtrado de Directiva de grupo con el grupo Servidores de alta seguridad en cada GPO, a fin de que los miembros de este grupo puedan utilizar cuentas de administrador de nivel de dominio en los servicios. Para ello, debe aplicar **permisos de lectura y de denegación de aplicación** en el GPO sólo para el grupo universal Servidores de alta seguridad.
  
Para administrar correctamente la pertenencia al grupo universal Servidores de alta seguridad, establezca un proceso de flujo de trabajo interno para solicitar adiciones al grupo. En este proceso se deben incluir pasos para validar la solicitud y evaluar los riesgos de seguridad asociados si se agrega el servidor solicitado al grupo. El proceso de flujo de trabajo podría ser tan sencillo como enviar un mensaje de correo electrónico a un alias de solicitud, aunque lo ideal es un procedimiento automatizado. [Solution Accelerator for Business Desktop Deployment Enterprise Edition](http://go.microsoft.com/fwlink/?linkid=37676) (en inglés) incluye un componente Zero Touch Provisioning (ZTP), que ofrece un procedimiento automatizado para este proceso.
  
Si desea obtener más información, consulte las siguientes guías:
  
-   [Guía del equipo especialista en la implementación de Zero Touch Provisioning](http://www.microsoft.com/technet/itsolutions/cits/dsd/enterprise/ztpdftguide_1.mspx) en www.microsoft.com/technet/itsolutions/  
    cits/dsd/enterprise/ZTPDFTGuide\_1.mspx (en inglés)
  
-   [Guía del desarrollador de Zero Touch Provisioning](http://www.microsoft.com/technet/itsolutions/cits/dsd/enterprise/zertpd_1.mspx) en www.microsoft.com/technet/itsolutions/cits/  
    dsd/enterprise/zertpd\_1.mspx (en inglés)
  
-   [Guía del usuario final de Zero Touch Provisioning](http://www.microsoft.com/technet/itsolutions/cits/dsd/enterprise/ztpeugiude_1.mspx) en www.microsoft.com/technet/itsolutions/cits/  
    dsd/enterprise/ZTPEUGiude\_1.mspx (en inglés)
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Administración de cambios de contraseñas de cuentas de servicios
  
Cuando se asigna una cuenta a un servicio, el administrador de control de servicios (SCM) exige la contraseña correcta para dicha cuenta antes de llevar a cabo la asignación. Si se proporciona una contraseña incorrecta, el SCM rechazará la cuenta.
  
Si configura una cuenta de servicio para que utilice las cuentas de sistema local, servicio local o servicio de red, no será necesario administrar la contraseña de la cuenta del servicio, ya que el sistema operativo se encargará de ello. Por lo tanto, no se requiere administración de contraseñas para estas cuentas de servicios.
  
Con otras cuentas de servicios, el SCM almacena la contraseña en la base de datos de los servicios. Una vez asignada la contraseña, el SCM no comprueba que la contraseña almacenada en la base de datos de los servicios y la asignada a la cuenta de usuario en el servicio de directorio de Active Directory® coincidan. Por lo tanto, se podría producir una situación similar a la siguiente:
  
1.  Se configura un servicio para que se ejecute bajo una determinada cuenta de usuario.
  
2.  El servicio se inicia bajo esa cuenta con la contraseña de la cuenta actual.
  
3.  Se cambia la contraseña de la cuenta de usuario.
  
4.  El servicio continúa ejecutándose. Sin embargo, si el servicio se detiene, no podrá reiniciarlo ya que el SCM sigue utilizando la antigua contraseña, que no es válida. Esto ocurre porque, al cambiar a la contraseña de Active Directory, no se cambia la contraseña almacenada en la base de datos de servicios.
  
Si ejecuta servicios bajo cuentas de usuario local o de dominio estándar, deberá actualizar las contraseñas de éstos cada vez que cambie la contraseña de la cuenta de usuario. Esta operación puede precisar una cantidad importante de tiempo si no sabe con seguridad qué servicios se ejecutan bajo dicha cuenta o qué equipos tienen servicios que se ejecutan bajo dicha cuenta. Se recomienda documentar el uso de estos tipos de cuentas de servicios y sus contraseñas. En una organización de gran tamaño, esto podría implicar la necesidad de obtener un archivo de datos cifrado sin conexión y de almacenarlo en un depósito seguro, mientras que, en una organización de menor tamaño, quizá resultaría más adecuado almacenar un documento en una caja fuerte o un cajón cerrado con llave.
  
**Importante:** Si utiliza las consolas Usuarios y grupos locales y Usuarios y equipos de Active Directory para cambiar una contraseña de cuenta de servicio de una aplicación como, por ejemplo, Exchange Server o SQL Server, también deberá cambiar la contraseña en la interfaz de la aplicación.
  
**Nota:** Si desea obtener más información sobre la forma de escribir una herramienta que automatice la tarea de actualizar contraseñas de cuentas de servicios, consulte [Cambio de la contraseña en una cuenta de usuario de servicio](http://msdn.microsoft.com/en-us/library/ms675577.aspx) en http://msdn.microsoft.com/library/default.asp?url=/library/  
en-us/ad/ad/changing\_the\_password\_on  
\_a\_serviceampaposs\_user\_account.asp (en inglés).
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Uso de contraseñas seguras
  
Es recomendable solicitar a los administradores de red de la organización que utilicen contraseñas seguras. Deben utilizar las directivas de contraseñas de Directiva de grupo para advertir a los usuarios que cambien de contraseña tras un período determinado de tiempo. Una contraseña segura debe tener un mínimo de 10 caracteres (lo ideal son 15 o más) y debe contener una combinación de letras mayúsculas y minúsculas, números y símbolos. En Windows 2000 Server y Windows Server 2003, se puede utilizar Directiva de grupo para obligar el uso de contraseñas seguras. Si desea obtener más información, consulte [Contraseñas y directivas de cuentas](http://technet.microsoft.com/en-us/library/cc783860.aspx) en www.microsoft.com/technet/prodtechnol/windowsserver2003/  
technologies/security/bpactlck.mspx (en inglés) y la [Guía de Seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14845) en http://go.microsoft.com/fwlink/?linkid=14845.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Comprobación automática de contraseñas de administrador poco seguras
  
Es recomendable solicitar a los administradores de red de la organización que utilicen de forma regular herramientas de comprobación automatizada para detectar los servidores implementados con contraseñas poco seguras en las cuentas de administrador local. En las pruebas se debe intentar adivinar la contraseña de la cuenta de administrador local integrada que existe en todos los equipos basados en Windows.
  
Las contraseñas poco seguras representan una de las vulnerabilidades más habituales en una red y suponen uno de los medios más sencillos que un intruso utiliza para obtener acceso de administrador al equipo y poner en peligro las credenciales de las cuentas de servicios almacenadas.
  
#### Uso de Microsoft Baseline Security Analyzer
  
Se puede utilizar la herramienta Microsoft Baseline Security Analyzer (MBSA) para analizar todos los equipos en la red y buscar contraseñas poco seguras. Si desea obtener más información sobre MBSA y descargar la herramienta, consulte el sitio de [Microsoft Baseline Security Analyzer V1.2.1](http://www.microsoft.com/spain/technet/seguridad/herramientas/mbsa.mspx) en http://www.microsoft.com/spain/technet/seguridad/herramientas/mbsa.mspx.
  
La herramienta MBSA enumera todas las cuentas de usuario y comprueba las siguientes vulnerabilidades de contraseñas:
  
-   La contraseña está en blanco.
  
-   La contraseña es la misma que el nombre de la cuenta de usuario.
  
-   La contraseña es la misma que el nombre del equipo.
  
-   La contraseña utiliza la palabra "contraseña".
  
-   La contraseña utiliza la palabra "admin" o "administrador".
  
La comprobación de MBSA también le notifica sobre las cuentas deshabilitadas o sobre cuentas que actualmente están bloqueadas.
  
MBSA utilizará cada una de las contraseñas enumeradas para intentar cambiar la contraseña en el equipo de destino. Si esta operación se realiza correctamente, MBSA indica la cuenta que utiliza esa contraseña. Aunque MBSA no vuelve a establecer ni cambia la contraseña de forma permanente, informa de si ésta es sencilla y representa un riesgo de seguridad.
  
Debe tener en cuenta que, aunque MBSA puede ayudar a encontrar algunas instancias de contraseñas inadecuadas habituales, no proporciona auditorías de contraseñas completas y capacidades de recuperación, tales como las que están disponibles con algunas herramientas y aplicaciones de análisis sin conexión de terceros existentes en el mercado.
  
**Nota:** MBSA restablece las directivas de bloqueo de cuentas detectadas en el equipo con el fin de que ninguna cuenta de usuario individual se bloquee durante esta rutina de comprobación de contraseñas. MBSA no lleva a cabo estas comprobaciones en equipos configurados como controladores de dominio.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 4: Resumen
  
Antes, los desarrolladores basaban los sistemas operativos de red en la idea de conceder prioridad al acceso, lo cual era una política válida para la mayor parte de las organizaciones de entonces. Si los usuarios no podían tener acceso a los recursos o ejecutar los servicios que necesitaban, perdían productividad. Se otorgaba más importancia a la necesidad de un fácil acceso y de servicios de ejecución sencilla, que a los riesgos relacionados con las intrusiones o ataques. No obstante, con la presencia cada vez mayor de creadores de virus y de códigos malintencionados, los riesgos han aumentado. En la actualidad, la seguridad es el objetivo prioritario para la mayoría de las organizaciones.
  
En el pasado, las aplicaciones y servicios se solían instalar en un entorno empresarial con los mayores permisos posibles para garantizar una funcionalidad completa.
  
Esto se debía a una serie de factores:
  
-   Los proveedores de software, incluyendo Microsoft, no tenían una visión global de los entornos de red del cliente.
  
-   Los clientes disponían de productos de diferentes proveedores de software que requerían interoperabilidad.
  
-   Se suponía que los usuarios que instalaban las aplicaciones y los que las ejecutaban formaban parte de un mismo grupo.
  
Sin embargo, estos factores también significaban que las organizaciones concedían a las cuentas de servicios niveles de privilegio mucho más elevados de lo necesario, y que las aplicaciones y servicios se convertían en el principal punto de vulnerabilidad que los atacantes podían aprovechar.
  
Los fabricantes independientes de software (ISV) se han enfrentado de alguna forma a este problema con la mayor integración de la seguridad basada en funciones en las aplicaciones que utilizan Microsoft® .NET Framework y entornos de desarrollo como Microsoft Visual Studio® 2005.
  
Asimismo, Microsoft se ha ocupado del problema a través de importantes cambios en su sistema operativo más reciente, Microsoft Windows Server™ 2003. La configuración básica de Windows Server 2003 hace que este sistema operativo sea más seguro desde un principio.
  
Entre los cambios realizados en el sistema operativo, se incluyen diferencias en los permisos predeterminados para recursos de archivo y carpetas compartidas, cambios en la pertenencia al grupo Todos y en la pertenencia de objetos, modificaciones en la configuración predeterminada para servicios comunes y cambios en el proceso de autenticación.
  
Para obtener más información sobre las diferencias de la configuración de seguridad predeterminada en Windows Server 2003 respecto a versiones anteriores de Windows, consulte el tema [Diferencias en la configuración de seguridad predeterminada](http://technet.microsoft.com/es-es/library/cc784762.aspx) en http://www.microsoft.com/technet/prodtechnol/  
windowsserver2003/es/library/ServerHelp/1494bf2c-b596-4785-93bb-bc86f8e548d5.mspx.
  
Los servicios siguen siendo los principales puntos de vulnerabilidad para los atacantes y aquellos que se ejecutan con demasiados privilegios representan un riesgo especialmente elevado. Si no se necesita utilizar un determinado servicio, es recomendable deshabilitarlo. De este modo, se reduce inmediatamente la superficie de ataque para la red. Los servicios que no autentican a los clientes o que emplean protocolos inseguros también suponen un alto riesgo. Para obtener más información, consulte la guía [Aislamiento de servidor y dominio mediante IPsec y Directiva de grupo](http://go.microsoft.com/fwlink/?linkid=33945) en http://go.microsoft.com/fwlink/?linkid=33945.
  
Cuando los servicios sean necesarios, identifique un proceso por el cual los administradores determinen qué servicios de Windows utilizan privilegios elevados, establezcan los menores privilegios posibles necesarios para ejecutarlos y, a continuación, vuelvan a implementarlos con privilegios de inferior nivel, según corresponda.
  
[](#rrtr)[Pasos siguientes](#rrtr)  
[](#ccrt)[Lecturas adicionales](#ccrt)
  
### Pasos siguientes
  
Si una organización aún no ha implementado ningún programa que defina cómo ejecutar servicios de forma segura, esta guía proporciona una base para planear dicho proyecto.
  
Los principales pasos que hay que tomar al planear la ejecución segura de servicios son los siguientes:  
  
-   Definir un proceso que identifique los niveles de privilegio existentes en los servicios de Windows.
  
-   Identificar una manera metódica de establecer el nivel de privilegio mínimo con el que se ejecutará cualquier servicio.
  
-   Definir una forma sistemática de reducción de privilegios en servicios no predeterminados con un impacto mínimo en el entorno de producción.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Lecturas adicionales
  
La integridad de un programa que ejecuta servicios con seguridad depende de su mantenimiento a largo plazo. En Microsoft Operations Framework (MOF), se incluye información general sobre las prácticas operativas más recomendadas. Para obtener más información sobre MOF, consulte el sitio de [Microsoft Operations Framework](http://www.microsoft.com/technet/itsolutions/cits/mo/mof/default.mspx) en www.microsoft.com/technet/itsolutions/cits/mo/mof/default.mspx (en inglés).
  
Esta guía consta fundamentalmente de una serie de prácticas recomendadas. Para obtener información adicional sobre los mejores procedimientos para la ejecución segura de servicios, consulte los siguientes recursos:
  
-   Para obtener más información sobre los servicios del sistema para Windows Server 2003, consulte el capítulo 7, "Servicios del sistema", de la guía [Introducción a las amenazas y contramedidas: Configuración de la seguridad en Windows Server 2003 y Windows XP](http://www.microsoft.com/spain/technet/recursos/articulos/secmod48.mspx) en http://www.microsoft.com/spain/technet/recursos/  
    articulos/secmod48.mspx.
  
-   Para obtener más información sobre cómo Windows Server 2003 con Service Pack 1 mejora la seguridad, aumenta la confiabilidad y simplifica la administración, consulte el sitio de [Windows Server 2003 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?displaylang=es&familyid=22cfc239-337c-4d81-8354-72593b1c1f43) en http://www.microsoft.com/spain/servidores/windowsserver2003/  
    download/sp1/default.mspx.
  
-   Para obtener más información sobre cómo Windows Server 2003 utiliza la infraestructura de servicios de Active Directory® y Directiva de grupo, consulte [Políticas de Grupo](http://www.microsoft.com/spain/windowsserver2003/technologies/management/grouppolicy/default.aspx) en http://www.microsoft.com/spain/servidores/windowsserver2003/  
    technologies/management/grouppolicy/default.aspx.
  
-   Para obtener más información sobre MBSA, consulte el sitio de [Microsoft Baseline Security Analyzer (MBSA)](http://www.microsoft.com/spain/technet/seguridad/herramientas/mbsa.mspx) en http://www.microsoft.com/spain/technet/seguridad/herramientas/mbsa.mspx.
  
-   Para obtener más información sobre el Instrumental de administración de Windows, consulte:
  
    -   [WMI: Introducción al Instrumental de administración de Windows](http://technet.microsoft.com/es-es/library/cc736575.aspx) en http://www.microsoft.com/technet/prodtechnol/windowsserver2003/es/library/ServerHelp/03d4cfdf-bc6b-41cd-8154-462cf51e8c70.mspx.
  
    -   [Introducción al Instrumental de administración de Windows](http://technet.microsoft.com/es-es/library/cc736575.aspx) en http://www.microsoft.com/windows2000/es/advanced  
        /help/default.asp?url=/windows2000/es/advanced/help/windows\_wmi\_overview.htm.
  
-   Para obtener más información sobre la seguridad en los sistemas operativos Windows actuales, consulte:
  
    -   [Guía de consolidación de la seguridad de Windows 2000](http://go.microsoft.com/fwlink/?linkid=22380) en http://go.microsoft.com/fwlink/?LinkID=22380 (en inglés).
  
    -   [Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14845) en http://go.microsoft.com/fwlink/?LinkId=14845.
  
    -   [Guía de seguridad de Windows XP](http://go.microsoft.com/fwlink/?linkid=14839) en http://go.microsoft.com/fwlink/?LinkId=14839.
  
    -   [Introducción al servicio y requisitos del puerto de red para el sistema Windows Server](http://support.microsoft.com/?kbid=832017) en http://support.microsoft.com/?kbid=832017.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Agradecimientos
  
El grupo Microsoft Solutions for Security (MSS) y Security Center of Excellence (SCOE) desean agradecer y reconocer la labor realizada por el equipo que ha elaborado la *Guía de planeamiento de la seguridad de servicios y cuentas de servicios*. Las personas que se citan a continuación fueron responsables directos o contribuyeron de forma decisiva en la redacción, elaboración y comprobación de esta solución.
  
### Autores
  
Steve Ryan, *Content Master*
  
Lee Walker
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Revisores
  
Bill Canning
  
Chase Carpenter
  
Kurt Dillard
  
Patrick Hanrion
  
Jesper Johansson
  
Uri London
  
John Morello
  
Jared Pfost
  
Joel Schaeffer
  
Claudio Vacalebre
  
Shain Wray
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Editores
  
Deborah Jay, *Content Master*
  
Jennifer Kerns, *Content Master*
  
Frank Manning, *Volt*
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Directores del programa
  
Neil Bufton, *Content Master*
  
Chase Carpenter
  
Alison Woolford, *Content Master*
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Evaluadores
  
Ashish Java, *Infosys Technologies*
  
Mehul Mediwala, *Infosys Technologies*
  
Gaurav Singh Bora, *Infosys Technologies*
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Administrador de versiones
  
Flicka Crandell
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Colaboradores
  
Tony Bailey
  
Krishna Bhardwaj, *Vidyatech Solutions*
  
Prabish Chandran, *Vidyatech Solutions*
  
Christine Duell, *Valente Solutions*
  
Amy Frampton
  
Michael Glass, *Volt*
  
Karl Grunwald
  
Joanne Kennedy
  
Karina Larson, *Volt*
  
Chrissy Lewis, *Siemens*
  
Don McGowan
  
Tessa Porterfield
  
Bivin Pachatt, *Vidyatech Solutions*
  
Vivek Manohar Prabhu, *Vidyatech Solutions*
  
Stacey Tsurusaki, *Volt*
  
David Visintainer, *Volt*
  
Vikas Walia, *Vidyatech Solutions*
  
[](#mainsection)[Principio de la página](#mainsection)
  
##### Descargar
  
![](images/Cc170953.icon_exe(es-es,TechNet.10).gif)[Guía de planeamiento de la seguridad de servicios y cuentas de servicios](http://www.microsoft.com/downloads/details.aspx?familyid=f4069a30-01d7-43e8-8b30-3799db2d9c2f&displaylang=en)
  
[](#mainsection)[Principio de la página](#mainsection)
