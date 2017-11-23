---
TOCTitle: Para especificar el contacto administrativo
Title: Para especificar el contacto administrativo
ms:assetid: '31777458-5530-4ae0-ac1f-131b3d98dd35'
ms:contentKeyID: 18127777
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720237(v=WS.10)'
---

Para especificar el contacto administrativo
===========================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

El administrador especificado en este procedimiento debe ser un administrador local en el servidor de certificación raíz, ya que el usuario que inicie sesión debe tener permisos en el archivo SubEnrollService.asmx del servidor de certificación raíz para que se puedan establecer los servicios en línea en un servidor de licencias. En caso de que el usuario intente establecer los servicios en línea en un servidor de licencias no tenga permisos sobre este archivo, el usuario puede enviar una solicitud al administrador designado en esta operación, para que conceda a la cuenta de usuario los permisos necesarios. Para obtener más información, vea "[Establecimiento de permisos en el archivo del servicio de subinscripción](https://technet.microsoft.com/737bb69b-fe26-4057-9569-e632f7bbf295)", anteriormente en este tema.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

Especificación del contacto administrativo
------------------------------------------

#### Para especificar el contacto administrativo

1.  Abra la página **Administración global** y, a continuación, junto al sitio Web en el que desee especificar un contrato administrativo, haga clic en **Administrar RMS en este sitio Web**.

2.  En el área **Vínculos de administración**, haga clic en **Configuración de certificación**.

3.  En el área **Contacto administrativo**, escriba la dirección de correo electrónico del administrador de contacto en caso de que surjan problemas de subinscripción durante el establecimiento de servicios en línea en un servidor de licencias, con el formato *nombre\_usuario*@*nombre\_dominio*.com.

4.  En la parte inferior de la página, haga clic en **Enviar**.
