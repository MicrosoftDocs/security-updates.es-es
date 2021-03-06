---
TOCTitle: Compatibilidad con el servidor de base de datos para RMS
Title: Compatibilidad con el servidor de base de datos para RMS
ms:assetid: 'c9844783-e6c4-49b4-8e7f-0f0377143b44'
ms:contentKeyID: 18127950
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747664(v=WS.10)'
---

Compatibilidad con el servidor de base de datos para RMS
========================================================

RMS utiliza un servidor de base de datos, como SQL Server o Microsoft SQL Server 2000 Desktop Engine (MSDE 2000) versión A, para ejecutar las bases de datos de configuración, registro y servicios de directorio de RMS. Se puede usar MSDE 2000 únicamente en una instalación de un solo servidor. Como protección ante eventuales bloqueos del sistema, se puede implementar un clúster de servidor de base de datos.

Para permitir requisitos de registro, también puede ejecutar las bases de datos de configuración y de registro en instancias de servidor de base de datos independientes, o implementar un clúster o una instancia de servidor de base de datos independiente para el clúster o servidor de certificación raíz y los clústeres de licencias. Para obtener más información sobre estas opciones, vea "Implementación de un sistema RMS", en esta recopilación de documentación.

De forma predeterminada, el grupo de servicio de RMS tiene permisos de ejecución sobre los procedimientos almacenados de estas bases de datos. La cuenta de usuario que se registró durante el establecimiento de servicios en línea tiene permisos de propietario sobre estas bases de datos.

> [!NOTE]
> Se recomienda el uso de Microsoft SQL Server Desktop Engine para permitir las bases de datos de RMS únicamente en entornos de pruebas, puesto que Microsoft SQL Server Desktop Engine no incluye las herramientas necesarias para que funcione completamente una base de datos a nivel corporativo. Además, dado que MSDE no permite el trabajo con red remota, debe instalarlo en el mismo servidor que RMS y no puede añadir servidores de RMS adicionales al clúster de RMS. Las condiciones de uso de Microsoft SQL Server Desktop Engine especifican que no se pueden utilizar herramientas de cliente de SQL Server para manipular una base de datos de Microsoft SQL Server Desktop Engine. Con esta restricción, no podrá realizar y restaurar copias de seguridad de la base de datos de configuración de RMS, ver información de registro o modificar directamente datos almacenados en la base de datos de configuración. 
