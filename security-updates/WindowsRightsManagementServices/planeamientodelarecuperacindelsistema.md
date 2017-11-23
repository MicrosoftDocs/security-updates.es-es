---
TOCTitle: Planeamiento de la recuperación del sistema
Title: Planeamiento de la recuperación del sistema
ms:assetid: 'a7779ffd-7a94-4e13-b846-0ffd00608e02'
ms:contentKeyID: 18127903
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747718(v=WS.10)'
---

Planeamiento de la recuperación del sistema
===========================================

Se producen errores del sistema a causa de numerosas razones imprevistas: errores de hardware, inundaciones, sobretensión de corriente, errores de software, etc. Una implementación correcta incluye una previsión para recuperar el sistema rápidamente en caso de error. En un sistema RMS, el requisito principal para proteger la funcionalidad de RMS es realizar con regularidad copias de seguridad de las bases de datos de RMS, especialmente de la base de datos de configuración. Esta práctica conserva las plantillas de directiva de permisos, las claves y otros datos necesarios para proporcionar acceso a licencias anteriores y contenido publicado. Si la instalación de RMS existente deja de estar disponible, puede instalar RMS en otros servidores y establecer los servicios en línea de RMS especificando que debe utilizarse la copia de seguridad de la base de datos de configuración. La nueva instalación a partir de la copia de seguridad será idéntica a la anterior en el momento en que se realizó la copia de seguridad por última vez.

Se tratan los siguientes temas:

-   [Preparación de la recuperación del sistema](https://technet.microsoft.com/885c047f-1e3b-4bf5-8248-3a4505759cbb)
-   [Copias de seguridad de sistema para RMS](https://technet.microsoft.com/c29894da-ee00-428c-8d48-80d8e5a83678)
-   [Copia de seguridad y restauración del sistema RMS](https://technet.microsoft.com/c11f3ac1-e512-402b-bf13-9ff21f5fe745)
-   [Copia de seguridad y restauración de plantillas de directiva de permisos](https://technet.microsoft.com/a6ed3328-4128-45e8-9236-3de484b460de)
