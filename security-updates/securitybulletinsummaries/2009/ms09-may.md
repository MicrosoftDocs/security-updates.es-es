---
TOCTitle: 'MS09-MAY'
Title: Resumen del boletín de seguridad de Microsoft de mayo 2009
ms:assetid: 'ms09-may'
ms:contentKeyID: 61225404
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms09-may(v=Security.10)'
--- 


Resumen del boletín de seguridad de Microsoft de mayo 2009
==========================================================

Publicado: martes, 12 de mayo de 2009 | Actualizado: martes, 9 de junio de 2009

**Versión:** 2.0

Este resumen del boletín enumera los boletines de seguridad publicados para mayo de 2009.

Con la publicación de los boletines de mayo de 2009, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 7 de mayo de 2009. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://technet.microsoft.com/security/bulletin/notify) (en inglés).

Microsoft va a realizar una conferencia en línea para atender las consultas de los clientes sobre estos boletines el 13 de mayo de 2009, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora a la conferencia en línea del boletín de seguridad de mayo](http://msevents.microsoft.com/cui/webcasteventdetails.aspx?culture=en-us&eventid=1032395223). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad y de alta prioridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

### Información del boletín

Resúmenes ejecutivos
--------------------

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-017">MS09-017</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Office PowerPoint podrían permitir la ejecución remota de código (967340)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y varias vulnerabilidades de las que se ha informado de forma privada en Microsoft Office PowerPoint que podrían permitir la ejecución remota de código si un usuario abre un archivo de PowerPoint especialmente diseñado. Un atacante que aprovechara cualquiera de estas vulnerabilidades podría lograr el control total de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y de identificador de CVE.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de que se publique código funcional que aproveche la vulnerabilidad en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Debe revisar cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/en-us/security/cc998259.aspx).

 
<p> </p>
<table style="border:1px solid black;">
<thead>
<tr class="header">
<th style="border:1px solid black;" >Identificador del boletín</th>
<th style="border:1px solid black;" >Título del boletín</th>
<th style="border:1px solid black;" >Identificador CVE</th>
<th style="border:1px solid black;" >Evaluación de índice de explotabilidad</th>
<th style="border:1px solid black;" >Notas clave</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-017">MS09-017</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office PowerPoint podrían permitir la ejecución remota de código (967340)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0220">CVE-2009-0220</a></td>
<td style="border:1px solid black;">Para versiones de Office compiladas sin /GS:<br />
<a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">La protección /GS generada al compilar Office 2003 Service Pack 3 y versiones posteriores de Office es un factor atenuante para esta vulnerabilidad que reduce considerablemente la exposición de dichos sistemas a <a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>3</strong></a> - Improbabilidad de código funcional que aproveche la vulnerabilidad.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-017">MS09-017</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office PowerPoint podrían permitir la ejecución remota de código (967340)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0221">CVE-2009-0221</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-017">MS09-017</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office PowerPoint podrían permitir la ejecución remota de código (967340)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0222">CVE-2009-0222</a></td>
<td style="border:1px solid black;">Para versiones de Office compiladas sin /GS:<br />
<a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">La protección /GS generada al compilar Office 2003 Service Pack 3 y versiones posteriores de Office es un factor atenuante para esta vulnerabilidad que reduce considerablemente la exposición de dichos sistemas a <a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>3</strong></a> - Improbabilidad de código funcional que aproveche la vulnerabilidad.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-017">MS09-017</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office PowerPoint podrían permitir la ejecución remota de código (967340)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0223">CVE-2009-0223</a></td>
<td style="border:1px solid black;">Para versiones de Office compiladas sin /GS:<br />
<a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">La protección /GS generada al compilar Office 2003 Service Pack 3 y versiones posteriores de Office es un factor atenuante para esta vulnerabilidad que reduce considerablemente la exposición de dichos sistemas a <a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>3</strong></a> - Improbabilidad de código funcional que aproveche la vulnerabilidad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-017">MS09-017</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office PowerPoint podrían permitir la ejecución remota de código (967340)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0224">CVE-2009-0224</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-017">MS09-017</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office PowerPoint podrían permitir la ejecución remota de código (967340)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0225">CVE-2009-0225</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-017">MS09-017</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office PowerPoint podrían permitir la ejecución remota de código (967340)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0226">CVE-2009-0226</a></td>
<td style="border:1px solid black;">Para versiones de Office compiladas sin /GS:<br />
<a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">La protección /GS generada al compilar Office 2003 Service Pack 3 y versiones posteriores de Office es un factor atenuante para esta vulnerabilidad que reduce considerablemente la exposición de dichos sistemas a <a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>3</strong></a> - Improbabilidad de código funcional que aproveche la vulnerabilidad.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-017">MS09-017</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office PowerPoint podrían permitir la ejecución remota de código (967340)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0227">CVE-2009-0227</a></td>
<td style="border:1px solid black;">Para versiones de Office compiladas sin /GS:<br />
<a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">La protección /GS generada al compilar Office 2003 Service Pack 3 y versiones posteriores de Office es un factor atenuante para esta vulnerabilidad que reduce considerablemente la exposición de dichos sistemas a <a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>3</strong></a> - Improbabilidad de código funcional que aproveche la vulnerabilidad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-017">MS09-017</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office PowerPoint podrían permitir la ejecución remota de código (967340)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0556">CVE-2009-0556</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><strong>Esta vulnerabilidad se está aprovechando actualmente en el ecosistema de Internet.</strong></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-017">MS09-017</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office PowerPoint podrían permitir la ejecución remota de código (967340)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1128">CVE-2009-1128</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-017">MS09-017</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office PowerPoint podrían permitir la ejecución remota de código (967340)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1129">CVE-2009-1129</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-017">MS09-017</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office PowerPoint podrían permitir la ejecución remota de código (967340)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1130">CVE-2009-1130</a></td>
<td style="border:1px solid black;">Para versiones de Office compiladas sin /GS:<br />
<a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">La protección /GS generada al compilar Office 2003 Service Pack 3 y versiones posteriores de Office es un factor atenuante para esta vulnerabilidad que reduce considerablemente la exposición de dichos sistemas a <a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>3</strong></a> - Improbabilidad de código funcional que aproveche la vulnerabilidad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-017">MS09-017</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office PowerPoint podrían permitir la ejecución remota de código (967340)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1131">CVE-2009-1131</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-017">MS09-017</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office PowerPoint podrían permitir la ejecución remota de código (967340)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1137">CVE-2009-1137</a></td>
<td style="border:1px solid black;">Para versiones de Office compiladas sin /GS:<br />
<a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">La protección /GS generada al compilar Office 2003 Service Pack 3 y versiones posteriores de Office es un factor atenuante para esta vulnerabilidad que reduce considerablemente la exposición de dichos sistemas a <a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>3</strong></a> - Improbabilidad de código funcional que aproveche la vulnerabilidad.</td>
</tr>
</tbody>
</table>
  
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
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Conjuntos de programas, sistemas y componentes de Microsoft Office  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-017**](http://technet.microsoft.com/security/bulletin/ms09-017)
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
Microsoft Office 2000 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Office PowerPoint 2000 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=f443312a-ac74-4ebc-a4ac-7a756aa67894)  
(KB957790)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Office PowerPoint 2002 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=a24ec7ab-c1c7-4ddb-8b6e-107f1af67f49)  
(KB957781)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Office PowerPoint 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=ccfa978b-3340-40db-a45d-c880ba36b106)  
(KB957784)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
2007 Microsoft Office System Service Pack 1 y 2007 Microsoft Office System Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft Office PowerPoint 2007 Service Pack 1 y Microsoft Office PowerPoint 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=11f8380f-ffb6-4c22-a89c-3dc55d0f9834)  
(KB957789)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Office para Mac
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-017**](http://technet.microsoft.com/security/bulletin/ms09-017)
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
Microsoft Office 2004 para Mac
</td>
<td style="border:1px solid black;">
[Microsoft Office 2004 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=5557bfb7-ebb4-4c42-8042-41e830c4e550)  
(KB969661)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2008 para Mac
</td>
<td style="border:1px solid black;">
[Microsoft Office 2008 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=58326da2-eb75-4b42-b1bc-e70319defb58)  
(KB971822)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Convertidor de archivos con formatos XML abiertos para Mac
</td>
<td style="border:1px solid black;">
[Convertidor de archivos con formatos XML abiertos para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=9d6d9eaa-8442-4184-8886-faab2803bde6)  
(KB971824)  
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
[**MS09-017**](http://technet.microsoft.com/security/bulletin/ms09-017)
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
PowerPoint Viewer
</td>
<td style="border:1px solid black;">
[PowerPoint Viewer 2003](http://www.microsoft.com/downloads/details.aspx?familyid=6a57e6ed-bd24-406f-87bb-117391e083e0)  
(KB969615)  
(Importante)  
[PowerPoint Viewer 2007 Service Pack 1 y PowerPoint Viewer 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=141b8338-5c52-4326-a9e4-d2f2d8940d9c)  
(KB970059)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007
</td>
<td style="border:1px solid black;">
[Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 1 y Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e1d3a4c3-538a-4f98-8d60-250803a80e2a)  
(KB969618)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Works 8.5
</td>
<td style="border:1px solid black;">
[Microsoft Works 8.5](http://www.microsoft.com/downloads/details.aspx?familyid=628280fe-e035-4274-85f2-393d9bad543c)  
(KB967043)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Works 9
</td>
<td style="border:1px solid black;">
[Microsoft Works 9](http://www.microsoft.com/downloads/details.aspx?familyid=f6fa110e-45c6-450f-ae47-c89a06e3f762)  
(KB967044)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS09-017**

Microsoft ha vuelto a publicar MS09-017 para proporcionar paquetes de actualización de seguridad para Microsoft Office 2004 para Mac, Microsoft Office 2008 para Mac, Convertidor de archivos con formatos XML abiertos para Mac, Microsoft Works 8.5 y Microsoft Works 9. Los clientes que actualmente tengan este software deben aplicar la actualización inmediatamente.

Cuando MS09-017 se publicó por primera vez, estos paquetes de actualización de seguridad todavía estaban en desarrollo. En ese momento, Microsoft publicó MS09-017 porque se disponía de paquetes de actualización preparados en el ciclo normal de publicación de boletines para una línea de producto completa dirigidos a la inmensa mayoría de clientes expuestos. Esta publicación de MS09-017 completa la gama de actualizaciones para el software que está afectado por las vulnerabilidades descritas en este boletín.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://go.microsoft.com/fwlink/?linkid=69903). [TechNet Security Center](http://go.microsoft.com/fwlink/?linkid=21171) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://www.microsoft.com/spain/athome/security/default.mspx), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747), [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130) y [Office Update](http://go.microsoft.com/fwlink/?linkid=21135). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://www.microsoft.com/downloads/search.aspx?displaylang=es). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS07-036"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Consejos para la detección y la implementación**

Microsoft ofrece recomendaciones para la detección y la implementación de las actualizaciones de seguridad de este mes. Esta orientación también ayudará a los profesionales de TI a comprender el funcionamiento de distintas herramientas que sirven de ayuda en la implementación de la actualización de seguridad, como Windows Update, Microsoft Update, Office Update, Microsoft Baseline Security Analyzer (MBSA), Office Detection Tool, Microsoft Systems Management Server (SMS) y Extended Security Update Inventory Tool (ESUIT). Para obtener más información, consulte el [artículo 910723 de Microsoft Knowledge Base](http://support.microsoft.com/kb/910723).

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://go.microsoft.com/fwlink/?linkid=21134).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar con rapidez y fiabilidad las actualizaciones críticas y de seguridad más recientes en sistemas operativos Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://www.microsoft.com/spain/technet/seguridad/herramientas/wsus.mspx).

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. La siguiente versión de SMS, System Center Configuration Manager 2007, ya está disponible; consulte también [System Center Configuration Manager 2007](http://technet.microsoft.com/en-us/library/bb735860.aspx). Para obtener más información acerca de cómo pueden utilizar los administradores SMS 2003 para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar [Software Updates Services Feature Pack](http://go.microsoft.com/fwlink/?linkid=33340) como ayuda para la implementación de actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://www.microsoft.com/spain/smserver/default.mspx).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer y Microsoft Office Detection Tool como ayuda para proporcionar un amplio soporte técnico para la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=33387) y en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet2.microsoft.com/windowsvista/en/library/4279e239-37a4-44aa-aec5-4e70fe39f9de1033.mspx?mfr=true) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Microsoft Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Artículo 894199 de Microsoft Knowledge Base](http://support.microsoft.com/kb/894199): Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones nuevas, revisadas y publicadas para productos de Microsoft distintos de Microsoft Windows](http://technet.microsoft.com/en-us/wsus/dd573344.aspx).

#### Microsoft Active Protections Program (MAPP)

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumeradas en [Asociados de Microsoft Active Protections Program (MAPP)](http://www.microsoft.com/security/msrc/mapp/partners.mspx).

#### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de actualizaciones](http://www.microsoft.com/spain/technet/seguridad/areas/actualiza/default.mspx) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://www.microsoft.com/downloads/search.aspx?displaylang=es) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](http://support.microsoft.com/kb/913086).

**Comunidad de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [IT Pro Security Community](http://go.microsoft.com/fwlink/?linkid=21164) (en inglés).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

-   Un investigador anónimo, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de dos problemas descritos en MS09-017
-   Sean Larsson, de [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de dos problemas descritos en MS09-017
-   Nicolas Joly, de [VUPEN Security](http://www.vupen.com/), por informar de un problema descrito en MS09-017
-   Marsu Pilami, de [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de varios problemas descritos en MS09-017
-   Nicolas Joly, de [VUPEN Security](http://www.vupen.com/), por informar de un problema descrito en MS09-017
-   Marsu Pilami, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS09-017
-   Ling y Wushi, de [team509](http://www.team509.com/), en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), y Sean Larsson, de [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS09-017
-   Carsten H. Eiram, de [Secunia](http://secunia.com/), por informar de un problema descrito en MS09-017

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Puede solicitar soporte técnico en los [Servicios de soporte técnico de Microsoft](http://support.microsoft.com/default.aspx?scid=fh;es-es;incidentsubmit) o a través del teléfono 902 197 198.
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (12 mayo de 2009): Publicación del resumen del boletín.
-   V1.1 (13 de mayo de 2009): Se ha quitado una nota errónea para MS09-017 que pertenece a las actualizaciones de seguridad KB969618 y KB957789 para las versiones compatibles de Microsoft Office PowerPoint 2007.
-   V2.0 (9 de junio de 2009): Se ha revisado para anunciar la nueva publicación de MS09-017, que proporciona paquetes de actualización de seguridad para Microsoft Office 2004 para Mac, Microsoft Office 2008 para Mac, Convertidor de archivos con formatos XML abiertos para Mac, Microsoft Works 8.5 y Microsoft Works 9. Los clientes que actualmente tengan instalado este software deben aplicar la actualización inmediatamente.

*Built at 2014-04-18T01:50:00Z-07:00*
