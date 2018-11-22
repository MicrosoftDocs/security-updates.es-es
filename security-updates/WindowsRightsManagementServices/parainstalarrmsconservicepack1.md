---
TOCTitle: Para instalar RMS con Service Pack 1
Title: Para instalar RMS con Service Pack 1
ms:assetid: 'dab20175-a690-43f8-b943-768d289daa0d'
ms:contentKeyID: 18127977
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747689(v=WS.10)'
---

Para instalar RMS con Service Pack 1
====================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

El equipo en el que instale RMS debe ser un servidor miembro de un dominio o un controlador de dominio. No es posible implementar RMS en un servidor independiente de un grupo de trabajo.

> [!IMPORTANT]
> No establezca los servicios en línea de RMS en ningún otro servidor hasta haber completado tanto la instalación como el establecimiento de servicios en línea en el primer servidor de certificación raíz. Para obtener instrucciones, vea "[Para establecer los servicios en línea en el primer servidor de certificación raíz](https://technet.microsoft.com/debc42f3-74ff-4c99-b7a4-4921fccdabc2)", "[Para establecer los servicios en línea en un servidor de licencias](https://technet.microsoft.com/4d67b898-0ba9-4eef-ab7d-ee0ca55a688e)" o "[Para agregar un servidor a un clúster](https://technet.microsoft.com/db635238-5528-4bec-9cc6-8244e2b3d733)", más adelante en este tema. 

> [!IMPORTANT]
> SP1 de RMS puede instalarse en un servidor que esté ejecutando la versión anterior de RMS. No obstante, si ha retirado RMS, RMS debe quitarse por completo mediante la opción Agregar o quitar programas antes de intentar instalar RMS SP1. 

Instalación de RMS con Service Pack 1
-------------------------------------

#### Para instalar RMS con Service Pack 1

1.  En el servidor en el que desea instalar RMS SP1, inicie sesión con una cuenta de dominio que sea miembro del grupo local Administradores.

2.  Cuando aparezca el cuadro de diálogo debienvenida, revise la lista de software que se va a instalar y, a continuación, haga clic en **Siguiente**.

3.  En el cuadro de diálogo **Contrato de licencia**, revise el contrato, seleccione **Acepto** y haga clic en **Siguiente**.

4.  En **Carpeta**, acepte la carpeta predeterminada o especifique una nueva carpeta y, a continuación, haga clic en **Siguiente**.

5.  En el cuadro de diálogo **Confirmación de instalación**, haga clic en **Instalar** para iniciar la instalación.

6.  Cuando aparezca el cuadro de diálogo **Instalación completa**, haga clic en **Cerrar**.

    > [!NOTE]
    > Si aparece un mensaje de error indicando que la aplicación se va a reiniciar, actualice la página **Administración global** en Microsoft Internet Explorer. 

También puede instalar RMS desde el símbolo del sistema. Para obtener instrucciones, vea "[Instalación de símbolo del sistema del servidor RMS](https://technet.microsoft.com/b55b1e2a-dd14-4168-a37f-9cdedbec660b)", más adelante en este tema.
