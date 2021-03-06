---
TOCTitle: 'MS09-SEP'
Title: Resumen del boletín de seguridad de Microsoft de septiembre 2009
ms:assetid: 'ms09-sep'
ms:contentKeyID: 61225407
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms09-sep(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de septiembre 2009
================================================================

Publicado: martes, 8 de septiembre de 2009 | Actualizado: martes, 10 de noviembre de 2009

**Versión:** 3.0

Este resumen del boletín enumera los boletines de seguridad publicados para septiembre de 2009.

Con la publicación de los boletines de septiembre de 2009, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 3 de septiembre de 2009. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 9 de septiembre de 2009, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de septiembre](http://msevents.microsoft.com/cui/webcasteventdetails.aspx?eventid=1032407486&eventcategory=4&culture=en-us&countrycode=us). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-045">MS09-045</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el motor de secuencias de comandos de JScript podría permitir la ejecución remota de código (971961)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en el motor de secuencias de comandos de JScript que podría permitir la ejecución remota de código si un usuario abre un archivo especialmente diseñado o visita un sitio web especialmente diseñado e invoca una secuencia de comandos con formato incorrecto. Si un usuario inicia sesión con derechos de usuario administrativos, un intruso que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-049">MS09-049</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el servicio de configuración automática de LAN inalámbrica podría permitir la ejecución remota de código (970710)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en el servicio de configuración automática de LAN inalámbrica. La vulnerabilidad podría permitir la ejecución remota de código si un cliente o un servidor con una interfaz de red inalámbrica recibe tramas inalámbricas especialmente diseñadas. Los sistemas sin una tarjeta inalámbrica no están expuestos a esta vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-047">MS09-047</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Windows Media Format podrían permitir la ejecución remota de código (973812)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Windows Media Format. Cualquier vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo multimedia especialmente diseñado. Si un usuario inicia sesión con derechos de usuario administrativos, un intruso que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-048">MS09-048</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en TCP/IP de Windows podrían permitir la ejecución remota de código (967723)</strong><br />
<br />
Esta actualización de seguridad resuelve varias vulnerabilidades de las que se ha informado de forma privada en el procesamiento del Protocolo de control de transmisión/Protocolo de Internet (TCP/IP). Las vulnerabilidades podrían permitir la ejecución remota de código si un atacante envía paquetes de TCP/IP especialmente diseñados a través de la red a un equipo con un servicio de escucha. Si se siguen las prácticas recomendadas relativas al uso de servidores de seguridad y se implementan las configuraciones de servidores de seguridad predeterminadas estándar, puede contribuirse a proteger una red de los ataques que se originen fuera del ámbito de la empresa. Se recomienda que los sistemas conectados a Internet tengan expuesta la cantidad mínima de puertos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-046">MS09-046</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el control ActiveX del componente de edición DHTML podría permitir la ejecución remota de código (956844)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en el control ActiveX del componente de edición DHMTL. Un atacante podría aprovechar esta vulnerabilidad mediante la creación de una página web especialmente diseñada. Si un usuario visita la página web, la vulnerabilidad podría permitir la ejecución remota de código. Un intruso que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario que ha iniciado sesión. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y de identificador de CVE.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de que se publique código funcional que aproveche la vulnerabilidad en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Debe revisar cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/en-us/security/cc998259.aspx).
  
| Identificador del boletín                                           | Título del boletín                                                                                                                      | Identificador CVE                                                                | Evaluación de índice de explotabilidad                                                                                                | Notas clave                                                                                                                                                   |  
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| [MS09-045](http://technet.microsoft.com/security/bulletin/ms09-045) | Una vulnerabilidad en el motor de secuencias de comandos de JScript podría permitir la ejecución remota de código (971961)              | [CVE-2009-1920](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1920) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                     |  
| [MS09-046](http://technet.microsoft.com/security/bulletin/ms09-046) | Una vulnerabilidad en el control ActiveX del componente de edición DHTML podría permitir la ejecución remota de código (956844)         | [CVE-2009-2519](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2519) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                     |  
| [MS09-047](http://technet.microsoft.com/security/bulletin/ms09-047) | Vulnerabilidades en Windows Media Format podrían permitir la ejecución remota de código (973812)                                        | [CVE-2009-2498](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2498) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                     |  
| [MS09-047](http://technet.microsoft.com/security/bulletin/ms09-047) | Vulnerabilidades en Windows Media Format podrían permitir la ejecución remota de código (973812)                                        | [CVE-2009-2499](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2499) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                     |  
| [MS09-048](http://technet.microsoft.com/security/bulletin/ms09-048) | Vulnerabilidades en TCP/IP de Windows podrían permitir la ejecución remota de código (967723)                                           | [CVE-2008-4609](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4609) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | Se trata de un tipo de denegación de servicio de consumo de memoria.                                                                                          |  
| [MS09-048](http://technet.microsoft.com/security/bulletin/ms09-048) | Vulnerabilidades en TCP/IP de Windows podrían permitir la ejecución remota de código (967723)                                           | [CVE-2009-1925](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1925) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | Es posible el código funcional que aproveche la vulnerabilidad pero no es probable que sea confiable. El resultado más probable es la denegación de servicio. |  
| [MS09-048](http://technet.microsoft.com/security/bulletin/ms09-048) | Vulnerabilidades en TCP/IP de Windows podrían permitir la ejecución remota de código (967723)                                           | [CVE-2009-1926](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1926) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | Se trata de un tipo de denegación de servicio de consumo de memoria.                                                                                          |  
| [MS09-049](http://technet.microsoft.com/security/bulletin/ms09-049) | Una vulnerabilidad en el servicio de configuración automática de LAN inalámbrica podría permitir la ejecución remota de código (970710) | [CVE-2009-1132](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1132) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | Las protecciones del montón dificultan que esta vulnerabilidad se aproveche de un modo confiable.                                                             |
  
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
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Microsoft Windows 2000  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-045**](http://technet.microsoft.com/security/bulletin/ms09-045)
</td>
<td style="border:1px solid black;">
[**MS09-049**](http://technet.microsoft.com/security/bulletin/ms09-049)
</td>
<td style="border:1px solid black;">
[**MS09-047**](http://technet.microsoft.com/security/bulletin/ms09-047)
</td>
<td style="border:1px solid black;">
[**MS09-048**](http://technet.microsoft.com/security/bulletin/ms09-048)
</td>
<td style="border:1px solid black;">
[**MS09-046**](http://technet.microsoft.com/security/bulletin/ms09-046)
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
Ninguna
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
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
Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
[JScript 5.1 y JScript 5.6](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=2bb3af8d-f36c-4497-9f48-fc59bcff2583)  
(KB971961)  
(Crítica)  

[JScript 5.7](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=b2773db5-b17d-4b98-b4e2-219b23854abd)  
(KB975542)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Módulo de tiempo de ejecución de Windows Media Format 9.0](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=02b9dc42-38c2-44b1-a77c-34854f4a86c4)  
(KB968816)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft Windows 2000 Service Pack 4<sup>[3]</sup>
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=6dd4b0f8-6b54-49a6-a6df-9420f9fd3333)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Windows XP
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-045**](http://technet.microsoft.com/security/bulletin/ms09-045)
</td>
<td style="border:1px solid black;">
[**MS09-049**](http://technet.microsoft.com/security/bulletin/ms09-049)
</td>
<td style="border:1px solid black;">
[**MS09-047**](http://technet.microsoft.com/security/bulletin/ms09-047)
</td>
<td style="border:1px solid black;">
[**MS09-048**](http://technet.microsoft.com/security/bulletin/ms09-048)
</td>
<td style="border:1px solid black;">
[**MS09-046**](http://technet.microsoft.com/security/bulletin/ms09-046)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Baja**](http://technet.microsoft.com/security/bulletin/rating)
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
[JScript 5.6 en Windows XP Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=0af373b2-2240-4079-a748-a38d1bc06f39)  
(KB971961)  
(Crítica)  

[JScript 5.7 en Windows XP Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=c933377d-e0bc-4334-bc75-029045d7a62a)<sup>[1]</sup>
(KB971961)  
(Crítica)  

[JScript 5.7 en Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=c933377d-e0bc-4334-bc75-029045d7a62a)  
(KB971961)  
(Crítica)  

[JScript 5.8](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=992602d8-d857-41cf-b7b1-527afdc1dc0f)<sup>[2]</sup>
(KB971961)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Módulo de tiempo de ejecución de Windows Media Format 9.0, módulo de tiempo de ejecución de Windows Media Format 9.5 y módulo de tiempo de ejecución de Windows Media Format 11](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=6ffc081e-f892-4818-acb9-6d79e15d473c)  
(KB968816)  
(Crítica)  
(Windows XP Service Pack 2 solamente)  

[Módulo de tiempo de ejecución de Windows Media Format 9.0, módulo de tiempo de ejecución de Windows Media Format 9.5 y módulo de tiempo de ejecución de Windows Media Format 11](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=31585f5a-9aaa-40da-b15a-11284b4b800c)  
(KB968816)  
(Crítica)  
(Windows XP Service Pack 3 solamente)
</td>
<td style="border:1px solid black;">
Windows XP Service Pack 2 y Windows XP Service Pack 3<sup>[3]</sup>
(Baja)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=8523d5be-88a2-4124-9b02-660f612e2a12)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[JScript 5.6](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=0d671004-da4e-4dbd-a066-861b53b0c59c)  
(KB971961)  
(Crítica)  

[JScript 5.7](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=9aae426d-ee9a-4736-b0a2-e0f8890a6895)<sup>[1]</sup>
(KB971961)  
(Crítica)  

[JScript 5.8](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=00bae02a-64eb-4b91-965f-da2dc987a2ff)<sup>[2]</sup>
(KB971961)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Módulo de tiempo de ejecución de Windows Media Format 9.5](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=3780d565-d027-4f54-8fc0-05f5c3c6ba1a)  
(KB968816)  
(Crítica)  

[Módulo de tiempo de ejecución de Windows Media Format 9.5 x64 Edition](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=ce515188-db3c-4694-85da-177c8f76b68c)  
(KB968816)  
(Crítica)  

[Módulo de tiempo de ejecución de Windows Media Format 11](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=9a465f92-3067-4a5a-9882-1fc2cf796c99)  
(KB968816)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2<sup>[3]</sup>
(Baja)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=dbc33f6b-61bf-409a-89b5-60002192e0e0)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-045**](http://go.microsoft.com/fwlink/?linkid=157304)
</td>
<td style="border:1px solid black;">
[**MS09-049**](http://technet.microsoft.com/security/bulletin/ms09-049)
</td>
<td style="border:1px solid black;">
[**MS09-047**](http://technet.microsoft.com/security/bulletin/ms09-047)
</td>
<td style="border:1px solid black;">
[**MS09-048**](http://technet.microsoft.com/security/bulletin/ms09-048)
</td>
<td style="border:1px solid black;">
[**MS09-046**](http://technet.microsoft.com/security/bulletin/ms09-046)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[JScript 5.6](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=6acc9d2d-b71f-4b5c-9aea-b217b6ae240b)  
(KB971961)  
(Crítica)  

[JScript 5.7](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=6af5d034-fd89-42e2-bc18-d44b7a6b0a85)<sup>[1]</sup>
(KB971961)  
(Crítica)  

[JScript 5.8](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=ecf9f7e2-3104-4de2-8b3d-99dcdcae6e62)<sup>[2]</sup>
(KB971961)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Módulo de tiempo de ejecución de Windows Media Format 9.5](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=4ab34e3d-34cb-4e35-a2da-b348ace8a8f7)  
(KB968816)  
(Crítica)  

[Servicios de Windows Media 9.1](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=61cd0581-c36e-4da6-ae95-41609adbe922)  
(KB972554)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=48d82036-2fde-4bb0-a60e-92eed83ddc3f)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=7478f73f-dd20-4cfa-a650-4c84f37ada2f)  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[JScript 5.6](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=d0de3ab1-73e9-4a09-841f-81ade41a8c81)  
(KB971961)  
(Crítica)  

[JScript 5.7](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=8f48bc05-ffac-4a21-8d21-dd20355cda8a)<sup>[1]</sup>
(KB971961)  
(Crítica)  

[JScript 5.8](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=643f9e2f-2e5b-48dd-b1a0-22ccb633ed18)<sup>[2]</sup>
(KB971961)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Módulo de tiempo de ejecución de Windows Media Format 9.5](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=8654ee33-6083-447f-ae5b-43ef8d8b613d)  
(KB968816)  
(Crítica)  

[Módulo de tiempo de ejecución de Windows Media Format 9.5 x64 Edition](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=ce515188-db3c-4694-85da-177c8f76b68c)  
(KB968816)  
(Crítica)  

[Servicios de Windows Media 9.1](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=67c46f26-e6df-4ba2-9c03-1590b31e454c)  
(KB972554)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=e0298ddf-026e-4137-8197-ed9d9b889825)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=88bf502d-1a7c-447a-ac4c-401e1698669b)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[JScript 5.6](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=e78cf021-54f5-4526-b5f0-f781aebf9d72)  
(KB971961)  
(Crítica)  

[JScript 5.7](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=fb1ca290-cea4-49c0-a37e-613a654bff3c)<sup>[1]</sup>
(KB971961)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=c948c4d8-5788-4c1a-9fb6-a969b06a888d)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=8d881ff8-f51f-4476-8cb6-2bebd5b2047f)  
(Moderada)
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-045**](http://technet.microsoft.com/security/bulletin/ms09-045)
</td>
<td style="border:1px solid black;">
[**MS09-049**](http://technet.microsoft.com/security/bulletin/ms09-049)
</td>
<td style="border:1px solid black;">
[**MS09-047**](http://technet.microsoft.com/security/bulletin/ms09-047)
</td>
<td style="border:1px solid black;">
[**MS09-048**](http://technet.microsoft.com/security/bulletin/ms09-048)
</td>
<td style="border:1px solid black;">
[**MS09-046**](http://technet.microsoft.com/security/bulletin/ms09-046)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
[JScript 5.7](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=bcb12e57-f5d6-4b4e-88ab-13c28137f11a)  
(KB971961)  
(Crítica)  

[JScript 5.8](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=80e7390f-df39-4d99-b2e1-01c7f6a951bb)<sup>[2]</sup>
(KB971961)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=e9fe967f-d78d-43c2-bbcc-5098bd20267e)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Módulo de tiempo de ejecución de Windows Media Format 11 y Microsoft Media Foundation](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=d2bdefcc-f6b9-47c3-a55d-a4f33f967828)  
(KB968816)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=7d72f845-9feb-4685-a669-f9d6ab54f9ed)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[JScript 5.7](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=8b1b76d5-a6b0-4c2f-8768-e55e82c2c118)  
(KB971961)  
(Crítica)  

[JScript 5.8](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=24457cdd-1973-40c9-9c2d-c1a75fdfa7fa)<sup>[2]</sup>
(KB971961)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=f93470bd-2e6d-4340-88c6-bb212baf750a)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Módulo de tiempo de ejecución de Windows Media Format 11 y Microsoft Media Foundation](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=97f00b25-fb8f-4300-80c0-c63179f32182)  
(KB968816)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=b2930ff1-5f0a-4a5d-bf2a-9fb76dd8da63)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-045**](http://technet.microsoft.com/security/bulletin/ms09-045)
</td>
<td style="border:1px solid black;">
[**MS09-049**](http://technet.microsoft.com/security/bulletin/ms09-049)
</td>
<td style="border:1px solid black;">
[**MS09-047**](http://technet.microsoft.com/security/bulletin/ms09-047)
</td>
<td style="border:1px solid black;">
[**MS09-048**](http://technet.microsoft.com/security/bulletin/ms09-048)
</td>
<td style="border:1px solid black;">
[**MS09-046**](http://technet.microsoft.com/security/bulletin/ms09-046)
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
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[JScript 5.7](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=df88e6e5-78d3-4fa6-858d-b935d812cada)\*  
(KB971961)  
(Crítica)  

[JScript 5.8](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=e7b07be6-a4f8-4847-9c55-9b3d2965fa77)\* <sup>[2]</sup>
(KB971961)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=ac3f6800-bc3e-4b35-a482-54e1a2da1ab5)\*\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Módulo de tiempo de ejecución de Windows Media Format 11 y Microsoft Media Foundation](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=9c111bff-aff6-4ff7-81f6-e736cfcbe3ed)\*\*  
(KB968816)  
(Crítica)  

[Servicios de Windows Media 2008](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=2801f69b-37d0-4d0f-9632-31382b824d36)\*  
(KB972554)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=35c1d5a9-a953-4fc6-90c0-d2358c7b89e6)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[JScript 5.7](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=f584f8ca-f6b1-4285-a44c-3df5e51e75de)\*  
(KB971961)  
(Crítica)  

[JScript 5.8](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=9eddbb89-4178-49c2-836a-2d292fe50936)\* <sup>[2]</sup>
(KB971961)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=7d1b9b4f-bf35-44aa-a660-afb2ef2c9e30)\*\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Módulo de tiempo de ejecución de Windows Media Format 11 y Microsoft Media Foundation](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=59615c8b-a07f-4326-836d-f17b2fcc4695)\*\*  
(KB968816)  
(Crítica)  

[Servicios de Windows Media 2008](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=7fad3793-174f-46db-9d0a-873a0ea8be65)\*  
(KB972554)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=6e46822e-f79d-492d-ad01-ee680ad324f5)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[JScript 5.7](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=b84fca1d-914d-45af-a48c-d9bc5d20c6b7)  
(KB971961)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?displaylang=es&amp;familyid=2ac76ee2-b1b6-4300-9cba-af33d9dd54eb)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
**Notas para Windows Server 2008**

**\*Instalación de Server Core de Windows Server 2008 afectada.** Para ediciones compatibles de Windows Server 2008, esta actualización se aplica con la misma clasificación de gravedad, independientemente de si Windows Server 2008 se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**\*\*Instalación de Windows Server 2008 Server Core no afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 si Windows Server 2008 se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**Notas para MS09-045**

<sup>[1]</sup>En sistemas con Internet Explorer 7 instalado

<sup>[2]</sup>En sistemas con Internet Explorer 8 instalado

**Nota para MS09-048**

<sup>[3]</sup> Ninguna actualización disponible. Para obtener más información, consulte la entrada de **Preguntas más frecuentes (P+F) relacionadas con esta actualización de seguridad** en [MS09-048](http://technet.microsoft.com/security/bulletin/ms09-048).

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/default.aspx). [TechNet Security Center](http://go.microsoft.com/fwlink/?linkid=21171) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://go.microsoft.com/fwlink/?linkid=85102), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://www.update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=es-es) y [Windows Update](http://www.update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=es-es). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS07-036"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Nota** A partir del 1 de agosto de 2009, Microsoft dejará de ofrecer soporte técnico a Office Update y Office Update Inventory Tool. Para seguir obteniendo las actualizaciones más recientes para los productos de Microsoft, use [Microsoft Update](http://www.update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=es-es). Para obtener más información, vea [Acerca de Microsoft Office Update: Preguntas más frecuentes](http://office.microsoft.com/en-us/downloads/fx010402221033.aspx).

**Consejos para la detección y la implementación**

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747).

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://go.microsoft.com/fwlink/?linkid=21134).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar con rapidez y fiabilidad las actualizaciones críticas y de seguridad más recientes en sistemas operativos Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://go.microsoft.com/fwlink/?linkid=50120).

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. La siguiente versión de SMS, System Center Configuration Manager 2007, ya está disponible; consulte también [System Center Configuration Manager 2007](http://technet.microsoft.com/en-us/library/bb735860.aspx). Para obtener más información acerca de cómo pueden utilizar los administradores SMS 2003 para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar Security Update Inventory Tool (SUIT) como ayuda para implementar las actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://go.microsoft.com/fwlink/?linkid=21158).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=33387) y en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet2.microsoft.com/windowsvista/en/library/4279e239-37a4-44aa-aec5-4e70fe39f9de1033.mspx?mfr=true) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Microsoft Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Artículo 894199 de Microsoft Knowledge Base](http://support.microsoft.com/kb/894199): Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones de meses anteriores para Windows Server Update Services](http://technet.microsoft.com/en-us/wsus/bb456965.aspx). Muestra todas las actualizaciones nuevas, revisadas y publicadas de nuevo para los productos de Microsoft que no sean Microsoft Windows.

#### Microsoft Active Protections Program (MAPP)

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumeradas en [Asociados de Microsoft Active Protections Program (MAPP)](http://www.microsoft.com/security/msrc/mapp/partners.mspx).

#### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de actualizaciones](http://go.microsoft.com/fwlink/?linkid=21168) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://www.update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=es-es).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](http://support.microsoft.com/kb/913086).

**Comunidad de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [IT Pro Security Community](http://go.microsoft.com/fwlink/?linkid=21164) (en inglés).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

-   Ling y Wushi, de [Team509](http://www.team509.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de Tipping Point, por informar de un problema descrito en MS09-045
-   Tavis Ormandy, de [Google Inc.](http://www.google.com/), por informar de un problema descrito en MS09-046
-   Peter Winter-Smith, de [NGS Software](http://www.ngssoftware.com/), por informar de un problema descrito en MS09-047
-   Hiroshi Noguchi, del club de admiradores de Alice Carroll, por informar de un problema descrito en MS09-047
-   Jack C. Louis, de [Outpost24](http://www.outpost24.com/), por informar de un problema descrito en MS09-048
-   Fabian Yamaguchi, de [Recurity Labs GmbH](http://www.recurity-labs.com/), por informar de un problema descrito en MS09-048

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Los clientes de Estados Unidos y Canadá pueden recibir soporte técnico del [soporte de seguridad](http://go.microsoft.com/fwlink/?linkid=21131) o en el teléfono 1-866-PCSAFETY. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de las opciones de asistencia disponibles, visite [Ayuda y soporte técnico de Microsoft](http://support.microsoft.com/).
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (8 de septiembre de 2009): Publicación del resumen del boletín.
-   V2.0 (9 de septiembre de 2009): Se han agregado Windows XP Service Pack 2, Windows XP Service Pack 3 y Windows XP Professional x64 Edition Service Pack 2 a la tabla Software afectado para MS09-048. No obstante, no hay disponible ninguna actualización para estas plataformas. Consulte la entrada de **Preguntas más frecuentes (P+F) relacionadas con esta actualización de seguridad** en MS09-048. No hubo cambios en las actualizaciones de seguridad de este boletín.
-   V3.0 (10 de noviembre de 2009): Se ha agregado JScript 5.7 en Microsoft Windows 2000 Service Pack 4 a la tabla Software afectado para MS09-045.

*Built at 2014-04-18T01:50:00Z-07:00*
