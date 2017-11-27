---
TOCTitle: Eliminación de cuentas de usuario
Title: Eliminación de cuentas de usuario
ms:assetid: 'bf73b141-d4d1-4807-a773-3aaff58b0db6'
ms:contentKeyID: 18127931
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747653(v=WS.10)'
---

Eliminación de cuentas de usuario
=================================

Cuando se elimina una cuenta de usuario de Active Directory, no se elimina automáticamente la entrada del certificado de cuenta de permisos del usuario que se encuentra en la tabla de claves de usuario de la base de datos de configuración del clúster de configuración raíz. Por esta razón, la tabla de claves de usuario puede crecer sin límites a medida que se agregan claves de usuario sin que se eliminen las antiguas.

Para mantener la base de datos de configuración, puede ejecutar un procedimiento almacenado que elimine una clave de usuario según su identificador de seguridad (SID) cada vez que la cuenta de usuario asociada se quite de Active Directory. Como alternativa, puede ejecutar periódicamente una secuencia de comandos que elimine todas las claves de usuario de la base de datos de configuración cuando los SID asociados dejen de existir en Active Directory. Tenga en cuenta que este paso supone una gran carga sobre SQL Server y Active Directory.
