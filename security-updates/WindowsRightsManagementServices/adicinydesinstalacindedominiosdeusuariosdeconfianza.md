---
TOCTitle: Adición y desinstalación de dominios de usuarios de confianza
Title: Adición y desinstalación de dominios de usuarios de confianza
ms:assetid: '7c440b15-01c4-49f1-b43c-00f67f3388c1'
ms:contentKeyID: 18127830
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747571(v=WS.10)'
---

Adición y desinstalación de dominios de usuarios de confianza
=============================================================

De forma predeterminada, Windows RMS no procesa solicitudes de usuarios cuyos certificados de cuenta de permisos hayan sido emitidos por una instalación de Windows RMS diferente. Sin embargo, puede agregar dominios de usuario a la lista de dominios de usuarios de confianza, lo que permite a RMS procesar este tipo de solicitudes.

Para cada dominio de confianza, también puede agregar y quitar usuarios o grupos de usuarios específicos. Además, puede quitar un dominio de usuario de confianza; de todos modos, no puede quitar el clúster de certificación raíz de este bosque de Active Directory de los dominios de usuarios de confianza. Todos los servidores de RMS de una implementación, incluido el servidor de certificación raíz, confían en el clúster de certificación raíz de su propio bosque.

Puede administrar los dominios de usuarios de confianza de la siguiente manera:

-   Para admitir usuarios externos en general, agregue el servicio Microsoft® .NET Passport a la lista de dominios de confianza. Esto permite que un servidor de RMS de la compañía procese las solicitudes de licencias que incluyan un certificado de cuenta de permisos emitido por el servicio Microsoft .NET Passport.
-   Para confiar en usuarios externos de la instalación de RMS de otra organización, puede agregar la organización a la lista de dominios de usuarios de confianza. Esto permite que un servidor de RMS procese una solicitud de licencias que incluya un certificado de cuenta de permisos que haya emitido un servidor de RMS que se encuentre en la otra organización.
-   Igualmente, para procesar solicitudes de licencias de usuarios de su organización que residan en otro bosque de Active Directory, puede agregar la instalación de RMS de dicho bosque a la lista de dominios de usuarios de confianza. Esto permite que un servidor de RMS que se encuentre en el bosque actual procese una solicitud de licencias que incluya un certificado de cuenta de permisos emitido por un servidor de RMS del otro bosque.
-   Para cada dominio de usuario de confianza, puede especificar qué dominios de correo electrónico son de confianza. Para los dominios de Passport de confianza, puede especificar qué usuarios o dominios de correo electrónico no son de confianza.

Para agregar una instalación de RMS a la lista de dominios de usuarios de confianza, debe importar el certificado emisor de licencias de servidor para la instalación de RMS que desee agregar. En primer lugar, el administrador debe exportar del servidor o clúster en el que desee confiar el certificado emisor de licencias de servidor y enviarle el archivo correspondiente. A continuación, puede importar el archivo especificando su ubicación. Para guardarlo, el usuario que haya iniciado sesión debe poseer permisos para la carpeta compartida. La información de la clave privada no se transfiere cuando se configura un dominio de usuario de confianza.

Para obtener instrucciones paso a paso acerca de cómo establecer dominios de usuarios de confianza, vea “[Para agregar un dominio de usuario de confianza](https://technet.microsoft.com/ed672e58-6272-4ac0-a434-d1d938037e93)”, más adelante en este tema.
