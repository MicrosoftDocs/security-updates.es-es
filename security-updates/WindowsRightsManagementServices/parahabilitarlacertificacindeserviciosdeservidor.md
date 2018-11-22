---
TOCTitle: Para habilitar la certificación de servicios de servidor
Title: Para habilitar la certificación de servicios de servidor
ms:assetid: '0ed78c85-7acb-4e3b-a594-613f8ccb5b14'
ms:contentKeyID: 18127726
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720196(v=WS.10)'
---

Para habilitar la certificación de servicios de servidor
========================================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que forme parte del grupo Administradores. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Este procedimiento sólo es aplicable en el clúster raíz.

Este procedimiento supone que ha creado un grupo de usuarios que contiene las cuentas de usuarios que los servicios de servidor suplantarán cuando utilicen contenido protegido por derechos.

Habilitación de la certificación de servicios de servidor
---------------------------------------------------------

#### Para habilitar la certificación de servicios de servidor

1.  Inicie sesión en el equipo como un miembro del grupo local de administradores.

2.  Abra un explorador de sistema de archivos y vaya a la carpeta &lt;unidad del sistema&gt;:\\Inetpub\\wwwroot\\\_wmcs\\Certification.

3.  Para que los servicios de servidor reciban certificados de cuenta de permisos (RAC), haga clic con el botón secundario del mouse en el archivo ServerCertification.asmx y, a continuación, haga clic en **Propiedades**.

4.  En la ficha **Seguridad**, haga clic en **Agregar** y agregue el grupo que ha creado para esta categoría de usuarios y el grupo de servicio de RMS (**RMS Service Group**).

5.  En las listas **Permisos** de los grupos, seleccione la casilla de verificación **Permitir** para los permisos de **Lectura & ejecución** y, a continuación, haga clic en **Aceptar**.

6.  Los pasos del 1 al 4 se deben repetir para cada servidor del clúster.

> [!NOTE]
> Para Microsoft Exchange Server 2007, debe agregar cada objeto de equipo de Active Directory del servidor cabeza de puente a la lista de control de acceso discrecional (DACL) de ServerCertification.asmx. Asimismo, para Microsoft Office SharePoint Server 2007, debe agregar el objeto de equipo de Active Directory del servidor Office SharePoint Server 2007 a esta DACL. Se recomienda agregar un grupo de seguridad a esta DACL y agregar los objetos de equipo apropiados a éste. 
