---
TOCTitle: 'Actualización de la implementación con RMS Service Pack 2 (SP2)'
Title: 'Actualización de la implementación con RMS Service Pack 2 (SP2)'
ms:assetid: '27ee06a1-f467-4a6c-b662-45ddb5f8c13e'
ms:contentKeyID: 18127766
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc720225(v=WS.10)'
---

Actualización de la implementación con RMS Service Pack 2 (SP2)
===============================================================

En esta sección se proporciona información para ayudarle a instalar Microsoft® Windows® Rights Management Services (RMS) con Service Pack 2 (SP2) en una organización con una implementación de RMS existente. Sólo las organizaciones que ya han implementado RMS deben actualizar su implementación con RMS con SP2. Las organizaciones que implementan RMS por primera vez pueden implementar RMS con SP2 si siguen las directrices de Planeamiento de una implementación de RMS ([http://go.microsoft.com/fwlink/?LinkId=74999](http://go.microsoft.com/fwlink/?linkid=74999)) e Implementación de un sistema RMS ([http://go.microsoft.com/fwlink/?LinkID=75000](http://go.microsoft.com/fwlink/?linkid=75000)) en esta recopilación de documentación.

Puede instalar RMS con SP2 sin quitar la instalación existente de RMS con SP1. El programa de instalación de RMS con SP2 detecta que RMS con SP1 está instalado y agrega características y configuraciones adicionales según sea necesario.

| ![](images/Cc720225.note(WS.10).gif)Nota                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| No se admite una ruta de actualización desde el servidor de RMS sin Service Pack a RMS con SP2. Si utiliza un servidor de RMS sin Service Pack, debe actualizar a RMS con SP1 antes de actualizar a RMS con SP2. El cliente de RMS se puede actualizar desde cualquier versión anterior del cliente de RMS. |

**En este tema**

-   [Preparar la actualización de RMS con SP2](#bkmk_preparingforsp2update)
-   [Realizar la actualización de RMS con SP2](#bkmk_performingsp2update)
-   [Actualizar clústeres](#bkmk_updateclusters)
-   [Actualizar clientes de RMS](#bkmk_updateclients)
-   [Interoperabilidad con RMS versión 1.0](#bkmk_interop)
-   [Quitar RMS con SP2](#bkmk_removingrms)

<span id="bkmk_PreparingForSP2Update"></span>
Preparar la actualización de RMS con SP2
----------------------------------------

La actualización de RMS con SP2 se ha diseñado para permitir continuar la ejecución de RMS sin interrupciones. No obstante, antes de actualizar el clúster de RMS, se recomienda realizar lo siguiente:

-   Realice una copia de seguridad de la base de datos de configuración y la clave privada de RMS. Para obtener más información, vea Copias de seguridad del sistema para RMS ([http://go.microsoft.com/fwlink/?LinkId=75001](http://go.microsoft.com/fwlink/?linkid=75001)) en esta recopilación de documentación.
-   Si usa una clave privada basada en software, asegúrese de disponer de la contraseña de la clave privada de RMS.
-   Realice la copia de seguridad de la base de datos de registro si desea conservar las estadísticas registradas anteriormente.
-   Asegúrese de que dispone de las actualizaciones críticas y actualizaciones de seguridad más recientes del sistema operativo instalado en sus clientes y servidores. Para comprobar si tiene todas las actualizaciones críticas y actualizaciones de seguridad, haga clic en **Inicio** y en **Windows Update**; a continuación, siga las instrucciones que aparecen en la pantalla.

<span id="bkmk_PerformingSP2Update"></span>
Realizar la actualización de RMS con SP2
----------------------------------------

Cuando el Asistente para la instalación de Rights Management Services con Service Pack 2 detecta la instalación de RMS, busca la instalación de RMS con SP1 actual y agrega sólo los archivos nuevos o reemplaza los archivos que se deben cambiar para RMS con SP2. Si ya está ejecutando RMS correctamente, no necesita efectuar el reaprovisionamiento ni llevar a cabo ninguna configuración adicional después de instalar RMS con SP2 para seguir ejecutando RMS.

<span id="bkmk_UpdateClusters"></span>
Actualizar clústeres
--------------------

Si ha instalado RMS en una configuración de clúster, debe planear la actualización de los clústeres para minimizar la repercusión de la actualización en su instalación. Tenga en cuenta las siguientes recomendaciones cuando determine la mejor forma de implementar RMS con SP2 en su organización:

-   Como procedimiento recomendado, instale RMS con SP2 en una parte de un clúster cada vez, de modo que la actualización del clúster pueda ser más predecible y haya menos probabilidades de que se produzca un deterioro del servicio durante la actualización.
-   Si tiene varios clústeres RMS, debe actualizar los clústeres de certificación raíz en primer lugar y, a continuación, actualizar los clústeres de licencias subinscritos.
-   Si usa la expansión de grupo entre bosques, debe actualizar los clústeres de los bosques independientemente sin que se vea afectada la capacidad de los servidores de RMS de expandir la pertenencia a grupos entre bosques.
-   Los servidores de RMS con SP2, RMS con SP1 y RMS versión 1.0 pueden coexistir e interoperar sólo si están en bosques de Active Directory distintos. No se recomienda tener distintas versiones del servidor de RMS en el mismo clúster.
-   El paquete de instalación de RMS con SP2 también se puede usar para instalar una nueva implementación de RMS con SP2 en un servidor; no requiere que RMS con SP1 esté instalado.

<span id="bkmk_UpdateClients"></span>
Actualizar clientes de RMS
--------------------------

En Windows Update o Centro de descarga de Microsoft hay disponible un nuevo cliente de RMS con SP2. El paquete de instalación del cliente de RMS con SP2 también se puede usar para instalar una nueva versión del cliente de RMS con SP2 en un equipo; no requiere que esté instalada la versión 1.0 del cliente de RMS. El cliente de RMS con SP2 incluye una característica de compatibilidad con versiones anteriores para poderlo usar con aplicaciones habilitadas para RMS que requieran la versión 1.0 de RMS.

Para obtener más información acerca de la actualización e instalación del cliente de RMS, vea Distribución del cliente de RMS ([http://go.microsoft.com/fwlink/?LinkId=75070](http://go.microsoft.com/fwlink/?linkid=75070)).

<span id="bkmk_InterOp"></span>
Interoperabilidad con RMS versión 1.0
-------------------------------------

Debido a que RMS con SP2 proporciona numerosas mejoras de rendimiento, debe instalarlo durante el siguiente ciclo de actualización. Aunque los servidores y clientes de RMS que ejecutan RMS con SP2 son completamente interoperables con los servidores y clientes de RMS que no ejecutan RMS con SP2, tenga en cuenta las siguientes diferencias en el modo en que funcionan en un entorno mixto:

-   Sólo los servidores que ejecutan RMS con SP1 y posterior pueden realizar la inscripción sin conexión.
-   Sólo los clientes que ejecutan RMS con SP1 y posterior se activan automáticamente.
-   En la siguiente tabla se presenta la funcionalidad admitida para entornos mixtos:

###  

 
<table style="border:1px solid black;">
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th style="border:1px solid black;" >Versión de servidor de RMS</th>
<th style="border:1px solid black;" >Características admitidas con los clientes de la versión 1</th>
<th style="border:1px solid black;" >Características admitidas con los clientes de SP2</th>
<th style="border:1px solid black;" >Características admitidas en entornos de clientes mixtos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;">1.0</td>
<td style="border:1px solid black;">Todas las características anteriores.
Sin inscripción sin conexión del servidor. El servidor se debe inscribir a través de Internet.
Sin clientes de activación automática.</td>
<td style="border:1px solid black;">Todas las características anteriores.
Sin inscripción sin conexión del servidor.
Clientes de activación automática.</td>
<td style="border:1px solid black;">Todas las características anteriores.
Los clientes de SP2 se activan automáticamente.
Los clientes de la versión 1 se deben activar a través de Internet.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">SP2</td>
<td style="border:1px solid black;">Todas las características anteriores.
Inscripción sin conexión del servidor.
Sin clientes de activación automática.</td>
<td style="border:1px solid black;">Todas las características de SP1.
Inscripción sin conexión del servidor.
Clientes de activación automática.
Caja de seguridad del servidor.
Microsoft SQL Server™ 2005 se admite de forma predeterminada.</td>
<td style="border:1px solid black;">Todas las características anteriores, además de las de SP2.
Inscripción sin conexión del servidor.
Los clientes de SP2 se activan automáticamente.
Los clientes de la versión 1 se deben activar a través de Internet.</td>
</tr>
</tbody>
</table>
 

<span id="bkmk_RemovingRMS"></span>
Quitar RMS con SP2
------------------

Si desea devolver el servidor de RMS a su configuración anterior después de instalar RMS con SP2, puede usar **Agregar o quitar programas** en **Panel de control** para quitar RMS con SP2.
