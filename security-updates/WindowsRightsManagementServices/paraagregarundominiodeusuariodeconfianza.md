---
TOCTitle: Para agregar un dominio de usuario de confianza
Title: Para agregar un dominio de usuario de confianza
ms:assetid: 'ed672e58-6272-4ac0-a434-d1d938037e93'
ms:contentKeyID: 18128024
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747793(v=WS.10)'
---

Para agregar un dominio de usuario de confianza
===============================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

Adición de dominios de usuario de confianza
-------------------------------------------

#### Para agregar un dominio de usuario de confianza

1.  Abra la página **Administración global** y, a continuación, junto al sitio Web en el que desee agregar un dominio de usuario de confianza, haga clic en **Administrar RMS en este sitio Web**.

2.  En el área **Vínculos de administración**, haga clic en **Directivas de confianza**.

3.  En el área **Dominios de usuarios de confianza**, haga clic en **Examinar**, busque y haga doble clic en el certificado emisor de licencias de servidor del dominio de usuario que desee importar para establecer la relación de confianza y, a continuación, haga clic en **Agregar**.

    El nombre del dominio aparece en la lista **Dominios de usuarios de confianza**.

4.  Para especificar los dominios de correo electrónico del dominio de usuario de confianza en los que se confía, haga clic en **Dominios de confianza** junto al nombre del certificado en la lista para abrir la ventana **Dominios de correo electrónico de confianza**.

5.  Elija alguna de las siguientes opciones de confianza:

    -   Seleccione la opción **Confiar en todos los dominios de correo electrónico** para confiar en todas las cuentas de usuario que sean miembros de dicho dominio.
        O bien,
    -   Seleccione la opción **Confiar sólo en dominios de correo electrónico especificados**, escriba el nombre del dominio de confianza; por ejemplo, example.com, y haga clic en **Agregar**. Se agrega el dominio a la lista Dominios de correo electrónico de confianza. Para quitar un nombre de la lista, seleccione el nombre y, a continuación, haga clic en **Quitar**. El listado de un dominio incluye todos sus subdominios.

6.  Si utiliza RMS en un entorno donde necesite ampliar la pertenencia a grupos entre bosques, seleccione la casilla de verificación **Confiar en licencias de RM para identificadores de seguridad (SID) de este dominio de usuario**.

7.  Cuando termine, haga clic en **Cerrar la ventana y volver a Directivas de confianza**.

Para obtener más información sobre cómo realizar este procedimiento, vea "[Adición y desinstalación de dominios de usuarios de confianza](https://technet.microsoft.com/7c440b15-01c4-49f1-b43c-00f67f3388c1)", anteriormente en este tema.
