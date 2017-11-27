---
TOCTitle: Planeamiento de una topología de RMS básica
Title: Planeamiento de una topología de RMS básica
ms:assetid: 'fec3201e-201f-4faf-910e-fa44132af83d'
ms:contentKeyID: 18128033
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747755(v=WS.10)'
---

Planeamiento de una topología de RMS básica
===========================================

La topología básica de RMS está formada por uno o varios servidores físicos que sirven como clúster de certificación raíz. Este clúster se utiliza para la certificación, emisión de licencias y publicación en la organización. En todas las implementaciones, excepto las más pequeñas, se suelen configurar varios servidores físicos como clúster detrás de una sola dirección URL. Este clúster se crea estableciendo los servicios en línea en el primer servidor para crear el servidor de certificación raíz, y agregando después servidores al clúster hasta que se haya escalado al número de servidores de certificación raíz necesarios para la actividad proyectada. La siguiente figura ilustra esta topología.

![](images/Cc747755.a3332719-4d25-4694-a89a-7c31fd97ca3b(WS.10).gif)

Cuando se unen servidores a un clúster, comparten las mismas bases de datos de configuración y registro, que son bases de datos de SQL Server. SQL Server puede residir en el servidor de certificación raíz o en un servidor diferente.

El equilibrio de carga se configura en todos los servidores que se encuentran en el clúster de certificación raíz. Todas las solicitudes de certificados y licencias se pasan al clúster de certificación raíz a través de la dirección URL común especificada durante la configuración del primer servidor del clúster.

Si piensa dar servicio a un número pequeño de clientes, puede configurar RMS en un único servidor con una base de datos local. El servidor es responsable de todos los procesos de certificación y emisión de licencias de la organización. Esta configuración proporciona un solo punto de error, por lo que se recomienda realizar copias de seguridad regulares de la configuración.