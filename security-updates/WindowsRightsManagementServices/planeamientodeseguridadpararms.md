---
TOCTitle: Planeamiento de seguridad para RMS
Title: Planeamiento de seguridad para RMS
ms:assetid: 'eb0fa784-1246-44aa-be31-2c332db7d09c'
ms:contentKeyID: 18128019
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747719(v=WS.10)'
---

Planeamiento de seguridad para RMS
==================================

Al igual que otros servidores de la organización, debe considerarse la seguridad como parte del planeamiento de implementación. RMS se implementa como servicio Web, de modo que puede controlar el acceso a RMS de la misma forma que lo haría con otros servicios Web, utilizando listas de control de acceso y capa de sockets seguros (SSL).

También puede implementarse RMS como parte de un dominio de acceso controlado si una parte de la implementación requiere RMS para proporcionar una capa adicional de control de la información confidencial.

Puesto que RMS utiliza un sistema de claves privadas para cifrar el contenido, debe guardar y gestionar la clave privada de RMS como parte de su plan de seguridad.

En la documentación se tratan los temas siguientes:

-   [Determinación de los requisitos de acceso](https://technet.microsoft.com/eb2ce9a5-0430-4811-bd40-4a94a84426a8)
-   [Definición de los requisitos de administración de claves](https://technet.microsoft.com/f0e08fb8-bf5e-4278-a09f-daa57696e786)