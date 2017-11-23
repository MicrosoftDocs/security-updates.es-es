---
TOCTitle: Administración del tamaño del registro
Title: Administración del tamaño del registro
ms:assetid: '431b32b3-02f0-4666-b52c-183eb65154fd'
ms:contentKeyID: 18127790
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720271(v=WS.10)'
---

Administración del tamaño del registro
======================================

El servicio de registro envía grandes cantidades de datos a la base de datos de SQL Server. Debe comprobar la base de datos de registro regularmente para asegurarse de que haya suficiente capacidad en disco para los datos. Si descubre que la cantidad de datos es excesiva y que no necesita parte de la información para sus informes, considere el establecimiento de filtros de SQL Server para que los archivos de registro sólo almacenen los datos que necesite. Para obtener instrucciones acerca del filtrado de la información de registro, consulte la Ayuda del Administrador corporativo de SQL Server.

Si observa que el tamaño de la base de datos de registro es excesivo para el espacio en disco disponible, puede moverla a un servidor diferente, como se describe en "[Reubicación de la base de datos de registro](https://technet.microsoft.com/34ea8045-dc94-422e-9601-29927cfc1534)", más adelante en este tema.

> [!IMPORTANT]
> También debe utilizar el Monitor del sistema para supervisar regularmente el tamaño de la cola de mensajes de registro salientes. Si el tamaño de la cola crece notablemente, compruebe si el servicio de escucha de registro funciona correctamente. Para obtener más información acerca del uso del Monitor del sistema, consulte el Centro de ayuda y soporte técnico de Windows Server 2003. 
