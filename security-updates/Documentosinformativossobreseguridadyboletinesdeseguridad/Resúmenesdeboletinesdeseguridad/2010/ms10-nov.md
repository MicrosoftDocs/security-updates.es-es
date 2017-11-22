---
TOCTitle: 'MS10-NOV'
Title: Resumen del boletín de seguridad de Microsoft de noviembre 2010
ms:assetid: 'ms10-nov'
ms:contentKeyID: 61225417
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms10-nov(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de noviembre 2010
===============================================================

Publicado: martes, 9 de noviembre de 2010 | Actualizado: miércoles, 13 de abril de 2011

**Versión:** 2.1

Este resumen del boletín enumera los boletines de seguridad publicados para noviembre de 2010.

Con la publicación de los boletines de noviembre de 2010, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 4 de noviembre de 2010. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance) .

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://technet.microsoft.com/es-es/security/dd252948.aspx) (en inglés).

Microsoft va a realizar una conferencia en línea para atender las consultas de los clientes sobre estos boletines el 10 de noviembre de 2010, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de noviembre](https://msevents.microsoft.com/cui/webcasteventdetails.aspx?culture=en-us&eventid=1032454441) . Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary) .

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad y de alta prioridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional** .

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-087">MS10-087</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Office podrían permitir la ejecución remota de código (2423930)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y cinco vulnerabilidades de las que se ha informado de forma privada en Microsoft Office. La vulnerabilidad más grave podría permitir la ejecución remota de código si un usuario abre un mensaje de correo electrónico RTF especialmente diseñado u obtiene una vista previa de él. Un intruso que aprovechara cualquiera de estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario local. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-088">MS10-088</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft PowerPoint podrían permitir la ejecución remota de código (2293386)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft Office que podrían permitir la ejecución remota de código si un usuario abre un archivo de PowerPoint especialmente diseñado. Un atacante que aprovechara cualquiera de estas vulnerabilidades podría lograr el control total de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-089">MS10-089</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Forefront Unified Access Gateway (UAG) podrían permitir la elevación de privilegios (2316074)</strong><br />
<br />
Esta actualización de seguridad resuelve cuatro vulnerabilidades de las que se ha informado de forma privada en Forefront Unified Access Gateway (UAG). La más grave de estas vulnerabilidades podría permitir la elevación de privilegios si un usuario visita un sitio web afectado mediante una URL especialmente diseñada. No obstante, el atacante no podría obligar a los usuarios a visitar un sitio web. Por lo tanto, tendría que atraerlos al sitio web; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger que lleve a los usuarios al sitio web del atacante.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Forefront United Access Gateway</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de nivel de evaluación de explotabilidad decreciente y, a continuación, por identificador de CVE. Sólo se incluyen las vulnerabilidades que tiene una clasificación de gravedad de crítica o importante en los boletines.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de que se publique código funcional que aproveche la vulnerabilidad en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Debe revisar cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/es-es/security/cc998259.aspx) .
  
| Identificador del boletín                                           | Título de vulnerabilidad                                                                                         | Identificador CVE                                                                | Evaluación de índice de explotabilidad                                                                                                  | Notas clave                                                                                            |  
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|  
| [MS10-088](http://technet.microsoft.com/security/bulletin/ms10-088) | Vulnerabilidad de desbordamiento del búfer de análisis en PowerPoint                                             | [CVE-2010-2572](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2572) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                              |  
| [MS10-089](http://technet.microsoft.com/security/bulletin/ms10-089) | Vulnerabilidad XSS en UAG que permite la elevación de privilegios                                                | [CVE-2010-2733](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2733) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                              |  
| [MS10-089](http://technet.microsoft.com/security/bulletin/ms10-089) | Vulnerabilidad de problema de XSS en sitio web de portal para móviles de UAG en Forefront Unified Access Gateway | [CVE-2010-2734](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2734) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                              |  
| [MS10-087](http://technet.microsoft.com/security/bulletin/ms10-087) | Vulnerabilidad de desbordamiento del búfer de la pila de RTF                                                     | [CVE-2010-3333](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-3333) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                              |  
| [MS10-087](http://technet.microsoft.com/security/bulletin/ms10-087) | Vulnerabilidad de registro de dibujos de Office                                                                  | [CVE-2010-3334](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-3334) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                              |  
| [MS10-087](http://technet.microsoft.com/security/bulletin/ms10-087) | Vulnerabilidad de control de excepciones de dibujos                                                              | [CVE-2010-3335](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-3335) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                              |  
| [MS10-087](http://technet.microsoft.com/security/bulletin/ms10-087) | Vulnerabilidad en la carga de bibliotecas no seguras                                                             | [CVE-2010-3337](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-3337) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | **Esa vulnerabilidad ya se ha divulgado**                                                              |  
| [MS10-089](http://technet.microsoft.com/security/bulletin/ms10-089) | Vulnerabilidad de XSS en Signurl.asp                                                                             | [CVE-2010-3936](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-3936) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                              |  
| [MS10-087](http://technet.microsoft.com/security/bulletin/ms10-087) | Vulnerabilidad de subdesbordamiento de enteros en PowerPoint que provoca daños en el montón                      | [CVE-2010-2573](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2573) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | [MS10-088](http://technet.microsoft.com/security/bulletin/ms10-088) también trata esta vulnerabilidad. |  
| [MS10-088](http://technet.microsoft.com/security/bulletin/ms10-088) | Vulnerabilidad de subdesbordamiento de enteros en PowerPoint que provoca daños en el montón                      | [CVE-2010-2573](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2573) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | [MS10-087](http://technet.microsoft.com/security/bulletin/ms10-087) también trata esta vulnerabilidad. |  
| [MS10-087](http://technet.microsoft.com/security/bulletin/ms10-087) | Vulnerabilidad de lectura de AV de SPID grande en MSO                                                            | [CVE-2010-3336](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-3336) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                              |  
| [MS10-089](http://technet.microsoft.com/security/bulletin/ms10-089) | Vulnerabilidad de suplantación de identidad de redireccionamiento de UAG                                         | [CVE-2010-2732](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2732) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | Se trata únicamente de una vulnerabilidad de suplantación                                              |
  
Ubicaciones de descarga y software afectado  
-------------------------------------------
  
Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.
  
**¿Cómo se usan estas tablas?**  
  
Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, se indica un hipervínculo a la actualización de software disponible y también se muestra la clasificación de gravedad de dicha actualización de software.
  
**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.
  
#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tr class="thead">
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Conjuntos de programas y componentes de Microsoft Office  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-087**](http://technet.microsoft.com/security/bulletin/ms10-087)
</td>
<td style="border:1px solid black;">
[**MS10-088**](http://technet.microsoft.com/security/bulletin/ms10-088)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
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
[Microsoft Office XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=f32648e3-2fb5-472c-932f-360e5d3c0931)  
(KB2289169)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft PowerPoint 2002 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=3efbf9f6-734a-46ac-8f92-87b6ec819bfa)  
(KB2413272)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Office 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=07a6cf76-2cea-4c54-b66d-50e9eed108ac)  
(KB2289187)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft PowerPoint 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=108286d4-fb68-40d6-a7b1-64b3a4eb87ee)  
(KB2413304)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft Office 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=be0c5878-60c0-4700-8836-50d369b51d04)  
(KB2289158)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2010 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2010 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=0b308508-0e1e-4e90-b2b8-7e32bfc5dbf4)  
(KB2289161)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2010 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=534c6a2a-e7c6-4adf-8b81-e009a2b5fff4)  
(KB2289161)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Office para Mac
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-087**](http://technet.microsoft.com/security/bulletin/ms10-087)
</td>
<td style="border:1px solid black;">
[**MS10-088**](http://technet.microsoft.com/security/bulletin/ms10-088)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
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
[Microsoft Office 2008 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=ad1b1984-b2b2-49b3-a1dd-385b77d9248a)  
(KB2476512)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office para Mac 2011
</td>
<td style="border:1px solid black;">
[Microsoft Office para Mac 2011](http://www.microsoft.com/downloads/details.aspx?familyid=8bd6ca3b-8004-4e8d-a09d-220dcbbce799)  
(KB2454823)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Convertidor de archivos con formatos XML abiertos para Mac
</td>
<td style="border:1px solid black;">
[Convertidor de archivos con formatos XML abiertos para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=b846d255-a7d4-4a2c-a084-d434c29fe676)  
(KB2476511)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Otro software de Office
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-087**](http://technet.microsoft.com/security/bulletin/ms10-087)
</td>
<td style="border:1px solid black;">
[**MS10-088**](http://technet.microsoft.com/security/bulletin/ms10-088)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft PowerPoint Viewer
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft PowerPoint Viewer 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=df826b79-7398-45de-943c-6f6f0af1b4e3)  
(KB2413381)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS10-087**

<sup>[1]</sup> La actualización de seguridad para Microsoft Office 2004 para Mac (KB2505924) está disponible desde el 12 de abril de 2011. Vea el boletín para obtener información detallada.

**Nota para MS10-088**

<sup>[1]</sup> La actualización de seguridad para Microsoft Office 2004 para Mac (KB2505924) está disponible desde el 12 de abril de 2011. Vea el boletín para obtener información detallada.

#### Software de acceso remoto de Microsoft

 
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
Microsoft Forefront Unified Access Gateway
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-089**](http://technet.microsoft.com/security/bulletin/ms10-089)
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
Microsoft Forefront Unified Access Gateway
</td>
<td style="border:1px solid black;">
[Forefront Unified Access Gateway 2010](http://www.microsoft.com/downloads/details.aspx?familyid=5f2ee08e-e289-47db-bd3f-7b9cfc1eb985)<sup>[1]</sup>
(KB2433585)  
(Importante)  

[Forefront Unified Access Gateway 2010 actualización 1](http://www.microsoft.com/downloads/details.aspx?familyid=db0b70c8-1fa5-4d92-9888-3500c7566b19)<sup>[1]</sup>
(KB2433584)  
(Importante)  

[Forefront Unified Access Gateway 2010 actualización 2](http://www.microsoft.com/downloads/details.aspx?familyid=4e3ee07a-771c-46ee-959f-82389bab67d7)<sup>[1]</sup>
(KB2418933)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS10-089**

<sup>[1]</sup> Esta actualización sólo está disponible en el Centro de descarga de Microsoft.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://go.microsoft.com/fwlink/?linkid=69903) . [TechNet Security Center](http://go.microsoft.com/fwlink/?linkid=21171) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://go.microsoft.com/fwlink/?linkid=85102) , donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130) . También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129) . Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155) . El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS07-036"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900) .

**Consejos para la detección y la implementación**

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747) .

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://go.microsoft.com/fwlink/?linkid=21134) .

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar de un modo rápido y confiable las actualizaciones críticas y de seguridad más recientes en sistemas operativos Microsoft Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://go.microsoft.com/fwlink/?linkid=50120) .

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. La siguiente versión de SMS, System Center Configuration Manager 2007, ya está disponible; consulte también [System Center Configuration Manager 2007](http://technet.microsoft.com/en-us/library/bb735860.aspx) . Para obtener más información acerca de cómo pueden utilizar los administradores SMS 2003 para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar Security Update Inventory Tool (SUIT) como ayuda para implementar las actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://go.microsoft.com/fwlink/?linkid=21158) .

**Nota** SMS usa las herramientas Microsoft Baseline Security Analyzer para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341) . Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161) ) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet2.microsoft.com/windowsvista/en/library/4279e239-37a4-44aa-aec5-4e70fe39f9de1033.mspx?mfr=true) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en) .

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Microsoft Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Microsoft Knowledge Base, artículo 894199](http://support.microsoft.com/kb/894199) : Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones de meses anteriores para Windows Server Update Services](http://technet.microsoft.com/en-us/wsus/bb456965.aspx) . Muestra todas las actualizaciones nuevas, revisadas y publicadas de nuevo para los productos de Microsoft que no sean Microsoft Windows.

#### Microsoft Active Protections Program (MAPP)

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumeradas en [Asociados de Microsoft Active Protections Program (MAPP)](http://www.microsoft.com/security/msrc/mapp/partners.mspx) .

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

-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de  [TippingPoint](http://www.tippingpoint.com/) , por informar de un problema descrito en MS10-087
-   [team509](http://www.team509.com/) , en colaboración con [Verisign iDefense Labs](http://labs.idefense.com/) , por informar de un problema descrito en MS10-087
-   Dyon Balding, de [Secunia](http://secunia.com/) , por informar de un problema descrito en MS10-087
-   Will Dorman, de [CERT Coordination Center](http://www.cert.org/) , por informar de un problema descrito en MS10-087
-   [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/) , por informar de un problema descrito en MS10-087
-   Chaouki Bekrar, de [VUPEN Vulnerability Research Team](http://www.vupen.com/) , por informar de un problema descrito en MS10-087
-   Haifei Li, de [FortiGuard Labs de Fortinet](http://www.fortiguard.com/) , por informar de un problema descrito en MS10-087
-   Simon Raner, de [ACROS Security](http://www.acrossecurity.com) , por informar de un problema descrito en MS10-087
-   Alin Rad Pop, de [Secunia Research](http://secunia.com/) , por informar de un problema descrito en MS10-088
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de  [TippingPoint](http://www.tippingpoint.com/) , por informar de un problema descrito en MS10-088
-   Eyal Gruner, de [BugSec](http://www.bugsec.com/) , por colaborar con nosotros en tres problemas descritos en MS10-089

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742) .
-   Los clientes de Estados Unidos y Canadá pueden recibir soporte técnico del [soporte de seguridad](http://go.microsoft.com/fwlink/?linkid=21131) o en el teléfono 1-866-PCSAFETY. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de las opciones de asistencia disponibles, visite [Ayuda y soporte técnico de Microsoft](http://support.microsoft.com/) .
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (9 de noviembre de 2010): Publicación del resumen del boletín.
-   V1.1 (9 de noviembre de 2010): Para MS10-088, se ha corregido la versión afectada de "Microsoft PowerPoint Viewer" a "Microsoft PowerPoint Viewer 2007 Service Pack 2". Se trata únicamente de un cambio informativo. Los clientes que ya han actualizado correctamente sus sistemas, incluidos los clientes con la actualización automática habilitada, no necesitan realizar ninguna acción. Es posible que los clientes que no hayan instalado esta actualización anteriormente tengan que volver a determinar si sus sistemas requieren esta actualización según la revisión del software afectado.
-   V1.2 (17 de noviembre de 2010): Para MS10-087, se ha corregido el índice de explotabilidad para agregar CVE-2010-2573 como una vulnerabilidad corregida por esta actualización. Se trata únicamente de un cambio informativo.
-   V2.0 (15 de diciembre de 2010): Se ha revisado este resumen del boletín para anunciar que para MS10-087 hay disponibles actualizaciones de seguridad para Microsoft Office 2008 para Mac (KB2476512) y Convertidor de archivos con formatos XML abiertos para Mac (KB2476511). Microsoft recomienda que los usuarios de este software apliquen estas actualizaciones lo antes posible.
-   V2.1 (13 de abril de 2011): Se ha revisado este resumen del boletín para anunciar que está disponible la actualización de seguridad para Microsoft Office 2004 para Mac (KB2505924). Vea MS10-087 y MS10-088 para obtener información detallada.

*Built at 2014-04-18T01:50:00Z-07:00*