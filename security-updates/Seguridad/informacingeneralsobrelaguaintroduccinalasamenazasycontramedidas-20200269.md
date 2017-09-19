---
TOCTitle: Información general sobre la guía Introducción a las amenazas y contramedidas
Title: Información general sobre la guía Introducción a las amenazas y contramedidas
ms:assetid: '9744e03e-61be-4938-8cf6-98c6f6047564'
ms:contentKeyID: 20200269
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Dd162275(v=TechNet.10)'
---

Amenazas y contramedidas
========================

### Información general

Actualizado: 27/12/05

##### En esta página

[](#edaa)[Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP](#edaa)
[](#ecaa)[Recursos relacionados](#ecaa)
[](#ebaa)[Comuníquenos su opinión](#ebaa)
[](#eaaa)[Servicios de consultoría y soporte técnico](#eaaa)
[](#yzwx)[Capítulo 1: Introducción a las amenazas y contramedidas: Configuración de la seguridad en Windows Server 2003 y Windows XP](#yzwx)
[](#badc)[Capítulo 2: Directivas de nivel de dominio](#badc)
[](#yyzz)[Capítulo 3: Directiva de auditoría](#yyzz)
[](#lmkw)[Capítulo 4: Derechos de usuario](#lmkw)
[](#jkuv)[Capítulo 5: Opciones de seguridad](#jkuv)
[](#rrrr)[Capítulo 6: Registro de eventos](#rrrr)
[](#ssss)[Capítulo 7: Servicios del sistema](#ssss)
[](#mmmm)[Capítulo 8: Directivas de restricción de software](#mmmm)
[](#zarv)[Capítulo 9: Plantillas administrativas de Windows XP y Windows Server 2003](#zarv)
[](#reoa)[Capítulo 10: Entradas del Registro adicionales](#reoa)
[](#iuyo)[Capítulo 11: Contramedidas adicionales](#iuyo)
[](#vcbn)[Capítulo 12: Conclusión](#vcbn)
[](#esrc)[Agradecimientos](#esrc)

### Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP

La guía *Introducción a las amenazas y contramedidas* ofrece una referencia a todos los parámetros de configuración de seguridad que proporcionan contramedidas para amenazas específicas contra las versiones actuales de los sistemas operativos Microsoft® Windows®. Esta guía es el complemento de otras dos publicaciones de Microsoft: [*Guía de seguridad de Windows Server 2003*](http://go.microsoft.com/fwlink/?linkid=14845), disponible en http://go.microsoft.com/fwlink/?LinkId=14845, y [*Guía de seguridad de Windows XP*](http://go.microsoft.com/fwlink/?linkid=14839), disponible en http://go.microsoft.com/fwlink/?LinkId=14839. Muchas de las contramedidas que se describen en esta guía no están dirigidas a las funciones de equipos específicas de las guías complementarias y, en algunos casos, a ninguna función en absoluto.

Los capítulos de esta guía se estructuran de una manera similar a cómo las secciones principales de configuración se muestran en la interfaz de usuario del Editor de directivas de grupo. Cada capítulo empieza con una breve explicación de lo que cubre ese capítulo, seguido de una lista de encabezados de subsecciones, cada uno de los cuales corresponde a una configuración o grupo de configuraciones. (Estos parámetros de configuración se incluyen en el libro de Microsoft Excel® que está disponible en la versión descargable de esta guía.) Cada subsección proporciona una explicación breve de la función de la contramedida, e incluye la siguiente información:

-   **Vulnerabilidad**. Explica cómo un atacante puede realizar un ataque si el parámetro se configura de una manera menos segura.

-   **Contramedida**. Explica cómo implementar la contramedida.

-   **Impacto potencial**. Explica las posibles consecuencias negativas de la implementación de la contramedida.

#### Destinatarios de la guía

Esta guía está destinada principalmente a consultores, expertos en seguridad, arquitectos de sistemas y profesionales de TI responsables de las fases de planeamiento del desarrollo de las aplicaciones o la infraestructura y la implementación de estaciones de trabajo Windows XP con SP2 o Windows Server 2003 con SP1 en entornos de empresa. No se ha diseñado para los usuarios domésticos.

#### Información general acerca de la guía

##### Capítulo 1: Presentación de la guía Introducción a las amenazas y contramedidas

En este capítulo se proporciona una breve descripción de la *guía Introducción a las amenazas y contramedidas* y se explica la forma en que está estructurada.

##### Capítulo 2: Directivas de nivel de dominio

En este capítulo se describen las directivas de cuenta de nivel de dominio; se incluyen las directivas de contraseñas, de bloqueo de cuentas y Kerberos.

##### Capítulo 3: Directiva de auditoría

En este capítulo se describen los diferentes parámetros de configuración que se aplican a las auditorías y se proporcionan ejemplos de eventos de auditoría creados por varias tareas comunes.

##### Capítulo 4: Derechos de usuario

En este capítulo se detallan los derechos y privilegios de inicio de sesión que se asignan según la configuración en la sección de asignación de derechos de usuario del Editor de directivas de grupo.

##### Capítulo 5: Opciones de seguridad

En este capítulo se analizan diversos parámetros de configuración de seguridad de los equipos, incluidos los relacionados con firmas digitales de datos, nombres de cuenta de administrador e invitado, acceso a las unidades de disquete y de CD ROM, comportamiento de la instalación de controladores y mensajes de inicio de sesión.

##### Capítulo 6: Registro de eventos

En este capítulo se analizan las configuraciones de directiva de grupo que se pueden utilizar para definir atributos relacionados con los registros de eventos de aplicación, seguridad y sistema.

##### Capítulo 7: Servicios del sistema

En este capítulo se describen todos los servicios del sistema incluidos en Windows Server 2003 y Windows XP.

##### Capítulo 8: Directivas de restricción de software

En este capítulo se proporciona una breve descripción de las directivas de restricción de software, que son una nueva característica en Windows XP y Windows Server 2003. Las directivas de restricción de software ofrecen un sistema basado en directivas que permite especificar qué programas se pueden ejecutar y cuáles no.

##### Capítulo 9: Plantillas administrativas de Windows XP y Windows Server 2003

En este capítulo se analizan las secciones de plantillas administrativas de Directiva de grupo que incluyen los parámetros basados en el Registro que determinan el comportamiento y el aspecto de los equipos en un entorno de red.

##### Capítulo 10: Entradas del Registro adicionales

En este capítulo se proporciona información acerca de las entradas de registro adicionales del archivo de plantilla de seguridad de línea de base que no están definidas en el archivo de plantilla administrativa (.adm).

##### Capítulo 11: Contramedidas adicionales

En este capítulo se describe la implementación de algunas contramedidas adicionales, tales como la creación de cuentas seguras.

##### Capítulo 12: Conclusión

En este capítulo de la guía se revisan los puntos más importantes mediante una breve descripción de todo lo tratado en los capítulos anteriores.

[](#mainsection)[Principio de la página](#mainsection)

### Recursos relacionados

Para obtener más información sobre los parámetros de configuración de seguridad que se describen en esta guía, descargue la publicación complementaria [*Guía de seguridad de Windows Server 2003*](http://go.microsoft.com/fwlink/?linkid=14845) en http://go.microsoft.com/fwlink/?LinkId=14845.

Puede consultar [otras soluciones de seguridad](http://www.microsoft.com/technet/community/columns/sectip/st0805.mspx) del equipo de Microsoft Solutions for Security and Compliance (MSSC) en www.microsoft.com/technet/community/columns/sectip/st0805.mspx.

[](#mainsection)[Principio de la página](#mainsection)

### Comuníquenos su opinión

El equipo de Microsoft Solutions for Security and Compliance (MSSC) agradece sus ideas acerca de ésta y otras soluciones de seguridad.

¿Tiene algún comentario? Háganoslo saber en la [bitácora de soluciones de seguridad para el profesional de TI.](http://blogs.technet.com/secguide)

O envíe sus comentarios por correo electrónico a la dirección siguiente: [SecWish@microsoft.com](mailto:secwish@microsoft.com?subject=guía%20introducción%20a%20las%20amenazas%20y%20contramedidas:%20configuración%20de%20la%20seguridad%20en%20windows%20server%202003%20y%20windows%20xp). Respondemos con frecuencia a los comentarios que se envían a este buzón.

Nos interesa su opinión.

[](#mainsection)[Principio de la página](#mainsection)

### Servicios de consultoría y soporte técnico

Existen muchos servicios disponibles para ayudar a las organizaciones en sus esfuerzos por mejorar su seguridad. Utilice los siguientes vínculos para encontrar los servicios que necesita:

Para buscar servicios de consultoría y soporte técnico adecuados a las necesidades de su organización, visite [Microsoft Services](http://www.microsoft.com/services/microsoftservices/default.mspx) en http://support.microsoft.com/msservices.

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 1: Introducción a las amenazas y contramedidas: Configuración de la seguridad en Windows Server 2003 y Windows XP

Actualizado: 27/12/05

El propósito de esta guía es brindarle una referencia a los parámetros de configuración de seguridad que proporcionan contramedidas para amenazas específicas contra las versiones actuales de los sistemas operativos Microsoft® Windows®.

Esta es una guía complementaria a otras dos publicaciones de Microsoft:

-   [*Guía de Seguridad de Windows Server 2003*](http://go.microsoft.com/fwlink/?linkid=14845), disponible en línea en
    http://go.microsoft.com/fwlink/?LinkId=14845

-   [*Guía de seguridad de Windows XP*](http://go.microsoft.com/fwlink/?linkid=14839), disponible en línea en
    http://go.microsoft.com/fwlink/?LinkId=14839* *

Muchas de las contramedidas que se describen en esta guía no están dirigidas a las funciones de equipos específicas de las guías complementarias y, en algunos casos, a ninguna función en absoluto. Estas contramedidas ayudan a garantizar la compatibilidad, la utilidad, la capacidad de administración, la disponibilidad o el rendimiento.

Aunque ya se ha mencionado, merece la pena repetir que la seguridad y la funcionalidad son los extremos opuestos de una secuencia; cuanto mayor sea el nivel de seguridad, menor será el nivel de funcionalidad, y viceversa. Hay excepciones, y si bien es cierto que existen contramedidas de seguridad que ayudan a mejorar la funcionalidad, en la mayoría de los casos la norma se cumple.

La estructura de capítulos de esta guía es semejante a la forma en que las secciones principales de configuración se muestran en la interfaz de usuario del Editor de objetos de directiva de grupo. Cada capítulo empieza con una breve explicación de lo que cubre ese capítulo, seguido de una lista de encabezados de subsecciones, cada uno de los cuales corresponde a una configuración o grupo de configuraciones. (Estos parámetros de configuración se incluyen en el libro de Microsoft Excel® que se describe más adelante en este capítulo). Cada subsección incluye una explicación breve de la función de la contramedida y las tres subsecciones adicionales siguientes:

-   **Vulnerabilidad**. Explica cómo un atacante puede aprovechar una función o su configuración.

-   **Contramedida**. Explica cómo implementar la contramedida.

-   **Impacto potencial**. Explica las posibles consecuencias negativas de la implementación de la contramedida.

Por ejemplo, el capítulo 2, "Directivas de nivel de dominio", comienza con las siguientes secciones:

**Directivas de cuentas**

-   Forzar el historial de contraseñas

    -   Vulnerabilidad

    -   Contramedida

    -   Impacto potencial

-   Vigencia máxima de la contraseña

    -   Vulnerabilidad

    -   Contramedida

    -   Impacto potencial

Esta pauta se repite a lo largo de toda la guía. Aquellos valores con una mayor relación entre sí se presentan en una sola sección. Por ejemplo, en el capítulo 5, "Opciones de seguridad", se presentan cuatro parámetros en la sección "Servidor y cliente de red de Microsoft: firmar digitalmente las comunicaciones (cuatro valores relacionados)". Estos parámetros son los siguientes:

-   Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (siempre)

-   Servidor de red de Microsoft: firmar digitalmente las comunicaciones (siempre)

-   Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)

-   Servidor de red de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)

Aunque en esta guía se documentan muchos parámetros de configuración de Directiva de grupo, no se incluyen aquellos que tienen como fin ayudar a las organizaciones a gestionar sus entornos. En esta guía sólo se examinan los parámetros de configuración (y sus funciones) en Microsoft Windows Server™ 2003 con SP1 y Windows XP con SP2 que pueden ayudar a las organizaciones a protegerse contra amenazas específicas. Los parámetros de configuración y las funciones que se agregaron después de esos Service Pack, o las funcionalidades que pueden haberse agregado en software disponible después de esos Service Pack, no se tratan en esta guía. Además, las características de administración y de seguridad que los administradores no pueden configurar no se describen en esta guía.

La información que se proporciona en esta guía le ayudará a usted y a su organización a entender las contramedidas que están disponibles en las versiones actuales del sistema operativo Windows, pero si desea orientación normativa acerca de qué configuración debe utilizar en casos específicos, consulte las dos guías complementarias:

-   *Guía de Seguridad de Windows Server 2003*, disponible en línea en
    [http://go.microsoft.com/fwlink/?LinkId=14845](http://go.microsoft.com/fwlink/?linkid=14845)

-   *Guía de seguridad de Windows XP*, disponible en línea en
    [http://go.microsoft.com/fwlink/?LinkId=14839](http://go.microsoft.com/fwlink/?linkid=14839)* *

El libro de Microsoft Excel "Configuración de la seguridad y los servicios predeterminados de Windows", que se incluye en esta guía, ofrece información sobre la configuración predeterminada. En la primera hoja de trabajo ("Windows Server 2003 Defaults") se detallan todos los parámetros de configuración predeterminada de Directiva de grupo que están disponibles en Windows Server 2003. Esta hoja de trabajo incluye las columnas siguientes:

-   La columna H, **Policy Setting Name in User Interface**, corresponde al nombre del valor tal y como aparece en el complemento Editor de directivas de grupo de Windows Server 2003.

-   La columna J, **Default Domain Policy**, hace referencia al valor de esa opción en la directiva de dominio predeterminada integrada que se crea al convertir el primer controlador de dominio en un nuevo dominio de servicio de directorio de Active Directory®.

-   La columna K, **Default Domain Controller Policy**, corresponde al valor de esa opción en la directiva de controlador de dominio predeterminada integrada que se crea al convertir el primer controlador de dominio en un nuevo dominio de Active Directory.

-   La columna L, **Stand-Alone Server Default Settings**, corresponde al valor predeterminado para esa opción en un servidor Windows Server 2003 independiente.

-   La columna M, **Domain Controller Effective Default Settings**, indica el valor real relativo a un controlador de dominio con la configuración predeterminada aún establecida.

-   La columna N, **Member Server Effective Default Settings**, muestra el valor real relativo a un miembro de dominio con la configuración predeterminada aún establecida.

Con “Configuración predeterminada real” se indica que éste es el valor real que tiene efecto en el sistema si no se han modificado los valores de seguridad. La configuración real en un sistema viene determinada por el motor de directivas de grupo cuando procesa una directiva de grupo durante el inicio del equipo. El motor asigna una orden de prioridad, tal y como se describe en la sección "Aplicación de Directiva de grupo" del capítulo 2, "Mecanismos de consolidación de Windows Server 2003" en la *Guía* *de seguridad* *de Windows Server 2003.*

Para facilitar la lectura de las hojas de cálculo, se han insertado columnas adicionales para ilustrar la jerarquía de objetos en el Editor de directivas de grupo. Las columnas de la A a la G representan cada nivel de la jerarquía. Por ejemplo, **Computer Configuration** aparece en la columna A, mientras que **Security Settings** aparece en la columna C. Se insertó además la columna I para facilitar la lectura de las hojas de cálculo.

La segunda hoja de trabajo, "Windows Server 2003 System Services", enumera todos los servicios disponibles en Windows Server 2003. Esta hoja de trabajo incluye las columnas siguientes:

-   La columna A, **Full Service Name**, enumera los servicios por sus nombres tal y como aparecen en las herramientas de administración gráficas, como la extensión Administrador de servicios de Microsoft Management Console (MMC).

-   La columna B, **Service Name**, enumera todos los servicios por sus nombres abreviados, formato que muchas herramientas de línea de comando emplean.

-   La columna C, **DC Startup Type**, muestra el estado de inicio predeterminado para el servicio en un controlador de dominio Windows Server 2003.

-   La columna D, **Member Server Startup Type**, muestra el estado de inicio predeterminado relativo al servicio en un equipo de Windows Server 2003 que es miembro de un dominio basado en Active Directory.

-   La columna E, **Stand-Alone Server Startup Type**, muestra el estado de inicio predeterminado relativo al servicio en un equipo independiente con Windows Server 2003.

-   La columna H, **Logon As**, muestra la cuenta que el servicio utiliza para iniciar sesión en una configuración predeterminada.

El formato de las hojas de trabajo adicionales ("Windows XP Defaults" y "Windows XP System Services") es semejante a estas dos hojas de trabajo. Brindan información sobre los servicios y los parámetros de configuración de seguridad en Windows XP.

[](#ccna)[Resúmenes de capítulos](#ccna)
[](#mcse)[Herramientas y plantillas](#mcse)

### Resúmenes de capítulos

Windows Server 2003 con SP1 y Windows XP con SP2 son hasta la fecha las versiones más fiables de estos sistemas operativos, con características mejoradas de seguridad y privacidad. Esta guía consta de doce capítulos; los capítulos 2 a 6 tratan los procedimientos que ayudan a crear un entorno seguro. Cada capítulo desarrolla un proceso completo que ayuda a proteger los equipos que utilizan estos sistemas operativos.

#### Capítulo 1: Introducción a las amenazas y contramedidas: Configuración de la seguridad en Windows Server 2003 y Windows XP

Este capítulo incluye información general sobre la guía, descripciones de la audiencia de destino, problemas que se tratan en la guía, así como la finalidad principal que se persigue con la misma.

#### Capítulo 2: Directivas de nivel de dominio

Este capítulo expone la configuración de directiva de grupo que se aplica en el nivel de dominio: las directivas de contraseñas, las directivas de bloqueo de cuentas y las directivas de protocolo de autenticación Kerberos. En conjunto, estas directivas se conocen como directivas de cuenta.

#### Capítulo 3: Directiva de auditoría

Este capítulo cubre el uso de directivas de auditoría para supervisar e implantar sus medidas de seguridad. Describe las distintas configuraciones y proporciona ejemplos sobre el modo en que se modifica la información de auditoría al cambiar la configuración.

#### Capítulo 4: Derechos de usuario

Este capítulo describe los distintos derechos de inicio de sesión y privilegios que proporcionan los sistemas operativos Windows, y ofrece orientación sobre las cuentas a las que se deben asignar a estos derechos.

#### Capítulo 5: Opciones de seguridad

En este capítulo se presenta la sección de Directiva de grupo "Opciones de seguridad" y se ofrece orientación acerca de los parámetros de configuración de seguridad como las firmas digitales de datos, los nombres de cuenta de administrador e invitado, el acceso a las unidades de disquete y de CD ROM, el comportamiento de la instalación de controladores y los mensajes de inicio de sesión.

#### Capítulo 6: Registro de eventos

En este capítulo se proporciona orientación acerca de cómo configurar los parámetros relacionados con los diversos registros eventos en equipos con Windows Server 2003 y Windows XP.

#### Capítulo 7: Servicios del sistema

Windows XP y Windows Server 2003 incluyen una variedad de servicios del sistema. Muchos de estos servicios están configurados para ejecutarse de forma predeterminada, pero existen otros que no están presentes a menos que se instalen componentes específicos. Este capítulo describe los distintos servicios que se incluyen con los sistemas operativos y proporciona recomendaciones específicas sobre los que se deben dejar habilitados y los que se pueden habilitar sin riesgos.

#### Capítulo 8: Directivas de restricción de software

En este capítulo se proporciona una breve descripción del mecanismo de directivas de restricción de software, que se introdujo en Windows XP y Windows Server 2003. Proporciona vínculos a recursos adicionales acerca de cómo diseñar y utilizar las directivas de restricción de software.

#### Capítulo 9: Plantillas administrativas de Windows XP y Windows Server 2003

Este capítulo describe las configuraciones que están disponibles a través de las plantillas administrativas de directiva de grupo. No examina cada parámetro disponible, sino que se centra en aquellos que se relacionan con la seguridad.

#### Capítulo 10: Entradas del Registro adicionales

Este capítulo ofrece información acerca de las entradas del Registro adicionales que no se incluyen en el archivo de plantillas administrativas, pero que están presentes en la plantilla de seguridad de línea de base. Proporciona instrucciones acerca de cómo modificar la interfaz del Editor de configuración de seguridad para exponer estas entradas en la interfaz de usuario. Proporciona también entradas de registro adicionales que están disponibles en Windows XP SP2 y Windows Server 2003 SP1.

#### Capítulo 11: Contramedidas adicionales

En este capítulo se describen varias medidas de seguridad adicionales que tal vez deban aplicarse a sus equipos. Sin embargo, estas contramedidas no se pueden aplicar fácilmente a través de Directiva de grupo ni otros medios automatizados. Estas contramedidas incluyen la protección de cuentas en servidores miembros, la configuración NTFS, la segmentación de datos y aplicaciones, la configuración del nombre de comunidad de SNMP, la deshabilitación de enlaces de NetBIOS, la configuración de Servicios de Terminal Server, Dr. Watson, las directivas de IPsec y una referencia a orientación más amplia sobre el Servidor de seguridad de Windows.

#### Capítulo 12: Conclusión

El capítulo final repasa puntos importantes de la guía mediante una breve descripción general de todo lo tratado en los capítulos anteriores.

[](#mainsection)[Principio de la página](#mainsection)

### Herramientas y plantillas

Se incluye una colección de archivos con la versión descargable de esta guía, para ayudar a su organización a evaluar, probar e implementar las contramedidas recomendadas. Colectivamente, se hace referencia a estos archivos como herramientas y plantillas.

Los archivos se incluyen en un archivo .msi dentro del archivo WinZip de extracción automática que contiene esta guía, que está disponible en el Centro de descarga de Microsoft en http://go.microsoft.com/fwlink/?LinkId=15160. Al ejecutar el archivo .msi, se creará la siguiente estructura de carpetas en la ubicación que especifique:

-   La carpeta **\\Threats and Countermeasures Guide Tools and Templates** contiene el libro de Microsoft Excel "Windows Default Security and Services Configuration.xls"; en el se resume el servicio y la configuración predeterminada para Windows Server 2003 con SP1 y Windows XP con SP2.

-   La carpeta **\\Threats and Countermeasures Guide Tools and Templates\\SCE Update** incluye archivos de texto y de secuencia de comandos. Puede utilizar los archivos de texto para modificar y personalizar la interfaz de usuario del Editor de configuración de seguridad. Puede utilizar los archivos de secuencia de comandos para aplicar automáticamente esta configuración o revertirla. Estos procedimientos se detallan en el capítulo 10, "Entradas del registro adicionales".

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 2: Directivas de nivel de dominio

Este capítulo expone la configuración de directiva de grupo que se aplica en el nivel de dominio. La directiva predeterminada de controladores de dominio integrada incluye valores de configuración predeterminados para estas directivas, a los que se conoce en conjunto con el nombre de directivas de cuenta.

[](#elaa)[Directivas de cuentas](#elaa)
[](#emaa)[Información adicional](#emaa)

### Directivas de cuentas

Hay tres tipos diferentes de directivas de cuenta: directivas de contraseña, directivas de bloqueo de cuentas y directivas de protocolo de autenticación Kerberos. Un solo dominio de Microsoft Windows Server™ 2003 puede tener una de cada una de estas directivas. Si se establecen estas directivas en cualquier otro nivel de Active Directory, sólo se verán afectadas las cuentas locales de los servidores miembro.

**Nota**: en relación con las cuentas de dominio, sólo podrá haber una directiva de cuenta por dominio. La directiva de cuenta se debe definir en la directiva de dominio predeterminada, o bien, en una nueva directiva vinculada a la raíz del dominio y con preferencia sobre la primera directiva que, a su vez, aplican los controladores que crean el dominio. Un controlador de dominio siempre obtiene la directiva de cuenta de la raíz del dominio, aun cuando se aplique una directiva de cuenta distinta a la unidad organizativa que contiene el controlador de dominio. La raíz del dominio es el contenedor del nivel superior del dominio, de modo que no debe confundirse con el dominio raíz de un bosque, que es el dominio del nivel superior dentro de ese bosque.

La configuración de directiva de cuenta en directiva de grupo se aplica en el nivel de dominio. Los valores predeterminados se encuentran en la directiva predeterminada de controladores de dominio integrada para directivas de contraseña, directivas de bloqueo de cuentas y directivas Kerberos. Al configurar estas directivas en el servicio de directorio Active Directory®, recuerde que Microsoft® Windows® sólo permite una directiva de cuenta de dominio, la directiva de cuenta que se aplica al dominio raíz del árbol de dominio. La directiva de cuenta de dominio será la directiva de cuenta predeterminada de cualquier equipo con Windows que sea miembro del dominio.

La única excepción a esta regla tiene lugar cuando se define otra directiva de cuenta para una unidad organizativa (UO). La configuración de la directiva de cuenta para la unidad organizativa afectará a la directiva local en cualquier equipo contenido en la unidad organizativa. Por ejemplo, si una directiva de la unidad organizativa establece una vigencia máxima de la contraseña que difiere de la directiva de cuenta de nivel de dominio, la directiva de la UO sólo se aplicará cuando algún usuario inicie sesión en el equipo local. Sólo las directivas de equipo local predeterminadas se aplicarán a equipos que estén en un grupo de trabajo o en un dominio donde no se aplique ni una directiva de cuenta de UO ni una directiva de dominio.

La configuración para cada uno de estos tipos de directiva se describe en este capítulo.

#### Directiva de contraseñas

En Windows y muchos otros sistemas operativos, el método más común para autenticar la identidad de un usuario es utilizar una contraseña o frase cifrada secreta. Un entorno seguro de red requiere que todos los usuarios utilicen contraseñas seguras (que tengan por lo menos diez caracteres e incluyan una combinación de letras, números y símbolos). Estas contraseñas ayudan a prevenir la alteración de cuentas de usuario y cuentas administrativas por personas no autorizadas que utilizan métodos manuales o herramientas automatizadas para adivinar las contraseñas no seguras. Las contraseñas seguras que se modifican con frecuencia reducen los riesgos de que se produzcan ataques a las mismas. (En la sección "Las contraseñas deben cumplir los requerimientos de complejidad" de este capítulo se proporciona información más detallada sobre las contraseñas seguras).

Puede implantar el uso de contraseñas seguras mediante una directiva de contraseñas apropiada. La configuración de la directiva de contraseñas controla la complejidad y la duración de las contraseñas. En esta sección se trata cada parámetro específico de la directiva de contraseñas de cuentas. Esta guía incluye además un libro de Microsoft Excel®, "Configuración de la seguridad y los servicios predeterminados de Windows", que documenta la configuración predeterminada.

Puede establecer la configuración de la directiva de contraseñas en la siguiente ubicación del Editor de objetos de directiva de grupo:

**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas de cuenta\\Directivas de contraseñas**

Si hay grupos que necesitan directivas de contraseñas independientes, se deberán segmentar en otro dominio o bosque basado en cualquier requisito adicional.

##### Forzar el historial de contraseñas

Esta configuración de directiva determina el número de nuevas contraseñas únicas que se deben asociar a una cuenta de usuario antes de que se pueda volver a utilizar una contraseña anterior.

Los valores posibles para la configuración **Forzar el historial de contraseñas** son:

-   Un valor especificado por el usuario entre 0 y 24

-   No está definido

##### Vulnerabilidad

La reutilización de contraseñas es una preocupación importante en cualquier organización. Muchos usuarios querrán utilizar o volver a utilizar la misma contraseña para su cuenta durante un largo periodo de tiempo. Cuanto más tiempo se utilice una contraseña en una cuenta determinada, más posibilidades habrá de que un atacante pueda averiguarla mediante un ataque de fuerza bruta. Además, cualquier cuenta que se haya visto afectada seguirá en peligro mientras la contraseña no se modifique. Si se requieren cambios de contraseña pero no se evita el uso de contraseñas anteriores, o si los usuarios pueden utilizar continuamente un pequeño número de ellas, la eficacia de una buena directiva de contraseñas se verá enormemente reducida.

Si especifica un número bajo para esta configuración de directiva, los usuarios serán capaces de utilizar el mismo número pequeño de contraseñas de forma repetida. Si no configura también el parámetro **Vigencia mínima de la contraseña**, los usuarios serán capaces de cambiar varias veces sus contraseñas hasta que puedan volver a emplear su contraseña original.

##### Contramedida

Configure **Forzar el historial de contraseñas** con un valor de **24**, el máximo posible, para reducir el número de vulnerabilidades causadas por una contraseña que se vuelve a emplear.

Para que este valor sea eficaz en la organización, no permita que las contraseñas se cambien inmediatamente al configurar el valor **Vigencia mínima de la contraseña**. El valor de **Forzar el historial de contraseñas** debe establecerse en un nivel que combine de forma razonable una vigencia máxima de la contraseña con un intervalo de cambio de contraseñas para todos los usuarios de la organización.

###### Impacto potencial

El principal impacto de esta configuración reside en que los usuarios deberán crear una contraseña nueva cada vez que se les inste a cambiar la antigua. Si se pide a los usuarios que cambien las contraseñas a valores únicos nuevos se incrementa el riesgo de que apunten las contraseñas para no olvidarlas. Otro riesgo es que los usuarios pueden crear contraseñas que cambian en incrementos (por ejemplo, *contraseña01*, *contraseña02*, etc.) para facilitar la memorización. Por otra parte, un valor excesivamente bajo del parámetro **Vigencia mínima de la contraseña** aumentará sin duda la carga administrativa, porque los usuarios que olvidan sus contraseñas solicitarán ayuda para restablecerlas.

##### Vigencia máxima de la contraseña

Esta configuración de directiva determina el número de días que una contraseña se puede utilizar antes de que el usuario la deba cambiar.

Los valores posibles para la configuración de **Vigencia máxima de la contraseña** son:

-   Un número de días especificado por el usuario entre 0 y 999

-   No está definido

###### Vulnerabilidad

Cualquier contraseña, incluso la más compleja, se puede adivinar o descifrar si un atacante dispone de tiempo suficiente y de la capacidad de procesamiento. Algunos de los siguientes parámetros de configuración de la directiva pueden evitar que se averigüe una contraseña en un plazo razonable. El riesgo de que una contraseña válida se averigüe puede reducirse si se obliga a los usuarios a que cambien sus contraseñas con frecuencia, lo que puede también mitigar el riesgo de un inicio de sesión no autorizado por alguien que haya adquirido una contraseña de forma ilegítima. La **Vigencia máxima de la contraseña** se puede configurar para que los usuarios no necesiten cambiarla en ningún momento, aunque esta configuración conlleva un riesgo significativo de la seguridad.

###### Contramedida

Configure la **Vigencia máxima de la contraseña** con un valor que sea conveniente en función de los requisitos empresariales de su organización. Microsoft recomienda un valor de 90 días para la mayoría de las organizaciones. Aunque esta configuración no se recomienda, puede configurar la **Vigencia máxima de la contraseña** en 0 para que las contraseñas nunca caduquen.

###### Impacto potencial

Si el parámetro de **Vigencia máxima de la contraseña** es demasiado bajo, hará que los usuarios tengan que cambiar las contraseñas muy a menudo. De hecho, esta configuración puede reducir la seguridad de la organización, porque es más probable que los usuarios anoten sus contraseñas en algún lugar para no olvidarlas, y que dejen la información en una ubicación insegura o la pierdan. Si el valor de esta configuración de directiva es demasiado alto, el nivel de seguridad dentro de una organización se reducirá porque los atacantes potenciales tendrán más tiempo para intentar averiguar las contraseñas de los usuarios o para usar cuentas afectadas.

##### Vigencia mínima de la contraseña

Esta configuración de directiva determina el número de días que una contraseña se puede utilizar antes de que el usuario pueda cambiarla. El valor de la **vigencia mínima de la contraseña** debe ser menor que el valor de la **vigencia máxima de la contraseña**.

Establezca esta configuración de directiva en una cifra superior a **0** si desea que el valor de **Forzar el historial de contraseñas** sea eficaz. Si configura el valor de **Forzar el historial de contraseñas** en **0**, el usuario no tendrá que elegir una contraseña nueva única cuando se le pida que cambie su contraseña. Si se emplea el historial de contraseñas, los usuarios tendrán que utilizar una contraseña nueva exclusiva cuando la cambien.

Los valores posibles para la configuración de **vigencia mínima de la contraseña** son:

-   Un número de días especificado por el usuario entre 0 y 998

-   No está definido

###### Vulnerabilidad

No es eficaz obligar a los usuarios a que cambien las contraseñas regularmente si pueden pasar de una contraseña a otra en varias ocasiones hasta volver a emplear una contraseña favorita. Utilice la configuración de directiva con un valor de **Forzar el historial de contraseñas** que evite que se vuelvan a utilizar contraseñas anteriores. Por ejemplo, si configura el valor de **Forzar el historial de contraseñas** para garantizar que los usuarios no puedan volver a emplear cualquiera de sus últimas 12 contraseñas, podrían cambiar su contraseña 13 veces en unos pocos minutos y volver a emplear la contraseña con la que iniciaron a menos que configure la **vigencia mínima de la contraseña** en un número mayor que 0. Debe establecer esta configuración de directiva en una cifra superior a **0** para que el valor de **Forzar el historial de contraseñas** sea eficaz.

###### Contramedida

Configure la **Vigencia mínima de la contraseña** en un valor de cuando menos **2 días.** Si configura el número de días en **0, **serían posibles los cambios inmediatos de contraseña, algo que no es aconsejable.

###### Impacto potencial

Hay un problema menor en relación con la configuración de la **Vigencia mínima de la contraseña** en una cifra superior a **0.** Si un administrador establece una contraseña para un usuario, pero desea que ese usuario la cambie la primera vez que inicie sesión, el administrador debe activar la casilla de verificación **El usuario debe cambiar la contraseña en el siguiente inicio de sesión.** De lo contrario, el usuario no podrá cambiar la contraseña hasta el siguiente día.

##### Longitud mínima de la contraseña

Esta configuración de directiva determina el número mínimo de caracteres que debe tener una contraseña para una cuenta de usuario. Existen diversas teorías para determinar la mejor longitud de contraseña para una organización, pero quizás el término "frase cifrada" sea más apropiado que "contraseña". En Microsoft Windows 2000 y versiones posteriores, las frases cifradas pueden ser bastante largas y pueden incluir espacios, signos de puntuación y caracteres Unicode. De esta forma, una frase como “Quiero tomarme una bebida de 5 €” es una frase cifrada válida. Esta frase es bastante más segura que una cadena de 8 o 10 caracteres de números y letras aleatorios, pero es más fácil de recordar.

Los valores posibles para la configuración de **longitud mínima de la contraseña** son:

-   Un número especificado por el usuario entre 0 y 14

-   No está definido

###### Vulnerabilidad

Existen varios tipos de ataques de contraseña que se pueden llevar a cabo con la intención de obtener la contraseña de una cuenta de usuario determinada. Entre ellos se pueden mencionar los ataques de diccionario (que intentan utilizar palabras y frases comunes) y los ataques de fuerza bruta (que prueban cualquier combinación posible de caracteres). Además, los atacantes tratan a veces de obtener la base de datos de cuentas para usar utilidades y averiguar las contraseñas y tener acceso a las cuentas.

###### Contramedida

Configure la **longitud mínima de la contraseña** con un valor de **8,** como mínimo. Si el número de caracteres se establece en **0**, no será necesaria ninguna contraseña.

En la mayoría de los entornos es aconsejable utilizar una contraseña de 8 caracteres, ya que es lo suficientemente larga para ofrecer una seguridad adecuada, pero no tan difícil para que los usuarios puedan recordarla. Esta configuración ofrecerá una defensa adecuada contra un ataque de fuerza bruta. Si se agregan requisitos de complejidad, disminuirá la posibilidad de que se produzca un ataque de diccionario. Estos requisitos se describen en la siguiente sección del capítulo. Debe tenerse en cuenta que en algunos países hay requisitos legales con respecto a la longitud de la contraseña.

###### Impacto potencial

Cuando las contraseñas son demasiado largas, la seguridad de la organización puede verse afectada de hecho, porque es más probable que los usuarios anoten sus contraseñas en algún lugar para no olvidarlas, y que dejen la información en una ubicación insegura o la pierdan. Sin embargo, si se enseña a los usuarios que pueden utilizar frases cifradas como se ha mencionado anteriormente, deben ser capaces de recordarlas fácilmente.

Si se permiten contraseñas cortas, la seguridad se verá reducida, ya que estas contraseñas resultan más fáciles de averiguar con herramientas que realizan ataques de diccionario o de fuerza bruta. Si se solicitan contraseñas muy largas, es posible que se generen errores al escribirlas que puedan tener como consecuencia un bloqueo de las cuentas y un aumento del volumen de llamadas al servicio de asistencia.

Las versiones más antiguas de Windows, como Windows 98 y Windows NT® 4,0, no admiten contraseñas de más de 14 caracteres. Los equipos en los que se ejecutan estos sistemas operativos más antiguos no podrán autenticarse en equipos o dominios que utilizan cuentas que requieren contraseñas largas.

##### Las contraseñas deben cumplir los requerimientos de complejidad

Esta configuración de directiva determina si las contraseñas deben cumplir una serie de instrucciones consideradas de importancia para una contraseña segura.

Si se habilita esta configuración de directiva, las contraseñas de los usuarios deben cumplir los siguientes requisitos:

-   La contraseña tendrá una longitud de al menos seis caracteres.

-   La contraseña contendrá caracteres de tres de las cuatro categorías siguientes:

    -   Caracteres en mayúsculas (A, B, C,...)

    -   Caracteres en minúsculas (a, b, c,...)

    -   Números (0, 1, 2, 3, 4, 5, 6, 7, 8, 9)

    -   Caracteres no alfanuméricos y Unicode (( ) \` ~ ! @ \# $ % ^ & \* - + = | \\ { } \[ \] : ; " ' &lt; &gt; , . ? / € Γ ƒ λ y el espacio)

-   La contraseña no incluirá tres o más caracteres consecutivos del nombre de cuenta o nombre que se muestra del usuario. Si el nombre de cuenta tiene una longitud inferior a tres caracteres, no se realiza esta comprobación ya que la velocidad a la que las contraseñas se rechazarían sería demasiado alta. Al comprobar el nombre completo del usuario, varios caracteres se consideran como delimitadores que dividen el nombre en símbolos individuales: comas, puntos, guiones, caracteres de subrayado, espacios, signos de número y tabulaciones. Por cada token con una longitud de tres o más caracteres, se busca el token en cuestión en la contraseña y, si está presente, el cambio de la contraseña se rechaza.

    Por ejemplo, el nombre "Sandra I. Martínez" se dividiría en tres símbolos: Sandra, I y Martínez Puesto que el segundo símbolo tiene una longitud de un solo carácter, se omitiría. de manera que este usuario no podría tener una contraseña que contuviese "sandra" ni "martínez" como subcadena. Todas estas comprobaciones no distinguen mayúsculas de minúsculas.

Estos requisitos de complejidad son de aplicación forzosa al cambiar una contraseña o al crear una nueva.

Las reglas que se incluyen en la directiva de Windows Server 2003 no se pueden modificar directamente, si bien se puede crear una nueva versión del archivo Passfilt.dll para aplicar un conjunto de reglas diferente. Para obtener más información acerca de cómo crear su propio filtro de contraseña, consulte la documentación de [Filtros de contraseña](http://msdn.microsoft.com/en-us/library/ms721882.aspx) en el kit de desarrollo de software (SDK) de la plataforma Windows en MSDN® en http://msdn.microsoft.com/library/en-us/secmgmt/security/password\_filters.asp.

Los valores posibles para la configuración **Las contraseñas deben cumplir los requerimientos de complejidad** son:

-   Habilitada

-   Deshabilitado

-   No está definido

###### Vulnerabilidad

Las contraseñas que sólo contienen caracteres alfanuméricos son extremadamente fáciles de averiguar mediante varias utilidades disponibles para el público en general. Para evitar que se descifren las contraseñas, deben contener una gama más amplia de caracteres.

###### Contramedida

Configure el parámetro **Las contraseñas deben cumplir los requerimientos de complejidad** como **Habilitado**.

Si este valor se combina con una **Longitud mínima de la contraseña** de **8**, esta configuración de directiva garantiza que el número de posibilidades distintas para una única contraseña sea tan grande que sería muy difícil (aunque no imposible) que una ataque de fuerza bruta tenga éxito. Un atacante con suficiente capacidad de procesamiento para probar un millón de contraseñas por segundo podría averiguar una contraseña así en unos siete días y medio o menos. (Si el valor del parámetro **longitud mínima de la contraseña** se incrementa, la media del tiempo necesario para que un ataque tenga éxito aumentará también.)

###### Impacto potencial

Si la configuración predeterminada de complejidad de la contraseña se mantiene, podrían incrementarse las solicitudes de asistencia por cuentas bloqueadas, ya que los usuarios pueden no estar acostumbrados a contraseñas que contienen caracteres no-alfabéticos. Sin embargo, todos los usuarios deberían ser capaces de cumplir el requisito de complejidad sin mayor dificultad.

Si su organización tiene requisitos de seguridad más rigurosos, puede crear una versión personalizada del archivo**Passfilt.dll**que permita el uso de reglas de seguridad de la contraseña arbitrariamente complejas. Por ejemplo, un filtro personalizado de contraseña podría estipular el uso de caracteres que no sean de la fila superior. (Los caracteres de la fila superior son los que requieren que se pulse la tecla Mayús y cualquiera de los dígitos entre 1 y 0.) Un filtro personalizado de contraseña podría realizar también una comprobación de diccionario para verificar que la contraseña propuesta no contiene palabras o fragmentos comunes de diccionario.

Además, la utilización de combinaciones de teclas Alt puede mejorar enormemente la complejidad de una contraseña. Sin embargo, si se establecen requisitos tan estrictos, es probable que surja el descontento y que aumenten las llamadas al servicio de asistencia. Alternativamente, su organización podría considerar como requisito para todas las contraseñas de administrador que utilicen los caracteres ALT en el intervalo 0128 – 0159. (Puede que los caracteres Alt que se hallen fuera de este intervalo representen caracteres alfanuméricos estándar que no impliquen una complejidad adicional a la contraseña.)

##### Almacenar contraseña usando cifrado reversible para todos los usuarios del dominio

Esta configuración de directiva determina si Microsoft Windows Server 2003, Windows 2000 Server, Windows 2000 Professional y Windows XP Professional almacenan contraseñas con cifrado reversible.

La configuración **Almacenar contraseña usando cifrado reversible para todos los usuarios del dominio** ofrece compatibilidad para protocolos de aplicación que requieren el conocimiento de la contraseña de usuario para propósitos de autenticación. Sin embargo, las contraseñas cifradas que se almacenan de manera reversible pueden ser descifradas. Un atacante experto que lo consiga podría tener acceso a los recursos de red utilizando la cuenta afectada.

**Precaución:** no habilite nunca esta configuración de directiva, a menos que los requisitos de la empresa tengan prioridad sobre la necesidad de proteger la información de contraseña.

El uso de la autenticación con protocolo de autenticación por desafío mutuo (CHAP) mediante servicios de acceso remoto o Servicio de autenticación de Internet (IAS) requiere que esta configuración de directiva esté habilitada. CHAP es un protocolo de autenticación que las conexiones de red y el acceso remoto de Microsoft pueden utilizar.

Los valores posibles de la configuración **Almacenar contraseña usando cifrado reversible para todos los usuarios del dominio** son:

-   Habilitada

-   Deshabilitado

-   No está definido

###### Vulnerabilidad

Con esta configuración de directiva se determina si Windows Server 2003 almacena contraseñas en un formato menos seguro que es mucho más proclive a riesgos.

###### Contramedida

Configure **Almacenar contraseña usando cifrado reversible para todos los usuarios del dominio** como **Deshabilitado**.

###### Impacto potencial

Si su organización utiliza el protocolo de autenticación por desafío mutuo (CHAP) mediante servicios de acceso remoto o IAS, o la autenticación de texto en IIS, debe establecer esta configuración de directiva como **Habilitado.** Se trata de un parámetro extremadamente peligroso si se aplica mediante una directiva de grupo dependiendo del usuario, ya que será necesario abrir el objeto de la cuenta de usuario adecuado en el complemento de Microsoft Management Console (MMC) Usuarios y equipos de Active Directory.

#### Directiva de bloqueo de cuentas

Si durante un intento de inicio de sesión en el sistema son varias las veces que la contraseña se escribe de forma incorrecta, puede que un atacante esté intentando averiguar la contraseña de una cuenta a través del método de ensayo y error. Windows Server 2003 con SP1 lleva un registro de los intentos de inicio de sesión, y se puede configurar el sistema operativo para que deshabilite la cuenta durante un periodo determinado después de un número específico de tentativas fallidas. La configuración de la directiva de bloqueo de cuentas controla el umbral de esta respuesta y qué acción se tomará cuando se alcanza este umbral. Esta guía incluye un libro de Microsoft Excel, "Configuración de la seguridad y los servicios predeterminados de Windows," que documenta la configuración predeterminada.

Puede establecer la configuración de la directiva de bloqueo de cuentas en la siguiente ubicación del Editor de objetos de directiva de grupo:

**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas de cuenta\\Directiva de bloqueo de cuentas**

##### Duración del bloqueo de cuenta

Esta configuración de directiva determina el número de minutos que una cuenta permanece bloqueada antes de desbloquearse automáticamente. El intervalo de valores disponible es de 1 a 99.999 minutos. Para especificar que la cuenta permanezca bloqueada hasta que un administrador la desbloquee manualmente, configure el valor en **0**. Si se define el umbral de bloqueos de la cuenta, la **Duración del bloqueo de cuenta** debe ser igual o mayor que el tiempo de restablecimiento.

Los valores posibles para la configuración **Duración del bloqueo de cuenta** son:

-   Un número de minutos especificado por el usuario entre 0 y 99.999

-   No está definido

###### Vulnerabilidad

Una condición de denegación de servicio (DoS) se puede crear si un atacante altera el **Umbral de bloqueos de la cuenta** e intenta iniciar sesión con una cuenta específica de forma repetida. Si configura el parámetro **Umbral de bloqueos de la cuenta**, la cuenta quedará bloqueada después de un número específico de tentativas fallidas. Si configura la **Duración del bloqueo de cuenta** en **0**, la cuenta permanecerá bloqueada hasta que el administrador la desbloquee de forma manual.

###### Contramedida

Configure la **Duración del bloqueo de cuenta** en un valor apropiado para su entorno. Para especificar que la cuenta permanezca bloqueada hasta que un administrador la desbloquee manualmente, configure el valor en **0**. Cuándo el parámetro **Duración del bloqueo de cuenta** se configura con un valor que no sea cero, los intentos automatizados de adivinar las contraseñas de las cuentas deben esperar que transcurra este intervalo para reanudar las tentativas contra una cuenta específica. Si utiliza este parámetro en combinación con el parámetro de **umbral de bloqueos de la cuenta**, tales intentos automatizados de adivinar las contraseñas pueden dificultarse o hacerse inútiles.

###### Impacto potencial

Aunque pueda parecer una buena idea establecer esta configuración de directiva de modo que nunca se desbloquee automáticamente una cuenta, esta configuración puede aumentar el número de consultas al personal de asistencia de su empresa para desbloquear cuentas bloqueadas por error.

##### Umbral de bloqueos de la cuenta

Esta configuración de directiva determina el número de intentos fallidos para iniciar sesión que provoca el bloqueo de una cuenta de usuario. Una cuenta bloqueada no se podrá utilizar hasta que un administrador la restablezca o hasta que finalice el periodo de duración del bloqueo de la cuenta. Puede especificar un valor hasta 999 intentos de inicio de sesión sin éxito, o bien puede configurar el valor en 0 para que la cuenta no se bloquee nunca. Si define un **umbral de bloqueos de la cuenta**, la **duración del bloqueo de cuenta** deberá ser igual o mayor que el tiempo de restablecimiento.

Los intentos de escribir una contraseña sin éxito en estaciones de trabajo o servidores miembro que se han bloqueado por medio de Ctrl+Alt+Supr o de protectores de pantalla protegidos por contraseña no contarán como intentos de inicio de sesión sin éxito, a menos que se habilite la configuración de directiva **Inicio de sesión interactivo: requerir la autenticación del controlador de dominio para desbloquear el equipo**. Si se habilita, los intentos de escribir la contraseña sin éxito para desbloquear la estación de trabajo se tendrán en cuenta en el umbral de bloqueos de la cuenta.

Los valores posibles para la configuración del **umbral de bloqueos de la cuenta** son:

-   Un valor definido por el usuario entre 0 y 999

-   No está definido

###### Vulnerabilidad

Puede que en los ataques de contraseña se empleen métodos automatizados con el propósito de probar miles o incluso millones de combinaciones de contraseña para una o todas las cuentas de usuario. La eficacia de tales ataques se puede eliminar casi por completo si limita el número de inicios de sesión fallidos que se pueden realizar.

Sin embargo, es importante no olvidar que se puede llevar a cabo un ataque de denegación de servicio en un dominio con un umbral de bloqueos de la cuenta configurado. Así, un atacante malintencionado puede intentar realizar una serie de ataques de contraseña en todos los usuarios de la organización de forma programada Si el número de intentos es mayor que el umbral de bloqueos de la cuenta, el atacante podría bloquear todas las cuentas.

###### Contramedida

Dado que pueden existir vulnerabilidades tanto si este valor está configurado como si no lo está, se definen dos contramedidas diferentes. Cada organización debería sopesar ambas alternativas teniendo presente las amenazas y los riesgos identificados que se quieran mitigar. Las dos opciones de contramedidas son:

-   Configurar **Umbral de bloqueos de la cuenta** en **0.** Esta configuración garantiza que no se bloqueen las cuentas y evita los ataques de denegación de servicio con los que se pretenda bloquear de forma intencional algunas cuentas específicas o todas. También reducirá las llamadas al servicio de asistencia, puesto que los usuarios no podrán bloquear por accidente sus propias cuentas.

    Dado que esto no impide que se produzca un ataque de fuerza bruta, seleccione este valor sólo si se cumplen explícitamente los siguientes criterios:

    -   La directiva de contraseñas obliga a los usuarios a tener contraseñas complejas compuestas de 8 o más caracteres.

    -   Existe un mecanismo de auditoría eficaz instalado para avisar a los administradores cuando se produzca una serie de inicios de sesión sin éxito en el entorno.

-   Si su organización no puede cumplir los criterios anteriores, configure el **umbral de bloqueos de la cuenta** en un valor suficientemente alto que proporcione a los usuarios la capacidad de escribir mal accidentalmente su contraseña varias veces antes de que la cuenta se bloquee, pero que a la vez asegura que un ataque de fuerza bruta a la contraseña haga que se bloquee la cuenta. Una recomendación buena para esta configuración es 50 intentos de inicio de sesión no válidos, que evitará los bloqueos de cuenta accidentales y reducirá el número de llamadas al departamento de soporte, aunque no evitará un ataque DoS (como se indica anteriormente).

###### Impacto potencial

Si se habilita esta configuración de directiva, no podrá utilizarse una cuenta bloqueada hasta que un administrador la restablezca o hasta que finalice el periodo de duración del bloqueo de la cuenta. Este valor generará con casi toda probabilidad un número de llamadas adicionales al servicio de asistencia. De hecho, en muchas organizaciones, la mayoría de las llamadas al servicio de asistencia se deben a cuentas bloqueadas.

Si configura el **umbral de bloqueos de la cuenta** en **0**, existe la posibilidad de que una tentativa de un atacante para averiguar contraseñas con un ataque de fuerza bruta pase inadvertido si no se cuenta con un mecanismo robusto de auditoría.

##### Restablecer la cuenta de bloqueos después de

Esta configuración de directiva determina el número de minutos que deben pasar antes de que el contador que lleva el registro de los intentos de inicio de sesión fallidos y activa los bloqueos de cuenta se restablezca a **0.** Si se define un **Umbral de bloqueos de la cuenta**, este tiempo de restablecimiento deberá ser igual o inferior al valor de **Duración del bloqueo de cuenta**.

Los valores posibles para la configuración **Restablecer la cuenta de bloqueos después de** son:

-   Un número de minutos especificado por el usuario entre 1 y 99.999

-   No está definido

###### Vulnerabilidad

Los usuarios pueden bloquear sus propias cuentas de manera accidental si escriben incorrectamente la contraseña varias veces. Para reducir la probabilidad de que esto ocurra, el valor de configuración **Restablecer la cuenta de bloqueos después de** determina el número de minutos que deben pasar antes de que el contador que lleva el registro de los intentos de inicio de sesión fallidos y activa los bloqueos de cuenta se restablezca a 0.

###### Contramedida

Configure el valor del parámetro **Restablecer la cuenta de bloqueos después de** en **30 minutos**.

###### Impacto potencial

Si no establece esta configuración de directiva o si el valor se configura en un intervalo demasiado largo, podría ocurrir un ataque de denegación de servicio. Un atacante podría intentar malintencionadamente iniciar sesión en la cuenta de usuario muchas veces para bloquearla, tal como se describe en los párrafos anteriores. Si no establece la configuración **Restablecer la cuenta de bloqueos después de**, los administradores tendrían que desbloquear manualmente todas las cuentas. Si establece esta configuración de directiva en un valor razonable, los usuarios permanecerán bloqueados durante algún tiempo, y una vez transcurrido ese periodo, sus cuentas se habrán desbloqueado automáticamente. Asegúrese de notificar a los usuarios de los valores utilizados para esta configuración de directiva para que esperen que el temporizador de bloqueo caduque antes de llamar al servicio de soporte por no poder iniciar sesión.

#### Directiva Kerberos

En Windows Server 2003 con SP1, el protocolo de autenticación de la versión 5 de Kerberos ofrece el mecanismo predeterminado para los servicios de autenticación de dominio, así como los datos de autorización necesarios para que un usuario tenga acceso a un recurso y realice una tarea en él. Si se reduce la vigencia máxima de los vales de Kerberos, desciende el riesgo de que un atacante robe las credenciales de un usuario legítimo y los utilice con éxito, si bien aumenta la carga administrativa que conlleva el proceso de autorización.

En la mayoría de los entornos no es necesario cambiar la configuración de la directiva Kerberos. Esta configuración de directiva se aplica en el nivel de dominio y los valores predeterminados se configuran en el GPO de la directiva de dominio predeterminada en una instalación predeterminada de un dominio de Active Directory de Windows 2000 o Windows Server 2003. Esta guía incluye un libro de Microsoft Excel, "Configuración de la seguridad y los servicios predeterminados de Windows," que documenta la configuración predeterminada.

Puede establecer la configuración de la directiva Kerberos en la siguiente ubicación del Editor de objetos de directiva de grupo:

**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas de cuenta\\Directiva Kerberos**

##### Forzar restricciones de inicio de sesión de usuario

Esta configuración de directiva determina si el Centro de distribución de claves (KDC) valida cada solicitud de vale de sesión en la directiva de derechos de usuario de la cuenta del usuario. La validación de cada solicitud de vale de sesión es opcional, ya que el paso adicional requiere tiempo y puede ralentizar el acceso de red a los servicios.

Los valores posibles para la configuración **Forzar restricciones de inicio de sesión de usuario** son:

-   Habilitada

-   Deshabilitado

-   No está definido

###### Vulnerabilidad

Si deshabilita esta configuración de directiva, los usuarios podrían recibir vales de sesión para servicios a los que ya no tengan derecho de uso porque el derecho se eliminó después de que iniciaron sesión.

###### Contramedida

Establezca **Forzar restricciones de inicio de sesión de usuario** en **Habilitado**.

###### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

##### Vigencia máxima del vale de servicio

Esta configuración de directiva determina la cantidad máxima de tiempo (en minutos) que un vale de sesión con permiso puede usar para obtener acceso a un servicio determinado. El valor debe ser de por lo menos 10 minutos, y menor o igual al valor establecido en **Vigencia máxima del vale de usuario**.

Si, al solicitar una conexión con un servidor un cliente presenta un vale de sesión caducado, el servidor devolverá un mensaje de error y el cliente debe solicitar un nuevo vale de sesión del KDC. Sin embargo, una vez que se autentica una conexión, ya no es importante que el vale de sesión siga siendo válido, ya que los vales de sesión se utilizan sólo para autenticar nuevas conexiones con los servidores. Del mismo modo, las operaciones no se verán interrumpidas si el vale de sesión con el que se ha autenticado la sesión caduca.

Los valores posibles para la configuración de **Vigencia máxima del vale de usuario** son:

-   Un número de minutos especificado por el usuario entre 10 y 99.999. Si establece esta configuración de directiva en 0, los vales de servicio no caducan.

-   No está definido

###### Vulnerabilidad

Si configura demasiado alto el valor **Vigencia máxima del vale de servicio**, entonces los usuarios podrían tener acceso a recursos de red fuera de sus horas de sesión. Además, los usuarios cuyas cuentas se han deshabilitado podrían seguir teniendo acceso a servicios de red con vales de servicio válidos expedidos antes de que sus cuentas se deshabilitaran.

###### Contramedida

Configure la **Vigencia máxima del vale de servicio** en **600 minutos**.

###### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

##### Vigencia máxima del vale de usuario

Esta configuración de directiva determina la cantidad máxima de tiempo (en horas) de un vale de concesión de vales de usuario. Este vale de usuario debe renovarse cuando caduque, o bien, solicitar uno nuevo.

Los valores posibles para la configuración de **Vigencia máxima del vale de usuario** son:

-   Un número de horas especificado por el usuario entre 0 y 99.999 El valor predeterminado es 10 horas.

-   No está definido

###### Vulnerabilidad

Si configura demasiado alto el valor **Vigencia máxima del vale de usuario**, entonces los usuarios podrían tener acceso a recursos de red fuera de sus horas de sesión. Además, los usuarios cuyas cuentas se han deshabilitado podrían seguir teniendo acceso a servicios de red con vales de servicio válidos expedidos antes de que sus cuentas se deshabilitaran.

###### Contramedida

Configure la **Vigencia máxima del vale de usuario** en 10 horas.

###### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

##### Edad máxima de renovación de tíquets de usuario

Esta configuración de directiva determina el periodo de tiempo (en días) durante el cual se puede renovar un vale de concesión de vales de usuario.

Los valores posibles para la configuración de **Vigencia máxima de renovación de vales de usuario** son:

-   Un número de minutos especificado por el usuario entre 0 y 99.999

-   No está definido

###### Vulnerabilidad

Si el valor de la configuración de **Vigencia máxima de renovación de vales de usuario** es demasiado alto, entonces los usuarios podrían renovar vales de usuario muy antiguos.

###### Contramedida

Configure la **Vigencia máxima de renovación de vales de usuario** en **10.080 minutos** (7 días).  

###### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

##### Tolerancia máxima para la sincronización de los relojes de los equipos

Esta configuración de directiva determina la diferencia máxima de tiempo (en minutos) que el protocolo Kerberos admite entre la hora del reloj del equipo cliente y la hora del controlador de dominio de Windows Server 2003 que ofrece autenticación Kerberos.

Los valores posibles para la configuración de **Tolerancia máxima para la sincronización de los relojes de los equipos** son:

-   Un número de minutos especificado por el usuario entre 1 y 99.999

-   No está definido

###### Vulnerabilidad

Para evitar “ataques de reproducción”, el protocolo de autenticación Kerberos utiliza marcas de tiempo como parte de su definición de protocolo. A fin de que las marcas de tiempo funcionen adecuadamente, los relojes del cliente y del controlador de dominio necesitarán estar sincronizados al máximo. Dado que los relojes de dos equipos distintos no suelen estar sincronizados, los administradores podrán utilizar esta directiva para establecer el máximo tiempo transcurrido dentro del que debe completarse una negociación Kerberos; el tiempo transcurrido se calcula a partir de las marcas de tiempo. El valor de este parámetro limita la diferencia máxima de tiempo que se puede tolerar entre el controlador de dominio y el equipo cliente.

###### Contramedida

Configure la **Tolerancia máxima para la sincronización de los relojes de los equipos** en **5 minutos**.

###### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

[](#mainsection)[Principio de la página](#mainsection)

### Información adicional

Los vínculos siguientes proporcionan información adicional acerca de los temas relacionados con el refuerzo de controladores de dominio en los que se ejecuta Windows Server 2003 con SP1:

-   Para ver una explicación detallada del funcionamiento de la complejidad de contraseñas en Windows y consejos específicos sobre cómo crear contraseñas más seguras que no sean demasiado difíciles de recordar, consulte el artículo "[Contraseñas seguras](http://www.microsoft.com/smallbusiness/support/articles/select_sec_passwords.mspx)", que está disponible en línea en www.microsoft.com/smallbusiness/support/articles/select\_sec\_passwords.mspx.

-   Para obtener más información sobre las instrucciones de seguridad autorizadas de Microsoft, consulte las [Prácticas recomendadas de seguridad](http://www.microsoft.com/technet/security/secnews/articles/enterprisesecbp.mspx) en www.microsoft.com/technet/security/secnews/articles/enterprisesecbp.msp.

-   Para obtener más información acerca de las directivas de grupo, incluida una lista de rutas y valores de todos los parámetros de configuración que se almacenan en el registro, y sobre cuáles están disponibles en las diferentes versiones de Windows, consulte [Group Policy Settings Reference for Windows Server 2003 with Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7821c32f-da15-438d-8e48-45915cd2bc14)” en www.microsoft.com/downloads/details.aspx?FamilyId=7821C32F-DA15-438D-8E48-45915CD2BC14.

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 3: Directiva de auditoría

Actualizado: 27/12/05

Un registro de auditoría registrará una entrada siempre que los usuarios realicen ciertas acciones específicas. Por ejemplo, la modificación de un archivo o una directiva puede desencadenar una entrada de auditoría que muestra la acción que se ha llevado a cabo, la cuenta de usuario asociada y la fecha y hora de la acción. Puede auditar tanto los intentos correctos como incorrectos en las acciones.

El estado del sistema operativo y las aplicaciones de un equipo es dinámico. Por ejemplo, puede que sea necesario que los niveles de seguridad cambien de forma temporal para permitir la resolución inmediata de un problema relacionado con la administración o la red. Sin embargo, muy a menudo estos cambios se olvidan y nunca se deshacen. Si los niveles de seguridad no se restablecen apropiadamente, puede que un equipo deje de cumplir los requisitos de seguridad de la empresa.

Los análisis de seguridad periódicos permiten a los administradores hacer un seguimiento y determinar que se están tomando medidas adecuadas de seguridad en cada equipo como parte de un programa de administración de riesgos de la empresa. Este análisis se centra en información altamente especificada sobre todos los aspectos del sistema relacionados con la seguridad, que los administradores pueden utilizar para ajustar los niveles de seguridad. Lo que es más importante, esta información puede ayudar a detectar cualquier defecto de seguridad que pueda darse en el sistema con el tiempo.

Las auditorías de seguridad son extremadamente importantes para cualquier red empresarial, ya que los registros de auditoría pueden brindar la única indicación de que se ha producido una infracción de seguridad. Si se descubre la infracción de cualquier otra forma, la configuración de auditoría adecuada generará un registro de auditoría que contenga información importante sobre la infracción.

A menudo, los registros de errores son mucho más informativos que los registros de aciertos, ya que los errores suelen indicar problemas. Por ejemplo, el inicio de sesión correcto en un equipo por parte de un usuario se consideraría normal. Sin embargo, que alguien intente sin éxito iniciar sesión en un equipo varias veces puede indicar que un atacante está intentando obtener acceso al equipo utilizando las credenciales de usuario de otra persona. Los registros de eventos hacen un seguimientos de los eventos en el equipo y, en los sistemas operativos Microsoft® Windows®, hay registros de eventos independientes para aplicaciones, eventos de seguridad y eventos de sistema. El registro de seguridad registra eventos de auditoría. El contenedor de registro de eventos de directiva de grupo se utiliza para definir atributos relacionados con la aplicación, la seguridad y los registros de eventos del sistema como, por ejemplo, el tamaño máximo del registro, los derechos de acceso para los registros, así como la configuración y los métodos de retención. Esta guía incluye un libro de Microsoft Excel®, "Configuración de la seguridad y los servicios predeterminados de Windows", que documenta la configuración predeterminada.

Antes de implementar cualquier proceso de auditoría, una organización debe determinar cómo reunirán, organizarán y analizarán los datos. Los volúmenes grandes de datos de auditoría no tienen mucho valor si no hay un plan para aprovecharlos. Además, la configuración de la auditoría puede afectar al rendimiento del equipo. El efecto de una combinación dada de parámetros de configuración puede ser insignificante en un equipo de usuario final, pero muy notable en un servidor ocupado. Por lo tanto, debe realizar algunas pruebas de rendimiento antes de implementar la nueva configuración de auditoría en su entorno de producción.

Puede establecer la configuración de directiva de auditoría en la siguiente ubicación del Editor de objetos de directiva de grupo:

**Configuración de equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales**
**\\Directiva de auditoría**

[](#oooo)[Configuración de auditoría](#oooo)
[](#cccc)[Ejemplo de auditoría: Resultados de un evento de inicio de sesión](#cccc)
[](#dddd)[Información adicional](#dddd)

### Configuración de auditoría

Las vulnerabilidades, contramedidas y posibles impactos de todos los valores de configuración de auditoría son idénticos. Por lo tanto, estos términos se describen sólo una vez. Cada descripción va seguida de explicaciones breves de cada parámetro.

Las opciones para cada uno de los parámetros de configuración de auditoría son:

-   **Correcto**. Se genera una entrada de auditoría cuando la acción solicitada se realiza correctamente.

-   **Erróneo**. Se genera una entrada de auditoría cuando la acción solicitada no se realiza correctamente.

-   **Sin auditoría**. No se genera una entrada de auditoría para la acción asociada.

**Vulnerabilidad**

Si no se establece ninguna configuración de auditoría, será complicado o imposible determinar lo que sucedió durante un incidente de seguridad. No obstante, si se configuran las auditorías para que demasiadas actividades autorizadas generen eventos, el registro de eventos de seguridad se llenará de datos poco útiles. Además, si configura las auditorías para muchos objetos, puede afectar al rendimiento del equipo en general.

**Contramedida**

Debe habilitar una configuración razonable de la directiva de auditoría para todos los equipos de su organización para que los usuarios puedan ser responsables de sus acciones y las actividades no autorizadas se puedan detectar y rastrear.

**Impacto potencial**

Si no se configura ninguna auditoría o si la auditoría tiene una configuración poco rígida en los equipos de la organización, no habrá suficientes evidencias disponibles para el análisis de la red después de que se produzcan los incidentes de seguridad. Sin embargo, si la configuración de auditoría es demasiado rígida, algunas entradas importantes del registro de seguridad pueden verse opacadas por todas las entradas irrelevantes, y el rendimiento del equipo puede deteriorarse significativamente. Las compañías que operan en ciertas industrias reguladas pueden tener obligaciones legales de registrar ciertos eventos o actividades.

#### Auditar eventos de inicio de sesión de cuenta

Esta configuración de directiva determina si se debe auditar cada instancia de un usuario que inicie o cierre una sesión en un equipo diferente al que registra el evento y valida la cuenta. Si define este valor de configuración de directiva, puede especificar si desea auditar los aciertos, los errores o no auditar el tipo de evento. Las auditorías de aciertos generan una entrada de auditoría cuando un intento de inicio de sesión de cuenta tiene éxito, lo que ofrece información útil para establecer la responsabilidad y para la investigación tras el incidente, de forma que se pueda determinar quién consiguió iniciar sesión y en qué equipo. Las auditorías fallidas generan una entrada de auditoría cuando falla un intento de inicio de sesión, lo que es útil para la detección de intrusiones. Sin embargo, esta configuración de directiva crea también el potencial para un ataque de denegación de servicio (DoS). Cuándo se habilita la configuración **Auditoría: apagar el sistema de inmediato si no puede registrar auditorías de seguridad**, un atacante puede generar millones de errores de inicio de sesión, llenar el registro de eventos de seguridad y obligar a que se cierre el equipo.

Si configura **Auditar eventos de inicio de sesión de cuenta** como **Correcto** en un controlador de dominio, se registrará una entrada para cada usuario que se valide en el controlador de dominio, aunque el usuario esté iniciando sesión en una estación de trabajo o servidor asociados al dominio.

#### Auditar la administración de cuentas

Esta configuración de directiva determina si se deben auditar todos los eventos de administración de cuentas de un equipo. Algunos ejemplos de eventos de administración de cuentas incluyen:

-   Se crea, cambia o elimina una cuenta de usuario o grupo.

-   Cambia el nombre de una cuenta de usuario, o bien, se desactiva o se activa una.

-   Se establece o cambia una contraseña.

Si configura **Auditar la administración de cuentas**, puede especificar si desea auditar los aciertos, los errores o no auditar el tipo de evento. Las auditorías de aciertos generan una entrada de auditoría cuando cualquier evento de administración de cuentas se lleva a cabo satisfactoriamente, y debe habilitarlas en todos los equipos de la empresa. Cuando una organización responde a incidentes de seguridad, es muy importante que pueda realizar un seguimiento de las personas que crearon, cambiaron o eliminaron una cuenta. Las auditorías de errores generan una entrada de auditoría cuando cualquier evento de administración de cuentas produce un error.

#### Auditar el acceso del servicio de directorio

Esta configuración de directiva determina si se debe auditar el acceso de usuario de un objeto de servicio de directorio Active Directory® que tiene una lista de control de acceso al sistema (SACL) asociada. Una SACL es una lista de usuarios y grupos cuyas acciones sobre un objeto se deben auditar en una red basada en Microsoft Windows.

Si configura **Auditar el acceso del servicio de directorio**, puede especificar si desea auditar los aciertos, los errores o no auditar el tipo de evento. Las auditorías de aciertos generan una entrada de auditoría cuando un usuario obtiene acceso correctamente a un objeto de Active Directory que tiene una SACL que indica que el usuario se debe auditar para la acción solicitada. Las auditorías de errores generan una entrada de auditoría cuando un usuario intenta obtener acceso sin éxito a un objeto de Active Directory que tiene una SACL que requiere de auditoría. (Ambos tipos de entradas de auditoría se crean antes de que se notifique al usuario que la solicitud fue correcta o incorrecta). Si habilita esta configuración de directiva y configura listas SACL en objetos de directorio, puede generarse un gran volumen de entradas en los registros de seguridad en controladores de dominio. Sólo debe habilitar esta configuración si realmente va a utilizar la información que se cree.

**Nota**: puede configurar una lista SACL en un objeto de Active Directory utilizando la ficha **Seguridad** del cuadro de diálogo **Propiedades** de ese objeto. Este método es parecido a **Auditar el acceso a objetos**, salvo que se aplica sólo a los objetos de Active Directory y no a los objetos del sistema de archivos y del registro.

#### Auditar eventos de inicio de sesión

Esta configuración de directiva determina si se debe auditar cada instancia de un usuario que inicie, cierre una sesión o realice una conexión de red al equipo que registra el evento de auditoría. Si registra eventos de auditoría de inicio de sesión correctos de cuenta en un controlador de dominio, los intentos de inicio de sesión de la estación de trabajo no generan auditorías de inicio de sesión. Sólo los intentos de inicio de sesión de red e interactivos en el controlador de dominio propiamente dicho generan eventos de inicio de sesión en el controlador de dominio. En resumen, los eventos de inicio de sesión de cuenta se generan donde se encuentra la cuenta, y los eventos de inicio de sesión se generan donde se produce el intento de inicio de sesión.

Si configura **Auditar eventos de inicio de sesión**, puede especificar si desea auditar los aciertos, los errores o no auditar el tipo de evento. Las auditorías de aciertos generan una entrada de auditoría cuando un intento de inicio de sesión tiene éxito; esto ofrece información útil de registro y de investigación tras el incidente, porque puede determinar quién consiguió iniciar sesión y en qué equipo. Las auditorías fallidas generan una entrada de auditoría cuando falla un intento de inicio de sesión, lo que es útil para la detección de intrusiones. Sin embargo, esta configuración crea también una condición potencial de DoS, porque un atacante podría generar millones de inicios de sesión fallidos, llenar el registro de eventos de seguridad y obligar a que se cierre el servidor.

#### Auditar el acceso a objetos

Esta configuración de directiva determina si se debe auditar el evento de un usuario que tiene acceso a un objeto (por ejemplo, un archivo, una carpeta, una clave de registro o una impresora) que tiene una lista SACL que especifica un requisito de auditoría.

Si configura **Auditar el acceso a objetos**, puede especificar si desea auditar los aciertos, los errores o no auditar el tipo de evento. Las auditorías de aciertos generan una entrada de auditoría cuando un usuario obtiene acceso correctamente a un objeto que tiene una lista SACL. Las auditorías de errores generan una entrada de auditoría cuando un usuario intenta obtener acceso sin éxito a un objeto que tiene una lista SACL (hay que contar con que se produzcan algunos eventos de error durante las operaciones normales de los equipos). Por ejemplo, muchas aplicaciones (como Microsoft Word) siempre intentan abrir los archivos con privilegios de lectura y escritura. Si las aplicaciones son incapaces de hacerlo, entonces tratan de abrir los archivos con privilegios de sólo lectura. Si habilita la auditoría de errores y la lista SACL apropiada en el archivo, se registrará un evento incorrecto cuando tal evento ocurre.

En Microsoft Windows Server™ 2003 con Service Pack 1 (SP1), puede auditar el acceso a objetos que se almacenan en la metabase el servidor de Información de Internet (IIS). Para habilitar la auditoría de objetos de metabase, debe habilitar **Auditar el acceso a objetos** en el equipo objetivo, y establecer las listas SACL en los objetos específicos de metabase cuyo acceso se desea auditar.

Si configura la directiva **Auditar el acceso a objetos** y configura las listas SACL en objetos, se puede generar un gran volumen de entradas en los registros de seguridad de los equipos en su organización. Por lo tanto, sólo debe habilitar esta configuración si realmente va a utilizar la información que se registra.

**Nota**: debe realizar un proceso de dos pasos para habilitar la función de auditoría de un objeto, como un archivo, una carpeta, una impresora o una clave del Registro en Windows Server 2003. Después de habilitar la directiva de auditoría de acceso a objetos, debe determinar los objetos cuyo acceso desea supervisar, y modificar sus listas SACL. Por ejemplo, si desea auditar cualquier intento por parte de los usuarios de abrir un archivo determinado, puede configurar el atributo de auditoría de errores y aciertos directamente en el archivo que desee supervisar para ese evento en particular con el Explorador de Windows o la directiva de grupo.

#### Auditar el cambio de directivas

Esta configuración de directiva determina si se debe auditar cada incidente de cambio de las directivas de asignación de derechos de usuario, de servidor de seguridad de Windows, de auditoría o de confianza.

Si configura **Auditar el cambio de directivas**, puede especificar si desea auditar los aciertos, los errores o no auditar el tipo de evento. Las auditorías de aciertos generan una entrada de auditoría cuando se produce un cambio correcto en las directivas de asignación de derechos de usuario, de auditoría o de confianza. Esta información de auditoría es útil con fines de seguimiento, y puede ayudar a determinar quién modificó exitosamente las directivas en el dominio o en equipos individuales. Las auditorías de error generan una entrada de auditoría cuando se produce un error al realizar un cambio en las directivas de asignación de derechos de usuario, de auditoría o de confianza.

Si habilita **Auditar el cambio de directivas** en Windows XP con SP2 y Windows Server 2003 con SP1, también se habilitan los cambios de configuración del componente de servidor de seguridad de Windows.

#### Auditar el uso de privilegios

Esta configuración de directiva determina si se debe auditar cada caso en el que un usuario ejecute un derecho de usuario.

Si configura **Auditar el uso de privilegios**, puede especificar si desea auditar los aciertos, los errores o no auditar el tipo de evento. Las auditorías de aciertos generan una entrada de auditoría cuando el ejercicio de un derecho de usuario tiene éxito. Las auditorías de errores generan una entrada de auditoría cuando el ejercicio de un derecho de usuario produce un error. Si habilita esta configuración de directiva, el volumen de eventos generado puede ser muy grande y puede resultar difícil clasificarlos. Sólo debe habilitar esta configuración si ha planeado cómo va a utilizar la información que se ha generado.

El uso de los siguientes derechos de usuario no genera eventos de auditoría, aunque se haya especificado la auditoría de aciertos o errores para esta configuración de directiva:

-   Omitir la comprobaciónde recorrido

-   Depurar programas

-   Crear un objetoToken

-   Reemplazar un token de nivel de proceso

-   Generar auditoríasde seguridad

-   Realizar copias de seguridad de archivos y directorios

-   Restaurar archivosy directorios

#### Auditar el seguimiento de procesos

Esta configuración de directiva determina si se debe auditar información de seguimiento detallada de eventos como la activación de programas, la salida de procesos, la duplicación de identificadores y el acceso indirecto a objetos.

Si configura **Auditar el seguimiento de procesos**, puede especificar si desea auditar los aciertos, los errores o no auditar el tipo de evento. Las auditorías de aciertos generan una entrada de auditoría cuando el proceso que se está siguiendo tiene éxito. Las auditorías de errores generan una entrada de auditoría cuando el proceso que se está siguiendo produce un error.

Si habilita **Auditar el seguimiento de procesos** en Windows XP con SP2 y Windows Server 2003 con SP1, Windows registrará también información acerca del modo y el estado de operación del componente Servidor de seguridad de Windows.

Cuándo **Auditar el seguimiento de procesos** está habilitado, se genera un gran número de eventos. Esta configuración de directiva se configura normalmente en **Sin auditoría.** Sin embargo, la información que esta configuración de directiva genera puede ser muy útil durante la respuesta a un incidente porque proporciona un registro detallado de los procesos que se iniciaron y cuándo se ejecutaron.

#### Auditar eventos del sistema

Esta configuración de directiva determina si se debe auditar el reinicio o cierre de un equipo realizado por un usuario o un evento que afecte a la seguridad del equipo o al registro de seguridad.

Si configura **Auditar eventos del sistema**, puede especificar si desea auditar los aciertos, los errores o no auditar el tipo de evento. Las auditorías de aciertos generan una entrada de auditoría cuando un evento se ejecuta correctamente. Las auditorías de errores generan una entrada de auditoría cuando un evento no se ejecuta correctamente. Puesto que se registran muy pocos eventos adicionales al habilitar las auditorías de aciertos y de errores para los eventos del sistema, y debido a que todos esos eventos son muy significativos, se recomienda establecer esta configuración de directiva como **Habilitado** en todos los equipos de la organización.

[](#mainsection)[Principio de la página](#mainsection)

### Ejemplo de auditoría: Resultados de un evento de inicio de sesión

Una vez que haya visto las distintas configuraciones de auditoría disponibles en Windows, puede ser útil estudiar un ejemplo concreto. Las auditorías se realizan desde el punto de vista de un equipo en particular, y no desde la perspectiva más holística que un administrador de empresa puede preferir. Debido a que los eventos se registran en equipos individuales, puede tener que examinar los registros de seguridad de varios equipos y correlacionar los datos para determinar lo que ocurrió.

En el resto de este capítulo se muestran los eventos principales que se escriben en los registros de eventos de un controlador de dominio, un servidor de archivos y un equipo de usuario final cuando un usuario autorizado inicia sesión en su equipo y obtiene acceso a un archivo en una carpeta compartida alojada en el servidor de archivos. Sólo los eventos principales se documentan; otros eventos que se generan a raíz de estas actividades se omiten por razones de claridad. Los nombres de las cuentas y los recursos relacionados con este ejemplo son:

-   Dominio = DOM

-   Controlador de dominio = DC1

-   Servidor de archivos = FS1

-   Equipo de usuario final = XP1

-   Usuario = Pablo

-   Carpeta compartida en FS1 = Recursos compartidos

-   Documento en la carpeta compartida = documento.txt

#### El usuario inicia sesión en su equipo

-   **Eventos registrados en el equipo del usuario final**

    -   Auditoría de aciertos para el Id. de evento 528, Inicio de sesión/Cierre de sesión de usuario para el usuario DOM\\Pablo en el equipo XP1.

-   **Eventos registrados en el controlador de dominio**

    -   Auditoría de aciertos para el Id. de evento 540, Inicio de sesión/Cierre de sesión de usuario para el usuario DOM\\Pablo en el equipo DC1.

-   **Eventos registrados en el servidor de archivos**

    -   No aplicable.

#### El usuario se conecta a la carpeta compartida denominada Recursos compartidos

-   **Eventos registrados en el equipo del usuario final**

    -   No aplicable.

-   **Eventos registrados en el controlador de dominio**

    -   Auditoría de aciertos para el Id. de evento 673, Inicio de sesión de cuenta para el usuario Pablo@DOM.com para el nombre de servicio FS1$.

    -   Auditoría de aciertos para el Id. de evento 673, Inicio de sesión de cuenta para el usuario F$$@DOM.com para el nombre de servicio FS1$.

    -   Auditoría de aciertos para el Id. de evento 673, Inicio de sesión de cuenta para el usuario XP1$@DOM.com para el nombre de servicio FS1$.

        **Nota**: todas estas son solicitudes de vale de servicio de protocolo de autenticación Kerberos.

-   **Eventos registrados en el servidor de archivos**

    -   Auditoría de aciertos para el Id. de evento 540, Inicio de sesión/Cierre de sesión de usuario para el usuario DOM\\Pablo en el equipo FS1.

    -   Auditoría de aciertos para el Id. de evento 560, Acceso a objetos para el usuario DOM\\Pablo al objeto denominado C:\\Recursos compartidos con tipos de acceso READ\_CONTROL, ReadData (o ListDirectory), ReadEA y ReadAttributes.

    -   Auditoría de aciertos para el Id. de evento 560, Acceso a objetos para el usuario DOM\\Pablo al objeto denominado C:\\Recursos compartidos\\documento.txt con tipos de acceso READ\_CONTROL, ReadData (o ListDirectory), ReadEA y ReadAttributes.

#### El usuario abre el archivo documento.txt.

-   **Eventos registrados en el equipo del usuario final**

    -   No aplicable.

-   **Eventos registrados en el controlador de dominio**

    -   No aplicable.

-   **Eventos registrados en el servidor de archivos**

    -   Auditoría de aciertos para el Id. de evento 560, Acceso a objetos para el usuario DOM\\Pablo al objeto denominado C:\\Recursos compartidos\\documento.txt con tipos de acceso READ\_CONTROL, ReadData (o ListDirectory), WriteDate (o AddFile), AppendDate (o AddSubdirectory o CreatePipeInstance), ReadEA, WriteEA, ReadAttributes y WriteAttributes.

    -   Auditoría de aciertos para el Id. de evento 560, Acceso a objetos para el usuario DOM\\Pablo al objeto denominado C:\\Recursos compartidos\\documento.txt con tipos de acceso ReadAttributes.

    -   Auditoría de aciertos para el Id. de evento 560, Acceso a objetos para el usuario DOM\\Pablo al objeto denominado C:\\Recursos compartidos con tipos de acceso ReadAttributes.

#### El usuario guarda el archivo documento.txt.

-   **Eventos registrados en el equipo del usuario final**

    -   No aplicable.

-   **Eventos registrados en el controlador de dominio**

    -   No aplicable.

-   **Eventos registrados en el servidor de archivos**

    -   Auditoría de aciertos para el Id. de evento 560, Acceso a objetos para el usuario DOM\\Pablo al objeto denominado C:\\Recursos compartidos\\documento.txt con tipos de acceso SYNCHRONIZE, ReadData (o ListDirectory), WriteDate (o AddFile), AppendDate (o AddSubdirectory o CreatePipeInstance), ReadEA, WriteEA, ReadAttributes y WriteAttributes.

    -   Auditoría de aciertos para el Id. de evento 560, Acceso a objetos para el usuario DOM\\Pablo al objeto denominado C:\\Recursos compartidos\\documento.txt con tipos de acceso READ\_CONTROL, SYNCHRONIZE y ReadData (o ListDirectory).

Aunque este ejemplo parezca una compleja serie de eventos, ha sido enormemente simplificado. Las acciones enumeradas generarían docenas de eventos de inicio de sesión, cierre de sesión y uso de privilegios en el controlador de dominio y el servidor de archivos. Cuando el usuario abre el archivo, se genera también una gran cantidad de eventos de acceso a objetos y cada vez que el usuario guarda el archivo se generan muchos más eventos. Como puede ver, el uso de datos de auditoría puede ser todo un desafío sin la ayuda de herramientas automatizadas como Microsoft Operations Manager.

[](#mainsection)[Principio de la página](#mainsection)

### Información adicional

Los vínculos siguientes proporcionan información adicional acerca de temas relacionados con directivas de auditoría en equipos en los que se ejecuta Windows XP con SP2 o Windows Server 2003 con SP1:

-   Para obtener más información sobre la directiva de auditoría, consulte la sección "[Directiva de auditoría](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/6847e72b-9c47-42ab-b3e3-691addac9f33.mspx)" en la documentación de TechCenter de Windows Server 2003 en Microsoft TechNet, en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/ServerHelp/6847e72b-9c47-42ab-b3e3-691addac9f33.mspx.

-   El artículo "[CÓMO: Utilizar Directiva de grupo para auditar claves del Registro en Windows Server 2003](http://support.microsoft.com/default.aspx?kbid=324739)" en http://support.microsoft.com/default.aspx?kbid=324739 describe cómo auditar el acceso a claves del Registro agregando listas SACL a esas claves.

-   Los artículos "[Descripciones de los sucesos de seguridad de Windows 2000 (Parte 1 de 2)](http://support.microsoft.com/kb/299475/)" en http://support.microsoft.com/kb/299475/ y "[Windows 2000 Security Event Descriptions (Part 2 of 2)"](http://support.microsoft.com/kb/301677/) en http://support.microsoft.com/kb/301677/ describen los eventos de seguridad registrados por Windows 2000 Server. También se aplican a Windows Server 2003 y Windows XP.

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 4: Derechos de usuario

Actualizado: 27/12/05

Los derechos de usuario permiten a los usuarios realizar tareas en un equipo o un dominio. Los derechos de usuario son *derechos de inicio de sesión* y *privilegios.* Con los derechos de inicio de sesión se controla quién tiene autorización para iniciar sesión en un equipo y el modo en que puede hacerlo, mientras que con los privilegios se supervisa el acceso a recursos del equipo y del dominio, y se anulan grupos de permisos establecidos en objetos determinados.

Un ejemplo de derecho de inicio de sesión es la capacidad de iniciar sesión en un equipo de forma local. Un ejemplo de privilegio consistiría en la capacidad de apagar el equipo. Estos derechos de usuario los asigna el administrador a usuarios individuales o a grupos como parte de la configuración de seguridad del equipo. Para ver un resumen de la configuración recomendada en este capítulo, vea el libro de Microsoft® Excel® "Configuración de la seguridad y los servicios predeterminados de Windows" que se incluye en esta guía. Este libro documenta la configuración predeterminada de asignación de derechos de usuario.

**Nota**: los servicios de Internet Information Server (IIS) esperan que ciertos derechos de usuario sean asignados a las cuentas integradas que los utilizan. La configuración de asignación de derechos de usuario en este capítulo identifica los derechos que IIS requiere; para obtener más información acerca de estos requisitos, consulte la lista de [IIS y cuentas integradas (IIS 6,0)](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/iis/3648346f-e4f5-474b-86c7-5a86e85fa1ff.mspx) en www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/3648346f-e4f5-474b-86c7-5a86e85fa1ff.mspx.

[](#ebama)[Configuración de Asignación de derechos de usuario](#ebama)
[](#eaamb)[Información adicional](#eaamb)

### Configuración de Asignación de derechos de usuario

Puede establecer la configuración de asignación de derechos de usuario en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:

**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\Asignación de derechos de usuario**

#### Tener acceso a este equipo desde la red

Esta configuración de directiva determina si los usuarios pueden conectarse al equipo desde la red. Esta capacidad es necesaria para una serie de protocolos de red, entre los que se encuentran protocolos basados en bloques de mensajes del servidor (SMB), NetBIOS, el sistema de archivos común de Internet (CIFS) y el modelo de objetos componentes Plus (COM+).

Los valores posibles para la configuración **Tener acceso a este equipo desde la red** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Los usuarios que se conectan a la red desde su equipo pueden tener acceso a recursos en los equipos de destino para los que tienen permiso. Por ejemplo, el derecho de usuario **Tener acceso a este equipo desde la red** es necesario para que los usuarios se conecten a impresoras y carpetas compartidas. Si se asigna este derecho de usuario al grupo **Todos** y algunas carpetas compartidas tienen permisos de recursos compartidos y NTFS para que el mismo grupo tenga acceso de lectura, cualquier usuario del grupo podrá ver los archivos de esas carpetas compartidas. Sin embargo, esta situación es improbable en instalaciones nuevas de Microsoft Windows Server™ 2003 con Service Pack 1 (SP1), ya que los permisos de recursos compartidos y NTFS predeterminados en Windows Server 2003 no incluyen el grupo **Todos**. Esta vulnerabilidad puede ser de alto riesgo en sistemas actualizados a partir de Windows NT® 4.0 o Windows 2000, ya que los permisos predeterminados para estos sistemas operativos no son tan restrictivos como los permisos predeterminados de Windows Server 2003.

##### Contramedida

Limite el derecho de usuario **Tener acceso a este equipo desde la red** sólo a aquellos usuarios que necesiten tener acceso al servidor. Por ejemplo, si establece esta configuración de directiva para los grupos de **Administradores** y **Usuarios**, los usuarios que inician sesión en el dominio serán capaces de tener acceso a los recursos compartidos de servidores en el dominio si los miembros del grupo **Usuarios del dominio** están incluidos en el grupo local de **Usuarios.**

##### Impacto potencial

Si elimina el derecho de usuario **Tener acceso a este equipo desde la red** en controladores de dominio para todos los usuarios, nadie será capaz de iniciar sesión en el dominio ni usar los recursos de red. Si elimina este derecho de usuario en servidores miembro, los usuarios no se podrán conectar a esos servidores mediante la red. Si ha instalado componentes opcionales como ASP.NET o los servicios de Internet Information Services (IIS), tal vez necesite asignar este derecho de usuario a cuentas adicionales que estos componentes requieren. Es importante comprobar que a los usuarios autorizados se les asigna este derecho de usuario para los equipos a los que necesitan tener acceso en la red.

#### Actuar como parte del sistema operativo

Esta configuración de directiva determina si un proceso puede asumir la identidad de cualquier usuario y así tener acceso a los recursos para los que el usuario tiene autorización de acceso. Generalmente, sólo los servicios de autenticación de bajo nivel requieren este derecho de usuario. Observe que el acceso potencial no se limita a los elementos asociados de forma predeterminada al usuario. El proceso que realiza las llamadas podría solicitar que se agreguen privilegios adicionales arbitrarios al token de acceso. Puede que el proceso que realiza la llamada cree un token de acceso que no ofrezca una identidad primaria para la auditoría en el registro de eventos del sistema.

Los valores posibles para la configuración **Actuar como parte del sistema operativo** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

El derecho de usuario **Actuar como parte del sistema operativo** es sumamente eficaz. Cualquier usuario que disfrute de él puede tener control total del equipo y eliminar prácticamente toda prueba de las actividades realizadas.

##### Contramedida

Limite el derecho de usuario **Actuar como parte del sistema operativo** al menor número de cuentas posible (en circunstancias normales, no debería asignarse ni siquiera al grupo **Administradores**). Cuando un servicio requiera este derecho de usuario, configure el servicio para iniciar sesión con la cuenta de sistema local, que tiene este privilegio de forma intrínseca. No cree una cuenta diferente para asignarle este derecho de usuario.

##### Impacto potencial

No debe haber prácticamente repercusiones porque el derecho de usuario **Actuar como parte del sistema operativo** rara vez lo necesitan cuentas que no sean la cuenta de sistema local.

#### Agregar estaciones de trabajo al dominio

Esta configuración de directiva determina si un usuario puede agregar un equipo a un dominio específico. Para que surta efecto, se debe asignar de modo que se aplique a por lo menos un controlador de dominio. Un usuario al que se le asigna este derecho de usuario puede agregar hasta diez estaciones de trabajo al dominio. Los usuarios también pueden unir un equipo a un dominio si tienen el permiso **Crear objetos de equipo** para una unidad organizativa o para el contenedor Equipos en el servicio de directorio Microsoft Active Directory®. Los usuarios que tengan asignado este permiso pueden agregar un número ilimitado de equipos al dominio, independientemente de si disfrutan del derecho de usuario **Agregar estaciones de trabajo al dominio**.

Los valores posibles para la configuración **Agregar estaciones de trabajo al dominio** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

El derecho de usuario **Agregar estaciones de trabajo al dominio** presenta una vulnerabilidad moderada. Los usuarios con este derecho pueden agregar un equipo al dominio configurado de forma que viole las directivas de seguridad de la empresa. Por ejemplo, si la empresa no quiere que los usuarios tengan privilegios administrativos en los equipos, un usuario podría instalar Windows en su equipo y, a continuación, agregar el equipo al dominio. De este modo, conocería la contraseña para la cuenta de administrador local, por lo que podría iniciar sesión con dicha cuenta y, a continuación, agregar su cuenta de dominio al grupo **Administradores** local.

##### Contramedida

Configure **Agregar estaciones de trabajo al dominio** para que sólo puedan agregar equipos al dominio los miembros autorizados del equipo de tecnología de la información (TI).

##### Impacto potencial

Esta contramedida no afectará a aquellas organizaciones que nunca hayan permitido a los usuarios que configuren sus propios equipos y los agreguen al dominio. Para aquellas que hayan permitido a todos o algunos usuarios que configuren sus propios equipos, esta contramedida obligará a establecer un proceso formal para la aplicación de estos procedimientos. No afectará a equipos existentes a menos que se eliminen del dominio y se vuelvan a agregar a él.

#### Ajustar las cuotas de memoria para un proceso

Esta configuración de directiva determina si usuarios pueden ajustar la cantidad máxima de memoria disponible para un proceso. Aunque esta capacidad es útil cuando necesita afinar equipos, debe considerar su potencial de abuso. Si no está en buenas manos, podría utilizarse para iniciar un ataque de denegación de servicio.

Los valores posibles para la configuración **Ajustar las cuotas de memoria para un proceso** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Un usuario con el privilegio **Ajustar las cuotas de memoria para un proceso** puede reducir la cantidad de memoria disponible para cualquier proceso, lo que podría causar que las aplicaciones importantes de la red se vuelvan lentas o fallen.

##### Contramedida

Restrinja el derecho de usuario **Ajustar las cuotas de memoria para un proceso** a usuarios que lo requieren para realizar sus trabajos, como administradores de aplicaciones que mantienen sistemas de administración de bases de datos o administradores de dominio que administran el directorio de la organización y su infraestructura de apoyo.

##### Impacto potencial

Las organizaciones que no han restringido a los usuarios a funciones con privilegios limitados encontrarán difícil implantar esta contramedida. Además, si ha instalado componentes opcionales como ASP.NET o los Servicios de Información de Internet (IIS), tal vez necesite asignar el derecho de usuario **Ajustar las cuotas de memoria para un proceso** a cuentas adicionales que estos componentes requieren. IIS requiere que este privilegio esté asignado explícitamente al servicio de red y las cuentas de servicio de IWAM\_*&lt;NombreEquipo&gt;*. De otro modo, esta contramedida no tendrá repercusión en la mayoría de los equipos. Si este derecho de usuario se necesita para una cuenta de usuario, se puede asignar a una cuenta de equipo local en vez de a una cuenta de dominio.

#### Permitir el inicio de sesión local

Esta configuración de directiva determina si un usuario puede iniciar una sesión interactiva en el equipo. Los usuarios que no disfruten de este derecho aún pueden iniciar una sesión interactiva remota en el equipo si disponen del derecho **Permitir inicio de sesión a través de Servicios de Terminal Server**.

Los valores posibles para la configuración **Permitir inicio de sesión local** son:

-   Lista de cuentas definida por el usuario

-   No está definido  

##### Vulnerabilidad

Una cuenta con el derecho de usuario **Permitir inicio de sesión local** puede iniciar sesión en la consola del equipo. Si no restringe este derecho de usuario a usuarios legítimos que necesitan iniciar sesión en la consola del equipo, algún usuario no autorizado podría descargar y ejecutar un código malintencionado para elevar sus privilegios.

##### Contramedida

Para los controladores de dominio, asigne solamente el derecho de usuario **Permitir el inicio de sesión local** al grupo **Administradores**. Para las otras funciones del servidor, puede optar por agregar los grupos **Operadores de copia de seguridad** y **Usuarios avanzados**. Para los equipos de usuario final, también deberá asignar este derecho al grupo **Usuarios**.

Otra posibilidad es la de asignar grupos como **Operadores de cuenta**, **Operadores de servidores** e **Invitados** al derecho de usuario **Denegar el inicio de sesión localmente**.

##### Impacto potencial

Al quitar estos grupos predeterminados, puede que se limiten las capacidades de aquellos usuarios que tengan asignadas funciones administrativas específicas en el entorno. Si ha instalado componentes opcionales como ASP.NET o los servicios de Internet Information Services, tal vez necesite asignar el derecho de usuario **Permitir inicio de sesión local** a cuentas adicionales que estos componentes requieren. IIS requiere que este derecho de usuario se asigne a la cuenta IUSR\_*&lt;NombreEquipo&gt;*. Debe confirmar que las actividades delegadas no se verán afectadas de forma negativa.

#### Permitir inicio de sesión a través de Servicios de Terminal Server

Esta configuración de directiva determina si los usuarios pueden iniciar sesión en el equipo mediante una conexión a Escritorio remoto. No debe asignar este derecho de usuario a otros usuarios o grupos, sino que resulta más eficaz agregar o eliminar usuarios del grupo **Usuarios de escritorio remoto** para controlar quién puede abrir una conexión de Escritorio remoto al equipo.

Los valores posibles para la configuración **Permitir inicio de sesión a través de Servicios de Terminal Server** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Una cuenta con el derecho de usuario **Permitir inicio de sesión a través de Servicios de Terminal Server** puede iniciar sesión en la consola remota del equipo. Si no restringe este derecho de usuario a usuarios legítimos que necesitan iniciar sesión en la consola del equipo, algún usuario no autorizado podría descargar y ejecutar un código malintencionado para elevar sus privilegios.

##### Contramedida

Para los controladores de dominio, asigne solamente el derecho de usuario **Permitir inicio de sesión a través de Servicios de Terminal Server** al grupo **Administradores**. Para otras funciones del servidor y equipos de usuario final, agregue el grupo **Usuarios de escritorio remoto**. Para servidores Terminal Server que no funcionan en el modo de servidor de aplicaciones, asegúrese de que sólo pertenecen a estos grupos el personal autorizado de TI que necesite administrar los equipos de forma remota.

**Advertencia**: para los servidores Terminal Server que funcionan en modo de servidor de aplicaciones, asegúrese de que solamente los usuarios que necesiten tener acceso al servidor tengan cuentas que pertenezcan al grupo **Usuarios de escritorio remoto**, ya que este grupo integrado tiene este derecho de inicio de sesión de forma predeterminada.

Otra posibilidad es la de asignar el derecho de usuario **Denegar el inicio de sesión a través de Servicios de Terminal Server** a grupos como **Operadores de cuenta**, **Operadores de servidor** e **Invitados**. Sin embargo, tenga cuidado al usar este método, ya que podría bloquear el acceso a administradores legítimos que también pertenecen a un grupo con el derecho de inicio de sesión **Denegar el inicio de sesión a través de Servicios de Terminal Server**.

##### Impacto potencial

La eliminación del derecho de usuario **Permitir inicio de sesión a través de Servicios de Terminal Server** de otros grupos o cambios de pertenencia en estos grupos predeterminados podrían limitar las capacidades de los usuarios que llevan a cabo funciones administrativas específicas en su entorno. Debe confirmar que las actividades delegadas no se verán afectadas de forma negativa.

#### Realizar copias de seguridad de archivos y directorios

Esta configuración de directiva determina si los usuarios pueden evadir los permisos de archivo y directorio al hacer una copia de seguridad del equipo. Este derecho de usuario sólo es eficaz cuando una aplicación intenta tener acceso a través de la interfaz de programación de aplicaciones (API) de la copia de seguridad NTFS mediante una utilidad de copia de seguridad como NTBACKUP.EXE. De lo contrario, se aplican los permisos estándar de directorios y archivos.

Los valores posibles para la configuración **Realizar copias de seguridad de archivos y directorios** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Los usuarios capaces de hacer copias de seguridad de datos de un equipo pueden llevar el medio de copia de seguridad a otro equipo que no pertenezca al dominio en el que tienen privilegios administrativos y, a continuación, restaurar los datos. Podrían asumir la propiedad de los archivos y ver cualquier información no cifrada que se encuentre dentro del conjunto de la copia de seguridad.

##### Contramedida

Restrinja el derecho de usuario **Realizar copias de seguridad de archivos y directorios** a aquellos miembros del equipo de TI que necesiten realizar copias de seguridad de datos de la empresa como parte de sus responsabilidades de trabajo diarias. Si utiliza software de copia de seguridad que se ejecuta en cuentas de servicio específicas, sólo estas cuentas (y no el personal de TI) deben tener el derecho de usuario **Realizar copias de seguridad de archivos y directorios.**

##### Impacto potencial

Al cambiar los miembros de los grupos que tienen el derecho de usuario **Realizar copias de seguridad de archivos y directorios** puede que se limiten las capacidades de aquellos usuarios que tengan asignadas funciones administrativas específicas en el entorno. Debe confirmar que los administradores de copias de seguridad autorizados pueden seguir realizando este tipo de operaciones.

#### Omitir la comprobación de recorrido

Esta configuración de directiva determina si los usuarios pueden pasar a través de carpetas sin que se verifique el permiso de acceso especial “Recorrer carpeta” cuando navegan en una ruta de objeto en el sistema de archivos NTFS o en el Registro. Este derecho de usuario no permite al usuario mostrar el contenido de una carpeta, sólo recorrer las carpetas.

Los valores posibles para la configuración **Omitir la comprobación de recorrido** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

El valor predeterminado de la configuración **Omitir la comprobación de recorrido** es permitir que cualquiera evite la comprobación de recorrido, y los administradores de sistemas de Windows experimentados configuran lista de control de acceso del sistema de archivos (ACL) de esta forma. El único escenario en el que la configuración predeterminada podría tener percances tiene lugar cuando el administrador que configura los permisos no comprende cómo funciona esta configuración de directiva. Por ejemplo, tal vez esperen que los usuarios que no tienen acceso a una carpeta tampoco tengan acceso al contenido de cualquier carpeta secundaria. Tal situación es improbable y, por lo tanto, esta vulnerabilidad presenta un riesgo pequeño.

##### Contramedida

Puede que aquellas organizaciones que se preocupen sumamente por la seguridad deseen quitar el grupo **Todos** o, incluso, el grupo **Usuarios** de la lista de grupos con el derecho de usuario **Omitir comprobación de recorrido**. Tomar el control explícito sobre las asignaciones de recorrido puede ser una manera muy eficaz de controlar el acceso a la información confidencial. (Además, puede usarse la función de [Enumeración basada en acceso](http://technet.microsoft.com/es-es/library/cc784710.aspx) que se agregó en Windows Server 2003 SP1. Si utiliza la enumeración basada en acceso, los usuarios no pueden ver ninguna carpeta o archivo a los que no tengan acceso. Para obtener más información acerca de esta función, visite www.microsoft.com/technet/prodtechnol/
windowsserver2003/library/BookofSP1/f04862a9-3e37-4f8c-ba87-917f4fb5b42c.mspx).

##### Impacto potencial

Los sistemas operativos Windows y muchas aplicaciones se han diseñado para que cualquier usuario que pueda tener acceso al equipo de forma legítima pueda disfrutar de este derecho de usuario. Por lo tanto, Microsoft recomienda que pruebe exhaustivamente cualquier cambio en las asignaciones del derecho de usuario **Omitir la comprobación de recorrido** antes hacer dichos cambios en los sistemas de producción. En particular, IIS requiere que este derecho de usuario se asigne a las cuentas de servicio de red, servicio local, IIS\_WPG, *IUSR\_&lt;NombreEquipo&gt; eIWAM\_&lt;NombreEquipo&gt;.* (Debe asignarse también a la cuenta de ASPNET a través de su pertenencia al grupo **Usuarios**). Esta guía recomienda que deje esta configuración de directiva en su valor predeterminado.

#### Cambiar la hora del sistema

Esta configuración de directiva determina si los usuarios pueden ajustar la hora en el reloj interno de equipo. No es necesario cambiar la zona horaria ni otras características de la hora del sistema.

Los valores posibles para la configuración **Cambiar la hora del sistema** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Los usuarios que pueden cambiar la hora de un equipo pueden provocar graves problemas. Por ejemplo, las marcas de tiempo en las entradas del registro de eventos podrían ser imprecisas, las marcas de tiempo en archivos y carpetas creados o modificados podrían ser incorrectas y los equipos que pertenezcan a un dominio podrían no ser capaces de autenticarse a sí mismos o a los usuarios que intentan iniciar sesión en el dominio desde ellos. Además, debido a que el protocolo de autenticación Kerberos requiere que el solicitante y el autenticador tengan sus relojes sincronizados dentro de un intervalo que define el administrador, un atacante que cambia la hora de un equipo puede causar que ese equipo sea incapaz de obtener o conceder vales Kerberos.

El riesgo de que ocurran este tipo de eventos se reduce en la mayoría de los controladores de dominio, servidores miembro y equipos de usuario final gracias al servicio Hora de Windows, que sincroniza la hora automáticamente con los controladores de dominio de las siguientes maneras:

-   Todos los equipos de escritorio cliente y los servidores miembro utilizan la autenticación del controlador de dominio como su asociado de hora de entrada.

-   Todos los controladores de dominio de un dominio concreto consideran al maestro de operaciones de emulador (PDC) del controlador de dominio principal como su asociado de hora de entrada.

-   Todos los maestros de operaciones de emulador PDC siguen la jerarquía de dominios a la hora de seleccionar su asociado de hora de entrada.

-   El maestro de operaciones de emulador PDC en la raíz del dominio es el recurso de hora autorizado de la organización. Por lo tanto, se recomienda que configure este equipo para que se sincronice con un servidor de tiempo externo seguro.

Esta vulnerabilidad resulta mucho más grave si un atacante puede cambiar la hora del sistema y detener el servicio Hora de Windows o volver a configurarlo para sincronizarlo con un servidor de hora que no es exacto.

##### Contramedida

Restrinja el derecho de usuario **Cambiar la hora del sistema** a usuarios que realmente necesiten poder cambiar la hora del sistema, como los miembros del equipo de TI.

##### Impacto potencial

No debería producirse ningún impacto en la mayoría de las organizaciones, ya que la sincronización de la hora debería estar completamente automatizada para todos los equipos que pertenecen al dominio. Los equipos que no pertenecen al dominio deberán configurarse para sincronizarlos con una fuente externa.

#### Crear un archivo de paginación

Esta configuración de directiva determina si los usuarios pueden crear y cambiar el tamaño de un archivo de paginación. En concreto, determina si pueden especificar un tamaño de archivo de paginación para una unidad concreta en el cuadro **Opciones de rendimiento** situado en la ficha **Avanzadas** del cuadro de diálogo **Propiedades del sistema**.

Los valores posibles para la configuración **Crear un archivo de paginación** son:

-   Lista de cuentas definida por el usuario

-   No está definido  

##### Vulnerabilidad

Los usuarios capaces de cambiar el tamaño de un archivo de paginación pueden hacerlo muy pequeño o moverlo a un volumen de almacenamiento muy fragmentado, lo que podría reducir el rendimiento del equipo.

##### Contramedida

Limite el derecho de usuario **Crear un archivo de paginación** a los usuarios del grupo **Administradores**.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Crear un objetoToken

Esta configuración de directiva determina si un proceso puede crear un token, que podrá utilizarse para conseguir acceso a cualquier recurso local cuando el proceso utilice NtCreateToken() u otra API de creación de token.

Los valores posibles para la configuración **Crear un objeto Token** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

El sistema operativo examina un token de acceso de usuario para determinar el nivel de privilegios del usuario. Los token de acceso se crean cuando los usuarios inician sesión en el equipo local o se conectan a un equipo remoto a través de la red. Cuando se revoca un privilegio, el cambio se registra, pero no se refleja en el token de acceso del usuario hasta la próxima vez que el usuario inicie sesión o se conecte. Un usuario con capacidad para crear o modificar tokens puede cambiar el nivel de acceso de cualquier cuenta que actualmente tenga una sesión iniciada, de modo que podría escalar sus propios privilegios o crear una condición de denegación de servicio.

##### Contramedida

No asigne el derecho de usuario **Crear un objeto Token** a ningún usuario. Los procesos que requieren este derecho de usuario deben utilizar la cuenta System, que ya lo incluye, en vez de una cuenta separada de usuario que tenga este derecho de usuario asignado.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Crear objetos globales

Esta configuración de directiva determina si los usuarios pueden crear objetos globales que están disponibles para todas las sesiones. Los usuarios pueden crear de todas formas objetos que son específicos a su propia sesión si no tienen este derecho de usuario.

Los valores posibles para la configuración **Crear objetos globales** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Aquellos usuarios que pueden crear objetos globales pueden afectar los procesos que se ejecutan en otras sesiones de usuario. Esto podría crear una serie de problemas, como errores en la aplicación o daños en los datos.

##### Contramedida

Limite el derecho de usuario **Crear objetos globales** a los miembros de los grupos **Administradores** y **Servicio** locales.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Crear objetos compartidos permanentes

Esta configuración de directiva determina si los usuarios pueden crear objetos de directorio en el administrador de objetos. Los usuarios que tienen esta capacidad pueden crear objetos compartidos de forma permanente, como dispositivos, semáforos y exclusiones múltiples. Este derecho de usuario es útil para componentes de modo de núcleo que amplían el espacio de nombres de objetos, y tienen este derecho de usuario intrínsecamente. Así pues, generalmente no es necesario asignar este privilegio de forma específica a ningún usuario.

Los valores posibles para la configuración **Crear objetos compartidos permanentes** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Los usuarios que tienen el derecho de usuario **Crear objetos compartidos permanentes** podrían crear objetos compartidos nuevos y exponer datos confidenciales a la red.

##### Contramedida

No asigne el derecho de usuario **Crear objetos compartidos permanentes** a ningún usuario. Los procesos que requieren este derecho de usuario deben utilizar la cuenta System (que ya incluye este derecho de usuario) en vez de una cuenta separada de usuario.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Depurar programas

Esta configuración de directiva determina si los usuarios pueden abrir o adjuntar en cualquier proceso, incluso en aquellos de los que no sean propietarios. Este derecho de usuario proporciona acceso a componentes críticos y confidenciales del sistema operativo.

Los posibles valores para el parámetro **Depurar programas** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

El derecho de usuario **Depurar programas** se puede aprovechar para capturar información confidencial del equipo de la memoria del sistema, o para tener acceso a las estructuras del núcleo o las aplicaciones, y modificarlas. Algunas herramientas de ataque aprovechan este derecho de usuario para extraer contraseñas con algoritmo hash e información de seguridad privada, o para llevar a cabo inserciones de código rootkit. De forma predeterminada, el derecho de usuario **Depurar programas** sólo se asigna a administradores, lo que ayuda a mitigar el riesgo de esta vulnerabilidad.

##### Contramedida

Revoque el derecho de usuario **Depurar programas** de todos los usuarios y grupos que no lo requieran.

##### Impacto potencial

Si revoca este derecho de usuario, nadie será capaz de depurar programas. Sin embargo, en circunstancias normales, rara vez se necesita esta función en los equipos de producción. Si surge un problema que requiera la depuración de una aplicación en un servidor de producción de forma temporal, puede cambiar el servidor a una unidad organizativa diferente y asignar el derecho de usuario **Depurar programas** a una directiva de grupo separada para esa unidad.

La cuenta de servicio que se utiliza para el servicio de clúster necesita el privilegio **Depurar programas**; si no fuera así, se produciría un error en los clústeres de Windows. Para obtener información adicional acerca de cómo configurar los clústeres de Windows en conjunción con el refuerzo de seguridad de un equipo, consulte el artículo 891597 de Microsoft Knowledge Base “[How to apply more restrictive security settings on a Windows Server 2003–based cluster server](http://support.microsoft.com/default.aspx?scid=891597)” en http://support.microsoft.com/default.aspx?scid=891597.

Las utilidades que se utilizan para administrar los procesos no podrán afectar a los procesos que no sean propiedad de la persona que se ejecuta las utilidades. Por ejemplo, la herramienta Kill.exe del Kit de Recursos de Windows Server 2003 precisa de este derecho de usuario para que un administrador termine los procesos que no haya iniciado.

Además, algunas versiones anteriores de Update.exe (que se utiliza para instalar actualizaciones de productos de Windows) requieren que la cuenta que aplica la actualización tenga este derecho de usuario. Si instala una de las revisiones que utiliza esta versión de Update.exe, el equipo podría dejar de responder. Para obtener más información, consulte el artículo 830846 de Microsoft Knowledge Base “[Windows Product Updates may stop responding or may use most or all the CPU resources](http://support.microsoft.com/default.aspx?scid=830846)” en http://support.microsoft.com/default.aspx?scid=830846.

#### Denegar el acceso desde la red a este equipo

Esta configuración de directiva determina si los usuarios pueden conectarse al equipo desde la red.

Los valores posibles para la configuración **Denegar el acceso desde la red a este equipo** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Los usuarios que pueden iniciar sesión en el equipo a través de la red pueden enumerar listas de nombres de cuentas, nombres de grupos y recursos compartidos. Los usuarios con permiso de acceso a recursos y archivos compartidos pueden conectarse a través de la red y, posiblemente, ver o modificar datos. Puede denegar de forma explícita este derecho de inicio de sesión a cuentas con alto riesgo (como la cuenta de invitado local y otras cuentas que no tienen necesidades empresariales para tener acceso al equipo a través de la red) para brindar un nivel de protección adicional.

##### Contramedida

Asigne el derecho de usuario **Denegar el acceso desde la red a este equipo** a las siguientes cuentas:

-   INICIO DE SESIÓN ANÓNIMO

-   Cuenta Administrador local integrada

-   Cuenta Invitado local

-   Cuenta integrada de soporte

-   Todas las cuentas de servicios

Una excepción importante a esta lista son todas las cuentas de servicio que se utilizan para iniciar servicios que necesiten conectarse al equipo a través de la red. Por ejemplo, si ha configurado una carpeta compartida para que los servidores web puedan tener acceso a ella y presentar su contenido mediante un sitio web, puede que sea necesario permitir la cuenta en la que se ejecuta IIS para iniciar la sesión en el servidor con las carpetas compartidas a través de la red. Este derecho de usuario es especialmente eficaz cuando necesita configurar servidores y estaciones de trabajo en las que se maneja información confidencial, debido a inquietudes de cumplimiento de la normatividad.

##### Impacto potencial

Si configura el derecho de usuario **Denegar el acceso desde la red a este equipo** para otros grupos, podría limitar las capacidades de los usuarios asignados a funciones administrativas específicas en su entorno. Debe verificar que las tareas delegadas no se ven afectadas de forma negativa.

#### Denegar el inicio de sesión como trabajo por lotes

Esta configuración de directiva determina si los usuarios pueden iniciar sesión a través de un servicio de cola por lotes, que es la característica en Windows Server 2003 que se utiliza para programar e iniciar trabajos automáticamente una o más veces en el futuro. Este derecho de usuario es necesario en aquellas cuentas que se emplean para iniciar trabajos programados a través del Programador de tareas.

Los valores posibles para la configuración **Denegar el inicio de sesión como trabajo por lotes** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Las cuentas que tienen el derecho de usuario **Denegar el inicio de sesión como trabajo por lotes** se podrían utilizar para programar los trabajos que podrían consumir recursos excesivos del equipo y provocar una condición de DoS.

##### Contramedida

Asigne el derecho de usuario **Denegar el inicio de sesión como trabajo por lotes** a la cuenta integrada de soporte y a la cuenta de invitado local.

##### Impacto potencial

Si asigna el derecho de usuario **Denegar el inicio de sesión como trabajo por lotes** a otras cuentas, podría negar a usuarios asignados a funciones administrativas específicas la capacidad de realizar sus actividades requeridas de trabajo. Debe confirmar que las tareas delegadas no se vean afectadas de forma negativa. Por ejemplo, si asigna este derecho de usuario a la cuenta IWAM\_*&lt;NombreEquipo&gt;*, el punto administración MSM fallará. En un equipo recién instalado con Windows Server 2003 esta cuenta no pertenece al grupo **Invitados**, pero en un equipo que se haya actualizado de Windows 2000 la cuenta es miembro del grupo **Invitados**. Por lo tanto, es importante que entienda qué cuentas pertenecen a los grupos a los que asigna el derecho de usuario **Denegar el inicio de sesión como trabajo por lotes.**

#### Denegar el inicio de sesión como servicio

Esta configuración de directiva determina si los usuarios pueden iniciar sesión como un servicio.

Los valores posibles para la configuración **Denegar el inicio de sesión como servicio** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Las cuentas que pueden iniciar sesión como servicio pueden utilizarse para configurar e iniciar nuevos servicios no autorizados, como aplicaciones de captura de teclado y otros programas malintencionados. La ventaja de la contramedida especificada se reduce en cierto modo por el hecho de que sólo los usuarios con privilegios administrativos pueden instalar y configurar servicios, de modo que un atacante que ya ha conseguido cierto nivel de acceso podría configurar el servicio para ejecutarlo con la cuenta System.

##### Contramedida

Esta guía recomienda que no asigne el derecho de usuario **Denegar el inicio de sesión como servicio** a ninguna cuenta, que es la configuración predeterminada. Puede que aquellas organizaciones que se preocupen mucho por la seguridad deseen asignar este derecho de usuario a grupos y cuentas que sepan con seguridad que nunca necesitarán iniciar sesión como servicio.

##### Impacto potencial

Si asigna el derecho de usuario **Denegar el inicio de sesión como servicio** a cuentas específicas, es posible que no se puedan iniciar los servicios y se podría producir una condición de DoS.

#### Denegar el inicio de sesión localmente

Esta configuración de directiva determina si los usuarios pueden iniciar sesión directamente en el teclado de equipo.

Los valores posibles para la configuración **Denegar el inicio de sesión localmente** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Una cuenta con la capacidad de iniciar sesión localmente se puede utilizar para iniciar una sesión en la consola del equipo. Si este derecho de usuario no se restringe a usuarios legítimos que necesiten iniciar sesión en la consola del equipo, cualquier usuario no autorizado podría descargar y ejecutar un código malintencionado para elevar sus privilegios.

##### Contramedida

Asigne el derecho de usuario **Denegar el inicio de sesión localmente** a la cuenta integrada de soporte. Si ha instalado componentes opcionales como ASP.NET, tal vez quiera asignar este derecho de usuario a cuentas adicionales que estos componentes requieren.

**Nota**: la cuenta Support\_388945a0 permite a los servicios de ayuda y soporte técnico interactuar con secuencias de comandos firmadas. Esta cuenta se utiliza principalmente para controlar el acceso a secuencias de comandos firmadas a las que se puede tener acceso desde los servicios de ayuda y soporte. Los administradores pueden utilizar esta cuenta para delegar en un usuario normal (sin acceso administrativo) la capacidad de ejecutar secuencias de comandos firmadas desde vínculos incrustados en los servicios de ayuda y soporte. Estas secuencias de comandos se pueden programar para que utilicen las credenciales de la cuenta Support\_388945a0 en lugar de las credenciales del usuario, con el fin de realizar operaciones administrativas específicas en el equipo local que, de otra manera, no serían compatibles con la cuenta del usuario normal.

Cuando el usuario delegado haga clic en un vínculo de los servicios de ayuda y soporte, la secuencia de comandos se ejecutará bajo el contexto de la cuenta Support\_388945a0. Esta cuenta tiene acceso limitado al equipo y se deshabilita de forma predeterminada.

##### Impacto potencial

Si asigna el derecho de usuario **Denegar el inicio de sesión localmente** a cuentas adicionales, podría limitar las capacidades de los usuarios que tienes asignadas funciones específicas en su entorno. Sin embargo, este derecho de usuario debe asignarse explícitamente a la cuenta ASPNET en equipos en los que se ejecuta IIS 6.0. Debe confirmar que las actividades delegadas no se verán afectadas de forma negativa.

#### Denegar inicio de sesión a través de Servicios de Terminal Server

Esta configuración de directiva determina si los usuarios pueden iniciar sesión en el equipo mediante una conexión a Escritorio remoto.

Los valores posibles para la configuración **Denegar inicio de sesión a través de Servicios de Terminal Server** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Una cuenta con este derecho puede utilizarse para iniciar sesión en la consola remota del equipo. Si este derecho de usuario no se restringe a usuarios legítimos que necesiten iniciar sesión en la consola del equipo, cualquier usuario no autorizado podría descargar y ejecutar un código malintencionado para elevar sus privilegios.

##### Contramedida

Asigne el derecho de inicio de sesión **Denegar inicio de sesión a través de Servicios de Terminal Server** a la cuenta Administrador local integrada y a todas las cuentas de servicio. Si ha instalado componentes opcionales como ASP.NET, tal vez quiera asignar este derecho de inicio de sesión a cuentas adicionales que estos componentes requieren.

##### Impacto potencial

Si asigna el derecho de usuario **Denegar inicio de sesión a través de Servicios de Terminal Server** a otros grupos, podría limitar las capacidades de los usuarios que tienes asignadas funciones administrativas específicas en su entorno. Las cuentas que tienen este derecho de usuario no podrán conectarse al equipo mediante los servicios de Terminal Server o la asistencia remota. Debe confirmar que las tareas delegadas no se vean afectadas de forma negativa.

#### Habilitar la opción De confianza para la delegación en las cuentas de usuario y de equipo

Esta configuración de directiva determina si los usuarios pueden cambiar la configuración **De confianza para la delegación** en un objeto de usuario o equipo en Active Directory. Los usuarios o equipos a los que se asigna este derecho de usuario también deben disponer de acceso de escritura a los indicadores de control de cuenta en el objeto.

La delegación de autenticación es una capacidad que las aplicaciones cliente/servidor de varios niveles emplean y que permite que el servicio de cliente utilice credenciales de cliente para autenticar un servicio de servidor. Para que esta configuración sea posible, se deben ejecutar tanto el cliente como el servidor bajo cuentas de confianza para la delegación.

Los valores posibles para la configuración **Habilitar la opción De confianza para la delegación en las cuentas de equipo de usuario** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

El mal uso del derecho de usuario **Habilitar la opción De confianza para la delegación en las cuentas de equipo de usuario** podría permitir que usuarios no autorizados suplantaran a otros usuarios en la red. Un atacante podría aprovechar este privilegio para obtener acceso a los recursos de la red y dificultar la determinación de lo ocurrido después de un incidente de la seguridad.

##### Contramedida

El derecho de usuario **Habilitar la opción De confianza para la delegación en las cuentas de equipo de usuario** sólo debe asignarse si resulta claro que se requiere esta funcionalidad. Cuando asigna este derecho, debe investigar el uso de la delegación restringida para controlar lo que pueden hacer las cuentas delegadas.

**Nota**: no existe motivo para asignar este derecho de usuario a cualquiera de los servidores miembro y estaciones de trabajo que pertenecen al dominio, porque no tiene sentido en dicho contexto. Sólo resulta importante para los controladores de dominio y equipos independientes.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Forzar el apagado de un sistema remoto

Esta configuración de directiva determina si un usuario puede apagar un equipo desde una ubicación remota de la red.

Los valores posibles para la configuración **Forzar el apagado desde un sistema remoto** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Cualquier usuario que pueda apagar un equipo puede provocar una condición de denegación de servicio. Por lo tanto, este derecho de usuario debe restringirse al máximo.

##### Contramedida

Restrinja el derecho de usuario **Forzar el apagado desde un sistema remoto** a miembros del grupo de **Administradores** o a otras funciones específicamente asignadas que requieren esta capacidad (como el personal del centro de operaciones no administrativas).

##### Impacto potencial

Si elimina el derecho de usuario **Forzar el apagado desde un sistema remoto** del grupo de **Operadores de servidor**, podría limitar las capacidades de los usuarios asignados a funciones administrativas específicas en su entorno. Debe confirmar que las actividades delegadas no se verán afectadas de forma negativa.

#### Generar auditorías de seguridad

Esta configuración de directiva determina si un proceso puede generar registros de auditoría en el registro de seguridad. Puede utilizar la información en el registro de seguridad para rastrear el acceso no autorizado a equipos.

Los valores posibles para la configuración **Generar auditorías de seguridad** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Un atacante puede emplear las cuentas que poseen derecho de escritura sobre el registro de seguridad para llenar ese registro con eventos que carecen de sentido. Si el equipo se ha configurado para sobrescribir los eventos cuando sea necesario, el atacante podría usar este método para eliminar la evidencia de las actividades no autorizadas que realiza. Si el equipo se ha configurado para apagarse cuando no pueda escribir en el registro de seguridad y no se ha configurado para crear automáticamente una copia de seguridad de los archivos de registro, este método se podría utilizar para crear una denegación de servicio.

##### Contramedida

Asegúrese de que sólo las cuentas de servicio y servicio de red tienen asignado el derecho de usuario **Generar auditorías de seguridad**.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Suplantar a un cliente después de la autenticación

El derecho de usuario **Suplantar a un cliente después de la autenticación** permite a los programas que se ejecutan en nombre de un usuario (u otra cuenta especificada) para que puedan actuar a favor del usuario. Si este derecho de usuario se requiere para este tipo de suplantación, un usuario no autorizado no podrá convencer a un cliente de que se conecte, por ejemplo, por llamada a procedimiento remoto (RPC) o canalizaciones con nombre, a un servicio creado para suplantar a ese cliente, que podría elevar los permisos del usuario no autorizado a niveles administrativos o de sistema.

Los servicios que se inician mediante el administrador de control de servicios tienen agregado de forma predeterminada el grupo **Servicio** integrado a sus tokens de acceso. Los servidores COM que se inician mediante la infraestructura COM y se configuran para que se ejecuten bajo cuentas específicas tienen agregado el grupo **Servicio** a sus tokens de acceso. Como consecuencia, al iniciarse estos servicios se les asigna este derecho de usuario.

Además, un usuario puede suplantar un token de acceso si se da alguna de las siguientes condiciones:

-   El token de acceso que se está suplantando es para este usuario.

-   El usuario, en esta sesión de inicio, inició sesión en la red con credenciales explícitas para crear el token de acceso.

-   El nivel solicitado es menor que Suplantar, como Anónimo o Identificar.

Debido a estas condiciones, normalmente los usuarios no necesitan que se les asigne este derecho de usuario.

Los valores posibles para la configuración **Suplantar a un cliente después de la autenticación** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Un atacante con el derecho de usuario **Suplantar a un cliente después de la autenticación** podría crear un servicio, engañar a un cliente para que se conecte al servicio, y entonces suplantar a ese cliente para elevar el nivel de acceso del atacante al mismo del cliente.

##### Contramedida

En servidores miembro, asegúrese de que sólo los grupos **Administradores** y **Servicio** tienen asignado el derecho de usuario **Suplantar a un cliente después de la autenticación**. Los equipos en los que se ejecuta IIS 6.0 deben tener este derecho de usuario asignado al grupo IIS\_WPG (que lo concede a la cuenta Servicio de red).

##### Impacto potencial

En la mayoría de los casos esta configuración no tendrá ninguna repercusión. Si ha instalado componentes opcionales como ASP.NET o IIS, tal vez necesite asignar el derecho de usuario **Suplantar a un cliente después de la autenticación** a cuentas adicionales que esos componentes requieran, como IUSR\_*&lt;NombreEquipo&gt;*, IIS\_WPG, ASP.NET o IWAM\_*&lt;NombreEquipo&gt;*.

#### Aumentar la prioridad de programación

Esta configuración de directiva determina si los usuarios pueden aumentar la clase de prioridad base de un proceso. (Aumentar la prioridad relativa dentro de una clase de prioridad no es una operación privilegiada). Las herramientas administrativas incluidas en el sistema operativo no necesitan este derecho de usuario, pero las herramientas de desarrollo de software sí pueden requerirlo.

Los valores posibles para la configuración **Aumentar la prioridad de programación** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Un usuario al que se asigna este derecho de usuario puede aumentar la prioridad de programación de un proceso a tiempo real, dejando poco tiempo de procesamiento para los demás procesos, lo que puede provocar una condición de denegación de servicio.

##### Contramedida

Compruebe que el derecho de usuario **Aumentar la prioridad de programación** se asigna solamente al grupo Administradores.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Cargar y descargar controladores de dispositivo

Esta configuración de directiva determina si los usuarios pueden cargar y descargar dinámicamente controladores de dispositivos. Este derecho de usuario no es necesario si ya existe un controlador firmado para el nuevo hardware en el archivo Driver.cab del equipo.

Los valores posibles para la configuración **Cargar y descargar controladores de dispositivos** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Los controladores de dispositivos se ejecutan como un código con privilegios elevados. Un usuario con el derecho de usuario **Cargar y descargar controladores de dispositivos** puede instalar involuntariamente un código malicioso que se haga pasar por un controlador de dispositivo. Los administradores deben tener más cuidado e instalar sólo aquellos controladores con firmas digitales comprobadas.

**Nota**: debe disfrutar de este derecho de usuario y, además, pertenecer al grupo **Administradores** o **Usuarios avanzados** para instalar un nuevo controlador para una impresora local o administrar una impresora local y configurar valores predeterminados de opciones como impresión a doble cara. Este requisito de tener el derecho de usuario y pertenecer al grupo **Administradores** o **Usuarios avanzados** es nuevo para Windows XP y Windows Server 2003.

##### Contramedida

No asigne el controlador de dispositivo **Cargar y descargar controladores de dispositivo** a ningún usuario o grupo que no sea **Administradores** en servidores miembro. En controladores de dominio, no asigne este derecho de usuario a ningún usuario ni grupo que no sea **Administradores de dominio**.

##### Impacto potencial

Si elimina el derecho de usuario **Cargar y descargar controladores de dispositivo** del grupo de **Operadores de impresión** o de otras cuentas, podría limitar las capacidades de los usuarios asignados a funciones administrativas específicas en su entorno. Debe asegurarse de que las tareas delegadas no se verán afectadas de forma negativa.

#### Bloquear páginas en la memoria

Esta configuración de directiva determina si un proceso puede mantener datos en la memoria física. Esto evita que el equipo pagine los datos en la memoria virtual del disco. Si asigna este derecho de usuario, podría afectar de manera significativa el rendimiento del equipo.

Los valores posibles para la configuración **Bloquear páginas en la memoria** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Los usuarios con el derecho de usuario **Bloquear páginas en la memoria** podrían asignar memoria física a varios procesos, lo que podría dejar sin memoria o con poca memoria a otros procesos y tener como resultado una condición DoS.

##### Contramedida

No asigne el derecho de usuario **Bloquear páginas en la memoria** a ninguna cuenta.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Iniciar sesión como proceso por lotes

Esta configuración de directiva determina si los usuarios pueden iniciar sesión mediante un servicio de cola por lotes como el servicio de Programador de tareas. Cuando un administrador utiliza el Asistente para agregar tarea programada con el fin de programar una tarea y ejecutarla bajo un nombre de usuario y contraseña específicos, se asignará automáticamente a dicho usuario el derecho de usuario **Iniciar sesión como proceso por lotes**. Cuando llegue el momento programado, el servicio del Programador de tareas hará que el usuario inicie sesión como trabajo por lotes, en lugar de usuario interactivo, y la tarea se ejecutará en el contexto de seguridad del usuario.

Los valores posibles para la configuración **Iniciar sesión como proceso por lotes** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

El derecho de usuario **Iniciar sesión como proceso por lotes** presenta una vulnerabilidad de bajo riesgo. Para la mayoría de las organizaciones, la configuración predeterminada es suficiente.

##### Contramedida

Debe permitir que el equipo administre automáticamente este derecho de inicio de sesión si desea permitir que la programación de tareas se ejecute para cuentas de usuario específicas. Si no desea utilizar el Programador de tareas de este modo, configure el derecho de usuario **Iniciar sesión como proceso por lotes** sólo para la cuenta de servicio local y la cuenta de soporte local (Support\_388945a0). Para los servidores IIS, debe configurar esta directiva localmente, en lugar de hacerlo a través de directivas de grupo basadas en un dominio, de forma que pueda garantizar que las cuentas locales *IUSR\_&lt;NombreEquipo&gt;* y *IWAM\_&lt;NombreEquipo&gt;* tienen este derecho de inicio de sesión.

##### Impacto potencial

Si configura **Iniciar sesión como proceso por lotes** a través de directivas de grupo basadas en el dominio, el equipo no podrá asignar el derecho de usuario a cuentas que se utilizan para trabajos programados en el Programador de tareas. Si instala componentes opcionales como ASP.NET o IIS, tal vez deba asignar este derecho de usuario a cuentas adicionales que estos componentes requieren. Por ejemplo, IIS requiere la asignación de este derecho de usuario al grupo **IIS\_WPG** y a las cuentas IUSR\_*&lt;NombreEquipo&gt;, *ASPNET e IWAM\_*&lt;NombreEquipo&gt;*. Si este derecho de usuario no se asigna a este grupo y estas cuentas, IIS será incapaz de ejecutar algunos objetos COM que son necesarios para la funcionalidad apropiada.

#### Iniciar sesión como servicio

Esta configuración de directiva determina si una entidad principal de seguridad puede iniciar sesión como un servicio. Los servicios se pueden configurar para ejecutarlos con las cuentas System local, Servicio local o Servicio de red, que tienen un derecho integrado para iniciar sesión como servicio. Todo servicio que se ejecute en una cuenta de usuario diferente debe tener asignado este derecho de usuario.

Los valores posibles para la configuración **Iniciar sesión como servicio** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

**Iniciar sesión como servicio** es un derecho de usuario muy amplio porque permite que las cuentas inicien servicios de red o servicios que se ejecutan continuamente en un equipo, aun cuando nadie se encuentre en una sesión en la consola. El riesgo se reduce por el hecho de que sólo los usuarios con privilegios administrativos pueden instalar y configurar servicios. Un atacante que ya ha conseguido este nivel de acceso puede configurar el servicio para ejecutarse con la cuenta de sistema local.

##### Contramedida

El conjunto predeterminado de entidades principales de seguridad que tienen el derecho de usuario **Iniciar sesión como servicio** está restringido al sistema local, al servicio local y al servicio de red, que son cuentas locales integradas. Debe minimizar el número de otras cuentas que tienen este derecho de usuario.

##### Impacto potencial

En la mayoría de los equipos, ésta es la configuración predeterminada y no habrá repercusiones negativas. Sin embargo, si ha instalado componentes opcionales como ASP.NET o IIS, tal vez tenga que asignar el derecho de usuario **Iniciar sesión como servicio a cuentas adicionales** a cuentas adicionales que estos componentes requieren. IIS requiere que este derecho de usuario se conceda explícitamente a la cuenta de usuario ASPNET.

#### Administrar registros de auditoría y de seguridad

Esta configuración de directiva determina si los usuarios pueden especificar opciones de auditoría de acceso a objetos para recursos individuales, como archivos, objetos de Active Directory y claves de registro. Las auditorías de acceso a objetos no se realizan a menos que las habilite mediante la **Directiva de auditoría**, situada en **Configuración de seguridad**, **Directivas locales**. Un usuario al que se asigna este derecho de usuario puede, además, ver y borrar el registro de eventos de seguridad desde el visor de eventos.

Los valores posibles para la configuración **Administrar registros de auditoría y seguridad** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

La capacidad de administrar el registro de eventos de seguridad es un derecho de usuario importante que debe protegerse estrictamente. Cualquiera con este privilegio de usuario podría borrar el registro de seguridad, lo que eliminaría pruebas importantes sobre actividades no autorizadas.

##### Contramedida

Asegúrese de que sólo el grupo **Administradores** local tiene el derecho de usuario **Administrar registros de auditoría y seguridad**.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Modificar valores de entorno del firmware

Esta configuración de directiva determina si los usuarios pueden modificar las variables de entorno del sistema mediante un proceso a través de una API o mediante un usuario a través de Propiedades del sistema.

Los valores posibles para la configuración **Modificar valores de entorno del firmware** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Cualquier persona que posea el derecho de usuario **Modificar valores de entorno del firmware** podría configurar los parámetros de un componente de hardware para generar un error, lo que puede provocar la corrupción de datos o una condición DoS.

##### Contramedida

Asegúrese de que sólo el grupo **Administradores** local tenga asignado el derecho de usuario **Modificar valores de entorno del firmware**.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Realizar tareas de mantenimiento de volúmenes

Esta configuración de directiva determina si los usuarios no administrativos o remotos pueden realizar las tareas de administración de disco o volumen, como desfragmentar un volumen existente, crear o eliminar volúmenes y ejecutar la herramienta de limpieza de disco. Windows Server 2003 comprueba este derecho de usuario en un token de acceso del usuario cuando un proceso que se ejecuta en un contexto de seguridad del usuario llama a SetFileValidData().

Los valores posibles para la configuración **Realizar tareas de mantenimiento de volúmenes** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Un usuario que tiene asignado el derecho de usuario **Realizar tareas de mantenimiento de volúmenes** podría borrar un volumen, lo que podría tener como resultado la pérdida de datos o una condición DoS.

##### Contramedida

Asegúrese de que sólo el grupo **Administradores** local tenga asignado el derecho de usuario **Realizar tareas de mantenimiento de volúmenes**.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Hacer perfil de un solo proceso

Esta configuración de directiva determina si los usuarios pueden probar el rendimiento de un proceso de aplicación. Por lo general no necesita este derecho de usuario para utilizar el complemento Rendimiento de la Microsoft Management Console (MMC). Sin embargo, sí necesita este derecho de usuario si el monitor de sistema se configura para reunir datos a través del Instrumental de administración de Windows (WMI).

Los valores posibles para la configuración **Hacer perfil de un solo proceso** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

El derecho de usuario **Hacer perfil de un solo proceso** presenta una vulnerabilidad moderada. Un atacante con este derecho de usuario podría supervisar el rendimiento de un equipo para intentar identificar procesos críticos que quizás quieran atacar directamente. El atacante también puede determinar cuáles son los procesos que se ejecutan en el sistema para poder identificar las contramedidas que deberá evitar, como un software antivirus, un sistema de detección de intrusos o los usuarios que hayan iniciado sesión en el equipo.

##### Contramedida

Asegúrese de que sólo el grupo **Administradores** local tenga asignado el derecho de usuario **Hacer perfil de un solo proceso**.

##### Impacto potencial

Si elimina el derecho de usuario **Hacer perfil de un solo proceso** del grupo **Usuarios avanzados** o de otras cuentas, podría limitar las capacidades de los usuarios asignados a funciones administrativas específicas en su entorno. Debe asegurarse de que las tareas delegadas no se verán afectadas de forma negativa.

#### Perfilar el rendimiento del sistema

Esta configuración de directiva determina si un usuario puede probar el rendimiento de procesos del sistema en un equipo. El complemento Rendimiento de MMC necesita este privilegio solamente si se configura para recopilar datos utilizando WMI. Por lo general no necesita este derecho de usuario para utilizar el complemento Rendimiento. Sin embargo, sí necesita este derecho de usuario si el monitor de sistema se configura para reunir datos a través de WMI.

Los valores posibles para la configuración **Perfilar el rendimiento del sistema** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

El derecho de usuario **Perfilar el rendimiento del sistema** presenta una vulnerabilidad moderada. Un atacante con este derecho de usuario podría supervisar el rendimiento de un equipo para intentar identificar procesos críticos que quizás quieran atacar directamente. El atacante también puede determinar cuáles son los procesos que están activos en el equipo para poder identificar las contramedidas que deberá evitar, como un software antivirus o un sistema de detección de intrusos.

##### Contramedida

Asegúrese de que sólo el grupo **Administradores** local tenga asignado el derecho de usuario **Perfilar el rendimiento del sistema**.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Quitar el equipo de la estación de acoplamiento

Esta configuración de directiva determina si el usuario de un equipo portátil puede hacer clic en **Retirar equipo** en el menú **Inicio** para quitar el equipo de la estación de acoplamiento.

Los valores posibles para la configuración **Quitar el equipo de la estación de acoplamiento** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Cualquiera que tenga el derecho de usuario **Quitar el equipo de la estación de acoplamiento** puede retirar un equipo portátil de su estación de acoplamiento. El valor de esta contramedida se reduce por varios factores:

-   si un atacante puede reiniciar el equipo, podría quitarlo de la estación de acoplamiento después de iniciarse BIOS, pero antes de iniciarse el sistema operativo.

-   Este parámetro no afecta a los servidores, ya que normalmente no se instalan en una estación de acoplamiento.

-   Un atacante podría robar el equipo y la estación de acoplamiento juntos.

##### Contramedida

Asegúrese de que sólo los grupos **Administradores** y **Usuarios avanzados** locales tengan asignado el derecho de usuario **Quitar el equipo de la estación de acoplamiento**.

##### Impacto potencial

Esta configuración es la configuración predeterminada, por lo que debe tener una repercusión mínima. Sin embargo, si los usuarios de la organización no pertenecen a los grupos **Usuarios avanzados** o **Administradores**, no podrán quitar sus propios equipos portátiles de las estaciones de acoplamiento sin antes apagarlos. Por lo tanto, puede que desee asignar el privilegio **Quitar el equipo de la estación de acoplamiento** al grupo **Usuarios** local para los equipos portátiles.

#### Reemplazar un token a nivel de proceso

Esta configuración de directiva determina si un proceso principal puede reemplazar el token de acceso asociado a un proceso secundario.

Los valores posibles para la configuración **Reemplazar un token de nivel de proceso** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Un usuario con el privilegio **Reemplazar un token de nivel de proceso** es capaz de iniciar procesos como otros usuarios. Podrían utilizar este método para ocultar sus acciones no autorizadas en el equipo. (En equipos con Windows 2000, el uso del derecho de usuario **Reemplazar un token de nivel de proceso** también requiere que el usuario tenga el derecho de usuario **Ajustar las cuotas de memoria para un proceso**, que ya se ha mencionado en este capítulo).

##### Contramedida

Para servidores miembro, asegúrese de que sólo las cuentas de servicio local y servicio de red tienen asignado el derecho de usuario **Reemplazar un token de nivel de proceso**.

##### Impacto potencial

En la mayoría de los equipos, ésta es la configuración predeterminada y no habrá repercusiones negativas. Sin embargo, si ha instalado componentes opcionales como ASP.NET o IIS, tal vez tenga que asignar el privilegio **Reemplazar un token de nivel de proceso** a cuentas adicionales. Por ejemplo, IIS requiere que a las cuentas de servicio, servicio de red e IWAM\_*&lt;NombreEquipo&gt;* se les conceda explícitamente este derecho de usuario.

#### Restaurar archivos y directorios

Esta configuración de directiva determina si un usuario puede eludir los permisos de archivo y directorio al restaurar archivos o directorios de una copia de seguridad y si puede establecer cualquier entidad principal de seguridad válida como propietaria de un objeto.

Los valores posibles para la configuración **Restaurar archivos y directorios** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Un atacante con el derecho de usuario **Restaurar archivos y directorios** podría restaurar datos confidenciales en un equipo y sobrescribir datos más recientes, lo que podría provocar una pérdida de datos importantes, corrupción de los datos o una condición de denegación de servicio. Un atacante podría sobrescribir los archivos ejecutables que utilizan los administradores o servicios del sistema legítimos con versiones que incluyen código malintencionado para concederse a sí mismos privilegios elevados, poner en peligro los datos o instalar puertas traseras para seguir teniendo acceso al equipo.

**Nota**: incluso si se configura esta contramedida, un atacante podría restaurar datos en un equipo dentro de un dominio que controle. Por lo tanto, es importante que las organizaciones protejan los medios que utilizan para realizar copias de seguridad de los datos.

##### Contramedida

Asegúrese de que sólo el grupo local **Administradores** tenga asignado el derecho de usuario **Restaurar archivos y directorios**, a menos que su organización haya definido claramente funciones de personal para operaciones de copia de seguridad y restauración.

##### Impacto potencial

Si elimina el derecho de usuario **Restaurar archivos y directorios** del grupo **Operadores de copia** y de otras cuentas, puede que aquellos usuarios en los que se han delegado determinadas tareas no puedan realizarlas. Debe comprobar que este cambio no afecte de forma negativa la capacidad del personal de la organización para realizar sus tareas.

#### Cerrar el sistema

Esta configuración de directiva determina si un usuario puede apagar el equipo local.

Los valores posibles para la configuración **Apagar el sistema** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

La capacidad para apagar los controladores de dominio se debería limitar a una pequeña cantidad de administradores de confianza. Aunque el derecho de usuario **Apagar el sistema** requiere de la capacidad de iniciar sesión en el servidor, debe tener cuidado con las cuentas y grupos a los que se concede permiso para apagar un controlador de dominio.

Cuando un controlador de dominio se apaga, ya no está disponible para procesar inicios de sesión o directivas de grupo ni para responder consultas de Protocolo ligero de acceso a directorios (LDAP). Si apaga controladores de dominio que poseen funciones de operaciones maestras únicas flexibles (FSMO), puede deshabilitar una funcionalidad importante del dominio, como el procesamiento de inicios de sesión para las nuevas contraseñas, que es la función del emulador del controlador de dominio principal.

##### Contramedida

Asegúrese de que sólo los grupos **Administradores** y **Operadores de copia** tengan asignado el derecho de usuario **Apagar el sistema** en los servidores miembro y que sólo el grupo **Administradores** lo tenga en los controladores de dominio.

##### Impacto potencial

Si quita estos grupos predeterminados del derecho de usuario **Apagar el sistema**, podrían limitarse las capacidades delegadas de las funciones asignadas en el entorno. Debe confirmar que las actividades delegadas no se verán afectadas de forma negativa.

#### Sincronizar los datos del servicio de directorio

Esta configuración de directiva determina si un proceso puede leer todos los objetos y propiedades del directorio, independientemente de la protección de los objetos y las propiedades. Este privilegio es necesario para poder usar los servicios de sincronización (dirsync) de directorios LDAP.

Los valores posibles para la configuración **Sincronizar los datos del servicio de directorio** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

El derecho de usuario **Sincronizar los datos del servicio de directorio** afecta a los controladores de dominio; sólo los controladores de dominio deben ser capaces de sincronizar datos del servicio de directorio. Los controladores de dominio tienen este derecho de forma intrínseca, ya que el proceso de sincronización se ejecuta en el contexto de la cuenta System en los controladores de dominio. Un atacante que tiene este derecho de usuario puede ver toda la información almacenada en el directorio. A continuación, puede utilizar parte de esta información para facilitar otros ataques o exponer datos confidenciales, como números de teléfono directos o direcciones físicas.

##### Contramedida

Asegúrese de que ninguna cuenta tenga asignado el derecho de usuario **Sincronizar los datos del servicio de directorio**.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Tomar posesión de archivos u otros objetos

Esta configuración de directiva determina si un usuario puede tomar posesión de cualquier objeto que se pueda asegurar del equipo, como los objetos de Active Directory, archivos y carpetas NTFS, impresoras, claves de registro, servicios, procesos y subprocesos.

Los valores posibles para la configuración **Tomar posesión de archivos u otros objetos** son:

-   Lista de cuentas definida por el usuario

-   No está definido

##### Vulnerabilidad

Cualquier usuario con el derecho de usuario **Tomar posesión de archivos u otros objetos** puede tomar el control de cualquier objeto, independientemente de los permisos del objeto, y entonces realizar los cambios que desee en ese objeto. Estos cambios podrían provocar que los datos se expongan o dañen o que se produzca una condición de denegación de servicio.

##### Contramedida

Asegúrese de que sólo el grupo **Administradores** local tiene el derecho de usuario **Tomar posesión de archivos u otros objetos**.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

[](#mainsection)[Principio de la página](#mainsection)

### Información adicional

Los siguientes vínculos proporcionan información adicional acerca de la asignación de derechos de usuario en Windows Server 2003 y Windows XP.

-   Podrá encontrar información completa sobre la asignación de derechos de usuario con SCE en la sección "[Asignación de derechos de usuario](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/71b2772f-e3c0-4134-b7f0-54c244ee9aef.mspx)" de la ayuda en línea del Editor de configuración de seguridad de Windows Server 2003 en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/
    serverhelp/71b2772f-e3c0-4134-b7f0-54c244ee9aef.mspx.

-   Podrá encontrar información completa sobre la asignación de derechos de usuario locales en equipos con Windows XP en el tema de ayuda "[To assign user rights for your local computer](http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/lpe_assign_user_right.mspx)" en www.microsoft.com/resources/documentation/windows/xp/all/proddocs/
    en-us/lpe\_assign\_user\_right.mspx.

-   Para obtener más información sobre la asignación de derechos de usuario en Windows XP, consulte la sección "[Asignación de derechos de usuario](http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/uratopnode.mspx)" en la documentación en línea de Windows XP Professional en www.microsoft.com/resources/documentation/windows/xp/all/proddocs/
    en-us/uratopnode.mspx.

-   Para obtener más información acerca de cómo personalizar la interfaz de usuario del Editor de configuración de seguridad, consulte el artículo de Microsoft Knowledge Base "[Cómo agregar configuraciones personalizadas del Registro al Editor de configuración de seguridad](http://support.microsoft.com/?scid=214752)" en http://support.microsoft.com/?scid=214752.

-   Para obtener más información acerca de cómo crear archivos de plantillas administrativas personalizadas en Windows, consulte el artículo de Microsoft Knowledge Base "[Cómo crear plantillas administrativas personalizadas en Windows 2000](http://support.microsoft.com/?scid=323639)" en http://support.microsoft.com/?scid=323639.

[](#mainsection)[Principio de la página](#mainsection)

### Capítulo 5: Opciones de seguridad

La sección Opciones de seguridad de directiva de grupo permite habilitar o deshabilitar la configuración de seguridad de los equipos para firmas digitales de datos, nombres de cuenta de administrador e invitado, acceso a la unidad de disquete y de CD-ROM, el comportamiento de la instalación de controladores y los mensajes de inicio de sesión. El libro de Microsoft Excel "Configuración de la seguridad y los servicios predeterminados de Windows", que se incluye en la versión descargable de esta guía, ofrece información sobre la configuración predeterminada.

[](#ekaa)[Configuración de opciones de seguridad](#ekaa)
[](#elaa)[Información adicional](#kkkk)

### Configuración de opciones de seguridad

Puede establecer la configuración de las opciones de seguridad en la siguiente ubicación del Editor de objetos de directiva de grupo:

**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\**
**Opciones de seguridad**

#### Cuentas: estado de la cuenta de administrador

Esta configuración de directiva habilita o deshabilita la cuenta de Administrador para condiciones de operación normales. Si inicia un equipo en modo seguro, la cuenta de Administrador siempre está habilitada, independientemente de cómo haya establecido esta configuración de directiva.

Los valores posibles para la configuración de **Cuentas: estado de la cuenta de administrador** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

En algunas organizaciones, el mantenimiento de un programa periódico de cambios de contraseña de las cuentas locales puede suponer un enorme reto de administración. Por lo tanto, puede que desee deshabilitar la cuenta de administrador integrada en vez de realizar cambios periódicos de contraseña para protegerla de ataques. Otro motivo para deshabilitar la cuenta integrada reside en que no se puede bloquear, independientemente de que acumule errores de inicio de sesión, lo que la convierte en un blanco obvio para ataques de fuerza bruta que intentan adivinar contraseñas. Además, esta cuenta tiene un identificador de seguridad (SID) muy conocido y existen herramientas de terceros con las que se puede autenticar a través de SID en lugar del nombre de cuenta. Esto quiere decir que, aun cuando se haya cambiado el nombre de la cuenta de administrador, un atacante puede realizar un ataque de fuerza bruta utilizando el SID para iniciar sesión.

##### Contramedida

Configure el valor **Cuentas: estado de la cuenta de administrador** como **Deshabilitado** para que la cuenta de administrador ya no se pueda utilizar durante un inicio normal del sistema.

##### Impacto potencial

En algunas circunstancias pueden presentarse problemas de mantenimiento si deshabilita la cuenta de Administrador. Por ejemplo, si el canal seguro entre un equipo miembro y el controlador de dominio presenta un error en un entorno de dominio por cualquier razón y hay otra cuenta de Administrador local, debe reiniciar en modo seguro para corregir el problema que interrumpió el canal seguro.

Si la contraseña de administrador actual no cumple los requisitos pertinentes, no podrá volver a habilitarla una vez que se deshabilite. Si esto ocurre, tendrá que ser otro miembro del grupo de administradores quien establezca la contraseña en la cuenta de administradores con la herramienta **Usuarios locales y grupos**.

#### Cuentas: estado de la cuenta de invitado

Esta configuración de directiva determina si la cuenta de Invitado se habilita o deshabilita.

Los valores posibles para la configuración de **Cuentas: estado de la cuenta de invitado** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

La cuenta predeterminada de invitado permite que los usuarios de red no autenticados inicien sesión como invitados y sin la necesidad de una contraseña. Estos usuarios no autorizados podrían tener acceso a cualquier recurso disponible para la cuenta de invitado en la red. Esta capacidad implica que cualquier recurso compartido de red con permisos que otorguen acceso a la cuenta de invitado, el grupo **Invitados** o el grupo **Todos** será accesible a través de la red, lo que podría provocar la exposición o el daño de datos.

##### Contramedida

Configure el valor **Cuentas: estado de la cuenta de invitado** como **Deshabilitado** para hacer que la cuenta de invitado ya no se pueda volver a utilizar.

##### Impacto potencial

Todos los usuarios de la red se deberán autenticar para poder tener acceso a los recursos compartidos. En caso de que haya deshabilitado la cuenta de invitado y haya establecido el valor **Acceso de red: modelo de seguridad y recursos compartidos** en **Sólo invitado**, se producirá un error en el inicio de sesión de red, como el realizado por el servidor de red Microsoft (servicio SMB). Esta configuración de directiva debería apenas afectar a la mayoría de las organizaciones, dado que se trata del valor predeterminado en Microsoft Windows® 2000, Windows XP y Windows Server™ 2003.

#### Cuentas: limitar el uso de cuentas locales con contraseña en blanco sólo para iniciar la consola

Esta configuración de directiva determina si se permiten los inicios de sesión interactivos remotos mediante servicios de red como Servicios Terminal Server, Telnet y Protocolo de transferencia de archivos (FTP) para cuentas locales con contraseñas en blanco. Si habilita esta configuración de directiva, una cuenta local deberá tener una contraseña que no esté en blanco para realizar un inicio de sesión de red o interactivo desde un cliente remoto.

Los valores posibles para la configuración de **Cuentas: limitar el uso de cuentas locales con contraseña en blanco sólo para iniciar la consola** son:

-   Habilitada

-   Deshabilitado

-   No está definido

**Nota**: esta configuración de directiva no influye en los inicios de sesión interactivos que se llevan a cabo físicamente en la consola, o en aquellos inicios de sesión que emplean cuentas de dominio.

**Precaución**: las aplicaciones de terceros que usan inicios de sesión remotos pueden pasar por alto esta configuración de directiva.

##### Vulnerabilidad

Las contraseñas en blanco constituyen una seria amenaza para la seguridad del equipo y, por lo tanto, deberían prohibirse tanto con medidas técnicas pertinentes como con directivas corporativas. De hecho, la configuración predeterminada para los dominios del servicio de directorio Active Directory® de Windows Server 2003 requiere contraseñas complejas con un mínimo de siete caracteres. Sin embargo, si un usuario con capacidad para crear cuentas nuevas elude sus directivas de contraseñas basadas en el dominio, podría crear cuentas con contraseñas en blanco. Así, un usuario podría crear un equipo independiente, generar una o varias cuentas con contraseñas en blanco y, a continuación, unir el equipo con el dominio. En tal caso las cuentas locales con contraseñas en blanco aún funcionarían, Todo aquel que conozca el nombre de una de estas cuentas sin proteger podría utilizarlo para iniciar sesión.

##### Contramedida

Habilite la opción **Cuentas: limitar el uso de cuentas locales con contraseña en blanco sólo para iniciar la consola**.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Cuentas: cambiar el nombre de la cuenta del administrador

Esta configuración de directiva determina si un nombre de cuenta diferente se asocia con el SID para la cuenta de Administrador.

Los valores posibles para la configuración de **Cuentas: cambiar el nombre de la cuenta del administrador** son:

-   Texto definido por el usuario

-   No está definido

##### Vulnerabilidad

La cuenta de Administrador existe en todos los equipos con sistemas operativos Windows 2000, Windows Server 2003 o Windows XP Professional. Si cambia el nombre de esta cuenta, hace que resulte un poco más difícil averiguar este nombre de usuario con privilegios y la combinación de la contraseña por parte de personas no autorizadas.

La cuenta de Administrador integrada no se puede bloquear, por muchas veces que un atacante use una contraseña incorrecta. Esto la convierte en un blanco popular para los ataques de fuerza bruta que intentan averiguar contraseñas. El valor de esta contramedida disminuye, ya que esta cuenta tiene un identificador de seguridad (SID) muy conocido y existen herramientas de terceros que permiten la autenticación mediante el SID en lugar del nombre de cuenta. Por lo tanto, aun cuando se haya cambiado el nombre de la cuenta de administrador, un atacante puede realizar un ataque de fuerza bruta utilizando el SID para iniciar sesión.

##### Contramedida

Especifique un nombre nuevo en la configuración **Cuentas: cambiar el nombre de la cuenta del administrador** para cambiar el nombre de la cuenta de Administrador.

**Nota**: en capítulos posteriores, esta configuración de directiva no se configura en las plantillas de seguridad, ni se sugiere un nuevo nombre de usuario para la cuenta en la guía. Las plantillas omiten esta configuración de directiva para que las numerosas organizaciones que utilizan esta guía no implementen el mismo nombre de usuario nuevo en sus entornos.

##### Impacto potencial

Deberá informar del nuevo nombre de cuenta a los usuarios autorizados para usarla. (La orientación para este parámetro supone que la cuenta de Administrador no se ha deshabilitado, como ya se recomendó en este capítulo.)

#### Cuentas: cambiar el nombre de la cuenta de invitado

El uso del valor **Cuentas: cambiar el nombre de la cuenta de invitado** determina si un nombre de cuenta distinto se relaciona con el SID de la cuenta de invitado.

Los valores que se pueden seleccionar para esta configuración de Directiva de grupo son los siguientes:

-   Texto definido por el usuario

-   No está definido

##### Vulnerabilidad

La cuenta de Invitado existe en todos los equipos con sistemas operativos Windows 2000, Windows Server 2003 o Windows XP Professional. Si cambia el nombre de esta cuenta resulta un poco más difícil averiguar este nombre de usuario con privilegios y la combinación de la contraseña por parte de personas no autorizadas.

##### Contramedida

Especifique un nombre nuevo en la configuración **Cuentas: cambiar el nombre de la cuenta de invitado** para cambiar el nombre de esta cuenta.

**Nota**: en capítulos posteriores, esta configuración de directiva no se configura en las plantillas de seguridad, ni se sugiere un nuevo nombre de usuario para la cuenta en la guía. Las plantillas omiten esta configuración de directiva para que las numerosas organizaciones que utilizan esta guía no implementen el mismo nombre de usuario nuevo en sus entornos.

##### Impacto potencial

El impacto debería ser mínimo, dado que la cuenta de invitado se deshabilita de forma predeterminada en Windows 2000, Windows XP y Windows Server 2003.

#### Auditoría: auditar el acceso de objetos globales del sistema

Si habilita esta configuración de directiva, se aplicará una lista de control de acceso de sistema (SACL) predeterminada cuando el equipo crea objetos de sistema tales como exclusiones mutuas, eventos, semáforos y dispositivos de MS-DOS®. Si habilita también el valor **Auditar el acceso a objetos** como se describe en el capítulo 3, el acceso a esos objetos de sistema se auditará.

Un objeto global del sistema (también conocido como "objeto base del sistema" u "objeto base con nombre") es un objeto de núcleo efímero al que la aplicación o el componente de sistema que lo ha creado asigna un nombre. Por lo general, estos objetos se emplean para sincronizar varias aplicaciones o diversas partes de una aplicación compleja. Como tienen un nombre, estos objetos tienen un alcance global que los hace visibles en todos los procesos del sistema. Al mismo tiempo, todos ellos cuentan con un descriptor de seguridad, si bien lo normal es que tengan una lista de control de acceso al sistema nula. Si habilita esta configuración de directiva al momento de iniciar, el núcleo asignará un SACL a estos objetos cuando ellos se creen.

Los valores posibles para la configuración **Auditoría: auditar el acceso de objetos globales del sistema** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Si no se protege un objeto con nombre visible globalmente del modo adecuado, podrá ser centro de un ataque por parte de un programa malintencionado que sepa su nombre. Por ejemplo, si un objeto de sincronización como una exclusión mutua tuviera una lista de control de acceso discrecional mal escogida, un programa malintencionado podría tener acceso a ella mediante el nombre y, de este modo, provocar que el programa creado no funcionara correctamente. No obstante, el riesgo de que esto ocurra es mínimo.

##### Contramedida

Habilite el valor **Auditoría: auditar el acceso de objetos globales del sistema**.

##### Impacto potencial

Si habilita el valor **Auditoría: auditar el acceso de objetos globales del sistema**, se podrían generar un gran número de eventos de seguridad, en particular en controladores de dominio y servidores de aplicaciones ocupados. Esto podría tener como consecuencia una respuesta del servidor lenta y obligaría al registro de eventos a registrar muchos eventos de escasa importancia. Esta configuración de directiva sólo puede habilitarse o deshabilitarse, y no hay forma de filtrar los eventos que se registran. Incluso en el caso de organizaciones con recursos suficientes para analizar eventos generados mediante esta configuración de directiva, es bastante improbable que posean el código fuente o una descripción sobre el uso de cada objeto con nombre. Por lo tanto, es improbable que muchas organizaciones se beneficien si el valor de esta configuración de directiva se establece en **Habilitado**.

#### Auditoría: auditar el uso del privilegio de copia de seguridad y restauración

Esta configuración de directiva determina si se auditará el uso de todos los privilegios de usuario, incluidos copia de seguridad y restauración, cuando la configuración **Auditar el uso de privilegios** está activada. Si habilita ambas configuraciones de directiva, se generará un evento de auditoría por cada uno de los archivos restaurados o de los que se haya hecho copia de seguridad.

Si habilita esta configuración de directiva en combinación con **Auditar el uso de privilegios**, se registrará cualquier uso de derechos de usuario en el registro de seguridad. Si, en cambio, deshabilita esta configuración de directiva las acciones de los usuarios con privilegios de copia de seguridad y restauración no se auditarán, incluso con el valor **Auditar el uso de privilegios** habilitado.

Los valores posibles para la configuración **Auditoría: auditar el uso del privilegio de copia de seguridad y restauración** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Si habilita este valor junto con **Auditar el uso de privilegios**, se generará un evento de auditoría por cada uno de los archivos restaurados o de los que se haya hecho copia de seguridad. Esta información podría ayudarle a identificar una cuenta que se utilizó, ya sea por error o malintencionadamente, para restaurar datos de forma no autorizada.

##### Contramedida

Active el parámetro **Auditar el uso del privilegio de copia de seguridad y restauración**. Alternativamente, implemente la copia de seguridad con registro automático configurando la clave de registro AutoBackupLogFiles, que se describe en el artículo de Microsoft Knowledge Base "[The event log stops logging events before reaching the maximum log size](http://support.microsoft.com/default.aspx?kbid=312571)" en http://support.microsoft.com/default.aspx?kbid=312571.

##### Impacto potencial

Si habilita esta directiva pueden generarse un gran número de eventos de seguridad, lo que causaría una respuesta lenta en los servidores y obligaría al registro de numerosos eventos de seguridad insignificantes. Si aumenta el tamaño del registro de seguridad para reducir las oportunidades de un cierre del sistema, un archivo de registro excesivamente grande puede afectar al rendimiento de sistema.

#### Auditoría: apagar el sistema de inmediato si no puede registrar auditorías de seguridad

Esta configuración de directiva determina si el equipo se cierra si no puede registrar eventos de seguridad. Las certificaciones Trusted Computer System Evaluation Criteria (TCSEC)-C2 y Common Criteria necesitan que el equipo pueda evitar la ocurrencia de eventos que pueden auditarse si el sistema de auditoría no puede registrarlos. Microsoft decidió cumplir este requisito deteniendo el equipo y mostrando un mensaje de parada en caso de que se produzca un error del sistema de auditoría. Si habilita esta configuración de directiva, el equipo se detiene si, por cualquier razón, no se puede registrar una auditoría de seguridad. Normalmente, no se puede registrar un evento cuando el registro de auditoría de seguridad está lleno y el método de retención especificado es **No sobrescribir eventos** o **Sobrescribir eventos por días**.

Cuando se habilita esta configuración de directiva, se muestra el mensaje siguiente de **parada** si el registro de seguridad está lleno y no puede sobrescribirse una entrada existente:

STOP: C0000244 {Error de auditoría}

Error al intentar generar una auditoría de seguridad.

Para recuperarse del error, un administrador debe iniciar sesión, archivar el registro (opcional), borrar el registro y desactivar esta opción para permitir que el equipo se reinicie. En ese punto, puede ser necesario borrar manualmente el registro de eventos de seguridad antes de que pueda establecer esta configuración de directivacomo **Habilitado**.

Los valores posibles para la configuración **Auditoría: apagar el sistema de inmediato si no puede registrar auditorías de seguridad** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

En caso de que el equipo no pueda registrar eventos en el registro de seguridad, no se podrá disponer de pruebas esenciales o información clave relativa a la solución de problemas para realizar una revisión tras haberse producido una incidencia de seguridad. Además, un atacante podría generar potencialmente un volumen grande de mensajes de registro de eventos de seguridad para forzar deliberadamente el cierre de un equipo.

##### Contramedida

Active la configuración **Apagar el sistema de inmediato si no puede registrar auditorías de seguridad**.

##### Impacto potencial

Si habilita esta configuración de directiva, la carga administrativa puede ser significativa, especialmente si configura también el método de **retención** del registro de seguridad en **No sobrescribir eventos** **(borrado manual del registro)**. Con esta configuración, una amenaza de rechazo (un operador de copia de seguridad puede negar que ha restaurado datos o ha hecho una copia de seguridad de ellos) se convierte en una vulnerabilidad de denegación de servicio (DoS), ya que puede hacer que un servidor se apague a la fuerza al saturarlo con eventos de inicio de sesión y otros eventos de seguridad que se escriben en el registro de seguridad. Asimismo, dado que el sistema se apaga de manera incorrecta, puede provocar daños irreparables en el sistema operativo, en las aplicaciones o en los datos. Aunque el sistema de archivos NTFS garantiza la integridad de los archivos en el caso de un apagado de sistema poco afortunado, no podrá garantizar que todos los archivos de datos de cada aplicación se puedan volver a usar una vez que el equipo se haya reiniciado.

#### DCOM: Restricciones de acceso al equipo en el lenguaje de definición de descriptores de seguridad (SDDL)

Esta configuración de directiva permite a los administradores definir controles de acceso adicionales en todo el equipo que controlan el acceso a todas las aplicaciones basadas en el modelo de objetos distribuido (DCOM) en un equipo. Estos controles restringen las peticiones de llamadas, activación o inicio en el equipo. La manera más sencilla de considerar estos controles de acceso es como una llamada adicional de comprobación de acceso que se hace contra una lista de control de acceso (ACL) de todo el equipo en cada llamada, activación o inicio de cualquier servidor COM en el equipo. Si se produce un error de comprobación de acceso, se denegará la llamada, la activación o la solicitud de inicio. (Esta comprobación es adicional a cualquier comprobación de acceso que se ejecuta contra las ACL específicas del servidor). De hecho, proporciona un estándar mínimo de autorización que se debe superar para tener acceso a cualquier servidor COM en el equipo. La configuración **DCOM: Restricciones de acceso al equipo en el lenguaje de definición de descriptores de seguridad (SDDL)** controla los permisos de acceso con la inclusión de derechos de llamada.

Estas ACL para todo el equipo constituyen un método para anular configuraciones de seguridad deficientes especificadas por una aplicación determinada por medio de la configuración de seguridad CoInitializeSecurity o específica de la aplicación. Proporcionan un estándar de seguridad mínimo que se debe superar, independientemente de la configuración del servidor específico.

Estas ACL proporcionan una ubicación centralizada para que el administrador establezca la directiva de autorización general aplicable a todos los servidores COM del equipo.

La configuración **DCOM: Restricciones de acceso al equipo en el lenguaje de definición de descriptores de seguridad (SDDL)** le permite especificar una lista ACL de dos formas diferentes. Puede escribir el descriptor de seguridad en SDDL, o bien puede elegir usuarios y grupos y concederles o denegarles permisos de acceso local y remoto. Microsoft recomienda que utilice la interfaz de usuario integrada para especificar el contenido de las ACL que desea aplicar con esta configuración.  

##### Vulnerabilidad

Muchas aplicaciones COM incluyen código específico de seguridad (por ejemplo, para llamar a CoInitializeSecurity), pero utilizan configuraciones deficientes que a menudo permiten el acceso sin autenticación al proceso. Los administradores no pueden anular estas configuraciones para aplicar una mayor seguridad en versiones anteriores de Windows sin modificar la aplicación. Un atacante podría intentar explotar una seguridad deficiente en una aplicación individual atacándola por medio de llamadas COM.

Asimismo, la infraestructura COM incluye RPCSS, un servicio del sistema que se ejecuta durante el inicio del equipo y que se ejecuta siempre después del mismo. Este servicio administra la activación de objetos COM y la tabla de objetos ejecutada, y proporciona servicios de ayudante a DCOM remoto. Expone interfaces de RPC que se pueden llamar de forma remota. Debido a que algunos servidores COM permiten acceso remoto no autenticado (como se explicó en la sección previa), estas interfaces puede invocarlas cualquiera, incluso usuarios no autenticados. Como resultado, el servicio RPCSS puede recibir el ataque de usuarios malintencionados que utilizan equipos remotos sin autenticación.

##### Contramedida

Para proteger las aplicaciones o los servicios individuales basados en COM, configure **DCOM: Restricciones de acceso al equipo en el lenguaje de definición de descriptores de seguridad (SDDL)** en una lista ACL apropiada de todo el equipo.

##### Impacto potencial

Windows XP con SP2 y Windows Server 2003 con SP1 implementan ACL COM predeterminadas tal como se especifica en sus respectivas documentaciones. Si implementa un servidor COM y anula la configuración de seguridad predeterminada, confirme que la lista ACL de permisos de llamada específicos de la aplicación asigne el permiso correcto a los usuarios apropiados. Si no lo hace, necesitará cambiar su lista ACL de permisos específicos de la aplicación de modo que proporcione a los usuarios apropiados los derechos de activación para que las aplicaciones y los componentes de Windows que utilizan DCOM no fallen.

**Nota**: para obtener más información acerca de las restricciones predeterminadas de acceso del equipo COM que se aplican en Windows XP con SP2, consulte la guía "[Managing Windows XP Service Pack 2 Features Using Group Policy](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/mangxpsp2/mngsecps.mspx)" en www.microsoft.com/technet/prodtechnol/winxppro/maintain/mangxpsp2/mngsecps.mspx. Para obtener información acerca de las restricciones que se aplican en Windows Server 2003 con SP1, consulte la sección "Mejoras de seguridad DCOM" de la guía "[Cambios de la funcionalidad de Microsoft Windows Server 2003 Service Pack 1](http://technet.microsoft.com/es-es/library/cc738214.aspx)" en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/
BookofSP1/ed9975ba-3933-4e28-bcb4-72b80d7865b7.mspx. Para obtener más información acerca de los permisos de inicio, consulte la página “[LaunchPermission](http://msdn.microsoft.com/es-es/library/ms687202(en-us,vs.85).aspx)” en Microsoft MSDN® en http://go.microsoft.com/fwlink/?LinkId=20924.

#### DCOM: Restricciones de inicio del equipo en el lenguaje de definición de descriptores de seguridad (SDDL)

Esta configuración de directiva es semejante a la configuración **DCOM: Restricciones de acceso al equipo en el lenguaje de definición de descriptores de seguridad (SDDL)** ya que permite a los administradores definir controles de acceso adicionales en todo el equipo que controlan el acceso a todas las aplicaciones basadas en DCOM en un equipo. Sin embargo, las listas ACL que se especifican en *esta* configuración de directiva *controlan las solicitudes* COM locales y remotas de inicio COM (no las solicitudes de acceso) en el equipo. La manera más sencilla de considerar este control de acceso es como una llamada adicional de comprobación de acceso que se hace contra una lista de control de acceso de todo el equipo en cada inicio de cualquier servidor COM en el equipo. Si se produce un error de comprobación de acceso, se denegará la llamada, la activación o la solicitud de inicio. (Esta comprobación es adicional a cualquier comprobación de acceso que se ejecuta contra las ACL específicas del servidor.) De hecho, proporciona un estándar mínimo de autorización que se debe superar para iniciar cualquier servidor COM en el equipo. La directiva anterior difiere en que proporciona una comprobación de acceso mínima que se aplica a intentos de tener acceso a un servidor COM ya iniciado.

Estas ACL para todo el equipo constituyen un método para anular configuraciones de seguridad deficientes especificadas por una aplicación determinada por medio de la configuración de seguridad CoInitializeSecurity o específica de la aplicación. Proporcionan un estándar de seguridad mínimo que se debe superar, independientemente de la configuración del servidor COM específico. Estas ACL proporcionan una ubicación centralizada para que el administrador establezca la directiva de autorización general aplicable a todos los servidores COM del equipo.

La configuración **DCOM: Restricciones de inicio del equipo en el lenguaje de definición de descriptores de seguridad (SDDL)** le permite especificar una lista ACL de dos formas diferentes. Puede escribir el descriptor de seguridad en SDDL, o bien puede elegir usuarios y grupos y concederles o denegarles permisos de acceso local y remoto. Microsoft recomienda que utilice la interfaz de usuario integrada para especificar el contenido de las ACL que desea aplicar con esta configuración.

##### Vulnerabilidad

Muchas aplicaciones COM incluyen código específico de seguridad (por ejemplo, para llamar a CoInitializeSecurity), pero utilizan configuraciones deficientes que a menudo permiten el acceso sin autenticación al proceso. Los administradores no pueden anular estas configuraciones para aplicar una mayor seguridad en versiones anteriores de Windows sin modificar la aplicación. Un atacante podría intentar explotar una seguridad deficiente en una aplicación individual atacándola por medio de llamadas COM.

Asimismo, la infraestructura COM incluye RPCSS, un servicio del sistema que se ejecuta durante el inicio del equipo y que se ejecuta siempre después del mismo. Este servicio administra la activación de objetos COM y la tabla de objetos ejecutada, y proporciona servicios de ayudante a DCOM remoto. Expone interfaces de RPC que se pueden llamar de forma remota. Debido a que algunos servidores COM permiten la activación de componentes remota no autenticada (como se explicó en la sección previa), estas interfaces puede invocarlas cualquiera, incluso usuarios no autenticados. Como resultado, el servicio RPCSS puede recibir el ataque de usuarios malintencionados que utilizan equipos remotos sin autenticación.

##### Contramedida

Para proteger las aplicaciones o los servicios individuales basados en COM, configure **DCOM: Restricciones de acceso al equipo en el lenguaje de definición de descriptores de seguridad (SDDL)** en una lista ACL apropiada de todo el equipo.

##### Impacto potencial

Windows XP con SP2 y Windows Server 2003 con SP1 implementan ACL COM predeterminadas tal como se especifica en sus respectivas documentaciones. Si implementa un servidor COM y anula la configuración de seguridad predeterminada, confirme que la lista ACL de permisos de inicio específicos de la aplicación asigne el permiso de activación a los usuarios apropiados. Si no lo hace, necesitará cambiar su lista ACL de permisos de inicio específicos de la aplicación de modo que proporcione a los usuarios apropiados los derechos de activación para que las aplicaciones y los componentes de Windows que utilizan DCOM no fallen.

**Nota**: para obtener más información acerca de las restricciones predeterminadas de inicio del equipo COM que se aplican en Windows XP con SP2, consulte la guía "[Managing Windows XP Service Pack 2 Features Using Group Policy](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/mangxpsp2/mngsecps.mspx)" en www.microsoft.com/technet/prodtechnol/winxppro/maintain/mangxpsp2/mngsecps.mspx. Para obtener información acerca de las restricciones que se aplican en Windows Server 2003 con SP1, consulte la sección "Mejoras de seguridad DCOM" de la guía "[Cambios de la funcionalidad de Microsoft Windows Server 2003 Service Pack 1](http://technet.microsoft.com/es-es/library/cc738214.aspx)" en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/
BookofSP1/ed9975ba-3933-4e28-bcb4-72b80d7865b7.mspx. Para obtener más información acerca de los permisos de inicio, consulte la página “[LaunchPermission](http://msdn.microsoft.com/es-es/library/ms687202(en-us,vs.85).aspx)” en MSDN en http://go.microsoft.com/fwlink/?LinkId=20924.

#### Dispositivos: permitir el desbloqueo sin tener que iniciar sesión

Esta configuración de directiva determina si un usuario debe iniciar sesión para solicitar permiso para quitar un equipo portátil de una estación de acoplamiento. Si habilita esta configuración de directiva, los usuarios podrán presionar el botón físico de expulsión de un equipo portátil acoplado para desbloquearlo de forma segura. Si deshabilita esta configuración de directiva, el usuario debe iniciar sesión para recibir el permiso de desbloquear el equipo. Sólo los usuarios que disfrutan del privilegio **Quitar el equipo de la estación de acoplamiento** pueden obtener este permiso.

**Nota**: esta configuración de directiva se debe deshabilitar sólo para aquellos equipos que no pueden desbloquearse de forma mecánica. Los equipos que pueden desbloquearse de forma mecánica pueden retirarse físicamente por parte del usuario, sin importar si utiliza o no la funcionalidad de desbloqueo de Windows.

Los valores posibles para la configuración **Dispositivos: permitir el desbloqueo sin tener que iniciar sesión** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Si esta configuración de directiva se habilita, cualquier usuario que tenga acceso físico a los equipos portátiles en la estación de acoplamiento podría quitarlos y, posiblemente, realizar alteraciones en ellos. Esta configuración de directiva no tiene impacto alguno en aquellos equipos que no tienen estaciones de acoplamiento.

##### Contramedida

Deshabilite el valor **Dispositivos: permitir el desbloqueo sin tener que iniciar sesión**.

##### Impacto potencial

Aquellos usuarios que hayan bloqueado sus equipos deberán iniciar sesión en la consola central para poder desbloquearlos.

#### Dispositivos: permitir formatear y expulsar medios extraíbles

Esta configuración de directiva determina quién puede formatear y expulsar medios extraíbles.

Los valores posibles para la configuración **Dispositivos: permitir formatear y expulsar medios extraíbles** son:

-   Administradores

-   Administradores y usuarios avanzados

-   Administradores y usuarios interactivos

-   No está definido

##### Vulnerabilidad

Los usuarios podrán mover información en discos extraíbles a otro equipo donde disfruten de privilegios administrativos para, de este modo, poder tomar posesión de cualquier archivo, otorgarse control total sobre él y verlo o cambiarlo. El hecho de que la mayoría de los dispositivos de almacenamiento extraíbles expulsen los soportes presionando un botón mecánico disminuye las ventajas de esta configuración de directiva.

##### Contramedida

Configure el parámetro **permitir formatear y expulsar medios extraíbles** como **Administradores.**

##### Impacto potencial

Los administradores serán los únicos habilitados para expulsar medios extraíbles formateados con NTFS.

#### Dispositivos: impedir que los usuarios instalen controladores de impresora

Para que un equipo pueda imprimir en una impresora de red, se debe instalar el controlador para esa impresora en el equipo local. La configuración **Dispositivos: impedir que los usuarios instalen controladores de impresora** determina quién puede instalar un controlador de impresora como parte del proceso de agregado de una impresora de red. Si habilita esta configuración de directiva, sólo los miembros de los grupos **Administradores** y **Usuarios avanzados** podrán instalar un controlador de impresora al agregar una impresora de red. Si deshabilita esta configuración de directiva, cualquier usuario puede instalar controladores de impresora al agregar una impresora de red. Esta configuración de directiva evita que los usuarios normales descarguen e instalen controladores de impresora no confiables.

**Nota**: esta configuración de directiva no tiene repercusión alguna si un administrador ha configurado una ruta confiable destinada a la descarga de controladores. Si usa rutas confiables, el subsistema de impresión intenta usarlas para descargar el controlador. Si la descarga con la ruta confiable es correcta, el controlador se instalará en nombre de cualquier usuario, pero si no, no se instalará y no se agregará la impresora de red.

Los valores posibles para la configuración **Dispositivos: impedir que los usuarios instalen controladores de impresora** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

En algunas organizaciones puede resultar apropiado permitir a los usuarios que instalen controladores de impresora en sus propias estaciones de trabajo. Sin embargo, no debe permitir que lo hagan en servidores. La instalación de un controlador de impresora en un servidor puede provocar, sin querer, que el equipo se vuelva menos estable. Por lo tanto, lo ideal sería que sólo los administradores tuvieran privilegios sobre los servidores. Un usuario malintencionado podría instalar controladores de impresora inadecuados en un intento deliberado de dañar el equipo, o un usuario quizás instale accidentalmente código malintencionado que se disfraza como un controlador de impresora.

##### Contramedida

Configure **Dispositivos: impedir que los usuarios instalen controladores de impresora** como **Habilitado**.

##### Impacto potencial

Sólo los usuarios con privilegios administrativos, de usuario avanzado o de operador de servidor pueden instalar impresoras en el servidor. Si esta configuración de directiva se encuentra habilitada, pero el controlador para la impresora de red ya existe en el equipo local, los usuarios aún podrán agregar la impresora de red.

#### Dispositivos: restringir el acceso al CD-ROM sólo al usuario con sesión iniciada localmente

Esta configuración de directiva determina si los usuarios locales y remotos pueden obtener acceso a un CD-ROM simultáneamente. Si se habilita, esta configuración de directiva permite solamente a los usuarios que han iniciado sesión de forma interactiva tener acceso a los soportes de CD-ROM extraíbles. Si se habilita y nadie ha iniciado sesión, el contenido del CD-ROM estará disponible a través de la red.

Los valores posibles para la configuración **Dispositivos: restringir el acceso al CD-ROM sólo al usuario con sesión iniciada localmente** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Un usuario remoto podría tener acceso a un CD-ROM montado que contiene información confidencial. El riesgo es pequeño porque las unidades de CD-ROM no están disponibles de manera automática como recursos compartidos de red, sino que han de ser los administradores los que decidan conscientemente si se comparte la unidad. Sin embargo, es posible que los administradores deseen denegar a los usuarios de red la opción de ver datos o ejecutar aplicaciones desde medios extraíbles en el servidor.

##### Contramedida

Habilite el valor **Dispositivos: restringir el acceso al CD-ROM sólo al usuario con sesión iniciada localmente**.

##### Impacto potencial

Los usuarios que se conectan a un servidor a través de la red no podrán utilizar las unidades de CD-ROM instaladas en el servidor cuando otro usuario haya iniciado sesión en la consola local del servidor. Las herramientas del sistema que requieren acceso a la unidad de CD-ROM fallarán. Por ejemplo, el servicio Instantáneas de volumen intenta tener acceso a todas las unidades de CD-ROM y de disquete que están presentes en el equipo cuando se inicializa, y si el servicio no puede tener acceso a una de estas unidades fallará. Esta condición impedirá la ejecución de la utilidad Copia de seguridad de Windows si se especificaron instantáneas de volumen para el trabajo de copia de seguridad. También se generará un error con cualquier producto de terceros cuando se deseen realizar copias de seguridad en las que se utilicen instantáneas de volumen. Esta configuración de directiva no procede en el caso de un equipo que funcione como reproductor de CD para los usuarios de la red.

#### Dispositivos: restringir el acceso a la unidad de disquete sólo al usuario con sesión iniciada localmente

Esta configuración de directiva determina si los usuarios locales y remotos pueden obtener acceso a soportes de disquete simultáneamente. Si se habilita, esta configuración de directiva permite solamente a los usuarios que han iniciado sesión de forma interactiva tener acceso a los soportes de disquete extraíbles. Si se habilita y nadie ha iniciado sesión, el contenido de la unidad de disquete estará disponible a través de la red.

Los valores posibles para la configuración **Dispositivos: restringir el acceso a la unidad de disquete sólo al usuario con sesión iniciada localmente** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Un usuario remoto podría tener acceso a un disquete montado que contiene información confidencial. El riesgo es pequeño porque las unidades de disquete no están disponibles de manera automática como recursos compartidos de red, sino que han de ser los administradores los que decidan conscientemente si se comparte la unidad. Sin embargo, es posible que los administradores deseen denegar a los usuarios de red la opción de ver datos o ejecutar aplicaciones desde medios extraíbles en el servidor.

##### Contramedida

Habilite el valor **Dispositivos: restringir el acceso a la unidad de disquete**.

##### Impacto potencial

Los usuarios que se conectan a un servidor a través de la red no podrán utilizar las unidades de disquete instaladas en el servidor cuando otro usuario haya iniciado sesión en la consola local del servidor. Las herramientas del sistema que requieren acceso a la unidad de disquete fallarán. Por ejemplo, el servicio Instantáneas de volumen intenta tener acceso a todas las unidades de CD-ROM y de disquete que están presentes en el equipo cuando se inicializa, y si el servicio no puede tener acceso a una de estas unidades fallará. Esta condición impedirá la ejecución de la utilidad Copia de seguridad de Windows si se especificaron instantáneas de volumen para el trabajo de copia de seguridad. También se generará un error con cualquier producto de terceros cuando se deseen realizar copias de seguridad en las que se utilicen instantáneas de volumen.

#### Dispositivos: comportamiento de instalación de controlador no firmado

Esta configuración de directiva determina lo que sucede cuando se intenta instalar un controlador de dispositivo no certificado o firmado por el laboratorio de calidad de hardware de Windows (WHQL) mediante la interfaz de programación de aplicaciones (API) del programa de instalación.

Los valores posibles para la configuración **Dispositivos: comportamiento de instalación de controlador no firmado** son:

-   Realizar en silencio

-   Avisar pero permitir la instalación

-   No permitir la instalación

-   No está definido

##### Vulnerabilidad

Esta configuración de directiva evita la instalación de controladores no firmados o advierte al administrador de que está a punto de instalar un software de controlador no firmado. Esta capacidad puede evitar el uso de la API del programa de instalación para instalar controladores que no se han certificado para ejecutarse en Windows XP ni Windows Server 2003. Esta configuración de directiva no impide que ciertas herramientas de ataque usen un método por el que los archivos .sys dañinos se copian y registran para iniciarse como servicios de sistema.

##### Contramedida

Configure **Dispositivos: comportamiento de instalación de controlador no firmado** en **Avisar pero permitir la instalación**, que es la opción predeterminada para Windows XP con SP2. La configuración predeterminada para Windows Server 2003 es **No está definido**.

##### Impacto potencial

Los usuarios con privilegios suficientes para instalar controladores de dispositivo podrán instalar igualmente controladores de dispositivo sin firmar, Sin embargo, esto puede traer problemas de estabilidad para los servidores. Otro problema que puede surgir con la configuración **Avisar pero permitir la instalación** es que se producirán errores en las secuencias de comandos de instalaciones desatendidas cuando intenten instalar controladores sin firmar.

#### Controlador de dominio: permitir a los operadores de servidor programar tareas

Esta configuración de directiva determina si los operadores de servidores tienen permiso para enviar trabajos mediante la herramienta de programación AT.

**Nota**: esta opción de seguridad sólo afecta a la herramienta de programación AT. No afecta a la herramienta Programador de tareas.

Los valores posibles para la configuración **Controlador de dominio: permitir a los operadores de servidor programar tareas** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Si habilita esta configuración de directiva, los trabajos que los operadores de servidor creen por medio del servicio AT se ejecutarán en el contexto de la cuenta que a su vez ejecuta este servicio. De forma predeterminada, dicha cuenta es la cuenta SYSTEM. Si habilita esta configuración de directiva, los operadores de servidor podrían realizar tareas que SYSTEM puede hacer, pero que por lo general no podrían, como agregar la cuenta al grupo **Administradores** local.

##### Contramedida

Deshabilite el valor **Controlador de dominio: permitir a los operadores de servidor programar tareas**.

##### Impacto potencial

El impacto es mínimo para la mayoría de las organizaciones. Los usuarios, incluidos los del grupo **Operadores de servidor**, podrán seguir creando trabajos utilizando el asistente del programador de tareas. Sin embargo, esos trabajos se ejecutarán en el contexto de la cuenta con la que se autentica el usuario al establecer el trabajo.

#### Controlador de dominio: requisitos de firma de servidor LDAP

Esta configuración de directiva determina si el servidor de Protocolo ligero de acceso a directorios (LDAP) requiere que los clientes LDAP negocien la firma de datos.

Los valores posibles para la configuración **Controlador de dominio: requisitos de firma de servidor LDAP** son:

-   **Ninguno**. Las firmas de datos no son necesarias para enlazar con el servidor. En caso de que el cliente solicite la firma de datos, el servidor la admitirá.

-   **Requerir firma**. La opción de firmar los datos LDAP ha de negociarse a menos que se use Seguridad de la capa de transporte/Nivel de sockets seguros (TLS/SSL).

-   **No está definido**.

##### Vulnerabilidad

El tráfico de red sin firmar es susceptible de sufrir ataques de "hombre en el medio". En dichos ataques, el intruso captura paquetes entre el servidor y el cliente y los modifica antes de reenviarlos al cliente. En el caso de los servidores LDAP, un atacante podría hacer que un cliente tomara decisiones en función de registros falsos del directorio LDAP. Para reducir el riesgo de un ataque en una red corporativa, puede poner en práctica medidas eficaces de seguridad física para proteger la infraestructura de la red. Además, puede conseguir que no sea nada fácil efectuar ataques de intermediario si implementa el modo de encabezado de autenticación (AH) de IPsec, que realiza funciones de autenticación mutua e integridad de paquete para el tráfico IP.

##### Contramedida

Configure **Controlador de dominio: requisitos de firma de servidor LDAP** en **Requerir firma**.

##### Impacto potencial

Los clientes no compatibles con la firma LDAP no podrán plantear consultas LDAP a los controladores de dominio; Todos los equipos con Windows 2000 en su organización que se administran desde equipos con Windows Server 2003 o Windows XP y que utilizan la autenticación desafío/respuesta de Windows NT® deberán tener instalado Windows 2000 Service Pack 3 (SP3). Alternativamente, estos clientes deben tener el cambio de registro que se describe en el artículo Q325465 de Microsoft Knowledge Base “[Windows 2000 domain controllers require SP3 or later when using Windows Server 2003 administration tools](http://support.microsoft.com/default.aspx?scid=325465)”, disponible en http://support.microsoft.com/default.aspx?scid=325465. Además, algunos sistemas operativos de terceros no admiten las firmas LDAP. Si habilita esta configuración de directiva, los equipos cliente que utilizan esos sistemas operativos pueden ser incapaces de tener acceso a los recursos del dominio.

#### Controlador de dominio: no permitir los cambios de contraseña de cuenta de equipo

Esta configuración de directiva determina si un controlador de dominio aceptará solicitudes de cambio de contraseña para cuentas de equipo.

Los valores posibles para la configuración **Controlador de dominio: no permitir los cambios de contraseña de cuenta de equipo** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Si habilita esta configuración de directiva en todos los controladores de dominio en un dominio, los miembros del dominio no serán capaces de cambiar sus contraseñas de cuenta de equipo, y esas contraseñas serán más vulnerables.

##### Contramedida

Deshabilite el valor **Controlador de dominio: no permitir los cambios de contraseña de cuenta de equipo**.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Miembro de dominio: descifrar o firmar digitalmente datos de un canal seguro (varias opciones relacionadas)

La configuración de directiva siguiente determina si se puede establecer un canal seguro con un controlador de dominio que no puede firmar o cifrar el tráfico de canal seguro:

-   **Miembro de dominio: descifrar o firmar digitalmente datos de un canal seguro (siempre)**

-   **Miembro de dominio: descifrar digitalmente datos de un canal seguro (cuando sea posible)**

-   **Miembro de dominio: firmar digitalmente datos de un canal seguro (cuando sea posible)**

Si habilita la configuración **Miembro de dominio: descifrar o firmar digitalmente datos de un canal seguro (siempre)**, impedirá que se establezca un canal seguro con un controlador de dominio que no puede firmar o cifrar todos los datos del canal.

Para proteger el tráfico de autenticación de ataques de intermediario, de reproducción y otros ataques similares de red, los equipos con Windows crean un canal de comunicación a través de NetLogon denominado Canal seguro. Estos canales autentican las cuentas de equipo y también las cuentas de usuario cuando un usuario remoto se conecta a un recurso de la red y la cuenta del usuario se halla en un dominio confiable. Esta autenticación se conoce como autenticación de paso de eventos y permite que un equipo que ejecuta Windows y que se ha unido a un dominio tenga acceso a la base de datos de cuentas de usuario de tal dominio en cualquier dominio confiable.

**Nota**: para habilitar el valor **Miembro de dominio: descifrar o firmar digitalmente datos de un canal seguro (siempre)** en una estación de trabajo o un servidor de un miembro, todos los controladores de dominio en el dominio al que este miembro pertenece deben poder firmar y cifrar todos los datos de canal seguro. Este requisito significa que los controladores de dominio en cuestión deberán ejecutar Windows NT 4.0 con Service Pack 6a o una versión posterior del sistema operativo Windows.

Si habilita el valor **Miembro de dominio: descifrar o firmar digitalmente datos de un canal seguro (siempre)**, el valor **Miembro de dominio: firmar digitalmente datos de canal seguro (cuando sea posible)** se habilitará igualmente de forma automática.

Los valores que se pueden seleccionar para esta configuración de directiva son los siguientes:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Cuando un equipo con Windows Server 2003, Windows XP, Windows 2000 o Windows NT se une a un dominio, se crea una cuenta de equipo. Una vez que se ha unido, el equipo utiliza la contraseña para esa cuenta con el fin de crear un canal seguro con el controlador de dominio para su dominio cada vez que se reinicie. Las solicitudes enviadas en el canal seguro se autentican y la información confidencial (como contraseñas) se cifra, pero no se comprueba la integridad del canal y no toda la información se cifra. Si un equipo se configura para cifrar o firmar *siempre* datos de canal seguro, pero el controlador de dominio no puede firmar o cifrar ninguna parte de los datos de canal seguro, el equipo y el controlador de dominio no pueden establecer un canal seguro. Si el equipo se configura para cifrar y firmar datos de canal seguro *cuando sea posible*, podrá establecer un canal seguro, si bien se deberá negociar el nivel de cifrado y firma.

##### Contramedida

-   Configure **Miembro de dominio: descifrar o firmar digitalmente datos de un canal seguro (siempre)** como **Habilitado**.

-   Configure **Miembro de dominio: descifrar digitalmente datos de un canal seguro (cuando sea posible)** como **Habilitado**.

-   Configure **Miembro de dominio: firmar digitalmente datos de un canal seguro (cuando sea posible)** como **Habilitado**.

##### Impacto potencial

El cifrado y la firma digitales del "canal seguro" son recomendables cuando se pueden aplicar. ya que el canal seguro protege las credenciales de dominio a medida que se envían al controlador del dominio. No obstante, sólo Windows NT 4.0 Service Pack 6a (SP6a) y las versiones posteriores del sistema operativo Windows son compatibles con el cifrado y la firma digitales del canal seguro. Por lo tanto, los clientes Windows 98 Second Edition no son compatibles, a menos que tengan dsclient instalado. En consecuencia, no puede habilitar el valor **Miembro de dominio: descifrar o firmar digitalmente datos de un canal seguro (siempre)** en controladores de dominio compatibles con clientes Windows 98 como miembros del dominio. Entre las repercusiones potenciales se pueden mencionar las siguientes:

-   La capacidad de crear o borrar relaciones de confianza de nivel inferior se deshabilitará.

-   Los inicios de sesión de clientes de nivel inferior se deshabilitarán.

-   La capacidad de autenticar a usuarios de otros dominios de un nivel inferior de confianza se deshabilitará.

Esta configuración de directiva podrá habilitarse una vez haya quitado todos los clientes Windows 9x del dominio y haya actualizado todos los servidores y controladores de dominio de Windows NT 4.0 de dominios de confianza o confiables a Windows NT 4.0 con SP6a. Puede habilitar las otras dos configuraciones de directiva, **Miembro de dominio: descifrar digitalmente datos de un canal seguro (cuando sea posible)** y **Miembro de dominio: firmar digitalmente datos de canal seguro (cuando sea posible)**, en todos los equipos del dominio que sean compatibles con estos valores sin que se vean afectados los clientes y aplicaciones de nivel inferior.

#### Miembro de dominio: deshabilitar los cambios de contraseña de cuentas de equipo

Esta configuración de directiva determina si un miembro de dominio cambia periódicamente la contraseña de la cuenta de su equipo. Si habilita esta configuración de directiva, el miembro de dominio no puede cambiar su contraseña de cuenta de equipo. Si deshabilita esta configuración de directiva, se permite al miembro del dominio cambiar su contraseña de cuenta en el equipo según se especifica en el valor **Miembro de dominio: duración máxima de contraseña de cuenta de equipo**, que de forma predeterminada es de 30 días.

**Precaución**: no habilite esta configuración de directiva. Las contraseñas de cuenta de equipo se utilizan para establecer comunicaciones de canal seguro entre miembros y controladores de dominio y, dentro del dominio, entre los propios controladores de dominio. Después de que se establecen dichas comunicaciones, el canal seguro transmite información confidencial necesaria a la hora de tomar decisiones de autorización y autenticación.

No emplee esta configuración de directiva con la intención de admitir escenarios de inicio múltiple que usan la misma cuenta de equipo. Si quiere admitir este caso para dos instalaciones unidas al mismo dominio, use nombres diferentes de equipo para las dos instalaciones. Esta configuración de directiva se agregó a Windows para facilitar el proceso a organizaciones con reservas de equipos ya creados que se ponen en funcionamiento meses después. Elimina la necesidad de que esos equipos vuelvan a unirse al dominio. Esta configuración de directiva también se utiliza a veces en equipos de imágenes o con prevención de cambios de nivel de hardware y software. Los procedimientos correctos de creación de imágenes hacen que la utilización de esta directiva sea innecesaria para equipos de imágenes.

Los valores posibles para la configuración **Miembro de dominio: deshabilitar los cambios de contraseña de cuentas de equipo** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

La configuración predeterminada en equipos con Windows Server 2003 pertenecientes a un dominio establece que automáticamente cada 30 días se deben cambiar las contraseñas de sus cuentas. Si deshabilita esta característica, los equipos que ejecutan Windows Server 2003 conservan las mismas contraseñas que sus cuentas de equipo. Los equipos que ya no pueden cambiar automáticamente sus contraseñas de cuenta están expuestos a un atacante que pueda determinar la contraseña para la cuenta de dominio del equipo.

##### Contramedida

Compruebe que el valor de la configuración **Miembro de dominio**: **deshabilitar los cambios de contraseña de cuentas de equipo** sea **Deshabilitado**.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Miembro de dominio: duración máxima de contraseña de cuenta de equipo

Esta configuración de directiva determina la duración máxima admisible de una contraseña de cuenta de equipo. Este valor es válido también para los equipos de Windows 2000, pero no está disponible a través de las herramientas del administrador de configuración de seguridad de los mismos.

Los valores posibles para la configuración **Miembro de dominio: duración máxima de contraseña de cuenta de equipo** son:

-   Un número de días especificado por el usuario entre 0 y 999

-   No está definido

##### Vulnerabilidad

En dominios basados en Active Directory, cada equipo posee una cuenta y una contraseña como todos los usuarios. De forma predeterminada, los miembros de dominio cambian automáticamente sus contraseñas cada 30 días. Si aumenta este intervalo de forma significativa o se fija en 0 para que los equipos no cambien las contraseñas, se da más tiempo al atacante para emprender un ataque de fuerza bruta para averiguar la contraseña de una o más cuentas de equipo.

##### Contramedida

Configure el valor **Miembro de dominio: duración máxima de contraseña de cuenta de equipo** en 30 días.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Miembro de dominio: requerir clave de sesión protegida (Windows 2000 o más reciente)

Esta configuración de directiva determina si se puede establecer un canal seguro con un controlador de dominio que no puede firmar o cifrar el tráfico de canal seguro con una clave de sesión segura de 128 bits. Si habilita esta configuración de directiva, no se podrá establecer un canal seguro con un controlador de dominio que no pueda cifrar datos de canal seguro con una clave protegida. Si deshabilita esta configuración de directiva, se permiten las claves de sesión de 64 bits.

**Nota**: para habilitar esta configuración de directiva en una estación de trabajo o servidor miembro, todos los controladores de dominio a los que este miembro pertenezca deberán ser capaces de cifrar datos de canal seguro utilizando una clave segura de 128 bits. Es decir, todos los controladores de dominio en cuestión deberán ejecutar Windows 2000 con Service Pack 6a o una versión posterior del sistema operativo Windows.

Los valores posibles para la configuración **Miembro de dominio: requerir clave de sesión protegida (Windows 2000 o más reciente)** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Las claves de sesión que se utilizan para establecer comunicaciones de canal seguro entre controladores de dominio y equipos miembro son mucho más seguras en Windows 2000 que en anteriores sistemas operativos de Microsoft.

Siempre que sea posible, se recomienda sacar partido de estas claves de sesión más seguras con el fin de proteger las comunicaciones del canal seguro frente a ataques que intentan secuestrar o interceptar sesiones de red. (La interceptación es una modalidad de secuestro que consiste en que los datos de la red se leen o se alteran en tránsito. Estos datos se pueden cambiar para ocultar o cambiar el destinatario, o bien para redireccionarlo).

##### Contramedida

Configure **Miembro de dominio: requerir clave de sesión protegida (Windows 2000 o más reciente)** como **Habilitado**.

Si se habilita esta configuración de directiva, todo el tráfico saliente de canales seguros requerirá una clave de cifrado segura (Windows 2000 o posterior). Si deshabilita esta configuración de directiva, se negocia la seguridad de la clave. Sólo debe habilitar esta configuración de directiva si los controladores de dominio de todos los dominios confiables son compatibles con claves seguras. Esta directiva está deshabilitada de forma predeterminada.

##### Impacto potencial

Los equipos que tienen habilitada esta configuración de directiva no serán capaces de unir dominios de Windows NT 4.0, y puede que las relaciones de confianza entre dominios de Active Directory y dominios de estilo Windows NT no funcionen apropiadamente. Además, los equipos que no admiten esta configuración de directiva no serán capaces de unir los dominios en los que los controladores de dominio tienen esta configuración de directiva habilitada.

#### Inicio de sesión interactivo: no mostrar el último nombre de usuario

Esta configuración de directiva determina si el cuadro de diálogo **Iniciar sesión en Windows** muestra el nombre del último usuario que ha iniciado una sesión en el equipo. Si habilita esta configuración de directiva, no se mostrará el nombre del último usuario que inició sesión correctamente. Si deshabilita esta configuración de directiva, se mostrará el nombre del último usuario que inició sesión correctamente.

Los valores posibles para la configuración **Inicio de sesión interactivo: no mostrar el último nombre de usuario** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Un atacante con acceso a la consola (p. ej., alguien con acceso físico o que puede conectarse al servidor por medio de los Servicios de Terminal Server) podría ver el nombre del último usuario que inició sesión en el servidor. El atacante podría entonces intentar adivinar la contraseña, utilizar un diccionario, o lanzar un ataque de fuerza bruta para tratar de iniciar sesión.

##### Contramedida

Configure **No mostrar el último nombre de usuario en la pantalla de inicio de sesión** como **Habilitado**.

##### Impacto potencial

El usuario tendrá siempre que escribir su nombre de usuario cuando desee iniciar sesión en los servidores.

#### Inicio de sesión interactivo: no requerir Ctrl+Alt+Supr

Esta configuración de directiva determina si los usuarios deben presionar Ctrl+Alt+Supr antes de iniciar sesión. Si habilita esta configuración de directiva, los usuarios pueden iniciar sesión sin esta combinación de teclas. Si deshabilita esta opción, los usuarios deben presionar Ctrl+Alt+Supr antes de iniciar la sesión en Windows, salvo que utilicen una tarjeta inteligente para el inicio de sesión en Windows. Una tarjeta inteligente es un dispositivo inalterable donde se almacena información de seguridad.

Los valores posibles para la configuración **Inicio de sesión interactivo: no requerir Ctrl+Alt+Supr** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Microsoft ha desarrollado esta característica con el objetivo de facilitar a aquellos usuarios con algún tipo de impedimento físico el inicio de sesión en equipos donde se ejecuta Windows. Si los usuarios no tienen que presionar la combinación de teclas Ctrl+Alt+Supr, se exponen a ataques de interceptación de contraseña. Si se requiere Ctrl+Alt+Supr antes del inicio de sesión, las contraseñas de usuario se comunican a través de una ruta de acceso de confianza.

Un atacante podría instalar un programa troyano que tuviera el aspecto del cuadro de diálogo de inicio de sesión de Windows estándar y, así, conseguir la contraseña del usuario. De este modo, podrá iniciar sesión en la cuenta en peligro con el nivel de privilegio que el usuario posea.

##### Contramedida

Configure **Deshabilitar el requisito de presionar Ctrl+Alt+Supr para iniciar sesión** como **Deshabilitado**.

##### Impacto potencial

Los usuarios deberán presionar tres teclas antes de que se muestre el cuadro de diálogo de inicio de sesión, a menos que tengan una tarjeta inteligente para iniciar sesión.

#### Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar una sesión

Los valores **Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar una sesión** e **Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión** están estrechamente relacionados. La primera configuración de directiva especifica un mensaje de texto que se muestra a los usuarios cuando inician sesión y la segunda configuración de directiva especifica un título que se muestra en la barra del título de la ventana que contiene el mensaje de texto. Muchas organizaciones utilizan este texto con fines legales; por ejemplo, para advertir a los usuarios acerca de las consecuencias del abuso de información de la empresa o que sus acciones se pueden auditar.

**Precaución**: Windows XP Professional agrega la compatibilidad para avisos de inicio de sesión que pueden sobrepasar los 512 caracteres de longitud y que, asimismo, pueden contener secuencias con retornos de carro y saltos de línea. Sin embargo, los clientes con Windows 2000 no pueden interpretar ni mostrar estos mensajes de texto. Se tendrá que usar un equipo de Windows 2000 para crear una directiva de mensaje de inicio de sesión que se aplique a equipos de Windows 2000. Proceda como se indica a continuación si crea una directiva de mensaje de inicio de sesión en un equipo de Windows XP Professional por error y descubre que no se muestra correctamente en equipos de Windows 2000:

-   Cambie la configuración a **No está definido**.

-   Vuelva a definirla usando un equipo de Windows 2000.

No se puede cambiar directamente un valor de mensaje de inicio de sesión definido con Windows XP Professional en un equipo de Windows 2000. Primero debe cambiar la configuración a **No está definido**.

Los valores que se pueden seleccionar para esta configuración de directiva son los siguientes:

-   Texto definido por el usuario

-   No está definido

##### Vulnerabilidad

Mostrar un mensaje de advertencia antes del inicio de sesión puede ayudar a evitar un ataque al advertir al atacante de sus malas intenciones. Puede ayudar también a reforzar las directivas corporativas al notificar a los empleados de la directiva apropiada durante el proceso de inicio de sesión.

##### Contramedida

Configure el **texto del mensaje para los usuarios que intentan iniciar una sesión** y el **título del mensaje para los usuarios que intentan iniciar una sesión** en un valor apropiado para su organización.

**Nota**: las advertencias que decida mostrar deben recibir la aprobación de los representantes de asuntos jurídicos y recursos humanos de su organización.

##### Impacto potencial

Los usuarios verán un mensaje en un cuadro de diálogo antes de que puedan iniciar sesión en la consola del servidor.

#### Inicio de sesión interactivo: núm. de inicios de sesión previos en la caché (en caso que el controlador de dominio no esté disponible)

Esta configuración de directiva determina el número de usuarios únicos diferentes que pueden iniciar sesión en un dominio de Windows utilizando información de cuenta en caché. La información de cuenta para cuentas de dominio se puede almacenar localmente en caché para que un usuario pueda iniciar una sesión aunque no sea posible contactar con un controlador de dominio en los posteriores inicios de sesión. Esta configuración de directiva determina el número de usuarios únicos cuya información de inicio de sesión se almacenará localmente en caché.

Si un controlador de dominio no se encuentra disponible y la información de inicio de sesión de un usuario se almacena en caché, se mostrará el siguiente mensaje:

Imposible conectar con ningún controlador de dominio para su dominio. Se ha iniciado su sesión utilizando información de cuentas en tabla caché. Los cambios hechos en su perfil desde la última vez que inició la sesión no estarán disponibles.

Si un controlador de dominio no se encuentra disponible y la información de inicio de sesión de un usuario se almacena en caché, se mostrará este mensaje:

El sistema no puede iniciar su sesión en este momento porque el dominio *&lt;NOMBRE\_DOMINIO&gt;* no está disponible.

Los valores posibles para la configuración **Inicio de sesión interactivo: núm. de inicios de sesión previos en la caché (en caso que el controlador de dominio no esté disponible)** son:

-   Número definido por el usuario (entre 0 y 50)

-   No está definido

##### Vulnerabilidad

El número asignado a esta configuración de directiva señala el número de usuarios cuya información de inicio de sesión almacenan en caché los servidores de forma local. Si el número fijado es 10, el servidor almacenará en caché la información de inicio de sesión de 10 usuarios. En el caso de que un undécimo usuario inicie sesión en el equipo, el servidor sobrescribirá la sesión de inicio de sesión almacenada en caché más antigua.

Las credenciales de inicio de sesión de los usuarios que tienen acceso a la consola del servidor se almacenan en caché en ese servidor, de forma que un atacante que tiene acceso al sistema de archivos del servidor podría localizar esta información almacenada en caché y realizar un ataque de fuerza bruta para intentar determinar las contraseñas de usuario.

Para mitigar este tipo del ataque, Windows cifra la información y oculta su ubicación física.

##### Contramedida

Configure **Inicio de sesión interactivo:núm. de inicios de sesión previos en la caché (en caso que el controlador de dominio no esté disponible)** en **0**, lo que deshabilita el almacenamiento de la información de inicio de sesión en caché local. Entre otras contramedidas se encuentran la de aplicar las directivas de contraseña segura y la protección física de las ubicaciones de los equipos.

##### Impacto potencial

Los usuarios no podrán iniciar sesión en ningún equipo si no hay un controlador de dominio disponible para autenticarlos. Puede que las organizaciones deseen establecer este valor en 2 para equipos de usuario final, en especial si se trata de usuarios móviles. Al establecer este valor en 2, la información de inicio de sesión del usuario aún permanecerá en caché incluso cuando un miembro del departamento de TI haya iniciado sesión recientemente en el equipo para realizar un mantenimiento del sistema. Este método permite a los usuarios iniciar sesión en sus equipos cuando no estén conectados a la red corporativa.

#### Inicio de sesión interactivo: pedir al usuario cambiar la contraseña antes de que caduque

Esta configuración de directiva determina con cuántos días de antelación se advierte a los usuarios de que sus contraseñas están a punto de caducar. Gracias a este mensaje de advertencia, el usuario tendrá tiempo de crear una contraseña suficientemente segura.

Los valores posibles para la configuración **Inicio de sesión interactivo: pedir al usuario cambiar la contraseña antes de que caduque** son:

-   Un número de días especificado por el usuario entre 1 y 999

-   No está definido

##### Vulnerabilidad

Microsoft recomienda que las contraseñas de usuario se configuren para que caduquen de forma periódica. Deberá avisarse a los usuarios que su contraseña va a caducar o, de lo contrario, es probable que el equipo se bloquee de forma inadvertida cuando sus contraseñas caduquen. Esto podría causar confusión en los usuarios que obtienen acceso a la red localmente, o imposibilitar el acceso a los usuarios que obtienen acceso a la red de su organización mediante conexiones de acceso telefónico o de red privada virtual (VPN).

##### Contramedida

Configure **Inicio de sesión interactivo: pedir al usuario cambiar la contraseña antes de que caduque** en 14 días:

##### Impacto potencial

Los usuarios verán un aviso de cambio de contraseña en un cuadro de diálogo cada vez que inicien sesión en el dominio cuando su contraseña está configurada para caducar en 14 días o menos.

#### Inicio de sesión interactivo: requerir la autenticación del controlador de dominio para desbloquear el equipo

La información de inicio de sesión es necesaria para desbloquear un equipo bloqueado. Para las cuentas de dominio, el uso del valor **Inicio de sesión interactivo: requerir la autenticación del controlador de dominio para desbloquear el equipo** determina si es necesario ponerse en contacto con un controlador de dominio para desbloquear un equipo. Si habilita este valor, será necesario que un controlador de dominio autentique la cuenta de dominio en uso para desbloquear el equipo. Si deshabilita este valor, no se requiere la confirmación de información de inicio de sesión con un controlador de dominio para que un usuario desbloquee el equipo. No obstante, si el valor **Inicio de sesión interactivo: núm. de inicios de sesión previos en la caché (en caso que el controlador de dominio no esté disponible)** se configura en un valor mayor que cero, las credenciales del usuario almacenadas en caché se emplearán para desbloquear el equipo.

**Nota**: esta configuración es aplicable a los equipos con Windows 2000, pero no está disponible a través de las herramientas del Administrador de configuración de seguridad de los mismos.

Los valores posibles para la configuración **Inicio de sesión interactivo: requerir la autenticación del controlador de dominio para desbloquear el equipo** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

De forma predeterminada, el equipo almacena en caché las credenciales de cualquier usuario que se haya autenticado de forma local. Al mismo tiempo, el equipo emplea estas credenciales almacenadas en caché para autenticar a quien intente desbloquear la consola. Al emplear credenciales almacenadas en caché, cualquier cambio realizado recientemente en la cuenta, como asignaciones de derechos de usuario, bloqueo de cuentas o que la cuenta esté deshabilitada, no se considerará ni se aplicará hasta que la cuenta se haya autenticado. Los privilegios de usuario no se actualizan y, lo que es más importante, las cuentas deshabilitadas aún podrán desbloquear la consola del equipo.

##### Contramedida

Configure **Inicio de sesión interactivo: requerir la autenticación del controlador de dominio para desbloquear el equipo** como **Habilitado** y configure **Inicio de sesión interactivo: núm. de inicios de sesión previos en la caché (en caso que el controlador de dominio no esté disponible)** en **0**.

##### Impacto potencial

Cuando la consola de un equipo se bloquea (ya sea mediante un usuario o de forma automática con un tiempo de espera del protector de pantalla), sólo podrá desbloquearse si un usuario se puede volver a autenticar en el controlador de dominio. Si no hay un controlador de dominio disponible, los usuarios no podrán desbloquear las estaciones de trabajo. No obstante, si configura **Inicio de sesión interactivo: núm. de inicios de sesión previos en la caché (en caso de que el controlador de dominio no esté disponible)** en **0,**los usuarios cuyos controladores de dominio no estén disponibles (como usuarios móviles o remotos) no podrán iniciar sesión.

#### Inicio de sesión interactivo: necesita una tarjeta inteligente

Esta configuración de directiva requiere que los usuarios tengan que iniciar sesión en un equipo con una tarjeta inteligente.

**Nota**: esta configuración es aplicable a los equipos con Windows 2000, pero no está disponible a través de las herramientas del Administrador de configuración de seguridad de los mismos.

Los valores posibles para la configuración **Inicio de sesión interactivo: necesita una tarjeta inteligente** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

El uso de contraseñas largas y complejas para la autenticación mejora la seguridad de la red, sobre todo si los usuarios deben cambiar las contraseñas con regularidad. Este enfoque reduce la posibilidad de que un atacante pueda averiguar una contraseña de usuario a través de un ataque de fuerza bruta. Sin embargo, es difícil hacer que los usuarios elijan contraseñas seguras, e incluso las contraseñas seguras son vulnerables a ataques de fuerza bruta si un atacante tiene tiempo y recursos informáticos suficientes.  El uso de tarjetas inteligentes en lugar de contraseñas para la autenticación aumenta la seguridad de forma muy notable, dado que, con la tecnología actual, es prácticamente imposible que un atacante suplante a otro usuario. Las tarjetas inteligentes que precisan números de identificación personal (PIN) proporcionan una autenticación de dos factores. Es decir, el usuario debe poseer la tarjeta inteligente y, por otro lado, conocer el PIN correspondiente. Un atacante que capturara el tráfico de autenticación entre el equipo del usuario y el controlador de dominio se encontraría con verdaderas dificultades para descifrar el tráfico y, aun consiguiéndolo, la próxima vez que el usuario iniciara sesión en la red, se generaría una clave de sesión nueva para cifrar el tráfico entre el usuario y el controlador de dominio.

##### Contramedida

Para cuentas importantes, expida tarjetas inteligentes a los usuarios y configure **Inicio de sesión interactivo: necesita una tarjeta inteligente** como **Habilitado.**

##### Impacto potencial

Todos los usuarios deben utilizar tarjetas inteligentes para iniciar sesión en la red, de forma que la organización deberá disponer de una infraestructura de claves públicas (PKI) confiable, además de tarjetas inteligentes y lectores de tarjetas inteligentes para todos los usuarios. Estos requisitos suponen desafíos significativos, porque se precisan recursos y experiencia para planificar e implementar estas tecnologías. Sin embargo, Windows Server 2003 incluye Servicios de Certificate Server, un servicio extremadamente avanzado que sirve para implementar y administrar certificados. Cuando los servicios de certificados se combinan con Windows XP, las características como inscripción y renovación automáticas del equipo y del usuario quedan disponibles.

#### Inicio de sesión interactivo: comportamiento de extracción de tarjeta inteligente

Esta configuración de directiva determina la acción que se debe realizar cuando la tarjeta inteligente de un usuario que ha iniciado sesión se retira del lector de tarjetas inteligentes.

Los valores posibles para la configuración **Inicio de sesión interactivo: comportamiento de extracción de tarjeta inteligente** son:

-   No se requiere acción

-   Bloquear estación de trabajo

-   Forzar cierre de sesión

-   No está definido

##### Vulnerabilidad

Si se utilizan tarjetas inteligentes para la autenticación, el equipo deberá bloquearse automáticamente cuando la tarjeta inteligente se extraiga. Este enfoque evitará que usuarios malintencionados tengan acceso a los equipos de usuarios que olviden bloquear manualmente las estaciones de trabajo cuando estén alejados.

##### Contramedida

Configure **Comportamiento de extracción de tarjeta inteligente** en **Bloquear estación de trabajo**.

Si selecciona **Bloquear estación de trabajo** en el cuadro de diálogo **Propiedades** para esta configuración de directiva, la estación de trabajo se bloqueará cuando se extraiga la tarjeta inteligente. Los usuarios pueden salir de la zona, llevarse las tarjetas inteligentes consigo y seguir manteniendo una sesión protegida.

Si selecciona **Forzar cierre de sesión** en el cuadro de diálogo **Propiedades**, se cierra automáticamente la sesión del usuario cuando la tarjeta inteligente se extrae.

##### Impacto potencial

Los usuarios deben volver a insertar las tarjetas inteligentes y a introducir el PIN cuando vuelvan a sus respectivas estaciones de trabajo.

#### Servidor y cliente de red de Microsoft: firmar digitalmente las comunicaciones (cuatro valores relacionados)

Existen cuatro configuraciones distintas en relación con la firma digital de las comunicaciones de Bloques de mensajes del servidor (SMB):

-   **Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (siempre)**

-   **Servidor de red de Microsoft: firmar digitalmente las comunicaciones (siempre)**

-   **Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)**

-   **Servidor de red de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)**

Los valores que se pueden seleccionar para estas configuraciones de directiva son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

La implementación de firmas digitales en redes de alta seguridad ayuda a evitar la suplantación de clientes y servidores. Este tipo de suplantación se conoce como secuestro de sesión; se utilizan herramientas que permiten que un atacante que ha tenido acceso a la misma red que el cliente o el servidor pueda interrumpir, finalizar o robar una sesión en progreso. Los atacantes pueden interceptar y modificar paquetes SMB sin firmar, alterar el tráfico a continuación y reenviarlo de manera que el servidor pueda realizar acciones no deseadas. Otro modo de ataque consiste en actuar como el servidor o el cliente tras autenticarse de forma legítima y obtener acceso no autorizado a los datos.

SMB es el protocolo para compartir recursos que es compatible con muchos de los sistemas operativos de Microsoft. Es la base de NetBIOS y de muchos otros protocolos. Las firmas SMB autentican tanto al usuario como al servidor donde se alojan los datos. Si se produce un error en alguno de ellos durante el proceso de autenticación, la transmisión de datos no se realizará.

**Nota**: otra posible contramedida con la que proteger todo el tráfico en la red consistiría en implementar firmas digitales con IPsec. Existen aceleradores basados en hardware para el cifrado y la firma de IPsec que podrían emplearse para reducir el impacto de rendimiento en CPU del servidor. Sin embargo, este tipo de aceleradores no existen para la firma SMB.

##### Contramedida

Configure la directiva de la siguiente manera:

-   **Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (siempre)** como **Deshabilitado**

-   **Servidor de redes de Microsoft: firmar digitalmente las comunicaciones (siempre)** como **Deshabilitado**

-   **Cliente de redes de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)** como **Habilitado**

-   **Servidor de red de Microsoft: firmar digitalmente las comunicaciones (si el servidor lo permite)** como **Habilitado**.

Algunos recursos recomiendan que configure todos estos valores como **Habilitado.** Sin embargo, esa configuración puede afectar el rendimiento de equipos cliente y evitar las comunicaciones con aplicaciones y sistemas operativos SMB heredados.

##### Impacto potencial

Las implementaciones del protocolo SMB de uso compartido de archivos e impresoras de Windows 2000 Server, Windows 2000 Professional, Windows Server 2003 y Windows XP Professional es compatible con la autenticación mutua, que previene los ataques de secuestro de sesión y admite la autenticación de mensaje para evitar los ataques de intermediario. La firma de SMB proporciona esta autenticación colocando una firma digital en cada SMB, que posteriormente comprueban el cliente y el servidor. La implementación de firmas SMB puede afectar negativamente al rendimiento ya que cada paquete debe firmarse y verificarse. Si los equipos se configuran para omitir todas las comunicaciones SMB sin firmar, las aplicaciones y los sistemas operativos anteriores no se podrán conectar entre sí. Si deshabilita completamente las firmas SMB, los equipos serán vulnerables a los ataques de secuestro de sesión.

#### Cliente de redes de Microsoft: enviar contraseña no cifrada para conectar SMB de otros fabricantes

Esta configuración de directiva permite al redirector SMB enviar contraseñas de texto sin formato a servidores SMB que no sean de Microsoft y no sean compatibles con el cifrado de contraseñas durante la autenticación.

Los valores posibles para la configuración **Cliente de redes de Microsoft: enviar contraseña no cifrada para conectar SMB de otros fabricantes** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Si habilita esta configuración de directiva, el servidor podrá transmitir contraseñas en texto sin formato a través de la red a otros equipos que proporcionen servicios SMB. Puede que estos otros equipos no utilicen ninguno de los mecanismos de seguridad SMB que se incluyen en Windows Server 2003.

##### Contramedida

Configure **Cliente de redes de Microsoft: enviar contraseña no cifrada para conectar a servidores SMB de terceros** como **Deshabilitado**.

##### Impacto potencial

Es posible que existan aplicaciones y sistemas operativos antiguos (como MS-DOS, Windows Para Trabajo en Grupo 3.11 y Windows 95a) que no puedan comunicarse con los servidores de la organización mediante el protocolo SMB.

#### Servidor de red de Microsoft: tiempo de inactividad requerido antes de suspender la sesión

Esta configuración de directiva determina el tiempo de inactividad continuado que debe transcurrir en una sesión de SMB antes de que la sesión se suspenda por inactividad. Los administradores pueden utilizar esta configuración de directiva para controlar el momento en que un equipo suspende una sesión SMB inactiva. La sesión se restablece automáticamente en el momento en que la actividad se reanuda. Un valor de **0** indica que la sesión inactiva se desconectará tan pronto como sea posible. El valor máximo es 99999, que corresponde a 208 días; en la práctica, este valor deshabilita el valor de directiva de grupo.

Los valores posibles para la configuración **Servidor de red de Microsoft: tiempo de inactividad requerido antes de suspender la sesión** son:

-   Período de tiempo en minutos definido por el usuario

-   No está definido

##### Vulnerabilidad

Cada sesión SMB consume recursos del servidor y, si se establecen varias sesiones nulas, el servidor puede funcionar más lento o incluso fallar. Un atacante puede establecer sesiones SMB de forma repetida hasta conseguir que el servidor se vuelva lento o deje de responder.

##### Contramedida

Configure **Servidor de red de Microsoft: tiempo de inactividad requerido antes de desconectar la sesión** en **15 minutos**.

##### Impacto potencial

El impacto es mínimo, dado que las sesiones SMB se restablecerán automáticamente cuando el cliente reanude la actividad.

#### Servidor de red de Microsoft: desconectar a los clientes cuando termine el tiempo de sesión

Esta configuración de directiva determina si se desconectará a los usuarios que están conectados al equipo local fuera de las horas de inicio de sesión válidas de sus cuentas de usuario. Afecta al componente SMB. Si habilita esta configuración de directiva, se fuerza la desconexión de las sesiones de cliente con el servicio SMB cuando se agoten las horas de inicio de sesión del cliente. Si deshabilita esta configuración de directiva, las sesiones de cliente establecidas se mantendrán después de las horas de inicio de sesión del cliente. Si habilita esta configuración de directiva, también deberá habilitar **Seguridad de red: forzar el cierre de sesión cuando expire la hora de inicio de sesión**.

Los valores posibles para la configuración **Servidor de red de Microsoft: desconectar a los clientes cuando termine el tiempo de sesión** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Si su organización configura el tiempo de sesión de los usuarios, resulta buena idea habilitar esta configuración de directiva. De lo contrario, los usuarios que no deben tener acceso a los recursos de la red fuera del tiempo de sesión que les corresponde, en realidad podrán continuar utilizando los recursos en distintas sesiones establecidas durante las horas permitidas.

##### Contramedida

Habilite la configuración **Servidor de red de Microsoft: desconectar a los clientes cuando termine el tiempo de sesión**.

##### Impacto potencial

Si su organización no controla el tiempo de sesión, esta configuración de directiva no tendrá ningún efecto. Si, por el contrario, sí lo controla, las sesiones de los usuarios se darán por terminadas en cuanto expire el tiempo de sesión correspondiente.

#### Acceso de red: permitir traducción SID/nombre anónima

Esta configuración de directiva determina si un usuario anónimo puede solicitar atributos de SID de otro.

Los valores posibles para la configuración **Acceso de red: permitir traducción SID/nombre anónima** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Si esta configuración de directiva se habilita, un usuario con acceso local podrá utilizar el SID conocido del administrador para averiguar el nombre real de la cuenta del administrador integrado, incluso si se ha cambiado el nombre de la cuenta. Esa persona podría entonces utilizar el nombre de cuenta para iniciar un ataque de contraseña.

##### Contramedida

Configure **Acceso de red: permitir traducción SID/nombre anónima** como **Deshabilitado**.

##### Impacto potencial

**Deshabilitado** es la configuración predeterminada de esta configuración de directiva en los equipos miembros, lo que significa que no tendrá efecto alguno sobre ellos. El valor de configuración predeterminado de los controladores de dominio es **Habilitado**. Si deshabilita esta configuración de directiva en controladores de dominio, puede que los equipos heredados sean incapaces de comunicarse con dominios basados en Windows Server 2003. Por ejemplo, puede que los siguientes equipos no funcionen:

-   Servidores de servicio de acceso remoto (RAS) basados en Microsoft Windows NT 4.0.

-   Microsoft SQL Servers™ en equipos Windows NT 3.X o Windows NT 4.0.

-   Equipos basados en servidores Microsoft SQL de servicio de acceso remoto Windows 2000 ubicados en dominios Windows NT 3.x o Windows NT 4.0.

#### Acceso a redes: no permitir enumeraciones anónimas de cuentas SAM

Esta configuración de directiva determina los permisos adicionales que se otorgarán para conexiones anónimas al equipo. Windows permite a los usuarios anónimos realizar determinadas actividades, como la enumeración de nombres de cuentas de dominio y recursos compartidos de red. Esta opción resulta útil, por ejemplo, cuando un administrador desea conceder acceso a usuarios en un dominio de confianza que no mantiene una confianza recíproca. Sin embargo, incluso si este valor está habilitado, los usuarios anónimos tendrán acceso a cualquier recurso con permisos que incluyen, de forma explícita, el grupo integrado especial **INICIO DE SESIÓN ANÓNIMO**.

En Windows 2000, una configuración de directiva similar denominada **Restricciones adicionales para conexiones anónimas** administraba un valor del Registro denominado **RestrictAnonymous**, que se encontraba en la clave del Registro **HKLM\\SYSTEM\\CurrentControlSet\\Control\\LSA**. En Windows Server 2003, la configuración de directiva **Acceso a redes: no permitir enumeraciones anónimas de cuentas SAM** y **Acceso de red: no permitir enumeraciones anónimas de cuentas y recursos compartidos SAM** sustituyen la configuración de directiva de Windows 2000. Ambas se encargan de administrar los valores de Registro **RestrictAnonymousSAM** y **RestrictAnonymous** respectivamente, que se encuentran en la clave de Registro **HKLM\\System\\CurrentControlSet\\Control\\Lsa\\**.

Los valores posibles para la configuración **Acceso a redes: no permitir enumeraciones anónimas de cuentas SAM** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Un usuario no autorizado puede obtener de forma anónima una lista con los nombres de cuentas y utilizar dicha información para intentar averiguar contraseñas o realizar ataques de ingeniería social. (Los ataques de ingeniería social tratan de engañar a los usuarios para obtener contraseñas o alguna otra forma de información de seguridad.)

##### Contramedida

Configure **Acceso a redes: no permitir enumeraciones anónimas de cuentas SAM** como **Habilitado**.

##### Impacto potencial

Resultará imposible establecer confianzas con dominios basados en Windows NT 4.0. Además, los equipos cliente que ejecutan versiones anteriores del sistema operativo Windows, tales como Windows NT 3.51 y Windows 95, experimentarán problemas al tratar de utilizar los recursos en el servidor.

#### Acceso a redes: no permitir enumeraciones anónimas de cuentas y recursos compartidos SAM

Esta configuración de directiva determina si se permite la enumeración anónima de cuentas y recursos compartidos del Administrador de cuentas de seguridad (SAM). Como se hizo notar en la sección anterior, Windows permite a los usuarios anónimos realizar determinadas actividades, como la enumeración de nombres de cuentas de dominio y recursos compartidos de red. Esta opción resulta útil, por ejemplo, cuando un administrador desea conceder acceso a usuarios en un dominio de confianza que no mantiene una confianza recíproca. Puede habilitar esta configuración de directiva si no desea permitir la enumeración anónima de cuentas y recursos compartidos SAM. Sin embargo, incluso si este valor está habilitado, los usuarios anónimos tendrán acceso a cualquier recurso con permisos que incluyen, de forma explícita, el grupo integrado especial **INICIO DE SESIÓN ANÓNIMO**.

En Windows 2000, una configuración de directiva similar denominada **Restricciones adicionales para conexiones anónimas** administraba un valor del Registro denominado **RestrictAnonymous**, que se encontraba en la clave del Registro **HKLM\\SYSTEM\\CurrentControlSet\\Control\\LSA**. En Windows Server 2003, las directivas **Acceso a redes: no permitir enumeraciones anónimas de cuentas SAM** y **Acceso de red: no permitir enumeraciones anónimas de cuentas y recursos compartidos SAM** sustituyen el valor de configuración de Windows 2000. Ambas se encargan de administrar los valores de Registro **RestrictAnonymousSAM** y **RestrictAnonymous** respectivamente, que se encuentran en la clave de Registro **HKLM\\System\\CurrentControlSet\\Control\\Lsa\\**.

Los valores posibles para la configuración **Acceso a redes: no permitir enumeraciones anónimas de cuentas y recursos compartidos SAM** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Un usuario no autorizado podría obtener de forma anónima una lista de los nombres de las cuentas y los recursos compartidos y utilizar dicha información para intentar averiguar contraseñas o realizar ataques de ingeniería social.

##### Contramedida

Configure **Acceso a redes: no permitir enumeraciones anónimas de cuentas y recursos compartidos SAM** como **Habilitado**.

##### Impacto potencial

No se podrá conceder acceso a usuarios de otro dominio a través de una confianza de una sola dirección, ya que los administradores del dominio de confianza no podrán enumerar listas de cuentas del otro dominio. Los usuarios con acceso anónimo a servidores de archivo e impresoras tampoco podrán enumerar los recursos compartidos de red en tales servidores, de tal modo que se deben autenticar antes de poder ver las listas de carpetas e impresoras compartidas.

#### Acceso a redes: no permitir el almacenamiento de credenciales o .NET Passports para la autenticación del dominio

Esta configuración de directiva determina si, una vez conseguida la autenticación en el dominio, la característica Nombres de usuarios y contraseñas almacenados puede guardar las contraseñas o credenciales para un uso posterior, cuando tenga autenticación de dominio. Si habilita esta configuración de directiva, la característica Nombres de usuarios y contraseñas almacenados de Windows no almacena contraseñas y credenciales.

Los valores posibles para la configuración **Acceso a redes: no permitir el almacenamiento de credenciales o .NET Passports para la autenticación del dominio** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Cuando inicie sesión en el equipo, el usuario podrá tener acceso a las contraseñas almacenadas en caché. Aunque esta información puede parecer obvia, puede surgir un problema si un usuario ejecuta sin saberlo un código hostil que lee las contraseñas y las reenvía a otro usuario no autorizado.

**Nota**: las posibilidades de que esta explotación y otras relacionadas con códigos hostiles tengan éxito se reducirán considerablemente en aquellas organizaciones que implementen y administren soluciones antivirus para empresas de forma eficaz, junto con directivas de restricción de software confidencial. Para obtener más información sobre las directivas de restricción de software consulte el capítulo 8 "Directivas de restricción de software".

##### Contramedida

Configure **Acceso a redes: no permitir el almacenamiento de credenciales o .NET Passports para la autenticación del dominio** como **Habilitado**.

##### Impacto potencial

Los usuarios deberán introducir contraseñas siempre que inicien sesión en su cuenta Passport o en otros recursos de red a los que no tiene acceso desde su cuenta de dominio. Esta configuración de directiva no debería afectar a los usuarios que obtienen acceso a los recursos de red y que están configurados para permitir el acceso con su cuenta de dominio basada en Active Directory.

#### Acceso de red: deja los permisos de Todos para aplicarse a usuarios anónimos

Esta configuración de directiva determina los permisos adicionales que se otorgan para conexiones anónimas al equipo. Si habilita esta configuración de directiva se permite a los usuarios anónimos la enumeración de nombres de cuentas de dominio y recursos compartidos de red y la realización de otras actividades. Esta opción resulta útil, por ejemplo, cuando un administrador desea conceder acceso a usuarios en un dominio de confianza que no mantiene una confianza recíproca.

De forma predeterminada, el token creado para conexiones anónimas no incluye el SID de Todos. Por lo tanto, los permisos que se asignan al grupo **Todos** no se aplican a los usuarios anónimos. Si habilita esta configuración de directiva, el SID de Todos se agrega al token que se crea para conexiones anónimas, y los usuarios anónimos podrán tener acceso a cualquier recurso para el que se hayan asignado permisos para el grupo **Todos**.

Los valores posibles para la configuración **Acceso de red: deja los permisos de Todos para aplicarse a usuarios anónimos** son:

-   Habilitada

-   Deshabilitado

-   No está definido

##### Vulnerabilidad

Un usuario no autorizado podría obtener de forma anónima una lista de los nombres de las cuentas y los recursos compartidos y utilizar dicha información para intentar averiguar contraseñas, realizar ataques de ingeniería social o lanzar ataques DoS.

##### Contramedida

Configure **Acceso de red: deja los permisos de Todos para aplicarse a usuarios anónimos** como **Deshabilitado**.

##### Impacto potencial

Ninguno. Ésta es la configuración predeterminada.

#### Acceso de red: canalizaciones con nombre accesibles anónimamente

Esta configuración de directiva determina qué sesiones de comunicación o canalizaciones tendrán atributos y permisos que les permitan el acceso anónimo.

Los valores posibles para la configuración **Acceso de red: canalizaciones con nombre accesibles anónimamente** son:

-   Una lista de recursos compartidos definida por el usuario

-   No está definido

Para que esta configuración de directiva surta efecto, debe habilitar también la configuración **Acceso de red: restringir acceso anónimo a canalizaciones con nombre y recursos compartidos**.

##### Vulnerabilidad

Puede restringir el acceso a canalizaciones con nombre como COMNAP y LOCATOR, para ayudar a evitar el acceso no autorizado a la red. La lista predeterminada de canalizaciones con nombre y su finalidad se proporciona en la tabla siguiente.

**Tabla 5.1: Canalizaciones con nombre predeterminadas a las que se puede tener acceso anónimamente**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Canalización con nombre</p></th>
<th><p>Finalidad</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>COMNAP</p></td>
<td style="border:1px solid black;"><p>Canalización con nombre SNABase. La arquitectura de redes de sistemas (SNA) es una recopilación de protocolos de red que se desarrolló en un principio para los equipos de grandes sistemas de IBM.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>COMNODE</p></td>
<td style="border:1px solid black;"><p>Canalización con nombre SNA Server.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>SQL\QUERY</p></td>
<td style="border:1px solid black;"><p>Canalización con nombre predeterminada para SQL Server.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>SPOOLSS</p></td>
<td style="border:1px solid black;"><p>Canalización con nombre para el servicio de cola de impresión.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>EPMAPPER</p></td>
<td style="border:1px solid black;"><p>Canalización con nombre de asignador de puntos finales.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>LOCATOR</p></td>
<td style="border:1px solid black;"><p>Canalización con nombre del servicio Localizador de llamada a procedimiento remoto.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>TrkWks</p></td>
<td style="border:1px solid black;"><p>Canalización con nombre de Cliente de seguimiento de vínculos distribuidos.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>TrkSvr</p></td>
<td style="border:1px solid black;"><p>Canalización con nombre de Servidor de seguimiento de vínculos distribuidos.</p></td>
</tr>  
</tbody>  
</table>
  
##### Contramedida
  
Configure **Acceso de red: canalizaciones con nombre accesibles anónimamente** con un valor nulo (es decir, habilite la configuración pero no introduzca canalizaciones con nombre en el cuadro de texto).
  
##### Impacto potencial
  
Esta configuración deshabilitará el acceso a sesión nula a través de canalizaciones con nombre y aplicaciones que utilizan esta característica o el acceso no autenticado a canalizaciones con nombre dejará de funcionar. Por ejemplo, con Microsoft Commercial Internet System 1.0, el servicio de correo de Internet se ejecuta con el proceso Inetinfo. Inetinfo se inicia en el contexto de la cuenta de sistema. Cuando el servicio de correo de Internet requiere realizar una consulta en la base de datos Microsoft SQL Server, utiliza la cuenta del sistema, que utiliza credenciales nulas para obtener acceso a una canalización SQL del equipo que está ejecutando SQL Server.
  
Para evitar este problema, consulte el artículo de Microsoft Knowledge Base "[How to access network files from IIS applications](http://support.microsoft.com/default.aspx?scid=207671)" en http://support.microsoft.com/default.aspx?scid=207671.
  
#### Acceso de red: rutas de Registro accesibles remotamente
  
Esta configuración de directiva determina qué rutas del registro serán accesibles cuando una aplicación o proceso hace referencia a la clave de **WinReg** para determinar los permisos de acceso.
  
Los valores posibles para la configuración **Acceso de red: rutas de Registro accesibles remotamente** son:
  
-   Una lista de rutas definida por el usuario
  
-   No está definido
  
##### Vulnerabilidad
  
El Registro es una base de datos que contiene información de configuración del equipo y la mayor parte de esta información es importante. Un atacante podría utilizar estos datos para facilitar actividades no autorizadas. Para reducir el riesgo de un ataque de este tipo, se asignan listas de control de acceso adecuadas a través del Registro para protegerlo del acceso de usuarios no autorizados.
  
##### Contramedida
  
Configure **Acceso de red: rutas de Registro accesibles remotamente** con un valor nulo (es decir, habilite la configuración pero no introduzca ninguna ruta en el cuadro de texto).
  
##### Impacto potencial
  
Las herramientas de administración remota como Microsoft Baseline Security Analyzer y Microsoft Systems Management Server requieren acceso remoto al Registro para supervisar y administrar correctamente dichos equipos. Si quita las rutas del Registro predeterminadas de la lista de las accesibles, es posible que tales herramientas de administración remota no puedan ejecutarse.
  
**Nota**: si desea permitir el acceso remoto, deberá habilitar también el servicio de Registro remoto.
  
#### Acceso de red: rutas y subrutas de Registro accesibles remotamente
  
Esta configuración de directiva determina qué rutas y subrutas del registro serán accesibles cuando una aplicación o proceso haga referencia a la clave de **WinReg** para determinar los permisos de acceso.
  
Los valores posibles para la configuración **Acceso de red: rutas y subrutas de Registro accesibles remotamente** son:
  
-   Una lista de rutas definida por el usuario
  
-   No está definido
  
##### Vulnerabilidad
  
Como ya se señaló, el registro contiene información importante de configuración del equipo que podría ser utilizada por un atacante para facilitar actividades no autorizadas. Este riesgo se reduce gracias que las listas ACL predeterminadas que se asignan a través del Registro son considerablemente restrictivas y ayudan a protegerlo del acceso de usuarios no autorizados.
  
##### Contramedida
  
Configure **Acceso de red: rutas y subrutas de Registro accesibles remotamente** con un valor nulo (es decir, habilite la configuración pero no introduzca ninguna ruta en el cuadro de texto).
  
##### Impacto potencial
  
Las herramientas de administración remota como Microsoft Baseline Security Analyzer y Microsoft Systems Management Server requieren acceso remoto al Registro para supervisar y administrar correctamente dichos equipos. Si quita las rutas del Registro predeterminadas de la lista de las accesibles, es posible que tales herramientas de administración remota no puedan ejecutarse.
  
**Nota**: si desea permitir el acceso remoto, deberá habilitar también el servicio de Registro remoto.
  
#### Acceso de red: restringir acceso anónimo a canalizaciones con nombre y recursos compartidos
  
Cuando está habilitada, esta configuración de directiva restringe el acceso anónimo a los recursos compartidos y canalizaciones con nombre en las configuraciones **Acceso de red: canalizaciones con nombre accesibles anónimamente** y **Acceso de red: recursos compartidos accesibles anónimamente**. Esta configuración de directiva controla el acceso de sesión nulo a los recursos compartidos de los equipos, agregando **RestrictNullSessAccess** con el valor **1** en la clave del registro **HKLM\\System\\CurrentControlSet\\Services\\LanManServer\\Parameters.** El valor de registro activa y desactiva los recursos compartidos de sesión nula para controlar si el servicio de servidor restringe el acceso de los clientes sin autenticación a los recursos con nombre.
  
Los valores posibles para la configuración **Acceso de red: restringir acceso anónimo a canalizaciones con nombre y recursos compartidos** son:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Vulnerabilidad
  
Las sesiones nulas son un punto débil que puede explotarse a través de los distintos recursos compartidos (incluidos los predeterminados) en los equipos de su entorno.
  
##### Contramedida
  
Configure **Acceso de red: restringir acceso anónimo a canalizaciones con nombre y recursos compartidos** como **Habilitado**.
  
##### Impacto potencial
  
Puede habilitar esta configuración de directiva para restringir el acceso a sesión nula para usuarios no autenticados en todas las canalizaciones y recursos compartidos de servidor, excepto los que aparecen en las entradas **NullSessionPipes** y **NullSessionShares.**
  
#### Acceso de red: recursos compartidos accesibles anónimamente
  
Esta configuración de directiva determina a qué recursos compartidos de red pueden tener acceso los usuarios anónimos.
  
Los valores posibles para la configuración **Acceso de red: recursos compartidos accesibles anónimamente** son:
  
-   Una lista de recursos compartidos definida por el usuario
  
-   No está definido
  
##### Vulnerabilidad
  
Es muy peligroso habilitar este parámetro. Los recursos compartidos que se enumeran en la lista están accesibles para cualquier usuario de la red, lo que podría resultar en la exposición o daños de datos confidenciales.
  
##### Contramedida
  
Configure **Acceso de red: recursos compartidos accesibles anónimamente** con un valor nulo.
  
##### Impacto potencial
  
El impacto debería ser pequeño dado que éste es el valor de configuración predeterminado. Sólo los usuarios autenticados tendrán acceso a los recursos compartidos del servidor.
  
#### Acceso de red: modelo de seguridad y para compartir para cuentas locales
  
Esta configuración de directiva determina la forma en que se autentican los inicios de sesión de red que utilizan cuentas locales. Si establece esta configuración de directiva en **Clásico**, los inicios de sesión de red que utilicen credenciales de cuenta local se autenticarán con dichas credenciales. Si establece esta configuración de directiva en **Sólo invitado**, los inicios de sesión de red que utilicen cuentas locales se asignarán automáticamente a la cuenta de invitado. El modelo **Clásico** proporciona un control preciso sobre el acceso a los recursos y permite otorgar diferentes tipos de acceso a distintos usuarios para el mismo recurso. Por su parte, el modelo **Sólo invitado** trata a todos los usuarios por igual como la cuenta de usuario de invitado, y reciben el mismo nivel de acceso a un determinado recurso, que puede tener propiedades como Sólo lectura o Modificar.
  
El valor predeterminado en Windows XP Professional independiente es **Sólo invitado**. El valor predeterminado para equipos Windows XP asociados a un dominio y a equipos Windows Server 2003 es **Clásico**.
  
**Nota**: esta configuración de directiva no afecta a los inicios de sesión de red que utilizan cuentas de dominio. Esta configuración de directiva tampoco afecta a los inicios de sesión interactivos que se realizan de forma remota al utilizar servicios como Telnet o Servicios de Terminal Server.
  
Cuando un equipo no se une a un dominio, esta configuración de directiva también ajusta las fichas **Compartir** y **Seguridad** del Explorador de Windows para corresponder al modelo seguridad y para compartir que se está utilizando.
  
Este valor no tiene ningún efecto en los equipos con Windows 2000.
  
Los valores posibles para la configuración **Acceso de red: modelo de seguridad y para compartir para cuentas locales** son:
  
-   Clásico. Los usuarios locales se autentican como ellos mismos.
  
-   Sólo invitado. Los usuarios locales se autentican como invitados.
  
-   No está definido
  
##### Vulnerabilidad
  
Con el modelo **Sólo invitado**, cualquier usuario que pueda autenticarse en su equipo a través de la red lo hace con privilegios de invitado, lo que puede suponer que no tenga acceso de escritura a recursos compartidos en ese equipo. Aunque esta restricción aumenta la seguridad, dificulta el acceso de los usuarios autorizados a los recursos compartidos en esos equipos, porque las listas ACL en esos recursos deben incluir entradas de control de acceso (ACE) para la cuenta de invitado. Con el modelo **Clásico**, las cuentas locales deben estar protegidas por contraseña. De lo contrario, si el acceso de invitado está habilitado, cualquiera puede utilizar esas cuentas de usuario para obtener acceso a recursos del sistema compartidos.
  
##### Contramedida
  
Para los servidores de la red, establezca el valor de configuración **Acceso de red: modelo de seguridad y para compartir para cuentas locales** en **Clásico: usuarios locales autenticados como ellos mismos**. Para sistemas de usuario final, establezca esta configuración de directiva en **Sólo invitado: usuarios locales autenticados como invitados**.
  
##### Impacto potencial
  
Ninguno. Ésta es la configuración predeterminada.
  
#### Seguridad de red: no almacenar valor de hash de LAN Manager en el próximo cambio de contraseña
  
Esta configuración de directiva determina si LAN Manager puede almacenar valores de hash para la contraseña nueva la próxima vez que cambie la contraseña.
  
Los valores posibles para la configuración **Seguridad de red: no almacenar valor de hash de LAN Manager en el próximo cambio de contraseña** son:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Vulnerabilidad
  
El archivo SAM puede ser objeto de ataques por parte de personas que buscan acceso a los valores hash de nombre de usuario y contraseña. Dichos ataques utilizan herramientas especiales para averiguar las contraseñas, que entonces pueden utilizarse para suplantar a usuarios y obtener acceso a recursos en su red. Estos tipos de ataques no se evitarán si habilita esta configuración de directiva, pero será mucho más difícil que tengan éxito.
  
##### Contramedida
  
Configure **Seguridad de red: no almacenar valor de hash de LAN Manager en el próximo cambio de contraseña** como **Habilitado**. Solicite a todos los usuarios que establezcan contraseñas nuevas la próxima vez que inicien sesión en el dominio para eliminar los valores hash de LAN Manager.
  
##### Impacto potencial
  
Los sistemas operativos anteriores como Windows 95, Windows 98 y Windows ME, así como algunas aplicaciones de terceros producirán un error.
  
#### Seguridad de red: forzar el cierre de sesión cuando expire la hora de inicio de sesión
  
Esta configuración de directiva determina si se desconectará a los usuarios que están conectados al equipo local fuera de las horas de inicio de sesión válidas de sus cuentas de usuario. Afecta al componente SMB. Si habilita esta configuración de directiva, se fuerza la desconexión de las sesiones de cliente con el servidor SMB cuando se agoten las horas de inicio de sesión del cliente. Si deshabilita esta configuración de directiva, las sesiones de cliente establecidas se mantendrán después de las horas de inicio de sesión del cliente.
  
Los valores posibles para la configuración **Seguridad de red: forzar el cierre de sesión cuando expire la hora de inicio de sesión** son:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Vulnerabilidad
  
Si deshabilita esta configuración de directiva, un usuario puede permanecer conectado al equipo fuera de sus horas de inicio de sesión permitidas.
  
##### Contramedida
  
Configure **Seguridad de red: forzar el cierre de sesión cuando expire la hora de inicio de sesión** como **Habilitado**. Esta configuración de directiva no se aplica a cuentas de administrador.
  
##### Impacto potencial
  
Cuando se termina el periodo de inicio de sesión de un usuario, las sesiones SMB finalizan. El usuario ya no podrá iniciar sesión en el equipo hasta el momento en que empiece el siguiente periodo de acceso programado.
  
#### Seguridad de red: nivel de autenticación de LAN Manager
  
LAN Manager (LM) es una familia del primer software cliente/servidor de Microsoft que permite a los usuarios enlazar equipos personales a una única red. Entre las capacidades de la red se incluyen el uso compartido transparente de archivos e impresoras, características de seguridad de usuario y herramientas de administración de red. En dominios de Active Directory, el protocolo Kerberos es el protocolo predeterminado de autenticación. Sin embargo, si el protocolo Kerberos no se negocia por alguna razón, Active Directory utilizará LM, NTLM o NTLMv2.
  
La autenticación LAN Manager incluye las variantes LM, NTLM y NTLM versión 2 (NTLMv2), y es el protocolo utilizado para autenticar todos los clientes de Windows cuando realizan operaciones como las siguientes:
  
-   Unirse a un dominio.
  
-   Autenticar entre bosques de Active Directory
  
-   Autenticar en dominios de nivel inferior
  
-   Autenticar en equipos sin Windows 2000, Windows Server 2003 o Windows XP
  
-   Autenticar en equipos que no forman parte del dominio
  
Los valores posibles para la configuración **Seguridad de red: nivel de autenticación de LAN Manager** son:
  
-   Enviar respuestas de LM y NTLM
  
-   Enviar Lan Manager y NT Lan Manager: usar la seguridad de sesión NT Lan Manager versión 2 si se negocia
  
-   Enviar sólo respuesta NTLM
  
-   Enviar sólo respuesta NTLMv2
  
-   Enviar sólo respuesta NTLMv2\\rechazar LM
  
-   Enviar sólo respuesta NTLMv2\\rechazar LM y NTLM
  
-   No está definido
  
El valor de configuración **Seguridad de red: nivel de autenticación de LAN Manager** determina el protocolo de autenticación de desafío/respuesta que se utiliza para los inicios de sesión en la red. Esta opción afecta al nivel de protocolo de autenticación utilizado por los clientes, al nivel de seguridad de la sesión que negocia el sistema y al nivel de autenticación aceptada por los servidores, como se detalla a continuación:
  
-   **Enviar respuestas de LM y NTLM**. Los clientes utilizan la autenticación LM y NTLM y nunca utilizan la seguridad de sesión NTLMv2. Los controladores de dominio aceptan la autenticación LM, NTLM y NTLMv2.
  
-   **Enviar LM y NTLM: usar la seguridad de sesión NTLMv2 si se negocia**. los clientes utilizan la autenticación LM y NTLM así como la seguridad de sesión NTLMv2 si el servidor la admite. Los controladores de dominio aceptan la autenticación LM, NTLM y NTLMv2.
  
-   **Enviar sólo respuesta NTLM**. los clientes utilizan sólo la autenticación NTLM y la seguridad de sesión NTLMv2 si el servidor la admite. Los controladores de dominio aceptan la autenticación LM, NTLM y NTLMv2.
  
-   **Enviar sólo respuesta NTLMv2**. los clientes utilizan sólo la autenticación NTLMv2 y la seguridad de sesión NTLMv2 si el servidor la admite. Los controladores de dominio aceptan la autenticación LM, NTLM y NTLMv2.
  
-   **Enviar sólo respuesta NTLMv2\\rechazar LM**. los clientes utilizan sólo la autenticación NTLMv2 y la seguridad de sesión NTLMv2 si el servidor la admite. Los controladores de dominio rechazan la autenticación LM (sólo aceptan la autenticación NTLM y NTLMv2).
  
-   **Enviar sólo respuesta NTLMv2\\rechazar LM y NTLM**. los clientes utilizan sólo la autenticación NTLMv2 y la seguridad de sesión NTLMv2 si el servidor la admite. Los controladores de dominio rechazan la autenticación LM y NTLM (sólo aceptan la autenticación NTLMv2).
  
Estos valores corresponden a los niveles discutidos en otros documentos de Microsoft como se muestra a continuación:
  
-   **Nivel 0: enviar respuestas de LM y NTLM, no usar nunca la seguridad de sesión NTLMv2**. Los clientes utilizan la autenticación LM y NTLM y nunca utilizan la seguridad de sesión NTLMv2. Los controladores de dominio aceptan la autenticación LM, NTLM y NTLMv2.
  
-   **Nivel 1: usar la seguridad de sesión NTLMv2 si se negocia**. Los clientes utilizan la autenticación LM y NTLM así como la seguridad de sesión NTLMv2 si el servidor la admite. Los controladores de dominio aceptan la autenticación LM, NTLM y NTLMv2.
  
-   **Nivel 2: enviar sólo respuesta NTLM**. Los clientes utilizan sólo la autenticación NTLM y la seguridad de sesión NTLMv2 si el servidor la admite. Los controladores de dominio aceptan la autenticación LM, NTLM y NTLMv2.
  
-   **Nivel 3: enviar sólo respuesta NTLMv2**. Los clientes utilizan la autenticación NTLMv2 y la seguridad de sesión NTLMv2 si el servidor la admite. Los controladores de dominio aceptan la autenticación LM, NTLM y NTLMv2.
  
-   **Nivel 4: los controladores de dominio rechazan la respuesta LM**. Los clientes utilizan la autenticación NTLM y la seguridad de sesión NTLMv2 si el servidor la admite. Los controladores de dominio rechazan la autenticación LM, es decir, aceptan la autenticación NTLM y NTLMv2.
  
-   **Nivel 5: los controladores de dominio rechazan la respuesta LM y NTLM (aceptan sólo NTLMv2)**. Los clientes utilizan la autenticación NTLMv2 y la seguridad de sesión NTLMv2 si el servidor la admite. Los controladores de dominio rechazan la autenticación NTLM y LM (sólo aceptan la autenticación NTLMv2).
  
##### Vulnerabilidad
  
Los clientes Windows 2000, Windows Server 2003 y Windows XP están configurados de forma predeterminada para enviar respuestas de autenticación LM y NTLM (los clientes Windows 9x sólo envían LM). El valor predeterminado de los servidores permite a todos los clientes autenticarse en los servidores y utilizar sus recursos. Sin embargo, esto significa que las respuestas LM (la forma de respuesta de autenticación menos segura) se envían a través de la red y los atacantes pueden rastrear ese tráfico para reproducir la contraseña del usuario con mayor facilidad.
  
Los sistemas operativos Windows 9x y Windows NT no utilizan el protocolo de la versión 5 de Kerberos para la autenticación, de manera que, en un dominio de Windows Server 2003, estos equipos utilizan una autenticación con los protocolos LM y NTLM de forma predeterminada para la autenticación de red. Puede aplicar un protocolo de autenticación más seguro para Windows 9x y Windows NT con el uso de NTLMv2. En el proceso de inicio de sesión, NTLMv2 utiliza un canal seguro para proteger el proceso de autenticación. Incluso si utiliza NTLMv2 para clientes y servidores heredados, los clientes y servidores basados en Windows que son miembros del dominio utilizarán el protocolo de autenticación Kerberos para autenticarse con controladores de dominio de Windows Server 2003.
  
Para obtener más información acerca de la autenticación NTLMv2, consulte el artículo de Microsoft Knowledge Base "[How to enable NTLM 2 authentication](http://support.microsoft.com/default.aspx?scid=239869)" en http://support.microsoft.com/?scid=239869. Microsoft Windows NT 4.0 requiere que Service Pack 4 (SP4) sea compatible con NTLMv2, mientras que las plataformas de Windows 9x deben tener los clientes del servicio de directorio instalados para ser compatibles con NTLMv2.
  
##### Contramedida
  
Configure **Seguridad de red: nivel de autenticación de LAN Manager** en **Enviar sólo respuesta NTLMv2.** Microsoft y otras organizaciones independientes recomiendan este nivel de autenticación cuando todos los clientes son compatibles con NTLMv2.
  
##### Impacto potencial
  
Los clientes que no son compatibles con la autenticación NTLMv2 no se podrán autenticar en el dominio y obtener acceso a los recursos del dominio con LM y NTLM.
  
**Nota**: para obtener información sobre una revisión para garantizar que este valor funcione en redes que incluyan equipos con Windows NT 4.0 junto con equipos con Windows 2000, Windows XP y Windows Server 2003, consulte el artículo de Microsoft Knowledge Base "[Authentication Problems in Windows 2000 with NTLM 2 Levels Above 2 in a Windows NT 4.0 Domain](http://support.microsoft.com/default.aspx?scid=305379)" en http://support.microsoft.com/default.aspx?scid=305379.
  
#### Seguridad de red: requisitos de firma de cliente LDAP
  
Esta configuración de directiva determina el nivel de firma de datos que se solicita en nombre de los clientes que emiten solicitudes BIND de LDAP, de la siguiente manera:
  
-   **Ninguno**. La solicitud LDAP BIND se emite con opciones que el llamador especifica.
  
-   **Negociar firma**. Si la Seguridad de la capa de transporte/Nivel de sockets seguros (TLS/SSL) no se ha iniciado, la solicitud LDAP BIND se iniciará con la opción de firma de datos LDAP establecida, además de con las opciones que el llamador haya especificado. En caso de que TLS/SSL se haya iniciado, la solicitud LDAP BIND se iniciará con las opciones especificadas por el llamador.
  
-   **Requerir firma**. Este nivel es el mismo que **Negociar firma**, si bien se informa al llamador de que se produjo un error en la solicitud de comando LDAP BIND cuando la respuesta saslBindInProgress intermedia del servidor LDAP no indique que se requiere la firma de tráfico LDAP.
  
**Nota**: esta configuración de directiva no tiene ninguna repercusión en ldap\_simple\_bind o ldap\_simple\_bind\_s. Ningún cliente de Microsoft LDAP incluido en Windows XP Professional utiliza ldap\_simple\_bind o ldap\_simple\_bind\_s para comunicarse con un controlador de dominio.
  
Los valores posibles para la configuración **Seguridad de red: requisitos de firma de cliente LDAP** son:
  
-   Ninguno
  
-   Negociar firma
  
-   Requerir firma
  
-   No está definido
  
##### Vulnerabilidad
  
El tráfico de red no firmado es susceptible de recibir ataques de intermediario en los que el intruso captura paquetes entre el servidor y el cliente y los modifica antes de reenviarlos al servidor. Para un servidor LDAP, esta susceptibilidad significa que un atacante podría hacer que un servidor tome decisiones basadas en datos falsos o alterados a partir de las consultas LDAP. Para reducir el riesgo en su red, puede poner en práctica medidas eficaces de seguridad física para proteger la infraestructura de la red. Además, realizar cualquier tipo de ataque de intermediario resultará una tarea extremadamente difícil si exige firmas digitales en todos los paquetes de red a través de encabezados de autenticación IPsec.
  
##### Contramedida
  
Configure **Seguridad de red: requisitos de firma de servidor LDAP** en **Requerir firma**.
  
##### Impacto potencial
  
Si establece que el servidor solicite firmas LDAP, deberá hacer lo propio con el cliente. Si no configura el cliente, no será capaz de comunicarse con el servidor, lo que podría causar errores en muchas características, incluidas la autenticación de usuario, la directiva de grupo y las secuencias de comandos de inicio de sesión.
  
#### Seguridad de red: seguridad mínima de sesión para clientes basados en NTLM SSP (incluyendo RPC seguro)
  
Esta configuración de directiva permite a un equipo cliente requerir la negociación de confidencialidad de mensaje (cifrado), integridad de mensaje, cifrado de 128 bits o seguridad de sesión de NTLMv2. Estos valores dependen del valor de la configuración de directiva del **nivel de autenticación de LAN Manager**.
  
Los valores posibles para la configuración **Seguridad de red: seguridad mínima de sesión para clientes basados en NTLM SSP (incluyendo RPC seguro)** son:
  
-   **Necesita confidencialidad de mensaje**. La conexión dará error si el cifrado no se ha negociado. El cifrado convierte los datos en una forma que impide leerlos hasta que se descifren.
  
-   **Necesita integridad de mensaje**. La conexión dará error si la integridad del mensaje no se ha negociado. La integridad de un mensaje se puede evaluar a través de la firma del mensaje. La firma del mensaje demuestra que el mensaje no se ha alterado; adjunta una firma cifrada que identifica al remitente y que consiste en una representación numérica del contenido del mensaje.
  
-   **Necesita cifrado de 128 bits**. La conexión no podrá establecerse si el cifrado de alta seguridad (128 bits) no se negocia.
  
-   **Necesita seguridad de sesión NTLMv2**. La conexión dará error si el protocolo NTLMv2 no se ha negociado.
  
-   **No está definido**.
  
##### Vulnerabilidad
  
Puede habilitar todas las opciones para esta configuración de directiva para proteger el tráfico de red que utiliza el Proveedor de compatibilidad con seguridad LM de Windows NT (NTLM SSP) para evitar que quede expuesto o que un atacante que haya obtenido acceso a la misma red lo altere. Es decir, estas opciones ayudan a proteger contra ataques de intermediario.
  
##### Contramedida
  
Habilite las cuatro opciones disponibles para la directiva **Seguridad de red: seguridad mínima de sesión para clientes basados en NTLM SSP (incluyendo RPC seguro)**.
  
##### Impacto potencial
  
Los equipos cliente que implanten estos valores no podrán comunicarse con servidores anteriores con los que no sean compatibles.
  
#### Seguridad de red: seguridad mínima de sesión para servidores basados en NTLM SSP (incluyendo RPC seguro)
  
Esta configuración de directiva permite a un servidor requerir la negociación de confidencialidad de mensaje (cifrado), integridad de mensaje, cifrado de 128 bits o seguridad de sesión de NTLMv2. Estos valores dependen del valor de la opción de seguridad del **nivel de autenticación de LAN Manager**.
  
Los valores posibles para la configuración **Seguridad de red: seguridad mínima de sesión para servidores basados en NTLM SSP (incluyendo RPC seguro)** son:
  
-   **Necesita confidencialidad de mensaje**. La conexión dará error si el cifrado no se ha negociado. El cifrado convierte los datos en una forma que impide que leerlos hasta que se descifren.
  
-   **Necesita integridad de mensaje**. La conexión dará error si la integridad del mensaje no se ha negociado. La integridad de un mensaje se puede evaluar a través de la firma del mensaje. La firma del mensaje demuestra que el mensaje no se ha alterado; adjunta una firma cifrada que identifica al remitente y que consiste en una representación numérica del contenido del mensaje.
  
-   **Necesita cifrado de 128 bits**. La conexión no podrá establecerse si el cifrado de alta seguridad (128 bits) no se negocia.
  
-   **Necesita seguridad de sesión NTLMv2**. La conexión dará error si el protocolo NTLMv2 no se ha negociado.
  
-   **No está definido**.
  
##### Vulnerabilidad
  
Puede habilitar todas las opciones para esta configuración de directiva para proteger el tráfico de red que utiliza el Proveedor de compatibilidad con seguridad LM de Windows NT (NTLM SSP) para evitar que quede expuesto o que un atacante que haya obtenido acceso a la misma red lo altere. Es decir, estas opciones sirven de protección frente a ataques de intermediario.
  
##### Contramedida
  
Habilite las cuatro opciones disponibles para la directiva **Seguridad de red: seguridad mínima de sesión para servidores basados en NTLM SSP (incluyendo RPC seguro)**.
  
##### Impacto potencial
  
Los clientes anteriores que no admitan estos valores de seguridad no podrán comunicarse con el equipo.
  
#### Consola de recuperación: permitir el inicio de sesión administrativo automático
  
Esta configuración de directiva determina si la contraseña de la cuenta Administrador debe proporcionarse antes de obtener acceso al equipo. Si habilita este parámetro, la cuenta de Administrador inicia sesión automáticamente en el equipo de la consola de recuperación; no se requiere contraseña.
  
Los valores posibles para la configuración **Consola de recuperación: permitir el inicio de sesión administrativo automático** son:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Vulnerabilidad
  
La consola de recuperación puede ser muy útil al realizar tareas de solución de problemas y de reparación en equipos que no se pueden iniciar. Sin embargo, es peligroso permitir el inicio de sesión automático en la consola. Cualquiera que tenga acceso físico al servidor puede desconectar la alimentación de corriente para apagarlo, y luego reiniciarlo, seleccionar **Consola de recuperación** del menú **Reiniciar** y tomar pleno control del servidor.
  
##### Contramedida
  
Configure **Consola de recuperación: permitir el inicio de sesión administrativo automático** como **Deshabilitado**.
  
##### Impacto potencial
  
Los usuarios deberán escribir un nombre de usuario y una contraseña para obtener acceso a la cuenta de la consola de recuperación.
  
#### Consola de recuperación: permitir la copia de disquetes y el acceso a todas las unidades y carpetas
  
Puede habilitar esta configuración de directiva para hacer que el comando SET de la consola de recuperación esté disponible, lo que permite establecer las siguientes variables de entorno en la consola de recuperación.
  
-   **AllowWildCards**. habilita la compatibilidad con comodines para algunos comandos (como el comando DEL).
  
-   **AllowAllPaths**. permite el acceso a todos los archivos y carpetas del equipo.
  
-   **AllowRemovableMedia**. permite la copia de archivos en medios extraíbles, como un disquete.
  
-   **NoCopyPrompt**. Suprime el aviso que se muestra normalmente antes de sobrescribir un archivo existente.
  
Los valores posibles para la configuración **Consola de recuperación: permitir la copia de disquetes y el acceso a todas las unidades y carpetas** son:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Vulnerabilidad
  
Un atacante que puede hacer que el sistema se reinicie en la consola de recuperación podría robar datos confidenciales sin dejar rastro ni registro de auditoría.
  
##### Contramedida
  
Configure **Consola de recuperación: permitir la copia de disquetes y el acceso a todas las unidades y carpetas** como **Deshabilitado**.
  
##### Impacto potencial
  
Los usuarios que hayan iniciado un servidor a través de la consola de recuperación y, al mismo tiempo, hayan iniciado sesión con la cuenta integrada Administrador no podrán copiar archivos ni carpetas en un disquete.
  
#### Apagado: permitir apagar el sistema sin tener que iniciar sesión
  
Esta configuración de directiva determina si un equipo se puede apagar sin tener que iniciar sesión en Windows. Si habilita esta configuración de directiva, el comando **Apagar** estará disponible en la pantalla de inicio de sesión de Windows. Si deshabilita esta configuración de directiva, la opción **Apagar** se elimina de la pantalla de inicio de sesión de Windows. Esta configuración requiere que los usuarios puedan iniciar sesión en el equipo con éxito y, además, tener asignado el derecho de usuario **Apagar el sistema** antes de que puedan apagar el equipo.
  
Los valores posibles para la configuración **Apagado: permitir apagar el sistema sin tener que iniciar sesión** son:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Vulnerabilidad
  
Los usuarios que tienen acceso a la consola localmente pueden apagar el equipo.
  
Los atacantes podrían obtener acceso a la consola local y reiniciar el servidor, lo que causaría una condición temporal de DoS. Los atacantes podrían apagar también el servidor y todas las aplicaciones y servicios dejarían de estar disponibles.
  
##### Contramedida
  
Configure **Permitir apagar el sistema sin tener que iniciar sesión** como **Deshabilitado**.
  
##### Impacto potencial
  
Los operadores deberán iniciar sesión en los servidores para apagarlos o reiniciarlos.
  
#### Apagado: borrar el archivo de paginación de la memoria virtual
  
Esta configuración de directiva determina si el archivo de paginación de la memoria virtual debe borrarse cuando se apaga el equipo. El soporte de la memoria virtual usa un archivo de paginación del sistema para intercambiar páginas de memoria al disco cuando éstas no se utilizan. En un equipo en ejecución, el sistema operativo es el único que puede abrir este archivo de paginación, que se encuentra bien protegido. Sin embargo, es posible que los equipos configurados para permitir el inicio de otros sistemas operativos deban asegurarse de que el archivo de paginación del sistema se borre cuando el equipo se apaga. Esta confirmación garantiza que la información confidencial de la memoria de procesos que pueda incluirse en el archivo de paginación no esté disponible para ningún usuario no autorizado que logre tener acceso directo al archivo de paginación después del apagado.
  
Cuando habilita esta configuración de directiva, el archivo de paginación del sistema se borra cuando el equipo se apaga. Además, esta configuración de directiva hará que el equipo borre el archivo de hibernación Hiberfil.sys cuando se deshabilita la hibernación en un equipo portátil.
  
Los valores posibles para la configuración **Apagado: borrar el archivo de paginación de la memoria virtual** son:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Vulnerabilidad
  
La información importante guardada en la memoria real se puede escribir periódicamente en el archivo de paginación para ayudar a que Windows Server 2003 controle las funciones multitarea. Un atacante con acceso físico a un servidor que se haya apagado podría ver el contenido del archivo de paginación, de manera que podría mover el volumen del sistema a un equipo distinto y analizar el contenido del archivo de paginación. Aunque este proceso es muy laborioso, podría exponer los datos almacenados en caché desde la memoria de acceso aleatorio (RAM) en el archivo de paginación.
  
**Precaución**: un atacante que tenga acceso físico al servidor podría pasar por alto esta contramedida tan sólo con desconectar la alimentación de corriente del servidor.
  
##### Contramedida
  
Configure **Borrar el archivo de paginación de la memoria virtual al apagar el sistema** como **Habilitado**. Esta configuración hace que Windows Server 2003 borre el archivo de paginación cuando el sistema se cierre, de modo que se eliminará toda la información almacenada en este archivo. La cantidad de tiempo que se requiere para completar este proceso depende del tamaño del archivo de paginación. Podrían pasar varios minutos antes de que el equipo se apague completamente.
  
##### Impacto potencial
  
Apagar y reiniciar el servidor llevará más tiempo, especialmente en los servidores que tengan archivos de paginación más grandes. En el caso de un servidor de 2 gigabytes (GB) de memoria RAM y un archivo de paginación de 2 GB, esta configuración de directiva podría alargar el proceso de apagado en 20 o 30 minutos, o incluso más. Para algunas empresas, este tiempo de desconexión infringe sus acuerdos de nivel de servicio interno. En consecuencia, tenga cuidado al implementar esta contramedida en el entorno.
  
#### Criptografía de sistema: establece una protección fuerte de clave para las aquellas claves del usuario en el equipo
  
Esta configuración de directiva determina si los usuarios pueden utilizar claves privadas, como la clave S/MIME, sin contraseña.
  
Los valores posibles para la configuración **Criptografía de sistema: establece una protección fuerte de clave para las aquellas claves del usuario en el equipo** son:
  
-   No es necesaria la intervención del usuario al guardar y usar nuevas claves
  
-   Se preguntará al usuario cuando se use la clave por primera vez
  
-   El usuario debe introducir una contraseña cada vez que use una clave
  
-   No está definido
  
##### Vulnerabilidad
  
Puede configurar esta configuración de directiva para que los usuarios proporcionen una contraseña distinta de su contraseña de dominio cada vez que utilicen una clave. Esta configuración hace más difícil que un atacante tenga acceso a claves de usuario almacenadas localmente, incluso si éste toma el control del equipo del usuario y determina la contraseña de inicio de sesión.
  
##### Contramedida
  
Configure **Criptografía de sistema: establece una protección fuerte de clave para las claves del usuario en el equipo** en **El usuario debe introducir una contraseña cada vez que use una clave**.
  
##### Impacto potencial
  
Los usuarios deberán escribir su contraseña cada vez que tengan acceso a una clave almacenada en el equipo. Por ejemplo, si los usuarios utilizan un certificado S-MIME para firmar digitalmente un mensaje, deberán escribir la contraseña para ese certificado cada vez que envíen un mensaje de correo electrónico firmado. Para algunas empresas, la carga que supone usar esta configuración puede resultar demasiado alta. Como mínimo, este parámetro debe configurarse en **Preguntar al usuario cuando se usa la clave por primera vez.**
  
#### Criptografía de sistema: usar algoritmos que cumplan la norma FIPS para cifrado, firma y operaciones hash
  
Esta configuración de directiva determina si el proveedor de seguridad TLS/SSL sólo admitirá el conjunto cifrado denominado TLS\_RSA\_WITH\_3DES\_EDE\_CBC\_SHA, lo que significa que el proveedor sólo admite el protocolo TLS como un cliente y como un servidor, de ser aplicable. Sólo utiliza el algoritmo de cifrado Triple Data Encryption Standard (DES) para el cifrado del tráfico de TLS; sólo el algoritmo de clave pública Rivest-Shamir-Adleman (RSA) para el intercambio de claves y la autenticación de TLS, y sólo el algoritmo hash Secure Hash Algorithm versión 1 (SHA-1) para los requisitos de operaciones hash de TLS.
  
Cuando se habilita este parámetro, el sistema de archivos de cifrado (EFS) sólo admite el algoritmo de cifrado Triple DES para cifrar los datos de archivo. De forma predeterminada, la implementación de Windows Server 2003 de EFS utiliza el estándar avanzado de cifrado (AES) con una clave de 256 bits. La implementación de Windows XP utiliza DESX.
  
Los valores posibles para la configuración **Criptografía de sistema: usar algoritmos que cumplan la norma FIPS para cifrado, firma y operaciones hash** son:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Vulnerabilidad
  
Puede habilitar esta directiva para garantizar que el equipo va a usar los algoritmos más eficaces que existen para el cifrado digital, la firma y las operaciones hash. El uso de estos algoritmos minimizará el riesgo de que un usuario no autorizado ponga en peligro los datos cifrados o firmados.
  
##### Contramedida
  
Configure **Criptografía de sistema: usar algoritmos que cumplan la norma FIPS para cifrado, firma y operaciones hash** como **Habilitado**.
  
##### Impacto potencial
  
Los equipos cliente que tienen esta configuración de directiva habilitada no podrán comunicarse con los servidores que no admiten estos algoritmos a través de protocolos cifrados o firmados digitalmente. Los clientes de red que no admiten estos algoritmos no podrán utilizar los servidores que los requieran para las comunicaciones de red. Por ejemplo, muchos servidores web basados en Apache no están configurados para admitir TLS. Si habilita esta configuración, también deberá configurar Internet Explorer para que utilice TLS. Esta configuración de directiva afecta también el nivel de cifrado que se utiliza para el Protocolo de escritorio remoto (RDP). La herramienta de Conexión a escritorio remoto utiliza el protocolo RDP para comunicarse con servidores en los que se ejecutan Servicios de Terminal Server y equipos cliente que se configuran para control remoto; las conexiones RDP fallarán si ambos equipos no se configuran para utilizar los mismos algoritmos de cifrado.
  
**Para habilitar Internet Explorer para que utilice TLS**
  
1.  En el menú de Internet Explorer **Herramientas**, abra el cuadro de diálogo **Opciones de Internet**.
  
2.  Haga clic en la ficha **Avanzadas**.
  
3.  Active la casilla de verificación **Usar TLS 1.0**.
  
Asimismo, se puede establecer esta configuración de directiva mediante la directiva de grupo o con el kit de administración de Internet Explorer.
  
#### Objetos de sistema: propietario predeterminado para objetos creados por miembros del grupo de administradores
  
Esta configuración de directiva determina si el grupo de **administradores** o un creador de objetos es el propietario predeterminado de cualquier objeto de sistema que se haya creado.
  
Los valores posibles para la configuración **Objetos de sistema: propietario predeterminado para objetos creados por miembros del grupo de administradores** son:
  
-   Grupo Administradores
  
-   Creador de objetos
  
-   No está definido
  
##### Vulnerabilidad
  
Si establece esta configuración de directiva en el **grupo** de **Administradores**, será imposible que se responsabilice a las personas por crear objetos de sistema nuevos.
  
##### Contramedida
  
Configure **Objetos de sistema: propietario predeterminado para objetos creados por miembros del grupo de administradores** en **Creador de objetos**.
  
##### Impacto potencial
  
Cuando se crean objetos de sistema, la propiedad de los mismos reflejará la cuenta que los ha creado en lugar del grupo genérico **Administradores**. Una consecuencia de esta configuración de directiva es que los objetos pasan a ser "huérfanos" cuando se borran las cuentas de usuario. Por ejemplo, cuando un miembro del grupo de informática deja de trabajar en la empresa, cualquier objeto que haya creado en el dominio carecerá de propietario. Esta situación podría pasar a ser una carga administrativa, ya que los administradores tendrán que asumir manualmente la propiedad de los objetos huérfanos para actualizar sus permisos. Esta carga potencial se puede minimizar si se asegura de que **Control total** esté siempre asignado a objetos nuevos para un grupo del dominio como **Administraciones del dominio**.
  
#### Objetos de sistema: requerir diferenciación de mayúsculas y minúsculas para subsistemas no basados en Windows
  
Esta configuración de directiva determina si se implanta la no distinción de mayúsculas y minúsculas en todos los subsistemas. El subsistema Microsoft Win32® hace distinción de mayúsculas y minúsculas, si bien el núcleo admite la distinción de mayúsculas y minúsculas para otros subsistemas, como la Interfaz de sistema operativo portátil de UNIX (POSIX). Si habilita este parámetro, se aplicará la diferenciación de mayúsculas y minúsculas para todos los objetos del directorio, vínculos simbólicos y objetos IO y de archivo. Si deshabilita este parámetro, el subsistema Win32 no hará distinción de mayúsculas y minúsculas.
  
Los valores posibles para la configuración **Objetos de sistema: requerir diferenciación de mayúsculas y minúsculas para subsistemas no basados en Windows** son:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Vulnerabilidad
  
Dado que Windows no hace distinción entre mayúsculas y minúsculas, pero el subsistema POSIX sí, no aplicar esta configuración de directiva haría posible que un usuario de ese subsistema creara un archivo con el mismo nombre que otro archivo, pero utilizando una combinación de mayúsculas y minúsculas en el nombre. A la larga, esto podría confundir a los usuarios cuando intentaran obtener acceso a estos archivos con herramientas normales de Win32, porque sólo estaría disponible uno de esos archivos.
  
##### Contramedida
  
Configure **Objetos de sistema: requerir diferenciación de mayúsculas y minúsculas para subsistemas no basados en Windows** como **Habilitado**.
  
##### Impacto potencial
  
Todos los subsistemas estarán obligados a diferenciar entre mayúsculas y minúsculas. Esta configuración puede confundir a los usuarios que estén acostumbrados a uno de los sistemas operativos basados en UNIX, donde se distingue entre mayúsculas y minúsculas.
  
#### Objetos de sistema: reforzar los permisos predeterminados de los objetos internos del sistema (p. ej. vínculos simbólicos)
  
Con esta configuración de directiva se determina la seguridad de la lista de control de acceso discrecional predeterminada para objetos. Windows mantiene una lista global de recursos compartidos del equipo (como nombres de dispositivos MS-DOS, exclusiones mutuas y semáforos) para localizar y compartir los objetos en los procesos.
  
Los valores posibles para la configuración **Objetos de sistema: reforzar los permisos predeterminados de los objetos internos del sistema (p. ej. vínculos simbólicos)** son:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Vulnerabilidad
  
Con este valor se determina la seguridad de la lista de control de acceso discrecional predeterminada para objetos. Windows Server 2003 mantiene una lista global de recursos compartidos del equipo para localizar y compartir los objetos en los procesos. Cada tipo de objeto se crea con una lista de control de acceso discrecional predeterminada que especifica quién puede tener acceso a los objetos y con qué permisos. Si habilita este parámetro, la DACL predeterminada es más segura porque permite a los usuarios no administrativos leer objetos compartidos, pero no permite modificar objetos compartidos que no hayan creado.
  
##### Contramedida
  
Configure **Objetos de sistema: reforzar los permisos predeterminados de los objetos internos del sistema (p. ej. vínculos simbólicos**) como **Habilitado**.
  
##### Impacto potencial
  
Ninguno. Ésta es la configuración predeterminada.
  
#### Configuración del sistema: Subsistemas opcionales
  
Esta configuración de directiva determina los subsistemas que son compatibles con las aplicaciones disponibles. Puede usar esta configuración de seguridad para especificar tantos subsistemas como el entorno solicite.
  
Los valores posibles para la configuración **Configuración del sistema: subsistemas opcionales** son:
  
-   Una lista de subsistemas definida por el usuario
  
-   No está definido
  
##### Vulnerabilidad
  
El subsistema POSIX es una norma del IEEE (Instituto de ingenieros eléctricos y electrónicos)que define un conjunto de servicios de sistemas operativos. El subsistema POSIX es necesario cuando el servidor admite aplicaciones que utilizan este subsistema en cuestión.
  
El subsistema POSIX implica un riesgo de seguridad relacionado con los procesos que pueden persistir a lo largo de los inicios de sesión. Si un usuario inicia un proceso y luego cierra la sesión, existe un riesgo potencial de que el siguiente usuario que inicie sesión en el equipo tenga acceso al proceso del usuario anterior. Este potencial es peligroso, porque todo lo que el segundo usuario haga con ese proceso se realizará con los privilegios del primer usuario.
  
##### Contramedida
  
Configure **Configuración del sistema: Subsistemas opcionales** con un valor nulo. El valor predeterminado es **POSIX**.
  
##### Impacto potencial
  
Las aplicaciones que dependen del subsistema POSIX dejarán de funcionar. Por ejemplo, los servicios de Microsoft para Unix (SFU) instalan una versión actualizada del subsistema POSIX que se necesita, de manera que tendría que volver a configurar este parámetro en una directiva de grupo para cualquier servidor que utilice SFU.
  
#### Configuración del sistema: usar reglas de certificado en archivos ejecutables de Windows para directivas de restricción de software
  
Esta configuración de directiva determina si se procesarán los certificados digitales cuando existen directivas de restricción de software y un usuario o un proceso intentan ejecutar software con una extensión de archivo .exe. Este valor de configuración de seguridad habilita o deshabilita las reglas de certificado (una clase de regla de directivas de restricción de software). Con las directivas de restricción de software, se puede crear una regla de certificado que permita o impida que se ejecute el software firmado por Microsoft Authenticode®, según el certificado digital asociado al software. Para que funcionen las reglas de certificado cuando hay directivas de restricción de software, debe habilitar esta configuración de seguridad.
  
Los valores posibles para la configuración **Configuración del sistema: usar reglas de certificado en archivos ejecutables de Windows para directivas de restricción de software** son:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Vulnerabilidad
  
Las directivas de restricción de software ayudan a proteger a los usuarios y equipos porque pueden evitar la ejecución de códigos no autorizados como virus y troyanos.
  
##### Contramedida
  
Configure **Configuración del sistema: usar reglas de certificado en archivos ejecutables de Windows para directivas de restricción de software** como **Habilitado**.
  
##### Impacto potencial
  
Si habilita reglas de certificado, las directivas de restricción de software comprobarán una lista de revocación de certificados (CRL) para asegurarse de que el certificado y la firma del software son válidos. Este proceso de comprobación puede afectar negativamente al rendimiento cuando los programas firmados se inician. Esta característica se puede deshabilitar si modifica las directivas de restricción de software en el GPO deseado. En el cuadro de diálogo **Propiedades de Editores de confianza**, desactive las casillas de verificación **Editor** y **Marca de hora**.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de las opciones de seguridad en Windows Server 2003 y Windows XP.
  
-   Para obtener más información acerca de las restricciones predeterminadas de acceso del equipo COM en Windows XP, consulte la guía "[Managing Windows XP Service Pack 2 Features Using Group Policy: Security-Related Policy Settings](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/mangxpsp2/mngsecps.mspx)" en www.microsoft.com/technet/prodtechnol/winxppro/maintain/mangxpsp2/mngsecps.mspx.
  
-   Para obtener información acerca de las restricciones predeterminadas de acceso COM en Windows Server 2003 con SP1, consulte la sección "Mejoras de seguridad DCOM" de la guía "[Cambios de la funcionalidad de Microsoft Windows Server 2003 Service Pack 1](http://technet.microsoft.com/es-es/library/cc738214.aspx)" en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/BookofSP1/.
  
-   Para obtener más información acerca de cómo habilitar NTLMv2, consulte el artículo de Microsoft Knowledge Base "[Cómo habilitar la autenticación NTLM 2](http://support.microsoft.com/default.aspx?scid=239869)" en http://support.microsoft.com/default.aspx?scid=239869.
  
-   Para obtener más información acerca de cómo garantizar que las configuraciones del nivel de autenticación de LAN Manager más seguras funcionen en redes con una mezcla de equipos con Windows 2000 y Windows NT® 4.0, consulte el artículo de Microsoft Knowledge Base "[Problemas de autenticación en Windows 2000 con niveles de NTLM 2 por encima de 2 en un dominio de Windows NT 4.0](http://support.microsoft.com/?scid=305379)" en http://support.microsoft.com/?scid=305379.
  
-   Para obtener más información acerca de los niveles de compatibilidad de LAN Manager, consulte el artículo de Microsoft Knowledge Base "[Incompatibilidades de clientes, servicios y programas que pueden darse al modificar la configuración de seguridad y las asignaciones de derechos de usuario](http://support.microsoft.com/?scid=823659)" en http://support.microsoft.com/?scid=823659.
  
-   Para obtener más información acerca de la autenticación NTLMv2, consulte el artículo de Microsoft Knowledge Base "[Cómo habilitar la autenticación NTLM 2](http://support.microsoft.com/?scid=239869)" en http://support.microsoft.com/?scid=239869.
  
-   Para obtener más información acerca de cómo restaurar la configuración de seguridad predeterminada de forma local, consulte el artículo de Microsoft Knowledge Base "[Cómo devolver la configuración de seguridad a los valores predeterminados](http://support.microsoft.com/?scid=313222)” en http://support.microsoft.com/?scid=313222.
  
-   Para obtener más información acerca de cómo restaurar la configuración de seguridad predeterminada en los objetos de directiva de grupo del domino integrados, consulte el artículo de Microsoft Knowledge Base "[Cómo restablecer derechos de usuario en la directiva de grupo del dominio predeterminada en Windows Server 2003](http://support.microsoft.com/?scid=324800)" en http://support.microsoft.com/?scid=324800.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 6: Registro de eventos
  
El registro de eventos realiza un seguimiento de los eventos en el equipo, y el registro de seguridad realiza un seguimiento de los eventos de auditoría. El contenedor del registro de eventos de la directiva de grupo se utiliza para definir los atributos relacionados con la aplicación, la seguridad y los registros de eventos del sistema como, por ejemplo, el tamaño máximo del registro, los derechos de acceso para los registros, así como la configuración y los métodos de retención. El libro de Microsoft® Excel® "Configuración de la seguridad y los servicios predeterminados de Windows", que se incluye con esta guía, documenta la configuración predeterminada del registro de eventos.
  
[](#eaza)[Configuración del registro de eventos](#eaza)  
[](#eexa)[Información adicional](#eexa)
  
### Configuración del registro de eventos
  
Puede establecer la configuración del registro de eventos en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Registro de eventos\\Configuración para registros de eventos**
  
#### Tamaño máximo del registro de eventos
  
Esta configuración de directiva especifica el tamaño máximo de los registros de eventos de aplicación, seguridad y sistema. Aunque las interfaces de usuario del Editor de objetos de directiva de grupo y del complemento Visor de eventos de Microsoft Management Console (MMC) permiten escribir valores de hasta cuatro gigabytes, ciertos factores hacen que el tamaño máximo eficaz de estos registros sea mucho menor.
  
El servicio de **registro de eventos** utiliza archivos asignados en memoria y se ejecuta como uno de los servicios del proceso services.exe como eventlog.dll. Cuando los archivos se cargan de esta forma, todo el archivo se carga en la memoria del sistema. Todas las versiones actuales de Microsoft Windows tienen una limitación arquitectónica relacionada con los archivos asignados en memoria: ningún proceso puede tener más de un gigabyte de archivos asignados en memoria en total. Esta limitación significa que todos los servicios que se ejecutan en el proceso services.exe deben compartir el grupo de un gigabyte. La memoria se asigna en partes contiguas de 64 KB, y si el equipo no puede asignar memoria adicional para expandir archivos asignados en memoria, surgen problemas.
  
Para el servicio del **registro de eventos**, el uso de archivos asignados en memoria implica que independientemente de la cantidad de memoria que especifique el parámetro **Tamaño máximo del registro de eventos**, los registros de eventos no podrán introducirse en el registro cuando el equipo no tenga más memoria disponible para el archivo asignado en memoria. No aparecerán mensajes de error; sencillamente los eventos no aparecerán en el registro de eventos o podrán sobrescribir otros eventos que se hayan registrado anteriormente. La fragmentación de archivos de registro en la memoria también ha demostrado que provoca problemas de rendimiento importantes en equipos ocupados.
  
Debido a estas limitaciones, a pesar de que el límite teórico para los archivos asignados en memoria sugiere lo contrario y las interfaces de usuario del Visor de eventos y del Editor de objetos de directiva de grupo permiten especificar hasta cuatro gigabytes por registro, Microsoft ha comprobado que el límite práctico está alrededor de los 300 MB en la mayoría de los servidores, es decir, 300 MB para *todos los registros de eventos combinados*. En Microsoft Windows XP, servidores miembros y servidores independientes el tamaño combinado de los registros de eventos de aplicación, seguridad y sistema no debería superar los 300 MB. En los controladores de dominio, el tamaño combinado de estos tres archivos, más el servicio de directorio de Active Directory®, el DNS y los registros de replicación no deben superar los 300 MB.
  
Estas limitaciones han causado problemas a algunos clientes de Microsoft, pero la única manera de eliminar las limitaciones implica cambios fundamentales en la forma en que se registran los eventos. Microsoft está reprogramando el sistema del registro de eventos para resolver estos problemas en la siguiente versión de Windows.
  
Aunque no existe ninguna ecuación sencilla para determinar el tamaño de registro óptimo para un servidor concreto, se puede calcular un tamaño razonable. El promedio de una entrada de evento requiere alrededor de 500 bytes en cada registro y los tamaños de archivo de registro deben ser múltiplos de 64 KB. Si puede calcular el número medio de eventos que se generan cada día para cada tipo de registro en su organización, puede determinar un tamaño adecuado para cada tipo de archivo de registro.
  
Por ejemplo, si su servidor de archivos genera 5.000 eventos al día en su registro de seguridad y desea garantizar que dispone de al menos 4 semanas de datos en todo momento, entonces deberá establecer el tamaño de este registro en aproximadamente 70 MB. (500 bytes \* 5000 eventos/día \* 28 días = 70 millones de bytes). Compruebe los servidores de forma ocasional en las siguientes cuatro semanas para comprobar sus cálculos y que los registros almacenan un número apropiado de eventos. Se deben definir el tamaño y el ajuste del registro de eventos de modo que cumplan los requisitos empresariales y de seguridad que determinó al diseñar el plan de seguridad de la empresa.
  
Los valores posibles para la configuración **Tamaño máximo del registro de eventos** son:
  
-   Un número de kilobytes especificado por el usuario entre 64 y 4.194.240. Sin embargo, debe ser un múltiplo de 64.
  
##### Vulnerabilidad
  
Si aumenta de forma significativa el número de objetos que se auditan en la empresa, existe el riesgo de que el registro de seguridad alcance su capacidad máxima, lo que obliga al equipo a apagarse si habilitó el parámetro **Auditoría: apagar el sistema de inmediato si no puede registrar auditorías de seguridad**. Si se produce un cierre, el equipo no se podrá utilizar hasta que un administrador borre el registro de seguridad. Para evitarlo, puede deshabilitar el parámetro **Auditoría: apagar el sistema de inmediato si no puede registrar auditorías de seguridad**, que se describe en el capítulo 5 "Opciones de seguridad", y aumentar el tamaño del registro de seguridad. Alternativamente, puede configurar la rotación con registro automático que se describe en el artículo de Microsoft Knowledge Base "[The event log stops logging events before reaching the maximum log size](http://support.microsoft.com/default.aspx?kbid=312571)" en http://support.microsoft.com/default.aspx?kbid=312571.
  
##### Contramedida
  
Debe activar directivas de tamaño de registro razonables en todos los equipos de su empresa para que los usuarios legítimos puedan ser responsables de sus acciones, las actividades no autorizadas se puedan detectar y seguir y los problemas del equipo se puedan detectar y diagnosticar.
  
##### Impacto potencial
  
Cuando los registros de eventos alcanzan el máximo de su capacidad, dejan de registrar información, a menos que el método de retención de cada uno se establezca para que el equipo sobrescriba las entradas más antiguas con las más recientes. Para mitigar el riesgo de pérdida de datos recientes, puede configurar el método de retención para que los eventos más antiguos se borren según se necesite.
  
La consecuencia de esta configuración es que los eventos más antiguos se eliminarán de los registros. Los atacantes pueden aprovechar esta configuración, ya que pueden generar un gran número de eventos superfluos para sobrescribir cualquier indicio de su ataque. Estos riesgos se pueden reducir en parte si automatiza el almacenamiento y la copia de seguridad de los datos del registro de eventos.
  
Lo ideal es que todos los eventos supervisados de forma específica se envíen a un servidor que utilice Microsoft Operations Manager (MOM) o cualquier otra herramienta automatizada de supervisión. Esta configuración es especialmente importante porque un atacante que consiga poner en peligro un servidor podría borrar el registro de seguridad. Si todos los eventos se envían a un servidor de supervisión, podrá recopilar información de análisis sobre las actividades del atacante.
  
#### Evitar que el grupo de invitados locales tenga acceso a los registros de eventos
  
Esta configuración de directiva determina si los invitados pueden tener acceso a los registros de eventos de aplicación, seguridad y sistema.
  
Los valores posibles para la configuración **Evitar que el grupo de invitados locales tenga acceso a los registros de eventos** son:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
**Nota**: esta configuración de directiva no aparece en el objeto Directiva de equipo local.
  
Esta configuración de directiva sólo afecta a equipos con Windows 2000 y las versiones posteriores de Windows.
  
##### Vulnerabilidad
  
Un atacante que ha conseguido iniciar sesión en un equipo con privilegios de invitado puede obtener información importante sobre el equipo si puede consultar los registros de eventos. El atacante podría utilizar entonces esta información para realizar más ataques.
  
##### Contramedida
  
Habilite el parámetro **Evitar que el grupo de invitados locales tenga acceso a los registros de eventos** para las directivas de los tres registros de eventos.
  
##### Impacto potencial
  
Ninguno. Ésta es la configuración predeterminada.
  
#### Conservar registros de eventos
  
Esta configuración de directiva determina el número de días de datos del registro de eventos a retener para los registros de aplicación, seguridad y sistema si el método de retención que se especifica para el registro es **Por días.** Configure este parámetro sólo si el registro se archiva a intervalos programados y asegúrese de que el tamaño máximo del registro es lo suficientemente grande como para incluir el intervalo.
  
Los valores posibles para la configuración **Conservar registros de eventos** son:
  
-   Un número de días especificado por el usuario entre 1 y 365
  
-   No está definido
  
**Nota**: esta configuración de directiva no aparece en el objeto Directiva de equipo local.
  
Un usuario debe tener asignado el derecho de usuario **Administración del registro de seguridad y auditoría** para tener acceso al registro de seguridad.
  
##### Vulnerabilidad
  
Si archiva el registro a intervalos programados:
  
1.  Abra el cuadro de diálogo **Propiedades** para esta directiva.
  
2.  Especifique el número de días correspondiente en el parámetro **Conservar el registro de aplicaciones.**
  
3.  Seleccione **Sobrescribir eventos por días** para el método de retención del registro de eventos.
  
Asegúrese también de que el tamaño máximo de registro es lo suficientemente grande para acomodar el intervalo.
  
##### Contramedida
  
Configure el parámetro **Conservar registros de eventos** para las directivas de los tres registros de eventos en **No está definido**.
  
##### Impacto potencial
  
Ninguno. Ésta es la configuración predeterminada.
  
#### Método de retención del registro de eventos
  
Esta configuración de directiva determina el método de ajuste de los registros de eventos de aplicación, seguridad y sistema.
  
Si no quiere archivar el registro de aplicaciones:
  
1.  Abra el cuadro de diálogo **Propiedades** para esta directiva.
  
2.  Active la casilla de verificación **Definir esta configuración de directiva.**
  
3.  Haga clic en **Sobrescribir eventos cuando sea necesario**.
  
Si quiere archivar el registro a intervalos programados:
  
1.  Abra el cuadro de diálogo **Propiedades** para esta directiva.
  
2.  Active la casilla de verificación **Definir esta configuración de directiva.**
  
3.  Haga clic en **Sobrescribir eventos por días**.
  
4.  Especifique el número de días correspondiente en el parámetro **Conservar el registro de aplicaciones.** Asegúrese de que el tamaño máximo de registro es lo suficientemente grande para acomodar el intervalo.
  
Si debe retener todos los eventos en el registro:
  
1.  Abra el cuadro de diálogo **Propiedades** para esta directiva.
  
2.  Active la casilla de verificación **Definir esta configuración de directiva.**
  
3.  Haga clic en **No sobrescribir eventos (borrado manual del registro)**.
  
Esta opción requiere que el registro se borre de forma manual. En esta configuración, los eventos nuevos se desechan cuando se alcanza el tamaño máximo de registro.
  
Los valores posibles para la configuración **Método de retención del registro de eventos** son:
  
-   Sobrescribir eventos por días
  
-   Sobrescribir eventos cuando sea necesario
  
-   No sobrescribir eventos (borrado manual del registro)
  
-   No está definido
  
**Nota**: esta configuración de directiva no aparece en el objeto Directiva de equipo local.
  
##### Vulnerabilidad
  
Si aumenta de forma significativa el número de objetos que se auditan en la empresa, existe el riesgo de que el registro de seguridad alcance su capacidad máxima, lo que obliga al equipo a apagarse. Si se produce un cierre, el equipo no se podrá utilizar hasta que un administrador borre el registro de seguridad. Para evitarlo, puede deshabilitar el parámetro **Auditoría: apagar el sistema de inmediato si no puede registrar auditorías de seguridad**, que se describe en el capítulo 5 "Opciones de seguridad", y aumentar el tamaño del registro de seguridad.
  
Si establece el **método de retención del registro de eventos** en **Manualmente** o en **Sobrescribir eventos por días** es posible que los eventos recientes importantes no se registren o que ocurra un ataque DoS.
  
##### Contramedida
  
Configure el método de retención para los tres registros de eventos en la opción **Sobrescribir eventos cuando sea necesario**. Algunos recursos recomiendan configurar este parámetro en **Manual**; sin embargo, la carga administrativa que supone es demasiado grande para la mayoría de las organizaciones.
  
Lo ideal es que todos los eventos significativos se envíen a un servidor de supervisión utilizando MOM o cualquier otra herramienta automatizada de supervisión.
  
##### Impacto potencial
  
Cuando los registros de eventos alcanzan el máximo de su capacidad, dejan de registrar información, a menos que el método de retención se establezca para que el equipo pueda sobrescribir las entradas más antiguas con las más recientes.
  
#### Delegación de acceso a los registros de eventos
  
En Microsoft Windows Server™ 2003, se pueden personalizar los permisos en todos los registros de eventos de un equipo. Esta función no estaba disponible en las versiones anteriores de Windows. Puede que algunas organizaciones deseen conceder acceso de sólo lectura a uno o más de los registros de eventos de sistema a algunos miembros del equipo de TI. La lista de control de acceso (ACL) se almacena como una cadena de lenguaje de definición de descriptores de seguridad (SDDL), en un valor REG\_SZ denominado "CustomSD" para cada registro de eventos en el registro, como se muestra en el siguiente ejemplo:
  
**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\EventLog\\CustomSD**  
**Crear un valor de registro REG\_SZ O:BAG:SYD:(D;;0xf0007;;;AN)(D;;0xf0007;;;BG)**  
**(A;;0xf0007;;;SY)(A;;0x7;;;BA)(A;;0x5;;;SO)(A;;0x1;;;IU)(A;;0x1;;;SU)**  
**(A;;0x1;;;S-1-5-3)(A;;0x2;;;LS)(A;;0x2;;;NS)**
  
Si modifica este valor y reinicia el equipo, se aplicará el nuevo parámetro.
  
**Precaución**: tenga cuidado al modificar los valores del Registro, ya que la función "deshacer” no existe en la herramienta Editor del Registro. Si comete un error, tendrá que corregirlo de forma manual. Además, puede configurar accidentalmente las ACL en un registro de eventos de forma que nadie pueda obtener acceso a ellas. Asegúrese de que comprende completamente el SDDL y los permisos predeterminados situados en cada registro de eventos antes de continuar. Asegúrese también de comprobar a fondo cualquier cambio antes de implementarlo en un entorno de producción.
  
Para obtener más información acerca de cómo configurar la seguridad para los registros de eventos en Windows Server 2003, consulte "Cómo configurar la seguridad del registro de eventos localmente o mediante la directiva de grupo en Windows Server 2003" en <http://support.microsoft.com/default.aspx?kbid=323076>.
  
Para obtener más información acerca de SDDL, consulte "[Lenguaje de definición de descriptores de seguridad](http://msdn.microsoft.com/en-us/library/aa379567(vs.85).aspx)" en MSDN® en http://msdn.microsoft.com/library/default.asp?url=/library/en-us/secauthz/  
security/security\_descriptor\_definition\_language.asp.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca del registro de eventos en Windows Server 2003 y Windows XP.
  
-   Para obtener más información acerca de cómo configurar la seguridad para los registros de eventos en Windows Server 2003, consulte "Cómo configurar la seguridad del registro de eventos localmente o mediante la directiva de grupo en Windows Server 2003" en <http://support.microsoft.com/default.aspx?kbid=323076>.
  
-   Para obtener más información acerca de SDDL, consulte el artículo de MSDN "[Lenguaje de definición de descriptores de seguridad](http://msdn.microsoft.com/en-us/library/aa379567(vs.85).aspx)" en http://msdn.microsoft.com/library/default.asp?url=/library/en-us/secauthz/  
    security/security\_descriptor\_definition\_language.asp.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 7: Servicios del sistema
  
Los servicios del sistema se describen de modo diferente a las demás configuraciones de esta guía puesto que las declaraciones de vulnerabilidad, contramedidas e impacto potencial son prácticamente idénticas para todos ellos.
  
Al instalar Microsoft® Windows Server™ 2003 o Microsoft Windows® XP, algunos servicios se instalan y configuran para que se ejecuten de forma predeterminada cuando se inicia el equipo. Hay menos servicios predeterminados de los que había en Windows 2000 Server, y en el caso de Windows Server 2003, los servicios específicos variarán de acuerdo con la función que se asigna a cada servidor. Tal vez no necesite todos los servicios predeterminados en su entorno, por lo que debe deshabilitar aquellos servicios innecesarios para reforzar la seguridad.
  
En este capítulo se ayudará a identificar la función y el propósito de cada servicio, y se explicará qué servicios se dejaron habilitados en Windows Server 2003 y Windows XP para garantizar la compatibilidad de las aplicaciones, la compatibilidad de los clientes o para facilitar la administración de sistemas informáticos. El libro de Microsoft Excel® "Configuración de la seguridad y los servicios predeterminados de Windows" que acompaña a la versión descargable de esta guía, documenta la configuración predeterminada de los servicios del sistema.
  
[](#gaaa)[Descripción general de los servicios](#gaaa)  
[](#agaa)[No establecer permisos en objetos de servicio](#agaa)  
[](#cgaa)[Descripciones de los servicios del sistema](#cgaa)  
[](#dgaa)[Información adicional](#dgaa)
  
### Descripción general de los servicios
  
Un servicio debe iniciar sesión para obtener acceso a los recursos y objetos en el sistema operativo, y en la mayor parte de los servicios no se puede cambiar la cuenta de inicio de sesión predeterminada. Si cambia la cuenta predeterminada, es probable que el servicio falle. Si selecciona una cuenta que no dispone de permiso para iniciar sesión como servicio, el complemento Servicios de Microsoft Management Console (MMC) otorgará automáticamente a esa cuenta la capacidad de iniciar sesión como un servicio en el equipo. No obstante, esta configuración automática no garantiza que el servicio se inicie. Windows Server 2003 ofrece tres cuentas locales integradas que se utilizan como cuentas de inicio de sesión para diversos servicios del sistema:
  
-   **Cuenta del sistema local**. Es una cuenta con muchos privilegios, que tiene acceso completo al equipo y actúa como equipo en la red. Si un servicio utiliza la cuenta del sistema local para iniciar sesión en un controlador de dominio, tendrá acceso a todo el dominio. Algunos servicios están configurados de forma predeterminada para que usen la cuenta del sistema local, y esto no debe cambiarse. La cuenta del sistema local no tiene una contraseña a la que tengan acceso los usuarios.
  
-   **Cuenta del servicio local**. Es una cuenta integrada especial, similar a una cuenta de usuario autenticado. Tiene idéntico nivel de acceso a los recursos y objetos que los miembros del grupo **Usuarios**. Este acceso limitado ayuda a proteger el equipo en caso de que se comprometa la seguridad de determinados servicios o procesos. Los servicios que usan la cuenta del servicio local tienen acceso a los recursos de red como una sesión nula con credenciales anónimas. El nombre de esta cuenta es NT AUTHORITY\\Local Service, y no tiene una contraseña a la que tenga acceso el usuario.
  
-   **Cuenta del servicio de red**. Es una cuenta integrada especial, similar a una cuenta de usuario autenticado. Al igual que la cuenta de servicio local, tiene idéntico nivel de acceso a los recursos y objetos que los miembros del grupo **Usuarios**, lo que ayuda a proteger el equipo. Los servicios que usan la cuenta del servicio de red tienen acceso a los recursos con las credenciales de la cuenta de equipo. El nombre de la cuenta es NT AUTHORITY\\Network Service, y no tiene una contraseña a la que tenga acceso el usuario.
  
**Importante**: si se modifica la configuración predeterminada del servicio, puede que los servicios clave no se ejecuten correctamente. Se debe proceder con especial precaución si cambia las configuraciones de **tipo de inicio** e **inicio de sesión** de los servicios que están configurados para que se inicien automáticamente.
  
Puede establecer la configuración de los servicios del sistema en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración de equipo\\Configuración de Windows\\Configuración de seguridad\\Servicios del sistema\\**
  
#### Vulnerabilidad
  
Todo servicio o aplicación es un punto de ataque potencial. Por tanto, debe deshabilitar o quitar del entorno todos aquellos servicios o archivos ejecutables que no sean necesarios. Existen otros servicios opcionales disponibles en Windows Server 2003, como los Servicios de Certificate Server, que no se agregan en la instalación predeterminada del sistema operativo.
  
Puede agregar estos servicios opcionales a un equipo existente a través de la opción Agregar o quitar programas del Panel de control o el Asistente para configurar su servidor de Windows Server 2003. También puede crear una instalación automática personalizada de Windows Server 2003. En la Directiva de línea de base de servidores miembro que se describe en la [*Guía de Seguridad de Windows Server 2003*](http://go.microsoft.com/fwlink/?linkid=14845) (disponible en http://go.microsoft.com/fwlink/?LinkId=14845), están deshabilitados estos servicios opcionales y todos los servicios innecesarios.
  
**Importante**: si habilita servicios adicionales, dichos servicios pueden depender de otros servicios. Agregue todos los servicios necesarios para una función de servidor específica a la directiva de la función que realiza el servidor dentro de la organización.
  
#### Contramedida
  
Deshabilite todos los servicios no necesarios.
  
Para cada servicio del sistema, puede asignar un estado del servicio a través de la directiva de grupo. Los valores que se pueden seleccionar para esta configuración de Directiva de grupo son los siguientes:
  
-   Automático
  
-   Manual
  
-   Deshabilitado
  
-   No está definido
  
Otra manera de administrar la seguridad del servicio es configurar una lista de control de acceso (ACL) para cada servicio con una lista de cuentas definida por el usuario. Este método proporciona una manera de controlar el inicio del servicio y el acceso al servicio cuando ya se está ejecutando.  
  
#### Impacto potencial
  
Si se deshabilitan algunos servicios (como el Administrador de cuentas de seguridad), no podrá reiniciar el equipo. Si se deshabilitan otros servicios críticos, es probable que el equipo no se pueda autenticar con los controladores de dominio. Si desea deshabilitar algunos servicios del sistema, debe probar la configuración cambiada en equipos que no sean de producción antes de hacer los cambios en un entorno de producción.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### No establecer permisos en objetos de servicio
  
Hay herramientas basadas en una interfaz gráfica de usuario (GUI) que puede utilizar para modificar los servicios. Sin embargo, las versiones anteriores de estas herramientas que se incluyeron con versiones previas del sistema operativo Windows (antes de Windows Server 2003) aplican automáticamente los permisos a cada servicio cuando configura cualquiera de las propiedades de un servicio. Las herramientas como el Editor de objetos de directiva de grupo y el complemento Plantillas de seguridad de MMC utilizan el DLL del Editor de configuración de seguridad para aplicar estos permisos.
  
Por ejemplo, cuando usted utiliza el complemento Plantillas de seguridad de MMC para configurar el estado de inicio de un servicio en Windows XP, se mostrará el cuadro de diálogo siguiente:
  
[![](images/Dd162275.tcfg0701(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/dd162275.tcfg0701_big(es-es,technet.10).gif)
  
**Figura 7.1 Cuadro de diálogo Seguridad de servicios**
  
Sin importar si hace clic en **Aceptar** o **Cancelar**, los permisos se aplicarán al servicio que se está configurando. Desgraciadamente, los permisos que este cuadro de diálogo propone no coinciden con los permisos predeterminados para la mayoría de los servicios que se incluyen con Windows. De hecho, los permisos causarán una serie de problemas en muchos servicios. Microsoft recomienda que no altere los permisos en los servicios que se incluyen con Windows XP o Windows Server 2003, porque los permisos predeterminados ya son bastante restrictivos.
  
Esta funcionalidad cambió en Windows Server 2003, y su versión del DLL del Editor de configuración de seguridad no le obliga a configurar los permisos cuando modifica las propiedades de un servicio. Dispone de varias opciones diferentes para lidiar con esta situación difícil:
  
-   Utilice el Asistente para configuración de seguridad, un componente opcional de Windows que se incluye con Windows Server 2003 Service Pack 1 (SP1). Microsoft recomienda este enfoque cuando necesite configurar los filtros de servicios y de puerto de red para varias funciones de servidor de Windows Server 2003.
  
-   Ejecute el complemento Plantilla de seguridad de MMC y el Editor de objetos de directiva de grupo en un servidor que ejecute Windows Server 2003 con SP1. Microsoft recomienda este enfoque cuando necesite configurar los servicios para plantillas de seguridad o Directivas de grupo que se aplicarán a Windows XP.
  
-   Utilice un editor de texto como Bloc de notas para modificar las plantillas de seguridad o las Directivas de grupo en un equipo con Windows XP Professional. Este método es el menos deseable, pero para algunos clientes podría ser el único disponible. Se proporcionan instrucciones detalladas en la siguiente sección.
  
#### Edición manual de las plantillas de seguridad
  
Aunque puede utilizar un editor de texto como el Bloc de notas para modificarlos manualmente, las plantillas de seguridad son archivos complejos. Las plantillas de seguridad que se crean con una especificación de plantilla definida incorrectamente pueden evitar que el equipo se inicie. Aunque la mayoría de los tipos de error no causarán un problema tan grave, debe ser paciente y prestar atención a los detalles si necesita modificar manualmente plantillas de seguridad.
  
Cuando utiliza una de las herramientas basadas en una interfaz gráfica de usuario para configurar los servicios en una plantilla de seguridad, la información de configuración se almacena en la sección del archivo relacionada con la configuración general del servicio. El siguiente texto de muestra es de una plantilla de seguridad en la que los servicios de alerta, de portafolios y de examinador de equipos tienen su estado de inicio configurado como **Deshabilitado** y el servicio de Cliente DHCP tiene su estado de inicio configurado como **Automático.**
  
```  
 \[Service General Setting\] Alerter,4,"D:AR(A;;CCDCLCSWRPWPDTLOCRSDRCWDWO;;;BA) (A;;CCDCLCSWRPWPDTLOCRSDRCWDWO;;;SY)(A;;CCLCSWLOCRRC;;;IU) S:(AU;FA;CCDCLCSWRPWPDTLOCRSDRCWDWO;;;WD)" ClipSrv,4,"D:AR(A;;CCDCLCSWRPWPDTLOCRSDRCWDWO;;;BA) (A;;CCDCLCSWRPWPDTLOCRSDRCWDWO;;;SY)(A;;CCLCSWLOCRRC;;;IU) S:(AU;FA;CCDCLCSWRPWPDTLOCRSDRCWDWO;;;WD)" Browser,4,"D:AR(A;;CCDCLCSWRPWPDTLOCRSDRCWDWO;;;BA) (A;;CCDCLCSWRPWPDTLOCRSDRCWDWO;;;SY)(A;;CCLCSWLOCRRC;;;IU) S:(AU;FA;CCDCLCSWRPWPDTLOCRSDRCWDWO;;;WD)" Dhcp,2,"D:AR(A;;CCDCLCSWRPWPDTLOCRSDRCWDWO;;;BA) (A;;CCDCLCSWRPWPDTLOCRSDRCWDWO;;;SY)(A;;CCLCSWLOCRRC;;;IU) S:(AU;FA;CCDCLCSWRPWPDTLOCRSDRCWDWO;;;WD)"   
```  
El formato para cada entrada incluye tres campos delimitados por comas.
  
-   El primer campo especifica el nombre del servicio. Por ejemplo, ClipSrv indica el servicio de portafolios.
  
-   El segundo campo define el estado de inicio:
  
    -   4 especifica Deshabilitado
  
    -   3 especifica Manual
  
    -   2 especifica Automático
  
-   El tercer campo define los permisos para el objeto de servicio en el Lenguaje de definición de descriptores de seguridad (SDDL).
  
No es necesario entender los detalles de SDDL para utilizar el Asistente para configuración de seguridad. Puede encontrar más información acerca de SDDL en el artículo "[Lenguaje de definición de descriptores de seguridad](http://msdn.microsoft.com/en-us/library/aa379567(vs.85).aspx)" de MSDN® en http://msdn.microsoft.com/library/en-us/secauthz/  
security/security\_descriptor\_definition\_language.asp.
  
Para resolver los problemas potenciales de permisos en los objetos del servicio, elimine la cadena SDDL en el tercer campo, pero deje el par de comillas dobles. El ejemplo siguiente muestra el texto correcto de los cuatro servicios mencionados:
  
```  
 \[Service General Setting\] Alerter,4,"" ClipSrv,4,"" Browser,4,"" Dhcp,2,""   
```  
Después de eliminar la información SDDL de todos los servicios en la plantilla de seguridad, guarde el archivo. Puede aplicar la plantilla de seguridad a través de cualquiera de los métodos típicos. Por supuesto, es muy importante que pruebe de forma exhaustiva las plantillas de seguridad antes de aplicarlas a los equipos de producción.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Descripciones de los servicios del sistema
  
Las subsecciones siguientes describen los servicios de Windows Server 2003 y de Windows XP en orden alfabético. Se incluyen los servicios que se instalan de forma predeterminada así como los servicios adicionales que se pueden agregar al equipo.
  
**Nota**: si no se inicia un servicio, otros servicios que dependan de ese servicio tampoco se iniciarán. Por lo tanto, si cambia el estado de un servicio, puede afectar a otros servicios que aparentemente no estén relacionados. Dichas dependencias existen para todos los servicios que se describen en esta sección. Para comprobar las dependencias de un servicio, haga clic en la ficha **Dependencias** del cuadro de diálogo de propiedades del servicio en el complemento Servicios de MMC.
  
#### Servicio de alerta
  
El servicio de **alerta** notifica a los usuarios y equipos seleccionados de las alertas administrativas. Puede utilizarlo para enviar mensajes de alerta a usuarios especificados que estén conectados a la red.
  
Los mensajes de alerta advierten a los usuarios de problemas relacionados con la seguridad, el acceso y la sesión de usuario Los mensajes de alerta se envían de un servidor a un equipo cliente, y el servicio de **Mensajería** debe ejecutarse en el equipo cliente para que éste pueda recibir mensajes de alerta. (El servicio de **Mensajería** está deshabilitado de forma predeterminada en Windows XP y Windows Server 2003 para que los usuarios malintencionados no puedan enviar notificaciones falsas).
  
Si el servicio de **alerta** está deshabilitado, las aplicaciones que utilizan las interfaces de programación de aplicaciones (API) NetAlertRaise o NetAlertRaiseEx no podrán notificar a un usuario o equipo, mediante un cuadro de mensaje que el servicio de **Mensajería** muestra, que se ha producido una alerta administrativa. Por ejemplo, muchas herramientas de administración de sistema de alimentación ininterrumpida (UPS) utilizan el servicio de **alerta** para notificar a los administradores acerca de eventos significativos relacionados con UPS. Si quiere utilizar este servicio, debe configurar su estado de inicio en **Automático** para que los componentes externos lo puedan utilizar cuando sea necesario.
  
#### Servicio de búsqueda de experiencia de aplicaciones
  
El **Servicio de búsqueda de experiencia de aplicaciones** (AELookupSvc) es una parte del Administrador de compatibilidad de aplicaciones. Procesa las solicitudes de búsqueda de compatibilidad de aplicaciones según se inician, proporciona compatibilidad para equipos Windows Server 2003 en un dominio, informa de problemas de compatibilidad y aplica automáticamente actualizaciones de software a programas.
  
El **Servicio de búsqueda de experiencia de aplicaciones** debe estar activo para que se apliquen las actualizaciones de software de compatibilidad de aplicaciones. No puede personalizar este servicio; el sistema operativo lo utiliza internamente. Este servicio no utiliza recursos de servicios de red, Internet ni de directorio de Active Directory®.
  
Si deshabilita el **Servicio de búsqueda de experiencia de aplicaciones**, el servicio seguirá ejecutándose pero no se harán llamadas al servicio. No es posible detener el proceso real.
  
#### Servicio de puerta de enlace de capa de aplicación
  
El **Servicio de puerta de enlace de capa de aplicación** es un subcomponente del subsistema de red de Windows. Ofrece compatibilidad para los complementos que permiten a los protocolos de red pasar a través del servidor de seguridad y trabajar detrás de ICS. Los complementos de Puerta de enlace de capa de aplicación (ALG) pueden abrir puertos y cambiar datos incrustados en paquetes, como puertos y direcciones IP. El protocolo de transferencia de archivos (FTP) es el único protocolo de red del que se ha incluido un complemento en Windows Server 2003 Standard Edition y Windows Server 2003 Enterprise Edition.
  
El complemento ALG FTP está diseñado para admitir sesiones FTP activas a través del motor de traducción de direcciones de red (NAT) que está incluido en Windows. El complemento ALG FTP redirige todo el tráfico que pasa por NAT destinado al puerto 21 a un puerto de escucha privado del 3000 al 5000 del adaptador de bucle de retorno. Después, el complemento ALG FTP supervisa y actualiza el tráfico en el canal de control FTP para que el complemento FTP pueda instalar las asignaciones de puertos a través de NAT para los canales de datos FTP. El complemento FTP también actualizará los puertos de la secuencia del canal de control FTP.
  
Si se detiene el **Servicio de puerta de enlace de capa de aplicación**, no se podrá disponer de conectividad de red para los protocolos en cuestión y esto afectará negativamente a la red. Por ejemplo, si deshabilita este servicio, las aplicaciones de mensajería instantánea Windows Messenger y MSN® Messenger producirán un error.
  
#### Administración de aplicaciones
  
El servicio de **Administración de aplicaciones** proporciona servicios de instalación de software como Asignar, Publicar y Quitar. Este servicio procesa las solicitudes de enumeración, instalación y eliminación de las aplicaciones instaladas a través de una red corporativa. Cuando se hace clic en **Agregar** en Agregar o quitar programas, en el Panel de control de un equipo incluido en un dominio, el programa llama a este servicio para recuperar la lista de aplicaciones instaladas. También se llama a este servicio cuando se utiliza Agregar o quitar programas para instalar o quitar una aplicación. También se llama cuando un componente, como el shell o COM, realiza una solicitud de instalación para que una aplicación controle una extensión de archivo, una clase del modelo de objetos componentes (COM) o un ProgID que no está presente en el equipo. El servicio se inicia con la primera llamada que se hace al mismo y no finaliza una vez iniciado.
  
**Nota**: para obtener más información acerca de COM, de la clases COM o de ProgIDs, consulte la información del kit de desarrollo de software (SDK) de la biblioteca MSDN en la página [Windows Resource Kits - Web Resources](http://www.microsoft.com/windows/reskits/webresources/) en www.microsoft.com/windows/reskits/webresources.
  
Si se deshabilita o detiene el servicio **Administración de aplicaciones**, los usuarios no podrán instalar, quitar o enumerar las aplicaciones instaladas en Active Directory mediante las tecnologías de administración de Microsoft IntelliMirror®. Si deshabilita este servicio, no recuperará la información de las aplicaciones instaladas y tampoco aparecerá esta información en la sección **Agregar nuevos programas** de Agregar o quitar programas en el Panel de control. El cuadro de diálogo **Agregar programasdesde la red** mostrará el siguiente mensaje:
  
No hay programas disponibles en la red.
  
No es posible detener este servicio una vez iniciado sin reiniciar el equipo. Si no necesita este servicio y no quiere que se inicie, debe deshabilitarlo.
  
#### Servicio de estado de ASP.NET
  
El **servicio de estado de ASP.NET** ofrece compatibilidad para los estados de sesión fuera de proceso de ASP.NET. ASP.NET incluye el concepto de estado de sesión, es decir, se puede tener acceso a un listado de los valores asociados a la sesión de cliente desde las páginas ASP.NET a través del parámetro **Session**. Se proporcionan tres opciones para almacenar los datos de sesión: en proceso, base de datos de Microsoft SQL Server™ y servidor de estado de sesión fuera de proceso.
  
El **servicio de estado de ASP.NET** almacena datos de sesión fuera de proceso. El servicio se comunica con ASP.NET, que se ejecuta en un servidor web mediante sockets. Si se deshabilita o detiene este servicio, no se procesarán solicitudes fuera de proceso. El código ejecutable para este servicio se instala de forma predeterminada, pero el servicio en sí está deshabilitado hasta que cambie manualmente su tipo de inicio a Automático o Manual.
  
#### Actualizaciones automáticas
  
El servicio de **Actualizaciones automáticas** permite la descarga e instalación de actualizaciones de seguridad importantes de Windows y Office. Proporciona de forma automática a los equipos con Windows las últimas actualizaciones, controladores y optimizaciones. Ya no tendrá que buscar de forma manual la información y las actualizaciones de seguridad; el sistema operativo las proporciona directamente a su equipo. El sistema operativo sabe cuándo el usuario está en línea y utiliza su conexión a Internet para buscar actualizaciones aplicables a través del servicio Windows Update. En función de los valores de configuración especificados, el servicio le notificará antes de la descarga, antes de la instalación, o bien, instalará de forma automática las actualizaciones.
  
Puede desactivar la característica Actualizaciones automáticas desde **Sistemas** en Panel de control. Alternativamente, puede hacer clic con el botón secundario del mouse en el icono **Mi PC** y, a continuación, hacer clic en **Propiedades**.
  
Asimismo, puede utilizar la plantilla administrativa del complemento Editor de objetos de directiva de grupo de MMC para configurar un servidor de intranet con los servicios de actualización de Windows Server de forma que aloje actualizaciones desde los sitios de Microsoft Update. Este parámetro le permite determinar un servidor en la red que funcione a modo de servicio de actualizaciones internas. El cliente de Actualizaciones automáticas buscará en este servicio las actualizaciones aplicables a los equipos de la red.
  
**Nota:** para obtener más información acerca de los servicios de Actualización de Windows Server, visite el sitio web de [servicios de actualización de Windows Server](http://go.microsoft.com/fwlink/?linkid=21133) en http://go.microsoft.com/fwlink/?LinkId=21133.
  
Si se detiene o deshabilita el servicio **Actualizaciones automáticas**, no se descargarán actualizaciones clave en el equipo de forma automática. Necesitará buscar, descargar e instalar las revisiones aplicables a través del sitio web de [Windows Update](http://update.microsoft.com/windowsupdate/v6/default.aspx?ln=es) en http://update.microsoft.com.
  
#### Servicio de transferencia inteligente en segundo plano (BITS)
  
El **Servicio de transferencia inteligente en segundo plano** constituye un mecanismo de transferencia de archivos en segundo plano, así como un administrador de cola. **BITS** transfiere archivos de forma asíncrona entre un cliente y un servidor HTTP. De forma predeterminada, se envían las solicitudes a **BITS** y los archivos se transfieren a través de un ancho de banda de red inactivo, para que otras actividades relacionadas con la red, como la exploración, no resulten afectadas.
  
**BITS** suspenderá la transferencia si se pierde la conexión o si el usuario cierra la sesión. La conexión **BITS** es persistente y transfiere información mientras el usuario está desconectado, entre desconexiones de la red y durante los reinicios del equipo. Cuando el usuario inicia sesión, **BITS** reanuda la tarea de transferencia del usuario.
  
**BITS** utiliza una cola para administrar las transferencias de archivos. Puede establecer prioridades en las tareas de transferencia de la cola y especificar si los archivos se transferirán en primer o en segundo plano. Las transferencias en segundo plano se optimizan con **BITS**, que aumenta y disminuye (o *regula*) la tasa de transferencia con base en la cantidad de ancho de banda de red inactiva que esté disponible. Si una aplicación de red empieza a consumir más ancho de banda, **BITS** reduce la velocidad de transferencia para mantener la experiencia interactiva del usuario.
  
**BITS** proporciona un nivel de prioridad en primer plano y tres en segundo plano, que se pueden utilizar para establecer prioridades en los trabajos de transferencia. Los trabajos con una prioridad superior se adelantan a los que tienen una prioridad inferior. Los trabajos con el mismo nivel de prioridad comparten el tiempo de transferencia; la programación por turnos evita que un trabajo de gran tamaño bloquee la cola de transferencia. Los trabajos con una prioridad menor no reciben tiempo de transferencia hasta que todos los que tienen una prioridad superior finalizan o se encuentran en estado de error.
  
**BITS** se configura para inicio manual tanto en Windows Server 2003 como en Windows XP. Se inicia a petición cuando se envía el primer trabajo. **BITS** se detiene una vez finalizados todos los trabajos pendientes.
  
Si **BITS** se detiene, características como Actualizaciones automáticas no podrán descargar programas y otra información de forma automática. Esta funcionalidad significa que el equipo no recibirá actualizaciones automáticas del servidor corporativo de Software Update Services (SUS), si éste se ha configurado mediante Directiva de grupo. Si deshabilita este servicio, impedirá que cualquier servicio que dependa explícitamente de él pueda transferir archivos, a menos que se ponga en marcha un mecanismo a prueba de errores que los transfiera directamente a través de otros métodos como Internet Explorer.
  
#### Servicios de Certificate Server
  
Los servicios de **Certificate Server** forman parte del núcleo del sistema operativo y permiten que una organización pueda actuar como su propia entidad emisora de certificados (CA) y emitir y administrar certificados digitales para aplicaciones como Secure/Multipurpose Internet Mail Extensions (S/MIME), Nivel de sockets seguros (SSL), Sistema de archivos de cifrado (EFS), IP Security (IPSec) y conexión de tarjeta inteligente. Windows Server 2003 admite varios niveles de jerarquía para una entidad emisora de certificados, así como una red de confianza de certificación cruzada, que incluye las entidades emisoras de certificados con y sin conexión.
  
Los servicios de **Certificate Server** no se instalan de forma predeterminada. Los administradores lo deben instalar a través de Agregar o quitar programas en el Panel de control. Si detiene o deshabilita los **servicios de certificados** después de la instalación, no se aceptarán las solicitudes de certificados y no se publicarán las listas de revocación de certificados (CRL) ni las diferencias entre listas CRL. Si el servicio se detiene durante el tiempo suficiente como para que las CRL caduquen, no se podrán validar los certificados existentes.
  
#### Servicio de cliente para NetWare
  
Los servidores que tienen instalado el servicio del sistema **Servicio de cliente para NetWare** proporcionan acceso a recursos de archivos e impresión en redes de NetWare para usuarios con inicio de sesión interactivo. Con el **Servicio de cliente para Netware** se puede obtener acceso a recursos de archivos e impresión en servidores Netware que ejecutan Servicios de directorio Novell (NDS) o seguridad de enlace (NetWare versiones 3.x o 4.x) desde el equipo.
  
El **Servicio de cliente para NetWare** no admite el protocolo IP y, por lo tanto, no se puede utilizar para interoperar con NetWare 5.x en un entorno únicamente de IP. Para contar con esta capacidad, deberá cargar el protocolo Internetwork Packet Exchange (IPX) en el servidor NetWare 5.x, o bien, utilizar un redirector que sea compatible con el protocolo de núcleo de NetWare (NCP) y que admita IP nativo.
  
Si detiene o deshabilita el **Servicio de cliente para NetWare**, no tendrá acceso a los recursos de archivos e impresión en las redes NetWare, a menos que instale el Cliente para NetWare de Novell. Este servicio no se instala ni habilita de forma predeterminada.
  
#### Portafolios
  
El servicio **Portafolios** habilita el Visor del Portafolios para crear y compartir páginas de datos que podrán revisar los usuarios remotos. Este servicio depende del servicio **DDE de red (NetDDE)** para crear los recursos compartidos de archivo a los que otros equipos se pueden conectar. La aplicación y el servicio Portafolios permiten crear las páginas de datos para compartir.
  
El servicio **Portafolios** se instala de forma predeterminada, pero su estado de inicio se configura como **Deshabilitado.** Cuando este servicio se detiene, el Visor del Portafolios no puede compartir información con equipos remotos. Sin embargo, se puede emplear clipbrd.exe para visualizar el Portafolios local, en el que se almacenan los datos cuando un usuario resalta texto y, a continuación, hace clic en **Copiar** en el menú **Edición** o presiona CTRL+C en el teclado.
  
#### Servicio de Cluster Server
  
El **Servicio de Cluster Server** controla las operaciones del clúster de servidor y administra la base de datos del clúster. Un clúster es un conjunto de equipos independientes que trabajan juntos para lograr un equilibrio de la carga y la conmutación de uno a otro cuando se produce un error que impide que uno de los equipos siga funcionando. Las aplicaciones que toman en cuenta el funcionamiento en clúster, como Microsoft Exchange Server y Microsoft SQL Server, utilizan el clúster para presentar un solo equipo virtual a los usuarios. El software de clúster distribuye las tareas de datos y procesamiento entre los nodos del clúster. Cuando se produce un error en un nodo, otro proporciona los servicios y datos que prestaba el que generó el error. Cuando se agrega o repara un nodo, el software del clúster migra algunas tareas de datos y procesamiento a dicho nodo.
  
Existen dos tipos diferentes de soluciones de clúster en la plataforma Windows que admiten diferentes estilos de aplicación: clústeres de servidor y de equilibrio de carga de red (NLB). Los primeros proporcionan un entorno de alta disponibilidad para aplicaciones que deben ejecutarse de forma continua sin errores, como los servidores de bases de datos o de archivos, y ofrecen compatibilidad de conmutación por error con una administración de clústeres estrechamente integrada. Los clústeres NLB proporcionan un entorno de gran disponibilidad y escalabilidad para otros tipos de aplicaciones, como los servidores web clientes y de equilibrio de la carga de las solicitudes de clientes entre un conjunto de servidores idénticos.
  
El **servicio de Cluster Server** proporciona compatibilidad para clústeres de servidor. Es el componente de software clave que controla todos los aspectos del funcionamiento del clúster de servidor y administra la base de datos del clúster. Cada nodo de un clúster ejecuta una instancia del **Servicio de Cluster Server**.
  
Windows Server 2003 admite clústeres de servidor de hasta ocho nodos tanto en Enterprise Server como en ediciones Datacenter Server de Windows. Sin embargo, un clúster sólo puede consistir de nodos que ejecuten una edición de Windows o la otra; no pueden ejecutarse ediciones diferentes dentro de un solo clúster.
  
Para los clústeres de servidor se pueden establecer tres configuraciones diferentes:
  
-   **Nodo único**. Estos clústeres de servidor se pueden configurar con o sin dispositivos de almacenamiento de clústeres externos. Para los que no tienen dicho dispositivo, el disco local se configura como dispositivo de almacenamiento de clústeres. Utilice las configuraciones de nodo único para desarrollar aplicaciones para clústeres o bien empléelas en producción para proporcionar supervisión de estado local y capacidades de reinicio a las aplicaciones.
  
-   **Dispositivo de quórum único**. estos clústeres de servidor tienen dos o más nodos y se configuran de modo que cada nodo está conectado a uno o varios dispositivos de almacenamiento de clústeres. Los datos de configuración del clúster se almacenan en un único dispositivo denominado disco de quórum.
  
-   **Conjunto de nodos mayoritario**. Estos clústeres de servidor tienen dos o más nodos que pueden estar conectados o no a uno o varios dispositivos de almacenamiento de clústeres. Los datos de configuración del clúster se almacenan en varios discos repartidos entre el clúster; el **Servicio de Cluster Server** garantiza la coherencia de los datos entre los diferentes discos.
  
El **Servicio de Cluster Server** no se instala ni habilita de forma predeterminada. Si el **Servicio de Cluster Server** se detiene después de que se instala, los clústeres no estarán disponibles. Para obtener información adicional acerca de cómo configurar la seguridad para clústeres de Windows, revise los vínculos pertinentes en la sección "Más Información" al final de este capítulo.
  
#### Sistema de eventos COM+
  
El servicio **Sistema de eventos COM+** proporciona la distribución automática de eventos a los componentes COM que están suscritos a él. Eventos COM+ amplía el modelo de programación COM+ para admitir eventos enlazados en tiempo de ejecución o llamadas de método entre el editor o suscriptor y el sistema de eventos. El sistema de eventos notifica a los consumidores de eventos cuando la información está disponible, y no sondea repetidas veces el servidor.
  
El servicio **Sistema de eventos COM+** maneja la mayor parte de la semántica de eventos para el editor y el suscriptor. Los editores ofrecen publicar tipos de evento, y los suscriptores solicitan tipos de evento de editores específicos. Las suscripciones se mantienen fuera del editor y el suscriptor, y se recuperan cuando se necesitan, lo que simplifica el modelo de programación para ambos. El suscriptor no necesita tener la lógica para construir las suscripciones; es posible construir a un suscriptor tan fácil como un componente COM. El ciclo de vida de la suscripción está separado del ciclo de vida del editor o del suscriptor. Puede construir las suscripciones antes de que se active el suscriptor o el editor.
  
Este servicio se instala de forma predeterminada, pero no se inicia hasta que una aplicación solicita sus servicios. Cuándo se detiene el **Sistema de eventos COM+** la **Notificación de eventos del sistema** se cerrará y no será capaz de proporcionar notificaciones de inicio o final de sesión. El servicio **Instantáneas de volumen**, necesario para Copia de seguridad de Windows y aplicaciones de copia de seguridad que dependen de la API de Copia de seguridad de Windows, requiere este servicio.
  
#### Aplicación del sistema COM+
  
El servicio del sistema **Aplicación del sistema COM+** administra la configuración y el seguimiento de los componentes basados en COM+. Si se detiene este servicio, la mayor parte de dichos componentes no funcionará correctamente. El servicio **Instantáneas de volumen**, necesario para Copia de seguridad de Windows y aplicaciones de copia de seguridad que dependen de la API de Copia de seguridad de Windows, requiere este servicio. Este servicio se instala y habilita de forma predeterminada.  
  
#### Examinador de equipos
  
El servicio **Examinador de equipos** mantiene una lista actualizada de los equipos de la red y la proporciona a los programas que la solicitan. Esteservicio lo utilizan equipos basados en Windows que necesitan visualizar recursos y dominios de red. Los equipos designados como examinadores mantienen las listas de búsqueda que contienen todos los recursos compartidos que se utilizan en la red. Las versiones anteriores de aplicaciones Windows, por ejemplo, Mis sitios de red, el comando NET VIEW y el Explorador de Windows NT® requieren la capacidad de búsqueda. Por ejemplo, si abre Mis sitios de red en un equipo con Windows 95, un equipo que se designa como explorador genera la lista de dominios y equipos que muestra.
  
Existen diferentes funciones que un equipo puede realizar en un entorno de búsqueda. En determinadas circunstancias, como cuando se apaga el equipo designado para una función de examinador o no funciona correctamente, los examinadores (o posibles examinadores) se pueden cambiar a una función de operación diferente.
  
El servicio **Examinador de equipos** se habilita y se inicia de forma predeterminada. Si se detiene, no se podrá actualizar o mantener la lista del examinador.
  
#### Servicios de cifrado
  
Los **Servicios de cifrado** proporcionan servicios de administración de claves para el equipo. **Se componen de tres servicios diferentes de administración**:
  
-   **Servicio de catálogo de base de datos**. Este servicio agrega, elimina y busca archivos de catálogo, que se utilizan para firmar todos los archivos en el sistema operativo. La protección de archivos de Windows (WFP), la firma de controladores y la configuración utilizan este servicio para comprobar los archivos firmados. No se puede detener este servicio durante la configuración. Si se detiene después de la instalación, se iniciará a petición.
  
-   **Servicio de raíz protegida**. Se encarga de agregar y quitar certificados de entidades emisoras de certificados raíz de confianza. Este servicio muestra un cuadro de mensaje de servicio con el nombre y la huella digital del certificado. Si hace clic en **Aceptar**, se agrega o elimina el certificado de la lista actual de entidades emisoras raíz de confianza. Únicamente las cuentas LocalSystem disponen de acceso de escritura a dicha lista. Si se detiene este servicio, el usuario actual no podrá agregar o quitar certificados de entidad emisora de certificados raíz de confianza.
  
-   **Servicio de claves**. Permite a los administradores inscribirse para obtener certificados en nombre de la cuenta del equipo local. El servicio proporciona varias funciones que se requieren para la inscripción, como la enumeración de las entidades emisoras de certificados, la enumeración de las plantillas de equipo disponibles, la capacidad para crear y emitir una solicitud de certificado en el contexto del equipo local, etc. Sólo los administradores se pueden inscribir en nombre de la cuenta del equipo local. El Servicio de claves también permite a los administradores instalar de forma remota archivos de intercambio de información personal (PFX) en el equipo. Si se detiene el servicio, la inscripción automática no podrá adquirir automáticamente el conjunto predeterminado de certificados de equipo.
  
Los **Servicios de cifrado** se habilitan y se inician automáticamente de forma predeterminada. Si se detienen, los servicios de administración que se mencionan en los párrafos anteriores no funcionarán apropiadamente.
  
#### Iniciador de procesos de servidor DCOM
  
En versiones anteriores de Windows, el servicio de llamada a procedimiento remoto (RPCSS) se ejecutaba como sistema local. Para reducir el área de incidencia de un ataque en Windows y proporcionar una defensa a fondo, la funcionalidad del servicio RPC se dividió en dos servicios en Windows XP Service Pack 2 y Windows Server 2003 Service Pack 1.
  
El servicio RPCSS retiene toda la funcionalidad original para la que no se necesitan privilegios de sistema local, y ahora se ejecuta bajo la cuenta Servicio de red. El servicio **Iniciador de procesos de servidor DCOM** (DCOMLaunch) incorpora las funciones del servicio RPC anterior para el que se necesitaban privilegios de sistema local; se ejecuta bajo la cuenta Sistema local. Este servicio se instala e inicia de forma predeterminada.
  
Si el servicio **Iniciador de procesos de servidor DCOM** se detiene, las llamadas de procedimiento remoto y las solicitudes DCOM en el equipo local no funcionarán correctamente. En particular, el servicio de Firewall de Windows fallará si se detiene este servicio.
  
#### Cliente DHCP
  
El servicio **Cliente DHCP** administra la configuración de red. Registra y actualiza las direcciones IP y los nombres DNS para el equipo. No es necesario modificar manualmente la configuración de IP para un equipo cliente, como un equipo portátil, que se conecta de ubicaciones diferentes en la red. El equipo cliente recibe automáticamente una dirección IP nueva, independientemente de la subred a la que se vuelve a conectar (siempre que se pueda tener acceso al servidor DHCP desde las subredes). No es necesario realizar de forma manual la configuración de DNS o WINS. El servidor DHCP puede ofrecer estos valores de configuración al cliente, siempre que el servidor se haya configurado para emitir dicha información. Para habilitar esta opción en el cliente, sólo tiene que hacer clic en la opción **Obtener la dirección DNS del servidor automáticamente**. Las direcciones IP duplicadas no producen ningún conflicto.
  
Si se detiene el servicio **Cliente DHCP**, el equipo no recibirá direcciones IP dinámicas, y las actualizaciones DNS dinámicas automáticas no se registrarán en el servidor DNS.
  
#### Servidor DHCP
  
El servicio **Servidor DHCP** asigna direcciones IP y permite de forma automática la configuración avanzada de parámetros de red como servidores DNS y WINS a clientes DHCP. DHCP emplea un modelo cliente/servidor. El administrador de la red establece uno o varios servidores DHCP que mantienen actualizada la información de configuración TCP/IP y la facilitan a los equipos cliente. La base de datos del servidor contiene:
  
-   Valores de configuración válidos para todos los equipos cliente de la red.
  
-   Direcciones IP válidas, que se mantienen en un grupo para su asignación a los equipos cliente, además de las direcciones reservadas para la asignación manual.
  
-   Duración de la concesión ofrecida por el servidor. La concesión define el período de tiempo en que la dirección IP asignada es válida.
  
DHCP es un estándar IP ideado para reducir la complejidad de la tarea de administrar las configuraciones de direcciones. Utiliza un servidor para administrar de modo centralizado las direcciones IP y otros detalles de configuración relacionados que se utilizan en la red. La familia Windows Server 2003 proporciona el servicio DHCP, que permite al equipo servidor funcionar como un servidor DHCP y configurar equipos clientes habilitados para DHCP en la red, tal como se describe en el borrador de estándar actual de DHCP, Internet Engineering Task Force (IETF) Request for Comments (RFC) 2131.
  
DHCP contiene el protocolo Multicast Address Dynamic Client Assignment Protocol (MADCAP), que se utiliza para realizar la asignación de direcciones de multidifusión. Cuando se asignan dinámicamente direcciones IP a equipos cliente registrados mediante MADCAP, los clientes pueden participar con eficacia en el proceso de transmisión de datos, por ejemplo, en las transmisiones de red en tiempo real de vídeo o audio.
  
Con un servidor DHCP instalado y configurado en la red, los equipos cliente habilitados para DHCP podrán obtener dinámicamente las direcciones IP y los valores de configuración relacionados cada vez que se inicien y se conecten a la red. Los servidores DHCP proporcionan esta configuración a modo de oferta de concesión de dirección a los equipos cliente que la solicitan.
  
Si detiene el servicio **Servidor DHCP**, no se podrá emitir direcciones IP u otros parámetros de configuración de forma automática. Este servicio sólo se instala y activa si configura un equipo Windows Server 2003 como servidor DHCP.
  
#### Sistema de archivos distribuido
  
Este servicioadministra volúmenes lógicos distribuidos a lo largo de una red de área local o extensa (WAN) y es necesario para el recurso compartido SYSVOL de Active Directory. El Sistema de archivos distribuido (DFS) es un servicio distribuido que integra recursos compartidos de archivos distintos en un solo espacio de nombres lógico.
  
Este espacio de nombres constituye la representación lógica de los recursos de almacenamiento en red que se encuentran disponibles para los usuarios de la red. Si se desactiva el servicio **Sistema de archivos distribuido**, no tendrá acceso a los archivos compartidos o datos de la red a través del espacio de nombres lógico. Para tener acceso a los datos cuando el servicio está detenido, será necesario conocer los nombres de todos los servidores y recursos compartidos del espacio de nombres y obtener acceso a cada uno de estos objetivos de forma independiente. Este servicio se instala y ejecuta de forma predeterminada en equipos con Windows Server 2003.
  
#### Cliente de seguimiento de vínculos distribuidos
  
El servicio **Cliente de seguimiento de vínculos distribuidos** mantiene vínculos entre los archivos del sistema de archivos NTFS dentro de un equipo o entre equipos de un dominio de red. Este servicio garantiza que los accesos directos y los vínculos OLE (vinculación e incrustación de objetos) continúen funcionando después de cambiar el nombre o mover el archivo de destino.
  
Cuando crea un acceso directo a un archivo en un volumen de NTFS, el seguimiento de vínculos distribuidos marca el archivo de destino con un identificador de objeto único (Id.) conocido como origen del vínculo. El archivo que hace referencia al archivo de destino (conocido como el cliente de vínculo) también almacena información sobre el Id. de objeto internamente. El seguimiento de vínculos distribuidos puede utilizar este Id. de objeto para buscar el archivo de origen del vínculo en los siguientes escenarios:
  
-   Cuando se cambia el nombre del archivo de origen del vínculo.
  
-   Cuando el archivo de origen del vínculo se ha movido a otra carpeta del mismo volumen o a otro volumen del mismo equipo.
  
-   Cuando el archivo de origen del vínculo se ha movido a otro equipo de la red.
  
    **Nota**: a menos que el equipo se encuentre en un dominio en el que esté disponible el servicio **Servidor de seguimiento de vínculos distribuidos**, este método de seguimiento de vínculos resulta menos confiable con el tiempo.
  
-   Cuando se cambia el nombre de la carpeta de red compartida que contiene el archivo de origen del vínculo.
  
En un dominio de Windows 2000 o Windows Server 2003 en el que esté disponible el servicio **Servidor de seguimiento de vínculos distribuidos**, el archivo de origen del vínculo se puede encontrar en los siguientes escenarios:
  
-   Cuando se cambia el nombre del equipo que contiene el archivo de origen del vínculo.
  
-   Cuando el volumen que contiene el archivo de origen del vínculo se ha movido a otro equipo del mismo dominio.
  
Los escenarios relacionados con el servicio **Servidor de seguimiento de vínculos distribuidos** requieren que el equipo cliente (en el que se ejecuta el servicio **Cliente de seguimiento de vínculos distribuidos**) tenga establecida la directiva de sistema **DLT\_AllowDomainMode**, para clientes que ejecutan Windows XP con SP1 o SP2. En todos los escenarios mencionados, el archivo de origen del vínculo deberá encontrarse en un volumen de NTFS que ejecute Windows 2000, Windows XP o la familia Windows Server 2003. Los volúmenes de NTFS no podrán estar en medios extraíbles.
  
**Nota**: el servicio **Cliente de seguimiento de vínculos distribuidos** controla la actividad en los volúmenes de NTFS y almacena la información de mantenimiento en un archivo denominado Tracking.log, que se ubica en una carpeta oculta denominada System Volume Information en la raíz de cada volumen. Esta carpeta está protegida por permisos que sólo permiten al equipo tener acceso a ella. Asimismo, otros servicios de Windows utilizan esta carpeta; por ejemplo, el **Servicio de Index Server**.
  
Si se detiene el servicio **Cliente de seguimiento de vínculos distribuidos**, los vínculos a contenido del equipo no se conservarán, ni se podrá realizar su seguimiento.
  
#### Servidor de seguimiento de vínculos distribuidos
  
El servicio del sistema **Servidor de seguimiento de vínculos distribuidos** almacena información de tal forma que los archivos movidos entre volúmenes se pueden controlar en cada volumen del dominio. Cuando está habilitado,este servicio se ejecuta en todos los controladores de dominio de un dominio. El serviciohace un seguimiento de los documentos vinculados que se han movido a una ubicación de otro volumen de NTFS del mismo dominio.
  
Este servicioestá deshabilitado de forma predeterminada. Si lo habilita, deberá hacerlo en todos los controladores de dominio de un dominio. Si el servicioestá habilitado en un controlador de dominio que se ha actualizado a una versión más reciente de Windows Server, se deberá volver a habilitar manualmente.
  
Si este servicioestá habilitado, se deberá habilitar la directiva de sistema **DLT\_AllowDomainMode** con el fin de que lo puedan utilizar los equipos cliente Windows XP. Si está habilitadoy lo deshabilita, deberá depurar las entradas de éste en Active Directory. Para obtener más información, consulte el artículo de Microsoft Knowledge Base “[Distributed Link Tracking on Windows–based domain controllers](http://support.microsoft.com/kb/312403/)” en http://support.microsoft.com/kb/312403/.
  
Si se detiene o deshabilita este servicio, los vínculos que mantiene el servicio **Cliente de seguimiento de vínculos distribuidos** se volverán menos confiables.
  
En Windows Server 2003, este serviciose instala de forma predeterminada, pero está deshabilitado.
  
#### Coordinador de transacciones distribuidas
  
El servicio **Coordinador de transacciones distribuidas** coordina las transacciones que se distribuyen entre varios equipos o administradores de recursos, como bases de datos, colas de mensajes, sistemas de archivos u otros administradores de recursos basados en transacciones. Este servicio es necesario si se van a configurar componentes transaccionales a través de COM+. También es necesario para las colas transaccionales de las operaciones de Message Queue Server (MSMQ) y de SQL Server que abarcan varios equipos.
  
El servicio **Coordinador de transacciones distribuidas** se instala y activa de forma predeterminada. Si se detiene, las transacciones que utilizan este servicio no se ejecutarán. Las instalaciones en clúster de Microsoft Exchange, SQL Server u otras aplicaciones que utilizan los servicios de transacción pueden verse afectadas si este servicio se detiene.
  
#### Cliente DNS
  
El servicio **Cliente DNS** resuelve y almacena en caché nombres DNS para el equipo. Este serviciodebe ejecutarse en todos los equipos que lleven a cabo la resolución de nombres DNS. La resolución de nombres DNS se necesita para ubicar a los controladores de dominio en dominios de Active Directory. El servicio **Cliente DNS** se necesita también para habilitar la ubicación de los dispositivos que se identifican a través de la resolución de nombre DNS.
  
El servicio **Cliente DNS** que se ejecuta en Windows Server 2003 implementa las características siguientes:
  
-   **Almacenamiento en caché para todo el sistema**. se agregan a la caché del cliente registros de recursos (RR) desde las respuestas a consultas a medida que las aplicaciones consultan a los servidores DNS. Esta información se almacena en caché durante un tiempo de vida (TTL) específico y se puede volver a utilizar para responder a consultas posteriores.
  
-   **Compatibilidad para almacenamiento en caché negativo compatible con RFC**. Además de almacenar en caché las respuestas positivas a consultas de los servidores DNS (que contienen información de registros de recursos en las respuestas contestadas) el servicio **Cliente DNS** también almacena en caché las respuestas negativas a las consultas.
  
    Una respuesta negativa se produce cuando no existe un registro de recursos para el nombre consultado. El almacenamiento en caché negativo evita que se repitan más consultas de nombres que no existen, lo que podría tener efectos negativos en el rendimiento del equipo cliente. Todas las informaciones de consultas negativas que se almacenan en caché se mantienen durante un período de tiempo inferior al de la información de consultas positivas; de forma predeterminada, no más de 5 minutos. Esta configuración evita que la información de consultas negativas caducada se guarde continuamente en caché si los registros pasan a estar disponibles posteriormente.
  
-   **Anulación de servidores DNS que no responden.** El servicio **Cliente DNS** utiliza una lista de búsqueda de servidor que se ordena según preferencias. Esta lista contiene todos los servidores DNS preferidos y alternativos configurados para cada una de las conexiones de red activas en el equipo. Windows Server 2003 reorganiza estas listas conforme a los siguientes criterios:
  
    -   Se otorga mayor prioridad a los servidores DNS preferidos.
  
    -   Si no hay ninguno disponible, se utilizarán los servidores DNS alternativos.
  
    -   Los servidores que no responden se quitan temporalmente de estas listas.
  
Si el servicio **Cliente DNS** se detiene, el equipo no será capaz de resolver los nombres DNS ni localizar controladores de dominio de Active Directory, y es probable que los usuarios no puedan iniciar sesión en el equipo.
  
#### Servidor DNS
  
El **Servidor DNS** permite la resolución de nombres DNS. Contesta las solicitudes de consultas y actualización para nombres DNS. Los servidores DNS se necesitan para localizar dispositivos identificados por sus nombres DNS y para localizar controladores de dominio en Active Directory.
  
Si detiene o deshabilita el servicio del sistema **Servidor DNS**, no se realizarán actualizaciones de DNS. No es necesario que el servicio **Servidor DNS** se ejecute en cada equipo. Sin embargo, si no existe un servidor DNS para una parte del espacio de nombres de DNS, la búsqueda de los dispositivos mediante nombres DNS en ella dará error. Si no existe un servidor DNS para el espacio de nombres de DNS que se utilice para nombrar los dominios de Active Directory, no se podrán localizar los controladores de dominio de ese dominio.
  
El **servicio del servidor DNS** sólo se instala y activa si configura un equipo Windows Server 2003 como servidor DNS.
  
#### Servicio de informe de errores
  
El **Servicio de informe de errores** recopila, almacena e informa a Microsoft de errores y cierres de aplicación inesperados. Autoriza también los informes de errores en servicios y aplicaciones que se ejecutan en entornos no estándar. Este servicio proporciona a los grupos de productos de Microsoft información eficiente y eficaz para depurar errores en controladores y aplicaciones.
  
Puede configurar el servicio de forma que envíe información sobre errores específicos de Microsoft y genere informes sobre errores del sistema operativo, de componentes de Windows o de programa. Un error del sistema operativo hará que el equipo muestre una pantalla de detención con códigos de error. Un error de programa o componente hará que dicho programa o componente deje de funcionar.
  
Si dispone de conexión a Internet, podrá notificar estos errores directamente a Microsoft. Puede configurar el informe de errores para que responda a errores de programa de uno de los siguientes modos: en cuanto se produce un error, el cuadro de diálogo **Informe de errores** puede solicitar al usuario que notifique el error a Microsoft, o bien,solicitar al administrador que notifique el error a Microsoft en la próxima ocasión en que éste inicie sesión.
  
Windows trata los errores y apagados no previstos del sistema operativo de forma diferente a los errores de programa. Cuando se producen, Windows escribe la información de error en un archivo de registro. La siguiente vez que un administrador inicia sesión, el cuadro de diálogo **Informe de errores** le insta a que notifique el error. Cuando se envía un informe de errores a Microsoft a través de Internet, se proporciona información técnica que la gente de Microsoft utiliza para mejorar las próximas versiones del producto. Estos datos se usan únicamente para el control de calidad y no para realizar un seguimiento de los usuarios o instalaciones con fines comerciales o publicitarios. Si hay información disponible para ayudar a solucionar el problema, Windows muestra un nuevo cuadro de diálogo **Informe de errores**, que contiene un vínculo a dicha información.
  
De modo alternativo, si la organización tiene configurada Directiva de grupo, los administradores del departamento de TI podrán utilizar Informe de errores corporativos para recopilar y notificar sólo los errores que consideren importantes. Para configurar Informe de errores corporativos en las estaciones de trabajo y servidores, los administradores pueden habilitar la directiva Informar de errores y configurar la Ruta de acceso al archivo de carga corporativa en el servidor de archivos local en el que está instalada la herramienta Informe de errores corporativos. Cuando se producen errores, la información se redirige automáticamente a este servidor de archivos. Los administradores pueden entonces revisar la información de errores, identificar los datos relevantes y enviarlos a Microsoft con la herramienta Informe de errores corporativos. Esta herramienta se puede descargar del sitio web del [kit de recursos de Office XP](http://www.microsoft.com/office/ork/xp/default.htm) en www.microsoft.com/office/ork/xp/default.htm.
  
Si se detiene el **Servicio de informe de errores**, no se llevará a cabo el informe de errores. Si se habilita el parámetro **Mostrar notificación de errores** en el cuadro de diálogo **Informe de errores**, los usuarios seguirán viendo un mensaje que indica que ha ocurrido un problema, pero no dispondrán de la opción de enviar esta información a Microsoft o a un recurso compartido de la red local. Este servicio se instala y se ejecuta de forma predeterminada.
  
#### Registro de eventos
  
El servicio del **Registro de eventos** permite visualizar los mensajes del registro de eventos emitidos por programas y componentes basados en Windows en el Visor de eventos. Estos mensajes del registro de eventos contienen información que puede ayudar a diagnosticar problemas con las aplicaciones, servicios y con el sistema operativo. Los registros se pueden consultar a través de las interfaces de programación de aplicaciones (API) del Registro de eventos o el complemento Visor de eventos de MMC.
  
De forma predeterminada, un equipo que ejecute un sistema operativo de la familia Windows Server 2003 registra los eventos en diferentes tres tipos de registros:
  
-   **Registro de aplicaciones**. Este registro lleva un seguimiento de los eventos de los programas de las aplicaciones. Por ejemplo, un programa de base de datos podría registrar un error de archivo en el registro de aplicaciones. Los desarrolladores de programas deciden qué eventos se van a registrar.
  
-   **Registro de seguridad**. Registra eventos como intentos de inicio de sesión válidos y no válidos, así como eventos relacionados con el uso de los recursos tales como la creación, apertura o eliminación de archivos u otros objetos. Por ejemplo, si habilita la auditoría de inicio de sesión, los intentos para iniciar sesión en el equipo se registran en el registro de seguridad.
  
-   **Registro del sistema**. Este registro lleva un seguimiento de los eventos relacionados con los componentes de Windows. Por ejemplo, registra si no se puede cargar un controlador u otro componente del sistema durante el inicio. Los tipos de eventos que registran los componentes del equipo de Windows vienen predeterminados por el servidor.  
  
Un equipo con Windows Server 2003 configurado como controlador de dominio registra los eventos en dos registros adicionales:
  
-   **Registro de servicio de directorio**. Este registro lleva un seguimiento de los eventos relacionados con Active Directory. Por ejemplo, los problemas de conexión entre el servidor y el catálogo global.
  
-   **Registro de servicio de replicación de archivos**. Este registro lleva un seguimiento de los eventos del servicio de réplica de archivo de Windows. Por ejemplo, los eventos y errores de replicación de archivos que tienen lugar mientras se actualizan controladores de dominio con información sobre los cambios del volumen del sistema.
  
Un equipo basado en Windows y que está configurado como servidor DNS registra eventos en un registro adicional:
  
-   **Registro de servidor DNS**. Contiene eventos registrados por el servicio DNS de Windows.
  
No puede detener el servicio de **registro de eventos**. Si se deshabilita, no se podrá realizar un seguimiento de los eventos, lo que reducirá significativamente la capacidad de diagnosticar correctamente los problemas del equipo. Además, no se auditarán los eventos de seguridad y no se podrán consultar registros de eventos anteriores a través del complemento Visor de eventos de MMC.
  
#### Compatibilidad de conmutación rápida de usuarios
  
El servicio **Compatibilidad de conmutación rápida de usuarios** proporciona la administración para las aplicaciones que requieren ayuda en un entorno multiusuario. La función de conmutación rápida de usuarios en Windows XP permite que varios usuarios que hayan iniciado una sesión en el equipo al mismo tiempo puedan alternar fácilmente entre sesiones. No necesitan cerrar las aplicaciones y cerrar la sesión.
  
Muchos programas no se diseñaron para ejecutarse en un entorno multiusuario y pueden experimentar problemas cuando varios usuarios inician una sesión en el equipo. El servicio **Compatibilidad de conmutación rápida de usuarios** realiza una de cuatro acciones diferentes cuando un programa específico que causa problemas está en el uso y cuando está activada la conmutación rápida de usuarios:
  
-   Con programas del tipo 1, el servicio permitirá al usuario cerrar la primera instancia de estos programas cuando se inicia una segunda instancia. Esta acción es la menos molesta, pero requiere que el usuario tenga privilegios administrativos.
  
-   Con los programas del tipo 2, el servicio los cierra cuando la sesión se desconecta (por una acción de "cambio de usuario" o cuando el equipo vuelve a la pantalla de bienvenida después de que se desactiva el protector de pantalla).
  
-   Con los programas del tipo 3, el servicio los cierra cuando la sesión se desconecta y los vuelve a iniciar cuando el usuario se vuelve a conectar a la sesión. Esta opción es buena para los programas que utilizan recursos que no se comparten fácilmente a través de varias sesiones, como los puertos COM.
  
-   Con los programas del tipo 4, el servicio los cierra cuando otro usuario inicia sesión. Esta opción se aplica a los programas que pueden ser molestos para el equipo pero no se tienen que cerrar al volver a la pantalla de bienvenida. El programa continuará ejecutándose cuando el usuario se desconecte y sólo se cerrará cuando otro usuario inicie sesión.
  
Si deshabilita el servicio **Compatibilidad de conmutación rápida de usuarios**, puede que algunas aplicaciones no trabajen correctamente en un equipo que tiene activada la función de conmutación rápida de usuarios.
  
#### Servicio de fax
  
El **Servicio de fax**, compatible con la interfaz de programación de aplicaciones de telefonía (TAPI), ofrece capacidades de fax desde el equipo de los usuarios. El **Servicio de fax** permite a los usuarios enviar y recibir faxes desde las aplicaciones de escritorio a través de un dispositivo de fax local o de red compartida. Entre sus ventajas se incluyen las siguientes:
  
-   Envío y recepción de faxes
  
-   Seguimiento y control de la actividad del fax
  
-   Enrutamiento de fax entrante
  
-   Administración de la configuración del servidor y el dispositivo
  
-   Archivado de faxes enviados
  
Si la cola de impresión o el servicio de telefonía están deshabilitados, el **servicio de fax** no se iniciará correctamente. Si se detiene este servicio, los usuarios no podrán enviar ni recibir faxes. El **servicio de fax** se interrumpe cuando no hay actividad del fax y se reinicia según sea necesario.
  
#### Replicación de archivos
  
El servicio **Réplica de archivos** permite que los archivos se copien automáticamente y almacenen simultáneamente en varios servidores. El Servicio de replicación de archivos (FRS) es un servicio automático en Windows 2000 y en la familia Microsoft Windows Server 2003 cuya función es replicar el contenido del volumen de sistema (SYSVOL) entre todos los controladores de dominio en un dominio. También se puede configurar para que replique los archivos entre destinos alternativos asociados al DFS de tolerancia a errores.
  
Si se detiene este servicio, no tendrá lugar la **replicación de archivos** y no se sincronizarán los datos del servidor. Además, la capacidad de funcionamiento de un controlador de dominio podría ser afectada gravemente si este servicio se detiene. El servicio **Réplica de archivos** se instala de forma predeterminada en Windows Server 2003, pero su estado de inicio se configura como **Manual.**
  
#### Servidor de archivos para Macintosh
  
El servicio **Servidor de archivos para Macintosh** permite a los usuarios de Macintosh almacenar y tener acceso a archivos en un equipo con Windows Server 2003. Si desactiva este servicio, los equipos cliente de Macintosh no serán capaces de almacenar y tener acceso a los archivos en equipos con Windows Server 2003. Este servicio no se instala ni se inicia de forma predeterminada.
  
#### Servicio de publicación FTP
  
El **Servicio de publicación FTP** permite la conectividad y la administración de FTP a través del complemento Microsoft Internet Information Server (IIS). Las características incluyen la capacidad de regular el ancho de banda, las cuentas de seguridad y el registro extensible. Este servicio incluye la nueva característica Aislamiento de usuario FTP, que permite a los usuarios obtener acceso sólo a sus archivos en un sitio FTP. Asimismo, se ofrece una compatibilidad internacional mejorada.
  
Si se detiene el **Servicio de publicación FTP**, el servidor no podrá funcionar como servidor FTP. Este servicio no se instala de forma predeterminada.
  
#### Ayuda y soporte técnico
  
El servicio **Ayuda y soporte técnico** permite que la aplicación Centro de ayuda y soporte técnico se ejecute en los equipos de los usuarios, da soporte a la aplicación y activa la comunicación entre la aplicación cliente y los datos de ayuda. Este servicio proporciona acceso a almacenes y servicios como la base de datos de taxonomía, que contiene metadatos e información sobre los temas de ayuda, el marco de automatización del soporte, que permite la recopilación de datos para proveedores de soporte técnico registrados, información de preferencias e historial del usuario y el administrador de motor de búsqueda. Cuando se interactúa con características de Centro de ayuda y soporte técnico como la búsqueda, el índice o el contenido, el servicio permite la transacción de los datos de todas estas características.
  
Si el servicio **Ayuda y soporte técnico** se configura como **Manual**, el servicio se iniciará si un usuario tiene acceso al Centro de ayuda y soporte técnico desde el escritorio. Si detiene o deshabilita este servicio, el Centro de ayuda y soporte técnico básicamente dejará de funcionar y los usuarios recibirán el siguiente mensaje:
  
Windows no puede abrir Ayuda y soporte técnico porque el servicio del sistema no se está ejecutando.
  
Los usuarios podrán tener acceso a algunos temas de alto nivel que quizás se guarden en el caché del equipo local, pero en la mayor parte de las funciones de la aplicación Centro de ayuda y soporte técnico (incluida la asistencia remota) no pueden funcionar si el servicio **Ayuda y soporte técnico** no está habilitado. Sin embargo, el usuario aún podrá visualizar los archivos \*.HLP y \*.CHM, ubicados en la carpeta **Windows\\Help**. El servicio **Ayuda y soporte técnico** se instala y se inicia automáticamente de forma predeterminada en Windows XP y Windows Server 2003.
  
#### SSL de HTTP
  
El servicio **SSL de HTTP** habilita IIS para que realice funciones de Secure Sockets Layer (SSL). SSL es un estándar abierto que establece canales de comunicaciones seguros y evita que se pueda interceptar información relevante como, por ejemplo, los números de las tarjetas de crédito. Permite principalmente realizar transacciones financieras electrónicas seguras en Internet, si bien está diseñado para operar también en otros servicios web.
  
Si se detiene el servicio **SSL de HTTP**, IIS no podrá realizar las funciones de SSL. Este servicio se instala al instalar IIS y no está presente ni activo de otro modo.
  
#### Acceso a dispositivo de interfaz humana
  
El servicio **Acceso a dispositivo de interfaz humana** permite el acceso de entrada genérico a dispositivos USB como teclados y mouse. El servicio activa y controla el uso de botones de acceso directo predefinidos en teclados, controles remotos y otros dispositivos multimedia. Este servicio se instala y inicia de forma predeterminada en equipos con Windows XP y Windows Server 2003.
  
Si se detiene este servicio, dejarán de funcionar los botones de acceso directo controlados por el mismo. Por ejemplo, los botones de acceso directo para retroceso, avance, volumen, pista anterior, etc. en teclados USB y los botones de volumen en altavoces USB no funcionarán.
  
#### Acceso a base de datos IAS Jet
  
El servicio **Acceso a base de datos IAS Jet** utiliza el protocolo Servicio de usuario de acceso telefónico de autenticación remota (RADIUS) para ofrecer servicios de autenticación, autorización y auditoría. Sólo está disponible en versiones de 64 bits de Windows. Con el Servicio de autenticación de Internet (IAS) puede administrar centralmente la autenticación, autorización y auditoría de los usuarios. También puede utilizar IAS para autenticar a los usuarios en función de controladores de dominio que ejecuten Windows NT® 4.0, Windows 2000 o Windows Server 2003. IAS funciona correctamente tanto en redes homogéneas como heterogéneas.
  
Este servicio se puede utilizar como proxy RADIUS para enrutar mensajes RADIUS entre clientes RADIUS (servidores de acceso) y servidores RADIUS, que realizan la auditoría, la autorización y la autenticación de los usuarios en los intentos de conexión. Cuando se utiliza como proxy RADIUS, IAS es un punto de enrutamiento o conmutación central a través del cual se transfieren mensajes de auditoría y acceso RADIUS. IAS incluye la información en un registro de auditoría relativo a los mensajes que se han reenviado.
  
Una infraestructura de auditoría, autorización y autenticación RADIUS consta de los siguientes componentes:
  
Existen dos bases de datos IAS Jet. Ias.mdb se utiliza para configurar IAS, y Dnary.mdb, que se emplea para validar el diccionario que IAS usa para realizar un seguimiento de los atributos específicos de proveedor de servidores de acceso de red compatibles con RADIUS. No modifique las bases de datos Jet.
  
Si se detiene el servicio del **Acceso a base de datos IAS Jet**, no estará disponible el acceso de red remoto que requiere la autenticación de usuarios. Por ejemplo, no funcionarán el acceso remoto telefónico, de VPN, de LAN inalámbrica (802.1x) ni de LAN Ethernet 802.1x. Si deshabilita este servicio, no se podrá iniciar ni el **Enrutamiento y acceso remoto (RRAS)** ni **IAS**. Tampoco se podrán administrar RRAS o IAS de forma local o remota. Este servicio no se instala de forma predeterminada en ninguna versión de Windows; sólo está disponible en las versiones basadas en Itanium la familia Windows Server 2003.
  
#### Servicio de administración IIS
  
El **Servicio de administración de IIS** permite la administración de componentes IIS como FTP, grupos de aplicaciones, sitios web, ampliaciones de servicios web y servidores virtuales de Protocolo de transferencia de noticias a través de la red (NNTP) y Protocolo simple de transferencia de correo (SMTP). Si detiene o deshabilita este servicio, no podrá ejecutar sitios web, FTP, NNTP o SMTP.
  
En Windows 2000, se instalan de forma predeterminada el **Servicio de administración IIS** y otros servicios relacionados. En lo que respecta a la familia Windows Server 2003, deberá instalar los componentes de IIS desde Agregar o quitar componentes de Windows o Configurar el servidor.
  
#### Servicio COM de grabación de CD de IMAPI
  
El **Servicio COM de grabación de CD de IMAPI** administra la creación de CD usando la interfaz de programación de aplicaciones de grabación de imágenes (IMAPI); también lleva a cabo escrituras de CD grabables (CD-R) cuando las solicita el usuario desde el Explorador de Windows, el Reproductor de Windows Media&\#174; o aplicaciones de otros fabricantes que utilicen esta API. IMAPI permite que una aplicación organice y grabe un archivo de audio sencillo o imágenes de datos en dispositivos de CD-R y CD regrabable (CD-RW). La API admite audio Redbook y formatos de disco de datos Joliet e ISO 9660. La arquitectura permite ampliar en un futuro el conjunto de formatos compatibles.
  
Si se detiene o deshabilita el **Servicio COM de grabación de CD de IMAPI**, su equipo no podrá grabar CD con las funciones integradas de Windows XP y Windows Server 2003. Si desactiva este servicio y utiliza una aplicación de CD-RW de terceros, su capacidad de grabar CD no se verá afectada (si el software de terceros no depende del servicio). Si el servicio se inicia una vez iniciada la sesión, deberá cerrarla y volver a abrirla para poder escribir datos en el CD-R desde el dispositivo de CD-R mediante el Explorador de Windows. Este servicio se instala de forma predeterminada en Windows XP, pero no se inicia hasta que un usuario solicite la escritura CD-R a través del Explorador de Windows. Se instala pero está deshabilitado de forma predeterminada en equipos con Windows Server 2003.
  
#### Servicio de Index Server
  
El **Servicio de Index Server** genera un índice del contenido y las propiedades de archivos en equipos locales y remotos y ofrece acceso inmediato a archivos a través de un lenguaje de consulta flexible. Asimismo, **este servicio** permite la capacidad de búsquedas rápidas de documentos en equipos locales y remotos y proporciona un índice de búsqueda del contenido compartido en el web. También genera índices de todo tipo de información textual en archivos y documentos. Tras completarse la generación del índice inicial, el **Servicio de Index Server** mantiene sus índices cada vez que se crea, modifica o elimina un archivo.
  
Esta generación inicial del índice puede requerir gran cantidad de recursos. De forma predeterminada, el **Servicio de Index Server** se establece para su inicio manual. Cuando el servicio está activo, indexará sólo cuando el equipo esté inactivo, aunque puede utilizar el complemento de índice MMC para configurar el servicio de modo que funcione cuando el equipo no está inactivo. MMC también le permite la optimización de la configuración de la asignación de recursos del servicio para los patrones de uso de la indización o las consultas.
  
Si detiene el **Servicio de Index Server**, se ralentizarán las búsquedas de texto.
  
#### Monitor de infrarrojos
  
El servicio del sistema **Monitor de infrarrojos** permite que se compartan archivos e imágenes mediante el uso de conexiones de infrarrojos. Este servicio sólo se instala de forma predeterminada en Windows XP si se detecta un dispositivo de infrarrojos durante la instalación del sistema operativo. No está disponible en las ediciones Windows Server 2003 Web, Enterprise o Datacenter Server.
  
Si se detiene el servicio **Monitor de infrarrojos**, no se podrán compartir archivos e imágenes por medio de conexiones de infrarrojos.
  
#### Servicio de autenticación de Internet
  
El **Servicio de autenticación de Internet** (IAS) centraliza la autenticación, la autorización, la auditoría y la administración de las cuentas de los usuarios que se conectan a una red, ya sea LAN o remota, mediante un equipo VPN, un Equipo de acceso remoto (RAS) o puntos de acceso inalámbricos 802.1x y de conmutadores Ethernet.
  
**IAS** implementa el protocolo RADIUS estándar de IETF, que permite equipos de acceso a red heterogéneos. Si se deshabilita o se detiene **IAS**, se produce una conmutación por error de las solicitudes de autenticación a un servidor IAS de copia de seguridad, si hubiera alguno disponible. Si no hay ninguno, los usuarios no se podrán conectar a la red. Este servicio se debe instalar manualmente y sólo está disponible en miembros de la familia Windows Server 2003.
  
#### Mensajería interna
  
El servicio de **Mensajería interna** permite el intercambio de mensajes entre equipos que ejecuten Windows Server. Este servicio se utiliza para la replicación basada en correo entre sitios. Active Directory proporciona compatibilidad para la replicación entre sitios a través de transporte SMTP sobre IP. El servicio SMTP, que es un componente de IIS, se encarga de proporcionar compatibilidad con **SMTP.**
  
El conjunto de transportes utilizados para la comunicación entre sitios debe ser extensible. Por lo tanto, cada transporte se define en una archivo de biblioteca de vínculos dinámicos (DLL) independiente. Estos archivos DLL complementarios se cargan en el servicio **Mensajería interna**, que se ejecuta en todos los controladores de dominio capaces de establecer las comunicaciones entre sitios. El **servicio** dirige las solicitudes de envío y recepción de mensajes a los archivos DLL complementarios de transporte adecuados que, por su parte, enrutan los mensajes al servicio **Mensajería interna** del equipo de destino.
  
Si se detiene el servicio **Mensajería interna**, no se intercambiarán mensajes, no funcionará la replicación de mensajería interna ni se calculará la información sobre enrutamiento de sitios para otros servicios. Este servicio se instala de forma predeterminada en equipos Windows Server 2003, pero se deshabilita hasta que el servidor sea promovido a la función de controlador de dominio.
  
#### Servicio de ayuda de IPv6
  
El **Servicio de ayuda de IPv6** ofrece conectividad del protocolo de Internet versión 6 (IPv6) en una red del protocolo de Internet versión 4 (IPv4). IPv6 es un nuevo paquete de protocolos estándar para la capa de red de Internet. Está diseñado para solucionar gran parte de los problemas de IPv4, en lo que respecta a cómo abordar la reducción de direcciones, la seguridad, la configuración automática y la extensibilidad. Este servicio, que se conoce a menudo como "6to4", permite la comunicación de hosts y sitios habilitados para IPv6 al utilizar IPv6 sobre una infraestructura IPv4, por ejemplo, Internet. Los hosts y sitios IPv6 pueden utilizar Internet y su prefijo de dirección 6to4 para comunicarse. No necesitan obtener un prefijo de dirección global IPv6 de un proveedor de servicios de Internet (ISP) y se conectan a 6bone, la parte activada para IPv6 de Internet.
  
6to4 es una técnica de túnel que se describe en RFC 3056. Los hosts 6to4 no requieren una configuración manual y crean direcciones 6to4 mediante el uso de la configuración automática estándar. 6to4 utiliza el prefijo de dirección global de 2002:WWXX:YYZZ::/48, donde WWXX:YYZZ es la representación hexadecimal dividida por dos puntos de una dirección IPv4 pública (w.x.y.z) que se asigna a un sitio o host, lo que también se conoce como la parte NLA (Next Level Aggregator) de una dirección 6to4.
  
Asimismo, el **Servicio de ayuda de IPv6** admite 6over4, también conocido como túnel de multidifusión IPv4, una técnica de túnel que se describe en RFC 2529. 6over4 permite que nodos IPv6 e IPv4 se comuniquen a través de IPv6 en una infraestructura IPv4. 6over4 utiliza la infraestructura IPv4 como un vínculo preparado para la multidifusión. Para que 6over4 funcione correctamente, la infraestructura IPv4 debe tener habilitada la multidifusión IPv4.
  
Si se detiene el **Servicio de ayuda de IPv6**, el equipo sólo dispondrá de conectividad IPv6 si se conecta a una red IPv6 nativa. Este servicio no se instala ni se activa de forma predeterminada.
  
#### Agente de directivas IPSec (Servicio IPSec)
  
El servicio **Agente de directivas IPSec (Servicio IPSec)** proporciona seguridad de un extremo a otro entre clientes y servidores en redes TCP/IP, administra la directiva IPSec, inicia el intercambio de claves de Internet (IKE) y coordina la configuración de la directiva IPSec con el controlador de seguridad IP. El servicio se controla a través de los comandos NET START o NET STOP.
  
IPSec opera en la capa IP y es transparente para otras aplicaciones y servicios de sistemas operativos. El servicio proporciona filtrado de paquetes y puede negociar seguridad entre equipos en redes IP. Puede configurar IPSec para proporcionar:
  
-   Filtrado de paquetes con acciones para permitir, bloquear o negociar la seguridad.
  
-   Comunicación IP segura y de confianza negociada. El protocolo IKE autentica tanto al remitente como al receptor de los paquetes de datos IP en función de la configuración de la directiva. La autenticación puede utilizar el protocolo de autenticación Kerberos, certificados digitales o una clave secreta compartida (contraseña). IKE genera de forma automática claves cifradas y asociaciones de seguridad IPSec.
  
-   Protección de paquetes IP con formatos IPSec seguros que proporcionan integridad cifrada, autenticidad y (opcionalmente) cifrado de paquetes IP.
  
-   Conexiones seguras de un extremo a otro con modo de transporte IPSec.
  
-   Túneles IP seguros utilizando el modo de túnel IPSec.
  
IPSec también proporciona seguridad para conexiones VPN de protocolo de túnel de capa dos (L2TP).
  
Si se detiene el **Agente de directivas IPSec (Servicio IPSec)**, se comprometerá la seguridad de TCP/IP entre clientes y servidores de la red. Este servicio se instala y se activa de forma predeterminada en equipos con Windows Server 2003 y Windows XP.
  
#### Centro de distribución de claves Kerberos
  
El servicio del **Centro de distribución de claves Kerberos** permite que los usuarios inicien una sesión en la red y se autentiquen utilizando el protocolo de autenticación Kerberos v5.
  
Como en otras implementaciones del protocolo Kerberos, el Centro de distribución de claves Kerberos (KDC) es un único proceso que ofrece dos servicios:
  
-   **Servicio de autenticación**. emite vales de concesión de vales (TGT) para la conexión al servicio de concesión de vales en su propio dominio o en cualquier otro dominio de confianza. Antes de que un equipo cliente pueda solicitar un vale a otro equipo, deberá solicitar un TGT al servicio de autenticación en su dominio de cuenta. El servicio de autenticación devuelve un TGT al servicio de concesión de vales en el dominio del equipo de destino. El TGT se puede seguir utilizando hasta que caduque, aunque el primer acceso a cualquier servicio de concesión de vales del dominio requiere siempre que el equipo cliente se pongan en contacto con el servicio de autenticación el su dominio de cuenta.
  
-   **Servicio de concesión de vales (TGS)**. emite vales para la conexión a equipos de su propio dominio. Cuando un equipo cliente desea obtener acceso a otro equipo, deberá solicitar un TGT y demandar un vale al equipo. El vale se puede seguir utilizando hasta que caduque, aunque el primer acceso a cualquier equipo requiere siempre ponerse en contacto con el servicio de concesión de vales en el dominio de cuenta del equipo de destino.
  
Si se detiene el servicio del **Centro de distribución de claves Kerberos**, los usuarios no podrán iniciar una sesión en la red ni obtener acceso a los recursos. Este servicio se instala en todos los equipos Windows Server 2003, pero sólo se ejecuta en controladores de dominio. Si deshabilita este servicio, los usuarios no podrán iniciar sesión en el dominio.
  
#### Servicio de registro de licencias
  
El **Servicio de registro de licencias** supervisa y registra la información de licencias de acceso a clientes. Trabaja con distintas partes del sistema operativo, como IIS, Servicios de Terminal Server, uso compartido de archivos e impresión y también con productos que no son parte del sistema operativo, como SQL Server o Microsoft Exchange Server.
  
Si se detiene o deshabilita el servicio **Servicio de registro de licencias**, se aplicarán las licencias, pero no se supervisarán. Este servicio se deshabilita de forma predeterminada en equipos con Windows Server 2003.
  
#### Administrador de discos lógicos
  
El servicio del **Administrador de discos lógicos** detecta y supervisa unidades de disco duro nuevas y envía información de volumen del disco al **Servicio del administrador de discos lógicos** para su configuración. Este servicio supervisa eventos Plug and Play para detectar unidades nuevas y utiliza un servicio de administrador y un servicio de vigilancia. No deshabilite el servicio si hay discos dinámicos en el equipo.
  
El servicio **Administrador de discos lógicos** se ejecuta de forma predeterminada en equipos con Windows Server 2003 y Windows XP. Si se detiene, el estado dinámico de disco y la información de configuración podrían pasar a ser obsoletos. Por ejemplo, no se detectarían las unidades de disco duro. El servicio de administrador y el servicio de vigilancia son básicamente un mismo componente. El servicio administrativo sólo se inicia cuando se configura una unidad o una partición, o cuando se detecta una unidad nueva.
  
#### Servicio del administrador de discos lógicos
  
El **Servicio del administrador de discos lógicos** realiza un servicio administrativo para solicitudes de administración de discos y configura las unidades de disco duro y los volúmenes. Sólo se inicia cuando se configura una unidad o una partición, o cuando se detecta una unidad nueva. No se inicia de forma predeterminada, sino que se activa cada vez que tiene lugar un cambio en la configuración de los discos dinámicos o cuando se abren el complemento Administración de discos MMC o la herramienta Diskpart.exe. Los cambios que pueden activar este servicio incluyen la conversión de un disco básico a dinámico, la recuperación de volúmenes de tolerancia a errores, el formateo de volúmenes o la modificación de un archivo de paginación.
  
El **Servicio del administrador de discos lógicos** sólo se ejecuta para procesos de configuración y detenciones. Si deshabilita este servicio, aparecerá el siguiente mensaje de error cada vez que se intente utilizar el complemento Administración de discos de MMC para configurar los discos:
  
No se puede conectar al servicio del administrador de discos lógicos
  
#### Administrador de depuración de equipos
  
El servicio **Administrador de depuración de equipos** administra la depuración local y remota de varias aplicaciones, como Microsoft Script Editor, varias versiones de la suite de Office y de Microsoft Visual Studio.
  
Si deshabilita el servicio **Administrador de depuración de equipos**, los intentos de depurar secuencias de comandos o procesos fallarán y mostrarán el mensaje de error siguiente:
  
No puede iniciarse la depuración. El servicio Administrador de depuración de equipos está deshabilitado.
  
Además, los usuarios no tendrán la oportunidad de depurar errores de secuencia de comandos en páginas web.
  
#### Servicios de Message Queue Server
  
Los **Servicios de Message Queue Server** son una herramienta de desarrollo e infraestructura de mensajería que permite crear aplicaciones de mensajería distribuidas para Windows. Estas aplicaciones pueden comunicarse en redes heterogéneas y enviar mensajes entre equipos que, temporalmente, no pueden conectarse entre sí. Este servicio ofrece la entrega de mensajes garantizada, un enrutamiento eficaz, seguridad y una mensajería basada en prioridades. Admite también la capacidad de enviar mensajes dentro de transacciones y proporciona a Microsoft Win32® y las API COM toda la funcionalidad de programación, incluida la administración.
  
La implementación de la funciones de lectura remota en la versión de Windows XP de **Servicios de Message Queue Server** permite a usuarios sin autenticación conectarse a colas. Un usuario malintencionado podría purgar una cola y crear una condición de denegación de servicio. Además, la lectura remota de datos de Servicios de Message Queue Server se transmite a través de la red en texto sin formato, lo que significa que un usuario malintencionado podría leerla y capturar datos de la red.
  
Para estas razones, Microsoft recomienda que no instale los **Servicios de Message Queue Server** en equipos con Windows XP que se exponen a redes que no son de confianza, como Internet. El servicio no se instala de forma predeterminada en Windows XP, así que la mayoría de las organizaciones ya deben estar protegidas contra esta vulnerabilidad.
  
Si se detiene el servicio **Servicios de Message Queue Server**, los mensajes distribuidos no estarán disponibles. Si deshabilita este servicio, cualquier otro servicio que dependa directamente del mismo no se podrá iniciar. Además, la funcionalidad **Componente en cola (QC) de COM+**, alguna funcionalidad de WMI y el servicio **Desencadenadores de Message Queue Server** se verán afectados. Este servicio no se instala de forma predeterminada en equipos con Windows Server 2003.
  
#### Compatibilidad de Message Queue Server con clientes de nivel inferior
  
El servicio **Message Queue Server con clientes de nivel inferior** proporciona acceso a Active Directory para clientes de Windows NT 4.0, Windows 9x y Windows 2000 que utilizan los **servicios de Message Queue Server** en controladores de dominio. Los **Servicios de Message Queue Server** utilizan opcionalmente información que se publica en Active Directory para obtener información de enrutamiento de objetos relacionados con la seguridad, tales como el destino de las claves públicas, y para saber más sobre las colas públicas. Si instala **Servicios de Message Queue Server** en modo de grupo de trabajo, en ningún momento podrá obtener acceso a Active Directory. Este servicio sólo es necesario en controladores de dominio de Windows Server 2003 que ejecutan los **servicios de Message Queue Server**.
  
Si se detiene el servicio **Compatibilidad de Message Queue Server con clientes de nivel inferior** en un controlador de dominio, las versiones del cliente MSMQ no podrán obtener servicios de Active Directory en el controlador de dominio especificado para el descubrimiento de colas públicas, el enrutamiento de mensajes y el reconocimiento de sitios. Este servicio no se instala de forma predeterminada en equipos con Windows Server 2003.
  
#### Desencadenadores de Message Queue Server
  
El servicio del sistema **Desencadenadores de Message Queue Server** ofrece la supervisión mediante reglas de los mensajes que llegan auna cola de **Message Queue Server**. Cuando se cumplen las condiciones de una regla, llama a un componente COM o a un programa ejecutable independiente para procesar el mensaje.
  
Este serviciose instala como parte integrante del servicio de **Message Queue Server**, que es un componente opcional de Windows, disponible en todas sus versiones excepto en Windows XP Home Edition.
  
Si se detiene el servicio de **Desencadenadores de Message Queue Server**, no podrá aplicar la supervisión mediante reglas ni llamar a programas para que procesen los mensajes de forma automática. Este servicio no se instala de forma predeterminada en equipos con Windows Server 2003.
  
#### Messenger
  
El servicio del sistema de **Mensajería** envía mensajes a usuarios, equipos, administradores y al Servicio de **alerta** y recibe mensajes de ellos. Este servicio no está relacionado con Windows Messenger, un servicio de mensajería instantánea disponible a través de MSN.
  
Si está deshabilitado,el equipo o los usuarios actualmente conectados no podrán enviar o recibir notificaciones a través del servicio de Mensajería. Además, los comandos de shell NET SEND y NET NAME dejarán de funcionar. Este servicio se instala pero se deshabilita de forma predeterminada en equipos con Windows Server 2003 y Windows XP.
  
#### Servicio Pop3 de Microsoft
  
El **Servicio Pop3 de Microsoft** ofrece servicios de transferencia y recuperación de correo electrónico. Los administradores pueden utilizarlo para almacenar y administrar las cuentas de correo electrónico en un servidor de correo. Cuando se instala el **Servicio POP3 de Microsoft** en un servidor de correo, los usuarios pueden conectarse a ese servidor y recuperar mensajes de correo electrónico con un cliente de correo electrónico compatible con el protocolo POP2, por ejemplo Microsoft Outlook®. El **Servicio POP3 de Microsoft** trabaja en combinación con el **Servicio SMTP**, que permite usuarios para enviar correo electrónico saliente.
  
Este servicioes el mecanismo que permite a los usuarios recuperar sus mensajes de correo electrónico de un servidor de correo. Los equipos del remitente y el destinatario se conectan a Internet a través de sus proveedores de servicios de Internet respectivos. Cuando el remitente utiliza un cliente de correo electrónico para enviar un mensaje, el **Servicio SMTP** transfiere el mensaje al proveedor de servicios de Internet del remitente. El mensaje se dirige entonces a Internet y se retransmite a través de varios servidores intermedios. Cuando el mensaje llega al proveedor de servicios de Internet del destinatario, se coloca en su buzón de correo. Cuando el equipo del destinatario se conecte a su ISP, éste transferirá el mensaje al cliente de correo electrónico del destinatario del equipo local según el protocolo POP3.
  
Si se detiene el **Servicio Pop3 de Microsoft**, dejarán de funcionar los servicios de transferencia y recuperación de correo electrónico. Este servicio se debe instalar manualmente en equipos con Windows Server 2003.
  
#### Proveedor de instantáneas de software de Microsoft
  
El servicio **Proveedor de instantáneas de software de Microsoft** administra instantáneas basadas en software tomadas por el **Servicio de instantáneas de volumen**. Una instantánea es una copia de un volumen de disco que representa un determinado punto en el tiempo coherente y de sólo lectura de dicho volumen. Este punto o momento permanece constante y permite que una aplicación, como un programa de copia de seguridad, copie datos de la instantánea en cinta.
  
Existen dos tipos generales de instantáneas:
  
-   **De hardware**. Las instantáneas de hardware son un reflejo de dos o más discos divididos en volúmenes independientes. Uno de los dos sigue siendo el espacio de trabajo, mientras que el otro se puede montar por separado.
  
-   **De software**. Las instantáneas de software utilizan un esquema de copia por escritura para copiar todos los sectores de un volumen que cambia con el tiempo a un área diferencial en el disco. Una vez que se monta la instantánea, todos los sectores no modificados se leen en el volumen original y los modificados se leen en el área diferencial.
  
Las instantáneas pueden resolver tres retos clásicos asociados con la copia de seguridad de datos:
  
-   La necesidad de realizar copias de seguridad de archivos abiertos para acceso exclusivo. La copia de seguridad de un archivo abierto es un desafío, porque es probable que esté en un estado de cambio. Sin una instantánea ni forma de suspender la aplicación, las copias de seguridad se dañan frecuentemente.
  
-   La necesidad de mantener la disponibilidad del equipo durante la instantánea.
  
-   Uso de los mismos canales de comunicación como instantáneas, a fin de facilitar la transferencia de información entre la aplicación y las herramientas de copia de seguridad.
  
La plataforma para instantáneas está formada por los siguientes elementos:
  
-   Un conjunto de API de instantánea, que maneja la sincronización de aplicaciones. Esta sincronización de aplicaciones garantiza que una instantánea esté correcta, puesto que los datos de las aplicaciones están en un estado conocido como válido. Estas API proporcionan las funciones necesarias para los proveedores de instantáneas de complementos y la coordinación de instantáneas multivolumen.
  
-   Un controlador de dispositivo de instantáneas que copia los sectores viejos a un "archivo de diferencias" cuando se reemplazan por primera vez, para proporcionar instantáneas de volumen para cualquier volumen montado de forma local. El archivo de diferencias se coloca sobre el volumen actual para sintetizar el volumen de instantánea.
  
-   Compatibilidad en las comunidades de desarrollo de software para las API de proveedor y sincronización.
  
Si el servicio del sistema **Proveedor de instantáneas de software de Microsoft** se detiene, las instantáneas de volumen basadas en software no se podrán administrar, lo que podría causar que la copia de seguridad de Windows falle. Este servicio se instala de forma predeterminada en Windows Server 2003, pero sólo se ejecuta cuando se solicita.
  
#### MSSQL$UDDI
  
El servicio **MSSQL$UDDI** se instala a la par que la función Universal Description, Discovery, and Integration (UDDI) de la familia Windows Server 2003. (Esta función ofrece capacidades UDDI a una organización). Cuando se instala este servicio, una instancia de base de datos de SQL Server se instala también. Esta instancia administra todos los archivos que componen las bases de datos usadas por el servicio y procesa todas las instrucciones Transact-SQL que se envían de aplicaciones cliente de SQL Server. El servicio **MSSQL$UDDI** asigna los recursos del equipo con eficacia entre varios usuarios simultáneos. Asimismo, fuerza las reglas empresariales definidas en los procedimientos almacenados y desencadenadores, asegura la coherencia de los datos y evita problemas lógicos, como que haya dos personas intentando actualizar los mismos datos a la vez.
  
UDDI es una especificación de la industria para la descripción y el descubrimiento de servicios web. La especificación UDDI agrega los estándares de protocolo SOAP (Simple Object Access Protocol), XML (lenguaje de marcado extensible) y HTTP/S, que fueron desarrollados por el World Wide Web Consortium (W3C) y el IETF. Los servicios UDDI son servicios web XML estándar que permiten que los desarrolladores empresariales publiquen, detecten, compartan y reutilicen con eficacia los servicios web directamente a través de sus herramientas de desarrollo. Integrados en Microsoft .NET Framework, los servicios UDDI utilizan la tecnología y herramientas probadas de Microsoft SQL Server con el objetivo de proporcionar un mecanismo de almacenamiento escalable. Los administradores de TI pueden utilizar el soporte de los servicios UDDI para esquemas de categorización estándar y autenticación de Active Directory, facilitando la integración con un entorno empresarial.
  
El servicio **MSSQL$UDDI** debe instalarse manualmente en equipos Windows Server 2003; cuando se instala, su tipo de inicio se configura en **Manual.** Si se detiene este servicio, la base de datos de SQL Server de UDDI dejará de estar disponible y los clientes no serán capaces de preguntar ni tener acceso a los datos en sus bases de datos.
  
#### MSSQLServerADHelper
  
El servicio del sistema **MSSQLServerADHelper** habilita Microsoft SQL Server y el servicio Analysis Services de Microsoft SQL Server para publicar información en Active Directory cuando estos servicios no se están invocando a través de la cuenta LocalSystem. Sólo se permite ejecutar una instancia del servicio **MSSQLServerADHelper** en un equipo. Todas las instancias de Microsoft SQL Server y Analysis Services de Microsoft SQL Server la utilizan cuando resulta necesario.
  
**MSSQLServerADHelper** no es un servicio de servidor y no acepta solicitudes del cliente. Tampoco utiliza un puerto TCP o UDP.
  
No puede detener el servicio **MSSQLServerADHelper**. y se inicia dinámicamente a través de una instancia de SQL Server o Analysis Manager cuando es necesario. Se detiene en cuanto ha finalizado el trabajo. Ejecute siempre este servicio con la cuenta del sistema local y no lo inicie manualmente desde la consola. Si lo deshabilita, puede haber problemas al agregar, actualizar o eliminar objetos de Active Directory relacionados con SQL Server. Este servicio se debe instalar manualmente en equipos con Windows Server 2003. Una vez instalado, su tipo de inicio se configura como **Manual.**
  
#### .NET Framework Support Service
  
El servicio del sistema **.NET Framework Support Service** notifica a un cliente de suscripción cuando un proceso especificado inicializa el servicio Client Runtime Service. **.NET Framework Support Service** proporciona un entorno de tiempo de ejecución denominado Common Language Runtime (CLR), que administra la ejecución de código y proporciona servicios que facilitan el proceso de desarrollo. Los compiladores y herramientas exponen la funcionalidad del tiempo de ejecución y permiten escribir código que puede aprovechar las ventajas de este entorno de ejecución administrado. CLR permite diseñar componentes y aplicaciones cuyos objetos interactúan entre lenguajes. Los objetos escritos en distintos lenguajes se pueden comunicar entre sí y sus comportamientos se pueden integrar bien. Este servicio se instala normalmente como parte del entorno de desarrollo Visual Studio.NET y no estará presente ni activo a menos que se instale manualmente.
  
Si se detiene o se deshabilita el servicio **.NET Framework Support Service**, el usuario no recibirá una notificación cuando una aplicación .NET inicie el CLR.
  
#### Inicio de sesión de red
  
El servicio de **Inicio de sesión en red** mantiene un canal seguro entre el equipo y el controlador del dominio que usa para autenticar a los usuarios y los servicios. Pasa las credenciales del usuario a través de un canal seguro hasta un controlador del dominio y devuelve los identificadores de seguridad del dominio y los derechos al usuario, lo que se conoce normalmente como autenticación pass-through. El servicio se instala en todos los equipos Windows Server 2003 y Windows XP, y su tipo de inicio se establece en Manual. Después de que el equipo se une a un dominio, el servicio se inicia automáticamente.
  
En las familias Windows 2000 Server y Windows Server 2003, este serviciopublica registros de recursos del servicio en DNS, que emplea para resolver nombres en las direcciones IP de controladores de dominio. El servicio Inicio de sesión en red implementa además el protocolo de replicación basado en la llamada a procedimiento remoto (RPC) para sincronizar los controladores principales de dominio (PDC) y de reserva (BDC) de Windows NT 4.0.
  
Si deshabilita este servicio,es posible que el equipo no pueda autenticar a los usuarios y servicios, así como que el controlador de dominio no pueda registrar registros DNS. Concretamente, se podrían denegar las solicitudes de autenticación NTLM y los equipos cliente podrían no encontrar los controladores de dominio.
  
#### Escritorio remoto compartido de NetMeeting
  
El servicio de **Escritorio remoto compartido de NetMeeting** permite a usuarios autorizados obtener acceso de forma remota al escritorio Windows con la aplicación Microsoft NetMeeting® desde otro equipo personal a través de una intranet. El servicio se instala y se deshabilita de forma predeterminada. Se debe habilitar de forma explícita con NetMeeting y se puede deshabilitar en NetMeeting o cerrarse mediante un icono de la bandeja de Windows.
  
Si se detiene o deshabilita el servicio **Escritorio remoto compartido de NetMeeting**, el controlador de pantalla de NetMeeting se descarga y el equipo no será capaz de proporcionar acceso remoto a su escritorio.
  
#### Conexiones de red
  
Este serviciose instala de forma predeterminada en equipos con Windows Server 2003 y Windows XP. Este servicio administra objetos en la carpeta **Conexiones de red**, donde se pueden ver conexiones de red y remotas. Este servicio es el responsable de la configuración de red del cliente y muestra el estado de la conexión en el área de notificación de la barra de tareas. Puede también ver y configurar la interfaz de red a través de este servicio.
  
El servicio **Conexiones de red** se inicia automáticamente cuando el tipo de inicio es Manual y se invoca la interfaz Conexiones de red. Si se detiene este servicio, no estará disponible la configuración en el cliente para conexiones LAN, de conexión telefónica o VPN. Si se deshabilita, puede que se den los siguientes resultados:
  
-   Las conexiones no aparecerán en la carpeta **Conexiones de red**, lo que impedirá el acceso telefónico y no se podrán configurar los valores de LAN.
  
-   Otros servicios que utilizan Conexiones de red para comprobar las directivas de grupo compatibles con Ubicación de red no funcionarán correctamente.
  
-   No se recibirán los eventos pertenecientes a conexiones y desconexiones de medios.
  
-   La conexión compartida a Internet no funcionará correctamente.
  
-   No se podrán configurar las conexiones entrantes, valores de configuración inalámbricos y la red doméstica.
  
-   No se crearán conexiones.
  
-   No se iniciarán los servicios que dependan directamente del mismo.
  
#### DDE de red
  
El servicio de **DDE de red** ofrece transporte y seguridad en la red para el intercambio dinámico de datos (DDE) en los programas que se ejecutan en el mismo equipo o en equipos diferentes. Puede crear en el equipo "recursos compartidos" de DDE de red de forma programada o con Ddeshare.exe, y hacerlos visibles para otras aplicaciones y equipos. Normalmente, el usuario que crea el recurso compartido generará y ejecutará un proceso de servidor para administrar las solicitudes entrantes de procesos o aplicaciones de cliente, tanto locales como remotas. Una vez conectados, estos procesos pueden intercambiar cualquier tipo de datos a través de un transporte de red seguro.
  
Este servicio se instala y se deshabilita de forma predeterminada. Para utilizar la funcionalidad DDE de red, debe establecer el tipo de inicio de servicio en Manual, después de lo cual el servicio sólo se inicia cuando lo invoca una aplicación que utiliza DDE de red, como Clipbrd.exe o Ddeshare.exe.
  
Si detiene el servicio **DDE de red**, la seguridad y el transporte de DDE no estarán disponibles. Si deshabilita este servicio, cualquier aplicación que dependa de él agotará el tiempo de espera cuando intente iniciar el servicio. Si una aplicación de un equipo remoto intenta iniciar el servicio **DDE de red** en otro equipo, no se podrá ver el equipo remoto en la red.
  
#### DSDM de DDE de red
  
El servicio **DSDM de DDE de red** administra los recursos compartidos de red DDE. Sólo el servicio **DDE de red** lo utiliza para administrar conversaciones DDE compartidas. Puede crear y confiar en los recursos compartidos de DDE a través de Ddeshare.exe, a fin de permitir que las aplicaciones y equipos remotos se conecten y compartan datos. El servicio **DSDM de DDE de red** mantiene una base de datos de recursos compartidos de DDE, que incluye información sobre los recursos compartidos de confianza. Para cada solicitud de conexión que se hace desde o a una aplicación, el servicio consulta la base de datos y valida la configuración de seguridad para determinar si se debe aprobar la solicitud.
  
El servicio **DSDM de DDE de red** se instala y se deshabilita de forma predeterminada. Para utilizar la funcionalidad DDE de red, debe establecer el tipo de inicio de servicio en Manual, después que lo cual el servicio sólo se inicia cuando lo invoca una aplicación que utiliza DDE de red. Si detiene el servicio **DSDM de DDE de red**, no estarán disponibles los recursos compartidos de red de DDE. Si deshabilita este servicio, cualquier aplicación que dependa de él agotará el tiempo de espera cuando intente iniciar el servicio.
  
#### NLA (Network Location Awareness)
  
El servicio **NLA (Network Location Awareness)** recopila y almacena información de configuración de red como cambios en el nombre de dominio y dirección IP, así como información sobre cambios en la ubicación. El servicio notifica a las aplicaciones compatibles cuando esta información cambia para que puedan reconfigurarse a sí mismas y utilizar la conexión de red actual.
  
El servicio **NLA (Network Location Awareness)** es un servicio predeterminado en Windows XP. Incluso si configura este servicio con un tipo de inicio manual, normalmente se iniciará a través de servicios dependientes. Si se detiene este servicio, la funcionalidad del conocimiento de ubicación de red no estará disponible.
  
#### Servicio de suministro de red
  
El **servicio de suministro de red** proporciona la capacidad de descargar y administrar archivos de configuración XML de servicios de suministro de red como Microsoft Wireless Provisioning Services (WPS), que permiten en suministro automático de red para proveedores de servicios de Internet y redes privadas. Este servicio trabaja con el servicio **Configuración inalámbrica rápida** para proporcionar compatibilidad con los últimos estándares de seguridad inalámbrica.
  
Si se detiene o se deshabilita el **servicio de suministro de red**, la configuración y operación de la interfaz de red inalámbrica podría ser incorrecta, aun cuando el entorno de red no utilice WPS o un equivalente.
  
#### Protocolo de transferencia de noticias a través de la red (NNTP)
  
El servicio del **Protocolo de transferencia de noticias a través de la red (NNTP)** permite que los equipos Windows Server 2003 actúen como servidores de noticias. Los equipos cliente pueden utilizar una aplicación cliente de noticias, como el cliente de mensajería Microsoft Outlook Express para recuperar grupos de noticias del servidor y leer las cabeceras o cuerpos de los artículos de cada grupo de noticias. A continuación, los equipos cliente pueden devolver los artículos al servidor.
  
NNTP es un estándar de Internet. El servicio NNTP que se incluye con Windows Server 2003 no admite transmisiones en las cuales dos servidores de noticias replican entre sí el contenido que alojan. No obstante, la versión incluida en Exchange 2000 sí contiene esta funcionalidad. Este servicio no se instala ni habilita de forma predeterminada. Sólo puede instalarse junto con IIS.
  
Si el servicio **de Protocolo de transferencia de noticias a través de la red (NNTP)** se detiene, los equipos cliente no podrán conectarse y leer o recuperar publicaciones.
  
#### Proveedor de compatibilidad con seguridad LM de Windows NT
  
El servicio **Proveedor de compatibilidad con seguridad LM de Windows NT** ofrece seguridad a programas de RPC que utilizan transportes que no son conductos con nombres. Permite a los usuarios iniciar una sesión en la red utilizando el protocolo de autenticación NTLM, que autentica a clientes que no utilizan la versión Kerberos 5 del protocolo de autenticación.
  
El protocolo de autenticación de desafío/respuesta de Windows NT (NTLM) se utiliza en redes que incluyen sistemas con versiones del sistema operativo Windows NT y en sistemas independientes. NTLM es el acrónimo de Windows NT LAN Manager, un nombre elegido para distinguir este protocolo de desafío/respuesta más avanzado de su predecesor más débil LAN Manager (LM).
  
Windows 2000 utilizó la versión Kerberos 5 del protocolo de autenticación, que proporciona mayor seguridad a redes de equipos que NTLM. Aunque el protocolo Kerberos es el protocolo de autenticación preferido para redes de Windows 2000 y Windows Server 2003, NTLM se admite todavía y debe utilizarse para la autenticación de red si la red incluye equipos en los que se ejecutan versiones de Windows NT, Windows 98 o Windows Millennium Edition. La autenticación del inicio de sesión en equipos independientes requiere también NTLM.
  
Las credenciales de NTLM están basadas en datos obtenidos durante el proceso de inicio de sesión interactivo y consisten en un nombre de dominio, un nombre de usuario y un hash unidireccional de la contraseña del usuario. NTLM utiliza un protocolo de desafío/respuesta cifrado para autenticar a un usuario, pero sin enviar su contraseña por la red. En su lugar, el equipo que solicita la autenticación debe realizar un cálculo que pruebe que tiene acceso a las credenciales de NTLM seguras.
  
La autenticación NTLM interactiva en una red implica típicamente el uso de dos equipos: un equipo cliente, en que el usuario solicita la autenticación, y un controlador de dominio que almacena la información relacionada con la contraseña del usuario. La autenticación no interactiva, que se puede requerir para permitir que un usuario que ya ha iniciado sesión obtenga acceso a un recurso como una aplicación de servidor, suele implicar a tres equipos: un cliente, un servidor y un controlador de dominio que hace los cálculos de autenticación en nombre del servidor.
  
El servicio **Proveedor de compatibilidad con seguridad LM de Windows NT** se instala y se ejecuta de forma predeterminada en todos los equipos con Windows XP y Windows Server 2003. Si detiene o se deshabilita este servicio, los clientes que utilizan el protocolo de autenticación NTLM no podrán iniciar sesión ni tener acceso a recursos de red. Microsoft Operations Manager (MOM) utiliza este servicio.
  
#### Registros y alertas de rendimiento
  
El servicio **Registros y alertas de rendimiento** recopila datos de rendimiento de equipos locales o remotos de acuerdo a parámetros de programación configurados previamente. A continuación, guarda la información en un registro o emite una alerta. Este servicio inicia y detiene cada recopilación de datos de rendimiento con nombre, según la información que se incluye en la configuración de recopilación de registro con nombre. Registros y alertas de rendimiento sólo se ejecuta si se ha programado al menos una recopilación. Sin embargo, se instala de forma predeterminada en Windows XP y Windows Server 2003.
  
Si se detiene o se deshabilita el servicio **Registros y alertas de rendimiento**, no se recopilará información de rendimiento. Además, cualquier colección de datos que esté actualmente activa se terminará y las colecciones programadas para el futuro no tendrán lugar.
  
#### Plug and Play
  
El servicio **Plug and Play** permite que un equipo reconozca y se adapte a los cambios de hardware con poca o ninguna intervención por parte del usuario. Este servicio permite agregar o quitar dispositivos sin tener conocimientos avanzados sobre el hardware de su equipo y sin necesidad de configurar manualmente el hardware o el sistema operativo. Por ejemplo, puede conectar un teclado USB y el servicio **Plug and Play** detectará este nuevo dispositivo, encontrará un controlador para el mismo y lo instalará. Asimismo, puede acoplar un equipo portátil y utilizar la tarjeta Ethernet de la estación de acoplamiento para conectarse a la red; no es necesario modificar la configuración. A continuación, puede desacoplar el mismo equipo y utilizar un módem para conectarse a la red, una vez más sin necesidad de realizar cambios manuales de configuración.
  
El servicio **Plug and Play** se instala y se configura para ejecutarse automáticamente en Windows Server 2003 y Windows XP. No puede detener ni deshabilitar el servicio a través del complemento de Servicios de MCC a causa de la repercusión en la estabilidad del sistema operativo. Si se detiene este servicio con la herramienta de solución de problemas MSCONFIG, la interfaz de Administrador de dispositivos aparecerá vacía sin ningún dispositivo de hardware.
  
#### Servicio del número de serie de medio portátil
  
El servicio **Servicio del número de serie de medio portátil** recupera el número de serie de cualquier reproductor de música portátil conectado al equipo. Este servicio permite que el Administrador de dispositivos de Windows Media (WMDM) obtenga el número de serie de los dispositivos portátiles de música para que el contenido del medio se pueda copiar con seguridad en dichos dispositivos. Sin el número de serie, no puede asociar el contenido a un dispositivo específico, lo que quizás evite que se transfiera el contenido protegido al dispositivo.
  
Para identificar el medio portátil, muchos fabricantes de medios de almacenamiento han implementado un número de serie único guardado en un área no volátil del dispositivo de almacenamiento. Por ejemplo, según la revisión 1.3 de la especificación CompactFlash de CompactFlash Association (CFA), las tarjetas CompactFlash deben tener un número de serie único. También algunos tipos de medios de almacenamiento extraíbles tienen números de serie únicos.
  
Para que un lector o adaptador de medios portátil resulte compatible con Windows Media, debe permitir que una aplicación recupere números de serie del medio.
  
El **Servicio del número de serie de medio portátil** se instala de forma predeterminada en Windows XP y Windows Server 2003. Su tipo de inicio se configura en **Manual**, y se inicia a petición de WMDM. Si el servicio se detiene o se deshabilita, puede que no se permita la transferencia del contenido protegido al dispositivo y que el número de serie no se recupere de los dispositivos de medios portátiles.
  
#### Servidor de impresión para Macintosh
  
El servicio **Servidor de impresión para Macintosh** permite que los clientes Apple Macintosh dirijan la impresión a un administrador de colas de impresión en un equipo con Windows Server 2003. Este servicio permite también que Windows Server 2003 Enterprise Edition se comunique con un dispositivo de impresión que utilice el protocolo AppleTalk. Este servicio no se instala de forma predeterminada.
  
Si se detiene el servicio **Servidor de impresión para Macintosh**, los clientes de Macintosh AppleTalk no podrán dirigir trabajos de impresión a una cola de impresión basada en Windows Server 2003.
  
#### Administrador de colas de impresión
  
El servicio **Cola de impresión** administra todas las colas de impresión locales y en red y controla todos los trabajos de impresión. La cola de impresión se comunica con los controladores de impresora y los componentes de entrada y salida (E/S) como el puerto USB y el conjunto de protocolos TCP/IP, y es el centro del subsistema de impresión de Windows. Se instala y se activa de forma predeterminada en equipos con Windows XP y Windows Server 2003.
  
Si se detiene el servicio **Cola de Impresión**, no podrá imprimir ni enviar faxes desde su equipo local. Cuando se detiene el servicio **Cola de Impresión** en un servidor en el que se ejecutan los Servicios de Terminal Server, el subárbol de sistema del Registro crecerá lentamente hasta que llene el volumen del sistema y cause el bloqueo del servidor. Este problema se produce por el hecho de que, cuando clientes nuevos inician sesión en el servidor a través de Servicios de Terminal Server, el sistema trata de asignar automáticamente la impresora local de cliente a un puerto de la impresora en el servidor, y registra esta cartografía en el registro. Sin embargo, el servicio de **Cola de Impresión** debe, supuestamente, borrar todos los registros cuando el usuario termina la sesión, y si el servicio no se ejecuta, los registros no usados nunca se borrarán.
  
Además, la función Printer Pruner de Active Directory depende del servicio **Cola de Impresión.** Para que Printer Pruner funcione en toda la empresa y permita que las colas huérfanas se limpien de forma no administrada, todos los sitios de la empresa deben tener al menos un controlador de dominio que ejecute el servicio **Cola de Impresión.** Si configurael servicio en **Deshabilitado** o **Manual**, no se iniciará automáticamente cuando se envíen trabajos de impresión.
  
#### Almacenamiento protegido
  
El servicio de **Almacenamiento protegido** protege el almacenamiento de información confidencial, como las claves privadas, y evita el acceso de servicios, procesos o usuarios no autorizados. El servicio proporciona un conjunto de bibliotecas de software que permite que las aplicaciones obtengan y recuperen información de seguridad, entre otras, desde ubicaciones de almacenamiento personal, ya que oculta la implementación y detalles de dicho almacenamiento.
  
La ubicación de almacenamiento que este servicio proporciona es segura y está protegida contra modificaciones. El servicio de **Almacenamiento protegido** utiliza HMAC (Hash-Based Message Authentication Code) y la función del hash de cifrado SHA1 (Secure Hash Algorithm 1) para cifrar la clave de sesión del usuario. Este componente no requiere configuración.
  
El servicio de **Almacenamiento protegido** se introdujo originalmente en Windows 2000. En Windows XP y Windows Server 2003, este servicio fue reemplazado por la API de Protección de datos (DPAPI), que es actualmente el servicio preferido para el almacenamiento protegido. Al contrario que DPAPI, la interfaz del servicio de **Almacenamiento protegido** no se encuentra expuesta públicamente.
  
Si este servicioestá deshabilitado, las claves privadas serán inaccesibles, el servicio de **Certificate Server de Windows** no estará operativo, S/MIME (extensiones seguras multipropósito al correo de Internet) y SSL no funcionarán, y el inicio de sesión con tarjeta inteligente dará error.
  
#### Servicio RSVP QoS
  
La calidad del servicio (QoS) es un estándar en toda la industria que se desarrolló para lograr el uso más eficiente de los recursos de red. Permite a clientes y servidores diferenciar entre tipos de datos diferentes y priorizar el tráfico de red de extremo a extremo. IETF (Internet Engineering Task Force) ha jugado un papel central para ayudar a asegurar que los estándares QoS permitan a todos los dispositivos de red afectados participar en la conexión de extremo a extremo con QoS. La calidad del servicio proporciona a las aplicaciones (o a los administradores de red) una forma de predecir y administrar los recursos de red, como el ancho de banda disponible y latencia, en equipos locales y dispositivos de red.
  
El **servicio QoS RSVP** implementa la compatibilidad QoS de Windows. Se instala de forma predeterminada en equipos con Windows XP, pero no se instala en equipos con Windows Server 2003. Una vez instalado, su tipo de inicio se configura como **Manual.** Si este servicio se deshabilita o se desinstala, el equipo no podrá participar en conexiones QoS ni hacer solicitudes para reservar recursos de ancho de banda controlado con QoS.
  
#### Administrador de conexión automática de acceso remoto
  
El servicio del **Administrador de conexión automática de acceso remoto** detecta los intentos erróneos de conexión a una red o equipo remoto y proporciona métodos alternativos de conexión. Cuando se produce un error en un programa en un intento por hacer referencia a un nombre o dirección DNS o NetBIOS remoto, o cuando el acceso de red no está disponible, el servicio muestra un cuadro de diálogo que le permite hacer una conexión de acceso telefónico o VPN al equipo remoto.
  
Con el propósito de servir de ayuda, el servicio **Administrador de conexión automática de acceso remoto** mantiene una base de datos local con las conexiones utilizadas anteriormente para entrar en contacto con los equipos o recursos compartidos con nombre. Si el servicio detecta un intento incorrecto de conexión a un equipo o recurso compartido remoto, ofrecerá marcar la última conexión empleada. Este servicio se instala de forma predeterminada en equipos con Windows XP y Windows Server 2003, pero su tipo de inicio se configura en **Manual.** Se inicia automáticamente según se requiera. Si deshabilita el servicio **Administrador de conexión automática de acceso remoto**, necesitará establecer manualmente conexiones a equipos remotos cuando necesite tener acceso a ellos.
  
#### Administrador de conexión de acceso remoto
  
El servicio del sistema **Administrador de conexión de acceso remoto** administra las conexiones de acceso telefónico y VPN establecidas desde el equipo a Internet u otras redes remotas. Si hace doble clic en una conexión de la carpeta **Conexiones de red** y, a continuación, selecciona el botón **Conectar,** el servicio **Administrador de conexión de acceso remoto** marca la conexión o envía una solicitud de conexión VPN, además de administrar las negociaciones posteriores con el servidor de acceso remoto, a fin de configurar la conexión.
  
El servicio **Administrador de conexión de acceso remoto** se descargará cuando no haya solicitudes pendientes. La carpeta **Conexiones de red** llama a este servicio para que enumere el conjunto de conexiones y muestre el estado de cada una de ellas. Aunque su estado de inicio predeterminado se configure en **Manual**, este servicio se iniciará si hay una o más conexiones VPN o de acceso telefónico en la carpeta **Conexiones de red**.
  
Si el servicio **Administrador de conexión de acceso remoto** se detiene o deshabilita, el equipo no podrá realizar conexiones de acceso telefónico o VPN con una red remota, ni aceptar solicitudes de conexión entrantes. Además, la carpeta **Conexiones de red** no mostrará conexiones de acceso telefónico o VPN, y el Panel de control de opciones de Internet no permitirá que el usuario configure ninguna opción relacionada con las conexiones de acceso telefónico o VPN.
  
#### Servicio de administración remota
  
El **Servicio de administración remota** lleva a cabo las siguientes tareas de administración remota al reiniciarse un servidor:
  
-   Aumenta el recuento de inicios de servidor.
  
-   Genera un certificado con firma automática.
  
-   Emite una alerta si no se ha especificado la fecha y la hora en el servidor.
  
-   Emite una alerta si no se ha configurado la funcionalidad Correo electrónico de alerta.
  
El **Servicio de administración remota** comienza la ejecución de las tareas pertinentes cuando el **Administrador de servidores remotos** así se lo solicita a través de una interfaz COM. El servicio utiliza la cuenta del sistema local y sólo acepta solicitudes sobre la interfaz COM de aquellos clientes que usan las cuentas de administradores o del sistema local.
  
Si el **Servicio de administración remota** se configura en **Manual**, se iniciará cuando lo invoque el servicio **Administrador de servidores remotos**. Se puede detener posteriormente sin ningún efecto en las funciones del servidor. Este servicio se instala y se configura para iniciarse automáticamente de forma predeterminada en equipos con Windows Server 2003.
  
Al detener el **Servicio de administración remota**, puede que algunas características de Herramientas de administración remota del servidor no funcionen debidamente como, por ejemplo, la interfaz web para la administración remota.
  
#### Administrador de sesión de Ayuda de escritorio remoto
  
El servicio del **Administrador de sesión de Ayuda de escritorio remoto** administra y controla la característica Asistencia remota de la aplicación Centro de ayuda y soporte técnico (helpctr.exe). Se instala de forma predeterminada en Windows XP y Windows Server 2003, pero sólo se inicia cuando se recibe una solicitud de Asistencia Remota.
  
Si se detiene el servicio **Administrador de sesión de Ayuda de escritorio remoto**, la Asistencia remota y la capacidad de solicitar ayuda a través de Asistencia remota no estarán disponibles.
  
#### Instalación remota
  
El servicio **Instalación remota** ofrece la posibilidad de instalar Windows 2000, Windows XP y Windows Server 2003 en equipos cliente habilitados para el medio de ejecución anterior al inicio (PXE) remoto preiniciados. El servicio Capa de negociación de información de inicio (BINL), que es el componente principal de los Servicios de instalación remota (RIS), responde a clientes PXE, comprueba Active Directory para la validación de clientes y pasa la información del cliente al servidor y la recibe del mismo. El servicio BINL se instala cuando se agrega el componente RIS mediante Agregar o quitar componentes de Windows o se selecciona al instalar inicialmente el sistema operativo.
  
RIS es una característica de implementación de Windows incluida en la familia Windows Server 2003. Con RIS, se pueden admitir instalaciones a petición del sistema operativo basadas en secuencias de comandos e imágenes, y a través de una conexión de red desde un servidor RIS a un equipo cliente. RIS se ha diseñado para simplificar la implementación de sistemas operativos y aplicaciones, así como para mejorar la capacidad de recuperación tras error.
  
Puede utilizar RIS de distintas formas, entre ellas las siguientes:
  
-   Para proporcionar un sistema operativo a los usuarios a petición. Puede utilizar RIS para crear imágenes de instalación automatizada de sistemas operativos de la familia Windows Server 2003, Windows XP y Windows 2000. Si un usuario inicia un equipo cliente, incluso si éste no dispone de sistema operativo, el servidor RIS podrá responder mediante la instalación de un sistema operativo a través de la red, sin la necesidad de CD. Para admitir esta capacidad, los equipos cliente deben utilizar PXE a través del adaptador de red.
  
-   Para proporcionar imágenes del sistema operativo que incluyan valores y aplicaciones específicos como, por ejemplo, una imagen que cumpla un estándar de equipo de escritorio corporativo. Se pueden ofrecer las imágenes designadas a un grupo de usuarios determinado.
  
El servicio de **Instalación remota** no se instala de forma predeterminada. Si instala el servicio y lo detiene, los equipos cliente compatibles con PXE no podrán instalar Windows de forma remota ni utilizar otras herramientas basadas en RIS desde el equipo.
  
#### Llamada a procedimiento remoto (RPC)
  
El servicio **Llamada a procedimiento remoto (RPC)** de Microsoft representa un mecanismo seguro de comunicación entre procesos (IPC) que permite el intercambio de datos y la activación de características que residen en un proceso diferente. Se pueden realizar diferentes procesos en el mismo equipo, la red de área local o a través de Internet. El servicio de **Llamada a procedimiento remoto (RPC)** sirve de asignador de puntos finales RPC y de Administrador de control de servicios (SCM) COM. Más de 50 servicios dependen del servicio RPC para iniciarse satisfactoriamente.
  
El servicio **Llamada a procedimiento remoto (RPC)** no se puede detener o deshabilitar. Si elservicio no está disponible, el sistema operativo no se cargará.
  
#### Localizador de llamadas a procedimiento remoto (RPC)
  
El servicio **Localizador de llamadas a procedimiento remoto (RPC)** permite que los clientes RPC puedan utilizar el conjunto de API de RpcNs\* para localizar los servidores RPC. Además, administra la base de datos del servicio de nombres RPC. Este servicio se desactiva de forma predeterminada y no ha sido utilizado por muchas aplicaciones que se publicaron después del lanzamiento de Windows 95.
  
Para obtener más información sobre la familia RpcNs de API, consulte la información del SDK en el vínculo de la biblioteca MSDN incluido en la página de [recursos web](http://www.microsoft.com/windows/reskits/webresources/)en www.microsoft.com/windows/reskits/webresources.
  
Si detiene o deshabilita el servicio **Localizador de llamadas a procedimiento remoto (RPC)**, es probable que los clientes RPC que necesitan localizar los servicios RPC en otros equipos no puedan localizar servidores, o bien podrían no iniciarse. Además, es posible que los clientes RPC que dependan de las API de RpcNs\* del mismo equipo no encuentren servidores RPC compatibles con una interfaz determinada. Si detiene o deshabilita este servicio en el controlador de dominio, podría ocasionar interrupciones en el servicio tanto a los clientes que utilicen las API de RpcNs\* como al controlador de dominio al intentar localizar clientes. Las API de RpcNs\* no se utilizan en Windows de forma interna; sólo necesita iniciar este servicio si aplicaciones de terceros lo precisan.
  
#### Servicio de Registro remoto
  
El **Servicio de Registro remoto** permite a los usuarios remotos que tengan los permisos adecuados modificar la configuración del registro en el controlador de dominio. Este servicio se instala y se ejecuta automáticamente de forma predeterminada en equipos con Windows XP y Windows Server 2003. Sin embargo, la configuración predeterminada del servicio sólo permite que los Administradores y Operadores de copia de seguridad tengan acceso remoto al registro. Este servicio es necesario para la utilidad Microsoft Baseline Security Analyzer (MBSA). MBSA es una herramienta que permite comprobar que se han instalado las revisiones en todos los servidores de la organización.
  
Si detiene el **servicio de registro remoto**, solamente se podrá modificar el registro en el equipo local. Si este servicio está deshabilitado, cualquier otro servicio que dependa directamente del mismo no se podrá iniciar, pero las operaciones del Registro en el equipo local no se verán afectadas. Sin embargo, ya no se conectarán otros equipos o dispositivos al registro del equipo local.
  
#### Administrador de servidores remotos
  
El servicio del **Administrador de servidores remotos** proporciona la siguiente funcionalidad:
  
-   Guarda la información de alertas de Administración remota.
  
-   Proporciona una interfaz para emitir, eliminar y enumerar alertas de Administración remota.
  
-   Proporciona una interfaz para ejecutar tareas de Administración remota.
  
El servicio **Administrador de servidores remotos** se instala y configura para que se inicie automáticamente de forma predeterminada en equipos con Windows Server 2003. El servicio actúa como proveedor de instancias WMI para los objetos de alerta de administración remota y como proveedor de métodos WMI para tareas de administración remota. El servicio se ejecuta en la cuenta del sistema local y sólo se aceptan solicitudes sobre la interfaz COM de aquellos clientes que se ejecutan en la cuenta del administrador o del sistema local.
  
Si el servicio del **Administrador de servidores remotos** se configura en **manual**, se iniciará cuando se reciba la siguiente solicitud de tareas o alertas de administración remota. Si el servicio se detiene, se reiniciará al obtener acceso a la interfaz web de la administración remota. Si este servicio está deshabilitado, cualquier otro servicio que dependa directamente del mismo no se podrá iniciar. Además, se producirá una pérdida de información sobre las alertas actuales de la administración remota si deshabilita el servicio.
  
#### Remote Server Monitor
  
El servicio **Administrador de servidores remotos** supervisa recursos importantes del equipo y administra el hardware temporizador de vigilancia opcional en servidores administrados de forma remota.
  
Si detiene este servicio,ya no podrá controlar los recursos críticos del equipo y se detendrá el temporizador de vigilancia.
  
#### Servicio de notificación de almacenamiento remoto
  
El **Servicio de notificación de almacenamiento remoto** notifica al usuario cuando un programa de usuario intenta leer o escribir archivos que sólo están disponibles desde un medio de almacenamiento secundario. Debido a la gran cantidad de tiempo que se invierte en el acceso a un archivo transferido a cinta, Almacenamiento remoto envía una notificación al usuario siempre que se produce un intento de lectura de un archivo migrado. Además, el servicio permite que el usuario cancele la solicitud en vez de esperar.
  
El servicio **Notificación de almacenamiento remoto** no se instala de forma predeterminada en Windows XP ni en Windows Server 2003. Si este servicio se detiene, no recibirá notificaciones adicionales cuando intente abrir archivos sin conexión, ni podrá cancelar una operación relacionada con este tipo de archivos.
  
#### Servidor de almacenamiento remoto
  
El servicio **Servidor de almacenamiento remoto** almacena archivos poco usados en medios de almacenamiento secundarios. Este servicio permite que el subsistema de almacenamiento remoto de Windows notifique al usuario si se ha obtenido acceso a un archivo sin conexión.
  
Almacenamiento remoto es una aplicación para la administración del almacenamiento jerárquico que mueve datos desde el almacenamiento de nivel superior al de nivel inferior. El almacenamiento de nivel superior se conoce comúnmente como almacenamiento local, o datos a los que se tiene acceso con frecuencia y se almacenan de forma local en discos de alto rendimiento. El almacenamiento de nivel inferior se conoce también como almacenamiento remoto, o datos a los que rara vez se tiene acceso y se almacenan en soportes más económicos hasta que se necesiten de nuevo. La administración de almacenamiento jerárquico reduce los costos de almacenar grandes cantidades de información, pero garantiza que aún se pueda obtener acceso a los datos.
  
El servicio **Servidor de almacenamiento remoto** se instala como parte del componente de almacenamiento remoto de Windows, que debe instalarse manualmente. Una vez instalado, el servicio está configurado para iniciarse automáticamente. Si el servicio se detiene, los archivos no se podrán mover ni recuperar de los medios de almacenamiento secundarios.
  
#### Almacenamiento de medios extraíbles
  
El servicio de **Almacenamiento de medios extraíbles** administra y cataloga los medios extraíbles y hace funcionar los dispositivos que los utilizan. Este servicio mantiene un catálogo con información de identificación de los medios extraíbles utilizados por el equipo, incluidas cintas y CD. Si el equipo contiene además dispositivos automatizados para mantener medios extraíbles, como un cargador automático de cintas o un jukebox de CD, el servicio de **Almacenamiento de medios extraíbles** también automatizará las funciones de montaje, desmontaje y expulsión de medios. Aplicaciones como Copia de seguridad y Almacenamiento remoto utilizan este servicio para catalogar medios y para tareas de automatización. En el resumen, este servicio etiqueta, cataloga y realiza un seguimiento de los medios, además de controlar unidades de biblioteca, ranuras y aperturas. Proporciona también operaciones de limpieza de unidades.
  
El servicio **Almacenamiento de medios extraíbles** se instala de forma predeterminada en Windows Server 2003 y Windows XP. Su configuración predeterminada es ejecutarse sólo cuando un programa solicita acceso al almacenamiento de medios extraíbles en el equipo local. Si este servicio se detiene, las aplicaciones dependientes de él, como Copia de seguridad y Almacenamiento remoto, funcionarán con mayor lentitud. El servicio **Almacenamiento de medios extraíbles** queda inactivo si no hay nada que procesar. Si no hay dispositivos automatizados conectados al equipo, el servicio sólo se ejecutará cuando lo utilicen las aplicaciones. Por lo tanto, no es necesario detener el servicio. Cuando se inicie en estas circunstancias, el Administrador de almacenamiento de medios extraíbles con frecuencia necesitará hacer un inventario de todo el contenido de los jukebox y cargadores automáticos conectados, que requiere el montaje de cada medio en una unidad.
  
#### Conjunto resultante de proveedor de directivas
  
El servicio **Conjunto resultante de proveedor de directivas** permite conectar con un controlador de dominio Windows Server 2003, obtener acceso a la base de datos WMI de dicho equipo y simular el conjunto resultante de directivas (RSoP) para la configuración de Directiva de grupo. La configuración de la directiva se determina para un usuario o equipo ubicado en Active Directory. Normalmente se denomina a esta simulación, modo de planeamiento.
  
El servicio **Conjunto resultante de proveedor de directivas** se instala de forma predeterminada en equipos con Windows Server 2003, pero su tipo de inicio se configura en **Manual**. Si este servicio se detiene en un controlador de dominio, la simulación de Modo de planificación de RSoP no estará disponible en ese controlador de dominio. RSoP sólo necesita ejecutarse en controladores de dominio; los servidores miembro y las estaciones de trabajo no necesitan ejecutar este servicio para utilizar la característica.
  
#### Enrutamiento y acceso remoto
  
El servicio **Enrutamiento y acceso remoto** ofrece los servicios de enrutamiento de varios protocolos: LAN a LAN, LAN a WAN, VPN y NAT. Este servicio proporciona también servicios remotos de acceso telefónico y VPN.
  
El servicio **Enrutamiento y acceso remoto** sustituye las características Servicio de enrutamiento y acceso remoto (RRAS) y Servicio de acceso remoto (RAS) en Windows NT 4.0. Se trata de un servicioúnico e integrado que finaliza las conexiones desde clientes de acceso telefónico o VPN y que proporciona enrutamiento de IP, IPX y Servicios para Macintosh. Su servidor puede usar este servicio para funcionar como un servidor de acceso remoto, un servidor VPN, una puerta de enlace o un enrutador de oficinas sucursales.
  
Desde un punto de vista del enrutamiento, este servicioadmite los protocolos de enrutamiento OSPF (Abrir primero la ruta de acceso más corta) y el protocolo de información de enrutamiento (RIP), además de controlar las tablas de enrutamiento para el motor de reenvío de pila TCP/IP.
  
El servicio **Enrutamiento y acceso remoto** se instala de forma predeterminada en equipos con Windows Server 2003. Está deshabilitado de forma predeterminada. Si este servicio se detiene, su equipo no podrá aceptar las conexiones de marcado a petición, VPN o RAS entrantes, y los protocolos de enrutamiento no se recibirán ni transmitirán.
  
#### Agente SAP
  
El servicio **Agente SAP** anuncia los servicios de red en una red IPX mediante el protocolo de anuncio de servicios IPX (SAP). Además, reenvía anuncios en un host multitarjeta. Algunas características, como Servicios de archivo e impresión para NetWare de Microsoft, dependen de este** **servicio.
  
El servicio **Agente SAP** necesita la instalación del protocolo de transferencia compatible con NWLINK IPX/SPX, y no se instala ni se activa de forma predeterminada. Si este servicio se desactiva, es posible que las características mencionadas no funcionen correctamente.
  
#### Inicio de sesión secundario
  
El servicio **Inicio de sesión secundario** permite a un usuario crear procesos dentro del contexto de diferentes entidades principales de seguridad. Un uso común de este servicio es cuando administradores inician sesión como usuarios restringidos pero necesitan privilegios administrativos para ejecutar una aplicación específica. Pueden utilizar un inicio de sesión secundario para ejecutar temporalmente dichas aplicaciones.
  
Otro componente del servicio **Inicio de sesión secundario** es RunAs.exe, que permite ejecutar como administrador programas (archivos \*.exe), consolas de MMC guardadas (\*.msc), accesos directos a programas y a consolas de MMC guardadas, además de elementos del Panel de control, mientras se está conectado al equipo como miembro de otro grupo, por ejemplo, el grupo **Usuarios**. En Windows 2000, este servicio se conoce como **servicio RunAs**.
  
El servicio **Inicio de sesión secundario** se instala y se ejecuta automáticamente de forma predeterminada en equipos con Windows XP y Windows Server 2003. Si se detiene o se deshabilita, este tipo de acceso de inicio de sesión no estará disponible. Todas las llamadas a la API **CreateProcessWithLogonW** darán error. Específicamente, si detiene o deshabilita este servicio, el complemento MMC que inicia las aplicaciones como otros usuarios y la herramienta RunAs.exe no funcionarán correctamente.
  
#### Administrador de cuentas de seguridad
  
El servicio **Administrador de cuentas de seguridad** (SAM) es un subsistema protegido que administra la información de cuentas de usuarios y grupos. En Windows 2000 y la familia de servidores Windows Server 2003, el servicio del registro del equipo local almacena las cuentas de seguridad de la estación de trabajo, mientras que las cuentas del controlador de dominio se almacenan en Active Directory. En Windows NT 4.0, las cuentas de seguridad local y de dominio se almacenan en el registro.
  
El inicio del servicio **Administrador de cuentas de seguridad** indica a otros servicios que está listo para aceptar solicitudes.
  
El servicio **Administrador de cuentas de seguridad** está presente en todas las versiones de Windows XP y Windows Server 2003, y no se puede detener. Si deshabilita este servicio, otros servicios en el equipo podrían no iniciarse correctamente. No deshabilite este servicio.
  
#### Security Center
  
El servicio **Security Center** proporciona una ubicación central para equipos que ejecutan Windows XP con SP2 para administrar la configuración relacionada con la seguridad. Está configurado para ejecutarse automáticamente de forma predeterminada. Cuándo se ejecuta, realiza las siguientes tareas:
  
-   Comprueba si el servicio **Firewall de Windows** se está ejecutando y verifica si están presentes y ejecutándose aplicaciones compatibles de servidor de seguridad de software de proveedores específicos WMI de terceros.
  
-   Verifica si está instalado software antivirus de proveedores específicos WMI de terceros, si el software está actualizado y si está activada la exploración en tiempo real.
  
-   Comprueba la configuración del servicio **Actualizaciones automáticas**. Si el servicio **Actualizaciones automáticas** se desactiva o no se configura con los valores recomendados, el servicio **Security Center** informará al usuario.
  
Si el servicio **Security Center** determina que falta un componente protegido, está mal configurado o no está actualizado, notifica al usuario a través de un mensaje e icono de alerta de inicio de sesión en el área de notificación de la barra de tareas.
  
Si deshabilita el servicio **Security Center**, los componentes protegidos continuarán funcionando de acuerdo con su configuración específica. Sin embargo, no se proporcionará un servicio centralizado de supervisión.
  
#### Servidor
  
Gracias al servicio **Servidor**, se pueden compartir las canalizaciones con nombre, las impresiones, los archivos y la compatibilidad con RPC a través de la red. Este servicio permite el uso compartido de recursos locales, como discos e impresoras, de forma que otros usuarios de la red puedan obtener acceso a los mismos. También posibilita la comunicación de canalizaciones con nombre entre aplicaciones que se ejecutan en otros equipos y en el suyo propio, que se utiliza para admitir las llamadas a procedimiento remoto (RPC). La comunicación de canalizaciones es un área de la memoria que se reserva de forma que la salida de un proceso se pueda utilizar como entrada de otro. No es necesario que el proceso de aceptación de entrada se realice de forma local, es decir, en el equipo. Este servicio se instala y se ejecuta automáticamente de forma predeterminada en equipos con Windows XP y Windows Server 2003.
  
Si se detiene o se deshabilita el servicio **Servidor**, el equipo no será capaz de compartir los archivos y las impresoras locales con otros equipos en la red, y no podrá satisfacer las solicitudes RPC remotas.
  
#### Detección de hardware shell
  
El servicio de **Detección de hardware shell** supervisa y proporciona notificaciones para los eventos de hardware de reproducción automática. La característica Reproducción automática detecta contenido como archivos de vídeo, imagen o música en medios y dispositivos extraíbles. AutoPlay inicia entonces automáticamente las aplicaciones para reproducir o mostrar ese contenido, lo que simplifica el uso de dispositivos periféricos especializados como reproductores MP3 y lectores digitales de fotografías. El servicio es también más fácil para los usuarios, porque no necesitan saber de antemano qué aplicaciones de software se necesitan para tener acceso a varios tipos contenido.
  
Reproducción automática admite distintos tipos de contenido y aplicaciones. Tanto los proveedores de software independientes (ISV) como los proveedores de hardware independientes (IHV) pueden ampliar esta compatibilidad a fin de incluir sus aplicaciones y dispositivos de hardware. Un usuario puede configurar una acción de Reproducción automática distinta para cualquier combinación de fotografías, archivos de música y vídeo.
  
Entre los tipos de medios y dispositivos admitidos por Reproducción automática se incluyen:
  
-   Medios de almacenamiento extraíbles
  
-   Medios Flash
  
-   Tarjetas de PC
  
-   Unidades USB externas de conexión directa o unidades fijas 1394
  
-   Entre los tipos de contenido admitidos se incluyen:
  
    -   Imágenes (archivos .jpg, .bmp, .gif y .tif)
  
    -   Archivos de música (archivos .mp3, .wma)
  
    -   Vídeo (archivos .mpg, .asf)
  
El servicio **Detección de hardware shell** se instala y se ejecuta automáticamente de forma predeterminada en equipos con Windows XP y Windows Server 2003. Si se detiene el servicio, la funcionalidad de reproducción automática de hardware no funcionará, los iconos y etiquetas de Mi PC volverán a la funcionalidad Windows 2000 y el rendimiento de shell se verá afectado también.
  
#### Protocolo simple de transferencia de correo (SMTP)
  
El servicio del **Protocolo simple de transferencia de correo (SMTP)** es un agente de envío y retransmisión de correo electrónico. Puede aceptar y poner en cola correo electrónico para destinos remotos y establecer conexiones a otros equipos a intervalos especificados. Los controladores del dominio Windows utilizan el servicio **SMTP** para la réplica basada en el correo electrónico entre sitios. Además, el componente Objetos de datos de colaboración (CDO) para Windows Server 2003 COM puede utilizar este servicio para enviar y poner en cola correo electrónico de salida.
  
El servicio **SMTP** se instala y se ejecuta de forma predeterminada en Windows Server 2003, Web Edition. En Windows XP y otras ediciones de Windows Server 2003, son un componente opcional que no se instala de forma predeterminada.
  
#### Servicios simples de TCP/IP
  
Los **Servicios simples de TCP/IP** implementan compatibilidad para los siguientes protocolos y puertos:
  
-   Eco, puerto 7, RFC 862
  
-   Descartar, puerto 9, RFC 863
  
-   Generador de caracteres (puerto 19, RFC 864)
  
-   Hora y día (puerto 13, RFC 867)
  
-   Cita del día (puerto 17, RFC 865)
  
Al habilitar **Servicios simples de TCP/IP**, se activan los cinco protocolos en todos los adaptadores. No se permite la habilitación selectiva de servicios específicos ni la activación de este servicio en cada uno de los adaptadores por separado.
  
Si detiene o deshabilita los **Servicios simples de TCP/IP**, el resto del sistema operativo no se ve afectado. Este servicio se debe instalar manualmente. No instale los Servicios simples de TCP/IP a menos que necesite específicamente que un equipo admita la comunicación con otros equipos que utilizan estos protocolos.
  
#### Groveler de almacenamiento de instancia única
  
El servicio del **Groveler de almacenamiento de instancia única (SIS)** es un componente integrante de los Servicios de Instalación remota (RIS). Este servicio rastrea el volumen de RIS para archivos duplicados para reducir la cantidad general de almacenamiento que se requiere en el volumen. Si el servicio encuentra archivos duplicados, copia el archivo original en el almacenamiento de instancia única y deja un archivo de vínculo en su lugar. Este archivo de vínculo contiene información sobre el archivo original como, por ejemplo, su ubicación actual, tamaño y atributos. Si una imagen contiene archivos duplicados, estos se copian en el almacén. De este modo, se precisa menos espacio en disco en el servidor RIS.
  
El servicio **SIS Groveler** tiene dos limitaciones.
  
-   No puede actuar en archivos a los que se hace referencia a través de puntos de unión.
  
-   No se puede utilizar con ningún sistema de archivos salvo NTFS, que es el único que admiten los servidores RIS.
  
El servicio **SIS Groveler** sólo está presente si el componente de servicios de instalación remota se ha instalado. En ese caso, se iniciará automáticamente al encender el equipo. Si se detiene el servicio **SIS Groveler**, los archivos se dejarán de vincular automáticamente de esta forma, pero se podrá seguir teniendo acceso a los archivos vinculados existentes. Las nuevas imágenes de instalación de RIS utilizarán el tamaño de imagen completo y ocuparán poco espacio. Si el servicio **SIS Groveler** ya no es necesario en el equipo, la forma correcta de dejar de utilizarlo consiste en seleccionar la herramienta Agregar o quitar componentes de Windows y eliminar el componente Servicios de instalación remota, con lo que se deshabilitará.
  
#### Tarjeta inteligente
  
El servicio de la **Tarjeta inteligente** administra y controla el acceso de una tarjeta inteligente insertada en un lector de este tipo de tarjetas conectado al equipo. El subsistema de tarjetas inteligentes se basa en los estándares del consorcio de grupos de trabajo para equipos personales y tarjetas inteligentes (PC/SC) y está formado por el componente Administrador de recursos, que administra el acceso a lectores y tarjetas inteligentes. Para administrar estos recursos, el Administrador de recursos realiza las siguientes funciones:
  
-   Identifica y realiza el seguimiento de los recursos.
  
-   Asigna lectores y recursos en varias aplicaciones.
  
-   Admite primitivas de transacción para el acceso a los servicios disponibles en una tarjeta determinada.
  
El administrador de recursos también expone un subconjunto de la API Win32 para proporcionar aplicaciones con acceso a una interfaz de usuario de selección de tarjetas o lectores. Este componente permite a las aplicaciones que reconocen las tarjetas inteligentes simples obtener acceso a una tarjeta y a un lector con un mínimo de código.
  
El servicio **Tarjeta inteligente** se instala automáticamente de forma predeterminada en equipos con Windows XP y Windows Server 2003. Su estado de inicio se configura en **Manual**, y se inicia cuando una aplicación solicita acceso de tarjeta inteligente. Si se detiene este servicio, su equipo no podrá leer tarjetas inteligentes.
  
#### Servicio SNMP
  
El **Servicio SNMP** permite al equipo local atender las solicitudes de entrada del protocolo simple de administración de redes (SNMP). Este servicio incluye agentes que supervisan la actividad en dispositivos de red e informan a la estación de trabajo de la consola de red, y ofrece una forma de administrar hosts de red como, por ejemplo, una estación de trabajo o equipos de servidor, enrutadores, puentes y concentradores de un equipo localizado centralmente que ejecuta software de administración de red. SNMP realiza los servicios de administración mediante la utilización de una arquitectura distribuida de equipos y agentes de administración.
  
Puede utilizar SNMP para realizar las tareas siguientes:
  
-   **Configurar dispositivos remotos**. Se puede enviar información de configuración a cada host en red desde el equipo de administración.
  
-   **Supervisar el rendimiento de la red**. Puede realizar un seguimiento de la velocidad de procesamiento, el rendimiento de la red, así como recopilar información sobre las transmisiones de datos realizadas correctamente.
  
-   **Detectar errores en la red o accesos inadecuados**. Puede configurar la activación de alarmas en los dispositivos de la red cuando se produzcan determinados eventos. Cuando se activa una alarma, el dispositivo reenvía un mensaje del evento al equipo de administración. Entre los tipos frecuentes de alarmas se incluyen un dispositivo que se apaga y se reinicia, un error de vínculo que se detecta en un enrutador y el acceso inadecuado.
  
-   **Auditar el uso en red**. Puede supervisar el uso general de la red para identificar el acceso de usuarios y grupos como los tipos de uso para los servicios y dispositivos de red.
  
El **Servicio SNMP** también incluye un agente SNMP que permite la administración centralizada y remota de los equipos que ejecutan las versiones siguientes del sistema operativo Windows:
  
-   Windows XP Home Edition
  
-   Windows XP Professional
  
-   Windows 2000 Professional
  
-   Windows 2000 Server
  
-   Familia Windows Server 2003
  
El agente SNMP también permite la administración de los siguientes servicios:
  
-   WINS basado en Windows XP o en la familia Windows Server 2003 y Windows 2000
  
-   DHCP basado en Windows XP o en la familia Windows Server 2003 y Windows 2000
  
-   Servicios de Internet Information Server basados en Windows XP o en la familia Windows Server 2003 y Windows 2000
  
-   LAN Manager
  
El **Servicio SNMP** sólo se instala si usted instala manualmente el componente opcional de SNMP a través del asistente para componentes de Windows. Una vez instalado, el servicio se inicia automáticamente. Si detiene o deshabilita el **Servicio SNMP**, el equipo dejará de responder a las solicitudes SNMP. Si hay herramientas de administración de redes basadas en SNMP supervisando el equipo, éstas ya no podrán recopilar datos del equipo ni controlar su funcionalidad a través del servicio.
  
#### Servicio de captura SNMP
  
El **Servicio de captura SNMP** intercepta mensajes generados por agentes SNMP locales o remotos, que contienen información sobre eventos específicos. El servicio envía los mensajes a programas de administración SNMP que se ejecutan en el equipo. El **Servicio SNMP**, cuando se ha configurado para un agente, genera mensajes de captura si se produce algún evento específico y estos mensajes son enviados a un destino de capturas. Por ejemplo, se puede configurar un agente para que inicie una captura de autenticación si un equipo de administración no reconocido envía una solicitud de información. Los destinos de capturas consisten en el nombre del equipo, la dirección IP o la dirección IPX del equipo de administración. El destino de captura debe ser un host habilitado para la red que ejecute software de administración SNMP. Estos destinos los puede configurar un usuario, pero los eventos que generan un mensaje de captura, como el reinicio de un equipo, los define internamente el agente SNMP.
  
El **Servicio de captura SNMP** sólo se instala si usted instala manualmente el componente opcional de SNMP a través del asistente para componentes de Windows. Una vez instalado, el servicio se inicia automáticamente. Si detiene o deshabilita el servicio, los programas basados en SNMP en el equipo no recibirán los mensajes de captura SNMP de otros equipos. Si este equipo supervisa los dispositivos de red o aplicaciones de servidor con capturas SNMP, se perderán eventos importantes del equipo.
  
#### Ayudante de la consola de administración especial
  
Puede utilizar el servicio del **Ayudante de la consola de administración especial** para realizar tareas de administración remota en un equipo que ejecute una versión de Windows Server 2003 si el equipo deja de funcionar debido a un mensaje de error de **detención.** El componente de servicios de administración de emergencia de Windows admite dos interfaces de consola fuera de banda: la Consola Especial de la Administración (SAC) y !SAC, que ofrece un subconjunto de comandos de SAC para el uso cuando el servidor se ha parado.
  
Tanto los componentes SAC como !SAC aceptan información de entrada y envían datos de salida a través del puerto fuera de banda. SAC es una entidad separada de los entornos de línea de comandos de la familia Windows Server 2003 y de !SAC. Una vez que se llega a un punto de error específico, los componentes de Servicios de administración de emergencia determinan cuándo se debe realizar el cambio de SAC a !SAC. Este último queda disponible automáticamente si SAC no se carga o no funciona. El servicio **Ayudante de la consola de administración especial** le permite crear los canales entrantes de comunicación a través del símbolo del sistema. Este servicio sólo se instala en equipos con Windows Server 2003 y sólo cuando usted habilita la función de los Servicios de Administración de emergencias como se describe en la documentación de Windows Server 2003.
  
Si detiene el servicio **Ayudante de la consola de administración especial**, los servicios de SAC dejarán de estar disponibles.
  
#### SQLAgent$\* (\*UDDI o WebDB)
  
**El servicio SQLAgent$\* (\* UDDI o WebDB)** es un programador de trabajos y un servicio de supervisión. Además, permite transferir información entre servidores SQL Server y se utiliza frecuentemente para realizar tanto copias de seguridad como replicaciones. Estos servicios no se instalan ni se activan de forma predeterminada.
  
Si detiene el servicio **SQLAgent$\* (\* UDDI o WebDB)**, no se realizará la replicación de SQL. Además, se producirá una interrupción en todos los trabajos programados, en la supervisión de alertas y eventos, así como en el inicio automático del servicio SQL Server.
  
#### Servicio de descubrimientos SSDP
  
El servicio del host Plug and Play universal que se incluye con Windows XP admite la funcionalidad Plug and Play de igual a igual para dispositivos de red. La especificación UPnP está diseñada para simplificar la instalación y administración del servicio de red y dispositivos. El servicio del host Plug and Play universal utiliza el Protocolo sencillo del descubrimiento del servicio (SSDP) para localizar e identificar dispositivos de red UPNP.
  
El **Servicio de descubrimientos SSDP** se instala y se configura en **Manual** en equipos con Windows XP. El servicio sólo se inicia cuando el equipo intenta localizar y configurar dispositivos UPNP. Si usted deshabilita este servicio, el equipo será incapaz de encontrar dispositivos UPNP en la red y el servicio de host Plug and Play universal no será capaz de encontrar e interactuar con dispositivos UPNP.
  
#### Notificación de eventos del sistema
  
La **Notificación de eventos del sistema** (SENS) supervisa y realiza un seguimiento de los eventos del equipo como, por ejemplo, eventos de red de inicio de sesión en Windows y de alimentación. Notifica también a los suscriptores del **sistema de eventos COM +** de estos eventos. Este servicio se instala de forma predeterminada y se ejecuta automáticamente en Windows XP y Windows Server 2003.
  
Si deshabilita el servicio **Notificación de eventos del sistema**, los suscriptores al servicio del **sistema de eventos COM+** no recibirán las notificaciones de evento y se presentarán los problemas siguientes:
  
-   No funcionarán las API Win32 IsNetworkAlive() ni las IsDestinationReachable(), que son las utilizan principalmente las aplicaciones móviles en los equipos portátiles.
  
-   No funcionarán las interfaces de ISens\*, Las notificaciones de inicio y cierre de sesión de SENS fallarán.
  
-   SyncMgr (Mobsync.exe) no funcionará correctamente. Depende de la información de conectividad así como de las notificaciones de inicio o cierre de sesión y conexión o desconexión de red de SENS.
  
-   El Sistema de eventos COM+ no podrá notificar algunos eventos a SENS.
  
-   El servicio **Instantáneas de volumen** no cargará apropiadamente, lo que hará que la API de Copia de seguridad de Windows falle.
  
#### Servicio de restauración del sistema
  
El **servicio de restauración del sistema** proporciona a los usuarios de Windows XP la capacidad de tomar fotografías de la configuración de su equipo y las guarda como una serie de puntos de recuperación. Estos puntos de recuperación se pueden utilizar como configuraciones infalibles después de un intento fracasado de instalación o mejora de un controlador de dispositivo o aplicación.
  
El **servicio de restauración del sistema** se habilita de forma predeterminada y creará automáticamente un nuevo punto de recuperación antes de que se realicen cambios mayores al equipo, como la instalación de controladores de dispositivos nuevos, de actualizaciones y aplicaciones. Los puntos automáticos de restauración se crean también diariamente, aunque este horario puede modificarse.
  
Si deshabilita el **servicio de restauración del sistema**, el equipo automático que restaura la funcionalidad ya no estará disponible y no se crearán puntos de restauración ni automáticos ni manuales.
  
#### Programador de tareas
  
El servicio del **Programador de tareas** permite configurar y programar tareas automatizadas en el equipo. El servicio supervisa los criterios seleccionados y realiza las tareas si se cumplen estos.
  
Puede utilizar la interfaz gráfica de usuario del servicio **Programador de tareas** para realizar las tareas siguientes:
  
-   Crear elementos de trabajo (actualmente el único tipo de elemento de trabajo disponible son las tareas).
  
-   Programar una tarea para que se ejecute a una hora específica o cuando tenga lugar un evento determinado. Por ejemplo, puede programar que el equipo ejecute ScanDisk a las 7:00 p.m. todos los domingos.
  
-   Cambiar la programación de una tarea.
  
-   Personalizar la forma en que se ejecutan las tareas.
  
-   Detener una tarea programada.
  
Puede iniciar el servicio **Programador de tareas** desde el complemento Servicios de MMC en Administración de equipos y configurar el inicio automático del mismo. De forma predeterminada, el servicio **Programador de tareas** se instala en equipos con Windows XP y Windows Server 2003. Se puede tener acceso a él desde la interfaz gráfica de usuario del Programador de tareas, a través de la API Programador de tareas, como se describe en el SDK, o bien desde la utilidad SchTasks.exe.
  
Si detiene el servicio **Programador de tareas**, las tareas no se ejecutarán a las horas programadas. Además, este servicio es necesario para Copia de seguridad de Windows y aplicaciones de copia de seguridad que dependen de la API de Copia de seguridad de Windows. Si no aparece ningún trabajo en la carpeta **%System Root%\\Tasks\\**, el efecto será mínimo si detiene el servicio. Por el contrario, los trabajos que es necesario que se ejecuten se pueden ver imposibilitados para comenzar. El paquete de características de servicios para la actualización del software del servidor de administración de sistemas producirá un error si no se encuentra disponible el servicio **Programador de tareas**. Tampoco las copias de seguridad programadas podrán ejecutarse si se detiene el servicio **Programador de Tareas**.
  
#### Ayuda de NetBIOS sobre TCP/IP
  
Este servicio ofrece compatibilidad para el servicio NetBIOS a través de **TCP/IP** (NetBT) y la resolución de nombres NetBIOS para clientes de la red. De esta forma, los usuarios pueden compartir archivos, imprimir e iniciar sesión en la red. En concreto, el** **servicio realiza la resolución de nombres DNS y hace el ping de un conjunto de direcciones IP que devuelven una lista de direcciones IP accesibles para proporcionar compatibilidad para el servicio de NetBT.
  
El **Servicio de Ayuda de NetBIOS sobre TCP/IP** se instala y se inicia automáticamente de forma predeterminada en Windows Server 2003 y Windows XP. Si detiene o deshabilita el servicio de Ayuda de NetBIOS sobre TCP/IP, los clientes de los servicios NetBT, Redirector (RDR), Server (SRV), **Net Logon** y **Messenger** no podrían compartir archivos o impresoras ni iniciar sesión en los equipos. Por ejemplo, la directiva de grupo basada en dominios dejará de funcionar.
  
#### Servidor de impresión TCP/IP
  
El servicio **Servidor de impresión TCP/IP** permite la impresión basada en TCP/IP mediante la utilización del protocolo Line Printer Daemon. El servicio Line Printer Daemon Service (LPDSVC) recibe en el servidor los documentos de utilidades Line Printer Remote (LPR) nativas que se ejecutan en los equipos UNIX.
  
El servicio **Servidor de Impresión TCP/IP** es un componente opcional que se debe instalar por separado del asistente para componentes de Windows. Si se detiene este servicio, la impresión TCP/IP, dejará de estar disponible.
  
#### Telefonía
  
El servicio **Telefonía** ofrece compatibilidad TAPI para programas que controlan dispositivos de telefonía, así como conexiones de voz basadas en IP en el equipo local y a través de LAN en servidores que también ejecutan el servicio. Este servicio permite que las aplicaciones puedan actuar como clientes en equipos de telefonía como centralitas (PBX), teléfonos y módems. El servicio admite la interfaz TAPI bajo la cual ofrece compatibilidad con distintos protocolos inalámbricos que se comunican con el equipo de telefonía. Estos protocolos se implementan en los proveedores de servicios de telefonía (TSP).
  
El servicio de **Telefonía** se instala de forma predeterminada en Windows XP y Windows Server 2003, y su estado de inicio se configura en **Manual.** Las aplicaciones que requieren TAPI lo pueden iniciar. Si se detiene o deshabilita el servicio de **Telefonía**, cualquier otro servicio que dependa directamente del mismo, como la compatibilidad de módem, no podrá iniciarse. No puede detener el servicio si hay otro servicio dependiente actualmente activo, como RAS. Si detiene el servicio cuando no haya servicios dependientes activos, se reiniciará cuando cualquier aplicación haga una llamada de inicialización a la interfaz TAPI.
  
#### Telnet
  
El servicio **Telnet** para Windows proporciona sesiones de terminal ASCII a los clientes Telnet. El servidor admite dos tipos de autenticación y cuatro tipos de terminales: American National Standards Institute (ANSI), VT-100, VT-52 y VTNT.
  
El servicio **Telnet** permite que un usuario remoto inicie sesión en un equipo y ejecute programas de la consola a través de la línea de comandos. Un equipo que ejecuta el servicio **Telnet** admite conexiones de varios clientes Telnet TCP/IP, incluidos equipos basados en UNIX y Windows. El servicio **Telnet** se instala en equipos con Windows XP y Windows Server 2003 de forma predeterminada, pero no está habilitado. Para la instalación de actualizaciones, se conserva el tipo de inicio del servicio **Telnet** en la versión anterior de Windows.
  
Si detiene el servicio **Telnet**, no estará disponible el acceso remoto del usuario a programas a través del cliente Telnet, los usuarios remotos no podrán conectarse a este equipo a través del protocolo Telnet y los usuarios normales no podrán conectarse al equipo ni ejecutar aplicaciones basadas en la consola.
  
#### Servicios de Terminal Server
  
Los **Servicios de Terminal Server** proporcionan un entorno de multisesión que permite que los dispositivos de cliente interactúen con sesiones virtuales de escritorio de Windows y programas basados en Windows que se ejecuten en un servidor.
  
De forma predeterminada, los **Servicios de Terminal Server** se instalan en el modo de administración remota en equipos con Windows Server 2003. Para instalar **Servicios de Terminal Server** en el modo de aplicación, utilice Configurar el servidor o Agregar o quitar componentes de Windows para cambiar el modo de **Servicios de Terminal Server**. Este servicio es necesario para utilizar el escritorio remoto en equipos con Windows Server 2003. En Windows XP, es necesario este servicio si desea utilizar la conmutación rápida de usuario, el escritorio remoto y la asistencia remota. En ambas versiones de Windows, este servicio se instala de forma predeterminada, con un tipo de inicio **Manual.**
  
Si el servicio **Servicios de Terminal Server** se detiene o si usted lo deshabilita, su equipo podría volverse poco fiable y la asistencia remota dejaría de estar disponible. Para evitar el uso remoto del equipo, desactive las casillas de verificación **Permitir asistencia remota** y **Permitir escritorio remoto** en la ficha **Acceso remoto** del cuadro de diálogo **Propiedades del sistema**.
  
#### Licencias de Servicios de Terminal Server
  
El servicio de **Licencias de Servicios de Terminal Server** instala un servidor de licencia y proporciona licencias de cliente registradas al conectar con un servidor Terminal Server. El servicio de **Licencia de Servicio de Terminal Server** es un servicio que tiene poco impacto y que almacena las licencias de clientes que se han emitido para un Terminal Server y luego hace un seguimiento de las licencias que se han emitido a equipos o terminales cliente. Este servicio sólo estará presente y sólo será necesario para servidores en los que el servicio de **Servicios de Terminal Server** se instala en el modo de aplicación.
  
Si desactiva el servicio **Licencias de Servicios de Terminal Server**, el servidor no podrá emitir licencias de Terminal Server a los clientes cuando las soliciten. Si se detecta otro servidor de licencia en un controlador de dominio del bosque, el servidor Terminal Server solicitante intentará utilizarlo.
  
#### Directorio de sesiones de Terminal Server
  
El servicio **Directorio de sesiones de Terminal Server** proporciona un entorno con varias sesiones que permite a los dispositivos cliente obtener acceso a una sesión de escritorio virtual de Windows y a programas basados en Windows que se ejecutan en Windows Server 2003.
  
El servicio **Directorio de sesiones de Terminal Server** permite a los clústeres de servidores Terminal Server con equilibrio de carga enrutar correctamente una solicitud de conexión de usuario al servidor en el que el usuario ya tiene una sesión activa. El servicio de equilibrio de carga de la red de Windows agrupa los recursos de proceso de varios servidores que utilizan el protocolo de red TCP/IP. Puede utilizar el servicio de equilibrio de carga de la red de Windows con un clúster de servidores Terminal Server para proporcionar un solo punto de acceso de Terminal Server a los usuarios al distribuir sesiones a través de múltiples servidores.
  
EL servicio **Directorio de sesiones de Terminal Server** realiza un seguimiento de las sesiones desconectadas del clúster y garantiza que los usuarios se vuelvan a conectar a esas sesiones. Este servicio se instala en equipos con Windows Server 2003 que tienen instalado el componente de Servicios de Terminal Server, pero el servicio se deshabilita de forma predeterminada. Microsoft recomienda que el servicio de **Directorio de sesiones de Terminal Server** se instale en un servidor que *no* sea un Terminal Server.
  
Si detiene el servicio de **Directorio de sesiones de Terminal Server**, las solicitudes de conexión se enrutarán al primer servidor disponible, independientemente de si tienen una sesión activa en otro lugar del clúster.
  
#### Temas
  
El servicio de **Temas** ofrece servicios de administración de temas para mejorar la experiencia del usuario. Este servicioofrece compatibilidad de procesamiento para la nueva GUI de Windows XP. Un tema de escritorio es un conjunto predefinido de iconos, fuentes, colores, sonidos y otros elementos que aportan al escritorio del equipo un aspecto unificado y distintivo. Puede cambiar de tema, crear uno propio modificándolo y guardándolo con un nuevo nombre o restaurar el aspecto tradicional de Windows clásico. En equipos Windows XP, el servicio de **Temas** está configurado para iniciarse automáticamente. En equipos Windows Server 2003, está deshabilitado.
  
Si se detiene o deshabilita el servicio de **Temas**, el nuevo estilo visual de Windows XP, ventanas, botones, barras de desplazamiento y otros controles volverá al estilo visual de Windows clásico.
  
#### Demonio FTP trivial
  
El servicio del **Demonio FTP trivial** (TFTP) no requiere un nombre de usuario ni una contraseña y forma parte integral de los Servicios de instalación remota (RIS) para Windows Server 2003. Este servicio incluye compatibilidad con el protocolo TFTP definido por las siguientes RFC:
  
-   RFC 1350 – TFTP
  
-   RFC 2347 – Extensión de opción
  
-   RFC 2348 - Opción de tamaño de bloque
  
-   RFC 2349 - Opciones de intervalo de tiempo de espera y tamaño de transferencia
  
El servidor de instalación remota utiliza el servicio **demonio FTP trivial** para descargar los archivos iniciales necesarios para comenzar el proceso de instalación remota. El archivo descargado con mayor frecuencia en el cliente a través de este servicio es Startrom.com, responsable del programa previo del equipo cliente. Si el usuario presiona F12 cuando se le solicita, se descarga el Asistente para instalación de clientes y comienza el proceso de instalación remota.
  
El **Demonio FTP Trivial** no se instala de forma predeterminada. Si detiene o deshabilita este servicio, los equipos cliente que soliciten el servicio RIS de este servidor no podrán instalarlo. La forma correcta de deshabilitar este servicio consiste en desinstalar los servicios de instalación remota.
  
#### Sistema de alimentación ininterrumpida
  
El servicio **Sistema de alimentación ininterrumpida** administra un sistema de alimentación ininterrumpida (UPS) conectado al equipo mediante un puerto serie. Este servicio de Telefonía se instala de forma predeterminada en Windows XP y Windows Server 2003, pero su tipo de inicio se configura como **Manual**.
  
Si detiene o deshabilita esteservicio, se perderán las comunicaciones con los UPS. Si hay un corte de corriente, es posible que el UPS no sea capaz de cerrar sin riesgos el equipo, lo que podría provocar la pérdida de datos.
  
#### Host de dispositivo Plug and Play universal
  
El servicio **Host de dispositivo Plug and Play universal** admite la funcionalidad Plug and Play universal de igual a igual para dispositivos de red. La especificación UPnP está diseñada para simplificar la instalación y administración del servicio de red y dispositivos. El UPNP realiza el descubrimiento del servicio y del dispositivo y los controla a través de mecanismos de protocolo basados en estándares.
  
Los dispositivos UPNP pueden configurar automáticamente las direcciones de red, anunciar su presencia en una subred de la red y habilitar el cambio de descripciones de dispositivo y servicio. Cuándo se instala el servicio de **host de dispositivo Plug and Play universal**, un equipo Windows XP puede actuar como punto de control UPNP para descubrir y controlar los dispositivos a través de una interfaz web o de aplicación. Este servicio se instala de forma predeterminada en equipos con Windows XP y Windows Server 2003, y se configura como **Manual**.
  
#### Administrador de carga
  
El servicio **Administrador de carga** administra la transferencia de archivos sincrónica y asincrónica entre los equipos clientes y los servidores de la red. Los datos del controlador se cargan de forma anónima desde los equipos cliente a Microsoft y, a continuación, se utilizan para ayudar a los usuarios a encontrar los controladores necesarios para sus equipos. El servidor de información de controladores de Microsoft pide permiso al cliente para cargar el perfil de hardware del equipo y, a continuación, busca en Internet información sobre cómo obtener el controlador adecuado o recibir soporte técnico adecuado de Microsoft o de terceros.
  
Los datos que se cargan desde el equipo con la finalidad de encontrar información sobre los controladores incluirán los números de identificación de hardware del dispositivo, la hora a la que finalizó el asistente para hardware de Windows y un Id. para el sistema operativo de Windows que se esté ejecutando. No se podrá realizar un seguimiento de la información del equipo cargada del usuario, equipo, organización, dirección IP ni cualquier otra fuente de información.
  
Los datos recopilados se utilizarán para realizar un seguimiento de los controladores de dispositivos que no se pueden obtener fácilmente. Si existe información adicional de controladores de dispositivos, quedará disponible después de que se cargue el número de identificación del dispositivo. Si, por el contrario, no hay disponible información adicional sobre controladores, Microsoft registrará el número de identificación del dispositivo para colaborar con los proveedores de hardware a fin de aumentar la disponibilidad de controladores de dispositivos para Windows o proporcionar información sobre la disponibilidad de controladores y compatibilidad de dispositivos.
  
El servicio **Administrador de carga** se instala y, de forma predeterminada, se configura en **Manual** en equipos con Windows Server 2003. Si se detiene el servicio, no tendrá lugar la transferencia de archivos sincrónica y asincrónica entre los clientes y los servidores de la red.
  
#### Servicio de disco virtual
  
El **Servicio de disco virtual** (VDS) ofrece una interfaz única para administrar el almacenamiento virtual de bloques en software de sistema operativo, subsistemas de hardware de almacenamiento de matriz redundante de discos independientes (RAID) u otros motores virtuales.
  
El **Servicio de disco virtual** proporciona una interfaz neutral con respecto a la tecnología y al proveedor para la administración de volúmenes lógicos (software) y unidades lógicas (hardware). Puede utilizar esta interfaz para administrar operaciones de enlace, la supervisión del rendimiento, el descubrimiento y seguimiento de la topología, el estado del volumen y el seguimiento de errores.
  
No debe confundir los discos virtuales con las instantáneas. A diferencia del **Servicio de Instantáneas de volumen**, el **Servicio de disco virtual** no se coordina con aplicaciones ni con el sistema de archivos, y los datos contenidos en un volumen no se sincronizarán antes de una operación de configuración de volumen o disco. Puede utilizar el **Servicio de disco virtual** para configurar un complejo de reflejo, pero es necesario un proveedor de instantáneas que realice la coordinación cuando se elimina el complejo y aparece la instantánea. Dicho uso queda fuera del ámbito de este documento con dos excepciones:
  
-   El **Servicio de disco virtual** se coordina con el sistema de archivos antes de ampliar o reducir volúmenes.
  
-   La copia de todas las instantáneas aparece como complejo en el **Servicio de disco virtual**.
  
El **Servicio de disco virtual** se instala y se configura en **Manual** en equipos con Windows Server 2003. El servicio sólo se inicia cuando una aplicación intenta utilizar los servicios VDS. Si se detiene, los servicios VDS dejarán de estar disponibles.
  
#### Instantáneas de volumen
  
El servicio **Instantáneas de volumen** administra e implementa instantáneas de volumen utilizadas para realizar copias de seguridad, entre otras funciones. El servicio administra las instantáneas de volumen. Cuando una aplicación de copia de seguridad intenta iniciar una copia de seguridad con la nueva infraestructura de instantáneas, la aplicación determina el número de editores que están activos actualmente en el servicio y, a continuación, consulta cada editor para reunir los metadatos necesarios. La aplicación de copia de seguridad puede recopilar los volúmenes que necesita para obtener una instantánea a fin de garantizar una sesión de copia de seguridad correcta. Los volúmenes se presentan en el coordinador de instantáneas y se crea una instantánea que, a su vez, crea volúmenes que coinciden con los volúmenes originales en el momento de la instantánea.
  
El servicio **Instantáneas de volumen** se instala en equipos con Windows XP y Windows Server 2003, y su estado de inicio se configura como **Manual.** Si detiene el servicio, las instantáneas no estarán disponibles para la copia de seguridad, por lo que este proceso no tendrá lugar. En particular, el servicio **Instantáneas de volumen** es necesario para Copias de seguridad de Windows y aplicaciones de copia de seguridad que dependen de la API de Copia de seguridad de Windows.
  
#### Cliente web
  
El servicio **WebClient** permite que las aplicaciones Win32 puedan obtener acceso a documentos que se encuentran en Internet. El servicio extiende la capacidad de la red de Windows; le permite a las aplicaciones estándar de Win32 crear, leer, y escribir archivos en servidores de archivos de Internet a través del uso de WebDAV, un protocolo de acceso a archivos que se describe en XML y se comunica a través de HTTP. Al utilizar el HTTP estándar, WebDAV se ejecuta en infraestructuras de Internet existentes, como servidores de seguridad y enrutadores.
  
El servicio **WebClient** se instala tanto en equipos con Windows XP como con Windows Server 2003. En Windows XP, el servicio se inicia automáticamente. En Windows Server 2003, el servicio está deshabilitado. Si detiene el servicio **WebClient**, los usuarios del equipo no podrán utilizar el Asistente para la publicación en Web para publicar datos en ubicaciones de Internet que utilicen el protocolo WebDAV.
  
#### Administrador de elementos web
  
El servicio **Administrador de elementos web** se instala sólo en equipos con Windows Server 2003, Web Edition. Sirve a los elementos web de la interfaz de usuario para el sitio web de administración en el puerto 8098, que determinan la siguiente información:
  
-   Fichas que se van a mostrar en el sitio web de administración
  
-   Tareas de administración remota que están disponibles para el administrador
  
-   Contenido
  
-   Temas de ayuda
  
-   Alertas de administración remota que se pueden mostrar
  
Para administrar de forma remota un servidor, un administrador puede conectarse al servidor en http://*&lt;servername&gt;*:8098. Cuando este sitio web recibe una conexión, el código predeterminado de Páginas Active Server (ASP) consulta el servicio **Administrador de elementos web** en busca de cada uno de los tipos de información a los que se hace referencia. Una vez recopilada toda la información, se muestra en el administrador la página web adecuada.
  
El servicio **Administrador de elementos web** carga toda la información en el momento del inicio y el cliente, en este caso el código ASP, solicita los elementos web de la interfaz de usuario a través de la interfaz COM. El servicio se ejecuta en la cuenta del sistema local y sólo se aceptan solicitudes sobre la interfaz COM de aquellos clientes que se ejecutan en la cuenta del administrador o del sistema local. Si detiene el servicio o si se configura como **manual,** se iniciará cuando reciba la siguiente solicitud de elementos de la interfaz de usuario web.
  
El servicio **Administrador de elementos web** se reinicia automáticamente cuando se tenga acceso a la interfaz web para la administración remota. Si deshabilita este servicio, cualquier otro servicio que dependa directamente del mismo no se podrá iniciar y la interfaz de usuario web de herramientas de administración remota para la administración del servidor no funcionará correctamente.
  
#### Audio de Windows
  
El servicio de **Audio de Windows** ofrece compatibilidad para el sonido y otras funciones relacionadas con el audio de Windows. Este servicio administra eventos compatibles con Plug and Play para los dispositivos de audio como las tarjetas de sonido y efectos de sonido globales (GFX) para las interfaces de programación de aplicaciones de audio de Windows. Ejemplos de GFX son la ecualización (EQ), el refuerzo de graves y la corrección de los altavoces. El servicio carga, descarga y almacena o restaura el estado de los GFX por sesión.
  
A través del panel de control Multimedia los usuarios pueden realizar lo siguiente:
  
-   Habilitar o deshabilitar un GFX.
  
-   Seleccionar entre varios filtros de GFX, si hay más de uno disponible que se haya diseñado para el hardware de audio específico. Un archivo INF del controlador de GFX especifica el hardware de destino para GFX.
  
El servicio de **Audio de Windows** se instala en equipos con Windows Server 2003 y Windows XP y se configura para iniciarse automáticamente en equipos que ejecutan Windows XP y Windows Server 2003, Standard Edition. El servicio se deshabilita en otras ediciones de Windows Server 2003.
  
No es posible detener el servicio **Audio de Windows** una vez iniciado. Si se deshabilita este servicio, la funcionalidad de audio podría verse afectada, con lo cual puede que no se escuche sonido o que no se procese GFX.
  
#### Servidor de seguridad de conexión a Internet y Conexión compartida a Internet de Windows
  
El servicio **Servidor de seguridad de conexión a Internet y Conexión compartida a Internet de Windows** (ICS**) **proporciona servicios de traducción de direcciones de red (NAT), direccionamiento y resolución de nombres y servicios de prevención de intrusión en todos los equipos de una red doméstica o de pequeña empresa a través de una conexión de acceso telefónico o banda ancha.
  
Cuando este servicio está habilitado, el equipo se convierte en una “puerta de enlace de Internet” en la red. Permite a otros equipos clientes compartir una conexión a Internet, compartir archivos y utilizar las mismas impresoras. Este servicio dispone de una directiva de grupo que reconoce la ubicación.
  
Anteriormente se denominaba Conexión compartida a Internet en Windows 2000 y Windows XP Service Pack 1. No se incluyó en la versión original de Windows Server 2003.
  
El servicio **Servidor de seguridad de conexión a Internet y Conexión compartida a Internet de Windows** es un servicio predeterminado que se instala y se inicia automáticamente en equipos con Windows XP. El servicio se instala también en equipos Windows Server 2003 de forma predeterminada, pero se configura como **Deshabilitado.**
  
Si se detiene el servicio **Servidor de seguridad de conexión a Internet y Conexión compartida a Internet de Windows**, los servicios de red tales como Internet compartido, la resolución de nombres, la resolución de direcciones y/o la prevención de intrusión no estarán disponibles. Los clientes de la red podrían no tener acceso a Internet y sus direcciones IP caducarán, lo que hará que algunos clientes utilicen las direcciones IP privadas automáticas (APIPA) para la conectividad de red de igual a igual.
  
#### Adquisición de imágenes de Windows (WIA)
  
El servicio **Adquisición de imágenes de Windows (WIA)** proporciona servicios de adquisición de imágenes para escáneres y cámaras.
  
Windows Server 2003 admite dispositivos de imágenes fijas a través de este servicio, que utiliza la arquitectura del modelo de controladores de Windows (WDM). El servicio proporciona una sólida comunicación entre aplicaciones y dispositivos de captura de imágenes, lo que le permite capturar imágenes de forma eficaz y transferirlas al equipo para su edición y uso. El servicio es necesario para capturar eventos generados por dispositivos de imágenes.
  
El servicio **Adquisición de imágenes de Windows (WIA)** admite la interfaz estándar de equipos pequeños (SCSI), IEEE 1394, USB, y dispositivos digitales en serie de imagen fija. La compatibilidad con dispositivos de imágenes fijas de infrarrojos, en paralelo y en serie, procede de las interfaces ya existentes de infrarrojos, en paralelo y en serie. Los escáneres de imágenes y las cámaras digitales son ejemplos de dispositivos de imágenes fijas. El servicio admite también Webcams y cámaras de vídeo digital basadas en Microsoft DirectShow® para capturar fotogramas de vídeo.
  
El servicio **Adquisición de imágenes de Windows (WIA)** se instala y se configura como **Manual** en equipos con Windows XP, y se instala y se deshabilita de forma predeterminada en equipos Windows Server 2003. Si detiene el servicio, no se capturarán ni procesarán los eventos de los dispositivos de imágenes. El servicio se reiniciará automáticamente al inicio si hay instalado un dispositivo WIA. Además, se reinicia cada vez que se abre una aplicación habilitada para WIA.
  
#### Windows Installer
  
El servicio **Windows Installer** administra la instalación y la eliminación de aplicaciones. Aplica un conjunto de reglas definidas centralmente durante el proceso de instalación que especifica cómo se instalan y se configuran las aplicaciones. También puede usar este servicio para modificar, reparar o eliminar las aplicaciones existentes. La tecnología de este servicio integra el servicio **Windows Installer** para los sistemas operativos Windows y el formato de archivos del paquete (.msi) que se utiliza para mantener información de la instalación y la configuración de la aplicación.
  
El servicio **Windows Installer** no es sólo un programa de instalación, sino un sistema de administración de software extensible. Este servicio administra la instalación, incorporación y eliminación de componentes de software, controla la resistencia de archivos y mantiene la recuperación básica de desastres utilizando opciones de restauración. También admite la instalación y operación de software de distintas fuentes y lo pueden personalizar los desarrolladores que deseen instalar aplicaciones personalizadas.
  
De forma predeterminada, el servicio de **Windows Installer** se instala y se configura como **Manual** en equipos con Windows XP y Windows Server 2003. Las aplicaciones que utilizan el instalador inician el servicio. Si este servicio se detiene, las aplicaciones que lo utilizan no podrán instalarse, eliminarse, repararse o modificarse. Asimismo, es probable que no se puedan ejecutar una serie de aplicaciones que lo utilizan cuando están activas.
  
#### Servicio de nombres Internet de Windows (WINS)
  
El **Servicio de nombres Internet de Windows (WINS)** permite la resolución de nombres NetBIOS. La presencia de servidores WINS es crucial para localizar los recursos de la red que pueden identificarse mediante nombres NetBIOS. Se requieren servidores WINS a menos que todos los dominios se hayan actualizado a Active Directory y que todos los equipos de la red ejecuten Windows 2000 Server o versiones posteriores del sistema operativo Windows.
  
Si detiene este servicio, ocurrirán los siguientes cambios en la funcionalidad:
  
-   No se podrán localizar los dominios y controladores de dominio de Windows NT4.0.
  
-   No se podrán localizar los dominios y controladores de dominio de Windows 2000 o Windows Server 2003 Active desde clientes con Windows NT 4.0.
  
-   Se producirá un error en la resolución de nombres NetBIOS, a menos que el dispositivo cuyo nombre se debe resolver esté en la misma subred que el dispositivo que intenta la resolución de nombres. Se debe configurar el dispositivo para que intente la resolución de nombres NetBIOS a través de difusiones.
  
El servicio **WINS** sólo estará presente en equipos Windows Server 2003 que se hayan configurado para actuar como servidor WINS.
  
#### Instrumental de administración de Windows
  
El servicio **Instrumental de administración de Windows** proporciona una interfaz común y un modelo de objeto para obtener acceso a la información de administración de sistemas operativos, dispositivos, aplicaciones y servicios. La WMI es una infraestructura que proporciona la capacidad para construir aplicaciones e instrumentos de administración, y se incluye como parte de la generación actual de sistemas operativos de Microsoft.
  
La infraestructura de WMI es un componente del sistema operativo Microsoft Windows que transfiere y almacena información sobre objetos administrados. La integran dos componentes: el servicio **Instrumental de administración de Windows** y el repositorio de WMI. El servicio actúa como intermediario entre los proveedores, las aplicaciones de administración y el repositorio de WMI, en el que incluye información de un proveedor. Este servicio también tiene acceso al repositorio de WMI cuando tienen lugar consultas e instrucciones de las aplicaciones de administración. Por último, permite pasar información directamente entre un proveedor y una aplicación de administración. Por el contrario, el repositorio de WMI actúa como área de almacenamiento para la información que introducen los distintos proveedores.
  
El servicio **Instrumental de administración de Windows** proporciona acceso a los datos de administración a través de una serie de interfaces, incluidas las API COM, las secuencias de comandos y las interfaces de línea de comandos. Es compatible con las anteriores interfaces y protocolos de administración como, por ejemplo, el protocolo simple de administración de redes (SNMP). Este servicio se instala y se ejecuta automáticamente en equipos con Windows XP y Windows Server 2003. Si se detiene este servicio, la mayor parte del software basado en Windows no funcionará correctamente.
  
#### Extensiones de controlador de Instrumentalde administración de Windows
  
El servicio **Extensiones de controlador de Instrumental de administración de Windows** supervisa todos los controladores y proveedores de seguimiento de eventos que se han configurado para publicar WMI o información de seguimiento de eventos. De forma predeterminada, este servicio se instala en equipos con Windows XP y Windows Server 2003 y se configura en **Manual.**
  
#### Servicios de Windows Media
  
El servicio **Servicios de Windows Media** proporciona servicios de medios de transmisión a través de redes basadas en IP. Estos servicios sustituyen los cuatro servicios independientes que incluían las versiones 4.0 y 4.1 de los Servicios de Windows Media:
  
-   Servicio Monitor de Windows Media
  
-   Servicio Programa de Windows Media
  
-   Servicio Estación de Windows Media
  
-   Servicio Monodifusión de Windows Media
  
**Servicios de Windows Media** constituye ahora un único servicio que se ejecuta en Windows Server 2003 Standard Edition, Windows Server 2003 Enterprise Edition, Windows Server 2003 Datacenter Edition y Windows Server 2003 Web Edition. Sus componentes principales se han desarrollado con COM y se ha creado una arquitectura flexible que se puede personalizar fácilmente para aplicaciones específicas. Es compatible con una mayor variedad de protocolos de control, entre ellos el protocolo de transmisión en tiempo real (RTSP), el protocolo Microsoft Media Server (MMS) y HTTP.
  
La plataforma **Servicios de Windows Media** es compatible con los siguientes estándares de la industria:
  
-   WMI para servicios de mensajería y notificación de eventos de servidor
  
-   SNMP para componentes de red
  
-   XML, lenguaje de integración multimedia sincronizada (SMIL) 2.0 y el modelo de objetos de documento (DOM) para la implementación de la lista de reproducción
  
-   Moving Picture Experts Group (MPEG) 1 y 2 para formatos de audio y vídeo
  
La mayoría de los escenarios multimedia de transmisión por secuencias utilizan los componentes principales que se instalan con **Servicios de Windows Media**. Sin embargo, para los escenarios más avanzados es posible que precise incorporar trabajo personalizado de programación e integración. Para los desarrolladores e integradores de sistemas, el SDK de **Servicios de Windows Media** proporciona acceso a todos los elementos del servidor a través de una combinación de complementos, un modelo de objetos totalmente documentado y una amplia variedad de notificaciones de eventos externas, todos ellos diseñados para que se puedan personalizar fácilmente.
  
Los **Servicios de Windows Media** son un servicio opcional que se debe instalar por separado en equipos con Windows Server 2003. Si se deshabilita o detiene este servicio, los servicios multimedia de transmisión por secuencias podrían dejar de estar disponibles.
  
#### Administrador de recursos del sistema de Windows
  
El servicio **Administrador de recursos del sistema de Windows** (WSRM) es una herramienta opcional que ayuda a los clientes a implementar aplicaciones en escenarios de consolidación. Proporciona administración basada en directivas del uso de la CPU y la memoria de los procesos que se ejecutan en una sola instancia de un sistema operativo. Los escenarios planeados incluyen varias aplicaciones de servidor heterogéneas, varios usuarios de Servicios de Terminal Server, varias instancias de SQL Server y varios grupos de aplicaciones IIS V6 o Exchange e IIS V6 juntos en el mismo equipo.
  
Los destinos de ancho de banda, expresados mediante porcentajes del uso de la CPU del sistema, son la opción principal para la administración de la CPU. Para mantener los objetivos, las prioridades del proceso se supervisan y se ajustan de forma dinámica. El servicio **WSRM** ofrece administración de afinidad, proporcionada mediante el uso de varias API por proceso para la afinidad segura.
  
Las opciones de administración de memoria incluyen límites de conjunto de trabajo y memoria máxima asignada aplicada por procesos. Los límites de conjunto de trabajo se definen en la directiva y WRM los aplica a través de una API de núcleo. Posteriormente, el administrador de memoria del núcleo paginará el proceso para aplicar y mantener los límites dentro del tamaño del conjunto de trabajo. La memoria asignada se controla muy fácilmente en un límite superior. Cuando se supera el límite superior, se termina el proceso o se registra un evento, a elección del usuario.
  
Las características adicionales incluyen características completas de calendario para la programación de las directivas deseadas, coincidencia de patrones sofisticados con procesos de identificación en el tiempo de ejecución, contadores específicos de WRM y un sistema de contabilidad de trabajo básico.
  
El servicio **WSRM** se implementa como una opción y se ejecuta en sistemas con versiones del sistema operativo Windows que se publicaron después de Windows 2000 Service Pack 3. Los componentes del servidor se pueden instalar en equipos con Windows Server 2003, Datacenter Edition y Windows Server 2003, Enterprise Edition (más las versiones x64 de estas ediciones). El cliente de WSRM se debe instalar en cada equipo administrado. Para la administración del servicio, se proporcionan un complemento MMC y programas de línea de comandos. Estas partes del cliente se pueden instalar y ejecutar en cualquier equipo Windows 2000, Windows XP Professional o Windows .NET. Puede que el servicio sólo esté instalado y se ejecute en .NET Datacenter y .NET Enterprise. Estos SKU se aplican en el momento de la instalación y en tiempo de ejecución.
  
#### Horario de Windows
  
El servicio de **hora de Windows** mantiene la sincronización de fecha y hora de todos los equipos de una red Windows. Utiliza el protocolo de tiempo de la red (NTP) para sincronizar los relojes de los equipos, de forma que se puede asignar un valor de reloj exacto (o marca de hora) a las solicitudes de validación de red y de acceso a recursos. La implementación de NTP y la integración de los proveedores horarios hacen que el servicio de **hora de Windows** sea un servicio fiable y adaptable para los administradores. Para equipos que no forman parte de un dominio, puede configurar el servicio de **hora de Windows** para que sincronice el horario con una fuente horaria externa. Si desactiva el servicio, la configuración horaria de los equipos locales no estará sincronizada con ningún servicio horario del dominio de Windows ni con un servicio horario configurado externamente.
  
Si detiene o deshabilita el servicio de **hora de Windows**, la sincronización de la fecha y hora no estará disponible en el bosque ni de un servidor NTP externo. Existen dos posibles escenarios:
  
-   Si se detiene el servicio de **hora de Windows** en una estación de trabajo, la estación de trabajo no será capaz de sincronizar su tiempo con otra fuente, pero ningún otro servidor externo se verá afectado
  
-   Si se detiene el servicio de **hora de Windows** en un controlador de dominio, se producirá el mismo efecto que en la situación anterior, pero los miembros del dominio tampoco podrán sincronizar su tiempo con él. Esta incapacidad para sincronizar puede afectar de forma negativa la sincronización de tiempo en la organización.
  
De forma predeterminada, el servicio de **hora de Windows** se instala y se inicia automáticamente en equipos con Windows XP y Windows Server 2003.
  
**Nota**: para más información acerca del servicio de **hora de Windows** en equipos con Windows Server 2003, consulte "[Cómo funciona el servicio de hora de Windows](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/techref/71e76587-28f4-4272-a3d7-7f44ca50c018.mspx)" en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/  
TechRef/71e76587-28f4-4272-a3d7-7f44ca50c018.mspx y "[Configuración y herramientas del servicio de hora de Windows](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/techref/b43a025f-cce2-4c82-b3ea-3b95d482db3a.mspx)" en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/TechRef/  
b43a025f-cce2-4c82-b3ea-3b95d482db3a.mspx.
  
#### Servicio de Descubrimiento automático de proxy web WinHTTP
  
El **Servicio de Descubrimiento automático de proxy web WinHTTP** implementa el protocolo de descubrimiento automático de proxy web (WPAD) para los servicios HTTP de Windows (WinHTTP). WPAD es un protocolo que permite a un cliente HTTP descubrir automáticamente la configuración de un proxy.
  
Si detiene o deshabilita el servicio,el protocolo WPAD se ejecutará dentro del proceso del cliente HTTP en lugar de en un proceso de servicio externo, y no se produciría la pérdida de funcionalidad. Este servicio se instala en equipos con Windows Server 2003 de forma predeterminada y su tipo de inicio se configura como **Manual.**
  
#### Configuración inalámbrica
  
El servicio **Configuración inalámbrica** permite la configuración automática para adaptadores inalámbricos IEEE 802.11 en comunicaciones inalámbricas. Microsoft ha colaborado con proveedores de tarjetas de interfaz de red (NIC) 802.11 para automatizar el proceso de configuración NIC, que asocia el NIC con una red disponible y mejora la experiencia inalámbrica itinerante en Windows.
  
**Nota**: el servicio de **Configuración inalámbrica** se marca como el servicio del **sistema Configuración inalámbrica** en equipos con Windows XP.
  
La tarjeta de interfaz de red inalámbrica y su especificación de interfaz de controlador de red (NDIS) se limitan prácticamente a ofrecer compatibilidad para algunos nuevos identificadores de objeto (OID) NDIS, utilizados para la consulta y la configuración del comportamiento de los dispositivos y controladores. NIC buscará redes disponibles y pasará la información a Windows. El servicio **Configuración inalámbrica** se ocupa de configurar la tarjeta NIC para una red disponible. Cuando hay dos redes que cubren la misma área, el usuario puede configurar el orden de red que prefiera y el equipo probará cada red en el orden correspondiente hasta que encuentre una activa. También se puede limitar la asociación a únicamente las redes configuradas que se deseen.
  
El servicio **Configuración inalámbrica** se instala y se inicia automáticamente en equipos con Windows Server 2003 y Windows XP (a excepción de Windows Server 2003, Web Edition, que lo configura como **Manual**). Si detiene este servicio, la configuración inalámbrica automática no estará disponible.
  
#### Adaptador de rendimiento de WMI
  
El servicio **Adaptador de rendimiento de WMI** proporciona información de la biblioteca de rendimiento a través de los proveedores HiPerf de WMI. Las aplicaciones y servicios que necesitan proporcionar contadores de rendimiento hoy en día pueden hacerlo de dos formas distintas: escribiendo un proveedor de alto rendimiento de WMI o escribiendo una biblioteca de rendimiento. Los usuarios de datos de alto rendimiento también tienen dos formas de solicitar datos de rendimiento; a través de WMI o mediante las API del Ayudante de los datos de rendimiento (PDH). Existen mecanismos que permiten que los dos modelos interactúen entre sí y que los clientes que tienen acceso a los contadores a través de cada modelo puedan seguir viendo los contadores que proporciona el otro modelo. El adaptador inverso es uno de esos mecanismos.
  
El servicio **Adaptador de rendimiento de WMI** transforma los contadores de rendimiento proporcionados por los proveedores de alto rendimiento de WMI en contadores que puede utilizar el ayudante PDH a través de la biblioteca de rendimiento del adaptador inverso. Este enfoque proporciona a los clientes PDH como Sysmon la capacidad de consumir contadores de rendimiento de cualquier proveedor WMI de alto rendimiento en el equipo.
  
Aunque se instale de forma predeterminada en Windows XP y Windows Server 2003, el servicio de **Adaptador de rendimiento de WMI** es un servicio manual; no se ejecuta de forma predeterminada. Se ejecuta a petición siempre que un cliente de rendimiento (por ejemplo, Sysmon) utiliza el Ayudante de los datos de rendimiento (PDH) para consultar los datos de rendimiento. Una vez desconectado el cliente, el servicio se detiene.
  
Si detiene el servicio **Adaptador de rendimiento de WMI**, los contadores de rendimiento de WMI no estarán disponibles.
  
#### Estación de trabajo
  
El servicio **Estación de trabajo** se instala y se ejecuta automáticamente de forma predeterminada en equipos con Windows XP y Windows Server 2003. Este servicio crea y mantiene las conexiones de red y comunicaciones del cliente. Este servicioes una envoltura en modo de usuario para el redirector de redes Microsoft. Carga y realiza funciones de configuración para el redirector, proporciona compatibilidad para establecer conexiones de red a servidores remotos, ofrece compatibilidad para las API WNet y facilita estadísticas del redirector.
  
Si deshabilita el servicio **Estación de trabajo**, los clientes no podrán establecer conexiones con los servidores remotos ni obtener acceso a los archivos mediante las canalizaciones con nombre. Los clientes y los programas no podrán tener acceso a los archivos y las impresoras en otros equipos remotos, pero la conectividad TCP/HTTP no se ve afectada. La exploración de Internet y el acceso al cliente web seguirán funcionando.
  
#### Servicio de publicación de World Wide Web
  
El **Servicio de publicación World Wide Web** proporciona conectividad y administración web de los sitios web a través del complemento de IIS de MMC. El servicio ofrece servicios HTTP para aplicaciones en la plataforma de Windows y contiene un administrador de procesos y uno de configuración. El administrador de procesos controla los procesos en los que residen las aplicaciones y los sitios web. El administrador de configuración, por su parte, lee la configuración del equipo almacenada y garantiza que Windows esté configurado para enrutar las solicitudes HTTP a los grupos de aplicaciones adecuadas o a los procesos del sistema operativo.
  
Este servicio puede controlar los procesos que alojan las aplicaciones personalizadas y proporciona servicios de reciclaje para dichas aplicaciones. El reciclaje es una propiedad de configuración de un grupo de aplicaciones y se puede realizar según los límites de la memoria, los de las solicitudes, el tiempo de procesamiento o la hora del día. El servicio incluirá las solicitudes HTTP en la cola si las aplicaciones personalizadas dejan de responder, y también intentará reiniciarlas.
  
Este servicio es un componente opcional que se puede instalar en Windows Server 2003 o Windows XP como parte del paquete IIS. Si detiene el **Servicio de publicación World Wide Web**, el sistema operativo Windows Server 2003 no podrá responder a ningún formulario de solicitud web.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de algunos de los parámetros de configuración que se tratan en este capítulo:
  
-   La descripción detallada sobre cómo configurar y bloquear clústeres en Windows Server está fuera del ámbito de esta guía. Sin embargo una fuente importante de orientación es el artículo 891597 de Microsoft Knowledge Base “[How to apply more restrictive security settings on a Windows Server 2003–based cluster server](http://support.microsoft.com/kb/891597)” en http://support.microsoft.com/kb/891597.
  
-   El Asistente para configuración de seguridad (SCW) de Windows Server 2003 incluye una base de datos de configuración con descripciones e información acerca de los servicios disponibles en Windows Server 2003 y muchos otros productos de servidor de Microsoft. Para examinar esta base de datos, puede instalar el componente de SCW en cualquier equipo con Windows Server 2003 e iniciar el SCW.
  
-   Una lista de diversos servicios de Windows Server 2003 e información relacionada de puertos de red está disponible en el artículo de Microsoft Knowledge Base “[Service overview and network port requirements for the Windows Server system](http://support.microsoft.com/kb/832017)” en http: //support.microsoft.com/kb/832017.
  
-   SDDL se describe en detalle en el artículo "[Security Descriptor Definition Language](http://msdn.microsoft.com/en-us/library/aa379567(vs.85).aspx)" en MSDN® en http://msdn.microsoft.com/library/en-us/secauthz/  
    security/security\_descriptor\_definition\_language.asp.
  
-   Para obtener más información acerca de cómo proteger los Servicios de Terminal Server, consulte “[Securing Windows 2000 Terminal Services](http://www.microsoft.com/technet/prodtechnol/win2kts/maintain/optimize/secw2kts.mspx)”. La información en este artículo es también pertinente para Windows Server 2003, y está disponible en www.microsoft.com/technet/prodtechnol/win2kts/maintain/optimize/secw2kts.mspx.
  
-   Para más información acerca de la configuración predeterminada de los servicios en Windows Server 2003, consulte la página [Configuración predeterminada de los servicios](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/2b1dc6cf-2e34-4681-9aa6-8d0ffba2d3e3.mspx)en Microsoft TechNet en www.microsoft.com/resources/documentation/windowsserv/2003/standard/proddocs/en-us/sys\_srv\_default\_settings.asp.
  
-   Para obtener más información acerca de cómo restaurar la configuración de seguridad predeterminada de forma local, consulte el artículo de Microsoft Knowledge Base "[Cómo devolver la configuración de seguridad a los valores predeterminados](http://support.microsoft.com/?scid=313222)” en http://support.microsoft.com/?scid=313222.
  
-   Para obtener más información acerca de cómo restaurar la configuración de seguridad predeterminada en los objetos de directiva de grupo del domino integrados, consulte el artículo de Microsoft Knowledge Base "[Cómo restablecer derechos de usuario en la directiva de grupo del dominio predeterminada en Windows Server 2003](http://support.microsoft.com/?scid=324800)" en http://support.microsoft.com/?scid=324800.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 8: Directivas de restricción de software
  
Las directivas de restricción de software son una característica nueva en Microsoft® Windows® XP y Microsoft Windows Server™ 2003. Proporcionan un sistema basado en directivas para especificar qué programas se pueden ejecutar y cuáles no.
  
[](#klaa)[La amenaza del software malintencionado](#klaa)  
[](#lkaa)[Información adicional](#lkaa)
  
### La amenaza del software malintencionado
  
El incremento en el uso de las redes informáticas y de Internet en las actividades empresariales diarias hace que sea más probable que nunca que los usuarios de la empresa se topen con software malintencionado. Las directivas de restricción de software pueden ayudar a las empresas a protegerse, ya que proporcionan una capa adicional de defensa contra virus, troyanos y otros tipos de código malintencionado.
  
#### Vulnerabilidad
  
Las personas utilizan las redes para colaborar de formas cada vez más sofisticadas; utilizan el correo electrónico, la mensajería instantánea y las aplicaciones de igual a igual. El aumento en las posibilidades de colaboración incrementa de igual forma el riesgo de virus, gusanos y otros tipos de software malintencionado. Es importante recordar que el correo electrónico y la mensajería instantánea pueden transportar código hostil no solicitado, y que ese código hostil puede adoptar muchas formas, desde archivos ejecutables nativos de Windows (.exe) a macros en documentos de procesamiento de textos (.doc) o secuencias de comandos (.vbs).
  
Los virus y los gusanos a menudo se transmiten en mensajes de correo electrónico, y suelen incluir técnicas de ingeniería social que engañan a los usuarios para que realicen una acción que activa el código malintencionado. Debido al abrumador número de virus y a la gran variedad de formas que puede adoptar el código malintencionado, resulta complicado que los usuarios distingan qué código pueden ejecutar con seguridad y cuál no. Cuando se activa, el código hostil puede dañar el contenido del disco duro, inundar de forma masiva una red con solicitudes que provocan un ataque de denegación de servicio (DoS), enviar información confidencial a Internet o poner en peligro la seguridad de un equipo.
  
#### Contramedida
  
Diseñe unas directivas de restricción de software sólidas y seguras en los equipos de usuario final en su empresa y, a continuación, realice pruebas de laboratorio con estas directivas antes de implementarlas en un entorno de producción.
  
#### Impacto potencial
  
Una implementación defectuosa de las directivas de restricción de software puede deshabilitar aplicaciones necesarias o permitir la ejecución de programas hostiles. Por lo tanto, resulta esencial que las empresas dediquen suficientes recursos a las labores de administración y solución de problemas de la implementación de directivas.
  
**Nota**: aunque las directivas de restricción de software son una herramienta importante para mejorar la seguridad de los equipos, no son el sustituto de otras medidas de seguridad como los programas antivirus, los servidores de seguridad y las listas de control de acceso (ACL) restrictivas.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca del diseño y la utilización de las directivas de restricción de software:
  
-   El artículo "[Microsoft Windows XP: uso de directivas de restricción de software para proteger contra software no autorizado](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/rstrplcy.mspx)" en www.microsoft.com/technet/prodtechnol/winxppro/  
    maintain/rstrplcy.mspx describe la forma de implementar directivas de restricción de software en equipos con Windows XP.
  
-   El [capítulo 6](http://www.microsoft.com/technet/security/prodtech/windowsxp/secwinxp/xpsgch06.mspx) de la *Guía de seguridad de Windows XP* en www.microsoft.com/technet/security/  
    prodtech/windowsxp/secwinxp/xpsgch06.mspx describe los detalles del diseño e implementación de directivas de restricción de software para equipos cliente con Windows XP.
  
-   El artículo de Microsoft Knowledge Base "[How To Use Software Restriction Policies in Windows Server 2003](http://support.microsoft.com/default.aspx?kbid=324036)" en http://support.microsoft.com/default.aspx?kbid=324036 describe los detalles de la implementación de directivas de restricción de software en sistemas con Windows Server 2003 y en dominios de servicio de directorio de Active Directory®.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 9: Plantillas administrativas de Windows XP y Windows Server 2003
  
En las plantillas administrativas de Directiva de grupo se incluyen valores basados en el Registro que determinan el comportamiento y el aspecto de los equipos del entorno. Estos valores también influyen en el comportamiento de los componentes y aplicaciones del sistema operativo. Existen cientos de estos valores disponibles para su configuración y se pueden importar archivos .adm adicionales para que haya más configuraciones disponibles.
  
En este capítulo se enumera la configuración de Plantilla administrativa que está en el nodo de Configuración del equipo de la Directiva de grupo que se define en esta guía, así como en el nodo Configuración de usuario. En este capítulo no se examinan todos los parámetros disponibles en las Plantillas administrativas para Microsoft® Windows® XP y Microsoft Windows Server™ 2003. Sin embargo, sí se proporciona la orientación para todos los parámetros relacionados con la seguridad en equipos en los que se ejecutan estos sistemas operativos. Algunas de las configuraciones no incluidas son específicas de: compatibilidad de aplicación, Programador de tareas, Windows Installer, Windows Messenger y Reproductor de Windows Media®.
  
Las versiones anteriores de esta guía incluían información acerca de las Plantillas administrativas para Office XP. Microsoft Office 2003 contiene muchas características nuevas y cambios a las Plantillas administrativas que se incluyen en el producto. Para obtener más información acerca de estos cambios, consulte la sección "Información adicional" al final de este capítulo.
  
[](#eckl)[Parámetros de Configuración del equipo](#eckl)  
[](#eblk)[Parámetros de Configuración de usuario](#eblk)  
[](#eacz)[Información adicional](#eacz)
  
### Parámetros de Configuración del equipo
  
Los siguientes parámetros de configuración se aplican a equipos que son miembros de un dominio de servicio de directorio Active Directory®. La información acerca de los parámetros de configuración de usuario se proporciona más adelante en este capítulo.
  
#### NetMeeting
  
Microsoft NetMeeting® permite que los usuarios mantengan reuniones virtuales en la red de la organización. Puede establecer la configuración de directiva de grupo de NetMeeting en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\**  
**NetMeeting**
  
##### Desactivar el uso compartido de escritorio remoto
  
Esta configuración de directiva le permite deshabilitar la función de escritorio remoto compartido de NetMeeting. Puede habilitar esta configuración de directiva para que los usuarios no puedan configurar NetMeeting para contestar automáticamente a las llamadas entrantes y permitir el control remoto del escritorio local.
  
Los valores posibles para la configuración **Desactivar el uso compartido de escritorio remoto** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Cuando esta configuración de directiva se habilita, los usuarios no podrán utilizar la función de escritorio compartido de NetMeeting.
  
###### Contramedida
  
Establezca **Desactivar el uso compartido de escritorio remoto** como **Habilitado**.
  
###### Impacto potencial
  
Los usuarios no podrán configurar el escritorio remoto compartido a través de NetMeeting, aunque seguirán pudiendo utilizar las características de Asistencia Remota y Escritorio Remoto de Windows si las han dejado habilitadas.
  
#### Configuración de equipo de Internet Explorer
  
Microsoft Internet Explorer es el explorador web que se distribuye con Windows XP y Windows Server 2003. Puede administrar varias de sus características a través de Directiva de grupo. Puede establecer la configuración de directiva de grupo de equipo con Internet Explorer en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\**  
**Internet Explorer**
  
##### Deshabilitar la instalación automática de componentes de Internet Explorer
  
Esta configuración de directiva le permite evitar la descarga automática de componentes a través de Internet Explorer cuando los usuarios exploren sitios web que los requieran para el total funcionamiento del explorador. Si deshabilita o no establece esta configuración de directiva, se pedirá a los usuarios que descarguen e instalen componentes cada vez que visiten los sitios web que los utilicen. El objetivo de esta configuración de directiva es ayudar a los administradores a controlar qué componentes puede instalar el usuario.
  
Los valores posibles para la configuración **Deshabilitar la instalación automática de componentes de Internet Explorer** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los operadores de sitios web malintencionados pueden alojar componentes que contengan código hostil. Los usuarios en su organización podrían descargar sin saberlo este código y ejecutarlo en los equipos de su entorno, lo que podría exponer los datos confidenciales, causar pérdidas de datos y crear inestabilidad.
  
###### Contramedida
  
Configure **Deshabilitar la instalación automática de componentes de Internet Explorer** como **Habilitado**.
  
###### Impacto potencial
  
Internet Explorer no podrá descargar de forma automática los componentes cuando los usuarios exploren los sitios web que los necesiten.
  
##### Deshabilitar comprobación periódica de actualizaciones de software de Internet Explorer
  
Si habilita esta configuración de directiva, Internet Explorer no podrá determinar si una versión posterior del explorador está disponible ni notificar a los usuarios de su disponibilidad. Si deshabilita o no establece esta directiva, Internet Explorer buscará actualizaciones cada 30 días (el valor predeterminado) y, posteriormente, notificará al usuario si existe una nueva versión. Con esta configuración de directiva se pretende ayudar a los administradores a mantener el control de las versiones de Internet Explorer, ya que no se informa a los usuarios de nuevas versiones disponibles del explorador.
  
Los valores posibles para la configuración **Deshabilitar comprobación periódica de actualizaciones de software de Internet Explorer** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Aunque Microsoft comprueba a fondo todas las revisiones y los Service Packs antes de su publicación, algunas organizaciones prefieren controlar rigurosamente todo el software instalado en sus sistemas administrados. Puede habilitar la configuración **Deshabilitar comprobación periódica de actualizaciones de software de Internet Explorer** para garantizar que los equipos no descarguen ni instalen automáticamente actualizaciones de Internet Explorer.
  
###### Contramedida
  
Configure **Deshabilitar comprobación periódica de actualizaciones de software de Internet Explorer** como **Habilitado**.
  
###### Impacto potencial
  
Internet Explorer no podrá descargar ni instalar de forma automática revisiones y Service Packs. Por lo tanto, los administradores deberán disponer de otro proceso alternativo para distribuir automáticamente las actualizaciones de software a todos los equipos administrados.
  
##### Deshabilitar las notificaciones del shell para actualizaciones de software al iniciar el programa
  
Esta configuración de directiva le permite evitar que se notifique a los usuarios cuando los programas que utilizan el canal de distribución de software de Microsoft instalan componentes nuevos. El canal de distribución de software constituye una forma de actualización dinámica del software en los equipos de los usuarios mediante el uso de tecnologías de distribución abierta de software (OSD).
  
Si habilita esta directiva, no se notificará a los usuarios si sus programas se actualizan mediante canales de distribución de software. Si deshabilita o no configura este parámetro, se notificará a los usuarios antes de que sus programas se actualicen. Esta configuración de directiva se destina a los administradores que desean utilizar canales de distribución de software para actualizar los programas de los usuarios sin la intervención de estos últimos.
  
Los valores posibles para la configuración **Deshabilitar las notificaciones del shell para actualizaciones de software al iniciar el programa** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Puede que las organizaciones que utilizan herramientas y tecnologías OSD prefieran que sus usuarios no sepan cuándo se instalan revisiones y Service Packs en sus equipos, porque los usuarios podrían intentar detener un proceso de instalación antes de que termine.
  
###### Contramedida
  
Configure **Deshabilitar las notificaciones del shell para actualizaciones de software al iniciar el programa** como **Habilitado**.
  
###### Impacto potencial
  
Los usuarios no recibirán notificación alguna cuando las actualizaciones de software se realicen mediante tecnologías OSD.
  
##### Configuración de proxy por equipo y no por usuario
  
Si habilita esta configuración de directiva, los usuarios no podrán alterar la configuración proxy específica del usuario. Deben utilizar las zonas creadas para todos los usuarios de los equipos a los que tienen acceso.
  
Los valores posibles para la configuración **Configuración de proxy por equipo y no por usuario** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Si deshabilita o no establece esta configuración de directiva, los usuarios del mismo equipo podrán establecer su propia configuración de proxy. Con esta configuración de directiva se pretende asegurar que la configuración de proxy está presente de modo uniforme en el mismo equipo y que no varía de usuario a usuario.
  
###### Contramedida
  
Establezca **Configuración de proxy por equipo y no por usuario** como **Habilitado**.
  
###### Impacto potencial
  
Todos los usuarios se verán obligados a utilizar la configuración de proxy definida para el equipo.
  
##### Zonas de seguridad: no permitir que los usuarios agreguen o eliminen sitios
  
Esta configuración de directiva le permite deshabilitar la configuración de administración de sitios para zonas de seguridad. (Para consultar la configuración de la administración del sitio para las zonas de seguridad, seleccione **Herramientas** y, a continuación, **Opciones de Internet** en la barra de menú de Internet Explorer. Haga clic en la ficha **Seguridad** y seleccione **Sitios**. Si deshabilita o no configura este parámetro, los usuarios podrán agregar o eliminar sitios web en las zonas de Sitios de confianza y Sitios restringidos. También serán capaces de alterar la configuración en la zona de intranet local.
  
Los valores posibles para la configuración **Zonas de seguridad: no permitir que los usuarios agreguen o eliminen sitios** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
**Nota**: si habilita el parámetro **Deshabilitar la página Seguridad**, que se localiza en  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet**  
, la ficha **Seguridad** se elimina de la interfaz. Cuando se habilita, esta configuración de directiva tiene prioridad sobre **Zonas de seguridad: no permitir que los usuarios agreguen o eliminen sitios.**
  
###### Vulnerabilidad
  
Si no configura esta configuración de directiva, los usuarios podrán agregar o quitar sitios web en las zonas Sitios de confianza y Sitios restringidos, así como modificar la configuración de la zona de intranet local. Esta configuración podría permitir que se agreguen a estas zonas sitios que alojan código malintencionado móvil, que los usuarios podrían ejecutar.
  
###### Contramedida
  
Configure **Zonas de seguridad: no permitir que los usuarios agreguen o eliminen sitios** como **Habilitado.**
  
###### Impacto potencial
  
Los usuarios podrán cambiar la configuración de la administración de sitios de las zonas de seguridad establecida por el administrador. Si el usuario necesita agregar o eliminar sitios de estas zonas de seguridad de Internet Explorer, un administrador deberá configurarlos previamente.
  
##### Zonas de seguridad: no permitir que los usuarios cambien las directivas
  
Esta configuración de directiva le permite deshabilitar de forma eficaz el botón **Nivel personalizado** y el nivel de seguridad para el control deslizante de zona en la ficha **Seguridad** del cuadro de diálogo **Opciones de Internet**. Si deshabilita o no establece esta configuración de directiva, los usuarios podrán cambiar la configuración de la zona de seguridad. Esta configuración de directiva se puede utilizar para evitar los cambios a la configuración de directiva de zona de seguridad que establece el administrador.
  
Los valores posibles para la configuración **Zonas de seguridad: no permitir que los usuarios cambien las directivas** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
**Nota**: si habilita el parámetro **Deshabilitar la página Seguridad**, que se localiza en  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet**  
, la ficha **Seguridad** se elimina de la interfaz. Cuando se habilita, esta configuración de directiva tiene prioridad sobre **Zonas de seguridad: no permitir que los usuarios cambien las directivas**.
  
###### Vulnerabilidad
  
Los usuarios que cambien su configuración de seguridad de Internet Explorer pueden permitir que se ejecuten tipos peligrosos de código desde Internet y sitios web incluidos en la zona Sitios restringidos del explorador.
  
###### Contramedida
  
Configure **Zonas de seguridad: no permitir que los usuarios cambien las directivas** como **Habilitado.**
  
###### Impacto potencial
  
Los usuarios no podrán establecer la configuración de seguridad para las zonas de Internet Explorer.
  
##### Zonas de seguridad: usar sólo la configuración del equipo
  
Esta configuración de directiva permitirá que los cambios que un usuario realice en una zona de seguridad se puedan aplicar a todos los usuarios del mismo equipo. Si deshabilita o no establece esta configuración de directiva, los usuarios del mismo equipo podrán establecer su propia configuración de zona de seguridad. Con esta configuración de directiva se pretende asegurar que la configuración de la zona de seguridad esté presente de modo uniforme en el mismo equipo y que no varíe de usuario a usuario.
  
Los valores posibles para la configuración **Zonas de seguridad: usar sólo la configuración del equipo** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los usuarios que cambien su configuración de seguridad de Internet Explorer pueden permitir que se ejecuten tipos peligrosos de código desde Internet y sitios web incluidos en la zona Sitios restringidos del explorador.
  
###### Contramedida
  
Configure **Zonas de seguridad: usar sólo la configuración del equipo** como **Habilitado.**
  
###### Impacto potencial
  
Los usuarios no podrán establecer la configuración de seguridad para las zonas de Internet Explorer.
  
##### Desactivar la detección de bloqueos
  
Esta configuración de directiva le permite administrar la característica de detección de bloqueos de administración de complementos en Internet Explorer. Si habilita esta configuración de directiva, un bloqueo en Internet Explorer será similar al de un equipo en el que se ejecute Windows XP Professional Service Pack 1 (SP1) y versiones anteriores: se invocará el Informe de errores de Windows. Si deshabilita esta configuración de directiva, funcionará la característica de detección de bloqueos en la administración de complementos.
  
Los valores posibles para la configuración **Desactivar la detección de bloqueos** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Un informe del bloqueo puede contener información confidencial de la memoria del equipo.
  
###### Contramedida
  
Establezca la configuración de directiva para **Desactivar la detección de bloqueos** como **Habilitado.**
  
###### Impacto potencial
  
La información acerca de los bloqueos causados por complementos de Internet Explorer no se enviará a Microsoft. Si experimenta bloqueos frecuentes y necesita informar de ellos para ayudar a solucionar el problema, el parámetro debe cambiarse temporalmente por **Deshabilitado.**
  
##### No permitir que usuarios habiliten ni deshabiliten complementos
  
Esta configuración de directiva le permite administrar si los usuarios tienen la capacidad de permitir o denegar los complementos a través de Administrar complementos. Si se establece esta configuración de directiva como **Habilitado**, los usuarios no podrán habilitar ni deshabilitar los complementos a través de la característica Administrar complementos. La única excepción se produce si un complemento se ha introducido específicamente en la configuración de directiva **Lista de complementos** de manera que los usuarios puedan seguir administrando el complemento a través de Administrar complementos. Si establece esta configuración de directiva como **Deshabilitada**, el usuario podrá habilitar o deshabilitar complementos.
  
**Nota**: para obtener más información acerca de cómo administrar complementos de Internet Explorer en Windows XP SP2, vea el artículo 883256 de Microsoft Knowledge Base acerca de [cómo administrar complementos de Internet Explorer en Windows XP Service Pack 2](http://support.microsoft.com/?kbid=883256), en http://support.microsoft.com/?kbid=883256.
  
Los valores posibles para la configuración **No permitir que usuarios habiliten ni deshabiliten complementos** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Es habitual que los usuarios decidan instalar complementos no permitidos por una directiva de seguridad de la organización. Dichos complementos pueden suponer un riesgo considerable para la seguridad y la privacidad en la red.
  
###### Contramedida
  
Configure el valor de **No permitir que usuarios habiliten ni deshabiliten complementos** como **Habilitado.**
  
###### Impacto potencial
  
Cuando se habilita la configuración **No permitir que usuarios habiliten ni deshabiliten complementos**, los usuarios no podrán habilitar ni deshabilitar sus propios complementos de Internet Explorer. Si su organización utiliza complementos, esta configuración puede afectar a su capacidad de trabajo.
  
#### Internet Explorer\\Panel de control Internet\\Página Seguridad
  
Puede establecer la configuración de directiva de grupo de la página Seguridad de Internet Explorer en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\**  
**Internet Explorer\\Panel de control Internet\\Página Seguridad**
  
La configuración de directiva individual para la página Seguridad se documenta al completo en los sistemas de ayuda de Windows XP y Windows Server 2003, y también en el sitio web de Microsoft. Por lo tanto, esta información no se repite en esta guía. Deben considerarse las siguientes pautas generales.
  
##### Vulnerabilidad
  
Si permite a los usuarios configurar su propia configuración de seguridad en Internet Explorer, podrán aumentar la vulnerabilidad de sus equipos al software malintencionado. Además, los usuarios serán capaces de evitar cualquier directiva estándar de seguridad de la organización que exista.
  
##### Contramedida
  
Utilice la configuración en el nodo **Internet Explorer\\Panel de control Internet\\página Seguridad** de Directiva de grupo para configurar los valores apropiados para zonas de seguridad y comportamiento relacionado con la zona de seguridad.
  
##### Impacto potencial
  
Windows XP SP2 y Windows Server 2003 SP1 introducen varias configuraciones de directiva nuevas para ayudarle a proteger la configuración de zonas de Internet Explorer en su entorno. Los valores predeterminados para estas configuraciones de directiva proporcionan seguridad mejorada sobre versiones anteriores de Windows. Sin embargo, puede ser necesario personalizar estas configuraciones de directivas para su entorno local. Por ejemplo, puede que quiera agregar a sus socios o proveedores a la zona de Sitios de confianza y no permitir a los usuarios hacer sus propios cambios a las listas de la zona.
  
#### Internet Explorer\\Panel de control Internet\\Página Opciones avanzadas
  
La configuración en esta parte de la Plantilla administrativa equivale a la configuración que está disponible en la ficha **Opciones avanzadas** del cuadro de diálogo **Opciones de Internet** en Internet Explorer.
  
Las siguientes dos configuraciones de directiva están disponibles tanto en Windows Server 2003 con SP1 como en Windows XP con SP2.
  
##### Permitir que el software se ejecute o instale incluso si la firma no es válida
  
Esta configuración de directiva le permite controlar si los usuarios pueden instalar o ejecutar el software descargado, si la firma no es válida. Una firma no válida podría indicar que alguien manipuló el archivo. Si habilita esta configuración de directiva, se preguntará a los usuarios si desean instalar o ejecutar los archivos cuya firma no es válida. Si deshabilita esta configuración de directiva, los usuarios no podrán ejecutar ni instalar archivos cuya firma no sea válida.
  
Los valores posibles para la configuración **Permitir que el software se ejecute o instale incluso si la firma no es válida** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los controles Microsoft ActiveX® y los archivos que se descargan suelen tener adjuntas firmas digitales que garantizan la integridad del archivo y la identidad del firmante (creador) del software. Estas firmas ayudan a asegurar que se descarga software no modificado y que el usuario pueda identificar al firmante para determinar si confía en éste lo suficiente como para ejecutar su software. La validez del código sin firmar no se puede determinar.
  
###### Contramedida
  
Establezca la configuración **Permitir que el software se ejecute o instale incluso si la firma no es válida** como **Deshabilitado** para que los usuarios no puedan ejecutar los componentes de ActiveX sin firmar.
  
###### Impacto potencial
  
Algunos programas y controles legítimos pueden tener una firma no válida. Debe probar con cuidado dicho software en aislamiento, antes de permitir que se use en la red de la organización.
  
##### Permitir que el contenido activo de los CD se ejecute en equipos de usuario
  
Esta configuración de directiva le permite determinar si el contenido activo en CD puede ejecutarse en equipos de usuarios. Las organizaciones sensibles a los aspectos de seguridad podrían desear evitar la ejecución de controles ActiveX u otro contenido activo que se proporcione en un CD.
  
Los valores posibles para la configuración **Permitir que el contenido activo de los CD se ejecute en equipos de usuario** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los usuarios pueden eludir accidentalmente una directiva de seguridad de la organización si ejecuta el contenido que se proporciona en un CD en vez de a través de la red.
  
###### Contramedida
  
Puede configurar el parámetro **Permitir que el contenido activo de los CD se ejecute en equipos de usuario** como **Deshabilitado.** Esta configuración evitará la ejecución del contenido activo que se almacena en los CD.
  
###### Impacto potencial
  
Cuando esta configuración de directiva se habilita, las aplicaciones diseñadas para instalarse desde CD podrían no funcionar apropiadamente sin la intervención del usuario.
  
##### Permitir extensiones de explorador de terceros
  
(Esta configuración de directiva sólo está disponible en Windows Server 2003.)
  
Los usuarios pueden instalar extensiones de explorador de terceros, que se conocen como objetos auxiliares del explorador (BHOs). El parámetro **Permitir extensiones de explorador de terceros** controla si los BHOs instalados se cargarán cuándo se inicie Internet Explorer.
  
Los valores posibles para el parámetro **Permitir extensiones de explorador de terceros** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Las extensiones del explorador de terceros son potencialmente peligrosas porque pueden contener vulnerabilidades o código malintencionado. Además, su instalación puede violar directivas de seguridad de la organización.
  
###### Contramedida
  
Configure **Permitir extensiones de explorador de terceros** como **Deshabilitado**.
  
###### Impacto potencial
  
Al configurar el parámetro **Permitir extensiones de explorador de terceros** como **Deshabilitado**, los usuarios serán capaces de instalar las extensiones de explorador de terceros, pero no se cargarán cuándo se inicie Internet Explorer. Esta configuración puede entorpecer el flujo de trabajo del usuario o generara llamadas adicionales al servicio de asistencia.
  
##### Comprobar la revocación del certificado del servidor
  
(Esta configuración de directiva sólo está disponible en Windows Server 2003.)
  
Cuando una conexión de nivel de sockets seguro (SSL) se establece entre el explorador y un servidor remoto, el servidor presenta un certificado al equipo cliente para utilizar en la negociación de seguridad inicial. Cuando el parámetro **Comprobar la revocación del certificado del servidor** se habilita, Internet Explorer determinará si el certificado presentado está en la lista de revocación de certificados de la autoridad emisora.
  
Los valores posibles para el parámetro **Comprobar la revocación del certificado del servidor** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los usuarios podrían comunicarse accidentalmente con un servidor cuya certificación haya caducado o haya sido revocada por la autoridad emisora. Tal situación podría llevar a la divulgación de información y hasta a ataques activos si el servidor remoto ha quedado comprometido.
  
###### Contramedida
  
Configure el parámetro **Comprobar la revocación del certificado del servidor** como **Habilitado.**
  
###### Impacto potencial
  
Cuando el parámetro **Comprobar la revocación del certificado del servidor** se habilita, los usuarios pueden recibir advertencias sobre sitios que antes se consideraban de confianza; es necesario educarlos para ayudarles a tomar decisiones de confianza cuando navegan por Internet.
  
##### Buscar firmas en programas descargados
  
(Esta configuración de directiva sólo está disponible en Windows Server 2003.)
  
Los programas descargados se pueden firmar con la tecnología Microsoft Authenticode®, que enlaza una firma digital a objetos ejecutables tales como los programas y los controles ActiveX. Cuando el parámetro **Buscar firmas en programas descargados** se habilita, Internet Explorer comprobará la firma digital de programas ejecutables y mostrará sus identidades antes de descargarlos.
  
Los valores posibles para la **Buscar firmas en programas descargados** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los usuarios podrían descargar contenido inadecuado o malintencionado sin darse cuenta.
  
###### Contramedida
  
Configure el parámetro **Buscar firmas en programas descargados** como **Habilitado.**
  
###### Impacto potencial
  
Cuando el parámetro **Buscar firmas en programas descargados** está habilitado, los usuarios consultarán información de identidad para los programas ejecutables que se han firmado.
  
##### No guardar páginas cifradas en disco
  
(Esta configuración de directiva sólo está disponible en Windows Server 2003.)
  
Cuando Internet Explorer recupera páginas de un servidor remoto, almacena las páginas en su archivo caché temporal. Esta función mejora el rendimiento y proporciona la capacidad de avanzar o retroceder en la lista del historial de exploración, sin reconexión al anfitrión.
  
Los valores posibles para el parámetro **No guardar páginas cifradas en disco** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Las páginas en caché de conexiones de SSL-seguras podrían contener información confidencial, como contraseñas o números de tarjetas de crédito.
  
###### Contramedida
  
Configure el parámetro **No guardar páginas cifradas en disco** como **Habilitado.**
  
###### Impacto potencial
  
Las páginas que se recuperan en conexiones SSL no se guardarán en caché. Esta configuración puede aumentar el uso del ancho de banda de red conforme los navegadores de los usuarios vuelven a descargar páginas que se habrían guardado en caché si esta configuración de directiva no estuviera vigente.
  
##### Vaciar la carpeta de archivos temporales de Internet cuando se cierre el explorador
  
(Esta configuración de directiva sólo está disponible en Windows Server 2003.)
  
Las páginas que Internet Explorer recupera se almacenan en su archivo caché temporal. Internet Explorer administra esta caché según los parámetros del cuadro de diálogo **Configuración temporal de archivos de Internet**. Cuando un archivo u objeto se descarga, se queda en la caché hasta que Internet Explorer lo elimine.
  
Los valores posibles para el parámetro **Vaciar la carpeta de archivos temporales de Internet cuando se cierre el explorador** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
La información confidencial puede quedarse en la carpeta **\\Archivos temporales de Internet** después que un usuario sale de Internet Explorer. Otro usuario en el mismo equipo podría lograr el acceso a estos archivos.
  
###### Contramedida
  
Configure el parámetro **Vaciar la carpeta de archivos temporales de Internet cuando se cierre el explorador** como **Habilitado.**
  
###### Impacto potencial
  
Internet Explorer utiliza la carpeta **\\Archivos temporales de Internet** como una caché para mejorar el rendimiento del explorador. Si deshabilita esta característica, puede aumentar el tiempo y el ancho de banda que los usuarios necesitan para explorar la Web.
  
#### Internet Explorer\\Características de Seguridad
  
La parte de **Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Características de seguridad** de las Plantillas administrativas de Windows incluye varias configuraciones de directiva que controlan varias características de seguridad que se agregaron a Internet Explorer 6,0 en Windows Server 2003 SP1 y Windows XP SP2. Cada una de estas configuraciones de directiva contiene tres parámetros subordinados:
  
-   **Procesos de Internet Explorer.** Este parámetro tiene tres valores posibles: **Habilitado**, **Deshabilitado**, y **No configurado.** Si está **Habilitado**, el comportamiento especificado se desactiva para los procesos de Internet Explorer y Explorador de Windows. Si configura el parámetro como **Deshabilitado** o **No configurado**, se seguirá aplicando el comportamiento predeterminado (descrito por separado para cada parámetro).
  
-   **Lista de procesos.** Este parámetro le permite especificar los procesos individuales para los que la característica de seguridad se habilitará o se deshabilitará. La lista de procesos controla qué procesos aplica la característica de control; un valor de 1 en el parámetro deshabilita la característica para esos procesos y un valor de 0 habilita la característica para esos procesos.
  
-   **Todos los procesos.** Este parámetro tiene tres valores posibles: **Habilitado**, **Deshabilitado**, y **No configurado.** Si está **Habilitado**, el comportamiento especificado se desactiva para los procesos de Internet Explorer y Explorador de Windows. Si configura el parámetro como **Deshabilitado** o **No configurado**, se seguirá aplicando el comportamiento predeterminado (descrito por separado para cada parámetro).
  
##### Restricción de seguridad de comportamiento binario
  
Internet Explorer contiene comportamientos binarios dinámicos, que son los componentes que encapsulan la funcionalidad específica de los elementos HTML a los que se adjuntaron. Estos comportamientos binarios no son controlados por cualquier parámetro de seguridad de Internet Explorer, lo que significa que funcionan en páginas web en la zona de sitios restringidos.
  
En Windows XP SP2 y Windows Server 2003 SP1, hay un parámetro de seguridad de Internet Explorer nuevo, para comportamientos binarios. Este nuevo parámetro de seguridad deshabilita los comportamientos binarios en la zona de sitios restringidos de forma predeterminada, y proporciona una mitigación general a vulnerabilidades en los comportamientos binarios de Internet Explorer.
  
Además de los parámetros de **Procesos de Internet Explorer**, la **Lista del proceso** y **Todos los procesos** que se describieron antes, el parámetro de **Restricción de seguridad del comportamiento binario** le da la posibilidad de permitir los comportamientos individuales con los parámetros **de comportamiento aprobados por el administrador**. Para controlar estos comportamientos de código binario y secuencia de comandos, ahora puede establecer las zonas apropiadas en **Aprobado por el administrador** y entonces utilizar este parámetro para especificar los comportamientos individuales que se pueden ejecutar en cada zona.
  
###### Vulnerabilidad
  
Las páginas web pueden invocar comportamientos mal escritos o malintencionados y provocar inestabilidad o posibles riesgos.
  
###### Contramedida
  
Deshabilitar por completo el uso de comportamientos binarios. También es posible especificar un conjunto de comportamientos permitidos con el parámetro **Comportamientos aprobados por el administrador**.
  
###### Impacto potencial
  
Las aplicaciones que dependen de comportamientos binarios podrían no funcionar apropiadamente si deshabilita los comportamientos de los que dependen.
  
##### Restricción de seguridad del protocolo MK
  
Esta configuración de directiva bloquea el protocolo MK, que rara vez se utiliza para reducir el área de superficie de ataque de un equipo. Algunas aplicaciones web más antiguas utilizan el protocolo MK para recuperar información de archivos comprimidos.
  
###### Vulnerabilidad
  
Pueden existir vulnerabilidades en el controlador del protocolo MK o en las aplicaciones que lo llaman.
  
###### Contramedida
  
Dado que el protocolo de MK no se utiliza de forma generalizada, debe bloquearse siempre que no se necesite. Deshabilitar el acceso al protocolo MK para todo el proceso.
  
###### Impacto potencial
  
Dado que se producirá un error en los recursos que utilizan el protocolo MK cuando implemente esta configuración, debe asegurarse de que ninguna de sus aplicaciones utiliza el protocolo MK.
  
##### Seguridad de bloqueo de zona Máquina local
  
Cuando Internet Explorer abre una página web, coloca restricciones en lo que la página puede hacer, basándose en la zona de seguridad de Internet Explorer a que la página pertenezca. Hay varias posibles zonas de seguridad y cada una tiene diferentes conjuntos de restricciones. La zona de seguridad de una página está determinada por su ubicación. Por ejemplo, las páginas ubicadas en Internet estarán por lo general en la zona de seguridad más restrictiva. Quizá no se les permita realizar algunas operaciones, como tener acceso al disco duro local. Las páginas que se localizan en la red de la organización estarían normalmente en la zona de seguridad de la Intranet y tendrían menos restricciones. Las restricciones precisas que se asocian con la mayor parte de estas zonas pueden configurarse por el usuario a través de **Opciones de Internet** en el menú **Herramientas** de Internet Explorer.
  
Antes de Windows XP SP2 y Windows Server 2003 SP1, el contenido en el sistema de archivos local se trató como segura y se asignó a la zona de seguridad de la Máquina local (excepto por el contenido que guarda Internet Explorer). Esta zona de seguridad por lo general permitía al contenido ejecutarse en Internet Explorer con relativamente pocas restricciones. Con la publicación de estos Service Packs, la configuración predeterminada de Internet Explorer proporciona ahora protección adicional para el usuario porque bloquea la zona Máquina local.
  
###### Vulnerabilidad
  
Los atacantes a menudo tratan de aprovecharse de la zona Máquina local para elevar sus privilegios y poner en peligro al equipo. Muchos de los puntos débiles que se relacionan con la zona Máquina local se mitigaron con otros cambios en Internet Explorer en Windows XP SP2, y estos cambios se incorporaron en Internet Explorer en Windows Server 2003 SP1. Sin embargo, los atacantes todavía pueden encontrar maneras de aprovechar la zona Máquina local.
  
###### Contramedida
  
Configure el parámetro **Seguridad de bloqueo de zona Máquina local** como **Habilitado.**
  
###### Impacto potencial
  
Las aplicaciones basadas en Internet Explorer que utilizan un HTML local no pueden funcionar apropiadamente si configura el parámetro **Seguridad de bloqueo de zona Máquina local** como **Habilitado.** El HTML local que se aloja en otras aplicaciones se ejecutará bajo parámetros menos restrictivos de la zona Máquina local que se utilizan en la versión anterior de Internet Explorer, a menos que esa aplicación utilice el cierre de zona Máquina local.
  
##### Administración de MIME consistente
  
Internet Explorer utiliza información de Extensiones seguras multipropósito al correo de Internet (MIME) para determinar cómo manejar los archivos que se descargan de un servidor web. El parámetro **Administración de MIME consistente** determina si Internet Explorer necesita que toda la información de tipo de archivo que se proporciona a través de los servidores web sea coherente. Por ejemplo, si el tipo MIME de un archivo es texto/sin formato pero los datos MIME indican que el archivo es realmente un archivo ejecutable, Internet Explorer cambia su extensión para reflejar el estado ejecutable. Esta capacidad ayuda a asegurar que ese código ejecutable no se haga pasar por otros tipos de datos en los que se puede confiar.
  
Si habilita esta configuración de directiva, Internet Explorer examina todos los archivos recibidos y exige que tengan datos MIME coherentes. Si deshabilita o no establece esta configuración de directiva, Internet Explorer no requerirá que los datos MIME sean coherentes en todos los archivos recibidos y utilizará los datos MIME proporcionados por el archivo.
  
**Nota:** esta configuración funciona conjuntamente con los parámetros de las **Características de seguridad de examen de MIME**, pero no los reemplaza.
  
###### Vulnerabilidad
  
Un servidor web malintencionado podría proporcionar el contenido ejecutable utilizando un tipo MIME no ejecutable, y un usuario que abriera el contenido podría ser engañado y hacer que el contenido se ejecute.
  
###### Contramedida
  
Configure el parámetro **Administración de MIME consistente** como **Habilitado.**
  
###### Impacto potencial
  
Las aplicaciones que dependen del servidor para establecer correctamente el tipo MIME de objetos descargados pueden fallar cuando este parámetro se habilita, si el servidor proporciona información inexacta de tipo MIME.
  
##### Características de seguridad de examen de MIME
  
El examen de MIME es el proceso que examina el contenido de un archivo MIME para determinar su contexto: si es un archivo de datos, un archivo ejecutable o algún otro tipo del archivo. Esta configuración de directiva determina si el examen de MIME de Internet Explorer evitará la conversión de un archivo de un tipo determinado a otro tipo más peligroso. Cuando esta directiva está habilitada, la función de examen de MIME no convertirá nunca un archivo de un tipo a otro tipo de archivo más peligroso. Si configura este parámetro de directiva como **Deshabilitado**, los procesos de Internet Explorer permitirán un examen de MIME que convierta un archivo de un tipo a un tipo de archivo más peligroso. Por ejemplo, es peligroso convertir un archivo de texto en un archivo ejecutable, porque cualquier código en el supuesto archivo de texto se ejecutaría.
  
###### Vulnerabilidad
  
Un sitio web malintencionado puede proporcionar el contenido de un tipo con una etiqueta MIME que indica que es seguro.
  
###### Contramedida
  
Configure el parámetro **Características de seguridad de examen de MIME que** para **Todos los procesos** como **Habilitado.**
  
###### Impacto potencial
  
Las aplicaciones que dependen de tipos MIME mal etiquetados para funcionar correctamente se romperán cuando se habilite esta configuración de directiva.
  
##### Protección de caché de objetos
  
En versiones anteriores de Internet Explorer, una página web podría mencionar un objeto que se guarda en la caché de otro sitio web. El parámetro **Protección de caché de objetos** le permite evitar dichas referencias a objetos en caché.
  
###### Vulnerabilidad
  
Un servidor malintencionado podría descargar un objeto a un equipo del usuario y activarlo a través de un código en otro sitio, quizás en una zona diferente de Internet Explorer. Por ejemplo, un atacante podría utilizar este método para crear secuencias de comandos que escuchan eventos o contenido en otro marco, tal como los números de tarjeta de crédito u otros datos confidenciales que se escriben en el otro marco.
  
###### Contramedida
  
Configure el parámetro **Protección de caché de objetos** para **Procesos de Internet Explorer** como **Habilitado.**
  
###### Impacto potencial
  
Las aplicaciones escritas apropiadamente no deben depender del acceso a objetos entre dominios. Las aplicaciones que lo hacen no funcionarán cuando esta configuración de directiva esté habilitada.
  
##### Restricciones de seguridad de ventanas con secuencias de comandos
  
Internet Explorer permite que mediante secuencias de comandos se abran distintos tipos de ventanas, así como que se cambie su tamaño y posición. El parámetro **Restricciones de seguridad de ventanas con secuencias de comandos** restringe las ventanas emergentes y prohíbe el desplegado de ventanas en las que el título y las barras de estado no son visibles para el usuario o que esconden otros títulos de ventanas y barras de estado. Si usted habilita esta configuración de directiva, Windows aplicará estas restricciones para el Explorador de Windows y procesos de Internet Explorer. Si deshabilita o no establece esta configuración de directiva, las secuencias de comandos pueden seguir creando ventanas emergentes y ventanas que oculten a otras.
  
Tenga en cuenta que hay muchas herramientas de terceros que intentan controlar ventanas emergentes de Internet Explorer. Muchas de esas herramientas restringen ventanas emergentes en una manera semejante a este parámetro. Los bloqueadores de elementos emergentes de terceros por lo general no interfieren con este parámetro y este parámetro no tiene efecto en esos bloqueadores.
  
###### Vulnerabilidad
  
Hay sitios web de mala reputación que cambian el tamaño de las ventanas para ocultar otras o que obligan al visitante a interactuar con una ventana que contiene código malintencionado.
  
###### Contramedida
  
Configure el parámetro **Restricciones** **de seguridad** **de ventanascon secuencias de comandos** para **Procesos de** **Internet** **Explorer** como **Habilitado.**
  
###### Impacto potencial
  
Las aplicaciones web que necesitan cambiar el tamaño o posición de las ventanas podrían no funcionar correctamente cuando este parámetro esté habilitado.
  
##### Protección contra elevación de zona
  
Internet Explorer establece restricciones para cada página web que abre, las cuales dependen de la ubicación de ésta (zona Internet, zona de intranet o zona Máquina local). Las páginas web de un equipo local tienen restricciones de seguridad mínimas y residen en la zona Máquina local, lo que convierte a la zona de seguridad Máquina local en un objetivo prioritario para los atacantes malintencionados.
  
Si habilita el parámetro **Procesos de Internet Explorer – Protección contra elevación de zona**, cualquier zona puede protegerse de la elevación de zona por procesos de Internet Explorer. Con este método se impide que se apliquen los privilegios elevados de una zona al contenido de otra zona.
  
###### Vulnerabilidad
  
Las páginas web malintencionadas pueden intentar elevarse a sí mismas de su zona actual a otra zona con privilegios más altos.
  
###### Contramedida
  
Configure el parámetro **Protección contra elevación de zona** para **Procesos de Internet Explorer** como **Habilitado.**
  
###### Impacto potencial
  
Ninguno.
  
##### Limitar la instalación de ActiveX
  
Este parámetro le permite bloquear avisos de instalación de control ActiveX para procesos de Internet Explorer. Si habilita esta configuración de directiva, no se avisará a los usuarios cuando una página incluya un control ActiveX que se tenga que instalar manualmente; no podrán instalar el control de la página web. Si deshabilita esta configuración de directiva, no se bloquearán los mensajes de instalación de controles ActiveX.
  
###### Vulnerabilidad
  
A menudo, los usuarios deciden instalar software (como, por ejemplo, controles de ActiveX) que la directiva de seguridad de la compañía no permite. Ese tipo de software puede entrañar riesgos considerables para la seguridad y la privacidad en la red.
  
###### Contramedida
  
Configure el parámetro **Limitar la instalación de ActiveX** para **Procesos de Internet Explorer** en **Habilitado.**
  
###### Impacto potencial
  
Si habilita esta configuración de directiva, los usuarios no podrán instalar controles ActiveX legítimos autorizados, como los que usa Windows Update. Si habilita esta configuración de directiva, asegúrese de implementar alguna forma alternativa de distribuir las actualizaciones de seguridad, como Windows Server Update Services (WSUS). Para obtener más información acerca de WSUS, consulte la página [Windows Server Update Services Product Overview](http://www.microsoft.com/windowsserversystem/updateservices/evaluation/overview.mspx) en www.microsoft.com/windowsserversystem/updateservices/evaluation/overview.mspx.
  
##### Limitar la descarga de archivos
  
Cuando el parámetro **Limitar la descarga de archivos** está habilitado, los procesos de Internet Explorer bloquean las solicitudes de descarga de archivos que no inicia el usuario.
  
###### Vulnerabilidad
  
En determinadas circunstancias los sitios web pueden iniciar diálogos de descarga de archivos sin la interacción de los usuarios. Esta técnica puede permitir que un sitio web coloque archivos no autorizados en el equipo de un usuario si éste hace clic en el botón equivocado y acepta la descarga.
  
###### Contramedida
  
Configure el parámetro **Limitar la descarga de archivos** para **Procesos de Internet Explorer** en **Habilitado.**
  
###### Impacto potencial
  
Ninguno. No hay razón legítima para que un sitio web inicie la transferencia de un archivo a la estación de trabajo de un usuario sin una solicitud del usuario.
  
##### Administración de complementos
  
Esta configuración de directiva, junto con la configuración **Lista de complementos**, le permite administrar los complementos en Internet Explorer. De forma predeterminada, la configuración **Lista de complementos** define una lista de complementos que se deben permitir o denegar a través de Directiva de grupo. La configuración **Denegar complementos a menos que se permitan específicamente en la Lista de complementos** supone que todos los complementos se deniegan a menos que aparezcan enumerados específicamente en la configuración **Lista de complementos.**
  
Si habilita esta configuración de directiva, Internet Explorer sólo permite complementos que se enumeran (y permiten) específicamente a través de la configuración de directiva **Lista de complementos.** Si deshabilita esta configuración, los usuarios pueden utilizar el Administrador de complementos para permitir o denegar cualquier complemento.
  
Considere la posibilidad de utilizar tanto la configuración **Denegar complementos a menos que se permitan específicamente en la Lista de complementos** como la configuración **Lista de complementos** para controlar los complementos que se pueden utilizar en su entorno. Este método ayudará a garantizar que sólo se utilicen complementos autorizados.
  
###### Vulnerabilidad
  
Los complementos mal escritos o malintencionados pueden desestabilizar o poner en peligro los equipos de los usuarios.
  
###### Contramedida
  
Configure la **Lista de complementos** con la lista de complementos de confianza de Internet Explorer a los que los usuarios deben tener acceso. A continuación, configure **Denegar complementos a menos que se permitan específicamente en la Lista de complementos** en **Habilitado**.
  
###### Impacto potencial
  
Si configura el **Denegar complementos a menos que se permitan específicamente en la Lista de complementos** como **Habilitado**, los usuarios no podrán instalar ni configurar sus propios complementos.
  
##### Bloqueo de protocolo de red
  
Windows Server 2003 SP1 y Windows XP SP2 agregan la capacidad de que los administradores eviten la ejecución del contenido activo que se descarga a través de protocolos de red específicos. Los administradores pueden especificar protocolos individuales (incluidos HTTP y HTTPS) en la configuración **Bloqueo de protocolo de red** para controlar qué protocolos se pueden utilizar para obtener el contenido activo.
  
###### Vulnerabilidad
  
Los usuarios pueden descargar y ejecutar contenido malintencionado de fuentes que no son de confianza.
  
###### Contramedida
  
Utilice el parámetro **Protocolos restringidos por zona de seguridad** para definir qué protocolos se pueden utilizar para descargar contenido en cada zona. A continuación, configure el parámetro **Bloqueo de protocolo de red** para **Procesos de Internet Explorer** en **Habilitado.**
  
###### Impacto potencial
  
Es posible que los usuarios no puedan ejecutar aplicaciones ni usar páginas que incluyen contenido activo si se establecen los controles por zona. Debe probar de forma exhaustiva las aplicaciones en cada zona para asegurarse de que funcionen apropiadamente cuando se utiliza el bloqueo de protocolo.
  
#### Servicios de Internet Information Server
  
La versión 6.0 de los Servicios de Internet Information Server (IIS) de Microsoft, el servidor web integrado en Windows Server 2003, facilita el uso compartido de documentos e información a través de Internet y de una intranet corporativa. Puede configurar IIS en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\**  
**Servicios de Internet Information Server**
  
##### Impedir la instalación de IIS
  
IIS 6.0 no se instala de forma predeterminada en Windows Server 2003. Puede habilitar el parámetro **Impedir la instalación de IIS** para evitar la instalación de IIS en equipos de su entorno.
  
Los valores posibles para la configuración **Impedir la instalación de IIS** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Las aplicaciones y versiones anteriores de IIS que utilizaban esta característica para el acceso de red experimentaron graves vulnerabilidades de seguridad que se pudieron aprovechar de forma remota. Aunque IIS 6.0 resulta mucho más seguro que sus predecesores, es posible que existan nuevas vulnerabilidades aún por descubrir y divulgar. Por lo tanto, puede que las organizaciones deseen asegurarse de que IIS no se pueda instalar en equipos que no sean los especificados como servidores web.
  
###### Contramedida
  
Establezca **Impedir la instalación de IIS** en **Habilitado**.
  
###### Impacto potencial
  
No se podrán instalar aplicaciones ni componentes de Windows que requieran IIS. Puede que los usuarios que los instalen no vean ningún mensaje de error ni advertencia de que IIS no se puede instalar debido a esta configuración de Directiva de grupo. Esta configuración de directiva no tendrá efecto si se habilita en un equipo en el que ya esté instalado IIS.
  
#### Servicios de Terminal Server
  
El componente Servicios de Terminal Server de Windows Server 2003 se ha desarrollado sobre la sólida base que constituía el modo de servidor de aplicaciones en los Servicios de Terminal Server de Windows 2000, y ahora incorpora a Windows XP las nuevas capacidades de protocolo y cliente. Los Servicios de Terminal Server permiten distribuir aplicaciones basadas en Windows, o el propio escritorio de Windows, en prácticamente cualquier dispositivo, incluyendo los que no pueden ejecutar Windows.
  
Los Servicios de Terminal Server en Windows Server 2003 pueden mejorar las capacidades de implementación de software de una organización en diversos escenarios, lo que permite una flexibilidad considerable en la infraestructura de administración y aplicaciones. Cuando un usuario ejecuta una aplicación en Terminal Server, la ejecución tiene lugar en el servidor y únicamente la información de pantalla, mouse y teclado se transmite a través de la red. Cada usuario ve únicamente su sesión individual, administrada con claridad por el sistema operativo del servidor, que es independiente de cualquier otra sesión del cliente.
  
Puede establecer la configuración de directiva de grupo de Terminal Server en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\**  
**Servicios de Terminal Server**
  
##### Denegar el cierre de sesión a un administrador con una sesión iniciada en la consola
  
Esta configuración de directiva especifica si un administrador que intenta conectarse a la consola de un servidor puede cerrar la sesión de un administrador con una sesión iniciada actualmente en la consola. La sesión de la consola también se denomina sesión 0. El acceso a ella se puede obtener utilizando el conmutador /console desde Conexión a Escritorio remoto en el campo de nombre de equipo o desde la línea de comandos.
  
Los valores posibles para la configuración **Denegar el cierre de sesión a un administrador con una sesión iniciada en la consola** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
Si habilita **Denegar el cierre de sesión a un administrador con una sesión iniciada en la consola**, nadie será capaz de cerrar la sesión de un administrador conectado al equipo. Si deshabilita esta configuración de directiva, un administrador podrá cerrar la sesión de otro administrador. Si no establece esta configuración de directiva, un administrador puede cerrar la sesión de otro administrador, pero este permiso se puede revocar en el nivel de Directiva de equipo local.
  
Esta directiva resulta útil cuando el administrador que está conectado no desea que otro administrador cierre su sesión. Si se cierra la sesión de un administrador conectado, perderá toda la información que no haya guardado.
  
###### Vulnerabilidad
  
Un atacante que haya podido establecer una sesión de Terminal Server y haya adquirido privilegios administrativos, puede hacer que la recuperación del control del equipo resulte aún más difícil al forzar el cierre de sesión de un administrador que intente iniciar la sesión en el servidor en la consola de sesión 0. El valor de esta contramedida se ve limitado, ya que un atacante con suficientes privilegios para cerrar la sesión de otros usuarios prácticamente ya tiene el control total del equipo.
  
###### Contramedida
  
Establezca **Denegar el cierre de sesión a un administrador con una sesión iniciada en la consola** como **Habilitado**.
  
###### Impacto potencial
  
Un administrador no podrá forzar el cierre de la sesión de otros administradores en la consola de sesión 0.
  
##### No permitir a los administradores locales personalizar permisos
  
Esta configuración de directiva le permite controlar los derechos de los administradores para personalizar los permisos de seguridad en la herramienta Configuración de Servicios de Terminal Server (TSCC). Si habilita esta configuración de directiva, los administradores no serán capaces de hacer cambios a los descriptores de seguridad para grupos de usuarios en la ficha **Permisos** de TSCC. En la configuración predeterminada, los administradores pueden hacer dichos cambios.
  
Si habilita el parámetro **No permitir a los administradores locales personalizar permisos**, la ficha **Permisos** de TSCC no se puede utilizar para personalizar los descriptores de seguridad por conexión ni para cambiar los descriptores de seguridad predeterminados de un grupo existente. Todos los descriptores de seguridad pasan a ser de sólo lectura. Si deshabilita o no establece esta configuración de directiva, los administradores del servidor tendrán todos los privilegios de lectura y escritura para los descriptores de seguridad del usuario en la ficha **Permisos** de TSCC.
  
Los valores posibles para la configuración **No permitir a los administradores locales personalizar permisos** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
**Nota**: la mejor forma de administrar el acceso de los usuarios es agregar usuarios al grupo Usuarios de escritorio remoto.
  
###### Vulnerabilidad
  
Un atacante que adquiere permisos administrativos en un servidor que ejecuta Servicios de Terminal Server puede modificar los permisos con la herramienta TSCC para evitar que otros usuarios se conecten al servidor, creando una condición de denegación de servicio (DoS).
  
El valor de esta contramedida se ve limitado, ya que un atacante con privilegios administrativos prácticamente ya se ha hecho con el control total del equipo.
  
###### Contramedida
  
Establezca **No permitir a los administradores locales personalizar permisos** en **Habilitado**.
  
###### Impacto potencial
  
La ficha **Permisos** de TSCC no se puede utilizar para personalizar los descriptores de seguridad por conexión ni para cambiar los descriptores de seguridad predeterminados de un grupo existente.
  
##### Establece reglas para el control remoto de sesiones de usuario de Servicios de Terminal Server
  
Esta configuración de directiva especifica el nivel de control remoto que se permite en una sesión de Terminal Server. El control remoto se puede establecer con o sin el permiso del usuario de la sesión. Esta configuración se puede emplear para seleccionar uno o dos niveles de control remoto: **Ver sesión** permite al usuario del control remoto ver una sesión; **Control total**, por su parte, permite al usuario interactuar con la sesión.
  
Si habilita **Establece reglas para el control remoto de sesiones de usuario de Servicios de Terminal Server**, los administradores pueden interactuar de forma remota con una sesión de Terminal Server de un usuario de acuerdo con las reglas especificadas. Para definir estas reglas, seleccione el nivel deseado de control y permiso en la lista Opciones. Para deshabilitar el control remoto, seleccione **Control remoto no permitido**. Si deshabilita o no establece esta configuración, el administrador del servidor puede determinar las reglas de control remoto con la herramienta TSCC. De forma predeterminada, los usuarios de control remoto pueden disponer de control total con el permiso del usuario de la sesión.
  
Los valores posibles para la configuración **Establece reglas para el control remoto de sesiones de usuario de Servicios de Terminal Server** son:
  
-   Habilitado, en el que se incluyen las siguientes opciones:
  
    -   Control remoto no permitido
  
    -   Control total con permisos del usuario
  
    -   Control total sin permisos del usuario
  
    -   Ver sesión con permisos del usuario
  
    -   Ver sesión sin permisos del usuario
  
-   Deshabilitado
  
-   No configurado
  
**Nota**: este parámetro existe en los nodos Configuración del equipo y Configuración de usuario. Cuando está configurado en ambos lugares, el parámetro Configuración del equipo tiene prioridad sobre el mismo parámetro en Configuración de usuario.
  
###### Vulnerabilidad
  
Un atacante con privilegios administrativos en el servidor podría utilizar la característica de control remoto de los Servicios de Terminal Server para observar las acciones de otros usuarios. Esto podría ocasionar la revelación de información confidencial. El valor de esta contramedida se ve limitado, ya que un atacante con privilegios administrativos prácticamente ya tiene el control total del equipo.
  
###### Contramedida
  
Defina **Establece reglas para el control remoto de sesiones de usuario de Servicios de Terminal Server** como **Habilitado** y seleccione la opción **Control remoto no permitido**.
  
###### Impacto potencial
  
Los administradores no podrán utilizar el control remoto para ayudar a otros usuarios de los Servicios de Terminal Server.
  
#### Redirección de datos cliente/servidor
  
Los Servicios de Terminal Server permiten que se redirijan los datos y los recursos del cliente y el servidor. Por ejemplo, los datos que se imprimen de una aplicación de servidor pueden redirigirse al cliente, o el portapapeles del cliente se puede utilizar en aplicaciones de servidor. La configuración en la sección "Redirección de datos cliente/servidor" de Directiva de grupo le permite personalizar los tipos de redirección que se permiten.
  
La configuración Redirección de datos cliente-servidor de los Servicios de Terminal Server se puede establecer en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\**  
**Servicios de Terminal Server\\Redirección de datos cliente/servidor\\**
  
##### Permitir redirección de zona horaria
  
Esta configuración de directiva especifica si se permite al equipo cliente redirigir su configuración de zona horaria a la sesión de Terminal Server. De forma predeterminada, la zona horaria de la sesión es la misma que la del servidor, y el equipo cliente no puede redireccionar su información de zona.
  
Si habilita el parámetro **Permitir redirección de zona horaria**, los clientes que pueden redirigir la zona horaria pueden enviar su información de zona al servidor. La hora de base del servidor se utiliza a continuación para calcular la hora de la sesión actual. Es decir, la hora de base del servidor más la zona horaria del cliente. Actualmente, Conexión a Escritorio remoto y Windows CE 5.1 son los únicos clientes que pueden redirigir su zona horaria. La sesión 0, la de la consola, siempre tiene la zona horaria y la configuración del servidor. Para cambiar la hora y la zona horaria del equipo, conéctese a la sesión 0.
  
Si deshabilita el parámetro **Permitir redirección de zona horaria**, no podrá realizarse la redirección de zona horaria. Si no establece esta configuración de directiva, la redirección de la zona horaria no se especificará en el nivel de Directiva de grupo y el comportamiento predeterminado será desactivar la redirección de la zona horaria. Cuando un administrador cambia esta configuración de directiva, únicamente las nuevas conexiones muestran el comportamiento especificado por la nueva configuración. Las sesiones que se iniciaron antes del cambio se tendrán que cerrar y volver a conectar para que se les aplique la nueva configuración. Microsoft recomienda que todos los usuarios cierren su sesión en el servidor después de que se cambie esta configuración de directiva.
  
Los valores posibles para la configuración **Permitir redirección de zona horaria** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
**Nota**: la redirección de la zona horaria sólo es posible para conexiones a un servidor Terminal Server de la familia de servidores Windows Server.
  
###### Vulnerabilidad
  
Los datos de zona horaria se pueden reenviar desde la sesión de Terminal Server del usuario a su equipo local sin ninguna interacción directa del mismo.
  
###### Contramedida
  
Establezca **Permitir redirección de zona horaria** en **Deshabilitado**.
  
###### Impacto potencial
  
No se podrá realizar la redirección de zona horaria.
  
##### No permitir redirección del portapapeles
  
Esta configuración específica controla si puede compartirse el contenido del portapapeles (redirección del portapapeles) entre un equipo remoto y un equipo cliente en una sesión de Servicios de Terminal Server. Puede emplearla para evitar que se redirija información del portapapeles entre el equipo remoto y el local. De forma predeterminada, los Servicios de Terminal Server permiten la redirección.
  
Si habilita el parámetro **No permitir redirección del portapapeles**, los usuarios no pueden redirigir los datos del portapapeles. Si deshabilita esta configuración de directiva, los Servicios de Terminal Server siempre permitirán la redirección del portapapeles. Si no establece esta configuración de directiva, la redirección del portapapeles no se especificará en el nivel de Directiva de grupo. Sin embargo, un administrador podrá seguir deshabilitando la redirección del portapapeles con la herramienta TSCC.
  
Los valores posibles para la configuración **No permitir redirección del portapapeles** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los datos se pueden reenviar desde una sesión de Terminal Server del usuario a su equipo local sin ninguna interacción directa del mismo.
  
###### Contramedida
  
Establezca **No permitir redirección del portapapeles** como**Habilitado**.
  
###### Impacto potencial
  
No se podrá realizar la redirección del portapapeles.
  
##### Permitir redirección de audio
  
Esta configuración de directiva especifica si los usuarios pueden escoger dónde reproducir la salida de audio del equipo remoto durante una sesión de Terminal Server. Los usuarios pueden hacer clic en la opción **Sonido de equipo remoto** en la ficha **Recursos locales** de Conexión a Escritorio remoto para seleccionar si reproducen el sonido en el equipo remoto o en el local. También se puede deshabilitar el audio. De forma predeterminada, no se puede aplicar la redirección de audio cuando la conexión se realiza mediante los Servicios de Terminal Server a un servidor que ejecuta Windows Server 2003. Los usuarios que se conectan a un equipo con Windows XP Professional pueden aplicar la redirección de audio de forma predeterminada.
  
Si habilita el parámetro **Permitir redirección de audio**, los usuarios pueden aplicar la redirección de audio. Si deshabilita esta configuración de directiva, los usuarios no pueden aplicar la redirección de audio. Si no establece esta configuración de directiva, la redirección de audio no se especificará en el nivel de Directiva de grupo. Sin embargo, un administrador aún podrá habilitar o deshabilitar la redirección de audio con la herramienta TSCC.
  
Los valores posibles para la configuración **Permitir redirección de audio** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los datos se pueden reenviar desde la sesión de Terminal Server del usuario a su equipo local sin ninguna interacción directa del mismo.
  
###### Contramedida
  
Establezca **Permitir redirección de audio** en **Deshabilitado**.
  
###### Impacto potencial
  
No se podrá realizar la redirección de audio.
  
##### No permitir redirección de puertos COM
  
Esta configuración de directiva se puede utilizar para evitar la redirección de datos a puertos de comunicación de cliente del equipo remoto en una sesión de Terminal Server. Si habilita esta configuración de directiva, los usuarios no podrán redirigir datos a periféricos de puertos COM ni asignar puertos COM locales mientras tienen abierta una sesión de Terminal Server. De forma predeterminada, los Servicios de Terminal Server permiten la redirección.
  
Si habilita el parámetro **No permitir redirección de puertos COM**, los usuarios no podrán redirigir los datos de servidor al puerto COM local. Si deshabilita esta configuración de directiva, la redirección de puertos COM de Servicios de Terminal Server se permite siempre. Si no establece esta configuración de directiva, la redirección de puertos COM no se especificará en el nivel de Directiva de grupo. Sin embargo, un administrador podrá seguir deshabilitando la redirección de puertos COM con la herramienta TSCC.
  
Los valores posibles para la configuración **No permitir redirección de puertos COM** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los datos se pueden reenviar desde la sesión de Terminal Server del usuario a su equipo local sin ninguna interacción directa del mismo.
  
###### Contramedida
  
Establezca **No permitir redirección de puertos COM** en **Habilitado**.
  
###### Impacto potencial
  
No se podrá realizar la redirección de puertos COM.
  
##### No permitir redirección de impresoras de cliente
  
Esta configuración de directiva especifica si pueden asignarse impresoras cliente en sesiones de Terminal Server. Puede utilizar esta configuración de directiva para evitar la redirección de trabajos de impresión a equipos locales (cliente) de usuarios desde el equipo remoto. De forma predeterminada, los Servicios de Terminal Server permiten la asignación de impresoras cliente.
  
Si habilita el parámetro **No permitir redirección de impresoras de cliente**, los usuarios no pueden redirigir trabajos de impresión del equipo remoto a una impresora local del cliente en sesiones de Terminal Server. Si deshabilita esta configuración de directiva, los usuarios pueden redirigir trabajos de impresión con la asignación de impresoras cliente. Si no establece esta configuración de directiva, la asignación de impresoras cliente no se especificará en el nivel de Directiva de grupo. Sin embargo, un administrador podrá seguir deshabilitando la asignación de impresoras con la herramienta TSCC.
  
Los valores posibles para la configuración **No permitir redirección de impresoras de cliente** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los datos se pueden reenviar desde la sesión de Terminal Server del usuario a su equipo local sin ninguna interacción directa del mismo.
  
###### Contramedida
  
Establezca **No permitir redirección de impresoras de cliente** en **Habilitado**.
  
###### Impacto potencial
  
No se podrá realizar la redirección de impresoras.
  
##### No permitir redirección de puertos LPT
  
Esta configuración de directiva especifica si se evitará la redirección de datos a puertos paralelos (LPT) cliente durante una sesión de Terminal Server. Puede utilizarla para evitar que los usuarios asignen puertos LPT locales para redirigir datos desde el equipo remoto a periféricos de puertos locales LPT. De forma predeterminada, los Servicios de Terminal Server permiten la redirección de puertos LPT.
  
Si usted habilita el parámetro **No permitir redirección de puertos LPT**, los usuarios en una sesión de Terminal Server no pueden redirigir los datos del servidor a su puerto LPT local. Si deshabilita esta configuración de directiva, la redirección de puertos LPT se permite siempre. Si no establece esta configuración, la redirección de puertos LPT no se especificará en el nivel de Directiva de grupo. Sin embargo, un administrador podrá seguir deshabilitando la redirección de puertos LPT locales con la herramienta TSCC.
  
Los valores posibles para la configuración **No permitir redirección de puertos LPT** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los datos se pueden reenviar desde la sesión de Terminal Server del usuario a su equipo local sin ninguna interacción directa del mismo.
  
###### Contramedida
  
Establezca **No permitir redirección de puertos LPT** en **Habilitado**.
  
###### Impacto potencial
  
No se podrá realizar la redirección de puertos LPT.
  
##### No permitir redirección de unidad
  
De forma predeterminada, los Servicios de Terminal Server asignan unidades de cliente automáticamente al conectarse. Las unidades asignadas aparecen en el árbol de carpeta de sesión en el formato *&lt;letra\_de\_la\_unidad&gt;* en *&lt;nombre\_del\_equipo&gt;*. Puede utilizar la configuración **No permitir redirección de unidad** para omitir este valor de configuración.
  
Puede habilitar el parámetro **No permitir redirección de unidad** para evitar la redirección de unidades cliente en sesiones de Terminal Server. Si deshabilita esta configuración de directiva, la redirección de unidades cliente se permite siempre. Si no establece esta configuración de directiva, la redirección de unidad cliente no se especificará en el nivel de Directiva de grupo. Sin embargo, un administrador podrá seguir deshabilitando la redirección de unidades de cliente con la herramienta TSCC.
  
Los valores posibles para la configuración **No permitir redirección de unidad** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los datos se pueden reenviar desde la sesión de Terminal Server del usuario a su equipo local sin ninguna interacción directa del mismo.
  
###### Contramedida
  
Establezca **No permitir redirección de unidad** en **Habilitado**.
  
###### Impacto potencial
  
No se podrá realizar la redirección de unidad.
  
##### No establecer impresora predeterminada de cliente como impresora predeterminada para una sesión
  
Esta configuración de directiva evita que los Servicios de Terminal Server especifiquen la impresora predeterminada cliente como la impresora predeterminada para sesiones de Terminal Server. De forma predeterminada, los servicios de Terminal Server designan automáticamente la impresora cliente como predeterminada. Este parámetro puede anular la configuración predeterminada.
  
Si habilita el parámetro **No establecer impresora predeterminada de cliente como impresora predeterminada para una sesión**, los servicios de Terminal Server no pueden establecer la impresora predeterminada cliente como la impresora predeterminada para la sesión. En su lugar, el servidor especificará la predeterminada en el servidor. Si deshabilita esta configuración de directiva, la impresora predeterminada será siempre la predeterminada de cliente. Si no configura este parámetro, la designación de impresora predeterminada no se implanta en el nivel de Directiva de grupo. Sin embargo, un administrador aún podrá configurar la impresora predeterminada para las sesiones de clientes utilizando la herramienta TSCC.
  
Los valores posibles para la configuración **No establecer impresora predeterminada de cliente como impresora predeterminada para una sesión** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los datos se pueden reenviar desde la sesión de Terminal Server del usuario a su equipo local sin ninguna interacción directa del mismo.
  
###### Contramedida
  
Establezca esta configuración de directivaen **Habilitado**.
  
###### Impacto potencial
  
La impresora predeterminada de un equipo cliente no será la predeterminada durante la sesión de Terminal Server.
  
#### Cifrado y seguridad
  
Puede establecer la configuración Cifrado y seguridad de Terminal Server en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\**  
**Servicios de Terminal Server\\Cifrado y seguridad.**
  
##### Establecer el nivel de cifrado de conexión de cliente
  
Esta configuración de directiva especifica si se aplica un nivel de cifrado a todos los datos enviados entre el cliente y el equipo remoto durante una sesión de Terminal Server.
  
Si habilita el parámetro **Establecer el nivel de cifrado de conexión de cliente**, puede especificar el nivel de cifrado para todas las conexiones al servidor. De forma predeterminada, el cifrado se establece en Alto nivel. Si deshabilita o no establece esta configuración de directiva, no se implanta un nivel de cifrado a través de Directiva de grupo. No obstante, los administradores aún podrán establecer el nivel en el servidor con la herramienta TSCC.
  
Los valores posibles para la configuración **Establecer el nivel de cifrado de conexión de cliente** son:
  
-   **Habilitado**, en el que se incluyen las siguientes opciones de cifrado:
  
    -   **Cliente compatible**. Este valor cifra los datos enviados entre el cliente y el servidor con la fuerza máxima de la clave admitida por el cliente. Emplee este nivel cuando el equipo remoto se ejecute en un entorno con clientes mezclados o heredados.
  
    -   **Alto nivel**. Este valor cifra los datos enviados entre el cliente y el servidor utilizando un cifrado seguro de 128 bits. Utilice este nivel siempre que el equipo remoto se ejecute en un entorno que sólo incluya clientes de 128 bits, como clientes de Conexión a Escritorio remoto. Los clientes que no admitan este nivel de cifrado no se podrán conectar.
  
    -   **Bajo nivel**. Este valor cifra los datos que se envían del cliente al servidor con cifrado de 56 bits. Cuando se especifica Bajo nivel, los datos enviados desde servidor al cliente no se cifran.
  
-   **Deshabilitado**
  
-   **No configurado**
  
**Importante**: si la conformidad con FIPS ya ha sido habilitada por el parámetro **Criptografía de sistema: usar algoritmos que cumplan la norma FIPS para cifrado,** **firma** **y** **operaciones hash**, no podrá cambiar el nivel de cifrado a través de esta configuración de directiva ni con la herramienta TSCC.
  
###### Vulnerabilidad
  
Si se permiten conexiones de cliente de Terminal Server que usen cifrado de bajo nivel, es más probable que un atacante pueda descifrar el tráfico de red capturado de Servicios de Terminal Server.
  
###### Contramedida
  
Defina **Establecer el nivel de cifrado de conexión de cliente** en **Alto nivel**.
  
###### Impacto potencial
  
Los clientes que no admitan el cifrado de 128 bits, no podrán establecer sesiones de Terminal Server.
  
##### Pedir siempre al cliente la contraseña al conectarse
  
Esta configuración de directiva especifica si los Servicios de Terminal Server solicitarán siempre al cliente una contraseña cuando se conecte. Puede utilizar esta configuración de directiva para forzar la petición de una contraseña a los usuarios que se conecten a los Servicios de Terminal Server, aunque ya se haya proporcionado una en el cliente de Conexión a Escritorio remoto. De forma predeterminada, los Servicios de Terminal Server permiten a los usuarios iniciar sesión de forma automática si han escrito una contraseña en el cliente de Conexión a Escritorio remoto.
  
Si habilita el parámetro **Pedir siempre al cliente la contraseña al conectarse**, los usuarios no podrán iniciar sesión de forma automática en los Servicios de Terminal Server, aun cuando hayan suministrado sus contraseñas en el cliente de Conexión a Escritorio remoto. Se les solicitará una contraseña para iniciar sesión. Si deshabilita esta configuración de directiva, los usuarios siempre podrán iniciar una sesión automáticamente en los Servicios de Terminal Server si suministran sus contraseñas en el cliente de Conexión a Escritorio remoto. Si no establece esta configuración de directiva, el inicio de sesión automático no se especificará en el nivel de Directiva de grupo. Sin embargo, un administrador podrá seguir solicitando la contraseña con la herramienta TSCC.
  
Los valores posibles para la configuración **Pedir siempre al cliente la contraseña al conectarse** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los usuarios pueden almacenar tanto su nombre de usuario como su contraseña cuando creen un nuevo acceso directo de Conexión a Escritorio remoto. Si el servidor que ejecuta los Servicios de Terminal Server permite a los usuarios que hayan utilizado esta característica iniciar sesión en el servidor sin tener que proporcionar la contraseña, es posible que un atacante que haya obtenido acceso físico al equipo del usuario se pueda conectar a un servidor Terminal Server con el método abreviado de Conexión a Escritorio remoto, aunque no conozca la contraseña del usuario.
  
###### Contramedida
  
Establezca **Pedir siempre al cliente la contraseña al conectarse** en **Habilitado**.
  
###### Impacto potencial
  
Los usuarios siempre tendrán que proporcionar sus contraseñas al establecer nuevas sesiones de Terminal Server.
  
#### Directiva de Seguridad RPC
  
El valor RPC Security de Terminal Server se puede configurar en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Servicios de Terminal Server\\Cifrado y seguridad\\Directiva de Seguridad RPC**
  
##### Servidor seguro (requerir seguridad)
  
Esta configuración de directiva especifica si un servidor Terminal Server requiere comunicaciones de llamada a procedimiento remoto (RPC) seguras con todos los clientes o, por el contrario, permite comunicaciones no seguras. Puede utilizarla para reforzar la seguridad de la comunicación RPC con los clientes, permitiendo únicamente solicitudes autenticadas y cifradas.
  
Si habilita el parámetro **Servidor seguro (requerir seguridad)**, los servicios de Terminal Server sólo aceptarán solicitudes de clientes RPC que admitan solicitudes seguras. No permitirá las comunicaciones no seguras con clientes que no sean de confianza. Si deshabilita esta configuración de directiva, los servicios de Terminal Server siempre aceptarán las solicitudes en cualquier nivel de seguridad para todo el tráfico RPC. Sin embargo, sí que se permite la comunicación no segura para los clientes RPC que no responden a la solicitud. Si no establece esta configuración de directiva, se permitirán las comunicaciones no seguras.
  
Los valores posibles para la configuración **Servidor seguro (requerir seguridad)** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
**Nota**: utilice la interfaz RPC para administrar y configurar los Servicios de Terminal Server.
  
###### Vulnerabilidad
  
La comunicación RPC no segura expone al servidor a los ataques de tipo "hombre en el medio" y de revelación de datos. Un ataque de tipo "hombre en el medio" se produce cuando un intruso captura paquetes entre un servidor y un cliente y los modifica antes de que se intercambien. Generalmente el atacante modificará la información de los paquetes para hacer que el cliente o el servidor revelen información importante.
  
###### Contramedida
  
Establezca **Servidor seguro (requerir seguridad)** como **Habilitado**.
  
###### Impacto potencial
  
Los clientes que no admiten RPC seguro no podrán administrar el servidor de forma remota.
  
#### Sesiones
  
Puede configurar valores adicionales de RPC Security de Terminal Server en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\Servicios de Terminal Server\\Cifrado y seguridad\\Sesiones**
  
##### Establece un tiempo límite para sesiones desconectadas
  
Esta configuración de directiva especifica un plazo límite para las sesiones de Terminal Server desconectadas. Puede utilizarla para especificar la cantidad máxima de tiempo que una sesión desconectada permanece activa en el servidor. De forma predeterminada, los Servicios de Terminal Server permiten a los usuarios desconectarse de una sesión remota, pero no requieren que cierren y terminen la sesión. Cuando una sesión se encuentra en estado desconectado, puede que los programas continúen en ejecución aunque el usuario ya no esté conectado de forma activa. De forma predeterminada, estas sesiones desconectadas se mantienen durante un tiempo ilimitado en el servidor.
  
Puede habilitar el parámetro **Establece un tiempo límite para sesiones desconectadas** para borrar sesiones desconectadas del servidor después de un cierto tiempo. Para aplicar el comportamiento predeterminado que mantiene las sesiones desconectadas durante un tiempo ilimitado, seleccione **Nunca**. Si deshabilita o no establece esta configuración de directiva, no se especifica un límite para las sesiones desconectadas en el nivel de Directiva de grupo.
  
Los valores posibles para la configuración **Establece un tiempo límite para sesiones desconectadas** son:
  
-   Habilitado, en el que se incluyen las siguientes opciones de especificación de tiempo:
  
    -   Nunca
  
    -   1 minuto
  
    -   5 minutos
  
    -   10 minutos
  
    -   15 minutos
  
    -   30 minutos
  
    -   1 hora
  
    -   2 horas
  
    -   3 horas
  
    -   1 día
  
    -   2 días
  
-   Deshabilitado
  
-   No configurado
  
**Nota**: esta configuración de directiva no se aplica a las sesiones de consola como, por ejemplo, sesiones de Escritorio remoto con equipos que ejecuten Windows XP Professional. Esta configuración de directiva existe en los nodos Configuración del equipo y Configuración de usuario. Cuando está configurado en ambos lugares, el parámetro Configuración del equipo tiene prioridad sobre el mismo parámetro en el nodo Configuración de usuario.
  
###### Vulnerabilidad
  
Todas las sesiones de Terminal Server utilizan recursos del sistema. A menos que las sesiones que se hayan desconectado durante un período largo de tiempo se den por terminadas, puede que los servidores se ejecuten con pocos recursos.
  
###### Contramedida
  
Defina **Establece un tiempo límite para sesiones desconectadas** como **Habilitado** y seleccione la opción **1 día** en el cuadro de lista **Terminar una sesión desconectada**.
  
###### Impacto potencial
  
Las sesiones de Terminal Server de aquellos usuarios que olviden desconectarse se darán por terminadas tras 24 horas de inactividad.
  
##### Permitir reconexiones sólo desde el cliente original
  
Esta configuración de directiva le permite evitar las reconexiones de Servicios de Terminal Server a sesiones desconectadas por parte de usuarios que utilizan equipos diferentes al equipo cliente original desde el que crearon la sesión. De forma predeterminada, los Servicios de Terminal Server permiten a los usuarios realizar una nueva conexión a las sesiones desconectadas desde cualquier equipo cliente.
  
Si habilita el parámetro **Permitir reconexiones sólo desde el cliente original**, los usuarios podrán conectarse de nuevo a sesiones desconectadas sólo desde el equipo cliente original. Si un usuario intentara conectar a la sesión desconectada desde otro equipo, se crearía una nueva sesión. Si deshabilita la configuración, los usuarios siempre se podrán conectar a una sesión desconectada desde cualquier equipo. Si no configura este parámetro, no se especifican reglas de reconexión de sesión en el nivel de Directiva de grupo.
  
Los valores posibles para la configuración **Permitir reconexiones sólo desde el cliente original** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
**Importante**: sólo los clientes de Citrix ICA que proporcionan un número de serie en la conexión admiten esta configuración; se ignora si el usuario se conecta con un cliente de Windows. Este parámetro existe en los nodos Configuración del equipo y Configuración de usuario. Cuando está configurado en ambos lugares, el parámetro Configuración del equipo tiene prioridad sobre el mismo parámetro en el nodo Configuración de usuario.
  
###### Vulnerabilidad
  
De forma predeterminada, los usuarios pueden volver a establecer las sesiones desconectadas de Terminal Server desde cualquier equipo. Si habilita este parámetro, los usuarios sólo podrán conectarse de nuevo desde el equipo que se utilizó originalmente para establecer la conexión. El valor de esta contramedida se ve limitado por el hecho de que sólo se aplica a los usuarios que se conectan con clientes de Citrix ICA.
  
###### Contramedida
  
Establezca **Permitir reconexiones sólo desde el cliente original** como **Habilitado**.
  
###### Impacto potencial
  
Los usuarios que se conectan a través de los clientes de Citrix ICA sólo podrán volver a establecer sesiones desconectadas con el equipo que hayan utilizado para establecer la sesión.
  
#### Explorador de Windows
  
Puede establecer la siguiente configuración del Explorador de Windows en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\**  
**Windows Explorer**
  
##### Desactivar modo protegido de protocolo de shell
  
Esta configuración de directiva le permite configurar el nivel de funcionalidad del protocolo de shell. La funcionalidad completa de este protocolo permite que las aplicaciones abran carpetas y ejecuten archivos. El modo protegido reduce la funcionalidad y sólo permite que las aplicaciones abran un conjunto limitado de carpetas. Las aplicaciones no pueden abrir los archivos cuando este protocolo se encuentra en modo protegido.
  
Microsoft recomienda que usted deje este protocolo en modo protegido para reforzar la seguridad de Windows. Si habilita el parámetro **Desactivar modo protegido de protocolo de shell**, el protocolo permite que cualquier aplicación abra cualquier carpeta o archivo. Si deshabilita o no establece esta configuración de directiva, el protocolo estará en modo protegido y las aplicaciones sólo podrán abrir un conjunto limitado de carpetas.
  
Los valores posibles para la configuración **Desactivar modo protegido de protocolo de shell** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
La funcionalidad completa de protocolo de shell permite que las aplicaciones abran carpetas y archivos. Esta capacidad puede tener como resultado la invocación accidental de software malintencionado o destructivo y la divulgación de información no autorizada. También podría tener como resultado una condición de denegación de servicio.
  
###### Contramedida
  
Establezca **Desactivar modo protegido de protocolo de shell** como **Habilitado**.
  
###### Impacto potencial
  
Si habilita el parámetro **Desactivar modo protegido de protocolo de shell**, las páginas web que dependen del uso del protocolo de shell no funcionarán apropiadamente.
  
#### Windows Messenger
  
Windows Messenger sirve para enviar mensajes instantáneos a otros usuarios en una red de equipos. Estos mensajes podrán incluir archivos y otros datos adjuntos.
  
Puede establecer la configuración recomendada de Windows Messenger en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\**  
**Windows Messenger**
  
##### No permitir que se ejecute Windows Messenger
  
El parámetro **No permitir que se ejecute Windows Messenger** le permite deshabilitar Windows Messenger. Puede configurar este parámetro como **Habilitado** para evitar el uso de Windows Messenger.
  
**Nota**: si configura este parámetro como Habilitado, la Asistencia Remota no puede utilizar Windows Messenger y los usuarios no pueden utilizar MSN® Messenger.
  
#### Windows Update
  
Utilice Windows Update para descargar elementos como, por ejemplo, actualizaciones de seguridad, actualizaciones importantes, los archivos de ayuda más recientes, controladores y productos de Internet. Puede establecer la configuración de Windows Update en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows\\**
  
##### Configurar actualizaciones automáticas
  
Esta configuración de directiva especifica si los equipos del entorno recibirán actualizaciones de seguridad y otra información importante a través del servicio de actualizaciones automáticas de Windows.
  
Si habilita el parámetro **Configurar actualizaciones automáticas**, Windows determina si los equipos están en línea y utiliza la conexión a Internet para buscar nuevas actualizaciones en el sitio web de Windows Update. Si deshabilita esta configuración de directiva, las actualizaciones se deben descargar manualmente y deben instalarse desde el sitio web [Windows Update](http://update.microsoft.com/windowsupdate/v6/default.aspx?ln=es) en http://windowsupdate.microsoft.com. Si no configura este parámetro, no se especifica el uso de Actualizaciones automáticas en el nivel de Directiva de grupo. No obstante, los administradores aún podrán seguir configurando las actualizaciones automáticas desde el Panel de control.
  
Los valores posibles para la configuración **Configurar actualizaciones automáticas** son:
  
-   **Habilitado**, con opciones en el cuadro de lista **Configurar actualización automática** para:
  
    -   **2. Notificar antes de descargar las actualizaciones y notificar de nuevo antes de instalarlas.**
  
        Cuando Windows encuentra actualizaciones aplicables a los equipos del entorno, aparece un icono en el área de estado con un mensaje que indica que ya se pueden descargar las actualizaciones. Si hace clic en el icono o mensaje, puede seleccionar actualizaciones específicas. A continuación, Windows descarga las actualizaciones seleccionadas en segundo plano. Una vez finalizada la descarga, el icono vuelve a aparecer en el área de estado, notificando que las actualizaciones ya se pueden instalar. Si hace clic en el icono o mensaje, puede seleccionar las actualizaciones que se van a instalar.
  
    -   **3. Descargar las actualizaciones automáticamente y enviar una notificación cuando se puedan instalar.** 
  
        Ésta es la configuración predeterminada. Windows encuentra actualizaciones aplicables a los equipos del entorno y las descarga en segundo plano sin notificar ni interrumpir al usuario durante este proceso. Una vez finalizada la descarga, aparece un icono en el área de estado, notificando que las actualizaciones ya se pueden instalar. Vuelva a hacer clic en el icono o mensaje para seleccionar las actualizaciones que se van a instalar.
  
    -   **4. Descargar las actualizaciones automáticamente e instalarlas en la programación especificada debajo.**
  
        Especifique la programación con las opciones de configuración de Directiva de grupo. Si no especifica ninguna, la programación predeterminada para todas las instalaciones será diariamente a las 3:00 a.m. Si alguna de las actualizaciones requiere que se reinicie el equipo para completar la instalación, Windows lo hará automáticamente. Si un usuario inicia una sesión en el equipo cuando Windows está preparado para reiniciarse, el usuario recibirá una notificación y podrá posponer el reinicio del sistema.
  
-   **Deshabilitado**
  
-   **No configurado**
  
Para habilitar esta configuración, haga clic en **Habilitado** y, a continuación, seleccione una de las opciones (2, 3 ó 4). Si selecciona 4, podrá definir una programación recurrente. Si no especifica ninguna programación, las instalaciones tendrán lugar diariamente a las 3:00 a.m.
  
###### Vulnerabilidad
  
Aunque Windows Server 2003 y Windows XP se sometieron a diversas pruebas exhaustivas antes de su comercialización, puede que se descubran problemas tras su distribución. El parámetro **Configurar** **actualizaciones automáticas** ayuda a garantizar que los equipos del entorno siempre tengan instaladas las actualizaciones y los Service Packs importantes más recientes del sistema operativo.
  
###### Contramedida
  
Establezca **Configurar actualizaciones automáticas** en **Habilitado** y seleccione **4. Descargar las actualizaciones automáticamente e instalarlas en la programación especificada debajo** del cuadro de lista **Configurar actualización automática**.
  
###### Impacto potencial
  
Las actualizaciones y los Service Packs importantes del sistema operativo se descargarán automáticamente a las 3:00 a.m. todos los días.
  
##### No reiniciar automáticamente para instalaciones de actualizaciones automáticas
  
Esta configuración de directiva especifica que las Actualizaciones automáticas esperarán a que los usuarios con una sesión iniciada en el equipo lo reinicien para completar una instalación programada.
  
Si habilita el parámetro **No reiniciar automáticamente para instalaciones de actualizaciones automáticas programadas**, Actualizaciones automáticas no reinicia automáticamente los equipos durante las instalaciones programadas. En su lugar, Actualizaciones automáticas solicita a los usuarios que reinicien los equipos con el fin de completar las instalaciones. Tenga en cuenta que Actualizaciones automáticas no detectará actualizaciones posteriores hasta que no se reinicien los equipos implicados. Si deshabilita o no configura este parámetro, Actualizaciones automáticas notificará al usuario que el equipo se reiniciará automáticamente en 5 minutos para completar la instalación.
  
Los valores posibles para la configuración **No reiniciar automáticamente para instalaciones de actualizaciones automáticas programadas** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
**Nota**: este parámetro sólo es aplicable al configurar Actualizaciones automáticas para que realicen las instalaciones de actualizaciones programadas. Si establece el parámetro **Configurar actualizaciones automáticas** como **Deshabilitado**, éste no tendrá efecto.
  
###### Vulnerabilidad
  
A veces, las actualizaciones requieren que los equipos actualizados se reinicien para completar una instalación. Si el equipo no se puede reiniciar automáticamente, la actualización más reciente no se instalará por completo. Asimismo, no se descargarán actualizaciones nuevas en el equipo hasta que no se reinicie.
  
###### Contramedida
  
Establezca **No reiniciar automáticamente para instalaciones de actualizaciones automáticas** en **Deshabilitado**.
  
###### Impacto potencial
  
Si usted habilita esta configuración de directiva, los sistemas operativos de los servidores del entorno se reiniciarán automáticamente. En el caso de servidores clave, esto podría ocasionar una condición DoS temporal y no esperada.
  
##### Volver a programar la instalación programada de actualizaciones automáticas
  
Esta configuración de directiva especifica el período de tiempo que Actualizaciones automáticas esperará (después del inicio) antes de proceder con las instalaciones programadas no completadas. Si habilita este parámetro, se iniciará la instalación que no tuvo lugar anteriormente, transcurrido un número determinado de minutos después del siguiente inicio del equipo. Si deshabilita o no configura este parámetro, las instalaciones programadas que se omitieron anteriormente ocurrirán con la siguiente instalación programada.
  
Los valores posibles para la configuración **Volver a programar la instalación programada de actualizaciones automáticas** son:
  
-   Habilitado, con la opción de especificar un período de entre 1 y 60 minutos.
  
-   Deshabilitado
  
-   No configurado
  
**Nota**: este parámetro sólo es aplicable al configurar Actualizaciones automáticas para que realicen las instalaciones de actualizaciones programadas. Si establece el parámetro **Configurar actualizaciones automáticas** como **Deshabilitado**, éste no tendrá efecto.
  
###### Vulnerabilidad
  
Si no obliga a que Actualizaciones automáticas espere varios minutos tras el reinicio del sistema, puede que los equipos del entorno no dispongan del tiempo suficiente para iniciar completamente todas sus aplicaciones y servicios. Si especifica un período de tiempo adecuado tras el reinicio del sistema, no tendrán lugar conflictos entre las instalaciones de actualizaciones nuevas y los procedimientos de inicio del equipo.
  
###### Contramedida
  
Establezca **Volver a programar la instalación programada de actualizaciones automáticas** como **Habilitado** y especifique 10 minutos.
  
###### Impacto potencial
  
Actualizaciones automáticas no se iniciará hasta que no hayan transcurrido 10 minutos tras el reinicio del equipo.
  
##### Especificar la ubicación del servicio Windows Update de la intranet
  
Esta configuración de directiva le permite especificar un servidor de intranet para alojar actualizaciones del sitio web Microsoft Update. A continuación, podrá utilizar esta ubicación del servicio de actualizaciones para actualizar automáticamente los equipos en la red. El cliente de Actualizaciones automáticas buscará en este servicio las actualizaciones aplicables a los equipos de la red.
  
Para utilizar el parámetro **Especificar la ubicación del servicio Windows Update de la intranet**, debe configurar dos valores de nombre de servidor: el servidor desde el que el cliente con Actualizaciones automáticas detecta y descarga las actualizaciones y el servidor en el que las estaciones de trabajo actualizadas cargarán las estadísticas. Puede definir ambos valores para que sean el mismo servidor.
  
Si habilita el parámetro **Especificar la ubicación del servicio Windows Update de la intranet**, el cliente con Actualizaciones automáticas se conectará a un servicio de actualizaciones de Microsoft de la intranet especificado (en lugar de a Windows Update) para buscar y descargar actualizaciones. Esta configuración permite que los usuarios finales en su organización eviten los problemas de servidor de seguridad, y le brinda la oportunidad de probar las actualizaciones antes de implementarlas. Si deshabilita o no establece esta configuración de directiva, el cliente con Actualizaciones automáticas se podrá conectar directamente con el sitio de Windows Update en Internet (si Actualizaciones automáticas no se ha deshabilitado desde Directiva de grupo o en las preferencias del usuario).
  
Los valores posibles para la configuración **Especificar la ubicación del servicio Windows Update de la intranet** son:
  
-   Habilitado. Tras seleccionar este valor, especifique el nombre del servidor de actualizaciones de la intranet y el nombre del servidor de estadísticas en el cuadro de diálogo **Propiedades**.
  
-   Deshabilitado
  
-   No configurado
  
**Nota**: si establece el parámetro **Configurar actualizaciones automáticas** como **Deshabilitado**, esta configuración de directiva no tendrá efecto.
  
###### Vulnerabilidad
  
De forma predeterminada, Actualizaciones automáticas intentará descargar las actualizaciones desde el sitio web de Microsoft Windows Update. Algunas organizaciones prefieren comprobar que todas las actualizaciones nuevas son compatibles con su entorno antes de implementarlas. Asimismo, la configuración de un servidor Software Update Service (SUS) interno ayudará a reducir la carga en los servidores de seguridad perimetrales, enrutadores y servidores proxy, así como la carga en los vínculos de red externos.
  
###### Contramedida
  
Establezca **Especificar la ubicación del servicio Windows Update de la intranet** como **Habilitado**. A continuación, especifique el nombre del servidor de actualizaciones de la intranet y el del servidor de estadísticas en el cuadro de diálogo **Propiedades**.
  
###### Impacto potencial
  
La administración de las actualizaciones y los Service Packs importantes la deberá llevar a cabo el personal de TI de la organización.
  
#### Sistema
  
Puede establecer la configuración de equipo de sistema recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema**
  
##### Desactivar reproducción automática
  
Reproducción automática inicia la lectura desde una unidad en cuanto inserte el medio en la misma, provocando el inicio inmediato del archivo de configuración de programas y los medios de audio. Puede habilitar el parámetro **Desactivar reproducción automática** para omitir la funcionalidad de reproducción automática. La reproducción automática se deshabilita de forma predeterminada en algunas unidades extraíbles, como unidades de disquete y de red, pero está habilitada de forma predeterminada en unidades de CD-ROM.
  
**Nota**: no puede utilizar este parámetro para habilitar la reproducción automática en unidades del equipo que están deshabilitadas de forma predeterminada, como unidades de disquete y de red.
  
###### Vulnerabilidad
  
Un atacante podría utilizar esta característica para iniciar un programa que dañe un equipo cliente o los datos del equipo.
  
###### Contramedida
  
Establezca **Desactivar reproducción automática** en **Habilitado**.
  
###### Impacto potencial
  
Los usuarios tendrán que iniciar manualmente los programas de instalación o de configuración que se proporcionan en medios extraíbles.
  
#### Inicio de sesión
  
Puede establecer la configuración de inicio de sesión del equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema\\Inicio de sesión**
  
##### No mostrar la pantalla de bienvenida de introducción al iniciar la sesión
  
Esta configuración de directiva oculta la pantalla de bienvenida que Microsoft Windows 2000 Professional y Windows XP Professional muestran cada vez que el usuario inicia sesión. No obstante, el usuario puede ver esta pantalla seleccionándola en el menú **Inicio**.
  
El parámetro **No mostrar la pantalla de bienvenida de introducción al iniciar la sesión** sólo se aplica a Microsoft Windows 2000 Professional y Windows XP Professional. No afecta al parámetro **Configurar el servidor** en Windows 2000 Server o Windows Server 2003.
  
Los valores posibles para la configuración **No mostrar la pantalla de bienvenida de introducción al iniciar la sesión** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
**Nota**: esta configuración de directiva aparece en los nodos Configuración del equipo y Configuración de usuario. Si configura ambos valores, el de Configuración del equipo tendrá prioridad sobre el del nodo Configuración de usuario.
  
###### Vulnerabilidad
  
La pantalla de bienvenida de introducción al iniciar la sesión anima a los usuarios a explorar el escritorio de Windows XP. Algunas organizaciones prefieren proporcionar a sus usuarios entrenamiento centrado en la función y las tareas que deben realizar, así como alejarlos de otras fuentes de información.
  
###### Contramedida
  
Establezca **No mostrar la pantalla de bienvenida de introducción al iniciar la sesión** en **Habilitado**.
  
###### Impacto potencial
  
Los usuarios no verán la pantalla de bienvenida de introducción al iniciar sesión en sus equipos.
  
##### No procesar la lista de ejecución heredada
  
El parámetro **No procesar la lista de ejecución heredada** hace que se ignore la lista de ejecución (lista de programas que Windows XP ejecuta automáticamente cuando se inicia). Las listas de ejecución personalizadas de Windows XP se almacenan en el registro en las siguientes ubicaciones:
  
-   HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\Run
  
-   HKEY\_CURRENT\_USER\\Software\\Microsoft\\Windows\\CurrentVersion\\Run
  
Los valores posibles para la configuración **No procesar la lista de ejecución heredada** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Un usuario malintencionado podría configurar un programa para que se ejecute cada vez que se inicia Windows, y poner en peligro los datos del equipo o causar otros daños.
  
###### Contramedida
  
Establezca **No procesar la lista de ejecución heredada** en **Habilitado**.
  
###### Impacto potencial
  
Si habilita este parámetro, no podrán ejecutarse algunos programas como el software antivirus y los programas de distribución y supervisión de software. Debe evaluar el nivel de amenaza en el entorno para cuya protección se ha diseñado este parámetro, antes de decidir la estrategia de uso del mismo en su organización.
  
##### No procesar la lista de una sola ejecución
  
Esta configuración de directiva hace que se ignore la lista de una sola ejecución (la lista de programas que Windows XP ejecuta automáticamente cuando se inicia). Esto difiere del parámetro **No procesar la lista de ejecución heredada** en que los programas de la lista se ejecutarán una sola vez la siguiente vez que se reinicie el cliente. Los programas de instalación y configuración a veces se agregan a esta lista para finalizar las instalaciones después de que un cliente se reinicie. Si habilita esta configuración de directiva, los atacantes no pueden utilizar la lista de una sola ejecución para iniciar aplicaciones malintencionadas, que era un método común de ataque en el pasado.
  
**Nota**: las listas personalizadas de una sola ejecución se almacenan en el Registro en la ubicación siguiente: **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce**.
  
Los valores posibles para la configuración **No procesar la lista de una sola ejecución** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Un usuario malintencionado puede explotar la lista de una sola ejecución para instalar un programa que comprometa la seguridad de los clientes Windows XP.
  
###### Contramedida
  
Establezca **No** **procesar la lista de una sola ejecución** como **Habilitado**.
  
###### Impacto potencial
  
Si habilita el parámetro **No** **procesar la lista de una sola ejecución**, se ocasionará una pérdida de funcionalidad mínima para los usuarios del entorno, sobre todo si se han configurado los clientes con todo el software estándar de la organización antes de aplicar este parámetro a través de Directiva de grupo. Sin embargo, esta configuración puede evitar que algunos programas de instalación y configuración, como los de Internet Explorer, funcionen apropiadamente.
  
#### Directiva de grupo.
  
Para modificar la forma en que se procesa la Directiva de grupo, puede configurar valores adicionales en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema\\Directiva de grupo**
  
##### Procesamiento de directivas de mantenimiento de Internet Explorer
  
Esta configuración de directiva determina cuándo se actualizan las directivas de mantenimiento de Internet Explorer. Afecta a todas las directivas que utilizan el componente Mantenimiento de Internet Explorer de Directiva de grupo, como las ubicadas en **Configuración de Windows\\Mantenimiento de Internet Explorer**. Este parámetro tiene prioridad sobre las configuraciones personalizadas que el programa de directiva de mantenimiento de Internet Explorer implementó al instalarse.
  
Si habilita el parámetro **Procesamiento de directivas de mantenimiento de Internet Explorer**, puede utilizar las casillas de verificación que se proporcionan para cambiar las opciones. Si deshabilita o no establece esta configuración de directiva, no hay repercusiones para el equipo.
  
Los valores posibles para la configuración **Procesamiento de directivas de mantenimiento de Internet Explorer** son:
  
-   **Habilitado**, en el que se incluyen las siguientes opciones:
  
    -   **Permitir el procesamiento a través de una conexión de red de baja velocidad**. con esta opción se actualizarán las directivas incluso cuando la transmisión se realice a través de una conexión de red de baja velocidad, como una línea telefónica. Las actualizaciones que se llevan a cabo a través de conexiones lentas pueden ocasionar retrasos significativos.
  
    -   **No aplicar durante el procesamiento periódico en segundo plano**. Esta opción impide que el equipo actualice las directivas afectadas en segundo plano mientras está en uso. Las actualizaciones en segundo plano pueden interrumpir al usuario, hacer que el programa se detenga o que funcione incorrectamente y, en raras ocasiones, dañar los datos.
  
    -   **Procesar incluso si los objetos de directiva de grupo no han cambiado**. Esta opción actualiza y vuelve a aplicar las directivas, aunque éstas no se hayan modificado. En las implementaciones de muchas directivas se especifica que sólo se actualizan cuando se han modificado. No obstante, puede que desee actualizar directivas que no hayan sufrido cambios, por ejemplo, para volver a aplicar una determinada configuración modificada por un usuario.
  
-   **Deshabilitado**
  
-   **No configurado**
  
###### Vulnerabilidad
  
Puede habilitar este parámetro y seleccionar la opción **Procesar incluso si los objetos de directiva de grupo no han cambiado** para garantizar que las directivas se vuelvan a procesar aunque no se hayan modificado. Este enfoque implantará directivas establecidas basadas en el dominio, incluso si se realizan cambios no autorizados de forma local.
  
###### Contramedida
  
Establezca **Procesamiento** de **directivas** de **mantenimiento** de **Internet** **Explorer** en **Habilitado**. A continuación, desactive las casillas de verificación **Permitir el procesamiento a través de una conexión de red de baja velocidad** y **No aplicar durante el procesamiento periódico en segundo plano** y active **Procesar incluso si los objetos de directiva de grupo no han cambiado**.
  
###### Impacto potencial
  
Las directivas de grupo se volverán a aplicar cada vez que se actualicen, lo que podría afectar levemente al rendimiento.
  
##### Procesamiento de directiva de seguridad IP
  
Esta configuración de directiva determina cuándo se actualizan las directivas de seguridad IP (IPSec). Afecta a todas las directivas que utilizan el componente IPSec de la Directiva de grupo. Esta configuración de directiva tiene prioridad sobre las configuraciones personalizadas que el programa de directiva de mantenimiento estableció al instalarse.
  
Si habilita el parámetro **Procesamiento de directiva de seguridad IP**, puede utilizar las casillas de verificación proporcionadas para cambiar las opciones. Si deshabilita o no configura este parámetro, no hay repercusiones para el equipo.
  
Los valores posibles para la configuración **Procesamiento de directiva de seguridad IP** son:
  
-   Habilitado, en el que se incluyen las siguientes opciones:
  
    -   Permitir el procesamiento a través de una conexión de red de baja velocidad
  
    -   No aplicar durante el procesamiento periódico en segundo plano
  
    -   Procesar incluso si los objetos de directiva de grupo no han cambiado
  
-   Deshabilitado
  
-   No configurado
  
El parámetro **Permitir el procesamiento a través de una conexión de red de baja velocidad** actualiza las directivas incluso cuando la actualización se está transmitiendo a través de una conexión de red de baja velocidad, como una línea telefónica o un enlace WAN de ancho de banda bajo. Las actualizaciones que se llevan a cabo a través de conexiones lentas pueden ocasionar retrasos significativos. El parámetro **No aplicar durante el procesamiento periódico en segundo plano** impide la actualización de las directivas afectadas en segundo plano mientras el equipo está en uso. Las actualizaciones en segundo plano pueden interrumpir al usuario, hacer que el programa se detenga o que funcione incorrectamente y, en raras ocasiones, dañar los datos. El parámetro **Procesar incluso si los objetos de directiva de grupo no han cambiado** actualiza y vuelve a aplicar las directivas aunque éstas no se hayan modificado. En las implementaciones de muchas directivas se especifica que sólo se actualizan cuando se han modificado. No obstante, puede que desee actualizar periódicamente las directivas que no hayan sufrido cambios para volver a aplicar una determinada configuración que tal vez hayan modificado los usuarios.
  
###### Vulnerabilidad
  
Puede habilitar este parámetro y, a continuación, seleccionar la opción **Procesar incluso si los objetos de directiva de grupo no han cambiado** para garantizar que las directivas se vuelvan a procesar aunque no se haya modificado ninguna de ellas. De este modo, cualquier cambio no autorizado que pudiera haberse configurado localmente deberá coincidir de nuevo con la configuración de directiva de grupo basada en el dominio.
  
###### Contramedida
  
Establezca **Procesamiento de directiva de seguridad IP** en **Habilitado**. A continuación, desactive la casilla de verificación **No aplicar durante el procesamiento periódico en segundo plano** y active **Procesar incluso si los objetos de directiva de grupo no han cambiado**.
  
###### Impacto potencial
  
Las directivas de grupo de seguridad IP se volverán a aplicar cada vez que se actualicen, lo que podría afectar levemente al rendimiento y podría interferir con la conectividad de red existente.
  
##### Procesamiento de directivas de Registro
  
Esta configuración de directiva determina cuándo se actualizan las directivas del Registro. Afecta a todas las directivas de la carpeta Plantillas administrativas y a cualquier otra directiva que almacene valores en el Registro. Esta configuración de directiva tiene prioridad sobre las configuraciones personalizadas que el programa de directiva del Registro estableció al instalarse.
  
Si habilita el parámetro **Procesamiento de directivas de Registro**, puede utilizar las casillas de verificación que se proporcionan para cambiar las opciones. Si deshabilita o no configura este parámetro, no hay repercusiones para el equipo.
  
La opción **No aplicar durante el procesamiento periódico en segundo plano** puede utilizarse para garantizar que el equipo no actualice las directivas afectadas en segundo plano mientras el equipo está en uso. Las actualizaciones en segundo plano pueden interrumpir al usuario, hacer que los programas se detengan o que funcionen incorrectamente y, en raras ocasiones, dañar los datos. La opción **Procesar incluso si los objetos de directiva de grupo no han cambiado** actualiza y vuelve a aplicar las directivas aunque éstas no se hayan modificado. En muchas implementaciones de directivas de grupo se especifica que sólo se actualizan cuando se han modificado. No obstante, puede que desee actualizar directivas que no hayan sufrido cambios para volver a aplicar una determinada configuración modificada por un usuario.
  
Los valores posibles para la configuración **Procesamiento de directiva de Registro** son:
  
-   Habilitado, en el que se incluyen las siguientes opciones:
  
    -   No aplicar durante el procesamiento periódico en segundo plano
  
    -   Procesar incluso si los objetos de directiva de grupo no han cambiado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Puede habilitar este parámetro y, a continuación, seleccionar la opción **Procesar incluso si los objetos de directiva de grupo no han cambiado** para garantizar que las directivas se vuelvan a procesar aunque no se haya modificado ninguna de ellas. De este modo, cualquier cambio no autorizado que pudiera haberse configurado localmente deberá coincidir de nuevo con la configuración de directiva de grupo basada en el dominio.
  
###### Contramedida
  
Establezca **Procesamiento de directivas de Registro** en **Habilitado**. A continuación, desactive la casilla de verificación **No aplicar durante el procesamiento periódico en segundo plano** y active **Procesar incluso si los objetos de directiva de grupo no han cambiado**.
  
###### Impacto potencial
  
Las directivas de grupo se volverán a aplicar cada vez que se actualicen, lo que podría afectar levemente al rendimiento.
  
##### Procesamiento de directiva de seguridad
  
Esta configuración de directiva determina cuándo se actualizan las directivas de seguridad. Tiene prioridad sobre las configuraciones personalizadas que el programa de directiva de seguridad implementó al instalarse.
  
Si habilita el parámetro **Procesamiento de directivas de seguridad**, puede utilizar las casillas de verificación que se proporcionan para cambiar las opciones. Si deshabilita o no configura este parámetro, no hay repercusiones para el equipo.
  
La opción **No aplicar durante el procesamiento periódico en segundo plano** puede utilizarse para garantizar que el equipo no actualice las directivas afectadas en segundo plano mientras el equipo está en uso. Las actualizaciones en segundo plano pueden interrumpir al usuario, hacer que los programas se detengan o que funcionen incorrectamente y, en raras ocasiones, dañar los datos. La opción **Procesar incluso si los objetos de directiva de grupo no han cambiado** actualiza y vuelve a aplicar las directivas aunque éstas no se hayan modificado. En muchas implementaciones de directivas de grupo se especifica que sólo se actualizan cuando se han modificado. No obstante, puede que desee actualizar directivas que no hayan sufrido cambios para volver a aplicar una determinada configuración modificada por un usuario.
  
Los valores posibles para la configuración **Procesamiento de directiva de seguridad** son:
  
-   Habilitado, en el que se incluyen las siguientes opciones:
  
    -   No aplicar durante el procesamiento periódico en segundo plano
  
    -   Procesar incluso si los objetos de directiva de grupo no han cambiado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Puede habilitar este parámetro y, a continuación, seleccionar la opción **Procesar incluso si los objetos de directiva de grupo no han cambiado** para garantizar que las directivas se vuelvan a procesar aunque no se haya modificado ninguna de ellas. De este modo, cualquier cambio no autorizado que pudiera haberse configurado localmente deberá coincidir de nuevo con la configuración de directiva de grupo basada en el dominio.
  
###### Contramedida
  
Establezca **Procesamiento de directiva de seguridad** como **Habilitado**. A continuación, desactive la casilla de verificación **No aplicar durante el procesamiento periódico en segundo plano** y active **Procesar incluso si los objetos de directiva de grupo no han cambiado**.
  
###### Impacto potencial
  
Las directivas de grupo se volverán a aplicar cada vez que se actualicen, lo que podría afectar levemente al rendimiento.
  
#### Asistencia remota
  
Establezca la configuración de equipo de asistencia remota recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema\\Asistencia remota**
  
##### Ofrecer asistencia remota
  
Esta configuración de directiva determina si un técnico de soporte o un experto de TI pueden ofrecer asistencia remota a usuarios de equipos en el entorno sin una solicitud explícita de ayuda a través de otro canal (como correo electrónico o mensajería instantáneas).
  
**Nota**: el experto no puede conectarse al equipo sin avisar o controlarlo sin permiso del usuario. Cuando intente conectarse, el usuario podrá optar por rechazar la conexión y otorgar privilegios de sólo vista a la estación de trabajo. El usuario debe hacer clic en **Sí** para permitir que el experto controle remotamente la estación de trabajo, después de establecer el parámetro Ofrecer asistencia remota como **Habilitado**.
  
Si habilita el parámetro **Ofrecer asistencia remota**, tendrá las siguientes opciones:
  
-   Dar permiso a los servicios de ayuda para que sólo vean el equipo
  
-   Dar permiso a los servicios de ayuda para que controlen el equipo remotamente
  
Al establecer esta configuración, también puede especificar una lista de usuarios o grupos de usuarios conocidos como "servicios de ayuda" que pueden ofrecer asistencia remota.
  
**Para configurar la lista de servicios de ayuda**
  
1.  En la ventana de configuración del parámetro **Ofrecer asistencia remota**, haga clic en **Mostrar**. Aparecerá una ventana nueva en la que puede introducir los nombres de los servicios de ayuda.
  
2.  Agregue cada usuario o grupo a la lista de servicios de ayuda mediante uno de los siguientes formatos:
  
    -   &lt;Nombre de dominio&gt;\\&lt;Nombre de usuario&gt;
  
    -   &lt;Nombre de dominio&gt;\\&lt;Nombre de grupo&gt;
  
Si deshabilita o no establece el parámetro **Ofrecer asistencia remota**, los usuarios o grupos no podrán ofrecer asistencia remota no solicitada a los usuarios de equipos de su entorno.
  
###### Vulnerabilidad
  
Es posible que se engañe a un usuario para que acepte una oferta no solicitada de asistencia remota de un usuario malintencionado.
  
###### Contramedida
  
Establezca **Ofrecer asistencia remota** en **Deshabilitado**.
  
###### Impacto potencial
  
El personal de asistencia y soporte técnico no será capaz de ofrecer ayuda por iniciativa propia, aunque sí pueden responder a solicitudes de ayuda del usuario.
  
##### Solicit Remote Assistance
  
Esta configuración** **de directiva determina si puede pedirse asistencia remota desde equipos con Windows XP en su entorno. Si la habilita, los usuarios podrán solicitar asistencia remota para su estación de trabajo a un experto de TI.
  
**Nota**: el experto no puede conectarse al equipo sin avisar o controlarlo sin permiso del usuario. Cuando intente conectarse, el usuario podrá optar por rechazar la conexión y otorgar al especialista privilegios de sólo vista a la estación de trabajo. El usuario debe hacer clic en **Sí** para permitir que el experto controle de forma remota la estación de trabajo.
  
Si habilita el parámetro **Solicitar asistencia remota**, tiene las opciones siguientes para permitir el control remoto del equipo del usuario:
  
-   Dar permiso a los servicios de ayuda para que controlen el equipo remotamente
  
-   Dar permiso a los servicios de ayuda para que sólo vean el equipo
  
Además, las siguientes opciones están disponibles para configurar cuánto tiempo permanece válida una solicitud de ayuda del usuario:
  
-   Validez máxima del vale (valores):
  
-   Validez máxima del vale (unidades): horas, minutos o días
  
Cuando el vale (solicitud de ayuda) caduca, el usuario debe enviar otra solicitud antes de que el experto se conecte al equipo. Si deshabilita el parámetro **Solicitar asistencia remota**, los usuarios no podrán enviar solicitudes de ayuda y el experto no se podrá conectar a los equipos.
  
Cuando el parámetro **Solicitar asistencia remota** no está configurado, los usuarios podrán configurar la asistencia remota solicitada a través del Panel de control. De forma predeterminada, se habilitan los siguientes parámetros a través del Panel de control: Asistencia remota solicitada, Buddy support y Control remoto. El valor de Validez máxima del vale se establece en 30 días. Si deshabilita este parámetro, nadie tendrá acceso a clientes de Windows XP en la red.
  
###### Vulnerabilidad
  
Cuando el parámetro **Solicitar asistencia remota** está habilitado, los usuarios pueden enviar solicitudes de asistencia remota a personal no autorizado.
  
###### Contramedida
  
Establezca **Solicitar asistencia remota** como **Deshabilitado**.
  
###### Impacto potencial
  
Si configura **Solicitar asistencia remota** como **Deshabilitado**, los usuarios no podrán solicitar asistencia remota al personal de asistencia o soporte técnico.
  
#### Informe de errores
  
La característica Informe de errores corporativos de Windows permite a los administradores administrar los archivos contenedores creados por DW.exe y redirigir los informes de errores de detención a un servidor de archivos local. Esta capacidad proporciona una alternativa al envío directo de información a Microsoft a través de Internet. Una vez recopiladas las suficientes entradas de error de detención, los administradores pueden revisar la información y enviar sólo aquellos datos que consideren de utilidad para Microsoft.
  
Con la herramienta Informe de errores corporativos de Windows, los administradores pueden revisar los tipos más comunes de errores de detención que experimentan los usuarios y aprovechar esta información para indicar a los usuarios el modo de evitar estas situaciones.
  
Puede configurar la característica Informe de errores en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Sistema\\Informe de errores**
  
##### Mostrar notificación de errores
  
Puede utilizar esta configuración de directiva para controlar el envío de informes de errores por parte del usuario. Si la habilita, se notificará al usuario cada vez que se produzca un error y se le proporcionará información detallada sobre el mismo. Si habilita además el parámetro **Informar** de **errores**, el usuario tendrá la posibilidad de informar sobre el error.
  
Si no habilita el parámetro **Mostrar notificación de errores**, el usuario no tendrá la posibilidad de informar sobre errores. Si habilita el parámetro **Informar de errores**, se informará automáticamente sobre los errores, pero no se avisará al usuario cuando se produzcan.
  
Es útil deshabilitar este parámetro para equipos de servidor que no tienen usuarios interactivos. Si no configura este parámetro, el usuario podrá ajustarlo desde el Panel de control donde, de forma predeterminada, aparece seleccionada la opción **Habilitar notificación** en Windows XP y **Deshabilitar notificación** en Windows Server 2003.
  
Los valores posibles para la configuración **Mostrar notificación de errores** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Si se da a los usuarios la posibilidad de informar o no sobre los errores, puede que no respeten las directrices marcadas por la organización a este respecto. Si establece esta configuración de directiva en **Deshabilitado**, los usuarios no podrán ver los mensajes del informe de errores.
  
###### Contramedida
  
Establezca **Mostrar notificación de errores** en **Deshabilitado**.
  
###### Impacto potencial
  
Los usuarios no podrán ver los mensajes de informes de errores cuando se generen.
  
##### Informar de errores
  
Esta configuración de directiva controla si se informa sobre errores. Si configura el parámetro **Informar** de **errores** como **Habilitado**, los usuarios tendrán la capacidad de informar de errores cuando se produzcan. Se puede informar de los errores a Microsoft a través de Internet o a recursos compartidos locales en las organizaciones de usuarios.
  
Los valores posibles para la configuración **Informar de errores** son:
  
-   **Habilitado**, en el que se incluyen las siguientes opciones:
  
    -   **No mostrar vínculos a ningún sitio web de "más información" proporcionado por Microsoft**. Si selecciona esta opción, no se muestran vínculos a sitios web de Microsoft que pueden tener más información acerca del mensaje de error.
  
    -   **No recopilar archivos adicionales**. Si selecciona esta opción, no se recopilan más archivos para incluirlos en los informes de errores.
  
    -   **No recopilar información de equipos adicionales**. Si selecciona esta opción, no se incluye ninguna información adicional sobre el equipo en el que se ha producido el error en los informes de errores.
  
    -   **Forzar el modo de cola para errores de aplicación**. Si selecciona esta opción, los usuarios no tienen una opción para enviar un informe de error. En su lugar, se colocará el error en un directorio de cola y se dará la opción de informar sobre el error al próximo administrador que inicie sesión en el equipo.
  
    -   **Ruta de acceso al archivo de carga corporativa**. Puede seleccionar esta opción para especificar una ruta de acceso UNC (convención de nomenclatura universal) hacia un recurso compartido donde se cargan los informes de errores. Esta opción habilita también la herramienta Informe de errores corporativos.
  
    -   **Reemplazar todos los casos en que aparezca la palabra "Microsoft".** Si selecciona esta opción, podrá personalizar los cuadros de diálogo de informes de error con el nombre de su empresa.
  
-   **Deshabilitado**
  
-   **No configurado**
  
Si usted no configura esta configuración de directiva, los usuarios no podrán ajustar el parámetro en el Panel de control. La configuración predeterminada es **Habilitado** en Windows XP Profesional y **Deshabilitado** en Windows Server 2003.
  
Si la opción **Informar de errores** está habilitada, se anulará la configuración establecida en el Panel de control para la notificación de errores. Esta configuración también implantará los valores predeterminados a las directivas de informes de errores que no estén configuradas.
  
###### Vulnerabilidad
  
En esta configuración predeterminada, la característica Informe de errores corporativos en Windows XP, Windows Server 2003 y Office envía a Microsoft una serie de datos considerados de carácter confidencial por algunas organizaciones. La declaración de privacidad de Microsoft relativa a esta característica garantiza que Microsoft no hará un uso indebido de los datos recopilados a través de Informe de errores corporativos de Windows. No obstante, puede que las organizaciones deseen configurar esta herramienta para que no se transmita ningún tipo de información sin que la revise previamente un miembro de confianza del equipo de TI.
  
Por el contrario, si el parámetro Informar de errores se deshabilita completamente, es más difícil que Microsoft identifique y diagnostique errores nuevos. Además, las organizaciones que desarrollen sus propias aplicaciones empresariales internas pueden aprovechar Informe de errores corporativos de Windows para localizar problemas en su código.
  
Para garantizar la privacidad y realizar al mismo tiempo un uso eficaz de esta característica, resulta útil configurar servidores internos de Informe de errores corporativos (CER). Configure los equipos cliente para que envíen a estos servidores los posibles informes de errores. De este modo, un administrador podrá revisar los informes recibidos en los servidores CER y generar un informe global para Microsoft que no contenga información confidencial.
  
###### Contramedida
  
Establezca **Informar** de **errores** en **Habilitado** y, a continuación, configure la opción **Ruta de acceso al archivo de carga corporativa** para que señale a la ruta UNC correspondiente al servidor CER de la organización.
  
**Nota**: para obtener más información acerca de cómo crear un servidor de CER para su organización, consulte el sitio web de [Informe de errores corporativos de Windows](http://www.microsoft.com/spain/licencias/sa/cer.mspx) en www.microsoft.com/resources/satech/cer/.
  
###### Impacto potencial
  
Se habilitará la creación de informes de errores y se enviarán nuevos informes al servidor CER.
  
#### Administración de comunicaciones de Internet
  
Los productos de las familias Windows Server 2003 y Windows XP incluyen una variedad de tecnologías de comunicación con Internet para brindar una mayor facilidad de uso. Las tecnologías de exploración y de correo electrónico son los ejemplos obvios, pero hay también tecnologías como las Actualizaciones automáticas que ayudan a obtener la información más reciente de software y de productos, incluidas las revisiones de seguridad y las correcciones de errores. Estas tecnologías proporcionan muchos beneficios, pero esto conlleva la comunicación con sitios de Internet, que los administradores tal vez quieran mantener bajo control.
  
Puede controlar esta comunicación mediante una serie de opciones integradas en los componentes individuales, en el sistema operativo en su conjunto y en los componentes de servidor que se diseñan para administrar configuraciones en toda su organización. Por ejemplo, como administrador puede utilizar la Directiva de grupo para controlar la manera en que se comunican algunos componentes. Para algunos componentes, puede dirigir todas las comunicaciones al propio sitio web interno de la empresa en vez de a un sitio externo en Internet. Además, en Windows Server 2003 con Service Pack 1 (SP1) puede utilizar Firewall de Windows y el Asistente para configuración de seguridad (SCW) para ayudarle a controlar varios aspectos de su configuración tales como los servicios que se ejecutan y los puertos que están abiertos.
  
Microsoft ha producido dos guías detalladas para la administración de comunicaciones de Internet:
  
-   [*Introduction to Controlling Communication with the Internet for Windows Server 2003 with SP1*](http://technet2.microsoft.com/windowsserver/en/library/9b22059a-b325-4e1b-9501-bdc4bef0f2951033.mspx) *en* www.microsoft.com/technet/prodtechnol/windowsserver2003/library/  
    W2K3InternetMgmt/55f681e2-de6f-4d76-81d2-af7f889d66f6.mspx) describe cómo controlar las comunicaciones de Internet en equipos con Windows Server 2003 con SP1.
  
-   La guía [*Using Windows XP Service Pack 2 In a Managed Environment*](http://www.microsoft.com/technet/prodtechnol/winxppro/maintain/intmgmt/01_xpint.mspx)* *en www.microsoft.com/technet/prodtechnol/winxppro/maintain/intmgmt/01\_xpint.mspx describe cómo controlar las comunicaciones de Internet en equipos con Windows XP con SP2.
  
#### COM Distribuido
  
COM proporciona listas de control de acceso (ACL) de todo el equipo que controlan el acceso de todas las solicitudes de llamada, activación o inicio en el equipo. Puede considerar estos controles de acceso como una llamada adicional de comprobación de acceso que se hace contra una lista ACL de todo el equipo en cada llamada, activación o inicio de cualquier servidor COM en el equipo. Esta comprobación es adicional a cualquier comprobación de acceso que se ejecuta contra las listas ACL específicas del servidor. Si se produce un error de comprobación de acceso, se rechaza la solicitud de llamada, activación o inicio. De hecho, esta comprobación proporciona un estándar mínimo de autorización que se debe superar para tener acceso a cualquier servidor COM en el equipo. Para obtener más información acerca de DCOM, consulte el "Modelo de objetos componentes" en [http://go.microsoft.com/fwlink/?LinkId=20922](http://go.microsoft.com/fwlink/?linkid=20922). Para obtener más información acerca de las nuevas características de seguridad de DCOM, consulte "DCOM: Restricciones de acceso al equipo en el lenguaje de definición de descriptores de seguridad (SDDL)" en el capítulo 5 de esta guía.
  
Puede administrar las nuevas características de seguridad de DCOM en Windows XP SP2 y Windows Server 2003 SP1 en la ubicación siguiente dentro del Editor de objetos de directiva de grupo:
  
**Configuración del equipo\\Plantillas administrativas\\Componentes de Windows**  
**Sistema\\COM Distribuido\\Configuración de compatibilidad de aplicaciones**
  
##### Problemas comunes
  
Las dos configuraciones en esta sección comparten información de vulnerabilidad, contramedidas y posibles repercusiones.
  
###### Vulnerabilidad
  
Los componentes COM mal escritos pueden ser objeto de ataques en la red, lo que puede tener como resultado la divulgación de información, la denegación de servicio o ataques de escalado de privilegios.
  
###### Contramedida
  
Utilice los parámetros **Permitir exenciones de comprobación de seguridad de activación local** y **Definir exenciones de comprobación de seguridad de activación** junto con los mecanismos de control del acceso DCOM que se describen en el capítulo 5 para imponer controles de acceso y ejecución sobre los componentes DCOM.
  
###### Impacto potencial
  
Si agrega controles de acceso DCOM a aplicaciones existentes, es posible que estas aplicaciones no se ejecuten correctamente.
  
##### Permitir exenciones de comprobación de seguridad de activación local
  
Esta configuración de directiva le permite especificar que los administradores de equipos locales pueden complementar la lista **Definir exenciones de comprobación de seguridad de activación** (ver el siguiente parámetro) con comprobaciones de seguridad de activación que ocurren en el equipo local. Si habilita esta configuración de directiva y DCOM no encuentra una entrada explícita para un identificador de aplicación de servidor DCOM (AppID) en la directiva Definir exenciones de comprobación de seguridad de activación, DCOM busca una entrada en la lista configurada de forma local.
  
##### Definir exenciones de comprobación de seguridad de activación
  
Esta configuración de directiva le permite ver y cambiar una lista de identificadores de aplicación de servidor DCOM (AppID) exentos de la comprobación de seguridad de activación DCOM. (Para obtener más información acerca de COM y la clave AppID, consulte “[COM Registry Entries](http://go.microsoft.com/fwlink/?linkid=32831)” en la Documentación COM de SDK en MSDN® en http://go.microsoft.com/fwlink/?LinkId=32831.)
  
DCOM utiliza dos listas de AppID de servidor DCOM para tomar las decisiones de seguridad. Una lista se configura a través de la configuración de directiva de grupo **Definir exenciones de comprobación de seguridad de activación** y la otra la crean los administradores de equipos locales. La clave AppID es una de las claves del Registro que usa COM; agrupa las opciones de configuración para uno o más objetos COM distribuidos en una ubicación centralizada en el Registro. Esta clave incluye el valor denominado AppID, que identifica el GUID de AppID que corresponde al archivo ejecutable denominado.
  
Si configura el parámetro **Definir exenciones de comprobación de seguridad de activación**, DCOM omite la segunda lista a menos que el parámetro asociado **Permitir exenciones de comprobación de seguridad de activación local** se habilite también. Debe encerrar cualquier AppID de servidor DCOM que agregue a la lista de AppID de servidor DCOM entre llaves; por ejemplo, {b5dcb061-cefb-42e0-a1be-e6a6438133fe}. (Este número de AppID es sólo un ejemplo). Si introduce un AppID inexistente o con formato incorrecto, DCOM lo agrega a la lista; no comprueba si hay errores.
  
Si habilita esta configuración de directiva, puede ver y cambiar la lista de exenciones de comprobación de seguridad de activación DCOM definidas en la configuración de Directiva de grupo.
  
Puede utilizar uno de los valores siguientes:
  
-   Si agrega un AppID a esta lista y establece su valor en **1**, DCOM no implanta la comprobación de seguridad de activación para ese servidor DCOM.
  
-   Si agrega un AppID a esta lista y establece su valor en **0**, DCOM siempre implanta la comprobación de seguridad de activación para ese servidor DCOM, independientemente de la configuración local.
  
**Nota**: los servidores DCOM que se agregan a esta lista de exenciones sólo se eximen si sus permisos personalizados de ejecución no contienen permisos específicos de inicio local, inicio remoto, activación local o activación remota establecidos en permitir o denegar para cualquier usuario o grupo. Las exenciones para AppID de servidor DCOM que agregue a esta lista se aplican a la versión de 32 bits y (si está presente) a la versión de 64 bits de Windows Server 2003.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Parámetros de Configuración de usuario
  
La configuración que ya se mencionó en este capítulo se aplica a equipos que son miembros de un dominio de Active Directory. La configuración en las secciones siguientes se aplica a usuarios individuales.
  
#### Configuración de usuario de Internet Explorer
  
Internet Explorer es el explorador web que se distribuye con Windows XP y Windows Server 2003. Puede administrar varias de sus características a través de la Directiva de grupo en la ubicación siguiente dentro del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\**  
**Internet Explorer**
  
##### Configurar Outlook Express
  
Esta configuración de directiva permite a los administradores habilitar y deshabilitar la capacidad de los usuarios de Microsoft Outlook® Express para guardar o abrir datos adjuntos que puedan contener virus. Si activa la casilla de verificación **Bloquear datos adjuntos que puedan contener virus**,los usuarios no podrán abrir o guardar datos adjuntos que pudieran contener virus. Asimismo, si habilita esta configuración de directiva, los usuarios podrán especificar si desean bloquear o aceptar los datos adjuntos del correo en el cuadro de diálogo **Opciones de Internet**.
  
Los valores posibles para la configuración **Configurar Outlook Express** son:
  
-   Habilitado, en el que se incluye la siguiente opción:
  
    -   Bloquear datos adjuntos que puedan contener virus
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los usuarios que decidan abrir los archivos adjuntos del correo electrónico podrían ejecutar, sin darse cuenta, código hostil, como un virus o un troyano.
  
###### Contramedida
  
Establezca **Configurar Outlook Express** en **Habilitado** y active la casilla de verificación **Bloquear datos adjuntos que puedan contener virus**.
  
###### Impacto potencial
  
Los usuarios no podrán abrir o ejecutar algunos tipos de datos adjuntos de mensajes en Outlook Express.
  
##### Deshabilitar la configuración de página de Opciones avanzadas
  
Esta configuración de directiva evita cambios del usuario a la configuración en la ficha **Opciones avanzadas** del cuadro de diálogo **Opciones de Internet.** Si habilita esta configuración de directiva, los usuarios no podrán cambiar la configuración avanzada de Internet, como las opciones de seguridad, multimedia e impresión, y no podrán seleccionar ni cancelar la selección de casillas de verificación en la ficha **Opciones avanzadas.** Si deshabilita o no establece esta configuración de directiva, los usuarios podrán seleccionar o cancelar la selección de opciones en la ficha **Opciones avanzadas**.
  
Si configura el parámetro **Deshabilitar la página Opciones avanzadas**, no necesita establecer esta configuración de directiva, porque ese parámetro elimina la ficha **Opciones avanzadas** de la interfaz.
  
Los valores posibles para la configuración **Deshabilitar la configuración de página de Opciones avanzadas** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los usuarios podrían cambiar parcialmente la configuración de seguridad de Internet Explorer, lo que les permitiría visitar un sitio web malintencionado y descargar o ejecutar código hostil.
  
###### Contramedida
  
Establezca **Deshabilitar la configuración de página de Opciones avanzadas** en **Habilitado**.
  
###### Impacto potencial
  
Los usuarios no podrán cambiar la configuración de la ficha **Opciones avanzadas** del cuadro de diálogo **Opciones de Internet**.
  
##### Deshabilitar cambio de valores de Configuración auto.
  
Esta configuración de directiva evita cambios del usuario a los valores de configuración automática. La configuración automática es un proceso que pueden utilizar los administradores para actualizar la configuración del explorador de forma periódica. Si habilita esta configuración de directiva, los valores de configuración automática aparecerán atenuados y no estarán disponibles. Estos valores se ubican en la sección **Configuración automática** del cuadro de diálogo **Configuración de la red de área local (LAN)**. Si deshabilita o no establece esta configuración de directiva, los usuarios podrán cambiar los valores de configuración automática.
  
Si habilita el parámetro **Deshabilitar la página Conexiones**, la ficha **Conexiones** se elimina de Internet Explorer en el Panel de control y su configuración anula esta configuración de directiva (**Deshabilitar cambio de valores de Configuración automática**).
  
Los valores posibles para la configuración **Deshabilitar cambio de valores de configuración automática** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los usuarios podrían cambiar parcialmente la configuración de seguridad de Internet Explorer, lo que les permitiría visitar un sitio web malintencionado y descargar o ejecutar código hostil.
  
###### Contramedida
  
Establezca **Deshabilitar cambio de valores de Configuración automática** como **Habilitado**.
  
###### Impacto potencial
  
Los usuarios no podrán cambiar los valores de configuración automática.
  
##### Deshabilitar cambio de config. de certificados
  
Esta configuración de directiva evita cambios del usuario en la configuración de los certificados en Internet Explorer. Los certificados se utilizan para comprobar la identidad de los fabricantes de software. Si habilita esta configuración de directiva, se atenuarán y dejarán de estar disponibles los valores de la sección **Certificados** de la ficha **Contenido** del cuadro de diálogo **Opciones de Internet.** Si la deshabilita o no la configura, los usuarios podrán importar nuevos certificados, quitar fabricantes aprobados y cambiar la configuración de certificados que ya se han aceptado.
  
El parámetro **Deshabilitar la página Contenido** (ubicado en **\\Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control de Internet**), que quita la ficha **Contenido** de Internet Explorer en el Panel de control, éste tendrá prioridad con respecto a esta configuración de directiva (**Deshabilitar cambio de config. de certificados**).
  
Los valores posibles para la configuración **Deshabilitar cambio de config. de certificados** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
**Advertencia**: si habilita esta configuración de directiva, los usuarios pueden hacer doble clic en un archivo de certificados (.spc) y ejecutar el Asistente para importación de Administrador de certificados. Este asistente permite a los usuarios importar y configurar propiedades para los certificados de los fabricantes de software que aún no se han configurado en Internet Explorer.
  
###### Vulnerabilidad
  
Los usuarios podrían importar nuevos certificados, quitar certificados aprobados o cambiar los valores de aquellos que ya se han configurado. Tales ocurrencias podrían provocar errores en las aplicaciones aprobadas o que se ejecute software sin aprobación.
  
###### Contramedida
  
Establezca **Deshabilitar cambio de config. de certificados** en **Habilitado.**
  
###### Impacto potencial
  
Los usuarios no podrán cambiar la configuración de los certificados.
  
##### Deshabilitar cambio de configuración de conexión
  
Esta configuración de directiva evita cambios del usuario a las propiedades de acceso telefónico. Si habilita esta configuración de directiva, se atenuará el botón **Configuración** de la ficha **Conexiones** del cuadro de diálogo **Opciones de Internet**. Si deshabilita o no establece esta configuración de directiva, los usuarios podrán cambiar su configuración para conexiones de marcado.
  
Si habilita la configuración **Deshabilitar la página Conexiones** (que se encuentra en \\**Configuración de usuario\\**  
**Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control de Internet**) la ficha **Conexiones** se elimina del cuadro de diálogo **Opciones de Internet** y no hay necesidad de configurar esta configuración de directiva (**Deshabilitar cambio de configuración de conexión**).
  
Los valores posibles para la configuración **Deshabilitar cambio de configuración de conexión** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los usuarios podrían modificar las conexiones existentes e impedir el uso de Internet Explorer para explorar algunos o todos los sitios web.
  
###### Contramedida
  
Configure **Deshabilitar cambio de configuración de conexión** en **Habilitado.**
  
###### Impacto potencial
  
Los usuarios no podrán cambiar la configuración de la conexión.
  
##### Deshabilitar el cambio de configuración de proxy
  
Esta configuración de directiva evita cambios del usuario a la configuración de proxy. Si habilita esta configuración de directiva, los valores de Configuración de proxy estarán atenuados y no disponibles. Se ubica en la sección **Servidor proxy** del cuadro de diálogo **Configuración de la red de área local (LAN)**, que aparece cuando el usuario hace clic en la ficha **Conexiones** y, a continuación, en el botón **Configuración LAN** del cuadro de diálogo **Opciones de Internet**.
  
Si establece el parámetro **Deshabilitar la página conexiones** (ubicado en **\\Configuración de usuario\\**  
**Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control de Internet**), no necesita configurar esta configuración de directiva (**Deshabilitar el cambio de configuración de proxy**), ya que el parámetro **Deshabilitar la página Conexiones**, elimina la ficha **Conexiones** del cuadro de diálogo **Opciones de Internet**.
  
Los valores posibles para la configuración **Deshabilitar el cambio de configuración de proxy** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los usuarios podrían modificar la configuración de servidor proxy existente e impedir el uso de Internet Explorer para explorar algunos o todos los sitios web.
  
###### Contramedida
  
Establezca **Deshabilitar el cambio de configuración de proxy** en **Habilitado.**
  
###### Impacto potencial
  
Los usuarios no podrán cambiar la configuración de proxy.
  
##### Deshabilitar Asistente para la conexión a Internet
  
Esta configuración de directiva controla la capacidad de usuarios para ejecutar el Asistente para la conexión a Internet (ICW). Si habilita este parámetro, se atenuará el botón **Configuración** de la ficha **Conexiones** del cuadro de diálogo **Opciones de Internet**. Esta configuración de directiva evita también la ejecución del asistente en otras maneras; por ejemplo, los usuarios no serán capaces de hacer clic en el icono **Conectarse a Internet** en el escritorio o seleccionar **Inicio**, **Programas**, **Accesorios**, **Comunicaciones** y, a continuación, **Asistente para la conexión a Internet**. Si deshabilita o no establece esta configuración de directiva, los usuarios podrán cambiar su configuración de la conexión por medio del ICW.
  
Los valores posibles para la configuración **Deshabilitar Asistente para la conexión a Internet** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
**Nota**: esta configuración de directiva se solapa con el valor **Deshabilitar la página Conexiones** (ubicado en **\\Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet**), que quita la ficha **Conexiones** del cuadro de diálogo **Opciones de Internet**. Sin embargo, si utiliza este parámetro, los usuarios podrán seguir ejecutando el ICW desde el escritorio o el menú de **Inicio**.
  
###### Vulnerabilidad
  
Los usuarios podrían ejecutar el Asistente para la conexión a Internet para crear una nueva conexión de red o de acceso telefónico, lo que permitiría a usuarios no autorizados obtener acceso a la red de la organización a través de una nueva conexión no administrada.
  
###### Contramedida
  
Establezca **Deshabilitar Asistente para la conexión a Internet** en **Habilitado**.
  
###### Impacto potencial
  
Los usuarios no podrán utilizar el Asistente para la conexión a Internet.
  
##### No permitir que Autocompletar guarde las contraseñas
  
Esta configuración de directiva deshabilita el autocompletado de los nombres de usuario y contraseñas en formularios de páginas web y evita que se muestre a los usuarios la pantalla para "guardar contraseña". Si habilita esta configuración de directiva, se atenuarán y dejarán de estar disponibles las casillas de verificación **Nombres de usuario y contraseñas en formularios** y **Preguntar si se guardan las contraseñas**. (Para mostrar estas casillas, los usuarios pueden abrir el cuadro de diálogo **Opciones de Internet**, hacer clic en la ficha **Contenido** y, a continuación, en el botón **Autocompletar**). Si deshabilita o no configura este parámetro, los usuarios pueden determinar si Internet Explorer completa automáticamente los nombres de usuario y contraseñas en formularios y les pedirá que guarden las contraseñas.
  
Si habilita el valor **Deshabilitar la página Contenido** (en **\\Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Panel de control Internet**), la ficha **Contenido** de Internet Explorer ya no estará disponible en el Panel de control y éste tendrá prioridad sobre esta configuración de directiva (**No permitir que Autocompletar guarde las contraseñas**).
  
Los valores posibles para la configuración **No permitir que Autocompletar guarde las contraseñas** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Aunque la característica Autocompletar resulta muy útil, carga las contraseñas en Almacenamiento protegido. Este último mecanismo es muy seguro, la información almacenada en el mismo debe ser accesible para el usuario que la guardó. En Internet se han distribuido diversas herramientas que permiten ver el contenido del almacenamiento protegido de un usuario. Estas herramientas sólo funcionan cuando las ejecuta un usuario para ver su almacenamiento protegido; no se pueden utilizar para consultar la contraseña o el almacenamiento protegido de ningún otro usuario. Si un usuario ejecuta una de ellas sin darse cuenta, podría exponer su contraseña a posibles atacantes.
  
###### Contramedida
  
Establezca **No permitir que Autocompletar guarde las contraseñas** en **Habilitado**.
  
###### Impacto potencial
  
Los usuarios no podrán utilizar la característica Autocompletar para guardar las contraseñas.
  
#### Panel de control Internet
  
Puede administrar configuraciones relacionadas con Internet a través del subprograma del Panel de control Internet. La disponibilidad de las características del subprograma se puede controlar a través del nodo Panel de control Internet en la Directiva de grupo. Estas configuraciones de directiva se pueden establecer en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\**  
**Internet Explorer\\Panel de control Internet**
  
##### Deshabilitar la página Opciones avanzadas
  
Esta configuración de directiva quita la ficha **Opciones avanzadas** del cuadro de diálogo **Opciones de Internet**. Si habilita esta configuración de directiva, evitará que los usuarios vean y modifiquen la configuración avanzada de Internet, por ejemplo, las opciones de impresión, multimedia y seguridad. Si deshabilita o no establece esta configuración de directiva, los usuarios podrán ver y cambiar estas configuraciones.
  
Si habilita esta configuración de directiva, se quitará la ficha **Opciones avanzadas** del cuadro de diálogo **Opciones de Internet**. Por lo tanto, ya no será necesario habilitar el valor **Deshabilitar la configuración de la página de Opciones avanzadas** (en **\\Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\**).
  
Los valores posibles para la configuración **Deshabilitar la página Opciones avanzadas** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los usuarios podrían cambiar parcialmente la configuración de seguridad de Internet Explorer, lo que les permitiría visitar un sitio web malintencionado y descargar o ejecutar código hostil.
  
###### Contramedida
  
Configure el parámetro **Deshabilitar la página Opciones avanzadas** en **Habilitado**.
  
###### Impacto potencial
  
Los usuarios no podrán ver el cuadro de diálogo **Opciones avanzadas**.
  
##### Deshabilitar la página Seguridad
  
Esta configuración de directiva quita la ficha **Seguridad** del cuadro de diálogo **Opciones de Internet**. Si habilita este parámetro, los usuarios no podrán ver o cambiar la configuración de las zonas de seguridad, como las secuencias de comandos, las descargas y la autenticación de usuario. Si deshabilita o no establece esta configuración, los usuarios podrán ver y cambiar estas configuraciones.
  
Los valores posibles para la configuración **Deshabilitar la página Seguridad** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
Cuando configura este parámetro, usted no necesita configurar los siguientes parámetros de Internet Explorer (porque la etiqueta Seguridad se elimina del cuadro de diálogo **Opciones de Internet**):
  
-   Zonas de seguridad: **no permitir que los usuarios cambien las directivas**
  
-   Zonas de seguridad: **no permitir que los usuarios agreguen o eliminen sitios**
  
###### Vulnerabilidad
  
Los usuarios podrían cambiar parcialmente la configuración de seguridad de Internet Explorer, lo que les permitiría visitar un sitio web malintencionado y descargar o ejecutar código hostil.
  
###### Contramedida
  
Configure el parámetro **Deshabilitar la página Seguridad** en **Habilitado**.
  
###### Impacto potencial
  
Los usuarios no podrán ver la página Seguridad.
  
#### Páginas sin conexión
  
Internet Explorer puede descargar y guardar en caché páginas para utilizarlas cuando los usuarios no estén conectados. Esta característica se puede controlar a través del nodo Páginas sin conexión en la Directiva de grupo. Estas configuraciones de directiva se pueden establecer en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer\\Páginas sin conexión**
  
##### Deshabilitar la posibilidad de agregar canales
  
Esta configuración de directiva puede eliminar la capacidad de los usuarios para agregar canales a Internet Explorer. Los canales son sitios web que se actualizan automáticamente en el equipo, de acuerdo con una programación especificada por el proveedor de canal.
  
Si habilita esta política de directiva, dejará de estar disponible el botón **Agregar Active Channel** en el que los usuarios deben hacer clic para suscribirse a los canales. Asimismo, los usuarios tampoco podrán agregar contenido basado en un canal; por ejemplo, no podrán agregar a su escritorio algunos de los elementos de Active Desktop®; desde la galería de Active Desktop de Microsoft. Si usted deshabilita o no configura este parámetro, los usuarios pueden agregar canales a la barra de canales o a su escritorio.
  
Los posibles valores para el parámetro **Deshabilitar la posibilidad de agregar canales** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Se podrían enviar datos al explorador de un usuario sin la interacción directa de éste. Es decir, el explorador podría descargar contenido web que no hubiera sido solicitado directamente por el usuario.
  
###### Contramedida
  
Configure el parámetro **Deshabilitar la posibilidad de agregar canales** en **Habilitado.**
  
###### Impacto potencial
  
Los usuarios no podrán agregar canales.
  
##### Deshabilitar la posibilidad de agregar programaciones para las páginas sin conexión
  
Esta configuración de directiva está dirigida a aquellas organizaciones a las que preocupa la carga del servidor. Puede utilizarlo para controlar la capacidad de los usuarios para especificar qué páginas web se pueden descargar y ver sin conexión cuando su equipo no está conectado al Internet.
  
Si habilita esta configuración de directiva, evitará que los usuarios agreguen nuevas programaciones para la descarga de contenido sin conexión. La casilla de verificación **Disponible sin conexión** del cuadro de diálogo **Agregar a Favoritos** se atenuará y dejará de estar disponible. Si deshabilita o no establece esta configuración de directiva, los usuarios podrán agregar nuevos programas de contenido desconectados. El parámetro **Menú Ocultar favoritos** (ubicado en **Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer**) tiene prioridad sobre esta configuración de directiva.
  
Los posibles valores para el parámetro **Deshabilitar la posibilidad de agregar canales** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Se podrían enviar datos al explorador de un usuario sin la interacción directa de éste. Es decir, el explorador podría descargar contenido web que no hubiera sido solicitado directamente por el usuario.
  
###### Contramedida
  
Configurar el parámetro **Deshabilitar la posibilidad de agregar programaciones para las páginas sin conexión** en **Habilitado**.
  
###### Impacto potencial
  
Los usuarios no podrán agregar programaciones para las páginas sin conexión.
  
##### Deshabilitar todas las páginas sin conexión programadas
  
Esta configuración de directiva está dirigida a aquellas organizaciones a las que preocupa la carga del servidor. Puede utilizarla para deshabilitar las programaciones que existen actualmente para descargar páginas web y que puedan ser vistas sin conexión. Cuando los usuarios hacen que las páginas web estén disponibles para verlas sin conexión, pueden consultar las páginas cuando su equipo no esté conectado a Internet.
  
Si habilita esta configuración de directiva, las casillas de verificación para la programación de la ficha **Programación** del cuadro de diálogo **Propiedades de la página web** se borran y los usuarios no pueden seleccionarlas. (Para mostrar esta ficha, los usuarios tienen que hacer clic en el menú **Herramientas** y luego en **Sincronizar**, seleccionar una página web, hacer clic en **Propiedades** y después en la ficha **Programación**.) Si deshabilita esta configuración de directiva, las páginas web se pueden actualizar según los horarios que se especifican en la ficha **Programación.** El parámetro Menú **Ocultar favoritos** (ubicado en **Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer**) tiene prioridad sobre esta configuración.
  
Los posibles valores para el parámetro **Deshabilitar la posibilidad de agregar canales** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Se podrían enviar datos al explorador de un usuario sin la interacción directa de éste. Es decir, el explorador podría descargar contenido web que no hubiera sido solicitado directamente por el usuario.
  
###### Contramedida
  
Configurar el parámetro **Deshabilitar todas las páginas sin conexión programadas** en **Habilitado**.
  
###### Impacto potencial
  
Los usuarios no podrán ver las páginas sin conexión programadas.
  
##### Deshabilita totalmente la interfaz de usuario del canal
  
Esta configuración de directiva determina si los usuarios pueden ver la interfaz de la Barra de canales. Los canales son sitios web que se actualizan automáticamente en el equipo, de acuerdo con una programación especificada por el proveedor de canal.
  
Si habilita esta configuración de directiva, se deshabilitará la interfaz de usuario (IU) de la **Barra de canales** y los usuarios no podrán activar la casilla de verificación **Barra de canales de Internet Explorer** en la ficha **web** del cuadro de diálogo Propiedades de Pantalla. Si deshabilita o no establece esta configuración, los usuarios podrán ver y suscribirse a canales a través de la interfaz de la Barra de canales.
  
Los valores posibles para la configuración **Deshabilita totalmente la interfaz de usuario del canal** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Se podrían enviar datos al explorador de un usuario sin la interacción directa de éste. Es decir, el explorador podría descargar contenido web que no hubiera sido solicitado directamente por el usuario.
  
###### Contramedida
  
Configurar el parámetro **Deshabilita totalmente la interfaz de usuario del canal** en **Habilitado**.
  
###### Impacto potencial
  
Los usuarios no podrán obtener acceso a la IU de la Barra de canales.
  
##### Deshabilita la descarga del contenido de las suscripciones a sitios
  
Esta configuración de directiva controla si los usuarios pueden descargar contenido de los sitios web a los que se suscriben. Esta capacidad permite a los usuarios ver páginas web cuando están desconectados (cuando su equipo no está conectado a Internet).
  
Si habilita esta configuración de directiva, los usuarios no podrán descargar contenido de los sitios web a los que se suscriban. No obstante, se seguirá produciendo la sincronización con las páginas web para determinar si se ha actualizado su contenido desde la última vez que el usuario las visitó o las sincronizó. Si deshabilita o no establece esta configuración de directiva, los usuarios podrán descargar contenido.
  
Los valores de configuración **Deshabilita la descarga del contenido de las suscripciones a sitios** y **Menú Ocultar favoritos** (ubicado en Configuración de **usuario\\Plantillas administrativas\\Componentes de Windows\\**  
**Internet Explorer**) anulan esta configuración de directiva.
  
Los valores posibles para el parámetro **Deshabilita la descarga del contenido de las suscripciones a sitios** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Se podrían enviar datos al explorador de un usuario sin la interacción directa de éste. Es decir, el explorador podría descargar contenido web que no hubiera sido solicitado directamente por el usuario.
  
###### Contramedida
  
Configure el parámetro **Deshabilita la descarga del contenido de las suscripciones a sitios** en **Habilitado**.
  
###### Impacto potencial
  
Los usuarios no podrán descargar contenido automáticamente a través de las suscripciones a sitios.
  
##### Deshabilitar la edición y creación de grupos de programaciones
  
Esta configuración de directiva controla si los usuarios pueden agregar, editar o eliminar programaciones para descargar contenido, de modo que las páginas web y los grupos de páginas web a los que los usuarios se suscriban puedan ser vistos sin conexión. Un grupo de suscripción está formado por una página web favorita y las páginas web a las que está vinculada.
  
Si activa esta directiva, se atenuarán y dejarán de estar disponibles los botones **Agregar**, **Quitar** y **Editar** de la ficha **Programación** del cuadro de diálogo de **Propiedades** de la página web. (Para mostrar esta ficha, los usuarios tienen que hacer clic en el menú **Herramientas** y luego en **Sincronizar**, seleccionar una página web, hacer clic en el botón **Propiedades** y después en la ficha **Programación**.) Si deshabilita o no configura este parámetro, los usuarios podrán agregar, eliminar y editar programaciones para sitios web y grupos de sitios web.
  
Los valores de configuración **Deshabilitar la edición de programaciones para páginas sin conexión** y **Menú Ocultar favoritos** (ubicado en Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer) anulan esta directiva.
  
Los valores posibles para la configuración **Deshabilitar la edición y creación de grupos de programaciones** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Se podrían enviar datos al explorador de un usuario sin la interacción directa de éste. Es decir, el explorador podría descargar contenido web que no hubiera sido solicitado directamente por el usuario.
  
###### Contramedida
  
Configure el parámetro **Deshabilitar la edición y creación de grupos de programaciones** en **Habilitado**.
  
###### Impacto potencial
  
Los usuarios no podrán agregar, editar o quitar programaciones para descargar el contenido de la página web para que se pueda ver desconectado.
  
##### Deshabilitar la edición de programaciones para páginas sin conexión
  
Esta configuración de directiva está dirigida a aquellas organizaciones a las que preocupa la carga del servidor. Controla si los usuarios pueden modificar las programaciones que ya existen para descargar páginas web para que puedan verse desconectadas (cuando el equipo no esté conectado al Internet).
  
Si habilita esta configuración de directiva, los usuarios no podrán mostrar las propiedades de la programación de páginas que estén configuradas para ser vistas sin conexión. Si los usuarios hacen clic en el menú **Herramientas**, **Sincronizar**, seleccionan una página web y hacen clic en el botón **Propiedades**, no se mostrará ninguna propiedad. No se muestra ninguna alerta que indique que la opción no está disponible. Si deshabilita o no establece esta configuración de directiva, los usuarios podrán editar las programaciones existentes para descargar contenido web para que se pueda verse sin conexión.
  
El parámetro **Menú Ocultar favoritos** (ubicado en **Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer**) tiene prioridad sobre esta configuración de directiva.
  
Los valores posibles para la configuración **Deshabilitar la edición de programaciones para páginas sin conexión** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Se podrían enviar datos al explorador de un usuario sin la interacción directa de éste. Es decir, el explorador podría descargar contenido web que no hubiera sido solicitado directamente por el usuario.
  
###### Contramedida
  
Configure el parámetro **Deshabilitar la posibilidad de editar programaciones para las páginas sin conexión** en **Habilitado**.
  
###### Impacto potencial
  
Los usuarios no podrán editar programaciones para controlar cuándo se podrá descargar el contenido de páginas web para que se pueda ver desconectado.
  
##### Deshabilitar la cuenta de visitas a la página sin conexión
  
Esta configuración de directiva controla si los proveedores de canales podrán registrar cada visita que hagan a sus páginas los usuarios que trabajan sin conexión.
  
Si habilita esta configuración de directiva, se deshabilitarán los valores del registro de canales configurados por los proveedores de canal en el archivo de formato de definición de canales (.cdf). Este archivo determina la programación y otros valores de configuración de la descarga de contenido web. Si deshabilita o no configura esta configuración de directiva si los proveedores de canal los proveedores de canal podrán registrar cada visita que hagan a sus páginas los usuarios que trabajan sin conexión.
  
Los valores posibles para la configuración **Deshabilitar la cuenta de visitas a la página sin conexión** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Se podrían enviar datos al explorador de un usuario sin la interacción directa de éste. Es decir, el explorador podría descargar contenido web que no hubiera sido solicitado directamente por el usuario.
  
###### Contramedida
  
Configurar el parámetro **Deshabilitar la cuenta de visitas a la página sin conexión** en **Habilitado**.
  
###### Impacto potencial
  
Las visitas que realicen los usuarios a páginas sin conexión no se reenviarán al sitio web la próxima vez que trabajen conectados.
  
##### Deshabilitar la posibilidad de quitar canales
  
Con esta directiva se pretende ayudar a los administradores a garantizar la actualización uniforme de los equipos de los usuarios de toda la organización. Controla si usuarios pueden deshabilitar la sincronización de canales en Internet Explorer. Los canales son sitios web que se actualizan automáticamente en el equipo, de acuerdo con una programación especificada por el proveedor de canal.
  
Si habilita esta configuración de directiva, los usuarios no pueden intervenir con sincronización de canal. Si deshabilita o no establece esta configuración de directiva, los usuarios podrán deshabilitar este proceso.
  
Los posibles valores para el parámetro **Deshabilitar la posibilidad de eliminar canales** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
**Nota**: esta configuración de directiva no impide que los usuarios puedan eliminar contenido activo de la interfaz de escritorio.
  
###### Vulnerabilidad
  
Se podrían enviar datos al explorador de un usuario sin la interacción directa de éste. Es decir, el explorador podría descargar contenido web que no hubiera sido solicitado directamente por el usuario.
  
###### Contramedida
  
Configure el parámetro **Deshabilitar la posibilidad de eliminar canales** en **Habilitado.**
  
###### Impacto potencial
  
Los usuarios no podrán quitar canales ni deshabilitar su sincronización.
  
##### Deshabilitar la eliminación de programaciones para páginas sin conexión
  
Esta configuración de directiva está dirigida a aquellas organizaciones a las que preocupa la carga del servidor. Controla si los usuarios pueden eliminar restricciones preconfiguradas impuestas sobre la descarga de páginas web para que puedan verse desconectadas (cuando el equipo no esté conectado al Internet).
  
Si habilita esta configuración de directiva, las casillas de verificación **Disponible sin conexión** del cuadro de diálogo **Organizar Favoritos** y **Página disponible sin conexión** se atenuarán estando activadas y dejarán de estar disponibles (aunque permanezcan seleccionadas). (Para mostrar la casilla **Página disponible sin conexión** los usuarios deben hacer clic en **Herramientas**, **Sincronizar** y a continuación, **Propiedades**). Si usted deshabilita o no establece esta configuración de directiva, los usuarios pueden eliminar las restricciones preconfiguradas de las páginas para descargarlas de modo que puedan ser vistas sin conexión.
  
El parámetro Menú **Ocultar favoritos** (ubicado en Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\Internet Explorer) tiene prioridad sobre esta configuración.
  
Los valores posibles para la configuración **Deshabilitar la eliminación de programaciones para páginas sin conexión** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Se podrían enviar datos al explorador de un usuario sin la interacción directa de éste. Es decir, el explorador podría descargar contenido web que no hubiera sido solicitado directamente por el usuario.
  
###### Contramedida
  
Configure el parámetro **Deshabilitar la posibilidad de agregar programaciones para las páginas sin conexión** en **Habilitado**.
  
###### Impacto potencial
  
Los usuarios no podrán quitar programaciones para las páginas sin conexión.
  
#### Menús del explorador
  
Las características individuales en el sistema de menús de Internet Explorer pueden habilitarse y deshabilitarse a través del nodo Menús del explorador en la Directiva de grupo. Estas configuraciones de directiva se pueden establecer en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\**  
**Internet Explorer\\Menús del explorador**
  
##### Deshabilitar la opción Guardar este programa en disco
  
Si habilita esta configuración de directiva, evitará que los usuarios hagan clic en el botón **Guardar este programa en disco** para descargar archivos de programas. Se informará a los usuarios que el comando no está disponible. Si deshabilita o no establece esta configuración, los usuarios podrán descargar los programas de sus exploradores.
  
Los valores posibles para la configuración de **Menús del explorador: Deshabilitar la opción Guardar este programa en disco** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los usuarios podrían descargar y ejecutar código hostil desde los sitios web.
  
###### Contramedida
  
Configure el parámetro **Deshabilitar la opción Guardar este programa en disco** en **Habilitado**.
  
###### Impacto potencial
  
Evitará que los usuarios hagan clic en el botón **Guardar este programa en disco** para descargar archivos de programas.
  
##### Comportamiento de persistencia
  
Internet Explorer permite que objetos dinámicos HTML (DHTML) guarden sus parámetros o datos en disco; esto se denomina *persistencia.* Los datos de formularios, estilos, estado y variables de secuencia de comandos se pueden persistir en la sesión actual de la memoria, en la lista de favoritos, en HTML o XML. Los cuatro comportamientos de persistencia DHTML son saveFavorite, saveHistory, saveSnapshot y userData. Internet Explorer le permite aplicar controles por zona de seguridad a la cantidad de datos que las aplicaciones pueden guardar utilizando este mecanismo.
  
Los valores posibles para la configuración **Comportamiento de persistencia** son:
  
-   Habilitado
  
    -   **Por dominio (en kilobytes).** Esta configuración controla la forma en que los datos totales pueden guardarse por secuencias de comandos que se asocian con un dominio dado.
  
    -   **Por documento (en kilobytes).** Esta configuración controla la forma en que los datos totales pueden guardarse por construcciones DHTML en una página web específica.
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Una página web malintencionada puede guardar secretamente los datos malintencionados o cantidades excesivas de datos, en un equipo de destino.
  
###### Contramedida
  
Habilite límites de tamaño por zona de seguridad para las zonas de Internet y de sitios restringidos.
  
###### Impacto potencial
  
Ninguno.
  
#### Administrador de datos adjuntos
  
En Windows Server 2003 SP1 y Windows XP SP2, un servicio nuevo llamado Administrador de datos adjuntos proporciona un conjunto coherente de comportamientos para datos adjuntos de archivos en mensajes de correo electrónico y páginas web. El servicio del Administrador de datos adjuntos implementa un conjunto uniforme de avisos que se utilizan para descargas de archivos, datos adjuntos de correo, ejecución de proceso shell y la instalación del programa. Estos avisos se han modificado para que sean más claros y más coherentes que en versiones anteriores de Windows. Además, la información del editor se mostrará ante un tipo de archivo que pueda firmarse y que podría dañar posiblemente el equipo del usuario si se abre. (Ejemplos comunes de archivos que pueden firmarse y que pueden dañar su equipo son .exe, .dll, .ocx, .msi y .cab). El servicio del Administrador de datos adjuntos incluye una interfaz de programación de aplicaciones (API) que permite que los desarrolladores de aplicaciones hagan uso de esta nueva interfaz de usuario.
  
El servicio del Administrador de datos adjuntos clasifica los archivos que usted recibe o descarga, basado en el tipo de archivo y la extensión del nombre de archivo. El servicio clasifica los archivos como de riesgo alto, medio y bajo. Cuando guarda archivos en su disco duro, desde un programa que utilice el servicio de Administrador de datos adjuntos, la información de zona del contenido web del archivo se guarda también con éste. Por ejemplo, si guardó un archivo comprimido (.zip) adjunto a un mensaje de correo electrónico, la información de la zona de contenido web también se habrá guardado y no podrá extraer el contenido a partir del archivo comprimido.
  
**Nota**: la información de zona del contenido web se guarda junto con los archivos sólo si el equipo utiliza el sistema de archivos de NTFS.
  
El servicio del Administrador de datos adjuntos divide los archivos en tres clases:
  
-   **Alto riesgo**. Si el archivo adjunto está en la lista de tipos de archivo de alto riesgo y es de la zona restringida, Windows bloquea el acceso al usuario antes de permitir el acceso al archivo. Si el archivo es de la zona de Internet, Windows pide confirmación al usuario antes de permitir el acceso al archivo.  
  
-   **Riesgo moderado.** Si el archivo adjunto está en la lista de tipos de archivo de riesgo moderado y es de la zona restringida o de Internet, Windows pide confirmación al usuario antes de permitir el acceso al archivo.  
  
-   **Bajo riesgo.** Si el archivo adjunto está en la lista de tipos de archivo de bajo riesgo, Windows no pedirá confirmación al usuario antes de permitir el acceso al archivo, independientemente de la información de la zona del archivo.
  
Estas configuraciones de directiva se pueden establecer en la siguiente ubicación del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\**  
**Administrador de datos adjuntos**
  
##### Nivel de riesgo predeterminado de los datos adjuntos de archivos
  
Esta configuración de directiva le permite administrar el nivel de riesgo para los tipos de archivo. Para personalizar completamente el nivel de riesgo para datos adjuntos de archivos, puede necesitar también configurar la lógica de confianza para datos adjuntos de archivos. Si habilita esta configuración de directiva, puede especificar el nivel predeterminado de riesgo para tipos de archivo que no se incluyan explícitamente en las listas de tipos de riesgo alto, medio o bajo.  Si deshabilita o no establece esta configuración de directiva, Windows establecerá el nivel de riesgo como moderado, de forma predeterminada.
  
Los valores posibles para la configuración **Nivel de riesgo predeterminado de los datos adjuntos de archivos** son:
  
-   Habilitado, con opciones para configurar el nivel predeterminado del riesgo a
  
    -   Alto riesgo
  
    -   Riesgo moderado
  
    -   Bajo riesgo
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Un atacante quizás disfrace el código malintencionado para engañar a los usuarios y hacer que lo ejecuten.
  
###### Contramedida
  
Configure el parámetro **Nivel de riesgo predeterminado de los datos adjuntos de archivos** en **Habilitado: riesgo moderado**.
  
###### Impacto potencial
  
Los usuarios tendrán que contestar avisos de seguridad antes de que puedan tener acceso a los archivos cuyos tipos no se incluyen explícitamente en la lista de tipos de archivo de bajo riesgo.
  
##### Lista de inclusión de tipos de archivo de riesgo alto
  
Esta configuración de directiva le permite configurar la lista de tipos de archivo de alto riesgo. Si los datos adjuntos del archivo están en la lista de tipos de archivo de alto riesgo y son de la zona restringida, Windows bloquea el acceso del usuario al archivo. Si el archivo es de la zona de Internet, Windows pide confirmación al usuario antes de permitir el acceso al archivo. Esta lista de inclusión tiene prioridad sobre las listas de inclusión de riesgo medio y bajo cuando una extensión se enumera en más de una lista de inclusión. Si habilita esta configuración de directiva, puede crear una lista personalizada de tipos de archivo de alto riesgo. Si deshabilita o no establece esta configuración de directiva, Windows utiliza su lista integrada de tipos de archivo de alto riesgo.
  
Los valores posibles para la configuración **Lista de inclusión de tipos de archivo de riesgo alto** son:
  
-   Habilitado (permite especificar una lista delimitada por comas de extensiones de archivo)
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los usuarios podrían abrir un archivo de alto riesgo de forma accidental, lo cual pondría en peligro sus equipos y, posiblemente, otros equipos de la red.
  
###### Contramedida
  
Configure el parámetro **Lista de inclusión de tipos de archivo de riesgo alto** como **Habilitado** y especifique los tipos de archivo adicionales que desea controlar.
  
###### Impacto potencial
  
Si un tipo de archivo está incluido en más de una lista, se aplicará la más restrictiva. Al definir un valor para este parámetro, se anula la lista integrada de inclusión de tipos de archivo de alto riesgo de Windows.
  
##### Lista de inclusión de tipos de archivo de riesgo moderado
  
Esta configuración de directiva le permite configurar la lista de tipos de archivo de riesgo moderado. Si el archivo adjunto está en la lista de tipos de archivo de riesgo moderado y es de la zona restringida o de Internet, Windows pide confirmación al usuario antes de permitir el acceso al archivo. Esta lista de inclusión anula la lista integrada de tipos de archivo de alto riesgo potencial y tiene prioridad sobre la lista de inclusión de bajo riesgo, pero tiene una prioridad más baja que la lista de inclusión de alto riesgo. Si habilita esta configuración de directiva, puede especificar tipos de archivo que suponen un riesgo moderado. Si deshabilita o no establece esta configuración de directiva, Windows utilizará la lógica de confianza predeterminada.
  
Los valores posibles para la configuración **Lista de inclusión de tipos de archivo de riesgo moderado** son:
  
-   Habilitado (permite especificar una lista delimitada por comas de extensiones de archivo)
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los usuarios podrían abrir un archivo de alto riesgo de forma accidental, lo cual pondría en peligro sus equipos y, posiblemente, otros equipos de la red.
  
###### Contramedida
  
Configure el parámetro **Lista de inclusión de tipos de archivos de riesgo moderado** como **Habilitado** y especifique los tipos de archivo adicionales que desea controlar.
  
###### Impacto potencial
  
Si un tipo de archivo está incluido en más de una lista, se aplicará la más restrictiva. Al definir un valor para esta configuración de directiva, se anula la lista integrada de inclusión de tipos de archivo de riesgo moderado de Windows. Tenga cuidado cuando mueva tipos de archivo de riesgo alto como .EXE a la lista de la inclusión de riesgo moderado, porque entonces será más fácil que los usuarios ejecuten archivos potencialmente peligrosos.
  
##### Lista de inclusión de tipos de archivo de riesgo bajo
  
Esta configuración de directiva le permite configurar la lista de tipos de archivo de bajo riesgo. Si el archivo adjunto está en la lista de tipos de archivo de bajo riesgo, Windows no pedirá confirmación al usuario antes de permitir el acceso al archivo, independientemente de la información de la zona del archivo. Esta lista de inclusión anula la lista integrada de Windows de tipos de archivo de alto riesgo y tiene una prioridad más baja que las listas de inclusión de riesgo alto o medio. Si habilita esta configuración de directiva, puede especificar tipos de archivo que suponen un bajo riesgo. Si deshabilita o no establece esta configuración de directiva, Windows utilizará la lógica de confianza predeterminada.
  
Los valores posibles para la configuración **Lista de inclusión de tipos de archivo de riesgo bajo** son:
  
-   Habilitado (permite especificar una lista delimitada por comas de extensiones de archivo)
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los usuarios podrían abrir un tipo de archivo de alto riesgo de forma accidental, lo cual pondría en peligro sus equipos y, posiblemente, otros equipos de la red.
  
###### Contramedida
  
Configure el parámetro **Lista de inclusión de tipos de archivos de riesgo moderado** como **Habilitado** y especifique los tipos de archivo adicionales que desea controlar.
  
###### Impacto potencial
  
Si un tipo de archivo está incluido en más de una lista, se aplicará la más restrictiva. Al definir un valor para esta configuración de directiva, se anula la lista integrada de inclusión de tipos de archivo de bajo riesgo de Windows. Tenga cuidado cuando mueva tipos de archivo de riesgo alto como. EXE a la lista de la inclusión de bajo riesgo, porque entonces será más fácil que los usuarios ejecuten archivos potencialmente peligrosos.
  
##### Lógica de confianza para datos adjuntos de archivos
  
Esta configuración de directiva le permite configurar la lógica que Windows utiliza para determinar el riesgo para datos adjuntos de archivos. Si habilita esta configuración de directiva, puede escoger el orden en que Windows procesa los datos de evaluación de riesgo.  Si deshabilita o no establece esta configuración de directiva, Windows utilizará la lógica de confianza predeterminada que prefiere el controlador de archivo sobre el tipo de archivo.
  
Los valores posibles para la configuración **Lógica de confianza para datos adjuntos de archivos** son:
  
-   Habilitado, con las opciones siguientes:
  
    -   **Examinar el controlador y el tipo de archivo**. Cuando se selecciona esta opción, Windows utilizará los datos de controlador de archivo o los datos de tipo de archivo, lo que sea más restrictivo.
  
    -   **Preferir el controlador de archivo**. Cuando se selecciona esta opción, Windows siempre confiará en el controlador de archivo (por ejemplo, notepad.exe), independientemente de cuál sea el tipo de archivo.
  
    -   **Preferir el tipo de archivo.** Cuando se selecciona esta opción, Windows siempre confiará en el tipo de archivo, independientemente de cuál sea el controlador de archivo.
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Un atacante puede crear un archivo para aprovechar una vulnerabilidad en un controlador de archivo específico.  
  
###### Contramedida
  
Configure el parámetro **Lógica de confianza para datos adjuntos de archivos** en **Habilitado: examinar el controlador y el tipo de archivo.**
  
###### Impacto potencial
  
Cuando configura el parámetro **Lógica de confianza para datos adjuntos de archivos** para que utilice el controlador y el tipo de archivo, los usuarios verán más avisos de seguridad sobre datos adjuntos porque Windows siempre utilizará el nivel más restrictivo para tomar las decisiones de seguridad de datos adjuntos.
  
##### No conservar la información de zona en los datos adjuntos de archivos
  
Esta configuración de directiva le permite administrar si Windows marca los datos adjuntos de archivos con información acerca de su zona de origen (restringido, Internet, intranet, local). Requiere NTFS para funcionar correctamente, y fallará sin aviso en un sistema de archivos FAT32. Si no se conserva la información de zona, Windows no puede realizar apropiadamente evaluaciones de riesgo. Si habilita esta configuración de directiva, Windows no marca datos adjuntos de archivos con su información de zona. Si deshabilita o no establece esta configuración de directiva, Windows marca los datos adjuntos de archivos con su información de zona.
  
Los valores posibles para la configuración **No conservar la información de zona en los datos adjuntos de archivos** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Un archivo que se descarga de un equipo en Internet o de la zona de sitios restringidos puede moverse a una ubicación que lo hace parecer seguro, como un recurso compartido de archivos de intranet, y un usuario confiado puede ejecutarlo.
  
###### Contramedida
  
Configure **No conservar la información de zona en los datos adjuntos de archivos** en **Habilitado**.
  
###### Impacto potencial
  
Ninguno.
  
##### Ocultar mecanismos para eliminar la información de zona
  
Esta configuración de directiva le permite administrar si los usuarios pueden eliminar manualmente la información de zona de datos adjuntos de archivos guardados. Normalmente, pueden hacer clic en el botón **Desbloquear** en la hoja **Propiedades** del archivo o utilizar una casilla de verificación en el cuadro de diálogo **Advertencia de seguridad**. Si pueden eliminar la información de zona, los usuarios podrían abrir datos adjuntos de archivos potencialmente peligrosos que Windows había bloqueado anteriormente. Si habilita esta configuración de directiva, Windows oculta la casilla de verificación y el botón **Desbloquear**. Si deshabilita o no establece esta configuración de directiva, Windows muestra la casilla de verificación y el botón **Desbloquear**.
  
Los valores posibles para la configuración **Ocultar mecanismos para eliminar la información de zona** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Un usuario podría eliminar información que indica que un archivo provino de una ubicación que no es de confianza.
  
###### Contramedida
  
Configure el parámetro **Ocultar mecanismos para eliminar la información de zona** en **Habilitado.**
  
###### Impacto potencial
  
Los usuarios que tienen una necesidad legítima de eliminar información de zona de los archivos no podrán hacerlo.
  
##### Notificar a los programas antivirus cuando se abren datos adjuntos
  
Esta configuración de directiva le permite administrar la forma en que los programas antivirus registrados reciben una notificación cuando se abren datos adjuntos. Si hay varios programas registrados, se notifica a todos. Si el programa antivirus registrado ya realiza comprobaciones al momento del acceso o exploraciones de archivos cuando llegan al servidor de correo electrónico del equipo, las llamadas adicionales serían superfluas. Si habilita esta configuración de directiva, Windows llama a los programas antivirus registrados para que exploren todos los datos adjuntos de archivos que abra el usuario. Si el programa antivirus falla, los datos adjuntos se bloquean y no se abren. Si deshabilita o no establece esta configuración de directiva, Windows no llama al programa antivirus registrado cuando se abren datos adjuntos de archivos.
  
Los valores posibles para la configuración **Notificar a los programas antivirus cuando se abren datos adjuntos** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los programas antivirus que no realizan comprobaciones al momento del acceso tal vez no puedan explorar los archivos descargados.
  
###### Contramedida
  
Configure **Notificar a los programas antivirus cuando se abren datos adjuntos** en **Habilitado**.
  
###### Impacto potencial
  
Cuando el parámetro **Notificar a los programas antivirus cuando se abren datos adjuntos** está **Habilitado**, se explorarán todos los datos adjuntos de archivos descargados o de correo electrónico que el usuario abra.
  
#### Explorador de Windows
  
El Explorador de Windows se utiliza para explorar el sistema de archivos en clientes Windows XP Professional.
  
Puede establecer la configuración de usuario recomendada del explorador de Windows en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Componentes de Windows\\**  
**Explorador de Windows**
  
##### Quitar las características de grabación de CD
  
Esta configuración de directiva elimina las funciones integradas de grabación de CD en Windows XP. Windows XP le permite crear y modificar CD regrabables si tiene una unidad de CD de lectura/escritura conectada al equipo. Esta característica se puede utilizar para copiar grandes cantidades de datos desde un disco duro a un CD, que entonces se puede eliminar del equipo.
  
**Nota**: esta configuración de directiva no impide que las aplicaciones de terceros creen o modifiquen CD con una grabadora de CD. En esta guía se recomienda que utilice directivas de restricción de software para evitar que las aplicaciones de terceros puedan crear o modificar CD. Si desea más información, consulte el capítulo 6 "Directiva de restricción de software para clientes Windows XP".
  
Otra forma de impedir que los usuarios graben CD consiste en quitar las grabadoras de CD de los equipos cliente del entorno y sustituirlas por unidades de CD de sólo lectura o quitarlas todas.
  
###### Vulnerabilidad
  
La función integrada de grabación de CD se puede utilizar para copiar subrepticiamente información que reside en el equipo o en la red.
  
###### Contramedida
  
Configure el parámetro **Quitar las características de grabación de CD** en **Habilitado.**
  
###### Impacto potencial
  
Cuando el parámetro **Quitar las características de grabación de CD** está **Habilitado**, no pueden escribirse CD sin el uso de aplicaciones de terceros.
  
##### Quitar la ficha Seguridad
  
Esta configuración de directiva deshabilita la ficha **Seguridad** en los cuadros de diálogo de propiedades de carpeta y de archivo en el Explorador de Windows. Si habilita esta configuración de directiva, los usuarios no pueden tener acceso a la ficha **Seguridad** (después de abrir el cuadro de diálogo **Propiedades**) para todos los objetos de sistema de archivos, lo que incluye carpetas, archivos, accesos directos y unidades. Los usuarios no podrán cambiar la configuración en la ficha **Seguridad** ni ver la lista de usuarios.
  
###### Vulnerabilidad
  
Los usuarios pueden tener acceso a la ficha **Seguridad** para determinar qué cuentas tienen permisos para cualquier objeto del sistema de archivos. Los atacantes pueden concentrarse en esas cuentas para lograr un mayor acceso.
  
###### Contramedida
  
Configure el parámetro **Quitar la ficha Seguridad** en **Habilitado.**
  
###### Impacto potencial
  
Cuando el parámetro **Quitar la ficha Seguridad** está **Habilitado**, los usuarios no pueden ver la ficha **Seguridad** para objetos del sistema de archivos, ni revisar o cambiar permisos a través del Explorador de Windows.
  
#### Sistema
  
Puede establecer la configuración de usuario de sistema recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Sistema**
  
##### Impedir el acceso a herramientas de edición del Registro
  
Esta configuración de directiva deshabilita los editores del Registro de Windows Regedit.exe y Regedt32.exe. Si habilita esta configuración de directiva, cuando el usuario intenta iniciar un editor del Registro, aparece un mensaje que le informa que no puede utilizar ninguno de estos editores. Esta configuración de directiva deniega el acceso del Registro con estas herramientas a usuarios o intrusos, pero no evita el acceso al propio Registro.
  
###### Vulnerabilidad
  
Los usuarios pueden tratar de utilizar herramientas de edición del Registro para eludir otras restricciones y directivas. Aunque muchos de los parámetros aplicados por la Directiva de grupo no se pueden omitir de esta forma, los parámetros que se aplican directamente al Registro sí se pueden modificar así.
  
###### Contramedida
  
Configure el parámetro **Impedir el acceso a herramientas de edición del Registro** en **Habilitado.**
  
###### Impacto potencial
  
Cuando el parámetro **Impedir el acceso a herramientas de edición del Registro** está **Habilitado**, los usuarios no pueden iniciar Regedit.exe ni Regedt32.exe para hacer cambios al Registro.
  
#### Sistema\\Administración de energía
  
Puede establecer la configuración de usuario de **Sistema\\Administración de energía** recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Sistema\\Administración de energía**
  
##### Solicitar contraseña al reanudar tras hibernación o suspensión
  
Esta configuración de directiva controla si los equipos cliente del entorno están bloqueados cuando se reanudan tras un estado de hibernación o suspensión. Si habilita este parámetro, los equipos cliente se bloquean cuando reanudan la operación y los usuarios deben introducir sus contraseñas para desbloquearlos. Si deshabilita o no configura este parámetro, existe el potencial para una infracción grave de seguridad, ya que cualquiera puede tener acceso a los equipos cliente después de reanudar el funcionamiento.
  
#### Configuración de protector de pantalla
  
En un principio, los protectores de pantalla se desarrollaron para evitar que se quemara la pantalla de los monitores de rayos catódicos. Desde su aparición, han evolucionado hasta convertirse en una herramienta que permite a los usuarios personalizar la apariencia y el comportamiento del escritorio virtual del equipo. Asimismo, los protectores de pantalla constituyen hoy día una herramienta de seguridad, ya que permiten bloquear automáticamente el escritorio. Esta característica resulta de gran utilidad porque proporciona protección adicional a los equipos de usuario final cuando no se bloquea la consola al dejar el equipo desatendido.
  
Puede establecer la configuración de protector de pantalla del equipo recomendada en la ubicación que se indica a continuación dentro del Editor de objetos de directiva de grupo:
  
**Configuración de usuario\\Plantillas administrativas\\Panel de control\\Pantalla**
  
##### Ocultar la ficha Protector de pantalla
  
Esta configuración de directiva determina si los usuarios pueden agregar, configurar o cambiar el protector de pantalla en el equipo.
  
Si habilita esta configuración de directiva, la ficha **Protector de pantalla** se elimina de **Pantalla** en el Panel de control y los usuarios no podrán cambiar la configuración del protector de pantalla. Si deshabilita o no establece esta configuración de directiva, los usuarios tendrán acceso a esta ficha.
  
Los valores posibles para la configuración **Ocultar la ficha Protector de pantalla** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Los usuarios pueden cambiar la configuración de sus protectores de pantalla para eliminar las contraseñas o aumentar el tiempo que debe pasar antes de que un protector de pantalla bloquee el equipo.
  
###### Contramedida
  
Establezca **Ocultar la ficha Protector de pantalla** en **Habilitado**.
  
###### Impacto potencial
  
Los usuarios no podrán cambiar la configuración del protector de pantalla.
  
##### Proteger el protector de pantalla mediante contraseña
  
Esta configuración de directiva determina si los protectores de pantalla que se utilizan en el equipo están protegidos por contraseña.
  
Si habilita esta configuración de directiva, todos los protectores de pantalla estarán protegidos por contraseña. Si deshabilita esta configuración de directiva, no se podrá establecer la protección por contraseña en ningún protector de pantalla. Esta configuración deshabilita también la casilla de verificación **Protegido por contraseña** de la ficha **Protector de pantalla** del cuadro de diálogo **Propiedades de Pantalla** en Panel de control, lo que ofrece otro modo de evitar que los usuarios modifiquen la configuración de la protección por contraseña.
  
Si no establece esta configuración de directiva, los usuarios podrán decidir si establecen o no la protección por contraseña para cada protector de pantalla utilizado en sus equipos. Para garantizar esta protección en el equipo, se recomienda habilitar el valor **Protector de pantalla** y, a continuación, especificar un tiempo de espera en **Tiempo de espera del protector de pantalla**.
  
Los valores posibles para la configuración **Proteger el protector de pantalla mediante contraseña** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
**Nota**: para quitar la ficha **Protector de pantalla**, utilice el parámetro **Ocultar la ficha Protector de pantalla**.
  
###### Vulnerabilidad
  
Los protectores de pantalla sin protección por contraseña no podrán bloquear la consola de los usuarios que dejen desatendidos sus equipos.
  
###### Contramedida
  
Establezca **Proteger el protector de pantalla mediante contraseña** en **Habilitado**.
  
###### Impacto potencial
  
Los usuarios deberán desbloquear sus equipos después de que se haya iniciado el protector de pantalla.
  
##### Protector de pantalla
  
Esta configuración de directiva habilita el funcionamiento de los protectores de pantalla del escritorio. Si deshabilita esta configuración de directiva, los protectores de pantalla no pueden ejecutarse.
  
Si no establece esta configuración de directiva, no hay efecto en el equipo. Si habilita esta configuración de directiva, los protectores de pantalla se podrán ejecutar siempre y cuando se cumplan las dos condiciones siguientes:
  
-   Se ha especificado un protector de pantalla válido en el equipo cliente desde Nombre del archivo ejecutable del protector de pantalla o en el Panel de control.
  
-   El tiempo de espera del protector de pantalla se establece en un valor distinto a cero en la configuración correspondiente o en el Panel de control.
  
Los valores posibles para la configuración **Protector de pantalla** son:
  
-   Habilitado
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Es necesario habilitar esta configuración para utilizar la característica de bloqueo del protector de pantalla descrita anteriormente.
  
###### Contramedida
  
Establezca **Protector de pantalla** en **Habilitado**.
  
###### Impacto potencial
  
Esta configuración de directiva habilita los protectores de pantalla en los equipos de usuario del entorno.
  
##### Nombre del archivo ejecutable del protector de pantalla
  
Esta configuración de directiva especifica el protector de pantalla que se muestra en el escritorio del usuario. Si habilita esta configuración de directiva, el equipo muestra el protector de pantalla especificado en el escritorio del usuario y deshabilita la lista desplegable de protectores de pantalla en la ficha **Protector de pantalla** de **Pantalla en el Panel de control** (para evitar cambios del usuario). Si deshabilita o no establece esta configuración de directiva, los usuarios podrán seleccionar cualquier protector de pantalla.
  
**Para habilitar la configuración Nombre del archivo ejecutable del protector de pantalla**
  
1.  Escriba el nombre del archivo que contiene el protector de pantalla. Incluya la extensión del nombre de archivo.
  
2.  Si el archivo del protector de pantalla no se encuentra en la carpeta **%Systemroot%\\System32**, escriba la ruta completa de acceso al mismo.
  
    Si el protector de pantalla especificado no está instalado en el equipo al que se aplica la configuración, ésta se pasará por alto.
  
Los valores posibles para la configuración **Nombre del archivo ejecutable del protector de pantalla** son:
  
-   Habilitado. Una vez especificado este valor, escriba el nombre del archivo ejecutable del protector de pantalla.
  
-   Deshabilitado
  
-   No configurado
  
**Nota**: esta configuración de directiva puede anularse con el parámetro **Protector de pantalla**. Si se deshabilita, se pasará por alto **Nombre del archivo ejecutable del protector de pantalla** y no se ejecutarán los protectores de pantalla.
  
###### Vulnerabilidad
  
Para que funcione la característica de bloqueo del protector de pantalla, se debe especificar un archivo ejecutable de protector de pantalla válido.
  
###### Contramedida
  
Establezca **Nombre del archivo ejecutable del protector de pantalla** en scrnsave.scr, el protector de pantalla vacío, o en cualquier otro archivo ejecutable de protector de pantalla.
  
###### Impacto potencial
  
El protector de pantalla vacío, o el que se haya especificado, se ejecutará cuando se cumpla el tiempo de espera establecido.
  
##### Tiempo de espera del protector de pantalla
  
Esta configuración de directiva especifica el tiempo de inactividad del usuario que debe transcurrir antes de que se inicie el protector de pantalla. Si configura este valor, podrá establecer el tiempo de inactividad desde un mínimo de 1 segundo hasta un máximo de 86.400 segundos, equivalente a 24 horas. Si configura este parámetro en 0, el protector de pantalla no se iniciará.
  
Esta configuración de directiva carece de efecto alguno en los siguientes casos:
  
-   Si la configuración de directiva está **Deshabilitada** o **No configurada.**
  
-   Si el tiempo de espera se ha establecido en 0.
  
-   Si se encuentra habilitada la configuración **Sin protector de pantalla**.
  
-   Si no se ha especificado un protector de pantalla válido existente en el cliente en la configuración **Nombre del archivo ejecutable del protector de pantalla** ni en la ficha **Protector de pantalla** del cuadro de diálogo **Propiedades de Pantalla** del equipo cliente.
  
Si deja sin configurar este valor, se utilizara el tiempo de espera especificado en el cliente mediante la ficha **Protector de pantalla** del cuadro de diálogo **Propiedades de Pantalla**. El valor predeterminado es de 15 minutos.
  
Los valores posibles para la configuración **Tiempo de espera del protector de pantalla** son:
  
-   Habilitado, con un tiempo de espera del protector de pantalla entre 1 y 86.400 segundos.
  
-   Deshabilitado
  
-   No configurado
  
###### Vulnerabilidad
  
Se debe configurar un tiempo de espera del protector de pantalla válido para que funcione la característica de bloqueo de este programa.
  
###### Contramedida
  
Configure **Tiempo de espera del protector de pantalla** con un valor adecuado a los requisitos de seguridad de su empresa.
  
###### Impacto potencial
  
El protector de pantalla se ejecutará tras un periodo de inactividad.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de Plantillas administrativas para Windows XP Professional y Windows Server 2003:
  
-   Para obtener un listado completo de todas las configuraciones de directiva de grupo de plantillas administrativas disponibles en Windows XP y Windows Server 2003, descargue la hoja de cálculo "[Group Policy Settings Reference for Windows Server 2003 with Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7821c32f-da15-438d-8e48-45915cd2bc14&displaylang=en)" en
  
    www.microsoft.com/downloads/details.aspx?FamilyId=  
    7821C32F-DA15-438D-8E48-45915CD2BC14.
  
-   Para obtener más información acerca de la ubicación de los archivos .adm, consulte el artículo de Microsoft Knowledge Base "[Ubicación de archivos ADM (plantilla administrativa) en Windows](http://support.microsoft.com/?scid=228460)" en http://support.microsoft.com/?scid=228460.
  
-   Para obtener más información acerca de cómo crear archivos de plantillas administrativas personalizadas en Windows, consulte el artículo de Microsoft Knowledge Base "[Cómo crear plantillas administrativas personalizadas en Windows 2000](http://support.microsoft.com/?scid=323639)" en http://support.microsoft.com/?scid=323639.
  
-   Para obtener información acerca de cómo crear sus propias Plantillas administrativas, consulte las notas del producto "[Implementing Registry-Based Group Policy](http://www.microsoft.com/windows2000/techinfo/howitworks/management/rbppaper.asp)" en
  
    www.microsoft.com/windows2000/techinfo/howitworks/management/rbppaper.asp.
  
-   Para obtener información acerca del Informe de errores, consulte el sitio web de [Informe de errores corporativos](http://www.microsoft.com/spain/licencias/sa/cer.mspx) de Windows en www.microsoft.com/resources/satech/cer/.
  
-   Para obtener información general acerca de Windows Server Update Services (WSUS), consulte la Actualización [Windows Server Update Services Product Overview](http://www.microsoft.com/windowsserversystem/updateservices/evaluation/overview.mspx) en
  
    www.microsoft.com/windowsserversystem/updateservices/evaluation/overview.mspx.
  
-   Para obtener información acerca de la implementación de WSUS, consulte [Deploying Microsoft Windows Server Update Services](http://technet.microsoft.com/es-es/library/cc708532.aspx) en
  
    www.microsoft.com/technet/prodtechnol/windowsserver2003/library/WSUS/  
    WSUSDeploymentGuideTC/.
  
-   Para obtener más información acerca de la Administración de Directiva de grupo, consulte [Enterprise Management with the Group Policy Management Console](http://www.microsoft.com/windowsserver2003/gpmc/default.mspx) en
  
    www.microsoft.com/windowsserver2003/gpmc/.
  
-   El sitio principal de [seguridad de Office 2003](http://office.microsoft.com/en-us/assistance/ha011403061033.aspx) tiene vínculos a artículos en los que se explica cómo utilizar la configuración de seguridad y las características de Office 2003 en
  
    http://office.microsoft.com/en-us/assistance/HA011403061033.aspx
  
-   La descarga "[Office 2003 Policy Template Files and Deployment Planning Tools](http://office.microsoft.com/es-es/help/ha011513711033.aspx)" incluye los archivos de Plantilla administrativa de Directiva de grupo de Oficina y hojas de cálculo en las que se resumen todos los parámetros disponibles en
  
    http://download.microsoft.com/download/9/5/f/95f7e000-d7ab-4b86-8a5d-804b124c7a69/Office-2003-SP1-ADMs-OPAs-and-Explain-Text.exe
  
-   "[Office 2003 Resource Kit toolset](http://download.microsoft.com/download/0/e/d/0eda9ae6-f5c9-44be-98c7-ccc3016a296a/ork.exe)" incluye "Office 2003 Policy Template Files and Deployment Planning Tools" así como otras herramientas útiles para implementar y administrar Office 2003 en
  
    http://download.microsoft.com/download/0/e/d/0eda9ae6-f5c9-44be-98c7-ccc3016a296a/ork.exe
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 10: Entradas del Registro adicionales
  
En este capítulo se proporciona información adicional sobre las entradas del Registro (conocidas también como *valores del Registro*) para el archivo de plantilla de seguridad de línea de base que no están definidas en el archivo de plantilla administrativa (.adm). El archivo .adm define las restricciones y directivas para el escritorio, shell y seguridad de Microsoft® Windows Server™ 2003.
  
[](#cdma)[Editor de configuración de seguridad personalizado](#cdma)  
[](#cdsa)[Entradas del registro relacionadas con TCP/IP](#cdsa)  
[](#wstr)[Entradas del registro varias](#wstr)  
[](#mest)[Entradas del Registro disponibles en Windows XP con SP2 y Windows Server 2003 con SP1](#mest)  
[](#resa)[Entradas del Registro disponibles en Windows XP con SP2](#resa)  
[](#llcc)[Entradas del Registro disponibles en Windows Server 2003 con SP1](#llcc)  
[](#ecec)[Información adicional](#mmdd)
  
### Editor de configuración de seguridad personalizado
  
Al cargar el complemento Plantillas de seguridad de Microsoft Management Console (MMC) y ver las plantillas de seguridad, las entradas de las tablas siguientes no se representan. Estas entradas se agregaron al archivo .inf mediante una versión personalizada del Editor de configuración de seguridad (SCE). También es posible ver o modificar estas entradas mediante un editor de textos como Bloc de notas. Se aplicarán a los equipos cuando se descarguen las directivas, independientemente de si se han modificado las interfaces de usuario del SCE de los equipos.
  
Estas entradas están incrustadas en las plantillas de seguridad para automatizar los cambios. La eliminación de la directiva no supondrá la eliminación automática de dichas entradas, que se deberán modificar manualmente mediante una herramienta de edición del Registro como Regedt32.exe. El libro de Microsoft Excel "Configuración de la seguridad y los servicios predeterminados de Windows" que se incluye con esta guía ofrece información sobre la configuración predeterminada.
  
#### Modificación de la interfaz de usuario del Editor de configuración de seguridad
  
El SCE se utiliza para definir plantillas de seguridad que se pueden aplicar a equipos individuales o a cualquier número de equipos a través de una directiva de grupo. Las plantillas de seguridad pueden contener directivas de contraseña, directivas de bloqueo, directivas de protocolo Kerberos, directivas de auditoría, valores de configuración del registro de eventos, valores de registro, modos de inicio del servicio, permisos del servicio, derechos de usuario, restricciones de pertenencia a grupos, permisos de registro y permisos de sistema de archivos. El SCE aparece en varios complementos de MMC y herramientas de administrador. Los complementos Plantillas de seguridad y Configuración y análisis de seguridad lo utilizan. El complemento Editor de directivas de grupo lo utiliza para la parte Configuración de seguridad del árbol Configuración del equipo. Las herramientas Configuración de seguridad local, Directiva de seguridad del controlador del dominio y Directiva de seguridad de dominio también lo utilizan.
  
Esta guía incluye las entradas adicionales que se agregaron al SCE al modificar el archivo Seregvl.inf (ubicado en la carpeta **%systemroot%\\inf**) y volver a registrar el archivo Scecli.dll. La configuración de seguridad original, así como las adicionales, aparecen bajo **Directivas locales\\Seguridad** en los complementos y herramientas enumerados en esta guía. Debe actualizar el archivo sceregvl.inf y volver a registrar scecli.dll en cualquier equipo en el que se vayan a modificar las plantillas de seguridad y las directivas de grupo que se facilitan con esta guía, como se describe en las secciones siguientes. Sin embargo, la información sobre la personalización del archivo sceregvl.inf utiliza características que sólo están disponibles a partir de Microsoft Windows XP Professional con Service Pack 1 y Windows Server 2003. No intente instalarla en versiones anteriores de Windows.
  
Una vez modificado y registrado el archivo Sceregvl.inf, los valores de registro personalizados se exponen en las interfaces de usuario del SCE del equipo en cuestión. Verá los valores de configuración nuevos al final de la lista de elementos del SCE, todos precedidos por el texto "MSS:", que corresponde a las siglas de Microsoft Solutions for Security, el nombre del grupo que ha creado esta guía. Puede crear directivas o plantillas de seguridad que definan los valores de registro nuevos. Estas plantillas o directivas pueden aplicarse a cualquier equipo, independientemente de si se ha modificado o no Sceregvl.inf en el equipo de destino. Los lanzamientos posteriores de la interfaz de usuario del SCE expondrán los valores de registro personalizados del usuario.
  
Las instrucciones para modificar la interfaz de usuario del SCE se proporcionan en los procedimientos siguientes. Hay instrucciones manuales que debe seguir si ya ha hecho otras personalizaciones en el SCE. Se proporciona una secuencia de comandos para agregar la configuración con una interacción mínima del usuario, y aunque la secuencia de mandos incluye funciones de detección de errores y recuperación, puede fallar. Si falla, debe determinar la causa y corregir el problema o seguir las instrucciones manuales. Se proporciona otra secuencia de comandos que puede utilizar para restaurar la interfaz de usuario del SCE a su estado predeterminado. Esta secuencia de comandos eliminará cualquier configuración personalizada y devolverá el SCE al estado en que aparece en una instalación predeterminada de Windows XP con SP2 o Windows Server 2003 con SP1.
  
**Para actualizar manualmente sceregvl.inf**
  
1.  Utilice un editor de texto como Bloc de notas para abrir el archivo **Values-sceregvl.txt** de la carpeta **SCE Update** de la descarga de esta guía.
  
2.  Abra otra ventana en el editor de texto y abra el archivo **%systemroot%\\inf\\sceregvl.inf**.
  
3.  Desplácese hasta el final de la sección "\[Register Registry Values\]" en el archivo **sceregvl.inf**. Copie y pegue el texto del archivo **Values-sceregvl.txt**, sin saltos de página, en esta sección del archivo **sceregvl.inf**.
  
4.  Cierre el archivo **Values-sceregvl.txt** y abra el archivo **Strings-sceregvl.txt** de la carpeta de **SCE Update** de la descarga.
  
5.  Desplácese hasta el final de la sección "\[Strings\]" en el archivo **sceregvl.inf**. Copie y pegue el texto del archivo **Strings-sceregvl.txt**, sin saltos de página, en esta sección del archivo sceregvl.inf.
  
6.  Guarde el archivo **sceregvl.inf** y cierre el editor de texto.
  
7.  Abra una ventana del símbolo del sistema y ejecute el comando **regsvr32 scecli.dll** para registrar de nuevo el archivo DLL.
  
Los lanzamientos posteriores del SCE mostrarán estos valores de registro personalizados.
  
**Para actualizar automáticamente sceregvl.inf**
  
1.  Los archivos **Values-sceregvl.txt,** **Strings-sceregvl.txt**y **Update\_SCE\_with\_MSS\_Regkeys.vbs** que se encuentran en la carpeta **SCE Update** de la descarga de esta guía deben estar todos en la misma ubicación para que la secuencia de comandos funcione.
  
2.  Ejecute la secuencia de comandos **Update\_SCE\_with\_MSS\_Regkeys.vbs** en el equipo que desea actualizar.
  
3.  Siga las instrucciones en pantalla
  
Este procedimiento eliminará sólo las entradas personalizadas creadas utilizando la secuencia de comandos que se describe en el procedimiento anterior, **Update\_SCE\_with\_MSS\_Regkeys.vbs**. Puede invertir también los cambios hechos por la secuencia de comandos de actualización automática.
  
**Para invertir los cambios hechos por la secuencia de comandos Update\_SCE\_with\_MSS\_Regkeys.vbs**
  
1.  Ejecute la secuencia de comandos **Rollback\_SCE\_for\_MSS\_Regkeys.vbs** en el equipo que desea actualizar.
  
2.  Siga las instrucciones en pantalla
  
Este procedimiento eliminará *cualquier* entrada personalizada que pudiera haber agregado a la interfaz de usuario del SCE, incluidas las de esta guía y otras que se pueden haber proporcionado en versiones anteriores de la guía o en otras guías de seguridad.
  
**Para restaurar el SCE a su estado predeterminado para Windows XP con SP2 o Windows Server 2003 con SP1**
  
1.  Los archivos **sceregvl\_W2K3\_SP1.inf.txt,** **sceregvl\_XPSP2.inf.txt**y **Restore\_SCE\_to\_Default.vbs** que se encuentran en la carpeta **SCE Update** de la descarga de esta guía deben estar todos en la misma ubicación para que la secuencia de comandos funcione.
  
2.  Ejecute la secuencia de comandos **Restore\_SCE\_to\_Default.vbs** en el equipo que desea actualizar.
  
3.  Siga las instrucciones en pantalla
  
**Para restaurar manualmente la interfaz de usuario del SCE a su estado predeterminado**
  
1.  Haga clic en **Inicio**, **Ejecutar**, escriba **regedit.exe** y presione ENTRAR para abrir la herramienta Editor del Registro.
  
2.  Desplácese a **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\SecEdit\\Reg Values**.
  
3.  Cada subclave en esta ubicación representa un elemento en la sección Opciones de seguridad del SCE. Borre con cuidado todas las subclaves. **No borre la clave principal** (Reg Values), sino sólo las subclaves contenidas en ella.
  
4.  Abra una ventana del símbolo del sistema y escriba el comando **regsvr32 scecli.dll** para registrar de nuevo el DLL de SCE.
  
5.  Los lanzamientos posteriores del SCE mostrarán sólo los valores originales del registro incluidos en su versión de Windows
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Entradas del registro relacionadas con TCP/IP
  
Para prevenir los ataques de denegación de servicio (DoS), debe mantener el equipo actualizado con las últimas actualizaciones de seguridad y consolidar la pila del protocolo TCP/IP en los equipos con Windows Server 2003 que se encuentren expuestos a atacantes potenciales. La configuración predeterminada de la pila TCP/IP se optimiza para el control del tráfico de la intranet estándar. Si conecta un equipo directamente a Internet, Microsoft recomienda la consolidación de la pila TCP/IP como protección contra ataques DoS.
  
Los ataques DoS dirigidos a la pila TCP/IP tienden a ser de dos clases: ataques que utilizan un número excesivo de recursos de sistema (una forma de hacerlo es abrir muchas conexiones TCP) o ataques que envían paquetes especialmente diseñados que causan que la pila de la red o todo el sistema operativo fallen. La siguiente configuración de registro contribuye a la protección contra los ataques dirigidos a la pila TCP/IP.
  
La configuración del registro de la tabla siguiente se agregó al archivo de plantilla en la subclave **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Tcpip\\Parameters\\**. Podrá encontrar información más detallada acerca de las diferentes configuraciones en las subsecciones posteriores a la tabla y en la página [Detalles de la implementación del TCP/IP en Microsoft Windows Server 2003](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/networking/tcpip03.mspx) en <http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/networking/tcpip03.mspx>.
  
**Tabla 10.1 Entradas del Registro relacionadas con TCP/IP en Windows Server 2003 con SP1 y Windows XP con SP2**

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
<th><p>Entrada de registro</p></th>  
<th><p>Formato</p></th>  
<th><p>XP SP2 predeterminado</p></th>  
<th><p>2003 SP1 predeterminado</p></th>  
<th><p>Valor más seguro (decimal)</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>DisableIPSourceRouting</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>2</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>EnableDeadGWDetect</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>0</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>EnableICMPRedirect</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>0</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>KeepAliveTime</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>7200000</p></td>
<td style="border:1px solid black;"><p>7200000</p></td>
<td style="border:1px solid black;"><p>300.000</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>PerformRouterDiscovery</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>2</p></td>
<td style="border:1px solid black;"><p>2</p></td>
<td style="border:1px solid black;"><p>0</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>SynAttackProtect</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>0</p></td>
<td style="border:1px solid black;"><p>1</p></td>
<td style="border:1px solid black;"><p>1</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>TcpMaxConnectResponseRetransmissions</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>2</p></td>
<td style="border:1px solid black;"><p>2</p></td>
<td style="border:1px solid black;"><p>2</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>TcpMaxDataRetransmissions</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>5</p></td>
<td style="border:1px solid black;"><p>5</p></td>
<td style="border:1px solid black;"><p>3</p></td>
</tr>  
</tbody>  
</table>
  
#### DisableIPSourceRouting: IP source routing protection level (protects against packet spoofing)
  
Esta entrada aparece como **MSS: (DisableIPSourceRouting) IP source routing protection level (protects against packet spoofing)** en el SCE. El enrutamiento de origen IP es un mecanismo que permite al remitente determinar la ruta IP que un datagrama debe seguir a través de la red.
  
##### Vulnerabilidad
  
Un atacante podría utilizar paquetes enrutados de origen para ocultar su identidad y ubicación. El enrutamiento de origen permite que un equipo que envía un paquete especifique la ruta que sigue dicho paquete.
  
##### Contramedida
  
Configure la entrada **MSS: (DisableIPSourceRouting) IP source routing protection level (protects against packet spoofing)** con el valor **Highest protection,source routing is completely disabled**.
  
Los valores posibles para esta entrada del Registro son:
  
-   0, 1 o 2. La configuración predeterminada es 1 (source routed packets are not forwarded).
  
En la IU del SCE, aparece la lista de opciones siguiente:
  
-   No additional protection, source routed packets are allowed.
  
-   Medium, source routed packets ignored when IP forwarding is enabled.
  
-   Highest protection, source routing is completely disabled.
  
-   No está definido.
  
##### Impacto potencial
  
Si configura este valor en **2** se descartarán todos los paquetes entrantes enrutados de origen.
  
#### EnableDeadGWDetect: Allow automatic detection of dead network gateways (could lead to DoS)
  
Esta entrada aparece como **MSS: (EnableDeadGWDetect) Allow automatic detection of dead network gateways (could lead to DoS)** en el SCE. Cuando se habilita la detección de puertas de enlace inactivas, IP puede cambiar a una puerta de enlace de reserva si varias conexiones experimentan dificultades.
  
##### Vulnerabilidad
  
Un atacante puede forzar al servidor a cambiar de puerta de enlace, posiblemente a una no prevista. Esto sería muy difícil de hacer, por lo que el valor de esta entrada es pequeño.
  
##### Contramedida
  
Configure la entrada **MSS: (EnableDeadGWDetect) Allow automatic detection of dead network gateways (could lead to DoS)** como **Deshabilitado**.
  
Los valores posibles para esta entrada del Registro son:
  
-   1 o 0. La configuración predeterminada es 1 (habilitado) en Windows Server 2003.
  
En la IU del SCE, estas opciones aparecen como:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Impacto potencial
  
Si configura este valor en **0**, Windows no puede detectar puertas de enlace inactivas y cambia automáticamente a otras alternativas.
  
#### EnableICMPRedirect: Allow ICMP redirects to override OSPF generated routes
  
Esta entrada aparece como **MSS: (EnableICMPRedirect) Allow ICMP redirects to override OSPF generated routes** en el SCE. Las redirecciones del protocolo ICMP (Protocolo de mensajes de control de Internet) hacen que la pila instale rutas de host. Estas rutas reemplazan las rutas generadas con OSPF (Abrir primero la ruta de acceso más corta).
  
##### Vulnerabilidad
  
Este comportamiento es de esperar. El problema es que el período de tiempo de espera de 10 minutos para las rutas instaladas de redirección ICMP crea una situación en la red en la que el tráfico ya no se enruta correctamente para el host afectado.
  
##### Contramedida
  
Configure la entrada **MSS: (EnableICMPRedirect) Allow ICMP redirects to override OSPF generated routes** en un valor de **Deshabilitado**.
  
Los valores posibles para esta entrada del Registro son:
  
-   1 o 0. La configuración predeterminada es 1 (habilitado).
  
En la IU del SCE, estas opciones aparecen como:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Impacto potencial
  
Cuando el Servicio de enrutamiento y acceso remoto (RRAS) está configurado como enrutador de límite de sistema autónomo (ASBR), no importa correctamente las rutas de subred de interfaz conectadas, En su lugar, inserta rutas de host en las rutas OSPF. Sin embargo, el enrutador OSPF no se puede utilizar como enrutador ASBR, y cuando se importan rutas de subred de interfaz conectadas a OSPF, el resultado son tablas de enrutamiento confusas con rutas de acceso de enrutamiento extrañas.
  
#### KeepAliveTime: How often keep-alive packets are sent in milliseconds (300,000 is recommended)
  
Esta entrada aparece como **MSS: (KeepAliveTime) How often keep-alive packets are sent in milliseconds (300,000 is recommended)** en el SCE. Controla la frecuencia con la que TCP envía un paquete de mantenimiento de conexión para verificar que una conexión inactiva permanece intacta. Si todavía se puede tener acceso al equipo remoto, confirma el paquete de mantenimiento de conexión.
  
##### Vulnerabilidad
  
Un atacante capaz de conectarse a aplicaciones de red podría establecer numerosas conexiones para causar una condición DoS.
  
##### Contramedida
  
Configure la entrada **MSS: (KeepAliveTime) How often keep-alive packets are sent in milliseconds (300,000 is recommended)** en un valor de **300000** **or 5 minutes**.
  
Los valores posibles para esta entrada del Registro son:
  
-   1 a 0xFFFFFFFF. La configuración predeterminada es 7.200.000 (dos horas).
  
En la IU del SCE, aparece la lista de opciones siguiente:
  
-   150000 or 2.5 minutes
  
-   300000 or 5 minutes **(recommended)**
  
-   600000 or 10 minutes
  
-   1200000 or 20 minutes
  
-   2400000 or 40 minutes
  
-   3600000 or 1 hour
  
-   7200000 or 2 hours **(default value)**
  
-   No está definido
  
##### Impacto potencial
  
De forma predeterminada, Windows no envía paquetes de mantenimiento de conexión. Sin embargo, algunas aplicaciones pueden configurar el indicador de pila TCP que solicita paquetes de mantenimiento de conexión. Para dichas configuraciones, puede reducir este valor de la configuración predeterminada de dos horas a cinco minutos para desconectar sesiones inactivas más rápidamente.
  
#### PerformRouterDiscovery: Allow IRDP to detect and configure Default Gateway addresses (could lead to DoS)
  
Esta entrada aparece como **MSS: (PerformRouterDiscovery) Allow IRDP to detect and configure Default Gateway addresses (could lead to DoS)** en el SCE. Habilita o deshabilita IRDP (Internet Router Discovery Protocol). IRDP permite al equipo detectar y configurar direcciones de puerta de enlace predeterminadas automáticamente (como se describe en RFC 1256) por interfaz.
  
##### Vulnerabilidad
  
Si un atacante consigue el control de un equipo en el mismo segmento de red, puede configurar un equipo de la red para suplantar a un enrutador. A continuación, otros segmentos con IRDP habilitado intentarían enrutar su tráfico a través del equipo en peligro.
  
##### Contramedida
  
Configure la entrada **MSS: (PerformRouterDiscovery) Allow IRDP to detect and configure Default Gateway addresses (could lead to DoS)** en un valor de **Deshabilitado**.
  
Los valores posibles para esta entrada del Registro son:
  
-   0, 1 o 2. La configuración predeterminada es 2 (enable only if DHCP sends the Perform Router Discovery option).
  
En la IU del SCE, estas opciones aparecen como:
  
-   0 (Disabled)
  
-   1 (Enabled)
  
-   2 (enable only if DHCP sends the Perform Router Discovery option)
  
-   No está definido
  
##### Impacto potencial
  
Si deshabilita esta entrada, Windows Server 2003, que admite IRDP, no podrá detectar y configurar automáticamente direcciones de puerta de enlace predeterminadas en el equipo.
  
#### SynAttackProtect: Syn attack protection level (protects against DoS)
  
Esta entrada aparece como **MSS: (SynAttackProtect) Syn attack protection level (protects against DoS)** en el SCE. Esta entrada hace que TCP ajuste la retransmisión de SYN-ACK. Al configurar esta entrada, se reduce la carga de transmisiones incompletas en un ataque de solicitud de conexión (SYN).
  
Puede utilizar esta entrada para configurar Windows de modo que envíe mensajes de descubrimiento de enrutador como difusiones en vez de multidifusiones, como se describe en RFC 1256. De forma predeterminada, si el descubrimiento de enrutador está habilitado, las solicitudes de descubrimiento de enrutador se envían al grupo de multidifusión de todos los enrutadores (224.0.0.2).
  
##### Vulnerabilidad
  
En un ataque "flood" de congestión del servidor SYN, el atacante envía una secuencia continua de paquetes SYN a un servidor. El servidor deja las conexiones semiabiertas hasta que queda desbordado y ya no puede responder a solicitudes legítimas.
  
##### Contramedida
  
Configure la entrada **MSS: (SynAttackProtect) Syn attack protection level (protects against DoS)** con el valor **Connections time out sooner if a SYN attack is detected**.
  
Los valores posibles para esta entrada del Registro son:
  
-   1 o 0. La configuración predeterminada es 1 (Habilitado) en Windows Server 2003 SP1 y 0 (Deshabilitado) en Windows XP SP2.
  
En la IU del SCE, estas opciones aparecen como:
  
-   Connections time out more quickly if a SYN attack is detected
  
-   No additional protection, use default settings
  
-   No está definido
  
##### Impacto potencial
  
Este valor agrega retrasos adicionales a las indicaciones de conexión, y las solicitudes de conexión TCP superan rápidamente el tiempo de espera en caso de producirse un ataque SYN. Si configura esta entrada de registro, las ventanas escalables y los parámetros TCP configurados en las opciones de socket de cada adaptador, incluidos RTT (Initial Round Trip Time) y el tamaño de las ventanas, dejan de funcionar. Cuando se ataca al equipo, las ventanas escalables (RFC 1323) y las opciones de parámetros TCP configurados por adaptador (RTT inicial, tamaño de la ventana) en cualquier socket ya no pueden habilitarse. La razón por la que estas opciones no se pueden habilitar es que cuando la protección funciona, la entrada de la ruta de caché no se revisa antes de que se envíe la señal SYN-ACK, y las opciones de Winsock no están disponible en esta etapa de la conexión.
  
#### TcpMaxConnectResponseRetransmissions: SYN-ACK retransmissions when a connection request is not acknowledged
  
Esta entrada aparece como **MSS: (TcpMaxConnectResponseRetransmissions) SYN-ACK retransmissions when a connection request is not acknowledged** en el SCE. Esta entrada determina el número de veces que TCP retransmite un SYN antes de anular el intento. El tiempo de espera de retransmisión se dobla con cada retransmisión sucesiva en un intento de conexión concreto. El valor de tiempo de espera inicial es de tres segundos.
  
##### Vulnerabilidad
  
En un ataque "flood" de congestión del servidor SYN, el atacante envía una secuencia continua de paquetes SYN a un servidor. El servidor deja las conexiones semiabiertas hasta que queda desbordado y ya no puede responder a solicitudes legítimas.
  
##### Contramedida
  
Configure la entrada **MSS: (TcpMaxConnectResponseRetransmissions) SYN-ACK retransmissions when a connection request is not acknowledged** con el valor **3 seconds,** **half-open connections dropped after nine seconds**.
  
Los valores posibles para esta entrada del Registro son:
  
-   0 a 0xFFFFFFFF. La configuración predeterminada es 2.
  
En la interfaz del usuario del SCE aparece la lista de opciones siguiente, que corresponde a los valores 0, 1, 2 y 3 respectivamente:
  
-   No retransmission, half-open connections dropped after 3 seconds
  
-   3 seconds, half-open connections dropped after 9 seconds
  
-   3 & 6 seconds, half-open connections dropped after 21 seconds
  
-   3, 6, & 9 seconds, half-open connections dropped after 45 seconds
  
-   No está definido
  
##### Impacto potencial
  
Si configura este valor como mayor que o igual a **2**, la pila empleará internamente la protección SYN-ATTACK. Si configura esta entrada en menor que **2**, la pila no puede leer los valores del Registro para protección SYN-ATTACK. Esta entrada reduce la cantidad de tiempo predeterminada necesaria para limpiar una conexión TCP semiabierta. Un sitio sometido a un ataque serio puede establecer un valor tan bajo como **1**. Un valor de **0** es también válido. Sin embargo, si este parámetro se establece en **0**, los SYN-ACK no se volverán a transmitir y el tiempo de espera se excederá en 3 segundos. Con un valor tan bajo, puede producirse un error en los intentos de conexión legítimos de clientes lejanos.
  
#### TcpMaxDataRetransmissions: How many times unacknowledged data is retransmitted (3 recommended, 5 is default)
  
Esta entrada aparece como **MSS: (TcpMaxDataRetransmissions) How many times unacknowledged data is retransmitted (3 recommended,** **5 is default)** en el SCE. Esta entrada controla el número de veces que TCP retransmite un segmento de datos individual (segmento sin conexión) antes de anular la conexión. El tiempo de espera de retransmisión se duplicará con cada retransmisión sucesiva en una conexión. Se restablece cuando se reanudan las respuestas. El valor base de tiempo de espera está determinado de forma dinámica por el tiempo de recorrido completo medido en la conexión.
  
##### Vulnerabilidad
  
Un usuario malintencionado podría agotar los recursos de un equipo vulnerable si nunca envió mensajes de reconocimiento para datos transmitidos por el equipo vulnerable.
  
##### Contramedida
  
Configure la entrada **MSS: (TcpMaxDataRetransmissions) How many times unacknowledged data is retransmitted (3 recommended,** **5 is default)** en un valor de **3**. Los valores posibles para esta entrada del Registro son:
  
-   0 a 0xFFFFFFFF. La configuración predeterminada es 5.
  
En la interfaz del usuario del SCE, este parámetro se puede ajustar utilizando una caja de la entrada de texto:
  
-   Número definido por el usuario
  
-   No está definido
  
##### Impacto potencial
  
TCP inicia un temporizador de retransmisión cuando cada segmento saliente se pasa a IP. Si no se ha recibido ningún acuse de recibo de los datos en un segmento concreto antes de que caduque el temporizador, el segmento se volverá a transmitir hasta tres veces.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Entradas del registro varias
  
Se recomiendan también las entradas del registro en la tabla siguiente. La información adicional de cada entrada, incluida la ubicación de cada parámetro de clave de Registro, se proporciona en las subsecciones que se muestran después de la tabla.
  
**Tabla 10.2 Entradas que no son de TCP/IP agregadas al registro en Windows Server 2003**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="33%" />  
<col width="33%" />  
<col width="33%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Entrada de registro</p></th>  
<th><p>Formato</p></th>  
<th><p>Valor más seguro (decimal)</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (AutoAdminLogon) Enable Automatic Logon (not recommended)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>No definido, excepto para entornos muy seguros, que deben utilizar 0.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (AutoReboot) Allow Windows to automatically restart after a system crash (recommended except for highly secure environments)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>No definido, excepto para entornos muy seguros, que deben utilizar 0.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (AutoShareWks) Enable Administrative Shares (not recommended except for highly secure environments)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>No definido, excepto para entornos muy seguros, que deben utilizar 1.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (DisableSavePassword) Prevent the dial-up passsword from being saved (recommended)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (Hidden) Hide Computer From the Browse List (not recommended except for highly secure environments)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>No definido, excepto para entornos muy seguros, que deben utilizar 1.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (NoDefaultExempt) Enable NoDefaultExempt for IPSec Filtering (recommended)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1 para equipos con Windows XP, 3 para equipos con Windows Server 2003.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (NoDriveTypeAutoRun) Disable Autorun for all drives (recommended)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>0xFF</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (NoNameReleaseOnDemand) Allow the computer to ignore NetBIOS name release requests except from WINS servers (Only recommended for servers)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (NtfsDisable8dot3NameCreation) Enable the computer to stop generating 8.3 style filenames (recommended)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (SafeDllSearchMode) Enable Safe DLL search mode (recommended)</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>1</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>MSS: (ScreenSaverGracePeriod) The time in seconds before the screen saver grace period expires (0 recommended)</p></td>
<td style="border:1px solid black;"><p>Cadena</p></td>
<td style="border:1px solid black;"><p>0</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>MSS: (WarningLevel) Percentage threshold for the security event log at which the system will generate a warning</p></td>
<td style="border:1px solid black;"><p>DWORD</p></td>
<td style="border:1px solid black;"><p>0</p></td>
</tr>  
</tbody>  
</table>
  
#### Disable Automatic Logon: Disable Automatic Logon
  
Esta entrada aparece como **MSS: (AutoAdminLogon) Enable Automatic Logon (not recommended)** en el SCE. Esta entrada determina si está habilitada la característica de inicio de sesión automático. (Esta entrada es independiente de la característica de pantalla de bienvenida en Windows XP; si deshabilita esa característica, esta entrada no se ve afectada). De forma predeterminada, la entrada no está habilitada. El inicio de sesión automático utiliza el dominio, el nombre de usuario y la contraseña que se almacenan en el registro para iniciar la sesión de los usuarios en al equipo cuando éste se inicia. No se muestra el cuadro de diálogo de inicio de sesión.
  
Para obtener información adicional, consulte el artículo de Microsoft Knowledge Base "[How to turn on automatic logon in Windows XP](http://support.microsoft.com/default.aspx?kbid=315231)" en <http://support.microsoft.com/default.aspx?kbid=315231>.
  
Puede agregar este valor de registro al archivo de plantilla en la subclave
  
**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\**  
**CurrentVersion\\Winlogon\\** .
  
##### Vulnerabilidad
  
Si configura un equipo para inicio de sesión automático, cualquiera que pueda obtener acceso físicamente al equipo puede obtener acceso también a todo lo que está en el equipo, incluidas las redes a las que está conectado el equipo. Además, si habilita el inicio de sesión automático, la contraseña se almacena en el registro en texto sin formato. La clave de Registro específica que almacena este parámetro puede leerla de forma remota el grupo de **Usuarios autenticados**. Por lo tanto, esta entrada sólo es apropiada si el equipo está protegido físicamente y si se asegura de que los usuarios que no son de confianza no puedan consultar de forma remota el Registro.
  
##### Contramedida
  
Sólo configure la entrada **MSS: (AutoAdminLogon) Enable Automatic Logon (not recommended)** en equipos sumamente seguros, donde debe configurarse en un valor de **Deshabilitado**.
  
Los valores posibles para esta entrada del Registro son:
  
-   1 o 0. La configuración predeterminada es 0 (deshabilitado).
  
En la IU del SCE, estas opciones aparecen como:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Impacto potencial
  
Ninguno. De forma predeterminada, esta entrada no se habilita.
  
#### Configurar el Reinicio automático tras bloqueos del sistema
  
Esta entrada aparece como **MSS: (AutoReboot) Allow Windows to automatically restart after a system crash (recommended except for highly secure environments)** en el SCE. Determina si el equipo se reinicia automáticamente después de un error.
  
Puede agregar este valor de registro al archivo de plantilla en la subclave
  
**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\CrashControl\\**
  
##### Vulnerabilidad
  
Existe la inquietud de que un equipo podría quedarse atascado en un bucle interminable de errores y reinicios. Sin embargo, la alternativa a esta entrada tampoco es muy atractiva: el equipo simplemente dejará de funcionar.
  
##### Contramedida
  
Configure la entrada **MSS: (AutoReboot) Allow Windows to automatically restart after a system crash (recommended except for highly secure environments)** en un valor de **Deshabilitado**.
  
Los valores posibles para esta entrada del Registro son:
  
-   1 o 0. La configuración predeterminada es 1 (habilitado).
  
Para obtener más información, consulte el artículo de Microsoft Knowledge Base "[How To Configure System Failure and Recovery Options in Windows](http://support.microsoft.com/?kbid=307973)" en <http://support.microsoft.com/?kbid=307973>.
  
En la interfaz del usuario del SCE, están disponibles las siguientes opciones:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Impacto potencial
  
El equipo ya no se reiniciará automáticamente después de un error.
  
#### Habilitar Recursos compartidos administrativos
  
Esta entrada aparece como **MSS: (AutoShareWks) Enable Administrative Shares (not recommended except for highly secure environments)** en el SCE. De forma predeterminada, Windows XP Professional crea automáticamente recursos compartidos administrativos como C$ e IPC$.
  
Para obtener información adicional, consulte el artículo de Microsoft Knowledge Base "[How to create and delete hidden or administrative shares on client computers](http://support.microsoft.com/default.aspx?kbid=314984)" en <http://support.microsoft.com/default.aspx?kbid=314984>.
  
Puede agregar este valor de registro al archivo de plantilla en la subclave
  
**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\LanmanServer\\**  
**Parameters\\**
  
##### Vulnerabilidad
  
Debido a que estos recursos compartidos administrativos integrados son muy conocidos y están presentes en la mayoría de los equipos con Windows, los usuarios malintencionados a menudo se concentran en ellos para sus ataques de fuerza bruta que intentan adivinar las contraseñas así como otros tipos de ataques.
  
##### Contramedida
  
Sólo configure **MSS: (AutoShareWks) Enable Administrative Shares (not recommended except for highly secure environments)** en equipos sumamente seguros, donde debe configurarse en un valor de **Habilitado.**
  
Los valores posibles para esta entrada del Registro son:
  
●    1 o 0. La configuración predeterminada es 1 (habilitado).
  
En la IU del SCE, estas opciones aparecen como:
  
●    Habilitado
  
●    Deshabilitado
  
●    No definido
  
##### Impacto potencial
  
Si borra estos recursos compartidos podría causar problemas a los administradores y programas o a los servicios que dependen de estos recursos compartidos. Por ejemplo, tanto Microsoft Systems Management Server (SMS) como Microsoft Operations Manager 2000 requieren los recursos compartidos administrativos para la instalación y operación correctas. Además, muchas aplicaciones de copia de seguridad de red de terceros necesitan los recursos compartidos administrativos.
  
#### Deshabilitar el guardado de contraseñas de marcado
  
Esta entrada aparece como **MSS: (DisableSavePassword) Prevent the dial-up passsword from being saved (recommended)** en el SCE. Determina si las contraseñas asociadas con entradas de la libreta de teléfonos de Conexiones de red se guardan. Si el usuario tiene muchas entradas de la libreta de teléfonos, las contraseñas guardadas acumuladas pueden causar una ligera demora después de que las credenciales de usuario se introducen en el cuadro de diálogo **Conectarse a**.
  
Puede agregar este valor del Registro a la plantilla en la subclave
  
**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\RasMan\\**  
**Parameters\\**
  
##### Vulnerabilidad
  
Un atacante que roba el equipo portátil de un usuario podría conectarse automáticamente a la red de la empresa si la casilla de verificación **Guardar esta contraseña** está activada para la entrada de marcado.
  
##### Contramedida
  
Configure la entrada **MSS: (DisableSavePassword) Prevent the dial-up password from being saved (recommended)** en un valor de **Deshabilitado**.
  
Los valores posibles para esta entrada del Registro son:
  
-   1 o 0. La configuración predeterminada es 0 (deshabilitado).
  
Para obtener más información, consulte el artículo de Microsoft Knowledge Base "[Disabling Save Password Option in Dial-Up Networking](http://support.microsoft.com/default.aspx?kbid=172430)" en <http://support.microsoft.com/default.aspx?kbid=172430>.
  
En la interfaz del usuario del SCE, están disponibles las siguientes opciones:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Impacto potencial
  
Los usuarios no podrán almacenar automáticamente sus credenciales de inicio de sesión para el marcado y las conexiones VPN.
  
#### Hide the Computer from Network Neighborhood Browse Lists: Hide Computer From the Browse List
  
Esta entrada aparece como **MSS: (Hidden) Hide Computer From the Browse List (not recommended except for highly secure environments)** en el SCE. Puede configurar un equipo para que no envíe anuncios a exploradores en el dominio. Si lo hace, ocultará el equipo de la lista de exploración; no se anuncia a otros equipos en la misma red.
  
Para obtener más información, consulte el artículo de Microsoft Knowledge Base "[HOW TO: Hide a Windows 2000–Based Computer from the Browser List](http://support.microsoft.com/default.aspx?kbid=321710)" en <http://support.microsoft.com/default.aspx?kbid=321710>.
  
Puede agregar este valor de registro al archivo de plantilla en la subclave
  
**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\LanmanServer\\**  
**Parameters\\**
  
##### Vulnerabilidad
  
Un atacante que sabe el nombre de un equipo puede reunir más fácilmente información adicional acerca del mismo. Si habilita esta entrada, elimina un método que un atacante puede utilizar para reunir información acerca de equipos en la red. Además, si habilita esta entrada, puede ayudar a reducir el tráfico de la red. Sin embargo, la vulnerabilidad es menor porque los atacantes pueden utilizar métodos alternativos para identificar y localizar posibles objetivos.
  
##### Contramedida
  
Sólo configure **MSS: (Hidden) Hide Computer From the Browse List (not recommended except for highly secure environments)** en equipos sumamente seguros, donde debe configurarse en un valor de **Habilitado.**
  
Los valores posibles para esta entrada del Registro son:
  
●    1 o 0. La configuración predeterminada es 0 (deshabilitado).
  
En la IU del SCE, estas opciones aparecen como:
  
●    Habilitado
  
●    Deshabilitado
  
●    No definido
  
##### Impacto potencial
  
El equipo ya no aparecerá en la lista de exploración ni en Mis sitios de red en otros equipos en la misma red.
  
#### Enable IPSec to protect Kerberos RSVP Traffic: Enable NoDefaultExempt for IPSec Filtering
  
Esta entrada aparece como **MSS: (NoDefaultExempt) Enable NoDefaultExempt for IPsec Filtering (recommended)** en el SCE. Las exenciones predeterminadas a filtros de directiva IPsec se documentan en la ayuda en línea de Microsoft Windows Server 2003 y Microsoft Windows XP. Estos filtros hacen posible que funcionen Internet Key Exchange (IKE) y el protocolo de autenticación Kerberos. Los filtros también hacen posible que Quality of Service (QoS) de la red se señalice (RSVP) cuando el tráfico de datos está protegido por IPsec, y para el tráfico que tal vez no esté protegido por IPsec, como el tráfico de multidifusión y difusión.
  
Para obtener más información, consulte el artículo de TechNet "[Specifying Default Exemptions to IPsec Filtering](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/depkit/c9a7d986-5b9a-4e01-bb80-82d5e3a87d5c.mspx)" en [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/DepKit/c9a7d986-5b9a-4e01-bb80-82d5e3a87d5c.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/depkit/c9a7d986-5b9a-4e01-bb80-82d5e3a87d5c.mspx). Además, puede consultar el artículo de Microsoft Knowledge Base "[IPsec Default Exemptions Can Be Used to Bypass IPsec Protection in Some Scenarios](http://support.microsoft.com/default.aspx?kbid=811832)" en <http://support.microsoft.com/default.aspx?kbid=811832>.
  
Puede agregar este valor de registro al archivo de plantilla en la subclave
  
**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\IPSEC\\**
  
##### Vulnerabilidad
  
Puesto que IPsec se utiliza cada vez más para el filtrado de paquetes básico de anfitrión a servidor de seguridad, especialmente en situaciones de exposición a Internet, el efecto de estas suposiciones predeterminadas no se ha comprendido completamente. Algunos administradores de IPsec pueden crear directivas IPsec que consideran seguras, pero que en realidad no lo son, contra ataques entrantes que utilizan las suposiciones predeterminadas. Los atacantes podrían falsificar tráfico de red que parecería contener paquetes legítimos de IKE, RSVP o Kerberos, pero que los dirige a otros servicios de red en el anfitrión.
  
##### Contramedida
  
No configure la entrada **MSS: (NoDefaultExempt) Enable NoDefaultExempt for IPsec Filtering (recommended)**, salvo en equipos que utilizan filtros IPsec, en cuyo caso esta entrada debe configurarse en un valor de **Habilitado**.
  
Los valores posibles para esta entrada del Registro son:
  
-   Un valor de 0 especifica que el tráfico multidifusión, difusión, RSVP, Kerberos e IKE (ISAKMP) está exento de filtros IPsec, que es la configuración predeterminada para Windows 2000 y Windows XP. Utilice este parámetro sólo si requiere compatibilidad con una directiva IPsec que ya existe en Windows 2000 y Windows XP.
  
-   Un valor de 1 especifica que el protocolo Kerberos y el tráfico de RSVP no están exentos de filtros IPsec, pero el tráfico de multidifusión, difusión e IKE sí lo están. Este parámetro es el valor recomendado para Windows 2000 y Windows XP.
  
-   Un valor de 1 especifica que el tráfico de multidifusión y difusión no están exentos de filtros IPsec, pero el tráfico RSVP, Kerberos e IKE sí lo están. Este parámetro sólo se admite en Windows Server 2003.
  
-   Un valor de 3 especifica que sólo el tráfico IKE está exento de filtros IPsec. Este parámetro se admite sólo en Windows Server 2003, que contiene este comportamiento predeterminado, aunque la clave de Registro no existe de forma predeterminada.
  
En la IU del SCE, estas opciones aparecen como:
  
-   0
  
-   1
  
-   2
  
-   3
  
##### Impacto potencial
  
Después de que habilita esta entrada, es posible que tenga que cambiar las directivas de seguridad que ya existen, para un funcionamiento correcto. Para ver más detalles, refiérase al artículo de Microsoft Knowledge Base "[IPsec Default Exemptions Can Be Used to Bypass IPsec Protection in Some Scenarios](http://support.microsoft.com/default.aspx?kbid=811832)" en <http://support.microsoft.com/default.aspx?kbid=811832>, que ya se mencionó en esta sección.
  
#### Disable Autorun: Disable Autorun for all drives
  
Esta entrada aparece como **MSS: (NoDriveTypeAutoRun) Disable Autorun for all drives (recommended)** en el SCE. La ejecución automática inicia la lectura de una unidad del equipo en cuanto se insertan medios en la misma. Como resultado, el archivo de configuración de programas y el sonido en medios de audio se inicia inmediatamente.
  
Para deshabilitar la ejecución automática en todas las unidades, puede agregar este valor del Registro al archivo de plantilla en la subclave
  
**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\**  
**Policies\\Explorer\\**
  
Alternativamente, para deshabilitar la ejecución automática únicamente en las unidades de CD/DVD, puede agregar este valor del Registro al archivo de plantilla en la subclave
  
**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\Cdrom\\**
  
##### Vulnerabilidad
  
Para evitar que se ejecute un programa malicioso al insertar un medio, la directiva de grupo deshabilita la ejecución automática en todas las unidades.
  
Un atacante que consiga acceso físico al equipo podría insertar un DVD o CD habilitado para ejecución automática en el equipo, con lo que ejecutaría código malicioso automáticamente.
  
##### Contramedida
  
Configure la entrada **MSS: (NoDriveTypeAutoRun) Disable Autorun for all drives (recommended)** en un valor de **255,** **disable Autorun for all drives.**
  
Los valores posibles para esta entrada del Registro son:
  
-   Un intervalo de valores hexadecimales
  
Para obtener más información, consulte el artículo de Microsoft Knowledge Base "[The AutoRun feature or the AutoPlay feature does not work when you insert a CD-ROM in the drive](http://support.microsoft.com/default.aspx?kbid=330135)" en <http://support.microsoft.com/default.aspx?kbid=330135>.
  
En la interfaz del usuario del SCE, están disponibles las siguientes opciones:
  
-   Null, allow Autorun
  
-   255, disable Autorun for all drives
  
-   No está definido
  
##### Impacto potencial
  
La ejecución automática ya no funcionará al insertar discos habilitados para ejecución automática en el equipo. Además, las utilidades de grabación de CD podrían no funcionar como se espera, porque es posible que no reconozcan los CD en blanco. Las aplicaciones de medios como Reproductor de Windows Media no reconocerán los CD ni DVD nuevos que se inserten, lo que obligará a los usuarios a iniciarlos manualmente.
  
#### Configure NetBIOS Name Release Security: (NoNameReleaseOnDemand) Allow the computer to ignore NetBIOS name release requests except from WINS servers
  
Esta entrada aparece como **MSS: (NoNameReleaseOnDemand) Allow the computer to ignore NetBIOS name release requests except from WINS servers (Only recommended for servers)** en el SCE. NetBIOS sobre TCP/IP (NetBT) es un protocolo de red que, entre otras cosas, ofrece un medio que permite resolver los nombres NetBIOS registrados en los equipos con Windows con respecto a las direcciones IP que se han configurado en los mismos. Este valor determina si el equipo libera su nombre NetBIOS al recibir una solicitud de liberación de nombre.
  
Puede agregar este valor de registro al archivo de plantilla en la subclave
  
**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Netbt\\Parameters\\**
  
##### Vulnerabilidad
  
El protocolo NetBT se ha diseñado para no utilizar ningún método de autenticación y, por lo tanto, es vulnerable a la imitación. La imitación consiste en hacer creer que la transmisión procede de un usuario distinto al que ha realizado la acción. Un usuario malicioso puede explotar la naturaleza sin autenticación del protocolo para enviar un datagrama nombre-conflicto a un equipo de destino y provocar que dicho equipo abandone su nombre y deje de responder a las solicitudes.
  
Como resultado, un ataque de estas características podría causar problemas de conectividad intermitente en el equipo de destino o impedir el uso del Entorno de red, el inicio de sesión en el dominio, el comando NET SEND o la resolución de otros nombres NetBIOS.
  
Para obtener más información, consulte el artículo de Microsoft Knowledge Base "[MS00-047: NetBIOS Vulnerability May Cause Duplicate Name on the Network Conflicts](http://support.microsoft.com/default.aspx?kbid=269239)en <http://support.microsoft.com/default.aspx?kbid=269239>.
  
##### Contramedida
  
Configure la entrada **MSS: (NoNameReleaseOnDemand) Allow the computer to ignore NetBIOS name release requests except from WINS servers (Only recommended for servers)** en un valor de **Habilitado**.
  
Los valores posibles para esta entrada del Registro son:
  
-   1 o 0. La configuración predeterminada es 1 (habilitado).
  
En la IU del SCE, estas opciones aparecen como:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
También puede deshabilitar el uso de WINS en el entorno y asegurarse de que todas las aplicaciones dependan de DNS para los servicios de resolución de nombres. Aunque este enfoque representa una estrategia a largo plazo recomendada, intentar aplicarla como solución a corto plazo suele resultar poco práctico para la mayoría de organizaciones. Las organizaciones que ejecutan WINS suelen tener dependencias de aplicación que no pueden resolverse rápidamente sin actualizaciones e instalaciones distribuidas de software, lo que requiere un planeamiento metódico y compromisos de tiempo significativos.
  
Si no puede implementar esta contramedida y desea garantizar la resolución de nombres de NetBIOS, realice el paso adicional de "precarga" de nombres NetBIOS en el archivo LMHOSTS de ciertos equipos. Para obtener más información acerca de cómo cargar de antemano el archivo LMHOSTS, consulte el artículo de Microsoft Knowledge Base "MS00-047: NetBIOS Vulnerability May Cause Duplicate Name on the Network Conflicts" que ya se mencionó en esta sección.
  
**Nota**: el mantenimiento de archivos LMHOSTS en la mayoría de los entornos requiere de una cantidad considerable de recursos. Microsoft recomienda el uso de WINS en lugar de LMHOSTS.
  
##### Impacto potencial
  
Un atacante podría enviar una solicitud a través de la red que pida a un equipo que libere su nombre NetBIOS. Como sucede con cualquier cambio que pueda afectar a las aplicaciones, Microsoft recomienda someter a prueba este cambio en un entorno que no sea el de producción antes de aplicarlo al entorno de producción.
  
#### Disable Auto Generation of 8.3 File Names: Enable the computer to stop generating 8.3 style filenames
  
Esta entrada aparece como **MSS: (NtfsDisable8dot3NameCreation) Enable the computer to stop generating 8.3 style filenames (recommended)** en el SCE. Windows Server 2003 admite formatos de nombre de archivo 8.3 para la compatibilidad con aplicaciones de 16 bits anteriores. (La convención de nombres de archivo 8.3 es un formato de nombre que permite nombres de archivo con una longitud máxima de ocho caracteres).
  
Puede agregar este valor de registro al archivo de plantilla en la subclave
  
**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\FileSystem\\**
  
##### Vulnerabilidad
  
Si permite los nombres de archivo con estilo 8.3, un atacante sólo necesita ocho caracteres para hacer referencia a un archivo que puede tener 20 caracteres de longitud. Por ejemplo, se puede hacer referencia a un archivo denominado EsteEsUnNombreDeArchivoLargo.doc con su nombre de archivo 8.3 EsteEs~1.doc. Si no utiliza aplicaciones de 16 bits, puede desactivar esta función. Además, el rendimiento de la enumeración de directorios mejora si deshabilita la generación de nombres cortos en una partición con el sistema de archivos NTFS.
  
Los atacantes pueden utilizar nombres de archivo cortos para tener acceso a los archivos de datos y aplicaciones con nombres de archivo largos que normalmente resultarían difíciles de localizar. Un atacante que haya conseguido acceso al sistema de archivos puede tener acceso a los datos o ejecutar aplicaciones.
  
##### Contramedida
  
Configure la entrada **MSS: (NtfsDisable8dot3NameCreation) Enable the computer to stop generating 8.3 style filenames (recommended)** en un valor de **Habilitado**.
  
Los valores posibles para esta entrada del Registro son:
  
-   1 o 0. La configuración predeterminada es 0 (deshabilitado).
  
En la IU del SCE, estas opciones aparecen como:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Impacto potencial
  
Las aplicaciones de 16 bits de la organización no podrán tener acceso a archivos que no estén en el formato 8.3. Algunas aplicaciones de 32 bits dependen también de la presencia de nombres cortos, porque los nombres cortos no suelen incluir espacios incrustados y por tanto no requieren comillas cuando se usan en líneas de comando. Las rutinas de instalación de algunos programas pueden fallar; los que están diseñados para ejecutarse en varias arquitecturas de CPU son probablemente aplicaciones de 16 bits. La instalación de Exchange 2000 SP2 fallará si esta entrada se habilita. La instalación de service packs para SQL 2000 fallarán si esta entrada se habilita y la ruta de la variable del sistema %temp% incluye un espacio; una solución provisional sencilla para este problema es redefinir la variable a una ruta sin espacios (por ejemplo, C:\\temp).
  
**Nota**: si aplica esta entrada a un servidor existente que ya tenga archivos con nombres de archivo 8.3 generados automáticamente, éstos no se eliminarán. Para quitar nombres de archivo 8.3 existentes, debe copiar los archivos en el servidor, eliminarlos de su ubicación original y copiarlos de nuevo en sus ubicaciones originales.
  
#### Enable Safe DLL Search Order: Enable Safe DLL search mode (recommended)
  
Esta entrada aparece como **MSS: (SafeDllSearchMode) Enable Safe DLL search mode (recommended)** en el SCE. La orden de búsqueda de la biblioteca de vínculos dinámicos (DLL) se puede configurar para que busque los archivos DLL solicitados de una de estas dos formas:
  
Si SafeDllSearchMode se configura en 1, el orden de la búsqueda es:
  
-   Directorio desde el que se cargó la aplicación.
  
-   Directorio del sistema.
  
-   Directorio del sistema de 16 bits. No hay ninguna función que obtenga la ruta de este directorio, pero se busca.
  
-   Directorio de Windows.
  
-   Directorio actual.
  
-   Directorios que se incluyen en la variable de entorno PATH.
  
Si SafeDllSearchMode se configura en 0, el orden de la búsqueda es:
  
-   Directorio desde el que se cargó la aplicación.
  
-   Directorio actual.
  
-   Directorio del sistema.
  
-   Directorio del sistema de 16 bits. No hay ninguna función que obtenga la ruta de este directorio, pero se busca.
  
-   Directorio de Windows.
  
-   Directorios que se incluyen en la variable de entorno PATH.
  
Puede agregar este valor de registro al archivo de plantilla en la subclave
  
**HKEY\_LOCAL\_MACHINE\\ SYSTEM\\CurrentControlSet\\Control\\Session Manager\\**
  
##### Vulnerabilidad
  
Si un usuario ejecuta sin saberlo código hostil que se ha empaquetado con archivos adicionales que incluyen versiones modificadas de archivos DLL del sistema, el código hostil puede cargar sus propias versiones y aumentar potencialmente el tipo y grado de daño que puede producir dicho código.
  
##### Contramedida
  
Configure la entrada **MSS: (SafeDllSearchMode) Enable Safe DLL search mode (recommended)** en un valor de **Habilitado**.
  
Los valores posibles para esta entrada del Registro son:
  
-   1 o 0. La configuración predeterminada para Windows XP es 0 y para Windows Server 2003 es 1.
  
En la IU del SCE, estas opciones aparecen como:
  
-   Habilitada
  
-   Deshabilitado
  
-   No está definido
  
##### Impacto potencial
  
Se forzará a las aplicaciones a buscar archivos DLL en la ruta de acceso del sistema en primer lugar. Para aplicaciones que requieran versiones únicas de estos archivos DLL incluidos con la aplicación, esta entrada podría provocar problemas de rendimiento o estabilidad.
  
#### Make Screensaver Password Protection Immediate: The time in seconds before the screen saver grace period expires (0 recommended)
  
Esta entrada aparece como **MSS: (ScreenSaverGracePeriod) The time in seconds before the screen saver grace period expires (0 recommended)** en el SCE. Windows incluye un período de gracia que abarca el período desde que se inicia el protector de pantalla hasta que se bloquea la consola de forma automática si se habilita el bloqueo del protector de pantalla.
  
Puede agregar este valor de registro al archivo de plantilla en la subclave
  
**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\**  
**CurrentVersion\\Winlogon\\** .
  
##### Vulnerabilidad
  
El período de gracia predeterminado permitido para el movimiento del usuario antes de que surta efecto el bloqueo del protector de pantalla es de cinco segundos. Si deja la configuración predeterminada del período de gracia, su equipo queda vulnerable a un posible ataque de alguien que podría dirigirse a la consola e intentar iniciar sesión en el equipo antes de que el bloqueo surta efecto. Se puede realizar una entrada en el registro para ajustar la duración del período de gracia.
  
##### Contramedida
  
Configure la entrada **MSS: (ScreenSaverGracePeriod) The time in seconds before the screen saver grace period expires (0 recommended)** en un valor de **0**.
  
Los valores posibles para esta entrada del Registro son:
  
-   0 a 255. El valor predeterminado es 5 segundos.
  
En la interfaz del usuario del SCE, el valor para esta entrada aparece como una caja de entrada de texto:
  
-   Número definido por el usuario
  
-   No está definido
  
##### Impacto potencial
  
Los usuarios tendrán que escribir sus contraseñas para reanudar las sesiones de consola en cuanto se active el protector de pantalla.
  
#### Security Log Near Capacity Warning: Percentage threshold for the security event log at which the system will generate a warning
  
Esta entrada aparece como **MSS: (WarningLevel) Percentage threshold for the security event log at which the system will generate a warning** en el SCE. Windows Server 2003 y Service Pack 3 para Windows 2000 incluyen una característica nueva para generar una auditoría de seguridad en el registro de eventos de seguridad cuando alcanza un umbral definido por el usuario. Por ejemplo, si este valor se establece en 90, una entrada de evento con Id. de evento 523 se introducirá en el registro cuando el registro de seguridad alcance el 90 por ciento de su capacidad. Esta entrada contiene el texto siguiente:
  
"The security event log is 90 percent full".
  
**Nota**: este parámetro no tendrá ningún efecto si el registro de eventos de seguridad está configurado para sobrescribir eventos según sea necesario.
  
Puede agregar este valor de registro al archivo de plantilla en la subclave
  
**HKEY\_LOCAL\_MACHINE\\ SYSTEM\\CurrentControlSet\\Services\\Eventlog\\Security\\**
  
##### Vulnerabilidad
  
Si el registro de seguridad alcanza el 90 por ciento de su capacidad y no se ha configurado el equipo para sobrescribir eventos como sea necesario, los eventos más recientes no se escribirán en el registro. Si dicho registro se llena y el equipo se ha configurado para apagarse cuando ya no pueda registrar eventos en el registro de seguridad, el equipo se apagará y ya no podrá proporcionar servicios de red.
  
##### Contramedida
  
Configure la entrada **MSS: (WarningLevel) Percentage threshold for the security event log at which the system will generate a warning** en un valor de **90**.
  
Los valores posibles para esta entrada del Registro son:
  
-   0 a 100. La configuración predeterminada es 0 (no se genera un evento de advertencia).
  
En la interfaz del usuario del SCE, están disponibles las siguientes opciones:
  
-   50%
  
-   60%
  
-   70%
  
-   80%
  
-   90%
  
-   No está definido
  
##### Impacto potencial
  
Este valor de configuración generará un evento de auditoría cuando el registro de seguridad alcance el límite del 90 por ciento de capacidad de almacenamiento, a menos que se configure el registro para sobrescribir eventos según sea necesario.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Entradas del Registro disponibles en Windows XP con SP2 y Windows Server 2003 con SP1
  
Las entradas del Registro que se describen en este capítulo se refieren a Microsoft Windows XP con SP1 y Windows Server 2003.
  
El lanzamiento de Windows XP SP2 y Windows Server 2003 SP1 introdujo entradas del Registro adicionales relacionadas con la seguridad que puede configurar para cubrir requisitos de seguridad específicos de su entorno.
  
Las entradas del Registro siguientes están disponibles en Windows XP con SP2 y Windows Server 2003 con SP1.
  
#### RestrictRemoteClients
  
Cuando una interfaz se registra a través de RpcServerRegisterIf, RPC permite que la aplicación de servidor restrinja el acceso a la interfaz, normalmente a través de una devolución de llamada de seguridad. La clave de Registro **RestrictRemoteClients** obliga a RPC a realizar controles de seguridad adicionales para todas las interfaces, incluso si la interfaz no tiene registrada una devolución de llamada de seguridad. Los clientes RPC que utilizan la secuencia de protocolo de canalización con nombre (ncacn\_np) están exentos de estas restricciones. La secuencia de protocolo de canalización con nombre no puede restringirse a causa de diversos problemas mayores de compatibilidad con productos anteriores.
  
La clave de Registro **RestrictRemoteClients** puede tener uno de tres valores DWORD:
  
-   **0**. Este valor es el predeterminado en Windows Server 2003 con SP1, y hace que el equipo omita la restricción de interfaz de RPC. Es responsabilidad de la aplicación de servidor el imponer las restricciones RPC apropiadas. Esta configuración equivale a la configuración de versiones anteriores de Windows.
  
-   **1**. Este valor es el predeterminado en Windows XP con SP2. Todas las llamadas anónimas remotas son rechazadas por el RPC de tiempo de ejecución, excepto las llamadas que entran a través de canalizaciones con nombre (ncacn\_np).
  
-   **2**. Todas las llamadas anónimas remotas son rechazadas por el RPC de tiempo de ejecución, sin excepciones. En esta configuración, un equipo no puede recibir las llamadas anónimas remotas con RPC.
  
Los programadores pueden modificar sus aplicaciones de modo que pasen indicadores al subsistema RPC con el fin de indicar si el cliente o el servidor aceptarán las solicitudes RPC anónimas.
  
##### Vulnerabilidad
  
Las interfaces de RPC que permiten conexiones sin autenticar podrían utilizarse para aprovechar saturaciones del búfer de forma remota y propagar código malintencionado.
  
##### Contramedida
  
La configuración predeterminada del valor **RestrictRemoteClients** en Windows Server 2003 con SP1 y Windows XP con SP2 permite compatibilidad con productos anteriores. Para agregar protección contra gusanos que pueden intentar aprovechar de forma remota las saturaciones del búfer en servicios RPC, configure **RestrictRemoteClients** en **1** o **2.**
  
##### Impacto potencial
  
Si habilita la clave de Registro **RestrictRemoteClients**, no se podrá tener acceso anónimo a la interfaz de asignador de puntos finales de RPC. Esta restricción es una mejora importante de la seguridad, pero cambia la forma en que se resuelven los puntos finales. Actualmente, un cliente RPC que intenta hacer una llamada utilizando un punto final dinámico consulta primero el asignador de puntos finales de RPC en el servidor para determinar a qué punto final se debe conectar. Esta consulta se realiza anónimamente, incluso si la llamada de cliente RPC utiliza seguridad RPC. Las llamadas anónimas a la interfaz del asignador de puntos finales de RPC provocarán un error en Windows Server 2003 con SP1 si la clave **RestrictRemoteClients** se establece en 1 o más. Por tanto, el tiempo de ejecución del cliente RPC debe modificarse para realizar una consulta autenticada al Asignador de extremos. Si se establece la clave **EnableAuthEpResolution**, el tiempo de ejecución de cliente RPC utilizará NTLM para autenticar en el asignador de puntos finales. Esta consulta autenticada sólo se dará si la llamada real del cliente RPC utiliza la autenticación RPC.
  
Algunas aplicaciones y servicios no funcionan apropiadamente cuando esta clave se habilita. Por lo tanto, deberá probarla exhaustivamente antes de implementarla en su entorno. Si piensa habilitar esta clave, debe utilizar también la clave **EnableAuthEpResolution** para habilitar la autenticación del asignador de puntos finales de RPC.
  
#### EnableAuthEpResolution
  
Las llamadas anónimas a la interfaz del asignador de puntos finales de RPC provocarán un error de forma predeterminada en Windows XP con SP2 a causa del valor predeterminado de la nueva clave **RestrictRemoteClients**. Por tanto, el tiempo de ejecución del cliente RPC debe modificarse para realizar una consulta autenticada al Asignador de extremos. Para hacerlo, configure la clave **EnableAuthEpResolution** en 1. Cuando esta configuración está habilitada, el tiempo de ejecución de cliente RPC utilizará NTLM para autenticar en la interfaz del asignador de puntos finales. Esta consulta autenticada sólo se dará si la llamada real del cliente RPC utiliza la autenticación RPC.
  
##### Vulnerabilidad
  
Las interfaces de RPC que permiten conexiones sin autenticar podrían utilizarse para aprovechar saturaciones del búfer de forma remota y propagar código malintencionado.
  
##### Contramedida
  
Para agregar protección contra gusanos que pueden intentar aprovechar de forma remota las saturaciones del búfer en servicios RPC, configure **RestrictRemoteClients** como se describe en la sección anterior y utilice **EnableAuthEpResolution** para habilitar la autenticación NTLM para solicitudes RPC de equipos.
  
##### Impacto potencial
  
Los clientes que no tienen habilitada la clave **EnableAuthEpResolution** no podrán hacer solicitudes del servicio RPC de servidores que han habilitado **RestrictRemoteClients**. Esta restricción puede causar que los servicios basados en RPC dejen de funcionar.
  
#### RunInvalidSignatures
  
De forma predeterminada, Windows Server 2003 con SP1 y Windows XP con SP2 evitan la instalación de objetos de código firmado con firmas no válidas. Estas firmas pueden no ser válidas porque el código se ha modificado, porque el certificado de firma ha caducado o porque el certificado de firma aparece en una lista de revocación de certificados (CRL). Internet Explorer 6.0 ya bloquea la instalación de código firmado con firmas no válidas, pero el service pack extiende este comportamiento a todas las aplicaciones.
  
##### Vulnerabilidad
  
Un control firmado de Microsoft ActiveX® que se ha manipulado puede descargarse y ejecutarse en una aplicación, lo que pone en peligro el equipo en que se ejecuta.
  
##### Contramedida
  
El valor predeterminado de **RunInvalidSignatures** bloquea esta vulnerabilidad.
  
##### Impacto potencial
  
Las aplicaciones que dependen de controles firmados legítimos no funcionarán si las firmas de dichos controles no son válidas por alguna razón. Si tiene una aplicación cuya firma parece no válida, puede cambiar la configuración de esta clave para permitir que el control se descargue y ejecute. Sin embargo, al hacerlo crea una vulnerabilidad de la seguridad. La mejor solución es ponerse en contacto con los programadores del control que se utiliza en la aplicación para obtener una versión con una firma válida.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Entradas del Registro disponibles en Windows XP con SP2
  
Las entradas del Registro siguientes sólo están disponibles en Windows XP con SP2.
  
#### Entradas del Registro de Security Center para XP
  
Hay tres valores del Registro de Security Center que determinan si el usuario recibe avisos para una característica dada. Si una clave tiene un valor de 0 o no existe, el icono de notificación y el sistema de aviso para esa característica están habilitados. Si existe un valor y no es 0, el icono de notificación y el sistema de aviso de la característica están deshabilitados.
  
Estos tres valores se encuentran en **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\**  
**Security Center**. Los valores son:
  
-   **AntiVirusDisableNotify**
  
-   **FirewallDisableNotify**
  
-   **UpdatesDisableNotify**
  
##### Vulnerabilidad
  
Los usuarios que deshabilitan las características de avisos de Security Center pueden no recibir las advertencias apropiadas si el antivirus, el servidor de seguridad o los servicios de actualizaciones automáticas instalados en sus equipos no funcionan apropiadamente por alguna razón.
  
##### Contramedida
  
Aplique una entrada del registro de directiva de grupo para implantar la configuración apropiada de advertencia para su entorno.
  
##### Impacto potencial
  
Estos valores del Registro son visibles en la interfaz de usuario de Security Center si la funcionalidad de Security Center está habilitada. Los usuarios con acceso local de administrador podrán cambiar los valores de Security Center.
  
#### StorageDevicePolicies\\WriteProtect
  
De forma predeterminada, los usuarios pueden montar dispositivos de almacenamiento USB de bloques en sus equipos con Windows XP, y leer y escribir en ellos sin limitaciones. En SP2, Microsoft agregó la función de restricción de la capacidad de los usuarios para escribir a dispositivos de almacenamiento USB de bloques por parte de los administradores.
  
Para restringir la capacidad de los usuarios de escribir en estos dispositivos, puede agregar el valor DWORD **WriteProtect** a **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\StorageDevicePolicies** y configurarlo en **1.** Cuando este valor está configurado, el controlador de Windows para dispositivos de almacenamiento USB de bloques rechazará las solicitudes de escritura a dispositivos de almacenamiento USB de bloques montados.
  
##### Vulnerabilidad
  
Un atacante podría copiar datos a un dispositivo USB extraíble y robarlos.
  
##### Contramedida
  
Cuando el valor **WriteProtect** se establece en 1, Windows XP con SP2 bloquea la escritura a dispositivos de almacenamiento USB de bloques.
  
##### Impacto potencial
  
Esta clave del registro proporciona una mitigación parcial de una amenaza grave. Sin embargo, hay muchas otras maneras en que un atacante hábil puede robar datos con un dispositivo USB. Por ejemplo, un dispositivo USB puede programarse para aparecer como un dispositivo de almacenamiento que no es de bloques (como una impresora o unidad de CD-ROM), lo que eludirá este control. Las organizaciones que desean evitar el robo de datos confidenciales por parte de usuarios o atacantes pueden utilizar esta entrada como parte de una estrategia más amplia de seguridad, en combinación con controles de acceso físico y otras medidas para restringir el acceso a los dispositivos USB con permisos de escritura.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Entradas del Registro disponibles en Windows Server 2003 con SP1
  
Las entradas del Registro siguientes sólo están disponibles en Windows Server 2003 with SP1.
  
#### UseBasicAuth
  
Distributed Authoring and Versioning (DAV) es un protocolo basado en HTTP que permite el acceso remoto a sistemas de archivos y servidores de archivos. Los usuarios pueden utilizar rutas de acceso UNC para tener acceso a los recursos en servidores DAV. Sin embargo, el redirector WebDAV en Windows Server 2003 se comunica con servidores web que admiten DAV a través de HTTP; no puede utilizar sesiones HTTP protegidas con SSL. Cuando estos sitios web permiten el uso de autenticación básica, las solicitudes DAV transmitirán las credenciales de autenticación del usuario en texto sin formato.
  
En Windows Server 2003 con SP1, el redirector WebDAV se ha modificado para que nunca envíe credenciales de usuario con la autenticación básica. Esta modificación puede afectar a los procesos de aplicaciones o negocio que dependen del redirector predeterminado DAV del equipo. (Tenga en cuenta que Microsoft Office utiliza su propio cliente DAV independiente y no se ve afectado por esta entrada).
  
Windows Server 2003 SP1 introduce la subclave **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\WebClient\\**  
**Parameters\\UseBasicAuth**. Si configura su valor en 1, el redirector WebDAV del equipo puede comunicarse con servidores web que sólo admiten autenticación básica.
  
##### Vulnerabilidad
  
Un atacante podría configurar un servidor web que utilice autenticación básica para luego engañar a los usuarios y hacer que se conecten al mismo con el fin de interceptar sus credenciales.
  
##### Contramedida
  
De forma predeterminada, el redirector WebDAV de Windows Server 2003 no utiliza la autenticación básica, lo que bloquea de forma eficaz esta vulnerabilidad.
  
##### Impacto potencial
  
Las aplicaciones que utilizan el redirector WebDAV integrado para tener acceso a los recursos web fallarán si el servidor web sólo admite la autenticación básica. Para resolver este problema, puede configurar el servidor web de modo que admita métodos de autenticación más seguros o puede habilitar el valor **UseBasicAuth**. Sin embargo, el mecanismo preferido es volver a configurar el servidor web, para no permitir la exposición de credenciales de los usuarios.
  
#### DisableBasicOverClearChannel
  
El redirector WebDAV forma parte de la pila del sistema de archivos remoto. Cuando los usuarios intentan abrir direcciones URL en equipos remotos, sus credenciales se pueden exponer si el servidor remoto admite sólo la autenticación básica. Un atacante puede ser capaz de engañar a un usuario y dirigirlo a un sitio web que solicita credenciales (a través de DAV) y utiliza la autenticación básica. Si el usuario responde, expondría sus credenciales al anfitrión malintencionado.
  
La entrada del Registro **UseBasicAuth** controla si la autenticación básica se puede utilizar para solicitudes WebDAV. Si configura el valor **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\WebClient\\**  
**Parameters\\ DisableBasicOverClearChannel** en 1, se bloquea el uso de la autenticación básica con otros recursos web.
  
##### Vulnerabilidad
  
Un atacante podría configurar un servidor web que utilice autenticación básica para luego engañar a los usuarios y hacer que se conecten al mismo con el fin de interceptar sus credenciales.
  
##### Contramedida
  
Configure el valor **DisableBasicOverClearChannel** en 1 en equipos cliente para restringir su capacidad de conectarse a servidores HTTP utilizando la autenticación básica.
  
##### Impacto potencial
  
Muchos dispositivos incrustados (como enrutadores, servidores de impresión y copiadoras) que ofrecen acceso HTTP sólo admiten la autenticación básica, al igual que algunas aplicaciones de negocio. Cuando se configura **DisableBasicOverClearChannel** en 1, los equipos cliente no podrán autenticar a estos dispositivos o aplicaciones.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de algunas de las entradas de configuración que se tratan en este capítulo:
  
-   Para ver un análisis completo acerca de cómo se cargan las DLL en Windows y cómo les afecta la entrada SafeDllSearchMode, consulte "[Dynamic-Link Library Search Order](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/dllproc/base/dynamic-link_library_search_order.asp)" en <http://msdn.microsoft.com/library/default.asp?url=/library/en-us/dllproc/base/dynamic-link_library_search_order.asp>.
  
-   Para obtener detalles acerca de cómo configurar entradas del Registro para deshabilitar controladores de Microsoft para dispositivos de E/S, consulte el artículo de Microsoft Knowledge Base "[HOWTO: Use Group Policy to disable USB, CD-ROM, Floppy Disk and LS-120 drivers](http://support.microsoft.com/default.aspx?kbid=555324)" en <http://support.microsoft.com/default.aspx?kbid=555324>.
  
-   Para obtener más información acerca de la arquitectura subyacente de la creación, edición y procesamiento de plantillas de seguridad, consulte "[How Security Settings Extension Works](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/techref/f546e58e-8473-4985-a05d-0b038dea4a9f.mspx)" en [http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/TechRef/f546e58e-8473-4985-a05d-0b038dea4a9f.mspx](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/techref/f546e58e-8473-4985-a05d-0b038dea4a9f.mspx). Este artículo incluye información detallada acerca del almacenamiento y la prioridad de las directivas de grupo, además de describir el modo en que algunas configuraciones persisten incluso cuando una directiva de grupo determinada ya no se aplica a un equipo (lo que coloquialmente suele denominarse "tatuar").
  
-   Para obtener más información acerca de cómo personalizar la interfaz de usuario del Editor de configuración de seguridad, consulte el artículo de Microsoft Knowledge Base "[Cómo agregar configuraciones personalizadas del Registro al Editor de configuración de seguridad](http://support.microsoft.com/?scid=214752)" en <http://support.microsoft.com/?scid=214752>.
  
-   Para obtener más información sobre los tipos de ataques a la red comunes, consulte "[Common Types of Network Attacks](http://www.microsoft.com/resources/documentation/windows/2000/server/reskit/en-us/cnet/cndb_ips_ddui.asp)", extraído del *Kit de recursos de Windows 2000 Server*, disponible en línea en [http://www.microsoft.com/resources/documentation/Windows/2000/server/reskit/en-us/cnet/cndb\_ips\_ddui.asp](http://www.microsoft.com/resources/documentation/windows/2000/server/reskit/en-us/cnet/cndb_ips_ddui.asp).
  
-   Para obtener más información acerca de cómo reforzar la pila TCP/IP de Windows Server 2003, consulte el artículo de Microsoft Knowledge Base "[Cómo reforzar la pila TCP/IP contra ataques de denegación de servicio en Windows Server 2003](http://support.microsoft.com/?scid=324270)" en [http://support.microsoft.com/?scid=324270 .](http://support.microsoft.com/?scid=324270)
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 11: Contramedidas adicionales
  
En este capítulo se describe cómo implementar algunas contramedidas adicionales, tales como la protección de las cuentas. También se ofrece información general, referencias y orientaciones de configuración para utilizar el filtrado Seguridad IP (IPSec) como una contramedida eficaz frente a los ataques a la red.
  
[](#mpag)[Procedimientos de consolidación de servidores miembro](#mpag)  
[](#cgap)[Configuración del Firewall de Windows](#cgap)  
[](#lemt)[Información adicional](#lemt)
  
### Procedimientos de consolidación de servidores miembro
  
Aunque la mayoría de las contramedidas que se describen en esta guía pueden aplicarse a través de la directiva de grupo, existen otros valores de configuración que son difíciles o no se pueden aplicar mediante dicha directiva. Las siguientes secciones proporcionan orientación acerca de cómo implementar esta configuración adicional para servidores miembro de dominio.
  
#### Protección de las cuentas
  
Microsoft® Windows Server™ 2003 con Service Pack 1 (SP1) dispone de una serie de cuentas de usuario integradas que no se pueden eliminar, pero a las que sí se les puede cambiar el nombre. Dos de las cuentas integradas más conocidas en Windows Server 2003 son Invitado y Administrador.
  
##### Vulnerabilidad
  
De forma predeterminada, se deshabilita la cuenta Invitado en los servidores miembro y controladores de dominio. Esta configuración no se debe modificar. Muchas variaciones de código malintencionado utilizan esta cuenta integrada Administrador como primer intento de acceso al servidor. La protección idónea contra atacantes que intentan utilizar esta cuenta tan conocida es cambiar el nombre de la cuenta de Administrador incorporada y alterar su descripción.
  
El valor de este cambio en la configuración se ha reducido en los últimos años debido a la existencia de herramientas de ataque que intentan obtener acceso al servidor mediante la especificación del identificador de seguridad (SID) de la cuenta integrada Administrador para averiguar su nombre real. Un SID es el identificador único de cada usuario, grupo, cuenta de equipo e inicio de sesión de una red. No se puede modificar en el caso de esta cuenta integrada.
  
##### Contramedida
  
Cambie el nombre de la cuenta de Administrador y modifique la contraseña utilizando un valor largo y complejo en cada servidor.
  
**Nota**: el nombre de la cuenta integrada de Administrador puede cambiarse mediante la utilización de la directiva de grupo. Las directivas de línea de base que se incluyen en la *Guía de seguridad* de *Windows* *Server* 2003 no implementan este parámetro porque cada organización debe elegir un nombre único para esta cuenta. Para cambiar el nombre de la cuenta, configure **Cambiar nombre de cuenta de administrador** en la directiva de grupo en la siguiente ubicación:  
**Configuración del equipo\\Configuración de Windows\\Configuración de seguridad\\Directivas locales\\**  
**Seguridad\\Opciones**  
Lo ideal sería que las organizaciones empleasen contraseñas diferentes en cada servidor, pero esto implica una carga de administración demasiado elevada. Sin embargo, debe tener en cuenta que si su organización utiliza los mismos nombres de cuenta y contraseñas en todos los servidores, los atacantes que logren tener acceso a un servidor miembro podrán tener acceso a todos los demás. Registre cualquier cambio que haga en una ubicación segura.
  
##### Impacto potencial
  
Los usuarios que administran los equipos deben realizar un seguimiento de los nombres de cuenta que se asignan a cada uno de los equipos. Los usuarios que deban iniciar la sesión en un servidor determinado con la cuenta de Administrador local, deberán consultar esta documentación protegida para averiguar el nombre de usuario y la contraseña de dicho servidor.
  
#### NTFS
  
Las particiones de valores de configuración NTFS admiten las listas de control de acceso (ACL) y, opcionalmente, el cifrado (mediante el Sistema de cifrado de archivos, EFS) en los niveles de archivo y carpeta. Esta compatibilidad no se encuentra disponible con los sistemas de archivos FAT (tabla de asignación de archivos), FAT32 o FAT32x. FAT32 es una versión actualizada del sistema de archivos FAT que permite tamaños predeterminados de clúster significativamente más pequeños y admite discos duros con un tamaño máximo de dos terabytes. FAT32 se incluye en Microsoft Windows® 95 OSR2, Windows 98, Windows Me, Windows Server 2003 y Windows XP.
  
##### Vulnerabilidad
  
Los usuarios no autorizados pueden ver, cambiar o eliminar fácilmente los archivos que no se pueden proteger con listas ACL, ya que pueden tener acceso a los mismos localmente o a través de la red. Hay otros archivos que pueden protegerse con las listas ACL, pero el cifrado ofrece una protección muy superior y resulta una opción viable para los archivos a los que sólo un usuario necesita tener acceso.
  
##### Contramedida
  
Formatee todas las particiones en cada servidor con NTFS. Emplee la utilidad de conversión para convertir de forma no destructiva particiones FAT a NTFS, pero no olvide que dicha utilidad configura las listas ACL de la unidad convertida en Todos (Control total).
  
En los sistemas basados en Windows Server 2003 y Windows XP, aplique las siguientes plantillas de seguridad localmente para configurar las listas ACL predeterminadas del sistema de archivos:
  
-   **En las estaciones de trabajo**. %windir%\\inf\\defltwk.inf
  
-   **En los servidores**. %windir%\\inf\\defltsv.inf
  
-   **En los controladores de dominio**. %windir%\\inf\\defltdc.inf
  
Consulte el capítulo 12, "Función de los host de baluarte" en la Guía de seguridad de *Windows* *Server* *2003* para ver instrucciones sobre cómo aplicar localmente las plantillas de seguridad.
  
**Nota**: la configuración de seguridad predeterminada de un controlador de dominio se aplica cuando un servidor se convierte en un controlador de dominio.
  
##### Impacto potencial
  
No tiene ningún impacto negativo.
  
**Importante**: la configuración correcta de los permisos de NTFS permite proteger los datos de la organización frente a la exposición o modificaciones no autorizadas, pero es fundamental que no se olvide de la seguridad física. Un atacante que haya obtenido el control físico de un equipo podrá iniciarlo en otro sistema operativo con un CD-ROM o disquete de inicio. Un atacante que haya extraído un disco duro de uno de los equipos de su organización podrá trasladarlo a otro equipo no administrado. Una vez que el atacante tenga control físico total del medio de almacenamiento, será muy difícil proteger los datos.
  
Se trata de un problema fundamental de la seguridad de los equipos que también existe en los sistemas de archivos de otros sistemas operativos. Cuando el atacante tiene acceso físico al disco, los permisos de NTFS (y la mayoría de las demás salvaguardas) pueden omitirse fácilmente. Las medidas obvias de seguridad física que su organización puede implementar son el acceso restringido a los edificios, la instalación de cerraduras magnéticas en las salas de los servidores, el uso de cerraduras en los soportes de servidor y el uso de cerraduras de estación de acoplamiento para equipos portátiles. Además de estas medidas de seguridad, Microsoft recomienda las siguientes tecnologías adicionales que pueden ayudar a disminuir los efectos de este tipo de ataques:
  
-   Utilice Syskey con una contraseña sin conexión para impedir que personas no autorizadas inicien el sistema operativo Windows.
  
-   Utilice EFS para cifrar los datos de usuario. Indique a los usuarios que utilicen sus cuentas de dominio y no configuren el agente de recuperación, o bien lo configuren para cuentas de administrador de dominio en lugar de la cuenta de administrador local.
  
-   Utilice contraseñas de BIOS para denegar a usuarios no autorizados la capacidad de iniciar equipos dentro de su organización.
  
-   Configure el BIOS del sistema para deshabilitar la función de inicio desde unidades de unidades de CD-ROM y disquete en los equipos. Esta configuración evitará que los usuarios no autorizados inicien equipos con su propio sistema operativo.
  
#### Segmentación de datos y aplicaciones
  
Durante mucho tiempo se ha considerado una práctica aconsejable ubicar los archivos de datos, de aplicaciones y de sistemas operativos en dispositivos de almacenamiento separados para mejorar el rendimiento del equipo. Si separa estos tipos de archivos en los servidores también ayuda a proteger las aplicaciones, los datos y los sistemas operativos frente a ataques transversales de directorio.
  
##### Vulnerabilidad
  
Hay dos tipos de vulnerabilidades que se exponen al colocar los archivos de aplicaciones, de datos y de registro en el mismo volumen de almacenamiento que el sistema operativo. Una vulnerabilidad es el potencial que tiene un usuario o usuarios de llenar deliberada o accidentalmente un archivo de registro de una aplicación o cargar archivos al servidor y llenar el volumen de almacenamiento con datos.
  
La segunda vulnerabilidad se conoce como ataque transversal de directorio; en este caso, un atacante se aprovecha de un error en un servicio de red para desplazarse por el árbol de directorio hasta la raíz del volumen del sistema. El atacante puede entonces buscar en las carpetas de archivos del sistema operativo para ejecutar una utilidad de forma remota.
  
Existen cientos de variaciones de los ataques de salto al directorio que aprovechan la vulnerabilidad de los sistemas operativos y las aplicaciones. IIS ha sido vulnerable a varios de estos ataques en los últimos años. Por ejemplo, los gusanos NIMDA y Code Red explotaron el desbordamiento de búfer para recorrer árboles de directorios de sitios web y ejecutar de forma remota Cmd.exe para obtener acceso a un shell remoto y ejecutar comandos adicionales.
  
##### Contramedida
  
Si es posible, reubique el contenido web, los archivos de aplicaciones, de datos, o de registro de la aplicación en una partición independiente del volumen del sistema.
  
##### Impacto potencial
  
Para las organizaciones que crean y mantienen los servidores de forma sólida, el impacto será mínimo. Para las organizaciones que no mantienen esta información, la repercusión será un poco mayor porque los administradores tendrán que investigar cómo está configurado cada equipo.
  
#### Configuración del nombre de comunidad SNMP
  
El Protocolo simple de administración de redes (SNMP) es una regla de administración de redes que se utiliza de forma generalizada en redes TCP/IP. SNMP proporciona un método de administrar los nodos de red (servidores, estaciones de trabajo, enrutadores, puentes y concentradores) desde un host central. SNMP realiza los servicios de administración correspondientes mediante la utilización de una arquitectura distribuida de sistemas y agentes de administración. Los equipos que ejecutan programas de administración de redes se conocen como sistemas de administración SNMP o administradores SNMP. Los nodos de red administrados se conocen como agentes SNMP.
  
El servicio SNMP ofrece una forma rudimentaria de seguridad mediante la utilización de nombres de comunidad y capturas de autenticación. Puede restringir las comunicaciones SNMP para agentes y permitirles comunicarse sólo con una lista específica de sistemas de administración SNMP, y los nombres de la comunidad pueden utilizarse para autenticar mensajes SNMP. Aunque un host puede pertenecer a varias comunidades a la vez, un agente SNMP no acepta solicitudes de un sistema de administración perteneciente a una comunidad que no se encuentre en su lista de nombres de comunidad aceptables. No existe ninguna relación entre los nombres de comunidad y los nombres de dominio o de grupo de trabajo. Un nombre de comunidad puede considerarse una contraseña compartida por las consolas de administración de SNMP y los equipos administrados. Forma parte de sus responsabilidades como administrador del sistema el crear nombres de comunidad difíciles de averiguar al instalar el servicio SNMP.
  
##### Vulnerabilidad
  
El protocolo SNMP es de por sí débil en materia de seguridad. La mayor vulnerabilidad de SNMP consiste en que prácticamente todos los proveedores establecen un nombre de cadena de comunidad predeterminado, y estos nombres predeterminados son bien conocidos. Por ejemplo, Microsoft utiliza la palabra Public.
  
Hay una segunda vulnerabilidad que es más difícil de solucionar. Dado que el tráfico SNMP se envía en texto sin formato, la cadena de comunidad se transmite a través de la red sin cifrar y sin utilizar valores hash cuando un dispositivo de administración SNMP se conecta con un cliente SNMP. Para contrarrestar esta segunda vulnerabilidad, puede cifrar todo el tráfico entre los servidores. Sin embargo, esta contramedida está fuera del ámbito de esta guía.
  
##### Contramedida
  
Configure la cadena de comunidad SNMP para acceso de lectura en todos los equipos con un valor alfanumérico aleatorio.
  
**Para configurar la cadena de comunidad SNMP**
  
1.  En la consola Servicios, haga doble clic en **Servicio SNMP**.
  
2.  Haga clic en la ficha **Seguridad** del cuadro de diálogo **Propiedades del servicio SNMP**.
  
3.  Seleccione **public** en la lista **Nombres de comunidad aceptados**.
  
4.  Haga clic en el botón **Editar** y, a continuación, escriba el nombre de comunidad nuevo en el cuadro de diálogo **Nombre de comunidad del servicio SNMP** cuando éste aparezca.
  
5.  Haga clic en el botón **Aceptar** para cerrar los cuadros de diálogo.
  
Deje deshabilitado el acceso de escritura mediante SNMP.
  
**Nota**: el nombre de comunidad se almacena en el Registro como un valor de registro con un valor DWORD de 4; para automatizar este cambio, cree una secuencia de comandos o agregue una línea a una plantilla de seguridad e importe la plantilla a una directiva de grupo basada en el dominio. El valor se almacena en: **HKLM\\SYSTEM\\CurrentControlSet\\Services\\SNMP\\Parameters\\ValidCommunities**.
  
##### Impacto potencial
  
Asimismo, debe volver a configurar la cadena de comunidad en todas las herramientas de administración que utilicen el protocolo SNMP.
  
#### Deshabilitación de NetBIOS y SMB en interfaces públicas
  
En esta sección se describen las recomendaciones específicas para los servidores que se encuentran en redes que no pueden controlarse por completo, como los servidores web accesibles públicamente o las puertas de acceso de correo electrónico. Este tipo de servidores se conoce a menudo como host de baluarte. Si tiene cualquiera de dichos servidores, debe considerar los procedimientos recomendados en esta contramedida. Sin embargo, debe probar cada cambio detenidamente y asegurarse de entender que será problemático administrar equipos en los que se ha deshabilitado NetBIOS.
  
##### Vulnerabilidad
  
Para ayudar a proteger un host de baluarte, puede reducir mucho el impacto de un ataque si deshabilita el bloque de mensajes del servidor (SMB) y NetBIOS sobre TCP/IP. Será difícil administrar servidores que operan con esta configuración y no podrán tener acceso a carpetas compartidas en la red. Sin embargo, estas medidas protegen de forma eficaz el servidor a través de los protocolos SMB y NetBIOS. Por lo tanto, debe deshabilitar SMB y NetBIOS a través de TCP/IP para las conexiones de red de los servidores a los que se puede tener acceso desde Internet.
  
##### Contramedida
  
No se evitará la comunicación SMB si deshabilita NetBIOS. SMB utilizará el puerto TCP 445, que se conoce como host directo de SMB o puerto del sistema común de archivos de Internet (CIFS), en ausencia de puertos NetBIOS uniformes. En consecuencia, deben realizarse algunos pasos explícitos para deshabilitar NetBIOS y SMB por separado.
  
NetBIOS hace uso de los siguientes puertos:
  
-   UDP/137 (servicio de nombres NetBIOS)
  
-   UDP/138 (servicio de datagramas NetBIOS)
  
-   TCP/139 (servicio de sesión NetBIOS)
  
SMB utiliza los siguientes puertos:
  
-   TCP/139
  
-   TCP/445
  
En servidores accesibles desde Internet, siga este procedimiento para eliminar Compartir impresoras y archivos para redes Microsoft y Cliente para redes Microsoft.
  
**Para deshabilitar SMB**
  
1.  En **Panel de control**, haga doble clic en Conexiones de red.
  
2.  Haga clic con el botón secundario en una conexión de Internet y, a continuación, haga clic en **Propiedades**.
  
3.  En el cuadro de diálogo **Propiedades**, seleccione **Cliente para redes Microsoft** y, a continuación, haga clic en **Desinstalar**.
  
4.  Siga los pasos de desinstalación.
  
5.  Seleccione **Compartir impresoras y archivos para redes Microsoft** y, a continuación, haga clic en **Desinstalar**.
  
6.  Siga los pasos de desinstalación.
  
**Para deshabilitar NetBIOS a través de TCP/IP**
  
1.  En **Panel de control**, haga doble clic en **Sistema**, haga clic en la ficha **Hardware** y, a continuación, seleccione el botón Administrador de dispositivos.
  
2.  En el menú **Ver**, haga clic en **Mostrar dispositivos ocultos**.
  
3.  Expanda **Controladores que no son Plug and Play**.
  
4.  Haga clic con el botón secundario en **NetBios a través de Tcpip** y, a continuación, haga clic en **Deshabilitar**.
  
De esta forma se deshabilitará el servicio de escucha de host directo de SMB en TCP/445 y UDP 445.
  
**Nota**: este procedimiento deshabilita el controlador Nbt.sys. Aunque deshabilita el servicio de sesión NetBIOS (que escucha en el puerto TCP 139), no deshabilita SMB completamente. Para hacerlo, siga los pasos del procedimiento "Para deshabilitar SMB" ya indicado.
  
##### Impacto potencial
  
Ningún equipo podrá conectarse al servidor a través de SMB. Los servidores no podrán tener acceso a las carpetas compartidas de la red. Las herramientas de administración que dependen de NetBIOS o SMB para la conectividad no podrán establecer conexión con los servidores.
  
#### Configuración del puerto de los Servicios de Terminal Server
  
Los Servicios de Terminal Server constituyen una herramienta de gran utilidad para los administradores de la red, porque habilitan la administración de los equipos del servidor remoto y del usuario final. El cliente de Escritorio remoto se instala de manera predeterminada en todos los equipos con Windows Server 2003 y Windows XP, y está disponible como componente opcional en el medio de instalación de Windows 2000 Server. Asimismo, se puede descargar un cliente Microsoft ActiveX® que se ejecuta en Internet Explorer o en Microsoft Management Console (MMC). El escritorio remoto y los clientes ActiveX se conocen conjuntamente como TSAC (Terminal Services Advanced Client, Cliente avanzado de Servicios de Terminal Server).
  
##### Vulnerabilidad
  
Los Servicios de Terminal Server escuchan en el puerto TCP 3389 de manera predeterminada, y todas las versiones de los clientes de Escritorio remoto intentan conectarse a dicho puerto. Aunque toda la sesión está cifrada (incluida la autenticación del usuario), los clientes de los Servicios de Terminal Server no realizan la autenticación del servidor. Un atacante que pueda imitar a un servidor legítimo de los Servicios de Terminal Server podrá engañar a los usuarios para que se conecten al servidor del atacante en lugar de hacerlo al servidor genuino. Para lograr este engaño, el atacante podría alterar los registros DNS para redirigir a los usuarios a su servidor o utilizar otros medios.
  
##### Contramedida
  
Cambie el puerto TCP utilizado por los Servicios de Terminal Server o implemente una directiva IPSec que requiera confianza y negociación AH (Encabezado de autenticación) o ESP (Carga de seguridad encapsuladora) mediante la utilización del modo de transporte IPSec (no el modo de túnel IPSec). En algunos casos, es posible aislar Terminal Server tras una puerta de enlace VPN, de modo que para tener acceso a Terminal Server sean necesarios túneles VPN protegidos mediante Protocolo de túnel punto a punto (PPTP) o mediante L2TP/IPSec.
  
Para obtener información acerca de cómo cambiar el puerto utilizado por los Servicios de Terminal Server y el cliente de Escritorio remoto, consulte el artículo de Microsoft Knowledge Base "[Cómo cambiar el puerto en el que escucha Terminal Server](http://support.microsoft.com/?scid=187623)" en http://support.microsoft.com/?scid=187623. Este artículo explica cómo cambiar el puerto que escucha en el cliente de escritorio normal. Para cambiarlo en el cliente web avanzado de Servicios de Terminal Server, deberá agregar la siguiente línea de secuencia de comandos a la página web:
  
MsRdpClient.RDPport = xxx
  
(xxx representa el número de puerto TCP deseado). Para obtener más información sobre el modo de utilizar y personalizar la Conexión web al Escritorio remoto para ejecutar sesiones de los Servicios de Terminal Server en Microsoft Internet Explorer, consulte "[Providing for RDP Client Security](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/termserv/termserv/providing_for_rdp_client_security.asp)", en la dirección http://msdn.microsoft.com/library/default.asp?url=/library/en-us/termserv/termserv/  
providing\_for\_rdp\_client\_security.asp.
  
##### Impacto potencial
  
La implementación de IPSec con AH tiene un impacto mínimo en el rendimiento del sistema; no obstante, implica un aumento de la carga para la administración de la configuración IPSec de cliente y servidor. Se requiere también un aumento de la carga para la administración de un método de confianza mutua entre los equipos cliente y servidor utilizados por la negociación de seguridad de Intercambio de claves de Internet (IKE) antes de establecer asociaciones de seguridad IPSec. La directiva IPSec se debe designar para proteger todo el tráfico al servidor o para que IPSec sea necesario únicamente para las conexiones al puerto TCP 3389. Si IPSec es necesario en el servidor, se denegará el acceso a los equipos cliente que no tengan una configuración y confianza compatibles con IPSec. Consulte la sección “Configuración de las directivas IPSec” más adelante en este capítulo para obtener más información acerca de la utilización de directivas IPSec para negociar la seguridad del tráfico TCP/IP.
  
Si cambia los puertos predeterminados en servidores y clientes de Servicios de Terminal Server, los usuarios legítimos que no tengan configurado su software cliente para utilizar el puerto nuevo no podrán conectarse a equipos cuyas asignaciones de puerto han cambiado. Además, no hay forma de cambiar el puerto TCP en la versión actual de TSAC.
  
#### Deshabilitar Dr. Watson: Deshabilitar la ejecución automática del depurador del sistema Dr. Watson
  
Los programas de depuración del sistema facilitan la solución de problemas en equipos y aplicaciones. Estos programas reúnen datos y los presentan al administrador del sistema o al desarrollador de aplicaciones mientras el equipo está en funcionamiento. La herramienta Dr. Watson que se incluye con Windows Server 2003 y Windows XP es un programa automatizado de depuración del sistema que registra información sobre el estado del sistema y las aplicaciones que estaban activas cuando se produce un error en un programa.
  
##### Vulnerabilidad
  
Algunas organizaciones pueden considerar que no se deben instalar programas de depuración en equipos críticos de producción. No hay vectores de ataque conocidos relacionados con Dr. Watson que puedan aprovechar usuarios que no tengan privilegios administrativos. Es decir, un atacante necesitaría pertenecer al grupo de **Administradores** local para utilizar Dr. Watson como herramienta de ataque contra otros usuarios o procesos. Un atacante que ya ha obtenido privilegios administrativos tiene el control completo del equipo así que, aunque deshabilite Dr. Watson, los atacantes podrían encontrar otros medios.
  
##### Contramedida
  
Para obtener más información acerca de cómo deshabilitar el programa de depuración Dr. Watson, consulte el artículo de Microsoft Knowledge Base "[How to Disable Dr. Watson for Windows](http://support.microsoft.com/?kbid=188296)" en http://support.microsoft.com/?kbid=188296.
  
##### Impacto potencial
  
No se ejecutará ningún programa de depuración del sistema y no se creará automáticamente ningún informe, si los programas se bloquean. Los administradores de sistemas y los desarrolladores tendrán menos información disponible para diagnosticar la causa de dichos problemas, y la función de informe de errores no funcionará.
  
#### Deshabilitar SSDP/UPNP: Deshabilitar SSDP/UPNP
  
Si deshabilita el servicio host Plug and Play universal (UPnP™), otras aplicaciones tales como Windows Messenger podrán seguir utilizando los servicios y procesos de descubrimiento del Protocolo simple de descubrimiento de servicios (SSDP) para identificar puertas de enlace de red u otros dispositivos de red.
  
Para obtener más información, consulte el artículo de Microsoft Knowledge Base "[Traffic Is Sent After You Turn Off the SSDP Discover Service and Universal Plug and Play Device Host](http://support.microsoft.com/?kbid=317843)" en http://support.microsoft.com/?kbid=317843.
  
##### Vulnerabilidad
  
Las funciones de UPnP incluidas en Windows XP y Windows Server 2003 pueden ser muy útiles para usuarios domésticos y de pequeñas empresas porque pueden automatizar la instalación y la configuración de dispositivos UPnP cuando se conectan a la red local. Puede que algunas organizaciones deseen asegurarse de que no haya ningún tráfico de UPnP o SSDP a través de su red. Aunque actualmente no hay vulnerabilidades conocidas relacionadas con estas características, hace un par de años se descubrió un problema mayor en Windows XP para el que se necesitó la aplicación de una revisión.
  
##### Contramedida
  
Para asegurarse de que ninguna aplicación utilice las funciones SSDP y UPnP incluidas en Windows XP, puede agregar un valor de registro REG\_DWORD llamado UPnPMode a la clave de registro siguiente:
  
**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\DirectPlayNATHelp\\DPNHUPnP\\**
  
y configurar su valor a 2.
  
##### Impacto potencial
  
Las funciones UPnP y SSDP se deshabilitarán completamente. Cuando se conecten dispositivos UPnP a la red, tendrá que configurarlos y administrarlos manualmente.
  
#### Configuración de las directivas IPSec
  
IPSec (disponible en los sistemas operativos Windows 2000, Windows XP y Microsoft Windows Server 2003) es una herramienta que permite que los administradores de seguridad de la red permitan, bloqueen o negocien la seguridad del tráfico TCP/IP. IPSec es independiente de las aplicaciones y transparente para las mismas. El objetivo de diseño para Windows 2000 consistía en proporcionar una forma de proteger el tráfico de la red con el formato AH o ESP del protocolo IPSec. La directiva IPSec proporciona filtros de tráfico TCP/IP estáticos (denominados también "*selectores*") necesarios para negociar la seguridad mediante IKE
  
El capítulo 6, "Deploying IPSec" en [*Windows Server 2003 Deployment Kit: Deploying Network Services*](http://technet.microsoft.com/en-us/library/cc775745.aspx) ofrece información más exhaustiva acerca de las capacidades más recientes de IPSec. La sección "Determining Your IPSec Needs" identifica los usos de IPSec: Este documento está disponible para su descarga en www.microsoft.com/downloads/details.aspx?  
FamilyID=d91065ee-e618-4810-a036-de633f79872e&DisplayLang=en.
  
Para la mayoría de las aplicaciones, el componente de Firewall de Windows proporciona la protección adecuada a nivel de anfitrión contra el tráfico de entrada malintencionado. El Asistente para configuración de seguridad (SCW) en Windows Server 2003 con SP1 simplifica mucho la instalación y la administración de la configuración del Firewall de Windows en implementaciones grandes. IPSec debe utilizarse para proteger el tráfico de anfitrión a anfitrión y de anfitrión a cliente según corresponda, y en general el Firewall de Windows se debe implementar extensamente en la mayor parte de las organizaciones como una capa de defensa adicional.
  
##### Vulnerabilidad
  
Aunque la mayoría de las estrategias de seguridad de la red se centran en la forma de evitar los ataques externos a la red de la organización, se puede perder una gran cantidad de información confidencial debido a ataques internos que interpretan los datos de la red o que explotan los puntos débiles de diseño o implementación de los protocolos de capa superior para tener acceso al equipo. Los atacantes pueden utilizar sesiones nulas de NetBT para obtener información que puede utilizarse para poner en peligro las contraseñas de administrador (si no se utilizan otros valores de configuración de seguridad o si éstos se desactivan accidentalmente).
  
Los atacantes sólo tienen que localizar una vulnerabilidad de un puerto de la aplicación para obtener acceso al equipo e incluso llegar a controlarlo por completo. Como ya se mencionó, debido a que muchos tipos de datos no están protegidos cuando viajan a través de la red, los empleados, el personal de apoyo o los visitantes pueden copiar datos para su análisis posterior. Los servidores de seguridad situados entre la red interna e Internet no ofrecen protección frente a este tipo de amenazas internas. Los servidores de seguridad internos a menudo no pueden proporcionar controles de acceso autenticados, necesarios para proteger a clientes y servidores, ni tampoco pueden proporcionar una seguridad total del tráfico de red entre equipos.
  
##### Contramedida
  
Los filtros IPSec reconocen el tráfico TCP/IP por la dirección IP de origen y de destino, por el tipo de protocolo IP y por los puertos TCP y UDP. Los filtros IPSec pueden ayudar a contener y controlar la propagación de código malicioso mediante el bloqueo del tráfico de gusanos y virus. Asimismo, puede resultar muy difícil para un atacante utilizar los shell remotos u otras utilidades de ataque para tener acceso al equipo desde una aplicación comprometida. Para obtener más detalles sobre cómo puede aplicarse una directiva de IPSec en Windows 2000 para bloquear puertos, consulte el artículo de Microsoft Knowledge Base “[Cómo bloquear protocolos y puertos específicos de red con IPsec](http://support.microsoft.com/?scid=813878)” en http://support.microsoft.com/?scid=813878. Además, las notas del producto "[Using IPsec to Lock Down a Server](http://www.microsoft.com/technet/itsolutions/network/security/ipsecld.mspx)" en www.microsoft.com/technet/itsolutions/network/security/ipsecld.mspx constituyen una guía de configuración detallada para el filtrado IPSec de permisos/bloqueos de Windows Server 2003, similar a esta guía. No obstante, para Windows 2000 se deben agregar los valores de configuración del registro NoDefaultExempt recomendados en el artículo de Microsoft Knowledge Base.
  
Windows Server 2003 proporciona el complemento Administración de directivas IPSec de MMC, que es una interfaz gráfica de usuario (GUI) que puede utilizar para administrar la directiva IPSec. Esta herramienta es muy similar a la de Windows 2000 y Windows XP. Windows Server 2003 proporciona el complemento Monitor IPSec de MMC y la utilidad de línea de comandos IPSec NETSH para mostrar los filtros de directiva IPSec aplicados en el equipo. Los filtros de permiso y bloqueo aparecen en la configuración de modo rápido IKE; los filtros de modo rápido IKE genéricos son los filtros definidos en la directiva IPSec asignada. Los filtros de modo rápido IKE específicos son el resultado de la aplicación de la directiva a la configuración IP concreta del equipo. Tenga en cuenta que la función específica del modo rápido IKE Buscar filtros coincidentes no se puede utilizar para buscar coincidencias de los filtros de permiso y bloqueo, sino únicamente para los filtros que tengan una acción de negociación.
  
Los términos siguientes se analizan en el resto de esta sección:
  
-   **Lista de filtros**. Incluye puertos, protocolos y direcciones. Las listas de filtros activan una decisión cuando el tráfico coincide con alguna especificación de la lista en cuestión. Una lista puede contener varios filtros.
  
-   **Acción de filtrado**. Respuesta necesaria cuando el tráfico coincide con una lista de filtros. Las acciones específicas incluyen el bloqueo o el permiso de determinado tráfico.
  
-   **Regla**. Una regla es la correlación de una lista de filtros con una acción de filtrado.
  
-   **Directiva IPSec**. Conjunto de reglas. Sólo puede estar activa una directiva al mismo tiempo.
  
Una forma fácil de registrar esta información es mediante una tabla denominada mapa de tráfico de red. Este tipo de mapa contiene información básica acerca de la función del servidor, la dirección del tráfico de la red, el destino del tráfico, la dirección IP de la interfaz, el protocolo IP, el puerto TCP y el puerto de Protocolo de datagramas de usuario (UDP) implicados. En la tabla siguiente se muestra un ejemplo de mapa de tráfico de red.
  
Un mapa de tráfico de red permite comprender qué tipo de tráfico de red entra y sale de determinados servidores. Antes de crear directivas IPSec, es fundamental que entienda qué tipo de tráfico se requiere para que el servidor funcione correctamente. De lo contrario, podrían crearse filtros demasiado estrictos que pueden originar errores de la aplicación.
  
**Para crear un mapa de tráfico**
  
1.  Determine los servicios básicos de red necesarios para la función del servidor.
  
2.  Identifique los protocolos y puertos necesarios para cada servicio. Este proceso puede implicar la utilización del Monitor de red para capturar y analizar el tráfico de la red a fin de determinar las direcciones de destino, los protocolos y los puertos. Asimismo, puede utilizar herramientas como el comando Netstat.exe para ver los puertos abiertos y las conexiones activas.
  
3.  Documente las reglas de filtrado IPSec necesarias para permitir sólo el tráfico identificado.
  
Si se empieza por los filtros IPSec más restrictivos y se abren puertos adicionales sólo cuando sea necesario, se puede obtener el máximo nivel de seguridad posible para estos valores de configuración. Este proceso es mucho más fácil si los servicios se dividen en servicios de cliente y de servidor. Deben definirse los servicios de servidor para cualquier servicio que el equipo proporcione a otros hosts.
  
**Tabla 11.1: Ejemplo de mapa de tráfico de red**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Servicio</p></th>  
<th><p>Protocolo</p></th>  
<th><p>Puerto de origen</p></th>  
<th><p>Puerto de destino</p></th>  
<th><p>Dirección de origen</p></th>  
<th><p>Dirección de destino</p></th>  
<th><p>Acción</p></th>  
<th><p>Reflejo</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Servidor HTTP</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>80</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Servidor HTTPS</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>443</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Cliente DNS</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>53</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>DNS</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Bloquear todo</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>BLOQUEAR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
</tbody>  
</table>
  
En este ejemplo de mapa de tráfico, el servidor web proporcionará servicios HTTP y HTTPS a los equipos desde cualquier dirección IP de origen con el fin de permitir el tráfico adecuado. El servicio IPSec interpreta el destino YO para crear un filtro para cada una de las direcciones IP del equipo. Cada uno de estos filtros se reflejará para permitir que el tráfico regrese al equipo de origen. Este enfoque significa que la regla del servidor HTTP permitirá que el tráfico que se origina en cualquier host de cualquier puerto de origen se conecte al puerto 80 del servidor IIS. El reflejo de esta regla permitirá que el tráfico TCP del puerto 80 del servidor IIS vaya a cualquier puerto de cualquier host.
  
Un servicio de cliente puede ser cualquier servicio realizado por el equipo en el que las directivas utilicen otro host. Por ejemplo, en el mapa de tráfico, el servidor puede necesitar que los servicios del cliente DNS realicen búsquedas de nombre para una de las aplicaciones web. En este ejemplo, se ha creado un filtro para permitir el tráfico a y desde los servidores DNS. Windows Server 2003 ofrece directivas mejoradas a través de Windows 2000 Server para este tipo de configuración, que permiten el tráfico al servidor DNS y a otros servidores de infraestructura. En Windows 2000, la directiva IPSec debe contener cada una de las direcciones IP del servidor DNS en la directiva. En Windows Server 2003, la directiva puede utilizar el DNS de nombre lógico, que se expandirá en un filtro para cada dirección IP del servidor DNS, en función de la configuración IP local del servidor.
  
**Nota**: las directivas IPSec que utilizan funciones de Windows Server 2003 como ésta última no deben asignarse a equipos que utilicen Windows 2000 o Windows XP.
  
El filtro de bloqueo reflejado de Cualquier dirección IP a Mi dirección IP bloqueará el resto del tráfico IP de unidifusión procedente o dirigido a una dirección IP del equipo. Este filtro es más general que los filtros específicos de protocolo y puerto definidos para DNS, HTTP y HTTPS. Dado que en Windows Server 2003 se han quitado las exenciones predeterminadas, este filtro buscará coincidencias y bloqueará los paquetes de difusión y multidifusión salientes, ya que la dirección IP de origen es Mi dirección IP y la dirección de destino coincide con Cualquier dirección IP. Sin embargo, tenga en cuenta que este filtro no busca coincidencias del tráfico de difusión y multidifusión entrante. La dirección de origen sería Cualquier dirección IP, pero la dirección de destino de un paquete de difusión o multidifusión no es una dirección IP específica del equipo, sino una dirección IP de difusión o multidifusión. Por lo tanto, esta regla no bloqueará el tráfico de difusión o multidifusión entrante en Windows Server 2003. Esta definición de filtro también es compatible con Windows 2000 y Windows XP. Sin embargo, sólo buscará coincidencias del tráfico IP de unidifusión. Estas plataformas no se han diseñado para buscar coincidencias de los paquetes de difusión y multidifusión con los filtros IPSec. Por lo tanto, se permitirán los paquetes de difusión y multidifusión entrantes y salientes aunque este filtro se aplique en equipos con Windows 2000 y Windows XP.
  
La última regla, Bloquear todo, muestra otra mejora de los filtros para Windows Server 2003. Esta regla no es compatible con Windows 2000 ni Windows XP. Esta regla bloquea el tráfico de difusión y multidifusión entrante y saliente, así como cualquier otro tráfico de unidifusión que no coincida con un filtro más específico. Si se utiliza esta regla, la regla anterior "Cualquier dirección IP a Me" no es necesaria.
  
Es importante indicar que si se aplicase una directiva de este tipo, el equipo no podría establecer comunicación con el servidor DHCP correspondiente para renovar una concesión, ni con los controladores de dominio, los servidores WINS, los sitios de revocación de listas CRL ni las estaciones de supervisión de servidores. Asimismo, esta directiva no permite que un administrador obtenga acceso a la administración remota mediante complementos MMC basados en RPC ni a una conexión con un cliente de Escritorio remoto. Observe también que si el servidor IIS de ejemplo tuviese dos tarjetas de interfaz de red (una para el acceso a Internet y otra para el acceso interno), todo el tráfico a través de ambas interfaces se filtraría de la misma forma. Por lo tanto, esta directiva debe personalizarse considerablemente para adaptarse a los entornos de producción. El tráfico de red se debe filtrar de forma diferente para la dirección IP interna o la subred. Las reglas de filtros utilizadas para solicitar la administración remota del cifrado IPSec desde estaciones de administración específicas también deberán utilizarse cuando sea posible para que otros servidores afectados no tengan acceso a los servidores a través de la interfaz interna, o capturen el tráfico de red de inicio de sesión administrativa para ataques sin conexión.
  
Si se requiere un servicio de cliente que no puede restringirse para la conexión con un servidor de destino concreto o con un número limitado de servidores de destino, el nivel de seguridad proporcionado por los filtros IPSec puede verse reducido considerablemente. En el siguiente ejemplo de mapa de tráfico de red, se agrega una regla, de modo que un administrador pueda utilizar un explorador web para tener acceso a cualquier sitio de Internet para obtener información de ayuda y descargar revisiones. Para ello es necesario un filtro de permiso estático saliente reflejado para el tráfico del puerto TCP 80 de destino.
  
**Tabla 11.2: Ejemplo de mapa de tráfico de red que permite la exploración web saliente**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Servicio</p></th>  
<th><p>Protocolo</p></th>  
<th><p>Puerto de origen</p></th>  
<th><p>Puerto de destino</p></th>  
<th><p>Dirección de origen</p></th>  
<th><p>Dirección de destino</p></th>  
<th><p>Acción</p></th>  
<th><p>Reflejo</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>ICMP entrante para TCP PMTU</p></td>
<td style="border:1px solid black;"><p>ICMP</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>NO</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>HTTP de servidor IIS entrante: 80</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>80</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>FTP de servidor IIS entrante: 21</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>21</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Servidor de terminal entrante</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>3389</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Todo el tráfico de Me a los DC del dominio</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>Nombre de dominio</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>UDP/TCP de DNS saliente</p></td>
<td style="border:1px solid black;"><p>UDP</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>53</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>DNS</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>UDP/TCP de DNS saliente</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>53</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>DNS</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>WINS saliente</p></td>
<td style="border:1px solid black;"><p>UDP</p></td>
<td style="border:1px solid black;"><p>137</p></td>
<td style="border:1px solid black;"><p>137</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>WINS</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>DHCP saliente</p></td>
<td style="border:1px solid black;"><p>UDP</p></td>
<td style="border:1px solid black;"><p>68</p></td>
<td style="border:1px solid black;"><p>67</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>DHCP</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>HTTP saliente: 80</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>80</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Bloquear todo</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>BLOQUEAR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
</tbody>  
</table>
  
Aunque este ejemplo de mapa de tráfico parece correcto, el resultado real es que la directiva no proporciona ninguna seguridad frente a un atacante que inicie una conexión entrante desde Cualquier dirección IP mediante el puerto TCP de origen 80. Este atacante puede obtener acceso a cualquier puerto TCP abierto a través del filtro de permiso entrante, y se permite la respuesta a través del filtro de permiso saliente de vuelta al puerto TCP de destino 80.
  
Cualquiera de las soluciones siguientes se podría utilizar para bloquear el ataque entrante:
  
-   Utilice reglas de filtrado IPSec adicionales que bloqueen la utilización del puerto 80 por parte de un atacante para obtener acceso entrante a los puertos abiertos.
  
-   Utilice un enrutador o servidor de seguridad de filtrado con estado de cliente que bloquee el tráfico entrante del puerto de origen 80 a menos que corresponda a una conexión saliente.
  
-   Además de esta directiva IPSec, configure el Firewall de Windows en el adaptador de red externo del servidor para que proporcione filtrado con estado para todo el tráfico saliente permitido por los filtros IPSec. Debido a que el Firewall de Windows se encuentra en una capa superior a IPSec, se debe configurar también para permitir el tráfico entrante de los puertos TCP 80 y 443 (aunque esta es la configuración predeterminada).
  
El ejemplo de mapa de tráfico en la siguiente tabla utiliza filtros IPSec adicionales que bloquean cualquier intento de obtener acceso a los puertos abiertos desde el puerto 80. En primer lugar, el comando Netstat -ano se utiliza para determinar qué puertos TCP deben estar abiertos en el servidor al que podría conectarse el atacante. La salida de este comando es similar a la siguiente:
  
```  
C:\\Documents and Settings\\testuser.domain.000&gt;netstat -ano Active Connections Proto  Local Address       Foreign Address     State         PID TCP    0.0.0.0:135         0.0.0.0:0           LISTENING     740 TCP    0.0.0.0:445         0.0.0.0:0           LISTENING     4 TCP    0.0.0.0:1025        0.0.0.0:0           LISTENING     884 TCP    0.0.0.0:1046        0.0.0.0:0           LISTENING     508 TCP    192.168.0.5:139     0.0.0.0:0           LISTENING     4 UDP    0.0.0.0:445         \*:\*                               4 UDP    0.0.0.0:500         \*:\*                               508 UDP    0.0.0.0:1026        \*:\*                               816 UDP    0.0.0.0:1029        \*:\*                               508 UDP    0.0.0.0:1051        \*:\*                               452 UDP    0.0.0.0:4500        \*:\*                               508 UDP    127.0.0.1:123       \*:\*                               884 UDP    192.168.0.5:123     \*:\*                               884 UDP    192.168.0.5:137     \*:\*                               4 UDP    192.168.0.5:138     \*:\*                               4  
```  
La regla se define para bloquear los ataques específicos del puerto TCP de origen 25 a cada puerto TCP abierto como se indica en la tabla a continuación:
  
**Tabla 11.3: Ejemplo de mapa de tráfico de red revisado que permite la exploración web saliente**

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
<col width="12%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th><p>Servicio</p></th>  
<th><p>Protocolo</p></th>  
<th><p>Puerto de origen</p></th>  
<th><p>Puerto de destino</p></th>  
<th><p>Dirección de origen</p></th>  
<th><p>Dirección de destino</p></th>  
<th><p>Acción</p></th>  
<th><p>Reflejo</p></th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>ICMP entrante para TCP PMTU</p></td>
<td style="border:1px solid black;"><p>ICMP</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>NO</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>HTTP de servidor IIS entrante: 80</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>80</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>FTP de servidor IIS entrante: 21</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>21</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Servidor de terminal entrante</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>3389</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Todo el tráfico de Me a los DC del dominio</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>Nombre de dominio</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>UDP/TCP de DNS saliente</p></td>
<td style="border:1px solid black;"><p>UDP</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>53</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>DNS</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>UDP/TCP de DNS saliente</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>53</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>DNS</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>WINS saliente</p></td>
<td style="border:1px solid black;"><p>UDP</p></td>
<td style="border:1px solid black;"><p>137</p></td>
<td style="border:1px solid black;"><p>137</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>WINS</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>DHCP saliente</p></td>
<td style="border:1px solid black;"><p>UDP</p></td>
<td style="border:1px solid black;"><p>68</p></td>
<td style="border:1px solid black;"><p>67</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>DHCP</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>HTTP saliente: 80</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>80</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>PERMITIR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Mitigación del ataque 80 de origen entrante</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>80</p></td>
<td style="border:1px solid black;"><p>135</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>BLOQUEAR</p></td>
<td style="border:1px solid black;"><p>NO</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Mitigación del ataque 80 de origen entrante</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>80</p></td>
<td style="border:1px solid black;"><p>139</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>BLOQUEAR</p></td>
<td style="border:1px solid black;"><p>NO</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Mitigación del ataque 80 de origen entrante</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>80</p></td>
<td style="border:1px solid black;"><p>445</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>BLOQUEAR</p></td>
<td style="border:1px solid black;"><p>NO</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Mitigación del ataque 80 de origen entrante</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>80</p></td>
<td style="border:1px solid black;"><p>1025</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>BLOQUEAR</p></td>
<td style="border:1px solid black;"><p>NO</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Mitigación del ataque 80 de origen entrante</p></td>
<td style="border:1px solid black;"><p>TCP</p></td>
<td style="border:1px solid black;"><p>80</p></td>
<td style="border:1px solid black;"><p>1046</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>YO</p></td>
<td style="border:1px solid black;"><p>BLOQUEAR</p></td>
<td style="border:1px solid black;"><p>NO</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Bloquear todo</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>CUALQUIERA</p></td>
<td style="border:1px solid black;"><p>BLOQUEAR</p></td>
<td style="border:1px solid black;"><p>SÍ</p></td>
</tr>  
</tbody>  
</table>
  
Este ejemplo muestra cómo crear filtros unidireccionales que bloqueen el tráfico entre un puerto de origen 80 y cualquier puerto activo del equipo, lo que bloquearía un ataque de entrada. Impide que se suplante la conexión de un puerto de origen 80 a los puertos necesarios para RPC, NetBT y SMB (CIFS).
  
Puede aplicar las directivas IPSec de varias maneras:
  
-   Aplicándolas en un equipo individual.
  
-   Adjuntándolas a una UO o dominio mediante una directiva de grupo.
  
-   Escribiendo una secuencia de comandos para el comando ipsec netsh y, a continuación, aplicando la secuencia de comandos en equipos seleccionados.
  
Es posible distribuir las directivas IPSec en función de la directiva de grupo. Sin embargo, cuando las directivas IPSec deben adaptarse a determinados equipos, puede ser más aconsejable utilizar directivas locales. Otra alternativa más fácil de administrar consiste en la combinación de la directiva local o basada en el dominio y la directiva persistente con secuencias de comandos NETSH IPSec. Concretamente, NETSH se debe utilizar para establecer una directiva persistente que ofrezca seguridad durante el inicio del equipo. Para obtener información más detallada, consulte la sección "Assigning Domain-based, OU-Level, and Local IPSec Policies" en el capítulo 6, "Deploying IPSec" en el *Windows* *Server* *2003 Deployment Kit: Deploying Network Services.*
  
###### Negociación de la protección IPSec del tráfico
  
La integración del protocolo IKE con el filtrado IPSec permite la negociación automática basada en directivas de la protección cifrada IPSec para el tráfico IP de unidifusión que coincida con los filtros IPSec. Los paquetes protegidos mediante IPSec pueden utilizar el formato AH o el formato ESP con las opciones de seguridad determinadas según la configuración de las directivas. La utilización de directivas IPSec para negociar el transporte protegido mediante IPSec de las aplicaciones y los protocolos de capa superior ofrece las ventajas siguientes:
  
-   Defensa en profundidad frente a los ataques a la red. IPSec es un protocolo de seguridad maduro y moderno que fue diseñado por el Internet Engineering Task Force (IETF). Permite agregar una capa de protección segura en una capa por debajo de todas las comunicaciones IP de unidifusión, para aumentar la seguridad basada en la aplicación. De esta forma, IPSec ofrece protección frente a las vulnerabilidades de la seguridad de los protocolos de capa superior y puede reforzar en gran medida la seguridad de las comunicaciones. Por ejemplo, el protocolo de uso compartido de archivos SMB se emplea de forma generalizada para la réplica, transferencia de archivos, impresión y descarga de directivas de grupo del servicio de directorio Active Directory®. Sin embargo, SMB no ofrece privacidad. Todos los datos enviados en SMB están visibles para el observador pasivo de la red. SMB proporciona firma digital, si bien en algunos casos es probable que no sea necesaria, ya que un valor de configuración afecta a todas las rutas de comunicación de SMB. IPSec se puede aplicar para proteger una ruta o un conjunto de rutas de red específico. Se han identificado dos problemas de seguridad de SMB en Windows 2000 y Windows XP. Aunque Microsoft dispone actualmente de soluciones admitidas para estos problemas de seguridad, es posible mejorar la seguridad si utiliza IPSec como primera capa de protección frente a los ataques a SMB o a otros protocolos. Si desea obtener más información acerca de las dos vulnerabilidades de la seguridad de SMB identificadas y las soluciones compatibles con Windows 2000 y Windows XP, consulte los artículos siguientes de Microsoft Knowledge Base:
  
    -   “[MS02-070: Flaw in SMB Signing May Permit Group Policy to Be Modified](http://support.microsoft.com/?kbid=329170)” en http://support.microsoft.com/?kbid=329170.
  
    -   “[MS02-045: Unchecked Buffer in Network Share Provider May Lead to Denial-of-Service](http://support.microsoft.com/?kbid=326830)” en http://support.microsoft.com/?kbid=326830.
  
-   Autenticación y cifrado basados en host de todo el tráfico entre dos o más equipos, para garantizar que el propietario administrativo de los datos mantenga el control completo de los mismos cuando éstos recorran la red. Los datos del tráfico de red contienen activos de información básicos que pertenecen a los propietarios. El robo de esta información mientras fluye a través de la red podría tener repercusiones graves en la empresa o en la misión de la organización. Si las relaciones de confianza empresariales y legales que administran la confianza y la integridad de la ruta de red no se aplican perfectamente o se ven comprometidas en silencio, las comunicaciones cifradas mediante IPSec permanecen protegidas.
  
-   Transversal de servidor de seguridad sencillo y protegido. Los servidores de seguridad interpretan los numerosos protocolos utilizados en las comunicaciones entre controladores de dominio, entre servidores o entre clientes y servidores únicamente como tráfico ESP IPSec (protocolo 50) o como tráfico AH (protocolo 51). Los servidores de seguridad se pueden configurar para permitir únicamente el tráfico para dichos protocolos (y el tráfico IKE), y estos protocolos se refuerzan frente a los ataques.
  
-   La utilización por parte de IPSec del algoritmo de cifrado 3DES y el algoritmo de integridad SHA1 está certificada por Common Criteria y FIPS 140-1. Numerosas instituciones gubernamentales, militares, financieras y sanitarias requieren la utilización de algoritmos certificados por Common Criteria o FIPS 140-1 para proteger su tráfico. El algoritmo de cifrado de secuencia RC4 se utiliza de manera predeterminada para cifrar el tráfico a través de la mayoría de protocolos de Windows, como RPC, el protocolo de autenticación Kerberos y el protocolo ligero de acceso a directorios (LDAP). RC4 no forma parte de los algoritmos certificados por Common Criteria o FIPS 140-1.
  
-   Al tratarse de una solución de Windows basada en software, IPSec resulta más rentable para proteger las comunicaciones de host a host que una solución basada en hardware. Las soluciones de seguridad basadas en hardware, como una red privada virtual (VPN) o una línea alquilada privada, pueden ser más caras que la utilización de Windows IPSec.
  
-   IPSec puede proporcionar una utilización inferior de la CPU que las medidas de seguridad específicas del protocolo, como la firma SMB. Los adaptadores de red que descargan procesamiento IPSec aceleran las operaciones de cifrado utilizadas para proteger los paquetes IPSec, minimizando así los costos de rendimiento del cifrado. En consecuencia, las conexiones TCP/IP protegidas mediante IPSec pueden lograr el mismo rendimiento que las conexiones TCP/IP que no están protegidas mediante IPSec, aunque estos adaptadores pueden implicar costos de equipo adicionales. Si no es posible utilizar estos adaptadores, el cifrado IPSec aumentará la carga de CPU de un controlador de dominio. Esta carga aumentada de CPU puede precisar o no de una capacidad adicional de CPU, en función de los CPU disponibles y de la cantidad de tráfico de red. Necesitará realizar pruebas de rendimiento para valorar el impacto de rendimiento en los controladores de dominio de escenarios concretos.
  
##### Impacto potencial
  
IPSec es una herramienta que puede utilizar para reforzar un servidor contra ataques a la red. No debe considerarse la única herramienta ni tampoco una solución completa. El filtrado IPSec no se ha diseñado para sustituir la necesidad de filtros de un enrutador o servidor de seguridad perimetral completo. Sólo se recomienda en los escenarios de filtrado sencillo de paquetes, para reforzar los clientes y servidores en los que los filtros estáticos pueden resultar eficaces. Asimismo, el filtrado IPSec se ha diseñado para aplicar una directiva basada en directorio a muchos equipos. Por lo tanto, el complemento de administración de directivas IPSec de MMC no puede ofrecer información detallada durante el proceso de configuración sobre el modo en que una directiva se aplicará a un equipo específico. Las limitaciones del filtrado IPSec son las siguientes:
  
-   No es posible aplicar filtros IPSec para una aplicación concreta. Sólo se pueden definir para los protocolos y puertos que utilice la aplicación.
  
-   Los filtros IPSec son estáticos. No proporcionan filtrado del tráfico saliente "con estado". Para permitir el tráfico de red saliente, generalmente es necesario un filtro de permiso saliente y entrante estático. Por lo tanto, IPSec no ofrece protección frente a un atacante que utilice el filtro de permiso entrante estático para obtener acceso a cualquier puerto abierto. Los filtros de permiso salientes sólo deben ser específicos de la dirección IP o el intervalo que los necesite.
  
-   Los filtros IPSec no establecen diferencias entre los distintos tipos de mensajes ICMP.
  
-   Los filtros IPSec no realizan inspecciones del contenido de los paquetes IP para detectar intrusos.
  
-   Los filtros IPSec pueden superponerse, pero no se pueden ordenar manualmente. El servicio IPSec realiza un cálculo de importancia interno que proporciona un orden de filtro automático. La parte del filtro que tiene preferencia es la dirección, seguida del protocolo y, por último, de los puertos de origen y destino.
  
-   Los filtros IPSec no son específicos de la interfaz. Pueden configurarse para ser específicos de la dirección IP, pero se buscarán coincidencias entre todo el tráfico de cada interfaz y la lista de filtros.
  
-   Los filtros IPSec no se pueden configurar explícitamente como entrantes o salientes. La dirección entrante y saliente se determina automáticamente en función de las direcciones especificadas en el filtro. En algunos casos, se generan automáticamente filtros entrantes y salientes.
  
-   La directiva IPSec no admite filtros duplicados.
  
-   Aunque Windows Server 2003 ha mejorado considerablemente el rendimiento del filtrado IPSec, el filtrado basado en host puede aumentar la carga de la CPU para los volúmenes de tráfico muy elevados. Un servidor de seguridad o enrutador de cliente optimizado puede filtrar el tráfico con mayor rapidez.
  
Cuando el filtrado IPSec (u otro dispositivo de red) bloquea el tráfico de red, puede provocar un comportamiento inusual de la aplicación y generar mensajes de eventos. El filtrado IPSec no proporciona un registro de fácil lectura del tráfico entrante y saliente interrumpido. Las capturas del Monitor de red (Netmon) del tráfico de red no permiten ver el tráfico saliente que está bloqueado. Aunque Netmon permite ver el tráfico entrante bloqueado, en el archivo de captura no se indica que se haya interrumpido un paquete determinado. Por lo tanto, un diagnóstico efectivo dependerá del conocimiento del comportamiento habitual de la aplicación, de los eventos y de los flujos de tráfico de red cuando no se ha asignado la directiva IPSec.
  
Asimismo, el diseño correcto de filtros IPSec para el tráfico de la aplicación puede depender del análisis detallado de los flujos de tráfico de red para conocer el modo en que la aplicación utiliza la red. Por ejemplo, el protocolo SMB utiliza el puerto TCP 139 para la transferencia de archivos y para el uso compartido de impresoras y archivos. Si IPSec bloquea este puerto, SMB también puede utilizar el puerto TCP 445. Otro ejemplo es cuando una aplicación requiere múltiples flujos de tráfico de red para diferentes destinos. Generalmente, SMB y otros protocolos autentican al usuario; esto puede provocar que el equipo localice e intercambie el tráfico Kerberos con el controlador de dominio. El protocolo Kerberos utiliza DNS UDP 53 o TCP 53 para descubrir una lista de direcciones IP de controladores de dominio y, a continuación, LDAP UDP 389 y UPD y el puerto TCP 88 para descubrir prácticamente cualquiera de las direcciones IP de controladores de dominio. Por lo tanto, un error de impresión puede deberse en realidad a un paquete bloqueado del controlador de dominio. Algunos protocolos, como RPC, utilizan una amplia gama de puertos TCP, que se determinan de forma dinámica al iniciar un equipo o al ejecutar una aplicación, lo que significa que las aplicaciones RPC no se pueden controlar de forma eficaz mediante el filtrado estático en los puertos, excepto cuando la aplicación RPC proporciona una configuración para requerir el uso de un puerto estático.
  
En Windows 2000 y Windows XP, las exenciones predeterminadas para los filtros especificados en la configuración de directivas se han diseñado para los tipos de tráfico de red IP que no pueden protegerse mediante IKE (paquetes IP de unidifusión y multidifusión), que deben estar exentos de la calidad de servicio (QoS) que se proporciona para el tráfico IPSec (protocolo RSVP), y que deben ser necesarios para que el sistema IPSec funcione (el propio IKE y el protocolo Kerberos como método de autenticación IKE). Aunque se ha proporcionado una clave de registro para quitarlas, estas exenciones a menudo no se deshabilitan cuando los filtros IPSec se han utilizado para escenarios de servidor de seguridad de permiso y bloqueo. Por lo tanto, Windows Server 2003 sólo proporciona una exención para el tráfico IKE. Microsoft recomienda quitar las exenciones predeterminadas de todos los escenarios IPSec que utilizan Windows 2000 y Windows XP. Para obtener más información acerca de las exenciones predeterminadas, consulte el artículo de Microsoft Knowledge Base "[IPSec Default Exemptions Can Be Used to Bypass IPSec Protection in Some Scenarios](http://support.microsoft.com/?kbid=811832)” en http://support.microsoft.com/?kbid=811832 y el artículo de Microsoft Knowledge Base "[IPSec default exemptions are removed in Windows Server 2003](http://support.microsoft.com/?kbid=810207)" en http://support.microsoft.com/?kbid=810207.
  
Cuando un equipo con Windows 2000 se conecta a Internet, un filtro de permiso saliente reflejado (como el puerto 80, que se explicó anteriormente en este capítulo) permite que un atacante tenga acceso desde Internet a cualquier puerto TCP abierto del servidor mediante el puerto de origen. Por lo tanto, un error en la configuración de IPSec puede provocar la pérdida de la seguridad esperada. Las configuraciones deben comprobarse para garantizar que proporcionen la seguridad y la protección esperadas frente a los ataques.
  
Un riesgo de seguridad que permite que un atacante obtenga acceso al sistema local o al administrador local podría permitirle deshabilitar o cambiar la directiva IPSec.
  
IPSec en Windows 2000 no ofrece filtrado completo durante el inicio del equipo. Hay un breve intervalo de tiempo en el que la pila TCP/IP es sensible. Un ataque automatizado podría tener acceso potencialmente a puertos de la aplicación que, de lo contrario, estarían bloqueados por la directiva IPSec. En la mayoría de los casos, las aplicaciones no pueden iniciar el proceso de las conexiones antes de establecer el filtrado IPSec. Para lograr el máximo nivel de seguridad mediante el filtrado IPSec, debe desconectar el equipo de la red durante el reinicio.
  
Windows Server 2003 proporciona una primera directiva de inicio que el controlador de IPSec utiliza cuando TCP/IP lo carga al iniciar el equipo. Cuando se inicia el servicio IPSec, éste aplica inmediatamente la directiva persistente. Si es posible determinar una asignación de directiva local o de dominio, el servicio aplica esta asignación de directiva además de la directiva persistente. Por lo tanto, una secuencia de comandos IPSec NETSH que configure una directiva persistente predeterminada que garantice la seguridad (por ejemplo, el bloqueo de todo el tráfico excepto el tráfico de administración), puede ofrecer protección total durante la transición del inicio a la directiva IPSec local o asignada por el dominio. Dispone de más información en la Ayuda en línea de Windows Server 2003 y en el Kit de implementación.
  
No obstante, Windows 2000 y Windows Server 2003 no están diseñados para permitir la configuración de dependencias de servicio en el inicio del servicio Agente de directivas IPSec. La configuración de una dependencia de servicio no garantiza de forma efectiva que los filtros se establezcan antes de iniciar el servicio dependiente.
  
Windows Server 2003 y Windows XP con SP2 proporcionan el servicio del Firewall de Windows, que realiza el filtrado con estado del tráfico saliente y proporciona controles básicos del acceso entrante a los puertos y los tipos de mensajes ICMP. El Firewall de Windows proporciona también un registro legible de los paquetes bloqueados entrantes y salientes. Los administradores deberán investigar las capacidades del Firewall de Windows para determinar si satisfacen sus necesidades de filtrado del tráfico. El filtrado con estado que proporciona el Firewall de Windows se puede utilizar en combinación con el filtrado IPSec para ofrecer protección cuando IPSec deba configurarse para utilizar filtros salientes reflejados que permitan el tráfico. En la medida de lo posible, debe utilizarse el filtrado de servidor de seguridad o enrutador de cliente como primera línea de defensa.
  
Merece la pena considerar el uso de un sistema de detección de intrusos basado en host y otros sistemas antivirus para detectar y protegerse potencialmente frente a la infección y los ataques en las aplicaciones y el tráfico de red permitido. Un servidor de seguridad de extremo o basado en host de terceros puede proporcionar la mejor solución para las necesidades de filtrado complejas.
  
###### Negociación de la protección IPSec del tráfico
  
Aunque la protección IPSec total puede mejorar considerablemente la seguridad, la implementación de comunicaciones protegidas mediante IPSec en su red implica costos administrativos y de aprendizaje adicionales. Puede implicar también costos adicionales de hardware si es necesario adquirir hardware IPSec o adaptadores de red de descarga o bien aumentar la capacidad de CPU. Por lo tanto, antes de implementar IPSec para un determinado escenario, considere y analice detenidamente las posibles amenazas de seguridad que IPSec pretende corregir, los requisitos de seguridad, los costos de la implementación de IPSec y los beneficios empresariales esperados.
  
La implementación de IPSec con AH implica un aumento de la carga para administrar una configuración IPSec cliente/servidor, así como la administración de un método de confianza mutua entre los equipos cliente/servidor. Si ambos equipos están siempre en el mismo dominio o en dominios de confianza mutua, la directiva de grupo puede ofrecer la configuración necesaria de la directiva IPSec, y la autenticación Kerberos puede establecer confianza para las asociaciones de seguridad de IPSec. Si los equipos no pueden utilizar la autenticación Kerberos, se pueden emplear certificados de equipo o una clave de autenticación previamente compartida. Sin embargo, en esta guía no se recomienda utilizar claves de autenticación previamente compartidas, ya que el valor de la clave se almacena sin protección en la configuración de la directiva IPSec.
  
Aunque únicamente pueden leer la directiva IPSec local los administradores que la han definido, la directiva almacenada en Active Directory deberá ser accesible a todos los equipos del dominio. Por lo tanto, resulta difícil mantener la privacidad del valor de la clave previamente compartida. Microsoft recomienda el uso de certificados digitales cuando el protocolo Kerberos no se puede utilizar para la autenticación de IKE. La directiva IPSec debe designarse para proteger todo el tráfico o para negociar IPSec sólo en puertos TCP o UDP específicos. La directiva IPSec del cliente generalmente se debe configurar con la dirección IP estática del servidor. Si necesita IPSec en el servidor, se negará el acceso a los equipos cliente que no dispongan de una configuración de directiva IPSec compatible y un método de confianza mutua.
  
Si desea obtener más información acerca de la implementación de Windows IPSec, consulte el sitio web de [Windows 2000](http://www.microsoft.com/windows2000/technologies/communications/ipsec/default.asp) en la dirección http://www.microsoft.com/windows2000/technologies/communications/ipsec/default.asp.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Configuración del Firewall de Windows
  
Un servidor de seguridad de Internet puede ayudar a evitar que los intrusos tengan acceso a su equipo desde Internet. Windows XP con SP2 y Windows Server 2003 con SP1 incluyen el Firewall de Windows, que es un servidor de seguridad integrado que puede proporcionar un nivel más de protección frente a ataques basados en la red, como por ejemplo, gusanos y ataques de denegación de servicio.
  
1.  Haga clic en **Inicio** y, a continuación, en **Panel de control**.
  
2.  Haga clic en **Firewall de Windows**.    
  
3.  Haga clic en el botón **activo (recomendado)**.
  
4.  Si es necesario, haga clic en la ficha **Excepciones** y configure las excepciones de los protocolos que desee permitir a través del servidor de seguridad.
  
5.  Haga clic en **Aceptar** para activar el Firewall de Windows.
  
El Firewall de Windows no tiene toda la gama de funciones de muchos productos de terceros, porque sólo ha sido creado con funciones básicas de prevención de intrusiones. El Firewall de Windows no permite que las personas reúnan datos acerca del equipo, y bloquea los intentos no solicitados de conexión. Sin embargo, no realiza un filtrado exhaustivo del tráfico saliente.
  
El Firewall de Windows agrega varias mejoras importantes con respecto al Servidor de seguridad de conexión a Internet (ICF) incluido en versiones anteriores de Windows. En particular, el Firewall de Windows se puede administrar centralmente a través de la directiva de grupo. Para obtener información acerca de las herramientas de administración y la configuración disponibles, consulte las notas del producto "[Deploying Windows Firewall Settings for Microsoft Windows XP with Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4454e0e1-61fa-447a-bdcd-499f73a637d1&displaylang=en)" en www.microsoft.com/downloads/details.aspx?  
FamilyID=4454e0e1-61fa-447a-bdcd-499f73a637d1&DisplayLang=en.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Información adicional
  
Los siguientes vínculos proporcionan información adicional acerca de las medidas adicionales de refuerzo en Windows Server 2003 y Windows XP.
  
-   La [*Guía de seguridad de Windows Server 2003*](http://go.microsoft.com/fwlink/?linkid=14845) en http://go.microsoft.com/fwlink/?LinkId=14845 proporciona una orientación completa para la configuración y administración de las funciones de seguridad de Windows Server 2003.
  
-   La guía [*Exchange Server Security Hardening Guide*](http://go.microsoft.com/fwlink/?linkid=37804)* *disponible para su descarga* *en http://go.microsoft.com/fwlink/?LinkId=37804 describe los procedimientos de refuerzo para equipos con Exchange Server en un dominio de Active Directory.
  
-   La [*Guía de consolidación de seguridad de Microsoft Internet Security and Acceleration (ISA) Server 2004*](http://download.microsoft.com/download/c/e/c/cecc8742-2102-42d4-9fc7-6b641bebbf56/isasecurityguide.doc) disponible para su descarga en http://download.microsoft.com/download/c/e/c/cecc8742-2102-42d4-9fc7-6b641bebbf56/ISASecurityGuide.doc describe los pasos necesarios para reforzar la seguridad de un equipo con ISA Server 2004, independientemente de si es un miembro de dominio.
  
-   Las notas del producto "[Deploying Windows Firewall Settings for Microsoft Windows XP with Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4454e0e1-61fa-447a-bdcd-499f73a637d1&displaylang=en)" en www.microsoft.com/downloads/  
    details.aspx?FamilyID=4454e0e1-61fa-447a-bdcd-499f73a637d1 describen un proceso para ayudarle a determinar la configuración apropiada para el Firewall de Windows y cómo implementarla.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Capítulo 12: Conclusión
  
En esta guía se han explicado las contramedidas de seguridad más importantes que están disponibles en Microsoft® Windows Server™ 2003 con SP1 y Microsoft Windows® Profesional de XP con SP2. Puede crear una plantilla de seguridad e importarla a un objeto de directiva de grupo vinculado a la unidad organizativa (UO) principal del servidor miembro para administrar la mayoría de los valores de configuración recomendados. Se pueden implementar otras configuraciones a través de las secciones de Plantillas administrativas (ADM) de la Directiva de grupo. No obstante, debido a que existen algunos procedimientos de consolidación que no se pueden aplicar mediante la Directiva de grupo, esta guía analiza también algunos parámetros de configuración manual.
  
### Información adicional
  
-   Para obtener más información acerca de la seguridad y la privacidad en Microsoft, consulte la página de [seguridad](http://www.microsoft.com/security) en wwww.microsoft.com/security.
  
-   Para obtener más información sobre las instrucciones de seguridad autorizadas de Microsoft, consulte las [Prácticas recomendadas de seguridad](http://www.microsoft.com/technet/security/secnews/articles/enterprisesecbp.mspx) en www.microsoft.com/technet/security/secnews/articles/enterprisesecbp.msp.
  
-   Para obtener información acerca de los [diez mandamientos de la seguridad](http://www.microsoft.com/technet/archive/community/columns/security/essays/10imlaws.mspx) consulte www.microsoft.com/technet/archive/community/columns/security/essays/10imlaws.msp.
  
-   Para obtener más información acerca de la seguridad en [Windows Server 2003](http://www.microsoft.com/technet/security/prodtech/windowsserver2003.mspx), consulte www.microsoft.com/technet/security/prodtech/windowsserver2003.msp.
  
-   Para obtener información acerca de cómo delegar la administración del servicio de directorios Active Directory®, consulte "[Design Considerations for Delegation of Administration in Active Directory](http://www.microsoft.com/technet/prodtechnol/windows2000serv/technologies/activedirectory/plan/addeladm.mspx)" en www.microsoft.com/technet/prodtechnol/windows2000serv/technologies/activedirectory/plan/addeladm.msp.
  
-   Para obtener más información sobre los tipos de ataques a la red comunes, consulte "[Common Types of Network Attacks](http://www.microsoft.com/resources/documentation/windows/2000/server/reskit/en-us/cnet/cndb_ips_ddui.asp)", extraído del *Kit de recursos de Windows 2000 Server*, disponible en línea en www.microsoft.com/resources/documentation/Windows/2000/server/reskit/  
    en-us/cnet/cndb\_ips\_ddui.asp.
  
-   Para obtener más información acerca de cómo reforzar la pila TCP/IP de Windows Server 2003, consulte el artículo de Microsoft Knowledge Base "[Cómo reforzar la pila TCP/IP contra ataques de denegación de servicio en Windows Server 2003](http://support.microsoft.com/?scid=324270)" en http://support.microsoft.com/?scid=324270 .
  
-   Para obtener más información sobre cómo consolidar la configuración para aplicaciones Windows Sockets, consulte el artículo de Microsoft Knowledge Base "[Internet Server Unavailable Because of Malicious SYN Attacks](http://support.microsoft.com/?scid=142641)" en http://support.microsoft.com/?scid=142641.
  
-   Para obtener más información acerca de la ubicación de los archivos .adm, consulte el artículo de Microsoft Knowledge Base "[Ubicación de archivos ADM (plantilla administrativa) en Windows](http://support.microsoft.com/?scid=228460)" en http://support.microsoft.com/?scid=228460.
  
-   Para obtener más información acerca de las Directivas de grupo, incluida una lista de rutas de acceso y valores para todas las configuraciones que se almacenan en el registro y que están disponibles para cada versión de Windows, consulte “[Group Policy Settings Reference for Windows Server 2003 with Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7821c32f-da15-438d-8e48-45915cd2bc14)” en www.microsoft.com/downloads/details.aspx?FamilyId=7821C32F-DA15-438D-8E48-45915CD2BC14.
  
-   Para obtener más información acerca de la arquitectura subyacente de la creación, edición y procesamiento de plantillas de seguridad, consulte “[How Security Settings Extension Works](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/techref/f546e58e-8473-4985-a05d-0b038dea4a9f.mspx)” en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/TechRef/  
    f546e58e-8473-4985-a05d-0b038dea4a9f.mspx Este artículo incluye información detallada acerca del almacenamiento y la prioridad de las directivas de grupo, además de describir el modo en que algunas configuraciones persisten incluso cuando una directiva de grupo determinada ya no se aplica a un equipo (lo que coloquialmente suele denominarse "tatuar").
  
-   Para obtener más información acerca de cómo personalizar la interfaz de usuario del Editor de configuración de seguridad, consulte el artículo de Microsoft Knowledge Base "[Cómo agregar configuraciones personalizadas del Registro al Editor de configuración de seguridad](http://support.microsoft.com/?scid=214752)" en http://support.microsoft.com/?scid=214752.
  
-   Para obtener más información acerca de cómo crear archivos de plantillas administrativas personalizadas en Windows, consulte el artículo de Microsoft Knowledge Base "[Cómo crear plantillas administrativas personalizadas en Windows 2000](http://support.microsoft.com/?scid=323639)" en http://support.microsoft.com/?scid=323639.
  
-   Para obtener más información acerca de cómo garantizar que las configuraciones del nivel de autenticación de LAN Manager más seguras funcionen en redes con una mezcla de equipos con Windows 2000 y Windows NT® 4.0, consulte el artículo de Microsoft Knowledge Base "[Problemas de autenticación en Windows 2000 con niveles de NTLM 2 por encima de 2 en un dominio de Windows NT 4.0](http://support.microsoft.com/?scid=305379)" en http://support.microsoft.com/?scid=305379.
  
-   Para obtener más información acerca de los niveles de compatibilidad de LAN Manager, consulte el artículo de Microsoft Knowledge Base "[Incompatibilidades de clientes, servicios y programas que pueden darse al modificar la configuración de seguridad y las asignaciones de derechos de usuario](http://support.microsoft.com/?scid=823659)" en http://support.microsoft.com/?scid=823659.
  
-   Para obtener más información acerca de la autenticación NTLMv2, consulte el artículo de Microsoft Knowledge Base "[Cómo habilitar la autenticación NTLM 2](http://support.microsoft.com/?scid=239869)" en http://support.microsoft.com/?scid=239869.
  
-   Para obtener más información acerca de la configuración predeterminada de los servicios en Windows Server 2003, consulte la página [Configuración predeterminada de los servicios](http://www.microsoft.com/resources/documentation/windowsserv/2003/standard/proddocs/en-us/sys_srv_default_settings.asp) en www.microsoft.com/resources/documentation/windowsserv/2003/standard/proddocs/en-us/sys\_srv\_default\_settings.asp.
  
-   Para obtener más información acerca de la implementación de tarjetas inteligentes en Windows Server 2003, consulte la página [Windows Server 2003 Smart Card](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/smrtcard.mspx) en Microsoft TechNet en www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/smrtcard.msp.
  
-   Para obtener más información acerca de las directivas de auditoría en Windows Server 2003, consulte la página [Auditing Policy](http://www.microsoft.com/technet/prodtechnol/windowsserver2003/library/serverhelp/6847e72b-9c47-42ab-b3e3-691addac9f33.mspx) en www.microsoft.com/technet/prodtechnol/windowsserver2003/library/ServerHelp/  
    6847e72b-9c47-42ab-b3e3-691addac9f33.mspx.
  
-   Para obtener más información acerca de la asignación de derechos de usuario en Windows Server 2003, consulte la página "[Asignación de derechos de usuario](http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/uratopnode.mspx)" en www.microsoft.com/resources/documentation/windows/  
    xp/all/proddocs/en-us/uratopnode.mspx.
  
-   Para obtener más información acerca de cómo proteger los Servicios de Terminal Server, consulte “[Securing Windows 2000 Terminal Services](http://www.microsoft.com/technet/prodtechnol/win2kts/maintain/optimize/secw2kts.mspx)”. La información en este artículo es también pertinente para Windows Server 2003, y está disponible en www.microsoft.com/technet/prodtechnol/win2kts/maintain/optimize/secw2kts.asp.
  
-   Para obtener más información acerca de cómo restaurar la configuración de seguridad predeterminada de forma local, consulte el artículo de Microsoft Knowledge Base "[Cómo devolver la configuración de seguridad a los valores predeterminados](http://support.microsoft.com/?scid=313222)” en http://support.microsoft.com/?scid=313222.
  
-   Para obtener más información acerca de cómo restaurar la configuración de seguridad predeterminada en los objetos de directiva de grupo del domino integrados, consulte el artículo de Microsoft Knowledge Base "[Cómo restablecer derechos de usuario en la directiva de grupo del dominio predeterminada en Windows Server 2003](http://support.microsoft.com/?scid=324800)" en http://support.microsoft.com/?scid=324800.
  
-   Para obtener más información sobre la seguridad de los distintos sistemas operativos Windows, consulte [*Microsoft Windows Security Resource Kit*](http://www.microsoft.com/learning/en/us/books/6815.aspx). La información sobre la compra de este libro está disponible en Microsoft Press en www.microsoft.com/MSPress/books/6418.asp.
  
-   Para obtener más información acerca del [Kit de recursos de Office XP](http://www.microsoft.com/office/ork/xp/default.htm) o para descargar las [Herramientas del kit de recursos de Office](http://www.microsoft.com/office/orkarchive/xpddl.htm), visite www.microsoft.com/office/ork/xp/default.htm y www.microsoft.com/office/ork/xp/appndx/appc00.htm.
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Agradecimientos
  
El grupo Microsoft Solutions for Security and Compliance (MSSC) desea agradecer y reconocer la labor realizada por el equipo que elaboró la guía *Amenazas y contramedidas: configuración de seguridad en Windows Server 2003 y Windows XP*. Las personas que se citan a continuación fueron responsables directos o contribuyeron de forma decisiva en la redacción, elaboración y comprobación de esta solución.
  
### Autores
  
Mike Danseglio
  
Kurt Dillard
  
José Maldonado
  
Paul Robichaux *(3Sharp,* *LLC)*
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Colaboradores de contenido
  
Liam Colvin *(3Sharp,* *LLC)*
  
William Dixon *(V6 Security Inc.)*
  
Tony Dowler *(3Sharp,* *LLC)*
  
Eric Fitzgerald
  
Devin Ganger *(3Sharp,* *LLC)*
  
Jesper Johansson
  
Brad Warrender
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Director del programa
  
Bomani Siwatu
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Administrador de versiones
  
Flicka Crandell
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Evaluadores
  
Kenon Bliss *(Volt Information Sciences)*
  
Paresh Gujar *(Infosys Technologies)* 
  
Vince Humphreys *(Volt Information Sciences)*
  
Ashish Java *(Infosys Technologies)* 
  
Mehul Mediwala *(Infosys Technologies)* 
  
Rob Pike
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Editores
  
Reid Bannecker
  
John Cobb *(Volt Information Sciences)*
  
Jon Tobey *(Volt Information Sciences)*
  
Steve Wacker *(Wadeware LLC)*
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Revisores
  
Roger Abell *(Universidad del Estado de Arizona)*
  
Rich Benack
  
Susan Bradley *(MVP de SBS)*
  
Buz Brodin
  
Steve Clark
  
Curtis Clay III
  
Karel Dekyvere
  
Christine Duell *(Valente Solutions)*
  
Robert Hensing
  
Don McGowan
  
James Noyce
  
*  (Consultor principal,* *Business Critical*
  
*  Consulting)*
  
Paul Rojas
  
Debra Littlejohn Shinder *(MVP de seguridad)*
  
Tom Shinder
  
*  (MVP de ISA y seguridad, y consultor de TI*
  
*  TACTeam)*
  
Ben Smith
  
Jeff Williams
  
Jim Whitney *(Configuresoft)*
  
[](#mainsection)[Principio de la página](#mainsection)
  
### Otros colaboradores
  
Ignacio Avellaneda
  
Ganesh Balakrishnan
  
Tony Bailey
  
Nathan Buggia
  
Derick Campbell
  
Chase Carpenter
  
Jeff Cohen
  
John Dwyer
  
Karl Grunwald
  
Joanne Kennedy
  
Karina Larson *(Volt Information Sciences)*
  
Chrissy Lewis *(Siemens Business Services)*
  
Kelly McMahon *(Content Master Ltd.)*
  
David Mowers
  
Jeff Newfeld
  
Rob Oikawa
  
Peter Meister
  
Bill Reid
  
Sandeep Sinha
  
Stacy Tsurusaki *(Volt Information Sciences)*
  
David Visintainer *(Volt Information Sciences*)
  
Rob Wickham
  
Graham Whiteley
  
Lori Woehler
  
Jay Zhang
  
A petición de Microsoft, el centro Center for Internet Security (CIS) y el instituto National Institute of Standards and Technology (NIST) del Departamento de Comercio de Estados Unidos también han participado en la revisión final de estos documentos de Microsoft y han proporcionado comentarios, que se han incorporado en la versiones publicadas.
  
[](#mainsection)[Principio de la página](#mainsection)
  
**Descargar**
  
[Obtenga la guía Introducción a las amenazas y contramedidas](http://www.microsoft.com/spain/technet/recursos/articulos/secmod48.mspx)
  
**Notificaciones de actualizaciones**
  
[Suscríbase para obtener más información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)
  
**Comentarios**
  
[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?subject=guía%20introducción%20a%20las%20amenazas%20y%20contramedidas:%20configuración%20de%20la%20seguridad%20en%20windows%20server%202003%20y%20windows%20xp)
  
[](#mainsection)[Principio de la página](#mainsection)
