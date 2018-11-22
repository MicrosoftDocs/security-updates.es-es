---
TOCTitle: Para especificar la ubicación de las plantillas de directiva de permisos
Title: Para especificar la ubicación de las plantillas de directiva de permisos
ms:assetid: 'e1bee46d-33db-424f-ba45-1dcedcb883ab'
ms:contentKeyID: 18127998
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747781(v=WS.10)'
---

Para especificar la ubicación de las plantillas de directiva de permisos
========================================================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

Si almacena plantillas de directiva de permisos en una carpeta compartida y, a continuación, cambia la ubicación de la carpeta compartida, deberá copiar manualmente las plantillas de directiva de permisos desde la ubicación actual a la nueva.

Las plantillas de directiva de permisos se almacenan también en la base de datos de configuración. Para obtener más información sobre la distribución de plantillas de directiva de permisos, vea "[Distribución de plantillas de directiva de permisos](https://technet.microsoft.com/ae6fa26f-d744-4ac9-9eb1-728ffab87bfe)", anteriormente en este tema.

Si utiliza Microsoft Office 2003 como aplicación compatible con RMS, la ubicación de las plantillas de directiva de permisos la controla la clave del registro `AdminTemplatePath` y el cliente de RMS intentará localizar plantillas en la ubicación especificada en la clave del registro en vez de cualquier otra ubicación.

Especificación de la ubicación de las plantillas de directiva de permisos
-------------------------------------------------------------------------

#### Para especificar la ubicación de las plantillas de directiva de permisos

1.  Abra la página **Administración global** y, a continuación, junto al sitio Web en el que desea especificar la ubicación de las plantillas de directiva de permisos, haga clic en **Administrar RMS en este sitio Web**.

2.  En el área **Vínculos de administración**, haga clic en **Plantillas de directiva de permisos**.

3.  En el área **Ubicación de la plantilla**, especifique la UNC (convención de nomenclatura universal) de una carpeta compartida donde se almacenarán las plantillas de directiva de permisos para este clúster, con el formato \\\\*nombre\_servidor*\\*nombre\_recurso\_compartido*. La cuenta que ejecuta el grupo de aplicaciones **Admin** debe tener permiso de escritura para la carpeta compartida. Asegúrese de que las plantillas estén almacenadas en una ubicación accesible de la red que cumpla las instrucciones de seguridad de la organización. Las carpetas compartidas para plantillas no deben crearse en las carpetas principales que utiliza RMS, como la carpeta Archivos de programa o las carpetas IISRoot.

4.  Haga clic en **Guardar**.

5.  Después de crear plantillas de directiva de permisos y guardarlas en esta ubicación, debe ponerlas a disposición de los usuarios. De forma predeterminada, el cliente de RMS busca las plantillas de directiva de permisos en la siguiente ubicación del equipo local:

    %HOMEPATH%\\Local Settings\\Application Data\\Microsoft\\DRM\\templates

    Las plantillas de directiva de permisos deben copiarse de la ubicación especificada en el paso 3 a esta ubicación para todos los usuarios de la organización que vayan a utilizar RMS.
