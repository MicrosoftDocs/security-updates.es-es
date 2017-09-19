---
TOCTitle: Inscripción en el servidor de certificación raíz
Title: Inscripción en el servidor de certificación raíz
ms:assetid: 'f08bc919-f090-4843-b2ce-b40d558012ce'
ms:contentKeyID: 18128029
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747734(v=WS.10)'
---

Inscripción en el servidor de certificación raíz
================================================

El primer servicio de una implementación de RMS debe inscribirse con el servicio de inscripción de Microsoft. Este servidor, que es un servidor de certificación raíz, puede inscribirse automáticamente durante el establecimiento de servicios en línea si el servidor tiene conexión a Internet o puede inscribirse manualmente si el servidor forma parte de una red cerrada. Para obtener más información sobre la inscripción manual de un servidor, vea "Para inscribir manualmente un servidor de certificación raíz" en "Operación de un servidor de RMS", en esta recopilación de documentación.

La solicitud de inscripción adopta los siguientes parámetros de entrada:

-   Una clave pública de 1024 bits. Ésta es la clave pública de RMS.
-   La versión, el nombre y la dirección URL del servidor de RMS que se va a inscribir.

El servicio de inscripción de Microsoft usa esta información sólo para crear el certificado emisor de licencias de servidor y únicamente almacena la información con fines de revocación.

El servicio de inscripción de Microsoft devuelve una cadena de certificados que contiene la cadena de certificados emisores de licencias del servidor de inscripción, junto con un certificado firmado por el servidor de inscripción. El certificado contiene la clave pública del servidor, que está firmada con la clave privada de inscripción y la versión y dirección URL del servidor inscrito. El certificado otorga al servidor de certificación raíz permiso para emitir certificados emisores de licencias de servidor a servidores de licencias, así como para emitir certificados de cuenta de permisos, certificados emisores de licencias de cliente y licencias de publicación y de uso.

El certificado emisor de licencias de servidor es válido durante un año. El período de validez comienza a contar en el momento en que se emite el certificado. Al final del período de validez, el certificado puede renovarse. Los certificados y las licencias emitidos por el servidor son válidos por siete años. El período de validez comienza a contar en el momento en que se emite el certificado o la licencia.

La información sobre la revocación del certificado se agrega al certificado emisor de licencias de servidor cuando se especifica en la solicitud de inscripción. La clave pública del servicio de inscripción de Microsoft se agrega al certificado como una clave de revocación. Además, si se especifica una clave de revocación de terceros, también se agrega al certificado como clave de revocación.
