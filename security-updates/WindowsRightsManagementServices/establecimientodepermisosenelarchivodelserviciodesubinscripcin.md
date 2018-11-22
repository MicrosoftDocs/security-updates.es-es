---
TOCTitle: Establecimiento de permisos en el archivo del servicio de subinscripción
Title: Establecimiento de permisos en el archivo del servicio de subinscripción
ms:assetid: '737bb69b-fe26-4057-9569-e632f7bbf295'
ms:contentKeyID: 18127815
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747627(v=WS.10)'
---

Establecimiento de permisos en el archivo del servicio de subinscripción
========================================================================

El servicio de subinscripción se ejecuta en el servidor de certificación raíz e inscribe un servidor de licencias durante el establecimiento de los servicios en línea. De forma predeterminada, el servicio de subinscripción sólo permite el acceso a la cuenta del sistema local que se encuentre en el servidor de certificación raíz. Para establecer los servicios en línea en un servidor de licencias, debe iniciar sesión en el servidor de licencias con esta cuenta. Como alternativa, un administrador local del servidor de certificación raíz debe cambiar la lista DACL en el archivo del servicio de subinscripción, SubEnrollService.asmx, para otorgar acceso a la cuenta de usuario que vaya a establecer los servicios en línea en el servidor de licencias. SubEnrollService.asmx se encuentra en el directorio virtual Certification del servidor de certificación raíz.
