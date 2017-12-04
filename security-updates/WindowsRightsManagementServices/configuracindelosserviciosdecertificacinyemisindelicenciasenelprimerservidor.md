---
TOCTitle: Configuración de los servicios de certificación y emisión de licencias en el primer servidor
Title: Configuración de los servicios de certificación y emisión de licencias en el primer servidor
ms:assetid: 'cce29a2f-984f-48ed-9187-0eb68286ec5b'
ms:contentKeyID: 18127961
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747756(v=WS.10)'
---

Configuración de los servicios de certificación y emisión de licencias en el primer servidor
============================================================================================

Para configurar RMS en un bosque, primero debe instalar RMS y establecer los servicios en línea. El primer servidor que se implementa es el servidor de certificación raíz. Este servidor proporciona compatibilidad de certificación y de licencia, y puede utilizarse como único servidor en una configuración de un solo servidor, o como servidor inicial de un clúster de certificación raíz.

Funciones, permisos y derechos necesarios para la instalación y el establecimiento de servicios en línea de servidores de RMS adicionales
-----------------------------------------------------------------------------------------------------------------------------------------

Para instalar RMS, debe iniciar la sesión en una cuenta con privilegios de administrador local. Además, debe iniciar la sesión en un dominio con una cuenta de dominio válida para que Active Directory pueda autenticar en RMS. Si está implementando RMS en un entorno en el que la infraestructura de Active Directory utiliza el modo nativo de Windows 2000, es posible que RMS no pueda leer el atributo memberOf de los objetos de Active Directory cuando intente ampliar la pertenencia a grupos. Para que RMS pueda leer el atributo memberOf, la cuenta de servicio de RMS debe ser una cuenta de dominio miembro del grupo de acceso compatible con versiones anteriores de Windows 2000 en el bosque. Si ha implementado grupos con pertenencia oculta, deberá configurar la cuenta de servicio de RMS con permisos que le permitan leer la pertenencia oculta.

> [!NOTE]
> La cuenta de servicio de RMS no puede ser la misma cuenta de dominio que se utilizó para instalar RMS. 

Instalación y establecimiento de servicios en línea del servidor inicial
------------------------------------------------------------------------

La implementación del servidor de RMS consiste en dos pasos. En primer lugar, debe instalarse el software del servidor de RMS junto con todo el software compatible como IIS, los servicios de Message Queue Server y ASP.NET. Para obtener más información acerca de la instalación, vea "Para instalar RMS con Service Pack 1" en "Operación de un servidor de RMS", en esta recopilación de documentación.

> [!NOTE]
> También puede instalarse RMS desde el símbolo del sistema. Para obtener más información, vea “Instalación de RMS desde el símbolo del sistema” en “Operación de un servidor de RMS”, en esta recopilación de documentación. 

Después de instalar RMS en un servidor, debe establecer los servicios en línea de RMS para utilizarlos en un único sitio Web del servidor. Cuando se establecen los servicios en línea en este sitio Web, se modifican muchas de las configuraciones del sitio y se agregan directorios virtuales. Para obtener más información acerca de estos cambios, vea “Compatibilidad con los Servicios de Internet Information Server para RMS” en “Referencia técnica de RMS”, en esta recopilación de documentación.

Puede utilizar el sitio Web predeterminado de IIS o crear uno nuevo. Para establecer los servicios en línea de RMS en un sitio diferente del sitio Web predeterminado, debe crear el sitio Web antes de empezar este proceso de establecimiento de servicios en línea. Si utiliza el sitio Web predeterminado para otros propósitos, debe crear un sitio nuevo para RMS de modo que se mantenga la configuración predeterminada para el sitio Web predeterminado.

Al hacer clic en **Administración de Windows RMS** en el menú **Inicio**, aparece la página **Administración global**. En esta página, puede empezar el proceso de establecimiento de servicios en línea en un sitio Web. Para establecer servicios en línea en el primer servidor de RMS, debe proporcionar la información siguiente:

-   Especifique el nombre de la base de datos que se utilizará para las bases de datos de configuración, registro y servicios de directorio de RMS.  

    Si el nombre de su instancia de SQL Server difiere del nombre del servidor local, debe configurarla como una instancia de SQL Server remota, incluso si todo está instalado en un único servidor.  

    Durante el establecimiento de servicios en línea, la cuenta de usuario que haya iniciado sesión actualmente debe tener permiso para crear bases de datos en el servidor de base de datos.

-   Especifique la cuenta que se utilizará para la cuenta de servicio de RMS. Para una configuración local, puede utilizar la cuenta del sistema local, aunque no es recomendable por los problemas de seguridad inherentes que conlleva ejecutar un servicio con los privilegios de esta cuenta.  

    Para una instalación que incluye una instancia de SQL Server remota o más de un servidor de RMS, debe especificar una cuenta de dominio. La cuenta de dominio que utilice debe tener privilegios de búsqueda en Active Directory y se usará para crear el grupo de aplicaciones de IIS con el que se ejecuta la consola de administración. Si no está actualizando ni utilizando una base de datos existente, la cuenta de servicio de RMS requiere privilegios de creación de bases de datos. Si está utilizando bases de datos existentes, la cuenta necesita permisos de lectura y escritura para cada una de las bases de datos de RMS.

-   Especifique la dirección URL que se utilizará para obtener acceso a este sitio Web. El valor predeterminado es el nombre del sitio donde vaya a establecer los servicios en línea (como el sitio Web predeterminado, si va a establecer los servicios en línea en un servidor con una instalación predeterminada de IIS). Puede especificar una dirección URL personalizada para obtener acceso a un sitio Web diferente, por ejemplo, para admitir una dirección URL de equilibrio de carga o permitir el acceso tanto a Internet como a una intranet. Debe comprobar que la dirección URL personalizada funciona, y debe añadir el nombre del sitio en DNS para asegurarse de que las páginas de **administración global** y de **establecimiento de servicios en línea** encuentren las raíces virtuales. Si esta dirección URL se va a utilizar para una implementación habilitada para Internet, asegúrese de que la nueva dirección URL esté disponible desde Internet y la red corporativa.

-   Seleccione el mecanismo que se utilizará para proteger la clave privada de la instalación raíz que se utiliza para la inscripción. De forma predeterminada, se utiliza cifrado de software y se almacena la clave privada cifrada en la base de datos de configuración de RMS. Si utiliza la configuración predeterminada, debe proporcionar una contraseña segura para cifrar el valor que se encuentra en la base de datos.  

    Sin embargo, si ha instalado y configurado un módulo de seguridad de hardware (HSM) en el equipo, también puede seleccionar un proveedor de servicios de cifrado (CSP) para utilizarlo con el módulo de seguridad de hardware y almacenar las claves privadas en hardware, como por ejemplo en una tarjeta inteligente. RMS necesita un proveedor RSA completo; en la lista de CSP sólo se incluyen estos proveedores. Se recomienda encarecidamente utilizar un HSM para proteger la clave privada de RMS.  

    Si utiliza un proveedor de servicios de cifrado (CSP) de software para proteger la clave privada de RMS con una contraseña, debe guardarla en un archivo seguro para futura referencia. También debe guardar una copia de seguridad de la base de datos de configuración con la contraseña. Al hacerlo, puede restaurar RMS si se daña la base de datos de SQL. Si cambia la contraseña por cualquier razón, realice una nueva copia de seguridad de la base de datos de configuración que almacena la clave privada protegida con dicha contraseña y guarde ambas en un archivo seguro. Para obtener más información acerca de cómo realizar copias de seguridad y restaurar la base de datos de configuración, vea “Copia de seguridad y restauración del sistema para RMS” en “Planeamiento de una implementación de RMS”, en esta recopilación de documentación.

-   Especifique el nombre que se utilizará en el certificado emisor de licencias de servidor. De forma predeterminada, es el nombre del servidor.

-   Especifique el servidor proxy (incluidos la dirección y el puerto) que se utilizará para conectarse a Internet, si es necesario.

-   Especifique una dirección de correo electrónico que puedan utilizar otros administradores de RMS para ponerse en contacto con un administrador si se producen problemas cuando el administrador intenta subinscribirse en un servidor de licencias. Después de establecer los servicios en línea en la instalación raíz, puede cambiar la dirección.

-   Seleccione un método de revocación de certificado emisor de licencias de servidor para controlar quién puede revocar el certificado emisor de licencias de servidor de la instalación raíz, aparte del servicio de inscripción de Microsoft. Para usar revocaciones de terceros, debe especificar la ruta de acceso y el nombre del archivo que contiene la clave pública de la entidad.

Si ha seleccionado la opción de inscripción en línea, al hacer clic en **Enviar** en la página de **establecimiento de servicios en línea** (después de configurar todas las opciones adecuadas), RMS genera un par de claves y envía la clave pública al servicio de inscripción de Microsoft. Si recibe mensajes de error, no cierre la página donde aparezcan. Después de resolver los errores, abra una ventana de símbolo de sistema y escriba `IISReset` para detener y reiniciar IIS, vuelva a la pantalla anterior, vuelva a escribir la información en la pantalla de establecimiento de servicios en línea y vuelva a hacer clic en **Enviar**. El servicio de inscripción de Microsoft crea un certificado emisor de licencias de servidor y lo devuelve a la base de datos de configuración en pocos minutos. Dado que es el primer servidor en el dominio en el que está instalado RMS, este paso constituye el proceso de inscripción del servidor de certificación raíz.

Si ha seleccionado la opción de inscripción sin conexión, inscribirá el servidor manualmente con el servicio de inscripción de Microsoft una vez que haya completado el proceso de establecimiento de servicios en línea. Hay que completar el proceso de inscripción para poder utilizar el servidor. Para obtener más información, vea “Para inscribir manualmente un servidor de certificación raíz” en “Operación de un servidor de RMS”, en esta recopilación de documentación.

Cuando termine de establecer servicios en línea e inscribir un servidor, los vínculos de la página **Administración global** cambian. El vínculo **Establecer los servicios en línea de RMS en este sitio Web** cambia a **Administrar RMS en este sitio Web**, el vínculo **Agregar este servidor a un clúster** se reemplaza por el vínculo **Cambiar la cuenta de servicio de RMS**, y se agrega el vínculo **Quitar RMS de este sitio Web** a la página.

Este servidor inicial establece la instalación raíz de RMS. La instalación raíz puede componerse de un único servidor o de un clúster. Después de finalizar la instalación del servidor inicial y el establecimiento de los servicios en línea en él, puede configurar servidores adicionales para proporcionar redundancia y compatibilidad con equilibrio de carga para los servicios de certificación y emisión de licencias.

Cuando haya completado la configuración, debe registrar el punto de conexión de servicio del clúster de certificación raíz en Active Directory para que los clientes compatibles con RMS puedan detectar el servicio. Para obtener más información, vea “Registro del punto de conexión de servicio” en “Operación de un servidor de RMS”, en esta recopilación de documentación. Si el punto de conexión de servicio no está registrado, su cliente de RMS no podrá utilizarse con RMS.

> [!IMPORTANT]
> Debe instalar y establecer los servicios en línea de RMS completamente en el primer servidor antes de instalar RMS en cualquier otro servidor. RMS admite la protección de contenido a grupos de Active Directory cuyos miembros abarquen distintos bosques. Si su organización no tiene varios bosques o grupos que abarquen varios bosques, puede optimizar el rendimiento del proceso de emisión de licencias de uso del servidor de RMS modificando la directiva de clúster **MaxCrossForestCalls** en la base de datos de configuración de RMS. Esta directiva especifica el número máximo de veces que los miembros de un grupo pueden cruzar los límites de los bosques. El valor predeterminado es 10. Para cambiar ese valor por 0, utilice el siguiente comando SQL: ```update DRMS_ClusterPolicies set PolicyData=0 donde PolicyName='MaxCrossForestCalls'``` 

Los temas siguientes describen los pasos necesarios para completar las tareas que están disponibles en la página Administración global de RMS:

-   Para obtener información acerca de cómo utilizar el asistente de instalación para instalar el servidor inicial, vea “Para instalar RMS con Service Pack 1” en “Operación de un servidor de RMS”, en esta recopilación de documentación.

-   Para obtener información acerca de cómo establecer los servicios en línea en el servidor inicial, vea “Para establecer los servicios en línea en el primer servidor de certificación raíz” en “Operación de un servidor de RMS”, en esta recopilación de documentación.

-   Para obtener información sobre cómo agregar servidores a la instalación raíz para crear un clúster, vea “[Adición de servidores para permitir la certificación y emisión de licencias](https://technet.microsoft.com/089ceb62-2a96-444f-ab42-1d5deaabd0c3)”, más adelante en este tema.
