---
TOCTitle: Evaluación de los requisitos de escala
Title: Evaluación de los requisitos de escala
ms:assetid: '89f0138c-946d-47d7-a286-041d4d9606a8'
ms:contentKeyID: 18127858
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747663(v=WS.10)'
---

Evaluación de los requisitos de escala
======================================

Para decidir si hay que implementar uno o varios servidores, determine cuántos usuarios utilizarán la implementación de RMS y cuántos archivos protegerán.

Esto proporciona los requisitos de uso medio. Planee los requisitos de uso máximo, que probablemente será tres veces más que los requisitos de uso medio.

Tenga en cuenta también los estándares de tolerancia a errores y de disponibilidad de servicio de la compañía.

Para establecer una medición del rendimiento, RMS se probó utilizando un servidor Pentium 4 a 2,4 GHz con procesador dual y 1 GB de RAM. En esta configuración, el servidor de RMS proporcionó aproximadamente 50 licencias por segundo.

Puede utilizar las siguientes cifras durante el planeamiento de la capacidad para calcular los requisitos de uso para un sistema RMS.

###  

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Transacción</th>
<th style="border:1px solid black;" >Incidencia</th>
<th style="border:1px solid black;" >Uso de ancho de banda de cliente a servidor (KB)</th>
<th style="border:1px solid black;" >Uso de ancho de banda de servidor a cliente (KB)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Solicitud de licencia</td>
<td style="border:1px solid black;">Repetida para cada usuario y cada fragmento de contenido</td>
<td style="border:1px solid black;">64</td>
<td style="border:1px solid black;">18</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Certificación de cuenta de permisos</td>
<td style="border:1px solid black;">Sólo tráfico de inicialización de RMS</td>
<td style="border:1px solid black;">12</td>
<td style="border:1px solid black;">16</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Inscripción de clientes</td>
<td style="border:1px solid black;">Sólo tráfico de inicialización de RMS</td>
<td style="border:1px solid black;">17</td>
<td style="border:1px solid black;">16</td>
</tr>
</tbody>
</table>
  
Además, el tráfico de consulta de Active Directory puede tener un impacto en el rendimiento de la red. Sin embargo, este no suele ser un factor si implementa servidores de RMS muy próximos a los servidores de catálogo global. La excepción se daría si un error de todos los servidores de catálogo global en un sitio causara una conmutación por error a otro sitio con una conexión que no tenía la misma capacidad.
  
En la siguiente tabla se proporcionan datos de línea de base sobre el uso del ancho de banda de las transacciones de RMS, que puede utilizar para evaluar el efecto del tráfico de consulta de Active Directory en la red de la organización.
  
###  

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Transacción</th>
<th style="border:1px solid black;" >Uso del ancho de banda de RMS al catálogo global (bytes)</th>
<th style="border:1px solid black;" >Uso del ancho de banda del catálogo global a RMS (bytes)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Establecimiento de conexión de RMS (ldap_bind)</td>
<td style="border:1px solid black;">1600</td>
<td style="border:1px solid black;">200</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Evaluación de pertenencia a grupos de RMS (ldap_search)</td>
<td style="border:1px solid black;">200</td>
<td style="border:1px solid black;">100</td>
</tr>
</tbody>
</table>
  
Al utilizar estas tablas de referencia, asegúrese de que está aplicando los datos de contenido de su implementación. Por ejemplo, si el usuario pertenece a 15 grupos, se necesitarán 200 bytes para la solicitud de búsqueda de RMS y 1.500 bytes (100 bytes x 15) para la respuesta del catálogo global.
  
El planeamiento de capacidad debe basarse en las cargas de solicitudes de licencia de contenido anticipadas, ya que las cargas de solicitudes de licencia de contenido representan la mayoría de las operaciones que lleva a cabo RMS. La velocidad de entrada y de salida y el rendimiento de la unidad de disco no son factores críticos para RMS, ya que las solicitudes de licencias no transfieren muchos datos y pueden basarse completamente en la información almacenada en la memoria caché.
  
El uso de CPU es la variable más importante para determinar el rendimiento del procesador. Por este motivo es esencial elegir los procesadores adecuados. Los requisitos de memoria de los servidores de RMS aumentan a medida que se incrementa la carga de los servidores y va más allá del rendimiento del servidor. Cuando esto se produce, los Servicios de Internet Information Server (IIS) ponen en cola las solicitudes entrantes en memoria hasta que el servidor puede procesarlas. En función del límite de cola que se configure en IIS, las solicitudes entrantes dejan de ponerse en cola y, en su lugar, se rechazan cuando la cola llega a la longitud máxima especificada.
  
Los requisitos de memoria de RMS (conjunto de trabajo) para un modelo de carga deben ajustarse totalmente a los límites del tamaño de la memoria física. El tamaño total de memoria viene condicionado por las necesidades de almacenamiento en memoria caché de la expansión de grupos más que por ningún otro factor. Se recomienda como mínimo 1 GB de RAM para cada servidor que ejecuta RMS.
  
Cada servidor de RMS es capaz de procesar un número definido de solicitudes de cliente en un período de tiempo definido (aproximadamente de 30 a 50 licencias por segundo). Por este motivo, al agregar servidores linealmente, se escala horizontalmente la capacidad de emisión de licencias de un clúster y también se proporciona una mayor confiabilidad. Como resultado, la escala debe ser adecuada no sólo para cada servidor individual, sino también para el número de servidores que se implementan. Los siguientes ejemplos de configuración muestran cómo puede utilizar estas estimaciones para calcular los requisitos de escalado para la implementación de RMS.
  
-   Configuración de uso ligero  
    Algunas organizaciones tienen requisitos muy bajos de uso para RMS. Por ejemplo, en una organización con aproximadamente 5.000 usuarios, el 10% de los cuales utiliza regularmente RMS para proteger contenido de correo electrónico, puede calcular que un usuario medio protegerá 3 mensajes de correo electrónico por hora. Basándose en esos requisitos, los servidores de RMS deberán proporcionar 1.500 licencias por hora, lo que equivale a 0,42 licencias por segundo. Esto le proporciona los requisitos de uso medio; la multiplicación de esta cifra por 3 proporciona el cálculo de uso máximo de 1,25 licencias por segundo.  
    Según este cálculo, el uso es muy reducido. Por este motivo, un solo servidor de RMS es adecuado para esta organización.  
-   Configuración de uso medio  
    Muchas organizaciones tienen grupos de usuarios bastante grandes con requisitos de uso moderados. Por ejemplo, en una organización que tiene aproximadamente 40.000 usuarios, el 50% de los cuales utiliza regularmente RMS para proteger contenido, puede calcular que un usuario medio protegerá 7 mensajes de correo electrónico y 1 documento u otro archivo por hora. Basándose en esos requisitos, los servidores de RMS deberán proporcionar 160.000 licencias por hora, lo que equivale a 44,4 licencias por segundo. Esto le proporciona los requisitos de uso medio; la multiplicación de esta cifra por 3 proporciona el cálculo de uso máximo de 133,3 licencias por segundo.  
    Según este cálculo, el uso sería moderadamente alto y 3 servidores de RMS serían adecuados para satisfacer las necesidades actuales de los usuarios, mientras que 6 servidores de RMS satisfarían las necesidades actuales de los usuarios y dejarían espacio para seguir creciendo.  
-   Configuración de uso intensivo  
    Las organizaciones grandes a menudo tienen grupos de usuarios muy grandes con requisitos de uso intensivo. Por ejemplo, en una organización con aproximadamente 150.000 usuarios, el 70% por ciento de los cuales utiliza regularmente RMS para proteger contenido, puede calcular que un usuario medio protegerá 15 mensajes de correo electrónico y 3 documentos u otros archivos por hora. Basándose en esos requisitos, los servidores de RMS deberán proporcionar 1.890.000 licencias por hora, lo que equivale a 525 licencias por segundo. Esto le proporciona los requisitos de uso medio; la multiplicación de esta cifra por 3 proporciona el cálculo de uso máximo de 1575 licencias por segundo.  
    Según este cálculo, el uso sería muy alto y serían necesarios 32 servidores de RMS para satisfacer las necesidades actuales de los usuarios, mientras que 51 servidores de RMS satisfarían las necesidades actuales y dejarían espacio para seguir creciendo.
  
Cuando los cálculos indican que se entregan de 30 a 50 licencias por segundo, se necesita otro servidor de RMS.
