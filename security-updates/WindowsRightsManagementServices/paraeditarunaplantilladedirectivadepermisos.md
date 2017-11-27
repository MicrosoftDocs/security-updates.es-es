---
TOCTitle: Para editar una plantilla de directiva de permisos
Title: Para editar una plantilla de directiva de permisos
ms:assetid: '9580b934-bd6f-4097-9d3c-4fc14a3147fa'
ms:contentKeyID: 18127877
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747684(v=WS.10)'
---

Para editar una plantilla de directiva de permisos
==================================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

Modificación de una plantilla de directiva de permisos
------------------------------------------------------

#### Para editar una plantilla de directiva de permisos

1.  Abra la página **Administración global** y, a continuación, junto al sitio Web en el que desee editar una plantilla de directiva de permisos, haga clic en **Administrar RMS en este sitio Web**.

2.  En el área **Vínculos de administración**, haga clic en **Plantillas de directiva de permisos**.

3.  En **Nombre de la plantilla**, haga clic en el nombre de la plantilla que va a editar.

4.  En el área **Identificación de la plantilla**, modifique la información de las áreas **Nombre de la plantilla**, **Descripción de la plantilla** y **Dirección URL de solicitud de permisos** según sea necesario.

5.  En el área **Usuarios y grupos**, realice uno o varios de los siguientes procedimientos:

    -   Para agregar un usuario o grupo, en **Agregar usuarios o grupos**, escriba la dirección de correo electrónico de un usuario o grupo específico que vaya a agregar, haga clic en **Agregar** y, a continuación, seleccione el nombre en **Usuarios o grupos actuales**. En el área **Permisos**, seleccione todos los permisos que se concederán al usuario o grupo seleccionado.
    -   Para modificar los permisos de un usuario o grupo existente, seleccione el nombre en **Usuarios o grupos actuales** y, a continuación, active o desactive las casillas de verificación de los permisos según sea necesario.
    -   Para quitar un usuario o grupo, seleccione el nombre en **Usuarios o grupos actuales** y, a continuación, haga clic en **Quitar**.

6.  En el área **Directiva de caducidad**, edite la información para cambiar cuándo caducan las licencias de contenido y cuándo deben renovarse, según sea necesario.

7.  En el área **Directiva extendida**, edite la información para cambiar cómo se implementarán las licencias de contenido, incluida la persistencia de los permisos de autor, si se admitirán exploradores de confianza, la persistencia de la licencia dentro del contenido y la exigencia de cualquier dato específico de la aplicación, según sea necesario.

8.  En el área **Directiva de revocación**, seleccione si será necesaria una lista de revocaciones para el contenido creado con esta plantilla. Si selecciona **Requerir revocación**, especifique las siguientes opciones de configuración, según sea necesario:

    -   En **Dirección URL**, escriba la dirección URL a la que se envía el archivo de lista de revocaciones. Si necesita dar soporte a usuarios desconectados o usuarios externos, esta dirección URL debe resultar accesible tanto desde la red corporativa como desde Internet. Para obtener más información acerca de la revocación, vea "[Implementación de revocaciones](https://technet.microsoft.com/4735f060-7197-4ae2-830a-f91bcc4de30a)", anteriormente en este tema.
    -   En **Intervalo de actualización de la lista de revocaciones**, escriba el número de días durante los cuales la lista de revocaciones continúa siendo válida. Si un usuario tiene una copia de la lista de revocaciones más antigua que este valor, el usuario debe obtener una lista de revocaciones actualizada para utilizar el contenido.
    -   En **Archivo de clave pública**, escriba la ruta de acceso y el nombre del archivo de clave pública de la lista de revocaciones. Para obtener más información acerca de este archivo, vea "Inserción de una firma en una lista de revocaciones", anteriormente en este tema.

    > [!CAUTION]
    > Tenga cuidado al implementar revocaciones. En función del intervalo de actualización que especifique, deberá renovar periódicamente la lista de revocaciones o caducará automáticamente, lo que impedirá que los usuarios utilicen el contenido que requiere esa lista. Para asegurarse de que no impide inadvertidamente que los usuarios utilicen contenido, evalúe detenidamente el intervalo necesario para actualizar la lista de revocaciones. Para obtener más información, vea "[Administración de revocaciones](https://technet.microsoft.com/df732a7d-1fb0-4845-87ca-fab4bc5f98a0)", anteriormente en este tema. 

9.  Haga clic en **Enviar**.

Para obtener más información sobre cómo realizar este procedimiento, vea "[Creación y modificación de plantillas de directiva de permisos](https://technet.microsoft.com/6014176f-ef71-4d29-b3e3-da129c18563d)", anteriormente en este tema.
