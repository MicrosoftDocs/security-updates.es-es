---
TOCTitle: Identificación de los componentes principales
Title: Identificación de los componentes principales
ms:assetid: 'c9ec225b-0e51-42f5-aff6-0aecb62e3b27'
ms:contentKeyID: 18127957
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747751(v=WS.10)'
---

Identificación de los componentes principales
=============================================

Para establecer una topología adecuada, es importante conocer los componentes básicos de una implementación de RMS y las funciones que desempeñan. En la siguiente lista, se identifican los servidores que serán parte de la implementación de RMS:

-   Servidores de certificación raíz. El servidor de certificación raíz es el primer componente de una implementación de RMS; todos los demás componentes dependen de él. El servidor de certificación raíz ejecuta todos los servicios de RMS, incluido el servicio de certificación de cuentas que proporciona certificados de cuenta de RMS a los clientes de RMS de la organización. Sólo puede haber un servidor de certificación raíz en cada bosque de Active Directory. Sin embargo, puede agregar varios servidores a la instalación para crear un clúster de certificación raíz, que se puede usar para la redundancia y el equilibrio de carga. Todos los servidores que forman parte del clúster de certificación raíz utilizan la misma base de datos de configuración que se definió cuando se establecieron los servicios en línea en el primer servidor de certificación de la instalación.
-   Servidores de licencias. Un servidor de licencias es opcional y no forma parte del clúster de certificación raíz; sin embargo, el servidor de licencias está subinscrito en el servidor de certificación raíz. Un servidor de licencias depende del servidor de certificación raíz para la certificación y otros servicios (no puede proporcionar servicios de certificación de cuentas), pero el servidor de licencias ejecuta los servicios de emisión de licencias para proporcionar licencias de publicación y de uso. Para configurar la redundancia y el equilibrio de carga, puede agregar varios servidores a la instalación para crear un clúster de licencias. Todos los servidores que se encuentran en el clúster de licencias utilizan la misma base de datos de configuración que se definió cuando se establecieron los servicios en línea en el primer servidor de licencias de este clúster.
-   Servidores que ejecutan componentes de infraestructura. Los servidores adicionales de su implementación pueden proporcionar la infraestructura necesaria, incluidos componentes como SQL Server 2000 y Active Directory. El lugar en el que implemente estos componentes y el número de servidores necesarios depende de sus requisitos.

La topología de RMS que diseñe para la organización debe solucionar la implementación de cada uno de estos componentes.
