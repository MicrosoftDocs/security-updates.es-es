---
TOCTitle: Configuración de un entorno de prueba
Title: Configuración de un entorno de prueba
ms:assetid: 'cdd96b05-49e2-4b6f-bfae-40b5c028ec66'
ms:contentKeyID: 18127964
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747673(v=WS.10)'
---

Configuración de un entorno de prueba
=====================================

RMS se integra con la infraestructura existente y los servidores de bases de datos de Active Directory, como los que ejecutan Microsoft SQL Server™ 2000. A causa de la naturaleza crítica de estos componentes compatibles, debe probar RMS de forma rigurosa en un entorno de prueba aislado antes de implementarlo en la organización. Es necesario que configure instalaciones separadas de Active Directory y servidor de bases de datos en el entorno de prueba.

Empiece con la configuración más básica de un servidor de RMS en un bosque con un servidor de base de datos y un cliente. Cuando se haya familiarizado con RMS, puede ampliar la configuración para adecuarse a la topología que implementará en el entorno de producción de su organización, agregando múltiples bosques y acceso externo, según sea necesario. Aunque es posible que el entorno de prueba no incluya toda la redundancia y las configuraciones de sitios múltiples del plan organizativo de implementación, debe incluir al menos un servidor que opere cada uno de los componentes compatibles que necesita implementar.

En la lista siguiente se describe una configuración mínima posible para un entorno de prueba que puede utilizar para probar una configuración básica de RMS:

-   Un controlador de dominio que ejecute Windows 2000 Server con Service Pack 3 (SP3) o posterior, además de SQL Server 2000 con SP3a instalado. SQL Server alberga el registro, la configuración y las bases de datos de servicios de directorio de RMS. RMS puede utilizarse con Microsoft SQL Server 2000 Desktop Engine (MSDE 2000) Versión A o SQL Server si la base de datos está en el mismo servidor que RMS. Si va a utilizar un servidor remoto para las bases de datos, es necesario SQL Server. Puede descargar MSDE 2000 del sitio Web de Microsoft.

| ![](images/Cc747673.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 2000 Server con Service Pack 3 (SP3) es el requisito mínimo para el controlador de dominio, pero se recomienda Windows Server 2003 por las mejoras de rendimiento en la expansión de grupo de Active Directory. Se recomienda el uso de MSDE 2000 para admitir las bases de datos de RMS únicamente en entornos de pruebas, ya que MSDE 2000 no admite ninguna interfaz de red. Además, los términos de uso de MSDE 2000 especifican que no pueden utilizarse herramientas de cliente de SQL Server para manipular MSDE 2000. Dada esta restricción, no podrá ver información de registro ni cambiar los datos almacenados en la base de datos de configuración. |

-   Un servidor de certificación raíz que ejecute Windows Server 2003, en el que RMS está instalado y se han establecido los servicios en línea. Si lo desea, puede agregar más servidores para crear un clúster de certificación a medida que progresan las pruebas.
-   Un equipo cliente que ejecute Windows XP Professional, un cliente de RMS y una aplicación compatible con RMS.
-   Las cuentas de usuario que tienen atributos de dirección de correo electrónico en Active Directory.

Para obtener más información acerca de la instalación y configuración de una infraestructura RMS básica, además de cómo aplicar los requisitos de infraestructura a un entorno de producción, vea "[Configuración de una infraestructura básica](https://technet.microsoft.com/3a0a3a47-e755-4455-bb22-0e05053723e4)", más adelante en este tema.
