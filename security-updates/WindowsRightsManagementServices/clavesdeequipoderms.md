---
TOCTitle: Claves de equipo de RMS
Title: Claves de equipo de RMS
ms:assetid: '56e59ec2-f681-4ca2-98c7-72218ab9e9d9'
ms:contentKeyID: 18127819
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747572(v=WS.10)'
---

Claves de equipo de RMS
=======================

Los equipos cliente de RMS SP1 tienen un par de claves RSA de 1024 bits, que se denominan claves de equipo.

La clave pública del equipo se usa para cifrar la clave privada del certificado de cuenta de permisos. El certificado de equipo de RMS contiene la clave pública del equipo. La caja de seguridad contiene la clave privada del equipo, que se usa para descifrar el certificado de cuenta de permisos con el fin de permitir el uso de la clave privada del usuario.
