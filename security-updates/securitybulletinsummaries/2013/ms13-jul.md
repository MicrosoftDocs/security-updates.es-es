---
TOCTitle: 'MS13-JUL'
Title: Resumen del boletín de seguridad de Microsoft de julio 2013
ms:assetid: 'ms13-jul'
ms:contentKeyID: 61225449
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms13-jul(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de julio 2013
===========================================================

Publicado: martes, 9 de julio de 2013 | Actualizado: martes, 27 de agosto de 2013

**Versión:** 3.0

Este resumen del boletín enumera los boletines de seguridad publicados para julio de 2013.

Con la publicación de los boletines de seguridad de julio de 2013, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 4 de julio de 2013. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 10 de julio de 2013, a las 11:00 a.m., hora del Pacífico (EE. UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de julio](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032556406&culture=en-us). Después de esta fecha, este webcast estará disponible [a petición](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032538733&culture=en-us).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, Información adicional.

### Información del boletín

#### Resúmenes ejecutivos

En la tabla siguiente se resumen los boletines de seguridad de este mes por orden de gravedad.

Para obtener detalles acerca del software afectado, vea la siguiente sección, Software afectado.

 
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299844">MS13-052</a></td>
<td style="border:1px solid black;">Vulnerabilidades en .NET Framework y Silverlight podrían permitir la ejecución remota de código (2861561) <br />
<br />
Esta actualización de seguridad resuelve cinco vulnerabilidades de las que se ha informado de forma privada en Microsoft .NET Framework y Microsoft Silverlight. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si una aplicación de confianza usa un determinado patrón de código. Un intruso que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario que ha iniciado sesión. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Microsoft .NET Framework,<br />
Microsoft Silverlight</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=301423">MS13-053</a></td>
<td style="border:1px solid black;">Vulnerabilidades en los controladores modo kernel de Windows podrían permitir la ejecución remota de código (2850851)<br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma pública y seis vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad más grave podría permitir la ejecución remota de código si un usuario consulta contenido compartido que inserta archivos de fuente TrueType. Un atacante que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=301531">MS13-054</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en GDI+ podría permitir la ejecución remota de código (2848295)<br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad en Microsoft Windows, Microsoft Office, Microsoft Lync y Microsoft Visual Studio de la que se ha informado de forma privada. La vulnerabilidad podría permitir la ejecución remota de código si un usuario consulta contenido compartido que inserta archivos de fuentes TrueType.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Microsoft Office,<br />
Microsoft Visual Studio,<br />
Microsoft Lync</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Actualización de seguridad acumulativa para Internet Explorer (2846071)  <br />
<br />
Esta actualización de seguridad resuelve diecisiete vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. La más grave de las vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un atacante que aprovechara la más grave de estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309326">MS13-056</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en Microsoft DirectShow podría permitir la ejecución remota de código (2845187)<br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo de imagen especialmente diseñado. Un intruso que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario local. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=301528">MS13-057</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en Tiempo de ejecución de Windows Media Format podría permitir la ejecución remota de código (2847883)<br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo multimedia especialmente diseñado. Un intruso que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario local. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=308992">MS13-058</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en Windows Defender podría permitir la elevación de privilegios (2847927)<br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Windows Defender para Windows 7 y Windows Defender cuando está instalado en Windows Server 2008 R2. La vulnerabilidad podría permitir la elevación de privilegios debido a los nombres de ruta de acceso que usa Windows Defender. Un atacante que consiga aprovechar esta vulnerabilidad podría ejecutar código arbitrario y tomar el control completo de un sistema afectado. De esta forma, el atacante podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Para aprovechar esta vulnerabilidad, el usuario debe tener unas credenciales de inicio de sesión válidas. Los usuarios remotos no pueden aprovechar esta vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">No requiere reinicio</td>
<td style="border:1px solid black;">Software de seguridad de Microsoft</td>
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299844">MS13-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de análisis de fuentes TrueType</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3129">CVE-2013-3129</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299844">MS13-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de infracción de acceso a matriz</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3131">CVE-2013-3131</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299844">MS13-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de omisión de reflejo de delegación</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3132">CVE-2013-3132</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299844">MS13-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de inserción de métodos anónimos</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3133">CVE-2013-3133</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299844">MS13-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de asignación de matriz</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3134">CVE-2013-3134</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299844">MS13-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de serialización de delegación</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3171">CVE-2013-3171</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299844">MS13-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de puntero nulo</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3178">CVE-2013-3178</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=301423">MS13-053</a></td>
<td style="border:1px solid black;">Vulnerabilidad de asignación de memoria en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1300">CVE-2013-1300</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=301423">MS13-053</a></td>
<td style="border:1px solid black;">Vulnerabilidad de anulación de referencia en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1340">CVE-2013-1340</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio en la versión de software más reciente.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=301423">MS13-053</a></td>
<td style="border:1px solid black;">Vulnerabilidad en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1345">CVE-2013-1345</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio en la versión de software más reciente.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=301423">MS13-053</a></td>
<td style="border:1px solid black;">Vulnerabilidad de análisis de fuentes TrueType</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3129">CVE-2013-3129</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=301423">MS13-053</a></td>
<td style="border:1px solid black;">Vulnerabilidad de divulgación de información en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3167">CVE-2013-3167</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de divulgación de información que podría conllevar la elevación de privilegios.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=301423">MS13-053</a></td>
<td style="border:1px solid black;">Vulnerabilidad de sobrescritura del búfer en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3173">CVE-2013-3173</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=301423">MS13-053</a></td>
<td style="border:1px solid black;">Vulnerabilidad de lectura de AV en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3660">CVE-2013-3660</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.<br />
<br />
Microsoft tiene constancia de ataques dirigidos que intentan aprovechar esta vulnerabilidad como una vulnerabilidad de elevación de privilegios.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=301531">MS13-054</a></td>
<td style="border:1px solid black;">Vulnerabilidad de análisis de fuentes TrueType</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3129">CVE-2013-3129</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3115">CVE-2013-3115</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3143">CVE-2013-3143</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3144">CVE-2013-3144</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3145">CVE-2013-3145</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3146">CVE-2013-3146</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3147">CVE-2013-3147</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3148">CVE-2013-3148</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3149">CVE-2013-3149</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3150">CVE-2013-3150</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3151">CVE-2013-3151</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3152">CVE-2013-3152</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3153">CVE-2013-3153</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3161">CVE-2013-3161</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3162">CVE-2013-3162</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3163">CVE-2013-3163</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Microsoft tiene constancia de ataques dirigidos que intentan aprovechar esta vulnerabilidad a través de Internet Explorer 8.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3164">CVE-2013-3164</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309324">MS13-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad de codificación de caracteres de desplazamiento JIS</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3166">CVE-2013-3166</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=309326">MS13-056</a></td>
<td style="border:1px solid black;">Vulnerabilidad de sobrescritura de memoria arbitraria en DirectShow</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3174">CVE-2013-3174</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=301528">MS13-057</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código en el descodificador de vídeo</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3127">CVE-2013-3127</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=308992">MS13-058</a></td>
<td style="border:1px solid black;">Vulnerabilidad de nombre de ruta de acceso incorrecto en Microsoft Windows 7 Defender</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3154">CVE-2013-3154</a></td>
<td style="border:1px solid black;">No está afectada</td>
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
  
#### Componentes y sistema operativo Windows

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="7" style="border:1px solid black;">
Windows XP  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-052](http://go.microsoft.com/fwlink/?linkid=299844)
</td>
<td style="border:1px solid black;">
[MS13-053](http://go.microsoft.com/fwlink/?linkid=301423)
</td>
<td style="border:1px solid black;">
[MS13-054](http://go.microsoft.com/fwlink/?linkid=301531)
</td>
<td style="border:1px solid black;">
[MS13-055](http://go.microsoft.com/fwlink/?linkid=309324)
</td>
<td style="border:1px solid black;">
[MS13-056](http://go.microsoft.com/fwlink/?linkid=309326)
</td>
<td style="border:1px solid black;">
[MS13-057](http://go.microsoft.com/fwlink/?linkid=301528)
</td>
</tr>
<tr class="alternateRow">
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
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 1.0 Service Pack 3  
(Media Center Edition 2005 Service Pack 3 y Tablet PC Edition 2005 Service Pack 3 solo)  
(2833951)  
(Importante)  
Microsoft .NET Framework 1.1 Service Pack 1  
(2833941)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2833940)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2844285)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2832411)  
(Crítica)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2840629)  
(Importante)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2832407)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2835393)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2840628)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows XP Service Pack 3  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows XP Service Pack 3  
(Windows GDI+)  
(2834886)  
(Crítica)  
Windows XP Service Pack 3  
(solo Windows XP Tablet PC Edition 2005)  
(Journal)  
(2835364)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 6   
(2846071)  
(Crítica)  
Internet Explorer 7   
(2846071)  
(Crítica)  
Internet Explorer 8   
(2846071)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows XP Service Pack 3  
(2845187)  
(Crítica)
</td>
<td style="border:1px solid black;">
Tiempo de ejecución de Windows Media Format 11<sup>[1]</sup>
(wmvdecod.dll)  
(Solo Media Center Edition)  
(2834904)  
(Crítica)  
Tiempo de ejecución de Windows Media Format 9.5  
(wmvdmod.dll)  
(Solo Media Center Edition)  
(2834905)  
(Crítica)  
Módulo de tiempo de ejecución de Windows Media Format 9  
(wmvdmod.dll)  
(2803821)  
(Crítica)  
Tiempo de ejecución de Windows Media Format 9.5<sup>[2]</sup>
(wmvdmod.dll)  
(2834902)  
(Crítica)  
Tiempo de ejecución de Windows Media Format 9.5<sup>[3]</sup>
(wmvdmod.dll)  
(2834903)  
(Crítica)  
Tiempo de ejecución de Windows Media Format 11  
(wmvdecod.dll)  
(2834904)  
(Crítica)  
wmv9vcm.dll (códec)  
(2845142)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 1.1 Service Pack 1  
(2833941)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2833940)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2(2844285)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2832411)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2832407)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2835393)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>(2840628)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2  
(Windows GDI+)  
(2834886)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 6   
(2846071)  
(Crítica)  
Internet Explorer 7   
(2846071)  
(Crítica)  
Internet Explorer 8   
(2846071)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2  
(2845187)  
(Crítica)
</td>
<td style="border:1px solid black;">
Tiempo de ejecución de Windows Media Format 9.5  
(wmvdmod.dll)  
(2803821)  
(Crítica)  
Tiempo de ejecución de Windows Media Format 9.5 x64  
(wmvdmod.dll)  
(2834902)  
(Crítica)  
Tiempo de ejecución de Windows Media Format 11  
(wmvdecod.dll)  
(2834904)  
(Crítica)  
wmv9vcm.dll (códec)  
(2845142)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-052](http://go.microsoft.com/fwlink/?linkid=299844)
</td>
<td style="border:1px solid black;">
[MS13-053](http://go.microsoft.com/fwlink/?linkid=301423)
</td>
<td style="border:1px solid black;">
[MS13-054](http://go.microsoft.com/fwlink/?linkid=301531)
</td>
<td style="border:1px solid black;">
[MS13-055](http://go.microsoft.com/fwlink/?linkid=309324)
</td>
<td style="border:1px solid black;">
[MS13-056](http://go.microsoft.com/fwlink/?linkid=309326)
</td>
<td style="border:1px solid black;">
[MS13-057](http://go.microsoft.com/fwlink/?linkid=301528)
</td>
</tr>
<tr class="alternateRow">
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
[Moderada](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 1.1 Service Pack 1  
(2833949)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2833940)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2844285)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2832411)  
(Crítica)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2840629)  
(Importante)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2832407)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2835393)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2840628)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(Windows GDI+)  
(2834886)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 6   
(2846071)  
(Moderada)  
Internet Explorer 7  
(2846071)  
(Moderada)  
Internet Explorer 8  
(2846071)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(2845187)  
(Crítica)
</td>
<td style="border:1px solid black;">
Tiempo de ejecución de Windows Media Format 9.5  
(wmvdmod.dll)  
(2803821)  
(Crítica)  
wmv9vcm.dll (códec)  
(2845142)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 1.1 Service Pack 1  
(2833941)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2833940)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2844285)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2832411)  
(Crítica)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2840629)  
(Importante)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2832407)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2835393)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2840628)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(Windows GDI+)  
(2834886)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 6   
(2846071)  
(Moderada)  
Internet Explorer 7  
(2846071)  
(Moderada)  
Internet Explorer 8  
(2846071)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2845187)  
(Crítica)
</td>
<td style="border:1px solid black;">
Tiempo de ejecución de Windows Media Format 9.5  
(wmvdmod.dll)  
(2803821)  
(Crítica)  
Tiempo de ejecución de Windows Media Format 9.5 x64  
(wmvdmod.dll)  
(2834902)  
(Crítica)  
Tiempo de ejecución de Windows Media Format 11  
(wmvdmod.dll)  
(2834904)  
(Crítica)  
wmv9vcm.dll (códec)  
(2845142)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 1.1 Service Pack 1  
(2833941)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2833940)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2844285)  
(Importante)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2840629)  
(Importante)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2835393)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2840628)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(Windows GDI+)  
(2834886)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 6   
(2846071)  
(Moderada)  
Internet Explorer 7  
(2846071)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2845187)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-052](http://go.microsoft.com/fwlink/?linkid=299844)
</td>
<td style="border:1px solid black;">
[MS13-053](http://go.microsoft.com/fwlink/?linkid=301423)
</td>
<td style="border:1px solid black;">
[MS13-054](http://go.microsoft.com/fwlink/?linkid=301531)
</td>
<td style="border:1px solid black;">
[MS13-055](http://go.microsoft.com/fwlink/?linkid=309324)
</td>
<td style="border:1px solid black;">
[MS13-056](http://go.microsoft.com/fwlink/?linkid=309326)
</td>
<td style="border:1px solid black;">
[MS13-057](http://go.microsoft.com/fwlink/?linkid=301528)
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
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 1.1 Service Pack 1  
(2833941)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2833947)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2844287)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2832412)  
(Crítica)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2840629)  
(Importante)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2832407)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2835393)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2840628)  
(Importante)  
Microsoft .NET Framework 4.5  
(2835622)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2833957)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2840642)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(DirectWrite)  
(2835361)  
(Crítica)  
Windows Vista Service Pack 2  
(Windows GDI+)  
(2834886)  
(Crítica)  
Windows Vista Service Pack 2  
(Journal)  
(2835364)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2846071)  
(Crítica)  
Internet Explorer 8  
(2846071)  
(Crítica)  
Internet Explorer 9   
(2846071)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2845187)  
(Crítica)
</td>
<td style="border:1px solid black;">
Reproductor de Windows Media 11  
(wmvdecod.dll)  
(2803821)  
(Crítica)  
wmv9vcm.dll (códec)  
(2845142)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 1.1 Service Pack 1  
(2833941)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2833947)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2844287)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2832412)  
(Crítica)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2840629)  
(Importante)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2832407)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2835393)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2840628)  
(Importante)  
Microsoft .NET Framework 4.5  
(2835622)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2833957)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2840642)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(DirectWrite)  
(2835361)  
(Crítica)  
Windows Vista x64 Edition Service Pack 2  
(Windows GDI+)  
(2834886)  
(Crítica)  
Windows Vista x64 Edition Service Pack 2  
(Journal)  
(2835364)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2846071)  
(Crítica)  
Internet Explorer 8  
(2846071)  
(Crítica)  
Internet Explorer 9   
(2846071)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2845187)  
(Crítica)
</td>
<td style="border:1px solid black;">
Reproductor de Windows Media 11  
(wmvdecod.dll)  
(2803821)  
(Crítica)  
wmv9vcm.dll (códec)  
(2845142)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-052](http://go.microsoft.com/fwlink/?linkid=299844)
</td>
<td style="border:1px solid black;">
[MS13-053](http://go.microsoft.com/fwlink/?linkid=301423)
</td>
<td style="border:1px solid black;">
[MS13-054](http://go.microsoft.com/fwlink/?linkid=301531)
</td>
<td style="border:1px solid black;">
[MS13-055](http://go.microsoft.com/fwlink/?linkid=309324)
</td>
<td style="border:1px solid black;">
[MS13-056](http://go.microsoft.com/fwlink/?linkid=309326)
</td>
<td style="border:1px solid black;">
[MS13-057](http://go.microsoft.com/fwlink/?linkid=301528)
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
[Moderada](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 1.1 Service Pack 1  
(2833941)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2833947)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2844287)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2832412)  
(Crítica)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2840629)  
(Importante)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2832407)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2835393)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2840628)  
(Importante)  
Microsoft .NET Framework 4.5  
(2835622)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2833957)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2840642)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(DirectWrite)  
(2835361)  
(Crítica)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(Windows GDI+)  
(2834886)  
(Crítica)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(Journal)  
(2835364)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2846071)  
(Moderada)  
Internet Explorer 8  
(2846071)  
(Moderada)  
Internet Explorer 9   
(2846071)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2845187)  
(Crítica)
</td>
<td style="border:1px solid black;">
Reproductor de Windows Media 11\[4\]  
(wmvdecod.dll)  
(2803821)  
(Crítica)  
wmv9vcm.dll (códec) \[5\]  
(2845142)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 1.1 Service Pack 1  
(2833941)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2833947)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2844287)  
(Importante)  
Microsoft .NET Framework 3.0 Service Pack 2  
(2832412)  
(Crítica)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2840629)  
(Importante)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2832407)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2835393)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2840628)  
(Importante)  
Microsoft .NET Framework 4.5  
(2835622)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2833957)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2840642)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(DirectWrite)  
(2835361)  
(Crítica)  
Windows Server 2008 para sistemas x64 Service Pack 2  
(Windows GDI+)  
(2834886)  
(Crítica)  
Windows Server 2008 para sistemas x64 Service Pack 2  
(Journal)  
(2835364)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2846071)  
(Moderada)  
Internet Explorer 8  
(2846071)  
(Moderada)  
Internet Explorer 9   
(2846071)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2845187)  
(Crítica)
</td>
<td style="border:1px solid black;">
Reproductor de Windows Media 11\[4\]  
(wmvdecod.dll)  
(2803821)  
(Crítica)  
wmv9vcm.dll (códec) \[5\]  
(2845142)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 1.1 Service Pack 1  
(2833941)  
(Importante)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2833947)  
(Crítica)  
Microsoft .NET Framework 2.0 Service Pack 2  
(2844287)  
(Importante)  
Microsoft .NET Framework 3.5 Service Pack 1  
(2840629)  
(Importante)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2835393)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2840628)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(Windows GDI+)  
(2834886)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2846071)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows 7
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-052](http://go.microsoft.com/fwlink/?linkid=299844)
</td>
<td style="border:1px solid black;">
[MS13-053](http://go.microsoft.com/fwlink/?linkid=301423)
</td>
<td style="border:1px solid black;">
[MS13-054](http://go.microsoft.com/fwlink/?linkid=301531)
</td>
<td style="border:1px solid black;">
[MS13-055](http://go.microsoft.com/fwlink/?linkid=309324)
</td>
<td style="border:1px solid black;">
[MS13-056](http://go.microsoft.com/fwlink/?linkid=309326)
</td>
<td style="border:1px solid black;">
[MS13-057](http://go.microsoft.com/fwlink/?linkid=301528)
</td>
</tr>
<tr class="alternateRow">
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
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2832414)  
(Crítica)  
Microsoft .NET Framework 3.5.1  
(2833946)  
(Crítica)  
Microsoft .NET Framework 3.5.1  
(2840631)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2844286)  
(Importante)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2835393)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2840628)  
(Importante)  
Microsoft .NET Framework 4.5  
(2833957)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2840642)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(DirectWrite)  
(2835361)  
(Crítica)  
Windows 7 para sistemas de 32 bits Service Pack 1  
(Windows GDI+)  
(2834886)  
(Crítica)  
Windows 7 para sistemas de 32 bits Service Pack 1  
(Journal)  
(2835364)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2846071)  
(Crítica)  
Internet Explorer 9   
(2846071)  
(Crítica)  
Internet Explorer 10   
(2846071)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2845187)  
(Crítica)
</td>
<td style="border:1px solid black;">
Reproductor de Windows Media 12  
(wmvdecod.dll)  
(2803821)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2832414)  
(Crítica)  
Microsoft .NET Framework 3.5.1  
(2833946)  
(Crítica)  
Microsoft .NET Framework 3.5.1  
(2840631)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2844286)  
(Importante)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2835393)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2840628)  
(Importante)  
Microsoft .NET Framework 4.5  
(2833957)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2840642)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(DirectWrite)  
(2835361)  
(Crítica)  
Windows 7 para sistemas x64 Service Pack 1  
(Windows GDI+)  
(2834886)  
(Crítica)  
Windows 7 para sistemas x64 Service Pack 1  
(Journal)  
(2835364)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2846071)  
(Crítica)  
Internet Explorer 9   
(2846071)  
(Crítica)  
Internet Explorer 10   
(2846071)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2845187)  
(Crítica)
</td>
<td style="border:1px solid black;">
Reproductor de Windows Media 12  
(wmvdecod.dll)  
(2803821)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Server 2008 R2
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-052](http://go.microsoft.com/fwlink/?linkid=299844)
</td>
<td style="border:1px solid black;">
[MS13-053](http://go.microsoft.com/fwlink/?linkid=301423)
</td>
<td style="border:1px solid black;">
[MS13-054](http://go.microsoft.com/fwlink/?linkid=301531)
</td>
<td style="border:1px solid black;">
[MS13-055](http://go.microsoft.com/fwlink/?linkid=309324)
</td>
<td style="border:1px solid black;">
[MS13-056](http://go.microsoft.com/fwlink/?linkid=309326)
</td>
<td style="border:1px solid black;">
[MS13-057](http://go.microsoft.com/fwlink/?linkid=301528)
</td>
</tr>
<tr class="alternateRow">
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
[Moderada](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2832414)  
(Crítica)  
Microsoft .NET Framework 3.5.1  
(2833946)  
(Crítica)  
Microsoft .NET Framework 3.5.1  
(2840631)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2844286)  
(Importante)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2835393)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2840628)  
(Importante)  
Microsoft .NET Framework 4.5  
(2833957)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2840642)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(DirectWrite)  
(2835361)  
(Crítica)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(Windows GDI+)  
(2834886)  
(Crítica)  
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(Journal)  
(2835364)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2846071)  
(Moderada)  
Internet Explorer 9   
(2846071)  
(Moderada)  
Internet Explorer 10   
(2846071)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2845187)  
(Crítica)
</td>
<td style="border:1px solid black;">
Reproductor de Windows Media 12\[4\]  
(wmvdecod.dll)  
(2803821)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2833946)  
(Crítica)  
Microsoft .NET Framework 3.5.1  
(2840631)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2844286)  
(Importante)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2835393)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2840628)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(DirectWrite)  
(2835361)  
(Crítica)  
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(Windows GDI+)  
(2834886)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2846071)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows 8
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-052](http://go.microsoft.com/fwlink/?linkid=299844)
</td>
<td style="border:1px solid black;">
[MS13-053](http://go.microsoft.com/fwlink/?linkid=301423)
</td>
<td style="border:1px solid black;">
[MS13-054](http://go.microsoft.com/fwlink/?linkid=301531)
</td>
<td style="border:1px solid black;">
[MS13-055](http://go.microsoft.com/fwlink/?linkid=309324)
</td>
<td style="border:1px solid black;">
[MS13-056](http://go.microsoft.com/fwlink/?linkid=309326)
</td>
<td style="border:1px solid black;">
[MS13-057](http://go.microsoft.com/fwlink/?linkid=301528)
</td>
</tr>
<tr class="alternateRow">
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
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2832418)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2833959)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2840633)  
(Importante)  
Microsoft .NET Framework 3.5  
(2844289)  
(Importante)  
Microsoft .NET Framework 4.5  
(2833958)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2840632)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(DirectWrite)  
(2835361)  
(Crítica)  
Windows 8 para sistemas de 32 bits  
(Journal)  
(2835364)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2846071)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2845187)  
(Crítica)
</td>
<td style="border:1px solid black;">
Reproductor de Windows Media 12  
(wmvdecod.dll)  
(2803821)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 8 para sistemas de 64 bits
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2832418)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2833959)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2840633)  
(Importante)  
Microsoft .NET Framework 3.5  
(2844289)  
(Importante)  
Microsoft .NET Framework 4.5  
(2833958)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2840632)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 64 bits  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 64 bits  
(DirectWrite)  
(2835361)  
(Crítica)  
Windows 8 para sistemas de 64 bits  
(Journal)  
(2835364)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2846071)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 64 bits  
(2845187)  
(Crítica)
</td>
<td style="border:1px solid black;">
Reproductor de Windows Media 12  
(wmvdecod.dll)  
(2803821)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Server 2012
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-052](http://go.microsoft.com/fwlink/?linkid=299844)
</td>
<td style="border:1px solid black;">
[MS13-053](http://go.microsoft.com/fwlink/?linkid=301423)
</td>
<td style="border:1px solid black;">
[MS13-054](http://go.microsoft.com/fwlink/?linkid=301531)
</td>
<td style="border:1px solid black;">
[MS13-055](http://go.microsoft.com/fwlink/?linkid=309324)
</td>
<td style="border:1px solid black;">
[MS13-056](http://go.microsoft.com/fwlink/?linkid=309326)
</td>
<td style="border:1px solid black;">
[MS13-057](http://go.microsoft.com/fwlink/?linkid=301528)
</td>
</tr>
<tr class="alternateRow">
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
[Moderada](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2832418)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2833959)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2840633)  
(Importante)  
Microsoft .NET Framework 3.5  
(2844289)  
(Importante)  
Microsoft .NET Framework 4.5  
(2833958)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2840632)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(DirectWrite)  
(2835361)  
(Crítica)  
Windows Server 2012  
(Journal)  
(2835364)(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2846071)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2845187)  
(Crítica)
</td>
<td style="border:1px solid black;">
Reproductor de Windows Media 12\[4\]  
(wmvdecod.dll)  
(2803821)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows RT
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-052](http://go.microsoft.com/fwlink/?linkid=299844)
</td>
<td style="border:1px solid black;">
[MS13-053](http://go.microsoft.com/fwlink/?linkid=301423)
</td>
<td style="border:1px solid black;">
[MS13-054](http://go.microsoft.com/fwlink/?linkid=301531)
</td>
<td style="border:1px solid black;">
[MS13-055](http://go.microsoft.com/fwlink/?linkid=309324)
</td>
<td style="border:1px solid black;">
[MS13-056](http://go.microsoft.com/fwlink/?linkid=309326)
</td>
<td style="border:1px solid black;">
[MS13-057](http://go.microsoft.com/fwlink/?linkid=301528)
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
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows RT
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 4.5  
(2833958)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2840632)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows RT  
(DirectWrite)  
(2835361)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2846071)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Reproductor de Windows Media 12  
(wmvdecod.dll)  
(2803821)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Opción de instalación Server Core
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-052](http://go.microsoft.com/fwlink/?linkid=299844)
</td>
<td style="border:1px solid black;">
[MS13-053](http://go.microsoft.com/fwlink/?linkid=301423)
</td>
<td style="border:1px solid black;">
[MS13-054](http://go.microsoft.com/fwlink/?linkid=301531)
</td>
<td style="border:1px solid black;">
[MS13-055](http://go.microsoft.com/fwlink/?linkid=309324)
</td>
<td style="border:1px solid black;">
[MS13-056](http://go.microsoft.com/fwlink/?linkid=309326)
</td>
<td style="border:1px solid black;">
[MS13-057](http://go.microsoft.com/fwlink/?linkid=301528)
</td>
</tr>
<tr class="alternateRow">
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
Ninguna
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
Ninguna
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
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(Windows GDI+)  
(2834886)  
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
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(Windows GDI+)  
(2834886)  
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
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5.1  
(2833946)  
(Crítica)  
Microsoft .NET Framework 3.5.1  
(2840631)  
(Importante)  
Microsoft .NET Framework 3.5.1  
(2844286)  
(Importante)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2835393)  
(Crítica)  
Microsoft .NET Framework 4<sup>[1]</sup>
(2840628)  
(Importante)  
Microsoft .NET Framework 4.5  
(2833957)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2840642)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(Windows GDI+)  
(2834886)  
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
Windows Server 2012 (instalación Server Core)
</td>
<td style="border:1px solid black;">
Microsoft .NET Framework 3.5  
(2832418)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2833959)  
(Crítica)  
Microsoft .NET Framework 3.5  
(2840633)  
(Importante)  
Microsoft .NET Framework 3.5  
(2844289)  
(Importante)  
Microsoft .NET Framework 4.5  
(2833958)  
(Crítica)  
Microsoft .NET Framework 4.5  
(2840632)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(2850851)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)  
(DirectWrite)  
(2835361)  
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
 
Notas para MS13-052

<sup>[1]</sup>.NET Framework 4 y .NET Framework 4 Client Profile están afectados. Los paquetes redistribuibles de .NET Framework versión 4 están disponibles en dos perfiles: .NET Framework 4.0 y .NET Framework 4.0 Client Profile. .NET Framework 4.0 Client Profile es un subconjunto de .NET Framework 4.0. La vulnerabilidad corregida en esta actualización afecta a .NET Framework 4.0 y .NET Framework 4.0 Client Profile. Para obtener más información, vea el artículo de MSDN [Instalar .NET Framework](http://msdn.microsoft.com/library/5a4x27ek).

Vea también las demás categorías de esta sección, Ubicaciones de descarga y software afectado, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

Nota para MS13-053 y MS13-055

Vea también las demás categorías de esta sección, Ubicaciones de descarga y software afectado, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

Nota para MS13-054

Vea también las demás categorías de esta sección, Ubicaciones de descarga y software afectado, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

Notas para MS13-057

<sup>[1]</sup>Esta actualización solo se ofrece los sistemas que se han actualizado a Tiempo de ejecución de Windows Media Format 11 o Reproductor de Windows Media 11.  
<sup>[2]</sup>Esta actualización sólo se ofrece a los sistemas que ejecutan Tiempo de ejecución de Windows Media Format 9.5 NL.  
<sup>[3]</sup>Esta actualización solo se ofrece los sistemas que ejecutan Tiempo de ejecución de Windows Media Format 9.5 L.  
\[4\]Esta actualización solo se ofrece si la característica Experiencia de escritorio está habilitada.  
\[5\]Esta actualización solo se ofrece si está habilitada la característica opcional Experiencia de escritorio y está presente el códec wmv9vcm.dll. Vea el boletín para obtener más información.

Vea también las demás categorías de esta sección, Ubicaciones de descarga y software afectado, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Software de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-054](http://go.microsoft.com/fwlink/?linkid=301531)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft Office 2003 Service Pack 3  
(2817480)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 3  
(2687309)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)  
(2687276)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)  
(2687276)  
(Importante)
</td>
</tr>
</table>
 
Nota para MS13-054

Vea también las demás categorías de esta sección, Ubicaciones de descarga y software afectado, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Herramientas y software para desarrolladores de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Visual Studio
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-052](http://go.microsoft.com/fwlink/?linkid=299844)
</td>
<td style="border:1px solid black;">
[MS13-054](http://go.microsoft.com/fwlink/?linkid=301531)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Visual Studio .NET 2003 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft Visual Studio .NET 2003 Service Pack 1<sup>[1]</sup>
(2856545)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Silverlight
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Silverlight 5
</td>
<td style="border:1px solid black;">
[MS13-052](http://go.microsoft.com/fwlink/?linkid=299844)
</td>
<td style="border:1px solid black;">
[MS13-054](http://go.microsoft.com/fwlink/?linkid=301531)
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
Ninguna
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
Microsoft Silverlight 5 cuando está instalado en Mac  
(2847559)  
(Crítica)  
Microsoft Silverlight 5 Developer Runtime cuando está instalado en Mac  
(2847559)  
(Crítica)  
Microsoft Silverlight 5 cuando está instalado en las ediciones de 32 bits de los clientes Microsoft Windows  
(2847559)  
(Crítica)  
Microsoft Silverlight 5 cuando está instalado en las ediciones x64 de los clientes Microsoft Windows  
(2847559)  
(Crítica)  
Microsoft Silverlight 5 Developer Runtime cuando está instalado en todas las versiones compatibles de los clientes Microsoft Windows  
(2847559)  
(Crítica)  
Microsoft Silverlight 5 cuando está instalado en las ediciones de 32 bits de los servidores Microsoft Windows  
(2847559)  
(Crítica)  
Microsoft Silverlight 5 cuando está instalado en las ediciones x64 de los servidores Microsoft Windows  
(2847559)  
(Crítica)  
Microsoft Silverlight 5 Developer Runtime cuando está instalado en todas las versiones compatibles de los servidores Microsoft Windows  
(2847559)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
Nota para MS13-052

Vea también las demás categorías de esta sección, Ubicaciones de descarga y software afectado, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

Notas para MS13-054

<sup>[1]</sup>Esta actualización solo está disponible en el Centro de descarga de Microsoft.

Vea también las demás categorías de esta sección, Ubicaciones de descarga y software afectado, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Software y plataformas de comunicaciones de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Lync
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-054](http://go.microsoft.com/fwlink/?linkid=301531)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync 2010 (32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Lync 2010 (32 bits)  
(2843160)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Lync 2010 (64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Lync 2010 (64 bits)  
(2843160)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync 2010 Attendee  
(instalación de nivel de usuario)
</td>
<td style="border:1px solid black;">
Microsoft Lync 2010 Attendee  
(instalación de nivel de usuario)  
(2843162)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Lync 2010 Attendee  
(instalación de nivel de administración)
</td>
<td style="border:1px solid black;">
Microsoft Lync 2010 Attendee  
(instalación de nivel de administración)  
(2843163)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync 2013 (32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Lync 2013 (32 bits)  
(2817465)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Lync Basic 2013 (32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Lync Basic 2013 (32 bits)  
(2817465)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Lync 2013 (64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Lync 2013 (64 bits)  
(2817465)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Lync Basic 2013 (64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Lync Basic 2013 (64 bits)  
(2817465)  
(Crítica)
</td>
</tr>
</table>
 
Nota para MS13-054

Vea también las demás categorías de esta sección, Ubicaciones de descarga y software afectado, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software

#### Software de seguridad de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Software antispyware
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-058](http://go.microsoft.com/fwlink/?linkid=308992)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Defender para Windows 7 (x86)
</td>
<td style="border:1px solid black;">
Windows Defender para Windows 7 (x86)   
(2847927)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Defender para Windows 7 (x64)
</td>
<td style="border:1px solid black;">
Windows Defender para Windows 7 (x64)   
(2847927)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Defender cuando está instalado en Windows Server 2008 R2 (x64)
</td>
<td style="border:1px solid black;">
Windows Defender cuando está instalado en Windows Server 2008 R2 (x64)   
(2847927)  
(Importante)
</td>
</tr>
</table>
 

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

Central de seguridad

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/bb245732). [TechNet Security TechCenter](http://technet.microsoft.com/es-es/security/default.aspx) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar el [Centro de seguridad y protección de Microsoft](http://go.microsoft.com/fwlink/?linkid=85102), donde esta información también está disponible haciendo clic en "Actualizaciones de seguridad".

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Para clientes de Microsoft Office para Mac, Microsoft AutoUpdate para Mac puede servir de ayuda para mantener actualizado el software de Microsoft. Para obtener más información acerca del uso de Microsoft AutoUpdate para Mac, vea [Buscar actualizaciones de software automáticamente](http://mac2.microsoft.com/help/office/14/en-us/word/item/ffe35357-8f25-4df8-a0a3-c258526c64ea).

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS13-001"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

Consejos para la detección y la implementación

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747).

Microsoft Baseline Security Analyzer

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, vea [Microsoft Baseline Security Analyzer](http://go.microsoft.com/fwlink/?linkid=21134).

Windows Server Update Services

Windows Server Update Services (WSUS) permite a los administradores implementar de un modo rápido y confiable las actualizaciones críticas y de seguridad más recientes en sistemas operativos Microsoft Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://technet.microsoft.com/wsus/default).

System Center Configuration Manager

La administración de actualizaciones de software de System Center Configuration Manager simplifica la tarea compleja de entregar y administrar actualizaciones para los sistemas de TI en toda la empresa. Con System Center Configuration Manager, los administradores de TI pueden ofrecer actualizaciones de los productos de Microsoft a una serie de dispositivos, incluidos equipos de escritorio, portátiles, servidores y dispositivos móviles.

La evaluación automática de vulnerabilidades en System Center Configuration Manager detecta las necesidades de actualizaciones e informa de las acciones recomendadas. La administración de actualizaciones de software en System Center Configuration Manager se basa en Microsoft Windows Software Update Services (WSUS), una infraestructura de actualizaciones probada con la que están familiarizados los administradores de TI de todo el mundo. Para obtener más información acerca de System Center Configuration Manager, vea [Recursos técnicos de System Center](http://technet.microsoft.com/systemcenter/bb980621).

Systems Management Server 2003

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales.

Nota System Management Server 2003 está fuera del soporte técnico general desde el 12 de enero de 2010. Para obtener más información acerca de los ciclos de vida de los productos, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742). Ya está disponible la siguiente versión de SMS, System Center Configuration Manager; vea la sección anterior, System Center Configuration Manager.

Para obtener más información acerca de cómo los administradores pueden usar SMS 2003 para implementar actualizaciones de seguridad, vea [Escenarios y procedimientos para Microsoft Systems Management Server 2003: Administración de distribución de software y revisiones](http://www.microsoft.com/downloads/details.aspx?familyid=32f2bb4c-42f8-4b8d-844f-2553fd78049f). Para obtener información acerca de SMS, visite [Microsoft Systems Management Server TechCenter](http://technet.microsoft.com/systemcenter/bb545936).

Nota SMS utiliza las herramientas Microsoft Baseline Security Analyzer para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://www.microsoft.com/downloads/en/details.aspx?familyid=7bd3a16e-1899-4e0b-bb99-1320e816167d)) para instalar estas actualizaciones.

Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones

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

Estrategias de administración de actualizaciones

En [Orientación de seguridad para la administración de actualizaciones](http://go.microsoft.com/fwlink/?linkid=21168) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

Obtención de otras actualizaciones de seguridad

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](http://support.microsoft.com/kb/913086).

Comunidad de seguridad para profesionales de tecnologías de la información

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [Comunidad de profesionales de TI de seguridad](http://go.microsoft.com/fwlink/?linkid=21164).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

MS13-052

-   Ling Chuan Lee y Lee Yee Chan, de [F-13 Laboratory](http://www.f13-labs.net/), por informar de la vulnerabilidad de análisis de fuentes TrueType (CVE-2013-3129)
-   Alon Fliess, por informar de la vulnerabilidad de infracción de acceso a matriz (CVE-2013-3131)
-   James Forshaw, de [Context Information Security](http://www.contextis.com/), por informar de la vulnerabilidad de omisión de reflejo de delegación (CVE-2013-3132)
-   James Forshaw, de [Context Information Security](http://www.contextis.com/), por informar de la vulnerabilidad de inserción de métodos anónimos (CVE-2013-3133)
-   James Forshaw, de [Context Information Security](http://www.contextis.com/), por informar de la vulnerabilidad de serialización de delegación (CVE-2013-3171)
-   Vitaliy Toropov, por informar de la vulnerabilidad de puntero nulo (CVE-2013-3178)

MS13-053

-   Jon Butler y Nils, de MWR Labs, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de asignación de memoria en Win32k (CVE-2013-1300)
-   Alexander Chizhov, de [Dr.Web](http://drweb.com/), por informar de la vulnerabilidad de anulación de referencia en Win32k (CVE-2013-1340)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de identificador de ventana en Win32k (CVE-2013-1345)
-   Ling Chuan Lee y Lee Yee Chan, de [F13 Laboratory](http://www.f13-labs.net/), por informar de la vulnerabilidad de análisis de fuentes TrueType (CVE-2013-3129)
-   Yinliang, de [Tencent PC Manager](http://guanjia.qq.com), por informar de la vulnerabilidad de divulgación de información en Win32k (CVE-2013-3167)
-   [Mateusz "j00ru" Jurczyk](http://j00ru.vexillium.org/)
-   , de
-   [Google Inc](http://www.google.com/)
-   , por informar de la vulnerabilidad de desbordamiento del búfer en Win32k (CVE-2013-3172)
-   Wen Yujie y Guo Pengfei de [Qihoo 360 Security Center](http://www.360.cn/) por informar de la vulnerabilidad de daños de sobrescritura de búfer en Win32k (CVE-2013-3173)

MS13-054

-   Ling Chuan Lee y Lee Yee Chan, de [F13 Laboratory](http://www.f13-labs.net/), por informar de la vulnerabilidad de análisis de fuentes TrueType (CVE-2013-3129)

MS13-055

-   Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3115)
-   SkyLined, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3143)
-   Simon Zuckerbraun, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3144)
-   Toan Pham Van, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3145)
-   Toan Pham Van, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3146)
-   [Aniway.Anyway@gmail.com](mailto:aniway.anyway@gmail.com)
-   , en colaboración con
-   [Zero Day Initiative](http://www.zerodayinitiative.com/)
-   de
-   [HP](http://www.hpenterprisesecurity.com/products)
-   , por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3147)
-   Bluesea, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3148)
-   Bluesea, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3149)
-   [Omair](http://krash.in/)
-   , en colaboración con
-   [Zero Day Initiative](http://www.zerodayinitiative.com/)
-   de
-   [HP](http://www.hpenterprisesecurity.com/products)
-   , por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3150)
-   Toan Pham Van, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3151)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3152)
-   e6af8de8b1d4b2b6d5ba2610cbf9cd38, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3153)
-   Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3161)
-   Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3162)
-   José Antonio Vázquez González, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3163)
-   Scott Bell, de [Security-Assessment.com](http://www.security-assessment.com/), por informar de la vulnerabilidad en la memoria de Internet Explorer (CVE-2013-3164)
-   Masato Kinugawa, por informar de la vulnerabilidad de codificación de caracteres Shift JIS (CVE-2013-3166)
-   Mark Yason, de IBM X-Force, por colaborar con nosotros en un cambio de defensa en profundidad incluido en este boletín (CVE-2013-4015)

MS13-056

-   Andrés Gómez Ramírez, por informar de la vulnerabilidad de sobrescritura de memoria arbitraria en DirectShow (CVE-2013-3174)

MS13-057

-   A in investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de ejecución remota de código en el descodificador de vídeo WMV (CVE-2013-3127)

MS13-058

-   Alton Blom, de [Reserve Bank of Australia](http://www.rba.gov.au/), por informar de la vulnerabilidad de nombre de ruta de acceso incorrecto en Microsoft Windows 7 Defender (CVE-2013-3154)

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Soluciones de seguridad para profesionales de TI: [Soporte técnico y solución de problemas de seguridad de TechNet](http://technet.microsoft.com/es-es/security/bb980617)
-   Ayuda para proteger su equipo con Windows de virus y malware: [Solución antivirus y centro de seguridad](http://support.microsoft.com/contactus/cu_sc_virsec_master)
-   Soporte local según su país: [Soporte internacional](http://support.microsoft.com/common/international.aspx)

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (9 de julio de 2013): Publicación del resumen del boletín.
-   V1.1 (9 de julio de 2013): para MS13-055, se ha revisado la evaluación de explotabilidad en Índice de explotabilidad para CVE-2013-3163. Microsoft tiene constancia de ataques dirigidos que intentan aprovechar esta vulnerabilidad a través de Internet Explorer 8. Se trata únicamente de un cambio informativo.
-   V2.0 (13 de agosto de 2013): para MS13-052, se ha revisado el boletín para publicar de nuevo las actualizaciones 2840628, 2840632, 2840642, 2844285, 2844286, 2844287 y 2844289. Para MS13-057, se ha revisado el boletín para publicar de nuevo la actualización 2803821 para Windows 7 y Windows 2008 R2. Los clientes deben instalar las actualizaciones publicadas de nuevo que se apliquen a sus sistemas. Vea los boletines correspondientes para obtener detalles.
-   V3.0 (27 de agosto de 2013): para MS13-057, el boletín se revisó para volver a publicar la actualización de seguridad 2803821 para Windows XP, Windows Server 2003, Windows Vista y Windows Server 2008; la actualización de seguridad 2834902 para Windows XP y Windows Server 2003; la actualización de seguridad 2834903 para Windows XP; la actualización de seguridad 2834904 para Windows XP y Windows Server 2003; y la actualización de seguridad 2834905 para Windows XP. Los clientes de Windows XP, Windows Server 2003, Windows Vista y Windows Server 2008 deben instalar las actualizaciones que se han vuelto a publicar que se apliquen a sus sistemas. Consulte el boletín para obtener detalles.

*Built at 2014-04-18T01:50:00Z-07:00*
