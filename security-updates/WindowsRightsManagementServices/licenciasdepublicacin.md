---
TOCTitle: Licencias de publicación
Title: Licencias de publicación
ms:assetid: '187228fc-370b-4e23-a53a-21bb296b84a1'
ms:contentKeyID: 18127743
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720211(v=WS.10)'
---

Licencias de publicación
========================

Los usuarios de aplicaciones compatibles con RMS pueden asignar permisos de uso específicos a información y archivos digitales que sean coherentes con las directivas corporativas existentes. Estos permisos de uso se almacenan en licencias de publicación donde se especifican los usuarios que pueden ver el contenido, así como el modo en que pueden editarlo y distribuirlo.

Una licencia de publicación puede emitirla una aplicación cliente compatible con RMS, el servidor de certificación raíz o un servidor de licencias RMS. Cuando una aplicación cliente compatible con RMS emite una licencia de publicación, el servidor de RMS otorga a la aplicación un certificado emisor de licencias de cliente. Esto se conoce como publicación sin conexión. Se trata de un método habitual de publicación, ya que permite a los usuarios de aplicaciones compatibles con RMS crear contenido protegido sin necesidad de una conexión al servidor de RMS. Si la aplicación cliente compatible con RMS no utiliza un certificado emisor de licencias de cliente, el usuario deberá poder conectarse a un servidor de RMS para recibir una licencia de publicación para el contenido protegido.

Una licencia de publicación contiene la clave simétrica de contenido para descifrar el contenido que está cifrado con la clave pública del servidor de RMS. De este modo, se garantiza que sólo el servidor pueda descifrar el contenido y emitir licencias de uso.

Las licencias de publicación están firmadas con la clave privada del servidor que las emite o con la clave privada del certificado emisor de licencias de cliente.
