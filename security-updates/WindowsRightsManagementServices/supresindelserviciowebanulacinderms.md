---
TOCTitle: 'Supresión del servicio Web (Anulación de RMS)'
Title: 'Supresión del servicio Web (Anulación de RMS)'
ms:assetid: '68b4e2b0-b1b7-4b0a-8c1a-82ac27c1f12e'
ms:contentKeyID: 18127838
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747602(v=WS.10)'
---

Supresión del servicio Web (Anulación de RMS)
=============================================

Una vez que se ha retirado el servidor de RMS y se ha eliminado toda la protección de RMS, puede eliminarse el servicio Web siguiendo estos pasos:

-   En la página **Administración global**, seleccione **Quitar RMS de este sitio Web**.

El paso siguiente depende del tipo de servidor que se va a quitar, aunque en todos los casos se eliminará RMS de IIS.

-   Si el servidor forma parte de un clúster (y no es el último servidor del clúster), no son necesarios más pasos.
-   Si el servidor sólo es un servidor de licencias, elimine la base de datos de servicios de directorio, pero conserve las bases de datos de configuración y de registro (las utiliza el servidor de certificación que sigue en servicio).
-   Si el servidor es el servidor final de RMS de la organización, conserve las bases de datos de configuración y de registro, pero elimine el punto de punto de conexión de servicio (SCP) de Active Directory.
