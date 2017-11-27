---
TOCTitle: Novedades de esta versión
Title: Novedades de esta versión
ms:assetid: 'c68ec6fd-0ff5-467e-85a8-a53b9f089de3'
ms:contentKeyID: 18127941
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747748(v=WS.10)'
---

Novedades de esta versión
=========================

Rights Management Services (RMS) con Service Pack 1 (SP1) es compatible con las siguientes características:

-   **Inscripción en el servidor de RMS sin conexión a Internet en el servidor**. En la versión anterior, el servidor de RMS necesitaba poder conectarse a Internet para inscribirse en el servicio de inscripción de Microsoft y recibir el certificado emisor de licencias de servidor raíz. Con RMS SP1 se sigue solicitando el certificado emisor de licencias de servidor raíz del servicio de inscripción de Microsoft, pero se puede solicitar utilizando otro equipo con conexión a Internet e importarlo al servidor de RMS después del establecimiento en línea.
-   **Los clientes se activan automáticamente**. En la versión anterior, los certificados de equipo y las cajas de seguridad para los equipos cliente debían descargarse del servicio de activación de Microsoft. Con RMS SP1, no es necesario volver a conectarse al servicio de activación de Microsoft.
-   **Compatibilidad con más tipos de clientes**. En esta versión, el servidor de RMS puede utilizarse para permitir clientes en dispositivos móviles y servicios de servidor. Como administrador del servidor de RMS, podrá controlar si desea o no que el servidor proporcione certificación a estos clientes cuando intentan utilizar sus servicios.
-   **Compatibilidad con plantillas multilingües**. En la versión anterior, las plantillas se basaban en la configuración de idioma de Internet Explorer. En esta versión puede especificar en la página Web de administración de RMS qué idioma desea utilizar para crear una plantilla.
-   **Compatibilidad con autenticación del cliente mediante tarjetas inteligentes**. En esta versión, el cliente de RMS puede utilizar credenciales almacenadas en certificados x.509 de tarjetas inteligentes para autenticar en el servidor de RMS para obtener certificados de cuenta de permisos (RAC) y utilizar licencias.
