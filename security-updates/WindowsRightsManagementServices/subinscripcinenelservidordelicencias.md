---
TOCTitle: Subinscripción en el servidor de licencias
Title: Subinscripción en el servidor de licencias
ms:assetid: '7bc63397-9186-464c-8824-867038adce9b'
ms:contentKeyID: 18127829
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747640(v=WS.10)'
---

Subinscripción en el servidor de licencias
==========================================

Los servidores de licencias se inscriben automáticamente durante el establecimiento de servicios en línea, en un proceso denominado subinscripción. No obstante, cuando se agrega un nuevo servidor a un clúster de servidores de licencias, éste no se subinscribe explícitamente, porque usa el certificado emisor de licencias de servidor y la base de datos de configuración del clúster.

En lugar de enviar la solicitud de subinscripción al servicio de inscripción de Microsoft, el servidor de licencias la envía al servidor de certificación raíz. La solicitud de subinscripción de un servidor de licencias es idéntica a una solicitud de inscripción del servidor de certificación raíz.

Cuando el servidor de certificación raíz recibe una solicitud de subinscripción, comprueba que esté formulada correctamente y, a continuación, devuelve una cadena de certificado que contiene la cadena del certificado emisor de licencias del servidor de certificación raíz y un certificado firmado por el servidor de certificación raíz. El certificado contiene la clave pública del servidor firmada con la clave privada del servidor de certificación raíz. El certificado otorga al servidor de licencias permiso para emitir licencias de uso y de publicación.

El certificado emisor de licencias de servidor es válido durante un año. El período de validez comienza a contar en el momento en que se emite el certificado. Al final del período de validez, el certificado puede renovarse. Los certificados y las licencias emitidos por el servidor son válidos por siete años. El período de validez comienza a contar en el momento en que se emite el certificado o la licencia.

De forma predeterminada, el servicio que se requiere para procesar una solicitud de subinscripción en el servidor de certificación raíz, SubEnrollService.asmx, está configurado para denegar todos los intentos de acceso. Para poder procesar las solicitudes, habrá que cambiar las listas DACL de modo que permitan el acceso al administrador de RMS.
