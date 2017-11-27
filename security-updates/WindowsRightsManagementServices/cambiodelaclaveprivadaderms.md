---
TOCTitle: Cambio de la clave privada de RMS
Title: Cambio de la clave privada de RMS
ms:assetid: 'da32137e-394a-42b2-9552-ba20f4547c23'
ms:contentKeyID: 18127975
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747765(v=WS.10)'
---

Cambio de la clave privada de RMS
=================================

Durante el establecimiento de servicios en línea, RMS crea la clave privada de RMS para el servidor. La clave privada de RMS se cifra y almacena en la base de datos de configuración. Se recomienda realizar una copia de seguridad y almacenar la clave privada en una ubicación segura. Además, considere el uso de un módulo de seguridad de hardware para proteger la clave privada de RMS porque esta clave se utiliza en el esquema de cifrado de todo el contenido protegido por el servidor de RMS. Si, por algún motivo, la clave privada de RMS se viera comprometida, tendrá que anular los servicios en línea de RMS en el servidor y, a continuación, establecerlos de nuevo para obtener un nueva clave privada de RMS.

Si se ha utilizado el servidor para proteger contenido, se debe notificar a todos los propietarios del contenido y el contenido se debe volver a publicar utilizando el servidor de RMS con la nueva clave privada. Las copias de contenido protegido con la clave privada que se ha visto comprometida deben destruirse, ya que no se puede considerar que tengan una protección adecuada.

> [!IMPORTANT]
> Aunque el servidor se haya inscrito con el servicio de inscripción de Microsoft, el servidor debe repetir el proceso de establecimiento de servicios en línea para obtener una nueva clave privada. Si intenta volver a inscribir un servidor de RMS, se utilizará la clave privada de RMS anterior. 
