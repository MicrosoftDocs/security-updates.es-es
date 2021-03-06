---
TOCTitle: 'MS14-SEP'
Title: Resumen del boletín de seguridad de Microsoft de septiembre de 2014
ms:assetid: 'ms14-sep'
ms:contentKeyID: 62841233
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms14-sep(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de septiembre de 2014
===================================================================

Publicado: 9 de septiembre de 2014

**Versión:** 1.0

Este resumen del boletín enumera los boletines de seguridad publicados para septiembre de 2014.

Con la publicación de los boletines de seguridad de septiembre de 2014, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 4 de septiembre de 2014. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar una difusión por web para atender las consultas de los clientes sobre estos boletines el 10 de septiembre de 2014, a las 11:00 a. m., hora del Pacífico (EE. UU. y Canadá). Para ver la difusión por web mensual y los vínculos a difusiones de los boletines de seguridad adicionales, vea [Difusión web del boletín de seguridad de Microsoft](http://technet.microsoft.com/security/dn756352).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

Resúmenes ejecutivos
--------------------

En la tabla siguiente se resumen los boletines de seguridad de este mes por orden de gravedad.

Para obtener detalles acerca del software afectado, vea la siguiente sección, **Software afectado**.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (2977629)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y treinta y seis vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un intruso que aprovechara estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los clientes cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507670">MS14-053</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en .NET Framework podría permitir la denegación de servicio (2990931)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft .NET Framework. La vulnerabilidad podría permitir la denegación de servicio si un atacante envía una pequeña cantidad de solicitudes especialmente diseñadas a un sitio web habilitado para .NET. De forma predeterminada, ASP.NET no se instala cuando Microsoft .NET Framework se instala en alguna edición compatible de Microsoft Windows. Para que se vean afectados por la vulnerabilidad, los clientes deben instalar y habilitar manualmente ASP.NET mediante su registro con IIS.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Denegación de servicio</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Microsoft .NET Framework</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507672">MS14-054</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Programador de tareas de Windows podría permitir la elevación de privilegios (2988948)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si un atacante inicia sesión en un sistema afectado y ejecuta una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local. Los usuarios anónimos o los usuarios remotos no pueden aprovechar esta vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507669">MS14-055</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Lync Server podrían permitir la denegación de servicio (2990928)</strong><br />
<br />
Esta actualización de seguridad resuelve tres vulnerabilidades de las que se ha informado de forma privada en Microsoft Lync Server. La más grave de estas vulnerabilidades podría permitir la denegación de servicio si un atacante envía una solicitud especialmente diseñada a un servidor Lync.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Denegación de servicio</td>
<td style="border:1px solid black;">No requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Lync Server</td>
</tr>
</tbody>
</table>
  
 
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y, a continuación, por identificador de CVE. Sólo se incluyen las vulnerabilidades que tiene una clasificación de gravedad de crítica o importante en los boletines.
  
¿Cómo se usa esta tabla?
  
Use esta tabla para obtener información acerca de la probabilidad de las vulnerabilidades de ejecución de código y de denegación de servicio en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Revise cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación de las actualizaciones de este mes. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/security/cc998259).
  
En las columnas siguientes, “Última versión de software” hace referencia al software en cuestión y “Versiones de software anteriores” hace referencia a todas las versiones anteriores y compatibles del software en cuestión, tal como se muestra en las tablas “Software afectado” y “Software no afectado” del boletín.
  
<p> </p>
<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de divulgación de información de recursos en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-7331">CVE-2013-7331</a></td>
<td style="border:1px solid black;">0: Vulnerabilidad detectada</td>
<td style="border:1px solid black;">0: Vulnerabilidad detectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente. Microsoft tiene constancia de ataques activos y limitados que intentan aprovechar esta vulnerabilidad.<br />
Esta vulnerabilidad afecta a la divulgación de información: el atacante puede deducir la presencia de archivos en las unidades locales.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2799">CVE-2014-2799</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4059">CVE-2014-4059</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4065">CVE-2014-4065</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4079">CVE-2014-4079</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4080">CVE-2014-4080</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4081">CVE-2014-4081</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4082">CVE-2014-4082</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4083">CVE-2014-4083</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4084">CVE-2014-4084</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4085">CVE-2014-4085</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4086">CVE-2014-4086</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4087">CVE-2014-4087</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4088">CVE-2014-4088</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4089">CVE-2014-4089</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4090">CVE-2014-4090</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4091">CVE-2014-4091</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4092">CVE-2014-4092</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4093">CVE-2014-4093</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4094">CVE-2014-4094</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4095">CVE-2014-4095</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4096">CVE-2014-4096</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4097">CVE-2014-4097</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4098">CVE-2014-4098</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4099">CVE-2014-4099</a></td>
<td style="border:1px solid black;">3: improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">3: improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">Esta vulnerabilidad de daños en la memoria podría provocar la denegación de servicio.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4100">CVE-2014-4100</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4101">CVE-2014-4101</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4102">CVE-2014-4102</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4103">CVE-2014-4103</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4104">CVE-2014-4104</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4105">CVE-2014-4105</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4106">CVE-2014-4106</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4107">CVE-2014-4107</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4108">CVE-2014-4108</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4109">CVE-2014-4109</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4110">CVE-2014-4110</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=509961">MS14-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4111">CVE-2014-4111</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507670">MS14-053</a></td>
<td style="border:1px solid black;">Vulnerabilidad de denegación de servicio en .NET Framework</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4072">CVE-2014-4072</a></td>
<td style="border:1px solid black;">3: improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">3: improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507672">MS14-054</a></td>
<td style="border:1px solid black;">Vulnerabilidad de Programador de tareas</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4074">CVE-2014-4074</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507669">MS14-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de denegación de servicio en Lync</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4068">CVE-2014-4068</a></td>
<td style="border:1px solid black;">3: improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">3: improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507669">MS14-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de divulgación de información de XSS en Lync</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4070">CVE-2014-4070</a></td>
<td style="border:1px solid black;">3: improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507669">MS14-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de denegación de servicio en Lync</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4071">CVE-2014-4071</a></td>
<td style="border:1px solid black;">3: improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">Temporal</td>
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
  
**Componentes y sistema operativo Windows**

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="4">
**Windows Server 2003**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-052**](http://go.microsoft.com/fwlink/?linkid=509961)
</td>
<td style="border:1px solid black;">
[**MS14-053**](http://go.microsoft.com/fwlink/?linkid=507670)
</td>
<td style="border:1px solid black;">
[**MS14-054**](http://go.microsoft.com/fwlink/?linkid=507672)
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
<td style="border:1px solid black;">
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 6  
(2977629)  
(Moderada)  
Internet Explorer 7  
(2977629)  
(Moderada)  
Internet Explorer 8  
(2977629)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 1.1 Service Pack 1  
(2972207)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2972214)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2973115)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972215)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 6  
(2977629)  
(Moderada)  
Internet Explorer 7  
(2977629)  
(Moderada)  
Internet Explorer 8  
(2977629)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2972214)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2973115)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972215)  
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
Internet Explorer 6  
(2977629)  
(Moderada)  
Internet Explorer 7  
(2977629)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2972214)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972215)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="4">
**Windows Vista**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-052**](http://go.microsoft.com/fwlink/?linkid=509961)
</td>
<td style="border:1px solid black;">
[**MS14-053**](http://go.microsoft.com/fwlink/?linkid=507670)
</td>
<td style="border:1px solid black;">
[**MS14-054**](http://go.microsoft.com/fwlink/?linkid=507672)
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
<td style="border:1px solid black;">
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2977629)  
(Crítica)  
Internet Explorer 8  
(2977629)  
(Crítica)  
Internet Explorer 9  
(2977629)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2974268)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2974269)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972215)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2972216)  
(Importante)
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
Internet Explorer 7  
(2977629)  
(Crítica)  
Internet Explorer 8  
(2977629)  
(Crítica)  
Internet Explorer 9  
(2977629)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2974268)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2974269)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972215)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2972216)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="4">
**Windows Server 2008**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-052**](http://go.microsoft.com/fwlink/?linkid=509961)
</td>
<td style="border:1px solid black;">
[**MS14-053**](http://go.microsoft.com/fwlink/?linkid=507670)
</td>
<td style="border:1px solid black;">
[**MS14-054**](http://go.microsoft.com/fwlink/?linkid=507672)
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
<td style="border:1px solid black;">
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2977629)  
(Moderada)  
Internet Explorer 8  
(2977629)  
(Moderada)  
Internet Explorer 9  
(2977629)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2974268)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2974269)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972215)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2972216)  
(Importante)
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
Internet Explorer 7  
(2977629)  
(Moderada)  
Internet Explorer 8  
(2977629)  
(Moderada)  
Internet Explorer 9  
(2977629)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2974268)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2974269)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972215)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2972216)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2977629)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2974268)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2974269)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972215)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="4">
**Windows 7**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-052**](http://go.microsoft.com/fwlink/?linkid=509961)
</td>
<td style="border:1px solid black;">
[**MS14-053**](http://go.microsoft.com/fwlink/?linkid=507670)
</td>
<td style="border:1px solid black;">
[**MS14-054**](http://go.microsoft.com/fwlink/?linkid=507672)
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
<td style="border:1px solid black;">
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2977629)  
(Crítica)  
Internet Explorer 9  
(2977629)  
(Crítica)  
Internet Explorer 10  
(2977629)  
(Crítica)  
Internet Explorer 11  
(2977629)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2972211)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2973112)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972215)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2972216)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2977629)  
(Crítica)  
Internet Explorer 9  
(2977629)  
(Crítica)  
Internet Explorer 10  
(2977629)  
(Crítica)  
Internet Explorer 11  
(2977629)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2972211)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2973112)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972215)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2972216)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="4">
**Windows Server 2008 R2**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-052**](http://go.microsoft.com/fwlink/?linkid=509961)
</td>
<td style="border:1px solid black;">
[**MS14-053**](http://go.microsoft.com/fwlink/?linkid=507670)
</td>
<td style="border:1px solid black;">
[**MS14-054**](http://go.microsoft.com/fwlink/?linkid=507672)
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
<td style="border:1px solid black;">
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2977629)  
(Moderada)  
Internet Explorer 9  
(2977629)  
(Moderada)  
Internet Explorer 10  
(2977629)  
(Moderada)  
Internet Explorer 11  
(2977629)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2972211)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2973112)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972215)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2972216)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2977629)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2972211)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2973112)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972215)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="4">
**Windows 8 y Windows 8.1**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-052**](http://go.microsoft.com/fwlink/?linkid=509961)
</td>
<td style="border:1px solid black;">
[**MS14-053**](http://go.microsoft.com/fwlink/?linkid=507670)
</td>
<td style="border:1px solid black;">
[**MS14-054**](http://go.microsoft.com/fwlink/?linkid=507672)
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
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2977629)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2972212)  
(Importante)  
Microsoft .NET Framework 3.5  
(2973113)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2977766)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2988948)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas x64
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2977629)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2972212)  
(Importante)  
Microsoft .NET Framework 3.5  
(2973113)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2977766)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(2988948)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2977629)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2972213)  
(Importante)  
Microsoft .NET Framework 3.5  
(2973114)  
(Importante)  
Microsoft .NET Framework 4.5.1/4.5.2  
(2977765)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(2988948)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2977629)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2972213)  
(Importante)  
Microsoft .NET Framework 3.5  
(2973114)  
(Importante)  
Microsoft .NET Framework 4.5.1/4.5.2  
(2977765)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(2988948)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="4">
**Windows Server 2012 y Windows Server 2012 R2**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-052**](http://go.microsoft.com/fwlink/?linkid=509961)
</td>
<td style="border:1px solid black;">
[**MS14-053**](http://go.microsoft.com/fwlink/?linkid=507670)
</td>
<td style="border:1px solid black;">
[**MS14-054**](http://go.microsoft.com/fwlink/?linkid=507672)
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
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2977629)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2972212)  
(Importante)  
Microsoft .NET Framework 3.5  
(2973113)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2977766)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2988948)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012 R2
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2977629)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2972213)  
(Importante)  
Microsoft .NET Framework 3.5  
(2973114)  
(Importante)  
Microsoft .NET Framework 4.5.1/4.5.2  
(2977765)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(2988948)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="4">
**Windows RT y Windows RT 8.1**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-052**](http://go.microsoft.com/fwlink/?linkid=509961)
</td>
<td style="border:1px solid black;">
[**MS14-053**](http://go.microsoft.com/fwlink/?linkid=507670)
</td>
<td style="border:1px solid black;">
[**MS14-054**](http://go.microsoft.com/fwlink/?linkid=507672)
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
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows RT
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2977629)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2977766)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT  
(2988948)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows RT 8.1
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2977629)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 4.5.1/4.5.2  
(2977765)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(2988948)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="4">
**Opción de instalación Server Core**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-052**](http://go.microsoft.com/fwlink/?linkid=509961)
</td>
<td style="border:1px solid black;">
[**MS14-053**](http://go.microsoft.com/fwlink/?linkid=507670)
</td>
<td style="border:1px solid black;">
[**MS14-054**](http://go.microsoft.com/fwlink/?linkid=507672)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**
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
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)
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
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)
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
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2972211)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2973112)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972215)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2972216)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
Microsoft .NET Framework 3.5  
(2972212)  
(Importante)  
Microsoft .NET Framework 3.5  
(2973113)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2977766)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(2988948)  
(Importante)
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
Microsoft .NET Framework 3.5  
(2972213)  
(Importante)  
Microsoft .NET Framework 3.5  
(2973114)  
(Importante)  
Microsoft .NET Framework 4.5.1/4.5.2  
(2977765)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(2988948)  
(Importante)
</td>
</tr>
</table>
 
 

**Software y plataformas de comunicaciones de Microsoft**

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
**Microsoft Lync Server**

</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-055**](http://go.microsoft.com/fwlink/?linkid=507669)
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
<tr>
<td style="border:1px solid black;">
Microsoft Lync Server 2010
</td>
<td style="border:1px solid black;">
Microsoft Lync Server 2010  
(Servidor)  
(2982385)  
(Sin clasificación de gravedad) <sup>[1]</sup>
Microsoft Lync Server 2010  
(Servicio de grupo de respuesta)  
(2982388)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync Server 2013
</td>
<td style="border:1px solid black;">
Microsoft Lync Server 2013  
(Servidor)  
(2986072)  
(Importante)  
Microsoft Lync Server 2013  
(Servicio de grupo de respuesta)  
(2982389)  
(Importante)  
Microsoft Lync Server 2013  
(Componentes principales)  
(2992965)  
(Importante)  
Microsoft Lync Server 2013  
(Web Components Server)  
(2982390)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS14-055**

<sup>[1]</sup>Las clasificaciones de gravedad no se aplican a esta actualización para el software especificado; no obstante, como medida de defensa en profundidad, Microsoft recomienda que los clientes de este software apliquen esta actualización de seguridad para protegerse de nuevos posibles ataques identificados en el futuro.

 

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

Hay disponibles varios recursos para ayudar a los administradores a implementar las actualizaciones de seguridad.

Microsoft Baseline Security Analyzer (MBSA) permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan y las configuraciones de seguridad incorrectas más comunes.

Windows Server Update Services (WSUS), Systems Management Server (SMS) y System Center Configuration Manager ayudan a los administradores a distribuir las actualizaciones de seguridad.

Los componentes del Evaluador de compatibilidad de aplicaciones incluidos con el kit de herramientas de compatibilidad de aplicaciones contribuyen a optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas.

Para obtener información acerca de estas y otras herramientas que hay disponibles, vea [Herramientas de seguridad para profesionales de TI](http://technet.microsoft.com/security/cc297183). 

Agradecimientos
---------------

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

**MS14-052**

-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2799)
-   [Adlab, de Venustech](http://www.venustech.com.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2799)
-   [Adlab, de Venustech](http://www.venustech.com.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4059)
-   AbdulAziz Hariri, de [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4065)
-   56e7aec02099b976120abfda31254b05, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4079)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4080)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4081)
-   [Adlab, de Venustech](http://www.venustech.com.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4081)
-   Yuki Chen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4082)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4082)
-   [Adlab, de Venustech](http://www.venustech.com.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4083)
-   [Adlab, de Venustech](http://www.venustech.com.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4084)
-   [KnownSec Team](http://www.knownsec.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4084)
-   Sky, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4085)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4086)
-   Liu Long, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4086)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4087)
-   Zhibin Hu, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4087)
-   Hui Gao, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4088)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4089)
-   Garage4Hackers, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4090)
-   Yuki Chen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4091)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4092)
-   A3F2160DCA1BDE70DA1D99ED267D5DC1EC336192, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4092)
-   Jason Kratzer, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4092)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4093)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4094)
-   Yuki Chen, de [Trend Micro](http://www.trendmicro.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-4095)
-   cloudfuzzer, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4096)
-   AbdulAziz Hariri, de [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4096)
-   Yuki Chen, de [Trend Micro](http://www.trendmicro.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-4096)
-   Yuki Chen, de [Trend Micro](http://www.trendmicro.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-4097)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4097)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4098)
-   SkyLined, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4099)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4100)
-   Xin Ouyang, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4101)
-   José A. Vázquez, de Yenteasy, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-4101)
-   Liu Long, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4102)
-   AbdulAziz Hariri, de [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4103)
-   Liu Long, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4104)
-   Yuki Chen, de [Trend Micro](http://www.trendmicro.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-4105)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4106)
-   AbdulAziz Hariri, de [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4107)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4108)
-   John Villamil (@day6reak), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4109)
-   [KnownSec Team](http://www.knownsec.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4110)
-   Yujie Wen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4111)
-   Masato Kinugawa y [Google Security Team](http://www.google.com/), por colaborar con nosotros en los cambios de defensa en profundidad incluidos en este boletín

**MS14-053**

-   Alexander Klink, de [Cynops GmbH](http://www.cynops.de/), por informar de la vulnerabilidad de denegación de servicio en .NET Framework (CVE-2014-4072)

**MS14-054**

-   James Forshaw, de [Context Information Security](http://www.contextis.com/), por informar de la vulnerabilidad de Programador de tareas (CVE-2014-4074)

**MS14-055**

-   Peter Schraffl, de [Telecommunication Software GmbH](http://www.telecomsoftware.com/), por informar de la vulnerabilidad de denegación de servicio en Lync (CVE-2014-4068)
-   Noam Rathaus, en colaboración con el equipo de [SecuriTeam Secure Disclosure](http://www.beyondsecurity.com/ssd.html) de Beyond Security, por informar de la vulnerabilidad de divulgación de información de XSS en Lync (CVE-2014-4070)

Información adicional:
----------------------

### Herramienta de eliminación de software malintencionado de Microsoft Windows

Para la publicación de boletines el segundo martes de cada mes, Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga. No hay disponible ninguna versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows para las publicaciones de boletín de seguridad fuera de ciclo.

### Actualizaciones no relacionadas con la seguridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Artículo 894199 de Microsoft Knowledge Base](https://support.microsoft.com/kb/894199): Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones de meses anteriores para Windows Server Update Services](http://technet.microsoft.com/wsus/bb456965). Muestra todas las actualizaciones nuevas, revisadas y publicadas de nuevo para los productos de Microsoft que no sean Microsoft Windows.

### Microsoft Active Protections Program (MAPP)

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumerados en [Asociados de Microsoft Active Protections Program (MAPP)](http://go.microsoft.com/fwlink/?linkid=215201).

### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de actualizaciones](http://go.microsoft.com/fwlink/?linkid=21168) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](https://support.microsoft.com/kb/913086).

**Comunidad de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [Comunidad de profesionales de TI de seguridad](http://go.microsoft.com/fwlink/?linkid=21164).

### Soporte técnico

El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).

Soluciones de seguridad para profesionales de TI: [Soporte técnico y solución de problemas de seguridad de TechNet](http://technet.microsoft.com/security/bb980617)

Ayuda para proteger su equipo con Windows de virus y malware: [Solución antivirus y centro de seguridad](http://support.microsoft.com/contactus/cu_sc_virsec_master)

Soporte local según su país: [Soporte internacional](http://support.microsoft.com/common/international.aspx)

### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra “tal cual”, sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

### Revisiones

-   V1.0 (9 de septiembre de 2014): Publicación del resumen del boletín.

*Página generada el 2014-09-18 16:20Z-07:00.*
