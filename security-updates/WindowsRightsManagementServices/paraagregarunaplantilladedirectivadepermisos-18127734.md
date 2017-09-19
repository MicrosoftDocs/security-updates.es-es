---
TOCTitle: Para agregar una plantilla de directiva de permisos
Title: Para agregar una plantilla de directiva de permisos
ms:assetid: '1a5555cd-6d39-4078-a879-4106864674be'
ms:contentKeyID: 18127734
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720206(v=WS.10)'
---

Para agregar una plantilla de directiva de permisos
===================================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

Adición de una plantilla de directiva de permisos
-------------------------------------------------

#### Para agregar una plantilla de directiva de permisos

1.  Abra la página **Administración global** y, a continuación, junto al sitio Web al que desee agregar una plantilla de directiva de permisos, haga clic en **Administrar RMS en este sitio Web**.

2.  En el área **Vínculos de administración**, haga clic en **Plantillas de directiva de permisos**.

3.  En **Idioma**, haga clic para seleccionar qué idioma desea que utilice la plantilla.

4.  Haga clic en **Agregar una plantilla de directiva de permisos**.

5.  En el área **Identificación de la plantilla**, especifique un nombre, una descripción y una dirección URL de solicitud de permisos para la plantilla.

6.  En el área **Usuarios y grupos**, en **Agregar usuarios o grupos**, escriba la dirección de correo electrónico válida de un usuario o grupo que vaya a agregar y, a continuación, haga clic en **Agregar**. Repita este proceso para agregar usuarios o grupos adicionales, según sea necesario.

7.  En **Usuarios o grupos actuales**, seleccione la dirección de correo electrónico de un usuario o grupo al que vaya a asignar permisos.

8.  Active las casillas de verificación de todos los permisos que se concederán al usuario o grupo seleccionado. Repita este proceso para conceder permisos a los restantes usuarios y grupos.

9.  En el área **Directiva de caducidad**, seleccione una de las tres opciones de caducidad y, a continuación, especifique una fecha u hora de caducidad, según sea lo adecuado. Si es necesario, seleccione **Las licencias de uso del contenido deben renovarse cada** y especifique el número de días entre renovaciones.

10. En el área **Directiva extendida**, seleccione una o varias de las cuatro opciones disponibles. Si selecciona **Exigir datos específicos de la aplicación**, especifique un nombre y un valor para los datos que se deben exigir y, a continuación, haga clic en **Agregar**.

11. Para implementar revocaciones, en el área **Directiva de revocación**, active la casilla de verificación **Requerir revocación** y, a continuación, siga estos pasos:

    1.  En **Dirección URL o UNC**, escriba la dirección URL a la que se envía el archivo de lista de revocaciones. Si necesita dar soporte a usuarios desconectados o usuarios externos, esta dirección URL debe resultar accesible tanto desde la red corporativa como desde Internet.
    2.  En **Intervalo de actualización de la lista de revocaciones**, escriba el número de días durante los cuales la lista de revocaciones continúa siendo válida. Si un usuario tiene una copia de la lista de revocaciones más antigua que este valor, el usuario debe obtener una lista de revocaciones actualizada para utilizar el contenido.
    3.  En **Archivo de clave pública**, escriba la ruta de acceso y el nombre de archivo o haga clic en **Examinar** para buscar el archivo de clave pública de la lista de revocaciones. Para obtener más información acerca de este archivo, vea "Inserción de una firma en una lista de revocaciones", anteriormente en este tema.

    | ![](images/Cc720206.Caution(WS.10).gif)Precaución                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
    |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Tenga cuidado al implementar revocaciones. En función del intervalo de actualización que especifique, deberá renovar periódicamente la lista de revocaciones o caducará automáticamente, lo que impedirá que los usuarios utilicen el contenido que requiere esa lista. Para asegurarse de que no impide inadvertidamente que los usuarios utilicen contenido, evalúe detenidamente el intervalo necesario para actualizar la lista de revocaciones. Para obtener más información, vea "[Administración de revocaciones](https://technet.microsoft.com/df732a7d-1fb0-4845-87ca-fab4bc5f98a0)", anteriormente en este tema. |

12. Haga clic en **Enviar**.

Para obtener más información sobre las revocaciones, vea "[Administración de revocaciones](https://technet.microsoft.com/df732a7d-1fb0-4845-87ca-fab4bc5f98a0)", anteriormente en este tema.

Para obtener consideraciones acerca de la especificación de opciones de revocación, vea "[Definición de directivas de revocación](https://technet.microsoft.com/e2fffe9f-def7-439b-a8aa-43f8a065813d)", anteriormente en este tema.

Para obtener más información sobre cómo realizar este procedimiento, vea "[Creación y modificación de plantillas de directiva de permisos](https://technet.microsoft.com/6014176f-ef71-4d29-b3e3-da129c18563d)", anteriormente en este tema.
