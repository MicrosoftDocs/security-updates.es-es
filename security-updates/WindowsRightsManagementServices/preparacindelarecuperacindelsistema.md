---
TOCTitle: Preparación de la recuperación del sistema
Title: Preparación de la recuperación del sistema
ms:assetid: '885c047f-1e3b-4bf5-8248-3a4505759cbb'
ms:contentKeyID: 18127873
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747659(v=WS.10)'
---

Preparación de la recuperación del sistema
==========================================

Si se producen errores en alguno de los componentes del sistema RMS, incluidas las conexiones de Internet e intranet que utiliza el servidor de RMS, el servidor de certificación de RMS, los servidores de licencias subinscritos de RMS o los servidores de base de datos que alojan las bases de datos de configuración de RMS pueden producir una pérdida inesperada de servicio. Cuando se configure un sistema RMS, es importante tener en cuenta el posible impacto sobre los sistemas informáticos y los datos importantes, por si se produce una pérdida de servicio de RMS y debe prepararse para recuperar el componente de la forma más eficaz posible.

Un error en los servidores de base de datos que alojan las bases de datos de configuración de RMS podría impedir el acceso continúo a la información protegida con RMS. En esta sección se describen las consideraciones y los factores importantes de cara a preparar la recuperación del sistema para un sistema RMS, entre los que se incluyen:

-   [Conectividad a Internet](#bkmk_1)
-   [Conectividad de intranet](#bkmk_2)
-   [Servicios de certificación y de licencias](#bkmk_3)
-   [Servidores de base de datos](#bkmk_4)
-   [Active Directory](#bkmk_5)

Conectividad a Internet
-----------------------

Si utiliza la inscripción de servidor en línea, el servidor de RMS necesitará conectividad a Internet durante el establecimiento de servicios en línea para obtener un certificado emisor de licencias de servidor (SLC) y renovarlo una vez al año. Al cabo de un año, el servidor de certificación le notificará que debe renovar el certificado mediante el registro de sucesos en el registro de sucesos del sistema. Los sucesos se registran un mes antes de llegar a la fecha de caducidad de SLC (Id. de suceso 16), una semana antes de la fecha de caducidad de SLC (Id. de suceso 17) y cuando el SLC caduque (Id. de suceso 18). La página Web Administración global de RMS del sitio Web de administración de RMS también le avisará de que se acerca la fecha de caducidad de SLC. Si utiliza RMS Management Pack para Microsoft Operations Manager (MOM), los sucesos de caducidad desencadenarán una alerta. Si no está disponible la conexión a Internet en el servidor de RMS, no se podrá renovar el certificado emisor de licencias del servidor con el botón **Renovar** del sitio Web de administración de RMS y se deberá utilizar el proceso de inscripción en línea para solicitar un certificado actualizado.

Es aconsejable efectuar la renovación con tiempo antes de su fecha de caducidad, a fin de evitar complicaciones en el caso de que la conexión a Internet no esté disponible al caducar el certificado. El servidor de RMS no puede proporcionar servicios de RMS sin un SLC válido; es decir, los usuarios no podrán publicar información protegida con RMS ni obtener las licencias de uso ni los certificados de cuenta de permisos (RAC) necesarios para leer información protegida con RMS. Los usuarios que previamente hayan adquirido licencias de uso y RAC para partes del contenido protegido con RMS seguirán teniendo acceso a la información hasta que sus licencias de uso o RAC caduquen.

Conectividad de intranet
------------------------

RMS es una tecnología de cliente y servidor que depende de una infraestructura conectada. Sin una red de intranet operativa, los servidores de RMS no se pueden conectar a los servicios requeridos de una empresa ni a los usuarios para suministrar servicios. Sin conectividad a intranet, los usuarios no pueden obtener certificados de cuenta de permisos (RAC), certificados emisores de licencias de cliente (CLC), ni licencias de uso de los servidores de RMS.

Es aconsejable que las organizaciones tengan en cuenta el establecimiento de arquitecturas de enrutamiento redundantes y vínculos de conmutación por error desde los sitios remotos a los sitios del servidor de RMS.

Una vez que un usuario haya obtenido un CLC para su equipo, el usuario podrá publicar la información protegida con RMS sin conexión cuando no se pueda obtener acceso a un servidor de RMS. Algunas aplicaciones de correo electrónico compatibles con RMS se han configurado para descargar automáticamente licencias de uso para los mensajes de correo electrónico asociados protegidos con RMS al sincronizar un buzón, de manera que el usuario pueda leer los mensajes de correo electrónico protegidos con RMS, aunque la conexión a intranet ya no exista.

Servicios de certificación y de licencias
-----------------------------------------

El sistema RMS depende en buena medida de dos directorios virtuales de los Servicios de Internet Information Server (IIS) 6.0: los servicios de certificación y de licencias. Estos servicios permiten a los usuarios y sus equipos inscribirse en el entorno RMS y las aplicaciones compatibles con RMS para publicar información protegida con RMS y obtener acceso a ella. Si estos servicios dejaran de estar disponibles, se podría denegar el servicio a los usuarios hasta su restablecimiento.

Para prepararse para una posible pérdida de servicio, considere la creación de clústeres de servidor de certificación y servidor de licencias subinscrito de manera que el error de un nodo en un clúster no afecte a la disponibilidad del servicio.

Es aconsejable crear un exceso de capacidad en los clústeres para que los errores de un nodo no afecten al rendimiento general. Cuando instale el primer servidor de certificación y cada servidor de licencias subinscrito, o bien el primer servidor de licencias subinscrito en un clúster, registre meticulosamente las opciones de configuración y los datos especificados durante el establecimiento de servicios en línea.

Servidores de base de datos
---------------------------

Los componentes más importantes del sistema RMS son los servidores de bases de datos que guardan las bases de datos de configuración. Cada servidor de RMS o clúster de servidores utiliza bases de datos para almacenar información de configuración y de registro. La información de configuración es esencial para el funcionamiento de RMS. Estas bases de datos alojan el certificado emisor de licencias de servidor, las plantillas de directiva de RMS que se han generado y una lista de usuarios inscritos en el sistema RMS; en caso de que no se utilice un módulo de seguridad de hardware con el servidor de RMS, también contendrán las claves privadas y públicas del servidor de RMS. Mediante las copias de seguridad de las bases de datos de RMS, puede restablecer una instalación de RMS anterior en un servidor nuevo y volver a crear un sistema RMS. El impacto de la pérdida de una base de datos depende de la base de datos. En la lista siguiente se describe el impacto de un error en una base de datos:

-   **Base de datos de configuración** Si esta base de datos deja de estar disponible durante el funcionamiento del servidor de RMS, los servicios de RMS podrán continuar funcionando porque RMS copia localmente en la memoria caché la información necesaria. Sin embargo, si se produce un suceso que requiere que el servicio de RMS interactúe con la base de datos de configuración, como una inscripción de un nuevo usuario, el servicio de RMS detectará un error y el nuevo usuario no podrá trabajar con el contenido protegido con RMS. Si se produce una operación que obliga al servidor de RMS a descartar la información almacenada en la caché, como el reinicio del servicio de IIS o una actualización programada de la caché local, el servicio de RMS dejará de funcionar. El servidor de RMS no podrá volver al servicio normal hasta que la base de datos de configuración esté disponible.

    Si la base de datos de configuración se daña o deja de estar disponible, los servidores de RMS dejarán de funcionar.
    
-   **Base de datos de servicios de directorio**. Aloja información almacenada en la caché sobre nombres de grupo y sus detalles de pertenencia obtenidos de un servidor de catálogo global. Si la tabla no está disponible durante breves períodos de tiempo, no habrá una reducción apreciable en los servicios de RMS. Su objetivo principal es proporcionar cargas de servicio reducidas y redundancia para el servidor de catálogo global.
-   **Base de datos de registro**. Si se ha habilitado el registro en el servidor de RMS, se utilizará esta base de datos para almacenar este registro. Si la base de datos no está disponible, las entradas de registros se acumularán en el servicio de Message Queue Server (también conocido como MSMQ) del servidor de RMS, y se utilizará todo el espacio en disco disponible a menos que se haya configurado para que no sea así.

Es aconsejable agrupar en clústeres los servidores de base de datos para ofrecer conmutación activa y recuperación de datos en caso de error. Asimismo, se debe hacer una copia de seguridad regularmente de las bases de datos para los clústeres y servidores de certificación de RMS, así como los clústeres y servidores licencias.

También es aconsejable utilizar el transvase de registros de transacciones para tener preparada una base de datos de seguridad. Aunque para esta práctica puede ser necesario hardware adicional, permite a las organizaciones recuperar las bases de datos más rápidamente. Microsoft IT ha implementado este método para la recuperación de la base de datos de configuración de RMS. Para ello, seleccione el nombre de SQL virtual durante el establecimiento de servicios en línea de RMS. El nombre de SQL virtual permite realizar la asignación a un nombre de SQL real mediante el servicio de nombres de dominio (DNS). En caso de que SQL Server deje de funcionar, podrá cambiar fácilmente al SQL Server de copia de seguridad modificando la asignación de nombres de DNS del servidor original por el del servidor de copia de seguridad. Para obtener más información acerca de la implementación interna de esta solución en Microsoft, vea el caso práctico de Microsoft Corporation en el [sitio Web de Microsoft](http://go.microsoft.com/fwlink/?linkid=42070) (http://go.microsoft.com/fwlink/?LinkId=42070).

Active Directory
----------------

RMS depende de Active Directory para dos importantes servicios: la autenticación del usuario y el servicio de catálogo global. En caso de que Active Directory no esté disponible, no se podrá realizar la autenticación de los usuarios, y tanto éstos como sus equipos no podrán inscribirse en el sistema RMS. Para obtener un RAC se necesita canalización de certificación; esta canalización necesita autenticación. Una vez que un usuario obtenga un RAC, éste podrá obtener licencias de uso sin más autenticaciones, porque de forma predeterminada la canalización de licencias es anónima.

Puesto que las entidades empresariales pueden utilizar la pertenencia a grupos en Active Directory para indicar quién tiene acceso a la información protegida con RMS, la pérdida de Active Directory impide a los usuarios adquirir licencias de uso. De forma predeterminada, la información de pertenencias a grupos se almacena en caché en el servidor de RMS durante 15 minutos, lo cual permite tolerar un pérdida temporal del servicio de catálogo global. Si desea aumentar o reducir el tiempo entre actualizaciones de la caché, puede modificar la clave del registro que controla el tiempo de validez. Para obtener más información, vea "Modificación de la configuración de caché de Active Directory" en "Operación de un servidor de RMS", en esta recopilación de documentación.