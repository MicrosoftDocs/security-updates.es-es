---
TOCTitle: Uso de la página Administración global
Title: Uso de la página Administración global
ms:assetid: '57bbf402-2351-4dee-823c-27f4dd32447c'
ms:contentKeyID: 18127821
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747575(v=WS.10)'
---

Uso de la página Administración global
======================================

En la página **Administración global** del sitio Web de administración, puede establecer los servicios en línea de un servidor de RMS y anularlos, así como cambiar la cuenta de servicio de RMS.

Para obtener acceso a esta página Web desde el servidor que desee administrar, siga estos pasos:

1.  Inicie sesión como administrador local.
2.  Haga clic en **Inicio**, seleccione **Todos los programas**, **Windows RMS** y haga clic en **Administración de Windows RMS**.

No es posible obtener acceso a la página **Administración global** desde un explorador que se encuentre en un equipo remoto.

Si todavía no ha establecido los servicios en línea en el servidor desde el cual esté obteniendo acceso a la página **Administración global**, aparecerán las siguientes opciones para cada sitio Web que se ejecute en el servidor:

-   **Establecer los servicios en línea de RMS en este sitio Web**. Haga clic en este vínculo si se trata del primer servidor del clúster donde desee establecer los servicios en línea. De esta manera, comienza el proceso de establecimiento de los servicios en línea, durante el cual se instalan los recursos de RMS, como los directorios virtuales. Asimismo, se instalan las bases de datos en el servidor de base de datos. Para obtener más información, vea "[Para establecer los servicios en línea en el primer servidor de certificación raíz](https://technet.microsoft.com/debc42f3-74ff-4c99-b7a4-4921fccdabc2)", más adelante en este tema.
-   **Agregar este servidor a un clúster**. Haga clic en este vínculo si desea establecer los servicios en línea en el servidor y agregarlo a un clúster existente. Puede unir un servidor al clúster de certificación raíz o a un clúster de licencias. Se instalan los recursos de RMS, como los directorios virtuales. Sin embargo, no se crean las bases de datos, puesto que este servidor utilizará las del clúster. Para obtener más información, vea “[Para agregar un servidor a un clúster](https://technet.microsoft.com/db635238-5528-4bec-9cc6-8244e2b3d733)”, más adelante en este tema.

Si obtiene acceso a la página **Administración global** desde un servidor donde ya se hayan establecido los servicios en línea, aparecerán las siguientes opciones:

-   **Administrar RMS en este sitio Web.**Haga clic en este vínculo para abrir la página Administración de clúster. Para obtener más información, vea “[Uso de la página principal de administración](https://technet.microsoft.com/6c155977-bd0e-47d6-ac65-1746cddb505e)”, más adelante en este tema.
-   **Cambiar la cuenta de servicio de RMS.**Haga clic en este vínculo para especificar una cuenta de servicio de RMS diferente con la que ejecutar RMS. Para obtener más información, vea “[Cambio de la cuenta de servicio de RMS](https://technet.microsoft.com/f257d66d-b823-41e4-bcb7-7c90eb295238)”, más adelante en este tema.
-   **Quitar RMS de este sitio Web.** Haga clic en este vínculo para anular los servicios en línea de RMS. Cuando anule los servicios en línea de RMS, se quitarán de este servidor las aplicaciones y los servidores virtuales de RMS, pero no se desinstalará RMS. Para obtener más información, vea “[Para desinstalar RMS](https://technet.microsoft.com/885e3b4f-ea32-466f-9f7f-d8440b0f7c28)”, más adelante en este tema.

> [!NOTE]
> El sitio Web de administración de RMS utiliza ventanas emergentes para la configuración de algunas funciones. Si utiliza un bloqueador de ventanas emergentes con el explorador Web, deberá configurar los valores del explorador para permitir que aparezcan las ventanas emergentes del sitio Web de administración de RMS. 
