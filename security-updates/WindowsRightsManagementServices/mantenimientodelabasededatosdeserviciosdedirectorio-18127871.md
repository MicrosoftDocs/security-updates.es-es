---
TOCTitle: Mantenimiento de la base de datos de servicios de directorio
Title: Mantenimiento de la base de datos de servicios de directorio
ms:assetid: '911a62f2-c1d6-4091-99b0-b53211be27a7'
ms:contentKeyID: 18127871
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747680(v=WS.10)'
---

Mantenimiento de la base de datos de servicios de directorio
============================================================

RMS incluye una base de datos de servicios de directorio albergada en el servidor de base de datos, que contiene información sobre usuarios, identificadores (como por ejemplo direcciones de correo electrónico), Id. de seguridad (SID), pertenencia a grupos e identificadores alternativos. Esta información se obtiene de las consultas LDAP que realiza el servicio de emisión de licencias de RMS al catálogo global de Active Directory, y se almacena localmente en esta base de datos para mejorar el tiempo de respuesta del servidor cuando los usuarios solicitan licencias de uso.

Dado que se insertan y se eliminan datos con frecuencia en esta base de datos, ésta es propensa a la fragmentación. Deberá realizar periódicamente (cada día o cada semana) una reorganización de los índices de todas las tablas de la base de datos DRMS\_DirectoryServices. Se reconstruirán los índices para que los datos ya no estén fragmentados. Si los datos están fragmentados, puede empeorar el rendimiento e incluso pueden producirse errores del servidor, si se permite que siga funcionando sin intervención del administrador.

Si utiliza SQL Server como servidor de base de datos, pueden llevarse a cabo reorganizaciones de la base de datos mediante el Asistente para mantenimiento, o ejecutando su propio comando personalizado a través del Agente SQL Server.

Si observa que el registro de transacción crece demasiado al reindizar la base de datos, puede minimizar este crecimiento cambiando del modo de recuperación completa al modo Registro masivo antes de reindizar.
