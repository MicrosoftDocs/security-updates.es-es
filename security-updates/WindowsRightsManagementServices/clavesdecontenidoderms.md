---
TOCTitle: Claves de contenido de RMS
Title: Claves de contenido de RMS
ms:assetid: '63c814bf-2809-477e-a2db-d90370442075'
ms:contentKeyID: 18127775
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720284(v=WS.10)'
---

Claves de contenido de RMS
==========================

Cuando un autor publica contenido protegido con RMS, una aplicación compatible con RMS crea una clave de contenido simétrica y la usa para cifrarlo. RMS utiliza Advanced Encryption Standard (AES) para crear la clave de contenido.

La clave de contenido se incluye en la licencia de publicación y se cifra con la clave pública del servidor de RMS que emitió la licencia.

Cuando el servidor recibe una solicitud de una licencia de uso, descifra la clave del contenido con la clave privada del servidor y, a continuación, vuelve a cifrarla con la clave pública del usuario (que recibió como parte de la solicitud). La clave de contenido se incluye en la licencia de uso.
