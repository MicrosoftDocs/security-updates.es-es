---
TOCTitle: Supresión de la protección de RMS del contenido
Title: Supresión de la protección de RMS del contenido
ms:assetid: 'c30361e3-50d2-4474-a87d-d38de502cf9e'
ms:contentKeyID: 18127939
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747658(v=WS.10)'
---

Supresión de la protección de RMS del contenido
===============================================

Decida con antelación qué archivos se recuperarán, quién los recuperará y cuándo, de modo que se conserve la información importante cuando haya terminado el proceso de retiro. Cuando haya eliminado la protección de RMS de todos los archivos protegidos con RMS necesarios, el servidor podrá eliminarse de la infraestructura.

Para quitar la protección de RMS del contenido, siga el procedimiento siguiente:

1.  El usuario debe eliminar del equipo todas las licencias de uso existentes. Esto garantiza que el cliente de RMS vaya al servidor para adquirir una licencia para abrir el contenido. Las licencias de uso se almacenan en la carpeta %USERPROFILE%\\Local Settings\\Application Data\\Microsoft\\DRM del equipo cliente, y el nombre de archivo va precedido por el prefijo EUL.
2.  Un usuario con acceso al servidor de retiro intenta abrir un archivo protegido con RMS.
3.  La aplicación se conecta al servidor de retiro y recibe la clave de contenido.
4.  El contenido se descifra y puede editarse, guardarse, reenviarse o imprimirse.
5.  El usuario guarda el contenido sin protección de RMS. Ahora todos los usuarios pueden abrir el contenido sin necesidad de conectarse al servidor de RMS.
