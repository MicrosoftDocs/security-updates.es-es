---
TOCTitle: Determinación de la topología de RMS
Title: Determinación de la topología de RMS
ms:assetid: 'bf516f7d-b3a1-4e7f-971f-bfab1db41812'
ms:contentKeyID: 18127927
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747651(v=WS.10)'
---

Determinación de la topología de RMS
====================================

En la topología de RMS básica, el clúster o servidor de certificación raíz de cada bosque de Active Directory proporciona todos los servicios de RMS para una organización. Esta topología de RMS funciona bien en organizaciones pequeñas y grandes. En una topología de RMS distribuida, uno o más servidores de licencias (a veces conocidos como servidores de licencias departamentales) pueden proporcionar algunos o todos los servicios de emisión de licencias a grupos y usuarios específicos que se encuentran en la organización. Aunque el servidor (o clúster) de certificación raíz continúa proporcionando la certificación de cuentas y los servicios proxy de activación para toda la organización, la topología de RMS distribuida está diseñada para organizaciones que tienen necesidades de licencias muy específicas y que desean mantener el control de RMS en un segmento de la organización.

Aunque sólo hay dos topologías de RMS básicas, los componentes de las topologías pueden ser muy diferentes. Para definir los componentes que son adecuados para la organización y crear la topología correcta para la implementación de RMS, debe:

-   Evaluar los objetivos y requisitos de la organización.
-   Definir cómo se debe usar la administración de permisos.
-   Analizar las cargas y los patrones de tráfico proyectados para implementar un nivel de servicio adecuado.

La definición de la topología y la toma de decisiones necesarias para implementar el diseño son un proceso repetitivo que continuará a lo largo del proceso de planeamiento de la implementación de RMS.

En este tema, se tratan los siguientes aspectos:

-   [Identificación de los componentes principales](https://technet.microsoft.com/c9ec225b-0e51-42f5-aff6-0aecb62e3b27)
-   [Establecimiento de los objetivos de la topología](https://technet.microsoft.com/8275a04d-3e5b-40b0-be9d-2f31b7aeca6b)
-   [Definición del ámbito de la implementación de RMS](https://technet.microsoft.com/4b5fe1be-643e-47c4-bf9b-50d1e97108fb)
-   [Evaluación de los requisitos de escala](https://technet.microsoft.com/89f0138c-946d-47d7-a286-041d4d9606a8)
-   [Redundancia y equilibrio de carga](https://technet.microsoft.com/162d547c-78a7-4848-b43e-58e481832af2)
-   [Evaluación de los requisitos de migración](https://technet.microsoft.com/cec07f45-dc52-4004-860b-5cc33e5fc209)
-   [Planeamiento de la infraestructura de servidor de base de datos](https://technet.microsoft.com/b12354bd-3143-4d1f-b5aa-450c4550653c)
-   [Planeamiento de la implementación entre bosques](https://technet.microsoft.com/2dfb40b7-95b1-4362-b32e-72867544b705)
-   [Planeamiento de usuarios externos de RMS](https://technet.microsoft.com/107e1338-4dcf-4ed5-a49d-e875cc883db1)
-   [Planeamiento de una topología de RMS básica](https://technet.microsoft.com/fec3201e-201f-4faf-910e-fa44132af83d)
-   [Planeamiento de una topología de RMS distribuida](https://technet.microsoft.com/8773a1e0-6ac3-41f5-9866-5890cef08d04)
