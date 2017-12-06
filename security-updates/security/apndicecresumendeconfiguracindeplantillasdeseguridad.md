---
TOCTitle: 'Apéndice C: Resumen de configuración de plantillas de seguridad'
Title: 'Apéndice C: Resumen de configuración de plantillas de seguridad'
ms:assetid: '80d2b596-9608-4ae0-8095-81238a707002'
ms:contentKeyID: 20200239
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc163104(v=TechNet.10)'
---

Guía de Seguridad de Windows Server 2003
========================================

### Apéndice C: Resumen de configuración de plantillas de seguridad

Actualizado: 27/12/05

El libro de Microsoft® Excel® "Windows Server 2003 Security Guide Settings.xls" (incluido con esta guía) documenta la configuración de directivas y servicios para todas las funciones y los entornos que contiene esta guía. Este libro contiene diez hojas de trabajo, una para cada función descrita en la guía:

-   La hoja de trabajo **Domain** (dominio) contiene la configuración de directiva de grupo que configura los objetos de directiva de nivel de dominio, tal y como se describe en el capítulo 3, "Directiva de dominio".

-   La hoja de cálculo **Member Server Baseline** (línea de base de servidores miembro) contiene la configuración de directiva de grupo y servicio de SCW que configura la directiva de línea de base de servidores miembro (MSBP), tal y como se describe en el capítulo 4, "Directiva de línea de base de servidores miembro".

-   La hoja de cálculo **Domain Controller** (controlador de dominio) contiene la configuración de directiva de grupo y servicio de SCW que configura la directiva de línea de base de controladores de dominio (DCBP), tal y como se describe en el capítulo 5, "Directiva de línea de base de controladores de dominio".

-   La hoja de cálculo **Infrastructure Server** (servidor de infraestructura) contiene la configuración de directiva de grupo y servicio de SCW que configura las directivas del servidor de infraestructura, tal y como se describe en el capítulo 6, "Función de servidor de infraestructura".

-   La hoja de cálculo **File Server** (servidor de archivos) contiene la configuración de directiva de grupo y servicio de SCW que configura las directivas del servidor de archivos, tal y como se describe en el capítulo 7, "Función de servidor de archivos".

-   La hoja de cálculo **Print Server** (servidor de impresión) contiene la configuración de directiva de grupo y servicio de SCW que configura las directivas del servidor de impresión, tal y como se describe en el capítulo 8, "Función del servidor de impresión".

-   La hoja de cálculo **Web Server** (servidor web) contiene la configuración de directiva de grupo y servicio de SCW que configura las directivas del servidor web de IIS, tal y como se describe en el capítulo 9, "Función de servidor web".

-   La hoja de cálculo **IAS Server** (servidor IAS) contiene la configuración de directiva de grupo y servicio de SCW que configura las directivas del servidor IAS, tal y como se describe en el capítulo 10, "Función de servidor IAS".

-   La hoja de cálculo **CA Server** (servidor de entidad emisora) contiene la configuración de directiva de grupo y servicio de SCW que configura las directivas del servidor de Servicios de Certificate Server, tal y como se describe en el capítulo 11, "Función de servidor de Servicios de Certificate Server".

-   La hoja de cálculo **Bastion Host** (host de baluarte) contiene la configuración de directiva de grupo y servicio de SCW que configura las directivas del servidor host de baluarte, tal y como se describe en el capítulo 12, "Función de los host de baluarte".

Cada hoja de cálculo contiene las columnas siguientes:

-   La columna H, **Policy Setting Name in User Interface** (nombre de configuración de directiva en interfaz de usuario), corresponde al nombre de la configuración que aparece en el complemento Editor de directivas de grupo de Windows Server 2003.

-   La columna J, **Legacy Client** (cliente heredado), es el valor recomendado para la configuración del entorno Cliente heredado (LC).

-   La columna K, **Enterprise Client** (cliente de empresa), es el valor recomendado para la configuración del entorno Cliente de empresa (EC).

-   La columna L, **SSLF**, es el valor recomendado para la configuración del entorno Seguridad especializada: Funcionalidad limitada (SSLF).

Para facilitar la lectura de las hojas de cálculo, se utilizan columnas adicionales para ilustrar la jerarquía de objetos dentro del Editor de directivas de grupo. Las columnas de la A a la G se emplean para representar cada nivel de la jerarquía. Por ejemplo, **Computer Configuration** (configuración del equipo) aparece en la columna A y **Security Settings** (configuración de seguridad) figura en la columna C. También se ha insertado la columna I para facilitar la lectura.

[](#mainsection)[Principio de la página](#mainsection)

**Descargar**

[Obtenga la Guía de seguridad de Windows Server 2003](http://go.microsoft.com/fwlink/?linkid=14846)

**Notificaciones de actualizaciones**

[Suscríbase para obtener más información sobre actualizaciones y nuevas versiones](http://go.microsoft.com/fwlink/?linkid=54982)

**Comentarios**

[Envíenos sus comentarios o sugerencias](mailto:secwish@microsoft.com?asunto=guía%20de%20seguridad%20de%20windows%20server%202003)

[](#mainsection)[Principio de la página](#mainsection)
