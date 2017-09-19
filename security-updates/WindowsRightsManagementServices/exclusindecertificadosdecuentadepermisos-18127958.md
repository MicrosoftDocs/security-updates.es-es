---
TOCTitle: Exclusión de certificados de cuenta de permisos
Title: Exclusión de certificados de cuenta de permisos
ms:assetid: 'cba5e901-942c-4d06-9865-e6c4648c95e6'
ms:contentKeyID: 18127958
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747670(v=WS.10)'
---

Exclusión de certificados de cuenta de permisos
===============================================

Si un usuario es de confianza pero sus credenciales de RMS están comprometidas, puede excluir la clave pública del usuario a fin de excluir su certificado de cuenta de permisos. Cuando haga esto, RMS denegará las nuevas solicitudes de licencias de uso que incluyan dicho certificado de cuenta. Una vez que haya excluido un certificado de cuenta de permisos, la vez siguiente que el usuario intente adquirir una licencia de uso para contenido nuevo, ésta será denegada. Para adquirir una licencia de uso, el usuario tendrá que obtener un nuevo certificado de cuenta de permisos con un nuevo par de claves.

Los certificados de cuenta de permisos pueden excluirse utilizando la página **Directivas de exclusión** del sitio Web de administración de RMS. Cuando excluya el certificado de cuenta de un usuario, RMS agregará la clave excluida, el nombre de cuenta del usuario, así como la fecha y la hora de la exclusión a la tabla DRMS\_GicExclusionList de la base de datos de configuración del clúster de certificación raíz. Esta información también aparece en la página **Directivas de exclusión** del sitio Web de administración. Asimismo, RMS elimina las claves privada y pública que estén asociadas al certificado de cuenta excluido de la tabla UD\_Users de la base de datos de configuración.

Para excluir un certificado de cuenta de permisos que esté en el servidor o clúster de certificación raíz, especifique la cuenta de dominio del usuario en la página **Directivas de exclusión** del servidor de certificación raíz. Debe excluir un certificado de cuenta de permisos en todos los servidores subinscritos en el sitio Web de administración de cada servidor. Para excluir un usuario en un servidor o clúster de licencias subinscrito, escriba el valor de la clave pública del certificado de cuenta de permisos en la página **Directivas de exclusión** del sitio Web de administración del servidor de licencias. Puede obtener este valor en la página **Directivas de exclusión** del sitio Web de administración del clúster de certificación raíz.

Para simplificar la exclusión de certificados de cuenta de permisos en una implementación de Windows RMS con varios clústeres, puede replicar la tabla DRMS\_GicExclusionList de la base de datos de configuración del clúster de certificación raíz en la base de datos de configuración de cada clúster de licencias. Si lo hace, no tendrá que especificar manualmente el valor de la clave pública en cada uno de los servidores.
