---
TOCTitle: Activación de equipo RMS
Title: Activación de equipo RMS
ms:assetid: '09a0d631-9860-477f-9d10-df61b3bfe125'
ms:contentKeyID: 18127681
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720182(v=WS.10)'
---

Activación de equipo RMS
========================

La activación de equipo es un prerrequisito para la publicación o utilización de contenido protegido con RMS en un equipo cliente. La activación de equipo es el proceso por el cual a un equipo cliente se le asigna una caja de seguridad única y el certificado de equipo de RMS correspondiente. La caja de seguridad contiene la clave privada del equipo, y el certificado de equipo contiene la clave pública del equipo. Puesto que la caja de seguridad contiene la clave privada del equipo, constituye el centro de seguridad para cifrado y descifrado. Cada uno de los usuarios del equipo tendrá un certificado de equipo único creado por el proceso de activación del equipo.

El proceso de activación del equipo utilizado con el cliente de RMS para Service Pack 1 es considerablemente diferente del proceso de activación de equipo en la versión 1. El cliente de RMS para Service Pack 1 es de activación automática. Cuando un usuario registrado instala el cliente RMS o un usuario que haya iniciado sesión utiliza por primera vez una característica de RMS, el cliente inicia el proceso de activación, que genera varios conjuntos de claves mediante la API de cifrado incluida en Windows. Estas claves se utilizan para realizar un conjunto de cifrados que generan un certificado de equipo que enlaza el usuario, el equipo y el cliente de RMS en la jerarquía de confianza de RMS.
