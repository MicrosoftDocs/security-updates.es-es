---
TOCTitle: Detección del servicio de emisión de licencias
Title: Detección del servicio de emisión de licencias
ms:assetid: '4eabbb76-b359-443a-b737-098c5659e9c6'
ms:contentKeyID: 18127745
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720269(v=WS.10)'
---

Detección del servicio de emisión de licencias
==============================================

El servicio de emisión de licencias de RMS emite licencias de uso, que permiten a los usuarios autenticados utilizar contenido protegido.

Este servicio se ejecuta en los servidores o clústeres de certificación raíz y de licencias. Para cursar una solicitud de licencia de uso, el cliente debe primero recuperar de Active Directory la dirección URL del directorio virtual Licensing del clúster de certificación raíz, en el que se encuentra el servicio de emisión de licencias. A continuación, adjunta la ruta al servicio de emisión de licencias.

Por ejemplo, la dirección URL del directorio Licensing del clúster de certificación raíz está almacenada en Active Directory con el formato siguiente:

http://*nombre\_servidor*/\_wmcs/Licensing

Cuando un servidor solicita una licencia de uso, adjunta el nombre del archivo del servicio de emisión de licencias a la dirección URL, del modo siguiente:

http://*nombre\_servidor*/\_wmcs/Licensing/License.asmx

El servicio se encuentra ubicado en el servidor de RMS o en la cuenta .NET Passport que emitió la licencia de publicación; la dirección URL se incluye en la licencia de publicación.

| ![](images/Cc720269.note(WS.10).gif)Nota                                              |
|--------------------------------------------------------------------------------------------------------------------|
| Si se ha habilitado SSL en el servidor de RMS, estas direcciones URL utilizarán el protocolo de conexión https://. |
