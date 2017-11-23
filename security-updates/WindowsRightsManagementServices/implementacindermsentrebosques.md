---
TOCTitle: Implementación de RMS entre bosques
Title: Implementación de RMS entre bosques
ms:assetid: 'd531dfdc-efff-4eb0-8d99-f1fd19d7a963'
ms:contentKeyID: 18127978
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747685(v=WS.10)'
---

Implementación de RMS entre bosques
===================================

Si su organización incluye múltiples bosques de Active Directory y desea habilitar el uso de RMS en la organización, asegúrese de que ha configurado la red de modo que RMS pueda identificar y autenticar cuentas de usuario y grupos de distribución que residan en distintos bosques.

RMS utiliza Active Directory para identificar usuarios y grupos de distribución. Cuando la implementación de Active Directory de una organización incluye múltiples bosques, RMS utiliza objetos de contacto para obtener las identidades de los usuarios y de los grupos que forman parte de un bosque diferente del servidor de RMS. Para cumplirlo son necesarias tres condiciones:

1.  Los servidores de certificación de RMS deben existir en el otro bosque, y los objetos de contacto deben estar definidos para cada grupo remoto.
2.  Las extensiones de esquema deben existir en los bosques que contienen objetos de contacto para que puedan referirse a los bosques que contienen los objetos.
3.  Los atributos de los objetos de contactos deben sincronizarse para referirse a los bosques que contienen el objeto.

Por ejemplo, supongamos que los grupos están definidos y administrados en un bosque y los usuarios están definidos y administrados en otro bosque. Un usuario desea asignar permisos a contenido que se basa en la pertenencia a un determinado grupo. En este escenario, *RMS\_Server\_U* es el servidor del bosque que contiene las cuentas de usuario y *RMS\_Server\_G* es el servidor del bosque que contiene las cuentas de grupo. Se ha establecido un dominio de cuenta de confianza entre estos dos servidores de RMS. Para que *RMS\_Server\_U* expanda la pertenencia a grupos especificada en la licencia de publicación a través de límites de bosques, debe existir un objeto de contacto en el bosque local de Active Directory que represente el grupo que está en el bosque remoto. RMS puede examinar los atributos del objeto de contacto y descubrir que este objeto representa un grupo que está en un bosque diferente; entonces puede buscar un servidor de RMS de ese bosque y determinar si existe una relación de confianza entre los dos servidores de RMS. Cuando *RMS\_Server\_U* busca en Active Directory el grupo especificado en la licencia de publicación, el objeto de contacto identificará que el grupo pertenece a otro bosque. Cuando *RMS\_Server\_U* reenvía la petición al servidor de RMS que aparece en el punto de conexión de servicio (SCP) de ese dominio. El SCP identifica a *RMS\_Server\_G* como el servidor de certificación de RMS para el dominio. *RMS\_Server\_U* buscará *RMS\_Server\_G* para obtener la pertenencia del grupo.

El atributo que busca RMS para esta información es **msExchOriginatingForest**. Este atributo está instalado de forma predeterminada en el esquema de Active Directory si tiene Exchange Server 2003 instalado en el bosque. Debe tener este atributo en el bosque de todos los esquemas de Active Directory que participarán en RMS. Si no utiliza Exchange Server 2003, puede agregar estas extensiones de esquema descargando el kit de herramientas administrativas de RMS. El kit de herramientas contiene un archivo de esquema e instrucciones sobre cómo agregarlo a Active Directory.

Estos atributos deben estar sincronizados para que el objeto de contacto se refiera al objeto en los otros bosques. Una vez agregado el atributo al esquema de Active Directory, debe configurar su valor para que sea el nombre de dominio completo (FQDN) del bosque en el que reside el grupo; por ejemplo, corp.fabrikam.com.

Puede hacerlo utilizando Microsoft Identity Integration Server (MIIS) 2003 o Identity Integration Feature Pack (IIFP) y el agente de administración de la lista global de direcciones de Active Directory (GAL).

Debe habilitar el servidor de RMS local para tener suficientes privilegios para realizar búsquedas en el Active Directory remoto y para llamar a las interfaces de .NET Remoting que se encuentran en la instalación remota de RMS.

Para permitir la expansión de grupos entre bosques, la cuenta que se utiliza para la cuenta de servicio de RMS de cada bosque debe tener también permisos de lectura y ejecución para Active Directory. RMS concede automáticamente acceso de lectura para Active Directory a todos los usuarios autenticados que tengan credenciales de dominio. Para aumentar la seguridad, puede eliminar este acceso de la lista de control de acceso discrecional (DACL) y reemplazarlo con cuentas de servicio individuales de los distintos bosques.

Dependiendo de la existencia o no de relaciones de confianza de Active Directory entre el bosque local y el remoto, los permisos necesarios para la cuenta de servicio de RMS pueden variar. La siguiente lista identifica los modelos de confianza y los permisos que se requieren:

-   **Existe confianza bidireccional**. El bosque de RMS local confía y disfruta de la confianza del bosque donde se originó el grupo. La cuenta de servicio de RMS para el servidor de RMS de cada bosque puede ser cualquier cuenta de dominio válida que esté en el bosque. Asegúrese de que agrega la cuenta de servicio local de RMS a la DACL de la carpeta \\Inetpub\\wwwroot\\\_wmcs\\drmRemote de todos los servidores de RMS que están en el bosque donde se originó el grupo.
-   **Existe confianza unidireccional**. El bosque de RMS local confía en el bosque donde se originó el grupo, pero éste no confía en el primero. La cuenta de servicio de RMS para todos los servidores de RMS de la organización debe ser de una cuenta de dominio válida que está en el bosque de confianza. Agregue esta cuenta a la DACL de la carpeta \\Inetpub\\wwwroot\\\_wmcs\\drmRemote de todos los servidores de RMS que están en el bosque donde se originó el grupo.
-   **No existe confianza**. Los bosques que se hallan en la organización no pueden autenticar usuarios y grupos de otros bosques. Se recomienda que no utilice la expansión de grupo entre bosques si los bosques participantes no tienen una relación de confianza. Sin embargo, si tiene que hacerlo debido a requisitos operativos, puede habilitar este escenario configurando la cuenta de servicio de RMS como cuenta de dominio válida en ambos bosques, y utilizando en ambos el mismo nombre de usuario y la misma contraseña. Además, debe crearse una cuenta de equipo local en cada servidor de RMS de solicitudes de cliente, también con el mismo nombre de usuario y la misma contraseña que las cuentas de dominio que se utilizan para la cuenta de servicio de RMS en ambos bosques. Esto concede automáticamente al servicio local los permisos suficientes para autenticarse en Active Directory remoto y en el servidor de RMS remoto.

Uso de directivas de confianza de RMS
-------------------------------------

Cuando se implementa RMS en una organización con múltiples bosques, debe implementarse un servidor de certificación de RMS en todos los bosques que contienen cuentas de usuario que participarán en el sistema RMS. Si desea que los usuarios de distintos bosques puedan compartir contenido protegido con RMS, debe configurar las directivas de confianza de RMS para que se pueda confiar en los certificados y licencias generados por el otro servidor de RMS. Hay dos directivas de confianzas que pueden utilizarse con RMS, dominios de usuarios de confianza y dominios de publicación de confianza. Los dominios de usuarios de confianza permiten a un servidor de RMS confiar en los certificados de cuenta de permisos (RAC) generados por otro servidor de certificación de RMS y emitir licencias de uso para los usuarios con certificados RAC del otro servidor. Los dominios de publicación de confianza permiten a un servidor de RMS generar licencias de uso basadas en licencias de publicación que especifican el otro servidor de licencias.

A continuación se muestran algunas opciones para utilizar directivas de confianza para permitir múltiples bosques:

-   Un clúster de certificación de RMS en cada bosque con un único clúster de licencias compartido por todos los usuarios. El clúster de licencias de RMS estaría configurado con un dominio de usuario de confianza que incluyera todos los clústeres de certificación de RMS. Los clientes de RMS estarían configurados utilizando una clave de registro para conectarse al clúster de licencias para obtener licencias de uso.
-   Un clúster de licencias y de certificación de RMS dentro de cada bosque con un dominio de usuario de confianza configurado en todos los clústeres para confiar en los servidores de RMS en los otros bosques. Cada uno de los usuarios utilizaría el servidor de RMS de su bosque para obtener licencias de uso y podría descubrir su servidor de licencias a través del punto de conexión de servicio de Active Directory.
-   Si los usuarios del contenido protegido con RMS forman parte de un bosque que no tiene acceso al bosque desde el que se publicó el contenido, puede establecerse un dominio de publicación de confianza para que el contenido pueda obtener licencia y utilizarse. Los dominios de publicación de confianza requieren que se importe la clave privada del servidor de RMS utilizado para publicar el contenido.

Para obtener más información sobre la configuración de la directiva de confianza, vea "Administración de la confianza y directivas de confianza" en "Operación de un servidor de RMS", en esta recopilación de documentación.
