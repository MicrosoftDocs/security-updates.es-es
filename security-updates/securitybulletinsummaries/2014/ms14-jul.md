---
TOCTitle: 'MS14-JUL'
Title: Resumen del boletín de seguridad de Microsoft de julio de 2014
ms:assetid: 'ms14-jul'
ms:contentKeyID: 62554620
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms14-jul(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de julio de 2014
==============================================================

Publicado: 8 de julio de 2014 | Actualizado: 29 de julio de 2014

**Versión:** 1.1

Este resumen del boletín enumera los boletines de seguridad publicados para julio de 2014.

Con la publicación de los boletines de seguridad de julio de 2014, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 3 de julio de 2014. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar una difusión por web para atender las consultas de los clientes sobre estos boletines el 9 de julio de 2014, a las 11:00 a. m., hora del Pacífico (EE. UU. y Canadá). Para ver la difusión por web mensual y los vínculos a difusiones de los boletines de seguridad adicionales, vea [Difusión web del boletín de seguridad de Microsoft](http://technet.microsoft.com/security/dn756352).

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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (2975687)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y veinticuatro vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un intruso que aprovechara estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los clientes cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402326">MS14-038</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Windows Journal podría permitir la ejecución remota de código (2975689)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo de Journal especialmente diseñado. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402327">MS14-039</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el teclado en pantalla podría permitir la elevación de privilegios (2975685)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si un atacante usa una vulnerabilidad en un proceso de integridad baja para ejecutar el texto en pantalla y carga un programa especialmente diseñado en el sistema de destino.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402328">MS14-040</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el controlador de función auxiliar (AFD) podría permitir la elevación de privilegios (2975684)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si un atacante inicia sesión en un sistema y ejecuta una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402330">MS14-041</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en DirectShow podría permitir la elevación de privilegios (2975681)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si un atacante primero aprovecha otra vulnerabilidad en un proceso de integridad baja y, a continuación, usa esta vulnerabilidad para ejecutar código especialmente diseñado en el contexto del usuario que ha iniciado sesión. De forma predeterminada, la experiencia de exploración moderna y envolvente en Windows 8 y Windows 8.1 se ejecuta con el modo de protección mejorado (EPM). Por ejemplo, los clientes que usan el explorador Internet Explorer 11 adaptado para dispositivos táctiles en tabletas Windows modernas usan el modo de protección mejorado de forma predeterminada. El modo de protección mejorado usa protecciones de seguridad avanzadas que pueden contribuir a atenuar el aprovechamiento de esta vulnerabilidad en sistemas de 64 bits.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402462">MS14-042</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Service Bus podría permitir la denegación de servicio (2972621)<br />
</strong><br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública en Microsoft Service Bus para Windows Server. La vulnerabilidad podría permitir la denegación de servicio si un atacante remoto autenticado crea y ejecuta un programa que envía una secuencia de mensajes AMQP (protocolo avanzado de Message Queue Server) especialmente diseñados al sistema de destino. Microsoft Service Bus para Windows Server no se incluye en ningún sistema operativo de Microsoft. Para que un sistema afectado sea vulnerable, primero se debe descargar, instalar y configurar Microsoft Service Bus, y sus detalles de configuración (certificado de granja de servidores) se deben compartir con otros usuarios.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Moderada</a> <br />
Denegación de servicio</td>
<td style="border:1px solid black;">No requiere reinicio</td>
<td style="border:1px solid black;">Software de servidor de Microsoft</td>
</tr>
</tbody>
</table>
  
 
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y, a continuación, por identificador de CVE. Sólo se incluyen las vulnerabilidades que tiene una clasificación de gravedad de crítica o importante en los boletines.
  
**¿Cómo se usa esta tabla?**  
  
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1763">CVE-2014-1763</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1765">CVE-2014-1765</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2785">CVE-2014-2785</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2786">CVE-2014-2786</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2787">CVE-2014-2787</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2788">CVE-2014-2788</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2789">CVE-2014-2789</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2790">CVE-2014-2790</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2791">CVE-2014-2791</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2792">CVE-2014-2792</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2794">CVE-2014-2794</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2795">CVE-2014-2795</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2797">CVE-2014-2797</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2798">CVE-2014-2798</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2800">CVE-2014-2800</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2801">CVE-2014-2801</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2802">CVE-2014-2802</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2803">CVE-2014-2803</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2804">CVE-2014-2804</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2806">CVE-2014-2806</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2807">CVE-2014-2807</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2809">CVE-2014-2809</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2813">CVE-2014-2813</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402324">MS14-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4066">CVE-2014-4066</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402326">MS14-038</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código en Windows Journal</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1824">CVE-2014-1824</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402327">MS14-039</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en el teclado en pantalla</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2781">CVE-2014-2781</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402328">MS14-040</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en el controlador de función auxiliar</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-1767">CVE-2014-1767</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=402330">MS14-041</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en DirectShow</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-2780">CVE-2014-2780</a></td>
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
  
**¿Cómo se usan estas tablas?**  
  
Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, también se muestra la clasificación de gravedad de dicha actualización de software.
  
**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.
  
### Componentes y sistema operativo Windows

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="6">
**Windows Server 2003**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-037**](http://go.microsoft.com/fwlink/?linkid=402324)
</td>
<td style="border:1px solid black;">
[**MS14-038**](http://go.microsoft.com/fwlink/?linkid=402326)
</td>
<td style="border:1px solid black;">
[**MS14-039**](http://go.microsoft.com/fwlink/?linkid=402327)
</td>
<td style="border:1px solid black;">
[**MS14-040**](http://go.microsoft.com/fwlink/?linkid=402328)
</td>
<td style="border:1px solid black;">
[**MS14-041**](http://go.microsoft.com/fwlink/?linkid=402330)
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
**Ninguna**
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
(2962872)  
(Moderada)  
Internet Explorer 7  
(2962872)  
(Moderada)  
Internet Explorer 8  
(2962872)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(2961072)  
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
(2962872)  
(Moderada)  
Internet Explorer 7  
(2962872)  
(Moderada)  
Internet Explorer 8  
(2962872)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2961072)  
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
(2962872)  
(Moderada)  
Internet Explorer 7  
(2962872)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2961072)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="6">
**Windows Vista**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-037**](http://go.microsoft.com/fwlink/?linkid=402324)
</td>
<td style="border:1px solid black;">
[**MS14-038**](http://go.microsoft.com/fwlink/?linkid=402326)
</td>
<td style="border:1px solid black;">
[**MS14-039**](http://go.microsoft.com/fwlink/?linkid=402327)
</td>
<td style="border:1px solid black;">
[**MS14-040**](http://go.microsoft.com/fwlink/?linkid=402328)
</td>
<td style="border:1px solid black;">
[**MS14-041**](http://go.microsoft.com/fwlink/?linkid=402330)
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2962872)  
(Crítica)  
Internet Explorer 8  
(2962872)  
(Crítica)  
Internet Explorer 9  
(2962872)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2971850)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2961072)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2972280)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2962872)  
(Crítica)  
Internet Explorer 8  
(2962872)  
(Crítica)  
Internet Explorer 9  
(2962872)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2971850)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2961072)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2972280)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="6">
**Windows Server 2008**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-037**](http://go.microsoft.com/fwlink/?linkid=402324)
</td>
<td style="border:1px solid black;">
[**MS14-038**](http://go.microsoft.com/fwlink/?linkid=402326)
</td>
<td style="border:1px solid black;">
[**MS14-039**](http://go.microsoft.com/fwlink/?linkid=402327)
</td>
<td style="border:1px solid black;">
[**MS14-040**](http://go.microsoft.com/fwlink/?linkid=402328)
</td>
<td style="border:1px solid black;">
[**MS14-041**](http://go.microsoft.com/fwlink/?linkid=402330)
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
(2962872)  
(Moderada)  
Internet Explorer 8  
(2962872)  
(Moderada)  
Internet Explorer 9  
(2962872)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2971850)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2961072)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2972280)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2962872)  
(Moderada)  
Internet Explorer 8  
(2962872)  
(Moderada)  
Internet Explorer 9  
(2962872)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2971850)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2961072)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2972280)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2962872)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2961072)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="6">
**Windows 7**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-037**](http://go.microsoft.com/fwlink/?linkid=402324)
</td>
<td style="border:1px solid black;">
[**MS14-038**](http://go.microsoft.com/fwlink/?linkid=402326)
</td>
<td style="border:1px solid black;">
[**MS14-039**](http://go.microsoft.com/fwlink/?linkid=402327)
</td>
<td style="border:1px solid black;">
[**MS14-040**](http://go.microsoft.com/fwlink/?linkid=402328)
</td>
<td style="border:1px solid black;">
[**MS14-041**](http://go.microsoft.com/fwlink/?linkid=402330)
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2962872)  
(Crítica)  
Internet Explorer 9  
(2962872)  
(Crítica)  
Internet Explorer 10  
(2962872)  
(Crítica)  
Internet Explorer 11  
(2962872)  
(Crítica)  
Internet Explorer 11  
(2963952)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2971850)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2961072)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2972280)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2962872)  
(Crítica)  
Internet Explorer 9  
(2962872)  
(Crítica)  
Internet Explorer 10  
(2962872)  
(Crítica)  
Internet Explorer 11  
(2962872)  
(Crítica)  
Internet Explorer 11  
(2963952)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2971850)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2961072)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2972280)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="6">
**Windows Server 2008 R2**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-037**](http://go.microsoft.com/fwlink/?linkid=402324)
</td>
<td style="border:1px solid black;">
[**MS14-038**](http://go.microsoft.com/fwlink/?linkid=402326)
</td>
<td style="border:1px solid black;">
[**MS14-039**](http://go.microsoft.com/fwlink/?linkid=402327)
</td>
<td style="border:1px solid black;">
[**MS14-040**](http://go.microsoft.com/fwlink/?linkid=402328)
</td>
<td style="border:1px solid black;">
[**MS14-041**](http://go.microsoft.com/fwlink/?linkid=402330)
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
(2962872)  
(Moderada)  
Internet Explorer 9  
(2962872)  
(Moderada)  
Internet Explorer 10  
(2962872)  
(Moderada)  
Internet Explorer 11  
(2962872)  
(Moderada)  
Internet Explorer 11  
(2963952)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2971850)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2961072)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2972280)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2962872)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2961072)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="6">
**Windows 8 y Windows 8.1**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-037**](http://go.microsoft.com/fwlink/?linkid=402324)
</td>
<td style="border:1px solid black;">
[**MS14-038**](http://go.microsoft.com/fwlink/?linkid=402326)
</td>
<td style="border:1px solid black;">
[**MS14-039**](http://go.microsoft.com/fwlink/?linkid=402327)
</td>
<td style="border:1px solid black;">
[**MS14-040**](http://go.microsoft.com/fwlink/?linkid=402328)
</td>
<td style="border:1px solid black;">
[**MS14-041**](http://go.microsoft.com/fwlink/?linkid=402330)
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2962872)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2971850)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2961072)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2972280)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas x64
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2962872)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(2971850)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(2961072)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(2972280)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2962872)  
(Crítica)  
Internet Explorer 11  
(2963952)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(2971850)  
(Crítica)  
Windows 8.1 para sistemas de 32 bits  
(2974286)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(2973201)  
(Importante)  
Windows 8.1 para sistemas de 32 bits  
(2973906)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(2961072)  
(Importante)  
Windows 8.1 para sistemas de 32 bits  
(2973408)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(2972280)  
(Importante)  
Windows 8.1 para sistemas de 32 bits  
(2973932)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2962872)  
(Crítica)  
Internet Explorer 11  
(2963952)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(2971850)  
(Crítica)  
Windows 8.1 para sistemas x64  
(2974286)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(2973201)  
(Importante)  
Windows 8.1 para sistemas x64  
(2973906)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(2961072)  
(Importante)  
Windows 8.1 para sistemas x64  
(2973408)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(2972280)  
(Importante)  
Windows 8.1 para sistemas x64  
(2973932)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="6">
**Windows Server 2012 y Windows Server 2012 R2**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-037**](http://go.microsoft.com/fwlink/?linkid=402324)
</td>
<td style="border:1px solid black;">
[**MS14-038**](http://go.microsoft.com/fwlink/?linkid=402326)
</td>
<td style="border:1px solid black;">
[**MS14-039**](http://go.microsoft.com/fwlink/?linkid=402327)
</td>
<td style="border:1px solid black;">
[**MS14-040**](http://go.microsoft.com/fwlink/?linkid=402328)
</td>
<td style="border:1px solid black;">
[**MS14-041**](http://go.microsoft.com/fwlink/?linkid=402330)
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
(2962872)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2971850)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2961072)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2972280)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012 R2
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2962872)  
(Moderada)  
Internet Explorer 11  
(2963952)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(2971850)  
(Crítica)  
Windows Server 2012 R2  
(2974286)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(2973201)  
(Importante)  
Windows Server 2012 R2  
(2973906)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(2961072)  
(Importante)  
Windows Server 2012 R2  
(2973408)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(2972280)  
(Importante)  
Windows Server 2012 R2  
(2973932)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="6">
**Windows RT y Windows RT 8.1**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-037**](http://go.microsoft.com/fwlink/?linkid=402324)
</td>
<td style="border:1px solid black;">
[**MS14-038**](http://go.microsoft.com/fwlink/?linkid=402326)
</td>
<td style="border:1px solid black;">
[**MS14-039**](http://go.microsoft.com/fwlink/?linkid=402327)
</td>
<td style="border:1px solid black;">
[**MS14-040**](http://go.microsoft.com/fwlink/?linkid=402328)
</td>
<td style="border:1px solid black;">
[**MS14-041**](http://go.microsoft.com/fwlink/?linkid=402330)
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
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows RT
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2962872)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows RT  
(2971850)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows RT  
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT  
(2961072)  
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
(2962872)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(2971850)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(2961072)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="6">
**Opción de instalación Server Core**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-037**](http://go.microsoft.com/fwlink/?linkid=402324)
</td>
<td style="border:1px solid black;">
[**MS14-038**](http://go.microsoft.com/fwlink/?linkid=402326)
</td>
<td style="border:1px solid black;">
[**MS14-039**](http://go.microsoft.com/fwlink/?linkid=402327)
</td>
<td style="border:1px solid black;">
[**MS14-040**](http://go.microsoft.com/fwlink/?linkid=402328)
</td>
<td style="border:1px solid black;">
[**MS14-041**](http://go.microsoft.com/fwlink/?linkid=402330)
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
**Ninguna**
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
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2961072)  
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
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2961072)  
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
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2961072)  
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
Windows Server 2012 (instalación Server Core)  
(2973201)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(2961072)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
(2973201)  
(Importante)  
Windows Server 2012 R2 (instalación Server Core)  
(2973906)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(2961072)  
(Importante)  
Windows Server 2012 R2 (instalación Server Core)  
(2973408)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
 

### Software de Windows Server

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="3">
**Microsoft Server Bus para Windows Server**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-042**](http://go.microsoft.com/fwlink/?linkid=402462)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;" colspan="2">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Service Bus para Windows Server
</td>
<td style="border:1px solid black;" colspan="2">
Microsoft Service Bus 1.1 cuando está instalado en Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2972621)  
(Moderada)  
Microsoft Service Bus 1.1 cuando está instalado en Windows Server 2012  
(2972621)  
(Moderada)  
Microsoft Service Bus 1.1 cuando está instalado en Windows Server 2012 R2  
(2972621)  
(Moderada)
</td>
</tr>
</table>
 

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

**MS14-037**

-   [VUPEN](http://www.vupen.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1763)
-   [Andreas Schmidt](https://technet.microsoft.com/es-ES/mailto:andreas.schmidt@siberas.de), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1765)
-   0016EECD9D7159A949DAD3BC17E0A939, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1765)
-   91fba4fa08fe776e7369ab4d96db6578, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-1765)
-   [Eric Lawrence](https://twitter.com/ericlaw), por informar de la vulnerabilidad de omisión de característica de seguridad en el certificado de validación extendida (CVE-2014-2783)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2785)
-   Liu Long, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2785)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2786)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2787)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2788)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2789)
-   Yujie Wen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2790)
-   Liu Long, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2790)
-   Arthur Gerkis, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2791)
-   Abdul Aziz Hariri, Matt Molinyawe y Jasiel Spelman, de [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2792)
-   ZhaoWei de [KnownSec](http://www.knownsec.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2794)
-   Hui Gao, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2795)
-   Royce Lu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2797)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2798)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2800)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2801)
-   Yuki Chen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2802)
-   Sky, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2802)
-   [Chen Zhang (demi6od)](https://github.com/demi6od), de [NSFOCUS Security Team](http://www.nsfocus.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2802)
-   AMol NAik, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2803)
-   Garage4Hackers, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2803)
-   Yuki Chen, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2803)
-   exp-sky, de [NSFOCUS Security Team](http://www.nsfocus.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2804)
-   [Chen Zhang (demi6od)](https://github.com/demi6od), de [NSFOCUS Security Team](http://www.nsfocus.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2806)
-   José A. Vázquez, de Yenteasy - Security Research en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2807)
-   [Aniway.Anyway@gmail.com](mailto:aniway.anyway@gmail.com), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2809)
-   Abdul Aziz Hariri, de [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-2813)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4066)

     

**MS14-038**

-   [Hamburgers.maccoy@gmail.com](mailto:hamburgers.maccoy@gmail.com), por informar de la vulnerabilidad de ejecución remota de código en Windows Journal (CVE-2014-1824)

     

**MS14-039**

-   [lokihardt@asrt](https://technet.microsoft.com/es-ES/mailto:lokihardt@asrt), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de elevación de privilegios en el teclado en pantalla (CVE-2014-2781)

     

**MS14-040**

-   [Sebastian Apelt](https://technet.microsoft.com/es-ES/mailto:sebastian.apelt@siberas.de), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de elevación de privilegios en el controlador de función auxiliar (CVE-2014-1767)

     

**MS14-041**

-   [VUPEN](http://www.vupen.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de elevación de privilegios en DirectShow (CVE-2014-2780)

     

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

-   V1.0 (8 de julio de 2014): Publicación del resumen del boletín.
-   V1.1 (29 de julio de 2014): para MS14-037, se ha corregido la evaluación de explotabilidad en Índice de explotabilidad para CVE-2014-4066. Se trata únicamente de un cambio informativo.

*Página generada el 2014-08-06 16:51Z-07:00.*
