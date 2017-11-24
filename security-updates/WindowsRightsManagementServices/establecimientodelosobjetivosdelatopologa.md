---
TOCTitle: Establecimiento de los objetivos de la topología
Title: Establecimiento de los objetivos de la topología
ms:assetid: '8275a04d-3e5b-40b0-be9d-2f31b7aeca6b'
ms:contentKeyID: 18127856
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747652(v=WS.10)'
---

Establecimiento de los objetivos de la topología
================================================

Uno de los pasos más importantes del diseño de la topología es establecer los objetivos adecuados. Algunas de las áreas clave que debe tratar en el diseño de la topología de RMS son:

-   **Costos administrativos**. La topología del sitio debe minimizar los costos administrativos. Esto incluye la centralización de la administración de servidores siempre que sea posible y la minimización del número de servidores utilizados.
-   **Latencia de red**. La latencia de la red entre el cliente y el servidor será percibida por los usuarios como una demora adicional cuando abran documentos y correo electrónico. En general, asegúrese de que la latencia sea inferior a dos segundos para cada dirección, al menos el 90 por ciento del tiempo.
-   **Confiabilidad**. La red entre el cliente y el servidor debe ser suficientemente confiable para que una sola solicitud HTTP y su respuesta tenga un índice de errores, es decir transacciones dañadas o perdidas, de menos del 5 por ciento.

Éstas son sólo directrices; debe establecer sus propios objetivos basándose en los recursos y los requisitos de su organización. El establecimiento de objetivos es el punto de partida para determinar si la topología satisface sus necesidades. Existen numerosos factores que afectan a la forma en que se cumplen los objetivos, incluidos el número de usuarios, solicitudes de licencias, consultas, mensajes y otros factores de tráfico relacionados con RMS. Además, la estrategia de implementación, que incluye en qué dominios y bosques se planea implementar RMS, puede tener un impacto significativo en la consecución de los objetivos de la topología. A medida que avanza por el proceso de diseño de la topología debe tener en cuenta sus objetivos y determinar qué impacto tendrá cada proceso de diseño en ellos.
