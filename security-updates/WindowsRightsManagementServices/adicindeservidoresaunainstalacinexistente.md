---
TOCTitle: Adición de servidores a una instalación existente
Title: Adición de servidores a una instalación existente
ms:assetid: '7f3598ff-cd19-4daa-aa65-877f7f95a8ec'
ms:contentKeyID: 18127850
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747648(v=WS.10)'
---

Adición de servidores a una instalación existente
=================================================

Puede agregar servidores a la instalación de RMS a medida que los necesite para hacer frente a un aumento de la demanda o para reemplazar los servidores que deban retirarse. Todas las instalaciones de RMS deben incluir al menos un servidor de certificación raíz y pueden incluir opcionalmente servidores de certificación raíz en un clúster. Además, las instalaciones de RMS pueden incluir servidores de licencias independientes o agrupados en un clúster.

Puede agregar servidores a una instalación de RMS utilizando cualquiera de los siguientes métodos:

-   Agregar uno o varios servidores de RMS a un clúster de certificación raíz.
-   Agregar un servidor de licencias independiente nuevo.
-   Agregar uno o varios servidores de RMS a un clúster de licencias.

**Adición de servidores de certificación raíz**

Para la mayoría de los fines, la adición de uno o varios servidores de RMS a un clúster de certificación raíz es el mejor método para aumentar la disponibilidad y la redundancia de la implementación. Un clúster de certificación raíz se compone de uno o varios servidores de certificación raíz. A diferencia de los servidores de licencias, que sólo proporcionan servicios de emisión de licencias y publicación, los servidores de certificación raíz proporcionan todos los servicios de RMS.

Durante la instalación y el establecimiento de los servicios en línea, puede elegir la opción de agregar un servidor a un clúster. Al hacerlo, el nuevo servidor de RMS se configura automáticamente como miembro del clúster. Para obtener instrucciones paso a paso sobre cómo instalar y establecer los servicios en línea en un servidor de RMS para agregarlo al clúster de certificación raíz, vea [Para instalar RMS con Service Pack 1](https://technet.microsoft.com/dab20175-a690-43f8-b943-768d289daa0d) y [Para agregar un servidor a un clúster](https://technet.microsoft.com/db635238-5528-4bec-9cc6-8244e2b3d733), más adelante en este tema.

Además de este paso de establecimiento de los servicios en línea, si desea crear un clúster por primera vez, debe configurar también software o hardware con funciones de clúster y equilibrio de carga. Si ya ha implementado un clúster, debe configurar el software o hardware de equilibrio de carga para que funcione con el nuevo miembro del clúster.

**Adición de servidores de licencias**

A diferencia del servidor de certificación raíz, que proporciona todos los servicios de RMS, un servidor de licencias sólo proporciona servicios de emisión de licencias y publicación.

Los servidores de licencias son opcionales y suelen implementarse para satisfacer requisitos de emisión de licencias específicos, tales como:

-   Para permitir la administración de permisos únicos de un departamento. Por ejemplo, los requisitos de seguridad para la administración de permisos de un grupo de su organización pueden ser diferentes a los del resto de la organización, y es posible que desee un control total sobre la implementación de licencias para su grupo. Puesto que sólo se permite un servidor de certificación raíz en un bosque, probablemente no es adecuado configurar un servidor de certificación raíz independiente. En este caso, puede configurar un servidor o un clúster de licencias dedicado a las necesidades de ese departamento. Después, puede configurar una directiva de permisos independiente para dicho servidor o clúster de licencias.
-   Para permitir la administración de permisos para empresas asociadas externas, como parte de una extranet que precise una separación segura y un seguimiento de los recursos para empresas asociadas específicas. Para obtener más información, vea "[Configuración de una dirección URL de la extranet](https://technet.microsoft.com/88fec9ff-c96c-4d20-8856-0485e7507572)", más adelante en este tema.
-   Para transferir tareas de emisión de licencias del servidor de certificación raíz. Esto puede mejorar el rendimiento en organizaciones que sólo posean un servidor de certificación raíz (en lugar de un clúster de certificación raíz).

Para la mayoría de los fines, es recomendable que agregue servidores de RMS al clúster de certificación raíz, con el fin de configurar la redundancia y el equilibrio de carga en todos los servidores de la implementación. Aunque también se pueden utilizar servidores de licencias para transferir el procesamiento de solicitudes de licencias y de publicación, no se puede realizar el equilibrio de carga de los servidores de licencias con el clúster de certificación raíz. A no ser que exista una necesidad específica de implementar servidores de licencias independientes, es mejor realizar el equilibrio de carga de todos los servidores de RMS haciéndolos miembros del clúster de certificación raíz.

Para obtener instrucciones paso a paso sobre la instalación y el establecimiento de los servicios en línea en un servidor de licencias de RMS, vea [Para instalar RMS con Service Pack 1](https://technet.microsoft.com/dab20175-a690-43f8-b943-768d289daa0d) y [Para establecer los servicios en línea en un servidor de licencias](https://technet.microsoft.com/4d67b898-0ba9-4eef-ab7d-ee0ca55a688e), más adelante en este tema.
