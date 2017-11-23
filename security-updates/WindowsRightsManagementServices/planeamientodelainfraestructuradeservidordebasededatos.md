---
TOCTitle: Planeamiento de la infraestructura de servidor de base de datos
Title: Planeamiento de la infraestructura de servidor de base de datos
ms:assetid: 'b12354bd-3143-4d1f-b5aa-450c4550653c'
ms:contentKeyID: 18127936
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747731(v=WS.10)'
---

Planeamiento de la infraestructura de servidor de base de datos
===============================================================

Dado que RMS utiliza bases de datos y procedimientos almacenados para operar, se requiere una infraestructura de base de datos para utilizar RMS en su organización. El servidor de base de datos puede estar en el mismo servidor que RMS o en un servidor distinto. Si no tiene un servidor de base de datos en su infraestructura para permitir RMS, puede utilizar Microsoft SQL Server 2000 Desktop Engine (MSDE 2000) Versión A como servidor de base de datos para probar RMS.

Se recomienda el uso de Microsoft SQL Server Desktop Engine para permitir las bases de datos de RMS únicamente en entornos de pruebas, puesto que Microsoft SQL Server Desktop Engine no incluye las herramientas necesarias para que funcione completamente una base de datos a nivel corporativo. Además, dado que MSDE no permite el trabajo con red remota, debe instalarlo en el mismo servidor que RMS y no puede añadir servidores de RMS adicionales al clúster de RMS. Las condiciones de uso de Microsoft SQL Server Desktop Engine especifican que no se pueden utilizar herramientas de cliente de SQL Server para manipular una base de datos de Microsoft SQL Server Desktop Engine. Con esta restricción, no podrá realizar y restaurar copias de seguridad de la base de datos de configuración de RMS, ver información de registro o modificar directamente datos almacenados en la base de datos de configuración.

Si tiene previsto albergar las bases de datos en un servidor diferente de la instalación de RMS, necesita utilizar un producto completo de servidor de base de datos, como SQL Server, a fin de proporcionar compatibilidad con bases de datos. Asegúrese de proporcionarle a la cuenta de servicio de RMS los permisos adecuados de lectura, escritura y creación de bases de datos en el servidor de bases de datos que utiliza para proporcionar compatibilidad con RMS.

Aunque RMS está diseñado y probado para servidores de bases de datos que se ejecuten con SQL Server 2000 y MSDE, y Microsoft no admite el uso de RMS junto con un proveedor de bases de datos que no sea SQL Server 2000 o MSDE, RMS puede ejecutarse en otros servidores de bases de datos que utilicen las interfaces ADO.NET proporcionadas por Microsoft .NET Framework. Por tanto, otros fabricantes de bases de datos pueden haber desarrollado proveedores de bases de datos compatibles con RMS. Puede utilizar cualquier proveedor de bases de datos con RMS con la condición de que los servidores de bases de datos correspondientes cumplan los criterios siguientes:

-   El servidor de base de datos debe aceptar Transact-SQL porque las secuencias de comandos de inicialización y los procedimientos almacenados de RMS utilizan Transact-SQL.
-   El servidor de base de datos debe ser compatible con todas las extensiones específicas de Microsoft SQL Server.

El proveedor de base de datos debe ser capaz de:

-   Responder a llamadas de método del espacio de nombres System.Data.SqlClient de .NET Framework.
-   Proporcionar la funcionalidad correspondiente del espacio de nombres System.Data.SqlClient.
-   Utilizar la autenticación integrada en Windows en lugar de la autenticación SQL.

Si utiliza RMS en cualquier otra configuración, póngase en contacto con el fabricante de bases de datos o proveedor de soluciones pertinente del proveedor de bases de datos que esté utilizando en su implementación personalizada.

> [!CAUTION]
> De forma predeterminada, todas las bases de datos de RMS están creadas con la recuperación completa activada, pero no se crean trabajos de copia de seguridad del registro de transacciones. Esto puede hacer que el disco duro del servidor se llene y se produzca un error del servidor de base de datos. Se recomienda la recuperación completa de la base de datos de configuración DRMS; las otras bases de datos DRMS pueden configurarse para que utilicen un modelo de recuperación diferente, más apropiado a su organización. 

Se tratan los siguientes temas:

-   [Cálculo de crecimiento de base de datos](https://technet.microsoft.com/87652cc2-b886-4797-8d40-356669768089)
-   [Mantenimiento de la base de datos de servicios de directorio](https://technet.microsoft.com/911a62f2-c1d6-4091-99b0-b53211be27a7)
-   [Mantenimiento de la base de datos de registro](https://technet.microsoft.com/de55058b-0d1a-4997-8a45-e14678ddd13f)