---
TOCTitle: Copia de seguridad y restauración del sistema RMS
Title: Copia de seguridad y restauración del sistema RMS
ms:assetid: 'c11f3ac1-e512-402b-bf13-9ff21f5fe745'
ms:contentKeyID: 18127946
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747745(v=WS.10)'
---

Copia de seguridad y restauración del sistema RMS
=================================================

Al planear la recuperación del sistema, deberá tener en cuenta un posible error del servidor de base de datos o del servidor de RMS. En caso de error del servidor de base de datos, puede restaurar las funciones de un clúster o servidor de RMS a partir de una copia de seguridad de la base de datos de configuración. Para hacerlo, no necesita obtener un nuevo certificado emisor de licencias de servidor o una clave privada nueva para el servidor de RMS, puesto que estos elementos se almacenan en la base de datos de configuración.

Planeamiento de una copia de seguridad del sistema RMS
------------------------------------------------------

Además de la clave del servidor, también se almacenan en la base de datos de configuración los datos de usuario, incluida la información de la clave pública. Para proteger los valiosos datos de claves, realice una copia de seguridad de la base de datos de configuración en medios y guárdelos en una ubicación segura. La base de datos de configuración del clúster de certificación raíz cambia frecuentemente, por lo que es recomendable realizar copias de seguridad regularmente. Cuanta mayor sea la frecuencia con que se agregan usuarios nuevos a su organización, tanto mayor debe ser la frecuencia con que realice copias de seguridad. Si está realizando una copia de seguridad del servidor de certificación raíz, deberá asegurarse también de incluir la tabla **sysmessages** de la base de datos principal en la copia de seguridad. Si esta tabla no incluye los mensajes específicos de RMS, el servidor de certificación raíz no podrá funcionar y devolverá un error. Si esta tabla no está en la copia de seguridad, puede volverse a crear repitiendo el proceso de establecimiento de los servicios en línea utilizando una base de datos existente.

La base de datos de registro de RMS contiene registros que pueden proporcionar datos interesantes de solución de problemas o de estadísticas, pero normalmente no es crítica para un sistema RMS. La base de datos de servicios de directorio es una caché local de la base de datos de Active Directory, de forma que se vuelve a crear automáticamente al restaurar un sistema RMS. Para establecer un plan para realizar copias de seguridad de las bases de datos de RMS, consulte al administrador de SQL Server.

Si utiliza un módulo de seguridad de hardware para proteger las claves privadas de RMS, también debe realizar una copia de seguridad de la configuración del módulo de seguridad de hardware. Para obtener más información acerca de cómo realizar copias de seguridad y restaurar la configuración del módulo de seguridad de hardware, consulte la documentación de dicho módulo.

> [!NOTE]
> Si ha utilizado un proveedor de servicios de cifrado (CSP) de software que no sea el predeterminado para cifrar las claves privadas de RMS, asegúrese de que existan prácticas de administración de claves en la organización (como los procedimientos de copia de seguridad y restauración) para ese CSP antes de utilizarlo con RMS. 

Planeamiento de la restauración de un sistema RMS
-------------------------------------------------

Si está restaurando un servidor de base de datos de una copia de seguridad, asegúrese de que la versión de RMS en ejecución sea la misma que la que estaba en ejecución cuando se creó la copia de seguridad. Informe a los usuarios del sistema RMS de que si empezaron a utilizar el sistema RMS después de la fecha de la copia de seguridad, deberán obtener un nuevo certificado de cuenta de permisos. Como resultado, no se pierde contenido protegido.

Para restaurar un único servidor de RMS de un clúster, reconstruya el servidor, reinstale RMS y, a continuación, una el servidor al clúster mediante la base de datos existente. Esta actividad no afecta a los usuarios del sistema RMS, ya que los servidores agrupados en un clúster funcionan como uno solo.
