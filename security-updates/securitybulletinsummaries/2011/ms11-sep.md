---
TOCTitle: 'MS11-SEP'
Title: Microsoft Security Bulletin Summary for septiembre 2011
ms:assetid: 'ms11-sep'
ms:contentKeyID: 61225431
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms11-sep(v=Security.10)'
---

Microsoft Security Bulletin Summary for septiembre 2011
=======================================================

Publicado: martes, 13 de septiembre de 2011 | Actualizado: martes, 13 de septiembre de 2011

**Versión:** 1.1

Este resumen del boletín enumera los boletines de seguridad publicados para septiembre de 2011.

Con la publicación de los boletines de seguridad de septiembre de 2011, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 8 de septiembre de 2011. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://technet.microsoft.com/es-es/security/bulletin/advance).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 14 de septiembre de 2011, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de septiembre](https://msevents.microsoft.com/cui/eventdetail.aspx?culture=en-us&eventid=1032487951). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, consulte los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217214).

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-070">MS11-070</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en WINS podría permitir la elevación de privilegios (2571621)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Servicio de nombres Internet de Windows (WINS). La vulnerabilidad podría permitir la elevación de privilegios si un usuario recibe un paquete de réplica de WINS especialmente diseñado en un sistema afectado que ejecuta el servicio WINS. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-071">MS11-071</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en los componentes de Windows podría</strong> <strong>permitir la ejecución remota de código (2570947)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad que se ha divulgado públicamente en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo de formato de texto enriquecido (.rtf), un archivo de texto (.txt) o un documento de Word (.doc) legítimo que se encuentre en el mismo directorio de red que un archivo de biblioteca de vínculos dinámicos (DLL) especialmente diseñado. Un intruso que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario local. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a>  <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-072">MS11-072</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Excel</strong> <strong>podrían</strong> <strong>permitir la ejecución remota de código (2587505)</strong> <br />
<br />
Esta actualización de seguridad resuelve cinco vulnerabilidades de las que se ha informado de forma privada en Microsoft Office. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario abre un archivo de Excel especialmente diseñado. Un intruso que aprovechara cualquiera de estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario que ha iniciado sesión. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos. La instalación y configuración de Validación de documento de Office (OFV) para prevenir la apertura de archivos sospechosos bloquea las vías de ataque para aprovechar las vulnerabilidades descritas en CVE-2011-1986 y CVE-2011-1987.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office, <br />
software de servidor de Microsoft</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-073">MS11-073</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Office</strong> <strong>podrían</strong> <strong>permitir la ejecución remota de código (2587634)</strong> <br />
<br />
Esta actualización de seguridad resuelve dos vulnerabilidades de las que se ha informado de forma privada en Microsoft Office Visio. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario abre un archivo de Office especialmente diseñado o si un usuario abre un archivo de Office legítimo que se encuentre en el mismo directorio de red que un archivo de biblioteca especialmente diseñado. Un intruso que aprovechara cualquiera de las vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario que ha iniciado sesión. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-074">MS11-074</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft SharePoint</strong> <strong>podrían</strong> <strong>permitir</strong> <strong>la elevación de privilegios (2451858)</strong> <br />
<br />
Esta actualización de seguridad resuelve cinco vulnerabilidades de las que se ha informado de forma privada y una vulnerabilidad de la que se ha informado de forma pública en Microsoft SharePoint y Windows SharePoint Services. Las vulnerabilidades más graves podrían permitir la elevación de privilegios si un usuario hace clic en una dirección URL especialmente diseñada o visita un sitio web especialmente diseñado. En las vulnerabilidades más graves, los usuarios de Internet Explorer 8 e Internet Explorer 9 que exploren un sitio de SharePoint en la zona Internet están menos expuestos porque, de forma predeterminada, el filtro XSS en Internet Explorer 8 e Internet Explorer 9 contribuye a bloquear los ataques en la zona Internet. No obstante, el filtro XSS en Internet Explorer 8 e Internet Explorer 9 no está habilitado de forma predeterminada en la zona Intranet.</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/rating">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office, <br />
software de servidor de Microsoft</td>
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
<th style="border:1px solid black;" >Evaluación de explotabilidad de ejecución de código para la última versión de software</th>
<th style="border:1px solid black;" >Evaluación de explotabilidad de ejecución de código para las versiones de software anteriores</th>
<th style="border:1px solid black;" >Evaluación de explotabilidad de denegación de servicio</th>
<th style="border:1px solid black;" >Notas clave</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-070">MS11-070</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios locales en WINS</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1984">CVE-2011-1984</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-071">MS11-071</a></td>
<td style="border:1px solid black;">Vulnerabilidad en la carga de bibliotecas no seguras en componentes de Windows</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1991">CVE-2011-1991</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-072">MS11-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de WriteAV después de la liberación en Excel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1986">CVE-2011-1986</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-072">MS11-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad de indización de matriz fuera de los límites en Excel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1987">CVE-2011-1987</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-072">MS11-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en el montón en Excel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1988">CVE-2011-1988</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">2</a> - Poca probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-072">MS11-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad de análisis de expresiones condicionales en Excel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1989">CVE-2011-1989</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-072">MS11-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad de indización de matriz fuera de los límites en Excel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1990">CVE-2011-1990</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-073">MS11-073</a></td>
<td style="border:1px solid black;">Vulnerabilidad en la carga de bibliotecas no seguras en los componentes de Office</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1980">CVE-2011-1980</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-073">MS11-073</a></td>
<td style="border:1px solid black;">Vulnerabilidad de puntero de objeto no inicializado en Office</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1982">CVE-2011-1982</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-074">MS11-074</a></td>
<td style="border:1px solid black;">Vulnerabilidad de XSS en el calendario de SharePoint</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-0653">CVE-2011-0653</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-074">MS11-074</a></td>
<td style="border:1px solid black;">Vulnerabilidad de saneamiento de HTML</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1252">CVE-2011-1252</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> - Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> - Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información<br />
<br />
Esta vulnerabilidad ya se ha divulgado públicamente</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-074">MS11-074</a></td>
<td style="border:1px solid black;">Vulnerabilidad de inserción de scripts de Editform</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1890">CVE-2011-1890</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-074">MS11-074</a></td>
<td style="border:1px solid black;">Vulnerabilidad de XSS reflejado en detalles de contacto</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1891">CVE-2011-1891</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-074">MS11-074</a></td>
<td style="border:1px solid black;">Vulnerabilidad de divulgación remota de archivos en SharePoint</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1892">CVE-2011-1892</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> - Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">3</a> - Improbabilidad de código funcional que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms11-074">MS11-074</a></td>
<td style="border:1px solid black;">Vulnerabilidad de XSS en SharePoint</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2011-1893">CVE-2011-1893</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/cc998259.aspx">1</a> - Bastante probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
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

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="3" style="border:1px solid black;">
Windows XP  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-070**](http://go.microsoft.com/fwlink/?linkid=225825)
</td>
<td style="border:1px solid black;">
[**MS11-071**](http://go.microsoft.com/fwlink/?linkid=223632)
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
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=70f944b0-9bf0-4168-b150-67d2ff68df2d)  
(Importante)
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
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4b9debed-edbb-43e1-b755-0faf01980289)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-070**](http://go.microsoft.com/fwlink/?linkid=225825)
</td>
<td style="border:1px solid black;">
[**MS11-071**](http://go.microsoft.com/fwlink/?linkid=223632)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1e6ac3b2-752e-49a0-84e5-5a8dfe955299)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d44274d2-0401-4fd8-bc4f-c59f6d81c34f)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f9378339-c58e-4e84-9427-85aeb35b0d99)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=935720ee-cee0-42c2-965e-ce1b07e95e1a)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=c35c71a8-13b4-47a6-9763-06f6f65327b1)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=78c2ac72-da89-42a4-bff9-79551b5d3c4e)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-070**](http://go.microsoft.com/fwlink/?linkid=225825)
</td>
<td style="border:1px solid black;">
[**MS11-071**](http://go.microsoft.com/fwlink/?linkid=223632)
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
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=15840336-4886-4a1b-8c1e-2c535c3938f7)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e80739b4-89bb-4317-8381-991244a71cb8)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-070**](http://go.microsoft.com/fwlink/?linkid=225825)
</td>
<td style="border:1px solid black;">
[**MS11-071**](http://go.microsoft.com/fwlink/?linkid=223632)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a9039660-3cc2-470d-a0a5-a70f78074495)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=05c39ab3-7b57-4147-8913-df5df6005799)\*  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5ea78a9b-b1f7-4e94-b69e-c984e1622ae9)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1499d988-fd55-4317-b859-ec170907d547)\*  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6e2d2ea9-0af6-4d23-875d-3211722cd62f)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows 7
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-070**](http://go.microsoft.com/fwlink/?linkid=225825)
</td>
<td style="border:1px solid black;">
[**MS11-071**](http://go.microsoft.com/fwlink/?linkid=223632)
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
Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits y Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=76b99ab2-7e99-4aad-a419-7996bae05c48)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 y Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=0f6d32de-d3ff-4af9-9b26-a4f12581f5fe)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows Server 2008 R2
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-070**](http://go.microsoft.com/fwlink/?linkid=225825)
</td>
<td style="border:1px solid black;">
[**MS11-071**](http://go.microsoft.com/fwlink/?linkid=223632)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=f58cf343-946c-4e74-bd9c-40ac934a4986)\*  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 y Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=a8a451bd-3e5c-4845-9941-daabd9418776)\*  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium y Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=0fdfb1f9-20b3-4d61-8019-33d1003290c8)  
(Importante)
</td>
</tr>
</table>
 
**Nota** **para** **Windows Server 2008 y Windows Server 2008 R2**

**\*La instalación de Server** **Core** **está afectada.** Esta actualización se aplica, con la misma clasificación de gravedad, a las ediciones compatibles de Windows Server 2008 o Windows Server 2008 R2 tal como se indica, independientemente de si se ha instalado con la opción de instalación Server Core. Para obtener más información acerca de esta opción de instalación, vea los artículos de TechNet [Administración de una instalación Server Core](http://technet.microsoft.com/en-us/library/ee441255(ws.10).aspx) y [Mantenimiento de una instalación Server Core](http://technet.microsoft.com/en-us/library/ff698994(ws.10).aspx). Tenga en cuenta que la opción de instalación Server Core no se aplica a determinadas ediciones de Windows Server 2008 y Windows Server 2008 R2; vea [Comparar opciones de instalación de Server Core](http://www.microsoft.com/windowsserver2008/en/us/compare-core-installation.aspx).

#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="4" style="border:1px solid black;">
Conjuntos de programas y componentes de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador** **del** **boletín**
</td>
<td style="border:1px solid black;">
[**MS11-072**](http://go.microsoft.com/fwlink/?linkid=225047)
</td>
<td style="border:1px solid black;">
[**MS11-073**](http://go.microsoft.com/fwlink/?linkid=225103)
</td>
<td style="border:1px solid black;">
[**MS11-074**](http://go.microsoft.com/fwlink/?linkid=204797)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
[Microsoft Excel 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=dee4f3d7-bc4b-47fd-8e3f-9d2b0e82d0f6)  
(KB2553072)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=7faa2f90-2e64-4dbf-ac93-bb8cffc9b5fe)  
(KB2584052)  
(Importante)
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
[Microsoft Excel 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=498ac241-d728-4944-abac-ec8444ca6418)  
(KB2553073)<sup>[1]</sup>
(Importante)  

[Microsoft Office 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=df04b9ce-2daa-4b4d-a944-a873075656f9)  
(KB2553089)<sup>[1]</sup>
(Importante)  

[Microsoft Office 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=90eef02b-db1f-4fdd-bb1d-408063671e4d)  
(KB2553090)<sup>[1]</sup>
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=34bbee95-0e83-4705-8bfe-02e4fb22f8e7)  
(KB2584063)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 y Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Excel 2010 y Microsoft Excel 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=4612c6e4-ac29-4cc4-9da5-88779ea3643e)  
(KB2553070)  
(Importante)  

[Microsoft Office 2010 y Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=1fd15144-5547-4927-8583-8d9b06819226)  
(KB2553091)  
(Importante)  

[Microsoft Office 2010 y Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=18840d78-944f-400a-addc-dce7e570a569)  
(KB2553096)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2010 y Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=3c8fd04a-9df6-4726-a9bc-811f49665981)  
(KB2584066)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2010 y Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Excel 2010 y Microsoft Excel 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=d40db27b-1318-4ca7-b44f-c90bb6342109)  
(KB2553070)  
(Importante)  

[Microsoft Office 2010 y Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=f83800aa-6403-4341-afea-d363e54d5831)  
(KB2553091)  
(Importante)  

[Microsoft Office 2010 y Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=92787e00-6f30-4020-9c1a-70270be5a623)  
(KB2553096)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2010 y Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=85360dc1-99e7-4e3e-be6f-3795e8a8122f)  
(KB2584066)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Microsoft Office para Mac
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-072**](http://go.microsoft.com/fwlink/?linkid=225047)
</td>
<td style="border:1px solid black;">
[**MS11-073**](http://go.microsoft.com/fwlink/?linkid=225103)
</td>
<td style="border:1px solid black;">
[**MS11-074**](http://go.microsoft.com/fwlink/?linkid=204797)
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
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2004 para Mac
</td>
<td style="border:1px solid black;">
[Microsoft Office 2004 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=868f4d9f-3498-4d59-a017-59204553889c)  
(KB2598782)  
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
Microsoft Office 2008 para Mac
</td>
<td style="border:1px solid black;">
[Microsoft Office 2008 para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=afa79cfc-6e8a-4d0b-88aa-0d7e05031e44)  
(KB2598781)  
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
Microsoft Office para Mac 2011
</td>
<td style="border:1px solid black;">
[Microsoft Office para Mac 2011](http://www.microsoft.com/downloads/details.aspx?familyid=535fcf4a-eeb2-44eb-b2a6-9c512509c49d)  
(KB2598783)  
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
Convertidor de archivos con formatos XML abiertos para Mac
</td>
<td style="border:1px solid black;">
[Convertidor de archivos con formatos XML abiertos para Mac](http://www.microsoft.com/downloads/details.aspx?familyid=9796588d-238f-4694-9598-1aa8d2becb55)  
(KB2598785)  
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
<th colspan="4" style="border:1px solid black;">
Microsoft Office Groove y Microsoft SharePoint Workspace
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-072**](http://go.microsoft.com/fwlink/?linkid=225047)
</td>
<td style="border:1px solid black;">
[**MS11-073**](http://go.microsoft.com/fwlink/?linkid=225103)
</td>
<td style="border:1px solid black;">
[**MS11-074**](http://go.microsoft.com/fwlink/?linkid=204797)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Groove 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office Groove 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5ea6192b-55e5-4ca4-8d91-cc768ede8277)  
(KB2552997)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Workspace 2010 y Microsoft SharePoint Workspace 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft SharePoint Workspace 2010 y Microsoft SharePoint Workspace 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=f6ee7e43-9da9-4b96-abd0-390cfcacb885)  
(KB2566445)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Workspace 2010 y Microsoft SharePoint Workspace 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft SharePoint Workspace 2010 y Microsoft SharePoint Workspace 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=234efac1-4f09-41f5-90a9-4a3c2e81c05e)  
(KB2566445)  
(Importante)
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Otro software de Microsoft Office
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-072**](http://go.microsoft.com/fwlink/?linkid=225047)
</td>
<td style="border:1px solid black;">
[**MS11-073**](http://go.microsoft.com/fwlink/?linkid=225103)
</td>
<td style="border:1px solid black;">
[**MS11-074**](http://go.microsoft.com/fwlink/?linkid=204797)
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
Ninguna
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Excel Viewer Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft Excel Viewer Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f82ca5da-a55a-487c-8170-46a40000c8e3)  
(KB2553075)  
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
Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
[Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=01093f22-06b7-4c9b-bff9-f54ac5d73bf8)  
(KB2553074)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
**Notas para MS11-072**

<sup>[1]</sup>Para Microsoft Excel 2007 Service Pack 2, además del paquete de actualización de seguridad KB2553073, KB2553089 y KB2553090, los clientes también deben instalar la actualización de seguridad para Paquete de compatibilidad de Microsoft Office para formatos de archivo de Word, Excel y PowerPoint 2007 Service Pack 2 (KB2553074) con el fin de protegerse de las vulnerabilidades descritas en este boletín.

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

**Nota para MS11-074**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Software de servidor de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft SharePoint Server
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-072**](http://go.microsoft.com/fwlink/?linkid=225047)
</td>
<td style="border:1px solid black;">
[**MS11-074**](http://go.microsoft.com/fwlink/?linkid=204797)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office SharePoint Server 2007 Service Pack 2 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Excel Services](http://www.microsoft.com/downloads/details.aspx?familyid=dd532201-485c-4270-88d3-63bd3f24327e)  
(KB2553093)<sup>[2]</sup>
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office SharePoint Server 2007 Service Pack 2 (coreserver) (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=ad52c341-13ce-4b53-87b4-269cb3f41275)  
(KB2508964)<sup>[1]</sup>
(Importante)  

[Microsoft Office SharePoint Server 2007 Service Pack 2 (oserver) (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=fd6189c9-ab3b-441f-a901-6ac7f3b202aa)  
(KB2553001)<sup>[1]</sup>
(Importante)  

[Microsoft Office SharePoint Server 2007 Service Pack 2 (sserverx) (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=d9601fae-4a80-45cd-a49b-ef441856d7e4)  
(KB2553002)<sup>[1]</sup>
(Importante)  

[Microsoft Office SharePoint Server 2007 Service Pack 2 (dlc) (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=55b60e2f-ec68-4ccb-803a-5d03add8a1f1)  
(KB2553003)<sup>[1]</sup>
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office SharePoint Server 2007 Service Pack 2 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Excel Services](http://www.microsoft.com/downloads/details.aspx?familyid=1086a5b0-e441-4e26-a8d1-924a20121dde)  
(KB2553093)<sup>[2]</sup>
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office SharePoint Server 2007 Service Pack 2 (coreserver) (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=e5e60751-242a-4fdb-9852-6d94050d3d0e)  
(KB2508964)<sup>[1]</sup>
(Importante)  

[Microsoft Office SharePoint Server 2007 Service Pack 2 (oserver) (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=b1466366-e2ae-498e-b964-135e034e7348)  
(KB2553001)<sup>[1]</sup>
(Importante)  

[Microsoft Office SharePoint Server 2007 Service Pack 2 (sserverx) (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=bb788c8d-8383-4e53-ac05-2a7dd9b83e70)  
(KB2553002)<sup>[1]</sup>
(Importante)  

[Microsoft Office SharePoint Server 2007 Service Pack 2 (dlc) (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=e8e1a5bb-a552-45fe-8e81-e05fbfbb57ee)<sup>[1]</sup>
(Importante)  
(KB2553003)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office SharePoint Server 2010 y Microsoft Office SharePoint Server 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft Excel Services](http://www.microsoft.com/downloads/details.aspx?familyid=0c150328-6a15-4852-a09c-4063142bd946)  
(KB2553094)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office SharePoint Server 2010 y Microsoft Office SharePoint Server 2010 Service Pack 1 (osrchwfe)](http://www.microsoft.com/downloads/details.aspx?familyid=c17eb04d-cbbc-457e-a424-4ee26b7a9654)  
(KB2494022)  
(Importante)  

[Microsoft Office SharePoint Server 2010 y Microsoft Office SharePoint Server 2010 Service Pack 1 (osrv)](http://www.microsoft.com/downloads/details.aspx?familyid=2a80a849-b712-47d4-9def-9395ee54a265)  
(KB2560885)  
(Importante)  

[Microsoft Office SharePoint Server 2010 y Microsoft Office SharePoint Server 2010 Service Pack 1 (pplwfe)](http://www.microsoft.com/downloads/details.aspx?familyid=b84c2bcb-0327-4916-871e-7a5c19b8c41b)  
(KB2560890)  
(Importante)  

[Microsoft Office SharePoint Server 2010 y Microsoft Office SharePoint Server 2010 Service Pack 1 (ppsmawfe)](http://www.microsoft.com/downloads/details.aspx?familyid=1597f295-02a9-4479-9d52-f18f0e83eaba)  
(KB2566456)  
(Importante)  

[Microsoft Office SharePoint Server 2010 y Microsoft Office SharePoint Server 2010 Service Pack 1 (dlc)](http://www.microsoft.com/downloads/details.aspx?familyid=e6b666a4-a795-441c-9bda-23e2de2e7b05)  
(KB2566954)  
(Importante)  

[Microsoft Office SharePoint Server 2010 y Microsoft Office SharePoint Server 2010 Service Pack 1 (ppsmamui)](http://www.microsoft.com/downloads/details.aspx?familyid=57592ce4-5d99-45c2-830f-380d67af8899)  
(KB2566958)  
(Importante)  

[Microsoft Office SharePoint Server 2010 y Microsoft Office SharePoint Server 2010 Service Pack 1 (wosrv)](http://www.microsoft.com/downloads/details.aspx?familyid=dd64a635-1e55-4b4d-9718-9b94c31c5625)  
(KB2566960)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Office Forms Server
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-072**](http://go.microsoft.com/fwlink/?linkid=225047)
</td>
<td style="border:1px solid black;">
[**MS11-074**](http://go.microsoft.com/fwlink/?linkid=204797)
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
Microsoft Office Forms Server 2007 Service Pack 2 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office Forms Server 2007 Service Pack 2 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=c4c8ad7e-50bd-460e-9678-d8c72c6ee7ab)  
(KB2553005)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Forms Server 2007 Service Pack 2 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office Forms Server 2007 Service Pack 2 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=7390b526-f411-45a4-8587-8077b473ac17)  
(KB2553005)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Groove Server
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-072**](http://go.microsoft.com/fwlink/?linkid=225047)
</td>
<td style="border:1px solid black;">
[**MS11-074**](http://go.microsoft.com/fwlink/?linkid=204797)
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
Microsoft Office Groove Data Bridge Server 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office Groove Data Bridge Server 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=5958247e-204e-409c-bdc1-7aff06e854b8)  
(KB2552999)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Groove Management Server 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office Groove Management Server 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6b5b4caf-6a95-487d-ac17-c4435225af3a)  
(KB2552998)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Groove Server 2010 y Microsoft Groove Server 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Groove Server 2010 y Microsoft Groove Server 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=71c0f217-5112-4dca-b9aa-46c69f6099e4)  
(KB2508965)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Office Web Apps
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del** **boletín**
</td>
<td style="border:1px solid black;">
[**MS11-072**](http://go.microsoft.com/fwlink/?linkid=225047)
</td>
<td style="border:1px solid black;">
[**MS11-074**](http://go.microsoft.com/fwlink/?linkid=204797)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Web Apps 2010 y Microsoft Office Web Apps 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft Excel Web App 2010 y Microsoft Excel Web App 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=73d49094-a9cf-407e-8921-1b22fbc30427)  
(KB2553095)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Office Web Apps 2010 y Microsoft Office Web Apps 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=288a7394-b8d5-4445-bd4c-65bbf4b10eaf)  
(KB2566449)  
(Importante)  

[Microsoft Word Web App 2010 y Microsoft Word Web App 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=152ff9f4-d720-41af-8f89-793133ece037)  
(KB2566450)  
(Importante)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Windows SharePoint Services y Microsoft SharePoint Foundation
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS11-072**](http://go.microsoft.com/fwlink/?linkid=225047)
</td>
<td style="border:1px solid black;">
[**MS11-074**](http://go.microsoft.com/fwlink/?linkid=204797)
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
Microsoft Windows SharePoint Services 2.0
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Windows SharePoint Services 2.0](http://www.microsoft.com/downloads/details.aspx?familyid=71e32745-cb05-4b87-a447-741ccdac7450)  
(KB2494007)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Windows SharePoint Services 3.0 Service Pack 2 (versiones de 32 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Windows SharePoint Services 3.0 Service Pack 2 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=0f306cbd-a652-4e77-b394-1a6dc38ba83c)  
(KB2493987)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Windows SharePoint Services 3.0 Service Pack 2 (versiones de 64 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Windows SharePoint Services 3.0 Service Pack 2 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=3137e4c6-783d-4461-88bd-90da064e3105)  
(KB2493987)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Foundation 2010 y Microsoft SharePoint Foundation 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft SharePoint Foundation 2010 y Microsoft SharePoint Foundation 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=0db799e2-896f-464b-8cd5-ecf2014f0588)  
(KB2494001)  
(Importante)
</td>
</tr>
</table>
 
**Notas para MS11-072**

<sup>[2]</sup>Esta actualización se aplica a los servidores que tienen instalados Servicios de Excel, como la configuración predeterminada de Microsoft Office SharePoint Server 2007 Enterprise y Microsoft Office SharePoint Server 2007 para sitios de Internet. Microsoft Office SharePoint Server 2007 Standard no incluye Servicios de Excel.

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

**Notas para MS11-074**

<sup>[1]</sup>Para las ediciones compatibles de Microsoft Office SharePoint Server 2007, además de los paquetes de actualización de seguridad para Microsoft Office SharePoint 2007 (KB2508964, KB2553001, KB2553002 y KB2553003), los clientes también deben instalar la actualización de seguridad para Microsoft Windows SharePoint Services 3.0 (KB2493987) a fin de estar protegidos contra las vulnerabilidades descritas en este boletín.

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/). [TechNet Security Center](http://technet.microsoft.com/es-es/security/default.aspx) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://www.microsoft.com/es-es/security/default.aspx), donde esta información también está disponible haciendo clic en “Últimas actualizaciones de seguridad”.

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

**System** **Center** **Configuration** **Manager** **2007**

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

Aprenda a mejorar la seguridad y a optimizar la infraestructura informática y comparta sus problemas de seguridad con otros profesionales del sector en [IT Pro Security Community](http://go.microsoft.com/fwlink/?linkid=21164) (en inglés).

#### Agradecimientos

Microsoft [muestra su agradecimiento](http://go.microsoft.com/fwlink/?linkid=21127) a todas las personas que han trabajado con nosotros para proteger a los clientes:

-   Nicolas Economou, de [Core Security Technologies](http://www.coresecurity.com/), por informar de un problema descrito en MS11-070
-   Un investigador anónimo, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS11-072
-   Sean Larsson, de [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS11-072
-   Un investigador anónimo, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS11-072
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de TippingPoint, por informar de un problema descrito en MS11-072
-   Omair, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.tippingpoint.com/), por informar de un problema descrito en MS11-072
-   Parvez Anwar, en colaboración con [Secunia Research](http://secunia.com/), por informar de un problema descrito en MS11-073
-   David Warren, de [CERT/CC](http://www.cert.org/), por informar de un problema descrito en MS11-073
-   Andrew Connell, de [Critical Path Training, LLC](http://www.criticalpathtraining.com/), por informar de un problema descrito en MS11-074
-   David Feldman, de [Raytheon](http://www.raytheon.com/), por informar de un problema descrito en MS11-074
-   Adi Cohen, de [IBM Rational Application Security](http://blog.watchfire.com/), por informar de un problema descrito en MS11-074
-   [Trend Micro](http://www.trendmicro.com/)
-   , por colaborar con nosotros en un problema descrito en MS11-074
-   Pedro Jimenez, de [ITT](http://www.itt.com/), por informar de un problema descrito en MS11-074
-   [Seeker automatic application security testing solution](http://www.seekersec.com/)
-   , por informar de un problema descrito en MS11-074
-   Nicolas Grégoire, de [Agarri](http://www.agarri.fr/), por informar de un problema descrito en MS11-074
-   Jim LaValley, de [LaValley Consulting, LLC](http://www.lavalley.net), por informar de un problema descrito en MS11-074
-   Irene Abezgauz, de [Seeker](http://www.seekersec.com), por colaborar con nosotros en una actualización de defensa en profundidad en MS11-074

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Los clientes de Estados Unidos y Canadá pueden recibir soporte técnico del [soporte de seguridad](http://go.microsoft.com/fwlink/?linkid=21131) o en el teléfono 1-866-PCSAFETY. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de las opciones de asistencia disponibles, visite [Ayuda y soporte técnico de Microsoft](http://support.microsoft.com/).
-   Los clientes internacionales pueden recibir soporte técnico en las subsidiarias de Microsoft de sus países. Las llamadas de soporte técnico relacionadas con las actualizaciones de seguridad son gratuitas. Para obtener más información acerca de cómo ponerse en contacto con Microsoft en relación con problemas de soporte técnico, visite [Ayuda y soporte técnico](http://go.microsoft.com/fwlink/?linkid=21155) internacional.

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (13 de septiembre de 2011): Publicación del resumen del boletín.
-   V1.1 (13 de septiembre de 2011): Para MS11-074, se ha agregado la información de vínculo para la actualización de Microsoft Office SharePoint Server 2010 y Microsoft Office SharePoint Server 2010 Service Pack 1 (pplwfe) (KB2560890).

*Built at 2014-04-18T01:50:00Z-07:00*
