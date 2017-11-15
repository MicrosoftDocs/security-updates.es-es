---
TOCTitle: Adición de servidores para permitir la certificación y emisión de licencias
Title: Adición de servidores para permitir la certificación y emisión de licencias
ms:assetid: '089ceb62-2a96-444f-ab42-1d5deaabd0c3'
ms:contentKeyID: 18127717
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720189(v=WS.10)'
---

Adición de servidores para permitir la certificación y emisión de licencias
===========================================================================

Una vez que haya instalado y establecido los servicios en línea del primer servidor para la instalación raíz de RMS, puede configurar servidores adicionales para proporcionar compatibilidad extendida para los servicios de certificación y licencia, como:

-   Puede agregar un servidor como miembro del clúster de certificación raíz para proporcionar un mayor servicio de certificación y emisión de licencias. Un servidor que se añade a este clúster utiliza la misma configuración y las mismas bases de datos que el servidor de certificación raíz.
-   Puede configurar un servidor de licencias independiente o que forme parte de un clúster de servidor de licencias. Está subinscrito en el clúster de certificación raíz y recibe su certificado emisor de licencias de servidor (SLC) a través de los servicios de certificación del servidor de certificación raíz. Todas las solicitudes de servicios de certificación de clientes que se envíen al servidor de licencias se reenvían al servidor de certificación. El servidor de licencias puede emitir licencias de uso y publicación sin enviar la solicitud al servidor de certificación raíz.

La opción que decida implementar depende del tamaño de la organización y de cómo desea implementar elementos como redundancia, escala, compatibilidad con equilibrio de carga y seguridad. Si va a implementar servidores de RMS adicionales para hacer frente al aumento de la demanda de publicación, certificación y emisión de licencias, debe implementar los servidores de RMS como parte del clúster de certificación raíz, de manera que pueda configurar la redundancia y el equilibrio de carga en todos ellos. Puede agrupar servidores de certificación y transferir el procesamiento de servicios de publicación y emisión de licencias subinscribiendo servidores de licencias (que también pueden ser agrupados para realizar el equilibrio de carga), pero no puede realizar el equilibrio de carga de un clúster de licencias subinscrito con un clúster de certificación raíz.

Los temas siguientes proporcionan una orientación sobre esta tarea:

-   [Funciones, permisos y derechos requeridos para la instalación y el establecimiento de servicios en línea](#bkmk_1)
-   [Procesos de establecimiento de servicios en línea para la certificación adicional y los servidores de licencias](#bkmk_2)
-   [Configuración de clústeres y equilibrio de carga](#bkmk_3)

Funciones, permisos y derechos requeridos para la instalación y el establecimiento de servicios en línea
--------------------------------------------------------------------------------------------------------

Para instalar servidores adicionales y establecer los servicios en línea en ellos, precisa las mismas funciones y permisos que para configurar el servidor inicial. Además, también debe tener permiso del servidor de certificación raíz para configurar un servidor de licencias separado, lo que se conoce como subinscripción. El servidor de certificación raíz se controla a través del DACL del archivo SubEnrollService.asmx. Los miembros del grupo de servicio de RMS, incluida la cuenta de servicio de RMS que especifica durante el establecimiento de los servicios en línea del servidor de certificación raíz, tienen permiso para llevar a cabo la subinscripción. Para obtener más información, vea “[Configuración de los servicios de certificación y emisión de licencias en el primer servidor](https://technet.microsoft.com/cce29a2f-984f-48ed-9187-0eb68286ec5b)”, anteriormente en este tema.

Procesos de establecimiento de servicios en línea para la certificación adicional y los servidores de licencias
---------------------------------------------------------------------------------------------------------------

Para agregar servidores a los clústeres de certificación y licencias, es preciso que el servidor complete el proceso de establecimiento de los servicios en línea. Este proceso varía según el tipo de servidor en el que se estén estableciendo los servicios en línea.

-   Si está estableciendo los servicios en línea de un servidor de licencias independiente, especifique una base de datos de configuración, una cuenta de servicio RMS, una URL de clúster y la información de protección de clave privada de la misma forma que especificó esta información para un servidor de certificación raíz. Sin embargo, no especifique una directiva de revocación de certificado emisor de licencias de servidor, ya que esta directiva está bajo control del servidor de certificación raíz.
-   Si está estableciendo los servicios en línea de un servidor como miembro del clúster, la única información que necesita especificar durante el establecimiento de los servicios en línea es la cuenta de servicio de RMS, la base de datos de configuración y la contraseña para la protección de clave privada (o utilizar el mismo CSP y la misma clave privada que en el clúster existente). Todos los servidores de un clúster comparten el mismo certificado emisor de licencias de servidor y el mismo par de claves de servidor.

> [!IMPORTANT]
> No empiece a instalar RMS en ningún otro servidor hasta que haya completado la configuración de RMS en el primer servidor, incluida la instalación y el establecimiento de los servicios en línea del servidor. 

Una vez que haya instalado y establecido los servicios en línea de un servidor adicional, queda configurado automáticamente como miembro del clúster. Sin embargo, si ha implementado el equilibrio de carga, debe configurar el software de equilibrio de carga para que funcione con el nuevo servidor

Configuración de clústeres y equilibrio de carga
------------------------------------------------

RMS está diseñado para permitir los clústeres de servidor. Crear clústeres de servidores de RMS proporciona mayor escalabilidad, confiabilidad y equilibrio de carga a la implementación de RMS.

**Creación de clústeres**

Para configurar un clúster, empiece con un servidor de certificación raíz o un servidor de licencias. Para el segundo servidor y los posteriores de cada clúster, instale RMS en el nuevo servidor, vaya a la página **Administración global** y haga clic en **Agregar este servidor a un clúster** para establecer los recursos necesarios y unir el servidor al clúster de certificación raíz o clúster de licencias.

Especifique un nombre de base de datos para el clúster que desea unir.

**Realizar el equilibrio de carga de los clústeres**

RMS no implementa automáticamente el equilibrio de carga. Puede utilizar equilibrio de carga de hardware o software, incluido el equilibrio de carga de red, para equilibrar la carga entre todos los servidores de RMS.

Los siguientes temas proporcionan información más detallada sobre esta materia:

-   Para obtener más información acerca de las diferencias entre servicios de certificación y licencia, vea "Información general del sistema RMS" en "Referencia técnica de RMS", en esta recopilación de documentación.
-   Para obtener más información acerca de cómo ajustar la implementación de servidores a los requisitos de disponibilidad y rendimiento de su organización, vea "Redundancia y equilibrio de carga" en "Planeamiento de una implementación de RMS", en esta recopilación de documentación.
-   Para obtener más información acerca de cómo determinar el número de servidores necesarios para permitir la implementación de RMS en su organización, vea "Evaluación de los requisitos de escala" en "Planeamiento de una implementación de RMS", en esta recopilación de documentación.
-   Para obtener más información acerca de cómo implementar la seguridad de IT con su implementación de RMS, vea "[Protección de la implementación de RMS](https://technet.microsoft.com/6de8b636-a824-4844-aefc-f26347abfc14)", más adelante en este tema.
-   Para obtener más información acerca de cómo instalar RMS, vea "Para instalar RMS con Service Pack 1" en "Operación de un servidor de RMS", en esta recopilación de documentación.
    También puede instalar RMS desde el símbolo del sistema. Para obtener más información, vea “Instalación de RMS desde el símbolo del sistema” en “Operación de un servidor de RMS”, en esta recopilación de documentación.
-   Para obtener más información acerca de cómo establecer los servicios en línea de un servidor de licencias, vea "Para establecer los servicios en línea de un servidor de licencias" en "Operación de un servidor de RMS", en esta recopilación de documentación.
-   Para obtener más información acerca de cómo establecer los servicios en línea de servidores adicionales en un clúster, vea "Para agregar un servidor a un clúster" en "Operación de un servidor de RMS", en esta recopilación de documentación
