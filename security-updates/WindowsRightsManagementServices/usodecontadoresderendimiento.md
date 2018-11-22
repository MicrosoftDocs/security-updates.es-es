---
TOCTitle: Uso de contadores de rendimiento
Title: Uso de contadores de rendimiento
ms:assetid: '096c3b17-c082-46c4-939c-4373af0c9dec'
ms:contentKeyID: 18127685
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720180(v=WS.10)'
---

Uso de contadores de rendimiento
================================

RMS incluye varios conjuntos de objetos y contadores de rendimiento que puede utilizar en el Monitor del sistema para supervisar la actividad de los servicios de RMS. Los contadores de rendimiento son específicos de cada uno de los objetos de rendimiento de RMS e incluyen los siguientes objetos:

-   Contadores de rendimiento de RMS: ActivationProxy para solicitudes de proxy de activación
-   Contadores de rendimiento de RMS: Certification para solicitudes de certificación de cuentas
-   Contadores de rendimiento de RMS: DirectoryServices para consultas en Active Directory
-   Contadores de rendimiento de RMS: Enrollment para solicitudes de subinscripción
-   Contadores de rendimiento de RMS: Licensing para solicitudes de licencias de uso y de publicación
-   Contadores de rendimiento de RMS: Logging para el registro de actividad

Estos contadores de rendimiento se instalan automáticamente durante el establecimiento de los servicios en línea, pero debe agregarlos al registro para iniciar la supervisión.

Para agregar un contador de rendimiento:

1.  En el menú **Inicio**, seleccione **Herramientas administrativas** y después haga clic en **Rendimiento**.
2.  En el cuadro de diálogo **Rendimiento**, haga clic con el botón secundario en un área vacía del panel de detalles y después haga clic en **Agregar contadores**.
3.  En el cuadro de diálogo **Agregar contadores**, en la lista de objetos **Rendimiento**, seleccione el contador que desee agregar y haga clic en **Agregar**.

Puede utilizar las opciones de **Registros y alertas de rendimiento**, disponibles en el cuadro de diálogo **Rendimiento**, para supervisar y administrar archivos de registro. Para obtener más información acerca de los contadores de rendimiento disponibles en RMS, vea “[Contadores de rendimiento de RMS](https://technet.microsoft.com/a2f4e30d-3c6f-4e74-bd11-8f2103f88b0c)”, más adelante en este tema. Para obtener información general sobre los contadores de rendimiento, consulte la Ayuda del Monitor del sistema.
