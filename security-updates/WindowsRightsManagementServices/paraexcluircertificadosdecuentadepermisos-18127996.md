---
TOCTitle: Para excluir certificados de cuenta de permisos
Title: Para excluir certificados de cuenta de permisos
ms:assetid: 'e5cd9dec-ac29-437e-8515-dc697ec75edf'
ms:contentKeyID: 18127996
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747785(v=WS.10)'
---

Para excluir certificados de cuenta de permisos
===============================================

Para realizar este procedimiento, debe iniciar sesión localmente en el sitio Web de administración con una cuenta de usuario de dominio que sea miembro del grupo Administradores del equipo al que tiene acceso. Los miembros del grupo Administradores del dominio también pueden realizar este procedimiento. Como procedimiento recomendado de seguridad, considere el uso de la opción **Ejecutar como** para realizar este proceso.

Para abrir la página **Administración global**, haga clic en **Inicio**, elija **Todos los programas**, **Windows RMS** y, a continuación, haga clic en **Administración de Windows RMS**.

El cliente obliga a cumplir estas condiciones en el momento en que la licencia de uso se enlaza al contenido protegido.

Exclusión de certificados de cuenta de permisos
-----------------------------------------------

#### Para excluir certificados de cuenta de permisos

1.  Abra la página **Administración global** y, a continuación, junto al sitio Web en el que desee excluir certificados de cuenta de permisos, haga clic en **Administrar RMS en este sitio Web**.

2.  En el área **Vínculos de administración**, haga clic en **Directivas de exclusión**.

3.  En el área de exclusión de certificados de cuenta de permisos, haga clic en **Habilitar** para excluir el certificado de cuenta de permisos de un usuario.

4.  Seleccione el método para especificar el certificado de cuenta que desea excluir:

    -   Para excluir el certificado de cuenta por nombre de usuario, haga clic en **Nombre de usuario** para el certificado de cuenta de permisos que se va a excluir, escriba el nombre del usuario que se va a excluir (con el formato *nombre\_usuario*@*nombre\_dominio.com*) y, a continuación, haga clic en **Agregar**. Utilice esta opción para excluir los certificados de cuenta de los usuarios internos que tengan cuentas de usuario de Active Directory.
    -   Para excluir un certificado de cuenta por su clave pública, haga clic en **Cadena de clave pública** para el certificado de cuenta de permisos que se va a excluir, escriba la cadena de clave pública de certificado de cuenta de permisos y, a continuación, haga clic en **Agregar**. Utilice esta opción para excluir los certificados de cuenta de los usuarios externos que no tengan cuentas de usuario de Active Directory.

    | ![](images/Cc747785.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                                                               |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Para eliminar un certificado de cuenta de la lista de exclusión, haga clic en el certificado de cuenta de permisos excluidos en la lista y, a continuación, haga clic en **Eliminar claves públicas seleccionadas de la lista de exclusión**. Los usuarios que tengan certificados de cuenta específicos podrán obtener ahora una licencia para el contenido protegido con RMS desde este servidor. |

    | ![](images/Cc747785.note(WS.10).gif)Nota                                |
    |------------------------------------------------------------------------------------------------------|
    | Para deshabilitar la exclusión de certificados de cuenta de permisos, haga clic en **Deshabilitar**. |

Para obtener más información acerca de cómo realizar este procedimiento, vea "[Exclusión de certificados de cuenta de permisos](https://technet.microsoft.com/cba5e901-942c-4d06-9865-e6c4648c95e6)", anteriormente en este tema.
