---
TOCTitle: Exclusión de versiones de la caja de seguridad
Title: Exclusión de versiones de la caja de seguridad
ms:assetid: 'e287f026-aab2-43ab-93bc-48087da82f36'
ms:contentKeyID: 18128001
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747700(v=WS.10)'
---

Exclusión de versiones de la caja de seguridad
==============================================

Puede asegurarse de que los clientes utilicen una versión mínima del software de cliente de RMS utilizando la versión de caja de seguridad asociada con el cliente para excluir las versiones anteriores del software de cliente de RMS. Cuando habilite esta característica, especifique la versión mínima de caja de seguridad más reciente que haya firmado el servicio de activación de Microsoft. A continuación, habilite la exclusión de la caja de seguridad en el sitio Web de administración de cada clúster en el que desee que entre en vigor. Todas las solicitudes de licencias y certificación se comprueban para garantizar que la caja de seguridad cumpla los criterios de versión mínima.

Si ha habilitado la exclusión según la versión de la caja de seguridad, los clientes que utilicen una versión anterior al valor especificado no podrán adquirir certificados de cuenta de permisos ni licencias de uso, puesto que sus solicitudes se verán denegadas. Estos clientes deben instalar una nueva versión del software de cliente de RMS para adquirir una nueva caja de seguridad que utilice la versión actual del software.

El cliente de RMS para Service Pack 1 (SP1) utiliza una versión de la caja de seguridad superior o igual a 5.0.0.0. Al establecer la exclusión de la caja de seguridad en esa versión mínima, obligará a los clientes de RMS de la organización a actualizar al cliente de RMS para SP1 a fin de utilizar contenido protegido con RMS.

Si se han emitido anteriormente licencias de contenido para un usuario cuya caja de seguridad esté excluida, éste todavía podrá utilizar el contenido sin adquirir una nueva caja de seguridad.
