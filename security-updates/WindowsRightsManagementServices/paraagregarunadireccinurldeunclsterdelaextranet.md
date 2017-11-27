---
TOCTitle: Para agregar una dirección URL de un clúster de la extranet
Title: Para agregar una dirección URL de un clúster de la extranet
ms:assetid: '12c83186-ce9e-4100-bbd1-d87a885331c7'
ms:contentKeyID: 18127688
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720193(v=WS.10)'
---

Para agregar una dirección URL de un clúster de la extranet
===========================================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

No olvide registrar la dirección URL en el Sistema de nombres de dominio (Domain Name System, DNS), comprobar que funciona y que está disponible desde la extranet de Internet. Si habilita SSL para los archivos de los servicios Web, debe especificar HTTPS para la dirección URL del clúster.

Si va a agregar una dirección URL de clúster de extranet a un servidor de RMS que ya esté en servicio, los clientes RMS actuales deben obtener nuevos certificados emisores de licencias de cliente para tener acceso al clúster de extranet a fin de obtener licencias.

Adición de una dirección URL de clúster de extranet
---------------------------------------------------

#### Para agregar una dirección URL de clúster de extranet

1.  Abra la página **Administración global** y, a continuación, junto al sitio Web al que desee agregar la dirección URL de un clúster de la extranet, haga clic en **Administrar RMS en este sitio Web**.

2.  En el área **Vínculos de administración**, haga clic en **Configuración de la dirección URL de clúster de extranet**.

3.  En el área **Dirección URL de clúster de extranet**, especifique la dirección URL de la que desea que los usuarios externos adquieran licencias. También puede seleccionar HTTP o HTTPS.

4.  Haga clic en **Enviar**.
