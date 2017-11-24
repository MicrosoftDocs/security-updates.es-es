---
TOCTitle: Claves de usuario
Title: Claves de usuario
ms:assetid: '12dad6e2-64e7-4bab-bde7-b72f90f5cb05'
ms:contentKeyID: 18127732
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720202(v=WS.10)'
---

Claves de usuario
=================

Un usuario de RMS tiene un par de claves de 1024 bits de RSA. El par de claves del usuario se almacena en la base de datos de configuración de RMS, de forma que un usuario dado siempre tenga el mismo par de claves en todo el sistema RMS.

Un certificado de cuenta de permisos contiene la clave pública del usuario. Esta clave se utiliza para cifrar la clave de contenido que se encuentra en las licencias de uso, de modo que sólo un usuario determinado pueda utilizar contenido protegido con RMS usando esta licencia.

El mismo certificado de cuenta de permisos contiene también la clave privada del usuario, que está cifrada con la clave pública de un equipo cliente. Esto garantiza que un certificado de cuenta de permisos pueda utilizarse únicamente en el equipo para el que se emitió, pero que todos los certificados de cuenta de permisos de un usuario determinado contengan siempre el mismo par de claves. La clave privada de usuario es necesaria para utilizar cualquier contenido que se haya protegido con RMS.
