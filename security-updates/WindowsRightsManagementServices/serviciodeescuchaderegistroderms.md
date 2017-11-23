---
TOCTitle: Servicio de escucha de registro de RMS
Title: Servicio de escucha de registro de RMS
ms:assetid: 'e81ea57d-1a7d-4c02-abfc-dbc1597e176b'
ms:contentKeyID: 18128007
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747709(v=WS.10)'
---

Servicio de escucha de registro de RMS
======================================

El programa de instalación de RMS instala el servicio de escucha de registro. Se ejecuta tanto en servidores de certificación raíz como en servidores de licencias. Todos los servicios Web de RMS registran todas las solicitudes y respuestas que reciben y envían y, a continuación, transmiten los datos a la cola de mensajes de registro mediante Message Queue Server. Después, el servicio de escucha de registro transfiere estos datos de la cola de mensajes a la base de datos de registro del clúster.

El registro puede activarse y desactivarse en el sitio Web de administración. Si se desactiva, los servicios Web no se registran y, además, se desactiva el servicio de escucha de registro.
