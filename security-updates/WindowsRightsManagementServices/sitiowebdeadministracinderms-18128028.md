---
TOCTitle: Sitio Web de administración de RMS
Title: Sitio Web de administración de RMS
ms:assetid: 'f003c1d9-9a17-4e50-9e1e-5d67677552a0'
ms:contentKeyID: 18128028
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747796(v=WS.10)'
---

Sitio Web de administración de RMS
==================================

Todos los clústeres raíz y de sólo licencias albergan un sitio web de administración, necesario para administrar RMS. Este sitio Web está disponible únicamente en el servidor de RMS que esté administrando o mediante una conexión a Escritorio remoto.

En este tema, se describen las funciones del sitio Web de administración. Encontrará instrucciones para usar el sitio web para administrar RMS en "RMS Cómo..." y "Administración de RMS" en "RMS: Operations" en esta recopilación de documentación.

**Nota   **La configuración del clúster es global. Es posible administrar la configuración de un clúster desde el sitio Web de administración de cualquiera de los servidores que lo componen.

Para realizar las tareas siguientes, abra la página **Administración global**:

-   Establecer los servicios en línea de RMS en un sitio Web.
-   Establecer los servicios en línea en un servidor y agregarlo a un clúster.
-   Quitar RMS de un sitio Web.
-   Ir a las páginas de administración del clúster.

Abra la página **Administración** de un clúster para realizar las tareas siguientes:

-   **Ver información de clúster.** Es posible ver información del clúster, como la dirección URL de instalación, la dirección URL del servidor, el nombre del certificado, el servidor de la base de datos de configuración, el nombre de la base de datos de configuración y la fecha de caducidad del certificado.
-   **Inscribir o renovar el certificado emisor de licencias de servidor.** Puede inscribir o renovar el certificado emisor de licencias de servidor del clúster.
-   **Establecer directivas de confianza.** Haga clic en el vínculo para abrir la página web Directivas de confianza, en la que puede agregar o quitar dominios de usuarios de confianza y dominios de publicación de confianza. Agregar o quitar usuarios de la lista de exclusión de un dominio de usuario de confianza. Exportar el certificado emisor de licencias de servidor a un archivo para importarlo en otra instalación de RMS.
-   **Configurar plantillas de directiva de permisos.** Haga clic en el vínculo para abrir la página web Plantillas de directiva de permisos, en la que puede crear y modificar plantillas de directiva de permisos para la empresa.
-   **Configurar el registro.**Haga clic en el vínculo para abrir la página web Configuración de registro, en la que puede activar y desactivar el registro y, a continuación, ver el servidor y la base de datos de registro.
-   **Especificar la dirección URL del clúster de la extranet.** Haga clic en el vínculo para abrir la página web Configuración de la dirección URL del clúster de la extranet, en la que puede especificar la dirección URL que se usará para obtener acceso a los servidores de certificación del clúster raíz desde la extranet.
-   **Especificar la configuración de proxy de RMS.** Haga clic en el vínculo para abrir la página web Configuración de proxy de RMS, donde puede especificar la dirección del servidor proxy, el tipo de autenticación y el nombre de usuario que se usarán cuando el servidor de RMS necesite conectarse a Internet a través de un servidor proxy.
-   **Realizar un seguimiento del número de certificados de cuenta de permisos distribuidos.** Haga clic en el vínculo para abrir la página web de seguimiento de certificados de cuenta de permisos, desde la que podrá ver cuántos certificados de cuenta de permisos ha distribuido el clúster raíz, lo cual puede servirle para calcular el número de licencias de acceso de cliente que necesita.
-   **Administrar la configuración de seguridad.** Haga clic en el vínculo para abrir la página web Configuración de seguridad, en la que puede agregar o quitar integrantes del grupo de superusuarios, que tienen control total sobre todo el contenido bajo licencia, así como restablecer la contraseña de clave privada.
-   **Ver y establecer la configuración de los certificados de cuenta.** Haga clic en el vínculo para abrir la página web Configuración de certificación, en la que puede especificar el período de validez del certificado, así como un administrador de contacto.
-   **Habilitar directivas de exclusión.** Haga clic en el vínculo para abrir la página web Directivas de exclusión, desde la que puede habilitar directivas de exclusión basándose en la versión de la caja de seguridad, la versión de Windows, certificados de cuenta y aplicaciones.
-   **Registrar el punto de conexión de servicio.** Haga clic en el vínculo para abrir la página web Punto de conexión de servicio, en la que puede registrar o eliminar el registro del punto de conexión de servicio del clúster.

Los administradores pueden realizar otras tareas, como supervisar eventos y administrar Active Directory, Servicios de Internet Information Server (IIS) y SQL Server, mediante la consola Microsoft Management Console (MMC).
