---
TOCTitle: Jerarquía de confianza de RMS
Title: Jerarquía de confianza de RMS
ms:assetid: '2d44182f-a653-4383-aba1-dade53f7cf9a'
ms:contentKeyID: 18127767
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720232(v=WS.10)'
---

Jerarquía de confianza de RMS
=============================

Un sistema RMS incluye los componentes siguientes: servicio de inscripción de Microsoft, servidores de RMS, equipos cliente y usuarios del sistema. Para cada uno de estos componentes, se emite un certificado que establece su identidad en el sistema. Una jerarquía de confianza define las relaciones de confianza entre esos certificados y, por tanto, entre las entidades que los poseen. Asimismo, define la relación de confianza entre las entidades de confianza y las licencias que éstas emiten a su vez a otras entidades de confianza.

La jerarquía de confianza conecta certificados y licencias en una cadena de confianza que RMS siempre puede seguir desde un certificado o licencia en particular hasta un par de claves de confianza. La cadena de confianza incluye el certificado actual, el certificado de la entidad que lo emitió, el certificado de la entidad que emitió el certificado de esta entidad y así sucesivamente, siguiendo la cadena hasta la raíz de confianza.

Para RMS, la raíz de confianza, o "ancla de confianza", es un par de claves de Microsoft. Esta raíz de confianza común permite a una organización crear un ecosistema de confianza que englobe a las entidades de confianza, como usuarios y socios, tanto de dentro como de fuera de la organización.

En el diagrama siguiente, se muestra la jerarquía de confianza de una organización. La cadena de confianza va hasta los servicios de Microsoft que emitieron los certificados base.

![](images/Cc720232.6c169175-94fb-4ec0-93bc-12748aae3ac4(WS.10).gif)
1.  Para cada equipo cliente se emite una caja de seguridad única que contiene la clave pública raíz de Microsoft.
2.  Cuando recibe una solicitud de licencia, RMS valida las entidades principales siguiendo la ruta de la jerarquía de confianza hasta la raíz de confianza.
3.  RMS comprueba la autenticidad de la entidad de confianza mencionada en la licencia.
4.  RMS comprueba que el certificado de la entidad de confianza fue emitido por un servidor que se encuentra en la jerarquía de confianza.

En cada nivel de la cadena de certificados, RMS valida la licencia o el certificado y, a continuación, comprueba que conecta con una raíz de confianza conocida mediante una cadena de confianza. RMS comprueba todas las licencias o los certificados que se encuentran en la cadena para comprobar que se cumplen las condiciones siguientes:

-   Su código XrML es válido.
-   La firma del emisor es válida.
-   La semántica de la licencia es apropiada para el uso pretendido.
-   Se cumplen las condiciones (como fechas de validez).
-   La licencia no se ha revocado.
-   La clave que ha firmado la licencia y la clave del emisor del certificado coinciden.
