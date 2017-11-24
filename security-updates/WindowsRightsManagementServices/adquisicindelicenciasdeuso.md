---
TOCTitle: Adquisición de licencias de uso
Title: Adquisición de licencias de uso
ms:assetid: '0b6cde34-418a-4dee-9d27-b65b93b535ac'
ms:contentKeyID: 18127725
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720194(v=WS.10)'
---

Adquisición de licencias de uso
===============================

Para utilizar contenido protegido con RMS, un usuario debe adquirir una licencia de uso del servicio de emisión licencias de RMS. En la figura siguiente, se muestra el proceso de solicitud y recepción de licencias de uso.

![](images/Cc720194.37b8d28c-9749-4e81-bc6a-22692fefb8b6(WS.10).gif)

El proceso de adquisición de una licencia de uso incluye los siguientes pasos:

1.  El usuario recibe un archivo protegido a través de un canal de distribución normal y, a continuación, lo abre con una aplicación compatible con RMS. Si el usuario no tiene un certificado de cuenta de permisos en el equipo o dispositivo actual, deberá adquirir uno.
2.  La aplicación compatible con RMS envía una solicitud de licencia de uso al servidor que emitió la licencia de publicación para el contenido protegido. La solicitud incluye el certificado de cuenta de permisos del usuario (que contiene la clave pública del usuario) y la licencia de publicación (que contiene la clave simétrica del contenido).
    Las licencias de publicación emitidas por un certificado emisor de licencias de cliente incluyen la dirección URL del servidor que emitió el certificado. En ese ejemplo, la solicitud de una licencia de uso se dirige al servidor que emitió el certificado emisor de licencias de cliente, y no al equipo que emitió la licencia de publicación.
3.  El servidor de licencias comprueba que el usuario esté autorizado y que se le menciona en la licencia de publicación y, a continuación, crea una licencia de uso. El servidor valida el certificado de cuenta del usuario y determina qué permisos se le han otorgado al usuario, ya sea directamente o como integrante de un grupo al que se le han concedido permisos.
    El servidor descifra la clave de contenido simétrica mediante la clave privada del servidor, la vuelve a cifrar usando la clave pública del destinatario y la agrega a la licencia de uso. Este paso garantiza que sólo el usuario en cuestión pueda descifrar la clave del contenido, y por tanto, el contenido protegido.
    El servidor agrega cualquier condición relevante a la licencia de uso, como la exclusión de una versión de Windows o de una aplicación. El cliente obliga a cumplir estas condiciones en el momento en que la licencia de uso se enlaza al contenido protegido con RMS.
4.  Cuando la validación ha finalizado, el servidor de licencias devuelve la licencia de uso al equipo cliente del usuario.
