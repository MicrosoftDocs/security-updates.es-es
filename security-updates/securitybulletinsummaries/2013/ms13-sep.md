---
TOCTitle: 'MS13-SEP'
Title: Resumen del boletín de seguridad de Microsoft de septiembre 2013
ms:assetid: 'ms13-sep'
ms:contentKeyID: 61225455
ms:mtpsurl: 'https://technet.microsoft.com/es-ES/library/ms13-sep(v=Security.10)'
---

Resumen del boletín de seguridad de Microsoft de septiembre 2013
================================================================

Publicado: martes, 10 de septiembre de 2013 | Actualizado: miércoles, 6 de noviembre de 2013

**Versión:** 1.1

Este resumen del boletín enumera los boletines de seguridad publicados para septiembre de 2013.

Con la publicación de los boletines de seguridad de septiembre de 2013, este resumen del boletín reemplaza la notificación de avance de boletines publicada originalmente el 5 de septiembre de 2013. Para obtener más información acerca del servicio de notificación de avance de boletines, vea [Notificación de avance de boletines de seguridad de Microsoft](http://go.microsoft.com/fwlink/?linkid=217213).

Para obtener información acerca de cómo recibir las notificaciones automáticas cuando se publiquen boletines de seguridad de Microsoft, visite [Microsoft Technical Security Notifications](http://go.microsoft.com/fwlink/?linkid=21163) (en inglés).

Microsoft va a realizar un webcast para atender las consultas de los clientes sobre estos boletines el 11 de septiembre de 2013, a las 11:00 a.m., hora del Pacífico (EE. UU. y Canadá). [Inscríbase ahora al webcast del boletín de seguridad de septiembre](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032557378&culture=en-us). Después de esta fecha, este webcast estará disponible [a petición](https://msevents.microsoft.com/cui/eventdetail.aspx?eventid=1032557378&culture=en-us).

Microsoft también proporciona información para ayudar a los clientes a asignar prioridades a las actualizaciones de seguridad mensuales con actualizaciones no relacionadas con la seguridad que se publicarán el mismo día que las actualizaciones de seguridad mensuales. Ver la sección, Información adicional.

### Información del boletín

#### Resúmenes ejecutivos

En la tabla siguiente se resumen los boletines de seguridad de este mes por orden de gravedad.

Para obtener detalles acerca del software afectado, vea la siguiente sección, Software afectado.

 
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=293350">MS13-067</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft SharePoint Server podrían permitir la ejecución remota de código (2834052)<br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma pública y nueve vulnerabilidades de las que se ha informado de forma privada en el software de Microsoft Office Server. La vulnerabilidad más grave podría permitir la ejecución remota de código en el contexto de una cuenta de servicio W3WP si un atacante envía contenido especialmente diseñado al servidor afectado.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office,<br />
Software de servidor de Microsoft</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=307055">MS13-068</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en Microsoft Outlook podría permitir la ejecución remota de código (2756473)<br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Outlook. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre u obtiene una vista previa de un mensaje de correo electrónico especialmente diseñado mediante una edición afectada de Microsoft Outlook. Un intruso que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario local. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320631">MS13-069</a></td>
<td style="border:1px solid black;">Actualización de seguridad acumulativa para Internet Explorer (2870699)<br />
<br />
Esta actualización de seguridad resuelve diez vulnerabilidades de las que se ha informado de forma privada en Internet Explorer. La más grave de las vulnerabilidades podría permitir la ejecución remota de código si un usuario, mediante Internet Explorer, visita una página web especialmente diseñada. Un atacante que aprovechara la más grave de estas vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows,<br />
Internet Explorer</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320629">MS13-070</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en OLE podría permitir la ejecución remota de código (2876217)<br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario abre un archivo que contiene un objeto OLE especialmente diseñado. Un atacante que aprovechara esta vulnerabilidad podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Crítica</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=314046">MS13-071</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en el archivo de tema de Windows podría permitir la ejecución remota de código (2864063)<br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la ejecución remota de código si un usuario aplica un tema de Windows especialmente diseñado en su sistema. En todos los casos, no se puede obligar al usuario a que abra el archivo o aplique el tema; para que el ataque se lleve a cabo, se debe convencer al usuario de que lo abra.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Office podrían permitir la ejecución remota de código (2845537)<br />
<br />
Esta actualización de seguridad resuelve 13 vulnerabilidades de las que se ha informado de forma privada enMicrosoft Office. Las vulnerabilidades más graves podrían permitir la ejecución remota de código si se abre un archivo especialmente diseñado en una versión afectada del software de Microsoft Office. Un atacante que aprovechara las vulnerabilidades más graves podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=293351">MS13-073</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Excel podrían permitir la ejecución remota de código (2858300)<br />
<br />
Esta actualización de seguridad resuelve tres vulnerabilidades de las que se ha informado de forma privada en Microsoft Office. Las vulnerabilidades más graves podrían permitir la ejecución remota de código si un usuario abre un archivo de Office especialmente diseñado con una versión afectada de Microsoft u otro software de Microsoft Office. Un atacante que aprovechara las vulnerabilidades más graves podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=308989">MS13-074</a></td>
<td style="border:1px solid black;">Vulnerabilidades en Microsoft Access podrían permitir la ejecución remota de código (2848637)<br />
<br />
Esta actualización de seguridad resuelve tres vulnerabilidades de las que se ha informado de forma privada en Microsoft Office. Las vulnerabilidades podrían permitir la ejecución remota de código si un usuario abre un archivo de Access especialmente diseñado con una versión afectada de Microsoft Access. Un atacante que aprovechara las vulnerabilidades podría conseguir el mismo nivel de derechos de usuario que el usuario actual. Los usuarios cuyas cuentas estén configuradas con menos derechos de usuario en el sistema correrían un riesgo menor que los que cuenten con derechos de usuario administrativos.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Ejecución remota de código</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=318022">MS13-075</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en Microsoft Office IME (chino) podría permitir la elevación de privilegios (2878687)<br />
<br />
Esta actualización de seguridad resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Office IME (chino). La vulnerabilidad podría permitir la elevación de privilegios si un atacante que ha iniciado la sesión inicia Internet Explorer desde la barra de herramientas en Microsoft Pinyin IME para chino simplificado. Un atacante que consiguiera aprovechar esta vulnerabilidad podría ejecutar código arbitrario en modo kernel. De esta forma, un intruso podría instalar programas; ver, cambiar o eliminar datos; o crear cuentas nuevas con todos los derechos administrativos. Solo las implementaciones de Microsoft Pinyin IME 2010 están afectadas por esta vulnerabilidad. Otras versiones de IME de chino simplificado y otras implementaciones de IME no están afectadas.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320624">MS13-076</a></td>
<td style="border:1px solid black;">Vulnerabilidades en los controladores modo kernel podrían permitir la elevación de privilegios (2876315)<br />
<br />
Esta actualización de seguridad resuelve siete vulnerabilidades de las que se ha informado de forma privada en Microsoft Windows. Las vulnerabilidades podrían permitir la elevación de privilegios si un atacante inicia sesión en el sistema y ejecuta una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, un atacante debe de tener unas credenciales de inicio de sesión válidas y ser capaz de aprovechar estas vulnerabilidades.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320630">MS13-077</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en el Administrador de control de servicios de Windows podría permitir la elevación de privilegios (2872339)<br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft Windows. La vulnerabilidad podría permitir la elevación de privilegios si un atacante convence a un usuario autenticado para que ejecute una aplicación especialmente diseñada. Para aprovechar esta vulnerabilidad, el atacante debe tener credenciales de inicio de sesión válidas y poder iniciar sesión localmente o convencer a un usuario para que ejecute la aplicación especialmente diseñada del atacante.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Elevación de privilegios</td>
<td style="border:1px solid black;">Requiere reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=318021">MS13-078</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en FrontPage podría permitir la divulgación de información (2825621)<br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Microsoft FrontPage. La vulnerabilidad podría permitir la divulgación de información si un usuario abre un documento de FrontPage especialmente diseñado. La vulnerabilidad no se puede aprovechar automáticamente; para que se realice el ataque, se debe convencer a un usuario para que abra el documento especialmente diseñado.</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Divulgación de información</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Office</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320666">MS13-079</a></td>
<td style="border:1px solid black;">Una vulnerabilidad en Active Directory podría permitir la denegación de servicio (2853587)<br />
<br />
Esta actualización de seguridad crítica resuelve una vulnerabilidad de la que se ha informado de forma privada en Active Directory. La vulnerabilidad podría permitir la denegación de servicio si un atacante envía una consulta especialmente diseñada al servicio de protocolo ligero de acceso a directorios (LDAP).</td>
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=21140">Importante</a> <br />
Denegación de servicio</td>
<td style="border:1px solid black;">Puede requerir reinicio</td>
<td style="border:1px solid black;">Microsoft Windows</td>
</tr>
</tbody>
</table>
  
Índice de explotabilidad  
------------------------
  
La siguiente tabla proporciona una evaluación de explotabilidad de cada una de las vulnerabilidades tratadas este mes. Las vulnerabilidades se enumeran por orden de identificador de boletín y, a continuación, por identificador de CVE. Sólo se incluyen las vulnerabilidades que tiene una clasificación de gravedad de crítica o importante en los boletines.
  
¿Cómo se usa esta tabla?
  
Use esta tabla para obtener información acerca de la probabilidad de las vulnerabilidades de ejecución de código y de denegación de servicio en el plazo de 30 días desde la publicación del boletín de seguridad para cada una de las actualizaciones que deba instalar. Revise cada una de las evaluaciones siguientes, según su configuración específica, con el fin de asignar prioridades a la implementación de las actualizaciones de este mes. Para obtener más información acerca de lo que significan estas clasificaciones y cómo se determinan, vea el [índice de explotabilidad de Microsoft](http://technet.microsoft.com/es-es/security/cc998259.aspx).
  
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
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=293350">MS13-067</a></td>
<td style="border:1px solid black;">Vulnerabilidad de denegación de servicio en SharePoint</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0081">CVE-2013-0081</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=293350">MS13-067</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Microsoft Office</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1315">CVE-2013-1315</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad también afecta a <a href="http://go.microsoft.com/fwlink/?linkid=293351">MS13-073</a>.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=293350">MS13-067</a></td>
<td style="border:1px solid black;">Vulnerabilidad de deshabilitación de MAC</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1330">CVE-2013-1330</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=293350">MS13-067</a></td>
<td style="border:1px solid black;">Vulnerabilidad de XSS en SharePoint</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3179">CVE-2013-3179</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=293350">MS13-067</a></td>
<td style="border:1px solid black;">Vulnerabilidad de XSS en POST</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3180">CVE-2013-3180</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esa vulnerabilidad ya se ha divulgado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=293350">MS13-067</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3847">CVE-2013-3847</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad también afecta a <a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a>.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=293350">MS13-067</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3848">CVE-2013-3848</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad también afecta a <a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a>.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=293350">MS13-067</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3849">CVE-2013-3849</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad también afecta a <a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a>.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=293350">MS13-067</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3857">CVE-2013-3857</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad también afecta a <a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a><a href="http://go.microsoft.com/fwlink/?linkid=293350"></a>.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=293350">MS13-067</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3858">CVE-2013-3858</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad también afecta a <a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a><a href="http://go.microsoft.com/fwlink/?linkid=293350"></a>.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=307055">MS13-068</a></td>
<td style="border:1px solid black;">Vulnerabilidad de certificado de mensaje</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3870">CVE-2013-3870</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320631">MS13-069</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3201">CVE-2013-3201</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Internet Explorer 11 no está afectado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320631">MS13-069</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3202">CVE-2013-3202</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Internet Explorer 11 no está afectado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320631">MS13-069</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3203">CVE-2013-3203</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Internet Explorer 11 no está afectado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320631">MS13-069</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3204">CVE-2013-3204</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Internet Explorer 11 no está afectado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320631">MS13-069</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3205">CVE-2013-3205</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Internet Explorer 11 no está afectado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320631">MS13-069</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3206">CVE-2013-3206</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Internet Explorer 11 no está afectado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320631">MS13-069</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3207">CVE-2013-3207</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Internet Explorer 11 no está afectado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320631">MS13-069</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3208">CVE-2013-3208</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Internet Explorer 11 no está afectado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320631">MS13-069</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3209">CVE-2013-3209</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Internet Explorer 11 no está afectado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320631">MS13-069</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria de Internet Explorer</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3845">CVE-2013-3845</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Internet Explorer 11 no está afectado.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320629">MS13-070</a></td>
<td style="border:1px solid black;">Vulnerabilidad de propiedad OLE</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3863">CVE-2013-3863</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Windows 8.1 y Windows Server 2012 R2 no están afectados.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=314046">MS13-071</a></td>
<td style="border:1px solid black;">Vulnerabilidad de ejecución remota de código en archivos de tema de Windows</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-0810">CVE-2013-0810</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Windows 8.1 y Windows Server 2012 R2 no están afectados.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad de resolución de entidades XML externas</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3160">CVE-2013-3160</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3847">CVE-2013-3847</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad también afecta a <a href="http://go.microsoft.com/fwlink/?linkid=293350">MS13-067</a>.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3848">CVE-2013-3848</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad también afecta a <a href="http://go.microsoft.com/fwlink/?linkid=293350">MS13-067</a>.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3849">CVE-2013-3849</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad también afecta a <a href="http://go.microsoft.com/fwlink/?linkid=293350">MS13-067</a>.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3850">CVE-2013-3850</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3851">CVE-2013-3851</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3852">CVE-2013-3852</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3853">CVE-2013-3853</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3854">CVE-2013-3854</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3855">CVE-2013-3855</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3856">CVE-2013-3856</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3857">CVE-2013-3857</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad también afecta a <a href="http://go.microsoft.com/fwlink/?linkid=293350">MS13-067</a>.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=299217">MS13-072</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Word</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3858">CVE-2013-3858</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad también afecta a <a href="http://go.microsoft.com/fwlink/?linkid=293350">MS13-067</a>.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=293351">MS13-073</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Microsoft Office</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1315">CVE-2013-1315</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad también afecta a <a href="http://go.microsoft.com/fwlink/?linkid=293350">MS13-067</a>.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=293351">MS13-073</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Microsoft Office</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3158">CVE-2013-3158</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=293351">MS13-073</a></td>
<td style="border:1px solid black;">Vulnerabilidad de resolución de entidades XML externas</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3159">CVE-2013-3159</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=308989">MS13-074</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Access</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3155">CVE-2013-3155</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=308989">MS13-074</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con el formato de archivo de Access</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3156">CVE-2013-3156</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=308989">MS13-074</a></td>
<td style="border:1px solid black;">Vulnerabilidad de daños en la memoria relacionada con Access</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3157">CVE-2013-3157</a></td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=318022">MS13-075</a></td>
<td style="border:1px solid black;">Vulnerabilidad en IME para chino</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3859">CVE-2013-3859</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">(Ninguna)</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320624">MS13-076</a></td>
<td style="border:1px solid black;">Vulnerabilidad de varias capturas en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1341">CVE-2013-1341</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Windows 8.1 y Windows Server 2012 R2 no están afectados.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320624">MS13-076</a></td>
<td style="border:1px solid black;">Vulnerabilidad de varias capturas en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1342">CVE-2013-1342</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Windows 8.1 y Windows Server 2012 R2 no están afectados.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320624">MS13-076</a></td>
<td style="border:1px solid black;">Vulnerabilidad de varias capturas en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1343">CVE-2013-1343</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Windows 8.1 y Windows Server 2012 R2 no están afectados.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320624">MS13-076</a></td>
<td style="border:1px solid black;">Vulnerabilidad de varias capturas en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-1344">CVE-2013-1344</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Windows 8.1 y Windows Server 2012 R2 no están afectados.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320624">MS13-076</a></td>
<td style="border:1px solid black;">Vulnerabilidad de varias capturas en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3864">CVE-2013-3864</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Windows 8.1 y Windows Server 2012 R2 no están afectados.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320624">MS13-076</a></td>
<td style="border:1px solid black;">Vulnerabilidad de varias capturas en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3865">CVE-2013-3865</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">1</a> - Probabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Windows 8.1 y Windows Server 2012 R2 no están afectados.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320624">MS13-076</a></td>
<td style="border:1px solid black;">Vulnerabilidad de elevación de privilegios en Win32k</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3866">CVE-2013-3866</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad en Windows 8 y Windows Server 2012.<br />
<br />
Windows 8.1 y Windows Server 2012 R2 no están afectados.<br />
<br />
Se trata de una vulnerabilidad de divulgación de información que podría conllevar la elevación de privilegios en otro software afectado.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320630">MS13-077</a></td>
<td style="border:1px solid black;">Vulnerabilidad de doble liberación en el Administrador de control de servicios</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3862">CVE-2013-3862</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">2</a> - Dificultad para crear código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Windows 8.1 y Windows Server 2012 R2 no están afectados.</td>
</tr>
<tr class="even">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=318021">MS13-078</a></td>
<td style="border:1px solid black;">Vulnerabilidad de divulgación en XML</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3137">CVE-2013-3137</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">No aplicable</td>
<td style="border:1px solid black;">Esta vulnerabilidad afecta a la divulgación de información.</td>
</tr>
<tr class="odd">
<td style="border:1px solid black;"><a href="http://go.microsoft.com/fwlink/?linkid=320666">MS13-079</a></td>
<td style="border:1px solid black;">Vulnerabilidad de denegación de servicio anónima remota</td>
<td style="border:1px solid black;"><a href="http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=cve-2013-3868">CVE-2013-3868</a></td>
<td style="border:1px solid black;">No está afectada</td>
<td style="border:1px solid black;"><a href="http://technet.microsoft.com/security/cc998259">3</a> - Improbabilidad de código que aproveche la vulnerabilidad</td>
<td style="border:1px solid black;">Permanente</td>
<td style="border:1px solid black;">Se trata de una vulnerabilidad de denegación de servicio.<br />
<br />
Windows 8.1 y Windows Server 2012 R2 no están afectados.</td>
</tr>
</tbody>
</table>
 

Software afectado
-----------------

Las siguientes tablas enumeran los boletines en orden de categoría de software principal y gravedad.

¿Cómo se usan estas tablas?

Estas tablas se pueden usar para conocer las actualizaciones de seguridad que quizá deba instalar. Debe revisar cada programa de software o componente enumerado para ver si hay alguna actualización de seguridad que corresponda a su instalación. Si se enumera un programa o componente de software, también se muestra la clasificación de gravedad de dicha actualización de software.

Nota Puede que tenga que instalar varias actualizaciones de seguridad para una sola vulnerabilidad. Revise toda la columna para cada identificador de boletín enumerado con el fin de comprobar las actualizaciones que debe instalar según los programas o componentes instalados en el sistema.

#### Componentes y sistema operativo Windows

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="7" style="border:1px solid black;">
Windows XP
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-069](http://go.microsoft.com/fwlink/?linkid=320631)
</td>
<td style="border:1px solid black;">
[MS13-070](http://go.microsoft.com/fwlink/?linkid=320629)
</td>
<td style="border:1px solid black;">
[MS13-071](http://go.microsoft.com/fwlink/?linkid=314046)
</td>
<td style="border:1px solid black;">
[MS13-076](http://go.microsoft.com/fwlink/?linkid=320624)
</td>
<td style="border:1px solid black;">
[MS13-077](http://go.microsoft.com/fwlink/?linkid=320630)
</td>
<td style="border:1px solid black;">
[MS13-079](http://go.microsoft.com/fwlink/?linkid=320666)
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
Internet Explorer 6   
(2870699)  
(Crítica)  
Internet Explorer 7   
(2870699)  
(Crítica)  
Internet Explorer 8   
(2870699)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows XP Service Pack 3  
(2876217)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows XP Service Pack 3  
(2864063)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows XP Service Pack 3  
(2876315)  
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
Internet Explorer 6   
(2870699)  
(Crítica)  
Internet Explorer 7   
(2870699)  
(Crítica)  
Internet Explorer 8   
(2870699)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2  
(2876217)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2  
(2864063)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows XP Professional x64 Edition Service Pack 2  
(2876315)  
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
<th colspan="7" style="border:1px solid black;">
Windows Server 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-069](http://go.microsoft.com/fwlink/?linkid=320631)
</td>
<td style="border:1px solid black;">
[MS13-070](http://go.microsoft.com/fwlink/?linkid=320629)
</td>
<td style="border:1px solid black;">
[MS13-071](http://go.microsoft.com/fwlink/?linkid=314046)
</td>
<td style="border:1px solid black;">
[MS13-076](http://go.microsoft.com/fwlink/?linkid=320624)
</td>
<td style="border:1px solid black;">
[MS13-077](http://go.microsoft.com/fwlink/?linkid=320630)
</td>
<td style="border:1px solid black;">
[MS13-079](http://go.microsoft.com/fwlink/?linkid=320666)
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
Internet Explorer 6   
(2870699)  
(Moderada)  
Internet Explorer 7  
(2870699)  
(Moderada)  
Internet Explorer 8  
(2870699)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(2876217)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(2864063)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 Service Pack 2  
(2876315)  
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
Internet Explorer 6   
(2870699)  
(Moderada)  
Internet Explorer 7  
(2870699)  
(Moderada)  
Internet Explorer 8  
(2870699)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2876217)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2864063)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 x64 Edition Service Pack 2  
(2876315)  
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
Internet Explorer 6   
(2870699)  
(Moderada)  
Internet Explorer 7  
(2870699)  
(Moderada)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2876217)  
(Crítica)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2864063)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2003 con SP2 para sistemas con Itanium  
(2876315)  
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
<th colspan="7" style="border:1px solid black;">
Windows Vista
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-069](http://go.microsoft.com/fwlink/?linkid=320631)
</td>
<td style="border:1px solid black;">
[MS13-070](http://go.microsoft.com/fwlink/?linkid=320629)
</td>
<td style="border:1px solid black;">
[MS13-071](http://go.microsoft.com/fwlink/?linkid=314046)
</td>
<td style="border:1px solid black;">
[MS13-076](http://go.microsoft.com/fwlink/?linkid=320624)
</td>
<td style="border:1px solid black;">
[MS13-077](http://go.microsoft.com/fwlink/?linkid=320630)
</td>
<td style="border:1px solid black;">
[MS13-079](http://go.microsoft.com/fwlink/?linkid=320666)
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
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Vista Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2870699)  
(Crítica)  
Internet Explorer 8  
(2870699)  
(Crítica)  
Internet Explorer 9   
(2870699)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2864063)  
(Sin clasificación de gravedad)
</td>
<td style="border:1px solid black;">
Windows Vista Service Pack 2  
(2876315)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Active Directory Lightweight Directory Services (AD LDS)  
(2853587)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2870699)  
(Crítica)  
Internet Explorer 8  
(2870699)  
(Crítica)  
Internet Explorer 9   
(2870699)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2864063)  
(Sin clasificación de gravedad)
</td>
<td style="border:1px solid black;">
Windows Vista x64 Edition Service Pack 2  
(2876315)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Active Directory Lightweight Directory Services (AD LDS)  
(2853587)  
(Importante)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Server 2008
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-069](http://go.microsoft.com/fwlink/?linkid=320631)
</td>
<td style="border:1px solid black;">
[MS13-070](http://go.microsoft.com/fwlink/?linkid=320629)
</td>
<td style="border:1px solid black;">
[MS13-071](http://go.microsoft.com/fwlink/?linkid=314046)
</td>
<td style="border:1px solid black;">
[MS13-076](http://go.microsoft.com/fwlink/?linkid=320624)
</td>
<td style="border:1px solid black;">
[MS13-077](http://go.microsoft.com/fwlink/?linkid=320630)
</td>
<td style="border:1px solid black;">
[MS13-079](http://go.microsoft.com/fwlink/?linkid=320666)
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
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2870699)  
(Moderada)  
Internet Explorer 8  
(2870699)  
(Moderada)  
Internet Explorer 9   
(2870699)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2864063)  
(Sin clasificación de gravedad)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas de 32 bits Service Pack 2  
(2876315)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Servicios de Active Directory  
(2853587)  
(Importante)  
Active Directory Lightweight Directory Services (AD LDS)  
(2853587)  
(Importante)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2870699)  
(Moderada)  
Internet Explorer 8  
(2870699)  
(Moderada)  
Internet Explorer 9   
(2870699)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2864063)  
(Sin clasificación de gravedad)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas x64 Service Pack 2  
(2876315)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Servicios de Active Directory  
(2853587)  
(Importante)  
Active Directory Lightweight Directory Services (AD LDS)  
(2853587)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2
</td>
<td style="border:1px solid black;">
Internet Explorer 7  
(2870699)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2864063)  
(Sin clasificación de gravedad)
</td>
<td style="border:1px solid black;">
Windows Server 2008 para sistemas con Itanium Service Pack 2  
(2876315)  
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
<th colspan="7" style="border:1px solid black;">
Windows 7
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-069](http://go.microsoft.com/fwlink/?linkid=320631)
</td>
<td style="border:1px solid black;">
[MS13-070](http://go.microsoft.com/fwlink/?linkid=320629)
</td>
<td style="border:1px solid black;">
[MS13-071](http://go.microsoft.com/fwlink/?linkid=314046)
</td>
<td style="border:1px solid black;">
[MS13-076](http://go.microsoft.com/fwlink/?linkid=320624)
</td>
<td style="border:1px solid black;">
[MS13-077](http://go.microsoft.com/fwlink/?linkid=320630)
</td>
<td style="border:1px solid black;">
[MS13-079](http://go.microsoft.com/fwlink/?linkid=320666)
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2870699)  
(Crítica)  
Internet Explorer 9   
(2870699)  
(Crítica)  
Internet Explorer 10   
(2870699)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2876315)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas de 32 bits Service Pack 1  
(2872339)  
(Importante)
</td>
<td style="border:1px solid black;">
Active Directory Lightweight Directory Services (AD LDS)  
(2853587)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2870699)  
(Crítica)  
Internet Explorer 9   
(2870699)  
(Crítica)  
Internet Explorer 10   
(2870699)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2876315)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows 7 para sistemas x64 Service Pack 1  
(2872339)  
(Importante)
</td>
<td style="border:1px solid black;">
Active Directory Lightweight Directory Services (AD LDS)  
(2853587)  
(Importante)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Server 2008 R2
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-069](http://go.microsoft.com/fwlink/?linkid=320631)
</td>
<td style="border:1px solid black;">
[MS13-070](http://go.microsoft.com/fwlink/?linkid=320629)
</td>
<td style="border:1px solid black;">
[MS13-071](http://go.microsoft.com/fwlink/?linkid=314046)
</td>
<td style="border:1px solid black;">
[MS13-076](http://go.microsoft.com/fwlink/?linkid=320624)
</td>
<td style="border:1px solid black;">
[MS13-077](http://go.microsoft.com/fwlink/?linkid=320630)
</td>
<td style="border:1px solid black;">
[MS13-079](http://go.microsoft.com/fwlink/?linkid=320666)
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2870699)  
(Moderada)  
Internet Explorer 9   
(2870699)  
(Moderada)  
Internet Explorer 10   
(2870699)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2876315)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1  
(2872339)  
(Importante)
</td>
<td style="border:1px solid black;">
Servicios de Active Directory  
(2853587)  
(Importante)  
Active Directory Lightweight Directory Services (AD LDS)  
(2853587)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1
</td>
<td style="border:1px solid black;">
Internet Explorer 8  
(2870699)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2876315)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas con Itanium Service Pack 1  
(2872339)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows 8
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-069](http://go.microsoft.com/fwlink/?linkid=320631)
</td>
<td style="border:1px solid black;">
[MS13-070](http://go.microsoft.com/fwlink/?linkid=320629)
</td>
<td style="border:1px solid black;">
[MS13-071](http://go.microsoft.com/fwlink/?linkid=314046)
</td>
<td style="border:1px solid black;">
[MS13-076](http://go.microsoft.com/fwlink/?linkid=320624)
</td>
<td style="border:1px solid black;">
[MS13-077](http://go.microsoft.com/fwlink/?linkid=320630)
</td>
<td style="border:1px solid black;">
[MS13-079](http://go.microsoft.com/fwlink/?linkid=320666)
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2870699)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 32 bits  
(2876315)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Active Directory Lightweight Directory Services (AD LDS)  
(2853587)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows 8 para sistemas de 64 bits
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2870699)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows 8 para sistemas de 64 bits  
(2876315)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Active Directory Lightweight Directory Services (AD LDS)  
(2853587)  
(Importante)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows Server 2012
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-069](http://go.microsoft.com/fwlink/?linkid=320631)
</td>
<td style="border:1px solid black;">
[MS13-070](http://go.microsoft.com/fwlink/?linkid=320629)
</td>
<td style="border:1px solid black;">
[MS13-071](http://go.microsoft.com/fwlink/?linkid=314046)
</td>
<td style="border:1px solid black;">
[MS13-076](http://go.microsoft.com/fwlink/?linkid=320624)
</td>
<td style="border:1px solid black;">
[MS13-077](http://go.microsoft.com/fwlink/?linkid=320630)
</td>
<td style="border:1px solid black;">
[MS13-079](http://go.microsoft.com/fwlink/?linkid=320666)
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
</tr>
<tr>
<td style="border:1px solid black;">
Windows Server 2012
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2870699)  
(Moderada)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows Server 2012  
(2876315)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Servicios de Active Directory  
(2853587)  
(Importante)  
Active Directory Lightweight Directory Services (AD LDS)  
(2853587)  
(Importante)
</td>
</tr>
<tr>
<th colspan="7" style="border:1px solid black;">
Windows RT
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-069](http://go.microsoft.com/fwlink/?linkid=320631)
</td>
<td style="border:1px solid black;">
[MS13-070](http://go.microsoft.com/fwlink/?linkid=320629)
</td>
<td style="border:1px solid black;">
[MS13-071](http://go.microsoft.com/fwlink/?linkid=314046)
</td>
<td style="border:1px solid black;">
[MS13-076](http://go.microsoft.com/fwlink/?linkid=320624)
</td>
<td style="border:1px solid black;">
[MS13-077](http://go.microsoft.com/fwlink/?linkid=320630)
</td>
<td style="border:1px solid black;">
[MS13-079](http://go.microsoft.com/fwlink/?linkid=320666)
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
Ninguna
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Windows RT
</td>
<td style="border:1px solid black;">
Internet Explorer 10   
(2870699)  
(Crítica)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Windows RT  
(2876315)  
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
<th colspan="7" style="border:1px solid black;">
Opción de instalación Server Core
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-069](http://go.microsoft.com/fwlink/?linkid=320631)
</td>
<td style="border:1px solid black;">
[MS13-070](http://go.microsoft.com/fwlink/?linkid=320629)
</td>
<td style="border:1px solid black;">
[MS13-071](http://go.microsoft.com/fwlink/?linkid=314046)
</td>
<td style="border:1px solid black;">
[MS13-076](http://go.microsoft.com/fwlink/?linkid=320624)
</td>
<td style="border:1px solid black;">
[MS13-077](http://go.microsoft.com/fwlink/?linkid=320630)
</td>
<td style="border:1px solid black;">
[MS13-079](http://go.microsoft.com/fwlink/?linkid=320666)
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
Windows Server 2008 para sistemas de 32 bits Service Pack 2 (instalación Server Core)  
(2876315)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Servicios de Active Directory  
(2853587)  
(Importante)  
Active Directory Lightweight Directory Services (AD LDS)  
(2853587)  
(Importante)
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
Windows Server 2008 para sistemas x64 Service Pack 2 (instalación Server Core)  
(2876315)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Servicios de Active Directory  
(2853587)  
(Importante)  
Active Directory Lightweight Directory Services (AD LDS)  
(2853587)  
(Importante)
</td>
</tr>
<tr>
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
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2876315)  
(Importante)
</td>
<td style="border:1px solid black;">
Windows Server 2008 R2 para sistemas x64 Service Pack 1 (instalación Server Core)  
(2872339)
</td>
<td style="border:1px solid black;">
Servicios de Active Directory  
(2853587)  
(Importante)  
Active Directory Lightweight Directory Services (AD LDS)  
(2853587)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
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
Windows Server 2012 (instalación Server Core)  
(2876315)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Servicios de Active Directory  
(2853587)  
(Importante)  
Active Directory Lightweight Directory Services (AD LDS)  
(2853587)  
(Importante)
</td>
</tr>
</table>
 

#### Conjuntos de programas y software de Microsoft Office

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="6" style="border:1px solid black;">
Microsoft Office 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-068](http://go.microsoft.com/fwlink/?linkid=307055)
</td>
<td style="border:1px solid black;">
[MS13-072](http://go.microsoft.com/fwlink/?linkid=299217)
</td>
<td style="border:1px solid black;">
[MS13-073](http://go.microsoft.com/fwlink/?linkid=293351)
</td>
<td style="border:1px solid black;">
[MS13-074](http://go.microsoft.com/fwlink/?linkid=308989)
</td>
<td style="border:1px solid black;">
[MS13-075](http://go.microsoft.com/fwlink/?linkid=318022)
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
Microsoft Office 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft Office 2003 Service Pack 3  
(MSO)  
(2817474)  
(Importante)  
Microsoft Word 2003 Service Pack 3  
(2817682)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Excel 2003 Service Pack 3  
(2810048)  
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
<th colspan="6" style="border:1px solid black;">
Microsoft Office 2007
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-068](http://go.microsoft.com/fwlink/?linkid=307055)
</td>
<td style="border:1px solid black;">
[MS13-072](http://go.microsoft.com/fwlink/?linkid=299217)
</td>
<td style="border:1px solid black;">
[MS13-073](http://go.microsoft.com/fwlink/?linkid=293351)
</td>
<td style="border:1px solid black;">
[MS13-074](http://go.microsoft.com/fwlink/?linkid=308989)
</td>
<td style="border:1px solid black;">
[MS13-075](http://go.microsoft.com/fwlink/?linkid=318022)
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
Microsoft Office 2007 Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft Outlook 2007 Service Pack 3  
(2825999)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft Office 2007 Service Pack 3  
(MSO)  
(2760411)  
(Importante)  
Microsoft Office 2007 Service Pack 3  
(MSPTLS)  
(2597973)  
(Importante)  
Microsoft Word 2007 Service Pack 3  
(2767773)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Excel 2007 Service Pack 3  
(2760583)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Access 2007 Service Pack 3  
(2596825)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Microsoft Office 2010
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-068](http://go.microsoft.com/fwlink/?linkid=307055)
</td>
<td style="border:1px solid black;">
[MS13-072](http://go.microsoft.com/fwlink/?linkid=299217)
</td>
<td style="border:1px solid black;">
[MS13-073](http://go.microsoft.com/fwlink/?linkid=293351)
</td>
<td style="border:1px solid black;">
[MS13-074](http://go.microsoft.com/fwlink/?linkid=308989)
</td>
<td style="border:1px solid black;">
[MS13-075](http://go.microsoft.com/fwlink/?linkid=318022)
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
Microsoft Office 2010 Service Pack 1 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Outlook 2010 Service Pack 1 (ediciones de 32 bits)  
(2794707)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft Word 2010 Service Pack 1 (ediciones de 32 bits)  
(2760769)  
(Importante)  
Microsoft Word 2010 Service Pack 1 (ediciones de 32 bits)  
(2767913)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Excel 2010 Service Pack 1 (ediciones de 32 bits)  
(2760597)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Access 2010 Service Pack 1 (ediciones de 32 bits)  
(2687423)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Pinyin IME 2010 (versión de 32 bits)  
(2687413)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Outlook 2010 Service Pack 2 (ediciones de 32 bits)  
(2794707)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft Word 2010 Service Pack 2 (ediciones de 32 bits)  
(2760769)  
(Importante)  
Microsoft Word 2010 Service Pack 2 (ediciones de 32 bits)  
(2767913)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Excel 2010 Service Pack 2 (ediciones de 32 bits)  
(2760597)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Access 2010 Service Pack 2 (ediciones de 32 bits)  
(2687423)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 1 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Outlook 2010 Service Pack 1 (ediciones de 64 bits)  
(2794707)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft Word 2010 Service Pack 1 (ediciones de 64 bits)  
(2760769)  
(Importante)  
Microsoft Word 2010 Service Pack 1 (ediciones de 64 bits)  
(2767913)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Excel 2010 Service Pack 1 (ediciones de 64 bits)  
(2760597)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Access 2010 Service Pack 1 (ediciones de 64 bits)  
(2687423)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Pinyin IME 2010 (versión de 64 bits)  
(2687413)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2010 Service Pack 2 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Outlook 2010 Service Pack 2 (ediciones de 64 bits)  
(2794707)  
(Crítica)
</td>
<td style="border:1px solid black;">
Microsoft Word 2010 Service Pack 2 (ediciones de 64 bits)  
(2760769)  
(Importante)  
Microsoft Word 2010 Service Pack 2 (ediciones de 64 bits)  
(2767913)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Excel 2010 Service Pack 2 (ediciones de 64 bits)  
(2760597)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Access 2010 Service Pack 2 (ediciones de 64 bits)  
(2687423)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<th colspan="6" style="border:1px solid black;">
Microsoft Office 2013
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-068](http://go.microsoft.com/fwlink/?linkid=307055)
</td>
<td style="border:1px solid black;">
[MS13-072](http://go.microsoft.com/fwlink/?linkid=299217)
</td>
<td style="border:1px solid black;">
[MS13-073](http://go.microsoft.com/fwlink/?linkid=293351)
</td>
<td style="border:1px solid black;">
[MS13-074](http://go.microsoft.com/fwlink/?linkid=308989)
</td>
<td style="border:1px solid black;">
[MS13-075](http://go.microsoft.com/fwlink/?linkid=318022)
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
Microsoft Office 2013 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft Excel 2013 (ediciones de 32 bits)  
(2768017)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Access 2013 (ediciones de 32 bits)  
(2810009)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office 2013 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft Excel 2013 (ediciones de 64 bits)  
(2768017)  
(Importante)
</td>
<td style="border:1px solid black;">
Microsoft Access 2013 (ediciones de 64 bits)  
(2810009)  
(Importante)
</td>
<td style="border:1px solid black;">
No aplicable
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office 2013 RT
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft Excel 2013 RT  
(2768017)  
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
<th colspan="6" style="border:1px solid black;">
Microsoft Office para Mac
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-068](http://go.microsoft.com/fwlink/?linkid=307055)
</td>
<td style="border:1px solid black;">
[MS13-072](http://go.microsoft.com/fwlink/?linkid=299217)
</td>
<td style="border:1px solid black;">
[MS13-073](http://go.microsoft.com/fwlink/?linkid=293351)
</td>
<td style="border:1px solid black;">
[MS13-074](http://go.microsoft.com/fwlink/?linkid=308989)
</td>
<td style="border:1px solid black;">
[MS13-075](http://go.microsoft.com/fwlink/?linkid=318022)
</td>
</tr>
<tr>
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
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
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
Microsoft Office para Mac 2011
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft Office para Mac 2011  
(2877813)  
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
<th colspan="6" style="border:1px solid black;">
Otro software de Microsoft Office
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-068](http://go.microsoft.com/fwlink/?linkid=307055)
</td>
<td style="border:1px solid black;">
[MS13-072](http://go.microsoft.com/fwlink/?linkid=299217)
</td>
<td style="border:1px solid black;">
[MS13-073](http://go.microsoft.com/fwlink/?linkid=293351)
</td>
<td style="border:1px solid black;">
[MS13-074](http://go.microsoft.com/fwlink/?linkid=308989)
</td>
<td style="border:1px solid black;">
[MS13-075](http://go.microsoft.com/fwlink/?linkid=318022)
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
Paquete de compatibilidad de Microsoft Office Service Pack 3
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office Service Pack 3  
(2760823)  
(Importante)
</td>
<td style="border:1px solid black;">
Paquete de compatibilidad de Microsoft Office Service Pack 3  
(2760588)  
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
Microsoft Word Viewer
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft Word Viewer  
(2817683)  
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
Microsoft Excel Viewer
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
No aplicable
</td>
<td style="border:1px solid black;">
Microsoft Excel Viewer  
(2760590)  
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
 

#### Software de servidor de Microsoft

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft SharePoint Portal Server 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-067](http://go.microsoft.com/fwlink/?linkid=293350)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Portal Server 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft Windows SharePoint Services 2.0  
(2810061)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft SharePoint Server 2007
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-067](http://go.microsoft.com/fwlink/?linkid=293350)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2007 Service Pack 3 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Microsoft Windows SharePoint Services 3.0 Service Pack 3 (versiones de 32 bits)  
(2760420)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2007 Service Pack 3 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Microsoft Windows SharePoint Services 3.0 Service Pack 3 (versiones de 64 bits)  
(2760420)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft SharePoint Server 2010
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-067](http://go.microsoft.com/fwlink/?linkid=293350)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Foundation 2010 Service Pack 1 (wss)  
(2810067)  
(Crítica)  
Microsoft SharePoint Server 2010 Service Pack 1 (coreserver)  
(2817393)  
(Crítica)  
Microsoft SharePoint Server 2010 Service Pack 1 (wosrv)  
(2817372)  
(Crítica)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2010 Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Foundation 2010 Service Pack 2 (wss)  
(2810067)  
(Crítica)  
Microsoft SharePoint Server 2010 Service Pack 2 (coreserver)  
(2817393)  
(Crítica)  
Microsoft SharePoint Server 2010 Service Pack 2 (wosrv)  
(2817372)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft SharePoint Server 2013
</th>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-067](http://go.microsoft.com/fwlink/?linkid=293350)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2013
</td>
<td style="border:1px solid black;">
Microsoft SharePoint Foundation 2013  
(2817315)  
(Importante)  
Microsoft SharePoint Server 2013 (coreserverloc)  
(2810083)  
(Importante)
</td>
</tr>
</table>
 
Nota para MS13-067

Vea también las demás categorías de esta sección, Software afectado, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software

#### Microsoft Office Services y Web Apps

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft SharePoint Server 2007
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-067](http://go.microsoft.com/fwlink/?linkid=293350)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2007 Service Pack 3 (ediciones de 32 bits)
</td>
<td style="border:1px solid black;">
Excel Services  
(2760589)  
(Importante)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2007 Service Pack 3 (ediciones de 64 bits)
</td>
<td style="border:1px solid black;">
Excel Services  
(2760589)  
(Importante)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft SharePoint Server 2010
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-067](http://go.microsoft.com/fwlink/?linkid=293350)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft SharePoint Server 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
Excel Services  
(2760595)  
(Crítica)  
Servidores de productividad de negocio de Microsoft  
(2553408)  
(Crítica)  
Word Automation Services  
(2760755)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft SharePoint Server 2010 Service Pack 2
</td>
<td style="border:1px solid black;">
Excel Services  
(2760595)  
(Crítica)  
Servidores de productividad de negocio de Microsoft  
(2553408)  
(Crítica)  
Word Automation Services  
(2760755)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Office Web Apps 2010
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-067](http://go.microsoft.com/fwlink/?linkid=293350)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Crítica](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Web Apps 2010 Service Pack 1
</td>
<td style="border:1px solid black;">
Microsoft Excel Web App 2010 Service Pack 1  
(2760594)  
(Crítica)  
Microsoft Word Web App 2010 Service Pack 1  
(2817384)  
(Crítica)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Microsoft Office Web Apps 2010 Service Pack 2
</td>
<td style="border:1px solid black;">
Microsoft Excel Web App 2010 Service Pack 2  
(2760594)  
(Crítica)  
Microsoft Word Web App 2010 Service Pack 2  
(2817384)  
(Crítica)
</td>
</tr>
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft Office Web Apps 2013
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-067](http://go.microsoft.com/fwlink/?linkid=293350)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft Office Web Apps 2013
</td>
<td style="border:1px solid black;">
Microsoft Office Web Apps Server 2013  
(2817305)  
(Importante)
</td>
</tr>
</table>
 
Nota para MS13-067

Vea también las demás categorías de esta sección, Software afectado, para obtener más archivos de actualización con el mismo identificador de boletín. Este boletín abarca varias categorías de software

#### Software de productividad

 
<p> </p>
<table style="border:1px solid black;">
<tr>
<th colspan="2" style="border:1px solid black;">
Microsoft FrontPage 2003
</th>
</tr>
<tr>
<td style="border:1px solid black;">
Identificador del boletín
</td>
<td style="border:1px solid black;">
[MS13-078](http://go.microsoft.com/fwlink/?linkid=318021)
</td>
</tr>
<tr class="alternateRow">
<td style="border:1px solid black;">
Clasificación de gravedad acumulada
</td>
<td style="border:1px solid black;">
[Importante](http://go.microsoft.com/fwlink/?linkid=21140)
</td>
</tr>
<tr>
<td style="border:1px solid black;">
Microsoft FrontPage 2003 Service Pack 3
</td>
<td style="border:1px solid black;">
Microsoft FrontPage 2003 Service Pack 3  
(2825621)  
(Importante)
</td>
</tr>
</table>
 

Herramientas y consejos para la detección e implementación
----------------------------------------------------------

Central de seguridad

Administre el software y las actualizaciones de seguridad que necesite implementar en servidores, equipos de escritorio y equipos móviles en su organización. Para obtener más información visite el [Centro de administración de actualizaciones de TechNet](http://go.microsoft.com/fwlink/?linkid=69903). [TechNet Security TechCenter](http://go.microsoft.com/fwlink/?linkid=21171) proporciona información adicional acerca de la seguridad de los productos de Microsoft. Los usuarios pueden visitar el [Centro de seguridad y protección de Microsoft](http://go.microsoft.com/fwlink/?linkid=85102), donde esta información también está disponible haciendo clic en "Actualizaciones de seguridad".

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

MS13-067

-   Will Dormann, de [CERT/CC](http://www.cert.org/), por informar de la vulnerabilidad de daños en la memoria relacionada con Microsoft Office (CVE-2013-1315)
-   Alexandre Herzog, de [Compass Security AG](http://www.csnc.ch/), por informar de la vulnerabilidad de MAC deshabilitada (CVE-2013-1330)
-   Benjamin Kunz Mejri, de Vulnerability Research Laboratory, por informar de la vulnerabilidad de XSS en SharePoint (CVE-2013-3179)
-   Mateusz Jurczyk, Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de varias vulnerabilidades de daños en la memoria en Microsoft Word (CVE-2013-3847, CVE-2013-3848, CVE-2013-3849, CVE-2013-3857 y CVE-2013-3858)

MS13-068

-   Alexander Klink, de [n.runs AG](https://www.nruns.com/), por informar de la vulnerabilidad de certificado de mensaje (CVE-2013-3870)

MS13-069

-   José Antonio Vázquez González, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3201)
-   José Antonio Vázquez González, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3202)
-   Arthur Gerkis, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3203)
-   Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3204)
-   Peter 'corelanc0d3r' Van Eeckhoutte, de [Corelan](http://www.corelangcv.com/), en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3205)
-   Bo Qu, de [Palo Alto Networks](http://www.paloaltonetworks.com/), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3205)
-   Arthur Gerkis, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3206)
-   Arthur Gerkis, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3207)
-   Arthur Gerkis, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3208)
-   Un investigador anónimo, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3209)
-   José Antonio Vázquez González, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de daños en la memoria de Internet Explorer (CVE-2013-3845)

MS13-070

-   G. Geshev, en colaboración con [Zero Day Initiative](http://www.zerodayinitiative.com/) de [HP](http://www.hpenterprisesecurity.com/products), por informar de la vulnerabilidad de propiedad OLE (CVE-2013-3863)

MS13-071

-   Eduardo Prado, en colaboración con [VeriSign iDefense Labs](http://labs.idefense.com/), por informar de la vulnerabilidad de ejecución remota de código en archivos de tema de Windows (CVE-2013-0810)

MS13-072

-   Timur Yunusov, Alexey Osipov e Ilya Karpov, de [Positive Technologies](http://www.ptsecurity.com/), por informar de la vulnerabilidad de resolución de entidades XML externas (CVE-2013-3160)
-   Mateusz Jurczyk, Ivan Fratric y Ben Hawkes, de [Google Security Team](http://www.google.com/), por informar de varias vulnerabilidades de daños en la memoria en Microsoft Word (CVE-2013-3847, CVE-2013-3848, CVE-2013-3849, CVE-2013-3850, CVE-2013-3851, CVE-2013-3852, CVE-2013-3853, CVE-2013-3854, CVE-2013-3855, CVE-2013-3856, CVE-2013-3857 y CVE-2013-3858)

MS13-073

-   Will Dormann, de [CERT/CC](http://www.cert.org/), por informar de la vulnerabilidad de daños en la memoria relacionada con Microsoft Office (CVE-2013-1315)
-   Will Dormann, de [CERT/CC](http://www.cert.org/), por informar de la vulnerabilidad de daños en la memoria relacionada con Microsoft Office (CVE-2013-3158)
-   Timur Yunusov, Alexey Osipov e Ilya Karpov, de [Positive Technologies](http://www.ptsecurity.com/), por informar de la vulnerabilidad de resolución de entidades XML externas (CVE-2013-3159)

MS13-074

-   Kaveh Ghaemmaghami, de [Secunia SVCRP](http://secunia.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Access (CVE-2013-3155)
-   Kaveh Ghaemmaghami, de [Secunia SVCRP](http://secunia.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con el formato de archivo de Access (CVE-2013-3156)
-   Kaveh Ghaemmaghami, de [Secunia SVCRP](http://secunia.com/), por informar de la vulnerabilidad de daños en la memoria relacionada con Access (CVE-2013-3157)

MS13-075

-   Wei Wang, de [VulnHunt](http://www.vulnhunt.com/), por informar de la vulnerabilidad de IME para chino (CVE-2013-3859)

MS13-076

-   [Gynvael Coldwind](http://gynvael.coldwind.pl/)
-    y 
-   [Mateusz "j00ru" Jurczyk](http://j00ru.vexillium.org/)
-   , de 
-   [Google Inc](http://www.google.com/)
-   , por informar de la vulnerabilidad de varias capturas en Win32k (CVE-2013-1341)
-   [Gynvael Coldwind](http://gynvael.coldwind.pl/)
-    y 
-   [Mateusz "j00ru" Jurczyk](http://j00ru.vexillium.org/)
-   , de 
-   [Google Inc](http://www.google.com/)
-   , por informar de la vulnerabilidad de varias capturas en Win32k (CVE-2013-1342)
-   [Gynvael Coldwind](http://gynvael.coldwind.pl/)
-    y 
-   [Mateusz "j00ru" Jurczyk](http://j00ru.vexillium.org/)
-   , de 
-   [Google Inc](http://www.google.com/)
-   , por informar de la vulnerabilidad de varias capturas en Win32k (CVE-2013-1343)
-   [Mateusz "j00ru" Jurczyk](http://j00ru.vexillium.org/)
-   , de
-   [Google Inc](http://www.google.com/)
-   , por informar de la vulnerabilidad de varias capturas en Win32k (CVE-2013-1344)
-   [Gynvael Coldwind](http://gynvael.coldwind.pl/)
-    y 
-   [Mateusz "j00ru" Jurczyk](http://j00ru.vexillium.org/)
-   , de 
-   [Google Inc](http://www.google.com/)
-   , por informar de la vulnerabilidad de varias capturas en Win32k (CVE-2013-3864)
-   [Gynvael Coldwind](http://gynvael.coldwind.pl/)
-    y 
-   [Mateusz "j00ru" Jurczyk](http://j00ru.vexillium.org/)
-   , de 
-   [Google Inc](http://www.google.com/)
-   , por informar de la vulnerabilidad de varias capturas en Win32k (CVE-2013-3865)
-   Guo Pengfei, de [Qihoo 360 Security Center](http://www.360.cn/), por informar de la vulnerabilidad de elevación de privilegios en Win32k (CVE-2013-3866)

MS13-078

-   Timur Yunusov, de [Positive Technologies](http://www.ptsecurity.com/), por informar de la vulnerabilidad de divulgación de XML (CVE-2013-3137)

#### Soporte técnico

-   El software afectado que se enumera se ha probado para determinar las versiones que están afectadas. Otras versiones han pasado su ciclo de vida de soporte técnico. Para determinar el ciclo de vida del soporte técnico de su versión de software, visite [Ciclo de vida del soporte técnico de Microsoft](http://go.microsoft.com/fwlink/?linkid=21742).
-   Soluciones de seguridad para profesionales de TI: [Soporte técnico y solución de problemas de seguridad de TechNet](http://technet.microsoft.com/es-es/security/bb980617.aspx)
-   Ayuda para proteger su equipo con Windows de virus y malware: [Solución antivirus y centro de seguridad](http://support.microsoft.com/contactus/cu_sc_virsec_master)
-   Soporte local según su país: [Soporte internacional](http://support.microsoft.com/common/international.aspx)

#### Renuncia

La información proporcionada en Microsoft Knowledge Base se suministra "tal cual", sin garantías de ningún tipo. Microsoft renuncia al otorgamiento de toda garantía, tanto expresa como implícita, incluidas las garantías de comerciabilidad e idoneidad para un determinado fin. Ni Microsoft Corporation ni sus proveedores se responsabilizarán en ningún caso de daños directos, indirectos, incidentales, consecuenciales, pérdida de beneficios o daños especiales, aun en el supuesto de que se hubiera informado a Microsoft Corporation o a sus proveedores de la posibilidad de dichos daños. Algunos estados de Estados Unidos no permiten la exclusión o limitación de responsabilidad por daños consecuenciales o incidentales, y, por tanto, la limitación anterior puede no ser aplicable en su caso.

#### Revisiones

-   V1.0 (10 de septiembre de 2013): Publicación del resumen del boletín.
-   V1.1 (6 de noviembre de 2013): para MS13-067, se ha corregido el nombre de producto de la actualización de Microsoft Office Web Apps Server 2013 (2817305).

*Built at 2014-04-18T01:50:00Z-07:00*
