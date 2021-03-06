---
TOCTitle: 'MS13-OCT'
Title: Resumen del boletín de seguridad de Microsoft de octubre 2013
ms:assetid: 'ms13-oct'
ms:contentKeyID: 61225454
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms13-oct(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de octubre 2013
=============================================================

Publicado: martes, 8 de octubre de 2013 | Actualizado: miércoles, 6 de noviembre de 2013

**Versión:** 1.2

Este resumen del boletín enumera los boletines de seguridad publicados para octubre de 2013.

Con la publicación de los boletines de seguridad de octubre de 2013, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 3 de octubre de 2013. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 9 de octubre de 2013, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de octubre](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032557381&culture=en-us).

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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324021">MS13-080</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (2879017)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y ocho vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. La más grave de las vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un atacante que aprovechara la más grave de estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=314048">MS13-081</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en los controladores modo kernel de Windows podrían permitir la ejecución remota de código (2870008)</strong><br />
<br />
Esta actualización de seguridad resuelve siete vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un usuario consulta contenido compartido que inserta archivos de fuente OpenType o TrueType. Un atacante que aprovechara estas vulnerabilidades podría obtener el control completo del sistema afectado.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=318048">MS13-082</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en .NET Framework podrían permitir la ejecución remota de código (2878890)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada y una vulnerabilidad de la que se ha informado de forma pública en Microsoft .NET Framework. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un usuario visita un sitio web que incluye un archivo de fuentes OpenType (OTF) especialmente diseñado con un explorador que pueda crear instancias de aplicaciones XBAP.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Microsoft .NET Framework</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=314045">MS13-083</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en la biblioteca de controles comunes de Windows podría permitir la ejecución remota de código (2864058)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un atacante envía una solicitud web especialmente diseñada a una aplicación web ASP.NET que se ejecute en un sistema afectado. Un atacante puede aprovechar esta vulnerabilidad sin autenticación para ejecutar código arbitrario.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324028">MS13-084</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft SharePoint Server podrían permitir la ejecución remota de código (2885089)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en el software de servidor de Microsoft Office. La vulnerabilidad más grave podría permitir la ejecución remota de código si un usuario abre un archivo de Office especialmente diseñado en una versión afectada de Microsoft SharePoint Server, Microsoft Office Services o Web Apps.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office,<br />
Software de servidor de Microsoft</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324026">MS13-085</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Excel podrían permitir la ejecución remota de código (2885080)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft Office. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario abre un archivo de Office especialmente diseñado con una versión afectada de Microsoft u otro software de Microsoft Office. Un atacante que aprovechara las vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324027">MS13-086</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Word podrían permitir la ejecución remota de código (2885084)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft Office. Las vulnerabilidades podrían permitir la ejecución remota de código si se abre un archivo especialmente diseñado en una versión afectada de Microsoft Word u otro software de Microsoft Office. Un atacante que aprovechara las vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324590">MS13-087</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Silverlight podría permitir la divulgación de información (2890788)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Silverlight. La vulnerabilidad podría permitir la divulgación de información si un atacante hospeda un sitio web que contenga una aplicación de Silverlight especialmente diseñada que pudiera aprovechar esta vulnerabilidad y convence a un usuario de que visite el sitio web. El atacante también podría aprovechar sitios web vulnerables y sitios web que aceptan o reciben contenido o anuncios proporcionados por el usuario. Los sitios web de este tipo podrían incluir contenido malintencionado a través del cual se podría aprovechar esta vulnerabilidad. No obstante, el atacante no podría en ningún caso obligar a los usuarios a visitar un sitio web. Por lo tanto, tendría que atraerlos a un sitio web; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico o de un mensaje de Instant Messenger que los lleve al sitio web del atacante. También sería posible que se mostrara contenido web diseñado especialmente mediante titulares de anuncios u otros métodos para hacer llegar contenido web a los sistemas afectados.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Divulgación de información</td>
<td style="border:1px solid black;">No requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Silverlight</td>
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324021">MS13-080</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3872">CVE-2013-3872</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324021">MS13-080</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3873">CVE-2013-3873</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324021">MS13-080</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3874">CVE-2013-3874</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324021">MS13-080</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3875">CVE-2013-3875</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324021">MS13-080</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3882">CVE-2013-3882</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324021">MS13-080</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3885">CVE-2013-3885</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324021">MS13-080</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3886">CVE-2013-3886</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324021">MS13-080</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3893">CVE-2013-3893</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esa vulnerabilidad ya se ha divulgado.<br />
<br />
Microsoft tiene constancia de ataques dirigidos que intentan aprovechar esta vulnerabilidad en Internet Explorer 8 e Internet Explorer 9.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324021">MS13-080</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3897">CVE-2013-3897</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Microsoft tiene constancia de ataques dirigidos que intentan aprovechar esta vulnerabilidad en Internet Explorer 8.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=314048">MS13-081</a></td>
<td style="border:1px solid black;">Vulnerabilidad de análisis de fuentes OpenType</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3128">CVE-2013-3128</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Esta vulnerabilidad también afecta a <a href="http://go.microsoft.com/fwlink/?linkid=318048">MS13-082</a><a href="http://go.microsoft.com/fwlink/?linkid=293350"></a>.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=314048">MS13-081</a></td>
<td style="border:1px solid black;">Vulnerabilidad del descriptor de USB en Windows</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3200">CVE-2013-3200</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=314048">MS13-081</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de Win32k después de la liberación</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3879">CVE-2013-3879</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=314048">MS13-081</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en el contenedor de aplicaciones</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3880">CVE-2013-3880</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de divulgación de información que podría conllevar la elevación de privilegios.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=314048">MS13-081</a></td>
<td style="border:1px solid black;">Vulnerabilidad de página nula en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3881">CVE-2013-3881</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=314048">MS13-081</a></td>
<td style="border:1px solid black;">Vulnerabilidad de doble captura en el subsistema del kernel de gráficos de DirectX</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3888">CVE-2013-3888</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=314048">MS13-081</a></td>
<td style="border:1px solid black;">Vulnerabilidad de la tabla CMAP de fuentes TrueType</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3894">CVE-2013-3894</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=318048">MS13-082</a></td>
<td style="border:1px solid black;">Vulnerabilidad de análisis de fuentes OpenType</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3128">CVE-2013-3128</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad también afecta a <a href="http://go.microsoft.com/fwlink/?linkid=314048">MS13-081</a><a href="http://go.microsoft.com/fwlink/?linkid=293350"></a>.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=318048">MS13-082</a></td>
<td style="border:1px solid black;">Vulnerabilidad de expansión de entidades</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3860">CVE-2013-3860</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=318048">MS13-082</a></td>
<td style="border:1px solid black;">Vulnerabilidad de análisis de JSON</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3861">CVE-2013-3861</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.<br />
<br />
Esa vulnerabilidad ya se ha divulgado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=314045">MS13-083</a></td>
<td style="border:1px solid black;">Vulnerabilidad de desbordamiento de enteros en Comctl32</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3195">CVE-2013-3195</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324028">MS13-084</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Microsoft Excel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3889">CVE-2013-3889</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad también afecta a <a href="http://go.microsoft.com/fwlink/?linkid=324026">MS13-085</a><a href="http://go.microsoft.com/fwlink/?linkid=293350"></a>.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324028">MS13-084</a></td>
<td style="border:1px solid black;">Vulnerabilidad de inserción de parámetros</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3895">CVE-2013-3895</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324026">MS13-085</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Microsoft Excel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3889">CVE-2013-3889</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad también afecta a <a href="http://go.microsoft.com/fwlink/?linkid=324028">MS13-084</a><a href="http://go.microsoft.com/fwlink/?linkid=293350"></a>.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324026">MS13-085</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Microsoft Excel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3890">CVE-2013-3890</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324027">MS13-086</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3891">CVE-2013-3891</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324027">MS13-086</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3892">CVE-2013-3892</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=324590">MS13-087</a></td>
<td style="border:1px solid black;">Vulnerabilidad de Silverlight</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3896">CVE-2013-3896</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de divulgación de información que podría conllevar la omisión de característica de seguridad.</td>
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
<th colspan="5" style="border:1px solid black;">
Windows XP  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-080**](http://go.microsoft.com/fwlink/?linkid=324021)
</td>
<td style="border:1px solid black;">
[**MS13-081**](http://go.microsoft.com/fwlink/?linkid=314048)
</td>
<td style="border:1px solid black;">
[**MS13-082**](http://go.microsoft.com/fwlink/?linkid=318048)
</td>
<td style="border:1px solid black;">
[**MS13-083**](http://go.microsoft.com/fwlink/?linkid=314045)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
Internet Explorer 6   
(2879017)  
(Crítica)  
Internet Explorer 7   
(2879017)  
(Crítica)  
Internet Explorer 8   
(2879017)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows XP Service Pack 3  
(2847311)  
(Crítica)  
Windows XP Service Pack 3  
(2862330)  
(Importante)  
Windows XP Service Pack 3  
(2862335)  
(Importante)  
Windows XP Service Pack 3  
(2868038)  
(Importante)  
Windows XP Service Pack 3  
(2883150)  
(Crítica)  
Windows XP Service Pack 3  
(2884256)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2863239)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2861189)  
(Crítica)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2861697)  
(Importante)  
Microsoft .NET Framework 4.0  
(2858302)  
(Importante)  
Microsoft .NET Framework 4.0  
(2861188)  
(Crítica)
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
Internet Explorer 6   
(2879017)  
(Crítica)  
Internet Explorer 7   
(2879017)  
(Crítica)  
Internet Explorer 8   
(2879017)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2  
(2847311)  
(Crítica)  
Windows XP Professional x64 Edition Service Pack 2  
(2862330)  
(Importante)  
Windows XP Professional x64 Edition Service Pack 2  
(2862335)  
(Importante)  
Windows XP Professional x64 Edition Service Pack 2  
(2868038)  
(Importante)  
Windows XP Professional x64 Edition Service Pack 2  
(2883150)  
(Crítica)  
Windows XP Professional x64 Edition Service Pack 2  
(2884256)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2863239)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2861189)  
(Crítica)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2861697)  
(Importante)  
Microsoft .NET Framework 4.0  
(2858302)  
(Importante)  
Microsoft .NET Framework 4.0  
(2861188)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2  
(2864058)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-080**](http://go.microsoft.com/fwlink/?linkid=324021)
</td>
<td style="border:1px solid black;">
[**MS13-081**](http://go.microsoft.com/fwlink/?linkid=314048)
</td>
<td style="border:1px solid black;">
[**MS13-082**](http://go.microsoft.com/fwlink/?linkid=318048)
</td>
<td style="border:1px solid black;">
[**MS13-083**](http://go.microsoft.com/fwlink/?linkid=314045)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 6   
(2879017)  
(Moderada)  
Internet Explorer 7  
(2879017)  
(Moderada)  
Internet Explorer 8  
(2879017)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(2847311)  
(Crítica)  
Windows Server 2003 Service Pack 2  
(2862330)  
(Importante)  
Windows Server 2003 Service Pack 2  
(2862335)  
(Importante)  
Windows Server 2003 Service Pack 2  
(2868038)  
(Importante)  
Windows Server 2003 Service Pack 2  
(2883150)  
(Crítica)  
Windows Server 2003 Service Pack 2  
(2884256)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2863239)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2861189)  
(Crítica)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2861697)  
(Importante)  
Microsoft .NET Framework 4.0  
(2858302)  
(Importante)  
Microsoft .NET Framework 4.0  
(2861188)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(2864058)  
(Sin clasificación de gravedad)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 6   
(2879017)  
(Moderada)  
Internet Explorer 7  
(2879017)  
(Moderada)  
Internet Explorer 8  
(2879017)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2847311)  
(Crítica)  
Windows Server 2003 x64 Edition Service Pack 2  
(2862330)  
(Importante)  
Windows Server 2003 x64 Edition Service Pack 2  
(2862335)  
(Importante)  
Windows Server 2003 x64 Edition Service Pack 2  
(2868038)  
(Importante)  
Windows Server 2003 x64 Edition Service Pack 2  
(2883150)  
(Crítica)  
Windows Server 2003 x64 Edition Service Pack 2  
(2884256)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2863239)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2861189)  
(Crítica)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2861697)  
(Importante)  
Microsoft .NET Framework 4.0  
(2858302)  
(Importante)  
Microsoft .NET Framework 4.0  
(2861188)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2864058)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
Internet Explorer 6   
(2879017)  
(Moderada)  
Internet Explorer 7  
(2879017)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2847311)  
(Crítica)  
Windows Server 2003 con SP2 para sistemas con Itanium  
(2862330)  
(Importante)  
Windows Server 2003 con SP2 para sistemas con Itanium  
(2862335)  
(Importante)  
Windows Server 2003 con SP2 para sistemas con Itanium  
(2868038)  
(Importante)  
Windows Server 2003 con SP2 para sistemas con Itanium  
(2883150)  
(Crítica)  
Windows Server 2003 con SP2 para sistemas con Itanium  
(2884256)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2863239)  
(Importante)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2861697)  
(Importante)  
Microsoft .NET Framework 4.0  
(2858302)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2864058)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-080**](http://go.microsoft.com/fwlink/?linkid=324021)
</td>
<td style="border:1px solid black;">
[**MS13-081**](http://go.microsoft.com/fwlink/?linkid=314048)
</td>
<td style="border:1px solid black;">
[**MS13-082**](http://go.microsoft.com/fwlink/?linkid=318048)
</td>
<td style="border:1px solid black;">
[**MS13-083**](http://go.microsoft.com/fwlink/?linkid=314045)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2879017)  
(Crítica)  
Internet Explorer 8  
(2879017)  
(Crítica)  
Internet Explorer 9   
(2879017)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2847311)  
(Crítica)  
Windows Vista Service Pack 2  
(2855844)  
(Crítica)  
Windows Vista Service Pack 2  
(2862330)  
(Importante)  
Windows Vista Service Pack 2  
(2862335)  
(Importante)  
Windows Vista Service Pack 2  
(2864202)  
(Importante)  
Windows Vista Service Pack 2  
(2868038)  
(Importante)  
Windows Vista Service Pack 2  
(2876284)  
(Importante)  
Windows Vista Service Pack 2  
(2883150)  
(Crítica)  
Windows Vista Service Pack 2  
(2884256)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2863253)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2861190)  
(Crítica)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2861697)  
(Importante)  
Microsoft .NET Framework 4.0  
(2858302)  
(Importante)  
Microsoft .NET Framework 4.0  
(2861188)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2861193)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2861208)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2864058)  
(Sin clasificación de gravedad)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2879017)  
(Crítica)  
Internet Explorer 8  
(2879017)  
(Crítica)  
Internet Explorer 9   
(2879017)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2847311)  
(Crítica)  
Windows Vista x64 Edition Service Pack 2  
(2855844)  
(Crítica)  
Windows Vista x64 Edition Service Pack 2  
(2862330)  
(Importante)  
Windows Vista x64 Edition Service Pack 2  
(2862335)  
(Importante)  
Windows Vista x64 Edition Service Pack 2  
(2864202)  
(Importante)  
Windows Vista x64 Edition Service Pack 2  
(2868038)  
(Importante)  
Windows Vista x64 Edition Service Pack 2  
(2876284)  
(Importante)  
Windows Vista x64 Edition Service Pack 2  
(2883150)  
(Crítica)  
Windows Vista x64 Edition Service Pack 2  
(2884256)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2863253)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2861190)  
(Crítica)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2861697)  
(Importante)  
Microsoft .NET Framework 4.0  
(2858302)  
(Importante)  
Microsoft .NET Framework 4.0  
(2861188)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2861193)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2861208)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2864058)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-080**](http://go.microsoft.com/fwlink/?linkid=324021)
</td>
<td style="border:1px solid black;">
[**MS13-081**](http://go.microsoft.com/fwlink/?linkid=314048)
</td>
<td style="border:1px solid black;">
[**MS13-082**](http://go.microsoft.com/fwlink/?linkid=318048)
</td>
<td style="border:1px solid black;">
[**MS13-083**](http://go.microsoft.com/fwlink/?linkid=314045)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2879017)  
(Moderada)  
Internet Explorer 8  
(2879017)  
(Moderada)  
Internet Explorer 9   
(2879017)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2847311)  
(Crítica)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2855844)  
(Crítica)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2862330)  
(Importante)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2862335)  
(Importante)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2864202)  
(Importante)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2868038)  
(Importante)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2876284)  
(Importante)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2883150)  
(Crítica)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2884256)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2863253)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2861190)  
(Crítica)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2861697)  
(Importante)  
Microsoft .NET Framework 4.0  
(2858302)  
(Importante)  
Microsoft .NET Framework 4.0  
(2861188)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2861193)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2861208)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2864058)  
(Sin clasificación de gravedad)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2879017)  
(Moderada)  
Internet Explorer 8  
(2879017)  
(Moderada)  
Internet Explorer 9   
(2879017)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2847311)  
(Crítica)  
Windows Server 2008 para sistemas x64 Service Pack 2  
(2855844)  
(Crítica)  
Windows Server 2008 para sistemas x64 Service Pack 2  
(2862330)  
(Importante)  
Windows Server 2008 para sistemas x64 Service Pack 2  
(2862335)  
(Importante)  
Windows Server 2008 para sistemas x64 Service Pack 2  
(2864202)  
(Importante)  
Windows Server 2008 para sistemas x64 Service Pack 2  
(2868038)  
(Importante)  
Windows Server 2008 para sistemas x64 Service Pack 2  
(2876284)  
(Importante)  
Windows Server 2008 para sistemas x64 Service Pack 2  
(2883150)  
(Crítica)  
Windows Server 2008 para sistemas x64 Service Pack 2  
(2884256)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2863253)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2861190)  
(Crítica)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2861697)  
(Importante)  
Microsoft .NET Framework 4.0  
(2858302)  
(Importante)  
Microsoft .NET Framework 4.0  
(2861188)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2861193)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2861208)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2864058)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2879017)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2847311)  
(Crítica)  
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2862330)  
(Importante)  
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2862335)  
(Importante)  
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2864202)  
(Importante)  
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2868038)  
(Importante)  
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2876284)  
(Importante)  
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2883150)  
(Crítica)  
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2884256)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2863253)  
(Importante)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2861697)  
(Importante)  
Microsoft .NET Framework 4.0  
(2858302)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2864058)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows 7
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-080**](http://go.microsoft.com/fwlink/?linkid=324021)
</td>
<td style="border:1px solid black;">
[**MS13-081**](http://go.microsoft.com/fwlink/?linkid=314048)
</td>
<td style="border:1px solid black;">
[**MS13-082**](http://go.microsoft.com/fwlink/?linkid=318048)
</td>
<td style="border:1px solid black;">
[**MS13-083**](http://go.microsoft.com/fwlink/?linkid=314045)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2879017)  
(Crítica)  
Internet Explorer 9   
(2879017)  
(Crítica)  
Internet Explorer 10   
(2879017)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2847311)  
(Crítica)  
Windows 7 para sistemas de 32 bits Service Pack 1  
(2855844)  
(Crítica)  
Windows 7 para sistemas de 32 bits Service Pack 1  
(2862330)  
(Importante)  
Windows 7 para sistemas de 32 bits Service Pack 1  
(2862335)  
(Importante)  
Windows 7 para sistemas de 32 bits Service Pack 1  
(2864202)  
(Importante)  
Windows 7 para sistemas de 32 bits Service Pack 1  
(2868038)  
(Importante)  
Windows 7 para sistemas de 32 bits Service Pack 1  
(2876284)  
(Importante)  
Windows 7 para sistemas de 32 bits Service Pack 1  
(2883150)  
(Crítica)  
Windows 7 para sistemas de 32 bits Service Pack 1  
(2884256)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2861191)  
(Crítica)  
Microsoft .NET Framework 3.5.1  
(2861698)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2863240)  
(Importante)  
Microsoft .NET Framework 4.0  
(2858302)  
(Importante)  
Microsoft .NET Framework 4.5  
(2861208)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2864058)  
(Sin clasificación de gravedad)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2879017)  
(Crítica)  
Internet Explorer 9   
(2879017)  
(Crítica)  
Internet Explorer 10   
(2879017)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2847311)  
(Crítica)  
Windows 7 para sistemas x64 Service Pack 1  
(2855844)  
(Crítica)  
Windows 7 para sistemas x64 Service Pack 1  
(2862330)  
(Importante)  
Windows 7 para sistemas x64 Service Pack 1  
(2862335)  
(Importante)  
Windows 7 para sistemas x64 Service Pack 1  
(2864202)  
(Importante)  
Windows 7 para sistemas x64 Service Pack 1  
(2868038)  
(Importante)  
Windows 7 para sistemas x64 Service Pack 1  
(2876284)  
(Importante)  
Windows 7 para sistemas x64 Service Pack 1  
(2883150)  
(Crítica)  
Windows 7 para sistemas x64 Service Pack 1  
(2884256)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2861191)  
(Crítica)  
Microsoft .NET Framework 3.5.1  
(2861698)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2863240)  
(Importante)  
Microsoft .NET Framework 4.0  
(2858302)  
(Importante)  
Microsoft .NET Framework 4.5  
(2861208)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2864058)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows Server 2008 R2
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-080**](http://go.microsoft.com/fwlink/?linkid=324021)
</td>
<td style="border:1px solid black;">
[**MS13-081**](http://go.microsoft.com/fwlink/?linkid=314048)
</td>
<td style="border:1px solid black;">
[**MS13-082**](http://go.microsoft.com/fwlink/?linkid=318048)
</td>
<td style="border:1px solid black;">
[**MS13-083**](http://go.microsoft.com/fwlink/?linkid=314045)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2879017)  
(Moderada)  
Internet Explorer 9   
(2879017)  
(Moderada)  
Internet Explorer 10   
(2879017)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2847311)  
(Crítica)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2855844)  
(Crítica)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2862330)  
(Importante)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2862335)  
(Importante)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2864202)  
(Importante)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2868038)  
(Importante)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2876284)  
(Importante)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2883150)  
(Crítica)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2884256)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2861191)  
(Crítica)  
Microsoft .NET Framework 3.5.1  
(2861698)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2863240)  
(Importante)  
Microsoft .NET Framework 4.0  
(2858302)  
(Importante)  
Microsoft .NET Framework 4.5  
(2861208)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2864058)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2879017)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2847311)  
(Crítica)  
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2855844)  
(Crítica)  
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2862330)  
(Importante)  
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2862335)  
(Importante)  
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2864202)  
(Importante)  
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2868038)  
(Importante)  
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2876284)  
(Importante)  
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2883150)  
(Crítica)  
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2884256)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2861698)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2863240)  
(Importante)  
Microsoft .NET Framework 4.0  
(2858302)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2864058)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows 8
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-080**](http://go.microsoft.com/fwlink/?linkid=324021)
</td>
<td style="border:1px solid black;">
[**MS13-081**](http://go.microsoft.com/fwlink/?linkid=314048)
</td>
<td style="border:1px solid black;">
[**MS13-082**](http://go.microsoft.com/fwlink/?linkid=318048)
</td>
<td style="border:1px solid black;">
[**MS13-083**](http://go.microsoft.com/fwlink/?linkid=314045)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2879017)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2847311)  
(Crítica)  
Windows 8 para sistemas de 32 bits  
(2862330)  
(Importante)  
Windows 8 para sistemas de 32 bits  
(2862335)  
(Importante)  
Windows 8 para sistemas de 32 bits  
(2863725)  
(Importante)  
Windows 8 para sistemas de 32 bits  
(2864202)  
(Importante)  
Windows 8 para sistemas de 32 bits  
(2868038)  
(Importante)  
Windows 8 para sistemas de 32 bits  
(2883150)  
(Crítica)  
Windows 8 para sistemas de 32 bits  
(2884256)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2861194)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2861704)  
(Importante)  
Microsoft .NET Framework 3.5  
(2863243)  
(Importante)  
Microsoft .NET Framework 4.5  
(2861702)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2864058)  
(Sin clasificación de gravedad)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 8 para sistemas de 64 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2879017)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 64 bits  
(2847311)  
(Crítica)  
Windows 8 para sistemas de 64 bits  
(2862330)  
(Importante)  
Windows 8 para sistemas de 64 bits  
(2862335)  
(Importante)  
Windows 8 para sistemas de 64 bits  
(2863725)  
(Importante)  
Windows 8 para sistemas de 64 bits  
(2864202)  
(Importante)  
Windows 8 para sistemas de 64 bits  
(2868038)  
(Importante)  
Windows 8 para sistemas de 64 bits  
(2883150)  
(Crítica)  
Windows 8 para sistemas de 64 bits  
(2884256)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2861194)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2861704)  
(Importante)  
Microsoft .NET Framework 3.5  
(2863243)  
(Importante)  
Microsoft .NET Framework 4.5  
(2861702)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 64 bits  
(2864058)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows Server 2012
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-080**](http://go.microsoft.com/fwlink/?linkid=324021)
</td>
<td style="border:1px solid black;">
[**MS13-081**](http://go.microsoft.com/fwlink/?linkid=314048)
</td>
<td style="border:1px solid black;">
[**MS13-082**](http://go.microsoft.com/fwlink/?linkid=318048)
</td>
<td style="border:1px solid black;">
[**MS13-083**](http://go.microsoft.com/fwlink/?linkid=314045)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2879017)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2847311)  
(Crítica)  
Windows Server 2012  
(2862330)  
(Importante)  
Windows Server 2012  
(2862335)  
(Importante)  
Windows Server 2012  
(2863725)  
(Importante)  
Windows Server 2012  
(2864202)  
(Importante)  
Windows Server 2012  
(2868038)  
(Importante)  
Windows Server 2012  
(2883150)  
(Crítica)  
Windows Server 2012  
(2884256)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2861194)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2861704)  
(Importante)  
Microsoft .NET Framework 3.5  
(2863243)  
(Importante)  
Microsoft .NET Framework 4.5  
(2861702)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2864058)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows RT
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-080**](http://go.microsoft.com/fwlink/?linkid=324021)
</td>
<td style="border:1px solid black;">
[**MS13-081**](http://go.microsoft.com/fwlink/?linkid=314048)
</td>
<td style="border:1px solid black;">
[**MS13-082**](http://go.microsoft.com/fwlink/?linkid=318048)
</td>
<td style="border:1px solid black;">
[**MS13-083**](http://go.microsoft.com/fwlink/?linkid=314045)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows RT
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2879017)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows RT  
(2847311)  
(Crítica)  
Windows RT  
(2862330)  
(Importante)  
Windows RT  
(2862335)  
(Importante)  
Windows RT  
(2863725)  
(Importante)  
Windows RT  
(2864202)  
(Importante)  
Windows RT  
(2868038)  
(Importante)  
Windows RT  
(2883150)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 4.5  
(2861702)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT  
(2864058)  
(Sin clasificación de gravedad)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows 8.1
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-080**](http://go.microsoft.com/fwlink/?linkid=324021)
</td>
<td style="border:1px solid black;">
[**MS13-081**](http://go.microsoft.com/fwlink/?linkid=314048)
</td>
<td style="border:1px solid black;">
[**MS13-082**](http://go.microsoft.com/fwlink/?linkid=318048)
</td>
<td style="border:1px solid black;">
[**MS13-083**](http://go.microsoft.com/fwlink/?linkid=314045)
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
**Ninguna**
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 11<sup>[1]</sup>   
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
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
Windows 8.1 para sistemas de 64 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 11<sup>[1]</sup>   
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows Server 2012 R2
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-080**](http://go.microsoft.com/fwlink/?linkid=324021)
</td>
<td style="border:1px solid black;">
[**MS13-081**](http://go.microsoft.com/fwlink/?linkid=314048)
</td>
<td style="border:1px solid black;">
[**MS13-082**](http://go.microsoft.com/fwlink/?linkid=318048)
</td>
<td style="border:1px solid black;">
[**MS13-083**](http://go.microsoft.com/fwlink/?linkid=314045)
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
**Ninguna**
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012 R2
</td>
<td style="border:1px solid black;">
Internet Explorer 11<sup>[1]</sup>   
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Windows RT 8.1
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-080**](http://go.microsoft.com/fwlink/?linkid=324021)
</td>
<td style="border:1px solid black;">
[**MS13-081**](http://go.microsoft.com/fwlink/?linkid=314048)
</td>
<td style="border:1px solid black;">
[**MS13-082**](http://go.microsoft.com/fwlink/?linkid=318048)
</td>
<td style="border:1px solid black;">
[**MS13-083**](http://go.microsoft.com/fwlink/?linkid=314045)
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
**Ninguna**
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows RT 8.1
</td>
<td style="border:1px solid black;">
Internet Explorer 11<sup>[1]</sup>   
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Opción de instalación Server Core
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-080**](http://go.microsoft.com/fwlink/?linkid=324021)
</td>
<td style="border:1px solid black;">
[**MS13-081**](http://go.microsoft.com/fwlink/?linkid=314048)
</td>
<td style="border:1px solid black;">
[**MS13-082**](http://go.microsoft.com/fwlink/?linkid=318048)
</td>
<td style="border:1px solid black;">
[**MS13-083**](http://go.microsoft.com/fwlink/?linkid=314045)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2847311)  
(Crítica)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2862330)  
(Importante)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2862335)  
(Importante)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2864202)  
(Importante)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2876284)  
(Importante)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2883150)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2864058)  
(Sin clasificación de gravedad)
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
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2847311)  
(Crítica)  
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2862330)  
(Importante)  
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2862335)  
(Importante)  
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2864202)  
(Importante)  
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2876284)  
(Importante)  
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2883150)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2864058)  
(Crítica)
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
(2847311)  
(Crítica)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2862330)  
(Importante)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2862335)  
(Importante)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2864202)  
(Importante)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2876284)  
(Importante)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2883150)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2861698)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2863240)  
(Importante)  
Microsoft .NET Framework 4.0  
(2858302)  
(Importante)  
Microsoft .NET Framework 4.5  
(2861208)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2864058)  
(Crítica)
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
Windows Server 2012 (instalación Server Core)  
(2847311)  
(Crítica)  
Windows Server 2012 (instalación Server Core)  
(2862330)  
(Importante)  
Windows Server 2012 (instalación Server Core)  
(2862335)  
(Importante)  
Windows Server 2012 (instalación Server Core)  
(2863725)  
(Importante)  
Windows Server 2012 (instalación Server Core)  
(2864202)  
(Importante)  
Windows Server 2012 (instalación Server Core)  
(2883150)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2861194)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2861704)  
(Importante)  
Microsoft .NET Framework 3.5  
(2863243)  
(Importante)  
Microsoft .NET Framework 4.5  
(2861702)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(2864058)  
(Crítica)
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
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
**Nota para MS13-080**

<sup>[1]</sup>Para Internet Explorer 11, los clientes deben aplicar el conjunto de actualizaciones de Windows RT 8.1, Windows 8.1 y Windows Server 2012 R2: Octubre de 2013 (2883200). Tenga en cuenta que el conjunto de actualizaciones 2883200 contiene cambios de seguridad y cambios no relacionados con la seguridad. Para obtener más información y los vínculos de descarga disponibles, vea el [artículo 2883200 de Microsoft Knowledge Base](http://support.microsoft.com/kb/2883200).

#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Office 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-085**](http://go.microsoft.com/fwlink/?linkid=324026)
</td>
<td style="border:1px solid black;">
[**MS13-086**](http://go.microsoft.com/fwlink/?linkid=324027)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**
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
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft Word 2003 Service Pack 3  
(2826020)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Office 2007
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-085**](http://go.microsoft.com/fwlink/?linkid=324026)
</td>
<td style="border:1px solid black;">
[**MS13-086**](http://go.microsoft.com/fwlink/?linkid=324027)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Microsoft Excel 2007 Service Pack 3  
(2827324)  
(Importante)  
Microsoft Office 2007 Service Pack 3  
(2760585)  
(Importante)  
Microsoft Office 2007 Service Pack 3  
(2760591)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Word 2007 Service Pack 3  
(2827330)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Office 2010
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-085**](http://go.microsoft.com/fwlink/?linkid=324026)
</td>
<td style="border:1px solid black;">
[**MS13-086**](http://go.microsoft.com/fwlink/?linkid=324027)
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
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Excel 2010 Service Pack 1 (ediciones de 32 bits)  
(2826033)  
(Importante)  
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)  
(2826023)  
(Importante)  
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)  
(2826035)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Excel 2010 Service Pack 1 (ediciones de 64 bits)  
(2826033)  
(Importante)  
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)  
(2826023)  
(Importante)  
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)  
(2826035)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Excel 2010 Service Pack 2 (ediciones de 32 bits)  
(2826033)  
(Importante)  
Microsoft Office 2010 Service Pack 2 (ediciones de 32 bits)  
(2826023)  
(Importante)  
Microsoft Office 2010 Service Pack 2 (ediciones de 32 bits)  
(2826035)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Excel 2010 Service Pack 2 (ediciones de 64 bits)  
(2826033)  
(Importante)  
Microsoft Office 2010 Service Pack 2 (ediciones de 64 bits)  
(2826023)  
(Importante)  
Microsoft Office 2010 Service Pack 2 (ediciones de 64 bits)  
(2826035)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Office 2013
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-085**](http://go.microsoft.com/fwlink/?linkid=324026)
</td>
<td style="border:1px solid black;">
[**MS13-086**](http://go.microsoft.com/fwlink/?linkid=324027)
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
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2013 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Excel 2013 (ediciones de 32 bits)  
(2827238)  
(Importante)  
Microsoft Office 2013 (ediciones de 32 bits)  
(2817623)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2013 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Excel 2013 (ediciones de 64 bits)  
(2827238)  
(Importante)  
Microsoft Office 2013 (ediciones de 64 bits)  
(2817623)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2013 RT
</td>
<td style="border:1px solid black;">
Microsoft Excel 2013 RT  
(2827238)  
(Importante)  
Microsoft Office 2013 RT  
(2817623)  
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
[**MS13-085**](http://go.microsoft.com/fwlink/?linkid=324026)
</td>
<td style="border:1px solid black;">
[**MS13-086**](http://go.microsoft.com/fwlink/?linkid=324027)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office para Mac 2011
</td>
<td style="border:1px solid black;">
Microsoft Office para Mac 2011  
(2889496)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Otro software de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-085**](http://go.microsoft.com/fwlink/?linkid=324026)
</td>
<td style="border:1px solid black;">
[**MS13-086**](http://go.microsoft.com/fwlink/?linkid=324027)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office Service Pack 3
</td>
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office Service Pack 3  
(2827326)  
(Importante)
</td>
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office Service Pack 3  
(2827329)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Excel Viewer
</td>
<td style="border:1px solid black;">
Microsoft Excel Viewer  
(2827328)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 

#### Software de servidor de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft SharePoint Server 2007
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-084**](http://go.microsoft.com/fwlink/?linkid=324028)
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
Microsoft SharePoint Server 2007 Service Pack 3 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Windows SharePoint Services 3.0 Service Pack 3 (wssloc) (versiones de 32 bits)  
(2596741)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2007 Service Pack 3 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Windows SharePoint Services 3.0 Service Pack 3 (wssloc) (versiones de 64 bits)  
(2596741)  
(Importante)
</td>
</tr>
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
[**MS13-084**](http://go.microsoft.com/fwlink/?linkid=324028)
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
Microsoft SharePoint Foundation 2010 Service Pack 1 (wssloc)  
(2589365)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2010 Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Foundation 2010 Service Pack 2 (wssloc)  
(2589365)  
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
[**MS13-084**](http://go.microsoft.com/fwlink/?linkid=324028)
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
Microsoft SharePoint Server 2013 (pptserver)  
(2760561)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS13-084**

Vea también las demás categorías de esta sección, **Software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Microsoft Office Services y Web Apps

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft SharePoint Server 2007
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-084**](http://go.microsoft.com/fwlink/?linkid=324028)
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
Microsoft SharePoint Server 2007 Service Pack 3 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Excel Services  
(2827327)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2007 Service Pack 3 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Excel Services  
(2827327)  
(Importante)
</td>
</tr>
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
[**MS13-084**](http://go.microsoft.com/fwlink/?linkid=324028)
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
Excel Services  
(2826029)  
(Importante)  
Word Automation Services  
(2826022)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2010 Service Pack 2
</td>
<td style="border:1px solid black;">
Excel Services  
(2826029)  
(Importante)  
Word Automation Services  
(2826022)  
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
[**MS13-084**](http://go.microsoft.com/fwlink/?linkid=324028)
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
Excel Services  
(2752002)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2013
</td>
<td style="border:1px solid black;">
Word Automation Services  
(2826036)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Office Web Apps 2010
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-084**](http://go.microsoft.com/fwlink/?linkid=324028)
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
Microsoft Office Web Apps 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft Web Applications 2010 Service Pack 1  
(2826030)  
(Importante)  
Microsoft Excel Web App 2010 Service Pack 1  
(2826028)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office Web Apps 2010 Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft Web Applications 2010 Service Pack 2  
(2826030)  
(Importante)  
Microsoft Excel Web App 2010 Service Pack 2  
(2826028)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Office Web Apps 2013
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-084**](http://go.microsoft.com/fwlink/?linkid=324028)
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
Microsoft Office Web Apps 2013
</td>
<td style="border:1px solid black;">
Microsoft Office Web Apps Server 2013  
(2827222)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS13-084**

Vea también las demás categorías de esta sección, **Software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

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
[**MS13-087**](http://go.microsoft.com/fwlink/?linkid=324590)
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
Microsoft Silverlight 5
</td>
<td style="border:1px solid black;">
Microsoft Silverlight 5 cuando está instalado en Mac  
(2890788)  
(Importante)  
Microsoft Silverlight 5 Developer Runtime cuando está instalado en Mac  
(2890788)  
(Importante)  
Microsoft Silverlight 5 cuando está instalado en todas las versiones compatibles de los clientes Microsoft Windows  
(2890788)  
(Importante)  
Microsoft Silverlight 5 Developer Runtime cuando está instalado en todas las versiones compatibles de los clientes Microsoft Windows  
(2890788)  
(Importante)  
Microsoft Silverlight 5 cuando está instalado en todas las versiones compatibles de los servidores Microsoft Windows  
(2890788)  
(Importante)  
Microsoft Silverlight 5 Developer Runtime cuando está instalado en todas las versiones compatibles de los servidores Microsoft Windows  
(2890788)  
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

**MS13-080**

-   [Aniway.Anyway@gmail.com](mailto:aniway.anyway@gmail.com)
-   , en colaboración con
-   [Zero Day Initiative](http://www.zerodayinitiative.com/)
-   de
-   [HP](http://www.hpenterprisesecurity.com/products)
-   , por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3872)
-   José A. Vázquez, de Yenteasy - Security Research en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3873)
-   Amol Naik, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3874)
-   Un investigador anónimo, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2013-3874)
-   José A. Vázquez, de Yenteasy - Security Research en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3875)
-   Ivan Fratric, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3882)
-   José A. Vázquez, de Yenteasy - Security Research, por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3882)
-   José A. Vázquez, de Yenteasy - Security Research, por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3885)
-   José A. Vázquez, de Yenteasy - Security Research en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3886)
-   Yoshihiro Ishikawa, de [LAC Co.](http://www.lac.co.jp/), por colaborar con nosotros en la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3893)
-   Hoodie22, en colaboración con National Cyber Security Centre de Países Bajos, por colaborar con nosotros en la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3897)
-   Daniel Chechik, de Trustwave SpiderLabs Team, por colaborar con nosotros en la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3897)
-   Renato Ettisberger, de [IOprotect GmbH](http://ioprotect.ch/), por colaborar con nosotros en la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3897)

**MS13-081**

-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de análisis de fuentes OpenType (CVE-2013-3128)
-   Andy Davis, de [NCC Group](http://www.nccgroup.com/), por informar de la vulnerabilidad del descriptor de USB en Windows (CVE-2013-3200)
-   Lucas Bouillot, de ANSSI, por informar de la vulnerabilidad del descriptor de USB en Windows (CVE-2013-3200)
-   Seth Gibson y Dan Zentner, de [Endgame](http://www.endgame.com/), por informar de la vulnerabilidad de página nula en Win32k (CVE-2013-3881)
-   ZombiE, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de la tabla CMAP de fuentes TrueType (CVE-2013-3895)

**MS13-082**

-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de análisis de fuentes OpenType (CVE-2013-3128)
-   James Forshaw, de [Context Information Security](http://www.contextis.com/), por informar de la vulnerabilidad de expansión de entidades (CVE-2013-3860)

**MS13-083**

-   孙晓山, por informar de la vulnerabilidad de desbordamiento de enteros en Comctl32 (CVE-2013-3195)

**MS13-084**

-   Mateusz Jurczyk, Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Microsoft Excel (CVE-2013-3889)
-   Nutan kumar panda, por informar de la vulnerabilidad de inserción de parámetros (CVE-2013-3895)
-   Ari Elias-Bachrach y Angela Kelso, de [National Institutes of Health](http://nih.gov/), por colaborar con nosotros en los cambios de defensa en profundidad incluidos en este boletín.

**MS13-085**

-   Mateusz Jurczyk, Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Microsoft Excel (CVE-2013-3889)
-   Mateusz Jurczyk, Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Microsoft Excel (CVE-2013-3890)

**MS13-086**

-   Yuhong Bao, por informar de la vulnerabilidad de daños en la memoria (CVE-2013-3891)
-   Mateusz Jurczyk, Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria (CVE-2013-3892)

**MS13-087**

-   Vitaliy Toropov, por informar de la vulnerabilidad de Silverlight (CVE-2013-3896)

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Soluciones de seguridad para profesionales de TI: [Soporte técnico y solución de problemas de seguridad de TechNet](http://technet.microsoft.com/security/bb980617)
-   Ayuda para proteger su equipo con Windows de virus y malware: [Solución antivirus y centro de seguridad](http://support.microsoft.com/contactus/cu_sc_virsec_master)
-   Soporte local según su país: [Soporte internacional](http://support.microsoft.com/common/international.aspx)

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (8 de octubre de 2013): Publicación del resumen del boletín.
-   V1.1 (10 de octubre de 2013): para MS13-080, se ha quitado la evaluación de explotabilidad del índice de explotabilidad para CVE-2013-3871. La inclusión de este CVE en el índice explotabilidad original fue un error de documentación. CVE-2013-3871 está programado para corregirse en una actualización de seguridad futura. Se trata únicamente de un cambio informativo. Para MS13-082, se ha revisado el boletín para indicar que las instalaciones Server Core de Windows Server 2012 están afectadas por la vulnerabilidad corregida en la actualización 2861194. No había cambios en la lógica de detección ni en los archivos de actualización de seguridad. Los clientes que ya han actualizado correctamente sus sistemas no necesitan realizar ninguna acción.
-   V1.2 (6 de noviembre de 2013): para MS13-084, se ha corregido el nombre de producto de la actualización de Microsoft Office Web Apps Server 2013 (2827222).

*Built at 2014-04-18T01:50:00Z-07:00*
