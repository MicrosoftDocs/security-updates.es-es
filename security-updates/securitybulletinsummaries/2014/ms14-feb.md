---
TOCTitle: 'MS14-FEB'
Title: Resumen del boletín de seguridad de Microsoft de febrero de 2014
ms:assetid: 'ms14-feb'
ms:contentKeyID: 61597920
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms14-feb(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de febrero de 2014
================================================================

Resumen del boletín de seguridad de Microsoft de febrero de 2014
----------------------------------------------------------------

Publicado: 11 de febrero de 2014 | Actualizado: 13 de febrero de 2014

**Versión:** 1.2

Este resumen del boletín enumera los boletines de seguridad publicados para febrero de 2014.

Con la publicación de los boletines de seguridad de febrero de 2014, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 10 de febrero de 2014. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar una difusión por web para atender las consultas de los clientes sobre estos boletines el 12 de febrero de 2014, a las 11:00 a.m., hora del Pacífico (EE. UU. y Canadá). [Inscríbase ahora a la conferencia en línea del boletín de seguridad de febrero](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032572879&culture=en-us).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, Información adicional.

Resúmenes ejecutivos
--------------------

En la tabla siguiente se resumen los boletines de seguridad de este mes por orden de gravedad.

Para obtener detalles acerca del software afectado, vea la siguiente sección, Software afectado.

 
<p> </p>
<table style="border:1px solid black;">
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><strong>Título de boletín y resumen ejecutivo</strong></td>
<td style="border:1px solid black;"><strong>Clasificación máxima de gravedad y consecuencias de la vulnerabilidad</strong></td>
<td style="border:1px solid black;"><strong>Requisito de reinicio</strong></td>
<td style="border:1px solid black;"><strong>Software afectado</strong></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Actualización de seguridad acumulativa para Internet Explorer (2909921)<br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y veintitrés vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. La más grave de las vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un atacante que aprovechara la más grave de estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=391023">MS14-011</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en el motor de scripting de VBScript podría permitir la ejecución remota de código (2928390)<br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en el motor de scripting de VBScript en Microsoft Windows. Esta vulnerabilidad podría permitir la ejecución remota de código si un usuario visita un sitio web especialmente diseñado. El atacante no podría obligar a los usuarios a visitar el sitio web. Por lo tanto, tendría que atraerlos para realizaran una acción; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger que lleve a los usuarios al sitio web del atacante.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386447">MS14-007</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en Direct2D podría permitir la ejecución remota de código (2912390)<br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. El atacante no podría obligar a los usuarios para que vieran el contenido especialmente diseñado. En su lugar, tendría que convencerlos para que realizaran alguna acción, normalmente incitándoles a que hagan clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger que los lleve al sitio web de un atacante o a que abran datos adjuntos enviados por correo electrónico.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390218">MS14-008</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en Microsoft Forefront Protection para Exchange podría permitir la ejecución remota de código (2927022)<br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Forefront. La vulnerabilidad podría permitir la ejecución remota de código si se analiza un mensaje de correo electrónico especialmente diseñado.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Software de seguridad de Microsoft</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386454">MS14-009</a></td>
<td style="border:1px solid black;">Vulnerabilidades en .NET Framework podrían permitir la elevación de privilegios (2916607)<br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma pública y una vulnerabilidad de la que se ha informado de forma privada en .NET Framework. La vulnerabilidad más grave podría permitir la elevación de privilegios si un usuario visita un sitio web especialmente diseñado o un sitio web que incluye contenido web especialmente diseñado. Sin embargo, el atacante no podría en ningún caso obligar a los usuarios a visitar estos sitios web. Por lo tanto, tendría que atraerlos al sitio web en peligro; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico o de un mensaje de Instant Messenger que los lleve al sitio web del atacante.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Microsoft .NET Framework</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=391022">MS14-005</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en Microsoft XML Core Services podría permitir la divulgación de información (2916036)<br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública en Microsoft XML Core Services, incluido en Microsoft Windows. La vulnerabilidad podría permitir la divulgación de información si un usuario visita una página web especialmente diseñada mediante Internet Explorer. El atacante no podría obligar a los usuarios para que vieran el contenido especialmente diseñado. En su lugar, tendría que convencerlos para que realizaran alguna acción, normalmente incitándoles a que hagan clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger que los lleve al sitio web de un atacante o a que abran datos adjuntos enviados por correo electrónico.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Divulgación de información</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386450">MS14-006</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en IPv6 podría permitir la denegación de servicio (2904659)<br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad que se ha divulgado públicamente en Microsoft Windows. La vulnerabilidad podría permitir la denegación de servicio si un atacante envía una gran cantidad de paquetes IPv6 especialmente diseñados a un sistema afectado. Para aprovechar la vulnerabilidad, el sistema de un atacante debe pertenecer a la misma subred que el sistema de destino.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Denegación de servicio</td>
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
  
En las columnas siguientes, "Última versión de software" hace referencia al software en cuestión y "Versiones de software anteriores" hace referencia a todas las versiones anteriores y compatibles del software en cuestión, tal como se muestra en las tablas "Software afectado" y "Software no afectado" del boletín.
  
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
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><strong>Título de vulnerabilidad</strong></td>
<td style="border:1px solid black;"><strong>Identificador CVE</strong></td>
<td style="border:1px solid black;"><strong>Evaluación de explotabilidad para la última versión de software</strong></td>
<td style="border:1px solid black;"><strong>Evaluación de explotabilidad para la versión de software anterior</strong></td>
<td style="border:1px solid black;"><strong>Evaluación de explotabilidad de denegación de servicio</strong></td>
<td style="border:1px solid black;"><strong>Notas clave</strong></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=391022">MS14-005</a></td>
<td style="border:1px solid black;">Vulnerabilidad de divulgación de información en MSXML</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0266">CVE-2014-0266</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información.<br />
<br />
Esta vulnerabilidad ya se ha divulgado públicamente.<br />
<br />
Microsoft tiene constancia de ataques dirigidos que intentan aprovechar esta vulnerabilidad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386450">MS14-006</a></td>
<td style="border:1px solid black;">Vulnerabilidad de denegación de servicio en TCP/IP versión 6 (IPv6)</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0254">CVE-2014-0254</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.<br />
<br />
Esta vulnerabilidad ya se ha divulgado públicamente.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386447">MS14-007</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con el componente de gráficos de Microsoft</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0263">CVE-2014-0263</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390218">MS14-008</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0294">CVE-2014-0294</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386454">MS14-009</a></td>
<td style="border:1px solid black;">Vulnerabilidad de DoS en las solicitudes POST</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0253">CVE-2014-0253</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.<br />
<br />
Esta vulnerabilidad ya se ha divulgado públicamente.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386454">MS14-009</a></td>
<td style="border:1px solid black;">Vulnerabilidad de recorrido de tipos</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0257">CVE-2014-0257</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386454">MS14-009</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ASLR en VSAVB7RT</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0295">CVE-2014-0295</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Es una vulnerabilidad de omisión de característica de seguridad.<br />
<br />
Esta vulnerabilidad ya se ha divulgado públicamente.<br />
<br />
Microsoft tiene constancia de ataques dirigidos y limitados que intentan aprovechar esta vulnerabilidad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0267">CVE-2014-0267</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0268">CVE-2014-0268</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0269">CVE-2014-0269</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0270">CVE-2014-0270</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0271">CVE-2014-0271</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0272">CVE-2014-0272</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0273">CVE-2014-0273</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0274">CVE-2014-0274</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0275">CVE-2014-0275</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0276">CVE-2014-0276</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0277">CVE-2014-0277</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0278">CVE-2014-0278</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0279">CVE-2014-0279</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0280">CVE-2014-0280</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0281">CVE-2014-0281</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0283">CVE-2014-0283</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0284">CVE-2014-0284</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0285">CVE-2014-0285</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0286">CVE-2014-0286</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0287">CVE-2014-0287</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0288">CVE-2014-0288</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0289">CVE-2014-0289</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0290">CVE-2014-0290</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=390977">MS14-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de divulgación de información entre dominios en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0293">CVE-2014-0293</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=391023">MS14-011</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con VBScript</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0271">CVE-2014-0271</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
</tbody>
</table>
  
Software afectado  
-----------------
  
Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.
  
¿Cómo se usan estas tablas?
  
Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, también se muestra la clasificación de gravedad de dicha actualización de software.
  
Nota Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.
  
### Componentes y sistema operativo Windows

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="7">
**Windows XP**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS14-010](http://go.microsoft.com/fwlink/?linkid=390977)
</td>
<td style="border:1px solid black;">
[MS14-011](http://go.microsoft.com/fwlink/?linkid=391023)
</td>
<td style="border:1px solid black;">
[MS14-007](http://go.microsoft.com/fwlink/?linkid=386447)
</td>
<td style="border:1px solid black;">
[MS14-009](http://go.microsoft.com/fwlink/?linkid=386454)
</td>
<td style="border:1px solid black;">
[MS14-005](http://go.microsoft.com/fwlink/?linkid=391022)
</td>
<td style="border:1px solid black;">
[MS14-006](http://go.microsoft.com/fwlink/?linkid=386450)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
Internet Explorer 6   
(2909921)  
(Crítica)  
Internet Explorer 7   
(2909921)  
(Crítica)  
Internet Explorer 8   
(2909921)  
(Crítica)
</td>
<td style="border:1px solid black;">
VBScript 5.7   
(2909212)  
(Crítica)  
VBScript 5.8   
(2909210)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 1.0 Service Pack 3  
(2904878)  
(Importante)  
(Media Center Edition 2005 Service Pack 3 y Tablet PC Edition 2005 Service Pack 3 solo)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2901111)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2898856)  
(Importante)  
Microsoft .NET Framework 4.0  
(2901110)  
(Importante)  
Microsoft .NET Framework 4.0  
(2898855)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows XP Service Pack 3  
(2916036)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 6   
(2909921)  
(Crítica)  
Internet Explorer 7   
(2909921)  
(Crítica)  
Internet Explorer 8   
(2909921)  
(Crítica)
</td>
<td style="border:1px solid black;">
VBScript 5.6  
(2909213)  
(Crítica)  
VBScript 5.7   
(2909212)  
(Crítica)  
VBScript 5.8   
(2909210)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2901111)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2898856)  
(Importante)  
Microsoft .NET Framework 4.0  
(2901110)  
(Importante)  
Microsoft .NET Framework 4.0  
(2898855)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2  
(2916036)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="7">
**Windows Server 2003**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS14-010](http://go.microsoft.com/fwlink/?linkid=390977)
</td>
<td style="border:1px solid black;">
[MS14-011](http://go.microsoft.com/fwlink/?linkid=391023)
</td>
<td style="border:1px solid black;">
[MS14-007](http://go.microsoft.com/fwlink/?linkid=386447)
</td>
<td style="border:1px solid black;">
[MS14-009](http://go.microsoft.com/fwlink/?linkid=386454)
</td>
<td style="border:1px solid black;">
[MS14-005](http://go.microsoft.com/fwlink/?linkid=391022)
</td>
<td style="border:1px solid black;">
[MS14-006](http://go.microsoft.com/fwlink/?linkid=386450)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Moderada](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Baja](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 6   
(2909921)  
(Moderada)  
Internet Explorer 7  
(2909921)  
(Moderada)  
Internet Explorer 8  
(2909921)  
(Importante)
</td>
<td style="border:1px solid black;">
VBScript 5.6  
(2909213)  
(Moderada)  
VBScript 5.7   
(2909212)  
(Moderada)  
VBScript 5.8   
(2909210)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 1.1 Service Pack 1  
(2901115)  
(Importante)  
Microsoft .NET Framework 1.1 Service Pack 1  
(2898860)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2901111)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2898856)  
(Importante)  
Microsoft .NET Framework 4.0  
(2901110)  
(Importante)  
Microsoft .NET Framework 4.0  
(2898855)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(2916036)  
(Baja)
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
(2909921)  
(Moderada)  
Internet Explorer 7  
(2909921)  
(Moderada)  
Internet Explorer 8  
(2909921)  
(Importante)
</td>
<td style="border:1px solid black;">
VBScript 5.6  
(2909213)  
(Moderada)  
VBScript 5.7   
(2909212)  
(Moderada)  
VBScript 5.8   
(2909210)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2901111)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2898856)  
(Importante)  
Microsoft .NET Framework 4.0  
(2901110)  
(Importante)  
Microsoft .NET Framework 4.0  
(2898855)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2916036)  
(Baja)
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
(2909921)  
(Moderada)  
Internet Explorer 7  
(2909921)  
(Moderada)
</td>
<td style="border:1px solid black;">
VBScript 5.6  
(2909213)  
(Moderada)  
VBScript 5.7   
(2909212)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2901111)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2898856)  
(Importante)  
Microsoft .NET Framework 4.0  
(2901110)  
(Importante)  
Microsoft .NET Framework 4.0  
(2898855)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2916036)  
(Baja)
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
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS14-010](http://go.microsoft.com/fwlink/?linkid=390977)
</td>
<td style="border:1px solid black;">
[MS14-011](http://go.microsoft.com/fwlink/?linkid=391023)
</td>
<td style="border:1px solid black;">
[MS14-007](http://go.microsoft.com/fwlink/?linkid=386447)
</td>
<td style="border:1px solid black;">
[MS14-009](http://go.microsoft.com/fwlink/?linkid=386454)
</td>
<td style="border:1px solid black;">
[MS14-005](http://go.microsoft.com/fwlink/?linkid=391022)
</td>
<td style="border:1px solid black;">
[MS14-006](http://go.microsoft.com/fwlink/?linkid=386450)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2909921)  
(Crítica)  
Internet Explorer 8  
(2909921)  
(Crítica)  
Internet Explorer 9   
(2909921)  
(Crítica)
</td>
<td style="border:1px solid black;">
VBScript 5.7   
(2909212)  
(Crítica)  
VBScript 5.8 sistemas que ejecutan Internet Explorer 8  
(2909210)  
(Crítica)  
VBScript 5.8 sistemas que ejecutan Internet Explorer 9  
(2909921)<sup>[1]</sup>
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2901113)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2898858)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2911502)  
(Importante)  
Microsoft .NET Framework 4.0  
(2901110)  
(Importante)  
Microsoft .NET Framework 4.0  
(2898855)  
(Importante)  
Microsoft .NET Framework 4.5  
(2901118)  
(Importante)  
Microsoft .NET Framework 4.5  
(2898864)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2901126)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898869)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2916036)  
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
(2909921)  
(Crítica)  
Internet Explorer 8  
(2909921)  
(Crítica)  
Internet Explorer 9   
(2909921)  
(Crítica)
</td>
<td style="border:1px solid black;">
VBScript 5.7   
(2909212)  
(Crítica)  
VBScript 5.8 sistemas que ejecutan Internet Explorer 8  
(2909210)  
(Crítica)  
VBScript 5.8 sistemas que ejecutan Internet Explorer 9  
(2909921)<sup>[1]</sup>
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2901113)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2898858)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2911502)  
(Importante)  
Microsoft .NET Framework 4.0  
(2901110)  
(Importante)  
Microsoft .NET Framework 4.0  
(2898855)  
(Importante)  
Microsoft .NET Framework 4.5  
(2901118)  
(Importante)  
Microsoft .NET Framework 4.5  
(2898864)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2901126)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898869)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2916036)  
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
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS14-010](http://go.microsoft.com/fwlink/?linkid=390977)
</td>
<td style="border:1px solid black;">
[MS14-011](http://go.microsoft.com/fwlink/?linkid=391023)
</td>
<td style="border:1px solid black;">
[MS14-007](http://go.microsoft.com/fwlink/?linkid=386447)
</td>
<td style="border:1px solid black;">
[MS14-009](http://go.microsoft.com/fwlink/?linkid=386454)
</td>
<td style="border:1px solid black;">
[MS14-005](http://go.microsoft.com/fwlink/?linkid=391022)
</td>
<td style="border:1px solid black;">
[MS14-006](http://go.microsoft.com/fwlink/?linkid=386450)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Moderada](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Baja](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2909921)  
(Moderada)  
Internet Explorer 8  
(2909921)  
(Importante)  
Internet Explorer 9   
(2909921)  
(Importante)
</td>
<td style="border:1px solid black;">
VBScript 5.7   
(2909212)  
(Moderada)  
VBScript 5.8 sistemas que ejecutan Internet Explorer 8  
(2909210)  
(Moderada)  
VBScript 5.8 sistemas que ejecutan Internet Explorer 9  
(2909921)<sup>[1]</sup>
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2901113)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2898858)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2911502)  
(Importante)  
Microsoft .NET Framework 4.0  
(2901110)  
(Importante)  
Microsoft .NET Framework 4.0  
(2898855)  
(Importante)  
Microsoft .NET Framework 4.5  
(2901118)  
(Importante)  
Microsoft .NET Framework 4.5  
(2898864)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2901126)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898869)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2916036)  
(Baja)
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
(2909921)  
(Moderada)  
Internet Explorer 8  
(2909921)  
(Importante)  
Internet Explorer 9   
(2909921)  
(Importante)
</td>
<td style="border:1px solid black;">
VBScript 5.7   
(2909212)  
(Moderada)  
VBScript 5.8 sistemas que ejecutan Internet Explorer 8  
(2909210)  
(Moderada)  
VBScript 5.8 sistemas que ejecutan Internet Explorer 9  
(2909921)<sup>[1]</sup>
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2901113)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2898858)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2911502)  
(Importante)  
Microsoft .NET Framework 4.0  
(2901110)  
(Importante)  
Microsoft .NET Framework 4.0  
(2898855)  
(Importante)  
Microsoft .NET Framework 4.5  
(2901118)  
(Importante)  
Microsoft .NET Framework 4.5  
(2898864)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2901126)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898869)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2916036)  
(Baja)
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
(2909921)  
(Moderada)
</td>
<td style="border:1px solid black;">
VBScript 5.7   
(2909212)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2901113)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2898858)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2911502)  
(Importante)  
Microsoft .NET Framework 4.0  
(2901110)  
(Importante)  
Microsoft .NET Framework 4.0  
(2898855)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2916036)  
(Baja)
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
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS14-010](http://go.microsoft.com/fwlink/?linkid=390977)
</td>
<td style="border:1px solid black;">
[MS14-011](http://go.microsoft.com/fwlink/?linkid=391023)
</td>
<td style="border:1px solid black;">
[MS14-007](http://go.microsoft.com/fwlink/?linkid=386447)
</td>
<td style="border:1px solid black;">
[MS14-009](http://go.microsoft.com/fwlink/?linkid=386454)
</td>
<td style="border:1px solid black;">
[MS14-005](http://go.microsoft.com/fwlink/?linkid=391022)
</td>
<td style="border:1px solid black;">
[MS14-006](http://go.microsoft.com/fwlink/?linkid=386450)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2909921)  
(Crítica)  
Internet Explorer 9   
(2909921)  
(Crítica)  
Internet Explorer 10   
(2909921)  
(Crítica)  
Internet Explorer 11   
(2909921)  
(Crítica)
</td>
<td style="border:1px solid black;">
VBScript 5.8 sistemas que ejecutan Internet Explorer 8  
(2909210)  
(Crítica)  
VBScript 5.8 sistemas que ejecutan Internet Explorer 9  
(2909921)<sup>[1]</sup>
(Crítica)  
VBScript 5.8 sistemas que ejecutan Internet Explorer 10  
(2909210)  
(Crítica)  
VBScript 5.8 sistemas que ejecutan Internet Explorer 11  
(2909210)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2912390)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2901112)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2898857)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2911501)  
(Importante)  
Microsoft .NET Framework 4.0  
(2901110)  
(Importante)  
Microsoft .NET Framework 4.0  
(2898855)  
(Importante)  
Microsoft .NET Framework 4.5  
(2901118)  
(Importante)  
Microsoft .NET Framework 4.5  
(2898864)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2901126)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898869)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2916036)  
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
(2909921)  
(Crítica)  
Internet Explorer 9   
(2909921)  
(Crítica)  
Internet Explorer 10   
(2909921)  
(Crítica)  
Internet Explorer 11   
(2909921)  
(Crítica)
</td>
<td style="border:1px solid black;">
VBScript 5.8 sistemas que ejecutan Internet Explorer 8  
(2909210)  
(Crítica)  
VBScript 5.8 sistemas que ejecutan Internet Explorer 9  
(2909921)<sup>[1]</sup>
(Crítica)  
VBScript 5.8 sistemas que ejecutan Internet Explorer 10  
(2909210)  
(Crítica)  
VBScript 5.8 sistemas que ejecutan Internet Explorer 11  
(2909210)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2912390)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2901112)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2898857)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2911501)  
(Importante)  
Microsoft .NET Framework 4.0  
(2901110)  
(Importante)  
Microsoft .NET Framework 4.0  
(2898855)  
(Importante)  
Microsoft .NET Framework 4.5  
(2901118)  
(Importante)  
Microsoft .NET Framework 4.5  
(2898864)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2901126)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898869)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2916036)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="7">
**Windows Server 2008 R2**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS14-010](http://go.microsoft.com/fwlink/?linkid=390977)
</td>
<td style="border:1px solid black;">
[MS14-011](http://go.microsoft.com/fwlink/?linkid=391023)
</td>
<td style="border:1px solid black;">
[MS14-007](http://go.microsoft.com/fwlink/?linkid=386447)
</td>
<td style="border:1px solid black;">
[MS14-009](http://go.microsoft.com/fwlink/?linkid=386454)
</td>
<td style="border:1px solid black;">
[MS14-005](http://go.microsoft.com/fwlink/?linkid=391022)
</td>
<td style="border:1px solid black;">
[MS14-006](http://go.microsoft.com/fwlink/?linkid=386450)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Moderada](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Baja](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2909921)  
(Importante)  
Internet Explorer 9   
(2909921)  
(Importante)  
Internet Explorer 10   
(2909921)  
(Importante)  
Internet Explorer 11   
(2909921)  
(Importante)
</td>
<td style="border:1px solid black;">
VBScript 5.8 sistemas que ejecutan Internet Explorer 8  
(2909210)  
(Moderada)  
VBScript 5.8 sistemas que ejecutan Internet Explorer 9  
(2909921)<sup>[1]</sup>
(Moderada)  
VBScript 5.8 sistemas que ejecutan Internet Explorer 10  
(2909210)  
(Moderada)  
VBScript 5.8 sistemas que ejecutan Internet Explorer 11  
(2909210)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2912390)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2901112)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2898857)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2911501)  
(Importante)  
Microsoft .NET Framework 4.0  
(2901110)  
(Importante)  
Microsoft .NET Framework 4.0  
(2898855)  
(Importante)  
Microsoft .NET Framework 4.5  
(2901118)  
(Importante)  
Microsoft .NET Framework 4.5  
(2898864)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2901126)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898869)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2916036)  
(Baja)
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
(2909921)  
(Importante)
</td>
<td style="border:1px solid black;">
VBScript 5.8 sistemas que ejecutan Internet Explorer 8  
(2909210)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2901112)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2898857)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2911501)  
(Importante)  
Microsoft .NET Framework 4.0  
(2901110)  
(Importante)  
Microsoft .NET Framework 4.0  
(2898855)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2916036)  
(Baja)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="7">
**Windows 8 y Windows 8.1**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS14-010](http://go.microsoft.com/fwlink/?linkid=390977)
</td>
<td style="border:1px solid black;">
[MS14-011](http://go.microsoft.com/fwlink/?linkid=391023)
</td>
<td style="border:1px solid black;">
[MS14-007](http://go.microsoft.com/fwlink/?linkid=386447)
</td>
<td style="border:1px solid black;">
[MS14-009](http://go.microsoft.com/fwlink/?linkid=386454)
</td>
<td style="border:1px solid black;">
[MS14-005](http://go.microsoft.com/fwlink/?linkid=391022)
</td>
<td style="border:1px solid black;">
[MS14-006](http://go.microsoft.com/fwlink/?linkid=386450)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2909921)  
(Crítica)
</td>
<td style="border:1px solid black;">
VBScript 5.8 sistemas que ejecutan Internet Explorer 10  
(2909210)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2912390)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2901120)  
(Importante)  
Microsoft .NET Framework 3.5  
(2898866)  
(Importante)  
Microsoft .NET Framework 4.5  
(2901119)  
(Importante)  
Microsoft .NET Framework 4.5  
(2898865)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2901127)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898870)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2916036)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2904659)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas x64
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2909921)  
(Crítica)
</td>
<td style="border:1px solid black;">
VBScript 5.8 sistemas que ejecutan Internet Explorer 10  
(2909210)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(2912390)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2901120)  
(Importante)  
Microsoft .NET Framework 3.5  
(2898866)  
(Importante)  
Microsoft .NET Framework 4.5  
(2901119)  
(Importante)  
Microsoft .NET Framework 4.5  
(2898865)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2901127)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898870)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(2916036)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(2904659)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 11   
(2909921)  
(Crítica)
</td>
<td style="border:1px solid black;">
VBScript 5.8 sistemas que ejecutan Internet Explorer 11  
(2909210)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(2912390)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2901125)  
(Importante)  
Microsoft .NET Framework 3.5  
(2898868)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2901128)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898871)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(2916036)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64
</td>
<td style="border:1px solid black;">
Internet Explorer 11   
(2909921)  
(Crítica)
</td>
<td style="border:1px solid black;">
VBScript 5.8 sistemas que ejecutan Internet Explorer 11  
(2909210)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(2912390)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2901125)  
(Importante)  
Microsoft .NET Framework 3.5  
(2898868)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2901128)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898871)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(2916036)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="7">
**Windows Server 2012 y Windows Server 2012 R2**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS14-010](http://go.microsoft.com/fwlink/?linkid=390977)
</td>
<td style="border:1px solid black;">
[MS14-011](http://go.microsoft.com/fwlink/?linkid=391023)
</td>
<td style="border:1px solid black;">
[MS14-007](http://go.microsoft.com/fwlink/?linkid=386447)
</td>
<td style="border:1px solid black;">
[MS14-009](http://go.microsoft.com/fwlink/?linkid=386454)
</td>
<td style="border:1px solid black;">
[MS14-005](http://go.microsoft.com/fwlink/?linkid=391022)
</td>
<td style="border:1px solid black;">
[MS14-006](http://go.microsoft.com/fwlink/?linkid=386450)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Moderada](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Baja](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2909921)  
(Importante)
</td>
<td style="border:1px solid black;">
VBScript 5.8 sistemas que ejecutan Internet Explorer 10  
(2909210)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2912390)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2901120)  
(Importante)  
Microsoft .NET Framework 3.5  
(2898866)  
(Importante)  
Microsoft .NET Framework 4.5  
(2901119)  
(Importante)  
Microsoft .NET Framework 4.5  
(2898865)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2901127)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898870)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2916036)  
(Baja)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2904659)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012 R2
</td>
<td style="border:1px solid black;">
Internet Explorer 11   
(2909921)  
(Importante)
</td>
<td style="border:1px solid black;">
VBScript 5.8 sistemas que ejecutan Internet Explorer 11  
(2909210)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(2912390)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2901125)  
(Importante)  
Microsoft .NET Framework 3.5  
(2898868)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2901128)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898871)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(2916036)  
(Baja)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="7">
**Windows RT y Windows RT 8.1**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS14-010](http://go.microsoft.com/fwlink/?linkid=390977)
</td>
<td style="border:1px solid black;">
[MS14-011](http://go.microsoft.com/fwlink/?linkid=391023)
</td>
<td style="border:1px solid black;">
[MS14-007](http://go.microsoft.com/fwlink/?linkid=386447)
</td>
<td style="border:1px solid black;">
[MS14-009](http://go.microsoft.com/fwlink/?linkid=386454)
</td>
<td style="border:1px solid black;">
[MS14-005](http://go.microsoft.com/fwlink/?linkid=391022)
</td>
<td style="border:1px solid black;">
[MS14-006](http://go.microsoft.com/fwlink/?linkid=386450)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows RT
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2909921)  
(Crítica)
</td>
<td style="border:1px solid black;">
VBScript 5.8 sistemas que ejecutan Internet Explorer 10  
(2909210)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows RT  
(2912390)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 4.5  
(2901119)  
(Importante)  
Microsoft .NET Framework 4.5  
(2898865)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2901127)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898870)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT  
(2916036)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT  
(2904659)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows RT 8.1
</td>
<td style="border:1px solid black;">
Internet Explorer 11   
(2909921)  
(Crítica)
</td>
<td style="border:1px solid black;">
VBScript 5.8 sistemas que ejecutan Internet Explorer 11  
(2909210)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(2912390)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 4.5.1  
(2901128)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898871)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(2916036)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="7">
**Opción de instalación Server Core**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS14-010](http://go.microsoft.com/fwlink/?linkid=390977)
</td>
<td style="border:1px solid black;">
[MS14-011](http://go.microsoft.com/fwlink/?linkid=391023)
</td>
<td style="border:1px solid black;">
[MS14-007](http://go.microsoft.com/fwlink/?linkid=386447)
</td>
<td style="border:1px solid black;">
[MS14-009](http://go.microsoft.com/fwlink/?linkid=386454)
</td>
<td style="border:1px solid black;">
[MS14-005](http://go.microsoft.com/fwlink/?linkid=391022)
</td>
<td style="border:1px solid black;">
[MS14-006](http://go.microsoft.com/fwlink/?linkid=386450)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Baja](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
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
VBScript 5.7   
(2909212)  
(Sin clasificación de gravedad)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2916036)  
(Baja)
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
VBScript 5.7   
(2909212)  
(Sin clasificación de gravedad)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2916036)  
(Baja)
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
VBScript 5.8   
(2909210)  
(Sin clasificación de gravedad)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2901112)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2898857)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2911501)  
(Importante)  
Microsoft .NET Framework 4.0  
(2901110)  
(Importante)  
Microsoft .NET Framework 4.5  
(2901118)  
(Importante)  
Microsoft .NET Framework 4.5  
(2898864)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2901126)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898869)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2916036)  
(Baja)
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
VBScript 5.8   
(2909210)  
(Sin clasificación de gravedad)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2901120)  
(Importante)  
Microsoft .NET Framework 3.5  
(2898866)  
(Importante)  
Microsoft .NET Framework 4.5  
(2901119)  
(Importante)  
Microsoft .NET Framework 4.5  
(2898865)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2901127)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898870)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(2916036)  
(Baja)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(2904659)  
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
VBScript 5.8   
(2909210)  
(Sin clasificación de gravedad)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2901125)  
(Importante)  
Microsoft .NET Framework 3.5  
(2898868)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2901128)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2898871)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(2916036)  
(Baja)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
Nota para MS14-011

<sup>[1]</sup>Para los sistemas que ejecutan Internet Explorer 9, la vulnerabilidad se corrige mediante la actualización acumulativa 2909921 para Internet Explorer 9 en [MS14-010](http://go.microsoft.com/fwlink/?linkid=390977).

 

### Software de seguridad de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="2">
**Microsoft Forefront Protection 2010 para Exchange Server**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS14-008](http://go.microsoft.com/fwlink/?linkid=390218)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Forefront Protection 2010 para Exchange Server
</td>
<td style="border:1px solid black;">
Microsoft Forefront Protection 2010 para Exchange Server  
(2927022)  
(Crítica)
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

Agradecimientos
---------------

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

MS14-005

-   [FireEye, Inc.](http://www2.fireeye.com/), por colaborar con nosotros en la vulnerabilidad de divulgación de información en MSXML (CVE-2014-0266)

MS14-007

-   [Omair](http://krash.in/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con el componente de gráficos de Microsoft (CVE-2014-0263)

MS14-009

-   James Forshaw, de [Context Information Security](http://www.contextis.com/), por informar de la vulnerabilidad de recorrido de tipos (CVE-2014-0257)

MS14-010

-   Liang Chen, de [KeenTeam](http://www.k33nteam.org/) (@K33nTeam), por colaborar con nosotros en la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0267)
-   Code Audit Labs, de [VulnHunt](http://www.vulnhunt.com/), por colaborar con nosotros en la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0267)
-   James Forshaw, de [Context Information Security](http://www.contextis.com/), por informar de la vulnerabilidad de elevación de privilegios en Internet Explorer (CVE-2014-0268)
-   Simon Zuckerbraun, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0269)
-   José A. Vázquez, de Yenteasy - Security Research en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0270)
-   José A. Vázquez, de Yenteasy - Security Research en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0270)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0272)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0273)
-   Arthur Gerkis, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0274)
-   lokihardt@ASRT, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0274)
-   Simon Zuckerbraun, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0275)
-   Scott Bell, de [Security-Assessment.com](http://www.security-assessment.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0276)
-   Scott Bell, de [Security-Assessment.com](http://www.security-assessment.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0277)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0278)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0278)
-   Scott Bell, de [Security-Assessment.com](http://www.security-assessment.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0279)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0279)
-   Scott Bell, de [Security-Assessment.com](http://www.security-assessment.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0280)
-   cons0ul y suto, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0281)
-   Sachin Shinde, por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0283)
-   Sachin Shinde, por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0284)
-   Simon Zuckerbraun, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0285)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0285)
-   Simon Zuckerbraun, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0286)
-   Peter 'corelanc0d3r' Van Eeckhoutte, de [Corelan](http://www.corelangcv.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0287)
-   Arthur Gerkis, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0288)
-   lokihardt@ASRT, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0289)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0290)
-   Zhibin Hu de [Qihoo](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0290)
-   Yuki Chen, de [Trend Micro](http://www.trendmicro.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0290)
-   [Dieyu dieu deus deva divine dio theos dievas dewa ilu Diyin Ayóo Átʼéii atua tiānzhŭ Yahweh Zeus Odin El](http://dieyu.org/), por informar de la vulnerabilidad de divulgación de información entre dominios en Internet Explorer (CVE-2014-0293)

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

Estrategias de administración de actualizaciones

En [Orientación de seguridad para la administración de actualizaciones](http://go.microsoft.com/fwlink/?linkid=21168) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

Obtención de otras actualizaciones de seguridad

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](https://support.microsoft.com/kb/913086).

Comunidad de seguridad para profesionales de tecnologías de la información

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [Comunidad de profesionales de TI de seguridad](http://go.microsoft.com/fwlink/?linkid=21164).

### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Soluciones de seguridad para profesionales de TI: [Soporte técnico y solución de problemas de seguridad de TechNet](http://technet.microsoft.com/security/bb980617)
-   Ayuda para proteger su equipo con Windows de virus y malware: [Solución antivirus y centro de seguridad](http://support.microsoft.com/contactus/cu_sc_virsec_master)
-   Soporte local según su país: [Soporte internacional](http://support.microsoft.com/common/international.aspx)

### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

### Revisiones

-   V1.0 (11 de febrero de 2014): Publicación del resumen del boletín.
-   V1.1 (12 de febrero de 2014): para MS14-008, se ha revisado la evaluación de explotabilidad correspondiente a la versión de software anterior en el **índice de explotabilidad** para CVE-2014-0294.
-   V1.2 (13 de febrero de 2014): para MS14-011, se ha revisado la evaluación de explotabilidad correspondiente a la última versión de software en el índice de explotabilidad para CVE-2014-0271.

*Página generada el 2014-04-23 12:19Z-07:00.*
