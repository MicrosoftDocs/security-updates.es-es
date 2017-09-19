---
TOCTitle: Grupos de seguridad de RMS
Title: Grupos de seguridad de RMS
ms:assetid: '25749a83-8c12-48ec-96ad-296d31fd55d4'
ms:contentKeyID: 18127697
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720215(v=WS.10)'
---

Grupos de seguridad de RMS
==========================

El programa de instalación de RMS crea dos grupos: el grupo de servicio de RMS y el grupo de superusuarios.

El grupo de servicio de RMS es un grupo de seguridad local que tiene concedidos permisos suficientes para obtener acceso a todos los recursos necesarios para el funcionamiento de RMS. Durante la instalación, el administrador especifica una cuenta de usuario para usarla como la cuenta de servicio de RMS. Esta cuenta de usuario se convierte automáticamente en integrante del grupo de servicio de RMS y, por tanto, tiene concedidos sus permisos. RMS se ejecuta con esta cuenta de usuario durante la mayor parte del funcionamiento normal.

Otro grupo importante de RMS es el grupo de superusuarios. Este grupo tiene control total sobre todo el contenido, lo que significa que un integrante de este grupo puede descifrar todos los archivos de contenido protegidos con RMS y quitar todas las protecciones de RMS que tengan. El grupo de superusuarios no tiene integrantes de forma predeterminada y tampoco incluye automáticamente a los administradores de RMS. Administrar correctamente la pertenencia a este grupo es vital para la seguridad del contenido protegido con RMS. Para obtener más información, vea "Uso del grupo de superusuarios" en "Operación de un servidor de RMS", en esta recopilación de documentación.
