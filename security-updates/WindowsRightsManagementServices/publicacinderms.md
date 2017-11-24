---
TOCTitle: Publicación de RMS
Title: Publicación de RMS
ms:assetid: 'a82f4172-546d-4fab-9f96-3f8b263a5b69'
ms:contentKeyID: 18127904
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747720(v=WS.10)'
---

Publicación de RMS
==================

El proceso de publicación permite a usuarios determinados utilizar un fragmento específico de contenido de una forma determinada. El servicio de publicación de RMS enlaza el contenido protegido con RMS con una licencia de publicación. Las licencias de publicación definen las directivas según las cuales se pueden emitir licencias de uso. Las licencias de uso, que emite el servicio de licencias de RMS, definen los permisos que un usuario determinado tiene para utilizar parte de contenido protegido con RMS.

El autor del contenido protegido con RMS especifica los permisos que se aplicarán a dicho contenido mediante una interfaz de usuario que suministra la aplicación compatible con RMS. Normalmente el autor selecciona una plantilla de directiva de permisos y, a continuación, especifica los destinatarios del contenido y sus permisos. Los administradores de RMS crean las plantillas de directiva de permisos y están disponibles en un servidor de RMS.

En la mayoría de los casos, el mismo servidor de RMS que emitió las licencias de publicación emite las licencias de uso. Cuando esto no es posible, se puede crear un dominio de publicación de confianza para permitir que un servidor emita una licencia de uso con una licencia de publicación de otro servidor. También se puede crear un dominio de usuario de confianza para permitir el proceso de las solicitudes de licencias de uso de usuarios que estén en otro bosque de Active Directory, ya sea de la misma empresa o de otra distinta.

Se tratan los siguientes temas:

-   [Plantillas de directiva de permisos](https://technet.microsoft.com/eee931c8-7c98-48e9-9e2c-d0b7bd4f2b96)
-   [Distribución del contenido protegido con RMS](https://technet.microsoft.com/98612cfb-4fd6-47f9-8b9f-025a93834cd9)
-   [Uso del contenido protegido con RMS](https://technet.microsoft.com/3cf6d64b-1187-433c-bbb2-c68069bc3c30)
-   [Dominios de usuarios de confianza](https://technet.microsoft.com/a09b883f-f455-4c46-a4fd-d37b689e1d24)
-   [Dominios de publicación de confianza](https://technet.microsoft.com/bca1c33a-d3ef-42b5-adbe-6e104979a71f)