---
TOCTitle: 'MS08-DEC'
Title: Resumen del boletín de seguridad de Microsoft de diciembre 2008
ms:assetid: 'ms08-dec'
ms:contentKeyID: 61225386
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms08-dec(v=Security.10)'
--- 


Resumen del boletín de seguridad de Microsoft de diciembre 2008
===============================================================

Publicado: martes, 9 de diciembre de 2008 | Actualizado: miércoles, 29 de abril de 2009

**Versión:** 6.0

Este resumen del boletín enumera los boletines de seguridad publicados para diciembre de 2008.

Con la publicación de los boletines de diciembre de 2008, este resumen de boletín reemplaza la notificación de avance de boletines publicada originalmente el 4 de diciembre de 2008. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://technet.microsoft.com/security/bulletin/notify) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 10 de diciembre de 2008, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de diciembre](http://msevents.microsoft.com/cui/webcasteventdetails.aspx?eventid=1032374647). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

Para el boletín de seguridad fuera de ciclo agregado a la versión 3.0 de este resumen del boletín, MS08-078, Microsoft va a realizar dos webcasts para atender las consultas de los clientes sobre estos boletines: El 17 de diciembre de 2008, a la 1:00 p.m., hora del Pacífico (EE.UU. y Canadá) y el 18 de diciembre de 2008, a las 11:00 a.m., hora del Pacífico. Inscríbase ahora al [webcast del 17 de diciembre](http://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032399448&culture=en-us) y al [webcast del 18 de diciembre](http://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032399449&culture=en-us). Posteriormente, estos webcasts estarán disponibles a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-071">MS08-071</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en GDI podrían permitir la ejecución remota de código (956802)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en GDI. Si se aprovechan estas vulnerabilidades, se podría permitir la ejecución remota de código si un usuario abre un archivo de imagen WMF especialmente diseñado. Un atacante que aprovechara estas vulnerabilidades podría obtener el control completo del sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-075">MS08-075</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Búsqueda de Windows podrían permitir la ejecución remota de código (959349)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Búsqueda de Windows. Estas vulnerabilidades podrían permitir la ejecución remota de código si un usuario abre y guarda un archivo de búsqueda guardada especialmente diseñado en el Explorador de Windows o si hace clic en una dirección URL especialmente diseñada. Un atacante que aprovechara estas vulnerabilidades podría obtener el control completo del sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-073">MS08-073</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (958215)</strong><br />
<br />
Esta actualización de seguridad resuelve cuatro vulnerabilidades de las que se ha informado de forma privada. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-078">MS08-078</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad para Internet Explorer (960714)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública. La vulnerabilidad podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, Internet Explorer</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-070">MS08-070</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en los archivos extendidos de tiempo de ejecución de Visual Basic 6.0 (controles ActiveX) podrían permitir la ejecución remota de código (932349)</strong><br />
<br />
Esta actualización de seguridad resuelve cinco vulnerabilidades de las que se ha informado de forma privada y una vulnerabilidad de la que se ha informado de forma pública en los controles ActiveX para los archivos extendidos de tiempo de ejecución de Microsoft Visual Basic 6.0. Estas vulnerabilidades podrían permitir la ejecución remota de código si un usuario visita un sitio web que incluye contenido especialmente diseñado. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Herramientas y software para desarrolladores de Microsoft, Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-072">MS08-072</a></td>
<td style="border:1px solid black;"><strong>Las vulnerabilidades en los filtros de Microsoft Office podrían permitir la ejecución remota de código (957173)</strong><br />
<br />
Esta actualización de seguridad resuelve ocho vulnerabilidades de las que se ha informado de forma privada en Microsoft Office Word y Microsoft Office Outlook que podrían permitir la ejecución remota de código si un usuario abre un archivo de Word o RTF (formato de texto enriquecido) especialmente diseñado. Un atacante que aprovechara estas vulnerabilidades podría obtener el control completo del sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-074">MS08-074</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Office Excel podrían permitir la ejecución remota de código (959070)</strong><br />
<br />
Esta actualización de seguridad resuelve tres vulnerabilidades de las que se ha informado de forma privada en Microsoft Office Excel que podrían permitir la ejecución remota de código si un usuario abre un archivo de Excel especialmente diseñado. Un atacante que aprovechara estas vulnerabilidades podría obtener el control completo del sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-077">MS08-077</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Office SharePoint Server podría provocar la elevación de privilegios (957175)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada. La vulnerabilidad podría permitir la elevación de privilegios si un atacante omite la autenticación al examinar una dirección URL administrativa en un sitio de SharePoint. Un ataque que conlleve la elevación de privilegios podría provocar la denegación de servicio o la divulgación de información.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office, software de servidor de Microsoft</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-076">MS08-076</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en los componentes de Windows Media podrían permitir la ejecución remota de código (959807)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en los siguientes componentes de Windows Media: Reproductor de Windows Media, módulo de tiempo de ejecución de Windows Media Format y Servicios de Windows Media. La vulnerabilidad más grave podría permitir la ejecución de código remoto. Si un usuario inicia sesión con derechos de usuario administrativos, un intruso que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-070">MS08-070</a></td>
<td style="border:1px solid black;">Vulnerabilidades en los archivos extendidos de tiempo de ejecución de Visual Basic 6.0 (controles ActiveX) podrían permitir la ejecución remota de código (932349)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-3704">CVE-2008-3704</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">El código que aprovecha la vulnerabilidad está disponible de forma pública</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-070">MS08-070</a></td>
<td style="border:1px solid black;">Vulnerabilidades en los archivos extendidos de tiempo de ejecución de Visual Basic 6.0 (controles ActiveX) podrían permitir la ejecución remota de código (932349)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4252">CVE-2008-4252</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-070">MS08-070</a></td>
<td style="border:1px solid black;">Vulnerabilidades en los archivos extendidos de tiempo de ejecución de Visual Basic 6.0 (controles ActiveX) podrían permitir la ejecución remota de código (932349)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4256">CVE-2008-4256</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-070">MS08-070</a></td>
<td style="border:1px solid black;">Vulnerabilidades en los archivos extendidos de tiempo de ejecución de Visual Basic 6.0 (controles ActiveX) podrían permitir la ejecución remota de código (932349)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4253">CVE-2008-4253</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-070">MS08-070</a></td>
<td style="border:1px solid black;">Vulnerabilidades en los archivos extendidos de tiempo de ejecución de Visual Basic 6.0 (controles ActiveX) podrían permitir la ejecución remota de código (932349)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4254">CVE-2008-4254</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-070">MS08-070</a></td>
<td style="border:1px solid black;">Vulnerabilidades en los archivos extendidos de tiempo de ejecución de Visual Basic 6.0 (controles ActiveX) podrían permitir la ejecución remota de código (932349)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4255">CVE-2008-4255</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Los sistemas Windows 2000 están más expuestos. Es poco probable que Windows XP SP2, Windows Server 2003 SP1 y los sistemas operativos más recientes estén afectados por el código funcional que aproveche la vulnerabilidad debido a protecciones del montón más sólidas.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-071">MS08-071</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en GDI podría permitir la ejecución remota de código (956802)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-3465">CVE-2008-3465</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-071">MS08-071</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en GDI podría permitir la ejecución remota de código (956802)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-2249">CVE-2008-2249</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>3</strong></a> Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-072">MS08-072</a></td>
<td style="border:1px solid black;">Las vulnerabilidades en los filtros de Microsoft Office podrían permitir la ejecución remota de código (957173)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4024">CVE-2008-4024</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-072">MS08-072</a></td>
<td style="border:1px solid black;">Las vulnerabilidades en los filtros de Microsoft Office podrían permitir la ejecución remota de código (957173)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4025">CVE-2008-4025</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-072">MS08-072</a></td>
<td style="border:1px solid black;">Las vulnerabilidades en los filtros de Microsoft Office podrían permitir la ejecución remota de código (957173)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4026">CVE-2008-4026</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-072">MS08-072</a></td>
<td style="border:1px solid black;">Las vulnerabilidades en los filtros de Microsoft Office podrían permitir la ejecución remota de código (957173)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4027">CVE-2008-4027</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-072">MS08-072</a></td>
<td style="border:1px solid black;">Las vulnerabilidades en los filtros de Microsoft Office podrían permitir la ejecución remota de código (957173)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4028">CVE-2008-4028</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-072">MS08-072</a></td>
<td style="border:1px solid black;">Las vulnerabilidades en los filtros de Microsoft Office podrían permitir la ejecución remota de código (957173)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4030">CVE-2008-4030</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-072">MS08-072</a></td>
<td style="border:1px solid black;">Las vulnerabilidades en los filtros de Microsoft Office podrían permitir la ejecución remota de código (957173)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4837">CVE-2008-4837</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-072">MS08-072</a></td>
<td style="border:1px solid black;">Las vulnerabilidades en los filtros de Microsoft Office podrían permitir la ejecución remota de código (957173)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4031">CVE-2008-4031</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>3</strong></a> Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-073">MS08-073</a></td>
<td style="border:1px solid black;">Actualización de seguridad acumulativa para Internet Explorer (958215)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4258">CVE-2008-4258</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-073">MS08-073</a></td>
<td style="border:1px solid black;">Actualización de seguridad acumulativa para Internet Explorer (958215)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4259">CVE-2008-4259</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-073">MS08-073</a></td>
<td style="border:1px solid black;">Actualización de seguridad acumulativa para Internet Explorer (958215)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4261">CVE-2008-4261</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-073">MS08-073</a></td>
<td style="border:1px solid black;">Actualización de seguridad acumulativa para Internet Explorer (958215)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4260">CVE-2008-4260</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-074">MS08-074</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office Excel podrían permitir la ejecución remota de código (959070)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4265">CVE-2008-4265</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-074">MS08-074</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office Excel podrían permitir la ejecución remota de código (959070)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4266">CVE-2008-4266</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-074">MS08-074</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office Excel podrían permitir la ejecución remota de código (959070)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4264">CVE-2008-4264</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-075">MS08-075</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Búsqueda de Windows podrían permitir la ejecución remota de código (959349)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4269">CVE-2008-4269</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-075">MS08-075</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Búsqueda de Windows podrían permitir la ejecución remota de código (959349)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4268">CVE-2008-4268</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>2</strong></a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-076">MS08-076</a></td>
<td style="border:1px solid black;">Vulnerabilidades en los componentes de Windows Media podrían permitir la ejecución remota de código (959807)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-3009">CVE-2008-3009</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Se puede crear código funcional que aproveche la vulnerabilidad de este problema. No obstante, debido a la naturaleza limitada de los escenarios de ataque es poco probable que se produzcan ataques reales.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-076">MS08-076</a></td>
<td style="border:1px solid black;">Vulnerabilidades en los componentes de Windows Media podrían permitir la ejecución remota de código (959807)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-3010">CVE-2008-3010</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Se puede crear código funcional que aproveche la vulnerabilidad de este problema. No obstante, debido a la naturaleza limitada de los escenarios de ataque es poco probable que se produzcan ataques reales.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-077">MS08-077</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en Microsoft Office SharePoint Server podría provocar la elevación de privilegios (957175)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4032">CVE-2008-4032</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Se puede crear código funcional que aproveche la vulnerabilidad de este problema. No obstante, es probable que los ataques que aprovechen esta vulnerabilidad sólo tenga como resultado la divulgación de información y no la ejecución remota de código.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms08-078">MS08-078</a></td>
<td style="border:1px solid black;">Actualización de seguridad para Internet Explorer (960714)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4844">CVE-2008-4844</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx"><strong>1</strong></a> - Bastante probabilidad de código que aproveche la vulnerabilidad<br />
(Público en el momento de publicarse el boletín)</td>
<td style="border:1px solid black;">Se ha detectado código coherente que aprovecha la vulnerabilidad en ataques activos. No obstante, Internet Explorer se ejecuta en modo protegido con las instalaciones predeterminadas en Windows Vista y Windows Server 2008, lo que presenta obstáculos para aprovechar la vulnerabilidad.</td>
</tr>
</tbody>
</table>
  
Ubicaciones de descarga y software afectado  
-------------------------------------------
  
**¿Cómo se usa esta tabla?**  
  
Esta tabla se puede usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa o componente enumerado para ver si hay alguna actualización de seguridad necesaria. Si se enumera un programa o componente de software, se indica un hipervínculo a la actualización de software disponible y también se muestra la clasificación de gravedad de dicha actualización de software.
  
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
[**MS08-071**](http://technet.microsoft.com/security/bulletin/ms08-071)
</td>
<td style="border:1px solid black;">
[**MS08-075**](http://technet.microsoft.com/security/bulletin/ms08-075)
</td>
<td style="border:1px solid black;">
[**MS08-073**](http://technet.microsoft.com/security/bulletin/ms08-073)
</td>
<td style="border:1px solid black;">
[**MS08-078**](http://technet.microsoft.com/security/bulletin/ms08-078)
</td>
<td style="border:1px solid black;">
[**MS08-076**](http://technet.microsoft.com/security/bulletin/ms08-076)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=3b775fb1-1077-455d-af4a-4ccb5237974f)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 5.01 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=c242ba42-556b-4c87-bf33-9d99166ff096)  
(Crítica)  
[Microsoft Internet Explorer 6 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=c0583745-7e57-4265-9429-c3415cb8465f)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 5.01 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=d3e18732-47f1-40ce-999c-d1fd283bf138)  
(Crítica)  
[Microsoft Internet Explorer 6 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=124c14b6-9323-4f6f-902b-727aa56444bc)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Reproductor de Windows Media 6.4](http://www.microsoft.com/downloads/details.aspx?familyid=c33d558e-45f9-4e85-b48c-03bd0e8cb4bc)  
(KB954600)  
(Importante)  
[Módulo de tiempo de ejecución de Windows Media Format 7.1 y módulo de tiempo de ejecución de Windows Media Format 9.0](http://www.microsoft.com/downloads/details.aspx?familyid=6a459497-0ab8-41cb-87d0-b551631d8d8a)  
(KB952069)  
(Importante)  
[Servicios de Windows Media 4.1](http://www.microsoft.com/downloads/details.aspx?familyid=58b7d241-cef6-48fa-aa52-017695f71db1)  
(KB952068)  
(Importante)
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
[**MS08-071**](http://technet.microsoft.com/security/bulletin/ms08-071)
</td>
<td style="border:1px solid black;">
[**MS08-075**](http://technet.microsoft.com/security/bulletin/ms08-075)
</td>
<td style="border:1px solid black;">
[**MS08-073**](http://technet.microsoft.com/security/bulletin/ms08-073)
</td>
<td style="border:1px solid black;">
[**MS08-078**](http://technet.microsoft.com/security/bulletin/ms08-078)
</td>
<td style="border:1px solid black;">
[**MS08-076**](http://technet.microsoft.com/security/bulletin/ms08-076)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Service Pack 2 y Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=2151fbba-c464-4d1e-82d4-5b096e82bed0)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=af9a6cb0-725d-490c-9858-16ec40e98560)  
(Crítica)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=1b582695-b3cc-4c65-bc4b-d673c9a6d82a)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=1d83e0af-46fa-4bfc-ba57-635435a7ef2d)  
(Crítica)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=0190a289-164e-41a7-8c01-fa1aaed3f531)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Reproductor de Windows Media 6.4](http://www.microsoft.com/downloads/details.aspx?familyid=99241309-e644-4088-a8f3-38837fab4037)  
(KB954600)  
(Importante)  
[Módulo de tiempo de ejecución de Windows Media Format 9.0, módulo de tiempo de ejecución de Windows Media Format 9.5 y módulo de tiempo de ejecución de Windows Media Format 11](http://www.microsoft.com/downloads/details.aspx?familyid=504f816c-f554-4b93-ac28-b085574d9bac)  
(Windows XP Service Pack 2 solamente)  
(KB952069)  
(Importante)  
[Módulo de tiempo de ejecución de Windows Media Format 9.0, módulo de tiempo de ejecución de Windows Media Format 9.5 y módulo de tiempo de ejecución de Windows Media Format 11](http://www.microsoft.com/downloads/details.aspx?familyid=ad76fcf3-a2f9-4e36-bd1b-c1536749173c)  
(Windows XP Service Pack 3 solamente)  
(KB952069)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2247f6a5-aa33-4c68-9ea8-a63488d126d3)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=60bf9851-24fe-4658-8333-d353e82063c7)  
(Crítica)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=107cf54b-29d4-4c54-b091-2b5b3ffbf49d)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=a585cb73-2c1a-4fa8-862a-ad6aeaeaf2f8)  
(Crítica)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=9ba71e23-8cef-4399-b215-983b0dcf5cb5)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Reproductor de Windows Media 6.4](http://www.microsoft.com/downloads/details.aspx?familyid=946d47c9-b208-4fab-8ef6-774413d61bc8)  
(KB954600)  
(Importante)  
[Módulo de tiempo de ejecución de Windows Media Format 9.5](http://www.microsoft.com/downloads/details.aspx?familyid=644ef023-ee40-45b0-9c9d-c76d9fab0005)  
(KB952069)  
(Importante)  
[Módulo de tiempo de ejecución de Windows Media Format 9.5 x64 Edition](http://www.microsoft.com/downloads/details.aspx?familyid=ae9e8b07-5354-42f3-a226-ba2193244524)  
(KB952069)  
(Importante)  
[Módulo de tiempo de ejecución de Windows Media Format 11](http://www.microsoft.com/downloads/details.aspx?familyid=2dadc017-2be5-4240-ab8f-0291756dca6b)  
(KB952069)  
(Importante)
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
[**MS08-071**](http://technet.microsoft.com/security/bulletin/ms08-071)
</td>
<td style="border:1px solid black;">
[**MS08-075**](http://technet.microsoft.com/security/bulletin/ms08-075)
</td>
<td style="border:1px solid black;">
[**MS08-073**](http://technet.microsoft.com/security/bulletin/ms08-073)
</td>
<td style="border:1px solid black;">
[**MS08-078**](http://technet.microsoft.com/security/bulletin/ms08-078)
</td>
<td style="border:1px solid black;">
[**MS08-076**](http://technet.microsoft.com/security/bulletin/ms08-076)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=0c396796-0929-4cd2-99e8-3c0f7075a89e)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=d53adf6f-9501-4862-a1ca-57eb4d40cd75)  
(Moderada)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=9cdd4f9e-c578-405c-af9e-628f2d77fdf4)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=d81e9cf9-ce0c-463a-a359-49a348cb89ae)  
(Crítica)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=388847ec-817e-45cf-8fa7-32c7e1f57f80)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Reproductor de Windows Media 6.4](http://www.microsoft.com/downloads/details.aspx?familyid=2315ce20-2f46-42c2-bb40-045f003409d7)  
(KB954600)  
(Importante)  
[Módulo de tiempo de ejecución de Windows Media Format 9.5](http://www.microsoft.com/downloads/details.aspx?familyid=d8958248-c889-499e-a6a9-3b394cdb27ea)  
(KB952069)  
(Importante)  
[Servicios de Windows Media 9 Series](http://www.microsoft.com/downloads/details.aspx?familyid=e71abc2d-d60e-444a-9b7b-062c5805fe9e)  
(KB952068)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6d5c7d2f-1a82-4cdf-b3f2-b2c2390c6a64)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=5e37cb34-32be-4bbe-87f3-c4e1974e4d00)  
(Moderada)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=7c36f92c-d8a0-4b70-b85f-83588a0299a0)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=015df302-d79f-43a1-b5c5-32ac04de0510)  
(Crítica)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=2ae17caf-6204-470e-8480-380d3d505657)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Reproductor de Windows Media 6.4](http://www.microsoft.com/downloads/details.aspx?familyid=4c29bed9-1b88-4d2f-80a5-305c2bedd89f)  
(KB954600)  
(Importante)  
[Módulo de tiempo de ejecución de Windows Media Format 9.5](http://www.microsoft.com/downloads/details.aspx?familyid=2278022e-a716-46c0-bedf-d626933bd815)  
(KB952069)  
(Importante)  
[Módulo de tiempo de ejecución de Windows Media Format 9.5 x64 Edition](http://www.microsoft.com/downloads/details.aspx?familyid=ae9e8b07-5354-42f3-a226-ba2193244524)  
(KB952069)  
(Importante)  
[Servicios de Windows Media 9 Series](http://www.microsoft.com/downloads/details.aspx?familyid=e0030155-1a9a-46cc-bbc8-6d0d1ed65c1f)  
(KB952068)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=1edb62b4-3d0f-4891-b4b3-8f8bc4e7bdfe)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=0da4e424-4682-4401-a226-7d8f1be19d44)  
(Moderada)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=3811030d-5958-4b91-b5b8-20587dc7c4d6)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=18016305-7f72-47f6-ab4c-94282289bf5f)  
(Crítica)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=97d6c093-f68d-4ddf-8e3c-f29662a1940f)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
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
[**MS08-071**](http://technet.microsoft.com/security/bulletin/ms08-071)
</td>
<td style="border:1px solid black;">
[**MS08-075**](http://technet.microsoft.com/security/bulletin/ms08-075)
</td>
<td style="border:1px solid black;">
[**MS08-073**](http://technet.microsoft.com/security/bulletin/ms08-073)
</td>
<td style="border:1px solid black;">
[**MS08-078**](http://technet.microsoft.com/security/bulletin/ms08-078)
</td>
<td style="border:1px solid black;">
[**MS08-076**](http://technet.microsoft.com/security/bulletin/ms08-076)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista y Windows Vista Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows Vista y Windows Vista Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=cddf9cf6-bdeb-4429-823a-879387a428d7)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista y Windows Vista Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=0dcc5373-0435-42d5-864d-298e5bb122d9)  
(KB958623)  
(Importante)  
[Windows Vista y Windows Vista Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5b1b65f0-6848-47c6-bdd5-be3c0621b323)  
(KB958624)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=3f62030a-9ce2-4c92-b948-143a6881921e)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=7887111d-4fac-4823-bdd2-a18d9468fdf0)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Módulo de tiempo de ejecución de Windows Media Format 11](http://www.microsoft.com/downloads/details.aspx?familyid=1fcdc8dd-26d9-4d1a-8b3f-7b6a21a95999)  
(KB952069)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=73dc3775-b6f0-40f1-bd36-6b5fb80eb2fa)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=2112c5c8-7c9f-4491-b127-b1093085e105)  
(KB958623)  
(Importante)  
[Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=eb1d0ffe-1644-457b-9e82-768bd4c7f7ab)  
(KB958624)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=d8800493-fba4-41f8-bde5-a53eeaf89d54)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=69979d92-8d45-47fe-ac4c-c2f1f23cf1fb)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Módulo de tiempo de ejecución de Windows Media Format 11](http://www.microsoft.com/downloads/details.aspx?familyid=8839f6cd-dfbf-448c-bf1e-1da9bb5f3f25)  
(KB952069)  
(Importante)
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
[**MS08-071**](http://technet.microsoft.com/security/bulletin/ms08-071)
</td>
<td style="border:1px solid black;">
[**MS08-075**](http://technet.microsoft.com/security/bulletin/ms08-075)
</td>
<td style="border:1px solid black;">
[**MS08-073**](http://technet.microsoft.com/security/bulletin/ms08-073)
</td>
<td style="border:1px solid black;">
[**MS08-078**](http://technet.microsoft.com/security/bulletin/ms08-078)
</td>
<td style="border:1px solid black;">
[**MS08-076**](http://technet.microsoft.com/security/bulletin/ms08-076)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=bbed9e8b-e75e-44ef-ba1d-fd6f852c1f67)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=90ab7e6f-5ae7-4f55-8838-868fc98d8a16)\*\*\*  
(KB958623)  
(Importante)  
[Windows Server 2008 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=470d506f-77ae-4a44-8598-df645f484295)\*\*\*  
(KB958624)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=45a0de3c-c7d1-4314-a456-1f7428b7c90a)\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=5552e564-dd1c-4e2a-9a42-6317522c884d)\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Módulo de tiempo de ejecución de Windows Media Format 11](http://www.microsoft.com/downloads/details.aspx?familyid=91ec4195-bc1c-444e-a7b0-ebde46c088fa)  
(KB952069)  
(Importante)  
[Servicios de Windows Media 2008](http://www.microsoft.com/downloads/details.aspx?familyid=ffb5d945-7f98-4849-b020-ed4873fa42df)\*  
(KB952068)  
(Importante)
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
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Servicios de Windows Media 2008](http://www.microsoft.com/downloads/details.aspx?familyid=ffb5d945-7f98-4849-b020-ed4873fa42df)\*  
(KB952068)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=48aecf4c-1296-490d-ba37-a28e3ec19bd6)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=e1deab57-ada2-4b12-9157-5615e7b0071d)\*\*\*  
(KB958623)  
(Importante)  
[Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=e41f23e4-6a2f-4ebb-b425-d241a08da316)\*\*\*  
(KB958624)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=405b28db-47d7-4d6b-90e6-834c0a409323)\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=889c6eb1-7d1f-4e60-b637-535cb6e4e443)\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Módulo de tiempo de ejecución de Windows Media Format 11](http://www.microsoft.com/downloads/details.aspx?familyid=8cab6fe8-161d-4d8c-9772-eb3174a2c3c3)  
(KB952069)  
(Importante)  
[Servicios de Windows Media 2008](http://www.microsoft.com/downloads/details.aspx?familyid=0204a366-5641-4036-9cb0-a46d04af9d72)\*  
(KB952068)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
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
<td style="border:1px solid black;">
[Servicios de Windows Media 2008](http://www.microsoft.com/downloads/details.aspx?familyid=0204a366-5641-4036-9cb0-a46d04af9d72)\*  
(KB952068)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=9bfe15cd-02ff-45cf-85c8-5ff1e6c1a871)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=48bed90d-c243-4969-8e54-326d9a7af343)  
(KB958623)  
(Importante)  
[Windows Server 2008 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=83de2263-de2a-4c13-96ba-ecfebdaf0bb9)  
(KB958624)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=f0d4f321-941e-4da7-958f-582c75542ee8)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=06cb502a-6818-4599-aa24-6eddb83e4b84)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
**Nota para MS08-078**

La vulnerabilidad tratada en MS08-078 se notificó después del lanzamiento de Windows Internet Explorer 8 Beta 2. Se recomienda que los usuarios que ejecutan Windows Internet Explorer 8 Beta 2 descarguen y apliquen la actualización en sus sistemas.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://www.microsoft.com/downloads/search.aspx?displaylang=es). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

**Notas para Windows Server 2008**

**\*Instalación principal de servidor de Windows Server 2008 afectada.** Para ediciones compatibles de Windows Server 2008, esta actualización se aplica con la misma clasificación de gravedad, independientemente de si Windows Server 2008 se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**\*\*Instalación principal de servidor de Windows Server 2008 no afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 si Windows Server 2008 se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**\*\*\*Instalación principal de servidor de Windows Server 2008 no afectada.** Las vulnerabilidades corregidas por estas actualizaciones no afectan a las ediciones compatibles de Windows Server 2008 si Windows Server 2008 se ha instalado con la opción de instalación Server Core, aun cuando los archivos afectados por estas vulnerabilidades puedan estar presentes en el sistema. No obstante, a los usuarios con los archivos afectados se les sigue ofreciendo esta actualización porque los archivos de actualización son más recientes (con números de versión más altos) que los que se encuentran actualmente en el sistema. Para obtener más información acerca de esta opción de instalación, vea [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

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
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Conjuntos de programas, sistemas y componentes de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS08-070**](http://technet.microsoft.com/security/bulletin/ms08-070)
</td>
<td style="border:1px solid black;">
[**MS08-072**](http://technet.microsoft.com/security/bulletin/ms08-072)
</td>
<td style="border:1px solid black;">
[**MS08-074**](http://technet.microsoft.com/security/bulletin/ms08-074)
</td>
<td style="border:1px solid black;">
[**MS08-077**](http://technet.microsoft.com/security/bulletin/ms08-077)
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
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2000 Service Pack 3
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office Word 2000 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=43e8c4d8-307b-48f6-ac99-a9617421d40a)  
(KB956328)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2000 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=f39d2a49-f861-4f2d-bf91-94a8a85af40c)  
(KB958435)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office XP Service Pack 3
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office Word 2002 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=3ef41412-50b3-4077-b0e3-9a3704d2f876)  
(KB956329)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2002 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=72076e21-2aa3-48e8-883a-c3cb756fc72a)  
(KB958372)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
[Microsoft Office Word 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=45c81c60-4b1b-4246-839b-198ebc4eeae2)  
(KB956357)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=6c0771e5-fcd4-4365-b903-1a3bd95d9e66)  
(KB958436)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
2007 Microsoft Office System
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office Word 2007](http://www.microsoft.com/downloads/details.aspx?familyid=5b51cb5e-3899-4257-82cf-7e92fa619c37)  
(KB956358)  
(Importante)  
[Microsoft Office Outlook 2007](http://www.microsoft.com/downloads/details.aspx?familyid=5b51cb5e-3899-4257-82cf-7e92fa619c37)  
(KB956358)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2007](http://www.microsoft.com/downloads/details.aspx?familyid=68bb8d99-f28b-4efd-9314-3eee0bb00ccf)  
(KB958437)\*\*\*\*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
2007 Microsoft Office System Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office Word 2007 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5b51cb5e-3899-4257-82cf-7e92fa619c37)  
(KB956358)  
(Importante)  
[Microsoft Office Outlook 2007 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5b51cb5e-3899-4257-82cf-7e92fa619c37)  
(KB956358)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2007 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=68bb8d99-f28b-4efd-9314-3eee0bb00ccf)  
(KB958437)\*\*\*\*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office FrontPage
</td>
<td style="border:1px solid black;">
[Microsoft Office FrontPage 2002 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=0a6130ae-c5b4-43cb-afe3-ab6a55b9d9ea)\*  
(KB957797)  
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
<td style="border:1px solid black;">
Microsoft Office Project
</td>
<td style="border:1px solid black;">
[Microsoft Office Project 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=89a44042-a629-40f3-800a-0bb45fc36591)  
(KB949045)  
(Crítica)  
[Microsoft Office Project 2007](http://www.microsoft.com/downloads/details.aspx?familyid=2fbf6a5b-ff35-4a2d-9fa0-4e62b6486fe6)  
(KB949046)  
(Crítica)  
[Microsoft Office Project 2007 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=2fbf6a5b-ff35-4a2d-9fa0-4e62b6486fe6)  
(KB949046)  
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
Microsoft Office para Mac
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS08-070**](http://technet.microsoft.com/security/bulletin/ms08-070)
</td>
<td style="border:1px solid black;">
[**MS08-072**](http://technet.microsoft.com/security/bulletin/ms08-072)
</td>
<td style="border:1px solid black;">
[**MS08-074**](http://technet.microsoft.com/security/bulletin/ms08-074)
</td>
<td style="border:1px solid black;">
[**MS08-077**](http://technet.microsoft.com/security/bulletin/ms08-077)
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
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office 2004 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=eca13ad8-62ae-41a8-b308-41e2d1773820)\*\*  
(KB960402)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2004 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=eca13ad8-62ae-41a8-b308-41e2d1773820)\*\*  
(KB960402)  
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
[Microsoft Office 2008 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=ab31a564-43d2-45bd-98bf-19e9ca477b62)\*\*  
(KB960401)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2008 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=ab31a564-43d2-45bd-98bf-19e9ca477b62)\*\*  
(KB960401)  
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
No aplicable
</td>
<td style="border:1px solid black;">
[Convertidor de archivos con formatos XML abiertos para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=edb6cd8f-832c-4123-8982-ac0c601ea0a7)\*\*  
(KB960403)  
(Importante)
</td>
<td style="border:1px solid black;">
[Convertidor de archivos con formatos XML abiertos para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=edb6cd8f-832c-4123-8982-ac0c601ea0a7)\*\*  
(KB960403)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Otro software de Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS08-070**](http://technet.microsoft.com/security/bulletin/ms08-070)
</td>
<td style="border:1px solid black;">
[**MS08-072**](http://technet.microsoft.com/security/bulletin/ms08-072)
</td>
<td style="border:1px solid black;">
[**MS08-074**](http://technet.microsoft.com/security/bulletin/ms08-074)
</td>
<td style="border:1px solid black;">
[**MS08-077**](http://technet.microsoft.com/security/bulletin/ms08-077)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
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
Microsoft Works
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Works 8](http://www.microsoft.com/downloads/details.aspx?familyid=1537d181-90d9-4bb5-b5ae-8d9990a349af)\*\*\*  
(KB959487)  
(Importante)
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
Microsoft Office Excel Viewer
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel Viewer 2003](http://www.microsoft.com/downloads/details.aspx?familyid=4b3989ef-02b8-4bd2-b2ab-c3716079936e)  
(KB958434)  
(Importante)  
[Microsoft Office Excel Viewer 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=4b3989ef-02b8-4bd2-b2ab-c3716079936e)  
(KB958434)  
(Importante)  
[Microsoft Office Excel Viewer](http://www.microsoft.com/downloads/details.aspx?familyid=9dbb35c1-aa7a-481b-a330-8ba916ddd443)  
(KB958442)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Word Viewer
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office Word Viewer 2003 Service Pack 3 y Microsoft Office Word Viewer](http://www.microsoft.com/downloads/details.aspx?familyid=70de7c3c-519f-4f4a-a03f-027f80b5415c)  
(KB956366)  
(Importante)
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
Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007](http://www.microsoft.com/downloads/details.aspx?familyid=55430121-4476-48b8-9f6f-4a60fa0b2970)  
(KB956828)  
(Importante)  
[Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=55430121-4476-48b8-9f6f-4a60fa0b2970)  
(KB956828)  
(Importante)
</td>
<td style="border:1px solid black;">
[Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007](http://www.microsoft.com/downloads/details.aspx?familyid=99cca4ed-f1f9-4cfd-a986-edbec82ced4f)  
(KB958439)  
(Importante)  
[Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=99cca4ed-f1f9-4cfd-a986-edbec82ced4f)  
(KB958439)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office SharePoint Server 2007
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
[Microsoft Office SharePoint Server 2007 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=f8f73997-6f4c-4b43-aa50-5c8276e83d3e)  
(KB956716)  
(Importante)  
[Microsoft Office SharePoint Server 2007 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=f8f73997-6f4c-4b43-aa50-5c8276e83d3e)  
(KB956716)  
(Importante)  
[Microsoft Office SharePoint Server 2007 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=a7fda284-273c-42ab-8188-433beaacca86)  
(KB956716)  
(Importante)  
[Microsoft Office SharePoint Server 2007 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=a7fda284-273c-42ab-8188-433beaacca86)  
(KB956716)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS08-070**  
Vea también la siguiente sección, **Herramientas y software para desarrolladores de Microsoft**, para obtener más archivos de actualización. Este boletín abarca tanto Microsoft Office como las herramientas y software para desarrolladores de Microsoft

**Nota para MS08-077**  
Vea también la siguiente sección, **Software de servidor de Microsoft**, para obtener más archivos de actualización. Este boletín abarca tanto los conjuntos de aplicaciones y el software de Microsoft Office como el software de servidor de Microsoft.

**Nota para Microsoft Office FrontPage en MS08-070**  
\*Esta actualización sólo se aplica a las versión de FrontPage 2002 Service Pack 3 en chino simplificado (China), chino pan (Hong Kong), chino tradicional (Taiwán) y coreano.

**Nota para Microsoft Office para Mac in MS08-072 y MS08-074**  
\*\*Las actualizaciones correspondientes son idénticas entre MS08-072 y MS08-074. Debido a que las vulnerabilidades están en los mismos archivos, estas actualizaciones son las mismas para ambos boletines.

**Nota para Works 8 en MS08-072**  
\*\*\*Para recibir esta actualización de seguridad, los clientes que ejecuten Microsoft Works 8.0 primero deben actualizarse a Works 8.5, tal como se describe en [Microsoft Works Update](http://www.microsoft.com/products/works/international/update_1001.mspx). Esto incluye a todos los clientes que usen Microsoft Works 8.0, Works Suite 2004 y Works Suite 2005. Para los clientes que ejecuten Works Suite 2006, Works 8.5 ya está incluido.

**Nota para Microsoft Office Excel 2007 y Microsoft Office Excel 2007 Service Pack 1 en MS08-074**  
\*\*\*\*Para Microsoft Office Excel 2007 y Microsoft Office Excel 2007 Service Pack 1, además del paquete de actualización de seguridad KB958437, los clientes también deben instalar la actualización de seguridad para [Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007](http://www.microsoft.com/downloads/details.aspx?familyid=99cca4ed-f1f9-4cfd-a986-edbec82ced4f) (KB958439) con el fin de protegerse de las vulnerabilidades descritas en MS08-074. Los clientes que ya han instalado correctamente los paquetes de actualización KB958437 y KB958439 no tienen que reinstalarlos.

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
Visual Studio
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS08-070**](http://technet.microsoft.com/security/bulletin/ms08-070)
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
Microsoft Visual Basic
</td>
<td style="border:1px solid black;">
[Archivos extendidos de tiempo de ejecución de Microsoft Visual Basic 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=e27eebcb-095d-43ec-a19e-4a46e591715c)  
(KB926857)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Visual Studio .NET
</td>
<td style="border:1px solid black;">
[Microsoft Visual Studio .NET 2002 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=afad980d-7f27-49d9-aa23-b762c7b94cd6)  
(KB958392)  
(Crítica)  
[Microsoft Visual Studio .NET 2003 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=6ac7cf8f-d046-43a8-b4ef-253153d65aed)  
(KB958393)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Visual FoxPro
</td>
<td style="border:1px solid black;">
[Microsoft Visual FoxPro 8.0 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=a6977f81-f7f6-486b-96ad-8d296d79f205)  
(KB958369)  
(Crítica)  
[Microsoft Visual FoxPro 9.0 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=386d27a6-b2c7-4acc-bf3e-edcbc7358172)  
(KB958370)  
(Crítica)  
[Microsoft Visual FoxPro 9.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5b1f28a9-da8d-463a-8ae4-dfc8fcc6c41a)  
(KB958371)  
(Crítica)
</td>
</tr>
</table>
 
**Nota para MS08-070**  
Vea también la sección anterior, **Conjuntos de aplicaciones y software de Microsoft Office**, para obtener más archivos de actualización. Este boletín abarca tanto los conjuntos de aplicaciones y el software de Microsoft Office como las herramientas y el software para desarrolladores de Microsoft.

#### Software de servidor de Microsoft

 
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
Servidor Search
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS08-077**](http://technet.microsoft.com/security/bulletin/ms08-077)
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
Microsoft Search Server
</td>
<td style="border:1px solid black;">
[Microsoft Search Server 2008 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=f8f73997-6f4c-4b43-aa50-5c8276e83d3e)\*  
(KB956716)  
(Importante)  
[Microsoft Search Server 2008 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=a7fda284-273c-42ab-8188-433beaacca86)\*\*  
(KB956716)  
(Importante)
</td>
</tr>
</table>
 
**Notas para MS08-077**

\*Incluye Microsoft Search Server 2008 Express (32 bits)

\*\*Incluye Microsoft Search Server 2008 Express (64 bits)

Vea también la sección, **Conjuntos de aplicaciones y software de Microsoft Office**, para obtener más archivos de actualización. Este boletín abarca tanto los conjuntos de aplicaciones y el software de Microsoft Office como el software de servidor de Microsoft.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://go.microsoft.com/fwlink/?linkid=69903). [TechNet Security Center](http://go.microsoft.com/fwlink/?linkid=21171) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://www.microsoft.com/spain/athome/security/default.mspx), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747), [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130) y [Office Update](http://go.microsoft.com/fwlink/?linkid=21135). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://www.microsoft.com/downloads/search.aspx?displaylang=es). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como “MS07-036”), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

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

-   [Artículo 894199 de Microsoft Knowledge Base](http://support.microsoft.com/kb/894199): Cambios de contenido de Software Update Services y Windows Server Update Services para 2008. Incluye todo el contenido de Windows.
-   [Actualizaciones nuevas, revisadas y publicadas para productos de Microsoft distintos de Microsoft Windows](http://technet.microsoft.com/en-us/wsus/bb466214.aspx).

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

-   ADLab, de [VenusTech](http://www.venustech.com.cn/), por informar de varios problemas descritos en MS08-070
-   Jason Medeiros, de [Affiliated Computer Services](http://www.acs-inc.com/), por informar de un problema descrito en MS08-070
-   Carsten Eiram, de [Secunia Research](http://secunia.com/), por informar de un problema descrito en MS08-070
-   Mark Dowd, de [McAfee Avert Labs](http://www.avertlabs.com/), por informar de un problema descrito en MS08-070
-   Brett Moore, de [Insomnia Security](http://www.insomniasec.com/), por informar de un problema descrito en MS08-070
-   CHkr\_D591, en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS08-070
-   Michal Bucko, en colaboración con [CERT/CC](http://www.cert.org/), por informar de un problema descrito en MS08-070
-   El [equipo de análisis de inteligencia de seguridad](http://www.symantec.com/) de Symantec, por colaborar con nosotros en un problema descrito en MS08-070
-   Jun Mao, de [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS08-071
-   Juan Caballero, en colaboración con el [grupo Bitblaze en Carnegie Mellon University y UC Berkeley](http://bitblaze.cs.berkeley.edu/), por informar de un problema descrito en MS08-071
-   Ricardo Narvaja, de [Core Security Technologies](http://www.coresecurity.com/), por informar de un problema descrito en MS08-072
-   Dyon Balding, de [Secunia Research](http://secunia.com/), por informar de un problema descrito en MS08-072
-   Yamata Li, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de un problema descrito en MS08-072
-   Wushi, en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS08-072
-   Aaron Portnoy, de [TippingPoint DVLabs](http://dvlabs.tippingpoint.com/), por informar de un problema descrito en MS08-072
-   Wushi de [team509](http://www.team509.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS08-072
-   Wushi y Ling, en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS08-072
-   Carlo Di Dato (también conocido como shinnai), por informar de un problema descrito en MS08-073
-   Brett Moore, en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS08-073
-   Chris Weber, de [Casaba Security](http://www.casabasecurity.com/), por informar de un problema descrito en MS08-073
-   Jun Mao, de [Verisign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS08-073
-   Joshua J. Drake, de [Verisign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS08-074
-   Claes M Nyberg, de [signedness.org](http://www.signedness.org/), por informar de un problema descrito en MS08-074
-   Dyon Balding, de [Secunia](http://secunia.com/), por informar de un problema descrito en MS08-074
-   Andre Protas, de [eEye Digital Security](http://www.eeye.com/), por informar de un problema descrito en MS08-075
-   Nate McFeters, por informar de un problema descrito en MS08-075
-   Un investigador anónimo, por informar de un problema descrito en MS08-077

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Puede solicitar soporte técnico en los [Servicios de soporte técnico de Microsoft](http://support.microsoft.com/default.aspx?scid=fh;es-es;incidentsubmit) o a través del teléfono 902 197 198.
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (9 de diciembre de 2008): Publicación del resumen del boletín.
-   V2.0 (10 de diciembre de 2008): Se ha corregido el software afectado de MS08-076 para enumerar el módulo de tiempo de ejecución de Windows Media Format 9.5 y el módulo de tiempo de ejecución de Windows Media Format 11 como actualizaciones independientes en Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2. También se han quitado las referencias erróneas al módulo de tiempo de ejecución de Windows Media Format 11 x64 Edition en Windows XP Professional x64 Edition, Windows XP Professional x64 Edition Service Pack 2, Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2 para MS08-076.
-   V3.0 (17 de diciembre de 2008): Se ha agregado el boletín de seguridad de Microsoft MS08-078, Actualización de seguridad para Internet Explorer (960714). También se han agregado vínculos de webcast de boletín para este boletín de seguridad fuera de ciclo.
-   V3.1 (18 de diciembre de 2008): Para MS08-078, se ha agregado una anotación de Server Core no afectado para Windows Internet Explorer 7 en Windows Server 2008 para sistemas de 32 bits y en Windows Server 2008 para sistemas x64.
-   V3.2 (7 de enero de 2009): Se ha quitado Microsoft Office Word Viewer 2003 de la tabla Software afectado para MS08-072.
-   V4.0 (13 de enero de 2009): Microsoft ha vuelto a publicar MS08-076 para ofrecer nuevos paquetes de actualización para Módulo de tiempo de ejecución de Windows Media Format 9.5 en Windows XP Service Pack 2 (KB952069) y Windows XP Service Pack 3 (KB952069). Los clientes que ejecutan todas las demás versiones admitidas y afectadas de los componentes de Windows Media que ya hayan aplicado los paquetes de actualización de seguridad de MS08-076 originales no tienen que realizar ninguna acción. También se incluyen Reproductor de Windows Media 6.4 y Servicios de Windows Media 4.1 como afectados en todas las ediciones de Microsoft Windows 2000 Service Pack 4 para MS08-076; los clientes a los que se ha ofrecido esta actualización (KB954600 para Reproductor de Windows Media 6.4 o KB952068 para Servicios de Windows Media 4.1) pero no la han aplicado tienen que hacerlo. Por último, se ha incluido Microsoft Office Word Viewer como afectado para MS08-072; lo clientes que ya han instalado correctamente la actualización de seguridad KB956366 no tienen que volver a instalarla.
-   V5.0 (28 de enero de 2009): Se ha agregado una nota al pie para MS08-074 a la tabla **Software afectado** correspondiente a los paquetes de actualización de seguridad KB958437 y KB958439 para las versiones compatibles de Microsoft Office Excel 2007. No había cambios en los archivos binarios de la actualización de seguridad o en la detección. Los clientes con Microsoft Office Excel 2007 o Microsoft Office Excel 2007 Service Pack 1 que ya hayan instalado correctamente KB958437 y KB958439 no tienen que reinstalarlos.
-   V6.0 (29 de abril de 2009): Se ha agregado Windows Media Services 2008 (KB952068) en las ediciones de 32 bits y x64 de Windows Server 2008 Service Pack 2 como software afectado para MS08-076. Se trata únicamente de un cambio de detección; no había cambios en los archivos binarios. Los clientes que ya han instalado correctamente KB952068 no tienen que volver a instalarlo.

*Built at 2014-04-18T01:50:00Z-07:00*
