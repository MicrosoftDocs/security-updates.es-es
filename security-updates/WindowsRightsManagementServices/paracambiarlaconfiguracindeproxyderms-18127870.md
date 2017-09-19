---
TOCTitle: Para cambiar la configuración de proxy de RMS
Title: Para cambiar la configuración de proxy de RMS
ms:assetid: '8f50bd4d-26b1-4996-b361-722ee21607f3'
ms:contentKeyID: 18127870
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747594(v=WS.10)'
---

Para cambiar la configuración de proxy de RMS
=============================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para obtener más información acerca de los métodos de autenticación del servidor y de cómo funcionan en Windows Server 2003, vea la Ayuda de Internet Information Server (IIS).

Cambio de la configuración de proxy de RMS
------------------------------------------

#### Para cambiar la configuración de proxy de RMS

1.  Abra la página **Administración global** y, a continuación, haga clic en **Administrar RMS en este sitio Web**.

2.  En **Administración de clúster**, haga clic en **Configuración de seguridad**.

3.  Si no ha utilizado previamente un servidor proxy con RMS, seleccione la casilla de verificación **Este equipo utiliza un servidor proxy para conectarse a Internet**. La página mostrará opciones de configuración adicionales para que las complete.

4.  En el cuadro **Dirección**, escriba la dirección IP o el nombre DNS del servidor proxy que desee utilizar.

5.  En el cuadro **Puerto**, escriba el número de puerto que el servidor proxy use para conectarse a Internet.

6.  Si no utiliza el servidor proxy para conectarse a recursos locales, seleccione la casilla de verificación **Omitir servidor proxy para direcciones locales**.

7.  Si corresponde, seleccione la casilla de verificación **Este servidor proxy requiere autenticación**.

    -   Elija el tipo de autenticación de la lista: **Básica**, **De texto implícita** o **De Windows integrada**.
    -   En **Nombre de usuario**, escriba el nombre de usuario que debe proporcionarse como respuesta al desafío del servidor proxy.
    -   En **Contraseña**, escriba la contraseña que debe proporcionarse como respuesta al desafío del servidor proxy.
    -   En **Confirmar contraseña**, vuelva a escribir la contraseña anterior para comprobar que la ha escrito correctamente.
    -   Si el servidor proxy utiliza autenticación de Windows integrada, en **Dominio**, escriba el dominio al que pertenezca el usuario.

8.  Haga clic en **Enviar**.
