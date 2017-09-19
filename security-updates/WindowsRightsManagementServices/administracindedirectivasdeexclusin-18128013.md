---
TOCTitle: Administración de directivas de exclusión
Title: Administración de directivas de exclusión
ms:assetid: 'ee31e099-e095-4648-95da-0009fbeb48cb'
ms:contentKeyID: 18128013
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747730(v=WS.10)'
---

Administración de directivas de exclusión
=========================================

Puede implementar directivas de exclusión de servidor para denegar las solicitudes de licencias y certificados que se basen en el certificado de cuenta de permisos o la versión de caja de seguridad. Las directivas de exclusión deniegan las nuevas solicitudes de licencias y certificados realizadas por entidades principales comprometidas, pero, al contrario que la revocación, no invalidan las entidades principales. Los administradores también pueden excluir aplicaciones comprometidas o potencialmente dañinas, de forma que no puedan descifrar contenido protegido con RMS. Asimismo, los administradores pueden excluir ciertas versiones de los sistemas operativos de Windows a fin de impedir que los equipos cliente que ejecuten dichas versiones puedan utilizar contenido protegido con permisos.

Cuando se excluye una entidad, las licencias de uso creadas por el servidor de RMS especifican dicha entidad en la lista de exclusión. Si, tras un período de tiempo, decide eliminar una entidad que previamente había incluido en una directiva de exclusión, puede eliminarla en la página Directivas de exclusión del sitio Web de administración. Se quitará la entidad de la lista de exclusión. Las nuevas solicitudes de licencias o certificación no considerarán esta entidad como excluida.

A no ser que haya excluido accidentalmente una entidad, es recomendable que no quite una entidad de una directiva de exclusión hasta que esté seguro de que hayan caducado todos los certificados que se emitieron antes de crear la directiva de exclusión. De lo contrario, tanto los certificados antiguos como los nuevos permitirán que se descifre el contenido, algo que es posible que su organización no desee.

Este tema proporciona información sobre la administración de directivas de exclusión. Para obtener instrucciones paso a paso sobre la exclusión de entidades, vea “[Habilitación de directivas de exclusión](https://technet.microsoft.com/bbb1ce50-bc11-41cf-b75b-a6756141908f)”, más adelante en este tema.

Se tratan los siguientes temas:

-   [Exclusión de versiones de la caja de seguridad](https://technet.microsoft.com/e287f026-aab2-43ab-93bc-48087da82f36)
-   [Exclusión de certificados de cuenta de permisos](https://technet.microsoft.com/cba5e901-942c-4d06-9865-e6c4648c95e6)
-   [Exclusión de versiones de Windows](https://technet.microsoft.com/8b8a184d-ac0e-4a43-822c-d2fae2faf484)
-   [Exclusión de aplicaciones](https://technet.microsoft.com/b68ae4b2-b9ba-44ae-90cb-c88df600ec86)
