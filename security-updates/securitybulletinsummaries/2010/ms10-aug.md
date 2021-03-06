---
TOCTitle: 'MS10-AUG'
Title: Resumen del boletín de seguridad de Microsoft de agosto 2010
ms:assetid: 'ms10-aug'
ms:contentKeyID: 61225409
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms10-aug(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de agosto 2010
============================================================

Publicado: lunes, 2 de agosto de 2010 | Actualizado: miércoles, 1 de septiembre de 2010

**Versión:** 2.1

Este resumen del boletín enumera los boletines de seguridad publicados para agosto de 2010.

Con la publicación de los boletines de agosto de 2010, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 5 de agosto de 2010. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar una conferencia en línea para atender las consultas de los clientes sobre estos boletines el 11 de agosto de 2010, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). Inscríbase ahora al [webcast del boletín de seguridad de agosto](https://msevents.microsoft.com/cui/webcasteventdetails.aspx?eventid=1032454431&eventcategory=4&culture=en-us&countrycode=us). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

Para el boletín de seguridad fuera de ciclo, [MS10-046](http://technet.microsoft.com/security/bulletin/ms10-046), anunciado originalmente en la versión 1.0 de este resumen del boletín, Microsoft publicó la notificación de avance de boletines correspondiente el 30 de julio de 2010 y celebró una conferencia en línea el 2 de agosto de 2010. La [conferencia en línea del 2 de agosto de 2010](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032456779&culture=en-us) está disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary).

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-046">MS10-046</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el shell de Windows podría permitir la ejecución remota de código (2286198)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad que se ha divulgado públicamente en el shell de Windows. La vulnerabilidad podría permitir la ejecución remota de código si se muestra el icono de un acceso directo especialmente diseñado. Un intruso que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario local. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-049">MS10-049</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en SChannel podrían permitir la ejecución remota de código (980436)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y una vulnerabilidad de la que se ha informado de forma privada en el paquete de seguridad de canal seguro (SChannel) en Windows. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un usuario visita un sitio web especialmente diseñado para aprovechar estas vulnerabilidades a través de un explorador web de Internet. Sin embargo, el atacante no podría en ningún caso obligar a los usuarios a visitar estos sitios web. Por lo tanto, tendría que atraerlos al sitio web; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger que lleve a los usuarios al sitio web del atacante.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-051">MS10-051</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft XML Core Services podría permitir la ejecución remota de código (2079403)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft XML Core Services. La vulnerabilidad podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. El atacante no podría obligar a los usuarios a visitar estos sitios web. Por lo tanto, tendría que atraerlos al sitio web; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger que lleve a los usuarios al sitio web del atacante.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-052">MS10-052</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en los códecs MPEG Layer-3 de Microsoft podría permitir la ejecución remota de código (2115168)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en los códecs de audio MPEG Layer-3 de Microsoft. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo multimedia especialmente diseñado o recibe contenido por secuencias especialmente diseñado de un sitio web o de cualquier aplicación que proporcione contenido web. Un intruso que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario local. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-053">MS10-053</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (2183461)</strong><br />
<br />
Esta actualización de seguridad resuelve seis vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. La más grave de las vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-054">MS10-054</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en el servidor SMB podrían permitir la ejecución remota de código (982214)</strong><br />
<br />
Esta actualización de seguridad resuelve varias vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un atacante crea un paquete SMB especialmente diseñado y lo envía a un sistema afectado. Los procedimientos recomendados para firewall y las configuraciones de firewall predeterminadas estándar pueden proteger a las redes de los ataques procedentes del exterior del perímetro de la empresa que intentan aprovechar estas vulnerabilidades.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-055">MS10-055</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el códec Cinepak podría permitir la ejecución remota de código (982665)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en el códec Cinepak. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo multimedia especialmente diseñado o recibe contenido por secuencias especialmente diseñado de un sitio web o de cualquier aplicación que proporcione contenido web. Un intruso que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario local. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-056">MS10-056</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Office Word podrían permitir la ejecución remota de código (2269638)</strong><br />
<br />
Esta actualización de seguridad resuelve cuatro vulnerabilidades de las que se ha informado de forma privada en Microsoft Office. Las vulnerabilidades más graves podrían permitir la ejecución remota de código si un usuario abre un mensaje de correo electrónico RTF especialmente diseñado u obtiene una vista previa de él. Un intruso que aprovechara cualquiera de estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario local. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-060">MS10-060</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft .NET Common Language Runtime y en Microsoft Silverlight podrían permitir la ejecución remota de código (2265906)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft .NET Framework y Microsoft Silverlight. Estas vulnerabilidades podrían permitir la ejecución remota de código en un sistema cliente si un usuario visualiza una página web especialmente diseñada mediante un explorador web que pueda ejecutar aplicaciones XAML del explorador (XBAP) o aplicaciones Silverlight, o si un atacante consigue convencer a un usuario para que ejecute una aplicación Microsoft .NET especialmente diseñada. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. Las vulnerabilidades también podrían permitir la ejecución remota de código en un sistema de servidor que ejecute IIS si dicho servidor permite el procesamiento de páginas ASP.NET y un atacante consigue cargar una página ASP.NET especialmente diseñada en el servidor y la ejecuta, como puede ser el caso de un escenario de hospedaje web.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, Microsoft .NET Framework, Microsoft Silverlight</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-047">MS10-047</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades del kernel de Windows podrían permitir la elevación de privilegios (981852)</strong><br />
<br />
Esta actualización de seguridad resuelve varias vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. La más grave de estas vulnerabilidades podría permitir la elevación de privilegios si un atacante ha iniciado sesión localmente y ha ejecutado una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de aprovechar estas vulnerabilidades. Los usuarios anónimos o los usuarios remotos no pueden aprovechar estas vulnerabilidades.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-048">MS10-048</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en los controladores en modo kernel de Windows podrían permitir la elevación de privilegios (2160329)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y cuatro vulnerabilidades de las que se ha informado de forma privada en los controladores en modo kernel de Windows. La más grave de estas vulnerabilidades podría permitir la elevación de privilegios si un atacante inicia sesión en un sistema afectado y ejecuta una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local. Los usuarios anónimos o los usuarios remotos no pueden aprovechar esta vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-050">MS10-050</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Windows Movie Maker podría permitir la ejecución remota de código (981997)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad en Windows Movie Maker de la que se ha informado de forma privada. La vulnerabilidad podría permitir la ejecución remota de código si un atacante envía un archivo de proyecto de Movie Maker especialmente diseñado y convence al usuario de que lo abra. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-057">MS10-057</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Office Excel podría permitir la ejecución remota de código (2269707)</strong> <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Office. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo de Excel especialmente diseñado. Un intruso que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario que ha iniciado sesión. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-058">MS10-058</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en TCP/IP podrían permitir la elevación de privilegios (978886)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. La más grave de estas vulnerabilidades podría permitir la elevación de privilegios debido a un error en el procesamiento de un búfer de entrada específico. Un atacante que pueda iniciar sesión en el sistema de destino podría aprovechar esta vulnerabilidad y ejecutar código arbitrario con privilegios de nivel del sistema. De esta forma, el atacante podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos de usuario.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms10-059">MS10-059</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en la característica de seguimiento de los servicios podrían permitir una elevación de privilegios (982799)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y una vulnerabilidad de la que se ha informado de forma privada en la característica de seguimiento para servicios. Las vulnerabilidades podrían permitir la elevación de privilegios si un atacante ejecuta una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local. Los usuarios anónimos o los usuarios remotos no pueden aprovechar esta vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de nivel de evaluación de explotabilidad decreciente y, a continuación, por identificador de CVE. Sólo se incluyen las vulnerabilidades que tiene una clasificación de gravedad de crítica o importante en los boletines.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de que se publique código funcional que aproveche la vulnerabilidad en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Debe revisar cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/es-es/security/cc998259.aspx).
  
| Identificador del boletín                                           | Título de vulnerabilidad                                                                                      | Identificador CVE                                                                | Evaluación de índice de explotabilidad                                                                                                  | Notas clave                                                                                                                                                                              |  
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| [MS10-060](http://technet.microsoft.com/security/bulletin/ms10-060) | Vulnerabilidad de daños en la memoria relacionada con Microsoft Silverlight                                   | [CVE-2010-0019](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-0019) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                |  
| [MS10-052](http://technet.microsoft.com/security/bulletin/ms10-052) | Vulnerabilidad de desbordamiento del búfer del descodificador de audio MPEG Layer-3                           | [CVE-2010-1882](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1882) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                |  
| [MS10-047](http://technet.microsoft.com/security/bulletin/ms10-047) | Vulnerabilidad de inicialización de datos en el kernel de Windows                                             | [CVE-2010-1888](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1888) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                |  
| [MS10-058](http://technet.microsoft.com/security/bulletin/ms10-058) | Vulnerabilidad de desbordamiento de enteros en la red de Windows                                              | [CVE-2010-1893](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1893) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                |  
| [MS10-048](http://technet.microsoft.com/security/bulletin/ms10-048) | Vulnerabilidad de control de excepciones en Win32k                                                            | [CVE-2010-1894](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1894) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | **Esa vulnerabilidad ya se ha divulgado.**                                                                                                                                               |  
| [MS10-048](http://technet.microsoft.com/security/bulletin/ms10-048) | Vulnerabilidad de desbordamiento de grupo en Win32k                                                           | [CVE-2010-1895](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1895) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                |  
| [MS10-048](http://technet.microsoft.com/security/bulletin/ms10-048) | Vulnerabilidad de validación de entrada de usuario en Win32k                                                  | [CVE-2010-1896](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1896) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                |  
| [MS10-048](http://technet.microsoft.com/security/bulletin/ms10-048) | Vulnerabilidad de creación de ventanas en Win32k                                                              | [CVE-2010-1897](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1897) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                |  
| [MS10-060](http://technet.microsoft.com/security/bulletin/ms10-060) | Vulnerabilidad de delegación de métodos virtuales en Microsoft Silverlight y Microsoft .NET Framework CLR     | [CVE-2010-1898](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1898) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                |  
| [MS10-056](http://technet.microsoft.com/security/bulletin/ms10-056) | Vulnerabilidad de análisis de registros en Word                                                               | [CVE-2010-1900](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1900) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                |  
| [MS10-056](http://technet.microsoft.com/security/bulletin/ms10-056) | Vulnerabilidad de daños en la memoria relacionada con el motor de análisis de RTF en Word                     | [CVE-2010-1901](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1901) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                |  
| [MS10-055](http://technet.microsoft.com/security/bulletin/ms10-055) | Vulnerabilidad en la descompresión del códec Cinepak                                                          | [CVE-2010-2553](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2553) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                |  
| [MS10-059](http://technet.microsoft.com/security/bulletin/ms10-059) | Vulnerabilidad de daños en la memoria relacionada con el seguimiento                                          | [CVE-2010-2555](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2555) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                |  
| [MS10-053](http://technet.microsoft.com/security/bulletin/ms10-053) | Vulnerabilidad de daños en la memoria sin inicializar                                                         | [CVE-2010-2557](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2557) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | Esta vulnerabilidad tiene mayor probabilidad de aprovecharse en Internet Explorer 6 debido a la ausencia de la prevención de ejecución de datos como factor atenuante.                   |  
| [MS10-053](http://technet.microsoft.com/security/bulletin/ms10-053) | Vulnerabilidad de daños en la memoria relacionada con el diseño HTML                                          | [CVE-2010-2560](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2560) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                |  
| [MS10-057](http://technet.microsoft.com/security/bulletin/ms10-057) | Vulnerabilidad de daños en la memoria relacionada con Excel                                                   | [CVE-2010-2562](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2562) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                |  
| [MS10-050](http://technet.microsoft.com/security/bulletin/ms10-050) | Vulnerabilidad de daños en la memoria relacionada con Movie Maker                                             | [CVE-2010-2564](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2564) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | (Ninguna)                                                                                                                                                                                |  
| [MS10-046](http://technet.microsoft.com/security/bulletin/ms10-046) | Vulnerabilidad en la carga de los iconos de los accesos directos                                              | [CVE-2010-2568](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2568) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad    | **Esta vulnerabilidad se está aprovechando actualmente en el ecosistema de Internet.**                                                                                                   |  
| [MS10-047](http://technet.microsoft.com/security/bulletin/ms10-047) | Vulnerabilidad de doble liberación en el kernel de Windows                                                    | [CVE-2010-1889](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1889) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                                |  
| [MS10-056](http://technet.microsoft.com/security/bulletin/ms10-056) | Vulnerabilidad de desbordamiento del búfer de análisis de RTF en Word                                         | [CVE-2010-1902](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1902) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | Existe menos probabilidad de que se aproveche en Windows Vista y Windows 7 debido a los mecanismos adicionales de atenuación en el montón.                                               |  
| [MS10-056](http://technet.microsoft.com/security/bulletin/ms10-056) | Vulnerabilidad de daños en la memoria relacionada con los objetos HTML vinculados en Word                     | [CVE-2010-1903](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1903) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                                |  
| [MS10-054](http://technet.microsoft.com/security/bulletin/ms10-054) | Vulnerabilidad de desbordamiento de grupo en SMB                                                              | [CVE-2010-2550](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2550) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | Es muy probable de que el aprovechamiento de la vulnerabilidad produzca una denegación de servicio en vez de una ejecución de código.                                                    |  
| [MS10-053](http://technet.microsoft.com/security/bulletin/ms10-053) | Vulnerabilidad de daños en la memoria sin inicializar                                                         | [CVE-2010-2556](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2556) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                                |  
| [MS10-053](http://technet.microsoft.com/security/bulletin/ms10-053) | Vulnerabilidad de daños en la memoria relacionada con la condición de ejecución                               | [CVE-2010-2558](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2558) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                                |  
| [MS10-053](http://technet.microsoft.com/security/bulletin/ms10-053) | Vulnerabilidad de daños en la memoria sin inicializar                                                         | [CVE-2010-2559](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2559) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                                |  
| [MS10-051](http://technet.microsoft.com/security/bulletin/ms10-051) | Vulnerabilidad de daños en la memoria relacionada con el tratamiento de las respuestas de Msxml2.XMLHTTP.3.0  | [CVE-2010-2561](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2561) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | (Ninguna)                                                                                                                                                                                |  
| [MS10-049](http://technet.microsoft.com/security/bulletin/ms10-049) | Vulnerabilidad de ejecución remota de código en solicitudes de certificado con formato incorrecto en SChannel | [CVE-2010-2566](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2566) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad        | Es probable que el aprovechamiento de la vulnerabilidad tenga como resultado una denegación de servicio. La ejecución remota de código es improbable.                                    |  
| [MS10-049](http://technet.microsoft.com/security/bulletin/ms10-049) | Vulnerabilidad de renegociación de TLS/SSL                                                                    | [CVE-2009-3555](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-3555) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | Se trata de una vulnerabilidad de suplantación. Se ha descrito en el [documento informativo sobre seguridad de Microsoft 977377](http://technet.microsoft.com/security/advisory/977377). |  
| [MS10-053](http://technet.microsoft.com/security/bulletin/ms10-053) | Vulnerabilidad entre dominios por controlador de eventos                                                      | [CVE-2010-1258](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1258) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | Esta vulnerabilidad afecta a la divulgación de información.                                                                                                                              |  
| [MS10-058](http://technet.microsoft.com/security/bulletin/ms10-058) | Vulnerabilidad de daños en la memoria relacionada con IPv6                                                    | [CVE-2010-1892](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-1892) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | Se trata de una vulnerabilidad de denegación de servicio.                                                                                                                                |  
| [MS10-054](http://technet.microsoft.com/security/bulletin/ms10-054) | Vulnerabilidad de validación de variables en SMB                                                              | [CVE-2010-2551](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2551) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | Se trata de una vulnerabilidad de denegación de servicio.                                                                                                                                |  
| [MS10-054](http://technet.microsoft.com/security/bulletin/ms10-054) | Vulnerabilidad de agotamiento de la pila en SMB                                                               | [CVE-2010-2552](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2010-2552) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Improbabilidad de código funcional que aproveche la vulnerabilidad | Se trata de una vulnerabilidad de denegación de servicio.                                                                                                                                |
  
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
<th colspan="14" style="border:1px solid black;">
Windows XP  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-046**](http://technet.microsoft.com/security/bulletin/ms10-046)
</td>
<td style="border:1px solid black;">
[**MS10-049**](http://technet.microsoft.com/security/bulletin/ms10-049)
</td>
<td style="border:1px solid black;">
[**MS10-051**](http://technet.microsoft.com/security/bulletin/ms10-051)
</td>
<td style="border:1px solid black;">
[**MS10-052**](http://technet.microsoft.com/security/bulletin/ms10-052)
</td>
<td style="border:1px solid black;">
[**MS10-053**](http://technet.microsoft.com/security/bulletin/ms10-053)
</td>
<td style="border:1px solid black;">
[**MS10-054**](http://technet.microsoft.com/security/bulletin/ms10-054)
</td>
<td style="border:1px solid black;">
[**MS10-055**](http://technet.microsoft.com/security/bulletin/ms10-055)
</td>
<td style="border:1px solid black;">
[**MS10-060**](http://technet.microsoft.com/security/bulletin/ms10-060)
</td>
<td style="border:1px solid black;">
[**MS10-047**](http://technet.microsoft.com/security/bulletin/ms10-047)
</td>
<td style="border:1px solid black;">
[**MS10-048**](http://technet.microsoft.com/security/bulletin/ms10-048)
</td>
<td style="border:1px solid black;">
[**MS10-050**](http://technet.microsoft.com/security/bulletin/ms10-050)
</td>
<td style="border:1px solid black;">
[**MS10-058**](http://technet.microsoft.com/security/bulletin/ms10-058)
</td>
<td style="border:1px solid black;">
[**MS10-059**](http://technet.microsoft.com/security/bulletin/ms10-059)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
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
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=12361875-b453-45e8-852b-90f2727894fd)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=ff00381c-e74b-48e5-9dd9-34dbedd906a2)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=dbdbbe5e-2ef9-4704-80c4-27ef28fd95ef)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=08159149-17de-4640-8818-cb7bd4811531)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=bc949915-4e16-4897-a295-2f99102548ab)  
(Crítica)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=4b489f8c-ada0-4051-8284-0a941c04d2ed)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=1662780f-370a-425b-9917-c601eb54a375)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=6e5e16f8-c140-4a1d-b898-8417a6bfd4d8)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=5ddb5e34-f97a-47c6-96c8-ba2ed06ccb77)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=648cfca5-19eb-4658-a6ad-fe546c4c44b9)  
(KB983582)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1e53f250-2d4b-4f61-86ee-9f9f3a9c0b48)  
(KB983583)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=e3574047-5ce5-4461-94aa-4eb3258d5e71)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=deeac521-d3a2-4019-8176-c9228e733cf4)  
(Importante)
</td>
<td style="border:1px solid black;">
[Movie Maker 2.1](http://www.microsoft.com/downloads/details.aspx?familyid=b211664b-434d-4626-816f-c77510cfd44d)<sup>[1]</sup>
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
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3b44bd67-48e2-497f-9165-42a702e2cc0d)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=eaffa70c-6f2b-4e66-b1bc-64bdbbbcd34f)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=4d4e8eeb-a0b2-41c6-9ee4-3f4beb44195e)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b7f28d7a-6b27-4059-865b-5fd55edb6299)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=96b7a562-af16-4f0d-840c-838fb12e7419)  
(Crítica)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=5296fb82-c446-4681-a9a0-0f80a2e248be)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=f8ae3978-bad6-4201-8357-2d212ab703ef)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=fd6cc359-e72e-46ec-a08b-763934e3e115)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/my%20documents/release/5cff5d6e-11a5-40ed-92ac-e12d287919e6)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=648cfca5-19eb-4658-a6ad-fe546c4c44b9)  
(KB983582)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1e53f250-2d4b-4f61-86ee-9f9f3a9c0b48)  
(KB983583)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d6c5455e-bc31-4842-aef4-ebff92324323)  
(Importante)
</td>
<td style="border:1px solid black;">
[Movie Maker 2.1](http://www.microsoft.com/downloads/details.aspx?familyid=decb1fe6-adc8-44f7-89c5-f25767f0cefe)<sup>[1]</sup>
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
<th colspan="14" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-046**](http://technet.microsoft.com/security/bulletin/ms10-046)
</td>
<td style="border:1px solid black;">
[**MS10-049**](http://technet.microsoft.com/security/bulletin/ms10-049)
</td>
<td style="border:1px solid black;">
[**MS10-051**](http://technet.microsoft.com/security/bulletin/ms10-051)
</td>
<td style="border:1px solid black;">
[**MS10-052**](http://technet.microsoft.com/security/bulletin/ms10-052)
</td>
<td style="border:1px solid black;">
[**MS10-053**](http://technet.microsoft.com/security/bulletin/ms10-053)
</td>
<td style="border:1px solid black;">
[**MS10-054**](http://technet.microsoft.com/security/bulletin/ms10-054)
</td>
<td style="border:1px solid black;">
[**MS10-055**](http://technet.microsoft.com/security/bulletin/ms10-055)
</td>
<td style="border:1px solid black;">
[**MS10-060**](http://technet.microsoft.com/security/bulletin/ms10-060)
</td>
<td style="border:1px solid black;">
[**MS10-047**](http://technet.microsoft.com/security/bulletin/ms10-047)
</td>
<td style="border:1px solid black;">
[**MS10-048**](http://technet.microsoft.com/security/bulletin/ms10-048)
</td>
<td style="border:1px solid black;">
[**MS10-050**](http://technet.microsoft.com/security/bulletin/ms10-050)
</td>
<td style="border:1px solid black;">
[**MS10-058**](http://technet.microsoft.com/security/bulletin/ms10-058)
</td>
<td style="border:1px solid black;">
[**MS10-059**](http://technet.microsoft.com/security/bulletin/ms10-059)
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
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
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
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=32fe91ef-5a8d-4095-90ee-2ca216696b09)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f76d68df-97e5-489c-a5f6-0c378c1f62ae)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=31ce233e-4d2d-404b-84a8-683319ba8ef7)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9c2110ec-7e6c-4e73-9785-0a8196095ea0)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=b0370e1e-dedf-4fe8-a06c-0e0f0a674205)  
(Crítica)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=8753ae27-60a4-475a-b8bc-6a7764480295)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=772e765d-0502-4b0b-bde8-d4f62b96db64)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=230e8559-e6df-49d5-acb5-b0cd4bde0bf4)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=648cfca5-19eb-4658-a6ad-fe546c4c44b9)  
(KB983582)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1e53f250-2d4b-4f61-86ee-9f9f3a9c0b48)  
(KB983583)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=59395f00-90f4-4b68-8dd3-03ff611c1bc8)  
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
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=923de214-c4fa-41e6-8307-2c5a37f13e8e)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4543bcf0-3505-407b-a5a9-6250ece6fbac)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=4d784b57-8564-4e7e-8f61-f897398e7ea5)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=fdfad4ca-37c4-4ac5-bebc-a5ad61299503)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=d92f5e69-43cf-4615-aa3b-41f9f40bb57b)  
(Crítica)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=fd3e9d06-1f8b-4ef7-84f6-61e85a1767b8)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=863edf45-0d3b-4408-a47c-258dc4a4fd94)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=03804f59-748e-4832-98e4-2d88564bd10a)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=648cfca5-19eb-4658-a6ad-fe546c4c44b9)  
(KB983582)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1e53f250-2d4b-4f61-86ee-9f9f3a9c0b48)  
(KB983583)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9ef1c600-bb93-4800-81b8-8c64b369c194)  
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
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=63aa5f8a-fe47-4892-b905-b54e4f3b6580)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=9ef992c3-96e9-4533-b844-07424a6054b3)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=d87ac8b3-41fb-4cdd-b305-181a0024d85c)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=782e2963-4a52-4a1d-b99a-34ba841038a7)  
(Crítica)  

[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=5e730064-8270-4d63-b497-c5ebeddea1fc)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=e4f4f8b3-7a39-4d77-a46b-02c86ad159c3)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=648cfca5-19eb-4658-a6ad-fe546c4c44b9)  
(KB983582)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=1e53f250-2d4b-4f61-86ee-9f9f3a9c0b48)  
(KB983583)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=f96b8154-9976-41b0-b9d7-d79887fe9364)  
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
<th colspan="14" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-046**](http://technet.microsoft.com/security/bulletin/ms10-046)
</td>
<td style="border:1px solid black;">
[**MS10-049**](http://technet.microsoft.com/security/bulletin/ms10-049)
</td>
<td style="border:1px solid black;">
[**MS10-051**](http://technet.microsoft.com/security/bulletin/ms10-051)
</td>
<td style="border:1px solid black;">
[**MS10-052**](http://technet.microsoft.com/security/bulletin/ms10-052)
</td>
<td style="border:1px solid black;">
[**MS10-053**](http://technet.microsoft.com/security/bulletin/ms10-053)
</td>
<td style="border:1px solid black;">
[**MS10-054**](http://technet.microsoft.com/security/bulletin/ms10-054)
</td>
<td style="border:1px solid black;">
[**MS10-055**](http://technet.microsoft.com/security/bulletin/ms10-055)
</td>
<td style="border:1px solid black;">
[**MS10-060**](http://technet.microsoft.com/security/bulletin/ms10-060)
</td>
<td style="border:1px solid black;">
[**MS10-047**](http://technet.microsoft.com/security/bulletin/ms10-047)
</td>
<td style="border:1px solid black;">
[**MS10-048**](http://technet.microsoft.com/security/bulletin/ms10-048)
</td>
<td style="border:1px solid black;">
[**MS10-050**](http://technet.microsoft.com/security/bulletin/ms10-050)
</td>
<td style="border:1px solid black;">
[**MS10-058**](http://technet.microsoft.com/security/bulletin/ms10-058)
</td>
<td style="border:1px solid black;">
[**MS10-059**](http://technet.microsoft.com/security/bulletin/ms10-059)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista Service Pack 1 y Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=52748886-6280-4247-8cbd-f64db229ee66)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=aca69406-f795-4398-968f-959fe3a74e89)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=bbfaadf8-ab38-456c-956a-ea18c64236c9)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=535c563e-cdac-4e3d-96b0-9947ea22deca)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=2062566b-8b81-43c2-875d-9c06d4e3fa82)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9087a3aa-aa55-41f6-8c4c-f322e4aa8681)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=60c81415-b61e-44a4-8dd9-cedec99eb70f)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 1 solamente:  
[Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=616c39f7-137a-40b9-b691-bc33c0aef7e1)  
(KB983587)  
(Crítica)  

Windows Vista Service Pack 1 solamente:  
[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=155bbb5c-247e-4bed-a287-527d978b7967)  
(KB983588)  
(Crítica)  

Windows Vista Service Pack 2 únicamente:  
[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7712e8ad-dea4-4a43-8a7b-dc154510c104)  
(KB983589)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4486f97c-4cf8-4236-bfc3-b50e72e2a5c1)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c9345207-7242-4b71-bf80-b52031e08f8c)  
(Importante)
</td>
<td style="border:1px solid black;">
[Movie Maker 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=8aded9dd-08d6-4b19-955f-0d8414868cf9)<sup>[1]</sup>
(Importante)  

[Movie Maker 2.6](http://www.microsoft.com/downloads/details.aspx?familyid=a1d8ed0d-a3b5-416a-ab8b-77501da62132)<sup>[2]</sup>
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4684c4df-0a5c-4dba-82e5-059378737118)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=dfb31aa2-7457-4581-9e28-7984a360edf4)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=37648e95-05c2-4802-9a0f-660200baa229)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e2835ed1-5ca6-4347-8ff1-e694b1ac49ff)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=577131cd-1229-4746-89d7-84d75f29e1f0)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=cd1185e3-ca22-4197-a53b-e7a2806ac352)  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=65b04e29-8e39-46de-94e8-b653969b1ffd)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=10c9d5f1-53ed-459b-a663-e69bdb845a6b)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=469b732d-ca62-4a48-bb55-99f2ae4ddcf5)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 1 solamente:  
[Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=616c39f7-137a-40b9-b691-bc33c0aef7e1)  
(KB983587)  
(Crítica)  

Windows Vista x64 Edition Service Pack 1 solamente:  
[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=155bbb5c-247e-4bed-a287-527d978b7967)  
(KB983588)  
(Crítica)  

Windows Vista x64 Edition Service Pack 2 únicamente:  
[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7712e8ad-dea4-4a43-8a7b-dc154510c104)  
(KB983589)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b547898e-f8a9-49dc-b49d-cffec5a001bc)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1620e7ac-3913-478d-8120-e9f46d98f453)  
(Importante)
</td>
<td style="border:1px solid black;">
[Movie Maker 6.0](http://www.microsoft.com/downloads/details.aspx?familyid=4baff9ae-dd25-4942-b45e-f281d0e1f4ac)<sup>[1]</sup>
(Importante)  

[Movie Maker 2.6](http://www.microsoft.com/downloads/details.aspx?familyid=0a226592-8f98-4f67-ac60-1d00cbc56598)<sup>[2]</sup>
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=18152cd4-815f-425f-8694-fbabcbe80609)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=110f932f-d13c-4486-a295-e6068d5d8d7a)  
(Importante)
</td>
</tr>
<tr>
<th colspan="14" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-046**](http://technet.microsoft.com/security/bulletin/ms10-046)
</td>
<td style="border:1px solid black;">
[**MS10-049**](http://technet.microsoft.com/security/bulletin/ms10-049)
</td>
<td style="border:1px solid black;">
[**MS10-051**](http://technet.microsoft.com/security/bulletin/ms10-051)
</td>
<td style="border:1px solid black;">
[**MS10-052**](http://technet.microsoft.com/security/bulletin/ms10-052)
</td>
<td style="border:1px solid black;">
[**MS10-053**](http://technet.microsoft.com/security/bulletin/ms10-053)
</td>
<td style="border:1px solid black;">
[**MS10-054**](http://technet.microsoft.com/security/bulletin/ms10-054)
</td>
<td style="border:1px solid black;">
[**MS10-055**](http://technet.microsoft.com/security/bulletin/ms10-055)
</td>
<td style="border:1px solid black;">
[**MS10-060**](http://technet.microsoft.com/security/bulletin/ms10-060)
</td>
<td style="border:1px solid black;">
[**MS10-047**](http://technet.microsoft.com/security/bulletin/ms10-047)
</td>
<td style="border:1px solid black;">
[**MS10-048**](http://technet.microsoft.com/security/bulletin/ms10-048)
</td>
<td style="border:1px solid black;">
[**MS10-050**](http://technet.microsoft.com/security/bulletin/ms10-050)
</td>
<td style="border:1px solid black;">
[**MS10-058**](http://technet.microsoft.com/security/bulletin/ms10-058)
</td>
<td style="border:1px solid black;">
[**MS10-059**](http://technet.microsoft.com/security/bulletin/ms10-059)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
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
Ninguna
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
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3aabd189-7d4c-4c9f-8854-f33127b1c309)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6e0253d4-f0c0-4f28-ba08-6907c2fcb339)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=73b5f45c-c9d6-491f-8483-98838b2a7c04)\*  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=8239cb9e-bb5a-4157-8038-33d0b329eaee)\*\*  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=409b9298-1e7d-48cf-9872-ffbdc56ebe53)\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a94e2e38-116a-4b63-9328-6c33e63bbbfe)\*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits únicamente:  
[Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=616c39f7-137a-40b9-b691-bc33c0aef7e1)\*\*  
(KB983587)  
(Crítica)  

Windows Server 2008 para sistemas de 32 bits únicamente:  
[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=155bbb5c-247e-4bed-a287-527d978b7967)\*\*  
(KB983588)  
(Crítica)  

Windows Server 2008 para sistemas de 32 bits Service Pack 2 únicamente:  
[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7712e8ad-dea4-4a43-8a7b-dc154510c104)\*\*  
(KB983589)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=611765ab-b3f3-45db-92b2-ee040b9cfd27)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a8b1a3f7-7147-494e-bfc0-b1979b9578e6)\*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=844404be-f2e8-47bc-9650-9e2bbe383814)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4c9b3e60-e166-40c9-8938-3cba0a399c47)\*  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=29c6fc2d-d318-4a63-9ab2-82e84272aaf2)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a96891ff-8771-47b3-81bb-8640adb6c098)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=43ece408-4aa7-4819-b3f6-7f0719ed3213)\*  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=5ef8abf0-c89e-4911-8d77-42400d9a398f)\*\*  
(Crítica)  

[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=9b869bab-0797-4f83-8c64-23dda9983c8d)\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=602dd3f6-0d09-4546-b1db-d7b6b04edb66)\*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 únicamente:  
[Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=616c39f7-137a-40b9-b691-bc33c0aef7e1)\*\*  
(KB983587)  
(Crítica)  

Windows Server 2008 para sistemas x64 únicamente:  
[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=155bbb5c-247e-4bed-a287-527d978b7967)\*\*  
(KB983588)  
(Crítica)  

Windows Server 2008 para sistemas x64 Service Pack 2 únicamente:  
[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7712e8ad-dea4-4a43-8a7b-dc154510c104)\*\*  
(KB983589)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=131f3512-1585-462e-a4f1-3f359aac44bd)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c1c25cb7-7e82-4c14-9666-aff52dd308b4)\*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=08491c73-66b1-4c4c-8740-ea596a730fc1)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=fa84e547-2190-402f-9467-2450deeff565)\*  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=cfe227b5-6660-49f8-9d71-a997dd83de0b)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3b16a422-0ee9-4eab-9cfe-e7688ffa0d76)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=b6faee94-e821-432d-bfa2-9008664566af)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=2f1eee63-2cca-4ec5-b196-36de3c0054cf)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=24d8f0a3-51a9-46c1-b870-a2239bf600e4)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium únicamente:  
[Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=616c39f7-137a-40b9-b691-bc33c0aef7e1)  
(KB983587)  
(Crítica)  

Windows Server 2008 para sistemas con Itanium únicamente:  
[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=155bbb5c-247e-4bed-a287-527d978b7967)  
(KB983588)  
(Crítica)  

Windows Server 2008 para sistemas con Itanium Service Pack 2 únicamente:  
[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7712e8ad-dea4-4a43-8a7b-dc154510c104)  
(KB983589)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=972efd3a-ec1e-49b2-835e-76f4b21b5b79)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=45fe5135-aa89-4f60-8cdb-ec0edc9a7e77)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8aa12902-c234-4fd9-bba3-6767eafc38fc)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=84f89dca-108c-4956-9aa2-866e17a872fc)  
(Importante)
</td>
</tr>
<tr>
<th colspan="14" style="border:1px solid black;">
Windows 7
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-046**](http://technet.microsoft.com/security/bulletin/ms10-046)
</td>
<td style="border:1px solid black;">
[**MS10-049**](http://technet.microsoft.com/security/bulletin/ms10-049)
</td>
<td style="border:1px solid black;">
[**MS10-051**](http://technet.microsoft.com/security/bulletin/ms10-051)
</td>
<td style="border:1px solid black;">
[**MS10-052**](http://technet.microsoft.com/security/bulletin/ms10-052)
</td>
<td style="border:1px solid black;">
[**MS10-053**](http://technet.microsoft.com/security/bulletin/ms10-053)
</td>
<td style="border:1px solid black;">
[**MS10-054**](http://technet.microsoft.com/security/bulletin/ms10-054)
</td>
<td style="border:1px solid black;">
[**MS10-055**](http://technet.microsoft.com/security/bulletin/ms10-055)
</td>
<td style="border:1px solid black;">
[**MS10-060**](http://technet.microsoft.com/security/bulletin/ms10-060)
</td>
<td style="border:1px solid black;">
[**MS10-047**](http://technet.microsoft.com/security/bulletin/ms10-047)
</td>
<td style="border:1px solid black;">
[**MS10-048**](http://technet.microsoft.com/security/bulletin/ms10-048)
</td>
<td style="border:1px solid black;">
[**MS10-050**](http://technet.microsoft.com/security/bulletin/ms10-050)
</td>
<td style="border:1px solid black;">
[**MS10-058**](http://technet.microsoft.com/security/bulletin/ms10-058)
</td>
<td style="border:1px solid black;">
[**MS10-059**](http://technet.microsoft.com/security/bulletin/ms10-059)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
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
Ninguna
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=22e62b5c-e4c1-47d0-ae4a-8bd2d70d0a0a)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=71716507-7080-4102-991e-6afc7cc377d5)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=31d0f5ac-2cff-42a1-8f18-128bbfc4e57d)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=ecaf42e0-a288-40c1-8602-21e967a87408)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=8d58ebc4-a5f9-4318-a6f1-168c1bcdae3c)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=2e782ac9-b5d5-490e-a01a-7d4481eab224)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=77d0c428-237c-4dab-9645-6400dd9e65f8)  
(KB983590)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=a7d60864-5942-47ed-a6f3-1c07b4833a14)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=68bddf4b-b597-477e-80e4-9293d7160496)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=3a5a088e-644a-4a0e-9a09-0370bcd97688)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=ce6233f3-2ee5-4329-908d-ba9b28ecc553)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=9499f771-c388-4de3-a5c7-8cc8b00b4395)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=c457d8ec-83b7-446f-b77c-e47d4187e616)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=a4f6d7c2-b475-4900-82f0-75f5be0b7b63)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=ca57a47a-9111-4abe-9356-4962ca2c1d65)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=ad1ddf94-d714-4b36-8256-42bf79d03a90)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=24751193-592f-4c44-a8d6-f4112d4f011b)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=77d0c428-237c-4dab-9645-6400dd9e65f8)  
(KB983590)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=b00ec47c-402e-4207-a4c9-6c1900f254f8)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=5ff09e03-d662-4b23-ab26-d25ca2ba58df)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=163fe2bd-f999-47c1-9a35-c4fc868bda51)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=146270fa-cd6f-440a-aa3e-e93af0bff447)  
(Importante)
</td>
</tr>
<tr>
<th colspan="14" style="border:1px solid black;">
Windows Server 2008 R2
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-046**](http://technet.microsoft.com/security/bulletin/ms10-046)
</td>
<td style="border:1px solid black;">
[**MS10-049**](http://technet.microsoft.com/security/bulletin/ms10-049)
</td>
<td style="border:1px solid black;">
[**MS10-051**](http://technet.microsoft.com/security/bulletin/ms10-051)
</td>
<td style="border:1px solid black;">
[**MS10-052**](http://technet.microsoft.com/security/bulletin/ms10-052)
</td>
<td style="border:1px solid black;">
[**MS10-053**](http://technet.microsoft.com/security/bulletin/ms10-053)
</td>
<td style="border:1px solid black;">
[**MS10-054**](http://technet.microsoft.com/security/bulletin/ms10-054)
</td>
<td style="border:1px solid black;">
[**MS10-055**](http://technet.microsoft.com/security/bulletin/ms10-055)
</td>
<td style="border:1px solid black;">
[**MS10-060**](http://technet.microsoft.com/security/bulletin/ms10-060)
</td>
<td style="border:1px solid black;">
[**MS10-047**](http://technet.microsoft.com/security/bulletin/ms10-047)
</td>
<td style="border:1px solid black;">
[**MS10-048**](http://technet.microsoft.com/security/bulletin/ms10-048)
</td>
<td style="border:1px solid black;">
[**MS10-050**](http://technet.microsoft.com/security/bulletin/ms10-050)
</td>
<td style="border:1px solid black;">
[**MS10-058**](http://technet.microsoft.com/security/bulletin/ms10-058)
</td>
<td style="border:1px solid black;">
[**MS10-059**](http://technet.microsoft.com/security/bulletin/ms10-059)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Moderada**](http://technet.microsoft.com/security/bulletin/rating)
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
Ninguna
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
Ninguna
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=0d9dd09b-db40-462b-88b0-4dbb8180e81f)\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=c9aeea25-ca14-4b42-9018-a27c9d8899c4)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=a48cdac5-4d78-49b5-a6d8-ecf6c58cace2)\*  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=e7757bbc-3ef0-421d-ab57-0083a302c77b)\*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=52642a8d-1081-4496-848e-9b03baf3fdac)\*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=77d0c428-237c-4dab-9645-6400dd9e65f8)\*  
(KB983590)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=c1ad1248-07f1-42d4-baa4-8a20837ec7b4)\*  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=6bbc9cb1-0b59-4473-adf9-2ce2f0f94c0a)\*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=a1f95600-34e5-44b3-b2cb-b2b2cbf645cb)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=333fb6e4-f867-4dcb-beb3-2d88e428ca2e)\*  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=ce2bb5d4-f661-44e3-ac28-0b81f7b72670)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=b7c2e91f-ca8a-4237-99c8-ca53c91cf73e)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft XML Core Services 3.0](http://www.microsoft.com/downloads/details.aspx?familyid=b4d3210e-f3ad-4dbb-9390-6e98eeb99eaa)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=7b457d04-03a9-4eb0-ba6a-ab45267e4f74)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=783fb42c-3698-4b1d-a692-3ff319578931)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=77d0c428-237c-4dab-9645-6400dd9e65f8)  
(KB983590)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=f23dec0f-a33b-4d8c-a86d-0e9368ae7ff5)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=2543191a-09cb-4417-bbb2-aac4d9a2a756)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=c3cd7f2f-e198-4fbd-a65d-21a1bf51eb61)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=62034ecb-a6bd-46c5-a03d-9642880bc2d6)  
(Importante)
</td>
</tr>
</table>
 
**Notas para Windows Server 2008 y Windows Server 2008 R2**

**\*La instalación de Server Core está afectada.** Esta actualización se aplica, con la misma clasificación de gravedad, a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, independientemente de si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**\*\*La instalación de Server Core no está afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

**Notas para MS10-050**

<sup>[1]</sup>Estas versiones de Windows Movie Maker se suministran con los sistemas operativos indicados.

<sup>[2]</sup>Windows Movie Maker 2.6 es una descarga opcional que se puede instalar en los sistemas operativos indicados.

**Nota para MS10-060**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

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
[**MS10-056**](http://technet.microsoft.com/security/bulletin/ms10-056)
</td>
<td style="border:1px solid black;">
[**MS10-057**](http://technet.microsoft.com/security/bulletin/ms10-057)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Office Word 2002 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=978eb887-25b6-4dde-a2ec-d2d1e7f1a434)  
(KB2251389)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2002 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=032e1530-8736-4e1c-a704-967679227619)  
(KB2264397)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Office Word 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=4360bcec-0731-4d4a-89eb-7d28a4607f06)  
(KB2251399)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office Excel 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=7cecbce3-bbb7-47d1-bda3-64d7e0f69f62)  
(KB2264403)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
2007 Microsoft Office System Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft Office Word 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=0d7210a3-662e-41e7-affc-ae94f9d89388)<sup>[1]</sup>
(KB2251419)  
(Crítica)
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
[**MS10-056**](http://technet.microsoft.com/security/bulletin/ms10-056)
</td>
<td style="border:1px solid black;">
[**MS10-057**](http://technet.microsoft.com/security/bulletin/ms10-057)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2004 para Mac
</td>
<td style="border:1px solid black;">
[Microsoft Office 2004 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=d2f44d4a-7cd8-4514-b3ff-1770bc47d595)  
(KB2284171)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2004 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=d2f44d4a-7cd8-4514-b3ff-1770bc47d595)  
(KB2284171)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2008 para Mac
</td>
<td style="border:1px solid black;">
[Microsoft Office 2008 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=6ece112f-0ca7-4b1f-ad20-603950edee66)  
(KB2284162)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2008 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=6ece112f-0ca7-4b1f-ad20-603950edee66)  
(KB2284162)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Convertidor de archivos con formatos XML abiertos para Mac
</td>
<td style="border:1px solid black;">
[Convertidor de archivos con formatos XML abiertos para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=a7b834a3-5a44-42d4-afe9-6ef207333834)  
(KB2284179)  
(Importante)
</td>
<td style="border:1px solid black;">
[Convertidor de archivos con formatos XML abiertos para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=a7b834a3-5a44-42d4-afe9-6ef207333834)  
(KB2284179)  
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
[**MS10-056**](http://technet.microsoft.com/security/bulletin/ms10-056)
</td>
<td style="border:1px solid black;">
[**MS10-057**](http://technet.microsoft.com/security/bulletin/ms10-057)
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
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Word Viewer
</td>
<td style="border:1px solid black;">
[Microsoft Office Word Viewer](http://www.microsoft.com/downloads/details.aspx?familyid=39fe2229-9201-4270-bdc1-20bc8e30a766)  
(KB2251437)  
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
[Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ed5b9671-651d-41f3-aed3-93ee8a28657f)  
(KB2277947)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Works 9
</td>
<td style="border:1px solid black;">
[Microsoft Works 9](http://www.microsoft.com/downloads/details.aspx?familyid=feb121ad-e5f6-40e2-bf12-045ae5c2a754)  
(KB2092914)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
**Nota para MS10-056**

<sup>[1]</sup>Para Microsoft Office Word 2007 Service Pack 2, además del paquete de actualización de seguridad KB2251419, los clientes también deben instalar la actualización de seguridad para Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2 (KB2277947) con el fin de protegerse de las vulnerabilidades descritas en MS10-056.

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
Microsoft Silverlight
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS10-060**](http://technet.microsoft.com/security/bulletin/ms10-060)
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
Microsoft Silverlight 2
</td>
<td style="border:1px solid black;">
[Microsoft Silverlight 2](http://www.microsoft.com/getsilverlight/get-started/install/default.aspx)<sup>[1]</sup> cuando está instalado en Mac  
(KB982926)  
(Crítica)  

[Microsoft Silverlight 2](http://www.microsoft.com/getsilverlight/get-started/install/default.aspx)<sup>[1]</sup> cuando está instalado en todas las versiones de los clientes Microsoft Windows  
(KB982926)  
(Crítica)  

[Microsoft Silverlight 2](http://www.microsoft.com/getsilverlight/get-started/install/default.aspx)<sup>[1]</sup> cuando está instalado en todas las versiones de los servidores Microsoft Windows\*\*  
(KB982926)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Silverlight 3
</td>
<td style="border:1px solid black;">
[Microsoft Silverlight 3](http://www.microsoft.com/downloads/details.aspx?familyid=7e3f6c16-1339-49bc-a60c-ddc6c3a54850)<sup>[2]</sup> cuando está instalado en Mac  
(KB978464)  
(Crítica)  

[Microsoft Silverlight 3](http://www.microsoft.com/downloads/details.aspx?familyid=7e3f6c16-1339-49bc-a60c-ddc6c3a54850)<sup>[2]</sup> cuando está instalado en todas las versiones de los clientes Microsoft Windows  
(KB978464)  
(Crítica)  

[Microsoft Silverlight 3](http://www.microsoft.com/downloads/details.aspx?familyid=7e3f6c16-1339-49bc-a60c-ddc6c3a54850)<sup>[2]</sup> cuando está instalado en todas las versiones de los servidores Microsoft Windows\*\*  
(KB978464)  
(Crítica)
</td>
</tr>
</table>
 
**Notas para MS10-060**

**\*\*La instalación de Server Core no está afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

<sup>[1]</sup>Esta descarga actualiza Microsoft Silverlight 2 a una versión más reciente que no está afectada por las vulnerabilidades descritas en el boletín.

<sup>[2]</sup>Esta actualización actualiza Microsoft Silverlight a una compilación posterior que no está afectada por las vulnerabilidades descritas en el boletín.

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/default.aspx). [TechNet Security Center](http://technet.microsoft.com/es-es/security/default.aspx) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://go.microsoft.com/fwlink/?linkid=85102), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS07-036"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Nota** A partir del 1 de agosto de 2009, Microsoft dejó de ofrecer soporte técnico a Office Update y Office Update Inventory Tool. Para seguir obteniendo las actualizaciones más recientes para los productos de Microsoft, use [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747). Para obtener más información, vea [Acerca de Microsoft Office Update: Preguntas más frecuentes](http://office.microsoft.com/en-us/downloads/fx010402221033.aspx).

**Consejos para la detección y la implementación**

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747).

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://technet.microsoft.com/es-es/security/cc184924.aspx).

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores de TI implementar las actualizaciones de productos de Microsoft más recientes en los equipos que ejecutan el sistema operativo Windows. Para obtener más información acerca de cómo implementar las actualizaciones de seguridad con Windows Server Update Services, vea el artículo de TechNet [Windows Server Update Services](http://technet.microsoft.com/en-us/wsus/default.aspx).

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. La siguiente versión de SMS, System Center Configuration Manager 2007, ya está disponible; consulte también [System Center Configuration Manager 2007](http://technet.microsoft.com/en-us/library/bb735860.aspx). Para obtener más información acerca de cómo pueden utilizar los administradores SMS 2003 para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar Security Update Inventory Tool (SUIT) como ayuda para implementar las actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://go.microsoft.com/fwlink/?linkid=21158).

**Nota** SMS usa las herramientas Microsoft Baseline Security Analyzer para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet2.microsoft.com/windowsvista/en/library/4279e239-37a4-44aa-aec5-4e70fe39f9de1033.mspx?mfr=true) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Microsoft Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Microsoft Knowledge Base, artículo 894199](http://support.microsoft.com/kb/894199): Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones de meses anteriores para Windows Server Update Services](http://technet.microsoft.com/en-us/wsus/bb456965.aspx). Muestra todas las actualizaciones nuevas, revisadas y publicadas de nuevo para los productos de Microsoft que no sean Microsoft Windows.

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

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [IT Pro Security Community](http://technet.microsoft.com/es-es/security/cc136632.aspx) (en inglés).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://technet.microsoft.com/security/bulletin/policy) a todas las personas que han trabajado con nosotros para proteger a los clientes:

-   Sergey I. Ulasen y Oleg Kupreev, de [VirusBlokAda](http://www.anti-virus.by/), por informar de un problema descrito en MS10-046
-   Andreas Marx y Maik Morgenstern, de [AV-Test](http://www.av-test.org/), por informar de un problema descrito en MS10-046
-   Will Dormann, de [CERT/CC](http://www.cert.org), por colaborar con nosotros en un problema descrito en MS10-046
-   Niels Teusink, por colaborar con nosotros en un problema descrito en MS10-046
-   Stefan Kanthak, por colaborar con nosotros en un problema descrito en MS10-046
-   Tavis Ormandy, de [Google Inc.](http://www.google.com/), por informar de tres problemas descritos en MS10-047
-   Tavis Ormandy, de [Google Inc.](http://www.google.com/), por informar de un problema descrito en MS10-048
-   Matthieu Suiche, de [MoonSols](http://moonsols.com/), por informar de dos problemas descritos en MS10-048
-   Matthieu Suiche, de [MoonSols](http://moonsols.com/), por colaborar con nosotros en los cambios de defensa tratados en MS10-048
-   Nicolás Economou, de [Core Security Technologies](http://www.coresecurity.com/), por informar de un problema descrito en MS10-048
-   Marsh Ray y Steve Dispensa, de [PhoneFactor](http://www.phonefactor.com/), por informar de un problema descrito en MS10-049
-   Dyon Balding, de [Secunia](http://secunia.com/), por informar de un problema descrito en MS10-050
-   Skylined, de [Google Inc.](http://www.google.com/), por informar de un problema descrito en MS10-051
-   Moritz Jodeit, de n.runs AG, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS10-052
-   David Bloom, de [Google Inc.](http://www.google.com/), por informar de un problema descrito en MS10-053
-   Nicolas Joly, de [VUPEN Vulnerability Research Team](http://www.vupen.com), por informar de cuatro problemas descritos en MS10-053
-   Gambino ZaDarkSide, por informar de un problema descrito en MS10-053
-   Laurent Gaffié, de [stratsec](http://www.stratsec.net/), por informar de un problema descrito en MS10-054
-   Todd Wease y Richard Johnson, de [Sourcefire VRT](http://www.sourcefire.com/services/sf_vrt.html), por informar de un problema descrito en MS10-054
-   Riku Hietamaki y Joshua Morin, de [Codenomicon](http://www.codenomicon.com/), por informar de un problema descrito en MS10-054
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS10-055
-   L.W.Z, de [team509](http://www.team509.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS10-056
-   Wushi, de [team509](http://www.team509.com/), en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS10-056
-   [team509](http://www.team509.com/), en colaboración con [Verisign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS10-056
-   Rodrigo Rubira Branco, del equipo de investigación IPS de [Check Point](http://www.checkpoint.com/), por informar de un problema descrito en MS10-056
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS10-056
-   Damian Frizza, de [Core Security Technologies](http://www.coresecurity.com/), por informar de un problema descrito en MS10-057
-   Darren Willis, de [Fourteenforty Research Institute, Inc.](http://www.fourteenforty.jp/), por informar de un problema descrito en MS10-058
-   Matthieu Suiche, de [MoonSols](http://moonsols.com/), por informar de un problema descrito en MS10-058
-   Cesar Cerrudo, de [Argeniss](http://www.argeniss.com/), por colaborar con nosotros en dos problemas descritos en MS10-059
-   Carsten Book, de , por informar de un problema descrito en MS10-060
-   [Eamon Nerbonne](http://eamon.nerbonne.org/), por informar de un problema descrito en MS10-060

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Los clientes de Estados Unidos y Canadá pueden recibir soporte técnico del [soporte de seguridad](http://go.microsoft.com/fwlink/?linkid=21131) o en el teléfono 1-866-PCSAFETY. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de las opciones de asistencia disponibles, visite [Ayuda y soporte técnico de Microsoft](http://support.microsoft.com/).
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (2 de agosto de 2010): Publicación del resumen del boletín.
-   V2.0 (10 de agosto de 2010): Se han agregado los boletines MS10-047 a MS10-060.
-   V2.1 (1 de septiembre de 2010): Se ha agregado una nota para MS10-056 para informar a los clientes que usan Word 2007 de que además del paquete de actualización de seguridad KB2251419, también deben instalar el paquete de actualización de seguridad KB2277947.

*Built at 2014-04-18T01:50:00Z-07:00*
