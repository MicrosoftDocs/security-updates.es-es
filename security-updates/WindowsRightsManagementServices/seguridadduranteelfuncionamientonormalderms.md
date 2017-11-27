---
TOCTitle: Seguridad durante el funcionamiento normal de RMS
Title: Seguridad durante el funcionamiento normal de RMS
ms:assetid: '98f3d584-6320-4aa1-9959-7133cfdb6df7'
ms:contentKeyID: 18127887
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747609(v=WS.10)'
---

Seguridad durante el funcionamiento normal de RMS
=================================================

Después de instalar y establecer los servicios en línea de RMS, los servicios Web de RMS funcionan como aplicaciones de IIS, obteniendo acceso a diversos recursos del sistema que requieren autenticación y autorización. Todos los recursos del sistema precisan de autenticación y no pueden configurarse de ningún otro modo. El resto de esta página describe el diseño de la autorización en RMS.

Los servicios Web de RMS se ejecutan en el contexto de un grupo de aplicaciones de IIS. Cada grupo de aplicaciones de IIS posee una identidad única que puede corresponder a una cuenta de usuario de dominio, una cuenta de usuario local, la cuenta local de servicio de red o del sistema local. Cada una de estas cuentas posee diversos grados de autorización en el sistema. Al establecer los servicios en línea de RMS, puede optar por ejecutar los servicios Web de RMS con la cuenta del sistema local o con una cuenta de usuario de dominio. A continuación, esta cuenta se convierte en la identidad del grupo de aplicaciones de RMS. El grupo de aplicaciones para el sitio Web Administración global es "DRMS Application Pool". El grupo de aplicaciones para el sitio Web donde establezca servicios en línea se denomina "\_DRMSAppPool1". El servicio de registro de RMS se ejecuta como un servicio de Windows independiente en la misma cuenta que se especifique para la identidad del grupo de aplicaciones de RMS.

Los recursos a los que los servicios Web de RMS necesitan tener acceso incluyen diversos archivos y carpetas del sistema, las bases de datos y los procedimientos almacenados en el servidor de base de datos, el registro local, Active Directory, la caché de ensamblados, la memoria y otros procesos que se ejecutan en el sistema. El servicio de registro de RMS también necesita acceso a la cola de registro en el sistema local. Todos estos recursos poseen sus propias listas DACL, que definen quién está autorizado para tener acceso al recurso y qué puede hacer con él.

Para simplificar la asignación de permisos y la administración de las cuentas de servicio, todos los permisos necesarios se asignan al grupo de servicio de RMS local que RMS creó durante el establecimiento de los servicios en línea. Puesto que la cuenta de servicio de RMS pertenece a este grupo, recibe todos los permisos asignados a él.

En la lista siguiente, se resumen los permisos que se conceden al grupo de servicio de RMS (RMS Service Group):

-   Permiso de lectura para los directorios raíz virtuales

-   Permiso de escritura para el directorio de la caché de ensamblados

-   Permiso de escritura para el directorio temporal del sistema

-   Permiso de escritura para la cola de registro

-   Permiso de lectura para Active Directory

Si utiliza Microsoft SQL Server 2000 como servidor de base de datos, debe tener en cuenta que utiliza un método algo distinto de asignación de permisos al de Windows Server 2003. Al establecer los servicios en línea de RMS se crea un inicio de sesión para la cuenta de servicio de RMS en el servidor SQL Server. Si eligió establecer los servicios en línea de RMS con la cuenta de sistema local, se crea un inicio de sesión de SQL Server con el formato *DOMINIO\\nombre\_equipo*, donde *DOMINIO* es el nombre del dominio de Active Directory al que pertenece el equipo y *nombre\_equipo* es el nombre del servidor. Se crea una función de SQL denominada rms\_service a la que se conceden todos los permisos necesarios. Se agrega el inicio de sesión de la cuenta de servicio de RMS a este grupo. No se conceden permisos explícitamente a la cuenta de servicio de RMS.

Asimismo, el servidor SQL Server asigna un propietario de base de datos (DBO) a cada base de datos. La propiedad de la base de datos se asigna de la siguiente manera durante el establecimiento de los servicios en línea:

-   Se asigna la cuenta de dominio que se utilizó para establecer los servicios en línea de RMS como DBO de la base de datos de configuración.

-   Se asigna la cuenta de servicio de RMS como DBO de las bases de datos de registro y servicios de directorio.

Los permisos para todos los recursos que ha creado RMS se han seleccionado detenidamente durante el diseño de RMS a fin de maximizar la seguridad. No debe haber ningún motivo para modificar los permisos que se asignan durante el establecimiento de los servicios en línea para ninguno de los recursos. Si debe cambiar la cuenta de usuario o la contraseña de la cuenta de servicio después de haber establecido los servicios en línea, puede hacerlo desde la página Web Administración global de RMS. Para obtener más información, vea "Para cambiar la cuenta de servicio de RMS" en "Operación de un servidor de RMS", en esta recopilación de documentación.