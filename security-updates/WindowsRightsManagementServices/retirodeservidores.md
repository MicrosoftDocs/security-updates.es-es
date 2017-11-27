---
TOCTitle: Retiro de servidores
Title: Retiro de servidores
ms:assetid: '52005e2e-9563-4ba0-906c-3cc76f9c378f'
ms:contentKeyID: 18127814
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747568(v=WS.10)'
---

Retiro de servidores
====================

Pueden darse ocasiones en las que necesite retirar un servidor de RMS, por ejemplo, en las siguientes:

-   Problemas o actualizaciones de equipos que conlleven el reemplazo de servidores específicos.
-   Disminución del tráfico de publicación y emisión de licencias, con el consiguiente retiro de algunos servidores.
-   Requisitos legales que obliguen a quitar servidores de ubicaciones determinadas cuya consecuencia sea el retiro de todo un clúster.
-   Fusión o venta de divisiones u otras partes de una organización cuya consecuencia sea una transferencia de activos.
-   Fusión de toda una organización con otra que también ejecute RMS, lo que elimina la necesidad de poseer dos instalaciones de RMS.

Antes de retirar un servidor, debe realizar una copia de seguridad de todas las bases de datos de RMS que se utilicen en el servidor, especialmente de la base de datos de configuración. Para obtener más información acerca de la copia de seguridad de las bases de datos, vea “Copia de seguridad y restauración del sistema RMS” en la sección "Planeamiento de una implementación de RMS" de esta recopilación de documentación. .

Una vez que haya realizado una copia de seguridad de las bases de datos, puede quitar el servidor. Los requisitos para quitar un servidor de RMS dependen de la función del servidor y de la topología de la instalación de RMS:

-   **Supresión de un servidor de un clúster**. Si el servidor de RMS que desea retirar está en un clúster donde todavía hay servidores de RMS activos y necesarios, la supresión de un servidor de RMS individual del clúster requiere anular los servicios en línea y desinstalar RMS en el servidor que desea retirar, quitar el hardware del clúster y archivar las bases de datos.
    > [!NOTE]
    > Sólo debe anular los servicios en línea en los servidores del clúster de instalación raíz antes de desinstalar RMS. Este proceso no es necesario para los servidores de licencias. 

-   **Retiro de un servidor independiente**. Si el servidor de RMS que desea retirar es un servidor de RMS independiente (es decir, no forma parte de un clúster con varios servidores) que va a reemplazar por un nuevo servidor, siga estos pasos: anule los servicios en línea y desinstale el servidor de RMS existente, quítelo de la red e, inmediatamente después, instale RMS y establezca los servicios en línea en el nuevo servidor. Configure el nuevo servidor de RMS para que utilice la misma dirección URL y la misma base de datos de configuración que el servidor de RMS retirado. Tenga en cuenta que, hasta que se instale el nuevo servidor y se establezcan en él los servicios en línea, los usuarios no podrán utilizar contenido publicado con el servidor retirado.
    > [!IMPORTANT]
    > Si el servidor de RMS que va a reemplazar utiliza un módulo de seguridad de hardware, debe transferir el entorno de seguridad al nuevo servidor antes de instalar RMS y establecer los servicios en línea en él. Para obtener instrucciones, consulte la documentación del módulo de seguridad de hardware. 

-   **Reemplazo de una instalación de RMS por otra existente**. En algunas circunstancias, puede ser necesario retirar una instalación de RMS y reemplazarla por otra existente; por ejemplo, en el caso de una fusión empresarial en la que ambas compañías ejecuten RMS.

Cuando anule los servicios en línea en un servidor y lo desinstale, éste se quitará de la tabla ClusterServer de la base de datos de configuración y se eliminará la base de datos de servicios de directorio del servidor SQL Server. Para obtener instrucciones acerca de la anulación de RMS, vea "[Para anular los servicios en línea de RMS](https://technet.microsoft.com/9fa63daa-5fb9-4afd-8371-b38248619857)" y "[Para desinstalar RMS](https://technet.microsoft.com/885e3b4f-ea32-466f-9f7f-d8440b0f7c28)", más adelante en este tema.