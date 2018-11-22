---
TOCTitle: Operación de un servidor de RMS
Title: Operación de un servidor de RMS
ms:assetid: '1533426b-89c2-43e0-8068-ca97ddab8606'
ms:contentKeyID: 18127733
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720205(v=WS.10)'
---

Operación de un servidor de RMS
===============================

Operación de un servidor de RMS hace referencia a las tareas de administración que se llevan a cabo después de implementar RMS en una organización. En este tema se proporciona información de ayuda para administrar el servidor de RMS, procedimientos para tareas administrativas comunes y recursos para obtener información adicional, así como información sobre procedimientos recomendados.

En este tema

-   [Administración de RMS](https://technet.microsoft.com/9b573c55-c14c-436c-b3c5-7ba445de1562)
-   [RMS Cómo...](https://technet.microsoft.com/82032075-f361-438f-a2c4-93ab29ae6cff)
-   [Recursos de RMS](https://technet.microsoft.com/d91221cf-e38e-4add-b7b9-50e63aad9a28)

Terminología utilizada en esta guía
-----------------------------------

**certificación de cuentas**  
Proceso que asocia cuentas de usuario con pares de claves en el certificado de cuenta de permisos o RAC.

<!-- -->

**servicio de certificación de cuentas**  
Servicio Web de RMS que crea y distribuye certificados de cuenta de RM. Vea también certificación de cuentas.

<!-- -->

**servicio proxy de activación**  
Servicio Web de RMS que admite la activación de equipos cliente de RMS versión 1.0. Se utiliza para reenviar solicitudes de activación de equipos al servicio de activación de Microsoft. El servicio de activación genera una caja de seguridad exclusiva y un certificado de equipo de RMS coincidente para el equipo cliente, que el servicio de proxy de activación del RMS reenvía de vuelta, a continuación, al cliente que realiza la solicitud. Vea también caja de seguridad.

<!-- -->

**servicio de administración**  
Servicio Web de RMS que aloja el sitio Web de administración. Permite la administración de RMS y actualiza la base de datos de configuración del clúster.

<!-- -->

**manifiesto de la aplicación**  
Documento XML que describe los módulos de una aplicación asociada compatible con RMS y lo que se puede ejecutar en el entorno de la aplicación. Cualquier aplicación que escriba en las interfaces de programación de aplicaciones (API) del cliente de RMS para crear o utilizar información protegida con RMS debe proporcionar un manifiesto en tiempo de ejecución.

<!-- -->

**atributo**  
En Active Directory, propiedad de un objeto. El esquema define, para cada clase de objeto, los atributos que una instancia de la clase debe tener y los atributos adicionales que puede tener.

<!-- -->

**enlace**  
Mecanismo que ejerce permisos en un sistema de RMS, en el que el cliente de RMS valida las condiciones de uso de una licencia comparándolas con los permisos que se solicitan. Si se cumplen las condiciones, se conceden los permisos.

<!-- -->

**certificado**  
Documento digital que se utiliza habitualmente para autenticación y para proteger información en redes abiertas. Un certificado enlaza de forma segura una clave pública con la entidad que ostenta la clave privada correspondiente. La entidad emisora de certificados (CA) firma digitalmente los certificados, que se pueden emitir para un usuario, un equipo o un servicio. Vea también clave privada; clave pública.

<!-- -->

**inscripción de clientes**  
Proceso de creación del certificado emisor de licencias de cliente, que permite al dispositivo o equipo del usuario crear licencias de publicación que aceptará un servidor de licencias.

<!-- -->

**certificado emisor de licencias de cliente**  
Certificado creado por un servidor de RMS y ubicado en equipos cliente de RMS, que permite a los usuarios publicar contenido protegido fuera de línea sin estar conectados a la red compatible con RMS. El certificado emisor de licencias de cliente contiene la clave que el cliente de RMS utiliza para firmar digitalmente las licencias de publicación.

<!-- -->

**condición**  
Conjunto de parámetros y restricciones especificadas que forman parte de los grupos de permisos que se incluyen en una licencia de publicación. Se aplican en el momento de su utilización. Una condición temporal es una condición común que permite a un usuario definir una fecha de caducidad para información protegida con RMS.

<!-- -->

**base de datos de configuración**  
Base de datos que contiene la información de configuración de RMS para un servidor o clúster.

<!-- -->

**utilizar el contenido**  
Descifrar y ejercer los permisos de uso de un fragmento de contenido protegido.

<!-- -->

**clave de contenido**  
Clave utilizada para cifrar y descifrar contenido protegido durante la publicación y la utilización. También se conoce como clave simétrica. RMS utiliza claves de contenido AES de 128 bits.

<!-- -->

**propietario del contenido**  
Persona u organización que establece la política de acceso al contenido protegido.

<!-- -->

**descifrado**  
Proceso por el cual los datos cifrados se pueden volver a leer mediante la conversión de texto cifrado en texto no cifrado.

<!-- -->

**firma digital**  
Medio a través del cual los originadores de un mensaje, archivo u otra información codificada digitalmente enlazan su identidad con la información. El proceso de firma digital de información conlleva transformar la información, así como información secreta que posee el emisor, en una etiqueta denominada firma. Las firmas digitales se utilizan en entornos de claves públicas y proporcionan servicios de no rechazo e integridad.

<!-- -->

**servicio DRMRemote**  
Servicio Web de RMS que expone servicios a través de .NET Remoting, que se utiliza para la comunicación entre diferentes servidores de RMS.

<!-- -->

**cifrado**  
Proceso de convertir información en un formato que sólo puede leer un receptor específico. El cifrado es un modo efectivo para ayudar a mantener la información protegida. Para descifrar un archivo que se ha cifrado, el receptor debe tener la clave secreta o la contraseña que lo traducirá. Vea también cifrado de claves públicas.

<!-- -->

**inscripción**  
Proceso por el que el servidor de certificación raíz obtiene un certificado emisor de licencias de servidor firmado por el servicio de inscripción de Microsoft.

<!-- -->

**solicitud de inscripción**  
Solicitud enviada por el servidor de certificación raíz de RMS al servicio de inscripción de Microsoft para obtener un certificado emisor de licencias de servidor.

<!-- -->

**exclusion**  
Proceso utilizado por el servidor de RMS para denegar una solicitud de licencia de uso a un cliente basándose en una directiva de exclusión. Vea también lista de exclusión.

<!-- -->

**lista de exclusión**  
Lista de entidades principales a las que el servicio de emisión de licencias de RMS debe denegar licencias.

<!-- -->

**directiva de exclusión**  
Configuración de la base de datos de configuración de RMS que controla la forma en que se aplica la exclusión en la organización.

<!-- -->

**Lenguaje de marcado de permisos extensible**  
El formato basado en XML que RMS utiliza para todas las licencias compatibles: certificados de equipo, certificados RAC, CLC, licencias de uso, licencias de publicación y certificados emisores de licencia de servidor, que son documentos que especifican la directiva de RMS que se aplica al contenido protegido.

<!-- -->

**licencia de emisión**  
Datos que especifican la directiva de RMS que se aplica al contenido protegido.

<!-- -->

**clúster de licencias**  
Uno o varios servidores que ejecutan servicios de publicación y emisión de licencias de RMS fuera del clúster de certificación raíz. Estos servidores utilizan una base de datos y una dirección URL comunes, y deben implementarse detrás de un equilibrador de carga de software o de hardware si se usa más de un servidor. A diferencia de un clúster raíz o de certificación, los servidores de RMS de un clúster de licencias no pueden realizar certificación de usuario.

<!-- -->

**servidor de licencias**  
Servidor que ejecuta los servicios de publicación y emisión de licencias de RMS fuera del clúster de certificación raíz.

<!-- -->

**servicio de emisión de licencias**  
Servicio Web de RMS que concede licencias de uso.

<!-- -->

**caja de seguridad**  
Módulo de software responsable de autenticar el uso válido de contenido protegido, de cifrar y descifrar la información, así como de proteger el procesamiento de software de confianza frente a modificaciones y observaciones. También se conoce como repositorio seguro.

<!-- -->

**servicio de registro**  
Servicio de escucha de RMS que transfiere los datos registrados de la cola de mensajes a la base de datos de registro del clúster o servidor de RMS.

<!-- -->

**activación de equipo**  
Proceso de obtención de una caja de seguridad única y un certificado de equipo para un equipo en RMS versión 1.0. En SP1 de RMS versión 1.0, la activación de equipo es el proceso de obtención de un certificado de equipo para cada usuario de dicho equipo.

<!-- -->

**manifiesto**  
Documento XML firmado que identifica las bibliotecas o programas que se pueden y no se pueden cargar en el espacio de procesamiento de la aplicación.

<!-- -->

**servicio de activación de Microsoft (Microsoft Activation Service)**  
Servicio Web alojado por Microsoft que concede certificados de equipo de RMS y cajas de seguridad en respuesta a las solicitudes de clientes de RMS versión 1.0.

<!-- -->

**servicio de inscripción de Microsoft (Microsoft Enrollment Service)**  
Servicio Web alojado por Microsoft que concede un certificado emisor de licencias de servidor al servidor de certificación raíz de una implementación de RMS.

<!-- -->

**precertificación**  
Característica del servicio de certificación de RMS que permite a una aplicación solicitar un certificado de cuenta de permisos desde el servidor de RMS en nombre de un usuario. Los certificados de cuenta de permisos obtenidos mediante precertificación sólo contienen la clave pública del usuario.

<!-- -->

**entidad principal**  
Entidad (como un usuario, grupo o administrador de contenido protegido) que tiene una función establecida en el esquema de seguridad de RMS y mediante la cual se pueden proteger objetos.

<!-- -->

**clave privada**  
Mitad secreta de un par de claves criptográficas que se utiliza con un algoritmo de clave pública. Las claves privadas se suelen utilizar para descifrar una clave de sesión simétrica, firmar datos digitalmente o descifrar datos que se hayan cifrado con la correspondiente clave pública. Vea también clave pública; cifrado de claves públicas.

<!-- -->

**establecer servicios en línea**  
Configurar un servidor de RMS para trabajar en una organización.

<!-- -->

**clave pública**  
Mitad no secreta de un par de claves criptográficas que se utiliza con un algoritmo de clave pública. Las claves públicas se suelen utilizar para cifrar una clave de sesión, verificar un firma digital o cifrar datos que se pueden descifrar con la clave privada correspondiente. Vea también clave privada; cifrado de claves públicas.

<!-- -->

**cifrado de claves públicas**  
Método de cifrado en el que se utilizan dos claves de cifrado relacionadas matemáticamente. Una clave se denomina clave privada y es confidencial. La otra se denomina clave pública y se concede libremente a todos los comunicantes posibles. En una situación habitual, un emisor utiliza la clave pública del receptor para cifrar un mensaje. El receptor es el único que tiene la clave privada relacionada para descifrar el mensaje. La complejidad de la relación entre la clave privada y la clave privada hace que, siempre que las claves sean lo suficientemente largas, no sea factible por medios informáticos distinguir la una de la otra. También se denomina cifrado asimétrico. Vea también clave privada; clave pública.

<!-- -->

**licencia de publicación**  
Licencia creada al publicar contenido protegido con RMS. Entre otras cosas, especifica quién y bajo qué condiciones puede tener acceso al contenido, así como qué permisos se conceden. También se conoce como licencia de emisión.

<!-- -->

**servicio de publicación**  
Servicio de RMS que firma licencias de publicación y emite certificados emisores de licencias de cliente. Vea también certificado emisor de licencias de cliente; licencia de publicación.

<!-- -->

**RAC**  
Vea la definición de certificado de cuenta de permisos.

<!-- -->

**revocation**  
Proceso por el que las licencias de las entidades se marcan como no válidas.

<!-- -->

**lista de revocaciones**  
Documento XrML que muestra los certificados que han sido revocados por el emisor. Vea también revocación.

<!-- -->

**permiso**  
Acción permitida a los usuarios especificados sobre el contenido protegido con la tecnología de RMS. Estos permisos se pueden restringir más aún mediante condiciones.

<!-- -->

**certificado de cuenta de permisos (RAC)**  
Certificado que utiliza el certificado de equipo de la activación de RMS para enlazar la cuenta y la clave de un usuario con un equipo específico o grupos de equipos. Los componentes del certificado se utilizan para permitir a los consumidores utilizar contenido protegido. También se conoce como certificado de identidad de grupo (GIC) en el SDK de RMS.

<!-- -->

**administración de permisos**  
Tecnología que proporciona protección permanente para información digital mediante cifrado, certificados y autenticación. Los usuarios o destinatarios autorizados deben adquirir una licencia para utilizar los archivos protegidos, de acuerdo con los permisos o las reglas empresariales definidas por el propietario del contenido.

<!-- -->

**cliente de Rights Management Services**  
Conjunto de interfaces de programación de aplicaciones (API) de RMS que cada equipo cliente de un sistema RMS debe instalar. Es un requisito previo para la activación del equipo y es necesario para utilizar aplicaciones compatibles con RMS.

<!-- -->

**plantilla de directiva de permisos**  
Describe un conjunto estándar de usuarios, permisos y condiciones que se pueden aplicar al contenido protegido con RMS. Cuando un usuario aplica una plantilla de directiva de permisos a un fragmento de contenido, los permisos y condiciones que describe se convierten en parte de la licencia de publicación.

<!-- -->

**activación de RMS**  
Proceso consistente en colocar una caja de seguridad en el equipo de un usuario final en RMS versión 1.0. Sólo lo puede proporcionar el servicio de activación de RMS y es esencial para utilizar la tecnología de RMS. En SP1 de RMS versión 1.0, es el proceso de obtener un certificado de equipo para un usuario de dicho equipo y no requiere conexión con el servicio de activación de RMS. También se conoce como activación.

<!-- -->

**servicio de certificación de RMS**  
Servicio Web alojado por Microsoft que emite certificados de cuenta de permisos a usuarios basándose en sus credenciales de Microsoft .NET Passport.

<!-- -->

**cliente de RMS**  
Conjunto de interfaces de programación de aplicaciones (API) de RMS que cada equipo cliente de un sistema RMS debe instalar. Es un requisito previo para la activación del equipo y es necesario para utilizar aplicaciones compatibles con RMS.

<!-- -->

**certificado de equipo de RMS**  
Certificado colocado en el equipo de un usuario final durante la activación de RMS. La clave pública en este certificado se usa para cifrar la clave privada del usuario contenida en los certificados de cuenta de permisos del usuario.

<!-- -->

**aplicación compatible con RMS**  
An application that has been extended by using the Rights Management Services SDK to allow users to specify the rights attached to content that they create.

<!-- -->

**equipo compatible con RMS**  
Equipo que tiene el componente cliente de RMS instalado y que se ha sometido a una activación de equipo de RMS para poder procesar contenido protegido con RMS.

<!-- -->

**contenido protegido con RMS**  
Información digital protegida con la tecnología de RMS.

<!-- -->

**clúster de certificación raíz**  
Uno o varios servidores de una implementación de RMS que ejecutan servicios de administración, inscripción, certificación de cuentas, proxy de activación, licencias y publicación. Estos servidores utilizan una dirección URL de conexión y una base de datos comunes, y deben implementarse detrás de un equilibrador de carga de software o hardware. Sólo puede haber un clúster de certificación raíz para el bosque de Active Directory.

<!-- -->

**servidor de certificación raíz**  
Servidor principal de una implementación de RMS que ejecuta servicios de administración, inscripción, certificación de cuentas, proxy de activación, licencias y publicación. Sólo puede haber un servidor de certificación raíz por bosque de Active Directory.

<!-- -->

**raíz de confianza**  
Entidad de confianza que proporciona la base para establecer la confianza de otros certificados. Todos los proveedores de certificados y el usuario final deben confiar en la raíz.

<!-- -->

**ID de seguridad (SID)**  
Estructura de datos de Windows que identifica las cuentas de usuario, de grupo y de equipo de Windows. Para cada cuenta de una red se emite un SID exclusivo al crearla. Los procesos internos de Windows consultan el id. de la cuenta antes que el nombre de usuario o de grupo de la cuenta.

<!-- -->

**certificado emisor de licencias de servidor**  
Certificado que establece las credenciales del servidor de RMS, haciendo que sea un servicio de emisión de licencias y certificación válido, y permitiendo que se ejecute. El certificado emisor de licencias contiene la clave pública que se utiliza para cifrar las claves de contenido en licencias de publicación.

<!-- -->

**servicio de servidor**  
Servicio Web de RMS previsto para ser usado por otro servicio.

<!-- -->

**punto de conexión de servicio (SCP)**  
Objeto de Active Directory que hace referencia a la dirección URL del clúster de certificación raíz de una implementación de RMS. El cliente de RMS utiliza esta información para localizar los servicios de RMS.

<!-- -->

**subinscripción**  
Parte del proceso de establecimiento de servicios en línea en un servidor de licencias, por el cual el servidor de licencias obtiene un certificado emisor de licencias de servidor del clúster de certificación raíz.

<!-- -->

**solicitud de subinscripción**  
Solicitud enviada por un servidor de licencias al clúster de certificación raíz para un certificado emisor de licencias de servidor.

<!-- -->

**servicio de subinscripción**  
Servicio Web de RMS del servidor de certificación raíz que responde a las solicitudes de certificados emisores de licencias de servidor que envían los servidores de licencias durante el establecimiento de servicios en línea.

<!-- -->

**superusuario**  
Miembro del grupo de superusuarios.

<!-- -->

**grupo de superusuarios**  
Grupo opcional de usuarios definido administrativamente para cada clúster de RMS al que concederá licencias de propietario el servidor de Windows RMS cuando abra el contenido publicado por ese servidor.

<!-- -->

**licencia de uso**  
Licencia donde se listan los permisos y las condiciones bajo las que un usuario final puede utilizar contenido protegido. También se conoce como licencia de usuario final (LUF).
