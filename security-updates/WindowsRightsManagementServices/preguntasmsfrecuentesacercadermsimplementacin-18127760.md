---
TOCTitle: 'Preguntas más frecuentes acerca de RMS: Implementación'
Title: 'Preguntas más frecuentes acerca de RMS: Implementación'
ms:assetid: '5559ae65-77ae-4e0b-bfd8-3512409ed29b'
ms:contentKeyID: 18127760
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720274(v=WS.10)'
---

Preguntas más frecuentes acerca de RMS: Implementación
======================================================

Preguntas más frecuentes acerca de la implementación de RMS
-----------------------------------------------------------

-   [Si las entidades principales de seguridad que se utilizan en RMS son miembros de la lista global de direcciones (GAL), ¿existe alguna dependencia en la versión de Exchange?](#bkmk_20)
-   [¿Qué papel tiene SQL Server en RMS?](#bkmk_21)
-   [¿Debe estar unido el equipo de un usuario al mismo dominio que el clúster de RMS para usar RMS?](#bkmk_22)
-   [Si un cliente desea poner el servidor de RMS en una red perimetral, ¿qué puertos deben estar abiertos en el firewall para Internet y el firewall para la intranet para comunicarse con RMS?](#bkmk_23)
-   [¿Cómo se inscriben los servidores subordinados en un clúster de sólo licencias? ¿Es necesario realizar alguna acción en los clientes para que tengan constancia de este clúster?](#bkmk_24)
-   [¿Cuál es la ventaja de usar un clúster de sólo licencias?](#bkmk_25)
-   [¿Qué debe hacerse para deshacer completamente una instalación de RMS?](#bkmk_26)
-   [Después de desinstalar el cliente de RMS mediante Agregar o quitar programas, ¿debo eliminar algún archivo más?](#bkmk_27)
-   [¿Funciona RMS con el sistema de archivos FAT?](#bkmk_28)
-   [¿Qué configuración típica de hardware se recomienda para el servidor de base de datos utilizado por RMS?](#bkmk_29)
-   [¿Cómo afecta el uso de RMS del catálogo global para la expansión de grupo al rendimiento del servidor de catálogo global?](#bkmk_30)
-   [¿Requiere RMS algún cambio de esquema en Active Directory?](#bkmk_31)
-   [¿Se replicará automáticamente el punto de conexión de servicio (SCP) entre los diferentes controladores de dominio en el dominio en el que está instalado el clúster de RMS?](#bkmk_32)
-   [Si los usuarios no poseen derechos administrativos en sus equipos, ¿cómo puede instalarse y configurarse el cliente de RMS?](#bkmk_33)
-   [¿Qué es la escalabilidad de RMS?](#bkmk_35)
-   [¿Acepta RMS módulos de seguridad de hardware (HSM) para proteger las claves de RMS en hardware?](#bkmk_36)

<span id="BKMK_20"></span>
#### Si las entidades principales de seguridad que se utilizan en RMS son miembros de la lista global de direcciones (GAL), ¿existe alguna dependencia en la versión de Exchange?

RMS depende de Active Directory pero no de Exchange. Sin embargo, Exchange 5.5 mantiene su propio directorio y no utiliza Active Directory. Asegúrese de que todos los objetos de grupo y de usuario de Active Directory tengan un atributo de correo electrónico válido que incluya un nombre de dominio completo. Esto se hace automáticamente si utiliza Exchange 2000 o posterior.

<span id="BKMK_21"></span>
#### ¿Qué papel tiene SQL Server en RMS?

RMS utiliza una base de datos para almacenar todos los datos de configuración del servicio, información sobre las entidades principales del sistema, datos de registro y consultas durante la expansión de Active Directory y listas de distribución. RMS se ha comprobado por completo con SQL Server 2000 y SQL Server 2005.

<span id="BKMK_22"></span>
#### ¿Debe estar unido el equipo de un usuario al mismo dominio que el servidor de RMS para utilizar RMS?

El equipo del usuario no tiene que ser miembro del mismo dominio que el clúster de RMS, pero debe ser capaz de encontrar un clúster de RMS. Para los equipos cliente, la forma más fácil de encontrar el clúster de RMS es mediante una consulta en Active Directory a través del punto de conexión de servicio (SCP). Sin embargo, también puede establecerse la configuración del Registro del cliente para encontrar el clúster de RMS sin usar una consulta de Active Directory. La configuración exacta del registro depende de la aplicación compatible con RMS.

<span id="BKMK_23"></span>
#### Si un cliente desea poner el servidor de RMS en una red perimetral, ¿qué puertos deben estar abiertos en el firewall para Internet y el firewall para la intranet para comunicarse con RMS?

Los usuarios internos necesitarán tener acceso a los servidores de RMS que emiten certificados de cuenta de permisos (RAC) y licencias de uso. De forma predeterminada, el servidor de RMS busca en HTTP (puerto TCP 80) o HTTPS (puerto TCP 443), en función de si el servidor está configurado para utilizar SSL, así que estos puertos deben estar abiertos en el cortafuegos para Internet. Necesitará abrir los puertos adicionales utilizados por servidores miembros en un dominio cortafuegos para intranet.

<span id="BKMK_24"></span>
#### ¿Cómo se inscriben los servidores subordinados en un clúster de sólo licencias? ¿Es necesario realizar alguna acción en los clientes para que tengan constancia de este clúster?

Cuando se crea el primer servidor de RMS en el clúster raíz, recibe un certificado emisor de licencias de servidor del servicio de inscripción de Microsoft. Cuando otro servidor de RMS está instalado y aprovisionado, puede unirlo al clúster raíz o inscribirlo como servidor de un clúster de sólo licencias subordinado. Si decide inscribirlo como servidor en un clúster de sólo licencias subordinado, envía una solicitud de inscripción al clúster raíz de RMS. Las aplicaciones habilitadas para RMS especifican dónde busca el clúster de sólo licencias la aplicación cliente. Office 2003 es un ejemplo de aplicación habilitada para RMS que, de forma predeterminada, busca en el clúster raíz. Puede reemplazarse este comportamiento con una opción del Registro para que la aplicación busque un nuevo clúster de sólo licencias subordinado.

<span id="BKMK_25"></span>
#### ¿Cuál es la ventaja de usar un clúster de sólo licencias subordinado?

Una ventaja consiste en aislar distintos departamentos de una organización. Si no se ha establecido un dominio de publicación de confianza entre clústeres de RMS, sólo pueden obtener acceso al contenido los usuarios que tengan acceso a un servidor de licencias en concreto. De esta forma, un departamento legal puede impedir que todos los otros lean su correo electrónico cifrado con RMS. Además, en el clúster de sólo licencias pueden establecerse distintas opciones, como plantillas de derechos, registro, pertenencia al grupo de superusuarios o directivas de exclusión.

<span id="BKMK_26"></span>
#### ¿Qué debe hacerse para deshacer completamente una instalación de RMS?

Para volver a la instalación anterior de RMS sin problemas, siga el procedimiento siguiente.

**Para volver a la instalación anterior de RMS**
1.  Quite el punto de conexión de servicio (SCP) del clúster de RMS con el sitio web de administración de RMS.

2.  En la página **Administración global**, haga clic en **Quitar RMS de este sitio Web** para anular los servicios en línea de RMS en el servidor. Deberá empezar anulando los servicios en línea de cualquier servidor subinscrito en clústeres de sólo licencias subordinados y, a continuación, anular los servicios en línea de los servidores de clúster raíz.

3.  En **Panel de control**, haga clic en **Agregar o quitar programas** y elimine **Servicios de Rights Management**.

4.  En el servidor de base de datos, elimine todas las bases de datos de RMS que queden.

5.  Elimine la cuenta de servicio de RMS de la lista de inicios de sesión autorizados de los servidores de base de datos y, a continuación, elimine la cuenta del propio Active Directory.

6.  Si los clientes de RMS ejecutan Windows XP y Windows 2000, quite el cliente de RMS de los equipos cliente.

| ![](images/Cc720274.Important(WS.10).gif)Importante                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Una vez completado este procedimiento, ya no puede abrir contenido protegido por derechos. Primero, retire RMS antes de volver a la instalación anterior de RMS si se usó RMS para proteger datos valiosos. |

<span id="BKMK_27"></span>
#### Después de desinstalar el cliente de RMS mediante Agregar o quitar programas, ¿debo eliminar algún archivo más?

Aunque no es necesario, puede eliminar la caja de seguridad de %systemroot%\\system32.

<span id="BKMK_28"></span>
#### ¿Funciona RMS con el sistema de archivos FAT?

Sí, RMS funciona en un equipo que utiliza FAT, aunque se recomienda el sistema de archivos NTFS.

<span id="BKMK_29"></span>
#### ¿Qué configuración típica de hardware se recomienda para el servidor de base de datos utilizado por RMS?

La base de datos de registro crecerá rápidamente, especialmente en entornos en los que se utilice mucho RMS. Si se está planteando usar SQL Server para el servidor de base de datos, debería considerar el uso de SQL Server 2000 Enterprise Edition o SQL Server 2005 Enterprise Edition en Windows 2000 Advanced Server o Windows Server 2003, Enterprise Edition, configurado en un clúster en una configuración con conmutación activa. En este caso, las configuraciones recomendadas son discos de registro RAID-1 y discos de datos RAID-5 y al menos 512 MB de RAM. La CPU mínima recomendada para esta configuración es un Pentium III a 1,4 GHz. En servidores de base de datos dedicados, no son necesarias múltiples CPU.

<span id="BKMK_30"></span>
#### ¿Cómo afecta el uso de RMS del catálogo global para la expansión de grupo al rendimiento del servidor de catálogo global?

El servidor de RMS almacenará todas las listas de expansión de grupo, de modo que no se coloque una gran carga en el servidor de catálogo global. La actualización frecuente de pertenencia a grupos aumenta la confianza en el servidor de catálogo global, aunque el tiempo de espera para adquirir nuevas listas de grupo se puede configurar a través del registro. La expansión frecuente de grupos grandes degrada el rendimiento. Para obtener más información, vea "Cambio de la configuración de caché de Active Directory" en "RMS: Operaciones" en esta recopilación de documentación.

<span id="BKMK_31"></span>
#### ¿Requiere RMS algún cambio de esquema en Active Directory?

Para que RMS pueda expandir más allá de los límites del bosque la pertenencia a grupos que se especifica en la licencia de publicación, debe existir un objeto de contacto en el bosque de Active Directory local que represente al grupo que se encuentra en el bosque remoto. RMS puede consultar los atributos del objeto de contacto y ver que este objeto representa a un grupo que se halla en un bosque diferente.

Para ello, Active Directory requiere el atributo de esquema msExchOriginatingForest de Exchange Server 2003 o posterior. Este atributo está instalado de forma predeterminada en el esquema de Active Directory si tiene un servidor que ejecute Exchange Server 2003 en el bosque. Debe tener este atributo en el bosque de todos los esquemas de Active Directory que participarán en RMS. Si no usa Exchange Server 2003, puede instalar el esquema por separado en la estructura de Active Directory si usa el kit de herramientas de administración de RMS.

<span id="BKMK_32"></span>
#### ¿Se replicará automáticamente el punto de conexión de servicio (SCP) entre los diferentes controladores de dominio en el dominio en el que está instalado el servidor de RMS?

Después de establecer los servicios en línea del primer servidor de RMS en un bosque, debe registrarse en Active Directory utilizando una cuenta de dominio que tenga suficientes permisos para crear un objeto contenedor bajo el contenedor de servicios en el contenedor de configuración de Active Directory. El grupo de seguridad integrado, Administradores de organización, es un ejemplo de cuenta con los privilegios necesarios. Esto crea el SCP. Dado que esto se produce en el contenedor de servicios, Active Directory replica la información en todos los controladores de dominio del bosque.

<span id="BKMK_33"></span>
#### Si los usuarios no poseen derechos administrativos en sus equipos, ¿cómo puede instalarse y configurarse el cliente de RMS?

El cliente de RMS es un archivo de Windows Installer, y puede ser distribuido utilizando una infraestructura de distribución de software como Systems Management Server 2003. También es posible distribuir el cliente de RMS utilizando un objeto de directiva de grupo (GPO) que utilice una cuenta de servicio con derechos administrativos. Si el cliente de RMS ejecuta Windows Vista, ya no se requiere una instalación de cliente de RMS por separado, ya que está integrado en el sistema operativo.

<span id="BKMK_35"></span>
#### ¿Qué es la escalabilidad de RMS?

RMS es un servicio Web independiente, que puede ser agrupado y se le puede realizar el equilibrio de carga como cualquier otro sitio o servicio Web. El rendimiento de RMS depende principalmente de la disponibilidad de procesador, de modo que añadir procesadores puede mejorar el rendimiento.

<span id="BKMK_36"></span>
#### ¿Acepta RMS módulos de seguridad de hardware (HSM) para proteger las claves de RMS en hardware?

Sí, RMS funciona con HSM compatibles con CAPI, como el HSM nCipher.
