---
TOCTitle: 'MS12-JUL'
Title: Resumen del boletín de seguridad de Microsoft de julio 2012
ms:assetid: 'ms12-jul'
ms:contentKeyID: 61225437
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms12-jul(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de julio 2012
===========================================================

Publicado: martes, 10 de julio de 2012 | Actualizado: miércoles, 12 de diciembre de 2012

**Versión:** 5.1

Este resumen del boletín enumera los boletines de seguridad publicados para julio de 2012.

Con la publicación de los boletines de seguridad de julio de 2012, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 5 de julio de 2012. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 11 de julio de 2012, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de julio](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032518600). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, vea los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217214).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información** **adicional**.

### Información del boletín

Resúmenes ejecutivos
--------------------

En la tabla siguiente se resumen los boletines de seguridad de este mes por orden de gravedad.

Para obtener detalles acerca del software afectado, vea la siguiente sección, **Ubicaciones** **de descarga y software afectado**.

 
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=254824"><strong>MS12-043</strong></a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft XML</strong> <strong>CoreServices</strong> <strong>podría permitir la ejecución remota de código (2722479)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública en Microsoft XML Core Services. La vulnerabilidad podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. El atacante no podría obligar a los usuarios a visitar dicho sitio web. Por lo tanto, tendría que atraerlos al sitio web; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger que lleve a los usuarios al sitio web del atacante.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Microsoft Office,<br />
Herramientas de desarrollo de Microsoft,<br />
Software de servidor de Microsoft</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=254377"><strong>MS12-044</strong></a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (2719177)</strong> <br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. Un intruso que aprovechara cualquiera de estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=254441"><strong>MS12-045</strong></a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Data Access</strong> <strong>Components</strong> <strong>podría permitir la ejecución remota de código (2698365)</strong> <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. Esta vulnerabilidad podría permitir la ejecución remota de código si un usuario visualiza una página web especialmente diseñada. Un atacante que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=252510"><strong>MS12-046</strong></a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Visual Basic para Aplicaciones podría permitir la ejecución remota de código (2707960)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública en Microsoft Visual Basic para Aplicaciones. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo legítimo de Microsoft Office (como un archivo .docx) que se encuentre en el mismo directorio que un archivo de biblioteca de vínculos dinámicos (DLL) especialmente diseñado. De esta forma, el atacante podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Si un usuario inicia sesión con derechos de usuario administrativos, un atacante podría lograr el control completo del sistema afectado. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office,<br />
Herramientas de desarrollo de Microsoft</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=254380"><strong>MS12-047</strong></a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en los controladores modo</strong> <strong>kernel</strong> <strong>de Windows</strong> <strong>podrían</strong> <strong>permitir la elevación de privilegios (2718523)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y otra vulnerabilidad de las que se ha informado de forma privada en Microsoft Windows. Las vulnerabilidades podrían permitir la elevación de privilegios si un atacante inicia sesión en el sistema y ejecuta una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=239507"><strong>MS12-048</strong></a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el</strong> <strong>shell</strong> <strong>de Windows podría permitir la ejecución remota de código (2691442)</strong> <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo o un directorio con un nombre especialmente diseñado. Un atacante que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=251035"><strong>MS12-049</strong></a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en TLS podría permitir la divulgación de información (2655992)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad que se ha divulgado públicamente en TLS. La vulnerabilidad podría permitir la divulgación de información si un atacante intercepta tráfico web cifrado que se sirva desde un sistema afectado. Todos los conjuntos de programas de cifrado que no usan el modo CBC no están afectados.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Divulgación de información</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=251611"><strong>MS12-050</strong></a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en SharePoint</strong> <strong>podrían</strong> <strong>permitir</strong> <strong>la elevación de privilegios (2695502)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y cinco vulnerabilidades de las que se ha informado de forma privada en Microsoft SharePoint y Windows SharePoint Services. Las vulnerabilidades más graves podrían permitir la elevación de privilegios si un usuario hace clic en una dirección URL especialmente diseñada que lo dirige a un sitio de SharePoint atacado.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office,<br />
Software de servidor de Microsoft</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=255000"><strong>MS12-051</strong></a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Office para Mac podría permitir la elevación de privilegios (2721015)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública en Microsoft Office para Mac. La vulnerabilidad podría permitir la elevación de privilegios si un ejecutable malintencionado se guarda en un sistema afectado por un atacante y otro usuario inicia sesión posteriormente y ejecuta el archivo ejecutable malintencionado. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">No requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y, a continuación, por identificador de CVE. Sólo se incluyen las vulnerabilidades que tiene una clasificación de gravedad de crítica o importante en los boletines.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de las vulnerabilidades de ejecución de código y de denegación de servicio en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Revise cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación de las actualizaciones de este mes. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/security/cc998259.aspx).
  
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=254824"><strong>MS12-043</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria no inicializada en MSXML</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1889">CVE-2012-1889</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.<br />
<br />
Microsoft es consciente de ataques limitados y dirigidos que intentan aprovechar esta vulnerabilidad.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=254377"><strong>MS12-044</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código en objetos almacenados en caché</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1522">CVE-2012-1522</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=254377"><strong>MS12-044</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código en eliminación de atributos</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1524">CVE-2012-1524</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=254441"><strong>MS12-045</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código de desbordamiento del montón de Cachesize de ADO</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1891">CVE-2012-1891</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=252510"><strong>MS12-046</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de carga de bibliotecas no seguras en Visual Basic para Aplicaciones</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1854">CVE-2012-1854</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.<br />
<br />
Microsoft es consciente de ataques limitados y dirigidos que intentan aprovechar esta vulnerabilidad.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=254380"><strong>MS12-047</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de distribución de teclado</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1890">CVE-2012-1890</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=254380"><strong>MS12-047</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de control de tipo incorrecto en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1893">CVE-2012-1893</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=239507"><strong>MS12-048</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de inserción de comandos</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-0175">CVE-2012-0175</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=251035"><strong>MS12-049</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de protocolo TLS</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1870">CVE-2012-1870</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.<br />
<br />
Esta vulnerabilidad afecta a la divulgación de información.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=251611"><strong>MS12-050</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de saneamiento de HTML</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1858">CVE-2012-1858</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.<br />
<br />
Esta vulnerabilidad afecta a la divulgación de información.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=251611"><strong>MS12-050</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de scriptresx.ashx de XSS</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1859">CVE-2012-1859</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=251611"><strong>MS12-050</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de script en nombre de usuario en SharePoint</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1861">CVE-2012-1861</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=251611"><strong>MS12-050</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de parámetro de lista reflejada en SharePoint</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1863">CVE-2012-1863</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=255000"><strong>MS12-051</strong></a></td>
<td style="border:1px solid black;">Vulnerabilidad de permisos de carpeta incorrectos en Office para Mac</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1894">CVE-2012-1894</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.</td>
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
<th colspan="7" style="border:1px solid black;">
Windows XP  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-043**](http://go.microsoft.com/fwlink/?linkid=254824)
</td>
<td style="border:1px solid black;">
[**MS12-044**](http://go.microsoft.com/fwlink/?linkid=254377)
</td>
<td style="border:1px solid black;">
[**MS12-045**](http://go.microsoft.com/fwlink/?linkid=254441)
</td>
<td style="border:1px solid black;">
[**MS12-047**](http://go.microsoft.com/fwlink/?linkid=254380)
</td>
<td style="border:1px solid black;">
[**MS12-048**](http://go.microsoft.com/fwlink/?linkid=239507)
</td>
<td style="border:1px solid black;">
[**MS12-049**](http://go.microsoft.com/fwlink/?linkid=251035)
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
Ninguna
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
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=017f1ed7-eed4-4de3-aca1-93fb25058866)  
(KB2719985)  
(Crítica)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c34c2511-84d4-4f7e-b61a-086e6ee26ffa)  
(KB2721691)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=017f1ed7-eed4-4de3-aca1-93fb25058866)  
(KB2719985)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Data Access Components 2.8 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=496e93ac-fcce-458f-839b-25ff1ab22fde)  
(KB2698365)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=a4bc78fb-3927-4059-ae1c-35c369e39203)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=405ce29a-7c97-44de-aed9-4c90cbdaaf1b)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=8324496f-aca4-4a86-833d-c22341e71cd3)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=d27bd5e9-a3a6-411e-bc50-2b03d64fb50c)  
(KB2719985)  
(Crítica)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=91fcc9f2-86ad-47e9-b298-91d74f852c19)  
(KB2721691)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=aaf10833-0487-4026-805b-97543140b1fd)  
(KB2721693)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Data Access Components 2.8 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=64f8d1a4-4a9d-4ee0-8a66-d157d516afb5)  
(KB2698365)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=94029b68-5b7b-4d0e-b175-cfc2b0eba91a)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=36fc4c85-fa93-4c6b-b93a-94460e9ba23b)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5f268365-9c18-4fc7-b11e-b1f19c4a5a2a)  
(KB2655992)  
(Importante)
</td>
</tr>
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
[**MS12-043**](http://go.microsoft.com/fwlink/?linkid=254824)
</td>
<td style="border:1px solid black;">
[**MS12-044**](http://go.microsoft.com/fwlink/?linkid=254377)
</td>
<td style="border:1px solid black;">
[**MS12-045**](http://go.microsoft.com/fwlink/?linkid=254441)
</td>
<td style="border:1px solid black;">
[**MS12-047**](http://go.microsoft.com/fwlink/?linkid=254380)
</td>
<td style="border:1px solid black;">
[**MS12-048**](http://go.microsoft.com/fwlink/?linkid=239507)
</td>
<td style="border:1px solid black;">
[**MS12-049**](http://go.microsoft.com/fwlink/?linkid=251035)
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
Ninguna
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=b7321c17-0e8e-4217-8da6-4c270dbfc802)  
(KB2719985)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c34c2511-84d4-4f7e-b61a-086e6ee26ffa)  
(KB2721691)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=3b56ba48-b74c-4681-8e17-715dc5d45e2c)  
(KB2721693)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Data Access Components 2.8 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=465ef3d0-df59-4f73-a06d-49a81286c01f)  
(KB2698365)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d53bd571-ad30-41c7-8c5f-f217097770f5)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1f058336-4a6a-47d0-ad6f-276dc381d1db)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b13e2388-01f3-46bf-97b4-612e2778477a)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=2b24d755-f96f-47d6-b286-2bfd4e278dcc)  
(KB2719985)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=91fcc9f2-86ad-47e9-b298-91d74f852c19)  
(KB2721691)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=aaf10833-0487-4026-805b-97543140b1fd)  
(KB2721693)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Data Access Components 2.8 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d1955b23-5931-4891-9c11-401efcb6c05c)  
(KB2698365)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5f261883-daec-4af3-8bc1-46da9c164de7)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5b6d6227-8695-4ecb-86e1-bb264f954898)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a0bd0591-62f8-40d1-93fa-7f0afc4fc09c)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=eab0f4c6-3f2e-435d-aef7-d9230295ab15)  
(KB2719985)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=77f45630-288e-46dd-8cb7-c59b07a4bde4)  
(KB2721691)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=68eb373e-2c1e-40db-8ad0-0a369a96255b)  
(KB2721693)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Data Access Components 2.8 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e46047d5-9a2d-48c4-b1c8-3db884c25b5c)  
(KB2698365)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=60c57c8b-6d56-42de-ab1e-e4e3258c7818)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=563399b3-cb19-40e9-ba9d-0079032c8cee)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=b91df558-5446-4858-92af-50cfbab27ff5)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-043**](http://go.microsoft.com/fwlink/?linkid=254824)
</td>
<td style="border:1px solid black;">
[**MS12-044**](http://go.microsoft.com/fwlink/?linkid=254377)
</td>
<td style="border:1px solid black;">
[**MS12-045**](http://go.microsoft.com/fwlink/?linkid=254441)
</td>
<td style="border:1px solid black;">
[**MS12-047**](http://go.microsoft.com/fwlink/?linkid=254380)
</td>
<td style="border:1px solid black;">
[**MS12-048**](http://go.microsoft.com/fwlink/?linkid=239507)
</td>
<td style="border:1px solid black;">
[**MS12-049**](http://go.microsoft.com/fwlink/?linkid=251035)
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
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=f8ccdb90-66bd-471a-9c78-825d1140b5ac)  
(KB2719985)  
(Crítica)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c34c2511-84d4-4f7e-b61a-086e6ee26ffa)  
(KB2721691)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=f8ccdb90-66bd-471a-9c78-825d1140b5ac)  
(KB2719985)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=b6a75978-0c11-49fb-8aa7-c47efb3bf4e8)  
(KB2719177)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Data Access Components 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=0c43c093-296e-4e12-b995-4f9e3f00cbe0)  
(KB2698365)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3c957f8a-8f32-4a12-ade9-10a7e2984e88)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2e9a4aeb-3f34-483c-ba3a-3141164e9e8a)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7286a6e2-9c31-493f-aae3-776f72e85503)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=e8553934-a202-4033-b9c5-27bc4207469d)  
(KB2719985)  
(Crítica)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=91fcc9f2-86ad-47e9-b298-91d74f852c19)  
(KB2721691)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=e8553934-a202-4033-b9c5-27bc4207469d)  
(KB2719985)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=8470af29-68e2-4fd2-bc30-3c9188e65c59)  
(KB2719177)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Data Access Components 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=4d9b91c9-a412-4344-b934-0d2fbd9526fd)  
(KB2698365)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7300636f-aefd-46bf-a7ba-780d6f939b4f)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=fe8467e2-8b37-4ec2-ba9f-324918f1f045)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c62ec513-887c-4a42-a3cc-3e92631526ed)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-043**](http://go.microsoft.com/fwlink/?linkid=254824)
</td>
<td style="border:1px solid black;">
[**MS12-044**](http://go.microsoft.com/fwlink/?linkid=254377)
</td>
<td style="border:1px solid black;">
[**MS12-045**](http://go.microsoft.com/fwlink/?linkid=254441)
</td>
<td style="border:1px solid black;">
[**MS12-047**](http://go.microsoft.com/fwlink/?linkid=254380)
</td>
<td style="border:1px solid black;">
[**MS12-048**](http://go.microsoft.com/fwlink/?linkid=239507)
</td>
<td style="border:1px solid black;">
[**MS12-049**](http://go.microsoft.com/fwlink/?linkid=251035)
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
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=42a869b9-085a-450a-b69e-f634d01075dd)  
(KB2719985)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c34c2511-84d4-4f7e-b61a-086e6ee26ffa)  
(KB2721691)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=42a869b9-085a-450a-b69e-f634d01075dd)  
(KB2719985)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=4009dd66-b6d0-4c14-acde-f52d75d8f9d1)  
(KB2719177)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Data Access Components 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=a8ed6a19-c128-46e5-ae38-5fa9f843ba0d)  
(KB2698365)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ed201422-7c65-4c20-a825-8cecab1aeebc)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6d873c5a-57dc-4792-942e-124ce1a4ec2b)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=97030267-6b19-46ae-84ce-0bb1f91ab951)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7b2d780-cc92-4f3e-b5a2-9f2ac66b6f1c)  
(KB2719985)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=91fcc9f2-86ad-47e9-b298-91d74f852c19)  
(KB2721691)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7b2d780-cc92-4f3e-b5a2-9f2ac66b6f1c)  
(KB2719985)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=b609981c-fda8-4085-ae8d-5b760ad4e73f)  
(KB2719177)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Data Access Components 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=043464e4-9572-419b-a03a-ca11bf918052)  
(KB2698365)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8e1a27c9-6495-4030-8a46-264afd78a5a1)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d49e3e7e-910a-4069-b0b0-0987bb9fdde2)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8a5f6e84-5e5b-42c3-a5b7-65defdb0665f)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=359a86d6-e94a-4de5-83d9-6b0273115bff)  
(KB2719985)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=77f45630-288e-46dd-8cb7-c59b07a4bde4)  
(KB2721691)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=359a86d6-e94a-4de5-83d9-6b0273115bff)  
(KB2719985)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Data Access Components 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=00638d5e-6156-4c1b-a131-3d1fff514bdb)  
(KB2698365)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=76f640b8-5aab-4880-9d74-22e2a5086342)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ca890b4d-124f-4293-b8d0-69f6302b5189)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e886c5f4-7f38-4c90-905b-a682e6a8ffd0)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows 7
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-043**](http://go.microsoft.com/fwlink/?linkid=254824)
</td>
<td style="border:1px solid black;">
[**MS12-044**](http://go.microsoft.com/fwlink/?linkid=254377)
</td>
<td style="border:1px solid black;">
[**MS12-045**](http://go.microsoft.com/fwlink/?linkid=254441)
</td>
<td style="border:1px solid black;">
[**MS12-047**](http://go.microsoft.com/fwlink/?linkid=254380)
</td>
<td style="border:1px solid black;">
[**MS12-048**](http://go.microsoft.com/fwlink/?linkid=239507)
</td>
<td style="border:1px solid black;">
[**MS12-049**](http://go.microsoft.com/fwlink/?linkid=251035)
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=d8a4817c-481c-4ed2-980a-21623f0ca6d2)  
(KB2719985)  
(Crítica)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c34c2511-84d4-4f7e-b61a-086e6ee26ffa)  
(KB2721691)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=d8a4817c-481c-4ed2-980a-21623f0ca6d2)  
(KB2719985)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=0be922a4-6b8a-4017-bc31-1cadd8cdb472)  
(KB2719177)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Data Access Components 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=ed997ae7-2e45-4620-bcbe-a5006aaca448)  
(KB2698365)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=b4bed780-b120-43a1-900e-89b3be7da8b1)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=8ab3eadf-9437-4323-8323-87dfd23245fd)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=da706b4e-7c22-4929-96d3-f8b0fa10f043)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=d8a4817c-481c-4ed2-980a-21623f0ca6d2)  
(KB2719985)  
(Crítica)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c34c2511-84d4-4f7e-b61a-086e6ee26ffa)  
(KB2721691)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=d8a4817c-481c-4ed2-980a-21623f0ca6d2)  
(KB2719985)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=0be922a4-6b8a-4017-bc31-1cadd8cdb472)  
(KB2719177)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Data Access Components 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=ed997ae7-2e45-4620-bcbe-a5006aaca448)  
(KB2698365)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b4bed780-b120-43a1-900e-89b3be7da8b1)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=8ab3eadf-9437-4323-8323-87dfd23245fd)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=da706b4e-7c22-4929-96d3-f8b0fa10f043)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas x64
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=e1962879-1725-4d60-933f-eb351bee56bc)  
(KB2719985)  
(Crítica)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=91fcc9f2-86ad-47e9-b298-91d74f852c19)  
(KB2721691)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=e1962879-1725-4d60-933f-eb351bee56bc)  
(KB2719985)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=739e4f24-8433-4dc9-a106-a70ae4040606)  
(KB2719177)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Data Access Components 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=4040c290-bf41-4e14-8269-da95ee06d8e7)  
(KB2698365)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=3efb0de1-252b-4b72-86f3-e747f8fa2229)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=f518f273-b3b9-4cbf-b820-05a1adc79342)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=07518fb7-031f-4fa0-836c-8f33c247868b)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=e1962879-1725-4d60-933f-eb351bee56bc)  
(KB2719985)  
(Crítica)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=91fcc9f2-86ad-47e9-b298-91d74f852c19)  
(KB2721691)  
(Crítica)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=e1962879-1725-4d60-933f-eb351bee56bc)  
(KB2719985)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=739e4f24-8433-4dc9-a106-a70ae4040606)  
(KB2719177)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Data Access Components 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=4040c290-bf41-4e14-8269-da95ee06d8e7)  
(KB2698365)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=3efb0de1-252b-4b72-86f3-e747f8fa2229)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=f518f273-b3b9-4cbf-b820-05a1adc79342)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=07518fb7-031f-4fa0-836c-8f33c247868b)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Server 2008 R2
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-043**](http://go.microsoft.com/fwlink/?linkid=254824)
</td>
<td style="border:1px solid black;">
[**MS12-044**](http://go.microsoft.com/fwlink/?linkid=254377)
</td>
<td style="border:1px solid black;">
[**MS12-045**](http://go.microsoft.com/fwlink/?linkid=254441)
</td>
<td style="border:1px solid black;">
[**MS12-047**](http://go.microsoft.com/fwlink/?linkid=254380)
</td>
<td style="border:1px solid black;">
[**MS12-048**](http://go.microsoft.com/fwlink/?linkid=239507)
</td>
<td style="border:1px solid black;">
[**MS12-049**](http://go.microsoft.com/fwlink/?linkid=251035)
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=f75a3d2d-8322-40a6-b735-faeb8b4873b6)  
(KB2719985)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=91fcc9f2-86ad-47e9-b298-91d74f852c19)  
(KB2721691)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=f75a3d2d-8322-40a6-b735-faeb8b4873b6)  
(KB2719985)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=91e8ecf8-4f6d-4e86-bc6b-617749090190)  
(KB2719177)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Data Access Components 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=e749883d-221a-411a-9c85-759d50cefa9d)  
(KB2698365)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=73a9ff32-4009-4fd4-a82b-1e22c09d3087)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=d16fa6b9-43aa-4d0f-a230-52664e972ab9)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=c9ef728f-abef-4076-bb13-7488af471aa4)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=f75a3d2d-8322-40a6-b735-faeb8b4873b6)  
(KB2719985)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=91fcc9f2-86ad-47e9-b298-91d74f852c19)  
(KB2721691)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=f75a3d2d-8322-40a6-b735-faeb8b4873b6)  
(KB2719985)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=91e8ecf8-4f6d-4e86-bc6b-617749090190)  
(KB2719177)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Data Access Components 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=e749883d-221a-411a-9c85-759d50cefa9d)  
(KB2698365)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=73a9ff32-4009-4fd4-a82b-1e22c09d3087)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d16fa6b9-43aa-4d0f-a230-52664e972ab9)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=c9ef728f-abef-4076-bb13-7488af471aa4)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=a745388e-9fef-412e-8d00-9195af506cf5)  
(KB2719985)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=77f45630-288e-46dd-8cb7-c59b07a4bde4)  
(KB2721691)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=a745388e-9fef-412e-8d00-9195af506cf5)  
(KB2719985)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Data Access Components 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=eeab7dbb-f6ca-44bd-a172-c07fc5803fd6)  
(KB2698365)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=772f2975-065d-44f3-adf8-82188bd43196)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=c9c3b471-4a81-4a44-93ad-674650454c53)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=49e182b5-4499-42a1-8180-9bb920e154cb)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=a745388e-9fef-412e-8d00-9195af506cf5)  
(KB2719985)  
(Moderada)  
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=77f45630-288e-46dd-8cb7-c59b07a4bde4)  
(KB2721691)  
(Moderada)  
[Microsoft XML Core Services 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=a745388e-9fef-412e-8d00-9195af506cf5)  
(KB2719985)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Data Access Components 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=eeab7dbb-f6ca-44bd-a172-c07fc5803fd6)  
(KB2698365)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=772f2975-065d-44f3-adf8-82188bd43196)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=c9c3b471-4a81-4a44-93ad-674650454c53)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=49e182b5-4499-42a1-8180-9bb920e154cb)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows 8
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-043**](http://go.microsoft.com/fwlink/?linkid=254824)
</td>
<td style="border:1px solid black;">
[**MS12-044**](http://go.microsoft.com/fwlink/?linkid=254377)
</td>
<td style="border:1px solid black;">
[**MS12-045**](http://go.microsoft.com/fwlink/?linkid=254441)
</td>
<td style="border:1px solid black;">
[**MS12-047**](http://go.microsoft.com/fwlink/?linkid=254380)
</td>
<td style="border:1px solid black;">
[**MS12-048**](http://go.microsoft.com/fwlink/?linkid=239507)
</td>
<td style="border:1px solid black;">
[**MS12-049**](http://go.microsoft.com/fwlink/?linkid=251035)
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
Ninguna
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
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c34c2511-84d4-4f7e-b61a-086e6ee26ffa)  
(KB2721691)  
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
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 8 para sistemas de 64 bits
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=91fcc9f2-86ad-47e9-b298-91d74f852c19)  
(KB2721691)  
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
<th colspan="7" style="border:1px solid black;">
Windows Server 2012
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-043**](http://go.microsoft.com/fwlink/?linkid=254824)
</td>
<td style="border:1px solid black;">
[**MS12-044**](http://go.microsoft.com/fwlink/?linkid=254377)
</td>
<td style="border:1px solid black;">
[**MS12-045**](http://go.microsoft.com/fwlink/?linkid=254441)
</td>
<td style="border:1px solid black;">
[**MS12-047**](http://go.microsoft.com/fwlink/?linkid=254380)
</td>
<td style="border:1px solid black;">
[**MS12-048**](http://go.microsoft.com/fwlink/?linkid=239507)
</td>
<td style="border:1px solid black;">
[**MS12-049**](http://go.microsoft.com/fwlink/?linkid=251035)
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
Ninguna
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
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=91fcc9f2-86ad-47e9-b298-91d74f852c19)  
(KB2721691)  
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
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Opción de instalación Server Core
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador** **del** **boletín**
</td>
<td style="border:1px solid black;">
[**MS12-043**](http://go.microsoft.com/fwlink/?linkid=254824)
</td>
<td style="border:1px solid black;">
[**MS12-044**](http://go.microsoft.com/fwlink/?linkid=254377)
</td>
<td style="border:1px solid black;">
[**MS12-045**](http://go.microsoft.com/fwlink/?linkid=254441)
</td>
<td style="border:1px solid black;">
[**MS12-047**](http://go.microsoft.com/fwlink/?linkid=254380)
</td>
<td style="border:1px solid black;">
[**MS12-048**](http://go.microsoft.com/fwlink/?linkid=239507)
</td>
<td style="border:1px solid black;">
[**MS12-049**](http://go.microsoft.com/fwlink/?linkid=251035)
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
Ninguna
</td>
<td style="border:1px solid black;">
Ninguna
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
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ed201422-7c65-4c20-a825-8cecab1aeebc)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6d873c5a-57dc-4792-942e-124ce1a4ec2b)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=97030267-6b19-46ae-84ce-0bb1f91ab951)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr>
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
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8e1a27c9-6495-4030-8a46-264afd78a5a1)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d49e3e7e-910a-4069-b0b0-0987bb9fdde2)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8a5f6e84-5e5b-42c3-a5b7-65defdb0665f)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64
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
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=73a9ff32-4009-4fd4-a82b-1e22c09d3087)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=d16fa6b9-43aa-4d0f-a230-52664e972ab9)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=c9ef728f-abef-4076-bb13-7488af471aa4)  
(KB2655992)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
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
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=73a9ff32-4009-4fd4-a82b-1e22c09d3087)  
(KB2718523)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d16fa6b9-43aa-4d0f-a230-52664e972ab9)  
(KB2691442)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=c9ef728f-abef-4076-bb13-7488af471aa4)  
(KB2655992)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS12-043**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="5" style="border:1px solid black;">
Conjuntos de programas y componentes de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador** **del** **boletín**
</td>
<td style="border:1px solid black;">
[**MS12-043**](http://go.microsoft.com/fwlink/?linkid=254824)
</td>
<td style="border:1px solid black;">
[**MS12-046**](http://go.microsoft.com/fwlink/?linkid=252510)
</td>
<td style="border:1px solid black;">
[**MS12-050**](http://go.microsoft.com/fwlink/?linkid=251611)
</td>
<td style="border:1px solid black;">
[**MS12-051**](http://go.microsoft.com/fwlink/?linkid=255000)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Microsoft Office 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=c4c925b8-df99-4d4f-b939-878d77d64514)  
(KB2687627)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=d49c4893-d867-4d16-90f5-354eb4757d90)<sup>[1]</sup>
(KB2687626)  
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
Microsoft Office 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=b45f5c9a-d601-4192-92c3-064e9b94785a)  
(KB2596856)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=181bbd45-9128-4c26-af1e-fadfd83ff756)<sup>[1]</sup>
(KB2596744)  
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
Microsoft Office 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=b45f5c9a-d601-4192-92c3-064e9b94785a)  
(KB2596856)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2007 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=181bbd45-9128-4c26-af1e-fadfd83ff756)<sup>[1]</sup>
(KB2596744)  
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
Microsoft Office 2010 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office 2010 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=a7cc8fdc-1c64-434f-87a6-72ddcc356654)  
(KB2598243)  
(Importante)  
[Microsoft Office 2010 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=3050c06c-3cfc-4ce7-83cd-017d0922d597)  
(KB2553447)  
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
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=a7cc8fdc-1c64-434f-87a6-72ddcc356654)  
(KB2598243)  
(Importante)  
[Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=3050c06c-3cfc-4ce7-83cd-017d0922d597)  
(KB2553447)  
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
Microsoft Office 2010 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office 2010 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=ab442918-8184-4c7c-84b0-5a3635fdb005)  
(KB2598243)  
(Importante)  
[Microsoft Office 2010 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=0a8af868-abf7-4aeb-813a-418a04b31608)  
(KB2553447)  
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
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=ab442918-8184-4c7c-84b0-5a3635fdb005)  
(KB2598243)  
(Importante)  
[Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=0a8af868-abf7-4aeb-813a-418a04b31608)  
(KB2553447)  
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
<th colspan="5" style="border:1px solid black;">
Microsoft Office para Mac
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-043**](http://go.microsoft.com/fwlink/?linkid=254824)
</td>
<td style="border:1px solid black;">
[**MS12-046**](http://go.microsoft.com/fwlink/?linkid=252510)
</td>
<td style="border:1px solid black;">
[**MS12-050**](http://go.microsoft.com/fwlink/?linkid=251611)
</td>
<td style="border:1px solid black;">
[**MS12-051**](http://go.microsoft.com/fwlink/?linkid=255000)
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
Ninguna
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office para Mac 2011
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
[Microsoft Office para Mac 2011](http://www.microsoft.com/downloads/details.aspx?familyid=877700ed-3d03-4d46-a77b-5063d8f7d2e3)  
(KB2721015)  
(Importante)
</td>
</tr>
<tr>
<th colspan="5" style="border:1px solid black;">
Otro software de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-043**](http://go.microsoft.com/fwlink/?linkid=254824)
</td>
<td style="border:1px solid black;">
[**MS12-046**](http://go.microsoft.com/fwlink/?linkid=252510)
</td>
<td style="border:1px solid black;">
[**MS12-050**](http://go.microsoft.com/fwlink/?linkid=251611)
</td>
<td style="border:1px solid black;">
[**MS12-051**](http://go.microsoft.com/fwlink/?linkid=255000)
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
Ninguna
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Word Viewer
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=b45f5c9a-d601-4192-92c3-064e9b94785a)  
(KB2596856)  
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
Paquete de compatibilidad de Microsoft Office Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=b45f5c9a-d601-4192-92c3-064e9b94785a)  
(KB2596856)  
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
Paquete de compatibilidad de Microsoft Office Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=b45f5c9a-d601-4192-92c3-064e9b94785a)  
(KB2596856)  
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
Microsoft Groove 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=31e1e6cc-9617-416b-8c91-5c026502d5f6)  
(KB2687497)(Crítica)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Groove 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=31e1e6cc-9617-416b-8c91-5c026502d5f6)  
(KB2687497)(Crítica)
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
<td style="border:1px solid black;">
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft InfoPath 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft InfoPath 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=da8fa3b6-5d01-49e1-a1ce-e3f47ace102b)  
(KB2596666)  
(Importante)  
[Microsoft InfoPath 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a0c826bc-aef8-4833-8471-1824a405c59f)  
(KB2596786)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft InfoPath 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft InfoPath 2007 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=da8fa3b6-5d01-49e1-a1ce-e3f47ace102b)  
(KB2596666)  
(Importante)  
[Microsoft InfoPath 2007 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=a0c826bc-aef8-4833-8471-1824a405c59f)  
(KB2596786)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft InfoPath 2010 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft InfoPath 2010 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=698e6369-253b-4dbe-b6cd-7ea5ea09e043)  
(KB2553431)  
(Importante)  
[Microsoft InfoPath 2010 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=036b2482-0fb4-46f0-9c38-8bae6d0d669b)  
(KB2553322)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft InfoPath 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft InfoPath 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=698e6369-253b-4dbe-b6cd-7ea5ea09e043)  
(KB2553431)  
(Importante)  
[Microsoft InfoPath 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=036b2482-0fb4-46f0-9c38-8bae6d0d669b)  
(KB2553322)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft InfoPath 2010 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft InfoPath 2010 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=3bf373aa-b4ad-4e1a-9578-800485ece148)  
(KB2553431)  
(Importante)  
[Microsoft InfoPath 2010 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=e24337cb-83b4-424f-bc4d-0d43437228a2)  
(KB2553322)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft InfoPath 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft InfoPath 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=3bf373aa-b4ad-4e1a-9578-800485ece148)  
(KB2553431)  
(Importante)  
[Microsoft InfoPath 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=e24337cb-83b4-424f-bc4d-0d43437228a2)  
(KB2553322)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
**Nota para MS12-043**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

**Notas para MS12-046**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

<sup>[1]</sup>Estas actualizaciones de Microsoft Office se aplican a todos los conjuntos de programas compatibles de Microsoft Office y a otro software de Microsoft que Office que contenga el componente de Office compartido vulnerable. Se incluyen, entre otras, las versiones compatibles de Microsoft Visio y Microsoft Project.

**Nota para MS12-050**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Software de servidor de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Office SharePoint Server
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-043**](http://go.microsoft.com/fwlink/?linkid=254824)
</td>
<td style="border:1px solid black;">
[**MS12-050**](http://go.microsoft.com/fwlink/?linkid=251611)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office SharePoint Server 2007 Service Pack 2 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=31e1e6cc-9617-416b-8c91-5c026502d5f6)  
(KB2687497)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office SharePoint Server 2007 Service Pack 2 (coreserver) (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=4073d6e1-32f0-44a8-ae55-3c140ebc09d2)<sup>[1]</sup>
(KB2596663)  
(Importante)  
[Microsoft Office SharePoint Server 2007 Service Pack 2 (xlsrvwfe) (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=d9091923-67c7-4535-b44c-40a5292a94d9)<sup>[1]</sup>
(KB2596942)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office SharePoint Server 2007 Service Pack 3 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=31e1e6cc-9617-416b-8c91-5c026502d5f6)  
(KB2687497)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office SharePoint Server 2007 Service Pack 3 (coreserver) (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=4073d6e1-32f0-44a8-ae55-3c140ebc09d2)<sup>[1]</sup>
(KB2596663)  
(Importante)  
[Microsoft Office SharePoint Server 2007 Service Pack 3 (xlsrvwfe) (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=d9091923-67c7-4535-b44c-40a5292a94d9)<sup>[1]</sup>
(KB2596942)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office SharePoint Server 2007 Service Pack 2 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=fb21c3f8-b3fd-42f2-9c34-e5fbd8cad689)  
(KB2687497)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office SharePoint Server 2007 Service Pack 2 (coreserver) (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=b1acb373-0041-4883-8834-90a72ac04c91)<sup>[1]</sup>
(KB2596663)  
(Importante)  
[Microsoft Office SharePoint Server 2007 Service Pack 2 (xlsrvwfe) (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=723a5553-8610-49bf-99c0-bd94926bdc0b)<sup>[1]</sup>
(KB2596942)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office SharePoint Server 2007 Service Pack 3 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=fb21c3f8-b3fd-42f2-9c34-e5fbd8cad689)  
(KB2687497)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office SharePoint Server 2007 Service Pack 3 (coreserver) (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=b1acb373-0041-4883-8834-90a72ac04c91)<sup>[1]</sup>
(KB2596663)  
(Importante)  
[Microsoft Office SharePoint Server 2007 Service Pack 2 (xlsrvwfe) (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=723a5553-8610-49bf-99c0-bd94926bdc0b)<sup>[1]</sup>
(KB2596942)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2010
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft SharePoint Server 2010 (wosrv)](http://www.microsoft.com/downloads/details.aspx?familyid=59cbb3d0-4ba5-4f89-b54c-ae9aa2aa3b41)  
(KB2553424)  
(Importante)  
[Microsoft SharePoint Server 2010 (coreserverloc)](http://www.microsoft.com/downloads/details.aspx?familyid=8a853489-a3ec-4be2-8093-6a992f9c8368)  
(KB2553194)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft SharePoint Server 2010 Service Pack 1 (wosrv)](http://www.microsoft.com/downloads/details.aspx?familyid=59cbb3d0-4ba5-4f89-b54c-ae9aa2aa3b41)  
(KB2553424)  
(Importante)  
[Microsoft SharePoint Server 2010 Service Pack 1 (coreserverloc)](http://www.microsoft.com/downloads/details.aspx?familyid=8a853489-a3ec-4be2-8093-6a992f9c8368)  
(KB2553194)  
(Importante)
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
[**MS12-043**](http://go.microsoft.com/fwlink/?linkid=254824)
</td>
<td style="border:1px solid black;">
[**MS12-050**](http://go.microsoft.com/fwlink/?linkid=251611)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
<td style="border:1px solid black;">
Microsoft Groove Server 2010
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Groove Server 2010](http://www.microsoft.com/downloads/details.aspx?familyid=e2346078-fc93-4355-bc83-0d0dc1cd4b2f)  
(KB2589325)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Groove Server 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Groove Server 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=e2346078-fc93-4355-bc83-0d0dc1cd4b2f)  
(KB2589325)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows SharePoint Services y Microsoft SharePoint Foundation
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-043**](http://go.microsoft.com/fwlink/?linkid=254824)
</td>
<td style="border:1px solid black;">
[**MS12-050**](http://go.microsoft.com/fwlink/?linkid=251611)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Windows SharePoint Services 2.0
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Windows SharePoint Services 2.0](http://www.microsoft.com/downloads/details.aspx?familyid=7a54f510-0782-44c4-848a-8ef90d332e61)<sup>[2]</sup>
(KB2760604)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Windows SharePoint Services 3.0 Service Pack 2 (versión de 32 bits):
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Windows SharePoint Services 3.0 Service Pack 2 (versión de 32 bits):](http://www.microsoft.com/downloads/details.aspx?familyid=61b9f234-3d9c-41d4-854d-30ca5e6fd2a6)  
(KB2596911)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Windows SharePoint Services 3.0 Service Pack 2 (versión de 64 bits):
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Windows SharePoint Services 3.0 Service Pack 2 (versión de 64 bits):](http://www.microsoft.com/downloads/details.aspx?familyid=24265175-635f-4846-afcc-f692d4710707)  
(KB2596911)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Foundation 2010
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft SharePoint Foundation 2010](http://www.microsoft.com/downloads/details.aspx?familyid=4d610646-a0bd-492c-9077-fb2c92588c14)  
(KB2553365)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Foundation 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft SharePoint Foundation 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=4d610646-a0bd-492c-9077-fb2c92588c14)  
(KB2553365)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS12-043**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

**Notas para MS12-050**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

<sup>[1]</sup>Para las ediciones compatibles de Microsoft Office SharePoint Server 2007, además de los paquetes de actualización de seguridad para Microsoft Office SharePoint 2007 (KB2596663 y KB2596942), los clientes también deben instalar la actualización de seguridad para Microsoft Windows SharePoint Services 3.0 (KB2596911) a fin de estar protegidos contra las vulnerabilidades descritas en este boletín.

<sup>[2]</sup>Esta actualización solo está disponible en el Centro de descarga de Microsoft.

#### Microsoft Office Web Apps

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Office Web Apps
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-050**](http://go.microsoft.com/fwlink/?linkid=251611)
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
Microsoft Office Web Apps 2010
</td>
<td style="border:1px solid black;">
[Microsoft Office Web Apps 2010](http://www.microsoft.com/downloads/details.aspx?familyid=f2d1c371-d617-4792-966e-14ae9ed6b8a1)  
(KB2598239)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office Web Apps 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft Office Web Apps 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=f2d1c371-d617-4792-966e-14ae9ed6b8a1)  
(KB2598239)
</td>
</tr>
</table>
 
**Nota para MS12-050**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Herramientas y software para desarrolladores de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Expression Web
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-043**](http://go.microsoft.com/fwlink/?linkid=254824)
</td>
<td style="border:1px solid black;">
[**MS12-046**](http://go.microsoft.com/fwlink/?linkid=252510)
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
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Expression Web Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=b45f5c9a-d601-4192-92c3-064e9b94785a)  
(KB2596856)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Expression Web 2
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=b45f5c9a-d601-4192-92c3-064e9b94785a)  
(KB2596856)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Visual Basic para Aplicaciones
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador** **del** **boletín**
</td>
<td style="border:1px solid black;">
[**MS12-043**](http://go.microsoft.com/fwlink/?linkid=254824)
</td>
<td style="border:1px solid black;">
[**MS12-046**](http://go.microsoft.com/fwlink/?linkid=252510)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Visual Basic para Aplicaciones
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Visual Basic para Aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=ea7c5762-586f-4e38-ad63-43eb05e79f4d)<sup>[1]</sup>
(KB2688865)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
SDK de Microsoft Visual Basic para aplicaciones
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
SDK de Microsoft Visual Basic para Aplicaciones<sup>[2]</sup><sup>[3]</sup>
(Importante)
</td>
</tr>
</table>
 
**Nota para MS12-043**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

**Notas para MS12-046**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

<sup>[1]</sup>Este paquete de actualización se aplica a las versiones compatibles del módulo de tiempo de ejecución de Microsoft Visual Basic para Aplicaciones (Vbe6.dll) y sólo está disponible en el Centro de descarga de Microsoft.

<sup>[2]</sup>Las versiones compatibles de VBA SDK son SDK de Microsoft Visual Basic para Aplicaciones 6.3, SDK de Microsoft Visual Basic para Aplicaciones 6.4 y SDK de Microsoft Visual Basic para Aplicaciones 6.5.

<sup>[3]</sup>La versión actualizada del SDK de Visual Basic para Aplicaciones que corrige la vulnerabilidad descrita en este boletín está disponible para los proveedores de software independientes (ISV) en Summit Software Company.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/bb245732). [TechNet Security Center](http://technet.microsoft.com/es-es/security) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://www.microsoft.com/es-es/security/default.aspx), donde esta información también está disponible haciendo clic en "Últimas actualizaciones de seguridad".

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Para clientes de Microsoft Office para Mac, Microsoft AutoUpdate para Mac puede servir de ayuda para mantener actualizado el software de Microsoft. Para obtener más información acerca del uso de Microsoft AutoUpdate para Mac, vea [Buscar actualizaciones de software automáticamente](http://mac2.microsoft.com/help/office/14/en-us/word/item/ffe35357-8f25-4df8-a0a3-c258526c64ea).

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS07-036"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Consejos para la detección y la implementación**

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747).

**Microsoft** **Baseline** **Security** **Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://go.microsoft.com/fwlink/?linkid=21134).

**Windows Server** **UpdateServices**

Windows Server Update Services (WSUS) permite a los administradores implementar de un modo rápido y confiable las actualizaciones críticas y de seguridad más recientes en sistemas operativos Microsoft Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://technet.microsoft.com/en-us/wsus/default.aspx).

**System** **Center** **Configuration** **Manager**

La administración de actualizaciones de software de System Center Configuration Manager simplifica la tarea compleja de entregar y administrar actualizaciones para los sistemas de TI en toda la empresa. Con System Center Configuration Manager, los administradores de TI pueden ofrecer actualizaciones de los productos de Microsoft a una serie de dispositivos, incluidos equipos de escritorio, portátiles, servidores y dispositivos móviles.

La evaluación automática de vulnerabilidades en System Center Configuration Manager detecta las necesidades de actualizaciones e informa de las acciones recomendadas. La administración de actualizaciones de software en System Center Configuration Manager se basa en Microsoft Windows Software Update Services (WSUS), una infraestructura de actualizaciones probada con la que están familiarizados los administradores de TI de todo el mundo. Para obtener más información acerca de cómo los administradores pueden usar System Center Configuration Manager para implementar actualizaciones, vea [Administración de actualizaciones de software](http://www.microsoft.com/systemcenter/en/us/configuration-manager/cm-software-update-management.aspx). Para obtener más información acerca de System Center Configuration Manager, visite [System Center Configuration Manager](http://www.microsoft.com/systemcenter/en/us/configuration-manager.aspx).

**Systems** **Management Server 2003**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales.

**Nota** System Management Server 2003 está fuera del soporte técnico general desde el 12 de enero de 2010. Para obtener más información acerca de los ciclos de vida de los productos, visite [Ciclo de vida del soporte técnico de Microsoft](http://support.microsoft.com/common/international.aspx?rdpath=dm;en-us;lifecycle). Ya está disponible la siguiente versión de SMS, System Center Configuration Manager; vea la sección anterior, **System** **Center** **Configuration** **Manager**.

Para obtener más información acerca de cómo los administradores pueden usar SMS 2003 para implementar actualizaciones de seguridad, vea [Escenarios y procedimientos para Microsoft Systems Management Server 2003: Administración de distribución de software y revisiones](http://www.microsoft.com/downloads/en/details.aspx?familyid=32f2bb4c-42f8-4b8d-844f-2553fd78049f&displaylang=en). Para obtener información acerca de SMS, visite [Microsoft Systems Management Server TechCenter](http://technet.microsoft.com/en-us/systemcenter/bb545936.aspx).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://www.microsoft.com/downloads/en/details.aspx?familyid=7bd3a16e-1899-4e0b-bb99-1320e816167d&displaylang=en)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet2.microsoft.com/windowsvista/en/library/4279e239-37a4-44aa-aec5-4e70fe39f9de1033.mspx?mfr=true) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Artículo 894199 de Microsoft Knowledge Base](http://support.microsoft.com/kb/894199)
-   : Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones de meses anteriores para Windows Server Update Services](http://technet.microsoft.com/en-us/wsus/bb456965.aspx)
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

-   [Google Security Team](http://www.google.com/)
-   , por colaborar con nosotros en un problema descrito en MS12-043
-   [Qihoo 360 Security Center](http://www.360.cn/)
-   , por informar de un problema descrito en MS12-043
-   Jose A. Vazquez, de spa-s3c.blogspot.com, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS12-044
-   Omair, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS12-044
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.hpenterprisesecurity.com/products/hp-tippingpoint-network-security/), por informar de un problema descrito en MS12-045
-   Bai Haowen, de [Huawei Security Labs](http://www.huawei.com), por informar de un problema descrito en MS12-046
-   Nicolas Economou, de [Core Security Technologies](http://www.coresecurity.com/), por informar de un problema descrito en MS12-047
-   [Qihoo 360 Security Center](http://www.360.cn/)
-   , por informar de un problema descrito en MS12-047
-   Lufeng Li, de Neusoft Corporation, en colaboración con [Secunia Research](http://secunia.com/), por informar de un problema descrito en MS12-047
-   Adi Cohen, de [IBM Security Systems - Application Security](http://blog.watchfire.com/), por informar de un problema descrito en MS12-048
-   Adi Cohen, de [IBM Security Systems - Application Security](http://blog.watchfire.com/), por informar de un problema descrito en MS12-050
-   Yang Yang, de [Salesforce.com Product Security Team](https://trust.salesforce.com/), por informar de un problema descrito en MS12-050

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Soluciones de seguridad para profesionales de TI: Soporte técnico y solución de problemas de seguridad de TechNet
-   Ayuda para proteger su equipo con Windows de virus y malware: [Solución antivirus y centro de seguridad](http://support.microsoft.com/contactus/cu_sc_virsec_master)
-   Soporte local según su país: [Soporte internacional](http://support.microsoft.com/common/international.aspx)

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (10 de julio de 2012): Publicación del resumen del boletín.
-   V1.1 (10 de julio de 2012): Se ha quitado CVE-2012-1860 del índice de explotabilidad debido a que la vulnerabilidad tiene una clasificación de gravedad moderada. Sólo se incluyen en el índice de explotabilidad las vulnerabilidades que tienen una clasificación de gravedad crítica o importante en los boletines.
-   V2.0 (15 de agosto de 2012): Para MS12-043, se agregaron los vínculos de descarga para Microsoft XML Core Services 5.0.
-   V3.0 (9 de octubre de 2012): para MS12-043, se agregó Microsoft XML Core Services 4.0 cuando está instalado en ediciones compatibles de Windows 8 y Windows Server 2012 para el software afectado. Vea el boletín MS12-043 para obtener detalles.
-   V4.0 (13 de noviembre de 2012): para MS12-046, la actualización KB2598361 se reemplazó por la actualización KB2687626 para Microsoft Office 2003 Service Pack 3. Vea el boletín MS12-046 para obtener detalles.
-   V5.0 (11 de diciembre de 2012): para MS12-043, se ha reemplazado la actualización KB2687324 por la actualización KB2687627 para Microsoft XML Core Services 5.0 cuando está instalado en Microsoft Office 2003 Service Pack 3 y se ha reemplazado la actualización KB2596679 por la actualización KB2687497 para Microsoft XML Core Services 5.0 cuando se instala con todas las ediciones afectadas de Microsoft Groove 2007, Microsoft Groove Server 2007 y Microsoft Office SharePoint Server 2007. Vea el boletín MS12-043 para obtener detalles.
-   V5.1 (12 de diciembre de 2012): para MS12-050, se ha revisado el resumen del boletín para anunciar la disponibilidad de una actualización para Microsoft Windows SharePoint Services 2.0. Esta actualización solo está disponible en el Centro de descarga de Microsoft.

*Built at 2014-04-18T01:50:00Z-07:00*
