---
TOCTitle: 'MS10-MAR'
Title: Resumen del boletín de seguridad de Microsoft de marzo 2010
ms:assetid: 'ms10-mar'
ms:contentKeyID: 61225415
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms10-mar(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de marzo 2010
===========================================================

Publicado: martes, 9 de marzo de 2010 | Actualizado: miércoles, 11 de agosto de 2010

**Versión:** 3.1

Este resumen del boletín enumera los boletines de seguridad publicados para marzo de 2010.

Con la publicación de los boletines de marzo de 2010, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 4 de marzo de 2010. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar una conferencia en línea para atender las consultas de los clientes sobre estos boletines el 10 de marzo de 2010, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora a la conferencia en línea del boletín de seguridad de marzo](http://msevents.microsoft.com/cui/webcasteventdetails.aspx?eventid=1032427711&eventcategory=4&culture=en-us&countrycode=us). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

Para el boletín de seguridad fuera de ciclo agregado a la versión 2.0 de este resumen de boletín, MS10-018, Microsoft realizará un webcast para atender las preguntas de los clientes acerca del boletín el 30 de marzo de 2010, a la 1:00 p.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del 30 de marzo a la 1:00 p.m](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032448112&culture=en-us). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-018">MS10-018</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (980182)</strong> <br />
<br />
Esta actualización de seguridad resuelve nueve vulnerabilidades de las que se ha informado de forma privada y una vulnerabilidad de la que se ha informado de forma pública en Internet Explorer. La más grave de las vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-016">MS10-016</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Windows Movie Maker podría permitir la ejecución remota de código (975561)</strong><br />
<br />
Esta actualización de seguridad corrige una vulnerabilidad de la que se ha informado de forma privada en Windows Movie Maker y Microsoft Producer 2003. Windows Live Movie Maker, que está disponible para Windows Vista y Windows 7, no está afectado por esta vulnerabilidad. La vulnerabilidad podría permitir la ejecución remota de código si un atacante envía un archivo de proyecto de Movie Maker o Microsoft Producer especialmente diseñado y convence al usuario de que lo abra. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-017">MS10-017</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Office Excel podrían permitir la ejecución remota de código (980150)</strong><br />
<br />
Esta actualización de seguridad resuelve siete vulnerabilidades de las que se ha informado de forma privada en Microsoft Office Excel. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario abre un archivo de Excel especialmente diseñado. Un intruso que aprovechara cualquiera de estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario local. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de nivel de evaluación de explotabilidad decreciente y, a continuación, por identificador de CVE.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de que se publique código funcional que aproveche la vulnerabilidad en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Debe revisar cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/es-es/security/cc998259.aspx).
  
| Identificador del boletín                                           | Título de vulnerabilidad                                                                                       | Identificador CVE                                                                | Evaluación de índice de explotabilidad                                                                                                  | Notas clave                                                                           |  
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|  
| [MS10-017](http://technet.microsoft.com/security/bulletin/ms10-017) | Vulnerabilidad de daños en la memoria relacionada con los registros en Microsoft Office Excel                  | [CVE-2010-0257](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0257) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                             |  
| [MS10-017](http://technet.microsoft.com/security/bulletin/ms10-017) | Vulnerabilidad del desbordamiento del montón del registro MDXTUPLE en Microsoft Office Excel                   | [CVE-2010-0260](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0260) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                             |  
| [MS10-017](http://technet.microsoft.com/security/bulletin/ms10-017) | Vulnerabilidad del desbordamiento del montón del registro MDXSET en Microsoft Office Excel                     | [CVE-2010-0261](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0261) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                             |  
| [MS10-017](http://technet.microsoft.com/security/bulletin/ms10-017) | Vulnerabilidad de ejecución de código al analizar el archivo XLSX en Microsoft Office Excel                    | [CVE-2010-0263](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0263) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                             |  
| [MS10-017](http://technet.microsoft.com/security/bulletin/ms10-017) | Vulnerabilidad del análisis del registro DbOrParamQry en Microsoft Office Excel                                | [CVE-2010-0264](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0264) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                             |  
| [MS10-016](http://technet.microsoft.com/security/bulletin/ms10-016) | Vulnerabilidad de desbordamiento del búfer en Movie Maker y Producer                                           | [CVE-2010-0265](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0265) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                             |  
| [MS10-018](http://technet.microsoft.com/security/bulletin/ms10-018) | Vulnerabilidad de daños en la memoria relacionada con los objetos                                              | [CVE-2010-0491](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0491) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                             |  
| [MS10-018](http://technet.microsoft.com/security/bulletin/ms10-018) | Vulnerabilidad de daños en la memoria relacionada con los objetos                                              | [CVE-2010-0492](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0492) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                             |  
| [MS10-018](http://technet.microsoft.com/security/bulletin/ms10-018) | Vulnerabilidad entre dominios por elemento HTML                                                                | [CVE-2010-0494](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0494) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | La ejecución de código sólo es posible en Windows 2000                                |  
| [MS10-018](http://technet.microsoft.com/security/bulletin/ms10-018) | Vulnerabilidad de daños en la memoria sin inicializar                                                          | [CVE-2010-0806](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0806) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | **Esta vulnerabilidad se está aprovechando actualmente en el ecosistema de Internet** |  
| [MS10-018](http://technet.microsoft.com/security/bulletin/ms10-018) | Vulnerabilidad de daños en la memoria relacionada con el procesamiento HTML                                    | [CVE-2010-0807](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0807) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                             |  
| [MS10-017](http://technet.microsoft.com/security/bulletin/ms10-017) | Vulnerabilidad de confusión de tipo de objeto de hoja en Microsoft Office Excel                                | [CVE-2010-0258](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0258) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                             |  
| [MS10-017](http://technet.microsoft.com/security/bulletin/ms10-017) | Vulnerabilidad en la memoria sin inicializar relacionada con el registro FNGROUPNAME de Microsoft Office Excel | [CVE-2010-0262](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0262) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                             |  
| [MS10-018](http://technet.microsoft.com/security/bulletin/ms10-018) | Vulnerabilidad de daños en la memoria relacionada con la condición de ejecución                                | [CVE-2010-0489](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0489) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                             |  
| [MS10-018](http://technet.microsoft.com/security/bulletin/ms10-018) | Vulnerabilidad de daños en la memoria                                                                          | [CVE-2010-0805](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0805) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                             |  
| [MS10-018](http://technet.microsoft.com/security/bulletin/ms10-018) | Vulnerabilidad de daños en la memoria sin inicializar                                                          | [CVE-2010-0267](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0267) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | (Ninguna)                                                                             |  
| [MS10-018](http://technet.microsoft.com/security/bulletin/ms10-018) | Vulnerabilidad de divulgación de información posterior a la codificación                                       | [CVE-2010-0488](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0488) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | (Ninguna)                                                                             |  
| [MS10-018](http://technet.microsoft.com/security/bulletin/ms10-018) | Vulnerabilidad de daños en la memoria sin inicializar                                                          | [CVE-2010-0490](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0490) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | (Ninguna)                                                                             |
  
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
<th style="border:1px solid black;" >
</th>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Windows 2000  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-016**](http://technet.microsoft.com/security/bulletin/ms10-016)
</td>
<td style="border:1px solid black;">
[**MS10-018**](http://technet.microsoft.com/security/bulletin/ms10-018)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 5.01 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=389da7a9-e0a3-4b5d-801e-0a38fc55dcec)  
(Crítica)  

[Internet Explorer 6 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=daf199c4-da56-4a7f-80e6-3936ce5c267b)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows XP
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-016**](http://technet.microsoft.com/security/bulletin/ms10-016)
</td>
<td style="border:1px solid black;">
[**MS10-018**](http://technet.microsoft.com/security/bulletin/ms10-018)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Service Pack 2 y Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Movie Maker 2.1](http://www.microsoft.com/downloads/details.aspx?familyid=6301e462-02be-4b9a-bae9-7c4821b42d2d)<sup>[1]</sup>
(Importante)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=2f2caa01-5cd1-45cb-9995-e34d933920d4)  
(Crítica)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=167ed896-d383-4dc0-9183-cd4cb73e17e7)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=46172617-293a-44c7-95b6-18202ab06a41)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Movie Maker 2.1](http://www.microsoft.com/downloads/details.aspx?familyid=cae81585-d0df-41b8-9277-ca02f1265056)<sup>[1]</sup>
(Importante)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=6c711387-6853-477c-917e-820a97613cf9)  
(Crítica)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=aadb1d97-5cec-45ed-9967-aaf41a0bcdac)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=284d70ea-24a3-4e67-a2a8-e9f272f728db)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-016**](http://technet.microsoft.com/security/bulletin/ms10-016)
</td>
<td style="border:1px solid black;">
[**MS10-018**](http://technet.microsoft.com/security/bulletin/ms10-018)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=dc77f1c9-8240-42d9-aee9-30ac4f33bde7)  
(Importante)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=e957a7cf-e5ca-454d-b199-ec8fe6a6a2bf)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=53fc3285-63c4-487f-ad9a-7e1673aeffc7)  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=2be85462-28ec-4184-a326-0459554b7213)  
(Importante)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=cb0e39f8-9730-4454-a0e3-479b610b1591)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=5201a0c5-8162-4809-b9d1-0e972b0f0066)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=04abea55-ea2f-423f-b410-5536ea184ea3)  
(Importante)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=7ebd99b4-da6b-4dff-9f89-6a86d275a3da)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-016**](http://technet.microsoft.com/security/bulletin/ms10-016)
</td>
<td style="border:1px solid black;">
[**MS10-018**](http://technet.microsoft.com/security/bulletin/ms10-018)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
[Movie Maker 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=ae2e9b75-1616-4fe3-91bb-e2e28252ff1c)<sup>[1]</sup>
(Importante)  

[Movie Maker 2.6](http://www.microsoft.com/downloads/details.aspx?familyid=ca2d1118-ca64-419d-86af-9396e61b90b0)<sup>[2]</sup>
(Importante)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=511aba0e-6f15-42cf-9c5d-b2f3e215b5a8)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=c9584689-5196-4840-927c-23c8038f3382)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Movie Maker 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=e27f353e-deb6-4d61-8808-c751d20a42a1)<sup>[1]</sup>
(Importante)  

[Movie Maker 2.6](http://www.microsoft.com/downloads/details.aspx?familyid=6a1f4126-97f2-4aee-bfe1-05bd13a0667b)<sup>[2]</sup>
(Importante)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=c8933a45-62a7-4c19-be30-02e3a461f081)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=50809cc3-6baa-41b4-ba0a-596a1dd846ed)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-016**](http://technet.microsoft.com/security/bulletin/ms10-016)
</td>
<td style="border:1px solid black;">
[**MS10-018**](http://technet.microsoft.com/security/bulletin/ms10-018)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=42f8c1f2-ee55-47af-b113-8d9f4bd40c8f)\*\*  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=c69a6dfe-66b1-4426-96a5-d64000296e76)\*\*  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=769043b5-df52-4446-9bd8-dc37d9fa00df)\*\*  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=e16c10d2-896d-48f3-bc76-5fa70881396a)\*\*  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=c1c2309d-22db-4dbf-ad95-3219847cd42d)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows 7
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-016**](http://technet.microsoft.com/security/bulletin/ms10-016)
</td>
<td style="border:1px solid black;">
[**MS10-018**](http://technet.microsoft.com/security/bulletin/ms10-018)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=c0145563-428e-47b6-b245-b59dce88ac0e)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas x64
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=6172dbec-6bfc-40bd-a0d4-67c39fb41b87)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows Server 2008 R2
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-016**](http://technet.microsoft.com/security/bulletin/ms10-016)
</td>
<td style="border:1px solid black;">
[**MS10-018**](http://technet.microsoft.com/security/bulletin/ms10-018)
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
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=8b7c664b-8612-458f-bd0a-cf28b67f8374)\*\*  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=82fa6f47-002f-4943-888c-2e852675e76e)  
(Moderada)
</td>
</tr>
</table>
 
**Nota para Windows Server 2008 y Windows Server 2008 R2**

**\*\*La instalación de Server Core no está afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de MSDN [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx) y [Server Core para Windows Server 2008 R2](http://msdn.microsoft.com/en-us/library/ee391631(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparación de las opciones de instalación Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**Notas para MS10-016**

<sup>[1]</sup>Estas versiones de Windows Movie Maker se suministran con los sistemas operativos indicados.

<sup>[2]</sup>Windows Movie Maker 2.6 es una descarga opcional que se puede instalar en los sistemas operativos indicados.

Vea también las demás categorías de esta sección, Ubicaciones de descarga y software afectado, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

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
Conjuntos de programas, sistemas y componentes de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-017**](http://technet.microsoft.com/security/bulletin/ms10-017)
</td>
<td style="border:1px solid black;">
[**MS10-016**](http://technet.microsoft.com/security/bulletin/ms10-016)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office XP
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2002 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=e0136f62-60ce-4ebd-8660-be81eba29ae8)  
(KB978471)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2003
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=7e42793e-747b-48da-968a-1ec29ea37151)  
(KB978474)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
2007 Microsoft Office System
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2007 Service Pack 1 y Microsoft Office Excel 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=03429f8a-8aab-4a59-97e4-7ce047f100a5)<sup>[1]</sup>
(KB978382)  
(Importante)
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
[**MS10-017**](http://technet.microsoft.com/security/bulletin/ms10-017)
</td>
<td style="border:1px solid black;">
[**MS10-016**](http://technet.microsoft.com/security/bulletin/ms10-016)
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
Ninguna
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2004 para Mac
</td>
<td style="border:1px solid black;">
[Microsoft Office 2004 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=ae5936f8-fe3f-4d23-a37c-d80f228e475e)  
(KB980837)  
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
[Microsoft Office 2008 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=e0ed1569-ab2f-407c-b728-4eddc463c385)  
(KB980839)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Convertidor de archivos con formatos XML abiertos para Mac
</td>
<td style="border:1px solid black;">
[Convertidor de archivos con formatos XML abiertos para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=4c5487d5-c912-4087-8c83-769e3fb78ea9)  
(KB980840)  
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
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-017**](http://technet.microsoft.com/security/bulletin/ms10-017)
</td>
<td style="border:1px solid black;">
[**MS10-016**](http://technet.microsoft.com/security/bulletin/ms10-016)
</td>
</tr>
<tr class="alternateRow">
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
<tr>
<td style="border:1px solid black;">
Microsoft Office Excel Viewer
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel Viewer Service Pack 1 y Microsoft Office Excel Viewer Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=010d0a4d-02a4-4142-963b-a38cd06cc897)  
(KB978383)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007
</td>
<td style="border:1px solid black;">
[Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 1 y Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=314f076e-8f9d-46c2-b666-86599a02bf15)  
(KB978380)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office SharePoint Server 2007 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Office SharePoint Server 2007 Service Pack 1 y Microsoft Office SharePoint Server 2007 Service Pack 2 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=94ddf6ef-3392-4d77-a02b-3bc0470721cd)<sup>[2]</sup>
(KB979439)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office SharePoint Server 2007 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Office SharePoint Server 2007 Service Pack 1 y Microsoft Office SharePoint Server 2007 Service Pack 2 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=06f6bffb-3fad-4fb5-878b-39550812e9b5)<sup>[2]</sup>
(KB979439)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Producer 2003
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Producer 2003](http://www.microsoft.com/downloads/details.aspx?familyid=1b3c76d5-fc75-4f99-94bc-784919468e73)<sup>[3]</sup>
(Importante)
</td>
</tr>
</table>
 
**Notas para MS10-017**

<sup>[1]</sup>Para Microsoft Office Excel 2007 Service Pack 1 y Microsoft Office Excel 2007 Service Pack 2, además del paquete de actualización de seguridad KB978382, los clientes también deben instalar la actualización de seguridad para [Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 1 y Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=314f076e-8f9d-46c2-b666-86599a02bf15) (KB978380) con el fin de protegerse de las vulnerabilidades descritas en este boletín.

<sup>[2]</sup>Esta actualización se aplica a los servidores que tienen instalados Servicios de Excel, como la configuración predeterminada de Microsoft Office SharePoint Server 2007 Enterprise y Microsoft Office SharePoint Server 2007 para sitios de Internet. Microsoft Office SharePoint Server 2007 Standard no incluye Servicios de Excel.

**Notas para MS10-016**

<sup>[3]</sup>Esta descarga actualiza la instalación de Microsoft Producer 2003 a la nueva versión, Microsoft Producer. Microsoft Producer sólo está disponible en inglés.

Vea también las demás categorías de esta sección, Ubicaciones de descarga y software afectado, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/default.aspx). [TechNet Security Center](http://technet.microsoft.com/es-es/security/default.aspx) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://go.microsoft.com/fwlink/?linkid=85102), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS07-036"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Nota** A partir del 1 de agosto de 2009, Microsoft dejó de ofrecer soporte técnico a Office Update y Office Update Inventory Tool. Para seguir obteniendo las actualizaciones más recientes para los productos de Microsoft, use [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747). Para obtener más información, vea [Acerca de Microsoft Office Update: Preguntas más frecuentes](http://office.microsoft.com/en-us/downloads/fx010402221033.aspx).

**Consejos para la detección y la implementación**

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747).

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://technet.microsoft.com/es-es/security/cc184924.aspx).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar de un modo rápido y confiable las actualizaciones críticas y de seguridad más recientes en sistemas operativos Microsoft Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://go.microsoft.com/fwlink/?linkid=50120).

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. La siguiente versión de SMS, System Center Configuration Manager 2007, ya está disponible; consulte también [System Center Configuration Manager 2007](http://technet.microsoft.com/en-us/library/bb735860.aspx). Para obtener más información acerca de cómo pueden utilizar los administradores SMS 2003 para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar Security Update Inventory Tool (SUIT) como ayuda para implementar las actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://go.microsoft.com/fwlink/?linkid=21158).

**Nota** SMS usa las herramientas Microsoft Baseline Security Analyzer para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet2.microsoft.com/windowsvista/en/library/4279e239-37a4-44aa-aec5-4e70fe39f9de1033.mspx?mfr=true) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Microsoft Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Microsoft Knowledge Base, artículo 894199](http://support.microsoft.com/kb/894199): Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones de meses anteriores para Windows Server Update Services](http://technet.microsoft.com/en-us/wsus/bb456965.aspx). Muestra todas las actualizaciones nuevas, revisadas y publicadas de nuevo para los productos de Microsoft que no sean Microsoft Windows.

#### Microsoft Active Protections Program (MAPP)

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumeradas en [Asociados de Microsoft Active Protections Program (MAPP)](http://www.microsoft.com/security/msrc/mapp/partners.mspx).

#### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de actualizaciones](http://go.microsoft.com/fwlink/?linkid=21168) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](http://support.microsoft.com/kb/913086).

**Comunidad de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [IT Pro Security Community](http://technet.microsoft.com/es-es/security/cc136632.aspx) (en inglés).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

-   Damián Frizza, de [Core Security Technologies](http://www.coresecurity.com/), por informar de un problema descrito en MS10-016
-   Nicolas Joly, de [VUPEN Vulnerability Research Team](http://www.vupen.com/), por informar de un problema descrito en MS10-017
-   Sean Larsson, de [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de cuatro problemas descritos en MS10-017
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS10-017
-   Damián Frizza, de [Core Security Technologies](http://www.coresecurity.com/), por informar de un problema descrito en MS10-017
-   [Secunia](http://secunia.com), por colaborar con nosotros en un problema descrito en MS10-018
-   Daiki Fukumori, de [Cyber Defense Institute Inc.](http://www.cyberdefense.jp/), por informar de un problema descrito en MS10-018
-   Alexander Kornbrust, de [Red Database Security](http://www.red-database-security.com/), por informar de un problema descrito en MS10-018
-   Ivan Fratric, de [iSIGHT Partners](http://www.isightpartners.com/) Global Vulnerability Partnership, por informar de un problema descrito en MS10-018
-   Wushi, de [team509](http://www.team509.com/), en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS10-018
-   Simon Zuckerbraun, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS10-018
-   Paul Stone, de [Context Information Security](http://www.contextis.co.uk/), por informar de un problema descrito en MS10-018
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS10-018
-   ADLab, de [VenusTech](http://www.venustech.com.cn/), por informar de dos problemas descritos en MS10-018

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Los clientes de Estados Unidos y Canadá pueden recibir soporte técnico del [soporte de seguridad](http://go.microsoft.com/fwlink/?linkid=21131) o en el teléfono 1-866-PCSAFETY. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de las opciones de asistencia disponibles, visite [Ayuda y soporte técnico de Microsoft](http://support.microsoft.com/).
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (9 de marzo de 2010): Publicación del resumen del boletín.
-   V2.0 (30 de marzo de 2010): Se ha agregado el boletín de seguridad de Microsoft MS10-018, Actualización acumulativa para Internet Explorer (980182). También se ha agregado un vínculo de webcast de boletín para este boletín de seguridad fuera de ciclo.
-   V3.0 (3 de mayo de 2010): Se ha anunciado la disponibilidad de la descarga de Microsoft Producer asociada a MS10-016.
-   V3.1 (11 de agosto de 2010): Se ha quitado Windows Movie Maker 2.6 como componente afectado en Windows 7 para MS10-016.

*Built at 2014-04-18T01:50:00Z-07:00*
