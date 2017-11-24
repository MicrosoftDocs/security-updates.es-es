---
TOCTitle: Certificados de cuenta de permisos
Title: Certificados de cuenta de permisos
ms:assetid: '2ff315cc-211d-4e6e-85e8-56867c2abd94'
ms:contentKeyID: 18127702
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720230(v=WS.10)'
---

Certificados de cuenta de permisos
==================================

Las organizaciones deben identificar a los usuarios que son entidades de confianza en su sistema RMS. Para ello, RMS emite certificados de cuenta de permisos que asocian cuentas de usuarios con equipos específicos. El certificado de cuenta de permisos del usuario debe incluirse con la solicitud para certificados emisores de licencias de cliente y licencias de uso. Los certificados emisores de licencias de cliente permiten a los autores publicar contenido protegido con RMS, como archivos y correo electrónico, mientras están sin conexión. Las licencias de uso permiten a los usuarios utilizar contenido protegido con RMS. Todos los certificados de cuenta de permisos contienen la clave pública del usuario, que se usa para cifrar los datos destinados a ese usuario.

Existen dos tipos de certificados de cuenta de permisos: estándar y temporal. Se puede especificar el período de validez para ambos tipos. Los certificados estándar tienen una duración que se especifica en días (365 días es el valor predeterminado), mientras que los certificados de cuenta temporales tienen una duración que se especifica en minutos (15 minutos es el valor predeterminado). Los certificados de cuenta temporales permiten a los usuarios utilizar contenido temporalmente, por ejemplo, en un quiosco, cuando no pueden obtener acceso al equipo que usan normalmente. Esto evita que otro usuario utilice el contenido desde este equipo más tarde.
