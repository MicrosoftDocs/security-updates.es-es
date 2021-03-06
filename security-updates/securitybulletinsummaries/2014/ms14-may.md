---
TOCTitle: 'MS14-MAY'
Title: Resumen del boletín de seguridad de Microsoft de mayo de 2014
ms:assetid: 'ms14-may'
ms:contentKeyID: 62258019
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms14-may(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de mayo de 2014
=============================================================

Publicado: 1 de mayo de 2014 | Actualizado: 13 de mayo de 2014

**Versión:** 2.0

Este resumen del boletín enumera los boletines de seguridad publicados para mayo de 2014.

Con la publicación de los boletines de seguridad de mayo de 2014, este resumen del boletín reemplaza a la notificación de avance de boletines publicada originalmente el 8 de mayo de 2014. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar una difusión por web para atender las consultas de los clientes sobre estos boletines el 14 de mayo de 2014, a las 11:00 a. m., hora del Pacífico (EE. UU. y Canadá). [Inscríbase ahora a la conferencia en línea del boletín de seguridad de mayo](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032572979&culture=en-us).

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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=397669"><strong>MS14-021</strong></a><br />
(Publicado fuera de ciclo el 1 de mayo de 2014)</td>
<td style="border:1px solid black;"><strong>Actualización de seguridad para Internet Explorer (2965111)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública en Internet Explorer. La vulnerabilidad podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante una versión afectada de Internet Explorer. Un atacante que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=395261"><strong>MS14-029</strong></a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad para Internet Explorer (2962482)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. Un intruso que aprovechara estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los clientes cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386285"><strong>MS14-022</strong></a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft SharePoint Server podrían permitir la ejecución remota de código (2952166)</strong><br />
<br />
Esta actualización de seguridad resuelve varias vulnerabilidades de las que se ha informado de forma privada en el software de servidor y productividad de Microsoft Office. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un atacante autenticado envía contenido de página especialmente diseñado a un servidor de SharePoint de destino.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Software de servidor de Microsoft,<br />
Software de productividad</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=393745"><strong>MS14-023</strong></a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Office podrían permitir la ejecución remota de código (2961037)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft Office. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo de Office que se encuentre en el mismo directorio de red que un archivo de biblioteca especialmente diseñado. Un atacante que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los clientes cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=396820"><strong>MS14-025</strong></a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en las preferencias de directiva de grupo podría permitir la elevación de privilegios (2962486)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad que se ha divulgado públicamente en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si las preferencias de directiva de grupo de Active Directory se usan para distribuir contraseñas por el dominio, una práctica que podría permitir que un atacante recuperara y descifrara la contraseña almacenada con las preferencias de directiva de grupo.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=396825"><strong>MS14-026</strong></a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en .NET Framework podría permitir la elevación de privilegios (2958732)<br />
</strong><br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft .NET Framework. La vulnerabilidad podría permitir la elevación de privilegios si un usuario autenticado envía datos especialmente diseñados a una estación de trabajo o a un servidor afectado que use .NET Remoting. .NET Remoting no se usa ampliamente en las aplicaciones, solo las personalizadas que se hayan diseñado específicamente para usar .NET Remoting expondrían un sistema a la vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Microsoft .NET Framework</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=396823"><strong>MS14-027</strong></a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el controlador del shell de Windows podría permitir la elevación de privilegios (2962488)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si un atacante ejecuta una aplicación especialmente diseñada que use ShellExecute. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=393744"><strong>MS14-028</strong></a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en iSCSI podría permitir la denegación de servicio (2962485)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. Las vulnerabilidades podrían permitir la denegación de servicio si un atacante envía grandes cantidades de paquetes iSCSI especialmente diseñados a través de la red de destino. Esta vulnerabilidad solo afecta a los servidores para los que se ha habilitado el rol de destino iSCSI.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Denegación de servicio</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=396835"><strong>MS14-024</strong></a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en un control común de Microsoft podría permitir la omisión de característica de seguridad (2961033)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en la biblioteca de controles comunes MSCOMCTL. La vulnerabilidad podría permitir la omisión de la característica de seguridad si un usuario consulta una página web especialmente diseñado en un explorador web que pueda ejecutar componentes COM, como Internet Explorer. En un escenario de ataque de exploración web, un atacante que aprovechara esta vulnerabilidad podría omitir la característica de seguridad de selección aleatoria del diseño del espacio de direcciones (ASLR), que contribuye a proteger a los usuarios de una amplia gama de vulnerabilidades. La omisión de la característica de seguridad en sí misma no permite la ejecución de código arbitrario. No obstante, un atacante podría usar esta vulnerabilidad de omisión de ASLR conjuntamente con otra vulnerabilidad, como la de ejecución remota de código, que pudiera aprovechar la omisión de ASLR para ejecutar código arbitrario.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Omisión de característica de seguridad</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=397669"><strong>MS14-021</strong></a><br />
(Publicado fuera de ciclo el 1 de mayo de 2014)</td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1776">CVE-2014-1776</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente. Esta vulnerabilidad se describió por primera vez en el <a href="https://technet.microsoft.com/library/security/2963983">documento informativo sobre seguridad de Microsoft 2963983</a>.<br />
<br />
Microsoft tiene constancia de ataques limitados y dirigidos que intentan aprovechar esta vulnerabilidad en Internet Explorer.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386285"><strong>MS14-022</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de contenido de página en SharePoint</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0251">CVE-2014-0251</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386285"><strong>MS14-022</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de XSS en SharePoint</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1754">CVE-2014-1754</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=386285"><strong>MS14-022</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de contenido de página de las aplicaciones web</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1813">CVE-2014-1813</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=393745"><strong>MS14-023</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad en la corrección gramatical para chino en Microsoft Office</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1756">CVE-2014-1756</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=393745"><strong>MS14-023</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de reutilización de token</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1808">CVE-2014-1808</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=396835"><strong>MS14-024</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de ASLR en MSCOMCTL</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1809">CVE-2014-1809</a></td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Es una vulnerabilidad de omisión de característica de seguridad.<br />
<br />
Microsoft tiene constancia de ataques dirigidos y limitados que intentan aprovechar esta vulnerabilidad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=396820"><strong>MS14-025</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en las contraseñas de las preferencias de directiva de grupo</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1812">CVE-2014-1812</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=396825"><strong>MS14-026</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de TypeFilterLevel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1806">CVE-2014-1806</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=396823"><strong>MS14-027</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad en la asociación de archivos del shell de Windows</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1807">CVE-2014-1807</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Microsoft tiene constancia de ataques limitados que intentan aprovechar esta vulnerabilidad.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=393744"><strong>MS14-028</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de denegación de servicio remoto en destino iSCSI</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0255">CVE-2014-0255</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=393744"><strong>MS14-028</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de denegación de servicio remoto en destino iSCSI</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0256">CVE-2014-0256</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=395261"><strong>MS14-029</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-0310">CVE-2014-0310</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=395261"><strong>MS14-029</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1815">CVE-2014-1815</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Microsoft tiene constancia de ataques limitados que intentan aprovechar esta vulnerabilidad en Internet Explorer.</td>
</tr>
</tbody>
</table>
  
Software afectado  
-----------------
  
Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.
  
**¿Cómo se usan estas tablas?**  
  
Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, también se muestra la clasificación de gravedad de dicha actualización de software.
  
**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.
  
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
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-021**](http://go.microsoft.com/fwlink/?linkid=397669)
</td>
<td style="border:1px solid black;">
[**MS14-029**](http://go.microsoft.com/fwlink/?linkid=395261)
</td>
<td style="border:1px solid black;">
[**MS14-025**](http://go.microsoft.com/fwlink/?linkid=396820)
</td>
<td style="border:1px solid black;">
[**MS14-026**](http://go.microsoft.com/fwlink/?linkid=396825)
</td>
<td style="border:1px solid black;">
[**MS14-027**](http://go.microsoft.com/fwlink/?linkid=396823)
</td>
<td style="border:1px solid black;">
[**MS14-028**](http://go.microsoft.com/fwlink/?linkid=309325)
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
<td style="border:1px solid black;">
**Ninguna**
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
Internet Explorer 6  
(2964358)  
(Crítica)  
Internet Explorer 7  
(2964358)  
(Crítica)  
Internet Explorer 8  
(2964358)  
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
<td style="border:1px solid black;">
No aplicable
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
(2964358)  
(Crítica)  
Internet Explorer 7  
(2964358)  
(Crítica)  
Internet Explorer 8  
(2964358)  
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
<td style="border:1px solid black;">
No aplicable
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
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-021**](http://go.microsoft.com/fwlink/?linkid=397669)
</td>
<td style="border:1px solid black;">
[**MS14-029**](http://go.microsoft.com/fwlink/?linkid=395261)
</td>
<td style="border:1px solid black;">
[**MS14-025**](http://go.microsoft.com/fwlink/?linkid=396820)
</td>
<td style="border:1px solid black;">
[**MS14-026**](http://go.microsoft.com/fwlink/?linkid=396825)
</td>
<td style="border:1px solid black;">
[**MS14-027**](http://go.microsoft.com/fwlink/?linkid=396823)
</td>
<td style="border:1px solid black;">
[**MS14-028**](http://go.microsoft.com/fwlink/?linkid=309325)
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 6  
(2964358)  
(Moderada)  
Internet Explorer 7  
(2964358)  
(Moderada)  
Internet Explorer 8  
(2964358)  
(Moderada)
</td>
<td style="border:1px solid black;">
Internet Explorer 6   
(2953522)  
(Moderada)  
Internet Explorer 7   
(2953522)  
(Moderada)  
Internet Explorer 8   
(2953522)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 1.1 Service Pack 1  
(2931352)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2932079)  
(Importante)  
Microsoft .NET Framework 4.0  
(2931365)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(2926765)  
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
(2964358)  
(Moderada)  
Internet Explorer 7  
(2964358)  
(Moderada)  
Internet Explorer 8  
(2964358)  
(Moderada)
</td>
<td style="border:1px solid black;">
Internet Explorer 6   
(2953522)  
(Moderada)  
Internet Explorer 7   
(2953522)  
(Moderada)  
Internet Explorer 8   
(2953522)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2932079)  
(Importante)  
Microsoft .NET Framework 4.0  
(2931365)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2926765)  
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
(2964358)  
(Moderada)  
Internet Explorer 7  
(2964358)  
(Moderada)
</td>
<td style="border:1px solid black;">
Internet Explorer 6   
(2953522)  
(Moderada)  
Internet Explorer 7   
(2953522)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2932079)  
(Importante)  
Microsoft .NET Framework 4.0  
(2931365)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2926765)  
(Importante)
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
[**MS14-021**](http://go.microsoft.com/fwlink/?linkid=397669)
</td>
<td style="border:1px solid black;">
[**MS14-029**](http://go.microsoft.com/fwlink/?linkid=395261)
</td>
<td style="border:1px solid black;">
[**MS14-025**](http://go.microsoft.com/fwlink/?linkid=396820)
</td>
<td style="border:1px solid black;">
[**MS14-026**](http://go.microsoft.com/fwlink/?linkid=396825)
</td>
<td style="border:1px solid black;">
[**MS14-027**](http://go.microsoft.com/fwlink/?linkid=396823)
</td>
<td style="border:1px solid black;">
[**MS14-028**](http://go.microsoft.com/fwlink/?linkid=309325)
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
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2964358)  
(Crítica)  
Internet Explorer 8  
(2964358)  
(Crítica)  
Internet Explorer 9  
(2964358)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2953522)  
(Crítica)  
Internet Explorer 8  
(2953522)  
(Crítica)  
Internet Explorer 9  
(2953522)  
(Crítica)
</td>
<td style="border:1px solid black;">
Herramientas de administración remota del servidor  
(2928120)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2931354)  
(Importante)  
Microsoft .NET Framework 4.0  
(2931365)  
(Importante)  
Microsoft .NET Framework 4.5  
(2931368)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2931368)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2926765)  
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
(2964358)  
(Crítica)  
Internet Explorer 8  
(2964358)  
(Crítica)  
Internet Explorer 9  
(2964358)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2953522)  
(Crítica)  
Internet Explorer 8  
(2953522)  
(Crítica)  
Internet Explorer 9  
(2953522)  
(Crítica)
</td>
<td style="border:1px solid black;">
Herramientas de administración remota del servidor  
(2928120)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2931354)  
(Importante)  
Microsoft .NET Framework 4.0  
(2931365)  
(Importante)  
Microsoft .NET Framework 4.5  
(2931368)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2931368)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2926765)  
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
[**MS14-021**](http://go.microsoft.com/fwlink/?linkid=397669)
</td>
<td style="border:1px solid black;">
[**MS14-029**](http://go.microsoft.com/fwlink/?linkid=395261)
</td>
<td style="border:1px solid black;">
[**MS14-025**](http://go.microsoft.com/fwlink/?linkid=396820)
</td>
<td style="border:1px solid black;">
[**MS14-026**](http://go.microsoft.com/fwlink/?linkid=396825)
</td>
<td style="border:1px solid black;">
[**MS14-027**](http://go.microsoft.com/fwlink/?linkid=396823)
</td>
<td style="border:1px solid black;">
[**MS14-028**](http://go.microsoft.com/fwlink/?linkid=309325)
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
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2964358)  
(Moderada)  
Internet Explorer 8  
(2964358)  
(Moderada)  
Internet Explorer 9  
(2964358)  
(Moderada)
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2953522)  
(Moderada)  
Internet Explorer 8  
(2953522)  
(Moderada)  
Internet Explorer 9  
(2953522)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2928120)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2931354)  
(Importante)  
Microsoft .NET Framework 4.0  
(2931365)  
(Importante)  
Microsoft .NET Framework 4.5  
(2931368)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2931368)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2926765)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2964358)  
(Moderada)  
Internet Explorer 8  
(2964358)  
(Moderada)  
Internet Explorer 9  
(2964358)  
(Moderada)
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2953522)  
(Moderada)  
Internet Explorer 8  
(2953522)  
(Moderada)  
Internet Explorer 9  
(2953522)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2928120)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2931354)  
(Importante)  
Microsoft .NET Framework 4.0  
(2931365)  
(Importante)  
Microsoft .NET Framework 4.5  
(2931368)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2931368)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2926765)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2964358)  
(Moderada)
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2953522)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2928120)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2931354)  
(Importante)  
Microsoft .NET Framework 4.0  
(2931365)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2926765)  
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
[**MS14-021**](http://go.microsoft.com/fwlink/?linkid=397669)
</td>
<td style="border:1px solid black;">
[**MS14-029**](http://go.microsoft.com/fwlink/?linkid=395261)
</td>
<td style="border:1px solid black;">
[**MS14-025**](http://go.microsoft.com/fwlink/?linkid=396820)
</td>
<td style="border:1px solid black;">
[**MS14-026**](http://go.microsoft.com/fwlink/?linkid=396825)
</td>
<td style="border:1px solid black;">
[**MS14-027**](http://go.microsoft.com/fwlink/?linkid=396823)
</td>
<td style="border:1px solid black;">
[**MS14-028**](http://go.microsoft.com/fwlink/?linkid=309325)
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
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2964358)  
(Crítica)  
Internet Explorer 9  
(2964358)  
(Crítica)  
Internet Explorer 10  
(2964358)  
(Crítica)  
Internet Explorer 11  
(2964358)  
(Crítica)  
Internet Explorer 11  
(2964444)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2953522)  
(Crítica)  
Internet Explorer 9  
(2953522)  
(Crítica)  
Internet Explorer 10  
(2953522)  
(Crítica)  
Internet Explorer 11  
(2953522)  
(Crítica)  
Internet Explorer 11  
(2961851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Herramientas de administración remota del servidor  
(2928120)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2931356)  
(Importante)  
Microsoft .NET Framework 4.0  
(2931365)  
(Importante)  
Microsoft .NET Framework 4.5  
(2931368)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2931368)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2926765)  
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
(2964358)  
(Crítica)  
Internet Explorer 9  
(2964358)  
(Crítica)  
Internet Explorer 10  
(2964358)  
(Crítica)  
Internet Explorer 11  
(2964358)  
(Crítica)  
Internet Explorer 11  
(2964444)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2953522)  
(Crítica)  
Internet Explorer 9  
(2953522)  
(Crítica)  
Internet Explorer 10  
(2953522)  
(Crítica)  
Internet Explorer 11  
(2953522)  
(Crítica)  
Internet Explorer 11  
(2961851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Herramientas de administración remota del servidor  
(2928120)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2931356)  
(Importante)  
Microsoft .NET Framework 4.0  
(2931365)  
(Importante)  
Microsoft .NET Framework 4.5  
(2931368)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2931368)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2926765)  
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
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-021**](http://go.microsoft.com/fwlink/?linkid=397669)
</td>
<td style="border:1px solid black;">
[**MS14-029**](http://go.microsoft.com/fwlink/?linkid=395261)
</td>
<td style="border:1px solid black;">
[**MS14-025**](http://go.microsoft.com/fwlink/?linkid=396820)
</td>
<td style="border:1px solid black;">
[**MS14-026**](http://go.microsoft.com/fwlink/?linkid=396825)
</td>
<td style="border:1px solid black;">
[**MS14-027**](http://go.microsoft.com/fwlink/?linkid=396823)
</td>
<td style="border:1px solid black;">
[**MS14-028**](http://go.microsoft.com/fwlink/?linkid=309325)
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
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
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
(2964358)  
(Moderada)  
Internet Explorer 9  
(2964358)  
(Moderada)  
Internet Explorer 10  
(2964358)  
(Moderada)  
Internet Explorer 11  
(2964358)  
(Moderada)  
Internet Explorer 11  
(2964444)  
(Moderada)
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2953522)  
(Moderada)  
Internet Explorer 9  
(2953522)  
(Moderada)  
Internet Explorer 10  
(2953522)  
(Moderada)  
Internet Explorer 11  
(2953522)  
(Moderada)  
Internet Explorer 11  
(2961851)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2928120)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2931356)  
(Importante)  
Microsoft .NET Framework 4.0  
(2931365)  
(Importante)  
Microsoft .NET Framework 4.5  
(2931368)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2931368)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2926765)  
(Importante)
</td>
<td style="border:1px solid black;">
iSCSI Software Target 3.3  
(2933826)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2964358)  
(Moderada)
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2953522)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2928120)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2931356)  
(Importante)  
Microsoft .NET Framework 4.0  
(2931365)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2926765)  
(Importante)
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
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-021**](http://go.microsoft.com/fwlink/?linkid=397669)
</td>
<td style="border:1px solid black;">
[**MS14-029**](http://go.microsoft.com/fwlink/?linkid=395261)
</td>
<td style="border:1px solid black;">
[**MS14-025**](http://go.microsoft.com/fwlink/?linkid=396820)
</td>
<td style="border:1px solid black;">
[**MS14-026**](http://go.microsoft.com/fwlink/?linkid=396825)
</td>
<td style="border:1px solid black;">
[**MS14-027**](http://go.microsoft.com/fwlink/?linkid=396823)
</td>
<td style="border:1px solid black;">
[**MS14-028**](http://go.microsoft.com/fwlink/?linkid=309325)
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
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2964358)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2953522)  
(Crítica)
</td>
<td style="border:1px solid black;">
Herramientas de administración remota del servidor  
(2928120)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2931357)  
(Importante)  
Microsoft .NET Framework 4.5  
(2931367)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2931367)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2926765)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas x64
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2964358)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2953522)  
(Crítica)
</td>
<td style="border:1px solid black;">
Herramientas de administración remota del servidor  
(2928120)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2931357)  
(Importante)  
Microsoft .NET Framework 4.5  
(2931367)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2931367)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(2926765)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2964358)  
(Crítica)  
Internet Explorer 11  
(2964444)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2953522)  
(Crítica)  
Internet Explorer 11  
(2961851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Herramientas de administración remota del servidor  
(2928120)  
(Importante)  
Herramientas de administración remota del servidor  
(2961899)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2931358)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2931366)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(2926765)  
(Importante)  
Windows 8.1 para sistemas de 32 bits  
(2962123)  
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
(2964358)  
(Crítica)  
Internet Explorer 11  
(2964444)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2953522)  
(Crítica)  
Internet Explorer 11  
(2961851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Herramientas de administración remota del servidor  
(2928120)  
(Importante)  
Herramientas de administración remota del servidor  
(2961899)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2931358)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2931366)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(2926765)  
(Importante)  
Windows 8.1 para sistemas x64  
(2962123)  
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
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-021**](http://go.microsoft.com/fwlink/?linkid=397669)
</td>
<td style="border:1px solid black;">
[**MS14-029**](http://go.microsoft.com/fwlink/?linkid=395261)
</td>
<td style="border:1px solid black;">
[**MS14-025**](http://go.microsoft.com/fwlink/?linkid=396820)
</td>
<td style="border:1px solid black;">
[**MS14-026**](http://go.microsoft.com/fwlink/?linkid=396825)
</td>
<td style="border:1px solid black;">
[**MS14-027**](http://go.microsoft.com/fwlink/?linkid=396823)
</td>
<td style="border:1px solid black;">
[**MS14-028**](http://go.microsoft.com/fwlink/?linkid=309325)
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
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
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
(2964358)  
(Moderada)
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2953522)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2928120)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2931357)  
(Importante)  
Microsoft .NET Framework 4.5  
(2931367)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2931367)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2926765)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2933826)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012 R2
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2964358)  
(Moderada)  
Internet Explorer 11  
(2964444)  
(Moderada)
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2953522)  
(Moderada)  
Internet Explorer 11  
(2961851)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(2928120)  
(Importante)  
Windows Server 2012 R2  
(2961899)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2931358)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2931366)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(2926765)  
(Importante)  
Windows Server 2012 R2  
(2962123)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(2933826)  
(Importante)  
Windows Server 2012 R2  
(2962073)  
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
[**MS14-021**](http://go.microsoft.com/fwlink/?linkid=397669)
</td>
<td style="border:1px solid black;">
[**MS14-029**](http://go.microsoft.com/fwlink/?linkid=395261)
</td>
<td style="border:1px solid black;">
[**MS14-025**](http://go.microsoft.com/fwlink/?linkid=396820)
</td>
<td style="border:1px solid black;">
[**MS14-026**](http://go.microsoft.com/fwlink/?linkid=396825)
</td>
<td style="border:1px solid black;">
[**MS14-027**](http://go.microsoft.com/fwlink/?linkid=396823)
</td>
<td style="border:1px solid black;">
[**MS14-028**](http://go.microsoft.com/fwlink/?linkid=309325)
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows RT
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2964358)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2953522)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 4.5  
(2931367)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2931367)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT  
(2926765)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows RT 8.1
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2964358)  
(Crítica)  
Internet Explorer 11  
(2964444)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2953522)  
(Crítica)  
Internet Explorer 11  
(2961851)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 4.5.1  
(2931366)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(2926765)  
(Importante)  
Windows RT 8.1  
(2962123)  
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
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-021**](http://go.microsoft.com/fwlink/?linkid=397669)
</td>
<td style="border:1px solid black;">
[**MS14-029**](http://go.microsoft.com/fwlink/?linkid=395261)
</td>
<td style="border:1px solid black;">
[**MS14-025**](http://go.microsoft.com/fwlink/?linkid=396820)
</td>
<td style="border:1px solid black;">
[**MS14-026**](http://go.microsoft.com/fwlink/?linkid=396825)
</td>
<td style="border:1px solid black;">
[**MS14-027**](http://go.microsoft.com/fwlink/?linkid=396823)
</td>
<td style="border:1px solid black;">
[**MS14-028**](http://go.microsoft.com/fwlink/?linkid=309325)
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
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2926765)  
(Importante)
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
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2926765)  
(Importante)
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
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2931356)  
(Importante)  
Microsoft .NET Framework 4.0  
(2931365)  
(Importante)  
Microsoft .NET Framework 4.5  
(2931368)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2931368)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2926765)  
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
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2931357)  
(Importante)  
Microsoft .NET Framework 4.5  
(2931367)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2931367)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(2926765)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(2933826)  
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
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2931358)  
(Importante)  
Microsoft .NET Framework 4.5.1  
(2931366)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(2926765)  
(Importante)  
Windows Server 2012 R2 (instalación Server Core)  
(2962123)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(2933826)  
(Importante)  
Windows Server 2012 R2 (instalación Server Core)  
(2962073)  
(Importante)
</td>
</tr>
</table>
 
 

### Conjuntos de programas y software de Office

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="3">
**Microsoft Office 2007**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-023**](http://go.microsoft.com/fwlink/?linkid=393745)
</td>
<td style="border:1px solid black;">
[**MS14-024**](http://go.microsoft.com/fwlink/?linkid=396835)
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
<tr>
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 3 (herramientas de corrección)  
(2767772)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 3 (mscomct2)  
(2596804)  
(Importante)  
Microsoft Office 2007 Service Pack 3 (mscomctlocx)  
(2817330)  
(Importante)  
Microsoft Office 2007 Service Pack 3 (msaddndr)  
(2880508)  
(Importante)  
Microsoft Office 2007 Service Pack 3 (msstdfmt)  
(2880507)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="3">
**Microsoft Office 2010**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-023**](http://go.microsoft.com/fwlink/?linkid=393745)
</td>
<td style="border:1px solid black;">
[**MS14-024**](http://go.microsoft.com/fwlink/?linkid=396835)
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
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits) (herramientas de corrección)  
(2878284)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits) (mscomct2)  
(2589288)  
(Importante)  
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits) (mscomctlocx)  
(2810073)  
(Importante)  
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits) (msaddndr)  
(2880971)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 32 bits) (herramientas de corrección)  
(2878284)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 32 bits) (mscomct2)  
(2589288)  
(Importante)  
Microsoft Office 2010 Service Pack 2 (ediciones de 32 bits) (mscomctlocx)  
(2810073)  
(Importante)  
Microsoft Office 2010 Service Pack 2 (ediciones de 32 bits) (msaddndr)  
(2880971)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits) (herramientas de corrección)  
(2878284)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits) (mscomct2)  
(2589288)  
(Importante)  
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits) (msaddndr)  
(2880971)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 64 bits) (herramientas de corrección)  
(2878284)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 64 bits) (mscomct2)  
(2589288)  
(Importante)  
Microsoft Office 2010 Service Pack 2 (ediciones de 64 bits) (msaddndr)  
(2880971)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="3">
**Microsoft Office 2013 y Microsoft Office 2013 RT**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-023**](http://go.microsoft.com/fwlink/?linkid=393745)
</td>
<td style="border:1px solid black;">
[**MS14-024**](http://go.microsoft.com/fwlink/?linkid=396835)
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
<tr>
<td style="border:1px solid black;">
Microsoft Office 2013 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office 2013 (ediciones de 32 bits) (herramientas de corrección)  
(2880463)  
(Importante)  
Microsoft Office 2013 (ediciones de 32 bits) (mso)  
(2878316)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Office 2013 (ediciones de 32 bits) (mscomct2)  
(2760272)  
(Importante)  
Microsoft Office 2013 (ediciones de 32 bits) (mscomctlocx)  
(2880502)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2013 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office 2013 Service Pack 1 (ediciones de 32 bits) (herramientas de corrección)  
(2880463)  
(Importante)  
Microsoft Office 2013 Service Pack 1 (ediciones de 32 bits) (mso) (2878316)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Office 2013 Service Pack 1 (ediciones de 32 bits) (mscomct2)  
(2760272)  
(Importante)  
Microsoft Office 2013 Service Pack 1 (ediciones de 32 bits) (mscomctlocx)  
(2880502)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2013 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office 2013 (ediciones de 64 bits) (herramientas de corrección)  
(2880463)  
(Importante)  
Microsoft Office 2013 (ediciones de 64 bits) (mso)  
(2878316)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Office 2013 (ediciones de 64 bits) (mscomct2)  
(2760272)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2013 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office 2013 Service Pack 1 (ediciones de 64 bits) (herramientas de corrección)  
(2880463)  
(Importante)  
Microsoft Office 2013 Service Pack 1 (ediciones de 64 bits) (mso)  
(2878316)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Office 2013 Service Pack 1 (ediciones de 64 bits) (mscomct2)  
(2760272)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="3">
**Microsoft Office 2013 RT**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-023**](http://go.microsoft.com/fwlink/?linkid=393745)
</td>
<td style="border:1px solid black;">
[**MS14-024**](http://go.microsoft.com/fwlink/?linkid=396835)
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
<tr>
<td style="border:1px solid black;">
Microsoft Office 2013 RT
</td>
<td style="border:1px solid black;">
Microsoft Office 2013 RT (herramientas de corrección)  
(2880463)  
(Importante)  
Microsoft Office 2013 RT (mso)  
(2878316)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Office 2013 RT (mscomct2)  
(2760272)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2013 RT Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft Office 2013 RT Service Pack 1 (herramientas de corrección)  
(2880463)  
(Importante)  
Microsoft Office 2013 RT Service Pack 1 (mso)  
(2878316)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Office 2013 RT Service Pack 1 (mscomct2)  
(2760272)  
(Importante)
</td>
</tr>
</table>
 
 

### Software de servidor de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="2">
**Microsoft SharePoint Server 2007**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-022**](http://go.microsoft.com/fwlink/?linkid=386285)
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
Microsoft SharePoint Server 2007 Service Pack 3 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Windows SharePoint Services 3.0 Service Pack 3 (versiones de 32 bits)  
(2837616)  
(Crítica)  
SharePoint Server 2007 Service Pack 3 (ediciones de 32 bits) (dlcapp)  
(2596902)  
(Crítica)  
SharePoint Server 2007 Service Pack 3 (ediciones de 32 bits) (dlc)  
(2596763)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2007 Service Pack 3 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Windows SharePoint Services 3.0 Service Pack 3 (versiones de 64 bits)  
(2837616)  
(Crítica)  
SharePoint Server 2007 Service Pack 3 (ediciones de 64 bits) (dlcapp)  
(2596902)  
(Crítica)  
SharePoint Server 2007 Service Pack 3 (ediciones de 64 bits) (dlc)  
(2596763)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="2">
**Microsoft SharePoint Server 2010**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-022**](http://go.microsoft.com/fwlink/?linkid=386285)
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
Microsoft SharePoint Server 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Foundation 2010 Service Pack 1 (wss)  
(2837588)  
(Crítica)  
Microsoft SharePoint Server 2010 Service Pack 1 (coreserver)  
(2837598)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2010 Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Foundation 2010 Service Pack 2 (wss)  
(2837588)  
(Crítica)  
Microsoft SharePoint Server 2010 Service Pack 2 (coreserver)  
(2837598)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="2">
**Microsoft SharePoint Server 2013**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-022**](http://go.microsoft.com/fwlink/?linkid=386285)
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
Microsoft SharePoint Server 2013
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Foundation 2013 (sts)  
(2863856)  
(Crítica)  
Microsoft SharePoint Foundation 2013 (wssloc)  
(2863863)  
(Crítica)  
Microsoft SharePoint Server 2013 (coreserverloc)  
(2863829)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2013 Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Foundation 2013 Service Pack 1 (sts)  
(2863856)  
(Crítica)  
Microsoft SharePoint Foundation 2013 Service Pack 1 (wssloc)  
(2863863)  
(Crítica)  
Microsoft SharePoint Server 2013 Service Pack 1 (coreserver)  
(2863829)  
(Crítica)
</td>
</tr>
</table>
 
**Nota para MS14-022**

Este boletín abarca varias categorías de software. Vea las demás tablas de esta sección para determinar el software afectado.

 

### Microsoft Office Services y Web Apps

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="2">
**Microsoft SharePoint Server 2010**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-022**](http://go.microsoft.com/fwlink/?linkid=386285)
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
Microsoft SharePoint Server 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft Project Server 2010 Service Pack 1  
(2863922)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2010 Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft Project Server 2010 Service Pack 2  
(2863922)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="2">
**Microsoft SharePoint Server 2013**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-022**](http://go.microsoft.com/fwlink/?linkid=386285)
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
Microsoft SharePoint Server 2013
</td>
<td style="border:1px solid black;">
Microsoft Project Server 2013  
(2760236)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2013 Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft Project Server 2013 Service Pack 1  
(2760236)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="2">
**Microsoft Office Web Apps 2010**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-022**](http://go.microsoft.com/fwlink/?linkid=386285)
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
Microsoft Office Web Apps 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft Web Applications 2010 Service Pack 1  
(2880536)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Web Apps 2010 Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft Web Applications 2010 Service Pack 2  
(2880536)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="2">
**Microsoft Office Web Apps 2013**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-022**](http://go.microsoft.com/fwlink/?linkid=386285)
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
Microsoft Office Web Apps 2013
</td>
<td style="border:1px solid black;">
Microsoft Office Web Apps Server 2013  
(2880453)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Web Apps 2013 Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft Office Web Apps Server 2013 Service Pack 1  
(2880453)  
(Crítica)
</td>
</tr>
</table>
 
**Nota para MS14-022**

Este boletín abarca varias categorías de software. Vea las demás tablas de esta sección para determinar el software afectado.

 

### Software de productividad

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="2">
**SDK de componentes de cliente de SharePoint Server 2013**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-022**](http://go.microsoft.com/fwlink/?linkid=386285)
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
SDK de componentes de cliente de SharePoint Server 2013 (versión de 32 bits)
</td>
<td style="border:1px solid black;">
SDK de componentes de cliente de SharePoint Server 2013 (versión de 32 bits)  
(2863854)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
SDK de componentes de cliente de SharePoint Server 2013 (versión de 64 bits)
</td>
<td style="border:1px solid black;">
SDK de componentes de cliente de SharePoint Server 2013 (versión de 64 bits)  
(2863854)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="2">
**Microsoft SharePoint Designer 2007**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-022**](http://go.microsoft.com/fwlink/?linkid=386285)
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
Microsoft SharePoint Designer 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Designer 2007 Service Pack 3 (ewd)  
(2596861)  
(Crítica)  
Microsoft SharePoint Designer 2007 Service Pack 3 (spd)  
(2596810)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="2">
**Microsoft SharePoint Designer 2010**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-022**](http://go.microsoft.com/fwlink/?linkid=386285)
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
Microsoft SharePoint Designer 2010 Service Pack 1 (versiones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Designer 2010 Service Pack 1 (versiones de 32 bits)  
(2810069)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Designer 2010 Service Pack 2 (versiones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Designer 2010 Service Pack 2 (versiones de 32 bits)  
(2810069)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Designer 2010 Service Pack 1 (versiones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Designer 2010 Service Pack 1 (versiones de 64 bits)  
(2810069)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Designer 2010 Service Pack 2 (versiones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Designer 2010 Service Pack 2 (versiones de 64 bits)  
(2810069)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Microsoft SharePoint Designer 2013**
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-022**](http://go.microsoft.com/fwlink/?linkid=386285)
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
Microsoft SharePoint Designer 2013 (versiones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Designer 2013 (versiones de 32 bits) (spdcore)  
(2752096)  
(Crítica)  
Microsoft SharePoint Designer 2013 (versiones de 32 bits) (spd)  
(2863836)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Designer 2013 Service Pack 1 (versiones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Designer 2013 Service Pack 1 (versiones de 32 bits) (spdcore)  
(2752096)  
(Crítica)  
Microsoft SharePoint Designer 2013 Service Pack 1 (versiones de 32 bits) (spd)  
(2863836)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Designer 2013 (versiones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Designer 2013 (versiones de 64 bits) (spdcore)  
(2752096)  
(Crítica)  
Microsoft SharePoint Designer 2013 (versiones de 64 bits) (spd)  
(2863836)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Designer 2013 Service Pack 1 (versiones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Designer 2013 Service Pack 1 (versiones de 64 bits) (spdcore)  
(2752096)  
(Crítica)  
Microsoft SharePoint Designer 2013 Service Pack 1 (versiones de 64 bits) (spd)  
(2863836)  
(Crítica)
</td>
</tr>
</table>
 
**Nota para MS14-022**

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

**MS14-021**

-   [FireEye Co.](http://www2.fireeye.com/), por colaborar con nosotros en la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-1776)

     

**MS14-023**

-   [NSFOCUS Security Team](http://www.nsfocus.com/), por informar de la vulnerabilidad en la corrección gramatical para chino en Microsoft Office (CVE-2014-1756)
-   Arnaud Maillet, de [ANSSI](http://www.ssi.gouv.fr/), por informar de la vulnerabilidad de reutilización de token (CVE-2014-1808)

     

**MS14-026**

-   James Forshaw, de [Context Information Security](http://www.contextis.com/), por informar de la vulnerabilidad de TypeFilterLevel (CVE-2014-1806)

     

**MS14-028**

-   Un investigador anónimo, en colaboración con el proyecto [SecuriTeam Secure Disclosure](http://www.beyondsecurity.com/ssd.html) de Beyond Security, por informar de la vulnerabilidad de denegación de servicio remoto en destino iSCSI (CVE-2014-0255)
-   Un investigador anónimo, en colaboración con el proyecto [SecuriTeam Secure Disclosure](http://www.beyondsecurity.com/ssd.html) de Beyond Security, por informar de la vulnerabilidad de denegación de servicio remoto en destino iSCSI (CVE-2014-0256)

     

**MS14-029**

-   Fermín J. Serna, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0310)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-0310)
-   Clément Lecigne, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2014-1815)

     

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

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

### Revisiones

-   V1.0 (1 de mayo de 2014): Publicación del resumen del boletín.
-   V2.0 (13 de mayo de 2014): se han agregado los boletines del MS13-022 al MS13-029 y se ha agregado el vínculo de la difusión por web de boletín del 14 de mayo.

*Página generada el 2014-05-14 10:22Z-07:00.*
