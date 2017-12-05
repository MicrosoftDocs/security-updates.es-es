---
TOCTitle: Para habilitar la certificación de dispositivos móviles
Title: Para habilitar la certificación de dispositivos móviles
ms:assetid: '93ec088e-9056-4c3c-bd97-1173fb194578'
ms:contentKeyID: 18127875
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747603(v=WS.10)'
---

Para habilitar la certificación de dispositivos móviles
=======================================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Este procedimiento sólo es aplicable en el clúster de certificación raíz.

Este procedimiento supone que ha creado un grupo de usuarios que contiene las cuentas de usuarios de dispositivos móviles que utilizan contenido protegido por RMS.

Habilitación de la certificación de dispositivos móviles
--------------------------------------------------------

#### Para habilitar la certificación de dispositivos móviles

1.  En el servidor de certificación raíz, abra un explorador de sistema de archivos y vaya a la carpeta &lt;unidad del sistema&gt;:\\Inetpub\\wwwroot\\\_wmcs\\Certification.

2.  Para que los dispositivos móviles puedan recibir certificados de cuenta de permisos (RAC), haga clic con el botón secundario del mouse en el archivo MobileDeviceCertification.asmx y, a continuación, haga clic en **Propiedades**.

3.  En la ficha **Seguridad**, haga clic en **Agregar** y agregue el grupo que ha creado para esta categoría de usuarios y el grupo de servicio de RMS (**RMS Service Group**).

4.  En la lista **Permisos** de los grupos, seleccione la casilla de verificación **Permitir** para los permisos de **lectura** y de **lectura& y ejecución** y, a continuación, haga clic en **Aceptar**.
