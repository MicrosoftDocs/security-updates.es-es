---
TOCTitle: Cómo admitir el inicio de sesión de tarjeta inteligente en conexiones de acceso remoto VPN
Title: Cómo admitir el inicio de sesión de tarjeta inteligente en conexiones de acceso remoto VPN
ms:assetid: '8a7bcb4b-3c92-4c44-a9aa-be5bb20e7c62'
ms:contentKeyID: 20200266
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc875840(v=TechNet.10)'
---

Cómo admitir el inicio de sesión de tarjeta inteligente en conexiones de acceso remoto VPN
==========================================================================================

Publicado: 29/08/2006

##### En esta página

[](#edaa)[Introducción](#edaa)
[](#ecaa)[Tecnologías de las tarjetas inteligentes](#ecaa)
[](#ebaa)[Inicio de sesión de tarjeta inteligente en un escenario de VPN de acceso remoto](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Introducción

Los avances en tecnologías de comunicación, determinados por la necesidad de costos reducidos y el mantenimiento de la capacidad competitiva en un mercado en expansión, permiten a las organizaciones no sólo mantener canales de comunicación las 24 horas del día, siete días a la semana, sino también proporcionar conectividad a los datos y servicios de la empresa desde una ubicación remota.

Internet permite a las organizaciones y a los trabajadores usar equipos para comunicarse y compartir datos en todo el mundo y ofrece ventajas como la accesibilidad, la escalabilidad, el rendimiento y una reducción de los costos relacionados con el negocio. Sin embargo, Internet no es un entorno seguro y resulta potencialmente hostil para las organizaciones que operan en él. El reto al que se enfrentan las organizaciones es utilizar las ventajas que Internet proporciona al tiempo que mantienen los niveles necesarios de seguridad de comunicación y datos.

Las redes privadas virtuales (VPN) permiten a las organizaciones utilizar Internet al tiempo que limitan la exposición de los canales de datos y comunicaciones; esto se logra al proporcionar varias características de seguridad, entre ellas, la autenticación fiable y los mecanismos de cifrado.

#### Quién debería leer esta guía

Esta guía está destinada a profesionales de TI (tecnologías de la información) responsables de la implementación de un servicio VPN en sus entornos de red.

La información de esta guía es aplicable a las pequeñas y medianas empresas que deben ofrecer un acceso remoto fiable a sus redes.

#### Información general

Al configurar un acceso VPN remoto a los recursos de red, puede utilizarse el mismo conjunto de credenciales que se utiliza para tener acceso a la red desde el lugar de trabajo: una contraseña y nombre de usuario de red. Sin embargo, puede no ser la solución más segura. Las tarjetas de presentación o la documentación de la empresa incluyen con frecuencia nombres de usuario, por ejemplo. También son susceptibles de ataques de prueba y error. Si hay terceros que conocen su nombre de usuario, su contraseña seguirá siendo el único mecanismo de seguridad que protege la red corporativa.

Los secretos simples, como las contraseñas, pueden ser controles de seguridad eficaces. Una contraseña larga formada por letras aleatorias, números y caracteres especiales puede ser muy difícil de descifrar. Además, las frases codificadas ofrecen una mejor seguridad que las contraseñas simples.

Desgraciadamente, los usuarios no siempre pueden recordar datos confidenciales complejos y pueden optar por anotarlos. Cuando la complejidad de la contraseña no tiene asociada ninguna restricción, los usuarios tienden a crear contraseñas fáciles de recordar y, por tanto, fáciles de adivinar.

Las soluciones de contraseña y nombre de usuario se denominan de una fase porque sólo se utiliza algo conocido para tener acceso a la red. Los sistemas de autenticación de varias fases superan los problemas que presenta la autenticación de una fase al combinar una serie de requisitos, entre otros:

-   Algo que el usuario conoce, como una contraseña o un número de identificación personal (NIP).

-   Algo que el usuario tiene, como un símbolo (token) de hardware o una tarjeta inteligente.

-   Algo que el usuario es, como una huella dactilar o la exploración de retina.

Las tarjetas inteligentes y los NIP asociados son una forma cada vez más popular, fiable y rentable de una autenticación en dos fases. Los usuarios deben tener sus tarjetas inteligentes y conocer los NIP para obtener acceso a los recursos de red. El requisito de dos fases reduce de forma significativa la posibilidad de obtener acceso no autorizado a la red de la organización.

#### Ventajas de VPN

Cuando la organización deba conectar redes que contengan datos confidenciales y de propietario a Internet para el acceso remoto, el mayor grado de conectividad incluye un notable riesgo para la seguridad.

En el entorno potencialmente hostil de Internet, la gravedad de la solución VPN aumenta ya que, además de los ahorros operativos potenciales, ayuda a mantener la seguridad relacionada con una infraestructura de red privada. Una solución VPN proporciona seguridad porque usa una conexión de túnel segura que cifra los datos y sólo permite que los usuarios autenticados obtengan acceso a la red corporativa.

Las VPN admiten una gran variedad de métodos de autenticación, protocolos de túnel y tecnologías de cifrado para mantener la seguridad de los datos de la empresa.

Los métodos de autenticación VPN incluyen:

-   Protocolo de autenticación de contraseña (PAP).

-   Protocolo de autenticación por desafío mutuo (CHAP).

-   Protocolo de autenticación por desafío mutuo de Microsoft® (MS-CHAP).

-   MS-CHAP versión 2 (MS-CHAP v2).

-   Protocolo de autenticación extensible (EAP).

Los protocolos VPN de túnel son:

-   Protocolo de túnel punto a punto (PPTP).

-   Protocolo de túnel de capa 2 (L2TP).

Los protocolos de cifrado de VPN son:

-   Cifrado punto a punto de Microsoft (MPPE).

-   Seguridad IP (IPsec).

Para admitir el mayor número de sistemas operativos de cliente de Microsoft, utilice una versión de MS-CHAP, PPTP y MPPE.

Si utiliza Microsoft Windows® 2000 o posterior, podrá proporcionar mayores niveles de seguridad mediante EAP, L2TP y IPsec.

Para obtener más información acerca de la autenticación, túnel y cifrado VPN, consulte el artículo [Red privada virtual: información general](http://www.microsoft.com/technet/prodtechnol/windows2000serv/plan/vpnoverview.mspx)de Microsoft TechNet en www.microsoft.com/technet/prodtechnol/windows2000serv/plan/vpnoverview.mspx (puede estar en inglés).

[](#mainsection)[Principio de la página](#mainsection)

### Tecnologías de las tarjetas inteligentes

Las tarjetas inteligentes proporcionan autenticación en dos fases. La autenticación en dos fases va más allá de la combinación simple de nombre de usuario y contraseña y requiere que un usuario envíe algún tipo de toquen único junto con un NIP.

Las tarjetas inteligentes son objetos de plástico del tamaño de una tarjeta de crédito que contienen una microcomputadora y una pequeña cantidad de memoria. Permiten un almacenamiento seguro y protegido de claves privadas y certificados de seguridad X.509.

Para autenticarse en un equipo o a través de una conexión de acceso remoto, el usuario inserta la tarjeta inteligente en un lector adecuado y escribe su NIP. El usuario no puede tener acceso a la red sólo con el NIP o la tarjeta inteligente. No existe la posibilidad de que se produzcan ataques de fuerza bruta en el NIP de la tarjeta inteligente ya que ésta se bloquea tras varios intentos incorrectos de escribir el NIP correcto.

Las tarjetas inteligentes ejecutan sistemas operativos incrustados y un tipo de sistema de archivos en el que se pueden almacenar los datos. El sistema operativo de la tarjeta inteligente debe poder realizar las siguientes tareas:

-   Almacenar las claves pública y privada de un usuario

-   Almacenar un certificado asociado de clave pública

-   Recuperar el certificado de clave pública

-   Realizar operaciones de clave privada en representación del usuario

Para obtener más información acerca de las tarjetas inteligentes y una lista de los lectores de tarjetas inteligentes compatibles con Microsoft, consulte el tema [Tarjetas inteligentes](http://www.microsoft.com/technet/security/topics/identitymanagement/scard.mspx) de Microsoft TechNet en www.microsoft.com/technet/security/topics/identitymanagement/scard.mspx (puede estar en inglés).

#### Requisitos de implementación de las tarjetas inteligentes

Para admitir el inicio de sesión de tarjeta inteligente para el acceso remoto de VPN, el sistema requiere componentes de hardware y software concretos.

Para obtener más información acerca de las especificaciones y los requisitos para la implementación de la tarjeta inteligente, consulte la [*Guía de planeamiento de acceso seguro mediante tarjetas inteligentes*](http://www.microsoft.com/technet/security/topics/networksecurity/securesmartcards/default.mspx) en Microsoft TechNet en www.microsoft.com/technet/security/topics/networksecurity/securesmartcards/
default.mspx (puede estar en inglés).

##### Requisitos de hardware de cliente de la tarjeta inteligente

Para admitir la solución VPN de tarjeta inteligente, los usuarios deberán tener un equipo cliente capaz de ejecutar Windows XP.

Además, los usuarios necesitan un lector de tarjetas inteligentes conectado a una interfaz periférica estándar, como un puerto serie RS-232, PS/2, PC Card o puerto USB (bus serie universal).

##### Requisitos de software de cliente de la tarjeta inteligente

Los clientes de acceso remoto necesitan Windows XP para admitir la solución VPN de tarjeta inteligente. Además, se recomienda instalar Service Pack 2 (SP2).

Cada equipo cliente deberá instalar un proveedor de servicios de cifrado (CSP) compatible con la tarjeta inteligente elegida. Windows XP incluye un CSP compatible con varias soluciones de tarjeta inteligente. Como alternativa, el proveedor de soluciones de tarjeta inteligente ofrecerá un CSP. El CSP realiza las siguientes funciones:

-   Funciones de cifrado, incluida la firma digital

-   Administración de clave privada

-   Comunicación segura entre el lector de tarjetas inteligentes del equipo cliente y la tarjeta inteligente

En cada equipo cliente habrá que instalar los controladores de dispositivos del lector de tarjetas inteligentes específico. Los controladores de dispositivos asignan la funcionalidad del lector a los servicios originales suministrados por Windows XP y la infraestructura de la tarjeta inteligente. El controlador de dispositivo del lector de tarjetas inteligentes comunica la inserción de la tarjeta y los eventos de extracción y ofrece prestaciones para la comunicación bidireccional de los datos con la tarjeta.

Connection Manager es una función estándar de Windows XP que facilita y administra las conexiones de red, de acceso telefónico y VPN. Además, es posible usar el Kit de administración de Connection Manager (CMAK) para personalizar perfiles de Connection Manager y crear un archivo de instalación que configura automáticamente la conexión VPN, que se distribuye a los clientes.

La implementación de tarjetas inteligentes puede incluir el software de administración de la tarjeta en el cliente. El software incluye administración de la tarjeta inteligente, conectividad y herramientas de seguridad que permiten ver el contenido de las tarjetas inteligentes, restablecer los NIP y agregar certificados adicionales.

##### Requisitos de hardware del servidor VPN

Las conexiones VPN suponen una carga de procesador adicional en el servidor de acceso remoto. El inicio de sesión seguro con tarjeta inteligente no se agrega aparentemente a esta carga. Los servidores de acceso remoto de VPN que dan servicio a un gran volumen de conexiones entrantes requieren procesadores rápidos, preferiblemente en una configuración con multiprocesador, además de capacidad de alto rendimiento de la red. Las organizaciones que utilizan redes VPN protegidas con IPsec pueden implementar tarjetas de red que descarguen el proceso de cifrado IPsec en un procesador independiente ubicado en la tarjeta de red.

##### Requisitos de software de servidor VPN

Los requisitos de software de servidor VPN para el acceso de tarjeta inteligente son relativamente sencillos. Los servidores de acceso remoto deben ejecutar Windows 2000 Server o posterior, tener habilitado el enrutamiento y acceso remoto, y deben admitir el Protocolo de autenticación extensible y la Seguridad de la capa de transporte (EAP-TLS).

EAP-TLS es un mecanismo de autenticación mutua desarrollado para utilizarse junto con dispositivos de seguridad, como tarjetas inteligentes y símbolos (tokens) de hardware. EAP-TLS admite el Protocolo punto a punto (PPP) y las conexiones VPN, y posibilita el intercambio de claves secretas compartidas para MPPE, además de IPsec.

Las principales ventajas de EAP-TLS son su resistencia a los ataques y el hecho de que admite autenticación mutua. Con la autenticación mutua, tanto el cliente como el servidor pueden comprobar las respectivas identidades. Si el cliente o el servidor no envían un certificado para validar la identidad, se interrumpe la conexión.

Microsoft Windows Server™ 2003 admite EAP-TLS para las conexiones de acceso telefónico y VPN, lo que permite el uso de tarjetas inteligentes para usuarios remotos. Para obtener más información acerca de EAP-TLS, consulte el tema [Protocolo de autenticación extensible (EAP)](http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/auth_eap.mspx) en www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/auth\_eap.mspx (puede estar en inglés).

Para obtener más información acerca de los requisitos de certificado EAP, consulte el artículo de Microsoft Knowledge Base "[Requisitos de certificado cuando se usa EAP-TLS o PEAP con EAP-TLS](http://support.microsoft.com/default.aspx?scid=814394)" en http://support.microsoft.com/default.aspx?scid=814394 (puede estar en inglés).

#### Requisitos previos de la infraestructura de red para la implementación de tarjetas inteligentes

Las tarjetas inteligentes necesitan una infraestructura apropiada que admita el sistema operativo y los elementos de red. Antes de comenzar el proceso de implementación de la tarjeta inteligente, es necesario ocuparse de la necesidad de los siguientes componentes:

-   Requisitos de usuario

-   Infraestructura de clave pública (PKI)

-   Plantillas de certificado

-   Servicio de directorio Active Directory®

-   Grupos de seguridad

-   Estaciones de inscripción y agentes de inscripción

##### Requisitos de usuario

La identificación de usuarios y grupos que requieren acceso de VPN es una parte importante de la implementación de la tarjeta inteligente. Identifique estas cuentas al comenzar el proceso para ayudar a definir el alcance de los costos de proyecto y control.

##### Infraestructura de clave pública (PKI)

Las soluciones de tarjeta inteligente requieren una PKI para proporcionar certificados con pares de clave pública/clave privada que permitan la asignación de cuentas en Active Directory. Esta PKI se puede implementar de dos formas: proporcionar la infraestructura de certificado interna a una organización externa o utilizar Servicios de Certificate Server de Windows Server 2003. Para usar Servicios de Certificate Server de Windows Server 2003 en la solución de tarjeta inteligente, la entidad de certificación (CA) debe ser una entidad empresarial que requiera Active Directory.

Para obtener más información acerca de los Servicios de Certificate Server de Windows Server 2003, consulte el sitio web [Infraestructura de clave pública para Windows Server 2003](http://www.microsoft.com/windowsserver2003/technologies/pki/default.mspx) en www.microsoft.com/windowsserver2003/technologies/pki/default.mspx (puede estar en inglés).

La PKI debe tener un mecanismo que se encargue de la revocación de certificados. La revocación de certificados es necesaria cuando un certificado caduca o cuando un atacante puede haber puesto en peligro un certificado. Al revocar un certificado, un administrador deniega el acceso a cualquier usuario que use el certificado. Cada certificado incluye la ubicación de su lista de revocaciones de certificados (CRL).

Para obtener más información sobre cómo administrar la revocación de certificados, consulte el tema [Administración de revocación de certificados](http://technet2.microsoft.com/windowsserver/en/library/92a5e655-3eb2-4843-b9cb-58c84c0a91d61033.mspx?mfr=true) de Microsoft TechNet en http://technet2.microsoft.com/WindowsServer/en/library/92a5e655-3eb2-4843-b9cb-58c84c0a91d61033.mspx?mfr=true (puede estar en inglés).

PKI se utiliza para asignar un certificado a cada tarjeta inteligente en la solución VPN. Una CA en la que el servidor VPN confíe debe emitir el certificado. Si utiliza los Servicios de Certificate Server de Windows Server 2003, asegúrese de que instala el certificado raíz PKI en el servidor VPN.

Si la autenticación es mutua, debe asignar un certificado al servidor VPN desde una CA en la que el cliente confíe. Si utiliza los Servicios de Certificate Server de Windows Server 2003, asegúrese de que instala el certificado raíz PKI en el cliente VPN.

##### Plantillas de certificado

Windows Server 2003 proporciona plantillas de certificado específicas para emitir certificados digitales que pueden utilizarse con soluciones de tarjeta inteligente. Las tres plantillas de certificado para el uso de tarjetas inteligentes son:

-   Agente de inscripción, que permite a un usuario autorizado solicitar certificados para otros usuarios.

-   Usuario de tarjeta inteligente, que permite a un usuario iniciar sesión con una tarjeta inteligente y firmar mensajes de correo electrónico. Además, este certificado permite la autenticación de cliente.

-   Inicio de sesión de Tarjeta inteligente, que permite a un usuario iniciar sesión con una tarjeta inteligente y la autenticación de cliente, pero no permite firmar mensajes de correo electrónico.

**Nota**   Microsoft recomienda encarecidamente que actualice la PKI actual de Windows Server 2003 a la PKI de Windows Server 2003 con Service Pack 1 (SP1) para aprovechar las medidas de seguridad mejoradas.

La solución VPN requerirá al menos un administrador con un certificado de agente de inscripción que asigne certificados a las tarjetas inteligentes. Además, los clientes requerirán certificados de inicio de sesión en sus tarjetas inteligentes.

Para obtener más información sobre las plantillas de certificado, consulte el tema [Plantillas de certificados](http://technet2.microsoft.com/windowsserver/en/library/7d82b420-10ef-4f20-a56f-17ee7ee352d21033.mspx?mfr=true) de TechNet en http://technet2.microsoft.com/WindowsServer/en/Library/7d82b420-10ef-4f20-a56f-17ee7ee352d21033.mspx?mfr=true (puede estar en ingles).

##### Active Directory

Active Directory proporciona los medios para administrar las identidades y relaciones que forman parte de los entornos de red y es un componente clave para la implementación de soluciones de tarjeta inteligente. Active Directory en Windows Server 2003 contiene compatibilidad integrada para establecer un inicio de sesión de tarjeta inteligente y la capacidad de asignar cuentas a los certificados. Esta capacidad para asignar cuentas de usuario a certificados vincula la clave privada de la tarjeta inteligente al certificado integrado en Active Directory.

Cuando el agente de inscripción asigna un certificado a una tarjeta inteligente para un usuario específico, el proceso asigna el certificado a la cuenta de usuario en Active Directory. La presentación de las credenciales de tarjeta inteligente en el inicio de sesión requiere Active Directory para hacer coincidir esta tarjeta específica con la cuenta de usuario, que proporciona al usuario permisos relevantes y capacidades en la red.

Para obtener más información sobre la asignación de certificados, consulte el tema [Asignar certificados a cuentas de usuario](http://www.microsoft.com/resources/documentation/windowsserv/2003/all/deployguide/en-us/dssch_pki_cyek.asp) de Microsoft TechNet en www.microsoft.com/resources/documentation/WindowsServ/2003/all/deployguide/en-us/dssch\_pki\_cyek.asp (puede estar en inglés).

Para obtener más información sobre Active Directory, consulte la página [Windows Server 2003 Active Directory](http://www.microsoft.com/windowsserver2003/technologies/directory/activedirectory/default.mspx) en www.microsoft.com/windowsserver2003/technologies/directory/activedirectory/
default.mspx (puede estar en inglés).

##### Grupos de seguridad

El proceso de implementación y administración de tarjetas inteligentes es significativamente más fácil si se usan grupos de seguridad en Active Directory para organizar a los usuarios. Por ejemplo, una tarjeta inteligente típica puede requerirle que cree los siguientes grupos de seguridad:

-   **Agentes de inscripción de tarjeta inteligente**. Los agentes de inscripción de tarjeta inteligente son los responsables de la distribución de tarjetas inteligentes a los usuarios.

-   **Ensayo de tarjeta inteligente**. El grupo de ensayo de tarjeta inteligente contiene todos los usuarios que reciben tarjetas inteligentes, pero para los cuales aún no se ha inscrito un agente de inscripción ni se han activado sus tarjetas.

-   **Usuarios de tarjeta inteligente**. El grupo de usuarios de tarjeta inteligente contiene todos los usuarios que han finalizado el proceso de inscripción y tienen una tarjeta inteligente activada. El agente de inscripción desplaza al usuario transfiere el grupo de ensayo de tarjeta inteligente al grupo de usuarios de tarjeta inteligente.

-   **Excepciones temporales de tarjeta inteligente**. El grupo de excepciones temporales de tarjeta inteligente es para usuarios que requieren excepciones temporales a los requisitos de tarjeta inteligente, por ejemplo, tras la pérdida o el olvido de la tarjeta inteligente.

-   **Excepciones permanentes de tarjeta inteligente**. El grupo de excepciones permanentes de tarjeta inteligente incluye cuentas que necesitan excepciones permanentes de requisito para el inicio de sesión de tarjeta inteligente.

Como mínimo, la solución VPN requerirá grupos para agentes de inscripción y usuarios de tarjeta inteligente. La creación de esos grupos permite administrar y configurar varios usuarios de una forma más sencilla.

##### Estaciones de inscripción y agentes de inscripción

Es posible utilizar una interfaz basada en Web para emitir o inscribir usuarios de tarjetas inteligentes, pero no se recomienda. Debido a que los usuarios deben introducir sus nombres de usuario y contraseñas para obtener sus tarjetas inteligentes, este método disminuye de manera eficaz la seguridad de la tarjeta inteligente al mismo nivel que las credenciales presentadas en la interfaz web. La solución preferida es crear estaciones de inscripción y designar uno o varios administradores como agentes de inscripción.

Una estación de inscripción típica es un equipo que tiene un lector de tarjetas inteligentes y un editor de tarjetas inteligentes asociados. El lector permite al agente de inscripción iniciar sesión y el editor crea nuevas tarjetas inteligentes para los usuarios. La estación de inscripción tiene una configuración de directiva de grupo que obliga a cerrar sesión en el momento en que el agente de inscripción extrae la tarjeta inteligente.

Un administrador designado asume la función de agente de inscripción y usa su tarjeta inteligente para iniciar sesión en la estación de inscripción. A continuación, abre la página web de los Servicios de Certificate Server, comprueba la identidad del usuario, lo inscribe y emite la tarjeta inteligente inscrita. Los agentes de inscripción requieren un certificado de agente de inscripción y deben tener permisos para tener acceso a las plantillas de certificado.

#### Consideraciones operativas

La solución VPN de tarjeta inteligente debe ocuparse de la capacidad de supervisar el estado operativo de la solución. Las herramientas de supervisión deben mostrar la información necesaria para proporcionar un soporte operativo. Si la solución no cumple este requisito, el personal de seguridad no puede determinar si la solución mantiene conexiones de acceso remoto seguras de forma efectiva.

Las consideraciones operativas son:

-   **Prueba de autenticación de aplicaciones internas**. Una tarjeta inteligente sólo debe afectar al inicio de sesión inicial. El programa de prueba debe probar y comprobar la correcta autenticación de aplicaciones internas.

-   **Solución de problemas de cliente remoto**. Para una solución de problemas con éxito, los problemas del cliente pueden requerir una estrecha cooperación entre varios equipos repartidos en diferentes zonas horarias. Pruebas rigurosas y una implementación piloto adecuada ayudan a reducir las llamadas de soporte técnico.

-   **Descripción de escenarios de acceso remoto organizativos y amenazas**. Es necesario describir los escenarios de acceso remoto de la organización y las amenazas que afectan a la seguridad, además del equilibrio entre ellos. Debe establecerse la prioridad de los recursos que necesitan la máxima protección y determinar el equilibrio adecuado entre costos y riesgos.

-   **Anticipación a los retos técnicos**. Debe anticiparse a los retos técnicos, como las rutinas de instalación y la distribución de herramientas de administración de tarjetas inteligentes. Es posible que necesite integrar la solución de tarjeta inteligente en sus herramientas de administración empresarial existentes.

-   **Supervisión y administración de los problemas de rendimiento**. Debe supervisar y administrar los problemas de rendimiento y establecer las expectativas del usuario antes de la implementación.

-   **Consideración de los recursos personales**. Recuerde que los equipos domésticos de los empleados son propiedad privada y no están administrados por un departamento de TI de la organización. Si un empleado no puede instalar el hardware y el software para admitir un acceso remoto de tarjeta inteligente seguro, existen otras opciones disponibles. Por ejemplo, Microsoft Outlook® Web Access (OWA) proporciona a los empleados acceso a sus buzones de Microsoft Exchange Server a través de las conexiones cifradas de Capa de sockets seguros (SSL).

    Para obtener más información sobre la seguridad del correo electrónico, consulte el artículo "[Cómo proteger la confidencialidad del correo electrónico en sectores regulados](http://go.microsoft.com/fwlink/?linkid=71176)" de esta serie en http://go.microsoft.com/fwlink/?LinkId=71176 (puede estar en inglés).

-   **Administración de los cambios realizados en la solución**. Debe administrar cualquier cambio y mejora realizados en la solución a través de procesos similares a los requeridos para la implementación inicial.

-   **Optimización de la solución**. Todos los aspectos de la solución de tarjeta inteligente requieren revisiones y optimizaciones periódicas. De forma periódica, es preciso revisar el proceso de inscripción y la necesidad de excepciones de cuenta con el objetivo de mejorar la seguridad y la integridad.

[](#mainsection)[Principio de la página](#mainsection)

### Inicio de sesión de tarjeta inteligente en un escenario de VPN de acceso remoto

El proceso definido en esta sección para la configuración de inicio de sesión de tarjeta inteligente para las VPN de acceso remoto está relacionado con escenarios de pequeñas y medianas empresas. En la siguiente figura se muestra una red de pequeñas y medianas empresas; es posible que tenga todos o algunos de los servicios mostrados en su propio entorno.

![](images/Cc875840.SCLVPN01(es-es,TechNet.10).gif)

**Figura 1. Acceso remoto en el entorno de TI mediano**

Concretamente, este proceso se ajusta a escenarios en los cuales los usuarios remotos requieren acceso a los datos corporativos y servicios desde ubicaciones externas. Para obtener este acceso, los usuarios remotos crean una conexión VPN al servidor VPN de Windows Server 2003 y usan tarjetas inteligentes para la autenticación.

Los siguientes procesos le ayudarán a preparar, implementar y configurar el soporte para tarjetas inteligentes en VPN de acceso remoto.

#### Cómo preparar una entidad de certificación (CA) para emitir certificados de tarjeta inteligente

En primer lugar, debe preparar la CA para asignar los certificados necesarios, el agente de inscripción y el inicio de sesión de tarjeta inteligente.

**Para preparar una CA con el fin de emitir certificados de tarjeta inteligente**

1.  Inicie sesión con derechos de administrador.

2.  Abra **Sitios y servicios de Active Directory**.

3.  Haga clic en el menú **Ver** y, a continuación, seleccione **Mostrar el nodo de servicios**.

4.  Expanda **Servicios**, haga clic en **Servicios de clave pública** y, a continuación, haga clic en **Plantillas de certificado** (se muestra en la siguiente captura de pantalla).

    [![](images/Cc875840.SCLVPN02(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875840.sclvpn02_big(es-es,technet.10).gif)

5.  Haga clic con el botón secundario en la plantilla de certificado del **Agente de inscripción** y, a continuación, seleccione **Propiedades**.

6.  Agregue el grupo de seguridad de los agentes de inscripción que ha creado como parte de los requisitos previos de la implementación y asigne permisos de **Lectura** e **Inscripción** (se muestran en la siguiente captura de pantalla). A continuación, haga clic en **Aceptar**.

    [![](images/Cc875840.SCLVPN03(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875840.sclvpn03_big(es-es,technet.10).gif)

7.  Cierre **Sitios y servicios de Active Directory**.

8.  Abra **Entidad emisora de certificados**.

9.  Expanda el nombre del servidor y, a continuación, seleccione **Plantillas de certificado**. En el panel derecho, puede ver la lista de certificados que la CA puede asignar (se muestra en la siguiente captura de pantalla).

    [![](images/Cc875840.SCLVPN04(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875840.sclvpn04_big(es-es,technet.10).gif)

10. Haga clic con el botón secundario en **Plantillas de certificado**, seleccione **Nuevo** y, a continuación, haga clic en **Plantilla de certificado que se va a emitir**.

11. Mantenga presionada la tecla CTRL y, en la lista **Habilitar plantillas de certificados**, seleccione **Agente de inscripción** e **Inicio de sesión de Tarjeta inteligente** (se muestra en la siguiente captura de pantalla). A continuación, haga clic en **Aceptar**.

    [![](images/Cc875840.SCLVPN05(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875840.sclvpn05_big(es-es,technet.10).gif)

12. Cierre **Entidad emisora de certificados**.

#### Cómo implementar certificados en las tarjetas inteligentes

A continuación, puede asignar certificados a tarjetas inteligentes de usuarios remotos. Inicie sesión como agente de inscripción para el dominio en el que se ubica la cuenta de usuario.

**Para implementar certificados en las tarjetas inteligentes**

1.  Abra Microsoft Internet Explorer®.

2.  En la barra de direcciones, escriba la dirección de la CA que emite certificados de inicio de sesión de tarjeta inteligente y, a continuación, presione ENTRAR.

3.  Haga clic en **Solicitar un certificado** y, a continuación, en **Solicitud de certificado avanzada**. Se mostrará una pantalla parecida a la siguiente.

    [![](images/Cc875840.SCLVPN06(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875840.sclvpn06_big(es-es,technet.10).gif)

4.  Haga clic en **Solicitar un certificado para una tarjeta inteligente de otro usuario usando la Estación de inscripción de certificados para tarjetas inteligentes**. Si aparece un mensaje para aceptar un control ActiveX® de Microsoft, haga clic en **Sí**. Debe habilitar el uso de controles ActiveX en Internet Explorer.

5.  En la pantalla **Estación de inscripción de certificados para tarjetas inteligentes** (se muestra en la siguiente captura de pantalla), seleccione **Inicio de sesión de Tarjeta inteligente**. Además, debería ver los nombres de la **Entidad emisora de certificados**, el **Proveedor de servicios de cifrado** y **Certificado de firma del administrador**. Si no puede seleccionar un administrador que firme el certificado, no habrá asignado un certificado de agente de inscripción al usuario que ha iniciado sesión.

    [![](images/Cc875840.SCLVPN07(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875840.sclvpn07_big(es-es,technet.10).gif)

6.  De la lista desplegable **Entidad emisora de certificados**, seleccione el nombre de la CA que desea que emita el certificado de tarjeta inteligente.

7.  De la lista desplegable **Proveedor de servicios de cifrado**, seleccione el fabricante de la tarjeta inteligente.

8.  En **Certificado de firma del administrador**, escriba el nombre del certificado de agente de inscripción que firmará la solicitud de inscripción o haga clic en **Seleccionar certificado** para seleccionar un nombre.

9.  Haga clic en **Seleccionar usuario** y, a continuación, seleccione la cuenta de usuario adecuada. Haga clic en **Inscripción**.

10. Cuando el sistema lo solicite, inserte la tarjeta inteligente en el lector de tarjetas inteligentes del equipo y, a continuación, haga clic en **Aceptar**. Cuando el sistema le solicite un número de identificación personal (NIP), escriba el NIP de la tarjeta inteligente.

#### Cómo configurar servidores VPN para la autenticación de tarjetas inteligentes

Ahora puede configurar el servidor VPN.

**Para configurar el servicio Enrutamiento y acceso remoto para aceptar la autenticación EAP**

1.  Inicie el complemento Enrutamiento y acceso remoto.

2.  Haga clic con el botón secundario en ***&lt;nombre\_servidor&gt;***, seleccione **Propiedades** y, a continuación, haga clic en la ficha **Seguridad**.

3.  Haga clic en **Métodos de autenticación**.

4.  Active la casilla **Protocolo de autenticación extensible (EAP)** (se muestra en la siguiente captura de pantalla) y, a continuación, haga clic en **Aceptar**.

    [![](images/Cc875840.SCLVPN08(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875840.sclvpn08_big(es-es,technet.10).gif)

5.  Haga clic en **Aceptar**.

#### Cómo configurar directivas de acceso remoto para la autenticación de tarjetas inteligentes

Ahora puede habilitar EAP en directivas de acceso remoto. El componente Directivas de acceso remoto se incluye de manera predeterminada en el complemento Enrutamiento y acceso remoto. Sin embargo, si el Servicio de autenticación de Internet (IAS) (también conocido como Servicio de usuario de acceso telefónico de autenticación remota o RADIUS) está instalado, en su lugar, se incluye el componente Directivas de acceso remoto en el complemento IAS.

**Para habilitar EAP con directivas de acceso remoto**

1.  En el panel izquierdo de Enrutamiento y acceso remoto, haga clic en **Directivas de acceso remoto**.

2.  En el panel derecho, haga doble clic en **Conexiones al servidor de Enrutamiento y acceso remoto de Microsoft**. Se mostrará una pantalla parecida a la siguiente.

    [![](images/Cc875840.SCLVPN09(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875840.sclvpn09_big(es-es,technet.10).gif)

3.  Haga clic en **Editar perfil**, elija la ficha **Autenticación** y seleccione **Métodos EAP** (se muestra en la siguiente captura de pantalla).

    [![](images/Cc875840.SCLVPN10(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875840.sclvpn10_big(es-es,technet.10).gif)

4.  Si no aparece **Tarjeta inteligente u otro certificado** en la lista de **tipos EAP** como se muestra en la siguiente captura de pantalla, haga clic en **Agregar**, seleccione **Tarjeta inteligente u otro certificado** y haga clic en **Aceptar**.

    [![](images/Cc875840.SCLVPN11(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875840.sclvpn11_big(es-es,technet.10).gif)

5.  Seleccione **Tarjeta inteligente u otro certificado** y, a continuación, haga clic en **Editar**. Se mostrará una pantalla parecida a la siguiente.

    [![](images/Cc875840.SCLVPN12(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875840.sclvpn12_big(es-es,technet.10).gif)

6.  En la lista desplegable, seleccione el certificado que desee utilizar para la autenticación y, a continuación, haga clic en **Aceptar** tres veces.

7.  Asegúrese de que ha seleccionado **Conceder permiso de acceso remoto**, haga clic en **Aceptar** y cierre Enrutamiento y acceso remoto.

#### Cómo configurar clientes VPN para la autenticación de tarjetas inteligentes

A continuación, configure el cliente para usar la autenticación EAP de manera que admita tarjetas inteligentes.

**Para crear una entrada de libreta de teléfonos**

1.  Haga clic en **Inicio**, seleccione **Conectarse a**, elija **Mostrar todas las conexiones** y, a continuación, en la lista **Tareas de red** haga clic en **Crear una nueva conexión**. A continuación, haga clic en **Siguiente** en la pantalla de bienvenida **Asistente para conexión nueva**. Se mostrará la siguiente pantalla.

    [![](images/Cc875840.SCLVPN13(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875840.sclvpn13_big(es-es,technet.10).gif)

2.  Seleccione **Conectar a la red de mi lugar de trabajo** y haga clic en **Siguiente**.

3.  Seleccione **Conexión de red privada virtual** y haga clic en **Siguiente**.

4.  Escriba un nombre para la conexión en el cuadro **Nombre de la compañía** y, a continuación, haga clic en **Siguiente**. Se mostrará la siguiente pantalla.

    ![](images/Cc875840.SCLVPN14(es-es,TechNet.10).gif)

5.  Si dispone de una conexión permanente a Internet, seleccione **No usar la conexión inicial** y haga clic en **Siguiente**. De manera alternativa, si necesita crear una conexión antes de crear la VPN, seleccione **Usar automáticamente esta conexión inicial**, elija la conexión que se va a usar en la lista desplegable y, a continuación, haga clic en **Siguiente**.

6.  Escriba el nombre del servidor VPN o la dirección IP en el cuadro **Nombre del host o dirección IP** y haga clic en **Siguiente**.

7.  Seleccione **Usar mi tarjeta inteligente**, haga clic en **Siguiente** y después en **Finalizar**.

Una vez creada la libreta de teléfonos, configure esta entrada para usar EAP.

**Para configurar una conexión actual para que utilice la autenticación de tarjeta inteligente**

1.  Haga clic con el botón secundario en la conexión, seleccione **Propiedades** y, a continuación, haga clic en la ficha **Seguridad**. Se mostrará la siguiente pantalla.

    ![](images/Cc875840.SCLVPN15(es-es,TechNet.10).gif)

2.  Asegúrese de que ha seleccionado **Típica (configuración recomendada)** y, a continuación, seleccione **Usar tarjeta inteligente** en la lista desplegable **Validar mi identidad como sigue**.

3.  Seleccione **Avanzada (configuración personalizada)** y haga clic en **Configuración**.

4.  Haga clic en **Tarjeta inteligente u otro certificado (cifrado habilitado)**.

5.  Haga clic en **Propiedades** y, a continuación, haga clic en **Usar mi tarjeta inteligente**.

6.  Asegúrese de que se ha activado la opción **Validar un certificado de servidor**.

7.  Si es necesario, active la casilla **Conectar siempre que el nombre del equipo termine por**.

8.  En el cuadro **Entidad emisora raíz de confianza**, haga clic en el nombre de la CA que ha emitido el certificado para usarlo con una tarjeta inteligente o el certificado de usuario instalado.

9.  Si es necesario, active la casilla **Usar un nombre de usuario distinto para la conexión**.

10. El usuario debe iniciar sesión en el equipo para usar EAP con un certificado de usuario.

#### Cómo configurar clientes VPN para la autenticación de tarjetas inteligentes que utilizan Connection Manager

Si necesita configurar conexiones VPN para varios clientes, puede usar Connection Manager.

**Para instalar CMAK en un equipo en el que se ejecute Windows Server 2003**

1.  Haga clic en **Inicio**, seleccione **Panel de control** y, a continuación, haga doble clic en **Agregar o quitar programas**.

2.  En el cuadro de diálogo **Agregar o quitar programas**, haga clic en **Agregar o quitar componentes de Windows**.

3.  En la pantalla **Asistente para componentes de Windows**, seleccione **Herramientas de administración y supervisión**, y haga clic en **Detalles**. Se mostrará una pantalla parecida a la siguiente.

    [![](images/Cc875840.SCLVPN16(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875840.sclvpn16_big(es-es,technet.10).gif)

4.  En el cuadro de diálogo **Herramientas de administración y supervisión**, seleccione **Asistente para el Kit de administración de Connection Manager**, haga clic en **Aceptar**, seleccione **Siguiente** y haga clic en **Finalizar**.

**Para usar CMAK con el fin de crear un perfil de conexión VPN que se pueda distribuir a los usuarios**

1.  Haga clic en **Inicio**, elija **Herramientas administrativas** y, a continuación, haga clic en **Asistente para el Kit de administración de Connection Manager**.

2.  En la pantalla **Asistente para el Kit de administración de Connection Manager**, haga clic en **Siguiente**.

3.  Asegúrese de que ha seleccionado **Nuevo perfil** y haga clic en **Siguiente**.

4.  Escriba un nombre para el perfil en el cuadro **Nombre del servicio** y un nombre para el archivo ejecutable que va a distribuir a los clientes en el cuadro **Nombre del archivo**.

5.  La pantalla **Nombre de dominio** (se muestra en la siguiente captura de pantalla) le permite agregar un nombre de dominio al nombre de usuario. Quizá aparezca un mensaje para pedirle que agregue un nombre de dominio para identificar a los usuarios si se conectan a su VPN a través de un servidor de acceso a la red de terceros que utilice RADIUS para transmitir credenciales de autenticación de red a sus servidores IAS.

    Seleccione **No agregar un nombre de territorio al nombre de usuario** (a menos que sea necesario) y haga clic en **Siguiente**.

    ![](images/Cc875840.SCLVPN17(es-es,TechNet.10).gif)

6.  La pantalla **Combinar información de perfiles** permite combinar perfiles de Connection Manager configurados con anterioridad. Haga esto si necesita incorporar información contenida en otros perfiles (como números de acceso a la red) al perfil actual. Agregue todos los perfiles necesarios y, a continuación, haga clic en **Siguiente**.

7.  La pantalla **Compatibilidad con VPN** (se muestra en la siguiente captura de pantalla) permite crear una libreta de teléfonos del perfil y configurar el servidor o servidores VPN para los clientes VPN.

    ![](images/Cc875840.SCLVPN18(es-es,TechNet.10).gif)

    Una libreta de teléfonos contiene información como código de área, número de teléfono y métodos de autenticación de usuario. La libreta de teléfonos de Connection Manager también incluye diferentes configuraciones de red que se configuran al ejecutar el asistente de CMAK.

    Si desea que el cliente tenga la opción de conectarse a varios servidores VPN, puede crear una lista de servidores VPN en un archivo de texto (se muestra en la siguiente captura de pantalla). Si desea que la conexión utilice una lista de servidores VPN, seleccione **Permitir al usuario elegir un servidor VPN antes de conectarse**, vaya al archivo de texto y, a continuación, haga clic en **Siguiente**.

    ![](images/Cc875840.SCLVPN19(es-es,TechNet.10).gif)

8.  En la pantalla **Entradas VPN**, seleccione el perfil que esté creando, haga clic en **Editar** y, a continuación, haga clic en la ficha **Seguridad**. Se mostrará el siguiente cuadro de diálogo.

    [![](images/Cc875840.SCLVPN20(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875840.sclvpn20_big(es-es,technet.10).gif)

9.  En la lista desplegable **Configuración de seguridad**, seleccione **Usar configuración de seguridad avanzada** y haga clic en **Configurar**. Se mostrará el siguiente cuadro de diálogo.

    ![](images/Cc875840.SCLVPN21(es-es,TechNet.10).gif)

10. Asegúrese de que la lista desplegable **Cifrado de datos** tiene habilitado **Requiere cifrado** y de que selecciona el protocolo de túnel adecuado en la lista desplegable Estrategia de VPN.

    Seleccione **Usar Protocolo de autenticación extensible (EAP) y Tarjeta inteligente u otro certificado (cifrado habilitado)** en la correspondiente lista desplegable y, a continuación, haga clic en **Propiedades**. Se mostrará una pantalla parecida a la siguiente.

    ![](images/Cc875840.SCLVPN22(es-es,TechNet.10).gif)

11. Asegúrese de que ha seleccionado **Usar mi tarjeta inteligente** y **Validar un certificado de servidor** si desea que el cliente confirme la validez del servidor. Además, puede escribir el nombre de uno o varios servidores a los que conectarse y la entidad de certificación raíz con la que validar el servidor. Si el cliente debe autenticarse mediante un nombre de usuario distinto del certificado, seleccione **Usar un nombre de usuario distinto para la conexión**. Haga clic en **Aceptar** tres veces y, a continuación, haga clic en **Siguiente**.

12. La pantalla **Libreta de teléfonos** permite incluir un archivo de la libreta de teléfonos adicional en el perfil y descargar automáticamente actualizaciones de la libreta de teléfonos. La libreta de teléfonos incluye información como código de área, número de teléfono y métodos de autenticación de usuario admitidos. La libreta de teléfonos de Connection Manager también incluye diferentes configuraciones de red que se configuran al ejecutar el asistente de CMAK. Si selecciona **Descargar automáticamente actualizaciones de la libreta de teléfonos**, debe especificar la ubicación desde la que se descargan las actualizaciones. Si no necesita descargar actualizaciones de la libreta de teléfonos, no seleccione esta opción. Haga clic en **Siguiente.**

13. Si utiliza el acceso telefónico a redes con la conexión, seleccione la entrada y, a continuación, haga clic en **Editar** en la pantalla Entradas de acceso telefónico a redes. Si no utiliza el acceso telefónico a redes en la conexión, verá cómo deshabilitarlo en un procedimiento subsiguiente. Cuando haya realizado la configuración necesaria o si necesita usar el acceso telefónico a redes, haga clic en **Siguiente**. Las pantallas del asistente descritas en las tareas 14 a 25 configuran componentes opcionales que principalmente cambian la apariencia y el funcionamiento de la conexión.

14. Puede usar la configuración de la pantalla **Actualización de tabla de enrutamiento** para configurar la información de enrutamiento de la conexión. La configuración predeterminada es tener el cliente VPN conectado a todas las redes no conectadas directamente a través de la interfaz VPN. Sin embargo, si no configura el cliente VPN para utilizar la conexión VPN como su puerta de enlace predeterminada, puede crear entradas de tabla de enrutamiento personalizadas que permitan al cliente VPN tener acceso a subredes seleccionadas en la red interna. Cuando termine, haga clic en **Siguiente**.

15. Puede usar la configuración de la pantalla **Configuración automática de servidor proxy** para obligar a los clientes VPN a usar el servidor VPN como su servidor proxy web. Haga clic en **Siguiente.**

16. Utilice la configuración de la pantalla **Acciones personalizadas** para especificar programas que se iniciarán automáticamente antes, después o durante la conexión VPN. Haga clic en **Siguiente.**

17. Utilice la configuración de la pantalla **Mapa de bits de inicio de sesión** para crear un gráfico especial que aparezca cuando el usuario abra la conexión VPN. Si crea un gráfico personalizado, asegúrese de que tiene 330 x 140 píxeles. Haga clic en **Siguiente.**

18. Utilice la configuración de la pantalla **Mapa de bits de Libreta de teléfonos** para crear un gráfico especial que aparezca cuando el usuario abra la libreta de teléfonos. Si crea un gráfico personalizado, asegúrese de que tiene 114 x 309 píxeles. Haga clic en **Siguiente.**

19. Utilice la configuración de la pantalla **Iconos** para especificar iconos que desee mostrar en la interfaz de usuario de Connection Manager. Haga clic en **Siguiente.**

20. Utilice la configuración de la pantalla **Menú contextual del área de notificación** para agregar elementos a los menús contextuales de Connection Manager. Haga clic en **Siguiente.**

21. Utilice la configuración de la pantalla **Archivo de ayuda** para asignar un archivo de ayuda personalizado a los usuarios. Haga clic en **Siguiente.**

22. Utilice la configuración de la pantalla **Información de soporte técnico** para proporcionar información de soporte técnico a los usuarios. Haga clic en **Siguiente.**

23. Puede revisar la configuración de la pantalla **Software de Connection Manager**. Tiene la opción de instalar Connection Manager versión 1.3 en los clientes que aún no lo tengan instalado en su equipo. Haga clic en **Siguiente.**

24. Utilice la configuración de la pantalla **Contrato de licencia** para incluir un contrato de licencia personalizado en la conexión. Haga clic en **Siguiente.**

25. Puede usar la pantalla **Archivos adicionales** para incluir archivos adicionales en el perfil de Connection Manager. Haga clic en **Siguiente.**

26. En la pantalla **Listo para crear el perfil de servicio**, seleccione **Personalización avanzada** y, a continuación, haga clic en **Siguiente**.

27. La pantalla **Personalización avanzada** (se muestra en la siguiente captura de pantalla) permite configurar el valor de la configuración en sus archivos de configuración de perfil. En las conexiones VPN con tarjeta inteligente habilitada, debería desactivar el acceso telefónico estableciendo el valor en 0. Los valores HideDomain, HideUserName y HidePassword también se han habilitado.

    ![](images/Cc875840.SCLVPN23(es-es,TechNet.10).gif)

28. Los archivos de configuración de perfil se basan en texto y tienen extensiones de nombre de archivo .inf, .cms y .cmp. El asistente lee en los archivos predeterminados .inf, .cms y .cmp de plantilla instalados con CMAK.

    Cuando termina el asistente, se crean nuevos archivos de configuración de perfil como nombreDePerfil.inf, nombreDePerfil.cms y nombreDePerfil.cmp. Puede editar los archivos de plantilla predeterminados para agregar configuraciones adicionales que cualquier usuario del asistente puede configurar.

    Para obtener más información sobre las opciones de personalización avanzada de Connection Manager, consulte la página [Opciones de personalización avanzada de Connection Manager](http://www.microsoft.com/resources/documentation/windows/2000/server/reskit/en-us/ierk/ch14_d.asp) en www.microsoft.com/resources/documentation/Windows/2000/server/reskit/en-us/ierk/Ch14\_d.asp (puede estar en inglés).

    El archivo de plantilla **.cms** (se muestra en la siguiente captura de pantalla) se ha editado para incluir la capacidad de ocultar el dominio, el nombre de usuario y los cuadros de contraseña de manera que la funcionalidad se pueda incluir cuando sea necesario. MPPE usa la contraseña de usuario en el proceso de cifrado, por lo que en algunos casos la solución requiere cuadros de contraseña y nombre de usuario.

    [![](images/Cc875840.SCLVPN24(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875840.sclvpn24_big(es-es,technet.10).gif)

29. Cuando complete todos los cambios de configuración, haga clic en **Siguiente** para crear los archivos ejecutables y de configuración. Anote dónde se almacenarán los archivos y, a continuación, haga clic en **Finalizar**. Distribuya el archivo ejecutable a los clientes mediante mecanismos de distribución de software estándar. El cliente puede ejecutar el archivo manualmente o se puede automatizar el proceso para instalar la conexión VPN.

#### Cómo comprobar la solución VPN de tarjeta inteligente

El objetivo del proceso de comprobación es identificar cualquier problema con el diseño o la configuración de la solución antes de la implementación completa. Para comprobar la solución VPN de tarjeta inteligente, debe llevar a cabo los procedimientos fundamentales de la solución. Los procedimientos fundamentales que se deben comprobar son:

-   Asignación de un certificado a una tarjeta inteligente.

-   Distribución del perfil de Connection Manager.

-   Instalación del perfil de Connection Manager.

-   Conexión al servidor VPN mediante la autenticación de tarjeta inteligente.

-   Acceso a los recursos de red interna a través de la conexión VPN.

#### Cómo solucionar los problemas de la solución VPN de tarjeta inteligente

El objetivo del proceso de comprobación es resolver los problemas de la solución, identificar dónde presenta anomalías el proceso y concentrar los esfuerzos en ese área.

En la siguiente tabla se muestran algunas directrices de solución de problemas de la solución de tarjeta inteligente VPN.

**Tabla 1. Directrices de solución de problemas de tarjeta inteligente VPN**

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Problema</p></th>
<th><p>Solución</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>No existen certificados relevantes disponibles en la CA.</p></td>
<td style="border:1px solid black;"><p>Habilitar plantillas de certificados en Sitios y servicios de Active Directory.</p>
<p>Asignar permisos de inscripción.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>No se pueden asignar certificados a la tarjeta inteligente.</p></td>
<td style="border:1px solid black;"><p>Instalar el editor de tarjetas inteligentes.</p>
<p>Asignar certificado de agente de inscripción.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>El servidor VPN no puede autenticar clientes remotos.</p></td>
<td style="border:1px solid black;"><p>Configurar el servidor para admitir la autenticación EAP-TLS.</p>
<p>Asegurarse de que el cliente confía en el certificado usado en el servidor.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>El cliente intenta crear una conexión antes de crear la VPN.</p></td>
<td style="border:1px solid black;"><p>Configurar el cliente de modo que no cree una conexión inicial.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>El cliente no intenta crear una conexión antes de crear la VPN.</p></td>
<td style="border:1px solid black;"><p>Configurar el cliente para crear una conexión inicial.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Cuando el cliente intenta crear la VPN, aparece un mensaje para pedirle el nombre de usuario, el nombre de dominio y la contraseña.</p></td>
<td style="border:1px solid black;"><p>Asegurarse de que la conexión VPN está configurada para usar una tarjeta inteligente.</p>
<p>Asegurarse de que los valores HideUserName, HideDomain y HidePassword están habilitados.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>El cliente no tiene un objeto de conexión en las conexiones de red.</p></td>
<td style="border:1px solid black;"><p>Asegurarse de que se ha distribuido el perfil de Connection Manager al cliente.</p>
<p>Asegurarse de que se ejecuta el perfil ejecutable de Connection Manager.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>El cliente no conecta con el servidor VPN.</p></td>
<td style="border:1px solid black;"><p>Asegurarse de que la conexión del cliente está configurada con el nombre de servidor VPN correcto.</p>
<p>Asegurarse de que el cliente ha seleccionado el servidor correcto de la lista de servidores VPN.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>El cliente no puede autenticarse con el servidor VPN.</p></td>
<td style="border:1px solid black;"><p>Asegurarse de que el cliente está conectado al servidor VPN correcto.</p>
<p>Asegurarse de que el servidor VPN confía en el certificado de la tarjeta inteligente.</p></td>
</tr>
</tbody>
</table>
<p> </p>

Para obtener más información sobre la solución de problemas generales de las conexiones VPN, consulte el tema **[Solución de problemas de VPN](http://technet2.microsoft.com/windowsserver/en/library/4543aff5-e10f-487c-92ad-bb5518a736201033.mspx) de Microsoft TechNet en http://technet2.microsoft.com/WindowsServer/en/Library/4543aff5-e10f-487c-92ad-bb5518a736201033.mspx (puede estar en inglés).

[](#mainsection)[Principio de la página](#mainsection)

### Resumen

La implementación de tarjetas inteligentes para autenticar conexiones de acceso remoto ofrece más seguridad que las combinaciones simples de nombre de usuario y contraseña. Las tarjetas inteligentes implementan autenticación en dos fases mediante la combinación de la tarjeta inteligente y un NIP. Es considerablemente más difícil poner en peligro la autenticación en dos fases y, para el usuario, es más fácil recordar el NIP que una contraseña segura.

La prestación de autenticación de tarjeta inteligente para usuarios de acceso remoto ayuda a proporcionar un método fiable y rentable que aumenta la seguridad de la red.

[](#mainsection)[Principio de la página](#mainsection)

**Descargar**

[Obtener el artículo Cómo admitir el inicio de sesión de tarjeta inteligente en conexiones de acceso remoto VPN](http://go.microsoft.com/fwlink/?linkid=71173)

[](#mainsection)[Principio de la página](#mainsection)
