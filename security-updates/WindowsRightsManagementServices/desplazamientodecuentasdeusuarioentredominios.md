---
TOCTitle: Desplazamiento de cuentas de usuario entre dominios
Title: Desplazamiento de cuentas de usuario entre dominios
ms:assetid: '0010b0ea-07c0-41c9-81f7-5881343d1d55'
ms:contentKeyID: 18127707
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720179(v=WS.10)'
---

Desplazamiento de cuentas de usuario entre dominios
===================================================

Cuando se configura un servidor de certificación raíz de una organización y se establecen los servicios en línea en él, el servidor se registra en Active Directory en una configuración por bosque como proveedor de servicios de RMS. Sólo puede existir un clúster de certificación raíz en cada bosque de Active Directory.

En general, cuando se mueve una cuenta de usuario de un dominio a otro del mismo bosque, se crea un nuevo SID para la cuenta de usuario del nuevo dominio. Después, cuando un usuario intenta adquirir un nuevo certificado de cuenta del servidor, el usuario parece ser un usuario nuevo en el servidor debido al nuevo SID. El servidor genera claves nuevas para el usuario y emite el nuevo certificado de cuenta de permisos utilizando la dirección de correo electrónico original del usuario. Cuando el usuario intente utilizar el nuevo certificado de cuenta de permisos con una licencia existente, el SID y las claves no coincidirán y será necesario que adquiera una licencia nueva. Esto también ocurre cuando se mueve una cuenta de usuario a un dominio de un bosque diferente.
