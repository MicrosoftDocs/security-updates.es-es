---
TOCTitle: Protección de servidores de RMS
Title: Protección de servidores de RMS
ms:assetid: '7e6c4d3a-6cfb-4e96-9dda-ead83f961a6e'
ms:contentKeyID: 18127841
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747574(v=WS.10)'
---

Protección de servidores de RMS
===============================

Puede utilizar las siguientes recomendaciones para administrar la configuración de seguridad y las cuentas de usuario correspondientes a los servidores de RMS:

-   Los directorios virtuales del sitio Web que utilice para administrar RMS poseen listas de control de acceso discrecional (DACL) que limitan el acceso a administradores locales. Un administrador local puede crear un grupo de seguridad adicional para lograr un mayor control sobre el acceso mediante la adición y desinstalación de miembros, así como el establecimiento de entradas de control de acceso adicionales (ACE) en las páginas Web de administración.
-   A fin de mejorar la seguridad, cambie la configuración de DACL de la página Web Configuración de seguridad (SecurityPolicy.aspx). Para permitir el establecimiento de servicios en línea, la entrada ACE predeterminada otorga control total a la cuenta que establezca los servicios en línea de RMS. Después del establecimiento de los servicios en línea, debe cambiar la entrada ACE a una persona o a un grupo de seguridad restringido.
-   Además de los permisos de cada servidor de RMS, preste especial atención a los requisitos para proteger la base de datos de configuración, que resulta vital para proteger la implementación completa. Para obtener más información, vea "[Protección de la base de datos de configuración](https://technet.microsoft.com/e023b96f-81d0-45fb-8cc5-becaf6d47ae1)", más adelante en este tema.

Para obtener más información sobre cómo proteger Microsoft SQL Server™, consulte la página Web **Seguridad en SQL Server** en el [sitio Web de Microsoft](http://www.microsoft.com/) (http://www.microsoft.com/).

Para obtener más información acerca de cómo proteger los equipos que ejecuten uno de los sistemas operativos de la familia Microsoft Windows Server 2003, obtenga la guía de seguridad "Windows Server 2003  Security Guide" (en inglés) en el Centro de descarga de Microsoft, disponible en el [sitio Web de Microsoft](http://www.microsoft.com/) (http://www.microsoft.com/).
