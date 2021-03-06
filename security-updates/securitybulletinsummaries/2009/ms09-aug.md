---
TOCTitle: 'MS09-AUG'
Title: Resumen del boletín de seguridad de Microsoft de agosto 2009
ms:assetid: 'ms09-aug'
ms:contentKeyID: 61225397
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms09-aug(v=Security.10)'
--- 


Resumen del boletín de seguridad de Microsoft de agosto 2009
============================================================

Publicado: martes, 11 de agosto de 2009 | Actualizado: martes, 27 de octubre de 2009

**Versión:** 4.0

Este resumen del boletín enumera los boletines de seguridad publicados para agosto de 2009.

Con la publicación de los boletines de agosto de 2009, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 6 de agosto de 2009. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar una conferencia en línea para atender las consultas de los clientes sobre estos boletines el 12 de agosto de 2009, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora a la conferencia en línea del boletín de seguridad de agosto](http://msevents.microsoft.com/cui/webcasteventdetails.aspx?eventid=1032407484&eventcategory=4&culture=en-us&countrycode=us). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad y de alta prioridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-043">MS09-043</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Office Web Components podrían permitir la ejecución remota de código (957638)</strong><br />
<br />
Esta actualización de seguridad resuelve varias vulnerabilidades de las que se ha informado de forma privada en Microsoft Office Web Components que podrían permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada. Un intruso que aprovechara estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario local. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office, Microsoft Visual Studio, Microsoft ISA Server, Microsoft BizTalk Server</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-044">MS09-044</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Conexión a Escritorio remoto podrían permitir la ejecución remota de código (970927)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Conexión a Escritorio remoto de Microsoft. Las vulnerabilidades podrían permitir la ejecución remota de código si un atacante convence a un usuario de Terminal Services para que se conecte a un servidor RDP malintencionado o si un usuario visita un sitio web especialmente diseñado que aproveche esta vulnerabilidad. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, Cliente de Conexión a Escritorio remoto para Mac</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-039">MS09-039</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en WINS podrían permitir la ejecución remota de código (969883)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Servicio de nombres Internet de Windows (WINS). Cualquier vulnerabilidad podría permitir la ejecución remota de código si un usuario recibe un paquete de réplica de WINS especialmente diseñado en un sistema afectado que ejecuta el servicio WINS. De forma predeterminada, WINS no se instala en ninguna versión de sistema operativo afectada. Sólo los clientes que instalen manualmente este componente están afectados por este problema.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-038">MS09-038</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en el procesamiento de archivos de Windows Media podrían permitir la ejecución remota de código (971557)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en el procesamiento de archivos de Windows Media. Cualquier vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo AVI especialmente diseñado. Si un usuario inicia sesión con derechos de usuario administrativos, un intruso que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-037">MS09-037</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Active Template Library (ATL) podrían permitir la ejecución remota de código (973908)</strong><br />
<br />
Esta actualización de seguridad resuelve varias vulnerabilidades de las que se ha informado de forma privada en Microsoft Active Template Library (ATL). Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario carga un componente o control especialmente diseñado hospedado en un sitio web malintencionado. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-041">MS09-041</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el servicio de estación de trabajo podría permitir la elevación de privilegios (971657)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en el servicio de estación de trabajo de Windows. La vulnerabilidad podría permitir la elevación de privilegios si un atacante crea un mensaje RPC especialmente diseñado y lo envía a un sistema afectado. Un atacante que consiga aprovechar esta vulnerabilidad podría ejecutar código arbitrario y tomar el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Un atacante debe tener credenciales válidas de inicio de sesión en un sistema vulnerable para aprovechar esta vulnerabilidad. Usuarios remotos no pueden aprovechar esta vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-040">MS09-040</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Message Queue Server podría permitir la elevación de privilegios (971032)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Message Queue Server (MSMQ). La vulnerabilidad podría permitir la elevación de privilegios si un usuario recibe una solicitud especialmente diseñada en un servicio MSMQ afectado. De forma predeterminada, el componente Message Queue Server no se instala en ninguna edición de sistema operativo afectada y sólo lo puede habilitar un usuario con privilegios administrativos. Sólo los clientes que instalen manualmente el componente Message Queue Server pueden ser vulnerables a este problema.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-036">MS09-036</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en ASP.NET en Microsoft Windows podría permitir la denegación de servicio (970957)</strong><br />
<br />
Esta actualización de seguridad corrige una vulnerabilidad de denegación de servicio de la que se ha informado de forma privada en el componente Microsoft .NET Framework de Microsoft Windows. Esta vulnerabilidad sólo se puede aprovechar cuando Internet Information Services (IIS) 7.0 está instalado y ASP.NET está configurado para usar el modo integrado en las versiones afectadas de Microsoft Windows. Un atacante podría crear solicitudes HTTP anónimas especialmente diseñadas que podrían provocar que el servidor web afectado dejara de responder hasta que se reinicie el grupo de aplicaciones asociado. Los clientes que ejecutan grupos de aplicaciones de IIS 7.0 en modo clásico no están afectados por esta vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Denegación de servicio</td>
<td style="border:1px solid black;">No requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, Microsoft .NET Framework</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-042">MS09-042</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Telnet podría permitir la ejecución remota de código (960859)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad en el servicio Telnet de Microsoft. La vulnerabilidad podría permitir que un atacante obtuviera las credenciales y las usara para volver a iniciar sesión en los sistemas afectados. El atacante adquiriría derechos de usuario en un sistema idénticos a los del usuario que ha iniciado sesión. Este escenario podría, en última instancia, tener como resultado la ejecución remota de código en sistemas afectados. Un atacante que aprovechara esta vulnerabilidad podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y de identificador de CVE.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de que se publique código funcional que aproveche la vulnerabilidad en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Debe revisar cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/en-us/security/cc998259.aspx).
  
| Identificador del boletín                                           | Título del boletín                                                                                                        | Identificador CVE                                                                | Evaluación de índice de explotabilidad                                                                                                  | Notas clave                                                                                                                                                                                                                                                                                                                       |  
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| [MS09-036](http://technet.microsoft.com/security/bulletin/ms09-036) | Una vulnerabilidad en ASP.NET en Microsoft Windows podría permitir la denegación de servicio (970957)                     | [CVE-2009-1536](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1536) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | Probabilidad de una herramienta de denegación de servicio. No obstante, es improbable código funcional que aproveche la vulnerabilidad para la ejecución remota de código.                                                                                                                                                        |  
| [MS09-037](http://technet.microsoft.com/security/bulletin/ms09-037) | Vulnerabilidades en Microsoft Active Template Library (ATL) podrían permitir la ejecución remota de código (973908)       | [CVE-2008-0015](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-0015) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | **Esta vulnerabilidad se está aprovechando actualmente en el ecosistema de Internet.**                                                                                                                                                                                                                                            |  
| [MS09-037](http://technet.microsoft.com/security/bulletin/ms09-037) | Vulnerabilidades en Microsoft Active Template Library (ATL) podrían permitir la ejecución remota de código (973908)       | [CVE-2008-0020](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-0020) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                                                                                                                                                         |  
| [MS09-037](http://technet.microsoft.com/security/bulletin/ms09-037) | Vulnerabilidades en Microsoft Active Template Library (ATL) podrían permitir la ejecución remota de código (973908)       | [CVE-2009-0901](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0901) | Ninguna                                                                                                                                 | (A esta vulnerabilidad ya se le ha asignado una evaluación de índice de explotabilidad en el [resumen del boletín de julio](http://technet.microsoft.com/security/bulletin/ms09-jul). Esto se debe a que esta vulnerabilidad ya se trató por primera vez en [MS09-035](http://technet.microsoft.com/security/bulletin/ms09-035).) |  
| [MS09-037](http://technet.microsoft.com/security/bulletin/ms09-037) | Vulnerabilidades en Microsoft Active Template Library (ATL) podrían permitir la ejecución remota de código (973908)       | [CVE-2009-2493](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2493) | Ninguna                                                                                                                                 | (A esta vulnerabilidad ya se le ha asignado una evaluación de índice de explotabilidad en el [resumen del boletín de julio](http://technet.microsoft.com/security/bulletin/ms09-jul). Esto se debe a que esta vulnerabilidad ya se trató por primera vez en [MS09-035](http://technet.microsoft.com/security/bulletin/ms09-035).) |  
| [MS09-037](http://technet.microsoft.com/security/bulletin/ms09-037) | Vulnerabilidades en Microsoft Active Template Library (ATL) podrían permitir la ejecución remota de código (973908)       | [CVE-2009-2494](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2494) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                                                                                                                                                         |  
| [MS09-038](http://technet.microsoft.com/security/bulletin/ms09-038) | Vulnerabilidades en el procesamiento de archivos de Windows Media podrían permitir la ejecución remota de código (971557) | [CVE-2009-1545](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1545) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                                                                                                                                                                         |  
| [MS09-038](http://technet.microsoft.com/security/bulletin/ms09-038) | Vulnerabilidades en el procesamiento de archivos de Windows Media podrían permitir la ejecución remota de código (971557) | [CVE-2009-1546](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1546) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                                                                                                                                                                         |  
| [MS09-039](http://technet.microsoft.com/security/bulletin/ms09-039) | Vulnerabilidades en WINS podrían permitir la ejecución remota de código (969883)                                          | [CVE-2009-1923](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1923) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                                                                                                                                                         |  
| [MS09-039](http://technet.microsoft.com/security/bulletin/ms09-039) | Vulnerabilidades en WINS podrían permitir la ejecución remota de código (969883)                                          | [CVE-2009-1924](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1924) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | Hay mayor probabilidad de que se aproveche la vulnerabilidad en un objetivo de Windows 2000.                                                                                                                                                                                                                                      |  
| [MS09-040](http://technet.microsoft.com/security/bulletin/ms09-040) | Una vulnerabilidad en Message Queue Server podría permitir la elevación de privilegios (971032)                           | [CVE-2009-1922](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1922) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | No es posible un ataque remoto debido a esta vulnerabilidad.                                                                                                                                                                                                                                                                      |  
| [MS09-041](http://technet.microsoft.com/security/bulletin/ms09-041) | Una vulnerabilidad en el servicio de estación de trabajo podría permitir la elevación de privilegios (971657)             | [CVE-2009-1544](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1544) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | Para aprovechar esta vulnerabilidad, el atacante requeriría autenticación.                                                                                                                                                                                                                                                        |  
| [MS09-042](http://technet.microsoft.com/security/bulletin/ms09-042) | Una vulnerabilidad en Telnet podría permitir la ejecución remota de código (960859)                                       | [CVE-2009-1930](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1930) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | Esta vulnerabilidad es similar a las vulnerabilidades de reflexión de credenciales NTLM anteriores para las que ya existe código para aprovecharlas.                                                                                                                                                                              |  
| [MS09-043](http://technet.microsoft.com/security/bulletin/ms09-043) | Vulnerabilidades en Microsoft Office Web Components podrían permitir la ejecución remota de código (957638)               | [CVE-2009-0562](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0562) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                                                                                                                                                         |  
| [MS09-043](http://technet.microsoft.com/security/bulletin/ms09-043) | Vulnerabilidades en Microsoft Office Web Components podrían permitir la ejecución remota de código (957638)               | [CVE-2009-1136](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1136) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | El código para aprovechar la vulnerabilidad se ha expuesto de forma pública.                                                                                                                                                                                                                                                      |  
| [MS09-043](http://technet.microsoft.com/security/bulletin/ms09-043) | Vulnerabilidades en Microsoft Office Web Components podrían permitir la ejecución remota de código (957638)               | [CVE-2009-1534](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1534) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                                                                                                                                                         |  
| [MS09-043](http://technet.microsoft.com/security/bulletin/ms09-043) | Vulnerabilidades en Microsoft Office Web Components podrían permitir la ejecución remota de código (957638)               | [CVE-2009-2496](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2496) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                                                                                                                                                         |  
| [MS09-044](http://technet.microsoft.com/security/bulletin/ms09-044) | Vulnerabilidades en Conexión a Escritorio remoto podrían permitir la ejecución remota de código (970927)                  | [CVE-2009-1133](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1133) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                                                                                                                                                                         |  
| [MS09-044](http://technet.microsoft.com/security/bulletin/ms09-044) | Vulnerabilidades en Conexión a Escritorio remoto podrían permitir la ejecución remota de código (970927)                  | [CVE-2009-1929](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1929) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                                                                                                                                                         |
  
Ubicaciones de descarga y software afectado  
-------------------------------------------
  
Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.
  
**¿Cómo se usan estas tablas?**  
  
Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, se indica un hipervínculo a la actualización de software disponible y también se muestra la clasificación de gravedad de dicha actualización de software.
  
**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.
  
#### Componentes y sistema operativo Windows

 
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
<th style="border:1px solid black;" >
</th>
</tr>
<tr>
<th colspan="9" style="border:1px solid black;">
Microsoft Windows 2000  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-044**](http://technet.microsoft.com/security/bulletin/ms09-044)
</td>
<td style="border:1px solid black;">
[**MS09-039**](http://technet.microsoft.com/security/bulletin/ms09-039)
</td>
<td style="border:1px solid black;">
[**MS09-038**](http://technet.microsoft.com/security/bulletin/ms09-038)
</td>
<td style="border:1px solid black;">
[**MS09-037**](http://technet.microsoft.com/security/bulletin/ms09-037)
</td>
<td style="border:1px solid black;">
[**MS09-041**](http://technet.microsoft.com/security/bulletin/ms09-041)
</td>
<td style="border:1px solid black;">
[**MS09-040**](http://technet.microsoft.com/security/bulletin/ms09-040)
</td>
<td style="border:1px solid black;">
[**MS09-036**](http://technet.microsoft.com/security/bulletin/ms09-036)
</td>
<td style="border:1px solid black;">
[**MS09-042**](http://technet.microsoft.com/security/bulletin/ms09-042)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
[Versión 5.0 de RDP](http://www.microsoft.com/downloads/details.aspx?familyid=027e757d-08d5-4932-b8c4-52ee1be1c864)\*\*\*  
(KB958471) y [versión 5.0 de RDP](http://www.microsoft.com/downloads/details.aspx?familyid=ae72782e-920f-4176-a27b-c3b91d50c7d2) (KB958470)  
(Crítica)  
[Versión 5.1 de RDP](http://www.microsoft.com/downloads/details.aspx?familyid=ae72782e-920f-4176-a27b-c3b91d50c7d2)\*\*\*\*  
(KB958470)  
(Crítica)  
[Versión 5.2 de RDP](http://www.microsoft.com/downloads/details.aspx?familyid=ae72782e-920f-4176-a27b-c3b91d50c7d2)\*\*\*\*  
(KB958470)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Server Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=b5b9228a-66c0-49e6-afde-cc2825a6851f)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=5f80bf0b-898c-46ca-b20c-21e0e729c332)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Outlook Express 5.5 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6f9fcbe9-8496-4d23-8a16-b334157688c2)  
(KB973354)  
(Crítica)  
[Microsoft Outlook Express 6 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=f340af34-b9a0-44fb-b595-dbb346c727bf)  
(KB973354)  
(Crítica)  
[Reproductor de Windows Media 9](http://www.microsoft.com/downloads/details.aspx?familyid=bd7c9fc4-61cb-4c23-9961-6d63f234731c)  
(KB973540)  
(Crítica)  
[Componente de Windows ATL](http://www.microsoft.com/downloads/details.aspx?familyid=c773149a-f4fc-486a-b718-6b8ff7a36ae2)  
(KB973507)  
(Crítica)  
[Control ActiveX del componente de edición DHTML](http://www.microsoft.com/downloads/details.aspx?familyid=223e25d2-83d7-4cb7-85c4-46a42b8110e0)  
(KB973869)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=8ed8bad7-2885-452c-9c34-3982cd498be8)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=240977d6-3581-4058-b9f1-7847e4edcf8a)  
(Importante)
</td>
</tr>
<tr>
<th colspan="9" style="border:1px solid black;">
Windows XP
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-044**](http://technet.microsoft.com/security/bulletin/ms09-044)
</td>
<td style="border:1px solid black;">
[**MS09-039**](http://technet.microsoft.com/security/bulletin/ms09-039)
</td>
<td style="border:1px solid black;">
[**MS09-038**](http://technet.microsoft.com/security/bulletin/ms09-038)
</td>
<td style="border:1px solid black;">
[**MS09-037**](http://technet.microsoft.com/security/bulletin/ms09-037)
</td>
<td style="border:1px solid black;">
[**MS09-041**](http://technet.microsoft.com/security/bulletin/ms09-041)
</td>
<td style="border:1px solid black;">
[**MS09-040**](http://www.microsoft.com/spaintechnet/security/bulletin/ms09-040.mspx)
</td>
<td style="border:1px solid black;">
[**MS09-036**](http://technet.microsoft.com/security/bulletin/ms09-036)
</td>
<td style="border:1px solid black;">
[**MS09-042**](http://technet.microsoft.com/security/bulletin/ms09-042)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Service Pack 2 y Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Versión 5.1 de RDP en Windows XP Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2a8830dd-8fb3-4556-a6e7-2c237235357f)  
(KB958470)  
(Crítica)  
[Versión 5.2 de RDP para Windows XP Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=cf9f9898-10c8-45ab-9df3-85e0b37e6046)\*\*\*\*  
(KB958469)  
(Crítica)  
[Versión 5.2 de RDP en Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=cf9f9898-10c8-45ab-9df3-85e0b37e6046)  
(KB958469)  
(Crítica)  
[Versión 6.0 de RDP para Windows XP Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d1f82d76-eeb2-4ff4-9d2c-46882f214719)\*\*\*\*  
(KB956744)  
(Importante)  
[Versión 6.1 de RDP](http://www.microsoft.com/downloads/details.aspx?familyid=d1f82d76-eeb2-4ff4-9d2c-46882f214719)\*\*\*\*  
(KB956744)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=2e8a68ee-eb24-424c-b084-450636ccaeec)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Outlook Express 6](http://www.microsoft.com/downloads/details.aspx?familyid=c67b5506-00ea-47cc-a0e8-897057b7380c)  
(KB973354)  
(Crítica)  
[Reproductor de Windows Media 9, Reproductor de Windows Media 10 y Reproductor de Windows Media 11](http://www.microsoft.com/downloads/details.aspx?familyid=34b2b14d-5811-4635-ba83-f837dcb03d04)  
(KB973540)  
(Crítica)  
(Windows XP Service Pack 2 solamente)  
[Reproductor de Windows Media 9, Reproductor de Windows Media 10 y Reproductor de Windows Media 11](http://www.microsoft.com/downloads/details.aspx?familyid=ec84c98b-6bc7-442f-9280-d6e204280b2f)  
(KB973540)  
(Crítica)  
(Windows XP Service Pack 3 solamente)  
[Componente de Windows ATL](http://www.microsoft.com/downloads/details.aspx?familyid=4b4c6fc5-e8e6-4d89-a181-e231240468f9)  
(KB973507)  
(Crítica)  
[Control ActiveX del componente de edición DHTML](http://www.microsoft.com/downloads/details.aspx?familyid=bdfcd0c3-7c18-4e63-91dd-d8f82cd89592)  
(KB973869)  
(Crítica)  
[Control ActiveX MSWebDVD de Microsoft](http://www.microsoft.com/downloads/details.aspx?familyid=8b71bcc9-5146-4afc-8847-0af21d7fad36)  
(KB973815)  
(Crítica)  
[Control ActiveX del objeto HtmlInput](http://www.microsoft.com/downloads/details.aspx?familyid=46aa443c-4e7b-4bd5-8b4e-0068c3dc0e79)  
(KB973768)  
(Crítica)  
(Sólo Media Center Edition 2005)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=9c0e5bff-c248-4e87-a83b-82ba52f5299d)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=93490aa7-9985-4658-b0d7-88fb3f27ada0)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=b3331388-1e52-4924-b512-23275a8fde84)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Versión 5.2 de RDP en Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=948da99a-44ed-4390-b1b4-7ed3f15a9cda)  
(KB958469)  
(Crítica)  
[Versión 6.0 de RDP para Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5061615f-fa8f-465f-ac8f-393998b7e91b)\*\*\*\*  
(KB956744)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a1ff2ace-b9dc-4cf3-a151-ac6959bcb3a6)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Outlook Express 6](http://www.microsoft.com/downloads/details.aspx?familyid=ede1a73a-e303-435e-a2c7-0281ce2370da)  
(KB973354)  
(Crítica)  
[Reproductor de Windows Media 10](http://www.microsoft.com/downloads/details.aspx?familyid=bb98187a-8db9-47e4-88ac-15544c5268f6)  
(KB973540)  
(Crítica)  
[Reproductor de Windows Media 11](http://www.microsoft.com/downloads/details.aspx?familyid=9e8b9027-4407-4c31-a2ba-9e094557d467)  
(KB973540)  
(Crítica)  
[Componente de Windows ATL](http://www.microsoft.com/downloads/details.aspx?familyid=2f2b93fc-f977-4f23-af90-c27f744fad0a)  
(KB973507)  
(Crítica)  
[Control ActiveX del componente de edición DHTML](http://www.microsoft.com/downloads/details.aspx?familyid=d04a6959-41a4-4a87-b3ad-7455d8fe8b99)  
(KB973869)  
(Crítica)  
[Control ActiveX MSWebDVD de Microsoft](http://www.microsoft.com/downloads/details.aspx?familyid=85b2dcdb-cea9-4c4a-8ebd-50264e781ade)  
(KB973815)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7b64a454-d383-47e3-b469-b87e2b3c1a9f)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=12e6be68-dc87-450e-927b-3c9b6873eb13)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a6ee7af3-3e39-4866-a893-92bf1c786cd4)  
(Importante)
</td>
</tr>
<tr>
<th colspan="9" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-044**](http://technet.microsoft.com/security/bulletin/ms09-044)
</td>
<td style="border:1px solid black;">
[**MS09-039**](http://technet.microsoft.com/security/bulletin/ms09-039)
</td>
<td style="border:1px solid black;">
[**MS09-038**](http://technet.microsoft.com/security/bulletin/ms09-038)
</td>
<td style="border:1px solid black;">
[**MS09-037**](http://technet.microsoft.com/security/bulletin/ms09-037)
</td>
<td style="border:1px solid black;">
[**MS09-041**](http://technet.microsoft.com/security/bulletin/ms09-041)
</td>
<td style="border:1px solid black;">
[**MS09-040**](http://technet.microsoft.com/security/bulletin/ms09-040)
</td>
<td style="border:1px solid black;">
[**MS09-036**](http://technet.microsoft.com/security/bulletin/ms09-036)
</td>
<td style="border:1px solid black;">
[**MS09-042**](http://technet.microsoft.com/security/bulletin/ms09-042)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Versión 5.2 de RDP](http://www.microsoft.com/downloads/details.aspx?familyid=60c79729-ef01-4630-bd67-ec63e7f8b56b)  
(KB958469)  
(Crítica)  
[Versión 6.0 de RDP](http://www.microsoft.com/downloads/details.aspx?familyid=a37a2d8a-a5ce-4f06-bf07-8cafa16e7a59)\*\*\*\*  
(KB956744)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3a8d8ef9-ad41-4237-9cbb-daecfd8f216c)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=cba78658-899c-428f-8b04-cfe14ce3c255)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Outlook Express 6](http://www.microsoft.com/downloads/details.aspx?familyid=3119ab1e-6729-40a1-b28f-0dab50502be6)  
(KB973354)  
(Crítica)  
[Reproductor de Windows Media 10](http://www.microsoft.com/downloads/details.aspx?familyid=ab054890-983b-4414-ad0a-da1b2d2a4895)  
(KB973540)  
(Crítica)  
[Componente de Windows ATL](http://www.microsoft.com/downloads/details.aspx?familyid=7d9369b5-0c54-4c17-bc62-fba0a7b4728c)  
(KB973507)  
(Crítica)  
[Control ActiveX del componente de edición DHTML](http://www.microsoft.com/downloads/details.aspx?familyid=bfc474c2-e3c5-40df-85d4-4ac666ff0561)  
(KB973869)  
(Crítica)  
[Control ActiveX MSWebDVD de Microsoft](http://www.microsoft.com/downloads/details.aspx?familyid=301ad191-8d3f-41d3-b41c-e2e863893f73)  
(KB973815)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9cb0477f-0656-47f5-bd35-5716e0572fbd)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=52f59c56-2aba-4626-a90e-311e0e73c813)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3fe9c745-d87c-43b0-9b2a-356fb34282b4)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Versión 5.2 de RDP](http://www.microsoft.com/downloads/details.aspx?familyid=57393588-dc96-4bda-ab1e-ae550961e5d4)  
(KB958469)  
(Crítica)  
[Versión 6.0 de RDP](http://www.microsoft.com/downloads/details.aspx?familyid=957c2e01-89a1-4550-aacb-de8ff896d762)\*\*\*\*  
(KB956744)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e132d051-4444-4ef1-9b6f-2d7da9d2e88e)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=58a7c8d9-ec36-46a6-a89b-d8dfd989fda4)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Outlook Express 6](http://www.microsoft.com/downloads/details.aspx?familyid=17bd00e3-810c-4a72-bd13-1b55ffb52a5e)  
(KB973354)  
(Crítica)  
[Reproductor de Windows Media 10](http://www.microsoft.com/downloads/details.aspx?familyid=5890233a-d8f7-490c-8bf5-3ed4bd1c6991)  
(KB973540)  
(Crítica)  
[Componente de Windows ATL](http://www.microsoft.com/downloads/details.aspx?familyid=90e0e014-ed7e-498a-9f61-18bb09a384b3)  
(KB973507)  
(Crítica)  
[Control ActiveX del componente de edición DHTML](http://www.microsoft.com/downloads/details.aspx?familyid=9f502d79-99a8-45dc-9876-2df27e14ffaa)  
(KB973869)  
(Crítica)  
[Control ActiveX MSWebDVD de Microsoft](http://www.microsoft.com/downloads/details.aspx?familyid=2ae71a65-5eee-4dd2-bc79-b7c5a73022bc)  
(KB973815)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=96fbf65f-1db2-432d-92a0-6669d8abaeb0)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2f77ef7b-54f8-4260-b6a6-d62a0f85ef45)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e2a788e7-a9d1-4574-b106-f8ab44c6c4a2)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Versión 5.2 de RDP](http://www.microsoft.com/downloads/details.aspx?familyid=8f88a714-b917-4193-9002-19fa65722028)  
(KB958469)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=96c3f496-7b2f-4dbc-b484-216c9943c2b1)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=187b02bd-73d6-4f72-81d1-d9477d495499)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Outlook Express 6](http://www.microsoft.com/downloads/details.aspx?familyid=7978b921-c5b5-461f-a284-b9848f568aa9)  
(KB973354)  
(Crítica)  
[Componente de Windows ATL](http://www.microsoft.com/downloads/details.aspx?familyid=ad1791b3-8553-4433-a9f7-8b4f857665be)  
(KB973507)  
(Crítica)  
[Control ActiveX del componente de edición DHTML](http://www.microsoft.com/downloads/details.aspx?familyid=82c0bb02-70ad-4605-a1f4-4698adf9f4ac)  
(KB973869)  
(Crítica)  
[Control ActiveX MSWebDVD de Microsoft](http://www.microsoft.com/downloads/details.aspx?familyid=5b8a8958-c3cd-4b24-85a2-1baacf92d218)  
(KB973815)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=11321f48-8997-4b99-982a-3ba4ad3f5992)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=ad55c653-ee6b-4c92-b7f4-3923bb916546)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=4f625d39-29d4-44f9-b4bd-cd99f1ea422d)  
(Importante)
</td>
</tr>
<tr>
<th colspan="9" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-044**](http://technet.microsoft.com/security/bulletin/ms09-044)
</td>
<td style="border:1px solid black;">
[**MS09-039**](http://technet.microsoft.com/security/bulletin/ms09-039)
</td>
<td style="border:1px solid black;">
[**MS09-038**](http://technet.microsoft.com/security/bulletin/ms09-038)
</td>
<td style="border:1px solid black;">
[**MS09-037**](http://technet.microsoft.com/security/bulletin/ms09-037)
</td>
<td style="border:1px solid black;">
[**MS09-041**](http://technet.microsoft.com/security/bulletin/ms09-041)
</td>
<td style="border:1px solid black;">
[**MS09-040**](http://technet.microsoft.com/security/bulletin/ms09-040)
</td>
<td style="border:1px solid black;">
[**MS09-036**](http://technet.microsoft.com/security/bulletin/ms09-036)
</td>
<td style="border:1px solid black;">
[**MS09-042**](http://technet.microsoft.com/security/bulletin/ms09-042)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
[Versión 6.0 de RDP en Windows Vista](http://www.microsoft.com/downloads/details.aspx?familyid=cf95a552-f6fd-4e35-815a-d16c015cd3ea)  
(KB956744)  
(Importante)  
[Versión 6.1 de RDP para Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=cf95a552-f6fd-4e35-815a-d16c015cd3ea)  
(KB956744)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=81fce7bd-f33c-4586-949d-ac40d415f755)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Reproductor de Windows Media 11](http://www.microsoft.com/downloads/details.aspx?familyid=3766aed9-93f5-478e-a5bf-b7ee0b577088)  
(KB973540)  
(Crítica)  
[Componente de Windows ATL](http://www.microsoft.com/downloads/details.aspx?familyid=80de158d-157e-4c21-9154-c1dbd6e57cb3)  
(KB973507)  
(Crítica)  
[Control ActiveX del objeto HtmlInput](http://www.microsoft.com/downloads/details.aspx?familyid=59fefa17-0ad4-4a62-82be-e6a2b7a0aec3)  
(KB973768)  
(Crítica)  
(Sólo Media Center Edition 2005)
</td>
<td style="border:1px solid black;">
[Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=979ac9da-940f-49e7-91a2-b12db3708076)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Vista](http://www.microsoft.com/downloads/details.aspx?familyid=00afd94c-b483-4155-884f-b617acca6e7d)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista solamente: [Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=d42444bb-5030-4b47-87fa-9df3a8c640ff) (KB972591) y [Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=310f3aa6-c264-45a2-b24a-3f178b41830e)\*\*\*\*\* (KB972592)  
(Importante)  
Windows Vista Service Pack 1 solamente:  
[Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=cbf40800-f3b3-43da-ace1-d942d3378ccd) (KB972593) y [Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=87c4a868-b3b5-467d-96a4-633532ab548f)\*\*\*\*\* (KB972594)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d77f406d-11cb-4d19-94ec-938b356c3427)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Versión 6.0 de RDP en Windows Vista x64 Edition](http://www.microsoft.com/downloads/details.aspx?familyid=5e19cef7-2413-4575-9597-c6273a097aad)  
(KB956744)  
(Importante)  
[Versión 6.1 de RDP en Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5e19cef7-2413-4575-9597-c6273a097aad)  
(KB956744)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a6cea61a-4ad9-4e18-bf18-348ae4ae51c4)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Reproductor de Windows Media 11](http://www.microsoft.com/downloads/details.aspx?familyid=64edbd64-9faa-4f54-b0d5-836c683ca7cd)  
(KB973540)  
(Crítica)  
[Componente de Windows ATL](http://www.microsoft.com/downloads/details.aspx?familyid=82940d30-6a30-47ca-b184-2ac96e35c294)  
(KB973507)  
(Crítica)  
[Control ActiveX del objeto HtmlInput](http://www.microsoft.com/downloads/details.aspx?familyid=92de8a2e-2d50-4278-937e-ccb862c5ab8f)  
(KB973768)  
(Crítica)  
(Sólo Media Center Edition 2005)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b9aa04cc-a5c5-47ae-bf0f-250cff275d26)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition](http://www.microsoft.com/downloads/details.aspx?familyid=a0c698aa-a913-4981-8798-6bbb8cacfb86)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition solamente: [Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=d42444bb-5030-4b47-87fa-9df3a8c640ff) (KB972591) y [Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=310f3aa6-c264-45a2-b24a-3f178b41830e)\*\*\*\*\* (KB972592)  
(Importante)  
Windows Vista x64 Edition Service Pack 1 solamente:  
[Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=cbf40800-f3b3-43da-ace1-d942d3378ccd) (KB972593) y [Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=87c4a868-b3b5-467d-96a4-633532ab548f) (KB972594)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7a41b8c1-f955-474e-a08e-5e73964327d1)  
(Moderada)
</td>
</tr>
<tr>
<th colspan="9" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-044**](http://technet.microsoft.com/security/bulletin/ms09-044)
</td>
<td style="border:1px solid black;">
[**MS09-039**](http://technet.microsoft.com/security/bulletin/ms09-039)
</td>
<td style="border:1px solid black;">
[**MS09-038**](http://technet.microsoft.com/security/bulletin/ms09-038)
</td>
<td style="border:1px solid black;">
[**MS09-037**](http://technet.microsoft.com/security/bulletin/ms09-037)
</td>
<td style="border:1px solid black;">
[**MS09-041**](http://technet.microsoft.com/security/bulletin/ms09-041)
</td>
<td style="border:1px solid black;">
[**MS09-040**](http://technet.microsoft.com/security/bulletin/ms09-040)
</td>
<td style="border:1px solid black;">
[**MS09-036**](http://technet.microsoft.com/security/bulletin/ms09-036)
</td>
<td style="border:1px solid black;">
[**MS09-042**](http://technet.microsoft.com/security/bulletin/ms09-042)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Versión 6.1 de RDP](http://www.microsoft.com/downloads/details.aspx?familyid=71c17a87-710b-434d-9b2a-2f471674915a)\*\*  
(KB956744)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=fdc96a07-ed79-4798-8077-b2e9ca64cd0f)\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Reproductor de Windows Media 11](http://www.microsoft.com/downloads/details.aspx?familyid=85d9e69f-99a2-467f-bf37-4b47466a12d4)\*\*  
(KB973540)  
(Crítica)  
[Componente de Windows ATL](http://www.microsoft.com/downloads/details.aspx?familyid=ba423491-6c29-49f2-811b-ac3f9bbc58fc)\*  
(KB973507)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=24c77c27-0b7d-4a35-a871-b453f90e5913)\*  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits únicamente: [Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=cbf40800-f3b3-43da-ace1-d942d3378ccd) (KB972593) y [Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=87c4a868-b3b5-467d-96a4-633532ab548f) (KB972594)\*\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=62f2e0a6-5e68-41c7-a851-d99bcff6ff3e)\*  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Versión 6.1 de RDP](http://www.microsoft.com/downloads/details.aspx?familyid=f095d2d5-4513-4ae1-96c7-cbcf83304261)\*\*  
(KB956744)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8e3afba4-6761-4b3d-98bb-4b4145e27b7f)\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Reproductor de Windows Media 11](http://www.microsoft.com/downloads/details.aspx?familyid=9501c8c2-a526-4661-8cba-7847bace1aa0)\*\*  
(KB973540)  
(Crítica)  
[Componente de Windows ATL](http://www.microsoft.com/downloads/details.aspx?familyid=b9311953-889a-415f-a396-250a005e95cd)\*  
(KB973507)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=48d0432e-704a-4bbb-b0a1-cd14069a8e93)\*  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 únicamente: [Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=cbf40800-f3b3-43da-ace1-d942d3378ccd) (KB972593) y [Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=87c4a868-b3b5-467d-96a4-633532ab548f) (KB972594)\*\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6e5d1db9-efef-4112-8138-62f14670cf0d)\*  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Versión 6.1 de RDP](http://www.microsoft.com/downloads/details.aspx?familyid=65d0af4e-22a2-4524-a003-2f4858012fa8)  
(KB956744)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=aa1bb13a-5905-48c4-8e74-a41104593046)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Componente de Windows ATL](http://www.microsoft.com/downloads/details.aspx?familyid=e5612bb4-5f37-4b38-bd2e-f198c413371c)  
(KB973507)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c119223c-f4e0-449b-8e7b-a6bf11c98f94)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium únicamente: [Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=cbf40800-f3b3-43da-ace1-d942d3378ccd) (KB972593) y [Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=87c4a868-b3b5-467d-96a4-633532ab548f) (KB972594)  
(Importante
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4b813c74-b2ae-4962-9ebb-1311193d9e2d)  
(Moderada)
</td>
</tr>
</table>
 
**Notas para Windows Server 2008**

**\*Instalación de Server Core de Windows Server 2008 afectada.** Para ediciones compatibles de Windows Server 2008, esta actualización se aplica con la misma clasificación de gravedad, independientemente de si Windows Server 2008 se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**\*\*Instalación principal de servidor de Windows Server 2008 no afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 si Windows Server 2008 se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**Notas para MS09-044**

\*\*\*Los usuarios de la versión 5.0 de RDP en Microsoft Windows 2000 Service Pack 4 deben instalar KB958471 y KB958470.

\*\*\*\*Los administradores pueden haber instalado manualmente esta descarga inmediata.

Vea también la subsección "Software de cliente para Mac", en la sección **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

**Nota para MS09-036**

\*\*\*\*\*Debido a que IIS 7.0 no se ejecuta en Windows Vista Starter y Windows Vista Home Basic, las siguientes ediciones no están afectadas: Windows Vista Starter (32 bits), Windows Vista Home Basic (32 bits) y Windows Vista Home Basic (64 bits).

#### Software de cliente para Mac

 
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
Escritorio remoto
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-044**](http://technet.microsoft.com/security/bulletin/ms09-044)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Cliente de Conexión a Escritorio remoto para Mac
</td>
<td style="border:1px solid black;">
[Cliente de Conexión a Escritorio remoto de Microsoft para Mac 2.0](http://www.microsoft.com/downloads/details.aspx?familyid=cd9ec77e-5b07-4332-849f-046611458871)\*  
(Importante)
</td>
</tr>
</table>
 
**Notas para MS09-044**

\*Esta descarga actualiza Cliente de Conexión a Escritorio remoto para Mac 2.0 a Cliente para Conexión a Escritorio remoto para Mac 2.0.1, que corrige la vulnerabilidad.

Vea también la subsección "Componentes y sistema operativo Windows", en la sección **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

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
Conjuntos de programas, sistemas y componentes de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-043**](http://technet.microsoft.com/security/bulletin/ms09-043)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office XP
</td>
<td style="border:1px solid black;">
[Microsoft Office XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=60e2e4e7-aa75-441d-b6fc-7e850bf8e580)  
(KB947320)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2003
</td>
<td style="border:1px solid black;">
[Microsoft Office 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=95c94c9a-6aca-42fb-9679-3234f06c72f7)  
(KB947319)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Office Web Components
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-043**](http://technet.microsoft.com/security/bulletin/ms09-043)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2000 Web Components
</td>
<td style="border:1px solid black;">
[Microsoft Office 2000 Web Components Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=60e2e4e7-aa75-441d-b6fc-7e850bf8e580)  
(KB947320)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office XP Web Components
</td>
<td style="border:1px solid black;">
[Microsoft Office XP Web Components Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=60e2e4e7-aa75-441d-b6fc-7e850bf8e580)  
(KB947320)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2003 Web Components
</td>
<td style="border:1px solid black;">
[Microsoft Office 2003 Web Components Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=95c94c9a-6aca-42fb-9679-3234f06c72f7)  
(KB947319)  
(Crítica)  
[Microsoft Office 2003 Web Components Service Pack 1 para 2007 Microsoft Office System](http://www.microsoft.com/downloads/details.aspx?familyid=644008e0-77c9-4a02-ac9b-e30d0930c4be)\*  
(KB947318)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Otro software de Office
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-043**](http://technet.microsoft.com/security/bulletin/ms09-043)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office Small Business Accounting 2006
</td>
<td style="border:1px solid black;">
[Microsoft Office Small Business Accounting 2006](http://www.microsoft.com/downloads/details.aspx?familyid=0d77ddb3-4d34-4cfe-913b-d05981f59a82)  
(KB968377)  
(Crítica)
</td>
</tr>
</table>
 
**Notas para MS09-043**

\*SQL Server 2008 y Microsoft Forefront Threat Management Gateway Medium Business Edition redistribuyen el componente afectado Office 2003 Web Components para 2007 Microsoft Office System. La actualización del componente Office 2003 Web Components para 2007 Microsoft Office System detecta SQL Server 2008 y Microsoft Forefront Threat Management Gateway Medium Business Edition y ofrecerá la actualización a los clientes.

Vea también las demás subsecciones, en la sección **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador del boletín. Este boletín abarca varias categorías de software.

#### Herramientas y software para desarrolladores de Microsoft

 
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
Microsoft Visual Studio
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-043**](http://technet.microsoft.com/security/bulletin/ms09-043)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Visual Studio .NET 2003
</td>
<td style="border:1px solid black;">
[Microsoft Visual Studio .NET 2003 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=ba2915a0-f5f4-4e18-b0c0-534d2a948585)  
(KB969172)  
(Crítica)
</td>
</tr>
</table>
 
**Nota para MS09-043**

Vea también las demás subsecciones, en la sección **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador del boletín. Este boletín abarca varias categorías de software.

#### Software de servidor y seguridad de Microsoft

 
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
Microsoft Internet Security and Acceleration Server
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-043**](http://technet.microsoft.com/security/bulletin/ms09-043)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Internet Security and Acceleration Server 2004
</td>
<td style="border:1px solid black;">
[Microsoft Internet Security and Acceleration Server 2004 Standard Edition Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=8f79a073-27e8-46ef-87d8-f09b93521326)\*  
(KB947826)  
(Crítica)  
[Microsoft Internet Security and Acceleration Server 2004 Enterprise Edition Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=8f79a073-27e8-46ef-87d8-f09b93521326)  
(KB947826)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Internet Security and Acceleration Server 2006
</td>
<td style="border:1px solid black;">
[Microsoft Internet Security and Acceleration Server 2006 Standard Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=8f79a073-27e8-46ef-87d8-f09b93521326)  
(KB947826)  
(Crítica)  
[Microsoft Internet Security and Acceleration Server 2006 Enterprise Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=8f79a073-27e8-46ef-87d8-f09b93521326)  
(KB947826)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft BizTalk Server
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-043**](http://technet.microsoft.com/security/bulletin/ms09-043)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft BizTalk Server 2002
</td>
<td style="border:1px solid black;">
[Microsoft BizTalk Server 2002](http://www.microsoft.com/downloads/details.aspx?familyid=495839b6-0322-4755-997d-4a7762c53333)  
(KB971388)  
(Crítica)
</td>
</tr>
</table>
 
**Notas para MS09-043**

\*Microsoft ISA Server 2004 Standard Edition se proporciona como un producto independiente. Microsoft ISA Server 2004 Standard Edition también se proporciona como un componente de Windows Small Business Server 2003 Premium Edition Service Pack 1 y Windows Small Business Server 2003 R2 Premium Edition.

Vea también las demás subsecciones, en la sección **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador del boletín. Este boletín abarca varias categorías de software.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://go.microsoft.com/fwlink/?linkid=69903). [TechNet Security Center](http://go.microsoft.com/fwlink/?linkid=21171) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://www.microsoft.com/spain/protect/default.mspx), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS07-036"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Nota** A partir del 1 de agosto de 2009, Microsoft dejó de ofrecer soporte técnico a Office Update y Office Update Inventory Tool. Para seguir obteniendo las actualizaciones más recientes para los productos de Microsoft, use [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747). Para obtener más información, vea [Acerca de Microsoft Office Update: Preguntas más frecuentes](http://office.microsoft.com/en-us/downloads/fx010402221033.aspx).

**Consejos para la detección y la implementación**

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747).

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://go.microsoft.com/fwlink/?linkid=21134).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar con rapidez y fiabilidad las actualizaciones críticas y de seguridad más recientes en sistemas operativos Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://go.microsoft.com/fwlink/?linkid=50120).

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. La siguiente versión de SMS, System Center Configuration Manager 2007, ya está disponible; consulte también [System Center Configuration Manager 2007](http://technet.microsoft.com/en-us/library/bb735860.aspx). Para obtener más información acerca de cómo pueden utilizar los administradores SMS 2003 para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar Security Update Inventory Tool (SUIT) como ayuda para implementar las actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://www.microsoft.com/spain/configurationmanager/default.aspx).

**Nota** SMS usa las herramientas Microsoft Baseline Security Analyzer para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=33387) y en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet2.microsoft.com/windowsvista/en/library/4279e239-37a4-44aa-aec5-4e70fe39f9de1033.mspx?mfr=true) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Microsoft Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Microsoft Knowledge Base, artículo 894199](http://support.microsoft.com/kb/894199): Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones nuevas, revisadas y publicadas para productos de Microsoft distintos de Microsoft Windows](http://technet.microsoft.com/en-us/wsus/dd573344.aspx).

#### Microsoft Active Protections Program (MAPP)

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumeradas en [Asociados de Microsoft Active Protections Program (MAPP)](http://www.microsoft.com/security/msrc/mapp/partners.mspx).

#### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de actualizaciones](http://go.microsoft.com/fwlink/?linkid=21168) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](http://support.microsoft.com/kb/913086).

**Comunidad de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [IT Pro Security Community](http://go.microsoft.com/fwlink/?linkid=21164) (en inglés).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

-   Alexander Pfandt, de [Digitiria](http://www.digitaria.com/), por informar de un problema descrito en MS09-036
-   Ryan Smith y Alex Wheeler, de [IBM ISS X-Force](http://www.iss.net/), por informar del problema descrito inicialmente en MS09-037
-   Robert Freeman, de [IBM ISS X-Force](http://www.iss.net/), por informar de un problema descrito en MS09-037
-   David Dewey, de [IBM ISS X-Force](http://www.iss.net/), por informar de un problema descrito en MS09-037
-   Ryan Smith, de [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de dos problemas descritos en MS09-037
-   Vinay Anantharaman, de [Adobe Systems, Inc.](http://www.adobe.com/), por informar de dos problemas descritos en MS09-038
-   [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS09-039
-   LiGen, de [National University of Defense Technology](http://english.nudt.edu.cn/), por informar de un problema descrito en MS09-039
-   Nikita Tarakanov, de [Positive Technologies Research Team](http://en.securitylab.ru/lab/), por informar de un problema descrito en MS09-040
-   Cody Pierce, de [TippingPoint DVLabs](http://dvlabs.tippingpoint.com/), por informar de un problema descrito en MS09-041
-   Peter Vreugdenhil, de [Zero Day Initiative](http://www.zerodayinitiative.com/), por informar de un problema descrito en MS09-043
-   Peter Vreugdenhil, de [Zero Day Initiative](http://www.zerodayinitiative.com/), y Haifei Li, de [FortiGuard Global Security Research Team](http://www.fortiguardcenter.com/) de Fortinet, por informar de un problema descrito en MS09-043
-   Sean Larsson, de [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS09-043
-   Wushi de [Team509](http://www.team509.com/), en colaboración con Zero Day Initiative, por informar de un problema descrito en MS09-044
-   Yamata Li, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de un problema descrito en MS09-044

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Los clientes de Estados Unidos y Canadá pueden recibir soporte técnico del [soporte de seguridad](http://go.microsoft.com/fwlink/?linkid=21131) o en el teléfono 1-866-PCSAFETY. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de las opciones de asistencia disponibles, visite [Ayuda y soporte técnico de Microsoft](http://support.microsoft.com/).
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (11 de agosto de 2009): Publicación del resumen del boletín.
-   V1.1 (13 de agosto de 2009): Se ha corregido la lista de actualizaciones de RDP para Windows XP Service Pack 2 y Windows XP Service Pack 3 de MS09-044 para que coincidan con el boletín. Se han cambiado los requisitos de reinicio para MS09-037, MS09-042 y MS09-044.
-   V2.0 (25 de agosto de 2009): Para MS09-044 se ha corregido el vínculo de descarga para la versión 5.2 de RDP para Windows XP Service Pack 2 (KB958469). También se ha corregido la nota al pie que indicaba una secuencia de instalación errónea para KB958471 y KB958470. Los clientes que han instalado correctamente estas actualizaciones no tienen que volver a instalarlas.
-   V3.0 (8 de septiembre de 2009): Microsoft ha vuelto a publicar MS09-037 para ofrecer nuevas actualizaciones para el control ActiveX del objeto HtmlInput en Windows XP Media Center Edition 2005 y en todas las ediciones compatibles de Windows Vista.
-   V4.0 (27 de octubre de 2009): Microsoft ha vuelto a publicar MS09-043 para ofrecer de nuevo la actualización para Microsoft Office 2003 Service Pack 3 y Microsoft Office 2003 Web Components Service Pack 3 para corregir un problema de detección. Se trata únicamente de un cambio de detección; no había cambios en los archivos binarios. Los clientes que han actualizado correctamente sus sistemas no necesitan volver a instalar esta actualización.

*Built at 2014-04-18T01:50:00Z-07:00*
