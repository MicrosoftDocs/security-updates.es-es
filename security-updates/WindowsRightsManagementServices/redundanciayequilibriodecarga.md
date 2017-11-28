---
TOCTitle: Redundancia y equilibrio de carga
Title: Redundancia y equilibrio de carga
ms:assetid: '162d547c-78a7-4848-b43e-58e481832af2'
ms:contentKeyID: 18127690
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720199(v=WS.10)'
---

Redundancia y equilibrio de carga
=================================

Para garantizar que los usuarios puedan adquirir licencias y publicar el contenido cuando sea necesario, se recomienda implementar servidores de RMS redundantes mediante clústeres. Esto significa que como mínimo debe implementar un clúster de certificación raíz que esté formado por al menos dos servidores. Si también implementa un servidor de licencias diferente para dar respuesta a las necesidades de licencias específicas de un grupo concreto de su organización, también debe implementar el servidor de licencias como un clúster de dos servidores como mínimo.

Los diversos servidores físicos del clúster de certificación raíz o de cualquier clúster de licencias constituyen un "conjunto de servidores Web" detrás de una dirección URL compartida o una dirección virtual. Si su organización utiliza un conjunto de servidores, puede integrar RMS en cualquier técnica que utilice para las direcciones virtuales, como DNS de operación por turnos, el servicio de equilibrio de carga de red o una solución de hardware dedicado.

Además del equilibrio de carga, las direcciones virtuales son beneficiosas cuando se utilizan con Windows RMS, porque eliminan la dependencia de cualquier servidor físico para los servicios de certificación o emisión de licencias. Ningún equipo de usuario final requiere acceso directo a ningún servidor que se encuentre en un clúster.