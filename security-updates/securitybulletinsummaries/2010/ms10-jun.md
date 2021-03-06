---
TOCTitle: 'MS10-JUN'
Title: Microsoft Security Bulletin Summary for junio 2010
ms:assetid: 'ms10-jun'
ms:contentKeyID: 61225414
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms10-jun(v=Security.10)'
---

Microsoft Security Bulletin Summary for junio 2010
==================================================

Publicado: martes, 8 de junio de 2010 | Actualizado: martes, 13 de septiembre de 2011

**Versión:** 2.0

Este resumen del boletín enumera los boletines de seguridad publicados para junio de 2010.

Con la publicación de los boletines de junio de 2010, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 3 de junio de 2010. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/es-es/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar una conferencia en línea para atender las consultas de los clientes sobre estos boletines el 9 de junio de 2010, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de junio](https://msevents.microsoft.com/cui/webcasteventdetails.aspx?eventid=1032427727&eventcategory=4&culture=en-us&countrycode=us). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/es-es/security/bulletin/summary).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad y de alta prioridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información** **adicional**.

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms10-033">MS10-033</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en la descompresión de medios</strong> <strong>podrían</strong> <strong>permitir la ejecución remota de código (979902)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario abre un archivo multimedia especialmente diseñado o recibe contenido por secuencias especialmente diseñado de un sitio web o de cualquier aplicación que proporcione contenido web. Un intruso que aprovechara estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario local. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms10-034">MS10-034</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa de bits de interrupción de ActiveX (980195)</strong><br />
<br />
Esta actualización de seguridad corrige dos vulnerabilidades de las que se ha informado de forma privada para el software de Microsoft. Esta actualización de seguridad se considera crítica para todas las ediciones compatibles de Microsoft Windows 2000, Windows XP, Windows Vista y Windows 7, y moderada para todas las ediciones compatibles de Windows Server 2003, Windows Server2008 y Windows Server 2008 R2.<br />
<br />
Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada que ejecute un control ActiveX específico mediante Internet Explorer. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos. Esta actualización también incluye bits de interrupción para cuatro controles ActiveX de terceros.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms10-035">MS10-035</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (982381)</strong><br />
<br />
Esta actualización de seguridad resuelve cinco vulnerabilidades de las que se ha informado de forma privada y una vulnerabilidad de la que se ha informado de forma pública en Internet Explorer. La más grave de las vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms10-032">MS10-032</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en los controladores en modo</strong> <strong>kernel</strong> <strong>de Windows</strong> <strong>podrían</strong> <strong>permitir la elevación de privilegios (979559)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma pública y una vulnerabilidad de la que se ha informado de forma privada en los controladores en modo kernel de Windows. Las vulnerabilidades podrían permitir elevación de privilegios si un usuario consulta el contenido representado en una fuente TrueType especialmente diseñada.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms10-036">MS10-036</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en la validación COM en Microsoft Office podría permitir la ejecución remota de código (983235)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en la validación COM en Microsoft Office. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo de Excel, Word, Visio, Publisher o PowerPoint especialmente diseñado con una versión afectada de Microsoft Office. La vulnerabilidad no puede aprovecharse automáticamente mediante el correo electrónico. Para que se realice el ataque, un usuario debe abrir los datos adjuntos enviados en un mensaje de correo electrónico.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms10-037">MS10-037</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el controlador de</strong> <strong>OpenType</strong> <strong>CFF (Compact Font</strong> <strong>Format) podría permitir la elevación de privilegios (980218)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en el controlador OpenType CFF (Compact Font Format) de Windows. La vulnerabilidad podría permitir elevación de privilegios si un usuario consulta el contenido representado en una fuente CFF especialmente diseñada. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local. Los usuarios anónimos o los usuarios remotos no pueden aprovechar esta vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms10-038">MS10-038</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Office Excel</strong> <strong>podrían</strong> <strong>permitir la ejecución remota de código (2027452)</strong><br />
<br />
Esta actualización de seguridad resuelve catorce vulnerabilidades de las que se ha informado de forma privada en Microsoft Office. Las siete vulnerabilidades más graves podrían permitir la ejecución remota de código si un usuario abre un archivo de Excel especialmente diseñado. Un intruso que aprovechara cualquiera de estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario local. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms10-039">MS10-039</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en</strong> <strong>Microsoft SharePoint</strong> <strong>podrían</strong> <strong>permitir la elevación de privilegios (2028554)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y dos vulnerabilidades de las que se ha informado de forma privada en Microsoft SharePoint. La vulnerabilidad más grave podría permitir la elevación de privilegios si un atacante convence a un usuario de un sitio de SharePoint atacado para hacer clic en un vínculo especialmente diseñado.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office, software de servidor de Microsoft</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms10-040">MS10-040</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Internet</strong> <strong>InformationServices</strong> <strong>podría permitir la ejecución remota de código (982666)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Internet Information Services (IIS). La vulnerabilidad podría permitir la ejecución remota de código si un usuario recibe una solicitud HTTP especialmente diseñada. Un atacante que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms10-041">MS10-041</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft .NET Framework podría permitir la alteración (981343)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública en Microsoft .NET Framework. La vulnerabilidad podría permitir la alteración de datos en el contenido XML firmado sin que se detecte. En las aplicaciones personalizadas, la repercusión de seguridad depende del modo en que se usa el contenido firmado en la aplicación específica. Los escenarios en los que los mensajes XML firmados se transmiten a través de un canal seguro (como SSL) no están afectados por esta vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a><br />
Alteración</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, Microsoft .NET Framework</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de nivel de evaluación de explotabilidad decreciente y, a continuación, por identificador de CVE. Sólo se incluyen las vulnerabilidades que tiene una clasificación de gravedad de crítica o importante en los boletines.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de que se publique código funcional que aproveche la vulnerabilidad en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Debe revisar cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/es-es/security/cc998259.aspx).
  
| Identificador del boletín                                                 | Título de vulnerabilidad                                                                     | Identificador CVE                                                                | Evaluación de índice de explotabilidad                                                                                                  | Notas clave                                                                                                                                                                      |  
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| [MS10-032](http://technet.microsoft.com/es-es/security/bulletin/ms10-032) | Vulnerabilidad de creación de ventanas en Win32k                                             | [CVE-2010-0485](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0485) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                        |  
| [MS10-039](http://technet.microsoft.com/es-es/security/bulletin/ms10-039) | Vulnerabilidad de XSS en Help.aspx                                                           | [CVE-2010-0817](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0817) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | Se informó de esta vulnerabilidad por primera vez en el [documento informativo sobre seguridad de Microsoft 983438](http://technet.microsoft.com/es-es/security/advisory/983438) |  
| [MS10-038](http://technet.microsoft.com/es-es/security/bulletin/ms10-038) | Vulnerabilidad de desbordamiento de la pila de objetos en Excel                              | [CVE-2010-0822](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0822) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                        |  
| [MS10-038](http://technet.microsoft.com/es-es/security/bulletin/ms10-038) | Vulnerabilidad de daños en la memoria relacionada con registros en Excel                     | [CVE-2010-0824](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0824) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                        |  
| [MS10-038](http://technet.microsoft.com/es-es/security/bulletin/ms10-038) | Vulnerabilidad de daños en la memoria relacionada con registros en Excel                     | [CVE-2010-1245](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1245) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                        |  
| [MS10-038](http://technet.microsoft.com/es-es/security/bulletin/ms10-038) | Vulnerabilidad de daños en la memoria relacionada con RTD en Excel                           | [CVE-2010-1246](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1246) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                        |  
| [MS10-038](http://technet.microsoft.com/es-es/security/bulletin/ms10-038) | Vulnerabilidad de daños en la memoria relacionada con Excel                                  | [CVE-2010-1247](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1247) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                        |  
| [MS10-038](http://technet.microsoft.com/es-es/security/bulletin/ms10-038) | Vulnerabilidad de daños en la memoria relacionada con HFPicture en Excel                     | [CVE-2010-1248](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1248) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                        |  
| [MS10-038](http://technet.microsoft.com/es-es/security/bulletin/ms10-038) | Vulnerabilidad de daños en la memoria relacionada con Excel                                  | [CVE-2010-1249](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1249) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                        |  
| [MS10-038](http://technet.microsoft.com/es-es/security/bulletin/ms10-038) | Vulnerabilidad de daños en la memoria relacionada con EDG en Excel                           | [CVE-2010-1250](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1250) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                        |  
| [MS10-038](http://technet.microsoft.com/es-es/security/bulletin/ms10-038) | Vulnerabilidad de objetos ADO en Excel                                                       | [CVE-2010-1253](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1253) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                        |  
| [MS10-038](http://technet.microsoft.com/es-es/security/bulletin/ms10-038) | Vulnerabilidad de permisos en XML abierto en Mac Office                                      | [CVE-2010-1254](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1254) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                        |  
| [MS10-035](http://technet.microsoft.com/es-es/security/bulletin/ms10-035) | Vulnerabilidad de daños en la memoria sin inicializar                                        | [CVE-2010-1259](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1259) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                        |  
| [MS10-035](http://technet.microsoft.com/es-es/security/bulletin/ms10-035) | Vulnerabilidad de daños en la memoria                                                        | [CVE-2010-1262](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1262) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                        |  
| [MS10-036](http://technet.microsoft.com/es-es/security/bulletin/ms10-036) | Vulnerabilidad de validación COM                                                             | [CVE-2010-1263](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1263) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                        |  
| [MS10-033](http://technet.microsoft.com/es-es/security/bulletin/ms10-033) | Vulnerabilidad en la descompresión de medios                                                 | [CVE-2010-1879](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1879) | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                        |  
| [MS10-035](http://technet.microsoft.com/es-es/security/bulletin/ms10-035) | Vulnerabilidad de divulgación de información entre dominios                                  | [CVE-2010-0255](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0255) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | Se informó de esta vulnerabilidad por primera vez en el [documento informativo sobre seguridad de Microsoft 980088](http://technet.microsoft.com/es-es/security/advisory/980088) |  
| [MS10-032](http://technet.microsoft.com/es-es/security/bulletin/ms10-032) | Vulnerabilidad de validación incorrecta de datos en Win32k                                   | [CVE-2010-0484](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0484) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                        |  
| [MS10-037](http://technet.microsoft.com/es-es/security/bulletin/ms10-037) | Vulnerabilidad de daños en la memoria relacionada con el controlador de fuentes OpenType CFF | [CVE-2010-0819](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0819) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                        |  
| [MS10-038](http://technet.microsoft.com/es-es/security/bulletin/ms10-038) | Vulnerabilidad de daños en la memoria relacionada con el análisis de registros en Excel      | [CVE-2010-0821](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0821) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                        |  
| [MS10-038](http://technet.microsoft.com/es-es/security/bulletin/ms10-038) | Vulnerabilidad de daños en la memoria relacionada con Excel                                  | [CVE-2010-0823](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0823) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                        |  
| [MS10-038](http://technet.microsoft.com/es-es/security/bulletin/ms10-038) | Vulnerabilidad de daños en la pila de registros en Excel                                     | [CVE-2010-1251](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1251) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                        |  
| [MS10-038](http://technet.microsoft.com/es-es/security/bulletin/ms10-038) | Vulnerabilidad de variables de cadena en Excel                                               | [CVE-2010-1252](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1252) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                        |  
| [MS10-032](http://technet.microsoft.com/es-es/security/bulletin/ms10-032) | Vulnerabilidad de análisis de fuentes TrueType en Win32k                                     | [CVE-2010-1255](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1255) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                        |  
| [MS10-040](http://technet.microsoft.com/es-es/security/bulletin/ms10-040) | Vulnerabilidad de daños en la memoria relacionada con la autenticación de IIS                | [CVE-2010-1256](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1256) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                        |  
| [MS10-033](http://technet.microsoft.com/es-es/security/bulletin/ms10-033) | Vulnerabilidad en la descompresión de medios MJPEG                                           | [CVE-2010-1880](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1880) | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                        |  
| [MS10-041](http://technet.microsoft.com/es-es/security/bulletin/ms10-041) | Vulnerabilidad de omisión de autenticación de truncamiento HMAC de firma XML                 | [CVE-2009-0217](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0217) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | Se trata de una vulnerabilidad de suplantación y alteración                                                                                                                      |  
| [MS10-035](http://technet.microsoft.com/es-es/security/bulletin/ms10-035) | Vulnerabilidad de divulgación de información de toStaticHTML                                 | [CVE-2010-1257](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1257) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | Esta vulnerabilidad también afecta a [MS10-039](http://technet.microsoft.com/es-es/security/bulletin/ms10-039)                                                                   |  
| [MS10-039](http://technet.microsoft.com/es-es/security/bulletin/ms10-039) | Vulnerabilidad de divulgación de información de toStaticHTML                                 | [CVE-2010-1257](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1257) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | Esta vulnerabilidad también afecta [a MS10-035](http://technet.microsoft.com/es-es/security/bulletin/ms10-035)                                                                   |  
| [MS10-039](http://technet.microsoft.com/es-es/security/bulletin/ms10-039) | Vulnerabilidad de denegación de servicio en la página de ayuda de SharePoint                 | [CVE-2010-1264](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1264) | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | (Ninguna)                                                                                                                                                                        |
  
Ubicaciones de descarga y software afectado  
-------------------------------------------
  
Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.
  
**¿Cómo se usan estas tablas?**  
  
Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, se indica un hipervínculo a la actualización de software disponible y también se muestra la clasificación de gravedad de dicha actualización de software.
  
**Nota** Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.
  
#### Componentes y sistema operativo Windows

 
<p> </p>
<table style="border:1px solid black;">
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Windows 2000</td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows XP</td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Server 2003</td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows Vista</td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Server 2008</td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows 7</td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Server 2008 R2</td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=184917"><strong>MS10-032</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191065"><strong>MS10-033</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=185159"><strong>MS10-034</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=190898"><strong>MS10-035</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=190508"><strong>MS10-037</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191788"><strong>MS10-040</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=185042"><strong>MS10-041</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Clasificación de gravedad acumulada</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;">Ninguna</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Windows 2000 Service Pack 4</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=60c8579b-1540-40d8-80a0-956edadd63ce">Microsoft Windows 2000 Service Pack 4</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=a51c53bd-f9c1-4d53-8ed2-034fd57bc75a">Quartz.dll (DirectShow) (DirectX 9)</a><sup>[1]</sup><br />
(KB975562)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=8417c0ac-bb6d-48f1-8237-77a4bdd8ccb2">Tiempo de ejecución de Windows Media Format 9</a><sup>[2]</sup><br />
(KB978695)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=5b5398c1-5b30-4162-95b6-948d9be103bf">Codificador de Windows Media 9 x86</a><br />
(KB979332)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=1f929739-08a1-4faf-9ccf-5f1f43c5bb9e">Asycfilt.dll (componente COM)</a><br />
(KB979482)<br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=d3955983-0079-476e-a488-99713097259c">Microsoft Windows 2000 Service Pack 4</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=0a6c09e5-c655-41a0-a133-78d55267a527">Internet Explorer 5.01 Service Pack 4</a><br />
(Sin clasificación de gravedad)<sup>[1]</sup><br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=e2f27eeb-54be-40be-a00e-72867090b8e7">Internet Explorer 6 Service Pack 1</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=5d645891-31e9-42c4-b12b-eb351473fd0c">Microsoft Windows 2000 Service Pack 4</a><br />
(Importante)</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=5e55ee58-f00a-4237-bddc-492b63a18b96">Microsoft .NET Framework 1.1 Service Pack 1</a><br />
(KB979906)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=43810ead-1fcc-4a97-ad82-00ee42c27bad">Microsoft .NET Framework 2.0 Service Pack 2</a><br />
(KB979909)<br />
(Importante)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=184917"><strong>MS10-032</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191065"><strong>MS10-033</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=185159"><strong>MS10-034</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=190898"><strong>MS10-035</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=190508"><strong>MS10-037</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191788"><strong>MS10-040</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=185042"><strong>MS10-041</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Clasificación de gravedad acumulada</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;">Ninguna</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows XP Service Pack 2 y Windows XP Service Pack 3</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=023a777a-3d83-4a4e-8029-da8b095b074b">Windows XP Service Pack 2 y Windows XP Service Pack 3</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=e77d5af8-e8e0-425c-a809-4cf274e17cc5">Quartz.dll (DirectShow)</a><br />
(KB975562)<br />
(Crítica)<br />
<br />
Windows XP Service Pack 2 únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=bf8b9b46-ba28-4f48-9dac-6a90b7d592d3">Tiempo de ejecución de Windows Media Format 9, Tiempo de ejecución de Windows Media Format 9.5 y Tiempo de ejecución de Windows Media Format 11</a><br />
(KB978695)<br />
(Crítica)<br />
<br />
Windows XP Service Pack 3 únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=ebbccd82-c637-4c88-86ea-d39ae713c085">Tiempo de ejecución de Windows Media Format 9, Tiempo de ejecución de Windows Media Format 9.5 y Tiempo de ejecución de Windows Media Format 11</a><br />
(KB978695)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=5b5398c1-5b30-4162-95b6-948d9be103bf">Codificador de Windows Media 9 x86</a><br />
(KB979332)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=55c05cb8-aa6c-460b-9aa7-084842dab280">Asycfilt.dll (componente COM)</a><br />
(KB979482)<br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=8c3f2e81-c0ea-494a-a47c-4f8982effb49">Windows XP Service Pack 2 y Windows XP Service Pack 3</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=bfe87761-ed9e-4fec-a393-d7fddb919db4">Internet Explorer 6</a><br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=fc02fc7e-ee85-4377-b54c-012fa60a8c9c">Internet Explorer 7</a><br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=9cff9aba-7743-4c33-87c7-37d06ed60a21">Internet Explorer 8</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=b42a17c5-997e-4504-ba5b-bfa62166b460">Windows XP Service Pack 2 y Windows XP Service Pack 3</a><br />
(Importante)</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Windows XP Media Center Edition 2005 únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=c658c108-abd3-4c24-898d-34d490151394">Microsoft .NET Framework 1.0 Service Pack 3</a><br />
(KB979904)<br />
(Importante)<br />
<br />
Windows XP Media Center Edition 2005 y Windows XP Tablet PC Edition 2005 únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=c658c108-abd3-4c24-898d-34d490151394">Microsoft .NET Framework 1.0 Service Pack 3</a><br />
(KB979904)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=5e55ee58-f00a-4237-bddc-492b63a18b96">Microsoft .NET Framework 1.1 Service Pack 1</a><br />
(KB979906)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=1b41e880-d774-4292-b2aa-2a66568142c9">Microsoft .NET Framework 3.5</a><br />
(KB982865)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=43810ead-1fcc-4a97-ad82-00ee42c27bad">Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET 3.5 Service Pack 1</a><br />
(KB979909)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows XP Professional x64 Edition Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=8e3aac9d-7747-435f-9678-f621e314e070">Windows XP Professional x64 Edition Service Pack 2</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=7914fdae-9a7a-4a10-8ce7-c621eb903452">Quartz.dll (DirectShow)</a><br />
(KB975562)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=b56839e3-e7d3-48da-b90c-d403d8dbeed2">Tiempo de ejecución de Windows Media Format 9.5</a><br />
(KB978695)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=80006082-55f2-4857-9d2c-276c758b5555">Tiempo de ejecución de Windows Media Format 9.5 x64 Edition</a><sup>[3]</sup><br />
(KB978695)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=d2887448-9d3c-472f-a0bd-ab083a65eafc">Tiempo de ejecución de Windows Media Format 11</a><br />
(KB978695)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=94c654f0-f70f-4fbd-84de-797be20fc3b9">Codificador de Windows Media 9 x86</a><br />
(KB979332)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=2b7a3cb7-151c-4184-9865-f197ef6ee8e7">Codificador de Windows Media 9 x64</a><br />
(KB979332)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=c110d26e-9a1e-4e47-9ce2-4068f2733a2f">Asycfilt.dll (componente COM)</a><br />
(KB979482)<br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=f3e462fb-df95-4b79-a8bc-5359c2967503">Windows XP Professional x64 Edition Service Pack 2</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=7780af61-a206-49aa-a805-a49bdcbb5419">Internet Explorer 6</a><br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=6c7cda29-161e-49b4-976a-c718c0aa11a0">Internet Explorer 7</a><br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=37cd7533-ddad-4d0d-85c0-1491308e1ff8">Internet Explorer 8</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=dc835b94-3368-4c1c-8f29-40517c73540e">Windows XP Professional x64 Edition Service Pack 2</a><br />
(Importante)</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=5e55ee58-f00a-4237-bddc-492b63a18b96">Microsoft .NET Framework 1.1 Service Pack 1</a><br />
(KB979906)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=1b41e880-d774-4292-b2aa-2a66568142c9">Microsoft .NET Framework 3.5</a><br />
(KB982865)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=43810ead-1fcc-4a97-ad82-00ee42c27bad">Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1</a> (KB979909)<br />
(Importante)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=184917"><strong>MS10-032</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191065"><strong>MS10-033</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=185159"><strong>MS10-034</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=190898"><strong>MS10-035</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=190508"><strong>MS10-037</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191788"><strong>MS10-040</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=185042"><strong>MS10-041</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Clasificación de gravedad acumulada</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Moderada</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Moderada</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Server 2003 Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=79a11dcd-5d88-4d83-beae-6580ef6fc2c0">Windows Server 2003 Service Pack 2</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=fc15c43b-d48f-4872-8f9d-ed973170db9a">Quartz.dll (DirectShow)</a><br />
(KB975562)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=bb580e94-8c02-46f1-b7f6-e7d4373cb1c5">Tiempo de ejecución de Windows Media Format 9.5</a><br />
(KB978695)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=5b5398c1-5b30-4162-95b6-948d9be103bf">Codificador de Windows Media 9 x86</a><br />
(KB979332)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=0ddf95ac-dd49-4cb1-b6f6-bd4e987b0f06">Asycfilt.dll (componente COM)</a><br />
(KB979482)<br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=3c0bd349-aa77-47de-ba1d-1fcc72dcad28">Windows Server 2003 Service Pack 2</a><br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=bfb9acdb-2d9c-4c22-963c-8b9ce247350f">Internet Explorer 6</a><br />
(Moderada)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=f0187b69-3ed9-494c-89f1-90a35e22078c">Internet Explorer 7</a><br />
(Moderada)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=ebab6101-fcf1-4842-b22d-893a20c1c10f">Internet Explorer 8</a><br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=ca49b5b5-db8e-4ebc-9a3c-b1ace09ac3c0">Windows Server 2003 Service Pack 2</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=0761c207-5465-4f42-b61f-bd02efcef27d">Internet Information Services 6.0</a><sup>[1]</sup><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=f82e1b73-7f8b-4f4c-8187-4050a11db44c">Microsoft .NET Framework 1.1 Service Pack 1</a><br />
(KB979907)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=1b41e880-d774-4292-b2aa-2a66568142c9">Microsoft .NET Framework 3.5</a><br />
(KB982865)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=43810ead-1fcc-4a97-ad82-00ee42c27bad">Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1</a><br />
(KB979909)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows Server 2003 x64 Edition Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=f42cc5d4-1bea-4a4a-8a08-b3eb92503588">Windows Server 2003 x64 Edition Service Pack 2</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=d28ecdf7-9fd4-437e-9db7-c6b579248abe">Quartz.dll (DirectShow)</a><br />
(KB975562)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=41faf16f-c7a8-4ce0-b388-a65478576163">Tiempo de ejecución de Windows Media Format 9.5</a><br />
(KB978695)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=80006082-55f2-4857-9d2c-276c758b5555">Tiempo de ejecución de Windows Media Format 9.5 x64 Edition</a><sup>[3]</sup><br />
(KB978695)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=94c654f0-f70f-4fbd-84de-797be20fc3b9">Codificador de Windows Media 9 x86</a><br />
(KB979332)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=2b7a3cb7-151c-4184-9865-f197ef6ee8e7">Codificador de Windows Media 9 x64</a><br />
(KB979332)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=77b1d55c-b015-4863-aab0-6463b90d4bf7">Asycfilt.dll (componente COM)</a><br />
(KB979482)<br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=4aa0ec4f-5502-4f2a-9732-975518c34444">Windows Server 2003 x64 Edition Service Pack 2</a><br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=81644c43-22c0-4c61-b395-3264516516a6">Internet Explorer 6</a><br />
(Moderada)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=50b8ee2e-31f8-473d-83d1-822c89c28070">Internet Explorer 7</a><br />
(Moderada)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=87e13912-f861-4985-ab9d-260a5898dfd4">Internet Explorer 8</a><br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=b0794e7e-c925-4672-b7a5-4bb3f847f045">Windows Server 2003 x64 Edition Service Pack 2</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=023572ff-ce5d-4428-a96b-1245db6ff312">Internet Information Services 6.0</a><sup>[1]</sup><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=5e55ee58-f00a-4237-bddc-492b63a18b96">Microsoft .NET Framework 1.1 Service Pack 1</a><br />
(KB979906)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=1b41e880-d774-4292-b2aa-2a66568142c9">Microsoft .NET Framework 3.5</a><br />
(KB982865)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=43810ead-1fcc-4a97-ad82-00ee42c27bad">Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1</a><br />
(KB979909)<br />
(Importante)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Server 2003 con SP2 para sistemas con Itanium</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=50efb1cf-9d89-4522-929d-f87fd98d6fe8">Windows Server 2003 con SP2 para sistemas con Itanium</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=7f101f4c-dcc8-474c-a844-fe0c45d6697c">Quartz.dll (DirectShow)</a><br />
(KB975562)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=f34bc115-022b-46b0-9517-806bd0fc73c5">Asycfilt.dll (componente COM)</a><br />
(KB979482)<br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=55d9d7f0-f9d9-4833-b5cc-eb87a62da6a8">Windows Server 2003 con SP2 para sistemas con Itanium</a><br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=abcdc3bb-4659-4b63-a9bd-e448f8bed90a">Internet Explorer 6</a><br />
(Moderada)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=123bf547-9005-451f-9eba-97a68037304e">Internet Explorer 7</a><br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=6e76ebea-bde1-4352-a283-dd71c2cc51a1">Windows Server 2003 con SP2 para sistemas con Itanium</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=f1f3e524-8ac6-4210-a3a8-4ffc58a606ea">Internet Information Services 6.0</a><sup>[1]</sup><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=5e55ee58-f00a-4237-bddc-492b63a18b96">Microsoft .NET Framework 1.1 Service Pack 1</a><br />
(KB979906)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=1b41e880-d774-4292-b2aa-2a66568142c9">Microsoft .NET Framework 3.5</a><br />
(KB982865)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=43810ead-1fcc-4a97-ad82-00ee42c27bad">Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1</a><br />
(KB979909)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=184917"><strong>MS10-032</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191065"><strong>MS10-033</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=185159"><strong>MS10-034</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=190898"><strong>MS10-035</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=190508"><strong>MS10-037</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191788"><strong>MS10-040</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=185042"><strong>MS10-041</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Clasificación de gravedad acumulada</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows Vista Service Pack 1 y Windows Vista Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=7cb64633-d2a0-4e38-be35-ec32ea655a04">Windows Vista Service Pack 1 y Windows Vista Service Pack 2</a><br />
(Importante)</td>
<td style="border:1px solid black;">Windows Vista Service Pack 1 solamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=b64107f2-990a-42df-a75a-5bf371709fd6">Quartz.dll (DirectShow)</a><br />
(KB975562)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=75e4c9cb-a55a-4e2a-9c97-60a40353cae3">Asycfilt.dll (componente COM)</a><br />
(KB979482)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=9fab91da-1528-4df9-a2dd-90e57a3c24cf">Codificador de Windows Media 9 x86</a><br />
(KB979332)<br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=2ddaa4b3-1a98-4183-94af-ebdae4e7b76a">Windows Vista Service Pack 1 y Windows Vista Service Pack 2</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=661c9528-917d-4df6-a330-c89f39dc5ce4">Internet Explorer 7</a><br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=640f9216-3e99-46b6-aac8-cd051eedad3c">Internet Explorer 8</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=363b503a-2e1e-4284-a029-9695d2acfcb6">Windows Vista Service Pack 1 y Windows Vista Service Pack 2</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=01382926-2313-4769-a0a5-262c4f9f18a1">Internet Information Services 7.0</a><sup>[1]</sup><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=5e55ee58-f00a-4237-bddc-492b63a18b96">Microsoft .NET Framework 1.1 Service Pack 1</a><br />
(KB979906)<br />
(Importante)<br />
<br />
Windows Vista Service Pack 1 únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=3ffa2aa2-96a6-4317-8a81-c0ab6d570778">Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5</a><br />
(KB979913)<br />
(Importante)<br />
<br />
Windows Vista Service Pack 1 únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=818acb7e-f984-4793-9418-bb01ed8cfb68">Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1</a><br />
(KB979911)<br />
(Importante)<br />
<br />
Windows Vista Service Pack 2 únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=14c2fa85-f73e-4b62-84ca-d5ea7439aebb">Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1</a> (KB979910)<br />
(Importante)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=bbfc4d80-67eb-4deb-9595-cb67942a0df2">Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2</a><br />
(Importante)</td>
<td style="border:1px solid black;">Windows Vista x64 Edition Service Pack 1 solamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=0754addb-2f04-45c9-8594-174b8b8b297c">Quartz.dll (DirectShow)</a><br />
(KB975562)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=c9f033f6-f587-494d-b968-1316f1deed06">Asycfilt.dll (componente COM)</a><br />
(KB979482)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=63bba49e-6d80-47b3-b109-fa9b2392af4f">Codificador de Windows Media 9 x86</a><br />
(KB979332)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=e19aeef8-6bef-45ee-bc9f-3e4b81a58e33">Codificador de Windows Media 9 x64</a><br />
(KB979332)<br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=ddf55e74-dbaa-45f7-ac5b-ae3da24e0e33">Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=d9f5feb0-fa1a-40c1-9971-9b8af6f0b4a5">Internet Explorer 7</a><br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=3076d1ea-7716-4b54-8ec4-660374f14dcb">Internet Explorer 8</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=3f512b86-3a99-47f7-a90e-1ae9b291385c">Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=7fb6f2b8-c7a6-4239-99f3-cf3aacf89b0f">Internet Information Services 7.0</a><sup>[1]</sup><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=5e55ee58-f00a-4237-bddc-492b63a18b96">Microsoft .NET Framework 1.1 Service Pack 1</a><br />
(KB979906)<br />
(Importante)<br />
<br />
Windows Vista x64 Edition Service Pack 1 únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=3ffa2aa2-96a6-4317-8a81-c0ab6d570778">Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5</a><br />
(KB979913)<br />
(Importante)<br />
<br />
Windows Vista x64 Edition Service Pack 1 únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=818acb7e-f984-4793-9418-bb01ed8cfb68">Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1</a><br />
(KB979911)<br />
(Importante)<br />
<br />
Windows Vista x64 Edition Service Pack 2 únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=14c2fa85-f73e-4b62-84ca-d5ea7439aebb">Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1</a><br />
(KB979910)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=184917"><strong>MS10-032</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191065"><strong>MS10-033</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=185159"><strong>MS10-034</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=190898"><strong>MS10-035</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=190508"><strong>MS10-037</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191788"><strong>MS10-040</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=185042"><strong>MS10-041</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Clasificación de gravedad acumulada</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Moderada</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Moderada</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=22d550fe-ba35-4750-a9d6-624858b67c94">Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2</a>\*<br />
(Importante)</td>
<td style="border:1px solid black;">Windows Server 2008 para sistemas de 32 bits únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=18fd814b-51f3-470b-a5bd-97be752298d9">Quartz.dll (DirectShow)</a>\*\*<br />
(KB975562)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=5c5e2dfc-0078-4f2a-9c2e-75e45bb7638e">Asycfilt.dll (componente COM)</a>\*<br />
(KB979482)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=1ce1e47f-b1c3-4480-bafd-74f8b12e2171">Codificador de Windows Media 9 x86</a>\*\*<br />
(KB979332)<br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=a06b9f42-47ac-4ff2-ac32-e4958cdb611e">Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2</a>\*\*<br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=bed14484-7fc5-455d-b996-3192467543cc">Internet Explorer 7</a>\*\*<br />
(Moderada)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=24ed08c7-a474-4458-8269-3b9de5e22385">Internet Explorer 8</a>\*\*<br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=e78ad607-d209-48c4-b0f3-ed4c70993174">Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2</a>\*<br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=84a54246-5d9e-49e2-8170-af48b43f984d">Internet Information Services 7.0</a>\*<sup>[1]</sup><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=5e55ee58-f00a-4237-bddc-492b63a18b96">Microsoft .NET Framework 1.1 Service Pack 1</a>\*\*<br />
(KB979906)<br />
(Importante)<br />
<br />
Windows Server 2008 para sistemas de 32 bits únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=3ffa2aa2-96a6-4317-8a81-c0ab6d570778">Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5</a>\*\*<br />
(KB979913)<br />
(Importante)<br />
<br />
Windows Server 2008 para sistemas de 32 bits únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=818acb7e-f984-4793-9418-bb01ed8cfb68">Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1</a>\*\*<br />
(KB979911)<br />
(Importante)<br />
<br />
Windows Server 2008 para sistemas de 32 bits Service Pack 2 únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=14c2fa85-f73e-4b62-84ca-d5ea7439aebb">Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1</a>\*\*<br />
(KB979910)<br />
(Importante)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=09025626-4116-4a31-8700-215382898ee2">Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2</a>\*<br />
(Importante)</td>
<td style="border:1px solid black;">Windows Server 2008 para sistemas x64 únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=4e40da51-23ee-44f0-9ea0-99bda8cca731">Quartz.dll (DirectShow)</a>\*\*<br />
(KB975562)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=bfc0b62c-2d79-48dd-896f-d05057c02e8c">Asycfilt.dll (componente COM)</a>\*<br />
(KB979482)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=93cc5ace-6382-4a2f-875b-9348b7e198a6">Codificador de Windows Media 9 x86</a>\*\*<br />
(KB979332)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=d650a7d7-5620-4bb7-a7ad-0848dd28dae3">Codificador de Windows Media 9 x64</a>\*\*<br />
(KB979332)<br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=6d0a3f7c-2617-4bc6-a4c7-cda26c6471e1">Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2</a>\*\*<br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=a24554e8-213b-4c24-b062-ec424d64128e">Internet Explorer 7</a>\*\*<br />
(Moderada)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=cf84469b-ce6d-45e8-8336-7b4501c6cf91">Internet Explorer 8</a>\*\*<br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=85f6fc5d-efd1-4351-b4c0-b9b7080e6173">Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2</a>\*<br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=38286e43-89a6-4895-8ff9-69452df38706">Internet Information Services 7.0</a>\*<sup>[1]</sup><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=5e55ee58-f00a-4237-bddc-492b63a18b96">Microsoft .NET Framework 1.1 Service Pack 1</a>\*\*<br />
(KB979906)<br />
(Importante)<br />
<br />
Windows Server 2008 para sistemas x64 únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=3ffa2aa2-96a6-4317-8a81-c0ab6d570778">Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5</a>\*\*<br />
(KB979913)<br />
(Importante)<br />
<br />
Windows Server 2008 para sistemas x64 únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=818acb7e-f984-4793-9418-bb01ed8cfb68">Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1</a>\*\*<br />
(KB979911)<br />
(Importante)<br />
<br />
Windows Server 2008 para sistemas x64 Service Pack 2 únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=14c2fa85-f73e-4b62-84ca-d5ea7439aebb">Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1</a>\*\*<br />
(KB979910)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=0035cfe2-d38d-41cd-b704-ec1feda307d8">Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2</a><br />
(Importante)</td>
<td style="border:1px solid black;">Windows Server 2008 para sistemas con Itanium únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=120c68f5-4575-4e2a-912a-eed52736c403">Quartz.dll (DirectShow)</a><br />
(KB975562)<br />
(Crítica)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=6e5753ab-848d-475f-917d-ba70f70b65f5">Asycfilt.dll (componente COM)</a><br />
(KB979482)<br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=38347fa6-5946-4bb5-9fea-a5b2f4e7c1f2">Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2</a><br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=dee5c0c0-b844-490d-8daf-6e6ec8a39e35">Internet Explorer 7</a><br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=c6f1aae5-e8fd-4121-89b2-b97c571e8223">Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=8ad19eba-9821-48b4-a942-4ee4f002f913">Internet Information Services 7.0</a><sup>[1]</sup><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=5e55ee58-f00a-4237-bddc-492b63a18b96">Microsoft .NET Framework 1.1 Service Pack 1</a><br />
(KB979906)<br />
(Importante)<br />
<br />
Windows Server 2008 para sistemas con Itanium únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=3ffa2aa2-96a6-4317-8a81-c0ab6d570778">Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5</a><br />
(KB979913)<br />
(Importante)<br />
<br />
Windows Server 2008 para sistemas con Itanium únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=818acb7e-f984-4793-9418-bb01ed8cfb68">Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1</a><br />
(KB979911)<br />
(Importante)<br />
<br />
Windows Server 2008 para sistemas con Itanium Service Pack 2 únicamente:<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=14c2fa85-f73e-4b62-84ca-d5ea7439aebb">Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1</a><br />
(KB979910)<br />
(Importante)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=184917"><strong>MS10-032</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191065"><strong>MS10-033</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=185159"><strong>MS10-034</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=190898"><strong>MS10-035</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=190508"><strong>MS10-037</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191788"><strong>MS10-040</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=185042"><strong>MS10-041</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Clasificación de gravedad acumulada</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows 7 para sistemas de 32 bits</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=3e0ff389-4612-4c92-bbff-bb45b5bdfc6a">Windows 7 para sistemas de 32 bits</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=63567e99-087d-4804-953a-f23bdeba7772">Asycfilt.dll (componente COM)</a><br />
(KB979482)<br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=5bce87fe-dcbb-4638-b248-3f0755537b00">Windows 7 para sistemas de 32 bits</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=5c835885-9375-4882-a92f-4d4cfcacc005">Internet Explorer 8</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=969af8d6-f6da-4dd1-a7d7-2de54a5a8978">Windows 7 para sistemas de 32 bits</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=588167cb-f62a-4fb8-8a18-ac15dc322495">Internet Information Services 7.5</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=a49532d7-53f6-4190-aaf6-b1a818924764">Microsoft .NET Framework 3.5.1</a><br />
(KB979916)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows 7 para sistemas x64</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=2b1e4aff-605a-4e94-88f9-135ce35f0646">Windows 7 para sistemas x64</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=6c261dbf-14c6-4071-8523-e8ba8059fa54">Asycfilt.dll (componente COM)</a><br />
(KB979482)<br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=ee68ecd0-5b8a-4c1e-bdee-bd8616558d43">Windows 7 para sistemas x64</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=5cfc5776-0c6b-4092-bc98-94df077c60d8">Internet Explorer 8</a><br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=b069e5b2-aa2d-452e-b687-8734b5ba0051">Windows 7 para sistemas x64</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=1c45d0c8-1629-470b-8167-c6bf66054595">Internet Information Services 7.5</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=a49532d7-53f6-4190-aaf6-b1a818924764">Microsoft .NET Framework 3.5.1</a><br />
(KB979916)<br />
(Importante)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=184917"><strong>MS10-032</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191065"><strong>MS10-033</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=185159"><strong>MS10-034</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=190898"><strong>MS10-035</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=190508"><strong>MS10-037</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191788"><strong>MS10-040</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=185042"><strong>MS10-041</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Clasificación de gravedad acumulada</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Crítica</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Moderada</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Moderada</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Windows Server 2008 R2 para sistemas x64</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=4272277f-b2dd-4406-8bbd-bc461c9923b8">Windows Server 2008 R2 para sistemas x64</a>\*<br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=1331f2bc-7479-4be7-a413-52afb488a330">Asycfilt.dll (componente COM)</a>\*<br />
(KB979482)<br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=901f7c89-02af-4f87-8592-dad318997d77">Windows Server 2008 R2 para sistemas x64</a>\*\*<br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=7c4ff5ae-eadd-431e-b982-d5f179efb8c0">Internet Explorer 8</a>\*\*<br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=45242c7c-3752-44bf-a766-024ad7d28f53">Windows Server 2008 R2 para sistemas x64</a>\*<br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=5d9b7705-6280-4d2e-94fa-3160b3ce5cfa">Internet Information Services 7.5</a>\*<br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=a49532d7-53f6-4190-aaf6-b1a818924764">Microsoft .NET Framework 3.5.1</a>\*<br />
(KB979916)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Windows Server 2008 R2 para sistemas con Itanium</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=7d636f82-e828-468c-ac36-808ff9d37c7f">Windows Server 2008 R2 para sistemas con Itanium</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=7a1ee54f-3f73-4557-9071-5af236e70937">Asycfilt.dll (componente COM)</a><br />
(KB979482)<br />
(Crítica)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=4958b221-2776-43d7-9e1c-1e1cb318a694">Windows Server 2008 R2 para sistemas con Itanium</a><br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=52c04d85-911f-47be-852e-c9bb4934744d">Internet Explorer 8</a><br />
(Moderada)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=0a271fb5-da5b-4a17-9593-e56b9a843b8f">Windows Server 2008 R2 para sistemas con Itanium</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=869e900a-0063-4d8b-9b7c-7d12f6be12cd">Internet Information Services 7.5</a><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=a49532d7-53f6-4190-aaf6-b1a818924764">Microsoft .NET Framework 3.5.1</a><br />
(KB979916)<br />
(Importante)</td>
</tr>
</tbody>
</table>
 

**Notas para Windows Server 2008 y Windows Server 2008 R2**

**\*La instalación de Server** **Core** **está afectada.** Esta actualización se aplica, con la misma clasificación de gravedad, a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, independientemente de si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de MSDN [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx) y [Server Core para Windows Server 2008 R2](http://msdn.microsoft.com/en-us/library/ee391631(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparación de las opciones de instalación Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**\*\*La instalación de Server** **Core** **no está afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de MSDN [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx) y [Server Core para Windows Server 2008 R2](http://msdn.microsoft.com/en-us/library/ee391631(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparación de las opciones de instalación Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**Nota para MS10-033**

<sup>[1]</sup>La actualización para Quartz.dll (Direct Show) (DirectX 9) también se aplica a DirectX 9.0a, DirectX 9.0b y DirectX 9.0c.

<sup>[2]</sup>Este paquete de actualización se aplica a Tiempo de ejecución de Windows Media Format 9 SDK en Microsoft Windows 2000 con la actualización para los reproductores multimedia habilitados para DRM (KB891122). Para obtener más información, vea el [artículo 974316 de Microsoft Knowledge Base](http://support.microsoft.com/kb/974316).

<sup>[3]</sup>Si ha instalado Tiempo de ejecución de Windows Media Format 9.5 x64 Edition, debe aplicar las actualizaciones de seguridad de Tiempo de ejecución de Media Format 9.5 y Tiempo de ejecución de Windows Media Format 9.5 x64 Edition para estar completamente protegido de las vulnerabilidades descritas en MS10-033.

**Nota para MS10-035**

<sup>[1]</sup>Las clasificaciones de gravedad no se aplican a esta actualización porque las vulnerabilidades tratadas en este boletín no afectan a este software. Sin embargo, esta actualización se ofrece para corregir un problema de regresión derivado de [MS09-054](http://technet.microsoft.com/es-es/security/bulletin/ms09-054). Vea [MS10-035](http://technet.microsoft.com/es-es/security/bulletin/ms10-035) para obtener detalles.

**Nota para MS10-040**

<sup>[1]</sup>Este sistema operativo sólo está afectado cuando se ha instalado la protección ampliada para la autenticación. Vea el [artículo 973917 de Microsoft Knowledge Base](http://support.microsoft.com/kb/973917).

#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Conjuntos de programas, sistemas y componentes de Microsoft Office</td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Office para Mac</td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Otro software de Office</td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Identificador</strong> <strong>del</strong> <strong>boletín</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=190554"><strong>MS10-036</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191053"><strong>MS10-038</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191905"><strong>MS10-039</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Clasificación de gravedad acumulada</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Office XP Service Pack 3</td>
<td style="border:1px solid black;">Microsoft Office XP Service Pack 3<sup>[1]</sup><br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=fec14a92-79a1-4281-8ee2-659b2dfd283f">Microsoft Office Excel 2002 Service Pack 3</a><br />
(KB982299)<br />
(Importante)</td>
<td style="border:1px solid black;">No aplicable</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Office 2003 Service Pack 3</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=80fdd134-2a86-4115-aea1-841f19af92e3">Microsoft Office 2003 Service Pack 3</a><br />
(KB982311)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=757b5d8f-ade5-4896-b152-43f76516bcf1">Microsoft Office Excel 2003 Service Pack 3</a><sup>[2]</sup><br />
(KB982133)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=6b6204c1-559f-45a5-8f6c-a1e216192efc">Microsoft Office PowerPoint 2003 Service Pack 3</a><sup>[2]</sup><br />
(KB982157)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=87bac893-81ec-4ede-aca1-a9aa48b92cd4">Microsoft Office Publisher 2003 Service Pack 3</a><sup>[2]</sup><br />
(KB982122)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=1595ada3-bb4f-40f6-8137-23eba918bc8a">Microsoft Office Visio 2003 Service Pack 3</a><sup>[2]</sup><br />
(KB982126)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=d2c40eb5-1149-4466-840c-84f406f64245">Microsoft Office Word 2003 Service Pack 3</a><sup>[2]</sup><br />
(KB982134)<br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=757b5d8f-ade5-4896-b152-43f76516bcf1">Microsoft Office Excel 2003 Service Pack 3</a><br />
(KB982133)<br />
(Importante)</td>
<td style="border:1px solid black;">No aplicable</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">2007 Microsoft Office System Service Pack 1 y 2007 Microsoft Office System Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=6deb4fb0-cbfc-40df-8f62-35fa1db0e167">2007 Microsoft Office System Service Pack 1 y 2007 Microsoft Office System Service Pack 2</a><br />
(KB982312)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=1b2599f0-1e5d-463c-b100-6c6a1b17b2ec">Microsoft Office Excel 2007 Service Pack 1 y Microsoft Office Excel 2007 Service Pack 2</a><sup>[3]</sup><br />
(KB982308)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=decb834d-3958-45cc-a5ae-4283adb2462a">Microsoft Office PowerPoint 2007 Service Pack 1 y Microsoft Office PowerPoint 2007 Service Pack 2</a><sup>[3]</sup><br />
(KB982158)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=6a74b986-1e99-4aa1-828f-757a36896f65">Microsoft Office Publisher 2007 Service Pack 1 y Microsoft Office Publisher 2007 Service Pack 2</a><sup>[3]</sup><br />
(KB982124)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=d5df052e-1f38-4308-bcca-296cff22729b">Microsoft Office Visio 2007 Service Pack 1 y Microsoft Office Visio 2007 Service Pack 2</a><sup>[3]</sup><br />
(KB982127)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=7e9708f0-8cd6-4f0b-8585-bccc54fa2755">Microsoft Office Word 2007 Service Pack 1 y Microsoft Office Word 2007 Service Pack 2</a><sup>[3]</sup><br />
(KB982135)<br />
(Importante)</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=1b2599f0-1e5d-463c-b100-6c6a1b17b2ec">Microsoft Office Excel 2007 Service Pack 1 y Microsoft Office Excel 2007 Service Pack 2</a><sup>[1]</sup><br />
(KB982308)<br />
(Importante)</td>
<td style="border:1px solid black;">No aplicable</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=190554"><strong>MS10-036</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191053"><strong>MS10-038</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191905"><strong>MS10-039</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Clasificación de gravedad acumulada</strong></td>
<td style="border:1px solid black;">Ninguna</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;">Ninguna</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Office 2004 para Mac</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=16c71ab8-9284-407a-856a-93c67995f125">Microsoft Office 2004 para Mac</a><br />
(KB2028866)<br />
(Importante)</td>
<td style="border:1px solid black;">No aplicable</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Office 2008 para Mac</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=d46255bd-6470-4106-9fe2-ea67acd3f1bd">Microsoft Office 2008 para Mac</a><br />
(KB2028864)<br />
(Importante)</td>
<td style="border:1px solid black;">No aplicable</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Convertidor de archivos con formatos XML abiertos para Mac</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=b6ca7b05-cf97-43a2-95eb-7b5caf7c1528">Convertidor de archivos con formatos XML abiertos para Mac</a><br />
(KB2078051)<br />
(Importante)</td>
<td style="border:1px solid black;">No aplicable</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=190554"><strong>MS10-036</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191053"><strong>MS10-038</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191905"><strong>MS10-039</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Clasificación de gravedad acumulada</strong></td>
<td style="border:1px solid black;">Ninguna</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Excel Viewer Service Pack 1 y Microsoft Office Excel Viewer Service Pack 2</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=033b3bf3-7826-4064-b001-11e4dce2d91a">Microsoft Office Excel Viewer Service Pack 1 y Microsoft Office Excel Viewer Service Pack 2</a><br />
(KB982333)<br />
(Importante)</td>
<td style="border:1px solid black;">No aplicable</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 1 y Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=7f89a734-cda4-4abb-9a10-f6dfe560e8d0">Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 1 y Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2</a><br />
(KB982331)<br />
(Importante)</td>
<td style="border:1px solid black;">No aplicable</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Office InfoPath 2003 Service Pack 3</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=4f79d376-0ea2-4218-9200-3c34c83ba336">Microsoft Office InfoPath 2003 Service Pack 3</a><br />
(KB980923)<br />
(Importante)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;">Microsoft Office InfoPath 2007 Service Pack 1 y Microsoft Office InfoPath 2007 Service Pack 2</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=bfa8765a-7970-4feb-996c-7c27d71c97c6">Microsoft Office InfoPath 2007 Service Pack 1 y Microsoft Office InfoPath 2007 Service Pack 2</a><br />
(KB979441)<br />
(Importante)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Office SharePoint Server 2007 Service Pack 1 y Microsoft Office SharePoint Server 2007 Service Pack 2</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=52a55423-f33b-4cd1-919d-806972a553df">Microsoft Office SharePoint Server 2007 Service Pack 1 (ediciones de 32 bits)</a><sup>[1]</sup><br />
(KB979445)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=52a55423-f33b-4cd1-919d-806972a553df">Microsoft Office SharePoint Server 2007 Service Pack 2 (ediciones de 32 bits)</a><sup>[1]</sup><br />
(KB979445)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=4d84a25b-532f-4319-9ab2-90e5b82ebd90">Microsoft Office SharePoint Server 2007 Service Pack 1 (ediciones de 64 bits)</a><sup>[1]</sup><br />
(KB979445)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=4d84a25b-532f-4319-9ab2-90e5b82ebd90">Microsoft Office SharePoint Server 2007 Service Pack 2 (ediciones de 64 bits)</a><sup>[1]</sup><br />
(KB979445)<br />
(Importante)</td>
</tr>
</tbody>
</table>
 

**Notas para MS10-036**

<sup>[1]</sup>Ninguna actualización disponible. Consulte el boletín para obtener más detalles.

<sup>[2]</sup>Además de esta actualización, los clientes también deben instalar la actualización para Microsoft Office 2003 Service Pack 3 (KB982311) con el fin de protegerse de la vulnerabilidad descrita en este boletín.

<sup>[3]</sup>Además de esta actualización, los clientes también deben instalar la actualización para 2007 Microsoft Office System Service Pack 1 y 2007 Microsoft Office System Service Pack 2 (KB982312) con el fin de protegerse de la vulnerabilidad descrita en este boletín.

**Nota para MS10-038**

<sup>[1]</sup>Además de esta actualización, los clientes también deben instalar la actualización de seguridad para Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 1 y Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2 (KB982308) con el fin de estar protegidos de las vulnerabilidades descritas en este boletín.

**Notas para MS10-039**

<sup>[1]</sup>Para las ediciones compatibles de Microsoft Office SharePoint Server 2007, además del paquete de actualización de seguridad KB979445, los clientes también deben instalar la actualización de seguridad para Microsoft Windows SharePoint Services 3.0 (KB983444) con el fin de protegerse de las vulnerabilidades descritas en este boletín.

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Software de servidor de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tbody>
<tr class="odd">
<td style="border:1px solid black;">Windows SharePoint Services</td>
<td style="border:1px solid black;"></td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><strong>Identificador del boletín</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=191905"><strong>MS10-039</strong></a></td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><strong>Clasificación de gravedad acumulada</strong></td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140"><strong>Importante</strong></a></td>
</tr>
<tr class="even">
<td style="border:1px solid black;">Microsoft Windows SharePoint Services 3.0 Service Pack 1 y Microsoft Windows SharePoint Services 3.0 Service Pack 2</td>
<td style="border:1px solid black;"><a href="http://www.microsoft.com/downloads/details.aspx?familyid=3841ceda-d0af-4e5e-8a1a-7dd954850783">Microsoft Windows SharePoint Services 3.0 Service Pack 1 y Microsoft Windows SharePoint Services 3.0 Service Pack 2 (ediciones de 32 bits)</a><br />
(KB983444)<br />
(Importante)<br />
<br />
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=94bc76d4-78e4-4bda-8922-36c3a9d3854f">Microsoft Windows SharePoint Services 3.0 Service Pack 1 y Microsoft Windows SharePoint Services 3.0 Service Pack 2 (ediciones de 64 bits)</a><br />
(KB983444)<br />
(Importante)</td>
</tr>
</tbody>
</table>
 

**Nota para MS10-039**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/bb245732). [TechNet Security Center](http://technet.microsoft.com/es-es/security/default.aspx) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://www.microsoft.com/es-es/security/default.aspx), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS07-036"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Nota** A partir del 1 de agosto de 2009, Microsoft dejará de ofrecer soporte técnico a Office Update y Office Update Inventory Tool. Para seguir obteniendo las actualizaciones más recientes para los productos de Microsoft, use [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747). Para obtener más información, vea [Acerca de Microsoft Office Update: Preguntas más frecuentes](http://office.microsoft.com/en-us/downloads/fx010402221033.aspx).

**Consejos para la detección y la implementación**

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747).

**Microsoft** **Baseline** **Security** **Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://go.microsoft.com/fwlink/?linkid=21134).

**Windows Server** **UpdateServices**

Windows Server Update Services (WSUS) permite a los administradores implementar de un modo rápido y confiable las actualizaciones críticas y de seguridad más recientes en sistemas operativos Microsoft Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://go.microsoft.com/fwlink/?linkid=50120).

**Systems** **Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. La siguiente versión de SMS, System Center Configuration Manager 2007, ya está disponible; consulte también [System Center Configuration Manager 2007](http://technet.microsoft.com/en-us/library/bb735860.aspx). Para obtener más información acerca de cómo pueden utilizar los administradores SMS 2003 para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar Security Update Inventory Tool (SUIT) como ayuda para implementar las actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://go.microsoft.com/fwlink/?linkid=21158).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet2.microsoft.com/windowsvista/en/library/4279e239-37a4-44aa-aec5-4e70fe39f9de1033.mspx?mfr=true) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Microsoft Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Artículo 894199 de Microsoft Knowledge Base](http://support.microsoft.com/kb/894199)
-   : Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones de meses anteriores para Windows Server Update Services](http://technet.microsoft.com/en-us/wsus/bb456965.aspx)
-   . Muestra todas las actualizaciones nuevas, revisadas y publicadas de nuevo para los productos de Microsoft que no sean Microsoft Windows.

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

-   Sebastien Renaud, de [VUPEN Vulnerability Research Team](http://www.vupen.com/), por informar de un problema descrito en MS10-032
-   [Secunia Research](http://secunia.com/)
-   , por colaborar con nosotros en un problema descrito en MS10-032
-   Yamata Li, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de dos problemas descritos en MS10-033
-   Shaun Colley, de [NGS Software](http://www.ngssoftware.com/), por informar de un problema descrito en MS10-034
-   Chris Ries, de Carnegie Mellon University Computing Services, por informar de un problema descrito en MS10-034
-   Chris Weber, de [Casaba Security](http://www.casabasecurity.com/), por informar de un problema descrito en MS10-035 y MS10-039
-   Takeshi Terada, de [Mitsui Bussan Secure Directions, Inc.](http://www.mbsd.jp/), por informar de un problema descrito en MS10-035
-   Michal Zalewski, de [Google Inc.](http://www.google.com/), por informar de un problema descrito en MS10-035
-   Chris Rohlf, de [Matasano Security](http://www.matasano.com/), por informar de un problema descrito en MS10-035
-   Peter Vreugdenhil, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS10-035
-   David Dewey, de [IBM ISS X-Force](http://www.iss.net/), y Ryan Smith, de [Accuvant](http://www.accuvant.com/), anteriormente de [VeriSign iDefense Labs](http://labs.idefense.com/), por colaborar con nosotros en los cambios de defensa en profundidad incluidos en MS10-036
-   Chris Carton, de Laserforce International, en colaboración con [Secunia](http://secunia.com/), por informar de un problema descrito en MS10-037
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS10-038
-   Nicolas Joly, de [VUPEN Vulnerability Research Team](http://www.vupen.com/), por informar de ocho problemas descritos en MS10-038
-   Bing Liu, de [FortiGuard Labs de Fortinet](http://www.fortiguard.com/), por informar de dos problemas descritos en MS10-038
-   Carsten Eiram, de [Secunia](http://secunia.com/), por informar de dos problemas descritos en MS10-038
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS10-038
-   Rick Glaspie, de Gilbert Public Schools en Gilbert, Arizona, por informar de un problema descrito en MS10-038
-   Rik Jones, de Dallas County Community College District, por informar de un problema descrito en MS10-039
-   Arian Evans, de [WhiteHat Security](http://www.whitehatsec.com), por informar del problema de omisión en la validación de solicitud ASP.NET que se corrige en MS10-041 mediante un cambio de defensa en profundidad

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Los clientes de Estados Unidos y Canadá pueden recibir soporte técnico del [soporte de seguridad](http://go.microsoft.com/fwlink/?linkid=21131) o en el teléfono 1-866-PCSAFETY. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de las opciones de asistencia disponibles, visite [Ayuda y soporte técnico de Microsoft](http://support.microsoft.com/).
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (8 de junio de 2010): Publicación del resumen del boletín.
-   V1.1 (9 de junio de 2010): Se han revisado las notas de MS10-033 en la sección **Ubicaciones de descarga y software afectado**.
-   V2.0 (13 de septiembre de 2011): Se ha vuelto a publicar el boletín MS10-035 para ofrecer de nuevo las actualizaciones para Internet Explorer en Microsoft Windows 2000 y Windows XP para corregir un problema de detección. No había cambios en los archivos de la actualización de seguridad. Los clientes que ya han actualizado correctamente sus sistemas no necesitan realizar ninguna acción.

*Built at 2014-04-18T01:50:00Z-07:00*
