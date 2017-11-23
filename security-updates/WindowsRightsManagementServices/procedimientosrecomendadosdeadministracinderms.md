---
TOCTitle: Procedimientos recomendados de administración de RMS
Title: Procedimientos recomendados de administración de RMS
ms:assetid: '385f8112-da00-417f-a2b8-42dc1e06b717'
ms:contentKeyID: 18127854
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720245(v=WS.10)'
---

Procedimientos recomendados de administración de RMS
====================================================

Tenga en cuenta los siguientes procedimientos recomendados para administrar RMS.

-   **No implemente servicios adicionales en los servidores de RMS**

    Si ejecuta servicios distintos de los servicios de RMS en los servidores, pueden producirse conflictos que conlleven problemas de seguridad. Utilice contadores de rendimiento para vigilar posibles conflictos o degradaciones del servicio.
-   **Realice frecuentes copias de seguridad de las bases de datos de configuración**

    Las bases de datos de configuración almacenan información fundamental para el funcionamiento de RMS. Además, la base de datos de configuración del clúster de certificación raíz almacena los pares de claves de toda la instalación. Si realiza copias de seguridad con regularidad, podrá conseguir que RMS funcione de nuevo enseguida en caso de que falle un servidor de base de datos. Además de realizar copias de seguridad con regularidad, también deberá comprobar regularmente la validez de dichas copias de seguridad realizando restauraciones de ejecución simulada (en un entorno de prueba separado). Para obtener más información, vea “Copia de seguridad y restauración del sistema RMS” en la sección "Planeamiento de una implementación de RMS" en esta recopilación de información.

-   **Recorte regularmente la base de datos de registro**

-   **Utilice Microsoft Operations Manager (MOM) para supervisar el servidor de RMS**

    Utilice MOM y MOM Pack de RMS para capturar sucesos críticos o detectar una degradación del rendimiento y enviar notificaciones de dichos sucesos.