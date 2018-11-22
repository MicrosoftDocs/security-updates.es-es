---
TOCTitle: Para exportar un dominio de usuario de confianza
Title: Para exportar un dominio de usuario de confianza
ms:assetid: '40281ba3-2674-43ca-aa6d-1deb9302eb0e'
ms:contentKeyID: 18127788
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720259(v=WS.10)'
---

Para exportar un dominio de usuario de confianza
================================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

Los dominios de usuarios de confianza permiten a un servidor de RMS proporcionar licencias a los usuarios cuyos certificados RAC habían sido concedidos por otro servidor de RMS.

Exportación de un dominio de usuario de confianza
-------------------------------------------------

#### Para exportar un dominio de usuario de confianza

1.  En la página **Directivas de confianza**, en el área **Dominios de usuarios de confianza**, haga clic en **Exportar**.

2.  Aparecerá el cuadro de diálogo **Descarga de archivos**. Haga clic en **Guardar**.

3.  Aparecerá el cuadro de diálogo **Guardar como**. Es recomendable modificar el nombre de archivo .bin de forma que incluya el nombre de su servidor, como por ejemplo RMS\_Server1\_LicensorCert.bin.

    De forma predeterminada, el archivo se guarda en el escritorio. Si lo desea, puede especificar una ubicación distinta.

4.  Haga clic en **Guardar** para guardar el archivo en la ubicación especificada.

Para obtener más información sobre cómo realizar este procedimiento, vea "[Adición y desinstalación de dominios de usuarios de confianza](https://technet.microsoft.com/7c440b15-01c4-49f1-b43c-00f67f3388c1)", anteriormente en este tema.
