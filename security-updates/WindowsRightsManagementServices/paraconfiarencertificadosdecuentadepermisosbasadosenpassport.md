---
TOCTitle: Para confiar en certificados de cuenta de permisos basados en Passport
Title: Para confiar en certificados de cuenta de permisos basados en Passport
ms:assetid: 'c096fa36-c40d-4b28-843c-e9cbbe8eef70'
ms:contentKeyID: 18127956
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747655(v=WS.10)'
---

Para confiar en certificados de cuenta de permisos basados en Passport
======================================================================

Microsoft proporciona un servicio de certificación de cuentas que utiliza credenciales de Microsoft .NET Passport para establecer los certificados de cuenta de permisos para el usuario. Si desea que los usuarios con certificados de cuenta de permisos de este servicio puedan obtener licencias de uso del clúster de RMS, debe configurar un dominio de usuario de confianza que acepte credenciales de usuario del servicio de certificación de cuentas de Microsoft.

Para utilizar esta característica, debe configurar Servicios de Internet Information Services para permitir el acceso anónimo al servicio de emisión de licencias de RMS. Este paso es esencial para los usuarios externos, puesto que el servicio de licencias está configurado para utilizar la autenticación integrada de Windows de forma predeterminada. Si no se establece el acceso anónimo, los usuarios externos con certificados de cuenta de permisos (RAC) basados en Passport no podrán obtener licencias.

Confianza en certificados de cuenta de permisos basados en Passport
-------------------------------------------------------------------

#### Para habilitar el acceso anónimo al servicio de emisión de licencias de RMS

1.  Abra el complemento **Administrador de Servicios de Internet Information Server** y expanda el servidor que aloja RMS.

2.  En el árbol de la consola, expanda **Sitios Web** y, a continuación, expanda el sitio Web en el que ha configurado RMS. De forma predeterminada, es el **Sitio Web predeterminado**.

3.  En el árbol de la consola, expanda el sitio Web **\_wmcs** y, a continuación, seleccione el directorio virtual **licensing**.

4.  Haga clic con el botón secundario en el directorio virtual **licensing** y seleccione **Propiedades**.

5.  En el cuadro de diálogo **Propiedades de Licensing**, haga clic en **Seguridad de directorios**.

6.  Haga clic en **Editar** en el área **Autenticación y control de acceso**.

7.  Active la casilla de selección **Habilitar el acceso anónimo**.

#### Para confiar en certificados de cuenta de permisos basados en Passport

1.  Abra la página **Administración global** y, a continuación, junto al sitio Web en cuyos certificados de cuenta de permisos basados en Passport desee confiar, haga clic en **Administrar RMS en este sitio Web**.

2.  En el área **Vínculos de administración**, haga clic en **Directivas de confianza**.

3.  En el área **Dominios de usuarios de confianza**, haga clic en **Confiar en certificados RAC basados en Passport**. El servicio Microsoft RM Certification Service aparece en la lista **Dominios de usuarios de confianza**.

4.  Opcionalmente, puede excluir usuarios por sus direcciones de correo electrónico. Para ello, haga clic en **Identidades excluidas** y, a continuación, escriba la dirección de correo electrónico del usuario en el que no confía.
