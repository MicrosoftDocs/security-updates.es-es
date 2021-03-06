---
TOCTitle: 'MS14-AUG'
Title: Resumen del boletín de seguridad de Microsoft de agosto de 2014
ms:assetid: 'ms14-aug'
ms:contentKeyID: 62757296
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms14-aug(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de agosto de 2014
===============================================================

Publicado: 12 de agosto de 2014 | Actualizado: 19 de diciembre de 2014

**Versión:** 2.2

Este resumen del boletín enumera los boletines de seguridad publicados para agosto de 2014.

Con la publicación de los boletines de seguridad de agosto de 2014, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 7 de agosto de 2014. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar una difusión por web para atender las consultas de los clientes sobre estos boletines el 13 de agosto de 2014, a las 11:00 a. m., hora del Pacífico (EE. UU. y Canadá). Para ver la difusión por web mensual y los vínculos a difusiones de los boletines de seguridad adicionales, vea [Difusión web del boletín de seguridad de Microsoft](http://technet.microsoft.com/security/dn756352).

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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (2976627)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y veinticinco vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un intruso que aprovechara estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los clientes cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507337">MS14-043</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Windows Media Center podría permitir la ejecución remota de código (2978742)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo de Microsoft Office especialmente diseñado que invoca recursos de Windows Media Center. Un atacante que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los clientes cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402461">MS14-048</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en OneNote podría permitir la ejecución remota de código (2977201)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft OneNote. La vulnerabilidad podría permitir la ejecución remota de código si se abre un archivo especialmente diseñado en una versión afectada de Microsoft OneNote. Un atacante que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los clientes cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507036">MS14-044</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en SQL Server podrían permitir la elevación de privilegios (2984340)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft SQL Server (una en SQL Server Servicios de datos Maestros y la otra en el sistema de administración de bases de datos relacionales de SQL Server). La más grave de estas vulnerabilidades, que afecta a SQL Server Master Data Services, podría permitir la elevación de privilegios si un usuario visita un sitio web especialmente diseñado que inserta un script del lado cliente en la instancia del usuario de Internet Explorer. El atacante no podría en ningún caso obligar a los usuarios a ver el contenido controlado por el atacante. En su lugar, tendría que convencerlos para que realizaran alguna acción, normalmente incitándoles a que hagan clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger que los lleve al sitio web del atacante o a que abran datos adjuntos enviados por correo electrónico.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft SQL Server</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507035">MS14-045</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en los controladores modo kernel podrían permitir la elevación de privilegios (2984615)</strong><br />
<br />
Esta actualización de seguridad resuelve tres vulnerabilidades de las que se ha informado de forma privada<strong></strong>en Microsoft Windows. La más grave de estas vulnerabilidades podría permitir la elevación de privilegios si un atacante inicia sesión en el sistema y ejecuta una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de aprovechar estas vulnerabilidades.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=396822">MS14-049</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el servicio Windows Installer podría permitir la elevación de privilegios (2962490)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad que se ha divulgado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si un atacante ejecuta una aplicación especialmente diseñada que intenta reparar una aplicación instalada anteriormente. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402463">MS14-050</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft SharePoint Server podría permitir la elevación de privilegios (2977202)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft SharePoint Server. Un atacante autenticado que aprovechara esta vulnerabilidad podría usar una aplicación especialmente diseñada para ejecutar código JavaScript arbitrario en el contexto del usuario en el sitio de SharePoint actual.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Software de servidor de Microsoft</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507038">MS14-046</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en .NET Framework podría permitir la omisión de característica de seguridad (2984625)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft .NET Framework. La vulnerabilidad podría permitir la omisión de característica de seguridad si un usuario visita un sitio web especialmente diseñado. En un escenario de ataque de exploración web, un atacante que aprovechara esta vulnerabilidad podría omitir la característica de seguridad de selección aleatoria del diseño del espacio de direcciones (ASLR), que contribuye a proteger a los usuarios de una amplia gama de vulnerabilidades. La omisión de la característica de seguridad en sí misma no permite la ejecución de código arbitrario. No obstante, un atacante podría usar esta vulnerabilidad de omisión de ASLR conjuntamente con otra vulnerabilidad, como la de ejecución remota de código, que pudiera aprovechar la omisión de ASLR para ejecutar código arbitrario.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Omisión de característica de seguridad</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Microsoft .NET Framework</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507336">MS14-047</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en LRPC podría permitir la omisión de característica de seguridad (2978668)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la omisión de característica de seguridad si un atacante usa la vulnerabilidad en combinación con otra vulnerabilidad, como una vulnerabilidad de ejecución remota de código, que aprovecha la omisión de ASLR para ejecutar código arbitrario.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Omisión de característica de seguridad</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507337">MS14-043</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de CSyncBasePlayer después de la liberación</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4060">CVE-2014-4060</a></td>
<td style="border:1px solid black;">2 - Poca probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">2 - Poca probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507036">MS14-044</a></td>
<td style="border:1px solid black;">Vulnerabilidad de XSS en SQL Master Data Services</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1820">CVE-2014-1820</a></td>
<td style="border:1px solid black;">2 - Poca probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507036">MS14-044</a></td>
<td style="border:1px solid black;">Vulnerabilidad de desbordamiento de la pila en Microsoft SQL Server</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4061">CVE-2014-4061</a></td>
<td style="border:1px solid black;">3 - Improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">3 - Improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507035">MS14-045</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0318">CVE-2014-0318</a></td>
<td style="border:1px solid black;">3 - Improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">3 - Improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507035">MS14-045</a></td>
<td style="border:1px solid black;">Vulnerabilidad de doble captura de fuentes</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1819">CVE-2014-1819</a></td>
<td style="border:1px solid black;">2 - Poca probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">2 - Poca probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507035">MS14-045</a></td>
<td style="border:1px solid black;">Vulnerabilidad de asignación de grupos en el kernel de Windows</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4064">CVE-2014-4064</a></td>
<td style="border:1px solid black;">3 - Improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">3 - Improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507038">MS14-046</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ASLR en .NET</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4062">CVE-2014-4062</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">2 - Poca probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Es una vulnerabilidad de omisión de característica de seguridad.<br />
<br />
En el momento de publicar este boletín de seguridad, Microsoft no había recibido ninguna información que indicara que esta vulnerabilidad se hubiera utilizado para atacar a clientes.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507336">MS14-047</a></td>
<td style="border:1px solid black;">Vulnerabilidad de omisión de ASLR en LRPC</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0316">CVE-2014-0316</a></td>
<td style="border:1px solid black;">3 - Improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">3 - Improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Es una vulnerabilidad de omisión de característica de seguridad.<br />
<br />
En el momento de publicar este boletín de seguridad, Microsoft no había recibido ninguna información que indicara que esta vulnerabilidad se hubiera utilizado para atacar a clientes.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402461">MS14-048</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código en OneNote</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2815">CVE-2014-2815</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">2 - Poca probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=396822">MS14-049</a></td>
<td style="border:1px solid black;">Vulnerabilidad de reparación de Windows Installer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1814">CVE-2014-1814</a></td>
<td style="border:1px solid black;">2 - Poca probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">2 - Poca probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402463">MS14-050</a></td>
<td style="border:1px solid black;">Vulnerabilidad de contenido de página en SharePoint</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2816">CVE-2014-2816</a></td>
<td style="border:1px solid black;">2 - Poca probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2774">CVE-2014-2774</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2784">CVE-2014-2784</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2796">CVE-2014-2796</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2808">CVE-2014-2808</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2810">CVE-2014-2810</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2811">CVE-2014-2811</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2817">CVE-2014-2817</a></td>
<td style="border:1px solid black;">0 - Vulnerabilidad detectada</td>
<td style="border:1px solid black;">0 - Vulnerabilidad detectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Microsoft tiene constancia de ataques limitados que intentan aprovechar esta vulnerabilidad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2818">CVE-2014-2818</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2819">CVE-2014-2819</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2820">CVE-2014-2820</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2821">CVE-2014-2821</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2822">CVE-2014-2822</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2823">CVE-2014-2823</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2824">CVE-2014-2824</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2825">CVE-2014-2825</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2826">CVE-2014-2826</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2827">CVE-2014-2827</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4050">CVE-2014-4050</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4051">CVE-2014-4051</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4052">CVE-2014-4052</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4055">CVE-2014-4055</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4056">CVE-2014-4056</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4057">CVE-2014-4057</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4058">CVE-2014-4058</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4063">CVE-2014-4063</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4067">CVE-2014-4067</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4145">CVE-2014-4145</a></td>
<td style="border:1px solid black;">1 - Mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507027">MS14-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-6354">CVE-2014-6354</a></td>
<td style="border:1px solid black;">1 - Mayor probabilidad de explotación</td>
<td style="border:1px solid black;">No afectado</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Ninguna</td>
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
<th colspan="7" style="border:1px solid black;">
Windows Server 2003
  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-051**](http://go.microsoft.com/fwlink/?linkid=507027)
</td>
<td style="border:1px solid black;">
[**MS14-043**](http://go.microsoft.com/fwlink/?linkid=507337)
</td>
<td style="border:1px solid black;">
[**MS14-045**](http://go.microsoft.com/fwlink/?linkid=507035)
</td>
<td style="border:1px solid black;">
[**MS14-049**](http://go.microsoft.com/fwlink/?linkid=396822)
</td>
<td style="border:1px solid black;">
[**MS14-046**](http://go.microsoft.com/fwlink/?linkid=507038)
</td>
<td style="border:1px solid black;">
[**MS14-047**](http://go.microsoft.com/fwlink/?linkid=507336)
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
**Ninguna**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 6  
(2976627)  
(Moderada)  
Internet Explorer 7  
(2976627)  
(Moderada)  
Internet Explorer 8  
(2976627)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(2993651)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(2918614)  
(Importante)
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
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 6  
(2976627)  
(Moderada)  
Internet Explorer 7  
(2976627)  
(Moderada)  
Internet Explorer 8  
(2976627)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2993651)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2918614)  
(Importante)
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
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
Internet Explorer 6  
(2976627)  
(Moderada)  
Internet Explorer 7  
(2976627)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2993651)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="7">
**Windows Vista**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-051**](http://go.microsoft.com/fwlink/?linkid=507027)
</td>
<td style="border:1px solid black;">
[**MS14-043**](http://go.microsoft.com/fwlink/?linkid=507337)
</td>
<td style="border:1px solid black;">
[**MS14-045**](http://go.microsoft.com/fwlink/?linkid=507035)
</td>
<td style="border:1px solid black;">
[**MS14-049**](http://go.microsoft.com/fwlink/?linkid=396822)
</td>
<td style="border:1px solid black;">
[**MS14-046**](http://go.microsoft.com/fwlink/?linkid=507038)
</td>
<td style="border:1px solid black;">
[**MS14-047**](http://go.microsoft.com/fwlink/?linkid=507336)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
(2976627)  
(Crítica)  
Internet Explorer 8  
(2976627)  
(Crítica)  
Internet Explorer 9  
(2976627)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2993651)  
(Importante)  
Windows Vista Service Pack 2  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2937608)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2943344)  
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
(2976627)  
(Crítica)  
Internet Explorer 8  
(2976627)  
(Crítica)  
Internet Explorer 9  
(2976627)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2993651)  
(Importante)  
Windows Vista x64 Edition Service Pack 2  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2937608)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2943344)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="7">
**Windows Server 2008**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-051**](http://go.microsoft.com/fwlink/?linkid=507027)
</td>
<td style="border:1px solid black;">
[**MS14-043**](http://go.microsoft.com/fwlink/?linkid=507337)
</td>
<td style="border:1px solid black;">
[**MS14-045**](http://go.microsoft.com/fwlink/?linkid=507035)
</td>
<td style="border:1px solid black;">
[**MS14-049**](http://go.microsoft.com/fwlink/?linkid=396822)
</td>
<td style="border:1px solid black;">
[**MS14-046**](http://go.microsoft.com/fwlink/?linkid=507038)
</td>
<td style="border:1px solid black;">
[**MS14-047**](http://go.microsoft.com/fwlink/?linkid=507336)
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
**Ninguna**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
(2976627)  
(Moderada)  
Internet Explorer 8  
(2976627)  
(Moderada)  
Internet Explorer 9  
(2976627)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2993651)  
(Importante)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2937608)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2943344)  
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
(2976627)  
(Moderada)  
Internet Explorer 8  
(2976627)  
(Moderada)  
Internet Explorer 9  
(2976627)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2993651)  
(Importante)  
Windows Server 2008 para sistemas x64 Service Pack 2  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2937608)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2943344)  
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
(2976627)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2993651)  
(Importante)  
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2937608)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2943344)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="7">
**Windows 7**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-051**](http://go.microsoft.com/fwlink/?linkid=507027)
</td>
<td style="border:1px solid black;">
[**MS14-043**](http://go.microsoft.com/fwlink/?linkid=507337)
</td>
<td style="border:1px solid black;">
[**MS14-045**](http://go.microsoft.com/fwlink/?linkid=507035)
</td>
<td style="border:1px solid black;">
[**MS14-049**](http://go.microsoft.com/fwlink/?linkid=396822)
</td>
<td style="border:1px solid black;">
[**MS14-046**](http://go.microsoft.com/fwlink/?linkid=507038)
</td>
<td style="border:1px solid black;">
[**MS14-047**](http://go.microsoft.com/fwlink/?linkid=507336)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2976627)  
(Crítica)  
Internet Explorer 9  
(2976627)  
(Crítica)  
Internet Explorer 10  
(2976627)  
(Crítica)  
Internet Explorer 11  
(2976627)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(todas las ediciones excepto Starter y Home Basic)  
(2978742)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2993651)  
(Importante)  
Windows 7 para sistemas de 32 bits Service Pack 1  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2937610)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2943357)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2978668)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2976627)  
(Crítica)  
Internet Explorer 9  
(2976627)  
(Crítica)  
Internet Explorer 10  
(2976627)  
(Crítica)  
Internet Explorer 11  
(2976627)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(todas las ediciones excepto Starter y Home Basic)  
(2978742)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2993651)  
(Importante)  
Windows 7 para sistemas x64 Service Pack 1  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2937610)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2943357)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2978668)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="7">
**Windows Server 2008 R2**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-051**](http://go.microsoft.com/fwlink/?linkid=507027)
</td>
<td style="border:1px solid black;">
[**MS14-043**](http://go.microsoft.com/fwlink/?linkid=507337)
</td>
<td style="border:1px solid black;">
[**MS14-045**](http://go.microsoft.com/fwlink/?linkid=507035)
</td>
<td style="border:1px solid black;">
[**MS14-049**](http://go.microsoft.com/fwlink/?linkid=396822)
</td>
<td style="border:1px solid black;">
[**MS14-046**](http://go.microsoft.com/fwlink/?linkid=507038)
</td>
<td style="border:1px solid black;">
[**MS14-047**](http://go.microsoft.com/fwlink/?linkid=507336)
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
**Ninguna**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2976627)  
(Moderada)  
Internet Explorer 9  
(2976627)  
(Moderada)  
Internet Explorer 10  
(2976627)  
(Moderada)  
Internet Explorer 11  
(2976627)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2993651)  
(Importante)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2937610)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2943357)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2978668)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2976627)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2993651)  
(Importante)  
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2937610)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2943357)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2978668)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="7">
**Windows 8 y Windows 8.1**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-051**](http://go.microsoft.com/fwlink/?linkid=507027)
</td>
<td style="border:1px solid black;">
[**MS14-043**](http://go.microsoft.com/fwlink/?linkid=507337)
</td>
<td style="border:1px solid black;">
[**MS14-045**](http://go.microsoft.com/fwlink/?linkid=507035)
</td>
<td style="border:1px solid black;">
[**MS14-049**](http://go.microsoft.com/fwlink/?linkid=396822)
</td>
<td style="border:1px solid black;">
[**MS14-046**](http://go.microsoft.com/fwlink/?linkid=507038)
</td>
<td style="border:1px solid black;">
[**MS14-047**](http://go.microsoft.com/fwlink/?linkid=507336)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
(2976627)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Media Center cuando está instalado en Windows 8 para sistemas de 32 bits (solo Professional Edition)  
(2978742)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2993651)  
(Importante)  
Windows 8 para sistemas de 32 bits  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2966825)  
(Importante)  
Microsoft .NET Framework 3.5  
(2966827)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2978668)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas x64
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2976627)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Media Center cuando está instalado en Windows 8 para sistemas x64 (solo Professional Edition)  
(2978742)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(2993651)  
(Importante)  
Windows 8 para sistemas x64  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2966825)  
(Importante)  
Microsoft .NET Framework 3.5  
(2966827)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(2978668)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2976627)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Media Center cuando está instalado en Windows 8.1 para sistemas de 32 bits (solo Professional Edition)  
(2978742)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(2993651)  
(Importante)  
Windows 8.1 para sistemas de 32 bits  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2966826)  
(Importante)  
Microsoft .NET Framework 3.5  
(2966828)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(2978668)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2976627)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Media Center cuando está instalado en Windows 8.1 para sistemas x64 (solo Professional Edition)  
(2978742)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(2993651)  
(Importante)  
Windows 8.1 para sistemas x64  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2966826)  
(Importante)  
Microsoft .NET Framework 3.5  
(2966828)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(2978668)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="7">
**Windows Server 2012 y Windows Server 2012 R2**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-051**](http://go.microsoft.com/fwlink/?linkid=507027)
</td>
<td style="border:1px solid black;">
[**MS14-043**](http://go.microsoft.com/fwlink/?linkid=507337)
</td>
<td style="border:1px solid black;">
[**MS14-045**](http://go.microsoft.com/fwlink/?linkid=507035)
</td>
<td style="border:1px solid black;">
[**MS14-049**](http://go.microsoft.com/fwlink/?linkid=396822)
</td>
<td style="border:1px solid black;">
[**MS14-046**](http://go.microsoft.com/fwlink/?linkid=507038)
</td>
<td style="border:1px solid black;">
[**MS14-047**](http://go.microsoft.com/fwlink/?linkid=507336)
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
**Ninguna**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
(2976627)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2993651)  
(Importante)  
Windows Server 2012  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2966825)  
(Importante)  
Microsoft .NET Framework 3.5  
(2966827)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2978668)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012 R2
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2976627)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(2993651)  
(Importante)  
Windows Server 2012 R2  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2966826)  
(Importante)  
Microsoft .NET Framework 3.5  
(2966828)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(2978668)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="7">
**Windows RT y Windows RT 8.1**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-051**](http://go.microsoft.com/fwlink/?linkid=507027)
</td>
<td style="border:1px solid black;">
[**MS14-043**](http://go.microsoft.com/fwlink/?linkid=507337)
</td>
<td style="border:1px solid black;">
[**MS14-045**](http://go.microsoft.com/fwlink/?linkid=507035)
</td>
<td style="border:1px solid black;">
[**MS14-049**](http://go.microsoft.com/fwlink/?linkid=396822)
</td>
<td style="border:1px solid black;">
[**MS14-046**](http://go.microsoft.com/fwlink/?linkid=507038)
</td>
<td style="border:1px solid black;">
[**MS14-047**](http://go.microsoft.com/fwlink/?linkid=507336)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows RT
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2976627)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows RT  
(2993651)  
(Importante)  
Windows RT  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows RT  
(2978668)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows RT 8.1
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2976627)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(2993651)  
(Importante)  
Windows RT 8.1  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(2978668)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="7">
**Opción de instalación Server Core**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-051**](http://go.microsoft.com/fwlink/?linkid=507027)
</td>
<td style="border:1px solid black;">
[**MS14-043**](http://go.microsoft.com/fwlink/?linkid=507337)
</td>
<td style="border:1px solid black;">
[**MS14-045**](http://go.microsoft.com/fwlink/?linkid=507035)
</td>
<td style="border:1px solid black;">
[**MS14-049**](http://go.microsoft.com/fwlink/?linkid=396822)
</td>
<td style="border:1px solid black;">
[**MS14-046**](http://go.microsoft.com/fwlink/?linkid=507038)
</td>
<td style="border:1px solid black;">
[**MS14-047**](http://go.microsoft.com/fwlink/?linkid=507336)
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
**Ninguna**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2993651)  
(Importante)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2918614)  
(Importante)
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
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2993651)  
(Importante)  
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2918614)  
(Importante)
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
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2993651)  
(Importante)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2937610)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2943357)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2978668)  
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
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(2993651)  
(Importante)  
Windows Server 2012 (instalación Server Core)  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2966825)  
(Importante)  
Microsoft .NET Framework 3.5  
(2966827)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(2978668)  
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
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(2993651)  
(Importante)  
Windows Server 2012 R2 (instalación Server Core)  
(2976897)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(2918614)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2966826)  
(Importante)  
Microsoft .NET Framework 3.5  
(2966828)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(2978668)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS14-043**

Este boletín abarca varias categorías de software. Vea las demás tablas de esta sección para determinar el software afectado.

 

**Software de Microsoft Office**

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
**Software de Microsoft Office**

</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-048**](http://go.microsoft.com/fwlink/?linkid=402461)
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
Microsoft OneNote 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft OneNote 2007 Service Pack 3  
(2596857)  
(Importante)
</td>
</tr>
</table>
 
 

**Microsoft SQL Server**

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="2">
**SQL Server 2008**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-044**](http://go.microsoft.com/fwlink/?linkid=507036)
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
Microsoft SQL Server 2008 para sistemas de 32 bits Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 para sistemas de 32 bits Service Pack 3  
(GDR)  
(2977321)  
(Importante)  
Microsoft SQL Server 2008 para sistemas de 32 bits Service Pack 3  
(QFE)  
(2977322)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 para sistemas x64 Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 para sistemas x64 Service Pack 3  
(GDR)  
(2977321)  
(Importante)  
Microsoft SQL Server 2008 para sistemas x64 Service Pack 3  
(QFE)  
(2977322)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 para sistemas con Itanium Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 para sistemas con Itanium Service Pack 3  
(GDR)  
(2977321)  
(Importante)  
Microsoft SQL Server 2008 para sistemas con Itanium Service Pack 3  
(QFE)  
(2977322)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="2">
**SQL Server 2008 R2**
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
Microsoft SQL Server 2008 R2 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 R2 para sistemas de 32 bits Service Pack 2  
(GDR)  
2977320)  
(Importante)  
Microsoft SQL Server 2008 R2 para sistemas de 32 bits Service Pack 2  
(QFE)  
(2977319)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 R2 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 R2 para sistemas x64 Service Pack 2  
(GDR)  
(2977320)  
(Importante)  
Microsoft SQL Server 2008 R2 para sistemas x64 Service Pack 2  
(QFE)  
(2977319)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 R2 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 R2 para sistemas con Itanium Service Pack 2  
(GDR)  
(2977320)  
(Importante)  
Microsoft SQL Server 2008 R2 para sistemas con Itanium Service Pack 2  
(QFE)  
(2977319)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="2">
**SQL Server 2012**
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
Microsoft SQL Server 2012 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft SQL Server 2012 para sistemas de 32 bits Service Pack 1  
(GDR)  
(2977326)  
(Importante)  
Microsoft SQL Server 2012 para sistemas de 32 bits Service Pack 1  
(QFE)  
(2977325)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2012 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft SQL Server 2012 para sistemas x64 Service Pack 1  
(GDR)  
(2977326)  
(Importante)  
Microsoft SQL Server 2012 para sistemas x64 Service Pack 1  
(QFE)  
(2977325)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="2">
**SQL Server 2014**
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
Microsoft SQL Server 2014 para sistemas x64
</td>
<td style="border:1px solid black;">
Microsoft SQL Server 2014 para sistemas x64  
(GDR)  
(2977315)  
(Importante)  
Microsoft SQL Server 2014 para sistemas x64  
(QFE)  
(2977316)  
(Importante)
</td>
</tr>
</table>
 
 

**Software de servidor de Microsoft**

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="2">
**Microsoft SharePoint Server**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-050**](http://go.microsoft.com/fwlink/?linkid=402463)
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
Microsoft SharePoint Server 2013
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2013  
(2880994)  
(Importante)  
Microsoft SharePoint Foundation 2013  
(2880994)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2013 Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2013 Service Pack 1  
(2880994)  
(Importante)  
Microsoft SharePoint Foundation 2013 Service Pack 1  
(2880994)  
(Importante)
</td>
</tr>
</table>
 
 

**Otro software**

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="2">
**Windows Media Center TV Pack para Windows Vista**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-043**](http://go.microsoft.com/fwlink/?linkid=507337)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Media Center TV Pack para Windows Vista (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Windows Media Center TV Pack para Windows Vista (ediciones de 32 bits)  
(2978742)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Media Center TV Pack para Windows Vista (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Windows Media Center TV Pack para Windows Vista (ediciones de 64 bits)  
(2978742)  
(Crítica)
</td>
</tr>
</table>
 
**Nota para MS14-043**

Este boletín abarca varias categorías de software. Vea las demás tablas de esta sección para determinar el software afectado.

 

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

**MS14-043**

-   Alisa Esage (@alisaesage), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad en el uso de CSyncBasePlayer después de la liberación (CVE-2014-4060)

**MS14-045**

-   Wang Yu, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de doble captura de fuentes (CVE-2014-1819)
-   Ilja Van Sprundel, por informar de la vulnerabilidad de asignación de grupos en el kernel de Windows (CVE-2014-4064)

**MS14-047**

-   [Alex Ionescu](http://www.alex-ionescu.com/), por informar de la vulnerabilidad de omisión de ASLR en LRPC (CVE-2014-0316)

**MS14-048**

-   Eduardo Prado, en colaboración con el programa [SecuriTeam Secure Disclosure](http://www.beyondsecurity.com/ssd.html) de Beyond Security, por informar de la vulnerabilidad de ejecución remota de código en OneNote (CVE-2014-2815)

**MS14-049**

-   Denis Gundarev, de [Entisys](http://www.entisys.com/), por informar de la vulnerabilidad de reparación de Windows Installer (CVE-2012-4784)
-   [Stepfan Kanthak](http://home.arcor.de/skanthak/safer.html), por colaborar con nosotros en los cambios de defensa en profundidad incluidos en este boletín

**MS14-051**

-   AbdulAziz Hariri, de [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2774)
-   Yujie Wen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2784)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2796)
-   [Chen Zhang (demi6od)](https://github.com/demi6od), de [NSFOCUS Security Team](http://www.nsfocus.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2808)
-   [Chen Zhang (demi6od)](https://github.com/demi6od), de [NSFOCUS Security Team](http://www.nsfocus.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2810)
-   IronRock, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2811)
-   James Forshaw, de [Context Information Security](http://www.contextis.com/), por informar de la vulnerabilidad de elevación de privilegios en Internet Explorer (CVE-2014-2817)
-   AbdulAziz Hariri, de [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2818)
-   Zeguang Zhao, de [Team509](http://team509.com/), y Liang Chen, de [KeenTeam](http://www.k33nteam.org/) (@K33nTeam), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de elevación de privilegios en Internet Explorer (CVE-2014-2819)
-   Arthur Gerkis, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2820)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2821)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2822)
-   [Chen Zhang (demi6od)](https://github.com/demi6od), de [NSFOCUS Security Team](http://www.nsfocus.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2823)
-   Yuki Chen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2824)
-   [Chen Zhang (demi6od)](https://github.com/demi6od), de [NSFOCUS Security Team](http://www.nsfocus.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2825)
-   [Chen Zhang (demi6od)](https://github.com/demi6od), de [NSFOCUS Security Team](http://www.nsfocus.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2826)
-   Simon Zuckerbraun, de [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2827)
-   [Omair](http://krash.in/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-4050)
-   Peter 'corelanc0d3r' Van Eeckhoutte, de [Corelan](http://www.corelangcv.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4051)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4052)
-   Simon Zuckerbraun, de [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4055)
-   Peter 'corelanc0d3r' Van Eeckhoutte, de [Corelan](http://www.corelangcv.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4056)
-   Yuki Chen, de [Trend Micro](http://www.trendmicro.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-4057)
-   Sky, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4058)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4063)
-   Wei Wang, de [VulnHunt](http://www.vulnhunt.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4067)
-   [lokihardt@ASRT](https://technet.microsoft.com/es-ES/mailto:lokihardt@asrt), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4067)
-   Omair, junto con la [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products) para la generación de informes de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-4145)
-   Omair, junto con la [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products) para la generación de informes de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-6354)

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

-   V1.0 (12 de agosto de 2014): Publicación del resumen del boletín.
-   V2.0 (27 de agosto de 2014): para MS14-045, se ha vuelto a publicar el boletín para anunciar el reemplazo de la actualización 2982791 por la actualización 2993651 para todas las versiones compatibles de Microsoft Windows. Consulte el boletín para obtener detalles.
-   V2.1 (8 de octubre de 2014): para MS14-051, se ha corregido la evaluación de explotabilidad en Índice de explotabilidad para CVE-2014-4145. Se trata únicamente de un cambio informativo.
-   V2.2 (19 de diciembre de 2014): Para MS14-051, agregada una evaluación de explotabilidad en el índice de explotabilidad para CVE-2014-6354. Esto es solo un cambio informativo.

*Página generada el 2014-10-07 17:05Z-07:00.*
