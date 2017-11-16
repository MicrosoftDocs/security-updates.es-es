---
TOCTitle: Detección del servicio de publicación
Title: Detección del servicio de publicación
ms:assetid: '5d500841-a202-4865-b5d2-d0775d4e1bbc'
ms:contentKeyID: 18127833
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747580(v=WS.10)'
---

Detección del servicio de publicación
=====================================

El servicio de publicación de RMS emite licencias de publicación que se usan para proteger contenido. También emite certificados emisores de licencias de cliente, que permiten a los usuarios publicar contenido cuando no están conectados a la red corporativa.

El servicio de publicación está disponible en el clúster de certificación raíz o en los servidores de licencias. Las aplicaciones compatibles con RMS solicitan este servicio cuando un autor publica contenido protegido con RMS. Para cursar una solicitud de servicio de publicación, la aplicación debe primero recuperar de Active Directory la dirección URL del directorio virtual Licensing del servidor, donde se encuentra el servicio de publicación. A continuación, adjuntan la ruta al servicio de publicación.

Por ejemplo, la dirección URL del directorio virtual Licensing de un servidor se almacena en Active Directory con el formato siguiente:

http://*nombre\_servidor*/\_wmcs/Licensing

Cuando un servidor solicita una licencia de publicación, adjunta el nombre del archivo del servicio de publicación a la dirección URL, del modo siguiente:

http://*nombre\_servidor*/\_wmcs/Licensing/Publish.asmx

Si RMS detecta que el certificado de cuenta de permisos se basa en la autenticación de usuario de Windows, el bosque de Active Directory determinará la ubicación del servicio de publicación. Esto se aplica tanto a los usuarios internos como a los externos que se conecten a la red de la empresa a través de una red privada virtual (VPN, Virtual Private Network).

Si RMS detecta que el certificado de cuenta de permisos se basa en Microsoft® .NET Passport, la ubicación del servicio de publicación será la cuenta de .NET Passport que se especifique en el contenido protegido con RMS.

> [!NOTE]
> Si se ha habilitado SSL en el servidor de RMS, estas direcciones URL utilizarán el protocolo de conexión https://. 
