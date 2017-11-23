---
TOCTitle: Licencias de uso y usuarios externos
Title: Licencias de uso y usuarios externos
ms:assetid: '02db9bda-180e-438f-863d-26252083a471'
ms:contentKeyID: 18127683
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720176(v=WS.10)'
---

Licencias de uso y usuarios externos
====================================

RMS permite a los autores compartir contenido protegido con usuarios externos autorizados a través de Internet. RMS ofrece el mismo nivel de protección para la publicación de contenido a usuarios internos y externos, ya que los permisos adjuntos al contenido deben obtener una licencia de un servidor de RMS. Esto permite a las organizaciones compartir documentos confidenciales, como contratos, y trabajar juntas en ellos a través de Internet.

Un usuario externo suele obtener acceso a RMS a través de Internet. (Si un usuario externo puede obtener acceso a la red interna directamente, por ejemplo, a través de una conexión VPN, funcionalmente es equivalente a un usuario interno.) Tanto si el usuario pertenece a la organización de publicación como si es un usuario externo, el proceso de adquisición de una licencia de uso es básicamente el mismo, descrito en "[Adquisición de licencias de uso](https://technet.microsoft.com/0b6cde34-418a-4dee-9d27-b65b93b535ac)", anteriormente en este tema. No se requiere al usuario que esté dentro de la red del autor o que tenga una cuenta de usuario en ella para solicitar una licencia de uso.

Todo lo que se precisa es lo siguiente:

-   Que el usuario tenga un certificado de cuenta de permisos válido.
-   Que el usuario tenga acceso al servidor de licencias de RMS que ha emitido la licencia de publicación, que puede encontrarse en la intranet o en una extranet.
-   Que la instalación de RMS que emitió el certificado de cuenta de usuario esté en la lista de dominios de usuario de confianza en la instalación de RMS que emite la licencia de uso.

Los siguientes tipos de usuarios externos pueden obtener licencias de uso:

-   Usuarios cuyas cuentas formen parte de un bosque distinto de Active Directory que también tenga una instalación de RMS. La instalación de RMS del otro bosque debe estar definida como dominio de usuario de confianza en la primera instalación.
-   Usuarios de otra organización que también ejecuten una instalación de RMS que se haya agregado a la lista de dominios de usuarios de confianza de esta instalación.
-   Usuarios que tengan certificados de cuenta de permisos basados en .NET Passport cuando el servicio de certificación de RMS de Microsoft esté en la lista de dominios de usuarios de confianza de esta instalación.

Se puede agregar otra organización u otra instalación de RMS de la organización a la lista de dominios de usuarios de confianza. Después de agregar un dominio, se puede definir qué dominios de correo electrónico de dicho dominio son de confianza, así como determinar si se debe confiar en los identificadores de seguridad (SID) de ese dominio.

Otra organización ajena o una instalación de RMS que se encuentre en su organización pueden agregar la instalación de RMS a su lista de dominios de usuarios de confianza de forma que los servidores de RMS de dicha organización o instalación puedan procesar solicitudes de licencias de uso de los usuarios que pertenecen a la misma instalación que usted.

Para obtener más información acerca de cómo crear dominios de usuarios de confianza entre RMS y otras organizaciones, vea "[Dominios de usuarios de confianza](https://technet.microsoft.com/a09b883f-f455-4c46-a4fd-d37b689e1d24)", más adelante en este tema, y "Adición y desinstalación de dominios de publicación de confianza" en "Operación de un servidor de RMS", en esta recopilación de documentación.
