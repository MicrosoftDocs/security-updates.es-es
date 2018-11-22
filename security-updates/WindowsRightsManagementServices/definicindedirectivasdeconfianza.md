---
TOCTitle: Definición de directivas de confianza
Title: Definición de directivas de confianza
ms:assetid: 'e8d78300-4b26-4f15-9e4f-5ae9eb827ef9'
ms:contentKeyID: 18128000
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747711(v=WS.10)'
---

Definición de directivas de confianza
=====================================

Puede definir dominios de publicación y de usuario de confianza de la siguiente manera:

-   **Dominios de usuarios de confianza**. Cuando agregue un dominio de usuario, RMS podrá procesar solicitudes de licencias de uso procedentes de usuarios cuyos certificados de cuenta de permisos hayan sido emitidos por una instalación de RMS de un bosque de Active Directory diferente, es decir, un clúster de certificación raíz diferente. Agregue un dominio de usuario de confianza importando el certificado emisor de licencias de servidor de la instalación en la que desea confiar.
-   **Dominios de publicación de confianza**. La adición de un dominio de publicación permite que un servidor de RMS emita licencias de uso utilizando licencias de publicación que hayan sido emitidas por otro servidor de RMS. Agregue un dominio de publicación de confianza importando el certificado emisor de licencias de servidor y la clave privada de la instalación en la que desee confiar.

Para obtener más información, vea “[Adición y desinstalación de dominios de usuarios de confianza](https://technet.microsoft.com/7c440b15-01c4-49f1-b43c-00f67f3388c1)” y “[Adición y desinstalación de dominios de publicación de confianza](https://technet.microsoft.com/d87b502d-5497-4ccd-badf-f6807d587cee)”, más adelante en este tema. Para obtener instrucciones paso a paso, vea “[Establecimiento de directivas de confianza](https://technet.microsoft.com/6c2be3c2-1837-4de4-a72e-3ba3eec3321d)”, más adelante en este tema.
