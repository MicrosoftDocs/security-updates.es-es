---
TOCTitle: Uso del contenido protegido con RMS
Title: Uso del contenido protegido con RMS
ms:assetid: '3cf6d64b-1187-433c-bbb2-c68069bc3c30'
ms:contentKeyID: 18127786
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720251(v=WS.10)'
---

Uso del contenido protegido con RMS
===================================

Cuando los usuarios utilizan contenido protegido, se realizan dos procesos que pasan inadvertidos a los usuarios. En primer lugar, cuando el usuario abre el documento, la aplicación compatible con RMS solicita una licencia de uso. En segundo lugar, la aplicación examina la licencia de uso para determinar si requiere una lista de revocaciones y comprueba si se ha revocado algún certificado que esté en su cadena de confianza o en la del certificado de cuenta de RMS. Una vez realizados ambos procesos, y si todos los permisos y revocaciones lo permiten, la aplicación compatible con RMS procesa el contenido protegido con RMS.

Si se requiere una lista de revocaciones, la aplicación busca una copia local de dicha lista que no haya caducado. Si fuera necesario, recupera una copia actualizada de la lista de revocaciones. A continuación, la aplicación aplica cualquier condición de revocación relevante en el contexto actual.

Si no existe ninguna condición de revocación que bloquee el acceso al contenido, la aplicación lo procesa y el usuario puede ejercitar los permisos que le hayan sido conferidos.

Es posible configurar RMS para que usuarios externos autorizados puedan procesar solicitudes de licencias de uso. Esto permite a los usuarios compartir contenido protegido a través de Internet.

En esta sección, se tratan los siguientes temas:

-   [Adquisición de licencias de uso](https://technet.microsoft.com/0b6cde34-418a-4dee-9d27-b65b93b535ac)
-   [Licencias de uso y usuarios externos](https://technet.microsoft.com/02db9bda-180e-438f-863d-26252083a471)
