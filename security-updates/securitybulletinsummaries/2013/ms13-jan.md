---
TOCTitle: 'MS13-JAN'
Title: Resumen del boletín de seguridad de Microsoft de enero 2013
ms:assetid: 'ms13-jan'
ms:contentKeyID: 61225448
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms13-jan(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de enero 2013
===========================================================

Publicado: martes, 8 de enero de 2013 | Actualizado: martes, 12 de marzo de 2013

**Versión:** 4.0

Este resumen del boletín enumera los boletines de seguridad publicados para enero de 2013.

Con la publicación de los boletines de seguridad de enero de 2013, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 3 de enero de 2013 y la notificación de avance fuera de ciclo publicada el 13 de enero de 2013. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 9 de enero de 2013, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora a la conferencia en línea del boletín de seguridad de enero](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032538623&culture=en-us). Después de esta fecha, este webcast estará disponible [a petición](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032538623&culture=en-us).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre el boletín de seguridad fuera de ciclo el 14 de enero de 2013, a la 1:00 p.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad fuera de ciclo el 14 de enero de 2013](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032541648&culture=en-us). Después de esta fecha, este webcast estará disponible [a petición](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032541648&culture=en-us).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

### Información del boletín

#### Resúmenes ejecutivos

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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275222">MS13-008</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad para Internet Explorer (2799329)  <br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública en Internet Explorer. La vulnerabilidad podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. Un atacante que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, <br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=273848">MS13-001</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en los componentes del servicio de administrador de trabajos de impresión podría permitir la ejecución remota de código (2769369)  <br />
<br />
</strong>Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un servidor de impresión recibe un trabajo de impresión especialmente diseñado. Los procedimientos recomendados para firewall y las configuraciones de firewall predeterminadas estándar pueden proteger a las redes de los ataques procedentes del exterior del perímetro de la empresa. Se recomienda que los sistemas conectados directamente a Internet tengan expuesta una cantidad mínima de puertos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=264923">MS13-002</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft XML</strong> <strong>CoreServicespodrían</strong> <strong>permitir</strong> <strong>la ejecución remota de código (2756145)</strong> <br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft XML Core Services. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. El atacante no podría obligar a los usuarios a visitar dicho sitio web. Por lo tanto, tendría que atraerlos al sitio web; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger que lleve a los usuarios al sitio web del atacante.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, <br />
Microsoft Office, <br />
Herramientas de desarrollo de Microsoft,  <br />
Software de servidor de Microsoft</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=261863">MS13-003</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en</strong> <strong>System</strong> <strong>Center</strong> <strong>Operations</strong> <strong>Manager</strong> <strong>podrían</strong> <strong>permitir la elevación de privilegios (2748552)  <br />
<br />
</strong>Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft System Center Operations Manager. Las vulnerabilidades podrían permitir la elevación de privilegios si un usuario visita un sitio web afectado mediante una dirección URL especialmente diseñada. El atacante no podría obligar a los usuarios a visitar dicho sitio web. Por lo tanto, tendría que atraerlos al sitio web; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger que lleve a los usuarios al sitio web afectado.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">No requiere reinicio</td>
<td style="border:1px solid black;">Software de servidor de Microsoft</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=268279">MS13-004</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en .NET Framework podrían permitir la elevación de privilegios (2769324)  <br />
<br />
</strong>Esta actualización de seguridad resuelve cuatro vulnerabilidades de las que se ha informado de forma privadaen .NET Framework. La más grave de estas vulnerabilidades podría permitir la elevación de privilegios si un usuario visita una página web especialmente diseñada mediante un explorador web que pueda ejecutar aplicaciones XAML del explorador (XBAP). Las vulnerabilidades también las podrían usar aplicaciones Windows .NET para omitir las restricciones de seguridad de acceso del código (CAS). Un intruso que aprovechara estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario que ha iniciado sesión. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Microsoft .NET Framework</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=273826">MS13-005</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el controlador en modo</strong> <strong>kernel</strong> <strong>de Windows podría permitir la elevación de privilegios (2778930)  <br />
<br />
</strong>Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si un atacante ejecuta una aplicación especialmente diseñada.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=273872">MS13-006</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Windows podría permitir la omisión de característica de seguridad (2785220)  <br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en la implementación de SSL y TLS en Microsoft Windows. La vulnerabilidad podría permitir la omisión de la característica de seguridad si un atacante intercepta protocolos de enlace de tráfico web cifrado.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Omisión de característica de seguridad</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=268284">MS13-007</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el protocolo Open Data podría provocar la denegación de servicio (2769327)  <br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en el protocolo Open Data (OData). La vulnerabilidad podría permitir la denegación de servicio si un usuario sin autentica envía solicitudes HTTP especialmente diseñadas a un sitio afectado. Los procedimientos recomendados para firewall y las configuraciones de firewall predeterminadas estándar pueden proteger a las redes de los ataques procedentes del exterior del perímetro de la empresa. Se recomienda que los sistemas conectados a Internet tengan expuesta la cantidad mínima de puertos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Denegación de servicio</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Microsoft .NET Framework</td>
</tr>
</tbody>
</table>
 

Índice de explotabilidad
------------------------

La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y, a continuación, por identificador de CVE. Sólo se incluyen las vulnerabilidades que tiene una clasificación de gravedad de crítica o importante en los boletines.

**¿Cómo se usa esta tabla?**  

Use esta tabla para obtener información acerca de la probabilidad de las vulnerabilidades de ejecución de código y de denegación de servicio en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Revise cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación de las actualizaciones de este mes. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/es-es/security/cc998259.aspx).

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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=273848">MS13-001</a></td>
<td style="border:1px solid black;">Vulnerabilidad en los componentes del servicio de administrador de trabajos de impresión de Windows</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0011">CVE-2013-0011</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=264923">MS13-002</a></td>
<td style="border:1px solid black;">Vulnerabilidad de truncamiento de enteros en MSXML</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0006">CVE-2013-0006</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=264923">MS13-002</a></td>
<td style="border:1px solid black;">Vulnerabilidad de XSLT en MSXML</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0007">CVE-2013-0007</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=261863">MS13-003</a></td>
<td style="border:1px solid black;">Vulnerabilidad de XSS en la consola web de System Center Operations Manager</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0009">CVE-2013-0009</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=261863">MS13-003</a></td>
<td style="border:1px solid black;">Vulnerabilidad de XSS en la consola web de System Center Operations Manager</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0010">CVE-2013-0010</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=268279">MS13-004</a></td>
<td style="border:1px solid black;">Vulnerabilidad de desbordamiento del búfer en WinForms</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0002">CVE-2013-0002</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=268279">MS13-004</a></td>
<td style="border:1px solid black;">Vulnerabilidad de desbordamiento del búfer en S.DS.P</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0003">CVE-2013-0003</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=268279">MS13-004</a></td>
<td style="border:1px solid black;">Vulnerabilidad de doble construcción</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0004">CVE-2013-0004</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=273826">MS13-005</a></td>
<td style="border:1px solid black;">Vulnerabilidad de tratamiento de mensajes incorrecto en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0008">CVE-2013-0008</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=273872">MS13-006</a></td>
<td style="border:1px solid black;">Vulnerabilidad de omisión de característica de seguridad en los protocolos SSL versión 3 y TLS</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0013">CVE-2013-0013</a></td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Es una vulnerabilidad de omisión de característica de seguridad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=268284">MS13-007</a></td>
<td style="border:1px solid black;">Vulnerabilidad de denegación de servicio en el reemplazo</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0005">CVE-2013-0005</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275222">MS13-008</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de Internet Explorer después de la liberación</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-4792">CVE-2012-4792</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.<br />
<br />
Microsoft tiene constancia de ataques dirigidos que intentan aprovechar esta vulnerabilidad a través de Internet Explorer 8.</td>
</tr>
</tbody>
</table>
 

Ubicaciones de descarga y software afectado
-------------------------------------------

Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.

**¿Cómo se usan estas tablas?**  

Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, se indica un hipervínculo a la actualización de software disponible y también se muestra la clasificación de gravedad de dicha actualización de software.

**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.

#### Componentes y sistema operativo Windows

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="8" style="border:1px solid black;">
Windows XP
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-008**](http://go.microsoft.com/fwlink/?linkid=275222)
</td>
<td style="border:1px solid black;">
[**MS13-001**](http://go.microsoft.com/fwlink/?linkid=273848)
</td>
<td style="border:1px solid black;">
[**MS13-002**](http://go.microsoft.com/fwlink/?linkid=264923)
</td>
<td style="border:1px solid black;">
[**MS13-004**](http://go.microsoft.com/fwlink/?linkid=268279)
</td>
<td style="border:1px solid black;">
[**MS13-005**](http://go.microsoft.com/fwlink/?linkid=273826)
</td>
<td style="border:1px solid black;">
[**MS13-006**](http://go.microsoft.com/fwlink/?linkid=273872)
</td>
<td style="border:1px solid black;">
[**MS13-007**](http://go.microsoft.com/fwlink/?linkid=268284)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
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
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=20d8d873-a709-4834-a956-f3d9d82dbb73)   
(KB2799329)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=dcdcf814-e39d-4515-bc5d-12e11f214d08)  
(KB2799329)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=4e0d584a-c684-408c-bc47-6bd4ecaa9b8a)  
(KB2799329)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1e2738b9-d3c2-4dfe-8a79-335d5feee55b)  
(KB2758694)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=137cc5ee-abf0-4a10-b1c4-d464331cbcfd)  
(KB2757638)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.0 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=155a2984-2cd9-40a4-abaa-c1ea21e76062)  
(KB2742607)  
(Media Center Edition 2005 Service Pack 3 y Tablet PC Edition 2005 Service Pack 3 solo)  
(Importante)  
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5091f66f-9b89-496f-95ce-9ac556faa7b5)  
(KB2742597)  
(Importante)  
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8e2cc005-08c5-4e47-b05a-5b36fe539610)  
(KB2742596)  
(Importante)  
[Microsoft .NET Framework 3.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=20d07bcd-95cc-44a2-8e3e-f88b22682e21)  
(KB2756918)  
(Sin clasificación de gravedad<sup>[2]</sup>)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b476d44d-8a79-4857-8c3e-9d547e9b9e2d)  
(KB2736416)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=f35f2ea5-d60e-405a-9ed3-248e0d733c2b)   
(KB2799329)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=36c9d6a9-d939-4e19-b9f5-576fee048764)  
(KB2799329)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=396f26bd-8c8b-459d-9467-6ec17a11c9d4)  
(KB2799329)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=d147f865-6a56-4db2-8d78-14f2bee6da18)  
(KB2757638)  
(Crítica)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=7dabf372-4b31-4c9e-a660-4e0f4a65db04)  
(KB2758694)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=0b13a83c-1e51-4604-a09d-afb2e25646f9)  
(KB2758696)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5091f66f-9b89-496f-95ce-9ac556faa7b5)  
(KB2742597)  
(Importante)  
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8e2cc005-08c5-4e47-b05a-5b36fe539610)  
(KB2742596)  
(Importante)  
[Microsoft .NET Framework 3.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=20d07bcd-95cc-44a2-8e3e-f88b22682e21)  
(KB2756918)  
(Sin clasificación de gravedad<sup>[2]</sup>)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b476d44d-8a79-4857-8c3e-9d547e9b9e2d)  
(KB2736416)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr>
<th colspan="8" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-008**](http://go.microsoft.com/fwlink/?linkid=275222)
</td>
<td style="border:1px solid black;">
[**MS13-001**](http://go.microsoft.com/fwlink/?linkid=273848)
</td>
<td style="border:1px solid black;">
[**MS13-002**](http://go.microsoft.com/fwlink/?linkid=264923)
</td>
<td style="border:1px solid black;">
[**MS13-004**](http://go.microsoft.com/fwlink/?linkid=268279)
</td>
<td style="border:1px solid black;">
[**MS13-005**](http://go.microsoft.com/fwlink/?linkid=273826)
</td>
<td style="border:1px solid black;">
[**MS13-006**](http://go.microsoft.com/fwlink/?linkid=273872)
</td>
<td style="border:1px solid black;">
[**MS13-007**](http://go.microsoft.com/fwlink/?linkid=268284)
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
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
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
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=1a7cfc5a-2872-4516-a371-f42d4d3969a6)   
(KB2799329)  
(Moderada)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=4b7c2bcd-a732-46ba-9d09-cc192efd4755)  
(KB2799329)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=7f134d1c-670d-4528-b755-22124aa4d8c9)  
(KB2799329)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1e2738b9-d3c2-4dfe-8a79-335d5feee55b)  
(KB2758694)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=6a12de5f-de80-48e4-8276-6c420f5a2948)  
(KB2758696)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=f1a2eb6e-0290-4a53-b93c-017a48b19973)  
(KB2742604)  
(Importante)  
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8e2cc005-08c5-4e47-b05a-5b36fe539610)  
(KB2742596)  
(Importante)  
[Microsoft .NET Framework 3.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=20d07bcd-95cc-44a2-8e3e-f88b22682e21)  
(KB2756918)  
(Sin clasificación de gravedad<sup>[2]</sup>)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b476d44d-8a79-4857-8c3e-9d547e9b9e2d)  
(KB2736416)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=00304f3b-069f-49dc-a416-b0b5fb97aa4b)   
(KB2799329)  
(Moderada)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=4911899c-863f-4499-9477-340ef8daad29)  
(KB2799329)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=b0cf6516-aea6-4879-9a6e-171d4825ae20)  
(KB2799329)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=29985fdc-8aba-44b2-9420-970ca475052e)  
(KB2757638)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=7dabf372-4b31-4c9e-a660-4e0f4a65db04)  
(KB2758694)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=0b13a83c-1e51-4604-a09d-afb2e25646f9)  
(KB2758696)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5091f66f-9b89-496f-95ce-9ac556faa7b5)  
(KB2742597)  
(Importante)  
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8e2cc005-08c5-4e47-b05a-5b36fe539610)  
(KB2742596)  
(Importante)  
[Microsoft .NET Framework 3.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=20d07bcd-95cc-44a2-8e3e-f88b22682e21)  
(KB2756918)  
(Sin clasificación de gravedad<sup>[2]</sup>)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b476d44d-8a79-4857-8c3e-9d547e9b9e2d)  
(KB2736416)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=b2c635b7-56ad-426b-8bd6-4aee9deadb69)   
(KB2799329)  
(Moderada)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=b33197ab-f489-4c11-a229-044b186d7dda)  
(KB2799329)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=bca95077-a28f-406c-9fe4-51dbcf6adee8)  
(KB2757638)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=4719776a-5ff0-491a-934e-99220d8ac3a3)  
(KB2758694)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=fb834cf7-d1fe-4291-8a0d-c866fdbdf0e6)  
(KB2758696)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5091f66f-9b89-496f-95ce-9ac556faa7b5)  
(KB2742597)  
(Importante)  
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8e2cc005-08c5-4e47-b05a-5b36fe539610)  
(KB2742596)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b476d44d-8a79-4857-8c3e-9d547e9b9e2d)  
(KB2736416)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr>
<th colspan="8" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-008**](http://go.microsoft.com/fwlink/?linkid=275222)
</td>
<td style="border:1px solid black;">
[**MS13-001**](http://go.microsoft.com/fwlink/?linkid=273848)
</td>
<td style="border:1px solid black;">
[**MS13-002**](http://go.microsoft.com/fwlink/?linkid=264923)
</td>
<td style="border:1px solid black;">
[**MS13-004**](http://go.microsoft.com/fwlink/?linkid=268279)
</td>
<td style="border:1px solid black;">
[**MS13-005**](http://go.microsoft.com/fwlink/?linkid=273826)
</td>
<td style="border:1px solid black;">
[**MS13-006**](http://go.microsoft.com/fwlink/?linkid=273872)
</td>
<td style="border:1px solid black;">
[**MS13-007**](http://go.microsoft.com/fwlink/?linkid=268284)
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
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=95d603e8-9440-4aa6-9765-20c77a55966a)  
(KB2799329)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=64b498a6-54fc-4b88-bcc3-2cc15a16abb5)  
(KB2799329)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1e2738b9-d3c2-4dfe-8a79-335d5feee55b)  
(KB2758694)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=d477235d-60f4-420d-8161-82194b4e62e7)  
(KB2757638)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5091f66f-9b89-496f-95ce-9ac556faa7b5)  
(KB2742597)  
(Importante)  
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=39406634-48ad-4ecf-a6be-f5a47885704b)  
(KB2742601)  
(Importante)  
[Microsoft .NET Framework 3.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b8cb7a04-f913-47cc-96c1-27fb7154a791)  
(KB2756919)  
(Sin clasificación de gravedad<sup>[2]</sup>)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=dafc6924-d798-46b4-9fa5-ea7c35f06fa0)  
(KB2742613)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8b1aef73-cfb2-4998-bca6-35cccfbb2078)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3107fadf-5ba8-48f6-bb23-0c0003b4ba76)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b476d44d-8a79-4857-8c3e-9d547e9b9e2d)  
(KB2736416)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=a35ccbff-c476-4ee2-be9c-5b6a4b1664e9)  
(KB2799329)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=b427bace-5297-4593-9dd2-66847ae506c6)  
(KB2799329)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=873eba5d-5a8f-410e-bad8-e9d538acf1b3)  
(KB2757638)  
(Crítica)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=7dabf372-4b31-4c9e-a660-4e0f4a65db04)  
(KB2758694)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=873eba5d-5a8f-410e-bad8-e9d538acf1b3)  
(KB2757638)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5091f66f-9b89-496f-95ce-9ac556faa7b5)  
(KB2742597)  
(Importante)  
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=39406634-48ad-4ecf-a6be-f5a47885704b)  
(KB2742601)  
(Importante)  
[Microsoft .NET Framework 3.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b8cb7a04-f913-47cc-96c1-27fb7154a791)  
(KB2756919)  
(Sin clasificación de gravedad<sup>[2]</sup>)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=dafc6924-d798-46b4-9fa5-ea7c35f06fa0)  
(KB2742613)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4287381f-6f23-4a36-a7dc-f79c44bac124)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=098958e5-83cd-4ed2-b758-e970cef33325)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b476d44d-8a79-4857-8c3e-9d547e9b9e2d)  
(KB2736416)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr>
<th colspan="8" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-008**](http://go.microsoft.com/fwlink/?linkid=275222)
</td>
<td style="border:1px solid black;">
[**MS13-001**](http://go.microsoft.com/fwlink/?linkid=273848)
</td>
<td style="border:1px solid black;">
[**MS13-002**](http://go.microsoft.com/fwlink/?linkid=264923)
</td>
<td style="border:1px solid black;">
[**MS13-004**](http://go.microsoft.com/fwlink/?linkid=268279)
</td>
<td style="border:1px solid black;">
[**MS13-005**](http://go.microsoft.com/fwlink/?linkid=273826)
</td>
<td style="border:1px solid black;">
[**MS13-006**](http://go.microsoft.com/fwlink/?linkid=273872)
</td>
<td style="border:1px solid black;">
[**MS13-007**](http://go.microsoft.com/fwlink/?linkid=268284)
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
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=3ce450f1-f71f-4d5d-bf1c-db4742522d18)  
(KB2799329)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=2d1266fc-f6b0-4062-9799-7b3721c2cf52)  
(KB2799329)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1e2738b9-d3c2-4dfe-8a79-335d5feee55b)  
(KB2758694)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=e6439fef-e5e7-479b-8fc4-daacf3a39f3a)  
(KB2757638)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5091f66f-9b89-496f-95ce-9ac556faa7b5)  
(KB2742597)  
(Importante)  
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=39406634-48ad-4ecf-a6be-f5a47885704b)  
(KB2742601)  
(Importante)  
[Microsoft .NET Framework 3.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b8cb7a04-f913-47cc-96c1-27fb7154a791)  
(KB2756919)  
(Sin clasificación de gravedad<sup>[2]</sup>)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=dafc6924-d798-46b4-9fa5-ea7c35f06fa0)  
(KB2742613)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c635ad51-4e15-461c-8927-a86d79f90b45)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b3ed781e-b740-4153-aaf3-daafdeb91004)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b476d44d-8a79-4857-8c3e-9d547e9b9e2d)  
(KB2736416)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=0f87dd60-92c2-444c-a9ea-dfeb106c88fa)  
(KB2799329)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=2f71f8e6-309c-4bea-abde-d91040c46611)  
(KB2799329)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=1511377b-0adc-455f-8caa-f3498832c735)  
(KB2757638)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=7dabf372-4b31-4c9e-a660-4e0f4a65db04)  
(KB2758694)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=1511377b-0adc-455f-8caa-f3498832c735)  
(KB2757638)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5091f66f-9b89-496f-95ce-9ac556faa7b5)  
(KB2742597)  
(Importante)  
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=39406634-48ad-4ecf-a6be-f5a47885704b)  
(KB2742601)  
(Importante)  
[Microsoft .NET Framework 3.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b8cb7a04-f913-47cc-96c1-27fb7154a791)  
(KB2756919)  
(Sin clasificación de gravedad<sup>[2]</sup>)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=dafc6924-d798-46b4-9fa5-ea7c35f06fa0)  
(KB2742613)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=eff3a82e-f3db-4733-95aa-a68621e27068)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4aa3e3a7-3ebc-4b47-ab62-c22243a4edcc)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b476d44d-8a79-4857-8c3e-9d547e9b9e2d)  
(KB2736416)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=e47425e9-f53e-4e20-a7ec-b4c552bd66eb)  
(KB2799329)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=c11ec9cd-1a85-4514-a1b9-9da5cdd0926b)  
(KB2757638)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=4719776a-5ff0-491a-934e-99220d8ac3a3)  
(KB2758694)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=c11ec9cd-1a85-4514-a1b9-9da5cdd0926b)  
(KB2757638)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5091f66f-9b89-496f-95ce-9ac556faa7b5)  
(KB2742597)  
(Importante)  
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=39406634-48ad-4ecf-a6be-f5a47885704b)  
(KB2742601)  
(Importante)  
[Microsoft .NET Framework 3.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b8cb7a04-f913-47cc-96c1-27fb7154a791)  
(KB2756919)  
(Sin clasificación de gravedad<sup>[2]</sup>)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d949fde9-31e7-4553-a34c-b41625a8cdc8)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ab117984-c4cb-473b-8c20-2b0d0409d8d6)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b476d44d-8a79-4857-8c3e-9d547e9b9e2d)  
(KB2736416)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr>
<th colspan="8" style="border:1px solid black;">
Windows 7
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-008**](http://go.microsoft.com/fwlink/?linkid=275222)
</td>
<td style="border:1px solid black;">
[**MS13-001**](http://go.microsoft.com/fwlink/?linkid=273848)
</td>
<td style="border:1px solid black;">
[**MS13-002**](http://go.microsoft.com/fwlink/?linkid=264923)
</td>
<td style="border:1px solid black;">
[**MS13-004**](http://go.microsoft.com/fwlink/?linkid=268279)
</td>
<td style="border:1px solid black;">
[**MS13-005**](http://go.microsoft.com/fwlink/?linkid=273826)
</td>
<td style="border:1px solid black;">
[**MS13-006**](http://go.microsoft.com/fwlink/?linkid=273872)
</td>
<td style="border:1px solid black;">
[**MS13-007**](http://go.microsoft.com/fwlink/?linkid=268284)
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
Windows 7 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=d20f50ed-89c3-48cb-a78d-a44470fa1285)  
(KB2799329)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=abbc3f31-e940-4750-acb6-5af477bc8390)  
(KB2769369)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1e2738b9-d3c2-4dfe-8a79-335d5feee55b)  
(KB2758694)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=3a160fc4-1bf0-4db2-aa8d-6ba4f07d196b)  
(KB2757638)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=782fdaa7-7607-4617-97cc-516925e06d8a)  
(KB2742598)  
(Importante)  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=b8d0c829-ccb8-41a6-86ec-a7afde21c127)  
(KB2756920)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=057726d1-cdb4-4488-8cd8-822dabfc62a6)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=6120322b-7e04-4eeb-a9a4-11fe563a9f27)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=4c77925d-4326-483b-9d20-ad533d91c0f4)  
(KB2736418)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=d20f50ed-89c3-48cb-a78d-a44470fa1285)  
(KB2799329)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=abbc3f31-e940-4750-acb6-5af477bc8390)  
(KB2769369)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1e2738b9-d3c2-4dfe-8a79-335d5feee55b)  
(KB2758694)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=3a160fc4-1bf0-4db2-aa8d-6ba4f07d196b)  
(KB2757638)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=5b23d8db-12d3-4404-b089-0c808eec1bd0)  
(KB2742599)  
(Importante)  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=a41722e4-4b94-4539-a80e-2714269f8ae3)  
(KB2756921)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=dafc6924-d798-46b4-9fa5-ea7c35f06fa0)  
(KB2742613)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=057726d1-cdb4-4488-8cd8-822dabfc62a6)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=6120322b-7e04-4eeb-a9a4-11fe563a9f27)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=28f51d80-d87e-4a58-9ef2-d650dd84ad97)  
(KB2736422)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas x64
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=c113b67f-42ca-4fea-ba45-aba6f94de154)  
(KB2799329)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=1868c2ca-a184-494e-8eb3-82db45b08e32)  
(KB2769369)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=4b442601-2808-4192-aa7d-b6476668cd23)  
(KB2757638)  
(Crítica)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=7dabf372-4b31-4c9e-a660-4e0f4a65db04)  
(KB2758694)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=4b442601-2808-4192-aa7d-b6476668cd23)  
(KB2757638)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=782fdaa7-7607-4617-97cc-516925e06d8a)  
(KB2742598)  
(Importante)  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=b8d0c829-ccb8-41a6-86ec-a7afde21c127)  
(KB2756920)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=64249562-1fc3-436d-a9e1-4c9378b632d7)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=c9e2a55e-170f-4fe1-a306-eda676fd0fdb)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=4c77925d-4326-483b-9d20-ad533d91c0f4)  
(KB2736418)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=c113b67f-42ca-4fea-ba45-aba6f94de154)  
(KB2799329)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1868c2ca-a184-494e-8eb3-82db45b08e32)  
(KB2769369)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=4b442601-2808-4192-aa7d-b6476668cd23)  
(KB2757638)  
(Crítica)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=7dabf372-4b31-4c9e-a660-4e0f4a65db04)  
(KB2758694)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=4b442601-2808-4192-aa7d-b6476668cd23)  
(KB2757638)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=5b23d8db-12d3-4404-b089-0c808eec1bd0)  
(KB2742599)  
(Importante)  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=a41722e4-4b94-4539-a80e-2714269f8ae3)  
(KB2756921)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=dafc6924-d798-46b4-9fa5-ea7c35f06fa0)  
(KB2742613)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=64249562-1fc3-436d-a9e1-4c9378b632d7)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=c9e2a55e-170f-4fe1-a306-eda676fd0fdb)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=28f51d80-d87e-4a58-9ef2-d650dd84ad97)  
(KB2736422)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr>
<th colspan="8" style="border:1px solid black;">
Windows Server 2008 R2
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-008**](http://go.microsoft.com/fwlink/?linkid=275222)
</td>
<td style="border:1px solid black;">
[**MS13-001**](http://go.microsoft.com/fwlink/?linkid=273848)
</td>
<td style="border:1px solid black;">
[**MS13-002**](http://go.microsoft.com/fwlink/?linkid=264923)
</td>
<td style="border:1px solid black;">
[**MS13-004**](http://go.microsoft.com/fwlink/?linkid=268279)
</td>
<td style="border:1px solid black;">
[**MS13-005**](http://go.microsoft.com/fwlink/?linkid=273826)
</td>
<td style="border:1px solid black;">
[**MS13-006**](http://go.microsoft.com/fwlink/?linkid=273872)
</td>
<td style="border:1px solid black;">
[**MS13-007**](http://go.microsoft.com/fwlink/?linkid=268284)
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
Windows Server 2008 R2 para sistemas x64
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=d2fffc43-a88f-4fe5-9b24-5677258011b8)  
(KB2799329)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=8de63e96-2822-4e62-af54-bd8d4c6d5c19)  
(KB2769369)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=cd979acf-ed95-4d86-a046-ca7dc53523a3)  
(KB2757638)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=7dabf372-4b31-4c9e-a660-4e0f4a65db04)  
(KB2758694)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=cd979acf-ed95-4d86-a046-ca7dc53523a3)  
(KB2757638)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=782fdaa7-7607-4617-97cc-516925e06d8a)  
(KB2742598)  
(Importante)  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=b8d0c829-ccb8-41a6-86ec-a7afde21c127)  
(KB2756920)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=934a2e78-c88b-4d06-9b8f-1d0b612f3fd5)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=7fd8a313-9ee3-4665-b8ba-b129994aae1e)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=4c77925d-4326-483b-9d20-ad533d91c0f4)  
(KB2736418)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=d2fffc43-a88f-4fe5-9b24-5677258011b8)  
(KB2799329)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=8de63e96-2822-4e62-af54-bd8d4c6d5c19)  
(KB2769369)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=cd979acf-ed95-4d86-a046-ca7dc53523a3)  
(KB2757638)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=7dabf372-4b31-4c9e-a660-4e0f4a65db04)  
(KB2758694)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=cd979acf-ed95-4d86-a046-ca7dc53523a3)  
(KB2757638)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=5b23d8db-12d3-4404-b089-0c808eec1bd0)  
(KB2742599)  
(Importante)  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=a41722e4-4b94-4539-a80e-2714269f8ae3)  
(KB2756921)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=dafc6924-d798-46b4-9fa5-ea7c35f06fa0)  
(KB2742613)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=934a2e78-c88b-4d06-9b8f-1d0b612f3fd5)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7fd8a313-9ee3-4665-b8ba-b129994aae1e)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=28f51d80-d87e-4a58-9ef2-d650dd84ad97)  
(KB2736422)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=fbcee22b-9801-4c9e-ba0c-eb4a54526d38)  
(KB2799329)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=18070321-8635-4c2e-b9f9-0fc58c924136)  
(KB2769369)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=e4dfbf88-0e7f-43ca-affe-5d8ddea8657e)  
(KB2757638)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=4719776a-5ff0-491a-934e-99220d8ac3a3)  
(KB2758694)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=e4dfbf88-0e7f-43ca-affe-5d8ddea8657e)  
(KB2757638)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=782fdaa7-7607-4617-97cc-516925e06d8a)  
(KB2742598)  
(Importante)  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=b8d0c829-ccb8-41a6-86ec-a7afde21c127)  
(KB2756920)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=12917b84-1f91-4c19-9197-a7d1e7adcdfc)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=86e5b2fc-f530-4259-af90-259b64fcdd73)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=4c77925d-4326-483b-9d20-ad533d91c0f4)  
(KB2736418)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=fbcee22b-9801-4c9e-ba0c-eb4a54526d38)  
(KB2799329)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=18070321-8635-4c2e-b9f9-0fc58c924136)  
(KB2769369)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=e4dfbf88-0e7f-43ca-affe-5d8ddea8657e)  
(KB2757638)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=4719776a-5ff0-491a-934e-99220d8ac3a3)  
(KB2758694)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=e4dfbf88-0e7f-43ca-affe-5d8ddea8657e)  
(KB2757638)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=5b23d8db-12d3-4404-b089-0c808eec1bd0)  
(KB2742599)  
(Importante)  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=a41722e4-4b94-4539-a80e-2714269f8ae3)  
(KB2756921)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup>
(KB2742595)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=12917b84-1f91-4c19-9197-a7d1e7adcdfc)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=86e5b2fc-f530-4259-af90-259b64fcdd73)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=28f51d80-d87e-4a58-9ef2-d650dd84ad97)  
(KB2736422)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup>
(KB2736428)  
(Importante)
</td>
</tr>
<tr>
<th colspan="8" style="border:1px solid black;">
Windows 8
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-008**](http://go.microsoft.com/fwlink/?linkid=275222)
</td>
<td style="border:1px solid black;">
[**MS13-001**](http://go.microsoft.com/fwlink/?linkid=273848)
</td>
<td style="border:1px solid black;">
[**MS13-002**](http://go.microsoft.com/fwlink/?linkid=264923)
</td>
<td style="border:1px solid black;">
[**MS13-004**](http://go.microsoft.com/fwlink/?linkid=268279)
</td>
<td style="border:1px solid black;">
[**MS13-005**](http://go.microsoft.com/fwlink/?linkid=273826)
</td>
<td style="border:1px solid black;">
[**MS13-006**](http://go.microsoft.com/fwlink/?linkid=273872)
</td>
<td style="border:1px solid black;">
[**MS13-007**](http://go.microsoft.com/fwlink/?linkid=268284)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad** **acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
<td style="border:1px solid black;">
**Ninguna**
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
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1e2738b9-d3c2-4dfe-8a79-335d5feee55b)  
(KB2758694)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=e19d1373-a3f3-4f60-9142-c2484726aac8)  
(KB2757638)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=e1251343-b585-4feb-8465-7e775ae47998)  
(KB2742616)  
(Importante)  
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=43bbbc5a-e175-467a-9302-810a2a09eb7e)  
(KB2756923)  
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=f21e2bdd-b158-45d5-a6cf-a8f32f099a7a)  
(KB2742614)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=1f5441f1-a66d-42c0-bf0e-2f6867d4d43a)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=9f40864f-5347-44ef-bb08-afea45b5351b)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=b0bbe58b-cb41-4b52-9dd2-b8b4bc0076eb)  
(KB2736693)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 8 para sistemas de 64 bits
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=c669190d-964c-42d3-b09d-40a397ae3a9c)  
(KB2757638)  
(Crítica)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=7dabf372-4b31-4c9e-a660-4e0f4a65db04)  
(KB2758694)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=c669190d-964c-42d3-b09d-40a397ae3a9c)  
(KB2757638)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=e1251343-b585-4feb-8465-7e775ae47998)  
(KB2742616)  
(Importante)  
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=43bbbc5a-e175-467a-9302-810a2a09eb7e)  
(KB2756923)  
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=f21e2bdd-b158-45d5-a6cf-a8f32f099a7a)  
(KB2742614)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 64 bits](http://www.microsoft.com/downloads/details.aspx?familyid=9d71dc77-9c01-4a1f-b403-8a18ca10979d)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 64 bits](http://www.microsoft.com/downloads/details.aspx?familyid=1b40baad-784a-4eba-a4ef-703250248057)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=b0bbe58b-cb41-4b52-9dd2-b8b4bc0076eb)  
(KB2736693)  
(Importante)
</td>
</tr>
<tr>
<th colspan="8" style="border:1px solid black;">
Windows Server 2012
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-008**](http://go.microsoft.com/fwlink/?linkid=275222)
</td>
<td style="border:1px solid black;">
[**MS13-001**](http://go.microsoft.com/fwlink/?linkid=273848)
</td>
<td style="border:1px solid black;">
[**MS13-002**](http://go.microsoft.com/fwlink/?linkid=264923)
</td>
<td style="border:1px solid black;">
[**MS13-004**](http://go.microsoft.com/fwlink/?linkid=268279)
</td>
<td style="border:1px solid black;">
[**MS13-005**](http://go.microsoft.com/fwlink/?linkid=273826)
</td>
<td style="border:1px solid black;">
[**MS13-006**](http://go.microsoft.com/fwlink/?linkid=273872)
</td>
<td style="border:1px solid black;">
[**MS13-007**](http://go.microsoft.com/fwlink/?linkid=268284)
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
**Ninguna**
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
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7e434e5-1ce8-4754-b9b4-07f3d84e0528)  
(KB2757638)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=7dabf372-4b31-4c9e-a660-4e0f4a65db04)  
(KB2758694)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7e434e5-1ce8-4754-b9b4-07f3d84e0528)  
(KB2757638)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=e1251343-b585-4feb-8465-7e775ae47998)  
(KB2742616)  
(Importante)  
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=43bbbc5a-e175-467a-9302-810a2a09eb7e)  
(KB2756923)  
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=f21e2bdd-b158-45d5-a6cf-a8f32f099a7a)  
(KB2742614)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=2ad7872c-a387-41a1-8606-732a6ff0701d)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=4f0b9fb1-f1c4-4773-a956-94c8983c008a)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=b0bbe58b-cb41-4b52-9dd2-b8b4bc0076eb)  
(KB2736693)  
(Importante)  
[Extensión IIS Management OData](http://www.microsoft.com/downloads/details.aspx?familyid=77b6fb5f-10b8-4bc2-a5c3-97055c92acf1)  
(KB2753596)  
(Importante)
</td>
</tr>
<tr>
<th colspan="8" style="border:1px solid black;">
Windows RT
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-008**](http://go.microsoft.com/fwlink/?linkid=275222)
</td>
<td style="border:1px solid black;">
[**MS13-001**](http://go.microsoft.com/fwlink/?linkid=273848)
</td>
<td style="border:1px solid black;">
[**MS13-002**](http://go.microsoft.com/fwlink/?linkid=264923)
</td>
<td style="border:1px solid black;">
[**MS13-004**](http://go.microsoft.com/fwlink/?linkid=268279)
</td>
<td style="border:1px solid black;">
[**MS13-005**](http://go.microsoft.com/fwlink/?linkid=273826)
</td>
<td style="border:1px solid black;">
[**MS13-006**](http://go.microsoft.com/fwlink/?linkid=273872)
</td>
<td style="border:1px solid black;">
[**MS13-007**](http://go.microsoft.com/fwlink/?linkid=268284)
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
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows RT
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft XML Core Services 4.0<sup>[1]</sup>
(KB2758694)  
(Crítica)  
Microsoft XML Core Services 6.0<sup>[1]</sup>
(KB2757638)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 4.5<sup>[3]</sup>
(KB2742614)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT<sup>[1]</sup>
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT<sup>[1]</sup>
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="8" style="border:1px solid black;">
Opción de instalación Server Core
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador** **del** **boletín**
</td>
<td style="border:1px solid black;">
[**MS13-008**](http://go.microsoft.com/fwlink/?linkid=275222)
</td>
<td style="border:1px solid black;">
[**MS13-001**](http://go.microsoft.com/fwlink/?linkid=273848)
</td>
<td style="border:1px solid black;">
[**MS13-002**](http://go.microsoft.com/fwlink/?linkid=264923)
</td>
<td style="border:1px solid black;">
[**MS13-004**](http://go.microsoft.com/fwlink/?linkid=268279)
</td>
<td style="border:1px solid black;">
[**MS13-005**](http://go.microsoft.com/fwlink/?linkid=273826)
</td>
<td style="border:1px solid black;">
[**MS13-006**](http://go.microsoft.com/fwlink/?linkid=273872)
</td>
<td style="border:1px solid black;">
[**MS13-007**](http://go.microsoft.com/fwlink/?linkid=268284)
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
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1e2738b9-d3c2-4dfe-8a79-335d5feee55b)  
(KB2758694)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=e6439fef-e5e7-479b-8fc4-daacf3a39f3a)  
(KB2757638)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c635ad51-4e15-461c-8927-a86d79f90b45) (instalación Server Core)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b3ed781e-b740-4153-aaf3-daafdeb91004) (instalación Server Core)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=1511377b-0adc-455f-8caa-f3498832c735) (instalación Server Core)  
(KB2757638)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=7dabf372-4b31-4c9e-a660-4e0f4a65db04) (instalación Server Core)  
(KB2758694)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=1511377b-0adc-455f-8caa-f3498832c735) (instalación Server Core)  
(KB2757638)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=eff3a82e-f3db-4733-95aa-a68621e27068) (instalación Server Core)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4aa3e3a7-3ebc-4b47-ab62-c22243a4edcc) (instalación Server Core)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=8de63e96-2822-4e62-af54-bd8d4c6d5c19)(instalación Server Core)  
(KB2769369)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=cd979acf-ed95-4d86-a046-ca7dc53523a3) (instalación Server Core)  
(KB2757638)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=7dabf372-4b31-4c9e-a660-4e0f4a65db04) (instalación Server Core)  
(KB2758694)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=cd979acf-ed95-4d86-a046-ca7dc53523a3) (instalación Server Core)  
(KB2757638)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=782fdaa7-7607-4617-97cc-516925e06d8a) (instalación Server Core)  
(KB2742598)  
(Importante)  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=b8d0c829-ccb8-41a6-86ec-a7afde21c127) (instalación Server Core)  
(KB2756920)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=934a2e78-c88b-4d06-9b8f-1d0b612f3fd5)(instalación Server Core)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=7fd8a313-9ee3-4665-b8ba-b129994aae1e)(instalación Server Core)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=4c77925d-4326-483b-9d20-ad533d91c0f4) (instalación Server Core)  
(KB2736418)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=8de63e96-2822-4e62-af54-bd8d4c6d5c19) (instalación Server Core)  
(KB2769369)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=cd979acf-ed95-4d86-a046-ca7dc53523a3) (instalación Server Core)  
(KB2757638)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=7dabf372-4b31-4c9e-a660-4e0f4a65db04) (instalación Server Core)  
(KB2758694)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=cd979acf-ed95-4d86-a046-ca7dc53523a3) (instalación Server Core)  
(KB2757638)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=5b23d8db-12d3-4404-b089-0c808eec1bd0) (instalación Server Core)  
(KB2742599)  
(Importante)  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=a41722e4-4b94-4539-a80e-2714269f8ae3) (instalación Server Core)  
(KB2756921)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4991c-05f1-48c7-96ea-1389281985e5)<sup>[1]</sup> (instalación Server Core)  
(KB2742595)  
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=dafc6924-d798-46b4-9fa5-ea7c35f06fa0) (instalación Server Core)  
(KB2742613)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=934a2e78-c88b-4d06-9b8f-1d0b612f3fd5) (instalación Server Core)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7fd8a313-9ee3-4665-b8ba-b129994aae1e) (instalación Server Core)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=28f51d80-d87e-4a58-9ef2-d650dd84ad97) (instalación Server Core)  
(KB2736422)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=1d22f0d5-d87d-4e4a-bbc9-49826cec79a7)<sup>[1]</sup> (instalación Server Core)  
(KB2736428)  
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
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7e434e5-1ce8-4754-b9b4-07f3d84e0528) (instalación Server Core)  
(KB2757638)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=7dabf372-4b31-4c9e-a660-4e0f4a65db04) (instalación Server Core)  
(KB2758694)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7e434e5-1ce8-4754-b9b4-07f3d84e0528) (instalación Server Core)  
(KB2757638)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=e1251343-b585-4feb-8465-7e775ae47998) (instalación Server Core)  
(KB2742616)  
(Importante)  
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=43bbbc5a-e175-467a-9302-810a2a09eb7e) (instalación Server Core)  
(KB2756923)  
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=f21e2bdd-b158-45d5-a6cf-a8f32f099a7a) (instalación Server Core)  
(KB2742614)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=2ad7872c-a387-41a1-8606-732a6ff0701d) (instalación Server Core)  
(KB2778930)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=4f0b9fb1-f1c4-4773-a956-94c8983c008a) (instalación Server Core)  
(KB2785220)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=b0bbe58b-cb41-4b52-9dd2-b8b4bc0076eb) (instalación Server Core)  
(KB2736693)  
(Importante)  
[Extensión IIS Management OData](http://www.microsoft.com/downloads/details.aspx?familyid=77b6fb5f-10b8-4bc2-a5c3-97055c92acf1) (instalación Server Core)  
(KB2753596)  
(Importante)
</td>
</tr>
</table>
 
**Notas para MS13-002**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

<sup>[1]</sup>Las actualizaciones de seguridad de Windows RT se proporcionan a través de [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130).

**Notas para MS13-004**

<sup>[1]</sup>**.NET Framework 4 y .NET Framework 4** **ClientProfile** **están afectados.** Los paquetes redistribuibles de .NET Framework versión 4 están disponibles en dos perfiles: .NET Framework 4.0 y .NET Framework 4.0 Client Profile. .NET Framework 4.0 Client Profile es un subconjunto de .NET Framework 4.0. La vulnerabilidad corregida en esta actualización afecta a .NET Framework 4.0 y .NET Framework 4.0 Client Profile. Para obtener más información, vea el artículo de MSDN [Instalar .NET Framework](http://msdn.microsoft.com/en-us/library/5a4x27ek.aspx).

<sup>[2]</sup>Las clasificaciones de gravedad no se aplican a esta actualización para el software especificado porque las vías de ataque conocidas para la vulnerabilidad tratada en este boletín están bloqueadas en una configuración predeterminada. No obstante, como medida de defensa en profundidad, Microsoft recomienda que los clientes de este software apliquen esta actualización de seguridad.

<sup>[3]</sup>Las actualizaciones de seguridad de Windows RT se proporcionan a través de [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130).

**Nota para MS13-005**

<sup>[1]</sup>Las actualizaciones de seguridad de Windows RT se proporcionan a través de [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130).

**Nota para MS13-006**

<sup>[1]</sup>Las actualizaciones de seguridad de Windows RT se proporcionan a través de [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130).

**Nota para MS13-007**

<sup>[1]</sup>**.NET Framework 4 y .NET Framework 4** **ClientProfile** **están afectados.** Los paquetes redistribuibles de .NET Framework versión 4 están disponibles en dos perfiles: .NET Framework 4.0 y .NET Framework 4.0 Client Profile. .NET Framework 4.0 Client Profile es un subconjunto de .NET Framework 4.0. La vulnerabilidad corregida en esta actualización afecta a .NET Framework 4.0 y .NET Framework 4.0 Client Profile. Para obtener más información, vea el artículo de MSDN [Instalar .NET Framework](http://msdn.microsoft.com/en-us/library/5a4x27ek.aspx).

#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Conjuntos de programas y componentes de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador** **del** **boletín**
</td>
<td style="border:1px solid black;">
[**MS13-002**](http://go.microsoft.com/fwlink/?linkid=264923)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=d108d56c-f9fb-4823-b38e-3d2f838592de)  
(KB2760574)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=7ba27dc9-4e9c-4ab5-867e-888c01716e11)  
(KB2687499)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=7ba27dc9-4e9c-4ab5-867e-888c01716e11)  
(KB2687499)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Otro software de Microsoft Office
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-002**](http://go.microsoft.com/fwlink/?linkid=264923)
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
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Word Viewer
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=7ba27dc9-4e9c-4ab5-867e-888c01716e11)  
(KB2687499)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=7ba27dc9-4e9c-4ab5-867e-888c01716e11)  
(KB2687499)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=7ba27dc9-4e9c-4ab5-867e-888c01716e11)  
(KB2687499)  
(Crítica)
</td>
</tr>
</table>
 
**Nota para MS13-002**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Herramientas y software para desarrolladores de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Visual Studio Team Foundation Server
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-002**](http://go.microsoft.com/fwlink/?linkid=264923)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Expression Web Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=7ba27dc9-4e9c-4ab5-867e-888c01716e11)  
(KB2687499)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Expression Web 2
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=7ba27dc9-4e9c-4ab5-867e-888c01716e11)  
(KB2687499)  
(Crítica)
</td>
</tr>
</table>
 
**Nota paras MS13-002**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Software de servidor de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft SharePoint Server
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-002**](http://go.microsoft.com/fwlink/?linkid=264923)
</td>
<td style="border:1px solid black;">
[**MS13-003**](http://go.microsoft.com/fwlink/?linkid=261863)
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
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2007 Service Pack 2 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=31e1e6cc-9617-416b-8c91-5c026502d5f6)  
(KB2687497)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2007 Service Pack 2 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=fb21c3f8-b3fd-42f2-9c34-e5fbd8cad689)  
(KB2687497)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2007 Service Pack 3 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=31e1e6cc-9617-416b-8c91-5c026502d5f6)  
(KB2687497)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2007 Service Pack 3 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=fb21c3f8-b3fd-42f2-9c34-e5fbd8cad689)  
(KB2687497)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Groove Server
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-002**](http://go.microsoft.com/fwlink/?linkid=264923)
</td>
<td style="border:1px solid black;">
[**MS13-003**](http://go.microsoft.com/fwlink/?linkid=261863)
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
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Groove Server 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=fb21c3f8-b3fd-42f2-9c34-e5fbd8cad689)  
(KB2687497)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Groove Server 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=fb21c3f8-b3fd-42f2-9c34-e5fbd8cad689)  
(KB2687497)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft System Center Operations Manager
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS13-002**](http://go.microsoft.com/fwlink/?linkid=264923)
</td>
<td style="border:1px solid black;">
[**MS13-003**](http://go.microsoft.com/fwlink/?linkid=261863)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad** **acumulada**
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
Microsoft System Center Operations Manager 2007 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft System Center Operations Manager 2007 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=f848d74d-fdae-4a19-a0f5-12d2d4389db9)<sup>[1]</sup>
(KB2809182)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft System Center Operations Manager 2007 R2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft System Center Operations Manager 2007 R2](http://www.microsoft.com/downloads/details.aspx?familyid=4e1ab3bd-af0c-41f8-8ebc-1cdc68a3ee37)<sup>[1]</sup><sup>[2]</sup>
(KB2783850)  
(Importante)
</td>
</tr>
</table>
 
**Nota paras MS13-002**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

**Notas para MS13-003**

<sup>[1]</sup>Esta actualización solo está disponible en el Centro de descarga de Microsoft.

<sup>[2]</sup>Esta actualización es acumulativa y reemplaza las actualizaciones acumulativas anteriores del software especificado.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/bb245732). [TechNet Security TechCenter](http://technet.microsoft.com/es-es/security/) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar el [Centro de seguridad y protección de Microsoft](http://www.microsoft.com/es-es/security/default.aspx), donde esta información también está disponible haciendo clic en "Actualizaciones de seguridad".

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Para clientes de Microsoft Office para Mac, Microsoft AutoUpdate para Mac puede servir de ayuda para mantener actualizado el software de Microsoft. Para obtener más información acerca del uso de Microsoft AutoUpdate para Mac, vea [Buscar actualizaciones de software automáticamente](http://mac2.microsoft.com/help/office/14/en-us/word/item/ffe35357-8f25-4df8-a0a3-c258526c64ea).

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS13-001"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Consejos para la detección y la implementación**

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747).

**Microsoft** **Baseline** **Security** **Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, vea [Microsoft Baseline Security Analyzer](http://technet.microsoft.com/es-es/security/cc184924.aspx).

**Windows Server** **UpdateServices**

Windows Server Update Services (WSUS) permite a los administradores implementar de un modo rápido y confiable las actualizaciones críticas y de seguridad más recientes en sistemas operativos Microsoft Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://technet.microsoft.com/wsus/default).

**System** **Center** **Configuration** **Manager**

La administración de actualizaciones de software de System Center Configuration Manager simplifica la tarea compleja de entregar y administrar actualizaciones para los sistemas de TI en toda la empresa. Con System Center Configuration Manager, los administradores de TI pueden ofrecer actualizaciones de los productos de Microsoft a una serie de dispositivos, incluidos equipos de escritorio, portátiles, servidores y dispositivos móviles.

La evaluación automática de vulnerabilidades en System Center Configuration Manager detecta las necesidades de actualizaciones e informa de las acciones recomendadas. La administración de actualizaciones de software en System Center Configuration Manager se basa en Microsoft Windows Software Update Services (WSUS), una infraestructura de actualizaciones probada con la que están familiarizados los administradores de TI de todo el mundo. Para obtener más información acerca de System Center Configuration Manager, vea [Recursos técnicos de System Center](http://technet.microsoft.com/systemcenter/bb980621).

**Systems** **Management Server 2003**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales.

**Nota** System Management Server 2003 está fuera del soporte técnico general desde el 12 de enero de 2010. Para obtener más información acerca de los ciclos de vida de los productos, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742). Ya está disponible la siguiente versión de SMS, System Center Configuration Manager; vea la sección anterior, **System** **Center** **Configuration** **Manager**.

Para obtener más información acerca de cómo los administradores pueden usar SMS 2003 para implementar actualizaciones de seguridad, vea [Escenarios y procedimientos para Microsoft Systems Management Server 2003: Administración de distribución de software y revisiones](http://www.microsoft.com/downloads/details.aspx?familyid=32f2bb4c-42f8-4b8d-844f-2553fd78049f). Para obtener información acerca de SMS, visite [Microsoft Systems Management Server TechCenter](http://technet.microsoft.com/es-es/systemcenter/bb545936).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://www.microsoft.com/downloads/en/details.aspx?familyid=7bd3a16e-1899-4e0b-bb99-1320e816167d)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet.microsoft.com/library/cc749197) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

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

-   Nicolas Gregoire, de [Agarri](http://www.agarri.fr/), por informar de un problema descrito en MS13-002
-   Andy Yang, de BAE Systems Detica, por informar de un problema descrito en MS13-003
-   Jon Erickson, de [iSIGHT Partners Labs](http://www.isightpartners.com/), por informar de un problema descrito en MS13-004
-   Vitaliy Toropov, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de dos problemas descritos en MS13-004
-   James Forshaw, de Context Information Security, por informar de un problema descrito en MS13-004
-   [Kenichiro Katayama](https://twitter.com/pin_ptr)
-   por informar de un problema descrito en MS13-006
-   [Exodus Intelligence](https://www.exodusintel.com)
-   , por colaborar con nosotros en un problema de descrito en MS13-008

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Soluciones de seguridad para profesionales de TI: Soporte técnico y solución de problemas de seguridad de TechNet
-   Ayuda para proteger su equipo con Windows de virus y malware: [Solución antivirus y centro de seguridad](http://support.microsoft.com/contactus/cu_sc_virsec_master)
-   Soporte local según su país: [Soporte internacional](http://support.microsoft.com/common/international.aspx)

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (8 de enero de 2013): Publicación del resumen del boletín.
-   V1.1 (8 de enero de 2013): para MS13-002, se agregaron entradas de instalación Server Core en Software afectado para Microsoft XML Core Services 4.0 cuando está instalado en Windows Server 2008 para sistemas de 32 bits Service Pack 2 y Microsoft XML Core Services 6.0 en Windows Server 2008 para sistemas de 32 bits Service Pack 2. Se trata únicamente de un cambio informativo. Los clientes que ya han actualizado correctamente sus sistemas no necesitan realizar ninguna acción.
-   V2.0 (14 de enero de 2013): se ha agregado el boletín de seguridad de Microsoft MS13-008, Actualización de seguridad para Internet Explorer (2799329), y se ha agregado el vínculo de webcast de boletín para este boletín de seguridad fuera de ciclo.
-   V3.0 (22 de enero de 2013): para MS13-004, se ha vuelto a publicar el boletín para ofrecer de nuevo la actualización KB2756920 para sistemas Windows 7 y Windows Server 2008 R2 que se ejecutan en configuraciones específicas que se sabe que tienen problemas de compatibilidad potenciales. Vea el boletín para obtener más información.
-   V4.0 (12 de marzo de 2013): para MS13-003, se volvió a publicar el boletín para anunciar la disponibilidad de una actualización para Microsoft System Center Operations Manager 2007 Service Pack 1. Ningún otro paquete de actualización está afectado por esta nueva publicación. Vea el boletín para obtener más información.

*Built at 2014-04-18T01:50:00Z-07:00*
