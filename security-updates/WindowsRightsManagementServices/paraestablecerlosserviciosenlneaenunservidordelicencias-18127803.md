---
TOCTitle: Para establecer los servicios en línea en un servidor de licencias
Title: Para establecer los servicios en línea en un servidor de licencias
ms:assetid: '4d67b898-0ba9-4eef-ab7d-ee0ca55a688e'
ms:contentKeyID: 18127803
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747563(v=WS.10)'
---

Para establecer los servicios en línea en un servidor de licencias
==================================================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Además, el proceso de subinscripción requiere permisos de lectura y ejecución tanto para la cuenta de usuario de dominio como para el grupo de servicio de RMS (RMS Service Group). Para obtener más información, vea "[Establecimiento de permisos en el archivo del servicio de subinscripción](https://technet.microsoft.com/737bb69b-fe26-4057-9569-e632f7bbf295)", anteriormente en este tema. Si está utilizando una base de datos de SQL Server remota, la cuenta con la que inicie sesión debe tener también la función de creador de bases de datos en el servidor SQL Server. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

En cada servidor, puede establecer los servicios en línea de RMS en un solo sitio Web. Si desea establecer los servicios en línea de RMS en un sitio Web diferente del sitio Web predeterminado, utilice el Administrador de servicios de Internet Information Server para agregar el sitio Web antes de iniciar este proceso de establecimiento de servicios en línea. Si el sitio Web en el que desea establecer los servicios en línea no aparece en la lista de sitios Web, cierre la página **Administración global**, agregue el sitio Web y, a continuación, inicie de nuevo el proceso de establecimiento de servicios en línea.

Si está implementando RMS en un entorno en el que el nivel funcional del dominio de Active Directory está establecido en el modo nativo de Windows 2000, es posible que RMS no pueda leer el atributo **memberOf** de los objetos de Active Directory cuando intente ampliar la pertenencia a grupos. Para que RMS pueda leer el atributo **memberOf**, la cuenta de servicio de RMS debe utilizar una cuenta de dominio que sea miembro del grupo Acceso compatible con versiones anteriores de Windows 2000 (integrado) en el bosque.

Si escribe una dirección URL personalizada para el clúster, no olvide registrarla en el Sistema de nombres de dominio (DNS, Domain Name System) y comprobar que funciona. Si se trata de una implementación que dispone de Internet, compruebe que la dirección URL esté disponible tanto desde Internet como desde el interior de la organización. Si habilita SSL para los archivos de los servicios Web, debe especificar HTTPS para la dirección URL del clúster.

Establecer servicios en línea en servidores de licencias
--------------------------------------------------------

#### Para establecer los servicios en línea en un servidor de licencias

1.  Abra la página **Administración global** y, a continuación, junto al sitio Web en el que desee establecer los servicios en línea de RMS, haga clic en **Establecer los servicios en línea de RMS en este sitio Web**.

    Puede seleccionar el sitio Web predeterminado u otro sitio Web creado en los Servicios de Internet Information Server (IIS) con este propósito.

    > [!WARNING]
    > No se admite la ejecución de sitios o servicios Web adicionales en el mismo servidor que RMS. Si se hiciera así, muchos servicios y aplicaciones se ejecutarían con la misma cuenta que RMS, lo que podría exponer las claves privadas a operaciones no deseadas. 

2.  En el área **Base de datos de configuración**, la opción predeterminada es crear la base de datos de configuración en el servidor local. Puede utilizar un servidor de base de datos como SQL Server™ 2000 con SP3 o Microsoft SQL Server 2000 Desktop Engine (MSDE) para una base de datos local. Si utiliza una base de datos remota, o si ejecuta su servidor de base de datos en el servidor local pero la instancia de servidor de base de datos tiene un nombre distinto al de este servidor, seleccione **Base de datos remota** y, a continuación, escriba el nombre del servidor de base de datos.

    > [!IMPORTANT]
    > Se recomienda el uso de Microsoft SQL Server Desktop Engine para las bases de datos de RMS únicamente en entornos de pruebas, puesto que Microsoft SQL Server Desktop Engine no admite ninguna interfaz de red. Además, las condiciones de uso de Microsoft SQL Server Desktop Engine especifican que no se pueden utilizar herramientas de cliente de SQL Server para manipular una base de datos de Microsoft SQL Server Desktop Engine. Dada esta restricción, no podrá ver información de registro ni cambiar los datos almacenados en la base de datos de configuración.  

3.  En el área **Cuenta de servicio de RMS**, especifique la cuenta de servicio de RMS con la que se ejecutará RMS para la mayoría de las operaciones normales. Para una instalación de un solo servidor, puede especificar la cuenta del sistema local o una cuenta de dominio. Para todas las demás instalaciones, debe especificar una cuenta de dominio. Para una cuenta de dominio, proporcione el nombre de cuenta con el formato *nombre\_servidor*\\*nombre\_usuario* y la contraseña.

    > [!WARNING]
    > La cuenta del sistema local tiene acceso a casi todos los recursos del sistema operativo y, en consecuencia, tiene importantes implicaciones de seguridad. Siempre que sea posible, evite utilizar la cuenta del sistema local como cuenta de servicio de RMS. En cambio, cree una cuenta de usuario de dominio especial para usarla como cuenta de servicio de RMS y no le conceda ningún permiso especial. La cuenta de servicio de RMS no puede ser la misma cuenta de dominio que se utilizó para instalar RMS. 

4.  En el área **Dirección URL del clúster**, escriba la dirección URL del servidor o del clúster que se utilizará para clientes de la red interna. La entrada predeterminada utiliza el nombre del servidor, por ejemplo Contoso-cert. Puede modificarlo si es necesario, por ejemplo para configurar una dirección URL para el clúster o para un equilibrador de carga que sirva al clúster. También puede seleccionar HTTP o HTTPS. Vea la sección **Notas**, al final de la lista de este procedimiento, para obtener más información acerca de la configuración de la dirección URL de un clúster. Después de establecer los servicios en línea, puede configurar, en las páginas Web de administración, la dirección URL de un clúster externo que pueden utilizar los clientes que estén fuera de la red interna.

5.  En el área **Protección de clave privada y subinscripción**, seleccione el mecanismo para proteger la clave privada de servidor siguiendo alguno de los procedimientos siguientes:

    -   **Utilizar la protección de clave privada de software predeterminada**. Si selecciona esta opción, la clave privada se almacena en la base de datos de configuración de RMS. Debe proporcionar una contraseña segura para cifrar la clave en la base de datos.

    > [!IMPORTANT]
    > Proteja esta contraseña en un archivo seguro para futuras referencias. Almacene una copia de seguridad de la base de datos de configuración (también protegida con esta contraseña) en el archivo seguro. Esto proporciona un mecanismo para restaurar RMS si se daña la base de datos de SQL Server. Si cambia la contraseña por cualquier razón, realice una nueva copia de seguridad de la base de datos de configuración que utilice como clave esa contraseña y, a continuación, guarde ambas en el archivo seguro. 

    -   **Utilizar un proveedor de servicios de cifrado (CSP)**. Para utilizar un CSP o un módulo de seguridad de hardware (HSM), desactive la casilla de verificación **Utilizar la protección de clave privada de software predeterminada**. En la lista **Seleccione el proveedor de servicios de cifrado**, seleccione el CSP o HSM instalado.

    > [!NOTE]
    > RMS necesita un proveedor Rivest-Shamir-Adleman (RSA) completo; en la lista de CSP sólo se incluyen estos proveedores. 

    > [!NOTE]
    > Es recomendable utilizar la protección de clave privada de software predeterminada o un HSM. Si utiliza un CSP de software diferente, asegúrese de que se utilicen prácticas de administración de claves de organización (tales como procedimientos de copia de seguridad y restauración) para ese CSP antes de utilizarlo con RMS. 

6.  Este paso sólo se aplica si se seleccionó un CSP. Para especificar el par de claves de servidor que se va a utilizar, siga alguno de estos procedimientos:

    -   Para una nueva instalación, seleccione **Crear un nuevo par de claves pública y privada**.
    -   Si va a recuperar o actualizar un servidor de RMS existente, seleccione **Utilizar un par de claves pública y privada existente**. En Contenedor de claves existente, haga clic en **Examinar** y, a continuación, seleccione el contenedor de claves para el par de claves de servidor.

    > [!NOTE]
    > Los CSP mejorados y seguros basados en Microsoft comparten la misma ubicación de almacenamiento de claves. 

    > [!NOTE]
    > Si no utiliza un par de claves existente al recuperar o actualizar un servidor de RMS existente, será preciso borrar los almacenes de licencias (las licencias de uso y los certificados de cuenta de permisos) de todos los clientes de RMS, que luego tendrán que obtener nuevas licencias del servidor para utilizar contenido. 

7.  En **Nombre del certificado emisor de licencias de servidor**, escriba el nombre que se utilizará dentro del certificado emisor de licencias de servidor. De forma predeterminada, es el nombre del servidor.

8.  Si la organización utiliza un servidor proxy para conectarse a Internet, active la casilla de verificación **Este equipo utiliza un servidor proxy para conectarse a Internet** y, a continuación, escriba la dirección y el puerto del servidor proxy.

    Si el servidor proxy requiere autenticación, seleccione el tipo de autenticación y proporcione un nombre de usuario y una contraseña que el servidor proxy pueda autenticar. Si utiliza autenticación de Windows integrada, también debe especificar un dominio.

9.  Haga clic en **Enviar**.

    El servicio de subinscripción de RMS genera un par de claves pública y privada para el servidor de licencias y firma la clave pública con la clave privada del servidor de certificación raíz. También crea un certificado emisor de licencias de servidor para el servidor de licencias. En pocos minutos, envía estos elementos a la base de datos de configuración.

    > [!IMPORTANT]
    > Si aparecen mensajes de error, no cierre la página. En su lugar, corrija los errores, utilice IISReset desde la línea de comandos para iniciar y reiniciar IIS, vuelva a la página anterior y, a continuación, haga clic otra vez en **Enviar**. Si obtiene el error "Tiempo de espera agotado para esta solicitud", cierre la ventana, compruebe que el sistema cumple los requisitos mínimos de hardware e intente establecer los servicios en línea en el servidor otra vez. 

Para obtener instrucciones acerca del establecimiento de servicios en línea en servidores de licencias adicionales y cómo agregarlos a un clúster, vea "[Para agregar un servidor a un clúster](https://technet.microsoft.com/db635238-5528-4bec-9cc6-8244e2b3d733)", más adelante en este tema.
