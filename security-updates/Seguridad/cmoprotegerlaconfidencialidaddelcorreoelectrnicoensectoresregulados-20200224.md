---
TOCTitle: Cómo proteger la confidencialidad del correo electrónico en sectores regulados
Title: Cómo proteger la confidencialidad del correo electrónico en sectores regulados
ms:assetid: '1c41144a-813b-4a0d-b982-4060269eacfb'
ms:contentKeyID: 20200224
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc875813(v=TechNet.10)'
---

Cómo proteger la confidencialidad del correo electrónico en sectores regulados
==============================================================================

Publicado: agosto 18, 2006

##### En esta página

[](#ecaa)[Introducción](#ecaa)
[](#ebaa)[Ayuda para proteger el escenario de confidencialidad del correo electrónico](#ebaa)
[](#eaaa)[Resumen](#eaaa)

### Introducción

Todas las organizaciones se enfrentan a desafíos legales y normativos importantes en áreas como la seguridad de la información, la privacidad y la confiabilidad. Estos desafíos pueden requerir cambios de envergadura en los sistemas y procesos de toda la organización. Los negocios deben reaccionar y tomar medidas ante la estructura y regulación crecientes que rodean a los gastos y al control para cumplir diversos objetivos legales y éticos. La conformidad implica cumplir con todos los requisitos legales y empresariales a los que se enfrenta una organización y debe demostrarse durante el curso de las operaciones y de la actividad empresarial. La conformidad también implica la comprensión del marco legal en el que funcionan los requisitos judiciales y corporativos. El proceso para conseguir esta conformidad se extiende a cada departamento y empleado. La conformidad no se puede obtener a través de la implementación de una única solución o proceso; debe crearse en cada sección empresarial de una organización.

El entorno normativo es cada vez más complejo. A menudo la conformidad no resulta un proceso sencillo y las regulaciones son diferentes en función de lo específicos que sean sus requisitos. Por tanto, una organización debe realizar una evaluación completa de riesgos e impactos.

El ámbito de este artículo es describir algunos de los procesos y tecnologías que puede utilizar para contribuir a estandarizar y racionalizar los esfuerzos de conformidad en el área de la confidencialidad del correo electrónico. En este artículo se describen los recursos y opciones que muchas medianas empresas se pueden encontrar al intentar cumplir con las leyes y normativas. Este artículo no constituye un plan de conformidad normativa ni ofrece asesoramiento legal sobre ninguno de estos temas. Los lectores deben consultar con sus propios asesores y abogados antes de decretar un programa o proceso de conformidad.

#### Quién debería leer esta guía

Esta guía está dirigida a profesionales de TI que son responsables de la instalación, mantenimiento y administración de un servicio de correo electrónico basado en Microsoft® Exchange Server 2003 en sus entornos de red.

La información contenida en esta guía se aplica a pequeñas y medianas empresas que deben entregar mensajes de correo electrónico confidenciales en su red.

#### Descripción general

Aunque las funciones de seguridad de los mensajes han estado disponibles en Microsoft Exchange Server desde la primera versión del producto, normalmente sólo los clientes que tienen personal y requisitos especializados en seguridad han utilizado estas funciones. Los únicos que necesitaban comprender los conceptos de seguridad en los mensajes de correo electrónico eran los especialistas en seguridad y aquellos usuarios con conocimientos en criptografía. Gracias al soporte mejorado de Secure/Multipurpose Internet Mail Extensions (S/MIME) en Exchange Server 2003 y a la necesidad de una conformidad normativa, los administradores comenzaron a necesitar comprender estos principios y conceptos.

El paquete de funciones de seguridad y mensajería (Messaging and Security Feature Pack) para Windows Mobile 5.0 ofrece soporte para los certificados S/MIME en teléfonos inteligentes. Además, Microsoft Exchange Server 2003 Service Pack 2 (SP2) ofrece soporte para S/MIME en Microsoft Outlook® Web Access (OWA).

En este artículo se ofrece una introducción a S/MIME y a sus conceptos relacionados y ofrece una guía normativa sobre su implementación. No es necesario disponer de conocimientos en seguridad. En este artículo se explican los conceptos generales de S/MIME para que pueda aplicarlos de manera específica en Exchange Server.

##### Ventajas de S/MIME

Antes de S/MIME, los administradores utilizaban un protocolo de correo electrónico muy extendido para transferir los mensajes, el protocolo simple de transferencia de correo (SMTP), que era intrínsecamente menos seguro. O bien, los administradores utilizaban soluciones más seguras pero de propietario. En esencia, se vieron forzados a elegir una solución que se centrara en la seguridad o en la conectividad. Con S/MIME, los administradores tienen ahora una opción de correo electrónico que ayuda a ofrecer una mayor seguridad que SMTP, lo que permite una conectividad de correo electrónico generalizada y segura.

S/MIME ofrece dos servicios de seguridad:

-   Firmas digitales

-   Cifrado de mensajes

Estos dos servicios constituyen el núcleo de la seguridad de mensajes basada en S/MIME. El resto de conceptos relacionados con la seguridad de mensajes admiten estos dos servicios. Aunque el ámbito completo de la seguridad de mensajes puede parecer complejo, estos dos servicios constituyen la base para alcanzar esa seguridad.

Las firmas digitales y el cifrado de mensajes son servicios que no se excluyen mutuamente. Cada servicio se ocupa de problemas de seguridad específicos. Las firmas digitales se encargan de los problemas de autenticación y de rechazo y el cifrado de mensajes se ocupa de los problemas de confidencialidad. Debido a que cada servicio se encarga de problemas diferentes, una estrategia de seguridad de mensajes requerirá la presencia de ambos, a menudo al mismo tiempo. Estos dos servicios se han diseñado para utilizarse de manera conjunta ya que cada uno por separado se ocupa de una de las partes en la relación remitente-destinatario. Las firmas digitales se encargan de los problemas de seguridad relacionados con los remitentes, mientras que el cifrado se encarga principalmente de los problemas de seguridad relacionados con los destinatarios.

Cuando las firmas digitales y el cifrado de mensajes se utilizan conjuntamente, los usuarios se benefician de ambos servicios. El empleo de ambos servicios en los mensajes no cambia el control o procesamiento de cada servicio.

#### Firmas digitales

Las firmas digitales son el servicio más utilizado de S/MIME. Como su propio nombre sugiere, las firmas digitales son la contrapartida digital de la firma tradicional y legal de un documento de papel. Al igual que ocurre con una firma legal, las firmas digitales proporcionan las siguientes capacidades de seguridad:

-   **Autenticación**. Una firma sirve para validar una identidad. Comprueba la respuesta a la pregunta "¿quién es?" al proporcionar los medios para diferenciar esa entidad del resto y probar que procede de un origen de confianza mutua. Puesto que no hay autenticación en el correo electrónico SMTP, no existe forma de saber quién envía realmente un mensaje. La autenticación en una firma digital ayuda a resolver este problema al permitir a un destinatario saber si el mensaje lo ha enviado la persona u organización que afirma haberlo hecho.

-   **No rechazo**. La exclusividad de una firma ayuda a impedir que el propietario de la firma rechace la firma. Esta capacidad se denomina no rechazo. De esta forma, la autenticación que proporciona una firma ofrece los medios para impedir el rechazo. El concepto de no rechazo es más conocido en el contexto de los contratos en papel: Un contrato firmado es un documento legalmente vinculante y es más difícil negar una firma autenticada. Las firmas digitales proporcionan la misma función y, cada vez más en algunas áreas, se reconocen como legalmente vinculantes, de forma parecida a las firmas en papel. Debido a que el correo electrónico SMTP no proporciona medios de autenticación, no se puede proporcionar el no rechazo. Es sencillo para un remitente negar la propiedad de un mensaje de correo electrónico SMTP.

-   **Integridad de los datos**. Un servicio de seguridad adicional que ofrecen las firmas digitales es la integridad de los datos. La integridad de los datos es el resultado de las operaciones específicas que hacen posible las firmas digitales. Con los servicios de integridad de datos, cuando el destinatario de un mensaje de correo electrónico firmado digitalmente valida la firma digital, el destinatario ayuda a garantizar que el mensaje de correo electrónico que se ha recibido es, de hecho, el mismo mensaje que ha firmado y enviado y que no se ha alterado durante el envío. Toda alteración realizada en el mensaje durante el envío tras haberse firmado anula la firma. De esta forma, las firmas digitales son capaces de contribuir a proporcionar una garantía que no pueden ofrecer las de papel, ya que resulta imposible alterar un documento en papel una vez se ha firmado.

#### Cifrado de mensajes

El cifrado de mensajes ofrece una solución a la divulgación de información. El correo electrónico de Internet basado en SMTP no protege los mensajes. Un mensaje de correo electrónico de Internet SMTP lo puede leer cualquier usuario que lo vea durante su envío o verlo en el lugar en el que se ha almacenado. S/MIME contribuye a solucionar estos problemas mediante el uso del cifrado.

El cifrado es una forma de cambiar la información para que no se pueda leer o entender hasta que se devuelve a un formato legible y compresible.

Aunque el cifrado de mensajes no se utiliza tanto como las firmas digitales, logra solucionar lo que muchas personas perciben como la debilidad más grave del correo electrónico en Internet. El cifrado de mensajes proporciona dos servicios de seguridad específicos:

-   **Confidencialidad**. El cifrado de mensajes contribuye a proteger el contenido de un mensaje de correo electrónico. Sólo el destinatario deseado puede ver el contenido y éste permanece confidencial y no puede conocerlo nadie más que quien recibirá o verá el mensaje. El cifrado permite proporcionar confidencialidad mientras el mensaje se encuentra en tránsito o almacenado.

-   **Integridad de los datos**. Al igual que con las firmas digitales, el cifrado de mensajes contribuye a proporcionar los servicios de integridad de datos como resultado de las operaciones específicas que lo hacen posible.

##### Requisitos de S/MIME

Para proporcionar confidencialidad al correo electrónico, el entorno precisa de unos componentes de software específicos. En esta sección se describen esos componentes.

#### Infraestructura de clave pública (PKI)

Las soluciones S/MIME requieren una PKI para proporcionar certificados digitales con pares clave pública/privada y permiten la asignación de certificados en el servicio de directorio Active Directory®. El estándar S/MIME especifica que los certificados digitales utilizados para S/MIME deben cumplir con el estándar X.509 de la Unión internacional de telecomunicaciones (ITU, del inglés International Telecommunications Union). La versión S/MIME 3 requiere específicamente que se cumpla con la versión 3 de X.509. Debido a que S/MIME depende de un estándar establecido y reconocido para la estructura de certificados digitales, el estándar de S/MIME se basa en el crecimiento de ese estándar y, por ese motivo, aumenta su aceptación.

Puede implementar una PKI para que admita S/MIME mediante dos formas: proporcionar la infraestructura de certificados interna a una organización externa, o utilizar Servicios de Certificate Server en Microsoft Windows Server™ 2003.

Para obtener más información acerca de los Servicios de Certificate Server de Windows Server 2003, consulte el sitio web [Infraestructura de clave pública para Windows Server 2003](http://www.microsoft.com/windowsserver2003/technologies/pki/default.mspx) en www.microsoft.com/windowsserver2003/technologies/pki/default.mspx (puede estar en inglés).

La PKI debe tener un mecanismo que se encargue de la revocación de certificados. La revocación de certificados es necesaria cuando un certificado caduca o cuando un atacante puede haber puesto en peligro un certificado. Al revocar un certificado, un administrador deniega el acceso a cualquier usuario que use el certificado. Cada certificado incluye la ubicación de su lista de revocaciones de certificados (CRL).

Para obtener más información sobre cómo administrar la revocación de certificados, consulte el tema [Administrar la revocación de certificados](http://technet2.microsoft.com/windowsserver/en/library/de0ae267-14e6-46f8-bcc7-8ac480889b951033.mspx?mfr=true) en http://technet2.microsoft.com/WindowsServer/en/Library/de0ae267-14e6-46f8-bcc7-8ac480889b951033.mspx (puede estar en inglés)

#### Plantillas de certificado

Windows Server 2003 proporciona plantillas de certificado específicas para emitir certificados digitales que pueden utilizarse con S/MIME. Se pueden utilizar tres plantillas de certificados de usuarios de varias funciones para emitir certificados para correo electrónico seguro:

-   **Administrador**. Permite a un administrador utilizar un certificado para la autenticación, el cifrado del sistema de archivo cifrado (EFS), el correo electrónico seguro y la firma de lista de confianza de certificados.

-   **Usuario**. Permite a un usuario utilizar un certificado para la autenticación, el cifrado EFS y el correo electrónico seguro.

-   **Usuario de tarjeta inteligente**. Permite a un usuario iniciar sesión con una tarjeta inteligente y firmar correo electrónico. Además, este certificado proporciona la autenticación del cliente.

**Nota**   Microsoft recomienda encarecidamente que actualice la PKI actual de Windows Server 2003 a la PKI de Windows Server 2003 con Service Pack 1 (SP1) para aprovechar las medidas de seguridad mejoradas.

Para obtener más información sobre las plantillas de certificado, consulte el tema [Plantillas de certificado](http://technet2.microsoft.com/windowsserver/en/library/7d82b420-10ef-4f20-a56f-17ee7ee352d21033.mspx) de Microsoft TechNet en http://technet2.microsoft.com/windowsserver/en/library/7D82B420-10EF-4F20-A56F-17EE7EE352D21033.mspx (puede estar en inglés).

#### Active Directory

Active Directory es un componente clave de la implementación de certificados S/MIME. Para distribuir certificados a los usuarios para que los utilicen con los servicios de correo electrónico, un administrador puede utilizar la función de inscripción automática de directivas de grupo de Active Directory. Además, Active Directory en Windows Server 2003 ofrece compatibilidad como el directorio PKI para varios clientes de correo electrónico de Microsoft, incluidos Outlook, Outlook Express y Outlook Web Access (OWA) con S/MIME y la capacidad de asignar cuentas de usuario a los certificados.

Para obtener más información sobre la asignación de certificados, consulte el tema [Asignar certificados a cuentas de usuario](http://technet2.microsoft.com/windowsserver/en/library/0539dcf5-82c5-48e6-be8a-57bca16c7e171033.mspx?mfr=true) en http://technet2.microsoft.com/WindowsServer/en/library/0539dcf5-82c5-48e6-be8a-57bca16c7e171033.mspx?mfr=true (puede estar en inglés).

#### Exchange Server 2003

Al ofrecer compatibilidad para una variedad de clientes de correo electrónico, los administradores de Exchange Server 2003 pueden personalizar la implementación para que cumpla sus necesidades específicas. La compatibilidad de S/MIME de Exchange Server 2003 para clientes se parece a la compatibilidad global para clientes en que los usuarios pueden utilizar cualquiera de los clientes admitidos al mismo tiempo. De esta forma, una solución basada en S/MIME de Exchange Server 2003 puede admitir clientes de Outlook, de OWA y de Outlook Express utilizando todos ellos POP3 al mismo tiempo. Sin embargo, puesto que el cliente de correo electrónico debe admitir la versión 3 de S/MIME y además ser un cliente de correo electrónico de Exchange compatible, no todos los clientes de correo pueden ser clientes S/MIME.

S/MIME también se incluye en Exchange Server 2000 y Exchange Server 2007.

##### Clientes de correo electrónico

Exchange Server 2003 admite clientes S/MIME a través de su compatibilidad existente con protocolos de cliente. Si un cliente compatible también admite S/MIME, ese cliente se puede utilizar con Exchange Server 2003. Si el cliente no admite la versión 3 de S/MIME, ese cliente aún podrá leer los mensajes sin firma.

#### Microsoft Outlook 2003

Outlook admite la conectividad basada en MAPI (Interfaz de programación de aplicaciones de mensajería) con Exchange Server 2003. Además, Outlook puede establecer conexión mediante POP3 e IMAP4. S/MIME de Exchange Server 2003 se puede utilizar con cualquier versión de Outlook que admita certificados digitales X.509 v3. La compatibilidad total en Outlook para los certificados digitales X.509 v3 se introdujo por primera vez con Outlook 2000 Service Release 1 (SR-1).

#### Clientes POP3 y IMAP4

Exchange Server 2003 ofrece compatibilidad completa para los clientes S/MIME mediante los protocolos estándar de correo electrónico en Internet POP3 e IMAP4, si el cliente de correo electrónico admite S/MIME versión 2 o versión 3. Cualquier cliente de correo electrónico que admita S/MIME versión 2 o versión 3, y POP3 o IMAP4, se puede utilizar como cliente de correo electrónico en un sistema de seguridad de mensajes de Exchange Server 2003. Puesto que cualquier cliente de correo electrónico que admita el estándar S/MIME proporciona compatibilidad completa para todos los servicios de seguridad de mensajes, estos clientes se pueden utilizar como clientes de correo electrónico con todas sus funciones. Microsoft proporciona compatibilidad con la versión 3 de S/MIME en clientes POP3 e IMAP4 en Outlook Express 5.5 o posterior, y en Outlook 2000 SR-1a o posterior.

**Nota**   Los diferentes estándares de Internet y clientes de correo electrónico tienen sus propios requisitos y formas de tratar los certificados X.509 v3. Preste atención a estos requisitos y problemas de compatibilidad cuando vaya a decidir qué clientes de correo electrónico se admitirán.

##### Consideraciones operativas

Tras implementar y comprobar los elementos de esta solución, debe considerar un número de actividades continuadas para garantizar que la solución seguirá funcionando correctamente para proteger con éxito la confidencialidad del correo electrónico.

Las consideraciones operativas incluyen:

-   **Aplicar Service Packs**. Entre las mejoras incluidas en Exchange Server SP2 se encuentran las realizadas en el sistema contra el correo electrónico no deseado. Para obtener más información, consulte el tema [Mejoras del sistema contra el correo electrónico no deseado en Exchange Server 2003 Service Pack 2](http://go.microsoft.com/fwlink/?linkid=55849) de TechNet en http://go.microsoft.com/fwlink/?linkid=55849 (puede estar en inglés).

-   **Aplicar las actualizaciones de seguridad más recientes**. Proteja todos sus servidores con las actualizaciones del centro de descarga de Microsoft.

-   **Anticiparse a los desafíos técnicos**. Visite con frecuencia [Microsoft Update](http://update.microsoft.com/) en http://update.microsoft.com/ para descargar e instalar otras actualizaciones de seguridad para Exchange Server y Windows Server.

-   **Ejecutar Microsoft Baseline Security Analyzer (MBSA)**. Puede realizar una búsqueda de actualizaciones de seguridad que falten en Exchange Server 2003 mediante la descarga de MBSA.

-   **Utilizar el filtro inteligente de mensajes de Microsoft Exchange Server**. Ayuda a reducir la entrada de correo no deseado cuando combina el filtro inteligente de mensajes de Exchange Server con Outlook 2003 para realizar un filtrado de mensajes avanzado en el servidor basado en heurística. Para obtener más información sobre como mantener actualizado el filtro inteligente de mensajes, consulte el artículo titulado [Ya está disponible la "Guía de operaciones del filtro inteligente de mensajes de Microsoft Exchange Server versión 2"](http://support.microsoft.com/?kbid=907747) http://support.microsoft.com/?kbid=907747 (puede estar en inglés).

-   **Ejecutar la Herramienta de análisis de procedimientos recomendados de Microsoft Exchange Server**. Esta herramienta, que se puede descargar de manera gratuita, recopila de forma remota los datos de configuración de cada servidor de la topología y los analiza automáticamente. En el informe resultante se describen con detalle los problemas de configuración críticos, los problemas potenciales y la configuración del producto no predeterminada. Si sigue estas recomendaciones, puede conseguir un mayor rendimiento, escalabilidad, confiabilidad y tiempo de actividad.

-   **Comprobar periódicamente si hay información de seguridad actualizada**. Para obtener información técnica orientativa sobre seguridad, visite la página [Biblioteca de documentación técnica de Exchange Server 2003: Seguridad y protección](http://www.microsoft.com/technet/prodtechnol/exchange/2003/security.mspx), en www.microsoft.com/technet/prodtechnol/exchange/2003/security.mspx (puede estar en inglés).

[](#mainsection)[Principio de la página](#mainsection)

### Ayuda para proteger el escenario de confidencialidad del correo electrónico

El siguiente procedimiento para proteger la confidencialidad del correo electrónico está relacionado con escenarios de pequeñas y medianas empresas y se parece al mostrado en la siguiente figura.

[![](images/Cc875813.PECRI01(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875813.pecri01_big(es-es,technet.10).gif)

**Figura 1. Servicios de correo electrónico en el entorno de TI para medianas empresas**

De manera específica, los usuarios de correo electrónico requieren la confidencialidad para el correo electrónico enviado hacia ubicaciones tanto internas como externas. Para facilitar este objetivo, implemente Exchange Server 2003 y los clientes de correo electrónico para que admitan S/MIME.

#### Ayuda para proteger la confidencialidad del correo electrónico

Los pasos siguientes identifican los procedimientos de configuración necesarios para facilitar la protección de la confidencialidad del correo electrónico.

##### Antes de comenzar

Antes de implementar S/MIME en un entorno de Exchange Server 2003, debe comprender qué le ocurrirá a los mensajes si ha implementado alguna de las siguientes opciones:

-   Receptores de eventos

-   Software antivirus

#### Receptores de eventos y mensajes firmados digitalmente

Los receptores de eventos pueden realizar acciones sobre los mensajes de correo electrónico cuando los gestiona Exchange Server. Por ejemplo, algunos receptores de eventos pueden alterar el contenido y los encabezados de un mensaje de correo electrónico con el fin de filtrar el mensaje. Una firma digital válida indica que un mensaje no se ha alterado en tránsito. Un receptor de eventos que altera el mensaje de correo electrónico anula la validez de las firmas digitales. Cuando el destinatario recibe el mensaje y procesa la firma digital, ésta no será válida ya que el receptor de eventos ha modificado el mensaje después de que lo firmara el remitente.

#### Software antivirus y mensajes S/MIME

Cuando se utiliza una solución de antivirus basada en servidor, el cifrado que ayuda a proteger la confidencialidad del cuerpo del mensaje y cualquier dato adjunto de usuarios no autorizados también impide que el software antivirus basado en servidor examine el mensaje y sus datos adjuntos en busca de virus. Como el software antivirus no puede examinar el mensaje, un mensaje cifrado podría incluir un virus en un dato adjunto. Debe determinar cómo solucionar este riesgo en función de su directiva de seguridad.

Además, si un programa antivirus detecta un virus en un mensaje de correo electrónico firmado digitalmente y limpia el mensaje, esta acción puede hacer que la firma digital no sea válida, porque el programa antivirus ha alterado el mensaje mientras estaba en tránsito. Aunque la alteración no es malintencionada, desde la perspectiva de la firma digital, el mensaje se ha modificado y, por tanto, se identificará como alterado.

##### Cómo configurar Exchange Server 2003 para contribuir a proporcionar confidencialidad al correo electrónico

Cuando Exchange Server almacena mensajes de correo electrónico S/MIME, el único requisito es que el almacén de mensajes se configure para gestionar firmas S/MIME. Puesto que los mensajes S/MIME se pueden almacenar en buzones de usuario y en carpetas públicas, tanto los almacenes públicos como los de buzón se pueden configurar para contener mensajes con firmas S/MIME.

1.  Inicie sesión con una cuenta que sea miembro de los dos grupos siguientes:

    -   El grupo Administradores del equipo local

    -   Un grupo al que se haya asignado como mínimo la función Administrador con permiso de vista de Exchange en el nivel Grupo administrativo

2.  Haga clic en **Inicio**, seleccione **Todos los programas**, elija **Microsoft Exchange** y, a continuación, haga clic en **Administrador del sistema**. Se mostrará el Administrador del sistema de Exchange (que se muestra en la siguiente captura de pantalla).

    [![](images/Cc875813.PECRI02(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875813.pecri02_big(es-es,technet.10).gif)

3.  Haga clic en **Servidores**, seleccione ***&lt;nombreServidor&gt;***, haga clic en **Grupo de almacenamiento**, haga clic con el botón secundario en **Almacén del buzón** y seleccione **Propiedades**.

    En la página **Propiedades**, active la casilla **Los clientes admiten firmas S/MIME**, que se muestra en la siguiente captura de pantalla.

    ![](images/Cc875813.PECRI03(es-es,TechNet.10).gif)

##### Cómo implementar certificados digitales para S/MIME mediante la inscripción automática

La inscripción automática permite a los clientes enviar automáticamente peticiones de certificado a una entidad de certificación (CA) y recuperar y almacenar los certificados emitidos. Los clientes de Microsoft Windows® XP y Windows Server™ 2003 pueden participar en la inscripción automática para certificados de usuario y de equipo. La inscripción automática reduce el costo total de propiedad (TCO) al reducir los costos asociados con el proceso de inscripción y renovación de certificados.

**Para habilitar la configuración de inscripción automática**

1.  Inicie sesión con derechos de administrador.

2.  En Herramientas administrativas, abra Usuarios y equipos de Active Directory.

3.  En el árbol de consola, haga clic con el botón secundario donde desee implementar la configuración de inscripción automática y, a continuación, haga clic en Propiedades.

    Para la inscripción automática, el objeto de directiva de grupo (GPO) tiene que estar vinculado al dominio o a la unidad organizativa donde se almacenan las cuentas de usuario o de equipo.

    ![](images/Cc875813.PECRI04(es-es,TechNet.10).gif)

4.  En el cuadro de diálogo **Propiedades de NombreDeDominio**, en la ficha **Directiva de grupo**, haga clic en **Abrir** para abrir la Consola de administración de directivas de grupo.

5.  Cree un a GPO vinculado al dominio.

6.  En Editor de objetos de directiva de grupo, en el árbol de consola, expanda **Configuración de usuario**.

7.  En el árbol de consola, expanda **Configuración de Windows**, expanda **Configuración de seguridad** y haga clic en **Directivas de claves públicas**, como se muestra en la siguiente captura de pantalla.

    [![](images/Cc875813.PECRI05(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875813.pecri05_big(es-es,technet.10).gif)

8.  En el panel de detalles, haga doble clic en **Configuración de inscripción automática**. En el cuadro de diálogo **Configuración de inscripción automática**, asegúrese de que estén seleccionados los siguientes valores, como se muestra en la siguiente captura de pantalla:

    -   **Registrar certificados automáticamente**. Este valor permite la inscripción automática de certificados de la unidad organizativa donde está vinculado el GPO.

    -   Casilla **Renovar certificados caducados, actualizar certificados pendientes y quitar certificados revocados**. Este valor permite la inscripción automática de certificados para la renovación de certificados, la emisión de certificados pendientes y la eliminación de certificados revocados del almacén de certificados del objeto.

    -   Casilla **Actualizar certificados que usan plantillas de certificados**. Este valor permite la inscripción automática para plantillas de certificados reemplazadas.

    ![](images/Cc875813.PECRI06(es-es,TechNet.10).gif)

9.  Haga clic en **Aceptar**.

Ahora la inscripción automática se ha habilitado para la unidad organizativa en que está vinculado el GPO.

La configuración de inscripción automática se aplicará la próxima vez que se aplique el GPO al usuario. La inscripción automática de usuarios se activa cuando el usuario realiza un inicio de sesión interactivo y en intervalos de actualización de la directiva de grupo.

Puede actualizar manualmente la configuración de GPO en un cliente que ejecute Windows XP o Windows Server 2003 si se fuerza la actualización de la directiva de grupo. Puede actualizar la configuración de GPO si ejecuta **GPUpdate /force** en el símbolo del sistema en la estación de trabajo de destino.

##### Cómo configurar Outlook 2003 para contribuir a proporcionar confidencialidad al correo electrónico

Para enviar correctamente un mensaje de correo electrónico cifrado, el destinatario debe disponer previamente de un certificado digital. Si intenta enviar un mensaje de este tipo a un usuario que no tiene un certificado digital, recibirá un error. Asegúrese de que ha seguido las instrucciones descritas en el tema anterior "Cómo implementar certificados digitales para S/MIME mediante la inscripción automática" de este artículo antes de enviar mensajes de correo electrónico a los destinatarios.

**Para configurar Outlook para proporcionar confidencialidad al correo electrónico**

1.  Inicie sesión en el dominio como miembro del grupo Usuarios del dominio.

2.  Haga clic en **Inicio**, seleccione **Todos los programas**, elija **Microsoft Office** y, a continuación, haga clic en **Microsoft** **Office Outlook 2003**.

3.  Haga clic en **Herramientas** y elija **Opciones**. Se mostrará el siguiente cuadro de diálogo.

    ![](images/Cc875813.PECRI07(es-es,TechNet.10).gif)

4.  Haga clic en la ficha **Seguridad** y elija **Configuración.**

5.  Outlook rellena el cuadro de diálogo **Cambiar la configuración de seguridad** con la información predeterminada. Haga clic en **Aceptar** para aceptar los valores predeterminados, como se muestra en la siguiente captura de pantalla.

    ![](images/Cc875813.PECRI08(es-es,TechNet.10).gif)

6.  Haga clic en **Aceptar** para cerrar el cuadro de diálogo **Opciones**.

En este punto, se ha configurado Outlook para proporcionar confidencialidad al correo electrónico.

**Para enviar un mensaje firmado digitalmente mediante Outlook**

1.  Inicie sesión en el dominio como miembro del grupo Usuarios del dominio.

2.  Haga clic en **Inicio**, seleccione **Todos los programas**, elija **Microsoft Office** y, a continuación, haga clic en **Microsoft** **Office Outlook 2003**.

3.  Para redactar un mensaje nuevo, haga clic en **Nuevo**.

4.  Agregue un destinatario para el mensaje de prueba y rellene los campos del mensaje.

5.  Asegúrese de que se ha seleccionado el botón **Agregar firma digital a este mensaje**. Puesto que desea probar únicamente la firma digital, asegúrese de que no esté seleccionado el botón **Cifrar el contenido del mensaje y de los datos adjuntos**.

    [![](images/Cc875813.PECRI09(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875813.pecri09_big(es-es,technet.10).gif)

6.  Haga clic en **Enviar**.

En este punto, se ha enviado el mensaje firmado digitalmente al destinatario, que podrá a continuación comprobar la firma digital.

**Para enviar un mensaje cifrado mediante Outlook**

1.  Inicie sesión en el dominio como miembro del grupo Usuarios del dominio.

2.  Haga clic en **Inicio**, seleccione **Todos los programas**, elija **Microsoft Office** y, a continuación, haga clic en **Microsoft** **Office Outlook 2003**.

3.  Para redactar un mensaje nuevo, haga clic en **Nuevo**.

4.  Agregue un destinatario para el mensaje de prueba y rellene los campos del mensaje.

5.  En la barra de herramientas, asegúrese de que esté seleccionado el botón **Cifrar el contenido del mensaje y de los datos adjuntos**. Puesto que desea probar únicamente el cifrado, asegúrese de que no esté seleccionado el botón **Agregar firma digital a este mensaje**.

    [![](images/Cc875813.PECRI10(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875813.pecri10_big(es-es,technet.10).gif)

En este punto, se ha enviado el mensaje cifrado al destinatario, que podrá abrirlo y leerlo.

##### Cómo configurar Outlook Express para contribuir a proporcionar confidencialidad al correo electrónico

Para enviar correctamente un mensaje de correo electrónico cifrado, el destinatario debe disponer previamente de un certificado digital. Si intenta enviar un mensaje de este tipo a un usuario que no tiene un certificado digital, recibirá un error. Asegúrese de que ha seguido las instrucciones descritas en el tema anterior "Cómo implementar certificados digitales para S/MIME mediante la inscripción automática" de este artículo antes de enviar mensajes de correo electrónico a los destinatarios.

**Para enviar un mensaje firmado digitalmente mediante Outlook Express**

1.  Inicie sesión en el dominio como miembro del grupo Usuarios del dominio.

2.  Haga clic en **Inicio**, seleccione **Todos los programas** y, a continuación, haga clic en **Outlook Express**.

3.  Si se le pide, escriba la contraseña del usuario.

4.  Para redactar un mensaje nuevo, haga clic en **Crear un mensaje**.

5.  Para agregar un destinatario de Active Directory, haga clic en **Para**.

6.  En el cuadro **Escriba el nombre o selecciónelo de la lista**, haga clic en **Buscar**. Se mostrará el siguiente cuadro de diálogo.

    ![](images/Cc875813.PECRI11(es-es,TechNet.10).gif)

7.  En la lista **Buscar en**, haga clic en **Active Directory**, en el cuadro **Nombre**, escriba el nombre del destinatario y haga clic en **Buscar ahora**.

8.  Seleccione el nombre y haga clic en **Para**.

9.  Haga clic en **Aceptar** para cerrar el cuadro **Seleccionar destinatarios**.

10. En la barra de herramientas, encontrará dos iconos nuevos: uno para cifrar mensajes y otro para firmarlos. Asegúrese de que el botón **Firmar** esté seleccionado, como se muestra en la siguiente captura de pantalla. Puesto que desea probar únicamente la firma digital, asegúrese de que no esté seleccionado el botón **Cifrar**.

    [![](images/Cc875813.PECRI12(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875813.pecri12_big(es-es,technet.10).gif)

11. Haga clic en **Enviar**.

En este punto, se ha enviado el mensaje firmado digitalmente al destinatario, que podrá comprobar la firma digital.

**Para enviar un mensaje cifrado mediante Outlook Express**

1.  Inicie sesión en el dominio como miembro del grupo Usuarios del dominio.

2.  Haga clic en **Inicio**, seleccione **Todos los programas** y elija **Outlook Express**.

3.  Si se le pide, escriba la contraseña del usuario.

4.  Para redactar un mensaje nuevo, haga clic en **Crear un mensaje**.

5.  Para agregar un destinatario de Active Directory, haga clic en **Para**.

6.  En el cuadro **Escriba el nombre o selecciónelo de la lista**, haga clic en **Buscar**.

7.  En la lista **Buscar en**, haga clic en **Active Directory**, escriba el nombre del destinatario en **Nombre** y haga clic en **Buscar ahora**.

8.  Seleccione el nombre y haga clic en **Para**.

9.  Haga clic en **Aceptar** para cerrar el cuadro **Seleccionar destinatarios**.

10. En la barra de herramientas, asegúrese de que esté seleccionado el botón **Cifrar**, como se muestra en la siguiente captura de pantalla. Puesto que desea probar únicamente el cifrado, asegúrese de que no esté seleccionado el botón **Firmar**.

    [![](images/Cc875813.PECRI13(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875813.pecri13_big(es-es,technet.10).gif)

11. Haga clic en **Enviar**.

En este punto, se ha enviado el mensaje cifrado al destinatario, que podrá abrirlo y leerlo.

##### Cómo comprobar que el usuario tiene un certificado digital para S/MIME en Active Directory

Puede utilizar la opción Usuarios y equipos de Active Directory para comprobar que una cuenta de usuario de Active Directory tiene un certificado digital para S/MIME.

**Para comprobar que el certificado se ha agregado a la cuenta Active Directory del usuario**

1.  Inicie sesión en el dominio como miembro del grupo de administradores de la entidad de certificación.

2.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Herramientas administrativas** y haga clic en **Usuarios y equipos de** **Active Directory**.

3.  Haga clic en **Ver** y, a continuación, en **Características avanzadas,** como se muestra en la siguiente captura de pantalla.

    [![](images/Cc875813.PECRI14(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875813.pecri14_big(es-es,technet.10).gif)

4.  En el panel izquierdo, haga clic en la carpeta **Usuarios**.

5.  En el panel derecho, haga doble clic en uno de los usuarios de prueba.

6.  Haga clic en la ficha **Certificados publicados**.

7.  En la **Lista de certificados X509 publicados para la cuenta del usuario** (que se muestra en la siguiente captura de pantalla), verá el certificado digital del usuario procedente de la entidad de certificación de Windows junto con cualquier otro certificado digital almacenado para este usuario en Active Directory.

    ![](images/Cc875813.PECRI15(es-es,TechNet.10).gif)

En este punto, se ha realizado la comprobación de que el certificado se ha agregado a la cuenta de usuario de Active Directory.

##### Cómo comprobar que Exchange Server está configurado para contribuir a proporcionar confidencialidad al correo electrónico

Puede utilizar el administrador de sistema del servidor de Microsoft Exchange para comprobar que el servidor de Microsoft Exchange se ha configurado para que admita clientes que utilizan S/MIME.

1.  Inicie sesión con una cuenta que sea miembro de los dos grupos siguientes:

    -   El grupo Administradores del equipo local.

    -   Un grupo al que se haya asignado como mínimo la función Administrador con permiso de vista de Exchange en el nivel Grupo administrativo

2.  Haga clic en **Inicio**, seleccione **Todos los programas**, elija **Microsoft Exchange** y, a continuación, haga clic en **Administrador del sistema**.

3.  Haga clic en **Servidores** y en ***&lt;nombre del servidor&gt;***, seleccione **Grupo de almacenamiento**, haga clic con el botón secundario en **Almacén del** **buzón** o en **Almacén de carpetas públicas** y haga clic en **Propiedades**.

4.  En la página **Propiedades**, compruebe que la casilla **Los clientes admiten firmas S/MIME** de la ficha **General** está activada, tal como se muestra en la captura de pantalla siguiente.

    ![](images/Cc875813.PECRI16(es-es,TechNet.10).gif)

En este punto, se ha realizado la comprobación de que Exchange Server está configurado para permitir la confidencialidad del correo electrónico.

##### Cómo comprobar que Outlook 2003 puede recibir correo electrónico configurado para contribuir a proporcionar confidencialidad al correo electrónico

Puede utilizar Outlook 2003 para comprobar que puede recibir mensajes de correo electrónico configurados para cifrado y firmas digitales.

**Para ver un mensaje firmado digitalmente con Outlook**

1.  Inicie sesión en el dominio como miembro del grupo Usuarios del dominio.

2.  Haga clic en **Inicio**, seleccione **Todos los programas**, elija **Microsoft Office** y, a continuación, haga clic en **Microsoft** **Office Outlook 2003**.

3.  En la bandeja de entrada, busque el mensaje de prueba firmado digitalmente y haga doble clic en él.

4.  Cuando se abra el mensaje, haga clic en el botón **Comprobar firma** (que se muestra en la captura de pantalla siguiente) para comprobar la firma.

    [![](images/Cc875813.PECRI17(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875813.pecri17_big(es-es,technet.10).gif)

    Después de hacer clic en el botón **Comprobar firma**, aparece el cuadro de diálogo **Firma digital** (que se muestra en la captura de pantalla siguiente), que indica que la firma digital es válida.

    ![](images/Cc875813.PECRI18(es-es,TechNet.10).gif)

En este punto, se ha comprobado la firma digital del mensaje.

**Para ver un mensaje cifrado con Outlook**

1.  Inicie sesión en el dominio como miembro del grupo Usuarios del dominio.

2.  Haga clic en **Inicio**, seleccione **Todos los programas**, elija **Microsoft Office** y, a continuación, haga clic en **Microsoft** **Office Outlook 2003**.

3.  En la bandeja de entrada, busque el mensaje de prueba cifrado y haga doble clic en él.

4.  Cuando se abra el mensaje, haga clic en el botón **Comprobar firma** (que se muestra en la captura de pantalla siguiente) para comprobar el cifrado.

    [![](images/Cc875813.PECRI19(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875813.pecri19_big(es-es,technet.10).gif)

5.  Después de hacer clic en el botón **Comprobar cifrado**, aparece el cuadro de diálogo **Propiedades de seguridad del mensaje** siguiente, que indica que el mensaje cifrado es válido.

    ![](images/Cc875813.PECRI20(es-es,TechNet.10).gif)

En este punto, se ha comprobado el cifrado del mensaje.

Una vez que haya llevado a cabo estos pasos, se habrán comprobado todos los elementos para el uso de S/MIME en Outlook 2003. Esta información le permite ver cómo funcionará para los usuario un sistema S/MIME que utilice Outlook.

##### Cómo comprobar que Outlook Express puede recibir correo electrónico configurado para contribuir a proporcionar confidencialidad al correo electrónico

Puede utilizar Outlook Express para comprobar que puede recibir mensajes de correo electrónico configurados para cifrado y firmas digitales.

**Para ver un mensaje firmado digitalmente con Outlook Express**

1.  Inicie sesión en el dominio como miembro del grupo Usuarios del dominio.

2.  Haga clic en **Inicio**, seleccione **Todos los programas** y elija **Outlook Express**.

3.  Si se le pide, escriba la contraseña de usuario.

4.  En la bandeja de entrada, busque el mensaje de prueba firmado digitalmente y haga doble clic en él.

5.  Cuando se abre el mensaje, Outlook Express muestra el siguiente mensaje con una explicación de las firmas digitales. Active la casilla **No volver a mostrar esta pantalla de Ayuda** y haga clic en **Continuar**.

    [![](images/Cc875813.PECRI21(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875813.pecri21_big(es-es,technet.10).gif)

6.  Para comprobar la firma, haga clic en el botón **Comprobar firma**.

    Después de hacer clic en el botón **Comprobar firma**, se muestra el siguiente cuadro de diálogo de **comprobación de firma digital**, que indica que la firma digital es válida.

    ![](images/Cc875813.PECRI22(es-es,TechNet.10).gif)

En este punto, se ha comprobado la firma digital del mensaje.

**Para ver un mensaje cifrado con Outlook Express**

1.  Inicie sesión en el dominio como miembro del grupo Usuarios del dominio.

2.  Haga clic en **Inicio**, seleccione **Todos los programas** y elija **Outlook Express**.

3.  Si se le pide, escriba la contraseña del usuario.

4.  En la bandeja de entrada, busque el mensaje de prueba cifrado y haga doble clic en él.

5.  Cuando se abre el mensaje, Outlook Express muestra el siguiente mensaje con una explicación del cifrado. Active la casilla **No volver a mostrar esta pantalla de Ayuda** y haga clic en **Continuar**.

    [![](images/Cc875813.PECRI23(es-es,TechNet.10).gif)](https://technet.microsoft.com/es-es/cc875813.pecri23_big(es-es,technet.10).gif)

6.  Para comprobar la firma, haga clic **Comprobar cifrado**.

    Tras hacer clic en el botón **Comprobar cifrado**, se mostrará el siguiente cuadro de diálogo de **prueba de cifrado**, en el que se indica que el mensaje cifrado es válido.

    ![](images/Cc875813.PECRI24(es-es,TechNet.10).gif)

En este punto, se ha comprobado el cifrado del mensaje.

Tras completar estos pasos, habrá probado todos los elementos de utilizar S/MIME en Outlook Express. Esta información le permite ver cómo funcionará para sus usuarios el sistema S/MIME que utiliza Outlook Express.

##### Cómo solucionar problemas de correo electrónico para contribuir a proporcionar la confidencialidad

En esta sección se describe un número de problemas comunes que se producen en un sistema S/MIME basado en Exchange Server 2003. Aunque la lista no es exhaustiva, proporciona información sobre problemas que podrían producirse en la implementación, así como recomendaciones sobre cómo resolver estos problemas.

#### Problema: No se puede comprobar la firma digital del remitente

Este problema puede producirse cuando el certificado digital de la entidad de certificación raíz o el certificado digital de la entidad de certificación intermedia del remitente no está presente en el servidor Exchange del destinatario.

#### Solución

Para resolver este problema, importe el certificado digital de la entidad de certificación raíz o la entidad de certificación del remitente en la carpeta Entidades emisoras de certificados raíz de confianza en el almacén de certificados del equipo local del servidor Exchange del destinatario. La importación del certificado digital para una entidad de certificación raíz otorga confianza, de manera inherente, a todos los certificados digitales emitidos por la jerarquía de las entidades de certificación raíz. Esas organizaciones para las que la concesión de esta confianza está prohibida por su directiva de seguridad desearán explorar la alternativa de las estrategias de certificados cruzados. Para obtener más información sobre cómo implementar la certificación cruzada cuando utilice Windows Server 2003 CA, consulte [Planeamiento e implementación de la certificación cruzada y la subordinación completa mediante Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=17806) en http://go.microsoft.com/fwlink/?LinkId=17806 (puede estar en inglés).

**Para importar el certificado digital de la entidad de certificación raíz del remitente en las entidades emisoras raíz de confianza**

1.  Inicie sesión en el servidor Exchange del destinatario con una cuenta que sea miembro del grupo de administradores locales.

2.  En el menú **Inicio**, haga clic en **Ejecutar**, escriba **mmc** y haga clic en **Aceptar**.

3.  Haga clic en **Archivo** y después en **Agregar o quitar complemento**.

4.  En la ficha **Independiente**, haga clic en **Agregar**.

5.  Seleccione **Certificados** y, a continuación, haga clic en **Agregar**. Cuando se le pida, seleccione **Cuenta de equipo** y haga clic en **Siguiente**.

6.  En la página **Seleccionar equipo**, seleccione **Equipo local: (el equipo en el que se está ejecutando esta consola)** y, a continuación, haga clic en **Finalizar**.

7.  En MMC, expanda **Certificados (equipo local)** y **Entidades emisoras** **raíz de confianza**.

8.  En el panel de detalles, haga clic con el botón secundario y seleccione **Todas las tareas** y haga clic en **Importar**.

9.  En la primera página del Asistente para importación de certificados, haga clic en **Siguiente**.

10. En el cuadro de diálogo **Nombre de archivo**, escriba el nombre y la ubicación del archivo que contiene el certificado digital de la entidad de certificación raíz y, a continuación, haga clic en **Siguiente**.

11. En la página **Almacén de certificados**, haga clic en **Colocar todos los certificados en el siguiente almacén**, asegúrese de que en el cuadro de diálogo **Almacén de certificados** muestre **Entidades emisoras raíz de confianza** y haga clic en **Siguiente**.

12. En la última página del asistente, haga clic en **Finalizar**.

Tras importar el certificado digital de la entidad de certificación raíz del remitente, Exchange Server podrá validar el certificado digital del remitente en nombre del destinatario.

**Para importar el certificado digital de las entidades emisoras intermedias del remitente en las entidades emisoras de certificados intermedias**

1.  Inicie sesión en el servidor Exchange del destinatario con una cuenta que sea miembro del grupo de administradores locales.

2.  En el menú **Inicio**, haga clic en **Ejecutar**, escriba **mmc** y haga clic en **Aceptar**.

3.  Haga clic en **Archivo** y después en **Agregar o quitar complemento**.

4.  En la ficha **Independiente**, haga clic en **Agregar**.

5.  Seleccione **Certificados** y, a continuación, haga clic en **Agregar**. Cuando se le pida, seleccione **Cuenta de**  **equipo** y, a continuación, haga clic en **Siguiente**.

6.  En la página **Seleccionar equipo**, seleccione **Equipo local: (el equipo en el que se está ejecutando esta consola)** y, a continuación, haga clic en **Finalizar**.

7.  En MMC, expanda **Certificados (equipo local)** y **Entidades emisoras** **de certificados intermedias**.

8.  En el panel de detalles, haga clic con el botón secundario y seleccione **Todas las tareas** y haga clic en **Importar**.

9.  En la primera página del Asistente para importación de certificados, haga clic en **Siguiente**.

10. En el cuadro de diálogo **Nombre de archivo**, escriba el nombre y la ubicación del archivo que contiene el certificado digital de la entidad de certificación raíz y, a continuación, haga clic en **Siguiente**.

11. En la página **Almacén de certificados**, haga clic en **Colocar todos los certificados en el siguiente almacén**, asegúrese de que en el cuadro de diálogo **Almacén de certificados** muestre **Entidades emisoras de certificados intermedias** y haga clic en **Siguiente**.

12. En la última página del asistente, haga clic en **Finalizar**.

Tras importar el certificado digital de la entidad de certificación intermedia del remitente, Exchange Server podrá validar correctamente el certificado digital del remitente en nombre del destinatario.

#### Problema: No se tiene acceso a la lista CRL

Este problema puede producirse cuando el punto de distribución de la lista de revocaciones de certificados (CRL) especificado en los certificados digitales sólo es accesible a través de un firewall, o cuando el servidor Exchange del usuario carece de los derechos para tener acceso al punto de distribución de la lista CRL.

#### Solución

Para resolver este problema, realice una de las siguientes opciones:

-   Descargue manualmente la lista CRL del punto de distribución CRL e impórtela en el almacén de certificados del equipo local del servidor Exchange del usuario.

-   Instale y configure un cliente de firewall para los protocolos adecuados en el servidor Exchange del destinatario.

-   Conceda de manera explícita permiso para la cuenta LocalSystem del servidor Exchange del usuario para tener acceso al punto de distribución CRL o vuelva a configurar el punto de distribución CRL para que no requiera autenticación.

**Para importar manualmente una lista CRL**

1.  Inicie sesión en el servidor Exchange del destinatario con una cuenta que sea miembro del grupo de administradores locales.

2.  Descargue la lista CRL del punto de distribución CRL especificado en el certificado digital.

3.  Haga clic con el botón secundario en el archivo **.cer** o **.crl**, seleccione **Instalar certificado** o **Instalar CRL** y haga clic en **Siguiente**.

4.  Cuando se abra el Asistente para importación de certificados, haga clic en **Seleccionar automáticamente el almacén de certificados en base al tipo de certificado**.

#### Problema: Se utilizan certificados diferentes cuando se usan clientes de correo electrónico diferentes

Este problema puede producirse porque hay dos atributos en Active Directory en los que se pueden almacenar certificados digitales de S/MIME: el atributo **userCertificate** y el atributo **userSMIMECertificate**. De manera predeterminada, Outlook busca primero en el atributo **userSMIMECertificate** y utiliza cualquier certificado S/MIME válido que detecte en ese atributo. Hay otros clientes de correo electrónico, incluido OWA, que es posible que busquen primero en el atributo **userCertificate** y que utilicen cualquier certificado S/MIME válido que detecte en ese atributo.

Si se almacenan certificados digitales diferentes en los atributos **userCertificate** y **userSMIMECertificate**, es posible que Outlook y OWA utilicen certificados digitales diferentes ya que cada uno hace referencia a atributos diferentes de Active Directory.

#### Solución

Para solucionar este problema, asegúrese de que los mismos certificados se almacenan los dos atributos, **userCertificate** y **userSMIMECertificate**. Para obtener más información, consulte el artículo "[Outlook 2003 continúa utilizando certificados antiguos después de migrar de Servidor de administración de claves a Infraestructura de clave pública](http://go.microsoft.com/fwlink/?linkid=3052&kbid=822504)" en http://go.microsoft.com/fwlink/?linkid=3052&kbid=822504 (puede estar en inglés).

#### Problema: Outlook Express intenta firmar automáticamente los mensajes de correo electrónicos

De manera predeterminada, cuando un usuario responde a un mensaje firmado, o lo reenvía, mientras utiliza Outlook Express, Outlook Express permite la firma digital de ese mensaje. Si a continuación el usuario intenta enviar el mensaje y no tiene un certificado de firma válido, Outlook Express muestra un mensaje de error "**No tiene un identificador digital.**" y no envía el mensaje.

#### Solución

Para solucionar este problema, deshabilite la firma digital para ese mensaje. Para obtener más información, consulte el artículo "[Recibe un mensaje de error cuando intenta reenviar o responder a un mensaje de correo electrónico firmado digitalmente](http://go.microsoft.com/fwlink/?linkid=3052&kbid=816830)" en http://go.microsoft.com/fwlink/?linkid=3052&kbid=816830 (puede estar en inglés).

[](#mainsection)[Principio de la página](#mainsection)

### Resumen

Debido al crecimiento de Internet en los últimos años, los fundamentos del correo electrónico han cambiado. Ya no constituye únicamente una herramienta organizativa interna. En lugar de eso, ahora une a personas entre compañías y países o regiones e incluso ha permitido a personas de la tierra compartir información con personas en el espacio, como si se encontraran en el mismo edificio. Se puede afirmar que el correo electrónico se ha convertido en la ventaja más importante que ofrece Internet hasta la fecha. Las personas y compañías integran cada vez más el correo electrónico en sus vidas por lo que su importancia crece cada día.

El crecimiento sin precedentes del correo electrónico ha sido posible gracias a la adopción en todo el mundo del protocolo subyacente o lenguaje de correo electrónico de Internet: SMTP. El estándar SMTP permite que diferentes sistemas de correo electrónicos conectados Internet intercambien información entre sí.

Sin embargo, a pesar de todas las ventajas que ha aportado SMTP a Internet, tiene un problema inherente. El estándar SMTP se desarrolló originalmente para transportar mensajes breves y relativamente poco importantes en una red cerrada y no para transportar información vital y confidencial en un mundo interconectado. Ninguno de los creadores del estándar SMTP llegó a imaginar el papel que desempeñaría en el presente. Por este motivo, SMTP no se diseñó para proteger el tipo de información que transporta por las redes que utiliza hoy en día. Se diseñó para transportar información más simple a través de redes más simples, de ahí el nombre Protocolo simple de transferencia de correo (SMTP). Por ejemplo, SMTP envía la información a través de Internet mediante un método que permite a cualquiera leer el mensaje.

Afortunadamente, S/MIME ha surgido como estándar para contribuir a mejorar los mensajes de correo electrónico y las capacidades de seguridad de SMTP. Con S/MIME, el cifrado ayuda a proteger el contenido de los mensajes de correo electrónico, mientras que las firmas digitales permiten comprobar la identidad del supuesto remitente de un correo electrónico.

La implementación de S/MIME en el correo electrónico requiere una solución que abarque varios productos y tecnologías.

[](#mainsection)[Principio de la página](#mainsection)

**Descargar**

[Obtener el artículo Cómo proteger la confidencialidad del correo electrónico en sectores regulados](http://go.microsoft.com/fwlink/?linkid=71176)

[](#mainsection)[Principio de la página](#mainsection)
