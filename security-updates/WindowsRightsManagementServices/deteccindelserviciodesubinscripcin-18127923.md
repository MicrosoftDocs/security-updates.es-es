---
TOCTitle: Detección del servicio de subinscripción
Title: Detección del servicio de subinscripción
ms:assetid: 'b159953a-af38-4a9e-8c87-1aff5fb4e366'
ms:contentKeyID: 18127923
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747641(v=WS.10)'
---

Detección del servicio de subinscripción
========================================

Un servidor de licencias independiente, o el primer servidor de licencias de un clúster, debe enviar una solicitud de subinscripción al servidor de certificación raíz de RMS para obtener un certificado emisor de licencias de servidor. Para ello, el servidor de licencias obtiene la dirección URL del servicio de subinscripción de certificación raíz del modo siguiente.

Durante el establecimiento de servicios en línea de un servidor de licencias, el programa de instalación de RMS envía una consulta a Active Directory y, a continuación, detecta el punto de conexión de servicio del clúster de certificación raíz. RMS utiliza la dirección URL almacenada en este punto de conexión de servicio para localizar el clúster de certificación raíz y, a continuación, solicita un certificado emisor de licencias de servidor del servicio de subinscripción del servidor de certificación raíz.

Para cursar una solicitud de servicio de subinscripción, el servidor de licencias debe recuperar primero de Active Directory la dirección URL del directorio virtual Certification del servidor de certificación raíz, en el que se encuentra el servicio de subinscripción. A continuación, adjunta la ruta al servicio de subinscripción.

Por ejemplo, la dirección URL del directorio virtual Certification del servidor de certificación raíz está almacenada en Active Directory con el formato siguiente:

http://*nombre\_servidor*/\_wmcs/Certification

Cuando un servidor de licencias solicita el servicio de subinscripción, adjunta el nombre del archivo del servicio a la dirección URL, del modo siguiente:

http://nombre\_servidor/\_wmcs/Certification/SubEnrollService.asmx

| ![](images/Cc747641.note(WS.10).gif)Nota                                              |
|--------------------------------------------------------------------------------------------------------------------|
| Si se ha habilitado SSL en el servidor de RMS, estas direcciones URL utilizarán el protocolo de conexión https://. |
