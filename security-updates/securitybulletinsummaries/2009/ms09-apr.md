---
TOCTitle: 'MS09-APR'
Title: Resumen del boletín de seguridad de Microsoft de abril 2009
ms:assetid: 'ms09-apr'
ms:contentKeyID: 61225396
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms09-apr(v=Security.10)'
--- 


Resumen del boletín de seguridad de Microsoft de abril 2009
===========================================================

Publicado: martes, 14 de abril de 2009 | Actualizado: jueves, 16 de abril de 2009

**Versión:** 1.1

Este resumen del boletín enumera los boletines de seguridad publicados para abril de 2009.

Con la publicación de los boletines de abril de 2009, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 9 de abril de 2009. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://technet.microsoft.com/security/bulletin/notify) (en inglés).

Microsoft va a realizar una conferencia en línea para atender las consultas de los clientes sobre estos boletines el 15 de abril de 2009, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora a la conferencia en línea del boletín de seguridad de abril](http://msevents.microsoft.com/cui/webcasteventdetails.aspx?eventid=1032395126). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-010">MS09-010</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en los convertidores de texto de WordPad y Office podrían permitir la ejecución remota de código (960477)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma pública y dos vulnerabilidades de las que se ha informado de forma privada en los convertidores de texto de Microsoft WordPad y Microsoft Office. Las vulnerabilidades podrían permitir la ejecución remota de código si se abre un archivo especialmente diseñado en WordPad o Microsoft Office Word. No abra archivos de Microsoft Office, RTF, Write o WordPerfect que procedan de fuentes que no sean de confianza con las versiones afectadas de WordPad o Microsoft Office Word.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-013">MS09-013</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en los servicios HTTP de Windows podrían permitir la ejecución remota de código (960803)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y dos vulnerabilidades de las que se ha informado de forma privada en los servicios HTTP de Microsoft Windows (WinHTTP). La vulnerabilidad más grave podría permitir la ejecución de código remoto. Un atacante que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-011">MS09-011</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft DirectShow podría permitir la ejecución remota de código (961373)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft DirectX. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo MJPEG especialmente diseñado. Un atacante que aprovechara esta vulnerabilidad podría lograr el control completo de un sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-014">MS09-014</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet (963027)</strong><br />
<br />
Esta actualización de seguridad resuelve cuatro vulnerabilidades de las que se ha informado de forma privada y dos vulnerabilidades de las que se ha informado de forma pública en Internet Explorer. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer o si se conecta al servidor de un atacante mediante el protocolo HTTP. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, Internet Explorer</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-009">MS09-009</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Office Excel podrían provocar la ejecución remota de código (968557)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada y otra de la que se ha informado de forma pública en Microsoft Office Excel. Las vulnerabilidades podrían permitir la ejecución remota de código si el usuario abre un archivo de Excel especialmente diseñado. Un atacante que aprovechara estas vulnerabilidades podría obtener el control completo del sistema afectado. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-012">MS09-012</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades del kernel de Windows podrían permitir la elevación de privilegios (959454)</strong><br />
<br />
Esta actualización de seguridad resuelve cuatro vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. Las vulnerabilidades podrían permitir la elevación de privilegios si se permite que un atacante inicie sesión en el sistema y, a continuación, ejecute una aplicación especialmente diseñada. El atacante debe poder ejecutar código en el equipo local para aprovechar esta vulnerabilidad. Un atacante que aprovechara cualquiera de estas vulnerabilidades podría lograr el control total sobre el sistema afectado.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-016">MS09-016</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft ISA Server y Forefront Threat Management Gateway (Medium Business Edition) podrían provocar la denegación de servicio (961759)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada y otra vulnerabilidad de la que se ha informado de forma pública en Microsoft Internet Security and Acceleration (ISA) Server y Microsoft Forefront Threat Management Gateway (TMG), Medium Business Edition (MBE). Estas vulnerabilidades podrían permitir la denegación de servicio si un atacante envía paquetes de red especialmente diseñados al sistema afectado o la divulgación de información si un usuario hace clic en una dirección URL malintencionada o visita un sitio web que incluya contenido controlado por el atacante.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Denegación de servicio</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Forefront Edge Security</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-015">MS09-015</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad de amenaza mixta en SearchPath podría permitir la elevación de privilegios (959426)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública en la función SearchPath de Windows que podría permitir la elevación de privilegios si un usuario descarga un archivo especialmente diseñado en una ubicación específica y, a continuación, abre una aplicación que podría cargar el archivo en determinadas circunstancias.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Moderada</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y de identificador de CVE.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de que se publique código funcional que aproveche la vulnerabilidad en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Debe revisar cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/en-us/security/cc998259.aspx).
  
| Identificador del boletín                                           | Título del boletín                                                                                                                                           | Identificador CVE                                                                    | Evaluación de índice de explotabilidad                                                                                                  | Notas clave                                                                                                                                                                                                                                                                                                  |  
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| [MS09-009](http://technet.microsoft.com/security/bulletin/ms09-009) | Vulnerabilidades en Microsoft Office Excel podrían provocar la ejecución remota de código (968557)                                                           | [CVE-2009-0100](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0100)     | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                                                                                                                                                    |  
| [MS09-009](http://technet.microsoft.com/security/bulletin/ms09-009) | Vulnerabilidades en Microsoft Office Excel podrían provocar la ejecución remota de código (968557)                                                           | [CVE-2009-0238](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0238)     | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | **Esta vulnerabilidad se está aprovechando actualmente en el ecosistema de Internet.**                                                                                                                                                                                                                       |  
| [MS09-010](http://technet.microsoft.com/security/bulletin/ms09-010) | Vulnerabilidades en los convertidores de texto de WordPad y Office podrían permitir la ejecución remota de código (960477)                                   | [CVE-2008-4841](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-4841)     | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | **Esta vulnerabilidad se está aprovechando actualmente en el ecosistema de Internet.**                                                                                                                                                                                                                       |  
| [MS09-010](http://technet.microsoft.com/security/bulletin/ms09-010) | Vulnerabilidades en los convertidores de texto de WordPad y Office podrían permitir la ejecución remota de código (960477)                                   | [CVE-2009-0087](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0087)     | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | Es una vulnerabilidad compleja debido a las múltiples rutas de código. La mayor parte del código que aprovecha la vulnerabilidad producirá resultados incoherentes. Los factores atenuantes predeterminados protegen contra esta situación.                                                                  |  
| [MS09-010](http://technet.microsoft.com/security/bulletin/ms09-010) | Vulnerabilidades en los convertidores de texto de WordPad y Office podrían permitir la ejecución remota de código (960477)                                   | [CVE-2009-0088](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0088)     | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | Esta vulnerabilidad se puede aprovechar, pero sólo afecta a versiones anteriores y a un formato de archivo anterior y poco habitual. Las versiones más recientes, como 2007 Microsoft Office system y Microsoft Office 2003 Service Pack 3, no están afectadas.                                              |  
| [MS09-010](http://technet.microsoft.com/security/bulletin/ms09-010) | Vulnerabilidades en los convertidores de texto de WordPad y Office podrían permitir la ejecución remota de código (960477)                                   | [CVE-2009-0235](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0235)     | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | Esta vulnerabilidad de daños en la memoria se puede aprovechar fácilmente.                                                                                                                                                                                                                                   |  
| [MS09-011](http://technet.microsoft.com/security/bulletin/ms09-011) | Una vulnerabilidad en Microsoft DirectShow podría permitir la ejecución remota de código (961373)                                                            | [CVE-2009-0084](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0084)     | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                                                                                                                                                    |  
| [MS09-012](http://technet.microsoft.com/security/bulletin/ms09-012) | Vulnerabilidades del kernel de Windows podrían permitir la elevación de privilegios (959454)                                                                 | [CVE-2008-1436](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-1436)     | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | **Esta vulnerabilidad se está aprovechando actualmente en el ecosistema de Internet.**                                                                                                                                                                                                                       |  
| [MS09-012](http://technet.microsoft.com/security/bulletin/ms09-012) | Vulnerabilidades del kernel de Windows podrían permitir la elevación de privilegios (959454)                                                                 | [CVE-2009-0078](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0078)     | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | **Esta vulnerabilidad se está aprovechando actualmente en el ecosistema de Internet.**                                                                                                                                                                                                                       |  
| [MS09-012](http://technet.microsoft.com/security/bulletin/ms09-012) | Vulnerabilidades del kernel de Windows podrían permitir la elevación de privilegios (959454)                                                                 | [CVE-2009-0079](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0079)     | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | **Esta vulnerabilidad se está aprovechando actualmente en el ecosistema de Internet.**                                                                                                                                                                                                                       |  
| [MS09-012](http://technet.microsoft.com/security/bulletin/ms09-012) | Vulnerabilidades del kernel de Windows podrían permitir la elevación de privilegios (959454)                                                                 | [CVE-2009-0080](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0080)     | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | **Esta vulnerabilidad se está aprovechando actualmente en el ecosistema de Internet.**                                                                                                                                                                                                                       |  
| [MS09-013](http://technet.microsoft.com/security/bulletin/ms09-013) | Vulnerabilidades en los servicios HTTP de Windows podrían permitir la ejecución remota de código (960803)                                                    | [CVE-2009-0086](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0086)     | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | Es una vulnerabilidad de memoria fácilmente controlable con varias vías de ataque y oportunidades para aprovecharla debido a la amplia difusión del uso de esta tecnología.                                                                                                                                  |  
| [MS09-013](http://technet.microsoft.com/security/bulletin/ms09-013) | Vulnerabilidades en los servicios HTTP de Windows podrían permitir la ejecución remota de código (960803)                                                    | [CVE-2009-0089](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0089)     | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                                                                                                                                    |  
| [MS09-013](http://technet.microsoft.com/security/bulletin/ms09-013) | Vulnerabilidades en los servicios HTTP de Windows podrían permitir la ejecución remota de código (960803)                                                    | [CVE-2009-0550](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0550)\*\* | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | El código que aprovecha la vulnerabilidad es público.                                                                                                                                                                                                                                                        |  
| [MS09-014](http://technet.microsoft.com/security/bulletin/ms09-014) | Actualización de seguridad acumulativa para Internet (963027)                                                                                                | [CVE-2008-2540](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-2540)\*   | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | Los detalles del ataque se han hecho públicos, pero no existe actualmente ninguna vía de ataque para este problema. Para que se aproveche esta vulnerabilidad, el atacante y el usuario deben realizar una serie de pasos complejos, que incluye el almacenamiento de archivos específicos en el escritorio. |  
| [MS09-014](http://technet.microsoft.com/security/bulletin/ms09-014) | Actualización de seguridad acumulativa para Internet (963027)                                                                                                | [CVE-2009-0550](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0550)\*\* | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | El código que aprovecha la vulnerabilidad es público.                                                                                                                                                                                                                                                        |  
| [MS09-014](http://technet.microsoft.com/security/bulletin/ms09-014) | Actualización de seguridad acumulativa para Internet (963027)                                                                                                | [CVE-2009-0551](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0551)     | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                                                                                                                                                    |  
| [MS09-014](http://technet.microsoft.com/security/bulletin/ms09-014) | Actualización de seguridad acumulativa para Internet (963027)                                                                                                | [CVE-2009-0552](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0552)     | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | Los factores atenuantes para Internet Explorer 7 evitan la ejecución de código. Internet Explorer 6 y las versiones anteriores están más expuestas a la vulnerabilidad si no se actualizan con todas las actualizaciones de seguridad.                                                                       |  
| [MS09-014](http://technet.microsoft.com/security/bulletin/ms09-014) | Actualización de seguridad acumulativa para Internet (963027)                                                                                                | [CVE-2009-0553](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0553)     | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | (Ninguna)                                                                                                                                                                                                                                                                                                    |  
| [MS09-014](http://technet.microsoft.com/security/bulletin/ms09-014) | Actualización de seguridad acumulativa para Internet (963027)                                                                                                | [CVE-2009-0554](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0554)     | [**1**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                                                                                                                                    |  
| [MS09-015](http://technet.microsoft.com/security/bulletin/ms09-015) | Una vulnerabilidad de amenaza mixta en SearchPath podría permitir la elevación de privilegios (959426)                                                       | [CVE-2008-2540](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2008-2540)\*   | [**2**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | Los detalles del ataque se han hecho públicos, pero no existe actualmente ninguna vía de ataque para este problema. Para que se aproveche esta vulnerabilidad, el atacante y el usuario deben realizar una serie de pasos complejos, que incluye el almacenamiento de archivos específicos en el escritorio. |  
| [MS09-016](http://technet.microsoft.com/security/bulletin/ms09-016) | Vulnerabilidades en Microsoft ISA Server y Forefront Threat Management Gateway (Medium Business Edition) podrían provocar la denegación de servicio (961759) | [CVE-2009-0077](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0077)     | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | Es muy probable la denegación de servicio basada en servicio. No obstante, no es posible la ejecución de código.                                                                                                                                                                                             |  
| [MS09-016](http://technet.microsoft.com/security/bulletin/ms09-016) | Vulnerabilidades en Microsoft ISA Server y Forefront Threat Management Gateway (Medium Business Edition) podrían provocar la denegación de servicio (961759) | [CVE-2009-0237](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-0237)          | [**3**](http://technet.microsoft.com/en-us/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | Es posible la divulgación de información. La ejecución de código es muy improbable.                                                                                                                                                                                                                          |
  
\*Este par de vulnerabilidades, a las que se ha asignado el mismo número CVE, se corrige en dos actualizaciones de seguridad. Consulte los boletines correspondientes para obtener más información.
  
\*\*Este par de vulnerabilidades, a las que se ha asignado el mismo número CVE, se corrige en dos actualizaciones de seguridad. Consulte los boletines correspondientes para obtener más información.
  
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
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Microsoft Windows 2000  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-010**](http://technet.microsoft.com/security/bulletin/ms09-010)
</td>
<td style="border:1px solid black;">
[**MS09-013**](http://technet.microsoft.com/security/bulletin/ms09-013)
</td>
<td style="border:1px solid black;">
[**MS09-011**](http://technet.microsoft.com/security/bulletin/ms09-011)
</td>
<td style="border:1px solid black;">
[**MS09-014**](http://technet.microsoft.com/security/bulletin/ms09-014)
</td>
<td style="border:1px solid black;">
[**MS09-012**](http://technet.microsoft.com/security/bulletin/ms09-012)
</td>
<td style="border:1px solid black;">
[**MS09-015**](http://technet.microsoft.com/security/bulletin/ms09-015)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
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
(Sin clasificación de gravedad)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=552d322a-5282-42c7-9c1e-1d8c494a7318)  
(KB923561)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=39d5468e-5733-4c3e-9e75-3adac8ac8cb9)  
(Crítica)
</td>
<td style="border:1px solid black;">
[DirectX 8.1](http://www.microsoft.com/downloads/details.aspx?familyid=0ec5b7c7-13d3-467a-b24e-3cc6fb47adf6)  
(Crítica)  
[DirectX 9.0](http://www.microsoft.com/downloads/details.aspx?familyid=8b98ed5c-a3ab-45a7-a61e-349eae304bc6)\*\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 5.01 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=7799fd05-5b26-449f-8a14-50227c9164d1)  
(Crítica)  
[Microsoft Internet Explorer 6 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=87f0c380-5c31-4099-a6a9-c12f9d69b03b)  
(Crítica)
</td>
<td style="border:1px solid black;">
Actualización del servicio de transacciones de MSDTC:  
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=52b756e7-636f-4d9e-8a17-dbf467bfbe4d)  
(KB952004)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=c4e408d7-6716-4a12-ad3a-8029667f5c84)  
(Sin clasificación de gravedad)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows XP
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-010**](http://technet.microsoft.com/security/bulletin/ms09-010)
</td>
<td style="border:1px solid black;">
[**MS09-013**](http://technet.microsoft.com/security/bulletin/ms09-013)
</td>
<td style="border:1px solid black;">
[**MS09-011**](http://technet.microsoft.com/security/bulletin/ms09-011)
</td>
<td style="border:1px solid black;">
[**MS09-014**](http://technet.microsoft.com/security/bulletin/ms09-014)
</td>
<td style="border:1px solid black;">
[**MS09-012**](http://technet.microsoft.com/security/bulletin/ms09-012)
</td>
<td style="border:1px solid black;">
[**MS09-015**](http://technet.microsoft.com/security/bulletin/ms09-015)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
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
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows XP Service Pack 2 y Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=50a8519a-503e-43dd-a78a-c1bc764fd213)  
(KB923561)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=35af4151-1858-4c9a-85e4-9ff45feca1a4)  
(Crítica)
</td>
<td style="border:1px solid black;">
[DirectX 9.0](http://www.microsoft.com/downloads/details.aspx?familyid=feb5d821-f210-40e8-b1aa-2ca3170df8df)\*\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=052c29fc-e8df-402c-9ab1-1079bc738e1b)  
(Crítica)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=55d6729a-9f96-4da4-b564-676c0a0c9390)  
(Crítica)
</td>
<td style="border:1px solid black;">
Actualización del servicio de transacciones de MSDTC:  
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=90fe715e-8190-43e9-9c43-df5be564d923)  
(KB952004)  
(Importante)  
Actualización de aislamiento de servicio de Windows:  
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=73d2324f-be59-4b0c-b1ac-9876a13c2c03)  
(KB956572)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=3de0684d-605c-489b-bdc7-08bce9b2d4f6)  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=323f4211-5add-4e02-bce1-e5a1b489982c)  
(KB923561)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=49b16f0f-f6c3-4ca8-8041-392f4f7b5bbb)  
(Crítica)
</td>
<td style="border:1px solid black;">
[DirectX 9.0](http://www.microsoft.com/downloads/details.aspx?familyid=f1be8b7c-4874-4342-99b3-76ff725fbb9a)\*\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=84c62211-2e82-4ccc-9f9b-26462b026d86)  
(Crítica)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=191c2f20-89ae-4e1c-bdd4-24b4abfe6b6c)  
(Crítica)
</td>
<td style="border:1px solid black;">
Actualización del servicio de transacciones de MSDTC:  
[Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a794c32a-9a0c-47d9-9c57-ff5d4a8e4944)  
(KB952004)  
(Importante)  
Actualización de aislamiento de servicio de Windows:  
[Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b2f12ae5-0e46-47e1-ac5b-93550d030189)  
(KB956572)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition y Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b743a7fe-7bf4-420d-a72e-39471e5659fa)  
(Moderada)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-010**](http://technet.microsoft.com/security/bulletin/ms09-010)
</td>
<td style="border:1px solid black;">
[**MS09-013**](http://technet.microsoft.com/security/bulletin/ms09-013)
</td>
<td style="border:1px solid black;">
[**MS09-011**](http://technet.microsoft.com/security/bulletin/ms09-011)
</td>
<td style="border:1px solid black;">
[**MS09-014**](http://technet.microsoft.com/security/bulletin/ms09-014)
</td>
<td style="border:1px solid black;">
[**MS09-012**](http://technet.microsoft.com/security/bulletin/ms09-012)
</td>
<td style="border:1px solid black;">
[**MS09-015**](http://technet.microsoft.com/security/bulletin/ms09-015)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
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
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2233a4d2-7c8a-4c89-b020-100d9afb43c8)  
(KB923561)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=42509f5a-d0f9-444a-9445-5eabdb555011)  
(Crítica)
</td>
<td style="border:1px solid black;">
[DirectX 9.0](http://www.microsoft.com/downloads/details.aspx?familyid=c1b4cd76-1dd6-43fa-bb9a-20c428985bfd)\*\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=f73a3669-c17f-4b18-8456-96cb7d52ed86)  
(Importante)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=6a45dbd0-0520-4d9b-b76e-3f5109dd310d)  
(Importante)
</td>
<td style="border:1px solid black;">
Actualización del servicio de transacciones de MSDTC:  
[Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=25adec10-db8c-4cac-bf74-2c784678150a)  
(KB952004)  
(Importante)  
Actualización de aislamiento de servicio de Windows:  
[Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=42aba890-8b76-4c5a-8fb6-609797d19831)  
(KB956572)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 1 y Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=992bb0cd-fbc7-4a7c-9088-f7f9d9a3ead0)  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=323f4211-5add-4e02-bce1-e5a1b489982c)  
(KB923561)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7373ea32-bc2e-49f1-8b9f-4eeda5acc74c)  
(Crítica)
</td>
<td style="border:1px solid black;">
[DirectX 9.0](http://www.microsoft.com/downloads/details.aspx?familyid=f0e1e1db-94a5-451c-ab11-6b431fa065f1)\*\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=03a9d581-2bd5-4151-9826-17b96e16f606)  
(Importante)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=60ccc1d6-ea31-420c-b630-d7878a8dc527)  
(Importante)
</td>
<td style="border:1px solid black;">
Actualización del servicio de transacciones de MSDTC:  
[Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b014c399-f404-4cb2-8f9d-864df382efeb)  
(KB952004)  
(Importante)  
Actualización de aislamiento de servicio de Windows:  
[Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a0609f65-82d9-4d82-9f48-f3266e8de123)  
(KB956572)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition y Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f0a58e8c-7d63-4d7d-ba95-b3787cf408f0)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=e840b9cb-f1f4-482a-aa07-eb6b42b477c4)  
(KB923561)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=05e33cc5-cff6-4c71-be71-285f66a95e01)  
(Crítica)
</td>
<td style="border:1px solid black;">
[DirectX 9.0](http://www.microsoft.com/downloads/details.aspx?familyid=8f36c215-fa8a-40c2-b680-6b1fece03b8d)\*\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=53d13c07-80b0-4f05-b372-a2dac17e6157)  
(Importante)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=0abaa2fb-7c4f-4149-993d-1575888bfc84)  
(Importante)
</td>
<td style="border:1px solid black;">
Actualización del servicio de transacciones de MSDTC:  
[Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=6ada372b-ba17-433e-b022-d2c57b35af8a)  
(KB952004)  
(Importante)  
Actualización de aislamiento de servicio de Windows:  
[Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=fda8837c-e5d2-4489-9b44-4c24a1102e77)  
(KB956572)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP1 para sistemas con Itanium y Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=00c6479d-f81f-445d-b8e4-7b71d77d540a)  
(Moderada)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-010**](http://technet.microsoft.com/security/bulletin/ms09-010)
</td>
<td style="border:1px solid black;">
[**MS09-013**](http://technet.microsoft.com/security/bulletin/ms09-013)
</td>
<td style="border:1px solid black;">
[**MS09-011**](http://technet.microsoft.com/security/bulletin/ms09-011)
</td>
<td style="border:1px solid black;">
[**MS09-014**](http://technet.microsoft.com/security/bulletin/ms09-014)
</td>
<td style="border:1px solid black;">
[**MS09-012**](http://technet.microsoft.com/security/bulletin/ms09-012)
</td>
<td style="border:1px solid black;">
[**MS09-015**](http://technet.microsoft.com/security/bulletin/ms09-015)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
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
Windows Vista y Windows Vista Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista y Windows Vista Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=f071d770-3b6b-4040-9911-d4de8cde4c68)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=d743849d-f3b5-4114-adef-ade2716d55ac)  
(Crítica)
</td>
<td style="border:1px solid black;">
Actualización del servicio de transacciones de MSDTC:  
[Windows Vista y Windows Vista Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=f111b99a-e555-4f29-8d1f-e9ec03d5cf1f)  
(KB952004)  
(Importante)  
Actualización de aislamiento de servicio de Windows:  
[Windows Vista y Windows Vista Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d0ea1598-45cb-4c79-8945-caae98969675)  
(KB956572)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista y Windows Vista Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=2b672d45-f33b-4edc-9f22-2f2c8c726a8b)  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7ceef2d0-f316-48d1-aecc-d74f91cc5e1f)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=d191c8dc-a965-4a6a-b6d8-1470505eb55f)  
(Crítica)
</td>
<td style="border:1px solid black;">
Actualización del servicio de transacciones de MSDTC:  
[Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=fa153bdc-6b48-4df2-9e5e-abacd6da782c)  
(KB952004)  
(Importante)  
Actualización de aislamiento de servicio de Windows:  
[Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=6dd82f4b-bb33-41ec-90a7-9ef91329b240)  
(KB956572)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7576e7d5-5bb1-4a53-b568-1ee0500ce721)  
(Moderada)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-010**](http://technet.microsoft.com/security/bulletin/ms09-010)
</td>
<td style="border:1px solid black;">
[**MS09-013**](http://technet.microsoft.com/security/bulletin/ms09-013)
</td>
<td style="border:1px solid black;">
[**MS09-011**](http://technet.microsoft.com/security/bulletin/ms09-011)
</td>
<td style="border:1px solid black;">
[**MS09-014**](http://technet.microsoft.com/security/bulletin/ms09-014)
</td>
<td style="border:1px solid black;">
[**MS09-012**](http://technet.microsoft.com/security/bulletin/ms09-012)
</td>
<td style="border:1px solid black;">
[**MS09-015**](http://technet.microsoft.com/security/bulletin/ms09-015)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
Ninguna
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
Windows Server 2008 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=4c36548f-c8c9-4318-91e2-9e0501339548)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=e2c6313c-3ba9-4f7c-b259-b4582a390146)\*\*  
(Importante)
</td>
<td style="border:1px solid black;">
Actualización del servicio de transacciones de MSDTC:  
[Windows Server 2008 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=9e3c7b52-65a7-42fb-beb5-1b374934737f)\*  
(KB952004)  
(Importante)  
Actualización de aislamiento de servicio de Windows:  
[Windows Server 2008 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=d58702af-bbf8-4f1b-ae72-ced9ef23d581)\*  
(KB956572)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=6b73cf5e-66fe-4b7d-95fc-91a1c262c1e5)\*  
(Moderada)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=1c3f0997-a8a9-4340-ae0c-2c4d6792c65c)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=ebbade9d-704c-440b-8796-6d64225ac01a)\*\*  
(Importante)
</td>
<td style="border:1px solid black;">
Actualización del servicio de transacciones de MSDTC:  
[Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=eebb4d4d-29d2-4247-8cbb-63a3b17585ec)\*  
(KB952004)  
(Importante)  
Actualización de aislamiento de servicio de Windows:  
[Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=20bf4e9b-909b-4bc3-ae43-322d74a4f1c3)\*  
(KB956572)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=7e60847c-b341-4c38-bc25-2e3cf2d4ae14)\*  
(Moderada)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=0885b3b0-b78e-4980-902d-dff3886bcaac)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=1b04aa6f-b787-4122-bf82-0d150618fe7a)  
(Importante)
</td>
<td style="border:1px solid black;">
Actualización del servicio de transacciones de MSDTC:  
[Windows Server 2008 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=cc383c24-b0f6-47c1-9e89-6a378b09e82f)  
(KB952004)  
(Importante)  
Actualización de aislamiento de servicio de Windows:  
[Windows Server 2008 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=bcc2b18f-67db-4109-a9f4-764f985423ee)  
(KB956572)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=de1c2b4b-af47-4b9a-8363-720e5527573c)  
(Moderada)
</td>
</tr>
</table>
 
**Notas para Windows Server 2008**

**\*Instalación principal de servidor de Windows Server 2008 afectada.** Para ediciones compatibles de Windows Server 2008, esta actualización se aplica con la misma clasificación de gravedad, independientemente de si Windows Server 2008 se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**\*\*Instalación principal de servidor de Windows Server 2008 no afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 si Windows Server 2008 se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**Nota para MS09-010**

Vea también la sección, **Conjuntos de aplicaciones y software de Microsoft Office**, para obtener más archivos de actualización. Este boletín abarca tanto el sistema operativo y los componentes de Windows como los conjuntos de programas y software de Microsoft Office.

**Nota para MS09-011**

\*\*\*La actualización para DirectX 9.0 también se aplica a DirectX 9.0a, DirectX 9.0b y DirectX 9.0c.

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
Conjuntos de programas, sistemas y componentes de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-010**](http://technet.microsoft.com/security/bulletin/ms09-010)
</td>
<td style="border:1px solid black;">
[**MS09-009**](http://technet.microsoft.com/security/bulletin/ms09-009)
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
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2000 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Office Word 2000 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=95876927-e612-414c-bdec-3632a3100415)  
(KB921606)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2000 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=3dc8b670-25a5-4f46-b7de-12bc693b628a)  
(KB959964)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Office Word 2002 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=e1db55c6-78fb-498d-89a5-9ad54d971546)  
(KB933399)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2002 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=9a52bf4b-05f6-4b73-94b9-28ed7e20f86c)  
(KB959988)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=d9dbfa63-c0cb-4c84-9b8a-6e52568045b0)  
(KB959995)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
2007 Microsoft Office System Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2007 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=50d8630b-1365-4007-81a0-18c0d6d4b86e)\*  
(KB959997)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Office para Mac
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-010**](http://technet.microsoft.com/security/bulletin/ms09-010)
</td>
<td style="border:1px solid black;">
[**MS09-009**](http://technet.microsoft.com/security/bulletin/ms09-009)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2004 para Mac
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office 2004 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=52271140-89be-4b9c-baa2-cea09097d703)  
(KB968695)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2008 para Mac
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office 2008 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=f6e407eb-11a5-433f-8006-4b822953ca98)  
(KB968694)  
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
[**MS09-010**](http://technet.microsoft.com/security/bulletin/ms09-010)
</td>
<td style="border:1px solid black;">
[**MS09-009**](http://technet.microsoft.com/security/bulletin/ms09-009)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Excel Viewer
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel Viewer 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=c72e6087-b48f-4d2d-8366-01d9f5ff6b6c)  
(KB959993)  
(Importante)  
[Microsoft Office Excel Viewer](http://www.microsoft.com/downloads/details.aspx?familyid=58b3929c-5373-47a4-aa97-66d179758792)  
(KB960000)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=05f7c517-e551-4dcd-b24a-5d548f2d09cf)  
(KB960003)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Paquete de convertidores de Microsoft Office
</td>
<td style="border:1px solid black;">
[Paquete de convertidores de Microsoft Office](http://www.microsoft.com/downloads/details.aspx?familyid=d763fae3-b2af-47f9-a554-ec786766b3c3)  
(KB960476)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
**Nota para MS09-010**

Vea también la sección **Sistema operativo y componentes de Windows**, para obtener más archivos de actualización. Este boletín abarca tanto el sistema operativo y los componentes de Windows como el software de servidor de Microsoft.

**Nota para MS09-009**

\*Para Microsoft Office Excel 2007 Service Pack 1, los clientes también deben instalar la actualización de seguridad para Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 1 con el fin de protegerse de las vulnerabilidades descritas en este boletín.

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
Microsoft Forefront
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-016**](http://technet.microsoft.com/security/bulletin/ms09-016)
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
Microsoft Forefront Threat Management Gateway
</td>
<td style="border:1px solid black;">
[Microsoft Forefront Threat Management Gateway, Medium Business Edition](http://www.microsoft.com/downloads/details.aspx?familyid=6abf9fb4-42d0-4c67-935f-8dc67850148b)\*  
(KB968075)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Internet Security and Acceleration Server
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-016**](http://technet.microsoft.com/security/bulletin/ms09-016)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Internet Security and Acceleration Server 2004
</td>
<td style="border:1px solid black;">
[Microsoft Internet Security and Acceleration Server 2004 Standard Edition Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=adf623fa-2d74-4f2a-9835-4b8debdb0e1b)\*\*  
(KB960995)  
(Importante)  
[Microsoft Internet Security and Acceleration Server 2004 Enterprise Edition Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=d1d55ab6-3de5-4811-9693-8d43f49f5fe8)  
(KB960995)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Internet Security and Acceleration Server 2006
</td>
<td style="border:1px solid black;">
[Microsoft Internet Security and Acceleration Server 2006](http://www.microsoft.com/downloads/details.aspx?familyid=eda30bcc-0582-4f60-a4c5-ea5000b7c770)  
(KB968078)  
(Importante)  
[Actualización de compatibilidad de Microsoft Internet Security and Acceleration Server 2006](http://www.microsoft.com/downloads/details.aspx?familyid=eda30bcc-0582-4f60-a4c5-ea5000b7c770)  
(KB968078)  
(Importante)  
[Microsoft Internet Security and Acceleration Server 2006 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=eda30bcc-0582-4f60-a4c5-ea5000b7c770)  
(KB968078)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS09-016**

\*Microsoft Forefront Threat Management Gateway, Medium Business Edition, se proporciona como un producto independiente y como un componente de Windows Essential Business Server 2008.

\*\*Microsoft ISA Server 2004 Standard Edition se proporciona como un producto independiente. Microsoft ISA Server 2004 Standard Edition también se proporciona como un componente de Windows Small Business Server 2003 Enterprise Edition Service Pack 1 y Windows Small Business Server 2003 R2 Enterprise Edition.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://go.microsoft.com/fwlink/?linkid=69903). [TechNet Security Center](http://go.microsoft.com/fwlink/?linkid=21171) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://www.microsoft.com/spain/athome/security/default.mspx), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747), [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130) y [Office Update](http://go.microsoft.com/fwlink/?linkid=21135). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://www.microsoft.com/downloads/search.aspx?displaylang=es). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS07-036"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Consejos para la detección y la implementación**

Microsoft ofrece recomendaciones para la detección y la implementación de las actualizaciones de seguridad de este mes. Esta orientación también ayudará a los profesionales de TI a comprender el funcionamiento de distintas herramientas que sirven de ayuda en la implementación de la actualización de seguridad, como Windows Update, Microsoft Update, Office Update, Microsoft Baseline Security Analyzer (MBSA), Office Detection Tool, Microsoft Systems Management Server (SMS) y Extended Security Update Inventory Tool (ESUIT). Para obtener más información, consulte el [artículo 910723 de Microsoft Knowledge Base](http://support.microsoft.com/kb/910723).

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://go.microsoft.com/fwlink/?linkid=21134).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar con rapidez y fiabilidad las actualizaciones críticas y de seguridad más recientes en sistemas operativos Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://www.microsoft.com/spain/technet/seguridad/herramientas/wsus.mspx).

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. La siguiente versión de SMS, System Center Configuration Manager 2007, ya está disponible; consulte también [System Center Configuration Manager 2007](http://technet.microsoft.com/en-us/library/bb735860.aspx). Para obtener más información acerca de cómo pueden utilizar los administradores SMS 2003 para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar [Software Updates Services Feature Pack](http://go.microsoft.com/fwlink/?linkid=33340) como ayuda para la implementación de actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://www.microsoft.com/spain/smserver/default.mspx).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer y Microsoft Office Detection Tool como ayuda para proporcionar un amplio soporte técnico para la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=33387) y en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet2.microsoft.com/windowsvista/en/library/4279e239-37a4-44aa-aec5-4e70fe39f9de1033.mspx?mfr=true) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones 5.0](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Microsoft Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Artículo 894199 de Microsoft Knowledge Base](http://support.microsoft.com/kb/894199): Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones nuevas, revisadas y publicadas para productos de Microsoft distintos de Microsoft Windows](http://technet.microsoft.com/en-us/wsus/dd573344.aspx).

#### Microsoft Active Protections Program (MAPP)

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumeradas en [Asociados de Microsoft Active Protections Program (MAPP)](http://www.microsoft.com/security/msrc/mapp/partners.mspx).

#### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de actualizaciones](http://www.microsoft.com/spain/technet/seguridad/areas/actualiza/default.mspx) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://www.microsoft.com/downloads/search.aspx?displaylang=es) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747).
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](http://support.microsoft.com/kb/913086).

**Comunidad de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [IT Pro Security Community](http://go.microsoft.com/fwlink/?linkid=21164) (en inglés).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

-   Haifei Li, de [FortiGuard Global Security Research Team](http://www.fortiguardcenter.com/) de Fortinet, por informar de un problema descrito en MS09-009
-   Sean Larsson y Jun Mao, de [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS09-010
-   Un investigador en colaboración con [FortiGuard Global Security Research Team](http://www.fortiguardcenter.com/) de Fortinet, por informar de un problema descrito en MS09-010
-   Un investigador en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS09-010
-   Piotr Bania, de [Kryptos Logic](http://www.kryptoslogic.com/), por informar de un problema descrito en MS09-011
-   Cesar Cerrudo, de [Argeniss](http://www.argeniss.com/), por informar de varios problemas descritos en MS09-012
-   Greg MacManus, de [iSIGHT Partners Labs](http://www.isightpartners.com/), por informar de un problema descrito en MS09-013
-   Wan-Teh Chang y Cem Paya, de [Google Inc.](http://www.google.com/), por informar de un problema descrito en MS09-013
-   [Aviv Raff](http://aviv.raffon.net/), por informar de un problema descrito en MS09-014
-   Michal Zalewski, de [Google Inc.](http://www.google.com/), por informar de un problema descrito en MS09-014
-   Ivan Fratric, de [iSIGHT Partners Labs](http://www.isightpartners.com/), por informar de un problema descrito en MS09-014
-   Skylined, de [Google Inc.](http://www.google.com/), por informar de un problema descrito en MS09-014
-   ADLab, de [VenusTech](http://www.venustech.com.cn/), por informar de un problema descrito en MS09-014
-   [Aviv Raff](http://aviv.raffon.net/), por informar de un problema descrito en MS09-015
-   El director de informática del estado de Nueva York / Departamento de tecnología, por informar de un problema descrito en MS09-016

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Puede solicitar soporte técnico en los [Servicios de soporte técnico de Microsoft](http://support.microsoft.com/default.aspx?scid=fh;es-es;incidentsubmit) o a través del teléfono 902 197 198.
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (14 de abril de 2009): Publicación del resumen del boletín.
-   V1.1 (16 de abril de 2009): Se ha actualizado el índice de explotabilidad: se han quitado las notas de clave para CVE-2009-0089 y se han cambiado las notas de clave para CVE-2008-2540 en MS09-014 y MS09-015.

*Built at 2014-04-18T01:50:00Z-07:00*
