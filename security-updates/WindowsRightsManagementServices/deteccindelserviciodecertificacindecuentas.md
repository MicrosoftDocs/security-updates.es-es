---
TOCTitle: Detección del servicio de certificación de cuentas
Title: Detección del servicio de certificación de cuentas
ms:assetid: '293a2f91-4712-45ec-8b74-7533f4144cbd'
ms:contentKeyID: 18127700
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720224(v=WS.10)'
---

Detección del servicio de certificación de cuentas
==================================================

El servicio de certificación de cuentas de RMS otorga certificados de cuenta de permisos a los usuarios. Cada certificado de cuenta de permisos (RAC) sólo es válido para un equipo o dispositivo específico y requiere que el usuario que solicita el certificado tenga un certificado de equipo válido.

Sólo el servidor o clúster de certificación raíz ejecuta el servicio de certificación de cuentas. Para cursar una solicitud de certificación de cuenta, el cliente debe recuperar primero de Active Directory la dirección URL del directorio virtual Certification del servidor de certificación raíz, en el que se encuentra el servicio de certificación de cuentas. A continuación, adjunta la ruta al servicio de certificación de cuentas.

Por ejemplo, la dirección URL de certificación del servidor de certificación raíz se almacena en Active Directory con el formato siguiente:

http://*nombre\_servidor*/\_wmcs/Certification

Cuando un cliente solicita un certificado de cuenta de permisos, adjunta el nombre del archivo de servicio de certificación de cuentas a la dirección URL del modo siguiente:

http://*nombre\_servidor*/\_wmcs/Certification/Certification.asmx

> [!NOTE]
> Si se ha habilitado SSL en el servidor de RMS, estas direcciones URL utilizarán el protocolo de conexión https://. 
