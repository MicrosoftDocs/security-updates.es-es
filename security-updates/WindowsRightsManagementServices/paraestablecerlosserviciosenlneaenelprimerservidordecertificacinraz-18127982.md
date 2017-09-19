---
TOCTitle: Para establecer los servicios en línea en el primer servidor de certificación raíz
Title: Para establecer los servicios en línea en el primer servidor de certificación raíz
ms:assetid: 'debc42f3-74ff-4c99-b7a4-4921fccdabc2'
ms:contentKeyID: 18127982
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747768(v=WS.10)'
---

Para establecer los servicios en línea en el primer servidor de certificación raíz
==================================================================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Si está creando una base de datos de SQL Server remota, esta cuenta deberá tener además la función de creador de bases de datos en el servidor SQL Server. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

En cada servidor, puede establecer los servicios en línea de RMS en un solo sitio Web. Si desea establecer los servicios en línea de RMS en un sitio Web diferente del sitio Web predeterminado, utilice el Administrador de servicios de Internet Information Server para agregar el sitio Web antes de iniciar este proceso de establecimiento de servicios en línea. Si el sitio Web en el que desea establecer los servicios en línea no aparece en la lista de sitios Web, cierre la página **Administración global**, agregue el sitio Web y, a continuación, inicie de nuevo el proceso de establecimiento de servicios en línea.

Si está implementando RMS en un entorno en el que el nivel funcional del dominio de Active Directory está establecido en el modo nativo de Windows 2000, es posible que RMS no pueda leer el atributo **memberOf** de los objetos de Active Directory cuando intente ampliar la pertenencia a grupos. Para que RMS pueda leer el atributo **memberOf**, la cuenta de servicio de RMS debe utilizar una cuenta de dominio que sea miembro del grupo Acceso compatible con versiones anteriores de Windows 2000 (integrado) en el bosque.

Si escribe una dirección URL personalizada para el clúster, no olvide registrarla en el Sistema de nombres de dominio (DNS, Domain Name System) y comprobar que funciona. Si se trata de una implementación que dispone de Internet, compruebe que la dirección URL esté disponible tanto desde Internet como desde el interior de la organización. Si habilita SSL para los archivos de los servicios Web, debe especificar HTTPS para la dirección URL del clúster.

Establecimiento de servicios en línea en el primer servidor de certificación raíz
---------------------------------------------------------------------------------

#### Para establecer los servicios en línea en el primer servidor de certificación raíz

1.  Después de instalar RMS en un servidor que vaya a ser el primer servidor de certificación raíz de un bosque de Active Directory, abra la página **Administración global**.

2.  Junto al sitio Web en el que desee establecer los servicios en línea de RMS, haga clic en **Establecer los servicios en línea de RMS en este sitio Web**. Puede seleccionar el sitio Web predeterminado u otro sitio Web creado en los Servicios de Internet Information Server (IIS) con este propósito.

    | ![](images/Cc747768.Warning(WS.10).gif)Advertencia                                                                                                                                                                                   |
    |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | No se admite la ejecución de sitios o servicios Web adicionales en el mismo servidor que RMS. Si se hiciera así, muchos servicios y aplicaciones se ejecutarían con la misma cuenta que RMS, lo que podría exponer las claves privadas a operaciones no deseadas. |

3.  En el área **Base de datos de configuración**, la opción predeterminada es crear la base de datos de configuración en el servidor local. Puede utilizar un servidor de base de datos como SQL Server™ 2000 con SP3 o Microsoft SQL Server 2000 Desktop Engine (MSDE) para una base de datos local. Si utiliza una base de datos remota, o si ejecuta su servidor de base de datos en el servidor local pero la instancia de servidor de base de datos tiene un nombre distinto al de este servidor, seleccione **Base de datos remota** y, a continuación, escriba el nombre del servidor de base de datos.

    | ![](images/Cc747768.Important(WS.10).gif)Importante                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
    |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Se recomienda el uso de Microsoft SQL Server Desktop Engine para las bases de datos de RMS únicamente en entornos de pruebas, puesto que Microsoft SQL Server Desktop Engine no admite ninguna interfaz de red. Además, las condiciones de uso de Microsoft SQL Server Desktop Engine especifican que no se pueden utilizar herramientas de cliente de SQL Server para manipular una base de datos de Microsoft SQL Server Desktop Engine. Dada esta restricción, no podrá ver información de registro ni cambiar los datos almacenados en la base de datos de configuración.  |

4.  En el área **Cuenta de servicio de RMS**, especifique la cuenta de servicio de RMS con la que se ejecutará RMS para la mayoría de las operaciones normales. Para una instalación de un solo servidor, puede especificar la cuenta del sistema local o una cuenta de dominio. Para todas las demás instalaciones, debe especificar una cuenta de dominio. Para una cuenta de dominio, proporcione el nombre de cuenta con el formato *nombre\_servidor*\\*nombre\_usuario* y la contraseña.

    | ![](images/Cc747768.Warning(WS.10).gif)Advertencia                                                                                                                                                                                                                                                                                                                                                                                                                                     |
    |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | La cuenta del sistema local tiene acceso a casi todos los recursos del sistema operativo y, en consecuencia, tiene importantes implicaciones de seguridad. Siempre que sea posible, evite utilizar la cuenta del sistema local como cuenta de servicio de RMS. En cambio, cree una cuenta de usuario de dominio especial para usarla como cuenta de servicio de RMS y no le conceda ningún permiso especial. La cuenta de servicio de RMS no puede ser la misma cuenta de dominio que se utilizó para instalar RMS. |

    | ![](images/Cc747768.Important(WS.10).gif)Importante                                                                                                                                                                                                                        |
    |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Por razones de seguridad, es recomendable crear una cuenta de usuario de dominio especial para usarla como cuenta de servicio de RMS y no concederle ningún permiso especial. La cuenta de servicio de RMS no puede ser la misma cuenta de dominio que se utilizó para instalar RMS con Service Pack 1. |

5.  En el área **Dirección URL del clúster**, escriba la dirección URL del servidor o del clúster que se utilizará para clientes de la red interna. La entrada predeterminada utiliza el nombre del servidor, por ejemplo Contoso-cert. Puede modificarlo si es necesario, por ejemplo para configurar una dirección URL para el clúster o para un equilibrador de carga que sirva al clúster. También puede seleccionar HTTP o HTTPS. Vea la sección **Notas**, al final de la lista de este procedimiento, para obtener más información acerca de la configuración de la dirección URL de un clúster. Después de establecer los servicios en línea, puede configurar, en las páginas Web de administración, la dirección URL de un clúster externo que pueden utilizar los clientes que estén fuera de la red interna.

6.  En el área **Protección de clave privada e inscripción**, seleccione el mecanismo para proteger la clave privada de servidor siguiendo alguno de los procedimientos siguientes:

    -   **Utilizar la protección de clave privada de software predeterminada**. Si selecciona esta opción, la clave privada se almacena en la base de datos de configuración de RMS. Debe proporcionar una contraseña segura para cifrar la clave en la base de datos.

    | ![](images/Cc747768.Important(WS.10).gif)Importante                                                                                                                                                                                                                                                                                                                                                                                                                                         |
    |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Proteja esta contraseña en un archivo seguro para futuras referencias. Almacene una copia de seguridad de la base de datos de configuración (también protegida con esta contraseña) en el archivo seguro. Esto proporciona un mecanismo para restaurar RMS si se daña la base de datos de SQL Server. Si cambia la contraseña por cualquier razón, realice una nueva copia de seguridad de la base de datos de configuración que utilice como clave esa contraseña y, a continuación, guarde ambas en el archivo seguro. |

    -   **Utilizar un proveedor de servicios de cifrado (CSP)**. Para utilizar un CSP o un módulo de seguridad de hardware (HSM), desactive la casilla de verificación **Utilizar la protección de clave privada de software predeterminada**. En la lista **Seleccione el proveedor de servicios de cifrado**, seleccione el CSP o HSM instalado.

    | ![](images/Cc747768.note(WS.10).gif)Nota                                                  |
    |------------------------------------------------------------------------------------------------------------------------|
    | RMS necesita un proveedor Rivest-Shamir-Adleman (RSA) completo; en la lista de CSP sólo se incluyen estos proveedores. |

    | ![](images/Cc747768.note(WS.10).gif)Nota                                                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Es recomendable utilizar la protección de clave privada de software predeterminada o un HSM. Si utiliza un CSP de software diferente, asegúrese de que se utilicen prácticas de administración de claves de organización (tales como procedimientos de copia de seguridad y restauración) para ese CSP antes de utilizarlo con RMS. |

7.  Este paso sólo se aplica si se seleccionó un CSP. Para especificar el par de claves de servidor que se va a utilizar, siga alguno de estos procedimientos:

    -   Para una nueva instalación, seleccione **Crear un nuevo par de claves pública y privada**.
    -   Si va a recuperar o actualizar un servidor de RMS existente, seleccione **Utilizar un par de claves pública y privada existente**. En **Contenedor de claves existente**, haga clic en **Examinar** y, a continuación, seleccione el contenedor de claves para el par de claves de servidor.

    | ![](images/Cc747768.note(WS.10).gif)Nota                                      |
    |------------------------------------------------------------------------------------------------------------|
    | Los CSP mejorados y seguros basados en Microsoft comparten la misma ubicación de almacenamiento de claves. |

    | ![](images/Cc747768.note(WS.10).gif)Nota                                                                                                                                                                                                                                                              |
    |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Si no utiliza un par de claves existente al recuperar o actualizar un servidor de RMS existente, será preciso borrar los almacenes de licencias (las licencias de uso y los certificados de cuenta de permisos) de todos los clientes de RMS, que luego tendrán que obtener nuevas licencias del servidor para utilizar contenido. |

8.  En **Conectividad a Internet del servidor**, especifique si este servidor se conecta a Internet para obtener un certificado emisor de licencias de servidor.

    -   Seleccione **En línea** para conectarse automáticamente al servicio de inscripción de Microsoft y obtener un certificado emisor de licencias de servidor durante el proceso de establecimiento de servicios en línea.
    -   Seleccione **Sin conexión** si el servidor de RMS no tiene conexión a Internet o si desea obtener manualmente el certificado emisor de licencias de servidor e importarlo al servidor de RMS una vez establecidos los servicios en línea.

9.  En **Nombre del certificado emisor de licencias de servidor**, escriba el nombre que se utilizará dentro del certificado emisor de licencias de servidor. De forma predeterminada, es el nombre del servidor.

10. Si la organización utiliza un servidor proxy para conectarse a Internet, active la casilla de verificación **Este equipo utiliza un servidor proxy para conectarse a Internet** y, a continuación, escriba la dirección y el puerto del servidor proxy.

    Si el servidor proxy requiere autenticación, seleccione el tipo de autenticación y proporcione un nombre de usuario y una contraseña que el servidor proxy pueda autenticar. Si utiliza autenticación de Windows integrada, también debe especificar un dominio.

    | ![](images/Cc747768.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
    |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Esta configuración se puede modificar después de establecer los servicios en línea desde la página **Configuración de seguridad** del sitio Web de administración de RMS. Sin embargo, dicha página no está disponible hasta que el servidor se haya inscrito con el servicio de inscripción de Microsoft. Si su organización le obliga a utilizar un servidor proxy para conectarse a Internet y no ha configurado un servidor proxy porque había seleccionado la opción **Sin conexión** para **Conectividad a Internet del servidor**, no podrá cambiar la configuración del proceso de inscripción ni del servidor proxy hasta finalizar el proceso de inscripción manual o hasta que vuelva a establecer los servicios en línea de RMS. |

11. En **Contacto administrativo**, escriba la dirección de correo electrónico del administrador de contacto si se producen problemas con el establecimiento de otros servidores. Después de establecer los servicios en línea, puede cambiar esta dirección de correo electrónico.

12. En el área **Revocación**, seleccione si se autorizará o no que una entidad de terceros revoque el certificado emisor de licencias de este servidor. Si selecciona esta opción, escriba la ruta de acceso y el nombre del archivo de clave pública de la entidad de terceros.

13. Haga clic en **Enviar**.

    Al hacer clic en **Enviar**, se establecen los servicios en línea. Si ha seleccionado la inscripción en línea, también se llevará a cabo el proceso de inscripción para el servidor de certificación raíz. Durante este proceso, RMS genera un par de claves pública y privada y envía la clave pública al servicio de inscripción de Microsoft. El servicio de inscripción de Microsoft crea un certificado emisor de licencias de servidor y lo devuelve a la base de datos de configuración en pocos minutos. Si está utilizando la inscripción sin conexión, deberá completar la tarea descrita en "[Para inscribir manualmente un servidor de certificación raíz](https://technet.microsoft.com/aecdebb5-b28b-4b58-937a-392bb6ce9643)", más adelante en este tema, para poder configurar el servidor de RMS.

    | ![](images/Cc747768.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                               |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Este servidor no podrá utilizarse hasta que se haya registrado el punto de conexión de servicio (SCP) de RMS en Active Directory; siga los pasos que se indican en "[Para registrar un punto de conexión de servicio](https://technet.microsoft.com/630cc3c3-9ed9-4423-8874-cbaceb43b353)", más adelante en este tema, para completar este proceso. |

Para ver instrucciones acerca del establecimiento de servicios en línea en servidores de certificación raíz adicionales y cómo agregarlos a un clúster, vea "[Para agregar un servidor a un clúster](https://technet.microsoft.com/db635238-5528-4bec-9cc6-8244e2b3d733)", más adelante en este tema.
