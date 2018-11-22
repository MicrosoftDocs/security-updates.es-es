---
TOCTitle: Certificación de cuenta de RMS
Title: Certificación de cuenta de RMS
ms:assetid: 'c9a385c5-6dbb-47f5-a80f-69718e6f9deb'
ms:contentKeyID: 18127952
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747750(v=WS.10)'
---

Certificación de cuenta de RMS
==============================

El proceso de certificación de cuentas crea un certificado de cuenta de permisos, que asocia una cuenta de usuario con un equipo específico y permite al usuario utilizar contenido protegido con RMS de dicho equipo. La primera vez que un usuario publica contenido protegido con RMS o intenta utilizar contenido protegido con RMS de un equipo cliente, la aplicación compatible con RMS envía una solicitud de un certificado de cuenta de permisos al servicio de certificación de cuentas de RMS.

El servicio de certificación puede autenticar al usuario mediante autenticación de Windows o mediante un certificado x.509 que se almacena en un dispositivo de cifrado de hardware, como una tarjeta inteligente. Una vez autenticado el usuario, el servidor de RMS crea un certificado de cuenta de permisos que se basa en sus credenciales autenticadas. Cifra la clave privada del usuario con la clave pública del certificado de equipo de RMS del equipo cliente e incluye la clave cifrada en el certificado de cuenta de permisos. A continuación emite el certificado de cuenta de permisos a la aplicación solicitante, que almacena el certificado de cuenta de permisos en el equipo o dispositivo, para que esté disponible para posteriores solicitudes de licencias de publicación o de uso. El certificado de cuenta de permisos se almacena también en la base de datos de configuración.

La certificación de cuentas se realiza con posterioridad al proceso de activación del equipo, ya que se necesita el certificado de equipo de RMS del equipo cliente para solicitar el certificado de cuenta de permisos.

Los usuarios deben adquirir un certificado de cuenta de permisos para cada uno de los equipos que usen. Si un usuario trabaja en más de un equipo, sólo se emitirá un único certificado de cuenta de permisos para cada equipo, pero todos los equipos contendrán el mismo par de claves para dicho usuario.

Cuando una aplicación compatible con RMS solicita una licencia de uso, incluye el certificado de cuenta de permisos en la solicitud. El servicio de licencias utiliza la clave pública del certificado de cuenta de permisos para cifrar la clave de contenido; esto garantiza que sólo el usuario autenticado utilice la licencia de uso.

El proceso de certificación de cuentas implica los siguientes pasos:

1.  La primera vez que un usuario publica contenido protegido con RMS o intenta utilizar contenido protegido con RMS en un equipo determinado, la aplicación compatible con RMS envía una solicitud de un certificado de cuenta de permisos al servicio de certificación de cuentas que se está ejecutando en el servidor de certificación raíz.
2.  El servicio de certificación de cuentas autentica al usuario mediante el proceso de autenticación de Windows.
3.  El servicio de certificación de cuentas crea un certificado de cuenta de permisos para el usuario que se basa en sus credenciales autenticadas. Cifra la clave privada del usuario con la clave pública del certificado de equipo de RMS e incluye la clave cifrada en el certificado. A continuación emite el certificado de cuenta de permisos a la aplicación solicitante.
4.  La aplicación almacena el certificado de cuenta de permisos en el equipo o dispositivo, para que esté disponible para posteriores solicitudes de licencias de publicación o de uso.

El servicio de certificación de cuentas que utiliza el cliente para solicitar el RAC depende del tipo de equipo en el que esté instalado el cliente de RMS. Los equipos de escritorio estándares se conectan al servicio de certificación de cuentas (certification.asmx). Los servicios de servidor que se han habilitado para utilizarse con RMS SP1 reciben certificados RAC del servicio de certificación de servidores (ServeCertfication.asmx). Los dispositivos móviles que se han habilitado para utilizarse con RMS SP1 reciben certificados RAC del servicio de certificación de dispositivos móviles (MobileDeviceCertfication.asmx). En una instalación predeterminada de RMS SP1 únicamente está habilitado el servicio de certificación de cuentas.

Para obtener más información acerca del uso de RMS SP1 con dispositivos móviles y servicios de servidor, vea "Habilitación de la compatibilidad del servidor de RMS con dispositivos móviles y servicios de servidor" en el apartado Operación de un servidor de RMS de esta recopilación de documentación.
