---
TOCTitle: Proceso de retiro
Title: Proceso de retiro
ms:assetid: '57bd9949-9433-437b-93ed-ffb2dff9992e'
ms:contentKeyID: 18127756
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720276(v=WS.10)'
---

Proceso de retiro
=================

Mediante los Servicios de Internet Information Server (IIS), RMS expone varios servicios que ofrece. Por ejemplo, el servicio de certificación inscribe a los usuarios y sus equipos, y el servicio de licencias publica contenido y proporciona acceso a información protegida con RMS. Para iniciar el proceso de retiro es necesario habilitar un servicio adicional en el servidor de RMS, llamado servicio de retiro. Cuando el servicio de retiro está habilitado, el resto de los servicios de RMS proporcionados por el servidor están deshabilitados.

Una vez que el servidor de RMS ha sido habilitado para el retiro, las aplicaciones pueden obtener una clave de contenido del servicio de retiro, que permite a la aplicación descifrar permanentemente el contenido protegido con RMS.

Cuando el servidor de RMS funciona en modo de retiro, cualquier usuario, tanto si dispone como si no de permisos sobre el contenido original protegido con RMS, puede obtener una clave de contenido y recibir todos los permisos sobre el contenido.

Una vez descifrado el contenido, el usuario debe guardar el contenido sin protección de RMS. Recuerde que para utilizar el servicio de retiro, el usuario debe estar inscrito en la infraestructura de RMS. Un usuario sin un cliente de RMS activado no puede utilizar el servicio de retiro para obtener acceso a contenido protegido con RMS.