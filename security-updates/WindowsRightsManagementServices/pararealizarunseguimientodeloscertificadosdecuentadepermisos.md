---
TOCTitle: Para realizar un seguimiento de los certificados de cuenta de permisos
Title: Para realizar un seguimiento de los certificados de cuenta de permisos
ms:assetid: 'f9efac9f-c725-4bce-a89f-7691b0d8ffc0'
ms:contentKeyID: 18128036
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747752(v=WS.10)'
---

Para realizar un seguimiento de los certificados de cuenta de permisos
======================================================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

Esta función sólo está disponible en el clúster de certificación raíz; no está disponible en ningún servidor ni clúster de licencias.

Este procedimiento sólo puede utilizarse para estimar el número de licencias de uso, y sólo es útil si son licencias facturables. El número que se muestra en la página Informe de certificación de cuentas de RM es una aproximación. Si no actualizó la base de datos de facturación para eliminar los usuarios que ya no están activos, este número no será correcto. Además, si tiene usuarios para los que se hayan emitido varias licencias en varios bosques, las licencias adicionales no se incluirán en el número que se muestra.

Seguimiento de certificados de cuenta de permisos
-------------------------------------------------

#### Para realizar un seguimiento de los certificados de cuenta de permisos

1.  Abra la página **Administración global** y, a continuación, junto al sitio Web en el que desea realizar el seguimiento de certificados, haga clic en **Administrar RMS en este sitio Web**.

2.  En el área **Vínculos de administración**, haga clic en Informe de certificación de cuentas de RM.

3.  En **Número total de usuarios certificados**, observe el número de usuarios que han recibido certificados de cuenta de permisos desde este clúster de certificación raíz.

Para obtener más información, vea "[Seguimiento de certificados de cuenta de permisos](https://technet.microsoft.com/5bb0f3cf-fc44-4e60-a93f-c789d6f8a902)", anteriormente en este tema.
