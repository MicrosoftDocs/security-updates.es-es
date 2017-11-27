---
TOCTitle: Para excluir aplicaciones
Title: Para excluir aplicaciones
ms:assetid: '422f2ddd-bcf4-45f1-905a-b8bad30fd7dd'
ms:contentKeyID: 18127789
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720262(v=WS.10)'
---

Para excluir aplicaciones
=========================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

El cliente obliga a cumplir las directivas de exclusión en el momento en que la licencia de uso se enlaza al contenido protegido.

Exclusión de aplicaciones o detención de la exclusión de aplicaciones
---------------------------------------------------------------------

#### Para excluir aplicaciones

1.  Abra la página **Administración global** y, a continuación, junto al sitio Web en el que desee controlar qué versiones de las aplicaciones se pueden usar con contenido protegido con permisos, haga clic en **Administrar RMS en este sitio Web**.

2.  En el área **Vínculos deadministración**, haga clic en **Directivas de exclusión**.

3.  En el área **Exclusión de aplicación**, haga clic en **Habilitar** para excluir una aplicación o componente compatible con RMS.

    Para deshabilitar la exclusión de aplicaciones, haga clic en **Deshabilitar**.

4.  Escriba el nombre de archivo de la aplicación o componente que desea excluir, escriba las versiones mínima y máxima que se deben excluir (con el formato *x*.*x*.*x*.*x*) y, a continuación, haga clic en **Excluir esta aplicación**.

    Para eliminar una aplicación (o componente) de la lista de exclusión, seleccione el nombre de archivo y, a continuación, haga clic en **Eliminar las aplicaciones seleccionadas de la lista de exclusión**.

    > [!NOTE]
    > RMS requiere que se especifique la versión de la aplicación en un formato de 4 dígitos separados por puntos (\#.\#.\#.\# ). Sin embargo, algunas aplicaciones especifican la versión de la aplicación en un formato de 2 o 3 dígitos separados por puntos. En este caso, deberá agregar tantas veces como convenga .0 para que el número de versión coincida con el formato requerido por RMS. 

#### Para detener la exclusión de aplicaciones

1.  Abra la página **Administración global** y, a continuación, junto al sitio Web en el que desee controlar qué versiones de las aplicaciones se pueden usar con contenido protegido con permisos, haga clic en **Administrar RMS en este sitio Web**.

2.  En el área **Vínculos deadministración**, haga clic en **Directivas de exclusión**.

3.  En el área **Exclusión de aplicaciones**, haga clic en **Deshabilitar**.

Para obtener más información acerca de cómo realizar este procedimiento, vea "[Exclusión de aplicaciones](https://technet.microsoft.com/b68ae4b2-b9ba-44ae-90cb-c88df600ec86)", anteriormente en este tema.
