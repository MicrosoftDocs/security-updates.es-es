---
TOCTitle: 'Paso 1: revisar los requisitos de instalación de WSUS'
Title: 'Paso 1: revisar los requisitos de instalación de WSUS'
ms:assetid: '57d7f8ec-1523-4485-9967-604be9ba2aac'
ms:contentKeyID: 18158346
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720547(v=WS.10)'
---

Paso 1: revisar los requisitos de instalación de WSUS
=====================================================

Esta guía ofrece instrucciones para instalar Microsoft Windows Server Update Services (WSUS) en los sistemas operativos Microsoft Windows Server 2003 (exceptuando la versión Web Edition y todas las versiones de 64 bits). Si tiene un servidor que ejecuta Microsoft Windows 2000 Server y necesita más información, vea las notas del producto “Deploying Microsoft Windows Server Update Services” (el documento puede estar en inglés).

A continuación se exponen los requisitos de instalación de línea de base para las instalaciones en las que se utilizan las opciones predeterminadas. Encontrará los requisitos de hardware y software para otras instalaciones en las notas del producto “Deploying Microsoft Windows Server Update Services” (el documento puede estar en inglés).

Recomendaciones de hardware para un servidor con 500 clientes como máximo:

-   Procesador de 1 gigahercio (GHz)
-   1 gigabyte (GB) de RAM

Requisitos de software
----------------------

Para instalar WSUS con las opciones predeterminadas, debe tener el software siguiente instalado en el equipo. Para obtener más información acerca de los requisitos de software de WSUS, vea las notas del producto “Deploying Microsoft Windows Server Update Services” (el documento puede estar en inglés). Si alguna de estas actualizaciones requiere que se reinicie el equipo al finalizar la instalación, debe reiniciar el servidor antes de instalar WSUS.

-   Servicios de Microsoft Internet Information Server (IIS) 6.0 Para obtener las instrucciones de instalación de IIS, vea las notas del producto “Deploying Microsoft Windows Server Update Services” (el documento puede estar en inglés) o el Centro de ayuda y soporte técnico de Windows Server 2003.
-   Microsoft .NET Framework 1.1 Service Pack 1 para Windows Server 2003. Para obtener este software, vaya al [Centro de descarga](http://go.microsoft.com/fwlink/?linkid=47358), en la dirección http://go.microsoft.com/fwlink/?LinkId=47358 (puede que esté en inglés).
    Alternativamente, puede ir a http://www.windowsupdate.com y buscar Critical Updates and Service Packs – Install Microsoft .NET Framework 1.1 Service Pack 1 for Windows Server 2003.
-   Servicio de transferencia inteligente en segundo plano (BITS) 2.0. Actualmente, BITS 2.0 para Windows Server 2003 no está disponible en el Centro de descarga. Para obtener este software, vaya al [sitio Web de Microsoft](http://go.microsoft.com/fwlink/?linkid=47357) para Windows Server Update Services Open Evaluation, en la dirección http://go.microsoft.com/fwlink/?LinkId=47357 (puede que esté en inglés).

| ![](images/Cc720547.note(WS.10).gif)Nota                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aunque se requiere software de base de datos para instalar WSUS, no se incluye aquí porque la instalación predeterminada de WSUS en Windows Server 2003 incluye el software de base de datos Windows SQL Server™ 2000 Desktop Engine (WMSDE). |

Requisitos y recomendaciones para el disco
------------------------------------------

Para instalar WSUS, el sistema de archivos del servidor debe satisfacer los siguientes requisitos:

-   La partición del sistema y la partición en la que se instala WSUS deben tener formato del sistema de archivos NTFS.
-   Se requiere un espacio libre mínimo de 1 GB para la partición del sistema.
-   Se requiere, como mínimo, un espacio libre de 6 GB para el volumen donde WSUS almacena contenido; se recomiendan 30 GB.
-   Se requieren, como mínimo, 2 GB de espacio libre en el volumen donde el programa de instalación de WSUS instala Windows SQL Server 2000 Desktop Engine (WMSDE).

Requisitos de Actualizaciones automáticas
-----------------------------------------

Actualizaciones automáticas es el componente de cliente de WSUS. No tiene otros requisitos de hardware aparte de estar conectado a la red. Puede utilizar Actualizaciones automáticas con WSUS en los equipos que ejecuten alguno de los siguientes sistemas operativos:

-   Microsoft Windows 2000 Professional con Service Pack 3 (SP3) o Service Pack 4 (SP4), Windows 2000 Server con SP3 o SP4, o Windows 2000 Advanced Server con SP3 o SP4.
-   Microsoft Windows XP Professional, con o sin Service Pack 1 o Service Pack 2.
-   Microsoft Windows Server 2003 Standard Edition, Windows Server 2003 Enterprise Edition, Windows Server 2003 Datacenter Edition o Windows Server 2003 Web Edition.
