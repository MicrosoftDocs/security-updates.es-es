---
TOCTitle: Uso de tarjetas inteligentes para autenticar clientes
Title: Uso de tarjetas inteligentes para autenticar clientes
ms:assetid: '5caacd67-fb16-46f1-b1ad-4aef0a632bf0'
ms:contentKeyID: 18127831
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747579(v=WS.10)'
---

Uso de tarjetas inteligentes para autenticar clientes
=====================================================

Si utiliza tarjetas inteligentes en su organización para proporcionar seguridad adicional y control sobre las credenciales de usuario, ahora podrá utilizar dichas tarjetas al obtener certificados de cuenta de permisos y licencias de usuario del servidor RMS. Para configurar el servidor de RMS de modo que exija la autenticación del cliente, deberá habilitar la capa de sockets seguros (SSL) para el sitio Web en el que haya establecido los servicios en línea de RMS y configurar el método de autenticación en los servicios de Internet Information Server (IIS). Puede seguir los pasos siguientes para llevar a cabo esta tarea:

1.  Abra **Administrador de servicios de Internet Information Server**.
2.  Expanda el elemento del servidor, haga clic con el botón secundario en la carpeta del sitio Web y, a continuación, haga clic en **Propiedades**.
3.  Haga clic en la ficha **Seguridad de directorios** y, luego, en el área **Comunicaciones seguras**, seleccione la casilla de verificación **Habilitar el asignador de servicios de directorio de Windows**.
4.  Expanda la carpeta del sitio Web, abra el directorio virtual **\_wmcs** y, a continuación, expanda el directorio virtual (**Licencia** o **Certificación**) para el que desea configurar la autenticación.
    -   Para configurar la autenticación cuando un usuario solicita una licencia de uso, haga clic con el botón secundario en el archivo license.asmx y, a continuación, haga clic en **Propiedades**.
    -   Para configurar la autenticación cuando un usuario solicita un certificado de usuario, haga clic con el botón secundario en el archivo certification.asmx y, a continuación, haga clic en **Propiedades**.
5.  Haga clic en la ficha **Seguridad de archivo** y, a continuación, en el área **Comunicaciones seguras**, haga clic en **Editar** para abrir el cuadro de diálogo **Comunicaciones seguras**.
6.  Seleccione **Requerir canal seguro (SSL)** y, a continuación, haga clic en una de las opciones siguientes:
    -   **Requerir certificados de cliente** si sólo desea que los clientes con certificados de cliente como tarjetas inteligentes puedan conectarse al servicio.
    -   **Aceptar certificados de cliente** si desea que los clientes puedan proporcionar credenciales de autenticación mediante un certificado de tarjeta inteligente o un nombre de usuario y una contraseña.
7.  Seleccione **Habilitar asignación de certificado de cliente** y, a continuación, haga clic en **Aceptar**.
8.  Si desea utilizar la autenticación de cliente para la certificación y las licencias, repita este procedimiento seleccionando el otro directorio virtual la segunda vez.

Una vez definida esta configuración, cuando un usuario intente abrir contenido protegido con RMS publicado por este servidor, se le pedirá que proporcione credenciales de autenticación para que el servidor pueda proporcionarle un certificado de cuenta de permisos o una licencia de uso.
