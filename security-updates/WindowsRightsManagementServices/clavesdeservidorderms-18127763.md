---
TOCTitle: Claves de servidor de RMS
Title: Claves de servidor de RMS
ms:assetid: '5f4100a1-9aa5-42af-85c8-4bc691022f06'
ms:contentKeyID: 18127763
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720280(v=WS.10)'
---

Claves de servidor de RMS
=========================

Un servidor de RMS tiene un par de claves de 1024 bits de RSA.

La clave pública del servidor se usa para cifrar la clave de contenido que se encuentra en la licencia de publicación, de forma que sólo el servidor de RMS pueda recuperar la clave de contenido y emitir licencias de uso para esa licencia de publicación. El certificado emisor de licencias de servidor contiene la clave pública del servidor.

La clave privada del servidor se usa para firmar todos los certificados y licencias que emita el servidor.

Protección de la clave privada del servidor
-------------------------------------------

De forma predeterminada, durante el establecimiento de servicios en línea, se crea la clave privada del servidor y se almacena cifrada en la base de datos de RMS. Como alternativa, durante el establecimiento de servicios en línea, se puede especificar un proveedor de servicios de cifrado (CSP) que esté ya instalado en el servidor.

Este CSP se puede usar de dos formas distintas:

-   Elegir entre las implementaciones de CSP de software instaladas de forma predeterminada con el servidor.
    O bien
-   Usar un CSP de software que no es de Microsoft que ha instalado en el servidor.

> [!NOTE]
> Si se desea usar un módulo de protección de hardware, será preciso asegurarse de seleccionar un CSP compatible con este tipo de módulos. 

Si se decide a proteger la clave privada del servidor mediante un CSP, RMS almacenará el nombre del proveedor y el del contenedor de la clave que figura en la base de datos de configuración.
