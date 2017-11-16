---
TOCTitle: Creación de la cuenta de servicio de RMS
Title: Creación de la cuenta de servicio de RMS
ms:assetid: '6eb38729-f0f0-431a-bc8c-17102cf175d8'
ms:contentKeyID: 18127845
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747546(v=WS.10)'
---

Creación de la cuenta de servicio de RMS
========================================

Durante la instalación, RMS crea un grupo de seguridad llamado **grupo de servicio de RMS** en el equipo local y le concede los permisos adecuados sobre todos los recursos necesarios para que RMS funcione.

Al establecer los servicios en línea de RMS en un servidor, se especifica una cuenta de usuario como la cuenta de servicio de RMS. La cuenta que especifica se convierte en miembro del grupo de servicio de RMS, y se le conceden los permisos asociados a este grupo. Durante el funcionamiento normal, RMS se ejecuta bajo la cuenta de servicio de RMS para la mayoría de los fines.

> [!NOTE]
> La cuenta de servicio de RMS no puede ser la misma cuenta de dominio que se utilizó para instalar RMS. 

Por motivos de seguridad, se recomienda crear una cuenta de usuario especial para utilizar la cuenta de servicio de RMS y no utilizarla para ningún otro propósito. Además, no debe otorgar a esta cuenta ningún permiso adicional.

> [!IMPORTANT]
> Debe crear esta cuenta de usuario especial antes de instalar RMS y establecer los servicios en línea. 

Para obtener más información acerca de los permisos que se conceden al grupo de servicio de RMS y las cuentas bajo las que se ejecuta RMS, vea “Modelo de seguridad de RMS” en “Referencia técnica de RMS”, en esta recopilación de documentación.
