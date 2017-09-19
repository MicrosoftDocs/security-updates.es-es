---
TOCTitle: Publicación sin conexión
Title: Publicación sin conexión
ms:assetid: 'f6384ed2-f917-442e-aa63-c1394a1c4d06'
ms:contentKeyID: 18128025
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747741(v=WS.10)'
---

Publicación sin conexión
========================

La publicación sin conexión es distinta de la publicación en línea por el modo en que la aplicación compatible con RMS adquiere la licencia de publicación.

Antes de que un autor publique contenido sin conexión, debe adquirir un certificado emisor de licencias de cliente mientras tiene acceso al servidor de certificación raíz a través de la red.

El proceso de publicación sin conexión implica los siguientes pasos:

1.  El autor crea el documento con la aplicación compatible con RMS y, a continuación, especifica los permisos y las condiciones para el contenido.
2.  Cuando el autor guarda el archivo, el certificado emisor de licencias de cliente permite al equipo o dispositivo local emitir y firmar un licencia de publicación para el archivo.
    La licencia de publicación contiene dos copias de la clave del contenido: una que se cifra con la clave pública del certificado emisor de licencias de cliente, y otra que se cifra con la clave pública del servidor que emitió el certificado emisor de licencias de cliente. También contiene la dirección URL del servidor. Las dos claves públicas y la dirección URL provienen del certificado emisor de licencias de cliente.
3.  El equipo utiliza el certificado emisor de licencias de cliente para crear una licencia de propietario, que es una licencia de uso especial que otorga al autor el permiso para utilizar el contenido protegido con RMS mientras se encuentra sin conexión. El certificado emisor de licencias de cliente usa su clave privada para descifrar la clave de contenido simétrica de la licencia de publicación y, a continuación, vuelve a cifrarla en la licencia de propietario.
4.  La aplicación cifra el archivo con la clave de contenido y enlaza la licencia de publicación con el archivo. Sólo el servidor de RMS que emitió la licencia de publicación, o un servidor que sea integrante de un dominio de publicación de confianza, puede emitir licencias para descifrar este archivo.
