---
TOCTitle: Exclusión de RMS
Title: Exclusión de RMS
ms:assetid: 'c17e393e-b6a9-4ae5-aee5-18baa6b32d4d'
ms:contentKeyID: 18127947
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747656(v=WS.10)'
---

Exclusión de RMS
================

Las exclusiones evitan que entidades principales específicas adquieran nuevas licencias de un clúster o servidor de RMS determinado. Sin embargo, a diferencia de la revocación, la exclusión no invalida las entidades principales. Cualquier licencia existente que esté asociada con entidades principales excluidas es aún válida, sólo se denegarán las nuevas solicitudes de licencias.

Todos los clústeres o servidores de RMS poseen directivas de exclusión propias, y estas directivas no se propagan por el sistema. Desde el sitio Web de **administración de RMS**, los administradores establecen las directivas de exclusión para cada uno de los clústeres o servidores de RMS.

Los administradores pueden excluir entidades principales basándose en la versión de la caja de seguridad, la versión de Windows, el certificado de cuenta de permisos o la aplicación compatible con RMS.
