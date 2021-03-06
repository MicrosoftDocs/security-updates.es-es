---
TOCTitle: 'MS12-DEC'
Title: Resumen del boletín de seguridad de Microsoft de diciembre 2012
ms:assetid: 'ms12-dec'
ms:contentKeyID: 61225434
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms12-dec(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de diciembre 2012
===============================================================

Publicado: martes, 11 de diciembre de 2012 | Actualizado: jueves, 20 de diciembre de 2012

**Versión:** 2.0

Este resumen del boletín enumera los boletines de seguridad publicados para diciembre de 2012.

Con la publicación de los boletines de seguridad de diciembre de 2012, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 6 de diciembre de 2012. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 12 de diciembre de 2012, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de diciembre](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032522564&culture=en-us). Después de esta fecha, este webcast estará disponible [a petición](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032522564&culture=en-us).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información adicional**.

### Información del boletín

#### Resúmenes ejecutivos

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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-077">MS12-077</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (2761465)  <br />
<br />
</strong>Esta actualización de seguridad resuelve tres vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. La más grave de las vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un intruso que aprovechara estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows, <br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-078">MS12-078</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en los controladores en modo</strong> <strong>kernel</strong> <strong>de Windows</strong> <strong>podrían</strong> <strong>permitir la ejecución remota de código<br />
(2783534)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un usuario abre un documento especialmente diseñado o visita una página web malintencionada que inserta archivos de fuentes TrueType u OpenType. Tendría que atraerlos al sitio web; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico que lleve a los usuarios al sitio web del atacante.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-079">MS12-079</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Word podría permitir la ejecución remota de código (2780642)  <br />
<br />
</strong>Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Office. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo RTF especialmente diseñado con una versión afectada del software de Microsoft Office o bien obtiene una vista previa o abre un mensaje de correo electrónico RTF especialmente diseñado en Outlook con Microsoft Word como el visor de correo electrónico. Un atacante que aprovechara la vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-080">MS12-080</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en Microsoft Exchange</strong> <strong>Server</strong> <strong>podrían</strong> <strong>permitir la ejecución remota de código (2784126)  <br />
<br />
</strong>Esta actualización de seguridad resuelve vulnerabilidades de las que se ha informado de forma pública y una vulnerabilidad de la que se ha informado de forma privada en Microsoft Exchange Server. Las vulnerabilidades más graves se encuentran en Microsoft Exchange Server WebReady Document Viewing y podrían permitir la ejecución remota de código en el contexto de seguridad del servicio de transcodificación en el servidor Exchange si un usuario obtiene una vista previa de un archivo especialmente diseñado mediante Outlook Web App (OWA). El servicio de transcodificación de Exchange que se usa para WebReady Document Viewing se ejecuta en la cuenta LocalService. La cuenta LocalService tiene privilegios mínimos en el equipo local y presenta credenciales anónimas en la red.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Software de servidor de Microsoft</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-081">MS12-081</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el componente de tratamiento de archivos de Windows podría permitir la ejecución remota de código (2758857)  <br />
<br />
</strong>Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario explora una carpeta que contiene un archivo o una subcarpeta con un nombre especialmente diseñado. Un atacante que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-082">MS12-082</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en</strong> <strong>DirectPlay</strong> <strong>podría permitir la ejecución remota de código (2770660)  <br />
<br />
</strong>Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un atacante consigue convencer a un usuario para que vea un documento de Office especialmente diseñado con contenido incrustado. Un atacante que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-083">MS12-083</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el componente IP-HTTPS podría permitir la omisión de característica de seguridad (2765809)  <br />
<br />
</strong>Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la omisión de característica de seguridad si un atacante presenta un certificado revocado a un servidor IP-HTTPS usado de forma habitual en las implementaciones de Microsoft DirectAccess. Para aprovechar la vulnerabilidad, el atacante debe usar un certificado que haya emitido el dominio para la autenticación del servidor IP-HTTPS. Para el inicio de sesión en un sistema interno de la organización seguiría siendo necesario contar con credenciales del sistema o del dominio.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Omisión de característica de seguridad</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y, a continuación, por identificador de CVE. Sólo se incluyen las vulnerabilidades que tiene una clasificación de gravedad de crítica o importante en los boletines.
  
**¿Cómo se usa esta tabla?**  
  
Use esta tabla para obtener información acerca de la probabilidad de las vulnerabilidades de ejecución de código y de denegación de servicio en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Revise cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación de las actualizaciones de este mes. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/es-es/security/cc998259).
  
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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-077">MS12-077</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de InjectHTMLStream después de la liberación</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-4781">CVE-2012-4781</a></td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-077">MS12-077</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de CMarkup después de la liberación</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-4782">CVE-2012-4782</a></td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-077">MS12-077</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso del recuento de referencia incorrecto después de la liberación</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-4787">CVE-2012-4787</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-078">MS12-078</a></td>
<td style="border:1px solid black;">Vulnerabilidad de análisis de fuentes OpenType</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-2556">CVE-2012-2556</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Esta vulnerabilidad ya se ha divulgado públicamente.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-078">MS12-078</a></td>
<td style="border:1px solid black;">Vulnerabilidad de análisis de fuentes TrueType</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-4786">CVE-2012-4786</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-079">MS12-079</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código &quot;listoverridecount&quot; de RTF en Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-2539">CVE-2012-2539</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-080">MS12-080</a></td>
<td style="border:1px solid black;">Oracle Outside In contiene varias vulnerabilidades que se pueden aprovechar</td>
<td style="border:1px solid black;">Varias*</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">*Varias vulnerabilidades, vea el boletín MS12-080 para obtener detalles.<br />
<br />
Estas vulnerabilidades se han divulgado de forma pública.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-080">MS12-080</a></td>
<td style="border:1px solid black;">Vulnerabilidad de denegación de servicio en Exchange provocada por la fuente RSS</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-4791">CVE-2012-4791</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-081">MS12-081</a></td>
<td style="border:1px solid black;">Vulnerabilidad de análisis de nombres de archivo en Windows</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-4774">CVE-2012-4774</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-082">MS12-082</a></td>
<td style="border:1px solid black;">Vulnerabilidad de desbordamiento del montón en DirectPlay</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1537">CVE-2012-1537</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-083">MS12-083</a></td>
<td style="border:1px solid black;">Vulnerabilidad de omisión de certificado revocado</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-2549">CVE-2012-2549</a></td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Es una vulnerabilidad de omisión de característica de seguridad.</td>
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
<th colspan="6" style="border:1px solid black;">
Windows XP  
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-077**](http://go.microsoft.com/fwlink/?linkid=268393)
</td>
<td style="border:1px solid black;">
[**MS12-078**](http://go.microsoft.com/fwlink/?linkid=271624)
</td>
<td style="border:1px solid black;">
[**MS12-081**](http://go.microsoft.com/fwlink/?linkid=266541)
</td>
<td style="border:1px solid black;">
[**MS12-082**](http://go.microsoft.com/fwlink/?linkid=271751)
</td>
<td style="border:1px solid black;">
[**MS12-083**](http://go.microsoft.com/fwlink/?linkid=263950)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**
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
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=e39c8368-9cd3-4f29-8c9c-aa784122bef0)   
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=d1881d12-2a40-4cb1-9428-31d6633746be)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=8359ec5a-07f8-4b29-8576-7356a84daf82)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=e4a2cd3b-598b-4cf4-8b42-2582d369bab5)  
(KB2753842)  
(Crítica)  
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=7a7a68cf-42a2-49a4-bf0c-88dd582ddd0d)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=f189ee1c-1457-4d50-87cd-5be268b04f16)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=98ceaf36-ef87-4ea3-8b73-bb0a1a624fe0)  
(KB2770660)  
(Importante)
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
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=ed2d3c6e-b90a-49a7-867e-9549b14eb0bf)   
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=18e165e9-346b-4337-81d2-77f3bf5f5f3f)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=5d0a76e1-80d3-4f81-be5e-8d235babaa61)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=27e6c4df-7988-4d03-b2f6-bc9ce37483f9)  
(KB2753842)  
(Crítica)  
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d2a59846-74fd-4166-9d65-1cc98cb7d934)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2bf25fc8-6458-4807-bb7d-1c07ec424638)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=421b0c02-e572-4362-b690-73ad63b028de)  
(KB2770660)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
[**MS12-077**](http://go.microsoft.com/fwlink/?linkid=268393)
</td>
<td style="border:1px solid black;">
[**MS12-078**](http://go.microsoft.com/fwlink/?linkid=271624)
</td>
<td style="border:1px solid black;">
[**MS12-081**](http://go.microsoft.com/fwlink/?linkid=266541)
</td>
<td style="border:1px solid black;">
[**MS12-082**](http://go.microsoft.com/fwlink/?linkid=271751)
</td>
<td style="border:1px solid black;">
[**MS12-083**](http://go.microsoft.com/fwlink/?linkid=263950)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**
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
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=478f4789-0f5e-4bfb-9536-94314f84f12c)   
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=5ca71c15-0add-45cd-991f-e5810791c434)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=0157c9ee-58c5-419f-ba97-6c4334318b75)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=efe4755b-3bc4-4a65-9826-7ecaa3856093)  
(KB2753842)  
(Crítica)  
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=74847cb5-a092-4818-bf7a-912ccaed7a12)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2242a927-cafb-41eb-8bf2-01302b5a5d94)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1b487137-8b5a-4f22-8395-f3fc4f25f00b)  
(KB2770660)  
(Importante)
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
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=66b552b4-8b55-45de-ba0a-940dc24e6f56)   
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=e9fb2cf9-3acb-48ac-80ac-f61f1a47a188)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=23c4962c-8526-4e18-9b8d-50f3c3a2bf6d)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=019d80e2-7622-4951-9437-5d613c5fb2fb)  
(KB2753842)  
(Crítica)  
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b0c9df15-857f-490a-96df-3883a11c3234)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4d97b0a5-1ba7-44f0-88b6-1e0a8039b9b1)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=39d79b5b-f11c-465a-8ddd-aecb571c711f)  
(KB2770660)  
(Importante)
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
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=890d1149-7bb3-4d6e-a4ce-f9116c658eda)   
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=d8025298-be72-4ef2-8914-7698494f4368)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=419b9fd2-dbe6-45b5-b025-9712bb9319d6)  
(KB2753842)  
(Crítica)  
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=323c122b-be77-45e9-805d-ab14f5cc76f9)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=e74713fd-e1bc-4a63-9a00-2f33000eac27)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=312975f6-2269-4c6f-996b-8fb04e8c08d6)  
(KB2770660)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
[**MS12-077**](http://go.microsoft.com/fwlink/?linkid=268393)
</td>
<td style="border:1px solid black;">
[**MS12-078**](http://go.microsoft.com/fwlink/?linkid=271624)
</td>
<td style="border:1px solid black;">
[**MS12-081**](http://go.microsoft.com/fwlink/?linkid=266541)
</td>
<td style="border:1px solid black;">
[**MS12-082**](http://go.microsoft.com/fwlink/?linkid=271751)
</td>
<td style="border:1px solid black;">
[**MS12-083**](http://go.microsoft.com/fwlink/?linkid=263950)
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
**Ninguna**
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=3701a40d-e423-4204-9527-26e527f47fb0)   
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=394963e9-edd6-4b5d-b9d4-e6fb86d7eb54)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=bd3a6f9b-7bfd-40e1-9393-a125030f2964)  
(KB2761465)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=0cadef72-625f-4c91-8289-c10a96bb3423)  
(KB2753842)  
(Crítica)  
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=f2854a4e-2597-49ab-8a85-715ea9194208)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ebd25f89-e6d9-4c48-a673-f665d189905c)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=cd60c749-bb24-4147-9699-a1a75939a28f)  
(KB2770660)  
(Importante)
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
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=2856c7b8-d5c0-444d-8273-5bd116f8898b)   
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=7a0c6dbd-e537-43d7-97cc-0d3df354e46a)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=482fadb3-0974-40f3-af35-f29210913c81)  
(KB2761465)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=dd5eb06a-c805-4518-a784-5e29d7636037)  
(KB2753842)  
(Crítica)  
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b6baf170-65b0-4068-b2a0-196c3e4b3aed)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e7629d85-5c18-4979-a8e2-054a6175cf21)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[](http://www.microsoft.com/downloads/details.aspx?familyid=?...?)[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=d6f2c1d9-b775-48a0-b154-cf61b1e2674c)</a>
(KB2770660)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
[**MS12-077**](http://go.microsoft.com/fwlink/?linkid=268393)
</td>
<td style="border:1px solid black;">
[**MS12-078**](http://go.microsoft.com/fwlink/?linkid=271624)
</td>
<td style="border:1px solid black;">
[**MS12-081**](http://go.microsoft.com/fwlink/?linkid=266541)
</td>
<td style="border:1px solid black;">
[**MS12-082**](http://go.microsoft.com/fwlink/?linkid=271751)
</td>
<td style="border:1px solid black;">
[**MS12-083**](http://go.microsoft.com/fwlink/?linkid=263950)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=a4824a10-4011-4ce5-9454-693d42acddf3)   
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=e3d584f5-fc25-4e66-a911-4595018c51e3)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=ffff647e-8d05-4c77-aea6-542ab8d76c57)  
(KB2761465)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9a51b84d-2200-42c5-a6ab-4d570fa20609)  
(KB2753842)  
(Crítica)  
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=bdad28e8-987e-492e-a405-b3be552d2d7a)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ced1ffc6-7d30-480a-a3e0-8071981d1863)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=20ffdbfd-c786-41ca-9367-d7499108d711)  
(KB2770660)  
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
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=750797e5-1da7-49a9-8c27-ff35fe7516a1)   
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=ca4a5972-faec-412a-b51a-130253cebcab)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=8f22603d-3a0d-49da-9691-671c0c950867)  
(KB2761465)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9c60014b-133e-455e-b03f-d73f6e36d3de)  
(KB2753842)  
(Crítica)  
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6298d55c-2ed2-4a90-9dfe-43bae0932e27)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b9a687e6-9ab7-4dae-9771-5f7bb3123e06)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=cfeb7a06-5812-4a49-b69b-88be06d63d71)  
(KB2770660)  
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
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=4d49cd73-feea-44c7-86f2-048dd69233a4)   
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=68e6d5c4-cb20-4291-8864-4270db36ead0)  
(KB2753842)  
(Crítica)  
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2293a5fb-4a1c-41d9-ab67-b89e00078029)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=202b3919-0075-4c54-a189-123de852fc7b)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=0345e31f-6d0d-4d46-8f02-8b2ffbf795f0)  
(KB2770660)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
[**MS12-077**](http://go.microsoft.com/fwlink/?linkid=268393)
</td>
<td style="border:1px solid black;">
[**MS12-078**](http://go.microsoft.com/fwlink/?linkid=271624)
</td>
<td style="border:1px solid black;">
[**MS12-081**](http://go.microsoft.com/fwlink/?linkid=266541)
</td>
<td style="border:1px solid black;">
[**MS12-082**](http://go.microsoft.com/fwlink/?linkid=271751)
</td>
<td style="border:1px solid black;">
[**MS12-083**](http://go.microsoft.com/fwlink/?linkid=263950)
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
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=5b461a22-6ca4-4ab9-8874-84d7928cc668)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=38b15264-1a1d-41a6-8803-2d3facdb2dc3)   
(KB2761465)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=d1894fc3-603a-4a94-9e27-e1c564688294)  
(KB2753842)  
(Crítica)  
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=48f7d41e-f1c4-428d-9889-543fcb1e272b)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=cdaae723-6287-4607-9dc2-c23e1fb31f80)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=27e57b08-8616-4eb3-9724-3647e6841296)  
(KB2770660)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=5b461a22-6ca4-4ab9-8874-84d7928cc668)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=38b15264-1a1d-41a6-8803-2d3facdb2dc3)   
(KB2761465)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d1894fc3-603a-4a94-9e27-e1c564688294)  
(KB2753842)  
(Crítica)  
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=48f7d41e-f1c4-428d-9889-543fcb1e272b)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=cdaae723-6287-4607-9dc2-c23e1fb31f80)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=27e57b08-8616-4eb3-9724-3647e6841296)  
(KB2770660)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas x64
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=d19dfe38-77ef-4479-b3d9-8f6385ddee80)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=7accb5a9-98a1-4358-90ba-534d197885c1)   
(KB2761465)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=d7b5c43d-b659-4843-8944-62bf52738bbc)  
(KB2753842)  
(Crítica)  
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=ae9f0c19-169b-4bcd-92f7-654b84bab01f)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=4a389411-bf52-4cb2-9051-ba7344b58474)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=5f7c21b9-7dd3-4b9f-84af-1450af6c7ee3)  
(KB2770660)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=d19dfe38-77ef-4479-b3d9-8f6385ddee80)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=7accb5a9-98a1-4358-90ba-534d197885c1)   
(KB2761465)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d7b5c43d-b659-4843-8944-62bf52738bbc)  
(KB2753842)  
(Crítica)  
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=ae9f0c19-169b-4bcd-92f7-654b84bab01f)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=4a389411-bf52-4cb2-9051-ba7344b58474)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=5f7c21b9-7dd3-4b9f-84af-1450af6c7ee3)  
(KB2770660)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
[**MS12-077**](http://go.microsoft.com/fwlink/?linkid=268393)
</td>
<td style="border:1px solid black;">
[**MS12-078**](http://go.microsoft.com/fwlink/?linkid=271624)
</td>
<td style="border:1px solid black;">
[**MS12-081**](http://go.microsoft.com/fwlink/?linkid=266541)
</td>
<td style="border:1px solid black;">
[**MS12-082**](http://go.microsoft.com/fwlink/?linkid=271751)
</td>
<td style="border:1px solid black;">
[**MS12-083**](http://go.microsoft.com/fwlink/?linkid=263950)
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=8968122d-d3b9-404e-ba23-846be9041e3f)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=14bd26c2-b006-4465-88cc-4ecdc5de540f)   
(KB2761465)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=fedee43c-0065-42bf-9714-171b5b74f099)  
(KB2753842)  
(Crítica)  
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=3dfa40ef-86a2-44a0-b523-f4a85c7ac82c)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=9e06181f-de06-423b-bbeb-df1f451fb817)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=efe0d293-9cfb-46cb-b52e-0b90bde3f8e9)  
(KB2770660)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=d3fb096b-87b5-4715-a093-9ec9b021a40f)  
(KB2765809)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=8968122d-d3b9-404e-ba23-846be9041e3f)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=14bd26c2-b006-4465-88cc-4ecdc5de540f)   
(KB2761465)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=fedee43c-0065-42bf-9714-171b5b74f099)  
(KB2753842)  
(Crítica)  
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=3dfa40ef-86a2-44a0-b523-f4a85c7ac82c)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=9e06181f-de06-423b-bbeb-df1f451fb817)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=efe0d293-9cfb-46cb-b52e-0b90bde3f8e9)  
(KB2770660)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d3fb096b-87b5-4715-a093-9ec9b021a40f)  
(KB2765809)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=9191365d-5541-4277-9079-f4e72e98fd19)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=f26098f5-6b6c-48f9-8737-345ad4956cb0)  
(KB2753842)  
(Crítica)  
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=51b562f4-8b1a-416e-88dc-93b561ad850a)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=2a0a6f92-c4bf-45a3-b103-b7937121b675)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=33096b07-bfa3-4879-b214-dfa81cd73cae)  
(KB2770660)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=88a3452c-b416-41cf-867a-fdc64666c0a6)  
(KB2765809)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=9191365d-5541-4277-9079-f4e72e98fd19)  
(KB2761465)  
(Sin clasificación de gravedad<sup>[1]</sup>)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=f26098f5-6b6c-48f9-8737-345ad4956cb0)  
(KB2753842)  
(Crítica)  
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=51b562f4-8b1a-416e-88dc-93b561ad850a)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=2a0a6f92-c4bf-45a3-b103-b7937121b675)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=33096b07-bfa3-4879-b214-dfa81cd73cae)  
(KB2770660)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=88a3452c-b416-41cf-867a-fdc64666c0a6)  
(KB2765809)  
(Importante)
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Windows 8
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador** **del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-077**](http://go.microsoft.com/fwlink/?linkid=268393)
</td>
<td style="border:1px solid black;">
[**MS12-078**](http://go.microsoft.com/fwlink/?linkid=271624)
</td>
<td style="border:1px solid black;">
[**MS12-081**](http://go.microsoft.com/fwlink/?linkid=266541)
</td>
<td style="border:1px solid black;">
[**MS12-082**](http://go.microsoft.com/fwlink/?linkid=271751)
</td>
<td style="border:1px solid black;">
[**MS12-083**](http://go.microsoft.com/fwlink/?linkid=263950)
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
**Ninguna**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=28fb32a1-12fd-420d-94ff-570742a02b8d)  
(KB2761465)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=385265c4-f920-4ac1-b474-a166b3d3ab42)  
(KB2753842)  
(Crítica)  
[Windows 8 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=75969782-d3f8-40dd-8922-4408eefad6f3)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=15f86dbf-d8db-445c-8996-cc789c8a894d)  
(KB2770660)  
(Importante)
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
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=ad0ee30f-b550-434b-9fe0-ff418e052d3f)  
(KB2761465)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 64 bits](http://www.microsoft.com/downloads/details.aspx?familyid=543af274-d6cf-4f85-a120-b7f3936d7fc2)  
(KB2753842)  
(Crítica)  
[Windows 8 para sistemas de 64 bits](http://www.microsoft.com/downloads/details.aspx?familyid=2332059d-30d3-4b44-b172-f054e26d8971)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 8 para sistemas de 64 bits](http://www.microsoft.com/downloads/details.aspx?familyid=dfdda0c8-a440-49ab-832b-cdd343c57770)  
(KB2770660)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Windows Server 2012
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-077**](http://go.microsoft.com/fwlink/?linkid=268393)
</td>
<td style="border:1px solid black;">
[**MS12-078**](http://go.microsoft.com/fwlink/?linkid=271624)
</td>
<td style="border:1px solid black;">
[**MS12-081**](http://go.microsoft.com/fwlink/?linkid=266541)
</td>
<td style="border:1px solid black;">
[**MS12-082**](http://go.microsoft.com/fwlink/?linkid=271751)
</td>
<td style="border:1px solid black;">
[**MS12-083**](http://go.microsoft.com/fwlink/?linkid=263950)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
**Ninguna**
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
Windows Server 2012
</td>
<td style="border:1px solid black;">
[Internet Explorer 10](http://www.microsoft.com/downloads/details.aspx?familyid=96fda694-876a-45e9-911a-b68b3bd03290)  
(KB2761465)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=15298129-8f1c-47d7-a7e9-efb40823d91a)  
(KB2753842)  
(Crítica)  
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=f8e84ff9-a9c0-4363-b5a6-1b90254edd73)  
(KB2779030)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=59be5ec7-df5a-4f01-8e27-ad76f1fe76bb)  
(KB2770660)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=d6654bf1-1ab9-4691-8729-793eb6d0e563)  
(KB2765809)  
(Importante)
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Windows RT
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-077**](http://go.microsoft.com/fwlink/?linkid=268393)
</td>
<td style="border:1px solid black;">
[**MS12-078**](http://go.microsoft.com/fwlink/?linkid=271624)
</td>
<td style="border:1px solid black;">
[**MS12-081**](http://go.microsoft.com/fwlink/?linkid=266541)
</td>
<td style="border:1px solid black;">
[**MS12-082**](http://go.microsoft.com/fwlink/?linkid=271751)
</td>
<td style="border:1px solid black;">
[**MS12-083**](http://go.microsoft.com/fwlink/?linkid=263950)
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
**Ninguna**
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows RT
</td>
<td style="border:1px solid black;">
Internet Explorer 10<sup>[2]</sup>
(KB2761465)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows RT<sup>[1]</sup>
(KB2753842)  
(Crítica)  
Windows RT<sup>[1]</sup>
(KB2779030)  
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
<th colspan="6" style="border:1px solid black;">
Opción de instalación Server Core
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador** **del** **boletín**
</td>
<td style="border:1px solid black;">
[**MS12-077**](http://go.microsoft.com/fwlink/?linkid=268393)
</td>
<td style="border:1px solid black;">
[**MS12-078**](http://go.microsoft.com/fwlink/?linkid=271624)
</td>
<td style="border:1px solid black;">
[**MS12-081**](http://go.microsoft.com/fwlink/?linkid=266541)
</td>
<td style="border:1px solid black;">
[**MS12-082**](http://go.microsoft.com/fwlink/?linkid=271751)
</td>
<td style="border:1px solid black;">
[**MS12-083**](http://go.microsoft.com/fwlink/?linkid=263950)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
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
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9a51b84d-2200-42c5-a6ab-4d570fa20609) (instalación Server Core)  
(KB2753842)  
(Importante)  
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=bdad28e8-987e-492e-a405-b3be552d2d7a) (instalación Server Core)  
(KB2779030)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ced1ffc6-7d30-480a-a3e0-8071981d1863) (instalación Server Core)  
(KB2758857)  
(Crítica)
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
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=9c60014b-133e-455e-b03f-d73f6e36d3de) (instalación Server Core)  
(KB2753842)  
(Importante)  
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=6298d55c-2ed2-4a90-9dfe-43bae0932e27) (instalación Server Core)  
(KB2779030)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b9a687e6-9ab7-4dae-9771-5f7bb3123e06) (instalación Server Core)  
(KB2758857)  
(Crítica)
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
Windows Server 2008 R2 para sistemas x64 (instalación Server Core)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=fedee43c-0065-42bf-9714-171b5b74f099) (instalación Server Core)  
(KB2753842)  
(Importante)  
[Windows Server 2008 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=3dfa40ef-86a2-44a0-b523-f4a85c7ac82c) (instalación Server Core)  
(KB2779030)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=9e06181f-de06-423b-bbeb-df1f451fb817)(instalación Server Core)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=d3fb096b-87b5-4715-a093-9ec9b021a40f)(instalación Server Core)  
(KB2765809)  
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
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=fedee43c-0065-42bf-9714-171b5b74f099) (instalación Server Core)  
(KB2753842)  
(Importante)  
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=3dfa40ef-86a2-44a0-b523-f4a85c7ac82c) (instalación Server Core)  
(KB2779030)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=9e06181f-de06-423b-bbeb-df1f451fb817) (instalación Server Core)  
(KB2758857)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=d3fb096b-87b5-4715-a093-9ec9b021a40f) (instalación Server Core)  
(KB2765809)  
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
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=15298129-8f1c-47d7-a7e9-efb40823d91a) (instalación Server Core)  
(KB2753842)  
(Importante)  
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=f8e84ff9-a9c0-4363-b5a6-1b90254edd73) (instalación Server Core)  
(KB2779030)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2012](http://www.microsoft.com/downloads/details.aspx?familyid=d6654bf1-1ab9-4691-8729-793eb6d0e563) (instalación Server Core)  
(KB2765809)  
(Importante)
</td>
</tr>
</table>
 
**Notas para MS12-077**

<sup>[1]</sup>Las clasificaciones de gravedad no se aplican a esta actualización para el software especificado porque las vías de ataque conocidas para la vulnerabilidad tratada en este boletín están bloqueadas en una configuración predeterminada. No obstante, como medida de defensa en profundidad, Microsoft recomienda que los clientes de este software apliquen esta actualización de seguridad.

<sup>[2]</sup>Esta actualización solo está disponible a través de [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130).

**Nota para MS12-078**

<sup>[1]</sup>Esta actualización solo está disponible a través de [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130).

#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Conjuntos de programas y componentes de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador** **del** **boletín**
</td>
<td style="border:1px solid black;">
[**MS12-079**](http://go.microsoft.com/fwlink/?linkid=271609)
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
Microsoft Office 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Word 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=6947d500-f197-4001-bb39-1c4221af1b36)  
(KB2760497)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft Word 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=52aad8a5-14d9-4c02-828a-5c1164a01f27)<sup>[1]</sup>
(KB2760421)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Word 2007 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=52aad8a5-14d9-4c02-828a-5c1164a01f27)<sup>[1]</sup>
(KB2760421)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Word 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=68c69b37-c544-4f24-8589-4212b868dd69)  
(KB2760410)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Word 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=9d776c2b-1a9a-4ccb-9e76-dd2cb0f9a80d)  
(KB2760410)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Otro software de Microsoft Office
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-079**](http://go.microsoft.com/fwlink/?linkid=271609)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Word Viewer
</td>
<td style="border:1px solid black;">
[Microsoft Word Viewer](http://www.microsoft.com/downloads/details.aspx?familyid=4ccaabd9-5128-4505-ba2f-20bcf02b97ec)  
(KB2760498)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office Service Pack 2
</td>
<td style="border:1px solid black;">
[Paquete de compatibilidad de Microsoft Office Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c82de87d-3457-423e-9bfc-ec3f950049e7)  
(KB2760416)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office Service Pack 3
</td>
<td style="border:1px solid black;">
[Paquete de compatibilidad de Microsoft Office Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=c82de87d-3457-423e-9bfc-ec3f950049e7)  
(KB2760416)  
(Importante)
</td>
</tr>
</table>
 
**Notas para MS12-079**

<sup>[1]</sup>Para Microsoft Office Word 2007, además del paquete de actualizaciones de seguridad KB2760421, los clientes también deben instalar la actualización de seguridad para Paquete de compatibilidad de Microsoft Office (KB2760416) con el fin de protegerse de la vulnerabilidad descrita en este boletín.

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Software de servidor de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Exchange Server
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-079**](http://go.microsoft.com/fwlink/?linkid=271609)
</td>
<td style="border:1px solid black;">
[**MS12-080**](http://go.microsoft.com/fwlink/?linkid=272389)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Clasificación de gravedad acumulada**
</td>
<td style="border:1px solid black;">
**Ninguna**
</td>
<td style="border:1px solid black;">
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Exchange Server 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Exchange Server 2007 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=605fc9bc-a05c-4466-ace6-9c2af087d797)   
(KB2746157)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Exchange Server 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Exchange Server 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=e43b1164-d768-4152-b9a3-d1491e2f3cba)   
(KB2787763)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Exchange Server 2010 Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Exchange Server 2010 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2a49ed58-9dab-4d48-ae8a-c7139e3b34ba)   
(KB2785908)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft SharePoint Server
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-079**](http://go.microsoft.com/fwlink/?linkid=271609)
</td>
<td style="border:1px solid black;">
[**MS12-080**](http://go.microsoft.com/fwlink/?linkid=272389)
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
**Ninguna**
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
[Word Automation Services](http://www.microsoft.com/downloads/details.aspx?familyid=62007dcd-80db-42e4-8478-9e81f89cab98)  
(KB2760405)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="3" style="border:1px solid black;">
Microsoft Office Web Apps
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-079**](http://go.microsoft.com/fwlink/?linkid=271609)
</td>
<td style="border:1px solid black;">
[**MS12-080**](http://go.microsoft.com/fwlink/?linkid=272389)
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
**Ninguna**
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Web Apps 2010 Service Pack 1 
</td>
<td style="border:1px solid black;">
[Microsoft Office Web Apps 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=c98d8ef3-e9a8-4e7c-9e0a-02e192bab39c)   
(KB2687412)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 
**Nota para MS12-079**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central** **de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://go.microsoft.com/fwlink/?linkid=69903). [TechNet Security TechCenter](http://go.microsoft.com/fwlink/?linkid=21171) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar el [Centro de seguridad y protección de Microsoft](http://go.microsoft.com/fwlink/?linkid=85102), donde esta información también está disponible haciendo clic en "Actualizaciones de seguridad".

Las actualizaciones de seguridad están disponibles en [Microsoft Update](http://go.microsoft.com/fwlink/?linkid=40747) y [Windows Update](http://go.microsoft.com/fwlink/?linkid=21130). También hay actualizaciones de seguridad disponibles en el [Centro de descarga de Microsoft](http://go.microsoft.com/fwlink/?linkid=21129). Si realiza una búsqueda de las palabras clave “actualización de seguridad” podrá encontrarlas fácilmente.

Para clientes de Microsoft Office para Mac, Microsoft AutoUpdate para Mac puede servir de ayuda para mantener actualizado el software de Microsoft. Para obtener más información acerca del uso de Microsoft AutoUpdate para Mac, vea [Buscar actualizaciones de software automáticamente](http://mac2.microsoft.com/help/office/14/en-us/word/item/ffe35357-8f25-4df8-a0a3-c258526c64ea).

Finalmente, las actualizaciones de seguridad se pueden descargar del [Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=96155). El Catálogo de Microsoft Update ofrece un catálogo en el que se pueden realizar búsquedas del contenido que está disponible a través de Windows Update y Microsoft Update, incluidas las actualizaciones de seguridad, los controladores y los Service Packs. Al realizar la búsqueda con el número del boletín de seguridad (como "MS12-001"), puede agregar todas las actualizaciones aplicables a la cesta (incluidos diferentes idiomas para una actualización) y descargarlas en la carpeta que elija. Para obtener más información sobre el Catálogo de Microsoft Update, vea las [preguntas más frecuentes del Catálogo de Microsoft Update](http://go.microsoft.com/fwlink/?linkid=97900).

**Consejos para la detección y la implementación**

Microsoft ofrece orientación para la detección y la implementación de las actualizaciones de seguridad. Dicha orientación contiene recomendaciones e información que pueden ayudar a los profesionales de TI a comprender el modo de usar varias herramientas para la detección y la implementación de las actualizaciones de seguridad. Para obtener más información, vea el [artículo 961747 de Microsoft Knowledge Base](http://support.microsoft.com/kb/961747).

**Microsoft** **Baseline** **Security** **Analyzer**

Esta herramienta permite a los administradores examinar sistemas remotos y locales para detectar las actualizaciones de seguridad que faltan así como las configuraciones de seguridad incorrectas más comunes. Para obtener más información acerca de MBSA, vea [Microsoft Baseline Security Analyzer](http://go.microsoft.com/fwlink/?linkid=21134).

**Windows Server** **UpdateServices**

Windows Server Update Services (WSUS) permite a los administradores implementar de un modo rápido y confiable las actualizaciones críticas y de seguridad más recientes en sistemas operativos Microsoft Windows 2000 y versiones posteriores, Office XP y versiones posteriores, Exchange Server 2003 y SQL Server 2000 hasta Windows 2000 y sistemas operativos posteriores.

Para obtener más información acerca de cómo implementar esta actualización de seguridad con Windows Server Update Services, visite [Windows Server Update Services](http://technet.microsoft.com/wsus/default).

**System** **Center** **Configuration** **Manager**

La administración de actualizaciones de software de System Center Configuration Manager simplifica la tarea compleja de entregar y administrar actualizaciones para los sistemas de TI en toda la empresa. Con System Center Configuration Manager, los administradores de TI pueden ofrecer actualizaciones de los productos de Microsoft a una serie de dispositivos, incluidos equipos de escritorio, portátiles, servidores y dispositivos móviles.

La evaluación automática de vulnerabilidades en System Center Configuration Manager detecta las necesidades de actualizaciones e informa de las acciones recomendadas. La administración de actualizaciones de software en System Center Configuration Manager se basa en Microsoft Windows Software Update Services (WSUS), una infraestructura de actualizaciones probada con la que están familiarizados los administradores de TI de todo el mundo. Para obtener más información acerca de System Center Configuration Manager, vea [Recursos técnicos de System Center](http://technet.microsoft.com/systemcenter/bb980621).

**Systems** **Management Server 2003**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales.

**Nota** System Management Server 2003 está fuera del soporte técnico general desde el 12 de enero de 2010. Para obtener más información acerca de los ciclos de vida de los productos, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742). Ya está disponible la siguiente versión de SMS, System Center Configuration Manager; vea la sección anterior, **System** **Center** **Configuration** **Manager**.

Para obtener más información acerca de cómo los administradores pueden usar SMS 2003 para implementar actualizaciones de seguridad, vea [Escenarios y procedimientos para Microsoft Systems Management Server 2003: Administración de distribución de software y revisiones](http://www.microsoft.com/downloads/details.aspx?familyid=32f2bb4c-42f8-4b8d-844f-2553fd78049f). Para obtener información acerca de SMS, visite [Microsoft Systems Management Server TechCenter](http://technet.microsoft.com/systemcenter/bb545936).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://www.microsoft.com/downloads/en/details.aspx?familyid=7bd3a16e-1899-4e0b-bb99-1320e816167d)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet.microsoft.com/library/cc749197) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

### Información adicional:

#### Herramienta de eliminación de software malintencionado de Microsoft Windows

Microsoft ha publicado una versión actualizada de la Herramienta de eliminación de software malintencionado de Microsoft Windows en Windows Update, Microsoft Update, Windows Server Update Services y Centro de descarga.

#### Actualizaciones no relacionadas con la seguridad en MU, WU y WSUS

Para obtener información acerca de las publicaciones no relacionadas con la seguridad en Windows Update y Microsoft Update, vea:

-   [Artículo 894199 de Microsoft Knowledge Base](http://support.microsoft.com/kb/894199)
-   : Descripción de cambios de contenido de Software Update Services y Windows Server Update Services. Incluye todo el contenido de Windows.
-   [Actualizaciones de meses anteriores para Windows Server Update Services](http://technet.microsoft.com/wsus/bb456965)
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

-   [Rosario Valotta](https://sites.google.com/site/tentacoloviola)
-   , por informar de dos problemas descritos en MS12-077
-   Fermin J. Serna, de [Google Inc](http://www.google.com), por informar de un problema descrito en MS12-077
-   Eetu Luodemaa y Joni Vähämäki, de [Documill](http://www.documill.com), en colaboración con Chromium Security Rewards Program, por informar de un problema en MS12-078
-   Un colaborador anónimo, en colaboración con el programa [SecuriTeam Secure Disclosure de Beyond Security](http://www.beyondsecurity.com/ssd.html), por informar de un problema descrito en MS12-079
-   Lucas Apa, de [IOActive](http://ioactive.co.uk/), por informar de un problema descrito en MS12-081
-   [Aniway](mailto:aniway.anyway@gmail.com)
-   , en colaboración con
-   [VeriSign iDefense Labs](http://labs.idefense.com/)
-   , por informar de un problema descrito en MS12-082

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Soluciones de seguridad para profesionales de TI: Soporte técnico y solución de problemas de seguridad de TechNet
-   Ayuda para proteger su equipo con Windows de virus y malware: [Solución antivirus y centro de seguridad](http://support.microsoft.com/contactus/cu_sc_virsec_master)
-   Soporte local según su país: [Soporte internacional](http://support.microsoft.com/common/international.aspx)

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (11 de diciembre de 2012): Publicación del resumen del boletín.
-   V1.1 (12 de diciembre de 2012): se ha corregido la entrada de requisito de reinicio para MS12-082. Se trata únicamente de un cambio informativo. No había cambios en los archivos de la actualización de seguridad.
-   V2.0 (20 de diciembre de 2012): para MS12-078, se volvió a publicar la actualización KB2753842 para resolver un problema con las fuentes OpenType que no se representan correctamente después de instalarse la actualización original. Los clientes que han instalado correctamente la actualización KB2753842 original deben instalar la actualización que se publica de nuevo.

*Built at 2014-04-18T01:50:00Z-07:00*
