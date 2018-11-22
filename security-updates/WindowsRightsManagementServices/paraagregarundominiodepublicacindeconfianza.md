---
TOCTitle: Para agregar un dominio de publicación de confianza
Title: Para agregar un dominio de publicación de confianza
ms:assetid: '731416d8-ddf4-4d4a-9f1a-bbd1ea48fe3c'
ms:contentKeyID: 18127809
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747624(v=WS.10)'
---

Para agregar un dominio de publicación de confianza
===================================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

Si utiliza un módulo de seguridad de hardware para proteger la clave privada de RMS y desea importar un certificado emisor de licencias de servidor desde una instalación de RMS que utilice protección de clave privada de software, debe especificar una contraseña para la clave privada en la página **Configuración de seguridad** de cada servidor de RMS del clúster antes de intentar importar el certificado.

Adición de dominios de publicación de confianza
-----------------------------------------------

#### Para agregar un dominio de publicación de confianza

1.  Abra la página **Administración global** y, a continuación, junto al sitio Web en el que desee agregar un dominio de publicación de confianza, haga clic en **Administrar RMS en este sitio Web**.

2.  En el área **Vínculos de administración**, haga clic en **Directivas de confianza**.

3.  En el área **Dominios de publicación de confianza**, haga clic en **Examinar**. Haga doble clic en el certificado del dominio de publicación que desee agregar. En **Contraseña para descifrar el archivo que se está importando**, escriba la contraseña necesaria para descifrar este archivo y, a continuación, haga clic en **Importar**.

    El archivo cifrado con contraseña contiene el certificado emisor de licencia, la clave privada (si la clave se almacena en software) y plantillas de directiva de permisos.

4.  El nombre del dominio aparece en la lista **Dominios de publicación de confianza**.

Para obtener más información sobre cómo realizar este procedimiento, vea "[Adición y desinstalación de dominios de publicación de confianza](https://technet.microsoft.com/d87b502d-5497-4ccd-badf-f6807d587cee)", anteriormente en este tema.
