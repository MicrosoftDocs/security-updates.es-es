---
TOCTitle: Detección del servicio de activación
Title: Detección del servicio de activación
ms:assetid: 'e178d81b-b35c-4958-87ef-e077e2204b32'
ms:contentKeyID: 18127985
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747697(v=WS.10)'
---

Detección del servicio de activación
====================================

El servicio de activación emite cajas de seguridad y certificados de equipo de RMS para clientes de RMS versión 1.0. Se mantiene por cuestiones de compatibilidad con la versión 1.0 de RMS. El clúster de certificación raíz de RMS proporciona el servicio proxy de activación, que es el encargado de reenviar las solicitudes de activación de equipo de RMS al servicio de activación desde los equipos cliente que se ejecutan en la red corporativa.

Para cursar una solicitud de activación de equipo de RMS, un cliente de RMS versión 1.0 recupera primero de Active Directory la dirección URL del directorio virtual Certification del servidor de certificación raíz, donde se encuentra el servicio proxy de activación. A continuación, adjunta la ruta al servicio proxy de activación.

Por ejemplo, la dirección URL del directorio virtual Certification del servidor de certificación raíz está almacenada en Active Directory con el formato siguiente:

http://*nombre\_servidor*/\_wmcs/Certification

Cuando un cliente solicita la activación de equipo de RMS, adjunta el nombre del archivo del servicio proxy de activación a la dirección URL del modo siguiente:

http://*nombre\_servidor*/\_wmcs/Certification/Activation.asmx

Los clientes que se ejecutan fuera de la red corporativa usan UDDI con el fin de localizar el servicio de activación. Para obtener más información, vea "[Publicación de servicios alojados por Microsoft](https://technet.microsoft.com/7ee8cb4d-1b46-48be-8a4c-5ff6a458231a)", anteriormente en este tema.

> [!NOTE]
> Si se ha habilitado SSL en el servidor de RMS, estas direcciones URL utilizarán el protocolo de conexión https://. 
