---
TOCTitle: Copia de seguridad y restauración de plantillas de directiva de permisos
Title: Copia de seguridad y restauración de plantillas de directiva de permisos
ms:assetid: 'a6ed3328-4128-45e8-9236-3de484b460de'
ms:contentKeyID: 18127920
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747625(v=WS.10)'
---

Copia de seguridad y restauración de plantillas de directiva de permisos
========================================================================

Para proteger las valiosas plantillas de directiva de permisos, realice una copia de seguridad en medios de sus datos (que se encuentran en la base de datos de configuración) con cierta regularidad y guarde estos medios en una ubicación segura. Así, si se produce un error del sistema, puede restaurar las plantillas de directiva de permisos con la copia de seguridad.

Realice alguno de estos procedimientos:

-   Realice una copia de seguridad de toda la base de datos de configuración que incluye los datos de plantillas de directiva de permisos. Para obtener más información sobre cómo realizar copias de seguridad de una base de datos de SQL Server, consulte la documentación de SQL Server.

    O bien

-   Realice una copia de seguridad únicamente de los datos de plantillas de directiva de permisos que se encuentran en la base de datos de configuración. Para ello, exporte la información de GUID y TemplateData de la tabla DRMS\_RightsTemplate a un archivo de texto nuevo. Para obtener más información sobre cómo exportar datos de una base de datos de SQL Server, consulte la documentación de SQL Server.

Si necesita restaurar los datos de plantillas de directiva de permisos que se encuentran en la base de datos de configuración, puede extraer la información de GUID y TemplateData de la tabla DRMS\_RightsTemplate de la copia de seguridad de la base de datos de configuración o simplemente importar los datos del archivo de texto. Para obtener más información sobre cómo realizar estas tareas, consulte la documentación de SQL Server.

> [!NOTE]
> Para establecer un plan para realizar copias de seguridad de las plantillas de directiva de permisos, consulte al administrador de SQL Server. 