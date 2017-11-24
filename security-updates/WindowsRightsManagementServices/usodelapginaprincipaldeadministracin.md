---
TOCTitle: Uso de la página principal de administración
Title: Uso de la página principal de administración
ms:assetid: '6c155977-bd0e-47d6-ac65-1746cddb505e'
ms:contentKeyID: 18127840
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720290(v=WS.10)'
---

Uso de la página principal de administración
============================================

En la **página principal de** administración, puede ver información sobre el servidor o clúster, así como obtener acceso a las opciones de administración. Esta página está disponible únicamente después de haber establecido los servicios en línea en el servidor.

Para obtener acceso a esta página Web desde el servidor que desee administrar, siga estos pasos:

1.  Inicie sesión como administrador local.
2.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Windows RMS** y haga clic en **Administración de Windows RMS**.
3.  En la página **Administración global**, haga clic en **Administrar RMS en este sitio Web**.

Si ha habilitado la administración remota mediante la capa de sockets seguros (SSL), también puede tener acceso a la **página principal de administración** desde un equipo diferente siguiendo este procedimiento:

1.  En la barra de dirección del explorador Web, escriba la siguiente dirección URL:  
    https://*nombre\_clúster:número\_puerto*/\_wmcs/admin  

    Donde *nombre\_clúster:número\_puerto* es la dirección URL que especificó para este clúster durante el establecimiento de los servicios en línea. Proporcione el número de puerto únicamente si especificó uno diferente al predeterminado, 80.

2.  Cuando lo solicite el sistema, escriba las credenciales de un administrador local del servidor al que esté obteniendo acceso.

La **página principal de administración** muestra información sobre el clúster, como la dirección URL, el nombre y la ubicación de la base de datos de configuración, la fecha de caducidad del certificado emisor de licencias de servidor, etc. Además, proporciona vínculos a páginas donde puede configurar las siguientes opciones de administración para el clúster:

-   **Directivas de confianza.**Agregue y quite dominios de confianza. Para obtener más información, vea “[Administración de la confianza y directivas de confianza](https://technet.microsoft.com/1c96ee74-fd28-4511-be21-087e2b04c3ee)”, más adelante en este tema.
-   **Plantillas de directiva de permisos**. Cree y modifique plantillas de directiva de permisos. Para obtener más información, vea “[Administración de plantillas de directiva de permisos](https://technet.microsoft.com/718286dc-3399-4556-96c9-ec3a33d31877)”, más adelante en este tema.
-   **Configuración del registro**. Active y desactive el registro, y vea el nombre del servidor y la base de datos de registro. Para obtener más información, vea “[Administración del registro](https://technet.microsoft.com/8fccfc57-2135-494e-8e44-f6191bf5e4a0)”, más adelante en este tema.
-   **Configuración de la dirección URL de clúster de extranet.**Especifique una dirección URL disponible externamente para las solicitudes de licencias y certificación de cuentas. Para obtener más información, vea “[Configuración de una dirección URL de la extranet](https://technet.microsoft.com/88fec9ff-c96c-4d20-8856-0485e7507572)”, más adelante en este tema.
-   **Configuración de proxy de RMS.**Especifique la dirección del servidor proxy, el tipo de autenticación y el nombre de usuario que se usarán cuando el servidor de RMS deba conectarse a Internet a través de un servidor proxy. Para obtener más información, vea “[Configuración de proxy de RMS](https://technet.microsoft.com/179d2970-62e9-4487-aa5b-f4334234991e)”, más adelante en este tema.
-   **Configuración de seguridad.**Restablezca la contraseña de la clave privada del servidor, especifique el grupo de superusuarios, cuyos miembros pueden descifrar todo el contenido con licencia, y retire RMS. Para obtener más información, vea “[Administración de la seguridad al utilizar RMS](https://technet.microsoft.com/62050812-de4f-4392-8d63-f2f89aa01ed4)”, más adelante en este tema.
-   **Configuración de certificación.**Especifique el período de validez de los certificados de cuenta de permisos y los datos de contacto de un administrador. Esta opción está disponible únicamente en el clúster de certificación raíz, no en los servidores de licencias. Para obtener más información, vea “[Administración de certificados de cuenta de permisos](https://technet.microsoft.com/49c5c2ba-e197-4e4b-b3b3-b3248f068bcc)”, más adelante en este tema.
-   **Directivas de exclusión.**Especifique la exclusión basándose en la versión de la caja de seguridad, el certificado de cuenta de permisos, la versión de Windows o la aplicación compatible con RMS. Para obtener más información, vea “[Administración de directivas de exclusión](https://technet.microsoft.com/ee31e099-e095-4648-95da-0009fbeb48cb)”, más adelante en este tema.
-   **Informe de certificación de cuentas de RM.**Vea el número de certificados de cuenta de permisos que se han emitido. Esta opción está disponible únicamente en el clúster de certificación raíz, no en los servidores de licencias. Para obtener más información, vea “[Seguimiento de certificados de cuenta de permisos](https://technet.microsoft.com/5bb0f3cf-fc44-4e60-a93f-c789d6f8a902)”, más adelante en este tema.

Los demás temas de esta sección explican cómo utilizar estas funciones. Para obtener instrucciones paso a paso, vea “[RMS Cómo...](https://technet.microsoft.com/82032075-f361-438f-a2c4-93ab29ae6cff)”, más adelante en este tema.

> [!NOTE]
> El sitio Web de administración de RMS utiliza ventanas emergentes para la configuración de algunas funciones. Si utiliza un bloqueador de ventanas emergentes con el explorador Web, deberá configurar los valores del explorador para permitir que aparezcan las ventanas emergentes del sitio Web de administración de RMS. 
