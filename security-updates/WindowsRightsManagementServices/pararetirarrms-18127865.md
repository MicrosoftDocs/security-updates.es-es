---
TOCTitle: Para retirar RMS
Title: Para retirar RMS
ms:assetid: '8b563c25-17cd-4b9b-ae42-695497ab6439'
ms:contentKeyID: 18127865
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747665(v=WS.10)'
---

Para retirar RMS
================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

| ![](images/Cc747665.Warning(WS.10).gif)Advertencia                                                    |
|------------------------------------------------------------------------------------------------------------------------------------|
| Cuando se retira un servidor, no es posible restaurar en él una configuración de RMS estándar. Este procedimiento es irreversible. |

| ![](images/Cc747665.Warning(WS.10).gif)Advertencia                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Una vez retirado, RMS debe quitarse por completo mediante la opción Agregar o quitar programas antes de intentar instalar otra instancia de RMS. |

Retiro de RMS
-------------

#### Para retirar RMS

1.  Inicie sesión en el servidor en el que desee retirar RMS.

2.  Abra la página **Administración global** y, a continuación, haga clic en el vínculo **Administrar RMS en este sitio Web**.

3.  En la **página principal de administración**, haga clic en el vínculo **Configuración de seguridad**.

4.  En el área **Retiro de RMS**, active la casilla de verificación **Habilitar el retiro de la instalación de RMS** y, a continuación, haga clic en **Retirar**.

5.  Cuando el sistema lo solicite, haga clic en **Aceptar** para confirmar que desea retirar permanentemente la instalación de RMS.
