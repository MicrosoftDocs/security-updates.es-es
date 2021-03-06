---
TOCTitle: 'MS13-MAR'
Title: Resumen del boletín de seguridad de Microsoft de marzo 2013
ms:assetid: 'ms13-mar'
ms:contentKeyID: 61225451
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms13-mar(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de marzo 2013
===========================================================

Publicado: martes, 12 de marzo de 2013 | Actualizado: viernes, 15 de marzo de 2013

**Versión:** 1.1

Este resumen del boletín enumera los boletines de seguridad publicados para marzo de 2013.

Con la publicación de los boletines de seguridad de marzo de 2013, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 7 de marzo de 2013. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/es-es/security/gg309152.aspx).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 13 de marzo de 2013, a las 11:00 a.m., hora del Pacífico (EE. UU. y Canadá). [Inscríbase ahora a la conferencia en línea del boletín de seguridad de marzo](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032538636&culture=en-us). Después de esta fecha, este webcast estará disponible [a petición](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032538636&culture=en-us).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

### Información del boletín

#### Resúmenes ejecutivos

En la tabla siguiente se resumen los boletines de seguridad de este mes por orden de gravedad.

Para obtener detalles acerca del software afectado, vea la siguiente sección, **Ubicaciones de descarga y software afectado**.

 
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=279923">MS13-021</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (2809289)  <br />
<br />
</strong>Esta actualización de seguridad resuelve ocho vulnerabilidades de las que se ha informado de forma privada y una vulnerabilidad de la que se ha informado de forma pública en Internet Explorer. La más grave de las vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un intruso que aprovechara estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275737">MS13-022</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Silverlight podría permitir la ejecución remota de código (2814124)</strong> <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Silverlight. La vulnerabilidad podría permitir la ejecución remota de código si un atacante hospeda un sitio web que contenga una aplicación de Silverlight especialmente diseñada que pudiera aprovechar esta vulnerabilidad y convence a un usuario de que visite el sitio web. El atacante también podría aprovechar sitios web vulnerables y sitios web que aceptan o reciben contenido o anuncios proporcionados por el usuario. Los sitios web de este tipo podrían incluir contenido malintencionado a través del cual se podría aprovechar esta vulnerabilidad. No obstante, el atacante no podría en ningún caso obligar a los usuarios a visitar un sitio web. Por lo tanto, tendría que atraerlos a un sitio web; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico o de un mensaje de Instant Messenger que los lleve al sitio web del atacante. También sería posible que se mostrara contenido web diseñado especialmente mediante titulares de anuncios u otros métodos para hacer llegar contenido web a los sistemas afectados.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">No requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Silverlight</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=276801">MS13-023</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Visio</strong> <strong>Viewer</strong> <strong>2010 podría permitir la ejecución remota de código (2801261)  <br />
<br />
</strong>Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Office. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo de Visio especialmente diseñado. Un atacante que aprovechara la vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=271610">MS13-024</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en SharePoint</strong> <strong>podrían</strong> <strong>permitir la elevación de privilegios (2780176)  <br />
<br />
</strong>Esta actualización de seguridad resuelve cuatro vulnerabilidades de las que se ha informado de forma privada en Microsoft SharePoint y Microsoft SharePoint Foundation. Las vulnerabilidades más graves podrían permitir la elevación de privilegios si un usuario hace clic en una dirección URL especialmente diseñada que lo dirige a un sitio de SharePoint atacado.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office, software de servidor de Microsoft</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=282355">MS13-025</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft OneNote podría permitir la divulgación de información (2816264)  <br />
<br />
</strong>Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft OneNote. La vulnerabilidad podría permitir la divulgación de información si un atacante convence a un usuario de que abra un archivo de OneNote especialmente diseñado.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Divulgación de información</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=280673">MS13-026</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Office para Mac podría permitir la divulgación de información (2813682)  <br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Office para Mac. La vulnerabilidad podría permitir la divulgación de información si un usuario abre un mensaje de correo electrónico especialmente diseñado.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Divulgación de información</td>
<td style="border:1px solid black;">No requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=282639">MS13-027</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en los controladores modo</strong> <strong>kernelpodrían</strong> <strong>permitir la elevación de privilegios (2807986)  <br />
<br />
</strong>Esta actualización de seguridad resuelve tres vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. Estas vulnerabilidades podrían permitir la elevación de privilegios si un atacante obtiene acceso a un sistema.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y, a continuación, por identificador de CVE. Sólo se incluyen las vulnerabilidades que tiene una clasificación de gravedad de crítica o importante en los boletines.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de las vulnerabilidades de ejecución de código y de denegación de servicio en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Revise cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación de las actualizaciones de este mes. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/security/cc998259).
  
En las columnas siguientes, "Última versión de software" hace referencia al software en cuestión y "Versiones de software anteriores" hace referencia a todas las versiones anteriores y compatibles del software en cuestión, tal como se muestra en las tablas "Software afectado" y "Software no afectado" del boletín.
  
| Identificador del boletín                                 | Título de vulnerabilidad                                                                         | Identificador CVE                                                                | Evaluación de explotabilidad para la última versión de software                                                               | Evaluación de explotabilidad para la versión de software anterior                                                             | Evaluación de explotabilidad de denegación de servicio | Notas clave                                                 |  
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|-------------------------------------------------------------|  
| [MS13-021](http://go.microsoft.com/fwlink/?linkid=279923) | Vulnerabilidad en el uso de OnResize después de la liberación en Internet Explorer               | [CVE-2013-0087](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0087) | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                   |  
| [MS13-021](http://go.microsoft.com/fwlink/?linkid=279923) | Vulnerabilidad en el uso de saveHistory después de la liberación en Internet Explorer            | [CVE-2013-0088](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0088) | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                   |  
| [MS13-021](http://go.microsoft.com/fwlink/?linkid=279923) | Vulnerabilidad en el uso de CMarkupBehaviorContext después de la liberación en Internet Explorer | [CVE-2013-0089](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0089) | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                   |  
| [MS13-021](http://go.microsoft.com/fwlink/?linkid=279923) | Vulnerabilidad en el uso de CCaret después de la liberación en Internet Explorer                 | [CVE-2013-0090](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0090) | [2](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Dificultad para crear código que aproveche la vulnerabilidad | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                   |  
| [MS13-021](http://go.microsoft.com/fwlink/?linkid=279923) | Vulnerabilidad en el uso de CElement después de la liberación en Internet Explorer               | [CVE-2013-0091](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0091) | No está afectada                                                                                                              | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                   |  
| [MS13-021](http://go.microsoft.com/fwlink/?linkid=279923) | Vulnerabilidad en el uso de GetMarkupPtr después de la liberación en Internet Explorer           | [CVE-2013-0092](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0092) | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                   |  
| [MS13-021](http://go.microsoft.com/fwlink/?linkid=279923) | Vulnerabilidad en el uso de OnBeforeCopy después de la liberación en Internet Explorer           | [CVE-2013-0093](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0093) | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                   |  
| [MS13-021](http://go.microsoft.com/fwlink/?linkid=279923) | Vulnerabilidad en el uso de removeChild después de la liberación en Internet Explorer            | [CVE-2013-0094](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0094) | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                   |  
| [MS13-021](http://go.microsoft.com/fwlink/?linkid=279923) | Vulnerabilidad en el uso de CTreeNode después de la liberación en Internet Explorer              | [CVE-2013-1288](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1288) | No está afectada                                                                                                              | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | Esta vulnerabilidad ya se ha divulgado públicamente.        |  
| [MS13-022](http://go.microsoft.com/fwlink/?linkid=275737) | Vulnerabilidad de anulación de referencia doble en Silverlight                                   | [CVE-2013-0074](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0074) | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                                                                                                  | No aplicable                                           | (Ninguna)                                                   |  
| [MS13-023](http://go.microsoft.com/fwlink/?linkid=276801) | Vulnerabilidad de confusión de tipo de objeto de árbol en Visio Viewer                           | [CVE-2013-0079](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0079) | No está afectada                                                                                                              | [2](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Dificultad para crear código que aproveche la vulnerabilidad | No aplicable                                           | (Ninguna)                                                   |  
| [MS13-024](http://go.microsoft.com/fwlink/?linkid=271610) | Vulnerabilidad de la función de devolución de llamada                                            | [CVE-2013-0080](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0080) | No está afectada                                                                                                              | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                   |  
| [MS13-024](http://go.microsoft.com/fwlink/?linkid=271610) | Vulnerabilidad de XSS en SharePoint                                                              | [CVE-2013-0083](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0083) | No está afectada                                                                                                              | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                   |  
| [MS13-024](http://go.microsoft.com/fwlink/?linkid=271610) | Vulnerabilidad de recorrido de directorios en SharePoint                                         | [CVE-2013-0084](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0084) | No está afectada                                                                                                              | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | No aplicable                                           | (Ninguna)                                                   |  
| [MS13-024](http://go.microsoft.com/fwlink/?linkid=271610) | Vulnerabilidad de desbordamiento del búfer                                                       | [CVE-2013-0085](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0085) | No está afectada                                                                                                              | [3](http://technet.microsoft.com/security/cc998259) - Improbabilidad de código que aproveche la vulnerabilidad                | Temporal                                               | Se trata de una vulnerabilidad de denegación de servicio.   |  
| [MS13-025](http://go.microsoft.com/fwlink/?linkid=282355) | Vulnerabilidad de validación del tamaño del búfer                                                | [CVE-2013-0086](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0086) | No está afectada                                                                                                              | [3](http://technet.microsoft.com/security/cc998259) - Improbabilidad de código que aproveche la vulnerabilidad                | No aplicable                                           | Esta vulnerabilidad afecta a la divulgación de información. |  
| [MS13-026](http://go.microsoft.com/fwlink/?linkid=280673) | Vulnerabilidad de carga de contenido no intencionada                                             | [CVE-2013-0095](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0095) | [3](http://technet.microsoft.com/security/cc998259) - Improbabilidad de código que aproveche la vulnerabilidad                | [3](http://technet.microsoft.com/security/cc998259) - Improbabilidad de código que aproveche la vulnerabilidad                | No aplicable                                           | Esta vulnerabilidad afecta a la divulgación de información. |  
| [MS13-027](http://go.microsoft.com/fwlink/?linkid=282639) | Vulnerabilidad del descriptor de USB en Windows                                                  | [CVE-2013-1285](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1285) | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | Permanente                                             | (Ninguna)                                                   |  
| [MS13-027](http://go.microsoft.com/fwlink/?linkid=282639) | Vulnerabilidad del descriptor de USB en Windows                                                  | [CVE-2013-1286](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1286) | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | Permanente                                             | (Ninguna)                                                   |  
| [MS13-027](http://go.microsoft.com/fwlink/?linkid=282639) | Vulnerabilidad del descriptor de USB en Windows                                                  | [CVE-2013-1287](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1287) | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | [1](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Probabilidad de código que aproveche la vulnerabilidad       | Permanente                                             | (Ninguna)                                                   |
  
Ubicaciones de descarga y software afectado  
-------------------------------------------
  
Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.
  
**¿Cómo se usan estas tablas?**  
  
Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, se indica un hipervínculo a la actualización de software disponible y también se muestra la clasificación de gravedad de dicha actualización de software.
  
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
[**MS13-021**](http://go.microsoft.com/fwlink/?linkid=279923)
</td>
<td style="border:1px solid black;">
[**MS13-027**](http://go.microsoft.com/fwlink/?linkid=282639)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=ace6994d-7482-40de-84ad-a87853a35860)   
(2809289)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=50c59794-4ec7-404a-b316-dae314521ebb)  
(2809289)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=7e5d96a7-d9f5-4832-b4f9-b6e0148c655b)  
(2809289)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=ba528d03-b0a6-40a5-a6bd-13c062a8a877)   
(2807986)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=795cef4e-9c01-447f-916c-e52e69eca4a3)   
(2809289)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=16993a2c-1fe1-4c1e-bcd9-db1a7dd4a058)  
(2809289)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=66a08524-883d-4d67-82cc-2c0f55c56b31)  
(2809289)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4f8a48d4-b1bb-465c-a232-d29fe94d1429)   
(2807986)  
(Importante)
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
[**MS13-021**](http://go.microsoft.com/fwlink/?linkid=279923)
</td>
<td style="border:1px solid black;">
[**MS13-027**](http://go.microsoft.com/fwlink/?linkid=282639)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=e3c911b3-7fdd-4105-a20a-eef65b0908e3)   
(2809289)  
(Moderada)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=0f58d63e-0d2c-41d2-9792-edbb2f4a539d)  
(2809289)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=e6b63da9-a414-40ee-b877-4fb0d62bacba)  
(2809289)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=835651b7-79fb-4d50-b48e-f02173062253)   
(2807986)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=eaf2c568-089a-4c2f-bca6-da83f7332de9)   
(2809289)  
(Moderada)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=5a18b139-2773-44c8-85f9-8dce24249e71)  
(2809289)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=d6feba92-f014-4521-b6c4-7f5f358a3ce3)  
(2809289)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9d5f1ed1-f33b-4c90-9b29-ee8ac587d31b)   
(2807986)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=088fd3ec-62e1-4737-8132-6b51219ed37f)   
(2809289)  
(Moderada)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=799748d8-056d-4139-86e1-9bd0cb0151b4)  
(2809289)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=28d441e7-abcf-4cc9-84e0-572e5b79aab7)   
(2807986)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador** **del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-021**](http://go.microsoft.com/fwlink/?linkid=279923)
</td>
<td style="border:1px solid black;">
[**MS13-027**](http://go.microsoft.com/fwlink/?linkid=282639)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=0bf77905-1199-4219-a67d-1e9ad3f63757)  
(2809289)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=76e328f8-4f86-4e50-b7e0-22db0385ab01)  
(2809289)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=c26f74fc-e224-4533-a4e3-b52125dca5cd)   
(2809289)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b8472bc7-9e20-4238-adcf-a1e1a91687a1)   
(2807986)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=7b652bb4-7a0a-437b-bcc5-ebbbb820c559)  
(2809289)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=67b09398-ceb6-403c-bba4-261d9d9dea98)  
(2809289)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=3f1795a5-4376-4929-8748-743840ec2154)   
(2809289)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e412c54a-a93d-4c5b-9b13-40b59d1dff35)   
(2807986)  
(Importante)
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
[**MS13-021**](http://go.microsoft.com/fwlink/?linkid=279923)
</td>
<td style="border:1px solid black;">
[**MS13-027**](http://go.microsoft.com/fwlink/?linkid=282639)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=0303fcb1-34d5-47da-b6ee-18222fe3235a)  
(2809289)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=337068a5-9281-4db6-9ff1-5282cdfa0763)  
(2809289)  
(Moderada)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=c672c196-5072-468c-8d88-34534fa219fd)   
(2809289)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f1ca4fe0-3ee3-4162-a9fa-48c54fc8b08e)   
(2807986)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=f22b9327-1430-44cb-a609-ea1bb9b7b8f8)  
(2809289)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=0496cbfe-77d2-4de6-b78d-937225dc8974)  
(2809289)  
(Moderada)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=5c40f237-b4c8-41eb-a649-baad46dfa13c)   
(2809289)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8b61f3e5-0cf9-4eab-8a59-829957135dd6)   
(2807986)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=09e4832c-b95e-4581-a73b-49cb6a60c1df)  
(2809289)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=af2e8e83-fb8f-4ba5-83ec-8bd4347a5fe6)   
(2807986)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows 7
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-021**](http://go.microsoft.com/fwlink/?linkid=279923)
</td>
<td style="border:1px solid black;">
[**MS13-027**](http://go.microsoft.com/fwlink/?linkid=282639)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=b07b63d5-925d-4c4f-ae19-18a9b141eaa0)  
(2809289)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=54c619b7-e156-4f07-a90e-56ed9a618085)   
(2809289)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=c72f78be-e6a8-43b4-9303-7c93dd11d502)   
(2807986)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=b07b63d5-925d-4c4f-ae19-18a9b141eaa0)  
(2809289)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=54c619b7-e156-4f07-a90e-56ed9a618085)   
(2809289)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=c72f78be-e6a8-43b4-9303-7c93dd11d502)   
(2807986)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas x64
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=610da6c6-e8a9-4726-ae54-11f01fb5ab2d)  
(2809289)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=86f2a369-d71d-4a36-95ed-d5be89cbbbae)   
(2809289)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=6a8a22d6-0e6e-4d3b-afd0-d4841274ade0)   
(2807986)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=610da6c6-e8a9-4726-ae54-11f01fb5ab2d)  
(2809289)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=86f2a369-d71d-4a36-95ed-d5be89cbbbae)   
(2809289)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=6a8a22d6-0e6e-4d3b-afd0-d4841274ade0)   
(2807986)  
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
[**MS13-021**](http://go.microsoft.com/fwlink/?linkid=279923)
</td>
<td style="border:1px solid black;">
[**MS13-027**](http://go.microsoft.com/fwlink/?linkid=282639)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=cf5f65e1-93ae-4ec3-84d2-eb017efdc9d6)  
(2809289)  
(Moderada)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=c5018865-7162-4d8d-86fc-aacd6d5f0a37)   
(2809289)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=84ba3686-14ed-4aac-8db1-4438aa9e0a2e)   
(2807986)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=cf5f65e1-93ae-4ec3-84d2-eb017efdc9d6)  
(2809289)  
(Moderada)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=c5018865-7162-4d8d-86fc-aacd6d5f0a37)   
(2809289)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=84ba3686-14ed-4aac-8db1-4438aa9e0a2e)   
(2807986)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=3436d1d1-bf20-40cc-8c51-f093da67c8a9)  
(2809289)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=01498cd0-e27e-4256-8f21-7a6eeedfb77c)   
(2807986)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=3436d1d1-bf20-40cc-8c51-f093da67c8a9)  
(2809289)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=01498cd0-e27e-4256-8f21-7a6eeedfb77c)   
(2807986)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows 8
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-021**](http://go.microsoft.com/fwlink/?linkid=279923)
</td>
<td style="border:1px solid black;">
[**MS13-027**](http://go.microsoft.com/fwlink/?linkid=282639)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=7c348fe3-f4f0-4f22-8a7f-8563705c1f64)   
(2809289)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=de4ec125-c337-4615-b39b-8456658dae22)   
(2807986)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 8 para sistemas de 64 bits
</td>
<td style="border:1px solid black;">
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=0c503b83-5b13-41da-a5ff-7519bc244521)   
(2809289)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 64 bits](http://www.microsoft.com/downloads/details.aspx?familyid=c1539e94-0635-4f51-8172-a96a737d81d3)   
(2807986)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows Server 2012
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-021**](http://go.microsoft.com/fwlink/?linkid=279923)
</td>
<td style="border:1px solid black;">
[**MS13-027**](http://go.microsoft.com/fwlink/?linkid=282639)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012
</td>
<td style="border:1px solid black;">
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=f9b299f1-8a73-40b2-9942-e6419496bb39)   
(2809289)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=959c78e1-29d9-40a3-9eb3-1206c09e3752)   
(2807986)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows RT
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-021**](http://go.microsoft.com/fwlink/?linkid=279923)
</td>
<td style="border:1px solid black;">
[**MS13-027**](http://go.microsoft.com/fwlink/?linkid=282639)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows RT
</td>
<td style="border:1px solid black;">
Internet Explorer 10<sup>[1]</sup>   
(2809289)  
(Crítica)
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
**Identificador** **del** **boletín**
</td>
<td style="border:1px solid black;">
[**MS13-021**](http://go.microsoft.com/fwlink/?linkid=279923)
</td>
<td style="border:1px solid black;">
[**MS13-027**](http://go.microsoft.com/fwlink/?linkid=282639)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
Ninguna
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
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f1ca4fe0-3ee3-4162-a9fa-48c54fc8b08e) (instalación Server Core)   
(2807986)  
(Importante)
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
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8b61f3e5-0cf9-4eab-8a59-829957135dd6) (instalación Server Core)   
(2807986)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=84ba3686-14ed-4aac-8db1-4438aa9e0a2e)(instalación Server Core)   
(2807986)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=84ba3686-14ed-4aac-8db1-4438aa9e0a2e) (instalación Server Core)   
(2807986)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=959c78e1-29d9-40a3-9eb3-1206c09e3752) (instalación Server Core)   
(2807986)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS13-021**

<sup>[1]</sup>Las actualizaciones de seguridad de Windows RT se proporcionan a través de [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130).

#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="4" style="border:1px solid black;">
Software de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-023**](http://go.microsoft.com/fwlink/?linkid=276801)
</td>
<td style="border:1px solid black;">
[**MS13-025**](http://go.microsoft.com/fwlink/?linkid=282355)
</td>
<td style="border:1px solid black;">
[**MS13-026**](http://go.microsoft.com/fwlink/?linkid=280673)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Visio Viewer 2010 Service Pack 1 (edición de 32 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Visio Viewer 2010 Service Pack 1 (edición de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=b01b4410-1107-472f-bf96-234304e91e77)   
(2687505)  
(Crítica)
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
Microsoft Visio Viewer 2010 Service Pack 1 (edición de 64 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Visio Viewer 2010 Service Pack 1 (edición de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=24065dd5-251b-4a3c-bb44-8d552a1f265e)   
(2687505)  
(Crítica)
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
Microsoft Visio 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Visio 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=7a1a21e7-3137-4201-a005-cc66379fc1c5)   
(2760762)  
(Sin clasificación de gravedad)<sup>[1]</sup>
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
Microsoft Visio 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Visio 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=7b7d39f0-a341-4d48-8177-329cccb5a7f1)   
(2760762)  
(Sin clasificación de gravedad)<sup>[1]</sup>
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
Microsoft Office 2010 Filter Pack Service Pack 1 (versión de 32 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2010 Filter Pack Service Pack 1 (versión de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=f10db48f-a980-47bf-83a5-c0da4e615114)   
(2553501)  
(Sin clasificación de gravedad)<sup>[1]</sup>
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
Microsoft Office 2010 Filter Pack Service Pack 1 (versión de 64 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2010 Filter Pack Service Pack 1 (versión de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=70d3372b-74a8-4b68-b6c4-18863835915d)   
(2553501)  
(Sin clasificación de gravedad)<sup>[1]</sup>
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
Microsoft OneNote 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft OneNote 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=da4bfd31-65b9-496b-aa98-4fa8b729dcf3)   
(2760600)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft OneNote 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft OneNote 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=10fc7350-e1d4-40b6-a5d1-8670263faf05)   
(2760600)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2008 para Mac
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office 2008 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=d7aef20a-922b-4495-b473-1afa4a7ac514)   
(2817449)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office para Mac 2011
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office para Mac 2011](http://www.microsoft.com/downloads/details.aspx?familyid=4960674b-1cb4-499a-999e-7aa4d4c49e5e)   
(2817452)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS13-023**

<sup>[1]</sup>Las clasificaciones de gravedad no se aplican a esta actualización para el software especificado porque las vías de ataque conocidas para la vulnerabilidad están bloqueadas.

#### Herramientas y software para desarrolladores de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Silverlight
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-022**](http://go.microsoft.com/fwlink/?linkid=275737)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Silverlight 5 cuando está instalado en Mac
</td>
<td style="border:1px solid black;">
[Microsoft Silverlight 5](http://www.microsoft.com/downloads/details.aspx?familyid=75eef049-1f39-47b4-9a1e-839974fc89b9) cuando está instalado en Mac   
(2814124)   
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Silverlight 5 Developer Runtime cuando está instalado en Mac
</td>
<td style="border:1px solid black;">
[Microsoft Silverlight 5 Developer Runtime](http://www.microsoft.com/downloads/details.aspx?familyid=75eef049-1f39-47b4-9a1e-839974fc89b9) cuando está instalado en Mac   
(2814124)   
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Silverlight 5 cuando está instalado en todas las versiones compatibles de los clientes Microsoft Windows
</td>
<td style="border:1px solid black;">
[Microsoft Silverlight 5](http://www.microsoft.com/downloads/details.aspx?familyid=75eef049-1f39-47b4-9a1e-839974fc89b9) cuando está instalado en todas las versiones compatibles de los clientes Microsoft Windows   
(2814124)   
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Silverlight 5 Developer Runtime cuando está instalado en todas las versiones compatibles de los clientes Microsoft Windows
</td>
<td style="border:1px solid black;">
[Microsoft Silverlight 5 Developer Runtime](http://www.microsoft.com/downloads/details.aspx?familyid=75eef049-1f39-47b4-9a1e-839974fc89b9) cuando está instalado en todas las versiones compatibles de los clientes Microsoft Windows   
(2814124)   
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Silverlight 5 cuando está instalado en todas las versiones compatibles de los servidores Microsoft Windows
</td>
<td style="border:1px solid black;">
[Microsoft Silverlight 5](http://www.microsoft.com/downloads/details.aspx?familyid=75eef049-1f39-47b4-9a1e-839974fc89b9) cuando está instalado en todas las versiones compatibles de los servidores Microsoft Windows  
(2814124)   
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Silverlight 5 Developer Runtime cuando está instalado en todas las versiones compatibles de los servidores Microsoft Windows
</td>
<td style="border:1px solid black;">
[Microsoft Silverlight 5 Developer Runtime](http://www.microsoft.com/downloads/details.aspx?familyid=75eef049-1f39-47b4-9a1e-839974fc89b9) cuando está instalado en todas las versiones compatibles de los servidores Microsoft Windows  
(2814124)   
(Crítica)
</td>
</tr>
</table>
 

#### Software de servidor de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft SharePoint Server
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-024**](http://go.microsoft.com/fwlink/?linkid=271610)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft SharePoint Server 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=a9e8acbd-90e5-4acd-aa8f-b743a352787b)<sup>[1]</sup>   
(wasrv)  
(2553407)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft SharePoint Foundation
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-024**](http://go.microsoft.com/fwlink/?linkid=271610)
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
Microsoft SharePoint Foundation 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft SharePoint Foundation 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=293666ec-3290-4c6f-a7f6-b44c9b7fa0a6)   
(2687418)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS13-024**

<sup>[1]</sup>Para las ediciones compatibles de Microsoft SharePoint Server 2010, además del paquete de actualización de seguridad de Microsoft SharePoint 2010 (2553407), los clientes también deben instalar la actualización de seguridad para Microsoft SharePoint Foundation 2010 (2687418) con el fin de protegerse de las vulnerabilidades descritas en este boletín.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/bb245732). [TechNet Security TechCenter](http://go.microsoft.com/fwlink/?linkid=21171) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar el [Centro de seguridad y protección de Microsoft](http://go.microsoft.com/fwlink/?linkid=85102), donde esta información también está disponible haciendo clic en "Actualizaciones de seguridad".

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Para clientes de Microsoft Office para Mac, Microsoft AutoUpdate para Mac puede servir de ayuda para mantener actualizado el software de Microsoft. Para obtener más información acerca del uso de Microsoft AutoUpdate para Mac, vea [Buscar actualizaciones de software automáticamente](http://mac2.microsoft.com/help/office/14/en-us/word/item/ffe35357-8f25-4df8-a0a3-c258526c64ea).

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS13-001"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Consejos para la detección y la implementación**

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747).

**Microsoft** **Baseline** **Security** **Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, vea [Microsoft Baseline Security Analyzer](http://go.microsoft.com/fwlink/?linkid=21134).

**Windows Server** **UpdateServices**

Windows Server Update Services (WSUS) permite a los administradores implementar de un modo rápido y confiable las actualizaciones críticas y de seguridad más recientes en sistemas operativos Microsoft Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://technet.microsoft.com/wsus/default).

**System** **Center** **Configuration** **Manager**

La administración de actualizaciones de software de System Center Configuration Manager simplifica la tarea compleja de entregar y administrar actualizaciones para los sistemas de TI en toda la empresa. Con System Center Configuration Manager, los administradores de TI pueden ofrecer actualizaciones de los productos de Microsoft a una serie de dispositivos, incluidos equipos de escritorio, portátiles, servidores y dispositivos móviles.

La evaluación automática de vulnerabilidades en System Center Configuration Manager detecta las necesidades de actualizaciones e informa de las acciones recomendadas. La administración de actualizaciones de software en System Center Configuration Manager se basa en Microsoft Windows Software Update Services (WSUS), una infraestructura de actualizaciones probada con la que están familiarizados los administradores de TI de todo el mundo. Para obtener más información acerca de System Center Configuration Manager, vea [Recursos técnicos de System Center](http://technet.microsoft.com/systemcenter/bb980621).

**Systems** **Management Server 2003**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales.

**Nota** System Management Server 2003 está fuera del soporte técnico general desde el 12 de enero de 2010. Para obtener más información acerca de los ciclos de vida de los productos, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742). Ya está disponible la siguiente versión de SMS, System Center Configuration Manager; vea la sección anterior, **System** **Center** **Configuration** **Manager**.

Para obtener más información acerca de cómo los administradores pueden usar SMS 2003 para implementar actualizaciones de seguridad, vea [Escenarios y procedimientos para Microsoft Systems Management Server 2003: Administración de distribución de software y revisiones](http://www.microsoft.com/downloads/details.aspx?familyid=32f2bb4c-42f8-4b8d-844f-2553fd78049f). Para obtener información acerca de SMS, visite [Microsoft Systems Management Server TechCenter](http://technet.microsoft.com/systemcenter/bb545936).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://www.microsoft.com/downloads/en/details.aspx?familyid=7bd3a16e-1899-4e0b-bb99-1320e816167d)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet.microsoft.com/library/cc749197) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Para la publicación de boletines el segundo martes de cada mes, Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga. No hay disponible ninguna versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows para las publicaciones de boletín de seguridad fuera de ciclo.

#### Actualizaciones no relacionadas con la seguridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Artículo 894199 de Microsoft Knowledge Base](http://support.microsoft.com/kb/894199)
-   : Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones de meses anteriores para Windows Server Update Services](http://technet.microsoft.com/wsus/bb456965)
-   . Muestra todas las actualizaciones nuevas, revisadas y publicadas de nuevo para los productos de Microsoft que no sean Microsoft Windows.

#### Microsoft Active Protections Program (MAPP)

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumerados en [Asociados de Microsoft Active Protections Program (MAPP)](http://go.microsoft.com/fwlink/?linkid=215201).

#### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de actualizaciones](http://go.microsoft.com/fwlink/?linkid=21168) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](http://support.microsoft.com/kb/913086).

**Comunidad de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [Comunidad de profesionales de TI de seguridad](http://go.microsoft.com/fwlink/?linkid=21164).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

**MS13-021**

-   Arseniy Akuney, de [TELUS Security Labs](http://telussecuritylabs.com/), por informar de la vulnerabilidad en el uso de OnResize después de la liberación en Internet Explorer (CVE-2013-0087)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad en el uso de saveHistory después de la liberación en Internet Explorer (CVE-2013-0088)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad en el uso de CMarkupBehaviorContext después de la liberación en Internet Explorer (CVE-2013-0089)
-   Stephen Fewer, de [Harmony Security](http://www.harmonysecurity.com) en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad en el uso de CCaret después de la liberación en Internet Explorer (CVE-2013-0090)
-   SkyLined, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad en el uso de CCaret después de la liberación en Internet Explorer (CVE-2013-0090)
-   José A. Vázquez, de Yenteasy - Security Research, en colaboración con [Exodus Intelligence](https://www.exodusintel.com/), por informar de la vulnerabilidad en el uso de CElement después de la liberación en Internet Explorer (CVE-2013-0091)
-   [Aniway.Aniway@gmail.com](mailto:aniway.aniway@gmail.com)
-   , en colaboración con
-   [Zero Day Initiative](http://www.zerodayinitiative.com/)
-   de
-   [HP](http://www.hpenterprisesecurity.com/products)
-   , por informar de la vulnerabilidad en el uso de GetMarkupPtr después de la liberación en Internet Explorer (CVE-2013-0092)
-   [Aniway.Aniway@gmail.com](mailto:aniway.aniway@gmail.com)
-   , en colaboración con
-   [Zero Day Initiative](http://www.zerodayinitiative.com/)
-   de
-   [HP](http://www.hpenterprisesecurity.com/products)
-   , por informar de la vulnerabilidad en el uso de onBeforeCopy después de la liberación en Internet Explorer (CVE-2013-0093)
-   Simon Zuckerbraun, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad en el uso de removeChild después de la liberación en Internet Explorer (CVE-2013-0094)
-   Gen Chen, de [Venustech](http://www.venustech.com.cn/) ADLab, por colaborar con nosotros en la vulnerabilidad en el uso de CTreeNode después de la liberación en Internet Explorer (CVE-2013-1288)
-   [Qihoo 360 Security Center](http://www.360.cn/)
-   , por colaborar con nosotros en la vulnerabilidad en el uso de CTreeNode después de la liberación en Internet Explorer (CVE-2013-1288)

**MS13-022**

-   James Forshaw, [Context Information Security](http://www.contextis.com/), por informar de la vulnerabilidad de anulación de referencia doble en Silverlight (CVE-2013-0074)

**MS13-023**

-   [Aniway.Anyway@gmail.com](mailto:aniway.anyway@gmail.com)
-   , en colaboración con
-   [VeriSign iDefense Labs](http://labs.idefense.com/)
-   , por informar de la vulnerabilidad de confusión de tipo de objeto de árbol en Visio Viewer (CVE-2013-0079)

**MS13-024**

-   Emanuel Bronshtein, de [BugSec](http://www.bugsec.com/), por informar de la vulnerabilidad de la función de devolución de llamada (CVE-2013-0080)
-   Sunil Yadav, de INR Labs ([Network Intelligence India](http://niiconsulting.com/)), por informar de la vulnerabilidad de XSS en SharePoint (CVE-2013-0083)
-   Moritz Jodeit, de [n.runs AG](http://www.nruns.com/), por informar de la vulnerabilidad de recorrido de directorios en SharePoint (CVE-2013-0084)

**MS13-025**

-   Christopher Gabriel, de , por informar de la vulnerabilidad de validación del tamaño del búfer (CVE-2013-0086)

**MS13-026**

-   [Nick Semenkovich](https://technet.microsoft.com/es-ES/mailto:semenko@alum.mit.edu)
-   , por informar de la vulnerabilidad de carga de contenido no intencionada (CVE- 2013-0095)

**MS13-027**

-   Andy Davis, de NCC Group, por informar de la vulnerabilidad del descriptor de USB en Windows (CVE-2013-1285)
-   Andy Davis, de NCC Group, por informar de la vulnerabilidad del descriptor de USB en Windows (CVE-2013-1286)
-   Andy Davis, de NCC Group, por informar de la vulnerabilidad del descriptor de USB en Windows (CVE-2013-1287)

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Soluciones de seguridad para profesionales de TI: Soporte técnico y solución de problemas de seguridad de TechNet
-   Ayuda para proteger su equipo con Windows de virus y malware: [Solución antivirus y centro de seguridad](http://support.microsoft.com/contactus/cu_sc_virsec_master)
-   Soporte local según su país: [Soporte internacional](http://support.microsoft.com/common/international.aspx)

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (12 de marzo de 2013): Publicación del resumen del boletín.
-   V1.1 (15 de marzo de 2013) Para MS13-026, se ha corregido el título del boletín en la sección **Resúmenes ejecutivos**.

*Built at 2014-04-18T01:50:00Z-07:00*
