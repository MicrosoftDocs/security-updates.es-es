---
TOCTitle: 'MS11-AUG'
Title: Microsoft Security Bulletin Summary for agosto 2011
ms:assetid: 'ms11-aug'
ms:contentKeyID: 61225421
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms11-aug(v=Security.10)'
---

Microsoft Security Bulletin Summary for agosto 2011
===================================================

Publicado: martes, 9 de agosto de 2011 | Actualizado: miércoles, 26 de octubre de 2011

**Versión:** 1.2

Este resumen del boletín enumera los boletines de seguridad publicados para agosto de 2011.

Con la publicación de los boletines de seguridad de agosto de 2011, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 4 de agosto de 2011. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/es-es/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 10 de agosto de 2011, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de agosto](https://msevents.microsoft.com/cui/eventdetail.aspx?culture=en-us&eventid=1032487857). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, vea los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217214).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información** **adicional**.

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-057">MS11-057</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (2559049)</strong> <br />
<br />
Esta actualización de seguridad resuelve cinco vulnerabilidades de las que se ha informado de forma privada y dos vulnerabilidades de las que se ha informado de forma pública en Internet Explorer. La más grave de las vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un intruso que aprovechara cualquiera de estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario local. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, <br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-058">MS11-058</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en el servidor DNS</strong> <strong>podrían</strong> <strong>permitir la ejecución remota de código (2562485)</strong> <br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en el servidor DNS de Windows. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un atacante registra un dominio, crea un registro NAPTR DNS y, a continuación, envía una consulta NAPTR especialmente diseñada al servidor DNS de destino. Los servidores que no tienen habilitado el rol DNS no están expuestos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-059">MS11-059</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Data Access</strong> <strong>Components</strong> <strong>podría permitir la ejecución remota de código (2560656)</strong> <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo de Excel legítimo (como un archivo .xlsx) que se encuentre en el mismo directorio de red que un archivo de biblioteca especialmente diseñado. Un intruso que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario que ha iniciado sesión. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-060">MS11-060</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Visio</strong> <strong>podrían</strong> <strong>permitir la ejecución remota de código (2560978)</strong> <br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft Visio. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario abre un archivo de Visio especialmente diseñado. Un intruso que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario que ha iniciado sesión. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-061">MS11-061</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Acceso web a Escritorio remoto podría permitir la elevación de privilegios (2546250)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Acceso web a Escritorio remoto. Se trata de una vulnerabilidad de scripts de sitios (XSS) que podría permitir la elevación de privilegios, lo que permitiría que un atacante ejecutar comandos arbitrarios en el sitio en el contexto del usuario atacado. El filtro XSS en Internet Explorer 8 e Internet Explorer 9 impide este ataque a sus usuarios al explorar un servidor de Acceso web a Escritorio remoto en la zona Internet. El filtro XSS en Internet Explorer 8 e Internet Explorer 9 no está habilitado de forma predeterminada en la zona Intranet.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-062">MS11-062</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el controlador NDISTAPI de Servicio de acceso remoto podría permitir la elevación de privilegios (2566454)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en todas las ediciones compatibles de Windows XP y Windows Server 2003. Esta actualización de seguridad se considera importante para todas las ediciones compatibles de Windows XP y Windows Server 2003. Windows Vista, Windows Server 2008, Windows 7 y Windows Server 2008 R2 no están afectados por la vulnerabilidad.<br />
<br />
La vulnerabilidad podría permitir la elevación de privilegios si un atacante inicia sesión en un sistema afectado y ejecuta una aplicación especialmente diseñada con la finalidad de aprovechar la vulnerabilidad y tomar el control completo sobre el sistema afectado. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-063">MS11-063</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el subsistema de tiempo de ejecución de cliente-servidor de Windows podría permitir la elevación de privilegios (2567680)</strong> <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si un atacante inicia sesión en un sistema afectado y ejecuta una aplicación especialmente diseñada para enviar un mensaje de evento de dispositivo a un proceso de mayor integridad. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-064">MS11-064</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en la pila de TCP/IP</strong> <strong>podrían</strong> <strong>permitir la ejecución remota de código (2563894)</strong> <br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. Las vulnerabilidades podrían permitir la denegación de servicio si un atacante envía una secuencia de mensajes de protocolo de mensajes de control de Internet (ICMP) especialmente diseñados a un sistema de destino o envía una solicitud de dirección URL especialmente diseñada a un servidor que sirve contenido web y tiene habilitada la característica de calidad de servicio (QoS) basada en dirección URL.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Denegación de servicio</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-065">MS11-065</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el protocolo de Escritorio remoto podría permitir la denegación de servicio (2570222)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en el protocolo de Escritorio remoto. La vulnerabilidad podría permitir la denegación de servicio si un sistema afectado recibe una secuencia de paquetes RDP especialmente diseñados. Microsoft también ha recibido informes de ataques limitados y dirigidos que intentan aprovechar esta vulnerabilidad. De forma predeterminada, el protocolo de Escritorio remoto (RDP) no está habilitado en ningún sistema operativo Windows.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Denegación de servicio</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-066">MS11-066</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el control de gráficos de Microsoft podría permitir la divulgación de información (2567943)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en los controles de gráficos de ASP.NET. La vulnerabilidad podría permitir la divulgación de información si un atacante envía una solicitud GET especialmente diseñada a un servidor afectado que hospede los controles de gráficos. Es importante mencionar que la vulnerabilidad no permitirá al atacante ejecutar código o elevar directamente sus derechos de usuario, pero podría servir para recuperar información que se podría usar para poner en peligro el sistema afectado. Solo las aplicaciones web que usan el control de gráficos de Microsoft están afectadas por este problema. Las instalaciones predeterminadas de .NET Framework no están afectadas.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Divulgación de información</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft .NET Framework, <br />
Herramientas de desarrollo de Microsoft</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-067">MS11-067</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft</strong> <strong>ReportViewer</strong> <strong>podría permitir la divulgación de información (2578230)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Report Viewer. La vulnerabilidad podría permitir la divulgación de información si un usuario visita una página web especialmente diseñada. Sin embargo, el atacante no podría en ningún caso obligar al usuario a visitar el sitio web. Por lo tanto, tendría que atraerlo al sitio web; por lo general, convenciéndole para que haga clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger que lleve al usuario al sitio web vulnerable.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Divulgación de información</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Herramientas de desarrollo de Microsoft</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-068">MS11-068</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el</strong> <strong>kernel</strong> <strong>de Windows podría permitir la denegación de servicio (2556532)</strong> <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la denegación de servicio si un usuario obtiene acceso a un recurso compartido de red (o visita un sitio web que apunta a un recurso compartido de red) que contenga un archivo especialmente diseñado. Sin embargo, el atacante no podría en ningún caso obligar al usuario a tener acceso al recurso compartido de red o a visitar el sitio web. Por lo tanto, tendría que atraerlo; por lo general, convenciéndole para que haga clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Moderada</a><br />
Denegación de servicio</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-069">MS11-069</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en .NET Framework podría permitir la divulgación de información (2567951)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft .NET Framework. La vulnerabilidad podría permitir la divulgación de información si un usuario visita una página web especialmente diseñada mediante un explorador web que pueda ejecutar aplicaciones del explorador XAML (XBAP). En el caso de un ataque basado en web, el intruso podría alojar un sitio web que contuviera una página web para aprovechar esta vulnerabilidad. Además, los sitios web vulnerables y los sitios web que aceptan o alojan contenido o anuncios proporcionados por el usuario podrían incluir contenido especialmente diseñado que permita aprovechar esta vulnerabilidad. Sin embargo, el atacante no podría en ningún caso obligar a los usuarios a visitar estos sitios web. Por lo tanto, tendría que atraerlos al sitio web; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger que lleve a los usuarios al sitio web del atacante. Esta vulnerabilidad también la podrían usar aplicaciones Windows .NET para omitir las restricciones de seguridad de acceso del código (CAS).</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Moderada</a><br />
Divulgación de información</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft .NET Framework</td>
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
<th style="border:1px solid black;" >Evaluación de explotabilidad de ejecución de código para la última versión de software</th>
<th style="border:1px solid black;" >Evaluación de explotabilidad de ejecución de código para las versiones de software anteriores</th>
<th style="border:1px solid black;" >Evaluación de explotabilidad de denegación de servicio</th>
<th style="border:1px solid black;" >Notas clave</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-057">MS11-057</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de apertura de ventana</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1257">CVE-2011-1257</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-057">MS11-057</a></td>
<td style="border:1px solid black;">Vulnerabilidad de divulgación de información en controladores de evento</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1960">CVE-2011-1960</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-057">MS11-057</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código en el controlador de telnet</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1961">CVE-2011-1961</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-057">MS11-057</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con XSLT</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1963">CVE-2011-1963</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-057">MS11-057</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con los objetos de estilo</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1964">CVE-2011-1964</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-058">MS11-058</a></td>
<td style="border:1px solid black;">Vulnerabilidad de consulta NAPTR en DNS</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1966">CVE-2011-1966</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-058">MS11-058</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria no inicializada en DNS</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1970">CVE-2011-1970</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-059">MS11-059</a></td>
<td style="border:1px solid black;">Vulnerabilidad en la carga de bibliotecas no seguras en Data Access Components</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1975">CVE-2011-1975</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-060">MS11-060</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código en liberación de pStream</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1972">CVE-2011-1972</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-060">MS11-060</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código de desplazamiento</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1979">CVE-2011-1979</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-061">MS11-061</a></td>
<td style="border:1px solid black;">Vulnerabilidad de Acceso web a Escritorio remoto</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1263">CVE-2011-1263</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-062">MS11-062</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en NDISTAPI</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1974">CVE-2011-1974</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-063">MS11-063</a></td>
<td style="border:1px solid black;">Vulnerabilidad de CSRSS</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1967">CVE-2011-1967</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-064">MS11-064</a></td>
<td style="border:1px solid black;">Vulnerabilidad de denegación de servicio en ICMP</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1871">CVE-2011-1871</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-064">MS11-064</a></td>
<td style="border:1px solid black;">Vulnerabilidad de denegación de servicio en QoS de TCP/IP</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1965">CVE-2011-1965</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-065">MS11-065</a></td>
<td style="border:1px solid black;">Vulnerabilidad de protocolo de Escritorio remoto</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1968">CVE-2011-1968</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se ha informado de ataques limitados y dirigidos para esta vulnerabilidad<br />
<br />
Se trata de una vulnerabilidad de denegación de servicio</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-066">MS11-066</a></td>
<td style="border:1px solid black;">Vulnerabilidad de divulgación de información en el control de gráficos</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1977">CVE-2011-1977</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-067">MS11-067</a></td>
<td style="border:1px solid black;">Vulnerabilidad de XSS en los controles de Report Viewer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1976">CVE-2011-1976</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información</td>
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
  
**Tabla 1**

 
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
<th style="border:1px solid black;" >
</th>
</tr>
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
[**MS11-057**](http://go.microsoft.com/fwlink/?linkid=221946)
</td>
<td style="border:1px solid black;">
[**MS11-058**](http://go.microsoft.com/fwlink/?linkid=221812)
</td>
<td style="border:1px solid black;">
[**MS11-059**](http://go.microsoft.com/fwlink/?linkid=221539)
</td>
<td style="border:1px solid black;">
[**MS11-061**](http://go.microsoft.com/fwlink/?linkid=217099)
</td>
<td style="border:1px solid black;">
[**MS11-062**](http://go.microsoft.com/fwlink/?linkid=223669)
</td>
<td style="border:1px solid black;">
[**MS11-063**](http://go.microsoft.com/fwlink/?linkid=221864)
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
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=90312c78-1fbd-4143-b2e6-ae5c48af6f57)  
(Crítica)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=a771c93b-55a4-456f-a315-d0d1f2696960)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=5feb8ed7-99d2-4dd6-986f-57a7fd0c6f19)  
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
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=6bc1f0ac-223d-4b0b-86cd-2ba3863955c4)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=0231c103-c0cb-4705-9d92-5356b8cbb265)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=23d77f3b-13f8-49f3-9c3c-27ad217cd59e)  
(Crítica)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=acb14d82-a801-4ec7-84cc-9f131009ebcb)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=272c813b-bd39-4e63-9fa7-c5b8ed0b08d7)  
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
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d5ee6787-408d-4870-af70-9338158b161b)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=09276f6e-e3f4-4b7e-996e-4ec376c103e1)  
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
[**MS11-057**](http://go.microsoft.com/fwlink/?linkid=221946)
</td>
<td style="border:1px solid black;">
[**MS11-058**](http://go.microsoft.com/fwlink/?linkid=221812)
</td>
<td style="border:1px solid black;">
[**MS11-059**](http://go.microsoft.com/fwlink/?linkid=221539)
</td>
<td style="border:1px solid black;">
[**MS11-061**](http://go.microsoft.com/fwlink/?linkid=217099)
</td>
<td style="border:1px solid black;">
[**MS11-062**](http://go.microsoft.com/fwlink/?linkid=223669)
</td>
<td style="border:1px solid black;">
[**MS11-063**](http://go.microsoft.com/fwlink/?linkid=221864)
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
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=26b5fb48-346a-49f1-840f-03f218a41c20)  
(Importante)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=042552ad-f46a-4bfc-9e5c-58f095eba1de)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=648596fc-fd97-438a-97be-d5d590f1c561)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c2d4aa38-9241-465d-8d65-aba73e936d0f)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8de0f2db-aa09-48cd-a13b-e26a973e9cdc)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=870fdfdd-16bf-42a2-a23b-ed6045438d5e)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=9c3d14d8-6716-4423-91a9-a05373227237)  
(Importante)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=c9e283d8-d4a2-41e2-a73c-92fae957ba3d)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=470d56d1-5789-42cc-a088-a2c8ac934ab3)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2db4098a-f4f9-4211-b55d-5d0df1409c43)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8f208407-4bb3-41fe-b0d6-fc8a5e30e667)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=31af27b8-7b73-4090-94bd-2fb89d3970fc)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=64496a87-2225-402a-a94a-a8e92b17ac83)  
(Importante)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=5aa3a493-4188-48a9-a549-cf9ba01ed32a)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=1934acfa-5637-4ae9-9e9a-fc7e58930b7a)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=ef140089-d022-4ee8-9cc4-7fb25295a39d)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=410c72d8-3b78-4c4a-ad61-acb7f854ffc2)  
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
[**MS11-057**](http://go.microsoft.com/fwlink/?linkid=221946)
</td>
<td style="border:1px solid black;">
[**MS11-058**](http://go.microsoft.com/fwlink/?linkid=221812)
</td>
<td style="border:1px solid black;">
[**MS11-059**](http://go.microsoft.com/fwlink/?linkid=221539)
</td>
<td style="border:1px solid black;">
[**MS11-061**](http://go.microsoft.com/fwlink/?linkid=217099)
</td>
<td style="border:1px solid black;">
[**MS11-062**](http://go.microsoft.com/fwlink/?linkid=223669)
</td>
<td style="border:1px solid black;">
[**MS11-063**](http://go.microsoft.com/fwlink/?linkid=221864)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=66ddc7ce-5280-494d-bb3c-dab06e27fb5c)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=a080f36e-c24f-40ac-bb40-b26cb31bcae3)  
(Crítica)  

[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=c82417ec-232f-4f84-ba2c-0ffad77e9bb5)  
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
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8f25ced5-ef86-4b9d-91fb-443c9a2c1458)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=3f119902-8398-4814-8229-9eb9f0980e87)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=704c1c9c-d1c1-40cb-97a7-fbb1f195f9f8)  
(Crítica)  

[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=a6ff7b27-bc21-4945-8b2e-757b6f83fa58)  
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
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d5b8ff09-237e-49f1-a566-e323ca11fbc3)  
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
[**MS11-057**](http://go.microsoft.com/fwlink/?linkid=221946)
</td>
<td style="border:1px solid black;">
[**MS11-058**](http://go.microsoft.com/fwlink/?linkid=221812)
</td>
<td style="border:1px solid black;">
[**MS11-059**](http://go.microsoft.com/fwlink/?linkid=221539)
</td>
<td style="border:1px solid black;">
[**MS11-061**](http://go.microsoft.com/fwlink/?linkid=217099)
</td>
<td style="border:1px solid black;">
[**MS11-062**](http://go.microsoft.com/fwlink/?linkid=223669)
</td>
<td style="border:1px solid black;">
[**MS11-063**](http://go.microsoft.com/fwlink/?linkid=221864)
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
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=da9c98d1-973c-44d9-aee5-f5c4a8e8c0e1)\*\*  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=d65ae4cc-d82a-42da-829f-d9479e23b7a5)\*\*  
(Crítica)  

[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=70065bd0-7c97-4ffc-828f-2cc245d04429)\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ac2d5122-6f9b-46f5-9840-77aa7ff84308)\*  
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
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1fbaabb9-8601-4760-813d-aeedfdcafb8b)\*  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=9facff69-618f-4a64-8665-5dd6cde07de9)\*\*  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=00f28d81-3714-403c-bcd7-55f2ac97f75b)\*\*  
(Crítica)  

[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=9ce60689-ca85-4c9f-af96-a73b1e43c10b)\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5f605f6f-3854-403d-878b-637626aef78f)\*  
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
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2e7253d8-fdc7-4563-9714-21ca3c77e4b1)\*  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=01885624-cfb1-4918-abef-ab0ea765cb04)  
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
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=fe37eb6d-b1fa-496c-a0d3-19a6d35a6cb9)  
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
[**MS11-057**](http://go.microsoft.com/fwlink/?linkid=221946)
</td>
<td style="border:1px solid black;">
[**MS11-058**](http://go.microsoft.com/fwlink/?linkid=221812)
</td>
<td style="border:1px solid black;">
[**MS11-059**](http://go.microsoft.com/fwlink/?linkid=221539)
</td>
<td style="border:1px solid black;">
[**MS11-061**](http://go.microsoft.com/fwlink/?linkid=217099)
</td>
<td style="border:1px solid black;">
[**MS11-062**](http://go.microsoft.com/fwlink/?linkid=223669)
</td>
<td style="border:1px solid black;">
[**MS11-063**](http://go.microsoft.com/fwlink/?linkid=221864)
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
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=7019de24-8c58-4565-ada1-ca8755115096)  
(Crítica)  

[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=12292081-23f7-4968-8cd7-17aaef2aed6a)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=6bc168d9-6664-41fb-914f-dbd7514a4b0e)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=f4551b77-eb09-448a-9dc5-66de846035e7)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=fcdb872f-2ee2-4f74-b7ae-1b82daf66761)  
(Crítica)  

[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=ef664114-6582-49d3-b332-078a7d075337)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=aafeff2d-db9a-4b3b-b620-be4ec5f5bdcc)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=0fc9a501-523d-4cbb-8d99-a773089afc4c)  
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
[**MS11-057**](http://go.microsoft.com/fwlink/?linkid=221946)
</td>
<td style="border:1px solid black;">
[**MS11-058**](http://go.microsoft.com/fwlink/?linkid=221812)
</td>
<td style="border:1px solid black;">
[**MS11-059**](http://go.microsoft.com/fwlink/?linkid=221539)
</td>
<td style="border:1px solid black;">
[**MS11-061**](http://go.microsoft.com/fwlink/?linkid=217099)
</td>
<td style="border:1px solid black;">
[**MS11-062**](http://go.microsoft.com/fwlink/?linkid=223669)
</td>
<td style="border:1px solid black;">
[**MS11-063**](http://go.microsoft.com/fwlink/?linkid=221864)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=14fe68eb-2aa6-4a59-b9d8-deeae5236af2)\*\*  
(Crítica)  

[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=dd709da2-4cb1-482f-88eb-dfab4d3c59c6)\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=6a86e2cf-4e7d-4012-88c3-6957a3842dd3)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=c29deec3-4672-4658-a550-dce244434cd4)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=777f3bbe-094c-411d-879d-34a5a20ae7f3)\*\*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=2f4043df-c07c-4611-b06a-7fcbb7416e7d)\*  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=82403fd3-ed75-4ea8-aa3f-ed9dda75612a)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1d6b8036-d38f-408a-a36c-027553faefc1)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b420cae3-de30-4c6c-8ed9-7431ad7ab4da)  
(Importante)
</td>
</tr>
</table>
 
**Notaspara** **Windows Server 2008 y Windows Server 2008 R2**

**\*La instalación de Server** **Core** **está afectada.** Esta actualización se aplica, con la misma clasificación de gravedad, a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, independientemente de si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**\*\*La instalación de Server** **Core** **no está afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**Tabla 2**

 
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
Windows XP
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-064**](http://go.microsoft.com/fwlink/?linkid=221808)
</td>
<td style="border:1px solid black;">
[**MS11-065**](http://go.microsoft.com/fwlink/?linkid=221880)
</td>
<td style="border:1px solid black;">
[**MS11-066**](http://go.microsoft.com/fwlink/?linkid=221536)
</td>
<td style="border:1px solid black;">
[**MS11-068**](http://go.microsoft.com/fwlink/?linkid=223578)
</td>
<td style="border:1px solid black;">
[**MS11-069**](http://go.microsoft.com/fwlink/?linkid=221537)
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
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=c07e1630-43ba-491e-bd59-9eb53105986c)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=6ca837f7-eda1-4ebe-b48a-8c77f949ebfd)<sup>[1]</sup>
(KB2487367)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=14fdbaa4-b42b-499c-819f-bb239b48a4cc)  
(KB2539631)  
(Moderada)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)<sup>[1]</sup>
(KB2539636)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=797a01dc-39fb-4511-832a-42d2975133f5)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=6ca837f7-eda1-4ebe-b48a-8c77f949ebfd)<sup>[1]</sup>
(KB2487367)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=14fdbaa4-b42b-499c-819f-bb239b48a4cc)  
(KB2539631)  
(Moderada)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)<sup>[1]</sup>
(KB2539636)  
(Moderada)
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-064**](http://go.microsoft.com/fwlink/?linkid=221808)
</td>
<td style="border:1px solid black;">
[**MS11-065**](http://go.microsoft.com/fwlink/?linkid=221880)
</td>
<td style="border:1px solid black;">
[**MS11-066**](http://go.microsoft.com/fwlink/?linkid=221536)
</td>
<td style="border:1px solid black;">
[**MS11-068**](http://go.microsoft.com/fwlink/?linkid=223578)
</td>
<td style="border:1px solid black;">
[**MS11-069**](http://go.microsoft.com/fwlink/?linkid=221537)
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
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=694ba1a6-7512-497d-a572-646a6e07b13b)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=6ca837f7-eda1-4ebe-b48a-8c77f949ebfd)<sup>[1]</sup>
(KB2487367)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=14fdbaa4-b42b-499c-819f-bb239b48a4cc)  
(KB2539631)  
(Moderada)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)<sup>[1]</sup>
(KB2539636)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=308da543-d49d-4591-8bbc-d65c524bb0ad)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=6ca837f7-eda1-4ebe-b48a-8c77f949ebfd)<sup>[1]</sup>
(KB2487367)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=14fdbaa4-b42b-499c-819f-bb239b48a4cc)  
(KB2539631)  
(Moderada)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)<sup>[1]</sup>
(KB2539636)  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=3b459bf0-7844-4740-895c-d149d56e781f)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=6ca837f7-eda1-4ebe-b48a-8c77f949ebfd)<sup>[1]</sup>
(KB2487367)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=14fdbaa4-b42b-499c-819f-bb239b48a4cc)  
(KB2539631)  
(Moderada)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)<sup>[1]</sup>
(KB2539636)  
(Moderada)
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-064**](http://go.microsoft.com/fwlink/?linkid=221808)
</td>
<td style="border:1px solid black;">
[**MS11-065**](http://go.microsoft.com/fwlink/?linkid=221880)
</td>
<td style="border:1px solid black;">
[**MS11-066**](http://go.microsoft.com/fwlink/?linkid=221536)
</td>
<td style="border:1px solid black;">
[**MS11-068**](http://go.microsoft.com/fwlink/?linkid=223578)
</td>
<td style="border:1px solid black;">
[**MS11-069**](http://go.microsoft.com/fwlink/?linkid=221537)
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
Ninguna
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=114c2835-921a-4d3e-be91-dfd217fd26a9)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=6ca837f7-eda1-4ebe-b48a-8c77f949ebfd)<sup>[1]</sup>
(KB2487367)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9713b7b8-f260-440d-a994-845f17683fe9)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2f7348c0-a036-4d86-b7bb-bd6810cdc834)  
(KB2539633)  
(Moderada)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)<sup>[1]</sup>
(KB2539636)  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=0fcee476-8d7e-49a7-b6ea-89043304a653)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=6ca837f7-eda1-4ebe-b48a-8c77f949ebfd)<sup>[1]</sup>
(KB2487367)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4d67ec00-e86a-49b6-a9a2-85b2520fa4bb)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2f7348c0-a036-4d86-b7bb-bd6810cdc834)  
(KB2539633)  
(Moderada)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)<sup>[1]</sup>
(KB2539636)  
(Moderada)
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-064**](http://go.microsoft.com/fwlink/?linkid=221808)
</td>
<td style="border:1px solid black;">
[**MS11-065**](http://go.microsoft.com/fwlink/?linkid=221880)
</td>
<td style="border:1px solid black;">
[**MS11-066**](http://go.microsoft.com/fwlink/?linkid=221536)
</td>
<td style="border:1px solid black;">
[**MS11-068**](http://go.microsoft.com/fwlink/?linkid=223578)
</td>
<td style="border:1px solid black;">
[**MS11-069**](http://go.microsoft.com/fwlink/?linkid=221537)
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
Ninguna
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c01d9132-af5f-4039-8195-95f6761f2d0e)\*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=6ca837f7-eda1-4ebe-b48a-8c77f949ebfd)\*\*<sup>[1]</sup>
(KB2487367)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=da219735-b8b7-4f97-b8a8-7c253838de6b)\*\*\*  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2f7348c0-a036-4d86-b7bb-bd6810cdc834)\*\*  
(KB2539633)  
(Moderada)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)\*\*<sup>[1]</sup>
(KB2539636)  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=70797adb-d693-4102-9e7c-ba1ea8fb07d0)\*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=6ca837f7-eda1-4ebe-b48a-8c77f949ebfd)\*\*<sup>[1]</sup>
(KB2487367)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8e077af5-5823-4377-a997-44b022a694d8)\*\*\*  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2f7348c0-a036-4d86-b7bb-bd6810cdc834)\*\*  
(KB2539633)  
(Moderada)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)\*\*<sup>[1]</sup>
(KB2539636)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9babf81a-8b21-42ae-a65c-f414793516ab)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=6ca837f7-eda1-4ebe-b48a-8c77f949ebfd)<sup>[1]</sup>
(KB2487367)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=560efa6f-c956-47cb-a2f4-a1f45278b7cd)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2f7348c0-a036-4d86-b7bb-bd6810cdc834)  
(KB2539633)  
(Moderada)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)<sup>[1]</sup>
(KB2539636)  
(Moderada)
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Windows 7
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-064**](http://go.microsoft.com/fwlink/?linkid=221808)
</td>
<td style="border:1px solid black;">
[**MS11-065**](http://go.microsoft.com/fwlink/?linkid=221880)
</td>
<td style="border:1px solid black;">
[**MS11-066**](http://go.microsoft.com/fwlink/?linkid=221536)
</td>
<td style="border:1px solid black;">
[**MS11-068**](http://go.microsoft.com/fwlink/?linkid=223578)
</td>
<td style="border:1px solid black;">
[**MS11-069**](http://go.microsoft.com/fwlink/?linkid=221537)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=814bbdfa-7cbc-40e5-8ca3-8fed9d13ff00)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=6ca837f7-eda1-4ebe-b48a-8c77f949ebfd)<sup>[1]</sup>
(KB2487367)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=6c8dd72b-abf8-4e1f-aafc-777c1a3ef3db)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits únicamente:  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=b8c628c6-5dcc-4c8f-b379-e2249a44f12c)  
(KB2539634)  
(Moderada)  

Windows 7 para sistemas de 32 bits únicamente:  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)<sup>[1]</sup>
(KB2539636)  
(Moderada)  

Windows 7 para sistemas de 32 bits Service Pack 1 únicamente:  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=e1f84749-77bb-42bf-a539-fb647cacff8b)  
(KB2539635)  
(Moderada)  

Windows 7 para sistemas de 32 bits Service Pack 1 únicamente:  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)<sup>[1]</sup>
(KB2539636)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=085ee785-b6ad-4c68-835a-e17bc8f12a53)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=6ca837f7-eda1-4ebe-b48a-8c77f949ebfd)<sup>[1]</sup>
(KB2487367)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d90c07c1-3c07-4989-825c-fb8453541a0e)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 únicamente:  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=b8c628c6-5dcc-4c8f-b379-e2249a44f12c)  
(KB2539634)  
(Moderada)  

Windows 7 para sistemas x64 únicamente:  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)<sup>[1]</sup>
(KB2539636)  
(Moderada)  

Windows 7 para sistemas x64 Service Pack 1 únicamente:  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=e1f84749-77bb-42bf-a539-fb647cacff8b)  
(KB2539635)  
(Moderada)  

Windows 7 para sistemas x64 Service Pack 1 únicamente:  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)<sup>[1]</sup>
(KB2539636)  
(Moderada)
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Windows Server 2008 R2
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-064**](http://go.microsoft.com/fwlink/?linkid=221808)
</td>
<td style="border:1px solid black;">
[**MS11-065**](http://go.microsoft.com/fwlink/?linkid=221880)
</td>
<td style="border:1px solid black;">
[**MS11-066**](http://go.microsoft.com/fwlink/?linkid=221536)
</td>
<td style="border:1px solid black;">
[**MS11-068**](http://go.microsoft.com/fwlink/?linkid=223578)
</td>
<td style="border:1px solid black;">
[**MS11-069**](http://go.microsoft.com/fwlink/?linkid=221537)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=9fd2b4ba-d98e-4ad6-99f2-c471335042d3)\*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 únicamente:  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=6ca837f7-eda1-4ebe-b48a-8c77f949ebfd)<sup>[1]</sup>
(KB2487367)  
(Importante)  

Windows Server 2008 R2 para sistemas x64 Service Pack 1 únicamente:  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=6ca837f7-eda1-4ebe-b48a-8c77f949ebfd)\*<sup>[1]</sup>
(KB2487367)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=67cccd09-5b82-4546-884a-d2a9e2400820)\*\*\*  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 únicamente:  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=b8c628c6-5dcc-4c8f-b379-e2249a44f12c)\*  
(KB2539634)  
(Moderada)  

Windows Server 2008 R2 para sistemas x64 únicamente:  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)<sup>[1]</sup>
(KB2539636)  
(Moderada)  

Windows Server 2008 R2 para sistemas x64 Service Pack 1 únicamente:  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=e1f84749-77bb-42bf-a539-fb647cacff8b)\*  
(KB2539635)  
(Moderada)  

Windows Server 2008 R2 para sistemas x64 Service Pack 1 únicamente:  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)\*<sup>[1]</sup>
(KB2539636)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=93752c8f-5461-4e6f-9cab-6401b985ef17)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=6ca837f7-eda1-4ebe-b48a-8c77f949ebfd)<sup>[1]</sup>
(KB2487367)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=a1edf843-9a2a-4334-a95f-78e75a9b3ef1)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium únicamente:  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=b8c628c6-5dcc-4c8f-b379-e2249a44f12c)  
(KB2539634)  
(Moderada)  

Windows Server 2008 R2 para sistemas con Itanium únicamente:  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)<sup>[1]</sup>
(KB2539636)  
(Moderada)  

Windows Server 2008 R2 para sistemas con Itanium Service Pack 1 únicamente:  
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=e1f84749-77bb-42bf-a539-fb647cacff8b)  
(KB2539635)  
(Moderada)  

Windows Server 2008 R2 para sistemas con Itanium Service Pack 1 únicamente:  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=e2069b12-d78b-420c-84b7-46bba12827c8)<sup>[1]</sup>
(KB2539636)  
(Moderada)
</td>
</tr>
</table>
 
**Notaspara** **Windows Server 2008 y Windows Server 2008 R2**

**\*La instalación de Server** **Core** **está afectada.** Esta actualización se aplica, con la misma clasificación de gravedad, a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, independientemente de si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**\*\*La instalación de Server** **Core** **no está afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**\*\*\*La instalación de Server** **Core** **no está afectada.** La vulnerabilidad corregida por esta actualización no afecta a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2, tal como se ha indicado, cuando se ha instalado con la opción de instalación Server Core, incluso si los archivos afectados por esta vulnerabilidad puedan estar presentes en el sistema. No obstante, a los usuarios con los archivos afectados se les sigue ofreciendo esta actualización porque los archivos de actualización son más recientes (con números de versión más altos) que los que se encuentran actualmente en el sistema. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**Notas para MS11-066**

<sup>[1]</sup>**.NET Framework 4** **ClientProfile** **no está afectado.** Los paquetes redistribuibles de .NET Framework versión 4 están disponibles en dos perfiles: .NET Framework 4.0 y .NET Framework 4.0 Client Profile. .NET Framework 4.0 Client Profile es un subconjunto de .NET Framework 4.0. La vulnerabilidad corregida en esta actualización afecta solo a .NET Framework 4.0 y .no a NET Framework 4.0 Client Profile. Para obtener más información, vea el artículo de MSDN [Instalar .NET Framework](http://msdn.microsoft.com/es-es/library/5a4x27ek.aspx).

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

**Nota para MS11-069**

<sup>[1]</sup>**.NET Framework 4 y .NET Framework 4** **ClientProfile** **están afectados.** Los paquetes redistribuibles de .NET Framework versión 4 están disponibles en dos perfiles: .NET Framework 4.0 y .NET Framework 4.0 Client Profile. .NET Framework 4.0 Client Profile es un subconjunto de .NET Framework 4.0. La vulnerabilidad corregida en esta actualización afecta a .NET Framework 4.0 y .NET Framework 4.0 Client Profile. Para obtener más información, vea el artículo de MSDN [Instalar .NET Framework](http://msdn.microsoft.com/es-es/library/5a4x27ek.aspx).

#### Conjuntos de programas y software de Microsoft Office

 
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
Microsoft Visio
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-060**](http://go.microsoft.com/fwlink/?linkid=223425)
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
Microsoft Visio 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Visio 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=866d64b3-7147-4b5f-80fe-4d3317f140df)  
(KB2553009)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Visio 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft Visio 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a0eeabde-5a92-45ae-aef6-81b7bdb4e0cd)  
(KB2553010)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Visio 2010 y Microsoft Visio 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft Visio 2010 y Microsoft Visio 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=6da236c2-0ef5-4c13-8393-673b70298a77)  
(KB2553008)  
(Importante)  

[Microsoft Visio 2010 y Microsoft Visio 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=b7f5f2a9-116a-41ef-a19e-a7dd0947d2cb)  
(KB2553008)  
(Importante)
</td>
</tr>
</table>
 

#### Herramientas y software para desarrolladores de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr class="thead">
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
<th style="border:1px solid black;" >
</th>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Control de gráficos
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-066**](http://go.microsoft.com/fwlink/?linkid=221536)
</td>
<td style="border:1px solid black;">
[**MS11-067**](http://go.microsoft.com/fwlink/?linkid=223643)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
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
Control de gráficos para Microsoft .NET Framework 3.5 Service Pack 1
</td>
<td style="border:1px solid black;">
[Control de gráficos para Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=8a80cc03-0db9-4446-9ce6-159ad02cab52)  
(KB2500170)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Visual Studio y Microsoft Report Viewer
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-066**](http://go.microsoft.com/fwlink/?linkid=221536)
</td>
<td style="border:1px solid black;">
[**MS11-067**](http://go.microsoft.com/fwlink/?linkid=223643)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Visual Studio 2005 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Visual Studio 2005 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=59231988-5413-4238-a3aa-32a127871430)  
(KB2548826)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Paquete redistribuible de Microsoft Report Viewer 2005 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Paquete redistribuible de Microsoft Report Viewer 2005 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=28bf2ae0-9e21-4201-b7f1-a207abc2866f)  
(KB2579115)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS11-066**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://go.microsoft.com/fwlink/?linkid=69903). [TechNet Security Center](http://technet.microsoft.com/es-es/security/default.aspx) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://go.microsoft.com/fwlink/?linkid=85102), donde esta información también está disponible haciendo clic en "Últimas actualizaciones de seguridad".

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

**System** **Center** **Configuration** **Manager 2007**

La administración de actualizaciones de software de Configuration Manager 2007 simplifica la tarea compleja de entregar y administrar actualizaciones para los sistemas de TI en toda la empresa. Con Configuration Manager 2007, los administradores de TI pueden ofrecer actualizaciones de los productos de Microsoft a una serie de dispositivos, incluidos equipos de escritorio, portátiles, servidores y dispositivos móviles.

La evaluación automática de vulnerabilidades en Configuration Manager 2007 detecta las necesidades de actualizaciones e informa de las acciones recomendadas. La administración de actualizaciones de software en Configuration Manager 2007 se basa en Microsoft Windows Software Update Services (WSUS), una infraestructura de actualizaciones probada con la que están familiarizados los administradores de TI de todo el mundo. Para obtener más información acerca de cómo los administradores pueden usar Configuration Manager 2007 para implementar actualizaciones, vea [Administración de actualizaciones de software](http://www.microsoft.com/systemcenter/en/us/configuration-manager/cm-software-update-management.aspx). Para obtener más información acerca de Configuration Manager, visite [System Center Configuration Manager](http://www.microsoft.com/systemcenter/en/us/configuration-manager.aspx).

**Systems** **Management Server 2003**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales.

**Nota** System Management Server 2003 está fuera del soporte técnico general desde el 12 de enero de 2010. Para obtener más información acerca de los ciclos de vida de los productos, visite [Ciclo de vida del soporte técnico de Microsoft](http://support.microsoft.com/common/international.aspx?rdpath=dm;en-us;lifecycle). Ya está disponible la siguiente versión de SMS, System Center Configuration Manager 2007; vea la sección anterior, **System** Center Configuration Manager 2007.

Para obtener más información acerca de cómo los administradores pueden usar SMS 2003 para implementar actualizaciones de seguridad, vea [Escenarios y procedimientos para Microsoft Systems Management Server 2003: Administración de distribución de software y revisiones](http://www.microsoft.com/downloads/en/details.aspx?familyid=32f2bb4c-42f8-4b8d-844f-2553fd78049f&displaylang=en). Para obtener información acerca de SMS, visite [Microsoft Systems Management Server TechCenter](http://technet.microsoft.com/en-us/systemcenter/bb545936.aspx).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://www.microsoft.com/downloads/en/details.aspx?familyid=7bd3a16e-1899-4e0b-bb99-1320e816167d&displaylang=en)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet2.microsoft.com/windowsvista/en/library/4279e239-37a4-44aa-aec5-4e70fe39f9de1033.mspx?mfr=true) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Microsoft Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

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

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumeradas en [Asociados de Microsoft Active Protections Program (MAPP)](http://go.microsoft.com/fwlink/?linkid=215201).

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

-   Yngve N. Pettersen, de [Opera Software ASA](http://www.opera.com/), por informar de un problema descrito en MS11-057
-   [Lostmon Lords](http://lostmon.blogspot.com)
-   , por informar de un problema descrito en MS11-057
-   Makoto Shiotsuki, de [Security Professionals Network Inc.](http://www.sec-pro.net/), por informar de un problema descrito en MS11-057
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de TippingPoint, por informar de un problema descrito en MS11-057
-   Stephen Fewer, de [Harmony Security](http://www.harmonysecurity.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de dos problemas descritos en MS11-057
-   Michal Zalewski, de [Google Inc.](http://www.google.com/), por colaborar con nosotros en los cambios de defensa en profundidad incluidos en ms11-057
-   Grischa Zengel (Zengel Medizintechnik GmbH), por informar de un problema descrito en MS11-058
-   Linlin Zhao, de [Baidu Security Team](http://www.baidu.com), por informar de dos problemas descritos en MS11-060
-   Sven Taute, por informar de un problema descrito en MS11-061
-   Lufeng Li, de , por informar de un problema descrito en MS11-062
-   Alex Ionescu, de Winsider Seminars & Solutions Inc., por informar de un problema descrito en MS11-063
-   Nico Leidecker y James Forshaw, de Context Information Security, por informar de un problema descrito en MS11-066
-   Adam Bixby, de [Gotham Digital Science](http://www.gdssecurity.com/), por informar de un problema descrito en MS11-067
-   Zheng Wenbin, de [Qihoo 360 Security Center](http://www.360.cn/), por informar de un problema descrito en MS11-068
-   Michael J. Liu, por informar de un problema descrito en MS11-069

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Los clientes de Estados Unidos y Canadá pueden recibir soporte técnico del [soporte de seguridad](http://go.microsoft.com/fwlink/?linkid=21131) o en el teléfono 1-866-PCSAFETY. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de las opciones de asistencia disponibles, vea [Ayuda y soporte técnico de Microsoft](http://support.microsoft.com/).
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico internacional](http://go.microsoft.com/fwlink/?linkid=21155).

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (9 de agosto de 2011): Publicación del resumen del boletín.
-   V1.1 (10 de agosto de 2011): Para MS11-059, se ha corregido la información de requisito de reinicio en la sección **Resúmenes ejecutivos**. Para MS11-065, se ha corregido la nota clave del **índice de** **explotabilidad** para CVE-2011-1968. Para MS11-068, se ha revisado la notación de Server Core para Windows Server 2008 y Windows Server 2008 R2.
-   V1.2 (26 de octubre de 2011): Para MS11-066 y MS11-069, se ha corregido la aplicabilidad de la instalación de Server Core para .NET Framework 4.0 en Windows Server 2008 R2 para sistemas x64.

*Built at 2014-04-18T01:50:00Z-07:00*