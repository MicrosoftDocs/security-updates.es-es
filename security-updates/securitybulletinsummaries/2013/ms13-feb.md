---
TOCTitle: 'MS13-FEB'
Title: Resumen del boletín de seguridad de Microsoft de febrero 2013
ms:assetid: 'ms13-feb'
ms:contentKeyID: 61225447
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms13-feb(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de febrero 2013
=============================================================

Publicado: martes, 12 de febrero de 2013 | Actualizado: miércoles, 13 de febrero de 2013

**Versión:** 1.2

Este resumen del boletín enumera los boletines de seguridad publicados para febrero de 2013.

Con la publicación de los boletines de seguridad de febrero de 2013, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 7 de febrero de 2013. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 13 de febrero de 2013, a las 11:00 a.m., hora del Pacífico (EE. UU. y Canadá). [Inscríbase ahora a la conferencia en línea del boletín de seguridad de febrero](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032538626&culture=en-us). Después de esta fecha, este webcast estará disponible [a petición](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032538626&culture=en-us).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, Información adicional.

### Información del boletín

#### Resúmenes ejecutivos

En la tabla siguiente se resumen los boletines de seguridad de este mes por orden de gravedad.

Para obtener detalles acerca del software afectado, vea la siguiente sección, Ubicaciones de descarga y software afectado.

 
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275670">MS13-009</a></td>
<td style="border:1px solid black;">Actualización de seguridad acumulativa para Internet Explorer (2792100)  <br />
<br />
Esta actualización de seguridad resuelve trece vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. La más grave de las vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un intruso que aprovechara estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, <br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275837">MS13-010</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en el lenguaje de marcado vectorial podría permitir la ejecución remota de código (2797052) <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en la implementación de Microsoft del lenguaje de marcado vectorial (VML). La vulnerabilidad podría permitir la ejecución remota de código si un usuario visita una página web especialmente diseñada mediante Internet Explorer. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, <br />
Internet Explorer</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=271307">MS13-011</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en la descompresión de medios podría permitir la ejecución remota de código (2780091)  <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo multimedia especialmente diseñado (como un archivo .mpg), abre un documento de Microsoft Office (como un archivo .ppt) que contiene un archivo multimedia insertado especialmente diseñado o recibe contenido de transmisión por secuencias especialmente diseñado. Un atacante que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=279801">MS13-012</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Exchange Server podrían permitir la ejecución remota de código (2809279)  <br />
<br />
Esta actualización de seguridad resuelve vulnerabilidades de las que se ha informado de forma pública en Microsoft Exchange Server. La vulnerabilidad más grave se encuentra en Microsoft Exchange Server WebReady Document Viewing y podría permitir la ejecución remota de código en el contexto de seguridad del servicio de transcodificación en el servidor Exchange si un usuario obtiene una vista previa de un archivo especialmente diseñado mediante Outlook Web App (OWA). El servicio de transcodificación de Exchange que se usa para WebReady Document Viewing se ejecuta en la cuenta LocalService. La cuenta LocalService tiene privilegios mínimos en el equipo local y presenta credenciales anónimas en la red.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Software de servidor de Microsoft</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=279005">MS13-020</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en la automatización OLE podría permitir la ejecución remota de código (2802968)  <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en la automatización de vinculación e incrustación de objetos (OLE) de Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo especialmente diseñado. Un atacante que aprovechara la vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=272434">MS13-013</a></td>
<td style="border:1px solid black;">Vulnerabilidades en el análisis de FAST Search Server 2010 for SharePoint podrían permitir la ejecución remota de código (2784242)  <br />
<br />
Esta actualización de seguridad resuelve vulnerabilidades que se han divulgado de forma pública en Microsoft FAST Search Server 2010 for SharePoint. Las vulnerabilidades podrían permitir la ejecución remota de código en el contexto de seguridad de una cuenta de usuario con un token restringido. FAST Search Server for SharePoint solo está afectado por este problema cuando Advanced Filter Pack está habilitado. De forma predeterminada, Advanced Filter Pack está deshabilitado.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office, <br />
Software de servidor de Microsoft</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=276948">MS13-014</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en el servidor NFS podría permitir la denegación de servicio (2790978)  <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la denegación de servicio si un atacante intenta una operación de archivo en un recurso compartido de solo lectura. Un atacante que aprovechara esta vulnerabilidad podría provocar que el sistema afectado dejara de responder y se reiniciara. La vulnerabilidad solo afecta a Windows Server con el rol NFS habilitado.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Denegación de servicio</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275736">MS13-015</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en .NET Framework podría permitir la elevación de privilegios (2800277)  <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privadaen .NET Framework. La vulnerabilidad podría permitir la elevación de privilegios si un usuario visita una página web especialmente diseñada mediante un explorador web que pueda ejecutar aplicaciones del explorador XAML (XBAP). La vulnerabilidad también la podrían usar aplicaciones Windows .NET para omitir las restricciones de seguridad de acceso del código (CAS). Un atacante que aprovechara la vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, <br />
Microsoft .NET Framework</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidades en el controlador modo kernel de Windows podrían permitir la elevación de privilegios (2778344 <br />
Esta actualización de seguridad resuelve 30 vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. Las vulnerabilidades podrían permitir la elevación de privilegios si un atacante inicia sesión en el sistema y ejecuta una aplicación especialmente diseñada. Para aprovechar las vulnerabilidades, un atacante debe tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=278914">MS13-017</a></td>
<td style="border:1px solid black;">Vulnerabilidades del kernel de Windows podrían permitir la elevación de privilegios (2799494) <br />
Esta actualización de seguridad resuelve tres vulnerabilidades de las que se ha informado de forma privada en todas las versiones compatibles de Microsoft Windows. Las vulnerabilidades podrían permitir la elevación de privilegios si un atacante inicia sesión en el sistema y ejecuta una aplicación especialmente diseñada. Para aprovechar las vulnerabilidades, un atacante debe tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=278912">MS13-018</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en TCP/IP podría permitir la denegación de servicio (2790655)  <br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la denegación de servicio si un atacante sin autenticar envía un paquete de finalización de conexión especialmente diseñado al servidor.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Denegación de servicio</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=278896">MS13-019</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en el subsistema de tiempo de ejecución de cliente-servidor (CSRSS) de Windows podría permitir la elevación de privilegios (2790113)  <br />
Esta actualización de seguridad resuelve una vulnerabilidad que se ha divulgado públicamente en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si un atacante inicia sesión en un sistema y ejecuta una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275670">MS13-009</a></td>
<td style="border:1px solid black;">Vulnerabilidad de codificación de caracteres de desplazamiento JIS</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0015">CVE-2013-0015</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275670">MS13-009</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de SetCapture después de la liberación en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0018">CVE-2013-0018</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275670">MS13-009</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de COmWindowProxy después de la liberación en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0019">CVE-2013-0019</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275670">MS13-009</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de CMarkup después de la liberación en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0020">CVE-2013-0020</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275670">MS13-009</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de vtable después de la liberación en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0021">CVE-2013-0021</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275670">MS13-009</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de LsGetTrailInfo después de la liberación en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0022">CVE-2013-0022</a></td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275670">MS13-009</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de CDispNode después de la liberación en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0023">CVE-2013-0023</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275670">MS13-009</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de pasteHTML después de la liberación en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0024">CVE-2013-0024</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275670">MS13-009</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de SLayoutRun después de la liberación en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0025">CVE-2013-0025</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275670">MS13-009</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de InsertElement después de la liberación en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0026">CVE-2013-0026</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275670">MS13-009</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de CPasteCommand después de la liberación en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0027">CVE-2013-0027</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275670">MS13-009</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de CObjectElement después de la liberación en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0028">CVE-2013-0028</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275670">MS13-009</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de CHTML después de la liberación en Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0029">CVE-2013-0029</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275837">MS13-010</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con VML</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0030">CVE-2013-0030</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Microsoft tiene constancia de que esta vulnerabilidad se usa como una vulnerabilidad de divulgación de información en ataques limitados y dirigidos.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=271307">MS13-011</a></td>
<td style="border:1px solid black;">Vulnerabilidad en la descompresión de medios</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0077">CVE-2013-0077</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=279801">MS13-012</a></td>
<td style="border:1px solid black;">Oracle Outside In contiene varias vulnerabilidades que se pueden aprovechar</td>
<td style="border:1px solid black;">Varias*</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">*Varias vulnerabilidades, vea el boletín MS13-012 para obtener detalles.<br />
<br />
Estas vulnerabilidades se han divulgado de forma pública.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=272434">MS13-013</a></td>
<td style="border:1px solid black;">Oracle Outside In contiene varias vulnerabilidades que se pueden aprovechar</td>
<td style="border:1px solid black;">Varias*</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">*Varias vulnerabilidades, vea el boletín MS13-013 para obtener detalles.<br />
<br />
Estas vulnerabilidades se han divulgado de forma pública.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=276948">MS13-014</a></td>
<td style="border:1px solid black;">Vulnerabilidad de anulación de referencia nula</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1281">CVE-2013-1281</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275736">MS13-015</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en la devolución de llamada de WinForms</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0073">CVE-2013-0073</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1248">CVE-2013-1248</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una medida de defensa en profundidad en el software más reciente.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1249">CVE-2013-1249</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una medida de defensa en profundidad en el software más reciente.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1250">CVE-2013-1250</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1251">CVE-2013-1251</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1252">CVE-2013-1252</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1253">CVE-2013-1253</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1254">CVE-2013-1254</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1255">CVE-2013-1255</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1256">CVE-2013-1256</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1257">CVE-2013-1257</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1258">CVE-2013-1258</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1259">CVE-2013-1259</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1260">CVE-2013-1260</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1261">CVE-2013-1261</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1262">CVE-2013-1262</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1263">CVE-2013-1263</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1264">CVE-2013-1264</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1265">CVE-2013-1265</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1266">CVE-2013-1266</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1267">CVE-2013-1267</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1268">CVE-2013-1268</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1269">CVE-2013-1269</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1270">CVE-2013-1270</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1271">CVE-2013-1271</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1272">CVE-2013-1272</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1273">CVE-2013-1273</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1274">CVE-2013-1274</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1275">CVE-2013-1275</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1276">CVE-2013-1276</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=275718">MS13-016</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución de Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1277">CVE-2013-1277</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=278914">MS13-017</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución del kernel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1278">CVE-2013-1278</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=278914">MS13-017</a></td>
<td style="border:1px solid black;">Vulnerabilidad de condición de ejecución del kernel</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1279">CVE-2013-1279</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=278914">MS13-017</a></td>
<td style="border:1px solid black;">Vulnerabilidad de recuento de referencias en el kernel de Windows</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1280">CVE-2013-1280</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=278912">MS13-018</a></td>
<td style="border:1px solid black;">Vulnerabilidad de FIN WAIT en TCP</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0075">CVE-2013-0075</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=278896">MS13-019</a></td>
<td style="border:1px solid black;">Vulnerabilidad de recuento de referencias</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0076">CVE-2013-0076</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=279005">MS13-020</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código en automatización OLE</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1313">CVE-2013-1313</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
</tbody>
</table>
  
Ubicaciones de descarga y software afectado  
-------------------------------------------
  
Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.
  
¿Cómo se usan estas tablas?
  
Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, se indica un hipervínculo a la actualización de software disponible y también se muestra la clasificación de gravedad de dicha actualización de software.
  
Nota Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.
  
#### Componentes y sistema operativo Windows

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="11" style="border:1px solid black;">
Windows XP  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-009](http://go.microsoft.com/fwlink/?linkid=275670)
</td>
<td style="border:1px solid black;">
[MS13-010](http://go.microsoft.com/fwlink/?linkid=275837)
</td>
<td style="border:1px solid black;">
[MS13-011](http://go.microsoft.com/fwlink/?linkid=271307)
</td>
<td style="border:1px solid black;">
[MS13-020](http://go.microsoft.com/fwlink/?linkid=279005)
</td>
<td style="border:1px solid black;">
[MS13-014](http://go.microsoft.com/fwlink/?linkid=276948)
</td>
<td style="border:1px solid black;">
[MS13-015](http://go.microsoft.com/fwlink/?linkid=275736)
</td>
<td style="border:1px solid black;">
[MS13-016](http://go.microsoft.com/fwlink/?linkid=275718)
</td>
<td style="border:1px solid black;">
[MS13-017](http://go.microsoft.com/fwlink/?linkid=278914)
</td>
<td style="border:1px solid black;">
[MS13-018](http://go.microsoft.com/fwlink/?linkid=278912)
</td>
<td style="border:1px solid black;">
[MS13-019](http://go.microsoft.com/fwlink/?linkid=278896)
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
Ninguna
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
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
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=9bf087e7-4487-48bf-84e9-04b816411a0f)   
(KB2792100)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=4501ef62-7d06-49b7-af86-c84e399e6275)  
(KB2792100)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=2ab64eac-8ecf-4178-9a01-5f10fc2f049e)  
(KB2792100)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=daed0c2e-bd9a-4685-a5f9-1c01f7fdeccf)   
(KB2797052)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=fd693211-bcc8-4267-9aa1-86bac45e25bf)  
(KB2797052)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=e8924d23-f6e2-41bf-9542-f8991d084db9)  
(KB2797052)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Quartz.dll (DirectShow)](http://www.microsoft.com/downloads/details.aspx?familyid=95f5acea-32a0-42a5-a14d-837edf313984)   
(KB2780091)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=3a8ddbab-5999-48b7-9de8-423954f345b6)  
(KB2802968)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=eb202940-0ece-4631-83d5-8cf52c7dbf36)  
(KB2789643)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=cdaa7282-c354-4d70-938a-a025631205a2)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=9100bf70-8723-4635-9b78-f7c3048a950f)  
(KB2799494)    
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
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=c42347dd-5ec8-4760-a685-2cd7b6bb7bb2)   
(KB2792100)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=6513176c-e9cb-4863-a228-5bc369135996)  
(KB2792100)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=25e15457-ffd2-4466-aff9-1d0830e967d7)  
(KB2792100)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=dd9383b9-a6df-44a7-bea9-8f7d088bc488)   
(KB2797052)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=b042e717-bf4e-44a1-a1ba-6359bf551e8e)  
(KB2797052)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=c8618c96-25c0-415b-b147-5713ec5ab5b1)  
(KB2797052)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Quartz.dll (DirectShow)](http://www.microsoft.com/downloads/details.aspx?familyid=06ef35a1-f76f-4e99-a8b2-6b086c7e51be)   
(KB2780091)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=eb202940-0ece-4631-83d5-8cf52c7dbf36)  
(KB2789643)   
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f72228df-8379-4bd9-b446-cb9505e9d228)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9a945336-b037-4ee6-9ea2-dfb885747b97)  
(KB2799494)    
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
<th colspan="11" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-009](http://go.microsoft.com/fwlink/?linkid=275670)
</td>
<td style="border:1px solid black;">
[MS13-010](http://go.microsoft.com/fwlink/?linkid=275837)
</td>
<td style="border:1px solid black;">
[MS13-011](http://go.microsoft.com/fwlink/?linkid=271307)
</td>
<td style="border:1px solid black;">
[MS13-020](http://go.microsoft.com/fwlink/?linkid=279005)
</td>
<td style="border:1px solid black;">
[MS13-014](http://go.microsoft.com/fwlink/?linkid=276948)
</td>
<td style="border:1px solid black;">
[MS13-015](http://go.microsoft.com/fwlink/?linkid=275736)
</td>
<td style="border:1px solid black;">
[MS13-016](http://go.microsoft.com/fwlink/?linkid=275718)
</td>
<td style="border:1px solid black;">
[MS13-017](http://go.microsoft.com/fwlink/?linkid=278914)
</td>
<td style="border:1px solid black;">
[MS13-018](http://go.microsoft.com/fwlink/?linkid=278912)
</td>
<td style="border:1px solid black;">
[MS13-019](http://go.microsoft.com/fwlink/?linkid=278896)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
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
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
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
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=35b58c7a-aae3-4445-957a-42ee708d77a5)   
(KB2792100)  
(Moderada)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=3ee73b80-b8f6-4843-afba-41c7b55faf17)  
(KB2792100)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=d67754e2-7ebd-484d-a008-ed8719e0c72d)  
(KB2792100)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=9b96ebfc-93e9-41bb-81f9-35c433ca5479)   
(KB2797052)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=b902617d-1f35-4b17-9a44-235c0d3c27d2)  
(KB2797052)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=47ca5d22-b957-4ac9-91e9-c440b0614728)  
(KB2797052)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Quartz.dll (DirectShow)](http://www.microsoft.com/downloads/details.aspx?familyid=e3b0b928-0f76-4b51-871a-aeda2ee3b7d5)   
(KB2780091)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=eb202940-0ece-4631-83d5-8cf52c7dbf36)  
(KB2789643)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8daebdb5-eba2-4685-b781-ead5c2185548)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c005c0a0-4025-4a07-a76d-c57ed5afbd68)  
(KB2799494)    
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
Windows Server 2003 x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=075de724-b996-413f-8ff3-74f435d94b9b)   
(KB2792100)  
(Moderada)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=a90d6861-7ff6-4501-9200-f72b5a9f1817)  
(KB2792100)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=319a7a93-c03e-4c0b-a5c4-6a4f379d781e)  
(KB2792100)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=b3ca28b1-9d3c-4df5-b8d7-f31d70f6e714)   
(KB2797052)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=e13c9366-9cb6-4e62-bf6c-a09fe7842463)  
(KB2797052)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=80aab9c7-4511-4d44-b570-c77cdb50e542)  
(KB2797052)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Quartz.dll (DirectShow)](http://www.microsoft.com/downloads/details.aspx?familyid=493377a4-4ce2-4dd9-ba84-090466248669)   
(KB2780091)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=eb202940-0ece-4631-83d5-8cf52c7dbf36)  
(KB2789643)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e7d03ef2-517b-4442-a968-5aaa300dd2ba)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=dc004424-61f9-49ed-9cb3-b89ed9e98aef)  
(KB2799494)    
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
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=92ce1fa1-4b12-4fd5-9a02-21fc9b119fb9)   
(KB2792100)  
(Moderada)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=5965ce09-c5d7-4072-bad3-df46f9b76478)  
(KB2792100)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=63791740-00e2-4569-967e-36086efe6ca6)   
(KB2797052)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=d1a9b2b2-191c-4ffe-9c8a-8ef641a45eb7)  
(KB2797052)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Quartz.dll (DirectShow)](http://www.microsoft.com/downloads/details.aspx?familyid=8e9a09fd-f360-4471-ac89-481dc2935cec)   
(KB2780091)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=eb202940-0ece-4631-83d5-8cf52c7dbf36)  
(KB2789643)  
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=2a3039a4-9b46-4db8-a539-07d52bbf1b92)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=3cad66f1-6651-4948-9579-9df050fdaa1b)  
(KB2799494)    
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
<th colspan="11" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-009](http://go.microsoft.com/fwlink/?linkid=275670)
</td>
<td style="border:1px solid black;">
[MS13-010](http://go.microsoft.com/fwlink/?linkid=275837)
</td>
<td style="border:1px solid black;">
[MS13-011](http://go.microsoft.com/fwlink/?linkid=271307)
</td>
<td style="border:1px solid black;">
[MS13-020](http://go.microsoft.com/fwlink/?linkid=279005)
</td>
<td style="border:1px solid black;">
[MS13-014](http://go.microsoft.com/fwlink/?linkid=276948)
</td>
<td style="border:1px solid black;">
[MS13-015](http://go.microsoft.com/fwlink/?linkid=275736)
</td>
<td style="border:1px solid black;">
[MS13-016](http://go.microsoft.com/fwlink/?linkid=275718)
</td>
<td style="border:1px solid black;">
[MS13-017](http://go.microsoft.com/fwlink/?linkid=278914)
</td>
<td style="border:1px solid black;">
[MS13-018](http://go.microsoft.com/fwlink/?linkid=278912)
</td>
<td style="border:1px solid black;">
[MS13-019](http://go.microsoft.com/fwlink/?linkid=278896)
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
Ninguna
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Moderada](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=eea43429-2691-4a31-a640-d74035145d2d)  
(KB2792100)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=5c195229-8e63-4fff-a304-13c13b2fa132)  
(KB2792100)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=7f7ce868-28ce-497e-882f-3abfdd9b89e8)   
(KB2792100)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=4f946407-cd81-48b5-a279-1ab81388b70b)  
(KB2797052)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=e0cfc24f-293c-4817-a69c-f9cfd514e1c1)  
(KB2797052)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=4fab0417-5c9a-4e5d-864d-b1b3bee6fc89)   
(KB2797052)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Quartz.dll (DirectShow)](http://www.microsoft.com/downloads/details.aspx?familyid=d730eacf-e30a-45aa-89da-dfec5e87906a)   
(KB2780091)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b59753f0-b7cb-41c2-9c31-4f2de8356477)  
(KB2789646)   
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)    
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=b5cfc358-e5ff-445c-8d43-3f79fead6139)  
(KB2789648)   
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=0ff0475c-cc1b-4886-971e-1a71e6b311c3)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4de1249f-012e-47cb-ad08-4fd5bddb0879)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=80b766e7-3b7f-4d04-9a80-71864a13df8c)  
(KB2790655)    
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=308d99ff-7575-4d70-958f-0d57fd6bffab)  
(KB2792100)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=d9d4987e-95ad-4246-a52b-7ac859a40e67)  
(KB2792100)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=74b370c0-29f5-4acb-a3cd-bd2c2b708bb7)   
(KB2792100)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=6ffb3215-1c90-4eb2-9143-0866efc98374)  
(KB2797052)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=649dbf4e-654b-48a2-bd35-2df7f34fbb56)  
(KB2797052)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=44fbe00c-eeb4-4a80-a934-7ce58c02d6ec)   
(KB2797052)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Quartz.dll (DirectShow)](http://www.microsoft.com/downloads/details.aspx?familyid=4cd6b10c-b310-4aee-bbca-f23049c14455)   
(KB2780091)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b59753f0-b7cb-41c2-9c31-4f2de8356477)  
(KB2789646)   
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)    
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=b5cfc358-e5ff-445c-8d43-3f79fead6139)  
(KB2789648)   
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e5043a08-a9e4-422b-8455-80a5091d38b9)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=448ac43a-0a6f-4049-be2b-c853b5dbfab3)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=92bad797-5b66-422c-a096-8070d02bb8b2)  
(KB2790655)    
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="11" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-009](http://go.microsoft.com/fwlink/?linkid=275670)
</td>
<td style="border:1px solid black;">
[MS13-010](http://go.microsoft.com/fwlink/?linkid=275837)
</td>
<td style="border:1px solid black;">
[MS13-011](http://go.microsoft.com/fwlink/?linkid=271307)
</td>
<td style="border:1px solid black;">
[MS13-020](http://go.microsoft.com/fwlink/?linkid=279005)
</td>
<td style="border:1px solid black;">
[MS13-014](http://go.microsoft.com/fwlink/?linkid=276948)
</td>
<td style="border:1px solid black;">
[MS13-015](http://go.microsoft.com/fwlink/?linkid=275736)
</td>
<td style="border:1px solid black;">
[MS13-016](http://go.microsoft.com/fwlink/?linkid=275718)
</td>
<td style="border:1px solid black;">
[MS13-017](http://go.microsoft.com/fwlink/?linkid=278914)
</td>
<td style="border:1px solid black;">
[MS13-018](http://go.microsoft.com/fwlink/?linkid=278912)
</td>
<td style="border:1px solid black;">
[MS13-019](http://go.microsoft.com/fwlink/?linkid=278896)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
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
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=71c805ed-a68b-4d3e-97ca-922557cfbf67)  
(KB2792100)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=775ea105-4a71-4b7b-9dc0-50f1eecab96d)  
(KB2792100)  
(Moderada)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=ccdf8abc-9657-4aff-8d73-4824a558c168)   
(KB2792100)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=d432acb3-10a0-4f4c-a793-381aedd4bdd1)  
(KB2797052)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=b91ce04a-a464-4388-9386-54dd2815b8dd)  
(KB2797052)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=58f0810c-f253-4740-ac9f-75b8a4506b06)   
(KB2797052)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Quartz.dll (DirectShow)](http://www.microsoft.com/downloads/details.aspx?familyid=86cc3b51-818a-49a6-abab-488ac316e021)   
(KB2780091)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b59753f0-b7cb-41c2-9c31-4f2de8356477)  
(KB2789646)   
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)    
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=b5cfc358-e5ff-445c-8d43-3f79fead6139)  
(KB2789648)   
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=850e319f-dd6e-4480-86c3-a5129f084817)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6d7a74c8-de4b-4bcb-8b3f-581858d0776b)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c24aa6f3-82a5-4b1f-adc8-4aece948161c)  
(KB2790655)    
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=de1b96b7-a5ac-4a39-9808-c00c6b1a4325)  
(KB2792100)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=e5775802-e529-4894-b1cf-2839948706c2)  
(KB2792100)  
(Moderada)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=51df1e78-f014-4492-8a3d-83b3c821458b)   
(KB2792100)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=152f90b3-efae-42e6-a845-59052383a8a0)  
(KB2797052)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=304ac41e-b4e5-4bf8-94d2-f2bd9a07bcff)  
(KB2797052)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=7b85336a-d3f7-4077-b6eb-55b3042f5335)   
(KB2797052)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Quartz.dll (DirectShow)](http://www.microsoft.com/downloads/details.aspx?familyid=fe239f9b-d986-4828-a01d-8abd494037ec)   
(KB2780091)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b59753f0-b7cb-41c2-9c31-4f2de8356477)  
(KB2789646)   
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)    
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=b5cfc358-e5ff-445c-8d43-3f79fead6139)  
(KB2789648)   
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8978769b-447b-4b01-848a-cbcdf692f17a)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c9fbb7cc-c33b-4af9-8416-9d16015e79c1)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2738fbe4-2163-4e77-82e6-208a7a08a70c)  
(KB2790655)    
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=61c1964f-9307-4128-9470-bcb20e07856b)  
(KB2792100)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=1a2af9dc-e9a7-477e-9943-8132eb7fea81)  
(KB2797052)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Quartz.dll (DirectShow)](http://www.microsoft.com/downloads/details.aspx?familyid=4b3e48e3-0dbe-449b-9bca-0ba8bbdcbab0)   
(KB2780091)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 2.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b59753f0-b7cb-41c2-9c31-4f2de8356477)  
(KB2789646)   
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=0f84e24c-43f4-4851-932c-8849171b2505)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f3e18038-b8a1-4eba-9542-8396903a3709)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c269c175-f47c-456a-9360-f38bbdfd7ed0)  
(KB2790655)    
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="11" style="border:1px solid black;">
Windows 7
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-009](http://go.microsoft.com/fwlink/?linkid=275670)
</td>
<td style="border:1px solid black;">
[MS13-010](http://go.microsoft.com/fwlink/?linkid=275837)
</td>
<td style="border:1px solid black;">
[MS13-011](http://go.microsoft.com/fwlink/?linkid=271307)
</td>
<td style="border:1px solid black;">
[MS13-020](http://go.microsoft.com/fwlink/?linkid=279005)
</td>
<td style="border:1px solid black;">
[MS13-014](http://go.microsoft.com/fwlink/?linkid=276948)
</td>
<td style="border:1px solid black;">
[MS13-015](http://go.microsoft.com/fwlink/?linkid=275736)
</td>
<td style="border:1px solid black;">
[MS13-016](http://go.microsoft.com/fwlink/?linkid=275718)
</td>
<td style="border:1px solid black;">
[MS13-017](http://go.microsoft.com/fwlink/?linkid=278914)
</td>
<td style="border:1px solid black;">
[MS13-018](http://go.microsoft.com/fwlink/?linkid=278912)
</td>
<td style="border:1px solid black;">
[MS13-019](http://go.microsoft.com/fwlink/?linkid=278896)
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
Ninguna
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Moderada](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=4df9414b-02da-4254-ab29-5091151e2900)  
(KB2792100)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=b21bd7b3-2eb8-433a-b6c2-8243c5128038)   
(KB2792100)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=d7d64177-deec-4fd3-9716-b7816fe3c623)  
(KB2797052)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=04a101c6-d553-426f-b3cd-412eefeec580)   
(KB2797052)  
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
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=3b25dd48-053d-4d9e-9774-905c66c3aca9)  
(KB2789644)    
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=631adede-ba0f-461f-85e1-82b60a7efec1)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=912ac2e1-e737-43fb-acc8-a01a918a8475)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=cb4270c4-cec5-49e0-a56b-97539d6352a0)  
(KB2790655)    
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=d4d02ef9-b0a4-46a3-ad92-7508aa26ad3b)  
(KB2790113)    
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=4df9414b-02da-4254-ab29-5091151e2900)  
(KB2792100)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=b21bd7b3-2eb8-433a-b6c2-8243c5128038)   
(KB2792100)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=d7d64177-deec-4fd3-9716-b7816fe3c623)  
(KB2797052)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=04a101c6-d553-426f-b3cd-412eefeec580)   
(KB2797052)  
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
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=0da657e5-161d-46bc-a2b7-7c4696e37062)  
(KB2789645)    
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)    
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=b5cfc358-e5ff-445c-8d43-3f79fead6139)  
(KB2789648)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=631adede-ba0f-461f-85e1-82b60a7efec1)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=912ac2e1-e737-43fb-acc8-a01a918a8475)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=cb4270c4-cec5-49e0-a56b-97539d6352a0)  
(KB2790655)    
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d4d02ef9-b0a4-46a3-ad92-7508aa26ad3b)  
(KB2790113)    
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas x64
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=6ef9cbf9-d131-420d-b566-6b0f94f2e1c1)  
(KB2792100)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=4b2402ff-035a-47c4-b982-00d428eab379)   
(KB2792100)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=d503795a-b1a3-48dc-b1e6-27628aeb150a)  
(KB2797052)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=36eb59be-6703-40c0-b01c-0fffb1456719)   
(KB2797052)  
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
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=3b25dd48-053d-4d9e-9774-905c66c3aca9)  
(KB2789644)    
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=8dab3aca-fde1-4bd9-b82a-e4805a2e8d39)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=0d1601cc-fb76-4276-bf0b-a46b7f8055ae)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=5d93cb19-7854-4b49-9743-8d6a11be2dd6)  
(KB2790655)    
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=77277398-c5b4-4ba4-8425-465710b0bef2)  
(KB2790113)    
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=6ef9cbf9-d131-420d-b566-6b0f94f2e1c1)  
(KB2792100)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=4b2402ff-035a-47c4-b982-00d428eab379)   
(KB2792100)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=d503795a-b1a3-48dc-b1e6-27628aeb150a)  
(KB2797052)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=36eb59be-6703-40c0-b01c-0fffb1456719)   
(KB2797052)  
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
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=0da657e5-161d-46bc-a2b7-7c4696e37062)  
(KB2789645)    
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)    
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=b5cfc358-e5ff-445c-8d43-3f79fead6139)  
(KB2789648)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=8dab3aca-fde1-4bd9-b82a-e4805a2e8d39)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=0d1601cc-fb76-4276-bf0b-a46b7f8055ae)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5d93cb19-7854-4b49-9743-8d6a11be2dd6)  
(KB2790655)    
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=77277398-c5b4-4ba4-8425-465710b0bef2)  
(KB2790113)    
(Importante)
</td>
</tr>
<tr>
<th colspan="11" style="border:1px solid black;">
Windows Server 2008 R2
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-009](http://go.microsoft.com/fwlink/?linkid=275670)
</td>
<td style="border:1px solid black;">
[MS13-010](http://go.microsoft.com/fwlink/?linkid=275837)
</td>
<td style="border:1px solid black;">
[MS13-011](http://go.microsoft.com/fwlink/?linkid=271307)
</td>
<td style="border:1px solid black;">
[MS13-020](http://go.microsoft.com/fwlink/?linkid=279005)
</td>
<td style="border:1px solid black;">
[MS13-014](http://go.microsoft.com/fwlink/?linkid=276948)
</td>
<td style="border:1px solid black;">
[MS13-015](http://go.microsoft.com/fwlink/?linkid=275736)
</td>
<td style="border:1px solid black;">
[MS13-016](http://go.microsoft.com/fwlink/?linkid=275718)
</td>
<td style="border:1px solid black;">
[MS13-017](http://go.microsoft.com/fwlink/?linkid=278914)
</td>
<td style="border:1px solid black;">
[MS13-018](http://go.microsoft.com/fwlink/?linkid=278912)
</td>
<td style="border:1px solid black;">
[MS13-019](http://go.microsoft.com/fwlink/?linkid=278896)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Moderada](http://go.microsoft.com/fwlink/?linkid=21140)
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
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=e7b455a3-6a44-430c-a7d1-30c03ef7f141)  
(KB2792100)  
(Moderada)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=7e9d97f2-c006-4e5a-bc80-10450069b8c5)   
(KB2792100)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=7a36109b-f1e2-4cde-9ede-9f7449c5412c)  
(KB2797052)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=be2fd20a-4c37-47a6-a322-e16acd99db2c)   
(KB2797052)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=aadb2003-ed7b-46ee-afd0-33cec4ac39b4)  
(KB2790978)   
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=3b25dd48-053d-4d9e-9774-905c66c3aca9)  
(KB2789644)    
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=ca5a8735-1568-454d-8b4c-b83107eac036)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=201e6d1f-425b-406e-84a1-37cee035dddb)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=01284b28-043a-4e27-b363-c1e641164a01)  
(KB2790655)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=97241fdb-991d-4411-8fe1-ea56172360ab)  
(KB2790113)    
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=e7b455a3-6a44-430c-a7d1-30c03ef7f141)  
(KB2792100)  
(Moderada)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=7e9d97f2-c006-4e5a-bc80-10450069b8c5)   
(KB2792100)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=7a36109b-f1e2-4cde-9ede-9f7449c5412c)  
(KB2797052)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=be2fd20a-4c37-47a6-a322-e16acd99db2c)   
(KB2797052)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=aadb2003-ed7b-46ee-afd0-33cec4ac39b4)  
(KB2790978)    
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=0da657e5-161d-46bc-a2b7-7c4696e37062)  
(KB2789645)    
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)    
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=b5cfc358-e5ff-445c-8d43-3f79fead6139)  
(KB2789648)   
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=ca5a8735-1568-454d-8b4c-b83107eac036)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=201e6d1f-425b-406e-84a1-37cee035dddb)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=01284b28-043a-4e27-b363-c1e641164a01)  
(KB2790655)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=97241fdb-991d-4411-8fe1-ea56172360ab)  
(KB2790113)    
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=c1eb941e-833d-46f0-bf65-d9701d67bc20)  
(KB2792100)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=c2e1c1b3-5b75-47cf-91d5-82d413b358e6)  
(KB2797052)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=8e37196c-2f43-457d-8d87-336d8775c0bf)  
(KB2790978)    
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=3b25dd48-053d-4d9e-9774-905c66c3aca9)  
(KB2789644)    
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=99320f36-1481-446c-bc3e-d33fcfd1f2c1)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=9f0b132a-8616-49cd-8927-393f35d0cf21)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=e1be5dea-dd13-42b5-a37f-4bcd828cc65f)  
(KB2790655)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=9fbc37dd-53ec-4de1-b1c1-9761a8f83ab8)  
(KB2790113)    
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=c1eb941e-833d-46f0-bf65-d9701d67bc20)  
(KB2792100)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=c2e1c1b3-5b75-47cf-91d5-82d413b358e6)  
(KB2797052)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=8e37196c-2f43-457d-8d87-336d8775c0bf)  
(KB2790978)    
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=0da657e5-161d-46bc-a2b7-7c4696e37062)  
(KB2789645)    
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(KB2789642)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=99320f36-1481-446c-bc3e-d33fcfd1f2c1)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=9f0b132a-8616-49cd-8927-393f35d0cf21)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=e1be5dea-dd13-42b5-a37f-4bcd828cc65f)  
(KB2790655)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=9fbc37dd-53ec-4de1-b1c1-9761a8f83ab8)  
(KB2790113)    
(Importante)
</td>
</tr>
<tr>
<th colspan="11" style="border:1px solid black;">
Windows 8
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-009](http://go.microsoft.com/fwlink/?linkid=275670)
</td>
<td style="border:1px solid black;">
[MS13-010](http://go.microsoft.com/fwlink/?linkid=275837)
</td>
<td style="border:1px solid black;">
[MS13-011](http://go.microsoft.com/fwlink/?linkid=271307)
</td>
<td style="border:1px solid black;">
[MS13-020](http://go.microsoft.com/fwlink/?linkid=279005)
</td>
<td style="border:1px solid black;">
[MS13-014](http://go.microsoft.com/fwlink/?linkid=276948)
</td>
<td style="border:1px solid black;">
[MS13-015](http://go.microsoft.com/fwlink/?linkid=275736)
</td>
<td style="border:1px solid black;">
[MS13-016](http://go.microsoft.com/fwlink/?linkid=275718)
</td>
<td style="border:1px solid black;">
[MS13-017](http://go.microsoft.com/fwlink/?linkid=278914)
</td>
<td style="border:1px solid black;">
[MS13-018](http://go.microsoft.com/fwlink/?linkid=278912)
</td>
<td style="border:1px solid black;">
[MS13-019](http://go.microsoft.com/fwlink/?linkid=278896)
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
Ninguna
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Moderada](http://go.microsoft.com/fwlink/?linkid=21140)
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
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=7966de38-c6a6-4137-8b7e-8ccd3306521a)   
(KB2792100)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=0389b515-59bf-4733-aab4-ffb822efdbea)   
(KB2797052)  
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
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=639674a0-12a3-4185-9858-b2a31ed2f014)  
(KB2789650)    
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=27d83684-d4f7-4fe0-a54d-25a3d2009be0)  
(KB2789649)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=d5395864-1822-4151-a10c-f6a036f8853f)  
(KB2778344)    
(Sin clasificación de gravedad<sup>[2]</sup>)
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=5b74e5b3-7b8d-4669-b403-c776e70bf072)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=e7739ba6-9c62-4180-a095-47fdb6c741e9)  
(KB2790655)    
(Moderada)
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
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=d6720d21-269b-4605-b95e-573bc327afd9)   
(KB2792100)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=c1859853-d43f-4497-b212-e6a4daa43485)   
(KB2797052)  
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
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=639674a0-12a3-4185-9858-b2a31ed2f014)  
(KB2789650)    
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=27d83684-d4f7-4fe0-a54d-25a3d2009be0)  
(KB2789649)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 64 bits](http://www.microsoft.com/downloads/details.aspx?familyid=79aaaa3a-747a-4320-9fd2-5f4a6de3d13c)  
(KB2778344)    
(Sin clasificación de gravedad<sup>[2]</sup>)
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 64 bits](http://www.microsoft.com/downloads/details.aspx?familyid=a41a2b38-5e5c-48bc-8727-e19402519f12)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 64 bits](http://www.microsoft.com/downloads/details.aspx?familyid=dd2042b8-c784-4dfc-8fca-61905693cda5)  
(KB2790655)    
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="11" style="border:1px solid black;">
Windows Server 2012
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-009](http://go.microsoft.com/fwlink/?linkid=275670)
</td>
<td style="border:1px solid black;">
[MS13-010](http://go.microsoft.com/fwlink/?linkid=275837)
</td>
<td style="border:1px solid black;">
[MS13-011](http://go.microsoft.com/fwlink/?linkid=271307)
</td>
<td style="border:1px solid black;">
[MS13-020](http://go.microsoft.com/fwlink/?linkid=279005)
</td>
<td style="border:1px solid black;">
[MS13-014](http://go.microsoft.com/fwlink/?linkid=276948)
</td>
<td style="border:1px solid black;">
[MS13-015](http://go.microsoft.com/fwlink/?linkid=275736)
</td>
<td style="border:1px solid black;">
[MS13-016](http://go.microsoft.com/fwlink/?linkid=275718)
</td>
<td style="border:1px solid black;">
[MS13-017](http://go.microsoft.com/fwlink/?linkid=278914)
</td>
<td style="border:1px solid black;">
[MS13-018](http://go.microsoft.com/fwlink/?linkid=278912)
</td>
<td style="border:1px solid black;">
[MS13-019](http://go.microsoft.com/fwlink/?linkid=278896)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Moderada](http://go.microsoft.com/fwlink/?linkid=21140)
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
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
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
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=8e3fdcd0-ab75-4500-aac7-7ecb4f39fca7)   
(KB2792100)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=3b39813e-5ee2-412e-b1f1-a16617a70f43)   
(KB2797052)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=b284296a-1db5-47dc-af2c-bf55d0ad09e6)  
(KB2790978)   
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=639674a0-12a3-4185-9858-b2a31ed2f014)  
(KB2789650)    
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=27d83684-d4f7-4fe0-a54d-25a3d2009be0)  
(KB2789649)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=aac38d33-fad6-4060-bad4-61cf7c059af9)  
(KB2778344)    
(Sin clasificación de gravedad<sup>[2]</sup>)
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=4e427f56-436e-43d0-b4f8-eee8427b3741)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=f74a104d-4749-4dd5-b144-2e4ce9c284a2)  
(KB2790655)    
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="11" style="border:1px solid black;">
Windows RT
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-009](http://go.microsoft.com/fwlink/?linkid=275670)
</td>
<td style="border:1px solid black;">
[MS13-010](http://go.microsoft.com/fwlink/?linkid=275837)
</td>
<td style="border:1px solid black;">
[MS13-011](http://go.microsoft.com/fwlink/?linkid=271307)
</td>
<td style="border:1px solid black;">
[MS13-020](http://go.microsoft.com/fwlink/?linkid=279005)
</td>
<td style="border:1px solid black;">
[MS13-014](http://go.microsoft.com/fwlink/?linkid=276948)
</td>
<td style="border:1px solid black;">
[MS13-015](http://go.microsoft.com/fwlink/?linkid=275736)
</td>
<td style="border:1px solid black;">
[MS13-016](http://go.microsoft.com/fwlink/?linkid=275718)
</td>
<td style="border:1px solid black;">
[MS13-017](http://go.microsoft.com/fwlink/?linkid=278914)
</td>
<td style="border:1px solid black;">
[MS13-018](http://go.microsoft.com/fwlink/?linkid=278912)
</td>
<td style="border:1px solid black;">
[MS13-019](http://go.microsoft.com/fwlink/?linkid=278896)
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
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Moderada](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
Ninguna
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows RT
</td>
<td style="border:1px solid black;">
Internet Explorer 10<sup>[1]</sup>   
(KB2792100)  
(Crítica)
</td>
<td style="border:1px solid black;">
Internet Explorer 10<sup>[1]</sup>   
(KB2797052)  
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
Windows RT<sup>[1]</sup>
(KB2778344)  
(Sin clasificación de gravedad<sup>[2]</sup>)
</td>
<td style="border:1px solid black;">
Windows RT<sup>[1]</sup>
(KB2799494)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows RT<sup>[1]</sup>
(KB2790655)   
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="11" style="border:1px solid black;">
Opción de instalación Server Core
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-009](http://go.microsoft.com/fwlink/?linkid=275670)
</td>
<td style="border:1px solid black;">
[MS13-010](http://go.microsoft.com/fwlink/?linkid=275837)
</td>
<td style="border:1px solid black;">
[MS13-011](http://go.microsoft.com/fwlink/?linkid=271307)
</td>
<td style="border:1px solid black;">
[MS13-020](http://go.microsoft.com/fwlink/?linkid=279005)
</td>
<td style="border:1px solid black;">
[MS13-014](http://go.microsoft.com/fwlink/?linkid=276948)
</td>
<td style="border:1px solid black;">
[MS13-015](http://go.microsoft.com/fwlink/?linkid=275736)
</td>
<td style="border:1px solid black;">
[MS13-016](http://go.microsoft.com/fwlink/?linkid=275718)
</td>
<td style="border:1px solid black;">
[MS13-017](http://go.microsoft.com/fwlink/?linkid=278914)
</td>
<td style="border:1px solid black;">
[MS13-018](http://go.microsoft.com/fwlink/?linkid=278912)
</td>
<td style="border:1px solid black;">
[MS13-019](http://go.microsoft.com/fwlink/?linkid=278896)
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
Ninguna
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
Ninguna
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
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
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=850e319f-dd6e-4480-86c3-a5129f084817) (instalación Server Core)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6d7a74c8-de4b-4bcb-8b3f-581858d0776b) (instalación Server Core)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c24aa6f3-82a5-4b1f-adc8-4aece948161c) (instalación Server Core)  
(KB2790655)    
(Importante)
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
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=8978769b-447b-4b01-848a-cbcdf692f17a) (instalación Server Core)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c9fbb7cc-c33b-4af9-8416-9d16015e79c1) (instalación Server Core)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2738fbe4-2163-4e77-82e6-208a7a08a70c) (instalación Server Core)  
(KB2790655)    
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 (instalación Server Core)
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
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=aadb2003-ed7b-46ee-afd0-33cec4ac39b4)(instalación Server Core)  
(KB2790978)    
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=3b25dd48-053d-4d9e-9774-905c66c3aca9) (instalación Server Core)  
(KB2789644)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=ca5a8735-1568-454d-8b4c-b83107eac036)(instalación Server Core)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=201e6d1f-425b-406e-84a1-37cee035dddb)(instalación Server Core)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=01284b28-043a-4e27-b363-c1e641164a01)(instalación Server Core)  
(KB2790655)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=97241fdb-991d-4411-8fe1-ea56172360ab)(instalación Server Core)  
(KB2790113)    
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)
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
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=aadb2003-ed7b-46ee-afd0-33cec4ac39b4) (instalación Server Core)  
(KB2790978)    
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5.1](http://www.microsoft.com/downloads/details.aspx?familyid=0da657e5-161d-46bc-a2b7-7c4696e37062) (instalación Server Core)  
(KB2789645)    
(Importante)  
[Microsoft .NET Framework 4.0](http://www.microsoft.com/downloads/details.aspx?familyid=182f4d35-f18b-4485-be22-43becbd3cc05)<sup>[1]</sup>
(Instalación Server Core) (KB2789642)  
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=b5cfc358-e5ff-445c-8d43-3f79fead6139) (instalación Server Core)  
(KB2789648)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=ca5a8735-1568-454d-8b4c-b83107eac036) (instalación Server Core)  
(KB2778344)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=201e6d1f-425b-406e-84a1-37cee035dddb) (instalación Server Core)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=01284b28-043a-4e27-b363-c1e641164a01) (instalación Server Core)  
(KB2790655)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=97241fdb-991d-4411-8fe1-ea56172360ab) (instalación Server Core)  
(KB2790113)    
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012 (instalación Server Core)
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
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=b284296a-1db5-47dc-af2c-bf55d0ad09e6) (instalación Server Core)  
(KB2790978)   
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft .NET Framework 3.5](http://www.microsoft.com/downloads/details.aspx?familyid=639674a0-12a3-4185-9858-b2a31ed2f014) (instalación Server Core)  
(KB2789650)    
(Importante)  
[Microsoft .NET Framework 4.5](http://www.microsoft.com/downloads/details.aspx?familyid=27d83684-d4f7-4fe0-a54d-25a3d2009be0) (instalación Server Core)  
(KB2789649)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=aac38d33-fad6-4060-bad4-61cf7c059af9) (instalación Server Core)  
(KB2778344)    
(Sin clasificación de gravedad<sup>[2]</sup>)
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=4e427f56-436e-43d0-b4f8-eee8427b3741) (instalación Server Core)  
(KB2799494)    
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=f74a104d-4749-4dd5-b144-2e4ce9c284a2) (instalación Server Core)  
(KB2790655)    
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
Notas para MS13-009, MS13-010, MS13-017 y MS13-018

<sup>[1]</sup>Las actualizaciones de seguridad de Windows RT se proporcionan a través de [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130).

Notas para MS13-015

<sup>[1]</sup>.NET Framework 4 y .NET Framework 4 Client Profile están afectados. Los paquetes redistribuibles de .NET Framework versión 4 están disponibles en dos perfiles: .NET Framework 4.0 y .NET Framework 4.0 Client Profile. .NET Framework 4.0 Client Profile es un subconjunto de .NET Framework 4.0. La vulnerabilidad corregida en esta actualización afecta a .NET Framework 4.0 y .NET Framework 4.0 Client Profile. Para obtener más información, vea el artículo de MSDN [Instalar .NET Framework](http://msdn.microsoft.com/en-us/library/5a4x27ek.aspx).

Notas para MS13-016

<sup>[1]</sup>Las actualizaciones de seguridad de Windows RT se proporcionan a través de [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130).

<sup>[2]</sup>Las clasificaciones de gravedad no se aplican a esta actualización para el software especificado. No obstante, como medida de defensa en profundidad, Microsoft recomienda que los clientes de este software apliquen esta actualización de seguridad.

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
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-012](http://go.microsoft.com/fwlink/?linkid=279801)
</td>
<td style="border:1px solid black;">
[MS13-013](http://go.microsoft.com/fwlink/?linkid=272434)
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
Ninguna
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Exchange Server 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Exchange Server 2007 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=316a1aff-b72d-4d96-8ee5-bd86b0e29e6f)   
(KB2788321)   
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Exchange Server 2010 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft Exchange Server 2010 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=498e7612-73b5-4e28-99a4-b3157ac69932)   
(KB2746164)   
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft FAST Search Server 2010 for SharePoint
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-012](http://go.microsoft.com/fwlink/?linkid=279801)
</td>
<td style="border:1px solid black;">
[MS13-013](http://go.microsoft.com/fwlink/?linkid=272434)
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
Microsoft FAST Search Server 2010 para SharePoint Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Advanced Filter Pack](http://www.microsoft.com/downloads/details.aspx?familyid=0ae86754-69a8-4c82-855c-2ee2b7887fa5)<sup>[1]</sup>   
(KB2553234)  
(Importante)
</td>
</tr>
</table>
 
Nota para MS13-013

<sup>[1]</sup>Esta actualización solo está disponible en el Centro de descarga de Microsoft.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

Central de seguridad

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/bb245732). [TechNet Security TechCenter](http://technet.microsoft.com/es-es/security/) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar el [Centro de seguridad y protección de Microsoft](http://www.microsoft.com/es-es/security/default.aspx), donde esta información también está disponible haciendo clic en "Actualizaciones de seguridad".

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

-   Masato Kinugawa, por informar de un problema descrito en MS13-009
-   [Omair](http://krash.in/)
-   , en colaboración con
-   [Zero Day Initiative](http://www.zerodayinitiative.com/)
-   de
-   [HP](http://www.hpenterprisesecurity.com/products)
-   , por informar de dos problemas descritos en MS13-009
-   SkyLined, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de un problema descrito en MS13-009
-   Arthur Gerkis, en colaboración con Exodus Intelligence, por informar de un problema descrito en MS13-009
-   Stephen Fewer, de [Harmony Security](http://www.harmonysecurity.com), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de dos problemas descritos en MS13-009
-   [Aniway.Aniway@gmail.com](mailto:aniway.aniway@gmail.com)
-   , en colaboración con
-   [Zero Day Initiative](http://www.zerodayinitiative.com/)
-   de
-   [HP](http://www.hpenterprisesecurity.com/products)
-   , por informar de un problema descrito en MS13-009
-   Tencent PC Manager, por informar de un problema descrito en MS13-009
-   Arthur Gerkis, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de un problema descrito en MS13-009
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de un problema descrito en MS13-009
-   Scott Bell, de [Security-Assessment.com](http://www.security-assessment.com), por informar de dos problemas descritos en MS13-009
-   José A. Vázquez, de Yenteasy Security Research, en colaboración con Exodus Intelligence, por informar de un problema descrito en MS13-009
-   José A. Vázquez, de Yenteasy Security Research, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de un problema descrito en MS13-009
-   Mark Yason, de IBM X-Force, por informar de un problema descrito en MS13-009
-   Ollie Whitehouse, de [NCC Group](http://www.nccgroup.com/), por colaborar con nosotros en los cambios de defensa adicionales incluidos en MS13-009
-   [Tencent Security Team](http://security.tencent.com/)
-   , por informar por informar de un problema descrito en MS13-011
-   James Forshaw, de [Context Information Security](http://www.contextis.com/), por informar de un problema descrito en MS13-015
-   [Mateusz "j00ru" Jurczyk](http://j00ru.vexillium.org/)
-   , de
-   [Google Inc](http://www.google.com)
-   , y
-   [Tencent Security Team](http://security.tencent.com/)
-   , por informar de un problema descrito en MS13-016
-   [Mateusz "j00ru" Jurczyk](http://j00ru.vexillium.org/)
-   , de
-   [Google Inc](http://www.google.com/)
-   , por informar de 25 problemas descritos en MS13-016
-   [Gynvael Coldwind](http://gynvael.coldwind.pl/)
-   y
-   [Mateusz "j00ru" Jurczyk](http://j00ru.vexillium.org/)
-   , de
-   [Google Inc](http://www.google.com)
-   , por informar de tres problemas descritos en MS13-016
-   [Gynvael Coldwind](http://gynvael.coldwind.pl/)
-   y
-   [Mateusz "j00ru" Jurczyk](http://j00ru.vexillium.org/)
-   , de
-   [Google Inc](http://www.google.com)
-   , por informar de dos problemas descritos en MS13-017
-   Max DeLiso, por colaborar con nosotros en un problema descrito en MS13-019
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de un problema descrito en MS13-020

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Soluciones de seguridad para profesionales de TI: [Soporte técnico y solución de problemas de seguridad de TechNet](http://technet.microsoft.com/es-es/security/bb980617.aspx)
-   Ayuda para proteger su equipo con Windows de virus y malware: [Solución antivirus y centro de seguridad](http://support.microsoft.com/contactus/cu_sc_virsec_master)
-   Soporte local según su país: [Soporte internacional](http://support.microsoft.com/common/international.aspx)

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (12 de febrero de 2013): Publicación del resumen del boletín.
-   V1.1 (12 de febrero de 2013): para MS13-009, se ha corregido la evaluación de explotabilidad correspondiente a la última versión de software en Índice de explotabilidad para CVE-2013-0022.
-   V1.2 (13 de febrero de 2013): para MS13-014, se ha corregido la evaluación de explotabilidad correspondiente a la última versión de software en Índice de explotabilidad para CVE-2013-1281.

*Built at 2014-04-18T01:50:00Z-07:00*
