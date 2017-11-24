---
TOCTitle: Protección de las bases de datos que utiliza RMS
Title: Protección de las bases de datos que utiliza RMS
ms:assetid: '65802f9a-81bc-4398-968a-00c9b1dca2fa'
ms:contentKeyID: 18127784
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720285(v=WS.10)'
---

Protección de las bases de datos que utiliza RMS
================================================

RMS crea y utiliza tres bases de datos que poseen diversos requisitos de seguridad, como se explica a continuación:

-   **Servicios de directorio**. Esta base de datos copia en la memoria caché los resultados de las consultas de pertenencia a grupos de Active Directory. Puesto que contiene únicamente información acerca Active Directory, no precisa de más seguridad que la que se configura automáticamente durante el establecimiento de los servicios en línea de RMS.

-   **Registro**. La información incluida en esta base de datos es más confidencial que la de la base de datos de servicios de directorio, ya que de revelarse, la privacidad del usuario puede verse afectada. Microsoft se ha esforzado especialmente en garantizar que no se registre información personal identificable (PII) y que toda la información que se registre en esta base de datos esté protegida con las medidas de seguridad adecuadas. No se precisan más modificaciones en la seguridad de esta base de datos, a no ser que se mueva a otro equipo que ejecute SQL Server. Si se mueve la base de datos a otro servidor, debe asegurarse de que se apliquen al nuevo entorno los mismos mecanismos de protección.

-   **Configuración**. Esta base de datos constituye el recurso más valioso e importante de la implementación de RMS, además de las claves privadas del servidor. Contiene información confidencial crucial que debe protegerse con cuidado. Contiene todos los certificados y claves, la clave privada cifrada del servidor (a no ser que utilizara el cifrado de hardware recomendado) y el algoritmo hash de la contraseña de la clave privada, además de información de configuración.

Cuando RMS crea la base de datos de configuración, establece permisos que restringen el acceso y contribuyen a garantizar la seguridad de la base de datos.

Aumento de la seguridad de las bases de datos
---------------------------------------------

Puede realizar los procedimientos siguientes adicionales para aumentar la seguridad global de las bases de datos ubicadas en su entorno de red y servidor:

-   Ejecute el servidor de base de datos en un equipo con Windows Server 2003. Este sistema operativo es más seguro, de forma predeterminada, que Windows 2000 Server. Aunque puede bloquear un equipo basado en Windows 2000 Server, puede ser un proceso prolongado y es posible que se cometan errores que permitan el acceso de usuarios malintencionados a su base de datos.

-   Restrinja el acceso físico al servidor de base de datos.

-   Asegúrese de que los permisos y las DACL de las bases de datos que se encuentren en archivos de base de datos limiten el acceso al personal autorizado. Las listas DACL y los permisos predeterminados que se configuran con RMS son seguros. Tenga cuidado cuando cambie cualquiera de las configuraciones predeterminadas.

-   No ejecute servicios innecesarios en el servidor de base de datos, como Servicios de Microsoft Internet Information Server (IIS), de Message Queue Server o de Terminal Server.

-   No ejecute ninguna base de datos en el servidor de base de datos a excepción de las de RMS.

Proteja las bases de datos de SQL Server mediante la configuración de SSL o la seguridad del protocolo Internet (IPSec) para proporcionar canales cifrados. El cifrado de las comunicaciones de bases de datos ayuda a impedir que usuarios maliciosos capturen o modifiquen los datos registrados.

Para obtener más información acerca de la configuración de SSL para SQL Server, consulte el sitio Web de MSDN ([http://go.microsoft.com/fwlink/?LinkID=17060](http://go.microsoft.com/fwlink/?linkid=17060)).

Para obtener más información acerca de la configuración de IPsec para SQL Server 2000, consulte el sitio Web de MSDN ([http://go.microsoft.com/fwlink/?LinkID=17061](http://go.microsoft.com/fwlink/?linkid=17061)).

Para obtener más información acerca de la protección de los sistemas operativos de la familia Microsoft Windows Server 2003, obtenga la "Guía de seguridad de Windows Server 2003" en el Centro de descarga Microsoft ([http://go.microsoft.com/fwlink/?LinkId=36719](http://go.microsoft.com/fwlink/?linkid=36719)).