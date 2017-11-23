---
TOCTitle: Modelo de seguridad de RMS
Title: Modelo de seguridad de RMS
ms:assetid: '665db831-366d-4dca-9bb3-cc2912481fe1'
ms:contentKeyID: 18127853
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747598(v=WS.10)'
---

Modelo de seguridad de RMS
==========================

Durante su funcionamiento, RMS obtiene acceso a varios recursos, entre los que se encuentran el servidor de base de datos, Active Directory, la cola de mensajes y el disco duro local. Además, el programa de instalación de RMS crea y expone ciertos recursos que son necesarios para su funcionamiento, como entradas SOAP, páginas Web, colas de mensajes de registro, etc. El programa de instalación de RMS configura las listas DACL de los recursos que crea y expone, y también configura la autenticación de IIS para cada recurso.

En esta sección, se proporciona información sobre el modo en que RMS configura la seguridad de los recursos que utiliza, y sobre el modo en que obtiene acceso a los recursos durante las distintas fases de su funcionamiento: instalación, establecimiento de servicios en línea y normal.

Se tratan los siguientes temas:

-   [Grupos de seguridad de RMS](https://technet.microsoft.com/25749a83-8c12-48ec-96ad-296d31fd55d4)
-   [Modos de seguridad para RMS](https://technet.microsoft.com/d7792293-5bb2-4232-9d48-e81e87ab6219)
-   [Seguridad durante la instalación de RMS](https://technet.microsoft.com/0a3d40b2-f27e-4e63-baff-a9c8433f5f91)
-   [Seguridad durante el establecimiento de los servicios en línea](https://technet.microsoft.com/9f1282c5-5642-4870-a9a4-c3a485f8ff76)
-   [Seguridad durante el funcionamiento normal de RMS](https://technet.microsoft.com/98f3d584-6320-4aa1-9959-7133cfdb6df7)
