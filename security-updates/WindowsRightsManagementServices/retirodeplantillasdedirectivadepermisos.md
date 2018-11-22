---
TOCTitle: Retiro de plantillas de directiva de permisos
Title: Retiro de plantillas de directiva de permisos
ms:assetid: '32bf98c7-edda-4507-a4b8-4c11bddd6e60'
ms:contentKeyID: 18127783
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720239(v=WS.10)'
---

Retiro de plantillas de directiva de permisos
=============================================

Para retirar una plantilla de directiva de permisos, debe eliminarla. Este procedimiento se describe en “[Para eliminar una plantilla de directiva de permisos](https://technet.microsoft.com/9c9a1496-cf55-4c65-a4c6-9fe245edce00)”, más adelante en este tema. Sin embargo, en general, no debe eliminar plantillas de directiva de permisos. Si desea retirar una plantilla de directiva de permisos, debe asegurarse de quitar sus copias de los equipos de los usuarios. Debe hacerlo porque, cuando un autor utiliza una plantilla de directiva de permisos para publicar contenido, se envía una solicitud al servidor de RMS. RMS utiliza una copia de la plantilla de directiva de permisos que está almacenada en la base de datos para responder a la solicitud. Si la plantilla de directiva de permisos no existe en la base de datos, no se acepta la solicitud.

> [!NOTE]
> Un método para administrar el retiro de una plantilla de directiva de permisos es crear una secuencia de comandos que quite la plantilla de los equipos de todos los usuarios.