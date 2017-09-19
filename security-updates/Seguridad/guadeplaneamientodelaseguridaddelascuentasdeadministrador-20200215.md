---
TOCTitle: Guía de planeamiento de la seguridad de las cuentas de administrador
Title: Guía de planeamiento de la seguridad de las cuentas de administrador
ms:assetid: '9e7be0f2-06cb-4150-b560-e8f25c3ee488'
ms:contentKeyID: 20200215
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc162797(v=TechNet.10)'
---

Guía de planeamiento de la seguridad de las cuentas de administrador
====================================================================

Actualizado: 25/5/2005

##### En esta página

[](#bcdi)[Información general](#bcdi)
[](#bcde)[Capítulo 1: Introducción](#bcde)
[](#bcdf)[Capítulo 2: Cómo mejorar la seguridad de las cuentas de administrador](#bcdf)
[](#bcdh)[Capítulo 3: Directrices para mejorar la seguridad de las cuentas de administrador](#bcdh)
[](#bcdg)[Capítulo 4: Resumen](#bcdg)
[](#bcdj)[Agradecimientos](#bcdj)

### Información general

Debido a sus permisos y privilegios inherentes, las cuentas de administrador de los equipos con el sistema operativo Microsoft® Windows Server™ 2003 son las cuentas más útiles y, a la vez, las potencialmente más peligrosas del equipo. Cualquier otra cuenta a la que conceda privilegios equivalentes a los de administrador plantean los mismos riesgos elevados.

Esta guía es un recurso indispensable cuando se planean estrategias para proteger las cuentas de nivel de administrador en sistemas operativos basados en Microsoft Windows NT®, como Windows Server 2003 y Windows® XP. Se trata el problema de intrusos que obtienen las credenciales de la cuenta de administrador y las utilizan para poner en peligro la red. El principal objetivo de esta guía es facilitar asesoramiento normativo en cuanto a los pasos que puede seguir para proteger los grupos y cuentas de nivel de administrador locales y basadas en dominio. Esta guía está basada en la experiencia de Security Center of Excellence (SCoE) de Microsoft en entornos de cliente y representa las prácticas recomendadas de Microsoft.

[](#edaa)[Descripción general](#edaa)
[](#ecaa)[Destinatarios de la guía](#ecaa)
[](#ebaa)[Guía de planeamiento: descripción general](#ebaa)
[](#eaaa)[Comuníquenos su opinión](#eaaa)

### Descripción general

Un aspecto importante de la seguridad de la red es la administración de los usuarios y grupos que tienen acceso administrativo a la base de datos de cuentas locales en equipos independientes y en equipos miembros del dominio, y al servicio de directorio Active Directory® en los controladores de dominio. Existen principalmente dos tipos de atacantes de los que debe protegerse:

-   Cualquier usuario malintencionado con acceso administrativo a los servidores miembro o a los controladores de dominio podría burlar la seguridad de la red. Estos individuos podrían ser usuarios sin autorización que han obtenido las contraseñas administrativas por medios ilícitos, o incluso administradores legítimos coaccionados de alguna manera por terceros o descontentos con su situación.

-   Usuarios a los que se les concede acceso administrativo. Estos individuos podrían provocar problemas inintencionadamente por no ser conscientes de las ramificaciones de los cambios de configuración.

Personas no autorizadas o inconscientes con privilegios de administrador podrían perjudicar a su organización malintencionadamente o accidentalmente si copian o eliminan datos confidenciales, propagan virus o deshabilitan la red. Es esencial administrar de forma adecuada a los usuarios y los grupos con control administrativo sobre los servidores y los controladores de dominio de la red.

La configuración de seguridad predeterminada de Windows Server 2003 es suficiente para proteger las cuentas locales y de Active Directory de prácticamente cualquier amenaza. Sin embargo, deberá reforzar la configuración predeterminada de las cuentas administrativas para mejorar el nivel de seguridad de la red y esta guía le ayudará a hacerlo.

Respetar los principios y prácticas recomendadas de esta guía puede ayudarle a reducir el riesgo de que usuarios no autorizados obtengan acceso administrativo a controladores de dominio, servidores miembro y Active Directory. La seguridad de las cuentas de administrador es una iniciativa importante para las organizaciones que desean garantizar la seguridad total de sus activos de la red.

[](#mainsection)[Principio de la página](#mainsection)

### Destinatarios de la guía

Esta guía se destina principalmente a consultores, expertos en seguridad, arquitectos de sistemas y profesionales de TI responsables de las fases de planeamiento del desarrollo de las aplicaciones o la infraestructura, así como de la implementación de Windows Server 2003. Entre las funciones a las que va destinada se incluyen:

-   Diseñadores y arquitectos de sistemas responsables de los esfuerzos en materia de arquitectura de los clientes de sus organizaciones.

-   Expertos en seguridad de TI que garanticen la seguridad de las distintas plataformas de sus organizaciones.

-   Arquitectos empresariales que administren toda la empresa y no sólo una red concreta.

-   Administradores de TI cuya responsabilidad sea determinar qué tecnología debe utilizarse para resolver determinados problemas de negocio.

-   Analistas de negocio y responsables de la toma de decisiones con requisitos y objetivos de negocio de vital importancia que dependan de la compatibilidad de los clientes.

-   Consultores de socios y servicios de Microsoft que precisen recursos detallados con información útil y relevante para asociados y clientes empresariales.

Aunque se ha escrito principalmente para estas funciones, la *Guía de planeamiento de la seguridad de las cuentas de administrador* también puede resultar útil para los generalistas de TI en organizaciones medianas y grandes, y las funciones de los equipos de infraestructura, operaciones y seguridad identificados en el modelo de equipo de Microsoft Operations Framework (MOF). Para obtener más información acerca de MOF, consulte la página de inicio de [Microsoft Operations Framework](http://www.microsoft.com/technet/itsolutions/cits/mo/mof/default.mspx) en www.microsoft.com/technet/itsolutions/cits/mo/mof/default.mspx.

[](#mainsection)[Principio de la página](#mainsection)

### Guía de planeamiento: descripción general

Esta guía incluye:

**Capítulo 1: Introducción**

En este capítulo se proporciona un resumen ejecutivo y una descripción general y se sugieren los destinatarios recomendados de la guía. También se proporciona un resumen de los capítulos de la guía.

**Capítulo 2: Cómo mejorar la seguridad de las cuentas de administrador**

En este capítulo se proporciona una descripción general de los grupos y cuentas de usuarios administrativos que puede utilizar para iniciar la sesión en un equipo o dominio y se describen los principios que deben aplicarse cuando se planea la protección de las cuentas de administrador.

**Capítulo 3: Directrices para mejorar la seguridad de las cuentas de administrador**

En este capítulo se describen algunas directrices de prácticas recomendadas que se deben seguir al proteger las cuentas administrativas. Estas directrices siguen los principios que se han descrito en el capítulo anterior.

**Capítulo 4: Resumen**

En este capítulo se resume la orientación proporcionada y se tratan los problemas que pueden surgir cuando se sigue esta guía. También se proporcionan vínculos a otros materiales de lectura que pueden resultarle útiles.

[](#mainsection)[Principio de la página](#mainsection)

### Comuníquenos su opinión

Microsoft valora su opinión acerca de este material. Apreciaríamos especialmente cualquier comentario relacionado con las preguntas siguientes:

-   ¿En qué medida ha resultado útil la información proporcionada?

-   ¿Los procedimientos paso a paso fueron precisos?

-   ¿Los capítulos le resultaron fáciles de leer e interesantes?

-   ¿Cómo calificaría esta solución en líneas generales?

Envíe sus comentarios a la siguiente dirección de correo electrónico: [cisfdbk@microsoft.com](mailto:cisfdbk@microsoft.com?subject=guía%20de%20planeamiento%20de%20la%20seguridad%20de%20las%20cuentas%20de%20administrador)

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 1: Introducción

[](#abcm)[Resumen ejecutivo](#abcm)
[](#abcn)[Guía de planeamiento: descripción general](#abcn)

### Resumen ejecutivo

Debido a sus permisos y privilegios inherentes, las cuentas de administrador de los equipos con el sistema operativo Microsoft® Windows Server™ 2003 son las cuentas más útiles y, al mismo tiempo, las potencialmente más peligrosas de su equipo. Cualquier otra cuenta a la que conceda privilegios equivalentes a los de administrador plantean los mismos riesgos elevados.

Esta guía es un recurso indispensable cuando se planean estrategias para proteger las cuentas de nivel de administrador en sistemas operativos basados en Microsoft Windows NT®, como Windows Server 2003 y Windows® XP. Se trata el problema de intrusos que obtienen las credenciales de la cuenta de administrador y las utilizan para poner en peligro la red. El principal objetivo de esta guía es facilitar asesoramiento normativo en cuanto a los pasos que puede seguir para proteger los grupos y cuentas de nivel de administrador locales y basadas en dominio. Esta guía está basada en la experiencia de Security Center of Excellence (SCoE) de Microsoft en entornos de cliente y representa las prácticas recomendadas de Microsoft.

#### Descripción general

Un aspecto importante de la seguridad de la red es la administración de los usuarios y grupos que tienen acceso administrativo a la base de datos de cuentas locales en equipos independientes y en equipos miembros del dominio, y al servicio de directorio Active Directory® en los controladores de dominio. Existen principalmente dos tipos de atacantes de los que debe protegerse:

-   Cualquier usuario malintencionado con acceso administrativo a los servidores miembro o a los controladores de dominio podría burlar la seguridad de la red. Estos individuos podrían ser usuarios sin autorización que han obtenido las contraseñas administrativas por medios ilícitos, o incluso administradores legítimos coaccionados de alguna manera por terceros o descontentos con su situación.

-   Usuarios a los que se les concede acceso administrativo. Estos individuos podrían provocar problemas inintencionadamente por no ser conscientes de las ramificaciones de los cambios de configuración.

Personas no autorizadas o inconscientes con privilegios de administrador podrían perjudicar a su organización malintencionadamente o accidentalmente si copian o eliminan datos confidenciales, propagan virus o deshabilitan la red. Es esencial administrar de forma adecuada a los usuarios y los grupos con control administrativo sobre los servidores y los controladores de dominio de la red.

La configuración de seguridad predeterminada de Windows Server 2003 es suficiente para proteger las cuentas locales y de Active Directory de prácticamente cualquier amenaza. Sin embargo, deberá reforzar la configuración predeterminada de las cuentas administrativas para mejorar el nivel de seguridad de la red y esta guía le ayudará a hacerlo.

Respetar los principios y prácticas recomendadas de esta guía puede ayudarle a reducir el riesgo de que usuarios no autorizados obtengan acceso administrativo a controladores de dominio, servidores miembro y Active Directory. La seguridad de las cuentas de administrador es una iniciativa importante para las organizaciones que desean garantizar la seguridad total de sus activos de la red.

#### Destinatarios de la guía

Esta guía se destina principalmente a consultores, expertos en seguridad, arquitectos de sistemas y profesionales de TI responsables de las fases de planeamiento del desarrollo de las aplicaciones o la infraestructura, así como de la implementación de Windows Server 2003. Entre las funciones a las que va destinada se incluyen:

-   Diseñadores y arquitectos de sistemas responsables de los esfuerzos en materia de arquitectura de los clientes de sus organizaciones.

-   Expertos en seguridad de TI que garanticen la seguridad de las distintas plataformas de sus organizaciones.

-   Arquitectos empresariales que administren toda la empresa y no sólo una red concreta.

-   Administradores de TI cuya responsabilidad sea determinar qué tecnología debe utilizarse para resolver determinados problemas de negocio.

-   Analistas de negocio y responsables de la toma de decisiones con requisitos y objetivos de negocio de vital importancia que dependan de la compatibilidad de los clientes.

-   Consultores de socios y servicios de Microsoft que precisen recursos detallados con información útil y relevante para asociados y clientes empresariales.

Aunque se ha escrito principalmente para estas funciones, la *Guía de planeamiento de la seguridad de las cuentas de administrador* también puede resultar útil para los generalistas de TI en organizaciones medianas y grandes, y las funciones de los equipos de infraestructura, operaciones y seguridad identificados en el modelo de equipo de Microsoft Operations Framework (MOF). Para obtener más información acerca de MOF, consulte la página de inicio de [Microsoft Operations Framework](http://www.microsoft.com/technet/itsolutions/cits/mo/mof/default.mspx) en www.microsoft.com/technet/itsolutions/cits/mo/mof/default.mspx.

[](#mainsection)[Principio de la página](#mainsection)

### Guía de planeamiento: descripción general

Esta guía incluye:

#### Capítulo 1: Introducción

En este capítulo se proporciona un resumen ejecutivo y una descripción general y se sugieren los destinatarios recomendados de la guía. También se proporciona un resumen de los capítulos de la guía.

#### Capítulo 2: Cómo mejorar la seguridad de las cuentas de administrador

En este capítulo se proporciona una descripción general de los grupos y cuentas de usuarios administrativos que puede utilizar para iniciar la sesión en un equipo o dominio y se describen los principios que deben aplicarse cuando se planea la protección de las cuentas de administrador.

#### Capítulo 3: Directrices para mejorar la seguridad de las cuentas de administrador

En este capítulo se describen algunas directrices de prácticas recomendadas que se deben seguir al proteger las cuentas administrativas. Estas directrices siguen los principios que se han descrito en el capítulo anterior.

#### Capítulo 4: Resumen

En este capítulo se resume la orientación proporcionada y se tratan los problemas que pueden surgir cuando se sigue esta guía. También se proporcionan vínculos a otros materiales de lectura que pueden resultarle útiles.

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 2: Cómo mejorar la seguridad de las cuentas de administrador

En este capítulo se describe por qué es importante proteger al máximo las cuentas de administrador y se proporciona una descripción general de los grupos y cuentas de usuarios administrativos que puede utilizar para iniciar la sesión en un equipo o dominio. También se describen los principios básicos que deben aplicarse cuando se planea la protección de las cuentas de administrador.

[](#abcd)[Por qué es importante mejorar la seguridad de las cuentas de administrador](#abcd)
[](#abce)[Descripción general de las cuentas y los grupos administrativos](#abce)
[](#abcf)[Principios para mejorar la seguridad de las cuentas de administrador](#abcf)

#### Por qué es importante mejorar la seguridad de las cuentas de administrador

Es esencial que las cuentas de administrador sean tan seguras como sea posible para garantizar la protección total de los activos de la red de la organización. Deberá proteger todos los equipos que pueda utilizar un administrador (controladores de dominio, servidores y las estaciones de trabajo que éste utilice). El grupo de TI de su empresa debe garantizar la seguridad de los controladores de dominio y servidores de entidad emisora de certificados, pues se consideran activos de máxima confianza. También deberán protegerse los equipos de escritorio y móviles de los administradores como activos de confianza, pues los administradores los utilizan para administrar de forma remota el bosque, el dominio y la infraestructura.

Los servidores miembro que se conectan con frecuencia a controladores de dominio requieren privilegios elevados para conectarse y proporcionar servicios. Como es habitual que esto signifique la existencia de credenciales elevadas en el servidor (normalmente derechos de administrador de dominio), si se compromete la seguridad de alguno de estos servidores, se comprometerá la de todo el dominio. Por ejemplo, un atacante podría asumir el control de un solo servidor miembro y utilizarlo como un punto desde el cual atacar a todo el dominio.

Garantizar la seguridad de las cuentas de administrador de dominio es aún más importante cuando se utilizan confianzas de entorno seguro entre bosques o dominios. Las organizaciones deben poder asumir que pueden utilizar cuentas de dominio en todos los dominios de confianza y que se aplican los mismos estándares elevados de protección de las cuentas de administrador a todos los dominios. Por ejemplo, supongamos que tuviera un dominio raíz llamado Prueba.com y dos subdominios, PruebaA.com y PruebaB.com. Si a los administradores de PruebaB.com se les otorgara explícitamente privilegios administrativos en PruebaA.com o si fueran miembros del grupo Administradores de organización en todo el bosque, sería inútil proteger las cuentas de administrador en PruebaA.com. El motivo es que, si las cuentas de administrador de PruebaB.com no son seguras, los intrusos que logren entrar en el dominio poco seguro PruebaB.com podrían obtener acceso administrativo al dominio seguro PruebaA.com.

#### Por qué no debe iniciar una sesión en su equipo como administrador

Si normalmente inicia la sesión en su equipo como administrador para llevar a cabo las tareas comunes basadas en aplicaciones, hará que el equipo sea vulnerable ante software malintencionado y otros riesgos para la seguridad pues el software malintencionado se ejecutará con los mismos privilegios que se utilizaron para iniciar la sesión. Si visita un sitio de Internet o abre un archivo adjunto a un mensaje de correo, puede dañar el equipo ya que podría descargarse y ejecutarse en su equipo código malintencionado.

Si inicia la sesión como administrador en un equipo local, el código malintencionado podría, entre otras acciones, formatear la unidad de disco duro, eliminar archivos y crear una nueva cuenta de usuario con privilegios administrativos. Si inicia la sesión como miembro del grupo Administradores de dominio, el grupo Administradores de organización o el grupo Administradores de esquema en el servicio de directorio Active Directory®, el código malintencionado podría crear una nueva cuenta de usuario de dominio con acceso administrativo y poner en peligro los datos de dominio, configuración o esquema.

En un equipo local, deber agregar su cuenta de usuario de dominio sólo al grupo Usuarios (y no al grupo Administradores) para llevar a cabo tareas rutinarias como ejecutar programas o visitar sitios de Internet. Cuando sea necesario llevar a cabo tareas administrativas en un equipo local o en Active Directory, utilice el comando **Ejecutar como** para iniciar un programa con credenciales administrativas.

El comando **Ejecutar como** permite llevar a cabo tareas administrativas sin poner en peligro los datos de Active Directory o su equipo. Para obtener más información acerca de cómo utilizar el comando **Ejecutar como**, consulte la sección Utilizar el servicio de inicio de sesión secundario del capítulo 3 de esta guía, "Directrices para mejorar la seguridad de las cuentas de administrador".

![](images/Cc162797.note(es-es,TechNet.10).gif)**Nota:** para obtener más información acerca del uso de **Ejecutar como** en Microsoft® Windows® 2000, Windows XP y Windows Server™ 2003, consulte los artículos de Knowledge Base 294676, 305780, 325859 y 325362. Puede encontrar estos artículos por su número en el sitio Web [Búsqueda de Knowledge Base (KB) de soporte técnico](http://support.microsoft.com/default.aspx) en http://support.microsoft.com/default.aspx?scid=fh;en-us;KBHOWTO ** **

[](#mainsection)[Principio de la página](#mainsection)

#### Descripción general de las cuentas y los grupos administrativos

Existen varios grupos y cuentas de usuario administrativo cuyas credenciales pueden utilizarse para iniciar la sesión en un equipo o dominio. Entre las cuentas administrativas del dominio de Active Directory se incluyen las siguientes:

-   La cuenta Administrador, que se crea con la instalación de Active Directory en el primer controlador del dominio. Es la cuenta con más privilegios. La persona encargada de instalar Active Directory en el equipo crea la contraseña de esta cuenta durante la instalación. Si el dominio es el primero creado en un bosque, se convierte automáticamente en el dominio raíz del bosque y, por lo tanto, contiene el grupo Administradores de organización. La cuenta de administrador para este dominio raíz de bosque es miembro del grupo Administradores de organización de forma predeterminada y como tal tiene privilegios administrativos para todo el bosque. De forma predeterminada, la primera cuenta de administrador creada en cada dominio es también el Agente de recuperación de datos (DRA) para el Sistema de cifrado de archivos (EFS) en cada dominio.

-   Las cuentas que cree posteriormente y a las que asigne directamente privilegios administrativos o coloque en un grupo con privilegios administrativos.

-   Las cuentas que utilizan certificados del Agente de recuperación de datos para EFS, certificados de un Agente de inscripción o certificados de Agente de recuperación de claves. Las cuentas que utilizan estos certificados de agente tienen muchos privilegios y también deben protegerse. Por ejemplo, si alguien consigue un certificado de Agente de inscripción puede inscribirse para un certificado y generar una tarjeta inteligente en nombre de otro usuario de la organización. La tarjeta inteligente resultante podría utilizarse para iniciar sesión en la red y suplantar al usuario real. Debido a las enormes capacidades de estas cuentas de certificado de agente, se recomienda que las organizaciones mantengan una directiva de seguridad estricta sobre quién tiene una de esas cuentas.

El número de grupos administrativos en un dominio Active Directory varía según los servicios instalados. Entre los grupos utilizados específicamente para la administración de Active Directory se incluyen:

-   Grupos administrativos que ya existen en el contenedor Builtin; por ejemplo, operadores de cuentas y operadores de servidores. Tenga en cuenta que los grupos del contenedor Builtin no se pueden cambiar de ubicación.

-   Grupos administrativos que ya existen en el contenedor Usuarios; por ejemplo, Administradores de dominio y Propietarios del creador de directivas de grupo.

-   Los grupos que se creen posteriormente y se incluyan en un grupo con privilegios administrativos o a la que se asignen directamente estos privilegios.

Las cuentas y los grupos administrativos predeterminados de un entorno de dominio son:

-   Administradores de organización (existen sólo en los dominios raíz del bosque)

-   Administradores de dominio (existen en todos los dominios)

-   Administradores de esquema (existen sólo en los dominios raíz del bosque)

-   Propietarios del creador de directivas de grupo (existen sólo en los dominios raíz del bosque)

-   Grupo Administradores

-   Cuenta de administrador

-   Cuenta de administrador del modo de restauración de SD (disponible sólo en Modo de restauración de servicios de directorio. Esta cuenta es local para el controlador de dominio y no es una cuenta de todo el dominio. La contraseña para esta cuenta se establece al instalar Active Directory en el equipo).

Para obtener una descripción completa de cada uno de estas cuentas y grupos administrativos, consulte los temas "Grupos predeterminados: Active Directory" y "Cuentas de usuarios y equipos" en el Centro de ayuda y soporte técnico de Windows Server 2003.

##### Tipos de cuenta de administrador

Existen básicamente tres categorías de cuentas de administrador para iniciar la sesión en un equipo o dominio. Cada categoría tiene privilegios y capacidades exclusivas.

-   **Cuentas de administrador local**. Esta categoría incluye la cuenta de administrador integrada que crea y utiliza Windows Server 2003 la primera vez que se instala en un equipo. Esta categoría también incluye cualquier otra cuenta de usuario que posteriormente cree y agregue al grupo Administradores local integrado. Los miembros de este grupo tienen acceso completo sin restricciones al equipo local.

-   **Cuentas de administrador de dominio**. Esta categoría incluye la cuenta de administrador de dominio integrada que crea y utiliza Active Directory la primera vez que se instala. Esta categoría también incluye cualquier otra cuenta de usuario que posteriormente cree y agregue al grupo Administradores local integrado o al grupo Administradores de dominio. Los miembros de estos grupos tienen acceso completo sin restricciones al dominio y, si no se protegen adecuadamente, a todo el bosque.

-   **Cuentas de administrador de bosque**. Esta categoría incluye la cuenta de administrador de dominio integrada del primer dominio creado en el bosque, que se denomina dominio raíz del bosque, porque la cuenta de administrador del dominio raíz del bosque se agrega automáticamente al grupo Administradores de organización al instalar Active Directory. Esta categoría también incluye cualquier otra cuenta de usuario que posteriormente cree y agregue al grupo Administradores de organización. Los miembros del grupo Administradores de organización tienen acceso completo sin restricciones a todo el bosque. Los administradores de organización también pueden instalar entidades emisoras de certificados, que pueden utilizarse para suplantar a cualquier usuario del bosque.

[](#mainsection)[Principio de la página](#mainsection)

#### Principios para mejorar la seguridad de las cuentas de administrador

Al planear cómo proteger mejor sus cuentas administrativas, debe:

-   Aplicar el principio de privilegios mínimos

-   Seguir las directrices de prácticas recomendadas para mejorar la seguridad de las cuentas de administrador

##### Principio de privilegios mínimos

La mayoría de cursos y documentos relacionados con la seguridad proponen la implementación de un principio de privilegios mínimos; no obstante, las organizaciones siguen esta recomendación en contadas ocasiones. El principio es simple y el efecto de aplicarlo correctamente aumenta considerablemente la seguridad y reduce los riesgos. El principio especifica que todos los usuarios deben iniciar la sesión con una cuenta de usuario que sólo tenga los permisos mínimos necesarios para llevar a cabo la tarea actual. Ésta es una forma de protección contra código malintencionado, entre otros ataques. Este principio es válido para los equipos y para los usuarios de dichos equipos.

Un motivo por el que este principio funciona tan bien es que le obliga a hacer ciertas averiguaciones internas. Por ejemplo, deberá determinar los privilegios de acceso que realmente necesita un equipo o usuario y, a continuación, implementarlos. Para muchas organizaciones, esta tarea podría parecer inicialmente una ingente cantidad de trabajo; sin embargo, es un paso esencial para proteger correctamente el entorno de red.

Debe otorgar a todos los usuarios administradores de dominio sus privilegios de dominio según el concepto de privilegios mínimos. Por ejemplo, si un administrador inicia la sesión con una cuenta con privilegios e inintencionadamente ejecuta un programa de virus, el virus tendrá acceso administrativo al equipo local y a todo el dominio. Si el administrador hubiera iniciado la sesión con una cuenta sin privilegios (no administrativa), el virus sólo afectaría al equipo local pues se ejecuta como usuario del equipo local.

Otro ejemplo: las cuentas a las que se otorgan derechos de administrador de nivel de dominio no deben tener derechos elevados en otro bosque, aunque exista una relación de confianza entre los bosques. Esta táctica evita daños mayores si un atacante consigue poner en peligro un bosque administrado. Las organizaciones deben auditar periódicamente su red para protegerla de la elevación de privilegios no autorizada.

##### Prácticas recomendadas para mejorar la seguridad de las cuentas de administrador

Entre las directrices de prácticas recomendadas que debe seguir para mejorar la seguridad de las cuentas administrativas en Windows Server 2003 se incluyen:

-   Separar las funciones Administrador de dominio y Administrador de organización.

-   Separar las cuentas de usuario y administrador.

-   Utilizar el servicio de inicio de sesión secundario.

-   Ejecutar una sesión independiente de Servicios de Terminal Server para administración.

-   Cambiar el nombre de la cuenta Administrador predeterminada.

-   Crear una cuenta Administrador señuelo.

-   Crear una cuenta de administrador secundaria y deshabilitar la cuenta Administrador integrada.

-   Habilitar el bloqueo de la cuenta para inicios de sesión de administrador remotos.

-   Crear una contraseña de administrador segura.

-   Detectar automáticamente contraseñas poco seguras.

-   Utilizar credenciales administrativas sólo en equipos de confianza.

-   Auditar las cuentas y contraseñas periódicamente.

-   Prohibir la delegación de cuentas.

-   Controlar el proceso de inicio de sesión administrativa.

Para obtener más información acerca de estas directrices de prácticas recomendadas, consulte el capítulo 3, "Directrices para mejorar la seguridad de las cuentas de administrador" de esta guía.

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 3: Directrices para mejorar la seguridad de las cuentas de administrador

En este capítulo se describen algunas directrices de prácticas recomendadas generales para mejorar la seguridad de las cuentas administrativas. Estas directrices siguen los principios que se han presentado en el capítulo 2, "Cómo mejorar la seguridad de las cuentas de administrador".

##### Descripción general de las directrices para mejorar la seguridad de las cuentas de administrador

Cada nueva instalación del servicio de directorio Active Directory® crea una cuenta Administrador para cada dominio. De forma predeterminada, esta cuenta no se puede eliminar ni bloquear. En Microsoft® Windows Server™ 2003, la cuenta Administrador se puede deshabilitar, pero se vuelve a habilitar automáticamente al iniciar el equipo en modo a prueba de errores.

Un usuario malintencionado que intenta tener acceso a un equipo empieza normalmente por buscar una cuenta válida y, a continuación, intenta aumentar los privilegios de dicha cuenta. También puede intentar el uso de técnicas para averiguar contraseñas con el fin de obtener la contraseña de la cuenta Administrador. Se centra en esta cuenta porque tiene más privilegios y no se puede bloquear. También puede intentar engañar al administrador para que ejecute código malintencionado que concederá acceso al atacante.

##### Separar las funciones Administrador de dominio y Administrador de organización

Debido a que la función Administrador de organización tiene los máximos privilegios en un entorno de bosque, debe llevar a cabo una de estas dos acciones para garantizar que su uso está bien controlado. Puede crear y seleccionar una única cuenta bien protegida que sea miembro de Administradores de organización u optar por no configurar una cuenta con dichas credenciales y, en su lugar, crear esa cuenta únicamente cuando una tarea autorizada que requiera estos privilegios así lo exija. Después de que la cuenta termine la tarea, debe eliminar inmediatamente la cuenta de Administradores de organización temporal.

##### Separar las cuentas de usuario y administrador

Para cada usuario que desempeñe una función de administrador, debe crear dos cuentas: una cuenta de usuario normal para las tareas cotidianas típicas, como correo electrónico y otros programas, y una cuenta administrativa únicamente para las tareas administrativas. No debe habilitar estas cuentas administrativas para el correo electrónico, utilícelas para ejecutar programas estándar o explorar Internet. Cada cuenta debe disponer de una contraseña única. Si adopta estas precauciones simples, contribuirá a reducir considerablemente la exposición de las cuentas a los riesgos externos y la cantidad de tiempo que las cuentas administrativas están activas en un equipo o dominio.

##### Utilizar el servicio de inicio de sesión secundario

En Microsoft Windows® 2000, Windows XP Professional y Windows Server 2003, se pueden ejecutar programas como un usuario distinto del que ha iniciado la sesión actualmente. En Windows 2000, el servicio **Ejecutar como** proporciona esta capacidad, mientras que en Windows XP y Windows Server 2003, se denomina servicio de inicio de sesión secundario. Los servicios **Ejecutar como** e Inicio de sesión secundario son el mismo pero con nombres distintos.  

El inicio de sesión secundario permite a los administradores iniciar sesión en el equipo con una cuenta no administrativa y, sin cerrar la sesión, llevar a cabo tareas administrativas mediante la ejecución de programas administrativos de confianza en contextos administrativos.

Un servicio de inicio de sesión secundario soluciona los riesgos de seguridad que se les presentan a los administradores que ejecutan programas que son vulnerables al código malintencionado; por ejemplo, un usuario que obtiene acceso a un sitio Web mientras ha iniciado sesión con privilegios administrativos.

El inicio de sesión secundario está destinado principalmente a administradores del sistema; no obstante, puede utilizarlo cualquier usuario que disponga de varias cuentas y necesite iniciar programas en distintos contextos de cuenta sin cerrar la sesión.

El servicio de inicio de sesión secundario está configurado para iniciarse automáticamente, utiliza la herramienta **Ejecutar como** de interfaz de usuario y emplea **runas.exe** de interfaz de línea de comandos. Con **Ejecutar como**, puede ejecutar programas (\*.exe), consolas de Microsoft Management Console (MMC) guardadas (\*.msc), accesos directos a programas y elementos del Panel de control. Puede ejecutar estos programas como administrador aunque haya iniciado la sesión en su equipo con una cuenta de usuario estándar que no disponga de privilegios administrativos, siempre que proporcione las credenciales adecuadas para la contraseña y la cuenta de usuario administrativo cuando se le soliciten.

**Ejecutar como** permite administrar un servidor de otro dominio o bosque si dispone de las credenciales de la cuenta de administrador del otro dominio.

![](images/Cc162797.note(es-es,TechNet.10).gif)**Nota:** algunos elementos, como la carpeta Impresoras, Mi PC y Mis sitios de red del escritorio, no se pueden iniciar con **Ejecutar como**.

#### Uso de Ejecutar como

**Ejecutar como** se puede utilizar de varias formas:

**Para utilizar Ejecutar como con el fin de iniciar un shell de comandos con credenciales de cuenta de administrador**

1.  Haga clic en **Inicio** y, a continuación, en **Ejecutar**.

2.  En el cuadro de diálogo **Ejecutar**, escriba **runas /user:**&lt;*nombre\_dominio*&gt;**\\administrador cmd** (donde &lt;*nombre\_dominio*&gt; es el nombre del dominio) y, a continuación, haga clic en **Aceptar**.

3.  Cuando se le pida que especifique una contraseña para la cuenta *nombre\_dominio*\\administrador, escriba la contraseña de la cuenta de administrador y, a continuación, presione ENTRAR.

4.  Aparecerá una nueva ventana de consola, que se ejecuta en el contexto administrativo. El título de la consola se identifica como **Ejecutándose como** *nombre\_dominio***\\administrador**.

**Para utilizar Ejecutar como con el fin de ejecutar un elemento del Panel de control**

1.  En Windows XP o Windows Server 2003, haga clic en **Inicio** y, a continuación, en **Panel de control**.

2.  Mientras mantiene presionada la tecla MAYÚS, haga clic con el botón secundario del mouse (ratón) en la herramienta o programa que desee ejecutar en un contexto administrativo (por ejemplo, **Agregar hardware**).

3.  En el menú contextual, haga clic en **Ejecutar como**.

4.  En el cuadro de diálogo **Ejecutar como**, haga clic en **El siguiente usuario** y, a continuación, escriba el nombre de dominio adecuado, el nombre de la cuenta de administrador y la contraseña; por ejemplo:

    DOMINIOEMP\\Administrador

    C0ntr@señ@

5.  Haga clic en **Aceptar**. El programa se ejecuta en el contexto administrativo.

**Para utilizar Ejecutar como con el fin de abrir un programa del menú Inicio, como Usuarios y equipos de Active Directory**

1.  En Windows Server 2003, haga clic en **Inicio**, seleccione **Herramientas administrativas** y, a continuación, haga clic con el botón secundario del mouse (ratón) en **Usuarios y equipos de Active Directory**.

2.  En el menú contextual, haga clic en **Ejecutar como**.

También puede emplear la utilidad de la línea de comandos ejecutable **runas.exe** para ejecutar programas e iniciar consolas de administración desde la línea de comandos.

**Para iniciar una instancia del símbolo del sistema como administrador en un equipo local**

1.  Haga clic en **Inicio** y, a continuación, en **Ejecutar**.

2.  En el cuadro de diálogo **Ejecutar**, escriba **runas /user:**&lt;*nombre\_equipo\_local*&gt;**\\administrador cmd**

3.  Haga clic en **Aceptar**.

4.  Cuando se le pida, escriba la contraseña del administrador en la ventana del símbolo del sistema y, a continuación, presione ENTRAR.

**Para iniciar una instancia del complemento Administración de equipos con una cuenta de administrador de dominio denominada** ***administradordominio*** **en el** **dominio*dominioemp***

1.  Haga clic en **Inicio** y, a continuación, en **Ejecutar**.

2.  En el cuadro de diálogo **Ejecutar**, escriba **runas /user:**&lt;*dominioemp*&gt;**\\**&lt;*administradordominio*&gt; **"mmc %windir%\\system32\\compmgmt.msc"** 

3.  Haga clic en **Aceptar**.

4.  Cuando se le pida, escriba la contraseña de la cuenta en la ventana del símbolo del sistema y, a continuación, presione ENTRAR.

También puede utilizar **runas.exe** para ejecutar programas e iniciar consolas de administración desde la línea de comandos con credenciales de tarjeta inteligente.

**Para iniciar una instancia del símbolo del sistema como administrador en su equipo local con credenciales de tarjeta inteligente**

1.  Haga clic en **Inicio** y, a continuación, en **Ejecutar**.

2.  En el cuadro de diálogo **Ejecutar**, escriba **runas /smartcard /user:**&lt;*nombre\_equipo\_local&gt;***\\administrador cmd** 

3.  Haga clic en **Aceptar**.

4.  Cuando se le pida, escriba el número PIN de la tarjeta inteligente en la ventana del símbolo del sistema y, a continuación, presione ENTRAR.

![](images/Cc162797.note(es-es,TechNet.10).gif)**Nota:** no es posible especificar la contraseña como un parámetro de la línea de comandos para **runas.exe** porque no sería seguro hacerlo.

##### Ejecutar una sesión independiente de Servicios de Terminal Server para administración

**Ejecutar como** es el enfoque más habitual que los administradores utilizan cuando realizan cambios en sus equipos locales y posiblemente ejecutar algunos programas de línea de negocios. Para las tareas administrativas basadas en TI, puede utilizar Servicios de Terminal Server para conectarse a los servidores que necesita administrar. Resulta más sencillo para administrar varios servidores remotos sin tener que desplazarse físicamente a cada uno y este enfoque reduce la necesidad de derechos de inicio de sesión interactivo en los servidores. Para utilizar este método, inicie la sesión con las credenciales de su cuenta de usuario normal y, a continuación, ejecute una sesión de Servicios de Terminal Server como administrador del dominio. Sólo debe realizar tareas de administración de dominio en esta ventana de sesión.

##### Cambiar el nombre de la cuenta Administrador predeterminada

Cuando se cambia el nombre de la cuenta Administrador predeterminada, se elimina la indicación evidente de que esta cuenta dispone de privilegios elevados. Aunque un atacante sigue necesitando la contraseña para utilizar la cuenta Administrador predeterminada, al cambiar el nombre de dicha cuenta se agrega un nivel adicional de protección contra los ataques de elevación de privilegios. Una posibilidad sería utilizar un nombre y unos apellidos ficticios que tengan el mismo formato que los demás nombres de usuario.

![](images/Cc162797.note(es-es,TechNet.10).gif)**Nota:** al cambiar el nombre de la cuenta Administrador predeterminada sólo se impiden determinados tipos de ataque. Continúa siendo relativamente sencillo para un atacante determinar cuál es la cuenta Administrador predeterminada, ya que el Id. de seguridad de esta cuenta siempre es el mismo. Además, existen herramientas que enumeran miembros de grupos y siempre se muestra la cuenta de administrador original en primer lugar. Para obtener la máxima protección contra ataques a la cuenta de administrador integrada, cree una nueva cuenta de administración y, a continuación, deshabilite la integrada.

**Para cambiar el nombre de la cuenta Administrador predeterminada en un dominio**

1.  Inicie sesión como miembro del grupo de administradores de dominio (pero no la cuenta Administrador integrada) y, a continuación, abra **Usuarios y equipos de Active Directory**.

2.  En el árbol de consola, haga clic en **Users**.

3.  En el panel de detalles, haga clic con el botón secundario del mouse (ratón) en **Administrador** y, a continuación, haga clic en **Cambiar nombre**.

4.  Escriba un nombre y unos apellidos ficticios y, a continuación, presione Entrar.

5.  En el cuadro de diálogo **Cambiar nombre de usuario**, modifique los valores de los campos **Nombre completo**, **Nombre**, **Apellidos**, **Nombre para mostrar**, **Nombre de inicio de sesión de usuario** y **Nombre de inicio de sesión de usuario (anterior a Windows 2000)** para que coincidan con los de la cuenta ficticia y, a continuación, haga clic en **Aceptar**.

6.  En el panel de detalles, haga clic con el botón secundario del mouse (ratón) en el nuevo nombre y, a continuación, haga clic en **Propiedades**.

7.  Haga clic en la ficha **General**. En el cuadro **Descripción**, elimine **Cuenta para la administración del equipo o dominio** y, a continuación, escriba una descripción similar a las demás cuentas de usuario (en muchas organizaciones este valor está en blanco).

8.  Haga clic en **Aceptar**.

**Para cambiar el nombre de la cuenta Administrador local predeterminada**

1.  Inicie sesión como miembro del grupo Administradores local (pero no la cuenta Administrador integrada) y abra la herramienta de complemento **Usuarios locales y grupos** en la consola **Administración de equipos**.

2.  En el árbol de consola, expanda **Usuarios locales y grupos** y, a continuación, haga clic en **Usuarios**.

3.  En el panel de detalles, haga clic con el botón secundario del mouse (ratón) en **Administrador** y, a continuación, haga clic en **Cambiar nombre**.

4.  Escriba un nombre y unos apellidos ficticios y, a continuación, presione Entrar.

5.  En el panel de detalles, haga clic con el botón secundario del mouse (ratón) en el nuevo nombre y, a continuación, haga clic en **Propiedades**.

6.  Haga clic en la ficha **General**. En el cuadro **Nombre completo**, escriba el nuevo nombre completo. En el cuadro **Descripción**, elimine **Cuenta para la administración del equipo o dominio** y, a continuación, escriba una descripción similar a las demás cuentas de usuario (en muchas organizaciones este valor está en blanco).

7.  Haga clic en **Aceptar**.

![](images/Cc162797.note(es-es,TechNet.10).gif)**Nota:** también existe una configuración de objeto de directiva de grupo (GPO) que puede utilizar para cambiar el nombre de la cuenta Administrador predeterminada en gran cantidad de equipos. No obstante, esta configuración no permite modificar la descripción predeterminada. Para obtener más información, consulte el artículo de Knowledge Base [HOW TO: Rename the Administrator and Guest Account in Windows Server 2003](http://support.microsoft.com/default.aspx?scid=kb;en-us;816109) en http://support.microsoft.com/default.aspx?scid=kb;en-us;816109.

##### Crear una cuenta Administrador señuelo

La creación de una cuenta Administrador señuelo agrega un nivel adicional de protección. Puede engañar a un atacante que planee un ataque de contraseña en la cuenta Administrador para que lo haga en una cuenta que no tenga privilegios especiales, por lo que es muy poco probable que el atacante descubra que ha cambiado el nombre de la cuenta Administrador. También es aconsejable para detener a un atacante, asegurándose de que esta cuenta señuelo no se bloquea y estableciendo una contraseña segura. Después de crear la cuenta señuelo, debe asegurarse de que no es miembro de ningún grupo de seguridad con privilegios y, a continuación, supervise el uso de la cuenta por si se produce alguna actividad inesperada, como errores de inicio de sesión. Para obtener más información, consulte [Seguridad en grupos administrativos y cuentas de Active Directory](http://www.microsoft.com/technet/security/topics/networksecurity/sec_ad_admin_groups.mspx) en www.microsoft.com/technet/security/topics/networksecurity/sec\_ad\_admin\_groups.mspx.

**Para crear una cuenta Administrador señuelo en un dominio**

1.  Inicie sesión como miembro del grupo Admins. del dominio y abra **Usuarios y equipos de Active Directory**.

2.  Haga clic con el botón secundario del mouse (ratón) en el contenedor **Users**, seleccione **Nuevo** y, a continuación, haga clic en **Usuario**.

3.  En los cuadros **Nombre** y **Nombre de inicio de sesión de usuario**, escriba **Administrador** y, a continuación, haga clic en **Siguiente**.

4.  Escriba una contraseña y confírmela.

5.  Desactive la casilla de verificación **El usuario debe cambiar la contraseña al iniciar una sesión de nuevo** y, a continuación, haga clic en **Siguiente**.

6.  Compruebe que la información de la cuenta señuelo es correcta y, a continuación, haga clic en **Finalizar**.

7.  En el panel de detalles, haga clic con el botón secundario del mouse en **Administrador** y, a continuación, haga clic en **Propiedades**.

8.  Haga clic en la ficha **General**. En el cuadro **Descripción**, escriba **Cuenta para la administración del equipo o dominio** y, a continuación, haga clic en **Aceptar**.

**Para crear una cuenta Administrador señuelo local**

1.  Inicie sesión como miembro del grupo Administradores local y abra la herramienta de complemento **Usuarios locales y grupos** en la consola **Administración de equipos**.

2.  En el árbol de la consola, amplíe **Usuarios locales y grupos**.

3.  Haga clic con el botón secundario del mouse (ratón) en la carpeta **Usuarios** y, a continuación, haga clic en **Nuevo usuario**.

4.  En el cuadro **Nombre de usuario**, escriba **Administrador**. En el cuadro **Descripción**, escriba **Cuenta para la administración del equipo o dominio**.

5.  Escriba una contraseña y confírmela.

6.  Desactive la casilla de verificación **El usuario debe cambiar la contraseña al iniciar una sesión de nuevo**.

7.  Haga clic en **Crear**.

##### Crear una cuenta de administrador secundaria y deshabilitar la cuenta integrada

Aunque no utilice Servicios de Terminal Server para la administración o no permita que los usuarios no administrativos tengan acceso a los servidores, se recomienda crear un usuario adicional como cuenta de administrador secundaria para administrar los servidores. Debe convertir a este usuario en miembro del grupo Administradores. Después de crear la cuenta secundaria, puede deshabilitar la cuenta Administrador integrada.

**Para crear una cuenta de administrador secundaria**

1.  Inicie sesión como administrador y, a continuación, abra **Usuarios y equipos de Active Directory**.

2.  Haga clic con el botón secundario del mouse (ratón) en el contenedor **Users**, seleccione **Nuevo** y, a continuación, haga clic en **Usuario**.

3.  En **Nombre** y **Nombre de inicio de sesión de usuario**, escriba &lt;*nombre de usuario*&gt;y, a continuación, haga clic en **Siguiente**.

4.  Escriba una contraseña segura y confírmela.

5.  Desactive la casilla de verificación **El usuario debe cambiar la contraseña al iniciar una sesión de nuevo** y, a continuación, haga clic en **Siguiente**.

6.  Compruebe que la información de cuenta es correcta y, a continuación, haga clic en **Finalizar**.

7.  En el panel de detalles, haga clic con el botón secundario del mouse (ratón) en *nombre de usuario* y, a continuación, haga clic en **Propiedades**.

8.  Haga clic en la ficha **Miembro de**, haga clic en **Agregar**, escriba **administradores**, haga clic en **Comprobar nombres**y, a continuación, en **Aceptar**.

9.  Vuelva a hacer clic en **Aceptar** para cerrar la página **Propiedades**.

**Para deshabilitar la cuenta Administrador integrada**

1.  Inicie sesión con la cuenta de administrador secundario que acaba de crear y abra **Usuarios y equipos de Active Directory**.

2.  Haga clic en el contenedor **Users**, haga clic con el botón secundario del mouse (ratón) en el nombre de la cuenta Administrador integrada y, a continuación, haga clic en **Propiedades**.

3.  Haga clic en la ficha **Cuenta**.

4.  En **Opciones de cuenta**, desplácese hacia abajo y, a continuación, active la casilla de verificación **Cuenta deshabilitada**.

5.  Haga clic en **Aceptar**.

**Advertencia:** Debe estar seguro de que existe otra cuenta que tiene los privilegios de administrador adecuados cuando deshabilite la cuenta Administrador integrada. Si deshabilita la cuenta sin asegurarse de que hay disponible otra cuenta, puede perder el control administrativo del dominio, lo que puede requerir una operación de restauración o nueva instalación del sistema.

##### Habilitar el bloqueo de la cuenta para inicios de sesión de administrador remotos

Una forma de impedir que los piratas informáticos utilicen las credenciales de contraseña y de cuenta de administrador integrada es permitir que la cuenta de administrador esté bloqueada en la red por una directiva de cuenta después de que se produzca un número determinado de errores de inicio de sesión. De forma predeterminada, la cuenta de administrador integrada no se puede bloquear; no obstante, se puede utilizar **passprop.exe**, un programa de la línea de comandos del *kit de recursos de Microsoft Windows 2000 Server*, para habilitar el bloqueo de inicios de sesión remotos que utilizan la cuenta de administrador. Cuando se ejecuta la utilidad **passprop** con el modificador /ADMINLOCKOUT, la cuenta de administrador se somete a las directivas de bloqueo de cuenta. En Windows 2000 Server, esto sólo se aplica a los inicios de sesión remotos y debido a que la cuenta de administrador integrada nunca se puede bloquear en su equipo local, este programa permite proteger la cuenta de administrador de ataques a través de la red pero sigue permitiendo el acceso interactivo.

**Advertencia:** en Windows Server 2003, **passprop** permite que la cuenta de administrador integrada se bloquee en los inicios de sesión interactivos así como en los remotos.

Puede utilizar los siguientes modificadores de bloqueo de cuenta con **passprop**:

passprop \[/adminlockout\] \[/noadminlockout\]

El modificador /adminlockout mantiene el bloqueo del administrador.

El modificador /noadminlockout quita el bloqueo del administrador.

![](images/Cc162797.note(es-es,TechNet.10).gif)**Nota:** cuando se habilita esta configuración, y la cuenta se bloquea, ningún usuario puede realizar administración remota con la cuenta de administrador.

##### Crear una contraseña de administrador segura

Utilice una contraseña segura para la cuenta Administrador integrada. Una contraseña segura minimiza la amenaza de que un atacante averigüe la contraseña y obtenga las credenciales de la cuenta Administrador. Una contraseña de cuenta de administrador segura debe:

-   Contener 15 caracteres como mínimo.

-   No contener un nombre de cuenta, nombre real o nombre de compañía.

-   No contener una palabra de diccionario completa, ni siquiera de argot o jerga, en ningún idioma.

-   Ser considerablemente distinta de las contraseñas anteriores. Las contraseñas que incluyen un incremento (Contraseña1, Contraseña2, Contraseña3, ...) no son seguras.

-   Contener caracteres, como mínimo, de tres de los cinco grupos enumerados en la tabla siguiente.

**Tabla 3.1 Tipos de caracteres para una contraseña de administrador segura**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipos de caracteres</p></th>
<th><p>Ejemplo</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Letras mayúsculas</p></td>
<td style="border:1px solid black;"><p>A, B, C ...</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Letras minúsculas</p></td>
<td style="border:1px solid black;"><p>a, b, c ...</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Números</p></td>
<td style="border:1px solid black;"><p>0, 1, 2, 3 ...</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Símbolos de teclado no alfanuméricos</p></td>
<td style="border:1px solid black;"><p>` ~ ! @ # $ % ^ &amp; * ( ) _ + - = { } | [ ] \ : &quot; ; ' &lt; &gt; ? , . /</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Caracteres Unicode</p></td>
<td style="border:1px solid black;"><p>€, G, ƒ, ?</p></td>
</tr>  
</tbody>  
</table>
  
##### Utilizar frases cifradas en vez de contraseñas
  
La forma de crear una contraseña segura que no tenga que anotar consiste en utilizar una frase cifrada. Una frase cifrada es fundamentalmente una frase que puede recordar, como "Mi hijo Juan es tres años mayor que mi hija Ana". Puede crear una contraseña razonablemente segura con la primera letra de cada palabra de la frase. Por ejemplo, "mhjetamqmha". No obstante, puede crear una contraseña todavía más segura con una combinación de mayúsculas y minúsculas, números y caracteres especiales que parezcan letras. Por ejemplo, si utiliza la misma frase fácil de recordar y unos cuantos trucos, la contraseña ahora sería MhJe3@mqmh@.
  
Aunque las frases cifradas son vulnerables a los ataques de diccionario, la mayoría del software de averiguación de contraseñas comercial no comprueba las contraseñas de más de 14 caracteres. Si los usuarios utilizan frases cifradas largas, es menos probable que se averigüen sus contraseñas y resultan más fáciles de recordar que las contraseñas seguras tradicionales. También es menos probable que los usuarios anoten las contraseñas si son fáciles de recordar. A continuación se ofrecen buenos ejemplos de una frase cifrada segura:
  
-   ¡H0y he c0mido 4 s@lchich@s!
  
-   ¡Re@lmente quiero c0mprar 11 Perros!
  
Estos ejemplos contienen más de 20 caracteres, son frases cifradas muy largas e incluyen caracteres de cuatro de los cinco grupos posibles. No son frases muy conocidas, pero son más fáciles de recordar que una contraseña de 15 caracteres que tuviera una combinación alfanumérica de caracteres no relacionados, símbolos y signos de puntuación que no tienen un significado intrínseco.
  
##### No utilizar contraseñas de administrador en blanco o poco seguras
  
Aunque supone un riesgo importante para la seguridad, algunas organizaciones tienen contraseñas poco seguras o en blanco para las cuentas de administrador. Las contraseñas en blanco o poco seguras representan una de las vulnerabilidades más habituales en una red y uno de los puntos de acceso más sencillo para los intrusos.
  
Cuando se establecen contraseñas en blanco o poco seguras para la cuenta de administrador, los usuarios malintencionados puede obtener acceso mediante el uso de combinaciones básicas, como “Administrador” para el nombre de usuario o un valor en blanco o “administrador” para la contraseña. Las contraseñas en blanco y poco seguras sucumben rápidamente a los intentos de averiguación de contraseñas y son vulnerables a los ataques de diccionario, que prueban metódicamente una palabra tras otra, y los ataques de fuerza bruta, que utilizan una lista de caracteres comunes, como A-Z y 0-9, en combinaciones lineales.
  
Aunque una buena contraseña no puede garantizar que un intruso no obtenga acceso a la red, proporciona una excelente defensa de primera línea.
  
##### Utilizar contraseñas seguras
  
Debe asegurarse de que los administradores de red de la organización utilizan contraseñas seguras. En Windows 2000 Server y Windows Server 2003, puede utilizar Directiva de grupo para aplicar el uso de contraseñas seguras.
  
Para obtener información acerca de las contraseñas seguras, consulte las notas del producto [Aplicación del uso de contraseñas seguras en las organizaciones](http://www.microsoft.com/smallbusiness/gtm/securityguidance/articles/enforce_strong_passwords.mspx) en www.microsoft.com/smallbusiness/gtm/securityguidance/articles/enforce\_strong\_passwords.mspx y [Contraseñas seguras](http://www.microsoft.com/smallbusiness/gtm/securityguidance/articles/select_sec_passwords.mspx) en www.microsoft.com/smallbusiness/gtm/securityguidance/articles/select\_sec\_passwords.mspx.
  
##### Cambiar las contraseñas de administrador periódicamente
  
Debe cambiar las contraseñas de las cuentas con privilegios periódicamente. El intervalo entre cada cambio se debe determinar según las consecuencias que el riesgo de la cuenta supongan para la organización. Para obtener directrices acerca de cómo se pueden determinar estas consecuencias, consulte la [Guía de administración de riesgos de seguridad](http://www.microsoft.com/technet/security/guidance/secrisk/default.mspx)**en www.microsoft.com/technet/security/guidance/secrisk/default.mspx.
  
Debe cambiar periódicamente las contraseñas de las cuentas de administrador locales. Puede automatizar este proceso para los servidores y estaciones de trabajo con la herramienta **cusrmgr.exe** incluida en el *kit de recursos de Microsoft Windows 2000 Server*. Para obtener más información acerca de cómo utilizar **cusrmgr.exe**, consulte el artículo de Knowledge Base [How to Use the Cusrmgr.exe Tool to Change Administrator Account Password on Multiple Computers](http://support.microsoft.com/kb/272530) en http://support.microsoft.com/kb/272530.
  
También debe cambiar la contraseña del administrador de Modo de restauración de servicios de directorio (DSRM) en los controladores de dominio de forma periódica. Windows 2000 emplea la utilidad **setpwd** para restablecer la contraseña DSRM. En Windows Server 2003, la herramienta **Ntdsutil** ofrece esa funcionalidad. Puede utilizar estas herramientas de forma remota.
  
##### Detectar automáticamente contraseñas poco seguras
  
Las contraseñas poco seguras y en blanco suponen un peligro importante para la seguridad global de la red de una organización. Las organizaciones deben crear o adquirir software que detecte o pruebe automáticamente contraseñas en blanco y poco seguras.
  
Estos tipos de herramientas emplean dos enfoques básicos:
  
-   **Múltiples intentos de inicio de sesión en línea a través de la red mediante contraseñas poco seguras comunes**. Microsoft Baseline Security Analyzer (MBSA) constituye un ejemplo de este tipo de herramienta. No es el método recomendado porque la metodología en línea puede provocar la denegación de servicio si se habilitan los bloqueos de cuenta.
  
-   **Análisis de contraseñas sin conexión**. Hay disponibles algunas buenas herramientas de análisis sin conexión de terceros que pueden contribuir a reducir el riesgo de seguridad de una organización al permitir a los administradores que identifiquen y solucionen vulnerabilidades de seguridad derivadas de contraseñas poco seguras o que se puedan averiguar fácilmente. Normalmente estas herramientas buscan contraseñas poco seguras y, a continuación, proporcionan valoración de calidad de contraseña, información y capacidades de corrección. Éste es el método recomendado para probar contraseñas poco seguras.
  
Después de identificar una cuenta con una contraseña en blanco o poco segura, la respuesta a la incidencia debe seguir el protocolo de respuesta a incidencias establecido de la organización. Algunos ejemplos de protocolo de respuesta a incidencias son:
  
-   El sistema automatizado restablece la contraseña de la cuenta por una contraseña segura.
  
-   El sistema automatizado envía un mensaje de correo electrónico al propietario del servidor para solicitar un restablecimiento de contraseña.
  
Esta última respuesta puede prolongar el período de vulnerabilidad del servidor.
  
##### Analizar contraseñas con Microsoft Baseline Security Analyzer
  
Puede utilizar la herramienta [Microsoft Baseline Security Analyzer (MBSA)](http://www.microsoft.com/technet/security/tools/mbsahome.mspx), disponible en www.microsoft.com/technet/security/tools/mbsahome.mspx, para analizar todos los equipos de la red y buscar contraseñas poco seguras.
  
Entre otras pruebas de seguridad, MBSA puede enumerar todas las cuentas de usuario y comprobar los siguientes puntos débiles de las contraseñas:
  
-   La contraseña está en blanco
  
-   La contraseña es la misma que el nombre de la cuenta de usuario
  
-   La contraseña es la misma que el nombre de equipo
  
-   La contraseña utiliza la palabra "contraseña"
  
-   La contraseña utiliza la palabra "admin" o "administrador"
  
Como resultado del análisis, esta comprobación también informa de las cuentas deshabilitadas o bloqueadas actualmente.
  
Para realizar esta prueba, MBSA intenta cambiar la contraseña en su equipo de destino utilizando cada una de estas contraseñas. MBSA no restablece ni cambia permanentemente la contraseña, pero avisa si la contraseña no es lo suficientemente segura y, por lo tanto, representa un riesgo de seguridad.
  
##### Utilizar credenciales administrativas sólo en equipos de confianza
  
Asegúrese de que los administradores de la organización nunca utilizan sus credenciales administrativas para iniciar sesión en un equipo en el que carezcan de control total. En un equipo puede haber ejecutándose un capturador de teclado o pantalla que capture las credenciales de contraseña del administrador.
  
Un capturador de teclado es un programa de software espía silencioso que se ejecuta en segundo plano en un equipo de un usuario. Los programadores de software espía diseñan sus capturadores de teclado para que estén en modo oculto mientras registran todas las pulsaciones sin el consentimiento o el conocimiento del usuario. A continuación, esta información se almacena para recuperarla más adelante o transmitirla al autor del capturador de teclado para que la examine. Los capturadores de teclado pueden registrar todas las pulsaciones, incluida información personal como contraseñas o números de tarjeta de crédito. También pueden registrar todo el correo electrónico redactado o las sesiones de charla en línea.
  
Un capturador de pantalla captura los datos basados en caracteres de un equipo o programa; para esto, examina el contenido de una pantalla que no está diseñada realmente para el transporte de datos o su inspección por parte de programas y, a continuación, lo presenta con un formato de interfaz gráfica de usuario (GUI) más fácil de entender. Los capturadores de pantalla más recientes presentan la información en HTML, por lo que se puede tener acceso a la información con un explorador.
  
##### Auditar las cuentas y contraseñas periódicamente
  
Las auditorías periódicas contribuyen a garantizar la integridad de la seguridad de dominio y a proteger contra la elevación de privilegios. La elevación de privilegios puede proporcionar a las cuentas de usuario privilegios administrativos no autorizados. A menos que proteja las capacidades administrativas, los atacantes pueden provocar vulnerabilidades y eludir las medidas de seguridad. Por ejemplo, los atacantes que dispongan de privilegios administrativos pueden crear cuentas de usuario ficticias, agregar cuentas a grupos, elevar los privilegios de las cuentas que ya existen, agregar o modificar directivas y deshabilitar opciones de seguridad.
  
Debe auditar a todos los usuarios y grupos administrativos de nivel de dominio y a todos los usuarios y grupos administrativos de servidores confidenciales de forma periódica. Debido a que los administradores pueden disponer de la capacidad, pero no de la autoridad, para realizar modificaciones en sus propias cuentas administrativas, las organizaciones deben garantizar que las cuentas cumplen la directiva de seguridad de los usuarios administrativos de nivel de dominio. Es importante auditar el uso de estas credenciales con privilegios y comprender que la auditoría no es una simple comprobación de la seguridad de las contraseñas. La auditoría también resulta útil para averiguar las tareas que han llevado a cabo las cuentas administrativas. Utilice Visor de sucesos para consultar los registros de seguridad que se han creado después de configurar y habilitar la auditoría. Las auditorías también pueden detectar cuentas administrativas de nivel de dominio que no se utilizan. Las cuentas administrativas de nivel de dominio inactivas suponen una vulnerabilidad para el entorno de red, en concreto si un atacante las pone en peligro sin que se advierta. Debe quitar todas las cuentas y grupos de administradores de nivel de dominio que no se utilicen.
  
##### Prohibir la delegación de cuentas
  
Debe designar todas las cuentas de usuario administrador de nivel de dominio como **La cuenta es importante y no se puede delegar**. Esta acción contribuye a impedir que se suplanten las credenciales mediante un servidor marcado como de **confianza para la delegación**.
  
La autenticación delegada se produce cuando un servicio de red acepta una solicitud de un usuario y supone la identidad de dicho usuario para iniciar una nueva conexión a un segundo servicio de red. La autenticación delegada resulta útil para aplicaciones de varios niveles que utilizan capacidades de inicio de sesión único en varios equipos. Por ejemplo, se confía automáticamente en los controladores de dominio para la delegación. Si habilita el sistema de cifrado de archivos (EFS) en un servidor de archivos, el servidor debe ser de confianza para la delegación con el fin de almacenar los archivos cifrados en nombre de los usuarios. La autenticación delegada también resulta útil para los programas en los que Servicios de Internet Information Server (IIS) admite una interfaz Web a una base de datos que se ejecuta en otro equipo, como Microsoft Outlook® Web Access (OWA) en Microsoft Exchange Server o para las páginas de compatibilidad de inscripción Web para una entidad emisora de certificados de empresa si las páginas se alojan en otro servidor Web.
  
Debe denegar el derecho a participar en la autenticación delegada a las cuentas de equipo en Active Directory, a los equipos que no son seguros físicamente y a las cuentas de administrador de dominio. Las cuentas de administrador de dominio tienen acceso a recursos confidenciales y, si se ponen en peligro, suponen un alto riesgo para la organización. Para obtener más información, consulte el tema [Enabling Delegated Authentication](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/deployguide/en-us/dsscc_aut_vwcs.asp)**en el [kit de implementación de Windows Server 2003](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/depkit/c283b699-6124-4c3a-87ef-865443d7ea4b.mspx) en www.microsoft.com/resources/documentation/WindowsServ/2003/all/deployguide/en-us/dsscc\_aut\_vwcs.asp.
  
##### Controlar el proceso de inicio de sesión administrativa
  
Los miembros de los grupos Administradores, Administradores de organización y Admins. del dominio representan las cuentas con más privilegios de cada dominio. Para minimizar los riesgos de seguridad, adopte las medidas descritas en las secciones siguientes de esta guía para aplicar credenciales administrativas seguras.
  
##### Solicitar tarjetas inteligentes para el inicio de sesión administrativo
  
A los administradores de dominio se les debe solicitar el uso de autenticación de dos factores para todas sus funciones administrativas. La autenticación de dos factores requiere dos partes:
  
-   Algo que el usuario tiene, como una tarjeta inteligente.
  
-   Algo que el usuario sabe, como un número de identificación personal (PIN).
  
Solicitar ambos factores reduce los riesgos de un acceso no autorizado mediante credenciales de factor único compartidas, robadas o duplicadas, como los nombres de usuario y las contraseñas.
  
La autenticación de dos factores es un elemento importante cuando se protegen las cuentas de administrador de dominio porque los nombres de usuario y las contraseñas convencionales son credenciales de texto libre que, por lo general, se componen de juegos de caracteres de lenguaje natural. Como tales, un usuario malintencionado puede robarlas, compartirlas o duplicarlas si:
  
-   Un usuario de confianza comparte su contraseña con un usuario no autorizado o registra la contraseña de un modo no seguro (por ejemplo, una nota adherida al monitor).
  
-   La contraseña se transmite en formato de texto sin cifrar.
  
-   Se utiliza un dispositivo de hardware o software para capturar datos del teclado durante el inicio de sesión.
  
Si se requiere a los administradores que utilicen tarjetas inteligentes para los inicios de sesión interactivos, se exige a los usuarios administrativos que dispongan físicamente de las tarjetas para iniciar la sesión y se garantiza el uso de contraseñas seguras cifradas generadas de modo aleatorio en sus cuentas de usuario. Estas contraseñas seguras protegen del robo de contraseñas poco seguras con el fin de obtener acceso administrativo.
  
Puede aplicar el uso de tarjetas inteligentes si habilita la opción de cuenta **La tarjeta inteligente es necesaria para un inicio de sesión interactivo** para cada cuenta de usuario administrativo.
  
El PIN de la tarjeta inteligente es un código cifrado que cada propietario de tarjeta establece y almacena en ella. El PIN es una cadena que el usuario debe facilitar cuando se autentica con la tarjeta inteligente para utilizar la clave privada. Cada clave privada de una tarjeta inteligente es única, lo que garantiza la singularidad de la autenticación.
  
La autenticación de tarjeta inteligente resulta muy importante cuando un administrador de dominio utiliza el inicio de sesión interactivo. Las tarjetas inteligentes facilitan las tareas a los administradores de dominio que están encargados de varios servidores y cada uno de los cuales necesita autenticación. En vez de obligar a los administradores a disponer de una contraseña independiente por cada servidor en el que deben autenticarse, puede proteger los servidores con tarjetas inteligentes exclusivas que compartan un PIN común.
  
![](images/Cc162797.note(es-es,TechNet.10).gif)**Nota:** Windows 2000 Server admite el uso de tarjetas inteligentes para el acceso remoto; no obstante, se necesita Windows Server 2003 para poder utilizar tarjetas inteligentes para cuentas de nivel de dominio. También se necesita Windows Server 2003 para utilizar credenciales de tarjeta inteligente con el comando **runas** del servicio de inicio de sesión secundario.
  
La implementación de tarjetas inteligentes para administradores de dominio y la adopción de los principios y prácticas que se describen en esta guía pueden servir para que las organizaciones mejoren la seguridad de sus activos de red.
  
Para obtener más información acerca del uso de tarjetas inteligentes para la autenticación, consulte los recursos siguientes:
  
-   [The Smart Card Deployment Cookbook](http://technet.microsoft.com/es-es/library/dd277386.aspx), en el sitio Web de Microsoft TechNet en www.microsoft.com/technet/security/topics/smrtcard/smrtcdcb/default.mspx.
  
-   [Planning a Smart Card Deployment](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/depkit/f65c054e-4cb3-4a6e-84f6-8a9787819df5.mspx), en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/DepKit/f65c054e-4cb3-4a6e-84f6-8a9787819df5.mspx.
  
##### Compartir credenciales de inicio de sesión para cuentas administrativas importantes
  
Por cada cuenta que considere importante, por ejemplo, una que sea miembro de los grupos Administradores de organización o Administradores de dominio del dominio raíz del bosque, asigne dos usuarios que compartan dicha cuenta con el fin de que ambos estén presentes para iniciar la sesión correctamente con ella. Cuando se comparten estas cuentas, se proporciona una auditoría visual inherente: Un usuario observa las acciones que lleva a cabo el otro. También se evita que un usuario inicie la sesión por su cuenta para tener acceso al equipo como administrador con el objeto de poner en peligro su seguridad como administrador malintencionado o en una situación de coacción.
  
Puede implementar cuentas administrativas compartidas que utilicen contraseñas o tarjetas inteligentes además de números PIN. Si utiliza credenciales basadas en contraseña para las cuentas administrativas, divida la contraseña entre los dos usuarios que comparten dicha cuenta para que cada uno conozca sólo la mitad de la contraseña. Cada usuario es responsable de mantener su mitad de la contraseña. Por ejemplo, puede crear una cuenta administrativa denominada Admin1 y asignarle dos usuarios de confianza, María y Roberto, para compartir esta cuenta. Cada usuario mantiene la mitad de la contraseña. Para que uno de ellos inicie la sesión y utilice la cuenta, el otro debe estar presente para especificar la otra mitad de la contraseña.
  
El inconveniente de la opción de cuenta administrativa compartida es que existe una falta inherente de responsabilidad en la auditoría. Las organizaciones necesitarán disponer de otro sistema de control, como cámaras de vigilancia, para garantizar que los usuarios no realizan un uso abusivo de estos privilegios compartidos.
  
Si utiliza credenciales basadas en tarjeta inteligente para las cuentas administrativas, divida la propiedad de la tarjeta inteligente y su PIN entre los dos usuarios que comparten la cuenta para que un usuario sea el propietario físico de la tarjeta inteligente y el otro mantenga el PIN. De este modo, ambos usuarios deben estar presentes para iniciar sesión en la cuenta.
  
##### Restringir el modo y el lugar donde los administradores de dominio pueden iniciar sesión
  
Las organizaciones deben restringir el modo y el lugar donde un administrador de nivel de dominio puede iniciar sesión. Si así lo requiere su tarea o función, los administradores pueden iniciar sesión interactivamente en los controladores de dominio en los que tienen privilegios, pero se debe seguir solicitando la autenticación de dos factores.
  
Se debe prohibir a los administradores de dominio que inicien sesión en cualquier equipo no esté aprobado específicamente para el uso de administradores de dominio en los siguientes casos:
  
-   Cuando se utilicen inicios de sesión interactivos
  
-   Cuando se utilice Escritorio remoto
  
-   Cuando se inicie sesión como un servicio
  
-   Cuando se inicie sesión como un trabajo por lotes
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 4: Resumen
  
Debido a sus permisos y privilegios inherentes, las cuentas de administrador de los equipos son las cuentas más útiles y, al mismo tiempo, las potencialmente más peligrosas del equipo.
  
Las organizaciones deben poner un énfasis especial en la protección de las cuentas de administrador de nivel de dominio, pues un intruso que pueda poner en peligro la cuenta de un administrador de dominio podría obtener acceso a todos los equipos de sus dominios y bosques. Microsoft ha definido pasos para proteger las cuentas de administrador de dominio en su red corporativa y apremia a otras organizaciones a hacer lo mismo.  
  
Debe seguir las prácticas recomendadas que se describen esta guía para administrar la red y adherirse a sus principios para reducir el riesgo de que usuarios no autorizados puedan obtener acceso administrativo a los activos confidenciales de la red y a los datos del servicio de directorio Active Directory®.
  
Mejorar lo máximo posible la seguridad de las cuentas de administrador es una iniciativa importante para las organizaciones que desean proteger sus activos de la red.
  
[](#abcg)[Próximos pasos](#abcg)  
[](#abch)[Lecturas adicionales](#abch)  
#### Próximos pasos
  
Si una organización todavía no ha implementado un programa para garantizar la seguridad de las cuentas de administrador, en esta guía de planeamiento se facilitan las bases para planear un programa de este tipo.
  
Los principales pasos que deben seguir las organizaciones para garantizar la seguridad de las cuentas de administrador son los siguientes:
  
-   Definir un proceso para reducir el riesgo de amenazas en la cuenta de administrador.
  
-   Identificar estrategias para mejorar la seguridad de las cuentas administrativas en Active Directory.
  
-   Utilizar el principio de privilegios mínimos.
  
-   Separar las funciones Administrador de dominio y Administrador de organización.
  
-   Utilizar el servicio de inicio de sesión secundario para separar las cuentas de usuario y de administrador.
  
-   Seguir las directrices de prácticas recomendadas para mejorar la seguridad de las cuentas de administrador.
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Lecturas adicionales
  
La integridad de un programa para proteger las cuentas de administrador depende de su mantenimiento a largo plazo. Para obtener más información acerca de las prácticas operativas recomendadas consulte el sitio Web de [Microsoft® Operations Framework (MOF)](http://technet.microsoft.com/es-es/library/bb232042.aspx) en www.microsoft.com/technet/itsolutions/techguide/mof/default.mspx.
  
Esta guía para mejorar la seguridad de las cuentas de administrador constituye esencialmente una recopilación de las prácticas recomendadas de Microsoft. Para tener acceso a consideraciones adicionales de prácticas recomendadas para proteger su infraestructura de Active Directory, consulte los recursos siguientes:
  
-   Para obtener más información acerca de cómo garantizar la seguridad de los controladores de dominio, consulte [Consolidación de la seguridad de los controladores de dominio Windows Server 2003](http://www.microsoft.com/technet/security/guidance/secmod120.mspx) de la *Guía de seguridad de Windows Server™ 2003* en www.microsoft.com/technet/security/guidance/secmod120.mspx.
  
-   Para obtener información acerca de cómo mejorar la seguridad de Windows Server 2003, descargue la [Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14846) en http://go.microsoft.com/fwlink/?linkid=14846.
  
-   Para obtener más información acerca de las contraseñas de cuenta y las directivas en Windows Server 2003, consulte las notas del producto "[Account Passwords and Policies](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/bpactlck.mspx)" en www.microsoft.com/technet/prodtechnol/windowsserver2003/  
    technologies/security/bpactlck.mspx.
  
-   Para obtener más información acerca de cómo planear, crear y mantener un programa de administración de riesgos de seguridad correcto, consulte la [Guía de administración de riesgos de seguridad](http://www.microsoft.com/technet/security/guidance/secrisk/default.mspx) en www.microsoft.com/technet/security/guidance/secrisk/default.mspx.
  
-   Para obtener más información acerca de una utilización más segura y coherente de las contraseñas, consulte los siguientes documentos del Centro de instrucciones de seguridad:
  
    -   "[Aplicación del uso de contraseñas seguras en las organizaciones](http://www.microsoft.com/smallbusiness/gtm/securityguidance/articles/enforce_strong_passwords.mspx)" en www.microsoft.com/smallbusiness/gtm/securityguidance/  
        articles/enforce\_strong\_passwords.mspx.
  
    -   "[Contraseñas seguras](http://www.microsoft.com/smallbusiness/gtm/securityguidance/articles/select_sec_passwords.mspx)" en www.microsoft.com/smallbusiness/gtm/securityguidance/  
        articles/select\_sec\_passwords.mspx.
  
-   Para obtener más información acerca de la seguridad de Active Directory, consulte:
  
    -   [Best Practice Guide for Securing Windows Server Active Directory Installations](http://www.microsoft.com/windowsserver2003/techinfo/overview/adsecurity.mspx) (Windows Server 2003) en el sitio Web de Microsoft en www.microsoft.com/windowsserver2003/techinfo/overview/adsecurity.mspx.
  
    -   [Best Practices for Delegating Active Directory Administration](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/directory/activedirectory/actdid1.mspx) en www.microsoft.com/technet/prodtechnol/windowsserver2003/  
        technologies/directory/activedirectory/actdid1.mspx.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Agradecimientos
  
El grupo Microsoft Solutions for Security (MSS) y Security Center of Excellence (SCOE) desean agradecer y reconocer la labor realizada por el equipo que elaboró la *Guía de planeamiento de la seguridad de las cuentas de administrador*. Las personas que se citan a continuación fueron responsables directos o contribuyeron de forma decisiva en la redacción, elaboración y comprobación de esta solución.
  
#### Autores
  
Steve Ryan, *Content Master*
  
Lee Walker
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Editores
  
Deborah Jay, *Content Master*
  
Jennifer Kerns, *Content Master*
  
Frank Manning, *Volt*
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Revisores
  
Bill Canning
  
Chase Carpenter
  
Fernando Cima
  
David Cross
  
Mike Danseglio
  
Kurt Dillard
  
Jesper Johansson
  
Matt Kestian
  
Claudio Vacalebre
  
Shain Wray
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Directores del programa
  
Neil Bufton, *Content Master*
  
Chase Carpenter
  
Alison Woolford, *Content Master*
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Comprobadores
  
Ashish Java, *Infosys Technologies*
  
Mehul Mediwala, *Infosys Technologies*
  
Gaurav Singh Bora, *Infosys Technologies*
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Administrador de versiones
  
Flicka Crandell
  
[](#mainsection)[Principio de la página](#mainsection)
  
#### Colaboradores
  
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
  
Bivin Pachatt *Vidyatech Solutions*
  
Tessa Porterfield
  
Vivek Manohar Prabhu, *Vidyatech Solutions*
  
Stacey Tsurusaki, *Volt*
  
David Visintainer, *Volt*
  
Vikas Walia, *Vidyatech Solutions*
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**  
[![](images/Cc162797.icon_exe(es-es,TechNet.10).gif) Guía de planeamiento de supervisión de la seguridad y detección de ataques](http://go.microsoft.com/fwlink/?linkid=41316)
  
[](#mainsection)[Principio de la página](#mainsection)
