---
TOCTitle: 'Windows Server Update Services 3.0 - Introducción a Microsoft Windows Server Update Services 3.0'
Title: 'Windows Server Update Services 3.0 - Introducción a Microsoft Windows Server Update Services 3.0'
ms:assetid: '632f98ac-9d45-480b-b801-996b714cebd0'
ms:contentKeyID: 18158351
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708429(v=WS.10)'
---

Windows Server Update Services 3.0
==================================

### Introducción a Microsoft Windows Server Update Services 3.0

Publicado: septiembre 11, 2007

Microsoft® Windows Server® Update Services 3.0 (WSUS 3.0) permite a los administradores de las tecnologías de la información implementar las últimas actualizaciones de productos de Microsoft en equipos que ejecutan los sistemas operativos de Microsoft Windows Server 2003, Windows Server 2008, Windows Vista, Microsoft Windows® XP con Service Pack 2 y Windows 2000 con Service Pack 4. Mediante WSUS, los administradores pueden administrar completamente la distribución de las actualizaciones lanzadas al mercado a través de Microsoft Update a los equipos de la red.

Puede descargar una copia de este documento [aquí](http://go.microsoft.com/fwlink/?linkid=71191).

### Funcionamiento de WSUS

WSUS ofrece una infraestructura de administración formada por los elementos siguientes:

#### Microsoft Update

El sitio web de Microsoft que distribuye actualizaciones de productos de Microsoft.

#### Servidor de Windows Server Update Services

Este componente está instalado en Windows Server 2003 SP1 o en el servidor Windows Server 2008 dentro del firewall corporativo. El servidor WSUS permite a los administradores administrar y distribuir actualizaciones a través de la consola de administración de WSUS 3.0, la cual puede instalarse en cualquier equipo Windows en el dominio. Además, un servidor WSUS puede ser el origen de actualizaciones para otros servidores WSUS dentro de la organización. Al menos un servidor WSUS de la red debe conectarse a Microsoft Update para obtener información acerca de las actualizaciones disponibles. En función de la seguridad y la configuración de la red, el administrador puede determinar si los otros servidores deberán conectarse directamente a Microsoft Update.

#### Actualizaciones automáticas

Este componente se crea en los sistemas operativos Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP y Windows 2000 SP4. El componente Actualizaciones automáticas permite que tanto el servidor como los equipos cliente reciban actualizaciones desde Microsoft Update o desde un servidor WSUS.

[](#mainsection)[Principio de la página](#mainsection)
