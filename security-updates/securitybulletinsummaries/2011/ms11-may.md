---
TOCTitle: 'MS11-MAY'
Title: Resumen del boletín de seguridad de Microsoft de mayo 2011
ms:assetid: 'ms11-may'
ms:contentKeyID: 61225428
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms11-may(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de mayo 2011
==========================================================

Publicado: martes, 10 de mayo de 2011 | Actualizado: martes, 14 de junio de 2011

**Versión:** 1.2

Este resumen del boletín enumera los boletines de seguridad publicados para mayo de 2011.

Con la publicación de los boletines de seguridad de mayo de 2011, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 5 de mayo de 2011. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213) .

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 11 de mayo de 2011, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora a la conferencia en línea del boletín de seguridad de mayo](https://msevents.microsoft.com/cui/webcasteventdetails.aspx?culture=en-us&eventid=1032455071&eventcategory=4) . Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary) .

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional** .

### Información del boletín

Resúmenes ejecutivos
--------------------

En la tabla siguiente se resumen los boletines de seguridad de este mes por orden de gravedad.

Para obtener detalles acerca del software afectado, vea la siguiente sección, **Ubicaciones de descarga y software afectado** .

 
<p> </p>
<table style="border:1px solid black;">
<thead>
<tr class="header">
<th style="border:1px solid black;" >Identificador del boletín</th>
<th style="border:1px solid black;" >Título de boletín y resumen ejecutivo</th>
<th style="border:1px solid black;" >Clasificación máxima de gravedad y consecuencias de la vulnerabilidad</th>
<th style="border:1px solid black;" >Requisito de reinicio</th>
<th style="border:1px solid black;" >Software afectado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms11-035">MS11-035</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en WINS podría permitir la ejecución remota de código (2524426)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Servicio de nombres Internet de Windows (WINS). La vulnerabilidad podría permitir la ejecución remota de código si un usuario recibe un paquete de réplica de WINS especialmente diseñado en un sistema afectado que ejecuta el servicio WINS. De forma predeterminada, WINS no se instala en ningún sistema operativo afectado. Sólo los clientes que instalaron manualmente este componente están afectados por este problema.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms11-036">MS11-036</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft PowerPoint podrían permitir la ejecución remota de código (2545814)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft PowerPoint. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario abre un archivo de PowerPoint especialmente diseñado. Un intruso que aprovechara cualquiera de estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario que ha iniciado sesión. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos. La instalación y configuración de Validación de documento de Office (OFV) para prevenir la apertura de archivos sospechosos bloquea las vías de ataque para aprovechar las vulnerabilidades descritas en CVE-2011-1269 y CVE-2011-1270.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de nivel de evaluación de explotabilidad decreciente y, a continuación, por identificador de CVE. Sólo se incluyen las vulnerabilidades que tiene una clasificación de gravedad de crítica o importante en los boletines.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de las vulnerabilidades de ejecución de código y de denegación de servicio en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Revise cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación de las actualizaciones de este mes. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/es-es/security/cc998259.aspx) .
  
En las columnas siguientes, "Última versión de software" hace referencia al software en cuestión y "Versiones de software anteriores" hace referencia a todas las versiones anteriores y compatibles del software en cuestión, tal como se muestra en las tablas "Software afectado" y "Software no afectado" del boletín.
  
| Identificador del boletín                                           | Título de vulnerabilidad                                                                            | Identificador CVE                                                                | Evaluación de explotabilidad de ejecución de código para la última versión de software                                       | Evaluación de explotabilidad de ejecución de código para las versiones de software anteriores                                       | Evaluación de explotabilidad de denegación de servicio | Notas clave |  
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|-------------|  
| [MS11-036](http://technet.microsoft.com/security/bulletin/ms11-036) | Vulnerabilidad de ejecución remota de código por daños en la memoria relacionada con presentaciones | [CVE-2011-1269](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1269) | No está afectada                                                                                                             | [1](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | No aplicable                                           | (Ninguna)   |  
| [MS11-035](http://technet.microsoft.com/security/bulletin/ms11-035) | Vulnerabilidad de error de respuesta en el servicio WINS                                            | [CVE-2011-1248](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1248) | [2](http://technet.microsoft.com/es-es/security/cc998259.aspx) – Poca probabilidad de código que aproveche la vulnerabilidad | [2](http://technet.microsoft.com/es-es/security/cc998259.aspx) – Poca probabilidad de código que aproveche la vulnerabilidad        | Temporal                                               | (Ninguna)   |  
| [MS11-036](http://technet.microsoft.com/security/bulletin/ms11-036) | Vulnerabilidad de ejecución remota de código por desbordamiento del búfer en las presentaciones     | [CVE-2011-1270](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1270) | No está afectada                                                                                                             | [3](http://technet.microsoft.com/es-es/security/cc998259.aspx) – Improbabilidad de código funcional que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)   |
  
Ubicaciones de descarga y software afectado  
-------------------------------------------
  
Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.
  
**¿Cómo se usan estas tablas?**  
  
Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, se indica un hipervínculo a la actualización de software disponible y también se muestra la clasificación de gravedad de dicha actualización de software.
  
**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.
  
#### Componentes y sistema operativo Windows

 
<p> </p>
<table style="border:1px solid black;">
<tr class="thead">
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Windows Server 2003  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-035**](http://technet.microsoft.com/security/bulletin/ms11-035)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=0d289146-8470-45dd-a886-d1b35a2c6d4b)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=0d3e85a9-42ff-447b-ab8c-095a1c0b224c)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=4c388fe8-883a-4118-a7ff-50f1e9d0a071)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-035**](http://technet.microsoft.com/security/bulletin/ms11-035)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9019a3ff-d953-4b0b-8c7a-05aa9cf65c92) \*  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=841130fa-4522-4079-b7eb-f8466ac3ef12) \*  
(Crítica)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Windows Server 2008 R2
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-035**](http://technet.microsoft.com/security/bulletin/ms11-035)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=8732b41e-2f25-4ee1-a8b7-a8b8b9e22d08) \*  
(Crítica)
</td>
</tr>
</table>
 
**Nota para Windows Server 2008 y Windows Server 2008 R2**

**\*La instalación de Server Core está afectada.** Esta actualización se aplica, con la misma clasificación de gravedad, a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, independientemente de si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx) . Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx) .

#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tr class="thead">
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Conjuntos de programas y componentes de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-036**](http://technet.microsoft.com/security/bulletin/ms11-036)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft PowerPoint 2002 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=2e8a30ac-bcfe-4535-8ceb-723c25b43d5f)  
(KB2535802)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft PowerPoint 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=fc1cfcac-64cc-484a-97f2-3dcfe84cfdcd)  
(KB2535812)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft PowerPoint 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9a181739-709a-4c0d-a97f-f9891c45c04c)  
(KB2535818)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Office para Mac
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-036**](http://technet.microsoft.com/security/bulletin/ms11-036)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2004 para Mac
</td>
<td style="border:1px solid black;">
Microsoft Office 2004 para Mac <sup>[1]</sup>
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2008 para Mac
</td>
<td style="border:1px solid black;">
Microsoft Office 2008 para Mac <sup>[1]</sup>
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Convertidor de archivos con formatos XML abiertos para Mac
</td>
<td style="border:1px solid black;">
Convertidor de archivos con formatos XML abiertos para Mac <sup>[1]</sup>
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Otro software de Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-036**](http://technet.microsoft.com/security/bulletin/ms11-036)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
[Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5be09069-1cac-4b1e-ac94-4fb7024fb4ac)  
(KB2540162)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS11-036**

<sup>[1]</sup> Las actualizaciones de seguridad para Microsoft Office 2004 para Mac (KB2555786), Microsoft Office 2008 para Mac (KB2555785) y Convertidor de archivos con formatos XML abiertos para Mac (KB2555787) están disponibles desde el 14 de junio de 2011. Vea el boletín para obtener detalles.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/bb245732) . [TechNet Security Center](http://go.microsoft.com/fwlink/?linkid=21171) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://www.microsoft.com/spain/protect/default.mspx) , donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130) . También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129) . Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Para clientes de Microsoft Office para Mac, Microsoft AutoUpdate para Mac puede servir de ayuda para mantener actualizado el software de Microsoft. Para obtener más información acerca del uso de Microsoft AutoUpdate para Mac, vea [Buscar actualizaciones de software automáticamente](http://mac2.microsoft.com/help/office/14/en-us/word/item/ffe35357-8f25-4df8-a0a3-c258526c64ea) .

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155) . El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS07-036"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900) .

**Consejos para la detección y la implementación**

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747) .

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://go.microsoft.com/fwlink/?linkid=21134) .

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar de un modo rápido y confiable las actualizaciones críticas y de seguridad más recientes en sistemas operativos Microsoft Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://go.microsoft.com/fwlink/?linkid=50120) .

**System Center Configuration Manager 2007**

La administración de actualizaciones de software de Configuration Manager 2007 simplifica la tarea compleja de entregar y administrar actualizaciones para los sistemas de TI en toda la empresa. Con Configuration Manager 2007, los administradores de TI pueden ofrecer actualizaciones de los productos de Microsoft a una serie de dispositivos, incluidos equipos de escritorio, portátiles, servidores y dispositivos móviles.

La evaluación automática de vulnerabilidades en Configuration Manager 2007 detecta las necesidades de actualizaciones e informa de las acciones recomendadas. La administración de actualizaciones de software en Configuration Manager 2007 se basa en Microsoft Windows Software Update Services (WSUS), una infraestructura de actualizaciones probada con la que están familiarizados los administradores de TI de todo el mundo. Para obtener más información acerca de cómo los administradores pueden usar Configuration Manager 2007 para implementar actualizaciones, vea [Administración de actualizaciones de software](http://www.microsoft.com/systemcenter/en/us/configuration-manager/cm-software-update-management.aspx) . Para obtener más información acerca de Configuration Manager, visite [System Center Configuration Manager](http://www.microsoft.com/systemcenter/en/us/configuration-manager.aspx) .

**Systems Management Server 2003**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales.

**Nota** System Management Server 2003 está fuera del soporte técnico general desde el 12 de enero de 2010. Para obtener más información acerca de los ciclos de vida de los productos, visite [Ciclo de vida del soporte técnico de Microsoft](http://support.microsoft.com/common/international.aspx?rdpath=dm;en-us;lifecycle) . Ya está disponible la siguiente versión de SMS, System Center Configuration Manager 2007; vea la sección anterior, **System Center Configuration Manager 2007** .

Para obtener más información acerca de cómo los administradores pueden usar SMS 2003 para implementar actualizaciones de seguridad, vea [Escenarios y procedimientos para Microsoft Systems Management Server 2003: Administración de distribución de software y revisiones](http://www.microsoft.com/downloads/en/details.aspx?familyid=32f2bb4c-42f8-4b8d-844f-2553fd78049f&displaylang=en) . Para obtener información acerca de SMS, visite [Microsoft Systems Management Server TechCenter](http://technet.microsoft.com/en-us/systemcenter/bb545936.aspx) .

**Nota** SMS usa las herramientas Microsoft Baseline Security Analyzer para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341) . Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://www.microsoft.com/downloads/en/details.aspx?familyid=7bd3a16e-1899-4e0b-bb99-1320e816167d&displaylang=en) ) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet2.microsoft.com/windowsvista/en/library/4279e239-37a4-44aa-aec5-4e70fe39f9de1033.mspx?mfr=true) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en) .

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Microsoft Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Microsoft Knowledge Base, artículo 894199](http://support.microsoft.com/kb/894199) : Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones de meses anteriores para Windows Server Update Services](http://technet.microsoft.com/en-us/wsus/bb456965.aspx) . Muestra todas las actualizaciones nuevas, revisadas y publicadas de nuevo para los productos de Microsoft que no sean Microsoft Windows.

#### Microsoft Active Protections Program (MAPP)

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumeradas en [Asociados de Microsoft Active Protections Program (MAPP)](http://go.microsoft.com/fwlink/?linkid=215201) .

#### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de actualizaciones](http://go.microsoft.com/fwlink/?linkid=21168) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) .
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](http://support.microsoft.com/kb/913086) .

**Comunidad de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [IT Pro Security Community](http://go.microsoft.com/fwlink/?linkid=21164) (en inglés).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

-   Luigi Auriemma, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/) , por informar de un problema descrito en MS11-035
-   Will Dormann, de [CERT/CC](http://www.cert.org/) , por colaborar con nosotros en dos problemas descritos en MS11-036

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742) .
-   Los clientes de Estados Unidos y Canadá pueden recibir soporte técnico del [soporte de seguridad](http://go.microsoft.com/fwlink/?linkid=21131) o en el teléfono 1-866-PCSAFETY. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de las opciones de asistencia disponibles, visite [Ayuda y soporte técnico de Microsoft](http://support.microsoft.com/) .
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (10 de mayo de 2011): Publicación del resumen del boletín.
-   V1.1 (17 de mayo de 2011): para MS11-036, se ha quitado una nota errónea de la tabla Software afectado perteneciente a las actualizaciones KB2535818 y KB2540162 para Microsoft PowerPoint 2007 Service Pack 2.
-   V1.2 (14 de junio de 2011): Para MS11-036, se ha revisado este resumen del boletín para anunciar que están disponibles las actualizaciones de seguridad para Microsoft Office 2004 para Mac (KB2555786), Microsoft Office 2008 para Mac (KB2555785) y Convertidor de archivos con formatos XML abiertos para Mac (KB2555787). Vea MS11-036 para obtener detalles.

*Built at 2014-04-18T01:50:00Z-07:00*