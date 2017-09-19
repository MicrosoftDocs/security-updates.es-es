---
TOCTitle: 'Paso 4: sincronizar el servidor'
Title: 'Paso 4: sincronizar el servidor'
ms:assetid: 'a5514e46-a50b-46a6-9e5b-33c87c5b7cef'
ms:contentKeyID: 18158562
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc708523(v=WS.10)'
---

Paso 4: sincronizar el servidor
===============================

Una vez configurada la conexión de red, se pueden obtener actualizaciones. De manera predeterminada, WSUS está configurado para descargar actualizaciones críticas y de seguridad para todos los productos de Microsoft. Para obtener actualizaciones, debe *sincronizar* el servidor WSUS.

Para la sincronización, el servidor WSUS se pone en contacto con Microsoft Update. Una vez establecido el contacto, WSUS determina si hay actualizaciones nuevas disponibles desde la última vez que se sincronizó. Debido a que es la primera vez que se sincroniza el servidor WSUS, todas las actualizaciones están disponibles y listas para que las apruebe para su instalación.

| ![](images/Cc708523.note(WS.10).gif)Nota                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Este documento describe cómo realizar la sincronización con la configuración predeterminada, pero WSUS incluye opciones que permiten reducir al mínimo el uso de banda ancha durante la sincronización. Para obtener más información, vea las notas del producto “Deploying Microsoft Windows Server Update Services” (el documento puede estar en inglés). |

**Para sincronizar el servidor WSUS**
1.  En la barra de herramientas de la consola de WSUS, haga clic en **Opciones** y, a continuación, en **Opciones de sincronización**.

2.  En **Tareas**, haga clic en **Sincronizar ahora**.

Cuando finalice la sincronización, haga clic en **Actualizaciones** en la barra de herramientas de la consola de WSUS para ver la lista de actualizaciones.
