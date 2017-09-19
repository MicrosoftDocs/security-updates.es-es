---
TOCTitle: Para activar o desactivar el registro
Title: Para activar o desactivar el registro
ms:assetid: '8e672f95-566f-4070-9a2a-2f70f087148f'
ms:contentKeyID: 18127888
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747674(v=WS.10)'
---

Para activar o desactivar el registro
=====================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

Asegúrese de que el servidor de RMS dispone de conexión con el servidor de base de datos y de que el servicio de base de datos se ha iniciado antes de activar el registro. Si Message Queue Server no puede proporcionar los registros para la base de datos de registros, almacenará los datos en cola en el disco duro del servidor de RMS. Seguirá realizando esta operación hasta que no quede espacio libre de almacenamiento en el servidor. RMS no muestra ningún error en esta situación, ya que se supone que esta función permite el registro cuando la conexión con SQL Server está interrumpida.

Activación o desactivación del registro
---------------------------------------

#### Para activar o desactivar el registro

1.  Abra la página **Administración global** y, a continuación, junto al sitio Web en el que desee activar o desactivar el registro, haga clic en **Administrar RMS en este sitio Web**.

2.  En el área **Vínculos de administración**, haga clic en **Configuración de registro**.

3.  En el área **Servidor y base de datos de registro**, active la casilla de verificación **Activar registro** y, a continuación, haga clic en **Actualizar**.

    Para desactivar el registro, desactive la casilla de verificación y, a continuación, haga clic en **Actualizar**.

Para obtener más información sobre cómo realizar este procedimiento, vea "[Activación y desactivación del registro](https://technet.microsoft.com/50ccd827-2d39-41e7-a395-3d5f5836869b)", anteriormente en este tema.
