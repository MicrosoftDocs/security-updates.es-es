---
TOCTitle: Revisión del diseño de RMS
Title: Revisión del diseño de RMS
ms:assetid: '0ed1dd67-8e07-47c9-9e2e-0104438bd19f'
ms:contentKeyID: 18127687
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720185(v=WS.10)'
---

Revisión del diseño de RMS
==========================

Antes de comenzar la implementación, asegúrese de que su plan de RMS cumple las siguientes condiciones:

-   Se ha seleccionado una aplicación cliente compatible con RMS y se han establecido planes de implementación.
-   Se ha determinado un método para la distribución del cliente de RMS.
-   Hay un servidor de base de datos instalado y accesible.
-   Se ha seleccionado una topología de RMS, ya sea básica o distribuida.
-   Active Directory está instalado en los controladores de dominio que ejecutan Windows 2000 con Service Pack 3 (SP3) o posterior, y todos los usuarios tienen un objeto de contacto con un atributo de correo electrónico configurado. Windows Server 2003 está instalado con las actualizaciones más recientes. Message Queue Server, los Servicios de Internet Information Server y la versión 1.1 de ASP.NET están habilitados.

> [!NOTE]
> Si tiene previsto instalar RMS en un equipo de 64 bits, vea las instrucciones de configuración especiales que se indican en "Requisitos de software para RMS" en "Planeamiento de una implementación de RMS" en esta recopilación de documentación. 

-   Se han definido métodos de equilibrio de carga y de migración tras error del servidor.
-   Se ha configurado el registro de DNS para los servidores de RMS.
-   Existen planes de copia de seguridad y de recuperación.
-   Existen consideraciones de seguridad completas adecuadas para su organización.
