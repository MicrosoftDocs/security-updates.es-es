---
TOCTitle: Exclusión de versiones de Windows
Title: Exclusión de versiones de Windows
ms:assetid: '8b8a184d-ac0e-4a43-822c-d2fae2faf484'
ms:contentKeyID: 18127881
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747590(v=WS.10)'
---

Exclusión de versiones de Windows
=================================

El cliente de Microsoft® Windows® Rights Management Services (RMS) 1.0 es compatible con equipos que ejecutan Microsoft Windows 98 Second Edition o Windows Millennium Edition; sin embargo, estos sistemas operativos no admiten la autenticación NTLM. Por esta razón, es posible que desee impedir que los usuarios utilicen contenido protegido con RMS desde un equipo que ejecute uno de estos sistemas operativos y requerir que utilicen versiones de Windows posteriores a Windows Me, a fin de aumentar la seguridad del contenido.

Cuando se establece una directiva de exclusión para excluir usuarios según la versión de Windows, se establece una condición en todas las licencias de uso que impide que se utilicen en clientes con Windows 98 Second Edition y Windows Millennium Edition. Debe habilitar la exclusión de versión de Windows en la página **Directivas de exclusión** del sitio Web de administración de cada clúster en el que desee que entre en vigor.
