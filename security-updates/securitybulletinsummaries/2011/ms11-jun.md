---
TOCTitle: 'MS11-JUN'
Title: Microsoft Security Bulletin Summary for junio 2011
ms:assetid: 'ms11-jun'
ms:contentKeyID: 61225426
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms11-jun(v=Security.10)'
---

Microsoft Security Bulletin Summary for junio 2011
==================================================

Publicado: martes, 14 de junio de 2011 | Actualizado: miércoles, 18 de enero de 2012

**Versión:** 3.1

Este resumen del boletín enumera los boletines de seguridad publicados para junio de 2011.

Con la publicación de los boletines de seguridad de junio de 2011, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 9 de junio de 2011. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar una conferencia en línea para atender las consultas de los clientes sobre estos boletines el 15 de junio de 2011, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de junio](https://msevents.microsoft.com/cui/webcasteventdetails.aspx?culture=en-us&eventid=1032455073&eventcategory=4). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, vea los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217214).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-038">MS11-038</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en la automatización OLE podría permitir la ejecución remota de código (2476490)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en la automatización de vinculación e incrustación de objetos (OLE) de Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario visita un sitio web que contiene una imagen WMF especialmente diseñada. No obstante, el atacante no podría en ningún caso obligar a los usuarios a visitar un sitio web. Por lo tanto, tendría que atraerlos a un sitio web malintencionado; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico o una solicitud de Instant Messenger.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-039">MS11-039</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en .NET Framework y Microsoft Silverlight podría permitir la ejecución remota de código (2514842)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft .NET Framework y Microsoft Silverlight. La vulnerabilidad podría permitir la ejecución remota de código en un sistema cliente si un usuario visita una página web especialmente diseñada mediante un explorador web que pueda ejecutar aplicaciones XAML del explorador (XBAP) o aplicaciones Silverlight. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos. La vulnerabilidad también podría permitir la ejecución remota de código en un sistema de servidor que ejecute IIS si dicho servidor permite el procesamiento de páginas ASP.NET y un atacante consigue cargar una página ASP.NET especialmente diseñada en el servidor y la ejecuta, como puede ser el caso de un escenario de hospedaje web. Esta vulnerabilidad también la podrían usar aplicaciones Windows .NET para omitir las restricciones de seguridad de acceso del código (CAS).</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Microsoft .NET Framework,<br />
Microsoft Silverlight</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-040">MS11-040</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el cliente firewall de Threat Management Gateway podría permitir la ejecución remota de código (2520426)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en el cliente de Microsoft Forefront Threat Management Gateway (TMG) 2010, que anteriormente se denominaba Cliente firewall de Microsoft Forefront Threat Management Gateway. La vulnerabilidad podría permitir la ejecución remota de código si un atacante aprovecha un equipo cliente para realizar solicitudes específicas en un sistema donde se use el cliente firewall de TMG.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Forefront Threat Management Gateway</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-041">MS11-041</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en los controladores en modo kernel de Windows podría permitir la ejecución remota de código (2525694)</strong> <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario obtiene acceso a un recurso compartido de red (o visita un sitio web que apunta a un recurso compartido de red) que contenga una fuente OpenType (OTF) especialmente diseñada. Sin embargo, el atacante no podría en ningún caso obligar al usuario a visitar el sitio web o tener acceso al recurso compartido de red. Por lo tanto, tendría que atraerlo al sitio web o al recurso compartido de red; por lo general, convenciéndole para que haga clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-042">MS11-042</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en el sistema de archivos distribuido podrían permitir la ejecución remota de código (2535512)</strong> <br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado en el sistema de archivos distribuido (DFS) de Microsoft. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un atacante envía una respuesta DFS especialmente diseñada a una solicitud DFS iniciada por el cliente. Un atacante que consiga aprovechar esta vulnerabilidad podría ejecutar código arbitrario y tomar el control completo de un sistema afectado. Los procedimientos recomendados para firewall y las configuraciones de firewall predeterminadas estándar pueden proteger a las redes de los ataques procedentes del exterior del perímetro de la empresa. Se recomienda que los sistemas conectados a Internet tengan expuesta la cantidad mínima de puertos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-043">MS11-043</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el cliente SMB podría permitir la ejecución remota de código (2536276)</strong> <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un atacante ha enviado una respuesta SMB especialmente diseñada a una solicitud SMB iniciada por el cliente. Para aprovechar la vulnerabilidad, un atacante debe convencer al usuario para que inicie una conexión SMB a un servidor SMB especialmente diseñado.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-044">MS11-044</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en .NET Framework podría permitir la ejecución remota de código (2538814)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública en Microsoft .NET Framework. La vulnerabilidad podría permitir la ejecución remota de código en un sistema cliente si un usuario visita una página web especialmente diseñada mediante un explorador web que pueda ejecutar aplicaciones XAML del explorador (XBAP). Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos. La vulnerabilidad también podría permitir la ejecución remota de código en un sistema de servidor que ejecute IIS si dicho servidor permite el procesamiento de páginas ASP.NET y un atacante consigue cargar una página ASP.NET especialmente diseñada en el servidor y la ejecuta, como puede ser el caso de un escenario de hospedaje web. Esta vulnerabilidad también la podrían usar aplicaciones Windows .NET para omitir las restricciones de seguridad de acceso del código (CAS).</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Microsoft .NET Framework</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-050">MS11-050</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (2530548)</strong> <br />
<br />
Esta actualización de seguridad resuelve once vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. La más grave de las vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un intruso que aprovechara cualquiera de estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario local. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-052">MS11-052</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el lenguaje de marcado vectorial podría permitir la ejecución remota de código (2544521)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en la implementación de Microsoft del lenguaje de marcado vectorial (VML). Esta actualización de seguridad se considera crítica para Internet Explorer 6, Internet Explorer 7 e Internet Explorer 8 en clientes Windows; y moderada para Internet Explorer 6, Internet Explorer 7 e Internet Explorer 8 en servidores Windows. Internet Explorer 9 no está afectado por la vulnerabilidad.<br />
<br />
La vulnerabilidad podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-037">MS11-037</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en MHTML podría permitir la divulgación de información (2544893)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública en el controlador de protocolo MHTML en Microsoft Windows. La vulnerabilidad podría permitir la divulgación de información si un usuario abre una dirección URL especialmente diseñada del sitio web de un atacante. Un atacante tendría que atraerlo al sitio web, por lo general, convenciéndole para que siga un vínculo de un mensaje de correo electrónico o de Instant Messenger.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Divulgación de información</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-045">MS11-045</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Excel podrían permitir la ejecución remota de código (2537146)</strong> <br />
<br />
Esta actualización de seguridad resuelve ocho vulnerabilidades de las que se ha informado de forma privada en Microsoft Office. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario abre un archivo de Excel especialmente diseñado. Un intruso que aprovechara cualquiera de estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario que ha iniciado sesión. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos. La instalación y configuración de Validación de documento de Office (OFV) para prevenir la apertura de archivos sospechosos bloquea las vías de ataque para aprovechar las vulnerabilidades descritas en CVE-2011-1272, CVE-2011-1273 y CVE-2011-1279. Microsoft Excel 2010 es el único afectado por la vulnerabilidad CVE-2011-1273 descrita en este boletín. La solución Microsoft Fix it automatizada, &quot;Deshabilitar la edición en Vista protegida para Excel 2010&quot;, disponible en el artículo 2501584 de Microsoft Knowledge Base, bloquea las vías de ataque para aprovechar CVE-2011-1273.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-046">MS11-046</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el controlador de función auxiliar podría permitir la elevación de privilegios (2503665)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública en el controlador de función auxiliar (AFD) de Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si un atacante inicia sesión en el sistema del usuario y ejecuta una aplicación especialmente diseñada. Para aprovechar la vulnerabilidad, un atacante debe tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-047">MS11-047</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Hyper-V podría permitir la denegación de servicio (2525835)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Windows Server 2008 Hyper-V y en Windows Server 2008 R2 Hyper-V. La vulnerabilidad podría permitir la denegación de servicio si se envía un paquete especialmente diseñado a VMBus por parte de un usuario autenticado en una de las máquinas virtuales invitadas que hospeda el servidor Hyper-V. Para aprovechar esta vulnerabilidad, un atacante debe tener unas credenciales de inicio de sesión válidas y ser capaz de enviar contenido especialmente diseñado desde una máquina virtual invitada. Los usuarios anónimos o los usuarios remotos no pueden aprovechar esta vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Denegación de servicio</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-048">MS11-048</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el servidor SMB podría permitir la denegación de servicio (2536275)</strong> <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la denegación de servicio si un atacante crea un paquete SMB especialmente diseñado y lo envía a un sistema afectado. Los procedimientos recomendados para firewall y las configuraciones de firewall predeterminadas estándar pueden proteger a las redes de los ataques procedentes del exterior del perímetro de la empresa que intentan aprovechar esta vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Denegación de servicio</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-049">MS11-049</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el Editor XML de Microsoft podría permitir la divulgación de información (2543893)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en el Editor XML de Microsoft. La vulnerabilidad podría permitir la divulgación de información si un usuario abre un archivo de detección de servicios web (.disco) en el software afectado que se enumera en este boletín. Es importante mencionar que la vulnerabilidad no permitirá al atacante ejecutar código o elevar directamente sus derechos de usuario, pero podría servir para producir información útil que pudiera usarse para tratar de sacar más provecho del sistema afectado.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Divulgación de información</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office,<br />
Microsoft SQL Server,<br />
Microsoft Visual Studio</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-051">MS11-051</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Inscripción en web de Servicios de Certificate Server de Active Directory podría permitir la elevación de privilegios (2518295)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Inscripción en web de Servicios de Certificate Server de Active Directory. Se trata de una vulnerabilidad de scripts de sitios (XSS) que podría permitir la elevación de privilegios, lo que permitiría que un atacante ejecutar comandos arbitrarios en el sitio en el contexto del usuario atacado. Un atacante que aprovechara esta vulnerabilidad debería enviar un vínculo especialmente diseñado y convencer a un usuario para que hiciera clic en él. Sin embargo, el atacante no podría en ningún caso obligar al usuario a visitar el sitio web. Por lo tanto, tendría que atraerlo al sitio web; por lo general, convenciéndole para que haga clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger que lleve al usuario al sitio web vulnerable.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-037">MS11-037</a></td>
<td style="border:1px solid black;">Vulnerabilidad de procesamiento de solicitudes con formato MIME en MHTML</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1894">CVE-2011-1894</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente<br />
<br />
Esta vulnerabilidad afecta a la divulgación de información</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-038">MS11-038</a></td>
<td style="border:1px solid black;">Vulnerabilidad de desbordamiento de la automatización OLE</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-0658">CVE-2011-0658</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-039">MS11-039</a></td>
<td style="border:1px solid black;">Vulnerabilidad de desplazamiento de matrices en .NET Framework</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-0664">CVE-2011-0664</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-040">MS11-040</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con el cliente firewall de TMG</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1889">CVE-2011-1889</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-041">MS11-041</a></td>
<td style="border:1px solid black;">Vulnerabilidad de validación de OTF en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1873">CVE-2011-1873</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">2</a> – Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">2</a> – Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-042">MS11-042</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con DFS</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1868">CVE-2011-1868</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-042">MS11-042</a></td>
<td style="border:1px solid black;">Vulnerabilidad de respuesta de referencia DFS</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1869">CVE-2011-1869</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-043">MS11-043</a></td>
<td style="border:1px solid black;">Vulnerabilidad de análisis de respuesta SMB</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1268">CVE-2011-1268</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-044">MS11-044</a></td>
<td style="border:1px solid black;">Vulnerabilidad de optimización JIT en .NET Framework</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1271">CVE-2011-1271</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">2</a> – Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">2</a> – Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-045">MS11-045</a></td>
<td style="border:1px solid black;">Vulnerabilidad de validación insuficiente de registros en Excel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1272">CVE-2011-1272</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-045">MS11-045</a></td>
<td style="border:1px solid black;">Vulnerabilidad de análisis incorrecto de registros en Excel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1273">CVE-2011-1273</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-045">MS11-045</a></td>
<td style="border:1px solid black;">Vulnerabilidad de acceso a matriz fuera de los límites en Excel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1274">CVE-2011-1274</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">2</a> – Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-045">MS11-045</a></td>
<td style="border:1px solid black;">Vulnerabilidad de sobrescritura del montón de memoria en Excel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1275">CVE-2011-1275</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">2</a> – Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-045">MS11-045</a></td>
<td style="border:1px solid black;">Vulnerabilidad de desbordamiento del búfer en Excel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1276">CVE-2011-1276</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-045">MS11-045</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Excel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1277">CVE-2011-1277</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-045">MS11-045</a></td>
<td style="border:1px solid black;">Vulnerabilidad de WriteAV en Excel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1278">CVE-2011-1278</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-045">MS11-045</a></td>
<td style="border:1px solid black;">Vulnerabilidad de WriteAV fuera de los límites en Excel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1279">CVE-2011-1279</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-046">MS11-046</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en el controlador de función auxiliar</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1249">CVE-2011-1249</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente<br />
<br />
Se trata de una vulnerabilidad de elevación de privilegios</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-047">MS11-047</a></td>
<td style="border:1px solid black;">Vulnerabilidad de DoS persistente en VMBus</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1872">CVE-2011-1872</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-048">MS11-048</a></td>
<td style="border:1px solid black;">Vulnerabilidad de análisis de solicitudes en SMB</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1267">CVE-2011-1267</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-049">MS11-049</a></td>
<td style="border:1px solid black;">Vulnerabilidad de resolución de entidades XML externas</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1280">CVE-2011-1280</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-050">MS11-050</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con el tratamiento de propiedades de vínculo</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1250">CVE-2011-1250</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">2</a> – Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-050">MS11-050</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con la manipulación de DOM</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1251">CVE-2011-1251</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-050">MS11-050</a></td>
<td style="border:1px solid black;">Vulnerabilidad de divulgación de información de toStaticHTML</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1252">CVE-2011-1252</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> – Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-050">MS11-050</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con la operación de arrastrar y colocar</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1254">CVE-2011-1254</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-050">MS11-050</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con el elemento de tiempo</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1255">CVE-2011-1255</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-050">MS11-050</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con la modificación de DOM</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1256">CVE-2011-1256</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">2</a> – Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-050">MS11-050</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con el diseño HTML</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1260">CVE-2011-1260</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-050">MS11-050</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con los objetos de selección</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1261">CVE-2011-1261</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-050">MS11-050</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con el redireccionamiento de HTTP</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1262">CVE-2011-1262</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">2</a> – Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-051">MS11-051</a></td>
<td style="border:1px solid black;">Vulnerabilidad de Servicios de Certificate Server de Active Directory</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1264">CVE-2011-1264</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de elevación de privilegios</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-052">MS11-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con VML</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1266">CVE-2011-1266</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
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
<th style="border:1px solid black;" >
</th>
</tr>
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
[**MS11-038**](http://go.microsoft.com/fwlink/?linkid=212284)
</td>
<td style="border:1px solid black;">
[**MS11-039**](http://go.microsoft.com/fwlink/?linkid=212287)
</td>
<td style="border:1px solid black;">
[**MS11-041**](http://go.microsoft.com/fwlink/?linkid=217499)
</td>
<td style="border:1px solid black;">
[**MS11-042**](http://go.microsoft.com/fwlink/?linkid=215838)
</td>
<td style="border:1px solid black;">
[**MS11-043**](http://go.microsoft.com/fwlink/?linkid=215841)
</td>
<td style="border:1px solid black;">
[**MS11-044**](http://go.microsoft.com/fwlink/?linkid=216436)
</td>
<td style="border:1px solid black;">
[**MS11-050**](http://go.microsoft.com/fwlink/?linkid=217212)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=2371079f-fb20-4fd5-999e-e73f3701818c)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=686e5192-63e4-410e-b653-2cfddd5b409f)  
(KB2478656)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=3db8a718-4441-4e1a-889f-abcc4bde1125)  
(KB2478658)  
(Crítica)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c72635e4-c733-4fa1-9db0-75de6ead9e1c)<sup>[1]</sup>
(KB2478663)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=67a25abd-f43c-4b01-b507-a109b739238f)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=492310d3-bbb4-4fff-b5fe-3470c17e7681)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=960f8920-906b-48a8-8700-94f09babc628)  
(KB2518864)  
(Sin clasificación de gravedad<sup>[2]</sup>)  

[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=c7e115a1-486b-4a2b-a7d6-42c4018fc02d)  
(KB2530095)  
(Crítica)  

[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=960f8920-906b-48a8-8700-94f09babc628)  
(KB2518864)  
(Crítica)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7afba05-974f-48f8-b600-9e131ceb7951)<sup>[1]</sup>
(KB2518870)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=26ec66af-9727-4423-90da-012ed5b30856)  
(Crítica)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=4203a59a-a809-45db-a234-fef0ff5063f9)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=4a49ec89-2a8f-41d9-8f0b-ee57fdf21f50)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b53d6631-4ded-48f5-a503-925b89b322b2)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=686e5192-63e4-410e-b653-2cfddd5b409f)  
(KB2478656)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=3db8a718-4441-4e1a-889f-abcc4bde1125)  
(KB2478658)  
(Crítica)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c72635e4-c733-4fa1-9db0-75de6ead9e1c)<sup>[1]</sup>
(KB2478663)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=035d5115-54b6-41d3-b9f0-890041ead178)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=af6b7627-c462-45fe-8948-70da37e60659)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e10a4c3c-2ef8-4cfc-ac9b-4d97bfa79ac1)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=960f8920-906b-48a8-8700-94f09babc628)  
(KB2518864)  
(Sin clasificación de gravedad<sup>[2]</sup>)  

[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=c7e115a1-486b-4a2b-a7d6-42c4018fc02d)  
(KB2530095)  
(Crítica)  

[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=960f8920-906b-48a8-8700-94f09babc628)  
(KB2518864)  
(Crítica)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7afba05-974f-48f8-b600-9e131ceb7951)<sup>[1]</sup>
(KB2518870)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=f6e05fef-ee8c-44ff-a106-d7b8659c8d91)  
(Crítica)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=9fc734db-a177-43d2-a74a-b1fe6ea6f779)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=4e4e18a4-97dc-4c5e-a078-8466913aa29e)  
(Crítica)
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
[**MS11-038**](http://go.microsoft.com/fwlink/?linkid=212284)
</td>
<td style="border:1px solid black;">
[**MS11-039**](http://go.microsoft.com/fwlink/?linkid=212287)
</td>
<td style="border:1px solid black;">
[**MS11-041**](http://go.microsoft.com/fwlink/?linkid=217499)
</td>
<td style="border:1px solid black;">
[**MS11-042**](http://go.microsoft.com/fwlink/?linkid=215838)
</td>
<td style="border:1px solid black;">
[**MS11-043**](http://go.microsoft.com/fwlink/?linkid=215841)
</td>
<td style="border:1px solid black;">
[**MS11-044**](http://go.microsoft.com/fwlink/?linkid=216436)
</td>
<td style="border:1px solid black;">
[**MS11-050**](http://go.microsoft.com/fwlink/?linkid=217212)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7e6ff410-4552-4687-81ab-83d9c91f8af5)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=686e5192-63e4-410e-b653-2cfddd5b409f)  
(KB2478656)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=3db8a718-4441-4e1a-889f-abcc4bde1125)  
(KB2478658)  
(Crítica)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c72635e4-c733-4fa1-9db0-75de6ead9e1c)<sup>[1]</sup>
(KB2478663)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3aa8f1bc-07de-451a-8244-1733247e6f2e)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2719e0fb-3cfd-47b2-906d-3e07b0e3c978)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=960f8920-906b-48a8-8700-94f09babc628)  
(KB2518864)  
(Sin clasificación de gravedad<sup>[2]</sup>)  

[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=c7e115a1-486b-4a2b-a7d6-42c4018fc02d)  
(KB2530095)  
(Crítica)  

[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=960f8920-906b-48a8-8700-94f09babc628)  
(KB2518864)  
(Crítica)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7afba05-974f-48f8-b600-9e131ceb7951)<sup>[1]</sup>
(KB2518870)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=638f6dd6-bea0-4356-b23a-45e865a6b28b)  
(Moderada)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=a3bd0012-4a45-4f96-8a51-3ff1f85d1e37)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=19557984-5088-44cc-b5ba-9bab33df8e7e)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9c1a539f-1472-4394-8354-bd549d8332e0)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=686e5192-63e4-410e-b653-2cfddd5b409f)  
(KB2478656)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=3db8a718-4441-4e1a-889f-abcc4bde1125)  
(KB2478658)  
(Crítica)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c72635e4-c733-4fa1-9db0-75de6ead9e1c)<sup>[1]</sup>
(KB2478663)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4aa8c003-0353-4a5b-8aea-c01a103af393)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e9018258-5a72-47a1-8584-3d1aa52317c3)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c962531e-f580-4195-989b-cf348cc96fa7)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=960f8920-906b-48a8-8700-94f09babc628)  
(KB2518864)  
(Sin clasificación de gravedad<sup>[2]</sup>)  

[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=c7e115a1-486b-4a2b-a7d6-42c4018fc02d)  
(KB2530095)  
(Crítica)  

[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=960f8920-906b-48a8-8700-94f09babc628)  
(KB2518864)  
(Crítica)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7afba05-974f-48f8-b600-9e131ceb7951)<sup>[1]</sup>
(KB2518870)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=ce616970-343d-49f1-994d-4269b9a11448)  
(Moderada)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=70ece3b4-e5bb-469c-bfef-c8310681f5a7)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=c92d94c5-5e8f-45aa-a24a-f4d0efd93732)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=c194dd35-b9db-44a5-a252-38f9f803802f)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=686e5192-63e4-410e-b653-2cfddd5b409f)  
(KB2478656)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=3db8a718-4441-4e1a-889f-abcc4bde1125)  
(KB2478658)  
(Crítica)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c72635e4-c733-4fa1-9db0-75de6ead9e1c)<sup>[1]</sup>
(KB2478663)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=2e07b5fa-c9fa-495b-9352-c07ce46a7e8b)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=96309c49-4822-4c47-b364-2ba65327cac5)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=ea18a916-03cf-4eac-bacc-ceb006491f24)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=960f8920-906b-48a8-8700-94f09babc628)  
(KB2518864)  
(Sin clasificación de gravedad<sup>[2]</sup>)  

[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=c7e115a1-486b-4a2b-a7d6-42c4018fc02d)  
(KB2530095)  
(Crítica)  

[Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=960f8920-906b-48a8-8700-94f09babc628)  
(KB2518864)  
(Crítica)  

[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7afba05-974f-48f8-b600-9e131ceb7951)<sup>[1]</sup>
(KB2518870)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=f58ebc9e-00e1-413c-8076-d7a44003d0c7)  
(Moderada)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=80231a27-b37c-4101-a34f-19a26a040836)  
(Crítica)
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
[**MS11-038**](http://go.microsoft.com/fwlink/?linkid=212284)
</td>
<td style="border:1px solid black;">
[**MS11-039**](http://go.microsoft.com/fwlink/?linkid=212287)
</td>
<td style="border:1px solid black;">
[**MS11-041**](http://go.microsoft.com/fwlink/?linkid=217499)
</td>
<td style="border:1px solid black;">
[**MS11-042**](http://go.microsoft.com/fwlink/?linkid=215838)
</td>
<td style="border:1px solid black;">
[**MS11-043**](http://go.microsoft.com/fwlink/?linkid=215841)
</td>
<td style="border:1px solid black;">
[**MS11-044**](http://go.microsoft.com/fwlink/?linkid=216436)
</td>
<td style="border:1px solid black;">
[**MS11-050**](http://go.microsoft.com/fwlink/?linkid=217212)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista Service Pack 1 y Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f33c9e54-c2e5-498d-a798-5bbfe9e4249c)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 1 solamente: [Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=2eabacce-394f-4b9a-8306-0875ca19a3a9)  
(KB2478657)  
(Crítica)  

Windows Vista Service Pack 1 solamente: [Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=55fd3254-7e59-4cf9-afa8-45ae66bc7390)  
(KB2478659)  
(Crítica)  

Windows Vista Service Pack 2 únicamente: [Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=afa11dda-a543-42a7-b997-5292fd869a8b)  
(KB2478660)  
(Crítica)  

Windows Vista Service Pack 1 y Windows Vista Service Pack 2: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c72635e4-c733-4fa1-9db0-75de6ead9e1c)<sup>[1]</sup>
(KB2478663)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=aded8f20-479d-40c1-9560-c0581c6f77a2)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a62edfd8-9016-4bb5-bf48-885498fa0042)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 1 solamente: [Microsoft .NET Framework 2.0 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5f7092fe-079d-4175-b8b7-412f259ff7e4)  
(KB2518863)  
(Sin clasificación de gravedad<sup>[2]</sup>)  

Windows Vista Service Pack 1 solamente: [Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=80423e37-0a54-413d-b44a-41c68c2030b8)  
(KB2518865)  
(Sin clasificación de gravedad<sup>[2]</sup>)  

Windows Vista Service Pack 1 solamente: [Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=5f7092fe-079d-4175-b8b7-412f259ff7e4)  
(KB2518863)  
(Crítica)  

Windows Vista Service Pack 1 solamente: [Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=80423e37-0a54-413d-b44a-41c68c2030b8)  
(KB2518865)  
(Crítica)  

Windows Vista Service Pack 2 únicamente: [Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1e3ca981-5565-41a8-ab5e-941c92e74c7d)  
(KB2518866)  
(Sin clasificación de gravedad<sup>[2]</sup>)  

Windows Vista Service Pack 2 únicamente: [Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1e3ca981-5565-41a8-ab5e-941c92e74c7d)  
(KB2518866)  
(Crítica)  

Windows Vista Service Pack 1 y Windows Vista Service Pack 2: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7afba05-974f-48f8-b600-9e131ceb7951)<sup>[1]</sup>
(KB2518870)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=fea735a8-032b-4fa6-8337-1fa411df0b88)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=4cddfc68-eff6-4587-8607-63307d039489)  
(Crítica)  
Windows Vista Service Pack 2 únicamente: [Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=392316fc-f531-469c-aa60-4ecf061a5354)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4566528f-62ee-4d78-b3af-131a7cc15e1f)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 1 solamente: [Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=2eabacce-394f-4b9a-8306-0875ca19a3a9)  
(KB2478657)  
(Crítica)  

Windows Vista x64 Edition Service Pack 1 solamente: [Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=55fd3254-7e59-4cf9-afa8-45ae66bc7390)  
(KB2478659)  
(Crítica)  

Windows Vista x64 Edition Service Pack 2 únicamente: [Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=afa11dda-a543-42a7-b997-5292fd869a8b)  
(KB2478660)  
(Crítica)  

Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c72635e4-c733-4fa1-9db0-75de6ead9e1c)<sup>[1]</sup>
(KB2478663)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a519a5d7-bfe3-4e53-99e9-d85f7e34237f)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=962cb40c-680c-4c37-98d4-ca9789ca7270)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=cb561ba6-af4d-40cc-947c-923f9cca9a7e)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 1 solamente: [Microsoft .NET Framework 2.0 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5f7092fe-079d-4175-b8b7-412f259ff7e4)  
(KB2518863)  
(Sin clasificación de gravedad<sup>[2]</sup>)  

Windows Vista x64 Edition Service Pack 1 solamente: [Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=80423e37-0a54-413d-b44a-41c68c2030b8)  
(KB2518865)  
(Sin clasificación de gravedad<sup>[2]</sup>)  

Windows Vista x64 Edition Service Pack 1 solamente: [Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=5f7092fe-079d-4175-b8b7-412f259ff7e4)  
(KB2518863)  
(Crítica)  

Windows Vista x64 Edition Service Pack 1 solamente: [Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=80423e37-0a54-413d-b44a-41c68c2030b8)  
(KB2518865)  
(Crítica)  

Windows Vista x64 Edition Service Pack 2 únicamente: [Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1e3ca981-5565-41a8-ab5e-941c92e74c7d)  
(KB2518866)  
(Sin clasificación de gravedad<sup>[2]</sup>)  

Windows Vista x64 Edition Service Pack 2 únicamente: [Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1e3ca981-5565-41a8-ab5e-941c92e74c7d)  
(KB2518866)  
(Crítica)  

Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7afba05-974f-48f8-b600-9e131ceb7951)<sup>[1]</sup>
(KB2518870)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=49dcb47b-3c79-4f69-ba07-f471304c16e2)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=e0a8fbac-2c31-4cf8-9967-6171edabd560)  
(Crítica)  
Windows Vista x64 Edition Service Pack 2 únicamente: [Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=44b2aa73-c318-47ac-ad87-0d24afd9cdd7)  
(Crítica)
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
[**MS11-038**](http://go.microsoft.com/fwlink/?linkid=212284)
</td>
<td style="border:1px solid black;">
[**MS11-039**](http://go.microsoft.com/fwlink/?linkid=212287)
</td>
<td style="border:1px solid black;">
[**MS11-041**](http://go.microsoft.com/fwlink/?linkid=217499)
</td>
<td style="border:1px solid black;">
[**MS11-042**](http://go.microsoft.com/fwlink/?linkid=215838)
</td>
<td style="border:1px solid black;">
[**MS11-043**](http://go.microsoft.com/fwlink/?linkid=215841)
</td>
<td style="border:1px solid black;">
[**MS11-044**](http://go.microsoft.com/fwlink/?linkid=216436)
</td>
<td style="border:1px solid black;">
[**MS11-050**](http://go.microsoft.com/fwlink/?linkid=217212)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=0c9614d9-6f61-463d-b1fa-bd5eb2c1a5c5)\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits únicamente: [Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=2eabacce-394f-4b9a-8306-0875ca19a3a9)\*\*  
(KB2478657)  
(Crítica)  

Windows Server 2008 para sistemas de 32 bits únicamente: [Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=55fd3254-7e59-4cf9-afa8-45ae66bc7390)\*\*  
(KB2478659)  
(Crítica)  

Windows Server 2008 para sistemas de 32 bits Service Pack 2 únicamente: [Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=afa11dda-a543-42a7-b997-5292fd869a8b)\*\*  
(KB2478660)  
(Crítica)  

Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c72635e4-c733-4fa1-9db0-75de6ead9e1c)\*\*<sup>[1]</sup>
(KB2478663)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8ebfa067-0236-4454-8605-df1b99742f90)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8ab9679e-6a69-4ca3-9210-7ca4fb1980c2)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits únicamente: [Microsoft .NET Framework 2.0 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5f7092fe-079d-4175-b8b7-412f259ff7e4)\*\*  
(KB2518863)  
(Sin clasificación de gravedad<sup>[2]</sup>)  

Windows Server 2008 para sistemas de 32 bits únicamente: [Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=80423e37-0a54-413d-b44a-41c68c2030b8)\*\*  
(KB2518865)  
(Sin clasificación de gravedad<sup>[2]</sup>)  

Windows Server 2008 para sistemas de 32 bits únicamente: [Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=5f7092fe-079d-4175-b8b7-412f259ff7e4)\*\*  
(KB2518863)  
(Crítica)  

Windows Server 2008 para sistemas de 32 bits únicamente: [Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=80423e37-0a54-413d-b44a-41c68c2030b8)\*\*  
(KB2518865)  
(Crítica)  

Windows Server 2008 para sistemas de 32 bits Service Pack 2 únicamente: [Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1e3ca981-5565-41a8-ab5e-941c92e74c7d)\*\*  
(KB2518866)  
(Crítica)  

Windows Server 2008 para sistemas de 32 bits Service Pack 2 únicamente: [Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1e3ca981-5565-41a8-ab5e-941c92e74c7d)\*\*  
(KB2518866)  
(Crítica)  

Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7afba05-974f-48f8-b600-9e131ceb7951)\*\*<sup>[1]</sup>
(KB2518870)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=b6547ff0-b059-495d-8816-bb094ac11be7)\*\*  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=c9650c47-ac52-433d-b409-ce1cfe8d3e87)\*\*  
(Crítica)  
Windows Server 2008 para sistemas de 32 bits Service Pack 2 únicamente: [Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=7f9b1ba2-8247-494b-990c-f62003188c5a)\*\*  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=36698775-0e4e-4980-ae4c-43542de424ca)\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 únicamente: [Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=2eabacce-394f-4b9a-8306-0875ca19a3a9)\*\*  
(KB2478657)  
(Crítica)  

Windows Server 2008 para sistemas x64 únicamente: [Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=55fd3254-7e59-4cf9-afa8-45ae66bc7390)\*\*  
(KB2478659)  
(Crítica)  

Windows Server 2008 para sistemas x64 Service Pack 2 únicamente: [Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=afa11dda-a543-42a7-b997-5292fd869a8b)\*\*  
(KB2478660)  
(Crítica)  

Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c72635e4-c733-4fa1-9db0-75de6ead9e1c)\*\*<sup>[1]</sup>
(KB2478663)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=cd8f3713-b408-4db6-aecd-7eed2176a715)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f1d76b82-9996-4d08-894b-9c16a4b3bb1e)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=22c63fc3-2c5a-4e50-9026-2e04a6e74210)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 únicamente: [Microsoft .NET Framework 2.0 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5f7092fe-079d-4175-b8b7-412f259ff7e4)\*\*  
(KB2518863)  
(Sin clasificación de gravedad<sup>[2]</sup>)  

Windows Server 2008 para sistemas x64 únicamente: [Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=80423e37-0a54-413d-b44a-41c68c2030b8)\*\*  
(KB2518865)  
(Sin clasificación de gravedad<sup>[2]</sup>)  

Windows Server 2008 para sistemas x64 únicamente: [Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=5f7092fe-079d-4175-b8b7-412f259ff7e4)\*\*  
(KB2518863)  
(Crítica)  

Windows Server 2008 para sistemas x64 únicamente: [Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=80423e37-0a54-413d-b44a-41c68c2030b8)\*\*  
(KB2518865)  
(Crítica)  

Windows Server 2008 para sistemas x64 Service Pack 2 únicamente: [Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1e3ca981-5565-41a8-ab5e-941c92e74c7d)\*\*  
(KB2518866)  
(Crítica)  

Windows Server 2008 para sistemas x64 Service Pack 2 únicamente: [Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1e3ca981-5565-41a8-ab5e-941c92e74c7d)\*\*  
(KB2518866)  
(Crítica)  

Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7afba05-974f-48f8-b600-9e131ceb7951)\*\*<sup>[1]</sup>
(KB2518870)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=feff3364-4bfd-45f5-99da-9192b47ef5d4)\*\*  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=7dff9f08-19cb-41dd-a315-84c1dac81510)\*\*  
(Crítica)  
Windows Server 2008 para sistemas x64 Service Pack 2 únicamente: [Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=fdf88a52-c099-44eb-95a0-650129c0e678)\*\*  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3edb613f-5bf0-4e28-9835-4afbb6ef0e01)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium únicamente: [Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=2eabacce-394f-4b9a-8306-0875ca19a3a9)  
(KB2478657)  
(Crítica)  

Windows Server 2008 para sistemas con Itanium únicamente: [Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=55fd3254-7e59-4cf9-afa8-45ae66bc7390)  
(KB2478659)  
(Crítica)  

Windows Server 2008 para sistemas con Itanium Service Pack 2 únicamente: [Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=afa11dda-a543-42a7-b997-5292fd869a8b)  
(KB2478660)  
(Crítica)  

Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c72635e4-c733-4fa1-9db0-75de6ead9e1c)<sup>[1]</sup>
(KB2478663)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5a61f888-c81e-4b8a-8932-2fe67df4b2ad)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f80c89c6-27ab-4f6a-afad-9c8e92cbbce4)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5bb889de-8ff6-4587-8ef9-ffb13e8d60fd)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium únicamente: [Microsoft .NET Framework 2.0 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5f7092fe-079d-4175-b8b7-412f259ff7e4)  
(KB2518863)  
(Sin clasificación de gravedad<sup>[2]</sup>)  

Windows Server 2008 para sistemas con Itanium únicamente: [Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=80423e37-0a54-413d-b44a-41c68c2030b8)  
(KB2518865)  
(Sin clasificación de gravedad<sup>[2]</sup>)  

Windows Server 2008 para sistemas con Itanium únicamente: [Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=5f7092fe-079d-4175-b8b7-412f259ff7e4)  
(KB2518863)  
(Crítica)  

Windows Server 2008 para sistemas con Itanium únicamente: [Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=80423e37-0a54-413d-b44a-41c68c2030b8)  
(KB2518865)  
(Crítica)  

Windows Server 2008 para sistemas con Itanium Service Pack 2 únicamente: [Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1e3ca981-5565-41a8-ab5e-941c92e74c7d)  
(KB2518866)  
(Crítica)  

Windows Server 2008 para sistemas con Itanium Service Pack 2 únicamente: [Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1e3ca981-5565-41a8-ab5e-941c92e74c7d)  
(KB2518866)  
(Crítica)  

Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7afba05-974f-48f8-b600-9e131ceb7951)<sup>[1]</sup>
(KB2518870)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=d81a9219-da95-4fbf-af7f-898f553b0572)  
(Crítica)
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
[**MS11-038**](http://go.microsoft.com/fwlink/?linkid=212284)
</td>
<td style="border:1px solid black;">
[**MS11-039**](http://go.microsoft.com/fwlink/?linkid=212287)
</td>
<td style="border:1px solid black;">
[**MS11-041**](http://go.microsoft.com/fwlink/?linkid=217499)
</td>
<td style="border:1px solid black;">
[**MS11-042**](http://go.microsoft.com/fwlink/?linkid=215838)
</td>
<td style="border:1px solid black;">
[**MS11-043**](http://go.microsoft.com/fwlink/?linkid=215841)
</td>
<td style="border:1px solid black;">
[**MS11-044**](http://go.microsoft.com/fwlink/?linkid=216436)
</td>
<td style="border:1px solid black;">
[**MS11-050**](http://go.microsoft.com/fwlink/?linkid=217212)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=50ae36ff-2406-48a4-97cc-12782b6d30ac)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits únicamente: [Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=9720a317-ca4c-4a47-b99c-2c66301e62c6)  
(KB2478661)  
(Crítica)  

Windows 7 para sistemas de 32 bits Service Pack 1 únicamente: [Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=c8152a18-0367-4c00-a3c7-669325a899f4)  
(KB2478662)  
(Crítica)  

Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c72635e4-c733-4fa1-9db0-75de6ead9e1c)<sup>[1]</sup>
(KB2478663)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=9de1bf5d-6f25-496d-bc44-a32c5e8920fe)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=19a15098-1754-4536-a9ca-ff07d16464b7)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits únicamente: [Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=bff13134-ed84-4370-beb4-340c340a5d98)  
(KB2518867)  
(Crítica)  

Windows 7 para sistemas de 32 bits Service Pack 1 únicamente: [Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=dab623bf-d23d-42a9-9e74-ae75d779b980)  
(KB2518869)  
(Crítica)  

Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7afba05-974f-48f8-b600-9e131ceb7951)<sup>[1]</sup>
(KB2518870)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=91b98f02-a09e-48f1-9f78-a949f7268542)  
(Crítica)  

[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=79f846da-3b17-43c9-9016-a055c2c56975)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1241f0f8-a5c7-420a-a5b7-b6c3caa9e5e2)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 únicamente: [Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=9720a317-ca4c-4a47-b99c-2c66301e62c6)  
(KB2478661)  
(Crítica)  

Windows 7 para sistemas x64 Service Pack 1 únicamente: [Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=c8152a18-0367-4c00-a3c7-669325a899f4)  
(KB2478662)  
(Crítica)  

Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c72635e4-c733-4fa1-9db0-75de6ead9e1c)<sup>[1]</sup>
(KB2478663)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=e7f52b13-5b3d-438c-ae14-86da50c8b67a)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=50d1c677-57aa-4e3f-bdfc-6f01b5d3bfe2)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b449f23e-b3df-46e5-bfe3-98268d20ad54)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 únicamente: [Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=bff13134-ed84-4370-beb4-340c340a5d98)  
(KB2518867)  
(Crítica)  

Windows 7 para sistemas x64 Service Pack 1 únicamente: [Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=dab623bf-d23d-42a9-9e74-ae75d779b980)  
(KB2518869)  
(Crítica)  

Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7afba05-974f-48f8-b600-9e131ceb7951)<sup>[1]</sup>
(KB2518870)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=264107cc-68b4-401c-82f7-de64b535c18d)  
(Crítica)  

[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=e87a09f2-b755-48ef-9b85-fc78d0bfce43)  
(Crítica)
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
[**MS11-038**](http://go.microsoft.com/fwlink/?linkid=212284)
</td>
<td style="border:1px solid black;">
[**MS11-039**](http://go.microsoft.com/fwlink/?linkid=212287)
</td>
<td style="border:1px solid black;">
[**MS11-041**](http://go.microsoft.com/fwlink/?linkid=217499)
</td>
<td style="border:1px solid black;">
[**MS11-042**](http://go.microsoft.com/fwlink/?linkid=215838)
</td>
<td style="border:1px solid black;">
[**MS11-043**](http://go.microsoft.com/fwlink/?linkid=215841)
</td>
<td style="border:1px solid black;">
[**MS11-044**](http://go.microsoft.com/fwlink/?linkid=216436)
</td>
<td style="border:1px solid black;">
[**MS11-050**](http://go.microsoft.com/fwlink/?linkid=217212)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=8181c359-cd79-438a-87be-093b363d0b04)\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 únicamente: [Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=9720a317-ca4c-4a47-b99c-2c66301e62c6)\*  
(KB2478661)  
(Crítica)  

Windows Server 2008 R2 para sistemas x64 únicamente: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c72635e4-c733-4fa1-9db0-75de6ead9e1c)<sup>[1]</sup>
(KB2478663)  
(Crítica)  

Windows Server 2008 R2 para sistemas x64 Service Pack 1 únicamente: [Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=c8152a18-0367-4c00-a3c7-669325a899f4)\*  
(KB2478662)  
(Crítica)  

Windows Server 2008 R2 para sistemas x64 Service Pack 1 únicamente: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c72635e4-c733-4fa1-9db0-75de6ead9e1c)\*<sup>[1]</sup>
(KB2478663)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b77e5be6-d3eb-4e3a-9be2-831578f0447c)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=9d66b1e7-dbf9-4475-a973-49fb85557eca)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=06008192-3cac-477b-a913-83eed39d8718)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 únicamente: [Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=bff13134-ed84-4370-beb4-340c340a5d98)\*  
(KB2518867)  
(Crítica)  

Windows Server 2008 R2 para sistemas x64 únicamente: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7afba05-974f-48f8-b600-9e131ceb7951)<sup>[1]</sup>
(KB2518870)  
(Crítica)  

Windows Server 2008 R2 para sistemas x64 Service Pack 1 únicamente: [Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=dab623bf-d23d-42a9-9e74-ae75d779b980)\*  
(KB2518869)  
(Crítica)  

Windows Server 2008 R2 para sistemas x64 Service Pack 1 únicamente: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7afba05-974f-48f8-b600-9e131ceb7951)\*<sup>[1]</sup>
(KB2518870)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=8b18e6f9-96b8-4dec-bcd0-d71f1bac3eb0)\*\*  
(Crítica)  

[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=81814b15-ebdf-4817-932b-5ea7a37fa6ed)\*\*  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=6b63a1eb-445a-4cd3-b357-9a1dd82d7a35)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium únicamente: [Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=9720a317-ca4c-4a47-b99c-2c66301e62c6)  
(KB2478661)  
(Crítica)  

Windows Server 2008 R2 para sistemas con Itanium Service Pack 1 únicamente: [Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=c8152a18-0367-4c00-a3c7-669325a899f4)  
(KB2478662)  
(Crítica)  

Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=c72635e4-c733-4fa1-9db0-75de6ead9e1c)<sup>[1]</sup>
(KB2478663)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=c00a33bc-c874-4693-b0f7-5034c5df9424)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=3c8455f1-b8a0-4ba2-84a2-043d25ef75c5)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=93a32bd9-7e67-4ace-8c45-116f91b032f9)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium únicamente: [Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=bff13134-ed84-4370-beb4-340c340a5d98)  
(KB2518867)  
(Crítica)  

Windows Server 2008 R2 para sistemas con Itanium Service Pack 1 únicamente: [Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=dab623bf-d23d-42a9-9e74-ae75d779b980)  
(KB2518869)  
(Crítica)  

Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1: [Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=f7afba05-974f-48f8-b600-9e131ceb7951)<sup>[1]</sup>
(KB2518870)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=ab2406a8-06f7-4f88-9af4-dc136d64bc35)  
(Crítica)
</td>
</tr>
</table>
 
**Notas para Windows Server 2008 y Windows Server 2008 R2**

**\*La instalación de Server Core está afectada.** Esta actualización se aplica, con la misma clasificación de gravedad, a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, independientemente de si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**\*\*La instalación de Server Core no está afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**Notas para MS11-039**

<sup>[1]</sup>**.NET Framework 4.0 y .NET Framework 4.0 Client Profile están afectados.** Los paquetes redistribuibles de .NET Framework versión 4 están disponibles en dos perfiles: .NET Framework 4.0 y .NET Framework 4.0 Client Profile. .NET Framework 4.0 Client Profile es un subconjunto de .NET Framework 4.0. La vulnerabilidad corregida en esta actualización afecta a .NET Framework 4.0 y .NET Framework 4.0 Client Profile. Para obtener más información, vea el artículo de MSDN [Instalar .NET Framework](http://msdn.microsoft.com/es-es/library/5a4x27ek.aspx).

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

**Notas para MS11-044**

<sup>[1]</sup>**.NET Framework 4.0 y .NET Framework 4.0 Client Profile están afectados.** Los paquetes redistribuibles de .NET Framework versión 4 están disponibles en dos perfiles: .NET Framework 4.0 y .NET Framework 4.0 Client Profile. .NET Framework 4.0 Client Profile es un subconjunto de .NET Framework 4.0. La vulnerabilidad corregida en esta actualización afecta a .NET Framework 4.0 y .NET Framework 4.0 Client Profile. Para obtener más información, vea el artículo de MSDN [Instalar .NET Framework](http://msdn.microsoft.com/es-es/library/5a4x27ek.aspx).

<sup>[2]</sup>Las clasificaciones de gravedad no se aplican a esta actualización porque la vulnerabilidad tratada en este boletín no afecta a este software. No obstante, como medida defensiva para protegerse de nuevos posibles ataques identificados en el futuro, Microsoft recomienda que los usuarios de este software apliquen esta actualización de seguridad.

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
[**MS11-052**](http://go.microsoft.com/fwlink/?linkid=218115)
</td>
<td style="border:1px solid black;">
[**MS11-037**](http://go.microsoft.com/fwlink/?linkid=217912)
</td>
<td style="border:1px solid black;">
[**MS11-046**](http://go.microsoft.com/fwlink/?linkid=217464)
</td>
<td style="border:1px solid black;">
[**MS11-047**](http://go.microsoft.com/fwlink/?linkid=217468)
</td>
<td style="border:1px solid black;">
[**MS11-048**](http://go.microsoft.com/fwlink/?linkid=215840)
</td>
<td style="border:1px solid black;">
[**MS11-051**](http://go.microsoft.com/fwlink/?linkid=217101)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=6c760c7f-94f1-437f-a645-fd33b50d03f4)  
(Crítica)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=0b88f9e9-3439-44e5-92c8-66a3c97cb03d)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=03b45ad8-cc6b-473b-8112-bd513ed97f5d)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=ce5bc2d7-9438-4bf0-be5e-be9dd00c3286)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=a1db7736-f3e4-45df-af1d-52746978a0a8)  
(Importante)
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
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=c94c0d17-fdbe-41b3-a23d-98f43f907b89)  
(Crítica)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=ff955dc3-58ca-40ea-b7f1-9ff40c37f997)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=ed502ece-737e-44cb-84fd-8a0d1bc321c8)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7b211b02-a005-46a3-ad1d-d4baaeec8289)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=71497891-41a2-476d-b524-4eb5cecb9639)  
(Importante)
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
Windows Server 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-052**](http://go.microsoft.com/fwlink/?linkid=218115)
</td>
<td style="border:1px solid black;">
[**MS11-037**](http://go.microsoft.com/fwlink/?linkid=217912)
</td>
<td style="border:1px solid black;">
[**MS11-046**](http://go.microsoft.com/fwlink/?linkid=217464)
</td>
<td style="border:1px solid black;">
[**MS11-047**](http://go.microsoft.com/fwlink/?linkid=217468)
</td>
<td style="border:1px solid black;">
[**MS11-048**](http://go.microsoft.com/fwlink/?linkid=215840)
</td>
<td style="border:1px solid black;">
[**MS11-051**](http://go.microsoft.com/fwlink/?linkid=217101)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación** **de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Baja**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=5dafb455-969e-4be9-8735-d4ee0682d22f)  
(Moderada)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=ba3beb80-a921-489e-a6ff-a7b2d665ada6)  
(Moderada)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=a8038325-0d14-445b-a5d9-ce7ac1fa44b5)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6427ea5d-05d0-4367-805c-9cb305802b3c)  
(Baja)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c614cb8b-223e-4f84-b94c-f15747760aa5)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ef90d6c1-ea7f-4c32-9c90-0303e04c7436)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=e78829d0-8215-4e56-8959-ebd3bc8e9a91)  
(Moderada)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=3bec943e-5758-4439-a947-a8fafd30edec)  
(Moderada)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=5f7bcbad-f647-4fbb-88d4-b19c54db6f00)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e7f65891-32c0-4817-b3b2-d8be73145df9)  
(Baja)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9a951087-25c5-4f5c-8407-a1585491ae0b)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=62944095-33d6-4131-be32-a79d9ec4d4a9)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=1e822515-9f0a-4ef0-bb70-d4889d200f47)  
(Moderada)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=47a0fdc6-7576-4c32-b8fd-cbb05d57599d)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=ca8b1d09-9f80-417b-99b1-8f86e86e1f11)  
(Baja)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=dd48b93b-24fa-45a3-91fb-9f9f9418c49f)  
(Importante)
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
Windows Vista
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-052**](http://go.microsoft.com/fwlink/?linkid=218115)
</td>
<td style="border:1px solid black;">
[**MS11-037**](http://go.microsoft.com/fwlink/?linkid=217912)
</td>
<td style="border:1px solid black;">
[**MS11-046**](http://go.microsoft.com/fwlink/?linkid=217464)
</td>
<td style="border:1px solid black;">
[**MS11-047**](http://go.microsoft.com/fwlink/?linkid=217468)
</td>
<td style="border:1px solid black;">
[**MS11-048**](http://go.microsoft.com/fwlink/?linkid=215840)
</td>
<td style="border:1px solid black;">
[**MS11-051**](http://go.microsoft.com/fwlink/?linkid=217101)
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
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista Service Pack 1 y Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=e541f1bb-c9bf-4dc8-96ec-58a3de5ba7fd)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=cd059690-52b0-4b37-9fbb-d9906ae46fed)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ebea38a7-1fbe-4141-a529-52d7a7326d6a)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b69e3bda-940b-4524-a724-0af4ae0ec719)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5f0007c3-8d11-4940-8766-1112e3777aae)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=6c7d7162-ef19-49f4-a8fc-5db7415445a4)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=256bb26f-df9e-4259-881b-e8313a9fafa8)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=54833350-a385-4a31-995a-9ddc38798c21)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e3a26bc5-1757-4b38-9cae-419c919f4877)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=fadf6f12-1f09-4d49-93b1-8fce01400b4f)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
[**MS11-052**](http://go.microsoft.com/fwlink/?linkid=218115)
</td>
<td style="border:1px solid black;">
[**MS11-037**](http://go.microsoft.com/fwlink/?linkid=217912)
</td>
<td style="border:1px solid black;">
[**MS11-046**](http://go.microsoft.com/fwlink/?linkid=217464)
</td>
<td style="border:1px solid black;">
[**MS11-047**](http://go.microsoft.com/fwlink/?linkid=217468)
</td>
<td style="border:1px solid black;">
[**MS11-048**](http://go.microsoft.com/fwlink/?linkid=215840)
</td>
<td style="border:1px solid black;">
[**MS11-051**](http://go.microsoft.com/fwlink/?linkid=217101)
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
[**Baja**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=4446121a-0aab-4fbc-ba74-68d7650e8bca)\*\*  
(Moderada)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=ed089de4-c9ec-4ac7-a711-5f7cb29c05bc)\*\*  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6a3bbd67-94db-40b2-8786-cb39a493ec92)\*\*  
(Baja)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e34e4cf9-cdae-4240-8574-950c0be00822)\*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8960dd62-7cf7-41cb-97b2-b082bd1750aa)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=46ade106-e0cb-4c71-8230-793a15062823)\*\*  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=01399fc7-dc2b-461e-a1a5-751a3b61bde0)\*\*  
(Moderada)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=dd32b7c6-daa1-47aa-807f-25a678790cf2)\*\*  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4cb870f3-9878-4075-b8fd-2ee90c8e3bc8)\*\*  
(Baja)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a3604f05-26b2-451b-9153-0e718158371e)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=24789423-72b7-48d1-bdc1-f0e5174d99bb)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=0abc6908-ac6a-4da3-843a-af6841ccc1db)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6141a1c5-ecaf-4553-9d27-dd6e5c4a13fd)\*\*  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=16a8b78a-3979-4cc7-bbe5-6d962aa64336)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e1243011-00e6-49f2-a676-c04cb805d36a)  
(Baja)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e8a82b44-e1d8-45f8-b8b8-b1f74e1efce0)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=057f1356-9c70-4457-a1df-69334fdab467)  
(Importante)
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
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-052**](http://go.microsoft.com/fwlink/?linkid=218115)
</td>
<td style="border:1px solid black;">
[**MS11-037**](http://go.microsoft.com/fwlink/?linkid=217912)
</td>
<td style="border:1px solid black;">
[**MS11-046**](http://go.microsoft.com/fwlink/?linkid=217464)
</td>
<td style="border:1px solid black;">
[**MS11-047**](http://go.microsoft.com/fwlink/?linkid=217468)
</td>
<td style="border:1px solid black;">
[**MS11-048**](http://go.microsoft.com/fwlink/?linkid=215840)
</td>
<td style="border:1px solid black;">
[**MS11-051**](http://go.microsoft.com/fwlink/?linkid=217101)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=27e767d8-84e3-434f-bb8d-3b2303774ad0)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=c3647646-658a-423b-b0cb-bba7613b67e7)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=63d8b801-5178-474b-a21e-72a0ce501d3e)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=cf9e5ecd-68f7-4982-b4ed-be80859b757c)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=747ba56a-0d47-4946-99a4-bae1f11ea748)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7996511d-4b8e-49c3-a0fa-4da907a6c947)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=cd7d3cb9-cb60-4b62-b0df-a38fe21802e9)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=2707650a-604c-4044-acc4-07a30b5640d8)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
[**MS11-052**](http://go.microsoft.com/fwlink/?linkid=218115)
</td>
<td style="border:1px solid black;">
[**MS11-037**](http://go.microsoft.com/fwlink/?linkid=217912)
</td>
<td style="border:1px solid black;">
[**MS11-046**](http://go.microsoft.com/fwlink/?linkid=217464)
</td>
<td style="border:1px solid black;">
[**MS11-047**](http://go.microsoft.com/fwlink/?linkid=217468)
</td>
<td style="border:1px solid black;">
[**MS11-048**](http://go.microsoft.com/fwlink/?linkid=215840)
</td>
<td style="border:1px solid black;">
[**MS11-051**](http://go.microsoft.com/fwlink/?linkid=217101)
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
[**Baja**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=cff7f53d-0fd6-48f8-a9d6-bf19e0a32905)\*\*  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=40354f73-4f4d-4a4a-abac-f8a3d4c3ae5f)\*\*  
(Baja)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=e67c73ca-d0f9-40c1-8b6e-25b1b13caa3a)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=c9c6c36d-a455-42f7-b7d4-9fb9824c07cb)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=f9824310-772d-4e1e-980e-11e2db3ac53e)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1da04414-6210-43ea-8e0a-cf21cf144076)\*\*  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=4dd2c0f4-b29c-4648-a123-83d3ae6a878f)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=22853823-8f63-4258-8991-1ad50e58a0d9)  
(Baja)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=72d1d6b6-e8bd-492b-b65a-82060beef441)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=0533d293-e186-4d39-a925-ab3d9ed46290)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
**Nota para Windows Server 2008 y Windows Server 2008 R2**

**\*La instalación de Server Core está afectada.** Esta actualización se aplica, con la misma clasificación de gravedad, a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, independientemente de si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**\*\*La instalación de Server Core no está afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

#### Conjuntos de programas y software de Microsoft Office

 
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
Conjuntos de programas y componentes de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-045**](http://go.microsoft.com/fwlink/?linkid=217502)
</td>
<td style="border:1px solid black;">
[**MS11-049**](http://go.microsoft.com/fwlink/?linkid=217077)
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
Microsoft Office XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Excel 2002 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=853c0663-94f7-4634-98ad-47ca4b1f7b1e)  
(KB2541003)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Excel 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=f38f183a-9c64-406b-9bf6-807cb2d55e56)  
(KB2541025)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft Excel 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5b271f87-a279-419f-9437-ded224fa19f1)<sup>[1]</sup>
(KB2541007)  
(Importante)
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
[Microsoft Excel 2010 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=baba7ec1-4a5e-4e13-9d0e-9085a39a0554)  
(KB2523021)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Excel 2010 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=d6e9f422-43b0-4da5-8356-c38482e8eebb)  
(KB2523021)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Office para Mac
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-045**](http://go.microsoft.com/fwlink/?linkid=217502)
</td>
<td style="border:1px solid black;">
[**MS11-049**](http://go.microsoft.com/fwlink/?linkid=217077)
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
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2004 para Mac
</td>
<td style="border:1px solid black;">
[Microsoft Office 2004 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=d12d0868-4f28-4c0a-ab61-338878064b70)  
(KB2555786)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2008 para Mac
</td>
<td style="border:1px solid black;">
[Microsoft Office 2008 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=9e2d348b-c753-4eab-838c-370cd5af5e14)  
(KB2555785)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office para Mac 2011
</td>
<td style="border:1px solid black;">
[Microsoft Office para Mac 2011](http://www.microsoft.com/downloads/details.aspx?familyid=3c58555c-1eba-42fe-a10f-b30af9031e44)  
(KB2555784)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Convertidor de archivos con formatos XML abiertos para Mac
</td>
<td style="border:1px solid black;">
[Convertidor de archivos con formatos XML abiertos para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=6118d5f5-b6fd-4584-be25-209534772379)  
(KB2555787)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft InfoPath
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-045**](http://go.microsoft.com/fwlink/?linkid=217502)
</td>
<td style="border:1px solid black;">
[**MS11-049**](http://go.microsoft.com/fwlink/?linkid=217077)
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
Microsoft InfoPath 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft InfoPath 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=88eedb0b-a2cf-4a1b-b1b9-0b2926c25872)  
(KB2510061)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft InfoPath 2010 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft InfoPath 2010 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=90ffe910-bd9c-48aa-8007-2b43e1a99999)  
(KB2510065)  
(Importante)
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
[Microsoft InfoPath 2010 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=f3244003-fb63-44d8-bedc-6399c39aacba)  
(KB2510065)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Otro software de Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-045**](http://go.microsoft.com/fwlink/?linkid=217502)
</td>
<td style="border:1px solid black;">
[**MS11-049**](http://go.microsoft.com/fwlink/?linkid=217077)
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
Microsoft Excel Viewer
</td>
<td style="border:1px solid black;">
[Microsoft Excel Viewer Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=77c1e7e2-207f-46fd-81f2-43a25eddc010)  
(KB2541015)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
[Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3512a033-871d-49ec-a8d2-1b9c7dec4936)  
(KB2541012)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
**Nota para MS11-045**

<sup>[1]</sup>Para Microsoft Office Excel 2007 Service Pack 2, además del paquete de actualización de seguridad KB2541007, los clientes también deben instalar la actualización de seguridad para Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2 (KB2541012) con el fin de protegerse de las vulnerabilidades descritas en este boletín.

**Nota para MS11-049**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Software de servidor de Microsoft

 
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
Microsoft SQL Server
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-049**](http://go.microsoft.com/fwlink/?linkid=217077)
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
SQL Server 2005 Service Pack 3
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2005 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=faca7f7a-c346-48e3-9bf5-f140a51aae4e)  
(KB2494113)  
(Importante)  

Actualización de QFE:  
[SQL Server 2005 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=d214763c-5a16-4959-90ff-08112345d867)  
(KB2494112)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
SQL Server 2005 x64 Edition Service Pack 3
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2005 x64 Edition Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=faca7f7a-c346-48e3-9bf5-f140a51aae4e)  
(KB2494113)  
(Importante)  

Actualización de QFE:  
[SQL Server 2005 x64 Edition Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=d214763c-5a16-4959-90ff-08112345d867)  
(KB2494112)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
SQL Server 2005 para sistemas con Itanium Service Pack 3
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2005 para sistemas con Itanium Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=faca7f7a-c346-48e3-9bf5-f140a51aae4e)  
(KB2494113)  
(Importante)  

Actualización de QFE:  
[SQL Server 2005 para sistemas con Itanium Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=d214763c-5a16-4959-90ff-08112345d867)  
(KB2494112)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
SQL Server 2005 Service Pack 4
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2005 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=2aba4a2e-477f-4267-9ebe-ab7b29d218ad)  
(KB2494120)  
(Importante)  

Actualización de QFE:  
[SQL Server 2005 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=2975ad1a-1852-4771-b3fa-2be79899be57)  
(KB2494123)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
SQL Server 2005 x64 Edition Service Pack 4
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2005 x64 Edition Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=2aba4a2e-477f-4267-9ebe-ab7b29d218ad)  
(KB2494120)  
(Importante)  

Actualización de QFE:  
[SQL Server 2005 x64 Edition Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=2975ad1a-1852-4771-b3fa-2be79899be57)  
(KB2494123)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
SQL Server 2005 para sistemas con Itanium Service Pack 4
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2005 para sistemas con Itanium Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=2aba4a2e-477f-4267-9ebe-ab7b29d218ad)  
(KB2494120)  
(Importante)  

Actualización de QFE:  
[SQL Server 2005 para sistemas con Itanium Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=2975ad1a-1852-4771-b3fa-2be79899be57)  
(KB2494123)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
SQL Server 2005 Express Edition Service Pack 3
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2005 Express Edition Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=faca7f7a-c346-48e3-9bf5-f140a51aae4e)  
(KB2494113)  
(Importante)  

Actualización de QFE:  
[SQL Server 2005 Express Edition Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=d214763c-5a16-4959-90ff-08112345d867)  
(KB2494112)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
SQL Server 2005 Express Edition Service Pack 4
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2005 Express Edition Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=2aba4a2e-477f-4267-9ebe-ab7b29d218ad)  
(KB2494120)  
(Importante)  

Actualización de QFE:  
[SQL Server 2005 Express Edition Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=2975ad1a-1852-4771-b3fa-2be79899be57)  
(KB2494123)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
SQL Server 2005 Express Edition con Advanced Services Service Pack 3
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2005 Express Edition con Advanced Services Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=faca7f7a-c346-48e3-9bf5-f140a51aae4e)  
(KB2494113)  
(Importante)  

Actualización de QFE:  
[SQL Server 2005 Express Edition con Advanced Services Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=d214763c-5a16-4959-90ff-08112345d867)  
(KB2494112)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
SQL Server 2005 Express Edition con Advanced Services Service Pack 4
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2005 Express Edition con Advanced Services Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=2aba4a2e-477f-4267-9ebe-ab7b29d218ad)  
(KB2494120)  
(Importante)  

Actualización de QFE:  
[SQL Server 2005 Express Edition con Advanced Services Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=2975ad1a-1852-4771-b3fa-2be79899be57)  
(KB2494123)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
SQL Server Management Studio Express (SSMSE) 2005
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server Management Studio Express (SSMSE) 2005](http://www.microsoft.com/downloads/details.aspx?familyid=34c3ba21-b158-4e6d-82ba-831053d41161)  
(KB2546869)  
(Importante)  

Actualización de QFE:  
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
SQL Server Management Studio Express (SSMSE) 2005 x64 Edition
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server Management Studio Express (SSMSE) 2005 x64 Edition](http://www.microsoft.com/downloads/details.aspx?familyid=34c3ba21-b158-4e6d-82ba-831053d41161)  
(KB2546869)  
(Importante)  

Actualización de QFE:  
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
SQL Server 2008 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2008 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=ae7db514-d96b-4cff-a13d-c74f4cf8cf0c)<sup>[1]</sup>
(KB2494096)  
(Importante)  

Actualización de QFE:  
[SQL Server 2008 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=312a39c4-cb32-4216-8672-1b1c0937ba6c)<sup>[1]</sup>
(KB2494100)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
SQL Server 2008 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2008 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=ae7db514-d96b-4cff-a13d-c74f4cf8cf0c)<sup>[1]</sup>
(KB2494096)  
(Importante)  

Actualización de QFE:  
[SQL Server 2008 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=312a39c4-cb32-4216-8672-1b1c0937ba6c)<sup>[1]</sup>
(KB2494100)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
SQL Server 2008 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2008 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=ae7db514-d96b-4cff-a13d-c74f4cf8cf0c)  
(KB2494096)  
(Importante)  

Actualización de QFE:  
[SQL Server 2008 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=312a39c4-cb32-4216-8672-1b1c0937ba6c)  
(KB2494100)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
SQL Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6f4767bf-257d-4822-b768-7b6702261276)<sup>[1]</sup>
(KB2494089)  
(Importante)  

Actualización de QFE:  
[SQL Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=23240963-e2c6-4d40-8179-661117b53e91)<sup>[1]</sup>
(KB2494094)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
SQL Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6f4767bf-257d-4822-b768-7b6702261276)<sup>[1]</sup>
(KB2494089)  
(Importante)  

Actualización de QFE:  
[SQL Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=23240963-e2c6-4d40-8179-661117b53e91)<sup>[1]</sup>
(KB2494094)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
SQL Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6f4767bf-257d-4822-b768-7b6702261276)  
(KB2494089)  
(Importante)  

Actualización de QFE:  
[SQL Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=23240963-e2c6-4d40-8179-661117b53e91)  
(KB2494094)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
SQL Server 2008 R2 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2008 R2 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=80e98567-1b28-49b1-a646-579f8c115a41)<sup>[1]</sup>
(KB2494088)  
(Importante)  

Actualización de QFE:  
[SQL Server 2008 R2 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=9df95137-d1b3-4fac-8958-8042aa2010c4)<sup>[1]</sup>
(KB2494086)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
SQL Server 2008 R2 para sistemas x64
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=80e98567-1b28-49b1-a646-579f8c115a41)<sup>[1]</sup>
(KB2494088)  
(Importante)  

Actualización de QFE:  
[SQL Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=9df95137-d1b3-4fac-8958-8042aa2010c4)<sup>[1]</sup>
(KB2494086)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
SQL Server 2008 R2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=80e98567-1b28-49b1-a646-579f8c115a41)  
(KB2494088)  
(Importante)  

Actualización de QFE:  
[SQL Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=9df95137-d1b3-4fac-8958-8042aa2010c4)  
(KB2494086)  
(Importante)
</td>
</tr>
</table>
 
**Notas para MS11-049**

<sup>[1]</sup>Esta actualización también se aplica a las correspondientes ediciones Express y Express con Advanced Services.

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

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
Microsoft Silverlight
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-039**](http://go.microsoft.com/fwlink/?linkid=212287)
</td>
<td style="border:1px solid black;">
[**MS11-049**](http://go.microsoft.com/fwlink/?linkid=217077)
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
Microsoft Silverlight 4
</td>
<td style="border:1px solid black;">
[Microsoft Silverlight 4](http://www.microsoft.com/downloads/details.aspx?familyid=2f71b104-b66f-4146-9d70-fcde766c91b8) cuando está instalado en Mac  
(KB2512827)  
(Crítica)  

[Microsoft Silverlight 4](http://www.microsoft.com/downloads/details.aspx?familyid=2f71b104-b66f-4146-9d70-fcde766c91b8) cuando está instalado en todas las versiones de los clientes Microsoft Windows  
(KB2512827)  
(Crítica)  

[Microsoft Silverlight 4](http://www.microsoft.com/downloads/details.aspx?familyid=2f71b104-b66f-4146-9d70-fcde766c91b8) cuando está instalado en todas las versiones de los servidores Microsoft Windows \*\*  
(KB2512827)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Visual Studio
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-039**](http://go.microsoft.com/fwlink/?linkid=212287)
</td>
<td style="border:1px solid black;">
[**MS11-049**](http://go.microsoft.com/fwlink/?linkid=217077)
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
[Microsoft Visual Studio 2005 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=e5ce8a9a-e89b-4095-9f21-7e6f307fbf2b)  
(KB2251481)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Visual Studio 2008 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Visual Studio 2008 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=cc01bce9-3f38-4590-9c6e-a4048c886d33)  
(KB2251487)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Visual Studio 2010
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Visual Studio 2010](http://www.microsoft.com/downloads/details.aspx?familyid=213b820f-dcba-4895-b339-b50eeb92524d)  
(KB2251489)  
(Importante)
</td>
</tr>
</table>
 
**Notas para MS11-039**

**\*\*La instalación de Server Core no está afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

**Nota para MS11-049**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Software de seguridad de Microsoft

 
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
Microsoft Forefront
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-040**](http://go.microsoft.com/fwlink/?linkid=217470)
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
Cliente de Microsoft Forefront Threat Management Gateway 2010
</td>
<td style="border:1px solid black;">
[Cliente de Microsoft Forefront Threat Management Gateway 2010](http://www.microsoft.com/downloads/details.aspx?familyid=d1c85acd-a6df-4634-9cd4-c562ad92097e)  
(Crítica)
</td>
</tr>
</table>
 

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/bb245732). [TechNet Security Center](http://technet.microsoft.com/es-es/security/default.aspx) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://www.microsoft.com/es-es/security/default.aspx), donde esta información también está disponible haciendo clic en "Últimas actualizaciones de seguridad".

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Para clientes de Microsoft Office para Mac, Microsoft AutoUpdate para Mac puede servir de ayuda para mantener actualizado el software de Microsoft. Para obtener más información acerca del uso de Microsoft AutoUpdate para Mac, vea [Buscar actualizaciones de software automáticamente](http://mac2.microsoft.com/help/office/14/en-us/word/item/ffe35357-8f25-4df8-a0a3-c258526c64ea).

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS07-036"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Consejos para la detección y la implementación**

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747).

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://go.microsoft.com/fwlink/?linkid=21134).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar de un modo rápido y confiable las actualizaciones críticas y de seguridad más recientes en sistemas operativos Microsoft Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://technet.microsoft.com/en-us/wsus/default.aspx).

**System Center Configuration Manager 2007**

La administración de actualizaciones de software de Configuration Manager 2007 simplifica la tarea compleja de entregar y administrar actualizaciones para los sistemas de TI en toda la empresa. Con Configuration Manager 2007, los administradores de TI pueden ofrecer actualizaciones de los productos de Microsoft a una serie de dispositivos, incluidos equipos de escritorio, portátiles, servidores y dispositivos móviles.

La evaluación automática de vulnerabilidades en Configuration Manager 2007 detecta las necesidades de actualizaciones e informa de las acciones recomendadas. La administración de actualizaciones de software en Configuration Manager 2007 se basa en Microsoft Windows Software Update Services (WSUS), una infraestructura de actualizaciones probada con la que están familiarizados los administradores de TI de todo el mundo. Para obtener más información acerca de cómo los administradores pueden usar Configuration Manager 2007 para implementar actualizaciones, vea [Administración de actualizaciones de software](http://www.microsoft.com/systemcenter/en/us/configuration-manager/cm-software-update-management.aspx). Para obtener más información acerca de Configuration Manager, visite [System Center Configuration Manager](http://www.microsoft.com/systemcenter/en/us/configuration-manager.aspx).

**Systems Management Server 2003**

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

-   Billy Rios y Eduardo Vela Nava, de [Google Security Team](http://www.google.com/), por colaborar con nosotros en los cambios de MS11-037
-   Yamata Li, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de un problema descrito en MS11-038
-   Michael J. Liu, por informar de un problema descrito en MS11-039
-   Koro, de [www.korosoft.net](http://www.korosoft.net/), por informar de un problema descrito en MS11-041
-   Laurent Gaffié, de [NGS Software](http://www.ngssoftware.com/), por informar de un problema descrito en MS11-042
-   Dan Kaminsky, por colaborar con nosotros en un problema descrito en MS11-044
-   Bing Liu, de [FortiGuard Labs de Fortinet](http://www.fortiguard.com/), por informar de dos problemas descritos en MS11-045
-   Un investigador anónimo, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS11-045
-   Omair, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS11-045
-   Un investigador anónimo, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS11-045
-   Nicolas Gregoire, de [Agarri](http://www.agarri.fr/), en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS11-045
-   Omair, por informar de un problema descrito en MS11-045
-   Will Dormann, de [CERT/CC](http://www.cert.org/), por informar de dos problemas descritos en MS11-045
-   Steven Adair, de [Shadowserver Foundation](http://www.shadowserver.org), y Chris S., por informar de un problema descrito en ms11-046
-   Nicolas Economou, de [Core Security Technologies](http://www.coresecurity.com/), por informar de un problema descrito en MS11-047
-   Jesse Ou, de [Cigital](http://www.cigital.com), por informar de un problema descrito en MS11-049
-   Robert Swiecki, de [Google Inc.](http://www.google.com/), por informar de un problema descrito en MS11-050
-   [NSFOCUS Security Team](http://www.nsfocus.com/)
-   , por informar de un problema descrito en MS11-050
-   Un investigador anónimo, en colaboración con el programa [SecuriTeam Secure Disclosure de Beyond Security](http://www.beyondsecurity.com/ssd.html), por informar de un problema descrito en MS11-050
-   Adi Cohen, de [IBM Rational Application Security](http://blog.watchfire.com/), por informar de un problema descrito en MS11-050
-   [Trend Micro](http://www.trendmicro.com/)
-   , por colaborar con nosotros en un problema descrito en MS11-050
-   Nirmal Singh Bhary, de [Norman](http://www.norman.com), por informar de un problema descrito en MS11-050
-   Un investigador anónimo, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS11-050
-   Damian Put, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS11-050
-   Yoel Gluck, Yogesh Badwe y Varun Badhwar, del equipo de seguridad de productos de [salesforce.com](http://www.salesforce.com/), por informar de un problema descrito en MS11-050
-   José Antonio Vázquez González, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS11-050
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS11-050
-   Peter Winter-Smith, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS11-050
-   Stephen Fewer, de [Harmony Security](http://www.harmonysecurity.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por colaborar con nosotros en los cambios de defensa tratados en MS11-050
-   Ruggero Strabla, de [Emaze](http://www.emaze.net/) Networks; [Saipem Security Team](http://www.saipem.com/), por informar de un problema descrito en MS11-051
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS11-052

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Los clientes de Estados Unidos y Canadá pueden recibir soporte técnico del [soporte de seguridad](http://go.microsoft.com/fwlink/?linkid=21131) o en el teléfono 1-866-PCSAFETY. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de las opciones de asistencia disponibles, vea [Ayuda y soporte técnico de Microsoft](http://support.microsoft.com/).
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico internacional](http://go.microsoft.com/fwlink/?linkid=21155).

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (14 de junio de 2011): Publicación del resumen del boletín.
-   V1.1 (14 de junio de 2011): Para MS11-042, se ha quitado Windows 7 para sistemas de 32 bits Service Pack 1, Windows 7 para sistemas x64 Service Pack 1, Windows Server 2008 R2 para sistemas x64 Service Pack 1 y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1 de la subsección **Ubicaciones de descarga y software afectado**. Se trata únicamente de un cambio informativo. No había cambios en los archivos de la actualización de seguridad o en la lógica de la detección.
-   V2.0 (9 de agosto de 2011): Se ha vuelto a publicar MS11-043 para ofrecer de nuevo la actualización en todos los sistemas operativos compatibles para solucionar un problema de estabilidad. Los clientes que ya han actualizado sus sistemas deben volver a instalar MS11-043. Además, se ha vuelto a publicar MS11-049 para anunciar un cambio de detección en la actualización para Microsoft Visual Studio 2005 Service Pack 1 para agregar detección del software relacionado. No hubo cambios en los archivos de la actualización de seguridad en MS11-049. Los clientes que ya han actualizado correctamente sus sistemas no necesitan volver a instalar MS11-049.
-   V2.1 (26 de octubre de 2011): Para MS11-039 y MS11-044, se ha corregido la aplicabilidad de la instalación de Server Core para .NET Framework 4.0 en Windows Server 2008 R2 para sistemas x64.
-   V3.0 (8 de noviembre de 2011): Se ha vuelto a publicar MS11-037 para ofrecer de nuevo la actualización en todas las ediciones compatibles de Windows XP y Windows Server 2003. Los clientes que usan Windows XP y Windows Server 2003, incluidos los que hayan instalado correctamente la actualización que se ofreció originalmente el 14 de junio de 2011, deben instalar la actualización que se ofrece de nuevo.
-   V3.1 (18 de enero de 2012): Para MS11-049, se ha agregado una nota a la sección Software afectado y Ubicaciones de descarga para aclarar que esta actualización también se aplica a las ediciones SQL Server 2008 y SQL Server 2008 R2 Express y Express Advanced para 32 bits y x64.

*Built at 2014-04-18T01:50:00Z-07:00*
