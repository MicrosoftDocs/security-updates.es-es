---
TOCTitle: 'Actualización de la implementación con Service Pack 1 (SP1) de RMS'
Title: 'Actualización de la implementación con Service Pack 1 (SP1) de RMS'
ms:assetid: 'a562c4b0-15df-46db-9d61-24db74871cfa'
ms:contentKeyID: 18127900
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747714(v=WS.10)'
---

Actualización de la implementación con Service Pack 1 (SP1) de RMS
==================================================================

En esta sección se proporciona información para ayudarle a instalar Microsoft® Windows® Rights Management Services (RMS) Service Pack 1 (SP1) en una organización con una implementación de RMS existente. Sólo las organizaciones que ya han implementado RMS deben actualizar su implementación con RMS SP1. Las organizaciones que implementan RMS por primera vez pueden implementar RMS con SP1 si siguen las directrices de Planeamiento de una implementación de RMS e Implementación de un sistema RMS.

Puede instalar RMS SP1 sin quitar la instalación existente de RMS. El programa de instalación de RMS SP1 detecta que RMS está instalado y agrega características y configuraciones adicionales según sea necesario.

**En este tema**

-   [Preparar la actualización de RMS SP1](#bkmk_1)
-   [Realizar la actualización de RMS SP1](#bkmk_2)
-   [Actualizar clústeres](#bkmk_3)
-   [Actualizar clientes de RMS](#bkmk_4)
-   [Interoperabilidad con RMS versión 1.0](#bkmk_5)
-   [Quitar RMS con SP1](#bkmk_6)

<span id="BKMK_1"></span>
Preparar la actualización de RMS SP1
------------------------------------

La actualización de RMS SP1 se ha diseñado para permitir continuar las operaciones de RMS sin interrupciones. No obstante, antes de actualizar los servidores de RMS, se recomienda realizar lo siguiente:

-   Realice una copia de seguridad de la base de datos de configuración y la clave privada de RMS. Para obtener más información, vea "Copias de seguridad del sistema para RMS" en la sección "Planeamiento de una implementación de RMS" de esta recopilación de documentación.
-   Asegúrese de que dispone de la contraseña de clave privada.
-   Realice la copia de seguridad de la base de datos de registro si desea conservar las estadísticas registradas anteriormente.
-   Asegúrese de que dispone de las actualizaciones críticas y actualizaciones de seguridad más recientes del sistema operativo instalado en sus clientes y servidores. Para comprobar si tiene todas las actualizaciones críticas y actualizaciones de seguridad, haga clic en **Inicio** y en **Windows Update**; a continuación, siga las instrucciones que aparecen en la pantalla.

<span id="BKMK_2"></span>
Realizar la actualización de RMS SP1
------------------------------------

Cuando el Asistente para la instalación de RMS SP1 detecta su instalación de RMS, sólo agrega los archivos nuevos o reemplaza los que se deben cambiar para RMS SP1. Si ya está ejecutando RMS correctamente, no necesita efectuar el reaprovisionamiento ni llevar a cabo ninguna configuración adicional después de instalar RMS SP1 para seguir ejecutando RMS.

<span id="BKMK_3"></span>
Actualizar clústeres
--------------------

Si ha instalado RMS en una configuración de clúster, debe planear la actualización de los clústeres para minimizar la repercusión de la actualización en su instalación. Tenga en cuenta las siguientes recomendaciones cuando determine la mejor forma de implementar RMS SP1 en su organización:

-   Como procedimiento recomendado, instale RMS SP1 en una parte de un clúster cada vez, de modo que la actualización del clúster pueda ser más predecible y haya menos probabilidades de que se produzca un deterioro del servicio durante la actualización.
-   Si tiene varios clústeres RMS, debe actualizar los clústeres de certificación raíz en primer lugar y, a continuación, actualizar los clústeres de licencias subinscritos.
-   Si usa la expansión de grupo entre bosques, debe actualizar los clústeres de los bosques independientemente sin que se vea afectada la capacidad de los servidores de RMS de expandir la pertenencia a grupos entre bosques.
-   Los servidores de RMS SP1 y RMS versión 1.0 pueden coexistir e interoperar.
-   El paquete de instalación de RMS SP1 también se puede usar para instalar una nueva versión de RMS SP1 en un servidor; no requiere que RMS versión 1.0 esté instalado.

<span id="BKMK_4"></span>
Actualizar clientes de RMS
--------------------------

En RMS con SP1 se incluye un nuevo cliente de RMS. El paquete de instalación del cliente de RMS SP1 también se puede usar para instalar una nueva versión del cliente de RMS SP1 en un equipo; no requiere que esté instalada la versión 1.0 del cliente de RMS. El cliente de RMS SP1 incluye una característica de compatibilidad con versiones anteriores para poderlo usar con aplicaciones habilitadas para RMS que requieran la versión 1.0 de RMS.

Este nuevo cliente de RMS proporciona las siguientes características:

-   El cliente ya no se debe conectar a Microsoft a través de Internet y descargar una caja de seguridad.
-   Si instala el cliente de RMS con una directiva de SMS o de grupo, no se requieren privilegios de administrador para la instalación.
-   El cliente de RMS SP1 incluye una nueva caja de seguridad de servidor (también denominada procesador de seguridad de servidor) que se puede usar para los servicios web habilitados para RMS o aplicaciones en el servidor, como Windows SharePoint® Services y Exchange Server 2003, con el fin de permitir que el servicio consuma y distribuya contenido protegido con RMS. Esta caja se ha diseñado para tener un elevado rendimiento y escalabilidad cuando se usa en aplicaciones de servidor de confianza
-   El cliente de RMS usa algoritmos de cifrado con certificado FIPS 140-2. Esto permite que el cliente se implemente en una organización compatible con FIPS.

<span id="BKMK_5"></span>
Interoperabilidad con RMS versión 1.0
-------------------------------------

Debido a que RMS SP1 proporciona numerosas mejoras de rendimiento, debe instalarlo después de haber completado las pruebas. Aunque los servidores y clientes de RMS que ejecutan RMS SP1 son completamente interoperables con los servidores y clientes de RMS que no ejecutan RMS SP1, tenga en cuenta las siguientes diferencias en el modo en que funcionan en un entorno mixto:

-   Sólo los servidores que ejecutan RMS SP1 pueden realizar la inscripción sin conexión.
-   Sólo los clientes que ejecutan RMS SP1 y posterior se activan automáticamente.
-   En la siguiente tabla se presenta la funcionalidad admitida para entornos mixtos:

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
<th>Versión de servidor de RMS</th>
<th>Características admitidas con los clientes de la versión 1</th>
<th>Características admitidas con los clientes de SP1</th>
<th>Características admitidas en entornos de clientes mixtos (versión 1 y SP1)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>1.0</p></td>
<td style="border:1px solid black;"><p>Todas las características anteriores.</p>
<p>Sin inscripción sin conexión del servidor. El servidor se debe inscribir a través de Internet.</p>
<p>Sin clientes de activación automática.</p></td>
<td style="border:1px solid black;"><p>Todas las características anteriores.</p>
<p>Sin inscripción sin conexión del servidor.</p>
<p>Clientes de activación automática.</p></td>
<td style="border:1px solid black;"><p>Todas las características anteriores.</p>
<p>Los clientes de SP1 se activan automáticamente.</p>
<p>Los clientes de la versión 1 se deben activar a través de Internet.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>SP1</p></td>
<td style="border:1px solid black;"><p>Todas las características anteriores.</p>
<p>Inscripción sin conexión del servidor.</p>
<p>Sin clientes de activación automática.</p></td>
<td style="border:1px solid black;"><p>Todas las características de SP1.</p>
<p>Inscripción sin conexión del servidor.</p>
<p>Clientes de activación automática.</p>
<p>Caja de seguridad del servidor.</p></td>
<td style="border:1px solid black;"><p>Todas las características anteriores, además de las de SP1.</p>
<p>Inscripción sin conexión del servidor.</p>
<p>Los clientes de SP1 se activan automáticamente.</p>
<p>Los clientes de la versión 1 se deben activar a través de Internet.</p></td>
</tr>
</tbody>
</table>
<p> </p>

<span id="BKMK_6"></span>
Quitar RMS con SP1
------------------

Si desea devolver el servidor de RMS a su configuración anterior después de instalar RMS SP1, puede usar **Agregar o quitar programas** en **Panel de control** para quitar RMS SP1.

**Nota**   Si ha efectuado una copia de seguridad de la base de datos de configuración antes de instalar RMS SP1, puede restaurarla para quitar por completo todos los cambios de RMS SP1. Si no realizó una copia de seguridad de la base de datos de configuración, podrá usar la base de datos de configuración de la instalación de RMS SP1 con la instalación de RMS restaurada. La instalación de RMS restaurada pasará por alto los campos adicionales que la instalación de RMS SP1 agrega a la base de datos de configuración porque no los usa.
