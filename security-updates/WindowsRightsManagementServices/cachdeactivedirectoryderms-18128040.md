---
TOCTitle: Caché de Active Directory de RMS
Title: Caché de Active Directory de RMS
ms:assetid: 'c721a2eb-2fe9-4346-b426-3cc169b97265'
ms:contentKeyID: 18128040
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747662(v=WS.10)'
---

Caché de Active Directory de RMS
================================

Todos los clústeres o servidores de certificación raíz y servidores de licencias de RMS tienen una caché de Active Directory local que contiene el resultado de las consultas sobre pertenencia a grupos realizadas en el catálogo global de Active Directory. Además de la caché que se encuentra en cada servidor, existe una caché compartida en cada clúster almacenada en la base de datos de servicios de directorio. La finalidad de estas cachés es reducir el número de consultas que se envían al catálogo global y minimizar así el tiempo de respuesta para las solicitudes de licencias.

Cuando un usuario solicita una licencia de uso, el servidor debe evaluar si ese usuario tiene o no los permisos necesarios en la licencia de publicación. En el caso más simple, el usuario que solicita una licencia aparece nombrado explícitamente en la licencia de publicación. Sin embargo, en muchos otros casos, el autor otorga permisos a un grupo, en lugar de a usuarios individuales.

Si la licencia de publicación no nombra explícitamente al usuario solicitante, sino que concede permisos a un grupo, el servidor deberá evaluar la pertenencia a grupos del usuario para determinar si éste es integrante o no de un grupo al que se le hayan otorgado permisos. Para ello, el servidor enviará una consulta LDAP al catálogo global.

Los servidores de RMS almacenan todos los resultados de las consultas de pertenencia a grupos en la caché de Active Directory local y en la base de datos de los servicios de directorio del clúster. De este modo, los servidores pueden obtener información sobre la pertenencia a grupos de dichas cachés, lo que reduce el número de consultas que deben enviar al catálogo global. De forma predeterminada, la consulta se realiza en el servidor más cercano, sin embargo, se puede configurar la clave del Registro GC para especificar los servidores del catálogo global a los que se deben enviar las consultas. Para obtener más información acerca de esta configuración, vea "Modificación de la configuración del Registro del grupo de conexiones de Active Directory" en "Operación de un servidor de RMS", en esta recopilación de documentación.

Para evaluar la pertenencia a grupos de un usuario, el servidor comprueba primero su caché para ver si la información sobre este usuario está ya almacenada. Si no lo está, el servidor comprueba la base de datos de servicios de directorio del clúster. Si la información de pertenencia a grupos tampoco está almacenada en esta base de datos, el servidor envía una consulta al catálogo global.

En el caso de usuarios y grupos, se almacenan los siguientes atributos de Active Directory en las cachés:

-   mail
-   ProxyAddresses (sólo direcciones de correo electrónico SMTP)
-   objectSID
-   sidHistory
-   memberOf (GUID de los grupos de los que el usuario o grupo es integrante)

En las entradas de la caché local de Active Directory se registra la fecha y hora en que se almacenaron. La configuración del Registro especifica el período de validez de las entradas que se encuentran en la caché, así como el número total de entradas que pueden almacenarse. Esta configuración puede afectar al rendimiento de los servidores. Para obtener más información, vea "Modificación de la configuración de caché de Active Directory" en "Operación de un servidor de RMS", en esta recopilación de documentación.
