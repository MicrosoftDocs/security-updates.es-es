---
TOCTitle: Procedimientos recomendados de seguridad con RMS
Title: Procedimientos recomendados de seguridad con RMS
ms:assetid: '762037ce-9bee-4d89-bb14-7dd1c004dca3'
ms:contentKeyID: 18127818
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747564(v=WS.10)'
---

Procedimientos recomendados de seguridad con RMS
================================================

Los siguientes procedimientos recomendados proporcionan instrucciones que pueden ayudarle a administrar efectivamente la seguridad con Rights Management Services (RMS). Hallará información general acerca de procedimientos recomendados de seguridad en el sitio Web de Microsoft ([http://go.microsoft.com/fwlink/?LinkId=49428](http://go.microsoft.com/fwlink/?linkid=49428)).

-   **Utilice la autenticación de certificado SSL en los servicios Web de RMS**. De forma predeterminada, las solicitudes del cliente de RMS al clúster de RMS no se cifran. Al instalar un certificado de Capa de sockets seguros (SSL) y requerir autenticación SSL en los directorios virtuales RMS de todos los servidores de RMS del clúster, las solicitudes de certificación y licencia se cifran como si se enviarán por la red. Para seguridad adicional, puede habilitar la autenticación de tarjeta inteligente para los servicios Web de RMS.

-   **Utilizar un CSP basado en hardware para proteger la clave privada de RMS**. Al instalar RMS, la protección de clave predeterminada para claves privadas del clúster de RMS es un proveedor de servicios de cifrado (CSP) basado en software que cifra la clave del clúster de RMS y la almacena en la base de datos de configuración de RMS. Para seguridad adicional, se puede utilizar un CSP basado en hardware o un módulo de seguridad de hardware. Este método de protección de claves almacena la clave en una tarjeta inteligente que se adjunta a los servidores de RMS. La ventaja frente a un CSP basado en hardware consiste en que la clave privada de RMS no se almacena en el equipo. Pida al proveedor de hardware si tiene un CSP basado en hardware que se haya probado para usar con RMS.

-   **Proteger el grupo de superusuarios de RMS**. El grupo de superusuarios de RMS tiene control total sobre todo el contenido protegido por derechos y sólo se debe habilitar y usar cuando sea necesario. Por tanto, se debe utilizar un grupo restringido de Active Directory® para controlar la pertenencia al grupo de superusuarios de RMS.

-   **Usar una cuenta de dominio para la cuenta de servicio de RMS con privilegios estándar**. Una cuenta de dominio que esté en el grupo de seguridad Usuarios del dominio de Active Directory se debe usar para la cuenta de servicio de RMS. No se deben conceder permisos adicionales para esta cuenta.

-   **Proteger el atributo de Active Directory de la dirección de correo electrónico**. Las aplicaciones de Microsoft® Office habilitadas para RMS usan el correo electrónico y los atributos proxyaddresses almacenados en Active Directory como la identidad exclusiva del usuario de RMS para certificar y conceder licencia del contenido protegido por derechos. Es muy importante limitar los permisos de estos atributos en Active Directory a administradores de confianza. Además, se debe aplicar una directiva de seguridad de información en la organización que prohíba la capacidad de reciclar una dirección de correo electrónico para otro usuario.

    > [!NOTE]
    > Una alternativa para evitar este problema consiste en asignar permisos a grupos en lugar de empleados individuales en las plantillas de directiva de permisos. Si la pertenencia a grupos está determinada cuando se solicita una licencia, la directiva de derechos refleja la pertenencia a grupos actual. También puede mitigar el problema de las direcciones de correo electrónico recicladas si usa aplicaciones habilitadas para RMS que publican identificadores de seguridad (SID) en vez direcciones de correo electrónico. 

-   **Mejorar las ACL en las canalizaciones de RMS.** Las listas de control de acceso (ACL) en las canalizaciones del directorio virtual de IIS de RMS son restrictivas de forma predeterminada. Sin embargo, para obtener más control los usuarios que pueden utilizar RMS, puede limitar las canalizaciones de certificación y publicación de RMS a grupos de seguridad de Active Directory específicos, en lugar de utilizar el grupo de seguridad Usuarios de dominio predeterminado.

-   **Desactivar la autenticación anónima en la canalización de licencias de RMS.** Si su topología de RMS no requiere usuarios externos, como los que inician sesión mediante Windows Live™ ID, se debe desactivar la autenticación anónima en la canalización de licencias de RMS.

-   **Minimizar el número de servicios en todos los servidores de RMS.** Al igual que en todas las estrategias de defensa en profundidad para asegurar servidores, se deben deshabilitar todos los servicios no necesarios de todos los servidores de RMS individuales en cada clúster de RMS. En un entorno de RMS, RMS y los componentes necesarios deben ser los únicos servicios que se ejecuten en los servidores del clúster de RMS.

-   **Utilizar un firewall de nivel de aplicación cuando utilice RMS en una extranet.** Cuando se utiliza RMS en una extranet, se debe usar un firewall de nivel de aplicación. Un firewall de nivel de aplicación, como Microsoft Internet Security and Acceleration (ISA) Server, analiza las solicitudes de certificación y licencia enviadas al servidor de RMS terminando la conexión SSL en el firewall, analizando el tráfico y restableciendo a continuación una conexión independiente de forma interna.

-   **Desactivar el modo de autenticación de SQL Server en la base de datos de configuración de RMS**. Cuando Message Queue Server envía mensajes desde los servidores de clúster de RMS a la base de datos de registro, pasa las credenciales de la cuenta de servicio de RMS a la base de datos. En el modo de autenticación de SQL Server, las credenciales se pasan en texto no cifrado en la cadena de conexión. Debido a que RMS no utiliza el modo de autenticación de SQL, se debe desactivar y configurar SQL Server para que sólo admita las solicitudes de autenticación de Windows.

-   **Cifrar la comunicación entre los clústeres y las bases de datos de RMS.** Para evitar que usuarios mal intencionados capturen o modifiquen datos registrados, proteja las bases de datos de RMS configurando la Capa de sockets seguros (SSL) o el protocolo de seguridad de Internet (IPSec) para proporcionar canales cifrados. Para obtener más información acerca de cómo usar SSL para la comunicación segura con SQL Server, vea [http://go.microsoft.com/fwlink/?LinkID=99948](http://go.microsoft.com/fwlink/?linkid=99948.). Para obtener más información acerca de cómo usar IPsec para proporcionar comunicación segura entre dos servidores, vea [http://go.microsoft.com/fwlink/?LinkID=99950](http://go.microsoft.com/fwlink/?linkid=99950).

-   **Utilizar la firma LDAP para proteger las comunicaciones de red**. Las comunicaciones entre RMS y el catálogo global de Active Directory deben firmarse. El tráfico LDAP firmado garantiza que los datos empaquetados vienen de una fuente conocida y que no han sido alterados. Windows Server® 2003 permite la firma y cifrado LDAP de forma predeterminada. La firma LDAP también se admite en Windows 2000 Server con Service Pack 3 (SP3).

-   **Supervisar el tamaño de la cola de mensajes de registro**. Use el Monitor del sistema para supervisar regularmente el tamaño de la cola de mensajes de registro de salida. Si el tamaño de la cola crece notablemente, compruebe si el servicio de escucha de registro funciona correctamente. Si un usuario malintencionado hace que se detenga el servicio de escucha de registro, la cola de mensajes salientes de registro crecerá y acabará excediendo el espacio en disco del servidor de RMS. Si esto se produce, el servidor denegará las solicitudes. Para obtener más información acerca del servicio de escucha de registro, consulte "Servicio de escucha de registro de RMS" en "Referencia técnica de RMS", en esta recopilación de documentación.

-   **Habilitar la auditoría en el servidor de base de datos**. La auditoría de la actividad del servidor de bases de datos proporciona seguridad adicional para la instalación de RMS, porque realiza un seguimiento de la actividad y de los cambios que se realizan en las bases de datos.

-   **Supervisar el tráfico de red en los servidores de RMS**. Debe supervisar y administrar RMS en su organización del mismo modo que otros servicios Web. Los servidores de RMS pueden ser objetivo de ataques de denegación de servicio y se deben administrar adecuadamente.