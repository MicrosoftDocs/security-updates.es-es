---
TOCTitle: Establecimiento de permisos de directorio virtual
Title: Establecimiento de permisos de directorio virtual
ms:assetid: '45112111-9608-45b1-9a86-7b313d0a1579'
ms:contentKeyID: 18127795
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747549(v=WS.10)'
---

Establecimiento de permisos de directorio virtual
=================================================

Una vez habilitado el retiro, está disponible como servicio. No obstante, el servicio de retiro es un directorio virtual de IIS con permisos de acceso asociados. Para que los usuarios puedan utilizar el servicio, deberá establecer permisos en el directorio virtual y en el archivo real, decommission.asmx.

De forma predeterminada, la autenticación de Windows integrada está habilitada para el directorio virtual, pero tan sólo las cuentas del sistema y de administrador tienen acceso al archivo real. Al especificar los permisos para la DACL del archivo decommission.asmx, puede conceder el acceso a un grupo específico de usuarios de confianza para quitar la protección con RMS o puede permitir que todo el mundo acceda al servicio.

Antes de que los usuarios puedan empezar a utilizar el servicio de retiro, es preciso modificar la aplicación del usuario para que se puedan enviar solicitudes de una licencia de uso a este nuevo conducto de retiro. En el sistema Microsoft Office 2003, esto se hace agregando una entrada de registro en el equipo del usuario. Si utiliza Office 2003, puede seguir este procedimiento para llevar a cabo este paso:

1.  Abra el Editor del Registro.
2.  Desplácese a `HKEY_CURRENT_USER\Software\Microsoft\Office\11.0\Common\DRM` y agregue una nueva clave con el nombre `Retiro`.
3.  Bajo la clave Retiro, agregue la nueva entrada **Valor de la cadena** que se indica a continuación, reemplazando *su-servidor-de-licencias* por el nombre del servidor de RMS:  
    `http://`*su-servidor-de-licencias*`/_wmcs/licensing`
4.  A continuación, haga clic con el botón secundario del mouse en la entrada y seleccione **Modificar** para especificar los datos del valor para que haga referencia al servicio de retiro:  
    `http://`*su-servidor-de-licencias*`/_wmcs/decommission`

> [!NOTE]
> Pueden existir múltiples entradas para esta clave cuando hay varios servidores de RMS en la organización en modo de retiro. 
