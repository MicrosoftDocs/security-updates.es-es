---
TOCTitle: Para habilitar la administración remota de RMS
Title: Para habilitar la administración remota de RMS
ms:assetid: '00f17054-5f5d-47e2-89c1-7a593b930bb3'
ms:contentKeyID: 18127709
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720181(v=WS.10)'
---

Para habilitar la administración remota de RMS
==============================================

Internet Explorer 6.0 o posterior debe estar instalado en el equipo que se utilice para la administración remota de RMS.

Habilitación de la administración remota de RMS
-----------------------------------------------

#### Para habilitar la administración remota de RMS

1.  Inicie sesión en el servidor que desee administrar de forma remota.

2.  En **Herramientas administrativas**, abra el complemento **Administrador de Internet Information Services (IIS)**.

3.  Expanda el elemento que representa el sitio Web en el que estableció los servicios en línea de RMS.

4.  Haga clic con el botón secundario del mouse en la carpeta **\_wmcs** y haga clic en **Propiedades**. En la ficha **Seguridad de directorios**, en **Comunicaciones seguras**, haga clic en **Editar**, después en **Requerir canal seguro** y finalmente en **Aceptar**. Esto aplica protección de capa de sockets seguros (SSL) a los servicios Web de RMS. Para obtener más información sobre cómo administrar sitios Web utilizando IIS, vea la Ayuda de IIS.

    | ![](images/Cc720181.Important(WS.10).gif)Importante                                                                                                                                                                                                  |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Puede proteger los servicios Web de RMS con SSL para obtener seguridad adicional y permitir el acceso HTTP remoto a las páginas Web de administración de RMS. Si piensa habilitar SSL para los servicios Web de RMS, obtenga e instale un certificado de servidor Web SSL válido. |

5.  Haga clic con el botón secundario del mouse en la carpeta **Admin** y haga clic en **Propiedades**. En la ficha **Seguridad de directorios**, en **Restricciones de nombre de dominio y dirección IP**, haga clic en **Editar** y, a continuación, en **Restricciones de acceso de direcciones IP**, haga clic en **Concederá el acceso** para permitir que todos los equipos soliciten una conexión con este sitio Web.
