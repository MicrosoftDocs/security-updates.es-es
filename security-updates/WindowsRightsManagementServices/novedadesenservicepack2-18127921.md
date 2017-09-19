---
TOCTitle: Novedades en Service Pack 2
Title: Novedades en Service Pack 2
ms:assetid: 'a944cb73-d900-42bb-b7aa-92916dead408'
ms:contentKeyID: 18127921
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747629(v=WS.10)'
---

Novedades en Service Pack 2
===========================

Rights Management Services (RMS) con Service Pack 2 (SP2) proporciona compatibilidad con las siguientes características:

-   **Compatibilidad nativa para Microsoft® SQL Server™ 2005**. En versiones anteriores de RMS, se necesitaba una solución para usar RMS con SQL Server 2005. Para obtener información acerca de esta solución, vea el artículo 913372 de Microsoft Knowledge Base ([http://go.microsoft.com/fwlink/?LinkId=68638](http://go.microsoft.com/fwlink/?linkid=68638)). En RMS con SP2 este problema se ha corregido.
-   **Microsoft Office SharePoint® Server 2007**. En esta versión se admite Office SharePoint Server 2007. La biblioteca de documentos de Office SharePoint Server 2007 aplica automáticamente los permisos de RMS a los documentos en función de los derechos de Office SharePoint Server 2007 tal como se han descargado. Esto se logra mediante la instalación del cliente de RMS con SP2 en el servidor de Office SharePoint Server 2007. No se recomienda instalar el servidor de RMS con SP2 y Office SharePoint Server 2007 en el mismo equipo.
-   **Mayor seguridad en los mensajes de la base de datos de registro**. En esta versión, todos los mensajes de Message Queue Server de los servidores de RMS en la base de datos de registro de RMS se firman digitalmente.
-   **Tamaños de lotes de servidores de mayor tamaño**. En esta versión, una aplicación habilitada para RMS puede recuperar varias licencias de uso para distintas cuentas de usuario a partir de una sola solicitud de licencia al servidor de RMS. De este modo, se incrementa el rendimiento mediante la reducción de la sobrecarga de varias solicitudes de licencia para el mismo elemento de contenido protegido por derechos.
-   **Expansión de grupo mejorada entre bosques**. En esta versión, la expansión de grupo de RMS entre bosques se lleva a cabo mediante una solicitud de Protocolo simple de acceso a objetos (SOAP) a un nuevo servicio web de ASP.NET que se ejecuta en el servidor de RMS.
