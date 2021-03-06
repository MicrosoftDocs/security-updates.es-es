---
TOCTitle: 'MS14-JAN'
Title: Resumen del boletín de seguridad de Microsoft de enero de 2014
ms:assetid: 'ms14-jan'
ms:contentKeyID: 61597921
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms14-jan(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de enero de 2014
==============================================================

Publicado: martes, 14 de enero de 2014

**Versión:** 1.0

Este resumen del boletín enumera los boletines de seguridad publicados para enero de 2014.

Con la publicación de los boletines de seguridad de enero de 2014, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 9 de enero de 2014. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar una difusión por web para atender las consultas de los clientes sobre estos boletines el 15 de enero de 2014, a las 11:00 a.m., hora del Pacífico (EE. UU. y Canadá). [Inscríbase ahora a la conferencia en línea del boletín de seguridad de enero](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032572876&culture=en-us).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

### Información del boletín

#### Resúmenes ejecutivos

En la tabla siguiente se resumen los boletines de seguridad de este mes por orden de gravedad.

Para obtener detalles acerca del software afectado, vea la siguiente sección, **Software afectado**.

 
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386452">MS14-001</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Word y Office Web Apps podrían permitir la ejecución remota de código (2916605)<br />
<br />
</strong>Esta actualización de seguridad resuelve tres vulnerabilidades de las que se ha informado de forma privada en<strong></strong>Microsoft Office. Las vulnerabilidades podrían permitir la ejecución remota de código si se abre un archivo especialmente diseñado en una versión afectada de Microsoft Word u otro software de Microsoft Office. Un atacante que aprovechara las vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office,<br />
Software de servidor de Microsoft</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=389579">MS14-002</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el kernel de Windows</strong> <strong>podría</strong> <strong>permitir la elevación de privilegios (2914368</strong>)<strong><br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad que se ha divulgado públicamente en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si un atacante inicia sesión en un sistema y ejecuta una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=389578">MS14-003</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en los controladores modo kernel de Windows podría permitir la elevación de privilegios (2913602)<br />
<br />
</strong>Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si un usuario inicia sesión en un sistema y ejecuta una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386402">MS14-004</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Dynamics AX podría permitir la denegación de servicio (2880826)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Dynamics AX. La vulnerabilidad podría permitir la denegación de servicio si un atacante autenticado envía datos especialmente diseñados a una instancia de Application Object Server (AOS) de Microsoft Dynamics AX afectada. Un atacante que aprovechara esta vulnerabilidad podría provocar que la instancia AOS de destino dejara de responder a las solicitudes de cliente.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a><br />
Denegación de servicio</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Dynamics AX</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y, a continuación, por identificador de CVE. Sólo se incluyen las vulnerabilidades que tiene una clasificación de gravedad de crítica o importante en los boletines.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de las vulnerabilidades de ejecución de código y de denegación de servicio en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Revise cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación de las actualizaciones de este mes. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/security/cc998259).
  
En las columnas siguientes, "Última versión de software" hace referencia al software en cuestión y "Versiones de software anteriores" hace referencia a todas las versiones anteriores y compatibles del software en cuestión, tal como se muestra en las tablas "Software afectado" y "Software no afectado" del boletín.

 
<p> </p>
<table style="border:1px solid black;">
<thead>
<tr class="header">
<th style="border:1px solid black;" >Identificador del boletín</th>
<th style="border:1px solid black;" >Título de vulnerabilidad</th>
<th style="border:1px solid black;" >Identificador CVE</th>
<th style="border:1px solid black;" >Evaluación de explotabilidad para la última versión de software</th>
<th style="border:1px solid black;" >Evaluación de explotabilidad para la versión de software anterior</th>
<th style="border:1px solid black;" >Evaluación de explotabilidad de denegación de servicio</th>
<th style="border:1px solid black;" >Notas clave</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386452">MS14-001</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0258">CVE-2014-0258</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386452">MS14-001</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0259">CVE-2014-0259</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386452">MS14-001</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0260">CVE-2014-0260</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=389579">MS14-002</a></td>
<td style="border:1px solid black;">Vulnerabilidad de NDProxy en el kernel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-5065">CVE-2013-5065</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.<br />
<br />
Microsoft tiene constancia de ataques dirigidos y limitados que intentan aprovechar esta vulnerabilidad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=389578">MS14-003</a></td>
<td style="border:1px solid black;">Vulnerabilidad de identificador de ventana en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0262">CVE-2014-0262</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386402">MS14-004</a></td>
<td style="border:1px solid black;">Vulnerabilidad de denegación de servicio en el filtro de consulta</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0261">CVE-2014-0261</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.</td>
</tr>
</tbody>
</table>
  
Software afectado  
-----------------
  
Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.
  
**¿Cómo se usan estas tablas?**  
  
Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, también se muestra la clasificación de gravedad de dicha actualización de software.
  
**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.
  
#### Componentes y sistema operativo Windows

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="3" style="border:1px solid black;">
Windows XP  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-002**](http://go.microsoft.com/fwlink/?linkid=389579)
</td>
<td style="border:1px solid black;">
[**MS14-003**](http://go.microsoft.com/fwlink/?linkid=389578)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
**Ninguna**[](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
Windows XP Service Pack 3  
(2914368)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2  
(2914368)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-002**](http://go.microsoft.com/fwlink/?linkid=389579)
</td>
<td style="border:1px solid black;">
[**MS14-003**](http://go.microsoft.com/fwlink/?linkid=389578)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
**Ninguna**[](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(2914368)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2914368)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2914368)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-002**](http://go.microsoft.com/fwlink/?linkid=389579)
</td>
<td style="border:1px solid black;">
[**MS14-003**](http://go.microsoft.com/fwlink/?linkid=389578)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**[](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
**Ninguna**[](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-002**](http://go.microsoft.com/fwlink/?linkid=389579)
</td>
<td style="border:1px solid black;">
[**MS14-003**](http://go.microsoft.com/fwlink/?linkid=389578)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**[](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
**Ninguna**[](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows 7
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador** **del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-002**](http://go.microsoft.com/fwlink/?linkid=389579)
</td>
<td style="border:1px solid black;">
[**MS14-003**](http://go.microsoft.com/fwlink/?linkid=389578)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**[](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2913602)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2913602)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows Server 2008 R2
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-002**](http://go.microsoft.com/fwlink/?linkid=389579)
</td>
<td style="border:1px solid black;">
[**MS14-003**](http://go.microsoft.com/fwlink/?linkid=389578)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**[](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2913602)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2913602)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows 8 y Windows 8.1
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-002**](http://go.microsoft.com/fwlink/?linkid=389579)
</td>
<td style="border:1px solid black;">
[**MS14-003**](http://go.microsoft.com/fwlink/?linkid=389578)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**[](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
**Ninguna**[](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 8 para sistemas x64
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows Server 2012 y Windows Server 2012 R2
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-002**](http://go.microsoft.com/fwlink/?linkid=389579)
</td>
<td style="border:1px solid black;">
[**MS14-003**](http://go.microsoft.com/fwlink/?linkid=389578)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**[](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
**Ninguna**[](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2012 R2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows RT y Windows RT 8.1
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-002**](http://go.microsoft.com/fwlink/?linkid=389579)
</td>
<td style="border:1px solid black;">
[**MS14-003**](http://go.microsoft.com/fwlink/?linkid=389578)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**[](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
**Ninguna**[](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows RT
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows RT 8.1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Opción de instalación Server Core
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-002**](http://go.microsoft.com/fwlink/?linkid=389579)
</td>
<td style="border:1px solid black;">
[**MS14-003**](http://go.microsoft.com/fwlink/?linkid=389578)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**[](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2913602)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 

#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Office 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-001**](http://go.microsoft.com/fwlink/?linkid=386452)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft Word 2003 Service Pack 3  
(2863866)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Office 2007
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-001**](http://go.microsoft.com/fwlink/?linkid=386452)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft Word 2007 Service Pack 3  
(2837617)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Office 2010
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-001**](http://go.microsoft.com/fwlink/?linkid=386452)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Word 2010 Service Pack 1 (ediciones de 32 bits)  
(2863902)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Word 2010 Service Pack 1 (ediciones de 32 bits)  
(2863901)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Word 2010 Service Pack 2 (ediciones de 32 bits)  
(2863902)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Word 2010 Service Pack 2 (ediciones de 32 bits)  
(2863901)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Word 2010 Service Pack 1 (ediciones de 64 bits)  
(2863902)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Word 2010 Service Pack 1 (ediciones de 64 bits)  
(2863901)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Word 2010 Service Pack 2 (ediciones de 64 bits)  
(2863902)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Word 2010 Service Pack 2 (ediciones de 64 bits)  
(2863901)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Office 2013 y Microsoft Office 2013 RT
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-001**](http://go.microsoft.com/fwlink/?linkid=386452)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2013 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Word 2013 (ediciones de 32 bits)  
(2827224)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2013 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Word 2013 (ediciones de 32 bits)  
(Word PIA)  
(2863834)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2013 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Word 2013 (ediciones de 64 bits)  
(2827224)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2013 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Word 2013 (ediciones de 64 bits)  
(Word PIA)  
(2863834)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2013 RT
</td>
<td style="border:1px solid black;">
Microsoft Word 2013 RT  
(2827224)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Otro software de Office
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-001**](http://go.microsoft.com/fwlink/?linkid=386452)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office Service Pack 3
</td>
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office Service Pack 3  
(2837615)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Word Viewer
</td>
<td style="border:1px solid black;">
Microsoft Word Viewer  
(2863867)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS14-001**

Este boletín abarca varias categorías de software. Vea las demás tablas de esta sección para determinar el software afectado.

#### Microsoft Office Services y Web Apps

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft SharePoint Server 2010
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-001**](http://go.microsoft.com/fwlink/?linkid=386452)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
Word Automation Services  
(2837577)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2010 Service Pack 2
</td>
<td style="border:1px solid black;">
Word Automation Services  
(2837577)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft SharePoint Server 2013
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-001**](http://go.microsoft.com/fwlink/?linkid=386452)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2013
</td>
<td style="border:1px solid black;">
Word Automation Services  
(2837625)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Office Web Apps 2010
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-001**](http://go.microsoft.com/fwlink/?linkid=386452)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office Web Apps 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft Web Applications 2010 Service Pack 1  
(2837596)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Web Apps 2010 Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft Web Applications 2010 Service Pack 2  
(2837596)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Office Web Apps 2013
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-001**](http://go.microsoft.com/fwlink/?linkid=386452)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office Web Apps 2013
</td>
<td style="border:1px solid black;">
Microsoft Office Web Apps Server 2013  
(2863879)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS14-001**

Este boletín abarca varias categorías de software. Vea las demás tablas de esta sección para determinar el software afectado.

#### Soluciones Microsoft Enterprise Resource Planning (ERP)

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Dynamics AX 4.0
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-004**](http://go.microsoft.com/fwlink/?linkid=386402)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Dynamics AX 4.0 Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft Dynamics AX 4.0 Service Pack 2  
(2920510)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Dynamics AX 2009
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-004**](http://go.microsoft.com/fwlink/?linkid=386402)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de** **gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Dynamics AX 2009 Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft Dynamics AX 2009 Service Pack 1  
(2914058)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Dynamics AX 2012 y Microsoft Dynamics AX 2012 R2
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-004**](http://go.microsoft.com/fwlink/?linkid=386402)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Dynamics AX 2012
</td>
<td style="border:1px solid black;">
Microsoft Dynamics AX 2012  
(2914055)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Dynamics AX 2012 R2
</td>
<td style="border:1px solid black;">
Microsoft Dynamics AX 2012 R2  
(2914057)  
(Importante)
</td>
</tr>
</table>
 

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

Hay disponibles varios recursos para ayudar a los administradores a implementar las actualizaciones de seguridad.

-   Microsoft Baseline Security Analyzer (MBSA) permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan y las configuraciones de seguridad incorrectas más comunes.
-   Windows Server Update Services (WSUS), Systems Management Server (SMS) y System Center Configuration Manager ayudan a los administradores a distribuir las actualizaciones de seguridad.
-   Los componentes del Evaluador de compatibilidad de aplicaciones incluidos con el kit de herramientas de compatibilidad de aplicaciones contribuyen a optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas.

Para obtener información acerca de estas y otras herramientas que hay disponibles, vea [Herramientas de seguridad para profesionales de TI](http://technet.microsoft.com/security/cc297183).

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Para la publicación de boletines el segundo martes de cada mes, Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga. No hay disponible ninguna versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows para las publicaciones de boletín de seguridad fuera de ciclo.

#### Actualizaciones no relacionadas con la seguridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Artículo 894199 de Microsoft Knowledge Base](https://support.microsoft.com/kb/894199): Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones de meses anteriores para Windows Server Update Services](http://technet.microsoft.com/wsus/bb456965). Muestra todas las actualizaciones nuevas, revisadas y publicadas de nuevo para los productos de Microsoft que no sean Microsoft Windows.

#### Microsoft Active Protections Program (MAPP)

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumerados en [Asociados de Microsoft Active Protections Program (MAPP)](http://go.microsoft.com/fwlink/?linkid=215201).

#### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de actualizaciones](http://go.microsoft.com/fwlink/?linkid=21168) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](https://support.microsoft.com/kb/913086).

**Comunidad de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [Comunidad de profesionales de TI de seguridad](http://go.microsoft.com/fwlink/?linkid=21164).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

**MS14-001**

-   Mateusz Jurczyk, Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Word (CVE-2014-0258)
-   Mateusz Jurczyk, Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Word (CVE-2014-0259)
-   Mateusz Jurczyk, Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Word (CVE-2014-0260)

**MS14-002**

-   [FireEye, Inc.](http://www2.fireeye.com/), por ayudarnos con la vulnerabilidad de NDProxy en el kernel (CVE-2013-5065)

**MS14-003**

-   Yujie Wen y Renguang Yuan, de [Qihoo](http://www.360.cn/), por informar de la vulnerabilidad de identificador de ventana en Win32k (CVE-2014-0262)

**MS14-004**

-   Andrey Maykov, desarrollador jefe en [FTO Project](http://www.fto.com.ru/), por informar de la vulnerabilidad de denegación de servicio en el filtro de consulta (CVE-2014-0261)

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Soluciones de seguridad para profesionales de TI: [Soporte técnico y solución de problemas de seguridad de TechNet](http://technet.microsoft.com/security/bb980617)
-   Ayuda para proteger su equipo con Windows de virus y malware: [Solución antivirus y centro de seguridad](http://support.microsoft.com/contactus/cu_sc_virsec_master)
-   Soporte local según su país: [Soporte internacional](http://support.microsoft.com/common/international.aspx)

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (14 de enero de 2014): Publicación del resumen del boletín.

*Built at 2014-04-18T01:50:00Z-07:00*
