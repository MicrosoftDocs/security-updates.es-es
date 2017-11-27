---
TOCTitle: Seguridad durante la instalación de RMS
Title: Seguridad durante la instalación de RMS
ms:assetid: '0a3d40b2-f27e-4e63-baff-a9c8433f5f91'
ms:contentKeyID: 18127723
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720192(v=WS.10)'
---

Seguridad durante la instalación de RMS
=======================================

Para instalar y configurar los archivos de RMS, el programa de instalación de RMS utiliza las credenciales del usuario que ha iniciado la sesión. Con este fin, el administrador que realiza la instalación debe iniciar sesión con una cuenta de usuario que sea integrante del grupo Administradores local. Para todas las instalaciones, excepto para las realizadas en un equipo independiente, ésta debe ser también una cuenta de usuario de dominio.

Durante el procedimiento de instalación, se inicia el Instalador de Windows (Msiexec.exe). Este servicio hereda el símbolo de su usuario primario. Posteriormente, si se realizan acciones personalizadas después del proceso, el servicio Msiexec.exe utilizará la identidad del usuario que inició sesión. Esto ocurrirá ya se inicie el proceso desde un explorador o desde la línea de comandos.

El programa de instalación de RMS realiza las siguientes tareas:

-   Copia archivos a la carpeta C:\\Archivos de programa\\RMS. Esta carpeta, normalmente, permite el acceso tanto a administradores como a superusuarios. Durante el proceso de instalación, se puede cambiar la unidad y la ubicación en que se copiarán los archivos.

-   Crea el sitio Web de establecimiento de servicios en línea, el sitio Web de administración de RMS, en el puerto 5720 de forma predeterminada. Este sitio Web señala a los archivos instalados.

-   Crea un grupo de aplicaciones, WMCSProvisioningAppPool, y lo asocia con el sitio Web de administración de RMS. La cuenta de servicio utilizada por este grupo de aplicaciones es la cuenta Servicio de red.

-   Instala contadores de rendimiento.

-   Otorga al grupo de servicio de RMS permisos de lectura y de escritura para la siguiente clave de registro.

    En equipos con la versión de 32 bits de Windows Server 2003:

    `HKEY_LOCAL_MACHINE\Software\Microsoft\DRMS\1.0`  

    En equipos con la versión de 64 bits de Windows Server 2003:  
    
    `HKEY_LOCAL_MACHINE\Software\WOW6432Node\Microsoft\DRMS\1.0`