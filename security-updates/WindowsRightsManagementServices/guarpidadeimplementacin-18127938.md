---
TOCTitle: Guía rápida de implementación
Title: Guía rápida de implementación
ms:assetid: 'b8fb69b6-3e0b-4836-8c05-8bd93f522a7c'
ms:contentKeyID: 18127938
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747735(v=WS.10)'
---

Guía rápida de implementación
=============================

Esta guía pretende ayudarle a configurar de forma rápida un servidor de Windows RMS con Service Pack 1, para poder evaluarlo y decidir si desea una implementación a mayor escala en su organización.

**Paso 1 - Preparación para RMS**

RMS depende de otros componentes que se instalan y configuran antes de utilizar este servicio. Una infraestructura satisfará los requisitos básicos de RMS después de completar los siguientes pasos:

1.  Configure un equipo que ejecute Windows Server 2003 y únalo después a un dominio de Active Directory. Para pequeñas organizaciones que sólo tienen un servidor, este equipo también puede ser el controlador de dominio para Active Directory. Sin embargo, en este caso, el equipo debe ejecutar Windows Server 2003, Standard Edition; Windows Server 2003, Enterprise Edition o Windows Server 2003, Datacenter Edition. Un equipo que ejecute Windows Server 2003, Web Edition, no puede ser un controlador de dominio.
2.  Configure el servidor para la función **Servidor de aplicaciones**. Para ello, haga clic en **Inicio**, haga doble clic en **Panel de control** y después en la herramienta **Agregar o quitar programas**. En **Agregar o quitar programas**, haga clic en **Agregar o quitar componentes de Windows** y asegúrese de que los siguientes servicios estén habilitados en **Servidor de aplicaciones**:
    -   **ASP.NET**
    -   **Servicios de Internet Information Server (IIS)**
    -   **Servicios de Message Queue Server**

    Acepte las opciones predeterminadas para cada servicio. No se necesita ninguna configuración más.
3.  Configure una base de datos utilizando alguna de las siguientes aplicaciones de base de datos:
    -   Microsoft® SQL Server 2000 con SP3a. Puede ser una instalación local de SQL Server 2000 o una instalación remota que se encuentre en el mismo dominio.
    -   Microsoft SQL Server 2000 Desktop Engine (MSDE 2000) Versión A. Debe ser una instalación local. Puede descargar MSDE 2000 del [sitio Web de Microsoft](http://go.microsoft.com/fwlink/?linkid=17799) (http://go.microsoft.com/fwlink/?LinkID=17799).

    Se recomienda el uso de Microsoft SQL Server Desktop Engine para permitir las bases de datos de RMS únicamente en entornos de pruebas, puesto que Microsoft SQL Server Desktop Engine no incluye las herramientas necesarias para que funcione completamente una base de datos a nivel corporativo. Además, dado que MSDE no permite el trabajo con red remota, debe instalarlo en el mismo servidor que RMS y no puede añadir servidores de RMS adicionales al clúster de RMS. Las condiciones de uso de Microsoft SQL Server Desktop Engine especifican que no se pueden utilizar herramientas de cliente de SQL Server para manipular una base de datos de Microsoft SQL Server Desktop Engine. Con esta restricción, no podrá realizar copias de seguridad y restaurar la base de datos de configuración de RMS, ver información de registro o modificar directamente datos almacenados en la base de datos de configuración.
4.  Decida el nombre por el que desea que se conozca este servicio cuando los usuarios intenten conectarse a la intranet (por ejemplo, http://certification.contoso.com). Configure el sistema de nombres de dominio (DNS) para resolver esa dirección URL en la dirección IP del equipo de RMS. Debe utilizar un nombre de dominio DNS completo para la dirección URL de clúster a fin de garantizar que los clientes de otras zonas DNS puedan resolver la dirección IP de los servidores de RMS.
5.  Cree una cuenta de administrador para usarla con RMS.
6.  Ahora ya está preparado para instalar RMS SP1. Para obtener instrucciones adicionales acerca de este paso, vea “Para instalar RMS con Service Pack 1” en “Operación de un servidor de RMS”, en esta recopilación de información.

**Características opcionales utilizadas habitualmente**

Las características que se describen a continuación son opcionales. Si decide utilizarlas, no olvide preparar todo lo necesario antes de comenzar la instalación y el proceso de establecimiento de servicios en línea de RMS.

-   Puede configurar RMS para utilizar un módulo de seguridad de hardware (HSM) para almacenar claves privadas. Si desea utilizar un módulo de seguridad de hardware, asegúrese de que los controladores estén correctamente configurados y que se haya definido el entorno de seguridad.
-   Puede descargar automáticamente un certificado emisor de licencias de servidor durante el proceso de establecimiento de servicios en línea si su equipo de RMS tiene conexión a Internet. Si su organización utiliza un servidor proxy para conectarse a Internet, compruebe la configuración del proxy en Internet Explorer, incluidos los requisitos de autenticación, y anótela para usarla más tarde.
-   Si va a ejecutar RMS en un controlador de dominio y planea usar una cuenta de usuario para ejecutar los servicios de RMS, asegúrese de que la Directiva de seguridad del controlador de dominio esté configurada para conceder al usuario permiso para iniciar sesión localmente. Para obtener más información acerca de cómo configurar la Directiva de seguridad del controlador de dominio, vea la Ayuda y Soporte técnico de Windows Server 2003.

**Paso 2 - Establecer servicios en línea del primer servidor de RMS**

El establecimiento de servicios en línea es el proceso de configuración de un sitio Web con RMS para que los usuarios puedan empezar a usar ese servicio. Siga estos pasos para establecer los servicios en línea en el servidor de certificación raíz para su organización:

1.  Inicie sesión en el equipo como usuario de dominio con privilegios de administrador local. Si va a instalar RMS en un controlador de dominio, inicie la sesión como administrador de dominio.
2.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Windows RMS** y haga clic en **Administración de Windows RMS** para abrir la página **Administración global**. Esta página muestra los sitios Web que están disponibles en este servidor.
3.  Haga clic en el sitio Web en el que desee establecer servicios en línea de RMS y, a continuación, haga clic en **Establecer los servicios en línea de RMS en este sitio Web**. Cuando se abre la página, muestra **Establecer servicios en línea en el servidor de certificación raíz de RMS** en la parte superior.
4.  Rellene la página con la información de su organización.
    -   En el cuadro **Dirección URL del clúster**, escriba el nombre de servicio (como certification.contoso.com) que ha configurado en el paso 4 del procedimiento anterior. Si desea utilizar SSL con su instalación, haga clic en el protocolo HTTPS en la lista de protocolos. Al hacerlo, se activa SSL; sin embargo, esta selección no requerirá SSL para los servicios Web de RMS. Debe configurarlo por separado a través e IIS.
    -   Si el servidor está conectado a Internet a través de un servidor proxy, en el área **Configuración de proxy de RMS** rellene la sección con la información de Internet Explorer como se indica en la sección de características opcionales del procedimiento anterior.
    -   En el área **Conectividad a Internet del servidor**, seleccione **En línea** si desea que el servidor se conecte al servicio de inscripción de Microsoft a través de Internet y obtener automáticamente un certificado emisor de licencias de servidor durante el proceso de establecimiento de servicios en línea. Seleccione **Sin conexión** si desea conectarse manualmente al servicio de inscripción de Microsoft y descargar un certificado emisor de licencias de servidor para importarlo después de establecer los servicios en línea de RMS.
5.  Haga clic en **Enviar**.
    En aproximadamente 60 o 90 segundos, se habrá completado el establecimiento de los servicios en línea, lo que permitirá volver a la página **Administración global**, donde podrá administrar el servidor de RMS en el que se acaban de establecer los servicios en línea.
6.  En la página **Administración global**, seleccione **Administrar RMS en este sitio Web** para abrir la **página principal de administración** del servidor de RMS.
    Si ha seleccionado Sin conexión en Conectividad a Internet del servidor en el paso 4, complete el proceso "Para inscribir manualmente un servidor de certificación raíz" antes de continuar.
7.  En la página principal de administración, haga clic en el vínculo **Punto de conexión de servicio de RMS**.

> [!NOTE]
> El paso siguiente de este procedimiento: registrar un punto de conexión de servicio, requiere el uso de una cuenta de dominio con privilegios suficientes para crear un objeto contenedor en el contenedor de servicios del contenedor de configuración de bosques de Active Directory. El grupo de seguridad predefinido, **Administradores de organización**, es un ejemplo de cuenta con los privilegios necesarios. 

1.  En la página **Punto de conexión de servicio de RMS**, haga clic en el botón **Registrar URL**. Se registra el punto de conexión de servicio de RMS en Active Directory, a fin de que las aplicaciones compatibles con RMS puedan detectar sus licencias de RMS, el proxy de activación y los servicios de certificación.

**Paso 3 - Probar RMS**

Para poder utilizar totalmente RMS, debe instalar el cliente de Servicios de Microsoft Windows Rights Management y una aplicación compatible con RMS en los equipos cliente. Los usuarios deben ser miembros del dominio de Active Directory y los equipos cliente deben unirse al dominio. Asimismo, los usuarios del dominio deben tener direcciones de correo electrónico que se definen en Active Directory. Para probar RMS:

1.  Inicie sesión en el equipo cliente como usuario válido.
2.  Instale el cliente RMS para Service Pack 1.
3.  Instale una aplicación compatible con RMS.
4.  Cree un archivo protegido con RMS, dé a todo el mundo permisos de sólo lectura a ese archivo y después guarde el archivo en un recurso compartido de archivos al que los usuarios tengan acceso completo.
5.  Inicie sesión en el equipo como un usuario diferente. Abra el archivo e intente realizar cambios. Con RMS instalado correctamente, no puede realizar cambios en este archivo.
