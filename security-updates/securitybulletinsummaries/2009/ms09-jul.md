---
TOCTitle: 'MS09-JUL'
Title: Resumen del boletín de seguridad de Microsoft de julio 2009
ms:assetid: 'ms09-jul'
ms:contentKeyID: 61225401
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms09-jul(v=Security.10)'
--- 


Resumen del boletín de seguridad de Microsoft de julio 2009
===========================================================

Publicado: martes, 14 de julio de 2009 | Actualizado: martes, 9 de marzo de 2010

**Versión:** 8.0

Este resumen del boletín enumera los boletines de seguridad publicados para julio de 2009.

Con el lanzamiento de los boletines para julio de 2009, este resumen reemplaza a la notificación de avance de boletines publicada originalmente el 9 de julio de 2009, y al boletín de notificaciones fuera de ciclo publicado originalmente el 24 de julio de 2009. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar una conferencia en línea para atender las consultas de los clientes sobre estos boletines el 15 de julio de 2009, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). Esta conferencia en línea está ahora disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

Para los boletines de seguridad fuera de ciclo agregados a la versión 2.0 de este resumen de boletín, MS09-034 y MS09-035, Microsoft hospeda dos conferencias en línea para atender las preguntas de los clientes acerca de estos boletines el 28 de julio de 2009, a la 1:00 p.m. Hora del Pacífico (EE.UU. y Canadá) y a las 4:00 p.m. Hora del Pacífico (EE.UU. y Canadá). Inscríbase ahora a la [conferencia en línea del 28 de julio a la 1:00 p.m.](http://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032422339&culture=en-us) y a la [conferencia en línea del 28 de julio a las 4:00 p.m](http://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032422341&culture=en-us). Posteriormente, estos webcasts estarán disponibles a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-029">MS09-029</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en el motor de fuentes OpenType incrustadas podrían permitir la ejecución remota de código (961371)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en el componente de Microsoft Windows Motor de fuentes OpenType incrustadas (EOT). Las vulnerabilidades podrían permitir la ejecución remota de código. Un atacante que aprovechara cualquiera de estas vulnerabilidades podría lograr el control total de un sistema afectado de forma remota. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-028">MS09-028</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft DirectShow podrían permitir la ejecución remota de código (971633)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y dos vulnerabilidades de las que se ha informado de forma privada en Microsoft DirectShow. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario abre un archivo multimedia QuickTime especialmente diseñado. Un intruso que aprovechara cualquiera de estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario local. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-032">MS09-032</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa de bits de interrupción de ActiveX (973346)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada y que se está aprovechando actualmente. La vulnerabilidad del control ActiveX Video de Microsoft podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada con Internet Explorer, con lo que se ejecuta el control ActiveX. Este control ActiveX no se diseñó para ejecutarse en Internet Explorer. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-034">MS09-034</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (972260)</strong><br />
<br />
Se publica esta actualización de seguridad fuera de ciclo junto con el boletín de seguridad de Microsoft MS09-035, que describe las vulnerabilidades en aquellos componentes y controles que se han desarrollado utilizando versiones vulnerables de Microsoft Active Template Library (ATL). Como medida de defensa en profundidad, esta actualización de seguridad para Internet Explorer ayuda a mitigar vectores de ataque conocidos dentro de Internet Explorer para aquellos componentes y controles que se han desarrollado con versiones vulnerables de ATL como se describe en el documento informativo sobre seguridad de Microsoft (973882) y el boletín de seguridad Microsoft MS09-035.<br />
<br />
Esta actualización de seguridad también resuelve tres vulnerabilidades informadas de forma privada en Internet Explorer. Estas vulnerabilidades podrían permitir la ejecución de código remoto si el usuario ve una página web especialmente preparada utilizando Internet Explorer. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, Internet Explorer</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-033">MS09-033</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Virtual PC y Virtual Server podría permitir la elevación de privilegios (969856)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Virtual PC y Microsoft Virtual Server. Un atacante que consiga aprovechar esta vulnerabilidad podría ejecutar código arbitrario y tomar el control completo de un sistema operativo invitado afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Virtual PC, Virtual Server</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-031">MS09-031</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft ISA Server 2006 podría provocar la elevación de privilegios (970953)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Internet Security and Acceleration (ISA) Server 2006. La vulnerabilidad podría permitir la elevación de privilegios si un atacante suplanta una cuenta de usuario administrador para un servidor ISA configurado para la autenticación de contraseña Radius de un solo uso (OTP) y la delegación de autenticación con la delegación restringida de Kerberos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft ISA Server</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-030">MS09-030</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Office Publisher podría permitir la ejecución remota de código (969516)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Office Publisher que podría permitir la ejecución remota de código si un usuario abre un archivo de Publisher especialmente diseñado. Un atacante que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-035">MS09-035</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Visual Studio Active Template Library podrían permitir la ejecución remota de código (969706)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad informada de manera privada en las versiones públicas de Microsoft Active Template Library (ATL) incluidas con Visual Studio. Esta actualización de seguridad se destina especialmente a desarrolladores de componentes y controles. Los desarrolladores que construyen y redistribuyen componentes y controles a través de ATL deberían instalar la actualización que se ofrece en este boletín y seguir los consejos para crear y distribuir a sus clientes, componentes y controles que no son se ven afectados por las vulnerabilidades que se describen en este boletín de seguridad.<br />
<br />
Este boletín de seguridad trata vulnerabilidades que podrían permitir la ejecución remota de código si un usuario cargó un componente o control con versiones vulnerables de ATL.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Moderada</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Visual Studio</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y de identificador de CVE.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de que se publique código funcional que aproveche la vulnerabilidad en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Debe revisar cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/en-us/security/cc998259.aspx).
  
| Identificador del boletín                                           | Título del boletín                                                                                                   | Identificador CVE                                                                | Evaluación de índice de explotabilidad                                                                                                | Notas clave                                                                                              |  
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|  
| [MS09-028](http://technet.microsoft.com/security/bulletin/ms09-028) | Vulnerabilidades en Microsoft DirectShow podrían permitir la ejecución remota de código (971633)                     | [CVE-2009-1537](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1537) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | **Esta vulnerabilidad se está aprovechando actualmente en el ecosistema de Internet.**                   |  
| [MS09-028](http://technet.microsoft.com/security/bulletin/ms09-028) | Vulnerabilidades en Microsoft DirectShow podrían permitir la ejecución remota de código (971633)                     | [CVE-2009-1538](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1538) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                |  
| [MS09-028](http://technet.microsoft.com/security/bulletin/ms09-028) | Vulnerabilidades en Microsoft DirectShow podrían permitir la ejecución remota de código (971633)                     | [CVE-2009-1539](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1539) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                |  
| [MS09-029](http://technet.microsoft.com/security/bulletin/ms09-028) | Vulnerabilidades en el motor de fuentes OpenType incrustadas podrían permitir la ejecución remota de código (961371) | [CVE-2009-0231](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0231) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                |  
| [MS09-029](http://technet.microsoft.com/security/bulletin/ms09-028) | Vulnerabilidades en el motor de fuentes OpenType incrustadas podrían permitir la ejecución remota de código (961371) | [CVE-2009-0232](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0232) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                |  
| [MS09-030](http://technet.microsoft.com/security/bulletin/ms09-030) | Una vulnerabilidad en Microsoft Office Publisher podría permitir la ejecución remota de código (969516)              | [CVE-2009-0566](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0566) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                |  
| [MS09-031](http://technet.microsoft.com/security/bulletin/ms09-031) | Una vulnerabilidad en Microsoft ISA Server 2006 podría provocar la elevación de privilegios (970953)                 | [CVE-2009-1135](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1135) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                |  
| [MS09-032](http://technet.microsoft.com/security/bulletin/ms09-032) | Actualización de seguridad acumulativa de bits de interrupción de ActiveX (973346)                                   | [CVE-2008-0015](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-0015) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | **Esta vulnerabilidad se está aprovechando actualmente en el ecosistema de Internet.**                   |  
| [MS09-033](http://technet.microsoft.com/security/bulletin/ms09-033) | Una vulnerabilidad en Virtual PC y Virtual Server podría permitir la elevación de privilegios (969856)               | [CVE-2009-1542](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1542) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | Es posible la ejecución de código funcional que aproveche la vulnerabilidad con resultados incoherentes. |  
| [MS09-034](http://technet.microsoft.com/security/bulletin/ms09-034) | Actualización de seguridad acumulativa de Internet Explorer (972260)                                                 | [CVE-2009-1917](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1917) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | Ejecución de código funcional es simple y confiable.                                                     |  
| [MS09-034](http://technet.microsoft.com/security/bulletin/ms09-034) | Actualización de seguridad acumulativa de Internet Explorer (972260)                                                 | [CVE-2009-1918](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1918) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | Es posible la ejecución de código funcional que aproveche la vulnerabilidad con resultados incoherentes. |  
| [MS09-034](http://technet.microsoft.com/security/bulletin/ms09-034) | Actualización de seguridad acumulativa de Internet Explorer (972260)                                                 | [CVE-2009-1919](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1919) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | Es posible la ejecución de código funcional que aproveche la vulnerabilidad con resultados incoherentes. |  
| [MS09-035](http://technet.microsoft.com/security/bulletin/ms09-035) | Vulnerabilidades en Visual Studio Active Template Library podrían permitir la ejecución remota de código (969706)    | [CVE-2009-0901](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0901) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | Ejecución de código funcional es simple y confiable.                                                     |  
| [MS09-035](http://technet.microsoft.com/security/bulletin/ms09-035) | Vulnerabilidades en Visual Studio Active Template Library podrían permitir la ejecución remota de código (969706)    | [CVE-2009-2493](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2493) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | Ejecución de código funcional es simple y confiable.                                                     |  
| [MS09-035](http://technet.microsoft.com/security/bulletin/ms09-035) | Vulnerabilidades en Visual Studio Active Template Library podrían permitir la ejecución remota de código (969706)    | [CVE-2009-2495](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2495) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | Un error de divulgación de información, sin amenaza de ejecución de código.                              |
  
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
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Microsoft Windows 2000  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-029**](http://technet.microsoft.com/security/bulletin/ms09-029)
</td>
<td style="border:1px solid black;">
[**MS09-028**](http://technet.microsoft.com/security/bulletin/ms09-028)
</td>
<td style="border:1px solid black;">
[**MS09-032**](http://technet.microsoft.com/security/bulletin/ms09-032)
</td>
<td style="border:1px solid black;">
[**MS09-034**](http://technet.microsoft.com/security/bulletin/ms09-034)
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
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=1efbbd95-cd72-43df-b1ce-7e2b0c0cb9e2)  
(Crítica)
</td>
<td style="border:1px solid black;">
[DirectX 7.0](http://www.microsoft.com/downloads/details.aspx?familyid=e3e54348-6548-4162-b4c0-9910ec6e18b3)  
(Crítica)  
[DirectX 8.1](http://www.microsoft.com/downloads/details.aspx?familyid=ce297c3e-8122-4276-a9c2-d1a404f8028d)\*\*\*  
(Crítica)  
[DirectX 9.0](http://www.microsoft.com/downloads/details.aspx?familyid=862db2ad-3c1f-4a26-af70-d8c4f5a69dda)\*\*\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=89d941f0-3f71-46e3-8096-716561396b72)  
(Sin clasificación de gravedad\*\*)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 5.01 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=50ffc8f4-7ab7-4e64-9965-5767db5f53cd)  
(Crítica)  
[Microsoft Internet Explorer 6 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=93bd1baa-e2fb-4e8c-9dd7-738efef32282)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows XP
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-029**](http://technet.microsoft.com/security/bulletin/ms09-029)
</td>
<td style="border:1px solid black;">
[**MS09-028**](http://technet.microsoft.com/security/bulletin/ms09-028)
</td>
<td style="border:1px solid black;">
[**MS09-032**](http://technet.microsoft.com/security/bulletin/ms09-032)
</td>
<td style="border:1px solid black;">
[**MS09-034**](http://technet.microsoft.com/security/bulletin/ms09-034)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
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
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=6914167b-6961-480c-a4d4-808cd58a035b)  
(Crítica)
</td>
<td style="border:1px solid black;">
[DirectX 9.0](http://www.microsoft.com/downloads/details.aspx?familyid=09d585cb-481d-4767-875e-9c6ebe456b80)\*\*\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=24701af8-b87e-4e85-9463-f50755a1b6ad)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=22bed634-5227-4a22-8df5-801f3e2e232a)  
(Crítica)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=c874c8f8-0449-42b1-8d8b-901040069568)  
(Crítica)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=0acc8aaa-0ae1-412a-9f2b-dc7c707cae00)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3b8b019e-e6d8-4ce2-8f1f-3a6399b252d1)  
(Crítica)
</td>
<td style="border:1px solid black;">
[DirectX 9.0](http://www.microsoft.com/downloads/details.aspx?familyid=f8cd4803-82da-467c-8cb1-520f5a6021d4)\*\*\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2cbf3699-7f79-4006-99e9-0a4c0d394c48)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=35ab0c5e-df3d-4873-8139-d1d98b3ac350)  
(Crítica)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=113cc76a-c434-42ff-b594-4834989ad5ba)  
(Crítica)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=29c8d9e6-2cb8-42b6-b0a6-2510fdb49eab)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-029**](http://technet.microsoft.com/security/bulletin/ms09-029)
</td>
<td style="border:1px solid black;">
[**MS09-028**](http://technet.microsoft.com/security/bulletin/ms09-028)
</td>
<td style="border:1px solid black;">
[**MS09-032**](http://technet.microsoft.com/security/bulletin/ms09-032)
</td>
<td style="border:1px solid black;">
[**MS09-034**](http://technet.microsoft.com/security/bulletin/ms09-034)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
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
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=018ef53d-f78e-4084-940d-7c86bf59d83c)  
(Crítica)
</td>
<td style="border:1px solid black;">
[DirectX 9.0](http://www.microsoft.com/downloads/details.aspx?familyid=571d57c5-1ef8-4dc4-a1e5-2211a805f0cc)\*\*\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b0a458d6-c34c-41c7-964a-c130cfcb0d01)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=44852619-58ad-48f2-bc55-e8e1c72b1ba9)  
(Moderada)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=f4112c25-9e6f-473a-bdbc-3df6dd66e6af)  
(Moderada)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=f4ae65a7-142f-4953-a542-315dac2ac606)  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7f5fc902-f5d8-4a87-a73f-68632f9a0935)  
(Crítica)
</td>
<td style="border:1px solid black;">
[DirectX 9.0](http://www.microsoft.com/downloads/details.aspx?familyid=1779cbc0-0c29-4fac-a3a6-8b335ffcb98e)\*\*\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8b7a7bb0-80ef-4f25-bc70-3d0ac06007c5)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=bd7f36c6-c5c5-4f19-ab59-39f1aaba7fe2)  
(Moderada)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=a594ee0d-ec8f-47df-9125-89d0bbf2115d)  
(Moderada)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=3bc0e17b-898b-4f29-aa29-607527e1c1cd)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=7df0fce2-543c-4e82-85e6-012bfc8bf130)  
(Crítica)
</td>
<td style="border:1px solid black;">
[DirectX 9.0](http://www.microsoft.com/downloads/details.aspx?familyid=48282a89-f849-405a-a31e-2676f45b5042)\*\*\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=7be36edf-02af-402f-983a-f9ca8128b6b5)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=cdb70acf-77c3-40a4-b6a3-0fbc0fc0d7fc)  
(Moderada)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=adb6bad2-9931-4ede-856e-bb43bb0f6071)  
(Moderada)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-029**](http://technet.microsoft.com/security/bulletin/ms09-029)
</td>
<td style="border:1px solid black;">
[**MS09-028**](http://technet.microsoft.com/security/bulletin/ms09-028)
</td>
<td style="border:1px solid black;">
[**MS09-032**](http://technet.microsoft.com/security/bulletin/ms09-032)
</td>
<td style="border:1px solid black;">
[**MS09-034**](http://technet.microsoft.com/security/bulletin/ms09-034)
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
Ninguna
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
[Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c67d85c4-25c5-4821-8db9-91764888f893)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6c90240e-c201-4dad-9835-ea71e3527b45)  
(Sin clasificación de gravedad\*\*)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=d3be9a13-1a5b-4b74-9649-449df923f573)  
(Crítica)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=b05a19f7-7412-4c2b-ad11-34396e54ca43)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3f8ae651-59f7-48e1-9e8c-8e07c6806964)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d2084e8d-212b-4c39-9163-a71ec6d1b1c7)  
(Sin clasificación de gravedad\*\*)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=2b23cd74-6cf1-413b-82a7-b602347e3ce6)  
(Crítica)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=900e9a05-2f71-42de-b603-47e4ac061bcb)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-029**](http://technet.microsoft.com/security/bulletin/ms09-029)
</td>
<td style="border:1px solid black;">
[**MS09-028**](http://technet.microsoft.com/security/bulletin/ms09-028)
</td>
<td style="border:1px solid black;">
[**MS09-032**](http://technet.microsoft.com/security/bulletin/ms09-032)
</td>
<td style="border:1px solid black;">
[**MS09-034**](http://technet.microsoft.com/security/bulletin/ms09-034)
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
Ninguna
</td>
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=91f6ee68-0e39-4ec3-b4cd-45f05404e2fb)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=0194f994-5821-4fb9-b9e1-ed6af248c995)\*  
(Sin clasificación de gravedad\*\*)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=92e3af41-71b0-4a28-afc7-123733180ead)\*  
(Moderada)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=30f99bda-9107-4969-90af-2a30e12acdae)\*  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5cdc3014-97b3-47b5-a6b7-cd0e12ec60e4)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4127b125-fdaa-489a-a80c-14b5647ac7e0)\*  
(Sin clasificación de gravedad\*\*)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=1958ec40-3b7b-43a9-9fdc-742735dcf516)\*  
(Moderada)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=acd3667b-6676-4010-b23b-e8372dd55f93)\*  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=03330a14-9cfa-4146-a3d3-4b7a76975d2d)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4082c776-318c-4e0c-83fc-2f3f472c039a)  
(Sin clasificación de gravedad\*\*)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=470387ac-6d75-4b7e-8ca5-376b67a8bd4d)  
(Moderada)
</td>
</tr>
</table>
 
**Nota para Windows Server 2008**

**\*Instalación principal de servidor de Windows Server 2008 no afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 si Windows Server 2008 se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**Nota para MS09-032**

\*\*Las clasificaciones de gravedad no se aplican a esta actualización porque la vulnerabilidad tratada en este boletín no afecta a este software. No obstante, como medida defensiva para protegerse de nuevos posibles ataques identificados en el futuro, Microsoft recomienda que los usuarios de este software apliquen esta actualización de seguridad.

**Notas para MS09-028**

\*\*\*La actualización para DirectX 8.1 también se aplica a DirectX 8.1b.

\*\*\*\*La actualización para DirectX 9.0 también se aplica a DirectX 9.0a, DirectX 9.0b y DirectX 9.0c.

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
[**MS09-030**](http://technet.microsoft.com/security/bulletin/ms09-030)
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
2007 Microsoft Office System Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft Office Publisher 2007 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d4b0665d-5744-49c7-a3c0-f231fd08d3b8)  
(KB969693)  
(Importante)
</td>
</tr>
</table>
 

#### Herramientas y software para desarrolladores de Microsoft

 
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
Microsoft Visual Studio
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-035**](http://technet.microsoft.com/security/bulletin/ms09-035)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Visual Studio .NET 2003
</td>
<td style="border:1px solid black;">
[Microsoft Visual Studio .NET 2003 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=63ce454e-f69c-44e3-89fb-eb23c2e2154e)  
(KB971089)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Visual Studio 2005
</td>
<td style="border:1px solid black;">
[Microsoft Visual Studio 2005 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7c8729dc-06a2-4538-a90d-ff9464dc0197)  
(KB971090)  
(Moderada)  
[Microsoft Visual Studio 2005 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=9d7ee45b-9892-41b5-ac08-5fde9cde1b42)\*  
(KB973673)  
(Moderada)  
[Microsoft Visual Studio 2005 Service Pack 1 64-bit Hosted Visual C++ Tools](http://www.microsoft.com/downloads/details.aspx?familyid=43f96f2a-69c6-4c5e-b72c-0edfa35f4fc2)  
(KB973830)  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Embedded CE 6.0
</td>
<td style="border:1px solid black;">
[Windows Embedded CE 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=99d114f8-4d95-4075-a0f1-45f498f0ade8)\*\*  
(KB974616)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Visual Studio 2008
</td>
<td style="border:1px solid black;">
[Microsoft Visual Studio 2008](http://www.microsoft.com/downloads/details.aspx?familyid=8f9da646-94dd-469d-baea-a4306270462c)  
(KB971091)  
(Moderada)  
[Microsoft Visual Studio 2008](http://www.microsoft.com/downloads/details.aspx?familyid=e3bb6602-b7f4-4614-9999-77f5c6f66ccd)\*  
(KB973674)  
(Moderada)  
[Microsoft Visual Studio 2008 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=294de390-3c94-49fb-a014-9a38580e64cb)  
(KB971092)  
(Moderada)  
[Microsoft Visual Studio 2008 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=75fbf397-5140-4961-92a9-78a88ba7228f)\*  
(KB973675)  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Visual C++ 2005
</td>
<td style="border:1px solid black;">
[Paquete redistribuible de Microsoft Visual C++ 2005 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=766a6af7-ec73-40ff-b072-9112bab119c2)  
(KB973544)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Visual C++ 2008
</td>
<td style="border:1px solid black;">
[Paquete redistribuible de Microsoft Visual C++ 2008](http://www.microsoft.com/downloads/details.aspx?familyid=8b29655e-9da4-4b6b-9ac5-687ca0770f93)  
(KB973551)  
(Moderada)  
[Paquete redistribuible de Microsoft Visual C++ 2008 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=2051a0c1-c9b5-4b0a-a8f5-770a549fd78c)  
(KB973552)  
(Moderada)
</td>
</tr>
</table>
 
**Notas para MS09-035**

\*Para aplicaciones móviles que usen ATL para dispositivos inteligentes

\*\*Instala la actualización mensual de Windows Embedded CE 6.0 (diciembre de 2009). Este paquete de actualización sólo está disponible en el Centro de descarga de Microsoft.

#### Software de servidor y seguridad de Microsoft

 
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
Microsoft Internet Security and Acceleration Server
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-031**](http://technet.microsoft.com/security/bulletin/ms09-031)
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
Microsoft Internet Security and Acceleration Server 2006
</td>
<td style="border:1px solid black;">
[Microsoft Internet Security and Acceleration Server 2006](http://www.microsoft.com/downloads/details.aspx?familyid=c4e9b1dd-526d-407b-bc23-ebc2738b1b19)  
(KB970811)  
(Importante)  
[Actualización de compatibilidad de Microsoft Internet Security and Acceleration Server 2006](http://www.microsoft.com/downloads/details.aspx?familyid=e8ccd770-a925-411c-b994-78e4cf5c3476)  
(KB970811)  
(Importante)  
[Microsoft Internet Security and Acceleration Server 2006 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=e536cfed-c1af-4868-b2ac-79178d6355a5)  
(KB971143)  
(Importante)
</td>
</tr>
</table>
 

#### Software de virtualización de Microsoft

 
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
Microsoft Virtual PC
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-033**](http://technet.microsoft.com/security/bulletin/ms09-033)
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
Microsoft Virtual PC 2004
</td>
<td style="border:1px solid black;">
[Microsoft Virtual PC 2004 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=56a160e1-59b5-45bc-aecf-dfe614a7efad)  
(KB969856)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Virtual PC 2007
</td>
<td style="border:1px solid black;">
[Microsoft Virtual PC 2007](http://www.microsoft.com/downloads/details.aspx?familyid=5318c1fa-daf1-4028-832b-eaec9906a46a)  
(KB969856)  
(Importante)  
[Microsoft Virtual PC 2007 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=88de1513-8d35-410f-8896-fe668f885ca0)  
(KB969856)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Virtual PC 2007 x64 Edition
</td>
<td style="border:1px solid black;">
[Microsoft Virtual PC 2007 x64 Edition](http://www.microsoft.com/downloads/details.aspx?familyid=5318c1fa-daf1-4028-832b-eaec9906a46a)  
(KB969856)  
(Importante)  
[Microsoft Virtual PC 2007 x64 Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=88de1513-8d35-410f-8896-fe668f885ca0)  
(KB969856)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Virtual Server
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-033**](http://technet.microsoft.com/security/bulletin/ms09-033)
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
Microsoft Virtual Server 2005
</td>
<td style="border:1px solid black;">
[Microsoft Virtual Server 2005](http://www.microsoft.com/downloads/details.aspx?familyid=092a389a-2296-4c3b-a160-2523154ec764)  
(KB969856)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Virtual Server 2005 R2
</td>
<td style="border:1px solid black;">
[Microsoft Virtual Server 2005 R2 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1481024d-b430-4d0e-be16-2f141c6a7e57)  
(KB969856)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Virtual Server 2005 R2 x64 Edition
</td>
<td style="border:1px solid black;">
[Microsoft Virtual Server 2005 R2 x64 Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1481024d-b430-4d0e-be16-2f141c6a7e57)  
(KB969856)  
(Importante)
</td>
</tr>
</table>
 

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/default.aspx). [TechNet Security Center](http://go.microsoft.com/fwlink/?linkid=21171) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://www.microsoft.com/spain/protect/default.mspx), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS07-036"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Nota** A partir del 1 de agosto de 2009, Microsoft dejará de ofrecer soporte técnico a Office Update y Office Update Inventory Tool. Para seguir obteniendo las actualizaciones más recientes para los productos de Microsoft, use [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747). Para obtener más información, vea [Acerca de Microsoft Office Update: Preguntas más frecuentes](http://office.microsoft.com/en-us/downloads/fx010402221033.aspx).

**Consejos para la detección y la implementación**

Microsoft ofrece recomendaciones para la detección y la implementación de las actualizaciones de seguridad de este mes. Esta orientación también ayudará a los profesionales de TI a comprender el funcionamiento de distintas herramientas que sirven de ayuda en la implementación de la actualización de seguridad, como Windows Update, Microsoft Update, Office Update, Microsoft Baseline Security Analyzer (MBSA), Office Detection Tool, Microsoft Systems Management Server (SMS) y Extended Security Update Inventory Tool (ESUIT). Para obtener más información, consulte el [artículo 910723 de Microsoft Knowledge Base](http://support.microsoft.com/kb/910723).

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://go.microsoft.com/fwlink/?linkid=21134).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar con rapidez y fiabilidad las actualizaciones críticas y de seguridad más recientes en sistemas operativos Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://go.microsoft.com/fwlink/?linkid=50120).

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. La siguiente versión de SMS, System Center Configuration Manager 2007, ya está disponible; consulte también [System Center Configuration Manager 2007](http://technet.microsoft.com/en-us/library/bb735860.aspx). Para obtener más información acerca de cómo pueden utilizar los administradores SMS 2003 para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar [Software Updates Services Feature Pack](http://go.microsoft.com/fwlink/?linkid=33340) como ayuda para la implementación de actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://go.microsoft.com/fwlink/?linkid=21158).

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

En [Orientación de seguridad para la administración de actualizaciones](http://go.microsoft.com/fwlink/?linkid=21168) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](http://support.microsoft.com/kb/913086).

**Comunidad de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [IT Pro Security Community](http://go.microsoft.com/fwlink/?linkid=21164) (en inglés).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

-   Thomas Garnier, de [SkyRecon](http://www.skyrecon.com/), y Zheng Wenbin, Liu Qi y Song Shenlei, de [Qihoo 360 Security Center](http://www.360.cn/), por informar de un problema descrito en MS09-028
-   Yamata Li, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de un problema descrito en MS09-028
-   Aaron Portnoy, de [TippingPoint DVLabs](http://dvlabs.tippingpoint.com/), y un investigador anónimo en colaboración con TippingPoint's [Zero Day Initiative](http://www.zerodayinitiative.com/), Thomas Garnier, de [SkyRecon](http://www.skyrecon.com/), y Yamata Li, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de un problema descrito en MS09-028
-   [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS09-029
-   Tavis Ormandy, de [Google Inc.](http://www.google.com), por informar de un problema descrito en MS09-029
-   Thomas Garnier, por informar de un problema descrito en MS09-029
-   Lionel d'Hauenens, de [Labo Skopia](http://www.laboskopia.com/), en colaboración con [VeriSign iDefense Labs](http://www.idefense.com/), por informar de un problema descrito en MS09-030
-   Ryan Smith y Alex Wheeler, de [IBM IIS X-Force](http://www.iss.net/), por informar de un problema descrito inicialmente en MS09-032
-   Julien Tinnes y Tavis Ormandy, de [Google Inc.](http://www.google.com/), por informar de un problema descrito en MS09-033
-   Peter Vreugdenhil, de [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS09-034
-   Wushi y Ling, de [team509](http://www.team509.com/), en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS09-034
-   Peter Vreugdenhil, en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS09-034
-   David Dewey, de [IBM ISS X-Force](http://www.iss.net/), por informar de un problema descrito en MS09-035
-   Ryan Smith, de [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS09-035

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Los clientes de Estados Unidos y Canadá pueden recibir soporte técnico del [soporte de seguridad](http://go.microsoft.com/fwlink/?linkid=21131) o en el teléfono 1-866-PCSAFETY. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de las opciones de asistencia disponibles, visite [Ayuda y soporte técnico de Microsoft](http://support.microsoft.com/).
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (14 de julio de 2009): Publicación del resumen del boletín.
-   V1.1 (15 de julio de 2009): Se ha actualizado el resumen ejecutivo para MS09-032, se ha corregido el requisito de reinicio para MS09-029 y se han realizado varias modificaciones.
-   V2.0 (28 de julio de 2009): Se han agregado los boletines de seguridad de Microsoft MS09-034, Actualización de seguridad acumulativa para Internet Explorer (972260), y MS09-035, Vulnerabilidades en Visual Studio Active Template Library podrían permitir la ejecución remota de código (969706). También se han agregado vínculos a la conferencia en línea del boletín para este boletín de seguridad fuera de banda.
-   V3.0 (4 de agosto de 2009): Se ha revisado para anunciar la nueva publicación de la actualización para Microsoft Internet Explorer 6 Service Pack 1 en Microsoft Windows 2000 Service Pack 4. Todos los clientes que ya hayan instalado la actualización original para Internet Explorer 6 Service Pack 1 en Microsoft Windows 2000 Service Pack 4 ya están protegidos. No obstante, los clientes que tengan la versión en coreano de Internet Explorer 6 Service Pack 1 pueden reinstalar la actualización para Internet Explorer 6 Service Pack 1 en sus sistemas Windows 2000 para tener las mismas protecciones y también resolver un problema de impresión. Vea el boletín de seguridad de Microsoft MS09-034.
-   V4.0 (11 de agosto de 2009): Se ha revisado para anunciar la nueva publicación de MS09-035. Se ha vuelto a publicar el boletín para ofrecer nuevas actualizaciones para Microsoft Visual Studio 2005 Service Pack 1 (KB973673), Microsoft Visual Studio 2008 (KB973674) y Microsoft Visual Studio 2008 Service Pack 1 (KB973675), para los desarrolladores que usan Visual Studio para crear componentes y controles para aplicaciones móviles que usan ATL para dispositivos inteligentes.
-   V4.1 (13 de agosto de 2009): Se ha corregido el requisito de reinicio para MS09-035.
-   V5.0 (19 de agosto de 2009): Se ha agregado una nota al pie para el boletín MS09-028 con el fin de aclarar el software afectado para DirectX 8.1.
-   V6.0 (25 de agosto de 2009): Revisión para anunciar la nueva publicación de la actualización del idioma japonés para Windows XP Service Pack 2, Windows XP Service Pack 3 y Windows XP Professional x64 Edition Service Pack 2. Todos los clientes que hayan instalado la actualización original ya están protegidos. No obstante, los clientes que tienen la versión del idioma japonés de Windows XP Service Pack 2, Windows XP Service Pack 3 o Windows XP Professional x64 Edition Service Pack 2 deben reinstalar la actualización para tener las mismas protecciones y, además, resolver un problema de impresión. Vea el boletín de seguridad de Microsoft MS09-029.
-   V7.0 (12 de enero de 2010): Se ha revisado para agregar Windows Embedded CE 6.0 al software afectado para MS09-035. La actualización de Windows Embedded CE 6.0 (KB974616) es una actualización acumulativa que sólo está disponible en el Centro de descarga de Microsoft. Los clientes que usan la plataforma Windows Embedded CE 6.0 deben considerar la posibilidad de aplicar la actualización acumulativa.
-   V8.0 (9 de marzo de 2010): Se ha revisado para agregar Microsoft Virtual Server 2005 al software afectado para MS09-033.

*Built at 2014-04-18T01:50:00Z-07:00*
