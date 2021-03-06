---
TOCTitle: 'MS09-OCT'
Title: Resumen del boletín de seguridad de Microsoft de octubre 2009
ms:assetid: 'ms09-oct'
ms:contentKeyID: 61225406
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms09-oct(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de octubre 2009
=============================================================

Publicado: martes, 13 de octubre de 2009 | Actualizado: martes, 22 de junio de 2010

**Versión:** 4.2

Este resumen del boletín enumera los boletines de seguridad publicados para octubre de 2009.

Con la publicación de los boletines de octubre de 2009, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 8 de octubre de 2009. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/advance) .

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 14 de octubre de 2009, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de octubre](http://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032407488&culture=en-us) . Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/security/bulletin/summary) .

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad y de alta prioridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional** .

### Información del boletín

Resúmenes ejecutivos
--------------------

En la tabla siguiente se resumen los boletines de seguridad de este mes por orden de gravedad.

Para obtener detalles acerca del software afectado, vea la siguiente sección, **Ubicaciones de descarga y software afectado** .

 
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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-050">MS09-050</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Smbv2 podrían permitir la ejecución remota de código (975517)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y dos vulnerabilidades de las que se ha informado de forma privada en Bloque de mensajes del servidor versión 2 (SMBv2). La vulnerabilidad más grave podría permitir la ejecución remota de código si un atacante envía un paquete SMB especialmente diseñado a un equipo que ejecute el servicio Servidor. Los procedimientos recomendados para firewall y las configuraciones de firewall predeterminadas estándar pueden proteger a las redes de los ataques procedentes del exterior del perímetro de la empresa. Se recomienda que los sistemas conectados a Internet tengan expuesta la cantidad mínima de puertos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-051">MS09-051</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en el módulo de tiempo de ejecución de Windows Media podrían permitir la ejecución remota de código (975682)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en el módulo de tiempo de ejecución de Windows Media. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario abre un archivo multimedia especialmente diseñado o recibe contenido de secuencias especialmente diseñado de un sitio web o de cualquier aplicación que proporcione contenido web. Un intruso que aprovechara estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario local. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-052">MS09-052</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el Reproductor de Windows Media podría permitir la ejecución remota de código (974112)</strong><br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad en Reproductor de Windows Media de la que se ha informado de forma privada. La vulnerabilidad podría permitir la ejecución remota de código si se reproduce un archivo ASF especialmente diseñado mediante Reproductor de Windows Media 6.4. Un atacante que aprovechara esta vulnerabilidad podría obtener los mismos derechos de usuario que el usuario local. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-054">MS09-054</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (974455)</strong><br />
<br />
Esta actualización de seguridad resuelve tres vulnerabilidades de las que se ha informado de forma privada y una vulnerabilidad de la que se ha informado de forma pública en Internet Explorer. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. Los usuarios de Firefox que ejecutan el complemento de Windows Presentation Foundation (WPF) y no lo tienen deshabilitado, también deben aplicar esta actualización de seguridad. Para obtener más información acerca de este problema, consulte la sección de preguntas más frecuentes de la vulnerabilidad en el tratamiento de componentes HTML (CVE-2009-2529).</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-055">MS09-055</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa de bits de interrupción de ActiveX (973525)</strong><br />
<br />
Esta actualización de seguridad corrige una vulnerabilidad de la que se ha informado de forma privada que es común a varios controles ActiveX y que se está aprovechando actualmente. La vulnerabilidad que afecta a los controles ActiveX que se compilaron con la versión vulnerable de Microsoft Active Template Library (ATL) podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada con Internet Explorer, con lo que se ejecuta el control ActiveX. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-060">MS09-060</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en los controles ActiveX de Microsoft Active Template Library (ATL) podrían permitir la ejecución remota de código en Microsoft Office (973965)</strong><br />
<br />
Esta actualización de seguridad resuelve varias vulnerabilidades de las que se ha informado de forma privada en los controles ActiveX para Microsoft Office que se han compilado con una versión vulnerable de Microsoft Active Template Library (ATL). Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario carga un componente o control especialmente diseñado. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-061">MS09-061</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft .NET Common Language Runtime podrían permitir la ejecución remota de código (974378)</strong><br />
<br />
Esta actualización de seguridad resuelve tres vulnerabilidades de las que se ha informado de forma privada en Microsoft .NET Framework y Microsoft Silverlight. Las vulnerabilidades podrían permitir la ejecución remota de código en un sistema cliente si un usuario visualiza una página web especialmente diseñada mediante un explorador web que pueda ejecutar aplicaciones XAML del explorador (XBAP) o aplicaciones Silverlight, o si un atacante consigue convencer a un usuario para que ejecute una aplicación Microsoft .NET especialmente diseñada. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos. Las vulnerabilidades también podrían permitir la ejecución remota de código en un sistema de servidor que ejecute IIS si dicho servidor permite el procesamiento de páginas ASP.NET y un atacante consigue cargar una página ASP.NET especialmente diseñada en el servidor y la ejecuta, como puede ser el caso de un escenario de hospedaje web. Las aplicaciones Microsoft .NET, las aplicaciones Silverlight, las aplicaciones XBAP y las páginas ASP.NET que no sean malintencionadas no están expuestas a esta vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Microsoft .NET Framework,<br />
Microsoft Silverlight</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-062">MS09-062</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en GDI+ podría permitir la ejecución remota de código (957488)</strong><br />
<br />
Esta actualización de seguridad resuelve varias vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows GDI+. Estas vulnerabilidades podrían permitir la ejecución remota de código si un usuario visualiza un archivo de imagen especialmente diseñado con el software afectado o explora un sitio web que incluya contenido especialmente diseñado. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Crítica</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer,<br />
Microsoft .NET Framework,<br />
Microsoft Office,<br />
Microsoft SQL Server,<br />
Herramientas de desarrollo de Microsoft,<br />
Microsoft Forefront</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-053">MS09-053</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en el servicio FTP de Internet Information Services podrían permitir la ejecución remota de código (975254)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades que se han divulgado de forma pública en el servicio FTP en Microsoft Internet Information Services (IIS) 5.0, Microsoft Internet Information Services (IIS) 5.1, Microsoft Internet Information Services (IIS) 6.0 y Microsoft Internet Information Services (IIS) 7.0. En IIS 7.0, sólo está afectado el servicio FTP 6.0. Las vulnerabilidades podrían permitir la ejecución remota de código (RCE) en los sistemas que ejecutan el servicio FTP en IIS 5.0, o la denegación de servicio (DoS) en los sistemas que ejecutan el servicio FTP en IIS 5.0, IIS 5.1, IIS 6.0 o IIS 7.0.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-056">MS09-056</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Windows CryptoAPI podrían permitir la suplantación de identidad (spoofing) (974571)</strong><br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. Las vulnerabilidades podrían permitir la suplantación de identidad si un atacante obtiene acceso al certificado que usa el usuario final para la autenticación.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Suplantación</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-057">MS09-057</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en los servicios de Index Server podría permitir la ejecución remota de código (969059)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un atacante configura una página web malintencionada que invoque el servicio de Index Server a través de una llamada a su componente ActiveX. Esta llamada podría incluir una dirección URL malintencionada y aprovechar la vulnerabilidad, lo que concedería al atacante acceso al sistema cliente con los privilegios del usuario que explora la página web. Por tanto, los usuarios cuyas cuentas estén configuradas con pocos derechos de usuario en el sistema correrían un riesgo menor que aquellos que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-058">MS09-058</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades del kernel de Windows podrían permitir la elevación de privilegios (971486)</strong><br />
<br />
Esta actualización de seguridad resuelve varias vulnerabilidades en el kernel de Windows de las que se ha informado de forma privada. La vulnerabilidad más grave podría permitir la elevación de privilegios si un atacante ha iniciado sesión en el sistema y ha ejecutado una aplicación especialmente diseñada. Para aprovechar estas vulnerabilidades, un atacante debe tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar sesión de forma local en el sistema. Los usuarios anónimos o los usuarios remotos no pueden aprovechar estas vulnerabilidades.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/ms09-059">MS09-059</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el servicio del subsistema de autoridad de seguridad local podría permitir la denegación de servicio (975467)</strong><br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la denegación de servicio si un atacante envía un paquete diseñado de forma malintencionada durante el proceso de autenticación NTLM.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/bulletin/rating">Importante</a><br />
Denegación de servicio</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y de identificador de CVE.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de que se publique código funcional que aproveche la vulnerabilidad en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Debe revisar cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/es-es/security/cc998259.aspx) .
  
| Identificador del boletín                                           | Título del boletín                                                                                                                                               | Identificador CVE                                                                | Evaluación de índice de explotabilidad                                                                                                | Notas clave                                                                                                                                                                                                                                                                                                                                                                                                                          |  
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
| [MS09-050](http://technet.microsoft.com/security/bulletin/ms09-050) | Vulnerabilidades en Smbv2 podrían permitir la ejecución remota de código (975517)                                                                                | [CVE-2009-2526](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2526) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | Se trata de una vulnerabilidad de denegación de servicio limitada.                                                                                                                                                                                                                                                                                                                                                                   |  
| [MS09-050](http://technet.microsoft.com/security/bulletin/ms09-050) | Vulnerabilidades en Smbv2 podrían permitir la ejecución remota de código (975517)                                                                                | [CVE-2009-2532](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2532) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-050](http://technet.microsoft.com/security/bulletin/ms09-050) | Vulnerabilidades en Smbv2 podrían permitir la ejecución remota de código (975517)                                                                                | [CVE-2009-3103](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-3103) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | Se ha hecho público el código que aprovecha la vulnerabilidad.                                                                                                                                                                                                                                                                                                                                                                       |  
| [MS09-051](http://technet.microsoft.com/security/bulletin/ms09-051) | Vulnerabilidades en el módulo de tiempo de ejecución de Windows Media podrían permitir la ejecución remota de código (975682)                                    | [CVE-2009-0555](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0555) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-051](http://technet.microsoft.com/security/bulletin/ms09-051) | Vulnerabilidades en el módulo de tiempo de ejecución de Windows Media podrían permitir la ejecución remota de código (975682)                                    | [CVE-2009-2525](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2525) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-052](http://technet.microsoft.com/security/bulletin/ms09-052) | Una vulnerabilidad en el Reproductor de Windows Media podría permitir la ejecución remota de código (974112)                                                     | [CVE-2009-2527](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2527) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-053](http://technet.microsoft.com/security/bulletin/ms09-053) | Vulnerabilidades en el servicio FTP de Internet Information Services podrían permitir la ejecución remota de código (975254)                                     | [CVE-2009-2521](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2521) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | Se trata de una vulnerabilidad de denegación de servicio. Se ha hecho público el código que aprovecha la vulnerabilidad.                                                                                                                                                                                                                                                                                                             |  
| [MS09-053](http://technet.microsoft.com/security/bulletin/ms09-053) | Vulnerabilidades en el servicio FTP de Internet Information Services podrían permitir la ejecución remota de código (975254)                                     | [CVE-2009-3023](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-3023) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | Se ha hecho público el código que aprovecha la vulnerabilidad.                                                                                                                                                                                                                                                                                                                                                                       |  
| [MS09-054](http://technet.microsoft.com/security/bulletin/ms09-054) | Actualización de seguridad acumulativa para Internet Explorer (974455)                                                                                           | [CVE-2009-1547](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-1547) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-054](http://technet.microsoft.com/security/bulletin/ms09-054) | Actualización de seguridad acumulativa para Internet Explorer (974455)                                                                                           | [CVE-2009-2529](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2529) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-054](http://technet.microsoft.com/security/bulletin/ms09-054) | Actualización de seguridad acumulativa para Internet Explorer (974455)                                                                                           | [CVE-2009-2530](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2530) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | En los sistemas de Microsoft Windows 2000, la falta de protecciones del montón aumenta la evaluación de índice explotabilidad a [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad.                                                                                                                                                                |  
| [MS09-054](http://technet.microsoft.com/security/bulletin/ms09-054) | Actualización de seguridad acumulativa para Internet Explorer (974455)                                                                                           | [CVE-2009-2531](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2531) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      |                                                                                                                                                                                                                                                                                                                                                                                                                                      |  
| [MS09-055](http://technet.microsoft.com/security/bulletin/ms09-055) | Actualización de seguridad acumulativa de bits de interrupción de ActiveX (973525)                                                                               | [CVE-2009-2493](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2493) | Ninguna                                                                                                                               | (A esta vulnerabilidad ya se le ha asignado una evaluación de índice de explotabilidad en el [resumen del boletín de julio](http://technet.microsoft.com/security/bulletin/ms09-jul) . Esto se debe a que esta vulnerabilidad ya se trató por primera vez en [MS09-035](http://technet.microsoft.com/security/bulletin/ms09-035) .) Vea el mismo número CVE en [MS09-060](http://technet.microsoft.com/security/bulletin/ms09-060) . |  
| [MS09-056](http://technet.microsoft.com/security/bulletin/ms09-056) | Vulnerabilidades en Windows CryptoAPI podrían permitir la suplantación de identidad (spoofing) (974571)                                                          | [CVE-2009-2510](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2510) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | Se trata de una vulnerabilidad de suplantación.                                                                                                                                                                                                                                                                                                                                                                                      |  
| [MS09-056](http://technet.microsoft.com/security/bulletin/ms09-056) | Vulnerabilidades en Windows CryptoAPI podrían permitir la suplantación de identidad (spoofing) (974571)                                                          | [CVE-2009-2511](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2511) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | Se trata de una vulnerabilidad de suplantación.                                                                                                                                                                                                                                                                                                                                                                                      |  
| [MS09-057](http://technet.microsoft.com/security/bulletin/ms09-057) | Una vulnerabilidad en Servicios de Index Server podría permitir la ejecución remota de código (969059)                                                           | [CVE-2009-2507](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2507) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-058](http://technet.microsoft.com/security/bulletin/ms09-058) | Vulnerabilidades en el kernel de Windows podrían permitir la elevación de privilegios (971486)                                                                   | [CVE-2009-2515](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2515) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-058](http://technet.microsoft.com/security/bulletin/ms09-058) | Vulnerabilidades en el kernel de Windows podrían permitir la elevación de privilegios (971486)                                                                   | [CVE-2009-2516](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2516) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | Esta vulnerabilidad provoca una condición de denegación de servicio cuando se usa un recurso compartido de red y una condición de elevación de privilegios cuando se usa localmente para atacar un sistema local.                                                                                                                                                                                                                    |  
| [MS09-058](http://technet.microsoft.com/security/bulletin/ms09-058) | Vulnerabilidades en el kernel de Windows podrían permitir la elevación de privilegios (971486)                                                                   | [CVE-2009-2517](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2517) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | Se trata de una vulnerabilidad de denegación de servicio.                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-059](http://technet.microsoft.com/security/bulletin/ms09-059) | Vulnerabilidad en el servicio de subsistema de autoridad de seguridad local podría permitir la denegación de servicio (975467)                                   | [CVE-2009-2524](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2524) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | Se trata de una vulnerabilidad de denegación de servicio limitada.                                                                                                                                                                                                                                                                                                                                                                   |  
| [MS09-060](http://technet.microsoft.com/security/bulletin/ms09-060) | Vulnerabilidades en los controles ActiveX de Microsoft Active Template Library (ATL) podrían permitir la ejecución remota de código en Microsoft Office (973965) | [CVE-2009-0901](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0901) | Ninguna                                                                                                                               | (A esta vulnerabilidad ya se le ha asignado una evaluación de índice de explotabilidad en el [resumen del boletín de julio](http://technet.microsoft.com/security/bulletin/ms09-jul) . Esto se debe a que esta vulnerabilidad ya se trató por primera vez en [MS09-035](http://technet.microsoft.com/security/bulletin/ms09-035) .)                                                                                                  |  
| [MS09-060](http://technet.microsoft.com/security/bulletin/ms09-060) | Vulnerabilidades en los controles ActiveX de Microsoft Active Template Library (ATL) podrían permitir la ejecución remota de código en Microsoft Office (973965) | [CVE-2009-2493](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2493) | Ninguna                                                                                                                               | (A esta vulnerabilidad ya se le ha asignado una evaluación de índice de explotabilidad en el [resumen del boletín de julio](http://technet.microsoft.com/security/bulletin/ms09-jul) . Esto se debe a que esta vulnerabilidad ya se trató por primera vez en [MS09-035](http://technet.microsoft.com/security/bulletin/ms09-035) .) Vea el mismo número CVE en [MS09-055](http://technet.microsoft.com/security/bulletin/ms09-055) . |  
| [MS09-060](http://technet.microsoft.com/security/bulletin/ms09-060) | Vulnerabilidades en los controles ActiveX de Microsoft Active Template Library (ATL) podrían permitir la ejecución remota de código en Microsoft Office (973965) | [CVE-2009-2495](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2495) | [**3**](http://technet.microsoft.com/es-es/security/cc998259.aspx) Improbabilidad de código funcional que aproveche la vulnerabilidad | Esta vulnerabilidad afecta a la divulgación de información.                                                                                                                                                                                                                                                                                                                                                                          |  
| [MS09-061](http://technet.microsoft.com/security/bulletin/ms09-061) | Vulnerabilidades en Microsoft .NET Common Language Runtime podrían permitir la ejecución remota de código (974378)                                               | [CVE-2009-0090](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0090) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-061](http://technet.microsoft.com/security/bulletin/ms09-061) | Vulnerabilidades en Microsoft .NET Common Language Runtime podrían permitir la ejecución remota de código (974378)                                               | [CVE-2009-0091](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-0091) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-061](http://technet.microsoft.com/security/bulletin/ms09-061) | Vulnerabilidades en Microsoft .NET Common Language Runtime podrían permitir la ejecución remota de código (974378)                                               | [CVE-2009-2497](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2497) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | Existe el potencial de ataques que afectan a Internet.                                                                                                                                                                                                                                                                                                                                                                               |  
| [MS09-062](http://technet.microsoft.com/security/bulletin/ms09-062) | Vulnerabilidades en GDI+ podría permitir la ejecución remota de código (957488)                                                                                  | [CVE-2009-2500](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2500) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-062](http://technet.microsoft.com/security/bulletin/ms09-062) | Vulnerabilidades en GDI+ podría permitir la ejecución remota de código (957488)                                                                                  | [CVE-2009-2501](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2501) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-062](http://technet.microsoft.com/security/bulletin/ms09-062) | Vulnerabilidades en GDI+ podría permitir la ejecución remota de código (957488)                                                                                  | [CVE-2009-2502](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2502) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-062](http://technet.microsoft.com/security/bulletin/ms09-062) | Vulnerabilidades en GDI+ podría permitir la ejecución remota de código (957488)                                                                                  | [CVE-2009-2503](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2503) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-062](http://technet.microsoft.com/security/bulletin/ms09-062) | Vulnerabilidades en GDI+ podría permitir la ejecución remota de código (957488)                                                                                  | [CVE-2009-2504](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2504) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-062](http://technet.microsoft.com/security/bulletin/ms09-062) | Vulnerabilidades en GDI+ podría permitir la ejecución remota de código (957488)                                                                                  | [CVE-2009-2518](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2518) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-062](http://technet.microsoft.com/security/bulletin/ms09-062) | Vulnerabilidades en GDI+ podría permitir la ejecución remota de código (957488)                                                                                  | [CVE-2009-2528](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-2528) | [**1**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Bastante probabilidad de código que aproveche la vulnerabilidad  | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |  
| [MS09-062](http://technet.microsoft.com/security/bulletin/ms09-062) | Vulnerabilidades en GDI+ podría permitir la ejecución remota de código (957488)                                                                                  | [CVE-2009-3126](http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2009-3126) | [**2**](http://technet.microsoft.com/es-es/security/cc998259.aspx) - Poca probabilidad de código que aproveche la vulnerabilidad      | (Ninguna)                                                                                                                                                                                                                                                                                                                                                                                                                            |
  
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
</tr>
<tr>
<th colspan="13" style="border:1px solid black;">
Microsoft Windows 2000  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-050**](http://technet.microsoft.com/security/bulletin/ms09-050)
</td>
<td style="border:1px solid black;">
[**MS09-051**](http://technet.microsoft.com/security/bulletin/ms09-051)
</td>
<td style="border:1px solid black;">
[**MS09-052**](http://technet.microsoft.com/security/bulletin/ms09-052)
</td>
<td style="border:1px solid black;">
[**MS09-054**](http://technet.microsoft.com/security/bulletin/ms09-054)
</td>
<td style="border:1px solid black;">
[**MS09-055**](http://technet.microsoft.com/security/bulletin/ms09-055)
</td>
<td style="border:1px solid black;">
[**MS09-061**](http://technet.microsoft.com/security/bulletin/ms09-061)
</td>
<td style="border:1px solid black;">
[**MS09-062**](http://technet.microsoft.com/security/bulletin/ms09-062)
</td>
<td style="border:1px solid black;">
[**MS09-053**](http://technet.microsoft.com/security/bulletin/ms09-053)
</td>
<td style="border:1px solid black;">
[**MS09-056**](http://technet.microsoft.com/security/bulletin/ms09-056)
</td>
<td style="border:1px solid black;">
[**MS09-057**](http://technet.microsoft.com/security/bulletin/ms09-057)
</td>
<td style="border:1px solid black;">
[**MS09-058**](http://technet.microsoft.com/security/bulletin/ms09-058)
</td>
<td style="border:1px solid black;">
[**MS09-059**](http://technet.microsoft.com/security/bulletin/ms09-059)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Ninguna**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Windows 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Códec de voz de WMA de DirectShow](http://www.microsoft.com/downloads/details.aspx?familyid=4fe0dff5-04d9-4409-8d1d-52419537126b)  
(KB969878)  
(Crítica)  

[Descodificador de voz de Windows Media Audio](http://www.microsoft.com/downloads/details.aspx?familyid=8f850a82-61f9-447b-a0aa-a2c192cc5d2e)  
(KB954155)  
(Crítica)  

[Administrador de compresión de audio](http://www.microsoft.com/downloads/details.aspx?familyid=6dfd5405-cabe-4bd7-9330-b6bde1d99194)  
(KB975025)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Reproductor de Microsoft Windows Media 6.4](http://www.microsoft.com/downloads/details.aspx?familyid=13035ef7-7e47-487c-8b7c-7795d33ce7de)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 5.01 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=26515c7b-d7a6-4405-96b5-a518dcb39d38)  
(Crítica)  

[Microsoft Internet Explorer 6 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=8154ba37-0fbc-4d31-9d6e-0b21586ad65a)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=edfea805-9544-4dc0-a52c-d7594205657b)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=78ac8b97-8327-4ae1-8bb0-6cf227f3968f) (KB953297)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d4a328b5-5470-46b0-86c7-cfe0e6a3ea01) (KB953300)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=491874d4-5eea-4545-9b7d-3861857c862e) (KB974417)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=f3fef608-dafb-4b37-a65a-9cc4ae8e2c4c)  
(KB958869)  
(Crítica)  

[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=ecf78619-80fa-417d-852b-1b5b2cf574e2)  
(KB971108)  
(Importante)  

[Microsoft .NET Framework 2.0 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=3e534aa8-29c2-4379-9f57-931a6ff47418)  
(KB971110)  
(Importante)  

[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e6f5e730-85cc-4c08-a50d-c456b1e9f5bc)  
(KB971111)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=7fecd367-aaff-458b-91bc-8925c8e57528)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=52b9198d-b65f-467a-a5ab-141e23d64a86)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=b34d94b5-b828-4e16-a636-04344c60d945)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Windows 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=bdfa6583-28a2-4d6b-91d2-157a8518b664)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="13" style="border:1px solid black;">
Windows XP
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-050**](http://technet.microsoft.com/security/bulletin/ms09-050)
</td>
<td style="border:1px solid black;">
[**MS09-051**](http://technet.microsoft.com/security/bulletin/ms09-051)
</td>
<td style="border:1px solid black;">
[**MS09-052**](http://technet.microsoft.com/security/bulletin/ms09-052)
</td>
<td style="border:1px solid black;">
[**MS09-054**](http://technet.microsoft.com/security/bulletin/ms09-054)
</td>
<td style="border:1px solid black;">
[**MS09-055**](http://technet.microsoft.com/security/bulletin/ms09-055)
</td>
<td style="border:1px solid black;">
[**MS09-061**](http://technet.microsoft.com/security/bulletin/ms09-061)
</td>
<td style="border:1px solid black;">
[**MS09-062**](http://technet.microsoft.com/security/bulletin/ms09-062)
</td>
<td style="border:1px solid black;">
[**MS09-053**](http://technet.microsoft.com/security/bulletin/ms09-053)
</td>
<td style="border:1px solid black;">
[**MS09-056**](http://technet.microsoft.com/security/bulletin/ms09-056)
</td>
<td style="border:1px solid black;">
[**MS09-057**](http://technet.microsoft.com/security/bulletin/ms09-057)
</td>
<td style="border:1px solid black;">
[**MS09-058**](http://technet.microsoft.com/security/bulletin/ms09-058)
</td>
<td style="border:1px solid black;">
[**MS09-059**](http://technet.microsoft.com/security/bulletin/ms09-059)
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
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
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
No aplicable
</td>
<td style="border:1px solid black;">
[Códec de voz de WMA de DirectShow](http://www.microsoft.com/downloads/details.aspx?familyid=4fe0dff5-04d9-4409-8d1d-52419537126b)  
(KB969878)  
(Crítica)  

[Descodificador de voz de Windows Media Audio](http://www.microsoft.com/downloads/details.aspx?familyid=4516c219-e357-485e-a52b-23dcb8ee49d8)  
(KB954155)  
(Crítica)  
(Windows XP Service Pack 2 solamente)  

[Descodificador de voz de Windows Media Audio](http://www.microsoft.com/downloads/details.aspx?familyid=746d3440-5a6a-421e-9286-7b534a1dfe54)  
(KB954155)  
(Crítica)  
(Windows XP Service Pack 3 solamente)  

[Administrador de compresión de audio](http://www.microsoft.com/downloads/details.aspx?familyid=6ecc7129-8caa-4daf-a8e2-8f3536225fb3)  
(KB975025)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Reproductor de Microsoft Windows Media 6.4](http://www.microsoft.com/downloads/details.aspx?familyid=b2efe1ac-d8d7-41bb-b87d-fc5e22afef0f)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=9aacf890-afb4-46a7-a13f-dd9fe3c0ca4a)  
(Crítica)  

[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=dc166dc6-577f-4d8d-94df-dd963233dd85)  
(Crítica)  

[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=8799159d-df69-49f6-9db5-49147690ce0c)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=171d43d3-669c-4923-b266-e47591833c05)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.0 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=1bc56c26-1c7c-47e3-94f4-37af7e00392c)  
(KB953295)  
(Crítica)  
(Tablet PC Edition 2005 y Media Center Edition 2005 únicamente)  

[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=78ac8b97-8327-4ae1-8bb0-6cf227f3968f) (KB953297)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=d4a328b5-5470-46b0-86c7-cfe0e6a3ea01) (KB953300)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=491874d4-5eea-4545-9b7d-3861857c862e) (KB974417)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=e2acde20-a6d3-4135-b6eb-1214f743d474)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=2ae0bdd4-f8b2-420a-b1ac-d2cdaa87c828)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=9c5ab624-e37b-418a-a919-d8f652b15679)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=768fd74e-0a2f-4353-ac22-65d0d6321739)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=cece4c55-0756-4357-9d2d-6709e8426068)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 2 y Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=e997ea40-668e-40df-bd50-0ca53437b375) <sup>[1]</sup>
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Códec de voz de WMA de DirectShow](http://www.microsoft.com/downloads/details.aspx?familyid=c116ae9d-e416-4b7d-be75-4b4b2ebcc33a)  
(KB969878)  
(Crítica)  

[Descodificador de voz de Windows Media Audio](http://www.microsoft.com/downloads/details.aspx?familyid=4729de51-8fd8-46c6-b4ad-9c9f25202684)  
(KB954155)  
(Crítica)  

[Descodificador de voz de Windows Media Audio](http://www.microsoft.com/downloads/details.aspx?familyid=fe0d51b2-345e-4eb7-a036-d8c3f6a683d2) en SDK de Windows Media Format 9.5 x64 Edition  
(KB954155)  
(Crítica)  

[Descodificador de voz de Windows Media Audio](http://www.microsoft.com/downloads/details.aspx?familyid=a866a490-6d3a-4ecd-acf4-770312ba2fd6) en SDK de Windows Media Format 11  
(KB954155)  
(Crítica)  

[Administrador de compresión de audio](http://www.microsoft.com/downloads/details.aspx?familyid=46daf7c7-1cd3-4f47-9c7a-d5eb6ea7327b)  
(KB975025)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Reproductor de Microsoft Windows Media 6.4](http://www.microsoft.com/downloads/details.aspx?familyid=a9e7dfd8-7ba1-4f14-8e60-92ef00d91467)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=89a2cf2a-a7a2-4d4b-aa6f-24dde288d500)  
(Crítica)  

[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=bd54e595-25f2-4839-a838-2a0f809bde2b)  
(Crítica)  

[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=77b18fc2-e769-47c6-8e72-916716a49e58)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c08623bf-94bc-4c50-8c10-f50fb8448a0b)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=78ac8b97-8327-4ae1-8bb0-6cf227f3968f) (KB953297)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=d4a328b5-5470-46b0-86c7-cfe0e6a3ea01) (KB953300)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=491874d4-5eea-4545-9b7d-3861857c862e) (KB974417)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ad92503a-8c91-4d73-98b0-942d7961637d)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=819dd2d1-cad5-4784-9baf-185d8a76df5d)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ad29696d-4611-4a12-9dfa-74fa6866b759)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=270ec100-5ba1-4f8c-aa36-105d30ad57bf)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5459b7d4-1fab-4a04-ab9d-b8323505c1e2)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=17008892-7950-44c4-850d-002c8d73495f) <sup>[1]</sup>
(Importante)
</td>
</tr>
<tr>
<th colspan="13" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-050**](http://technet.microsoft.com/security/bulletin/ms09-050)
</td>
<td style="border:1px solid black;">
[**MS09-051**](http://technet.microsoft.com/security/bulletin/ms09-051)
</td>
<td style="border:1px solid black;">
[**MS09-052**](http://technet.microsoft.com/security/bulletin/ms09-052)
</td>
<td style="border:1px solid black;">
[**MS09-054**](http://technet.microsoft.com/security/bulletin/ms09-054)
</td>
<td style="border:1px solid black;">
[**MS09-055**](http://technet.microsoft.com/security/bulletin/ms09-055)
</td>
<td style="border:1px solid black;">
[**MS09-061**](http://technet.microsoft.com/security/bulletin/ms09-061)
</td>
<td style="border:1px solid black;">
[**MS09-062**](http://technet.microsoft.com/security/bulletin/ms09-062)
</td>
<td style="border:1px solid black;">
[**MS09-053**](http://technet.microsoft.com/security/bulletin/ms09-053)
</td>
<td style="border:1px solid black;">
[**MS09-056**](http://technet.microsoft.com/security/bulletin/ms09-056)
</td>
<td style="border:1px solid black;">
[**MS09-057**](http://technet.microsoft.com/security/bulletin/ms09-057)
</td>
<td style="border:1px solid black;">
[**MS09-058**](http://technet.microsoft.com/security/bulletin/ms09-058)
</td>
<td style="border:1px solid black;">
[**MS09-059**](http://technet.microsoft.com/security/bulletin/ms09-059)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
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
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Códec de voz de WMA de DirectShow](http://www.microsoft.com/downloads/details.aspx?familyid=4fe0dff5-04d9-4409-8d1d-52419537126b)  
(KB969878)  
(Crítica)  

[Descodificador de voz de Windows Media Audio](http://www.microsoft.com/downloads/details.aspx?familyid=00b3cb86-c9eb-4fbe-987e-2b0d94271d87)  
(KB954155)  
(Crítica)  

[Administrador de compresión de audio](http://www.microsoft.com/downloads/details.aspx?familyid=ab1803ff-2371-487f-a7b6-95747c46ba4e)  
(KB975025)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Reproductor de Microsoft Windows Media 6.4](http://www.microsoft.com/downloads/details.aspx?familyid=5f82d01c-573e-425e-b9f2-86a54f377b19)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=8101625d-ee93-46e5-aec2-3bdbf2d86472)  
(Crítica)  

[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=4647bcf1-69fb-4ad6-9e03-7bc22d8a914b)  
(Crítica)  

[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=9eae7eca-1a6f-4397-a6e2-7dda6b9d5276)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f3249c99-82e4-45dc-a254-28e647e822c8)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d1b4a58b-f0b1-4400-a6e6-0255b0513bd1) (KB953298)  
(Importante)  

[Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=d4a328b5-5470-46b0-86c7-cfe0e6a3ea01) (KB953300)  
(Importante)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=491874d4-5eea-4545-9b7d-3861857c862e) (KB974417)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=414466a4-39a0-476d-9a43-ae7674cbd6a0)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=48256ea3-b433-4e84-9019-22300069cfc1)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d170cef9-f5d2-4fcd-997b-e778ad5a6797)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=78072164-84d1-44da-8ede-2a9d212d47a9)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1e3f3842-f8fd-4969-a2cf-706db38d7580)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9dff4662-7771-4bdc-87ec-7899d79b3a55) <sup>[1]</sup>
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Códec de voz de WMA de DirectShow](http://www.microsoft.com/downloads/details.aspx?familyid=c116ae9d-e416-4b7d-be75-4b4b2ebcc33a)  
(KB969878)  
(Crítica)  

[Descodificador de voz de Windows Media Audio](http://www.microsoft.com/downloads/details.aspx?familyid=13ba4839-7fa9-4bbb-95f6-3fafb6c49f20)  
(KB954155)  
(Crítica)  

[Descodificador de voz de Windows Media Audio](http://www.microsoft.com/downloads/details.aspx?familyid=fe0d51b2-345e-4eb7-a036-d8c3f6a683d2) en SDK de Windows Media Format 9.5 x64 Edition  
(KB954155)  
(Crítica)  

[Administrador de compresión de audio](http://www.microsoft.com/downloads/details.aspx?familyid=46daf7c7-1cd3-4f47-9c7a-d5eb6ea7327b)  
(KB975025)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Reproductor de Microsoft Windows Media 6.4](http://www.microsoft.com/downloads/details.aspx?familyid=65e9036e-2e1b-40ff-a84b-c507107bcce8)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=2f966053-01eb-4a23-a9d5-71deac2498ea)  
(Crítica)  

[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=e7d77bd9-8317-42f3-9ad1-a0b8bfa65b53)  
(Crítica)  

[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=708a549d-11fd-43bf-a6e1-309e3205d59d)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1ad3f7b3-58d5-4507-ae20-a265e47cee9c)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=78ac8b97-8327-4ae1-8bb0-6cf227f3968f) (KB953297)  
(Importante)  

[Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=d4a328b5-5470-46b0-86c7-cfe0e6a3ea01) (KB953300)  
(Importante)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=491874d4-5eea-4545-9b7d-3861857c862e) (KB974417)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=eb95e8d9-6ef5-4526-99d2-507e50de049b)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=61bded07-201e-4815-ac1e-468bf907e063)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d170cef9-f5d2-4fcd-997b-e778ad5a6797)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8aa1f97d-ad53-4450-bb93-4a147dd10a87)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=95286b8d-4b53-4e6c-af59-e9e18fad3559)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8df7a2d9-2f97-4f18-84e8-415a1632cf09) <sup>[1]</sup>
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
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
[Microsoft Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=79a1a94d-3b47-47e9-9476-2f591c3f6a59)  
(Crítica)  
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=07e66c09-2cd7-47ba-bf87-d3da602184b4)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=575e75d9-e348-4fbb-9eaa-43240e4d715e)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=78ac8b97-8327-4ae1-8bb0-6cf227f3968f) (KB953297)  
(Importante)  

[Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=d4a328b5-5470-46b0-86c7-cfe0e6a3ea01) (KB953300)  
(Importante)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=491874d4-5eea-4545-9b7d-3861857c862e) (KB974417)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=a678ceb9-a37a-4c29-8bd1-f209922990e5)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=b99d4d9b-e0cc-4a8c-ad99-6a53958b37c8)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=2ede1eb9-7f5f-411d-bbc3-5db46d80e0bb)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=fb5678b9-5ef1-42db-902e-c9ea02880e0a)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=faef714b-5f46-47f2-bea7-881df05a1bc0)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=83c77015-7f96-4c0d-bd56-60aef90ea2f8) <sup>[1]</sup>
(Importante)
</td>
</tr>
<tr>
<th colspan="13" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-050**](http://technet.microsoft.com/security/bulletin/ms09-050)
</td>
<td style="border:1px solid black;">
[**MS09-051**](http://technet.microsoft.com/security/bulletin/ms09-051)
</td>
<td style="border:1px solid black;">
[**MS09-052**](http://technet.microsoft.com/security/bulletin/ms09-052)
</td>
<td style="border:1px solid black;">
[**MS09-054**](http://technet.microsoft.com/security/bulletin/ms09-054)
</td>
<td style="border:1px solid black;">
[**MS09-055**](http://technet.microsoft.com/security/bulletin/ms09-055)
</td>
<td style="border:1px solid black;">
[**MS09-061**](http://technet.microsoft.com/security/bulletin/ms09-061)
</td>
<td style="border:1px solid black;">
[**MS09-062**](http://technet.microsoft.com/security/bulletin/ms09-062)
</td>
<td style="border:1px solid black;">
[**MS09-053**](http://technet.microsoft.com/security/bulletin/ms09-053)
</td>
<td style="border:1px solid black;">
[**MS09-056**](http://technet.microsoft.com/security/bulletin/ms09-056)
</td>
<td style="border:1px solid black;">
[**MS09-057**](http://technet.microsoft.com/security/bulletin/ms09-057)
</td>
<td style="border:1px solid black;">
[**MS09-058**](http://technet.microsoft.com/security/bulletin/ms09-058)
</td>
<td style="border:1px solid black;">
[**MS09-059**](http://technet.microsoft.com/security/bulletin/ms09-059)
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
Windows Vista
</td>
<td style="border:1px solid black;">
[Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=29842c0c-8930-4b5f-83c6-1a718974b63f)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Descodificador de voz de Windows Media Audio](http://www.microsoft.com/downloads/details.aspx?familyid=f17ee0ea-f1e2-49f4-9f90-60296246ddfe)  
(KB954155)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=f6995616-2a84-4c26-9599-26f1314873ed)  
(Crítica)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=e8f6014f-950b-4e11-a105-51d298069f1a)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7313c03b-8844-4086-a0cc-43dfdb3ca48c)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=78ac8b97-8327-4ae1-8bb0-6cf227f3968f) (KB953297)  
(Crítica)  

[Microsoft .NET Framework 2.0](http://www.microsoft.com/downloads/details.aspx?familyid=6f99521e-86b3-4083-9132-e5ac06d40b63) (KB974468)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=3cf329c6-6d3d-41eb-bb72-8ba241df0882) (KB974292)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7438eb1e-6e86-4aa1-b1f4-f71a7699d233) (KB974467)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista y Windows Vista Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=19aa01f3-026d-4264-85f8-216d0597969b)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=bb96eb1c-66a2-4276-9773-eea22179bcd4)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8b5a9a95-9439-40c8-acef-000b919daa04)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista y Windows Vista Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=acf6f3e6-282e-4f05-9060-8d0ebb874b97)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista, Windows Vista Service Pack 1 y Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=04ae306b-0d0d-4767-ab54-cc11aec477ed)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista Service Pack 1
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=78ac8b97-8327-4ae1-8bb0-6cf227f3968f) (KB953297)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=30e5410d-0942-4964-9037-52330488efda) (KB974291)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=72fe9066-2397-439d-82fb-2b7f9d2bcce8) (KB974469)  
(Crítica)
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=78ac8b97-8327-4ae1-8bb0-6cf227f3968f) (KB953297)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=614a92ee-0512-4ccc-b6b8-32ebcec8e6a4) (KB974470)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=acf6f3e6-282e-4f05-9060-8d0ebb874b97)  
(Moderada)
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista x64 Edition
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=62ed5d0a-5ca6-4942-80c9-7808b14cb6b5)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Descodificador de voz de Windows Media Audio](http://www.microsoft.com/downloads/details.aspx?familyid=26905f12-92c7-4d45-99e7-227f03d2cb82)  
(KB954155)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=b3de5236-afdd-436e-8648-5382d564cc99)  
(Crítica)  
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=85978f28-5fc0-481b-9b03-2021c785889b)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7216bcb1-ff16-402b-ad1b-1500d46d0157)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=78ac8b97-8327-4ae1-8bb0-6cf227f3968f) (KB953297)  
(Crítica)  

[Microsoft .NET Framework 2.0](http://www.microsoft.com/downloads/details.aspx?familyid=6f99521e-86b3-4083-9132-e5ac06d40b63) (KB974468)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 1 y Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=3cf329c6-6d3d-41eb-bb72-8ba241df0882) (KB974292)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7438eb1e-6e86-4aa1-b1f4-f71a7699d233) (KB974467)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=8f5f0c1d-1dd6-47fa-aef2-d3c96c8fc06e)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=bce096c8-833b-45c8-99cd-1280f0744f2f)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4a60f789-1a4a-49a8-8d13-fda989ed40be)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition y Windows Vista x64 Edition Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=13a3fe0b-e300-4568-aa08-d586ab8d5434)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition, Windows Vista x64 Edition Service Pack 1 y Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=58c995ca-f308-4e07-8e60-2e542384d95d)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 1
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=78ac8b97-8327-4ae1-8bb0-6cf227f3968f) (KB953297)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=30e5410d-0942-4964-9037-52330488efda) (KB974291)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=72fe9066-2397-439d-82fb-2b7f9d2bcce8) (KB974469)  
(Crítica)
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=78ac8b97-8327-4ae1-8bb0-6cf227f3968f) (KB953297)  
(Crítica)  

[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=614a92ee-0512-4ccc-b6b8-32ebcec8e6a4) (KB974470)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=13a3fe0b-e300-4568-aa08-d586ab8d5434)  
(Moderada)
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
</tr>
<tr>
<th colspan="13" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-050**](http://technet.microsoft.com/security/bulletin/ms09-050)
</td>
<td style="border:1px solid black;">
[**MS09-051**](http://technet.microsoft.com/security/bulletin/ms09-051)
</td>
<td style="border:1px solid black;">
[**MS09-052**](http://technet.microsoft.com/security/bulletin/ms09-052)
</td>
<td style="border:1px solid black;">
[**MS09-054**](http://technet.microsoft.com/security/bulletin/ms09-054)
</td>
<td style="border:1px solid black;">
[**MS09-055**](http://technet.microsoft.com/security/bulletin/ms09-055)
</td>
<td style="border:1px solid black;">
[**MS09-061**](http://technet.microsoft.com/security/bulletin/ms09-061)
</td>
<td style="border:1px solid black;">
[**MS09-062**](http://technet.microsoft.com/security/bulletin/ms09-062)
</td>
<td style="border:1px solid black;">
[**MS09-053**](http://technet.microsoft.com/security/bulletin/ms09-053)
</td>
<td style="border:1px solid black;">
[**MS09-056**](http://technet.microsoft.com/security/bulletin/ms09-056)
</td>
<td style="border:1px solid black;">
[**MS09-057**](http://technet.microsoft.com/security/bulletin/ms09-057)
</td>
<td style="border:1px solid black;">
[**MS09-058**](http://technet.microsoft.com/security/bulletin/ms09-058)
</td>
<td style="border:1px solid black;">
[**MS09-059**](http://technet.microsoft.com/security/bulletin/ms09-059)
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
Ninguna
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Baja**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
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
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ff6bfcf3-76c9-4c45-b57d-22f94458dd6e) \*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Descodificador de voz de Windows Media Audio](http://www.microsoft.com/downloads/details.aspx?familyid=2eaa9857-a147-4f31-9bf4-b9e2cf4c15c3) \*\*  
(KB954155)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=72dd580e-eb53-41da-a5c0-a392ad388bfc) \*\*  
(Crítica)  

[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=1baf7e96-ba3e-47e7-8ea3-eb092e653a39) \*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=51eb56fa-8204-45f3-86d7-6d03a2c8d78d) \*\*  
(Baja)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=78ac8b97-8327-4ae1-8bb0-6cf227f3968f) \*\*  
(KB953297)  
(Importante)  

[Microsoft .NET Framework 2.0 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=30e5410d-0942-4964-9037-52330488efda) \*\*  
(KB974291)  
(Importante)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=72fe9066-2397-439d-82fb-2b7f9d2bcce8) \*\*  
(KB974469)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=fd1694af-8873-43aa-9243-91f7cde452b7) \*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d9c5039f-d0cf-4d84-850f-f2f7701dcb79) \*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f9b487af-fe73-42a8-b240-d59c4321f95b) \*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=71aec6f6-a36b-465e-8885-b094dfd30423) \*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits y Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f2f617c2-f149-4e9b-bfdd-08ed0f3f99db) \*  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=78ac8b97-8327-4ae1-8bb0-6cf227f3968f) \*\*  
(KB953297)  
(Importante)  

[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=614a92ee-0512-4ccc-b6b8-32ebcec8e6a4) \*\*  
(KB974470)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=71aec6f6-a36b-465e-8885-b094dfd30423) \*  
(Moderada)
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=aff6f9c7-4a72-48f2-b750-204d796c7daa) \*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Descodificador de voz de Windows Media Audio](http://www.microsoft.com/downloads/details.aspx?familyid=70aabba3-53d6-4b52-be83-6d3f3869ecbd) \*\*  
(KB954155)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=0111d741-bda4-4a50-a12b-d3337ff4441d) \*\*  
(Crítica)  

[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=7a4b755b-7fa0-43aa-8862-c1d0c7d94c2c) \*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=131b047a-ae93-4a99-83e5-71d5a79e96ea) \*\*  
(Baja)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=78ac8b97-8327-4ae1-8bb0-6cf227f3968f) \*\*  
(KB953297)  
(Importante)  

[Microsoft .NET Framework 2.0 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=30e5410d-0942-4964-9037-52330488efda) \*\*  
(KB974291)  
(Importante)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=72fe9066-2397-439d-82fb-2b7f9d2bcce8) \*\*  
(KB974469)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=41bc4cdb-273a-4a6e-80d9-c8ce20e32da9) \*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=db969ddc-708e-42b7-9956-6c27bf346bbb) \*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=0d8a2a3e-d7d4-47fb-8364-16fce28e4d38) \*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=88f4189f-71fe-404a-869e-3f76692acf94) \*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 y Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=deb84cb8-2ba3-47e3-9185-2bbc5b0a7e18) \*  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=78ac8b97-8327-4ae1-8bb0-6cf227f3968f) \*\*  
(KB953297)  
(Importante)  

[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=614a92ee-0512-4ccc-b6b8-32ebcec8e6a4) \*\*  
(KB974470)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=88f4189f-71fe-404a-869e-3f76692acf94) \*  
(Moderada)
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7b70108b-7f59-4898-ab4e-76be990de878)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=e81f30b7-ef05-4488-b62a-d330e17129cf)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3d16c5bf-ee5c-4220-9755-5cb92eac2aae)  
(Baja)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=78ac8b97-8327-4ae1-8bb0-6cf227f3968f)  
(KB953297)  
(Importante)  

[Microsoft .NET Framework 2.0 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=30e5410d-0942-4964-9037-52330488efda)  
(KB974291)  
(Importante)  

[Microsoft .NET Framework 2.0 Service Pack 2 y Microsoft .NET Framework 3.5 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=72fe9066-2397-439d-82fb-2b7f9d2bcce8)  
(KB974469)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=a4f42085-1cb9-4b8d-a931-85be71fdf06d)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a221451a-cb4e-4a43-a225-4b1e86e87525)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8962f0b6-f346-4e88-9d83-4d15b699dd9d)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=3e0f0b1c-ca5d-43fc-9770-73396a5f191c)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium y Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4aac0e3e-9b49-4a4a-ab17-707ff03b4d9b)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 1.1 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=78ac8b97-8327-4ae1-8bb0-6cf227f3968f)  
(KB953297)  
(Importante)  

[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=614a92ee-0512-4ccc-b6b8-32ebcec8e6a4)  
(KB974470)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3e0f0b1c-ca5d-43fc-9770-73396a5f191c)  
(Moderada)
</td>
<td style="border:1px solid black;">
Igual que el anterior
</td>
</tr>
<tr>
<th colspan="13" style="border:1px solid black;">
Windows 7
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-050**](http://technet.microsoft.com/security/bulletin/ms09-050)
</td>
<td style="border:1px solid black;">
[**MS09-051**](http://technet.microsoft.com/security/bulletin/ms09-051)
</td>
<td style="border:1px solid black;">
[**MS09-052**](http://technet.microsoft.com/security/bulletin/ms09-052)
</td>
<td style="border:1px solid black;">
[**MS09-054**](http://technet.microsoft.com/security/bulletin/ms09-054)
</td>
<td style="border:1px solid black;">
[**MS09-055**](http://technet.microsoft.com/security/bulletin/ms09-055)
</td>
<td style="border:1px solid black;">
[**MS09-061**](http://technet.microsoft.com/security/bulletin/ms09-061)
</td>
<td style="border:1px solid black;">
[**MS09-062**](http://technet.microsoft.com/security/bulletin/ms09-062)
</td>
<td style="border:1px solid black;">
[**MS09-053**](http://technet.microsoft.com/security/bulletin/ms09-053)
</td>
<td style="border:1px solid black;">
[**MS09-056**](http://technet.microsoft.com/security/bulletin/ms09-056)
</td>
<td style="border:1px solid black;">
[**MS09-057**](http://technet.microsoft.com/security/bulletin/ms09-057)
</td>
<td style="border:1px solid black;">
[**MS09-058**](http://technet.microsoft.com/security/bulletin/ms09-058)
</td>
<td style="border:1px solid black;">
[**MS09-059**](http://technet.microsoft.com/security/bulletin/ms09-059)
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
Ninguna
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
Ninguna
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
<td style="border:1px solid black;">
[**Importante**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits
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
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=89d1fb78-68cd-48dd-afc2-15a79ebe9fde)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=b64bcc14-38a7-45b9-8f85-acc573777506)  
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
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=ad6f06d5-27db-445d-a8b2-c42adc90afc0)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=35b85783-90df-4f67-a3cb-02351432133e)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64
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
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=10d9f7ac-65f4-437c-91cc-171632c69b0e)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=809e29f3-ec68-4a2b-b04e-11759dd16001)  
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
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=70cd0270-77e9-492a-82d9-798364640c10)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=97010f2c-6c10-4fda-84fd-6c8749968db5)  
(Importante)
</td>
</tr>
<tr>
<th colspan="13" style="border:1px solid black;">
Windows Server 2008 R2
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-050**](http://technet.microsoft.com/security/bulletin/ms09-050)
</td>
<td style="border:1px solid black;">
[**MS09-051**](http://technet.microsoft.com/security/bulletin/ms09-051)
</td>
<td style="border:1px solid black;">
[**MS09-052**](http://technet.microsoft.com/security/bulletin/ms09-052)
</td>
<td style="border:1px solid black;">
[**MS09-054**](http://technet.microsoft.com/security/bulletin/ms09-054)
</td>
<td style="border:1px solid black;">
[**MS09-055**](http://technet.microsoft.com/security/bulletin/ms09-055)
</td>
<td style="border:1px solid black;">
[**MS09-061**](http://technet.microsoft.com/security/bulletin/ms09-061)
</td>
<td style="border:1px solid black;">
[**MS09-062**](http://technet.microsoft.com/security/bulletin/ms09-062)
</td>
<td style="border:1px solid black;">
[**MS09-053**](http://technet.microsoft.com/security/bulletin/ms09-053)
</td>
<td style="border:1px solid black;">
[**MS09-056**](http://technet.microsoft.com/security/bulletin/ms09-056)
</td>
<td style="border:1px solid black;">
[**MS09-057**](http://technet.microsoft.com/security/bulletin/ms09-057)
</td>
<td style="border:1px solid black;">
[**MS09-058**](http://technet.microsoft.com/security/bulletin/ms09-058)
</td>
<td style="border:1px solid black;">
[**MS09-059**](http://technet.microsoft.com/security/bulletin/ms09-059)
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
Ninguna
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
<td style="border:1px solid black;">
[**Baja**](http://technet.microsoft.com/security/bulletin/rating)
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
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=f50307d6-7869-4996-9ff7-23f87d08994b) \*\*  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=bcd2b944-6852-48f2-820b-cce7d195e391) \*\*  
(Baja)
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
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=ce78c019-ec08-4ec6-abec-334f5ec5cb76) \*  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=597ac3a7-e02d-49a5-9b8e-d097e867acea) \*  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium
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
[Windows Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=9b6a28ae-b3f2-42b0-8209-e3950ec37abb)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=85e76e55-3766-4ffe-9a18-8655de935b7c)  
(Baja)
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
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=6442a77a-3c0d-4beb-b2d2-2885376c2135)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=abc94857-37d8-4bb8-ad9e-46e687fca40e)  
(Importante)
</td>
</tr>
</table>
 
**Notas para Windows Server 2008 y Windows Server 2008 R2**

**\*La instalación de Server Core está afectada.** Esta actualización se aplica, con la misma clasificación de gravedad, a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, independientemente de si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de MSDN [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx) y [Server Core para Windows Server 2008 R2](http://msdn.microsoft.com/en-us/library/ee391631(vs.85).aspx) . Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparación de las opciones de instalación Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx) .

**\*\*La instalación de Server Core no está afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de MSDN [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx) y [Server Core para Windows Server 2008 R2](http://msdn.microsoft.com/en-us/library/ee391631(vs.85).aspx) . Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparación de las opciones de instalación Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx) .

**Nota para MS09-061**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado** , para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

**Notas para MS09-062**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado** , para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

**Nota para MS09-059**

\[ 1 \]Este sistema operativo sólo está afectado cuando se ha instalado KB968389, Protección ampliada para la autenticación (consulte el [documento informativo sobre seguridad de Microsoft 973811](http://technet.microsoft.com/security/advisory/973811) ). Para obtener más información, consulte la entrada de Preguntas más frecuentes (P+F) relacionadas con esta actualización de seguridad en [MS09-059](http://technet.microsoft.com/security/bulletin/ms09-059) .

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
[**MS09-060**](http://technet.microsoft.com/security/bulletin/ms09-060)
</td>
<td style="border:1px solid black;">
[**MS09-062**](http://technet.microsoft.com/security/bulletin/ms09-062)
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
Microsoft Office XP
</td>
<td style="border:1px solid black;">
[Microsoft Outlook 2002 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=04878c2c-eb97-426f-be08-89036a6799db)  
(KB973702)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=b4ac7fbe-dd19-4940-a576-89a6b7ed602d) <sup>[2]</sup>
(KB974811)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2003
</td>
<td style="border:1px solid black;">
[Microsoft Office Outlook 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=79e2b2e8-d5e8-4014-b489-720af2b5083d)  
(KB973705)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=48752ab4-5928-476d-a8bc-e998d188b1f7) <sup>[3]</sup>
(KB972580)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
2007 Microsoft Office System
</td>
<td style="border:1px solid black;">
[Microsoft Office Outlook 2007 Service Pack 1 y Microsoft Office Outlook 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d39234a3-c62c-44ba-a626-3179a183ca09)  
(KB972363)  
(Crítica)
</td>
<td style="border:1px solid black;">
[2007 Microsoft Office System Service Pack 1 y 2007 Microsoft Office System Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=98d7c4ab-f8ca-4806-a609-453fb29b02ec) <sup>[4]</sup>  
(KB972581)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Otro software de Microsoft Office
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-060**](http://technet.microsoft.com/security/bulletin/ms09-060)
</td>
<td style="border:1px solid black;">
[**MS09-062**](http://technet.microsoft.com/security/bulletin/ms09-062)
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
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Visio
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Visio 2002 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=920ee70b-c5c1-47b5-8f33-938ffe14eea4)  
(KB975365)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Visio Viewer
</td>
<td style="border:1px solid black;">
Microsoft Visio 2002 Viewer <sup>[1]</sup>
(Crítica)  

Microsoft Office Visio 2003 Viewer <sup>[1]</sup>
(Crítica)  

[Microsoft Office Visio Viewer 2007 Service Pack 1 y Microsoft Office Visio Viewer 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d20004c5-dd01-459e-8120-5f127e20c085)  
(KB973709)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office Visio Viewer 2007 Service Pack 1 y Microsoft Office Visio Viewer 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=98d7c4ab-f8ca-4806-a609-453fb29b02ec) <sup>[4]</sup>  
(KB972581)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office Project
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office Project 2002 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b4ac7fbe-dd19-4940-a576-89a6b7ed602d) <sup>[2]</sup>
(KB974811)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Word Viewer, Microsoft Office Excel Viewer y Microsoft PowerPoint Viewer
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Word Viewer 2003 Service Pack 3 y Microsoft Office Excel Viewer 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=48752ab4-5928-476d-a8bc-e998d188b1f7) <sup>[3]</sup>
(KB972580)  
(Importante)  

[Microsoft Office Excel Viewer Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=98d7c4ab-f8ca-4806-a609-453fb29b02ec) <sup>[4]</sup>  
(KB972581)  
(Importante)  

[PowerPoint Viewer 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=98d7c4ab-f8ca-4806-a609-453fb29b02ec) <sup>[4]</sup>  
(KB972581)  
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
[Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 1 y Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=98d7c4ab-f8ca-4806-a609-453fb29b02ec) <sup>[4]</sup>  
(KB972581)  
Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Works
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Works 8.5](http://www.microsoft.com/downloads/details.aspx?familyid=6f96de9a-62d8-428f-9567-51d55c129be6)  
(KB973636)  
(Importante)
</td>
</tr>
</table>
 
**Notas para MS09-060**

<sup>[1]</sup> Microsoft recomienda que los usuarios de Microsoft Visio Viewer 2002 y Microsoft Visio Viewer 2003 se actualicen a Microsoft Office Visio Viewer 2007 Service Pack 2.

**Notas para MS09-062**

<sup>[2]</sup> Estas actualizaciones son idénticas.

<sup>[3]</sup> Estas actualizaciones son idénticas.

<sup>[4]</sup> Estas actualizaciones son idénticas.

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado** , para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

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
[**MS09-062**](http://technet.microsoft.com/security/bulletin/ms09-062)
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
SQL Server 2000 Reporting Services Service Pack 2
</td>
<td style="border:1px solid black;">
Actualización de RDA  
No aplicable  

Actualización de QFE:  
[SQL Server 2000 Reporting Services Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=33554f96-5af7-4683-a537-9db293b67b8d)  
(KB970899)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
SQL Server 2005 Service Pack 2
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2005 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d971a262-1dfb-498c-a4f3-59fdc1b85d23) <sup>[1]</sup>
(KB970895)  
(Crítica)  

Actualización de QFE:  
[SQL Server 2005 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=76d3d653-e9a0-48bc-afae-d3553f7b9235) <sup>[1]</sup>
(KB970896)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
SQL Server 2005 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2005 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d971a262-1dfb-498c-a4f3-59fdc1b85d23) <sup>[1]</sup>
(KB970895)  
(Crítica)  

Actualización de QFE:  
[SQL Server 2005 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=76d3d653-e9a0-48bc-afae-d3553f7b9235) <sup>[1]</sup>
(KB970896)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
SQL Server 2005 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2005 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d971a262-1dfb-498c-a4f3-59fdc1b85d23) <sup>[1]</sup>
(KB970895)  
(Crítica)  

Actualización de QFE:  
[SQL Server 2005 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=76d3d653-e9a0-48bc-afae-d3553f7b9235) <sup>[1]</sup>
(KB970896)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
SQL Server 2005 Service Pack 3
</td>
<td style="border:1px solid black;">
Actualización de RDA  
[SQL Server 2005 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=0d878f4b-71e8-4170-9a14-1bce684811ce) <sup>[2]</sup>
(KB970892)  
(Crítica)  

Actualización de QFE:  
[SQL Server 2005 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=e6f307c1-8b21-406e-9c6f-b1a3a1e9a98f) <sup>[2]</sup>
(KB970894)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
SQL Server 2005 x64 Edition Service Pack 3
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2005 x64 Edition Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=0d878f4b-71e8-4170-9a14-1bce684811ce) <sup>[2]</sup>
(KB970892)  
(Crítica)  

Actualización de QFE:  
[SQL Server 2005 x64 Edition Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=e6f307c1-8b21-406e-9c6f-b1a3a1e9a98f) <sup>[2]</sup>
(KB970894)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
SQL Server 2005 para sistemas con Itanium Service Pack 3
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[SQL Server 2005 para sistemas con Itanium Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=0d878f4b-71e8-4170-9a14-1bce684811ce) <sup>[2]</sup>
(KB970892)  
(Crítica)  

Actualización de QFE:  
[SQL Server 2005 para sistemas con Itanium Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=e6f307c1-8b21-406e-9c6f-b1a3a1e9a98f) <sup>[2]</sup>
(KB970894)  
(Crítica)
</td>
</tr>
</table>
 
**Nota para MS09-062**

\[ <sup>1</sup> \]Los clientes de SQL Server 2005 Service Pack 2 con una dependencia de Reporting Services SharePoint también deben instalar el [complemento de Microsoft SQL Server 2005 Reporting Services para Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=%20f4d4d0ae-e5d4-4ed1-8d78-7137578161ce&displaylang=en) del Centro de descarga de Microsoft.

\[ <sup>2</sup> \]Los clientes de SQL Server 2005 Service Pack 3 con una dependencia de Reporting Services SharePoint también deben instalar el [complemento de Microsoft SQL Server 2005 Reporting Services para Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=%20648766ac-2a35-4238-a3f4-c26d7077f2a9&displaylang=en) del Centro de descarga de Microsoft.

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado** , para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

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
[**MS09-061**](http://technet.microsoft.com/security/bulletin/ms09-061)
</td>
<td style="border:1px solid black;">
[**MS09-062**](http://technet.microsoft.com/security/bulletin/ms09-062)
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
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Silverlight
</td>
<td style="border:1px solid black;">
[Microsoft Silverlight 2](http://www.microsoft.com/silverlight/get-started/install/default.aspx) <sup>[1]</sup> Cuando instalado en Mac  
(KB970363)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Silverlight
</td>
<td style="border:1px solid black;">
[Microsoft Silverlight 2](http://www.microsoft.com/silverlight/get-started/install/default.aspx) <sup>[1]</sup> Cuando instalado en todas versiones de los clientes de Microsoft Windows  
(KB970363)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Silverlight
</td>
<td style="border:1px solid black;">
[Microsoft Silverlight 2](http://www.microsoft.com/silverlight/get-started/install/default.aspx) <sup>[1]</sup> Cuando instalado en todas versiones de los servidores de Microsoft Windows  
(KB970363)  
(Moderada)
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
[**MS09-061**](http://technet.microsoft.com/security/bulletin/ms09-061)
</td>
<td style="border:1px solid black;">
[**MS09-062**](http://technet.microsoft.com/security/bulletin/ms09-062)
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
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Visual Studio .NET 2003 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Visual Studio .NET 2003 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=9e3b52d3-b211-4d62-891c-ae8f2e4ffc6c)  
(KB971022)  
(Sin clasificación de gravedad <sup>[2]</sup> )
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Visual Studio 2005 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Visual Studio 2005 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=e186aeed-e9d7-4a02-84b3-bbed116ca060)  
(KB971023)  
(Sin clasificación de gravedad <sup>[2]</sup> )
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Visual Studio 2008
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Visual Studio 2008](http://www.microsoft.com/downloads/details.aspx?familyid=4fa10c93-ce20-43df-a725-ef4c77353747)  
(KB972221)  
(Sin clasificación de gravedad <sup>[2]</sup> )
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
[Microsoft Visual Studio 2008 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b904dee8-8a26-43f8-8ca9-86ad12cfdb52)  
(KB972222)  
(Sin clasificación de gravedad <sup>[2]</sup> )
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Visual FoxPro 8.0 Service Pack 1 cuando está instalado en Microsoft Windows 2000 Service Pack 4  
(KB971104)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Visual FoxPro 8.0 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=e5d0d515-4b36-4025-bc6f-1c5cdf09e1af)  
cuando está instalado en Microsoft Windows 2000 Service Pack 4  
(KB971104)  
(Sin clasificación de gravedad <sup>[2]</sup> )
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Visual FoxPro 9.0 Service Pack 2 cuando está instalado en Microsoft Windows 2000 Service Pack 4  
(KB971105)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Visual FoxPro 9.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2a930f56-59ac-49a6-830f-bfae7c540ec7)  
cuando está instalado en Microsoft Windows 2000 Service Pack 4  
(KB971105)  
(Sin clasificación de gravedad <sup>[2]</sup> )
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Report Viewer
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-061**](http://technet.microsoft.com/security/bulletin/ms09-061)
</td>
<td style="border:1px solid black;">
[**MS09-062**](http://technet.microsoft.com/security/bulletin/ms09-062)
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
[**Crítica**](http://technet.microsoft.com/security/bulletin/rating)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Paquete redistribuible de Microsoft Report Viewer 2005 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Paquete redistribuible de Microsoft Report Viewer 2005 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=0dfaf300-2b53-4678-a779-0d805ddfe538)  
(KB971117)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Paquete redistribuible de Microsoft Report Viewer 2008
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Paquete redistribuible de Microsoft Report Viewer 2008](http://www.microsoft.com/downloads/details.aspx?familyid=42ed040f-cf94-4754-b0b3-c8016fbcbe22)  
(KB971118)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Paquete redistribuible de Microsoft Report Viewer 2008 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Paquete redistribuible de Microsoft Report Viewer 2008 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=6aaa74bd-a46e-4478-b4e1-2063d18d2d42)  
(KB971119)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Platform SDK redistribuible: GDI+.
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Platform SDK redistribuible: GDI+](http://www.microsoft.com/downloads/details.aspx?familyid=6a63ab9c-df12-4d41-933c-be590feaa05a)  
(KB975337)  
(Sin clasificación de gravedad <sup>[2]</sup> )
</td>
</tr>
</table>
 
**Notas para MS09-061**

<sup>[1]</sup> Con esta descarga, se actualiza Microsoft Silverlight 2 a Microsoft Silverlight 3, que corrige la vulnerabilidad descrita en el boletín.

**\*\*La instalación de Server Core no está afectada.** Las vulnerabilidades corregidas por esta actualización no afectan a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de MSDN [Server Core](http://msdn.microsoft.com/en-us/library/ms723891(vs.85).aspx) y [Server Core para Windows Server 2008 R2](http://msdn.microsoft.com/en-us/library/ee391631(vs.85).aspx) . Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparación de las opciones de instalación Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx) .

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado** , para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

**Notas para MS09-062**

<sup>[2]</sup> Las clasificaciones de gravedad no se aplican esta actualización porque Microsoft no ha detectado ninguna vía de ataque relacionada con las vulnerabilidades descritas en este boletín específico de este software. No obstante, esta actualización de seguridad se ofrece a los desarrolladores que usan este software para que puedan publicar su propia versión actualizada de sus aplicaciones.

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado** , para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

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
Microsoft Forefront Security
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS09-062**](http://technet.microsoft.com/security/bulletin/ms09-062)
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
Microsoft Forefront Client Security 1.0
</td>
<td style="border:1px solid black;">
[Microsoft Forefront Client Security 1.0](http://www.microsoft.com/downloads/details.aspx?familyid=c0ce624c-8df3-4223-8a7a-5cba4ac334a8)  
cuando está instalado en Microsoft Windows 2000 Service Pack 4  
(KB975962)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS09-062**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado** , para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://go.microsoft.com/fwlink/?linkid=69903) . [TechNet Security Center](http://go.microsoft.com/fwlink/?linkid=21171) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://go.microsoft.com/fwlink/?linkid=85102) , donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130) . También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129) . Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155) . El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como " MS07-036 " ), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900) .

**Nota** A partir del 1 de agosto de 2009, Microsoft dejará de ofrecer soporte técnico a Office Update y Office Update Inventory Tool. Para seguir obteniendo las actualizaciones más recientes para los productos de Microsoft, use [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) . Para obtener más información, vea [Acerca de Microsoft Office Update: Preguntas más frecuentes](http://office.microsoft.com/en-us/downloads/fx010402221033.aspx) .

**Consejos para la detección y la implementación**

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747) .

**Microsoft Baseline Security Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, visite [Microsoft Baseline Security Analyzer](http://go.microsoft.com/fwlink/?linkid=21134) .

**Windows Server Update Services**

Windows Server Update Services (WSUS) permite a los administradores implementar con rapidez y fiabilidad las actualizaciones críticas y de seguridad más recientes en sistemas operativos Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://go.microsoft.com/fwlink/?linkid=50120) .

**Systems Management Server**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales. La siguiente versión de SMS, System Center Configuration Manager 2007, ya está disponible; consulte también [System Center Configuration Manager 2007](http://technet.microsoft.com/en-us/library/bb735860.aspx) . Para obtener más información acerca de cómo pueden utilizar los administradores SMS 2003 para implementar actualizaciones de seguridad, visite [Administración de revisiones de seguridad de SMS 2003](http://go.microsoft.com/fwlink/?linkid=22939) (en inglés). Los usuarios de SMS 2.0 también pueden usar Security Update Inventory Tool (SUIT) como ayuda para implementar las actualizaciones de seguridad. Para obtener información acerca de SMS, visite [Microsoft Systems Management Server](http://go.microsoft.com/fwlink/?linkid=21158) .

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341) . Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=33387) y en [SMS 2.0 Administration Feature Pack](http://go.microsoft.com/fwlink/?linkid=21161) ) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet2.microsoft.com/windowsvista/en/library/4279e239-37a4-44aa-aec5-4e70fe39f9de1033.mspx?mfr=true) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en) .

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Microsoft Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad de alta prioridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Artículo 894199 de Microsoft Knowledge Base](http://support.microsoft.com/kb/894199) : Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones de meses anteriores para Windows Server Update Services](http://technet.microsoft.com/en-us/wsus/bb456965.aspx) . Muestra todas las actualizaciones nuevas, revisadas y publicadas de nuevo para los productos de Microsoft que no sean Microsoft Windows.

#### Microsoft Active Protections Program (MAPP)

Para mejorar las protecciones de seguridad de los clientes, Microsoft proporciona información acerca de las vulnerabilidades a los principales proveedores de software de seguridad antes de cada publicación mensual de las actualizaciones de seguridad. De este modo, los proveedores de software de seguridad pueden usar esta información para proporcionar protecciones actualizadas a los clientes mediante su software o dispositivos de seguridad, como, por ejemplo, antivirus, sistemas de detección de intrusiones de red o sistemas de prevención de intrusiones de host. Para determinar si hay disponibles protecciones activas en los proveedores de software de seguridad, visite los sitios web de protecciones activas que proporcionan los asociados, enumeradas en [Asociados de Microsoft Active Protections Program (MAPP)](http://www.microsoft.com/security/msrc/mapp/partners.mspx) .

#### Estrategias de seguridad y comunidad

**Estrategias de administración de actualizaciones**

En [Orientación de seguridad para la administración de actualizaciones](http://go.microsoft.com/fwlink/?linkid=21168) (en inglés), se proporciona información adicional acerca de los procedimientos recomendados de Microsoft para aplicar actualizaciones de seguridad.

**Obtención de otras actualizaciones de seguridad**

Las actualizaciones para otros problemas de seguridad están disponibles en las ubicaciones siguientes:

-   En el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129) hay actualizaciones de seguridad disponibles. Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.
-   Las actualizaciones para plataformas de usuarios están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) .
-   Puede obtener las actualizaciones de seguridad ofrecidas este mes en Windows Update, en los archivos de imagen de CD ISO del centro de descarga de versiones de seguridad y críticas. Para obtener más información, vea el [artículo 913086 de Microsoft Knowledge Base](http://support.microsoft.com/kb/913086) .

**Comunidad de seguridad para profesionales de tecnologías de la información**

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [IT Pro Security Community](http://go.microsoft.com/fwlink/?linkid=21164) (en inglés).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

-   [Matthieu Suiche](http://www.msuiche.net/) , de [Netherlands Forensics Institute](http://www.nederlandsforensischinstituut.nl/) , por informar de un problema descrito en MS09-050
-   Ivan Fratric, de [Zero Day Initiative](http://www.zerodayinitiative.com/) , y Jun Xie, de [McAfee Avert Labs](http://www.avertlabs.com/) , por informar de un problema descrito en MS09-051
-   Vinay Anantharaman, de [Adobe Systems, Inc.](http://www.adobe.com/) , por informar de un problema descrito en MS09-051
-   Yamata Li, de [Palo Alto Networks](http://www.paloaltonetworks.com/) , por informar de un problema descrito en MS09-052
-   Skylined, de [Google Inc.](http://www.google.com/) , por informar de un problema descrito en MS09-054
-   Mark Dowd, de [IBM ISS X-Force](http://www.iss.net/) , por informar de un problema descrito en MS09-054
-   [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/) , por informar de un problema descrito en MS09-054
-   Sam Thomas, de eshu.co.uk, en colaboración con [TippingPoint](http://www.tippingpoint.com/) y [Zero Day Initiative](http://www.zerodayinitiative.com/) , por informar de un problema descrito en MS09-054
-   Ian Wright y Jean-Luc Giraud, de [Citrix](http://www.citrix.com/) , por su colaboración en un problema descrito en MS09-056
-   Dan Kaminsky, de [IOActive](http://www.ioactive.com/) , por informar de dos problemas descritos en MS09-056
-   Yamata Li, de [Palo Alto Networks](http://www.paloaltonetworks.com/) , por informar de un problema descrito en MS09-057
-   Tavis Ormandy y Neel Mehta, de [Google Inc.](http://www.google.com/) , por informar de dos problemas descritos en MS09-058
-   [NSFocus Security Team](http://www.nsfocus.com/) , por informar de un problema descrito en MS09-058
-   David Dewey, de [IBM ISS X-Force](http://www.iss.net/) , por informar de un problema descrito en MS09-060
-   Ryan Smith, de [VeriSign iDefense Labs](http://labs.idefense.com/) , por informar de dos problemas descritos en MS09-060
-   [Pavel Minaev](http://int19h.org/) , por informar de un problema describió en MS09-061
-   Jeroen Frijters, de [Sumatra](http://www.sumatra.nl/) , por informar de un problema descrito en MS09-061.
-   Yamata Li, de [Palo Alto Networks](http://www.paloaltonetworks.com/) , por informar de un problema descrito en MS09-062
-   Thomas Garnier, de [SkyRecon](http://www.skyrecon.com/) , por informar de un problema descrito en MS09-062
-   Wushi, de [VeriSign iDefense Labs](http://labs.idefense.com/) , por informar de un problema descrito en MS09-062
-   Ivan Fratric, de [Zero Day Initiative](http://www.zerodayinitiative.com/) , por informar de un problema descrito en MS09-062
-   Tavis Ormandy, de [Google Inc.](http://www.google.com/) , por informar de dos problemas descritos en MS09-062
-   Carlo Di Dato (también conocido como shinnai), por informar de un problema descrito en MS09-062
-   Marsu Pilami, de [VeriSign iDefense Labs](http://labs.idefense.com/) , por informar de un problema descrito en MS09-062
-   Carsten H. Eiram, de [Secunia](http://secunia.com/) , por informar de un problema descrito en MS09-062

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742) .
-   Los clientes de Estados Unidos y Canadá pueden recibir soporte técnico del [soporte de seguridad](http://go.microsoft.com/fwlink/?linkid=21131) o en el teléfono 1-866-PCSAFETY. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de las opciones de asistencia disponibles, visite [Ayuda y soporte técnico de Microsoft](http://support.microsoft.com/) .
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra " tal cual " , sin garantía de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (13 de octubre de 2009): Publicación del resumen del boletín.
-   V1.1 (14 de octubre de 2009): Se ha corregido el vínculo de descarga para Windows XP x64 Edition Service Pack 2 para MS09-055.
-   V1.2 (18 de octubre de 2009): Se ha revisado el resumen ejecutivo de MS09-054 para proporcionar instrucciones a los usuarios de Firefox.
-   V2.0 (28 de octubre de 2009): Se han agregado Microsoft Office Visio Viewer 2007, Microsoft Office Visio Viewer 2007 Service Pack 1 y Microsoft Office Visio Viewer 2007 Service Pack 2 como software afectado para MS09-062 y se han agregado notas para MS09-062 para los clientes de SQL Server 2005 con una dependencia de Reporting Services SharePoint.
-   V3.0 (2 de noviembre de 2009): Se ha revisado para anunciar la disponibilidad de una revisión para MS09-054 para corregir problemas de compatibilidad de aplicaciones. Los clientes que ya han aplicado esta actualización pueden instalar la revisión del artículo 976749 de Microsoft Knowledge Base.
-   V3.1 (4 de noviembre de 2009): Se han quitado las referencias erróneas a la versión de lanzamiento original de Microsoft Office Visio Viewer 2007 como software afectado en MS09-060 y MS09-062.
-   V4.0 (10 de noviembre de 2009): Se ha revisado el boletín para comunicar la nueva publicación de la actualización para Administrador de compresión de audio en Microsoft Windows 2000 Service Pack 4 en MS09-051 para corregir un problema de detección. Se trata únicamente de un cambio de detección; no había cambios en los archivos binarios. Los clientes que han actualizado correctamente sus sistemas no necesitan volver a instalar esta actualización.
-   V4.1 (12 de enero de 2010): Se ha quitado Microsoft Expression Web, Microsoft Expression Web 2, Microsoft Office Groove 2007 y Microsoft Office Groove 2007 Service Pack 1 como software afectado en MS09-062.
-   V4.2 (22 de junio de 2010): Se ha quitado .NET Framework 1.1 Service Pack 1 como componente afectado en Windows 7 y Windows Server 2008 R2 para MS09-061.

*Built at 2014-04-18T01:50:00Z-07:00*
