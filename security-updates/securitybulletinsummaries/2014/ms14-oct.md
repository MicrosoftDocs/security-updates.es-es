---
TOCTitle: 'MS14-OCT'
Title: Resumen del boletín de seguridad de Microsoft de octubre de 2014
ms:assetid: 'ms14-oct'
ms:contentKeyID: 63171985
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms14-oct(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de octubre de 2014
================================================================

Publicado: 14 de octubre de 2014

**Versión:** 1.0

Este resumen del boletín enumera los boletines de seguridad publicados para octubre de 2014.

Con la publicación de los boletines de seguridad de octubre de 2014, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 9 de octubre de 2014. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar una difusión por web para atender las consultas de los clientes sobre estos boletines el 15 de octubre de 2014, a las 11:00 a. m., hora del Pacífico (EE. UU. y Canadá). Para ver la difusión por web mensual y los vínculos a difusiones de los boletines de seguridad adicionales, vea [Difusión web del boletín de seguridad de Microsoft](http://technet.microsoft.com/security/dn756352).

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
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><strong>Título de boletín y resumen ejecutivo</strong></td>
<td style="border:1px solid black;"><strong>Clasificación máxima de gravedad y consecuencias de la vulnerabilidad</strong></td>
<td style="border:1px solid black;"><strong>Requisito de reinicio</strong></td>
<td style="border:1px solid black;"><strong>Software afectado</strong></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513092">MS14-056</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (2987107)</strong><br />
<br />
Esta actualización de seguridad resuelve catorce vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un intruso que aprovechara estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los clientes cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513095">MS14-057</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en .NET Framework podrían permitir la ejecución remota de código (3000414)<br />
<br />
</strong>Esta actualización de seguridad resuelve tres vulnerabilidades de las que se ha informado de forma privada en Microsoft .NET Framework. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un atacante envía un URI especialmente diseñado que contenga caracteres internacionales a una aplicación web .NET. En aplicaciones .NET 4.0, la funcionalidad vulnerable (iriParsing) está deshabilitada de forma predeterminada; para que la vulnerabilidad se pueda aprovechar, una aplicación debe habilitar esta funcionalidad explícitamente. En aplicaciones .NET 4.5, iriParsing está habilitado de forma predeterminada y no se puede deshabilitar.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Microsoft .NET Framework</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513104">MS14-058</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el controlador en modo kernel podría permitir la ejecución remota de código (3000061)<br />
<br />
</strong>Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un atacante convence a un usuario para que abra un documento especialmente diseñado o para que visite un sitio web que no es de confianza y que contenga fuentes TrueType insertadas. Sin embargo, el atacante no podría en ningún caso obligar a los usuarios a realizar estas acciones. En su lugar, el atacante tendría que convencer a los usuarios de que lo hagan, normalmente haciendo que hagan clic en un vínculo en un mensaje de correo electrónico o de Instant Messenger.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507673">MS14-059</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en ASP.NET MVC podría permitir la omisión de característica de seguridad (2990942)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública en ASP.NET MVC. La vulnerabilidad podría permitir la omisión de la característica de seguridad si un atacante convence a un usuario para que haga clic en un vínculo especialmente diseñado o visite una página web que incluye contenido especialmente diseñado para aprovechar la vulnerabilidad. En un escenario de ataque web, el atacante podría hospedar un sitio web especialmente diseñado para aprovechar la vulnerabilidad mediante un explorador web y convencer a un usuario para que visite el sitio web. El atacante también podría aprovechar sitios web vulnerables y sitios web que aceptan o reciben contenido o anuncios proporcionados por el usuario. Estos sitios web podrían incluir contenido malintencionado a través del cual se podría aprovechar la vulnerabilidad. No obstante, el atacante no podría en ningún caso obligar a los usuarios a ver el contenido controlado por el atacante. En su lugar, tendría que convencerlos para que realizaran alguna acción, normalmente incitándoles a que hagan clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger que los lleve al sitio web del atacante o a que abran datos adjuntos enviados por correo electrónico.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Omisión de característica de seguridad</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Herramientas de desarrollo de Microsoft</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513097">MS14-060</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Windows OLE podría permitir la ejecución remota de código (3000869)<br />
<br />
</strong>Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo de Microsoft Office que contiene un objeto OLE especialmente diseñado. Un atacante que consiguiera aprovechar esta vulnerabilidad podría ejecutar código arbitrario en el contexto del usuario actual. Si el usuario actual inicia sesión con derechos de administrador, el atacante podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Los clientes cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513106">MS14-061</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Word y Office Web Apps podría permitir la ejecución remota de código (3000434)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Office. La vulnerabilidad podría permitir la ejecución remota de código si un atacante convence a un usuario para que abra un archivo de Microsoft Word especialmente diseñado. Un atacante que aprovechara la vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Si el usuario actual inicia sesión con derechos de administrador, el atacante podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Los clientes cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office,<br />
Microsoft Office Services,<br />
Microsoft Office Web Apps</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513107">MS14-062</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el servicio de Message Queue Server podría permitir la elevación de privilegios (2993254)<br />
<br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad que se ha divulgado públicamente en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si un atacante envía una solicitud de control entrada/salida (IOCTL) especialmente diseñada al servicio de Message Queue Server. Si se aprovecha esta vulnerabilidad, se podría obtener acceso completo al sistema afectado. De forma predeterminada, el componente Message Queue Server no se instala en ninguna edición de sistema operativo afectada y sólo lo puede habilitar un usuario con privilegios administrativos. Sólo los clientes que habiliten manualmente el componente Message Queue Server pueden ser vulnerables a este problema.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513102">MS14-063</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el controlador de particiones de disco FAT32 que podría permitir la elevación de privilegios (2998579)<br />
<br />
</strong>Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. Existe una vulnerabilidad de elevación de privilegios en la forma en que el controlador del sistema FASTFAT de Windows interactúa con las particiones de disco FAT32. Un atacante que consiguiera aprovechar esta vulnerabilidad podría ejecutar código arbitrario con privilegios elevados.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513092">MS14-056</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4123">CVE-2014-4123</a></td>
<td style="border:1px solid black;">0: Vulnerabilidad detectada</td>
<td style="border:1px solid black;">0: Vulnerabilidad detectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de elevación de privilegios mediante la omisión del espacio aislado de Internet Explorer.<br />
<br />
Microsoft tiene constancia de ataques limitados que intentan aprovechar esta vulnerabilidad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513092">MS14-056</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4124">CVE-2014-4124</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de elevación de privilegios.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513092">MS14-056</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4126">CVE-2014-4126</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513092">MS14-056</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4127">CVE-2014-4127</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513092">MS14-056</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4128">CVE-2014-4128</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513092">MS14-056</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4129">CVE-2014-4129</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513092">MS14-056</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4130">CVE-2014-4130</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513092">MS14-056</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4132">CVE-2014-4132</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513092">MS14-056</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4133">CVE-2014-4133</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513092">MS14-056</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4134">CVE-2014-4134</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513092">MS14-056</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4137">CVE-2014-4137</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513092">MS14-056</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4138">CVE-2014-4138</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513092">MS14-056</a></td>
<td style="border:1px solid black;">Vulnerabilidad de omisión de ASLR en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4140">CVE-2014-4140</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Es una vulnerabilidad de omisión de característica de seguridad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513092">MS14-056</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4141">CVE-2014-4141</a></td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513095">MS14-057</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en .NET ClickOnce</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4073">CVE-2014-4073</a></td>
<td style="border:1px solid black;">2 - Poca probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">2 - Poca probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de elevación de privilegios.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513095">MS14-057</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código en .NET Framework</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4121">CVE-2014-4121</a></td>
<td style="border:1px solid black;">2 - Poca probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">2 - Poca probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513095">MS14-057</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ASLR en .NET</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4122">CVE-2014-4122</a></td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Es una vulnerabilidad de omisión de característica de seguridad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513104">MS14-058</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en Win32k.sys</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4113">CVE-2014-4113</a></td>
<td style="border:1px solid black;">0: Vulnerabilidad detectada</td>
<td style="border:1px solid black;">0: Vulnerabilidad detectada</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de elevación de privilegios.<br />
<br />
Microsoft tiene constancia de ataques limitados que intentan aprovechar esta vulnerabilidad.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513104">MS14-058</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código en el análisis de fuentes TrueType</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4148">CVE-2014 -4148</a></td>
<td style="border:1px solid black;">0: Vulnerabilidad detectada</td>
<td style="border:1px solid black;">0: Vulnerabilidad detectada</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Microsoft tiene constancia de ataques limitados que intentan aprovechar esta vulnerabilidad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=507673">MS14-059</a></td>
<td style="border:1px solid black;">Vulnerabilidad de XSS en MVC</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4075">CVE-2014-4075</a></td>
<td style="border:1px solid black;">3: improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">3: improbabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Es una vulnerabilidad de omisión de característica de seguridad.<br />
<br />
Esta vulnerabilidad ya se ha divulgado públicamente.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513097">MS14-060</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código en Windows OLE</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4114">CVE-2014-4114</a></td>
<td style="border:1px solid black;">0: Vulnerabilidad detectada</td>
<td style="border:1px solid black;">0: Vulnerabilidad detectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Microsoft tiene constancia de ataques limitados que intentan aprovechar esta vulnerabilidad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513106">MS14-061</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el formato de archivo de Microsoft Word </td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4117">CVE-2014-4117</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513107">MS14-062</a></td>
<td style="border:1px solid black;">Vulnerabilidad de escalación de privilegios de escritura arbitrarios en MQAC</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4971">CVE-2014-4971</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">1: mucha probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de elevación de privilegios.<br />
<br />
Esta vulnerabilidad ya se ha divulgado públicamente.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=513102">MS14-063</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en el controlador de particiones de disco de Microsoft Windows</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2014-4115">CVE-2014-4115</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">2 - Poca probabilidad de que se aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de elevación de privilegios.</td>
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
**Windows Server 2003**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-056**](http://go.microsoft.com/fwlink/?linkid=513092)
</td>
<td style="border:1px solid black;">
[**MS14-057**](http://go.microsoft.com/fwlink/?linkid=513095)
</td>
<td style="border:1px solid black;">
[**MS14-058**](http://go.microsoft.com/fwlink/?linkid=513104)
</td>
<td style="border:1px solid black;">
[**MS14-060**](http://go.microsoft.com/fwlink/?linkid=513097)
</td>
<td style="border:1px solid black;">
[**MS14-062**](http://go.microsoft.com/fwlink/?linkid=513107)
</td>
<td style="border:1px solid black;">
[**MS14-063**](http://go.microsoft.com/fwlink/?linkid=513102)
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
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 6  
(2987107)  
(Moderada)  
Internet Explorer 7  
(2987107)  
(Moderada)  
Internet Explorer 8  
(2987107)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2972105)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2979574)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972106)  
(Crítica)  
Microsoft .NET Framework 4.0  
(2979575)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(2993254)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(2998579)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 6  
(2987107)  
(Moderada)  
Internet Explorer 7  
(2987107)  
(Moderada)  
Internet Explorer 8  
(2987107)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2972105)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2979574)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972106)  
(Crítica)  
Microsoft .NET Framework 4.0  
(2979575)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2993254)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2998579)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
Internet Explorer 6  
(2987107)  
(Moderada)  
Internet Explorer 7  
(2987107)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2972105)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2979574)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972106)  
(Crítica)  
Microsoft .NET Framework 4.0  
(2979575)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2993254)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2998579)  
(Importante)
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
[**MS14-056**](http://go.microsoft.com/fwlink/?linkid=513092)
</td>
<td style="border:1px solid black;">
[**MS14-057**](http://go.microsoft.com/fwlink/?linkid=513095)
</td>
<td style="border:1px solid black;">
[**MS14-058**](http://go.microsoft.com/fwlink/?linkid=513104)
</td>
<td style="border:1px solid black;">
[**MS14-060**](http://go.microsoft.com/fwlink/?linkid=513097)
</td>
<td style="border:1px solid black;">
[**MS14-062**](http://go.microsoft.com/fwlink/?linkid=513107)
</td>
<td style="border:1px solid black;">
[**MS14-063**](http://go.microsoft.com/fwlink/?linkid=513102)
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
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2987107)  
(Crítica)  
Internet Explorer 8  
(2987107)  
(Crítica)  
Internet Explorer 9  
(2987107)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2968292)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2972098)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2979568)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972106)  
(Crítica)  
Microsoft .NET Framework 4.0  
(2979575)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2972107)  
(Crítica)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2979578)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(3000869)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2998579)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2987107)  
(Crítica)  
Internet Explorer 8  
(2987107)  
(Crítica)  
Internet Explorer 9  
(2987107)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2968292)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2972098)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2979568)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972106)  
(Crítica)  
Microsoft .NET Framework 4.0  
(2979575)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2972107)  
(Crítica)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2979578)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(3000869)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2998579)  
(Importante)
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
[**MS14-056**](http://go.microsoft.com/fwlink/?linkid=513092)
</td>
<td style="border:1px solid black;">
[**MS14-057**](http://go.microsoft.com/fwlink/?linkid=513095)
</td>
<td style="border:1px solid black;">
[**MS14-058**](http://go.microsoft.com/fwlink/?linkid=513104)
</td>
<td style="border:1px solid black;">
[**MS14-060**](http://go.microsoft.com/fwlink/?linkid=513097)
</td>
<td style="border:1px solid black;">
[**MS14-062**](http://go.microsoft.com/fwlink/?linkid=513107)
</td>
<td style="border:1px solid black;">
[**MS14-063**](http://go.microsoft.com/fwlink/?linkid=513102)
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
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2987107)  
(Moderada)  
Internet Explorer 8  
(2987107)  
(Moderada)  
Internet Explorer 9  
(2987107)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2968292)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2972098)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2979568)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972106)  
(Crítica)  
Microsoft .NET Framework 4.0  
(2979575)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2972107)  
(Crítica)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2979578)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(3000869)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2998579)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2987107)  
(Moderada)  
Internet Explorer 8  
(2987107)  
(Moderada)  
Internet Explorer 9  
(2987107)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2968292)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2972098)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2979568)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972106)  
(Crítica)  
Microsoft .NET Framework 4.0  
(2979575)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2972107)  
(Crítica)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2979578)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(3000869)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2998579)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2987107)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 2.0 Service Pack 2  
(2968292)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2972098)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2979568)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972106)  
(Crítica)  
Microsoft .NET Framework 4.0  
(2979575)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(3000869)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2998579)  
(Importante)
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
[**MS14-056**](http://go.microsoft.com/fwlink/?linkid=513092)
</td>
<td style="border:1px solid black;">
[**MS14-057**](http://go.microsoft.com/fwlink/?linkid=513095)
</td>
<td style="border:1px solid black;">
[**MS14-058**](http://go.microsoft.com/fwlink/?linkid=513104)
</td>
<td style="border:1px solid black;">
[**MS14-060**](http://go.microsoft.com/fwlink/?linkid=513097)
</td>
<td style="border:1px solid black;">
[**MS14-062**](http://go.microsoft.com/fwlink/?linkid=513107)
</td>
<td style="border:1px solid black;">
[**MS14-063**](http://go.microsoft.com/fwlink/?linkid=513102)
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
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2987107)  
(Crítica)  
Internet Explorer 9  
(2987107)  
(Crítica)  
Internet Explorer 10  
(2987107)  
(Crítica)  
Internet Explorer 11  
(2987107)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2968294)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2972100)  
(Crítica)  
Microsoft .NET Framework 3.5.1  
(2979570)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972106)  
(Crítica)  
Microsoft .NET Framework 4.0  
(2979575)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2972107)  
(Crítica)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2979578)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(3000869)  
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
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2987107)  
(Crítica)  
Internet Explorer 9  
(2987107)  
(Crítica)  
Internet Explorer 10  
(2987107)  
(Crítica)  
Internet Explorer 11  
(2987107)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2968294)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2972100)  
(Crítica)  
Microsoft .NET Framework 3.5.1  
(2979570)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972106)  
(Crítica)  
Microsoft .NET Framework 4.0  
(2979575)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2972107)  
(Crítica)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2979578)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(3000869)  
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
**Windows Server 2008 R2**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-056**](http://go.microsoft.com/fwlink/?linkid=513092)
</td>
<td style="border:1px solid black;">
[**MS14-057**](http://go.microsoft.com/fwlink/?linkid=513095)
</td>
<td style="border:1px solid black;">
[**MS14-058**](http://go.microsoft.com/fwlink/?linkid=513104)
</td>
<td style="border:1px solid black;">
[**MS14-060**](http://go.microsoft.com/fwlink/?linkid=513097)
</td>
<td style="border:1px solid black;">
[**MS14-062**](http://go.microsoft.com/fwlink/?linkid=513107)
</td>
<td style="border:1px solid black;">
[**MS14-063**](http://go.microsoft.com/fwlink/?linkid=513102)
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
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2987107)  
(Moderada)  
Internet Explorer 9  
(2987107)  
(Moderada)  
Internet Explorer 10  
(2987107)  
(Moderada)  
Internet Explorer 11  
(2987107)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2968294)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2972100)  
(Crítica)  
Microsoft .NET Framework 3.5.1  
(2979570)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972106)  
(Crítica)  
Microsoft .NET Framework 4.0  
(2979575)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2972107)  
(Crítica)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2979578)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(3000869)  
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
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2987107)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2968294)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2972100)  
(Crítica)  
Microsoft .NET Framework 3.5.1  
(2979570)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972106)  
(Crítica)  
Microsoft .NET Framework 4.0  
(2979575)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(3000869)  
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
**Windows 8 y Windows 8.1**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-056**](http://go.microsoft.com/fwlink/?linkid=513092)
</td>
<td style="border:1px solid black;">
[**MS14-057**](http://go.microsoft.com/fwlink/?linkid=513095)
</td>
<td style="border:1px solid black;">
[**MS14-058**](http://go.microsoft.com/fwlink/?linkid=513104)
</td>
<td style="border:1px solid black;">
[**MS14-060**](http://go.microsoft.com/fwlink/?linkid=513097)
</td>
<td style="border:1px solid black;">
[**MS14-062**](http://go.microsoft.com/fwlink/?linkid=513107)
</td>
<td style="border:1px solid black;">
[**MS14-063**](http://go.microsoft.com/fwlink/?linkid=513102)
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
Windows 8 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2987107)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2968295)  
(Importante)  
Microsoft .NET Framework 3.5  
(2972101)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2979571)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978042)  
(Crítica)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2979577)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(3000869)  
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
Windows 8 para sistemas x64
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2987107)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2968295)  
(Importante)  
Microsoft .NET Framework 3.5  
(2972101)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2979571)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978042)  
(Crítica)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2979577)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas x64  
(3000869)  
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
Windows 8.1 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2987107)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2968296)  
(Importante)  
Microsoft .NET Framework 3.5  
(2972103)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2979573)  
(Importante)  
Microsoft .NET Framework 4.5.1/4.5.2  
(2978041)  
(Crítica)  
Microsoft .NET Framework 4.5.1/4.5.2  
(2979576)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas de 32 bits  
(3000869)  
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
Windows 8.1 para sistemas x64
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2987107)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2968296)  
(Importante)  
Microsoft .NET Framework 3.5  
(2972103)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2979573)  
(Importante)  
Microsoft .NET Framework 4.5.1/4.5.2  
(2978041)  
(Crítica)  
Microsoft .NET Framework 4.5.1/4.5.2  
(2979576)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8.1 para sistemas x64  
(3000869)  
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
**Windows Server 2012 y Windows Server 2012 R2**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-056**](http://go.microsoft.com/fwlink/?linkid=513092)
</td>
<td style="border:1px solid black;">
[**MS14-057**](http://go.microsoft.com/fwlink/?linkid=513095)
</td>
<td style="border:1px solid black;">
[**MS14-058**](http://go.microsoft.com/fwlink/?linkid=513104)
</td>
<td style="border:1px solid black;">
[**MS14-060**](http://go.microsoft.com/fwlink/?linkid=513097)
</td>
<td style="border:1px solid black;">
[**MS14-062**](http://go.microsoft.com/fwlink/?linkid=513107)
</td>
<td style="border:1px solid black;">
[**MS14-063**](http://go.microsoft.com/fwlink/?linkid=513102)
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
Windows Server 2012
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2987107)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2968295)  
(Importante)  
Microsoft .NET Framework 3.5  
(2972101)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2979571)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978042)  
(Crítica)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2979577)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(3000869)  
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
Windows Server 2012 R2
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2987107)  
(Moderada)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2968296)  
(Importante)  
Microsoft .NET Framework 3.5  
(2972103)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2979573)  
(Importante)  
Microsoft .NET Framework 4.5.1/4.5.2  
(2978041)  
(Crítica)  
Microsoft .NET Framework 4.5.1/4.5.2  
(2979576)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2  
(3000869)  
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
**Windows RT y Windows RT 8.1**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-056**](http://go.microsoft.com/fwlink/?linkid=513092)
</td>
<td style="border:1px solid black;">
[**MS14-057**](http://go.microsoft.com/fwlink/?linkid=513095)
</td>
<td style="border:1px solid black;">
[**MS14-058**](http://go.microsoft.com/fwlink/?linkid=513104)
</td>
<td style="border:1px solid black;">
[**MS14-060**](http://go.microsoft.com/fwlink/?linkid=513097)
</td>
<td style="border:1px solid black;">
[**MS14-062**](http://go.microsoft.com/fwlink/?linkid=513107)
</td>
<td style="border:1px solid black;">
[**MS14-063**](http://go.microsoft.com/fwlink/?linkid=513102)
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
Windows RT
</td>
<td style="border:1px solid black;">
Internet Explorer 10  
(2987107)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978042)  
(Crítica)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2979577)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows RT  
(3000869)  
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
Windows RT 8.1
</td>
<td style="border:1px solid black;">
Internet Explorer 11  
(2987107)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 4.5.1/4.5.2  
(2978041)  
(Crítica)  
Microsoft .NET Framework 4.5.1/4.5.2  
(2979576)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows RT 8.1  
(3000869)  
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
**Opción de instalación Server Core**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-056**](http://go.microsoft.com/fwlink/?linkid=513092)
</td>
<td style="border:1px solid black;">
[**MS14-057**](http://go.microsoft.com/fwlink/?linkid=513095)
</td>
<td style="border:1px solid black;">
[**MS14-058**](http://go.microsoft.com/fwlink/?linkid=513104)
</td>
<td style="border:1px solid black;">
[**MS14-060**](http://go.microsoft.com/fwlink/?linkid=513097)
</td>
<td style="border:1px solid black;">
[**MS14-062**](http://go.microsoft.com/fwlink/?linkid=513107)
</td>
<td style="border:1px solid black;">
[**MS14-063**](http://go.microsoft.com/fwlink/?linkid=513102)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
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
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2998579)  
(Importante)
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
(3000061)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2998579)  
(Importante)
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
(2968294)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2972100)  
(Crítica)  
Microsoft .NET Framework 3.5.1  
(2979570)  
(Importante)  
Microsoft .NET Framework 4.0  
(2972106)  
(Crítica)  
Microsoft .NET Framework 4.0  
(2979575)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2972107)  
(Crítica)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2979578)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(3000061)  
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
Windows Server 2012 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2968295)  
(Importante)  
Microsoft .NET Framework 3.5  
(2972101)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2979571)  
(Importante)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2978042)  
(Crítica)  
Microsoft .NET Framework 4.5/4.5.1/4.5.2  
(2979577)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(3000061)  
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
Windows Server 2012 R2 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2968296)  
(Importante)  
Microsoft .NET Framework 3.5  
(2972103)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2979573)  
(Importante)  
Microsoft .NET Framework 4.5.1/4.5.2  
(2978041)  
(Crítica)  
Microsoft .NET Framework 4.5.1/4.5.2  
(2979576)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 R2 (instalación Server Core)  
(3000061)  
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
</table>
 
 

### Herramientas y software para desarrolladores de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="2">
**ASP.NET MVC**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-059**](http://go.microsoft.com/fwlink/?linkid=507673)
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
ASP.NET MVC 2.0
</td>
<td style="border:1px solid black;">
ASP.NET MVC 2.0  
(2993939)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
ASP.NET MVC 3.0
</td>
<td style="border:1px solid black;">
ASP.NET MVC 3.0  
(2993937)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
ASP.NET MVC 4.0
</td>
<td style="border:1px solid black;">
ASP.NET MVC 4.0  
(2993928)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
ASP.NET MVC 5.0
</td>
<td style="border:1px solid black;">
ASP.NET MVC 5.0  
(2992080)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
ASP.NET MVC 5.1
</td>
<td style="border:1px solid black;">
ASP.NET MVC 5.1  
(2994397)  
(Importante)
</td>
</tr>
</table>
 
 

### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<td style="border:1px solid black;" colspan="2">
**Microsoft Office 2007**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-061**](http://go.microsoft.com/fwlink/?linkid=513106)
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
Microsoft Office 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 3  
(2883031)  
(Importante)  
Microsoft Word 2007 Service Pack 3  
(2883032)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="2">
**Microsoft Office 2010**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-061**](http://go.microsoft.com/fwlink/?linkid=513106)
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
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)  
(2883008)  
(Importante)  
Microsoft Word 2010 Service Pack 1 (ediciones de 32 bits)  
(2883013)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 32 bits)  
(2883008)  
(Importante)  
Microsoft Word 2010 Service Pack 2 (ediciones de 32 bits)  
(2883013)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)  
(2883008)  
(Importante)  
Microsoft Word 2010 Service Pack 1 (ediciones de 64 bits)  
(2883013)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 64 bits)  
(2883008)  
(Importante)  
Microsoft Word 2010 Service Pack 2 (ediciones de 64 bits)  
(2883013)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="2">
**Microsoft Office para Mac**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-061**](http://go.microsoft.com/fwlink/?linkid=513106)
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
Microsoft Office para Mac 2011
</td>
<td style="border:1px solid black;">
Microsoft Office para Mac 2011  
(3004865)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;" colspan="2">
**Otro software de Office**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS14-061**](http://go.microsoft.com/fwlink/?linkid=513106)
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
Paquete de compatibilidad de Microsoft Office Service Pack 3
</td>
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office Service Pack 3  
(2883031)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS14-061**

Estos boletines abarcan más de una categoría de software. Vea las demás tablas de esta sección para determinar el software afectado.

 

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
[**MS14-061**](http://go.microsoft.com/fwlink/?linkid=513106)
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
Microsoft SharePoint Server 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
Word Automation Services  
(2883098)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2010 Service Pack 2
</td>
<td style="border:1px solid black;">
Word Automation Services  
(2883098)  
(Importante)
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
[**MS14-061**](http://go.microsoft.com/fwlink/?linkid=513106)
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
Microsoft Office Web Apps 2010
</td>
<td style="border:1px solid black;">
Microsoft Office Web Apps Server 2010  
(2889827)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Web Apps 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft Office Web Apps Server 2010 Service Pack 1  
(2889827)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Web Apps 2010 Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft Office Web Apps Server 2010 Service Pack 2  
(2889827)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS14-061**

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

**MS14-056**

-   James Forshaw, de [Context Information Security](http://www.contextis.com/), por informar de la vulnerabilidad de elevación de privilegios en Internet Explorer (CVE-2014-4123)
-   James Forshaw, de [Context Information Security](http://www.contextis.com/), por informar de la vulnerabilidad de elevación de privilegios en Internet Explorer (CVE-2014-4124)
-   Rohit Mothe, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4126)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4127)
-   Omair, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4128)
-   Jason Kratzer, por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4128)
-   [Adlab, de Venustech](http://www.venustech.com.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4129)
-   Sky, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4130)
-   Zhibin Hu, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4132)
-   José A. Vázquez, de Yenteasy - Security Research en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4132)
-   Zhibin Hu, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4133)
-   Zhibin Hu, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4134)
-   Liu Long, de [Qihoo 360](http://www.360.cn/), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4137)
-   SkyLined, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4138)
-   John Villamil (@day6reak), por informar de la vulnerabilidad de omisión de la característica de seguridad en Internet Explorer (CVE-2014-4140)
-   Peter 'corelanc0d3r' Van Eeckhoutte, de [Corelan](http://www.corelangcv.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria relacionada con Internet Explorer (CVE-2014-4141)

**MS14-057**

-   James Forshaw, de [Context Information Security](http://www.contextis.com/), por informar de la vulnerabilidad de elevación de privilegios de ClickOnce en .NET (CVE-2014-4073)

**MS14-058**

-   [CrowdStrike Intelligence Team](http://www.crowdstrike.com/), por colaborar con nosotros en la vulnerabilidad de elevación de privilegios en Win32k.sys (CVE-2014-4113)
-   [FireEye, Inc.](http://www.fireeye.com/), por colaborar con nosotros en la vulnerabilidad de elevación de privilegios en Win32k.sys (CVE-2014-4113)
-   [FireEye, Inc.](http://www.fireeye.com/), por colaborar con nosotros en la vulnerabilidad de elevación de privilegios en el análisis de fuentes TrueType (CVE-2014-4148)

**MS14-060**

-   [iSIGHT Partners](http://www.isightpartners.com/), por informar de la vulnerabilidad de ejecución remota de código en Windows OLE (CVE-2014-4114)

**MS14-061**

-   3S Labs, en colaboración con [HP](http://www.hpenterprisesecurity.com/products)[Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de la vulnerabilidad en el formato de archivo de Microsoft Word (CVE-2014-4117)

**MS14-063**

-   Marcin “Icewall” Noga, de [Cisco Talos](http://www.sourcefire.com/solutions/research), por informar de la vulnerabilidad de elevación de privilegios en el controlador de particiones de disco de Windows (CVE-2014-4115)

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

-   V1.0 (14 de octubre de 2014): Publicación del resumen del boletín.

*Página generada el 2014-10-13 14:39Z-07:00.*
