---
TOCTitle: Detección del servicio de inscripción
Title: Detección del servicio de inscripción
ms:assetid: 'bbeb00bd-04e0-4df6-8615-76aa8125b620'
ms:contentKeyID: 18127930
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747737(v=WS.10)'
---

Detección del servicio de inscripción
=====================================

El primer servidor de RMS para el que se establezcan servicios en línea en un bosque debe conectarse con el servicio de inscripción de Microsoft para inscribirse y obtener un certificado emisor de licencias de servidor. Para adquirir la dirección URL del servicio de inscripción, el programa de instalación de RMS envía una solicitud UDDI al [sitio Web de UDDI de Microsoft](http://go.microsoft.com/fwlink/?linkid=14794) (http://go.microsoft.com/fwlink/?LinkId=14794). Los siguientes servidores para los que se establezcan servicios en línea como parte del clúster de certificación raíz no necesitan obtener certificados emisores de licencias de servidor, puesto que comparten la configuración del primer servidor de certificación raíz.
