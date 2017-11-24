---
TOCTitle: Para anular los servicios en línea de RMS
Title: Para anular los servicios en línea de RMS
ms:assetid: '9fa63daa-5fb9-4afd-8371-b38248619857'
ms:contentKeyID: 18127894
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747706(v=WS.10)'
---

Para anular los servicios en línea de RMS
=========================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

Cuando se anulan los servicios en línea en un servidor, éste se quita de la tabla ClusterServer de la base de datos de configuración. Cuando se anulan los servicios en línea en el último servidor de un clúster, la base de datos de servicios de directorio se elimina del servidor SQL Server. Cuando anule servicios en línea en el último servidor de certificación raíz de un clúster, debe anular manualmente el registro del punto de conexión de servicio de certificación (SCP). La anulación de servicios en línea y la desinstalación no quitan el punto de conexión de servicio (SCP) de Active Directory.

Si decide desinstalar un servidor de certificación raíz antes de haber establecido los servicios en línea, se le advertirá de que todavía no se han anulado los servicios en línea en el sitio y de que no se quitará el SCP de Active Directory. No obstante, si selecciona **Sí** para continuar, se anularán los servicios en línea del sitio. La desinstalación no quita el punto de conexión de servicio de Active Directory.

Anulación de los servicios en línea de RMS
------------------------------------------

#### Para anular los servicios en línea de RMS

1.  Inicie sesión en el servidor en el que desee anular los servicios en línea de RMS.

2.  Abra la página **Administración global**.

3.  Junto al sitio Web donde están establecidos los servicios en línea de RMS, seleccione **Quitar RMS de este sitio Web** y haga clic en **Aceptar**.

4.  Haga clic en **Anular registro de URL** en la página Web Punto de conexión de servicio de RMS, para anular el registro de la conexión del servicio de certificación en Active Directory.
