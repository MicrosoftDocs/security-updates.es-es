---
TOCTitle: Para exportar un dominio de publicación de confianza
Title: Para exportar un dominio de publicación de confianza
ms:assetid: '3fb138dd-e324-43f8-97e0-da0027a036a3'
ms:contentKeyID: 18127721
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720252(v=WS.10)'
---

Para exportar un dominio de publicación de confianza
====================================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

Exportación de un dominio de publicación de confianza
-----------------------------------------------------

#### Para exportar un dominio de publicación de confianza

1.  Abra la página **Administración global** y, a continuación, junto al sitio Web en el que desee agregar un dominio de publicación de confianza, haga clic en **Administrar RMS en este sitio Web**.

2.  En el área **Vínculos de administración**, haga clic en **Directivas de confianza**.

3.  En la página **Directivas de confianza**, en el área **Dominios de publicación de confianza**, haga clic en **Exportar** junto al contenedor de la clave para este servidor de RMS.

4.  Aparecerá el cuadro de diálogo **Exportación del dominio de publicación de confianza**.

5.  Escriba la contraseña que se utilizará para cifrar el archivo de dominio de publicación de confianza. Necesitará esta contraseña para importar este archivo en otro servidor de RMS. La contraseña debe ser segura.

6.  Vuelva a introducir la contraseña para confirmar que ha introducido la contraseña que desea utilizar.

7.  Introduzca la ruta de acceso y el nombre del archivo que se utilizará para el archivo de dominio de publicación de confianza .xml. Asegúrese de especificar la extensión de archivo .xml.

8.  Haga clic en **Exportar** para crear el archivo de dominio de publicación de confianza.

Para obtener más información sobre cómo realizar este procedimiento, vea "[Adición y desinstalación de dominios de publicación de confianza](https://technet.microsoft.com/d87b502d-5497-4ccd-badf-f6807d587cee)", anteriormente en este tema.
