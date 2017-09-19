---
TOCTitle: Requisitos previos y listas de comprobación para RMS
Title: Requisitos previos y listas de comprobación para RMS
ms:assetid: '836d96ef-d0fd-4935-b595-e8dec19cbb2b'
ms:contentKeyID: 18127868
ms:mtpsurl: 'https://technet.microsoft.com/es-es/library/Cc747582(v=WS.10)'
---

Requisitos previos y listas de comprobación para RMS
====================================================

Antes de empezar a instalar RMS, revise los requisitos previos de tecnología para utilizar RMS; todas las tecnologías que se enumeran forman parte de RMS y conocerlas es importante para implementar RMS correctamente. Utilice las listas de comprobación siguientes para crear listas de tareas y planes de implementación y administración de RMS:

-   [Requisitos previos de tecnología](#bkmk_9)
-   [Listas de comprobación para la implementación de RMS](#bkmk_10)
-   [Listas de comprobación para la administración de RMS](#bkmk_14)

<span id="BKMK_9"></span>
Requisitos previos de tecnología
--------------------------------

Esta recopilación de documentación contiene información que sirve para comprender el funcionamiento de Windows RMS, planear y realizar la implementación en su organización y administrar el sistema. Asume que tiene conocimiento de las siguientes áreas:

-   Implementación y administración de Windows Server 2003
-   Implementación y administración de Active Directory
-   Implementación y administración de los Servicios de Microsoft® Internet Information Server (IIS) 6.0
-   Administración de Microsoft® SQL Server™ 2000
-   Conceptos básicos de infraestructura de clave pública (PKI)
-   Seguridad y trabajo en red de servidores

Para obtener más información sobre estos temas, vea “Recursos adicionales” en [Operación de un servidor de RMS, en esta recopilación de documentación.](http://go.microsoft.com/fwlink/?linkid=42495)

<span id="BKMK_10"></span>
Listas de comprobación para la implementación de RMS
----------------------------------------------------

En esta sección se proporcionan listas de comprobación para las tareas de implementación siguientes:

-   [Implementación de una instalación de un solo servidor](#bkmk_11)
-   [Implementación de clústeres de licencias y de certificación raíz](#bkmk_12)
-   [Implementación de RMS entre bosques](#bkmk_13)

Para obtener más información sobre la implementación de RMS, vea [Implementación de un sistema RMS](http://go.microsoft.com/fwlink/?linkid=42494), en esta recopilación de documentación.

<span id="BKMK_11"></span>
Implementación de una instalación de un solo servidor
-----------------------------------------------------

Utilice la siguiente lista de comprobación para implementar un solo servidor de RMS.

###  

<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Paso</th>
<th>Referencia</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><p>Revisar conceptos e información de planeamiento.</p></td>
<td style="border:1px solid black;"><p>&quot;Preparación de una implementación de RMS&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a>.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Revisar los requisitos del sistema y comprobar que todo el hardware y el software necesario están disponibles.</p></td>
<td style="border:1px solid black;"><p>&quot;Requisitos previos de infraestructura para RMS&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=37537">Planeamiento de una implementación de RMS</a>.</p>
<p>&quot;Planeamiento de la infraestructura de servidor de base de datos&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=37537">Planeamiento de una implementación de RMS</a>.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Configurar la infraestructura, incluidos los requisitos previos de hardware y de software, las cuentas administrativas y la compatibilidad con directivas de grupo, según corresponda.</p></td>
<td style="border:1px solid black;"><p>&quot;Preparación de una implementación de RMS&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a>.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Instale y configure RMS en el servidor.</p></td>
<td style="border:1px solid black;"><p>&quot;Configuración de servicios de certificación y emisión de licencias en el primer servidor&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a>.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Probar la implementación.</p></td>
<td style="border:1px solid black;"><p>&quot;Configuración de un entorno de prueba&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a>.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Implemente el servicio RMS en el entorno de producción.</p></td>
<td style="border:1px solid black;"><p>&quot;Definición del ámbito de la implementación de RMS&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a>.</p></td>
</tr>  
</tbody>  
</table>
  
<span id="BKMK_12"></span>  
Implementación de clústeres de licencias y de certificación raíz  
----------------------------------------------------------------
  
Utilice la siguiente lista de comprobación para implementar clústeres de licencias y de certificación raíz.
  
###  

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th>Paso</th>  
<th>Referencia</th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Revisar conceptos e información de planeamiento.</p></td>
<td style="border:1px solid black;"><p>&quot;Preparación de una implementación de RMS&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a>.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Revisar los requisitos del sistema y comprobar que todo el hardware y el software necesario están disponibles.</p></td>
<td style="border:1px solid black;"><p>&quot;Requisitos previos de infraestructura para RMS&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=37537">Planeamiento de una implementación de RMS</a>.</p>
<p>&quot;Planeamiento de la infraestructura de servidor de base de datos&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=37537">Planeamiento de una implementación de RMS</a>.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Revisar el plan de implementación para comprender la topología y los componentes que se instalarán.</p></td>
<td style="border:1px solid black;"><p>&quot;Determinación de la topología de RMS&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=37537">Planeamiento de una implementación de RMS</a>.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Configurar la infraestructura, incluidos los requisitos previos de hardware y de software, las cuentas administrativas y la compatibilidad con directivas de grupo, según corresponda.</p></td>
<td style="border:1px solid black;"><p>&quot;Preparación de una implementación de RMS&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a>.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Instale y configure RMS en los servidores que están en el clúster de certificación raíz.</p></td>
<td style="border:1px solid black;"><p>&quot;Configuración de servicios de certificación y emisión de licencias en el primer servidor&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a>.</p>
<p>&quot;Adición de servidores para permitir la certificación y emisión de licencias&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a>.</p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Instale y configure RMS en los servidores que están en los clústeres de licencias.</p></td>
<td style="border:1px solid black;"><p>&quot;Configuración de servicios de certificación y emisión de licencias en el primer servidor&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a>.</p>
<p>&quot;Adición de servidores para permitir la certificación y emisión de licencias&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a>.</p></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><p>Configurar el equilibrio de carga.</p></td>
<td style="border:1px solid black;"><p>&quot;Expansión de la infraestructura básica para permitir los clústeres&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a>.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Probar la implementación.</p></td>
<td style="border:1px solid black;"><p>&quot;Configuración de un entorno de prueba&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a>.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Implemente el servicio RMS en el entorno de producción.</p></td>
<td style="border:1px solid black;"><p>&quot;Definición del ámbito de la implementación de RMS&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a>.</p></td>
</tr>  
</tbody>  
</table>
  
<span id="BKMK_13"></span>  
Implementación de RMS entre bosques  
-----------------------------------
  
Utilice la lista de comprobación siguiente para implementar RMS entre bosques.
  
###  

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th>Paso</th>  
<th>Referencia</th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Revisar conceptos e información de planeamiento.</p></td>
<td style="border:1px solid black;"><p>&quot;Preparación de una implementación de RMS&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a>.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Configurar los permisos necesarios basándose en el modelo de confianza.</p></td>
<td style="border:1px solid black;"><p>&quot;Implementación de RMS entre bosques&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a>.</p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Defina los atributos de Active Directory adecuados para sus bosques.</p></td>
<td style="border:1px solid black;"><p>&quot;Implementación de RMS entre bosques&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a>.</p></td>
</tr>  
</tbody>  
</table>
  
<span id="BKMK_14"></span>  
Listas de comprobación para la administración de RMS  
----------------------------------------------------
  
En esta sección se proporcionan listas de comprobación para las tareas de administración siguientes:
  
-   [Implementación de una plantilla de directiva de permisos](#bkmk_15)  
-   [Implementación de un nuevo cliente de RMS](#bkmk_16)  
-   [Adición de dominios de usuario de confianza](#bkmk_17)  
-   [Adición de dominios de publicación de confianza](#bkmk_18)
  
Para obtener más información sobre la administración de RMS, vea [Operación de un servidor de RMS, en esta recopilación de documentación.](http://go.microsoft.com/fwlink/?linkid=42495)
  
<span id="BKMK_15"></span>  
Implementación de una plantilla de directiva de permisos  
--------------------------------------------------------
  
Utilice la lista de comprobación siguiente para implementar una plantilla de directiva de permisos.
  
###  

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th>Paso</th>  
<th>Referencia</th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Revisar los conceptos pertinentes.</p></td>
<td style="border:1px solid black;"><p>&quot;Plantillas de directiva de permisos&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42496">Referencia técnica de RMS</a>.</p></td>
</tr>  
<tr class="even">
<td style="border:1px solid black;"><p>Especificar la ubicación de la plantilla de directiva de permisos.</p></td>
<td style="border:1px solid black;"><p>&quot;Para especificar la ubicación de las plantillas de directiva de permisos&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42495">Operación de un servidor de RMS.</a></p></td>
</tr>  
<tr class="odd">
<td style="border:1px solid black;"><p>Crear la plantilla de directiva de permisos.</p></td>
<td style="border:1px solid black;"><p>&quot;Creación y modificación de plantillas de directiva de permisos&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42495">Operación de un servidor de RMS.</a></p>
<p>&quot;Para agregar una plantilla de directiva de permisos&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42495">Operación de un servidor de RMS.</a></p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Distribuir la plantilla de directiva de permisos.</p></td>
<td style="border:1px solid black;"><p>&quot;Distribución de plantillas de directiva de permisos&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42495">Operación de un servidor de RMS.</a></p></td>
</tr>  
</tbody>  
</table>
  
<span id="BKMK_16"></span>  
Implementación de un nuevo cliente de RMS  
-----------------------------------------
  
Utilice la lista de comprobación siguiente para implementar una nueva versión del cliente de RMS.
  
###  

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th>Paso</th>  
<th>Referencia</th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Revisar los conceptos pertinentes.</p></td>
<td style="border:1px solid black;"><p>&quot;Planeamiento de la distribución de clientes&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42494">Implementación de un sistema RMS</a></p>
<p>&quot;Exclusión de versiones de la caja de seguridad&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42495">Operación de un servidor de RMS.</a></p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Para imponer a todos los clientes la actualización a la versión más reciente de cliente, excluya la versión obsoleta de la caja de seguridad.</p></td>
<td style="border:1px solid black;"><p>&quot;Para excluir versiones de la caja de seguridad&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42495">Operación de un servidor de RMS.</a></p></td>
</tr>  
</tbody>  
</table>
  
<span id="BKMK_17"></span>  
Adición de dominios de usuario de confianza  
-------------------------------------------
  
Utilice la lista de comprobación siguiente para agregar un dominio de usuario de confianza.
  
###  

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th>Paso</th>  
<th>Referencia</th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Revisar los conceptos pertinentes.</p></td>
<td style="border:1px solid black;"><p>&quot;Dominios de usuarios de confianza&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42496">Referencia técnica de RMS</a>.</p>
<p>&quot;Adición y desinstalación de dominios de usuarios de confianza&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42495">Operación de un servidor de RMS.</a></p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Obtener el certificado emisor de licencias de servidor del dominio de usuario que se desea agregar. El administrador de la instalación debe proporcionarlo. A continuación, se debe agregar el dominio de usuario a la instalación.</p></td>
<td style="border:1px solid black;"><p>&quot;Para agregar un dominio de usuario de confianza&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42495">Operación de un servidor de RMS.</a></p></td>
</tr>  
</tbody>  
</table>
  
<span id="BKMK_18"></span>  
Adición de dominios de publicación de confianza  
-----------------------------------------------
  
Utilice la lista de comprobación siguiente para agregar un dominio de publicación de confianza.
  
###  

<p> </p>
<table style="border:1px solid black;">  
<colgroup>  
<col width="50%" />  
<col width="50%" />  
</colgroup>  
<thead>  
<tr class="header">  
<th>Paso</th>  
<th>Referencia</th>  
</tr>  
</thead>  
<tbody>  
<tr class="odd">
<td style="border:1px solid black;"><p>Revisar los conceptos pertinentes.</p></td>
<td style="border:1px solid black;"><p>&quot;Dominios de publicación de confianza&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42496">Referencia técnica de RMS</a>.</p>
<p>&quot;Adición y desinstalación de dominios de publicación de confianza&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42495">Operación de un servidor de RMS.</a></p></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><p>Obtener el certificado emisor de licencias de servidor cifradas y la clave privada del dominio de publicación que se desea agregar; a continuación, se debe agregar el dominio a la instalación.</p></td>
<td style="border:1px solid black;"><p>&quot;Para agregar un dominio de publicación de confianza&quot; en <a href="http://go.microsoft.com/fwlink/?linkid=42495">Operación de un servidor de RMS.</a></p></td>
</tr>  
</tbody>  
</table>
