---
TOCTitle: 'MS12-AUG'
Title: Resumen del boletín de seguridad de Microsoft de agosto 2012
ms:assetid: 'ms12-aug'
ms:contentKeyID: 61225433
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms12-aug(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de agosto 2012
============================================================

Publicado: martes, 14 de agosto de 2012 | Actualizado: martes, 11 de diciembre de 2012

**Versión:** 3.0

Este resumen del boletín enumera los boletines de seguridad publicados para agosto de 2012.

Con la publicación de los boletines de seguridad de agosto de 2012, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 9 de agosto de 2012. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 15 de agosto de 2012, a las 11:00 a.m., hora del Pacífico (EE.UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de agosto](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032522490&culture=en-us). Después de esta fecha, este webcast estará disponible a petición. Para obtener más información, vea los [webcasts y resúmenes de boletines de seguridad de Microsoft](http://technet.microsoft.com/es-es/security/bulletinarchive?y=2012&m=12).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, **Información** **adicional**.

### Información del boletín

Resúmenes ejecutivos
--------------------

En la tabla siguiente se resumen los boletines de seguridad de este mes por orden de gravedad.

Para obtener detalles acerca del software afectado, vea la siguiente sección, **Ubicaciones** **de descarga y software afectado**.

 
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
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-052">MS12-052</a></td>
<td style="border:1px solid black;"><strong>Actualización de seguridad acumulativa para Internet Explorer (2722913)</strong> <br />
<br />
Esta actualización de seguridad resuelve cuatro vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. La más grave de las vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un intruso que aprovechara cualquiera de estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-053">MS12-053</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en el Escritorio remoto podría permitir la ejecución remota de código (2723135)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en el protocolo de Escritorio remoto. La vulnerabilidad podría permitir la ejecución remota de código si un atacante envía una secuencia de paquetes RDP a un sistema afectado. De forma predeterminada, el protocolo de Escritorio remoto (RDP) no está habilitado en ningún sistema operativo Windows. Los sistemas que no tienen RDP habilitado no están expuestos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-054">MS12-054</a></td>
<td style="border:1px solid black;"><strong>Vulnerabilidades en los componentes de red de Windows</strong> <strong>podrían</strong> <strong>permitir la ejecución remota de código (2733594)</strong> <br />
<br />
Esta actualización de seguridad resuelve cuatro vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. La más grave de estas vulnerabilidades podría permitir la ejecución remota de código si un atacante envía una respuesta especialmente diseñada a una solicitud del administrador de trabajos de impresión de Windows. Los procedimientos recomendados para firewall y las configuraciones de firewall predeterminadas estándar pueden proteger a las redes de los ataques procedentes del exterior del perímetro de la empresa. Se recomienda que los sistemas conectados directamente a Internet tengan expuesta una cantidad mínima de puertos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-060">MS12-060</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en los controles comunes de Windows podría permitir la ejecución remota de código (2720573)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en los controles comunes de Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario visita un sitio web que incluye contenido especialmente diseñado para aprovechar la vulnerabilidad. No obstante, el atacante no podría en ningún caso obligar a los usuarios a visitar un sitio web. Por lo tanto, tendría que atraerlos al sitio web; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger que lleve a los usuarios al sitio web del atacante. El archivo malintencionado también se podría enviar como datos adjuntos de correo electrónico, pero el atacante tendría que convencer el usuario para que abriera los datos adjuntos con el fin de aprovechar la vulnerabilidad.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office,<br />
Microsoft SQL Server,<br />
Software de servidor de Microsoft,<br />
Herramientas de desarrollo de Microsoft</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-058">MS12-058</a></td>
<td style="border:1px solid black;"><strong>Las vulnerabilidades en Microsoft Exchange Server</strong> <strong>WebReadyDocumentViewing</strong> <strong>podría permitir la ejecución remota de código (2740358)  <br />
</strong>Esta actualización de seguridad resuelve vulnerabilidades que se han divulgado de forma pública en Microsoft Exchange Server WebReady Document Viewing. Las vulnerabilidades podrían permitir la ejecución remota de código en el contexto de seguridad del servicio de transcodificación en el servidor Exchange si un usuario obtiene una vista previa de un archivo especialmente diseñado mediante Outlook Web App (OWA). El servicio de transcodificación de Exchange que se usa para WebReady Document Viewing se ejecuta en la cuenta LocalService. La cuenta LocalService tiene privilegios mínimos en el equipo local y presenta credenciales anónimas en la red.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">No requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Exchange Server</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-055">MS12-055</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en los controladores modo</strong> <strong>kernel</strong> <strong>de Windows podría permitir la elevación de privilegios</strong> <strong>(2731847)</strong> <br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si un atacante inicia sesión en el sistema y ejecuta una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de iniciar una sesión local.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-056">MS12-056</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en los motores de VBScript y</strong> <strong>JScript</strong> <strong>podría permitir la ejecución remota de código (2706045)</strong> <br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en los motores de scripting de JScript y VBScript en las versiones de 64 bits de Microsoft Windows. Esta vulnerabilidad podría permitir la ejecución remota de código si un usuario visita un sitio web especialmente diseñado. El atacante no podría obligar a los usuarios a visitar el sitio web. Por lo tanto, tendría que atraerlos al sitio web; por lo general, convenciéndoles para que hagan clic en un vínculo de un mensaje de correo electrónico o de Instant Messenger que lleve a los usuarios al sitio web del atacante.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-057">MS12-057</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Office podría permitir la ejecución remota de código (2731879)  <br />
</strong>Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Office. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo especialmente diseñado o inserta un archivo gráfico CGM especialmente diseñado en un archivo de Office. Un atacante que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-059">MS12-059</a></td>
<td style="border:1px solid black;"><strong>Una vulnerabilidad en Microsoft Visio podría permitir la ejecución remota de código (2733918)  <br />
</strong>Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Office. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo de Visio especialmente diseñado. Un atacante que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
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
<th style="border:1px solid black;" >Evaluación de explotabilidad para la última versión de software</th>
<th style="border:1px solid black;" >Evaluación de explotabilidad para la versión de software anterior</th>
<th style="border:1px solid black;" >Evaluación de explotabilidad de denegación de servicio</th>
<th style="border:1px solid black;" >Notas clave</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-052">MS12-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con el diseño HTML</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1526">CVE-2012-1526</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-052">MS12-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código en el acceso asincrónico a objetos NULL</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-2521">CVE-2012-2521</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-052">MS12-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código de daños en la tabla de funciones virtuales</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-2522">CVE-2012-2522</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-052">MS12-052</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código en desbordamiento de enteros en JavaScript</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-2523">CVE-2012-2523</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-056">MS12-056</a> también trata esta vulnerabilidad.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-053">MS12-053</a></td>
<td style="border:1px solid black;">Vulnerabilidad de protocolo de Escritorio remoto</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-2526">CVE-2012-2526</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-054">MS12-054</a></td>
<td style="border:1px solid black;">Vulnerabilidad de denegación de servicio en el protocolo de administración remota</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1850">CVE-2012-1850</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-054">MS12-054</a></td>
<td style="border:1px solid black;">Vulnerabilidad de cadena de formato del servicio de administrador de trabajos de impresión</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1851">CVE-2012-1851</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-054">MS12-054</a></td>
<td style="border:1px solid black;">Vulnerabilidad de desbordamiento del montón en el protocolo de administración remota</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1852">CVE-2012-1852</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-054">MS12-054</a></td>
<td style="border:1px solid black;">Vulnerabilidad de desbordamiento de la pila en el protocolo de administración remota</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1853">CVE-2012-1853</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-055">MS12-055</a></td>
<td style="border:1px solid black;">Vulnerabilidad en el uso de Win32k después de la liberación</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-2527">CVE-2012-2527</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-056">MS12-056</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código en desbordamiento de enteros en JavaScript</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-2523">CVE-2012-2523</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-052">MS12-052</a> también trata esta vulnerabilidad.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-057">MS12-057</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con el formato de archivo CGM</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-2524">CVE-2012-2524</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-058">MS12-058</a></td>
<td style="border:1px solid black;">Oracle Outside In contiene varias vulnerabilidades que se pueden aprovechar</td>
<td style="border:1px solid black;">Varias*</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">*Varias vulnerabilidades, vea el boletín <a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-058">MS12-058</a> para obtener detalles.<br />
<br />
Estas vulnerabilidades se han divulgado de forma pública.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-059">MS12-059</a></td>
<td style="border:1px solid black;">Vulnerabilidad de desbordamiento del búfer en el formato de archivo DXF de Visio</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1888">CVE-2012-1888</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/es-es/security/bulletin/ms12-060">MS12-060</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código en MSCOMCTL</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2012-1856">CVE-2012-1856</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/en-us/security/cc998259.aspx">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Temporal</td>
<td style="border:1px solid black;">Microsoft tiene constancia de ataques limitados y dirigidos que intentan aprovechar esta vulnerabilidad.</td>
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
[**MS12-052**](http://go.microsoft.com/fwlink/?linkid=255327)
</td>
<td style="border:1px solid black;">
[**MS12-053**](http://go.microsoft.com/fwlink/?linkid=257906)
</td>
<td style="border:1px solid black;">
[**MS12-054**](http://go.microsoft.com/fwlink/?linkid=257914)
</td>
<td style="border:1px solid black;">
[**MS12-055**](http://go.microsoft.com/fwlink/?linkid=257907)
</td>
<td style="border:1px solid black;">
[**MS12-056**](http://go.microsoft.com/fwlink/?linkid=256487)
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
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows XP Service Pack 3
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=e1df425a-a67e-42f8-9eb5-a503f684c201)  
(KB2722913)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=5afc85e3-a214-4774-93ab-17f9d199ebde)  
(KB2722913)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=213b3590-381e-437c-9391-ff6d7400f250)  
(KB2722913)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=ccc3d8fb-2631-42d0-87ed-5d29d4b1f598)  
(KB2723135)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=5403c78c-6b87-4788-89c3-0140b887ec6f)  
(KB2705219)  
(Crítica)  
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=c28e01d6-0030-417d-80dd-b34febd22ec1)  
(KB2712808)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=db21a230-0f6b-4d74-9f32-3718a59efd28)  
(KB2731847)  
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
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=2fdbe657-1810-4c5d-9ba8-5da148272756)  
(KB2722913)  
(Crítica)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=ce5e8621-5457-4a27-9816-9ce719fd6937)  
(KB2722913)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=01784bbc-20fc-4d0f-bfcd-a5a25dd603e8)  
(KB2722913)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a8eb0583-071d-4d8e-92fb-937035411b49)  
(KB2705219)  
(Crítica)  
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b9e41497-5c49-45fc-8ad0-c853516609df)  
(KB2712808)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows XP Professional x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=a036c343-5c6e-4484-b7f7-c7161c6880fd)  
(KB2731847)  
(Importante)
</td>
<td style="border:1px solid black;">
[JScript 5.8 y VBScript 5.8](http://www.microsoft.com/downloads/details.aspx?familyid=e1b9a081-0329-4db6-b026-04a332cb0b4d)  
(KB2706045)  
(Importante)
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
[**MS12-052**](http://go.microsoft.com/fwlink/?linkid=255327)
</td>
<td style="border:1px solid black;">
[**MS12-053**](http://go.microsoft.com/fwlink/?linkid=257906)
</td>
<td style="border:1px solid black;">
[**MS12-054**](http://go.microsoft.com/fwlink/?linkid=257914)
</td>
<td style="border:1px solid black;">
[**MS12-055**](http://go.microsoft.com/fwlink/?linkid=257907)
</td>
<td style="border:1px solid black;">
[**MS12-056**](http://go.microsoft.com/fwlink/?linkid=256487)
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
[**Crítica**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Baja**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=e5e3e9be-ba36-4fdf-93f6-a30fb087d273)  
(KB2722913)  
(Moderada)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=0bced0f3-9778-4ee3-86fb-7f28b57adbce)  
(KB2722913)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=19393940-2519-4e97-89cd-de993ced31d5)  
(KB2722913)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2847952f-0234-4cf6-820a-1f0a285b2fb7)  
(KB2705219)  
(Importante)  
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c20f475d-5211-4fdc-8a2f-4408f1baaece)  
(KB2712808)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=50090b08-3f82-4680-b871-2b18fc2386d0)  
(KB2731847)  
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
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=eb92185b-405a-4d96-b119-13f234a9c4ac)  
(KB2722913)  
(Moderada)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=26cda257-6607-4bd8-9152-cbcc2a753915)  
(KB2722913)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=fe7a78fc-f882-4748-a9e3-04b85d136ca2)  
(KB2722913)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=3833d768-1dab-4a85-822f-87c7fa3db261)  
(KB2705219)  
(Importante)  
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ad883d42-d8bb-482b-bf36-e2007cf73f84)  
(KB2712808)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7f72ba9a-80b2-459d-acad-da6a8b900d6f)  
(KB2731847)  
(Importante)
</td>
<td style="border:1px solid black;">
[JScript 5.8 y VBScript 5.8](http://www.microsoft.com/downloads/details.aspx?familyid=81f5d8a5-12e5-4227-ae6f-5aea6ffff2a5)  
(KB2706045)  
(Baja)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Internet Explorer 6](http://www.microsoft.com/downloads/details.aspx?familyid=6c5edf14-ecb6-40af-a315-b049457415d6)  
(KB2722913)  
(Moderada)  
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=c890335b-6ceb-427a-9cc7-95ef8c26d306)  
(KB2722913)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=2fba3a11-3621-464d-ab22-d902195205f4)  
(KB2705219) (Importante)  
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=2857701f-3447-452c-a986-9f2fe42fe64d)(KB2712808)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Windows Server 2003 con SP2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=9e647f22-2e80-4f4a-b648-615243741df2)  
(KB2731847)  
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
[**MS12-052**](http://go.microsoft.com/fwlink/?linkid=255327)
</td>
<td style="border:1px solid black;">
[**MS12-053**](http://go.microsoft.com/fwlink/?linkid=257906)
</td>
<td style="border:1px solid black;">
[**MS12-054**](http://go.microsoft.com/fwlink/?linkid=257914)
</td>
<td style="border:1px solid black;">
[**MS12-055**](http://go.microsoft.com/fwlink/?linkid=257907)
</td>
<td style="border:1px solid black;">
[**MS12-056**](http://go.microsoft.com/fwlink/?linkid=256487)
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
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=862bd543-2fc5-4c4c-8d18-4623ccc68166)  
(KB2722913)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=709a85b7-d192-4bba-990a-ea98fdf6e882)  
(KB2722913)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=430a43fa-78b8-4273-81e1-3081767ddcf9)  
(KB2722913)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=cbae6606-3721-48b9-ba3e-9d85df7e08b9)  
(KB2705219)  
(Moderada)  
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b4b216dc-533e-4fb4-acc8-ce5eb231320e)  
(KB2712808)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=41362740-876e-4c9e-9729-67dea6830438)  
(KB2731847)  
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
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=da933584-40ba-42a0-82fc-b84b41c6c5a4)  
(KB2722913)  
(Crítica)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=ec48d017-d9ed-4b0e-b51f-0f04996088b6)  
(KB2722913)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=5341a615-b737-4e48-8dfd-828725d9d513)  
(KB2722913)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e4b4e53b-69d6-4ab6-98bb-3f8871048abe)  
(KB2705219)  
(Moderada)  
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=dc966826-83e6-4bdc-bc58-8b6eb8917934)  
(KB2712808)  
(Importante)
</td>
<td style="border:1px solid black;">
[Windows Vista x64 Edition Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=007b4d50-b770-4e8f-b8d0-060f7bb58ad5)  
(KB2731847)  
(Importante)
</td>
<td style="border:1px solid black;">
[JScript 5.8 y VBScript 5.8](http://www.microsoft.com/downloads/details.aspx?familyid=294a7eb4-c47f-449f-8931-262bec7d6ecc)  
(KB2706045)  
(Importante)
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
[**MS12-052**](http://go.microsoft.com/fwlink/?linkid=255327)
</td>
<td style="border:1px solid black;">
[**MS12-053**](http://go.microsoft.com/fwlink/?linkid=257906)
</td>
<td style="border:1px solid black;">
[**MS12-054**](http://go.microsoft.com/fwlink/?linkid=257914)
</td>
<td style="border:1px solid black;">
[**MS12-055**](http://go.microsoft.com/fwlink/?linkid=257907)
</td>
<td style="border:1px solid black;">
[**MS12-056**](http://go.microsoft.com/fwlink/?linkid=256487)
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
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Baja**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=91062e12-401e-472e-a6b6-0eb7216f5264)  
(KB2722913)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=77612ea1-13fb-4c53-bbd2-8796f0d5a9ed)  
(KB2722913)  
(Moderada)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=f016949d-b931-49f3-867b-f1c64839379e)  
(KB2722913)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=354e502b-3016-4c5e-8611-bc1b35e1a7eb)  
(KB2705219)  
(Moderada)  
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=35fb03b1-162a-4552-8bb9-6b564acbd57b)  
(KB2712808)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ec759712-2f38-41a9-8b6d-c6908cc58479)  
(KB2731847)  
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
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=a610d606-ca70-4dbd-9971-b6915dc4dc59)  
(KB2722913)  
(Moderada)  
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=defe6c53-66d7-4ea5-93b1-7487ccf19f24)  
(KB2722913)  
(Moderada)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=e5ab43bb-dbdb-4b2b-bbf2-260297ee5518)  
(KB2722913)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2b8a730c-46ac-49b7-b9ae-73062d5a79f2)  
(KB2705219)  
(Moderada)  
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e89024ca-a9e8-4ebf-91eb-cbf8e05398e7)  
(KB2712808)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=caf68d77-3315-4383-a901-ba0385ffe561)  
(KB2731847)  
(Importante)
</td>
<td style="border:1px solid black;">
[JScript 5.8 y VBScript 5.8](http://www.microsoft.com/downloads/details.aspx?familyid=47b2e47f-30f1-48e8-a857-70df319011ef)  
(KB2706045)  
(Baja)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Internet Explorer 7](http://www.microsoft.com/downloads/details.aspx?familyid=6564a6a1-c8ba-4275-81b5-6664c8e3d010)  
(KB2722913)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=cce9a924-a74c-49e0-869f-6b9c1cd12cba)  
(KB2705219)  
(Moderada)  
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=57153478-4837-438a-8487-929a48fd758a)  
(KB2712808)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=dee601c7-4ab4-4556-8d83-90864b09d365)  
(KB2731847)  
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
[**MS12-052**](http://go.microsoft.com/fwlink/?linkid=255327)
</td>
<td style="border:1px solid black;">
[**MS12-053**](http://go.microsoft.com/fwlink/?linkid=257906)
</td>
<td style="border:1px solid black;">
[**MS12-054**](http://go.microsoft.com/fwlink/?linkid=257914)
</td>
<td style="border:1px solid black;">
[**MS12-055**](http://go.microsoft.com/fwlink/?linkid=257907)
</td>
<td style="border:1px solid black;">
[**MS12-056**](http://go.microsoft.com/fwlink/?linkid=256487)
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
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows 7 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=625c45f5-5ad1-4ade-8883-33019587ab49)  
(KB2722913)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=b2760784-6163-4a8d-86fb-72c88ed2b8ef)  
(KB2722913)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=f83f6d97-24f1-4ee0-971d-ab79071fede6)  
(KB2705219)  
(Moderada)  
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=2bcfb574-a7d0-4d7e-b557-41bdcddfde42)  
(KB2712808)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=c709aabf-4b3f-4780-8b82-c6c33a211e31)  
(KB2731847)  
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
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=625c45f5-5ad1-4ade-8883-33019587ab49)  
(KB2722913)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=b2760784-6163-4a8d-86fb-72c88ed2b8ef)  
(KB2722913)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=f83f6d97-24f1-4ee0-971d-ab79071fede6)  
(KB2705219)  
(Moderada)  
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=2bcfb574-a7d0-4d7e-b557-41bdcddfde42)  
(KB2712808)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=c709aabf-4b3f-4780-8b82-c6c33a211e31)  
(KB2731847)  
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
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=f5bc6713-2540-4571-ae1f-04f427b33019)  
(KB2722913)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=cac3b463-fb9c-474e-9e3d-bb96f7b4c14f)  
(KB2722913)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=f49e3f9e-8a96-43e6-8b0a-5c9b78cd819d)  
(KB2705219)  
(Moderada)  
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=655182f9-110b-4b81-b140-0a5986d7343f)  
(KB2712808)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=f62cf24a-8926-4dde-95ac-cc5f62e448be)  
(KB2731847)  
(Importante)
</td>
<td style="border:1px solid black;">
[JScript 5.8 y VBScript 5.8](http://www.microsoft.com/downloads/details.aspx?familyid=ece661be-4ddf-42cc-a62b-15ce53b9d74b)  
(KB2706045)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=f5bc6713-2540-4571-ae1f-04f427b33019)  
(KB2722913)  
(Crítica)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=cac3b463-fb9c-474e-9e3d-bb96f7b4c14f)  
(KB2722913)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=f49e3f9e-8a96-43e6-8b0a-5c9b78cd819d)  
(KB2705219)  
(Moderada)  
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=655182f9-110b-4b81-b140-0a5986d7343f)  
(KB2712808)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows 7 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=f62cf24a-8926-4dde-95ac-cc5f62e448be)  
(KB2731847)  
(Importante)
</td>
<td style="border:1px solid black;">
[JScript 5.8 y VBScript 5.8](http://www.microsoft.com/downloads/details.aspx?familyid=ece661be-4ddf-42cc-a62b-15ce53b9d74b)  
(KB2706045)  
(Importante)
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
[**MS12-052**](http://go.microsoft.com/fwlink/?linkid=255327)
</td>
<td style="border:1px solid black;">
[**MS12-053**](http://go.microsoft.com/fwlink/?linkid=257906)
</td>
<td style="border:1px solid black;">
[**MS12-054**](http://go.microsoft.com/fwlink/?linkid=257914)
</td>
<td style="border:1px solid black;">
[**MS12-055**](http://go.microsoft.com/fwlink/?linkid=257907)
</td>
<td style="border:1px solid black;">
[**MS12-056**](http://go.microsoft.com/fwlink/?linkid=256487)
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
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Importante**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
<td style="border:1px solid black;">
[**Baja**](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=f6ea664b-575c-4cf0-b479-d1a2653288ee)  
(KB2722913)  
(Moderada)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=30a43d95-f489-49c2-a48a-a262fa196bbf)  
(KB2722913)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=e15d2bae-1511-4d74-93cb-0d614820e175)  
(KB2705219)  
(Moderada)  
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=20c9a72f-a8b6-4b4c-a9ea-de93069cff3a)  
(KB2712808)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=fc5b9df9-c836-407a-a1d4-364c1a885242)  
(KB2731847)  
(Importante)
</td>
<td style="border:1px solid black;">
[JScript 5.8 y VBScript 5.8](http://www.microsoft.com/downloads/details.aspx?familyid=bbb876e6-a6b9-4193-be5e-d84390d30f1e)  
(KB2706045)  
(Baja)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=f6ea664b-575c-4cf0-b479-d1a2653288ee)  
(KB2722913)  
(Moderada)  
[Internet Explorer 9](http://www.microsoft.com/downloads/details.aspx?familyid=30a43d95-f489-49c2-a48a-a262fa196bbf)  
(KB2722913)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=e15d2bae-1511-4d74-93cb-0d614820e175)  
(KB2705219)  
(Moderada)  
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=20c9a72f-a8b6-4b4c-a9ea-de93069cff3a)  
(KB2712808)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=fc5b9df9-c836-407a-a1d4-364c1a885242)  
(KB2731847)  
(Importante)
</td>
<td style="border:1px solid black;">
[JScript 5.8 y VBScript 5.8](http://www.microsoft.com/downloads/details.aspx?familyid=bbb876e6-a6b9-4193-be5e-d84390d30f1e)  
(KB2706045)  
(Baja)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=05a09f6e-b608-4430-b6d4-bb9d10d8347a)  
(KB2722913)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=be89e6a5-34ef-4c23-8e16-722b9ae92073)  
(KB2705219)  
(Moderada)  
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=27b52fb5-ff3c-4dca-9752-1517b873c9cb)  
(KB2712808)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=7f17c057-939e-415d-b56a-01082695ab77)  
(KB2731847)  
(Importante)
</td>
<td style="border:1px solid black;">
[JScript 5.8 y VBScript 5.8](http://www.microsoft.com/downloads/details.aspx?familyid=97004a96-0c83-421d-91a9-d55be32610c9)  
(KB2706045)  
(Baja)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
[Internet Explorer 8](http://www.microsoft.com/downloads/details.aspx?familyid=05a09f6e-b608-4430-b6d4-bb9d10d8347a)  
(KB2722913)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=be89e6a5-34ef-4c23-8e16-722b9ae92073)  
(KB2705219)  
(Moderada)  
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=27b52fb5-ff3c-4dca-9752-1517b873c9cb)  
(KB2712808)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=7f17c057-939e-415d-b56a-01082695ab77)  
(KB2731847)  
(Importante)
</td>
<td style="border:1px solid black;">
[JScript 5.8 y VBScript 5.8](http://www.microsoft.com/downloads/details.aspx?familyid=97004a96-0c83-421d-91a9-d55be32610c9)  
(KB2706045)  
(Baja)
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
[**MS12-052**](http://go.microsoft.com/fwlink/?linkid=255327)
</td>
<td style="border:1px solid black;">
[**MS12-053**](http://go.microsoft.com/fwlink/?linkid=257906)
</td>
<td style="border:1px solid black;">
[**MS12-054**](http://go.microsoft.com/fwlink/?linkid=257914)
</td>
<td style="border:1px solid black;">
[**MS12-055**](http://go.microsoft.com/fwlink/?linkid=257907)
</td>
<td style="border:1px solid black;">
[**MS12-056**](http://go.microsoft.com/fwlink/?linkid=256487)
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
[**Moderada**](http://go.microsoft.com/fwlink/?linkid=21140)
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
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=354e502b-3016-4c5e-8611-bc1b35e1a7eb)  
(KB2705219)  
(Moderada)  
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=35fb03b1-162a-4552-8bb9-6b564acbd57b)  
(KB2712808)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=ec759712-2f38-41a9-8b6d-c6908cc58479)  
(KB2731847)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=2b8a730c-46ac-49b7-b9ae-73062d5a79f2)  
(KB2705219)  
(Moderada)  
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=e89024ca-a9e8-4ebf-91eb-cbf8e05398e7)  
(KB2712808)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=caf68d77-3315-4383-a901-ba0385ffe561)  
(KB2731847)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
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
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=e15d2bae-1511-4d74-93cb-0d614820e175)  
(KB2705219)  
(Moderada)  
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=20c9a72f-a8b6-4b4c-a9ea-de93069cff3a)  
(KB2712808)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=fc5b9df9-c836-407a-a1d4-364c1a885242)  
(KB2731847)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=e15d2bae-1511-4d74-93cb-0d614820e175)  
(KB2705219)  
(Moderada)  
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=20c9a72f-a8b6-4b4c-a9ea-de93069cff3a)  
(KB2712808)  
(Moderada)
</td>
<td style="border:1px solid black;">
[Windows Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=fc5b9df9-c836-407a-a1d4-364c1a885242)  
(KB2731847)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
</table>
 

#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="4" style="border:1px solid black;">
Conjuntos de programas y software de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador** **del** **boletín**
</td>
<td style="border:1px solid black;">
[**MS12-060**](http://go.microsoft.com/fwlink/?linkid=254386)
</td>
<td style="border:1px solid black;">
[**MS12-057**](http://go.microsoft.com/fwlink/?linkid=257684)
</td>
<td style="border:1px solid black;">
[**MS12-059**](http://go.microsoft.com/fwlink/?linkid=255002)
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
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Office 2003 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=fd9626f7-4265-48ae-94b2-68243605db6b)  
(Controles comunes de Windows)  
(KB2726929)  
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
Microsoft Office 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft Office 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b1c185e9-5328-4bf7-b175-fd9d7fc64097)  
(Controles comunes de Windows)  
(KB2687441)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=cc2a0eae-5b7e-465b-ab4c-a93ae7c7c458)  
(KB2596615)  
(Importante)  
[Microsoft Office 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=c2b0cb0f-db07-452f-a9a4-886124d3943e)  
(KB2596754)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Office 2007 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=b1c185e9-5328-4bf7-b175-fd9d7fc64097)  
(Controles comunes de Windows)  
(KB2687441)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2007 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=cc2a0eae-5b7e-465b-ab4c-a93ae7c7c458)  
(KB2596615)  
(Importante)  
[Microsoft Office 2007 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=c2b0cb0f-db07-452f-a9a4-886124d3943e)  
(KB2596754)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=4e08bab7-1408-444d-bad7-a4db76c7f6d3)  
(Controles comunes de Windows)  
(KB2597986)  
(Crítica)
</td>
<td style="border:1px solid black;">
[Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=953b9b69-2f66-4f71-b342-467cc05030ba)  
(KB2687501)  
(Importante)  
[Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=a55a33f9-1eb6-469a-967c-a483764772c3)  
(KB2687510)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Visio 2010 Service Pack 1 (ediciones de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=de95d8b9-51a5-43cd-8ba3-8cbb1320d099)  
(KB2687508)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=90b99372-4f13-4f3a-ae52-da6543745248)  
(KB2687501)  
(Importante)  
[Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=da8a4d12-d4fc-4b6e-b65f-096dedddf529)  
(KB2687510)  
(Importante)
</td>
<td style="border:1px solid black;">
[Microsoft Visio 2010 Service Pack 1 (ediciones de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=af690cd8-cb2c-4743-96f0-ffaec77adf10)  
(KB2687508)  
(Importante)
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Microsoft Office Web Components
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-060**](http://go.microsoft.com/fwlink/?linkid=254386)
</td>
<td style="border:1px solid black;">
[**MS12-057**](http://go.microsoft.com/fwlink/?linkid=257684)
</td>
<td style="border:1px solid black;">
[**MS12-059**](http://go.microsoft.com/fwlink/?linkid=255002)
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
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2003 Web Components Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft Office 2003 Web Components Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=fd9626f7-4265-48ae-94b2-68243605db6b)  
(Controles comunes de Windows)  
(KB2726929)  
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
<th colspan="4" style="border:1px solid black;">
Otro software de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-060**](http://go.microsoft.com/fwlink/?linkid=254386)
</td>
<td style="border:1px solid black;">
[**MS12-057**](http://go.microsoft.com/fwlink/?linkid=257684)
</td>
<td style="border:1px solid black;">
[**MS12-059**](http://go.microsoft.com/fwlink/?linkid=255002)
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
Microsoft Visio Viewer 2010 Service Pack 1 (edición de 32 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Visio Viewer 2010 Service Pack 1 (edición de 32 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=62e87f7b-f48e-43a7-86d7-cbb8f0603ea3)  
(KB2598287)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Visio Viewer 2010 Service Pack 1 (edición de 64 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
[Microsoft Visio Viewer 2010 Service Pack 1 (edición de 64 bits)](http://www.microsoft.com/downloads/details.aspx?familyid=3889e1b3-69b2-4a8f-a0d9-de8c7dc6f5ec)  
(KB2598287)  
(Importante)
</td>
</tr>
</table>
 
**Nota para MS12-060**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Software de servidor de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="4" style="border:1px solid black;">
Microsoft SQL Server
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-060**](http://go.microsoft.com/fwlink/?linkid=254386)
</td>
<td style="border:1px solid black;">
[**MS12-058**](http://go.microsoft.com/fwlink/?linkid=259630)
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
Microsoft SQL Server 2000 Service Pack 4
</td>
<td style="border:1px solid black;">
Actualización de RDA:  
[Microsoft SQL Server 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=22be7d30-86f8-4a3b-ba46-b08624581c61)  
(KB983812)  
(Crítica)  
Actualización de QFE:  
[Microsoft SQL Server 2000 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=09ebb11b-2b82-4891-8ae9-03481c0d7b29)  
(KB983811)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2000 Analysis Services Service Pack 4
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2000 Analysis Services Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=3f5f7d2c-1fd1-437d-a74c-f316c2cd7818)  
(KB983813)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2005 para sistemas de 32 bits Service Pack 4
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2005 para sistemas de 32 bits Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=fd9626f7-4265-48ae-94b2-68243605db6b)<sup>[1]</sup>
(Controles comunes de Windows)  
(KB2726929)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2005 para sistemas x64 Service Pack 4
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2005 para sistemas x64 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=fd9626f7-4265-48ae-94b2-68243605db6b)<sup>[1]</sup>
(Controles comunes de Windows)  
(KB2726929)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2005 para sistemas con Itanium Service Pack 4
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2005 para sistemas con Itanium Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=fd9626f7-4265-48ae-94b2-68243605db6b)<sup>[1]</sup>
(Controles comunes de Windows)  
(KB2726929)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2005 Express Edition con Advanced Services Service Pack 4
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2005 Express Edition con Advanced Services Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=fd9626f7-4265-48ae-94b2-68243605db6b)<sup>[1]</sup>
(Controles comunes de Windows)  
(KB2726929)(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b1c185e9-5328-4bf7-b175-fd9d7fc64097)<sup>[2]</sup>
(Controles comunes de Windows)  
(KB2687441)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2008 para sistemas de 32 bits Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 para sistemas de 32 bits Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=b1c185e9-5328-4bf7-b175-fd9d7fc64097)<sup>[2]</sup>
(Controles comunes de Windows)  
(KB2687441)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b1c185e9-5328-4bf7-b175-fd9d7fc64097)<sup>[2]</sup>
(Controles comunes de Windows)  
(KB2687441)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2008 para sistemas x64 Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 para sistemas x64 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=b1c185e9-5328-4bf7-b175-fd9d7fc64097)<sup>[2]</sup>
(Controles comunes de Windows)  
(KB2687441)(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b1c185e9-5328-4bf7-b175-fd9d7fc64097)<sup>[2]</sup>
(Controles comunes de Windows)  
(KB2687441)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2008 para sistemas con Itanium Service Pack 3
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 para sistemas con Itanium Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=b1c185e9-5328-4bf7-b175-fd9d7fc64097)<sup>[2]</sup>
(Controles comunes de Windows)  
(KB2687441)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 R2 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 R2 para sistemas de 32 bits](http://www.microsoft.com/downloads/details.aspx?familyid=b1c185e9-5328-4bf7-b175-fd9d7fc64097)<sup>[2]</sup>
(Controles comunes de Windows)  
(KB2687441)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2008 R2 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 R2 para sistemas de 32 bits Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b1c185e9-5328-4bf7-b175-fd9d7fc64097)<sup>[2]</sup>
(Controles comunes de Windows)  
(KB2687441)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 R2 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 R2 para sistemas de 32 bits Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b1c185e9-5328-4bf7-b175-fd9d7fc64097)<sup>[2]</sup>
(Controles comunes de Windows)  
(KB2687441)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2008 R2 para sistemas x64
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 R2 para sistemas x64](http://www.microsoft.com/downloads/details.aspx?familyid=b1c185e9-5328-4bf7-b175-fd9d7fc64097)<sup>[2]</sup>
(Controles comunes de Windows)  
(KB2687441)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 R2 para sistemas x64 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b1c185e9-5328-4bf7-b175-fd9d7fc64097)<sup>[2]</sup>
(Controles comunes de Windows)  
(KB2687441)(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2008 R2 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 R2 para sistemas x64 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b1c185e9-5328-4bf7-b175-fd9d7fc64097)<sup>[2]</sup>
(Controles comunes de Windows)  
(KB2687441)(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 R2 para sistemas con Itanium
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 R2 para sistemas con Itanium](http://www.microsoft.com/downloads/details.aspx?familyid=b1c185e9-5328-4bf7-b175-fd9d7fc64097)<sup>[2]</sup>
(Controles comunes de Windows)  
(KB2687441)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SQL Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 R2 para sistemas con Itanium Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=b1c185e9-5328-4bf7-b175-fd9d7fc64097)<sup>[2]</sup>
(Controles comunes de Windows)  
(KB2687441)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SQL Server 2008 R2 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft SQL Server 2008 R2 para sistemas con Itanium Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=b1c185e9-5328-4bf7-b175-fd9d7fc64097)<sup>[2]</sup>
(Controles comunes de Windows)  
(KB2687441)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Microsoft Commerce Server
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-060**](http://go.microsoft.com/fwlink/?linkid=254386)
</td>
<td style="border:1px solid black;">
[**MS12-058**](http://go.microsoft.com/fwlink/?linkid=259630)
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
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Commerce Server 2002 Service Pack 4
</td>
<td style="border:1px solid black;">
[Microsoft Commerce Server 2002 Service Pack 4](http://www.microsoft.com/downloads/details.aspx?familyid=9ad19d40-16ed-47ad-b907-8a48bb64c6d3)  
(KB2716389)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Commerce Server 2007 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft Commerce Server 2007 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=7d972437-f71a-4576-b5c1-a940c0824438)  
(KB2716390)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Commerce Server 2009
</td>
<td style="border:1px solid black;">
[Microsoft Commerce Server 2009](http://www.microsoft.com/downloads/details.aspx?familyid=3879fecd-8360-4c01-b88e-d56e8570cafb)  
(KB2716392)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Commerce Server 2009 R2
</td>
<td style="border:1px solid black;">
[Microsoft Commerce Server 2009 R2](http://www.microsoft.com/downloads/details.aspx?familyid=ce4f9470-e2b2-417e-9015-30355e837fbb)  
(KB2716393)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Microsoft Host Integration Server
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Host Integration Server 2004 Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft Host Integration Server 2004 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=3dde4ef1-d41f-45b0-8660-a546cbe3fc81)  
(KB2711207)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="4" style="border:1px solid black;">
Microsoft Exchange Server
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-060**](http://go.microsoft.com/fwlink/?linkid=254386)
</td>
<td style="border:1px solid black;">
[**MS12-058**](http://go.microsoft.com/fwlink/?linkid=259630)
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
[Microsoft Exchange Server 2007 Service Pack 3](http://www.microsoft.com/downloads/details.aspx?familyid=21a26e23-9d83-41b6-95be-4b48f6e76023)  
(KB2756497)  
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
[Microsoft Exchange Server 2010 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=8646aaca-9829-4d3f-a77b-d24673818da7)  
(KB2756496)  
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
[Microsoft Exchange Server 2010 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=4b24182a-cee9-4ca0-9cc5-c4453475999d)  
(KB2756485)  
(Crítica)
</td>
</tr>
</table>
 
**Notas para MS12-060**

<sup>[1]</sup>Esta actualización es la misma que la actualización KB2726929 de Microsoft Office 2003

<sup>[2]</sup>Esta actualización es la misma que la actualización KB2687441 de Microsoft Office 2007

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

#### Herramientas y software para desarrolladores de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Visual FoxPro
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-060**](http://go.microsoft.com/fwlink/?linkid=254386)
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
Microsoft Visual FoxPro 8.0 Service Pack 1
</td>
<td style="border:1px solid black;">
[Microsoft Visual FoxPro 8.0 Service Pack 1](http://www.microsoft.com/downloads/details.aspx?familyid=0bef712a-b9e0-4ea9-98bf-68db366c8b8b)  
(KB2708940)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Visual FoxPro 9.0 Service Pack 2
</td>
<td style="border:1px solid black;">
[Microsoft Visual FoxPro 9.0 Service Pack 2](http://www.microsoft.com/downloads/details.aspx?familyid=1ee09491-4871-41ca-a39c-8360d5a568d4)  
(KB2708941)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Visual Basic
</th>
</tr>
<tr>
<td style="border:1px solid black;">
**Identificador del boletín**
</td>
<td style="border:1px solid black;">
[**MS12-060**](http://go.microsoft.com/fwlink/?linkid=254386)
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
Visual Basic 6.0 Runtime
</td>
<td style="border:1px solid black;">
[Visual Basic 6.0 Runtime](http://www.microsoft.com/downloads/details.aspx?familyid=847ec64b-95be-463b-bdfb-969e91fe3207)  
(KB2708437)  
(Crítica)
</td>
</tr>
</table>
 
**Nota para MS12-060**

Vea también las demás categorías de esta sección, **Ubicaciones de descarga y software afectado**, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software.

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

**Central de seguridad**

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://technet.microsoft.com/es-es/updatemanagement/bb245732). [TechNet Security Center](http://technet.microsoft.com/es-es/security) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar [Seguridad en el hogar](http://www.microsoft.com/es-es/security/default.aspx), donde esta información también está disponible haciendo clic en "Últimas actualizaciones de seguridad".

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

**System** **Center** **Configuration** **Manager**

La administración de actualizaciones de software de System Center Configuration Manager simplifica la tarea compleja de entregar y administrar actualizaciones para los sistemas de TI en toda la empresa. Con System Center Configuration Manager, los administradores de TI pueden ofrecer actualizaciones de los productos de Microsoft a una serie de dispositivos, incluidos equipos de escritorio, portátiles, servidores y dispositivos móviles.

La evaluación automática de vulnerabilidades en System Center Configuration Manager detecta las necesidades de actualizaciones e informa de las acciones recomendadas. La administración de actualizaciones de software en System Center Configuration Manager se basa en Microsoft Windows Software Update Services (WSUS), una infraestructura de actualizaciones probada con la que están familiarizados los administradores de TI de todo el mundo. Para obtener más información acerca de cómo los administradores pueden usar System Center Configuration Manager para implementar actualizaciones, vea [Administración de actualizaciones de software](http://www.microsoft.com/systemcenter/en/us/configuration-manager/cm-software-update-management.aspx). Para obtener más información acerca de System Center Configuration Manager, visite [System Center Configuration Manager](http://www.microsoft.com/systemcenter/en/us/configuration-manager.aspx).

**Systems** **Management Server 2003**

Microsoft Systems Management Server (SMS) ofrece una solución empresarial altamente configurable para la administración de las actualizaciones. Mediante SMS, los administradores pueden identificar los sistemas basados en Windows que necesitan actualizaciones de seguridad, así como realizar la implementación controlada de las actualizaciones en la empresa con una repercusión mínima para los usuarios finales.

**Nota** System Management Server 2003 está fuera del soporte técnico general desde el 12 de enero de 2010. Para obtener más información acerca de los ciclos de vida de los productos, visite [Ciclo de vida del soporte técnico de Microsoft](http://support.microsoft.com/common/international.aspx?rdpath=dm;en-us;lifecycle). Ya está disponible la siguiente versión de SMS, System Center Configuration Manager; vea la sección anterior, **System** **Center** **Configuration** **Manager**.

Para obtener más información acerca de cómo los administradores pueden usar SMS 2003 para implementar actualizaciones de seguridad, vea [Escenarios y procedimientos para Microsoft Systems Management Server 2003: Administración de distribución de software y revisiones](http://www.microsoft.com/downloads/en/details.aspx?familyid=32f2bb4c-42f8-4b8d-844f-2553fd78049f&displaylang=en). Para obtener información acerca de SMS, visite [Microsoft Systems Management Server TechCenter](http://technet.microsoft.com/en-us/systemcenter/bb545936.aspx).

**Nota** SMS utiliza las herramientas Microsoft Baseline Security Analyzer para proporcionar un amplio soporte técnico en la detección e implementación de las actualizaciones indicadas en los boletines de seguridad. Puede que estas herramientas no detecten algunas actualizaciones de software. Los administradores pueden usar las prestaciones de inventario de SMS en estos casos para concretar qué actualizaciones se deben aplicar en cada sistema. Para obtener más información sobre este procedimiento, vea [Implementar actualizaciones de software mediante la característica de distribución de software SMS](http://go.microsoft.com/fwlink/?linkid=33341). Algunas actualizaciones de seguridad pueden requerir derechos administrativos y que se reinicie el sistema. Los administradores pueden usar la utilidad Elevated Rights Deployment Tool (disponible en [SMS 2003 Administration Feature Pack](http://www.microsoft.com/downloads/en/details.aspx?familyid=7bd3a16e-1899-4e0b-bb99-1320e816167d&displaylang=en)) para instalar estas actualizaciones.

**Evaluador de compatibilidad de aplicaciones y kit de herramientas de compatibilidad de aplicaciones**

Las actualizaciones normalmente escriben en los mismos archivos y configuración del Registro necesarios para que se ejecuten las aplicaciones. Esto puede desencadenar incompatibilidades y aumentar el tiempo que dura la implementación de actualizaciones de seguridad. Puede optimizar las pruebas y la validación de las actualizaciones de Windows en las aplicaciones instaladas con los componentes del [Evaluador de compatibilidad de actualizaciones](http://technet.microsoft.com/library/cc749197) incluidos con el [Kit de herramientas de compatibilidad de aplicaciones](http://www.microsoft.com/downloads/details.aspx?familyid=24da89e9-b581-47b0-b45e-492dd6da2971&displaylang=en).

El kit de herramientas de compatibilidad de aplicaciones (ACT) contiene las herramientas y la documentación necesarias para evaluar y mitigar los problemas de compatibilidad de aplicaciones antes de implementar Windows Vista, una actualización de Windows, una actualización de seguridad de Microsoft o una nueva versión de Windows Internet Explorer en su entorno.

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

-   GWSlabs, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de un problema descrito en MS12-052
-   Derek Soeder, en colaboración con el programa [SecuriTeam Secure Disclosure de Beyond Security](http://www.beyondsecurity.com/ssd.html), por informar de un problema descrito en MS12-052
-   Sung-ting Tsai y Ming-Chieh Pan, de [Trend Micro](http://www.trendmicro.com/), por informar de un problema descrito en MS12-052
-   Cris Neckar de [Chrome Security Team de Google](http://chrome.google.com/) por informar de un problema descrito en MS12-052
-   Edward Torkington, de NCC Group, por informar de un problema descrito en MS12-053
-   Yamata Li, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de cuatro problemas descritos en MS12-054
-   [Mateusz "j00ru" Jurczyk](http://j00ru.vexillium.org/)
-   , de
-   [Google Inc](http://www.google.com/)
-   , por informar de un problema descrito en MS12-055
-   Cris Neckar de [Chrome Security Team de Google](http://chrome.google.com/) por informar de un problema descrito en MS12-056
-   [Andrei Costin](http://www.andreicostin.com)
-   , por informar de un problema descrito en MS12-057
-   Will Dorman, de [CERT/CC](http://www.cert.org/), por colaborar con nosotros en 13 problemas descritos en MS12-058
-   Alexander Gavrun, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [TippingPoint](http://www.hpenterprisesecurity.com/products/hp-tippingpoint-network-security/), por informar de un problema descrito en MS12-059

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Soluciones de seguridad para profesionales de TI: Soporte técnico y solución de problemas de seguridad de TechNet
-   Ayuda para proteger su equipo con Windows de virus y malware: [Solución antivirus y centro de seguridad](http://support.microsoft.com/contactus/cu_sc_virsec_master)
-   Soporte local según su país: [Soporte internacional](http://support.microsoft.com/common/international.aspx)

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (14 de agosto de 2012): Publicación del resumen del boletín.
-   V2.0 (9 de octubre de 2012): resumen del boletín revisado para que se corresponda con la nueva publicación de los paquetes de actualización de MS12-053, MS12-054, MS12-055 y MS12-058. Los clientes deben aplicar los paquetes de actualización publicados de nuevo para evitar un problema con certificados digitales descrito en el documento informativo sobre seguridad de Microsoft 2749655. Vea los boletines para obtener más información.
-   V3.0 (11 de diciembre de 2012): para MS12-057, se han reemplazado las actualizaciones KB2553260 y KB2589322 por las actualizaciones KB2687501 y KB2687510, respectivamente, para todas las ediciones afectadas de Microsoft Office 2010. Para MS12-059, se ha reemplazado la actualización KB2597171 por la actualización KB2687508 para todas las ediciones afectadas de Microsoft Visio 2010. Para MS12-060, se ha reemplazado la actualización KB2687323 por la actualización KB2726929 para los controles comunes de Windows en todas las variantes afectadas de Microsoft Office 2003, Microsoft Office 2003 Web Components y Microsoft SQL Server 2005.

*Built at 2014-04-18T01:50:00Z-07:00*
