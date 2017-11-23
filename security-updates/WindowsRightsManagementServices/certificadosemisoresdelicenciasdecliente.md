---
TOCTitle: Certificados emisores de licencias de cliente
Title: Certificados emisores de licencias de cliente
ms:assetid: 'bfb36387-3e15-4cde-8b8f-482219569a64'
ms:contentKeyID: 18127954
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747744(v=WS.10)'
---

Certificados emisores de licencias de cliente
=============================================

Un certificado emisor de licencias de cliente otorga a un autor el permiso para publicar contenido protegido con RMS sin estar conectado a la red corporativa.

Para obtener un certificado emisor de licencias de cliente, el autor envía una solicitud de inscripción de cliente al servidor de certificación raíz o al servidor de licencias desde un equipo cliente. A continuación, el servidor devuelve el certificado emisor de licencias de cliente a ese equipo.

Los certificados emisores de licencias de cliente contienen la clave pública del emisor de licencias de cliente, junto con la clave privada de dicho emisor de licencias de cliente, cifrada con la clave pública del autor que solicitó el certificado. Además, contienen la clave pública del servidor que emitió el certificado, firmada con la clave privada de este mismo servidor. La clave privada del emisor de licencias de cliente se usa para firmar las licencias de publicación que crea el autor.
