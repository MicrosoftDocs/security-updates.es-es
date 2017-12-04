---
TOCTitle: Base de datos de registro de RMS
Title: Base de datos de registro de RMS
ms:assetid: '8ba147f3-16e4-4d9a-ac8f-f05ba2ba11bb'
ms:contentKeyID: 18127864
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747669(v=WS.10)'
---

Base de datos de registro de RMS
================================

Para cada clúster de certificación raíz o de licencias, el programa de instalación de RMS instala una base de datos de registro en la misma instancia de servidor de base de datos donde se aloja la base de datos de configuración. El programa de instalación crea también una cola de mensajes privada para el registro en Message Queue Server. El servicio de escucha de registro transmite los datos de esta cola de mensajes a la base de datos de registro.

El grupo de servicio de RMS tiene permisos de ejecución sobre los procedimientos almacenados que se encuentran en la base de datos de registro.

El servicio de escucha de registro envía grandes cantidades de datos a la base de datos de registro; por tanto, los administradores deben crear filtros para que esta base de datos almacene sólo la información necesaria para la organización.
