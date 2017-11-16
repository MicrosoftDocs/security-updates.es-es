---
TOCTitle: 'Capítulo 2: Mecanismos de seguridad de Windows Server 2003'
Title: 'Capítulo 2: Mecanismos de seguridad de Windows Server 2003'
ms:assetid: '7cc50ea6-80d8-4ef6-81de-f47a60ebf8fa'
ms:contentKeyID: 20200242
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163110(v=TechNet.10)'
---

Guía de Seguridad de Windows Server 2003
========================================

### Capítulo 2: Mecanismos de seguridad de Windows Server 2003

Actualizado: 27/12/05

### En esta página

[](#eeaa)[Información general](#eeaa)
[](#edaa)[Seguridad con el Asistente para configuración de seguridad](#edaa)
[](#ecaa)[Seguridad de los servidores con la directiva de grupo de Active Directory](#ecaa)
[](#ebaa)[Información general del proceso](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Información general

Este capítulo ofrece información sobre los mecanismos que se pueden utilizar para implementar la configuración de seguridad en Microsoft® Windows Server™ 2003. El Service Pack 1 (SP1) de Windows Server 2003 proporciona el Asistente para configuración de seguridad (SCW), una nueva herramienta basada en funciones que puede utilizar para hacer que los servidores sean más seguros. Si se usa junto con objetos de directiva de grupo (GPO), SCW permite lograr un mayor control, flexibilidad y coherencia en el proceso de seguridad.

Este capítulo se centra en los temas siguientes:

-   Cómo se utiliza SCW para crear, probar e implementar directivas de seguridad basadas en funciones.

-   Cómo el servicio de directorio de Active Directory® facilita una seguridad coherente en la empresa a través del uso de objetos GPO.

-   Cómo el diseño de dominio de Active Directory, de unidades organizativas (UO), de la directiva de grupo y de grupos administrativos afecta a las implementaciones de seguridad.

-   Cómo utilizar tanto SCW como la directiva de grupo para crear un enfoque administrable basado en funciones para reforzar la seguridad de los servidores que ejecutan el SP1 de Windows Server 2003.

Esta información proporciona una base y una perspectiva que puede utilizar para evolucionar un entorno de Cliente heredado (LC) a uno de Seguridad especializada: Funcionalidad limitada (SSLF) dentro de una infraestructura del dominio.

[](#mainsection)[Principio de la página](#mainsection)

### Seguridad con el Asistente para configuración de seguridad

El propósito de SCW es proporcionar un proceso flexible paso a paso para reducir la superficie de ataque de los servidores que ejecutan Windows Server 2003 con SP1. SCW es realmente una colección de herramientas que se combina con una base de datos de reglas XML. Su objetivo es ayudar a los administradores a determinar de una forma rápida y precisa la funcionalidad mínima necesaria para las funciones de servidores específicos.

Con SCW, los administradores pueden escribir, probar, solucionar problemas e implementar directivas de seguridad que deshabiliten toda la funcionalidad secundaria. También proporciona la capacidad de revertir directivas de seguridad. SCW ofrece compatibilidad nativa para la administración de directivas de seguridad en servidores individuales, así como en grupos de servidores que comparten funcionalidad relacionada.

SCW es una herramienta completa que puede ayudarle a realizar las tareas siguientes:

-   Determinar qué servicios deben estar activos, qué servicios deben ejecutarse cuando proceda y qué servicios se pueden deshabilitar

-   Administrar el filtrado de puertos de red en combinación con el Firewall de Windows

-   Controlar qué extensiones web de IIS se permiten para los servidores web

-   Reducir la exposición de protocolo a los protocolos basados en el bloque de mensajes de servidor (SMB), NetBIOS, el sistema común de archivos de Internet (CIFS) y el Protocolo ligero de acceso a directorios (LDAP)

-   Crear útiles directivas de auditoría que capturen los eventos de interés

Hay disponibles instrucciones detalladas acerca de cómo instalar, utilizar y solucionar problemas de SCW en la versión descargable de la documentación del [Asistente para configuración de seguridad](http://www.microsoft.com/downloads/details.aspx?familyid=903fd496-9eb9-4a45-aa00-3f2f20fd6171&displaylang=en) en www.microsoft.com/downloads/details.aspx?FamilyID=903fd496-9eb9-4a45-aa00-3f2f20fd6171&displaylang=en.

**Nota**: SCW sólo se puede usar con Windows Server 2003 con SP1. No se puede utilizar para crear directivas para Windows 2000 Server, Windows XP ni Windows Small Business Server 2003. Para reforzar la seguridad de un número considerable de equipos que ejecutan estos sistemas operativos, deberá aprovechar las ventajas que ofrecen los mecanismos de seguridad basados en la directiva de grupo que se describen más adelante en este capítulo.

#### Creación y prueba de directivas

Puede utilizar SCW para crear y probar rápidamente las directivas de seguridad de varios servidores o grupos de servidores desde un único equipo. Esta capacidad le permite administrar las directivas de toda la empresa desde una ubicación. Estas directivas proporcionan medidas de seguridad compatibles y coherentes que son apropiadas para las funciones que cada servidor proporciona dentro de la organización. Si utiliza SCW para crear y probar las directivas, debe implementar SCW en todos los servidores de destino. Aunque cree la directiva en una estación de administración, SCW intentará comunicarse con los servidores de destino para inspeccionar su configuración y ajustar la directiva resultante.

SCW se integra con los subsistemas IPSec y Firewall de Windows, y modificará esa configuración según proceda. Salvo que se impida, SCW configurará el Firewall de Windows de modo que se permita tráfico de red entrante en los puertos importantes que el sistema operativo necesita, así como escuchar las aplicaciones. Si se necesitan filtros de puerto adicionales, SCW puede crearlos. Como resultado, las directivas creadas por SCW dan respuesta a la necesidad de que las secuencias de comandos personalizadas establezcan o modifiquen filtros IPSec para bloquear el tráfico no deseado. Esta capacidad simplifica la administración de seguridad de la red. La configuración de filtros de red para servicios que utilizan puertos RPC o dinámicos también se pueden simplificar.

SCW proporciona también la capacidad de personalizar en gran medida las directivas creadas. Esta flexibilidad le ayuda a crear una configuración que, además de permitir la funcionalidad necesaria, ayuda a reducir los riesgos de seguridad. Además de los comportamientos y la configuración de línea de base, puede invalidar SCW en las áreas siguientes:

-   Servicios

-   Puertos de red

-   Aplicaciones aprobadas por el Firewall de Windows

-   Configuración del Registro

-   Configuración de IIS

-   Inclusión de plantillas de seguridad previamente existentes (archivos .inf)

SCW aconseja al administrador acerca de algunos de los valores de configuración del Registro más importantes. Para reducir la complejidad de la herramienta, los diseñadores decidieron incluir sólo la configuración que más afecta a la seguridad. Sin embargo, en esta guía se explican muchos otros valores de configuración del Registro. Para contrarrestar las limitaciones de SCW, puede combinar plantillas de seguridad con los resultados de SCW con el fin de crear una configuración más completa.

Al utilizar SCW para crear una directiva nueva, se usa la configuración actual de un servidor como configuración inicial. Por lo tanto, debe centrarse en un servidor del mismo tipo que los servidores en los que pretende implementar la directiva para que pueda describir con precisión la configuración de las funciones del servidor. Al utilizar la interfaz gráfica de usuario (GUI) de SCW para crear una directiva nueva, se crea un archivo XML y se guarda en la carpeta **%systemdir%\\security\\msscw\\Policies** de forma predeterminada. Después de crear las directivas, puede utilizar la interfaz gráfica de usuario de SCW o la herramienta de línea de comandos Scwcmd para aplicar las directivas a los servidores de prueba.

Cuando pruebe las directivas, es posible que deba quitar directivas que ha implementado. Puede utilizar la interfaz gráfica de usuario o la herramienta de línea de comandos para revertir la última directiva que ha aplicado a un servidor o grupo de servidores. SCW guarda la configuración previa en archivos XML.

Para las organizaciones que dispongan de recursos limitados para diseñar y probar las configuraciones de seguridad, SCW puede ser suficiente. Esas organizaciones que carecen de dichos recursos ni tan siquiera deben intentar reforzar la seguridad de los servidores, ya que dichos esfuerzos a menudo conllevan problemas inesperados y una pérdida de productividad. Si su organización no dispone de experiencia ni de tiempo para tratar este tipo de problemas, debe centrarse en otras actividades de seguridad importantes, como las actualizaciones de las aplicaciones y los sistemas operativos a las versiones actuales y la administración de las actualizaciones.

#### Implementación de directivas

Dispone de tres opciones para implementar las directivas:

-   Aplicar la directiva con la interfaz gráfica de usuario de SCW

-   Aplicar la directiva con la herramienta de línea de comandos Scwcmd

-   Convertir la directiva de SCW en un objeto de directiva de grupo y vincularlo a un dominio o UO

Cada opción tiene sus propias ventajas e inconvenientes, que se describen en las subsecciones siguientes.

### Aplicación de la directiva con la interfaz gráfica de usuario de SCW

La ventaja principal de la opción de la interfaz gráfica de usuario de SCW es la sencillez. La interfaz gráfica de usuario permite a los administradores seleccionar fácilmente una directiva predefinida y aplicarla a un único equipo.

La desventaja de la opción de la interfaz gráfica de usuario de SCW es que sólo permite la aplicación de directivas a un solo equipo a la vez. Esta opción no es por tanto muy válida para entornos grandes y en esta guía no se utiliza este método.

### Aplicación de la directiva con la herramienta de línea de comandos Scwcmd

Una forma de aplicar directivas nativas de SCW a varios equipos sin Active Directory es usar la herramienta Scwcmd. También puede combinar el uso de Scwcmd con tecnologías de secuencias de comandos para proporcionar un nivel de implementación automático de directivas, tal vez como parte de un proceso existente que se utilice para crear e implementar servidores.

La desventaja principal de usar la opción de Scwcmd es que el proceso no es automático. Tiene que especificar la directiva y el servidor de destino, bien manualmente o a través de una solución de secuencias de comandos, lo que significa que hay probabilidades de que se inserte la directiva errónea en el equipo equivocado. Si tiene servidores en un grupo con configuraciones ligeramente distintas, tendrá que trabajar con una directiva independiente para cada uno de los equipos y aplicarlas de forma separada. Debido a estas limitaciones, en esta guía no se utiliza este método.

### Conversión de la directiva de SCW en un objeto de directiva de grupo

La tercera opción disponible para implementar directivas de SCW es usar la herramienta Scwcmd para convertir la directiva basada en XML en un objeto de directiva de grupo (GPO). Aunque esta conversión pueda parecer inicialmente un paso innecesario, entre sus ventajas se incluyen las siguientes:

-   Las directivas se replican, implementan y aplican con mecanismos conocidos basados en Active Directory.

-   Al tratarse de objetos GPO nativos, las directivas se pueden usar con unidades organizativas (UO), herencia de directivas y directivas incrementales para ajustar la seguridad de los servidores que tienen una configuración similar aunque no sea exactamente la misma. Mediante la directiva de grupo, los servidores se colocan en una UO secundaria y se aplica una directiva incremental. Sin embargo, con SCW, es necesario crear una directiva nueva para cada configuración.

-   Las directivas se aplican automáticamente a todos servidores colocados en las UO correspondientes. Las directivas nativas de SCW deben aplicarse de forma manual o utilizarse en combinación con una solución de secuencias de comandos.

[](#mainsection)[Principio de la página](#mainsection)

### Seguridad de los servidores con la directiva de grupo de Active Directory

Active Directory permite a las aplicaciones buscar, utilizar y administrar recursos de directorio en un entorno informático distribuido. Aunque la información detallada sobre el diseño de una estructura de Active Directory podría por sí sola llenar un libro completo, en esta sección solamente se tratan brevemente estos conceptos a fin de establecer un contexto para el resto de la guía. Esta información de diseño es necesaria para comprender el uso de la directiva de grupo con el fin de administrar de forma segura los dominios, los controladores de dominio y determinadas funciones de servidor de la organización. Si su organización ya cuenta con un diseño de Active Directory, este capítulo puede brindarle la oportunidad de conocer algunas de las ventajas o posibles problemas relacionados con la seguridad.

Esta guía no ofrece ninguna orientación específica acerca de cómo proteger la base de datos de Active Directory. Para obtener ese tipo de ayuda, consulte el documento "[Best Practice Guide for Securing Active Directory Installations](http://technet.microsoft.com/es-es/library/cc773365.aspx)" (en inglés) al que se hace referencia en la sección "Información adicional" al final de este capítulo.

Al crear una infraestructura de Active Directory, debe considerar minuciosamente los límites de seguridad del entorno. Si planea de forma adecuada una delegación de seguridad y un programa de implementación de la organización, el resultado será un diseño de Active Directory mucho más seguro para la organización. Sólo tiene que reestructurar el diseño para los cambios principales en el entorno, como una adquisición o reorganización.

#### Límites de Active Directory

Existen diversos tipos de límites dentro de Active Directory, que definen el bosque, el dominio, la topología del sitio y la delegación de permisos; estos límites se establecen automáticamente al instalar Active Directory. Sin embargo, debe asegurarse de que los límites de los permisos incorporen los requisitos y las directivas de la organización. La delegación de permisos administrativos puede ser bastante flexible para dar cabida a los distintos requisitos de la organización. Por ejemplo, para mantener un equilibrio adecuado entre la seguridad y la funcionalidad administrativa, puede dividir los límites de delegación de permisos en límites de seguridad y límites administrativos.

### Límites de seguridad

Este tipo de límite permite definir la autonomía o aislamiento de diferentes grupos dentro de una organización. Resulta difícil establecer el equilibrio entre garantizar una seguridad adecuada, basada en la forma en que se establecen los límites empresariales de la compañía, y la necesidad de continuar ofreciendo un nivel coherente de funcionalidad de base. Para poder lograr este equilibrio, debe contraponer las posibles amenazas que pueden afectar a la organización frente a las repercusiones de seguridad que conlleva la delegación de permisos administrativos y otras opciones relacionadas con la arquitectura de red del entorno.

El bosque es el auténtico límite de seguridad del entorno de red. En esta guía se recomienda crear bosques distintos para que el entorno esté protegido y la seguridad no se vea comprometida por los administradores de otros dominios. Este enfoque también ayuda a garantizar que la seguridad comprometida de un bosque no se traslade a toda la empresa.

Un dominio es un límite de administración de Active Directory, no un límite de seguridad. En una organización de individuos con buenas intenciones, el límite del dominio proporcionará una administración autónoma de los servicios y datos dentro de cada dominio de la organización. Desafortunadamente, por lo que respecta a la seguridad, el aislamiento no es tan fácil de conseguir. El dominio, por ejemplo, no aislará totalmente un ataque de un administrador de dominio malintencionado. Este nivel de separación sólo se puede lograr en el nivel de bosque.

Dentro del dominio, la unidad organizativa (UO) proporciona otro nivel de límite de administración. Las UO proporcionan una manera flexible de agrupar recursos relacionados y delegar el acceso de administración al personal apropiado sin proporcionarles la capacidad de administrar todo el dominio. Al igual que los dominios, las UO no son un auténtico límite de seguridad. Aunque puede asignar permisos a una UO, todas las UO que estén en el mismo dominio autentican los recursos con los recursos del dominio y el bosque. Además, una jerarquía de UO bien diseñada ayudará al desarrollo, la implementación y la administración de medidas de seguridad eficaces.

Puede que su organización necesite considerar la división del control administrativo de los servicios y datos dentro del diseño actual de Active Directory. Un diseño eficaz de Active Directory exige un conocimiento profundo de los requisitos de la organización en cuanto a la autonomía y el aislamiento tanto de servicios como de datos.

### Límites administrativos

Dada la posible necesidad de segmentar servicios y datos, es preciso definir los distintos niveles de administración necesarios. Aparte de los administradores que puedan realizar servicios exclusivos para la organización, se recomienda considerar los siguientes tipos de administradores.

#### Administradores de servicios

Los administradores de servicios de Active Directory son los encargados de configurar y distribuir el servicio de directorio. Así, por ejemplo, estos administradores mantienen los servidores de los controladores de dominio, controlan los parámetros de configuración de todo el directorio y garantizan la disponibilidad del servicio. Los administradores de Active Directory de la organización se deben considerar los administradores de servicios.

La configuración del servicio de Active Directory viene determinada a menudo por los valores de atributo. Estos valores se corresponden con la configuración de los objetos correspondientes que se almacenan en el directorio. Por tanto, los administradores de servicios de Active Directory también lo son de los datos. Es posible que debido a las necesidades de su organización tenga que considerar otros grupos de administradores de servicios para el diseño del servicio de Active Directory. Algunos ejemplos son:

-   Un grupo de administración de dominio que sea el principal responsable de los servicios de directorio.

    El administrador del bosque selecciona el grupo que administrará cada dominio. Debido al alto nivel de acceso que se otorga a los administradores de cada dominio, éstos deberán ser personas de un alto grado de confianza. Los administradores de dominios controlan los dominios a través del grupo **Administradores de dominio** y otros grupos integrados.

-   Los grupos de administradores que administran DNS.

    El grupo de administradores de DNS realiza el diseño de DNS y administra la infraestructura del mismo. El administrador de DNS supervisa la infraestructura de DNS a través del grupo **Administradores de DNS**.

-   Los grupos de administradores que administran las unidades organizativas (UO).

    El administrador de UO designa un grupo o una persona como administrador de cada UO. El administrador de UO administra los datos almacenados dentro de la UO asignada de Active Directory. Estos grupos pueden controlar la forma en que se delega la administración y el modo en el que se aplica a objetos dentro de las UO. Asimismo, los administradores de UO pueden crear nuevos subárboles y delegar la administración de las UO de las que son responsables.

-   Los grupos de administradores que administran los servidores de la infraestructura.

    El grupo responsable de la administración de los servidores de la infraestructura administra la infraestructura de WINS, DHCP y potencialmente DNS. En algunos casos, el grupo que controla la administración del dominio administrará la infraestructura de DNS, ya que Active Directory está integrado en DNS y se almacena y administra en los controladores de dominio.

#### Administradores de datos

Los administradores de datos de Active Directory administran los datos almacenados en Active Directory o en equipos unidos a Active Directory. Estos administradores no tienen ningún control sobre la configuración o distribución del servicio de directorio. Estos administradores forman parte de un grupo de seguridad que crea la organización. En algunos casos, los grupos de seguridad predeterminados en Windows no tienen sentido en todas las situaciones de la organización. Por tanto, las organizaciones pueden desarrollar sus propias normas y significados de nomenclatura para los grupos de seguridad que mejor se adapten a su entorno. Algunas de las tareas diarias de los administradores de datos incluyen:

-   Controlar un subconjunto de objetos en el directorio. A través del control de acceso al nivel de atributo heredado, se puede otorgar a los administradores de datos el control de secciones muy concretas del directorio, sin que lleguen a tener de por sí el control completo de la configuración del servicio.

-   Administrar equipos miembro del directorio y los datos que contienen.

**Nota**: en numerosos casos, los valores de atributo de los objetos almacenados en el directorio determinan la configuración del servicio del directorio.

En resumen, antes de permitir que los propietarios de las estructuras del directorio y el servicio de Active Directory se unan a una infraestructura de bosque o de dominio, la organización debe tener confianza en todos los administradores de servicios del bosque y de todos los dominios. Asimismo, los programas de seguridad de las empresas deben desarrollar directivas y procedimientos estándar para que se realicen comprobaciones exhaustivas de los administradores. En el contexto de esta guía de seguridad, confiar en los administradores de servicios implica:

-   Creer razonablemente que los administradores de servicios protegerán los intereses que sean mejores para la organización. Las organizaciones no deberán elegir unirse a un bosque o dominio si existen motivos legítimos para pensar que los propietarios actúan de forma malintencionada contra la organización.

-   Creer razonablemente que los administradores de servicios pondrán en práctica las mejores recomendaciones y limitarán el acceso físico a los controladores de dominio.

-   Comprender y aceptar los riesgos para la organización que conlleva la posibilidad de:

    -   **Administradores deshonestos:** los administradores de confianza se pueden volver deshonestos y abusar de los privilegios que tienen en la red. Un administrador deshonesto dentro de un bosque podría consultar fácilmente el identificador de seguridad (SID) de un administrador de otro dominio. Este administrador podría entonces utilizar una herramienta de interfaz de programación de aplicaciones (API), un editor de discos o un depurador para agregar el SID robado a la lista SID History de una cuenta dentro de su propio dominio. Con el SID robado agregado a esta lista, el administrador deshonesto tendría privilegios administrativos en el dominio del SID robado, así como en su propio dominio.

    -   **Administradores coaccionados:** un administrador de confianza podría verse coaccionado u obligado a realizar operaciones que pongan en peligro la seguridad de un equipo o la red. Un usuario o administrador podría aplicar técnicas sociales de ingeniería u otro tipo de amenazas físicas o daños sobre los administradores legítimos de un equipo a fin de obtener la información que necesita para obtener acceso al equipo.

Puede que algunas organizaciones acepten el riesgo de una infracción en la seguridad llevada a cabo por un administrador deshonesto o coaccionado desde otra parte de la organización. En este caso, dichas organizaciones deberían determinar si las ventajas tanto en el nivel de colaboración como de ahorro de costos que supone la participación en una infraestructura compartida compensan este riesgo. Sin embargo, otras organizaciones no podrán aceptar el riesgo de las graves consecuencias que supondrían las infracciones en la seguridad.

#### Active Directory y la directiva de grupo

Aunque las UO ofrecen una forma fácil de agrupar equipos, usuarios, grupos y otras entidades principales de seguridad, también constituyen un mecanismo eficaz para la segmentación de los límites administrativos. Además, las UO proporcionan una estructura crucial para la implementación de objetos de directiva de grupo (GPO), ya que pueden segmentar los recursos según la necesidad de seguridad y le permiten ofrecer una seguridad diferente según las distintas UO. El uso de UO para administrar y asignar directivas de seguridad basadas en la función de servidor es una parte integral de la arquitectura de seguridad general de la organización.

### Delegación de administración y aplicación de Directiva de grupo

Las UO son contenedores dentro de la estructura de directorios de un dominio. Estos contenedores pueden incluir cualquier entidad principal de seguridad del dominio, aunque normalmente se utilizan para contener objetos de un tipo específico. Para conceder o revocar permisos de acceso a UO a un grupo o usuario individual, puede establecer listas de control de acceso (ACL) específicas en la UO y los permisos los heredarán todos los objetos de la UO.

Puede utilizar una UO para proporcionar capacidades administrativas basadas en funciones. Por ejemplo, un grupo de administradores podría ser responsable de las UO de usuario y grupo, mientras otro grupo podría administrar las UO que contienen los servidores. También se puede crear una UO que contenga el grupo de servidores de recursos que administrarán otros usuarios a través de un proceso denominado delegación de control. Este enfoque proporciona al grupo delegado un control autónomo sobre una UO concreta, pero no los aísla del resto del dominio.

Es probable que los administradores que delegan el control sobre determinadas UO sean administradores de servicios. En un nivel de autoridad inferior, los usuarios que controlan las UO son generalmente administradores de datos.

### Grupos administrativos

Los administradores pueden crear grupos administrativos para segmentar clústeres de usuarios, grupos de seguridad o servidores en contenedores para la administración autónoma.

Por ejemplo, considere los servidores de infraestructura que residen en un dominio. Estos servidores incluyen todos los controladores que no son de dominio que ejecutan servicios de red básicos, incluidos los servidores que proporcionan servicios WINS y DHCP. A menudo, un grupo de operaciones o un grupo de administración de infraestructura mantiene estos servidores. Puede utilizar una UO para proporcionar de una forma sencilla capacidades administrativas a estos servidores.

En la siguiente figura se ofrece una vista de alto nivel de esta configuración de UO.

![](images/Cc163110.sgfg0201(es-es,TechNet.10).gif)

**Figura 2.1 Delegación de administración de UO**

Cuando al grupo de **administración de infraestructura** se le delega el control de la UO Infraestructura, los miembros de este grupo tendrán un control total de dicha UO y de todos los servidores y objetos de la misma. Esta capacidad permite a los miembros del grupo proteger las funciones de servidor con la directiva de grupo.

Este enfoque es solamente uno de los métodos de utilizar las UO para proporcionar una segmentación administrativa. En el caso de organizaciones más complejas, consulte la sección "Información adicional" al final de este capítulo.

**Nota:** como Active Directory depende en gran medida de DNS, es habitual ejecutar el servicio DNS en los controladores de dominio. Los controladores de dominio se colocan de forma predeterminada en la UO integrada denominada Controladores de dominio. Los ejemplos de esta guía siguen esta práctica y, por tanto, la función del servidor de infraestructura no incluye el servicio DNS.

### Aplicación de Directiva de grupo

Utilice Directiva de grupo y delegue la administración para aplicar parámetros, derechos y comportamientos específicos en todos los servidores dentro de una UO. Al utilizar Directiva de grupo en lugar de realizar los pasos manualmente, resulta sencillo actualizar varios servidores con cualquier cambio adicional que pueda ser necesario.

Las directivas de grupo se acumulan y se aplican en el orden mostrado en la siguiente figura.

[![](images/Cc163110.sgfg0202(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163110.sgfg0202_big(es-es,technet.10).gif)

**Figura 2.2 Jerarquía de aplicación de GPO**

Como se ha visto en la figura, las directivas se aplican en primer lugar en el nivel de directiva local del equipo. A continuación, todos los GPO se aplican en el nivel del sitio y, a continuación, en el nivel de dominio. Si el servidor se anida en varias UO, se aplican primero los GPO existentes en la UO de máximo nivel. El proceso de aplicación de GPO continúa hacia abajo en la jerarquía de UO. El último GPO en aplicarse es el del nivel secundario de UO que contiene el objeto de servidor. El orden de prioridad para el procesamiento de la directiva de grupo va desde la UO de nivel superior (la más alejada de la cuenta de usuario o equipo) hasta la de nivel inferior (que en realidad contiene la cuenta de usuario o equipo).

Tenga en cuenta las siguientes consideraciones básicas cuando aplique la directiva de grupo:

-   Debe establecer el orden de aplicación de GPO para los niveles de directiva de grupo con varios GPO. Si varias directivas especifican la misma opción, la última aplicada tendrá prioridad.

-   Debe configurar una directiva de grupo con la opción **No reemplazar** si no desea que otros GPO la reemplacen. Si utiliza la Consola de administración de directivas de grupo (GPMC) para administrar los GPO, el nombre de esta opción es **Forzado**.

### Configuración de la hora

Muchos servicios de seguridad, especialmente la autenticación, se basan en un reloj preciso de un equipo para realizar los trabajos. Asegúrese de que la hora del equipo es exacta y de que todos los servidores de la organización usan el mismo recurso de hora. El servicio W32Time de Windows Server 2003 proporciona sincronización de la hora para los equipos basados en Windows Server 2003 y Microsoft Windows XP que se ejecutan en un dominio Active Directory.

El servicio W32Time sincroniza los relojes de los equipos basados en Windows Server 2003 con los controladores de un dominio. El protocolo Kerberos y otros protocolos de autenticación necesitan esta sincronización para funcionar adecuadamente. El funcionamiento correcto de varios componentes de la familia de servidores de Windows Server depende de si la hora es exacta y está sincronizada. Si los relojes no están sincronizados en los clientes, el protocolo de autenticación Kerberos podría denegar el acceso a usuarios.

Otra ventaja importante que aporta la sincronización de la hora es la correlación de los eventos en todos los clientes de la empresa. La sincronización de los relojes de los clientes del entorno garantiza que se puedan analizar correctamente los eventos que tienen lugar de forma secuencial uniforme en los clientes de la organización.

El servicio W32Time utiliza el Protocolo de tiempo de la red (NTP) para sincronizar los relojes de los equipos que ejecutan Windows Server 2003. En un bosque de Windows Server 2003, la hora se sincroniza de forma predeterminada de la siguiente manera:

-   El maestro de operaciones emulador del controlador principal de dominio (PDC) del dominio raíz del bosque es el recurso de hora autorizado de la organización.

-   Todos los maestros de operaciones PDC de los demás dominios del bosque siguen la jerarquía de dominios cuando seleccionan un emulador PDC para sincronizar su hora.

-   Todos los controladores de un dominio sincronizan su hora con el maestro de operaciones emulador de PDC de su dominio como su asociado de hora de entrada.

-   Todos los servidores miembro y equipos de escritorio cliente utilizan la autenticación del controlador de dominio como su asociado de tiempo de entrada.

Para garantizar que la hora es exacta, el emulador PDC del dominio raíz del bosque se puede sincronizar con un recurso de hora autorizado, como un recurso NTP confiable o un reloj de elevada exactitud de la red. Tenga en cuenta que la sincronización de NTP utiliza el puerto UDP 123. Antes de realizar una sincronización con un servidor externo, debe valorar las ventajas de abrir este puerto frente al posible riesgo de seguridad que supone.

Además, si realiza la sincronización con un servidor externo que no controla, existe el riesgo de configurar los servidores con la hora incorrecta. Un atacante podría comprometer el servidor externo o suplantar su identidad para manipular con fines malintencionados los relojes de los equipos. Como se explicó anteriormente, el protocolo de autenticación Kerberos requiere que los relojes de los equipos estén sincronizados. Si no lo están, podría producirse una denegación de servicio.

### Administración de plantillas de seguridad

Las plantillas de seguridad son archivos basados en texto que se pueden usar para aplicar una configuración de seguridad a un equipo. Se pueden modificar con el complemento Plantillas de seguridad de Microsoft Management Console (MMC) o con un editor de texto como Bloc de notas. Algunas secciones de los archivos de plantilla contienen listas de control de acceso (ACL) específicas, escritas en el lenguaje de definición de descriptores de seguridad (SDDL). Hay disponible más información acerca de cómo editar las plantillas de seguridad y SDDL en la página sobre el [lenguaje de definición de descriptores de seguridad](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/secauthz/security/security_descriptor_definition_language.asp) de Microsoft MSDN® en http://msdn.microsoft.com/library/
en-us/secauthz/security/security\_descriptor\_definition\_language.asp.

De forma predeterminada, los usuarios autenticados tienen derecho de lectura de toda la configuración que se incluye en un objeto de directiva de grupo. Por tanto, es muy importante almacenar las plantillas de seguridad de un entorno de producción en una ubicación segura a la que sólo puedan tener acceso los administradores que implementan la directiva de grupo. La finalidad de esto no es impedir que se vean los archivos \*.inf, sino evitar que se realicen cambios no autorizados en las plantillas de seguridad de origen.

Todos los equipos que ejecutan Windows Server 2003 almacenan las plantillas de seguridad en la carpeta **%SystemRoot%\\security\\templates**. Esta carpeta no se replica entre los diversos controladores de dominio, así que tendrá que designar una ubicación para almacenar la copia maestra de las plantillas de seguridad con el fin de evitar que se produzcan problemas de control de versión con las plantillas. Una vez modificada la plantilla que se encuentra en la ubicación central, puede volver a implementarla en los equipos apropiados. De este modo, siempre modificará la misma copia de las plantillas.

### Eventos de aplicaciones de GPO con éxito

Aunque un administrador puede comprobar manualmente toda la configuración para garantizar que se ha aplicado correctamente a los servidores de la organización, también debería aparecer un evento en el registro de eventos que informe al administrador de que la directiva de dominio se ha descargado correctamente en cada uno de los servidores. En el registro de aplicación deberá aparecer un evento similar al siguiente con su propio número de Id. de evento:

**Tipo**: Información

**Id. de origen**: SceCli

**Id. de evento**: 1704

**Descripción:** Se ha aplicado satisfactoriamente la directiva de seguridad en los objetos de directiva de grupo.

De forma predeterminada, la configuración de seguridad se actualiza cada 90 minutos en una estación de trabajo o servidor y cada 5 minutos en un controlador de dominio. Verá este tipo de evento si se ha producido algún cambio durante estos intervalos. Además, la configuración se actualiza cada 16 horas, ya se realicen cambios o no. También puede forzar manualmente la configuración de directiva de grupo para realizar una actualización mediante el procedimiento descrito más adelante en este capítulo.

### Unidades organizativas de funciones de servidor

En el ejemplo anterior se mostró una manera de administrar los servidores de infraestructura de una organización. Este método se puede hacer extensivo a otros servidores y servicios de una organización. Los objetivos son crear una directiva de grupo perfecta para todos los servidores y garantizar que los servidores que residen dentro de Active Directory cumplen los estándares de seguridad del entorno.

Este tipo de directiva de grupo constituye una línea de base coherente para la configuración estándar de todos los servidores de la organización. Además, la estructura de UO y la aplicación de directivas de grupo deben ofrecer un diseño detallado a fin de proporcionar una configuración de seguridad para los tipos de servidores específicos de una organización. Por ejemplo, Internet Information Server (IIS), los servicios de archivos y impresión, el Servicio de autenticación de Internet (IAS) y los Servicios de Certificate Server son algunas de las funciones de servidor de una organización que puede que necesiten directivas de grupo exclusivas.

**Importante**: para que resulte más sencillo, en los ejemplos de este capítulo se supone que se utiliza el entorno Cliente de empresa (EC). Si utiliza uno de los otros dos entornos, sustituya los nombres de archivo correspondientes. Las diferencias entre los tres entornos y su funcionalidad se plantean en el capítulo 1, "Introducción a la Guía de seguridad de Windows Server 2003".

#### Directiva de línea de base de servidores miembro

El primer paso para establecer las UO de funciones de servidor consiste en crear una directiva de línea de base. Para crear tal directiva, puede utilizar SCW en un servidor miembro estándar para crear un archivo .xml de línea de base de servidores miembro. Como parte de la creación del archivo XML, use SCW para incluir una de las plantillas de seguridad de línea de base de servidores miembro proporcionadas: LC-Member Server Baseline.inf, EC-Member Server Baseline.inf o SSLF-Member Server Baseline.inf.

Una vez generada la directiva SCW, ésta se convierte en un GPO y se vincula a las UO de los servidores miembro. Este nuevo GPO de línea de base aplicará la configuración de la directiva de grupo de línea de base a cualquier servidor que forme parte de la UO Servidores miembro, así como cualquier servidor de las UO secundarias. La directiva de línea de base de servidores miembro se trata en el capítulo 4, "Directiva de línea de base de servidores miembro".

Debe definir la configuración que desea para la mayoría de los servidores de la organización en la directiva de grupo de línea de base. Aunque es posible que haya algunos servidores a los que no desee aplicar la directiva de línea de base, estos no deben ser muchos. Si crea su propia directiva de grupo de línea de base, hágala lo más restrictiva posible y segmente todos los servidores que deban ser distintos de esta directiva en UO específicas de servidor independientes.

#### Tipos de funciones y unidades organizativas de servidores

Cada función de servidor identificada requiere una directiva de SCW, una plantilla de seguridad y una UO, además de la UO de línea de base. Este enfoque permite la creación de directivas distintas para los cambios incrementales que cada función necesita.

En un ejemplo anterior, los servidores de infraestructura se colocaron en la UO** **Infraestructura, que es una unidad organizativa secundaria de la UO Servidores miembro. El siguiente paso consiste en aplicar la configuración adecuada a estos servidores. Esta solución proporciona tres plantillas de seguridad, una para cada entorno de seguridad: LC-Infrastructure Server.inf, EC-Infrastructure Server.inf y** **SSLF-Infrastructure Server.inf. Si estas plantillas se utilizan junto con SCW, podrá crear una directiva de seguridad que contenga los ajustes específicos que DHCP y WINS necesitan. La directiva resultante se convierte luego en un nuevo GPO y se vincula a la UO Infraestructura.

Este GPO usa la configuración **Grupos restringidos** para agregar los tres grupos siguientes al grupo de **administradores locales** de todos los servidores de la UO Infraestructura:

-   **Administradores de dominio**

-   **Administradores de organización**

-   **Administradores de infraestructura**

Como se mencionó anteriormente en este capítulo, este enfoque es solamente una de las múltiples maneras que existen para crear una estructura de UO para implementar los GPO. Para obtener más información acerca de cómo crear UO para la implementación de la directiva de grupo, consulte el capítulo "[Diseñar la estructura de Active Directory](http://www.microsoft.com/resources/documentation/windows/2000/server/reskit/en-us/deploy/dgbd_ads_heqs.asp?frame=true)" y los temas relacionados en www.microsoft.com/resources/documentation/Windows/2000/server/reskit/
en-us/deploy/dgbd\_ads\_heqs.asp?frame=true.

En la siguiente tabla se incluyen las funciones de servidor y los archivos de plantilla correspondientes que se han definido en esta guía para Windows Server 2003. Los nombres de archivo de las plantillas de seguridad llevan el prefijo variable *&lt;Env&gt;*, que se reemplazará por LC (Cliente heredado), EC (Cliente de empresa) o SSLF (Seguridad especializada: Funcionalidad limitada) según corresponda.

**Tabla 2.1 Funciones de servidor de Windows Server 2003**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Función de servidor</th>
<th style="border:1px solid black;" >Descripción</th>
<th style="border:1px solid black;" >Nombre de archivo de la plantilla de seguridad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Servidor miembro</td>
<td style="border:1px solid black;">Todos los servidores que son miembros del dominio y residen en la UO Servidores miembro o en UO secundarias.</td>
<td style="border:1px solid black;"><em>&lt;Env&gt;-</em>Member Server Baseline.inf<br />
</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Controlador de dominio</td>
<td style="border:1px solid black;">Todos los controladores de dominio de Active Directory. Estos servidores son también servidores DNS.</td>
<td style="border:1px solid black;"><em>&lt;Env&gt;-</em>Domain Controller.inf<br />
</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servidor de infraestructura</td>
<td style="border:1px solid black;">Todos los servidores WINS y DHCP bloqueados.</td>
<td style="border:1px solid black;"><em>&lt;Env&gt;-</em>Infrastructure Server.inf<br />
</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servidor de archivos</td>
<td style="border:1px solid black;">Todos los servidores de archivos bloqueados.</td>
<td style="border:1px solid black;"><em>&lt;Env&gt;-</em>File Server.inf</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servidor de impresión</td>
<td style="border:1px solid black;">Todos los servidores de impresión bloqueados.</td>
<td style="border:1px solid black;"><em>&lt;Env&gt;-</em>Print Server.inf</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servidor web</td>
<td style="border:1px solid black;">Todos los servidores web de IIS bloqueados.</td>
<td style="border:1px solid black;"><em>&lt;Env&gt;-</em>Web Server.inf</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Servidor IAS</td>
<td style="border:1px solid black;">Todos los servidores IAS bloqueados.</td>
<td style="border:1px solid black;"><em>&lt;Env&gt;-</em>IAS Server.inf</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servidor de Servicios de Certificate Server</td>
<td style="border:1px solid black;">Todos los servidores de entidad de certificación (CA) bloqueados.</td>
<td style="border:1px solid black;"><em>&lt;Env&gt;-</em>CA Server.inf</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Host de baluarte</td>
<td style="border:1px solid black;">Todos los servidores expuestos a Internet.</td>
<td style="border:1px solid black;"><em>&lt;Env&gt;-</em>Bastion Host.inf</td>
</tr>
</tbody>
</table>
  
Todos los archivos de plantilla, excepto los de los servidores host de baluarte, se aplican a las UO secundarias correspondientes. Cada una de estas UO secundarias requieren que se aplique la configuración específica para definir la función que cumplirá cada equipo en la organización.
  
Los requisitos de seguridad de cada una de estas funciones de servidor son distintos. La configuración de seguridad correspondiente de cada función se trata con mayor detalle en los siguientes capítulos. Tenga en cuenta que no todas las funciones tienen plantillas que se correspondan con todos los entornos. Por ejemplo, la función de host de baluarte siempre se considera que está en el entorno SSLF.
  
**Importante**: en esta guía se supone que los equipos con Windows Server 2003 realizarán funciones definidas específicamente. Si los servidores de la organización no coinciden con estas funciones o dispone de servidores con distintas finalidades, utilice la configuración definida aquí como instrucciones base para la creación de sus propias plantillas de seguridad. Sin embargo, tenga en cuenta que cuantas más funciones realicen los servidores, más vulnerables serán a los ataques.
  
En la siguiente figura se muestra un ejemplo de diseño de UO final que es compatible con estas funciones de servidor definidas en el entorno EC.
  
[![](images/Cc163110.sgfg0203(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc163110.sgfg0203_big(es-es,technet.10).gif)
  
**Figura 2.3 Ejemplo de diseño de UO**
  
#### Diseño de UO, GPO y grupos
  
Las UO y directivas recomendadas que se explicaron en la sección anterior crean un entorno de línea de base o nuevo para volver a organizar la estructura existente de UO de los equipos que ejecutan Windows Server 2003 de una organización. Los administradores usan los límites de administración predefinidos para crear los grupos administrativos correspondientes. En la siguiente tabla se muestra un ejemplo de la correlación de estos grupos con las UO que administran.
  
**Tabla 2.2 UO y grupos administrativos**

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Nombre de UO</th>
<th style="border:1px solid black;" >Grupo administrativo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Controladores de dominio</td>
<td style="border:1px solid black;">Ingeniería de dominio</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Servidores miembro</td>
<td style="border:1px solid black;">Ingeniería de dominio</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Infraestructura</td>
<td style="border:1px solid black;">Administraciones de infraestructura</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Archivo</td>
<td style="border:1px solid black;">Administraciones de infraestructura</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Imprimir</td>
<td style="border:1px solid black;">Administraciones de infraestructura</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">IAS</td>
<td style="border:1px solid black;">Ingeniería de dominio</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Web</td>
<td style="border:1px solid black;">Servicios web</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Entidad emisora</td>
<td style="border:1px solid black;">Administradores de organización</td>
</tr>
</tbody>
</table>
  
Los miembros de **Ingeniería de dominio**, que son los responsables de la infraestructura y seguridad de Active Directory, crearon cada uno de los grupos administrativos como un grupo global dentro del dominio. Utilizaron el GPO correspondiente para agregar cada uno de estos grupos administrativos al grupo restringido apropiado. Los grupos administrativos que aparecen en la tabla sólo serán miembros del grupo de **administradores locales** para los equipos ubicados en las UO que contengan específicamente equipos relacionados con sus funciones de trabajo.
  
Por último, los miembros de **Ingeniería de dominio** establecen permisos en cada GPO de modo que sólo los administradores del grupo correspondiente puedan modificarlos.
  
Tenga en cuenta que la creación y configuración de estos grupos es una parte del proceso de diseño e implementación general de Active Directory. No es parte de esta guía.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Información general del proceso
  
En esta guía se combinan las ventajas de los enfoques basados en SCW y en la directiva de grupo. Este enfoque híbrido le permite crear y probar las configuraciones de seguridad de una forma más sencilla, además de proporcionar la flexibilidad y escalabilidad que necesitan las redes Windows de gran tamaño.
  
El proceso utilizado para crear, probar e implementar las directivas es el siguiente:
  
1.  Cree el entorno de Active Directory, incluidos los grupos y las UO. Debe crear los grupos administrativos apropiados y delegar permisos de UO a los grupos correspondientes.
  
2.  Configure la sincronización de hora en el controlador de dominio que aloja el FSMO del emulador PDC.
  
3.  Configure las directivas de dominio.
  
4.  Cree las directivas de línea de base con SCW.
  
5.  Pruebe las directivas de línea de base con SCW.
  
6.  Convierta las directivas de línea de base en GPO y vincúlelas a los GPO apropiados.
  
7.  Cree las directivas de función con SCW y las plantillas de seguridad incluidas.
  
8.  Pruebe las directivas de función con SCW.
  
9.  Convierta las directivas de función en GPO y vincúlelas a los GPO apropiados.
  
En las siguientes secciones se describen estos pasos con más detalle.
  
**Importante**: para que resulte más sencillo, en los ejemplos de esta sección se supone que se utiliza el entorno Cliente de empresa (EC). Si utiliza uno de los otros dos entornos, sustituya los nombres de archivo correspondientes. Las diferencias entre los tres entornos y su funcionalidad se plantean en el capítulo 1, "Introducción a la Guía de seguridad de Windows Server 2003".
  
#### Creación del entorno de Active Directory
  
Para poder empezar el proceso de seguridad, primero debe tener definida una estructura de UO y de dominios de Active Directory apropiada. En el procedimiento siguiente se indican los pasos que deberá seguir para crear las UO y los grupos utilizados en esta guía y configurarlos para que dispongan del acceso administrativo oportuno.
  
1.  Abra el complemento MMC Usuarios y equipos de Active Directory (Dsa.msc).
  
2.  En la raíz del objeto de dominio, cree una UO denominada Servidores miembro.
  
3.  Desplácese a esta nueva UO y cree una UO secundaria dentro de ella denominada Infraestructura.
  
4.  Mueva todos los servidores WINS y DHCP a la UO Infraestructura.
  
5.  Cree un grupo de seguridad global denominado **Administraciones de infraestructura** y agregue las cuentas de dominio apropiadas a él.
  
6.  Ejecute el Asistente para delegación de control para conceder al grupo **Administraciones de infraestructura** control completo de la UO.
  
7.  Repita los pasos del 3 al 6 para las funciones del servidor de archivos, el servidor de impresión, el servidor web, el servidor IAS y el servidor de Servicios de Certificate Server. Utilice la información de la tabla 2.2. relativa a los nombres de UO y grupos correspondientes.
  
#### Configuración de la sincronización de hora
  
En el procedimiento siguiente se garantiza que los controladores de dominio y los servidores miembro estén sincronizados con un recurso de hora externo. Esta sincronización será útil para garantizar que la autenticación Kerberos funciona correctamente y le permitirá mantener sincronizado el dominio de Active Directory con los equipos externos que pueda tener.
  
1.  En el controlador de dominio con el FSMO del emulador PDC, abra una ventana del símbolo del sistema y ejecute el siguiente comando, donde *&lt;PeerList&gt;* es una lista separada por comas de nombres DNS o direcciones IP de los recursos de hora que desee:
  
    ```  
w32tm /config /syncfromflags:manual /manualpeerlist:&lt;PeerList&gt;  
```
  
2.  Para actualizar la configuración, ejecute el comando siguiente:
  
    ```  
w32tm /config /update  
```
  
3.  Compruebe el registro de eventos. Si el equipo no puede alcanzar a los servidores, se produce un error en el procedimiento y se inserta una entrada en el registro de eventos.
  
El uso más frecuente de este proceso es para sincronizar el recurso de hora autorizado de la red interna con un recurso de hora externo de gran precisión. No obstante, este procedimiento se puede ejecutar en cualquier equipo con Windows XP o que sea miembro de la familia Windows Server 2003. Normalmente, no es necesario sincronizar los relojes de todos los servidores con un recurso externo si están sincronizados con el mismo recurso de hora interno. De forma predeterminada, los equipos miembro siempre sincronizan sus relojes con los controladores de dominio.
  
**Nota**: para un análisis exacto del registro, debe sincronizar también los relojes de los equipos de la red que ejecuten otros sistemas operativos que no sean Windows con el emulador PDC de Windows Server 2003 o con el mismo recurso de hora de ese servidor.
  
#### Configuración de la directiva de dominio
  
En el procedimiento siguiente se importan las plantillas de seguridad proporcionadas con esta guía para la directiva de nivel de dominio. Esta directiva se proporciona como una plantilla de seguridad, ya que SCW no se ocupa de las directivas de nivel de dominio. Antes de implementar el siguiente procedimiento, debe encontrar el archivo de directiva (.inf) específico en el equipo.
  
**Advertencia**: las plantillas de seguridad de esta guía se han diseñado para aumentar la seguridad del entorno. Es bastante probable que su instalación cause alguna pérdida de funcionalidad en el entorno y que se produzcan errores en aplicaciones importantes.
  
Resulta **esencial** probar minuciosamente esta configuración antes de implementarla en un entorno de producción. Realice una copia de seguridad de cada controlador de dominio y servidor del entorno antes de aplicar una nueva configuración de seguridad. Asegúrese de que el estado del sistema se incluye en la copia de seguridad, que habilitará la configuración del Registro y restaurará los objetos de Active Directory si es necesario.
  
**Para importar las plantillas de seguridad de directiva de dominio**
  
1.  En Usuarios y equipos de Active Directory, haga clic con el botón secundario en el dominio y, a continuación, seleccione **Propiedades**.
  
2.  En la ficha **Directiva de grupo**, haga clic en **Nuevo** para agregar un nuevo objeto de directiva de grupo (GPO).
  
3.  Escriba **Directiva de dominio de EC** y, a continuación, presione ENTRAR.
  
4.  Haga clic con el botón secundario en **Directiva de dominio de EC** y, a continuación, seleccione **No reemplazar**.
  
5.  Seleccione **Directiva de dominio de EC** y, a continuación, haga clic en **Editar**.
  
6.  En la ventana Editor de objetos de directiva de grupo, haga clic en **Configuración del equipo\\Configuración de Windows**. Haga clic con el botón secundario en **Configuración de seguridad** y, a continuación, seleccione **Importar directiva**.
  
7.  En el cuadro de diálogo **Importar la directiva desde**, navegue hasta **"\\Tools and Templates\\Security Guide\\Security Templates"** y, a continuación, haga doble clic en **EC-Domain.inf**.
  
8.  Cierre la directiva de grupo que se haya modificado.
  
9.  Cierre la ventana **Propiedades de dominio**.
  
10. Si no desea esperar a que se aplique la directiva de grupo programada, puede iniciar el proceso manualmente. Para ello, realice lo siguiente:
  
    -   Abra una ventana del símbolo del sistema, escriba **gpupdate /Force** y presione ENTRAR.
  
11. Compruebe en el registro de eventos que la directiva de grupo se ha descargado correctamente y que el servidor puede comunicarse con los otros controladores de dominio en el dominio.
  
**Advertencia**: al crear la directiva de dominio de EC, asegúrese de que está habilitada la opción **No reemplazar** para que esta directiva se aplique a todo el dominio. Se trata de la única directiva de grupo de esta guía en la que se debe habilitar la opción **No reemplazar**. No habilite esta opción en ninguna de las demás directivas de grupo especificadas en esta guía. Asimismo, no modifique la directiva de dominio predeterminada de Windows Server 2003 por si necesita restaurar la configuración predeterminada.
  
Para asegurarse de que esta nueva directiva de grupo tiene prioridad sobre la directiva predeterminada, colóquela de modo que tenga la máxima prioridad entre los vínculos de GPO.
  
**Importante**: debe importar esta directiva de grupo en todos los dominios adicionales de la organización para garantizar que se aplica de forma coherente la directiva de contraseña. Sin embargo, es frecuente encontrar entornos en los que la directiva de contraseña de dominio raíz es mucho más estricta que la de cualquiera de los demás dominios. También es preciso garantizar que todos los demás dominios que utilizarán esta misma directiva tengan los mismos requisitos empresariales. Debido a que la directiva de contraseñas sólo se puede establecer a nivel de dominios, puede que haya requisitos empresariales o legales que segmenten a algunos de los usuarios en un dominio distinto simplemente para aplicar el uso de una directiva de contraseñas más estricta en dicho grupo.
  
**Para desactivar la opción Permitir que los permisos heredables del primario se propaguen a este objeto y a todos los objetos secundarios**
  
De forma predeterminada, la nueva estructura de UO hereda un gran número de parámetros de seguridad de su contenedor principal. Para cada UO, desactive la casilla de verificación **Permitir que los permisos heredables del primario se propaguen a este objeto y a todos los objetos secundarios.**
  
1.  Abra Usuarios y equipos de Active Directory.
  
2.  Haga clic en **Ver** y, a continuación, en **Características avanzadas** para seleccionar la vista de opciones avanzadas.
  
3.  Haga clic con el botón secundario en la UO apropiada y, a continuación, haga clic en **Propiedades**.
  
4.  Haga clic en la ficha **Seguridad** y, a continuación, en **Opciones avanzadas**.
  
5.  Desactive la casilla de verificación **Permitir que los permisos heredables del primario se propaguen a este objeto y a todos los objetos secundarios. Incluirlos junto con las entradas indicadas aquí de forma explícita.**
  
Quite los grupos innecesarios agregados anteriormente por los administradores y agregue el grupo de dominio que corresponda a cada UO de función de servidor. Conserve la configuración **Control total** para el grupo **Administradores de dominio**.
  
#### Creación de las directivas de línea de base con SCW
  
El siguiente paso consiste en utilizar SCW para crear la directiva de línea de base de servidores miembro.
  
Debe utilizar una instalación nueva del sistema operativo para empezar su trabajo de configuración, lo que garantiza que no haya ninguna configuración heredada ni software de configuraciones previas. Si es posible, utilice hardware similar al que empleará en la implementación para garantizar la máxima compatibilidad posible. La instalación nueva se llama *equipo de referencia*.
  
Durante los pasos de creación de la directiva de línea de base de servidores miembro (MSBP), tenga en cuenta que quitará la función de servidor de archivos de la lista de funciones detectadas. Esta función se configura comúnmente en servidores que no la requieren y se podría considerar un riesgo de seguridad. Para habilitar la función de servidor de archivos para servidores que la requieren, puede aplicar una segunda directiva más adelante en este proceso.
  
**Para crear la directiva de línea de base de servidores miembro (MSBP)**
  
1.  Cree una instalación nueva de Windows Server 2003 con SP1 en un equipo de referencia nuevo.
  
2.  Instale el componente del Asistente para configuración de seguridad en el equipo mediante Panel de control, Agregar o quitar programas, Agregar o quitar componentes de Windows.
  
3.  Una el equipo al dominio.
  
4.  Instale sólo las aplicaciones obligatorias que deben estar en cada servidor en su entorno. Los ejemplos incluyen su software y los agentes de administración, agentes de copia de seguridad en cinta y las utilidades antivirus o contra software espía.
  
5.  Inicie SCW, seleccione **Crear directiva nueva** y vaya al equipo de referencia.
  
6.  Elimine la función de servidor de archivos de las funciones detectadas que se enumeran.
  
7.  Compruebe que las características de cliente detectadas son adecuadas para su entorno.
  
8.  Compruebe que las opciones administrativas detectadas son adecuadas para su entorno.
  
9.  Compruebe que se han detectado todos los servicios adicionales que necesita la línea de base, como los agentes de copia de seguridad o el software antivirus.
  
10. Decida cómo tratar los servicios no especificados en su entorno. Para una mayor seguridad, tal vez desee definir esta configuración como **Deshabilitar**. Debe probar esta configuración antes de implementarla en su red de producción porque puede provocar problemas si los servidores de producción ejecutan servicios adicionales que no están duplicados en su equipo de referencia.
  
11. Revise la configuración de la red y asegúrese de que se han detectado los puertos y aplicaciones adecuados y de que se configurarán como excepciones para el Firewall de Windows.
  
12. Ignore la sección "Configuración del Registro".
  
13. Ignore la sección "Directiva de auditoría".
  
14. Incluya la plantilla de seguridad apropiada (por ejemplo, EC-Member Server Baseline.inf).
  
15. Guarde la directiva con un nombre apropiado (por ejemplo, Member Server Baseline.xml).
  
**Para crear la directiva de controladores de dominio**
  
Debe usar un equipo configurado como controlador de dominio para crear la directiva de controladores de dominio. Puede utilizar un controlador de dominio existente o crear un equipo de referencia y utilizar la herramienta Dcpromo para crear un controlador de dominio para el equipo. Sin embargo, la mayoría de las organizaciones no quieren agregar un controlador de dominio a su entorno de producción porque puede violar su directiva de seguridad. Si utiliza un controlador de dominio existente, asegúrese de que no aplica ningún parámetro con SCW ni modifica su configuración.
  
1.  Instale el componente del Asistente para configuración de seguridad en el equipo mediante Panel de control, Agregar o quitar programas, Agregar o quitar componentes de Windows.
  
2.  Instale sólo las aplicaciones obligatorias que deben estar en cada servidor en su entorno. Los ejemplos incluyen su software y los agentes de administración, agentes de copia de seguridad en cinta y las utilidades antivirus o contra software espía.
  
3.  Inicie la interfaz gráfica de usuario de SCW, seleccione **Crear directiva nueva** y vaya al equipo de referencia.
  
4.  Compruebe que las funciones detectadas son adecuadas para su entorno.
  
5.  Compruebe que las características de cliente detectadas son adecuadas para su entorno.
  
6.  Compruebe que las opciones administrativas detectadas son adecuadas para su entorno.
  
7.  Compruebe que se han detectado todos los servicios adicionales requeridos por su línea de base, como agentes de copia de seguridad o software antivirus.
  
8.  Decida cómo tratar los servicios no especificados en su entorno. Para una mayor seguridad, defina esta configuración de directiva como **Deshabilitada**. Debe probar esta configuración antes de implementarla en la red de producción, ya que se pueden producir problemas si los servidores de producción ejecutan servicios adicionales que no están duplicados en el equipo de referencia.
  
9.  Revise la configuración de la red y asegúrese de que se han detectado los puertos y aplicaciones adecuados y de que se configurarán como excepciones para el Firewall de Windows.
  
10. Ignore la sección "Configuración del Registro".
  
11. Ignore la sección "Directiva de auditoría".
  
12. Incluya la plantilla de seguridad adecuada (por ejemplo, EC-Domain Controller.inf).
  
13. Guarde la directiva con un nombre apropiado (por ejemplo, Domain Controller.xml).
  
#### Realización de pruebas de las directivas de línea de base con SCW
  
Después de crear y guardar las directivas de línea de base, Microsoft recomienda implementarlas en el entorno de prueba. Lo ideal sería que los servidores de prueba tuvieran la misma configuración de hardware y software que los servidores de producción. Este planteamiento le permitirá encontrar y solucionar posibles problemas, como la presencia de servicios imprevistos requeridos por dispositivos de hardware específicos.
  
Hay dos opciones disponibles para probar las directivas. Puede utilizar los servicios de implementación nativos de SCW o implementar las directivas mediante un GPO.
  
Cuando empiece a crear sus directivas, debe considerar la utilización de los servicios de implementación nativos de SCW. Puede utilizar SCW para insertar las directivas en un solo servidor cada vez o usar Scwcmd para insertarlas en un grupo de servidores. El método nativo de implementación ofrece la ventaja de poder deshacer fácilmente las directivas implementadas desde SCW. Esta capacidad puede ser muy útil cuando se hacen varios cambios en las directivas durante el proceso de pruebas.
  
Las directivas probadas para garantizar que se pueden aplicar a los servidores de destino no afectarán negativamente a las funciones importantes. Una vez que haya aplicado los cambios de configuración, deberá comenzar a comprobar la funcionalidad principal del equipo. Por ejemplo, si el servidor se ha configurado como una entidad emisora de certificados (CA), asegúrese de que los clientes puedan solicitar y obtener certificados, descargar una lista de revocación de certificados, etc.
  
Cuando esté satisfecho con la configuración de la directiva, puede utilizar Scwcmd como se muestra en el procedimiento siguiente para convertir las directivas a GPO.
  
Para obtener más información acerca de cómo probar las directivas de SCW, consulte la "[Guía de implementación para el Asistente para configuración de seguridad](http://technet.microsoft.com/es-es/library/cc776871.aspx)"* *en www.microsoft.com/technet/prodtechnol/windowsserver2003/  
library/SCWDeploying/5254f8cd-143e-4559-a299-9c723b366946.mspx,* *así como la versión descargable de la [documentación del Asistente para configuración de seguridad](http://go.microsoft.com/fwlink/?linkid=43450) en http://go.microsoft.com/fwlink/?linkid=43450.
  
#### Conversión de las directivas de línea de base en GPO
  
Una vez probadas minuciosamente las directivas de línea de base, siga los pasos siguientes para convertirlas en GPO y vincularlas a las UO apropiadas:
  
1.  En el símbolo del sistema, escriba lo siguiente:
  
    ```  
scwcmd transform /p:&lt;PathToPolicy.xml&gt; /g:&lt;GPODisplayName&gt;  
```
  
    y, a continuación, pulse Entrar. Por ejemplo:
  
    ```  
 scwcmd transform /p:"C:\\Windows\\Security\\msscw\\Policies\\Infrastructure.xml" /g:"Infrastructure Policy"  
```
  
    **Nota**: la información que se introducirá en el símbolo del sistema se muestra aquí en más de una línea a causa de las limitaciones de pantalla. Esta información debe introducirse en una línea.
  
2.  Utilice la Consola de administración de directivas de grupo para vincular los nuevos GPO creados a la UO apropiada.
  
Observe que, si el archivo de directiva de seguridad de SCW contiene configuración de Firewall de Windows, el Firewall de Windows debe estar activo en el equipo local para que este procedimiento se pueda completar correctamente. Para comprobar que el Firewall de Windows está activo, abra el Panel de control y haga doble clic en **Firewall de Windows**.
  
Deberá realizar una última prueba para asegurarse de que el GPO aplica la configuración deseada. Para completar este procedimiento, confirme que se ha establecido la configuración apropiada y que los servicios no se ven afectados.
  
#### Creación de las directivas de función con SCW
  
El siguiente paso consiste en utilizar SCW para crear las directivas de función para cada servidor miembro.
  
Los pasos para crear las directivas específicas de función son similares a los que ha seguido para crear la directiva de línea de base de servidores miembro (MSBP). Debe utilizar una vez más un equipo de referencia para asegurarse de que no hay ninguna configuración heredada o software de configuración anterior.
  
**Para crear las directivas de función**
  
1.  Cree una instalación nueva de Windows Server 2003 con SP1 en un equipo de referencia nuevo.
  
2.  Instale el componente del Asistente para configuración de seguridad en el equipo mediante Panel de control, Agregar o quitar programas, Agregar o quitar componentes de Windows.
  
3.  Una el servidor nuevo al dominio.
  
4.  Instale sólo las aplicaciones obligatorias que deben estar en cada servidor del entorno. Los ejemplos incluyen su software y los agentes de administración, agentes de copia de seguridad en cinta y las utilidades antivirus o contra software espía.
  
5.  Configure las funciones apropiadas para el equipo. Por ejemplo, si los servidores de destino ejecutarán DHCP y WINS, instale esos componentes. No tienen que estar configurados exactamente igual que los servidores implementados, pero las funciones deben estar instaladas.
  
6.  Inicie SCW.
  
7.  Seleccione **Crear directiva nueva** y vaya al equipo de referencia.
  
8.  Compruebe que las funciones detectadas son adecuadas para su entorno.
  
9.  Compruebe que las características de cliente detectadas son adecuadas para su entorno.
  
10. Compruebe que las opciones administrativas detectadas son adecuadas para su entorno.
  
11. Compruebe que se han detectado todos los servicios adicionales requeridos por la línea de base, como los agentes de copia de seguridad o el software antivirus.
  
12. Decida cómo tratar los servicios no especificados en su entorno. Para una mayor seguridad (y funcionalidad reducida), tal vez desee establecer esta configuración de directiva como **Deshabilitar**, que deshabilitará cualquier servicio nuevo que no se permita de forma explícita con SCW. Debe probar esta configuración antes de implementarla en su red de producción porque puede provocar problemas si los servidores de producción ejecutan servicios adicionales que no están duplicados en su equipo de referencia.
  
13. Confirme todos los cambios de servicio que se indican en la lista.
  
14. Revise la configuración de red y asegúrese de que SCW ha detectado los puertos y las aplicaciones apropiados para configurarlos como excepciones en el Firewall de Windows.
  
15. Ignore la sección "Configuración del Registro".
  
16. Ignore la sección "Directiva de auditoría".
  
17. Si el servidor se configura con la función de servidor web, siga los pasos de la sección "Servicios de Internet Information Server" para asegurarse de que SCW está configurado de modo que sea compatible con las características de IIS necesarias.
  
18. Haga clic en **Incluir plantillas de seguridad** para agregar la plantilla de seguridad apropiada.
  
19. Guarde la directiva con un nombre apropiado.
  
#### Realización de pruebas de las directivas de función con SCW
  
Al igual que con las directivas de línea de base, hay dos maneras diferentes de probar las directivas. Puede utilizar los servicios de implementación nativos de SCW o implementar las directivas mediante objetos GPO. Microsoft también recomienda en este caso implementar las directivas de función en un entorno de prueba antes de usarlas en producción. Este enfoque ayudará a reducir al mínimo el tiempo de inactividad y los errores en el entorno de producción. Después de probar completamente la nueva configuración, puede convertir las directivas en objetos GPO como se muestra en el siguiente procedimiento y aplicarlas a la UO apropiada.
  
#### Conversión de las directivas de función en GPO
  
Una vez probadas minuciosamente las directivas de función, siga los pasos siguientes para convertirlas en objetos GPO y vincularlas a las UO apropiadas:
  
1.  En el símbolo del sistema, escriba lo siguiente:
  
    ```  
scwcmd transform /p:&lt;PathToPolicy.xml&gt; /g:&lt;GPODisplayName&gt;  
```
  
    y, a continuación, pulse Entrar. Por ejemplo:
  
    ```  
 scwcmd transform /p:"C:\\Windows\\Security\\msscw\\Policies\\Infrastructure.xml" /g:"Infrastructure Policy"  
```
  
    **Nota**: la información que se introducirá en el símbolo del sistema se muestra aquí en más de una línea a causa de las limitaciones de pantalla. Esta información debe introducirse en una línea.
  
2.  Utilice la Consola de administración de directivas de grupo para vincular el objeto GPO creado recientemente a la UO apropiada y asegúrese de moverlo a un nivel superior del de la directiva predeterminada de controladores de dominio para que tenga la máxima prioridad.
  
Observe que, si el archivo de directiva de seguridad de SCW contiene configuración de Firewall de Windows, el Firewall de Windows debe estar activo en el equipo local para que este procedimiento se pueda completar correctamente. Para comprobar que el Firewall de Windows está activo, abra el Panel de control y haga doble clic en Firewall de Windows.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Resumen
  
Es necesario que los administradores de seguridad conozcan las ventajas y los inconvenientes de SCW en comparación con los métodos de seguridad convencionales basados en la directiva de grupo para que puedan elegir el método adecuado para el entorno. SCW y la directiva de grupo se pueden utilizar a la vez para crear de una forma rápida y coherente prototipos de directivas que SCW proporciona junto con las funciones de administración e implementación escalable de la directiva de grupo.
  
Es necesario tener en cuenta algunos aspectos relacionados con el diseño al revisar los diseños de los bosques, dominios y UO para proporcionar seguridad a un entorno.
  
Es importante investigar y documentarse sobre los requisitos de aislamiento y autonomía específicos de la organización. La autonomía en cuanto a directivas, el aislamiento operativo y el aislamiento jurídico o legal constituyen en su totalidad razones válidas para considerar diseños de bosques complejos.
  
Es importante que entienda cómo controlar los administradores de servicios. Los administradores de servicio malintencionados pueden suponer un gran riesgo para la organización. A un nivel inferior, los administradores de dominio malintencionados pueden obtener acceso a los datos de cualquier dominio del bosque.
  
Aunque no sea una tarea fácil cambiar el diseño del bosque o de los dominios de una organización, puede que sea necesario tomar medidas para impedir que se produzcan algunos riesgos de seguridad. También es importante planear la implementación de UO en la organización según las necesidades de los administradores de servicios y los administradores de datos. En este capítulo se ha proporcionado información detallada acerca de cómo crear un modelo de UO que sea compatible con el uso de objetos GPO para realizar una administración continuada de las distintas funciones de servidor de la organización.
  
#### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de los temas relacionados con la seguridad de los servidores que ejecutan Windows Server 2003 con SP1.
  
-   Para obtener más información acerca de la seguridad y privacidad en Microsoft, consulte la página sobre [seguridad de Trustworthy Computing](http://www.microsoft.com/mscorp/twc/default.mspx) (en inglés) en www.microsoft.com/mscorp/twc/default.mspx.
  
-   Para ver instrucciones sobre seguridad, consulte la página que contiene los [diez mandamientos de la seguridad](http://www.microsoft.com/technet/archive/community/columns/security/essays/10imlaws.mspx) (en inglés) en www.microsoft.com/technet/archive/community/columns/security/essays/10imlaws.mspx.
  
-   Para obtener instrucciones acerca de cómo proteger la base de datos de Active Directory, consulte el documento "[Best Practice Guide for Securing Active Directory Installations](http://technet.microsoft.com/es-es/library/cc773365.aspx)" (en inglés) en www.microsoft.com/downloads/details.aspx?FamilyID=4e734065-3f18-488a-be1e-f03390ec5f91&.
  
-   Para obtener información sobre aspectos de diseño de Active Directory, consulte la página sobre [consideraciones de diseño para la delegación de la administración en Active Directory](http://www.microsoft.com/technet/prodtechnol/windows2000serv/technologies/activedirectory/plan/addeladm.mspx) (en inglés) en www.microsoft.com/technet/prodtechnol/windows2000serv/technologies/activedirectory/plan/addeladm.mspx.
  
-   Para obtener información acerca de cómo configurar un servidor horario, consulte el artículo de Microsoft Knowledge Base sobre [cómo configurar un servidor horario autorizado en Windows 2000](http://support.microsoft.com/?kbid=216734) en http://support.microsoft.com/?kbid=216734.
  
-   Para obtener información acerca de los puertos de red utilizados por las aplicaciones de Microsoft, consulte el artículo de Microsoft Knowledge Base "[Introducción al servicio y requisitos del puerto de red para el sistema Windows Server](http://support.microsoft.com/kb/832017)" en http://support.microsoft.com/kb/832017.
  
-   Para obtener información acerca de la delegación de permisos de Active Directory, consulte la página sobre [recomendaciones para la delegación de la administración en Active Directory](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/activedirectory/actdid1.mspx) (en inglés) en http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/activedirectory/actdid1.mspx.
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtenga la Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14846)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener más información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?asunto=guía%20de%20seguridad%20de%20windows%20server%202003)
  
[](#mainsection)[Principio de la página](#mainsection)
