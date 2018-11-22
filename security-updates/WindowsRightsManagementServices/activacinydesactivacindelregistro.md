---
TOCTitle: Activación y desactivación del registro
Title: Activación y desactivación del registro
ms:assetid: '50ccd827-2d39-41e7-a395-3d5f5836869b'
ms:contentKeyID: 18127806
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747565(v=WS.10)'
---

Activación y desactivación del registro
=======================================

Puede activar y desactivar el registro para el clúster o el servidor actual en la página **Configuración de registro**. Al desactivarse el registro, los servicios Web de RMS dejan de enviar datos registrados a la cola de mensajes de registro. También se detiene el servicio de escucha de registro. No se admite la desactivación del registro mediante la herramienta de administración de los Servicios de Windows Server 2003.

Los registros de RMS se envían al servidor de base de datos mediante Message Queue Server. Si no se ha establecido ninguna conexión con el servidor de base de datos, Message Queue Server almacenará los registros en una caché local hasta que se restablezca la conectividad. La primera vez que habilite el registro, debe asegurarse de que el servidor RMS tiene una conexión con el servidor de base de datos y de que se ha iniciado el servicio de la base de datos. Si utiliza SQL Server como servidor de base de datos, puede verificar que los registros se escriben en la base de datos siguiendo estos pasos:

-   En el Administrador corporativo de SQL Server, vaya a la base de datos de registro, expanda **Bases de datos** y después expanda la base de datos que contiene la base de datos de registro de RMS.
-   Haga clic en la base de datos de registro, después en **Tablas**, haga clic con el botón secundario en **DRMS\_log\_master** y, a continuación, en **Abrir tabla, Devolver todas las filas**. Si se están creando archivos de registro, verá uno o más archivos.
