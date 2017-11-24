---
TOCTitle: Reubicación de la base de datos de registro
Title: Reubicación de la base de datos de registro
ms:assetid: '34ea8045-dc94-422e-9601-29927cfc1534'
ms:contentKeyID: 18127750
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720238(v=WS.10)'
---

Reubicación de la base de datos de registro
===========================================

La configuración de RMS predeterminada ubica las bases de datos de configuración y de registro en el mismo servidor. Es recomendable que compruebe que el servidor SQL Server posea espacio suficiente para ambas bases de datos.

Si la base de datos de registro es demasiado grande, puede moverla a un servidor diferente en cualquier momento. No es posible cambiar la ubicación de la base de datos de registro desde el sitio Web de administración; en su lugar, debe hacerlo manualmente siguiendo estos pasos:

1.  Desactive el registro como se describe en “[Para activar o desactivar el registro](https://technet.microsoft.com/8e672f95-566f-4070-9a2a-2f70f087148f)”, más adelante en este tema.

2.  Copie la base de datos de registro desde el servidor de origen al de destino utilizando el Administrador corporativo de SQL Server. Asegúrese de que las tablas y los procedimientos almacenados se creen en la nueva base de datos. Un método para hacerlo es utilizar el Asistente para copiar bases de datos del Administrador corporativo de SQL Server.

3.  Cambie la base de datos de configuración para que refleje los nuevos nombres de servidor y de base de datos. En la tabla DRMS\_ClusterPolicies de la base de datos de configuración del clúster para el que vaya a desplazar la base de datos, haga lo siguiente:

    -   Cambie el valor de la directiva LoggingDatabaseServer para reflejar el nombre del nuevo servidor de base de datos.

    -   Cambie el valor de la directiva LoggingDatabaseName para reflejar el nuevo nombre de la base de datos.

    > [!NOTE]
    > El Administrador corporativo de SQL Server no funciona con campos db\_variant, por lo que no puede utilizarlo para esta tarea. En su lugar, puede utilizar el Analizador de consultas, incluido con SQL Server, u otra herramienta de edición de bases de datos. 

4.  Reinicie IIS en todos los servidores del clúster.

5.  Vuelva a activar el registro.