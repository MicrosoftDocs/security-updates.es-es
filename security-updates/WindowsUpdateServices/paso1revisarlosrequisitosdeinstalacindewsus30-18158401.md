---
TOCTitle: 'Paso 1: revisar los requisitos de instalación de WSUS 3.0'
Title: 'Paso 1: revisar los requisitos de instalación de WSUS 3.0'
ms:assetid: '912b37d7-021e-4c95-b317-49dd15b4611c'
ms:contentKeyID: 18158401
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708484(v=WS.10)'
---

Paso 1: revisar los requisitos de instalación de WSUS 3.0
=========================================================

En esta guía se explica cómo instalar WSUS 3.0. Para obtener información sobre los requisitos de software y plataformas admitidas para WSUS 3.0, consulte las notas de la versión ([http://go.microsoft.com/fwlink/?LinkId=71220](http://go.microsoft.com/fwlink/?linkid=71220), en inglés) para los sistemas operativos Windows Server 2003 Service Pack 1 y Windows Server® 2008.

Requisitos de software para la instalación de WSUS 3-0 en Windows Server 2003 Service Pack 1
--------------------------------------------------------------------------------------------

Para instalar WSUS 3.0 en Windows Server 2003 Service Pack 1, debe tener instalado en su equipo lo siguiente. Si alguna de estas actualizaciones requiere que se reinicie el servidor al finalizar la instalación, debe reiniciarlo antes de instalar WSUS 3.0.

-   Microsoft Internet Information Services (IIS) 6.0
-   Actualización del Servicio de transferencia inteligente en segundo plano (BITS) 2.0 y WinHTTP 5.1 Windows Server 2003. Para descargar este software, vaya al Centro de descarga ([http://go.microsoft.com/fwlink/?LinkID=47251](http://go.microsoft.com/fwlink/?linkid=47251)).
-   Paquete redistribuible de Microsoft .NET Framework versión 2.0 (x86). Para descargar este software, vaya al Centro de descarga ([http://go.microsoft.com/fwlink/?LinkID=68935](http://go.microsoft.com/fwlink/?linkid=68935)). Para las plataformas de 64 bits, vaya también al Centro de descarga \[[http://go.microsoft.com/fwlink/?LinkID=70637](http://go.microsoft.com/fwlink/?linkid=70637)\].
-   Microsoft Report Viewer Redistributable 2005. Para descargar este software, vaya al Centro de descarga ([http://go.microsoft.com/fwlink/?LinkID=70410](http://go.microsoft.com/fwlink/?linkid=70410)).
-   Microsoft Management Console 3.0 para Windows Server 2003 (KB907265). Para descargar este software, vaya al Centro de descarga ([http://go.microsoft.com/fwlink/?LinkID=70412](http://go.microsoft.com/fwlink/?linkid=70412)). Para las plataformas de 64 bits, vaya también al Centro de descarga \[[http://go.microsoft.com/fwlink/?LinkID=70638](http://go.microsoft.com/fwlink/?linkid=70638)\].

Requisitos de software para la instalación de WSUS 3.0 en Windows Server 2008
-----------------------------------------------------------------------------

Para instalar WSUS 3.0 en Windows Server 2008, debe tener instalado en su equipo lo siguiente. Si alguna de estas actualizaciones requiere que se reinicie el servidor al finalizar la instalación, debe reiniciarlo antes de instalar WSUS 3.0.

-   Microsoft Internet Information Services (IIS) 7.0 Asegúrese de que están habilitados los componentes siguientes:
    -   Autenticación de Windows
    -   ASP.NET
    -   Compatibilidad con la administración de 6.0
    -   Compatibilidad con la metabase de IIS
-   Microsoft Report Viewer Redistributable 2005. Para descargar este software, vaya al Centro de descarga ([http://go.microsoft.com/fwlink/?LinkID=70410](http://go.microsoft.com/fwlink/?linkid=70410)).
-   Microsoft SQL Server™ 2005 Service Pack 1. Para descargar este software, vaya al Centro de descarga ([http://go.microsoft.com/fwlink/?LinkID=66143](http://go.microsoft.com/fwlink/?linkid=66143)).

Las actualizaciones de .NET Framework 2.0 y BITS 2.0 están disponibles en Windows Server 2008 como parte del sistema operativo.

Requisitos del disco y recomendaciones
--------------------------------------

Para instalar WSUS 3.0, el sistema de archivos del servidor debe cumplir los requisitos siguientes:

-   Tanto la partición del sistema como la partición en la que instala WSUS 3.0 deben tener el formato de sistema de archivos NTFS.
-   Se recomienda un mínimo de 1 GB de espacio libre para la partición del sistema.
-   Se necesita un mínimo de 20 GB de espacio libre para el volumen donde WSUS almacena el contenido; se recomienda 30 GB de espacio libre.
-   Se recomienda un mínimo de 2 GB de espacio libre en el volumen donde el programa de instalación de WSUS instala Windows® Internal Database.

Requisitos de instalación sólo para consola
-------------------------------------------

WSUS 3.0 permite instalar la consola de administración de WSUS en sistemas remotos independientes del servidor de WSUS. Las instalaciones sólo para consola se pueden realizar en los siguientes sistemas operativos:

-   Windows Server® 2008
-   Windows Vista®
-   Windows Server 2003 Service Pack 1
-   Windows XP Service Pack 2

A continuación se indican los requisitos previos del software para la instalación sólo para consola.

-   Paquete redistribuible de Microsoft .NET Framework versión 2.0 (x86), disponible en el Centro de descarga de Microsoft ([http://go.microsoft.com/fwlink/?LinkId=68935](http://go.microsoft.com/fwlink/?linkid=68935)). Para las plataformas de 64 bits, vaya al paquete redistribuible de Microsoft .NET Framework versión 2.0 (x64) ([http://go.microsoft.com/fwlink/?LinkId=70637](http://go.microsoft.com/fwlink/?linkid=70637)).
-   Microsoft Management Console 3.0 para Windows Server 2003 (KB907265), disponible en el Centro de descarga de Microsoft ([http://go.microsoft.com/fwlink/?LinkId=70412](http://go.microsoft.com/fwlink/?linkid=70412)). Para plataformas de 64 bits, vaya a Microsoft Management Console 3.0 para Windows Server 2003 x64 Edition (KB907265) ([http://go.microsoft.com/fwlink/?LinkId=70638](http://go.microsoft.com/fwlink/?linkid=70638)).
-   Microsoft Report Viewer Redistributable 2005, disponible en el Centro de descarga de Microsoft ([http://go.microsoft.com/fwlink/?LinkId=70410](http://go.microsoft.com/fwlink/?linkid=70410)).

Requisitos de actualizaciones automáticas
-----------------------------------------

Actualizaciones automáticas es el componente cliente de WSUS 3.0. El único requisito de hardware de Actualizaciones automáticas es estar conectado a la red. Puede usar Actualizaciones automáticas con WSUS 3.0 en aquellos equipos que tengan alguno de los siguientes sistemas operativos:

-   Windows Vista.
-   Windows Server® 2008.
-   Microsoft Windows® Server 2003, todas las versiones y Service Pack.
-   Microsoft Windows XP Professional, Service Pack 1 o Service Pack 2.
-   Microsoft Windows 2000 Professional Service Pack 4, Windows 2000 Server Service Pack 4 o Windows 2000 Advanced Server Service Pack 4.

Permisos
--------

Se deben conceder los siguientes permisos de disco para directorios especificados a usuarios determinados:

1.  Los usuarios del grupo integrado o la cuenta de NT Authority\\Network Service (en Windows Server 2003) deben tener permiso de lectura para la carpeta raíz en el disco donde reside el directorio de contenido de WSUS. Si falta este permiso, se producirá un error en las descargas de BTIS.
2.  La cuenta de NT Authority\\Network Service debe tener permiso de "Control total" para el directorio de contenido de WSUS, por lo general &lt;SystemDriver&gt;:WSUS\\WsusContent. Este permiso lo establece la configuración del servidor de WSUS cuando crea el directorio, pero algún software de seguridad podría restablecer este permiso. Si falta este permiso, se producirá un error en las descargas de BTIS.
3.  La cuenta de NT Authority\\Network Service debe tener el permiso "Control total" para las carpetas siguientes para que el complemento de administración de WSUS se muestre correctamente:
    -   %windir%\\Microsoft .NET\\Framework\\v2.0.50727\\Temporary ASP.NET Files
    -   %windir%\\Temp

Para obtener más información sobre cómo establecer permisos, consulte DCPROMO no conserva permisos en algunas carpetas de IIS en [http://go.microsoft.com/fwlink/?LinkID=76332](http://go.microsoft.com/fwlink/?linkid=76332) (en inglés).
