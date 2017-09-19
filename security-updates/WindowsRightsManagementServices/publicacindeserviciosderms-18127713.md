---
TOCTitle: Publicación de servicios de RMS
Title: Publicación de servicios de RMS
ms:assetid: '3cca9325-6bd3-49ad-aa3f-e0693205d3f4'
ms:contentKeyID: 18127713
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720247(v=WS.10)'
---

Publicación de servicios de RMS
===============================

Las direcciones URL de los servicios de RMS se publican en Active Directory durante el establecimiento de servicios en línea en los servidores. Además, en ese proceso, el programa de instalación de RMS envía una consulta a Active Directory para determinar si se han instalado o no otros servidores de RMS en ese bosque. Si no hay otros servidores instalados, el programa de instalación de RMS configura el servidor como servidor de certificación raíz. Antes de usar RMS, se debe registrar el punto de conexión de servicio (SCP) en Active Directory para permitir que los clientes detecten la dirección URL del servidor de certificación raíz. Los clientes que solicitan conexiones con los servicios que se ejecutan en el servidor de certificación raíz comienzan por enviar una consulta a Active Directory para obtener la dirección URL de este servidor. Para obtener más información, vea "Registro del punto de conexión de servicio" en "Operación de un servidor de RMS", en esta recopilación de documentación.

| ![](images/Cc720247.note(WS.10).gif)Nota                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Si la topología de la empresa incluye varios servidores que forman un clúster de servidores de certificación raíz, la dirección URL señala al servidor encargado de la distribución de la carga del clúster, que el administrador proporciona durante el establecimiento de servicios en línea. |
