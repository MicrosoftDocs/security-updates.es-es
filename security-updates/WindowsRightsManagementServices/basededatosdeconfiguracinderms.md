---
TOCTitle: Base de datos de configuración de RMS
Title: Base de datos de configuración de RMS
ms:assetid: '769adbdc-f32f-464b-85c4-e8b160036187'
ms:contentKeyID: 18127908
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747634(v=WS.10)'
---

Base de datos de configuración de RMS
=====================================

RMS utiliza un servidor de base de datos, como Microsoft® SQL Server o Microsoft SQL Server 2000 Desktop Engine (MSDE 2000) versión A para almacenar la información sobre configuración y directivas. Existe una base de datos de configuración para cada servidor o clúster de RMS que almacena, comparte y recupera datos de configuración y otros datos.

La base de datos de configuración del servidor o clúster de certificación raíz contiene una lista de las identidades de los usuarios de Windows y de sus certificados de cuenta de permisos. El par de claves del certificado se cifra en la clave pública del servidor de RMS antes de almacenarse en la base de datos. Las bases de datos de configuración de los servidores de licencias no contienen esta información.

El grupo de servicio de RMS (RMS Service Group) tiene permiso de ejecución en los procedimientos almacenados de la base de datos.

**Importante**  Se recomienda el uso de MSDE 2000 para admitir las bases de datos de RMS únicamente en entornos de pruebas, ya que MSDE 2000 no admite ninguna interfaz de red. Además, las condiciones de uso de MSDE 2000 especifican que no se pueden utilizar herramientas de cliente de SQL Server para manipular una base de datos de MSDE 2000. Dada esta restricción, no podrá ver información de registro ni cambiar los datos almacenados en la base de datos de configuración.
