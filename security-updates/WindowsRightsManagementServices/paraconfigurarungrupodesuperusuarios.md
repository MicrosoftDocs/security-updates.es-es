---
TOCTitle: Para configurar un grupo de superusuarios
Title: Para configurar un grupo de superusuarios
ms:assetid: 'f2ef847e-2824-471f-9079-5c343094aba8'
ms:contentKeyID: 18128022
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747798(v=WS.10)'
---

Para configurar un grupo de superusuarios
=========================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

Para poder designarlo como grupo de superusuarios de RMS, el grupo debe existir en Active Directory y sus propiedades deben incluir una dirección de correo electrónico (especificada como nombre completo de dominio) que sea igual que el nombre de cuenta.

Configuración de un grupo de superusuarios
------------------------------------------

#### Para configurar un grupo de superusuarios

1.  Abra la página **Administración global** y, a continuación, junto al sitio Web en el que desee configurar un grupo de superusuarios, haga clic en **Administrar RMS en este sitio Web**.

2.  En el área **Vínculos de administración**, haga clic en **Configuración de seguridad**.

3.  En el área **Superusuarios**, haga clic en **Habilitar** para agregar un grupo de superusuarios.

4.  En **Nombre del grupo de superusuarios**, escriba el nombre de domino completo, con el formato *nombre\_grupo*@*nombre\_dominio.com*, de un grupo existente en este bosque de Active Directory a cuyos miembros se concederán permisos de propietario para todos los documentos protegidos con RMS y, a continuación, haga clic en **Guardar**.

    Para deshabilitar los permisos del grupo de superusuarios, haga clic en **Deshabilitar**.

Para obtener más información acerca de cómo realizar este procedimiento, vea "[Uso del grupo de superusuarios](https://technet.microsoft.com/0febcb3e-7124-4e51-971a-1013b928d33b)", anteriormente en este tema.
