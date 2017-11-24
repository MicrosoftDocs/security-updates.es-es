---
TOCTitle: Claves de emisor de licencias de cliente
Title: Claves de emisor de licencias de cliente
ms:assetid: '28781125-2692-4ff9-99b1-e09227d72966'
ms:contentKeyID: 18127699
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720221(v=WS.10)'
---

Claves de emisor de licencias de cliente
========================================

Los autores pueden adquirir certificados emisores de licencias de cliente para publicar contenido protegido con RMS mientras no están conectados a la red compatible con RMS. Los certificados emisores de licencias de cliente tienen un par de claves RSA de 1024 bits.

El cliente de RMS utiliza la clave pública del certificado emisor de licencias de cliente al emitir una licencia de publicación para llevar a cabo las siguientes tareas:

-   Cifrar la clave de contenido simétrica.
-   Firmar las licencias de publicación que se emiten localmente mientras el usuario no está conectado a la red.
